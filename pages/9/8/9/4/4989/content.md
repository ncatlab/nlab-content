
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Cohesive site
* table of contents
{: toc}

## Idea

A **cohesive site** is a small [[site]] whose [[topos of sheaves]] is a [[cohesive topos]].

## Definition


+-- {: .un_def}
###### Definition

Let $C$ be a small [[site]], i.e. a [[small category]] equipped with a [[coverage]]/[[Grothendieck topology]].  We say that $C$ is a **cohesive site** if

1. $C$ has a [[terminal object]].

1. The coverage on $C$ makes it a [[locally connected site]], i.e. every [[cover|covering]] [[sieve]] on an object $U\in C$ is [[connected category|connected]] as a [[subcategory]] of the [[slice category]] $C/U$.

1. Every object $U\in C$ admits a [[global section]] $*\to U$.

1. $C$ is a [[cosifted category]].

=--

Notice that if $C$ has finite [[product]]s then it is also cosifted.

## Properties: sheaves on a cohesive site

+-- {: .un_prop}
###### Proposition

For $C$ a cohesive site, the [[category of sheaves]] $Sh(C)$ on $C$ 
is a [[cohesive topos]] over [[Set]] for which _cohesive pieces have points_ .

=--

+-- {: .proof}
###### Proof

Following the notation at [[cohesive topos]], we write 

$$
  (Disc \dashv \Gamma) := (L Const \dashv \Gamma) : Sh(C) \to Set
$$

for the [[global section]] [[geometric morphism]], where the [[inverse image]] $Disc$ constructs [[discrete object]]s. We need to exhibit two more adjoints

$$
  (\Pi_0 \dashv Disc \dashv \Gamma \dashv CoDisc) : Sh(C) \to Set
$$

and show that $\Pi_0$ preserves finite [[product]]s. Finally we need to show that $\Gamma X \to \Pi_0 X$ is an [[epimorphism]] for all $X$.

Firstly, since $C$ is a [[locally connected site]], any constant presheaf is a sheaf.  This implies that the functor $Disc$ has a further [[left adjoint]] given by taking colimits over $C^{op}$, which we denote $\Pi_0$.  Hence $Sh(C)$ is a [[locally connected topos]].

Moreover, since $C$ is [[cosifted category|cosifted]], $\Pi_0$ preserves finite products.  In particular, $Sh(C)$ is [[connected topos|connected]] and even *strongly connected*.

Next, we claim that $C$ is a [[local site]].  This means that its [[terminal object]] $*$ is *cover-irreducible*, i.e. any covering [[sieve]] of $*$ must contain its identity map.  But since $C$ is a locally connected site, every covering family is inhabited, and since every object has a global section, every covering sieve must include a global section.  In the case of $*$, the only global section is an identity map; hence $C$ is a local site, and so $Sh(C)$ is a [[local topos]].  The [[right adjoint]] $Codisc$ of $\Gamma$ is defined by

$$ 
  CoDisc(A)(U) = A^{C(*,U)} = A^{\Gamma(U)}
  \,.
$$

We now claim that the transformation $Disc(A) \to Codisc(A)$ is [[monic]].  Since sheaves are closed under limits in presheaves, this condition can be checked pointwise at each object $U\in C$.  But since constant presheaves are sheaves, the map $Disc(A)(U) \to Codisc(A)(U)$ is just the [[diagonal morphism|diagonal]]

$$ 
  A \to A^{C(*,U)} 
$$

which is monic since $C(*,U)$ is always inhabited (by assumption on $C$).

=--

## Examples

### Cohesive presheaf sites

Consider a category $C$ equipped with the trivial coverage/topology. Then the [[category of sheaves]] on $C$ is the [[category of presheaves]] on $C$

$$
  Sh(C) \simeq PSh(C)
$$

and trivially every constant presheaf is a sheaf. So we always has a triple of adjoint functors

$$
  (\Pi_0 \dashv Disc \dashv \Gamma) : Sh(C) \to Set
  \,,
$$

where

* $\Pi_0$ is the functor that takes [[colimit]]s of functors $X : C^{op} \to Set$ 

  $$
    \Pi_0 X = {\lim_\to} X
  $$

