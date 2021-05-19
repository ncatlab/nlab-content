
> This entry is about the notion of spans/correspondences which generalizes that of _[[relations]]_. For spans in [[vector spaces]] or [[modules]], see _[[linear span]]_.


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
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

### Correspondences

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

This way of composing spans lets us define a [[2-category]] [[Span]]$(C)$ with:

* objects of $C$ as objects
* spans as morphisms
* maps between spans as 2-morphisms

This is a weak 2-category: it has a nontrivial [[associator]]: composition of spans is not strictly associative, because pullbacks are defined only up to canonical isomorphism.  A [[Lack's coherence theorem|naturally defined]] [[strict 2-category]] which is equivalent to $Span(C)$ is the strict 2-category of [[linear polynomial functors]] between [[slice categories]] of $C$.

(Note that we must choose a specific pullback when defining the composite of a pair of morphisms in $Span(C)$, if we want to obtain a [[bicategory]] as traditionally defined; this requires the [[axiom of choice]]. Otherwise we obtain a bicategory with 'composites of morphisms defined only up to canonical iso-2-morphism'; such a structure can be modeled by an [[anabicategory]] or an [[opetopic bicategory]].)

By including functions as well, instead of a 2-category we obtain a [[double category]].


## Properties

### The 1-category of spans

Let $C$ be a category with [[pullback]]s and let $Span_1(C) := (Span(C))_{\sim 1}$ be the 1-category of objects of $C$ and isomorphism class of spans between them as morphisms.

Then

* $Span_1(C)$ is a [[dagger category]].

Next assume that $C$ is a [[cartesian monoidal category]]. Then clearly $Span_1(C)$ naturally becomes a [[monoidal category]] itself, but more: then

* $Span_1(C)$ is a [[dagger compact category]].

### Universal property of the 2-category of spans

([Dawson-Par&#233;-Pronk 04](#DawsonParePronk04)) (...)


### Limits and colimits
 {#LimitsAndColimits}

Since a category of spans/correspondences $Corr(\mathcal{C})$ is evidently [[equivalence of categories|equivalent]] to its [[opposite category]], it follows that to the extent that [[limits]] exists they are also [[colimits]] and vice versa.

If the underlying category $\mathcal{C}$ is an [[extensive category]], then the [[coproduct]]/[[product]] in $Corr(\mathcal{C})$ is given by the [[disjoint union]] in $\mathcal{C}$. (See also [this](http://mathoverflow.net/questions/32526/what-is-the-product-in-the-2-category-of-spans) MO discussion).

More generally, every [[van Kampen colimit]] in $\mathcal{C}$ is a (co)limit in $Corr(\mathcal{C})$ &#8212; and conversely, this property characterizes van Kampen colimits. ([Sobocinski-Heindel 11](SobocinskiHeindel11)).

### Relation to relations
 {#RelationToRelations}

Correspondences may be seen as generalizations of [[relations]]. A relation is a [[correspondence]] which is [[(-1)-truncated]] as a [[morphism]] into the [[cartesian product]]. See at _[[relation]]_ and at _[[Rel]]_ for more on this.

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

* [[sink]]

* [[multispan]]

A category of correspondences is a refinement of a category [[Rel]] of relations. See there for more.

## References ##

The $Span(C)$ construction was introduced by Jean B&#233;nabou (as an example of a bicategory) in

* [[Jean Bénabou]], Introduction to Bicategories, _Lecture Notes in Mathematics 47_, Springer (1967), pp.1-77. ([doi](http://dx.doi.org/10.1007/BFb0074299))

B&#233;nabou cites an article by Yoneda (1954) for introducing the concept of span (in the category of categories).

An exposition discussing the role of spans in [[quantum theory]]:

* [[John Baez]], _Spans in quantum Theory_ ([web](http://math.ucr.edu/home/baez/span/), [pdf](http://math.ucr.edu/home/baez/span/span.pdf), [blog](http://golem.ph.utexas.edu/category/2007/10/spans_in_quantum_theory.html))

The relationship between spans and [[bimodules]] is briefly discussed in

* [[John Baez]], _Bimodules versus spans_ ([blog](http://golem.ph.utexas.edu/category/2008/08/bimodules_versus_spans.html))

The relation to [[van Kampen colimits]] is discussed in 

* {#SobocinskiHeindel11} [[Pawel Sobocinski]], Tobias Heindel, _Being Van Kampen is a universal property_, ([arXiv:1101.4594](http://arxiv.org/abs/1101.4594))
 

The [[universal property]] of categories of spans is discussed in 

* {#DawsonParePronk04} R. Dawson, [[Robert Paré]], [[Dorette Pronk]], _Universal properties of Span_, Theory and Appl. of Categories __13__, 2004, No. 4, 61-85, [TAC](http://www.tac.mta.ca/tac/volumes/13/4/13-04abs.html), [MR2005m:18002](http://www.ams.org/mathscinet-getitem?mr=2116323)
  


*  {#DawsonParePronk10} R. Dawson, [[Robert Paré]], [[Dorette Pronk]], _The span construction_, Theory Appl. Categ. __24__ (2010), No. 13, 302&#8211;377, [TAC](http://www.tac.mta.ca/tac/volumes/24/13/24-13abs.html) [MR2720187](http://www.ams.org/mathscinet-getitem?mr=2720187)
 

The structure of a [[k-tuply monoidal (n,r)-category|monoidal]] [[tricategory]] on spans in [[2-categories]] is discussed in  

* {#Hoffnung} [[Alex Hoffnung]], _Spans in 2-Categories: A monoidal tricategory_ ([arXiv:1112.0560](http://arxiv.org/abs/1112.0560))
 

Generally, an [[(∞,n)-category of spans]] is indicated in section 3.2 of

* {#Lurie} [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_
 

[[!redirects spans]]

[[!redirects correspondence]]
[[!redirects correspondences]]

[[!redirects category of spans]]
[[!redirects categories of spans]]

[[!redirects category of correspondences]]
[[!redirects categories of correspondences]]

[[!redirects correspondence space]]
[[!redirects correspondence spaces]]
