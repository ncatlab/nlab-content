[[!redirects Siegel modular forms]]


## Idea

_Siegel modular forms_ are one generalization of [[modular forms]] to functions in more than one complex variable (another such generalization are [[Hilbert modular forms]]). 

Where ordinary modular forms are locally functions on the [[moduli stack of elliptic curves]] over the complex numbers, so Siegel modular forms are locally functions on something like the moduli stack of higher-dimensional complex [[abelian varieties]].

## Definition

Let $\mathcal{H}_{g}$ be the [[Siegel upper half-space]] of degree $g$ and let $\Sp_{2g}(\mathbb{Z})$ the subgroup of elements in the [[symplectic group]] $\Sp_{2g}(\mathbb{R})$ with integral entries. Let $V$ be a finite-dimensional vector space over $\mathbb{C}$ and fix a representation

$$\rho:\GL_{g}(\mathbb{C})\to \GL(V).$$

A _Siegel modular form of weight $\rho$_ is a [[holomorphic function]] $f:\mathcal{H}_{g}\to V$ such that

$$f(\gamma(\tau))=\rho(C\tau+D)f(\tau)$$

for all $\tau=\begin{pmatrix}A & B\\C & D\end{pmatrix}\in\Sp_{2g}(\mathbb{Z})$ and all $\tau\in\mathcal{H}_{g}$. If $g=1$, we additionally require that $f$ is holomorphic at $\infty$. A _classical Siegel modular form of weight $k$_ is the special case when the representation $\rho$ is given by taking $k$-th powers of the determinant. Further specializing to $g=1$, this gives classical (also known as elliptic) [[modular forms]].

## Related concepts

* [[Siegel upper half space]]

## References

Gerard van der Greer, _Siegel Modular Forms_, [arxiv:0605346](https://arxiv.org/abs/math/0605346)
