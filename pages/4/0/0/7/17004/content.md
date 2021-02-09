
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Spheres
+--{: .hide}
[[!include spheres -- contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

The [[generalized cohomology theory]] which is [[Brown representability theorem|represented]] by the [[sphere spectrum]] is also called _stable cohomotopy_, as it is the [[stable homotopy theory]] version of [[cohomotopy]]. 

Equivalently, it is the cohomological [[duality|dual]] concept to [[stable homotopy homology theory]].

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

### The third stable framed bordism group

The [[third stable homotopy group of spheres]] is the [[cyclic group]] of [[order of a group|order]] 24:

$$
  \array{
    \pi_3^s &\simeq& \mathbb{Z}/24
    \\
    [h_{\mathbb{H}}] &\leftrightarrow& [1]
  }
$$

where the generator $[1] \in \mathbb{Z}/24$ is represented by the [[quaternionic Hopf fibration]] $S^7 \overset{h_{\mathbb{H}}}{\longrightarrow} S^4$.

Under the [[Pontrjagin-Thom isomorphism]], identifying the [[stable homotopy groups of spheres]] with the [[bordism ring]] $\Omega^{fr}_\bullet$ of [[stable framing|stably framed]] manifolds (see at _[[MFr]]_), this generator is represented by the [[3-sphere]] (with its left-invariant framing induced from the identification with the [[Lie group]] [[SU(2)]] $\simeq$ [[Sp(1)]] )


$$
  \array{
    \pi_3^s & \simeq & \Omega_3^{fr} 
    \\
    [h_{\mathbb{H}}] & \leftrightarrow & [S^3]
    \,.
  }
$$

Moreover, the relation $2 4 [S^3] \,\simeq\, 0$ is represented by the [[complement]] of 24 [[open balls]] inside [[generalized the|the]] [[K3]]-manifold ([MO:a/44885/381](https://mathoverflow.net/a/44885/381), [MO:a/218053/381](https://mathoverflow.net/a/218053/381)).




### Kahn-Priddy theorem

The [[Kahn-Priddy theorem]] characterizes a comparison map between stable cohomotopy and [[cohomology]] with [[coefficients]] in the infinite [[real projective space]] $\mathbb{R}P^\infty \simeq B \mathbb{Z}/2$.


### Boardman homomorphisms

#### To ordinary cohomology

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


#### To topological modular forms

Write $\mathbb{S}$ for the [[sphere spectrum]] and _[[tmf]]_ for the [[connective spectrum]] of [[topological modular forms]].

Since [[tmf]] is an [[E-∞ ring|E-∞]][[ring spectrum]], there is an essentially unique homomorphism of [[E-∞ ring|E-∞]][[ring spectra]]

$$
  \mathbb{S}
  \overset{e_{tmf}}{\longrightarrow}
  tmf
  \,.
$$

Regarded as a morphism of [[generalized homology]]-theories, this is called the [[Hurewicz homomorphism]], or rather the [[Boardman homomorphism]] for $tmf$

+-- {: .num_prop}
###### Proposition
**(Boardman homomorphism in $tmf$ is 6-connected)**

The [[Boardman homomorphism in tmf]]

$$
  \mathbb{S}
  \overset{e_{tmf}}{\longrightarrow}
  tmf
$$

induces an [[isomorphism]] on [[stable homotopy groups]] 
(hence from the [[stable homotopy groups of spheres]] to the stable homotopy groups of tmf), up to degree 6:

$$
  \pi_{\bullet \leq 6}(\mathbb{S})
  \underoverset{\simeq}{\pi_{\bullet \leq 6}(e_{tmf})}{\longrightarrow}
  \pi_{\bullet\leq 6}(tmf)
  \,.
$$


=--

([Hopkins 02, Prop. 4.6](Boardman+homomorphism+in+tmf#Hopkins02), [DFHH 14, Ch. 13](Boardman+homomorphism+in+tmf#DFHH14))



## Related concepts

[[!include flavours of cohomotopy -- table]]

\linebreak

* [[Boardman homomorphism]]

* [[Spanier-Whitehead duality]]

\linebreak

[[!include flavours of cobordism cohomology theories -- table]]


## References

The concept of stable Cohomotopy as such:

* {#Adams74} [[Frank Adams]], part III, section 6, p. 204 of: _[[Stable homotopy and generalised homology]]_, 1974

* [[John Rognes]], p. 1 of: _The sphere spectrum_, 2004 ([[RognesSphereSpectrum.pdf:file]])

Discussion of stable Cohomotopy as [[framed manifold|framed]] [[cobordism cohomology theory]]:

* {#Stong68} [[Robert Stong]], Chapter IV, Example 1, p. 40 of _Notes on Cobordism theory_, Princeton University Press, 1968 ([toc pdf](http://pi.math.virginia.edu/StongConf/Stongbookcontents.pdf), [ISBN:9780691649016](http://press.princeton.edu/titles/6465.html))

Discussion of stable Cohomotopy of [[Lie groups]]:

* C. T. Stretch, _Stable cohomotopy and cobordism of abelian groups_, Mathematical Proceedings of the Cambridge Philosophical Society, Volume 90, Issue 2 September 1981, pp. 273-278 ([doi:10.1017/S0305004100058734](https://doi.org/10.1017/S0305004100058734))

* Ken-ichi Maruyama, _$e$-invariants on the stable cohomotopy groups of Lie groups_, Osaka J. Math. Volume 25, Number 3 (1988), 581-589 ([euclid:ojm/1200780982](https://projecteuclid.org/euclid.ojm/1200780982))

* Sławomir Nowak, _Stable cohomotopy groups of compact spaces_, Fundamenta Mathematicae 180 (2003), 99-137 ([doi:10.4064/fm180-2-1](https://www.impan.pl/en/publishing-house/journals-and-series/fundamenta-mathematicae/all/180/2))


The identification of stable cohomotopy with the [[K-theory of a permutative category|K-theory of the permutative category]] of [[finite sets]] is due to 

* {#BarrattPriddy72} [[Michael Barratt]], [[Stewart Priddy]], _On the homology of non-connected monoids and their associated groups_, Commentarii Mathematici Helvetici, December 1972, Volume 47, Issue 1, pp 1–14 ([doi:10.1007/BF02566785](https://link.springer.com/article/10.1007/BF02566785))

* {#Segal74} [[Graeme Segal]], _Categories and cohomology theories_, Topology vol 13, pp.  293-312,  1974  (<a href="https://doi.org/10.1016/0040-9383(74)90022-6">doi:10.1016/0040-9383(74)90022-6</a>, [pdf](http://ncatlab.org/nlab/files/SegalCategoriesAndCohomologyTheories.pdf))

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

Discussion of stable Cohomotopy as [[framed manifold|framed]] [[cobordism cohomology theory]]:

* {#ConnerFloyd66} [[Pierre Conner]], [[Edwin Floyd]], Section 5 of: _[[The Relation of Cobordism to K-Theories]]_, Lecture Notes in Mathematics __28__ Springer 1966 ([doi:10.1007/BFb0071091](https://link.springer.com/book/10.1007/BFb0071091), [MR216511](http://www.ams.org/mathscinet-getitem?mr=216511))




The relation to [[β-rings]] is discussed in 

* E. Vallejo, _Polynomial operations from Burnside rings to representation functors_, J. Pure Appl. Algebra, 65 (1990), pp. 163–190.

* E. Vallejo, _Polynomial operations on stable cohomotopy_, Manuscripta Math., 67 (1990), pp. 345–365

* E. Vallejo, _The free β-ring on one generator, J. Pure Appl. Algebra, 86 (1993), pp. 95–108.

* [Guillot 06](#Guillot06)

see also

* [[Jack Morava]], Rekha Santhanam, _Power operations and absolute geometry_ ([pdf](http://www.lemiller.net/media/slidesconf/AbsolutePower.pdf))


Discussion of [[Boardman homomorphisms]] from stable cohomotopy is in 

* {#Arlettaz04} [[Dominique Arlettaz]], _The generalized Boardman homomorphisms_, Central European Journal of Mathematics March 2004, Volume 2, Issue 1, pp 50-56 ([doi:10.2478/BF02475949](https://doi.org/10.2478/BF02475949))


A lift of [[Seiberg-Witten invariants]] to classes in [[circle group]]-[[equivariant stable cohomotopy]] is discussed in

* _A stable cohomotopy refinement of Seiberg-Witten invariants: I_ ([arXiv:math/0204340](http://arxiv.org/abs/math/0204340))

* _A stable cohomotopy refinement of Seiberg-Witten invariants: II_ ([arXiv:math/0204267](http://arxiv.org/abs/math/0204267))


[[!redirects stable Cohomotopy]]


[[!redirects stable cohomotopy theory]]
[[!redirects stable Cohomotopy theory]]

[[!redirects stable cohomotopy cohomology theory]]
[[!redirects stable Cohomotopy cohomology theory]]

[[!redirects MFr]]

[[!redirects framed bordism theory]]
[[!redirects framed bordism theories]]

[[!redirects framed cobordism homology theory]]
[[!redirects framed cobordism homology theories]]

[[!redirects framed bordism homology theory]]
[[!redirects framed bordism homology theories]]



[[!redirects framed bordism ring]]
[[!redirects framed bordism rings]]

[[!redirects framed cobordism ring]]
[[!redirects framed cobordism rings]]




