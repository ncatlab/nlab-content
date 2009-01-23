The term **exact category** has several different meanings.  Perhaps this should eventually be a disambiguation page, but right now it is about exact categories in the sense of Barr (also called "effective regular categories").

## Definition ##

An **exact category** (in the sense of Barr) is a [[regular category]] in which every [[equivalence relation]] is a [[kernel pair]] (that is, every equivalence relation is _effective_).

Exact categories are also called **effective regular categories**.

## Consequences ##

If $R\hookrightarrow X\times X$ is an equivalence relation which is the kernel pair of $f:X \to Y$, then if $f = m p$ is the image factorization of $f$, one can show that $p$ is a [[coequalizer]] of $R$.  (Therefore, equivalence relations have [[quotient object|quotient]]s in an exact category.)  However the converse is not true: there are regular categories having all coequalizers which are not exact.

## Examples ##

* Any [[topos]] is an exact category.

* Any category which is [[monad|monadic]] over a power of [[Set]] is exact.

* One can construct, for any regular category $C$, a "free" exact category $C_{ex/reg}$ on $C$ by adjoining formal quotients for equivalence relations.  One way to define $C_{ex/reg}$ is as the (locally discrete) [[2-category]] whose objects are equivalence relations in $C$ and whose morphisms are [[anafunctor|anafunctors]].  If $C$ is already exact, then $C_{ex/reg}$ is equivalent to $C$.

* Similarly, one can construct the "free" exact category $C_{ex/lex}$ on any category $C$ with finite limits, or even with [[weak limit|weak finite limits]].  The exact categories of the form $C_{ex/lex}$ for a category $C$ with weak finite limits are exactly those which have [[projective object|enough (regular) projectives]]; in this case the projective objects are the retracts of objects of $C$ (Carboni-Vitale 1998).

# References #

Carboni, A. and Vitale, E. M.  Regular and exact completions, _JPAA_ 125, 1998.
