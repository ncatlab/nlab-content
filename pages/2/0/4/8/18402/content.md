
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Spheres
+--{: .hide}
[[!include spheres -- contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The _Reeb sphere theorem_ in [[differential topology]] says that: 

If a [[compact topological space|compact]] [[differentiable manifold]] $X$ admits a [[differentiable function]] $X \to \mathbb{R}$ with exactly two [[critical points]] which are non-degenerate, then $X$ is [[homeomorphism|homeomorphic]] to an [[n-sphere]] (with its [[Euclidean space|Euclidean]] [[metric topology]]).

In fact this holds true even if the two critical points happen to be degenerate ([Milnor 64, theorem 1' on p. 166](#Milnor64))

## Proof

Let $x_{min}$ be the critical point at which $f$ attains its [[minimum]] and $f_{max}$ the critical point at which it attains its maximum. 

By the fact that $X$ is a [[differential manifold]] we find an [[closed neighbourhood]] $B \subset X$ of $x_{min}$ which is [[diffeomorphic]] to an [[closed  ball]].

By the assumption that there are no other critical points, $f$ is monotonically increasing along the [[flow lines]] $\gamma$ of $\nabla f$ on $X \setminus \{x_{min}, x_{max}\}$, in that the function $ \nabla_f(d \gamma_t) = \nabla f(\nabla f) =  {\vert \nabla f\vert^2 }$ is strictly positive:

$$
  \vert\nabla f\vert^2 \colon X \setminus \{x_{min}, x_{max}\} \to (0,\infty) \subset \mathbb{R}
  \,.
$$

Hence for $C \subset X$ a [[compact topological space|compact]], the [[extreme value theorem]] implies that this function attains its [[minimum]]. 

This implies that for every $y \in \mathbb{R}$ with $f(x_{min}) \lt y \lt f(x_{max})$ there exists $t \in \mathbb{R}$ such that the [[flow of a vector field|flow]] $\phi_{\nabla f}$ along $\nabla f$ satisfies $\phi_{\nabla f}(x,t) \geq y$ for all $x \in \partial B$. In particular this is the case for $y$ the maximum of $f|_{C}$. This implies that $C$ is contained in the image of $B$ under some flow of $\nabla f$. But this image is, by the nature of the flow, diffeomorphic to a Euclidean ball. 

In conclusion this shows that every compact subspace of $X$ is contained in an open subspace diffeomorphic to a Euclidean ball. With this the claim follows by the [[Brown-Stallings lemma]].


## Applications

Notice that the Reeb sphere theorem does _not_ speak of [[diffeomorphism]] to an [[n-sphere]], just about [[homeomorphism]]. Indeed, the theorem may be used as an ingredient in the construction of [[exotic smooth structures]] on some $n$-spheres. 

## References

Due to:

* [[Georges Reeb]], *Sur les points singuliers d'une forme de Pfaff completement integrable ou d'une fonction numerique*, Comptes Rendus Acad. Sciences Paris **222** (1946) 847-849 $[$[crid:1571417125676878592](https://cir.nii.ac.jp/crid/1571417125676878592)$]$


Review:

* [[John Milnor]], theorem 4.1 in _Morse theory_ ([pdf](http://www.maths.ed.ac.uk/~aar/papers/milnmors.pdf))

* {#Milnor64} [[John Milnor]], _Differential topology_, chapter 6 in T. L. Saaty (ed.) _Lectures On Modern Mathematic II_ 1964 ([web](https://archive.org/details/LecturesOnModernMathematicsIi), [pdf](https://ia801700.us.archive.org/6/items/LecturesOnModernMathematicsIi/Saaty-LecturesOnModernMathematicsIi.pdf)) 

See also 

* Wikipedia, *[Reeb sphere theorem](https://en.wikipedia.org/wiki/Reeb_sphere_theorem)*

