
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

A _super $\infty$-groupoid_ is an [[∞-groupoid]] modeled on [[super point]]s. The notion subsumes and generalizes that of _bare_ [[super group]]s, not thought that of [[super Lie group]]s, these are instead examples of [[smooth super ∞-groupoid]]s.

## Definition

Fix a ground [[field]] $k$. Write $anAlg_k$ for the [[category]] whose objects are $\mathbb{Z}_2$-[[graded algebra]]s of the form $k \oplus N$ with $N$ nilponent and whose morphisms are $k$-algebra homomorphisms. Write 

$$
  SuperPoint := anAlg_k^{op}
$$

for its [[opposite category]]. Regard this as a [[site]] with trivial [[coverage]].  

We say that the [[(∞,1)-sheaf (∞,1)-topos]] over $SuperPoint$

$$
  Super\infty Grpd := Sh_{(\infty,1)}(SuperPoint)
$$

is the [[(∞,1)-topos]] of **super $\infty$-groupoids**.

## Properties

$Super\infty Grpd$ is a [[cohesive (∞,1)-topos]].

## References

The proposal that the study of super-structures in mathematics should be regarded as taking place over the [[topos]] on the [[site]] of [[super point]]s has been made by [[Albert Schwarz]] in 

* [[Albert Schwarz]], _On the definition of superspace_ Teoret. Mat. Fiz., 1984,  Volume 60,  Number 1, Pages 37&#8211;42   (Mi tmf5111), ([russian original](http://www.mathnet.ru/links/b12306f831b8c37d32d5ba8511d60c93/tmf5111.pdf))

A survey of elements of this approach with an eye towards the notion of [[super manifold]]s is in 

* Anatoly Konechny and [[Albert Schwarz]], 

  _On $(k \oplus l|q)$-dimensional supermanifolds_ in _Supersymmetry and Quantum Field Theory_ (D. Volkov memorial volume) Springer-Verlag, 1998 ,
Lecture Notes in Physics, 509 , J. Wess and V. Akulov (editors)([arXiv:hep-th/9706003](http://arxiv.org/abs/hep-th/9706003))

  _Theory of $(k \oplus l|q)$-dimensional supermanifolds_ Sel. math., New ser. 6 (2000) 471 { 486

See also

* [[Albert Schwarz]], I- Shapiro, _Supergeometry and Arithmetic Geometry_ ([arXiv:hep-th/0605119](http://arxiv.org/abs/hep-th/0605119))


[[!redirects super ∞-groupoid]]
