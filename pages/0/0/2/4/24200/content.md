
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
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea 

In classical [[algebraic topology]], there is a **[[spectrification]]** functor which is [[left adjoint]] to the inclusion of [[spectra]] in [[prespectra]]. For instance, this is how a [[suspension spectrum]] is constructed: by spectrifying the prespectrum $X_n \coloneqq \Sigma^n A$. There is an analogue in [[homotopy type theory]] which constructs the spectrification of a [[sequential spectrum type]] (i.e. prespectrum types) into a [[Omega-spectrum type]] (i.e. spectrum types). 

## Definition

The following [[higher inductive type]] should construct spectrification in [[homotopy type theory]] (though this has not yet been verified formally). (There are some abuses of notation below, which can be made precise using Coq typeclasses and implicit arguments.)

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

## See also

* [[higher inductive type]]

* [[sequential spectrum type]]

* [[Omega-spectrum type]]

* [[spectrification]]

## References ##

* [[Univalent Foundations Project]], *[[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013)

* [[Floris van Doorn]] (2018), _On the Formalization of Higher Inductive Types and Synthetic Homotopy Theory_, ([arXiv:1808.10690](https://arxiv.org/abs/1808.10690), [web](http://florisvandoorn.com/papers/dissertation.pdf))
