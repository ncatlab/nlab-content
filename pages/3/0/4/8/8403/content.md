
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

## Examples

* The [[real numbers]] are a first-countable space with respect to the [[Euclidean topology]]. 

## Related countability properties

[[!include topology - countability axioms]]

## Related concepts

* [[sigma-topological space]]

* [[sigma-frame]]

## References

The real numbers are a first-countable space according to:

* {#BFS19} Martin E. Bidlingmaier, Florian Faissole, [[Bas Spitters]], *Synthetic topology in Homotopy Type Theory for probabilistic programming*. Mathematical Structures in Computer Science, 2021;31(10):1301-1329. &lbrack;[doi:10.1017/S0960129521000165](https://doi.org/10.1017/S0960129521000165), [arXiv:1912.07339](https://arxiv.org/abs/1912.07339)&rbrack;

[[!redirects first-countable]]

[[!redirects first-countable space]]
[[!redirects first-countable spaces]]
[[!redirects first countable space]]
[[!redirects first countable spaces]]

[[!redirects first-countable topological space]]
[[!redirects first-countable topological spaces]]
[[!redirects first countable topological space]]
[[!redirects first countable topological spaces]]
