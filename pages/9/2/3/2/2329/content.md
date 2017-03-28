[[!redirects locally ringed space]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A __locally ringed space__ is a [[ringed space]] $(X,\mathcal{O})$ such that the [[stalks]] of the [[structure sheaf]] $\mathcal{O}$ are [[local ring]]s. 

A [[morphism]] of locally ringed space is a morphism of ringed spaces $(f,f^\sharp):(X,\mathcal{O}_X)\to (Y,\mathcal{O}_Y)$, where $f:X\to Y$, such that the [[comorphism]] $f^\sharp:\mathcal{O}_Y\to f_*\mathcal{O}_X$ is a morphism of [[local rings]] (that is, a map of rings which respects the [[maximal ideal]] (reflects invertibility)).

## Examples
* The category of smooth manifolds has a canonical inclusion into the category of locally ringed spaces. Indeed, any smooth manifold $M$ comes equipped with a sheaf of smooth real valued functions $\mathcal{C}^{\infty}_M$, and the maximal ideal in a given stalk consists precisely of germs of smooth functions which vanish at that point. Moreover, a smooth map $f: M \to N$ determines a comorphism $f^\sharp: \mathcal{C}^{\infty}_N \to f_* \mathcal{C}^{\infty}_M$ by the usual precomposition. In fact, the inclusion of smooth manifolds into locally ringed spaces is fully faithful. For a proof, see Lucas Braune's [nice answer](http://math.stackexchange.com/questions/225528/differentiable-manifolds-as-locally-ringed-spaces) on math stackexchange.
* [[scheme|Schemes]] are usually thought of as locally ringed spaces.

## On the locality condition

The condition that all stalks $\mathcal{O}_{X,x}$ are local rings can be reformulated without referring to the points of $X$:

* The only open subset $U$ such that $\mathcal{O}_X(U)$ is the zero ring is $U = \emptyset$.
* Let $f, g \in \mathcal{O}_X(U)$ be local sections such that $f + g$ is invertible in $\mathcal{O}_X(U)$. Then there is an open covering $U = V \cup W$ such that $f|_V \in \mathcal{O}_X(V)$ and $g|_W \in \mathcal{O}_X(W)$ are invertible. (It's allowed that $V$ or $W$ are empty.)

## Related concepts

* [[ringed space]], **locally ringed space**

* [[ringed locale]], [[locally ringed locale]]

* [[ringed site]], [[locally ringed site]]

* [[ringed topos]], [[locally ringed topos]]

* [[locally algebra-ed topos]]

* [[structured (∞,1)-topos]]

## References


* [[Aise Johan de Jong]], _[[The Stacks Project]]_, ([tag 01HA](http://stacks.math.columbia.edu/tag/01HA))
{#deJong}

* [[James Milne]], section 4 of _[[Lectures on Étale Cohomology]]_

[[!redirects locally ringed topological spaces]]


[[!redirects locally ringed spaces]]

