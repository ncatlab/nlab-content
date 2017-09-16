The __Legendre polynomial__ $P_l$ (for $l =0,1,2,\ldots$) is the [[polynomial]] in one variable given by the formula
$$
P_l(x) = \frac{1}{2^l l!} \frac{d^l}{d x^l}(x^2-1)^l
$$
 
Alternatively they can be defined via a generating function:

$$
\frac{1}{\sqrt{1-2tx+t^2}} = \sum_{n\geq 0} P_n(x) t^n
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

Legendre polynomials form a system of orthogonal polynomials on the interval $[-1,1]$. The first few Legendre polynomials are $P_0(x) = 1$, $P_1(x) = x$, $P_2(x)=\frac{1}{2}(3x^2-1)$, $P_3(x)=\frac{1}{2}(5x^2-3)$, $P_4(x)=\frac{1}{8}(35x^4-30x^2+3)$.
Their values at $0$ are 
$$
P_{2n+1}(0)=0,\,\,\,\,\,P_{2n}(0)=(-1)^n\frac{(2n-1)!!}{(2n)!} = \frac{(-1)^n (2n)!}{2^{2n}(n!)^2}
$$
and $P_l(\pm 1)= (\pm 1)^l$.

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
recursion relation
$$
x P^m_l(x) = \frac{l+|m|}{2l+1}P^m_{l-1}(x)+\frac{l-|m|+1}{2l+1} P^m_{l+1}(x)
$$
and the differential equation
$$
\frac{d}{d x}[(1-x^2)\frac{d P^m_l}{d x}]+[(l(l+1)-\frac{m^2}{1-x^2}]P^m_l = 0
$$

$P_\nu(x)$ is a special case of a [[hypergeometric function]], namely
$$
P_\nu(x)={}_2 F_1(-\nu,\nu+1;1;\frac{1-x}{2})
$$

Legendre polynomials enter the expressions for the [[spherical function]]s for sphere $S^2$ in 3d:
$$
Y_{l m}(\theta,\phi) = \sqrt{ \frac{2l+1}{4\pi}\frac{(l-m)!}{(l+m)!} } P^m_l(cos\theta) e^{im\phi}
$$
(If it is not clear from mathML rendering -- both fractions are under square root -- including both the numerators and denominators). 

If $(\theta,\phi)$ and $(\theta',\phi')$ are two points of the unit sphere in spherical coordinates (polar angle, azimuth), and $\gamma$ is the angle between the two corresponding rays from the origin then

$$
P_l(cos \gamma) = \sum_{m=-l}^l (-1)^m P_l^m(cos \theta)P_l^{-m}(cos \theta') cos(m(\phi-\phi')) = \frac{4\pi}{2l+1}\sum_{m=-l}^l Y_{lm}(\theta,\phi) Y_{lm}^*(\theta',\phi')
$$

what for $l=1$ reduces to the __spherical law of cosine__ from [spherical trigonometry](http://en.wikipedia.org/wiki/Spherical_trigonometry):

$$
cos \gamma = P_1(cos \gamma) = cos\theta cos\theta' + sin\theta sin\theta' cos(\phi-\phi')
$$

The orthogonality relation for Legendre polynomials gives
Laplace's formula

$$
\int_{S^2} d\Omega_{\hat{k}} Y_l(\hat{k}) P_l(\hat{k}\hat{p}) = \frac{4\pi}{2l+1} \delta_{ll'} Y_l(\hat{p})
$$

where $\hat{k},\hat{p}$ are unit vectors and $Y_l = \sum a_m Y_{lm}$ is some spherical function.  

The following orthogonality integral relation is over product of unit spheres in $\mathbb{R}^3$: 
$$
\int_{\hat{k}}\int_{\hat{p}} d\Omega_{\hat{k}}d\Omega_{\hat{p}} P_l(\hat{k}\hat{p}) P_{l'}(\hat{k}\hat{q}) P_{l''}(\hat{p}\hat{q}) = \left(\frac{4\pi}{2l+1}\right)\delta_{ll'}\delta_{ll''}, \,\,\,\,\,(*)
$$
where the arguments of Legendre polynomials are the scalar products of the unit vectors. 

_Zoran_: the last formula $(*)$ is in my own formula notes which I have written as a student many years ago and used hundreds of times, but it now looks to me suspicious; I have no time to check it right now. 


[[!redirects Legendre polynomials]]