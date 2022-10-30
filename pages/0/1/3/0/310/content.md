
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{:toc}

## Definition

+-- {: .un_defn}
###### Definition

A **Heyting algebra** is a [[lattice]] $L$ which as a [[poset]] admits an operation of [[implication]] 

$$\Rightarrow: L^{op} \times L \to L$$ 

satisfying the condition (really a [[universal property]])

$$(x \wedge a) \leq b \qquad if\;and\;only\;if \qquad x \leq (a \Rightarrow b)$$ 
=--

This is equivalent to the following definition.

+-- {: .un_defn}
###### Definition

A Heyting algebra is a [[bicartesian closed category|bicartesian closed]] [[poset]], that is a poset which (when thought of as a [[thin category]]) is

* [[finitely complete category|finitely complete]], 

* finitely cocomplete, 

* and [[cartesian closed category|cartesian closed]].
=--

The implication $a\Rightarrow b$ is the [[exponential object]] $b^a$. 

+-- {: .un_remark}
###### Remark

Insofar as all these properties of a poset are described by [[universal properties]], being a Heyting algebra is a [[property-like structure]] on a poset; a poset can be a Heyting algebra in at most one way. 
=--

The definition of Heyting algebra may be recast into purely [[equational theory|equational form]], and so we can speak of an __[[internalization|internal]] Heyting algebra__ in any [[cartesian monoidal category|category with products]]. 

+-- {: .un_defn}
###### Definition

A Heyting algebra [[homomorphism]] is a homomorphism of the underlying [[lattice]]s that preserve $\Rightarrow$ .  Heyting algebras and their homomorphisms form a [[concrete category]] [[HeytAlg]].
=--


## Relation to other concepts

### To logic

In [[logic]], Heyting algebras are precisely algebraic models for [[intuitionistic logic|intuitionistic]] [[propositional calculus]], just as [[Boolean algebra|Boolean algebras]] model [[classical logic|classical]] propositional calculus. As one might guess from this description, the "law of the [[excluded middle]]" does not generally hold in a Heyting algebra; see the discussion below.

In a [[Heyting category]], every [[subobject poset]] $Sub(A)$ is a Heyting algebra.  In particular, this holds for every [[topos]].  Furthermore, in a topos, the [[power object]] $\mathcal{P}(A)$ is an internal Heyting algebra that corresponds to the external Heyting algebra $Sub(A)$.  In a [[boolean topos]], the internal Heyting algebras are all internal [[boolean algebras]].  In general, however, the [[internal logic]] of a topos (or other Heyting category) is intuitionistic.


### To topology

One of the chief sources of Heyting algebras is given by [[topology|topologies]]. As a poset, the topology of a topological space $X$ is a lattice (it has arbitrary, in particular finite joins and finite meets), and the implication operator is given by 

$$(U \Rightarrow V) = int(U^c \vee V)$$ 

where $U, V$ are open sets, $U^c$ is the set-theoretic complement of $U$, and $int(S)$ denotes the interior of a subset $S \subseteq X$. 

Somewhat more generally, a [[frame]] (a [[sup-lattice]] in which finite meets distribute over arbitrary sups) also carries a Heyting algebra structure. In a frame, we may define 

$$(u \Rightarrow v) = \bigvee_{x \wedge u \leq v} x$$ 

and the distributivity property guarantees that the universal property for implication holds. (The detailed proof is a "baby" application of an [[adjoint functor theorem]].) 

Thus frames are extensionally the same thing as _[[complete lattice|complete]] Heyting algebras_. However, _intensionally_ they are quite different; that is, a morphism of frames is not usually a morphism of complete Heyting algebras: they do not preserve the implication operator. 

A [[locale]] is the same thing as a frame, but again the morphisms are different; they are reversed.

Topologies that are Boolean algebras are the exception rather than the rule; basic examples include topologies of [[Stone duality|Stone spaces]]. Another example is the topology of a [[discrete space]] $X$.


### To Boolean algebras 

In any Heyting algebra $L$, we may define a [[negation]] operator 

$$\neg\colon L^{op} \to L$$ 

by $\neg x = (x \Rightarrow 0)$, where $0$ is the bottom element of the lattice. A Heyting algebra is Boolean if the [[double negation]] 

$$\neg \neg: L \to L$$ 

coincides with the identity map; this gives one of many ways of defining a Boolean algebra. 

In any Heyting algebra $L$, we have for all $a, b \in L$ the inequality 

$$(\neg a \vee b) \leq (a \Rightarrow b)$$ 

and another characterization of Boolean algebra is a Heyting algebra in which this is an equality for all $a, b$. 

There are several ways of passing back and forth between Boolean algebras and Heyting algebras, having to do with the [[double negation]] operator. A useful lemma in this regard is 

+-- {: .un_lemma}
###### Lemma

The double negation $\neg \neg: L \to L$ is a [[monad]] that preserves finite meets. 
=--

