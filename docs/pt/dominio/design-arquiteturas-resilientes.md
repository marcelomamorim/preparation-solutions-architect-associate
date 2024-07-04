# 📋 Guia do Exame: Domínio 2 - Design de Arquiteturas Resilientes

## 🎯 Tarefa 2.1: Projetar arquiteturas escaláveis e fracamente acopladas

### Conhecimentos Necessários

- 🌐 Criação e gerenciamento de APIs (por exemplo, Amazon API Gateway, REST API)  
  **Serviços correlacionados**: Amazon API Gateway

- ⚙️ Serviços gerenciados da AWS com casos de uso apropriados (por exemplo, AWS Transfer Family, Amazon Simple Queue Service [Amazon SQS], Secrets Manager)  
  **Serviços correlacionados**: AWS Transfer Family, Amazon SQS, AWS Secrets Manager

- 💾 Estratégias de cache  
  **Serviços correlacionados**: Amazon ElastiCache

- 🛠️ Princípios de design para microsserviços (por exemplo, workloads sem estado em comparação com workloads com estado)  
  **Serviços correlacionados**: AWS Lambda, AWS Fargate, Amazon ECS, Amazon EKS

- 🔄 Arquiteturas orientadas a eventos  
  **Serviços correlacionados**: Amazon EventBridge, Amazon SNS

- 🔄 Escalabilidade horizontal e vertical  
  **Serviços correlacionados**: Amazon EC2 Auto Scaling, AWS Lambda

- 🚀 Uso apropriado de aceleradores de borda (por exemplo, Content Delivery Network [CDN])  
  **Serviços correlacionados**: Amazon CloudFront, AWS Global Accelerator

- 📦 Migração de aplicações para containers  
  **Serviços correlacionados**: Amazon ECS, Amazon EKS, AWS Fargate

- ⚖️ Conceitos de balanceamento de carga (por exemplo, Application Load Balancer)  
  **Serviços correlacionados**: Elastic Load Balancing

- 🏗️ Arquiteturas em múltiplos níveis  
  **Serviços correlacionados**: Amazon EC2, Amazon RDS

- 📬 Conceitos de filas e mensagens (por exemplo, public/subscribe)  
  **Serviços correlacionados**: Amazon SQS, Amazon SNS

- 🚀 Tecnologias e padrões serverless (por exemplo, AWS Fargate, AWS Lambda)  
  **Serviços correlacionados**: AWS Fargate, AWS Lambda

- 💾 Tipos de armazenamento com características associadas (por exemplo, objeto, arquivo, bloco)  
  **Serviços correlacionados**: Amazon S3, Amazon EFS, Amazon EBS

- ⚙️ Orquestração de containers (por exemplo, Amazon Elastic Container Service [Amazon ECS], Amazon Elastic Kubernetes Service [Amazon EKS])  
  **Serviços correlacionados**: Amazon ECS, Amazon EKS

- 🔄 Quando usar réplicas de leitura  
  **Serviços correlacionados**: Amazon RDS

- 🛠️ Orquestração de workflows (por exemplo, AWS Step Functions)  
  **Serviços correlacionados**: AWS Step Functions

### Habilidades Necessárias

- 🛠️ Projetar arquiteturas orientadas a eventos, microsserviços e/ou em múltiplos níveis com base em requisitos  
  **Serviços correlacionados**: Amazon EventBridge, AWS Lambda

- 🔄 Determinar estratégias de escalabilidade para componentes usados em um design de arquitetura  
  **Serviços correlacionados**: Amazon EC2 Auto Scaling, AWS Lambda

- 🛠️ Determinar os serviços AWS necessários para alcançar desacoplamento com base nos requisitos  
  **Serviços correlacionados**: Amazon SQS, Amazon SNS, AWS Step Functions

- 📦 Determinar quando usar containers  
  **Serviços correlacionados**: Amazon ECS, Amazon EKS

- 🚀 Determinar quando usar tecnologias e padrões serverless  
  **Serviços correlacionados**: AWS Lambda, AWS Fargate

- 📊 Recomendar tecnologias adequadas de computação, armazenamento, rede e banco de dados com base nos requisitos  
  **Serviços correlacionados**: Amazon EC2, Amazon S3, Amazon RDS

