+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+-- {: .hide}
[[!include (0,1)-category theory - contents]]
=--
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

\tableofcontents

## Idea

A **tight apartness relation** $\#$ is an [[apartness relation]] which is also a [[tight relation]]. Tight apartness relations is contrasted with [[denial inequality]], which is the [[negation]] of [[equality]]. In the context of [[excluded middle]], every denial inequality is a tight apartness relation, so one simply talks about "inequality". 

## Definition

### In set theory

In [[set theory]], a **tight apartness relation** on a [[set]] $S$ is a [[binary relation]] $\#$ such that 

* for all $a \in S$, $\neg(a \# a)$
* for all $a \in S$ and $b \in S$, $a \# b$ implies $b \# a$
* for all $a \in S$, $b \in S$, and $c \in S$, $a \# c$ implies that either $a \# b$ or $b \# c$
* for all $a \in S$ and $b \in S$, $a = b$ if and only if $\neg(a \# b)$  

### In dependent type theory

In [[dependent type theory]], a **tight apartness relation** on a [[set]] $S$ consists of

* a type family $a:T, b:T \vdash a \# b \; \mathrm{type}$ 
* a family of terms $a:T, b:T \vdash \mathrm{proptrunc}(a, b):\mathrm{isProp}(a \# b)$
* a family of terms $a:T \vdash \mathrm{irr}(a):(a \# a) \to \mathbb{0}$
* a family of terms $a:T, b:T \vdash \mathrm{sym}(a, b):(a \# b) \to (b \# a)$
* a family of terms $a:T, b:T, c:T \vdash \mathrm{com}(a, b, c):(a \# c) \to \left[(a \# b) + (b \# c)\right]$
* a family of terms $a:T, b:T \vdash \mathrm{tight}(a, b):\mathrm{isEquiv}(\mathrm{idtonotapart}(a, b))$ 

where $a:T, b:T \vdash \mathrm{idtonotapart}(a, b):(a =_T b) \to ((a \# b) \to \mathbb{0})$ is inductively defined by 

$$a:T \vdash \beta_{\mathrm{idtonotapart}}^{\mathrm{refl}_T}(a):\mathrm{idtonotapart}(a, a)(\mathrm{refl}_T(a)) =_{(a \# a) \to \mathbb{0}} \mathrm{irr}(a)$$

The last condition ensures that the type is an [[h-set]].

## Properties

### Strongly extensional functions

Given two sets with tight apartness relations $(S, \#)$ and $(T, \#)$, a [[function]] $f\colon S \to T$ is __[[strongly extensional function|strongly extensional]]__ if $f(x) \# f(y)$ implies $x \# y$; that is, $f$ reflects apartness. $f$ is a [[strongly injective function|strongly injective]] if $f(x) \# f(y)$ is logically equivalent to $x \# y$. The [[contrapositive]] of the both conditions imply that $f$ preserves equality and is an [[injection]] respectively. 

### Stable and decidable inequality

A tight apartness relation is stable if it is logically equivalent to [[denial inequality]]; i.e. for all elements $a \in S$ and $b \in S$, $a \neq b$ if and only if $a \# b$. Stable tight apartness is simply called "inequality", as there is no need to distinguish between tight apartness and [[denial inequality]] in this case. 

A tight apartness relation is decidable if for all elements $a \in S$ and $b \in S$, $a \# b$ or $a = b$. Decidable tight apartness implies stable tight apartness, so it is usually called decidable inequality. In the context of [[excluded middle]], every tight apartness relation is decidable. 

## The category of sets with tight apartness

In the category of sets with tight apartness, [[monomorphisms]] between sets with tight apartness are strongly extensional functions that preserve strict inequality, or strong [[injections]]. These monomorphisms are [[regular monomorphisms]]. The category of sets with tight apartness has all (small) [[limits]], [[created limit|created]] by the [[forgetful functor]] to [[Set]]. (For example, $(a,b) \# (x,y)$ iff $a \# x$ or $b \# y$.) Similarly, it has all finite [[coproducts]]. In fact, this category is a [[complete category]]. It is *not*, however, a [[Grothendieck topos]] (or even a [[topos]] at all), because it doesn\'t have all infinite coproducts. (To be precise, the statement that it has all small coproducts, or even that it has a subobject classifier, seems to be equivalent to excluded middle.) Nor is it [[finitely cocomplete]], because it does not have all [[quotients]]. 

We can say, however, that it has coproducts indexed by sets with tight apartness, although to make this precise is a triviality. More interestingly, it has products indexed by sets with tight apartness; that is, it is (even [[locally cartesian closed category|locally]]) a [[cartesian closed category]]. In particular, given sets with tight apartness $X$ and $Y$, the set $\StrExt(X,Y)$ of strongly extensional functions from $X$ to $Y$ becomes a set with tight apartness under the rule that $f \# g$ iff $f(x) \# g(x)$ for some $x\colon X$. Finally, the category of sets with tight apartness has a [[real numbers object]], the [[Dedekind real numbers]]. 

## Foundational status

### In set theory

In [[classical mathematics]], it is true that every [[set]] has a tight apartness relation. In [[constructive mathematics]], however, not all sets have tight apartness relations. Instead, one can add an axiom to the [[foundations of mathematics]] which states that every set has a tight apartness relation. 

**Axiom of tight apartness**: Every set has a tight apartness relation. 

Alternatively, one could take the tight apartness relaiton to be foundational, in which the [[axiom of extensionality]] becomes

**[[axiom of extensionality|Axiom of extensionality]]**: for any set $x$ and $y$, $\neg(x \# y)$ if and only if for all $z$, $z \in x$ if and only if $z \in y$. 

### In dependent type theory

In [[dependent type theory]], one can make every type into a set with tight apartness by adding the following set of rules to the type theory:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, a:A, b:A \vdash a \# b \; \mathrm{type}} \quad \frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, a:A, b:A \vdash \mathrm{proptrunc}(a, b):\mathrm{isProp}(a \# b)}$$
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, a:A \vdash \mathrm{irr}(a):(a \# a) \to \mathbb{0}} \quad \frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, a:A, b:A \vdash \mathrm{sym}(a, b):(a \# b) \to (b \# a)}$$
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, a:A, b:A, c:A \vdash \mathrm{comp}(a, b, c):(a \# c) \to \left[(a \# b) + (b \# c)\right]}$$
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, a:A, b:A \vdash \mathrm{idtonotapart}(a, b):(a =_A b) \to ((a \# b) \to \mathbb{0})}$$ 
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, a:A \vdash \mathrm{idtonotapart}(a, a)(\mathrm{refl}_A(a)) \equiv \mathrm{irr}(a):(a \# a) \to \mathbb{0}}$$
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, a:A, b:A \vdash \mathrm{tight}(a, b):\mathrm{isEquiv}(\mathrm{idtonotapart}(a, b))}$$

This implies [[axiom K]] and [[uniqueness of identity proofs]]. 

### Omniscience principles

There are also generalisations of the [[principles of omniscience]] involving sets with tight apartness:

* Every set with tight apartness has [[decidable tight apartness]], which generalises [[LPO]] and [[analytic LPO]]

* Every set with tight apartness has [[decidable equality]], which generalises [[WLPO]] and [[analytic WLPO]]

* Every set with tight apartness has [[stable relation|stable]] [[tight apartness]], which generalises [[Markov's principle]] and [[analytic Markov's principle]]

The first one is equivalent to the [[category of sets]] being a [[boolean category]], since given a [[subsingleton]] $S$, that the function set $S \to \mathbb{2}$ from $S$ to the [[boolean domain]] $\mathbb{2}$ has decidable tight apartness is equivalent to $S$ being either a [[singleton]] or an [[empty set]], which is precisely the condition that [[Set]] is a boolean category. 

The latter two are all still weaker than [[Set]] being a [[boolean category]] since in general, the [[set of truth values]] is only an set with tight apartness if and only if [[excluded middle]] holds. 

## In algebra

Since sets with tight apartness have finite limits, the usual constructions of [[universal algebra]] apply; it\'s straightforward to define strong refutative inequality [[groups]], strong refutative inequality [[rings]], and so on.

The various subsets that appear in algebra (such as [[subgroups]], [[ideals]], and [[cosets]]) become less fundamental than certain subsets that are, classically, simply their complements. For example, a left ideal in a ring $R$ is a subset $I$ such that $0 \in I$, $x + y \in I$ whenever $x, y \in I$, and $x y \in I$ whenever $x \in I$. But a left _[[antiideal]]_ in an inequality ring $R$ is an $\#$-open subset $A$ such that $0 \in A$ is false, $x \in A$ or $y \in A$ whenever $x + y \in A$, and $x \in A$ whenever $x y \in A$.  (The $\#$-openness requirement is automatic if $\neg(0\in A)$ is strengthened to $p\# 0$ for all $p\in A$, using that the ring operations are strongly extensional.)  Note that the complement of an antiideal is an ideal, but not every ideal can be constructively shown to be the complement of an antiideal; so antiideals are more fundamental than ideals, in an inequality ring.

[[prime ideal|Prime ideals]] are even more interesting. A two-sided antiideal $A$ (so also satisfying that $y \in A$ whenever $x y \in A$) is _antiprime_ (or simply _prime_ if no confusion is expected) if $1 \in A$ and $x y \in A$ whenever $x, y \in A$. Now the complement of an antiprime antiideal may *not* be a prime ideal (as normally defined). But in fact, it is antiprime antiideals that are more important in constructive algebra. In particular, an [[integral domain]] in constructive algebra is an inequality ring in which the antiideal of nonzero elements is antiprime.

Any [[apartness relation]] on a set with tight apartness $X$ is the same as the (strongly) [[closed subspace|closed]] [[equivalence relation]] on the discrete locale $X$. This localic perspective on [[apartness relations]] extends naturally to anti-algebra: an antiideal is the same as a *closed* ideal in a discrete localic ring that respects the closed equivalence relation corresponding to $\#$. Equivalently, this is a closed ideal of the $\#$-topology regarded as a (non-discrete) localic ring.  The spatial part of this closed localic ideal is then the ordinary ideal complementary to the antiideal, and so on.  Moreover, since unions of closed sublocales correspond to intersections of their open complements, an antiideal $A$ is antiprime exactly when its corresponding closed localic ideal $\mathsf{C}A$ is "prime" in an appropriate internal sense in [[Loc]], namely that $m^*(\mathsf{C}A) \subseteq (\mathsf{C}A \times R) \cup (R\times \mathsf{C}A)$, where $m:R\times R\to R$ is the multiplication.  The fact that the complement of an antiprime antiideal need not be prime in the usual sense corresponds to the fact that taking the spatial part of sublocales doesn't commute with unions.

For more about apartness algebra, see [[antisubalgebra]].

## Related concepts

* [[denial inequality]]

* [[strict total order]]

* [[classical set]]

## References

* {#TvD} Anne Troelstra\'s and Dirk van Dalen\'s _Constructivism in Mathematics_ (1988) uses  "preapartness" and "apartness" instead of "apartness" and "tight apartness" respectively.

* {#Shulman2022} [[Michael Shulman]], *Affine logic for constructive mathematics*. Bulletin of Symbolic Logic, Volume 28, Issue 3, September 2022. pp. 327 - 386 ([doi:10.1017/bsl.2022.28](https://doi.org/10.1017/bsl.2022.28), [arXiv:1805.07518](https://arxiv.org/abs/1805.07518))

[[!redirects tight apartness]]
[[!redirects tight apartnesses]]
[[!redirects tight apartness structure]]
[[!redirects tight apartness structures]]
[[!redirects tight apartness relation]]
[[!redirects tight apartness relations]]

[[!redirects connected apartness]]
[[!redirects connected apartnesses]]
[[!redirects connected apartness structure]]
[[!redirects connected apartness structures]]
[[!redirects connected apartness relation]]
[[!redirects connected apartness relations]]

[[!redirects set with tight apartness]]
[[!redirects sets with tight apartness]]

[[!redirects set with a tight apartness relation]]
[[!redirects sets with a tight apartness relation]]

[[!redirects category of sets with tight apartness]]
[[!redirects categories of sets with tight apartness]]

[[!redirects category of sets with a tight apartness relation]]
[[!redirects categories of sets with a tight apartness relation]]

[[!redirects axiom of tight apartness]]
[[!redirects axioms of tight apartness]]
