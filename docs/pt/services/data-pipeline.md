---
title: "Data Pipeline"
---

# Data Pipeline

## Descrição

Adicione uma breve descrição do serviço aqui.

## Links Úteis

- [O que é DatapiPine](https://docs.aws.amazon.com/datapipeline/latest/DeveloperGuide/what-is-datapipeline.html)
- [Pipeline de gerenciamento de DP](https://docs.aws.amazon.com/datapipeline/latest/DeveloperGuide/dp-managing-pipeline.html)
- [Conceitos de DP](https://docs.aws.amazon.com/datapipeline/latest/DeveloperGuide/dp-concepts.html)
- [Modelos de dp](https://docs.aws.amazon.com/datapipeline/latest/DeveloperGuide/dp-templates.html)
- [Atividades de DP](https://docs.aws.amazon.com/datapipeline/latest/DeveloperGuide/dp-activities.html)

## Tópicos Principais

### O que é a AWS Data Pipeline?

AWS Data Pipeline é um serviço da web que você pode usar para automatizar o movimento e a transformação de
dados.Com o pipeline de dados da AWS, você pode definir fluxos de trabalho orientados a dados, para que as tarefas possam depender
a conclusão bem -sucedida de tarefas anteriores.Você define os parâmetros de seus dados
Transformações e Pipeline de dados da AWS aplicam a lógica que você configurou.

Os seguintes componentes do pipeline de dados da AWS trabalham juntos para gerenciar seus dados:

Por exemplo, você pode usar o AWS Data Pipeline para arquivar os logs do seu servidor da web no Amazon Simple Storage Service (Amazon S3)
Todos os dias e depois executa um cluster semanal da Amazon EMR (Amazon EMR) sobre esses logs para gerar tráfego
relatórios.AWS Data Pipeline agenda as tarefas diárias para copiar dados e a tarefa semanal para lançar o
Amazon EMR Cluster.O AWS Data Pipeline também garante que a Amazon EMR aguarde que os dados do dia final sejam carregados
para a Amazon S3 antes de começar sua análise, mesmo que haja um atraso imprevisto no upload do
Histórico.

Você pode criar, acessar e gerenciar seus dutos usando qualquer um dos seguintes
interfaces:

## Exemplos de Uso

Adicione exemplos de uso do serviço aqui.

## Melhores Práticas

Adicione melhores práticas relacionadas ao uso do serviço aqui.

## Palavras-chave

Nenhuma palavra-chave disponível.
