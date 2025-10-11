
> See also _[[compact symplectic group]]_.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The *quaternion unitary group*, often  denoted $Sp(n)$ in the math literature (rarely but alternatively: $\mathrm{U}(n, \mathbb{H})$, is a [[Lie group]] which is the analog of the [[unitary group]] as one passes from the [[complex numbers]] to the [[quaternions]], hence it is the group of quaternion-[[unitary transformations]] of the [[quaternionic vector space]] $\mathbb{H}^n$.  

Beware that this group is also called the *[[compact symplectic group]]*, since both it and the [[symplectic group]] $Sp(2n, \mathbb{R})$ are [[real forms]] of the [[complex Lie group]] $Sp(2n,\mathbb{C})$, but $Sp(n)$ is the compact form.  

## Definition

\begin{definition}
\[
  \label{TheDefinition}
  Sp(n) \equiv U(n,\mathbb{H})
  \;\coloneqq\;
  \Big\{
    U \in Mat_{n \times n}(\mathbb{H})
    \;\Big\vert\;
    U \cdot U^\dagger = I_n
  \Big\}
\]
\end{definition}

(cf. [Zhang 1997, p. 28](#Zhang1997))

\begin{remark}
The condition in (eq:TheDefinition) is indeed sufficient, since for $B \in Mat_{n \times n}(\mathbb{H})$ we have
$$
  \begin{array}{cl}
    & B \cdot B^\dagger = I_n
    \\
    \Leftrightarrow
    &
    B^\dagger \cdot B = I_n
  \end{array}
$$
(cf. [Zhang 1997, Prop. 4.1](#Zhang1997)).
\end{remark}

## Properties

### Exceptional isomorphisms

* $Sp(1) \simeq$ [[Spin(3)]] ([this Prop.](Spin3#ExceptionalIsoToSp2))

* $Sp(2) \simeq$ [[Spin(5)]] ([this Prop.](Spin5#ExceptionalIsomorphismOfSU2ToSpin3AndSp1))

## Related concepts

* A [[Riemannian manifold]] of [[dimension]] $4n$ is called a _[[quaternion-Kähler manifold]]_ if its [[holonomy group]] is a [[subgroup]] of the [[quotient group]] [[Sp(n).Sp(1)]] of the [[direct product group]] $Sp(n) \times Sp(1)$. If it is even a subgroup  of just the $Sp(n)$ factor, then it is called a _[[hyperkähler manifold]]_.

* [[Gromoll-Meyer sphere]]

* [[quaternionic projective space]]

* [[symplectic group]]

* [[SL(2,H)]]

## References

* {#Zhang1997} [[Fuzhen Zhang]], p. 28 of: *Quaternions and matrices of quaternions*, Linear Algebra and its Applications **251** (1997) 21-57 \[<a href="https://doi.org/10.1016/0024-3795(95)00543-9">doi:10.1016/0024-3795(95)00543-9</a>\]

* [[Howard Georgi]], §26 in: *Lie Algebras In Particle Physics*, Westview Press (1999), CRC Press (2019) &lbrack;[doi:10.1201/9780429499210](https://doi.org/10.1201/9780429499210)&rbrack;

* {#CohenDeLeo99} Nir Cohen, Stefano De Leo, Cor. 6.4 in: *The quaternionic determinant*, Electronic Journal of Linear Algebra **7** (2000) 100-111 &lbrack;[arXiv:math-ph/9907015](https://arxiv.org/abs/math-ph/9907015), [doi:10.13001/1081-3810.1050](https://doi.org/10.13001/1081-3810.1050), [eudml:121484](https://eudml.org/doc/121484)&rbrack;

See also:

* _Quaternionic groups_ ([pdf](http://www-math.mit.edu/~dav/quatcoordfree.pdf))




[[!redirects quaternionic unitary groups]]

[[!redirects Sp(n)]]

[[!redirects quaternion unitary group]]
[[!redirects quaternion unitary groups]]
