
> This entry is about the notion of spans/correspondences which generalizes that of _[[relations]]_. For spans in [[vector spaces]] or [[modules]], see _[[linear span]]_.


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### Set theory
+-- {: .hide}
[[!include set theory - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}


## Definition 

### In set theory

In [[set theory]], a **span** or **correspondence** between [[sets]] $A$ and $B$ is a set $C$ with a [[function]] $R:C \to A \times B$ to the [[product set]] $A \times B$. A span between a set $A$ and $A$ itself is a [[directed pseudograph]], which is used to define [[categories]] in set theory. 

### In dependent type theory

In [[dependent type theory]], there is a distinction between a *span*, a *multivalued partial function*, and a *correspondence*:

* A **span** between types $A$ and $B$ is a type $C$ with families of elements $x:C \vdash g(x):A$ and $x:C \vdash h(x):B$

* A **[[multivalued partial function]]** from type $A$ to type $B$ is a type family $x:A \vdash P(x)$ with a family of elements $x:A, p:P(x) \vdash f(x, p):B$

* A **correspondence** between types $A$ and $B$ is a type family $x:A, y:B \vdash R(x, y)$. 

However, from any one of the above structures, one could get the other two structures, provided one has [[identity types]] and [[dependent pair types]] in the dependent type theory. Given a type family $x:A \vdash P(x)$, let $z:\sum_{x:A} P(x) \vdash \pi_1(z):A$ and $z:\sum_{x:A} P(x) \vdash \pi_2(z):P(\pi_1(z))$ be the dependent pair projections for the [[dependent pair type]] $\sum_{x:A} P(x)$. 

* From every span one could get a multivalued partial function by defining the type family $x:A \vdash P(x)$ as $P(x) \coloneqq \sum_{y:C} g(y) =_A x$ and the family of elements $x:A, p:P(x) \vdash f(x, p):B$ as $f(x, p) \coloneqq h(\pi_1(x))$. 

* From every multivalued partial function one could get a span by defining the type $C$ as $C \coloneqq \sum_{x:A} P(x)$ and the family of elements $x:C \vdash g(x):A$ as $g(x) \coloneqq \pi_1(x)$. 

* From every multivalued partial function one could get a correspondence by defining the type family $x:A, y:B \vdash R(x, y)$ as $R(x, y) \coloneqq \sum_{p:P(x)} f(x, p) =_B y$. 

* From every correspondence one could get a multivalued partial function by defining the type family $x:A \vdash P(x)$ as $P(x) \coloneqq \sum_{y:B} R(x, y)$, and the family of elements $x:A, p:P(x) \vdash h(x, p):B$ as $h(x, p) \coloneqq \pi_1(p)$

* From every span one could get a correspondence by defining the type family $x:A, y:B \vdash R(x, y)$ as $R(x, y) \coloneqq \sum_{z:C} (g(z) =_A x) \times (h(z) =_B y)$. 

* From every correspondence one could get a span by defining the type $C$ as $C \coloneqq \sum_{x:A} \sum_{y:B} R(x, y)$, the family of elements $z:C \vdash g(z):A$ as $g(z) \coloneqq \pi_1(z)$, and the function $z:C \vdash h(z):B$ as $h(z) \coloneqq \pi_1(\pi_2(z))$ 

Given types $A$, $B$, and $C$ and spans $(D, x:D \vdash g_D(x):A, x:D \vdash h_D(x):B)$ between $A$ and $B$ and $(E, y:E \vdash g_E(y):B, y:E \vdash h_E(y):C)$ between $B$ and $C$, there is a span 
$$(E \circ D, z:E \circ D \vdash g_{E \circ D}(z):A, z:E \circ D \vdash h_{E \circ D}(z):C)$$ 
defined by
$$E \circ D \coloneqq \sum_{x:D} \sum_{y:E} h_D(x) =_B g_E(y)$$
$$z:E \circ D \vdash g_{E \circ D}(z) \coloneqq g_D(\pi_1(z))$$
$$z:E \circ D \vdash h_{E \circ D}(z) \coloneqq h_E(\pi_1(\pi_2(\pi_1(z))(z)))$$

Given types $A$, $B$, and $C$ and correspondences $x:A, y:B \vdash R(x, y)$ and $y:B, z:C \vdash S(y, z)$, there is a correspondence $x:A, z:C \vdash (S \circ R)(x, z)$ defined by 
$$(S \circ R)(x, z) \coloneqq \sum_{y:B} R(x, y) \times S(y, z)$$


### In category theory

In any [[category]] $C$, a __span__, or __roof__, or __correspondence__, from an [[object]] $x$ to an object $y$ is a [[diagram]] of the form

$$
  \array{
     && s
      \\
      & {}^{f}\swarrow
      && \searrow^{g}
     \\
     x
     &&&&
     y
  }
$$

where $s$ is some other object of the category.  (The word "correspondence" is also sometimes used for a [[profunctor]].)

This [[diagram]] is also called a 'span' because it looks like a little bridge; 'roof' is similar.  The term 'correspondence' is prevalent in geometry and related areas; it comes about because a correspondence is a generalisation of a binary [[relation]].  

Note that a span with $f = 1$ is just a morphism from $x$ to $y$, while a span with $g = 1$ is a morphism from $y$ to $x$.  So, a span can be thought of as a generalization of a morphism in which there is no longer any asymmetry between source and target.

A span in the [[opposite category]] $C^op$ is called a [[co-span]] in $C$.  

A span that has a [[cocone]] is called a [[coquadrable span]].

### Categories of spans

If the category $C$ has [[pullback|pullbacks]], we can compose spans.  Namely, given a span from $x$ to $y$ and a span from $y$ to $z$:
$$
  \array{
     && s &&&& t
      \\
      & {}^{f}\swarrow
      && \searrow^{g}
       &
       & {}^{h}\swarrow
      && \searrow^{i}
     \\
     x
     &&&&
     y
     &&&&
     z
  }
$$

we can take a pullback in the middle:

$$
  \array{
     &&&& s \times_y t 
     \\& 
    &&
      {}^{p_s}\swarrow
      && \searrow^{p_t}
    \\
     && s &&&& t
      \\
      & {}^{f}\swarrow
      && \searrow^{g}
       &
       & {}^{h}\swarrow
      && \searrow^{i}
     \\
     x
     &&&&
     y
     &&&&
     z
  }
$$

and obtain a span from $x$ to $z$:

$$
  \array{
     && s \times_y t
      \\
      & {}^{f p_s}\swarrow
      && \searrow^{i p_t}
     \\
     x
     &&&&
     z
  }
$$

This way of composing spans lets us define a [[bicategory]] [[Span]]$(C)$ with:

* objects of $C$ as objects
* spans as morphisms
* maps between spans as 2-morphisms

This is a weak 2-category: it has a nontrivial [[associator]]: composition of spans is not strictly associative, because pullbacks are defined only up to canonical isomorphism.  A [[Lack's coherence theorem|naturally defined]] [[strict 2-category]] which is equivalent to $Span(C)$ is the strict 2-category of [[linear polynomial functors]] between [[slice categories]] of $C$.

(Note that we must choose a specific pullback when defining the composite of a pair of morphisms in $Span(C)$, if we want to obtain a [[bicategory]] as traditionally defined; this requires the [[axiom of choice]]. Otherwise we obtain a bicategory with 'composites of morphisms defined only up to canonical iso-2-morphism'; such a structure can be modeled by an [[anabicategory]] or an [[opetopic bicategory]].)

We can also obtain a [[pseudo-double category]], whose [[loose]] structure is as above, whose [[tight]] morphisms are functions, and whose cells are commuting diagrams,

\begin{tikzcd}
	A & S & B \\
	{A'} & {S'} & {B'}
	\arrow["p", from=1-1, to=2-1]
	\arrow["f"', from=1-2, to=1-1]
	\arrow["g", from=1-2, to=1-3]
	\arrow["q", from=1-2, to=2-2]
	\arrow["r", from=1-3, to=2-3]
	\arrow["h", from=2-2, to=2-1]
	\arrow["i"', from=2-2, to=2-3]
\end{tikzcd}

Moreover, when $C$ is an arbitrary category, not necessarily having pullbacks, one can still obtain a [[covirtual double category]]. More details can be found in Section 4 of [Dawson, Paré, Pronk](#DawsonParePronk10) (where the term oplax double category is used).

## Properties

### The 1-category of spans

Let $C$ be a category with [[pullback]]s and let $Span_1(C) := (Span(C))_{\sim 1}$ be the 1-category of objects of $C$ and isomorphism classes of spans between them as morphisms.

Then

* $Span_1(C)$ is a [[dagger category]].

Next assume that $C$ is a [[cartesian monoidal category]]. Then clearly $Span_1(C)$ naturally becomes a [[monoidal category]] itself, but more: then

* $Span_1(C)$ is a [[dagger compact category]].


### Universal property of the bicategory of spans
 {#UniversalPropertyOfTheBicategoryOfSpans}

We discuss the [[universal property]] that characterizes 2-categories of spans. 

For $C$ be a [[category]] with [[pullbacks]], write 

1. $Span_2(C) \coloneqq (Span(C))_{\sim2}$ for the [[weak 2-category]] of objects of $C$, spans as morphisms, and maps between spans as 2-morphisms, 

1. $\eta_C: C \rightarrow Span_2(C)$ for the functor given by:

\begin{centre}
\begin{tikzcd}
  & & & & 
  x 
  \arrow[ld, "1_x"{above}] 
  \arrow[rd, "f"] 
  & 
  \\
  x 
  \arrow[r, "f"] 
  & 
  y 
  & 
  \mapsto 
  & 
  x 
  & & 
  y
\end{tikzcd}
\end{centre}

Now let

1. $K$ be any [[bicategory]]

1. $F, G \,\colon\, C \rightarrow K$ be [[functors]] such that every map in $C$ is sent to a map in $K$ possessing a [[right adjoint]] and satisfying the [[Beck-Chevalley Condition]] for any [[commutative square]] in $K$, 

1. $\alpha \,\colon\, F \rightarrow G$ be a [[natural transformation]].

Then: 

\begin{proposition}
**(universal property of the bicategory of spans)**
\linebreak
The following holds:

1. $\eta_C$ is [[universal]] among such functors $F$, i.e. $F$ as above factors as $F = \hat{F} \circ \eta_C$ for a functor $\hat{F} \,\colon\, Span_2(C) \rightarrow K$ which is unique up to isomorphism.

1. There exists a unique [[lax natural transformation]]: $\hat{\alpha} \,\colon\, \hat{F} \rightarrow \hat{G}$ such that $\hat{\alpha} \eta_C = \alpha$. 

1. Let $x, y$ be objects in $C$ and $f: x \rightarrow y$ be a morphism in $C$. If $(\alpha_x, \alpha_y)$ induce a pseudo-map of adjoints $F(f) \dashv (Ff)^* \rightarrow G(f) \dashv (Gf)^*$, then $\hat{\alpha}$ is a [[pseudonatural transformation]]

Furthermore, if we denote $Pbk$ as the [[2-category]] of categories with pullbacks, [[pullback]]-preserving [[functor]]s, and [[equifibered natural transformation]]s and $BiCat$ as the [[tricategory]] of [[bicategories]], $Span(-): Pbk \rightarrow BiCat$ is well-defined as a functor. 
\end{proposition}
This is due to [Hermida 1999](#Hermida99).


### Limits and colimits
 {#LimitsAndColimits}

Since a category of spans/correspondences $Corr(\mathcal{C})$ is evidently [[equivalence of categories|equivalent]] to its [[opposite category]], it follows that to the extent that [[limits]] exists they are also [[colimits]] and vice versa.

If the underlying category $\mathcal{C}$ is an [[extensive category]], then the [[coproduct]]/[[product]] in $Corr(\mathcal{C})$ is given by the [[disjoint union]] in $\mathcal{C}$. (See also [this](http://mathoverflow.net/questions/32526/what-is-the-product-in-the-2-category-of-spans) MO discussion).

More generally, every [[van Kampen colimit]] in $\mathcal{C}$ is a (co)limit in $Corr(\mathcal{C})$ &#8212; and conversely, this property characterizes van Kampen colimits. ([Sobocinski-Heindel 11](SobocinskiHeindel11)).

### Relation to relations
 {#RelationToRelations}

Correspondences may be seen as generalizations of [[relations]]. A relation is a [[correspondence]] which is [[(-1)-truncated]] as a [[morphism]] into the [[cartesian product]]. See at _[[relation]]_ and at _[[Rel]]_ for more on this.

### Closure

When $E$ is a [[locally cartesian closed category]], $Span(E)$ is a [[closed bicategory]]: see there for details.

## Examples

* Spans in [[FinSet]] behave like the [[categorification]] of  [[matrices]] with entries in the [[natural number]]s: for $X_1 \leftarrow N \to X_2$ a span of finite sets, the [[cardinality]] of the [[fiber]] $X_{x_1, x_2}$ over any two elements $x_1 \in X_1$ and $x_2 \in X_2$ plays the role of the corresponding matrix entry. Under this identification composition of spans indeed corresponds to matrix multiplication. This implies that the category of spans of finite sets is equivalent to the [[Lawvere theory]] of commutative monoids, that is, to the [[PROP]] for the free bicommutative [[bialgebra]].  Spans over finite sets is a [[rig category]] with respect to the tensor products induced by the coproduct and product in FinSet.  The coproduct in FinSet remains the coproduct, but the product becomes the bilinear [[tensor product of modules]].


* The [[Burnside category]] is essentially the category of correspondences in [[G-sets]] for $G$ a [[finite group]].

* A [[cobordism]] $\Sigma$ from $\Sigma_{in}$ to $\Sigma_{out}$ is an example of a cospan $\Sigma_{in} \to \Sigma \leftarrow \Sigma_{out}$ in the category of [[smooth manifold]]s. However, composition of cobordisms is not quite the pushout-composition of these cospans: to make the composition be a [[smooth manifold]] again some extra technical aspects must be added ("[[collars]]").

* In [[prequantum field theory]] (see there for details), spans of [[stacks]] model [[trajectories]] of [[field (physics)|fields]].

* The [[category of Chow motives]] has as [[morphisms]] [[equivalence classes]] of [[linear combinations]] of spans of [[smooth variety|smooth]] [[projective varieties]].

* The [[Weinstein symplectic category]] has as morphisms [[Lagrangian correspondences]] between [[symplectic manifolds]]. 

  More generally [[symplectic dual pairs]] are correspondences between [[Poisson manifolds]].

* Cospans of homomorphisms of [[C*-algebras]] represent morphisms in [[KK-theory]] (by Cuntz' result).

* Correspondences of [[flag manifolds]] play a role as [[twistor correspondences]], see at _[Schubert calculus -- Correspondences](Schubert+calculus#Correspondences)_ and at _[[horocycle correspondence]]_

* The [[Fourier-Mukai transform]] is a pull-push operation through correspondences equipped with objects in a cocycle given by an object in a [[derived category of quasi-coherent sheaves]].

* [[Hecke correspondence]]

* A [[hypergraph]] is a span from a set of vertices to a set of (hyper)edges.

## Related concepts

* [[(∞,n)-category of spans]].

* [[sink]], [[cosink]]

* [[product]], [[coproduct]]

* [[multispan]]

* [[correspondence type]]

* [[reflexive graph]]

A category of correspondences is a refinement of a category [[Rel]] of relations. See there for more.

## References ##

The terminology "span" appears on page 533 of:

* [[Nobuo Yoneda]], *On ext and exact sequences* (PhD thesis), Journal of the Faculty of Science, Section I. **8** University of Tokyo (1960) 507–576 &lbrack;[pdf](http://alpha.math.uga.edu/~lorenz/YonedaExtExactSequences.pdf), [CiNii:naid/500000325773](https://ci.nii.ac.jp/naid/500000325773)&rbrack;

The $Span(C)$ construction was introduced by Jean B&#233;nabou (as an example of a bicategory) in

* [[Jean Bénabou]], Introduction to Bicategories, _Lecture Notes in Mathematics 47_, Springer (1967), pp.1-77. ([doi](http://dx.doi.org/10.1007/BFb0074299))

B&#233;nabou cites an article by Yoneda (1954) for introducing the concept of span (in the category of categories).

An exposition discussing the role of spans in [[quantum theory]]:

* [[John Baez]], _Spans in quantum Theory_ ([web](http://math.ucr.edu/home/baez/span/), [pdf](http://math.ucr.edu/home/baez/span/span.pdf), [blog](http://golem.ph.utexas.edu/category/2007/10/spans_in_quantum_theory.html))

The relationship between spans and [[bimodules]] is briefly discussed in

* [[John Baez]], _Bimodules versus spans_ ([blog](http://golem.ph.utexas.edu/category/2008/08/bimodules_versus_spans.html))

The relation to [[van Kampen colimits]] is discussed in 

* {#SobocinskiHeindel11} [[Pawel Sobocinski]], Tobias Heindel, _Being Van Kampen is a universal property_, ([arXiv:1101.4594](http://arxiv.org/abs/1101.4594))
 

The [[universal property]] of categories of spans is due to

* {#Hermida99} [[Claudio Hermida]], _Representable Multicategories_, Advances in Mathematics, __151__ (2000), No. 2, 164-225, ([doi:10.1006/aima.1999.1877](https://doi.org/10.1006/aima.1999.1877))

and further discussed in:

* {#DawsonParePronk04} R. Dawson, [[Robert Paré]], [[Dorette Pronk]], _Universal properties of Span_, Theory and Appl. of Categories __13__, 2004, No. 4, 61-85, [TAC](http://www.tac.mta.ca/tac/volumes/13/4/13-04abs.html), [MR2005m:18002](http://www.ams.org/mathscinet-getitem?mr=2116323)
  

*  {#DawsonParePronk10} R. Dawson, [[Robert Paré]], [[Dorette Pronk]], _The span construction_, Theory Appl. Categ. __24__ (2010), No. 13, 302&#8211;377, [TAC](http://www.tac.mta.ca/tac/volumes/24/13/24-13abs.html) [MR2720187](http://www.ams.org/mathscinet-getitem?mr=2720187)

* [[Charles Walker]], _Universal properties of bicategories of polynomials_, Journal of Pure and Applied Algebra 223.9 (2019): 3722-3777.

* [[Charles Walker]], _Bicategories of spans as generic bicategories_, [arXiv:2002.10334](https://arxiv.org/abs/2002.10334) (2020).

See also Theorem 5.2.1 and 5.3.7 of:

* Paul Balmer, and Ivo Dell'Ambrogio. _Mackey 2-functors and Mackey 2-motives_. [arXiv:1808.04902](https://arxiv.org/abs/1808.04902) (2018).

The structure of a [[k-tuply monoidal (n,r)-category|monoidal]] [[tricategory]] on spans in [[2-categories]] is discussed in  

* {#Hoffnung} [[Alex Hoffnung]], _Spans in 2-Categories: A monoidal tricategory_ ([arXiv:1112.0560](http://arxiv.org/abs/1112.0560))
 

Generally, an [[(∞,n)-category of spans]] is indicated in section 3.2 of

* {#Lurie} [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_
 

[[!redirects spans]]

[[!redirects category of spans]]
[[!redirects categories of spans]]
[[!redirects bicategory of spans]]

[[!redirects correspondence]]
[[!redirects correspondences]]

[[!redirects category of correspondences]]
[[!redirects categories of correspondences]]

[[!redirects correspondence space]]
[[!redirects correspondence spaces]]
