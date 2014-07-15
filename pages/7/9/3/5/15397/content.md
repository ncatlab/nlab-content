
#Contents#
* table of contents
{:toc}


## Definition

+-- {: .num_defn #Pseudogroup}
###### Definition

A **[[pseudogroup]]** (also called transformation pseudogroup) on a [[topological space]] (or [[locale]]) $X$ is a [[groupoid]] $G$ each of whose [[objects]] is an [[open subset]] of $X$, and whose [[morphisms]] are [[homeomorphisms]] between such open sets, satisfying the following conditions:

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

More generally, an abstract pseudogroup is a sub-[[inverse semigroup]] of the inverse semigroup of partial bijections of a set (or, even more generally, local automorphisms of an object in more general context).

## Related concepts

* [[manifold]]
* [[inverse semigroup]]

## References

The concept was introduced in

* {#Cartan05} [[Élie Cartan]], _Sur la structure des groupes infinis de transformation (suite)_ Ann. Sci. &#201;cole Norm. Sup. (3), 22:219&#8211;308, 1905 ([Numdam](http://www.numdam.org/item?id=ASENS_1904_3_21__153_0))

* {#Cartan09} [[Élie Cartan]], _Les groupes de transformations continus, infinis, simples_. Annales Scientifiques de l'&#201;cole Normale Sup&#233;rieure 26: 93&#8211;161, 1909 ([Numdam](http://www.numdam.org/item?id=ASENS_1909_3_26__93_0))


* {#Golab39} St. Golab, _&#220;ber den Begriff der "Pseudogruppe von Transformationen"_ Mathematische Annalen 116: 768&#8211;780 (1939)

Discussion in the broader context of [[étale groupoids]]/[[étale stacks]] is in 

* {#Carchedi12} [[David Carchedi]], _&#201;tale Stacks as Prolongations_ ([arXiv:1212.2282](http://arxiv.org/abs/1212.2282))

See also

* Wikipedia, _[Pseudogroup](http://en.wikipedia.org/wiki/Pseudogroup)_

Abstract pseudogroups are studied in [[inverse semigroup]] literature, e.g.

* [[Mark V. Lawson]], _Inverse semigroups: the theory of partial symmetries_, World Scientific, 1998.

[[!redirects pseudogroups]]
[[!redirects pseudogroup of transformations]]