
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

A [[function]] $f\colon X \to V$ on a [[topological space]] with values in a [[vector space]] $V$ (or really any [[pointed set]] with the basepoint called $0$) has __compact support__ (or is __compactly supported__) if the [[closure]] of its [[support]], the set of points where it is non-zero, is a [[compact space|compact subset]].  That is, the subset $\overline{f^{-1}(V \setminus \{0\})}$ is a [[compact subspace|compact subset]] of $X$.

Typically, $X$ is [[Hausdorff space|Hausdorff]], $f$ is a [[continuous function]], and $V$ is a Hausdorff [[topological vector space]] (or at least a pointed topological space whose basepoint is closed), so that $f^{-1}(V \setminus \{0\})$ is an [[open subspace]] of $X$, yet any compact subspace of $X$ must be [[closed subspace|closed]]; this is why we take the closure.

If we work with [[locales]] instead of topological spaces, then a closed point $0$ in $V$ still has an open subspace of $V$ as its formal dual, and we use this in the place of $V \setminus \{0\}$.


## Related concepts

* [[bump function]]

* [[compactly supported distribution]]

* [[integrable function]], [[square-integrable function]]

* [[bounded function]]

* __compactly supported function__

* [[measurable function]]

* [[rapidly decreasing function]]


[[!redirects compact support]]
[[!redirects compact supports]]

[[!redirects compactly supported continuous function]]
[[!redirects compactly supported continuous functions]]

[[!redirects compactly supported function]]
[[!redirects compactly supported functions]]
