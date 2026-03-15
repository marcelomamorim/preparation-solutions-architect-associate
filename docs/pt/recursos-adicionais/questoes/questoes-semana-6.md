# Questões de Prática - Parte 6: Armazenamento e Computacao de Alto Desempenho

> Teste seus conhecimentos sobre S3, EBS, EFS, EC2, Lambda e estratégias de escalabilidade.

---

### Questao 1

Uma aplicação de análise de dados precisa processar arquivos grandes armazenados no S3. Os arquivos são acessados frequentemente durante os primeiros 30 dias e raramente depois. Qual estratégia de armazenamento otimiza custos?

**A)** Armazenar tudo no S3 Standard permanentemente

**B)** Configurar S3 Lifecycle Policy para mover objetos para S3 Standard-IA apos 30 dias e S3 Glacier apos 90 dias

**C)** Usar S3 One Zone-IA desde o inicio

**D)** Armazenar em EBS gp3

> **Resposta: B** - S3 Lifecycle Policies automatizam a transicao entre classes de armazenamento. S3 Standard para acesso frequente nos primeiros 30 dias, Standard-IA para acesso menos frequente, e Glacier para arquivamento de longo prazo. Isso otimiza custos automaticamente.

---

### Questao 2

Uma aplicação de processamento de imagens precisa de armazenamento compartilhado acessível por múltiplas instâncias EC2 em diferentes AZs simultaneamente. Qual serviço de armazenamento e mais adequado?

**A)** Amazon EBS (Elastic Block Store)

**B)** Amazon S3

**C)** Amazon EFS (Elastic File System)

**D)** Instance Store

> **Resposta: C** - Amazon EFS é um sistema de arquivos NFS elástico que pode ser montado simultaneamente em múltiplas instâncias EC2 em diferentes AZs. EBS e anexado a uma única instância (exceto io2 com Multi-Attach). S3 e armazenamento de objetos, não sistema de arquivos.

---

### Questao 3

Uma função Lambda e invocada por um API Gatéway e precisa acessar um banco de dados RDS PostgreSQL. Durante picos de tráfego, o banco de dados fica sobrecarregado com muitas conexões. Qual solução resolve esse problema?

**A)** Aumentar o tamanho da instância RDS

**B)** Usar Amazon RDS Proxy entre Lambda e RDS

**C)** Migrar para DynamoDB

**D)** Aumentar a memória da função Lambda

> **Resposta: B** - Amazon RDS Proxy gerencia um pool de conexões compartilhadas com o banco de dados. Lambda cria muitas conexões efemeras que sobrecarregam o RDS. O RDS Proxy reutiliza conexões existentes, reduzindo a carga no banco e melhorando o tempo de failover.

---

### Questao 4

Uma empresa precisa de um volume EBS com o melhor custo-benefício para uso geral, que suporte até 16.000 IOPS e 1.000 MB/s de throughput. Qual tipo de volume e mais adequado?

**A)** gp2 (General Purpose SSD)

**B)** gp3 (General Purpose SSD)

**C)** io2 (Provisioned IOPS SSD)

**D)** st1 (Throughput Optimized HDD)

> **Resposta: B** - gp3 oferece 3.000 IOPS e 125 MB/s de baseline (inclusos no preço) e permite provisionar até 16.000 IOPS e 1.000 MB/s independentemente do tamanho do volume. E mais econômico que gp2, que vincula IOPS ao tamanho do volume.

---

### Questao 5

Uma aplicação serverless processa eventos de um stream do Kinesis. A função Lambda precisa processar cada registro exatamente uma vez e na ordem correta. Qual configuração e necessária?

**A)** Usar SQS Standard como intermediario

**B)** Configurar Lambda com event source mapping para Kinesis com paralelismo por shard

**C)** Usar SNS para distribuir eventos

**D)** Configurar Lambda com invocacao assincrona

> **Resposta: B** - Lambda com event source mapping para Kinesis processa registros na ordem dentro de cada shard. O paralelismo e por shard, garantindo ordem. Use bisect batch on error para isolar registros problematicos e destination para falhas.

---

Voltar ao [Índice](../../../../index.md)
