
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

+-- {: .un_def}
###### Definition

The **framed little 2-disk operad** is the [[operad]] $P$ in [[Top]] whose [[topological space]] $P(n)$ of $n$-ary operations is the space of maps

$$
  \coprod_n D \to D
$$

from $n$-copies of the 2-[[ball]] to itself, which restrict on each component to a map that is a combination of 

* a translation

* a dilatation

* a rotation

of the disk (regarded via its standard [[embedding]] $D \hookrightarrow \mathbb{R}^2$ into the 2-simensional [[Cartesian space]]) such that the images of all disks are disjoint.
=--

+-- {: .un_remark}
###### Remark

This differs from the [[little 2-disk operad]] by the fact that rotations of the disks are admitted. Under passing to chains and then to [[homology]], this operation gives rise to the BV-operator in a [[BV-algebra]]. See [Properties](#Properties) below.

=--

## Properties {#Properties}


+-- {: .un_theorem}
###### Theorem

The [[homology]] of the framed little 2-disk operad in chain complexes is the operad for [[BV-algebra]]s.

=--

This is due to ([Getzler](#Getzler)).


+-- {: .un_def}
###### Definition

Write $R \beta_j$ for the [[ribbon braid group]] on $j$ elements and $P R \beta_j$ for the [[kernel]] of the surjection $R \beta_j \to \Sigma_j$ onto the [[symmetric group]].

Say that a [[ribbon operad]] $P$ is an **$R_\infty$-operad** if the [[ribbon braid group]]s  act freely and properly on $P$ and if each [[topological space]] $P(k)$ is [[contractible]].

=--

+-- {: .un_theorem}
###### Theorem


If $P$ is an $R_\infty$-operad, then the sequence of quotient spaces $\{P(n)/P R \beta_n\}$  forms a symmetric operad equivalent to the frame little disks operad.

=--

This is ([Wahl, lemma 1.5.17](#Wahl)).

# Related concpets

* **framed little 2-disk operad**

* [[framed little n-disk operad]]

## References

The framed little 2-disk operad was introduced in

* [[Ezra Getzler]], _Batalin-Vilkovisky algebras and two-dimensional topological field theories_ , Comm. Math. Phys. 159 (1994), no. 2, 265&#8211;285. ([arXiv](http://arxiv.org/abs/hep-th/9212043))
{#Getzler}

* Nathalie Wahl, _Ribbon braids and related operads_ PhD thesis, Oxford (2001) ([pdf](http://eprints.maths.ox.ac.uk/43/1/wahl.pdf)).
{#Wahl}

[[!redirects framed little disk operad]]