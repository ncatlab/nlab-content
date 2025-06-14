
> This is about [[idempotent semirings]] whose multiplication is [[idempotent]]. For idempotent semirings whose addition is idempotent, see [[additively idempotent semiring]]. 

> This article is about Boolean semirings as defined by [[Toby Bartels]]. For other notions of "Boolean semiring" or "Boolean rig", see [[Boolean semiring]]. 

----

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
=--
=--

\tableofcontents

## Idea

Recall that a [[semiring]] is a set $R$ equipped with two binary operations, denoted $+$, and $\cdot$ and called _addition_ and _multiplication_, satisfying the ring (or [[rng]]) axioms except that there may or may not be either be a zero nor a negative nor an inverse, for which reason do check.

## Definition

A [[semiring]] or [[rig]] is **(multiplicatively) idempotent** or **Boolean** if and only if multiplication is [[idempotent]]; that is, $x^2 = x$ holds for all $x \in S$.

## Terminology

From now on we will assume that semirings and rigs are synonyms of each other; i.e. the semiring, $S$, has a neutral element $\varepsilon$ for + and one $e$ for $\cdot$. Moreover we assume that for all $s\in S$, $s\cdot \varepsilon =\varepsilon \cdot s = \varepsilon$, making $S$ into a [[rig]]. 

