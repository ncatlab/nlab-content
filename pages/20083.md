

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

Generally, for $G$ a [[finite group]] and $V$ a [[linear representation]] of $G$ on a [[finite dimensional vector space|finite dimensional]] [[complex vector space]], the _McKay quiver_ or _McKaey graph_ associated with $V$ is the [[quiver]] whose [[vertices]] correspond to the [[irreducible representations]] $\rho_i$ of $G$ and which has $a_{i j} \in \mathbb{N}$ [[edges]] between the $i$th and the $j$th vertex, for $a_{i j}$ the [[coefficients]] in the expansion into [[irreps]] of the [[tensor product of representations]] of $V$ with these irreps:

$$
  V \otimes \rho_i
  \;\simeq\;
  \underset{j}{\bigoplus}
  a_{i j} \cdot \rho_j
  \,.
$$

Specifically this applies to the special case where $G \subset $ [[SU(2)]] a [[finite subgroup of SU(2)]] and $V$ its defining representation on $\mathbb{C}^2$. The [[McKay correspondence]] states that in this case the corresponding McKay quivers are [[Dynkin quivers]]/[[Dynkin diagrams]] in the same [[ADE classification]] as the [[ADE singularity]] $\mathbb{C}^2 \sslash G$.

## Related concepts

* [[Dynkin quiver]]

* [[McKay correspondence]]

* [[quiver gauge theory]]

## References

See also

* Wikipedia, _[McKay graph](https://en.wikipedia.org/wiki/McKay_graph)_


[[!redirects McKay quivers]] 

[[!redirects McKay graph]]
[[!redirects McKay graphs]]
