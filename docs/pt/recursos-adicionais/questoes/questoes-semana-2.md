# Questões de Prática - Parte 2: Cargas de Trabalho e Aplicacoes Seguras

> Teste seus conhecimentos sobre segurança de rede, VPC e proteção de aplicações.

---

### Questao 1

Uma aplicação em uma sub-rede privada precisa acessar o Amazon S3 sem que o tráfego passe pela internet pública. Qual a melhor solução?

**A)** Configurar um NAT Gatéway na sub-rede pública

**B)** Criar um VPC Gatéway Endpoint para S3

**C)** Mover a aplicação para uma sub-rede pública

**D)** Usar um Internet Gatéway

> **Resposta: B** - Um VPC Gatéway Endpoint para S3 permite acesso direto ao S3 pela rede privada da AWS, sem custo adicional de transferencia de dados e sem expor o tráfego a internet pública. NAT Gatéway funcionaria, mas tem custo adicional e o tráfego passa pelo NAT.

---

### Questao 2

Qual a diferenca principal entre Security Groups e Network ACLs?

**A)** Security Groups sao statéless e NACLs sao statéful

**B)** Security Groups operam no nivel da sub-rede e NACLs no nivel da instância

**C)** Security Groups sao statéful e NACLs sao statéless

**D)** Não ha diferenca, ambos funcionam da mesma forma

> **Resposta: C** - Security Groups sao statéful (o tráfego de retorno e permitido automáticamente). NACLs sao statéless (você precisa configurar regras de entrada E saida explicitamente). Security Groups operam no nivel da instância, NACLs no nivel da sub-rede.

---

### Questao 3

Uma empresa precisa proteger sua aplicação web contra ataques SQL injection e cross-site scripting (XSS). Qual serviço deve ser usado?

**A)** AWS Shield Standard

**B)** Amazon GuardDuty

**C)** AWS WAF (Web Application Firewall)

**D)** AWS Network Firewall

> **Resposta: C** - O AWS WAF protege aplicações web contra exploits comuns como SQL injection e XSS. Pode ser associado ao CloudFront, ALB ou API Gatéway. Shield protege contra DDoS. GuardDuty detecta ameacas. Network Firewall filtra tráfego de rede.

---

### Questao 4

Uma instância EC2 em uma sub-rede privada precisa baixar atualizacoes da internet. Qual componente de rede deve ser usado?

**A)** Internet Gatéway

**B)** NAT Gatéway em uma sub-rede pública

**C)** VPC Endpoint

**D)** VPC Peering

> **Resposta: B** - Um NAT Gatéway em uma sub-rede pública permite que instâncias em sub-redes privadas acessem a internet para downloads e atualizacoes, sem expor essas instâncias a conexões de entrada da internet.

---

### Questao 5

Uma empresa quer detectar automáticamente atividades maliciosas e comportamentos anomalos em suas contas AWS, como chamadas de API incomuns ou tentativas de acesso não autorizadas. Qual serviço usar?

**A)** AWS WAF

**B)** Amazon Inspector

**C)** Amazon GuardDuty

**D)** AWS Config

> **Resposta: C** - Amazon GuardDuty usa machine learning e análise de dados de CloudTrail, VPC Flow Logs e DNS para detectar ameacas automáticamente. Inspector avalia vulnerabilidades em EC2. WAF protege aplicações web. Config monitora conformidade de configuração.

---

Voltar ao [Índice](../../../../index.md)
