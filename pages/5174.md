
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

A _Lawvere distribution_ is a [[cosheaf]] valued in some [[topos]], such as the [[category of sets]] [[Set]].
The concept of _Lawvere distribution_ is a kind of _[[categorification]]_ of the concept of _[[distribution]]_ in [[functional analysis]].

To some extent one may think of a [[sheaf]] $F$ on a [[topological space]] as being a [[Set]]-valued [[function]] on that space: to each point $x \in X$ it assigns the [[stalk]] $x^* F \in Set$. In this analogy a _Lawvere distribution_ is the analog of a [[distribution]] in the sense of [[functional analysis]]: where the latter is a [[continuous linear functional]], the former is a [[colimit]]-preserving [[functor]].
(Here we think of a [[coproduct]] of sets as the [[categorification]] (under set [[cardinality]]) of the [[sum]] of [[numbers]] and hence read preservation of colimits as _linearity_ .)

Better yet, under [[∞-groupoid cardinality]] we may think of tame [[∞-groupoid]]s as [[real numbers]] and hence of [[(∞,1)-sheaves]] as a [[higher category theory|higher]]/[[homotopy theory|homotopical]] [[categorification]] of real-number valued functions. This yields a more general notion of Lawvere distributions on [[(∞,1)-toposes]] given by [[(∞,1)-colimit]] preserving [[(∞,1)-functors]].

Still more generally one may allow to generalize $(\infty,1)$-toposes to general [[locally presentable (∞,1)-categories]]. Viewed this way, Lawvere distributions are the morphism in $Pr(\infty,1)Cat$, the [[symmetric monoidal (∞,1)-category of presentable (∞,1)-categories]].


## Definition

Throughout $\mathcal{S}$ is some base [[topos]] or [[(∞,1)-topos]] and all notions are to be understood as indexed over this base. 

+-- {: .un_defn}
###### Definition

(Lawvere, see Definition 1.3.4 in Bunge and Funk \cite{SCT}.)

Let $\mathcal{E}$ and $\mathcal{K}$ be [[(∞,1)-toposes]] over [[Set]] (more generally, over an [[elementary topos]] $S$ with a [[natural numbers object]]). A **distribution** on $\mathcal{E}$ with values in $\mathcal{K}$ is
an [[(∞,1)-cosheaf]] on $E$ with values in $K$, i.e.,
an [[(∞,1)-functor]]
$$
  \mu : \mathcal{E} \to \mathcal{K}
$$
that preserves $S$-small [[(∞,1)-colimit]]s.
We write
$$
  Dist_S(\mathcal{E}, \mathcal{K}) \subset (\infty,1)Func(\mathcal{E}, \mathcal{K})
$$
for the full [[sub-(∞,1)-category]] of the [[(∞,1)-category of (∞,1)-functors]] on those that are [[(∞,1)-cosheaves]], i.e., preserve $S$-small colimits.

=--

+-- {: .un_remark}
###### Remark

By the [[adjoint (∞,1)-functor theorem]] this is equivalently a pair
$$
  (\mu \dashv \mu^*) : \mathcal{E} \to \mathcal{K}
$$
of ($S$-indexed) [[adjoint (∞,1)-functor]]s.

=--

+-- {: .un_remark}
###### Notation

To amplify the interpretation in analogy with [[distribution]]s in [[functional analysis]] one sometimes writes 
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

This construction also works in the relative setting:
if $e\colon E\to K$ [[locally ∞-connected geometric morphism]] of [[(∞,1)-toposes]],
then $e_!\colon E\to K$ is a $K$-valued Lawvere distribution on $E$.

### Local toposes

If $E$ is a [[local (∞,1)-topos]],
more generally, $e\colon E\to K$ is a [[local (∞,1)-geometric morphism]] of [[(∞,1)-toposes]],
then the right adjoint $e_*$ is a (left exact) Lawvere distribution on $E$.


### Multiplication of distributions by functions

For $F \in \mathcal{E}$ an $(\infty,1)$-sheaf and $\mu : \mathcal{E} \to \mathcal{S}$ a distribution, there is a new distribution

$$
  F \cdot \mu : 
  G \mapsto 
  \mu(F \times G)
  \,.
$$

In the functional notation this is the formula

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

## Related entries

* [[symmetric topos]]
* [[bagdomain topos]]
* [[cosheaf]]

For the $(\infty,1)$-category theory generalization and related references:

* [[Pr(∞,1)Cat]]

## References

The 1-categorical notion has been described by [[Bill Lawvere]] in a series of talks and expositions. For instance in the context of [[cohesive topos]]es in 

* [[Bill Lawvere]], _Axiomatic cohesion_ , Theory and Applications of Categories, Vol. 19, No. 3, 2007, pp. 41&#8211;49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))

A comprehensive discussion is in

* [[Marta Bunge]] and [[Jonathon Funk]], _Singular coverings of toposes_ , Lecture Notes in Mathematics vol. 1890 Springer Heidelberg (2006). (chap. 1)

See also:

* [[Marta Bunge]], _Cosheaves and Distributions on Toposes_ , Alg. Univ. **34** (1995) pp.469-484.

* [[Marta Bunge]], [[Jonathon Funk]], _Spreads and the Symmetric Topos_ , JPAA **113** (1996) pp.1-38.

* [[Marta Bunge]], [[Jonathon Funk]], _Spreads and the Symmetric Topos II_ , JPAA **130** (1998) pp.49-84.

* [[Anders Kock]], [[Gonzalo E. Reyes]], _A Note on Frame Distributions_ , Cah. Top. G&#233;om. Diff. Cat.**40** (1999) pp.127-140.

* [[Andrew Pitts]], _On Product and Change of Base for Toposes_ , Cah. Top. G&#233;om. Diff. Cat.**26** (1985) pp.43-61.



[[!redirects topos distribution]]
[[!redirects Lawvere distributions]]
