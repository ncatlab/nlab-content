
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Universes
+-- {: .hide}
[[!include universe - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

### In dependent type theory

In [[dependent type theory]], having a [[type of all types]] results in various paradoxes, such as [[Russell's paradox]] and [[Girard's paradox]]. There are two ways to resolve this issue. One way is to simply add a [[universe of small types]] and accept that not all types are small. On the other hand, one can use a **hierarchy of universes** or **universe hierarchy** and postulate that every type is an element of universes in this universe hierarchy: Given an universe level $\kappa$, each [[type universe]] $U_\kappa$ consists of only the $U_\kappa$-small types, and $U_\kappa$ itself, while not an element of $U_\kappa$, is an element of the successor universe $U_{\kappa^+}$, where $\kappa^+$ is the successor universe level. Most commonly used for the universe levels are the [[natural numbers]], but other options are available as well, such as the [[integers]] or the [[ordinal numbers]]. 

There are a few advantages of using a hierarchy of universes where every type is an element of the hierarchy, instead of a single separate type judgment, in the formulation of dependent type theory:

1. Having a hierarchy of universes where every type in the type theory is an element of the hierarchy of universes avoids having to use long annotations everywhere. For example, if there is a single separate type judgment where not all types are elements of types, then given the type family $x:A \vdash B(x)$, if it is not small relative to the hierarchy of universes, then the [[indexed heterogeneous identity type]], elements $a:A$, $b:A$, $p:\mathrm{Id}_A(a, b)$, $y:B(a)$, and $z:B(b)$ is represented by $\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z)$, where the subscript $x:A.B(x)$ is a long annotation used to represent the type family $x:A \vdash B(x)$. With a hierarchy of universes where every type in the type theory is an element of the hierarchy of universes, the type family $x:A \vdash B(x):U$ is represented by the function $B:A \to U$, and the same indexed heterogeneous identity type is then represented by $\mathrm{hId}_{B}(a, b, p, y, z)$, which is more concise when written out, and in addition, the subscript $B$ is now represents that the type depends upon the universe, rather than merely being an annotation, and can be written as the dependent type $\mathrm{hId}(B, a, b, p, y, z)$. 

1. In the [[split context]] formalization of [[spatial type theory]] and [[cohesive type theory]] with an additional judgment for crisp terms of types, with a hierarchy of universes, one can define crisp types by simply postulating the type to crisply be an element of a type universe. However, without [[type universes]], one has to add to the theory a separate judgment for crisp types, and all the requisite [[inference rules]], [[structural rules]], and [[congruence rules]] for crisp type judgments. 

In addition, in [[dependent type theory]] with a hierarchy of universes, 

* the [[congruence rules]] for [[substitution]] implies the [[congruence rules]] for every type in the type theory

* one can define a symbol $B$ as a type $A:U$ using the [[propositional equality]] $B =_U A$ or [[judgmental equality of terms]] $A \equiv B:U$. 

However, with a single separate judgment for types, where not all types are elements of the hierarchy of universes, not all types can be compared using judgmental equality of terms, so neither of these are possible. There are two solutions to this, both of which are unwieldy:

* One can add [[judgmental equality]] of types, and the associated [[structural rules]] for strict judgmental equality of types. However, the [[congruence rules]] for [[substitution]] no longer implies the [[congruence rules]] for every type former in the type theory, because not all types are terms of universes. Thus, the [[congruence rules]] for every type in the type theory have to be added separately. 

* Alternatively, one could add [[definitional transport]] across [[judgmental equality of terms]] as [[definitional isomorphism]], whether using the [[definitional isomorphism type]] or using the [[natural deduction]] [[inference rules]] of [[strict negative copies]]. This results in a simpler formal theory, since one doesn't need any of the structural and congruence rules for judgmental equality of types. 

* If one doesn't even have [[judgmental equality of terms]], one would need to use [[transport]] across [[identity types]] or [[path types]]. However, one needs to define [[weak equivalence of types]] and prove the congruence rules for weak equivalences of types, before weak equivalence of types could be used for definitions. Weak equivalences are significantly more complex to define, since the symbol $B \simeq A$ usually representing the [[weak equivalence type]] hasn't been formally defined in the theory yet, and any definition of [[weak equivalence type]] or [[isEquiv]] for functions is itself a very complex expression when only using [[dependent function types]], [[function types]], [[dependent pair types]], [[pair types]], and [[identity types]] in the expression. Alternatively, one can add [[natural deduction]] [[inference rules]] for $B$ as a [[positive copy]] or [[weak negative copy]] of $A$, from which one can prove that the function in the introduction rule carries the structure of a weak equivalence of types. The proofs of the various congruence rules of type formers are also very complex; see [dependent product type § typal congruence rules § using weak equivalences of types](https://ncatlab.org/nlab/show/dependent+product+type#using_weak_equivalences_of_types) for a proof of the associated congruence rule for the formation rule of dependent product types and section 11.1.6 of [Rijke22](#Rijke22) for a proof of the associated congruence rule for the formation rule of dependent sum types. 

However, this all comes at the cost of having to formalize the theory of universe levels of the hierarchy of universes before formalizing the type theory. 

## Definition

There are two main ways to define a hierarchy of universes: 

* The first way is done in dependent type theories with only a single separate type judgment, by defining a type of universe levels $\mathrm{Level}$ inside the type theory and then defining a family of [[type universes]] indexed by $\mathrm{Level}$. Not all types are elements of universes in the universe hierarchy. 

* The second way is done in dependent type theories with either no separate type judgment [[à la Russell]], or a separate type judgment for every type universe in the type theory [[à la Coquand]], where every type in the theory is an element of the hierarchy of universes. Instead of having an internal type of universe levels, one has either a separate judgment $\kappa \mathrm{level}$ which is in an untyped [[first-order theory]] or a meta-theoretic [[sort]] $\mathrm{Level}$ which is in a typed [[first-order theory]] or a [[dependent type theory]], with an operation which takes level $\kappa$ to the successor level $\kappa^+$. Then for type theories à la Russell one has for each level $\kappa$ a universe $U_\kappa:U_{\kappa^+}$, and for type theories à la Coquand one has for each level $\kappa$ a type judgment $A \; \mathrm{type}_\kappa$ and a universe $U_\kappa \; \mathrm{type}_{\kappa^+}$. 

### Cumulativity

Types of a universe $U_\kappa$ in an hierarchy of universes are also types of the successor universe $U_{\kappa^+}$; i.e. $U_\kappa$ is a [[subtype]] of $U_{\kappa^+}$. There are two different ways of representing this, reminiscent of the distinction between [[Russell universes]] and [[Tarski universes]]. 

* Given a universe level $\kappa$, the universe $U_\kappa$ is **cumulative** if given an element $A:U_\kappa$, one can derive that $A:U_{\kappa^+}$. This is similar to Russell universes in that elements of a cumulative universe $U_\kappa$ are literally elements of $U_{\kappa^+}$, similar to how elements of a Russell universe are literally types. 

* Given a universe level $\kappa$, the universe $U_\kappa$ is **non-cumulative** if given a $U_\kappa$-small type $A:U_\kappa$, one can derive that $\mathrm{Lift}_\kappa(A):U_{\kappa^+}$. This is similar to Tarski universes in that elements of a cumulative universe $U_\kappa$ are codes for elements of $U_{\kappa^+}$, represented by the family of elements $A:U_\kappa \vdash \mathrm{Lift}_\kappa(A):U_{\kappa^+}$, similar to how elements of a Tarski universe are codes for types, represented by the family of types $A:U_\kappa \vdash \mathrm{Lift}_\kappa(A) \; \mathrm{type}$. 

## Examples

Some examples of type theories with a hierarchy of universes are as follows:

* [[Coq]] uses a hierarchy of Russell universes. For practical purposes, it also has cumulativity, although there is some question (perhaps mainly semantic) of whether this is true internally or whether it uses casts that are simply hidden from the user.

* [[Agda]] uses a hierarchy of non-cumulative Russell universes.

* [UFP13](#UFP13) (first edition) uses a hierarchy of cumulative Russell universes.

* [Rijke 22](#Rijke22) uses a hierarchy of non-cumulative Tarski universes. 

## Related concepts

* [[type universe]]

* [[coercion]]

* [[reflection principle]]

## References

The hierarchy of universes is discussed in section 1.3 of:

* {#UFP13} *Homotopy Type Theory: Univalent Foundations of Mathematics*, The [[Univalent Foundations Project]], Institute for Advanced Study, 2013. ([web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf))

and in section 6.2 of:

* {#Rijke22} [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082))

[[!redirects universe hierarchy]]
[[!redirects universe hierarchies]]

[[!redirects hierarchy of universes]]
[[!redirects hierarchies of universes]]

[[!redirects hierarchy of type universes]]
[[!redirects hierarchies of type universes]]

[[!redirects hierarchy of universes of types]]
[[!redirects hierarchies of universes of types]]

[[!redirects hierarchy of types of types]]
[[!redirects hierarchies of types of types]]

[[!redirects hierarchy of types]]
[[!redirects hierarchies of types]]

[[!redirects cumulativity]]
[[!redirects cumulative]]
[[!redirects non-cumulative]]
[[!redirects noncumulative]]

[[!redirects cumulative hierarchy of universes]]
[[!redirects cumulative hierarchies of universes]]
[[!redirects non-cumulative hierarchy of universes]]
[[!redirects non-cumulative hierarchies of universes]]
[[!redirects noncumulative hierarchy of universes]]
[[!redirects noncumulative hierarchies of universes]]