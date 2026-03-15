# Questoes de Pratica - Parte 3: Seguranca de Dados e Criptografia

> Teste seus conhecimentos sobre criptografia, KMS, protecao de dados e conformidade.

---

### Questao 1

Uma empresa precisa criptografar dados armazenados no Amazon S3 e manter controle total sobre as chaves de criptografia, incluindo auditoria de uso via CloudTrail. Qual opcao de criptografia deve ser usada?

**A)** SSE-S3 (Server-Side Encryption com chaves gerenciadas pelo S3)

**B)** SSE-KMS (Server-Side Encryption com chaves do AWS KMS)

**C)** SSE-C (Server-Side Encryption com chaves fornecidas pelo cliente)

**D)** Criptografia do lado do cliente

> **Resposta: B** - SSE-KMS oferece controle sobre as chaves de criptografia e registra cada uso da chave no CloudTrail para auditoria. SSE-S3 e mais simples mas nao oferece auditoria granular. SSE-C requer que o cliente gerencie as chaves fora da AWS.

---

### Questao 2

Uma aplicacao precisa armazenar credenciais de banco de dados de forma segura e rotaciona-las automaticamente a cada 30 dias. Qual servico e mais adequado?

**A)** AWS Systems Manager Parameter Store (SecureString)

**B)** AWS Secrets Manager

**C)** AWS KMS

**D)** Amazon S3 com criptografia

> **Resposta: B** - AWS Secrets Manager foi projetado especificamente para armazenar e rotacionar segredos como credenciais de banco de dados. Oferece rotacao automatica nativa com Lambda. Parameter Store pode armazenar segredos, mas nao tem rotacao nativa integrada.

---

### Questao 3

Uma empresa precisa garantir que todos os objetos enviados para um bucket S3 sejam criptografados. Qual a melhor abordagem?

**A)** Criptografar manualmente cada arquivo antes do upload

**B)** Configurar uma bucket policy que negue uploads sem criptografia (deny PutObject sem header de criptografia)

**C)** Habilitar o versionamento do bucket

**D)** Usar S3 Transfer Acceleration

> **Resposta: B** - Uma bucket policy que nega PutObject requests sem o header de criptografia garante que todos os objetos sejam criptografados. Alternativamente, o S3 agora suporta criptografia padrao (default encryption) com SSE-S3, que criptografa automaticamente todos os novos objetos.

---

### Questao 4

Qual servico da AWS detecta automaticamente dados sensiveis (como PII e numeros de cartao de credito) armazenados em buckets S3?

**A)** Amazon GuardDuty

**B)** Amazon Inspector

**C)** Amazon Macie

**D)** AWS Config

> **Resposta: C** - Amazon Macie usa machine learning para descobrir e proteger dados sensiveis no S3. Ele identifica automaticamente PII, dados financeiros e outros dados sensiveis, gerando alertas e relatorios.

---

### Questao 5

Uma empresa precisa garantir que certificados TLS/SSL para seus dominios sejam renovados automaticamente e integrados com CloudFront e ALB. Qual servico deve ser usado?

**A)** AWS KMS

**B)** AWS Certificate Manager (ACM)

**C)** AWS Secrets Manager

**D)** AWS CloudHSM

> **Resposta: B** - O AWS Certificate Manager provisiona e gerencia certificados TLS/SSL gratuitamente para uso com servicos AWS integrados (CloudFront, ALB, API Gateway). Os certificados sao renovados automaticamente antes de expirar.

---

Voltar ao [Indice](../../../../index.md)
