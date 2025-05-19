## Description

{:#description}

This tutorial introduces _RDF-Connect (RDF-C)_, a novel, language-agnostic framework for constructing streaming data processing pipelines both for RDF and non-RDF data. By leveraging RDF and the PROV-O ontology, RDF-C enables the creation of pipelines that seamlessly integrate data processors implemented in multiple programming languages. The tutorial is centered around the core concepts of pipeline construction and processor development, giving participants the skills and understanding needed to build their own streaming workflows.

Participants will gain hands-on experience with RDF-C, learning how to build pipelines by chaining together modular components -- called processors -- that each perform a specific operation on a (RDF) data stream. The tutorial focus on how to implement custom processors and integrate them into a functioning pipeline. Rather than emphasizing the solution to a specific data processing problem, the tutorial demonstrates how to structure and manage (RDF) data workflows that are adaptable across domains and use cases.

To make the learning experience tangible, the tutorial includes a practical project based on a common use case for ISWC's audience:
creating a _live_ and multilingual RDF knowledge graph using data from the Meteorological Agency of Japan. This example illustrates how different processors can be combined -- such as a REST API client in JavaScript, a Python-based ML model for language translation, a Java-based RML engine and SHACL validator, and a triple store (SPARQL) update processor.

The expected outcome will be a functional pipeline created by the participants that integrates both existing and custom components within the RDF-Connect framework. The pipeline will continuosly extract and transform to RDF, weather forecast data from an API of the Japan Meteorological Agency. This data will be validated against a predefined schema using a SHACL validator. The data will be passed then to a custom processor, implemented by the participant, that performs language-aware transformations based on a machine learning model. Specifically, this processor will translate all literal objects tagged as Japanese (`@ja`) into English, generating new triples tagged as English (`@en`). The resulting RDF data will be written into a triple store using a SPARQL-based processor. 

By the end of the tutorial, participants will be able to:

- Design language-independent, modular data processing pipelines.
- Create custom processors for diverse data processing tasks within RDF-Connect.
- Leverage RDF and PROV-O to document and trace pipeline structure and execution.

This tutorial is designed to empower researchers, developers, and data practitioners with the skills to build scalable, maintainable, and explainable streaming pipelines using RDF-based technologies.

## Motivation

{:#motivation}

As the Semantic Web community continues to embrace increasingly diverse data sources and application domains, there is a growing need for flexible, interoperable tooling that can bridge gaps between technologies, languages, and paradigms. _RDF-Connect (RDF-C)_ directly addresses this need by providing a language-agnostic framework for building streaming data pipelines that are modular, reusable and traceable.

Many Semantic Web workflows involve custom tooling built in specific languages, often leading to brittle, monolithic systems that are difficult to maintain, extend and reuse. RDF-C turns these challenges into opportunities by decoupling processing logic from implementation language and describing pipeline configurations using SHACL and an extension of the PROV-O ontology. This approach makes pipeline components easier to combine, reason about, and share across teams and communities.

Moreover, the importance of provenance is growing rapidly, especially in the age of AI-generated content and automated
decision-making. RDF-C makes it easy to publish machine-readable documentation, in line with the FAIR principles, of the steps and transformations applied to data, facilitating transparency, reproducibility, and trust.

This tutorial aims to fill a critical gap in current Semantic Web tooling by introducing a practical, extensible way to build
streaming data pipelines that are explainable and modular. It is particularly valuable for early-career researchers, practitioners building real-world applications, and anyone seeking to build more interoperable and maintainable data-centric systems.

## Format and Schedule

{:#format}

This tutorial is designed to be a **full-day session** as outlined in [](#planning), as it introduces a new framework
and guides participants through both conceptual foundations and hands-on implementation work.
A half-day format would not suffice to cover both the design principles of _RDFC_ and provide meaningful experience
building pipelines and processors.

The program is structured into four sessions, two in the morning and two in the afternoon, progressively building from a
conceptual overview to hands-on development.
The day concludes with a collaborative hackathon where participants apply what they’ve learned to explore extensions or
develop new applications.

The **first session** introduces RDF-Connect at a high level, highlighting its language-agnostic processor architecture.
This session includes an overview of the tutorial's content, as well as a detailed description of the pipeline
participants will build throughout the day.

The **second session** focuses on processor development. Participants will learn how to implement a processor in a
language of their choice, and configure it for pipeline integration.
They will implement a processor that transforms a set of triples.
This processor will have to identify triples with a literal as the object and a language tag `@ja`.
It will then translate these triples to English and add them as a new triple with the language tag `@en`.
We can implement this using a lightweight ML model that translates input from Japanese to English locally.
Alternatively, we could implement a processor that sends the input to a remote translation service.

The **third session** covers pipeline assembly using both existing and the custom-built processor from the previous
session.
Participants will construct a working streaming pipeline that pulls data, applies transformations, performs validation,
and publishes results to a triple store.

The **fourth session** is a hackathon, where all participants work together to either extend the pipeline created in the
previous session with new data sources, or build a new pipeline using existing processors to achieve a different goal.


<figure id="planning" markdown="1" class="table">

|                                      | Topic                                            | Duration |
|--------------------------------------|--------------------------------------------------|----------|
| **Morning 1: Introduction** (_1:20_) | Introduction                                     | 0:10     |
|                                      | Introduction to RDF-Connect Processors           | 0:40     |
|                                      | Introduction to RDF-Connect Pipelines            | 0:30     |
| *Break*                              | ---                                              | ---      |
| **Morning 2: Processors** (_1:20_)   | Recap: How to implement a RDFC Processor?        | 0:10     |
|                                      | Hands-on: Implementing a processor               | 1:10     |
| *Lunch Break*                        | ---                                              | ---      |
| **Afternoon 1: Apps** (_1:20_)       | Recap: How to build and execute a RDFC Pipeline? | 0:10     |
|                                      | Hands-on: Assembling a pipeline                  | 1:10     |
| *Break*                              | ---                                              | ---      |
| **Afternoon 1: Hackathon** (_1:20_)  | Hackathon                                        | 1:20     |

<figcaption markdown="block">
Planning of the tutorial
</figcaption>
</figure>


