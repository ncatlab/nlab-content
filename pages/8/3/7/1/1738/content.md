
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

\tableofcontents

## Definition

The **[[walking]] morphism** ([Ozornova & Rovelli 2024](#OR24), [Cisinski et al.](#CCNW)), **[[free-standing]] morphism**, or **[[free-living]] morphism** -- often denoted $2$ or $I$ or $\Delta[1]$ -- is the [[category]] with two [[object]]s and precisely one nontrivial [[morphism]] connecting them:

$$
  I =
  \left\{
    0 \to 1
  \right\}
  \,.
$$

The walking morphism serves as a [[combinatorial]] model for the [[directed space|directed]] [[interval]], hence the notation $I$. It is the directed canonical [[interval object]] in [[Cat]]. As a result, it may be called the **directed interval** or **directed interval category**. It may also be called the **interval** or **interval category**, although both terms are overloaded: 

* [[interval]] is also used in [[topology]] for the [[topological interval]] and in [[order theory]] for [[under categories]] and [[over categories]] of [[posets]]. It also appears in [[category theory]] in the term [[interval groupoid]] for the [[walking isomorphism]].  

* [[interval category]] is also used in [[category theory]] for the [[factorization category]] of a [[morphism]]

It is also commonly called the **interval preorder** or the **interval poset** (since it is indeed a [[poset]]).  

The walking morphism might also be called the "arrow category" although that term is [[arrow category|also used]] for a category of functors out of $I$. 

The notation $2$ comes from the fact that the walking morphism is also the [[ordinal number]] $2$ regarded as a [[poset]], regarded as a category.

It also appears as 

* the 1-[[simplex]];

* the first [[oriental]]; 

* the [[1-globe]].

Since every [[category]] is also an [[(n,r)-category]] for $n,r \geq 1$, we may regard $I$ also as some $(n,r)$-category. For instance regarded as a [[(∞,1)-category]] and modeled as a [[quasi-category]], the walking morphism is the [[simplicial set]] $\Delta[1]$.

## Properties

### Relation to the boolean domain

The [[boolean domain]] $\mathbb{2}$ is the [[discrete category]] consisting of two objects $0, 1 \in \mathbb{2}$. The boolean domain is the [[groupoid]] [[core]] of the walking morphism, and it is a [[fully faithful]] [[subcategory]] of the walking morphism. 

### Directed univalence

Since the groupoid core of the walking morphism is the boolean domain, using the [[recursion principle]] of the boolean domain, we can recursively define a [[family of sets]] $B:I \to \mathrm{Set}$ by $B_0 = \emptyset$ and $B_1 = \{*\}$ (Note that $B$ is not a [[functor]] as it doesn't preserve [[morphisms]]).

The walking morphism satisfies [[directed univalence]]: for all objects $x, y \in I$, we have a [[bijection]] between the [[function set]] $B_y^{B_x}$ and the [[hom-set]] $\mathrm{hom}_I(x, y)$. 

### Relation to the walking commutative triangle

The [[functor category]] $I^I$ is [[equivalence of categories|equivalent]] to the [[walking commutative triangle]] $\Delta[2]$ consisting of three objects $0, 1, 2 \in \Delta[2]$ and three morphisms $h_{01}:\mathrm{hom}_{\Delta[2]}(0, 1)$, $h_{02}:\mathrm{hom}_{\Delta[2]}(0, 2)$, $h_{12}:\mathrm{hom}_{\Delta[2]}(1, 2)$, such that $h_{02} = h_{12} \circ h_{01}$. This is equivalently [[Phoa's principle]] for $\mathbb{I}$ as a [[poset]]. 

### Relation to the walking isomorphism

Inverting the single non-identity arrow of the walking morphism, we obtain the [[walking isomorphism]], which is an (undirected) [[interval object]] in [[Cat]] and [[Grpd]].

## In dependent type theory

There are many [[dependent type theories]] which have a *directed interval [[type]]* $\mathbb{I}$ representing the walking morphism in the sense that given a type $A$, we have an equivalence of types between the [[function type]] from $\mathbb{I}$ to $A$ and the fibered [[hom type]] in $A$. 

$$\left(\mathbb{I} \to A\right) \simeq \left(\sum_{x:A} \sum_{y:A} \mathrm{hom}_A(x, y)\right)$$

### In simplicial type theory

In [[simplicial type theory]], the **directed interval type** ([Riehl & Shulman 2017](#RS17)) is a [[bounded total order]] $\mathbb{I}$. In [Gratzer, Weinberger & Buchholtz 2024](#GWB24) and [Gratzer, Weinberger & Buchholtz 2025](#GWB25), the directed interval type additionally satisfies [[synthetic quasi-coherence]] for finitely generated $\mathbb{I}$-algebras, which is sufficient to prove that $\mathbb{I}$ is a synthetic category in the sense of being a [[simplicial type|simplicial]] [[Rezk complete type|Rezk complete]] [[Segal type]], and the [[axiom]] that $\flat \mathbb{I} \simeq \mathrm{bool}$ which says that the [[core]] of the directed interval is the [[type of booleans]]. 

### In binary parametric observational type theory

In parametric observational type theory with binary [[internal parametricity]] or [[modal parametricity]], [[bridge types]] behave as [[hom types]] and [[heterogeneous bridge types]] behave as [[heterogeneous hom types]], and one can define the directed interval type as a [[higher inductive type]]. The [[inference rules]] are the same as that of the homotopical [[interval type]], except one uses the [[bridge types]] $\mathrm{Br}_A(x, y)$ instead of the [[identity types]] $\mathrm{Id}_A(x, y)$ for path constructors and the induction principle. 

\begin{definition}
The **directed interval type** is a type $\mathbb{I}$ with elements $0:\mathbb{I}$ and $1:\mathbb{I}$ and bridge $h:\mathrm{Br}_\mathbb{I}(0, 1)$ such that for any type family $(P(x))_{x:\mathbb{I}}$ with elements $p_0:P(0)$ and $p_1:P(1)$ and heterogeneous bridge $p_h:\mathrm{hBr}_P^h(p_0, p_1)$, one can construct a dependent function $p:\prod_{x:\mathbb{I}} P(x)$ such that 

$$p(0) \equiv p_0:P(0) \qquad p(1) \equiv p_1:P(1) \qquad \mathrm{apd}_P(p, 0, 1, h) \equiv p_h:\mathrm{hBr}_P^h(p_0, p_1)$$
\end{definition}

In the event that the [[bridge types]] are [[identity types]], such as in [[higher observational type theory]], this results in the usual notion of a homotopical [[interval type]]. However, one can also postulate that $0 \neq 1$ in the directed interval, making the directed interval $\mathbb{I}$ different from the homotopical interval type. 

## Applications

The walking morphism is one of those [[diagram]] category that are not terribly interesting in themselves, but that serve an important role in [[category theory]] as a whole. 

For instance a [[natural transformation]] $\eta : F \Rightarrow G$ between two [[functor]]s $F,G : C \to D$ is precisely the same as a strictly [[commuting diagram]]

$$
  \array{
    C \times \{0\}
    \\
    \downarrow & \searrow^{\mathrlap{F}}
    \\ 
    C \times I &\stackrel{\eta}{\to}& D
    \\
    \uparrow & \nearrow_{\mathrlap{G}}
    \\
    C \times \{1\}
  }
$$

in [[Cat]], where on the left we have the [[cartesian product]] of $C$ with $I$. 

Accordingly, for $I_{iso}$ the [[walking isomorphism]], a [[natural isomorphism]] $\eta : F \Rightarrow G$ is the same as a diagram

$$
  \array{
    C \times \{0\}
    \\
    \downarrow & \searrow^{\mathrlap{F}}
    \\ 
    C \times I_{iso} &\stackrel{\eta}{\to}& D
    \\
    \uparrow & \nearrow_{\mathrlap{G}}
    \\
    C \times \{1\}
  }
 \,.
$$

This is a [[left homotopy]] in $Cat$.

Dually, forming the [[functor category]] 

$$
  Arr(D) := [I,D]
$$

from the walking morphism produces the [[arrow category]] of $D$, and a natural transformation $\eta$ is also the same as a diagram

$$
  \array{
     && D \times \{0\}
     \\
     & {}^{\mathllap{F}}\nearrow & \uparrow
     \\
     C &\stackrel{\eta}{\to}& [I,D]
     \\
     & {}_{\mathllap{G}}\searrow & \downarrow
     \\
     && D \times \{1\}
  }
  \,.
$$

With $I$ replaced by $I_{iso}$ this is again a natural isomorphism, now represented as a [[right homotopy]] in [[Cat]].

The analogous statements are true in [[higher category theory]]. 

## Related concepts

[[!include notions of walking structure]]

* [[hom type]], [[bridge type]]

## References

The phrase “walking morphism” appears in:

* {#OR24} [[Viktoriya Ozornova]], [[Martina Rovelli]], *What is an equivalence in a higher category*, Bulletin of the London Mathematical Society, Volume 56, Issue 1, January 2024, Pages 1-58 ([doi:10.1112/blms.12947](https://doi.org/10.1112/blms.12947))

* {#CCNW} [[Denis-Charles Cisinski]], [[Bastiaan Cnossen]], [[Hoang Kim Nguyen]], [[Tashi Walde]], section 1.5 of: *Formalization of Higher Categories*, work in progress ([pdf](https://drive.google.com/file/d/1lKaq7watGGl3xvjqw9qHjm6SDPFJ2-0o/view))

The phrase "directed interval" appears in

* {#RS17} [[Emily Riehl]], [[Mike Shulman]], *A type theory for synthetic ∞-categories*, Higher Structures **1** 1 (2017) &lbrack;[arxiv:1705.07442](https://arxiv.org/abs/1705.07442), [published article](https://higher-structures.math.cas.cz/api/files/issues/Vol1Iss1/RiehlShulman)&rbrack;

* {#GWB24} [[Daniel Gratzer]], [[Jonathan Weinberger]], [[Ulrik Buchholtz]], *Directed univalence in simplicial homotopy type theory* ([arXiv:2407.09146](https://arxiv.org/abs/2407.09146))

* {#GWB25} [[Daniel Gratzer]], [[Jonathan Weinberger]], [[Ulrik Buchholtz]], *The Yoneda embedding in simplicial type theory* ([arXiv:2501.13229](https://arxiv.org/abs/2501.13229))

The phrase "interval" appears in 

* {#SY25} [[Jonathan Sterling]], [[Lingyuan Ye]], *Domains and Classifying Topoi* ([arXiv:2505.13096](https://arxiv.org/abs/2505.13096))

[[!redirects I]]
[[!redirects walking arrow]]
[[!redirects walking morphism]]
[[!redirects walking morphism category]]

[[!redirects interval preorder]]
[[!redirects interval proset]]
[[!redirects interval poset]]

[[!redirects directed interval]]
[[!redirects directed intervals]]

[[!redirects directed interval category]]
[[!redirects directed interval categories]]

[[!redirects directed interval type]]
[[!redirects directed interval types]]