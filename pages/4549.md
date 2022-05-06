
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Given [[connection on a bundle]] $\nabla$ over a [[space]] $X$, its [[parallel transport]] around some loop $\gamma : [0,1] \to X$, $\gamma(0) = \gamma(1) = x_0$ yields an element 

$$
  hol_\nabla(\gamma) \in G
$$ 

in the [[automorphism group]] of the [[fiber]] $P_{x_0}$ of the bundle. This is the **holonomy** of $\nabla$ around $\gamma$.

Fixing a connection $\nabla$ and a point $x \in X$ the collection of all elements $hol_\nabla(\gamma)$ for all loops $\gamma$ based at $x$ forms a subgroup of $G$, called the [[holonomy group]].

If the [[Levi-Civita connection]] on a [[Riemannian manifold]] $(X,g)$ has a holonomy group that is a proper subgroup of the [[special orthogonal group]] one says that $(X,g)$ is a manifold with [[special holonomy]]. (More precise would be: "with special holonomy group for the Levi-Civita connection".)

## Properties

Proposition. If on a smooth principal bundle $P\to X$ there is a connection $\nabla$ whose holonomy group is $G$ then the structure group can be reduced to $G$. 


(...)

+-- {: .un_theorem}
###### Theorem
**(Ambrose-Singer)**
[[Ambrose-Singer theorem]]: the [[Lie algebra]] of the holonomy group of a [[connection on a bundle]] $\nabla$ on $X$ at a point $x \in X$ is spanned by the [[parallel transport]] $Ad_{tra_\nabla(\gamma)}(F_A(v \vee w))$ of the [[curvature]] $F_A$ evaluated on any $v \vee w \in \wedge^2 T_y X$ at $y \in X$ along any path $\gamma$ from $x \to y$.
=--

We may think of $Id + \Ad_{tra_\nabla(\gamma)}(F_A(\phi))$ as being the holonomy around the loop obtained by

1. going along $\gamma$ from $x$ to $y$

1. going around the [[infinitesimal space|infinitesimal]] parallelogram spanned by $v$ and $w$;

1. coming back to $x$ along the reverse path $\gamma$.

## Applications

(...)

## Higher holonomy


The [[higher holonomy]] (see there) of [[circle n-bundles with connection]] is given by [[fiber integration in ordinary differential cohomology]].

## Related concepts

* [[connection on a bundle]], [[connection on a 2-bundle]], [[connection on an infinity-bundle]]

* [[parallel transport]], [[higher parallel transport]]

* **holonomy**

  * [[holonomy group]]

  * [[special holonomy]]

  * [[Wilson loop]]

  * [[nonabelian Stokes theorem]]
  
* [[fiber integration in differential cohomology]]

  * [[fiber integration in ordinary differential cohomology]]

## References

With an eye towards application in [[mathematical physics]]:

* [[Mikio Nakahara]], Section 10.2 of: _[[Geometry, Topology and Physics]]_, IOP 2003 ([doi:10.1201/9781315275826](https://doi.org/10.1201/9781315275826), <a href="http://alpha.sinp.msu.ru/~panov/LibBooks/GRAV/(Graduate_Student_Series_in_Physics)Mikio_Nakahara-Geometry,_Topology_and_Physics,_Second_Edition_(Graduate_Student_Series_in_Physics)-Institute_of_Physics_Publishing(2003).pdf">pdf</a>)



[[!redirects holonomies]]

[[!redirects Ambrose-Singer theorem]]


