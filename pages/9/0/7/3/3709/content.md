
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The theory of **meromorphic connections** is a modern viewpoint on a class of [[ordinary differential equation|systems of ODE]]-s on [[complex analytic manifold]]s. 

## Definition

### 1-Dimensional case

Consider the field $\mathcal{K}$ of meromorphic functions in a neighborhood of $0\in \mathbb{C}$ with possible pole at $0$ and a finite dimensional $\mathcal{K}$-module $M$. A **meromorphic** connection at $x=0$ is an operator $\nabla:M\to M$ satisfying

$$
\nabla(fu) = \frac{df}{dx}u + f\nabla(u),\,\,\,\,f\in\mathcal{K}, u\in M
$$

There is a natural tensor product on the category of $\mathcal{K}$-modules with meromorphic connections. Namely $(M,\nabla_M)\otimes (N\nabla_N) = (M\otimes N,\nabla)$ where

$$
\nabla(u\otimes v) = \nabla_M (u)\otimes v + u\otimes\nabla_N(v)
$$

There is also an inner hom, namely $HOM((M,\nabla_M),(P,\nabla_P))$ is $Hom_{\mathcal{K}}(M,P)$ with a meromorphic connection

$$
\nabla(\phi)(u) = \nabla_P (\phi(u)) - \phi(\nabla_M (u)),\,\,\,\,u\in M, \phi:M\to N.
$$

## References

* chapter 5, _Theory of meromorphic connections_, from R. Hotta, K. Takeuchi, T. Tanisaki, _D-modules, perverse sheaves, and representation theory_, Progress in Mathematics __236__, Birkh&#228;user

* C. Sabbah, _Isomonodromic deformations and Frobenius manifolds_, Springer 2007, [doi](http://dx.doi.org/10.1007/978-1-84800-054-4)

* P. Maisonobe, C. Sabbah, _D-modules coh&#233;rents et holonomes_, Hermann, Paris 1993.