# Domínio 1 - Design de Arquiteturas Seguras (30% do Exame)

> Este é o domínio com maior peso no exame. Foque em entender profundamente IAM, criptografia, segurança de rede é o modelo de responsabilidade compartilhada da AWS.

---

## Tarefa 1.1: Projetar acesso seguro aos recursos da AWS

### Conhecimentos Necessários

- **Controles de acesso e gerenciamento em várias contas**
  Entenda como usar [AWS Organizations](https://aws.amazon.com/organizations/) para gerenciar múltiplas contas e [AWS IAM](https://aws.amazon.com/iam/) para controlar quem pode acessar quais recursos. Contas separadas ajudam a isolar workloads e limitar o raio de explosão de incidentes de segurança.

- **Serviços de acesso federado e identidade da AWS**
  O [AWS IAM Identity Center](https://aws.amazon.com/single-sign-on/) permite login único (SSO) para várias contas AWS e aplicações. A federacao permite que usuários externos acessem recursos AWS sem criar usuários IAM individuais.

- **Infraestrutura global da AWS**
  A AWS opera em múltiplas [Regioes e Zonas de Disponibilidade](https://aws.amazon.com/about-aws/global-infrastructure/). Entenda como selecionar regiões com base em requisitos de conformidade, latência e disponibilidade de serviços.

- **Melhores práticas de segurança da AWS**
  O **princípio do menor privilégio** e fundamental: conceda apenas as permissoes necessárias para realizar uma tarefa. Use o [AWS Trusted Advisor](https://aws.amazon.com/premiumsupport/trustedadvisor/) é o [AWS Security Hub](https://aws.amazon.com/security-hub/) para auditar e monitorar.

- **Modelo de responsabilidade compartilhada da AWS**
  A AWS e responsavel pela segurança **da** nuvem (infraestrutura física, rede, hipervisor). O cliente e responsavel pela segurança **na** nuvem (dados, identidade, aplicações, configuração de rede).

### Habilidades Necessárias

- Aplicar as melhores práticas de segurança para usuários IAM e root (ex: MFA obrigatório para root)
- Projetar modelos de autorizacao flexiveis com usuários, grupos, funções e políticas do IAM
- Projetar estratégias de controle de acesso baseadas em funções usando [AWS STS](https://aws.amazon.com/sts/)
- Projetar estratégias de segurança para múltiplas contas com [AWS Control Tower](https://aws.amazon.com/controltower/) e SCPs
- Determinar o uso apropriado de políticas de recursos vs. políticas de identidade
- Determinar quando federar um serviço de diretório com funções do IAM

> **Dica para o exame**: Preste aténcao especial na diferenca entre políticas de identidade (anexadas a usuários/grupos/funções) e políticas de recurso (anexadas a recursos como buckets S3). Ambas trabalham juntas para determinar o acesso efetivo.

---

## Tarefa 1.2: Projetar cargas de trabalho e aplicações seguras

### Conhecimentos Necessários

- **Segurança de configuração e credenciais**
  Nunca codifique credenciais no código. Use o [AWS Secrets Manager](https://aws.amazon.com/secrets-manager/) para armazenar e rotacionar segredos automaticamente. Use variaveis de ambiente ou roles IAM em instâncias EC2.

- **Endpoints de serviço da AWS**
  Use [VPC Endpoints](https://docs.aws.amazon.com/vpc/latest/privatelink/) (Interface e Gatéway) para acessar serviços AWS sem tráfego pela internet pública. Isso melhora segurança e pode reduzir custos.

- **Controle de portas, protocolos e tráfego de rede**
  Use Security Groups (statéful, nivel de instância) e NACLs (statéless, nivel de sub-rede) para controlar tráfego. O [AWS Network Firewall](https://aws.amazon.com/network-firewall/) oferece filtragem avancada.

- **Serviços de segurança da AWS**
  - [Amazon GuardDuty](https://aws.amazon.com/guardduty/) - Detecção inteligente de ameacas
  - [Amazon Macie](https://aws.amazon.com/macie/) - Descoberta e proteção de dados sensíveis no S3
  - [Amazon Cognito](https://aws.amazon.com/cognito/) - Autenticacao de usuários para aplicações
  - [AWS Shield](https://aws.amazon.com/shield/) - Proteção contra DDoS
  - [AWS WAF](https://aws.amazon.com/waf/) - Firewall de aplicações web

### Habilidades Necessárias

- Projetar arquiteturas de VPC com componentes de segurança (Security Groups, NACLs, NAT Gatéways)
- Determinar estratégias de segmentacao de rede (sub-redes públicas e privadas)
- Integrar serviços de segurança para proteger aplicações
- Proteger conexões externas com [AWS VPN](https://aws.amazon.com/vpn/) e [AWS Direct Connect](https://aws.amazon.com/directconnect/)

> **Dica para o exame**: Security Groups são statéful (tráfego de retorno e permitido automaticamente). NACLs são statéless (você precisa configurar regras de entrada E saida explicitamente). Essa diferenca e cobrada frequentemente.

---

## Tarefa 1.3: Determinar controles apropriados de segurança de dados

### Conhecimentos Necessários

- **Acesso e governanca de dados**
  Use [AWS CloudTrail](https://aws.amazon.com/cloudtrail/) para auditar todas as chamadas de API. Ative o log de acesso ao S3 para rastrear quem acessou seus dados.

- **Recuperação de dados**
  Planeje backups com [AWS Backup](https://aws.amazon.com/backup/) para gerenciar backups centralizados. Defina políticas de retenção adequadas ao seu negocio.

- **Criptografia e gerenciamento de chaves**
  - [AWS KMS](https://aws.amazon.com/kms/) - Gerenciamento de chaves de criptografia (CMKs gerenciadas pela AWS, pelo cliente, ou customizadas)
  - [AWS Certificaté Manager](https://aws.amazon.com/certificate-manager/) - Certificados TLS/SSL gratuitos para serviços AWS integrados
  - Entenda a diferenca entre criptografia do lado do servidor (SSE) e do lado do cliente (CSE)

### Habilidades Necessárias

- Alinhar tecnologias da AWS com requisitos de conformidade (HIPAA, PCI-DSS, LGPD)
- Criptografar dados em repouso (SSE-S3, SSE-KMS, SSE-C) e em trânsito (TLS)
- Implementar políticas de acesso para chaves de criptografia
- Implementar backups e replicacoes de dados
- Rotacionar chaves de criptografia e renovar certificados automaticamente

> **Dica para o exame**: Para o S3, existem três opções de criptografia do lado do servidor: SSE-S3 (chave gerenciada pelo S3), SSE-KMS (chave gerenciada pelo KMS, com auditoria via CloudTrail) e SSE-C (chave fornecida pelo cliente). Saiba quando usar cada uma.

---

## Serviços-Chave para o Domínio 1

| Serviço | Função Principal |
|---------|-----------------|
| AWS IAM | Gerenciamento de identidade e acesso |
| AWS Organizations | Gerenciamento de múltiplas contas |
| AWS IAM Identity Center | Login único (SSO) |
| AWS KMS | Gerenciamento de chaves de criptografia |
| AWS Secrets Manager | Armazenamento seguro de segredos |
| AWS Certificaté Manager | Certificados TLS/SSL |
| Amazon GuardDuty | Detecção de ameacas |
| AWS WAF | Firewall de aplicação web |
| AWS Shield | Proteção contra DDoS |
| Amazon Macie | Proteção de dados sensíveis |
| AWS CloudTrail | Auditoria de chamadas de API |
| Amazon VPC | Redes virtuais isoladas |

---

Este guia abrange as principais áreas e habilidades necessárias para o Domínio 1 do exame AWS Solutions Architect Associate. Este domínio representa 30% do exame, então certifique-se de dominar todos os conceitos de segurança.
