# Domínio 2 - Design de Arquiteturas Resilientes (26% do Exame)

> Este domínio avalia sua capacidade de projetar arquiteturas que sejam escaláveis, fracamente acopladas, altamente disponiveis e tolerantes a falhas. Foque em desacoplamento, estratégias de DR e uso de múltiplas AZs.

---

## Tarefa 2.1: Projetar arquiteturas escaláveis e fracamente acopladas

### Conhecimentos Necessários

- **Criacao e gerenciamento de APIs**
  O [Amazon API Gatéway](https://aws.amazon.com/api-gateway/) permite criar, públicar e gerenciar APIs REST e WebSocket. Suporta throttling, caching, autorizacao e versionamento. Integra-se com Lambda para arquiteturas serverless.

- **Serviços gerenciados da AWS**
  Use serviços gerenciados sempre que possível para reduzir a carga operacional. O [AWS Transfer Family](https://aws.amazon.com/aws-transfer-family/) gerencia transferencias SFTP/FTP. O [Amazon SQS](https://aws.amazon.com/sqs/) desacopla componentes com filas de mensagens.

- **Estratégias de cache**
  O [Amazon ElastiCache](https://aws.amazon.com/elasticache/) oferece Redis e Memcached para caching in-memory. Use cache para reduzir latência e carga no banco de dados. Estratégias comuns: cache-aside (lazy loading), write-through e TTL.

- **Principios de design para microsserviços**
  Workloads **statéless** sao mais faceis de escalar horizontalmente. Armazene estado em serviços externos (DynamoDB, ElastiCache, S3). [AWS Lambda](https://aws.amazon.com/lambda/) e [AWS Fargaté](https://aws.amazon.com/fargate/) fácilitam microsserviços.

- **Arquiteturas orientadas a eventos**
  O [Amazon EventBridge](https://aws.amazon.com/eventbridge/) e o barramento de eventos serverless da AWS. O [Amazon SNS](https://aws.amazon.com/sns/) permite pub/sub para notificações. Combine com SQS para processamento assincrono confiável.

- **Escalabilidade horizontal e vertical**
  - **Horizontal** (scale out): Adicionar mais instâncias - preferido na AWS
  - **Vertical** (scale up): Aumentar o tamanho da instância - tem limites
  - [Amazon EC2 Auto Scaling](https://aws.amazon.com/autoscaling/) gerencia a escalabilidade horizontal automáticamente

- **Aceleradores de borda**
  O [Amazon CloudFront](https://aws.amazon.com/cloudfront/) e um CDN global que cacheia conteúdo em edge locations. O [AWS Global Accelerator](https://aws.amazon.com/global-accelerator/) melhora a disponibilidade e performance usando a rede global da AWS.

- **Containers e orquestracao**
  - [Amazon ECS](https://aws.amazon.com/ecs/) - Orquestracao de containers pela AWS
  - [Amazon EKS](https://aws.amazon.com/eks/) - Kubernetes gerenciado
  - [AWS Fargaté](https://aws.amazon.com/fargate/) - Serverless para containers (sem gerenciar servidores)

- **Balanceamento de carga**
  - **ALB** (Application Load Balancer) - Camada 7, roteamento por conteúdo HTTP/HTTPS
  - **NLB** (Network Load Balancer) - Camada 4, ultra-baixa latência, milhoes de requisicoes/segundo
  - **GLB** (Gatéway Load Balancer) - Para appliances de rede virtual

- **Filas e mensagens**
  - **Amazon SQS Standard** - Entrega pelo menos uma vez, sem garantia de ordem
  - **Amazon SQS FIFO** - Exatamente uma vez, ordem garantida (menor throughput)
  - **Amazon SNS** - Pub/Sub para fan-out de mensagens

### Habilidades Necessárias

- Projetar arquiteturas orientadas a eventos, microsserviços e multi-tier
- Determinar estratégias de escalabilidade para componentes da arquitetura
- Determinar serviços AWS para desacoplamento (SQS, SNS, Step Functions)
- Decidir quando usar containers vs. serverless vs. instâncias EC2
- Recomendar tecnologias adequadas de computacao, armazenamento, rede e banco de dados

> **Dica para o exame**: Quando a questao menciona "desacoplamento", pense em SQS, SNS e EventBridge. Quando menciona "escalabilidade", pense em Auto Scaling Groups e Lambda. A combinacao SQS + Auto Scaling e um padrão clássico no exame.

---

## Tarefa 2.2: Projetar arquiteturas altamente disponiveis e/ou tolerantes a falhas

### Conhecimentos Necessários

- **Infraestrutura global da AWS**
  Distribua recursos em múltiplas Zonas de Disponibilidade (AZs) para alta disponibilidade. Use múltiplas Regioes para disaster recovery. O [Amazon Route 53](https://aws.amazon.com/route53/) oferece DNS com health checks e failover.

- **Estratégias de recuperação de desastrês (DR)**
  Da mais barata para a mais rápida:
  1. **Backup & Restore** - RPO/RTO: horas. Backups em S3, restauracao manual
  2. **Pilot Light** - RPO/RTO: minutos. Componentes críticos em standby mínimo
  3. **Warm Standby** - RPO/RTO: minutos. Versao reduzida do ambiente em execucao
  4. **Active-Active (Multi-site)** - RPO/RTO: quase zero. Ambiente completo em múltiplas regiões

- **Padrões de design distribuido**
  Use [Amazon CloudFront](https://aws.amazon.com/cloudfront/) para distribuir conteúdo globalmente. O [AWS Global Accelerator](https://aws.amazon.com/global-accelerator/) melhora a disponibilidade com failover automático entre regiões.

- **Infraestrutura imutavel**
  Use [AWS CloudFormation](https://aws.amazon.com/cloudformation/) ou Terraform para definir infraestrutura como código. Em vez de atualizar servidores existentes, substitua-os por novos (Blue/Green, Canary deployments).

- **Proxies de banco de dados**
  O [Amazon RDS Proxy](https://aws.amazon.com/rds/proxy/) gerencia pools de conexões, melhora a resiliência e reduz o tempo de failover de banco de dados. Essencial para funções Lambda que acessam RDS.

- **Visibilidade de workloads**
  - [Amazon CloudWatch](https://aws.amazon.com/cloudwatch/) - Metricas, logs, alarmes e dashboards
  - [AWS X-Ray](https://aws.amazon.com/xray/) - Rastreamento distribuido para debugar microsserviços

### Habilidades Necessárias

- Determinar estratégias de automação para integridade da infraestrutura
- Fornecer arquiteturas altamente disponiveis em múltiplas AZs e Regioes
- Identificar métricas de negocio para soluções de alta disponibilidade
- Implementar designs para mitigar pontos únicos de falha (SPOF)
- Implementar estratégias para durabilidade e disponibilidade de dados
- Selecionar estratégias de DR apropriadas ao negocio

> **Dica para o exame**: Sempre distribua recursos em pelo menos 2 AZs. Se a questao pede "máxima disponibilidade", pense em Multi-AZ e Multi-Region. Para banco de dados, Multi-AZ RDS oferece failover automático. Aurora pode ter até 15 replicas de leitura em 3 AZs.

---

## Serviços-Chave para o Domínio 2

| Serviço | Função Principal |
|---------|-----------------|
| Amazon SQS | Filas de mensagens para desacoplamento |
| Amazon SNS | Pub/Sub para notificações e fan-out |
| Amazon EventBridge | Barramento de eventos serverless |
| Elastic Load Balancing | Distribuição de tráfego (ALB, NLB, GLB) |
| Amazon EC2 Auto Scaling | Escalabilidade automática de instâncias |
| Amazon Route 53 | DNS com health checks e failover |
| AWS CloudFormation | Infraestrutura como código |
| Amazon CloudWatch | Monitoramento e observabilidade |
| AWS Backup | Gerenciamento centralizado de backups |
| Amazon RDS Proxy | Pool de conexões para bancos de dados |

---

Este guia abrange as principais areas do Domínio 2. A resiliência e um dos pilares do Well-Architected Framework, então entenda profundamente os conceitos de alta disponibilidade, tolerância a falhas e recuperação de desastrês.
