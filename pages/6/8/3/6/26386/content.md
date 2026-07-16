
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

1. Having a hierarchy of universes where every type in the type theory is an element of the hierarchy of universes avoids having to add a theory of [[telescopes]] to the [[dependent type theory]]. For example, if there is a single separate type judgment where not all types are elements of types, then given the type family $x:A \vdash B(x)$, if it is not small relative to the hierarchy of universes, then the [[indexed heterogeneous identity type]], elements $a:A$, $b:A$, $p:\mathrm{Id}_A(a, b)$, $y:B(a)$, and $z:B(b)$ is represented by $\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z)$, where the subscript $x:A.B(x)$ is a [[telescope]] used to represent the type family $x:A \vdash B(x)$ in [[context]]. With a hierarchy of universes where every type in the type theory is an element of the hierarchy of universes, the type family $x:A \vdash B(x):U$ is represented by the function $B:A \to U$, and the same indexed heterogeneous identity type is then represented by $\mathrm{hId}_{B}(a, b, p, y, z)$, which is more concise when written out, and in addition, the subscript $B$ is now represents that the type depends upon the universe, rather than being a [[telescope]] in [[context]], and can be written as the dependent type $\mathrm{hId}(B, a, b, p, y, z)$. 

1. In the [[split context]] formalization of [[spatial type theory]] and [[cohesive type theory]] with an additional judgment for crisp terms of types, with a hierarchy of universes, one can define crisp types by simply postulating the type to crisply be an element of a type universe. However, without [[type universes]], one has to add to the theory a separate judgment for crisp types, and all the requisite [[inference rules]], [[structural rules]], and [[congruence rules]] for crisp type judgments. 

In addition, in [[dependent type theory]] with a hierarchy of universes, 

* the [[congruence rules]] for [[substitution]] implies the [[congruence rules]] for every type in the type theory

* one can define a symbol $B$ as a type $A:U$ using the [[propositional equality]] $B =_U A$ or [[judgmental equality of terms]] $A \equiv B:U$. 

However, with a single separate judgment for types, where not all types are elements of the hierarchy of universes, not all types can be compared using judgmental equality of terms, so neither of these are possible. There are two solutions to this, both of which are unwieldy:

* One can add [[judgmental equality]] of types, and the associated [[structural rules]] for strict judgmental equality of types. However, the [[congruence rules]] for [[substitution]] no longer implies the [[congruence rules]] for every type former in the type theory, because not all types are terms of universes. Thus, the [[congruence rules]] for every type in the type theory have to be added separately. 

* Alternatively, one could add [[definitional transport]] across [[judgmental equality of terms]] as [[definitional isomorphism]], whether using the [[definitional isomorphism type]] or using the [[natural deduction]] [[inference rules]] of [[strict negative copies]]. This results in a simpler formal theory, since one doesn't need any of the structural and congruence rules for judgmental equality of types. 

