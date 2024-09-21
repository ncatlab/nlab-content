

\tableofcontents

## Idea

In [[systems theory]], human-designed systems have designers, by definition. Components of systems interact with each other. Humans interact with each other when designing systems. Perhaps there is a connection between the structure of a system's interacting components and the structure of a system's designers.

## Definition

### Graphs

In 1968, Melvin Conway proposed **Conway's law**, stating that the [[graph]] of a system is equipped with a [[homomorphism]] to its graph of designers. Quoting ([Conway 1968](#Conway68)):

+-- {: .standout}
"Speaking as a mathematician might, we would say that there is a homomorphism from the linear graph of a system to the linear graph of its design organization."
=--

Conway argues informally as follows: a human cannot design a system component which interacts with another component without some sort of communication with that other component's designer, even indirectly through forwarded messages or documentation. As such, if any two components interact, then their designers must have communicated. Therefore the process of assigning designers to components must preserve adjacency. This assignment also is a [[function]] on vertices and therefore a [[graph homomorphism]].

Note that Conway writes of "linear graphs," which are graphs that include virtual vertices representing compositions of system components. Each virtual vertex is equivalent to a collection of edges, and the reader may verify that they are preserved by graph homomorphisms.

Also note that Conway is often ambiguous about whether graphs are directed or contain [[cycle|cycles]]. An application of Conway's law must choose [[directed graph|directed]] or undirected edges.


### Partial orders

Many organizations enforce a hierarchy. Additionally, the flow of time partially orders events. Therefore, Conway's law is often informally extended to [[poset|partial orders]]. In systems theory, the resulting preimages of [[lower set|lower sets]] are known as [[subsystem|subsystems]].


### Multigraphs

In disparate communities, there are often multiple inequivalent routes of communication. As such, Conway's law is also often extended to [[multigraph|multigraphs]]. By standard yoga, Conway's law can therefore be considered on [[category|categories]], leading to the following slogan:

+-- {: .standout}
Authorship is a functor from a system to its designers.
=--

## Properties

([Conway 1968](#Conway68)) also includes the following important corollary:

+-- {: .standout}
"To the extent that an organization is not completely flexible in its communication structure, that organization will stamp out an image of itself in every design it produces."
=--

This is seen as a constraint on what a team can build. A lone builder, working in a short span of time, has no structural limitations on what they produce. However, a highly structured team of builders, working across a long period of time where individual humans join and leave, has a large structure with many edges that each provoke a corresponding interaction in the resulting system.

Note that formally the organization actually stamps out a [[preimage]] of the homomorphism.


## Examples

[Conway 1968](#Conway68) gives the following anecdote: eight people were assigned to build two [[compiler|compilers]]. They were divided into a team of five people and a team of three people, each team producing one compiler. The five-person team produced a compiler that "ran in five phases, while the three-person team produced one that ran in three.


## References

The original paper:

* {#Conway68} [Melvin Conway](https://en.wikipedia.org/wiki/Melvin_Conway), *How Do Committees Invent?*, Datamation **14** 5 (1968) 28-31 &lbrack;[html](https://www.melconway.com/Home/Committees_Paper.html), [pdf](https://www.melconway.com/Home/pdf/committees.pdf)&rbrack;

See also:

* Wikipedia  *[Conway's law](https://en.m.wikipedia.org/wiki/Conway%27s_law)

