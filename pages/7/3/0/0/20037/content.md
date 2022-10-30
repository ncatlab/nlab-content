\tableofcontents

\section{Idea}

Rough Paths are a way of defining [[Stieltjes integral|Riemann-Stieltjes type integrals]] for paths with poor $p$-variation where Ito techniques don't work in the context of solving controlled [[differential equations]].

\section{Set-Up}

We want to solve differential equations of the form:

$$
y_t=y_0+\int_0^t V(y_s)\otimes dX_s
$$

where $V=(V_1,...,V_d)$ with $V_i\in C_b^\infty(\mathbb{R}^d,\mathbb{R}^d)$ smooth bounded vector fields and $X\in C^p([0,T],\mathbb{R}^d)=\{f\colon \|f\|_{p-var}\colon = (\sup_{\mathcal{P}} |f_t-f_s|^p)^{1/p}\lt \infty\}$ is a signal with finite $p$ variation. 

We want to solve this by a fixed point argument/Picard iteration. That means we must define:

$$
\int_0^t f(X_s)\otimes dX_s
$$ 

for smooth bounded $f$. 

The classical paper ([Young 1936](#Young36)) says, in short, that one can define this integral as a Riemann-Stieltjes integral iff $p\lt 2$.

A theorem by Bichdeller-Dellecherie says, in short, that one can define this [[Itô integral|integral in Itô sense]] if and only if $X$ is a [[semimartingale]].

\section{Main Result}

If one can define $X^1_{st}\colon = \int_s^t dX_{r_1}$, $X^2_{st}\colon =\int_s^t\int_s^{r_2} dX_{r_1}\otimes dX_{r_2}$,..., $X^\ell_{st}\colon =\int_s^t \int_s^{r_\ell}...\int_s^{r_2} dX_{r_1}\otimes...\otimes dX_{r_\ell}$ where $\ell=\lfloor p \rfloor$ then the following "corrected Riemann sum" converges:

$$\sum_{k=0}^{n} f(X_{t_k} )X^1_{t_k t_{k+1}}+Df(X_{t_k})X^2_{t_k t_{k+1}}+...+\frac{1}{(\ell-1)!}D^{\ell-1}f(X_{t_k})X^{\ell}_{t_k t_{k+1}}$$

\section{References}

* {#Young36} LC Young, _An inequality of the Hölder type, connected with Stieltjes integration_, Acta Math. **67** (1936), 251--282. doi:[10.1007/BF02401743](https://doi.org/10.1007/BF02401743), ([Project Euclid](https://projecteuclid.org/euclid.acta/1485888152)).

* Peter Friz and [[Martin Hairer]], A Course on Rough Paths, (2014), doi:[10.1007/978-3-319-08332-2](https://doi.org/10.1007/978-3-319-08332-2), ([pdf](http://www.hairer.org/notes/RoughPaths.pdf)).

* Peter Friz and Nicolas Victoir, _Multidimensional Stochastic Processes as Rough Paths: Theory and Applications_ (2010) doi:[10.1017/CBO9780511845079](https://doi.org/10.1017/CBO9780511845079) ([pdf](http://page.math.tu-berlin.de/~friz/master4_May6th.pdf)).