
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Equality and Equivalence
+-- {: .hide}
[[!include equality and equivalence - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

\tableofcontents

## Definition

An **affine set** or **antithesis set** or **$\mathcal{A}$-set** is a [[setoid]] $(A, \sim)$ with an [[irreflexive symmetric relation]] $\nsim$ such that the equivalence relation satisfies the [[principle of substitution]] for the irreflexive symmetric relation in both variables: for all $x$, $y$, and $z$ in $A$, 

$$(x \sim y) \to ((x \nsim z) \to (y \nsim z)) \quad \mathrm{and} \quad (x \sim y) \to ((z \nsim x) \to (z \nsim y))$$

In addition, 

* An $\mathcal{A}$-set is **strong** if $\nsim$ is an [[apartness relation]]. 

* An $\mathcal{A}$-set is **affirmative** if $\neg (x \sim y)$ implies $x \nsim y$. 

* An $\mathcal{A}$-set is **refutative** if $\neg (x \nsim y)$ implies $x \sim y$. 

Thus, every setoid is an affirmative $\mathcal{A}$-set. 

In [[dependent type theory]], an $\mathcal{A}$-set is a **[[univalent setoid|univalent]] $\mathcal{A}$-set** if the canonical inductively defined function $\mathrm{idtosim}(x, y)$ from $x =_A y$ to $x \sim y$ is an [[equivalence of types]] for all $x$ and $y$ in $A$. This means that univalent $\mathcal{A}$-sets are the same as [[h-sets]] equipped with an [[irreflexive symmetric relation]], since the principle of substitution is automatically satisfied via [[transport]] across the type families $(-) \nsim z$ and $z \nsim (-)$ for all $z$ in $A$. 

## Examples

Every type is an affirmative $\mathcal{A}$-set with the equivalence relation given by the [[propositional truncation]] of the [[identity type]] and the irreflexive symmetric relation given by the [[negation]] of the equivalence relation. 

* [[A-monoid]]

* [[A-group]]

* [[A-ring]]

## Related concepts

* [[setoid]]

* [[irreflexive symmetric relation]]

* [[antithesis interpretation]]

* [[antithesis partial order]]

* [[A-function]]

* [[cartesian product of A-sets]]

* [[tensor product of A-sets]]

## References

* {#Shulman2022} [[Michael Shulman]], *Affine logic for constructive mathematics*. Bulletin of Symbolic Logic, Volume 28, Issue 3, September 2022. pp. 327 - 386 ([doi:10.1017/bsl.2022.28](https://doi.org/10.1017/bsl.2022.28), [arXiv:1805.07518](https://arxiv.org/abs/1805.07518))

[[!redirects affine set]]
[[!redirects affine sets]]

[[!redirects strong affine set]]
[[!redirects strong affine sets]]

[[!redirects affirmative affine set]]
[[!redirects affirmative affine sets]]

[[!redirects refutative affine set]]
[[!redirects refutative affine sets]]

[[!redirects affine h-set]]
[[!redirects affine h-sets]]

[[!redirects strong affine h-set]]
[[!redirects strong affine h-sets]]

[[!redirects affirmative affine h-set]]
[[!redirects affirmative affine h-sets]]

[[!redirects refutative affine h-set]]
[[!redirects refutative affine h-sets]]

[[!redirects univalent affine set]]
[[!redirects univalent affine sets]]

[[!redirects strong univalent affine set]]
[[!redirects strong univalent affine sets]]

[[!redirects affirmative univalent affine set]]
[[!redirects affirmative univalent affine sets]]

[[!redirects refutative univalent affine set]]
[[!redirects refutative univalent affine sets]]

[[!redirects antithesis set]]
[[!redirects antithesis sets]]

[[!redirects strong antithesis set]]
[[!redirects strong antithesis sets]]

[[!redirects affirmative antithesis set]]
[[!redirects affirmative antithesis sets]]

[[!redirects refutative antithesis set]]
[[!redirects refutative antithesis sets]]

[[!redirects antithesis h-set]]
[[!redirects antithesis h-sets]]

[[!redirects strong antithesis h-set]]
[[!redirects strong antithesis h-sets]]

[[!redirects affirmative antithesis h-set]]
[[!redirects affirmative antithesis h-sets]]

[[!redirects refutative antithesis h-set]]
[[!redirects refutative antithesis h-sets]]

[[!redirects univalent antithesis set]]
[[!redirects univalent antithesis sets]]

[[!redirects strong univalent antithesis set]]
[[!redirects strong univalent antithesis sets]]

[[!redirects affirmative univalent antithesis set]]
[[!redirects affirmative univalent antithesis sets]]

[[!redirects refutative univalent antithesis set]]
[[!redirects refutative univalent antithesis sets]]

[[!redirects A-set]]
[[!redirects A-sets]]

[[!redirects strong A-set]]
[[!redirects strong A-sets]]

[[!redirects affirmative A-set]]
[[!redirects affirmative A-sets]]

[[!redirects refutative A-set]]
[[!redirects refutative A-sets]]

[[!redirects univalent A-set]]
[[!redirects univalent A-sets]]

[[!redirects strong univalent A-set]]
[[!redirects strong univalent A-sets]]

[[!redirects affirmative univalent A-set]]
[[!redirects affirmative univalent A-sets]]

[[!redirects refutative univalent A-set]]
[[!redirects refutative univalent A-sets]]