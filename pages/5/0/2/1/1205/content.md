Given two [[bialgebra]]s $A$ and $B$ in Hopf pairing $\langle, \rangle$ (i.e. making comultiplication on one transposed to multiplication to another and viceversa), one define a left [[Hopf action]] $\triangleright$ of $B$ on $A$ by formulas
$$
b\triangleright a = \sum \langle b, a_{(2)}\rangle a_{(1)}= (\langle,\rangle \otimes \id)(b\otimes \Delta_A(a))
$$
one forms the __Heisenberg double__ corresponding to these data as the crossed product algebra ("smash product") $A\sharp B$ associated to the Hopf action $\triangleright$. 

For example if $A = S(V)$ is the symmetric (Hopf) algebra on a finite-dimensional vector space $V$, and $B$ its algebraic dual $(S(V))^*\cong \hat{S}(V^*)$, considered as its dual topological Hopf algebra, the result is the Weyl algebra of regular differential operators, completed with respect to the filtration corresponding to the degree of differential operator. If $B$ is just the finite dual of $S(V)$ which is a usual Hopf algebra, then there is no completion, of course. 