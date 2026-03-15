# Reflexões e Boas Práticas de Arquitetura AWS

> Insights e padrões de arquitetura do mundo real que vao além do conteúdo do exame. Entender esses conceitos ajuda a responder questões de cenário com mais confianca.

---

## Os 6 Pilares do AWS Well-Architected Framework

O Well-Architected Framework e a base filosofica de muitas questões do exame. Entenda cada pilar:

### 1. Excelencia Operacional
- Automatize tudo que puder (CloudFormation, Systems Manager)
- Faca mudancas pequenas e frequentes, não grandes e arriscadas
- Antecipe falhas e pratique a resposta a incidentes
- **Serviços-chave**: CloudFormation, CloudWatch, Systems Manager, Config

### 2. Segurança
- Aplique segurança em todas as camadas (defense in depth)
- Rastreie tudo com logs e auditoria (CloudTrail, VPC Flow Logs)
- Automatize as melhores práticas de segurança
- Proteja dados em repouso e em trânsito
- **Serviços-chave**: IAM, KMS, WAF, Shield, GuardDuty, Security Hub

### 3. Confiabilidade
- Teste procedimentos de recuperação regularmente
- Escale horizontalmente para aumentar a disponibilidade
- Pare de adivinhar capacidade (use Auto Scaling)
- Gerencie mudancas com automação
- **Serviços-chave**: Route 53, ELB, Auto Scaling, CloudWatch, Backup

### 4. Eficiência de Performance
- Use tecnologias serverless e gerenciadas
- Experimente mais fácilmente na nuvem
- Considere "mechanical sympathy" (use a tecnologia certa para o problema)
- **Serviços-chave**: Lambda, ECS, CloudFront, ElastiCache, Aurora

### 5. Otimização de Custos
- Adote um modelo de consumo (pague apenas pelo que usa)
- Meca a eficiência geral
- Pare de gastar dinheiro com trabalho pesado indiferenciado
- Análise e atribua custos
- **Serviços-chave**: Cost Explorer, Budgets, Trusted Advisor, Compute Optimizer

### 6. Sustentabilidade
- Entenda seu impacto ambiental
- Estabeleca metas de sustentabilidade
- Maximize a utilização de recursos
- Use serviços gerenciados para reduzir o impacto
- **Serviços-chave**: EC2 Auto Scaling, Graviton, Lambda, S3 Intelligent-Tiering

---

## Padrões de Arquitetura Comuns no Exame

### Padrão 1: Aplicação Web de 3 Camadas
```
Internet → CloudFront → ALB → EC2 (Auto Scaling) → RDS (Multi-AZ)
                                    ↓
                              ElastiCache (Redis)
```
- **Quando usar**: Aplicacoes web tradicionais com necessidade de sessoes, cache e banco relacional
- **Pontos-chave**: ALB para roteamento HTTP, Auto Scaling para elasticidade, RDS Multi-AZ para alta disponibilidade

### Padrão 2: Arquitetura Serverless
```
API Gatéway → Lambda → DynamoDB
                ↓
              S3 (arquivos estáticos)
```
- **Quando usar**: APIs e microserviços com tráfego variável, quando se quer zero gerenciamento de servidores
- **Pontos-chave**: Lambda escala automáticamente, DynamoDB On-Demand para tráfego imprevisível

### Padrão 3: Processamento Assincrono
```
Produtor → SQS (fila) → Consumidor (EC2/Lambda)
              ↓
         Dead Letter Queue (DLQ)
```
- **Quando usar**: Desacoplar componentes, absorver picos de tráfego, processar tarefas em background
- **Pontos-chave**: SQS FIFO para ordem garantida, DLQ para mensagens com falha

### Padrão 4: Data Lake
```
Fontes de Dados → Kinesis/DataSync → S3 (Raw)
                                       ↓
                                   Glue (ETL)
                                       ↓
                                   S3 (Processed)
                                       ↓
                                   Athena / QuickSight
```
- **Quando usar**: Análise de grandes volumes de dados de múltiplas fontes
- **Pontos-chave**: S3 como armazenamento central, Glue para catalogo e ETL, Athena para queries SQL

### Padrão 5: Arquitetura Hibrida
```
On-Premises ←→ Direct Connect ←→ AWS VPC
                                    ↓
                              Transit Gatéway
                                    ↓
                            Multiplas VPCs
```
- **Quando usar**: Migracoes graduais, requisitos de conformidade, workloads que precisam ficar on-premises
- **Pontos-chave**: Direct Connect para latência consistente, VPN como backup, Transit Gatéway para simplificar

---

## Erros Comuns a Evitar

1. **Não usar Multi-AZ quando a questao pede alta disponibilidade**: Sempre distribua em pelo menos 2 AZs
2. **Confundir Security Groups com NACLs**: SGs sao statéful (nivel de instância), NACLs sao statéless (nivel de sub-rede)
3. **Escolher a opcao mais complexa**: Na AWS, prefira serviços gerenciados e serverless quando possível
4. **Ignorar custos de transferencia de dados**: Dados entre AZs e entre Regioes tem custo
5. **Não considerar limites de serviço**: Lambda tem 15 min de timeout, SQS tem 14 dias de retenção máxima
6. **Confundir Kinesis Data Streams com Firehose**: Streams e para processamento custom, Firehose e para entrega automática

---

## Analogias Uteis

| Conceito AWS | Analogia |
|-------------|---------|
| Regioes e AZs | Cidades e bairros |
| Security Groups | Porteiro do predio (checa quem entra, lembra quem saiu) |
| NACLs | Guarita do condomínio (checa entrada E saida) |
| SQS | Fila do banco (primeiro a chegar, primeiro a ser aténdido) |
| SNS | Lista de transmissao do WhatsApp (uma mensagem para muitos) |
| CloudFront | Filial de uma loja (produto mais perto do cliente) |
| Auto Scaling | Contratacao temporaria (mais funcionarios no Natal) |
| Lambda | Uber (paga apenas pela corrida, sem custo de carro parado) |

---

Voltar ao [Índice](../../../index.md)
