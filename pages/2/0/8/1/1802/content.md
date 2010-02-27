The **Mitchell--B&#233;nabou language** is a particuarly simple form of the [[internal language]] of an [[elementary topos]] $E$.  It makes use of the fact that in the presence of a [[subobject classifier]] $\Omega$, there is no need to treat formulas separately from terms, since a formula or [[proposition]] can be identified with a term of type $\Omega$.

Specifically, the language is a [[type theory]] $L(E)$ where:

* the (closed) **types** are the objects of $E$;
* the **variables** of type $A$ are the [[morphisms]] $x: 1 \to A$ in $E$;
* the **terms** of type $B$ in variables $x_i$ of type $X_i$ are morphisms from the product of the $X_i$ to $B$
* the **formulas** are terms of type $\Omega$, where $\Omega$ is the [[subobject classifier]];
* the propositional logical connectives are induced from the internal [[Heyting algebra]] structure of $\Omega$;
* the (type-bounded) quantifiers are induced from the internal completeness of $\Omega$ (i.e., the quantifiers are given by suitable morphisms from internal powers of $\Omega$ to $\Omega$)
* for each type $X$ there are also two binary relations $=_X$ (defined applying the diagonal map to the product term of the arguments) and $\in_X$ (defined applying the evaluation map to the product of the term and the power term of the arguments);
* a formula is true if the arrow which interprets it factors through the arrow $true: 1 \to \Omega$.
* one can also construct type families and dependent types, just as in any [[locally cartesian closed category]]: the types indexed by elements of some closed type $A$ are the objects of the slice category over $A$; sums and products of type families (i.e., $\Sigma$- and $\Pi$-types) are given by the left and right adjoints to change-of-base functors, respectively. As these slice categories will be topoi themselves, all the above structure can be interpreted for type families as well

The Mitchell--B&#233;nabou language, like the [[internal logic]] of any category, is a powerful way to describe various objects in a topos as if they were [[sets]].  It can be viewed as making the topos into a generalized [[set theory]] or a type theory, so that we can write and prove statements in a topos, and properties of a topos, using first order intuitionistic predicate logic.

As is usual for type theories, we can conversely generate a [[syntactic category|syntactic]] or [[free topos]] $E(L)$ from any suitable theory $L$ phrased in the above language.  The universal property of this topos says that [[logical functors]] $E(L)\to E$, for any other topos $E$, are equivalent to models of the theory $L$ in $E$.

[[!redirects Mitchell–Benabou language]]
[[!redirects Mitchell--Benabou language]]
[[!redirects Mitchell-Bénabou language]]
[[!redirects Mitchell–Bénabou language]]
[[!redirects Mitchell--Bénabou language]]
