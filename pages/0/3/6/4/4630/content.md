
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _split hypercover_ is a cofibrant [[resolution]] of a [[representable functor|representable]] in the _projective_ [[local model structure on simplicial presheaves]] $[C^{op}, sSet]_{proj,loc}$ over a [[site]] $C$.

It is a [[hypercover]] satisfying an extra condition that roughly says that it is degreewise freely given by representables.

## Definition

Regard $U \in C$ under the [[Yoneda embedding]] as an object $U \in [C^{op}, sSet]_{proj,loc}$. Then a morphism $(Y  \to X) \in [C^{op}, sSet]$ is a **split hypercover** of $X$ if

1. the morphism is an acylic fibration in $[C^{op}, sSet]_{proj,loc}$;

   (this makes $Y \to X$ a [[hypercover]]);

1. $Y$ is degreewise a [[coproduct]] of [[representable functor|representables]],

   $Y = \int^{[n] \in \Delta} \Delta[n] \cdot \coprod_{i_n} U_{i_n}$;

1. the image of the degeneracy maps identifies with a direct summand in each degree

   (this makes the hypercover be _split_ ).

## Properties

The splitness condition on the hypercover is precisely such that $Y$ becomes a cofibrant object in $[C^{op}, sSet]_{proj,loc}$, according to the characterization of such cofibrant objects described <a href="http://ncatlab.org/nlab/show/model+structure+on+simplicial+presheaves#CofibrantObjects">here</a>.

## Exmaples

Over the site [[CartSp]], the [[Cech nerve]] of an [[open cover]] becomes split as a height-0 hypercover precisely if the cover is a [[good open cover]].

## References

* [[Dan Dugger]], [[Sharon Hollander]], [[Dan Isaksen]], _Hypercovers and simplicial presheaves_ ([arXiv:math.AT/0205027](http://front.math.ucdavis.edu/0205.5027))


[[!redirects split hypercovers]]