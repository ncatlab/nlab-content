
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

There are various different paradigms for the interpretation of 
[[predicate logic]] in [[type theory]].  In "logic-enriched type theory", there is a separate class of "[[propositions]]" from the class of "[[types]]".  But we can also identify propositions with particular types.  In the _[[propositions as types]]_-paradigm, every proposition is a type, and also every type is identified with a proposition (the proposition that it is an [[inhabited type]]).

By contrast, in the paradigm that may be called **propositions as some types**, every proposition is a type, but not every type is a proposition.  The types which are propositions are generally those which "have at most one inhabitant" --- in [[homotopy type theory]] this is called being of [[h-level 1]] or being a [[homotopy n-type|(-1)-type]].  This paradigm is often used in the [[categorical semantics]] of type theory, such as the [[internal logic]] of various kinds of categories.

Under "propositions as types", all type-theoretic operations represent corresponding logical operations ([[dependent sum]] is the [[existential quantifier]], [[dependent product]] the [[universal quantifier]], and so on).  However, under "propositions as some types", not every such operation preserves the class of propositions; this is particularly the case for [[dependent sum]] and [[disjunction]]([[or]]).  Thus, in order to obtain the correct logical operations, we need to reflect these constructions back into propositions somehow, finding the "underlying proposition", corresponding to the [[truncated|(-1)-truncation]]/[[h-level 1|h-level 1-projection]].  This operation in type theory is called the **bracket type** (when denoted $[A]$); in [[homotopy type theory]] it can be identified with the [[higher inductive type]] $isInhab$.

## Definition

### In type theory

(...)

### In homotopy type theory
 {#DefinitionInHomotopyTypeTheory}

We discuss the definition in [[homotopy type theory]].

For $A$ a type, the **support**  of $A$ denoted $supp(A)$ or $isInhab(A)$ or $\tau_{-1} A$ or, lastly, $[A]$, is the [[higher inductive type]] defined by the two constructors

$$
  a \colon A \;\vdash \; isinhab(a) \colon supp(A)
$$

$$
  x \colon supp(A) \;,\; y \colon supp(A)
  \;\vdash \;
  inpath(x,y) \colon (x = y)
 \,,
$$

where in the last [[sequent]] on the right we have the [[identity type]]. ([Voevodsky](#Voevodsky), [HoTTLibrary](#HoTTLibrary))

This says that $supp(A)$ is the type which is [[universal property|universal]] with the property that the [[terms]] of $A$ map to it and that any two term of $A$ become [[equivalence in homotopy type theory|equivalent]] in $supp(A)$.

In [[Agda]] [[syntax]] this is

    data isinhab {i : Level} (A : Set i) : Set i where
      inhab : A &#8594; isinhab A
      inhab-path : (x y : isinhab A) &#8594; x &#8801; y



## Semantics

One presentation of the [[internal logic|internal]] [[type theory]] of 
[[regular categories]] consists of [[dependent type theory]] with the [[unit type]], 
[[strong extensional equality types]], strong [[dependent sums]], and bracket types.  (The internal logic of a regular category can alternatively be presented as a [[logic-enriched type theory]].)

The [[semantics]] of bracket types in a [[regular category]] $C$ is as follows.

A [[dependent type]] (a type in [[context]] $X$)

$$x\colon X \vdash A(x) \colon Type$$

is interpreted in $C$ as an arbitrary [[morphism]]


$$
  \array{
    A
    \\  
    \downarrow
    \\
    X
  }
  \,.
$$

The corresponding bracket type

$$ x\colon X \vdash [A(x)] \colon Type $$

is interpreted then as the [[image]]-[[(epi, mono) factorization system|factorization]] 

$$
  \array{
     A &&\to&& [A] & := im(A \to X)
     \\
     & \searrow && \swarrow
     \\
     && X
    \,.
  }
$$

Therefore $[A] \to X$ is a [[monomorphism]], and hence the interpretation of a [[proposition]] about the elements of $X$.


## Related concepts

* [[image]], [[inhabited type]]

* [[n-truncation modality]]

[[!include homotopy n-types - table]]

## References

The original articles are

* M.E. Maietti, _The Type Theory of Categorical Universes_ PhD thesis, Universit&#224; Delgi Studi di Padova, 1998

(which speaks of "mono types") and

* [[Frank Pfenning]], _Intensionality, extensionality, and proof irrelevance in modal type theory_, In Proceedings of the 16th Annual Symposium on Logic in Computer Science (LICS'01), June 2001. 

* [[Steve Awodey]], [[Andrej Bauer]], _Propositions as $[$Types$]$_, Journal of Logic and Computation. Volume 14, Issue 4, August 2004, pp. 447-471 ([pdf](http://andrej.com/papers/brackets_letter.pdf))

Exposition in the context of [[homotopy type theory]] is in 

* [[Mike Shulman]], _Minicourse on homotopy type theory_ (2012) ([web](http://www.math.ucsd.edu/~mshulman/hottminicourse2012/))
 {#Shulman}

Formalization in the context of homotopy type theory is in 

* [[Vladimir Voevodsky]], _The hProp version of the "inhabited" construction._ ([web](http://www.math.ias.edu/~vladimir/Foundations_library/hProp.html#lab140))
 {#Voevodsky}

* [[Coq]] [HoTT library](https://github.com/HoTT/HoTT/tree/master/Coq), _[IsInhab.v](https://github.com/HoTT/HoTT/blob/master/Coq/HIT/IsInhab.v)_
 {#HoTTLibrary}

Discussion of this in the more general context of truncations is in 

* [[Guillaume Brunerie]], _Truncations and truncated higher inductive types_ ([web](http://homotopytypetheory.org/2012/09/16/truncations-and-truncated-higher-inductive-types/))


[[!redirects bracket types]]
[[!redirects propositions as some types]]

[[!redirects isInhab]]
