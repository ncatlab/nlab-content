
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _$F$-Yang-Mills equation_ (or _$F$-YM equation_) arises from a generalization of the Yang-Mills action functional with a function, which scales the norm of the curvature form. Notable special cases include _exponential Yang-Mills connections_, _$p$-Yang-Mills connections_ and _Yang-Mills-Born-Infeld connections_ with positive and negative sign.

## $F$-Yang-Mills action functional

Let $F$ be a strictly increasing $C^2$-function with $F(0)=0$. Let:

$$
d_F
\coloneqq\sup_{t\geq 0}\frac{tF'(t)}{F(t)}.
$$

([Wei 22]({#Wei22}))

Since $F$ is a $C^2$ function, one can also consider the following constant:

$$
d_{F'}
=\sup_{t\geq 0}\frac{tF''(t)}{F'(t)}.
$$

([Baba & Shintani 23, Definition 4.8](#BabaShintani23), [Baba 23]({#Baba23}))

The _$F$-Yang-Mills action functional_ (or _$F$-YM action functional_) is given by:

$$
\operatorname{YM}_F(A)
\coloneqq\int_B F\left(
\frac{1}{2}\|F_A\|^2
\right)\mathrm{d}\vol_g.
$$

([Baba & Shintani 23, Definition 3.1](#BabaShintani23), [Baba 23]({#Baba23}))

For a flat connection $A\in\Omega^1(B,\operatorname{Ad}(E))$ (with $F_A=0$), one has $\operatorname{YM}_F(A)=F(0)\operatorname{vol}(M)$. Hence $F(0)=0$ is required to avert divergence for a non-compact manifold $B$, although this condition can also be left out as only the derivative $F'$ is of further importance.

## $F$-Yang-Mills connections and equation

A connection $A\in\Omega^1(B,\operatorname{Ad}(E))$ is called _$F$-Yang-Mills connection_ if it is a critical point of the $F$-Yang–Mills action functional, hence if:

$$
\frac{\mathrm{d}}{\mathrm{d}t}\operatorname{YM}_F(A(t))\vert_{t=0}
=0
$$

for all smooth families $A\colon(-\varepsilon,\varepsilon)\rightarrow\Omega^1(B,\operatorname{Ad}(E))$ with $A(0)=A$. This is the case iff the _$F$-Yang–Mills equation_ (or _$F$-YM equation_) is fulfilled:

$$
\mathrm{d}_A\star\left(
F'\left(
\frac{1}{2}\|F_A\|^2
\right)F_A
\right)
=0.
$$

([Baba & Shintani 23, Corollary 3.4](#BabaShintani23), [Baba 23]({#Baba23}))

For a $F$-Yang-Mills connection $A\in\Omega^1(B,\operatorname{Ad}(E))$, its curvature $F_A\in\Omega^2(B,\operatorname{Ad}(E))$ is called _$F$-Yang-Mills field_ (or _$F$-YM field_).

A $F$-Yang–Mills connection/field with:

* $F(t)=\exp(t)$ (or $F(t)=\exp(t)-1$ for normalization) is called _(normed) exponential Yang–Mills connection/field_. In this case, one has $d_{F'}=\infty$. The exponential and normed exponential Yang-Mills action functional are denoted with $\operatorname{YM}_\mathrm{e}$ and $\operatorname{YM}_\mathrm{e}^0$ respectively. ([Matsura & Urakawa 95]({#MatsuraUrakawa95}))

* $F(t)=\frac{1}{p}(2t)^{\frac{p}{2}}$ is called _$p$-Yang–Mills connection/field_. Usual Yang–Mills connections/fields are exactly the $2$-Yang–Mills connections/fields. In this case, one has $d_{F'}=\frac{p}{2}-1$.  The $p$-Yang-Mills action functional is denoted with $\operatorname{YM}_p$.

* $F(t)=\sqrt{1-2t}-1$ or $F(t)=\sqrt{1+2t}-1$ is called _Yang–Mills–Born–Infeld connection/field_ (or _YMBI connection/field_) with negative or positive sign respectively. In these cases, one has $d_{F'}=\infty$ and $d_{F'}=0$ respectively. The Yang-Mills-Born-Infeld action functionals with negative and positive sign are denoted with $\operatorname{YMBI}^-$ and $\operatorname{YMBI}^+$ respectively.

([Baba & Shintani 23, Example 3.2](#BabaShintani23), [Wei 22]({#Wei22}), [Baba 23]({#Baba23}))

## Stable $F$-Yang-Mills connections

Analogous to (weakly) stable Yang-Mills connections and (weakly) stable Yang-Mills-Higgs connections, one can also consider the positivity of the second derivative in $F$-Yang-Mills theory. $A$ is called a _stable $F$-Yang-Mills connection_ (or _stable $F$-YM connection_), if:

$$
\frac{\mathrm{d}^2}{\mathrm{d}t^2}\operatorname{YM}_F(A(t))\vert_{t=0}
\gt 0
$$

for all smooth families $A\colon(-\varepsilon,\varepsilon)\rightarrow\Omega^1(B,\operatorname{Ad}(E))$ with $A(t)=A$. It is called _weakly stable_ if only $\geq 0$ holds. A $F$-Yang–Mills connection, which is not weakly stable, is called _unstable_. If $A\in\Omega^1(B,\operatorname{Ad}(E))$ is a _(weakly) stable_ or _unstable $F$-Yang-Mills connection_, its curvature $F_A\in\Omega^2(B,\operatorname{Ad}(E))$ is also called _(weakly) stable_ or _unstable $F$-Yang-Mills field_.

([Baba & Shintani 23, Definition 3.6](#BabaShintani23), [Baba 23]({#Baba23}))

## Properties

\begin{lemma}
For a Yang-Mills connection with constant curvature, its stability as Yang-Mills connection implies its stability as exponential Yang-Mills connection.
\end{lemma}

([Matsura & Urakawa 95, Corollary 6.2]({#MatsuraUrakawa95}))

\begin{lemma}
Every non-flat exponential Yang-Mills connection over $S^n$ with $n\geq 5$ and:
$$
\|F_A\|
\leq\sqrt{\frac{n-4}{2}}
$$
is flat.
\end{lemma}

([Baba & Shintani 23, Proposition 4.14](#BabaShintani23), [Baba 23]({#Baba23}))

\begin{lemma}
Every non-flat Yang-Mills-Born-Infeld connection over $S^n$ with $n\geq 5$ and:
$$
\|F_A\|
\leq\sqrt{\frac{n-4}{n-2}}
$$
is flat.
\end{lemma}

([Baba & Shintani 23, Proposition 4.13](#BabaShintani23))

\begin{theorem}
For $n\gt 4(d_{F'}+1)$, every non-flat $F$-Yang-Mills connection over $S^n$ is unstable.
\end{theorem}

([Baba & Shintani 23, Theorem 1.2 and Corollary 4.12](#BabaShintani23), [Baba 23]({#Baba23}), [Baba 23]({#Baba23}))

\begin{lemma}
For $n\gt 2p$, every non-flat $p$-Yang-Mills connection over $S^n$ is unstable.
\end{lemma}
\begin{lemma}
For $n\gt 4$, every non-flat Yang-Mills-Born-Infeld connection with positive sign over $S^n$ is unstable.
\end{lemma}
\begin{lemma}
For $0\leq d_{F'}\leq\frac{1}{6}$, every non-flat $F$-Yang-Mills connection over the [[Cayley plane]] $F_4/\operatorname{Spin}(9)$ is instable.
\end{lemma}

([Baba 23]({#Baba23}))

## Related concepts

* [[Bi-Yang-Mills equation]]

## References

* {#MatsuraUrakawa95} Fumiaki Matsura, Hajime Urakawa, _On exponential Yang-Mills connections_ (1995), [DOI:10.1016/0393-0440(94)00041-2](https://doi.org/10.1016/0393-0440(94)00041-2)

* {#Wei22} Shihshu Walter Wei, _On exponential Yang-Mills fields and p-Yang-Mills fields_ (2022), [arXiv:2205.03016](https://arxiv.org/abs/2205.03016)

* {#BabaShintani23} Kurando Baba, Kazuto Shintani, _A Simons type condition for instability of F-Yang-Mills connections_ (2023), [arXiv:2301.04291](https://arxiv.org/abs/2301.04291)

* {#Baba23} Kurando Baba, _On instability of F-Yang-Mills connections
_ (2023), [Slides](https://www.rs.tus.ac.jp/kurando.baba/conference/record/2023/2023slide-baba.pdf)

See also:

* Wikipedia, _[F-Yang-Mills equations](https://en.wikipedia.org/wiki/F-Yang%E2%80%93Mills_equations)_

[[!redirects F-Yang-Mills equation]]
[[!redirects F-Yang-Mills connection]]
[[!redirects F-Yang-Mills connections]]
[[!redirects F-Yang-Mills field]]
[[!redirects F-Yang-Mills fields]]
[[!redirects F-YM equation]]
[[!redirects F-YM equations]]
[[!redirects F-YM connection]]
[[!redirects F-YM connections]]
[[!redirects F-YM field]]
[[!redirects F-YM fields]]

[[!redirects Yang-Mills-Born-Infeld equation]]
[[!redirects Yang-Mills-Born-Infeld equations]]
[[!redirects Yang-Mills-Born-Infeld connection]]
[[!redirects Yang-Mills-Born-Infeld connections]]
[[!redirects Yang-Mills-Born-Infeld field]]
[[!redirects Yang-Mills-Born-Infeld fields]]
[[!redirects YMBI equation]]
[[!redirects YMBI equations]]
[[!redirects YMBI connection]]
[[!redirects YMBI connections]]
[[!redirects YMBI field]]
[[!redirects YMBI fields]]

[[!redirects p-Yang-Mills equation]]
[[!redirects p-Yang-Mills equations]]
[[!redirects p-Yang-Mills connection]]
[[!redirects p-Yang-Mills connections]]
[[!redirects p-Yang-Mills field]]
[[!redirects p-Yang-Mills fields]]
[[!redirects p-YM equation]]
[[!redirects p-YM equations]]
[[!redirects p-YM connection]]
[[!redirects p-YM connections]]
[[!redirects p-YM field]]
[[!redirects p-YM fields]]

[[!redirects exponential Yang-Mills equation]]
[[!redirects exponential Yang-Mills equations]]
[[!redirects exponential Yang-Mills connection]]
[[!redirects exponential Yang-Mills connections]]
[[!redirects exponential Yang-Mills field]]
[[!redirects exponential Yang-Mills fields]]
[[!redirects exponential YM equation]]
[[!redirects exponential YM equations]]
[[!redirects exponential YM connection]]
[[!redirects exponential YM connections]]
[[!redirects exponential YM field]]
[[!redirects exponential YM fields]]
