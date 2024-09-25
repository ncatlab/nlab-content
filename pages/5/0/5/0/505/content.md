
\tableofcontents

## Definition

A **subsingleton** generally refers to a [[subset]] (of some ambient set $A$) having at most one element.  That is, it is a subset $B$ of $A$ such that any two elements of $B$ are equal.

Of course, classically any subsingleton is either [[empty set|empty]] or a [[singleton]], but [[constructive mathematics|constructively]] this need not hold.  In a [[topos]], the "object of subsingletons in $A$" is the [[partial map classifier]] for $A$, often denoted $A_\bot$.

+-- {: .num_remark}
###### Remark

Sometimes a slightly different convention is used: There what we call subsingletons are called **[[subterminal object|subterminals]]**, and a subset $B$ of $A$ is a *subsingleton* if and only if there exists an element $a \in A$ such that every element of $B$ is equal to $a$. With this nomenclature, any subsingleton is a subterminal, but the converse doesn't hold in general. (See _[[flabby sheaf]]_ for a class of examples where the converse does hold.)

=--

## Generating subsingletons from propositions

Given a proposition $P$ and a singleton $\{*\}$, one can construct the subsingleton

$$\{p \in \{*\} \vert (p = *) \wedge P\}$$

This means that one can use the set-theoretic operations to define the [[BHK interpretation]] of logic: Given two propositions $P$ and $Q$, purely $P$ or $Q$ is given by an element of the binary [[disjoint union]]

$$\{p \in \{*\} \vert (p = *) \wedge P\} \uplus \{p \in \{*\} \vert (p = *) \wedge Q\}$$

and the pure existential quantifier of a [[predicate]] $P(x)$ on a set $A$ is given by an element of the indexed [[disjoint union]]

$$\biguplus_{x \in A} \{p \in \{*\} \vert (p = *) \wedge P(x)\}$$

## Relation to the principles of omniscience

Suppose that $A$ is a subsingleton. Then the [[existential quantifier]] $\exists x.x \in A$ which says that $A$ is an [[inhabited set]] is [[logical equivalence|equivalent]] to the [[existential quantifier]] $\exists x:A.(\lambda t.1)(x) = 1$, where $\lambda t.1$ is the [[constant function]] from $A$ to the [[boolean domain]] which takes elements of $A$ to the boolean $1 \in \mathrm{bool}$. Then, one can show that various [[principles of omniscience]] are equivalent to weak versions of the [[internal logic|internal]] excluded middle, via the special case of the constant function $\lambda t.1$: 

* That the [[limited principle of omniscience]] holds for all subsingletons is equivalent to internal [[excluded middle]].

* That the [[weak limited principle of omniscience]] holds for all subsingletons is equivalent to internal [[weak excluded middle]].

* That the [[lesser limited principle of omniscience]] holds for all subsingletons is equivalent to internal [[de Morgan's law]].

* That [[Markov's principle]] holds for all subsingletons is equivalent to the internal [[double negation law]].

## See also

* [[h-proposition]]
* [[support]]
* [[decidable subsingleton]]

[[!include types and logic - table]]

[[!redirects subsingleton]]
[[!redirects subsingletons]]
[[!redirects subterminal]]
[[!redirects subterminals]]