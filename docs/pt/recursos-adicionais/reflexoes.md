# Reflexoes e Boas Praticas de Arquitetura AWS

> Insights e padroes de arquitetura do mundo real que vao alem do conteudo do exame. Entender esses conceitos ajuda a responder questoes de cenario com mais confianca.

---

## Os 6 Pilares do AWS Well-Architected Framework

O Well-Architected Framework e a base filosofica de muitas questoes do exame. Entenda cada pilar:

### 1. Excelencia Operacional
- Automatize tudo que puder (CloudFormation, Systems Manager)
- Faca mudancas pequenas e frequentes, nao grandes e arriscadas
- Antecipe falhas e pratique a resposta a incidentes
- **Servicos-chave**: CloudFormation, CloudWatch, Systems Manager, Config

### 2. Seguranca
- Aplique seguranca em todas as camadas (defense in depth)
- Rastreie tudo com logs e auditoria (CloudTrail, VPC Flow Logs)
- Automatize as melhores praticas de seguranca
- Proteja dados em repouso e em transito
- **Servicos-chave**: IAM, KMS, WAF, Shield, GuardDuty, Security Hub

### 3. Confiabilidade
- Teste procedimentos de recuperacao regularmente
- Escale horizontalmente para aumentar a disponibilidade
- Pare de adivinhar capacidade (use Auto Scaling)
- Gerencie mudancas com automacao
- **Servicos-chave**: Route 53, ELB, Auto Scaling, CloudWatch, Backup

### 4. Eficiencia de Performance
- Use tecnologias serverless e gerenciadas
- Experimente mais facilmente na nuvem
- Considere "mechanical sympathy" (use a tecnologia certa para o problema)
- **Servicos-chave**: Lambda, ECS, CloudFront, ElastiCache, Aurora

### 5. Otimizacao de Custos
- Adote um modelo de consumo (pague apenas pelo que usa)
- Meca a eficiencia geral
- Pare de gastar dinheiro com trabalho pesado indiferenciado
- Analise e atribua custos
- **Servicos-chave**: Cost Explorer, Budgets, Trusted Advisor, Compute Optimizer

### 6. Sustentabilidade
- Entenda seu impacto ambiental
- Estabeleca metas de sustentabilidade
- Maximize a utilizacao de recursos
- Use servicos gerenciados para reduzir o impacto
- **Servicos-chave**: EC2 Auto Scaling, Graviton, Lambda, S3 Intelligent-Tiering

---

## Padroes de Arquitetura Comuns no Exame

### Padrao 1: Aplicacao Web de 3 Camadas
```
Internet → CloudFront → ALB → EC2 (Auto Scaling) → RDS (Multi-AZ)
                                    ↓
                              ElastiCache (Redis)
```
- **Quando usar**: Aplicacoes web tradicionais com necessidade de sessoes, cache e banco relacional
- **Pontos-chave**: ALB para roteamento HTTP, Auto Scaling para elasticidade, RDS Multi-AZ para alta disponibilidade

### Padrao 2: Arquitetura Serverless
```
API Gateway → Lambda → DynamoDB
                ↓
              S3 (arquivos estaticos)
```
- **Quando usar**: APIs e microservicos com trafego variavel, quando se quer zero gerenciamento de servidores
- **Pontos-chave**: Lambda escala automaticamente, DynamoDB On-Demand para trafego imprevisivel

### Padrao 3: Processamento Assincrono
```
Produtor → SQS (fila) → Consumidor (EC2/Lambda)
              ↓
         Dead Letter Queue (DLQ)
```
- **Quando usar**: Desacoplar componentes, absorver picos de trafego, processar tarefas em background
- **Pontos-chave**: SQS FIFO para ordem garantida, DLQ para mensagens com falha

### Padrao 4: Data Lake
```
Fontes de Dados → Kinesis/DataSync → S3 (Raw)
                                       ↓
                                   Glue (ETL)
                                       ↓
                                   S3 (Processed)
                                       ↓
                                   Athena / QuickSight
```
- **Quando usar**: Analise de grandes volumes de dados de multiplas fontes
- **Pontos-chave**: S3 como armazenamento central, Glue para catalogo e ETL, Athena para queries SQL

### Padrao 5: Arquitetura Hibrida
```
On-Premises ←→ Direct Connect ←→ AWS VPC
                                    ↓
                              Transit Gateway
                                    ↓
                            Multiplas VPCs
```
- **Quando usar**: Migracoes graduais, requisitos de conformidade, workloads que precisam ficar on-premises
- **Pontos-chave**: Direct Connect para latencia consistente, VPN como backup, Transit Gateway para simplificar

---

## Erros Comuns a Evitar

1. **Nao usar Multi-AZ quando a questao pede alta disponibilidade**: Sempre distribua em pelo menos 2 AZs
2. **Confundir Security Groups com NACLs**: SGs sao stateful (nivel de instancia), NACLs sao stateless (nivel de sub-rede)
3. **Escolher a opcao mais complexa**: Na AWS, prefira servicos gerenciados e serverless quando possivel
4. **Ignorar custos de transferencia de dados**: Dados entre AZs e entre Regioes tem custo
5. **Nao considerar limites de servico**: Lambda tem 15 min de timeout, SQS tem 14 dias de retencao maxima
6. **Confundir Kinesis Data Streams com Firehose**: Streams e para processamento custom, Firehose e para entrega automatica

---

## Analogias Uteis

| Conceito AWS | Analogia |
|-------------|---------|
| Regioes e AZs | Cidades e bairros |
| Security Groups | Porteiro do predio (checa quem entra, lembra quem saiu) |
| NACLs | Guarita do condominio (checa entrada E saida) |
| SQS | Fila do banco (primeiro a chegar, primeiro a ser atendido) |
| SNS | Lista de transmissao do WhatsApp (uma mensagem para muitos) |
| CloudFront | Filial de uma loja (produto mais perto do cliente) |
| Auto Scaling | Contratacao temporaria (mais funcionarios no Natal) |
| Lambda | Uber (paga apenas pela corrida, sem custo de carro parado) |

---

Voltar ao [Indice](../../../index.md)
