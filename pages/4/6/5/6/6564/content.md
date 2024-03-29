
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

In the [[mechanics]] of [[rigid body dynamics]] in [[Cartesian space]] $\mathbb{R}^n$, the _moment of inertia_ of a [[rigid body]] is the analog of [[mass]] for [[rotational dynamics]].  In [[linear dynamics]], we have the formula
$$ p = m v $$
which says that the [[momentum]] $p$ is proportional to the [[velocity]] $v$.  Similarly, in rotational dynamics, we have the analogous formula
$$ L = I \Omega $$
where $L$ is the [[angular momentum]], $\Omega$ is the [[angular velocity]], and $I$ is the __moment of inertia__.

However, the rotational equation is somewhat more complicated than the linear one: firstly because $L$ and $\Omega$ are not naturally vectors but [[bivectors]]; and secondly because they are not necessarily proportional, so that $I$ cannot be a [[scalar]].  In general, the moment of inertia is a [[linear function]]
$$
  I \colon \wedge^2 \mathbb{R}^n \to \wedge^2 \mathbb{R}^n
$$
so that the above equation becomes simply
$$ L = I(\Omega). $$
This linear function is additionally *symmetric* with respect to the induced [[inner product]] on $\bigwedge^2 \mathbb{R}^n$, so it can be represented in coordinates by a symmetric $\frac{n(n-1)}{2} \times \frac{n(n-1)}{2}$ [[matrix]].

Similarly, differentiating this equation once with respect to [[time]] (and assuming that $I$ is constant as it is for a rigid body), we have
$$ \tau = I \alpha ,$$
relating the total [[torque]] $\tau$ to the [[angular acceleration]] $\alpha$ --- this is the rotational analogue of [[Newton's second law]] $F = m a$ (where $m$ must be constant).


## In low dimensions

In low dimensions, the situation can be (and usually is) simplified.

* In two [[dimensions]], [[bivectors]] form a one-dimensional [[vector space]], so that the moment of inertia is simply a scalar.

* In three dimensions, bivectors form a three-dimensional [[vector space]], so that the moment of inertia can be represented by a symmetric $3 \times 3$ matrix.  Additionally, in three dimensions, there is an [[isomorphism]] between [[bivectors]] and [[vectors]] (once we choose an [[orientation]] to go with our inner product); so that [[angular velocity]] and [[momentum]] can be (and usually are) identified with [[vectors]], and the moment of inertia with a symmetric rank-2 [[tensor]].


## In Hamiltonian dynamics

In terms of the discussion at [[Hamiltonian dynamics on Lie groups]], the [[rigid body dynamics]] in $\mathbb{R}^n$ is given by Hamiltonian motion on the [[special orthogonal group]] $SO(n)$. It is defined by any [[left invariant]] [[Riemannian metric]]

$$
  \langle -,-\rangle \in Sym^2_{C^\infty(G)} \Gamma(T G) 
$$

hence a bilinear non-degenarate form on the [[Lie algebra]] $\mathfrak{so}(n)$ (not necessarily the [[Killing form]]).

This bilinear form is the __moment of inertia__. (For instance [AbrahamMarsden, section 4.6](#AbrahamMarsden).)


## In terms of mass density

If a [[rigid body]] has [[mass density]] $\rho$, then its angular momentum is defined in terms of $\Omega$ by the $n$-dimensional integral
$$ L = \int \rho \vec{x} \wedge (\vec{x} \cdot \Omega) \,d^n x $$
over all space, where $\vec{x}$ is the vector from the origin to the point of integration, $\cdot$ denotes the [[interior product]] of a vector with a bivector (yielding a vector), and $\wedge$ denotes the [[exterior product]] of two vectors (yielding a bivector).

When $\Omega$ is the same everywhere (as for a rigid body), then we may view this as a function from $\Omega$ to $L$; this function is the __moment of inertia__.


## Related pages

* [[Hamiltonian dynamics on Lie groups]]

  * [[rigid body dynamics]]

    * [[angular velocity]]

    * [[angular momentum]]


## References

A classical textbook discussion is for instance section 4.6 of

* [[Ralph Abraham]], [[Jerrold Marsden]], _[[Foundations of Mechanics]]_ 
 {#AbrahamMarsden}

A pedestrian discussion of _moment of inertia_ in terms of [[bivector]]s that applies in any [[dimension]] of [[space]]([[spacetime]]) is around page 74 of 

* Chris Doran, Anthony Lasenby, _Geometric Algebra for Physicists_ Cambridge University Press

or around page 56 of 

* Chris Doran, Anthony Lasenby, _Physical applications of geometric algebra_ ([pdf](https://dspace.ist.utl.pt/bitstream/2295/52599/1/Lectures_on_Geometric_Algebra.pdf#page=56))

and around slide 6 in 

* Anthony Lasenby, Chris Doran and Robert Lasenby, _Rigid Body Dynamics and Conformal Geometric Algebra_ ([pdf](http://staff.science.uva.nl/~leo/agacse2010/talks_world/Lasenby.pdf))

These authors amplify the canonical embedding of bivectors into the [[Clifford algebra]], which they call "[[Geometric Algebra]]".
