Poisson manifolds are a mathematical setup for [[classical mechanics]] with finitely many degrees of freedom. 

A __[[Poisson algebra]]__ is a commutative unital [[associative algebra]] $A$, in this case over the field of [[real number|real]] or [[complex numbers]], equipped with a Lie bracket $\{,\}:A\otimes A\to A$ such that, for any $f\in A$, $\{ f,-\}:A\to A$ is a [[derivation]] of $A$ as an associative algebra.

A __Poisson manifold__ is a real smooth [[manifold]] $M$ together with a Lie algebra bracket $\{,\}:C^\infty(M)\times C^\infty(M)\to C^\infty(M)$ on the vector space of smooth functions on $M$ which together with the pointwise multiplication of functions makes it a Poisson algebra. As derivations of $C^\infty(M)$ correspond to smooth [[tangent vector fields]], for each $f\in C^\infty(M)$ there is a vector $X_f$ given by $X_f(g)=\{f,g\}$ and called the __Hamiltonian vector field__ corresponding to the function $f$, which is viewed as a classical hamiltonian function.  

Alternatively a Poisson structure on a manifold is given by a choice of smooth antisymmetric bivector called a __Poisson bivector__ $P\in\Lambda^2 T M$; then $\{f,g\}:=\langle df\otimes dg, P\rangle$. 

Every [[symplectic manifold]] carries a natural Poisson structure; however, such Poisson manifolds are very special. It is a basic theorem that Poisson structures on a manifold are equivalent to the smooth [[foliation]]s of the underlying manifold such that each leaf is a symplectic manifold.

The dual to a finite-dimensional [[Lie algebra]] has a natural structure of a Poisson manifold due to Kirillov. Its leaves are called [[coadjoint orbit]]s. 

A morphism $h:M\to N$ of Poisson manifolds is a morphism of smooth manifolds such that, for all $f,g\in C^\infty(N)$, $\{f\circ h, g\circ h\}_M = \{f,g\}_N$. 


[[!redirects Poisson manifolds]]
[[!redirects Poisson bivector]]