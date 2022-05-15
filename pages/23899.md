
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### $(\infty,1)$-Category theory
+-- {: .hide}
[[!include quasi-category theory contents]]
=--
#### $(\infty,1)$-Topos Theory
+-- {: .hide}
[[!include (infinity,1)-topos - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

In certain [[foundations of mathematics]], the "[[functions]]" between [[sets]] or [[types]] or [[presets]] do not preserve the [[equality]] in the [[set]]/[[type]]/[[preset]]. Many times, the functions that do not preserve equality are called "prefunctions", and a function is then defined to be a prefunction that satisfies [[function extensionality]]. 

## Definition 

### In set theory

Suppose that $X$ and $Y$ are [[sets]], a *prefunction* from $X$ to $Y$ is a [[mapping]] that does not preserve [[equality]]: it is [[not]] [[true]] that $a = b$ always [[implication|implies]] $f(a) = f(b)$. A function is defined as a prefunction that preserves equality; such a prefunction is said to be __extensional__.

For example, consider the identity prefunction on the set of pairs of positive numbers, $Z^+ \times Z^+$ and the set of positive fractions $Q^+$. From $Z^+ \times Z^+$ to $Q^+$, this is a function, since $a/b = c/d$ if $(a,b) = (c,d)$. But from $Q^+$ to $Z^+ \times Z^+$, it is not a function, since (for example) $2/4 = 3/6$ but $(2,4) \neq (3,6)$. A related example is the operation of taking the numerator of a (positive) fraction; from $Q^+$ to $Z^+$, we may view this as a prefunction but not as a function, although it is a function on $Z^+ \times Z^+$.

Given sets $X$ and $Y$, the [[function set]] from $X$ to $Y$ is a [[subset]] of this set of prefunctions between $X$ and $Y$. Composition of prefunctions is also possible, but likewise does not preserve equality. 

### In type theory

In many [[foundations of mathematics|foundations]] based on [[type theory]], such as in [[Martin-Löf type theory]], all [[types]] come equipped with an [[identity type]] which behaves similarly as [[equality]] does in [[Sets|sets]]. These types, therefore, are not [[presets]] in the strict sense, in that the latter do not carry any equality at all. However, [[function type|functions]] between such types usually do not satisfy [[function extensionality]], so that in the set-theoretic sense they are still like prefunctions. 


## Categorical semantics

The difference between functions and prefunctions in sets is modeled in [[category theory]] ([[categorical semantics]]) as the difference between an [[evaluational category]] (a [[concrete category]] where [[morphisms]] behave as functions do in [[Set]]) and an [[extensional category]] (which is an evaluational category where all functions preserve the equality in sets) relating equality of elements to equality of functions. 

The same difference in type theory (such as in [[intensional type theory|intensional]] [[Martin-Löf type theory]] and in [[homotopy type theory]]) is represented as concrete [[(infinity,1)-category|$(\infty,1)$-categorical]] versions of evaluational and extensional categories. These are usually internally represented by Tarski-style [[type universe|universes]] in the type theory: where the universes with the [[axiom]] of [[function extensionality]] are extensional [[locally cartesian closed (infinity,1)-categories|locally cartesian closed $(\infty,1)$-categories]], and the ones without the axiom are merely evaluational [[locally cartesian closed (infinity,1)-categories|locally cartesian closed $(\infty,1)$-categories]]. 

## See also ##

* [[preset]]

* [[universe]]

* [[function extensionality]]

* [[type theory]], [[homotopy type theory]]

* [[evaluational category]], [[extensional category]]

[[!redirects prefunction]]
[[!redirects prefunctions]]
[[!redirects pre-function]]
[[!redirects pre-functions]]