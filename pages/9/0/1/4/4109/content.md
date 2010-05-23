Currying is a process of transforming an operation on two variables into an operation on one variable.  The term is used in [[computer science]] and the [[lambda calculus]], where it is often technically important to have operations that act on only one variable at a time.  But [[category theory]] also recognises it as a [[natural isomorphism]] in a [[closed monoidal category]].

The [[inverse]] operation is, in the straightforward style of [[computer science]], called __uncurrying__.

Currying is named after [[Haskell Curry]], in accordance with [[Baez's law]], since it was invented by [[Moses Schonfinkel|Moses Schönfinkel]]. (Perhaps Curry helped popularize the application to lambda calculus?)


## Definitions

Since most people are familiar with [[Set]], we work there first.  In $Set$, currying transforms a [[function]] defined on a [[cartesian product]] to a function that takes values in a [[function set]].  That is, starting with
$$ f\colon X \times Y \to Z ,$$
we __curry__ $f$ to produce
$$ \hat{f}\colon X \to Z ^ Y $$
according to the formula 
$$\hat{f}(x) = (y \mapsto f(x, y)).$$


### In lambda calculus and CCCs

Similarly, in [[lambda calculus]], currying is a device which reduces the study of functions in several arguments to functions in one argument. For example, if $\phi$ is a lambda term in which variables $x$ and $y$ occur freely (so that $\phi$ is effectively a "function" of $x$ and $y$), the lambda calculus syntax favors the currified expression $\lambda x. \lambda y. \phi$, which denotes the intuitive expression $x \mapsto (y \mapsto \phi)$, where one abstracts variables one at a time. 

Later it was observed (by Lawvere) that this is just a special case of a more general "curryfication" for [[cartesian closed categories]] (such as [[Cat]] or a [[nice category of spaces]]), where one has a natural bijection of morphisms: 

$$\frac{X \times Y \to Z}{X \to Z^Y}$$

Indeed, cartesian closed categories are models for lambda calculus.


### In general

In fact, currying can be done in any (right) [[closed monoidal category]].  In that case, currying transforms a [[morphism]] whose [[source]] is a [[tensor product]] to a morphism whose [[target]] is an [[internal hom]].  That is, starting with
$$ f\colon X \otimes Y \to Z ,$$
we __curry__ $f$ to produce
$$ \hat{f}\colon X \to [Y, Z] .$$

Currying is invertible and natural in $X, Y, Z$; that is, $f \mapsto \hat{f}$ is a [[natural isomorphism]] (in any closed monoidal category).  


## Currying in which variable(s)?

By convention, currying is always done on the *last* variable.  This fits in very nicely with a convention that products associate on the left while internal homs associate on the right.  More explicitly, if we use (as is common in computer science) '$\times$' for the product (even if it is not cartesian) and '$to$' for the internal hom (so that we must use another symbol, say '$\vdash$', for the external hom), then we need no parentheses to generalise currying
$$ f\colon X \times Y \vdash Z $$
to produce
$$ \hat{f}\colon X \vdash Y \to Z ;$$
by currying several $n-1$ times in succession, we turn
$$ f\colon X_1 \times \cdots \times X_n \vdash Z $$
into
$$ \hat{\overset\vdots{\hat{f}}}\colon X_1 \vdash X_2 \to \cdots \to X_n \to Z .$$
This does not generalise to $n = 0$, which is one way to see that even the untyped lambda calculus actually has two objects, one of which is a [[terminal object]] $1$ and one of which can play every other role.

In a closed [[braided monoidal category]] (such as a closed [[symmetric monoidal category]], and including the cartesian closed categories such as $Set$ and the models of lambda calculus), we can also 'curry through the first variable' or 'co-curry' to produce a map
$$ \check{f}\colon Y \vdash X \to Z ,$$
but computer scientists (or even mathematicians who are being very careful) will see this as a composite operation whose first step is [[composition]] with the [[braiding]] $Y \times X \vdash X \times Y$.

In a left closed monoidal category, currying does not exist, but cocurrying does.  Perhaps the product should associate on the right in a left closed monoidal category?