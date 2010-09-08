# Koszul duality
* tic
{: toc}


__Koszul duality__ is a duality and phenomenon generalizing the duality between the symmetric and exterior algebra of a vector space to so-called quadratic [[differential graded algebra]]s (which can be obtained as a free dga module an ideal of relations which live in degree 2). For a pair of Koszul dual algebras, there is a correspondence between certain parts of their derived categories (precise formulation involves some finiteness conditions). In a setup in which one of the algebras is replaced by a cocomplete dg coalgebra, there is a formulation free of finiteness conditions, but involving [[twisting cochain]] (see that entry).


##Informal discussion

There are a lot of algebras whose derived categories are equivalent in surprising ways.  [[Morita equivalences]] are pretty simple, especially for finite dimensional algebras; essentially the only free parameter is the dimension of the object.

Namely, if $A Mod$ and $B Mod$ are equivalent, then the image of $A$ as a module over itself is a [[projective object|projective]] [[generator]] of $B Mod$, and for a finite-dimensional algebra, essentially the only thing you can do is take several copies of the [[indecomposable object|indecomposible]] projectives of $B$.

On the other hand, if you take the derived category of [[differential graded module|dg-modules]] over $A$ (the dg part of this is not a huge deal; it's just that they're very close to, but a bit better behaved than, actual derived/[[triangulated categories]], which are just crude truncations of truly funtorial dg/$A_\infty$ versions), this is equivalent to the category of dg-modules over the [[endomorphism algebra]] (this is in the dg sense, so it's a dg-algebra whose cohomology is the $Ext$ algebra) of *any* generating object.  There are a *lot* more generating objects than projective generators, so there are a lot of derived equivalences.

In particular, let $A$ be a finite dimensional algebra $A$, than an  obvious not-very-projective generating object is the sum of all the [[simple modules]], say $L$.  As mentioned above, there's an equivalence $A dg Mod = \mathrm{Ext}(L,L) dg Mod$, just given by taking $\mathrm{Ext}(L,-)$.   

In general, $\mathrm{Ext}(L,L)$ is in a very complicated object (for example, often for [[group algebras]] over [[finite field]]s), but sometimes it turns out to be nice.  For example, if $A$ is an  [[exterior algebra]], you'll get a [[polynomial ring]] on the dual vector space.  Another (closely related) example is that the cohomology of a [[reductive group]] (over $\mathbb{C}$) is Koszul dual to the cohomology of its classifying space.

One way to ensure that $\mathrm{Ext}(L,L)$ is nice is if the algebra $A$ is [[graded algebra|graded]]. Then $\mathrm{Ext}(L,L)$ inherits an "internal" grading in addition to its homological one.  If these coincide, then $A$ is called _Koszul_. 

In this case, $B=\mathrm{Ext}(L,L)$ is forced to be formal (if it had any interesting $A_\infty$ operations, they would break the grading), so you're dealing with a derived equivalence between actual algebras, though you have to be a bit careful about the dg-issues.  Thus the derived category of usual modules over $A$ is equivalent to dg-modules over $B$ (with its unique grading) and vice versa.  This can be fixed by taking graded modules on both sides.


##Examples

* The most famous example of Koszul dual algebras are the [[exterior algebra]] $Alt^{\bullet}V[-1]$ and the [[polynomial algebra]] $Sym^\bullet V^*[-2]$.

* A regular block of [[category O]] for any [[semisimple Lie algebra]] is a self-Koszul dual.

  * More generally, a singular block of [[parabolic category O]] is dual to a different singular block of parabolic category O where the combinatorial data determining the central character and finiteness conditions switch.

* Braden, Licata, Proudfoot and Webster gave a combinatorial construction of a large family of Koszul dual algebras in [Gale duality and Koszul duality](http://front.math.ucdavis.edu/0806.3256).


##Generalization to operads

There is a further generalization to [[quadratic operad]]s, predicted in 

* [[Maxim Kontsevich|M. Kontsevich]], _Formal (non)commutative symplectic geometry_,  The Gel&#697;fand Mathematical Seminars, 1990--1992,  173--187, Birkh&#228;user, Boston, MA, 1993 (cf. [[formal noncommutative symplectic geometry]]).

and developed in

* [[Victor Ginzburg]], [[Mikhail Kapranov]], _Koszul duality for operads_, Duke Math. J. __76__ (1994),  no. 1, 203--272; reprint [arxiv/0709.1228](http://arxiv.org/abs/0709.1228); *Erratum to: Koszul duality for operads*, Duke Math. J. __80__ (1995),  no. 1, 293. 

##Other references

Other historical references on Koszul duality include

* A. A. Be&#301;linson, V. A. Ginsburg, V. V. Schechtman, _Koszul duality_,  J. Geom. Phys.  5  (1988),  no. 3, 317--350.

* A. Beilinson, V. Ginzburg, W. Soergel, _Koszul duality patterns in representation theory_,  J. Amer. Math. Soc.  9  (1996),  no. 2, 473--527. 

Koszul duality is also discussed in [[John Baez]]' [This Week's Finds in Mathematical Physics](http://math.ucr.edu/home/baez/TWF.html):

* [Week 238](http://math.ucr.edu/home/baez/week238.html), [Week 239](http://math.ucr.edu/home/baez/week239.html)

in "the Everything Seminar" [koszul-duality-and-lie-algebroids](http://cornellmath.wordpress.com/2008/03/25/koszul-duality-and-lie-algebroids) and at MathOverflow: [What is Koszul duality?](http://mathoverflow.net/questions/329/what-is-koszul-duality), [Beilinson-Bernstein and Koszul duality](http://mathoverflow.net/questions/309/beilinson-bernstein-and-koszul-duality)