
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

#CW complexes
* table of contents
{: toc}


## Idea

A **CW-complex** is a [[nice topological space]] which can be built up inductively, by a process of attaching disks along their boundaries. They are principal objects of interest in algebraic topology; in fact, most spaces of interest to algebraic topologists are [[homotopy equivalence|homotopy equivalent]] to CW-complexes. (And every space is [[weak homotopy equivalence|weakly homotopy equivalent]] to a CW-complex, but need not be strongly homotopy equivalent to one.) 


## Definition

A CW-complex is a topological space $X$ which can be presented as the colimit (in [[Top]], or else in the category of [[compactly generated space]]s or many another [[nice category of spaces]]) of spaces $X_n$ (called $n$-skeleta of the presentation) 

\[\label{CW1}X_0 \hookrightarrow X_1 \hookrightarrow \ldots \hookrightarrow X_n \hookrightarrow \ldots
\]

where each space $X_n$ is the result of attaching copies of the $n$-disk $D^n = \{x \in \mathbb{R}^n: ||x|| \leq 1\}$ along their boundaries $S^{n-1} = \partial D^n$ to $X_{n-1}$. Specifically, $X_0$ (the 0-skeleton) is a discrete space, and each $X_n$ is a pushout in [[Top]] of a diagram of the form 

$$X_{n-1} \stackrel{(f_i)}{\leftarrow} \coprod_{i \in I} S_{i}^{n-1} \stackrel{\coprod_i j_i}{\to} \coprod_{i \in I} D_{i}^n$$ 

where $I$ is some index set, each $j_i: S_{i}^{n-1} \to D_{i}^n$ is the boundary inclusion of a copy of $D^n$, and 
$f_i: S_{i}^{n-1} \to X_{n-1}$ is a continuous map, often called an _attaching map_. The coprojections $X_{n-1} \to X_n$ of these pushouts give the arrows on which diagram (eq:CW1) is based. 

A "relative" CW-complex $(X, A)$ is similar, except $X_0$ is the disjoint union of $A$ with a discrete space. 

A _finite CW-complex_ is one which admits a presentation in which there are only finitely many attaching maps, and similarly a _countable CW-complex_ is one which admits a presentation with countably many attaching maps. 

Milnor has argued that the category of spaces which are homotopy equivalent to CW-complexes, also called [[m-cofibrant space]]s, is a convenient category of spaces for algebraic topology.


## Examples

* The [[geometric realization]] of any locally finite [[simplicial set]] is a CW-complex. 

  * J. Milnor, _The geometric realization of a semi-simplicial complex_, Annals of Mathematics, 2nd Ser., __65__, n. 2. (Mar., 1957), pp. 357-362; [pdf](http://www.math.binghamton.edu/dwyer/Milnor-GeomReal.pdf)

  * In particular in the context of the [[homotopy hypothesis]] the [[Quillen equivalence]]  between [[∞-groupoid]]s and [[nice topological space]]s maps each [[∞-groupoid]] to a CW-complex.

* any [[compact space|noncompact]] [[smooth manifold]] of [[dimension]] $n$ is [[homotopy equivalence|homotopy equivalent]] to an $(n-1)$-dimensional CW-complex.

  Details on this are in 

  Mohan Ramachandran, Napier _Elementary Construction of Exhausting Subsolutions of Ellitpic Operators_ L'Enseignement Math&#233;matique, t. 50 (2004), p. 1&#8211;24

## References

* J.P. May, [[A Concise Course in Algebraic Topology]], U. Chicago Press, 1999. 

* J. Milnor, On spaces having the homotopy type of a CW-complex, Trans. Amer. Math. Soc. 90 (2) (1959), 272-280.


[[!redirects CW complex]]
[[!redirects CW-complex]]
[[!redirects CW complexes]]
[[!redirects CW-complexes]]