**Presenters:** Sagar Malhotra

**Email:** sagar.malhotra@tuwien.ac.at

**Proposed Duration:** Half-Day Tutorial

# Introduction

Relational data is characterized by the rich structure it encodes in the
dependencies between the individual entities of a given domain.
Statistical Relational AI (StarAI) combines first-order logic and
probability to learn and reason over relational domains by creating
parametric probability distributions over relational structures
[@SRL_LISA; @SRL_LUC]. StarAI models can succinctly represent the
complex dependencies in relational data and admit learning and inference
under uncertainty. Such expressivity allows for StarAI models to be used
in various applications that simultaneously require knowledge
representation, learning, reasoning and uncertainty quantification.
These models have been extensively used in domains like social network
analysis [@Problog], synthesizing biological networks [@Brouard2013-iw]
and for various problems on knowledge graphs
[@bellomarini2022swift; @Nickel2015ARO]. Furthermore, many widely used
Neuro-Symbolic approaches for integrating neural networks with symbolic
methods have been obtained as neural extensions of StarAI models
[@belle2023statistical; @DeepProblog; @jaeger; @marra2020neural] . A key
feature of StarAI models is the inherent interpretability and
explainability. These features have lead to significant interest in
applying StarAI models to safety critical areas like Healthcare
[@medicine; @natarajan2017markov] and for analyzing complex social
[@social; @zhang2014identifying] and biological systems
[@riedel2009markov; @sakhanenko2010markov].

The need for using StarAI models at scale is consistently rising with
the ever-increasing quantities of relational data. However, StarAI
models are significantly limited when it comes to the **tractability**
of learning and inference. This limitation emerges from the
intractability of Weighted First Order Model Counting (WFOMC)
[@Symmetric_Weighted], as both learning and inference in many StarAI
models can be reduced to instances of WFOMC. Furthermore, fundamental
properties expected of sound statistical models, like **consistency** of
parameter estimation, do not hold for StarAI models.

In this tutorial, we will focus on both tractability and consistency of
StarAI models from a foundational perspective. The tutorial will be
divided into two focus-topic. First focus-topic will be on tractable
WFOMC, where we will discuss the recent developments in the fragments of
first order logic that admit tractable WFOMC. In the second focus-topic,
we will discuss consistency of parameter estimation and generalization
behavior of StarAI models across different domain sizes. The learning
goal of the tutorial would be to convey state-of-the-art knowledge of
foundations of StarAI models, the existing open-problems, and to
motivate further applications of recently introduced theoretical
results.

# Target Audience, Prerequisites and Learning Goals

Recent years have seen increasing interest in Relational AI within the
KR community. This interest is reflected in consistent StarAI related
events in previous editions of KR, including David Poole's 2020 keynote
speech on StarAI, and the tutorial of Braun, Gehrke and Wilhelm at KR
2023. In this tutorial, we will bring to attention some foundational
problems in StarAI. Hence, our tutorial will be of interest to the
existing StarAI community at KR. Furthermore, our tutorial is also
interesting to the community of complexity analysis of reasoning. As it
will contain a thorough introduction to key ideas behind tractable
WFOMC. We believe that this tutorial can be attended by anyone with
basic knowledge of probability and first order logic.

The attendees will learn about the relation between problems like: model
counting and probabilistic inference; the complexity of model counting
problems; and about fragments of first order logic that admit tractable
WFOMC. The tutorial will guide the audience through some of the key
combinatorial ideas behind tractable WFOMC. The tutorial will also
discuss the current state-of-the-art first-order model counters, their
applications and their inefficiencies. The audience will be made aware
of both theoretical and practical open-problems, whose resolution would
lead to efficient probabilistic inference and learning in StarAI models.

The attendees will also be introduced to the problem of consistency of
inference, and the recently developed theories of StarAI models that
admit consistent parameter estimation. Such models, also known as
*projective models*, open up a vast array of new avenues in StarAI, and
the tutorial will provide the audience with the most recent
developments. The audience will gain deep understanding of present
theoretical models of projectivity and their recent applications.
Finally, we will also discuss some recent results on domain-size
generalization of non-projective models, and discuss how simple
techniques like parameter re-scaling and regularization lead to provably
better generalization across domain sizes.

