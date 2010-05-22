Currying is the process of transforming a [[function]] defined on a [[cartesian product]] to a function that takes values in a [[function set]].  That is, starting with
$$ f\colon X \times Y \to Z ,$$
we __curry__ $f$ to produce
$$ \hat{f}\colon X \to Z ^ Y $$
according to the formula 
$$\hat{f}(x) = (y \mapsto f(x, y)).$$

Similarly, in [[lambda calculus]], currying is a device which reduces the study of functions in several arguments to functions in one argument. For example, if $\phi$ is a lambda term in which variables $x$ and $y$ occur freely (so that $\phi$ is effectively a "function" of $x$ and $y$), the lambda calculus syntax favors the currified expression $\lambda x. \lambda y. \phi$, which denotes the intuitive expression $x \mapsto (y \mapsto \phi)$, where one abstracts variables one at a time. 

Later it was observed (by Lawvere) that this is just a special case of a more general "curryfication" for cartesian closed categories (such as [[Cat]] or a [[nice category of spaces]]), where one has a natural bijection of morphisms: 

$$\frac{X \times Y \to Z}{X \to Z^Y}$$

The above paragraphs take place in cartesian closed categories such as [[Set]] and models for lambda calculus, but in fact, currying can be done in any [[closed monoidal category]].  In that case, currying transforms a [[morphism]] whose [[source]] is a [[tensor product]] to a morphism whose [[target]] is an [[internal hom]].  That is, starting with
$$ f\colon X \otimes Y \to Z ,$$
we __curry__ $f$ to produce
$$ \hat{f}\colon X \to [Y, Z] .$$

Currying is invertible and natural in $X, Y, Z$; that is, $f \mapsto \hat{f}$ is a [[natural isomorphism]] (in any closed monoidal category).  The [[inverse]] operation is, in the straightforward style of [[computer science]], called __uncurrying__.

Currying is named after [[Haskell Curry]], in accordance with [[Baez's law]], since it was invented by [[Moses Schonfinkel|Moses Schönfinkel]]. (Perhaps Curry helped popularize the application to lambda calculus?) 
