
> This article is about Boolean semirings as defined by Fernando Guzmán. For other notions of "Boolean rig" or "Boolean semiring", see [[Boolean semiring]]. 

----

\tableofcontents

## Definition

A **Boolean semiring** or **Boolean rig** is a [[multiplicatively idempotent semiring]] such that $1 + x + x = 1$. 

## Properties

### Commutativity

\begin{theorem}
Every Boolean semiring is [[commutative rig|commutative]]. 
\end{theorem}

\begin{proof}
By definition of a Boolean semiring, we have $1 + x + x = 1$, and by commutativity and associativity of $+$, we have $x + x + 1 = 1$. In addition, for all elements $x$ and $y$, we have 
$$
\begin{array}{c}
x y = x y (1 + x + x) = x (y + y x + y x) \\
= x ((y + y x)^2 + y x) = x (y + y x + y x + y x y + y x) \\
= x (y + y x y + y x) = x y + x y x y + x y x = x y x y + x y x y + x y x
= x y x ( y + y + 1) = x y x
\end{array}
$$
and
$$
\begin{array}{c}
y x = (x + x + 1) y x = (x y + x y + y) x \\
= (x y + (x y + y)^2) x = (x y + y x y + x y + x y + y) x \\
= (x y + y x y + y) x = x y x + y x y x + y x = x y x + y x y x + y x y x
= (y + y + 1) x y x = x y x
\end{array}
$$
Thus, we have $x y = y x$, showing that Boolean semirings are commutative. 
\end{proof}

### Join, meet, and negation operators

Even without subtraction, we may define the join operation $x \vee y \coloneqq x + x y + y$. We can prove that multiplication distributes over join, meaning that multiplication and join together form another rig structure. But we cannot prove that this semiring is also Boolean, or that join is a [[semilattice]] operation; in fact, if the Boolean semiring is a [[distributive lattice]], then the "join" operation defined above is the same as the addition operation. 

## Examples

The main examples are probably [[distributive lattices]].  In this case, the join operation called $\vee$ above will match the original join/addition operation called $+$ above.

Of course, a [[Boolean ring]] is a Boolean semiring, since any ring is a rig. However, since it\'s also a distributive lattice, a Boolean ring is actually a Boolean semiring in two different ways.

## Related concepts

* [[semiring]], [[rig]]

* [[multiplicatively idempotent semiring]]

* [[Boolean algebra]]

* [[Boolean ring]]

## References

* [[Fernando Guzmán]], *The variety of Boolean semirings*, Journal of Pure and Applied Algebra, Volume 78, Issue 3, 20 April 1992, Pages 253-270 &lbrack;<a href="https://doi.org/10.1016/0022-4049(92)90108-R">doi:10.1016/0022-4049(92)90108-R</a>&rbrack;

* [[Morgan Rogers]], *From free idempotent monoids to free multiplicatively idempotent rigs* &lbrack;[arXiv:2408.17440](https://arxiv.org/abs/2408.17440)&rbrack;

* [[J-B Vienney]], *Are Boolean rigs commutative?*, Category theory Zulip, ([web](https://categorytheory.zulipchat.com/#narrow/channel/266967-deprecated.3A-mathematics/topic/Are.20boolean.20rigs.20commutative.3F))

[[!redirects Boolean semiring (Guzmán)]]
[[!redirects Boolean semirings (Guzmán)]]
[[!redirects boolean semiring (Guzmán)]]
[[!redirects boolean semirings (Guzmán)]]

[[!redirects Boolean rig (Guzmán)]]
[[!redirects Boolean rigs (Guzmán)]]
[[!redirects boolean rig (Guzmán)]]
[[!redirects boolean rigs (Guzmán)]]