# Domínio 4 - Design de Arquiteturas Otimizadas por Custo (20% do Exame)

> Este domínio avalia sua capacidade de projetar soluções que minimizem custos sem comprometer desempenho ou confiabilidade. Foque em entender modelos de precificacao, right-sizing e estratégias de otimização.

---

## Tarefa 4.1: Projetar soluções de armazenamento otimizadas por custo

### Conhecimentos Necessários

- **Classes de armazenamento do S3**
  Escolha a classe correta baseado na frequência de acesso:
  - **S3 Standard** - Acesso frequente, alta disponibilidade
  - **S3 Intelligent-Tiering** - Movimentacao automática entre tiers (ideal quando o padrão de acesso e desconhecido)
  - **S3 Standard-IA** - Acesso pouco frequente, mas necessita de acesso rápido quando solicitado
  - **S3 One Zone-IA** - Menor custo, mas sem resiliência multi-AZ
  - **S3 Glacier Instant Retrieval** - Arquivamento com acesso em milissegundos
  - **S3 Glacier Flexible Retrieval** - Arquivamento com retrieval em minutos a horas
  - **S3 Glacier Deep Archive** - Menor custo, retrieval em até 12 horas

- **Gerenciamento de custos da AWS**
  - [AWS Cost Explorer](https://aws.amazon.com/aws-cost-management/aws-cost-explorer/) - Visualize e análise gastos
  - [AWS Budgets](https://aws.amazon.com/aws-cost-management/aws-budgets/) - Configure alertas de gastos
  - [AWS Cost and Usage Report](https://aws.amazon.com/aws-cost-management/aws-cost-and-usage-reporting/) - Relatorio detalhado de custos
  - **Tags de alocação de custos** - Rastreie custos por projeto, equipe ou ambiente

- **Ciclos de vida e estratégias de backup**
  Use S3 Lifecycle Policies para mover objetos automaticamente entre classes de armazenamento. Configure regras para excluir versoes antigas apos um periodo definido.

- **Armazenamento híbrido**
  - [AWS DataSync](https://aws.amazon.com/datasync/) - Transferencia rápida de dados
  - [AWS Transfer Family](https://aws.amazon.com/aws-transfer-family/) - SFTP/FTP gerenciado
  - [AWS Storage Gatéway](https://aws.amazon.com/storagegateway/) - Integracao on-premises com S3

- **Tipos de volume EBS**
  - **gp3** - SSD de uso geral, custo-benefício (padrão recomendado)
  - **gp2** - SSD de uso geral (mais antigo, IOPS vinculados ao tamanho)
  - **io2/io2 Block Express** - SSD de alto desempenho (IOPS provisionados)
  - **st1** - HDD otimizado para throughput (big data, logs)
  - **sc1** - HDD frio, menor custo (acesso pouco frequente)

### Habilidades Necessárias

- Projetar estratégias de armazenamento otimizadas por custo
- Determinar o tamanho correto de armazenamento para cada workload
- Gerenciar ciclos de vida de objetos S3 com transicoes automáticas
- Selecionar soluções de backup e arquivamento econômicas

> **Dica para o exame**: S3 Intelligent-Tiering e ideal quando você não sabe o padrão de acesso dos dados. Para dados que precisam ser retidos por anos (compliance), use S3 Glacier Deep Archive com Object Lock. S3 Lifecycle Policies são essenciais para automação de custos.

---

## Tarefa 4.2: Projetar soluções de computação otimizadas por custo

### Conhecimentos Necessários

- **Opcoes de compra do EC2**
  - **On-Demand** - Pague por segundo/hora, sem compromisso
  - **Reserved Instances (RI)** - Até 72% de desconto com compromisso de 1 ou 3 anos
  - **Savings Plans** - Desconto similar a RI, mais flexível (Compute ou EC2 Instance)
  - **Spot Instances** - Até 90% de desconto, pode ser interrompida pela AWS a qualquer momento
  - **Dedicatéd Hosts** - Servidor físico dedicado, para conformidade e licenciamento

- **Quando usar Spot Instances**
  Ideal para workloads tolerantes a interrupções: processamento em lote, CI/CD, treinamento de ML, big data (EMR). Não use para bancos de dados ou aplicações críticas.

- **Tipos e famílias de instâncias EC2**
  - **M** (General Purpose) - Uso geral, equilíbrio computação/memória
  - **C** (Compute Optimized) - Processamento intensivo, HPC
  - **R** (Memory Optimized) - Bancos de dados in-memory, cache
  - **T** (Burstable) - Workloads com picos esporadicos
  - **G/P** (Acceleratéd Computing) - Machine Learning, GPU

- **Computacao serverless vs. containers vs. EC2**
  - **Lambda** - Eventos esporadicos, funções curtas (< 15 min), escala a zero
  - **Fargaté** - Containers sem gerenciar servidores, pague por vCPU e memória usada
  - **EC2** - Controle total, ideal para workloads consistentes de longa duracao

### Habilidades Necessárias

- Selecionar o modelo de compra adequado (On-Demand, RI, Savings Plans, Spot)
- Determinar a familia e tamanho de instância corretos (right-sizing)
- Escolher entre Lambda, Fargaté e EC2 com base no custo
- Configurar Auto Scaling para otimizar custos (escalar para baixo quando possível)

> **Dica para o exame**: Para workloads estaveis e previsiveis, use Reserved Instances ou Savings Plans. Para workloads variaveis e tolerantes a falhas, use Spot Instances. Para workloads com baixo uso, considere Lambda para escalar a zero e não pagar quando ocioso.

---

## Tarefa 4.3: Projetar soluções de banco de dados otimizadas por custo

### Conhecimentos Necessários

- **Serviços de banco de dados e seus custos**
  - [Amazon Aurora Serverless](https://aws.amazon.com/rds/aurora/) - Escala automaticamente, pague por ACUs usadas (ideal para workloads imprevisíveis)
  - [Amazon DynamoDB](https://aws.amazon.com/dynamodb/) - Modo On-Demand (pague por requisicao) ou Provisioned (com auto-scaling)
  - [Amazon RDS](https://aws.amazon.com/rds/) - Reserved Instances disponíveis para economia de até 69%

- **Estratégias de cache para reducao de custos**
  [Amazon ElastiCache](https://aws.amazon.com/elásticache/) reduz custos ao diminuir a carga de leitura no banco de dados principal. Menos leituras = menos IOPS = instância menor necessária.

- **Politicas de retenção de dados**
  Configure periodos de retenção de backups automáticos no RDS. Use snapshots manuais para retencoes mais longas. Considere mover dados históricos para S3 com Athena para queries.

- **Migracoes de banco de dados**
  O [AWS DMS](https://aws.amazon.com/dms/) permite migrar de bancos comerciais caros (Oracle, SQL Server) para open source (PostgreSQL, MySQL) ou serviços AWS nativos (Aurora, DynamoDB), reduzindo custos de licenciamento.

### Habilidades Necessárias

- Projetar políticas de backup e retenção adequadas
- Escolher o motor de banco de dados mais econômico
- Decidir entre DynamoDB On-Demand vs. Provisioned
- Migrar de bancos comerciais para open source para reduzir custos

> **Dica para o exame**: Aurora Serverless v2 e ideal para workloads imprevisíveis (dev/test, aplicações com picos). DynamoDB On-Demand e melhor quando o tráfego e imprevisível; Provisioned com auto-scaling e mais econômico para tráfego previsível.

---

## Tarefa 4.4: Projetar arquiteturas de rede otimizadas por custo

### Conhecimentos Necessários

- **Custos de transferencia de dados**
  - Dados de entrada (ingress) são gratuitos
  - Dados de saida (egress) são cobrados
  - Transferencia entre AZs tem custo (use endpoints VPC para reduzir)
  - Transferencia entre Regioes tem custo maior

- **NAT Gatéway vs. NAT Instance**
  NAT Gatéway e gerenciado pela AWS, mais confiável, mas custa ~$0.045/hora + dados processados. NAT Instance (EC2) pode ser mais barato para baixo tráfego, mas requer gerenciamento.

- **Conectividade de rede**
  - **VPN** - Mais barato, mais rápido de configurar, usa internet
  - **Direct Connect** - Mais caro, mas custo previsível para alto volume de dados
  - **VPC Peering** - Gratuito para transferencia de dados na mesma AZ
  - **Transit Gatéway** - Simplifica redes complexas, mas tem custo por GB

- **Otimização com CDN e cache**
  Use [Amazon CloudFront](https://aws.amazon.com/cloudfront/) para cachear conteúdo na borda. Reduz custos de transferencia de dados da origem e melhora a experiência do usuário.

### Habilidades Necessárias

- Configurar NAT Gatéways otimizados (compartilhado vs. por AZ)
- Escolher entre Direct Connect e VPN baseado em custo
- Minimizar custos de transferencia de dados (usar VPC Endpoints, CloudFront)
- Usar Transit Gatéway vs. VPC Peering baseado na complexidade

> **Dica para o exame**: VPC Endpoints (Gatéway para S3 e DynamoDB, Interface para outros serviços) eliminam custos de NAT Gatéway para tráfego AWS. CloudFront reduz custos de egress do S3. Use S3 Transfer Acceleration para uploads rápidos de clientes distantes.

---

## Serviços-Chave para o Domínio 4

| Serviço | Função na Otimização de Custos |
|---------|-------------------------------|
| AWS Cost Explorer | Análise de gastos e tendencias |
| AWS Budgets | Alertas de orçamento |
| AWS Compute Optimizer | Recomendacoes de right-sizing |
| AWS Trusted Advisor | Recomendacoes de otimização |
| S3 Intelligent-Tiering | Otimização automática de armazenamento |
| EC2 Spot Instances | Até 90% de desconto em computação |
| Savings Plans | Descontos por compromisso de uso |
| Aurora Serverless | Banco de dados que escala a zero |
| VPC Endpoints | Elimina custos de NAT para serviços AWS |
| Amazon CloudFront | Reduz custos de transferencia de dados |

---

Este guia abrange as principais áreas do Domínio 4. A otimização de custos é um dos pilares do Well-Architected Framework. Lembre-se: o objetivo não e gastar menos, mas **gastar de forma inteligente** para maximizar o valor entregue.
