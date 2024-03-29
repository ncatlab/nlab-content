
#Contents#
* table of contents
{:toc}

## Idea

The concept of _reduced cylinder_ is the analog for [[pointed objects]] of [[cylinder]] constructions.

The [[mapping cone]] of $X \to \ast$ formed with the standard reduced cylinder is the [[reduced suspension]] of $X$.

Applying the reduced cylinder construction degreewise to a [[sequential spectrum]] yields the standard [[cylinder spectrum]] construction.


## For pointed topological spaces

Specifically in [[topological spaces]], with $I = [0,1] \subset \mathbb{R} \in $ [[Top]] the [[closed interval]] with its [[Euclidean space|Euclidean]] [[metric topology]] and $I_+ \in Top^{\ast/}$ its [[pointed topological space|pointed]] version with a basepoint freely adjoined, then for $X$ a [[pointed topological space]], the standard **reduced cylinder** over it is the [[smash product]]

$$
  X \wedge (I_+) \;\; \in Top^{\ast/}
  \,.
$$ 

This is obtained from the ordinary standard cylinder $X \times I$ by passing to the [[quotient space]] ([this example](quotient+space#QuotientBySubspace)) given by collapsing the copy of $I$ that sits over the basepoint $x$ of $X$:

$$
  X \wedge (I_+) \simeq (X \times I)/(\{x\} \times I)
  \,.
$$

For the purposes of [[generalized (Eilenberg-Steenrod) cohomology]] theory typically it does not matter whether one evaluates on the standard cylinder or the reduced cylinder. For example for [[topological K-theory]] since since $\{x\} \times I$ is a [[contractible topological space|contractible]] [[closed subspace]], then [this prop.](topological+vector+bundle#VectorBundlesOverQuotientByContractibleSubspaceAreEquivalentToVectorBundlesOnTotalSpace) says that [[topological vector bundles]] do not see a difference as long as $X$ is a [[compact Hausdorff space]].

## References

Early lecture notes include

* [[Frank Adams]], part III, section 2 _[[Stable homotopy and generalised homology]]_, 1974



[[!redirects reduced cylinders]]

[[!redirects reduced cylinder object]]
[[!redirects reduced cylinder objects]]