
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--
#Contents#
* table of contents
{: toc}

## Idea

In the language of [[(∞,1)-topos theory]] the ordinary definition of [[gerbe]] has the following simple re-formulation: 

In a given [[(2,1)-topos]], a _[[gerbe]]_ is an object which is 

1. [[1-connective]];

1. [[1-truncated]].

There are various evident generalizations of this, where one allows the degree in either of the two clauses to vary. In the literature one finds higher gerbes defined in either way, and so there are more general and more specific definitions.

## Definition 

### General

+-- {: .num_defn}
###### Definition

Let $\mathcal{X}$ be an [[(∞,1)-topos]].

For $n \in \overline{\mathbb{N}}$ an [[extended natural number]], 

* a **general $n$-gerbe** is an object $\mathcal{G} \in \mathbf{G}$ that is 

  1. [[1-connective]];

  1. [[n-truncated]].

* a **restricted $n$-gerbe** is an object $\mathcal{G} \in \mathbf{G}$ that is 

  1. [[n-connective]]

  1. [[n-truncated]].

=--

The definition of "restricted" $n$-gerbe appears as [[Higher Topos Theory|HTT, def. 7.2.2.20]]. For $n = 2$ the definition of "general $n$-gerbe" (called a _nonabelian 2-gerbe_ at [[2-gerbe]]) appears for instance in ([Breen](#Breen))

In particular we have then the following.

+-- {: .num_defn #InfinityGerbe}
###### Definition

An **$\infty$-gerbe** in $\mathcal{X}$ is a [[1-connective|connected]] object.

=--

+-- {: .num_remark}
###### Remark

If one adds to the definition of "restricted $n$-gerbe" the condition that $\mathcal{G}$ has a "global section", a [[global element]] $* \to \mathcal{G}$, then it becomes the definition of an [[Eilenberg-MacLane object]] in degree $n$. In other words, restricted $n$-gerbes are just like Eilenberg-MacLane objects without necessarily a global section.

By the main theorem at [[looping and delooping]] the connected _and_ [[pointed object|pointed]] objects in an [[(∞,1)-topos]] $\mathcal{X}$ are equivalently (the [[delooping]]s of) [[∞-group]] objects: we have an [[equivalence of (∞,1)-categories]]

$$
  (\Omega \dashv \mathbf{B})
  : 
  \infty Grp(\mathcal{X})
   \stackrel{\overset{\Omega}{\leftarrow}}{\underset{\mathbf{B}}{\to}}
  \mathcal{X}_{*, \geq 1}
  \,.
$$

Therefore a $\infty$-gerbe is much like the delooping of an $\infty$-group, only that a global section may be missing.

But notice that a section always exists locally: for 

$$
  (x^* \dashv x_*) : \infty Grpd 
   \stackrel{\overset{x^*}{\leftarrow}}{\underset{x_*}{\to}}
  \mathcal{X}
$$

any [[point of a topos|topos point]] and $P \in \mathcal{X}$ an $\infty$-gerbe, the [[stalk]] $x^* P \in $ [[∞Grpd]] is [[connected]], because the [[inverse image]] $x^*$ preserves the [[finite limit]]s that define [[categorical homotopy groups in an (∞,1)-topos]] and preserves the [[terminal object]] $*$:

$$
  x^* P \simeq B G_x
  \,.
$$

Therefore it is natural to consider the notion of an _$G$-$\infty$-gerbe_ for a fixed $G \in \infty Grp(\mathcal{X})$. This is done [below](#GInfinityGerbes).


=--

### $G$-$\infty$-Gerbes
 {#GInfinityGerbes}

Let $\mathcal{X}$ be an [[(∞,1)-topos]].

+-- {: .num_defn #GInfinityGerbe}
###### Definition

For $G \in \infty Grp(\mathcal{X})$ an [[∞-group]], a **$G$-$\infty$-gerbe** $P$ is

* an $\infty$-gerbe, def. \ref{InfinityGerbe};

* such that there exists an [[effective epimorphism in an (∞,1)-category|effective epimorphism]] $U \to *$ in $\mathcal{X}$ and an [[equivalence in an (∞,1)-category|equivalence]]

  $$
    P|_U \simeq \mathbf{B}G|_U
    \,.
  $$

=--

## Properties

### Classification of $G$-$\infty$-gerbes

> A brief note on a discussion that should go here in more detail:

Comparing with the discussion at [[associated ∞-bundle]] one finds that def. \ref{GInfinityGerbe} of $G$-$\infty$-gerbes defines "locally trivial $\mathbf{B}G$-fibrations". By the main theorem there, these are classified by [[cohomology]] in $\mathcal{X}$ with coefficients in the [[internalization|internal]] [[automorphism ∞-group]] 

$$
  AUT(G) := \underline{Aut}(\mathbf{B}G)
$$

in that 

$$
  \pi_0 Core(G Gerbe)
  \simeq
  \pi_0 \mathcal{X}(*,\mathbf{B}AUT(G))
  =:
  H^1(\mathcal{X}, AUT(G))
  \,.
$$

The right hand side classifies als $AUT(G)$-[[principal ∞-bundles]] and this equivalence identifies $G$-$\infty$-gerbes as the canonical $AUT(G)$-[[associated ∞-bundles]].

(Compare to the analogous discussion in the special case of [[gerbe]]s.)

## Related entries

* [[principal bundle]] / [[torsor]] / [[associated bundle]]

* [[principal 2-bundle]] / [[gerbe]] / [[bundle gerbe]]

* [[principal 3-bundle]] / [[2-gerbe]] / [[bundle 2-gerbe]]

* [[principal ∞-bundle]] / [[associated ∞-bundle]]  / **$\infty$-gerbe**.


Notice that the notion of [[bundle gerbe]] and [[bundle 2-gerbe]] etc. is not unrelated, but is _a priori_ a rather different notion.

## References

The notion of "restricted" $\infty$-gerbes in an $(\infty,1)$-topos appears in section 7.2.2 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

The "general" notion (but without a concept of ambient $(3,1)$-topos made explicit) for $n = 2$ (see [[2-gerbe]]) appears for instance in

* [[Lawrence Breen]], _Notes on 1- and 2-gerbes_ in [[John Baez]], [[Peter May]] (eds.) _[[Towards Higher Categories]]_ ([arXiv:math/0611317](http://arxiv.org/abs/math/0611317)).
  {#Breen}

The general notion for arbitrary $n$ in an $(\infty,1)$-topos context is discussed in section 2.3 of

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_ .


[[!redirects ∞-gerbe]]
[[!redirects ∞-gerbes]]
[[!redirects infinity-gerbe]]
[[!redirects infinity-gerbes]]

[[!redirects n-gerbe]]
[[!redirects n-gerbes]]
