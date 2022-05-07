
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}


## Statement

If $A$ is an $n \times n$ [[square matrix]], then the [[determinant]] of its [[exponential]] equals the [[exponential]] of its [[trace]] 

$$
  \det\big(\exp(A)\big) 
    \;=\; 
  \exp\big(tr(A)\big)
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
  \,.
\] 

This completes the proof. 

=-- 

## Related concepts

* [[determinant]], [[trace]]

* [[characteristic form]]

## References

The proof of (eq:DeterminantAsPolynomialInTracesOfPowers) is spelled out in 

* {#KondratyukKrivoruchenko92} L. A. Kondratyuk, I. Krivoruchenko, Appendix B of:  _Superconducting quark matter in $SU(2)$ colour group_, Zeitschrift für Physik A Hadrons and Nuclei March 1992, Volume 344, Issue 1, pp 99–115 ([doi:10.1007/BF01291027](https://doi.org/10.1007/BF01291027))

[[!redirects relation between trace and determinant]]
