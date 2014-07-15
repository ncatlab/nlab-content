
#Contents#
* table of contents
{:toc}


## Definition

+-- {: .num_defn #Pseudogroup}
###### Definition

A **[[pseudogroup]]** on a [[topological space]] (or [[locale]]) $X$ is a [[groupoid]] $G$ each of whose [[objects]] is an [[open subset]] of $X$, and whose [[morphisms]] are [[homeomorphisms]] between such open sets, satisfying the following conditions:

* The objects [[cover]] $X$. (Equivalently, in light of the last axiom, every open set of $X$ is an object of $G$.)
* If $g: V \to W$ belongs to $G$ and $U \subseteq V$ is an open set, then the restriction $g|_U: U \to g(U)$ belongs to $G$. (Equivalently, in light of the other axioms, every inclusion map $id|_U: U \to V$ belongs to $G$.)
* ([[sheaf]] property) If $g: U \to V$ is a homeomorphism and if there is a covering $U_\alpha$ of $U$ such that the restrictions $g|_{U_\alpha}: U_\alpha \to g(U_\alpha)$ are morphisms of $G$, then $g$ is also morphism of $G$.

=--

+-- {: .num_example}
###### Example

Commonly used choices for $X$ in def. \ref{Pseudogroup} include 

* the [[Cartesian space]] $\mathbb{R}^n$ (for real manifolds)

* the [[complex plane]] $\mathbb{C}^n$ (for [[complex manifolds]])

* the half-space $H^n = \{(x_1, \ldots, x_n) \in \mathbb{R}^n: x_1 \geq 0\}$ (for [[manifolds with boundary]])

* the $n$-[[cube]] $I^n = [0, 1]^n$. 

=--

## Related concepts

* [[manifold]]

## References

The concept was introduced in

* [[Élie Cartan]], _Sur la structure des groupes infinis de transformation (suite)_ Ann. Sci. &#201;cole Norm. Sup. (3), 22:219&#8211;308, 1905.

Discussion in a context of [[étale groupoids]]/[[étale stacks]] is in 

* {#Carchedi12} [[David Carchedi]], _&#201;tale Stacks as Prolongations_ ([arXiv:1212.2282](http://arxiv.org/abs/1212.2282))

[[!redirects pseudogroups]]
