
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Category of open subsets
* table of contents
{: toc}

## Definition

Given a [[topological space]] $X$, the **category of open subsets** $Op(X)$ of $X$ is the [[category]] whose

* [[object | objects]] are the [[open subset | open subsets]] $U \hookrightarrow X$ of $X$;

* [[morphism | morphisms]] are the inclusions 
$
  \array{
     V &&\hookrightarrow && U
     \\
     & \searrow && \swarrow
     \\
     && X
  }
$ of open subsets into each other.


## Properties

* The category $Op(X)$ is a [[poset]], in fact a [[frame]] (dually a [[locale]]): it is the [[frame of opens]] of $X$.

* The category $Op(X)$ is naturally equipped with the
structure of a [[site]], where a collection $\{U_i \to U\}_i$ of morphisms is a cover precisely if their [[union]] in $X$ equals $U$:
$$ \bigcup_i U_i = U .$$

  The [[category of sheaves]] on $Op(X)$ equipped with this site structure is typically referred to as the _[[category of sheaves on a topological space|category of sheaves on the topological space]]_ and denoted

  $$
    Sh(X) \;\coloneq\; Sh(Op(X))
    \,.
  $$

* The category $Op(X)$ is also a [[suplattice]].


## Related concepts

* [[spatial locale]]

* [[spatial topos]]

[[!redirects category of opens]]
[[!redirects categories of opens]]
[[!redirects category of open sets]]
[[!redirects categories of open sets]]
[[!redirects category of open subsets]]
[[!redirects categories of open subsets]]
[[!redirects category of open subspaces]]
[[!redirects categories of open subspaces]]

[[!redirects site of open subsets]]
[[!redirects site of opens]]

[[!redirects sites of open subsets]]
[[!redirects sites of opens]]

[[!redirects poset of open subsets]]
[[!redirects posets of open subsets]]

[[!redirects lattice of open subsets]]
[[!redirects lattices of open subsets]]


[[!redirects frame of open subsets]]
[[!redirects frames of open subsets]]


