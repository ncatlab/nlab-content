
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[ring]] of symmetric [[polynomials]] in $n$ [[variables]] has a [[linear basis]] $\{s_\lambda\}$ of __Schur polynomials__ indexed by [[partitions]] $\lambda = \lambda_1 \geq \lambda_2 \geq \ldots \geq \lambda_n$  in $n$ parts. 

The Schur polynomials  are precisely the [[irreducible characters]] of [[finite dimensional vector space|finite dimensional]] polynomial [[linear representation|representations]] of [[general linear group|GL(n)]]. 

Also, the character $\chi_{\lambda}$ of $V_\lambda$, the irreducible representation of $S_k$ attached to $\lambda$ (for $k$ the size $|\lambda|$ of the partition) maps to the Schur polynomial under the character map
$ch$ from virtual characters to symmetric polynomials. This correspondance between representations of the symmetric groups and the general linear groups is called [[Schur Weyl Duality]] 

## Definition

Given the [[partition]] $\lambda_1\geq \lambda_2\geq \ldots \geq \lambda_n$, the corresponding __Schur polynomial__ is defined as follows. First define the $n\times n$-[[determinant]] (for any partition $\alpha$ in $n$ parts)

$$
  a_\alpha \;\coloneqq\; det\big(x_i^{\alpha_j}\big).
$$

Let $\delta=(n-1, n-2, \dots, 1, 0)$. Then the Schur polynomial attached to $\lambda$ is the quotient

$$
  s_{\lambda}(x_1,x_2,\dots,x_n)
  =
  a_{\lambda+\delta}/a_{\delta}.
$$

As is usual in the theory of [[symmetric functions]] one can also deal with [[formal power series]] in infinitely many variables. To make this precise one uses an [[inverse limit]] (see Macdonald) and obtains a __Schur function__ $s_{\lambda}$ for each partition, depending on countably many variables $x_1, x_2,\dots,x_n,x_{n+1}, \dots$.

## Properties

### In terms of $Sym(n)$-Characters

\begin{prop}
**(Frobenius formula)**

$$
  s_\lambda
   \;=\;
  \frac{1}{n!}
  \underset
    {\sigma \in Sym(n)}
    {\sum}
  \chi^{(\lambda)}(\sigma)
  \cdot
  p_\sigma
$$
\end{prop}

([Sagan 01, Thm. 4.6.4](#Sagan01), [Sagan Enc., Thm. 3](#SaganEnc))



## Generalizations via Schur functors

[[Schur functors]] may be viewed as a [[categorification]] of Schur functions. In fact, the Schur functors make sense in more general [[symmetric monoidal categories]] than [[VectorSpaces]]. It is a theorem in the case of vector space that the [[trace]] of 
a Schur functor $\mathbf{S}_\lambda(V)\stackrel{\mathbf{S}_\lambda(g)}\to \mathbf{S}_\lambda(V)$ on an endomorphism $g\in GL(V)$ is the Schur function of the eigenvalues of $g$. Considering the trace of a Schur functor makes sense in a general situation allowing for Schur functors and for the trace ([[rigid monoidal category]]); of course choosing appropriate variables to express the trace may depend on a context. 

## Related concepts

* [[Schur positivity]]

* [[representation theory of the symmetric group]]

Generalizations:

* [[Jack polynomial]]

* [[Macdonald polynomial]]

* [[noncommutative Schur function]]

* [[quasisymmetric Schur function]]

\linebreak


## References

The concept first appears in work by [[Carl Jacobi]] on [[determinants]]. 

It is named after:

* [[Issai Schur]], *Über eine Klasse von Matrizen die sich einer gegeben Matrix zuordnen lassen*, Inaugural-Dissertation, Berlin (1901)

Textbook accounts:

* I. G. Macdonald, Section I.3 of: _Symmetric functions and Hall polynomials_, Oxford Math. Monographs, 2nd enlarged ed. 1995 ([ISBN:9780198739128](https://global.oup.com/academic/product/symmetric-functions-and-hall-polynomials-9780198739128?cc=ae&lang=en&))


* {#Sagan01} [[Bruce Sagan]], Section 4.4 of: _The symmetric group_, Springer 2001 ([doi:10.1007/978-1-4757-6804-6](https://link.springer.com/book/10.1007/978-1-4757-6804-6), [pdf](http://math.sfsu.edu/federico/Clase/RepTh/sagan.pdf))

* Stuart Martin, _Schur algebras and representation theory_, Cambridge Univ. Press 1994 


Survey:

* {#SaganEnc} [[Bruce E. Sagan]], _Schur functions_, in (M. Hazewinkel, ed.) Encyclopaedia of Mathematics, Springer ([pdf](http://www.mth.msu.edu/~sagan/Papers/Old/schur.pdf), [[SaganSchurFunctions.pdf:file]])

* Wikipedia, *[Schur polynomial](https://en.wikipedia.org/wiki/Schur_polynomial)*



See also:

* Olivier Blondeau-Fournier, Pierre Mathieu, _Schur superpolynomials: combinatorial definition and Pieri rule_, [arxiv/1408.2807](http://arxiv.org/abs/1408.2807)

* Miles Jones, Luc Lapointe, _Pieri rules for Schur functions in superspace_, [arxiv/1608.08577](https://arxiv.org/abs/1608.08577)

[[!redirects Schur functions]]

[[!redirects Schur polynomial]]
[[!redirects Schur polynomials]]


