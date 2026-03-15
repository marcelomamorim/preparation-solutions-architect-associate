# Questoes de Pratica - Parte 2: Cargas de Trabalho e Aplicacoes Seguras

> Teste seus conhecimentos sobre seguranca de rede, VPC e protecao de aplicacoes.

---

### Questao 1

Uma aplicacao em uma sub-rede privada precisa acessar o Amazon S3 sem que o trafego passe pela internet publica. Qual a melhor solucao?

**A)** Configurar um NAT Gateway na sub-rede publica

**B)** Criar um VPC Gateway Endpoint para S3

**C)** Mover a aplicacao para uma sub-rede publica

**D)** Usar um Internet Gateway

> **Resposta: B** - Um VPC Gateway Endpoint para S3 permite acesso direto ao S3 pela rede privada da AWS, sem custo adicional de transferencia de dados e sem expor o trafego a internet publica. NAT Gateway funcionaria, mas tem custo adicional e o trafego passa pelo NAT.

---

### Questao 2

Qual a diferenca principal entre Security Groups e Network ACLs?

**A)** Security Groups sao stateless e NACLs sao stateful

**B)** Security Groups operam no nivel da sub-rede e NACLs no nivel da instancia

**C)** Security Groups sao stateful e NACLs sao stateless

**D)** Nao ha diferenca, ambos funcionam da mesma forma

> **Resposta: C** - Security Groups sao stateful (o trafego de retorno e permitido automaticamente). NACLs sao stateless (voce precisa configurar regras de entrada E saida explicitamente). Security Groups operam no nivel da instancia, NACLs no nivel da sub-rede.

---

### Questao 3

Uma empresa precisa proteger sua aplicacao web contra ataques SQL injection e cross-site scripting (XSS). Qual servico deve ser usado?

**A)** AWS Shield Standard

**B)** Amazon GuardDuty

**C)** AWS WAF (Web Application Firewall)

**D)** AWS Network Firewall

> **Resposta: C** - O AWS WAF protege aplicacoes web contra exploits comuns como SQL injection e XSS. Pode ser associado ao CloudFront, ALB ou API Gateway. Shield protege contra DDoS. GuardDuty detecta ameacas. Network Firewall filtra trafego de rede.

---

### Questao 4

Uma instancia EC2 em uma sub-rede privada precisa baixar atualizacoes da internet. Qual componente de rede deve ser usado?

**A)** Internet Gateway

**B)** NAT Gateway em uma sub-rede publica

**C)** VPC Endpoint

**D)** VPC Peering

> **Resposta: B** - Um NAT Gateway em uma sub-rede publica permite que instancias em sub-redes privadas acessem a internet para downloads e atualizacoes, sem expor essas instancias a conexoes de entrada da internet.

---

### Questao 5

Uma empresa quer detectar automaticamente atividades maliciosas e comportamentos anomalos em suas contas AWS, como chamadas de API incomuns ou tentativas de acesso nao autorizadas. Qual servico usar?

**A)** AWS WAF

**B)** Amazon Inspector

**C)** Amazon GuardDuty

**D)** AWS Config

> **Resposta: C** - Amazon GuardDuty usa machine learning e analise de dados de CloudTrail, VPC Flow Logs e DNS para detectar ameacas automaticamente. Inspector avalia vulnerabilidades em EC2. WAF protege aplicacoes web. Config monitora conformidade de configuracao.

---

Voltar ao [Indice](../../../../index.md)
