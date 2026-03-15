# Semana 1 - Acesso Seguro aos Recursos da AWS

> **Domínio 1 - Tarefa 1.1** | Tempo estimado: 5-7 horas de estudo

## Objetivos de Aprendizado

Ao final desta semana, você deverá ser capaz de:
- Entender e aplicar o principio do menor privilegio no IAM
- Diferenciar entre usuários, grupos, funções e politicas do IAM
- Projetar estratégias de acesso entre contas com STS e AssumeRole
- Compreender o modelo de responsabilidade compartilhada da AWS
- Configurar AWS Organizations e SCPs para múltiplas contas

---

## Conhecimentos Necessários

- **Controles de acesso e gerenciamento em varias contas**
  Serviços: [AWS IAM](https://aws.amazon.com/iam/), [AWS Organizations](https://aws.amazon.com/organizations/)

- **Serviços de acesso federado e identidade da AWS**
  Serviços: [AWS IAM](https://aws.amazon.com/iam/), [AWS IAM Identity Center](https://aws.amazon.com/single-sign-on/)

- **Infraestrutura global da AWS** (Zonas de Disponibilidade, Regioes)
  Serviços: [Amazon VPC](https://aws.amazon.com/vpc/), [AWS CloudFormation](https://aws.amazon.com/cloudformation/)

- **Melhores práticas de segurança da AWS** (principio do menor privilegio)
  Serviços: [AWS Trusted Advisor](https://aws.amazon.com/premiumsupport/trustedadvisor/), [AWS Security Hub](https://aws.amazon.com/security-hub/)

- **Modelo de responsabilidade compartilhada da AWS**
  Serviços: [AWS CloudTrail](https://aws.amazon.com/cloudtrail/)

## Habilidades Necessárias

- Aplicar melhores práticas de segurança para usuários IAM e root (MFA obrigatório)
- Projetar modelos de autorizacao flexiveis com usuários, grupos, funções e politicas
- Projetar estratégias de controle de acesso baseadas em funções com [AWS STS](https://aws.amazon.com/sts/)
- Projetar estratégias de segurança para múltiplas contas com [AWS Control Tower](https://aws.amazon.com/controltower/) e SCPs
- Determinar o uso apropriado de politicas de recursos vs. politicas de identidade
- Determinar quando federar um serviço de diretório com funções do IAM

---

## Dicas de Estudo para esta Semana

1. **Crie uma conta AWS Free Tier** e pratique criando usuários, grupos e politicas IAM
2. **Leia a FAQ do IAM**: [IAM FAQ](https://aws.amazon.com/iam/faqs/)
3. **Entenda a diferenca entre politicas gerenciadas e inline** - isso e cobrado no exame
4. **Pratique com o IAM Policy Simulator**: Teste suas politicas antes de aplica-las
5. **Memorize**: A conta root deve ter MFA, não deve ter access keys, e so deve ser usada para tarefas que exigem root

## Recursos desta Semana

- [Questões de prática - Parte 1](../recursos-adicionais/questoes/questoes-semana-1.md)
- [Domínio 1 completo](../dominio/design-aplicacoes-seguras.md)

---

Voltar ao [Índice](../../../index.md)
