## Local picture

Local picture is explained in 

* [[Landau-Lifschitz]], Mechanics, vol I. of Course of theoretical physics, chapter 23, Canonical transformations

Suppose we choose a Lagrangean submanifold, what gives the splitting between submanifold coordinates $q_i$, $i = 1,\ldots, n$ and the corresponding moment $p_i$ where the Hamiltonian is $H(p,q,t)$ and $p = (p_1,\ldots, p_n)$, $ = (q_1,\ldots, q_n)$. The canonical transformation by definition preserves the equations of motion; let the new coordinates be $Q_j$ and momenta $P_j$ and the new Hamiltonian is $K$. Thus both variations 

$$
\delta \int p d q - H d t = \delta \int P d Q - K d t  = 0
$$

vanish. Here we of course write $p d q := \sum_{i = 1}^n p_i d q_i$. Subtracting the left and right hand side variations we get that the difference must be a (variation of the integral of the) total differential of a function, which can be chosen as a function of some set of old and new coordinates in a consistent way. For example in 1 dimension, we have 4 possibilities of one new and one old generalized coordinate. 

$$
p d q - H d t = P d Q - K d t + d F
$$

$$
d F = p d q - P d Q + (K - H) d t
$$

therefore if $F = F (q,Q, t)$ then $\frac{\partial F}{\partial q} = p$, $\frac{\partial F}{\partial Q} = -P$, $K = \frac{\partial F}{\partial t} + H$, what gives the relation between the old and new coordinates and momenta and the new Hamiltonian $K$, which must be expressed in terms of $P, Q, t$. 

If $F = F(q,P,t)$ then we add $P Q$, use the Leibniz rule $d (P Q) = P d Q + Q d P$ and we see that for the generating function of the "second kind", $\Phi(q,P,t) = F(q,P,t) + Q P$ the total differential

$$
d \Phi = d (F + P Q) = p d q + Q d P + (K - H) d t
$$
and $\frac{\partial \Phi}{\partial q} = p$, $\frac{\partial F}{\partial P} = Q$, $K = \frac{\partial \Phi}{\partial t} + H$. A similar analysis can be done straightfowardly for other possibilities of the choice of arguments.  

## Global picture

An invariant picture of generating functions on symplectic manifolds is in 

* C. Viterbo, _Symplectic topology as the geometry of generating functions_, Math. Ann. __292__ (1992), 685&#8211;710, [MR1157321](http://www.ams.org/mathscinet-getitem?mr=1157321), [doi](http://dx.doi.org/10.1007/BF01444643)

* L. Traynor, _Symplectic homology via generating function_, Geom. Funct. Anal. 4 (1994) 718-748, [MR1302337](http://www.ams.org/mathscinet-getitem?mr=1302337), [doi](http://dx.doi.org/10.1007/BF01896659)

An adaption of generating functions to the setup of symplectic micromorphisms is in

*  Alberto S. Cattaneo, Benoit Dherin, Alan Weinstein, _Symplectic microgeometry II: generating functions_, [arxiv/1103.0672](http://arxiv.org/abs/1103.0672)

[[!redirects generating functions in classical mechanics]]