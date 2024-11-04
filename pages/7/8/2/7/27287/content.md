
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

The _Bi-Yang-Mills equations_ (or _Bi-YM equations_) arise from a generalization of the Yang-Mills action functional, so that the curvature is replaced by its adjoint derivative. While a vanishing curvature gives a flat connection, its vanishing adjoint derivative gives a Yang-Mills connection. Hence by switching to local extrema, Bi-Yang-Mills connections are to Yang-Mills connections what these are to flat connections.

## Bi-Yang-Mills action functional

The _Bi-Yang-Mills action functional_ (or _Bi-YM action functional_) is given by:

$$
\operatorname{BiYM}_F(A)
\coloneqq\int_B\|\delta_A F_A\|^2\mathrm{d}\vol_g.
$$

([Chiang 13, Eq. (9)](#Chiang13))

## Bi-Yang-Mills connections and equation

A connection $A\in\Omega^1(B,\operatorname{Ad}(E))$ is called _Bi-Yang-Mills connection_ (or _Bi-YM connection_) it it is a critical point of the Bi-Yang-Mills action functional, hence if:

$$
\frac{\mathrm{d}}{\mathrm{d}t}\operatorname{BiYM}(A(t))\vert_{t=0}
=0
$$

for all smooth families $A\colon(-\varepsilon,\varepsilon)\rightarrow\Omega^1(B,\operatorname{Ad}(E))$ with $A(0)=A$.

([Chiang 13, Eq. (5.1) and (6.1)](#Chiang13))

This is the case iff the _Bi-Yang-Mills equation_ (or _Bi-YM equation_) is fulfilled:

$$
(\delta_A\mathrm{d}_A+\mathcal{R}_A)(\delta_A F_A)
=0.
$$

([Chiang 13, Eq. (10), (5.2) and (6.3)](#Chiang13))

For a Bi-Yang-Mills connection $A\in\Omega^1(B,\operatorname{Ad}(E))$, its curvature $F_A\in\Omega^2(B,\operatorname{Ad}(E))$ is called _Bi-Yang-Mills field_ (or _Bi-YM field_).

## Stable Bi-Yang-Mills connections

Analogous to (weakly) stable Yang-Mills connections and (weakly) stable Yang-Mills-Higgs connections, one can also consider the positivity of the second derivative in Bi-Yang-Mills theory. $A$ is called a _stable Bi-Yang-Mills connection_ (or _stable Bi-YM connection_), if:

$$
\frac{\mathrm{d}^2}{\mathrm{d}t^2}\operatorname{BiYM}(A(t))\vert_{t=0}
\gt 0
$$

for all smooth families $A\colon(-\varepsilon,\varepsilon)\rightarrow\Omega^1(B,\operatorname{Ad}(E))$ with $A(0)=A$. It is called _weakly stable_ if only $\geq 0$ holds. A Bi-Yang–Mills connection, which is not weakly stable, is called _unstable_. If $A\in\Omega^1(B,\operatorname{Ad}(E))$ is a _(weakly) stable_ or _unstable Bi-Yang-Mills connection_, its curvature $F_A\in\Omega^2(B,\operatorname{Ad}(E))$ is also called _(weakly) stable_ or _unstable Bi-Yang-Mills field_.

([Chiang 13, Definition 6.3.2](#Chiang13))

## Property

\begin{lemma}
Yang-Mills connections are weakly Bi-Yang-Mills connections.
\end{lemma}

([Chiang 13, Proposition 6.3.3](#Chiang13))

## Related concepts

* [[F-Yang-Mills equation]]

## References

* {#Chiang13} Yuan-Jen Chiang, _Developments of Harmonic Maps, Wave Maps and Yang-Mills Fields into Biharmonic Maps, Biwave Maps and Bi-Yang-Mills Fields_, [ISBN 978-3034805339](https://link.springer.com/book/10.1007/978-3-0348-0534-6)

See also:

* Wikipedia, _[Bi-Yang-Mills equations](https://en.wikipedia.org/wiki/Bi-Yang%E2%80%93Mills_equations)_

[[!redirects Bi-Yang-Mills equation]]
[[!redirects Bi-Yang-Mills connection]]
[[!redirects Bi-Yang-Mills connections]]
[[!redirects Bi-Yang-Mills field]]
[[!redirects Bi-Yang-Mills fields]]
[[!redirects Bi-YM equation]]
[[!redirects Bi-YM equations]]
[[!redirects Bi-YM connection]]
[[!redirects Bi-YM connections]]
[[!redirects Bi-YM field]]
[[!redirects Bi-YM fields]]