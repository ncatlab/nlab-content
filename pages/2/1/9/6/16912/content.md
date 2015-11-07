
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
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

## Definition

The construction that sends a [[smooth manifold]] $X$ to the [[algebraic K-theory]] [[spectrum]] $K(C^\infty(X,\mathbb{C}))$ of its [[ring]] of [[smooth functions]] (with values in the [[complex numbers]]) presents (after [[infinity-stackification]]) a [[sheaf of spectra]] on the [[site]] of [[smooth manifolds]], hence a [[smooth spectrum]]

$$
  \mathbf{K} \in Stab(Smooth\infty Grpd) \simeq T_\ast Smooth \infty Grpd
  \,,
$$

i.e. an object of the [[tangent cohesive (∞,1)-topos]] of [[Smooth∞Grpd]]. (See also [this definition](differential+cohomology+diagram#KTheoryOfStackOfVectorBundles) at _[[differential cohomology hexagon]]_.)

## Properties

### Shape and relation to topological K-theory

The [[shape modality|shape]] of this $\mathbf{K}$ is the [[topological K-theory]] spectrum $ku$ ([Bunke-Nikolaus-Voelkl 13, lemma 6.3](#BNV13), [Bunke 14, (48) with def. 2.21](#Bunke14)):

$$
  &#643; \mathbf{K} \simeq ku
  \,.
$$

Hence $\mathbf{K}$ is a [[differential cohomology]] refinement of $ku$, a form of [[differential K-theory]].

### Regulator and relation to differential K-theory
 {#Regulator}

There is also the more standard [[differential K-theory]] refinement $\mathbf{ku}_{conn}$ of $ku$ ([[Quadratic Functions in Geometry, Topology, and M-Theory|Hopkins-Singer 05]], [Bunke-Nikolaus-Voelkl 13](differential+K-theory#BunkeNikolausVoelkl13)) which is obtained by pulling back suitable sheaves of ($\mathbb{C}$-valued) [[differential forms]] $\mathbf{DD}^-$ along the usual  [[Chern character map]] $ch \colon ku \longrightarrow DD^{per}$. This Chern character lifts through the [[shape modality]] to a [[regulator]] map ([Bunke 14, (50)](#Bunke14))

$$
  \array{
    \mathbf{K} &\stackrel{\mathbf{reg}}{\longrightarrow}& \mathbf{DD}^-
    \\
    \downarrow^{\mathrlap{\eta^{&#643;}}} && \downarrow^{\mathrlap{\eta^{&#643;}}}
    \\
    ku &\stackrel{ch}{\longrightarrow}& DD^{per}
  }
$$

Moreover, this induces a differential [[regulator]] ([BNV 13, p.40 and example 6.9](#BNV13), [Bunke 14, def. 2.29](#Bunke14)):

$$
  \mathbf{reg}_{conn} \;\colon\; \mathbf{K} \longrightarrow \mathbf{ku}_{conn}
  \,.
$$

See also [this proposition](differential+cohomology+diagram#SmoothRegulator) at _[[differential cohomology diagram]]_.

### Moduli stacks

In ([Bunke 14](#Bunke14)) all this is generalized to the [[mapping spaces]] $[X,\mathbf{K}]$ out of a [[smooth manifold]] $X$, hence to the [[moduli stacks]] (here: moduli spectra) of algebraic K-theory cocycles on $X$.

The regulator from [above](#Regulator) induces a map

$$
  [X,\mathbf{reg}_{conn}]
  \;\colon\;
  [X,\mathbf{K}]
  \longrightarrow
  [X,\mathbf{ku}_{conn}]
  \,.
$$

(...)
 
## References

* {#BNV13} [[Ulrich Bunke]], [[Thomas Nikolaus]], [[Michael Völkl]], section 6 of _Differential cohomology theories as sheaves of spectra_, Journal of Homotopy and Related Structures October 2014 ([arXiv:1311.3188](http://arxiv.org/abs/1311.3188))


* {#Bunke14} [[Ulrich Bunke]], _A regulator for smooth manifolds and an index theorem_ ([arXiv:1407.1379](http://arxiv.org/abs/1407.1379))

* [[Ulrich Bunke]], _Smooth aspects of algebraic K-theory_ ([pdf](http://www.uni-regensburg.de/Fakultaeten/nat_Fak_I/Bunke/smooth-asp.pdf))
