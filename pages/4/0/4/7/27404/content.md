
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

* An $\mathcal{A}$-set is **[[stable relation|stable]]** if it is both affirmative and refutative. 

* An $\mathcal{A}$-set is **[[decidable relation|decidable]]** if $x \sim y$ or $x \nsim y$. 

Thus, every setoid is an affirmative $\mathcal{A}$-set. 

In [[dependent type theory]], an $\mathcal{A}$-set is a **[[univalent setoid|univalent]] $\mathcal{A}$-set** if the canonical inductively defined function $\mathrm{idtosim}(x, y)$ from $x =_A y$ to $x \sim y$ is an [[equivalence of types]] for all $x$ and $y$ in $A$. This means that univalent $\mathcal{A}$-sets are the same as [[h-sets]] equipped with an [[irreflexive symmetric relation]], since the principle of substitution is automatically satisfied via [[transport]] across the type families $(-) \nsim z$ and $z \nsim (-)$ for all $z$ in $A$. 

### Using the type of affine propositions

An affine proposition $P$ is interpreted as a pair $(P^+, P^-)$ of propositions in intuitionistic logic which are mutually exclusive in that $\neg (P^+ \wedge P^-)$ holds. Thus, we can define the type of affine propositions as the type 
$$\Omega_\pm \coloneqq \sum_{P^+:\Omega} \sum_{P^-:\Omega} \neg (P^+ \wedge P^-) =_\Omega \top$$ 
where $\Omega$ is the [[type of all propositions]]. We usually suppress the witness that $\neg (P^+ \wedge P^-)$ and denote elements of $\Omega_\pm$ as pairs $(P^+, P^-)$. 
The logical operations for the affine logic can be defined on $\Omega_\pm$ as demonstrated [[antithesis interpretation#AffineLogicalOperations|here]]. We denote affine truth by $1:\Omega_\pm$ and affine falsehood by $0:\Omega_\pm$, to contrast with intuitionistic truth $\top:\Omega$ and falsehood $\bot:\Omega$

An $\mathcal{A}$-set is a type $A$ with an affine equivalence relation, a function $\mathrm{Eq}:A \times A \to \Omega_\pm$ with witnesses that

* for all $x:A$, $\mathrm{Eq}(x, x)$

$$\mathrm{refl}_\mathrm{Eq}:\bigsqcap_{x:A} \mathrm{Eq}(x, x) =_{\Omega_\pm} 1$$

* for all $x:A$ and $y:A$, $\mathrm{Eq}(x, y)$ implies $\mathrm{Eq}(y, x)$

$$\mathrm{sym}_\mathrm{Eq}:\bigsqcap_{x:A} \bigsqcap_{y:A} \mathrm{Eq}(x, y) \multimap \mathrm{Eq}(y, x) =_{\Omega_\pm} 1$$

* for all $x:A$, $y:A$, and $z:A$, $\mathrm{Eq}(x, y)$ multiplicatively and $\mathrm{Eq}(y, z)$ implies $\mathrm{Eq}(x, z)$

$$\mathrm{trans}_\mathrm{Eq}^{\boxtimes}:\bigsqcap_{x:A} \bigsqcap_{y:A} \bigsqcap_{z:A} \mathrm{Eq}(x, y) \boxtimes \mathrm{Eq}(y, z) \multimap \mathrm{Eq}(x, z) =_{\Omega_\pm} 1$$

An $\mathcal{A}$-set is **strong** if 

* for all $x:A$, $y:A$, and $z:A$, $\mathrm{Eq}(x, y)$ additively and $\mathrm{Eq}(y, z)$ implies $\mathrm{Eq}(x, z)$

$$\mathrm{trans}_\mathrm{Eq}^{\sqcap}:\bigsqcap_{x:A} \bigsqcap_{y:A} \bigsqcap_{z:A} \mathrm{Eq}(x, y) \sqcap \mathrm{Eq}(y, z) \multimap \mathrm{Eq}(x, z) =_{\Omega_\pm} 1$$

An $\mathcal{A}$-set is a **[[univalent setoid|univalent]] $\mathcal{A}$-set** if the canonical inductively defined function $\mathrm{idtoeq}^+(x, y)$ from $x =_A y$ to $\mathrm{El}(\pi_1(\mathrm{Eq}(x, y)))$ is an [[equivalence of types]] for all $x$ and $y$ in $A$, where $\pi_1$ is the first projection function of the first [[dependent sum type]] used in the definition of $\Omega_\pm$. Univalent $\mathcal{A}$-sets are just [[h-sets]] with an [[irreflexive symmetric relation]]. 

## Examples

Every type is an affirmative $\mathcal{A}$-set with the equivalence relation given by the [[propositional truncation]] of the [[identity type]] and the irreflexive symmetric relation given by the [[negation]] of the equivalence relation. 

* [[A-monoid]]

* [[A-group]]

* [[A-ring]]

### In ring theory

Every [[negation|non]][[trivial ring|trivial]] [[commutative ring]] $R$ is an $\mathcal{A}$-set with the equivalence relation given by [[equality]] and the irreflexive symmetric relation given by $(y - x)$ being an [[invertible element]]. In addition, 

* $R$ is a strong $\mathcal{A}$-set if and only if $R$ is a [[local ring]], 

* $R$ is a strong affirmative $\mathcal{A}$-set if and only if $R$ is a [[Kock field]], 

* $R$ is a strong refutative $\mathcal{A}$-set if and only if $R$ is a [[Heyting field]]

* $R$ is a strong decidable $\mathcal{A}$-set if and only if $R$ is a [[discrete field]]

More generally, let $R$ be a [[negation|non]][[trivial ring|trivial]] [[commutative ring]] and let $M$ be a [[multiplicative subset]] of $R$ such that $-1 \in M$ and $\neg (0 \in M)$. Then $R$ is an $\mathcal{A}$-set with the equivalence relation given by [[equality]] and the irreflexive symmetric relation given by $(y - x) \in M$. 

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