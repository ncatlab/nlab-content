[[!redirects center of an ∞-group]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The generalization of the notion of [[center]] from [[group]]s to [[∞-groups]].

## Definition

For $G \in \infty Grp(\mathcal{X})$ an [[∞-group]], there is a canonical morphism

$$
  AUT(G) \to Out(G)
$$

from its [[automorphism ∞-group]] $AUT(G) := \underline{Aut}_{\mathcal{X}}(\mathbf{B}G)$ to its [[outer automorphism ∞-group]].

The [[homotopy fiber]] of this morphism 

$$
  \mathbf{B} Z(G) \to Aut(G) \to Out(G)
$$

is the [[delooping]] of an [[∞-group]] $Z(G)$. This is the **center** of $G$.

## Examples

### Centers of ordinary groups

For $\mathcal{X} = $ [[∞Grpd]] and $G$ [[truncated|0-truncated]], it is an ordinary [[discrete group]]. Its [[automorphism 2-group]] is the [[strict 2-group]] coming from the [[crossed module]] $[G \stackrel{Ad}{\to} Aut(G)]$. The morphism
$AUT(G) \to Out(G)$ is a [[fibration]] hence its [[homotopy fiber]] is, up to equivalence, the ordinary fiber, which is the crossed module $(G \stackrel{Ad}{\to} Inn(G))$, where $Inn(G) \subset Aut(G)$ is the group of [[inner automorphism]]s. This is equivalent to $(Z(G) \to 1)$, where $Z(G)$ is the ordinary [[center]] of $G$, and this is the crossed module corresponding to $\mathbf{B}Z(G)$. 

## Related concepts

* [[higher central extension]]

* [[group]], [[2-group]], [[∞-group]],

* [[automorphism group]], [[automorphism 2-group]], [[automorphism ∞-group]],

* [[center]], **center of an $\infty$-group**,

* [[inner automorphism group]]

* [[outer automorphism group]], [[outer automorphism ∞-group]]

