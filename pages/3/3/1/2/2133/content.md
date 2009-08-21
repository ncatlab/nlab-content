Given a finite-dimensional $k$-Lie algebra $L$ the __Killing form__ $B:L\otimes L\to K$ is the symmetric billinear form given by the formula

$$
B(x,y)  = tr(ad(x)ad(y))
$$

where $ad(x) = [x,-]:L\to L$ is the ad-operator giving an adjoint representation $ad: L\to Der(L)$. 
Killing form is _)invariant__ in the sense that $B([x,y],z)=B(x,[y,z])$. For complex Lie algebras, the nondegeneracy of Killing form is equivalent to the simisimplicity. For simple complex Lie algebras, any invariant nondegenerate symmetric bilinear form is proportional to the Killing form. 

Sometimes one considers more generally a Killing form $B_\rho$ for a more general faithful finite-dimensional representation $\rho$, $B_\rho(x,y)  = tr(\rho(x)\rho(y))$. If the Killing form is nondegenerate and $x_1,\ldots,x_n$ is a basis in $L$ and $x_1^*,\ldots,x_n^*$ the dual basis of $L^*$, with respect to the Killing form for $\rho$, then the canonical element $r = \sum_i x_i\otimes x_i^*$ defines the __Casimir operator__ $C(\rho) =(\rho\otimes\rho)(r)$ in the representation $\rho$; regarding that the representation is faithful, if the ground field is $\mathbb{C}$, by Schur's lemma $C(\rho)$ is a nonzero scalar operator. Instead of Casimir operators in particular faithful representations it is often useful to consider an analogous construction within the universal enveloping algebra, the __Casimir element__ in U(L).