
\tableofcontents

## Idea

Any [[triple]] of distinct points in a [[projective line]] over a [[field]] $K$ may be transformed by a [[projective transformation]] (an element of [[projective general linear group|PGL(2,K)]], in the case of $K = \mathbf{C}$ (the [[complex numbers]]) known as a [[Möbius transformation]]) to another given triple of distinct points (i.e., the group $PGL(2,K)$ is 3-transitive on the projective line). Therefore no projective invariant can be attached to a triple of points and if three points are the starting parameters for some problem in projective geometry we may and typically do give them fixed values of $0,1,\infty$ in $P^1(K) = P(K^2)$. (Here $P(K^2)$ is also identified with $K\cup\{\infty\}$.) However, for any projective line there is a unique (projective) isomorphism with $P^1(K)$ which sends three distinct points $A,B,C$ in a projective line to $\infty, 0,1$ in $P^1(K)$ respectively. 

The __cross ratio__ $(A,B;C,D)$ is then the image of $D$ under this isomorphism. Conversely, given distinct points $A,B,C$ in a projective line and $k\in K\cup\{\infty\}$ there is a unique point $D$ such that $(A,B;C,D) = k$.

## When the projective line is identified with $P^1(K)$

The unique element in $PGL(2,K)$ that takes $(A, B, C)$ to $(\infty, 0, 1)$ may be described as the [[fractional linear transformation]] 

$$p_{A, B, C}: z \mapsto \frac{z - B}{z - A} \cdot \frac{C - A}{C - B}$$  

The simplest projective invariant can be attached to a quadruple of points and it is the cross ratio. It can be expressed in various ways, e.g., 

$$
(A,B,C,D) \coloneqq \frac{A - C}{A - D}\frac{B - D}{B - C}
$$

which is the value $p_{A, B, C}(D)$ using the fractional linear transformation above. 

If the cross ratio for $(A,B;C,D)$ is $\lambda$ and the order of the four points is changed than the cross ratio takes one of the following values, depending on the permutation:

$$
\lambda, \frac{1}\lambda, 1-\lambda, \frac{1}{1-\lambda}, \frac{\lambda - 1}\lambda, \frac\lambda{\lambda-1}
$$ 

## Parametrized lines and cross ratio

Suppose the projective line is embedded in $P^n(K)$.
This line is given in homogeneous coordinates of $n$-dimensional space $P^n(K)$ by parametric equations
$$
\rho x_r = t a_r + u b_r, \,\,\,\,r = 0,\ldots,n
$$
where $a = (a_r)_r$ and $b = (b_r)_r$ are coordinates of
two points, $\rho$ is arbitrarily (by homogeneity) chosen constant and $\tau = t/u$ is a variable parameter determining a point. For $t = 0$ and $u = 0$ we get $b$ and $a$ respectively. If $\tau_1,\tau_2,\tau_3,\tau_4$ are the parameters of 4 points than the parameter cross ratio
$$
\frac{\tau_1 - \tau_3}{\tau_2 - \tau_3}\frac{\tau_1 - \tau_4}{\tau_2 - \tau_4}
$$
equals to the cross ratio of those 4 points.
 

## Application to homogeneous coordinates

Given an abstract projective $n$-space $P(V)$, a projective frame ("basis" for homogeneous coordinates) 
is given by $(n+2)$ points. 
One chooses an $n$-dimensional simplex whose $(n+1)$ vertices $A_r$ will have the coordinates $(x_0,\ldots,x_n)$ all zero except $x_r = 1$; $(n+1)$-tuple $(A_i)_i$ is the image of a lifted basis $(e_i)_{i=1,\ldots,n+1}$ in the $(n+1)$-dim vector space $V$. Such a basis is highly nonunique, hence this still does not determine a homogeneous coordinates of a general point: if we replace each vector of the basis by a multiple, a sum with some coefficients (components) will not be necessarily an overall multiple of that sum. To fix this, one needs to choose additional point $U$ not on any of the hyperplanes containing sides of the simplex, for which one postulates  coordinates $(1,\ldots,1)$. In other words, $U$ is the image of $e_1+\ldots+e_{n+1}$ under the projection $V\to P(V)$); this property of $U$ is preserved only if we change $e_i$ to $\alpha e_i$ where $\alpha$ does not depend on $i$. Thus, choice of $U$ forces a unique choice of a basis in $V$ up to a common multiple, which then makes coordinates of all other points well defined. Now we want to see which coordinates are assigned to an arbitrary other point $P$. 
Line $P U$ intersects the hyperplane $x_r = 0$ (containing the simplex face opposite to $A_r$) in a point $L_r$. The parametric equations of $P U$ are $\rho x_r = t x_r' + u 1$ for all $r$ if $(x_r')_r$ are coordinates of $P$. For $t = 0$ for $U$, $u = 0$ for $P$, then 
and $0 = t x_r + u$ for $L_r$. Hence the cross ratio $(L_k, L_r; U, P)$ for $k\neq r$ calculates as the parameter cross ratio
$$
(L_k, L_r; U, P) = (-x_r')/(-x_k')
$$
if $x_k'\neq 0$..
One fixes $k$ such that $x_k'\neq 0$, that is $P$ is not on the hyperplane opposite to $A_k$.
Thus this cross ratio times $x_k'$ is the $k$-th homogeneous coordinate of $p$ (and we can choose $x_k' = 1$). See D. M. Y. Sommerville, _Introduction to the geometry of N dimensions_, [gBooks](https://books.google.hr/books?id=4vXDDwAAQBAJ&pg=PA55).

## Harmonic quadruples

A quadruple of points $(A,B,C,D)$ is called [[harmonic ratio|harmonic]] if the cross-ratio $(A,B;C,D) = -1$; points $C$ and $D$ are then called harmonic conjugates and $(A,B;D,C) = -1$ as well. We say that this ratio is harmonic and that the quadruple $(A,B,C,D)$ is harmonic. For this reason, the cross ratio in general is often called the anharmonic ratio as it measures the difference from the harmonic special case. 

Harmonic conjugates can be characterized in geometric terms, see at [[harmonic ratio]].

## Literature

Modern treatment is in Chapter 6 of 

* [[Marcel Berger]], _Géométrie_, Cassini (Engl. transl. Geometry I, Springer)

An elementary introduction can be found in

* Lucienne Félix, The modern aspect of mathematics, (Rus. transl.: Элементарная математика в современном изложении, 1967)

and a quick overviews in

* F. Labourie, _What is a cross ratio_, Notices of the AMS, 55 (2008), no. 10, pp.1234--1235 [pdf](https://www.math.u-psud.fr/~labourie/preprints/pdf/whatis.pdf)
* wikipedia [cross-ratio](https://en.wikipedia.org/wiki/Cross-ratio), [Möbius transformation](https://en.wikipedia.org/wiki/M%C3%B6bius_transformation)

See also:

* Wikipedia: *[Cross-ratio](https://en.wikipedia.org/wiki/Cross-ratio)*

There is a [[noncommutative geometry|noncommutative]] version

* Vladimir Retakh, _Noncommutative cross-ratios_, Journal of Geometry and Physics __82__ (2014) 13-17 [arxiv/1401.5770](https://arxiv.org/abs/1401.5770) [doi](https://doi.org/10.1016/j.geomphys.2014.04.001)

category: geometry
[[!redirects cross-ratio]]
[[!redirects anharmonic ratio]]