* $\Gamma$ is the functor that takes [[limit]]s;

  $$
    \Gamma X = {\lim_\leftarrow} X    
    \,.
  $$

The condition that $\Pi_0$ preserves finite products is precisely the condition that $C$ be a [[cosifted category]].

In conclusion we have

+-- {: .un_prop}
###### Proposition

A small category equipped with the trivial coverage/topology is a cohesive site if

* it is cosifted;

* has a terminal object $*$.

* every object $U$ has a global points $* \to U$.

The first two conditions ensure that $Sh(C) = PSh(C)$ is a cohesive topos. The last condition implies that _cohesive pieces have points_ in $PSh(C)$.

=--

### Cohesive toposes of families of sets {#FamiliesOfSets}

We discuss cohesive toposes over sites with trivial coverage/topology, with terminal object _and_ initial object. In general these sites are not cohesive sites by the above definition in that not every object has a global point. Accordingly the cohesive toposes over these sites fail to satisfy the condition _cohesive pieces have points_ . The interest in these cases is that nevertheless they serve as a simple illustration of how the axioms model cohesiveness of points.

Consider the site given by the [[interval category]] 

$$
  C = \{\emptyset \to *\}
$$

equipped with trivial [[Grothendieck topology|topology]]. This evidently has an [[initial object]] $\emptyset$ (which makes it cosifted) and a [[terminal object]] $*$.

The category of sheaves = presheaves on this is the [[arrow category]] 

$$
  Sh(\{\emptyset \to *\})
  \simeq
   PSh(\{\emptyset \to *\})
  \simeq
  Arr(Set)
$$

since a presheaf $X$ on $C$ is given by a morphism

$$
  X : (\emptyset \to *) \mapsto (I \leftarrow S)
$$

in [[Set]]. We find

* $\Gamma : (I \leftarrow S) \mapsto S$

* $\Pi_0 : (I \leftarrow S) \mapsto I$.

Trivial as this is, it does provide some insight into the interpretation of cohesiveness: by decomposing $S$ into its [[fiber]]s, an object $(I \leftarrow S)$ is an $I$-indexed family of sets: $S = \coprod_i S_i$. The "cohesive pieces" are the $S_i$ and there are $|I|$-many of them. This is what $\Pi_0$ computes, which clearly preserves products.

Moreover we find for $K \in Set$:

* $Disc : K \mapsto (K \stackrel{Id}{\leftarrow} K)$;

* $CoDisc : K \mapsto (* \stackrel{}{\leftarrow} K)$

(and evidently both these functors are full and faithful).

This matches the interpretation we just found: $Disc K$ is the collection of elements of $K$ with no two of them lumped together by cohesion, while $Codisc K$ is all elements of $K$ lumped together.

The canonical morphism 

$$
  \Gamma (I \leftarrow S) \to \Pi_0 (I \leftarrow S)
$$

is

$$
  \Gamma Disc \Gamma (I \leftarrow S) \to \Gamma (I \leftarrow S) \to \Gamma Disc \Pi_0 (I \leftarrow S)
  \,.
$$

Plugging in the above this is just

$$
  S \to I
$$

itself. Indeed, by the above interpretation, this sends each point to its cohesive component. It is not an epimorphism in general, because the fiber $S_i$ over an element $i$ may be empty: the cohesive component $i$ may have no points.


This is the simplest special case of a general class of examples: for $C$ any [[small category]], we have the left and right [[Kan extension]] of presehaves $F : C^{op} \to Set$ along the [[functor]] $C^{op} \to *$. By definition, this are the [[colimit]] and [[limit]] functors

$$
  (\lim_\to \dashv Const \dashv \lim_\leftarrow) :
  PSh(C) \stackrel{\overset{\lim_{\to}}{\to}}{\stackrel{\overset{Const}{\leftarrow}}{\underset{\lim_\leftarrow}{\to}}}
  Set
  \,.
$$

+-- {: .un_lemma}
###### Observation

If $C$ has a [[terminal object]] $*$ then 

* $\lim_\leftarrow$ is given by evaluation on this object;

