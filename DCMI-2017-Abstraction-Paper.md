---
Title: Sticky and Leaky Abstractions for Data on the Web
Date: 05.14.2017
---

##Abstract
The W3C's Data on the Web working groups has recently produced two vocabularies for expressing information about the quality and usage of data on the web.
These vocabularies draw upon many namespaces, including dcterms, in order to build

This inheritence is a standard process of

However, there exists...

In this paper, we point out two forms of abstraction - leaky and sticky - that impact the use of these

The Data Usage Vocabulary is an example of leaky abstraction - it exposes (leaks) details and limitations of the underlying implementation that should ideally be hidden away. The Data Quality Vocabulary (DQV) is an example of a sticky abstraction - because quality is a relative concept it is difficult to express information about one context versus another (that is, the contextual knowledge sticks to a domain rather than transfers cleanly)


## Introduction

The logics of traditional grammar, as (X) points out, distinguish between nouns that are abstract (whiteness) and those that are concrete (white).

Abstraction is critical to knowledge representation generally, and the development of metadata, including particular instantiations like Dublin Core, in particular.

Yet, as we go up and down the ladder of abstraction there are many opportunities to mistakenly appeal to abstraction when concrete particulars are needed. That is, in moving away from

##Particular and Abstractions

The ladder of abstraction can be climbed for a number of reasons-

Moving away from a concrete particular, such as a

##The Ladder of Abstractction

Up  - is more Abstract
Down - is less

##Chutes and Ladders

Sticky vs Leaky knowledge was a distinction drawn by Brown and Duguid in 1987 - Leaky knowledge is that which spills over into


Type One Error: Sticky Abstraction



Type Two Error: Leaky Abstraction



Explicit accounts of the difference between concrete and abstract terms have riddled epistemology for decades -


Concrete:
Abstract:


"classes, propositions, concepts, the letter ‘A’, and Dante’s Inferno" are abstractions, while " stars, protons, electromagnetic fields, the chalk tokens of the letter ‘A’ written on a certain blackboard, and James Joyce’s copy of Dante’s Inferno" are examples of the concrete.

This matters when we deal with abstractions because it would appear that such terminology would  

Universal:
Particular:


In formal knowledge representation systems, this tradeoff is often described as the "expressiveness of a representational language and its computational tractability (Lavesque & Brachman, 1987). In short, the more expressive an AI language the more computationally costly it becomes. The same is true of any formalized standard of knowledge representatiton -


Second mover advantage -

For `dcat: distribution` this "Represents a specific available form of a dataset. Each dataset might be available in different forms, these forms might represent different formats of the dataset or different endpoints. Examples of distributions include a downloadable CSV file, an API or an RSS feed"


The logics of traditional grammar. as (X) points out, distinguish between nouns that are abstract (whiteness) and those that are concrete (white).

## Works Cited

Levesque, H. J., & Brachman, R. J. (1987). Expressiveness and tractability in knowledge representation and reasoning. Computational intelligence, 3(1), 78-93.

Teece, D. J. (1986) Profiting from Technological Innovation: Implications for Integration, Collaboration, Licensing and Public Policy. Research Policy, 15 (6), pp. 285-305.
