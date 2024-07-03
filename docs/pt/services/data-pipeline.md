---
title: "Data Pipeline"
---

# Data Pipeline

## Descrição

Adicione uma breve descrição do serviço aqui.

## Links Úteis

- [What Is Datapipeline](https://docs.aws.amazon.com/datapipeline/latest/DeveloperGuide/what-is-datapipeline.html)
- [Dp Managing Pipeline](https://docs.aws.amazon.com/datapipeline/latest/DeveloperGuide/dp-managing-pipeline.html)
- [Dp Concepts](https://docs.aws.amazon.com/datapipeline/latest/DeveloperGuide/dp-concepts.html)
- [Dp Templates](https://docs.aws.amazon.com/datapipeline/latest/DeveloperGuide/dp-templates.html)
- [Dp Activities](https://docs.aws.amazon.com/datapipeline/latest/DeveloperGuide/dp-activities.html)

## Tópicos Principais

### What is AWS Data Pipeline?

AWS Data Pipeline is a web service that you can use to automate the movement and transformation of
        data. With AWS Data Pipeline, you can define data-driven workflows, so that tasks can be dependent on
        the successful completion of previous tasks. You define the parameters of your data
        transformations and AWS Data Pipeline enforces the logic that you've set up. 

The following components of AWS Data Pipeline work together to manage your data:

 For example, you can use AWS Data Pipeline to archive your web server's logs to Amazon Simple Storage Service (Amazon S3)
        each day and then run a weekly Amazon EMR (Amazon EMR) cluster over those logs to generate traffic
        reports. AWS Data Pipeline schedules the daily tasks to copy data and the weekly task to launch the
        Amazon EMR cluster. AWS Data Pipeline also ensures that Amazon EMR waits for the final day's data to be uploaded
        to Amazon S3 before it begins its analysis, even if there is an unforeseen delay in uploading the
        logs.

You can create, access, and manage your pipelines using any of the following
            interfaces:

## Exemplos de Uso

Adicione exemplos de uso do serviço aqui.

## Melhores Práticas

Adicione melhores práticas relacionadas ao uso do serviço aqui.
