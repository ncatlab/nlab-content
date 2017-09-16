The __Legendre polynomial__ $P_l$ (for $l =0,1,2,\ldots$) is the [[polynomial]] in one variable given by the formula
$$
P_l(x) = \frac{1}{2^l l!} \frac{d^l}{d x^l}(x^2-1)^l
$$
 
The Legendre polynomials satisfy:

*  the following [[differential equation]] of the second order
$$
\frac{d}{d x}[(1-x^2)\frac{d P_l}{d x}] + l(l+1) P_l = 0
$$
*  the recursion relations 
$$
(l+1)P_{l+1}-(2l+1)x P_l+l P_{l-1}=0
$$
*  the mixed differential recursion relations
$$ \array {
P'_{l+1}-P'_{l-1} = (2l+1)P_l
\\
P'_{l+1}-x P'_l = (l+1)P_l
\\
(x^2-1)P_l'-l x P_l+l P_{l-1} = 0
} $$

The first few Legendre polynomials are $P_0(x) = 1$, $P_1(x) = x$, $P_2(x)=\frac{1}{2}(3x^2-1)$, $P_3(x)=\frac{1}{2}(5x^2-3)$, $P_4(x)=\frac{1}{8}(35x^4-30x^2+3)$.
Legendre polynomials form a system of orthogonal polynomials on the interval $[-1,1]$.

A generalization of Legendre polynomials are the __Legendre functions__ $P_\nu$ where $\nu$ is not necessarily an integer and $P^m_l$ which are given by
$$
P^m_l(x) = \frac{(-1)^m}{2^l l!} (1-x^2)^{m/2} \frac{d^{l+m}}{d x^{l+m}} (x^2-1)^l = (-1)^m (1-x^2)^{m/2} \frac{d^{l}}{d x^{l}} P_l(x) 
$$
for $m\geq 0$ and also
$$
P^{-m}_l(x)= (-1)^m\frac{(l-m)!}{(l+m)!} P^m_l(x)
$$

These $P^m_l$ are satisfying the orthogonality relations
$$
\int_{-1}^1 P^m_l(x) P^m_k(x) d x = \frac{2}{2l+1}\frac{(l+m)!}{(l-m)!}\delta_{lk}
$$
and the differential equation
$$
\frac{d}{d x}[(1-x^2)\frac{d P^m_l}{d x}]+[(l(l+1)-\frac{m^2}{1-x^2}]P^m_l = 0
$$

One also has the integral formulas
$$ \array {
\int^1_0 P_{2k+1}(x) d x = \frac{(-1)^k (2k)!}{2^{2k+1} k! (k+1)!}
\\
\int^1_0 P_{2k}(x) d x = \delta_{k0}
\\
\int^1_{-1} x P_l P_k = \left\lbrace
\array{  \frac{2(l+1)}{(2l+1)(2l+3)},&k=l+1 \\
\frac{(2l)}{(2l-1)(2l+1)},&k=l-1\\
0,& otherwise}
\right.
} $$

$P_\nu(x)$ is a special case of a [[hypergeometric function]], namely
$$
P_\nu(x)={}_2 F_1(-\nu,\nu+1;1;\frac{1-x}{2})
$$

Legendre polynomials enter the expressions for the [[spherical function]]s for sphere $S^2$ in 3d:
$$
Y_{l m}(\theta,\phi) = \sqrt{ \frac{2l+1}{4\pi}\frac{(l-m)!}{(l+m)!} } P^m_l(cos\theta) e^{im\phi}
$$


[[!redirects Legendre polynomials]]