* there is a further [[right adjoint]] $(\lim_\leftarrow \dashv CoConst)$

  given by

  $$
    CoConst : S \mapsto (c \mapsto Set(C(*,c), S)
    \,.
  $$

=--

+-- {: .proof}
###### Proof

The terminal object of $C$ is the [[initial object]] of the [[opposite category]] $C^{op}$ and therefore the limit over any functor $F : C^{op} \to Set$ is given by evaluation on this object

$$
  \lim_\leftarrow (C^{op} \stackrel{F}{\to} Set) \simeq F(*)
  \,.
$$

To see that we have a pair of [[adjoint functor]]s $(\lim_\to \dashv CoConst)$
we check the natural [[hom-set]] equivalence 
$PSh_C(F, CoConst S ) \simeq Set(\lim_\to F , S)$ by computing

$$
  \begin{aligned}
    PSh_C(F , CoConst S) 
     & \simeq 
      \int_{c \in C} Set(F(c), Set(C(*,c), S))
    \\
    & \simeq
        \int_{c \in C} Set(F(c) \times C(*,c), S)
    \\
     & \simeq 
         Set( \int^{c \in C} F(c) \times C(*,c) , \; S)
    \\
     & \simeq Set(F(*), S)
  \end{aligned}
  \,,
$$

Here the first step is the expression of [[natural transformation]]s by [[end]]-calculus, the second uses the fact that [[Set]] is a [[cartesian closed category]], the third uses that any [[hom-functor]] sends [[coend]]s in the first argument to ends, and the last one uses the [[co-Yoneda lemma]].

=--

The formal dual of this statement is the following.

+-- {: .un_lemma}
###### Corollary

If $C$ has an [[initial object]] $\emptyset$ then 

* $\lim_\to$ is given by evaluation on this object;

* there is a further [[left adjoint]] $(L \dashv \lim_\to)$,

  so that $\lim_\to$ preserves all small limits and in particular
  all finite products.

=--

In summary we have

+-- {: .un_lemma}
###### Proposition

If $C$ has both an [[initial object]] $\emptyset$ as well as a [[terminal object]] $*$ then there is a quadruple of adjoint functors

$$
  (\Pi_0 \dashv Disc \dashv \Gamma \dashv CoDisc)
   :
   PSh(C) \to Set
  \,,
$$

where

* $\Gamma$ is given by evaluation on $*$;

* $\Pi_0$ is given by evaluation of $\emptyset$ and preserves products.

=--

The above interpretation of the cohesiveness encoded by $C = \{\emptyset \to *\}$ still applies to the general case: a general object $X \in PSh(C)$ is, by restriction to the unique morphism $\emptyset \to *$ in $C$ a set-indexed  family of sets

$$
  X(\emptyset \to *) = (\Pi_0(X) = X(\emptyset) \leftarrow  X(*) = \Gamma(X))
$$

and $\Gamma$ picks out the total set of points, while $\Pi_0$ picks of the indexing set ("of cohesive components"). The extra information for general $C$ with initial and terminal object is that for every object $c \in C$ these cohesive lumps of points are refined to a hierarchy of lumps and lumps-of-lumps

$$
  X(\emptyset \to c \to *) = (\Pi_0(X) \leftarrow X(c) \leftarrow \Gamma(X))
  \,.
$$ 

### Sites of open balls

Any full small subcategory of [[Top]] on [[connected]] topological spaces with the canonical induced [[open cover]] [[coverage]] is a cohesive site. If a subcategory on [[contractible]] spaces, then this is also an [[(∞,1)-cohesive site]]. 

Specifically we have:

+-- {: .un_prop}
###### Proposition

The categories [[CartSp]] and [[ThCartSp]] equipped with the standard [[open cover]] [[coverage]] are cohesive sites.

=--

The axioms are readily checked.

Notice that the cohesive topos over $ThCartSp$ is the [[Cahiers topos]].

+-- {: .un_prop}
###### Proposition

The cohesive concrete objects of the cohesive topos $Sh(CartSp)$ are precisely the [[diffeological space]]s.

=-- 

See [[cohesive topos]] for more on this.


## Related concepts


* [[locally connected site]] / [[locally ∞-connected site]]

* **cohesive site** / [[(∞,1)-cohesive site]]


[[!redirects cohesive sites]]
[[!redirects site of cohesion]]
[[!redirects sites of cohesion]]
