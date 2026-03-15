# Checklist de Revisão Final - AWS Solutions Architect Associaté

> Use este checklist antes do exame para garantir que você cobriu todos os topicos importantes. Marque cada item conforme for revisando.

---

## Domínio 1: Design de Arquiteturas Seguras (30%)

### IAM e Gerenciamento de Acesso
- [ ] Usuarios, grupos, funções e politicas do IAM
- [ ] Politicas gerenciadas vs. inline vs. de recurso
- [ ] Principio do menor privilegio
- [ ] AWS Organizations e SCPs (Service Control Policies)
- [ ] AWS IAM Identity Center (SSO) e federacao
- [ ] AWS STS e AssumeRole para acesso entre contas
- [ ] MFA e politicas de senha

### Segurança de Rede
- [ ] VPC: sub-redes públicas e privadas
- [ ] Security Groups (statéful) vs. NACLs (statéless)
- [ ] NAT Gatéway vs. NAT Instance
- [ ] VPC Endpoints (Gatéway para S3/DynamoDB, Interface para outros)
- [ ] AWS Network Firewall
- [ ] AWS WAF e AWS Shield (Standard vs. Advanced)

### Criptografia e Proteção de Dados
- [ ] AWS KMS: CMKs gerenciadas pela AWS vs. pelo cliente
- [ ] Criptografia em repouso: SSE-S3, SSE-KMS, SSE-C
- [ ] Criptografia em trânsito: TLS/SSL com ACM
- [ ] AWS Secrets Manager vs. Systems Manager Parameter Store
- [ ] Amazon Macie para dados sensíveis no S3
- [ ] AWS CloudTrail para auditoria

### Modelo de Responsabilidade Compartilhada
- [ ] AWS: segurança DA nuvem (infraestrutura, rede, hipervisor)
- [ ] Cliente: segurança NA nuvem (dados, apps, configuração)

---

## Domínio 2: Design de Arquiteturas Resilientes (26%)

### Desacoplamento e Escalabilidade
- [ ] Amazon SQS: Standard vs. FIFO, Dead Letter Queues
- [ ] Amazon SNS: pub/sub, fan-out com SQS
- [ ] Amazon EventBridge: roteamento de eventos
- [ ] AWS Step Functions: orquestracao de workflows
- [ ] Escalabilidade horizontal vs. vertical
- [ ] EC2 Auto Scaling: politicas (Target Tracking, Step, Scheduled)

### Alta Disponibilidade
- [ ] Multi-AZ para RDS, ElastiCache, EFS
- [ ] ELB: ALB (camada 7) vs. NLB (camada 4) vs. GLB
- [ ] Amazon Route 53: politicas de roteamento (Simple, Weighted, Laténcy, Failover, Geolocation, Multivalue)
- [ ] Health checks e failover automático

### Recuperação de Desastrês
- [ ] RPO (Recovery Point Objective) e RTO (Recovery Time Objective)
- [ ] Estratégias de DR: Backup & Restore, Pilot Light, Warm Standby, Active-Active
- [ ] AWS Backup para gerenciamento centralizado
- [ ] Replicação cross-region para S3 e RDS

### Containers e Serverless
- [ ] Amazon ECS vs. Amazon EKS
- [ ] AWS Fargaté (serverless para containers)
- [ ] AWS Lambda: limites (15 min, 10 GB memoria, 1000 concorrência padrão)

---

## Domínio 3: Design de Arquiteturas de Alto Desempenho (24%)

### Armazenamento
- [ ] Amazon S3: classes de armazenamento e lifecycle policies
- [ ] Amazon EBS: gp3/gp2 (SSD geral), io2 (alto IOPS), st1/sc1 (HDD)
- [ ] Amazon EFS: elástico, compartilhado, NFS
- [ ] Amazon FSx: Windows File Server, Lustre
- [ ] S3 Transfer Acceleration e multipart upload

### Computacao
- [ ] Familias de instâncias EC2: M (geral), C (computacao), R (memoria), T (burst)
- [ ] Spot Instances, Reserved Instances, Savings Plans
- [ ] Lambda@Edge e CloudFront Functions
- [ ] AWS Batch para processamento em lote

### Banco de Dados
- [ ] Amazon RDS: motores suportados, Multi-AZ, replicas de leitura
- [ ] Amazon Aurora: até 15 replicas, 5x mais rápido que MySQL
- [ ] Amazon DynamoDB: chave-valor, DAX para cache, Global Tables
- [ ] Amazon ElastiCache: Redis vs. Memcached
- [ ] Amazon Redshift: data warehouse columnar

### Rede
- [ ] Amazon CloudFront: CDN, edge locations, Origin Access Control
- [ ] AWS Global Accelerator: IP anycast, failover entre regiões
- [ ] AWS Direct Connect: conexão dedicada, menor latência
- [ ] AWS VPN: Site-to-Site e Client VPN

### Dados e Analytics
- [ ] Amazon Kinesis: Data Streams vs. Data Firehose
- [ ] AWS Glue: ETL serverless, catalogo de dados
- [ ] Amazon Athena: SQL no S3
- [ ] Amazon QuickSight: BI e dashboards

---

## Domínio 4: Design de Arquiteturas Otimizadas por Custo (20%)

### Otimização de Computacao
- [ ] Right-sizing com AWS Compute Optimizer
- [ ] Modelos de compra EC2: On-Demand, RI, Savings Plans, Spot
- [ ] Lambda para workloads que escalam a zero
- [ ] Fargaté vs. EC2 para containers

### Otimização de Armazenamento
- [ ] S3 Intelligent-Tiering para padrões de acesso desconhecidos
- [ ] S3 Lifecycle Policies para transicoes automáticas
- [ ] EBS: gp3 e mais econômico que gp2 para mesmo desempenho
- [ ] Requester Pays para buckets S3

### Otimização de Banco de Dados
- [ ] Aurora Serverless para workloads imprevisiveis
- [ ] DynamoDB: On-Demand vs. Provisioned
- [ ] Migrar de bancos comerciais para open source com DMS
- [ ] Reserved Instances para RDS

### Otimização de Rede
- [ ] VPC Endpoints eliminam custos de NAT
- [ ] CloudFront reduz custos de egress
- [ ] Dados de entrada (ingress) sao gratuitos
- [ ] VPC Peering na mesma AZ e gratuito

### Ferramentas de Gerenciamento de Custos
- [ ] AWS Cost Explorer
- [ ] AWS Budgets (alertas)
- [ ] AWS Trusted Advisor
- [ ] Tags de alocação de custos

---

## Conceitos Transversais

- [ ] AWS Well-Architected Framework (6 pilares)
- [ ] Infraestrutura global: Regioes, AZs, Edge Locations
- [ ] Infraestrutura como Codigo: CloudFormation
- [ ] Monitoramento: CloudWatch (métricas, logs, alarmes)
- [ ] Automação: Systems Manager, EventBridge

---

Voltar ao [Índice](../../../index.md)
