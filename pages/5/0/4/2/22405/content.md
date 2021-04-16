
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

In as far as a general [[bundle]] over some base [[object]] $B$ is a [[morphism]] $E \to B$ into $B$, out of some "total space" [[object]] $E$, the *empty bundle* over $B$ is the one whose total space is "[[strict initial object|empty]]", hence whose projection map is the [[empty function]].

## Definition

In [[TopologicalSpaces]] an empty bundle has the [[empty topological space]] as its total space, while in [[SimplicialSets]] the empty bundle has the the [[empty simplicial set]] as its total space, etc.:

$$
  \array{
    \varnothing
    \\   
    \big\downarrow
    \\
    B
    \mathrlap{\,.}
  }
$$

Generally, one may speak of empty bundles [[internalization|internal]] to any ambient [[category]] in which the [[initial object]] is *[[strict initial object|strict]]* (e.g. any [[topos]]) in that every [[morphism]] to the [[initial object]] is an [[isomorphism]], so that

\[
  \label{InitialObjectIsEmpty}
  \exists 
  \big(
    X \overset{}{\rightarrow} \varnothing
  \big)
  \;\;\;\;\;
  \Leftrightarrow
  \;\;\;\;\;
  X \simeq \varnothing
  \,.
\]

## Properties

### In topological spaces
 {#InTopologicalSpaces}

In [[TopologicalSpaces]], any empty bundle 

* is a [[locally trivial]] [[fiber bundle]] with [[typical fiber]] the [[empty topological space]],

  because any [[product topological space]] with the [[empty topological space]] is itself empty:

  $$
    B \times \varnothing \;\simeq\; \varnothing
  $$

* is a [[Serre fibration]] (in fact a [[Hurewicz fibration]]),

  because none of the [[commuting squares]] that one would have to [[lifting property|lift in]] actually exist, by (eq:InitialObjectIsEmpty):

  $$
    \array{
      D^{n} &\overset{ \not \exists }{\longrightarrow}& \varnothing
      \\
      \big\downarrow && \big\downarrow
      \\
      D^n \times I &\longrightarrow& B
    }
  $$

### In simplicial sets
 {#InSimplicialSets}

Similarly, in [[SimplicialSets]] every empty bundle 

* is a [[Kan fibration]],

  since none of the [[commuting squares]] that one would have to [[lifting property|lift in]] actually exist, by (eq:InitialObjectIsEmpty):


  $$
    \array{
      \Lambda_k^n &\overset{ \not \exists }{\longrightarrow}& \varnothing
      \\
      \big\downarrow && \big\downarrow
      \\
      \Delta^n &\longrightarrow& B
    }
  $$

  (keeping in mind that the [0-simplex has no horns](horn#ZeroSimplexHasNoHorns), hence that all [[horns]] are [[inhabited set|inhabited]]).

## Application

### In equivariant bundle theory

Empty fiber bundles play a central role in the context of [[equivariant bundles]], where they frequently appear as [[fixed loci]] of non-empty bundles.


## Related concepts

[[!include empty objects -- contents]]

[[!redirects empty bundles]]
