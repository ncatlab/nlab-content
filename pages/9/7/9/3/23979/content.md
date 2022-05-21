+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition ##

There are multiple definitions of a Bézout ring:

\begin{definition}
A [[commutative ring]] $R$ is a **Bézout ring** if for every element $a \in R$ and $b \in R$, there exists elements $x \in R$, $y \in R$ called **Bézout coefficients** and $g \in R$ called a **common divisor**, such that $a \cdot x + b \cdot y = g$, $g \vert a$ and $g \vert b$.
\end{definition}

\begin{definition}
A [[commutative ring]] $R$ is a **Bézout ring** if it has functions $\beta_0:R \times R \to R$, $\beta_1:R \times R \to R$, $\gamma:R \times R \to R$ such that for every element $a \in R$ and $b \in R$, $a \cdot \beta_0(a, b) + b \cdot \beta_1(a, b) = \gamma(a, b)$, $\gamma(a, b) \vert a$ and $\gamma(a, b) \vert b$. 
\end{definition}

\begin{definition}
A [[commutative ring]] $R$ is a **Bézout ring** if every ideal with 2 generators is a [[principal ideal]]: 
\end{definition}

\begin{definition}
A [[commutative ring]] $R$ is a **Bézout ring** if every finitely generated ideal is a [[principal ideal]]. 
\end{definition}

If the commutative ring is a [[GCD ring]] and the common divisor is the [[greatest common divisor]], then the Bézout ring condition $a \cdot \beta_0(a, b) + b \cdot \beta_1(a, b) = \gcd(a, b)$ is called the **Bézout identity**. There might be multiple Bézout coefficient functions for each Bézout ring. 

## See also ##

* [[commutative ring]]

* [[GCD ring]]

* [[Bézout domain]]

* [[Euclidean ring]]

## References

* [[Henri Lombardi]], [[Claude Quitté]] (2010): *Commutative algebra: Constructive methods (Finite projective modules)* Translated by Tania K. Roblo, Springer (2015) ([doi:10.1007/978-94-017-9944-7](https://link.springer.com/book/10.1007/978-94-017-9944-7), [pdf](http://hlombardi.free.fr/CACM.pdf))

* Wikipedia, _[Bézout's identity](http://en.wikipedia.org/wiki/Bézout's_identity)

[[!redirects Bézout rings]]

[[!redirects Bezout ring]]
[[!redirects Bezout rings]]

[[!redirects Bézout's identity]]
[[!redirects Bezout's identity]]

[[!redirects Bézout coefficient]]
[[!redirects Bézout coefficients]]
[[!redirects Bezout coefficient]]
[[!redirects Bezout coefficients]]