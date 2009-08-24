A __Euclidean space__ is an [[affine space|affine]] [[inner product space]].  That is, it is an affine space $E$ modelled on a [[vector space]] $V$ which has an inner product.

One generally takes the inner product to be positive-definite; otherwise, we say that $E$ is only a _pseudo-Euclidean space_.  Also, one generally takes the dimension to be finite; [[Euclid]] himself only considered dimensions up to $3$.  For an infinite-dimensional Euclidean space, you would probably want $V$ to be a [[Hilbert space]].

Arguably, the spaces studied by Euclid were not really modelled on inner product spaces, as the distances were lengths, not [[real numbers]] (which, if non-negative, are ratios of lengths).  So we should say that $V$ has an inner product valued in some oriented [[line]] $L$ (or rather, in $L^2$).  Of course, Euclid did not use the inner product (which takes negative values) directly, but today we can recover it from what Euclid did discuss: lengths (valued in $L$) and angles (dimensionless).

Since the days of [[Rene Descartes]], it is common to identify a Euclidean space with a [[Cartesian space]], that is $\mathbb{R}^n$ for $n$ the dimension.  But Euclid\'s spaces had no coordinates; and in any case, what we do with them today is still coordinate-independent.


## Lengths and angles

Given two points $x$ and $y$ of a Euclidean space $E$, their difference $x - y$ belongs to the vector space $V$, where it has a norm
$$ \|x - y\| = \sqrt{\langle{x - y, x - y}\rangle} .$$
This real number (or properly, element of the line $L$) is the __distance__ between $x$ and $y$, or the __length__ of the line segment $\overline{x y}$.  This distance function makes $E$ into an ($L$-valued) [[metric space]].

Given three points $x, y, z$, with $x, y \ne z$ (so that $\|x - z\|, \|y - z\| \ne 0$), we can form the ratio
$$ \frac{\langle{x - z, y - z}\rangle}{\|x - z\|\,\|y - z\|} ,$$
which is a (dimensionless) real number.  By the Cauchy--Schwartz inequality, this number lies between $-1$ and $1$, so it\'s the cosine of a unique angle measure between $0$ and $\pi$ radians.  This is the measure of the __angle__ $\angle x z y$.  In a $2$-dimensional Euclidean space, we can interpret $\angle x z y$ as a signed angle if we fix an [[orientation]] of $E$.