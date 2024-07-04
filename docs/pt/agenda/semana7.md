# 🌟 Guia do Exame: Domínio 4 - Design de Arquiteturas Otimizadas por Custo

## 🎯 Tarefa 4.1: Projetar soluções de armazenamento otimizadas por custo

### Conhecimentos Necessários

- 🔐 Opções de acesso (por exemplo, um bucket [S3](https://aws.amazon.com/s3/) com armazenamento de objetos Requester Pays)  
  **Serviços correlacionados**: [Amazon S3](https://aws.amazon.com/s3/)

- 💲 Funcionalidades do serviço de gerenciamento de custos da AWS (por exemplo, tags de alocação de custos, faturamento de múltiplas contas)  
  **Serviços correlacionados**: [AWS Cost Explorer](https://aws.amazon.com/aws-cost-management/aws-cost-explorer/), [AWS Budgets](https://aws.amazon.com/aws-cost-management/aws-budgets/), [AWS Cost and Usage Report](https://aws.amazon.com/aws-cost-management/aws-cost-and-usage-reporting/)

- 🛠️ Ferramentas de gerenciamento de custos da AWS com casos de uso apropriados  
  **Serviços correlacionados**: [AWS Cost Explorer](https://aws.amazon.com/aws-cost-management/aws-cost-explorer/), [AWS Budgets](https://aws.amazon.com/aws-cost-management/aws-budgets/), [AWS Cost and Usage Report](https://aws.amazon.com/aws-cost-management/aws-cost-and-usage-reporting/)

- 📦 Serviços de armazenamento da AWS com casos de uso apropriados (por exemplo, [Amazon FSx](https://aws.amazon.com/fsx/), [Amazon EFS](https://aws.amazon.com/efs/), [Amazon S3](https://aws.amazon.com/s3/), [Amazon EBS](https://aws.amazon.com/ebs/))  
  **Serviços correlacionados**: [Amazon FSx](https://aws.amazon.com/fsx/), [Amazon EFS](https://aws.amazon.com/efs/), [Amazon S3](https://aws.amazon.com/s3/), [Amazon EBS](https://aws.amazon.com/ebs/)

- 🔄 Estratégias de backup  
  **Serviços correlacionados**: [AWS Backup](https://aws.amazon.com/backup/), [Amazon S3 Glacier](https://aws.amazon.com/s3/glacier/)

- 💾 Opções de armazenamento em bloco (por exemplo, tipos de volume HDD, tipos de volume SSD)  
  **Serviços correlacionados**: [Amazon EBS](https://aws.amazon.com/ebs/)

- ⏳ Ciclos de vida dos dados  
  **Serviços correlacionados**: [Amazon S3](https://aws.amazon.com/s3/)

- 📀 Opções de armazenamento híbrido (por exemplo, [DataSync](https://aws.amazon.com/datasync/), [Transfer Family](https://aws.amazon.com/aws-transfer-family/), [Storage Gateway](https://aws.amazon.com/storagegateway/))  
  **Serviços correlacionados**: [AWS DataSync](https://aws.amazon.com/datasync/), [AWS Transfer Family](https://aws.amazon.com/aws-transfer-family/), [AWS Storage Gateway](https://aws.amazon.com/storagegateway/)

- 📊 Padrões de acesso a armazenamento  
  **Serviços correlacionados**: [Amazon S3](https://aws.amazon.com/s3/), [Amazon EFS](https://aws.amazon.com/efs/)

- 🗄️ Hierarquização de armazenamento (por exemplo, tiering frio para armazenamento de objetos)  
  **Serviços correlacionados**: [Amazon S3 Glacier](https://aws.amazon.com/s3/glacier/)

- 📂 Tipos de armazenamento com características associadas (por exemplo, objeto, arquivo, bloco)  
  **Serviços correlacionados**: [Amazon S3 (objeto)](https://aws.amazon.com/s3/), [Amazon EFS (arquivo)](https://aws.amazon.com/efs/), [Amazon EBS (bloco)](https://aws.amazon.com/ebs/)

### Habilidades Necessárias

- 🛠️ Projetar estratégias de armazenamento apropriadas (por exemplo, uploads em lote para [Amazon S3](https://aws.amazon.com/s3/) em comparação com uploads individuais)  
  **Serviços correlacionados**: [Amazon S3](https://aws.amazon.com/s3/)

- 📏 Determinar o tamanho correto do armazenamento para uma carga de trabalho  
  **Serviços correlacionados**: [Amazon EBS](https://aws.amazon.com/ebs/), [Amazon S3](https://aws.amazon.com/s3/)

- 🚀 Determinar o método de menor custo para transferir dados para o armazenamento AWS  
  **Serviços correlacionados**: [AWS DataSync](https://aws.amazon.com/datasync/)

- 🔄 Determinar quando o autoescalamento de armazenamento é necessário  
  **Serviços correlacionados**: [Amazon S3](https://aws.amazon.com/s3/), [Amazon EFS](https://aws.amazon.com/efs/)

- 🗄️ Gerenciar ciclos de vida de objetos S3  
  **Serviços correlacionados**: [Amazon S3](https://aws.amazon.com/s3/)

- 📂 Selecionar a solução de backup e/ou arquivamento apropriada  
  **Serviços correlacionados**: [AWS Backup](https://aws.amazon.com/backup/), [Amazon S3 Glacier](https://aws.amazon.com/s3/glacier/)

- 🔄 Selecionar o serviço apropriado para migração de dados para serviços de armazenamento  
  **Serviços correlacionados**: [AWS DataSync](https://aws.amazon.com/datasync/)

- 🗄️ Selecionar o nível de armazenamento apropriado  
  **Serviços correlacionados**: [Amazon S3 Glacier](https://aws.amazon.com/s3/glacier/)

- 📊 Selecionar o ciclo de vida correto para o armazenamento  
  **Serviços correlacionados**: [Amazon S3](https://aws.amazon.com/s3/)

- 📦 Selecionar o serviço de armazenamento mais econômico para uma carga de trabalho  
  **Serviços correlacionados**: [Amazon S3](https://aws.amazon.com/s3/), [Amazon EBS](https://aws.amazon.com/ebs/), [Amazon EFS](https://aws.amazon.com/efs/)

---

## 🎯 Tarefa 4.2: Projetar soluções de computação otimizadas por custo

### Conhecimentos Necessários

- 💲 Funcionalidades do serviço de gerenciamento de custos da AWS (por exemplo, tags de alocação de custos, faturamento de múltiplas contas)  
  **Serviços correlacionados**: [AWS Cost Explorer](https://aws.amazon.com/aws-cost-management/aws-cost-explorer/), [AWS Budgets](https://aws.amazon.com/aws-cost-management/aws-budgets/), [AWS Cost and Usage Report](https://aws.amazon.com/aws-cost-management/aws-cost-and-usage-reporting/)

- 🛠️ Ferramentas de gerenciamento de custos da AWS com casos de uso apropriados  
  **Serviços correlacionados**: [AWS Cost Explorer](https://aws.amazon.com/aws-cost-management/aws-cost-explorer/), [AWS Budgets](https://aws.amazon.com/aws-cost-management/aws-budgets/), [AWS Cost and Usage Report](https://aws.amazon.com/aws-cost-management/aws-cost-and-usage-reporting/)

- 🌍 Infraestrutura global da AWS (por exemplo, Zonas de Disponibilidade, Regiões da AWS)  
  **Serviços correlacionados**: [Amazon EC2](https://aws.amazon.com/ec2/), [Amazon S3](https://aws.amazon.com/s3/)

- 💲 Opções de compra da AWS (por exemplo, Spot Instances, Reserved Instances, Savings Plans)  
  **Serviços correlacionados**: [Amazon EC2](https://aws.amazon.com/ec2/), [AWS Savings Plans](https://aws.amazon.com/savingsplans/)

- 🌐 Estratégias de computação distribuída (por exemplo, processamento na borda)  
  **Serviços correlacionados**: [AWS Lambda](https://aws.amazon.com/lambda/), [AWS Outposts](https://aws.amazon.com/outposts/)

- ⚙️ Opções de computação híbrida (por exemplo, [AWS Outposts](https://aws.amazon.com/outposts/), [AWS Snowball Edge](https://aws.amazon.com/snowball/edge/))  
  **Serviços correlacionados**: [AWS Outposts](https://aws.amazon.com/outposts/), [AWS Snowball Edge](https://aws.amazon.com/snowball/edge/)

- 🖥️ Tipos, famílias e tamanhos de instância (por exemplo, otimizados para memória, otimizados para computação, virtualização)  
  **Serviços correlacionados**: [Amazon EC2](https://aws.amazon.com/ec2/)

- ⚙️ Otimização da utilização de computação (por exemplo, containers, computação serverless, microsserviços)  
  **Serviços correlacionados**: [Amazon ECS](https://aws.amazon.com/ecs/), [AWS Lambda](https://aws.amazon.com/lambda/)

- 🔄 Estratégias de escalonamento (por exemplo, autoescalamento, hibernação)  
  **Serviços correlacionados**: [Amazon EC2 Auto Scaling](https://aws.amazon.com/autoscaling/)

### Habilidades Necessárias

- ⚖️ Determinar uma estratégia de balanceamento de carga apropriada (por exemplo, [Application Load Balancer](https://aws.amazon.com/elasticloadbalancing/) [Camada 7] em comparação com [Network Load Balancer](https://aws.amazon.com/elasticloadbalancing/) [Camada 4] em comparação com Gateway Load Balancer)  
  **Serviços correlacionados**: [Elastic Load Balancing](https://aws.amazon.com/elasticloadbalancing/)

- 🔄 Determinar métodos e estratégias de escalonamento apropriados para workloads elásticos (por exemplo, horizontal em comparação com vertical, hibernação de EC2)  
  **Serviços correlacionados**: [Amazon EC2 Auto Scaling](https://aws.amazon.com/autoscaling/)

- 💲 Determinar serviços de computação AWS econômicos com casos de uso apropriados (por exemplo, [Lambda](https://aws.amazon.com/lambda/), [Amazon EC2](https://aws.amazon.com/ec2/), [Fargate](https://aws.amazon.com/fargate/))  
  **Serviços correlacionados**: [AWS Lambda](https://aws.amazon.com/lambda/), [Amazon EC2](https://aws.amazon.com/ec2/), [AWS Fargate](https://aws.amazon.com/fargate/)

- 🔄 Determinar a disponibilidade necessária para diferentes classes de workloads (por exemplo, workloads de produção, workloads não-produtivos)  
  **Serviços correlacionados**: [Amazon EC2](https://aws.amazon.com/ec2/), [AWS Lambda](https://aws.amazon.com/lambda/)

- ⚙️ Selecionar a família de instâncias apropriada para uma carga de trabalho  
  **Serviços correlacionados**: [Amazon EC2](https://aws.amazon.com/ec2/)

- 📏 Selecionar o tamanho de instância apropriado para uma carga de trabalho  
  **Serviços correlacionados**: [Amazon EC2](https://aws.amazon.com/ec2/)

---

## 🎯 Tarefa 4.3: Projetar soluções de banco de dados otimizadas por custo

### Conhecimentos Necessários

- 💲 Funcionalidades do serviço de gerenciamento de custos da AWS (por exemplo, tags de alocação de custos, faturamento de múltiplas contas)  
  **Serviços correlacionados**: [AWS Cost Explorer](https://aws.amazon.com/aws-cost-management/aws-cost-explorer/), [AWS Budgets](https://aws.amazon.com/aws-cost-management/aws-budgets/), [AWS Cost and Usage Report](https://aws.amazon.com/aws-cost-management/aws-cost-and-usage-reporting/)

- 🛠️ Ferramentas de gerenciamento de custos da AWS com casos de uso apropriados  
  **Serviços correlacionados**: [AWS Cost Explorer](https://aws.amazon.com/aws-cost-management/aws-cost-explorer/), [AWS Budgets](https://aws.amazon.com/aws-cost-management/aws-budgets/), [AWS Cost and Usage Report](https://aws.amazon.com/aws-cost-management/aws-cost-and-usage-reporting/)

- 📊 Estratégias de cache  
  **Serviços correlacionados**: [Amazon ElastiCache](https://aws.amazon.com/elasticache/)

- 📜 Políticas de retenção de dados  
  **Serviços correlacionados**: [Amazon S3](https://aws.amazon.com/s3/), [Amazon RDS](https://aws.amazon.com/rds/)

- 📏 Planejamento de capacidade de banco de dados (por exemplo, unidades de capacidade)  
  **Serviços correlacionados**: [Amazon RDS](https://aws.amazon.com/rds/), [Amazon DynamoDB](https://aws.amazon.com/dynamodb/)

- 🔄 Conexões de banco de dados e proxies  
  **Serviços correlacionados**: [Amazon RDS Proxy](https://aws.amazon.com/rds/proxy/)

- ⚙️ Motores de banco de dados com casos de uso apropriados (por exemplo, migrações heterogêneas, migrações homogêneas)  
  **Serviços correlacionados**: [Amazon Aurora](https://aws.amazon.com/rds/aurora/), [Amazon RDS](https://aws.amazon.com/rds/)

- 🔄 Replicação de banco de dados (por exemplo, réplicas de leitura)  
  **Serviços correlacionados**: [Amazon RDS](https://aws.amazon.com/rds/)

- 🛠️ Tipos e serviços de banco de dados (por exemplo, relacional em comparação com não relacional, [Aurora](https://aws.amazon.com/rds/aurora/), [DynamoDB](https://aws.amazon.com/dynamodb/))  
  **Serviços correlacionados**: [Amazon Aurora](https://aws.amazon.com/rds/aurora/), [Amazon DynamoDB](https://aws.amazon.com/dynamodb/)

### Habilidades Necessárias

- 📊 Projetar políticas de backup e retenção apropriadas (por exemplo, frequência de snapshots)  
  **Serviços correlacionados**: [Amazon RDS](https://aws.amazon.com/rds/), [Amazon S3 Glacier](https://aws.amazon.com/s3/glacier/)

- 🛠️ Determinar um motor de banco de dados apropriado (por exemplo, MySQL em comparação com PostgreSQL)  
  **Serviços correlacionados**: [Amazon RDS](https://aws.amazon.com/rds/)

- 💲 Determinar serviços de banco de dados AWS econômicos com casos de uso apropriados (por exemplo, [DynamoDB](https://aws.amazon.com/dynamodb/) em comparação com [Amazon RDS](https://aws.amazon.com/rds/), serverless)  
  **Serviços correlacionados**: [Amazon DynamoDB](https://aws.amazon.com/dynamodb/), [Amazon Aurora Serverless](https://aws.amazon.com/rds/aurora/)

- 📊 Determinar tipos de banco de dados AWS econômicos (por exemplo, formato de série temporal, formato columnar)  
  **Serviços correlacionados**: [Amazon Timestream](https://aws.amazon.com/timestream/), [Amazon Redshift](https://aws.amazon.com/redshift/)

- 🔄 Migrar esquemas de banco de dados e dados para diferentes locais e/ou diferentes motores de banco de dados  
  **Serviços correlacionados**: [AWS Database Migration Service (AWS DMS)](https://aws.amazon.com/dms/)

---

## 🎯 Tarefa 4.4: Projetar arquiteturas de rede otimizadas por custo

### Conhecimentos Necessários

- 💲 Funcionalidades do serviço de gerenciamento de custos da AWS (por exemplo, tags de alocação de custos, faturamento de múltiplas contas)  
  **Serviços correlacionados**: [AWS Cost Explorer](https://aws.amazon.com/aws-cost-management/aws-cost-explorer/), [AWS Budgets](https://aws.amazon.com/aws-cost-management/aws-budgets/), [AWS Cost and Usage Report](https://aws.amazon.com/aws-cost-management/aws-cost-and-usage-reporting/)

- 🛠️ Ferramentas de gerenciamento de custos da AWS com casos de uso apropriados  
  **Serviços correlacionados**: [AWS Cost Explorer](https://aws.amazon.com/aws-cost-management/aws-cost-explorer/), [AWS Budgets](https://aws.amazon.com/aws-cost-management/aws-budgets/), [AWS Cost and Usage Report](https://aws.amazon.com/aws-cost-management/aws-cost-and-usage-reporting/)

- 📶 Conceitos de balanceamento de carga (por exemplo, [Application Load Balancer](https://aws.amazon.com/elasticloadbalancing/))  
  **Serviços correlacionados**: [Elastic Load Balancing](https://aws.amazon.com/elasticloadbalancing/)

- 🔀 Gateways NAT (por exemplo, custos de instância NAT em comparação com custos de gateway NAT)  
  **Serviços correlacionados**: [Amazon VPC](https://aws.amazon.com/vpc/)

- 🌐 Conectividade de rede (por exemplo, linhas privadas, linhas dedicadas, VPNs)  
  **Serviços correlacionados**: [AWS Direct Connect](https://aws.amazon.com/directconnect/), [AWS Site-to-Site VPN](https://aws.amazon.com/vpn/)

- 🛠️ Roteamento de rede, topologia e peering (por exemplo, [AWS Transit Gateway](https://aws.amazon.com/transit-gateway/), [VPC peering](https://docs.aws.amazon.com/vpc/latest/peering/what-is-vpc-peering.html))  
  **Serviços correlacionados**: [AWS Transit Gateway](https://aws.amazon.com/transit-gateway/), [VPC Peering](https://docs.aws.amazon.com/vpc/latest/peering/what-is-vpc-peering.html)

- 📶 Serviços de rede com casos de uso apropriados (por exemplo, DNS)  
  **Serviços correlacionados**: [Amazon Route 53](https://aws.amazon.com/route53/)

### Habilidades Necessárias

- 🛠️ Configurar tipos apropriados de gateway NAT para uma rede (por exemplo, um único gateway NAT compartilhado em comparação com gateways NAT para cada Zona de Disponibilidade)  
  **Serviços correlacionados**: [Amazon VPC](https://aws.amazon.com/vpc/)

- 🌐 Configurar conexões de rede apropriadas (por exemplo, [Direct Connect](https://aws.amazon.com/directconnect/) em comparação com [VPN](https://aws.amazon.com/vpn/) em comparação com internet)  
  **Serviços correlacionados**: [AWS Direct Connect](https://aws.amazon.com/directconnect/), [AWS Site-to-Site VPN](https://aws.amazon.com/vpn/)

- 🔄 Configurar rotas de rede apropriadas para minimizar os custos de transferência de rede (por exemplo, Região para Região, Zona de Disponibilidade para Zona de Disponibilidade, privado para público, [Global Accelerator](https://aws.amazon.com/global-accelerator/), [endpoints VPC](https://aws.amazon.com/privatelink/))  
  **Serviços correlacionados**: [AWS Global Accelerator](https://aws.amazon.com/global-accelerator/), [Amazon CloudFront](https://aws.amazon.com/cloudfront/), [AWS Transit Gateway](https://aws.amazon.com/transit-gateway/)

- 🌍 Determinar necessidades estratégicas para redes de entrega de conteúdo (CDNs) e cache na borda  
  **Serviços correlacionados**: [Amazon CloudFront](https://aws.amazon.com/cloudfront/)

- 🛠️ Revisar workloads existentes para otimizações de rede  
  **Serviços correlacionados**: [AWS Trusted Advisor](https://aws.amazon.com/premiumsupport/technology/trusted-advisor/)

- ⚖️ Selecionar uma estratégia de limitação de taxa apropriada  
  **Serviços correlacionados**: [AWS API Gateway](https://aws.amazon.com/api-gateway/)

- 📶 Selecionar a alocação de largura de banda apropriada para um dispositivo de rede (por exemplo, uma única VPN em comparação com múltiplas VPNs, velocidade do Direct Connect)  
  **Serviços correlacionados**: [AWS Direct Connect](https://aws.amazon.com/directconnect/), [AWS Site-to-Site VPN](https://aws.amazon.com/vpn/)

---

Este guia abrange as principais áreas e habilidades necessárias para o Domínio 4 do exame AWS Solutions Architect Associate. Certifique-se de revisar cada área e prática para garantir uma compreensão abrangente e aplicação das melhores práticas de otimização de custos da AWS.


---

🔙 [Voltar ao Índice](../../../index.md)
