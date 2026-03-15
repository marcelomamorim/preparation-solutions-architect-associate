# Questoes de Pratica - Parte 8: Rede, Migracao e Revisao Geral

> Teste seus conhecimentos sobre rede, otimizacao de custos de rede, migracao e conceitos transversais.

---

### Questao 1

Uma empresa precisa conectar seu data center on-premises a uma VPC da AWS com conexao dedicada de alta largura de banda e latencia consistente. Qual servico deve ser usado?

**A)** AWS Site-to-Site VPN

**B)** AWS Direct Connect

**C)** AWS Transit Gateway

**D)** VPC Peering

> **Resposta: B** - AWS Direct Connect estabelece uma conexao de rede dedicada entre o data center e a AWS, oferecendo largura de banda consistente (1 Gbps ou 10 Gbps) e latencia mais previsivel que uma VPN via internet. Para redundancia, combine com VPN como backup.

---

### Questao 2

Uma empresa quer reduzir os custos de transferencia de dados ao servir conteudo estatico (imagens, CSS, JavaScript) para usuarios globais. Qual servico e mais adequado?

**A)** Amazon S3 com Transfer Acceleration

**B)** Amazon CloudFront como CDN na frente do S3

**C)** AWS Global Accelerator

**D)** Elastic Load Balancer em multiplas regioes

> **Resposta: B** - CloudFront cacheia conteudo em edge locations proximas aos usuarios, reduzindo a latencia e os custos de transferencia de dados do S3. O custo de egress do CloudFront e menor que o egress direto do S3. Global Accelerator e melhor para aplicacoes dinamicas.

---

### Questao 3

Uma aplicacao em uma VPC precisa acessar o DynamoDB sem que o trafego passe pela internet. Qual tipo de VPC Endpoint deve ser criado?

**A)** VPC Interface Endpoint

**B)** VPC Gateway Endpoint

**C)** NAT Gateway

**D)** Internet Gateway

> **Resposta: B** - DynamoDB e S3 usam Gateway Endpoints (gratuitos). A maioria dos outros servicos AWS usa Interface Endpoints (com custo por hora e por GB). Gateway Endpoints adicionam uma entrada na tabela de roteamento da sub-rede.

---

### Questao 4

Uma empresa precisa migrar 50 TB de dados do data center on-premises para o Amazon S3. A conexao de internet tem largura de banda limitada de 100 Mbps. Qual servico oferece a forma mais rapida de migrar esses dados?

**A)** Transferir via internet usando S3 multipart upload

**B)** Usar AWS DataSync

**C)** Usar AWS Snowball Edge

**D)** Configurar Direct Connect

> **Resposta: C** - AWS Snowball Edge e um dispositivo fisico que pode armazenar ate 80 TB. A AWS envia o dispositivo, voce carrega os dados localmente e devolve para a AWS, que transfere para o S3. Com 100 Mbps, 50 TB levaria ~46 dias via internet. Snowball pode completar em ~1 semana incluindo envio.

---

### Questao 5

Uma empresa usa CloudFormation para gerenciar toda sua infraestrutura. Apos uma atualizacao, um stack falhou e precisa ser revertido. Qual e a melhor abordagem?

**A)** Deletar o stack e criar um novo manualmente

**B)** Usar o rollback automatico do CloudFormation

**C)** Editar os recursos manualmente no console

**D)** Criar um novo stack com um nome diferente

> **Resposta: B** - CloudFormation tem rollback automatico: se uma atualizacao de stack falhar, ele reverte automaticamente para o estado anterior. Voce tambem pode usar Change Sets para visualizar mudancas antes de aplica-las, reduzindo o risco de falhas.

---

Voltar ao [Indice](../../../../index.md)
