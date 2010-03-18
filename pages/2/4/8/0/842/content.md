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
$$

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
**(models by homotopy limits)**

Let $K$ and $C$ be categories [[enriched category|enriched]] in [[Kan complex|Kan complexes]] and $F : K \to C$ a morphism of Kan-enriched categories (i.e. an [[sSet]]-[[enriched functor]]). Then the [[homotopy limit]] of $F$  coincides with the quasi-categorical limit of $F$ under [[homotopy coherent nerve]].

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