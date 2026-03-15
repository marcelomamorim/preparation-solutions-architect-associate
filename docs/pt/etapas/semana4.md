# Semana 4 - Arquiteturas Escaláveis e Desacopladas

> **Domínio 2 - Tarefa 2.1** | Tempo estimado: 6-8 horas de estudo

## Objetivos de Aprendizado

Ao final desta semana, você deverá ser capaz de:
- Projetar arquiteturas fracamente acopladas com SQS, SNS e EventBridge
- Entender escalabilidade horizontal vs. vertical e Auto Scaling
- Diferenciar ALB, NLB e GLB e quando usar cada um
- Projetar arquiteturas de microsserviços com containers e serverless
- Implementar padrões de arquitetura orientada a eventos

---

## Conhecimentos Necessários

- **APIs**: [Amazon API Gatéway](https://aws.amazon.com/api-gateway/) - REST e WebSocket
- **Serviços gerenciados**: [Amazon SQS](https://aws.amazon.com/sqs/), [AWS Secrets Manager](https://aws.amazon.com/secrets-manager/)
- **Estratégias de cache**: [Amazon ElastiCache](https://aws.amazon.com/elasticache/) - Redis e Memcached
- **Microsserviços**: Workloads statéless vs. statéful. [Lambda](https://aws.amazon.com/lambda/), [Fargaté](https://aws.amazon.com/fargate/)
- **Arquiteturas orientadas a eventos**: [EventBridge](https://aws.amazon.com/eventbridge/), [SNS](https://aws.amazon.com/sns/)
- **Escalabilidade**: [EC2 Auto Scaling](https://aws.amazon.com/autoscaling/) - horizontal vs. vertical
- **Aceleradores de borda**: [CloudFront](https://aws.amazon.com/cloudfront/), [Global Accelerator](https://aws.amazon.com/global-accelerator/)
- **Containers**: [ECS](https://aws.amazon.com/ecs/), [EKS](https://aws.amazon.com/eks/), [Fargaté](https://aws.amazon.com/fargate/)
- **Balanceamento de carga**: ALB (camada 7), NLB (camada 4), GLB (appliances de rede)
- **Filas e mensagens**: SQS Standard vs. FIFO, SNS pub/sub
- **Armazenamento**: Objeto (S3), Arquivo (EFS), Bloco (EBS)

## Habilidades Necessárias

- Projetar arquiteturas orientadas a eventos, microsserviços e multi-tier
- Determinar estratégias de escalabilidade para componentes da arquitetura
- Determinar serviços de desacoplamento (SQS, SNS, Step Functions)
- Decidir quando usar containers vs. serverless
- Recomendar tecnologias de computacao, armazenamento, rede e banco de dados

---

## Dicas de Estudo para esta Semana

1. **SQS Standard vs. FIFO**: Standard tem entrega pelo menos uma vez (maior throughput). FIFO garante ordem e exatamente uma vez (300 msg/s)
2. **Padrão fan-out clássico**: SNS para múltiplas filas SQS (cada consumidor processa independentemente)
3. **Auto Scaling**: Target Tracking (mantem métrica em X%), Step Scaling (acoes por faixas), Scheduled (horarios)
4. **ALB vs. NLB**: ALB para roteamento HTTP (path, host). NLB para TCP/UDP, IP estático, ultra-baixa latência
5. **Pratique**: Crie um Auto Scaling Group com ALB e politica de Target Tracking no Free Tier

## Recursos desta Semana

- [Questões de prática - Parte 4](../recursos-adicionais/questoes/questoes-semana-4.md)
- [Domínio 2 completo](../dominio/design-arquiteturas-resilientes.md)

---

Voltar ao [Índice](../../../index.md)
