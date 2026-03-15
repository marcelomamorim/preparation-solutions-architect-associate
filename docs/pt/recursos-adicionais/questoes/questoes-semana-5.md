# Questões de Prática - Parte 5: Alta Disponibilidade e Recuperação de Desastrês

> Teste seus conhecimentos sobre Multi-AZ, failover, estratégias de DR e monitoramento.

---

### Questao 1

Uma empresa precisa garantir que seu banco de dados RDS MySQL esteja disponível mesmo se uma Zona de Disponibilidade inteira falhar. Qual configuração aténde a esse requisito?

**A)** Criar replicas de leitura na mesma AZ

**B)** Habilitar Multi-AZ para o RDS

**C)** Aumentar o tamanho da instância RDS

**D)** Fazer backups manuais a cada hora

> **Resposta: B** - RDS Multi-AZ cria uma replica sincrona em outra AZ. Em caso de falha da AZ primaria, o failover automático ocorre em 60-120 segundos. Replicas de leitura são para distribuir carga de leitura, não para failover automático.

---

### Questao 2

Uma aplicação crítica precisa de um RTO (Recovery Time Objective) de minutos é um RPO (Recovery Point Objective) próximo de zero. A empresa tem orçamento limitado. Qual estratégia de DR e mais adequada?

**A)** Backup & Restore

**B)** Pilot Light

**C)** Warm Standby

**D)** Active-Active (Multi-site)

> **Resposta: C** - Warm Standby mantem uma versão reduzida do ambiente em execucao em outra região, permitindo RTO de minutos. Pilot Light também oferece RTO de minutos, mas precisa escalar recursos durante o DR. Active-Active tem RTO quase zero, mas custa muito mais.

---

### Questao 3

Uma aplicação usa Route 53 para DNS e precisa redirecionar tráfego automaticamente para uma região de backup quando a região primaria ficar indisponível. Qual política de roteamento deve ser usada?

**A)** Simple Routing

**B)** Weighted Routing

**C)** Failover Routing com health checks

**D)** Laténcy-based Routing

> **Resposta: C** - Failover Routing com health checks monitora a saúde do endpoint primário e redireciona automaticamente para o endpoint secundário quando o primário falha. Health checks verificam a disponibilidade a cada 10 ou 30 segundos.

---

### Questao 4

Uma empresa precisa monitorar a utilização de CPU de suas instâncias EC2 e receber alertas automáticos quando a CPU ultrapassar 80% por mais de 5 minutos. Qual serviço e configuração deve ser usada?

**A)** AWS CloudTrail com filtros de eventos

**B)** Amazon CloudWatch Alarms com métrica CPUUtilization e periodo de 5 minutos

**C)** AWS Config com regras personalizadas

**D)** Amazon GuardDuty com detectores personalizados

> **Resposta: B** - CloudWatch Alarms monitora métricas (como CPUUtilization) e dispara acoes (notificação SNS, Auto Scaling) quando o limiar e atingido por um periodo específicado. CloudTrail registra chamadas de API, não métricas de recursos.

---

### Questao 5

Uma empresa quer replicar dados do S3 automaticamente para outra região AWS para fins de disaster recovery. Qual recurso do S3 deve ser configurado?

**A)** S3 Transfer Acceleration

**B)** S3 Cross-Region Replication (CRR)

**C)** S3 Lifecycle Policies

**D)** S3 Versioning apenas

> **Resposta: B** - S3 Cross-Region Replication (CRR) replica automaticamente objetos para um bucket em outra região. Requer que o versionamento esteja habilitado em ambos os buckets. E essencial para estratégias de DR que envolvem dados no S3.

---

Voltar ao [Índice](../../../../index.md)
