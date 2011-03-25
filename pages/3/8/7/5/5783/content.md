
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

A _super $\infty$-groupoid_ is an [[∞-groupoid]] modeled on [[super point]]s. 

The notion subsumes and generalizes that of _bare_ [[super group]]s, not thought that of [[super Lie group]]s. The latter are instead examples of [[smooth super ∞-groupoid]]s sitting over the base of super $\infty$-groupoids.

## Definition

Consider the category $SuperPoint$ of [[super point]]s as a  [[site]] with trivial [[coverage]].  

We say that the [[(∞,1)-sheaf (∞,1)-topos]] over $SuperPoint$

$$
  Super\infty Grpd := Sh_{(\infty,1)}(SuperPoint)
$$

is the [[(∞,1)-topos]] of **super $\infty$-groupoids**.

## Properties

### Cohesion

$Super\infty Grpd$ is a [[cohesive (∞,1)-topos]].

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

be the [[(∞,1)-sheaf (∞,1)-topos]] of [[smooth super ∞-groupoid]]s. This is cohesive over the [[base topos]] $Super \infty Grpd$.

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

### Supergeometry

(...) [[supergeometry]] (...)

## References
 {#References}

The proposal that the study of super-structures in mathematics should be regarded as taking place over the [[base topos]] on the [[site]] of [[super point]]s has been made around 1984 in

* [[Albert Schwarz]], _On the definition of superspace_ Teoret. Mat. Fiz., 1984,  Volume 60,  Number 1, Pages 37&#8211;42   (Mi tmf5111), ([russian original](http://www.mathnet.ru/links/b12306f831b8c37d32d5ba8511d60c93/tmf5111.pdf))

and in 

* V. Molotkov., _Infinite-dimensional $\mathbb{Z}_2^k$-supermanifolds_ , ICTP
preprints, IC/84/183, 1984.

and in

* [[Alexander Voronov]], _Maps of supermanifolds_ , Teoret. Mat.
Fiz., 60(1):43&#8211;48, 1984.

See also

* Anatoly Konechny and [[Albert Schwarz]], 

  _On $(k \oplus l|q)$-dimensional supermanifolds_ in _Supersymmetry and Quantum Field Theory_ (D. Volkov memorial volume) Springer-Verlag, 1998 ,
Lecture Notes in Physics, 509 , J. Wess and V. Akulov (editors)([arXiv:hep-th/9706003](http://arxiv.org/abs/hep-th/9706003))

  _Theory of $(k \oplus l|q)$-dimensional supermanifolds_ Sel. math., New ser. 6 (2000) 471 { 486

* [[Albert Schwarz]], I- Shapiro, _Supergeometry and Arithmetic Geometry_ ([arXiv:hep-th/0605119](http://arxiv.org/abs/hep-th/0605119))

A comprehensive discussion of the situation over the site of superpoints is given in 

* [[Christoph Sachse]], _A Categorical Formulation of Superalgebra and Supergeometry_ ([arXiv:0802.4067](http://arxiv.org/abs/0802.4067))

The site of formal duals not just to [[Grassmann algebra]]s but to all super-[[infinitesimally thickened point]]s is discussed in

* L. Balduzzi, C. Carmeli, R. Fioresi, _The local functors of points of Supermanifolds_ ([arXiv:0908.1872](http://arxiv.org/abs/0908.1872))


[[!redirects super ∞-groupoid]]

[[!redirects Super∞Grpd]]