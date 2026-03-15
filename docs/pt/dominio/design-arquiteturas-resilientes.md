# Dominio 2 - Design de Arquiteturas Resilientes (26% do Exame)

> Este dominio avalia sua capacidade de projetar arquiteturas que sejam escalaveis, fracamente acopladas, altamente disponiveis e tolerantes a falhas. Foque em desacoplamento, estrategias de DR e uso de multiplas AZs.

---

## Tarefa 2.1: Projetar arquiteturas escalaveis e fracamente acopladas

### Conhecimentos Necessarios

- **Criacao e gerenciamento de APIs**
  O [Amazon API Gateway](https://aws.amazon.com/api-gateway/) permite criar, publicar e gerenciar APIs REST e WebSocket. Suporta throttling, caching, autorizacao e versionamento. Integra-se com Lambda para arquiteturas serverless.

- **Servicos gerenciados da AWS**
  Use servicos gerenciados sempre que possivel para reduzir a carga operacional. O [AWS Transfer Family](https://aws.amazon.com/aws-transfer-family/) gerencia transferencias SFTP/FTP. O [Amazon SQS](https://aws.amazon.com/sqs/) desacopla componentes com filas de mensagens.

- **Estrategias de cache**
  O [Amazon ElastiCache](https://aws.amazon.com/elasticache/) oferece Redis e Memcached para caching in-memory. Use cache para reduzir latencia e carga no banco de dados. Estrategias comuns: cache-aside (lazy loading), write-through e TTL.

- **Principios de design para microsservicos**
  Workloads **stateless** sao mais faceis de escalar horizontalmente. Armazene estado em servicos externos (DynamoDB, ElastiCache, S3). [AWS Lambda](https://aws.amazon.com/lambda/) e [AWS Fargate](https://aws.amazon.com/fargate/) facilitam microsservicos.

- **Arquiteturas orientadas a eventos**
  O [Amazon EventBridge](https://aws.amazon.com/eventbridge/) e o barramento de eventos serverless da AWS. O [Amazon SNS](https://aws.amazon.com/sns/) permite pub/sub para notificacoes. Combine com SQS para processamento assincrono confiavel.

- **Escalabilidade horizontal e vertical**
  - **Horizontal** (scale out): Adicionar mais instancias - preferido na AWS
  - **Vertical** (scale up): Aumentar o tamanho da instancia - tem limites
  - [Amazon EC2 Auto Scaling](https://aws.amazon.com/autoscaling/) gerencia a escalabilidade horizontal automaticamente

- **Aceleradores de borda**
  O [Amazon CloudFront](https://aws.amazon.com/cloudfront/) e um CDN global que cacheia conteudo em edge locations. O [AWS Global Accelerator](https://aws.amazon.com/global-accelerator/) melhora a disponibilidade e performance usando a rede global da AWS.

- **Containers e orquestracao**
  - [Amazon ECS](https://aws.amazon.com/ecs/) - Orquestracao de containers pela AWS
  - [Amazon EKS](https://aws.amazon.com/eks/) - Kubernetes gerenciado
  - [AWS Fargate](https://aws.amazon.com/fargate/) - Serverless para containers (sem gerenciar servidores)

- **Balanceamento de carga**
  - **ALB** (Application Load Balancer) - Camada 7, roteamento por conteudo HTTP/HTTPS
  - **NLB** (Network Load Balancer) - Camada 4, ultra-baixa latencia, milhoes de requisicoes/segundo
  - **GLB** (Gateway Load Balancer) - Para appliances de rede virtual

- **Filas e mensagens**
  - **Amazon SQS Standard** - Entrega pelo menos uma vez, sem garantia de ordem
  - **Amazon SQS FIFO** - Exatamente uma vez, ordem garantida (menor throughput)
  - **Amazon SNS** - Pub/Sub para fan-out de mensagens

### Habilidades Necessarias

- Projetar arquiteturas orientadas a eventos, microsservicos e multi-tier
- Determinar estrategias de escalabilidade para componentes da arquitetura
- Determinar servicos AWS para desacoplamento (SQS, SNS, Step Functions)
- Decidir quando usar containers vs. serverless vs. instancias EC2
- Recomendar tecnologias adequadas de computacao, armazenamento, rede e banco de dados

> **Dica para o exame**: Quando a questao menciona "desacoplamento", pense em SQS, SNS e EventBridge. Quando menciona "escalabilidade", pense em Auto Scaling Groups e Lambda. A combinacao SQS + Auto Scaling e um padrao classico no exame.

---

## Tarefa 2.2: Projetar arquiteturas altamente disponiveis e/ou tolerantes a falhas

### Conhecimentos Necessarios

- **Infraestrutura global da AWS**
  Distribua recursos em multiplas Zonas de Disponibilidade (AZs) para alta disponibilidade. Use multiplas Regioes para disaster recovery. O [Amazon Route 53](https://aws.amazon.com/route53/) oferece DNS com health checks e failover.

- **Estrategias de recuperacao de desastres (DR)**
  Da mais barata para a mais rapida:
  1. **Backup & Restore** - RPO/RTO: horas. Backups em S3, restauracao manual
  2. **Pilot Light** - RPO/RTO: minutos. Componentes criticos em standby minimo
  3. **Warm Standby** - RPO/RTO: minutos. Versao reduzida do ambiente em execucao
  4. **Active-Active (Multi-site)** - RPO/RTO: quase zero. Ambiente completo em multiplas regioes

- **Padroes de design distribuido**
  Use [Amazon CloudFront](https://aws.amazon.com/cloudfront/) para distribuir conteudo globalmente. O [AWS Global Accelerator](https://aws.amazon.com/global-accelerator/) melhora a disponibilidade com failover automatico entre regioes.

- **Infraestrutura imutavel**
  Use [AWS CloudFormation](https://aws.amazon.com/cloudformation/) ou Terraform para definir infraestrutura como codigo. Em vez de atualizar servidores existentes, substitua-os por novos (Blue/Green, Canary deployments).

- **Proxies de banco de dados**
  O [Amazon RDS Proxy](https://aws.amazon.com/rds/proxy/) gerencia pools de conexoes, melhora a resiliencia e reduz o tempo de failover de banco de dados. Essencial para funcoes Lambda que acessam RDS.

- **Visibilidade de workloads**
  - [Amazon CloudWatch](https://aws.amazon.com/cloudwatch/) - Metricas, logs, alarmes e dashboards
  - [AWS X-Ray](https://aws.amazon.com/xray/) - Rastreamento distribuido para debugar microsservicos

### Habilidades Necessarias

- Determinar estrategias de automacao para integridade da infraestrutura
- Fornecer arquiteturas altamente disponiveis em multiplas AZs e Regioes
- Identificar metricas de negocio para solucoes de alta disponibilidade
- Implementar designs para mitigar pontos unicos de falha (SPOF)
- Implementar estrategias para durabilidade e disponibilidade de dados
- Selecionar estrategias de DR apropriadas ao negocio

> **Dica para o exame**: Sempre distribua recursos em pelo menos 2 AZs. Se a questao pede "maxima disponibilidade", pense em Multi-AZ e Multi-Region. Para banco de dados, Multi-AZ RDS oferece failover automatico. Aurora pode ter ate 15 replicas de leitura em 3 AZs.

---

## Servicos-Chave para o Dominio 2

| Servico | Funcao Principal |
|---------|-----------------|
| Amazon SQS | Filas de mensagens para desacoplamento |
| Amazon SNS | Pub/Sub para notificacoes e fan-out |
| Amazon EventBridge | Barramento de eventos serverless |
| Elastic Load Balancing | Distribuicao de trafego (ALB, NLB, GLB) |
| Amazon EC2 Auto Scaling | Escalabilidade automatica de instancias |
| Amazon Route 53 | DNS com health checks e failover |
| AWS CloudFormation | Infraestrutura como codigo |
| Amazon CloudWatch | Monitoramento e observabilidade |
| AWS Backup | Gerenciamento centralizado de backups |
| Amazon RDS Proxy | Pool de conexoes para bancos de dados |

---

Este guia abrange as principais areas do Dominio 2. A resiliencia e um dos pilares do Well-Architected Framework, entao entenda profundamente os conceitos de alta disponibilidade, tolerancia a falhas e recuperacao de desastres.
