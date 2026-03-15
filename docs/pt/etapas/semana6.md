# Semana 6 - Armazenamento e Computacao de Alto Desempenho

> **Dominio 3 - Tarefas 3.1 a 3.3** | Tempo estimado: 8-10 horas de estudo

## Objetivos de Aprendizado

Ao final desta semana, voce devera ser capaz de:
- Selecionar o tipo de armazenamento correto (S3, EBS, EFS, FSx) para cada cenario
- Entender familias de instancias EC2 e quando usar cada uma
- Projetar solucoes de banco de dados de alto desempenho (RDS, Aurora, DynamoDB)
- Implementar estrategias de cache com ElastiCache
- Configurar Auto Scaling para computacao elastica

---

## Conhecimentos Necessarios

### Armazenamento
- **Armazenamento hibrido**: [Storage Gateway](https://aws.amazon.com/storagegateway/) - File, Volume, Tape
- **S3**: Classes de armazenamento, lifecycle policies, versionamento
- **EBS**: gp3 (SSD geral), io2 (alto IOPS), st1 (throughput HDD), sc1 (frio HDD)
- **EFS**: Sistema de arquivos NFS elastico, compartilhado entre instancias
- **FSx**: Windows File Server, Lustre (HPC)

### Computacao
- **Servicos**: [AWS Batch](https://aws.amazon.com/batch/), [EMR](https://aws.amazon.com/emr/), [Fargate](https://aws.amazon.com/fargate/), [Lambda](https://aws.amazon.com/lambda/)
- **Auto Scaling**: Target Tracking, Step Scaling, Scheduled Scaling
- **Containers**: [ECS](https://aws.amazon.com/ecs/) vs. [EKS](https://aws.amazon.com/eks/) vs. [Fargate](https://aws.amazon.com/fargate/)

### Banco de Dados
- **Relacional**: [RDS](https://aws.amazon.com/rds/), [Aurora](https://aws.amazon.com/rds/aurora/) - replicas de leitura, Multi-AZ
- **NoSQL**: [DynamoDB](https://aws.amazon.com/dynamodb/) - chave-valor, latencia em milissegundos
- **Cache**: [ElastiCache](https://aws.amazon.com/elasticache/) - Redis vs. Memcached
- **Proxy**: [RDS Proxy](https://aws.amazon.com/rds/proxy/) - pool de conexoes

## Habilidades Necessarias

- Selecionar servicos de armazenamento baseados em IOPS, throughput e latencia
- Desacoplar workloads para escalabilidade independente
- Selecionar tipos de instancia EC2 adequados (M, C, R, T, G/P)
- Configurar replicas de leitura e integrar caching
- Escolher entre bancos relacionais e nao-relacionais

---

## Dicas de Estudo para esta Semana

1. **EBS gp3 vs. gp2**: gp3 permite configurar IOPS e throughput independentemente do tamanho. gp2 vincula IOPS ao tamanho
2. **S3 vs. EFS vs. EBS**: S3 = objetos via HTTP. EFS = NFS compartilhado. EBS = bloco para uma instancia
3. **Aurora vs. RDS**: Aurora e 5x mais rapido que MySQL, 3x que PostgreSQL. Ate 15 replicas vs. 5 no RDS
4. **Redis vs. Memcached**: Redis tem persistencia, replicacao, pub/sub. Memcached e mais simples, multi-thread
5. **Lambda**: 15 min max, 10 GB memoria, 1000 concorrencia padrao. Use RDS Proxy para acessar bancos relacionais

## Recursos desta Semana

- [Questoes de pratica - Parte 6](../recursos-adicionais/questoes/questoes-semana-6.md)
- [Dominio 3 completo](../dominio/design-arquiteturas-alto-desempenho.md)

---

Voltar ao [Indice](../../../index.md)
