
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[empty set]], among all sets, has two characteristic properties:

1. there is a *unique* [[function]] *out* of the empty set, to any other set;

1. there is *no* [[function]] *to* the empty set, except from itself.

The first property generalizes to arbitrary [[categories]] as the property of an *[[initial object]]*.

The corresponding generalization including also the second property is that of a *strict initial object*:


## Definition

An [[initial object]] $\varnothing$ is called a **strict initial object** if every [[morphism]] [[codomain|to]] $\varnothing$ is an [[isomorphism]]:

\[
  \label{MorphismToStrictInitialObjectIsIsomorphism}
  X \overset{f}{\longrightarrow} \varnothing
  \;\;\;\;\;\;\;\;\;
    \Rightarrow
  \;\;\;\;\;\;\;\;\;
  X \underoverset{\simeq}{f}{\longrightarrow} \emptyset
  \,.
\]


## Properties
 {#Properties}

* The [[Cartesian product]] of any [[object]] $X$ with a strict initial object is isomorphic to the strict initial object, $X \times \varnothing \simeq \varnothing$, because the [[projection]] $pr_1 \colon \varnothing \times X \to \varnothing$ exists by definition of Cartesian products, whence (eq:MorphismToStrictInitialObjectIsIsomorphism) implies that it is an isomorphism 

  $$
    \varnothing \times X 
      \underoverset
        {\;\;\;\simeq\;\;\;}
        {pr_1}
        {\longrightarrow} 
    \varnothing
    \,.
  $$



## Examples
 {#Examples}

The [[empty set]] is a strict initial object in [[Sets]].

The [[empty topological space]] is a strict initial object in [[TopologicalSpaces]].

The [[empty groupoid]] is a strict initial object in [[Groupoids]].

The initial objects of any of the following types of categories are strict:

* in [[posets]]

* in [[toposes]] 

* in [[extensive categories]] 

* in [[distributive categories]].

At the other extreme, a [[zero object]] is only a strict initial object if the category is trivial (equivalent to the [[terminal category]]).

## Related concepts

* An [[empty bundle]] is morphism out of a strict initial object (an [[empty morphism]]), regarded as a [[bundle]].

* [[formal dual]] concept: [[strict terminal object]]

[[!redirects strict initial objects]]
