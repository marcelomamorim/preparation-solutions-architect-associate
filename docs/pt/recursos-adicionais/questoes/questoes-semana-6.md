# Questoes de Pratica - Parte 6: Armazenamento e Computacao de Alto Desempenho

> Teste seus conhecimentos sobre S3, EBS, EFS, EC2, Lambda e estrategias de escalabilidade.

---

### Questao 1

Uma aplicacao de analise de dados precisa processar arquivos grandes armazenados no S3. Os arquivos sao acessados frequentemente durante os primeiros 30 dias e raramente depois. Qual estrategia de armazenamento otimiza custos?

**A)** Armazenar tudo no S3 Standard permanentemente

**B)** Configurar S3 Lifecycle Policy para mover objetos para S3 Standard-IA apos 30 dias e S3 Glacier apos 90 dias

**C)** Usar S3 One Zone-IA desde o inicio

**D)** Armazenar em EBS gp3

> **Resposta: B** - S3 Lifecycle Policies automatizam a transicao entre classes de armazenamento. S3 Standard para acesso frequente nos primeiros 30 dias, Standard-IA para acesso menos frequente, e Glacier para arquivamento de longo prazo. Isso otimiza custos automaticamente.

---

### Questao 2

Uma aplicacao de processamento de imagens precisa de armazenamento compartilhado acessivel por multiplas instancias EC2 em diferentes AZs simultaneamente. Qual servico de armazenamento e mais adequado?

**A)** Amazon EBS (Elastic Block Store)

**B)** Amazon S3

**C)** Amazon EFS (Elastic File System)

**D)** Instance Store

> **Resposta: C** - Amazon EFS e um sistema de arquivos NFS elastico que pode ser montado simultaneamente em multiplas instancias EC2 em diferentes AZs. EBS e anexado a uma unica instancia (exceto io2 com Multi-Attach). S3 e armazenamento de objetos, nao sistema de arquivos.

---

### Questao 3

Uma funcao Lambda e invocada por um API Gateway e precisa acessar um banco de dados RDS PostgreSQL. Durante picos de trafego, o banco de dados fica sobrecarregado com muitas conexoes. Qual solucao resolve esse problema?

**A)** Aumentar o tamanho da instancia RDS

**B)** Usar Amazon RDS Proxy entre Lambda e RDS

**C)** Migrar para DynamoDB

**D)** Aumentar a memoria da funcao Lambda

> **Resposta: B** - Amazon RDS Proxy gerencia um pool de conexoes compartilhadas com o banco de dados. Lambda cria muitas conexoes efemeras que sobrecarregam o RDS. O RDS Proxy reutiliza conexoes existentes, reduzindo a carga no banco e melhorando o tempo de failover.

---

### Questao 4

Uma empresa precisa de um volume EBS com o melhor custo-beneficio para uso geral, que suporte ate 16.000 IOPS e 1.000 MB/s de throughput. Qual tipo de volume e mais adequado?

**A)** gp2 (General Purpose SSD)

**B)** gp3 (General Purpose SSD)

**C)** io2 (Provisioned IOPS SSD)

**D)** st1 (Throughput Optimized HDD)

> **Resposta: B** - gp3 oferece 3.000 IOPS e 125 MB/s de baseline (inclusos no preco) e permite provisionar ate 16.000 IOPS e 1.000 MB/s independentemente do tamanho do volume. E mais economico que gp2, que vincula IOPS ao tamanho do volume.

---

### Questao 5

Uma aplicacao serverless processa eventos de um stream do Kinesis. A funcao Lambda precisa processar cada registro exatamente uma vez e na ordem correta. Qual configuracao e necessaria?

**A)** Usar SQS Standard como intermediario

**B)** Configurar Lambda com event source mapping para Kinesis com paralelismo por shard

**C)** Usar SNS para distribuir eventos

**D)** Configurar Lambda com invocacao assincrona

> **Resposta: B** - Lambda com event source mapping para Kinesis processa registros na ordem dentro de cada shard. O paralelismo e por shard, garantindo ordem. Use bisect batch on error para isolar registros problematicos e destination para falhas.

---

Voltar ao [Indice](../../../../index.md)