Multiplicatively idempotent semirings are sometimes called *idempotent rigs*, see e.g. [Baez 2022](#Bartels22). However, the term *idempotent rig* and *idempotent semiring* usually refers to [[additively idempotent semirings]] in the literature, and now redirects to the disambiguation page [[idempotent semiring]] on the nLab. 

Multiplicatively idempotent semirings are called *Boolean rigs* or *Boolean semirings* by [[Toby Bartels]], see e.g. [Bartels 2020](#Bartels20). The name originated from the fact that a [[Boolean ring]] is defined in the literature as a [[ring]] for which multiplication is idempotent ([Bartels 2020](#Bartels20), [Rogers 2024](#Rogers24)). However, the terms "[[Boolean rig]]" and "[[Boolean semiring]]" have multiple meanings in the literature representing some generalization of [[Boolean rings]] from [[rings]] to [[rigs]] and [[semirings]], and now redirects to the disambiguation page [[Boolean semiring]] on the nLab. 

## Properties

Let [[CMon]] be the [[concrete category|concrete]] [[monoidal category]] of [[abelian groups]], and let $U: CMon \to Set$ be the [[lax monoidal functor|lax monoidal]] underlying-set functor. 

\begin{theorem}
Every multiplicatively idempotent rig $R$ satisfies the equation
$$1_{U(R)} = \left(U(R) \stackrel{\delta}{\to} U(R) \times U(R) \stackrel{\lambda}{\to} U(R \otimes R) \stackrel{U(mult)}{\to} U(R) \right)$$
where $\lambda$ is a lax monoidal constraint. 
\end{theorem}

## Examples

The main examples are probably [[distributive lattices]].  

Of course, a [[Boolean ring]] is a multiplicatively idempotent semiring, since any ring is a semiring.  However, since it\'s also a distributive lattice, a Boolean ring is actually a multiplicatively idempotent semiring in two different ways.

Similarly, a [[Boolean semiring (Guzmán)|Boolean semiring]] as defined by Fernando Guzmán is a multiplicatively idempotent semiring by definition. 

### Smallest multiplicatively idempotent semirings

Let’s see what are the smallest multiplicatively idempotent semirings.

- The only multiplicatively idempotent semiring of [[cardinality]] $1$ is the zero ring $0$.

There are exactly two multiplicatively idempotent semirings of cardinality $2$. In such a multiplicatively idempotent semiring, we necessarily have $0 \neq 1$, because $0=1$ would imply that $x=1 \cdot x=0 \cdot x=0$ for every $x$ and then the multiplicatively idempotent semiring would be the zero ring $0$. The two elements of the multiplicatively idempotent semirings are thus $0$ and $1$. From the axioms of a semiring, we have $0+0=0$, $1+0=0+1=1$, $0 \cdot 0=0$, $1 \cdot 0=0 \cdot 1=0$ and $1 \cdot 1=1$. We then have two possibilities for $1+1$, either $0$ or $1$. The two possibilities give a multiplicatively idempotent semiring.  

* One of the two multiplicatively idempotent semirings of cardinality $2$ is $\mathbb{Z}/2\mathbb{Z}$ ($0$ can be interpreted as "False", $1$ as "True", $+$ as the [[exclusive disjunction]] and $\cdot$ as the [[conjunction]]).
* One of the two multiplicatively idempotent semirings of cardinality $2$ is $\mathbb{B}=\{0,1\}$ where $1+1=1$ ($0$ can be interpreted as "False", $1$ as "True", $+$ as the [[disjunction]] and $\cdot$ as the [[conjunction]]).

In either case, the multiplication is commutative and distributive over addition. 

* The three-element [[distributive lattice]] $\{0, u, 1\}$ with $0 \leq u \leq 1$ is a multiplicatively idempotent semiring with cardinality $3$. 

* The four-element [[distributive lattice]] $\{0, u, v, 1\}$ with $0 \leq u \leq v \leq 1$ is a multiplicatively idempotent semiring with cardinality $4$. 

* The four-element [[distributive lattice]] $\{0, u, v, 1\}$ with $0 \leq u \leq 1$ and $0 \leq v \leq 1$ but $u$ and $v$ incomparable (i.e. $\neg (u \leq v) \wedge \neg (v \leq u)$) is a multiplicatively idempotent semiring with cardinality $4$. 

* The previous four-element distributive lattice is also a [[Boolean algebra]], and so one can define a [[Boolean ring]] structure, resulting in yet another multiplicatively idempotent semiring with cardinality $4$. 

* The [[initial object|initial]] multiplicatively idempotent semiring, i.e. the [[free object|free]] multiplicatively idempotent semiring on the [[empty set]], has cardinality $4$ ([Rogers 2024](#Rogers24)), and is defined as the quotient of the [[natural numbers]] by the relation $n + 4 \sim n + 2$. This semiring is commutative. 

One can construct a non-commutative multiplicatively idempotent semiring of cardinal $9$ ([Rogers 2024](#Rogers24)). It is currently unknown if there are any smaller non-commutative multiplicatively idempotent semirings. 

## Related concepts

* [[semiring]], [[rig]]
* [[idempotent monoid]]
* [[Boolean semiring (Guzmán)]]
* [[additively idempotent semiring]]
* [[distributive lattice]]
* [[Boolean ring]]
* [[01-bounded semilattice]]

## References

The term *(multiplcatively) idempotent* appears in:

* {#Rogers24} [[Morgan Rogers]], *From free idempotent monoids to free multiplicatively idempotent rigs* &lbrack;[arXiv:2408.17440](https://arxiv.org/abs/2408.17440)&rbrack;

The term *idempotent rig* appears in:

* {#Baez22} [[John Baez]], *Free Idempotent Rigs and Monoids*, Azimuth Blog, 21 December 2022. &lbrack;[web](https://johncarlosbaez.wordpress.com/2022/12/21/free-idempotent-rigs-and-monoids/)&rbrack;

The term *Boolean rig* was used by [[Toby Bartels]] in this current article on the nLab, before it was renamed to *multiplcatively idempotent rig*:

* {#Bartels20} [[Toby Bartels]], *Boolean rig*, 5th revision of the nLab article "[[multiplicatively idempotent rig]]", August 15, 2020. &lbrack;[nLab](https://ncatlab.org/nlab/revision/multiplicatively+idempotent+rig/5)&rbrack;

The term *Boolean rig* was also used in this Category Theory Zulip discussion:

* {#Vienney22} [[J-B Vienney]], *Are Boolean rigs commutative?*, Category theory Zulip, ([web](https://categorytheory.zulipchat.com/#narrow/channel/266967-deprecated.3A-mathematics/topic/Are.20boolean.20rigs.20commutative.3F))

[[!redirects multiplicatively idempotent]]

[[!redirects multiplicatively idempotent rig]]
[[!redirects multiplicatively idempotent rigs]]

[[!redirects multiplicatively idempotent semiring]]
[[!redirects multiplicatively idempotent semirings]]

[[!redirects Boolean semiring (Bartels)]]
[[!redirects Boolean semirings (Bartels)]]
[[!redirects boolean semiring (Bartels)]]
[[!redirects boolean semirings (Bartels)]]

[[!redirects Boolean rig (Bartels)]]
[[!redirects Boolean rigs (Bartels)]]
[[!redirects boolean rig (Bartels)]]
[[!redirects boolean rigs (Bartels)]]
