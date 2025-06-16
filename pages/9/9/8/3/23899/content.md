
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

In many [[foundations of mathematics|foundations]] based on [[type theory]], such as in [[Martin-Löf type theory]], all [[types]] come equipped with an [[identity type]] which behaves similarly as [[equality]] does in [[Sets|sets]]. These types, therefore, are not [[presets]] in the strict sense, in that the latter do not carry any equality at all. The [[functions]] between such sets are also not [[prefunctions]] because [[function application on identifications]] implies that functions preserve [[identifications]]. 

However, there is a way to formalize [[presets]] and [[prefunctions]] in [[dependent type theory]] even with [[identity types]]: by instead defining [[propositional equality]] as the [[predicate]] that the [[identity type]] is [[contractible]] 

$$x = y \coloneqq \mathrm{isContr}(\mathrm{Id}_A(x, y))$$

Expanding out the definition of a [[contractible type]], a witness of propositional equality consists of an [[identification]] and a [[contraction]] showing that the identification is the [[center of contraction]] of the [[identity type]]. 

By this definition of equality, propositional equality is always a [[binary relation]], because [[isContr]] is always a [[proposition]] in [[dependent type theory]]. In fact, if all identifications in an [[identity type]] are unique (i.e. there is a function $\mathrm{Id}_A(x, y) \to x = y$), then the identity type is an [[h-proposition]], and if the identity type is an [[h-proposition]], then all identifications in the identity type are unique; hence the name *[[propositional equality]]* for unique identifications and the relation $x = y$ for the type $\mathrm{isContr}(\mathrm{Id}_A(x, y))$. 

A **[[set]]** is then precisely a type where all identifications are unique. The [[uniqueness of identity proofs]] states that all identity types are propositions and all identifications are unique. 

Propositional equality satisfies the [[principle of substitution]] by [[transport]] of the unique identification across [[predicates]], and satisifes the [[identity of indiscernibles]] because propositional equality is always a proposition, and so we have:

$$\prod_{x:A} \prod_{y:A} \mathrm{isContr}(\mathrm{Id}_A(x, y)) \simeq \prod_{x:A \to \mathrm{Prop}} P(x) \simeq P(y)$$

However, propositional equality is not an [[equivalence relation]] because it is not a [[reflexive relation]]: for any [[loop space type]] which is not a [[contractible type]], the proposition $\mathrm{isContr}(\mathrm{Id}_A(x, x))$ is an [[empty type]]. The only such types with a reflexive propositional equality are thus those that satisfy [[axiom K]]: the [[h-sets]], thus making non-set types [[presets]]. 

Furthermore, every function can still be interpreted as a **prefunction** in the following sense: while functions do preserve identifications, they do not preserve propositional equality in the sense of the uniqueness of identifications. *Any* [[identification]] is given by a function out of the [[interval type]] $\mathbb{I}$, and the inductively generated identification $p:\mathrm{Id}_\mathbb{I}(0, 1)$ in the interval type is unique in $\mathrm{Id}_\mathbb{I}(0, 1)$, but not all identifications are unique in the absence of [[uniqueness of identity proofs]]. One can define an [[extensional function]] as one that does preserve the uniqueness of identifications, and prove that functions between [[h-sets]] preserve the uniqueness of identifications, and that h-sets are precisely the types between which all functions preserve uniqueness of identifications. To say that all functions are extensional along the lines of the [[preset]] approach to [[set theory]] is equivalent to the [[uniqueness of identity proofs]] that implies that all types are [[h-sets]].  

## Categorical semantics

The difference between functions and prefunctions in sets is modeled in [[category theory]] ([[categorical semantics]]) as the difference between a [[concrete category]] and a [[category]] with a functor $U:C \to Set$ which is not faithful.

## See also ##

* [[preset]]

* [[universe]]

* [[function extensionality]]

* [[type theory]], [[homotopy type theory]]

* [[propositional equality]]

[[!redirects prefunction]]
[[!redirects prefunctions]]
[[!redirects pre-function]]
[[!redirects pre-functions]]