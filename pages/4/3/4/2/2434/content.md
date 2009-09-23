<div class="rightHandSide toc">

[[!include functorial quantum field theory - contents]]

***

[[!include supergeometry - contents]]


</div>


+-- {: .standout}

This is a sub-entry of [[geometric models for elliptic cohomology]] and [[A Survey of Elliptic Cohomology]] 

See there for background and context.

This entry here is about the definition of $(2|1)$-dimensional [[super-cobordism]] categories and $(2|1)$-dimensional [[FQFT]]s given by functors on these.

=--

Let [[SDiff]] be the [[category]] of [[supermanifold]]s.

We will define a [[stack]]/[[fibered category]] on $SDiff$ called $E Bord_{2|1}$ whose morphisms are smooth families of (2|1)-dimensional [[super-cobordism]]s, and a [[stack]]/[[fibered category]] $sTV^{fam}$ of topological super vector bundles.

So recall

* [[supergeometry - contents|supergeometry]].

**question**: What is the right notion of Riemannian or Euclidean structure on [[super-cobordism]]s?

**strategy**: From the [[path integral]] perspective we need some structure on $\Sigma$ such that the "space" of maps $Maps(\Sigma,X)$ naturally carries some measure that allows to perform a [[path integral]].

This perspective suggests certain genralizations of the notion of [[Riemannian manifold]] to [[supermanifold]]s which may be a little different than what one might have thought of naively.

We want to define [[Euclidean supermanifold]]s as a genralization of [[Riemannian manifold]] with _flat_ Riemannian metric.

notice that there is a canonical bijection between

* flat [[Riemannian metric]]s on a $d$-dimensional [[manifold]] $X$

* a maximal [[atlas]] on $X$ consisting of charts such that all transition functions belong the the **Euclidean group** or **Galileo group** 

  $$
    Eucl(\mathbb{R}^d)
    :=
    \mathbb{R}^d \rtimes O(\mathbb{R}^d)
  $$

  (rigid translations and rotations)

In analogy to that we define:

Similarly a **Euclidean structure** on a $(d|\delta)$-dimensional [[supermanifold]] is defined using the Euclidean [[super Lie group]] given by the [[semidirect product]]

$$
  Eucl(\mathbb{R}^{d|\delta})
  :=
  \mathbb{R}^{d|\delta}
  \rtimes
  Spin(\mathbb{R}^d)
$$

where the [[Spin]] group acts on the translations in $\mathbb{R}^{d|\delta}$ in a way to be specified.


first recall the notion of

* [[complex supermanifold]]

**goal** replace the standard Euclidean group $(\mathbb{R}^d, Eucl(\mathbb{R}^d))$ by the [[super Euclidean group]]
$(X,G)$ where $X$ is a suitable [[supermanifold]]
and $G$ a suitable [[super Lie group]].

This leads to the notion of

* [[Euclidean supermanifold]].

The morphisms of the category $E Bord_{(2|1)}$ will be [[cobordism]]s that are [[Euclidean supermanifold]]s.