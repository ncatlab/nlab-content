
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

Let $C$ be a small [[site]], i.e. a [[small category]] equipped with a [[Grothendieck topology]].  We say that $C$ is a **cohesive site** if

1. $C$ has finite [[products]].

1. The coverage on $C$ makes it a [[locally connected site]], i.e. every [[cover|covering]] [[sieve]] on an object $U\in C$ is [[connected category|connected]] as a [[subcategory]] of the [[slice category]] $C/U$.

1. Every object $U\in C$ admits a [[global section]] $*\to U$.

1. (more conditions?)

## Sheaves on cohesive sites

We claim that the topos $Sh(C)$ of sheaves on a cohesive site $C$ is a [[cohesive topos]].  We will write $Disc = L Const$ for the [[inverse image functor]] of the [[global sections]] [[geometric morphism]] $(L Const, \Gamma)\colon Sh(C) \to Set$, since it constructs [[discrete objects]] in the cohesive topos $Sh(C)$.

Firstly, since $C$ is a [[locally connected site]], any constant presheaf is a sheaf.  This implies that the functor $Disc$ has a further left adjoint given by taking colimits over $C^{op}$, which we denote $\Pi_0$.  Hence $Sh(C)$ is a [[locally connected topos]].

Moreover, since $C$ has finite products, it is in particular [[cosifted category|cosifted]], and therefore $\Pi_0$ preserves finite products.  In particular, $Sh(C)$ is [[connected topos|connected]] and even *strongly connected*.

Next, we claim that $C$ is a [[local site]].  This means that its [[terminal object]] $*$ is *cover-irreducible*, i.e. any covering [[sieve]] of $*$ must contain its identity map.  But since $C$ is a locally connected site, every covering family is inhabited, and since every object has a global section, every covering sieve must include a global section.  In the case of $*$, the only global section is an identity map; hence $C$ is a local site, and so $Sh(C)$ is a [[local topos]].  The right adjoint $Codisc$ of $\Gamma$ is defined by
$$ Codisc(A)(U) = A^{C(*,U)} = A^{\Gamma(U)}.$$

We now claim that the transformation $Disc(A) \to Codisc(A)$ is [[monic]].  Since sheaves are closed under limits in presheaves, this condition can be checked pointwise at each object $U\in C$.  But since constant presheaves are sheaves, the map $Disc(A)(U) \to Codisc(A)(U)$ is just the [[diagonal morphism|diagonal]]
$$ A \to A^{C(*,U)} $$
which is monic since $C(*,U)$ is always inhabited (by assumption on $C$).

Thus, it remains to show "continuity" of $\Pi_0$. ...

## Examples

### Families of sets {#FamiliesOfSets}

Consider the site given by the [[interval category]] 

$$
  C = \{\emptyset \to *\}
$$

equipped with trivial [[Grothendieck topology|topology]]. The category of sheaves = presheaves on this is the [[arrow category]] 

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

We may interpret this as follows: by decomposing $S$ into its [[fiber]]s, an object $(I \leftarrow S)$ is an $I$-indexed family of sets: $S = \coprod_i S_i$. The "cohesive pieces" are the $S_i$ and there are $|I|$-many of them. This is what $\Pi_0$ computes, which clearly preserves products.

Moreover we find for $K \in Set$:

* $Disc : K \mapsto (K \stackrel{Id}{\leftarrow} K)$;

* $CoDisc : K \mapsto (* \stackrel{}{\leftarrow} K)$

(and evidently both these functors are full and faithful).

This matches the interpretation we just found: $Disc K$ is the collection of elements of $K$ with no two of them lumped together by cohesion, while $Codisc K$ is all elements of $K$ lumped together.

What is not true in this example is that $Disc K \to Codisc K$ is a monomorphism. In particular, notice that the fibers $S_i$ may be empty. This is notably the case for the object $y(\emptyset) = (* \leftarrow \emptyset)$ represented by $\emptyset$. So there may be cohesive pieces that contain no point.

This is the simplest special case of a general class of examples:

for $C$ any [[small category]], we have the left and right [[Kan extension]] of presehaves $F : C^{op} \to Set$ along the [[functor]] $C^{op} \to *$. By definition, this are the [[colimit]] and [[limit]] functors

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

### Sites of balls

Any full small subcategory of [[Top]] on [[connected]] topological spaces with the canonical induced [[open cover]] [[coverage]] is a cohesive site. If a subcategory on [[contractible]] spaces, then this is also an [[(∞,1)-cohesive site]]. 

This includes notably the category [[CartSp]] of all [[open ball]]s (with either continuous maps or smooth maps as morphism). 
 


## Related concepts

An [[(n,1)-cohesive site]] is a site whose [[(n,1)-topos]] of $n$-sheaves is [[cohesive (n,1)-topos|cohesive]], and an [[(∞,1)-cohesive site]] is a site whose [[(∞,1)-topos]] of sheaves is [[cohesive (∞,1)-topos|cohesive]].


* [[locally connected site]] / [[locally ∞-connected site]]

* **cohesive site** / [[(∞,1)-cohesive site]]


[[!redirects cohesive sites]]
[[!redirects site of cohesion]]
[[!redirects sites of cohesion]]
