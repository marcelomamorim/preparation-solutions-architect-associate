# 🌟 Guia do Exame: Domínio 4 - Design de Arquiteturas Otimizadas por Custo

## 🎯 Tarefa 4.1: Projetar soluções de armazenamento otimizadas por custo

### Conhecimentos Necessários

- 🔐 Opções de acesso (por exemplo, um bucket S3 com armazenamento de objetos Requester Pays)  
  **Serviços correlacionados**: Amazon S3

- 💲 Funcionalidades do serviço de gerenciamento de custos da AWS (por exemplo, tags de alocação de custos, faturamento de múltiplas contas)  
  **Serviços correlacionados**: AWS Cost Explorer, AWS Budgets, AWS Cost and Usage Report

- 🛠️ Ferramentas de gerenciamento de custos da AWS com casos de uso apropriados  
  **Serviços correlacionados**: AWS Cost Explorer, AWS Budgets, AWS Cost and Usage Report

- 📦 Serviços de armazenamento da AWS com casos de uso apropriados (por exemplo, Amazon FSx, Amazon EFS, Amazon S3, Amazon EBS)  
  **Serviços correlacionados**: Amazon FSx, Amazon EFS, Amazon S3, Amazon EBS

- 🔄 Estratégias de backup  
  **Serviços correlacionados**: AWS Backup, Amazon S3 Glacier

- 💾 Opções de armazenamento em bloco (por exemplo, tipos de volume HDD, tipos de volume SSD)  
  **Serviços correlacionados**: Amazon EBS

- ⏳ Ciclos de vida dos dados  
  **Serviços correlacionados**: Amazon S3

- 📀 Opções de armazenamento híbrido (por exemplo, DataSync, Transfer Family, Storage Gateway)  
  **Serviços correlacionados**: AWS DataSync, AWS Transfer Family, AWS Storage Gateway

- 📊 Padrões de acesso a armazenamento  
  **Serviços correlacionados**: Amazon S3, Amazon EFS

- 🗄️ Hierarquização de armazenamento (por exemplo, tiering frio para armazenamento de objetos)  
  **Serviços correlacionados**: Amazon S3 Glacier

- 📂 Tipos de armazenamento com características associadas (por exemplo, objeto, arquivo, bloco)  
  **Serviços correlacionados**: Amazon S3 (objeto), Amazon EFS (arquivo), Amazon EBS (bloco)

### Habilidades Necessárias

- 🛠️ Projetar estratégias de armazenamento apropriadas (por exemplo, uploads em lote para Amazon S3 em comparação com uploads individuais)  
  **Serviços correlacionados**: Amazon S3

- 📏 Determinar o tamanho correto do armazenamento para uma carga de trabalho  
  **Serviços correlacionados**: Amazon EBS, Amazon S3

- 🚀 Determinar o método de menor custo para transferir dados para o armazenamento AWS  
  **Serviços correlacionados**: AWS DataSync

- 🔄 Determinar quando o autoescalamento de armazenamento é necessário  
  **Serviços correlacionados**: Amazon S3, Amazon EFS

- 🗄️ Gerenciar ciclos de vida de objetos S3  
  **Serviços correlacionados**: Amazon S3

- 📂 Selecionar a solução de backup e/ou arquivamento apropriada  
  **Serviços correlacionados**: AWS Backup, Amazon S3 Glacier

- 🔄 Selecionar o serviço apropriado para migração de dados para serviços de armazenamento  
  **Serviços correlacionados**: AWS DataSync

- 🗄️ Selecionar o nível de armazenamento apropriado  
  **Serviços correlacionados**: Amazon S3 Glacier

- 📊 Selecionar o ciclo de vida correto para o armazenamento  
  **Serviços correlacionados**: Amazon S3

- 📦 Selecionar o serviço de armazenamento mais econômico para uma carga de trabalho  
  **Serviços correlacionados**: Amazon S3, Amazon EBS, Amazon EFS

---

## 🎯 Tarefa 4.2: Projetar soluções de computação otimizadas por custo

### Conhecimentos Necessários

- 💲 Funcionalidades do serviço de gerenciamento de custos da AWS (por exemplo, tags de alocação de custos, faturamento de múltiplas contas)  
  **Serviços correlacionados**: AWS Cost Explorer, AWS Budgets, AWS Cost and Usage Report

