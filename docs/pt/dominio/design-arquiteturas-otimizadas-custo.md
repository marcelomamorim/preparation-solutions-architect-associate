# Dominio 4 - Design de Arquiteturas Otimizadas por Custo (20% do Exame)

> Este dominio avalia sua capacidade de projetar solucoes que minimizem custos sem comprometer desempenho ou confiabilidade. Foque em entender modelos de precificacao, right-sizing e estrategias de otimizacao.

---

## Tarefa 4.1: Projetar solucoes de armazenamento otimizadas por custo

### Conhecimentos Necessarios

- **Classes de armazenamento do S3**
  Escolha a classe correta baseado na frequencia de acesso:
  - **S3 Standard** - Acesso frequente, alta disponibilidade
  - **S3 Intelligent-Tiering** - Movimentacao automatica entre tiers (ideal quando o padrao de acesso e desconhecido)
  - **S3 Standard-IA** - Acesso pouco frequente, mas necessita de acesso rapido quando solicitado
  - **S3 One Zone-IA** - Menor custo, mas sem resiliencia multi-AZ
  - **S3 Glacier Instant Retrieval** - Arquivamento com acesso em milissegundos
  - **S3 Glacier Flexible Retrieval** - Arquivamento com retrieval em minutos a horas
  - **S3 Glacier Deep Archive** - Menor custo, retrieval em ate 12 horas