# Tutorial Outline

The tutorial will be divided into three parts:

### Introduction

\[30 Minutes\] We will first discuss some background on relational data
and probability distributions on relational structures. We will
formalize a general notion of probabilistic inference on relational
data, and show how it maps to WFOMC for StarAI models like Markov Logic
Networks and Problog. We will provide some initial examples, where
tractability and inconsistency of inference can be major hurdles in real
life applications.

### Tractability

\[60 Minutes\] This session will focus on conveying the key recent
results in the field of WFOMC. We will first introduce the notion of
types and tables in first order logic. We will then provide a thorough
introduction to WFOMC in the universally quantified fragment of first
order logic with two variables, providing a closed form formula for
WFOMC of any universally quantified two-variable formula
[@Symmetric_Weighted]. We will then extend this result to admit
existential quantifiers using the principle of inclusion-exclusion
[@broeck2013; @MalhotraS22]. Finally, we will extend these results to
admit cardinality constraints and counting quantifiers
[@kuzelka2020weighted]. The tutorial will convey key algorithmic and
combinatorial ideas [@MalhotraS22] that will bring the audience a deep
understanding of the state-of-the-art WFOMC. We will introduce key open
problems in this area, ranging from scalability of existing model
counters [@pmlr-v161-bremen21a] to fine-grain analysis of known
(potentially sub-optimal) upper-bounds on complexity of WFOMC. Finally,
we will give a brief overview of recent results that allow for efficient
model counting in first order logic fragments, with graph-theoretic
constraints [@LI_Tree; @Malhotra2023LiftedIB]. Such constraints, such as
axiomatising a relation to represent a tree, forest, a connected graph
etc., significantly extend the tractable fragment of WFOMC.

### Consistency

\[60 Minutes\] We will begin by introducing recent results
[@Projectivity_Rinaldo] that have shown that a large variety of widely
used probabilistic models, encompassing almost all of existing StarAI
models [@Projectivity_first], do not admit basic *consistency*
requirements expected of sound statistical models. The lack of such
consistency conditions means that StarAI models do not admit consistency
of parameter estimation, i.e., as you see more and more data, it is not
true that your parameters converge to the true value of the model
parameters. Such inherent inconsistencies in StarAI models make them
hard to be used across varying domain sizes [@DA_MLN]. We will discuss
recent theoretical developments in identifying fragments of StarAI
models, that admit consistency of parameter estimation
[@ECML_PROJ; @Felix_Weit]. These fragments also admit tractable
inference in the strongest theoretical sense, as inference complexity is
independent of the domain size. We will discuss the recently introduced
rich theoretical framework for projective models [@ijcai2020p591], and
the recent developments in their practical implementation and
applications [@jaeger2023a]. We will especially focus on the vast array
of potential applications of these models in problems like reasoning
over large scale data and random relational structure generation
[@jaeger2023a]. Finally, we will look into recent developments in
understanding generalization properties of StarAI models that do not
admit consistent parameter estimation [@DA_MLN; @chen2024understanding],
and how simple regularization and re-scaling approaches can lead to
provably improved domain-size generalization in practice.

We will close the session with a discussion on open problems and
potential new applications in this domain.

# Presenter Bio

Sagar Malhotra is a PostDoc at TU Wien, hosted by Prof. Thomas Gärtner.
He obtained his PhD in 2023 from the university of Trento on under the
supervision of Luciano Serafini. During his PhD he worked on novel
fragments of first order logic that admit tractable WFOMC
[@MalhotraS22; @Malhotra2023LiftedIB]. He also worked on consistency of
inference of Markov Logic Networks [@ECML_PROJ]. Recently, he has been
interested in quantifying domain-size generalization of StarAI models
which do not admit consistent parameter estimation
[@chen2024understanding].
