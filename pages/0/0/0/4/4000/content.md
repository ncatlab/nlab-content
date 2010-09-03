
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A _Chern-Simons 2-gerbe_ is a cocycle in degree 4 [[ordinary differential cohomology]] that is canonically associated to a $G$-[[principal bundle]] with [[connection on a bundle|connection]].

For $G$ a [[Lie group]] and $c : \mathcal{B}G \to K(\mathbb{Z},4)$ a cocycle for a degree 4 [[characteristic class]] in [[integral cohomology]] and $X$ a [[smooth manifold]], [[Chern-Weil theory]] provides a morphism (the refined [[Chern-Weil homomorphism]])

$$
  \hat c : G Bund_\nabla(X) \to H_{diff}^4(X)
$$

from $G$-[[principal bundle]]s with [[connection on a bundle|connection]] $\nabla$ to degree 4 [[ordinary differential cohomology]]. The cocycles on the right may be thought of as

* [[circle n-bundle with connection|circle 3-bundles with connection]] $\hat c(\nabla)$;

* [[bundle gerbe|bundle 2-gerbe]]s with connection.

By construction, the [[curvature]] 4-form of $\hat c(\nabla)$ is the [[curvature characteristic form]] $\langle F_\nabla \wedge F_\nabla\rangle$ of $\nabla$ and accordingly the 3-form connection on $\hat c(\nabla)$ is locally a [[Chern-Simons form]] $CS(\nabla)$ of $\nabla$.

Accordingly, the [[parallel transport]] induced by $\hat c(\nabla)$ over 3-dimensional manifolds $\phi : \Sigma \to X$ is the [[action functional]] of the [[quantum field theory]] called [[Chern-Simons theory]]. In this form it appears for instance as the [[gauge field]] called the [[supergravity C-field]] in certain [[supergravity]] theories. In particular, if (with due care) one takes $\nabla$ to be the _universal connection on the $G$-[[universal principal bundle]]_ over a smooth version of $B G$, then $\hat c(\nabla)$ is the background [[gauge field]] for bare [[Chern-Simons theory]].

Therefore this structure $\hat c(\nabla)$ has become known as the **Chern-Simons 2-gerbe**  of $\nabla$. We may also think of it as the _Chern-Simons [[circle n-bundle with connection|circle 3-bundle]]_ .

At least for simply connected $G$ one may enhance the assignment $\nabla \mapsto \hat c(\nabla)$ to a morphism of [[∞-groupoid]]s

$$
  \hat \mathbf{c} : \mathbf{H}_conn(X,\mathbf{B}G)
  \to \mathbf{H}_{diff}(X,\mathbf{B}^3 U(1))
  \,,
$$

where on the left we have the [[groupoid]] of smooth $G$-principal bundles with connection on $X$, and on the right the 3-groupoid of circle 3-bundles with connection. The [[homotopy fiber]]s of this morphism over a trivial circle 3-bundle with connection are 3-groupoids whose objects are naturally identified with pairs consisting of a connection $\nabla$ on a $G$-bundle and a _trivialization_ of its corresponding Chern-Simons 3-bundle. This in particular implies a trivialization of the underlying cocycle in degree 4 [[integral cohomology]] and therefore defines a [[string structure]]. One calls these homotopy fibers therefore [[differential string structure]]s.


## Constructions

### In Cech-Deligne cohomology

Assume that $G$ is a [[simply connected]] [[Lie group]].

In ([Brylinski-McLaughlin I](#GeomConstructionFirst)) is spelled out an explicit constructin of $\hat c(\nabla)$ for given $\nabla$ in [[Cech cohomology|Cech]]-[[Deligne cohomology]]. This is a special case of the general construction presented in ([Brylinski-McLaughlin II](#CechCocyclesForCharClasses)).

In this section here we review this exlicit cocycle construction. In the [next section](#InInfChernWeil) we discuss a systematic way to "derive" this construction.

(...)


### In $\infty$-Chern-Weil theory {#InInfChernWeil}

(...)

### As a bundle 2-gerbe

See ([CJMS](#CJMS), [Waldorf CS](#WaldorfCS)) (...)

## References

### Cech-Deligne cohomology

As cocycles in [[Cech cohomology|Cech]]-[[Deligne cohomology]] the Chern-Simons 2-gerbe has been constructed explicitly in 

* [[Jean-Luc Brylinski]] and Dennis McLaughlin, _A geometric construction of the first Pontryagin class_ (1993) ([pdf](http://www.math.uni-hamburg.de/home/schreiber/Brylinski-McLaughlin-I.pdf))
{#GeomConstructionFirst}

as a special case of the general construction in 

* [[Jean-Luc Brylinski]] and Dennis McLaughlin, _Cech cocycles for characteristic classes_ ,  Communications in Mathematical Phiysics, Volume 178, Number 1, ([Springer](http://www.springerlink.com/content/762g1m76jp6425x5/))
{#CechCocyclesForCharClasses}

### The 2-gerbe realization {#2GerbeReferences}

Conceived as a genuine [[gerbe]] the Chern-Simons 2-gerbe appears in


* [[Jean-Luc Brylinski]] and Dennis McLaughlin, _The geometry of degree-4 characteristic classes and of line bundles on loop spaces II_ ([pdf](http://www.math.uni-hamburg.de/home/schreiber/Brylinski-McLaughlin-Duke-II.pdf)).

Among the first references to apply specifically [[bundle gerbe]] technology to this construction is 

* [[Alan Carey]] and [[Stuart Johnson]] and [[Michael Murray]] and [[Danny Stevenson]] and [[Bai-Ling Wang]], _Bundle gerbes for Chern-Simons and Wess-Zumino-Witten theories_ Communications in Mathematical Physics, 259 (3). (2005) ([arXiv]())
{#CJMS}

This was later refined in 

* [[Konrad Waldorf]], _Multiplicative Bundle Gerbes with Connection_ ([arXiv:0804.4835](http://arxiv.org/abs/0804.4835))

Here are some slides from talks:

* [[Konrad Waldorf]], _Multiplicative gerbes and Chern-Simons theory_ ([pdf](http://www.konradwaldorf.de/docs/bonn.pdf))
{#WaldorfCS}

* [[Krzysztof Gawedzki]], _Wess-Zumino-Witten and Chern-Simons theories for non-simply connected Lie groups_ ([pdf](http://dftuz.unizar.es/ftzar/activities/highenergy09_talks/gawedzki.pdf))

[[!redirects Chern-Simons 2-gerbes]]