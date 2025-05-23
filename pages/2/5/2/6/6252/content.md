
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

Let $A: H\to H$  be an [[unbounded operator]] on a [[Hilbert space]] $H$. An unbounded operator $A^*$ is its __[[adjoint operator|adjoint]]__ if

* $(A x|y) = (x|A^*y)$ for all $x\in dom(A)$ and $y\in dom(A^*)$; and
* every $B$ satisfying the above property for $A^*$ is a restriction of $A$.

An adjoint does not need to exist in general. 

An unbounded operator is **symmetric** if $dom(A)\subset dom(A^*)$ and $A x = A^*x$ for all $x\in dom(A)$ (one also writes $A\subset A^*$).

The domain of $A^*$ is the set of all vectors $y\in H$ such that the linear functional
$x\mapsto (Ax|y)$ is bounded on $dom(A)$. 

The graph $\Gamma_A\subset H\oplus H$ satisfies $\Gamma_{A^*} = \tau(\Gamma_A)^\perp$ where $\perp$ denotes the [[orthogonal complement]] and $\tau$ denotes the transposition of the direct summands changing the sign of one of the factors, i.e. $x\oplus y\mapsto -y\oplus x$. An unbounded operator $A$ is __closed__ if $\Gamma_A$ is closed subspace of $H\oplus H$. An operator $B$ is a closure of an operator $A$ if $\Gamma_B$ is a closure of operator $\Gamma_A$. It is said that $B$ is an __extension__ of $A$ and one writes $B\supset A$ if $\Gamma_B\supset \Gamma_A$. The closure of an unbounded operator does not need to exist.

For any unbounded operator $A$ with a dense $dom(A)\subset H$, if the adjoint operator $A^*$ exists, then $A^*$ is closed, and if $(A^*)^*$ exists then it coincides with a closure of $A$.

An [[unbounded operator]] $A : H\to H$ on a Hilbert space $H$ is __self-adjoint__ if

* it has a densely defined domain $dom(A)\subset H$
* $A = A^*$, i.e. $dom(A^*)= dom(A)$ and $A x = A^* x$ for all $x\in dom(A)$

An (unbounded) operator is __essentially self-adjoint__ if it is symmetric and its [[spectrum]] (as a subspace of the [[complex plane]]) is contained in the [[real line]]. Alternatively, it is symmetric if its closure is self-adjoint. 

A __Hermitean__ (or __hermitian__) operator is a [[bounded operator|bounded]] symmetric operator (which is necessarily self-adjoint), although some authors use the term for any self-adjoint operator.

For a bounded operator $A: H\to K$ between Hilbert spaces, define the [[Hermitean conjugate]] operator $A^*: K\to H$ by $(Ax|y)_H = (x|A^*y)_K$, for all $x\in K$, $y\in H$. Distinguish it from the concept of the [[transposed operator]] $A^T: K^*\to H^*$ between the [[dual vector space|dual spaces]].

In an arbitrary $*$-[[star-algebra|algebra]], a __self-adjoint__ or __hermitian__ element is any element $A$ such that $A^* = A$.


## Related concepts

* [[self-adjoint extension]]

* [[unitary operator]]

* [[Hermitian form]], [[Hermitian matrix]]

* [[quantum observable]], [[daseinisation]]

* [[positive operator]]


## References

Original articles:

* {#vonNeumann30} [[John von Neumann]], §I in: *Allgemeine Eigenwerttheorie Hermitescher Funktionaloperatoren*, Math. Ann. **102** (1930) 49–131 &lbrack;[doi:10.1007/BF01782338](https://doi.org/10.1007/BF01782338)&rbrack;

See also:

* A. A. Kirillov, A. D. Gvi&#353;iani, &#1058;&#1077;&#1086;&#1088;&#1077;&#1084;&#1099; &#1080; &#1079;&#1072;&#1076;&#1072;&#1095;&#1080; &#1092;&#1091;&#1085;&#1082;&#1094;&#1080;&#1086;&#1085;&#1072;&#1083;&#1100;&#1085;&#1086;&#1075;&#1086; &#1072;&#1085;&#1072;&#1083;&#1080;&#1079;&#1072; (theorems and exercises in functional analysis), Moskva, Nauka 1979, 1988

* A. B. Antonevi&#269;, Ja. B. Radyno, Funkcional'nij analiz i integral'nye uravnenija, Minsk 1984

* S. Kurepa, _Funkcionalna analiza, elementi teorije operatora_, &#352;kolska knjiga, Zagreb 1981. 

* Reed, M.; Simon, B.: _Methods of modern mathematical physics_. Volume 1, Functional Analysis 

* Walter Rudin, _Functional analysis_

* Konrad Schmuedgen, _Unbounded self-adjoint operators on Hilbert space_, Springer GTM 265

[[!redirects self-adjoint]]
[[!redirects selfadjoint]]

[[!redirects self-adjoint element]]
[[!redirects self-adjoint elements]]
[[!redirects selfadjoint element]]
[[!redirects selfadjoint elements]]


[[!redirects self-adjoint operator]]
[[!redirects self-adjoint operators]]
[[!redirects selfadjoint operator]]
[[!redirects selfadjoint operators]]
[[!redirects self adjoint operator]]
[[!redirects self adjoint operators]]

[[!redirects essentially selfadjoint operator]]
[[!redirects essentially selfadjoint operators]]
[[!redirects essentially self-adjoint operator]]
[[!redirects essentially self-adjoint operators]]
[[!redirects essentially self adjoint operator]]
[[!redirects essentially self adjoint operators]]

[[!redirects Hermitian operator]]
[[!redirects Hermitian operators]]
[[!redirects Hermitean operator]]
[[!redirects Hermitean operators]]
[[!redirects hermitian operator]]
[[!redirects hermitian operators]]
[[!redirects hermitean operator]]
[[!redirects hermitean operators]]

[[!redirects symmetric operator]]
[[!redirects symmetric operators]]