- 🛠️ Usar serviços da AWS para workloads com propósito específico  
  **Serviços correlacionados**: Amazon Redshift, Amazon DynamoDB, AWS Glue

---

## 🔒 Tarefa 2.2: Projetar arquiteturas altamente disponíveis e/ou tolerantes a falhas

### Conhecimentos Necessários

- 🌍 Infraestrutura global da AWS (por exemplo, Zonas de Disponibilidade, Regiões da AWS, Amazon Route 53)  
  **Serviços correlacionados**: Amazon Route 53, AWS Regions

- ⚙️ Serviços gerenciados da AWS com casos de uso apropriados (por exemplo, Amazon Comprehend, Amazon Polly)  
  **Serviços correlacionados**: Amazon Comprehend, Amazon Polly

- 🌐 Conceitos básicos de rede (por exemplo, tabelas de roteamento)  
  **Serviços correlacionados**: Amazon VPC

- 🛠️ Estratégias de recuperação de desastres (por exemplo, backup e restauração, pilot light, warm standby, failover ativo-ativo, ponto de recuperação [RPO], tempo de recuperação [RTO])  
  **Serviços correlacionados**: AWS Backup, AWS Storage Gateway

- 🛡️ Padrões de design distribuído  
  **Serviços correlacionados**: Amazon CloudFront, AWS Global Accelerator

- 🔄 Estratégias de failover  
  **Serviços correlacionados**: Amazon Route 53

- 📦 Infraestrutura imutável  
  **Serviços correlacionados**: AWS Elastic Beanstalk, AWS CloudFormation

- ⚖️ Conceitos de balanceamento de carga (por exemplo, Application Load Balancer)  
  **Serviços correlacionados**: Elastic Load Balancing

- 🛡️ Conceitos de proxy (por exemplo, Amazon RDS Proxy)  
  **Serviços correlacionados**: Amazon RDS Proxy

- 📊 Quotas de serviço e limitação (por exemplo, como configurar as quotas de serviço para uma workload em um ambiente de standby)  
  **Serviços correlacionados**: AWS Trusted Advisor, AWS Management Console

- 💾 Opções de armazenamento e características (por exemplo, durabilidade, replicação)  
  **Serviços correlacionados**: Amazon S3, Amazon EBS, Amazon EFS

- 👀 Visibilidade de workloads (por exemplo, AWS X-Ray)  
  **Serviços correlacionados**: AWS X-Ray, Amazon CloudWatch

### Habilidades Necessárias

- 🛠️ Determinar estratégias de automação para garantir a integridade da infraestrutura  
  **Serviços correlacionados**: AWS CloudFormation, AWS Systems Manager

- 🌍 Determinar os serviços da AWS necessários para fornecer uma arquitetura altamente disponível e/ou tolerante a falhas em Regiões da AWS ou Zonas de Disponibilidade  
  **Serviços correlacionados**: Amazon Route 53, AWS Global Accelerator, Amazon RDS

- 📊 Identificar métricas com base nos requisitos de negócios para entregar uma solução altamente disponível  
  **Serviços correlacionados**: Amazon CloudWatch, AWS X-Ray

- 🔄 Implementar designs para mitigar pontos únicos de falha  
  **Serviços correlacionados**: Elastic Load Balancing, Amazon Route 53

- 🔒 Implementar estratégias para garantir a durabilidade e disponibilidade dos dados (por exemplo, backups)  
  **Serviços correlacionados**: AWS Backup, Amazon S3

- 🛠️ Selecionar uma estratégia de recuperação de desastres apropriada para atender aos requisitos de negócios  
  **Serviços correlacionados**: AWS Backup, AWS Storage Gateway

- 🚀 Usar serviços da AWS que melhorem a confiabilidade de aplicações legadas e aplicações não projetadas para a nuvem (por exemplo, quando mudanças na aplicação não são possíveis)  
  **Serviços correlacionados**: Amazon RDS Proxy, AWS App Mesh

- 🛠️ Usar serviços da AWS com propósito específico para workloads  
  **Serviços correlacionados**: Amazon Redshift, Amazon DynamoDB, AWS Glue

---

Este guia abrange as principais áreas e habilidades necessárias para o Domínio 2 do exame AWS Solutions Architect Associate. Certifique-se de revisar cada área e prática para garantir uma compreensão abrangente e aplicação das melhores práticas de resiliência da AWS.
