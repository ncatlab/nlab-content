
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _submanifold_ is a [[manifold]] inside another manifold.

## Definition

For a homomorphism of [[differentiable manifolds]]

$$
  X \hookrightarrow Y
$$

to qualify as a submanifold inclusion it is usually required to be an [[embedding of differentiable manifolds]], hence

1. an [[embedding of topological spaces]];

1. an [[immersion of differentiable manifolds]].

## Properties

\begin{proposition}\label{ExistenceOfSiceCharts}
**(submanifolds admit slice charts)**
For $X$ a [[smooth manifold]] and
$\iota \colon \Sigma \hookrightarrow X$ the [[embedding of smooth manifolds|embedding]] of a submanifold, then there exists *slice charts*:

For each point $\sigma \in \Sigma$ there is a [[coordinate chart]] $X \supset U \xrightarrow{\phi} \mathbb{R}^n$ of $X$ such that $\sigma \in U \subset M$ and $\phi(\Sigma \cap U)$ is a rectilinear [[hyperplane]] in $\phi(U) \subset \mathbb{R}^n$. 
\end{proposition}

(e.g. [Lee 2012, Thm. 5.8](#Lee12))

## Related concepts

* [[embedding of differentiable manifolds]]

* [[hypersurface]]

## References

Historical discussion for submanifolds of [[Euclidean space]]:

* [[Élie Cartan]] (translated by Vladislav Goldberg from Cartan's lectures at the Sorbonne in 1926–27): Part E of: *Riemannian Geometry in an Orthogonal Frame*, World Scientific (2001) &lbrack;[doi:10.1142/4808](https://doi.org/10.1142/4808), [pdf](https://softbank.iust.ac.ir/MathBooks/c/Cartan%20-%20Riemannian%20Geometry%20in%20an%20Orthogonal%20Frame.pdf)&rbrack;


Textbook account:

* {#Lee12} [[John Lee]], Chapter 5 of: *Introduction to Smooth Manifolds*, Springer (2012) &lbrack;[doi:10.1007/978-1-4419-9982-5](https://doi.org/10.1007/978-1-4419-9982-5), [book webpage](https://sites.math.washington.edu/~lee/Books/ISM/), [pdf](https://math.berkeley.edu/~jchaidez/materials/reu/lee_smooth_manifolds.pdf)&rbrack;

See also

* Wikipedia, _[Submanifold](https://en.wikipedia.org/wiki/Submanifold)_

On ([[isometric immersions|isometric]]) [[submanifolds]] of [[Euclidean space]] via (the [[algebraic geometry]] of) their higher-dimensional [[coframe fields]]:

* {#GriffithsHarris79} [[Phillip Griffiths]], [[Joseph Harris]], *Algebraic geometry and local differential geometry*, Annales scientifiques de l'École Normale Supérieure, Serie 4, Volume 12 no. 3 (1979) 355-452 &lbrack;[numdam:ASENS_1979_4_12_3_355_0](http://www.numdam.org/item/?id=ASENS_1979_4_12_3_355_0)&rbrack;



[[!redirects submanifolds]]

[[!redirects slice chart]]
[[!redirects slice charts]]



