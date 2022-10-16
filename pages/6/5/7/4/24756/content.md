+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

\tableofcontents

\section{Ideas}

In any [[foundations|foundational]] [[set theory]] out there, the [[sets]] and [[functions]], however defined, form a [[category]]. As a result, the set theory should have an internalization of the [[predicate logic]] used to define the [[set theory]], the [[internal logic]] of the resulting [[category of sets]] induced by the [[subsingletons]], the [[injections]], and the [[support sets]] of the set theory. This article will describe the internal logic of set theory, in the language of [[type theory#logic over type theory|predicate logic over set theory]]. 

\section{Families of sets}

We begin with the definition of [[families of sets]] and [[indexed sets]]. Recall that a [[fiber]] or [[preimage]] of a [[function]] $f$ with [[domain]] $A$ and [[codomain]] $B$ at an element $b \in B$ is the set of all elements $a \in A$ such that $f(a) = b$:

$$\{a \in A \vert f(a) = b\}$$

This could be thought of in turn as a set $S_b$ indexed by the element $b \in B$. 

$$S_b \coloneqq \{a \in A \vert f(a) = b\}$$

The whole [[collection]] of sets $(S_b)_{b \in B}$ is then the family of sets. 

\section{Indexed disjoint unions and cartesian products}

Given a family of sets $(S_i)_{i \in I}$ indexed by the set $I$, the indexed disjoint union is defined as the set of all pairs $(i, a)$ consisting of an element $i \in I$ and an element $a \in S_i$
$$\biguplus_{i \in I} S_i \coloneqq \{(i, a) \vert i \in I, a \in S_i\}$$ 
The indexed cartesian product is defined as the set of all pairs $(i, f)$ consisting of an element $i \in I$ and a [[function]] $f:I \to S_i$
$$\prod_{i \in I} S_i \coloneqq \{(i, f) \vert i \in I, f:I \to S_i\}$$ 

\section{Subsingletons and singletons}

A [[subsingleton]] is a set $S$ which has at most one element: every two elements $a \in S$ and $b \in S$ are equal to each other
$$\mathrm{isSubsingleton}(S) \coloneqq \forall a \in S.\forall b \in S. a = b$$

A [[singleton]] is a [[pointed set|pointed]] subsingleton. Equivalently, a [[singleton]] is a [[pointed set]] $S$ with specified element $a \in S$ such that every element $b \in S$ is equal to $a$, or a set $S$ where there exists an element $a \in S$ such that every element $b \in S$ is equal to $a$. 
$$\mathrm{isSingleton}(S) \coloneqq \exists a \in S.\forall b \in S. a = b$$

Every subsingleton is a [[subset]] of a [[singleton]]. 

In the internal logic of set theory, subsingletons represent the internal [[propositions]], families of subsingletons represent the internal [[predicates]], the [[empty set]] represents the internal [[truth value]] [[false]], and [[singletons]] represent the internal [[truth value]] [[true]]. 

Since any family of sets is defined by the fibers of a function $f:A \to B$, every family of subsingletons is defined such that the fibers of the function $f:A \to B$ are all subsingletons. However, that is just the requirement that the function $f:A \to B$ be an [[injection]]. Similarly, every family of singletons is equivalently just a [[bijection]] $f:A \simeq B$. 

\section{Support of a set}

Every set $S$ has a unique function $u:S \to 1$ into any [[singleton]] $1$ with point $* \in 1$, defined by $u(a) = *$ for all elements $a \in S$. 

Recall that the [[image]] of a function $f:A \to B$ is the subset of all elements $b \in B$ which are of the form $f(a)$ for all elements $a \in A$
$$\mathrm{image}(f) \coloneqq \{f(a) \vert a \in A, f:A \to B\}$$

The [[support]] of the set is defined as the [[image]] of the unique function $u:S \to 1$. 
$$[S] \coloneqq \{f(a) \vert a \in S, u:S \to 1\}$$

Since the [[image]] is always a [[subset]] of the [[codomain]] of the [[function]], the [[support]] of a set is thus a [[subsingleton]]. The support enables us to make every set $S$ into a [[subsingleton]]. 

One could also apply the support to any family of sets $(S_b)_{b \in S}$, resulting in the family of subsingletons $([S_b])_{b \in S}$. Since every family of subsingletons is equivalently an [[injection]], this is the same as the usual [[image factorization]] of every function into an [[injection]] and a [[surjection]]. 

\section{Internal logical operators}

Supports are important because they will allow us to define the logical operators [[conjunction]], [[disjunction]], [[implication]], [[logical equivalence]], [[negation]], [[existential quantification]], and [[universal quantification]] internal to the set theory:

The logical [[conjunction]] of two subsingletons is defined as the [[support]] of the [[cartesian product]] of the two subsingletons:

$$A \wedge B \coloneqq [A \times B]$$

The logical [[disjunction]] of two subsingletons is defined as the [[support]] of the [[disjoint union]] of the two subsingletons:

$$A \vee B \coloneqq [A \uplus B]$$

The logical [[implication]] of two subsingletons is defined as the [[support]] of the [[function set]] of the two subsingletons:

$$A \implies B \coloneqq [A \to B]$$

The logical [[equivalence]] of two subsingletons is defined as the [[support]] of the set of [[bijections]] of the two subsingletons:

$$A \iff B \coloneqq [A \simeq B]$$

The logical [[negation]] of a subsingleton is defined as the [[support]] of the [[function set]] into the [[empty set]]:

$$\neg A \coloneqq [A \to \emptyset]$$

The logical [[existential quantification]] of a family of subsingletons $(S_b)_{b \in B}$ ranging over the set $B$ is defined as the [[support]] of the indexed [[disjoint union]] of the family of subsingletons:

$$\exists b \in B.S_b \coloneqq \left[\biguplus_{b \in B} S_b\right]$$

The logical [[universal quantification]] of a family of subsingletons $(S_b)_{b \in B}$ ranging over the set $B$ is defined as the [[support]] of the indexed [[cartesian product]] of the family of subsingletons:

$$\forall b \in B.S_b \coloneqq \left[\prod_{b \in B} S_b\right]$$

All these operations are not restricted only to [[subsingletons]], they are also defined over general [[sets]]. However, by definition, these operations result in a [[subsingleton]]. 

\section{Internal and external axioms}

Since every logical operation in [[predicate logic]] have been internalized in the set theory itself, one then has to distinguish between the axioms written in the external predicate logic used to define the set theory, and the axioms written in the predicate logic internal to the set theory. 

For example, the external [[law of double negation]] states that for any proposition $P$ the double negation of $P$ implies $P$, $\neg \neg P \implies P$. The **internal law of double negation** would say that for every [[subsingleton]] $S$, the subsingleton $\neg \neg S \implies S$ is a [[singleton]], or equivalently, that for every set $S$ there is an element $\mathrm{doubleneg}_S \in \neg \neg [S] \implies [S]$. 

Similarly, the external [[law of excluded middle]] states that for any proposition $P$ it is possible to derive that $P \vee \neg P$. The **internal law of excluded middle** would say that for every for every [[subsingleton]] $S$, the [[subsingleton]] $S \vee \neg S$ is a singleton, or equivalently, that for every set $S$, there is a element $\mathrm{lem}_S \in[S] \vee \neg [S]$. 

\section{See also}

* [[split support]]
* [[internal logic]]
* [[dependent type theory]]
* [[propositions as types]]

[[!include types and logic - table]]