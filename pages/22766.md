
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Statement

The following is known as the *[[Carl Gauss|Gauss]] multiplication formula* or the *[[Legendre]] relation*:

\begin{prop}\label{GaussMultiplicationFormula}

For 

* a [[positive number|positive]] [[integer]] $N \in \mathbb{N}_+$,

* any $z \in \mathbb{R} \setminus  \{0, -1/N, -2/N, \cdots\} $,

the [[Gamma function]] $\Gamma(-)$ satisfies 

\[
  \underoverset
    {j = 0}
    {N-1}
    {\prod}
  \Gamma
  \left(
    z + \tfrac{j}{N}
  \right)
  \;=\;
  (2 \pi)^{ \tfrac{1}{2}(N-1) } 
  \cdot
  N^{ (\tfrac{1}{2} - N z) }
  \cdot
  \Gamma( N z )
  \,.
\]

\end{prop}

\begin{example}
In the special case of $N = 2$ this is known as the *duplication formula*:

$$
  \Gamma(z)
  \cdot
  \Gamma
  \big(
    z + 1/2
  \big)
  \;=\;
  (2\pi)^{1/2}
  \cdot
  2^{1/2 - 2z}
  \cdot
  \Gamma(2 z)
  \,.
$$
\end{example}

\begin{remark}
  A related expression gives a product of [[Barnes G-functions]] (see [there](Barnes+G-function#MultiplicationFormulaForGammaFunctionInTermsOfGFunction)):
$$
  \underoverset
    {j = 1}
    {N}
    {\prod}
  \Gamma(j/2)
  \;=\;
  \frac
    {
      G(N/2+ 1)
      \cdot
      G(N/2 + 1/2)
    }
    { G(1/2) }
  \,.
$$
\end{remark}

## References

* J. Sándor and L. Tóth, *A remark on the gamma function*, Elem. Math. 44 (3), pp. 73–76 (1989) ([dml:141455](https://eudml.org/doc/141455))

See also:

* Wikipedia, *[Multiplication theorem](https://en.wikipedia.org/wiki/Multiplication_theorem)*

* ProofWiki, *[Gauss Multiplication Formula](https://proofwiki.org/wiki/Gauss_Multiplication_Formula)*

* DLMF, *[Gamma function §5.5(iii) Multiplication](https://dlmf.nist.gov/5.5#iii)*

* Wolfram MathWorld, *[Gauss multiplication formula](https://mathworld.wolfram.com/GaussMultiplicationFormula.html)*

* Wolfram MathWorld, *[Legendre Duplication formula](https://mathworld.wolfram.com/LegendreDuplicationFormula.html)*

[[!redirects Legendre relation]]


[[!redirects multiplication theorem]]

[[!redirects duplication formula]]
[[!redirects Legendre duplication formula]]
