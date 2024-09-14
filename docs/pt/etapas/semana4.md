# 📋 Guia do Exame: Domínio 2 - Design de Arquiteturas Resilientes

## 🎯 Tarefa 2.1: Projetar arquiteturas escaláveis e fracamente acopladas

### Conhecimentos Necessários

- 🌐 Criação e gerenciamento de APIs (por exemplo, [Amazon API Gateway](https://aws.amazon.com/api-gateway/), REST API)  
  **Serviços correlacionados**: [Amazon API Gateway](https://aws.amazon.com/api-gateway/)

- ⚙️ Serviços gerenciados da AWS com casos de uso apropriados (por exemplo, [AWS Transfer Family](https://aws.amazon.com/aws-transfer-family/), [Amazon Simple Queue Service (Amazon SQS)](https://aws.amazon.com/sqs/), [AWS Secrets Manager](https://aws.amazon.com/secrets-manager/))  
  **Serviços correlacionados**: [AWS Transfer Family](https://aws.amazon.com/aws-transfer-family/), [Amazon SQS](https://aws.amazon.com/sqs/), [AWS Secrets Manager](https://aws.amazon.com/secrets-manager/)

- 💾 Estratégias de cache  
  **Serviços correlacionados**: [Amazon ElastiCache](https://aws.amazon.com/elasticache/)

- 🛠️ Princípios de design para microsserviços (por exemplo, workloads sem estado em comparação com workloads com estado)  
  **Serviços correlacionados**: [AWS Lambda](https://aws.amazon.com/lambda/), [AWS Fargate](https://aws.amazon.com/fargate/), [Amazon ECS](https://aws.amazon.com/ecs/), [Amazon EKS](https://aws.amazon.com/eks/)

- 🔄 Arquiteturas orientadas a eventos  
  **Serviços correlacionados**: [Amazon EventBridge](https://aws.amazon.com/eventbridge/), [Amazon SNS](https://aws.amazon.com/sns/)

- 🔄 Escalabilidade horizontal e vertical  
  **Serviços correlacionados**: [Amazon EC2 Auto Scaling](https://aws.amazon.com/autoscaling/), [AWS Lambda](https://aws.amazon.com/lambda/)

- 🚀 Uso apropriado de aceleradores de borda (por exemplo, Content Delivery Network [CDN])  
  **Serviços correlacionados**: [Amazon CloudFront](https://aws.amazon.com/cloudfront/), [AWS Global Accelerator](https://aws.amazon.com/global-accelerator/)

- 📦 Migração de aplicações para containers  
  **Serviços correlacionados**: [Amazon ECS](https://aws.amazon.com/ecs/), [Amazon EKS](https://aws.amazon.com/eks/), [AWS Fargate](https://aws.amazon.com/fargate/)

- ⚖️ Conceitos de balanceamento de carga (por exemplo, [Application Load Balancer](https://aws.amazon.com/elasticloadbalancing/))  
  **Serviços correlacionados**: [Elastic Load Balancing](https://aws.amazon.com/elasticloadbalancing/)

- 🏗️ Arquiteturas em múltiplos níveis  
  **Serviços correlacionados**: [Amazon EC2](https://aws.amazon.com/ec2/), [Amazon RDS](https://aws.amazon.com/rds/)

- 📬 Conceitos de filas e mensagens (por exemplo, public/subscribe)  
  **Serviços correlacionados**: [Amazon SQS](https://aws.amazon.com/sqs/), [Amazon SNS](https://aws.amazon.com/sns/)

- 🚀 Tecnologias e padrões serverless (por exemplo, [AWS Fargate](https://aws.amazon.com/fargate/), [AWS Lambda](https://aws.amazon.com/lambda/))  
  **Serviços correlacionados**: [AWS Fargate](https://aws.amazon.com/fargate/), [AWS Lambda](https://aws.amazon.com/lambda/)

- 💾 Tipos de armazenamento com características associadas (por exemplo, objeto, arquivo, bloco)  
  **Serviços correlacionados**: [Amazon S3](https://aws.amazon.com/s3/), [Amazon EFS](https://aws.amazon.com/efs/), [Amazon EBS](https://aws.amazon.com/ebs/)

- ⚙️ Orquestração de containers (por exemplo, [Amazon Elastic Container Service (Amazon ECS)](https://aws.amazon.com/ecs/), [Amazon Elastic Kubernetes Service (Amazon EKS)](https://aws.amazon.com/eks/))  
  **Serviços correlacionados**: [Amazon ECS](https://aws.amazon.com/ecs/), [Amazon EKS](https://aws.amazon.com/eks/)

- 🔄 Quando usar réplicas de leitura  
  **Serviços correlacionados**: [Amazon RDS](https://aws.amazon.com/rds/)

- 🛠️ Orquestração de workflows (por exemplo, [AWS Step Functions](https://aws.amazon.com/step-functions/))  
  **Serviços correlacionados**: [AWS Step Functions](https://aws.amazon.com/step-functions/)

### Habilidades Necessárias

- 🛠️ Projetar arquiteturas orientadas a eventos, microsserviços e/ou em múltiplos níveis com base em requisitos  
  **Serviços correlacionados**: [Amazon EventBridge](https://aws.amazon.com/eventbridge/), [AWS Lambda](https://aws.amazon.com/lambda/)

- 🔄 Determinar estratégias de escalabilidade para componentes usados em um design de arquitetura  
  **Serviços correlacionados**: [Amazon EC2 Auto Scaling](https://aws.amazon.com/autoscaling/), [AWS Lambda](https://aws.amazon.com/lambda/)

- 🛠️ Determinar os serviços AWS necessários para alcançar desacoplamento com base nos requisitos  
  **Serviços correlacionados**: [Amazon SQS](https://aws.amazon.com/sqs/), [Amazon SNS](https://aws.amazon.com/sns/), [AWS Step Functions](https://aws.amazon.com/step-functions/)

- 📦 Determinar quando usar containers  
  **Serviços correlacionados**: [Amazon ECS](https://aws.amazon.com/ecs/), [Amazon EKS](https://aws.amazon.com/eks/)

- 🚀 Determinar quando usar tecnologias e padrões serverless  
  **Serviços correlacionados**: [AWS Lambda](https://aws.amazon.com/lambda/), [AWS Fargate](https://aws.amazon.com/fargate/)

- 📊 Recomendar tecnologias adequadas de computação, armazenamento, rede e banco de dados com base nos requisitos  
  **Serviços correlacionados**: [Amazon EC2](https://aws.amazon.com/ec2/), [Amazon S3](https://aws.amazon.com/s3/), [Amazon RDS](https://aws.amazon.com/rds/)

- 🛠️ Usar serviços da AWS para workloads com propósito específico  
  **Serviços correlacionados**: [Amazon Redshift](https://aws.amazon.com/redshift/), [Amazon DynamoDB](https://aws.amazon.com/dynamodb/), [AWS Glue](https://aws.amazon.com/glue/)

---

Este guia abrange as principais áreas e habilidades necessárias para o Domínio 2 do exame AWS Solutions Architect Associate. Certifique-se de revisar cada área e prática para garantir uma compreensão abrangente e aplicação das melhores práticas de resiliência da AWS.

---

🔙 [Voltar ao Índice](../../../index.md)
