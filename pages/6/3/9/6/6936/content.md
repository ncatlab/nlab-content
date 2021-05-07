
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

    Inductive circle : Type :=
    | base : circle
    | loop : base == base.

Using the [[univalence axiom]], one can prove that the [[loop space]] `base == base` of the circle type is equivalent to the [[integers]]; see [this blog post](http://homotopytypetheory.org/2011/04/29/a-formal-proof-that-pi1s1-is-z/).

### The interval

The [[homotopy type]] of the [[interval]] can be encoded as

    Inductive interval : Type :=
    | zero : interval
    | one : interval
    | segment : zero == one.

See [[interval type]].  The interval can be proven to be [[contractible type|contractible]].  On the other hand, if the constructors `zero` and `one` satisfy their elimination rules definitionally, then the existence of an interval type implies [[function extensionality]]; see [this blog post](http://homotopytypetheory.org/2011/04/04/an-interval-type-implies-function-extensionality/).
The interval can be defined as the -1-truncation of the booleans; see [here](https://groups.google.com/d/msg/homotopytypetheory/-5mLEi_qMTo/gpNUsmI-ZT4J).

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

### Quotients of sets
 {#QuotientsOfSets}

The [[quotient]] of an [[hProp]]-value [[equivalence relation]], yielding an [[hSet]] (a [[0-truncated]] type):

    Inductive quotient (A : Type) (R : A -> A -> hProp) : Type :=
    | proj : A -> quotient A R
    | relate : forall (x y : A), R x y -> proj x == proj y
    | contr1 : forall (x y : quotient A R) (p q : x == y), p == q.

This is already interesting in [[extensional type theory]], where [[quotient types]] are not always included.  For more general homotopical quotients of "[[internal groupoids]]" as in the  [[(∞,1)-Giraud theorem]], we first need a good definition of what such an internal groupoid is.

### Rezk completion

According to [[Homotopy Type Theory -- Univalent Foundations of Mathematics]] the [[Rezk completion]] or [[stack completion]] of a [[pregroupoid]] to a [[groupoid]] is a higher inductive type and the [[1-truncated]] analogue of the quotient set construction above. 

... (translate into Agda)

### Cumulative hierarchy

According to [[Homotopy Type Theory -- Univalent Foundations of Mathematics]] the [[cumulative hierarchy]] of sets could be constructed from a type universe as a higher inductive type. 

... 

### Integers

A definition of the set of [[integers]] as a higher inductive type. 

    Inductive int : Type :=
    | zero : int
    | succ : int -> int
    | pred : int -> int
    | linv : forall (x : int) pred succ x == x
    | rinv : forall (x : int) succ pred x == x
    | contr1 : forall (x y : int) (p q : x == y), p == q.

Another definition of the integers as an inductive type: 

    Inductive int : Type :=
    | zero : int
    | succ : int -> int
    | neg : int -> int
    | axiom1 : neg zero  == zero
    | axiom2 : forall (x : int) succ neg succ x == neg x
    | contr1 : forall (x y : int) (p q : x == y), p == q.

### Polynomial rings over integers

A definition of the [[polynomial ring]] over the integers with a set of indeterminants $A$. 

    Inductive intpoly (A: Type)  :=
    | indet : A -> intpoly(A)
    | zero : intpoly(A)
    | one : intpoly(A)
    | neg : intpoly(A) -> intpoly(A)
    | add : intpoly(A) -> intpoly(A) -> intpoly(A)
    | mult : intpoly(A) -> intpoly(A) -> intpoly(A)
    | alunital : forall (x : intpoly(A)) add zero x == x
    | arunital : forall (x : intpoly(A)) add x zero == x
    | aassoc : forall (x y z : intpoly(A)) add x (add y z) == add (add x y) z
    | acomm : forall (x y : intpoly(A)) add x y = add y x
    | alinv : forall (x : intpoly(A)) add (neg x) x == zero
    | arinv : forall (x : intpoly(A)) add x (neg x) == zero
    | ldist : forall (x y z : intpoly(A)) mult x (add y z) == add (mult x y) (mult x z)
    | rdist : forall (x y z : intpoly(A)) mult (add x y) z == add (mult x z) (mult y z)
    | mlunital : forall (x : intpoly(A)) mult one x == x
    | mrunital : forall (x : intpoly(A)) mult x one == x
    | massoc : forall (x y z : intpoly(A)) mult x (mult y z) == mult (mult x y) z
    | mcomm : forall (x y : intpoly(A)) mult x y = mult y x
    | contr1 : forall (x y : intpoly(A)) (p q : x == y), p == q.

### Localization

Suppose we are given a family of [[function type|functions]]:

    Hypothesis I : Type.
    Hypothesis S T : I -> Type.
    Hypothesis f : forall i, S i -> T i.

A type is said to be $I$-**[[local object|local]]** if it sees each of these functions as an [[equivalence]]:

    Definition is_local Z := forall i,
      is_equiv (fun g : T i -> Z => g o f i).

The following HIT can be shown to be a [[reflection]] of all types into the local types, constructing the [[localization]] of the category of types at the given family of maps.

    Inductive localize X :=
    | to_local : X -> localize X
    | local_extend : forall (i:I) (h : S i -> localize X),
        T i -> localize X
    | local_extension : forall (i:I) (h : S i -> localize X) (s : S i),
        local_extend i h (f i s) == h s
    | local_unextension : forall (i:I) (g : T i -> localize X) (t : T i),
        local_extend i (g o f i) t == g t
    | local_triangle : forall (i:I) (g : T i -> localize X) (s : S i),
        local_unextension i g (f i s) == local_extension i (g o f i) s.

The first constructor gives a map from `X` to `localize X`, while the other four specify exactly that `localize X` is local (by giving adjoint equivalence data to the map that we want to become an equivalence).  See [this blog post](http://homotopytypetheory.org/2011/12/06/inductive-localization/) for details.  This construction is also already interesting in extensional type theory.

### Spectrification

A [[prespectrum]] is a sequence of [[pointed object|pointed types]] $X_n$ with pointed maps $X_n \to \Omega X_{n+1}$:

    Definition prespectrum :=
      {X : nat -> Type & 
       { pt : forall n, X n &
        { glue : forall n, X n -> pt (S n) == pt (S n) &
          forall n, glue n (pt n) == idpath (pt (S n)) }}}.

A prespectrum is a [[spectrum]] if each of these maps is an equivalence.

    Definition is_spectrum (X : prespectrum) : Type :=
      forall n, is_equiv (pr1 (pr2 (pr2 X)) n).

In classical [[algebraic topology]], there is a **spectrification** functor which is [[left adjoint]] to the inclusion of spectra in prespectra.  For instance, this is how a [[suspension spectrum]] is constructed: by spectrifying the prespectrum $X_n \coloneqq \Sigma^n A$.

The following HIT should construct spectrification in [[homotopy type theory]] (though this has not yet been verified formally).  (There are some abuses of notation below, which can be made precise using Coq typeclasses and implicit arguments.)

    Inductive spectrify (X : prespectrum) : nat -> Type :=
    | to_spectrify : forall n, X n -> spectrify X n
    | spectrify_glue : forall n, spectrify X n ->
        to_spectrify (S n) (pt (S n)) == to_spectrify (S n) (pt (S n))
    | to_spectrify_is_prespectrum_map : forall n (x : X n),
        spectrify_glue n (to_spectrify n x)
        == loop_functor (to_spectrify (S n)) (glue n x)
    | spectrify_glue_retraction : forall n
        (p : to_spectrify (S n) (pt (S n)) == to_spectrify (S n) (pt (S n))),
        spectrify X n
    | spectrify_glue_retraction_is_retraction : forall n (sx : spectrify X n),
        spectrify_glue_retraction n (spectrify_glue n sx) == sx
    | spectrify_glue_section : forall n
        (p : to_spectrify (S n) (pt (S n)) == to_spectrify (S n) (pt (S n))),
        spectrify X n
    | spectrify_glue_section_is_section : forall n
        (p : to_spectrify (S n) (pt (S n)) == to_spectrify (S n) (pt (S n))),
        spectrify_glue n (spectrify_glue_section n p) == p.

We can unravel this as follows, using more traditional notation.  Let $L X$ denote the spectrification being constructed.  The first constructor says that each $(L X)_n$ comes with a map from $X_n$, called $\ell_n$ say (denoted `to_spectrify n` above).  This induces a basepoint in each type $(L X)_n$, namely the image $\ell_n(*)$ of the basepoint of $X_n$.  The many occurrences of

    to_spectrify (S n) (pt (S n)) == to_spectrify (S n) (pt (S n))

simply refer to the based *loop space* of $\Omega_{\ell_{n+1}(*)} (L X)_{n+1}$ of $(L X)_{n+1}$ at this base point.

Thus, the second constructor `spectrify_glue` gives the structure maps $(L X)_n \to \Omega (L X)_{n+1}$ to make $L X$ into a prespectrum.  Similarly, the third constructor says that the maps $\ell_n\colon X_n \to (L X)_n$ commute with the structure maps up to a specified homotopy.

Since the basepoints of the types $(L X)_n$ are induced from those of each $X_n$, this automatically implies that the maps $(L X)_n \to \Omega (L X)_{n+1}$ are pointed maps (up to a specified homotopy) and that the $\ell_n$ commute with these pointings (up to a specified homotopy).  This makes $\ell$ into a map of prespectra.

Finally, the fourth through seventh constructors say that $L X$ is a spectrum, by giving [[h-isomorphism]] data: a retraction and a section for each glue map $(L X)_n \to \Omega (L X)_{n+1}$.  We could use adjoint equivalence data as we did for localization, but this approach avoids the presence of level-3 path constructors.  (We could have used h-iso data in localization too, thereby avoiding even level-2 constructors there.)  It is important, in general, to use a sort of equivalence data which forms an [[h-prop]]; otherwise we would be adding [[stuff, structure, property|structure]] rather than merely the property of such-and-such map being an equivalence.

## Semantics
See ([Lumsdaine-Shulman17](#LumsdaineShulman17)).

## Related concepts

* [[inductive type]], [[initial algebra of an endofunctor]]

* **higher inductive type**, [[initial algebra of a presentable ∞-monad]]


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
