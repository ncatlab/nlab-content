
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
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

*Higher inductive types* (HITs) are a generalization of [[inductive types]] which allow the constructors to produce, not just points of the type being defined, but also elements of its iterated [[identity types]].

While HITs are already useful in [[extensional type theory]], they are most useful and powerful in [[homotopy type theory]], where they allow the construction of [[cell complexes]], [[homotopy colimits]], [[n-truncated|truncations]], [[Bousfield localization of model categories|localizations]], and many other objects from classical [[homotopy theory]].

Defining what a HIT is "in general" is an open research problem.  One mostly precise proposal may be found in &lbrack;[Shulman & Lumsdaine (2016)](#ShulmanLumsdaine16)&rbrack;.  A more syntactic description of a class of HITs may be found in &lbrack;[Brunerie (2016)](#Brunerie16), [Vezzosi, Mörtberg & Abel (2019)](#VezzosiMörtbergAbel19)&rbrack;. A solution to this problem should determine how to define the concept of an [[elementary (∞,1)-topos]].


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

* [[pushout type]]

* [[suspension type]]

* [[join type]]

* [[wedge sum type]]

* [[smash product type]]

* [[localization of a type at a family of functions]]

* [[Eilenberg-MacLane space type]]

* [[spectrification of a sequential spectrum type]]

* [[James construction type]]

* [[Rezk completion]]

* [[dependent pushout type]]

## Semantics
See ([Lumsdaine-Shulman17](#LumsdaineShulman17)).

## Related concepts

* [[inductive type]], [[initial algebra of an endofunctor]]

* **higher inductive type**, [[initial algebra of a presentable ∞-monad]]

* [[quotient inductive type]]

* [[higher coinductive type]]

## References

Textbook account:

* [[Univalent Foundations Project]], §6 of: *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;


Expositions:

* [[Mike Shulman]], _Homotopy type theory IV_ ([blog entry](http://golem.ph.utexas.edu/category/2011/04/homotopy_type_theory_vi.html))

* [[Peter LeFanu Lumsdaine]], *Higher inductive types, a tour of the menagerie* (2011) &lbrack;[blog post](http://homotopytypetheory.org/2011/04/24/higher-inductive-types-a-tour-of-the-menagerie/)&rbrack;

* [[Peter LeFanu Lumsdaine]], *Higher Inductive Types: The circle and friends, axiomatically* (2011) &lbrack;[pdf](http://pages.cpsc.ucalgary.ca/~robin/FMCS/FMCS2011/Lumsdaine_slides.pdf), [[Lumsdaine-HITs.pdf:file]]&rbrack;

* Kajetan Söhnen, *Higher Inductive Types in Homotopy Type Theory*, Munich (2018) &lbrack;[pdf](https://www.math.lmu.de/~petrakis/Soehnen.pdf), [[Soehnen-HigherInductiveTypes.pdf:file]]&rbrack;


Details on the [[categorical semantics]] of HITs:

* {#LumsdaineShulman17} [[Peter LeFanu Lumsdaine]], [[Mike Shulman]], *Semantics of higher inductive types*, Math. Proc. Camb. Phil. Soc. **169** (2020) 159-208 &lbrack;[arXiv:1705.07088](https://arxiv.org/abs/1705.07088), talk slides [pdf](http://home.sandiego.edu/~shulman/papers/cellcxs.pdf), [doi:10.1017/S030500411900015X](https://doi.org/10.1017/S030500411900015X)&rbrack;

with precursors in

* {#ShulmanLumsdaine12} [[Mike Shulman]], [[Peter LeFanu Lumsdaine]], *Semantics of higher inductive types* (2012) &lbrack;[[ShulmanLumsdaine-HITs2012.pdf:file]]&rbrack;

* {#ShulmanLumsdaine16} [[Mike Shulman]], [[Peter LeFanu Lumsdaine]], _Semantics and syntax of higher inductive types_ (2016) &lbrack;[slides](http://home.sandiego.edu/~shulman/papers/stthits.pdf)&rbrack;


Discussion of HITs which arise as homotopy-[[initial algebras of an endofunctor]]:

* [[Kristina Sojakova]], *Higher Inductive Types as Homotopy-Initial Algebras*, ACM SIGPLAN Notices **50** 1 (2015) 31–42 &lbrack;[arXiv:1402.0761](http://arxiv.org/abs/1402.0761), [doi:10.1145/2775051.2676983](https://doi.org/10.1145/2775051.2676983)&rbrack;

* [[Steve Awodey]], [[Nicola Gambino]], [[Kristina Sojakova]], *Homotopy-initial algebras in type theory*, Journal of the ACM **63** 6 (2017) 1–45 &lbrack;[arXiv:1504.05531](http://arxiv.org/abs/1504.05531), [doi:10.1145/3006383](https://doi.org/10.1145/3006383)&rbrack;

Further developments:

* [[Henning Basold]], [[Herman Geuvers]], [[Niels van der Weide]], *Higher Inductive Types in Programming*, Journal of Universal Computer Science **23** 1 (2017) 63-88 &lbrack;[pdf](https://www.jucs.org/jucs_23_1/higher_inductive_types_in/jucs_23_01_0063_0088_basold.pdf), [slides pdf](https://nmvdw.github.io/pubs/Agda25.pdf)&rbrack;

* {#vanDoorn18} [[Floris van Doorn]], §3 in: *On the Formalization of Higher Inductive Types and Synthetic Homotopy Theory* (2018) &lbrack;[arXiv:1808.10690](https://arxiv.org/abs/1808.10690)&rbrack;

  > (formalization in [[Lean]])

* [[Niccolò Veltri]], [[Niels van der Weide]], *Constructing Higher Inductive Types as Groupoid Quotients*, Logical Methods in Computer Science **17** 2 (2021)  &lbrack;[arXiv:2002.08150](https://arxiv.org/abs/2002.08150), <a href="https://doi.org/10.23638/LMCS-17(2:8)2021">doi:10.23638/LMCS-17(2:8)2021</a>&rbrack;



Implementation of HITs in [[proof assistants]]:

in [[Agda]]:

* {#Brunerie16} [[Guillaume Brunerie]], _Implementation of higher inductive types in HoTT-Agda_ (2016) &lbrack;[github](https://github.com/HoTT/HoTT-Agda/blob/master/core/lib/types/HIT_README.txt)&rbrack;

  > (deprecated)

in [[Cubical Agda]]:

* {#VezzosiMörtbergAbel19} [[Andrea Vezzosi]], [[Anders Mörtberg]], [[Andreas Abel]], §4 in: *Cubical Agda: A Dependently Typed Programming Language with Univalence and Higher Inductive Types*, Proceedings of the ACM on Programming Languages **3** ICFP 87  (2019) 1–29 &lbrack;[doi:10.1145/3341691](https://doi.org/10.1145/3341691), [pdf](https://www.cse.chalmers.se/~abela/icfp19.pdf)&rbrack;

* [cubical Agda documentation](https://agda.readthedocs.io/en/v2.6.2.2.20221128/language/cubical.html): *[Higher Inductive Types](https://agda.readthedocs.io/en/v2.6.1/language/cubical.html#higher-inductive-types)*

in [[Coq]]:

* Bruno Barras, _Native implementation of Higher Inductive
Types (HITs) in Coq_ [PDF](http://www.crm.cat/en/activities/documents/barras-crm-2013.pdf)

in [[Lean]]: [van Doorn (2018)](#vanDoorn18)

Discussion of [[coinduction]] via HITs: 

* Magnus Baunsgaard Kristensen, [[Rasmus Ejlers Møgelberg]], [[Andrea Vezzosi]], *Greatest HITs: Higher inductive types in coinductive definitions via induction under clocks* ([arXiv:2102.01969](https://arxiv.org/abs/2102.01969))

Discussion of impredicative encodings of higher inductive types:

* [[Steve Awodey]], [[Jonas Frey]], and [[Sam Speight]]. “Impredicative Encodings of (Higher) Inductive Types”. In: Proceedings of the 33rd Annual ACM/IEEE Symposium on Logic in Computer Science. LICS ’18. Oxford, United Kingdom: ACM, 2018, pp. 76–85. (ISBN:978-1-4503-5583-4, [doi:10.1145/3209108.3209130](https://doi.org/10.1145/3209108.3209130))

[[!redirects higher inductive types]]

[[!redirects HIT]]
[[!redirects HITs]]
