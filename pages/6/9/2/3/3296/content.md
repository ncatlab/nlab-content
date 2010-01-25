<div class="rightHandSide toc">
[[!include cohomology - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}


## Idea

In the general context of [[cohomology]], as described there, a [[cocycle]] representing a cohomology class on an object $X$ with coefficients in an object $A$ is a [[morphism]] $c : X \to A$ in a given ambient [[(∞,1)-topos]] $\mathbf{H}$.

The same applies with the object $A$ taken as the domain object: for $B$ yet another object, the $B$-valued cohomology of $A$ is similarly $H(A,B) = \pi_0 \mathbf{H}(A,B)$. For $[k] \in H(A,B)$ any cohomology class in there, we obtain an [[∞-functor]]

$$
  [k(-)] : \mathbf{H}(X,A) \to H(X,B)
$$

from the $A$-valued cohomology of $X$ to its $B$-valued cohomology, simply from the composition operation

$$
  \mathbf{H}(X,A) \times \mathbf{H}(A,B) \to \mathbf{H}(X,B)
  \,.
$$

Quite generally, for $[c] \in H(X,A)$ an $A$-cohomology class, its image $[k(c)] \in H(X,B)$ is the corresponding **characteristic class**.

+-- {: .standout}

From the [[nPOV]], where [[cocycle]]s are elements in an [[derived hom space|(∞,1)-categorical hom-space]], forming **characteristic classes** is nothing but the _composition_ of cocycles.

=--

In practice one is interested in this notion for particularly simple objects $B$, notably for $B$ an [[Eilenberg-MacLane object]] $\mathbf{B}^n K$ for some component $K$ of a [[spectrum object]]. This serves to **characterize** cohomology with coefficients in a complicated object $A$ by a collection of cohomology classes with simpler coefficients. Therefore the name _characteristic class_ .

+--{.query}
Zoran: While the discussion of the name 'characteristic class' is plausible, it is, I think, unfortunately not historically true. The continuous map into the classifying space, by which the pullback of a universal class gives the characteristic class of a manifold is traditionally called the **characteristic map**. because that map characterizes that cohomology class. It is not the cohomology *theory* which is characterized by that map, but the very *class*. So characteristic classes are those which can be *characterized* by the maps to given classifying space.
=--

Then with the usual notation $H^n(X,K) := H(X, \mathbf{B}^n K)$ a given characteristic class in degree $n$ assigns

$$
  [k(-)] : \mathbf{H}(X,A) \to H^n(X,K)
  \,.
$$

Moreover, recall from the discussion at [[cohomology]] that to every [[cocycle]] $c : X \to A$ is associated the object $P \to X$ that it classifies -- its [[homotopy fiber]] -- which may be thought of as an $A$-[[principal ∞-bundle]] over $X$ with classifying map $X \to A$. One typically thinks of the characteristic class $[k(c)]$ as characterizing this [[principal ∞-bundle]] $P$.

## Examples

### Integral characteristic classes of principal bundles

This is the archetypical example: let $\mathbf{H}  =$ [[Top]] and let $G$ be a [[topological group]] and $\mathcal{B}G$ its [[classifying space]].

The [[integral cohomology]] of this classifying space is of course

$$
  H^n(\mathcal{B}G, \mathbb{Z}) = \pi_0 Top(\mathcal{B}G, \mathcal{B}^n\mathbb{Z})
  \,.
$$

A $G$-[[principal bundle]] $P \to X$ is classified by some map $c : X \to \mathcal{B}G$. For any $k \in H^n(\mathcal{B}G,\mathbb{Z})$ a degree $n$ cohomology class of the classifying space, the corresponding composite map
$X \stackrel{c}{\to} \mathcal{B}G \stackrel{k}{\to} \mathcal{B}^n \mathbb{Z}$ represents a class $[k(c)] \in H^n(X,\mathbb{Z})$. This is the corresponding characteristic class of the bundle.

Notable families of examples include:

* for $G = O$ the [[orthogonal group]]: [[Pontryagin class]]es;

* for $G = U$ the [[unitary group]]: [[Chern class]]es;

### Chern character

The [[Chern character]] is a natural characteristic class with values in real cohomology. See there for more details.