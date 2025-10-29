## Description

{:#description}

This tutorial introduces [_RDF-Connect (RDFC)_](https://github.com/rdf-connect/), a novel, language-agnostic framework
for constructing streaming data processing pipelines for RDF and non-RDF data. By leveraging RDF and PROV-O, RDFC
enables seamless integration of data processors in multiple programming languages. The tutorial focuses on pipeline
construction and processor development, equipping participants to build their own streaming workflows.

Participants will gain hands-on experience with RDFC, learning how to build pipelines by chaining modular components (
a.k.a. _processors_) that perform specific operations on (RDF) data streams. The tutorial focuses on implementing custom
processors and integrating them into functioning pipelines. Instead of solving a specific data processing problem, it
demonstrates structuring and managing adaptable (RDF) data workflows across domains and use cases.

To make the learning experience tangible, the tutorial includes a practical project based on a common use case for
ISWC's audience:
creating a _live_ and multilingual RDF knowledge graph. In this case, we will be using real data from the Japan Meteorological Agency. This example illustrates how different processors can be combined -- such as a REST API client in JavaScript, a Python-based ML model for language translation, a Java-based RML engine for RDF generation, a SHACL validator, and a triple store (SPARQL) update processor.

The expected outcome will be a functional pipeline created by the participants that integrates both existing and custom
components within the RDFC framework. The pipeline will continuously extract and transform weather forecast data
from the Japan Meteorological Agency’s API to RDF. It will then validate the data against a predefined shape using a
SHACL validator. Then, the custom processor, implemented by the participant, will perform language-aware
transformations based on a dedicated machine learning model. This processor will translate literal objects tagged as Japanese (
`@ja`) into English, generating new triples tagged as English (`@en`). The resulting RDF data will be written into a
triple store using a SPARQL-based processor.

By the end of the tutorial, participants will be able to:

- Design language-independent, modular data processing pipelines.
- Create custom processors for diverse data processing tasks within RDF-Connect.
- Leverage RDF and PROV-O to document and trace pipeline structure and execution.

This tutorial is designed to empower researchers, developers, and data practitioners with the skills to build scalable,
maintainable, and explainable streaming pipelines using RDF-based technologies.

## Motivation

{:#motivation}

As the Semantic Web community embraces increasingly diverse data sources and application domains, there is a growing
need for flexible, interoperable tooling bridging technology, language, and paradigm gaps.
RDFC directly addresses this need by providing a language-agnostic framework for building modular, reusable and
traceable
streaming data pipelines.

Semantic Web workflows often use custom tooling in specific languages, leading to brittle, monolithic systems difficult
to maintain, extend, and reuse. RDFC addresses these challenges by defining
a [specification](https://rdf-connect.github.io/specification/) that decouples processing logic from implementation
language and describes pipeline configurations using SHACL and an extension of PROV-O. This approach simplifies
pipeline component combination, reasoning, and sharing across teams and communities.

Moreover, the importance of provenance is more pressing than ever, especially in the current context of AI-generated
content and automated decision-making. RDFC simplifies the publication of machine-readable documentation in alignment
with the FAIR principles, of data transformations, enhancing transparency, reproducibility, and trust.

This tutorial aims to fill a critical gap in current Semantic Web tooling by introducing a practical, extensible way to
build explainable and modular streaming data pipelines. It is particularly valuable for early-career researchers,
practitioners building real-world applications, and anyone seeking to build more interoperable and maintainable
data-centric systems.

## Format and Schedule

{:#format}

This tutorial is designed as a **full-day session** as outlined in [](#planning). It includes presentations of the
conceptual foundations of the RDFC framework and hands-on implementation.

<figure id="planning" markdown="1" class="table">

|                                      | Topic                                                 | Start time |
|--------------------------------------|-------------------------------------------------------|------------|
| **Morning 1: Introduction** (_1:30_) | What will happen in this tutorial? 🤔                 | 9:00       |
|                                      | Let's make our hands dirty already! 🛠️                | 9:10       |
|                                      | The what and why of RDF-Connect 🎯                    | 10:00      |
| *Break*                              | ---                                                   | ---        |
| **Morning 2: Architecture** (_1:30_) | RDF-Connect concepts and architecture ⚙️              | 11:00      |
|                                      | Hands-on: Assembling a pipeline 🔗                    | 11:30      |
|--------------------------------------|-------------------------------------------------------|------------|
| *Lunch Break*                        | ---                                                   | ---        |
| **Afternoon 1: Roadmap** (_1:30_)    | What is next for RDF-Connect? 🛫                      | 13:30      |
|                                      | Hands-on: Implementing a custom processor 🏗️          | 14:00      |
| *Break*                              | ---                                                   | ---        |
| **Afternoon 1: Hackathon** (_1:30_)  | Hackathon 🧑‍💻                                          | 15:30      |

<figcaption markdown="block">
Planning of the tutorial
</figcaption>
</figure>


The program is structured into four sessions, two in the morning and two in the afternoon, progressively building a
conceptual overview while keeping participants engaged with hands-on tasks.
The day concludes with a collaborative hackathon where participants could apply what they have learned to explore extensions
or develop new applications.

The **first session** starts by presenting the tutorial's structure, immediately followed by a first hands-on task on
assembling a hello world pipeline. Later, a target example will be introduced, together with RDFC's high level overview and motivation.

The **second session** gives a deep dive into RDFC's design and architecture. Participants will then follow a step-by-step guide into setting up and running the target example pipeline, progresively increasing its complexity.learn to implement a processor in a
language of choice and configure it for pipeline integration.

The **third session** will cover the outlook and roadmap of RDFC and will teach participants how to develope their own custom processors. They will implement a processor that transforms a stream of RDF triples based on a configured language translation, leveraging a lightweight ML model to perform the translations locally. Once implemented, the custom processor will be incorporated int the pipeline built in the previous session.

The **fourth session** is a hackathon, where all participants work together to either extend the pipeline created in the
previous session with new data sources, or build a new pipeline using existing processors to achieve a different goal.
