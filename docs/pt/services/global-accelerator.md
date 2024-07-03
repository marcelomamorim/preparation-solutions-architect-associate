---
title: "Global Accelerator"
---

# Global Accelerator

## Descrição

Adicione uma breve descrição do serviço aqui.

## Links Úteis

- [What Is Global Accelerator](https://docs.aws.amazon.com/global-accelerator/latest/dg/what-is-global-accelerator.html)
- [Getting Started](https://docs.aws.amazon.com/global-accelerator/latest/dg/getting-started.html)
- [Security](https://docs.aws.amazon.com/global-accelerator/latest/dg/security.html)
- [Monitoring](https://docs.aws.amazon.com/global-accelerator/latest/dg/monitoring.html)
- [Api](https://docs.aws.amazon.com/global-accelerator/latest/dg/api.html)

## Tópicos Principais

### What is AWS Global Accelerator?

AWS Global Accelerator is a service in which you create accelerators to improve the performance 
		of your applications for local and global users. Depending on the type of accelerator you choose, you can
		gain additional benefits: 

Global Accelerator is a global service that supports endpoints in multiple AWS Regions. To determine if Global Accelerator or 
		other services are currently supported in a specific AWS Region, see the 
		AWS 
			Regional Services List.

By default, Global Accelerator provides you with static IP addresses that you associate with your accelerator. The static IP addresses 
		are anycast from the AWS edge network. For IPv4, Global Accelerator provides two static IPv4 addresses. For dual-stack, Global Accelerator provides
		a total of four addresses: two static IPv4 addresses and two static IPv6 addresses. For IPv4, instead of using the addresses 
		that Global Accelerator provides, you can configure these entry points to be IPv4 addresses from your own IP address ranges that you 
		bring to Global Accelerator (BYOIP). 

For standard accelerators, Global Accelerator uses the AWS global network to route traffic to the optimal regional endpoint based
		on health, client location, and policies that you configure, which increases the availability of your applications. 
		Endpoints for standard accelerators can be Network Load Balancers, Application Load Balancers, Amazon EC2 instances, or Elastic IP addresses that are located in 
		one AWS Region or multiple Regions. The service reacts instantly to changes in health or configuration to 
		ensure that internet traffic from clients is always directed to healthy endpoints.

## Exemplos de Uso

Adicione exemplos de uso do serviço aqui.

## Melhores Práticas

Adicione melhores práticas relacionadas ao uso do serviço aqui.
