#Contents#
* table of contents
{:toc}


## Idea

This page is used as a hub to gather references about [[category theory|category-theoretic]] work (and more widely, other mathematical foundational work) with explicit applications to biology. 


_Biology_ can be seen as an umbrella term for a spectrum of scientific domains all interested in studying life, at various [scales](https://en.wikipedia.org/wiki/Biological_organisation). A range of category-theoretic formalisms have now been proposed to model these scales, from [DNA mechanisms](https://www.cdc.gov/genomics/about/basics.htm) to [complex systems](https://en.wikipedia.org/wiki/Complex_system) through [protein interactions](https://en.wikipedia.org/wiki/Protein%E2%80%93protein_interaction). This page gathers works expressing their results in the language of biology by using category theory concepts. More works with potential applications to topics somewhat related to biological questions are referred at the end of the page.

## Categories

This section presents category theoretic models using categories as ways to describe biological mechanisms and relations.

### Ologs

[[ontology|Ontologies]] are used in [genomics](https://en.wikipedia.org/wiki/Genomics) to classify categories of observable phenomena such as [diseases](https://www.ebi.ac.uk/ols/ontologies/doid) or [gene expressions](https://en.wikipedia.org/wiki/Gene_Ontology). Ontologies can be formalized with category theory as [[ontology log|ontology logs]], or "ologs" for short. The idea is that an olog is like a [[diagram]] where each arrow describes an aspect of some types of things under study. For example, the following olog describes [single-gene genetic disorders](https://en.wikipedia.org/wiki/Genetic_disorder):

\begin{centre}
    \begin{xymatrix@C=10em}
        \fbox{$\textrm{a (monogenic) genetic disorder}$} \ar[r]^-{\textrm{is provoked by mutations in}} & \fbox{$\textrm{a gene}$} \ar[r]^-{\textrm{is found in}} & \fbox{$\textrm{a chromosome}$}
    \end{xymatrix}
\end{centre}


Ologs have been used to characterize hierarchies in biology.

### Segments {#CategoryOfSegments}

Categories of segments aim to model the set of natural and experimental operations that can be done on [DNA segments](https://en.wikipedia.org/wiki/DNA). The definition of their arrows is simple but flexible enough to express a wide range of biological mechanisms occurring in [genetics](https://en.wikipedia.org/wiki/Genetics) and related fields. 

For every non-negative integer $n$, we will denote the set $\{1,2,\dots,n\}$ as $[n]$. Note that $[0] = \emptyset$.

+-- {: .num_defn}
###### Definition
For every preorder $(\Omega,\preceq)$, we define a _segment on $\Omega$_ as a tuple $(n_0,n_1,t,c)$ where $n_0$ and $n_1$ are non-negative integers, $t:[n_1] \to [n_0]$ is an order-preserving surjection and $c:[n_0] \to \Omega$ is a function.
=--

If we take the preorder $\mathbf{2} = \{ 0\leq 1\}$, then the following diagram represents a segment $(14,5,c,t)$ in $\mathbf{2}$; the brackets represent the fibers of the order-preserving surjection $t$ while the corresponding colors represent the mappings of the function $c$, which lands in the set $\mathbf{2}$.

\begin{centre}
    \begin{xymatrix@C=-5pt}
       (\bullet&\bullet&\bullet)&(\circ&\circ)&(\bullet&\bullet&\bullet&\bullet)&(\circ&\circ)&(\bullet&\bullet&\bullet)
    \end{xymatrix}
\end{centre}


+-- {: .num_defn}
###### Definition
For every preorder $(\Omega,\preceq)$, we define a _morphism of segments_ from segment $(n_0,n_1,t,c)$ on $\Omega$ to a segment $(n_0',n_1',t',c')$ on $\Omega$ as a pair $(f_1,f_0)$ where $f_1:[n_1] \to [n_1']$ is an order-preserving injection and $f_0:[n_0] \to [n_0']$ is an order-preserving function such that the relation $c'(f_0(i)) \preceq c(i)$ holds in $(\Omega,\preceq)$ for every $i \in [n_0]$.
=--

We define the _category of segments over a preorder $(\Omega,\preceq)$_ as the category $\mathbf{Seg}(\Omega)$ whose objects are segments over $\Omega$ and whose arrows are the morphisms of segments between them. 

We can show that if the preorder $(\Omega,\preceq)$ defines a [[lattice]], then the category $\mathbf{Seg}(\Omega)$ can be equipped with a [[site]] structure.

### References

Ologs and biology:

* JY Wong, J McDonald, M Taylor-Pinney, [[David Spivak|DI Spivak]], KaplanDL , MJ Buehler, _Materials by Design: Merging Proteins and Music_, Nano Today. 2012 Dec 1;7(6):488-495,  [link](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3752788/)
* T. Giesa, [[David Spivak|DI Spivak]], MJ. Buehler, _Reoccurring patterns in hierarchical protein materials and music: The power of analogies_, [pdf](https://arxiv.org/pdf/1111.5297.pdf)

Introductory material for categories of segments:

* A [talk](https://www.youtube.com/watch?v=l2PB9by6IBc) by [[Kenny Courser|K Courser]]. 

* [[Remy Tuyeras|R Tuyeras]], _Category Theory for Genetics_,  [arXiv:1708.05255](https://arxiv.org/abs/1708.05255)

## Theories and models

This section presents category theoretic models taking the form of diagrams. These models can be either presented as functors with properties or as commutative diagrams. Common examples are models for a [[limit sketch]]. The first attempt to formalize biological systems in terms of diagrams (with limits) was initiated by Robert Rosen (see the references at the end of the page). However, Rosen's work stays quite abstract and does not treat of any specific biological phenomenon.

### Stock-flow diagrams and Petri nets

In the spirit of [[David Spivak|Spivak's]] approach in encoding databases as functors over small categories, functors have been used to organize (and hence model) biological data. One example is that of stock-flow diagrams, which are defined as follows.

Let us denote as $\mathsf{H}$ the free category generated over the following graph:

\begin{centre}
    \begin{xymatrix}
        \textrm{flow} \ar@<+1.2ex>[rr]^{u} \ar@<-1.2ex>[rr]_{d} && \textrm{stock}\\
        &\textrm{link}\ar[ru]_{s} \ar[lu]^{t} &
    \end{xymatrix}
\end{centre}

The previous diagram should be seen as a sketch specifying a structure in which there are _links_ that go from a _stock_ to a _flow_ such that each _flow_ goes from a _stock_ to another _stock_.

+-- {: .num_defn}
###### Definition
We define a _primitive stock-flow diagram_ as a functor $\mathsf{H} \to \mathbf{FinSet}$ where $\mathbf{FinSet}$ is the category of finite sets and functions.
=--

+-- {: .num_defn}
###### Definition
A _stock-flow diagram_ consists of primitive stock-flow diagram $F:\mathsf{H} \to \mathbf{FinSet}$ and, for every element $x \in F(\mathrm{flow})$, a continuous function $\mathbb{R}^{U_x} \to \mathbb{R}$ where $U_x$ denotes the finite fiber $F(t)^{-1}(x)$.
=--

There is a notion of _open_ stock-flow diagram that can be composed by using the composition of cospans. Stock-flow diagrams have been used to model [epidemics](https://en.wikipedia.org/wiki/List_of_epidemics) and more specifically [COVID-19](https://en.wikipedia.org/wiki/COVID-19).

### Pedigrads

A [[pedigrad]] is a model for a limit sketch defined on a [category of segments](#CategoryOfSegments). The functors defining pedigrads can land in any types of categories. These functors have been used to model [genomic data](https://en.wikipedia.org/wiki/Genomics) and design algorithms to study them.

### References

Stock-flow diagrams and petri nets:

* [[John Baez|JC Baez]], X Li, S Libkind, N Osgood and E Patterson, _Compositional modeling with stock and flow diagrams_, [arXiv:2205.08373](https://arxiv.org/abs/2205.08373)

* A Baas, J Fairbanks, M Halter, S Libkind and E Patterson, _An algebraic framework for structured epidemic modeling_, [arXiv:2203.16345](https://arxiv.org/abs/2203.16345)

* [[John Baez|JC Baez]], BS Pollard, _A Compositional Framework for Reaction Networks_, [arXiv:1704.02051](https://arxiv.org/abs/1704.02051)

Pedigrads:

* [[Remy Tuyeras|R Tuyeras]], _Category theory for genetics I: mutations and sequence alignments_, Theory and Applications of Categories, Vol. 33, 2018, No. 40, pp 1269-1317, [link](http://www.tac.mta.ca/tac/volumes/33/40/33-40abs.html)

* [[Remy Tuyeras|R Tuyeras]], _Category theory for genetics II: genotype, phenotype and haplotype_, [arXiv:1805.07004](https://arxiv.org/abs/1805.07004)

* [[Remy Tuyeras|R Tuyeras]], _A category theoretical argument for causal inference_, [arXiv:2004.09999](https://arxiv.org/abs/2004.09999)


## Adjunctions

[[adjunction|Adjunctions]] have been used to model [pathogens](https://en.wikipedia.org/wiki/Pathogen) and [disease diagnoses](https://en.wikipedia.org/wiki/Disease), and their corresponding [immune response](https://en.wikipedia.org/wiki/Immune_response). For example, denote as $I$ the set of immune responses and as $P$ the set pathogens and [disease symptoms](https://en.wikipedia.org/wiki/Signs_and_symptoms). In practice, we can map a subset of $P$ to a subset of $I$. This defines a binary relation as follows.
$$
Q \subseteq \mathsf{Sub}(P) \times \mathsf{Sub}(I)
$$
We can complete this binary [[relation]] into a functor of the following form.
$$
Q: \mathsf{Sub}(P)^{\mathsf{op}} \times \mathsf{Sub}(I) \to \mathbf{2} = \{0 \leq 1\}.
$$
We can then define a [[functor]] $F:\mathsf{Sub}(I) \to \mathsf{Sub}(P)$ with the following specification.
$$
F(i) = \bigcup\{p| Q(p,i) = 1\}
$$
If the binary relation $Q$ is defined such that $F$ preserves [[meet|meets]] (ie. intersections), then we can use the [[adjoint functor theorem]] to define a left-adjoint $L:\mathsf{Sub}(P) \to \mathsf{Sub}(I)$ for the functor $F$.
$$
L(p) = \bigcap\{i|p \subseteq F(i)\}
$$
The previous adjunction gives us a context in which we can reason about immune responses and their triggering pathogens and diseases. Further, the adjunction formalism ensures a certain _continuity_ in time and space regarding the linking of diseases/pathogens to their immune response (as suggested in the following correspondence).


\begin{centre}
\begin{xymatrix@R=-2pt[font = \large]}
&p \subseteq F(i) & \textrm{\normalsize{if a disease $p$ describes conditions (reportedly) triggering $i$}}&\\
\ar@{-}[rrr]&&&\\ 
&L(p) \subseteq LF(i) \subseteq i & \textrm{\normalsize{then the (expected) immune response for $p$ is in $i$}}&   
    \end{xymatrix}
\end{centre}


We can embed the previous type of models in time and space by filtering the sets $P$ and $I$ into a sequence (or a category) of subsets containing chronological and spatial occurrences of diseases and their immune responses, respectively. In this case, the corresponding binary relations $Q \subseteq \mathsf{Sub}(P) \times \mathsf{Sub}(I)$ need to be defined for each time and space parameter in a functorial way.

\begin{centre}
    \begin{xymatrix}
        \mathsf{Sub}(P_1)\ar[r]\ar@{->}@<-1.2ex>[d]\ar@{<-}@<+1.2ex>[d]&\mathsf{Sub}(P_2)\ar[r]\ar@{->}@<-1.2ex>[d]\ar@{<-}@<+1.2ex>[d]&\dots\ar[r]&\mathsf{Sub}(P_n)\ar[r]\ar@{->}@<-1.2ex>[d]\ar@{<-}@<+1.2ex>[d]&\dots\\
        \mathsf{Sub}(I_1)\ar[r]&\mathsf{Sub}(I_2)\ar[r]&\dots\ar[r]&\mathsf{Sub}(I_n)\ar[r]&\dots\\
    \end{xymatrix}
\end{centre}

### References

* [[Gianfranco Mascari|J-F Mascari]], D Giacchero and N Sfakianakis, _Symetries and asymetries of the immune system response: A categorification approach_, 2017 IEEE International Conference on Bioinformatics and Biomedicine (BIBM), 2017, pp. 1451-1454, [pdf](http://www.mcs.st-and.ac.uk/~ns210/files/Masc-Sfak-Categor.pdf)

## Operads and algebras

### Trees

[[operad|Operads]] have been used to model [phylogenetic trees](https://en.wikipedia.org/wiki/Phylogenetic_tree), see:

* [Operads and Phylogenetic Trees](https://golem.ph.utexas.edu/category/2015/12/operads_and_phylogenetic_trees.html)

### Axioms for algebras and gradient descent

A [[little cubes operad|little-disc-operad-inspired]] formalism was developed to model biological systems and cellular behaviors. This formalism considers [gradient descent](https://en.wikipedia.org/wiki/Gradient_descent) techniques to make certain subsets $A \subseteq \mathbb{R}^{\times n}$ converge towards [[algebra over an operad|algebra-like structures]]. 

More specifically, these gradient descent techniques use the underlying equations of the axioms for algebras as [objective functions](https://en.wikipedia.org/wiki/Loss_function). The sets $A$ obtained through these optimizations can be interpreted as models for [specialization of biological functions](https://en.wikipedia.org/wiki/Specialization) and [[entropy|entropic]] mechanisms in living organisms.

### References

Phylogenies:

* [[John Baez|JC Baez]], N Otter, _Operads and Phylogenetic Trees_, Theory and Applications of Categories, Vol. 32 No. 40 (2017), 1397-1453, [paper](http://www.tac.mta.ca/tac/volumes/32/40/32-40abs.html)

Specialization and gradient descent:

* [[Remy Tuyeras|R Tuyeras]] et al., _Cellular intelligence: dynamic specialization through non-equilibrium multi-scale compartmentalization_, [bioarxiv](https://www.biorxiv.org/content/10.1101/2021.06.25.449951v1.abstract)


## Related fields

This section gathers works in domains that often use category theory as a language for logical discourse.

### Algebraic topology

[[algebraic topology|Algebraic topology]] techniques and intuitions developed along with [[persistent homology]] have been used to study neuronal morphologies.

Additionally, the clustering algorithm [UMAP](https://umap-learn.readthedocs.io/en/latest/), commonly-used in computational biology to classify sequencing data, relies on properties holding for [[fuzzy simplicial set]]s. For more detail, see the following blog post:

* [[John Baez|JC Baez]], [The Category Theory Behind UMAP](https://johncarlosbaez.wordpress.com/2020/02/10/the-category-theory-behind-umap/), Azimuth


### Algebraic geometry

The concept of [[singularity|singularities]], in [[algebraic geometry]], has been used to model anatomic morphologies and behaviors.

Additionally, various concepts of algebraic geometry such as [[manifold|manifolds]] and [[moduli space|moduli spaces]] have been used by [[Mikhail Gromov|M Gromov]] to model molecular mechanisms in living cells.

### References

Persistent homology:

* L Kanari, P Dłotko, M Scolamiero, R Levi, J Shillcock, [[Kathryn Hess|K Hess]], H Markram (2016), _Quantifying topological invariants of neuronal morphologies_, [arXiv:1603.08432](https://arxiv.org/abs/1603.08432)

* Y Lee, SD Barthel, P Dłotko, SM Moosavi, [[Kathryn Hess|K Hess]], B Smit, (2017), _Pore-geometry recognition: on the importance of quantifying similarity in nanoporous materials_, [arXiv:1701.06953.](https://arxiv.org/abs/1701.06953)

Fuzzy simplicial sets:

* A Jackson, _The mathematics of UMAP_, [pdf](https://adelejackson.github.io/files/Maths_of_UMAP.pdf)

* [[David Spivak|DI Spivak]], _Metric Realization of Fuzzy Simplicial Sets_, [pdf](https://math.mit.edu/~dspivak/files/metric_realization.pdf)


Algebraic geometry:

*  EC Zeeman, _Catastrophe Theory_, Scientific American, April 1976; pp. 65–70, 75–83, [pdf](http://www.gaianxaos.com/pdf/dynamics/zeeman-catastrophe_theory.pdf)

* [[Mikhail Gromov|M Gromov]], Mathematical slices of molecular biology, [pdf](https://www.ihes.fr/~gromov/wp-content/uploads/2018/08/M01-03.pdf)

## Higher structures

### Hyperstructures


[[Nils Baas|N Baas]] has proposed [[hyperstructure|hyperstructures]] to describe hierarchical organizations in biology. While these structures were originally designed to organize [[extended cobordism]] structures, they are argued to also be appropriate for modeling multilevel systems in biology. Note that contrarily to multilevel structures such as [[n-category|$n$-categories]], hyperstructures offer more freedom in that biological processes are not necessarily oriented as [[globe|globular arrows]] but, instead, appear to be organized as "aggregates" with _bonds_.

The idea behind applying hyperstructures to biology is that they allow us to consider some set $X_0$ of "agents" such that any subset $S \subseteq X_0$ can define an _aggregate_ when it is "labeled" by an explanation (or description) $\omega$ for that aggregation.
\begin{centre}
    \begin{xymatrix@C=+80pt}
X_0 = \{\textrm{all cells}\} \ar[r]^-{\textrm{consider a subset}}& S = \{\textrm{all liver cells}\} \ar[r]^-{\textrm{label with}} & \omega = \fbox{$\textrm{liver cell}$} \ar[r]^{\textrm{define}}& (S,\omega)\textit{ an organ; a liver}
    \end{xymatrix}
\end{centre}
The pair $(S,\omega)$ can then be represented by another label, say $\beta$, that can classify a collection of pairs sharing similarities.
\begin{centre}
    \begin{xymatrix}
(S,\omega) = (\{\textrm{all liver cells for individual $i$}\}, \fbox{$\textrm{liver cell}$}) \ar@{|->}[r]&\beta = \fbox{$\textrm{liver in an individual}$}
    \end{xymatrix}
\end{centre}
The previous construction can then be repeated recursively on the set of labels $\beta$. This set, call it $X_1$, could potentially be the set of all the [biological organs](https://en.wikipedia.org/wiki/Organ) in an individual. Then, the next level $X_2$ (obtained from $X_1$ by following the previous procedure) can be the set of all [organ systems](https://en.wikipedia.org/wiki/Organ_system), which can subsequently be organized as [bodies](https://en.wikipedia.org/wiki/Human_body) on a fourth level $X_3$.

Note that hyperstructures also require compatibility properties between the labels. In particular, for each level $X_k$, the pairs $(S,\omega)$ should be organized into a [[Grothendieck construction]] $\int \Omega$ such that the mappings $(S,\omega) \mapsto \beta$ define a [[functor]] $\int \Omega \to \mathbf{Set}$.


### Bigraphs, $\lambda$-calculus and $\pi$-calculus

[Bigraphs](https://en.wikipedia.org/wiki/Bigraph) are a type of [[hypergraph|hypergraph-based]] structures that can be linked to [process algebras](https://en.wikipedia.org/wiki/Process_calculus) such as the [[lambda-calculus|$\lambda$-calculus]], the [$\pi$-calculus](https://en.wikipedia.org/wiki/%CE%A0-calculus) and its [stochastic variant](https://link.springer.com/referenceworkentry/10.1007/978-1-4419-9863-7_767). Each of these calculus formalisms has been used to model biological systems. 

Interestingly, it was shown that the $\pi$-calculus can be interpreted within a [[2-category theory|2-category-theoretic]] setting. 

A number of bigraph-based formalisms have been proposed to model complex systems, some with a category theoretic flavor. For example, [stochastic bigraphs](https://www.pure.ed.ac.uk/ws/portalfiles/portal/15231648/Stochastic_Bigraphs.pdf) and their compositions have been used to model [membrane budding](https://en.wikipedia.org/wiki/Budding) in a biological system.

### References

Hyperstructures:

* [[Nils Baas|NA Baas]], _On the Philosophy of Higher Structures_, [arXiv:1805.11943](https://arxiv.org/pdf/1805.11943.pdf)

* [[Nils Baas|NA Baas]], _On Higher Structures_,  [arXiv:1509.00403](https://arxiv.org/pdf/1509.00403.pdf)

* [[Nils Baas|NA Baas]], _Extended Memory Evolutive Systems in a Hyperstructure Context. Axiomathes 19, 215–221 (2009), [link](https://doi.org/10.1007/s10516-009-9066-3)

Bigraphs:

*  [[Robin Milner|R Milner]], _Bigraphs and Their Algebra_, Electronic Notes in Theoretical Computer Science
Volume 209, 24 April 2008, Pages 5-19, [link](https://www.sciencedirect.com/science/article/pii/S157106610800217X)

* J Krivine, [[Robin Milner|R Milner]], A Troina, _Stochastic Bigraphs_, Electronic Notes in Theoretical Computer Science
Volume 218, 22 October 2008, Pages 73-9, [link](https://www.sciencedirect.com/science/article/pii/S1571066108004003)

Relations between $\lambda$-calculus, $\pi$-calculus and biology:

* S Federhen, _Replication is Recursion; or, Lambda: the Biological Imperative_, [bioarxiv](https://www.biorxiv.org/content/biorxiv/early/2015/05/01/018804.full.pdf)

* [A Regev](https://en.wikipedia.org/wiki/Aviv_Regev), W Silverman, E Shapiro E, _Representation and simulation of biochemical processes using the pi-calculus process algebra_, Pacific Symposium on Biocomputing 6:459-470 (2001), [pdf](http://psb.stanford.edu/psb-online/proceedings/psb01/regev.pdf)

* See the blog post by [[John Baez]]: [Biology and the Pi-Calculus](https://johncarlosbaez.wordpress.com/2016/01/02/biology-and-the-pi-calculus/)

* [[Mike Stay|M Stay]], LG Meredith, _Higher category models of the pi-calculus_, [arXiv:1504.04311](https://arxiv.org/abs/1504.04311)

## Other references

A general discussion on using category theory for biology can be found on the $n$-category café:

* [category theory and biology](http://golem.ph.utexas.edu/category/2007/11/category_theory_and_biology.html).

Phylogenomics:

* L Pachter, B Sturmfels, _The mathematics of phylogenomics_, [math/0409132](http://arxiv.org/abs/math/0409132)

Cell biology:

* V Noel, D Grigoriev, S Vakulenko, O Radulescu, _Tropical geometries and dynamics of biochemical networks. Application to hybrid cell cycle models_, [pdf](http://logic.pdmi.ras.ru/~grigorev/pub/tropical_dynamics_modified.pdf)


Systems biology:

* Robert Rosen, _The representation of biological systems from the standpoint of the theory of categories_ , Bulletin of Mathematical Biophysics, Vol 20. 1958, [pdf]( http://www.few.vu.nl/~rplanque/Onderwijs/MathBio/PapersForProject/Rosen.pdf)

* IC Baianu, JF Glazebrook and R Brown, _A Category Theory And Higher Dimensional Algebra Approach To Complex Systems Biology, Meta-systems And Ontological Theory Of Levels: Emergence Of Life, Society, Human Consciousness And Artificial Intelligence_, [text](https://planetmath.org/ACATEGORYTHEORYANDHIGHERDIMENSIONALALGEBRAAPPROACHTOCOMPLEXSYSTEMSBIOLOGYMETASYSTEMSANDONTOLOGICALTHEORYOFLEVELS)

* Jan-Hendrik S. Hofmeyr, _A biochemically-realisable relational model of the self-manufacturing cell_, Biosystems Volume 207, September 2021, [doi: 10.1016/j.biosystems.2021.104463](https://doi.org/10.1016/j.biosystems.2021.104463)

* Federico Vega, _The cell as a realization of the (M, R) system_, Biosystems Volume 225, March 2023,
[doi:10.1016/j.biosystems.2023.104846](https://doi.org/10.1016/j.biosystems.2023.104846

Neuroscience:

* According to [[Mikhail Gromov]], the mathematical structures nearest to what is happening in the mind are [[n-categories]]. See his talk: [Ergologic and Interfaces Between Languages](https://www.youtube.com/watch?v=jRSqGYJQQM8)


* [[Andree Ehresmann|AC Ehresmann]] and P S Wlimes, _Towards a theoretical framework for wandering logic intelligence memory evolutive systems_. In P. L. Simeonov, L. S. Smith, and A. C. Ehresmann, editors, Integral. Biomathics: Tracing the Road to Reality. Springer-Verlag, 2012.


* [[Andree Ehresmann|AC Ehresmann]], J-P Vanbremeersch, _The memory evolutive systems as a model of Rosen's organisms_. Axiomathes, 16:165–214, 2006.

* [[Andree Ehresmann|AC Ehresmann]], J-P Vanbremeersch. _Memory Evolutive Systems: Hierarchy, Emergence, Cognition_, volume 4 of Studies in Multidisciplinarity. Elsevier, 2007.

* [[Andree Ehresmann|AC Ehresmann]], [[Nils Baas|N Baas]], and J-P Vanbremeersch. _Hyperstructures and memory evolutive systems_.
Intern. J. Gen. Sys., 33(5):553–568, 2004.

* D Pastor, E Beurier, [[Andree Ehresmann|AC Ehresmann]], R Waldeck, _Interfacing biology, category theory and mathematical statistics_, [pdf](https://arxiv.org/pdf/2009.06832.pdf)

The following article views biological systems as
information-processing agents, supporting recursion $\gt$ function hypothesis

* Sara Imari Walker, Paul C. W. Davies, _The algorithmic origins of life_, Journal of the Royal Society Interface, 10(79) 2013 [doi](https://doi.org/10.1098/rsif.2012.0869)