- 🛠️ Ferramentas de gerenciamento de custos da AWS com casos de uso apropriados  
  **Serviços correlacionados**: AWS Cost Explorer, AWS Budgets, AWS Cost and Usage Report

- 🌍 Infraestrutura global da AWS (por exemplo, Zonas de Disponibilidade, Regiões da AWS)  
  **Serviços correlacionados**: Amazon EC2, Amazon S3

- 💲 Opções de compra da AWS (por exemplo, Spot Instances, Reserved Instances, Savings Plans)  
  **Serviços correlacionados**: Amazon EC2, AWS Savings Plans

- 🌐 Estratégias de computação distribuída (por exemplo, processamento na borda)  
  **Serviços correlacionados**: AWS Lambda, AWS Outposts

- ⚙️ Opções de computação híbrida (por exemplo, AWS Outposts, AWS Snowball Edge)  
  **Serviços correlacionados**: AWS Outposts, AWS Snowball Edge

- 🖥️ Tipos, famílias e tamanhos de instância (por exemplo, otimizados para memória, otimizados para computação, virtualização)  
  **Serviços correlacionados**: Amazon EC2

- ⚙️ Otimização da utilização de computação (por exemplo, containers, computação serverless, microsserviços)  
  **Serviços correlacionados**: Amazon ECS, AWS Lambda

- 🔄 Estratégias de escalonamento (por exemplo, autoescalamento, hibernação)  
  **Serviços correlacionados**: Amazon EC2 Auto Scaling

### Habilidades Necessárias

- ⚖️ Determinar uma estratégia de balanceamento de carga apropriada (por exemplo, Application Load Balancer [Camada 7] em comparação com Network Load Balancer [Camada 4] em comparação com Gateway Load Balancer)  
  **Serviços correlacionados**: Elastic Load Balancing

- 🔄 Determinar métodos e estratégias de escalonamento apropriados para workloads elásticos (por exemplo, horizontal em comparação com vertical, hibernação de EC2)  
  **Serviços correlacionados**: Amazon EC2 Auto Scaling

- 💲 Determinar serviços de computação AWS econômicos com casos de uso apropriados (por exemplo, Lambda, Amazon EC2, Fargate)  
  **Serviços correlacionados**: AWS Lambda, Amazon EC2, AWS Fargate

- 🔄 Determinar a disponibilidade necessária para diferentes classes de workloads (por exemplo, workloads de produção, workloads não-produtivos)  
  **Serviços correlacionados**: Amazon EC2, AWS Lambda

- ⚙️ Selecionar a família de instâncias apropriada para uma carga de trabalho  
  **Serviços correlacionados**: Amazon EC2

- 📏 Selecionar o tamanho de instância apropriado para uma carga de trabalho  
  **Serviços correlacionados**: Amazon EC2

---

## 🎯 Tarefa 4.3: Projetar soluções de banco de dados otimizadas por custo

### Conhecimentos Necessários

- 💲 Funcionalidades do serviço de gerenciamento de custos da AWS (por exemplo, tags de alocação de custos, faturamento de múltiplas contas)  
  **Serviços correlacionados**: AWS Cost Explorer, AWS Budgets, AWS Cost and Usage Report

- 🛠️ Ferramentas de gerenciamento de custos da AWS com casos de uso apropriados  
  **Serviços correlacionados**: AWS Cost Explorer, AWS Budgets, AWS Cost and Usage Report

- 📊 Estratégias de cache  
  **Serviços correlacionados**: Amazon ElastiCache

- 📜 Políticas de retenção de dados  
  **Serviços correlacionados**: Amazon S3, Amazon RDS

- 📏 Planejamento de capacidade de banco de dados (por exemplo, unidades de capacidade)  
  **Serviços correlacionados**: Amazon RDS, Amazon DynamoDB

- 🔄 Conexões de banco de dados e proxies  
  **Serviços correlacionados**: Amazon RDS Proxy

- ⚙️ Motores de banco de dados com casos de uso apropriados (por exemplo, migrações heterogêneas, migrações homogêneas)  
  **Serviços correlacionados**: Amazon Aurora, Amazon RDS

- 🔄 Replicação de banco de dados (por exemplo, réplicas de leitura)  
  **Serviços correlacionados**: Amazon RDS

- 🛠️ Tipos e serviços de banco de dados (por exemplo, relacional em comparação com não relacional, Aurora, DynamoDB)  
  **Serviços correlacionados**: Amazon Aurora, Amazon DynamoDB