- **Gerenciamento de custos da AWS**
  - [AWS Cost Explorer](https://aws.amazon.com/aws-cost-management/aws-cost-explorer/) - Visualize e analise gastos
  - [AWS Budgets](https://aws.amazon.com/aws-cost-management/aws-budgets/) - Configure alertas de gastos
  - [AWS Cost and Usage Report](https://aws.amazon.com/aws-cost-management/aws-cost-and-usage-reporting/) - Relatorio detalhado de custos
  - **Tags de alocacao de custos** - Rastreie custos por projeto, equipe ou ambiente

- **Ciclos de vida e estrategias de backup**
  Use S3 Lifecycle Policies para mover objetos automaticamente entre classes de armazenamento. Configure regras para excluir versoes antigas apos um periodo definido.

- **Armazenamento hibrido**
  - [AWS DataSync](https://aws.amazon.com/datasync/) - Transferencia rapida de dados
  - [AWS Transfer Family](https://aws.amazon.com/aws-transfer-family/) - SFTP/FTP gerenciado
  - [AWS Storage Gateway](https://aws.amazon.com/storagegateway/) - Integracao on-premises com S3

- **Tipos de volume EBS**
  - **gp3** - SSD de uso geral, custo-beneficio (padrao recomendado)
  - **gp2** - SSD de uso geral (mais antigo, IOPS vinculados ao tamanho)
  - **io2/io2 Block Express** - SSD de alto desempenho (IOPS provisionados)
  - **st1** - HDD otimizado para throughput (big data, logs)
  - **sc1** - HDD frio, menor custo (acesso pouco frequente)

### Habilidades Necessarias

- Projetar estrategias de armazenamento otimizadas por custo
- Determinar o tamanho correto de armazenamento para cada workload
- Gerenciar ciclos de vida de objetos S3 com transicoes automaticas
- Selecionar solucoes de backup e arquivamento econômicas

> **Dica para o exame**: S3 Intelligent-Tiering e ideal quando voce nao sabe o padrao de acesso dos dados. Para dados que precisam ser retidos por anos (compliance), use S3 Glacier Deep Archive com Object Lock. S3 Lifecycle Policies sao essenciais para automacao de custos.

---

## Tarefa 4.2: Projetar solucoes de computacao otimizadas por custo

### Conhecimentos Necessarios

- **Opcoes de compra do EC2**
  - **On-Demand** - Pague por segundo/hora, sem compromisso
  - **Reserved Instances (RI)** - Ate 72% de desconto com compromisso de 1 ou 3 anos
  - **Savings Plans** - Desconto similar a RI, mais flexivel (Compute ou EC2 Instance)
  - **Spot Instances** - Ate 90% de desconto, pode ser interrompida pela AWS a qualquer momento
  - **Dedicated Hosts** - Servidor fisico dedicado, para conformidade e licenciamento

- **Quando usar Spot Instances**
  Ideal para workloads tolerantes a interrupcoes: processamento em lote, CI/CD, treinamento de ML, big data (EMR). Nao use para bancos de dados ou aplicacoes criticas.

- **Tipos e familias de instancias EC2**
  - **M** (General Purpose) - Uso geral, equilibrio computacao/memoria
  - **C** (Compute Optimized) - Processamento intensivo, HPC
  - **R** (Memory Optimized) - Bancos de dados in-memory, cache
  - **T** (Burstable) - Workloads com picos esporadicos
  - **G/P** (Accelerated Computing) - Machine Learning, GPU

- **Computacao serverless vs. containers vs. EC2**
  - **Lambda** - Eventos esporadicos, funcoes curtas (< 15 min), escala a zero
  - **Fargate** - Containers sem gerenciar servidores, pague por vCPU e memoria usada
  - **EC2** - Controle total, ideal para workloads consistentes de longa duracao

### Habilidades Necessarias

- Selecionar o modelo de compra adequado (On-Demand, RI, Savings Plans, Spot)
- Determinar a familia e tamanho de instancia corretos (right-sizing)
- Escolher entre Lambda, Fargate e EC2 com base no custo
- Configurar Auto Scaling para otimizar custos (escalar para baixo quando possivel)

> **Dica para o exame**: Para workloads estaveis e previsiveis, use Reserved Instances ou Savings Plans. Para workloads variaveis e tolerantes a falhas, use Spot Instances. Para workloads com baixo uso, considere Lambda para escalar a zero e nao pagar quando ocioso.

---

## Tarefa 4.3: Projetar solucoes de banco de dados otimizadas por custo

### Conhecimentos Necessarios

- **Servicos de banco de dados e seus custos**
  - [Amazon Aurora Serverless](https://aws.amazon.com/rds/aurora/) - Escala automaticamente, pague por ACUs usadas (ideal para workloads imprevisiveis)
  - [Amazon DynamoDB](https://aws.amazon.com/dynamodb/) - Modo On-Demand (pague por requisicao) ou Provisioned (com auto-scaling)
  - [Amazon RDS](https://aws.amazon.com/rds/) - Reserved Instances disponíveis para economia de ate 69%

- **Estrategias de cache para reducao de custos**
  [Amazon ElastiCache](https://aws.amazon.com/elasticache/) reduz custos ao diminuir a carga de leitura no banco de dados principal. Menos leituras = menos IOPS = instancia menor necessaria.

- **Politicas de retencao de dados**
  Configure periodos de retencao de backups automaticos no RDS. Use snapshots manuais para retencoes mais longas. Considere mover dados historicos para S3 com Athena para queries.

- **Migracoes de banco de dados**
  O [AWS DMS](https://aws.amazon.com/dms/) permite migrar de bancos comerciais caros (Oracle, SQL Server) para open source (PostgreSQL, MySQL) ou servicos AWS nativos (Aurora, DynamoDB), reduzindo custos de licenciamento.

### Habilidades Necessarias

- Projetar politicas de backup e retencao adequadas
- Escolher o motor de banco de dados mais economico
- Decidir entre DynamoDB On-Demand vs. Provisioned
- Migrar de bancos comerciais para open source para reduzir custos

> **Dica para o exame**: Aurora Serverless v2 e ideal para workloads imprevisiveis (dev/test, aplicacoes com picos). DynamoDB On-Demand e melhor quando o trafego e imprevisivel; Provisioned com auto-scaling e mais economico para trafego previsivel.

---

## Tarefa 4.4: Projetar arquiteturas de rede otimizadas por custo

### Conhecimentos Necessarios

- **Custos de transferencia de dados**
  - Dados de entrada (ingress) sao gratuitos
  - Dados de saida (egress) sao cobrados
  - Transferencia entre AZs tem custo (use endpoints VPC para reduzir)
  - Transferencia entre Regioes tem custo maior

- **NAT Gateway vs. NAT Instance**
  NAT Gateway e gerenciado pela AWS, mais confiavel, mas custa ~$0.045/hora + dados processados. NAT Instance (EC2) pode ser mais barato para baixo trafego, mas requer gerenciamento.

- **Conectividade de rede**
  - **VPN** - Mais barato, mais rapido de configurar, usa internet
  - **Direct Connect** - Mais caro, mas custo previsivel para alto volume de dados
  - **VPC Peering** - Gratuito para transferencia de dados na mesma AZ
  - **Transit Gateway** - Simplifica redes complexas, mas tem custo por GB

- **Otimizacao com CDN e cache**
  Use [Amazon CloudFront](https://aws.amazon.com/cloudfront/) para cachear conteudo na borda. Reduz custos de transferencia de dados da origem e melhora a experiencia do usuario.

### Habilidades Necessarias

- Configurar NAT Gateways otimizados (compartilhado vs. por AZ)
- Escolher entre Direct Connect e VPN baseado em custo
- Minimizar custos de transferencia de dados (usar VPC Endpoints, CloudFront)
- Usar Transit Gateway vs. VPC Peering baseado na complexidade

> **Dica para o exame**: VPC Endpoints (Gateway para S3 e DynamoDB, Interface para outros servicos) eliminam custos de NAT Gateway para trafego AWS. CloudFront reduz custos de egress do S3. Use S3 Transfer Acceleration para uploads rapidos de clientes distantes.

---

## Servicos-Chave para o Dominio 4

| Servico | Funcao na Otimizacao de Custos |
|---------|-------------------------------|
| AWS Cost Explorer | Analise de gastos e tendencias |
| AWS Budgets | Alertas de orcamento |
| AWS Compute Optimizer | Recomendacoes de right-sizing |
| AWS Trusted Advisor | Recomendacoes de otimizacao |
| S3 Intelligent-Tiering | Otimizacao automatica de armazenamento |
| EC2 Spot Instances | Ate 90% de desconto em computacao |
| Savings Plans | Descontos por compromisso de uso |
| Aurora Serverless | Banco de dados que escala a zero |
| VPC Endpoints | Elimina custos de NAT para servicos AWS |
| Amazon CloudFront | Reduz custos de transferencia de dados |

---

Este guia abrange as principais areas do Dominio 4. A otimizacao de custos e um dos pilares do Well-Architected Framework. Lembre-se: o objetivo nao e gastar menos, mas **gastar de forma inteligente** para maximizar o valor entregue.
