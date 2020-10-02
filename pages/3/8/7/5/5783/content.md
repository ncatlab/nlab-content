
> This entry is about [[∞-groupoids]] parameterized over [[superpoints]]. Hence [[discrete ∞-groupoids]] equipped with super-structure. For _smoothly_ supergeometric [[∞-groupoids]], parameterized over [[supermanifolds]], see _[[super smooth ∞-groupoid]]_ and _[[super formal smooth ∞-groupoid]]_.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
#### Supergeometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _super $\infty$-groupoid_ is an [[∞-groupoid]] modeled on [[super points]]. 

The notion subsumes and generalizes that of _bare_ [[super groups]], but not that of _[[super Lie groups]]_, the latter are instead examples of [[smooth super ∞-groupoids]] sitting over the base of super $\infty$-groupoids.

## Definition


+-- {: .num_defn #SuperInfinityGroupoids}
###### Definition

Let $SuperPoints$ be the [[category]] of [[super points]], regarded as a  [[site]] with trivial [[coverage]].  

The [[(∞,1)-sheaf (∞,1)-topos]] over $SuperPoint$

$$
  Super\infty Grpd := Sh_{(\infty,1)}(SuperPoint)
$$

we call the [[(∞,1)-topos]] of **super $\infty$-groupoids**.

=--

## Properties

### Infinitesimal cohesion
 {#InfinitesimalCohesion}

+-- {: .num_prop}
###### Proposition

The [[(∞,1)-topos]] $Super\infty Grpd$, def. \ref{SuperInfinityGroupoids}, is an [[infinitesimal cohesive (∞,1)-topos]] over [[∞Grpd]].

=--

+-- {: .proof}
###### Proof


Being an [[(∞,1)-category of (∞,1)-presheaves]] the constant $\infty$-presheaf [[(∞,1)-functor]] 

$$
  Disc \;\colon\; \infty Grpd \longrightarrow Super \infty Grpd
$$

has a [[left adjoint]] $\Pi$ given by forming [[(∞,1)-colimits]] and a [[right adjoint]] $\Gamma$ given by [[(∞,1)-limits]]. Since  the [[category]] $SuperPoints$ has a [[terminal object]] (the point $\mathbb{R}^{0|0}$) its [[opposite category]] has an [[initial object]] and so $\Gamma$ is just given by evaluation at that object. $\Gamma X \simeq X(\ast)$. 

It follows that $\Gamma\circ Disc \simeq Id$ and hence (by the discussion at [[adjoint (∞,1)-functor]]) that $Disc$ is a [[full and faithful (∞,1)-functor]].

Moreover, evaluation preserves [[(∞,1)-limits]] (since for [[(∞,1)-presheaves]] there are computed objectwise for each object of the [[site]]) and so by the [[adjoint (∞,1)-functor theorem]] there does exist a further [[right adjoint]] $coDisc \colon \infty Grpd \hookrightarrow Super \infty Grpd$. By the [[(∞,1)-Yoneda lemma]] and by [[adjoint (∞,1)-functor|adjointness]] this sends an [[∞-groupoid]] $X$ to the [[(∞,1)-presheaf]] given by

$$
  coDisc(X) 
   \;\colon\;
  \mathbb{R}^{0|q}
  \;\mapsto\;
  Super\infty Grpd(\mathbb{R}^{0|q}, coDisc(X))
  \simeq
  \infty Grpd(\Gamma(\mathbb{R}^{0|q}), X)
  \,.
$$

Now the crucial aspect is that $\Gamma(\mathbb{R}^{0|q}) \simeq \ast$ for all $q \in \mathbb{N}$ since every [[superpoint]] has a unique [[global point]], this being the archetypical property of [[infinitesimally thickened points]]. So it follows that 

$$
  coDisc \simeq Disc
$$

and hence that $\Pi \simeq \Gamma$. Therefore $\Pi$ preserves in particular [[finite products]] so that $Super \infty Grpd$ is [[cohesion|cohesive]], but of course this shows now that it is in fact [[infinitesimal cohesion|infinitesimally cohesive]].

=--

### Relation to smooth super $\infty$-groupoids

Let 

$$
  \begin{aligned}
    SmoothSuper\infty Grpd & := Sh_{(\infty,1)}(CartSp, Super\infty Grpd)
    \simeq
     Sh_{(\infty,1)}(CartSp\times SuperPoint, \infty Grpd)
    \\
    & =:
     Sh_{(\infty,1)}(CartSp\times SuperPoint)
  \end{aligned}
$$

be the [[(∞,1)-sheaf (∞,1)-topos]] of [[smooth super ∞-groupoids]]. This is cohesive over the [[base topos]] $Super \infty Grpd$.

For more on this see at _[[smooth super ∞-groupoid]]_.

### Superalgebra

$Super \infty Grpd$ is naturally a [[ringed topos]], with [[commutative ring]]-object

$$
  \mathbb{K} \in Super \infty Grpd
$$

which as a presheaf $\mathbb{K} : SuperPoint^{op} \simeq GrAlg \to Set \hookrightarrow sSet$ is given by

$$
  \mathbb{K} : Spec \Lambda \mapsto \Lambda_{even}
$$

with ring structure induced over each [[super point]] $\mathbb{R}^{0|q} = Spec \Lambda = Spec \wedge^\bullet \mathbb{R}^q$ from the ring structure of the even part $\Lambda_{even}$ of the [[Grassmann algebra]] $\lambda$.

The [[higher algebra]] over this ring object is what is called [[superalgebra]]. See there for details on this.

For $k$ the ground field and $j(k)$ its embedding as a super vector space into the topos by the map discussed at [superalgebra -- In the topos over superpoints -- K-modules](super+algebra#SuperModulesAsbbKModules) we have

$$
  \mathbb{K} \simeq j(k)
  \,.
$$



### Supergeometry

(...) [[supergeometry]] (...)

## Structures in $Super \infty Grpd$

We discuss the general abstract 
<a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#Structures">structures in a cohesive (∞,1)-topos</a> realized in $Super \infty Grpd$.

### Exponentiated $\infty$-Lie algebras
 {#ExponentiatedLieAlgebras}

We discuss <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#LieAlgebras">Exponentiated ∞-Lie algebras</a> in $Super \infty Grpd$.

+-- {: .num_defn #SuperLInfinityAlgebra}
###### Definition

A **[[super L-∞ algebra]]** is an [[L-∞ algebra]] [[internalization|internal to]] [[super vector space]]s. 

The [[category]] of super $L_\infty$-algebras is

$$
  S L_\infty Alg := (sdgcAlg^+_{sf})^{op} 
$$

the [[opposite category]]  of [[semi-free dga|semi-free]] [[dg-algebra]]s in [[super vector space]]s: [[commutative monoid]]s in the category of [[cochain complex]]es of [[super vector space]]s whose underlying commutative [[graded algebra]] is free on generators in positive degree.

For $\mathfrak{g}$ a super $L_\infty$-algebra we write $CE(\mathfrak{g})$
for the corresponding [[dg-algebra]]: its [[Chevalley-Eilenberg algebra]].

=--

+-- {: .num_defn #Exp}
###### Definition

For $\mathfrak{g}$ a super $L_\infty$-algebra, its [[Lie integration]] is the super $\infty$-groupoid presented by the [[simplicial presheaf]] 

$$
  \exp(\mathfrak{g}) \in [SuperPoint^{op}, sSet]
$$

on superpoints given by the assignment

$$
  \exp(\mathfrak{g}) 
  \;\colon\; 
  (\mathbb{R}^{0|q}, [k]) 
    \mapsto
   Hom_{sdgcAlg_k}\big(
     CE(\mathfrak{g}), 
    \Omega^\bullet_{vert,si}(\mathbb{R}^{0|q} \times \Delta^k)
   \big)
  \,.
$$

Here on the right we have [[vertical differential form]]s with respect to the projection of [[supermanifold]]s $\mathbb{R}^{0|q} \times \Delta^k \to \mathbb{R}^{0|q}$ and with [[sitting instants]] (see [[Lie integration]], [this Def.](Lie+integration#SmoothDifferentialFormsOnSimplicesWithSittingInstants)).

=--


+-- {: .num_lemma #SuperLieIntegrationOverSuperPointIsLieIntegrationOfEvenPartAfterTensoring}
###### Lemma


For $q \in \mathbb{N}$ write $\Lambda_q \coloneqq C^\infty(\mathbb{R}^{0|q})$ for the [[Grassmann algebra]] on $q$-generators, being the global functions on the [[super point]] $\mathbb{R}^{0|q}$. 


Over $\mathbb{R}^{0|q}$ the super Lie integration from def \ref{Exp} is the ordinary [[Lie integration]] of the ordinary [[L-∞ algebra]] $(\mathfrak{g} \otimes_k \Lambda_q)_{even}$

$$
  \exp\left(
    \mathfrak{g}
  \right)\left(\mathbb{R}^{0|q}\right)
    = 
  \exp\left( 
    (\mathfrak{g}\otimes_k \Lambda_q)_{even} 
  \right)
  \,.
$$

=--

+-- {: .proof}
###### Proof

This is the standard [[even rules]] mechanism. Using that the category $sVect$ of finite-dimensional [[super vector spaces]] is a [[compact closed category]], we compute

$$
  \begin{aligned}
    Hom_{sdgcAlg}
    \left(
      CE(\mathfrak{g}), 
      \Omega^\bullet_{vert,si}(\mathbb{R}^{0|q} \times \Delta^n)
    \right)
    & \simeq
    Hom_{sdgcAlg}\left(
      CE(\mathfrak{g}), 
      C^\infty(\mathbb{R}^{0|q}) \otimes \Omega^\bullet( \Delta^n)
    \right)
    \\
    & \simeq 
    Hom_{sdgcAlg}\left(
      CE(\mathfrak{g}), 
      \Lambda_q \otimes \Omega^\bullet( \Delta^n)
    \right)    
    \\
    & \subset
    Hom_{Ch^\bullet(sVect)}\left(
      \mathfrak{g}^*[1], 
      \Lambda_q \otimes \Omega^\bullet( \Delta^n)
    \right)
    \\
    & \simeq
    Hom_{Ch^\bullet(sVect)}\left(
      \mathfrak{g}^*[1]\otimes (\Lambda_q)^*,  
      \Omega^\bullet( \Delta^n)
    \right)
    \\
    & \simeq
    Hom_{Ch^\bullet(sVect)}\left(
      (\mathfrak{g} \otimes \Lambda_q)^*[1],  
      \Omega^\bullet( \Delta^n)
    \right)
    \\
    & \simeq
    Hom_{Ch^\bullet(sVect)}\left(
      (\mathfrak{g} \otimes \Lambda_q)^*[1]_{even},  
      \Omega^\bullet( \Delta^n)
    \right)
    \\
    & \supset
    Hom_{sdgcAlg}\left( 
      CE((\mathfrak{g}\otimes_k \Lambda_q)_{even}),  
      \Omega^\bullet( \Delta^n)
    \right)
  \end{aligned}
  \,.
$$

Here in the third step we used that the underlying dg-algebra of $CE(\mathfrak{g})$ is free to find the space of morphisms of dg-algebras inside that of super-vector spaces (of generators) as indicated. Since the differential on both sides is $\Lambda_q$-linear, the claim follows.

=--

## Related concepts

* [[cohesive (∞,1)-topos]]

  * [[discrete ∞-groupoid]]

  * [[Euclidean-topological ∞-groupoid]]

  * [[smooth ∞-groupoid]]

  * [[synthetic differential ∞-groupoid]]

  * **super ∞-groupoid**

  * [[smooth super ∞-groupoid]]

  * [[synthetic differential super ∞-groupoid]]



## References
 {#References}

The observation that the study of super-structures in mathematics is usefully regarded as taking place over the [[base topos]] on the [[site]] of [[super points]] has been made around 1984 in

* [[Albert Schwarz]], _On the definition of superspace_, Teoret. Mat. Fiz. (1984)  Volume 60,  Number 1, Pages 37&#8211;42, ([russian original pdf](http://www.mathnet.ru/links/b12306f831b8c37d32d5ba8511d60c93/tmf5111.pdf))

* [[Alexander Voronov]], _Maps of supermanifolds_ , Teoret. Mat. Fiz. (1984)  Volume 60,  Number 1, Pages 43&#8211;48

and in 

* V. Molotkov., _Infinite-dimensional $\mathbb{Z}_2^k$-supermanifolds_ , ICTP
preprints, IC/84/183, 1984.

A summary/review is in the appendix of

* Anatoly Konechny and [[Albert Schwarz]], 

  _On $(k \oplus l|q)$-dimensional supermanifolds_ in _Supersymmetry and Quantum Field Theory_ ([[Dmitry Volkov]] memorial volume) Springer-Verlag, 1998, Lecture Notes in Physics, 509 , J. Wess and V. Akulov (editors)([arXiv:hep-th/9706003](http://arxiv.org/abs/hep-th/9706003))

  _Theory of $(k \oplus l|q)$-dimensional supermanifolds_ Sel. math., New ser. 6 (2000) 471-486

* [[Albert Schwarz]], I- Shapiro, _Supergeometry and Arithmetic Geometry_ ([arXiv:hep-th/0605119](http://arxiv.org/abs/hep-th/0605119))

A fairly comprehensive and introductory review is in 

* [[Christoph Sachse]], _A Categorical Formulation of Superalgebra and Supergeometry_ ([arXiv:0802.4067](http://arxiv.org/abs/0802.4067))

The site of formal duals not just to [[Grassmann algebras]] but to all super-[[infinitesimally thickened point]]s is discussed in

* L. Balduzzi, C. Carmeli, R. Fioresi, _The local functors of points of Supermanifolds_ ([arXiv:0908.1872](http://arxiv.org/abs/0908.1872))


Discussion of [[smooth super ∞-groupoids]] as such:

* [[Urs Schreiber]], section 4.5 of: _[[schreiber:differential cohomology in a cohesive topos]]_

* [[Hisham Sati]], [[Urs Schreiber]], Section 3.1.3 of: _[[schreiber:Proper Orbifold Cohomology]]_ ([arXiv:2008.01101](https://arxiv.org/abs/2008.01101))

* [[Urs Schreiber]], _[[schreiber:Introduction to Higher Supergeometry]]_, lecture at _[[Higher Structures in M-Theory 2018]]_, [Durham Symposium](http://www.maths.dur.ac.uk/lms/)

  published in parts as: _Higher Structures in M-Theory_ (with [[Branislav Jurčo]], [[Christian Saemann]], [[Martin Wolf]]), Fortschritte der Physik (2019) ([arXiv:1903.02807](https://arxiv.org/abs/1903.02807), [doi:10.1002/prop.201910001]( https://doi.org/10.1002/prop.201910001))


[[!redirects super ∞-groupoid]]

[[!redirects super infinity-groupoids]]
[[!redirects super ∞-groupoids]]

[[!redirects Super∞Grpd]]

[[!redirects super ∞-group]]
[[!redirects super ∞-groups]]
[[!redirects super infinity-group]]
[[!redirects super infinity-groups]]