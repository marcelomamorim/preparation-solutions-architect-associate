---
title: "Cloudfront"
---

# Cloudfront

## Descrição

Adicione uma breve descrição do serviço aqui.

## Links Úteis

- [Introduction](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html)
- [Gettingstarted](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/GettingStarted.html)
- [Security](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Security.html)
- [Monitoring](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Monitoring.html)
- [Api](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/API.html)

## Tópicos Principais

### What is Amazon CloudFront?

Amazon CloudFront is a web service that speeds up distribution of your static and dynamic web content,
		such as .html, .css, .js, and image files, to your users. CloudFront delivers your content through
		a worldwide network of data centers called edge locations. When a user requests content that
		you're serving with CloudFront, the request is routed to the edge location that provides the
		lowest latency (time delay), so that content is delivered with the best possible
		performance.

As an example, suppose that you're serving an image from a 
		traditional web server, not from CloudFront. For example, you might serve an image, sunsetphoto.png,
		using the URL https://example.com/sunsetphoto.png.

Your users can easily navigate to this URL and see the image. But they probably don't know that 
		their request is routed from one network to anotherâthrough the complex collection of 
		interconnected networks that comprise the internetâuntil the image is found.

CloudFront speeds up the distribution of your content by routing each user request through the
			AWS backbone network to the edge 
			location that can best serve your content. Typically, this is a CloudFront edge server that 
			provides the fastest delivery to the viewer. Using the AWS network dramatically reduces the number of 
			networks that your users' requests must pass through, which improves performance. Users get lower 
			latencyâthe time it takes to load the first byte of the fileâand higher data transfer rates.

## Exemplos de Uso

Adicione exemplos de uso do serviço aqui.

## Melhores Práticas

Adicione melhores práticas relacionadas ao uso do serviço aqui.
