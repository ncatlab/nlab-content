#Definition#

Given a commutative unital ring $k$, and a (strict for simplicity) symmetric monoidal $k$-linear category $(C,\otimes,1)$ with the symmetry $\tau$ a **Lie algebra** in $(C,\otimes,1,\tau)$ is an object $L$ in $C$ together with a morphism $[,]: A\otimes A\to A$ such that the Jacobi identity 

$$[,[,]]+[,[,]]\circ(id_L\otimes\tau_{L,L})\circ(\tau\otimes id_L)+[,[,]]\circ (\tau_{L,L}\otimes id_L)\circ (id_L\otimes\tau_{L,L}) = 0$$ 

and antisymmetry 

$$[,]+[,]\otimes\tau_{L,L} = 0$$

hold. If $k=\mathbb{Z}$ then we say (internal) __Lie ring__, and if $k$ is a field and $C=Vec$ about __Lie $k$-algebra__. Other interesting cases are super-Lie algebras, which are the Lie algebras in the symmetric monoidal category $\mathbb{Z}_2-Vec$ of [[supervector space]]s and the Lie algebras in the [[Loday-Pirashvili tensor category]] of linear maps. 

Alternatively, Lie algebras are the algebras over certain quadratic operad, called the Lie algebra [[operad]]. The Koszul dual of this operad is the commutative algebra operad.  

A Lie algebra is a special case of an [[L-infinity algebra]] with generators only in lowest degree.

For the classically phrased definitions over a field see 
[Wikipedia: Lie algebra](http://en.wikipedia.org/wiki/Lie_algebra)


[[!redirects Lie algebras]]