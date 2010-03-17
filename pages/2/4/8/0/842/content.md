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
  lim F := TerminalObj(C_{/F})
  \,.
$$

A **colimit** in a quasi-category is accordingly an limit in the [[opposite quasi-category]].

=--


## Special cases

### Coproducts

...

### Pushouts

...


### Coequalizers

...

### Tensoring with $\infty$-groupoids


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

+-- {: .un_prop}
###### Proposition
**(models by homotopy limits)**

Let $K$ and $C$ be categories [[enriched category|enriched]] in [[Kan complex|Kan complexes]] and $F : K \to C$ a morphism of Kan-enriched categories (i.e. an [[sSet]]-[[enriched functor]]). Then the [[homotopy limit]] of $F$ (computed for instance as described at [[weighted limit]]) coincides with the quasi-categorical limit of $F$ under [[homotopy coherent nerve]].

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