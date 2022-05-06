
#Contents#
* table of contents
{:toc}

## Idea

Rotation of a Euclidean plane is an [[isometry]] which leaves exactly one point fixed or is the identity map. This point, if unique, is called the center of rotation. Rotation of an $n$-dimensional [[Euclidean space]], $n\geq 2$, is an isometry which either leaves exactly one $(n-2)$-dimensional plane (line in dimension $3$) fixed or is the identity map. This line or plane is called the axis or rotation. If we fix a point, this identifies the Euclidean space  as a set with a vector space $V$ and the group of all isometries fixing this point is the special orthogonal group $SO(V)$. Any choice of coordinates induces an  identification of rotations with orthogonal matrices with determinant $1$.   Therefore, in a basis, we may identify rotations with operators realizing [[action]] of a [[special orthogonal group]] $SO(n,\mathbf{R})$ on $\mathbf{R}^n$. 

## Properties

Recall that $SO(n,\mathbf{R})$ is a real [[Lie group]] of dimension $\frac{n(n-1)}{2}$, in particular $3$ for $n=3$. A particular global choice of parameters (giving also smooth coordinates on an open dense subset) in 3 dimensions are the [Euler angles](https://en.wikipedia.org/wiki/Euler_angles). A useful choice of parameters in 3d are also 4 [Euler-Rodrigues parameters](https://en.wikipedia.org/wiki/Euler%E2%80%93Rodrigues_formula) $a,b,c,d$ satisfying relation $a^2+b^2+c^2+d^2 = 1$, which parametrize rotation matrices in $SO(3,\mathbf{R})$ (also related, in a model, to components of unit quaternions).

In 2d every nonidentity rotation sends any ray from the center of rotation to another ray from the center of rotation. The pair of the original ray and its image is constituting an ordered pair of rays, hence an oriented angle whose measure and orientation does not depend on a choice of the original ray; the corresponding signed measure is called the (oriented) angle of rotation. The rotation in 2d is determined by its center and the oriented angle of rotation. 
In 2d every nonidentity rotation may be represented as a composition of two reflections around axes which intersect in the center of rotation. Conversely, a composition of two reflections is a rotation iff the intersection of axes of reflection is exactly one point, or the axes are the same (when we obtain the identity). The angle of rotation is the double of the (measure of the) angle between the axes of reflections. Any two reflections with the same center and oriented angle between their axes determine the same rotation in 2d. 

In general, the orthogonal complement to the axis of rotation, passing through a given point on the $(n-2)$-dimensional fixed point axis, is a 2-plane. The restriction of a rotation to this subspace is a rotation of the plane. The measure or the angle of the $n$-dimensional rotation is the measure of the angle of the rotation in such an orthogonal section plane and it does not depend on the choice of the section plane, that is on the point on the axis. A rotation in $n$ dimensions is determined by its $(n-2)$-axis and its oriented angle of rotation. (Orientation should be discussed here.) 


## Related concepts

* [[rigid body dynamics]]

* [[isometry]], [[translation]], [[reflection]], [[boost]]

[[!redirects rotations]]