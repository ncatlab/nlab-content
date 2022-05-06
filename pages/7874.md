

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Higher linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Higher spin geometry
+-- {: .hide}
[[!include higher spin geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _string orientation of tmf_ is the universal [[orientation in generalized cohomology]] for [[tmf]]-cohomology ("universal [[elliptic cohomology]]), given by a [[homomorphism]]

$$  
  \sigma \;\colon\; M String \longrightarrow tmf
$$

of [[E-∞ rings]], from the [[String structure]]-[[Thom spectrum]] to [[tmf]]  This is refinement of the [[Witten genus]] (see there for more)

$$
  w \;\colon\; \Omega^{String,rat}_\bullet \longrightarrow MF_\bullet
$$

(with values in the ring of [[modular forms]]) which it reproduces on [[homotopy groups]]

$$
  w \simeq \pi_\bullet(\sigma)
  \,.
$$

For this reason the string orientation of [[tmf]] is also referred to as the "topological Witten genus".

All this is due to ([Ando-Hopkins-Strickland 01](#AndoHopkinsStrickland01), [Ando-Hopkins-Rezk 10](#AndoHopkinsRezk10)).

See the Idea-section at _[[tmf]]_ and at _[[Witten genus]]_ for more background.


## Construction via Cubical structure

The construction proceeds via the relation between
orientations in complex orientable cohomology theory and [[cubical structures on line bundles]], see there for more.

## Properties

### Relation to twists of $tmf$

(...) relation to the [[twisted cohomology|twists]] of [[tmf]]-[[cohomology theory]] (...)

$$
  \array{
      && B String
      \\
      & \swarrow && \searrow
      \\
     \ast && && B Spin
     \\
      & \searrow && \swarrow
      \\
      && B^3 U(1)
      \\
      && \downarrow
      \\
      && B GL_1(tmf)
  }
$$

([ABG 10, (8.1)](#ABG10))


## Related concepts

* [[spin orientation of Tate K-theory]]

* [[sigma-orientation]]

* [[logarithmic cohomology operation]]

[[!include genera and partition functions - table]]

## References

The construction/identification of the string orientation and its relation to the Witten genus is due to

* {#AndoHopkinsStrickland01} [[Matthew Ando]], [[Michael Hopkins]], [[Neil Strickland]], _Elliptic spectra, the Witten genus and the theorem of the cube_, Invent. Math. 146 (2001) 595&#8211;687 MR1869850 ([doi:10.1007/s002220100175](https://doi.org/10.1007/s002220100175), [pdf](http://www.math.rochester.edu/people/faculty/doug/otherpapers/musix.pdf))

* {#AndoHopkinsStrickland02} [[Matthew Ando]], [[Michael Hopkins]], [[Neil Strickland]], _The sigma orientation is an H-infinity map_, American Journal of Mathematics Vol. 126, No. 2 (Apr., 2004), pp. 247-334 ([arXiv:math/0204053](http://arxiv.org/abs/math/0204053), [doi:10.1353/ajm.2004.0008](https://doi.org/10.1353/ajm.2004.0008))

* {#AndoHopkinsRezk10} [[Matthew Ando]], [[Mike Hopkins]], [[Charles Rezk]], _Multiplicative orientations of $KO$-theory and the spectrum of topological modular forms_, 2010 ([pdf](http://www.math.uiuc.edu/~mando/papers/koandtmf.pdf))

following announcements of results in 

* {#Hopkins02} [[Michael Hopkins]], _Algebraic topology and modular forms_ in Proceedings of the International Congress of Mathematicians,
Vol. I (Beijing, 2002), pages 291&#8211;317, Beijing, 2002. Higher Ed. Press ([arXiv:math/0212397](http://arxiv.org/abs/math/0212397)) 

which in turn follows the general program outlined in

* [[Michael Hopkins]], _Topological modular forms, the Witten genus, and the theorem of the cube_, Proceedings of the International Congress of Mathematicians, Vol. 1, 2 (Z&#168;urich, 1994) (Basel), Birkh&#228;user, 1995, 554&#8211;565. MR 97i:11043 ([pdf](http://www.mathunion.org/ICM/ICM1994.1/Main/icm1994.1.0554.0565.ocr.pdf))

An alternative construction using the [[derived algebraic geometry]] of the [[moduli stack of elliptic curves]] is sketched in

* [[Jacob Lurie]], section 5.3 of _[[A Survey of Elliptic Cohomology]]_

In fact the construction there is a refinement of the orientation of just $tmf$ to one of all $E_\infty$-rings $A$ carrying a [[derived elliptic curve]] $E \to Spec(A)$.

Discussion in relation to the [[twisted cohomology|twists]] of [[tmf]]-cohomology is in 

* {#ABG10} [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], _Twists of K-theory and TMF_, in Robert S. Doran, Greg Friedman, [[Jonathan Rosenberg]], _Superstrings, Geometry, Topology, and $C^*$-algebras_, Proceedings of Symposia in Pure Mathematics [vol 81](http://www.ams.org/bookstore-getitem/item=PSPUM-81), American Mathematical Society ([arXiv:1002.3004](http://arxiv.org/abs/1002.3004))
 
with some related chat in _[[schreiber:Quantization via Linear homotopy types]]_.

Possible hints for further relation between [[2d SCFT]] and [[tmf]] are presented in

* [[Davide Gaiotto]], [[Theo Johnson-Freyd]], _Holomorphic SCFTs with small index_ ([arXiv:1811.00589](https://arxiv.org/abs/1811.00589))

[[!redirects sigma-orientation]]

[[!redirects String orientation of tmf]]

[[!redirects string-orientation of tmf]]
[[!redirects String-orientation of tmf]]

