

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

\tableofcontents

## Definition

Given a [[group]] $G$ and an [[automorphism]] (or more generally an [[endomorphism]]) $\phi \colon G \xrightarrow{\;} G$, its [[set]] of [[fixed points]]

$$
  G^\phi
  \;\coloneqq\;
  \Big\{
    g \in G
    \;\Big\vert\;
    \phi(g)
    =
    g
  \Big\}
  \;\subset\;
  G
$$

evidently constitutes a [[subgroup]], called the *fixed-point subgroup* of $\phi$.

The analogous statement holds for $G$ replaced by any [[algebra|algebraic]] [[structure]]: The [[endomorphism]] property ensures that with a [[pair]] of [[elements]] being fixed by $\phi$, so is their [[binary operation|product]] $(-)\cdot(-)$ in the algebra:

$$
  \phi(g_i)
  =
  g_i
  \;\;\;\;\;
  \Rightarrow
  \;\;\;\;\;
  \phi\big(
    g_1 \cdot g_2
  \big)
  \;=\;
  \phi(g_1)
  \cdot
  \phi(g_2)
  \;=\;
  g_1 \cdot g_2
$$

## Examples

\begin{example}
  If $\phi = Ad_g$ is an [[inner automorphism]] acting by [[conjugation action|conjugation]] with an [[element]] $g \in G$, then its fixed-point subgroup $G^\phi$ is the *[[centralizer subgroup]]* $C_G(g)$.
\end{example}

## Related concepts

* [[fixed point subspace]]

## References

See also:

* Wikipedia: *[Fixed-point subgroup](https://en.wikipedia.org/wiki/Fixed-point_subgroup)*


[[!redirects fixed point group]]
[[!redirects fixed point groups]]

[[!redirects fixed-point group]]
[[!redirects fixed-point groups]]

[[!redirects fixed point subgroup]]
[[!redirects fixed point subgroups]]

[[!redirects fixed-point subgroup]]
[[!redirects fixed-point subgroups]]

[[!redirects fixed point monoid]]
[[!redirects fixed point monoids]]

[[!redirects fixed-point monoid]]
[[!redirects fixed-point monoids]]

[[!redirects fixed point submonoid]]
[[!redirects fixed point submonoids]]

[[!redirects fixed-point submonoid]]
[[!redirects fixed-point submonoids]]
