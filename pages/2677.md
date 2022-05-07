
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#F-un#
* table of contents
{:toc}

## Overview

Various phenomena in the context of  [[algebraic geometry]]/[[arithmetic geometry]] (and particularly in the context of [[algebraic groups]]) over  [[finite fields]] $\mathbb{F}_q$ turn out to make perfect sense _as expressions in $q$_ when extrapolated to the case $q=1$, and to reflect interesting (combinatorial, representation theoretical...) facts, even though, of course, there is no actual [[field]] with a single element (since in a field by definition the elements 1 and 0 are distinct).

Motivated by such observations, [[Jacques Tits]] envisioned in ([Tits 57](#Tits57)) a new kind of geometry adapted to the explanation of these identities. [[Christophe Soulé]] then expanded on Tits' ideas by introducing the notion of _field with one element_ and studying its fine arithmetic invariants. While there is no field with a single element in the standard sense of _[[field]]_, the idea is that there is some other object, denoted $\mathbb{F}_1$, such that it does make sense to speak of "geometry over $\mathbb{F}_1$". Following the French pronunciation one also writes $F_{un}$ (and is thus led to the inevitable pun).

In the [[relative point of view]] the $S$-schemes are schemes with a morphism of schemes over a base scheme $S$; but every $S$-scheme is a scheme over [[Spec(Z)]]. In __absolute algebraic geometry__ all "generalized schemes" should live over $Spec(F_1)$ and $Spec(F_1)$ should live **below** $Spec(\mathbb{Z})$; this is similar to the fact that the quotient stacks like $[*/G]$ live below the single point $*$ (there is a direct image functor from sheaves on a point to sheaves over $[*/G]$). One of the principal and very bold hopes is that the study of $F_{un}$ should lead to a natural proof of [[Riemann conjecture]] (see also MathOverflow [here](http://mathoverflow.net/questions/69389/riemann-hypothesis-via-absolute-geometry)). It was originally suggested by ([Manin 95](#Manin95)) that the [[Riemann hypothesis]] might be solved by finding an $\mathbb{F}_1$-[[analogy|analogue]] of [[André Weil]]'s proof for the case of [[arithmetic curves]] over the [[finite fields]] $\mathbb{F}_q$.

A first proposal for what a [[variety]] "over $\mathbb{F}_1$" ought to be is due to ([Soul&#233; 04](#Soule)).  After that a plethora of further proposals appeared, including ([Connes-Consani 08](#ConnesConsani08)). 

## Borger's absolute geometry
 {#BorgerAbsoluteGeometry}

Maybe an emerging consensus is that the preferred approach is [[Borger's absolute geometry]] ([Borger 09](#Borger09)). Here the structure of a [[Lambda-ring]] on a ring $R$, hence on $Spec(R) \to Spec(\mathbb{Z})$,  is interpreted as a collection of lifts of all [[Frobenius morphisms]] and hence as [[descent]] data for descent to $Spec(\mathbb{F}_1)$ (which is defined thereby).  This definition yields an [[essential geometric morphism]] of [[gros topos|gros]] [[etale toposes]]

$$
  Et(Spec(\mathbb{Z}))
   \stackrel{\overset{}{\longrightarrow}}{\stackrel{\overset{}{\longleftarrow}}{\underset{}{\longrightarrow}}}
  Et(Spec(\mathbb{F}_1))
  \,,
$$

where on the right the notation is just suggestive, the [[topos]] is a suitable one over [[Lambda-rings]]. Here the middle [[inverse image]] is the [[forgetful functor]] which forgets the Lambda structure, and its [[right adjoint]] [[direct image]] is given by the [[arithmetic jet space]] construction (via the [[ring of Witt vectors]] construction).

This proposal seems to subsume many aspects of other existing proposals (see e.g. [Le Bruyn 13](#LeBruyn13)) and stands out as yielding an "absolute [[base topos]]" $Et(Spec(\mathbb{F}_1))$ which is rich and genuinely interesting in its own right.

## Function field analogy

[[!include function field analogy -- table]]



## Algebra over $\mathbb{F}_1$
 {#AlgebraOverF1}

### Modules/Vector spaces over $\mathbb{F}_1$
 {#Modules}

It makes good sense to identify the concept of finite rank [[modules]]/[[finite-dimensional vector spaces]] over the field with one element with that of ([[pointed set|pointed]]) [[finite sets]] 

$$
  \mathbb{F}_1 Mod_{fin}
  \;\simeq\;
  Set^{\ast/}_{fin}
$$

and hence the [[symmetric group]] $\Sigma_n$ on $n$ [[elements]] with the [[general linear group]] over $\mathbb{F}_1$:

$$
  GL(n,\mathbb{F}_1)
  \;\simeq\;
  \Sigma_n
$$

(e.g. [Cohn 04, "puzzle 1"](#Cohn04), [Durov 07, 2.5.6](#Durov07), [Snyder 07](#Snyder07))

### Algebraic K-theory
 {#AlgebraicKTheory}
 
With the identification $\mathbb{F}_1 Mod \simeq FinSet^{\ast/}$ from [above](#Modules) it follows that the [[algebraic K-theory]] over $\mathbb{F}_1$ is _[[stable cohomotopy]]_:

$$
  \begin{aligned}
    K \mathbb{F}_1
    & \coloneqq\;
    K(\mathbb{F}_1 Mod)
    \\
    & \simeq\;
    K(FinSet)
    \\
    & \simeq
    \mathbb{S}
  \end{aligned}
  \,.
$$ 

Here in the second step we used the definition of algebraic K-theory for ordinary [[commutative rings]] as the [[K-theory of a permutative category|K-theory of the permutative category]] of modules ([this example](K-theory+of+a+permutative+category#examples#OrdinaryAlgebraicKTheoryFromPermutativeCategoryOfProjectiveModules)), in the second step we used the identification of modules over $\mathbb{F}_1$ with [[pointed set|pointed]] [[finite sets]] from [above](#Modules), and finally we used the identification of the [[K-theory of a permutative category|K-theory of the permutative category]] of [[finite set]] with the [[sphere spectrum]] ([this example](K-theory+of+a+permutative+category#StableCohomotopyIsKTheoryOfFinSet)), which is the spectrum representing [[stable cohomotopy]], by definition.

The perspective that the [[K-theory]] $K \mathbb{F}_1$ over $\mathbb{F}_1$ should be [[stable Cohomotopy]] has been highlighted in ([Deitmar 06, p. 2](#Deitmar06), [Guillot 06](#Guillot06), [Mahanta 17](#Mahanta17), [Dundas-Goodwillie-McCarthy 13, II 1.2](#DundasGoodwillieMcCarthy13), [Morava](#MoravaSomeBackground), [Connes-Consani 16](#ConnesConsani16)).). Generalized to [[equivariant stable homotopy theory]], the statement that [[equivariant K-theory]] $ K_G \mathbb{F}_1$ over $\mathbb{F}_1$ should be [[equivariant stable Cohomotopy]] is discussed in [Chu-Lorscheid-Santhanam 10, 5.3](#ChuLorscheidSanthanam10).



[[!include Segal completion -- table]]


## Related concepts

* [[Lambda-ring]], 

* [[blue scheme]]

* [[tropical geometry]].


## References

After the very first observations by Tits, pioneers were [[Christophe Soulé]] and Kapranov and Smirnov. More recently there are extensive works by [[Alain Connes]] and Katia Consani, [[Nikolai Durov]], [[James Borger]] and [[Oliver Lorscheid]]. 

### Expositions 

* {#Cohn04} Henry Cohn, _Projective geometry over $\mathbb{F}_1$ and the Gaussian binomial coefficients_, American Mathematical Monthly 111 (2004), 487-495 ([arXiv:math/0407093](https://arxiv.org/abs/math/0407093))

* [[Lieven Le Bruyn]], _Looking for $F_{un}$_, [blog](http://www.neverendingbooks.org/looking-for-f_un)

* {#Snyder07} [[Noah Snyder]], _[The field with one element](https://sbseminar.wordpress.com/2007/08/14/the-field-with-one-element/)_, 2007

* Javier L&#243;pez Pe&#241;a, [[Oliver Lorscheid]], _Mapping $F_1$-land:An overview of geometries over the field with one element_, [arXiv/0909.0069](http://arxiv.org/abs/0909.0069)

* [[John Baez]], _This Week's Finds 259_ ([html](http://math.ucr.edu/home/baez/week259.html) [blog](http://golem.ph.utexas.edu/category/2007/12/this_weeks_finds_in_mathematic_19.html))


* [[Alain Connes]], _Fun with $\mathbf{F}_1$_, 5 min. [video](http://www.dailymotion.com/video/x6xe0g_article-alain-connes_tech)

* [[Lieven Le Bruyn]], _The field with one element_, seminar notes 2008 ([web](http://win.ua.ac.be/~lebruyn/b2hd-LeBruyn2008d.html))

* {#Lorscheid14} [[Oliver Lorscheid]], _Lectures on $\mathbb{F}_1$_, 2014 ([pdf](http://www.impa.br/~lorschei/Lectures_on_F1.pdf))

* [[Oliver Lorscheid]], _$\mathbb{F}_1$ for everyone_, 2018 ([arXiv:1801.05337](https://arxiv.org/abs/1801.05337))

* [[Tim Hosgood]], _Under $\mathop{Spec}\mathbb{Z}$: a reader's companion_, master thesis, 2016 ([pdf](https://thosgood.com/assets/files/under-spec-z.pdf)).



### Original articles ###

* {#Tits57} [[Jacques Tits]], _Sur les analogues algebriques des groupes semi-simples complexes_. In Colloque d'algebre superieure, tenu a Bruxelles du 19 au 22 decembre 1956, Centre Belge de Recherches Mathematiques, pages 261-289. Etablissements Ceuterick, Louvain, 1957.

* {#Soule04} [[Christophe Soulé]], _Les varietes sur le corps a un element_ Mosc. Math. J., 4(1):217-244, 312, 2004 ([pdf](http://www.ams.org/distribution/mmj/vol4-1-2004/soule.pdf))

* {#Manin95} [[Yuri Manin]], _Lectures on zeta functions and motives (according to Deninger and Kurokawa)_ Asterisque, (228):4, 121-163, 1995. Columbia University Number Theory Seminar ([pdf](http://streams1.nts.jhu.edu/mathematics/ncgdocs/manin-zeta-absmotives.pdf))

* {#ToenVaquie05} [[Bertrand Toen]], [[Michel Vaquie]], _Under Spec Z_ ([arXiv:math/0509684](http://arxiv.org/abs/math/0509684))

Around (0.4.24.2) in 

* {#Durov07} [[Nikolai Durov]], _New Approach to Arakelov Geometry_ ([arXiv:0704.2030](http://arxiv.org/abs/0704.2030))

the algebraic structure of $\mathbb{F}_1$ is regarded as being the [[maybe monad]], hence [[modules]] over $\mathbb{F}_1$ are defined to be [[algebra over a monad|monad-algebras]] over the [[maybe monad]], hence [[pointed sets]].

Other approaches include
 
* [[Alain Connes]], [[Caterina Consani]], [[Matilde Marcolli]], _Fun with $\mathbf{F}_1$_, [arxiv/0806.2401](http://arxiv.org/abs/0806.2401)

* [[Yuri Manin]], _Cyclotomy and analytic geometry over $F_1$_, [arxiv/0809.1564](http://arxiv.org/abs/0809.1564)

* {#ConnesConsani08} [[Alain Connes]], [[Caterina Consani]], _On the notion of geometry over $\F_1$_, [arxiv/0809.2926](http://arxiv.org/abs/0809.2926); 

  _Schemes over $\F_1$ and zeta functions_, [arxiv/0903.2024](http://arxiv.org/abs/0903.2024); _Characteristic one, entropy and the absolute point _, in: Noncommutative Geometry, Arithmetic, and Related Topics, 21st Meeting of the Japan-U.S. Math. Inst., Baltimore 2009, JHUP (2012), pp. 75&#8211;139, [arxiv/0911.3537](http://arxiv.org/abs/0911.3537); 

  _From monoids to hyperstructures: in search of an absolute arithmetic_, [arxiv/1006.4810](http://arxiv.org/abs/1006.4810); 

  _On the arithmetic of the BC-system_, [arxiv/1103.4672](http://arxiv.org/abs/1103.4672); _Projective geometry in characteristic one and the epicyclic category_, [arxiv/1309.0406](http://arxiv.org/abs/1309.0406)

* [[M. Marcolli]], [[Ryan Thorngren]], _Thermodynamical semirings_, [arXiv/1108.2874](https://arxiv.org/abs/1108.2874)

* Bora Yalkinoglu, _On Endomotives, Lambda-rings and Bost-Connes systems_,  With an appendix by Sergey Neshveyev, [arxiv/1105.5022](http://arxiv.org/abs/1105.5022)

The approach in terms of [[Lambda-rings]] due to

* {#Borger09} [[James Borger]], _Lambda-rings and the field with one element_ ([arXiv/0906.3146](http://arxiv.org/abs/0906.3146))

with details in

* {#Borger08} [[James Borger]], _The basic geometry of Witt vectors, I: The affine case_ ([arXiv:0801.1691](http://arxiv.org/abs/0801.1691))

* {#Borger10} [[James Borger]], _The basic geometry of Witt vectors, II: Spaces_ ([arXiv:1006.0092](http://arxiv.org/abs/1006.0092))

More discussion relating to this includes

* {#LeBruyn13} [[Lieven Le Bruyn]], _Absolute geometry and the Habiro topology_ ([arXiv:1304.6532](http://arxiv.org/abs/1304.6532))

### Relation to stable homotopy theory

The interpretation of [[stable cohomotopy]] as [[algebraic K-theory]] over $\mathbb{F}_1$ is amplified in the following articles:

* {#Deitmar06} [[Anton Deitmar]], _Remarks on zeta functions and K-theory over $\mathbb{F}_1$_ ([arXiv:math/0605429](https://arxiv.org/abs/math/0605429))

* {#Guillot06} [[Pierre Guillot]], _Adams operations in cohomotopy_ ([arXiv:0612327](https://arxiv.org/abs/math/0612327))

* {#MoravaSanthanam} [[Jack Morava]], Rekha Santhanam, _Power operations and absolute geometry_, 2012 ([pdf](http://www.lemiller.net/media/slidesconf/AbsolutePower.pdf))

* {#Mahanta17} [[Snigdhayan Mahanta]], _G-theory of $\mathbb{F}_1$-algebras I: the equivariant Nishida problem_, J. Homotopy Relat. Struct. 12 (4), 901-930, 2017 ([arXiv:1110.6001](https://arxiv.org/abs/1110.6001))

* {#Berman18} John D. Berman, p. 92 of _Categorified algebra and equivariant homotopy theory_ ([arXiv:1805.08745](https://arxiv.org/abs/1805.08745))

* {#ChuLorscheidSanthanam10} Chenghao Chu, [[Oliver Lorscheid]], Rekha Santhanam, _Sheaves and K-theory for $\mathbb{F}_1$-schemes_, Advances in Mathematics, Volume 229, Issue 4, 1 March 2012, Pages 2239-2286 ([arxiv:1010.2896](https://arxiv.org/abs/1010.2896))

see also

* {#MoravaSomeBackground} [[Jack Morava]], _Some background on Manin's theorem $K(\mathbb{F}_1) \sim \mathbb{S}$_ ([pdf](http://www.alainconnes.org/docs/Morava.pdf), [[MoravaSomeBackground.pdf:file]])

* {#ConnesConsani16} [[Alain Connes]], [[Caterina Consani]], _Absolute algebra and Segal's Gamma sets_, Journal of Number Theory 162 (2016): 518-551 ([arXiv:1502.05585](https://arxiv.org/abs/1502.05585))






[[!redirects field of one element]]
[[!redirects Fun]]
[[!redirects absolute geometry]]
[[!redirects absolute algebraic geometry]]
[[!redirects absolute ground field]]
[[!redirects F1]]
