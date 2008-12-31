A _Heyting algebra_ is a lattice $L$ which as a poset admits a material implication operator 

$$\Rightarrow: L^{op} \times L \to L$$ 

satisfying the condition (really a universal property)

$$(x \wedge a) \leq b \qquad if and only if \qquad x \leq (a \Rightarrow b)$$ 

Alternatively, a Heyting algebra could be described as a poset which is finitely complete, finitely cocomplete, and cartesian closed; the implication $a\Rightarrow b$ plays the role of an exponential $b^a$. Insofar as all these properties of a poset are described by universal properties, the Heyting algebra operations are _categorical_ in the sense of logic; that is, a poset can carry at most one structure of Heyting algebra. 

In logic, Heyting algebras are precisely algebraic models for intuitionistic propositional calculus, just as Boolean algebras model classical propositional calculus. As one might guess from this description, the "law of the excluded middle" does not generally hold in a Heyting algebra; see the discussion below. 

The definition of Heyting algebra may be recast into purely equational form, and so we can speak of an internal Heyting algebra in any category with products. For example, it turns out that the subobject classifier of a topos carries an internal Heyting algebra with respect to that topos. (It is not generally an internal Boolean algebra, and this explains to a large degree why one often hears that the internal logic of a topos is intuitionistic.) 

### Example: topologies ### 

One of the chief sources of Heyting algebras is given by topologies. As a poset, the topology of a topological space $X$ is a lattice [it has arbitrary joins and meets, and therefore finite joins and meets], and the implication operator is given by 

$$(U \Rightarrow V) = int(\sim U \vee V)$$ 

where $U, V$ are open sets, $\sim U$ is the set-theoretic complement of $U$, and $int(S)$ denotes the interior of a subset $S \subseteq X$. 

Somewhat more generally, a locale (a sup-lattice in which finite meets distribute over arbitrary sups) also carries a Heyting algebra structure. In a locale, we may define 

$$(u \Rightarrow v) = \bigvee_{x \wedge u \leq v} x$$ 

and the distributivity guarantees that the universal property for implication holds (the detailed proof being a "baby" application of an adjoint functor theorem). 

Topologies which are actually Boolean algebras are the exception rather than the rule; the archetypal examples are topologies of Stone spaces. Another example is of course a power set $P(X)$, as the topology of a discrete space $X$. 

### Relations with Boolean algebras ###

In any Heyting algebra $L$, we may define a negation operator 

$$\neg: L^{op} \to L$$ 

by $\neg x = (x \Rightarrow 0)$, where $0$ is the bottom element of the lattice. A Heyting algebra is Boolean if the double negation 

$$\neg \neg: L \to L$$ 

coincides with the identity map; this gives one of many ways of defining a Boolean algebra. 

In any Heyting algebra $L$, we have for all $a, b \in L$ the inequality 

$$(\neg a \vee b) \leq (a \Rightarrow b)$$ 

and another characterization of Boolean algebra is a Heyting algebra in which this is an equality for all $a, b$. 

There are several ways of passing back and forth between Boolean algebras and Heyting algebras, most having to do with the double negation operator. A useful lemma in this regard is 

**Lemma:** The double negation $$\neg \neg: L \to L$$ preserves finite meets. 

With that result in hand, we have  

* The poset of _regular_ elements $x \in L$, i.e., those elements such that $\neg \neg x = x$, is a Boolean algebra denoted by $L_{\neg\neg}$. The inclusion $i: L_{\neg\neg} \to L$ preserves meets but not joins, and negations but not implications generally. 

+--{.query} 
Would like to include some material on the double negation translation and on the maximal Boolean quotient of a Heyting algebra. - Todd
=--