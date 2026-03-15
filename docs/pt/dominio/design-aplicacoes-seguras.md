# Dominio 1 - Design de Arquiteturas Seguras (30% do Exame)

> Este e o dominio com maior peso no exame. Foque em entender profundamente IAM, criptografia, seguranca de rede e o modelo de responsabilidade compartilhada da AWS.

---

## Tarefa 1.1: Projetar acesso seguro aos recursos da AWS

### Conhecimentos Necessarios

- **Controles de acesso e gerenciamento em varias contas**
  Entenda como usar [AWS Organizations](https://aws.amazon.com/organizations/) para gerenciar multiplas contas e [AWS IAM](https://aws.amazon.com/iam/) para controlar quem pode acessar quais recursos. Contas separadas ajudam a isolar workloads e limitar o raio de explosao de incidentes de seguranca.

- **Servicos de acesso federado e identidade da AWS**
  O [AWS IAM Identity Center](https://aws.amazon.com/single-sign-on/) permite login unico (SSO) para varias contas AWS e aplicacoes. A federacao permite que usuarios externos acessem recursos AWS sem criar usuarios IAM individuais.

- **Infraestrutura global da AWS**
  A AWS opera em multiplas [Regioes e Zonas de Disponibilidade](https://aws.amazon.com/about-aws/global-infrastructure/). Entenda como selecionar regioes com base em requisitos de conformidade, latencia e disponibilidade de servicos.

- **Melhores praticas de seguranca da AWS**
  O **principio do menor privilegio** e fundamental: conceda apenas as permissoes necessarias para realizar uma tarefa. Use o [AWS Trusted Advisor](https://aws.amazon.com/premiumsupport/trustedadvisor/) e o [AWS Security Hub](https://aws.amazon.com/security-hub/) para auditar e monitorar.

- **Modelo de responsabilidade compartilhada da AWS**
  A AWS e responsavel pela seguranca **da** nuvem (infraestrutura fisica, rede, hipervisor). O cliente e responsavel pela seguranca **na** nuvem (dados, identidade, aplicacoes, configuracao de rede).

### Habilidades Necessarias

- Aplicar as melhores praticas de seguranca para usuarios IAM e root (ex: MFA obrigatorio para root)
- Projetar modelos de autorizacao flexiveis com usuarios, grupos, funcoes e politicas do IAM
- Projetar estrategias de controle de acesso baseadas em funcoes usando [AWS STS](https://aws.amazon.com/sts/)
- Projetar estrategias de seguranca para multiplas contas com [AWS Control Tower](https://aws.amazon.com/controltower/) e SCPs
- Determinar o uso apropriado de politicas de recursos vs. politicas de identidade
- Determinar quando federar um servico de diretorio com funcoes do IAM

> **Dica para o exame**: Preste atencao especial na diferenca entre politicas de identidade (anexadas a usuarios/grupos/funcoes) e politicas de recurso (anexadas a recursos como buckets S3). Ambas trabalham juntas para determinar o acesso efetivo.

---

## Tarefa 1.2: Projetar cargas de trabalho e aplicacoes seguras

### Conhecimentos Necessarios

- **Seguranca de configuracao e credenciais**
  Nunca codifique credenciais no codigo. Use o [AWS Secrets Manager](https://aws.amazon.com/secrets-manager/) para armazenar e rotacionar segredos automaticamente. Use variaveis de ambiente ou roles IAM em instancias EC2.

- **Endpoints de servico da AWS**
  Use [VPC Endpoints](https://docs.aws.amazon.com/vpc/latest/privatelink/) (Interface e Gateway) para acessar servicos AWS sem trafego pela internet publica. Isso melhora seguranca e pode reduzir custos.

- **Controle de portas, protocolos e trafego de rede**
  Use Security Groups (stateful, nivel de instancia) e NACLs (stateless, nivel de sub-rede) para controlar trafego. O [AWS Network Firewall](https://aws.amazon.com/network-firewall/) oferece filtragem avancada.

- **Servicos de seguranca da AWS**
  - [Amazon GuardDuty](https://aws.amazon.com/guardduty/) - Deteccao inteligente de ameacas
  - [Amazon Macie](https://aws.amazon.com/macie/) - Descoberta e protecao de dados sensiveis no S3
  - [Amazon Cognito](https://aws.amazon.com/cognito/) - Autenticacao de usuarios para aplicacoes
  - [AWS Shield](https://aws.amazon.com/shield/) - Protecao contra DDoS
  - [AWS WAF](https://aws.amazon.com/waf/) - Firewall de aplicacoes web

### Habilidades Necessarias

- Projetar arquiteturas de VPC com componentes de seguranca (Security Groups, NACLs, NAT Gateways)
- Determinar estrategias de segmentacao de rede (sub-redes publicas e privadas)
- Integrar servicos de seguranca para proteger aplicacoes
- Proteger conexoes externas com [AWS VPN](https://aws.amazon.com/vpn/) e [AWS Direct Connect](https://aws.amazon.com/directconnect/)

> **Dica para o exame**: Security Groups sao stateful (trafego de retorno e permitido automaticamente). NACLs sao stateless (voce precisa configurar regras de entrada E saida explicitamente). Essa diferenca e cobrada frequentemente.

---

## Tarefa 1.3: Determinar controles apropriados de seguranca de dados

### Conhecimentos Necessarios

- **Acesso e governanca de dados**
  Use [AWS CloudTrail](https://aws.amazon.com/cloudtrail/) para auditar todas as chamadas de API. Ative o log de acesso ao S3 para rastrear quem acessou seus dados.

- **Recuperacao de dados**
  Planeje backups com [AWS Backup](https://aws.amazon.com/backup/) para gerenciar backups centralizados. Defina politicas de retencao adequadas ao seu negocio.

- **Criptografia e gerenciamento de chaves**
  - [AWS KMS](https://aws.amazon.com/kms/) - Gerenciamento de chaves de criptografia (CMKs gerenciadas pela AWS, pelo cliente, ou customizadas)
  - [AWS Certificate Manager](https://aws.amazon.com/certificate-manager/) - Certificados TLS/SSL gratuitos para servicos AWS integrados
  - Entenda a diferenca entre criptografia do lado do servidor (SSE) e do lado do cliente (CSE)

### Habilidades Necessarias

- Alinhar tecnologias da AWS com requisitos de conformidade (HIPAA, PCI-DSS, LGPD)
- Criptografar dados em repouso (SSE-S3, SSE-KMS, SSE-C) e em transito (TLS)
- Implementar politicas de acesso para chaves de criptografia
- Implementar backups e replicacoes de dados
- Rotacionar chaves de criptografia e renovar certificados automaticamente

> **Dica para o exame**: Para o S3, existem tres opcoes de criptografia do lado do servidor: SSE-S3 (chave gerenciada pelo S3), SSE-KMS (chave gerenciada pelo KMS, com auditoria via CloudTrail) e SSE-C (chave fornecida pelo cliente). Saiba quando usar cada uma.

---

## Servicos-Chave para o Dominio 1

| Servico | Funcao Principal |
|---------|-----------------|
| AWS IAM | Gerenciamento de identidade e acesso |
| AWS Organizations | Gerenciamento de multiplas contas |
| AWS IAM Identity Center | Login unico (SSO) |
| AWS KMS | Gerenciamento de chaves de criptografia |
| AWS Secrets Manager | Armazenamento seguro de segredos |
| AWS Certificate Manager | Certificados TLS/SSL |
| Amazon GuardDuty | Deteccao de ameacas |
| AWS WAF | Firewall de aplicacao web |
| AWS Shield | Protecao contra DDoS |
| Amazon Macie | Protecao de dados sensiveis |
| AWS CloudTrail | Auditoria de chamadas de API |
| Amazon VPC | Redes virtuais isoladas |

---

Este guia abrange as principais areas e habilidades necessarias para o Dominio 1 do exame AWS Solutions Architect Associate. Este dominio representa 30% do exame, entao certifique-se de dominar todos os conceitos de seguranca.
