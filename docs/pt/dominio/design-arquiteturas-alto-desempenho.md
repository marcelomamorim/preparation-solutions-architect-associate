# 🚀 Guia do Exame: Domínio 3 - Design de Arquiteturas de Alto Desempenho

## 🎯 Tarefa 3.1: Determinar soluções de armazenamento de alto desempenho e/ou escaláveis

### Conhecimentos Necessários

- 💾 Soluções de armazenamento híbrido para atender aos requisitos de negócios
  - **Serviços correlacionados**: Amazon S3, AWS Storage Gateway
- 📦 Serviços de armazenamento com casos de uso apropriados (por exemplo, Amazon S3, Amazon Elastic File System [Amazon EFS], Amazon Elastic Block Store [Amazon EBS])
  - **Serviços correlacionados**: Amazon S3, Amazon EFS, Amazon EBS
- 📂 Tipos de armazenamento com características associadas (por exemplo, objeto, arquivo, bloco)
  - **Serviços correlacionados**: Amazon S3 (objeto), Amazon EFS (arquivo), Amazon EBS (bloco)

### Habilidades Necessárias

- 🛠️ Determinar serviços de armazenamento e configurações que atendam às demandas de desempenho
  - **Serviços correlacionados**: Amazon S3, Amazon EBS, Amazon EFS
- 📈 Determinar serviços de armazenamento que possam escalar para acomodar necessidades futuras
  - **Serviços correlacionados**: Amazon S3, Amazon EFS

---

## 🎯 Tarefa 3.2: Projetar soluções de computação elásticas e de alto desempenho

### Conhecimentos Necessários

- ⚙️ Serviços de computação da AWS com casos de uso apropriados (por exemplo, AWS Batch, Amazon EMR, Fargate)
  - **Serviços correlacionados**: AWS Batch, Amazon EMR, AWS Fargate
- 🌍 Conceitos de computação distribuída suportados pela infraestrutura global da AWS e serviços de borda
  - **Serviços correlacionados**: Amazon CloudFront, AWS Global Accelerator
- 📬 Conceitos de filas e mensagens (por exemplo, public/subscribe)
  - **Serviços correlacionados**: Amazon SQS, Amazon SNS
- ⚖️ Capacidades de escalabilidade com casos de uso apropriados (por exemplo, Amazon EC2 Auto Scaling, AWS Auto Scaling)
  - **Serviços correlacionados**: Amazon EC2 Auto Scaling, AWS Auto Scaling
- 🚀 Tecnologias e padrões serverless (por exemplo, Lambda, Fargate)
  - **Serviços correlacionados**: AWS Lambda, AWS Fargate
- 🛠️ Orquestração de containers (por exemplo, Amazon ECS, Amazon EKS)
  - **Serviços correlacionados**: Amazon ECS, Amazon EKS

### Habilidades Necessárias

- 🔄 Desacoplar workloads para que os componentes possam escalar independentemente
  - **Serviços correlacionados**: Amazon SQS, Amazon SNS
- 📊 Identificar métricas e condições para realizar ações de escalabilidade
  - **Serviços correlacionados**: Amazon CloudWatch
- 🛠️ Selecionar as opções de computação e recursos adequados (por exemplo, tipos de instância EC2) para atender aos requisitos de negócios
  - **Serviços correlacionados**: Amazon EC2
- 📏 Selecionar o tipo e tamanho de recurso apropriado (por exemplo, quantidade de memória Lambda) para atender aos requisitos de negócios
  - **Serviços correlacionados**: AWS Lambda

---

## 🎯 Tarefa 3.3: Determinar soluções de banco de dados de alto desempenho

### Conhecimentos Necessários

- 🌍 Infraestrutura global da AWS (por exemplo, Zonas de Disponibilidade, Regiões da AWS)
  - **Serviços correlacionados**: Amazon RDS, Amazon DynamoDB
- 💾 Estratégias e serviços de cache (por exemplo, Amazon ElastiCache)
  - **Serviços correlacionados**: Amazon ElastiCache
- 📈 Padrões de acesso a dados (por exemplo, leitura intensiva versus escrita intensiva)
  - **Serviços correlacionados**: Amazon RDS, Amazon DynamoDB
- 📊 Planejamento de capacidade de banco de dados (por exemplo, unidades de capacidade, tipos de instância, IOPS provisionados)
  - **Serviços correlacionados**: Amazon RDS, Amazon DynamoDB
- 🔄 Conexões de banco de dados e proxies
  - **Serviços correlacionados**: Amazon RDS Proxy
- ⚙️ Motores de banco de dados com casos de uso apropriados (por exemplo, migrações heterogêneas, migrações homogêneas)
  - **Serviços correlacionados**: Amazon Aurora, Amazon RDS
- 🔄 Replicação de banco de dados (por exemplo, réplicas de leitura)
  - **Serviços correlacionados**: Amazon RDS
- 📊 Tipos e serviços de banco de dados (por exemplo, serverless, relacional versus não relacional, in-memory)
  - **Serviços correlacionados**: Amazon Aurora, Amazon DynamoDB, Amazon ElastiCache

