
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Duality in string theory
+-- {: .hide}
[[!include duality in string theory -- contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc} 

## Idea

To every complex 3-dimensional [[Calabi-Yau variety]] $X$ are associated two similar but differing types of [[sigma-model]] $N=2$-supersymmetric [[2d CFTs]]. There is at least for some CY $X$ a map $X \mapsto \hat X$ which exchanges the [[Hodge numbers]] $h^{1,1}$ and $h^{1,2}$ such that $SCFT_A(X)$ is expected to be equivalent to $SCFT_B(\hat X)$. 

$$
  SCFT_A(X) \simeq SCFT_B(\hat X)
  \,.
$$

This is called _mirror symmetry_. At least in some cases this can be understood as a special case of [[T-duality]] ([Strominger-Yau-Zaslow 96](#StromingerYauZaslow96)).

In this form mirror symmetry remains a conjecture, not the least because for the moment there is no complete construction of these SCFTs. But to every such $SCFT(X)$ one can associate two [[TCFT]]s, $A(X)$ and $B(X)$, the [[A-model]] and the [[B-model]]. These $N=1$ supersymmetric field theories were obtained by [[Edward Witten]] using a "topological twist". The topological [[A-model]] can be expressed in terms of [[symplectic geometry]] of a variety and the topological B-model can be expressed in terms of the [[algebraic geometry]] of a variety. 

These topological theories are easier to understand and do retain a little bit of the information encoded in the full SCFTs. In terms of these the statement of mirror symmetry says that passing to mirror CYs _exchanges_ the [[A-model]] with the $B$-model and conversely:

$$
  A(X) \simeq B(\hat X),\,\,\,\,\,\,\,B(X)\simeq A(\hat X)
  \,.
$$

By a version of the [[cobordism hypothesis]]-theorem, these [[TCFT]]s (see there) are encoded by [[A-∞ categories]] that are [[Calabi-Yau categories]]: the [[A-model]] by the [[Fukaya category]] $Fuk(X)$ of $X$ which can be understood as a [[stable (∞,1)-category]] representing the Lagrangian intersection theory on the underlying [[symplectic manifold]]; and the [[B-model]] by an [[enhanced triangulated category|enhancement]] of the [[derived category]] of [[coherent sheaves]] $D^b_\infty(\hat X)$ on $\hat X$.

In terms of this data, mirror symmetry is the assertion that these [[A-∞ categories]] are equivalent and simultaneously the same under exchange $X\leftrightarrow \hat{X}$:

$$
  Fuk(X) \simeq D^b_\infty(\hat{X}),
\,\,\,\, and \,\,\,\,
Fuk(\hat{X}) \simeq D^b_\infty(X).
$$

This categorical formulation was introduced by [[Maxim Kontsevich]] in 1994 under the name **homological mirror symmetry**. The equivalence of the categorical expression of mirror symmetry to the SCFT formulation has been proven by [[Maxim Kontsevich]] and independently by [[Kevin Costello]], who showed how the datum of a topological conformal field theory is equivalent to the datum of a [[Calabi-Yau category|Calabi-Yau A-∞-category]](see [[TCFT]]).


The mirror symmetry conjecture roughly claims that every Calabi-Yau 3-fold has a mirror. In fact one considers (mirror symmetry for) degenerating families for Calabi-Yau 3-folds in large volume limit (which may be expressed precisely via the Gromov-Hausdorff metric). The appropriate definition of (an appropriate version of) the [[Fukaya category]] of a symplectic manifold is difficult to achieve in desired generality. 
Invariants/tools of Fukaya category include symplectic [[Floer homology]] and Gromov-Witten invariants (building up the [[quantum cohomology]]). 

Mirror symmetry is related to the [[T-duality]] on each fiber of an associated Lagrangian fibration [Strominger-Yau-Zaslow 96](#StromingerYauZaslow96).  

Although the non-Calabi-Yau case may be of lesser interest to physics, one can still formulate some mirror symmetry statements for, for instance, Fano manifolds. The mirror to a Fano manifold is a [[Landau-Ginzburg model]] (see [Hori-Vafa 00](#HoriVafa00); see also work of Auroux for an explanation via the Strominger-Yau-Zaslow T-duality philosophy). Then the statements are: the [[A-model]] of the Fano (given by the Fukaya category) is equivalent to the B-model of the [[Landau-Ginzburg model]] (given by the category of matrix factorizations); and the B-model of the Fano (given by the derived category of sheaves) is equivalent to the [[A-model]] of the [[Landau-Ginzburg model]] (given by the Fukaya-Seidel category). A few of the relevant names: Kontsevich, Hori-Vafa, Auroux, Katzarkov, Orlov, Seidel, ...

## Properties

### Relation to tropical geometry.

Close relation to [[tropical geometry]], see e.g. [Gross 11](#Gross11).

## Related concepts

* [[moduli space of Calabi-Yau spaces]]

* [[3d mirror symmetry]]

* [[duality in physics]], [[duality in string theory]]

* [[geometric Langlands duality]]

* [[Landau-Ginzburg model]]

## References

### General

The original statement of the homological mirror symmetry conjecture is in

* [[Maxim Kontsevich]], _Homological algebra of mirror symmetry_, Proc. ICM Z&#252;rich 1994, [alg-geom/9411018](http://arxiv.org/abs/alg-geom/9411018)

See also

* [[Paul Aspinwall]], [[Brian Greene]], [[David Morrison]], _Calabi-Yau Moduli Space, Mirror Manifolds and Spacetime Topology Change in String Theory_, Nucl.Phys. B416 (1994) 414-480 ([arXiv:hep-th/9309097](http://arxiv.org/abs/hep-th/9309097))


Review contains 

* {#HoriVafa00} [[Kentaro Hori]], [[Cumrun Vafa]], _Mirror Symmetry_ ([arXiv:hep-th/0002222](https://arxiv.org/abs/hep-th/0002222))

* M. Ballard, _Meet homological mirror symmetry_ ([arxiv:0801.2014](http://arxiv.org/abs/0801.2014))

* A. Port, _An Introduction to Homological Mirror Symmetry and the Case of Elliptic Curves_ ([arXiv:1501.00730](http://arxiv.org/abs/1501.00730))

* {#IbanezUranga12} [[Luis Ibáñez]], [[Angel Uranga]], section 10.1.2 of _[[String Theory and Particle Physics -- An Introduction to String Phenomenology]]_, Cambridge University Press 2012

Discussion amplifying the role of [[category theory]], and [[higher geometry]] is in 

* {#Sharpe19} [[Eric Sharpe]], _Categorical Equivalence and the Renormalization Group_, Proceedings of LMS/EPSRC Symposium _[Higher Structures in M-Theory](http://www.maths.dur.ac.uk/lms/109/index.html)_, Fortschritte der Physik 2019 ([arXiv:1903.02880](https://arxiv.org/abs/1903.02880))

Other reviews include

* [[Paul Aspinwall]], [[Tom Bridgeland]], [[Alastair Craw]], [[Michael Douglas]], Mark Gross, [[Anton Kapustin]], [[Gregory Moore]], [[Graeme Segal]], [[Balázs Szendrői]], P. Wilson,

  _Dirichlet branes and mirror symmetry_, 

  Clay Mathematics Monograph Volume 4, Amer. Math. Soc. Clay Math. Institute 2009 

  ([pdf](http://www.claymath.org/library/monographs/cmim04c.pdf), [pdf](http://www2.maths.ox.ac.uk/cmi/library/monographs/cmim04.pdf))  (very readable!)

The relation to [[T-duality]] was established in

* {#StromingerYauZaslow96} [[Andrew Strominger]], [[Shing-Tung Yau]], [[Eric Zaslow]], _Mirror Symmetry is T-Duality_, Nucl.Phys.B479:243-259,1996 (DOI 10.1016/0550-3213(96)00434-8) [hep-th/9606040](http://arxiv.org/abs/hep-th/9606040)

Further references include

* [[Cumrun Vafa]], [[Shing-Tung Yau]] (eds.), _Winter school on mirror symmetry, vector bundles, and Lagrangian submanifolds_, Harvard 1999, AMS, Intern. Press (includes A. Strominger, S-T. Yau, E. Zaslow, _Mirror symmetry is $T$-duality_  as pages  333--347; ). 

* K. Hori, S. Katz, A. Klemm et al. _Mirror symmetry I_, AMS, Clay Math. Institute 2003.

* Paul Seidel, _Fukaya categories and Picard-Lefschetz theory_, Zurich Lectures in Advanced Mathematics. European Mathematical Society, Z&#252;rich, 2008. viii+326 pp

* Mark Gross, Bernd Siebert, _Mirror symmetry via logarithmic degeneration data I_, [math.AG/0309070](http://arxiv.org/abs/math/0309070), _From real affine geometry to complex geometry_, [math.AG/0703822](http://arxiv.org/abs/math/0703822), _Mirror symmetry via logarithmic degeneration data II_, [arxiv/0709.2290](http://arxiv.org/abs/0709.2290) 

* [[Anton Kapustin]], [[Dmitri Orlov]], _Lectures on mirror symmetry, derived categories, and D-branes_,  Uspehi Mat. Nauk __59__  (2004),  no. 5(359), 101--134;  translation in  Russian Math. Surveys __59__  (2004), no. 5, 907--940, [math.AG/0308173](http://arxiv.org/abs/math/0308173)

* [[Maxim Kontsevich]], [[Yan Soibelman]], _Homological mirror symmetry and torus fibrations_, [math.SG/0011041](http://arxiv.org/abs/math/0011041)

* Yong-Geun Oh, Kenji Fukaya, _Floer homology in symplectic geometry and mirror symmetry_, Proc. ICM 2006, [pdf](http://www.math.wisc.edu/~oh/Oh-icm2006.pdf)

* wikipedia: [mirror symmetry (string theory)](http://en.wikipedia.org/wiki/Mirror_symmetry_%28string_theory%29), [homological mirror symmetry](http://en.wikipedia.org/wiki/Homological_mirror_symmetry)

* partial notes from Miami 08 workshop: [miami08-notes](http://www-math.mit.edu/~auroux/frg/miami08-notes) and abstracts from [miami09](http://www-math.mit.edu/~auroux/frg/miami09-abstracts.html), [miami10](http://www-math.mit.edu/~auroux/frg/miami10-abstracts.html)

* {#Gross11} [[Mark Gross]], _Tropical geometry and mirror symmetry_, CBMS regional conf. ser. 114 (2011), based on the CBMS course in Kansas, [AMS book page] (http://www.ams.org/bookstore-getitem/item=CBMS-114), [pdf](http://www.math.ucsd.edu/~mgross/kansas.pdf) 

Discussion in the context of [[derived Morita equivalence]] includes

* {#Okada09} So Okada, _Homological mirror symmetry of Fermat polynomials_ ([arXiv:0910.2014](http://arxiv.org/abs/0910.2014))


### Complete proofs {#CompleteProofs}

Here is a list with references that give complete proofs of *homological* mirror symmetry on certain (types of) spaces.

* M. Abouzaid, I. Smith, _Homological mirror symmetry for the four-torus_, Duke Math. J. 152 (2010), 373&#8211;440, [arXiv:0903.3065](http://arxiv.org/abs/0903.3065)

* A. Polishchuk and E. Zaslow, _Categorical mirror symmetry: the elliptic curve_, Adv. Theor. Math. Phys. 2:443470, 1998.

* V. Golyshev, V. Lunts, D. Orlov, _Mirror symmetry for abelian varieties_, J. Alg. Geom. __10__ (2001), no. 3, 433--496, [math.AG/9812003](http://arxiv.org/abs/math/9812003)

* P. Seidel, _Homological mirror symmetry for the quartic surface_, [arXiv:0310414](http://arxiv.org/abs/math/0310414)

* Alexander I. Efimov, _Homological mirror symmetry for curves of higher genus_, Inventiones Math. __166__ (2006), 537&#8211;582, [arXiv:0907.3903](http://arxiv.org/abs/0907.3903)

* [[D. Auroux]], [[L. Katzarkov]], [[D. Orlov]], _Mirror symmetry for Del Pezzo surfaces: Vanishing cycles and coherent sheaves_, []();  _Mirror symmetry for weighted projective planes and their noncommutative deformations_, Ann. Math. __167__ (2008), 867&#8211;943, [math.AG/0404281](http://arxiv.org/abs/math/0404281)

* [[Mohammed Abouzaid]], Denis Auroux, Alexander I. Efimov, Ludmil Katzarkov, Dmitri Orlov, _Homological mirror symmetry for punctured spheres_, [arxiv/1103.4322](http://arxiv.org/abs/1103.4322)

* [[Paul Seidel]], _Homological mirror symmetry for the genus two curve_, J. Algebraic Geometry, to appear, [arXiv:0812.1171](http://arxiv.org/abs/0812.1171)

### Computation via topological recursion

Computation via [[topological recursion]] in [[matrix models]] and all-[[genus of  a surface|genus]] proofs of mirror symmetry is due to

* {#BouchardKlemmMarinoPasquetti09} [[Vincent Bouchard]], [[Albrecht Klemm]], [[Marcos Marino]], [[Sara Pasquetti]], _Remodeling the B-model_, Commun.Math.Phys.287:117-178, 2009 ([arXiv:0709.1453](https://arxiv.org/abs/0709.1453))

* [[Bertrand Eynard]], [[Amir-Kian Kashani-Poor]], Olivier Marchal, _A matrix model for the topological string I: Deriving the matrix model_ ([arXiv:1003.1737](https://arxiv.org/abs/1003.1737))

* [[Bertrand Eynard]], [[Amir-Kian Kashani-Poor]], Olivier Marchal, _A matrix model for the topological string II: The spectral curve and mirror geometry_ ([arXiv:1007.2194](https://arxiv.org/abs/1007.2194))

* {#EynardOrantin12} [[Bertrand Eynard]], [[Nicolas Orantin]], _Computation of open Gromov-Witten invariants for toric Calabi-Yau 3-folds by topological recursion, a proof of the BKMP conjecture_ ([arXiv:1205.1103](https://arxiv.org/abs/1205.1103))

* {#FangLiuZong13} Bohan Fang, Chiu-Chu Melissa Liu, Zhengyu Zong, _All Genus Open-Closed Mirror Symmetry for Affine Toric Calabi-Yau 3-Orbifolds_ ([arXiv:1310.4818](https://arxiv.org/abs/1310.4818))


[[!redirects homological mirror symmetry]]