
#Contents#
* table of contents
{:toc}

## Idea

(...) see at _[[chiral de Rham complex]]_ (...)

## Properties

### Relation to the Witten genus
 {#RelationToTheWittenGenus}

For $U \subset \mathbb{C}$ an [[open subset]] of the [[complex plane]] then the space $\mathcal{D}^{ch}(U)$ of chiral differential operators on $U$ is naturally a [[super vertex operator algebra]]. For $X$ a [[complex manifold]] such that its [[first Chern class]] and [[second Chern class]] vanish over the [[rational numbers]], then this assignment gives a [[sheaf of vertex operator algebras]] $\mathcal{D}^{ch}_X(-)$ on $X$. Its [[cochain cohomology]] $H^\bullet(\mathcal{D}^{ch}_X)$ is itself a [[super vertex operator algebra]] and its super-[[Kac-Weyl character]] is proportional to the [[Witten genus]] $w(X)$ of $X$:

$$
  char H^\bullet(\mathcal{D}^{ch}_X)\propto w(X)
  \,.
$$

Physically this result is understood by observing that $\mathcal{D}^{ch}_X$is the sheaf of [[quantum observables]] of the [[topological twist|topologically twisted]] [[2d (2,0)-superconformal QFT]] (see there for more on this) of which the [[Witten genus]] is (the [[large volume limit]] of) the [[partition function]].

See ([Cheung 10](#Cheung10)) for a brief review (where the problem of generalizing of this construction to [[sheaves of vertex operator algebras]] over more general [[string structure]] manifolds is addressed.)

### Relation to formal loop space

With $X$ a suitable scheme, its [[formal loop space]] $L_inf X$ in the sense of ([Kapranov-Vasserot I](#KapranovVasserotI)) has a [[Tate structure]] and hence an associated [[determinantal gerbe]] $Det_{L_{inf} X}$ with [[band]] $\mathcal{O}^\ast_{L_{inf} X}$. According to 
([Kapranov-Vasserot IV](#KapranovVasserotIV)) this [[gerbe]] is essentially identified with the [[gerbe]] $CDO_X$ of chiral differential operators on $X$. 


## Related concepts

* [[chiral de Rham complex]], [[vertex operator algebra]], [[chiral algebra]]

* [[formal loop space]]

## References

The original articles are

* {#GMS} [[Vassily Gorbounov]], [[Fyodor Malikov]], [[Vadim Schechtman]], _Gerbes of chiral differential operators_  Math. Res. Lett. __7__ (2000),  no. 1, 55--66, [MR2002c:17040](http://www.ams.org/mathscinet-getitem?mr=2002c:17040), [math.AG/9906117](http://arxiv.org/abs/math/9906117); _Gerbes of chiral differential operators. II. Vertex algebroids_, Invent. Math. __155__ (2004), no. 3, 605--680, [MR2005e:17047](http://www.ams.org/mathscinet-getitem?mr=2005e:17047), [math.AG/0003170](http://arxiv.org/abs/math/0003170), [doi](http://dx.doi.org/10.1007/s00222-003-0333-4); _Gerbes of chiral differential operators. III_, in: The orbit method in geometry and physics (Marseille, 2000),  73--100, Progr. Math. __213__, Birkh&#228;user 2003, [MR2005a:17028](http://www.ams.org/mathscinet-getitem?mr=2005a:17028), [math.AG/0005201](http://arxiv.org/abs/math/0005201), _On chiral differential operators over homogeneous spaces_, Int. J. Math. Math. Sci. __26__ (2001), no. 2, 83--106, [MR2002g:14020](http://www.ams.org/mathscinet-getitem?mr=2002g:14020), [math.AG/0008154](http://arxiv.org/abs/math/0008154), [doi](http://dx.doi.org/10.1155/S0161171201020051)

Surveys and further developments include

* Andrew R. Linshaw, _Introduction to invariant chiral differential operators_, in: Vertex operator algebras and related areas,  157--168, Contemp. Math. __497__, Amer. Math. Soc. 2009; _Invariant chiral differential operators and the $W_3$ algebra _, J. Pure Appl. Algebra __213__ (2009), 632-648, [arxiv/0710.0194](http://arxiv.org/abs/0710.0194), [MR2010b:17035](http://www.ams.org/mathscinet-getitem?mr=2010b:17035), [doi](http://dx.doi.org/10.1016/j.jpaa.2008.08.006)

* {#Cheung10} [[Pokman Cheung]], _Chiral differential operators and topology_, [arxiv/1009.5479](http://arxiv.org/abs/1009.5479)

The relation to [[formal loop space]] geometry is discussed in

* {#KapranovVasserotI} [[Mikhail Kapranov]], E. Vasserot, _Vertex algebras and the formal loop space_ Publications Math&#233;matiques de l'IH&#201;S,
100 (2004), 209&#8211;269. ([arXiv:math/0107143](http://arxiv.org/abs/math/0107143))
 

* [[Mikhail Kapranov]], E. Vasserot, _Formal Loops II : the local Riemann-Roch theorem for determinantal gerbes_, Ann. Sci. ENS, ([arXiv:math/0509646](http://arxiv.org/abs/math/0509646))

* [[Mikhail Kapranov]], E. Vasserot, _Formal loops III: Factorizing functions and the Radon transform_ ([arXiv:math/0510476](http://arxiv.org/abs/math/0510476))

* {#KapranovVasserotIV} [[Mikhail Kapranov]], E. Vasserot, _Formal loops IV: Chiral differential operators_ ([arXiv:math/0612371](http://arxiv.org/abs/math/0612371))
 

Tentative aspects of a generalization to [[differential geometry]] are discussed in 

* [[Pokman Cheung]], _Chiral differential operators: formal loop group actions and associated modules_ ([arXiv:1205.7089](http://arxiv.org/abs/1205.7089))


[[!redirects chiral differential operators]]