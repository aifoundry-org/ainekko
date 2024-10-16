# Iterative AI Design Principles

## Background
The idea behind this document is to establish a clearly articulated set of design principles for AI analogous to the [Twelve-Factor App](https://12factor.net/) for cloud-native software, or the [Twelve Principles of Agile Software](https://agilemanifesto.org/principles.html) from the [Manifesto for Agile Software Development](https://agilemanifesto.org/) for modern software development processes. 

(Although there is no single canonical DevOps manifesto, there are a set of widely known core principles such as "Configuration as Code." It is possible that as we articulate these principles we will decide that a single document is not needed, but rather that there is an emerging pattern language that we can socialize with the community.)

This first draft is a placeholder, not a final document. It distills ideas from conversations with Tanya and Roman, Avi's "Mission" email, and Anatoliy's PRD.

## Naming
We need a name for this document that in some way telegraphs the benefit of the approach or the intention behind it.

My original name was "modern AI" but modern is the wrong word for something that is so nascent. 

Roman and Tanya suggested "composable," and that's a better placeholder name.

In this draft I'm using "iterative" but I'm not sure that's right either.

I suspect we need a different word to describe this. I just don't know what it is yet. Suggestions & edits welcome.

## Basic assumptions
While the field of AI is ripe with great products, the devil is always in the details AKA End User License Agreements (fun fact: some of the EULAs are event [incompatible with the definition of Open Source](https://www.apache.org/legal/generative-tooling.html)). Just like Open Source licenses, EULAs are a form of a lincense agreement that exists to protect the balance of rights between owners/authors of the AI system and its users. Our core belief (and the source of a lot of the following principles) is that whatever the agreement, the [Four Freedoms of Open Source Software](https://www.gnu.org/philosophy/free-sw.html.en#clarifying) must be protected and fostered. More specifically:
* The freedom to use AI system as you wish
* The freedom to study all the source artifacts (not just source code!) and make changes
* The freedom to publish (including publishing modifications to existing systems)
* The freedom to collaborate with others and build on top of each other's work

## Principles
The intent behind these principles is to create AI systems that can be iteratively developed and engender trust. To that end:
* Optimize for iterative change, including removal. (An implication of this principle is working in layers.)
* Everything is traceable. We can track the provenance of everything: models, data, fine tuning, everything.
* Every artifact is versioned. We know what changed, and can roll forward and roll back.
* All updates and interactions are logged. We can audit all model updates as well as prompts and the responses.
* Validation is a top-level concern. Before a model is updated, there is a clear criteria by which a given update can be judged to be "better" or "worse" for the particular use case.
