---
title: "Fargate"
---

# Fargate

## Descrição

Adicione uma breve descrição do serviço aqui.

## Links Úteis

- [Aws_Fargate](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/AWS_Fargate.html)
- [Getting Started](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/getting-started.html)
- [Security](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/security.html)
- [Monitoring](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/monitoring.html)
- [Api](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/api.html)

## Tópicos Principais

### AWS Fargate for Amazon ECS

AWS Fargate is a technology that you can use with Amazon ECS to run containers without having to manage
        servers or clusters of Amazon EC2 instances. With AWS Fargate, you no longer have to
        provision, configure, or scale clusters of virtual machines to run containers. This removes
        the need to choose server types, decide when to scale your clusters, or optimize cluster
        packing.

When you run your tasks and services with the Fargate launch type, you
        package your application in containers, specify the CPU and memory requirements, define
        networking and IAM policies, and launch the application. Each Fargate task
        has its own isolation boundary and does not share the underlying kernel, CPU resources,
        memory resources, or elastic network interface with another task. You configure your task
        definitions for Fargate by setting the requiresCompatibilities
        task definition parameter to FARGATE. For more information, see Launch types.

Fargate offers platform versions for Amazon Linux 2 and Microsoft Windows 2019 Server
        Full and Core editions. Unless otherwise specified, the information on this page applies to
        all Fargate platforms.

This topic describes the different components of Fargate tasks and services,
        and calls out special considerations for using Fargate with Amazon ECS.

## Exemplos de Uso

Adicione exemplos de uso do serviço aqui.

## Melhores Práticas

Adicione melhores práticas relacionadas ao uso do serviço aqui.
