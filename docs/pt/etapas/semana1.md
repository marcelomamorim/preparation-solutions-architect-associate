# Semana 1 - Acesso Seguro aos Recursos da AWS

> **Dominio 1 - Tarefa 1.1** | Tempo estimado: 5-7 horas de estudo

## Objetivos de Aprendizado

Ao final desta semana, voce devera ser capaz de:
- Entender e aplicar o principio do menor privilegio no IAM
- Diferenciar entre usuarios, grupos, funcoes e politicas do IAM
- Projetar estrategias de acesso entre contas com STS e AssumeRole
- Compreender o modelo de responsabilidade compartilhada da AWS
- Configurar AWS Organizations e SCPs para multiplas contas

---

## Conhecimentos Necessarios

- **Controles de acesso e gerenciamento em varias contas**
  Servicos: [AWS IAM](https://aws.amazon.com/iam/), [AWS Organizations](https://aws.amazon.com/organizations/)

- **Servicos de acesso federado e identidade da AWS**
  Servicos: [AWS IAM](https://aws.amazon.com/iam/), [AWS IAM Identity Center](https://aws.amazon.com/single-sign-on/)

- **Infraestrutura global da AWS** (Zonas de Disponibilidade, Regioes)
  Servicos: [Amazon VPC](https://aws.amazon.com/vpc/), [AWS CloudFormation](https://aws.amazon.com/cloudformation/)

- **Melhores praticas de seguranca da AWS** (principio do menor privilegio)
  Servicos: [AWS Trusted Advisor](https://aws.amazon.com/premiumsupport/trustedadvisor/), [AWS Security Hub](https://aws.amazon.com/security-hub/)

- **Modelo de responsabilidade compartilhada da AWS**
  Servicos: [AWS CloudTrail](https://aws.amazon.com/cloudtrail/)

## Habilidades Necessarias

- Aplicar melhores praticas de seguranca para usuarios IAM e root (MFA obrigatorio)
- Projetar modelos de autorizacao flexiveis com usuarios, grupos, funcoes e politicas
- Projetar estrategias de controle de acesso baseadas em funcoes com [AWS STS](https://aws.amazon.com/sts/)
- Projetar estrategias de seguranca para multiplas contas com [AWS Control Tower](https://aws.amazon.com/controltower/) e SCPs
- Determinar o uso apropriado de politicas de recursos vs. politicas de identidade
- Determinar quando federar um servico de diretorio com funcoes do IAM

---

## Dicas de Estudo para esta Semana

1. **Crie uma conta AWS Free Tier** e pratique criando usuarios, grupos e politicas IAM
2. **Leia a FAQ do IAM**: [IAM FAQ](https://aws.amazon.com/iam/faqs/)
3. **Entenda a diferenca entre politicas gerenciadas e inline** - isso e cobrado no exame
4. **Pratique com o IAM Policy Simulator**: Teste suas politicas antes de aplica-las
5. **Memorize**: A conta root deve ter MFA, nao deve ter access keys, e so deve ser usada para tarefas que exigem root

## Recursos desta Semana

- [Questoes de pratica - Parte 1](../recursos-adicionais/questoes/questoes-semana-1.md)
- [Dominio 1 completo](../dominio/design-aplicacoes-seguras.md)

---

Voltar ao [Indice](../../../index.md)
