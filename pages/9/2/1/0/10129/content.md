
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[ordinary homology]]/[[ordinary cohomology]] represented as [[singular homology]]/[[singular cohomology]], then the _cap product_ operation over a [[topological space]] $X$ is the pairing

$$ 
  H^p(X)\otimes H_{p+q}(X) \longrightarrow H_q(X)
$$

given by combining the [[Kronecker pairing]] of the cohomology class with the image of the homology class under [[diagonal]] and using the [Eilenberg-Zilber theorem](Eilenberg-Zilber+theorem#ProdTopSp).

More generally, in [[relative cohomology|relative]] [[generalized (Eilenberg-Steenrod) cohomology]]/[[generalized homology]] represented by a [[ring spectrum]] $E$, then the cap product

$$
  E^p(X,A) \otimes E_{(p+q)}(X, A) \longrightarrow E_q(X)
$$

is given on representatives $(\alpha,\beta)$

$$
  [X/A \overset{\alpha}{\longrightarrow} \Sigma^{p} E]
  \,,
  \;\;\;  
  [S^{p+q} \overset{\beta}{\to} E \wedge X/A]
$$

(where $X/A$ denotes the [[homotopy cofiber]]/[[mapping cone]] by a map $A \to X$) by the element represented by the composite

$$
  S^{p+q}
   \overset{\beta}{\longrightarrow}
  E \wedge X/A
   \overset{id \wedge \Delta}{\longrightarrow}
  E \wedge X/A \wedge X
   \overset{id \wedge \alpha \wedge id}{\longrightarrow}
  E \wedge \Sigma^p E \wedge X
    \overset{\mu \wedge id}{\longrightarrow}
  \Sigma^p E \wedge X
$$

([e.g. Kochman 96, p. 136](#Kochman96))

This pairing induces a corresponding pairing on [[Atiyah-Hirzebruch spectral sequences]] (in the manner discussed at [[multiplicative cohomology theory]]/[[multiplicative spectral sequence]]), such that on the second page it restricts to the cap prodct in ordinary cohomology.

([e.g. Kochman 96, p. 138](#Kochman96))


## Related concepts

* [[cup product]]

* [[intersection pairing]]

* [[Poincaré duality]]

* [[fundamental class]]

## References

* {#Kochman96} [[Stanley Kochman]], (4.2.1) and prop. 4.2.10 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996


[[!redirects cap products]]