* If one doesn't even have [[judgmental equality of terms]], one would need to use [[transport]] across [[identity types]] or [[path types]]. However, one needs to define [[weak equivalence of types]] and prove the congruence rules for weak equivalences of types, before weak equivalence of types could be used for definitions. Weak equivalences are significantly more complex to define, since the symbol $B \simeq A$ usually representing the [[weak equivalence type]] hasn't been formally defined in the theory yet, and any definition of [[weak equivalence type]] or [[isEquiv]] for functions is itself a very complex expression when only using [[dependent function types]], [[function types]], [[dependent pair types]], [[pair types]], and [[identity types]] in the expression. Alternatively, one can add [[natural deduction]] [[inference rules]] for $B$ as a [[positive copy]] or [[weak negative copy]] of $A$, from which one can prove that the function in the introduction rule carries the structure of a weak equivalence of types. The proofs of the various congruence rules of type formers are also very complex; see [dependent product type § typal congruence rules § using weak equivalences of types](https://ncatlab.org/nlab/show/dependent+product+type#using_weak_equivalences_of_types) for a proof of the associated congruence rule for the formation rule of dependent product types and section 11.1.6 of [Rijke 2025](#Rijke25) for a proof of the associated congruence rule for the formation rule of dependent sum types. 

However, this all comes at the cost of having to formalize the theory of universe levels of the hierarchy of universes before formalizing the type theory. 

## Definition

There are two main ways to define a hierarchy of universes: 

* The first way is done in dependent type theories with only a single separate type judgment, by defining a type of universe levels $\mathrm{Level}$ inside the type theory and then defining a family of [[type universes]] indexed by $\mathrm{Level}$. 

* The second way is done in dependent type theories with either no separate type judgment [[à la Russell]] (see [Univalent Foundations Project 2013](#UFP13), [Kovács 2022](#Kovács22)), one separate type judgment (see [Sterbac & Sterling 2026](##SS26)), or a separate type judgment for every type universe in the type theory [[à la Coquand]] (see [Kovács 2022](#Kovács22)). Instead of having an internal type of universe levels, one has either a separate level [[judgment]] $\kappa \mathrm{level}$ (see [Bezem, Coquand, Dybjer, & Escardo 2023](#BCDE23)) or a meta-theoretic [[sort]] $\mathrm{Level}$ (see [Sterbac & Sterling 2026](##SS26)) for universe levels. 

### Properties of the universe levels

The universe levels of the universe hierarchy satisfy a number of properties: 

* the universe levels are ordered in some sense. How this is defined depends on the author:
  * the universe levels in [Kovács 2022](#Kovács22) come equipped with a [[well-founded relation|well-founded]] and [[transitive relation]] $\lt$.
  * the universe levels in [Sterbac & Sterling 2026](#SS26) come equipped with a [[preorder]] $\leq$ 
* the universe levels have a successor operation $\kappa \mapsto \kappa^+$ such that $\kappa \lt \kappa^+$ or $\kappa \leq \kappa^+$. Then for universe level $\kappa$, the universe $U_\kappa$ is $U_{\kappa^+}$-small or essentially $U_{\kappa^+}$-small. 

Most commonly used preorders for universe levels are the [[natural numbers]], such as in [Univalent Foundations Project 2013](#UFP13) and in the proof assistants [[Lean]], [[Agda]], and [[Rocq]]. However, the universe hierarchy used in [Rijke 2025](#Rijke25) are not indexed by the natural numbers. 

### Subtyping of universes

Types of a universe $U_\kappa$ in an hierarchy of universes are also types of the successor universe $U_{\kappa^+}$; i.e. $U_\kappa$ is a [[subtype]] of $U_{\kappa^+}$. There are two different ways of representing this, reminiscent of the distinction between [[Russell universes]] and [[Tarski universes]].

* The inclusion interpretation of subtyping of universes: given a universe level $\kappa$, the universe $U_\kappa$ is a subtype of $U_{\kappa^+}$ if given an element $A:U_\kappa$, one can derive that $A:U_{\kappa^+}$. This is similar to Russell universes in that elements of a cumulative universe $U_\kappa$ are literally elements of $U_{\kappa^+}$, similar to how elements of a Russell universe are literally types. 

* The [[coercion]] interpretation of subtyping of universes: given a universe level $\kappa$, the universe $U_\kappa$ is a subtype of $U_{\kappa^+}$ if given a $U_\kappa$-small type $A:U_\kappa$, one can derive that $\mathrm{Lift}_\kappa(A):U_{\kappa^+}$. This is similar to Tarski universes in that elements of a universe $U_\kappa$ are codes for elements of $U_{\kappa^+}$, represented by the family of elements $A:U_\kappa \vdash \mathrm{Lift}_\kappa(A):U_{\kappa^+}$, similar to how elements of a Tarski universe are codes for types, represented by the family of types $A:U_\kappa \vdash \mathrm{Lift}_\kappa(A) \; \mathrm{type}$. 

### Cumulativity

According to [Univalent Foundations Project 2013](#UFP13), a universe hierarchy is *cumulative* if given universe indices $i$ and $j$ such that $i \leq j$, types in the universe $U_i$ are also elements of the universe $U_j$. In [Sterbac & Sterling 2026](##SS26), cumulativity is defined as the following statement: 

\begin{definition}
For a hierarchy of universes $(U_\kappa, \mathrm{el}_\kappa)$ indexed by $\kappa:\mathrm{Level}$, given universe levels $i$ and $j$ where $i \leq j$ and $M:U_i$, the hierarchy is **cumulative** if one can construct $M':U_j$ such that $\mathrm{el}_i(M) \equiv \mathrm{el}_j(M')$ as types, where $\equiv$ is [[judgmental equality]]. 
\end{definition}

There are many ways to formalize cumulativity. 

* In [Univalent Foundations Project 2013](#UFP13), cumulativity of [[book HoTT]] is formalized by the following [[inference rule]]: Given the hierarchy of universes $U_\kappa$ and given universe indices $i$ and $j$ such that $i \leq j$ and $M:U_i$, one can construct the judgment $M:U_j$. 

* [Sterbac & Sterling 2026](##SS26) formalizes cumulativity of a universe hierarchy in terms of [[small|smallness]] [[judgments]] indexed by universe levels. 

## Examples

Some examples of type theories with a hierarchy of universes are as follows:

* [[Rocq]] uses a hierarchy of Russell universes indexed by the [[natural numbers]]. For practical purposes, it also has cumulativity, although there is some question (perhaps mainly semantic) of whether this is true internally or whether it uses casts that are simply hidden from the user.

* [[Agda]] uses a hierarchy of non-cumulative Russell universes indexed by the [[natural numbers]].

* [UFP13](#UFP13) (first edition) uses a hierarchy of cumulative Russell universes indexed by the [[natural numbers]].

* [Rijke 2025](#Rijke25) uses a hierarchy of non-cumulative Tarski universes that is not indexed by the [[natural numbers]]. 

## Related concepts

* [[type universe]]

* [[coercion]]

* [[reflection principle]]

## References

* {#UFP13} *Homotopy Type Theory: Univalent Foundations of Mathematics*, The [[Univalent Foundations Project]], Institute for Advanced Study, 2013. ([web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf))

* {#Kovács22} [[András Kovács]], *Generalized Universe Hierarchies and First-Class Universe Levels*, In 30th EACSL Annual Conference on Computer Science Logic (CSL 2022). Leibniz International Proceedings in Informatics (LIPIcs), Volume 216, pp. 28:1-28:17, Schloss Dagstuhl – Leibniz-Zentrum für Informatik (2022) &lbrack;[doi:10.4230/LIPIcs.CSL.2022.28](https://doi.org/10.4230/LIPIcs.CSL.2022.28)&rbrack;

* {#BCDE23} [[Marc Bezem]], [[Thierry Coquand]], [[Peter Dybjer]], [[Martín Escardó]], *Type Theory with Explicit Universe Polymorphism*, In 28th International Conference on Types for Proofs and Programs (TYPES 2022). Leibniz International Proceedings in Informatics (LIPIcs), Volume 269, pp. 13:1-13:16, Schloss Dagstuhl – Leibniz-Zentrum für Informatik (2023) &lbrack;[doi:10.4230/LIPIcs.TYPES.2022.13](https://doi.org/10.4230/LIPIcs.TYPES.2022.13)&rbrack;

* {#Rijke25} [[Egbert Rijke]]: *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press (2025) &lbrack;[doi:10.1017/9781108933568](https://doi.org/10.1017/9781108933568), [arXiv:2212.11082](https://arxiv.org/abs/2212.11082)&rbrack;

* {#SS26} [[Raphaël Sterbac]], [[Jonathan Sterling]], *Fuss-free cumulative universes: theory and practice* &lbrack;[arXiv:2607.11329](https://arxiv.org/abs/2607.11329)&rbrack;

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

[[!redirects cumulative hierarchy]]
[[!redirects cumulative hierarchies]]
[[!redirects non-cumulative hierarchy]]
[[!redirects non-cumulative hierarchies]]
[[!redirects noncumulative hierarchy]]
[[!redirects noncumulative hierarchies]]

[[!redirects cumulative universes]]
[[!redirects non-cumulative universes]]
[[!redirects noncumulative universes]]

[[!redirects cumulative hierarchy of universes]]
[[!redirects cumulative hierarchies of universes]]
[[!redirects non-cumulative hierarchy of universes]]
[[!redirects non-cumulative hierarchies of universes]]
[[!redirects noncumulative hierarchy of universes]]
[[!redirects noncumulative hierarchies of universes]]
