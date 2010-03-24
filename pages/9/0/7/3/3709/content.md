
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The theory of **meromorphic connections** is a modern viewpoint on local behaviour of a class of [[ordinary differential equation|systems of ODE]]-s with meromorphic coefficients in a complex domain. 

## Definition

### 1-Dimensional case

Consider the field $\mathcal{K}$ of meromorphic functions in a neighborhood of $0\in \mathbb{C}$ with possible pole at $0$ and a finite dimensional $\mathcal{K}$-module $M$. A **meromorphic** connection at $x=0$ is a $\mathbb{C}$-linear operator $\nabla:M\to M$ satisfying

$$
\nabla(fu) = \frac{df}{dx}u + f\nabla(u),\,\,\,\,f\in\mathcal{K}, u\in M
$$

In fact, it is customary, in modern literature to consider just a germ: the connections on two different neighborhoods agreeing on the intersection are identified. This way $\mathcal{K}$ is isomorphic to the field of formal Laurant power series $\mathbb{C}[ [u] ][u^{-1}]$.

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

* L.Katzarkov, [[Maxim Kontsevich|M.Kontsevich]], T.Pantev, _Hodge theoretic aspects of mirror symmetry_, [arxiv/0806.0107](http://arxiv.org/abs/0806.0107)

* D. Babbitt, V.S. Varadarajan, _Deformations of nilpotent matrices over rings and reduction of analytic families of meromorphic differential equations_, Mem. Amer. Math. Soc. __55__ (325), iv+147, 1985.

* V.S. Varadarajan, _Linear meromorphic differential equation: a modern point of view_, Bull. AMS __33__, n. 1, 1996, [pdf](http://www.ams.org/bull/1996-33-01/S0273-0979-96-00624-6/S0273-0979-96-00624-6.pdf), [citeseer:pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.104.8107&rep=rep1&type=pdf).

* [[Pierre Deligne]], _&#201;quations diff&#233;rentielles &#224; points singuliers r&#233;guliers_, Lect. Notes in Math. __163__, Springer-Verlag (1970)