## Idea ##

A symmetric space is a specially nice [[homogeneous space]], characterized by the property that for each point there is a symmetry fixing that point and acting as $-1$ on its tangent space.  An example would be the sphere, the Euclidean plane, or the hyperbolic plane.

## Definitions ##

A **symmetric space** is classically defined to be a manifold of the form $G/H$, where $G$ is a [[Lie group]] and the subgroup $H$ is the set of fixed points of some [[involution]] $\sigma : G \to G$, that is, a smooth homomorphism with $\sigma^2 = 1_G$.   Using the involution, every point $a \in G/H$ gives rise to a smooth map

$$   a \triangleright -  : G/H \to G/H $$

fixing the point $a$ and acting as $-1$ on the tangent space of $a$.  This operations satisfies the laws of an involutory [[quandle]].

More precisely, a **symmetric pair** is a pair $(G,H)$ where $G$ is a [[Lie group]] and the subgroup $H$ is the set of fixed points of some [[involution]] $\sigma : G \to G$.  Different pairs $(G,H)$, $(G',H')$ can give what is normally considered the same symmetric space $G/H \cong G'/H'$.   In other words, not every morphism of symmetric spaces arises from a morphism of symmetric pairs.

To avoid this problem, we may define a symmetric space more intrinsically to be an involutory [[quandle]] object $Q$ in the category of smooth manifolds, with the property that each point $a \in Q$ is an _isolated_ fixed point of the map $a \triangleright - : Q \to Q$.  

This definition in terms of quandles coincides with the classical definition in the case of connected symmetric spaces.  For details, including a comparison of other definitions of symmetric space, see:

* Wolgang Bertram, _The Geometry of Jordan and Lie Structures_, Lecture Notes in Mathematics **1754**, Springer, Berlin, 2000.

The relation to quandles is given in Theorem I.4.3.  Bertram attributes this result to:

* Ottmar Loos, _Symmetric Spaces I_, Chapter II, Benjamin, New York, 1969.

See also 

* Ottmar Loos, _Symmetric Spaces II_, Benjamin, New York, 1969.