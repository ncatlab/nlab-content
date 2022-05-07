
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

The [[category]] of [[simplicial abelian groups]] carries the [[mathematical structure|structure]] of a [[model category]] $sAbGrp_{proj}$ whose [[weak equivalences]] and [[fibrations]] are those of the [[forgetful functor|underlying]] morphisms in the [[classical model structure on simplicial sets]], hence whose

* [[weak equivalences]] are the [[simplicial weak homotopy equivalences]], 

* [[fibrations]] are the [[Kan fibrations]]

of [[forgetful functor|underlying]] [[simplicial sets]].

Hence the [[free functor|free]]/[[forgetful functor|underlying]]-[[adjoint functors]] (where the [[free functor]] produces [[free simplicial abelian groups]] $\mathbb{Z}[-]$) is a [[Quillen adjunction]] with the [[classical model structure on simplicial sets]] $sSet_{Qu}$:

\[
  \label{QuillenAdjunctionWithClassicalModelStructureOnSimplicialSets}
  sAbGrp_{proj}
  \underoverset
    {\underset{undrlng}{\longrightarrow}}
    {\overset{\mathbb{Z}[-]}{\longleftarrow}}
    {\bot_{\mathrm{Qu}}}
  sSet_{Qu}
\]

## Properties

### Monoidal structure
 {#MonoidalStructure}

With respect to the degreewise [[tensor product of abelian groups]] this is a [[monoidal model category]] ([Schwede & Shipley 2003, p. 312 (26 of 48)](#SchwedeShipley03)). 

### Dold-Kan correspondence

The [[Dold-Kan correspondence]] yields (see [there](Dold-Kan+correspondence#ModelCatVersion) for more) a [[Quillen equivalence]] to the projective [[model structure on connective chain complexes]].

([Quillen 67, Section II.4 item 5](#Quillen67), see also [Schwede-Shipley 03, section 4.1](#SchwedeShipley03), [p.17](http://www.math.uic.edu/~bshipley/monoidalequi.final.pdf#page=17), [Jardine 03, Lemma 1.5](#Jardine03)).

In fact, much more is true: all five classes of maps
in a [[model category]] ([[weak equivalences]], (acyclic) [[cofibrations]],
and (acyclic) [[fibrations]]) are [[preserved]] and [[reflected]]
by both of these equivalences.
That is to say, each [[model structure]] is obtained from the other
one by transferring it along the corresponding equivalence of categories.


## Related concepts

* [[Dold-Kan correspondence]]

* [[model structure on simplicial algebras]]



## References

Due to:

* {#Quillen67} [[Daniel Quillen]], Section II.4 in: _[[Homotopical Algebra]]_, Lecture Notes in Mathematics 43, Springer 1967([doi:10.1007/BFb0097438](https://doi.org/10.1007/BFb0097438))

Further discussion:

* {#SchwedeShipley03} [[Stefan Schwede]], [[Brooke Shipley]], _Equivalences of monoidal model categories_ , Algebr. Geom. Topol. 3 (2003), 287--334 ([arXiv:math.AT/0209342](http://arxiv.org/abs/math.AT/0209342), [euclid:euclid.agt/1513882376](https://projecteuclid.org/euclid.agt/1513882376))

* {#Jardine03} [[J. F. Jardine]], Lemma 1.5 in: _Presheaves of chain complexes_, K-theory 30.4 (2003): 365-420 ([pdf](https://pdfs.semanticscholar.org/360c/fd4eb76da956e0c8dd897377f6d6f342e44e.pdf), [[JardinePresheavesOfChainComplexes.pdf:file]])


