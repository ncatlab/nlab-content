
# Idempotent semirings
* table of contents
{: toc}

## Idea

Recall that a [[semiring]] is a set $R$ equipped with two binary operations, denoted $+$, and $\cdot$ and called _addition_ and _multiplication_, satisfying the ring (or [[rng]]) axioms except that there may neither be a zero nor a negative nor an inverse.


## Definition

An idempotent semiring (also known as a _dioid_) is one in which addition is [[idempotent]]: $x + x = x$, for all $x\in R$.


## Terminology

The term _dioid_ is sometimes used as an alternative name for idempotent semirings.

## Properties

On an idempotent semiring, there is a partial order given by

$$ x \leq y : \iff x + y = y. $$

To check transitivity observe that $ x \leq y $ and $ y \leq z$ imply $ z \stackrel{y \leq z}{=} y + z \stackrel{x \leq y}{=} (x + y) + z = x + (y + z) \stackrel{y \leq z}{=} x + z $. Due to idempotence the addition is a [[join]] with respect to this partial order: take a $z$ such that $x\leq z$ and $y\leq z$, then $z = z + z = x + z + y + z = x + y + z$. The partial order is preserved by multiplication.

## Examples

*  Any [[quantale]] is an idempotent semiring, or dioid, under [[join]] and multiplication.

* The set of [[language|languages]] over a given alphabet $A$ forms an idempotent semiring in which $L + L' = L \cup L'$ and multiplication is given by concatenation. In fact this is a quantale $P(A^\ast)$ where the multiplication is the $\mathbf{2}$-[[enriched category|enriched]] [[Day convolution]] product induced from the monoid multiplication of the free monoid $A^\ast$. 

*  The [[tropical semiring|tropical algebra]] and the [[max-plus algebra]] are idempotent semirings.

* Given an idempotent semiring $R$ one can form the __weak interval extension__ $I(R)$. This is the idempotent semiring defined on all close [[interval|intervals]] $[x, y] = \{ z \in R \mid x \leq z \leq y \}$ by the operations $[x, y] + [x', y'] = [x + x', y + y']$ and $[x, y] \cdot [x', y'] = [x \cdot x', y \cdot y']$. The multiplicative unit is given by $[1,1]$ and, if $R$ has an additive unit $0$, an additive unit is given by $[0,0]$.

## Related concepts

* [[ring]]
* [[rig]]
* [[idempotent semifield]]
* [[tropical semiring]]
* [[max-plus algebra]] 
* [[residuated idempotent semiring]]


[[!redirects idempotent semiring]]
[[!redirects idempotent semirings]]
[[!redirects dioid]]
[[!redirects dioids]]
