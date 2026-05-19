


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--



\tableofcontents

## Definition

### In differential geometry

Let $\pi \colon P \to X$ be a [[fiber bundle]] in the [[category]] [[Diff]] of [[smooth manifolds]]. 

The [[dg-algebra]] $\Omega^\bullet_{vert/X}(P)$ of _vertical differential forms_ on $P$ is the [[quotient object|quotient]] of the [[de Rham complex]] [[dg-algebra]] $\Omega^\bullet(P)$ of all [[differential forms]] on $P$, by the dg-ideal of [[horizontal differential forms]]:

$$
  \Omega^\bullet_{vert/X}\big(
    P
  \big)
  \simeq
  \Omega^\bullet\big(P\big)
  \big/
  \big\langle
    \pi^\ast \Omega^1(X)
  \big\rangle
$$


## Examples

\begin{example}
For a [[trivial fiber bundle]], $P \equiv X \times F \longrightarrow X$, the vertical differential forms are the smoothly $X$-parameterized differential forms on $F$:

$$
  \Omega^\bullet_{vert/X}\big(
    X \times F
  \big)
  \simeq
  C^\infty\big(
    X, \Omega^\bullet(F)
  \big)
  \mathrlap{\,.}
$$
\end{example}


## Related concepts

* [[horizontal differential form]]

* [[Lie integration]]

## References

* Philippe Bonnet, Alexandru Dimca, _Relative differential forms and complex polynomials_, Bulletin des Sciences Mathématiques **124** Issue 7 (2000) pp 557-571, doi:[10.1016/s0007-4497(00)01055-1](https://doi.org/10.1016/s0007-4497%2800%2901055-1), ([author pdf](https://web.archive.org/web/20150326174153/https://jones.math.unibas.ch/~bonnet/Publications/Bullscience.pdf))

[[!redirects vertical differential forms]]

