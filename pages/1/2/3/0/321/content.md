
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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

## Disambiguation

For spans in [[vector spaces]] (or [[modules]]), see [[linear span]].


## Definition 

### Spans

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

This [[diagram]] is called a 'span' because it looks like a little bridge; 'roof' is similar.  The term 'correspondence' is prevalent in geometry and related areas; it comes about because a correspondence is a generalisation of a binary [[relation]].  

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

This way of composing spans lets us define a [[2-category]] $Span(C)$ with:

* objects of $C$ as objects
* spans as morphisms
* maps between spans as 2-morphisms

This is a weak 2-category: it has a nontrivial [[associator]]: composition of spans is not strictly associative, because pullbacks are defined only up to canonical isomorphism.  A [[Lack's coherence theorem|naturally defined]] [[strict 2-category]] which is equivalent to $Span(C)$ is the strict 2-category of [[linear polynomial functors]] between [[slice categories]] of $C$.

(Note that we must choose a specific pullback when defining the composite of a pair of morphisms in $Span(C)$, if we want to obtain a [[bicategory]] as traditionally defined; this requires the [[axiom of choice]]. Otherwise we obtain a bicategory with 'composites of morphisms defined only up to canonical iso-2-morphism'; such a structure can be modeled by an [[anabicategory]] or an [[opetopic bicategory]].)


## Properties

### The 1-category of spans

Let $C$ be a category with [[pullback]]s and let $Span_1(C) := (Span(C))_{\sim 1}$ be the 1-category of objects of $C$ and isomorphism class of spans between them as morphisms.

Then

* $Span_1(C)$ is a [[dagger category]].

Next assume that $C$ is a [[cartesian monoidal category]]. Then clearly $Span_1(C)$ naturally becomes a [[monoidal category]] itself, but more: then

* $Span_1(C)$ is a [[dagger compact category]].

### Universal property of the 2-category of spans




## Examples

* Spans in [[FinSet]] behave like the [[categorification]] of  [[matrices]] with entries in the [[natural number]]s: for $X_1 \leftarrow N \to X_2$ a span of finite sets, the [[cardinality]] of the [[fiber]] $X_{x_1, x_2}$ over any two elements $x_1 \in X_2$ and $x_2 \in X_2$ plays the role of the corresponding matrix entry. Under this identification composition of spaces indeed corresponds to matrix multiplication.

* A [[cobordism]] $\Sigma$ from $\Sigma_{in}$ to $\Sigma_{out}$ is an example of a cospan $\Sigma_{in} \to \Sigma \leftarrow \Sigma_{out}$ in the category of [[smooth manifold]]s. However, composition of cobordisms is not quite the pushpout-compisition of these cospans: to make the composition be a [[smooth manifold]] again some extra technical aspects must be added ("collars").


## Related concepts

* [[(∞,n)-category of spans]].

* [[multispan]].

## References ##

An exposition discussing the role of spans in [[quantum field theory]]:

* [[John Baez]], _Spans in quantum Theory_ ([web](http://math.ucr.edu/home/baez/span/), [pdf](http://math.ucr.edu/home/baez/span/span.pdf), [blog](http://golem.ph.utexas.edu/category/2007/10/spans_in_quantum_theory.html))

The [[universal property]] of categories of spans is discussed in 

* R. Dawson, R. Par&#233;, [[Dorette Pronk]], _Universal properties of Span_, Theory and Appl. of Categories __13__, 2004, No. 4, 61-85, [TAC](http://www.tac.mta.ca/tac/volumes/13/4/13-04abs.html), [MR2005m:18002](http://www.ams.org/mathscinet-getitem?mr=2116323), _The span construction_, Theory Appl. Categ. __24__ (2010), No. 13, 302&#8211;377, [MR2720187](http://www.ams.org/mathscinet-getitem?mr=2720187)

The structure of a [[k-tuply monoidal (n,r)-category|monoidal]] [[tricategory]] on spans in [[2-categories]] is discussed in  

* [[Alex Hoffnung]], _Spans in 2-Categories: A monoidal tricategory_ ([arXiv:1112.0560](http://arxiv.org/abs/1112.0560))
 {#Hoffnung}

Generally, an [[(∞,n)-category of spans]] is indicated in section 3.2 of

in section 3.2 of 

* [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_
 {#Lurie}

[[!redirects spans]]
[[!redirects correspondence]]
[[!redirects correspondences]]

[[!redirects category of spans]]
[[!redirects categories of spans]]