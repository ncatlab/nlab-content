The **Mitchell--B&#233;nabou language** is a particuarly simple [[internal language]] of a [[topos]] $E$; the language is a [[type theory]] $L(E)$ where:

* the (closed) **types** are the objects of $E$;
* the **variables** of type $A$ are the [[morphisms]] $x: 1 \to A$ in $E$;
* the **terms** of type $B$ in variables $x_i$ of type $X_i$ are morphisms from the product of the $X_i$ to $B$
* the **formulas** are terms of type $\Omega$, where $\Omega$ is the [[subobject classifier]];
* the propositional logical connectives are induced from the internal [[Heyting algebra]] structure of $\Omega$;
* the (type-bounded) quantifiers are induced from the internal completeness of $\Omega$ (i.e., the quantifiers are given by suitable morphisms from internal powers of $\Omega$ to $\Omega$)
* for each type $X$ there are also two binary relations $=_X$ (defined applying the diagonal map to the product term of the arguments) and $\in_X$ (defined applying the evaluation map to the product of the term and the power term of the arguments);
* a formula is true if the arrow which interprets it factors through the arrow $true: 1 \to \Omega$.
* one can also construct type families and dependent types, just as in any [[locally cartesian closed category]]: the types indexed by elements of some closed type $A$ are the objects of the slice category over $A$; sums and products of type families (i.e., $\Sigma$- and $\Pi$-types) are given by the left and right adjoints to change-of-base functors, respectively. As these slice categories will be topoi themselves, all the above structure can be interpreted for type families as well

The Mitchell--B&#233;nabou language is a powerful way to describe various objects in a topos as if they were [[sets]] and hence is a way of making the topos into a generalized [[set theory]], to write and prove statements in a topos using first order intuitionistic predicate logic, to consider toposes as type theories and to express properties of a topos.

Any intuitionistic well-termed and well-typed language $L$ conversely generates a [[linguistic topos]] $E(L)$.



[[!redirects Mitchell–Benabou language]]
[[!redirects Mitchell--Benabou language]]
[[!redirects Mitchell-Bénabou language]]
[[!redirects Mitchell–Bénabou language]]
[[!redirects Mitchell--Bénabou language]]