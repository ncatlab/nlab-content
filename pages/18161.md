
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

In the theory of [[fiber bundles]] (including [[principal bundles]], [[vector bundles]], etc.) [[internalization|internal]] to [[TopologicalSpaces]] or [[SmoothManifolds]] etc., the condition that these be _locally trivial_ is typically crucial. This means that locally, i.e. over a [[neighbourhood]] of any [[point]] in their base space, these are equivalent to a [[trivial fiber bundle]], hence to the [[projection]] out of the [[Cartesian product]] of that neighbourhood with a [[fiber]]-space (the _[[typical fiber]]_).

Key implications of local triviality are:

1. the induced bundle isomorphisms between local trivializations on [[intersections]] of their open neighbourhoods give a system of [[transition functions]] which constitute the representation of the given fiber bundle as a [[cocycle]] in [[non-abelian cohomology|non-abelian]] [[Cech cohomology]]. 

1. the fact that [[Serre fibrations]] are detected locally (see [there](Serre+fibration#LocalRecognition)) implies that any local fiber bundle is a [[Serre fibration]] (and even a [[Hurewicz fibration]] if it is a [[numerable fiber bundle]]).



## Definition

### For topological fiber bundles

For $p \colon E \to X$ a [[bundles]] [[internalization|in]] [[TopologicalSpaces]], hence a [[continuous function]] between [[topological spaces]], then a _local trivialization_ is 

1. an [[open cover]] $\mathcal{U} \coloneqq \underset{i \in I}{\sqcup} U_i \longrightarrow X$ 

1. a [[topological space]] $F$, to be called the [[typical fiber]];

1. an [[isomorphism]] [[over-category|over]] $\mathcal{U}$ between the restriction of $E$ to $\mathcal{U}$ and the [[projection]] out of the [[Cartesian product]] of the cover with the typical fiber:

$$
  \array{
    U \times F 
    &\underoverset{t}{\simeq}{\longrightarrow}&
    &\longrightarrow& E
    \\
    &
    \searrow
    &
    \downarrow &{}^{{}_{(pb)}}& \downarrow^{\mathrlap{p}}
    \\
    &&
    \mathcal{U} &\longrightarrow& X
  }
$$

If this exist, then in particular the total square here is a [[pullback square]], and one says that $p$ is _locally trivializable_.

### For equivariant topological fiber bundles

For [[equivariant bundles]] one typically needs a slightly more sophisticated notion, see [there](equivariant+bundle#NotionsOfEquivariantLocalTriviality).



## References

See the references at _[[fiber bundle]]_.




[[!redirects local trivializations]]


[[!redirects locally trivial]]

[[!redirects local trivializability]]

[[!redirects local triviality]]


