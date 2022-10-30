
# Cayley--Dickson construction
* table of contents
{: toc}

## Idea

Consider how the [[complex numbers]] are formed from the [[real numbers]].  If you generalise this carefully, then you can perform this operation again to get the [[quaternions]], and so on.  This operation is the __Cayley--Dickson construction__.


## Definitions

Let $A$ be an [[nonassociative algebra|possibly nonassociative]] $*$-[[star-algebra|algebra]] over the field $\mathbb{R}$ of [[real numbers]]: an algebra equipped with an [[involution]] $x\mapsto \bar{x}$ which is an [[antiautomorphism]].  (Actually, $\mathbb{R}$ could be replaced by any [[commutative ring]] in the definitions, although some properties may depend on this ring.)

Then one defines a new algebra, the __Cayley--Dickson double__ $A^2$ of $A$ which is the [[direct sum]] $A \oplus A$ as an $\mathbb{R}$-[[vector space]], and with the multiplication rule given by
$$
(a,b)\cdot(u,v) \coloneqq (a u - \bar{v} b, b \bar{u} + v a),
$$
and the formula
$$
\widebar{(a,b)} := (\bar{a},-b)
$$
defines an involutive antiautomorphism on $A^2$, so the doubling procedure can be iterated.

The map $a\mapsto (a,0)$ is a [[monomorphism]] $A\to A^2$. If $A$ is [[unital algebra|unital]] with unit $1$ then $A^2$ is unital with unit $(1,0)$. In the unital case, the element $\mathrm{i} \coloneqq (0,1)$ has the property $\mathrm{i}^2 = -1 \coloneqq (-1,0)$, and we may write $(a,b)$ as $a + b \mathrm{i}$ (while $a + \mathrm{i} b = (a,\bar{b})$).  For this reason, we may write $A[\mathrm{i}]$ in place of $A^2$, at least when $A$ is unital.


## Properties

Generally speaking, the double $A^2$ of an algebra $A$ has a nice property iff $A$ is one level nicer.  For simplicity, assume that $A$ is unital (so that $\mathbb{R}$ is a subalgebra).  Since $\bar{\mathrm{i}} = -\mathrm{i}$, we see that the involution on $A^2$ is trivial iff the involution on $A$ is trivial and $A$ further has $2 = 0$.  Since $\mathrm{i} a = \bar{a} \mathrm{i}$, $A^2$ is [[commutative algebra|commutative]] iff $A$ is commutative and the involution in $A$ is trivial.  Since $a (b \mathrm{i}) = (b a) \mathrm{i}$, $A^2$ is [[associative algebra|associative]] iff $A$ is associative and commutative. Finally, $A^2$ is [[alternative algebra|alternative]] iff $A$ is associative (and hence also alternative).


## Examples

The standard example is the sequence of consecutive doubles starting with $\mathbb{R}$ itself (with the [[identity map]] as involution); these are the __Cayley--Dickson algebras__: the [[real number]]s $\mathbb{R}$, the [[complex number]]s $\mathbb{C}$, the [[quaternion]]s $\mathbb{H}$, the [[octonion]]s or Cayley numbers $\mathbb{O}$, the [[sedenion]]s $\mathbb{S}$, etc. These are the [[normed division algebras]] ($\mathbb{R}$, $\mathbb{C}$, $\mathbb{H}$, and $\mathbb{O}$), followed by further algebras which are not [[division algebras]].  All of these algebras are [[power-associative algebra|power-associative]] and unital and have all [[inverse elements]]; the subalgebra with $\bar{x} = x$ is always just $\mathbb{R}$.


## References

*  [[M M Postnikov]], _Lectures on geometry, Semester V: Lie groups and Lie algebras_, Lec. 14 (russian and english editions)

*  [[John Baez]], [The Cayley--Dickson construction](http://math.ucr.edu/home/baez/octonions/node5.html)

*  John Baez, [This Week's Finds --- Week 59](http://math.ucr.edu/home/baez/week59.html)


[[!redirects Cayley-Dickson construction]]
[[!redirects Cayley–Dickson construction]]
[[!redirects Cayley--Dickson construction]]

[[!redirects Cayley-Dickson double]]
[[!redirects Cayley–Dickson double]]
[[!redirects Cayley--Dickson double]]
[[!redirects double of an algebra with involution]]
[[!redirects double of algebra with involution]]
[[!redirects doubles of algebras with involution]]
[[!redirects double of a star-algebra]]
[[!redirects doubles of star-algebras]]
[[!redirects double of a *-algebra]]
[[!redirects doubles of *-algebras]]

[[!redirects Cayley-Dickson algebra]]
[[!redirects Cayley-Dickson algebras]]
[[!redirects Cayley–Dickson algebra]]
[[!redirects Cayley–Dickson algebras]]
[[!redirects Cayley--Dickson algebra]]
[[!redirects Cayley--Dickson algebras]]
