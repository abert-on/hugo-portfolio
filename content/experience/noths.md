---
title: Not on the High Street
description: Senior Engineer | 09/2019 - 02/2023
image: "/images/noths.png"
tags: ['Java', 'Spring', 'Spring Boot', 'Spring WebFlux', 'ECS', 'Lambda', 'CloudFormation', 'DynamoDB', 'SQS', 'SNS', 'Hazelcast', 'Terraform', 'Redis', 'Gradle', 'Maven']
weight: 1
---

## Company

An e-commerce marketplace, specialising in championing small businesses and helping customers find the perfect gifts. 

## Role

Senior Engineer

## Projects

### Product Management

Building a new product management service. Starting with creating new APIs to allow partners to add new product metadata to help surface their products in search results. A Spring Boot service deployed to ECS using CloudFormation and with RDS (MySQL) for persisting the data. 

![Product Management](/images/prdmgt.png)

### Product Listings and Search

A complete re-platforming of the backend functionality that powered search and category listings. Starting with facade APIs over the legacy monolith, allowing us to create new API specs and ensure high test coverage before re-writing functionality. 

Using Spring WebFlux and Reactive program to ensure high throughput and minimal overhead in calling the new APIs. Use of Elasticache (Redis) to further improve performance, as demonstrated via extensive JMeter testing. 

Gradually taking over logic to call a 3rd party provider to get the product listings information.. By replatforming we were then more easily able to experiment with new filters through A/B testing. 

![Filters](/images/filters.png)

Successfully migrated all search functionality to the new service, allowing it to service all search requests independently. 

### Product Catalog

The creation of a new backend service that would provide a centralised view of all product data to both the customers and 3rd parties. 

![Product Details](/images/pdp.png)

Starting as another Spring Webflux facade API, and gradually taking capturing the various different bits of product data. 

Subscribed to various SNS topics to pull in data from other systems, initially using Lambdas and DynamoDB to process and store the information from these messages. Then moved on to creating a Haazelcast cluster that would process and store the information whilst provided excellent read performance to the product APIs.

Also responsible for exporting product data to 3rd parties via S3 and FTP. 

### Version Controlled Monitors and Alerts

Moved our existing DataDog alerts and monitors to version control. Changes then work through a pipeline where they are checked, approved and any changes applied using [Terraform](https://registry.terraform.io/providers/DataDog/datadog/latest/docs). Provided a history of changes and greater portability. 


