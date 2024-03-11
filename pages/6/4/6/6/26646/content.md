This page collects a list of libraries of [[mathematics]] formalized in [[proof assistants]] using [[homotopy type theory]] and [[univalent foundations]], sorted by proof assistant.

## Coq

[[Coq]] is a proof assistant based originally on the intensional [[Calculus of Inductive Constructions]].

### Active

* [[UniMath project]].  Following the lead of Voevodsky's Foundations library (see below), UniMath generally uses only the core type constructors, such as [[Pi-types]] and [[Sigma-types]].

* [Coq-HoTT](https://github.com/HoTT/Coq-HoTT/).  This library roughly uses the type theory of the [[HoTT Book]], including higher inductive types implemented as "private" inductive types.  It also uses more advanced features of Coq such as named record types, tactics, and typeclasses.  It includes formalizations of many results in synthetic homotopy theory.

### Archived

* [[Vladimir Voevodsky]]'s [Foundations](https://github.com/vladimirias/Foundations) repository (now a part of [[UniMath|UniMath]])

* A repository of files for [Inductive types in HoTT](https://github.com/HoTT/Archive), by [[Steve Awodey]], [[Nicola Gambino]], and [[Kristina Sojakova]]. (See [this blog post](https://homotopytypetheory.org/2012/01/19/inductive-types-in-hott/).)

## Non-cubical Agda

[[Agda]] is a proof assistant based originally on intensional [[Martin-Lof Type Theory]].  By default it allows general pattern-matching which can prove [[axiom K (type theory)|axiom K]] making it incompatible with HoTT, but the `--without-K` flag turns this off.

### Active

* [Agda-UniMath](https://unimath.github.io/agda-unimath/)

* [TypeTopology](https://github.com/martinescardo/TypeTopology)

### Archived

* [HoTT-Agda](https://github.com/hott/hott-agda/)

## Cubical Agda

Agda has a `--cubical` mode that implements a version of [[cubical type theory]] that is similar to that of CCHM.  The following libraries use this feature.

### Active

* [cubical](https://github.com/agda/cubical)

* [1Lab](https://1lab.dev)

## RedTT

[RedTT](https://github.com/RedPRL/redtt) is (was?) an implementation of cartesian cubical type theory, with some basic development in an associated library.

## Arend

[Arend](https://github.com/JetBrains/Arend) implements a theory that enhances [[Book HoTT]] with an [[interval type]] similar to that of cubical type theory, but without the extra structure necessary to make univalence computational.

### Active

* [Arend Lib](https://github.com/JetBrains/arend-lib)

## Lean

[[Lean]] is a proof assistant implementing dependent type theory.  Current versions of Lean (3 and now 4) have [[UIP]] built-in and are not HoTT-compatible, but the old Lean 2 had a HoTT mode.

### Archived

* [Lean 2 HoTT Library](https://github.com/leanprover/lean2/tree/master/hott)
* [Spectral](https://github.com/cmu-phil/Spectral)
