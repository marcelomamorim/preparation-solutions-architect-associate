# 🌟 Guia de Estudo para o Exame AWS Solutions Architect Associate

## 📚 Índice

### 📅 Cronograma de 8 Semanas

| Semana                                                                                         | Conteúdo da Semana                                                                                   |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [Semana 1: Introdução e Domínio 1 - Design de Arquiteturas Resilientes (Parte 1)](#semana-1)   | [Conteúdo da Semana 1](docs/pt/agenda/semana1.md)                                                    |
| [Semana 2: Domínio 1 - Design de Arquiteturas Resilientes (Parte 2)](#semana-2)                | [Conteúdo da Semana 2](docs/pt/agenda/semana2.md)                                                    |
| [Semana 3: Domínio 1 - Design de Arquiteturas Resilientes (Parte 3)](#semana-3)                | [Conteúdo da Semana 3](docs/pt/agenda/semana3.md)                                                    |
| [Semana 4: Domínio 2 - Design de Arquiteturas de Alto Desempenho (Parte 1)](#semana-4)         | [Conteúdo da Semana 4](docs/pt/agenda/semana4.md)                                                    |
| [Semana 5: Domínio 2 - Design de Arquiteturas de Alto Desempenho (Parte 2)](#semana-5)         | [Conteúdo da Semana 5](docs/pt/agenda/semana5.md)                                                    |
| [Semana 6: Domínio 3 - Design de Aplicações Seguras e Arquiteturas](#semana-6)                 | [Conteúdo da Semana 6](docs/pt/agenda/semana6.md)                                                    |
| [Semana 7: Domínio 4 - Design de Arquiteturas Otimizadas por Custo](#semana-7)                 | [Conteúdo da Semana 7](docs/pt/agenda/semana7.md)                                                    |
| [Semana 8: Revisão Geral e Recursos Adicionais](#semana-8)                                     | [Conteúdo da Semana 8](docs/pt/agenda/semana8.md)                                                    |
| [Serviços não listados acima, mas presentes no Guia do Exame](#servicos-nao-listados)          |                                                                                                      |

### 📖 Domínios do Exame

- [Domínio 1: Design de Arquiteturas Resilientes](docs/pt/dominio/design-arquiteturas-resilientes.md)
- [Domínio 2: Design de Arquiteturas de Alto Desempenho](docs/pt/dominio/design-arquiteturas-alto-desempenho.md)
- [Domínio 3: Design de Aplicações Seguras](docs/pt/dominio/design-aplicacoes-seguras.md)
- [Domínio 4: Design de Arquiteturas Otimizadas por Custo](docs/pt/dominio/design-arquiteturas-otimizadas-custo.md)

---

## 📅 Semana 1: Introdução e Domínio 1 - Design de Arquiteturas Resilientes (Parte 1)

### Introdução ao Exame

- 📜 Visão geral da certificação: Explicação sobre a certificação AWS Solutions Architect Associate, incluindo os benefícios e requisitos.

- 🏆 Importância da certificação: Por que obter esta certificação pode ser valioso para sua carreira.

- 📋 Detalhes do exame: Informações sobre a estrutura do exame, tipos de perguntas e critérios de aprovação.

### Domínio 1: Design de Arquiteturas Resilientes

#### 1.1 Projetar uma solução de arquitetura em várias camadas

- **Conhecimento Avaliado**: Compreender como dividir a aplicação em várias camadas para aumentar a resiliência e a segurança.

- **Serviços correlacionados**: Amazon EC2, Amazon RDS, Amazon S3, Elastic Load Balancing, Amazon VPC

---

## 📅 Semana 2: Domínio 1 - Design de Arquiteturas Resilientes (Parte 2)

#### 1.2 Projetar arquiteturas altamente disponíveis e/ou tolerantes a falhas

- **Conhecimento Avaliado**: Entender como implementar soluções que garantem alta disponibilidade e resiliência a falhas.

- **Serviços correlacionados**: Amazon EC2 Auto Scaling, Amazon Route 53, Amazon S3, Amazon RDS, Elastic Load Balancing

#### 1.3 Projetar mecanismos de desacoplamento usando serviços AWS

- **Conhecimento Avaliado**: Utilizar serviços de mensagens e orquestração para desacoplar componentes da aplicação.

- **Serviços correlacionados**: Amazon SQS, Amazon SNS, Amazon EventBridge, AWS Step Functions

---

## 📅 Semana 3: Domínio 1 - Design de Arquiteturas Resilientes (Parte 3)

#### 1.4 Escolher armazenamento resiliente apropriado

- **Conhecimento Avaliado**: Selecionar as opções de armazenamento da AWS que melhor suportam a resiliência e a durabilidade dos dados.

- **Serviços correlacionados**: Amazon S3, Amazon EBS, Amazon EFS

---

## 📅 Semana 4: Domínio 2 - Design de Arquiteturas de Alto Desempenho (Parte 1)

### Task Statement 2.1: Design scalable and loosely coupled architectures.

#### Conhecimento de:

- Criação e gestão de APIs (por exemplo, Amazon API Gateway, REST API)

- Serviços gerenciados da AWS com casos de uso apropriados (por exemplo, AWS Transfer Family, Amazon SQS, Secrets Manager)

- Estratégias de caching

- Princípios de design para microsserviços (por exemplo, cargas de trabalho sem estado comparadas com cargas de trabalho com estado)

- Arquiteturas orientadas a eventos

- Escalonamento horizontal e vertical

- Uso apropriado de aceleradores de borda (por exemplo, CDN)

- Migração de aplicações para contêineres

- Conceitos de balanceamento de carga (por exemplo, Application Load Balancer)

- Arquiteturas de várias camadas

- Conceitos de enfileiramento e mensagens (por exemplo, publish/subscribe)

- Tecnologias e padrões serverless (por exemplo, AWS Fargate, AWS Lambda)

- Tipos de armazenamento com características associadas (por exemplo, objeto, arquivo, bloco)

- Orquestração de contêineres (por exemplo, Amazon ECS, Amazon EKS)

- Quando usar réplicas de leitura

- Orquestração de fluxos de trabalho (por exemplo, AWS Step Functions)

- **Serviços correlacionados**: Amazon API Gateway, AWS Transfer Family, Amazon SQS, AWS Secrets Manager, AWS Fargate, AWS Lambda, Amazon ECS, Amazon EKS, AWS Step Functions

---

## 📅 Semana 5: Domínio 2 - Design de Arquiteturas de Alto Desempenho (Parte 2)

### Task Statement 2.2: Design highly available and/or fault-tolerant architectures.

#### Conhecimento de:

- Infraestrutura global da AWS (por exemplo, Zonas de Disponibilidade, Regiões AWS, Amazon Route 53)

- Serviços gerenciados da AWS com casos de uso apropriados (por exemplo, Amazon Comprehend, Amazon Polly)

- Conceitos básicos de redes (por exemplo, tabelas de rotas)

- Estratégias de recuperação de desastres (por exemplo, backup e restauração, piloto leve, standby quente, failover ativo-ativo, RPO, RTO)

- Padrões de design distribuído

- Estratégias de failover

- Infraestrutura imutável

- Conceitos de balanceamento de carga (por exemplo, Application Load Balancer)

- Conceitos de proxy (por exemplo, Amazon RDS Proxy)

- Quotas de serviço e limitação (por exemplo, como configurar as quotas de serviço para uma carga de trabalho em um ambiente de standby)

- Opções de armazenamento e características (por exemplo, durabilidade, replicação)

- Visibilidade da carga de trabalho (por exemplo, AWS X-Ray)

- **Serviços correlacionados**: Amazon Route 53, Amazon Comprehend, Amazon Polly, Amazon RDS Proxy, AWS X-Ray, AWS CloudTrail, Amazon S3, Amazon RDS, Elastic Load Balancing

---

## 📅 Semana 6: Domínio 3 - Design de Aplicações Seguras e Arquiteturas

### Task Statement 1.1: Design secure access to AWS resources.

#### Conhecimento de:

- Controles de acesso e gerenciamento entre múltiplas contas

- Serviços de identidade e acesso federado da AWS (por exemplo, AWS IAM, AWS IAM Identity Center [AWS Single Sign-On])

- Infraestrutura global da AWS (por exemplo, Zonas de Disponibilidade, Regiões AWS)

- Melhores práticas de segurança da AWS (por exemplo, o princípio do menor privilégio)

- Modelo de responsabilidade compartilhada da AWS

- **Serviços correlacionados**: AWS IAM, AWS IAM Identity Center (AWS Single Sign-On), Amazon Cognito, AWS Control Tower, AWS KMS

### Task Statement 1.2: Design secure workloads and applications.

#### Conhecimento de:

- Segurança de configuração e credenciais de aplicativos

- Endpoints de serviços da AWS

- Controle de portas, protocolos e tráfego de rede na AWS

- Acesso seguro a aplicativos

- Serviços de segurança com casos de uso apropriados (por exemplo, Amazon Cognito, Amazon GuardDuty, Amazon Macie)

- Vetores de ameaça externos à AWS (por exemplo, DDoS, SQL injection)

- **Serviços correlacionados**: Amazon GuardDuty, Amazon Macie, AWS Shield, AWS WAF, AWS Secrets Manager, AWS Direct Connect

### Task Statement 1.3: Determine appropriate data security controls.

#### Conhecimento de:

- Acesso a dados e governança

- Recuperação de dados

- Retenção e classificação de dados

- Criptografia e gerenciamento de chaves apropriadas

- **Serviços correlacionados**: AWS KMS, AWS Certificate Manager, Amazon S3, AWS Backup

---

## 📅 Semana 7: Domínio 4 - Design de Arquiteturas Otimizadas por Custo

### Task Statement 4.1: Design cost-optimized storage solutions.

#### Conhecimento de:

- Opções de acesso (por exemplo, um bucket S3 com armazenamento de objeto Requester Pays)

- Funcionalidades de serviços de gerenciamento de custos da AWS (por exemplo, tags de alocação de custos, faturamento multi-conta)

- Ferramentas de gerenciamento de custos da AWS com casos de uso apropriados (por exemplo, AWS Cost Explorer, AWS Budgets, AWS Cost and Usage Report)

- Serviços de armazenamento da AWS com casos de uso apropriados (por exemplo, Amazon FSx, Amazon EFS, Amazon S3, Amazon EBS)

- Estratégias de backup

- Opções de armazenamento em bloco (por exemplo, tipos de volume HDD, tipos de volume SSD)

- Ciclos de vida de dados

- Opções de armazenamento híbrido (por exemplo, DataSync, Transfer Family, Storage Gateway)

- Padrões de acesso a armazenamento

- Tiering de armazenamento (por exemplo, tiering a frio para armazenamento de objeto)

- Tipos de armazenamento com características associadas (por exemplo, objeto, arquivo, bloco)

- **Serviços correlacionados**: Amazon S3, AWS Budgets, AWS Cost Explorer, AWS Cost and Usage Report, Amazon FSx, Amazon EFS, AWS DataSync, AWS Transfer Family, AWS Storage Gateway

### Task Statement 4.2: Design cost-optimized compute solutions.

#### Conhecimento de:

- Funcionalidades de serviços de gerenciamento de custos da AWS (por exemplo, tags de alocação de custos, faturamento multi-conta)

- Ferramentas de gerenciamento de custos da AWS com casos de uso apropriados (por exemplo, Cost Explorer, AWS Budgets, AWS Cost and Usage Report)

- Infraestrutura global da AWS (por exemplo, Zonas de Disponibilidade, Regiões AWS)

- Opções de compra da AWS (por exemplo, Spot Instances, Reserved Instances, Savings Plans)

- Estratégias de computação distribuída (por exemplo, processamento de borda)

- Opções de computação híbrida (por exemplo, AWS Outposts, AWS Snowball Edge)

- Tipos, famílias e tamanhos de instâncias (por exemplo, otimizadas para memória, otimizadas para computação, virtualização)

- Otimização da utilização de computação (por exemplo, contêineres, computação serverless, microsserviços)

- Estratégias de escalonamento (por exemplo, auto scaling, hibernação)

- **Serviços correlacionados**: Amazon EC2, AWS Lambda, AWS Fargate, AWS Outposts, AWS Snowball Edge

### Task Statement 4.3: Design cost-optimized database solutions.

#### Conhecimento de:

- Funcionalidades de serviços de gerenciamento de custos da AWS (por exemplo, tags de alocação de custos, faturamento multi-conta)

- Ferramentas de gerenciamento de custos da AWS com casos de uso apropriados (por exemplo, Cost Explorer, AWS Budgets, AWS Cost and Usage Report)

- Estratégias de caching

- Políticas de retenção de dados

- Planejamento de capacidade de banco de dados (por exemplo, unidades de capacidade)

- Conexões e proxies de banco de dados

- Motores de banco de dados com casos de uso apropriados (por exemplo, migrações heterogêneas, migrações homogêneas)

- Replicação de banco de dados (por exemplo, réplicas de leitura)

- Tipos e serviços de banco de dados (por exemplo, relacionais comparados com não-relacionais, Aurora, DynamoDB)

- **Serviços correlacionados**: Amazon RDS, Amazon DynamoDB, Amazon Aurora, Amazon ElastiCache, AWS Cost Explorer, AWS Budgets

### Task Statement 4.4: Design cost-optimized network architectures.

#### Conhecimento de:

- Funcionalidades de serviços de gerenciamento de custos da AWS (por exemplo, tags de alocação de custos, faturamento multi-conta)

- Ferramentas de gerenciamento de custos da AWS com casos de uso apropriados (por exemplo, Cost Explorer, AWS Budgets, AWS Cost and Usage Report)

- Conceitos de balanceamento de carga (por exemplo, Application Load Balancer)

- Gateways NAT (por exemplo, custos de instância NAT comparados com custos de gateway NAT)

- Conectividade de rede (por exemplo, linhas privadas, linhas dedicadas, VPNs)

- Roteamento, topologia e peering de rede (por exemplo, AWS Transit Gateway, peering VPC)

- Serviços de rede com casos de uso apropriados (por exemplo, DNS)

- **Serviços correlacionados**: AWS Direct Connect, AWS Transit Gateway, AWS VPN, AWS PrivateLink, AWS CloudFront, Elastic Load Balancing

---

## 📅 Semana 8: Revisão Geral e Recursos Adicionais

- 🔄 Revisão dos principais pontos de cada domínio: Revisão abrangente dos tópicos abordados nas semanas anteriores.

- 📚 Materiais de estudo adicionais: Recomendações de leitura e recursos adicionais para aprofundar o conhecimento.

- 📝 Exames práticos: Simulados para praticar e testar o conhecimento adquirido.

- 📄 Whitepapers da AWS: Documentos técnicos que fornecem insights e melhores práticas da AWS.

---

## Serviços não listados acima, mas presentes no Guia do Exame

- Amazon Elastic Transcoder
- Amazon Kinesis Video Streams
- AWS Application Discovery Service
- AWS Application Migration Service
- AWS DataSync
- AWS Migration Hub
- AWS Snow Family
- AWS Transfer Family
- AWS Client VPN
