
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--

\tableofcontents

## Idea

In [[logic]] and [[type theory]], $\alpha$-equivalence is the principle that two syntactic expressions ([[types]], [[terms]], [[propositions]], [[contexts]], whatever) are equivalent for all purposes if their only difference is the renaming of bound [[variables]].

Depending on the technicalities of how variables are managed, $\alpha$-equivalence may be a necessary axiom, a provable theorem, or entirely trivial.  In any case, it is often (usually? always?) seen as a technicality devoid of conceptual interest.  However, it can be a technically nontrivial task to implement $\alpha$-conversion (which is necessary to avoid capture of free variables upon [[substitution]]) when programming logic or type theory into a computer.

## Definition

We work in a [[dependent type theory]] which acts as the metatheory for our object type theory. 

The type $\mathbb{A}$ is a [[countable set]] (and thus a [[type]] with [[decidable equality]]) whose terms are called *names* or *atoms*. The [[type]] $\mathrm{Exp}$ of *syntactic expressions* is an [[h-set]] which is inductively defined by binary functions $P:\mathrm{Exp} \times \mathrm{Exp} \to \mathrm{Exp}$ and $B([(-)](-)):\mathbb{A} \times \mathrm{Exp} \to \mathrm{Exp}$. There are dependent types $E:\mathrm{Exp} \vdash \mathrm{occ} \; \mathrm{type}$ representing the occuring atoms, $E:\mathrm{Exp} \vdash \mathrm{free} \; \mathrm{type}$ representing the free atoms, and $E:\mathrm{Exp} \vdash \mathrm{bnd} \; \mathrm{type}$ representing the bound atoms, such that for each expression $E:\mathrm{Exp}$, there are [[embeddings]] 

$$i_\mathrm{occ}(E):\mathrm{occ}(E) \hookrightarrow \mathbb{A}$$ 
$$i_\mathrm{free}(E):\mathrm{free}(E) \hookrightarrow \mathbb{A}$$ 
$$i_\mathrm{bnd}(E):\mathrm{bnd}(E) \hookrightarrow \mathbb{A}$$

which may be defined by recursion on $\mathrm{Exp}$. 

We define the following dependent types $a:\mathbb{A}, E:\mathrm{Exp} \vdash a \lhd E \; \mathrm{type}$ as 
$$a \lhd E \coloneqq \sum_{x:\mathrm{occ}(E)} i_\mathrm{occ}(E)(x) =_\mathbb{A} a$$
representing that $a$ occurs in $E$ at least once,
$$a \lhd_\mathrm{free} E \coloneqq \sum_{x:\mathrm{free}(E)} i_\mathrm{free}(E)(x) =_\mathbb{A} a$$
representing that $a$ freely occurs in $E$ at least once, and 
$$a \# E \coloneqq (a \lhd_\mathrm{free} E) \to \emptyset$$
representing that $a$ is fresh (does not freely occurs in $E$ at least once)

...

## See also

* [[equality]], [[syntactic equality]], [[definitional equality]]
* [[substitution]]
* [[rewriting]]

## References

* [[Roy L. Crole]], *Alpha equivalence equalities*, Theoretical Computer Science, Volume 433, 18 May 2012, Pages 1-19, ([doi:10.1016/j.tcs.2012.01.030](https://doi.org/10.1016/j.tcs.2012.01.030))

The distinction between $\alpha$-equivalence and syntactic equality of expressions is briefly discussed in:

* [[Benno van den Berg]], [[Martijn den Besten]], *Quadratic type checking for objective type theory* ([arXiv:2102.00905](https://arxiv.org/abs/2102.00905))

[[!redirects alpha equivalent]]
[[!redirects alpha-equivalent]]
[[!redirects α-equivalent]]
[[!redirects alpha equivalence]]
[[!redirects alpha-equivalence]]
[[!redirects α-equivalence]]
[[!redirects alpha conversion]]
[[!redirects alpha-conversion]]
[[!redirects α-conversion]]
