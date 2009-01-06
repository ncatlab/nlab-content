#Definition#

A _monad_ in any [[bicategory]] $B$ is a [[monoid]] in the endomorphism category on an object of $B$.

#Explicit description#

This means that a monad is

* an object $a$ of $B$;

* an [[endomorphism]] $a \stackrel{A}{\to} a$ on $a$;

* a 2-morphism 
$$
  \array{
    &&
    a
    \\
    & 
    {}^A\nearrow &\Downarrow^\mu& \searrow^A
    \\
    a
    &&\stackrel{A}{\to}&&
    a
  }
$$

* and a 2-morphism
$
  i : Id_a \Rightarrow A
$

* such that

  * $\mu$ is associative in the obvious sense;

  * $\mu$ is unital with respect to $i$ in the obvious sense.


##Remarks##

* Originally monads were conceived and defined for $B =$ [[Cat]]. In parts of the literature "monad" still exclusively means monad in $Cat$. Similarly for algebras over monads.
Monads in $Cat$ are sometimes, mostly in older literature, also called **triple**s (alluding to the triple of data $(A,\mu,i)$). 


* We can picture a monad in $B$ as an image of the [[oriental|third oriental]] in $B$. See the remarks at [[monoidal category]].


#Algebra over a monad#

Given that a monad in $B$ is nothing but [[monoid]] in $B$, it is natural to consider [[module]]s over this monad. Such modules are called _algebras over the monad_.

This terminology is confusing from the point of view of monads as monoids, but justifies itself from the fact that modules for monads in [[Cat]] are a powerful tool to encode general algebraic structures. This is the topic of [[universal algebra]]. An alternative way of talking about monads and their algebras is [[operad]]s and _their_ algebras.

#References#

Introductory slides:

* John Baez, [Universal Algebra and Diagrammatic Reasoning](http://math.ucr.edu/home/baez/universal/universal_hyper.pdf)