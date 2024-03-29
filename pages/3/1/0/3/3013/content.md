
#Contents#
* table of contents
{:toc}

## Idea

Given a [[monoidal category]] $(\mathbf{M},\otimes,I)$ and a [[comonoid]] $C$ in $\mathbf{M}$ with coaugmentation $\eta:I\to C$, one can define the following pair $Triv \dashv Coinv$ of [[adjoint functor]]s:

$$ Triv: \mathbf{M}\to \mathbf{Comod}_C, \,\,\,\,X\mapsto X\otimes\eta $$

$$Coinv:\mathbf{Comod}_C\to \mathbf{M},\,\,\,\,(M,\rho)\mapsto M^{co C}:=M\Box_C I $$

where $\Box_C$ denotes the [[cotensor product]] bifunctor and $\rho:M\to M\otimes C$ is a right $C$-[[coaction]]. $Triv$ is called the __(co)free__ or __trivial comodule functor__ and $Coinv$ the __functor of coinvariants__.

If $(\mathbf{M},\otimes,I)$ is in fact a [[monoidal model category]], then we can ask whether this pair of functors is a Quillen pair. If so then the the **homotopy coinvariants functor** is the total right derived functor

$$ \mathbb{R}Coinv: Ho(\mathbf{Comod}_C)\to Ho(\mathbf{M}).$$

Given a $C$-[[comodule]] $(M,\rho)$, any representative of $\mathbb{R}Coinv(M,\rho)$ is called a *model* of the homotopy coinvariants of $M$. 

## Related concepts

* [[coinvariant]]

## References

* K. Hess, *Homotopic Hopf-Galois extensions: foundations and examples*, [arxiv/0902.3393](http://arxiv.org/abs/0902.3393)