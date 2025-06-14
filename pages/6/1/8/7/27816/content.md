
\tableofcontents

## Idea

The [[axiom schema]] of __subset collection__ combines fullness with the [[axiom schema of collection]] to apply in the situations where fullness is used.  In the presence (I think) of either collection or [[full separation]], subset collection is equivalent to fullness.

## Statement

See [Aczel & Rathjen 2001](#AczelRathjen01) for the time being.

## Relation to type theory

Subset collection is justified by predicative versions of constructive [[type theory]] in the sense of Martin--L&#246;f or Thierry Coquand.  To see this, note that these theories justify [[COSHEP]]; their types define (not sets in general but) _[[presets]]_ (following Bishop) or _[[completely presented sets]]_, which (as sets) are projective.  Analogously, an element of $F_{X,Y}$ may be considered an _operation_ or _prefunction_ (following 'preset') from $X$ to $Y$.

But note that the type of prefunctions from $X$ to $Y$, like the preset underlying $X$, is a categorical (unique) construction in type theory, while $F_{X,Y}$, like COSHEP, is not.  Thus type theory (or rather preset theory) gives us constructions that are not available in set theory (even with fullness or even COSHEP), such as the predicate that states whether two functions have equal underlying prefunctions.

## Related concepts

* [[axiom of fullness]]

* [[axiom schema of collection]]

* [[CZF]]

## References

* {#AczelRathjen01} [[Peter Aczel]], [[Michael Rathjen]], _Notes on Constructive Set theory_, 2001 ([pdf](https://events.math.unipd.it/3wftop/pdf/AczelRathjen.pdf), [[AczelRathjenCST.pdf:file]])

[[!redirects axiom of subset collection]]
[[!redirects axiom schema of subset collection]]
[[!redirects subset collection]]