
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

* Strict initial objects may be understood as [[van Kampen colimits]], see e.g. [Sobocinski & Heindel (2011), Exp. 4.5 (i)](#SobocinskiHeindel11). Indeed, the van Kampen-property in this case requires that the [[slice category]] $C/\varnothing$ be [[equivalence of categories|equivalent]] to the [[terminal category]] $\mathbf{1}$.



## Examples
 {#Examples}

* The [[empty set]] is a strict initial object in [[Sets]].

* The [[empty topological space]] is a strict initial object in [[TopologicalSpaces]].

* The [[empty groupoid]] is a strict initial object in [[Groupoids]].

* The [[empty simplicial set]] is a strict initial object in [[SimplicialSets]].

* The initial objects of any of the following types of categories are strict:

  * in [[posets]],

  * in [[toposes]],

  * in [[extensive categories]],

  * in [[distributive categories]].

* Specifically the initial objects of [[Set]], [[Cat]], [[Top]] are all strict.

* [[John Baez]] showed on the [Category Theory Zulip](https://categorytheory.zulipchat.com/#narrow/stream/229199-learning.3A-questions/topic/Integers.20and.20rational.20numbers.20as.20strict.20initial.20objects.3F/near/422742440) that the [[rational numbers]] are a strict initial object in the category of [[characteristic zero]] [[fields]] and [[ring homomorphisms]]. This implies that the rational numbers are a strict initial object in the category of [[ordered fields]] and [[ring homomorphisms]]. 

At the other extreme, a [[zero object]] is a strict initial object only if the category is trivial (i.e. [[equivalence of categories|equivalent]] to the [[terminal category]]).

## Related concepts

* An [[empty bundle]] is a [[morphism]] out of a strict initial object (an [[empty morphism]]), regarded as a [[bundle]].

* [[formal dual]] concept: [[strict terminal object]]

* [[weakly initial object]]

## References

* {#CarboniLackWalters93} [[Aurelio Carboni]], [[Stephen Lack]], [[Bob Walters|R. F. C. Walters]], Def. 2.7 in: _Introduction to extensive and distributive categories_, JPAA **84** (1993) pp. 145-158 (<a href="https://doi.org/10.1016/0022-4049(93)90035-R">doi:10.1016/0022-4049(93)90035-R</a>)

Discussion as [[van Kampen colimits]]:

* {#SobocinskiHeindel11} [[Pawel Sobocinski]], [[Tobias Heindel]], Exp. 4.5 (i) in: *Being Van Kampen is a universal property*, Logical Methods in Computer Science, **7** 1 (2011) &lbrack;[arXiv:1101.4594](https://arxiv.org/abs/1101.4594), <a href="https://doi.org/10.2168/LMCS-7(1:14)2011">doi:10.2168/LMCS-7(1:14)2011</a>&rbrack;



[[!redirects strict initial objects]]
