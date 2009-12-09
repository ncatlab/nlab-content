# Definition #

A **split idempotent** in a [[category]] $C$ is a [[morphism]] $e: A \to A$ which has a [[retract]], meaning an [[object]] $B$ and morphisms $r: A \to B$ and $s: B \to A$ such that $s \circ r = e$ but $r \circ s = 1_B$.

# Remarks #

* Any split idempotent is an [[idempotent]], since
   $$ e \circ e = (s \circ r) \circ (s \circ r) = s \circ (r \circ s) \circ r = s \circ 1_B \circ r = s \circ r = e .$$

*  The splitting of an idempotent $e$ is both the [[limit]] and the [[colimit]] of the diagram containing only two [[parallel morphisms|parallel]] [[endomorphisms]] of $A$, namely $e$ and the identity.  Splittings of idempotents are preserved by any functor, making them [[absolute limit|absolute]] (co)limits.  In ordinary (i.e. [[enriched category|unenriched]]) categories, every absolute (co)limit can be constructed from split idempotents.  Thus, the [[Cauchy complete category|Cauchy completion]] of an ordinary ([[Set]]-enriched) category is just its completion under split idempotents.

* The free completion of a category under split idempotents is also called its [[Karoubi envelope]].

[[!redirects split idempotents]]
