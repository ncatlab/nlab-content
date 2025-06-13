
> This is about [[idempotent semirings]] whose addition is [[idempotent]]. For idempotent semirings whose multiplication is idempotent, see [[multiplicatively idempotent semiring]]. 

\tableofcontents

## Idea

Recall that a [[semiring]] is a set $R$ equipped with two binary operations, denoted $+$, and $\cdot$ and called _addition_ and _multiplication_, satisfying the ring (or [[rng]]) axioms except that there may or may not be either be a zero nor a negative nor an inverse, for which reason do check.

## Definition

A [[semiring]] or [[rig]] is **(additively) idempotent** (also known as a _dioid_) [[if and only if]] addition is [[idempotent]]: $x + x = x$, for all $x\in S$.

## Terminology

From now on we will assume that semirings and rigs are synonyms of each other; i.e. the semiring, $S$, has a neutral element $\varepsilon$ for + and one $e$ for $\cdot$. Moreover we assume that for all $s\in S$, $s\cdot \varepsilon =\varepsilon \cdot s = \varepsilon$, making $S$ into a [[rig]]. 

The terms *idempotent semiring* and *idempotent rig* are typically used in the literature; however, *idempotent semiring* and *idempotent rig* are sometimes also used for [[multiplicatively idempotent semirings]], and so [[idempotent semiring]] is now a disambiguation page on the nLab. In this article, we shall however use the bare *idempotent semiring* to refer to additively idempotent semirings. 

The term _dioid_ is sometimes used as an alternative name for idempotent semirings.

## Properties
 {#Properties}

On an idempotent semiring, $S$, there is a partial order given by

$$ x \leq y : \iff x + y = y. $$

To check transitivity observe that $ x \leq y $ and $ y \leq z$ imply 
$$ z \stackrel{y \leq z}{=} y + z \stackrel{x \leq y}{=} (x + y) + z = x + (y + z) \stackrel{y \leq z}{=} x + z $$
 Due to idempotence the addition is a [[join]] with respect to this partial order: take a $z$ such that $x\leq z$ and $y\leq z$, then 
$$z = z + z = x + z + y + z = x + y + z$$ 
The partial order is preserved by multiplication.

Every idempotent semiring is a [[01-bounded join-semilattice]]. 

## Examples

*  Any [[quantale]] is an idempotent semiring, or dioid, under [[join]] and multiplication.

* The set of [[language|languages]] over a given alphabet $A$ forms an idempotent semiring in which $L + L' = L \cup L'$ and multiplication is given by concatenation. In fact this is a quantale $P(A^\ast)$ where the multiplication is the $\mathbf{2}$-[[enriched category|enriched]] [[Day convolution]] product induced from the monoid multiplication of the free monoid $A^\ast$. 

* Every [[Kleene star algebra|Kleene algebra]] is an idempotent semiring. 

* Every [[distributive lattice]] is an idempotent semiring. 

* The [[tropical semiring|tropical algebra]] and the [[max-plus algebra]] are idempotent semiring.

* Given an idempotent semiring $R$ one can form the __weak interval extension__ $I(R)$. This is the idempotent semiring defined on all close [[interval|intervals]] $[x, y] = \{ z \in R \mid x \leq z \leq y \}$ by the operations $[x, y] + [x', y'] = [x + x', y + y']$ and $[x, y] \cdot [x', y'] = [x \cdot x', y \cdot y']$. The multiplicative unit is given by $[1,1]$ and, if $R$ has an additive unit $0$, an additive unit is given by $[0,0]$.

## Related concepts

* [[ring]]
* [[rig]]
* [[semiring]]
* [[idempotent semifield]]
* [[tropical semiring]]
* [[max-plus algebra]] 
* [[residuated idempotent semiring]]
* [[01-bounded semilattice]]
* [[multiplicatively idempotent semiring]]

## References

The term *(additively) idempotent semiring* appears in:

* {#Rogers24} [[Morgan Rogers]], *From free idempotent monoids to free multiplicatively idempotent rigs* &lbrack;[arXiv:2408.17440](https://arxiv.org/abs/2408.17440)&rbrack;

[[!redirects additively idempotent]]

[[!redirects additively idempotent rig]]
[[!redirects additively idempotent rigs]]

[[!redirects additively idempotent semiring]]
[[!redirects additively idempotent semirings]]

[[!redirects dioid]]
[[!redirects dioids]]
