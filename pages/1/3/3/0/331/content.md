
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--


# Logic
* table of contents
{: toc}

## Idea

As a discipline, __logic__ is the study of methods of reasoning.  While in the past (and often today in philosophical circles), this discipline was prescriptive (describing how one *should* reason), it is increasingly (and usually in mathematical circles) descriptive (describing how one *does* reason).

As a (potentially) mathematical object, a __logic__ is a specific method of reasoning.  There are several ways to formalise this which for the moment we will not to get into, but maybe later.


## Category-theoretic logic

It turns out that logic is naturally expressed in the language of [[category theory]]: given any [[category]] $C$, its [[object]]s $T$ may be understood as [[type]]s of terms, and morphisms $\psi \stackrel{\Psi}{\to} T$ as [[term]]s ([[generalized element]]s of $T$). A [[proposition]] is then a [[subobject]], $\phi \hookrightarrow T$ -- the subobject of all those variables for which the proposition is true.

In summary:

* [[type theory]] deals with understanding categories in terms of their [[slice categories]], collected in their [[codomain fibration]];

* logic deals with understanding [[subobject]]s, hence [[subterminal object]]s of these slice categories.

For instance, 

* [[limit]]s and [[colimit]]s, [[exponential]]s, and [[object classifier]]s belong to the [[type theory]], 

* while [[image]]s, dual images, [[intersection]]s, [[union]]s, and [[subobject classifiers]] belong to the logic.

See also:

* [[internal language]],
* [[syntactic category]].


## Entries on logic

* [[axiom of choice]]
* [[Boolean algebra]]
* [[algebraic models for modal logics|Boolean algebra with operators]]
* [[boolean domain]]
* [[boolean function]]
* [[boolean-valued function]]
* [[classical logic]]
* [[constructive mathematics]]
* [[context]]
* [[equality]]
* [[evil]]
* [[excluded middle]]
* [[geometric logic]]
* [[Heyting algebra]]
* [[higher-order logic]]
* [[internal logic]]
* [[intuitionistic logic]]
* [[linear logic]]
* [[minimal logic]]
* [[modal logic]]

   * [[algebraic models for modal logics]]
      * [[closure algebra]]
      * [[monadic algebra]]
      * [[temporal algebra]]
   * [[arrow logic]]
   * [[epistemic logic]]
      * [[the logic K(m)]]
      * [[the logic T(m)]]
      * [[the logic S4(m)]]
      * [[the logic S5(m)]]
   * [[frame (modal logic)]]
   * [[geometric models for modal logics]]
   * [[temporal logic]]     
* [[negation]]
* [[Peirce's law]]
* [[predicate]]
* [[predicate logic]]
* [[predicative mathematics]]
* [[propositional logic]]
* [[relation]]
* [[truth value]]
* [[type]]
* [[type theory]]


## Related concepts

* [[type theory]], **logic**

* [[2-type theory]], [[2-logic]]

* [[(∞,1)-type theory]], [[(∞,1)-logic]]


## References

* [[Lambek]], J.; [[Philip Scott|Scott]], P.J. (1986), _Introduction to Higher Order Categorical Logic_, Cambridge University Press.
* [[Bart Jacobs]] (1999), _Categorical Logic and Type Theory_, Elsevier.
  

Historically, 'logic' was understood in a broader sense:

* [[Hegel]], _Wissenschaft der Logik_ ( _[[Science of Logic]]_ )


[[!redirects logic]]
[[!redirects logics]]

[[!redirects categorical logic]]
[[!redirects categorial logic]]
[[!redirects category-theoretic logic]]

[[!redirects symbolic logic]]
