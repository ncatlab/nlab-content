#Content#
* automatic table of contents goes here
{:toc}

## Definition ##

In any [[category]] $C$, a __span__, __roof__, or __correspondence__, from an [[object]] $x$ to an object $y$ is a [[diagram]]
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

This [[diagram]] is called a 'span' because it looks like a little bridge; 'roof' is similar.  The term 'correspondence' is prevalent in geometry and related areas; it comes about because a correspondence is a generalisation of a binary [[relation]].  Discussion of this terminology on the blog is [here](http://golem.ph.utexas.edu/category/2009/05/nlab_more_general_discussion.html#c023768).

Note that a span with $f = 1$ is just a morphism from $x$ to $y$, while a span with $g = 1$ is a morphism from $y$ to $x$.  So, a span can be thought of as a generalization of a morphism in which there is no longer any asymmetry between source and target.

A span in $C^op$ is called a [[co-span]] in $C$.  A [[cobordism]] is an example of a cospan in the category of smooth manifolds, and this nicely illustrates the symmetry between source and target.

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

This is a weak 2-category has a nontrivial [[associator]]: composition of spans is not strictly associative, because pullbacks are defined only up to canonical isomorphism.  A [[Lack's coherence theorem|naturally defined]] [[strict 2-category]] which is equivalent to $Span(C)$ is the strict 2-category of [[linear polynomial functors]] between [[slice categories]] of $C$.

(Note that we must choose a specific pullback when defining the composite of a pair of morphisms in $Span(C)$, if we want to obtain a [[bicategory]] as traditionally defined; this requires the [[axiom of choice]]. Otherwise we obtain a bicategory with 'composites of morphisms defined only up to canonical iso-2-morphism'; such a structure can be modeled by an [[anabicategory]] or an [[opetopic bicategory]].)

A span that has a [[cocone]] is called a [[coquadrable span]].

## Some facts about spans ##

Let $C$ be a category with pullbacks and let $Span_1(C) := (Span(C))_{\sim 1}$ be the 1-category of objects of $C$ and isomorphism class of spans between them as morphisms.

Then

* $Span_1(C)$ is a [[dagger category]].

Next assume that $C$ is a [[cartesian monoidal category]]. Then clearly $Span_1(C)$ naturally becomes a [[monoidal category]] itself, but more: then

* $Span_1(C)$ is a [[dagger compact category]].


## Generalizations ##

 See [[multispan]].

## References ##

The above list of facts about spans is described in

* [[John Baez]], _Spans in quantum Theory_ ([web](http://math.ucr.edu/home/baez/span/), [pdf](http://math.ucr.edu/home/baez/span/span.pdf), [blog](http://golem.ph.utexas.edu/category/2007/10/spans_in_quantum_theory.html))

which discusses how spans naturally capture crucial aspects of [[quantum field theory]].

[[!redirects spans]]
[[!redirects correspondence]]
[[!redirects correspondences]]
