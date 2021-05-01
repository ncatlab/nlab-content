
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

Regard $X \in C$ under the [[Yoneda embedding]] as an object $X \in [C^{op}, sSet]_{proj,loc}$. Then a morphism $(Y  \to X) \in [C^{op}, sSet]$ is a **split hypercover** of $X$ if

1. $Y$ is a [[hypercover]] in that

   1. $Y$ is degreewise a [[coproduct]] of [[representable functor|representables]],

      $Y = \int^{[n] \in \Delta} \Delta[n] \cdot \coprod_{i_n} U_{i_n} \;\,,
    \;\;\; with \{U_{i_n} \in C\}$ ;

   1. with $Y \to X$ regarded as a presheaf of [[augmented simplicial set]]s, for all $n \in \mathbb{N}$ the morphism $Y_{n+1} \to (\mathbf{cosk}_n Y)_{n+1}$ into the $n+1$-cells of the $n$-[[coskeleton]] is a [[local epimorphism]] with respect to the given [[Grothendieck topology]] on $C$

1. $Y$ is _split_ in that the image of the degeneracy maps identifies with a direct summand in each degree.


## Properties

The splitness condition on the hypercover is precisely such that $Y$ becomes a cofibrant object in $[C^{op}, sSet]_{proj,loc}$, according to the characterization of such cofibrant objects described <a href="http://ncatlab.org/nlab/show/model+structure+on+simplicial+presheaves#CofibrantObjects">here</a>.

## Examples

Over the site [[CartSp]], the [[Cech nerve]] of an [[open cover]] becomes split as a height-0 hypercover precisely if the cover is a [[good open cover]].

## References

* [[Dan Dugger]], [[Sharon Hollander]], [[Dan Isaksen]], _Hypercovers and simplicial presheaves_ ([arXiv:math.AT/0205027](https://arxiv.org/abs/math/0205027))


[[!redirects split hypercovers]]