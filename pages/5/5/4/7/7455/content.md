
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### $(\infty,2)$-Topos theory
+--{: .hide}
[[!include (infinity,2)-topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The generalization of the notion of _[[pretopos]]_ from [[category theory]] to [[2-category theory]].

## Definition 

Let $n$ be 2, (2,1), (1,2), or 1.  

+--{: .num_defn}
###### Definition

An **$n$-pretopos** is an $n$-[[exact 2-category|exact]] [[(n,r)-category|n-category]] which is also [[extensive 2-category|extensive]].  An **infinitary $n$-pretopos** is an $n$-pretopos which is infinitary-extensive.

=--

+--{: .num_remark}
###### Remark

As remarked [[coherent 2-category|here]], regularity plus extensivity implies coherency.  Thus an $n$-pretopos is, in particular, a [[coherent 2-category|coherent]] $n$-category.  Conversely, we have:

=--

+--{: .num_theorem}
###### Theorem

An $n$-category is an $n$-pretopos if and only if it is coherent and every (finitary) $n$-[[2-polycongruence|polycongruence]] is a kernel.

=--

## Examples 

* [[Cat]] is a 2-pretopos.  Likewise, [[Gpd]] is a (2,1)-pretopos and [[Pos]] is a (1,2)-pretopos.

* A 1-category is a 1-pretopos precisely when it is a [[pretopos]] in the usual sense.  Note that, as remarked for [[exact 2-category|exactness]], a 1-category is unlikely to be an $n$-pretopos for any $n\gt 1$.

* Since no nontrivial [[(0,1)-categories]] are extensive, the definition as phrased above is not reasonable for $n=(0,1)$.  However, for some purposes (such as the [[2-Giraud theorem|n-Giraud theorem]]), it is convenient to define an (infinitary) **(0,1)-pretopos** to simply be an (infinitary) coherent (0,1)-category (exactness being automatic).

## Properties

### Colimits 

An $n$-pretopos has [[2-coproducts]] and [[2-quotients]] of $n$-congruences, which are an important class of colimits.  However, it can fail to admit all finite colimits, for essentially the same reason as when $n=1$: namely, some ostensibly "finite" colimits secretly involve infinitary processes.  In a 1-category, this manifests in the construction of arbitrary coequalizers and pushouts, where we must first _generate_ an equivalence relation by an infinitary process and then take its quotient.

For 2-categories it is even easier to find counterexamples: the 1-pretopos $FinSet$ does in fact have all finite colimits, but the 2-pretopos [[FinCat]] of finite categories (that is, finitely many objects and finitely many morphisms) does not have coinserters, coinverters, or coequifiers.  (The category $FPCat$ of finitely _presented_ categories does have finite colimits, but fails to have finite limits.)

However, it is natural to conjecture that just as in the case $n=1$, once an $n$-pretopos is also countably-coherent, it does become finitely cocomplete.  See [[colimits in an n-pretopos]].

## References

This is due to 

* [[Mike Shulman]], _[[michaelshulman:2-pretopos]]_

based on 

* [[Ross Street]], _[[StreetCBS]]_

[[!redirects 2-pretopoi]]
[[!redirects 2-pretoposes]]
[[!redirects n-pretopos]]
[[!redirects n-pretopoi]]
[[!redirects n-pretoposes]]
[[!redirects infinitary 2-pretopos]]
[[!redirects infinitary 2-pretopoi]]
[[!redirects infinitary 2-pretoposes]]
[[!redirects infinitary n-pretopos]]
[[!redirects infinitary n-pretopoi]]
[[!redirects infinitary n-pretoposes]]
