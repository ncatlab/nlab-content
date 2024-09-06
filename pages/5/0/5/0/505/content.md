
\tableofcontents

## Definition

A **subsingleton** generally refers to a [[subset]] (of some ambient set $A$) having at most one element.  That is, it is a subset $B$ of $A$ such that any two elements of $B$ are equal.

Of course, classically any subsingleton is either [[empty set|empty]] or a [[singleton]], but [[constructive mathematics|constructively]] this need not hold.  In a [[topos]], the "object of subsingletons in $A$" is the [[partial map classifier]] for $A$, often denoted $A_\bot$.

+-- {: .num_remark}
###### Remark

Sometimes a slightly different convention is used: There what we call subsingletons are called **[[subterminal object|subterminals]]**, and a subset $B$ of $A$ is a *subsingleton* if and only if there exists an element $a \in A$ such that every element of $B$ is equal to $a$. With this nomenclature, any subsingleton is a subterminal, but the converse doesn't hold in general. (See _[[flabby sheaf]]_ for a class of examples where the converse does hold.)

=--

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