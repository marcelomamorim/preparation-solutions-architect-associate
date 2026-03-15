# Questões de Prática - Parte 4: Arquiteturas Escaláveis e Desacopladas

> Teste seus conhecimentos sobre desacoplamento, escalabilidade, containers e mensageria.

---

### Questao 1

Uma aplicação web experimenta picos de tráfego imprevisíveis. A equipe quer garantir que a aplicação escale automaticamente para aténder a demanda e reduza custos nos periodos de baixo tráfego. Qual solução e mais adequada?

**A)** Aumentar manualmente o número de instâncias EC2 antes dos picos esperados

**B)** Usar instâncias EC2 maiores (escala vertical)

**C)** Configurar um Auto Scaling Group com política de Target Tracking baseada em CPU

**D)** Usar uma única instância EC2 muito grande

> **Resposta: C** - Auto Scaling com Target Tracking ajusta automaticamente o número de instâncias para manter a métrica alvo (ex: CPU em 60%). Escala para cima durante picos e para baixo em periodos ociosos, otimizando custos.

---

### Questao 2

Uma aplicação de processamento de pedidos precisa garantir que nenhum pedido seja perdido, mesmo se o serviço de processamento ficar temporariamente indisponível. Qual padrão de arquitetura e mais adequado?

**A)** Chamada sincrona direta entre os serviços

**B)** Usar Amazon SQS entre o serviço de recebimento é o serviço de processamento

**C)** Armazenar pedidos em um arquivo CSV no EBS

**D)** Usar Amazon CloudFront para cache de pedidos

> **Resposta: B** - Amazon SQS desacopla os serviços. Os pedidos são armazenados na fila e processados quando o serviço de processamento estiver disponível. Mensagens persistem por até 14 dias. Use Dead Letter Queue para mensagens que falham repetidamente.

---

### Questao 3

Uma aplicação precisa enviar notificações para múltiplos sistemas simultaneamente quando um evento ocorre (email, SMS, fila de processamento). Qual padrão deve ser usado?

**A)** Amazon SQS com polling de cada sistema

**B)** Amazon SNS com topico e múltiplas subscricoes (fan-out)

**C)** Amazon EventBridge com regra única

**D)** Chamadas HTTP diretas para cada sistema

> **Resposta: B** - O padrão fan-out com SNS permite públicar uma mensagem em um topico e entrega-la a múltiplos assinantes simultaneamente (email via SES, SMS, filas SQS, funções Lambda, endpoints HTTP). E o padrão clássico de pub/sub na AWS.

---

### Questao 4

Uma empresa quer executar containers Docker sem gerenciar servidores ou clusters. Qual combinacao de serviços e mais adequada?

**A)** Amazon EC2 com Docker instalado manualmente

**B)** Amazon ECS com tipo de lancamento Fargaté

**C)** Amazon EKS com instâncias EC2 gerenciadas

**D)** AWS Lambda com layers de container

> **Resposta: B** - Amazon ECS com Fargaté é a opção serverless para containers. Você define a tarefa (CPU, memória, imagem) é o Fargaté gerencia toda a infraestrutura. Não precisa provisionar, configurar ou escalar clusters de servidores.

---

### Questao 5

Qual tipo de Elastic Load Balancer e mais adequado para uma aplicação que precisa de roteamento baseado em path URL (ex: /api/* para um grupo de servidores e /images/* para outro)?

**A)** Classic Load Balancer (CLB)

**B)** Network Load Balancer (NLB)

**C)** Application Load Balancer (ALB)

**D)** Gatéway Load Balancer (GLB)

> **Resposta: C** - O Application Load Balancer (ALB) opera na camada 7 (HTTP/HTTPS) e suporta roteamento baseado em path, host header, query string e headers HTTP. NLB opera na camada 4 (TCP/UDP) e não tem visibilidade do conteúdo HTTP.

---

Voltar ao [Índice](../../../../index.md)