The proof can be made purely equational, and is therefore internally valid in any category with products. Applied to the internal Heyting algebra $L = \Omega$ of a [[topos]], that is the [[subobject classifier]], this lemma says exactly that the double negation operator $\neg \neg: \Omega \to \Omega$ defines a [[Lawvere–Tierney topology]]. Similarly, we get the [[double negation sublocale]] of any [[locale]].

Now let $L_{\neg\neg}$ denote the poset of _regular_ elements of $L$, that is, those elements $x$ such that $\neg\neg x = x$. (When $L$ is the topology of a space, an open set $U$ is regular if and only if it is the interior of its closure.) With the help of the lemma above, we may prove

+-- {: .un_theorem}
###### Theorem

The poset $L_{\neg\neg}$ is a Boolean algebra. Moreover, the assignment $L \mapsto L_{\neg\neg}$ is the object part of a functor 
$$F: Heyt \to Bool$$
called _Booleanization_, which is left adjoint to the full and faithful inclusion 
$$i: Bool \hookrightarrow Heyt.$$
The unit of the [[adjoint functor|adjunction]], applied to a Heyting algebra $L$, is the map $L \to L_{\neg\neg}$ which maps each element $x$ to its _[[regular element|regularization]]_ $\neg\neg x$.
=--

Thus $\neg\neg\colon L \to L_{\neg\neg}$ preserves finite joins and finite meets and implication. In the other direction, we have an inclusion $i\colon L_{\neg\neg} \to L$, and this preserves meets but not joins, and negations but not implications generally. 

#### Proofs 

+-- {: .proof}
###### Proof of lemma
Since $\neg \neg$ preserves order, it is clear that $\neg \neg(x \wedge y) \leq \neg \neg x$ and $\neg \neg(x \wedge y) \leq \neg \neg y$, so 
$$\neg \neg (x \wedge y) \leq (\neg \neg x) \wedge (\neg \neg y)$$  
follows. In the other direction, to show 
$$\neg \neg x \wedge \neg \neg y \leq \neg \neg (x \wedge y),$$ 
we show $(\neg \neg x) \wedge (\neg \neg y) \wedge \neg (x \wedge y) \leq 0$. But we have $\neg (x \wedge y) = (y \Rightarrow \neg x)$, and we also have the general result 
$$(a \Rightarrow b) \wedge (b \Rightarrow c) \leq (a \Rightarrow c).$$ 
Putting $a = y$, $b = \neg x$, $c = 0$, we obtain 
$$\neg (x \wedge y) \wedge (\neg \neg x) \leq \neg y$$ 
and so now 
$$\neg (x \wedge y) \wedge (\neg \neg x) \wedge (\neg \neg y) \leq (\neg y) \wedge (\neg \neg y) \leq 0$$ 
as required. 
=-- 

+-- {: .proof}
###### Proof of theorem 
Since $\neg \neg$ is a monad, and $L_{\neg \neg}$ is the corresponding category (poset) of $\neg \neg$-algebras, the left adjoint $\neg \neg \colon L \to L_{\neg \neg}$ preserves joins (and since this map is epic, this also gives the fact that $L_{\neg \neg}$ has joins). It also preserves meets by the preceding lemma, and $\neg \neg 1 = \neg 0 = 1$. So, when computed in $L_{\neg \neg}$ (where the join will be written $\vee_{\neg\neg}$ and the meet $\wedge_{\neg\neg}$), we have for any $x \in L_{\neg \neg}$ the equations 

$$x \vee_\phi \neg x = \neg \neg (x \vee \neg x) = \neg (\neg x \wedge \neg \neg x) = \neg 0 = 1$$ 

$$\,$$ 

$$x \wedge_\phi \neg x = x \wedge \neg x = 0$$ 

so that $\neg x$ is the complement of $x \in L_{\neg \neg}$. Also the distributive laws hold in $L_{\neg\neg}$ because they hold in $L$ and $L \to L_{\neg\neg}$ is a surjective map of lattices. Since $L_{\neg\neg}$ is a complemented distributive lattice, it is a Boolean algebra. 
=-- 

### To toposes


An [[elementary topos]] is a [[vertical categorification]] of a Heyting algebra: the notion of Heyting algebra is essentially equivalent to that of [[(0,1)-topos]].  Note that a [[Grothendieck topos|Grothendieck]] $(0,1)$-topos is a [[locale]].


## Examples

+-- {: .un_prop}
###### Proposition

For $\mathcal{T}$ a [[topos]] and $X \in \mathcal{T}$ any [[object]], the poset $Sub(X)$ of [[subobject]]s of $X$ is a Heyting algebra.

In other words, every topos is a [[Heyting category]].
=--

In particular for $X = \Omega$ the [[subobject classifier]], $Sub(\Omega)$ is a Heyting algebra.

In $\mathcal{T} =$ [[Set]] for every set $S$ we have that $Sub(S)$ is the [[Boolean algebra]] of subset of $S$.

More details and examples are spelled out at [[internal logic]].


[[!redirects Heyting algebra]]
[[!redirects Heyting algebras]]
