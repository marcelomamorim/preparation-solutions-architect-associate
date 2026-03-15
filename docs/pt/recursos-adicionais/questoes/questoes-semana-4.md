# Questoes de Pratica - Parte 4: Arquiteturas Escalaveis e Desacopladas

> Teste seus conhecimentos sobre desacoplamento, escalabilidade, containers e mensageria.

---

### Questao 1

Uma aplicacao web experimenta picos de trafego imprevisiveis. A equipe quer garantir que a aplicacao escale automaticamente para atender a demanda e reduza custos nos periodos de baixo trafego. Qual solucao e mais adequada?

**A)** Aumentar manualmente o numero de instancias EC2 antes dos picos esperados

**B)** Usar instancias EC2 maiores (escala vertical)

**C)** Configurar um Auto Scaling Group com politica de Target Tracking baseada em CPU

**D)** Usar uma unica instancia EC2 muito grande

> **Resposta: C** - Auto Scaling com Target Tracking ajusta automaticamente o numero de instancias para manter a metrica alvo (ex: CPU em 60%). Escala para cima durante picos e para baixo em periodos ociosos, otimizando custos.

---

### Questao 2

Uma aplicacao de processamento de pedidos precisa garantir que nenhum pedido seja perdido, mesmo se o servico de processamento ficar temporariamente indisponivel. Qual padrao de arquitetura e mais adequado?

**A)** Chamada sincrona direta entre os servicos

**B)** Usar Amazon SQS entre o servico de recebimento e o servico de processamento

**C)** Armazenar pedidos em um arquivo CSV no EBS

**D)** Usar Amazon CloudFront para cache de pedidos

> **Resposta: B** - Amazon SQS desacopla os servicos. Os pedidos sao armazenados na fila e processados quando o servico de processamento estiver disponivel. Mensagens persistem por ate 14 dias. Use Dead Letter Queue para mensagens que falham repetidamente.

---

### Questao 3

Uma aplicacao precisa enviar notificacoes para multiplos sistemas simultaneamente quando um evento ocorre (email, SMS, fila de processamento). Qual padrao deve ser usado?

**A)** Amazon SQS com polling de cada sistema

**B)** Amazon SNS com topico e multiplas subscricoes (fan-out)

**C)** Amazon EventBridge com regra unica

**D)** Chamadas HTTP diretas para cada sistema

> **Resposta: B** - O padrao fan-out com SNS permite publicar uma mensagem em um topico e entrega-la a multiplos assinantes simultaneamente (email via SES, SMS, filas SQS, funcoes Lambda, endpoints HTTP). E o padrao classico de pub/sub na AWS.

---

### Questao 4

Uma empresa quer executar containers Docker sem gerenciar servidores ou clusters. Qual combinacao de servicos e mais adequada?

**A)** Amazon EC2 com Docker instalado manualmente

**B)** Amazon ECS com tipo de lancamento Fargate

**C)** Amazon EKS com instancias EC2 gerenciadas

**D)** AWS Lambda com layers de container

> **Resposta: B** - Amazon ECS com Fargate e a opcao serverless para containers. Voce define a tarefa (CPU, memoria, imagem) e o Fargate gerencia toda a infraestrutura. Nao precisa provisionar, configurar ou escalar clusters de servidores.

---

### Questao 5

Qual tipo de Elastic Load Balancer e mais adequado para uma aplicacao que precisa de roteamento baseado em path URL (ex: /api/* para um grupo de servidores e /images/* para outro)?

**A)** Classic Load Balancer (CLB)

**B)** Network Load Balancer (NLB)

**C)** Application Load Balancer (ALB)

**D)** Gateway Load Balancer (GLB)

> **Resposta: C** - O Application Load Balancer (ALB) opera na camada 7 (HTTP/HTTPS) e suporta roteamento baseado em path, host header, query string e headers HTTP. NLB opera na camada 4 (TCP/UDP) e nao tem visibilidade do conteudo HTTP.

---

Voltar ao [Indice](../../../../index.md)
