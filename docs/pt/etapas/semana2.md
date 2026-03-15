# Semana 2 - Cargas de Trabalho e Aplicacoes Seguras

> **Dominio 1 - Tarefa 1.2** | Tempo estimado: 5-7 horas de estudo

## Objetivos de Aprendizado

Ao final desta semana, voce devera ser capaz de:
- Projetar arquiteturas de VPC com componentes de seguranca
- Diferenciar Security Groups (stateful) de NACLs (stateless)
- Entender quando usar VPC Endpoints, VPN e Direct Connect
- Integrar servicos de seguranca como WAF, Shield, GuardDuty e Macie
- Proteger aplicacoes contra ameacas externas (DDoS, SQL injection)

---

## Conhecimentos Necessarios

- **Seguranca de configuracao e credenciais**
  Servicos: [AWS Secrets Manager](https://aws.amazon.com/secrets-manager/), [AWS IAM](https://aws.amazon.com/iam/)

- **Endpoints de servico da AWS**
  Servicos: [Amazon VPC](https://aws.amazon.com/vpc/), [AWS Direct Connect](https://aws.amazon.com/directconnect/)

- **Controle de portas, protocolos e trafego de rede**
  Servicos: [Amazon VPC](https://aws.amazon.com/vpc/), [AWS Network Firewall](https://aws.amazon.com/network-firewall/)

- **Acesso seguro a aplicacao**
  Servicos: [Amazon Cognito](https://aws.amazon.com/cognito/), [AWS IAM](https://aws.amazon.com/iam/)

- **Servicos de seguranca** (Cognito, GuardDuty, Macie)
  Servicos: [Amazon Cognito](https://aws.amazon.com/cognito/), [Amazon GuardDuty](https://aws.amazon.com/guardduty/), [Amazon Macie](https://aws.amazon.com/macie/)

- **Vetores de ameaca externos** (DDoS, SQL injection)
  Servicos: [AWS Shield](https://aws.amazon.com/shield/), [AWS WAF](https://aws.amazon.com/waf/)

## Habilidades Necessarias

- Projetar arquiteturas de VPC com Security Groups, NACLs, tabelas de rotas, NAT Gateways
- Determinar estrategias de segmentacao de rede (sub-redes publicas e privadas)
- Integrar Shield, WAF, IAM Identity Center e Secrets Manager para proteger aplicacoes
- Proteger conexoes externas com [VPN](https://aws.amazon.com/vpn/) e [Direct Connect](https://aws.amazon.com/directconnect/)

---

## Dicas de Estudo para esta Semana

1. **Desenhe uma VPC completa** no papel: sub-redes publicas/privadas, Internet Gateway, NAT Gateway, tabelas de roteamento
2. **Memorize**: Security Groups sao stateful (retorno automatico), NACLs sao stateless (regras de entrada E saida)
3. **VPC Endpoints**: Gateway (S3, DynamoDB - gratuito) vs. Interface (outros servicos - custo por hora)
4. **Pratique no console**: Crie uma VPC com sub-redes publicas e privadas usando o VPC Wizard
5. **Entenda a camada de protecao**: WAF (camada 7, SQL injection/XSS) vs. Shield (camada 3/4, DDoS)

## Recursos desta Semana

- [Questoes de pratica - Parte 2](../recursos-adicionais/questoes/questoes-semana-2.md)
- [Dominio 1 completo](../dominio/design-aplicacoes-seguras.md)

---

Voltar ao [Indice](../../../index.md)
