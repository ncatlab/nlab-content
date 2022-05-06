

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

Given a [[topological space]] $X$ and a [[natural number]] $n$, writing $X^n$ for the $n$-fold [[product topological space]] of $X$ with itself, its _fat diagonal_ 

$$
  \mathbf{\Delta}_X^n \hookrightarrow X^n
$$ 

is the [[topological subspace]] of [[n-tuples]] of pairwise non-coincident points:

$$
  \mathbf{\Delta}_X^n
  \;\coloneqq\;
  \left\{
    (x_i) \in X^n 
      \;\vert\;
    x_i \neq x_j \, \text{for all}\, i,j
  \right\}
  \,.
$$

## Properties

### Relation to configuration spaces
 {#RelationToConfigurationSpaces}

The [[complement]] $X^n \setminus \mathbf{\Delta}_X^n$ of the $n$-fold [[Cartesian product]] by its fat diagonal may be understood as the [[configuration space]] of $n$ _distinguishable_ points in $X$. The [[quotient space]] of that by the [[action]] of the [[symmetric group]] $S_n$ given by [[permutation]] of points in $X$ yields the [[configuration space]] of $n$ _indistinguishable_ points in $X$:

$$
  Conf_n(X)
  \;\coloneqq\;
  \left( X^n \setminus \mathbf{\Delta}_X^n\right)/S_n
  \,.
$$

### Relation to renormalization

Closely related to the role of the fat diagonal in [[configuration spaces]] is its role in [[renormalization]] of [[perturbative quantum field theories]], which may be formulated as the choice of [[extensions of distributions]] (of [[time-ordered products]]) from the [[complement]] of a fat diagonal to the fat diagonal (the locus of coinciding "[[virtual particles]]" where [[interactions]] take place).

For more on this see at _[[geometry of physics -- perturbative quantum field theory]]_ the chapter _[Interacting quantum fields](geometry+of+physics+--+perturbative+quantum+field+theory#QuantumObservables)_


[[!redirects fat diagonals]]