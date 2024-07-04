# 📋 Guia do Exame: Domínio 1 - Design de Arquiteturas Seguras

## 🛡️ Tarefa 1.1: Projetar acesso seguro aos recursos da AWS

### Conhecimentos Necessários

- 🔐 Controles de acesso e gerenciamento em várias contas
  - **Serviços correlacionados**: AWS Identity and Access Management (IAM), AWS Organizations
- 🛡️ Serviços de acesso federado e identidade da AWS (por exemplo, AWS Identity and Access Management [IAM], AWS IAM Identity Center [AWS Single Sign-On])
  - **Serviços correlacionados**: AWS IAM, AWS IAM Identity Center (AWS Single Sign-On)
- 🌍 Infraestrutura global da AWS (por exemplo, Zonas de Disponibilidade, Regiões da AWS)
  - **Serviços correlacionados**: Amazon VPC, AWS CloudFormation
- 📜 Melhores práticas de segurança da AWS (por exemplo, princípio do menor privilégio)
  - **Serviços correlacionados**: AWS Trusted Advisor, AWS Security Hub
- 🤝 Modelo de responsabilidade compartilhada da AWS
  - **Serviços correlacionados**: AWS Management Console, AWS CloudTrail

### Habilidades Necessárias

- 🛡️ Aplicar as melhores práticas de segurança da AWS para usuários IAM e usuários root (por exemplo, autenticação multifator [MFA])
  - **Serviços correlacionados**: AWS IAM, AWS Security Hub
- 🧩 Projetar um modelo de autorização flexível que inclua usuários, grupos, funções e políticas do IAM
  - **Serviços correlacionados**: AWS IAM, AWS Organizations
- 🎛️ Projetar uma estratégia de controle de acesso baseada em funções (por exemplo, AWS Security Token Service [AWS STS], troca de funções, acesso entre contas)
  - **Serviços correlacionados**: AWS IAM, AWS STS
- 🏢 Projetar uma estratégia de segurança para múltiplas contas da AWS (por exemplo, AWS Control Tower, políticas de controle de serviço [SCPs])
  - **Serviços correlacionados**: AWS Control Tower, AWS Organizations
- 🔒 Determinar o uso apropriado de políticas de recursos para serviços da AWS
  - **Serviços correlacionados**: AWS IAM, AWS Resource Access Manager (RAM)
- 🗂️ Determinar quando federar um serviço de diretório com funções do IAM
  - **Serviços correlacionados**: AWS IAM, AWS Directory Service

---

## 🛠️ Tarefa 1.2: Projetar cargas de trabalho e aplicações seguras

### Conhecimentos Necessários

- 🔧 Segurança de configuração e credenciais da aplicação
  - **Serviços correlacionados**: AWS Secrets Manager, AWS IAM
- 🌐 Endpoints de serviço da AWS
  - **Serviços correlacionados**: Amazon VPC, AWS Direct Connect
- 🚪 Controle de portas, protocolos e tráfego de rede na AWS
  - **Serviços correlacionados**: Amazon VPC, AWS Network Firewall
- 🔑 Acesso seguro à aplicação
  - **Serviços correlacionados**: Amazon Cognito, AWS IAM
- 🛡️ Serviços de segurança com casos de uso apropriados (por exemplo, Amazon Cognito, Amazon GuardDuty, Amazon Macie)
  - **Serviços correlacionados**: Amazon Cognito, Amazon GuardDuty, Amazon Macie
- 🚨 Vetores de ameaça externos à AWS (por exemplo, DDoS, injeção de SQL)
  - **Serviços correlacionados**: AWS Shield, AWS WAF

### Habilidades Necessárias

- 🛠️ Projetar arquiteturas de VPC com componentes de segurança (por exemplo, grupos de segurança, tabelas de rotas, ACLs de rede, gateways NAT)
  - **Serviços correlacionados**: Amazon VPC, AWS Network Firewall
- 🌐 Determinar estratégias de segmentação de rede (por exemplo, uso de sub-redes públicas e privadas)
  - **Serviços correlacionados**: Amazon VPC
- 🔗 Integrar serviços da AWS para proteger aplicações (por exemplo, AWS Shield, AWS WAF, IAM Identity Center, AWS Secrets Manager)
  - **Serviços correlacionados**: AWS Shield, AWS WAF, AWS Secrets Manager
- 🔒 Proteger conexões de rede externas para e da Nuvem AWS (por exemplo, VPN, AWS Direct Connect)
  - **Serviços correlacionados**: AWS Site-to-Site VPN, AWS Direct Connect

---

## 🔒 Tarefa 1.3: Determinar controles apropriados de segurança de dados

### Conhecimentos Necessários

- 🗄️ Acesso e governança de dados
  - **Serviços correlacionados**: AWS IAM, AWS CloudTrail
- 🛠️ Recuperação de dados
  - **Serviços correlacionados**: AWS Backup, AWS Storage Gateway
- 📂 Retenção e classificação de dados
  - **Serviços correlacionados**: Amazon S3, Amazon Macie
- 🗝️ Criptografia e gerenciamento apropriado de chaves
  - **Serviços correlacionados**: AWS Key Management Service (KMS), AWS Certificate Manager (ACM)

### Habilidades Necessárias

- ✅ Alinhar tecnologias da AWS para atender aos requisitos de conformidade
  - **Serviços correlacionados**: AWS Config, AWS Audit Manager
- 🔐 Criptografar dados em repouso (por exemplo, AWS Key Management Service [AWS KMS])
  - **Serviços correlacionados**: AWS KMS, Amazon S3 (Server-Side Encryption)
- 🔒 Criptografar dados em trânsito (por exemplo, AWS Certificate Manager [ACM] usando TLS)
  - **Serviços correlacionados**: AWS Certificate Manager (ACM)
- 🛡️ Implementar políticas de acesso para chaves de criptografia
  - **Serviços correlacionados**: AWS IAM, AWS KMS
- 💾 Implementar backups e replicações de dados
  - **Serviços correlacionados**: AWS Backup, AWS Storage Gateway
- 📝 Implementar políticas para acesso, ciclo de vida e proteção de dados
  - **Serviços correlacionados**: AWS IAM, Amazon S3 (Lifecycle Policies)
- 🔄 Rotacionar chaves de criptografia e renovar certificados
  - **Serviços correlacionados**: AWS KMS, AWS Certificate Manager (ACM)

---

Este guia abrange as principais áreas e habilidades necessárias para o Domínio 1 do exame AWS Solutions Architect Associate. Certifique-se de revisar cada área e prática para garantir uma compreensão abrangente e aplicação das melhores práticas de segurança da AWS.
