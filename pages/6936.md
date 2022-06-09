
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Induction
+-- {: .hide}
[[!include induction - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

*Higher inductive types* (HITs) are a generalization of [[inductive types]] which allow the constructors to produce, not just points of the type being defined, but also elements of its iterated [[identity types]].

While HITs are already useful in [[extensional type theory]], they are most useful and powerful in [[homotopy type theory]], where they allow the construction of [[cell complexes]], [[homotopy colimits]], [[n-truncated|truncations]], [[Bousfield localization of model categories|localizations]], and many other objects from classical [[homotopy theory]].

Defining what a HIT is "in general" is an open research problem.  One mostly precise proposal may be found in ([ShulmanLumsdaine16](#ShulmanLumsdaine16)).  A more syntactic description of a class of HITs may be found in ([Brunerie16](#Brunerie16)). A solution to this problem should determine how to define the concept of an [[elementary (∞,1)-topos]].

See also [[homotopytypetheory:higher inductive type]].

## Examples

All higher inductive types described below are given together with some pseudo-[[Coq]] code, which would implement that HIT if Coq supported HITs natively.

### The circle
 {#ExamplesTheCircle}

The [[circle type]] is:

    Inductive circle : Type :=
    | base : circle
    | loop : base == base.

Using the [[univalence axiom]], one can prove that the [[loop space]] `base == base` of the circle type is equivalent to the [[integers]].

([Licata & Shulman 13](circle#LicataShulman13), [Bezem, Buchholtz, Grayson & Shulman 19](circle#BezemBuchholtzGraysonShulman19)). 



### The interval

The [[homotopy type]] of the [[interval]] can be encoded as

    Inductive interval : Type :=
    | zero : interval
    | one : interval
    | segment : zero == one.

See [[interval type]].  The interval can be proven to be [[contractible type|contractible]].  On the other hand, if the constructors `zero` and `one` satisfy their elimination rules definitionally, then the existence of an interval type implies [[function extensionality]]; see [this blog post](http://homotopytypetheory.org/2011/04/04/an-interval-type-implies-function-extensionality/).
The interval can be defined as the -1-truncation of the booleans; see [here](https://groups.google.com/d/msg/homotopytypetheory/-5mLEi_qMTo/gpNUsmI-ZT4J): 

    Inductive interval : Type :=
    | inj : boolean -> interval
    | contr0 : forall (p q : interval) p == q

Or more directly: 

    Inductive interval : Type :=
    | zero : interval
    | one : interval
    | contr0 : forall (p q : interval) p == q

### The 2-sphere

Similarly the [[homotopy type]] of the 2-[[dimensional]] [[sphere]]

    Inductive sphere2 : Type :=
    | base2 : sphere2
    | surf2 : idpath base2 == idpath base2.

### Suspension

    Inductive susp (X : Type) : Type :=
    | north : susp X
    | south : susp X
    | merid : X -> north == south.

This is the unpointed [[suspension]].  It is also possible to define the pointed suspension.  Using either one, we can define the $n$-sphere by induction on $n$, since $S^{n+1}$ is the suspension of $S^n$.

### Mapping cylinders
 {#MappingCylinders}

The construction of [[mapping cylinders]] is given by

    Inductive cyl {X Y : Type} (f : X -> Y) : Y -> Type :=
    | cyl_base : forall y:Y, cyl f y
    | cyl_top : forall x:X, cyl f (f x)
    | cyl_seg : forall x:X, cyl_top x == cyl_base (f x).

Using this construction, one can define a (cofibration, trivial fibration) [[weak factorization system]] for types.

### Truncation


    Inductive is_inhab (A : Type) : Type :=
    | inhab : A -> is_inhab A
    | inhab_path : forall (x y: is_inhab A), x == y.

This is the [[(-1)-truncated|(-1)-truncation]] into [[h-propositions]].  One can prove that `is_inhab A` is always a [[proposition]] (i.e. $(-1)$-truncated) and that it is the reflection of $A$ into propositions.  More generally, one can construct the [[(effective epi, mono) factorization system]] by applying `is_inhab` fiberwise to a fibration.

Similarly, we have the [[0-truncated|0-truncation]] into [[h-sets]]:

    Inductive pi0 (X:Type) : Type :=
    | cpnt : X -> pi0 X
    | pi0_axiomK : forall (l : Circle -> pi0 X), refl (l base) == map l loop.

We can similarly define $n$-truncation for any $n$, and we should be able to define it inductively for all $n$ at once as well.

See at _[[n-truncation modality]]_.

### Pushouts

The (homotopy) [[homotopy pushout|pushout]] of $f \colon A\to B$ and $g\colon A\to C$:

    Inductive hpushout {A B C : Type} (f : A -> B) (g : A -> C) : Type :=
    | inl : B -> hpushout f g
    | inr : C -> hpushout f g
    | glue : forall (a : A), inl (f a) == inr (g a).

### Quotients of types
 {#QuotientsOfTypes}

The [[quotient]] of a pure or Type-valued [[equivalence relation]]:

    Inductive quotient (A : Type) (R : A -> A -> Type) : Type :=
    | proj : A -> quotient A R
    | relate : forall (x y : A), R x y -> proj x == proj y

This definition is translated into Coq from the Cubical Agda library. 

### Disjunctions

The [[disjunction]] of two types $A$ and $B$, yielding an [[hProp]]: 

    Inductive disjunction (A B:Type) : Type :=
    | inl : A -> disjunction A B
    | inr : B -> disjunction A B.
    | contr0 : forall (p q : disjunction A B) p == q

### Existential quantifiers

The [[existential quantifier]] of a type $A$ and a type family $B:A \to Type$, yielding an [[hProp]]: 

    Inductive existquant (A:Type) (B:A->Type) : Type :=
    | exist : forall (x:A), B x -> existquant A B
    | contr0 : forall (p q : existquant A B) p == q

### Quotients of sets
 {#QuotientsOfSets}

The [[quotient]] of an [[hProp]]-value [[equivalence relation]], yielding an [[hSet]] (a [[0-truncated]] type):

    Inductive quotient (A : Type) (R : A -> A -> hProp) : Type :=
    | proj : A -> quotient A R
    | relate : forall (x y : A), R x y -> proj x == proj y
    | contr1 : forall (x y : quotient A R) (p q : x == y), p == q.

This is already interesting in [[extensional type theory]], where [[quotient types]] are not always included.  For more general homotopical quotients of "[[internal groupoids]]" as in the  [[(∞,1)-Giraud theorem]], we first need a good definition of what such an internal groupoid is.

### Quotient inductive types

A [[quotient inductive type]] is a higher inductive type that includes a "0-truncation" constructor such as `contr1` for a set-quotient.  Many of these are useful in set-based mathematics; in addition to colimits in [[Set]], they can be used to construct free algebras and colimits of algebras of various sorts. Quotient [[inductive-inductive types]] are used to construct sets with [[proposition|propositional]] [[relations]] and various [[countable]] [[completions]] of structures. Examples can be found at [[quotient inductive type]], including:

* multiple definitions of the [[integers]]
* [[polynomial rings]]
* [[Sierpinski space]]
* the [[cumulative hierarchy]]
* the [[Cauchy real numbers]]
* [[partial map classifiers]]
* [[internal type theory]]

### FinSet

Since [[FinSet]] is the initial [[2-rig]], one should be able to construct it as a higher inductive type with a [[1-truncation]] constructor. 

### Integers

A definition of the set of [[integers]] as a higher inductive type. 

    Inductive int : Type :=
    | zero : int
    | succ : int -> int
    | pred1 : int -> int
    | pred2 : int -> int
    | sec : forall (x : int) pred1 succ x == x
    | ret : forall (x : int) succ pred2 x == x

### Other

* [[circle type]]

* [[sphere type]]

* [[cone type]]

* [[square type]]

* [[suspension type]]

* [[localization of a type at a family of functions]]

* [[Eilenberg-MacLane space type]]

* [[spectrification of a sequential spectrum type]]

* [[James construction type]]

* [[Rezk completion]]

## Semantics
See ([Lumsdaine-Shulman17](#LumsdaineShulman17)).

## Related concepts

* [[inductive type]], [[initial algebra of an endofunctor]]

* **higher inductive type**, [[initial algebra of a presentable ∞-monad]]

* [[quotient inductive type]]


## References

Expositions include

* [[Mike Shulman]], _Homotopy type theory IV_ ([blog entry](http://golem.ph.utexas.edu/category/2011/04/homotopy_type_theory_vi.html))

* [[Peter LeFanu Lumsdaine]], _Higher inductive types, a tour of the menageries_ ([blog post](http://homotopytypetheory.org/2011/04/24/higher-inductive-types-a-tour-of-the-menagerie/))

* [[Peter LeFanu Lumsdaine]], _Higher Inductive Types: The circle and friends, axiomatically_ ([pdf](http://pages.cpsc.ucalgary.ca/~robin/FMCS/FMCS2011/Lumsdaine_slides.pdf))

Details of the semantics are in 

* {#LumsdaineShulman17} [[Peter LeFanu Lumsdaine]] [[Mike Shulman]], _Semantics of higher inductive types_ ([arXiv:1705.07088](https://arxiv.org/abs/1705.07088), talk slides [pdf](http://home.sandiego.edu/~shulman/papers/cellcxs.pdf))

with precursors in

* {#ShulmanLumsdaine12} [[Mike Shulman]], [[Peter LeFanu Lumsdaine]], _Semantics of higher inductive types_, 2012 ([pdf](http://uf-ias-2012.wikispaces.com/file/view/semantics.pdf/410646692/semantics.pdf))

* {#ShulmanLumsdaine16} [[Mike Shulman]], [[Peter LeFanu Lumsdaine]], _Semantics and syntax of higher inductive types_, 2016, ([slides](http://home.sandiego.edu/~shulman/papers/stthits.pdf))

Discussion of a subset of the HITs is in:

* [[Kristina Sojakova]], _Higher Inductive Types as Homotopy-Initial Algebras_
[arXiv:1402.0761](http://arxiv.org/abs/1402.0761)


* [[Steve Awodey]], [[Nicola Gambino]], [[Kristina Sojakova]], _Homotopy-initial algebras in type theory_ ([arXiv:1504.05531](http://arxiv.org/abs/1504.05531))


* [[Michael Rathjen]], _[Homotopical Inductive Types](http://www2.macs.hw.ac.uk/~cm389/hexmaps/2014/03/epsrc-ict-50/grants/EP-K023128-1.php)_ on [[higher inductive types]]


Implementation in [[Agda]]/[[Coq]] is discussed in

* {#Brunerie16} [[Guillaume Brunerie]], _Implementation of higher inductive types in HoTT-Agda_, 2016, [github](https://github.com/HoTT/HoTT-Agda/blob/master/core/lib/types/HIT_README.txt)

* Bruno Barras, _Native implementation of Higher Inductive
Types (HITs) in Coq_ [PDF](http://www.crm.cat/en/activities/documents/barras-crm-2013.pdf)



[[!redirects higher inductive types]]

[[!redirects HIT]]
[[!redirects HITs]]
