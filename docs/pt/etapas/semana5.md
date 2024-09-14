# 📋 Guia do Exame: Domínio 2 - Design de Arquiteturas Resilientes

## 🔒 Tarefa 2.2: Projetar arquiteturas altamente disponíveis e/ou tolerantes a falhas

### Conhecimentos Necessários

- 🌍 Infraestrutura global da AWS (por exemplo, Zonas de Disponibilidade, Regiões da AWS, [Amazon Route 53](https://aws.amazon.com/route53/))  
  **Serviços correlacionados**: [Amazon Route 53](https://aws.amazon.com/route53/), [AWS Regions](https://aws.amazon.com/about-aws/global-infrastructure/regions_az/)

- ⚙️ Serviços gerenciados da AWS com casos de uso apropriados (por exemplo, [Amazon Comprehend](https://aws.amazon.com/comprehend/), [Amazon Polly](https://aws.amazon.com/polly/))  
  **Serviços correlacionados**: [Amazon Comprehend](https://aws.amazon.com/comprehend/), [Amazon Polly](https://aws.amazon.com/polly/)

- 🌐 Conceitos básicos de rede (por exemplo, tabelas de roteamento)  
  **Serviços correlacionados**: [Amazon VPC](https://aws.amazon.com/vpc/)

- 🛠️ Estratégias de recuperação de desastres (por exemplo, backup e restauração, pilot light, warm standby, failover ativo-ativo, ponto de recuperação [RPO], tempo de recuperação [RTO])  
  **Serviços correlacionados**: [AWS Backup](https://aws.amazon.com/backup/), [AWS Storage Gateway](https://aws.amazon.com/storagegateway/)

- 🛡️ Padrões de design distribuído  
  **Serviços correlacionados**: [Amazon CloudFront](https://aws.amazon.com/cloudfront/), [AWS Global Accelerator](https://aws.amazon.com/global-accelerator/)

- 🔄 Estratégias de failover  
  **Serviços correlacionados**: [Amazon Route 53](https://aws.amazon.com/route53/)

- 📦 Infraestrutura imutável  
  **Serviços correlacionados**: [AWS Elastic Beanstalk](https://aws.amazon.com/elasticbeanstalk/), [AWS CloudFormation](https://aws.amazon.com/cloudformation/)

- ⚖️ Conceitos de balanceamento de carga (por exemplo, [Application Load Balancer](https://aws.amazon.com/elasticloadbalancing/))  
  **Serviços correlacionados**: [Elastic Load Balancing](https://aws.amazon.com/elasticloadbalancing/)

- 🛡️ Conceitos de proxy (por exemplo, [Amazon RDS Proxy](https://aws.amazon.com/rds/proxy/))  
  **Serviços correlacionados**: [Amazon RDS Proxy](https://aws.amazon.com/rds/proxy/)

- 📊 Quotas de serviço e limitação (por exemplo, como configurar as quotas de serviço para uma workload em um ambiente de standby)  
  **Serviços correlacionados**: [AWS Trusted Advisor](https://aws.amazon.com/premiumsupport/trustedadvisor/), [AWS Management Console](https://aws.amazon.com/console/)

- 💾 Opções de armazenamento e características (por exemplo, durabilidade, replicação)  
  **Serviços correlacionados**: [Amazon S3](https://aws.amazon.com/s3/), [Amazon EBS](https://aws.amazon.com/ebs/), [Amazon EFS](https://aws.amazon.com/efs/)

- 👀 Visibilidade de workloads (por exemplo, [AWS X-Ray](https://aws.amazon.com/xray/))  
  **Serviços correlacionados**: [AWS X-Ray](https://aws.amazon.com/xray/), [Amazon CloudWatch](https://aws.amazon.com/cloudwatch/)

### Habilidades Necessárias

- 🛠️ Determinar estratégias de automação para garantir a integridade da infraestrutura  
  **Serviços correlacionados**: [AWS CloudFormation](https://aws.amazon.com/cloudformation/), [AWS Systems Manager](https://aws.amazon.com/systems-manager/)

- 🌍 Determinar os serviços da AWS necessários para fornecer uma arquitetura altamente disponível e/ou tolerante a falhas em Regiões da AWS ou Zonas de Disponibilidade  
  **Serviços correlacionados**: [Amazon Route 53](https://aws.amazon.com/route53/), [AWS Global Accelerator](https://aws.amazon.com/global-accelerator/), [Amazon RDS](https://aws.amazon.com/rds/)

- 📊 Identificar métricas com base nos requisitos de negócios para entregar uma solução altamente disponível  
  **Serviços correlacionados**: [Amazon CloudWatch](https://aws.amazon.com/cloudwatch/), [AWS X-Ray](https://aws.amazon.com/xray/)

- 🔄 Implementar designs para mitigar pontos únicos de falha  
  **Serviços correlacionados**: [Elastic Load Balancing](https://aws.amazon.com/elasticloadbalancing/), [Amazon Route 53](https://aws.amazon.com/route53/)

- 🔒 Implementar estratégias para garantir a durabilidade e disponibilidade dos dados (por exemplo, backups)  
  **Serviços correlacionados**: [AWS Backup](https://aws.amazon.com/backup/), [Amazon S3](https://aws.amazon.com/s3/)

- 🛠️ Selecionar uma estratégia de recuperação de desastres apropriada para atender aos requisitos de negócios  
  **Serviços correlacionados**: [AWS Backup](https://aws.amazon.com/backup/), [AWS Storage Gateway](https://aws.amazon.com/storagegateway/)

- 🚀 Usar serviços da AWS que melhorem a confiabilidade de aplicações legadas e aplicações não projetadas para a nuvem (por exemplo, quando mudanças na aplicação não são possíveis)  
  **Serviços correlacionados**: [Amazon RDS Proxy](https://aws.amazon.com/rds/proxy/), [AWS App Mesh](https://aws.amazon.com/app-mesh/)

- 🛠️ Usar serviços da AWS com propósito específico para workloads  
  **Serviços correlacionados**: [Amazon Redshift](https://aws.amazon.com/redshift/), [Amazon DynamoDB](https://aws.amazon.com/dynamodb/), [AWS Glue](https://aws.amazon.com/glue/)

### Material de estudos

<iframe src="./pdfs/Semana6.pdf" frameborder="0" width="600" height="400"></iframe>

---

Este guia abrange as principais áreas e habilidades necessárias para o Domínio 2 do exame AWS Solutions Architect Associate. Certifique-se de revisar cada área e prática para garantir uma compreensão abrangente e aplicação das melhores práticas de resiliência da AWS.

---

🔙 [Voltar ao Índice](../../../index.md)

