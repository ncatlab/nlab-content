
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
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

## Idea

A [[character]] of a [[group]] $G$ is a [[group homomorphism]] into the [[circle group]], or more generally into the [[group of units]] $k^\times$ of a given ground [[field]].

Dually a co-character is a homomorphism out of $k^\times$ into $G$.

The collection of characters is itself an [[abelian group]] under the pointwise multiplication, this is called the **character lattice**
$ Hom(G,k^\times) $
of the group. Similarly the **cocharacter lattice** is $Hom(k^\times, G)$.


For [[topological groups]] one considers [[continuous map|continuous]] characters. Specifically, for a [[locally compact Hausdorff]] group $G$ (often further assumed to be an [[abelian group]]), a __character__ of $G$ is continuous homomorphism to the [[circle]] group $\mathbb{R}/\mathbb{Z}$. If $G$ is [[profinite group|profinite]], then this is the same as an continuous homomorphism to the [[discrete space|discrete]] group $\mathbb{Q}/\mathbb{Z}$.  (See [MO](http://mathoverflow.net/questions/86089/two-definitions-of-character-of-topological-groups).)


## Properties

### Characters and fundamental group of tori
 {#CharactersAndFundamentalGroupsOfTori}
 

Write $S^1$ for the [[circle group]].

Let $T$ be a [[torus]], regarded as an [[abelian group]]. 
Write $[T,S^1]$ for its character group.

There is a [[bilinear form]]

$$
  \pi_1(T)\otimes [T, S^1] \longrightarrow \mathbb{Z}
$$

on the [[fundamental group]] of the [[torus]] and its character group, given by sending a [[homotopy class]] $[\gamma]$ of a [[continuous map]]

$$
  \gamma \colon S^1 \longrightarrow
$$

to the [[homotopy class]] $c(\gamma)$ of the [[composition]] with a [[character]] $c \colon T \longrightarrow S^1$

$$
  c(\gamma) \;\colon\; S^1 \stackrel{\gamma}{\longrightarrow}
  T \stackrel{c}{\longrightarrow} S^1
$$

regarded as an element $[c(\gamma)] \in \pi_1(S^1) \simeq \mathbb{Z}$.

This [[bilinear form]] is non-degenerate, and hence constitutes an [[isomorphism]]

$$
  \pi_1(T) \simeq [T,S^1]
  \,.
$$

## Related concepts

* [[Pontryagin duality]], [[Pontryagin dual]]


[[!redirects group characters]]

[[!redirects character lattice]]
[[!redirects character lattices]]

[[!redirects cocharacter lattice]]
[[!redirects cocharacter lattices]]

[[!redirects co-character lattice]]
[[!redirects co-character lattices]]

[[!redirects character group]]
[[!redirects character groups]]
