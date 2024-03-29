
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A priori a __locally compact topological group__ is a [[topological group]] $G$ whose underlying [[topological space]] is [[locally compact topological space|locally compact]]. 

Typically it is also assumed that $G$ is [[Hausdorff space|Hausdorff]]. (Notice that if not, then $G/\overline{\{1\}}$ is Hausdorff.). 

One often says just "locally compact group".

## Properties

### In harmonic analysis

We take here locally compact groups $G$ to be also Hausdorff. 

Locally compact topological groups are the standard object of study in classical abstract [[harmonic analysis]]. The crucial properties of locally compact groups is that they posses a left (right) [[Haar measure]] $\rho$ and that $L^1(\rho)$ has a structure of a 
[[Banach algebra|Banach]] $*$-[[star-algebra|algebra]]. 

A left (right) [[Haar measure]] on a locally compact topological group is a nonzero [[Radon measure]] which is invariant under the left (right) multiplications by elements in the group. A topological subgroup $H$ of a locally compact topological group $G$ is itself locally compact (in [[induced topology]]) iff it is closed in $G$. 

### Completeness 

Again taking locally compact groups $G$ to be Hausdorff, such are [[complete space|complete]] both with respect to their left [[uniform space|uniformity]] and their right uniformity. For if $\{x_\alpha\}$ is a [[Cauchy net]] in $G$ and $U$ is a compact neighborhood of the identity $e$, then there is $\alpha$ so large that $x_\beta x_\alpha^{-1} \in U$ for all $\beta \geq \alpha$. Those elements converge to a point $x \in U$ since $U$ is compact, and the original net converges to $x \cdot x_\alpha$. A similar argument is used for the right uniformity. 

### Pontrjagin duality

See at *[[Pontrjagin duality]]*.

### Kazhdan's property (T)

_[[Kazhdan's property (T)]]_

## Related concepts

* [[compact topological group]], [[compact Lie group]]

* [[maximal compact subgroup]], [[closed subgroup]]

* [[locally compact groupoid]]

* [[coset space coprojections admitting local sections]]

## References

* [[Linus Kramer]], *Locally Compact Groups*, 2017 ([pdf](https://www.uni-muenster.de/AGKramer/content/LCManuscript.pdf), [[Kramer_LocallyCompactGroups.pdf:file]])

* Gerald B. Folland, _A course in abstract harmonic analysis_, Studies in Adv. Math. CRC Press 1995 

See also:

* Wikipedia, *[Locally compact group](https://en.wikipedia.org/wiki/Locally_compact_group)*

[[!redirects locally compact topological groups]]

[[!redirects locally compact group]]
[[!redirects locally compact groups]]

