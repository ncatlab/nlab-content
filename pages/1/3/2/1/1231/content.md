+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Duality
+--{: .hide}
[[!include duality - contents]]
=--
=--
=--


# Koszul duality
* table of contents
{: toc}

## Idea

__Koszul duality__ (named after [[Jean-Louis Koszul]]) is a duality and phenomenon generalizing the duality between the symmetric and exterior algebra of a vector space to so-called quadratic [[differential graded algebra]]s (which can be obtained as a free dga module an ideal of relations which live in degree 2). For a pair of Koszul dual algebras, there is a correspondence between certain parts of their derived categories (precise formulation involves some finiteness conditions). In a setup in which one of the algebras is replaced by a cocomplete dg coalgebra, there is a formulation free of finiteness conditions, but involving [[twisting cochain]] (see that entry).


## On operads

Koszul duality is a duality between [[quadratic operad]]s, predicted in 

* [[Maxim Kontsevich|M. Kontsevich]], _Formal (non)commutative symplectic geometry_,  The Gel&#697;fand Mathematical Seminars, 1990--1992,  173--187, Birkh&#228;user, Boston, MA, 1993 (cf. [[formal noncommutative symplectic geometry]]).

and developed in

* [[Victor Ginzburg]], [[Mikhail Kapranov]], _Koszul duality for operads_, Duke Math. J. __76__ (1994),  no. 1, 203--272; reprint [arxiv/0709.1228](http://arxiv.org/abs/0709.1228); *Erratum to: Koszul duality for operads*, Duke Math. J. __80__ (1995),  no. 1, 293. 



## For associative and dg-algebras

From Ben Webster on [mathoverflow](https://mathoverflow.net/a/394/2362):

There are a lot of algebras whose derived categories are equivalent in surprising ways.  [[Morita equivalences]] are pretty simple, especially for finite dimensional algebras; essentially the only free parameter is the dimension of the object.

Namely, if $A Mod$ and $B Mod$ are equivalent, then the image of $A$ as a module over itself is a [[projective object|projective]] [[generator]] of $B Mod$, and for a finite-dimensional algebra, essentially the only thing you can do is take several copies of the [[indecomposable object|indecomposible]] projectives of $B$.

On the other hand, if you take the derived category of [[differential graded module|dg-modules]] over $A$ (the dg part of this is not a huge deal; it's just that they're very close to, but a bit better behaved than, actual derived/[[triangulated categories]], which are just crude truncations of truly functorial dg/$A_\infty$ versions), this is equivalent to the category of dg-modules over the [[endomorphism algebra]] (this is in the dg sense, so it's a dg-algebra whose cohomology is the $Ext$ algebra) of *any* generating object.  There are a *lot* more generating objects than projective generators, so there are a lot of derived equivalences.

In particular, let $A$ be a finite dimensional algebra $A$, than an  obvious not-very-projective generating object is the sum of all the [[simple modules]], say $L$.  As mentioned above, there's an equivalence $A dg Mod = \mathrm{Ext}(L,L) dg Mod$, just given by taking $\mathrm{Ext}(L,-)$.   

In general, $\mathrm{Ext}(L,L)$ is in a very complicated object (for example, often for [[group algebras]] over [[finite field]]s), but sometimes it turns out to be nice.  For example, if $A$ is an  [[exterior algebra]], you'll get a [[polynomial ring]] on the dual vector space.  Another (closely related) example is that the cohomology of a [[reductive group]] (over $\mathbb{C}$) is Koszul dual to the cohomology of its classifying space.

One way to ensure that $\mathrm{Ext}(L,L)$ is nice is if the algebra $A$ is [[graded algebra|graded]]. Then $\mathrm{Ext}(L,L)$ inherits an "internal" grading in addition to its homological one.  If these coincide, then $A$ is called _Koszul_. 

In this case, $B=\mathrm{Ext}(L,L)$ is forced to be formal (if it had any interesting $A_\infty$ operations, they would break the grading), so you're dealing with a derived equivalence between actual algebras, though you have to be a bit careful about the dg-issues.  Thus the derived category of usual modules over $A$ is equivalent to dg-modules over $B$ (with its unique grading) and vice versa.  This can be fixed by taking graded modules on both sides.


## Examples

* The most famous example of Koszul dual algebras are the [[exterior algebra]] $Alt^{\bullet}V[-1]$ and the [[polynomial algebra]] $Sym^\bullet V^*[-2]$.

* A regular block of [[category O]] for any [[semisimple Lie algebra]] is a self-Koszul dual.

  * More generally, a singular block of [[parabolic category O]] is dual to a different singular block of parabolic category O where the combinatorial data determining the central character and finiteness conditions switch.

* Braden, Licata, Proudfoot and Webster gave a combinatorial construction of a large family of Koszul dual algebras in [Gale duality and Koszul duality](http://arxiv.org/abs/0806.3256).

## Koszul duality between D-modules and Ω-modules

An important special case of Koszul duality
establishes a Quillen equivalence between model categories of D-modules
and Ω-modules.
This was first observed by Kapranov.

Here $D$ is the sheaf of differential operators
on a smooth manifold or a smooth variety
and $\Omega$ is the sheaf of differential forms on the same
manifold or variety.
Both $D$ and $\Omega$ are equipped with their canonical filtrations
(differential operators of order at most~$k$
respectively differential forms of degree at least~$k$)
and all constructions below work with sheaves
of filtered chain complexes.

The equivalence is implemented by tensoring with a certain filtered
$\Omega$-$D$-bimodule $DR$.
If we discard the differential, $DR=\Omega\otimes D$ as a filtered graded bimodule.
The differential is canonically determined by its degree 0
component, where we take the coevaluation map $O\to \Omega^1\otimes D^1_0$,
where $D^1_0$ denotes differential operators of order at most~1
with vanishing constant term, i.e., vector fields.

This equivalence allows one to define [[six operations]]
on D-modules by transfering them from Ω-modules,
where they can be defined in the usual manner,
since differential forms can be pulled back along maps,
unlike differential operators.

This fully explains the somewhat unintuitive explicit
formulas for the [[six operations]] on D-modules.

## Related concepts

* [[bar and cobar construction]]

* [[holography as Koszul duality]]

## References

Other historical references on Koszul duality include

* A. A. Beilinson, V. A. Ginsburg, V. V. Schechtman, _Koszul duality_,  J. Geom. Phys.  5  (1988),  no. 3, 317--350 [MR1048505](http://www.ams.org/mathscinet-getitem?mr=1048505) <a href="http://dx.doi.org/10.1016/0393-0440(88)90028-9">doi:10.1016/0393-0440(88)90028-9</a>

* [[Alexander Beilinson]], [[Victor Ginzburg]], [[Wolfgang Soergel]], _Koszul duality patterns in representation theory_,  J. Amer. Math. Soc.  9  (1996),  no. 2, 473--527 [corrigenda](http://home.mathematik.uni-freiburg.de/soergel/PReprints/KorrBGS.pdf)

Koszul duality is also discussed in 

* [[John Baez]], [TWF Week 238](http://math.ucr.edu/home/baez/week238.html), [Week 239](http://math.ucr.edu/home/baez/week239.html)

* _The Everything Seminar_ , _[koszul-duality-and-lie-algebroids](http://cornellmath.wordpress.com/2008/03/25/koszul-duality-and-lie-algebroids)_ 

* MathOverflow: [What is Koszul duality?](http://mathoverflow.net/questions/329/what-is-koszul-duality), [Beilinson-Bernstein and Koszul duality](http://mathoverflow.net/questions/309/beilinson-bernstein-and-koszul-duality), [what-extra-conditions-are-necessary-for-the-following-version-of-koszul-duality](http://mathoverflow.net/questions/67909/what-extra-conditions-are-necessary-for-the-following-version-of-koszul-duality)
* David Eisenbud, Gunnar Fl&#248;ystad, Frank-Olaf Schreyer, _Sheaf cohomology and free resolutions over 
exterior algebras_,  Trans. Amer. Math. Soc. 355 (2003), 4397-4426 [MR1990756](http://www.ams.org/mathscinet-getitem?mr=1990756) [doi](http://dx.doi.org/10.1090/S0002-9947-03-03291-4)
* Tyler Foster, Po Hu, Igor Kriz, _D-structures and derived Koszul duality for unital operad algebras_, [arxiv./1507.07151](http://arxiv.org/abs/1507.07151)


A "curved" generalization is discussed in

* Joseph Hirsh, Joan Mill&#232;s, _Curved Koszul duality theory_, Max Planck preprint MPIM2010-104, [pdf](http://www.mpim-bonn.mpg.de/preprints/send?bid=4217)
* Gunnar Fl&#248;ystad, _Koszul duality and equivalences of categories_,  Trans. Amer. Math. Soc. __358__ (2006), 2373-2398 [math.AG/0012264](http://arxiv.org/abs/math/0012264)
[MR2204036](http://www.ams.org/mathscinet-getitem?mr=2204036)
[doi](http://dx.doi.org/10.1090/S0002-9947-05-04035-3)

[[Bernhard Keller]] and his student Lef&#232;vre-Hasegawa described rather general framework for Koszul duality using dg-(co)algebras and [[twisting cochain]]s:

* [[Bernhard Keller]], _Koszul duality and coderived categories (after Lef&#232;vre-Hasegawa)_ (2003) [abstract](http://www.math.jussieu.fr/~keller/publ/kdcabs.html) [dvi](http://www.math.jussieu.fr/~keller/publ/kdc.dvi) [pdf](http://www.math.jussieu.fr/~keller/publ/kdc.pdf) [ps](http://www.math.jussieu.fr/~keller/publ/kdc.ps)

See also:



* Kenji Lef&#232;vre-Hasegawa, _Sur les A-infini cat&#233;gories_, [pdf](http://people.math.jussieu.fr/~keller/lefevre/TheseFinale/tel-00007761.pdf) [math/0310337](http://arxiv.org/abs/math.CT/0310337)
* Leonid Positselski, _Two kinds of derived categories, Koszul duality, and comodule-contramodule correspondence_, [arxiv/0905.2621](http://arxiv.org/abs/0905.2621)

* [[Dev Sinha]], _Koszul duality in algebraic topology - an historical perspective_, J. Homotopy Relat. Struct. (2013) 8: 1 ([arXiv:1001.2032](https://arxiv.org/abs/1001.2032))


* Aaron M Royer, _Generalized string topology and derived Koszul duality_, [arxiv/1306.6708](http://arxiv.org/abs/1306.6708)


* [[Mikhail Kapranov]], _On DG-modules over the de Rham complex and the vanishing cycles functor_, Algebraic Geometry, 
Lecture Notes in Mathematics __1479__, 1991, pp 57-86 


* [[Theo Johnson-Freyd]], _Exact triangles, Koszul duality, and coisotropic boundary conditions_, [arxiv/1608.08598](https://arxiv.org/abs/1608.08598)

* [[Jonathan Beardsley]], [[Maximilien Péroux]], _Koszul Duality in Higher Topoi_ ([arXiv:1909.11724](https://arxiv.org/abs/1909.11724))


A form of Koszul duality for dg-categories has been given by Holstein and Lazarev.

* [[Julian Holstein]] and A. Lazarev, _Categorical Koszul duality_ [Arxiv 2006.01706](https://arxiv.org/pdf/2006.01705.pdf)

[[!redirects Koszul dual]]