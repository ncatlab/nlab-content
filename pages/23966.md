

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

Various generalizations of this stability result exist, notably the *algebraic stability theorem* ([CCGGO09](#CCGGO09)).

From [Botnan & Lesnick 18, p. 2](#BotnanLesnick18):

> The algebraic stability theorem is perhaps the central theorem in the theory of persistent homology; it provides the core mathematical justification for the use of persistent homology in the study of noisy data. The theorem is used, in one form or another, in nearly all available results on the approximation, inference, and estimation of persistent homology.



## Related concepts

* [[well group]]


## References

The stability theorem originates in:

* {#CohenSteinerEdelsbrunnerHarer07} [[David Cohen-Steiner]], [[Herbert Edelsbrunner]], [[John Harer]], *Stability of Persistence Diagrams*, Discrete & Computational Geometry **37** (2007) 103–120 $[$[doi:10.1007/s00454-006-1276-5](https://doi.org/10.1007/s00454-006-1276-5)$]$


The algebraic stability theorem:

* {#CCGGO09} [[Frédéric Chazal]], [[David Cohen-Steiner]], [[Marc Glisse]], [[Leonidas J. Guibas]], [[Steve Y. Oudot]], *Proximity of persistence modules and their diagrams*, SCG '09: Proceedings of the twenty-fifth annual symposium on Computational geometry (2009) 237–246 $[$[doi:10.1145/1542362.1542407](https://doi.org/10.1145/1542362.1542407)$]$

* [[Ulrich Bauer]], [[Michael Lesnick]], *Induced Matchings and the Algebraic Stability of Persistence Barcodes*, Journal of Computational Geometry **6** 2 (2015) 162-191 $[$[arXiv:1311.3681](https://arxiv.org/abs/1311.3681), [doi:10.20382/jocg.v6i2a9](https://doi.org/10.20382/jocg.v6i2a9)$]$


Further developments:

* [[Frédéric Chazal]], [[Vin de Silva]], [[Marc Glisse]], [[Steve Oudot]],  *The structure and stability of persistence modules*, SpringerBriefs in Mathematics, Springer (2016) $[$[arXiv:1207.3674](https://arxiv.org/abs/1207.3674), [doi:10.1007/978-3-319-42545-0](https://doi.org/10.1007/978-3-319-42545-0)$]$

Generalization to [[zigzag persistence modules]]:

* {#BotnanLesnick18} [[Magnus Bakke Botnan]], [[Michael Lesnick]], *Algebraic Stability of Zigzag Persistence Modules*, Algebr. Geom. Topol. **18** (2018) 3133-3204 $[$[arXiv:1604.00655](https://arxiv.org/abs/1604.00655), [doi:10.2140/agt.2018.18.3133](https://doi.org/10.2140/agt.2018.18.3133)$]$


[[!redirects stability in persistent homology]]

[[!redirects bottleneck distance]]
[[!redirects bottleneck distances]]


