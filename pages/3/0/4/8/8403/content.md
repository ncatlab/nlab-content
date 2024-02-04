
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# First-countable spaces
* table of contents
{: toc}

## Idea

A [[space]] (such as a [[topological space]]) is _first-countable_ if, in a certain sense, there is only a [[countable set|countable]] amount of information locally in its topology.  (Change 'locally' to 'globally' to get a [[second-countable space]].)


## Definitions

+-- {: .num_defn}
###### Definition

A [[topological space]] is __first-countable__ if every [[point]] $x$ has a [[countable set|countable]] [[local basis]] $B_x$.
=--


## Generalizations

The __character__ of a space at a point $x$ is the [[minimum]] of the [[cardinalities]] of the possible bases $B_x$.  We are implicitly using the [[axiom of choice]] here, to suppose that this set of cardinalities (which really is a [[small set]] because bounded above by the number of [[neighbourhoods]] of $x$, and [[inhabited set|inhabited]] by this number as well) has a minimum.  But without Choice, we can still consider this collection of cardinalities.

Then a first-countable space is simply one whose characters are all countable.

The __character__, tout court, of a space is the [[supremum]] of the characters of its points; then a first-countable space is simply one with a countable character.


## Related countability properties

[[!include topology - countability axioms]]

## Related concepts

* [[sigma-topological space]]

* [[sigma-frame]]


[[!redirects first-countable space]]
[[!redirects first-countable spaces]]
[[!redirects first countable space]]
[[!redirects first countable spaces]]

[[!redirects first-countable topological space]]
[[!redirects first-countable topological spaces]]
[[!redirects first countable topological space]]
[[!redirects first countable topological spaces]]
