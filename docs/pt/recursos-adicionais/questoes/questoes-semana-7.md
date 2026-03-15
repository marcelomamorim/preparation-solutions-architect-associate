# Questoes de Pratica - Parte 7: Banco de Dados e Otimizacao de Custos

> Teste seus conhecimentos sobre bancos de dados AWS, otimizacao de custos de computacao e armazenamento.

---

### Questao 1

Uma startup precisa de um banco de dados para sua aplicacao web. O trafego e imprevisivel e pode variar de zero a milhares de requisicoes por segundo. A equipe quer minimizar custos quando nao ha trafego. Qual solucao e mais adequada?

**A)** Amazon RDS MySQL com instancia Multi-AZ

**B)** Amazon Aurora Serverless v2

**C)** Amazon DynamoDB com capacidade provisionada

**D)** Amazon EC2 com MySQL instalado

> **Resposta: B** - Aurora Serverless v2 escala automaticamente a capacidade de computacao baseada na demanda, podendo escalar ate quase zero quando nao ha trafego. E ideal para workloads imprevisiveis. DynamoDB On-Demand tambem seria uma opcao valida para NoSQL.

---

### Questao 2

Uma empresa tem workloads de processamento em lote que podem ser interrompidas sem impacto. Os jobs levam entre 2-4 horas para completar e podem ser reiniciados. Qual modelo de compra EC2 oferece o maior desconto?

**A)** On-Demand Instances

**B)** Reserved Instances (1 ano)

**C)** Spot Instances

**D)** Dedicated Hosts

> **Resposta: C** - Spot Instances oferecem ate 90% de desconto comparado a On-Demand. Como os workloads podem ser interrompidos e reiniciados, Spot e ideal. Use Spot Fleet ou EC2 Auto Scaling com diversificacao de tipos de instancia para maior disponibilidade.

---

### Questao 3

Uma empresa executa uma aplicacao com trafego previsivel e constante, 24/7, durante todo o ano. A empresa quer reduzir os custos de computacao EC2. Qual abordagem oferece a melhor economia?

**A)** Usar apenas On-Demand Instances

**B)** Comprar Compute Savings Plans com compromisso de 3 anos e pagamento antecipado total

**C)** Usar apenas Spot Instances

**D)** Usar instancias T3 com creditos ilimitados

> **Resposta: B** - Compute Savings Plans com compromisso de 3 anos e pagamento antecipado total oferecem o maior desconto (ate 72%). Para workloads previsiveis 24/7, o compromisso de longo prazo e a melhor estrategia. Spot nao e adequado para cargas criticas constantes.

---

### Questao 4

Uma aplicacao usa DynamoDB com trafego variavel. Durante o dia, recebe milhares de requisicoes por segundo. A noite, o trafego cai para quase zero. Qual modo de capacidade e mais economico?

**A)** Capacidade provisionada com valores altos fixos

**B)** Capacidade provisionada com Auto Scaling

**C)** Modo On-Demand

**D)** Capacidade provisionada com Reserved Capacity

> **Resposta: B** - Capacidade provisionada com Auto Scaling ajusta a capacidade automaticamente baseada no trafego, mantendo custos baixos a noite e escalando durante o dia. On-Demand e mais simples mas pode ser mais caro para padroes previsiveis. Reserved e para trafego muito estavel.

---

### Questao 5

Uma empresa quer identificar instancias EC2 que estao superdimensionadas (usando menos de 10% da CPU consistentemente) e receber recomendacoes de right-sizing. Qual servico fornece essas recomendacoes?

**A)** Amazon CloudWatch

**B)** AWS Trusted Advisor

**C)** AWS Compute Optimizer

**D)** AWS Cost Explorer

> **Resposta: C** - AWS Compute Optimizer analisa metricas de utilizacao (CPU, memoria, rede) e recomenda tipos de instancia ideais para cada workload. Trusted Advisor tambem identifica instancias ociosas, mas Compute Optimizer oferece recomendacoes mais detalhadas com estimativas de economia.

---

Voltar ao [Indice](../../../../index.md)
