
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
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

The [[generalized cohomology theory]] which is [[Brown representability theorem|represented]] by the [[sphere spectrum]] is also called _stable cohomotopy_, as it is the [[stable homotopy theory]] version of [[cohomotopy]]. 

Equivalenty, it is the cohomolgical [[duality|dual]] concept to [[stable homotopy homology theory]].

By the [[Pontryagin-Thom theorem]] this is equivalently [[framed manifold|framed]] [[cobordism cohomology theory]].

## Properties

### As algebraic K-theory over $\mathbb{F}_1$
 {#AsAlgebraicKTheoryOverTheFieldWithOneElement}

The following is known as the _Barratt-Priddy-Quillen theorem_:

+-- {: .num_prop #StableCohomotopyIsKTheoryOfFinSet}
###### Proposition
**([[stable cohomotopy]] is K-theory of [[FinSet]])**

Let $\mathcal{C} = $ [[FinSet]] be a [[skeleton]] of the category of [[finite sets]], regarded as a [[permutative category]]. Then the [[K-theory of a permutative category|K-theory of this permutative category]] 

$$
  K(FinSet) \;\simeq\; \mathbb{S}
$$

is represented by the [[sphere spectrum]], hence is stable cohomotopy.

=--

This is due to [Barratt-Priddy 72](#BarrattPriddy72) reproved in [Segal 74, Prop. 3.5](#Segal74). See also [Priddy 73](#Priddy73), [Glasman 13](#Glasman13).

+-- {: .num_remark #StableCohomotopyIsAlgebraicKTheoryOverFieldWithOneElement}
###### Remark
**([[stable cohomotopy]] as [[algebraic K-theory]] over the [[field with one element]])**

Notice that for $F$ a [[field]], the [[K-theory of a permutative category]] of its [[category of modules]] $F Mod$ is its [[algebraic K-theory]] $K F$ (see [this example](K-theory+of+a+permutative+category#OrdinaryAlgebraicKTheoryFromPermutativeCategoryOfProjectiveModules))

$$
  K F \;\simeq\; K(F Mod)
  \,.
$$ 

Now ([[pointed sets|pointed]]) [[finite sets]] may be regarded as the modules over the "[[field with one element]]" $\mathbb{F}_1$ (see [there](field+with+one+element#Modules)):

$$
  \mathbb{F}_1 Mod
  \;=\;
  FinSet^{\ast/}
$$

If this is understood, example \ref{StableCohomotopyIsKTheoryOfFinSet} says that [[stable cohomotopy]] is the algebraic K-theory of the [[field with one element]]:

$$
  \mathbb{S} \;\simeq\; K \mathbb{F}_1
  \,.
$$

=--

This perspective is highlighted for instance in ([Deitmar 06, p. 2](#Deitmar06), [Guillot 06](#Guillot06), [Mahanta 17](#Mahanta17), [Dundas-Goodwillie-McCarthy 13, II 1.2](#DundasGoodwillieMcCarthy13), [Morava](#MoravaSomeBackground), [Connes-Consani 16](#ConnesConsani16)).



The perspective that the [[K-theory]] $K \mathbb{F}_1$ over $\mathbb{F}_1$ should be [[stable Cohomotopy]] has been highlighted in ([Deitmar 06, p. 2](#Deitmar06), [Guillot 06](#Guillot06), [Mahanta 17](#Mahanta17), [Dundas-Goodwillie-McCarthy 13, II 1.2](#DundasGoodwillieMcCarthy13), [Morava](#MoravaSomeBackground), [Connes-Consani 16](#ConnesConsani16)). Generalized to [[equivariant stable homotopy theory]], the statement that [[equivariant K-theory]] $ K_G \mathbb{F}_1$ over $\mathbb{F}_1$ should be [[equivariant stable Cohomotopy]] is discussed in [Chu-Lorscheid-Santhanam 10, 5.3](#ChuLorscheidSanthanam10).

[[!include Segal completion -- table]]



### Kahn-Priddy theorem

The [[Kahn-Priddy theorem]] characterizes a comparison map between stable cohomotopy and [[cohomology]] with [[coefficients]] in the infinite [[real projective space]] $\mathbb{R}P^\infty \simeq B \mathbb{Z}/2$.


### Boardman homomorphisms


Consider the [[unit]] morphism

$$
  \mathbb{S} \longrightarrow H \mathbb{Z}
$$

from the [[sphere spectrum]] to the [[Eilenberg-MacLane spectrum]] of the [[integers]]. For any [[topological space]]/[[spectrum]] postcomposition with this morphism induces [[Boardman homomorphisms]] of [[cohomology groups]] (in fact of [[commutative rings]])

\[
  \label{BoardmandCohomotopyToOrdinaryCohomology}
  b^n
  \;\colon\;
  \pi^n(X)
  \longrightarrow
  H^n(X, \mathbb{Z})
\]

from the [[stable cohomotopy]] of $X$ in degree $n$ to its [[ordinary cohomology]] in degree $n$.

+-- {: .num_prop #BoundsOnCoKernelOfBoardmandFromStableCohomotopyToOrdinaryCohomology}
###### Proposition
**(bounds on ([[cokernel|co-]])[[kernel]] of [[Boardman homomorphism]] from [[stable cohomotopy]] to [[integral cohomology]])**

If $X$ is a [[CW-spectrum]] which

1. is $(m-1)$-[[n-connected object of an (infinity,1)-topos|(m-1)-connected]]

1. of dimension $d \in \mathbb{N}$

then 

1. the [[kernel]] of the [[Boardman homomorphism]] $b^n$ (eq:BoardmandCohomotopyToOrdinaryCohomology) for   
   
   $$
     m \leq n\leq d -1
   $$

   is a $\overline{\rho}_{d-n}$-[[torsion subgroup|torsion group]]:

   $$
     \overline{\rho}_{d-n} ker(b^n) \;\simeq\; 0
   $$


1. the [[cokernel]] of the [[Boardman homomorphism]] $b^n$ (eq:BoardmandCohomotopyToOrdinaryCohomology) for 

   $$
     m \leq n  \leq d - 2
   $$

   is a $\overline{\rho}_{d-n-1}$-[[torsion subgroup|torsion group]]:

   $$
     \overline{\rho}_{d-n-1} coker(b^n) \;\simeq\; 0
   $$

where

$$
  \overline{\rho}_{i}
   \;\coloneqq\;
   \left\{
   \array{
     1 &\vert& i\leq 1
     \\
     \underoverset{j = 1}{i}{\prod}  
       exp\left( 
         \pi_j\left( \mathbb{S}\right)
       \right)
     &\vert&
     \text{otherwise}
   }
   \right.
$$

is the [[multiplication|product]] of the [[exponent of a group|exponents]] of the [[stable homotopy groups of spheres]] in [[positive number|positive]] degree $\leq i$.
  
=--

([Arlettaz 04, theorem 1.2](#Arlettaz04))



## Related concepts

[[!include flavours of cohomotopy -- table]]



* [[Boardman homomorphism]]


## References

The basic concept appears in

* {#Adams74} [[Frank Adams]], part III, section 6 of _[[Stable homotopy and generalised homology]]_, 1974

The identification of stable cohomotopy with the [[K-theory of a permutative category|K-theory of the permutative category]] of [[finite set]] is due to 

* {#BarrattPriddy72} [[Michael Barratt]], [[Stewart Priddy]], _On the homology of non-connected monoids and their associated groups_, Commentarii Mathematici Helvetici, December 1972, Volume 47, Issue 1, pp 1–14 ([doi:10.1007/BF02566785](https://doi.org/10.1007/BF02566785))

* {#Segal74} [[Graeme Segal]], _Categories and cohomology theories_, Topology vol 13, pp.  293-312,  1974  ([pdf](http://ncatlab.org/nlab/files/SegalCategoriesAndCohomologyTheories.pdf))

see also

* {#Priddy73} [[Stewart Priddy]], _Transfer, symmetric groups, and stable homotopy theory_, in _Higher K-Theories_, Springer, Berlin, Heidelberg, 1973. 244-255 ([pdf](https://link.springer.com/content/pdf/10.1007/BFb0067060.pdf))

* {#Glasman13} [[Saul Glasman]], _The multiplicative Barratt-Priddy-Quillen theorem and beyond_, talk 2013 ([pdf](http://math.mit.edu/~sglasman/bpq-beamer.pdf))

The resulting interpretation of stable cohomotopy as [[algebraic K-theory]] over the [[field with one element]] is amplified in the following texts:

* {#DundasGoodwillieMcCarthy13} [[Bjørn Dundas]], [[Thomas Goodwillie]], [[Randy McCarthy]], chapter II, section 1.2 of  _The local structure of algebraic K-theory_, Springer 2013 ([pdf](http://math.mit.edu/~nrozen/juvitop/dundas.pdf))

* {#Deitmar06} [[Anton Deitmar]], _Remarks on zeta functions and K-theory over $\mathbb{F}_1$_ ([arXiv:math/0605429](https://arxiv.org/abs/math/0605429))

* {#Guillot06} [[Pierre Guillot]], _Adams operations in cohomotopy_ ([arXiv:0612327](https://arxiv.org/abs/math/0612327))

* {#Mahanta17} [[Snigdhayan Mahanta]], _G-theory of $\mathbb{F}_1$-algebras I: the equivariant Nishida problem_, J. Homotopy Relat. Struct. 12 (4), 901-930, 2017 ([arXiv:1110.6001](https://arxiv.org/abs/1110.6001))

* {#ChuLorscheidSanthanam10} Chenghao Chu, [[Oliver Lorscheid]], Rekha Santhanam, _Sheaves and K-theory for $\mathbb{F}_1$-schemes_, Advances in Mathematics, Volume 229, Issue 4, 1 March 2012, Pages 2239-2286 ([arxiv:1010.2896](https://arxiv.org/abs/1010.2896))


see also

* {#MoravaSomeBackground} [[Jack Morava]], _Some background on Manin's theorem $K(\mathbb{F}_1) \sim \mathbb{S}$_ ([pdf](http://www.alainconnes.org/docs/Morava.pdf), [[MoravaSomeBackground.pdf:file]])

* {#ConnesConsani16} [[Alain Connes]], [[Caterina Consani]], _Absolute algebra and Segal's Gamma sets_, Journal of Number Theory 162 (2016): 518-551 ([arXiv:1502.05585](https://arxiv.org/abs/1502.05585))

* {#Berman18} John D. Berman, p. 92 of _Categorified algebra and equivariant homotopy theory_, PhD thesis 2018  ([pdf](http://www.people.virginia.edu/~jdb8pc/Thesis.pdf))


The [[Kahn-Priddy theorem]] is due to

* {#KahnPriddy72} [[Daniel Kahn]], [[Stewart Priddy]], _Applications of the transfer to stable homotopy theory_, Bull. Amer. Math. Soc. Volume 78, Number 6 (1972), 981-987 ([Euclid](https://projecteuclid.org/euclid.bams/1183534135))



The relation to [[β-rings]] is discussed in 

* E. Vallejo, _Polynomial operations from Burnside rings to representation functors_, J. Pure Appl. Algebra, 65 (1990), pp. 163–190.

* E. Vallejo, _Polynomial operations on stable cohomotopy_, Manuscripta Math., 67 (1990), pp. 345–365

* E. Vallejo, _The free β-ring on one generator, J. Pure Appl. Algebra, 86 (1993), pp. 95–108.

* [Guillot 06](#Guillot06)

see also

* [[Jack Morava]], Rekha Santhanam, _Power operations and absolute geometry_ ([pdf](http://www.lemiller.net/media/slidesconf/AbsolutePower.pdf))


Discussion of [[Boardman homomorphisms]] from stable cohomotopy is in 

* {#Arlettaz04} Dominique Arlettaz, _The generalized Boardman homomorphisms_, Central European Journal of Mathematics March 2004, Volume 2, Issue 1, pp 50-56


A lift of [[Seiberg-Witten invariants]] to classes in [[circle group]]-[[equivariant stable cohomotopy]] is discussed in

* _A stable cohomotopy refinement of Seiberg-Witten invariants: I_ ([arXiv:math/0204340](http://arxiv.org/abs/math/0204340))

* _A stable cohomotopy refinement of Seiberg-Witten invariants: II_ ([arXiv:math/0204267](http://arxiv.org/abs/math/0204267))


[[!redirects stable cohomotopy theory]]

[[!redirects stable Cohomotopy]]

[[!redirects stable cohomotopy cohomology theory]]
[[!redirects stable Cohomotopy cohomology theory]]

