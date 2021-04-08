
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Group Theoryc
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea

A _topological group_ is a [[topological space]] with a continuous [[group]] structure: a [[group object]] in the [[category]] [[Top]].

## Definition

+-- {: .num_defn}
###### Definition

A _topological group_ is 

1. a [[group]], hence 

   1. a [[set]] $G$,

   1. a [[neutral element]] $e \in G$,

   1. a [[associativity|associative]] [[unitality|unitality]] [[function]]

   1. $(-)\cdot (-) \;\colon\; G \times G \to G$,

   1. a function $(-)^{-1} \;\colon\; G \to G$ such that $g \cdot g^{-1} = e = g^{-1} \cdot g$ for all $g \in G$;

1. a topology $\tau_G \subset P(G)$ giving $G$ the structure of a [[topological space]]

such that the operations $(-)^{-1}$ and $(-)\cdot (-)$ are [[continuous functions]] (the latter with respect to the [[product topology]]).

=--


## Properties

### General

+-- {: .num_lemma #OpenSubgroupOfTopologicalGroupIsClosed}
###### Lemma
**(open subgroups of topological groups are closed)**

Every [[open subset|open]] [[subgroup]] $H \subset G$ of a topological group is [[closed subset|closed]].

=--

(e.g [Arhangel'skii-Tkachenko 08, theorem 1.3.5](#ArhangelskiiTkachenko08))

+-- {: .proof}
###### Proof

The set of $H$-[[cosets]] is a [[cover]] of $G$ by [[disjoint subsets|disjoint]] [[open subsets]]. One of these cosets is $H$ itself and hence it is the complement of the union of the other cosets, hence the complement of an open subspace, hence closed.

=--

+-- {: .num_prop #ConnectedLocallyCompactTopologicalGroupsAreSigmaCompact}
###### Proposition
**([[connected space|connected]] [[locally compact topological space|locally compact]] [[topological groups]] are [[sigma-compact topological space|sigma-compact]])**

Every [[connected topological space|connected]] [[locally compact topological space|locally compact]] topological group is [[sigma-compact topological space|sigma-compact]].

Every [[locally compact topological space|locally compact]] topological group is [[paracompact topological space|paracompact]].

=--

(e.g. [Arhangel'skii-Tkachenko 08, cor. 3.1.4, cor. 3.1.5](#ArhangelskiiTkachenko08))

+-- {: .proof}
###### Proof

By assumption of local compactness, there exists a [[compact topological space|compact]] [[neighbourhood]] $C_e \subset G$ of the [[neutral element]]. We may assume without restriction of generality that with $g \in C_e$ any element, then also the [[inverse element]] $g^{-1} \in C_e$.

For if this is not the case, then we may enlarge $C_e$ by including its inverse elements, and the result is still a compact neighbourhood of the neutral element: Since taking [[inverse elements]] $(-)^{-1} \colon G \to G$ is a [[continuous function]], and since [[continuous images of compact spaces are compact]], it follows that also the set of inverse elements to elements in $C_e$ is compact, and the union of two compact subspaces is still compact (obviously, otherwise see [this prop](compact+space#UnionsAndIntersectionOfCompactSubspaces)). 

Now for $n \in \mathbb{N}$, write $C_e^n  \subset G$ for the [[image]] of $\underset{k \in \{1, \cdots n\}}{\prod} C_e \subset \underset{k \in \{1, \cdots, n\}}{\prod} G$ under the iterated group product operation $\underset{k \in \{1, \cdots, n\}}{\prod} G \longrightarrow G$.

Then 

$$
  H \coloneqq \underset{n \in \mathbb{N}}{\cup} C_e^n
    \;\subset\; 
  G
$$ 

is clearly a topological subgroup of $G$. 

Observe that each $C_e^n$ is compact. This is because $\underset{k \in \{1, \cdots, n\}}{\prod}C_e$ is compact by the [[Tychonoff theorem]], and since [[continuous images of compact spaces are compact]]. Thus 

$$
  H = \underset{n \in \mathbb{N}}{\cup} C_e^n
$$

is a countable union of compact subspaces, making it [[sigma-compact]]. Since [[locally compact and sigma-compact spaces are paracompact]], this implies that $H$ is paracompact.

Observe also that the subgroup $H$ is open, because it contains with the [[interior]] of $C_e$ a non-empty open subset $Int(C_e) \subset H$ and we may hence write $H$ as a union of open subsets

$$
  H = \underset{h \in H}{\cup} Int(C_e) \cdot h
  \,.
$$

Finally, as indicated in the proof of Lemma \ref{OpenSubgroupOfTopologicalGroupIsClosed}, the cosets of the open subgroup $H$ are all open and partition $G$ as a [[disjoint union space]] ([[coproduct]] in [[Top]]) of these open cosets. From this we may draw the following conclusions. 

* In the particular case where $G$ is connected, then there is just one such coset, namely $H$ itself. The argument above thus shows that a connected locally compact topological group is $\sigma$-compact and (by local compactness) also paracompact.

* In the general case, all the cosets are homeomorphic to $H$ which we have just shown to be a paracompact group. Thus $G$ is a [[disjoint union space]] of paracompact spaces. This is again paracompact (by [this prop.](paracompact+topological+space#ParacompactnessPreservedByDisjointUnion)).

=--

### Uniform structure

A topological group $G$ carries two canonical [[uniform space|uniformities]]: a right and left uniformity. The **right uniformity** consists of entourages $\sim_{l, U}$ where $x \sim_{l, U} y$ if $x y^{-1} \in U$; here $U$ ranges over neighborhoods of the identity that are symmetric: $g \in U \Leftrightarrow g^{-1} \in U$. The **left uniformity** similarly consists of entourages $\sim_{r, U}$ where $x \sim_{r, U} y$ if $x^{-1} y \in U$. The uniform topology for either coincides with the topology of $G$. 

Obviously when $G$ is commutative, the left and right uniformities coincide. They also coincide if $G$ is compact Hausdorff, since in that case there is only one uniformity whose uniform topology reproduces the given topology. 

Let $G$, $H$ be topological groups, and equip each with their left uniformities. Let $f: G \to H$ be a group homomorphism. 

+-- {: .num_prop}
######Proposition
The following are equivalent: 

* The map $f$ is continuous at a point of $G$; 

* The map $f$ is continuous; 

* The map $f$ is uniformly continuous. 

=-- 

+-- {: .proof} 
######Proof
Suppose $f$ is continuous at $g \in G$. Since neighborhoods of a point $x$ are $x$-translates of neighborhoods of the identity $e$, continuity at $g$ means that for all neighborhoods $V$ of $e \in H$, there exists a neighborhood $U$ of $e \in G$ such that 

$$f(g U) \subseteq f(g) V$$

Since $f$ is a homomorphism, it follows immediately from cancellation that $f(U) \subseteq V$. Therefore, for every neighborhood $V$ of $e \in H$, there exists a neighborhood $U$ of $e \in G$ such that 

$$x y^{-1} \in U \Rightarrow f(x) f(y)^{-1} = f(x y^{-1}) \in V$$ 

in other words such that $x \sim_U y \Rightarrow f(x) \sim_V f(y)$. Hence $f$ is uniformly continuous with respect to the right uniformity. By similar reasoning, $f$ is uniformly continuous with respect to the right uniformity.
=--


### Unitary representation on Hilbert spaces

+-- {: .num_defn}
###### Definition

A unitary [[representation]] $R$ of a topological group $G$ in a [[Hilbert space]] $\mathcal{H}$ is a continuous [[group homomorphism]]

$$
   R \colon G \to \mathcal{U}(\mathcal{H})
$$

where $\mathcal{U}(\mathcal{H})$ is the group of [[unitary operator]]s on $\mathcal{H}$ with respect to the [[strong topology]].

=--

+-- {: .num_remark}
###### Remark

Here $\mathcal{U}(\mathcal{H})$ is a complete, metrizable topological group in the [[strong topology]], see ([Schottenloher, prop. 3.11](#Schottenloher)).

=--

+-- {: .num_remark}
###### Remark


In [[physics]], when a [[classical mechanical system]] is symmetric, i.e. invariant in a proper sense, with respect to the action of a topological group $G$, then an unitary representation of $G$ is sometimes called a **quantization** of $G$. See at _[[geometric quantization]]_ and _[[orbit method]]_ for more on this.

=--


#### Why the strong topology is used

The reason that in the definition of a [[unitary representation]], the [[strong operator topology]] on $\mathcal{U}(\mathcal{H})$ is used and not the [[norm topology]], is that only few [[homomorphisms]] turn out to be [[continuous map|continuous]] in the norm topology.

Example: let $G$ be a [[compact topological space|compact]] [[Lie group]] and $L^2(G)$ be the [[Hilbert space]] of square integrable [[measurable function]]s with respect to its [[Haar measure]]. The right [[regular representation]] of $G$ on $L^2(G)$ is defined as

$$
      R: G \to \mathcal{U}(L^2(G))
$$

$$
         g \mapsto (R_g: f(x) \mapsto f(x g))
$$

and this will generally not be continuous in the norm topology, but is always continuous in the strong topology. 

### Which topological groups admit Lie group structure?

* _[[Hilbert's fifth problem]]_

### Protomodularity
 {#Protomodularity}

+-- {: .num_prop}
###### Proposition

The [[category]] [[TopGrp]] of topological groups and [[continuous function|continuous]] [[group homomorphisms]] between them is a [[protomodular category]].

=--

A proof is spelled out by [[Todd Trimble]] [here on MO](http://mathoverflow.net/questions/133110/why-is-topgrp-the-category-of-topological-groups-and-continous-homomorphisms-prot/133601#133601).

## Examples

* The [[classical Lie groups]] are in particular topological groups, such as the [[general linear group]] and its subgroups.

* ...


## Related concepts

* [[group]]

* [[discrete group]], [[finite group]]

* [[topological monoid]]

* **topological group**, 

  * [[locally compact topological group]]

  * [[compact topological group]]

  * [[amenable topological group]]

  * [[maximal compact subgroup]]

  * [[closed subgroup]]

  * [[loop group]]

* [[Lie group]]

## References

* {#Bredon72} [[Glen Bredon]], Chapter 0 of: _[[Introduction to compact transformation groups]]_, Academic Press  1972 ([ISBN 9780080873596](https://www.elsevier.com/books/introduction-to-compact-transformation-groups/bredon/978-0-12-128850-1), [pdf](http://www.indiana.edu/~jfdavis/seminar/Bredon,Introduction_to_Compact_Transformation_Groups.pdf))


* {#ArhangelskiiTkachenko08} Alexander Arhangel'skii, Mikhail Tkachenko, _Topological Groups and Related Structures_, Atlantis Press 2008

The following monograph is not particulary about group representations, but some content of this page is based on it:

* {#Schottenloher} [[Martin Schottenloher]], _A mathematical introduction to conformal field theory._ Springer, 2nd edition 2008 ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:1161.17014&format=complete))
 
 
[[!redirects topological groups]]

[[!redirects TopologicalGroups]]

