
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A _topological group_ is a [[topological space]] with a continuous [[group]] structure: a [[group object]] in the [[category]] [[Top]].

## Definition

A **topological group** is an [[internalization|internal]] [[group object]] in the category of [[topological space|topological spaces]].

More explicitly, it is a group equipped with a topology such that the multiplication and inversion maps are continuous.

## Uniform structure

A topological group $G$ carries two canonical [[uniform space|uniformities]]: a right and left uniformity. The **left uniformity** consists of entourages $\sim_{l, U}$ where $x \sim_{l, U} y$ if $x y^{-1} \in U$; here $U$ ranges over neighborhoods of the identity that are symmetric: $g \in U \Leftrightarrow g^{-1} \in U$. The **right uniformity** similarly consists of entourages $\sim_{r, U}$ where $x \sim_{r, U} y$ if $x^{-1} y \in U$. The uniform topology for either coincides with the topology of $G$. 

Obviously when $G$ is commutative, the left and right uniformities coincide. They also coincide if $G$ is compact Hausdorff, since in that case there is only one uniformity whose uniform topology reproduces the given topology. 

Let $G$, $H$ be topological groups, and equip each with their left uniformities. Let $f: G \to H$ be a group homomorphism. 

+-- {: .un_prop}
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

in other words such that $x \sim_U y \Rightarrow f(x) \sim_V f(y)$. Hence $f$ is uniformly continuous with respect to the left uniformities. By similar reasoning, $f$ is uniformly continuous with respect to the right uniformities.
=--


## Unitary representation on Hilbert spaces

**Definition.** A unitary [[representation]] $R$ of a topological group $G$ in a [[Hilbert space]] $\mathcal{H}$ is a continuous [[homomorphism]]

$$
   R: G \to \mathcal{U}(\mathcal{H})
$$

where $\mathcal{U}(\mathcal{H})$ is the group of [[unitary operator]]s on $\mathcal{H}$ with respect to the strong topology.

Note that $\mathcal{U}(\mathcal{H})$ is a complete, metrizable topological group in the strong topology, see proposition 3.11 in the book by Schottenloher cited in the references.

In physics, when a classical system is symmetric, i.e. invariant in a proper sense, with respect to the action of a topological group $G$, then an unitary representation of $G$ is often called a **quantization** of $G$.

### Why the strong topology is used

The reason that in the definition of an unitary representation, the strong operator topology on $\mathcal{U}(\mathcal{H})$ is used and not the norm topology, is that only few homomorphisms turn out to be continuous in the norm topology.

Example: let $G$ be a compact [[Lie group]] and $L^2(G)$ be the Hilbert space of square integrable measurable functions with respect to its [[Haar measure]]. The right regular representation of $G$ on $L^2(G)$ is defined as
$$
      R: G \to \mathcal{U}(L^2(G))
$$
$$
         g \mapsto (R_g: f(x) \mapsto f(x g))
$$
and this will generally not be continuous in the norm topology, but is always continuous in the strong topology. 

## Related concepts

* [[group]]

* **topological group**

* [[Lie group]]

## References

The following monograph is not particulary about group representations, but some content of this page is based on it:

* Martin Schottenloher: _A mathematical introduction to conformal field theory._ Springer, 2nd edition 2008 ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:1161.17014&format=complete))

[[!redirects topological groups]]