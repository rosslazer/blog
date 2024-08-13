+++
author = "Ross Lazerowitz"
title = "Opportunities in Observability"
date = "2024-08-13"
description = "The next big thing in Observability won’t come from the old ways — it’s time for new approaches."
images = ["/images/o11y-header.jpg"]
tags = [
    "observability",
    "ideas",
    "lessons-learned"]

+++

After nearly a decade of working on observability products, I'm taking a much-needed break and working on the first human security company. With all those years under my belt, I still have an axe to grind. This post is my best effort to summarize some of the trends and opportunities I see in this space.

## An ELK-Like Stack Built on Top of an Open-Source Data Warehouse

At Splunk, I watched the ELK stack take the world by storm. Elasticsearch, which started as a general search index, found a killer use case in log workloads. They quickly integrated open-source components like Logstash and Kibana, retooling their platform to offer a packaged experience for working with log data. This effort marked the first open-source initiative that viewed logging as a search indexing problem akin to Splunk's commercial offering. Elastic gained traction by giving away what I initially considered an inferior product and managed to monetize it successfully.

It's now been 14 years since Elasticsearch launched, and the world of Observability has evolved. Log data volumes have surged, metrics and tracing have become staples, and security teams have started consolidating data into data lakes. As Elastic has focused on monetizing its cloud, managing self-hosted ELK has become increasingly challenging for Observability teams. This blind spot presents a wide opening and appetite for a new Open Source solution to Observability.

Several new commercial offerings, like my previous employer, Observe, have capitalized on the fact that a cloud data warehouse can satisfy all Observability workloads with minimal management. By separating storage and compute, this technology makes storing large amounts of data economical without the hassle of maintaining and indexing, allowing for on-demand compute power. Vendors have noticed this and begun utilizing commercial data warehouses and open-source efforts like Clickhouse. This solves the engine part of the puzzle, but we still need a good UI and open-source data ingestion layer. While some have pointed Grafana at these warehouses with SQL, much of the essential complexity from the data warehouse layer must be integrated before offering an experience on par with solutions like Datadog.

## AI and The Universal Abstraction Layer

Most data ingested into an Observability platform is emitted from searchable sources like Cloudwatch. Why do companies spend big bucks on ingesting tools like Datadog if the data is already searchable? The answer is simple \- to make the data useful. With the shift to DevOps, engineers with little ops training are now responsible for monitoring and investigating their services. Instead of learning five different tools with various query interfaces, companies pay vendors like Datadog to simplify usage for their engineers.

AI and Observability may be buzzwords, but their integration holds massive potential. An AI system capable of correlating data across different tools without centralizing it would enhance the user experience and save money. However, an AI would need help with five different query interfaces, just as an engineer would. Therefore, the key to building an "AI On-Call Engineer" lies in creating an abstraction layer for logs, metrics, traces, and configuration metadata across different providers. Once this exists, AI could triage issues effectively, solving the biggest problem: determining the right question to ask.

This approach might eliminate the need to centralize data. Existing vendors have no incentive to build this since they prefer collecting all the data and avoiding stateful systems. This solution might also make mass anomaly detection a viable approach to finding issues. Historically, these systems have been too noisy, but auto-triaging the noise would mitigate this problem.

## AI-Assisted Instrumentation

One of the biggest challenges in Observability, and any analytics domain, is having good data. Engineers have long depended on messy log data lacking foresight, structure, or agreed-upon conventions. Today, the problem is worse; we’ve layered metrics and distributed tracing on top of logs, tasking engineers with little ops training with new responsibilities.

Automated instrumentation is a lifeline for busy teams, providing visibility into their application in minutes. However, this data is limited. Automated instrumentation helps understand general functionality, but there's no free lunch when instrumenting an application's unique parts. Those unique parts usually represent the core value. There’s a significant opportunity for AI to assist here. Tools like co-pilot generate code, but no one has attempted to build a co-pilot for instrumenting applications. LLMs are already adept at generating comments. Building a co-pilot that enhances every engineer by judging and improving instrumentation is feasible with the right prompting and metadata.

## Looking forward 
The observability space is ripe for innovation, but the same old approaches [won't shape the future](https://x.com/rosslazer/status/1819833199515804014). We need radical and different takes on the problem space. Cheaper logs, metrics, or tracing solutions, AI copilots for troubleshooting, or better mobile app monitoring won't cut it. We need transformative ideas that address the fundamental challenges in new ways. The technology to do so is here \-  it’s just not evenly distributed yet.

