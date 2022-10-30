
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Burali-Forti\'s paradox
* table of contents
{: toc}

## Summary

**Burali-Forti's paradox** is a [[paradox]] of naive [[material set theory|material]] [[set theory]] that was first observed by [[Cesare Burali-Forti]].  However, the paradox is not specific to material set theory and can be formulated in [[structural set theory]] or in [[type theory]].  When formulated in [[type theory]], it is often called **Girard's paradox** after [[Jean-Yves Girard]] (see at _[[type of types]]_).


## The paradox

Suppose that there were a [[set]] $Ord$ of all [[ordinal numbers]].  One could then prove that

1. The set $Ord$ is [[well-ordering|well-ordered]] by the relation $\lt$ on ordinals.
2. Thus, its [[order type]], call it say $\Omega$, is itself an ordinal number.
3. Thus $\Omega$ is an element of $Ord$, which implies $\Omega\lt\Omega$.
4. But this is provably impossible for any ordinal number.

There are many variations of the paradox, depending for instance on what precise definition of "well-ordered" (and "ordinal number") one chooses.


## In type theory: Girard's paradox
 {#GirardParadox}

As formulated in [[type theory]] by [[Jean-Yves Girard]], the Burali-Forti paradox shows that the original version of [[Per Martin-Löf]]'s type theory, which allowed a [[type of types]] $Type$ containg itself as a [[term]] $Type \colon Type$, is [[inconsistency|inconsistent]], in the precise sense that it contains (non-normalizing) [[proofs]] of [[false]].

Moreover, by an adaptation of the proof, one can construct a [[looping combinator]] in this type theory, which implies the [[decidability|undecidability]] of type-checking.


## Related entries

* [[Russell's paradox]]

* [[Cantor's paradox]]

## References

Girard's paradox is discussed in 

* {#MartinLoef74} [[Per Martin-Löf]], section 1.9, p. 7 of  _An intuitionistic theory of types: predicative part_, In Logic Colloquium (1973), ed. H. E. Rose and J. C. Shepherdson (North-Holland, 1974), 73-118. ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.131.926))

category: paradox

[[!redirects Burali-Forti paradox]]
[[!redirects Burali-Forti Paradox]]
[[!redirects Burali-Forti's paradox]]
[[!redirects Burali-Forti's Paradox]]
[[!redirects Burali-Forti's paradox]]
[[!redirects Burali-Forti's Paradox]]
[[!redirects Burali-Forti\'s paradox]]
[[!redirects Burali-Forti\'s Paradox]]

[[!redirects Girard paradox]]
[[!redirects Girard Paradox]]
[[!redirects Girard's paradox]]
[[!redirects Girard's Paradox]]
[[!redirects Girard's paradox]]
[[!redirects Girard's Paradox]]
[[!redirects Girard\'s paradox]]
[[!redirects Girard\'s Paradox]]
