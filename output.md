::: maketitle
[]{#likesection.1}[]{#x1-2r1}

## Fundamental Problems in Statistical Relational AI {#fundamental-problems-in-statistical-relational-ai .titleHead}

::: author
Sagar Malhotra
:::

::: institute
[TU Wien, Austria ]{.ptmr8t-x-x-90}
:::

[]{#Q1-1-1} []{#Q1-1-2}
:::

[Presenters: ]{.ptmb8t-}Sagar Malhotra

[Email: ]{.ptmb8t-}sagar.malhotra@tuwien.ac.at

[Proposed Duration: ]{.ptmb8t-}Half-Day Tutorial

### [1 ]{.titlemark} []{#x1-10001}Introduction {#introduction .sectionHead}

Relational data is characterized by the rich structure it encodes in the
dependencies between the individual entities of a given domain.
Statistical Relational AI (StarAI) combines first-order logic and
probability to learn and reason over relational domains by creating
parametric probability distributions over relational structures
[\[[1](#XSRL_LISA), [2](#XSRL_LUC)\]]{.cite}. StarAI models can
succinctly represent the complex dependencies in relational data and
admit learning and inference under uncertainty. Such expressivity allows
for StarAI models to be used in various applications that simultaneously
require knowledge representation, learning, reasoning and uncertainty
quantification. These models have been extensively used in domains like
social network analysis [\[[3](#XProblog)\]]{.cite}, synthesizing
biological networks [\[[4](#XBrouard2013-iw)\]]{.cite} and for various
problems on knowledge graphs
[\[[5](#Xbellomarini2022swift), [6](#XNickel2015ARO)\]]{.cite}.
Furthermore, many widely used Neuro-Symbolic approaches for integrating
neural networks with symbolic methods have been obtained as neural
extensions of StarAI models
[\[[7](#Xbelle2023statistical), [8](#XDeepProblog), [9](#Xjaeger), [10](#Xmarra2020neural)\]]{.cite}
. A key feature of StarAI models is the inherent interpretability and
explainability. These features have lead to significant interest in
applying StarAI models to safety critical areas like Healthcare
[\[[11](#Xmedicine), [12](#Xnatarajan2017markov)\]]{.cite} and for
analyzing complex social
[\[[13](#Xsocial), [14](#Xzhang2014identifying)\]]{.cite} and biological
systems
[\[[15](#Xriedel2009markov), [16](#Xsakhanenko2010markov)\]]{.cite}.

The need for using StarAI models at scale is consistently rising with
the ever-increasing quantities of relational data. However, StarAI
models are significantly limited when it comes to the [tractability
]{.ptmb8t-}of learning and inference. This limitation emerges from the
intractability of Weighted First Order Model Counting (WFOMC)
[\[[17](#XSymmetric_Weighted)\]]{.cite}, as both learning and inference
in many StarAI models can be reduced to instances of WFOMC. Furthermore,
fundamental properties expected of sound statistical models, like
[consistency ]{.ptmb8t-}of parameter estimation, do not hold for StarAI
models.

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

### [2 ]{.titlemark} []{#x1-20002}Target Audience, Prerequisites and Learning Goals {#target-audience-prerequisites-and-learning-goals .sectionHead}

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
[projective models]{.ptmri8t-}, open up a vast array of new avenues in
StarAI, and the tutorial will provide the audience with the most recent
developments. The audience will gain deep understanding of present
theoretical models of projectivity and their recent applications.
Finally, we will also discuss some recent results on domain-size
generalization of non-projective models, and discuss how simple
techniques like parameter re-scaling and regularization lead to provably
better generalization across domain sizes.

### [3 ]{.titlemark} []{#x1-30003}Tutorial Outline {#tutorial-outline .sectionHead}

The tutorial will be divided into three parts:

##### []{#x1-40003}Introduction {#introduction-1 .subsubsectionHead}

\[30 Minutes\] We will first discuss some background on relational data
and probability distributions on relational structures. We will
formalize a general notion of probabilistic inference on relational
data, and show how it maps to WFOMC for StarAI models like Markov Logic
Networks and Problog. We will provide some initial examples, where
tractability and inconsistency of inference can be major hurdles in real
life applications.

##### []{#x1-50003}Tractability {#tractability .subsubsectionHead}

\[60 Minutes\] This session will focus on conveying the key recent
results in the field of WFOMC. We will first introduce the notion of
types and tables in first order logic. We will then provide a thorough
introduction to WFOMC in the universally quantified fragment of first
order logic with two variables, providing a closed form formula for
WFOMC of any universally quantified two-variable formula
[\[[17](#XSymmetric_Weighted)\]]{.cite}. We will then extend this result
to admit existential quantifiers using the principle of
inclusion-exclusion
[\[[18](#Xbroeck2013), [19](#XMalhotraS22)\]]{.cite}. Finally, we will
extend these results to admit cardinality constraints and counting
quantifiers [\[[20](#Xkuzelka2020weighted)\]]{.cite}. The tutorial will
convey key algorithmic and combinatorial ideas
[\[[19](#XMalhotraS22)\]]{.cite} that will bring the audience a deep
understanding of the state-of-the-art WFOMC. We will introduce key open
problems in this area, ranging from scalability of existing model
counters [\[[21](#Xpmlr-v161-bremen21a)\]]{.cite} to fine-grain analysis
of known (potentially sub-optimal) upper-bounds on complexity of WFOMC.
Finally, we will give a brief overview of recent results that allow for
efficient model counting in first order logic fragments, with
graph-theoretic constraints
[\[[22](#XLI_Tree), [23](#XMalhotra2023LiftedIB)\]]{.cite}. Such
constraints, such as axiomatising a relation to represent a tree,
forest, a connected graph etc., significantly extend the tractable
fragment of WFOMC.

##### []{#x1-60003}Consistency {#consistency .subsubsectionHead}

\[60 Minutes\] We will begin by introducing recent results
[\[[24](#XProjectivity_Rinaldo)\]]{.cite} that have shown that a large
variety of widely used probabilistic models, encompassing almost all of
existing StarAI models [\[[25](#XProjectivity_first)\]]{.cite}, do not
admit basic [consistency ]{.ptmri8t-}requirements expected of sound
statistical models. The lack of such consistency conditions means that
StarAI models do not admit consistency of parameter estimation, i.e., as
you see more and more data, it is not true that your parameters converge
to the true value of the model parameters. Such inherent inconsistencies
in StarAI models make them hard to be used across varying domain sizes
[\[[26](#XDA_MLN)\]]{.cite}. We will discuss recent theoretical
developments in identifying fragments of StarAI models, that admit
consistency of parameter estimation
[\[[27](#XECML_PROJ), [28](#XFelix_Weit)\]]{.cite}. These fragments also
admit tractable inference in the strongest theoretical sense, as
inference complexity is independent of the domain size. We will discuss
the recently introduced rich theoretical framework for projective models
[\[[29](#Xijcai2020p591)\]]{.cite}, and the recent developments in their
practical implementation and applications
[\[[30](#Xjaeger2023a)\]]{.cite}. We will especially focus on the vast
array of potential applications of these models in problems like
reasoning over large scale data and random relational structure
generation [\[[30](#Xjaeger2023a)\]]{.cite}. Finally, we will look into
recent developments in understanding generalization properties of StarAI
models that do not admit consistent parameter estimation
[\[[26](#XDA_MLN), [31](#Xchen2024understanding)\]]{.cite}, and how
simple regularization and re-scaling approaches can lead to provably
improved domain-size generalization in practice.

We will close the session with a discussion on open problems and
potential new applications in this domain.

### [4 ]{.titlemark} []{#x1-70004}Presenter Bio {#presenter-bio .sectionHead}

Sagar Malhotra is a PostDoc at TU Wien, hosted by Prof. Thomas Gärtner.
He obtained his PhD in 2023 from the university of Trento on
"Tractability and Consistency of Probabilistic Inference in Relational
Domains" under the supervision of Luciano Serafini. During his PhD he
worked on novel fragments of first order logic that admit tractable
WFOMC [\[[19](#XMalhotraS22), [23](#XMalhotra2023LiftedIB)\]]{.cite}. He
also worked on consistency of inference of Markov Logic Networks
[\[[27](#XECML_PROJ)\]]{.cite}. Recently, he has been interested in
quantifying domain-size generalization of StarAI models which do not
admit consistent parameter estimation
[\[[31](#Xchen2024understanding)\]]{.cite}.

### []{#x1-80004}References {#references .likesectionHead}

::: thebibliography
[ [1.]{.ptmr8t-x-x-90}
[[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}]{.bibsp}]{.biblabel}[]{#XSRL_LISA}[Lise
Getoor and Ben Taskar. ]{.ptmr8t-x-x-90}[Introduction to Statistical
Relational Learning (Adaptive]{.ptmri8t-x-x-90} [Computation and Machine
Learning)]{.ptmri8t-x-x-90}[. The MIT Press, 2007.]{.ptmr8t-x-x-90}

[ [2.]{.ptmr8t-x-x-90}
[[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}]{.bibsp}]{.biblabel}[]{#XSRL_LUC}[Luc]{.ptmr8t-x-x-90}[ De
Raedt, Kristian Kersting, Sriraam Natarajan, and David Poole.
]{.ptmr8t-x-x-90}[Statistical]{.ptmri8t-x-x-90} [Relational Artificial
Intelligence: Logic, Probability, and Computation]{.ptmri8t-x-x-90}[.
Synthesis Lectures]{.ptmr8t-x-x-90} [on Artificial Intelligence and
Machine Learning. Morgan & Claypool Publishers, 2016.]{.ptmr8t-x-x-90}

[ [3.]{.ptmr8t-x-x-90}
[[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}]{.bibsp}]{.biblabel}[]{#XProblog}[Luc
De]{.ptmr8t-x-x-90}[ Raedt, Angelika Kimmig, and Hannu Toivonen.
Problog: A probabilistic]{.ptmr8t-x-x-90} [prolog and its application in
link discovery. In ]{.ptmr8t-x-x-90}[Proceedings of the 20th
International Joint]{.ptmri8t-x-x-90} [Conference on Artifical
Intelligence]{.ptmri8t-x-x-90}[, IJCAI'07, page 2468--2473, San
Francisco, CA, USA,]{.ptmr8t-x-x-90} [2007. Morgan Kaufmann Publishers
Inc.]{.ptmr8t-x-x-90}

[ [4.]{.ptmr8t-x-x-90}
[[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}]{.bibsp}]{.biblabel}[]{#XBrouard2013-iw}[C]{.ptmr8t-x-x-90}[éline
Brouard, Christel Vrain, Julie Dubois, David Castel, Marie-Anne Debily,
and]{.ptmr8t-x-x-90} [Florence d'Alch]{.ptmr8t-x-x-90}[é Buc. Learning a
markov logic network for supervised gene regulatory]{.ptmr8t-x-x-90}
[network inference. ]{.ptmr8t-x-x-90}[BMC
Bioinformatics]{.ptmri8t-x-x-90}[, 14:273, September
2013.]{.ptmr8t-x-x-90}

[ [5.]{.ptmr8t-x-x-90}
[[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}]{.bibsp}]{.biblabel}[]{#Xbellomarini2022swift}[Luigi
Bellomarini, Eleonora Laurenza, Emanuel Sallinger, and Evgeny
Sherkhonov.]{.ptmr8t-x-x-90} [Swift markov logic for probabilistic
reasoning on knowledge graphs, 2022.]{.ptmr8t-x-x-90}

[ [6.]{.ptmr8t-x-x-90}
[[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}]{.bibsp}]{.biblabel}[]{#XNickel2015ARO}[Maximilian
Nickel, Kevin]{.ptmr8t-x-x-90}[ P. Murphy, Volker Tresp, and Evgeniy
Gabrilovich. A review]{.ptmr8t-x-x-90} [of relational machine learning
for knowledge graphs. ]{.ptmr8t-x-x-90}[Proceedings of the
IEEE]{.ptmri8t-x-x-90}[, 104:11--33,]{.ptmr8t-x-x-90}
[2015.]{.ptmr8t-x-x-90}

[ [7.]{.ptmr8t-x-x-90}
[[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}]{.bibsp}]{.biblabel}[]{#Xbelle2023statistical}[Vaishak
Belle. Statistical relational learning and neuro-symbolic ai: what does
first-order]{.ptmr8t-x-x-90} [logic offer?, 2023.]{.ptmr8t-x-x-90}

[ [8.]{.ptmr8t-x-x-90}
[[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}]{.bibsp}]{.biblabel}[]{#XDeepProblog}[Robin
Manhaeve, Sebastijan Dumancic, Angelika Kimmig, Thomas Demeester,
and]{.ptmr8t-x-x-90} [Luc]{.ptmr8t-x-x-90}[ De Raedt. Deepproblog:
neural probabilistic logic programming. In ]{.ptmr8t-x-x-90}[Proceedings
of the]{.ptmri8t-x-x-90} [32nd International Conference on Neural
Information Processing Systems]{.ptmri8t-x-x-90}[, NIPS'18,
page]{.ptmr8t-x-x-90} [3753--3763, Red Hook, NY, USA, 2018. Curran
Associates Inc.]{.ptmr8t-x-x-90}

[ [9.]{.ptmr8t-x-x-90}
[[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}]{.bibsp}]{.biblabel}[]{#Xjaeger}[Manfred
Jaeger. Learning and Reasoning with Graph Data: Neural
and]{.ptmr8t-x-x-90} [Statistical-Relational Approaches. In Camille
Bourgaux, Ana Ozaki, and Rafael
Pe]{.ptmr8t-x-x-90}[ñaloza,]{.ptmr8t-x-x-90} [editors,
]{.ptmr8t-x-x-90}[International Research School in Artificial
Intelligence in Bergen (AIB 2022)]{.ptmri8t-x-x-90}[,]{.ptmr8t-x-x-90}
[volume]{.ptmr8t-x-x-90}[ 99 of ]{.ptmr8t-x-x-90}[Open Access Series in
Informatics (OASIcs)]{.ptmri8t-x-x-90}[, pages 5:1--5:42,
Dagstuhl,]{.ptmr8t-x-x-90} [Germany, 2022. Schloss Dagstuhl --
Leibniz-Zentrum f]{.ptmr8t-x-x-90}[ür Informatik.]{.ptmr8t-x-x-90}

[ [10.]{.ptmr8t-x-x-90}
[[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}]{.bibsp}]{.biblabel}[]{#Xmarra2020neural}[Giuseppe
Marra and Ond]{.ptmr8t-x-x-90}[řej Ku]{.ptmr8t-x-x-90}[želka. Neural
markov logic networks, 2020.]{.ptmr8t-x-x-90}

[ [11.]{.ptmr8t-x-x-90}
[[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}]{.bibsp}]{.biblabel}[]{#Xmedicine}[Sriraam
Natarajan, Kristian Kersting, Tushar Khot, and Jude Shavlik.
]{.ptmr8t-x-x-90}[Boosted Statistical]{.ptmri8t-x-x-90} [Relational
Learners: From Benchmarks to Data-Driven Medicine]{.ptmri8t-x-x-90}[.
Springer Publishing]{.ptmr8t-x-x-90} [Company, Incorporated,
2015.]{.ptmr8t-x-x-90}

[ [12.]{.ptmr8t-x-x-90}
[[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}]{.bibsp}]{.biblabel}[]{#Xnatarajan2017markov}[Sriraam
Natarajan, Vishal Bangera, Tushar Khot, Jose Picado, Anurag
Wazalwar,]{.ptmr8t-x-x-90} [Vitor]{.ptmr8t-x-x-90}[ Santos Costa, David
Page, and Michael Caldwell. Markov logic networks for
adverse]{.ptmr8t-x-x-90} [drug event extraction from text.
]{.ptmr8t-x-x-90}[Knowledge and information systems]{.ptmri8t-x-x-90}[,
51:435--457, 2017.]{.ptmr8t-x-x-90}

[ [13.]{.ptmr8t-x-x-90}
[[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}]{.bibsp}]{.biblabel}[]{#Xsocial}[Haiquan
Chen, Wei-Shinn Ku, Haixun Wang, Liang Tang, and Min-Te Sun. Scaling
up]{.ptmr8t-x-x-90} [markov logic probabilistic inference for social
graphs. ]{.ptmr8t-x-x-90}[IEEE Transactions on
Knowledge]{.ptmri8t-x-x-90} [and Data Engineering]{.ptmri8t-x-x-90}[,
29(2):433--445, 2017.]{.ptmr8t-x-x-90}

[ [14.]{.ptmr8t-x-x-90}
[[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}]{.bibsp}]{.biblabel}[]{#Xzhang2014identifying}[Weizhe
Zhang, Xiaoqiang Li, Hui He, Xing Wang, et]{.ptmr8t-x-x-90}[ al.
Identifying network public]{.ptmr8t-x-x-90} [opinion leaders based on
markov logic networks. ]{.ptmr8t-x-x-90}[The scientific world
journal]{.ptmri8t-x-x-90}[, 2014, 2014.]{.ptmr8t-x-x-90}

[ [15.]{.ptmr8t-x-x-90}
[[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}]{.bibsp}]{.biblabel}[]{#Xriedel2009markov}[Sebastian
Riedel, Hong-Woo Chun, Toshihisa Takagi, and Jun'ichi Tsujii. A
markov]{.ptmr8t-x-x-90} [logic approach to bio-molecular event
extraction. In ]{.ptmr8t-x-x-90}[Proceedings of the BioNLP
2009]{.ptmri8t-x-x-90} [Workshop Companion Volume for Shared
Task]{.ptmri8t-x-x-90}[, pages 41--49, 2009.]{.ptmr8t-x-x-90}

[ [16.]{.ptmr8t-x-x-90}
[[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}]{.bibsp}]{.biblabel}[]{#Xsakhanenko2010markov}[Nikita]{.ptmr8t-x-x-90}[ A
Sakhanenko and David]{.ptmr8t-x-x-90}[ J Galas. Markov logic networks in
the analysis of]{.ptmr8t-x-x-90} [genetic data.
]{.ptmr8t-x-x-90}[Journal of Computational Biology]{.ptmri8t-x-x-90}[,
17(11):1491--1508, 2010.]{.ptmr8t-x-x-90}

[ [17.]{.ptmr8t-x-x-90}
[[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}]{.bibsp}]{.biblabel}[]{#XSymmetric_Weighted}[Paul
Beame, Guy]{.ptmr8t-x-x-90}[ Van den Broeck, Eric Gribkoff, and Dan
Suciu. Symmetric weighted]{.ptmr8t-x-x-90} [first-order model counting.
In Tova Milo and Diego Calvanese, editors, ]{.ptmr8t-x-x-90}[Proceedings
of the]{.ptmri8t-x-x-90} [34th ACM Symposium on Principles of Database
Systems, PODS 2015, Melbourne, Victoria,]{.ptmri8t-x-x-90} [Australia,
May 31 - June 4, 2015]{.ptmri8t-x-x-90}[, pages 313--328. ACM,
2015.]{.ptmr8t-x-x-90}

[ [18.]{.ptmr8t-x-x-90}
[[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}]{.bibsp}]{.biblabel}[]{#Xbroeck2013}[Guy]{.ptmr8t-x-x-90}[ Van
den Broeck, Wannes Meert, and Adnan Darwiche. Skolemization
for]{.ptmr8t-x-x-90} [weighted first-order model counting. In Chitta
Baral, Giuseppe]{.ptmr8t-x-x-90}[ De Giacomo, and
Thomas]{.ptmr8t-x-x-90} [Eiter, editors, ]{.ptmr8t-x-x-90}[Principles of
Knowledge Representation and Reasoning: Proceedings of
the]{.ptmri8t-x-x-90} [Fourteenth International Conference, KR 2014,
Vienna, Austria, July 20-24, 2014]{.ptmri8t-x-x-90}[.
AAAI]{.ptmr8t-x-x-90} [Press, 2014.]{.ptmr8t-x-x-90}

[ [19.]{.ptmr8t-x-x-90}
[[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}]{.bibsp}]{.biblabel}[]{#XMalhotraS22}[Sagar
Malhotra and Luciano Serafini. Weighted model counting in FO2 with
cardinality]{.ptmr8t-x-x-90} [constraints and counting quantifiers: A
closed form formula. In ]{.ptmr8t-x-x-90}[Thirty-Sixth
AAAI]{.ptmri8t-x-x-90} [Conference on Artificial Intelligence, AAAI
2022, Thirty-Fourth Conference on Innovative]{.ptmri8t-x-x-90}
[Applications of Artificial Intelligence, IAAI 2022, The Twelveth
Symposium on Educational]{.ptmri8t-x-x-90} [Advances in Artificial
Intelligence, EAAI 2022 Virtual Event, February 22 - March 1,
2022]{.ptmri8t-x-x-90}[,]{.ptmr8t-x-x-90} [pages 5817--5824. AAAI Press,
2022.]{.ptmr8t-x-x-90}

[ [20.]{.ptmr8t-x-x-90}
[[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}]{.bibsp}]{.biblabel}[]{#Xkuzelka2020weighted}[Ondrej
Kuzelka. Weighted first-order model counting in the two-variable
fragment with]{.ptmr8t-x-x-90} [counting quantifiers.
]{.ptmr8t-x-x-90}[J. Artif. Intell. Res.]{.ptmri8t-x-x-90}[,
70:1281--1307, 2021.]{.ptmr8t-x-x-90}

[ [21.]{.ptmr8t-x-x-90}
[[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}]{.bibsp}]{.biblabel}[]{#Xpmlr-v161-bremen21a}[Timothy
van Bremen and Ond]{.ptmr8t-x-x-90}[řej Ku]{.ptmr8t-x-x-90}[želka.
Faster lifting for two-variable logic using]{.ptmr8t-x-x-90} [cell
graphs. In Cassio de]{.ptmr8t-x-x-90}[ Campos and
Marloes]{.ptmr8t-x-x-90}[ H. Maathuis, editors,
]{.ptmr8t-x-x-90}[Proceedings of]{.ptmri8t-x-x-90} [the Thirty-Seventh
Conference on Uncertainty in Artificial Intelligence]{.ptmri8t-x-x-90}[,
volume 161 of]{.ptmr8t-x-x-90} [Proceedings of Machine Learning
Research]{.ptmri8t-x-x-90}[, pages 1393--1402. PMLR, 27--30 Jul
2021.]{.ptmr8t-x-x-90}

[ [22.]{.ptmr8t-x-x-90}
[[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}]{.bibsp}]{.biblabel}[]{#XLI_Tree}[Timothy
van Bremen and Ond]{.ptmr8t-x-x-90}[řej Ku]{.ptmr8t-x-x-90}[želka.
Lifted Inference with Tree Axioms.]{.ptmr8t-x-x-90} [In
]{.ptmr8t-x-x-90}[Proceedings of the 18th International Conference on
Principles of Knowledge]{.ptmri8t-x-x-90} [Representation and
Reasoning]{.ptmri8t-x-x-90}[, pages 599--608, 11 2021.]{.ptmr8t-x-x-90}

[ [23.]{.ptmr8t-x-x-90}
[[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}]{.bibsp}]{.biblabel}[]{#XMalhotra2023LiftedIB}[Sagar
Malhotra, Davide Bizzaro, and Luciano Serafini. Lifted inference
beyond]{.ptmr8t-x-x-90} [first-order logic.
]{.ptmr8t-x-x-90}[ArXiv]{.ptmri8t-x-x-90}[, abs/2308.11738,
2023.]{.ptmr8t-x-x-90}

[ [24.]{.ptmr8t-x-x-90}
[[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}]{.bibsp}]{.biblabel}[]{#XProjectivity_Rinaldo}[Cosma]{.ptmr8t-x-x-90}[ Rohilla
Shalizi and Alessandro Rinaldo. Consistency under sampling
of]{.ptmr8t-x-x-90} [exponential random graph models.
]{.ptmr8t-x-x-90}[Annals of statistics]{.ptmri8t-x-x-90}[, 41
2:508--535, 2013.]{.ptmr8t-x-x-90}

[ [25.]{.ptmr8t-x-x-90}
[[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}]{.bibsp}]{.biblabel}[]{#XProjectivity_first}[Manfred
Jaeger and Oliver Schulte. Inference, learning, and population size:
Projectivity]{.ptmr8t-x-x-90} [for SRL models.
]{.ptmr8t-x-x-90}[CoRR]{.ptmri8t-x-x-90}[, abs/1807.00564,
2018.]{.ptmr8t-x-x-90}

[ [26.]{.ptmr8t-x-x-90}
[[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}]{.bibsp}]{.biblabel}[]{#XDA_MLN}[Happy
Mittal, Ayush Bhardwaj, Vibhav Gogate, and Parag Singla. Domain-size
aware]{.ptmr8t-x-x-90} [markov logic networks. In Kamalika Chaudhuri and
Masashi Sugiyama, editors, ]{.ptmr8t-x-x-90}[The 22nd]{.ptmri8t-x-x-90}
[International Conference on Artificial Intelligence and Statistics,
AISTATS 2019, 16-18 April]{.ptmri8t-x-x-90} [2019, Naha, Okinawa,
Japan]{.ptmri8t-x-x-90}[, volume]{.ptmr8t-x-x-90}[ 89 of
]{.ptmr8t-x-x-90}[Proceedings of Machine Learning
Research]{.ptmri8t-x-x-90}[,]{.ptmr8t-x-x-90} [pages 3216--3224. PMLR,
2019.]{.ptmr8t-x-x-90}

[ [27.]{.ptmr8t-x-x-90}
[[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}]{.bibsp}]{.biblabel}[]{#XECML_PROJ}[Sagar
Malhotra and Luciano Serafini. On projectivity
in]{.ptmr8t-x-x-90}[ markov logic networks. In]{.ptmr8t-x-x-90}
[Massih-Reza Amini, St]{.ptmr8t-x-x-90}[éphane Canu, Asja Fischer, Tias
Guns, Petra Kralj]{.ptmr8t-x-x-90}[ Novak, and]{.ptmr8t-x-x-90}
[Grigorios Tsoumakas, editors, ]{.ptmr8t-x-x-90}[Machine Learning and
Knowledge Discovery in Databases]{.ptmri8t-x-x-90}[,]{.ptmr8t-x-x-90}
[pages 223--238, Cham, 2023. Springer Nature
Switzerland.]{.ptmr8t-x-x-90}

[ [28.]{.ptmr8t-x-x-90}
[[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}]{.bibsp}]{.biblabel}[]{#XFelix_Weit}[Felix]{.ptmr8t-x-x-90}[ Q.
Weitk]{.ptmr8t-x-x-90}[ämper. An asymptotic analysis of probabilistic
logic programming, with]{.ptmr8t-x-x-90} [implications for expressing
projective families of distributions. ]{.ptmr8t-x-x-90}[Theory Pract.
Log. Program.]{.ptmri8t-x-x-90}[,]{.ptmr8t-x-x-90} [21(6):802--817,
2021.]{.ptmr8t-x-x-90}

[ [29.]{.ptmr8t-x-x-90}
[[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}]{.bibsp}]{.biblabel}[]{#Xijcai2020p591}[Manfred
Jaeger and Oliver Schulte. A complete characterization of projectivity
for]{.ptmr8t-x-x-90} [statistical relational models. In Christian
Bessiere, editor, ]{.ptmr8t-x-x-90}[Proceedings of the
Twenty-Ninth]{.ptmri8t-x-x-90} [International Joint Conference on
Artificial Intelligence, IJCAI-20]{.ptmri8t-x-x-90}[, pages
4283--4290.]{.ptmr8t-x-x-90} [International Joint Conferences on
Artificial Intelligence Organization, 7 2020. Main
track.]{.ptmr8t-x-x-90}

[ [30.]{.ptmr8t-x-x-90}
[[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}]{.bibsp}]{.biblabel}[]{#Xjaeger2023a}[Manfred
Jaeger, Antonio Longa, Steve Azzolin, Oliver Schulte, and Andrea
Passerini. A]{.ptmr8t-x-x-90} [simple latent variable model for graph
learning and inference. In ]{.ptmr8t-x-x-90}[The Second Learning
on]{.ptmri8t-x-x-90} [Graphs Conference]{.ptmri8t-x-x-90}[,
2023.]{.ptmr8t-x-x-90}

[ [31.]{.ptmr8t-x-x-90}
[[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}[ ]{.ptmr8t-x-x-90}]{.bibsp}]{.biblabel}[]{#Xchen2024understanding}[Florian
Chen, Felix Weitk]{.ptmr8t-x-x-90}[ämper, and Sagar Malhotra.
Understanding domain-size]{.ptmr8t-x-x-90} [generalization in markov
logic networks, 2024.]{.ptmr8t-x-x-90}
:::
