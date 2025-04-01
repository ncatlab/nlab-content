## Idea

Any triple of distinct points in a [[projective line]] over a [[field]] $K$ may be transformed by a [[projective transformation]] (an element of [[projective general linear group|PGL(2,K)]], in the case of $K = \mathbf{C}$ (the [[complex numbers]]) known as a [[Möbius transformation]]) to another given triple of distinct points (i.e., the group $PGL(2,K)$ is 3-transitive on the projective line). Therefore no projective invariant can be attached to a triple of points and if three points are the starting parameters for some problem in projective geometry we may and typically do give them fixed values of $0,1,\infty$. However for any projective line there is a unique isomorphism with $P(K)$ which sends three given points $A,B,C$ in the projective line to $\infty, 0,1$ in $P(K)$ respectively. The cross ratio $(A,B;C,D)$ is then the image of $D$ under this isomorphism. 

## When the projective line is identified with $P(K)$

The unique element in $PGL_2(K)$ that takes $(A, B, C)$ to $(\infty, 0, 1)$ may be described as the [[fractional linear transformation]] 

$$p_{A, B, C}: z \mapsto \frac{z - B}{z - A} \cdot \frac{C - A}{C - B}$$  

The simplest projective invariant can be attached to a quadruple of points and it is the cross ratio. It can be expressed in various ways, e.g., 

$$
(A,B,C,D) \coloneqq \frac{A - C}{A - D}\frac{B - D}{B - C}
$$

which is the value $p_{A, B, C}(D)$ using the fractional linear transformation above. 

If the cross ratio for $(A,B,C,D)$ is $\lambda$ and the order of the four points is changed than the cross ratio takes one of the following values, depending on the permutation:

$$
\lambda, \frac{1}\lambda, 1-\lambda, \frac{1}{1-\lambda}, \frac{\lambda - 1}\lambda, \frac\lambda{\lambda-1}
$$ 

## Literature

Modern treatment is in Chapter 6 of 

* [[Marcel Berger]], _Géométrie_, Cassini (Engl. transl. Geometry I, Springer)

An elementary introduction can be found in

* Lucienne Félix, The modern aspect of mathematics, (Rus. transl.: Элементарная математика в современном изложении, 1967)

and a quick overviews in

* F. Labourie, What is a Cross Ratio, Notices of the AMS, 55 (2008), no. 10, pp.1234–1235 [pdf](https://www.math.u-psud.fr/~labourie/preprints/pdf/whatis.pdf)
* wikipedia [cross-ratio](https://en.wikipedia.org/wiki/Cross-ratio), [Möbius transformation](https://en.wikipedia.org/wiki/M%C3%B6bius_transformation)

There is a noncommutative version

* Vladimir Retakh, _Noncommutative cross-ratios_, Journal of Geometry and Physics __82__ (2014) 13-17 [arxiv/1401.5770](https://arxiv.org/abs/1401.5770) [doi](https://doi.org/10.1016/j.geomphys.2014.04.001)


category: geometry
