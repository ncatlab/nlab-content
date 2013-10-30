In [[homotopy type theory]], the [[introduction rule]] is a [[dependent function]] 
$$\operatorname{refl} : \prod_{a : A} \big( a =_A a \big)$$
called **reflexivity**, which says that every element of $A$ is equal to itself (in a specified way). We regard $\operatorname{refl}_a$ as being the constant path at the point $a$.

In particular, this means that if $a$ and $b$ are [[judgmentally equal]], $a \equiv b$, then we also have an element $\operatorname{refl}_a : a =_A b$. This is well-typed because $a \equiv b$ means that also the type $a =_A b$ is judgmentally equal to $a =_A a$, which is the type of $\operatorname{refl}_a$.

* From page 63 of the book, <a href="http://homotopytypetheory.org/book/">Homotopy Type Theory</a>.