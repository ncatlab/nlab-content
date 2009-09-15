<div class="rightHandSide toc">
[[!include category theory - contents]]
</div>


A **Heyting algebra** is a [[lattice]] $L$ which as a poset admits an operation of [[implication]] 

$$\Rightarrow: L^{op} \times L \to L$$ 

satisfying the condition (really a [[universal property]])

$$(x \wedge a) \leq b \qquad if and only if \qquad x \leq (a \rightarrow b)$$ 

Alternatively, a Heyting algebra could be described as a [[partial order|poset]] which is [[finitely complete category|finitely complete]], finitely cocomplete, and cartesian closed; the implication $a\Rightarrow b$ plays the role of an [[exponential object]] $b^a$. Insofar as all these properties of a poset are described by universal properties, the Heyting algebra operations are _[[categorical operation|categorical]]_ in the sense of logic; that is, a poset can carry at most one structure of Heyting algebra. 

In logic, Heyting algebras are precisely algebraic models for [[intuitionistic logic|intuitionistic]] [[propositional calculus]], just as [[Boolean algebra|Boolean algebras]] model [[classical logic|classical]] propositional calculus. As one might guess from this description, the "law of the excluded middle" does not generally hold in a Heyting algebra; see the discussion below. 

The definition of Heyting algebra may be recast into purely equational form, and so we can speak of an [[internalization|internal]] Heyting algebra in any category with products. For example, it turns out that the [[subobject classifier]] of a [[topos]] carries an internal Heyting algebra with respect to that topos. (It is not generally an internal Boolean algebra, and this explains to a large degree why one often hears that the internal logic of a topos is intuitionistic.) 

We require Heyting algebra homomorphisms to preserve $\rightarrow$.


## Relation to topologies ##

One of the chief sources of Heyting algebras is given by [[topology|topologies]]. As a poset, the topology of a topological space $X$ is a lattice (it has arbitrary joins and meets, and therefore finite joins and meets), and the implication operator is given by 

$$(U \Rightarrow V) = int(U^c \vee V)$$ 

where $U, V$ are open sets, $U^c$ is the set-theoretic complement of $U$, and $int(S)$ denotes the interior of a subset $S \subseteq X$. 

Somewhat more generally, a [[frame]] (a [[sup-lattice]] in which finite meets distribute over arbitrary sups) also carries a Heyting algebra structure. In a frame, we may define 

$$(u \Rightarrow v) = \bigvee_{x \wedge u \leq v} x$$ 

and the distributivity property guarantees that the universal property for implication holds. (The detailed proof is a "baby" application of an [[adjoint functor theorem]].) 

Thus frames are extensionally the same thing as _[[complete lattice|complete]] Heyting algebras_. However, _intensionally_ they are quite different; that is, a morphism of frames is not usually a morphism of complete Heyting algebras: they do not preserve the implication operator. 

A [[locale]] is the same thing as a frame, but again the morphisms are different; they are reversed.

Topologies that are Boolean algebras are the exception rather than the rule; basic examples include topologies of [[Stone duality|Stone spaces]]. Another example is the topology of a [[discrete space]] $X$.


### Relation to Boolean algebras ###

In any Heyting algebra $L$, we may define a negation operator 

$$\neg: L^{op} \to L$$ 

by $\neg x = (x \Rightarrow 0)$, where $0$ is the bottom element of the lattice. A Heyting algebra is Boolean if the double negation 

$$\neg \neg: L \to L$$ 

coincides with the identity map; this gives one of many ways of defining a Boolean algebra. 

In any Heyting algebra $L$, we have for all $a, b \in L$ the inequality 

$$(\neg a \vee b) \leq (a \Rightarrow b)$$ 

and another characterization of Boolean algebra is a Heyting algebra in which this is an equality for all $a, b$. 

There are several ways of passing back and forth between Boolean algebras and Heyting algebras, having to do with the double negation operator. A useful lemma in this regard is 

+-- {: .un_lemma}
###### Lemma

The double negation $\neg \neg: L \to L$ is a [[monad]] that preserves finite meets. 
=--

The proof can be made purely equational, and is therefore internally valid in any category with products. Applied to the internal Heyting algebra $L = \Omega$ of a [[topos]], that is the [[subobject classifier]], this lemma says exactly that the double negation operator $\neg \neg: \Omega \to \Omega$ defines a Lawvere-Tierney [[site|topology]]. 

Now let $L_{\neg\neg}$ denote the poset of _regular_ elements of $L$, that is, those elements $x$ such that $\neg\neg x = x$. (When $L$ is the topology of a space, an open set $U$ is regular if and only if it is the interior of its closure.) With the help of the lemma above, we may prove

+-- {: .un_theorem}
###### Theorem

The poset $L_{\neg\neg}$ is a Boolean algebra. Moreover, the assignment $L \mapsto L_{\neg\neg}$ is the object part of a functor 
$$F: Heyt \to Bool$$
called _Booleanization_, which is left adjoint to the full and faithful inclusion 
$$i: Bool \hookrightarrow Heyt.$$
The unit of the [[adjoint functor|adjunction]], applied to a Heyting algebra $L$, is the map $L \to L_{\neg\neg}$ which maps each element $x$ to its _[[regular element|regularization]]_ $\neg\neg x$.
=--

Thus $\neg\neg: L \to L_{\neg\neg}$ preserves finite joins and finite meets and implication. In the other direction, we have an inclusion $i: L_{\neg\neg} \to L$, and this preserves meets but not joins, and negations but not implications generally. 


## Categorification

An [[elementary topos]] is a [[vertical categorification]] of a Heyting algebra.  In other words, a $0$-topos (or more precisely, a $(0,1)$-[[(0,1)-topos|topos]]) is essentially a Heyting algebra.  Note that a [[Grothendieck topos|Grothendieck]] $0$-topos is a [[locale]].


[[!redirects Heyting algebras]]