
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of _exact 2-catory_ is the analog in [[2-category theory]] of the notion of _[[exact category]]_ in [[category theory]].

## Definition

A [[regular category|regular 1-category]] is [[exact category|exact]] when every [[congruence]] has a kernel.  The definition for 2-categories is analogous.

+--{: .num_defn}
###### Definition
Let $-1\lt n\le 2$ be directed (see [[(n,r)-category]]).  A [[2-category]] is **$n$-exact** if it is [[regular 2-category|regular]] and every [[(n,r)-congruence]] is a kernel.

=--

+--{: .num_remark}
###### Remark


Recall (from [[regular 2-category]]) that a 1-category is [[regular category|regular]] as a 1-category iff it is regular as a homwise-discrete 2-category.  However, a regular 1-category is [[exact category|exact]] as a 1-category precisely when it is _1-exact_ as a 2-category.  Since general 2-congruences in a 1-category are internal categories, they will obviously not all be kernels.  This is why we add a prefix to "exact:" the best notion for 2-categories, which we call "2-exact," is not a conservative extension of the established meaning of "exact" for 1-categories.

Likewise, it is unreasonable to expect a (2,1)-category to be any more than (2,1)-exact, or a (1,2)-category to be any more than (1,2)-exact.

=--

## Examples 

* [[Cat]] is 2-exact.  Likewise, [[Gpd]] is (2,1)-exact, [[Pos]] is (1,2)-exact, and of course [[Set]] is 1-exact.

* Every regular (0,1)-category (that is, every [[meet-semilattice]]) is (0,1)-exact, and in fact even 2-exact, since there are no nontrivial congruences of any sort in a poset.

* If $K$ is 2-exact, then by the [[2-congruence|classification of congruences]], $gpd(K)$ is (2,1)-exact, $pos(K)$ is (1,2)-exact, $disc(K)$ is 1-exact, and $Sub(1)$ is (0,1)-exact.

* If $K$ is $n$-exact, then so is $K^{co}$, by the remarks about opposite [[2-congruences]].  For 1-categories and (2,1)-categories, of course, this is contentless, but for 2-categories and (1,2)-categories it is contentful.

## Properties

### Exact completion

See at _[[2-congruence]]_ the section _[Exactness](http://ncatlab.org/nlab/show/2-congruence#Exactness)_.

## References

The definition is originally due to

* [[Michael Shulman]], _[[michaelshulman:exact 2-category]]_

based on 

* [[Ross Street]], _[[StreetCBS]]_

[[!redirects exact 2-categories]]

[[!redirects 2-exact 2-category]]
[[!redirects (2,1)-exact 2-category]]
[[!redirects 1-exact 2-category]]

[[!redirects (2,1)-exact (2,1)-category]]

[[!redirects 2-exact 2-categories]]
[[!redirects (2,1)-exact 2-categories]]
[[!redirects 1-exact 2-categories]]

[[!redirects (2,1)-exact (2,1)-categories]]
