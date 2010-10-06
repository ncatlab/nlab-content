
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


A _strict $n$-category_ is a [[strict omega-category]] all whose [[k-morphism]]s for $k \gt n$ are identities.

The category $n Cat$ of strict $n$-categories can also be defined inductively by

* starting by setting $0 Cat :=$ [[Set]]; 

* noticing that [[Set]] is canonically a (symmetric, in fact cartesian) [[closed monoidal category]] such that one can consider [[enriched category|categories enriched]] over it;

* noticing that for $V$ any [[complete category|complete]] and [[cocomplete category|cocomplete]] closed monoidal category, also $V Cat$ has these same properties;

* finally setting, recursively, 

  $$
    (n+1)Cat := n Cat Cat
    \,.
  $$

The category $Str\omega Cat$ of strict $\omega$-categories can then in turn be defined as a suitable [[limit]] of the categories $n Cat$.

A strict 1-category is just a [[category]].  [[strict 2-category|Strict 2-categories]] are also very important, because the [[coherence theorem for bicategories]] states that any weak 2-category is [[equivalence of categories|equivalent]] to a strict one, and also because many 2-categories, such as [[Cat]], are naturally strict. However, for $n\ge 3$, these two properties fail, so that strict $n$-categories become less useful (though not useless).  Instead, one needs to use (at least) [[semistrict categories]].


[[!redirects strict n-categories]]
[[!redirects strict infinity-category]]
[[!redirects strict infinity-categories]]
[[!redirects strict ∞-category]]
[[!redirects strict ∞-categories]]