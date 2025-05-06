## Description
{:#description}

This tutorial introduces RDF Connect (RDFC), a novel, language-agnostic framework for constructing streaming data processing pipelines. By leveraging the Resource Description Framework (RDF) and the PROV-O ontology, RDFC enables the creation of pipelines that seamlessly integrate processors implemented in multiple programming languages.

Key Tutorial Highlights:

- **Language Agnostic**: Create processors in any programming language
- **Provenance-Driven**: Describe pipelines using RDF and PROV-O ontology
- **Hands-On Learning**: Build custom processors and complete pipelines

Tutorial Practical Project:
Participants will construct a machine learning pipeline that:

- Extracts weather data using JavaScript
- Ingests data into a Python-based ML model

By the end of the tutorial, you'll understand how to:

- Design language-independent data processing pipelines
- Create custom processors for diverse data sources
- Leverage RDF for comprehensive pipeline documentation


## Motivation
{:#motivation}

In today's fragmented data ecosystem, RDF libraries are spread across multiple programming languages, making data transformations complex and challenging. RDF Connect solves this by:

- Unifying data processing across language boundaries
- Enabling custom processors tailored to specific needs
- Providing comprehensive provenance tracking using PROV-O ontology

With the rise of Large Language Models (LLMs), provenance has never been more critical. RDF Connect allows you to:
- Publish pipeline configurations alongside generated datasets
- Trace data lineage and origin
- Streamline machine learning training by intelligently pruning data sources


## Format and Schedule
{:#description}

We plan a full day for this tutorial as shown in [](#planning).

The tutorial is structured into four distinct sessions.

The first session provides an introduction to RDF Connect, highlighting its language-agnostic processor architecture. This session includes an overview of the tutorial's content, as well as a detailed description of the pipeline participants will build throughout the day.

The second session delves into the process of building a custom processor. Participants will learn how to create a processor configuration and implement a client for the weather endpoint.

The third session focuses on building a pipeline using the processor created in the previous session. Participants will build a machine learning pipeline that consumes the weather information in their favorite model.

The fourth session is a hackathon, where all participants work together to either extend the pipeline created in the previous session with new data sources, or build a new pipeline using existing processors to achieve a different goal.


<figure id="planning" markdown="1" class="table">

|                                               | Topic | Duration |
|-----------------------------------------------|-------|----------|
| **Morning 1: Introduction** (_1:20_)          | Introduction | 0:10   |
|                                               | Introduction to RDF Connect Processors  | 0:40   |
|                                               | Introduction to RDF Connect Pipelines   | 0:30   |
| *Break*                                       | ---  | --- |
| **Morning 2: Processors** (_1:20_)              | RDF Connect Processors  | 0:40   |
|                                               | TBD  | 0:40   |
| *Lunch Break*                                 | ---  | --- |
| **Afternoon 1: Apps** (_1:20_)                | RDF Connect Pipelines | 0:40   |
|                                               | TBD | 0:40   |
| *Break*                                       | ---  | --- |
| **Afternoon 1: Hackathon** (_1:20_)           | Hackathon | 1:20   |

<figcaption markdown="block">
Planning of the tutorial
</figcaption>
</figure>


