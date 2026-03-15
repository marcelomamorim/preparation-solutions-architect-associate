# Semana 7 - Rede e Otimizacao de Custos

> **Dominio 3 (Tarefas 3.4-3.5) e Dominio 4** | Tempo estimado: 8-10 horas de estudo

## Objetivos de Aprendizado

Ao final desta semana, voce devera ser capaz de:
- Projetar arquiteturas de rede de alto desempenho (CloudFront, Global Accelerator, Direct Connect)
- Entender ingestao e transformacao de dados (Kinesis, Glue, Athena)
- Selecionar modelos de compra EC2 otimizados por custo (On-Demand, RI, Savings Plans, Spot)
- Otimizar custos de armazenamento com S3 Lifecycle Policies e classes de armazenamento
- Usar ferramentas de gerenciamento de custos (Cost Explorer, Budgets, Trusted Advisor)

---

## Conhecimentos Necessarios

### Rede de Alto Desempenho (Dominio 3)
- **Servicos de borda**: [CloudFront](https://aws.amazon.com/cloudfront/), [Global Accelerator](https://aws.amazon.com/global-accelerator/)
- **Balanceamento de carga**: ALB (camada 7), NLB (camada 4), GLB (appliances)
- **Conectividade**: [VPN](https://aws.amazon.com/vpn/), [Direct Connect](https://aws.amazon.com/directconnect/), [PrivateLink](https://aws.amazon.com/privatelink/)

### Ingestao e Transformacao de Dados (Dominio 3)
- **Streaming**: [Kinesis Data Streams](https://aws.amazon.com/kinesis/) vs. [Kinesis Data Firehose](https://aws.amazon.com/kinesis/data-firehose/)
- **ETL**: [AWS Glue](https://aws.amazon.com/glue/) - catalogo de dados, conversao de formatos
- **Analise**: [Amazon Athena](https://aws.amazon.com/athena/) - SQL no S3, [QuickSight](https://aws.amazon.com/quicksight/) - BI
- **Data Lake**: [Lake Formation](https://aws.amazon.com/lake-formation/) + S3

### Otimizacao de Custos (Dominio 4)
- **Computacao**: On-Demand, Reserved Instances, Savings Plans, Spot Instances
- **Armazenamento**: Classes S3, Lifecycle Policies, EBS gp3 vs. gp2
- **Banco de dados**: Aurora Serverless, DynamoDB On-Demand vs. Provisioned
- **Rede**: VPC Endpoints, CloudFront para reducao de egress, NAT Gateway vs. NAT Instance
- **Ferramentas**: [Cost Explorer](https://aws.amazon.com/aws-cost-management/aws-cost-explorer/), [Budgets](https://aws.amazon.com/aws-cost-management/aws-budgets/), [Compute Optimizer](https://aws.amazon.com/compute-optimizer/)

## Habilidades Necessarias

- Criar topologias de rede para arquiteturas globais e hibridas
- Construir e proteger data lakes com Lake Formation e S3
- Projetar pipelines de streaming e ETL
- Selecionar modelos de compra EC2 adequados ao workload
- Otimizar custos de armazenamento, banco de dados e rede
- Usar ferramentas de gerenciamento de custos para monitoramento

---

## Dicas de Estudo para esta Semana

1. **CloudFront vs. Global Accelerator**: CloudFront cacheia conteudo na borda. Global Accelerator roteia trafego pela rede AWS (sem cache)
2. **Kinesis Streams vs. Firehose**: Streams = processamento custom em tempo real. Firehose = entrega automatica (near real-time) a S3/Redshift
3. **Spot Instances**: Ate 90% de desconto, mas podem ser interrompidas. Use para batch, CI/CD, ML training
4. **VPC Endpoints**: Gateway (S3, DynamoDB - gratuito) elimina custos de NAT. Interface (outros - custo por hora)
5. **S3 Intelligent-Tiering**: Ideal quando o padrao de acesso e desconhecido. Move automaticamente entre tiers

## Recursos desta Semana

- [Questoes de pratica - Parte 7](../recursos-adicionais/questoes/questoes-semana-7.md)
- [Dominio 3 completo](../dominio/design-arquiteturas-alto-desempenho.md)
- [Dominio 4 completo](../dominio/design-arquiteturas-otimizadas-custo.md)

---

Voltar ao [Indice](../../../index.md)
