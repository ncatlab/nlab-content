# Definition #

In any [[category]] $C$, a **span** from an [[object]] $x$ to an object $y$ is a [[diagram]]

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

where $s$ is some other object of the category.  This diagram is called a 'span' because it looks like a little bridge.

Note that a span with $f = 1$ is just a morphism from $x$ to $y$, while a span with $g = 1$ is a morphism from $y$ to $x$.  So, a span can be thought of as a generalization of a morphism in which there is no longer any asymmetry between source and target.

A span in $C^op$ is called a _cospan_ in $C$.  A [[cobordism]] is an example of a cospan in the category of smooth manifolds, and this nicely illustrates the symmetry between source and target.

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
     &&&& s t 
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
     && s t
      \\
      & {}^{f p_s}\swarrow
      && \searrow^{i p_t}
     \\
     x
     &&&&
     z
  }
$$

This way of composing spans lets us define a [[bicategory]] $Span(C)$ with:

* objects of $C$ as objects
* spans as morphisms
* maps between spans as 2-morphisms

This bicategory has a nontrivial [[associator]]: composition of spans is not strictly associative, because pullbacks are defined only up to canonical isomorphism.  

(Note that we must choose a specific pullback when defining the composite of a pair of morphisms in $Span(C)$, if we want to obtain a bicategory as traditionally defined.  Otherwise we obtain a bicategory with 'composites of morphisms defined only up to canonical iso-2-morphism', sometimes called an [[ana-bicategory]] or [[opetopic bicategory]].)