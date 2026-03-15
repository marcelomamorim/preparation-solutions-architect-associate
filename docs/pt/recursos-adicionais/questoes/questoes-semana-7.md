# Questões de Prática - Parte 7: Banco de Dados e Otimização de Custos

> Teste seus conhecimentos sobre bancos de dados AWS, otimização de custos de computação e armazenamento.

---

### Questao 1

Uma startup precisa de um banco de dados para sua aplicação web. O tráfego e imprevisível e pode variar de zero a milhares de requisicoes por segundo. A equipe quer minimizar custos quando não há tráfego. Qual solução e mais adequada?

**A)** Amazon RDS MySQL com instância Multi-AZ

**B)** Amazon Aurora Serverless v2

**C)** Amazon DynamoDB com capacidade provisionada

**D)** Amazon EC2 com MySQL instalado

> **Resposta: B** - Aurora Serverless v2 escala automaticamente a capacidade de computação baseada na demanda, podendo escalar até quase zero quando não há tráfego. E ideal para workloads imprevisíveis. DynamoDB On-Demand também seria uma opção válida para NoSQL.

---

### Questao 2

Uma empresa tem workloads de processamento em lote que podem ser interrompidas sem impacto. Os jobs levam entre 2-4 horas para completar e podem ser reiniciados. Qual modelo de compra EC2 oferece o maior desconto?

**A)** On-Demand Instances

**B)** Reserved Instances (1 ano)

**C)** Spot Instances

**D)** Dedicatéd Hosts

> **Resposta: C** - Spot Instances oferecem até 90% de desconto comparado a On-Demand. Como os workloads podem ser interrompidos e reiniciados, Spot e ideal. Use Spot Fleet ou EC2 Auto Scaling com diversificação de tipos de instância para maior disponibilidade.

---

### Questao 3

Uma empresa executa uma aplicação com tráfego previsível e constante, 24/7, durante todo o ano. A empresa quer reduzir os custos de computação EC2. Qual abordagem oferece a melhor economia?

**A)** Usar apenas On-Demand Instances

**B)** Comprar Compute Savings Plans com compromisso de 3 anos e pagamento antecipado total

**C)** Usar apenas Spot Instances

**D)** Usar instâncias T3 com créditos ilimitados

> **Resposta: B** - Compute Savings Plans com compromisso de 3 anos e pagamento antecipado total oferecem o maior desconto (até 72%). Para workloads previsiveis 24/7, o compromisso de longo prazo é a melhor estratégia. Spot não e adequado para cargas críticas constantes.

---

### Questao 4

Uma aplicação usa DynamoDB com tráfego variável. Durante o dia, recebe milhares de requisicoes por segundo. A noite, o tráfego cai para quase zero. Qual modo de capacidade e mais econômico?

**A)** Capacidade provisionada com valores altos fixos

**B)** Capacidade provisionada com Auto Scaling

**C)** Modo On-Demand

**D)** Capacidade provisionada com Reserved Capacity

> **Resposta: B** - Capacidade provisionada com Auto Scaling ajusta a capacidade automaticamente baseada no tráfego, mantendo custos baixos a noite e escalando durante o dia. On-Demand e mais simples mas pode ser mais caro para padrões previsiveis. Reserved e para tráfego muito estável.

---

### Questao 5

Uma empresa quer identificar instâncias EC2 que estao superdimensionadas (usando menos de 10% da CPU consistentemente) e receber recomendações de right-sizing. Qual serviço fornece essas recomendações?

**A)** Amazon CloudWatch

**B)** AWS Trusted Advisor

**C)** AWS Compute Optimizer

**D)** AWS Cost Explorer

> **Resposta: C** - AWS Compute Optimizer analisa métricas de utilização (CPU, memória, rede) e recomenda tipos de instância ideais para cada workload. Trusted Advisor também identifica instâncias ociosas, mas Compute Optimizer oferece recomendações mais detalhadas com estimativas de economia.

---

Voltar ao [Índice](../../../../index.md)
