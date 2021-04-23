
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

The determinant is the (essentially unique) universal alternating multilinear map.

## Definition

### Preliminaries on exterior algebra

Let [[Vect]]${}_k$ be the [[category]] of [[vector space|vector spaces]] over a [[field]] $k$, and assume for the moment that the [[characteristic]] $char(k) \neq 2$. For each $j \geq 0$, let 

$$sgn_j \colon S_j \to \hom(k, k)$$ 

be the 1-dimensional [[sign representation]] on the [[symmetric group]] $S_j$, taking each transposition $(i j)$ to $-1 \in k^\ast$. We may linearly extend the sign action of $S_j$, so that $sgn$ names a (right) $k S_j$-[[module]] with underlying [[vector space]] $k$. At the same time, $S_j$ acts on the $j^{th}$ [[tensor product]] of a vector space $V$ by permuting tensor factors, giving a left $k S_j$-module structure on $V^{\otimes j}$. We define the [[Schur functor]] 

$$\Lambda^j \colon Vect_k \to Vect_k$$ 

by the formula 

$$\Lambda^j(V) = sgn_j \otimes_{k S_j} V^{\otimes j}.$$ 

It is called the $j^{th}$ **alternating power** (of $V$). 

Another point of view on the alternating power is via [[superalgebra]]. For any [[cosmos]] $\mathbf{V}$ let $CMon(\mathbf{V})$ be the category of [[commutative monoid]] objects in $\mathbf{V}$. The forgetful functor $CMon(\mathbf{V}) \to \mathbf{V}$ has a [[left adjoint]] 

$$\exp(V) = \sum_{n \geq 0} V^{\otimes n}/S_n$$ 

whose values are naturally regarded as graded by degree $n$. 

This applies in particular to $\mathbf{V}$ the category of [[supervector spaces]]; if $V$ is a supervector space concentrated in odd degree, say with component $V_{odd}$, then each symmetry $\sigma: V \otimes V \to V \otimes V$ maps $v \otimes w \mapsto -w \otimes v$ for elements $v, w \in V_{odd}$. It follows that the graded component $\exp(V)_n$ is concentrated in $parity(n)$ degree, with component $\Lambda^n(V_{odd})$. 

+-- {: .num_prop} 
###### Proposition 
There is a canonical natural isomorphism $\Lambda^n(V \oplus W) \cong \sum_{j + k = n} \Lambda^j(V) \otimes \Lambda^k(W)$. 
=-- 

+-- {: .proof} 
###### Proof 
Again take $\mathbf{V}$ to be the category of supervector spaces. Since the left adjoint $\exp: \mathbf{V} \to CMon(\mathbf{V})$ preserves [[coproducts]] and since the tensor product $\otimes$ of $\mathbf{V}$ provides the coproduct for commutative monoid objects, we have a natural isomorphism 

$$\exp(V \oplus W) \cong \exp(V) \otimes \exp(W).$$ 

Examining the grade $n$ component $\exp(V \oplus W)_n$, this leads to an identification 

$$\exp(V \oplus W)_n = \sum_{j + k = n} \exp(V)_j \otimes \exp(W)_k.$$ 

and now the result follows by considering the case where $V, W$ are concentrated in odd degree. 
=-- 

+-- {: .num_cor}
###### Corollary 
If $V$ is $n$-[[dimension|dimensional]], then $\Lambda^j(V)$ has dimension $\binom{n}{j}$. In particular, $\Lambda^n(V)$ is 1-dimensional. 
=-- 

+-- {: .proof}
###### Proof 
By induction on dimension. If $\dim(V) = 1$, we have that $\Lambda^0(V)$ and $\Lambda^1(V)$ are $1$-dimensional, and clearly $\Lambda^n(V) = 0$ for $n \geq 2$, at least when $char(k) \neq 2$. 

We then infer 

$$\array{
\Lambda^j(V \oplus k) & \cong & \sum_{p + q = j} \Lambda^p(V) \otimes \Lambda^q(k) \\ 
 & \cong & \Lambda^j(V) \oplus \Lambda^{j-1}(V)
}$$ 

where the dimensions satisfy the same recurrence relation as for [[binomial coefficients]]: $\binom{n+1}{j} = \binom{n}{j} + \binom{n}{j-1}$. 
=-- 

More concretely: if $e_1, \ldots, e_n$ is a basis for $V$, then expressions of the form $e_{n_1} \otimes \ldots \otimes e_{n_j}$ form a [[basis of a vector space|basis]] for $V^{\otimes j}$. Let $e_{n_1} \wedge \ldots \wedge e_{n_j}$ denote the [[image]] of this element under the [[quotient]] map $V^{\otimes j} \to \Lambda^j(V)$. We have 

