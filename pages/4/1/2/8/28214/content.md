## Overview

Faddeev--Le Verrier algorithm (also called Frame--Faddeev algorithm) is an $n$-step procedure to provide the inverse of an $n\times n$ square [[matrix]] $A$ if it exists and, along the way, the coefficients of the characteristic polynomial of $A$ using multiplication of matrices, calculating the trace and subtraction of matrices.

## Statement

Let $A$ be a $n\times n$ square matrix over a [[field]]
and $I$ the unit matrix of the same size. 
Define
$$\begin{matrix}
A_1 = A & \sigma_1 = tr A_1 & B_1 = A_1 - \sigma_1 I \\
A_2 = A B_1 & \sigma_2 = \frac{1}{2}tr A_2 & B_1 = A_2 - \sigma_2 I \\
\vdots &\vdots &\vdots \\
A_k = A B_{k-1}& \sigma_k = \frac{1}{k}tr A_k & B_k = A_k -\sigma_k I\\
\vdots &\vdots &\vdots\\
A_n = A B_{n-1}& \sigma_k = \frac{1}{k}tr A_n & B_n = A_n -\sigma_n I
\end{matrix}
$$
Then $B_n = 0$ and the [[characteristic polynomial]] 
$\kappa_A(\lambda) = det(\lambda I - A)$ of $A$ is then
explicitly
$$
\kappa_A(\lambda) = \lambda^n - \sigma_1 \lambda^{n-1} - \ldots - \sigma_n I.
$$
The matrix $A$ is regular (has an inverse) iff 
$\sigma_\n\neq 0$ and its inverse $A^{-1}$ is
$$
A^{-1} = \frac{B_{n-1}}{\sigma_n}.
$$

## References

* Urbain Le Verrier, _Sur les variations séculaires des éléments des orbites pour les sept planètes principales_, J. de Math. (1) 5, 230 (1840).  [PDF](http://gallica.bnf.fr/ark:/12148/bpt6k163849/f228n35.capture).

* D. K. Faddeev, I. S. Sominskii, _Problems in Higher Algebra_, (translated from the Russian by J. L. Brenner), W. H. Freeman and Company, 1965.
