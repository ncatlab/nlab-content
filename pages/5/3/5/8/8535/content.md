
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

**Burali-Forti's paradox** is a [[paradox]] of naive [[material set theory|material]] [[set theory]] that was first observed by [[Cesare Burali-Forti]].  However, the paradox is not specific to material set theory and can be formulated in [[structural set theory]] or in [[type theory]].  When formulated in type theory, it is often called **Girard's paradox** after [[Jean-Yves Girard]].


## The paradox

Suppose that there were a [[set]] $Ord$ of all [[ordinal numbers]].  One could then prove that

1. The set $Ord$ is [[well-ordering|well-ordered]] by the relation $\lt$ on ordinals.
2. Thus, its [[order type]], call it say $\Omega$, is itself an ordinal number.
3. Thus $\Omega$ is an element of $Ord$, which implies $\Omega\lt\Omega$.
4. But this is provably impossible for any ordinal number.

There are many variations of the paradox, depending for instance on what precise definition of "well-ordered" (and "ordinal number") one chooses.


## In type theory: Girard's paradox

As formulated in [[type theory]] by [[Jean-Yves Girard]], the Burali-Forti paradox shows that the original version of [[Per Martin-Löf]]'s type theory, which allowed $Type:Type$, is [[inconsistency|inconsistent]], in the precise sense that it contains (non-normalizing) [[proofs]] of [[false]].

Moreover, by an adaptation of the proof, one can construct a [[looping combinator]] in this type theory, which implies the [[decidability|undecidability]] of type-checking.


## Related entries

* [[Russell's paradox]]


[[!redirects Burali-Forti paradox]]
[[!redirects Burali-Forti's paradox]]
[[!redirects Burali-Forti's paradox]]
[[!redirects Girard paradox]]
[[!redirects Girard's paradox]]
[[!redirects Girard's paradox]]
