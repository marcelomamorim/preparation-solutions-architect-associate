# Questões de Prática - Parte 1: Acesso Seguro aos Recursos AWS

> Teste seus conhecimentos sobre IAM, Organizations e acesso seguro. Tente responder antes de ver a explicacao.

---

### Questao 1

Uma empresa precisa permitir que desenvolvedores de uma conta AWS de desenvolvimento acessem um bucket S3 em uma conta AWS de produção. Qual e a abordagem mais segura?

**A)** Criar usuários IAM na conta de produção para cada desenvolvedor

**B)** Compartilhar as credenciais de um usuário IAM da conta de produção

**C)** Criar uma função (role) IAM na conta de produção com uma politica de confianca para a conta de desenvolvimento e usar AssumeRole

**D)** Tornar o bucket S3 público

> **Resposta: C** - O acesso entre contas com IAM Roles e AssumeRole e a prática recomendada pela AWS. Evita criar usuários duplicados, não expoe credenciais e permite auditoria via CloudTrail.

---

### Questao 2

Qual serviço da AWS permite gerenciar centralmente politicas de acesso para múltiplas contas AWS?

**A)** AWS IAM

**B)** AWS Organizations com Service Control Policies (SCPs)

**C)** Amazon Cognito

**D)** AWS Directory Service

> **Resposta: B** - AWS Organizations com SCPs permite definir guardrails de permissoes que se aplicam a todas as contas da organizacao. SCPs limitam as permissoes máximas que podem ser concedidas em contas filhas.

---

### Questao 3

Uma empresa quer implementar single sign-on (SSO) para que seus funcionarios acessem múltiplas contas AWS e aplicações de negocio usando suas credenciais corporativas do Active Directory. Qual serviço deve ser usado?

**A)** AWS IAM com federacao SAML 2.0

**B)** AWS IAM Identity Center (antigo AWS SSO)

**C)** Amazon Cognito User Pools

**D)** AWS Directory Service

> **Resposta: B** - O AWS IAM Identity Center e o serviço recomendado para SSO em múltiplas contas AWS. Integra-se nativamente com AWS Organizations e suporta conexão com Active Directory corporativo. Cognito e para aplicações voltadas ao consumidor final.

---

### Questao 4

Segundo o modelo de responsabilidade compartilhada da AWS, qual das seguintes e responsabilidade do cliente?

**A)** Segurança física dos data centers

**B)** Patch do sistema operacional de instâncias EC2

**C)** Manutencao do hipervisor

**D)** Gerenciamento da infraestrutura de rede global

> **Resposta: B** - No modelo de responsabilidade compartilhada, o cliente e responsavel por gerenciar o sistema operacional de instâncias EC2, incluindo patches e atualizacoes. A AWS cuida da infraestrutura física, rede e hipervisor.

---

### Questao 5

Qual e a prática recomendada para proteger a conta root da AWS?

**A)** Usar a conta root para tarefas administrativas diarias

**B)** Compartilhar as credenciais root com administradores

**C)** Habilitar MFA, não criar access keys, e usar apenas para tarefas que exigem root

**D)** Deletar a conta root apos criar usuários IAM

> **Resposta: C** - A conta root deve ser protegida com MFA, não deve ter access keys criadas, e deve ser usada apenas para as poucas tarefas que exigem acesso root (como fechar a conta ou alterar o plano de suporte).

---

Voltar ao [Índice](../../../../index.md)
