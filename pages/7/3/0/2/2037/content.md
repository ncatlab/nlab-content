
# Cayley--Dickson construction
* table of contents
{: toc}

## Idea

Consider how the [[complex numbers]] are formed from the [[real numbers]].  If you generalise this carefully, then you can perform this operation again to get the [[quaternions]], and so on.  This operation is the __Cayley--Dickson construction__.


## Definitions

Let $A$ be an [[nonassociative algebra|possibly nonassociative]] $*$-[[star-algebra|algebra]] over the field $\mathbb{R}$ of [[real numbers]]: an algebra equipped with an [[involution]] $x\mapsto \bar{x}$ which is an [[antiautomorphism]].

Then one defines a new algebra, the __Cayley--Dickson double__ $A^2$ of $A$ which is the [[direct sum]] $A \oplus A$ as an $\mathbb{R}$-[[vector space]], and with the multiplication rule given by
$$
(a, b)\cdot(u,v) = (a u - \bar{v} b, b \bar{u} + v a).
$$

The map $a\mapsto (a,0)$ is a [[monomorphism]] $A\to A^2$. If $A$ is [[unital algebra|unital]] with unit $1$ then $A^2$ is unital with unit $(1,0)$. In the unital case, the element $e \coloneqq (0,1)$ has the property $e^2 = -1 \coloneqq (-1,0)$. Then the formula
$$
\widebar{a + b e} := \bar{a} - b e
$$
( _I'm assuming $e = (0,1)$, rather than $1 = (0,1)$ as before - David R_ ) defines an involutive antiautomorphism on $A^2$ and the doubling procedure can be iterated.

Regarding that $e a = \bar{a} e$, if the involution in $A$ is nontrivial then the double $A^2$ is non-[[commutative algebra|commutative]]. If $A$ is not commutative then the double is not even [[associative algebra|associative]]. However, if $A$ is associative then $A^2$ is still an [[alternative algebra]].

The standard example is the sequence of consecutive doubles starting with $\mathbb{R}$ (with the [[identity map]] as involution): the [[real number]]s $\mathbb{R}$, the [[complex number]]s $\mathbb{C}$, the [[quaternion]]s $\mathbb{H}$, the [[octonion]]s or Cayley numbers $\mathbb{O}$, the [[sedenion]]s $\mathbb{S}$, etc. These are the [[normed division algebras]], followed by further algebras which are not [[division algebras]].


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
