
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}



## Idea

The **Euler characteristic** of a [[space]] or [[∞-groupoid]] $X$ is an invariant of $X$ (a valued assigned to its [[equivalence class]]) that generalizes the [[cardinality]] of a set: where cardinality counts elements in a set, the Euler characteristic counts [[object]]s up to [[equivalence]]s up to [[2-morphism|2-equivalence]]s up to [[3-morphism|3-equivalence]], and so on. For  that reason it has also come to be known as [[groupoid cardinality]].

There are many different incarnations of [[space]]s and [[∞-groupoid]]s and accordingly there are many different definitions of Euler characteristics, that however agree in good cases.

For instance:

* The Euler characteristic of a [[topological space]] can be defined as the alternating sum of the ranks of its [[homology]] groups (when this is finite).

* There is a definition of Euler characteristic of a (finite) [[poset]], wich computes the topological Euler characteristic of its [[geometric realization of categories|geometric realization]]. This can be generalized to a notion of Euler characteristic of (finite) [[categories]].



## Definition

### Of a chain complex

+-- {: .num_defn #EulerCharOfChainComplex}
###### Definition

For $V$ a [[chain complex]] of [[module]]s over some [[ring]], its **Euler characteristic** is -- if it exists -- the [[integer]] given by the alternating sum of the [[rank]] of its [[homology group]]s

$$
  \chi(V) := \sum_{n \in \mathbb{Z}} (-1)^n rk_R H_n(V)
  \,.
$$

=--

+-- {: .num_remark }
###### Remark

The Euler characteristic of chain complexes is evidently invariant under the natural notion of [[equivalence in an (infinity,1)-category|equivalence]] of chain complexes: (zig-zags of) [[quasi-isomorphism]]s.

=--

### Of a topological space / of an $\infty$-groupoid

+-- {: .num_defn #EulerCharOfTopSpace}
###### Definition

For $X$ a [[topological space]] and $R$ some [[ring]], its Euler characteristic over $R$ is -- if it exists -- the Euler characteristic, according to def. \ref{EulerCharOfChainComplex}, of its [[homology]] [[chain complex]] (for instance [[singular homology]]): the alternating sum of its [[Betti number]]s

$$
  \chi(X) = \sum_{n \in \mathbb{N}} rk_{\mathbb{Z}} H_n(X, R)
  \,.
$$

=--

By default one takes $R = \mathbb{Z}$ to be the [[integer]]s.

This definition is usually known as the **Euler-Poincar&#233; formula**. Historically earlier was

+-- {: .num_defn #EulerCharOfCWComplex}
###### Definition/Proposition

Let $X$ be a finite [[CW-complex]]. Write $cell(X)_k$ for the set of its $k$-cells. Then the Euler characteristic of $X$ is

$$
  \chi(X) = \sum_{k \in \mathbb{N}} (-1)^k \vert cell(X)_k \vert
  \,.
$$

=--

In the special case that $X$ is a [[surface]] this reduces to the historical definition by [[Leonhard Euler]], which implicitly was known already to [[Rene Descartes]] around 1620:

+-- {: .num_defn #EulerCharOfSurface}
###### Definition/Proposition

Let $X$ be a convext [[polyhedron]]. Then its Euler characteristic is

$$
  \chi(X) = \vert Vertices(X)\vert - \vert Edges(X)\vert + 
   \vert Faces(X)\vert
  \,.
$$

=--

### Of posets, groupoids and categories

The process of sending a [[category]] $C$ to its 
[[geometric realization of categories]] ${\vert C \vert} \in $ [[Top]] $\simeq$ [[∞Grpd]] is a way to _present_ [[topological space]]s, and hence [[∞-groupoid]]s, by a category: we can think of $\vert C \vert$ as the [[Kan fibrant replacement]] of $C$: the [[universal property|universal solution]] to [[weak inverse|weakly inverting]] all [[morphism]]s of $C$.

In fact, up to the relevant notion of [[equivalence in an (infinity,1)-category]] (which is [[weak homotopy equivalence]]), _every_ [[∞-groupoid]] arises as the [[nerve]]/[[geometric realization of categories|geometric realization]] of a category. In fact one can assume the category to be a [[poset]]. (This follows from the existence of the [[Thomason model structure]], as discussed in more detail there.)

Since the combinatorial data in a [[category]] and all the more in a [[poset]] $C$ is much smaller than in that of its [[Kan fibrant replacement]] $|vert C \vert$, it is of interest to ask if one can read off the Euler characteristic $\chi(\vert C \vert)$ already from $C$ itself. This is indeed the case:

+-- {: .num_defn #EulerCharOfCat}
###### Definition

Let $C$ be a finite [[category]]. A **weighting** on $C$ is a [[function]]

$$
 k^{(-)} : ob C \to \mathbb{Q}
$$

satsifying 

$$
  \forall a \in ob C \;:\; \sum_{b \in ob C} \vert C(a,b) \vert k^b
  = 1
  \,,
$$

where $\vert C(a,b)\vert$ is the [[cardinality]]

$$
  \chi(C) := ...
$$

=--

The definition of Euler characteristic of [[poset]]s  appears for instance in ([Rota](#Rota)). For [[groupoid]] it has been amplified in [BaezDolan](#BaezDolan). The joint generalization to categories is due to ([Leinster](#Leinster)).

### Of an object in a symmetric monoidal category


+-- {: .num_defn #EulerCharInSymMonCat}
###### Definition

The Euler characteristic of a [[dualizable object]] in a [[symmetric monoidal category]] is the [[trace]] of its [[identity]] [[morphism]].

=--



## Properties

### General

Euler characteristic behaves well with respect to the basic operations in [[homotopy theory]]...

(...)

### Relations between the various definitions

The following propositions assert that and how the various definitions of Euler characteristics all suitably agree when thez jointly apply.

+-- {: .num_prop }
###### Proposition

For $X$ a [[compact space|compact]] [[manifold]] let $P_T(X)$ be the [[poset]] of inclusions of [[simplices]] of a [[triangulation]] $T$ of $X$. Then the poset Euler characteristic of $P_T(X)$ coincides with the Euler characteristic of $X$ as a topological space

$$
  \chi(X) = \chi(P_T(X))
  \,.
$$

=--

This appears as ([Stanley, 3.8](#Stanley)).

The following proposition asserts that the definition \ref{EulerCharOfCat} of Euler characteristic of a category is indeed consistent, in that it does compute the Euler characteristic, def. \ref{EulerCharOfTopSpace} of the corresponding $\infty$-groupoid:

+-- {: .num_prop }
###### Proposition

Let $C$ be a finite [[poset]] or, slightly more generally, a finite [[skeleton|skeletal]] [[category]] with no nontrivial [[endomorphism]]s.

Write $\vert C \vert \in $ [[Top]] $\simeq$ [[∞Grpd]] for its [[geometric realization of categories|geometric realization]]. Then

$$
  \chi(C) = \chi(\vert C \vert)
  \,.
$$
 
=--

For posets this is due to Philipp Hall, appearing as ([Stanley, prop. 3.8.5]) ([Leinster, cor. 1.5, prop. 2.11](#Leinster)).


+-- {: .num_prop }
###### Proposition

For $X$ a [[manifold]], regard its [[suspension spectrum]]

$$
  \Sigma^\infty X \in Ho(Spec)
$$

as an object in the [[stable homotopy category]]. Then its Euler characteristic as an object of a [[symmetric monoidal category]], def. \ref{EulerCharInSymMonCat} coincides with its topological Euler characteristic, def. \ref{EulerCharOfTopSpace}.

=--

This is due to ... (?)

+--{: .query}
[[Mike Shulman|Mike]]: Can the Euler characteristic of a category be recovered as the trace for a dualizable object in some symmetric monoidal category?
=---


## References

A standard textbook reference for topological Euler characteristics is page p. 156 and onwards in

* E.H. Spanier, _Algebraic topology_ , McGraw-Hill  (1966)  

Textbooks on combinatorial aspects of Euler characteristic include

* Richard P. Stanley, _Enumerative Combinatorics_ , Vol. I, Cambridge Studies in Advanced Mathematics 49, Cambridge University Press, corrected reprint (1997)
 {#Stanley}

* [[Gian-Carlo Rota]], _On the foundations of combinatorial theory I: theory of M&#246;bius functions_ , Z. Wahrscheinlichkeitstheorie und Verw. Gebiete 2 (1964), 340&#8211;368.
 {#Rota}

The Euler characteristic of groupoids -- [[groupoid cardinality]] -- has been amplified in 

* [[John Baez]], [[James Dolan]], _From Finite Sets to Feynman Diagrams_ ([arXiv](http://arxiv.org/abs/math.QA/0004133))
 {#BaezDolan}


The role of Euler characteristic of [[∞-groupoid]]s in [[quantization]] is touched on towards the end of

* [[Dan Freed]], [[Mike Hopkins]], [[Jacob Lurie]], [[Constantin Teleman]],  _[[Topological Quantum Field Theories from Compact Lie Groups]]_ 

The generalization of the definition of Euler characteristic from posets to categories is due to

* [[Tom Leinster]], _The Euler characteristic of a category_ ([arXiv](http://arxiv.org/abs/math/0610260))
  {#Leinster}

The compatibility of Euler characteristic of categories with [[homotopy colimits]] is discussed in 

* [[Thomas Fiore]], Wolfgang L&#252;ck, Roman Sauer, _Euler Characteristics of Categories and Homotopy Colimits_ ([arXiv:1007.3868](http://arxiv.org/abs/1007.3868))

More on Euler characteristics of categories is in

* Kazunori Noguchi, _The Euler characteristic of infinite acyclic categories with filtrations_, [arxiv/1004.2547](http://arxiv.org/abs/1004.2547)

