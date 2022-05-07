
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of _inner fibration_ of [[simplicial set]]s is one of the notion of [[fibrations of quasi-categories]].

When the notion of [[(∞,1)-category]] is incarnated in terms of the notion of [[quasi-category]], an _inner fibration_ is a morphism of [[simplicial set]]s $C \to D$ such that each fiber is a quasi-category and such that over each morphism $f : d_1 \to d_2$ of $D$, $C$ may be thought of as the [[cograph of a profunctor|cograph of an (∞,1)-profunctor]] $C_{d_1} &#8696; C_{d_2}$.

So when $D = {*}$ is the point, an inner fibration $C \to {*}$ is precisely a [[quasi-category]] $C$.

And when $D = N(\Delta[1])$ is the [[nerve]] of the [[interval category]], an inner fibration $C \to \Delta[1]$ may be thought of as the [[cograph of a profunctor|cograph of an (∞,1)-profunctor]] $C &#8696; D$.

This $(\infty,1)$-profunctor comes from an ordinary [[(∞,1)-functor]] $F : C \to D$ precisely if the inner fibration $K \to \Delta[1]$ is even a [[coCartesian fibration]]. And it comes from a functor $G : D \to C$ precisely if the fibration is even a [[Cartesian fibration]]. This is the content of the [[(∞,1)-Grothendieck construction]].

And precisely if the inner fibration/cograph of an $(\infty,1)$-profunctor $K  \to \Delta[1] $ is both a Cartesian as well as a coCartesian fibration does it exhibit a pair of [[adjoint (∞,1)-functor]]s.

## Definition

A [[morphism]] of [[simplicial set]]s $F : X \to Y$ is an **inner fibration** or **[[inner Kan fibration]]** if its has the [[right lifting property]] with respect to all inner [[horn]] inclusions, i.e. if for all [[commuting diagram]]s

$$
  \array{
    \Lambda[n]_i &\to& X
    \\
    \downarrow && \downarrow^{\mathrlap{F}}
    \\
    \Delta[n] &\to& Y
  }
$$

for $0 \lt i \lt n$ there exists a lift

$$
  \array{
    \Lambda[n]_i &\to& X
    \\
    \downarrow &\nearrow& \downarrow^{\mathrlap{F}}
    \\
    \Delta[n] &\to& Y
  }
  \,.
$$


The morphisms with the [[left lifting property]] against all inner fibrations are called **inner anodyne**.




## Properties

### General properties

+-- {: .un_remark}
###### Remark

By the [[small object argument]] we have that every morphism $f : X \to Y$ of simplicial sets may be factored as

$$
  f : X \to Z \to Y
$$

with $X \to Z$ a left/right/inner anodyne cofibration and $Z \to Y$ accordingly a left/right/inner Kan fibration.


=--


## Related concepts

* [[Kan fibration]], [[anodyne morphism]]

* [[right/left Kan fibration]], [[right/left anodyne map]]

* **inner fibration**

* [[Cartesian fibration]]  

* [[fibration]] in the [[model structure for quasi-categories]]

* [[fibration of (infinity,1)-operads]]



## References

Inner fibrations were introduced by [[Andre Joyal]]. A comprehensive account is in section 2.3 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_


Their relation to [[cograph of a profunctor|cographs]]/correspondence is discussed in section 2.3.1 there.

[[!redirects inner fibrations]]

[[!redirects inner Kan fibration]]
[[!redirects inner Kan fibrations]]
