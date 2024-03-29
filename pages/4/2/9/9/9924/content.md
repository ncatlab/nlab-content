[[!redirects Kan-Thurston Theorem]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

The _Kan-Thurston theorem_ says that every [[path-connected topological space]] is [[ordinary homology|homology]]-[[equivalence|equivalent]] to the [[classifying space]] $K(G,1)$ of a [[discrete group]] $G$.

## Statement

For every path connected  space $X$ with base point there exists a ([[Serre fibration|Serre-]])-[[fibration]]

$$
  t X \colon T X \rightarrow X
$$ 

which is natural with respect to $X$ and has the following properties. 

(i) The map $t X$ induces an [[isomorphism]] on ([[singular homology|singular]]-)[[homology]] and [[singular cohomology|cohomology]] with [[local coefficient bundle|local coefficients]]

$$H_*(T X;A)\cong H_*(X;A),\;\;  H^*(T X;A)\cong H^*(X;A)$$ 
for every local coefficient system $A$ on $X$, and 

(ii) $\pi_i\;(T X)$ is trivial for $i\neq 1$ and $\pi_1\;t X$ is onto.

Furthermore the [[homotopy type]] of $X$ is completely determined by the pair of groups $(G_X, P_X)$ where 
$G_X  = \pi_1T X,\;\; P_X = ker\;\pi_1t X$ and $P_X$ is a 
[[perfect group|perfect]] [[normal subgroup|normal]] [[subgroup]] of $G_X$. 

More precisely, $X$ can be recovered, up to homotopy, by applying the [[plus construction]] to $K(G_X,1)$ with respect to $P_X$.
 

More generally, the Kan-Thurston theorem
gives an embedding of the homotopy category of topological spaces into the category of presheaves on the category whose objects are groups and whose morphisms are conjugacy classes of [[group homomorphisms]].  Under this embedding a topological space $X$ is sent to the presheaf $G \mapsto [B G, X]$.

## References

* [[Daniel Kan]] and [[William Thurston]], _Every connected space has the homology of a $K(\pi,1)$_, Topology  Vol.  15.  pp.  253--258, 1976.  

