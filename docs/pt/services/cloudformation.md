---
title: "Cloudformation"
---

# Cloudformation

## Descrição

Adicione uma breve descrição do serviço aqui.

## Links Úteis

- [Bem-vindo](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/Welcome.html)
- [Começando](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/getting-started.html)
- [Segurança](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/security.html)
- [Monitoramento](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/monitoring.html)
- [API](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/api.html)

## Tópicos Principais

### O que é o AWS CloudFormation?

AWS CloudFormation é um serviço que ajuda você a modelar e configurar seus recursos da AWS para que você possa
gaste menos tempo gerenciando esses recursos e mais tempo focando em seus aplicativos que
correr na AWS.Você cria um modelo que descreve todos os recursos da AWS que você deseja
(como as instâncias do Amazon EC2 ou instâncias do Amazon RDS DB), e o CloudFormation cuida do provisionamento e
Configurando esses recursos para você.Você não precisa criar e configurar individualmente
Recursos da AWS e descubra o que depende de quê;CloudFormation lida com isso.O
Os cenários a seguir demonstram como a CloudFormation pode ajudar.

Para um aplicativo Web escalável que também inclua um banco de dados de back -end, você pode usar um
Grupo de dimensionamento automático, um balanceador de carga de balanceamento de carga elástico e uma instância do banco de dados de serviço do banco de dados relacional da Amazon.Você pode usar
Cada serviço individual para provisionar esses recursos e depois de criar os recursos,
Você teria que configurá -los para trabalhar juntos.Todas essas tarefas podem adicionar complexidade
E tempo antes de você colocar seu aplicativo em funcionamento.

Em vez disso, você pode criar um modelo de formação de nuvem ou modificar um existente.A
O modelo descreve todos os seus recursos e suas propriedades.
Quando você usa esse modelo para criar uma pilha de formas de nuvem, o CloudFormation Disposition the Auto Scaling
grupo, balanceador de carga e banco de dados para você.Depois que a pilha tem sido com sucesso
Criados, seus recursos da AWS estão em funcionamento.Você pode excluir a pilha assim como
facilmente, que exclui todos os recursos da pilha.Ao usar o CloudFormation, você facilmente
Gerencie uma coleção de recursos como uma única unidade.

Se o seu aplicativo exigir disponibilidade adicional, você poderá replicá -lo em
Várias regiões para que, se uma região ficar indisponível, seus usuários ainda poderão usar
seu aplicativo em outras regiões.O desafio de replicar seu aplicativo é que
Também exige que você replique seus recursos.Você não apenas precisa gravar todo o
Recursos que seu aplicativo exige, mas você também deve provisionar e configurar
esses recursos em cada região.

## Exemplos de Uso

Adicione exemplos de uso do serviço aqui.

## Melhores Práticas

Adicione melhores práticas relacionadas ao uso do serviço aqui.

## Palavras-chave

Nenhuma palavra-chave disponível.
