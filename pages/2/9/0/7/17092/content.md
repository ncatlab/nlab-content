
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _equivariant Whitehead theorem_ is the generalization of the [[Whitehead theorem]] from ([[stable homotopy theory|stable]]) [[homotopy]] to ([[equivariant stable homotopy theory|stable]]) [[equivariant homotopy theory]]:

Assume that the [[equivariance group]] be a [[compact Lie group]] ([Matumoto 71](#Matumoto71), [Illman 72](#Illman72), [James-Segal 78](#JamesSegal78), [Waner 80](#Waner80)). (This assumption is used, e.g. in [Waner 80, Rem. 7.4](#Waner80), to guarantee that [[Cartesian products]] of [[coset spaces]] $G/H$ are themselves [[G-CW-complexes]], which follows for [[compact Lie groups]], e.g. by the [[equivariant triangulation theorem]].)

Then: *$G$-[[homotopy equivalences]] $f \colon X \longrightarrow Y$ between [[G-CW complexes]] are equivalent to [[equivariant weak homotopy equivalences]], hence to [[maps]] that induce [[weak homotopy equivalences]] $f^H \colon X^H \longrightarrow Y^H$ on all [[fixed point spaces]] for all [[closed topological space|closed]] [[subgroups|subgroups]] $H \hookrightarrow G$*. 

This is due to [Matumoto 71, Thm. 5.3](#Matumoto71), [Illman 72, Prop. 2.5](#Illman72), [Waner 80, Theorem 3.4](#Waner80), see also [James-Segal 78, Thm. 1.1](#JamesSegal78) with [Kwasik 81](#Kwasik81), 
review in [Shah 10](#Shah10), [Blumberg 17, Cor. 1.2.14](#Blumberg17).

An analogous statement holds in [[stable equivariant homotopy theory]]:

A map $f \colon E \longrightarrow F$ between genuine [[G-spectra]] is a weak equivalence (isomorphism in the [[equivariant stable homotopy category]]) if it induces isomorphisms on all [[equivariant homotopy group]] [[Mackey functors]] $\pi_n(f)\colon \pi_n(E) \longrightarrow \pi_n(F) $ (e. g. [Greenlees-May 95, theorem 2.4](#GreenleesMay95), [Bohmann, theorem 3.2](#Bohmann)).

## Related concepts

* [[G-CW approximation theorem]], [[equivariant cellular approximation theorem]]

* [[Elmendorf's theorem]]

* [[tom Dieck splitting]]

## References

Proofs for general [[G-CW-complexes]] (for $G$ a [[compact Lie group]]) are due to

* {#Matumoto71} [[Takao Matumoto]], Theorem 5.3 in: _On $G$-CW complexes and a theorem of JHC Whitehead_, J. Fac. Sci. Univ. Tokyo Sect. IA 18, 363-374, 1971 ([[matumoto.pdf:file]])

following a partial result in

*  [[Takao Matumoto]], Lemma 4.3 in: _Equivariant K-theory and Fredholm operators, J. Fac. Sci. Tokyo 18 (1971/72), 109-112 ([pdf](https://repository.dl.itc.u-tokyo.ac.jp/?action=repository_action_common_download&item_id=39826&item_no=1&attribute_id=19&file_no=1), [[MatumotoEquivariantKTheory.pdf:file]])

and, independently, due to

* {#Illman72} [[Sören Illman]], Prop. 3.3 in: *Equivariant Algebraic Topology*, Princeton University 1972 ([[Illman_EquivariantAlgebraicTopology1972.pdf:file]])


* {#Illman72} [[Sören Illman]], Prop. 2.5 in: *Equivariant singular homology and cohomology for actions of compact lie groups* ([doi:10.1007/BFb0070055](https://doi.org/10.1007/BFb0070055)) In: H. T. Ku, L. N. Mann, J. L. Sicks, J. C. Su (eds.), *Proceedings of the Second Conference on Compact Transformation Groups* Lecture Notes in Mathematics, vol 298. Springer 1972 ([doi:10.1007/BFb0070029](https://link.springer.com/book/10.1007/BFb0070029))

See also:

* {#Waner80} [[Stefan Waner]], Theorem 3.4 in: _Equivariant Homotopy Theory and Milnor's Theorem_, Transactions of the American Mathematical Society Vol. 258, No. 2 (Apr., 1980), pp. 351-368 ([jstor:1998061](http://www.jstor.org/stable/1998061))

Discussion in [[equivariant stable homotopy theory]]:

* {#GreenleesMay95} [[John Greenlees]], [[Peter May]], _Equivariant stable homotopy theory_, in I.M. James (ed.), _Handbook of Algebraic Topology_ , pp. 279-325. 1995. ([pdf](http://www.math.uchicago.edu/~may/PAPERS/Newthird.pdf))

Review and Lecture notes:


* {#Blumberg17} [[Andrew Blumberg]], Section 1.2 in: _Equivariant homotopy theory_, 2017 ([pdf](https://www.ma.utexas.edu/users/a.debray/lecture_notes/m392c_EHT_notes.pdf), [GitHub](https://github.com/adebray/equivariant_homotopy_theory))


A proof for $G$-[[absolute neighbourhood retract|ANRs]] is due to:

* {#JamesSegal78}  [[Ioan James]], [[Graeme Segal]], Theorem 1.1 in: _On equivariant homotopy type_, Topology Volume 17, Issue 3, 1978, Pages 267-272 (<a href="https://doi.org/10.1016/0040-9383(78)90030-7">doi:10.1016/0040-9383(78)90030-7</a>)

Proof that these $G$-[[absolute neighbourhood retract|ANRs]] have the [[equivariant homotopy type]] of [[G-CW-complexes]] (for $G$ a [[compact Lie group]]):

* {#Kwasik81} [[Slawomir Kwasik]], _On the Equivariant Homotopy Type of $G$-ANR's_, Proceedings of the American Mathematical Society Vol. 83, No. 1 (Sep., 1981), pp. 193-194 (2 pages) ([jstor:2043921](https://www.jstor.org/stable/2043921))

Textbook account for $G$-ANRs:

* {#tomDieck79} [[Tammo tom Dieck]], Prop. 8.2.4, 8.2.6 in: _[[Transformation Groups and Representation Theory]]_, Lecture Notes in Mathematics 766, Springer 1979 ([doi:10.1007/BFb0085965](https://link.springer.com/book/10.1007/BFb0085965))

For the case of [[stable equivariant homotopy theory]]:


* {#Bohmann} [[Anna Marie Bohmann]], _Basic notions of equivariant stable homotopy theory_ ([pdf](http://math.northwestern.edu/~bohmann/basicequivnotions.pdf))

