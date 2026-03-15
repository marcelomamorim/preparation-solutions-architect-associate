# Questoes de Pratica - Parte 1: Acesso Seguro aos Recursos AWS

> Teste seus conhecimentos sobre IAM, Organizations e acesso seguro. Tente responder antes de ver a explicacao.

---

### Questao 1

Uma empresa precisa permitir que desenvolvedores de uma conta AWS de desenvolvimento acessem um bucket S3 em uma conta AWS de producao. Qual e a abordagem mais segura?

**A)** Criar usuarios IAM na conta de producao para cada desenvolvedor

**B)** Compartilhar as credenciais de um usuario IAM da conta de producao

**C)** Criar uma funcao (role) IAM na conta de producao com uma politica de confianca para a conta de desenvolvimento e usar AssumeRole

**D)** Tornar o bucket S3 publico

> **Resposta: C** - O acesso entre contas com IAM Roles e AssumeRole e a pratica recomendada pela AWS. Evita criar usuarios duplicados, nao expoe credenciais e permite auditoria via CloudTrail.

---

### Questao 2

Qual servico da AWS permite gerenciar centralmente politicas de acesso para multiplas contas AWS?

**A)** AWS IAM

**B)** AWS Organizations com Service Control Policies (SCPs)

**C)** Amazon Cognito

**D)** AWS Directory Service

> **Resposta: B** - AWS Organizations com SCPs permite definir guardrails de permissoes que se aplicam a todas as contas da organizacao. SCPs limitam as permissoes maximas que podem ser concedidas em contas filhas.

---

### Questao 3

Uma empresa quer implementar single sign-on (SSO) para que seus funcionarios acessem multiplas contas AWS e aplicacoes de negocio usando suas credenciais corporativas do Active Directory. Qual servico deve ser usado?

**A)** AWS IAM com federacao SAML 2.0

**B)** AWS IAM Identity Center (antigo AWS SSO)

**C)** Amazon Cognito User Pools

**D)** AWS Directory Service

> **Resposta: B** - O AWS IAM Identity Center e o servico recomendado para SSO em multiplas contas AWS. Integra-se nativamente com AWS Organizations e suporta conexao com Active Directory corporativo. Cognito e para aplicacoes voltadas ao consumidor final.

---

### Questao 4

Segundo o modelo de responsabilidade compartilhada da AWS, qual das seguintes e responsabilidade do cliente?

**A)** Seguranca fisica dos data centers

**B)** Patch do sistema operacional de instancias EC2

**C)** Manutencao do hipervisor

**D)** Gerenciamento da infraestrutura de rede global

> **Resposta: B** - No modelo de responsabilidade compartilhada, o cliente e responsavel por gerenciar o sistema operacional de instancias EC2, incluindo patches e atualizacoes. A AWS cuida da infraestrutura fisica, rede e hipervisor.

---

### Questao 5

Qual e a pratica recomendada para proteger a conta root da AWS?

**A)** Usar a conta root para tarefas administrativas diarias

**B)** Compartilhar as credenciais root com administradores

**C)** Habilitar MFA, nao criar access keys, e usar apenas para tarefas que exigem root

**D)** Deletar a conta root apos criar usuarios IAM

> **Resposta: C** - A conta root deve ser protegida com MFA, nao deve ter access keys criadas, e deve ser usada apenas para as poucas tarefas que exigem acesso root (como fechar a conta ou alterar o plano de suporte).

---

Voltar ao [Indice](../../../../index.md)