### Habilidades Necessárias

- 📊 Projetar políticas de backup e retenção apropriadas (por exemplo, frequência de snapshots)  
  **Serviços correlacionados**: Amazon RDS, Amazon S3 Glacier

- 🛠️ Determinar um motor de banco de dados apropriado (por exemplo, MySQL em comparação com PostgreSQL)  
  **Serviços correlacionados**: Amazon RDS

- 💲 Determinar serviços de banco de dados AWS econômicos com casos de uso apropriados (por exemplo, DynamoDB em comparação com Amazon RDS, serverless)  
  **Serviços correlacionados**: Amazon DynamoDB, Amazon Aurora Serverless

- 📊 Determinar tipos de banco de dados AWS econômicos (por exemplo, formato de série temporal, formato columnar)  
  **Serviços correlacionados**: Amazon Timestream, Amazon Redshift

- 🔄 Migrar esquemas de banco de dados e dados para diferentes locais e/ou diferentes motores de banco de dados  
  **Serviços correlacionados**: AWS Database Migration Service (AWS DMS)

---

## 🎯 Tarefa 4.4: Projetar arquiteturas de rede otimizadas por custo

### Conhecimentos Necessários

- 💲 Funcionalidades do serviço de gerenciamento de custos da AWS (por exemplo, tags de alocação de custos, faturamento de múltiplas contas)  
  **Serviços correlacionados**: AWS Cost Explorer, AWS Budgets, AWS Cost and Usage Report

- 🛠️ Ferramentas de gerenciamento de custos da AWS com casos de uso apropriados  
  **Serviços correlacionados**: AWS Cost Explorer, AWS Budgets, AWS Cost and Usage Report

- 📶 Conceitos de balanceamento de carga (por exemplo, Application Load Balancer)  
  **Serviços correlacionados**: Elastic Load Balancing

- 🔀 Gateways NAT (por exemplo, custos de instância NAT em comparação com custos de gateway NAT)  
  **Serviços correlacionados**: Amazon VPC

- 🌐 Conectividade de rede (por exemplo, linhas privadas, linhas dedicadas, VPNs)  
  **Serviços correlacionados**: AWS Direct Connect, AWS Site-to-Site VPN

- 🛠️ Roteamento de rede, topologia e peering (por exemplo, AWS Transit Gateway, VPC peering)  
  **Serviços correlacionados**: AWS Transit Gateway, VPC Peering

- 📶 Serviços de rede com casos de uso apropriados (por exemplo, DNS)  
  **Serviços correlacionados**: Amazon Route 53

### Habilidades Necessárias

- 🛠️ Configurar tipos apropriados de gateway NAT para uma rede (por exemplo, um único gateway NAT compartilhado em comparação com gateways NAT para cada Zona de Disponibilidade)  
  **Serviços correlacionados**: Amazon VPC

- 🌐 Configurar conexões de rede apropriadas (por exemplo, Direct Connect em comparação com VPN em comparação com internet)  
  **Serviços correlacionados**: AWS Direct Connect, AWS Site-to-Site VPN

- 🔄 Configurar rotas de rede apropriadas para minimizar os custos de transferência de rede (por exemplo, Região para Região, Zona de Disponibilidade para Zona de Disponibilidade, privado para público, Global Accelerator, endpoints VPC)  
  **Serviços correlacionados**: AWS Global Accelerator, Amazon CloudFront, AWS Transit Gateway

- 🌍 Determinar necessidades estratégicas para redes de entrega de conteúdo (CDNs) e cache na borda  
  **Serviços correlacionados**: Amazon CloudFront

- 🛠️ Revisar workloads existentes para otimizações de rede  
  **Serviços correlacionados**: AWS Trusted Advisor

- ⚖️ Selecionar uma estratégia de limitação de taxa apropriada  
  **Serviços correlacionados**: AWS API Gateway

- 📶 Selecionar a alocação de largura de banda apropriada para um dispositivo de rede (por exemplo, uma única VPN em comparação com múltiplas VPNs, velocidade do Direct Connect)  
  **Serviços correlacionados**: AWS Direct Connect, AWS Site-to-Site VPN

---

Este guia abrange as principais áreas e habilidades necessárias para o Domínio 4 do exame AWS Solutions Architect Associate. Certifique-se de revisar cada área e prática para garantir uma compreensão abrangente e aplicação das melhores práticas de otimização de custos da AWS.
