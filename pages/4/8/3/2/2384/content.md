#Contents#
* table of contents
{:toc}


## Idea

This page is used as a hub to gather references about [[category theory|category-theoretic]] work directly related to Biology. Biology can be seen as an umbrella term for a spectrum of scientific domains all interested in studying life, at various scales. A range of [[category theory|category-theoretic]] formalisms have been proposed to model these scales from DNA mechanisms to complex systems through protein dynamics. This page gathers works expressing their results in the language of biology by using category theory concepts. More works with potential applications to topics somewhat related to biological questions are referred at the end of the page.

## Categories

This section presents category theoretic models using categories as ways to describe biological mechanisms and relations.

### Ologs

Ontologies are used in genomics to classify categories of observable phenomena such as [diseases](https://www.ebi.ac.uk/ols/ontologies/doid) or [genes](http://geneontology.org/). D. Spivak proposed a model for ontologies called _Ologs_. Ologs are freely generated categories over graphs whose objects and arrows are defined by (English) sentences such that

* each object is a [nominal sentence](https://en.wikipedia.org/wiki/Nominal_sentence) about a given topic;

* each arrow is encoded by a [grammatical predicate](https://en.wikipedia.org/w/index.php?title=Predicate) starting with the verb _is_ but deprived of its last [grammatical object](https://en.wikipedia.org/wiki/Object) such that the arrow, its source and its target all together define a semantically correct (English) sentence.

The idea is that each arrow of an olog describe a fact about a given topic.

\begin{centre}
    \begin{xymatrix@C=10em}
        \fbox{$\textrm{chromosome }x$} \ar[r]^-{\textrm{is the owner of}} & \fbox{$\textrm{gene }y$} \ar[r]^-{\textrm{(which) is reponsible for}} & \fbox{$\textrm{disease }z$}
    \end{xymatrix}
\end{centre}


Ologs have been used to characterize hierarchies in biology.

### Segments {#CategoryOfSegments}

Categories of segments model natural and experimental operations that can be done on DNA segments. The definition of their arrows is simple but flexible enough to express a wide range of biological mechanisms occurring in genetics and related fields. 

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
For every preorder $(\Omega,\preceq)$, we define a _morphism of segments_ from segment $(n_0,n_1,t,c)$ on $\Omega$ to a segment $(n_0',n_1',t',c')$ on $\Omega$ as a pair $(f_1,f_0)$ where $f_1:[n_1] \to [n_1']$ is an order-preserving injection and $f_0:[n_0] \to [n_0']$ is an order-preserving surjection such that the relation $c'(f_0(i)) \preceq c(i)$ holds in $(\Omega,\preceq)$ for every $i \in [n_0]$.
=--

We define the _category of segments over a preorder $(\Omega,\preceq)$_ as the category $\mathbf{Seg}(\Omega)$ whose objects are segments over $\Omega$ and whose arrows are the morphisms of segments between them. 

If the preorder $(\Omega,\preceq)$ defines a [[lattice]], then we can show that the category $\mathbf{Seg}(\Omega)$ can be equipped with a [[site]] structure.

### References

Ologs and biology:

* DI Spivak, RE Kent, _Ologs: A categorical framework for knowledge representation_ [pdf](https://math.mit.edu/~dspivak/informatics/olog.pdf)
* JY Wong, J McDonald, M Taylor-Pinney, DI Spivak, KaplanDL , MJ Buehler, _Materials by Design: Merging Proteins and Music_, Nano Today. 2012 Dec 1;7(6):488-495. [link](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3752788/)
* T. Giesa, DI Spivak, MJ. Buehler, _Reoccurring patterns in hierarchical protein materials and music: The power of analogies_ [pdf](https://arxiv.org/pdf/1111.5297.pdf)

An introduction to categories of segments:

* R Tuyeras, _Category Theory for Genetics_,  [arXiv:1708.05255](https://arxiv.org/abs/1708.05255)

## Theories and models

This section presents category theoretic models taking the form of diagrams. These models can be either presented as functors with properties or as commutative diagrams. Common examples are models for a [[limit sketch]]. The first attempt to formalize biological systems in terms of this type of models was initiated by R. Rosen (see the references at the end of the page). However, Rosen's work stays quite abstract and does not treat of any specific biological phenomenon.

### Stock-flow diagrams and Petri nets

In the spirit of [[David Spivak|Spivak's]] approach in encoding databases as functors over small categories, functors have been used to encode environments to organize and hence model biological data. One example is that of stock-flow diagrams, which are defined as follows.

Let us denote as $\mathsf{H}$ the free category generated ove the following graph:

\begin{centre}
    \begin{xymatrix}
        \textrm{flow} \ar@<+1.2ex>[rr]^{u} \ar@<-1.2ex>[rr]_{d} && \textrm{stock}\\
        &\textrm{link}\ar[ru]_{s} \ar[lu]^{t} &
    \end{xymatrix}
\end{centre}

The previous diagram should be seen as a sketch specifying a structure in which there are _links_ that go from a _flow_ to a _stock_ such that each _flow_ goes from a _flow_ to  _flow_.

+-- {: .num_defn}
###### Definition
We define a _primitive stock-flow diagram_ as a functor $\mathsf{H} \to \mathbf{FinSet}$ where $\mathbf{FinSet}$ is the category of finite sets and functions.
=--

+-- {: .num_defn}
###### Definition
A _stock-flow diagram_ consists of primitive stock-flow diagram $F:\mathsf{H} \to \mathbf{FinSet}$ and, for every element $x \in F(\mathrm{flow})$, a continuous function $\mathbb{R}^{U_x} \to \mathbb{R}$ where $U_x$ denotes the finite fiber $F(t)^{-1}(x)$.
=--

There is a notion of _open_ stock-flow diagram that can be composed by using the composition of cospans. Stock-flow diagrams have been used to model epidemics and more specifically COVID-19.

### Pedigrads

A [[pedigrad]] is a model for a limit sketch defined on a [category of segments](#CategoryOfSegments) $\mathbf{Seg}(\Omega)$. The functors defining pedigrads are used to model genomic data and design algorithms to study them.

### References

Stock-flow diagrams and petri nets:

* J Baez, X Li, S Libkind, N Osgood and E Patterson, _Compositional modeling with stock and flow diagrams_, [pdf](https://arxiv.org/pdf/2205.08373.pdf)

* A Baas, J Fairbanks, M Halter, S Libkind and E Patterson, _An algebraic framework for structured epidemic modeling_, [pdf](https://arxiv.org/pdf/2203.16345.pdf)

* JC Baez, BS Pollard, _A Compositional Framework for Reaction Networks_, [pdf](https://arxiv.org/pdf/1704.02051.pdf)

Pedigrads:

* R Tuyeras, _Category theory for genetics I: mutations and sequence alignments_, Theory and Applications of Categories, Vol. 33, 2018, No. 40, pp 1269-1317, [pdf](http://www.tac.mta.ca/tac/volumes/33/40/33-40abs.html5)

* R Tuyeras, _Category theory for genetics II: genotype, phenotype and haplotype_, [pdf](https://arxiv.org/abs/1805.07004)

## Adjunctions

Adjunctions have been used to model pathogenes and diseases, and their corresponding immune response. For example, denote as $I$ the set of immune responses and as $P$ the set pathogenes and diseases. In practice, we can map a subset of $P$ to a subset of $I$. This defines a binary relation as follows.
$$
Q \subseteq \mathsf{Sub}(P) \times \mathsf{Sub}(I)
$$
We can complete this binary relation into a functor of the following form.
$$
Q: \mathsf{Sub}(P)^{\mathsf{op}} \times \mathsf{Sub}(I) \to \mathbf{2} = \{0 \leq 1\}.
$$
We can then define a functor $F:\mathsf{Sub}(I) \to \mathsf{Sub}(P)$ with the following specification.
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
&L(p) \subseteq i & \textrm{if immune response of a disease $p$ is in $i$}&\\
\ar@{-}[rrr]&&&\\    
&p \subseteq FL(p) \subseteq F(i) & \textrm{then disease $p$ describes conditions triggering $i$}&
    \end{xymatrix}
\end{centre}


We can embed the previous type of models in time and space by filtering the sets $P$ and $I$ into a sequence (or a category) of subsets containing chromological and spatial occurrences of diseases and their immune responses, respectively. In this case, the corresponding binary relations $Q \subseteq \mathsf{Sub}(P) \times \mathsf{Sub}(I)$ need to be defined for each time and space parameter in a functorial way.

\begin{centre}
    \begin{xymatrix}
        \mathsf{Sub}(P_1)\ar[r]\ar@{->}@<-1.2ex>[d]\ar@{<-}@<+1.2ex>[d]&\mathsf{Sub}(P_2)\ar[r]\ar@{->}@<-1.2ex>[d]\ar@{<-}@<+1.2ex>[d]&\dots\ar[r]&\mathsf{Sub}(P_n)\ar[r]\ar@{->}@<-1.2ex>[d]\ar@{<-}@<+1.2ex>[d]&\dots\\
        \mathsf{Sub}(I_1)\ar[r]&\mathsf{Sub}(I_2)\ar[r]&\dots\ar[r]&\mathsf{Sub}(I_n)\ar[r]&\dots\\
    \end{xymatrix}
\end{centre}

### References

* J-F Mascari, D Giacchero and N Sfakianakis, _Symetries and asymetries of the immune system response: A categorification approach_, 2017 IEEE International Conference on Bioinformatics and Biomedicine (BIBM), 2017, pp. 1451-1454, [pdf](http://www.mcs.st-and.ac.uk/~ns210/files/Masc-Sfak-Categor.pdf)

## Operads and algebras

### Trees

Operads have been used to model [phylogenetic trees](https://en.wikipedia.org/wiki/Phylogenetic_tree), see:

* [Operads and Phylogenetic Trees](https://golem.ph.utexas.edu/category/2015/12/operads_and_phylogenetic_trees.html)

### Axioms for algebras and gradient descent

A little-disc-operad-inspired formalism was developed to model biological systems and cellular behaviour. This formalism considers gradient descent techniques to make certain subsets $A \subseteq \mathbb{R}^{\times n}$ converge towards algebra-like structure. These gradient descent techniques use the equations encoding the axioms for algebras as objective functions. The resulting sets $A$ can be interpreted as models for specialization of biological functions and entropic mechanisms in living organisms.

### References

Phylogenies:

* JC Baez, N Otter, _Operads and Phylogenetic Trees_, Theory and Applications of Categories, Vol. 32 No. 40 (2017), 1397-1453, [paper](http://www.tac.mta.ca/tac/volumes/32/40/32-40abs.html)

Specialization and gradient descent:

* R Tuyeras et al., _Cellular intelligence: dynamic specialization through non-equilibrium multi-scale compartmentalization_, [bioarxiv](https://www.biorxiv.org/content/10.1101/2021.06.25.449951v1.abstract)


## Related fields

This section gathers works in domain that often use category theory as a language for logical discourse.

### Algebraic topology

Algebraic topology techniques and intuitions have been used to study neuronal morphologies.

### Algebraic geometry

Singularities in algebraic geometry have been used to study morphologies.

### References

* Kanari, Lida; Dłotko, Paweł; Scolamiero, Martina; Levi, Ran; Shillcock, Julian; Hess, Kathryn; Markram, Henry (2016), _Quantifying topological invariants of neuronal morphologies_, [arXiv:1603.08432](https://arxiv.org/abs/1603.08432)

* Lee, Yongjin; Barthel, Senja D.; Dłotko, Paweł; Moosavi, S. Mohamad; Hess, Kathryn; Smit, Berend (2017), _Pore-geometry recognition: on the importance of quantifying similarity in nanoporous materials_, [arXiv:1701.06953.](https://arxiv.org/abs/1701.06953)

*  E.C. Zeeman, _Catastrophe Theory_, Scientific American, April 1976; pp. 65–70, 75–83, [pdf](http://www.gaianxaos.com/pdf/dynamics/zeeman-catastrophe_theory.pdf)


## Higher structures

### Hyperstructures

Noticing that category theory at first is a formalism of _states_ and _processes_ (directed arrows) and $n$-category theory of processes of processes, etc., can we also naturally encode in its language _structures of structures_, i.e. hierarchical structures, which do not naturally or not manifestly have an interpretation as processes, in particular in that they are lacking the directionality of processes? Whatever the definition of [[hyperstructure]] really will be in the end, I think this question is what motivates them: a hyperstructure differs from an $\infty$-category in that in degree $n$ it has cells ( _bonds_ ) which _bind_ $(n-1)$-cells, but there is no directionality imposed on this, and not necessarily a notion of composition. 

Now, biological structures are often of the complex hierarchical structure that one would imagine the concept of  [[hyperstructure]] would describe to some extent, but if the notion of hyperstructure is good and natural, that should be just a very specific of a more general kind of applications which maybe should not be regarded as the archetypical application of the concept as such. In this respect it is maybe noteworthy that the idea of hyperstructure does not originate in a motivation from biology, but was originally conceived as a means to formalize [[extended cobordism]]s such as appear in the [[generalized tangle hypothesis]].

### n-Categories

According to [[Mikhail Gromov]], the mathematical structures nearest to what is happening in the mind are [[n-categories]].

### References

Higher categories:

* Talk by Mikhail Gromov, [Ergologic and Interfaces Between Languages](https://www.youtube.com/watch?v=jRSqGYJQQM8)

Hyperstructures:

* NA Baas, _On Higher Structures_, [arxiv](https://arxiv.org/pdf/1509.00403.pdf)

* NA Baas, _Extended Memory Evolutive Systems in a Hyperstructure Context. Axiomathes 19, 215–221 (2009). [link](https://doi.org/10.1007/s10516-009-9066-3)


## Other related works

A range of formalisms have been proposed to model complex systems, some with a category theoretic flavour. In particular [[process algebra]]s, such as the [[pi-calculus]] and its stochastic variant, have been used to [model](http://homepages.inf.ed.ac.uk/s0680923/bibliography.html) biological systems. (See also [here](http://www.itu.dk/research/pls/wiki/index.php/Reading_Group_:_Process_Algebraic_and_Agent-based_Modeling_of_Biological_Systems).)  Further developments point to Milner's [bigraphs](http://www.cl.cam.ac.uk/~rm135/uam-theme.html) ([bibliography](http://www.itu.dk/~mikkelbu/research/bigraphsbib/index.html)). In [Stochastic Bigraphs](http://www.lix.polytechnique.fr/~krivine/Research_files/KriMilTro08.pdf) the authors discuss membrane budding in a biological system.

For other approaches see [category theory and biology](http://golem.ph.utexas.edu/category/2007/11/category_theory_and_biology.html).


## Other references

* Lior Pachter, Bernd Sturmfels, _The mathematics of phylogenomics_, [math/0409132](http://arxiv.org/abs/math/0409132)

* V. Noel, D. Grigoriev, S. Vakulenko, O. Radulescu, _Tropical geometries and dynamics of biochemical networks. Application to hybrid cell cycle models_, [pdf](http://logic.pdmi.ras.ru/~grigorev/pub/tropical_dynamics_modified.pdf)

* A.C. Ehresmann and P. Smeonov. Wlimes: _Towards a theoretical framework for wandering logic intelligence memory evolutive systems_. In P. L. Simeonov, L. S. Smith, and A. C. Ehresmann, editors, Integral. Biomathics: Tracing the Road to Reality. Springer-Verlag, 2012.


* A.C. Ehresmann and J.-P. Vanbremeersch. _The memory evolutive systems as a model of Rosen's organisms_. Axiomathes, 16:165–214, 2006.

* A.C. Ehresmann and J.-P. Vanbremeersch. _Memory Evolutive Systems: Hierarchy, Emergence, Cognition_, volume 4 of Studies in Multidisciplinarity. Elsevier, 2007.

* A.C. Ehresmann, N. Baas, and J.-P. Vanbremeersch. _Hyperstructures and memory evolutive systems_.
Intern. J. Gen. Sys., 33(5):553–568, 2004.

* R Rosen, _The representation of biological systems from the standpoint of the theory of categories_ , Bulletin of Mathematical Biophysics, Vol 20. 1958, [pdf]( http://www.few.vu.nl/~rplanque/Onderwijs/MathBio/PapersForProject/Rosen.pdf)

* I. C. Baianu, James F. Glazebrook and Ronald Brown, _A Category Theory And Higher Dimensional Algebra Approach To Complex Systems Biology, Meta-systems And Ontological Theory Of Levels: Emergence Of Life, Society, Human Consciousness And Artificial Intelligence_, [text](https://planetmath.org/ACATEGORYTHEORYANDHIGHERDIMENSIONALALGEBRAAPPROACHTOCOMPLEXSYSTEMSBIOLOGYMETASYSTEMSANDONTOLOGICALTHEORYOFLEVELS)

* Dominique Pastor, Erwan Beurier, Andrée Ehresmann, Roger Waldeck, _Interfacing biology, category theory and mathematical statistics_, [https://arxiv.org/pdf/2009.06832.pdf](pdf)