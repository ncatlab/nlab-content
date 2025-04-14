

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Generally, for $G$ a [[finite group]] and $V$ a [[linear representation]] of $G$ on a [[finite dimensional vector space|finite dimensional]] [[complex vector space]], the _McKay quiver_ or _McKay graph_ associated with $V$ is the [[quiver]] whose [[vertices]] correspond to the [[irreducible representations]] $\rho_i$ of $G$ and which has $a_{i j} \in \mathbb{N}$ [[edges]] between the $i$th and the $j$th vertex, for $a_{i j}$ the [[coefficients]] in the expansion into [[irreps]] of the [[tensor product of representations]] of $V$ with these irreps:

$$
  V \otimes \rho_i
  \;\simeq\;
  \underset{j}{\bigoplus}
  a_{i j} \cdot \rho_j
  \,.
$$

Specifically this applies to the special case where $G \subset $ [[SU(2)]] a [[finite subgroup of SU(2)]] and $V$ its defining representation on $\mathbb{C}^2$. The [[McKay correspondence]] states that in this case the corresponding McKay quivers are [[Dynkin quivers]]/[[Dynkin diagrams]] in the same [[ADE classification]] as the [[ADE singularity]] $\mathbb{C}^2 \sslash G$.

More precisely: If one uses _all_ [[irreducible representations]] including the 1-dimensional [[trivial representation]] $\rho_0$ then one gets the "extended Dynkin diagram", where the extra node corresponds to $\rho_0$. This is the vertex indicated by a cross in the following diagrams:


\begin{center}
<img src="https://ncatlab.org/nlab/files/ExtendedADEQuivers.jpg" width="400">
\end{center}

> graphics grabbed from [GSV 83, p. 4](#GSV83)

In particular, for $G =\mathbb{Z}_N \subset SU(2)$ a [[cyclic group]] of [[order of a group|order]] $N$, there are $N$ complex [[irreps]] and the McKay quiver, i.e. the extended Dynkin diagram, has $N$-vertices, connected by edges to form a circle.


## Related concepts

* [[Dynkin quiver]]

* [[McKay correspondence]]

* [[quiver gauge theory]]

## References

The construction is due to

* {#McKay80} [[John McKay]], _Graphs, singularities, and finite groups_ Proc. Symp. Pure Math. Vol. 37. No. 183. 1980

Interpretation in terms of [[equivariant K-theory]] of the corresponding [[ADE-singularity]] and plain [[K-theory]] of its [[blowup]] is due to

* {#GSV83} [[Gérard Gonzalez-Sprinberg]], [[Jean-Louis Verdier]], p. 4 fo _Construction géométrique de la correspondance de McKay_, Ann. Sci. ́École Norm. Sup.16 (1983) 409–449. ([numdam](http://www.numdam.org/item?id=ASENS_1983_4_16_3_409_0))


See also

* Wikipedia, _[McKay graph](https://en.wikipedia.org/wiki/McKay_graph)_


[[!redirects McKay quivers]] 

[[!redirects McKay graph]]
[[!redirects McKay graphs]]
