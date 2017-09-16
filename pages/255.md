##Definition#

A _monad_ in any [[bicategory]] $B$ is a [[monoid]] in the endomorphism category on an object of $B$.

##Explicit description#

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


## Examples

Monads on [[partial order|posets]] are particularly simple.  In fact, monads on [[power set]]s are extremely common throughout mathematics; they are known in less categorially-inclined circles as [[Moore closure]]s, and there are many examples there.

Every [[algebraic theory]] with a notion of free algebra defines a monad on [[Set]].  For example, the operation taking a set $S$ to the underlying set of the [[free group]] on $S$ may be extended to a monad.

An [[internalization|internal]] monad on the [[subobject classifier]] of a [[topos]] $E$ is a [[Lawvere-Tierney topology]] on $E$.


##Algebras over a monad#

Given that a monad in $B$ is nothing but a [[monoid]] in a hom-category $B(a,a)$, it is natural to consider [[module]]s over this monad.  This notion of module is more general than a module in a monoidal category, however, since they need not live in $B(a,a)$ but can be in $B(b,a)$ (for left modules) or $B(a,c)$ (for right modules).

In a Cat-like bicategory, left modules over a monad are usually called _algebras over the monad_.  This terminology is confusing from the point of view of monads as monoids, but is justified because in [[Cat]] itself, such algebras with domain [[terminal category|1]] are just algebras for a monad in the classical sense.  Such algebras are a powerful tool to encode general algebraic structures; this is the topic of [[universal algebra]].

Some monads arise from [[operad]]s, in which case algebras for the monad are the same as algebras for the operad.  A [[Lawvere theory]] is another special sort of monad in $Cat$.

##References#

Introductory slides:

* John Baez, [Universal Algebra and Diagrammatic Reasoning](http://math.ucr.edu/home/baez/universal/universal_hyper.pdf)


[[!redirects algebra of a monad]]
[[!redirects algebra over a monad]]