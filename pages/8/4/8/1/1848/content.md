
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Second-countable spaces
* table of contents
{: toc}

## Idea

A [[space]] (such as a [[topological space]]) is _second-countable_ if, in a certain sense, there is only a [[countable set|countable]] amount of information globally in its topology.  (Change 'globally' to 'locally' to get a [[first-countable space]].)


## Definitions

+-- {: .num_defn #SecondContablTopologicalSpace}
###### Definition
**(second-countable topological space)**

A [[topological space]] is __second-countable__ if it has a [[base for a topology|base for its topology]] consisting of a [[countable set]] of [[subsets]].

=--

+-- {: .num_defn}
###### Definition

A [[locale]] is __second-countable__ if there is a [[countable set]] $B$ of [[open subspaces]] (elements of the [[frame of opens]]) such that every open $G$ is a [[join]] of some [[subset]] of $B$.  That is, we have
$$ G = \bigvee \{ U\colon B \;|\; U \subseteq G \} .$$
=--


## Generalisations

The __weight__ of a space is the [[minimum]] of the [[cardinalities]] of the possible bases $B$.  We are implicitly using the [[axiom of choice]] here, to suppose that this set of cardinalities (which really is a [[small set]] because bounded above by the number of open subspaces, and [[inhabited set|inhabited]] by this number as well) has a minimum.  But without Choice, we can still consider this collection of cardinalities.

Then a second-countable space is simply one with a countable weight.


## Examples

+-- {: .num_example #SecondCountableEuclideanSpace}
###### Example
**([[Euclidean space]] is second-countable)**

Let $n \in \mathbb{N}$. Consider the [[Euclidean space]] $\mathbb{R}^n$ with its [[Euclidean norm|Euclidean]] [[metric topology]]. Then $\mathbb{R}^n$ is second countable.

A [[countable set]] of [[topological base|base open subsets]] is given by the [[open balls]] $B^\circ_x(\epsilon)$ of [[rational number|rational]] [[radius]] $\epsilon \in \mathbb{Q}_{\geq 0} \subset \mathbb{R}_{\geq 0}$ and centered at points with [[rational number|rational]] [[coordinates]]: $x \in \mathbb{Q}^n \subset \mathbb{R}^n$.

=--




+-- {: .num_example }
###### Example

A [[compact space|compact]] [[metric space]] is second-countable. 

=--

+-- {: .num_example }
###### Example

A [[separable space|separable]] [[metric space]], e.g., a [[Polish space]], is second-countable. 

=--

+-- {: .num_remark}
###### Remark

It is *not* true that separable [[first-countable spaces]] are second-countable; a counterexample is the [[real line]] equipped with the half-open or lower limit topology that has as basis the collection of half-open intervals $[a, b)$.

=--

+-- {: .num_example }
###### Example

A [[Hausdorff space|Hausdorff]] [[locally Euclidean space]] is second-countable precisely  it is [[paracompact space|paracompact]] and has a [[countable set]] of  [[connected components]]. In this case it is called a _[[topological manifold]]_.

See at _[[topological space]]_ [this prop.](#RegularityConditionsForTopologicalManifoldsComparison).

=--

+-- {: .num_example}
###### Example

A [[countable set|countable]] [[coproduct]] ([[disjoint union space]]) of second-countable spaces is second-countable. 

Countable [[products]] ([[product topological spaces]]) of second-countable spaces are second-countable. 

[[subspace|Subspaces]] of second-countable spaces are second-countable. 

=--

+-- {: .num_exampl}
###### Example

If $X$ is second-countable and there is an [[open map|open]] [[surjection]] $f \colon X \to Y$, then $Y$ is second-countable. 

=--

+-- {: .num_example }
###### Example

For second-countable [[separation axiom|T_3]] spaces $X, Y$, if $X$ is [[locally compact topological space|locally compact]], then the [[mapping space]] $Y^X$ with the [[compact-open topology]] is second-countable. 

Cf. [[Urysohn metrization theorem]] and [[Polish space]]. I ([[Todd Trimble]]) am uncertain to what extent the $T_3$ assumption can be removed. 

=--

## Properties

* [[second-countable regular spaces are paracompact]]

* [[locally compact and second-countable spaces are sigma-compact]]

## Related countability properties

[[!include topology - countability axioms]]

[[!redirects second-countable]]

## References

* {#CCGM24} [[Felix Cherubini]], [[Thierry Coquand]], [[Freek Geerligs]], [[Hugo Moeneclaey]], *A Foundation for Synthetic Stone Duality* ([arXiv:2412.03203](https://arxiv.org/abs/2412.03203))

[[!redirects second-countable space]]
[[!redirects second-countable spaces]]
[[!redirects second countable space]]
[[!redirects second countable spaces]]

[[!redirects second-countable topological space]]
[[!redirects second-countable topological spaces]]
[[!redirects second countable topological space]]
[[!redirects second countable topological spaces]]

[[!redirects second-countable locale]]
[[!redirects second-countable locales]]
[[!redirects second countable locale]]
[[!redirects second countable locales]]
