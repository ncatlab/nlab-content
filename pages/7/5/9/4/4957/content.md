

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A **local geometric morphism** $f : E \to S$ between [[topos]]es $E,S$ is 

* a [[geometric morphism]]

  $$
    (f^* \dashv f_*) : E \stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}
    {\to}}  S
  $$

* such that a further [[left adjoint]] $f_! : E \to S$ exists (making $f$ an [[essential geometric morphism]]) _and_ a further [[right adjoint]] $f^! : S \to E$ 

  $$
    (f_! \dashv f^* \dashv f_* \dashv f^!) : 
    E
    \stackrel{\stackrel{\overset{f_!}{\to}}{\overset{f^*}{\leftarrow}}}{\stackrel{\underset{f_*}{\to}}{\underset{f^!}{\leftarrow}}}
    S
  $$

* and such that $f^!$ is a [[full and faithful functor]], so that hence

  $$
    S \stackrel{\overset{f_*}{\leftarrow}}{\underset{f^!}{\hookrightarrow}} E
  $$

  is a [[geometric embedding]] of $S$ into $E$.

If $f : E \to S$ is the [[global section]] geometric morphism in the category of toposes over $S$, then we say that $E$ is a **local topos**.

## Properties

Every local topos is a [[locally connected topos]].

## Examples

### Sheaves on $CartSp$

Let $E = Sh(CartSp)$ be the [[gros topos]] of [[sheaves]] on the [[site]] [[CartSp]] of [[Cartesian space]]s with the [[good open cover]] [[coverage]]. This is a local topos.

That it is a [[connected topos]] is discussed <a href="http://ncatlab.org/nlab/show/diffeological%20space#Connectedness">here</a>. 

The further right adjoint
is 

$$
  Codisc : Set \to Sh(CartSp)
$$

the functor that sends a set to the [[diffeological space]] on that set with _codiscrete_ smooth structure (every map of sets is smooth). 

(Thanks to [[David Carchedi]].)

## In higher category theory

See [[(∞,1)-local geometric morphism]].

## References

* [[Bill Lawvere]], _Axiomatic cohesion_ Theory and Applications of Categories, Vol. 19, No. 3, 2007, pp. 41&#8211;49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))


[[!redirects local geometric morphisms]]