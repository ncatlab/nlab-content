
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Let $\mathcal{X}$ be an [[(∞,1)-topos]] and $G \in \infty Grpd(\mathcal{X})$ an [[n-truncated]] [[∞-group]] object, for some $n \in \mathbb{N}$ (an [[n-group]] in $\mathcal{X}$).

Write

$$
  AUT(G) := \underline{Aut}(\mathbf{B}G) \hookrightarrow [\mathbf{B}G, \mathbf{B}G]
  \in 
  \mathcal{X}
$$

for the [[internalization|internal]] [[automorphism ∞-group]].

Then the [[truncated|n-truncation]]

$$
  Out(G) := \tau_n AUT(G) \in \infty Grp(\mathcal{X})
$$

is the **outer automorphism $\infty$-group** of $G$.

## Examples

* For $\mathcal{X} = $ [[∞Grpd]] and $n = 0$, $G$ is an ordinary [[discrete group]], and $AUT(G)$ is its [[automorphism 2-group]]. Then $Out(G)$ is the ordinary group of ordinary [[outer automorphism]]s.

## Applications

* Outer automorphism $\infty$-groups control part of the [[nonabelian cohomology]] of [[∞-gerbe]]s. See there for more details.


## Related concepts

* [[group]], [[∞-group]],

* [[automorphism group]], [[automorphism ∞-group]],

* [[center]], [[center of an ∞-group]]

* [[outer automorphism group]], **outer automorphism $\infty$-group**

[[!redirects outer automorphism ∞-group]]
[[!redirects outer automorphism ∞-groups]]
[[!redirects outer automorphism infinity-groups]]