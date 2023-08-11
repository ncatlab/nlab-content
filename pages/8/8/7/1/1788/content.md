
[[reader-writer (co)monads -- table]]

| ([[comonad|co]])[[monad]] name | [[underlying]] [[endofunctor]] | ([[comonad|co]])[[monad]] [[structure]] induced by |
|--|--|--|
| [[reader monad]] |  $W \to (\text{-})$ on [[cartesian monoidal category|cartesian]] types | [unique comonoid structure](comonoid#InACartesianMonoidalCategory) on $W$ |
| [[coreader comonad]] |  $W \times (\text{-})$ on [[cartesian monoidal category|cartesian]] types | [unique comonoid structure](comonoid#InACartesianMonoidalCategory) in $W$ |
| [[writer monad]] | $A \otimes (\text{-})$ on [[monoidal category|monoidal]] types | chosen [[monoid object|monoid structure]] on $A$ |
| [[cowriter comonad]] | $\array{A \to (\text{-}) \\ \\ A \otimes (\text{-})}$ on [[monoidal category|monoidal]] types | chosen [[monoid object|monoid structure]] on $A$ <br/><br/> chosen [[comonoid object|comonoid structure]] on $A$ |
| [[Frobenius monad|Frobenius]] (co)writer |  $\array{A \to (\text{-}) \\ A \otimes (\text{-})}$ on [[monoidal category|monoidal]] types | chosen [[Frobenius monoid|Frobenius monoid structure]] |  
