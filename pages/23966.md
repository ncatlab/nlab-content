

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The central [[theorem]] in [[persistent homology]] states how the data retained in [[persistence diagrams]]/[[barcodes]] is stable under small deformations of the initial data.

Specifically, the original form of the stability theorem ([Cohen, Steiner, Edelsbrunner & Harer 2007](#CohenSteinerEdelsbrunnerHarer07)) applies to [[persistence modules]] $V(f)_\bullet$ given by the [[connected components]] of the [[level set|sub-level]] sets of a [[continuous function]] $X \xrightarrow{f} \mathbb{R}$ on some data set $X$

$$
  V(f)_l 
    \;\coloneqq\; 
  H_0\Big(  f^{-1}\big( (-\infty, l] \big) \Big)
$$

(equipped with the evident inclusions) and states that as the function $f$ is deformed to another continuous function $g$, the [[bottleneck distance]] $d_B$ 
([CSEH07, p. 3](#CohenSteinerEdelsbrunnerHarer07)) 

$$
  d_B
  \big( 
    X
    ,\,
    Y
  \big)
  \;\coloneqq\;
  \underset{
    X \underoverset{\sim}{\gamma}{\to} Y
  }{inf}
  \;\;
  \underset{x \in X}{sup}
  \;
  \Vert
    x - \gamma(x)
  \Vert_\infty
$$

between the corresponding [[persistence diagrams]] $PDgr\big( V(f)_\bullet \big)$  is bounded by the [[supremum norm]] of the difference between the two functions:

$$
  d_B
  \Big(
    PDgr\big( V(f)_\bullet \big)
    ,\,
    PDgr\big( V(f)_\bullet \big)
  \Big)
  \;\leq\;
  \Vert
    f - g
  \Vert_\infty
  \,.
$$

## Related concepts

* [[well group]]


## References

The stability theorem originates in:

* {#CohenSteinerEdelsbrunnerHarer07} [[David Cohen-Steiner]], [[Herbert Edelsbrunner]], [[John Harer]], *Stability of Persistence Diagrams*, Discrete & Computational Geometry **37** (2007) 103–120 $[$[doi:10.1007/s00454-006-1276-5](https://doi.org/10.1007/s00454-006-1276-5)$]$


Further developments: 


* [[Frédéric Chazal]], [[Vin de Silva]], [[Marc Glisse]], [[Steve Oudot]],  *The structure and stability of persistence modules*, SpringerBriefs in Mathematics, Springer (2016) $[$[arXiv:1207.3674](https://arxiv.org/abs/1207.3674), [doi:10.1007/978-3-319-42545-0](https://doi.org/10.1007/978-3-319-42545-0)$]$



[[!redirects stability in persistent homology]]

[[!redirects bottleneck distance]]
[[!redirects bottleneck distances]]


