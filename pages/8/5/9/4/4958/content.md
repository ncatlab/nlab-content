


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The analog in the context of [[(∞,1)-topos]] theory of a [[local geometric morphism]] in [[topos theory]].

## Definition


A **local geometric morphism** $f : E \to S$ between [[(∞,1)-topos]]es $\mathbf{H},\mathbf{S}$ is 

* a [[geometric morphism]]

  $$
    (f^* \dashv f_*) 
     : 
      \mathbf{H} \stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}
    {\to}}  \mathbf{S}
  $$

* such that a further [[left adjoint]] $f_! : \mathbf{H} \to \mathbf{S}$ exists (making $f$ an [[essential geometric morphism]]) _and_ a further [[right adjoint]] $f^! : \mathbf{S} \to \mathbf{H}$ 

  $$
    (f_! \dashv f^* \dashv f_* \dashv f^!) : 
    \mathbf{H}
    \stackrel{\stackrel{\overset{f_!}{\to}}{\overset{f^*}{\leftarrow}}}{\stackrel{\underset{f_*}{\to}}{\underset{f^!}{\leftarrow}}}
    \mathbf{S}
  $$

* and such that $f^!$ is a [[full and faithful functor]], so that hence

  $$
    \mathbf{S} \stackrel{\overset{f_*}{\leftarrow}}{\underset{f^!}{\hookrightarrow}} \mathbf{H}
  $$

  is a [[geometric embedding]] of $\mathbf{S}$ into $\mathbf{H}$.

If $f : \mathbf{H} \to \mathbf{S}$ is the [[global section]] geometric morphism in the category of $(\infty,1)$toposes over $\mathbf{S}$, then we say that $\mathbf{H}$ is a **local $(\infty,1)$-topos**.

## Properties

Every local topos is a [[locally ∞-connected (∞,1)-topos]].

## Examples

### $(\infty,1)$Sheaves on $CartSp$

Let $\mathbf{H} = (\infty,1)Sh(CartSp)$ be the [[gros topos]] of [[(∞,1)-sheaves]] on the [[site]] [[CartSp]] of [[Cartesian space]]s with the [[good open cover]] [[coverage]]. This is the topos [[?LieGrpd]] of [[∞-Lie groupoid]]s.

This is a local $(\infty,1)$-topos.

That it is a [[connected topos]] is discussed [[?LieGrpd]].

## References

* [[Bill Lawvere]], _Axiomatic cohesion_ Theory and Applications of Categories, Vol. 19, No. 3, 2007, pp. 41&#8211;49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))



[[!redirects local (∞,1)-geometric morphisms]]
[[!redirects local (∞,1)-topos]]
