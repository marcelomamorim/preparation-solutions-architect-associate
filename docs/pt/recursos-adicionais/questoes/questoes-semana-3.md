# Questões de Prática - Parte 3: Segurança de Dados e Criptografia

> Teste seus conhecimentos sobre criptografia, KMS, proteção de dados e conformidade.

---

### Questao 1

Uma empresa precisa criptografar dados armazenados no Amazon S3 e manter controle total sobre as chaves de criptografia, incluindo auditoria de uso via CloudTrail. Qual opcao de criptografia deve ser usada?

**A)** SSE-S3 (Server-Side Encryption com chaves gerenciadas pelo S3)

**B)** SSE-KMS (Server-Side Encryption com chaves do AWS KMS)

**C)** SSE-C (Server-Side Encryption com chaves fornecidas pelo cliente)

**D)** Criptografia do lado do cliente

> **Resposta: B** - SSE-KMS oferece controle sobre as chaves de criptografia e registra cada uso da chave no CloudTrail para auditoria. SSE-S3 e mais simples mas não oferece auditoria granular. SSE-C requer que o cliente gerencie as chaves fora da AWS.

---

### Questao 2

Uma aplicação precisa armazenar credenciais de banco de dados de forma segura e rotaciona-las automáticamente a cada 30 dias. Qual serviço e mais adequado?

**A)** AWS Systems Manager Parameter Store (SecureString)

**B)** AWS Secrets Manager

**C)** AWS KMS

**D)** Amazon S3 com criptografia

> **Resposta: B** - AWS Secrets Manager foi projetado específicamente para armazenar e rotacionar segredos como credenciais de banco de dados. Oferece rotação automática nativa com Lambda. Parameter Store pode armazenar segredos, mas não tem rotação nativa integrada.

---

### Questao 3

Uma empresa precisa garantir que todos os objetos enviados para um bucket S3 sejam criptografados. Qual a melhor abordagem?

**A)** Criptografar manualmente cada arquivo antes do upload

**B)** Configurar uma bucket policy que negue uploads sem criptografia (deny PutObject sem header de criptografia)

**C)** Habilitar o versionamento do bucket

**D)** Usar S3 Transfer Acceleration

> **Resposta: B** - Uma bucket policy que nega PutObject requests sem o header de criptografia garante que todos os objetos sejam criptografados. Alternativamente, o S3 agora suporta criptografia padrão (default encryption) com SSE-S3, que criptografa automáticamente todos os novos objetos.

---

### Questao 4

Qual serviço da AWS detecta automáticamente dados sensíveis (como PII e números de cartao de credito) armazenados em buckets S3?

**A)** Amazon GuardDuty

**B)** Amazon Inspector

**C)** Amazon Macie

**D)** AWS Config

> **Resposta: C** - Amazon Macie usa machine learning para descobrir e proteger dados sensíveis no S3. Ele identifica automáticamente PII, dados financeiros e outros dados sensíveis, gerando alertas e relatórios.

---

### Questao 5

Uma empresa precisa garantir que certificados TLS/SSL para seus domínios sejam renovados automáticamente e integrados com CloudFront e ALB. Qual serviço deve ser usado?

**A)** AWS KMS

**B)** AWS Certificaté Manager (ACM)

**C)** AWS Secrets Manager

**D)** AWS CloudHSM

> **Resposta: B** - O AWS Certificaté Manager provisiona e gerencia certificados TLS/SSL gratuitamente para uso com serviços AWS integrados (CloudFront, ALB, API Gatéway). Os certificados sao renovados automáticamente antes de expirar.

---

Voltar ao [Índice](../../../../index.md)
