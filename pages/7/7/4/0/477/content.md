# Definition #

In a [[category]], a **product** (also called a **cartesian product**) of two [[object|objects]] $X$ and $Y$ is an object $X\times Y$ equipped with [[morphism|morphisms]] $p:X\times Y \to X$ and $q:X\times Y \to Y$, called **projections**, such that for any object $Z$ equipped with maps $f:Z\to X$ and $g:Z\to Y$ there exists a unique $h:Z\to X\times Y$ (called the __[[pairing]]__ of $f$ and $g$) such that $p \circ h=f$ and $q \circ h=g$.

# Remarks #

* When they exist, products are unique up to unique canonical isomorphism, so we often say "[[generalized the|the]] product."
* One can define in a similar way a product of any family of objects.  A product of the [[empty set|empty]] family is a [[terminal object]].
* A product is a special case of a [[limit]] in which the domain category is [[discrete category|discrete]].
* A product in $C$ is the same as a [[coproduct]] in its [[opposite category]] $C^{op}$.
* A product created by the [[forgetful functor]] of a [[concrete category]], especially in algebra, is often called a [[direct product]].

# Demonstration #

* [This interactive demonstration](http://www.j-paine.org/cgi-bin/webcats/set_prod_nlab.php) in the category of finite sets lets you type two sets and see a product, showing the unique map to it from a randomly chosen $Z$ equipped with $f$ and $g$. It also generates a second product, showing the unique canonical isomorphism between this and the first product.

[[!redirects products]]