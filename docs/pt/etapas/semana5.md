# Semana 5 - Alta Disponibilidade e Tolerancia a Falhas

> **Dominio 2 - Tarefa 2.2** | Tempo estimado: 6-8 horas de estudo

## Objetivos de Aprendizado

Ao final desta semana, voce devera ser capaz de:
- Projetar arquiteturas Multi-AZ e Multi-Region
- Entender as 4 estrategias de Disaster Recovery (DR)
- Configurar Route 53 com health checks e failover
- Implementar infraestrutura imutavel com CloudFormation
- Identificar e eliminar pontos unicos de falha (SPOF)

---

## Conhecimentos Necessarios

- **Infraestrutura global**: AZs, Regioes, [Route 53](https://aws.amazon.com/route53/)
- **Estrategias de DR**: Backup & Restore, Pilot Light, Warm Standby, Active-Active
- **RPO e RTO**: Recovery Point Objective e Recovery Time Objective
- **Padroes de design distribuido**: [CloudFront](https://aws.amazon.com/cloudfront/), [Global Accelerator](https://aws.amazon.com/global-accelerator/)
- **Infraestrutura imutavel**: [CloudFormation](https://aws.amazon.com/cloudformation/), Blue/Green deployments
- **Proxies de banco de dados**: [RDS Proxy](https://aws.amazon.com/rds/proxy/)
- **Visibilidade de workloads**: [CloudWatch](https://aws.amazon.com/cloudwatch/), [X-Ray](https://aws.amazon.com/xray/)
- **Failover**: [Route 53](https://aws.amazon.com/route53/) com health checks

## Habilidades Necessarias

- Determinar estrategias de automacao para integridade da infraestrutura
- Fornecer arquiteturas altamente disponiveis em multiplas AZs e Regioes
- Identificar metricas de negocio para solucoes de alta disponibilidade
- Implementar designs para mitigar pontos unicos de falha
- Implementar estrategias para durabilidade e disponibilidade de dados
- Selecionar estrategias de DR apropriadas ao negocio

---

## Dicas de Estudo para esta Semana

1. **Estrategias de DR** (da mais barata a mais rapida): Backup & Restore, Pilot Light, Warm Standby, Active-Active
2. **RDS Multi-AZ**: Failover automatico em 60-120 segundos. Replicas de leitura NAO sao Multi-AZ por padrao
3. **Route 53 Failover**: Configure health checks + failover routing para DR automatico
4. **Aurora**: Ate 15 replicas de leitura em 3 AZs, failover em menos de 30 segundos
5. **Memorize**: S3 tem 99.999999999% (11 noves) de durabilidade

## Recursos desta Semana

- [Questoes de pratica - Parte 5](../recursos-adicionais/questoes/questoes-semana-5.md)
- [Dominio 2 completo](../dominio/design-arquiteturas-resilientes.md)

---

Voltar ao [Indice](../../../index.md)
