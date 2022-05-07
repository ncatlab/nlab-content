
#Contents#
* table of contents
{:toc}

## Idea

A rotation of the [[Euclidean plane]] is an [[isometry]] which leaves exactly one point [[fixed point|fixed]] or is the [[identity map]]. This point, if unique, is called the _center of rotation_. 

A rotation of an $n$-dimensional [[Euclidean space]], $n\geq 2$, is an [[isometry]] which either leaves exactly one $(n-2)$-dimensional [[hyperplane]] (e.g. a [[line]] in dimension $3$) fixed or is the identity map. This line or plane is called the _axis of rotation_. 

If we fix a point, this identifies the Euclidean space  as a set with a [[vector space]] $V$ and the [[group]] of all isometries fixing this point is the [[special orthogonal group]] $SO(V)$. 

Moreover, any choice of linear [[coordinates]] induces an  identification of rotations with orthogonal [[matrices]] with [[determinant]] $1$.  Therefore, in a basis, we may identify rotations with operators realizing [[action]] of a [[special orthogonal group]] $SO(n,\mathbb{R})$ on $\mathbb{R}^n$. 

## Properties

Recall that $SO(n,\mathbf{R})$ is a real [[Lie group]] of dimension $\frac{n(n-1)}{2}$, in particular of dimension $3$ for $n=3$. A particular global choice of parameters (giving also smooth coordinates on an open dense subset) in 3 dimensions are the [[Euler angles]]. 

In 2d every nonidentity rotation sends any ray from the center of rotation to another ray from the center of rotation. The pair of the original ray and its image is constituting an ordered pair of rays, hence an oriented angle whose measure and orientation does not depend on a choice of the original ray; the corresponding signed measure is called the (oriented) angle of rotation. The rotation in 2d is determined by its center and the oriented angle of rotation. 
In 2d every nonidentity rotation may be represented as a composition of two reflections around axes which intersect in the center of rotation. Conversely, a composition of two reflections is a rotation iff the intersection of axes of reflection is exactly one point, or the axes are the same (when we obtain the identity). The angle of rotation is the double of the (measure of the) angle between the axes of reflections. Any two reflections with the same center and oriented angle between their axes determine the same rotation in 2d. 

In general, the orthogonal complement to the axis of rotation, passing through a given point on the $(n-2)$-dimensional fixed point axis, is a 2-plane. The restriction of a rotation to this subspace is a rotation of the plane. The measure or the angle of the $n$-dimensional rotation is the measure of the angle of the rotation in such an orthogonal section plane and it does not depend on the choice of the section plane, that is on the point on the axis. A rotation in $n$ dimensions is determined by its $(n-2)$-axis and its oriented angle of rotation. (Orientation should be discussed here.) 

The group of rotations is $SO(3,\mathbf{R})$, below just called $SO(3)$.

__Euler's theorem on rotations__: a composition of rotations of a sphere is a rotation of a sphere. It is trivial that it is an isometry (when viewed as a transformation of the space), the nontrivial part of the theorem is that there is a $(n-2)$-hyperplane fixed by the composition, the statement which itself is also called the Euler's theorem. This is trivial in dimension 2 and nontrivial in dimension 3 proved by Euler and in higher dimension. Each orthogonal transformation in odd dimensional real space has an invariant (1-dimensional) axis, the statement also called the Euler's theorem (this boils down to the statement that the eigenvalues of the orthogonal matrix are on the unit circle).

## Relation to quaternions in 3d and 4d

Consider the vector space $\mathbf{R}^3\subset\mathbf{H}$ of imaginary quaternions. Let $s\in\mathbf{R}^3\backslash\{0\}$. Then $\sigma_{s^\perp}:q\mapsto -s q s^{-1}$ is a reflection with respect to the plane through origin and orthogonal to $q$. If $s\in\mathbf{H}$ is a quaternion the map $\rho'_s:q\mapsto s q s^{-1}$ leaves the space $\mathbf{R}^3$ of imaginary quaternions invariant and the restriction $\rho_s = \rho'_s|_{\mathbf{R}^3}$ is a rotation. Every rotation arises in that way and the map $s\mapsto\rho_s$ factorizes as the quotient map to the space of real rays $\mathbf{H}\to\mathbf{R}P^3$ and a homeomorphism $\mathbf{R}P^3\cong SO(3)$. The composition of rotations corresponds to the multiplication of quaternions. Components $a,b,c,d$ of quaternions involved fixing $s\in\mathbf{H}$ at the unit sphere $S^3\subset\mathbf{H}$ are called __[Euler-Rodrigues parameters](https://en.wikipedia.org/wiki/Euler%E2%80%93Rodrigues_formula)__. There is a redundancy of 1 parameter (plus the matter of 2-element kernel in the map $S^3\to\mathbf{R}P^3$), but this choice has its advantage in numerical modeling as it avoids the special role of the boundaries for the Euler angles. 

There is a similar construction for [[SO(4)]] (e.g. [Berger 87, Thm 8.9.8](#Berger87)). Indeed, there is an epimorphism of Lie groups (see at *[Spin(4) -- exceptional isomorphisms](Spin4#ExceptionalIsomorphisms)*)

$$
  \tau   
  \;\colonb\; 
  S^3\times S^3\to SO(4),\,\,\,\,(s,r)\mapsto \{q\mapsto s q\overline{r}\}
$$
with [[kernel]] $\{(1,1),(-1,-1)\}$. The [[direct product group|direct product]] structure of the [[domain]] can be used to easily exhibit some nontrivial [[subgroups]] in $SO(4)$. 


## Related concepts

* [[finite rotation group]]

* [[rigid body dynamics]], [[Euler angles]]

* [[isometry]], [[translation]], [[reflection]], [[boost]]

## Literature


* {#Berger87} [[Marcel Berger]], *Geometry I*, Springer 1987 ([doi:10.1007/978-3-540-93815-6](https://doi.org/10.1007/978-3-540-93815-6))




* Hui Cheng, K. C. Gupta, _An historical note on finite rotations_, J. Appl. Mech. Mar 1989, 56(1): 139-145 (7 pages) [doi](https://doi.org/10.1115/1.3176034)

[[!redirects rotations]]