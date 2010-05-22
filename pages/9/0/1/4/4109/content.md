Currying is the process of transforming a [[function]] defined on a [[cartesian product]] to a function that takes values in a [[function set]].  That is, starting with
$$ f\colon X \times Y \to Z ,$$
we __curry__ $f$ to produce
$$ \hat{f}\colon X \to Z ^ Y .$$

The above paragraph speaks of [[sets]] and functions; that is, it takes place in [[Set]].  But in fact, currying can be done in any [[closed monoidal category]].  In that case, currying transforms a [[morphism]] whose [[source]] is a [[tensor product]] to a morphism whose [[target]] is an [[internal hom]].  That is, starting with
$$ f\colon X \otimes Y \to Z ,$$
we __curry__ $f$ to produce
$$ \hat{f}\colon X \to [Y, Z] .$$

Currying is invertible and natural in $X, Y, Z$; that is, $f \mapsto \hat{f}$ is a [[natural isomorphism]] (in any closed monoidal category).  The [[inverse]] operation is, in the straightforward style of [[computer science]], called __uncurrying__.

Currying is named after [[Haskell Curry]], in accordance with [[Baez's law]], since it was invented by [[Moses Schonfinkel|Moses Schönfinkel]].