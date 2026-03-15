# Questoes de Pratica - Parte 5: Alta Disponibilidade e Recuperacao de Desastres

> Teste seus conhecimentos sobre Multi-AZ, failover, estrategias de DR e monitoramento.

---

### Questao 1

Uma empresa precisa garantir que seu banco de dados RDS MySQL esteja disponivel mesmo se uma Zona de Disponibilidade inteira falhar. Qual configuracao atende a esse requisito?

**A)** Criar replicas de leitura na mesma AZ

**B)** Habilitar Multi-AZ para o RDS

**C)** Aumentar o tamanho da instancia RDS

**D)** Fazer backups manuais a cada hora

> **Resposta: B** - RDS Multi-AZ cria uma replica sincrona em outra AZ. Em caso de falha da AZ primaria, o failover automatico ocorre em 60-120 segundos. Replicas de leitura sao para distribuir carga de leitura, nao para failover automatico.

---

### Questao 2

Uma aplicacao critica precisa de um RTO (Recovery Time Objective) de minutos e um RPO (Recovery Point Objective) proximo de zero. A empresa tem orcamento limitado. Qual estrategia de DR e mais adequada?

**A)** Backup & Restore

**B)** Pilot Light

**C)** Warm Standby

**D)** Active-Active (Multi-site)

> **Resposta: C** - Warm Standby mantem uma versao reduzida do ambiente em execucao em outra regiao, permitindo RTO de minutos. Pilot Light tambem oferece RTO de minutos, mas precisa escalar recursos durante o DR. Active-Active tem RTO quase zero, mas custa muito mais.

---

### Questao 3

Uma aplicacao usa Route 53 para DNS e precisa redirecionar trafego automaticamente para uma regiao de backup quando a regiao primaria ficar indisponivel. Qual politica de roteamento deve ser usada?

**A)** Simple Routing

**B)** Weighted Routing

**C)** Failover Routing com health checks

**D)** Latency-based Routing

> **Resposta: C** - Failover Routing com health checks monitora a saude do endpoint primario e redireciona automaticamente para o endpoint secundario quando o primario falha. Health checks verificam a disponibilidade a cada 10 ou 30 segundos.

---

### Questao 4

Uma empresa precisa monitorar a utilizacao de CPU de suas instancias EC2 e receber alertas automaticos quando a CPU ultrapassar 80% por mais de 5 minutos. Qual servico e configuracao deve ser usada?

**A)** AWS CloudTrail com filtros de eventos

**B)** Amazon CloudWatch Alarms com metrica CPUUtilization e periodo de 5 minutos

**C)** AWS Config com regras personalizadas

**D)** Amazon GuardDuty com detectores personalizados

> **Resposta: B** - CloudWatch Alarms monitora metricas (como CPUUtilization) e dispara acoes (notificacao SNS, Auto Scaling) quando o limiar e atingido por um periodo especificado. CloudTrail registra chamadas de API, nao metricas de recursos.

---

### Questao 5

Uma empresa quer replicar dados do S3 automaticamente para outra regiao AWS para fins de disaster recovery. Qual recurso do S3 deve ser configurado?

**A)** S3 Transfer Acceleration

**B)** S3 Cross-Region Replication (CRR)

**C)** S3 Lifecycle Policies

**D)** S3 Versioning apenas

> **Resposta: B** - S3 Cross-Region Replication (CRR) replica automaticamente objetos para um bucket em outra regiao. Requer que o versionamento esteja habilitado em ambos os buckets. E essencial para estrategias de DR que envolvem dados no S3.

---

Voltar ao [Indice](../../../../index.md)
