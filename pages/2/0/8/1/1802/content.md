
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The **Mitchell--B&#233;nabou language** is a particularly simple form of the [[internal language]] of an [[elementary topos]] $E$.  It makes use of the fact that in the presence of a [[subobject classifier]] $\Omega$, there is no need to treat formulas separately from [[terms]], since a formula or [[proposition]] can be identified with a term of [[type]] $\Omega$.

Specifically, the language is a [[type theory]] $L(E)$ where:

* the (closed) **[[types]]** are the [[objects]] of $E$;

* the **[[variables]]** of type $A$ are interpreted as [[identity morphism|identity morphisms]] $\mathrm{id}_A: A \to A$ in $E$;

* the **[[terms]]** of type $B$ in variables $x_i$ of type $X_i$ are interpreted as [[morphisms]] from the product of the $X_i$ to $B$

* the **[[formulas]]** are terms of type $\Omega$, where $\Omega$ is the [[subobject classifier]];

* the [[propositional logic|propositional logical]] connectives are induced from the internal [[Heyting algebra]] structure of $\Omega$;

* the (type-bounded) [[quantifiers]] are induced from the internal completeness of $\Omega$ (i.e., the quantifiers are given by suitable morphisms from internal [[power object|powers]] of $\Omega$ to $\Omega$)

* for each type $X$ there are also two binary relations $=_X$ (defined applying the [[diagonal]] map to the [[product]] term of the arguments) and $\in_X$ (defined applying the evaluation map to the product of the term and the power term of the arguments);

* a formula is [[true]] if the arrow which interprets it factors through the arrow $true: 1 \to \Omega$.

* one can also construct type families and [[dependent types]], just as in any [[locally cartesian closed category]]: the types indexed by elements of some closed type $A$ are the objects of the [[slice category]] over $A$; [[dependent sum|sums]] and [[dependent product|products]] of type families (i.e., $\Sigma$- and $\Pi$-types) are given by the [[left adjoint|left]] and [[right adjoint]]s to [[base change|change-of-base functors]], respectively. As these slice categories will be topoi themselves, all the above structure can be interpreted for type families as well.

## Applications

The Mitchell--B&#233;nabou language, like the [[internal logic]] of any [[category]], is a powerful way to describe various objects in a topos as if they were [[sets]].  It can be viewed as making the topos into a generalized [[set theory]] or a [[type theory]], so that we can write and prove statements in a topos, and properties of a topos, using [[first order logic|first order]] [[intuitionistic logic|intuitionistic predicate logic]].

As is usual for type theories, we can conversely generate a [[syntactic category|syntactic]] or [[free topos]] $E(L)$ from any suitable theory $L$ phrased in the above language.  The universal property of this topos says that [[logical functors]] $E(L)\to E$, for any other topos $E$, are equivalent to models of the theory $L$ in $E$.


## Related concepts

* [[Kripke–Joyal semantics]]

* [[internal logic of an (infinity,1)-topos]]

## References
  {#References}

* {#MacLaneMoerdijk92} [[Saunders MacLane]], [[Ieke Moerdijk]], *[[Sheaves in Geometry and Logic]]*, Springer (1992) &lbrack;[doi:10.1007/978-1-4612-0927-0](https://link.springer.com/book/10.1007/978-1-4612-0927-0)&rbrack;

[[!redirects Mitchell-Benabou language]]
[[!redirects Mitchell–Benabou language]]
[[!redirects Mitchell--Benabou language]]
[[!redirects Mitchell-Bénabou language]]
[[!redirects Mitchell–Bénabou language]]
[[!redirects Mitchell--Bénabou language]]
[[!redirects Mitchell-Benabou languages]]
[[!redirects Mitchell–Benabou languages]]
[[!redirects Mitchell--Benabou languages]]
[[!redirects Mitchell-Bénabou languages]]
[[!redirects Mitchell–Bénabou languages]]
[[!redirects Mitchell--Bénabou languages]]

[[!redirects internal logic of a topos]]
[[!redirects internal logics of a topos]]
[[!redirects internal logic of toposes]]
[[!redirects internal logics of toposes]]
[[!redirects internal logic of topoi]]
[[!redirects internal logics of topoi]]
[[!redirects internal language of a topos]]
[[!redirects internal languages of a topos]]
[[!redirects internal language of toposes]]
[[!redirects internal languages of toposes]]
[[!redirects internal language of topoi]]
[[!redirects internal languages of topoi]]
