## Definition

A **reflexive pair** is a [[parallel pair]] $f,g\colon A\rightrightarrows B$ having a common [[section]], i.e. a map $s\colon B\to A$ such that $f s = g s = 1_B$.  A **reflexive coequalizer** is a [[coequalizer]] of a reflexive pair.  A category **has reflexive coequalizers** if it has coequalizers of all reflexive pairs.

A reflexive coequalizer in $C^{op}$ is called a *coreflexive equalizer* in $C$.

## Remarks

* Reflexive coequalizers should not be confused with [[split coequalizers]], a distinct concept.

* Any [[congruence]] is a reflexive pair, so in particular any [[quotient object|quotient]] of a congruence is a reflexive coequalizer.

## Applications

* Reflexive coequalizers figure in the [[crude monadicity theorem]].

* A theorem of Fred Linton states that if $T$ is a [[monad]] on a [[cocomplete category]] $C$, then the category $C^T$ of [[Eilenberg-Moore algebras]] is cocomplete if and only if it has reflexive coequalizers.  This is the case particularly if $T$ preserves reflexive coequalizers.

* If $F\colon C\times D\to E$ is a functor of two variables which preserves reflexive coequalizers in each variable separately (that is, $F(c,-)$ and $F(-,d)$ preserve reflexive coequalizers for all $c\in C$ and $d\in D$), then $F$ preserves reflexive coequalizers in both variables together.  (This is emphatically *not* the case for arbitrary coequalizers.)

  This result is particularly interesting when $F$ is the [[tensor product]] of a cocomplete [[closed monoidal category]].  In this case it implies that the free [[monoid]] monad on such a category preserves reflexive coequalizers, and thus (by Linton's theorem) the category of monoids is cocomplete.

## References

* F.E.J. Linton, "Coequalizers in categories of algebras"

[[!redirects reflexive coequalizers]]
[[!redirects reflexive coequaliser]]
[[!redirects coreflexive equalizer]]
[[!redirects coreflexive equaliser]]
[[!redirects reflexive coequalisers]]
[[!redirects coreflexive equalizers]]
[[!redirects coreflexive equalisers]]
