

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The [[free construction|free]] [[topological monoid]] $F X$ on a [[topological space]] $X$ is canonically [[filtered topological spaces|filtered]] by the length of words.  Given instead a [[pointed topological space]] $(X,x)$, there is also a reduced version by taking $F X$ and identifying $x$ with the identity of $F X$. This latter [[filtered topological space]] is known as the _[[James construction]]_ $J(X,x)$ ([James 55](#James55)). 

## Details

 The [[James construction]] $J(X,x)$ may be constructed [[homotopy theory|homotopy-theoretically]] ([Brunerie 13](#Brunerie13), [Brunerie 17](#Brunerie17)). Recall that, for $K$ a finite [[simplicial complex]], for $(X,A)$ a pair of spaces, its _polyhedral product_ $(X,A)^K$ is defined as the union $\bigcup_{\sigma\in S(K)}(X,A)^\sigma$ as a subspace of the Cartesian product $X^{V(K)}$. Here, for $\sigma\in S(K)$ a simplex of $K$, the subspace $(X,A)^\sigma$ consist of those $x\in X^{V(K)}$ such that, for each vertex $v$ in the complement of $\sigma$, the coordinate projection $\proj_v x$ lies in $A$. Equivalently, the polyhedral product $(X,A)^K$ can be considered as a homotopy colimit of these $(X,A)^\sigma$ over the poset $S(K)$ of simplexes $\sigma$ of $K$, where the maps are the respective inclusions.

+-- {: .num_defn}
###### Definition

For $X$ a space equipped with a basepoint $x$, define a filtered space $fil_\bullet$ as follows. Set $\fil_0$ as $\{x\}$.
For $k\ge 1$, require that the following square is homotopy pushout:
$$
  \array{
 &&&&
     (X,x)^{\partial \Delta[k-1]}
     &&&&
      \\
      & 
      && inc \swarrow
       &
       & \searrow 
      && 
     \\
&& X^k &&&& fil_{k-1}
\\
      & 
      && {}_{p_k}\searrow
       &
       & \swarrow_{j_k}
      && 
     \\
&&&&
     fil_k
     &&&&
  }
$$
where the unlabeled arrow is the homotopy colimit of a morphism of diagrams over $S(\partial \Delta[k-1])$ given by the maps 
$$(X,x)^\sigma \xrightarrow{\sim} X^{\dim(\sigma)+1} \xrightarrow{p_{\dim(\sigma)+1}} fil_{\dim(\sigma)+1}$$
for each simplex $\sigma$ of the boundary simplicial complex $\partial \Delta[k-1]$ of the standard $(k-1)$-simplex. The homotopy colimit $fil_\infty$ of the sequence of maps $fil_0 \stackrel{j_1}{\to} fil_1 \stackrel{j_2}{\to} \ldots$ is called the **James construction** on $(X, x)$. 
=-- 

+-- {: .num_prop #TypeOfJames}
###### Proposition
 For $(X,x)$ a pointed space, if $(X,x)$ is path-connected, then $fil_\infty \simeq \Omega\Sigma X$.
=--

## Properties

### Relation to configuration spaces

The [[James construction]] of $X$ is [[homotopy equivalence|homotopy equivalent]] to the [[configuration space (mathematics)|configuration space]] $C(\mathbb{R}^1, X)$ of points in the [[real line]] with "[[charges]]" taking values in $X$.

(e.g. [Bödigheimer 87, Example 9](#Boedigheimer87))



## References


The construction is due to 

* {#James55} [[Ioan James]], _Reduced product spaces_, Annals of Mathematics, Second Series, 62: 170–197 (1955)

Review:

* [[Michael Hopkins]] (notes by [[Akhil Mathew]]), Lectures 2,3 in: _Spectra and stable homotopy theory_, 2012 ([pdf](http://math.uchicago.edu/~amathew/256y.pdf), [[HopkinsMathewStableHomotopyTheory.pdf:file]])


* [[Dylan Wilson]], _James construction_, 2017 ([pdf](http://www.math.uchicago.edu/~dwilson/pretalbot2017/james-construction.pdf))

* Wikipedia, _[James reduced product](https://en.wikipedia.org/wiki/James_reduced_product)_

Discussion via [[configuration space (mathematics)|configuration spaces]] includes

* {#Boedigheimer87} [[Carl-Friedrich Bödigheimer]], _Stable splittings of mapping spaces_, Algebraic topology. Springer 1987. 174-187 ([pdf](http://www.math.uni-bonn.de/~cfb/PUBLICATIONS/stable-splittings-of-mapping-spaces.pdf))


Discussion via [[homotopy type theory]] includes the following

* {#Brunerie13} [[Guillaume Brunerie]] _The James Construction and $\pi_4(S^3)$_, talk at the Institute of Advanced Studies on March 27, 2013 ([recording](https://video.ias.edu/univalent/1213/0327-GuillaumeBrunerie))

* {#Brunerie17} [[Guillaume Brunerie]], _The James construction and $\pi_4(S^3)$ in homotopy type theory_ ([arXiv:1710.10307](https://arxiv.org/abs/1710.10307))



[[!redirects James constructions]]