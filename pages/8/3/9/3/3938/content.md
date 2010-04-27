
_Under Construction - The following material needs the blessing of an expert._

## Idea

Given [[manifold|smooth manifolds]] $\mathcal{M}$ and $\mathcal{N}$, a smooth map $F:\mathcal{M}\to\mathcal{N}$, an $n$-dimensional subdomain $\Sigma\to\mathcal{M}$ and an $n$-form $\alpha\in\Omega^n(\mathcal{N})$, we have the pullback $F^*\alpha\in\Omega^n(\mathcal{M})$ and the pushforward $F_*\Sigma$ that satisfy

$$\int_\Sigma F^*\alpha = \int_{F_*\Sigma} \alpha.$$

_Transgression_ can be thought of as a generalization of this situation. For instance, given a smooth manifold $\mathcal{M}$, let $\mathcal{L M}$ denote the [[loop space]] of $\mathcal{M}$, i.e. the space of loops in $\mathcal{M}$. A loop in $\mathcal{M}$ corresponds to a point in $\mathcal{L M}$.

Now a 0-form $\alpha\in\Omega^0(\mathcal{L M})$ "pulls back" to a 1-form $\mathcal{L}^*\alpha\in\Omega^1(\mathcal{M})$ and a loop $\gamma$ in $\mathcal{M}$ "pushes forward" to a point $\mathcal{L}_*\gamma$ in $\mathcal{L M}$. Once again we have

$$\int_\gamma \mathcal{L}^*\alpha = \int_{\mathcal{L}_*\gamma} \alpha.$$

Now, however, the integral of a 0-form is just evaluation so the integral of a 1-form $\mathcal{L}^*\alpha$ over a loop $\gamma\to\mathcal{M}$ is the evaluation of the 0-form $\mathcal{L}^*\alpha$ at the point $\mathcal{L}_*\gamma\to\mathcal{L M}$, i.e. 

$$\int_\gamma \mathcal{L}^*\alpha = \alpha(\mathcal{L}_*\gamma).$$
