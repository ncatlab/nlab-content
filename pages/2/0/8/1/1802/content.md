The **Mitchell--B&#233;nabou language** is a particuarly simply [[internal language]] of a [[topos]] $E$; the language is a [[type theory]] $L(E)$ where:

* the **types** are the objects of $E$;
* the **variables** of type $A$ are the [[morphisms]] $x: 1 \to A$ in $E$;
* the **terms** of type $B$ in variables $x_i$ of type $X_i$ are polynomial expressions $\phi(x_1,...,x_m): 1 \to B$ in the arrows $x_i: 1 \to X_i$ in $E$;
* the **formulas** are terms of type $\Omega$, where $\Omega$ is the [[subobject classifier]];
* the logical connectives are induced from the internal [[Heyting algebra]] structure of $\Omega$;
* quantifiers bounded by types and applied to formulas are also treated;
* for each type $X$ there are also two binary relations $=_X$ (defined applying the diagonal map to the product term of the arguments) and $\in_X$ (defined applying the evaluation map to the product of the term and the power term of the arguments);
* a formula is true if the arrow which interprets it factors through the arrow $true: 1 \to \Omega$.

The Mitchell--B&#233;nabou language is a powerful way to describe various objects in a topos as if they were [[sets]] and hence is a way of making the topos into a generalized [[set theory]], to write and prove statements in a topos using first order intuitionistic predicate logic, to consider toposes as type theories and to express properties of a topos.

Any appropriate language $L$ conversely generates a [[linguistic topos]] $E(L)$.


[[!redirects Mitchell--Benabou language]]
[[!redirects Mitchell–Benabou language]]
[[!redirects Mitchell-Bénabou language]]
[[!redirects Mitchell--Bénabou language]]
[[!redirects Mitchell–Bénabou language]]