## Description
{:#description}

RDF Connect (RDFC) is a revolutionary streaming data pipeline framework that breaks language barriers. Our tutorial introduces participants to a unique approach where processors can be implemented in multiple programming languages, seamlessly working together within a single pipeline.

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

The first session starts an introduction to RDF Connect, including the novel aspects of language agnostics processors. 
This section also includes an overview of the remained of the day, with a detailed description of the eventual pipeline that is built, including the new processor.

The seconds session includes the actual building of the processor. 
This allows participants to create the processor configuration and implementing a client for the weather endpoint.

The third session, allows participants to create a pipeline with their shiny processor and build a ML pipeline consuming this weather information in their favorite model.

We also have a fourth session.


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


