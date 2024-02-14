
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

The topological complexity is a [[topological invariant]] connected to the problem of motion planning and the [[immersion]] problem of [[real projective space]]. It was introduced by [[Michael Farber]] in 2001.

## Definition

For a [[topological space]] $X$ its _topological complexity_ $TC(X)$ is the smallest number $n$, so that there is an [[open cover]] $(U_k)_{k=1}^n$ of $n$ [[open subsets]] of $X\times X$ with local sections $s_k\colon X\times X\rightarrow PX$ of the evaluation map $PX\rightarrow X\times X,\gamma\mapsto(\gamma(0),\gamma(1))$ of the [[path space]] $PX$. It is also possible to define it using the [[Schwarz genus]] of the path space fibration $\Omega X\hookrightarrow PX\rightarrow X$.

There is also the convention of using the smallest number $n$, so that an [[open cover]] $(U_k)_{k=0}^n$ of $n+1$ [[open sets]] of $X\times X$ with the above property exists. This lowers all topological complexities by one, hence the convention used can be given by giving the topological complexity of the set with one point. ($TC(*)=1$ for the upper convention and $TC(*)=0$ for the lower convention.)

## Properties

\begin{proposition}
A [[topological space]] $X$ is [[contractible]] iff $TC(X)=1$.
\end{proposition}

([Farber 01, Theorem 1](#Farber01))

\begin{proposition}
The [[topological complexity]] is only dependent on the [[homotopy type]] of a [[topological space]].
\end{proposition}

([Farber 01, Theorem 3](#Farber01))

## Special topological complexities

### Spheres and tori

\begin{proposition}
The [[topological complexity]] of a [[sphere]] is
\[
  \label{TopologicalComplexityOfSpheres}
    TC
    \big(
      S^n
    \big)
    \;=\;
    \left\{
    \begin{array}{ll}
       2 & n \; odd
       \\
       3 & n \; even
    \end{array}
    \right.
\]
(with convention $\operatorname{TC}(*)=1$)
\end{proposition}

([Farber 01, Theorem 8](#Farber01))

This theorem can be generalized:

\begin{proposition}
The [[topological complexity]] of a product of spheres is
\[
  \label{TopologicalComplexityOfProductOfSpheres}
    TC
    \big(
      (S^m)^n
    \big)
    \;=\;
    \left\{
    \begin{array}{ll}
       n+1 & m \; odd
       \\
       2n+1 & m \; even
    \end{array}
    \right.
\]
(with convention $\operatorname{TC}(*)=1$).
\end{proposition}

([Farber 01, Theorem 13](#Farber01))

A special case of this proposition is $TC(T^n)=n+1$ for the [[topological complexity]] of the [[torus]].

### Real and complex projective space

\begin{proposition}
For $n\neq 1,3,7$, the smallest [[natural number]] $k\in\mathbb{N}$, so that there exists an [[immersion]] of [[real projective space]] $\mathbb{R}P^n$ into [[euclidean space]] $\mathbb{R}^{k-1}$ is the topologial complexity $\operatorname{TC}(\mathbb{R}P^n)$ (with convention $\operatorname{TC}(*)=1$).
\end{proposition}

([Farber & Tabachnikov & Yuzvinsky 02,  Theorem 12](#FarberTabachnikovYuzvinsky02))

\begin{proposition}
For $n=1,3,7$, one has $\operatorname{TC}(\mathbb{R}P^n)=n+1$ (with convention $\operatorname{TC}(*)=1$).
\end{proposition}

([Farber & Tabachnikov & Yuzvinsky 02,  Proposition 18](#FarberTabachnikovYuzvinsky02))

\begin{proposition}
For any $n\in\mathbb{N}$, one has $\operatorname{TC}(\mathbb{C}P^n)=2n+1$ (with convention $\operatorname{TC}(*)=1$).
\end{proposition}

([Farber & Tabachnikov & Yuzvinsky 02,  Corollary 2](#FarberTabachnikovYuzvinsky02))

### $\Sigma$ and $\Xi$ surfaces

\begin{proposition}
The [[topological complexity]] of a $\Sigma$ surface is
\[
  \label{TopologicalComplexityOfSigmaSurface}
    TC
    \big(
      \Sigma_g
    \big)
    \;=\;
    \left\{
    \begin{array}{ll}
       3 & m \leq 1
       \\
       5 & m \gt 1
    \end{array}
    \right.
\]
(with convention $TC(*)=1$)
\end{proposition}

([Farber 01, Theorem 9](#Farber01))

\begin{proposition}
For $n \geq 2$ and $g \geq 2$ one has
\[
  \label{TopologicalComplexityOfConnectedSumOfRealProjectiveSpace}
    TC
    \big(
      (\mathbb{R}P^n)^g
    \big)
    \;=\;
    2n
\]
for the [[connected sum]] of [[real projective space]] (with convention $TC(*)=0$).
\end{proposition}

([Cohen & Vandembrouq 18, Theorem 1.3.](#CohenVandembroucq18)) 

### Klein bottle

\begin{proposition}
The topological complexity of the [[Klein bottle]] is $4$ (with convention $TC(*)=0$).
\end{proposition}

([Cohen & Vandembrouq 16, Theorem 1](#CohenVandembroucq16))

## Configuration space

\begin{proposition} The topological complexity of a [[configuration space]] is
\[
  \label{TopologicalComplexityOfConfigurationSpace}
    TC
    \big(
      Conf(\mathbb{R}^m,n)
    \big)
    \;=\;
    \left\{
    \begin{array}{ll}
       2n-1 & m \; odd
       \\
       2n-2 & m \; even
    \end{array}
    \right.
\]
(with convention $TC(*)=1$).
\end{proposition}

([Farber & Grant 08, Theorem 1](#FarberGrant08))

## References

See also:

* Wikipedia, [topological complexity](https://en.wikipedia.org/wiki/Topological_complexity)

Definition and basic properties of topological complexity:

* {#Farber01} [[Michael Farber]], _Topological complexity of motion planning_ (2001), [arXiv:math/0111197](https://arxiv.org/abs/math/0111197);

On topological complexity of [[real projective space]] and connection with their [[immersion]] into [[cartesian space]]:

* {#FarberTabachnikovYuzvinsky02} [[Michael Farber]], [[Serge Tabachnikov]], [[Sergey Yuzvinsky]], _Topological robotics: motion planning in projective spaces_ (2002), [arXiv:math/0210018](https://arxiv.org/abs/math/0210018);

On topological complexity of [[connected sums]]:

* {#CohenVandembroucq18} [[Daniel C. Cohen]], [[Lucile Vandembroucq]], _Motion planning in connected sums of real projective spaces_ (2018), [arXiv:1807.09947](https://arxiv.org/abs/1807.09947)

On topological complexity of the [[Klein bottle]]:

* {#CohenVandembroucq16} [[Daniel C. Cohen]], [[Lucile Vandembroucq]], _Topological Complexity of the Klein bottle_ (2018), [arXiv:1612.03133v3](https://arxiv.org/abs/1612.03133v3)

On topological complexity of [[configuration space]]:

* {#FarberGrant08} [[Michael Farber]], [[Mark Grant]], _Topological Complexity of the Klein bottle_ (2008), [arXiv:0806.4111](https://arxiv.org/pdf/0806.4111.pdf)