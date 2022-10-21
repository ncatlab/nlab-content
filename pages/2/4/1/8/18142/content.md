
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

## Idea

The _Jordan curve theorem_ is a basic fact in [[topology]]. It stands out as having a statement that intuitively seems completely obvious, but which turns out to require a non-trivial [[formal proof]].

The theorem states that every [[continuous function|continuous]] [[loop]] (where a loop is a closed [[curve]]) in the [[Euclidean plane]] which does not intersect itself (a _[[Jordan curve]]_) divides the [[plane]] into two [[disjoint subsets]] (the [[connected components]] of the curve\'s [[complement]]), a [[bounded subspace|bounded]] region inside the curve, and an unbounded region outside of it, each of which has the original curve as its [[boundary]].

## In constructive mathematics

Given a notion of real number $\mathbb{R}$ in constructive mathematics, a [[Jordan curve]] consists of a [[set]] $J$ with a specific [[injection]] $i:J \to \mathbb{R}^2$ into the Euclidean plane $\mathbb{R}^2$, and a [[homeomorphism]] $h:\mathbb{S}^1 \to \mathrm{im}(i)$ from the topological [[unit circle]] $\mathbb{S}^1$ to the [[image]] of the subset injection. 

...

section under construction

...

In [[constructive mathematics]], the Jordan curve theorem is stated as 

\begin{theorem}
Given a Jordan curve $J$, two points $a$ and $b$ can be constructed off of $J$, such that given any point $c$ off of $J$, we can construct a polygonal path that is bounded away from $J$, and that joins $c$ to one of $a$ or $b$, and any polygonal path joining $a$ and $b$ comes arbitrarily close to $J$. 
\end{theorem}

## Generalization

The __Jordan--Brouwer separation theorem__ states that, in the [[Cartesian space]] $\mathbb{R}^n$, every simple closed continuous [[hypersurface]] (defined as the [[image]] of a [[continuous map|continuous]] [[injection]] from the [[sphere]] $S^{n-1}$) has an [[exterior]] with two [[connected components]], one [[bounded subspace|bounded]] (the inside of the hypersurface) and one unbounded, each of which has the original hypersurface as its [[boundary]].  (Furthermore, the continuous map defining the hypersurface can be extended to an [[automorphism|auto]]-[[homeomorphism]] of $\mathbb{R}^n$ under which the inside and outside appear as the images of the inside and outside of the sphere.)


## Related theorems

* [[Tietze extension theorem]]

* [[topological invariance of dimension]]

* [[Brouwer's fixed point theorem]]


## References

*  G. Berg, W. Julian, R. Mines, F. Richman, *The constructive Jordan curve theorem*,  Rocky Mountain J. Math. 5(2): 225-236 (Spring 1975). ([DOI:10.1216/RMJ-1975-5-2-225](https://doi.org/10.1216/rmj-1975-5-2-225))

* Wikipedia, _[Jordan curve theorem](https://en.wikipedia.org/wiki/Jordan_curve_theorem)_


[[!redirects Jordan curve theorem]]
[[!redirects Jordan Curve Theorem]]

[[!redirects Jordan-Brouwer theorem]]
[[!redirects Jordan-Brouwer Theorem]]
[[!redirects Jordan–Brouwer theorem]]
[[!redirects Jordan–Brouwer Theorem]]
[[!redirects Jordan--Brouwer theorem]]
[[!redirects Jordan--Brouwer Theorem]]
[[!redirects Jordan-Brouwer separation theorem]]
[[!redirects Jordan-Brouwer Separation Theorem]]
[[!redirects Jordan–Brouwer separation theorem]]
[[!redirects Jordan–Brouwer Separation Theorem]]
[[!redirects Jordan--Brouwer separation theorem]]
[[!redirects Jordan--Brouwer Separation Theorem]]

[[!redirects Jordan's curve theorem]]

