Lax equation is used in [[integrable system]]s; namely some systems are equivalent to the Lax equation. 

__Lax equation__ is a linear [[ordinary differential equation]] of the form
$$
\frac{d L}{d t} = [M, L]
$$
for $n\times n$-matrix-valued function $L = L(t)$, where $M$ is also a $n\times n$ matrix. The pair $(L,M)$ is also called a __Lax pair__. 

The Lax equation is the compatibility condition for the system
$$
\lambda \psi = L \psi 
$$
$$
\frac{d \psi}{d t} = M\psi
$$
where $\psi = \psi(t)$ is a vector function which is an eigenvector for $L$ with eigenvalue $\lambda$. To see this make a derivative of $L\psi$ and use the Leibniz rule. 
$$
M L \psi = M \lambda \psi = \lambda M \psi = \lambda \frac{d \psi}{d t} = \frac{d (\lambda\psi)}{d t} = \frac{d (L\psi)}{d t} = \frac{d L}{d t} \psi + L \frac{d \psi}{d t} = \frac{d L}{d t} \psi + L M\psi
$$

* Peter Lax, _Integrals of nonlinear equation of evolution and solitary waves_, Commun. on Pure and Applied Mathematics __21__:5, 467&#8211;490, 1968 [doi](http://dx.doi.org/10.1002/cpa.3160210503)
[[!redirects Lax equations]]
[[!redirects Lax pair]]