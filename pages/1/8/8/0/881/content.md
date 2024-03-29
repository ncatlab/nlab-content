
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

A (binary) [[relation]] $\sim$ on a set $A$ is __irreflexive__ if no element of $A$ is related to itself:
$$ \forall (x: A),\; x \nsim x .$$
(where $x\nsim x$ means that $x\sim x$ is false, i.e. that $\neg (x\sim x)$).

In the language of the $2$-poset [[Rel]] of sets and relations, a relation $R: A \to A$ is __irreflexive__ if it is [[disjoint]] from the [[identity relation]] on $A$:
$$ \id_A \cap R \subseteq \empty .$$
Of course, this containment is in fact an equality.

In [[constructive mathematics]], if $A$ is equipped with a [[tight apartness]] $\#$, we say that $\sim$ is __strongly irrelexive__ if only distinct elements of $A$ are related:
$$ \forall (x: A),\; \forall (y: A),\; x \sim y \;\Rightarrow x \# y .$$
Since $\#$ is irrelexive itself, any strongly irrelexive relation must be irrelexive.  The converse holds using [[excluded middle]], through which every set has a unique tight apartness.

## Examples

* A [[digraph]] is a graph in which the edge relation is irreflexive.

## Related concepts

* [[reflexive relation]]

[[!redirects irreflexive relation]]
[[!redirects irreflexive relations]]
[[!redirects irreflexivity]]
[[!redirects irreflexive]]

[[!redirects strongly irreflexive relation]]
[[!redirects strongly irreflexive relations]]
[[!redirects strong irreflexivity]]
[[!redirects strongly irreflexive]]
