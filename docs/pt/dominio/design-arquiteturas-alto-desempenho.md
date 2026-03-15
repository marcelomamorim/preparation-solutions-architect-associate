# Domínio 3 - Design de Arquiteturas de Alto Desempenho (24% do Exame)

> Este domínio avalia sua capacidade de selecionar soluções de armazenamento, computacao, banco de dados e rede que aténdam aos requisitos de performance. Foque em entender quando usar cada tipo de serviço e como escalar.

---

## Tarefa 3.1: Determinar soluções de armazenamento de alto desempenho e/ou escaláveis

### Conhecimentos Necessários

- **Solucoes de armazenamento híbrido**
  O [AWS Storage Gatéway](https://aws.amazon.com/storagegateway/) conecta ambientes on-premises ao armazenamento AWS. Tipos: File Gatéway (NFS/SMB para S3), Volume Gatéway (iSCSI para EBS snapshots) e Tape Gatéway (backup em fita virtual).

- **Serviços de armazenamento e seus casos de uso**
  - [Amazon S3](https://aws.amazon.com/s3/) - Armazenamento de objetos ilimitado, ideal para dados não estruturados, backups, data lakes
  - [Amazon EFS](https://aws.amazon.com/efs/) - Sistema de arquivos NFS elástico, compartilhado entre múltiplas instâncias EC2
  - [Amazon EBS](https://aws.amazon.com/ebs/) - Armazenamento de blocos persistente para EC2, ideal para bancos de dados e aplicações
  - [Amazon FSx](https://aws.amazon.com/fsx/) - Sistemas de arquivos gerenciados (Windows File Server, Lustre, NetApp ONTAP)

- **Tipos de armazenamento**
  - **Objeto** (S3) - Dados não estruturados, acesso via HTTP, altamente duravel (99.999999999%)
  - **Arquivo** (EFS, FSx) - Acesso compartilhado via NFS/SMB, hierarquia de diretórios
  - **Bloco** (EBS) - Baixa latência, alto IOPS, ideal para bancos de dados

### Habilidades Necessárias

- Selecionar serviços de armazenamento baseados em requisitos de desempenho (IOPS, throughput, latência)
- Escolher serviços que escalam automáticamente (S3 e EFS escalam sem intervencao)
- Entender classes de armazenamento do S3 e quando usar cada uma

> **Dica para o exame**: Para alto IOPS, use EBS io2 Block Express (até 256,000 IOPS). Para throughput alto com compartilhamento, use EFS ou FSx for Lustre. S3 escala automáticamente sem limites práticos de throughput.

---

## Tarefa 3.2: Projetar soluções de computacao elasticas e de alto desempenho

### Conhecimentos Necessários

- **Serviços de computacao da AWS**
  - [AWS Batch](https://aws.amazon.com/batch/) - Processamento em lote em escala
  - [Amazon EMR](https://aws.amazon.com/emr/) - Big data com Hadoop, Spark, Hive
  - [AWS Fargaté](https://aws.amazon.com/fargate/) - Containers serverless
  - [AWS Lambda](https://aws.amazon.com/lambda/) - Funcoes serverless (até 15 min, 10 GB de memoria)

- **Computacao distribuida e serviços de borda**
  [Amazon CloudFront](https://aws.amazon.com/cloudfront/) executa lógica na borda com Lambda@Edge e CloudFront Functions. O [AWS Global Accelerator](https://aws.amazon.com/global-accelerator/) roteia tráfego pela rede AWS para menor latência.

- **Escalabilidade**
  - [Amazon EC2 Auto Scaling](https://aws.amazon.com/autoscaling/) - Ajusta a quantidade de instâncias EC2
  - Politicas de escalabilidade: Target Tracking, Step Scaling, Simple Scaling, Scheduled
  - Metricas comuns: CPU, requisicoes por target, métricas customizadas

- **Orquestracao de containers**
  - [Amazon ECS](https://aws.amazon.com/ecs/) - Nativo AWS, mais simples de configurar
  - [Amazon EKS](https://aws.amazon.com/eks/) - Kubernetes gerenciado, portabilidade entre nuvens

### Habilidades Necessárias

- Desacoplar workloads para escalabilidade independente
- Identificar métricas e condições para acoes de escalabilidade
- Selecionar tipos de instância EC2 adequados (familias: M-geral, C-computacao, R-memoria, T-burst)
- Dimensionar recursos Lambda (memoria de 128 MB a 10 GB)

> **Dica para o exame**: Para workloads imprevisiveis, use Auto Scaling com Target Tracking. Para workloads agendadas (ex: pico as 9h), use Scheduled Scaling. Lambda escala automáticamente, mas tem limites de concorrência (1000 por padrão por região).

---

## Tarefa 3.3: Determinar soluções de banco de dados de alto desempenho

### Conhecimentos Necessários

- **Estratégias de cache**
  [Amazon ElastiCache](https://aws.amazon.com/elasticache/) oferece Redis (mais funcionalidades, persistência, replicação) e Memcached (mais simples, multi-thread). Use cache para leituras frequentes e dados que mudam pouco.

- **Padrões de acesso a dados**
  - **Leitura intensiva**: Use replicas de leitura e cache (ElastiCache)
  - **Escrita intensiva**: Use DynamoDB com modo on-demand ou Aurora com provisioned IOPS
  - **Acesso misto**: Combine cache + replicas de leitura + escritas no primário

- **Motores e tipos de banco de dados**
  - **Relacional** ([Amazon RDS](https://aws.amazon.com/rds/), [Aurora](https://aws.amazon.com/rds/aurora/)) - ACID, queries complexas, joins
  - **Chave-valor** ([Amazon DynamoDB](https://aws.amazon.com/dynamodb/)) - Latência em milissegundos, escala massiva
  - **In-memory** ([ElastiCache](https://aws.amazon.com/elasticache/)) - Microsegundos, cache e sessoes
  - **Documental** ([DocumentDB](https://aws.amazon.com/documentdb/)) - Compativel com MongoDB
  - **Grafo** ([Neptune](https://aws.amazon.com/neptune/)) - Relacionamentos complexos

- **Replicação e proxies**
  - Replicas de leitura no RDS: até 5 (MySQL/PostgreSQL), até 15 no Aurora
  - [Amazon RDS Proxy](https://aws.amazon.com/rds/proxy/) - Pool de conexões, reduz tempo de failover

### Habilidades Necessárias

- Configurar replicas de leitura para distribuir carga de leitura
- Projetar arquiteturas de banco de dados adequadas ao caso de uso
- Escolher entre bancos relacionais e não-relacionais
- Integrar caching para reduzir latência e carga no banco

> **Dica para o exame**: Aurora e até 5x mais rápido que MySQL e 3x mais rápido que PostgreSQL. DynamoDB Accelerator (DAX) oferece cache in-memory para DynamoDB com latência em microsegundos. Entenda quando usar cada opcao.

---

## Tarefa 3.4: Determinar arquiteturas de rede de alto desempenho e/ou escaláveis

### Conhecimentos Necessários

- **Serviços de rede de borda**
  - [Amazon CloudFront](https://aws.amazon.com/cloudfront/) - CDN com 400+ pontos de presenca global
  - [AWS Global Accelerator](https://aws.amazon.com/global-accelerator/) - Roteamento inteligente pela rede AWS

- **Arquitetura de rede**
  Projete VPCs com sub-redes públicas e privadas, tabelas de roteamento adequadas e CIDRs planejados para crescimento futuro.

- **Balanceamento de carga**
  - **ALB** - HTTP/HTTPS, roteamento por path/host, gRPC, WebSockets
  - **NLB** - TCP/UDP/TLS, IP estático, latência ultra-baixa
  - **GLB** - Appliances de rede virtual (firewalls, IDS/IPS)

- **Opcoes de conexão de rede**
  - [AWS VPN](https://aws.amazon.com/vpn/) - Conexão criptografada via internet (rápida de configurar)
  - [AWS Direct Connect](https://aws.amazon.com/directconnect/) - Conexão dedicada, latência consistente
  - [AWS PrivatéLink](https://aws.amazon.com/privatelink/) - Acesso privado a serviços sem internet

### Habilidades Necessárias

- Criar topologias de rede para arquiteturas globais, híbridas e multi-tier
- Configurar redes que escalam para necessidades futuras
- Selecionar estratégias de balanceamento de carga adequadas

> **Dica para o exame**: CloudFront e ideal para conteúdo estático e dinâmico com cache. Global Accelerator e melhor para aplicações que precisam de IP estático e failover rápido entre regiões. Direct Connect oferece maior largura de banda e latência mais consistente que VPN.

---

## Tarefa 3.5: Determinar soluções de ingestão e transformação de dados de alto desempenho

### Conhecimentos Necessários

- **Análise e visualização de dados**
  - [Amazon Athena](https://aws.amazon.com/athena/) - Queries SQL diretamente no S3 (serverless)
  - [AWS Lake Formation](https://aws.amazon.com/lake-formation/) - Criacao e gerenciamento de data lakes
  - [Amazon QuickSight](https://aws.amazon.com/quicksight/) - BI e visualização de dados

- **Ingestão e streaming de dados**
  - [Amazon Kinesis Data Streams](https://aws.amazon.com/kinesis/) - Streaming de dados em tempo real
  - [Amazon Kinesis Data Firehose](https://aws.amazon.com/kinesis/data-firehose/) - Entrega de dados para S3, Redshift, OpenSearch
  - [AWS DataSync](https://aws.amazon.com/datasync/) - Transferencia rápida de dados on-premises para AWS

- **Transformacao de dados**
  - [AWS Glue](https://aws.amazon.com/glue/) - ETL serverless, catalogo de dados, conversao de formatos (CSV para Parquet)

### Habilidades Necessárias

- Construir e proteger data lakes com Lake Formation e S3
- Projetar arquiteturas de streaming de dados com Kinesis
- Implementar pipelines de ETL com AWS Glue
- Selecionar opcoes de computacao para processamento de dados (EMR, Glue, Lambda)

> **Dica para o exame**: Kinesis Data Streams e para processamento em tempo real personalizado. Kinesis Data Firehose e para entrega automática (near real-time) a destinos como S3. Athena e ideal para queries ad-hoc no S3 sem necessidade de infraestrutura.

---

## Serviços-Chave para o Domínio 3

| Serviço | Função Principal |
|---------|-----------------|
| Amazon S3 | Armazenamento de objetos |
| Amazon EBS | Armazenamento de blocos |
| Amazon EFS | Sistema de arquivos elástico |
| Amazon EC2 Auto Scaling | Escalabilidade automática |
| AWS Lambda | Computacao serverless |
| Amazon ElastiCache | Cache in-memory (Redis/Memcached) |
| Amazon Aurora | Banco relacional de alto desempenho |
| Amazon DynamoDB | Banco NoSQL chave-valor |
| Amazon CloudFront | CDN global |
| Amazon Kinesis | Streaming de dados em tempo real |
| AWS Glue | ETL serverless |

---

Este guia abrange as principais areas do Domínio 3. Foque em entender as caracteristicas de desempenho de cada serviço e quando cada um e a melhor opcao para diferentes cenários.
