
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
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

To some extent one can think of a [[sheaf]] $F$ on a [[topological space]] as being like a [[Set]]-valued [[function]] on that space: to each point $x \in X$ it assigns the [[stalk]] $x^* F \in Set$. A _Lawvere distribution_ is in this analogy the analog of a [[distribution]] in the sense of [[functional analysis]]: where the latter is a [[linear functional]], the former is a [[colimit]]-preserving [[functor]].

Here we think of a [[coproduct]] of sets as the [[categorification]] (under set [[cardinality]]) of the sum of numbers and hence read preservation of colimits as _linearity_ .

Better yet, under [[∞-groupoid cardinality]] we may think of tame [[∞-groupoid]]s as [[real number]]s and hence of [[(∞,1)-sheaves]] as analogous to functions. This yields a notion of Lawvere distributions on [[(∞,1)-topos]]es given by [[(∞,1)-colimit]] preserving [[(∞,1)-functor]]s.

More generally one can allow to generalize $(\infty,1)$-toposes to general [[locally presentable (∞,1)-categories]]. Viewed this way, Lawvere distributions are the morphism in $Pr(\infty,1)Cat$, the [[symmetric monoidal (∞,1)-category of presentable (∞,1)-categories]].


## Definition

Throughout $\mathcal{S}$ is some base [[topos]] or [[(∞,1)-topos]] and all notions are to be understood as indexed over this base. 

+-- {: .un_defn}
###### Definition

Let $\mathcal{E}$ and $\mathcal{K}$ be [[(n,1)-topos]]es. A **distribution** on $\mathcal{E}$ with values in $\mathcal{K}$ is a [[(∞,1)-functor]]

$$
  \mu : \mathcal{E} \to \mathcal{K}
$$

that preserves small [[(∞,1)-colimit]]s.

Write

$$
  Dist(\mathcal{E}, \mathcal{K}) \subset (\infty,1)Func(\mathcal{E}, \mathcal{K})
$$

for the full [[sub-(∞,1)-category]] of the [[(∞,1)-category of (∞,1)-functors]] on those that preserve finite colimits.

=--

+-- {: .un_remark}
###### Remark

By the [[adjoint (∞,1)-functor theorem]] this is equivalently a pair

$$
  (\mu \dashv \mu^*) : \mathcal{E} \to \mathcal{K}
$$

of [[adjoint (∞,1)-functor]]s.

=--

+-- {: .un_remark}
###### Notation

To amplify the interpretation in analogy with [[distribution]]s in [[functional analysis]] one sometimes write 

$$
  \int_{\mathcal{E}} (-) d\mu : \mathcal{E} \to \mathcal{K}
$$

for a Lawvere distribution $\mu$.

Notably in the case that $\mathcal{K} = $ [[∞Grpd]] and $F$ is an [[(∞,1)-sheaf]] such that $\mu(F)$ is tame, we may use

$$
   \int_{\mathcal{E}} F d \mu \in \mathbb{R}
$$

for the corresponding [[∞-groupoid cardinality]].

=--


## Examples

### Dirac $\delta$-distributions {#DiracDeltaDistribution}

A [[point of a topos]] is a [[geometric morphism]] of the form

$$
  (p^* \dashv p_*) : \mathcal{S} \stackrel{\leftarrow}{\to} \mathcal{E}
  \,.
$$

The [[left adjoint]] $p^*$ is therefore a Lawvere distribution. This sends any [[(∞,1)-sheaf]] to its [[stalk]] at the point $p$. So this behaves like the [[Dirac distribution]] on functions.

### The canonical distribution on a locally $\infty$-connected topos

If $\mathcal{E}$ is a [[locally ∞-connected (∞,1)-topos]] then its terminal [[global section]] [[(∞,1)-geometric morphism]] by definition has a further left adjoint

$$
  (\Pi \dashv \Delta \dashv \Gamma) : \mathcal{E} \stackrel{\overset{\Pi_0}{\to}}{\stackrel{\overset{\Delta}{\leftarrow}}{\underset{\Gamma}{\to}}}
  \mathcal{S}
  \,.
$$

This left adjoint $\Pi$ (the [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]]) is therefore a canonical $\mathcal{S}$-valued distribution on $\mathcal{E}$. It is also written

$$
  \int_{\mathcal{E}}(-) d x : \mathcal{E} \to \infty Grpd
  \,.
$$

### Multiplication of distributions by functions

For $F \in \mathcal{E}$ an $(\infty,1)$-sheaf and $\mu : \mathcal{E} \to \mathcal{S}$ a distribution, there is a new distribution

$$
  F \cdot \mu : 
  G \mapsto 
  \mu(F \times G)
  \,.
$$

In the functional-notation this is the formula

$$
  \int_{\mathcal{E}} G d(F \times \mu)
  = 
  \int_{\mathcal{E}} G \times F d \mu
  \,.
$$


### Distributions on the point

The [[∞Grpd]]-valued distributions on $\infty Grpd \simeq Sh_{(\infty,1)}(*)$ itself coincide with the value at the single point

$$
  Dist(\infty Grpd, \infty Grpd) \simeq \infty Grpd.
$$



## References

The 1-categorical notion has been described by [[Bill Lawvere]] in a series of talks and expositions. For instance in the context of [[cohesive topos]]es in 

* [[Bill Lawvere]], _Axiomatic cohesion_ Theory and Applications of Categories, Vol. 19, No. 3, 2007, pp. 41&#8211;49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))

A comprehensive discussion is in

* [[Marta Bunge]] and Jonathan Funk, _Singular coverings of toposes_ Lecture Notes in Mathematics, (2006) Volume 1890/2006

  chapter 1 _Lawvere Distributions on Toposes_

For the $(\infty,1)$-category theory generalization see [[Pr(∞,1)Cat]] and references given there.