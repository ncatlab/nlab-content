
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--



# Bounded sets
* table of contents
{: toc}

## Idea

The term 'bounded' has several meaning in different branches of mathematics.  For a general axiomatic approach to boundedness, see [[bornological set]].  Here we list definitions in various fields.


## In metric spaces

+-- {: .num_defn #metric}
###### Definition
Let $E$ be a [[metric space]].  A [[subset]] $B \subseteq E$ is **bounded** if there is some [[real number]] $r$ such that $d(x,y) \lt r$ for all $x, y \in B$.
=--

This generalises immediately to pseudometric spaces, quasimetric spaces, extended metric spaces, and most generally to [[Lawvere metric spaces]].

We can also generalise to [[gauge spaces]]:
+-- {: .num_defn #metric}
###### Definition
Let $E$ be a [[gauge space]].  A [[subset]] $B \subseteq E$ is **bounded** if there is some [[real number]] $r$ such that $d(x,y) \lt r$ for all $x, y \in B$ and all gauging distances $d$.
=--

This generalises immediately to quasigauge spaces.

The family of all bounded sets of a quasigauge space (and hence of the more particular kinds of spaces above) defines a [[bornology]] on its [[underlying set]].


## In topological vector spaces

+-- {: .num_defn #bset}
###### Definition
Let $E$ be a [[LCTVS]].  A subset $B \subseteq E$ is **bounded** if whenever $U \subseteq E$ is a [[neighbourhood]] of $0$ then there is some [[real number]] $r$ such that $B \subseteq r U$.
=--

The family of all bounded sets of a LCTVS defines a [[bornology]] on its [[underlying set]].

## Related concepts

* [[totally bounded metric space]]

* [[bounded function]]

[[!redirects bounded set]]
[[!redirects bounded sets]]
[[!redirects bounded subset]]
[[!redirects bounded subsets]]
[[!redirects bounded subspace]]
[[!redirects bounded subspaces]]