$$e_{n_1} \wedge \ldots \wedge e_{n_i} \wedge e_{n_{i+1}} \wedge \ldots \wedge e_{n_j} = -e_{n_1} \wedge \ldots \wedge e_{n_{i+1}} \wedge e_{n_i} \wedge \ldots \wedge e_{n_j}$$ 

(consider the transposition in $S_j$ which swaps $i$ and $i+1$) and so we may take only such expressions on the left where $n_1 \lt \ldots \lt n_j$ as forming a spanning set for $\Lambda^j(V)$, and indeed these form a basis. The number of such expressions is $\binom{n}{j}$. 


+-- {: .num_remark}
###### Remark

In the case where $char(k) = 2$, the same development may be carried out by simply decreeing that $e_{n_1} \wedge \ldots \wedge e_{n_j} = 0$ whenever $n_i = n_{i'}$ for some pair of distinct indices $i$, $i'$. 

=--

Now let $V$ be an $n$-dimensional space, and let $f \colon V \to V$ be a [[linear map]]. By the proposition, the map 

$$\Lambda^n(f) \colon \Lambda^n(V) \to \Lambda^n(V),$$ 

being an [[endomorphism]] on a 1-dimensional space, is given by multiplying by a scalar $D(f) \in k$. It is manifestly [[functor|functorial]] since $\Lambda^n$ is, i.e., $D(f g) = D(f) D(g)$. The quantity $D(f)$ is called the **determinant** of $f$. 

### Determinant of a matrix 

We see then that if $V$ is of dimension $n$, 

$$\det \colon End(V) \to k$$ 

is a [[homomorphism]] of multiplicative [[monoids]]; by commutativity of multiplication in $k$, we infer that 

$$\det(U A U^{-1}) = \det(A)$$ 

for each [[inverse|invertible]] [[linear map]] $U \in GL(V)$. 

If we choose a [[basis of a vector space|basis]] of $V$ so that we have an identification $GL(V) \cong Mat_n(k)$, then the determinant gives a [[function]]

$$\det \colon Mat_n(k) \to k$$ 

that takes products of $n \times n$ [[matrices]] to products in $k$. The determinant however is of course independent of choice of basis, since any two choices are related by a change-of-basis matrix $U$, where $A$ and its transform $U A U^{-1}$ have the same determinant. 

By following the definitions above, we can give an explicit formula: 

$$
  \det(A)  
    \;=\; 
  \sum_{\sigma \in S_n} sgn(\sigma) \prod_{i = 1}^n a_{i \sigma(i)}
  \;
$$ 


This may equivalently be written using the [[Levi-Civita symbol]] $\epsilon$ and the [[Einstein summation convention]] as

\[
  \label{DeterminantInTermsOfLCSymbol}
  \det(A)  
    \;=\; 
    a_{1 j_1}
    a_{2 j_2}
    \cdots
    a_{n j_n}
    \,
    \epsilon^{j_1 j_2 \cdots j_n}
\]

which in turn may be re-written more symmetrically as

\[
  \label{DeterminantInTermsOfLCSymbols}
  \det(A)  
    \;=\;
    \frac{1}{n!}
    \epsilon^{ i_1 i_2 \cdots i_n }
    \,
    a_{i_1 j_1}
    a_{i_2 j_2}
    \cdots
    a_{i_n j_n}
    \,
    \epsilon^{j_1 j_2 \cdots j_n}
\]



## Properties

We work over [[fields]] of arbitrary [[characteristic]]. The determinant satisfies the following properties, which taken together uniquely characterize the determinant. Write a square [[matrix]] $A$ as a row of column [[vectors]] $(v_1, \ldots, v_n)$. 

1. $\det$ is separately linear in each column vector: 
$$\det(v_1, \ldots, a v + b w, \ldots, v_n) = a\det(v_1, \ldots, v, \ldots, v_n) + b\det(v_1, \ldots, w, \ldots, v_n)$$ 

1. $\det(v_1, \ldots, v_n) = 0$ whenever $v_i = v_j$ for distinct $i, j$. 

1. $\det(I) = 1$, where $I$ is the identity matrix. 

Other properties may be worked out, starting from the explicit formula or otherwise: 

* If $A$ is a diagonal matrix, then $\det(A)$ is the product of its diagonal entries. 

* More generally, if $A$ is an upper (or lower) triangular matrix, then $\det(A)$ is the product of the diagonal entries. 

* If $E/k$ is a [[field extension]] and $f$ is a $k$-linear map $V \to V$, then $\det(f) = \det(E \otimes_k f)$. Using the preceding properties and the [[Jordan normal form]] of a matrix, this means that $\det(f)$ is the product of its [[eigenvalues]] (counted with multiplicity), as computed in the [[algebraic closure]] of $k$. 

* If $A^t$ is the transpose of $A$, then $\det(A^t) = \det(A)$. 

### Cramer's rule 

A simple observation which flows from these basic properties is 

+-- {: .num_prop} 
###### Proposition
**(Cramer's Rule)**

Let $v_1, \ldots, v_n$ be column vectors of dimension $n$, and suppose 
$$w = \sum_j a_j v_j.$$
Then for each $i$ we have 
$$a_j \det(v_1, \ldots, v_i, \ldots, v_n) = \det(v_1, \ldots, w, \ldots, v_n)$$ 
where $w$ occurs as the $i^{th}$ column vector on the right. 
=-- 

+-- {: .proof}
###### Proof 
This follows straightforwardly from properties 1 and 2 above. 
=-- 

For instance, given a square matrix $A$ such that $\det(A) \neq 0$, and writing $A = (v_1, \ldots, v_n)$, this allows us to solve for a vector $a$ in an equation 

$$A \cdot a = w$$

and we easily conclude that $A$ is invertible if $\det(A) \neq 0$. 

+-- {: .num_remark}
###### Remark

This holds true even if we replace the field $k$ by an arbitrary commutative [[ring]] $R$, and we replace the condition $\det(A) \neq 0$ by the condition that $\det(A)$ is a unit. (The entire development given above goes through, _mutatis mutandis_.) 

=--

### Characteristic polynomial and Cayley-Hamilton theorem 

Given a linear endomorphism $f: M\to M$ of a finite rank free unital module over a commutative unital ring, one can consider the zeros of the [[characteristic polynomial]] $\det(t \cdot 1_V - f)$. The coefficients of the polynomial are the concern of the [[Cayley-Hamilton theorem]]. 

### Over the real numbers: volume and orientation

A useful intuition to have for determinants of [[real number|real]] matrices is that they measure _change of volume_. That is, an $n \times n$ matrix with real entries will map a standard unit cube in $\mathbb{R}^n$ to a parallelpiped in $\mathbb{R}^n$ (quashed to lie in a hyperplane if the matrix is singular), and the determinant is, up to sign, the volume of the parallelpiped. It is easy to convince oneself of this in the planar case by a simple dissection of a parallelogram, rearranging the dissected pieces in the style of Euclid to form a rectangle. In algebraic terms, the dissection and rearrangement amount to applying shearing or [[elementary column operations]] to the matrix which, by the properties discussed earlier, leave the determinant unchanged. These operations transform the matrix into a diagonal matrix whose determinant is the area of the corresponding rectangle. This procedure easily generalizes to $n$ dimensions. 

The sign itself is a matter of interest. An invertible transformation $f \colon V \to V$ is said to be **[[orientation]]-preserving** if $\det(f)$ is positive, and **orientation-reversing** if $\det(f)$ is negative. Orientations play an important role throughout geometry and algebraic topology, for example in the study of orientable manifolds (where the tangent bundle as $GL(n)$-bundle can be lifted to a $GL_+(n)$-bundle structure, $GL_+(n) \hookrightarrow GL(n)$ being the subgroup of matrices of positive determinant). See also [[KO-theory]]. 

Finally, we include one more property of determinants which pertains to matrices with real coefficients (which works slightly more generally for matrices with coefficients in a [[local field]]): 

### As a polynomial in traces of powers
 {#AsAPolynomialInTracesofPowers}

If $A$ is an $n \times n$ [[matrix]], the determinant of its [[exponential]] equals the [[exponential]] of its [[trace]] 

$$
  \det(\exp(A)) = \exp(tr(A))
  \,.
$$

More generally, the determinant of $A$ is a [[polynomial]] in the [[traces]] of the [[powers]] of $A$:

For $2 \times 2$-matrices:

$$
  det(A)
  \;=\;
  \tfrac{1}{2}\left( tr(A)^2 - tr(A^2) \right)
$$

For $3 \times 3$-matrices:

$$
  det(A)
  \;=\;
  \tfrac{1}{6}
  \left(
    (tr(A))^3
    - 
    3 tr(A^2) tr(A)
    +
    tr(A^3)
  \right)
$$

For $4 \times 4$-matrices:

$$
  det(A)  
  \;=\;
  \tfrac{1}{24}
  \left(
    (tr(A))^4
    -
    6 tr(A^2)(tr(A))^2
    +
    3 (tr(A^2))^2
    +
    8 tr(A^3) tr(A)
    -
    6 tr(A^4)
  \right)
$$

Generally for $n \times n$-matrices ([Kondratyuk-Krivoruchenko 92, appendix B](#KondratyukKrivoruchenko92)):

\[
  \label{DeterminantAsPolynomialInTracesOfPowers}
  det(A)
  \;=\;
  \underset{ 
     { k_1,\cdots, k_n \in \mathbb{N} }
     \atop
     { \underoverset{\ell = 1}{n}{\sum} \ell k_\ell = n }
  }{\sum}
  \underoverset{ l = 1 }{ n }{\prod} 
  \frac{ (-1)^{k_l + 1} }{ l^{k_l} k_l !  }
  \left(tr(A^l)\right)^{k_l}
\]

+-- {: .proof} 
###### Proof of (eq:DeterminantAsPolynomialInTracesOfPowers) 

It is enough to prove this for semisimple matrices $A$ (matrices that are [[diagonalizable matrix|diagonalizable]] upon passing to the [[algebraic closure]] of the ground field) because this [[subset]] of matrices is [[Zariski topology|Zariski]] [[dense subset|dense]] (using for example the nonvanishing of the [[discriminant]] of the [[characteristic polynomial]]) and the set of $A$ for which the equation holds is [[Zariski topology|Zariski]] [[closed subset|closed]]. 

Thus, without loss of generality we may suppose that $A$ is [[diagonal matrix|diagonal]] with $n$ [[eigenvalues]] $\lambda_1, \ldots, \lambda_n$ along the diagonal, where the statement can be rewritten as follows. Letting $p_k = tr(A^k) = \lambda_1^k + \ldots + \lambda_n^k$, the following identity holds: 

\[
\prod_{i=1}^n \lambda_i = \underset{ 
     { k_1,\cdots, k_n \in \mathbb{N} }
     \atop
     { \underoverset{\ell = 1}{n}{\sum} \ell k_\ell = n }
  }{\sum}
  \underoverset{ l = 1 }{ n }{\prod} 
  \frac{ (-1)^{k_l + 1} }{ l^{k_l} k_l !  }
  p_l^{k_l}
\]

This of course is just a [[polynomial]] identity, one closely related to various of the [[Newton identities]] that concern symmetric polynomials in indeterminates $x_1, \ldots, x_n$. Thus we again let $p_k = x_1^k + \ldots + x_n^k$, and define the [[elementary symmetric polynomials]] $\sigma_k = \sigma_k(x_1, \ldots, x_n)$ via the generating function identity 

\[
\sum_{k \geq 0} \sigma_k t^k = \prod_{i=1}^n (1 + x_i t). 
\]

Then we compute 

\[\array{
\sum_{k \geq 0} \sigma_k t^k & = & \prod_{i=1}^n (1 + x_i t) \\
 & = & \exp\left(\sum_{i=1}^n \log(1 + x_i t)\right) \\ 
 & = & \exp\left(\sum_{i=1}^n \sum_{k \geq 1} (-1)^{k+1} \frac{x_i^k}{k} t^k \right)\\ 
 & = & \exp\left( \sum_{k \geq 1} (-1)^{k+1} \frac{p_k}{k} t^k\right)
}\] 

and simply match coefficients of $t^n$ in the initial and final series expansions, where we easily compute 

\[
x_1 x_2 \ldots x_n = \sum_{n = k_1 + 2k_2 + \ldots + n k_n} \prod_{l=1}^n \frac1{(k_l)!} \left(\frac{p_l}{l}\right)^{k_l} (-1)^{k_l+1}
\] 

This completes the proof. 
=-- 

## In terms of Berezinian integrals

see [[Pfaffian]] for the moment

## Related entries


* [[matrix]], [[linear algebra]], [[exterior algebra]], [[characteristic polynomial]]

* [[principal submatrix]]

* [[quasideterminant]], [[Berezinian]],[[Jacobian]], [[Pfaffian]], [[hafnian]],  [[Wronskian]]

* [[Dieudonné determinant]]

* [[resultant]], [[discriminant]], [[hyperdeterminant]]

* [[functional determinant]]

* [[determinant line]], [[determinant line bundle]], [[Pfaffian line bundle]]

* [[density bundle]]

* [[pseudoscalar]]

## References

See also

* Wikipedia, _[Determinant](https://en.wikipedia.org/wiki/Determinant)_

One derivation of the formula (eq:DeterminantAsPolynomialInTracesOfPowers) for the determinant as a polynomial in traces of powers is spelled out in appendix B of 

* {#KondratyukKrivoruchenko92} L. A. Kondratyuk, I. Krivoruchenko, _Superconducting quark matter in $SU(2)$ colour group_, Zeitschrift für Physik A Hadrons and Nuclei March 1992, Volume 344, Issue 1, pp 99–115 ([doi:10.1007/BF01291027](https://doi.org/10.1007/BF01291027))



[[!redirects determinants]]

[[!redirects Cramer's rule]]
[[!redirects Cramer's rules]]

