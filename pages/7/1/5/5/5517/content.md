

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
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

* a **$n$-gerbe** is an object $\mathcal{G} \in \mathbf{G}$ that is 

  1. [[1-connective]];

  1. [[n-truncated]].

* an **EM $n$-gerbe** is an an $n$-gerbe that is 

  1. [[n-connective]]

  1. [[n-truncated]].

=--

The definition of "EM $n$-gerbes" appears as [[Higher Topos Theory|HTT, def. 7.2.2.20]]. For $n = 2$ the definition of "general $n$-gerbe" (called a _nonabelian 2-gerbe_ at [[2-gerbe]]) appears for instance in ([Breen](#Breen)).  

In particular we have then the following.

+-- {: .num_defn #InfinityGerbe}
###### Definition

An **$\infty$-gerbe** in $\mathcal{X}$ is a [[1-connective|connected]] object.

Write

$$
  \infty Gerbe \subset \mathcal{X}
$$

for the [[core]] of the full-[[sub-(∞,1)-category]] on the $\infty$-gerbes.

=--

+-- {: .num_remark}
###### Warning

The notion of [[morphisms]] between EM $n$-gerbes in [[Higher Topos Theory|HTT, pages 576, 577]] is more restrictive than this. This is the reason why the classification found there is a restriction of the general classification. This is discussed [below](#Properties).

=--

+-- {: .num_remark}
###### Remark

If one adds to the definition of "EM $n$-gerbe" the condition that $\mathcal{G}$ has a "global section", a [[global element]] $* \to \mathcal{G}$, then it becomes the definition of an [[Eilenberg-MacLane object]] in degree $n$. In other words, EM $n$-gerbes are just like Eilenberg-MacLane objects but without necessarily a global section.

By the main theorem at [[looping and delooping]] the connected _and_ [[pointed object|pointed]] objects in an [[(∞,1)-topos]] $\mathcal{X}$ are equivalently (the [[delooping]]s of) [[∞-group]] objects: we have an [[equivalence of (∞,1)-categories]]

$$
  (\Omega \dashv \mathbf{B})
  : 
  \infty Grp(\mathcal{X})
   \stackrel{\overset{\Omega}{\leftarrow}}{\underset{\mathbf{B}}{\to}}
  \mathcal{X}_{*, \geq 1}
  \,.
$$

Therefore an $\infty$-gerbe is much like the [[delooping]] of an $\infty$-group, only that a global section may be missing.

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

+-- {: .num_defn #AbelianBand}
###### Definition

A "restricted" $n$-gerbe $E$ has, by definition, a single non-trivial [[categorical homotopy group in an (infinity,1)-topos|homotopy sheaf]]. For $n \geq 2$ this is an sheaf of abelian groups $A$ in the underlying [[topos]]

$$
  \pi_n E \simeq A
  \,.
$$

This $A$ is called the **band** of $E$ and that $E$ is **banded by** $A$.

=--

In the case that $n = 1$ or that we have a "general" $n$-gerbe the notion of band is refined by [[nonabelian cohomology]]-information. See [below].

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
 {#Properties}

### Classification of EM $n$-gerbes.

Let $A \in Grp(\mathcal{X}) \subset \infty Grpd(\mathcal{X})$ be an [[abelian group]] object and fix $n \in \mathbb{N}$, $n \geq 2$. 

Recall the notion of $A$-banded $n$-gerbes from def. \ref{AbelianBand}.

Write

$$
  H^{n+1}_{\mathcal{X}}(X, A)  
   := 
  \pi_0 \mathcal{X}(*, \mathbf{B}^{n+1}A)
$$

for the [[cohomology]] in $\mathcal{X}$ of the [[terminal object]] with coefficients in $A$ in degree $n+1$.

+-- {: .num_prop}
###### Proposition

There is a canonical bijection 

$$
  \pi_0 EM n Gerbe_A
   \simeq
  H^{n+1}_{\mathcal{X}}(X, A)
  \,,
$$ 
where $EM n Gerbe_A$ is the category of all $EM$ $n$-gerbes banded over $A$.
=--

This appears as [[Higher Topos Theory|HTT, cor. 7.2.2.27]].

+-- {: .num_remark}
###### Warning

The morphisms of EM $n$-gerbes in [[Higher Topos Theory|HTT, p. 576-577]] are more restrictive than the morphisms of these objects regarded as general $n$-gerbes. 

By the discussion below, if EM $n$-gerbes are regarded as special $n$-gerbes, then their classification is by a [[nonabelian cohomology]]-extension of the above result.

=--

### Classification of $G$-$\infty$-gerbes

We discuss partial generalizations of the above result to nonabelian $\infty$-gerbes


Comparing with the discussion at [[associated ∞-bundle]] one finds that def. \ref{GInfinityGerbe} of $G$-$\infty$-gerbes defines "locally trivial $\mathbf{B}G$-fibrations". By the main theorem there, these are classified by [[cohomology]] in $\mathcal{X}$ with coefficients in the [[internalization|internal]] [[automorphism ∞-group]] 

$$
  AUT(G) := \underline{Aut}(\mathbf{B}G)
$$


+-- {: .num_prop}
###### Proposition

At least for $\mathcal{X}$ a [[n-localic (∞,1)-topos|1-localic]] [[(∞,1)-topos]] we have a canonical bijection

$$
  \pi_0 (G Gerbe)
  \simeq
  H^1(\mathcal{X}, AUT(G))
  \,.
$$

=--

This follows as a special case of the result by ([Wendt](#Wendt)) discussed at [[associated infinity-bundle]].

+-- {: .num_remark}
###### Remark


The right hand side classifies als $AUT(G)$-[[principal ∞-bundles]] and this equivalence identifies $G$-$\infty$-gerbes as the canonical $AUT(G)$-[[associated ∞-bundles]].

=--

(Compare to the analogous discussion in the special case of [[gerbe]]s.)

### Nonabelian banded $\infty$-gerbes

For $G \in \infty Grpd(\mathcal{X})$ an $n$-group (with $n \geq 1$) write

$$
  Out(G) := \tau_{n-1} AUT(G) = \tau_{n-1}\underline{Aut}(\mathbf{B}G)
  \,.
$$

Call this the [[outer automorphism infinity-group]] of $G$. By definition there is a canonical morphism

$$
  \mathbf{B} AUT(G) \to \mathbf{B} Out(G)
  \,.
$$

By the above classification, this induces a morphism

$$
  Band : \pi_0 G Gerbe \to H^1_{\mathcal{X}}(X, Out(G))
$$

from $G$-$n$-gerbes to [[nonabelian cohomology]] in degree 1 with coefficients in $Out(G)$. For $E \in G Gerbe$ the pair

$$
  (\pi_n, Band(E))
$$ 

is called the **band** of $E$. For $[K] \in H^1_{\mathcal{X}}(X, Out(G))$ the [[n-groupoid|(n+1)-groupoid]] $G Gerbe_K$ of $K$-banded $G$-$n$-gerbes is the [[homotopy pullback]] 

$$
  \array{
    G Gerbe_K &\to& *
    \\
    \downarrow && \downarrow^{\mathrlap{K}}
    \\  
    \mathcal{X}(X, \mathbf{B}AUT(G))
    &\to&
    \mathcal{X}(X, \mathbf{B}Out(G))
  }
  \,.
$$

Write $\mathbf{B}^2 Z(G)$ for the [[homotopy fiber]] of $\mathbf{B}AUT(G) \to \mathbf{B}Out(G)$, producing a [[fiber sequence]]

$$
  \mathbf{B}^2 Z(G) \to \mathbf{B} AUT(G) \to \mathbf{B}Out(G)
  \,.
$$

We call $Z(G)$ the [[center of an infinity-group|center of the infinity-group]].

In terms of this the above $G Gerbe_K$ is the  [[cocycle]] $(n+1)$-groupoid of the [[twisted cohomology|K-twisted Z(G)-cohomology]] in degree 2:

$$
  \pi_0 G Gerbe_K \simeq H^2_K(X,Z(G))
  \,.
$$

Notice that if $Z(G)$ itself is [[n-connected|higher connected]] then $H^2_K(X, Z(G))$ is accordingly cohomology in higher degree.

## Examples

### Classification of abelian 2-gerbes
  {#ClassificationOf2Gerbes}

For $X$ a [[topological space]], let $\mathcal{X} = Sh_{(\infty,1)}(X)$ be its [[(∞,1)-category of (∞,1)-sheaves]]. Write 

$$
  U(1) \in Grp(\mathcal{X}) \subset \infty Grp(\mathcal{X})
$$

for the [[sheaf]] of [[circle group]]-valued functions. And $\mathbf{B}U(1)$ for its [[delooping]]

Then

$$
  AUT(\mathbf{B}U(1))
  :=
  \underline{Aut}(\mathbf{B}^2 U(1))
  \simeq
  [U(1) \stackrel{0}{\to} U(1) \stackrel{0}{\to} \mathbb{Z}_2]
  \,,
$$

where on the right we display the [[crossed complex]] corresponding to this 3-group (the morphisms are all constant on the unit element, the action of $\mathbb{Z}_2$ on either of the $U(1)$s is the canonical one given by $\mathb{Z}_2 \simeq Aut(U(1))$ ). This is seen as follows: every invertible [[2-functor]] $F : \mathbf{B}^2 U(1) \to \mathbf{B}^2 U(1)$ comes from a group automorphism of $U(1)$, of which there are $\mathbb{Z}_2$. A [[pseudonatural transformation]] necessarily goes from any such $F$ to itself, and there are $U(1)$ of them. Similarly, any [[modification]] of these necessarily is an endo, and there are also $U(1)$ of them.


Therefore $\mathbf{B}U(1)$-2-gerbes are classified by the [[nonabelian cohomology]]

$$
  H^1(X,[U(1) \to 1 \to \mathbb{Z}_2])
  \,.
$$

This has a subgroup coming from the canonical inclusion

$$
  \mathbf{B}^3 U(1) = [U(1)\to 1 \to 1] \hookrightarrow [U(1) \to 1 \to \mathbb{Z}_2]
$$

on the trivial automorphism of $U(1)$. The classification of $U(1)$ EM-2-gerbes in [[Higher Topos Theory|HTT]] gives only this subgroup

$$
  H^3(X, U(1)) 
    \hookrightarrow 
  H^1(X, [U(1) \to 1 \to \mathbb{Z}_2])
  \,.
$$

In the terminology of [[orientifold]]/[[Jandl gerbe]]s the more general objects on the right are the "Jandl 2-gerbes" or "orientifold 2-gerbes".

## Related entries

* [[principal bundle]] / [[torsor]] / [[associated bundle]]

* [[principal 2-bundle]] / [[gerbe]] / [[bundle gerbe]]

* [[principal 3-bundle]] / [[2-gerbe]] / [[bundle 2-gerbe]]

* [[principal ∞-bundle]] / [[associated ∞-bundle]]  / **$\infty$-gerbe**.

  * [[Super Gerbes]]


Notice that the notion of [[bundle gerbe]] and [[bundle 2-gerbe]] etc. is not unrelated, but is _a priori_ a rather different notion.

## References

The notion of "EM" $\infty$-gerbes in an $(\infty,1)$-topos appears in section 7.2.2 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

The general notion (but without a concept of ambient $(3,1)$-topos made explicit) for $n = 2$ (see [[2-gerbe]]) appears for instance in

* [[Lawrence Breen]], _On the classification of 2-gerbes and 2-stacks_ , Ast&#233;risque 225 (1994).

* [[Lawrence Breen]], _Notes on 1- and 2-gerbes_ in [[John Baez]], [[Peter May]] (eds.) _[[Towards Higher Categories]]_ ([arXiv:math/0611317](http://arxiv.org/abs/math/0611317)).
  {#Breen}

The general notion for arbitrary $n$ in an $(\infty,1)$-topos context is discussed in section 2.3 of

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_ .

Discussion of the classification of $G$-$\infty$-gerbes and more general fiber bundles in 1-localic $(\infty,1)$-toposes  is in

* [[Matthias Wendt]], _Classifying spaces and fibrations of simplicial sheaves_ , Journal of  Homotopy and Related Structures 6(1), 2011, pp. 1--38.  ([arXiv](http://arxiv.org/abs/1009.2930)) ([published version](http://tcms.org.ge/Journals/JHRS/volumes/2011/volume6-1.htm))
{#Wendt}


[[!redirects ∞-gerbe]]
[[!redirects ∞-gerbes]]
[[!redirects infinity-gerbe]]
[[!redirects infinity-gerbes]]

[[!redirects n-gerbe]]
[[!redirects n-gerbes]]
