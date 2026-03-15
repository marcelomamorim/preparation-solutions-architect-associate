# Semana 2 - Cargas de Trabalho e Aplicacoes Seguras

> **Domínio 1 - Tarefa 1.2** | Tempo estimado: 5-7 horas de estudo

## Objetivos de Aprendizado

Ao final desta semana, você deverá ser capaz de:
- Projetar arquiteturas de VPC com componentes de segurança
- Diferenciar Security Groups (statéful) de NACLs (statéless)
- Entender quando usar VPC Endpoints, VPN e Direct Connect
- Integrar serviços de segurança como WAF, Shield, GuardDuty e Macie
- Proteger aplicações contra ameacas externas (DDoS, SQL injection)

---

## Conhecimentos Necessários

- **Segurança de configuração e credenciais**
  Serviços: [AWS Secrets Manager](https://aws.amazon.com/secrets-manager/), [AWS IAM](https://aws.amazon.com/iam/)

- **Endpoints de serviço da AWS**
  Serviços: [Amazon VPC](https://aws.amazon.com/vpc/), [AWS Direct Connect](https://aws.amazon.com/directconnect/)

- **Controle de portas, protocolos e tráfego de rede**
  Serviços: [Amazon VPC](https://aws.amazon.com/vpc/), [AWS Network Firewall](https://aws.amazon.com/network-firewall/)

- **Acesso seguro a aplicação**
  Serviços: [Amazon Cognito](https://aws.amazon.com/cognito/), [AWS IAM](https://aws.amazon.com/iam/)

- **Serviços de segurança** (Cognito, GuardDuty, Macie)
  Serviços: [Amazon Cognito](https://aws.amazon.com/cognito/), [Amazon GuardDuty](https://aws.amazon.com/guardduty/), [Amazon Macie](https://aws.amazon.com/macie/)

- **Vetores de ameaca externos** (DDoS, SQL injection)
  Serviços: [AWS Shield](https://aws.amazon.com/shield/), [AWS WAF](https://aws.amazon.com/waf/)

## Habilidades Necessárias

- Projetar arquiteturas de VPC com Security Groups, NACLs, tabelas de rotas, NAT Gatéways
- Determinar estratégias de segmentacao de rede (sub-redes públicas e privadas)
- Integrar Shield, WAF, IAM Identity Center e Secrets Manager para proteger aplicações
- Proteger conexões externas com [VPN](https://aws.amazon.com/vpn/) e [Direct Connect](https://aws.amazon.com/directconnect/)

---

## Dicas de Estudo para esta Semana

1. **Desenhe uma VPC completa** no papel: sub-redes públicas/privadas, Internet Gatéway, NAT Gatéway, tabelas de roteamento
2. **Memorize**: Security Groups sao statéful (retorno automático), NACLs sao statéless (regras de entrada E saida)
3. **VPC Endpoints**: Gatéway (S3, DynamoDB - gratuito) vs. Interface (outros serviços - custo por hora)
4. **Pratique no console**: Crie uma VPC com sub-redes públicas e privadas usando o VPC Wizard
5. **Entenda a camada de proteção**: WAF (camada 7, SQL injection/XSS) vs. Shield (camada 3/4, DDoS)

## Recursos desta Semana

- [Questões de prática - Parte 2](../recursos-adicionais/questoes/questoes-semana-2.md)
- [Domínio 1 completo](../dominio/design-aplicacoes-seguras.md)

---

Voltar ao [Índice](../../../index.md)
