
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Formal geometry
+--{: .hide}
[[!include formal geometry -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A [[topological ring]] $R$ is an __adic noetherian ring__ if it is [[noetherian ring|noetherian]] as a [[ring]] and it has a [[topological basis]] consisting of all translations of the [[neighborhoods]] of zero of the form $I^n$ ($n\gt 0$) where $I\subset R$ is a fixed [[ideal]] of $R$, and $R$ is [[Hausdorff space|Hausdorff]] and [[complete space|complete]] in that topology. A choice of such an ideal is said to be the __defining ideal__ or (more French) the __ideal of definition__ of the topological ring $R$. If $R$ is an adic noetherian ring, an ideal $J\subset R$ is a defining ideal iff it is open and its powers tend to $\{0\}$. 

The [[topology]] of an adic noetherian ring $R$ with the defining ideal $I$ is said to be the **$I$-adic topology** and the descending [[filtration]] of $R$ by the powers of $I$ to be the **$I$-adic filtration**.

For an adic noetherian ring $R$ there is a construction of a [[ringed space]], its [[formal spectrum]] $Spf(R)$, which does not depend on the choice of the ideal $I\subset R$ generating its (fixed in advance) topology. The underlying topological space of $Spf(R)$ is $Spec(R/I)$ which is (under the above assumptions on $R$ and $I$) a [[closed subspace]] of the [[spectrum (geometry)|spectrum]] $Spec(R)$ and it contains all closed points of $Spec(R)$.

## Related concepts

* [[completion of a ring]]

* [[linear topological ring]]

* [[pro-ring]]

## References

* PlanetMath _[I-adic topology](http://planetmath.org/iadictopology)_

* Wikipedia, _[Krull topology](https://en.wikipedia.org/wiki/Completion_%28algebra%29#Krull_topology)_

[[!redirects adic topology]]
[[!redirects adic topologies]] 
[[!redirects adic filtration]]

[[!redirects adic ring]]
[[!redirects adic rings]]