### Habilidades Necessárias

- 📊 Configurar réplicas de leitura para atender aos requisitos de negócios
  - **Serviços correlacionados**: Amazon RDS
- 🛠️ Projetar arquiteturas de banco de dados
  - **Serviços correlacionados**: Amazon RDS, Amazon DynamoDB
- 📊 Determinar um motor de banco de dados apropriado (por exemplo, MySQL versus PostgreSQL)
  - **Serviços correlacionados**: Amazon RDS
- 📊 Determinar um tipo de banco de dados apropriado (por exemplo, Amazon Aurora, Amazon DynamoDB)
  - **Serviços correlacionados**: Amazon Aurora, Amazon DynamoDB
- 🔄 Integrar caching para atender aos requisitos de negócios
  - **Serviços correlacionados**: Amazon ElastiCache

---

## 🎯 Tarefa 3.4: Determinar arquiteturas de rede de alto desempenho e/ou escaláveis

### Conhecimentos Necessários

- 🌍 Serviços de rede de borda com casos de uso apropriados (por exemplo, Amazon CloudFront, AWS Global Accelerator)
  - **Serviços correlacionados**: Amazon CloudFront, AWS Global Accelerator
- 🛠️ Como projetar arquitetura de rede (por exemplo, níveis de sub-rede, roteamento, endereçamento IP)
  - **Serviços correlacionados**: Amazon VPC
- ⚖️ Conceitos de balanceamento de carga (por exemplo, Application Load Balancer)
  - **Serviços correlacionados**: Elastic Load Balancing
- 🌐 Opções de conexão de rede (por exemplo, AWS VPN, Direct Connect, AWS PrivateLink)
  - **Serviços correlacionados**: AWS VPN, AWS Direct Connect, AWS PrivateLink

### Habilidades Necessárias

- 🛠️ Criar uma topologia de rede para várias arquiteturas (por exemplo, global, híbrida, multi-tier)
  - **Serviços correlacionados**: Amazon VPC
- 📈 Determinar configurações de rede que possam escalar para acomodar necessidades futuras
  - **Serviços correlacionados**: Amazon VPC, AWS Direct Connect
- 📍 Determinar o posicionamento apropriado dos recursos para atender aos requisitos de negócios
  - **Serviços correlacionados**: Amazon VPC, Amazon CloudFront
- ⚖️ Selecionar a estratégia de balanceamento de carga apropriada
  - **Serviços correlacionados**: Elastic Load Balancing

---

## 🎯 Tarefa 3.5: Determinar soluções de ingestão e transformação de dados de alto desempenho

### Conhecimentos Necessários

- 📊 Serviços de análise e visualização de dados com casos de uso apropriados (por exemplo, Amazon Athena, AWS Lake Formation, Amazon QuickSight)
  - **Serviços correlacionados**: Amazon Athena, AWS Lake Formation, Amazon QuickSight
- 🔄 Padrões de ingestão de dados (por exemplo, frequência)
  - **Serviços correlacionados**: Amazon Kinesis, AWS DataSync
- 📦 Serviços de transferência de dados com casos de uso apropriados (por exemplo, AWS DataSync, AWS Storage Gateway)
  - **Serviços correlacionados**: AWS DataSync, AWS Storage Gateway
- 🔄 Serviços de transformação de dados com casos de uso apropriados (por exemplo, AWS Glue)
  - **Serviços correlacionados**: AWS Glue
- 🔒 Acesso seguro aos pontos de ingestão
  - **Serviços correlacionados**: AWS Secrets Manager
- 📏 Tamanhos e velocidades necessários para atender aos requisitos de negócios
  - **Serviços correlacionados**: Amazon Kinesis, AWS DataSync
- 🔄 Serviços de streaming de dados com casos de uso apropriados (por exemplo, Amazon Kinesis)
  - **Serviços correlacionados**: Amazon Kinesis

### Habilidades Necessárias

- 📊 Construir e proteger data lakes
  - **Serviços correlacionados**: AWS Lake Formation, Amazon S3
- 🛠️ Projetar arquiteturas de streaming de dados
  - **Serviços correlacionados**: Amazon Kinesis
- 🔄 Projetar soluções de transferência de dados
  - **Serviços correlacionados**: AWS DataSync, AWS Storage Gateway
- 📊 Implementar estratégias de visualização
  - **Serviços correlacionados**: Amazon QuickSight
- 🛠️ Selecionar opções de computação apropriadas para processamento de dados (por exemplo, Amazon EMR)
  - **Serviços correlacionados**: Amazon EMR
- 📏 Selecionar configurações apropriadas para ingestão
  - **Serviços correlacionados**: Amazon Kinesis
- 🔄 Transformar dados entre formatos (por exemplo, .csv para .parquet)
  - **Serviços correlacionados**: AWS Glue

---

Este guia abrange as principais áreas e habilidades necessárias para o Domínio 3 do exame AWS Solutions Architect Associate. Certifique-se de revisar cada área e prática para garantir uma compreensão abrangente e aplicação das melhores práticas de desempenho da AWS.
