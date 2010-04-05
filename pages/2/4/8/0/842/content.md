<div class="rightHandSide toc">
[[!include infinity-limits - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The notion of [[limit]] and [[colimit]] generalize from [[category theory]] to [[(∞,1)-category theory]]. One model for [[(∞,1)-categories]] are [[quasi-categories]]. This entry discusses limits and colimits in quasi-categories.


## Definition

+-- {: .un_defn}
###### Definition

For $K$ and $C$ two [[quasi-category|quasi-categories]] and $F : K \to 
C$ an [[(∞,1)-functor]] (a morphism of the underlying [[simplicial set]]s) , the **limit** over $F$ is, if it exists, the [[terminal object in a quasi-category|quasi-categorical terminal object]] in the [[over quasi-category]] $C_{/F}$:

$$
  lim_{\leftarrow} F := TerminalObj(C_{/F})
  \,.
$$

A **colimit** in a quasi-category is accordingly an limit in the [[opposite quasi-category]].

=--

+-- {: .un_remark}
###### Remark

Notice from the discussion at [[join of quasi-categories]] that there are two definitions -- denoted $\star$ and $\diamondsuit$ -- of join, which yield results that differ as simplicial sets, though are equivalent as quasi-categories.

The notation $C_{/F}$ denotes the definition of [[over quasi-category]] induced from $*$, while the notation $C^{/F}$ denotes that induced from $\diamondsuit$. Either can be used for the computation of limits in a quasi-category, as for quasi-categorical purposes they are weakly equivalent.

So we also have

$$
  lim_{\leftarrow} F := TerminalObj(C^{/F})
  \,.
$$

See [[Higher Topos Theory|HTT, prop 4.2.1.5]].

=--



## Special cases

### Coproduct

...

### Pushout

The non-degenerate cells of the [[simplicial set]] $\Delta[1] \times \Delta[1]$ obtained as the [[cartesian product]] of the simplicial 1-[[simplex]] with itself look like

$$
  \array{
    (0,0) &\to& (1,0)
    \\
    \downarrow &\searrow& \downarrow
    \\
    (0,1) &\to& (1,1)
  }
$$

A **sqare** in a [[quasi-category]] $C$ is an image of this in $C$, i.e. a morphism

$$
  s : \Delta[1] \times \Delta[1] \to C
  \,.
$$

The simplicial square $\Delta[1]^{\times 2}$ is [[isomorphism|isomorphic]], as a [[simplicial set]], to the [[join of simplicial sets]] of a 2-[[horn]] with the point:

$$
  \Delta[1] \times \Delta[1]
  \simeq
  \{v\} \star \Lambda[2]_2
  = 
  \left(
  \array{
    v &\to& 1
    \\
    \downarrow &\searrow& \downarrow
    \\
    0 &\to& 2
  }
  \right)
$$

and

$$
  \Delta[1] \times \Delta[1]
  \simeq
  \Lambda[2]_0 \star \{v\}
  = 
  \left(
  \array{
    0&\to& 1
    \\
    \downarrow &\searrow& \downarrow
    \\
    2 &\to& v
  }
  \right)
  \,.
$$

If a square $\Delta[1] \times \Delta[1] \simeq \Lambda[2]_0 \star \{v\} \to C$ exhibits $\{v\} \to C$ as a colimit over $F : \Lambda[2]_0 \to C$, we say the colimit

$$
  v := \lim_\to F := F(1) \coprod_{F(0)} F(2)
$$

is [[generalized the|the]] **pushout** of the diagram $F$.

we have the following $(\infty,1)$-categorical analog of the familiar statement in ordinary [[category theory]]:

+-- {: .un_prop}
###### Proposition

A pasting diagram of two squares is a morphism

$$
  \Delta[2] \times \Delta[1] \to C
  \,.
$$

Schematically this looks like

$$
  \array{
     x &\to& y &\to& z
     \\
     \downarrow && \downarrow && \downarrow
     \\
     x' &\to& y' &\to& z'
  }
  \,.
$$

If the left square is a pushout diagram in $C$, then the right square is precisely if the outer square is.

=--

+-- {: .proof}
###### Proof

A proof appears as [[Higher Topos Theory|HTT, lemma 4.4.2.1]]

=--


### Coequalizer

...

### Tensoring with an $\infty$-groupoid


## Examples


## Properties 


One would like to claim the following _global_ characterization of 
$(\infty,1)$-limits.

Limit and colimit, as defined above, should be [[right adjoint|right]] and [[left adjoint|left]]
[[adjoint (infinity,1)-functor]] of the constant diagram $(\infinity,1)$-functor,
$constt : K \to Func(K,C)$.

$$
  (colim \dashv const \dashv lim)
  :
  Func(K,C)
  \stackrel{\overset{lim}{\to}}{\stackrel{\overset{const}{\leftarrow}}
  {\underset{colim}{\to}}}
  Func(*,C) \simeq C
  \,.
$$

By the discussion at [[adjoint (infinity,1)-functor]] ([[Higher Topos Theory|HTT, prop. 5.2.2.8]]) this requires exhibiitng a morphism $\eta : Id_{Func(K,C)} \to const colim$ in $Func(Func(K,C),Func(K,C))$ such that for every $f \in Func(K,C)$ and $Y \in C$ 
the induced morphism

$$
  Hom_{C}(colim(f),Y) \to Hom_{Func(K,C)}(const colim(f), const Y)
  \stackrel{Hom(\eta, const Y)}{\to}
  Hom_{Func(K,Y)}(f, const Y)
$$

is a weak equivalence in $sSet_{Quillen}$.


But first consider the following pointwise characterization.


**Proposition**

Let $C$ be a [[quasi-category]], $K$ a [[simplicial set]]. A co-cone diagram
$\bar p : K \star \Delta[0] \to C$ with cone point $X \in C$ 
is a colimiting diagram (an initial object in
$C_{p/}$) precisely if for every object $Y \in C$ the morphism

$$
  \phi_Y : Hom_C(X,Y) \to Hom_{Func(K,C)}(p, const Y)
$$

induced by the morpism $ p \to const X$ that is encoded by $\bar p$ is an 
equivalence (i.e. a [[homotopy equivalence]] of [[Kan complex]]es).

**Proof**

This is [[Higher Topos Theory|HTT, lemma 4.2.4.3]].

The key step is to realize that $Hom_{Func(K,C)}(p, const Y)$ is given (up to equivalence) by
the [[pullback]] $C^{p/} \times_C \{Y\}$ in [[sSet]].

Here is a detailed way to see this, 
using the discussion at [[hom-object in a quasi-category]]. 

We have that $Hom_{Func(K,C)}(p, const Y)$ is given by 
$(C^K)^{p/} \times_{C^K} const Y$. We compute

$$
  \begin{aligned}
    ((C^K)^{p/} \times_{C^K} const Y)_n
    & =
    Hom_{{\Delta[0]}/sSet}( \Delta[0] \diamondsuit \Delta[n] , C^K ) \times_{(C^K)_n} \{const Y\}
    \\
    & =
    Hom_{{\Delta[0]}/sSet}( \Delta[0] \coprod_{\Delta[n]} \Delta[n] \times \Delta[1] , C^K )
    \times_{(C^K)_n} \{const Y\}
    & =
    \{p\}
      \times_{Hom(\Delta[0],C^K)}
    Hom(\Delta[0], C^K)
      \times_{Hom(\Delta[n], C^K)}
    Hom(\Delta[n] \times \Delta[1], C^K \)
      \times_{Hom(\Delta[n], C^K)}
    \{const Y\}
    \\
    & =
    \{p\}
      \times_{Hom(K,C)}
    Hom(K,C)
      \times_{Hom(\Delta[n]\times K,C)}
    Hom(\Delta[n]\times K \times \Delta[1], C)
      \times_{Hom(\Delta[n]\times K, C)}
    Hom(\Delta[n],C)
      \times_{\Delta[n],C}
    \{Y\}
    \\
    &=
    \{p\} 
      \times_{Hom(K,C)}
    Hom(K \diamondsuit \Delta[n], C)
      \times_{Hom(\Delta[n],C)}
    \{Y\}
    \\
    &=
    (C^{p/}\times_C \{Y\})_n
  \end{aligned}
$$

Under this identification, $\phi_Y$ is the morphism

$$
  \left(
  C^{X/} 
   \stackrel{\phi'}{\to}
  C^{\bar p/}
    \stackrel{\phi''}{\to}
  C^{p/}
  \right)
  \times_C \{Y\}
  \,,
$$

in [[sSet]] where $\phi'$ is a section of the map $C^{\bar p/} \to C^{X/}$,
(which one checks is an acyclic [[Kan fibration]]) obtained by choosing composites
of the co-cone components with a given morphism $X \to Y$. 

The morphism $\phi''$ is a [[left fibration]] (using [[Higher Topos Theory|HTT, prop. 4.2.1.6]])

One finds that the morphism $\phi''$ is a [[left fibration]].

The strategy for the completion of the proof is: realize that the first condition
of the proposition is equivalent to $\phi''$ being an acyclic Kan fibration, and the
second statement equivalent to $\phi''_Y$ being an acyclic Kan fibration, then 
show that these two conditions in turn are equivalent.

**Remark**

This statement allows to relate limits in a quasi-category with [[homotopy limit]] in the corresponding [[simplicially enriched category]] as discussed at [[homotopy Kan extension]].

...

### Limits and colimits with values in $\infty Grpd$ 

Limits and colimits over a [[(∞,1)-functor]] with values in the [[(∞,1)-category]] [[∞-Grpd]] of [[∞-groupoids]] may be reformulation in terms of the  [[universal fibration of (infinity,1)-categories]].

Let [[∞-Grpd]] be the [[(∞,1)-category]] of [[∞-groupoid]]s. Let the [[(∞,1)-functor]] $Z|_{Grpd} \to \infty Grpd^{op}$ be the [[universal fibration of (infinity,1)-categories|universal ∞-groupoid fibration]] whose fiber over the object denoting some $\infty$-groupoid is that very $\infty$-groupoid.

Then let $X$ be any [[∞-groupoid]] and

$$
  F : X \to \infty Grpd
$$

an [[(∞,1)-functor]]. Recall that the [[Cartesian fibration|coCartesian fibration]] $E_F \to X$ classified by $F$ is the pullback of the [[universal fibration of (∞,1)-categories]] $Z$ along F:

$$
  \array{
    E_F &\to& Z|_{Grpd}
    \\
    \downarrow && \downarrow
    \\
    X &\stackrel{F}{\to}& \infty Grpd
  }
$$

+-- {: .un_prop }
###### Proposition

Let the assumptions be as above. Then:

* The colimit of $F$ is equivalent to $E_F$:

  $$
    E_F \simeq colim F
  $$

* The limit of $F$ is equivalent to the [[(infinity,1)-category of cartesian section|(∞,1)-groupoid of sections]] of $E_F \to X$

  $$
    \Gamma_X(E_F) \simeq lim F
    \,.
  $$

=-- 

+-- {: .proof}
###### Proof

The statement for the colimit is corollary 3.3.4.6 in [[Higher Topos Theory|HTT]]. The statement for the limit is corollary 3.3.3.4.

=--

If instead of [[∞-Grpd]] the target is the [[(∞,1)-category of (∞,1)-categories]] then the latter statement is true with the $(\infty,1)$-category of all sections replaced by [[(∞,1)-category of cartesian sections]].


### Relation to homotopy limits 

In the context of [[model categories]] and in particular for [[simplicial model categories]] there is the notion of [[homotopy limit]] and [[homotopy colimit]]. These notions are models for quasi-categorical limits and colimits.

See [[homotopy Kan extension]] for details.

+-- {: .un_prop}
###### Proposition

For $C$ and $A$ [[Kan complex]]-[[enriched categories]] and $F \in [C,A]$ an [[sSet]]-[[enriched functor]], a morphism $\eta : F \to const_q$ exhibits $q \in A$ as a homotopy colimit in $A$ in sense described at [[homotopy Kan extension]] precisely if for $N(f) : N(C) \to N(A)$ the corresponding morphism of [[quasi-categories]] under the [[homotopy coherent nerve]] and $N(f)^\triangleright : N(C)^\triangleright \to N(A)$ the extension to cones given by $\eta$, $N(f)^{\triangleright}$ is a quasi-categorical colimit diagram in the above sense.

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, theorem 4.2.4.1]].

=--

## References

The definition of limit in quasi-categories is due to

* [[André Joyal]], _Quasi-categories and Kan complexes_ Journal of Pure and Applied Algebra 175 (2002), 207-222.

A brief survey is on page 159 of

* [[André Joyal]], _The theory of quasicategories and its applications_ lectures at [Simplicial Methods in Higher Categories](http://www.crm.es/HigherCategories/), ([pdf](http://www.crm.cat/HigherCategories/hc2.pdf))


A detailed account is in [definition 1.2.13.4, p. 48](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=48) in 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ 


[[!redirects limit in a quasi-category]]
[[!redirects colimit in a quasi-category]]
[[!redirects limit in quasi-categories]]
[[!redirects limits in quasi-categories]]
[[!redirects colimit in quasi-categories]]
[[!redirects colimits in quasi-categories]]
[[!redirects limit in a quasicategory]]
[[!redirects colimit in a quasicategory]]
[[!redirects limit in quasicategories]]
[[!redirects limits in quasicategories]]
[[!redirects colimit in quasicategories]]
[[!redirects colimits in quasicategories]]
[[!redirects (infinity,1)-limit]]
[[!redirects (infinity,1)-colimit]]
[[!redirects (infinity,1)-limits]]
[[!redirects (infinity,1)-colimits]]