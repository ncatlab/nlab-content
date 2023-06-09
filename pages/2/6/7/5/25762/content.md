
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


\tableofcontents

## Idea

A *double monoid* &lbrack;[Aguiar & Mahajan (2010)](#AguiarMahajan10) or *duoid* *[Batanin & Markl (2012)](#BataninMarkl12)* is a [[set]] equipped with two compatible [[monoid]] [[structures]].

## Definitions

### With a binary operation and an element

A **duoid** is a [[set]] $D$ equipped with a [[pair]] of [[monoid]] [[structures]] $(\otimes, I)$ and $(\odot, J)$ such that:

\[
  (v \otimes x) \odot (y \otimes z) 
  \;=\; 
  (v \odot y) \otimes (x \odot z)
  \,.
\]

### In a duoidal category

See [[duoidal category]].

### As a trivial double category

A duoid is precisely a [[strict double category]] with a single [[object]], one [[horizontal morphism]], and one [[vertical morphism]].

## References

Duoids were introduced as "double monoids" in the context of [[duoidal categories]] in Definition 6.28:

* {#AguiarMahajan10} [[Marcelo Aguiar]], Swapneel Arvind Mahajan, _Monoidal functors, species and Hopf algebras_ **29** Providence, RI: American Mathematical Society (2010) &lbrack;[pdf](https://pi.math.cornell.edu/~maguiar/a.pdf), [ams:crmm-29](https://bookstore.ams.org/crmm-29)&rbrack;

They were given the name we use in:

* {#BataninMarkl12} [[Michael Batanin]], [[Martin Markl]], _Centers and homotopy centers in enriched monoidal categories_, Advances in Mathematics **230** 4-6 (2012) 1811-1858 &lbrack;[doi:10.1016/j.aim.2012.04.011](https://doi.org/10.1016/j.aim.2012.04.011)&rbrack;

as suggested by [[Ross Street]].

[[!redirects duoids]]