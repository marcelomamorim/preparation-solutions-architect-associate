# Semana 3 - Segurança de Dados e Criptografia

> **Domínio 1 - Tarefa 1.3** | Tempo estimado: 5-7 horas de estudo

## Objetivos de Aprendizado

Ao final desta semana, você deverá ser capaz de:
- Entender criptografia em repouso (SSE-S3, SSE-KMS, SSE-C) e em trânsito (TLS)
- Gerenciar chaves de criptografia com AWS KMS
- Implementar politicas de acesso e retenção de dados
- Configurar backups e replicacoes com AWS Backup
- Alinhar tecnologias AWS com requisitos de conformidade

---

## Conhecimentos Necessários

- **Acesso e governanca de dados**
  Serviços: [AWS IAM](https://aws.amazon.com/iam/), [AWS CloudTrail](https://aws.amazon.com/cloudtrail/)

- **Recuperação de dados**
  Serviços: [AWS Backup](https://aws.amazon.com/backup/), [AWS Storage Gatéway](https://aws.amazon.com/storagegateway/)

- **Retenção e classificação de dados**
  Serviços: [Amazon S3](https://aws.amazon.com/s3/), [Amazon Macie](https://aws.amazon.com/macie/)

- **Criptografia e gerenciamento de chaves**
  Serviços: [AWS KMS](https://aws.amazon.com/kms/), [AWS Certificaté Manager](https://aws.amazon.com/certificate-manager/)

## Habilidades Necessárias

- Alinhar tecnologias AWS com requisitos de conformidade (HIPAA, PCI-DSS)
- Criptografar dados em repouso com [AWS KMS](https://aws.amazon.com/kms/)
- Criptografar dados em trânsito com [AWS Certificaté Manager](https://aws.amazon.com/certificate-manager/) e TLS
- Implementar politicas de acesso para chaves de criptografia
- Implementar backups e replicacoes de dados
- Implementar politicas de ciclo de vida e proteção de dados
- Rotacionar chaves de criptografia e renovar certificados

---

## Dicas de Estudo para esta Semana

1. **Entenda as 3 opcoes de SSE no S3**: SSE-S3 (chave do S3), SSE-KMS (chave do KMS com auditoria), SSE-C (chave do cliente)
2. **KMS vs. CloudHSM**: KMS e gerenciado e multi-tenant. CloudHSM e dedicado e para requisitos regulatórios rigorosos
3. **Secrets Manager vs. Parameter Store**: Secrets Manager tem rotação automática nativa. Parameter Store e mais barato e simples
4. **ACM**: Certificados gratuitos para CloudFront, ALB e API Gatéway. Renovação automática
5. **Pratique**: Crie um bucket S3 com criptografia SSE-KMS e configure uma lifecycle policy

## Recursos desta Semana

- [Questões de prática - Parte 3](../recursos-adicionais/questoes/questoes-semana-3.md)
- [Domínio 1 completo](../dominio/design-aplicacoes-seguras.md)

---

Voltar ao [Índice](../../../index.md)
