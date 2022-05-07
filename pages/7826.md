
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
* table of contents
{:toc}

## Definition

+-- {: .num_defn}
###### Definition

A ([[topological space|topological]]) [[space]] whose only [[connected topological space|connected]] [[subspaces]] are [[singletons]] is called *totally disconnected*.
=--

## Examples

+-- {: .num_example}
###### Example

[[discrete space|Discrete spaces]] are totally disconnected.

=--

+-- {: .num_example #RationalNumbersAreTotallyDisconnected}
###### Example
**(the rational numbers are totally disconnected)**

The [[rational numbers]] $\mathbb{Q} \subset \mathbb{R}$ equipped with their [[subspace topology]] inherited from the [[Euclidean space|Euclidean]] [[metric topology]] on the [[real numbers]], form a totally disconnected space.

=--

+-- {: .proof}
###### Proof

By construction, a [[base for a topology|base for the topology]] is given by the open subsets which are restrictions of [[open intervals]] of real numbers to the rational numbers

$$
  (a,b)_{\mathbb{Q}} \coloneqq (a,b) \cap \mathbb{Q}
$$

for $a \lt b \in \mathbb{R}$.

Now for any such $a \lt b$ there exists an [[irrational number]] $r \in \mathbb{R}\backslash \mathbb{Q}$ with $a \lt r \lt b$. This being irrational implies that $(a,r)_{\mathbb{Q}} \subset \mathbb{Q}$ and $(r,b)_{\mathbb{Q}} \subset \mathbb{Q}$ are disjoint subsets. Therefore every basic open subset is the disjoint union of (at least) two open subsets:

$$
  (a,b)_{\mathbb{Q}} = (a,r)_{\mathbb{Q}} \cup (r,b)_{\mathbb{Q}}
  \,.
$$

Hence no [[inhabited set|inhabited]] open subspace of the rational numbers is connected.

=-- 

+-- {: .num_example #limits} 
###### Example 
A [[product]] in $Top$ of totally disconnected spaces is totally disconnected. A subspace of a totally disconnected space is totally disconnected. Hence [[limits]] in $Top$ of diagrams of totally disconnected spaces are totally disconnected. 
=-- 

For example, the [[Baire space]] of [[irrational numbers]] is [[homeomorphism|homeomorphic]] to a [[countable set|countable]] [[product space]] $\mathbb{N}^\mathbb{N}$ (via [[continued fractions]]), so it is totally disconnected. Similarly, [[Cantor space]] $2^\mathbb{N}$ is totally disconnected. Another notable special case of the preceding class of examples is the following. 

+-- {: .num_example}
###### Example

Every [[profinite group]] is totally disconnected and in particular the set of [[p-adic number|p-adic numbers]] is totally disconnected. 

=-- 

See also _[[Stone space]]_. 


* [[extremally disconnected topological space|extremally disconnected]] Hausdorff space


## Properties 

The general class of examples in Example \ref{limits} may be seen in the following light. 

+-- {: .num_theorem} 
###### Theorem 
The [[category]] of totally disconnected spaces and continuous maps is a [[reflective subcategory]] of [[Top]]. 
=-- 

+-- {: .proof} 
###### Proof 
The reflector takes a space $X$ to the space of connected components, i.e., the [[quotient space]] $X/\sim$ of $X$ where $\sim$-equivalence classes are precisely the connected components of $X$. We check that connected components $C$ of $X/\sim$ are singletons. Let $q: X \to X/\sim$ be the quotient map; it suffices to check that $q^{-1}(C) \subseteq X$ is connected (because then $q^{-1}(C)$ is contained in a single $\sim$-equivalence class, making $C = q q^{-1}(C)$ a single point). So, suppose the (closed) set $q^{-1}(C)$ is a disjoint union $K_1 + K_2$ of closed sets $K_1, K_2$; we are required to show one or the other is empty. For each $c \in C$, the inverse image $q^{-1}(\{c\})$ is connected, hence we must have $q^{-1}(\{c\}) \subseteq K_1$ or $q^{-1}(\{c\}) \subseteq K_2$. Thus we can partition $C$ into sets 

$$C_1 \coloneqq \{c \in C: q^{-1}(\{c\}) \subseteq K_1\}, \qquad C_2 \coloneqq \{c \in C: q^{-1}(\{c\}) \subseteq K_2\}$$ 

and we observe $q^{-1}(C_1) = K_1$ and $q^{-1}(C_2) = K_2$. By definition of quotient topology, since $K_1, K_2$ are closed we infer $C_1, C_2$ are closed. They are also disjoint and $C = C_1 + C_2$, so by connectedness of $C$ either $C_1 = \emptyset$ or $C_2 = \emptyset$, and therefore $K_1 = q^{-1}(C_1)$ or $K_2 = q^{-1}(C_2)$ is empty, as required. 

Finally, given a continuous map $f: X \to Y$ with $Y$ totally disconnected, each connected component $C$ of $X$ is mapped to a connected set $f(C)$ of $Y$ which is a singleton by total disconnectedness of $Y$, and so we get a (unique) factoring through a map $X/\sim \to Y$, continuous of course by virtue of the quotient topology. This completes the proof. 
=-- 


## Related concepts

* [[locally connected topological space]]

* [[extremally disconnected topological space]] 

* [[connected space]] 

[[!redirects totally disconnected spaces]]

[[!redirects totally disconnected topological space]]
[[!redirects totally disconnected topological spaces]]
[[!redirects totally disconnected]]
