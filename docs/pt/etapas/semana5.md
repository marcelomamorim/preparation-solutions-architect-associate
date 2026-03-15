# Semana 5 - Alta Disponibilidade e Tolerância a Falhas

> **Domínio 2 - Tarefa 2.2** | Tempo estimado: 6-8 horas de estudo

## Objetivos de Aprendizado

Ao final desta semana, você deverá ser capaz de:
- Projetar arquiteturas Multi-AZ e Multi-Region
- Entender as 4 estratégias de Disaster Recovery (DR)
- Configurar Route 53 com health checks e failover
- Implementar infraestrutura imutavel com CloudFormation
- Identificar e eliminar pontos únicos de falha (SPOF)

---

## Conhecimentos Necessários

- **Infraestrutura global**: AZs, Regioes, [Route 53](https://aws.amazon.com/route53/)
- **Estratégias de DR**: Backup & Restore, Pilot Light, Warm Standby, Active-Active
- **RPO e RTO**: Recovery Point Objective e Recovery Time Objective
- **Padrões de design distribuido**: [CloudFront](https://aws.amazon.com/cloudfront/), [Global Accelerator](https://aws.amazon.com/global-accelerator/)
- **Infraestrutura imutavel**: [CloudFormation](https://aws.amazon.com/cloudformation/), Blue/Green deployments
- **Proxies de banco de dados**: [RDS Proxy](https://aws.amazon.com/rds/proxy/)
- **Visibilidade de workloads**: [CloudWatch](https://aws.amazon.com/cloudwatch/), [X-Ray](https://aws.amazon.com/xray/)
- **Failover**: [Route 53](https://aws.amazon.com/route53/) com health checks

## Habilidades Necessárias

- Determinar estratégias de automação para integridade da infraestrutura
- Fornecer arquiteturas altamente disponiveis em múltiplas AZs e Regioes
- Identificar métricas de negocio para soluções de alta disponibilidade
- Implementar designs para mitigar pontos únicos de falha
- Implementar estratégias para durabilidade e disponibilidade de dados
- Selecionar estratégias de DR apropriadas ao negocio

---

## Dicas de Estudo para esta Semana

1. **Estratégias de DR** (da mais barata a mais rápida): Backup & Restore, Pilot Light, Warm Standby, Active-Active
2. **RDS Multi-AZ**: Failover automático em 60-120 segundos. Replicas de leitura NAO são Multi-AZ por padrão
3. **Route 53 Failover**: Configure health checks + failover routing para DR automático
4. **Aurora**: Até 15 replicas de leitura em 3 AZs, failover em menos de 30 segundos
5. **Memorize**: S3 tem 99.999999999% (11 noves) de durabilidade

## Recursos desta Semana

- [Questões de prática - Parte 5](../recursos-adicionais/questoes/questoes-semana-5.md)
- [Domínio 2 completo](../dominio/design-arquiteturas-resilientes.md)

---

Voltar ao [Índice](../../../index.md)
