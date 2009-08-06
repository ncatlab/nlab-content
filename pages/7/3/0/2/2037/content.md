Let $A$ be a [[nonassociative algebra]] over the field $\mathbb{R}$ of real numbers equipped with an [[involution]] $x\mapsto \bar{x}$ which is an involutive antiautomorphism. Then one defines a new algebra, the __double__ $A^2$ of $A$ which is the [[direct sum]] $A\oplus A$ as an $\mathbb{R}$-vector space, and with the multiplication rule given by
$$
(a, b)\cdot(u,v) = (a u - \bar{v} b, b \bar{u} + v a).
$$
The map $a\mapsto (a,0)$ is a [[monomorphism]] $A\to A^2$. If $A$ is unital with unit $1$ then $A^2$ is unital with unit $(1,0)$. In the unital case, the element $e:=(0,1)$ has the property $e^2 = -1 = (-1,0)$. Then the formula
$$
\widebar{a + b e} := \bar{a} - b e
$$
defines an involution in $A^2$ and the doubling procedure can be iterated.

Regarding that $e a = \bar{a} e$, if the involution in $A$ is nontrivial then the double $A^2$ is noncommutative. If $A$ is not commutative then the double is not even associative. If $A$ is associative then $A^2$ is still an [[alternative algebra]].

The standard example is the sequence of consecutive doubles starting with $\mathbb{R}$ (with trivial involution): the [[real number]]s $\mathbb{R}$, the [[complex number]]s $\mathbb{C}$, the [[quaternion]]s $\mathbb{H}$, the [[octonion]]s or Cayley numbers $\mathbb{O} = \mathbb{Ca}$, the [[sedenion]]s $\mathbb{Ca}^2$, etc. 


## References

*  [[M M Postnikov]], _Lectures on geometry, Semester V: Lie groups and Lie algebras_, Lec. 14 (russian and english editions)
*  [TWF Week 59](http://math.ucr.edu/home/baez/week59.html)


[[!redirects double of an algebra with involution]]
[[!redirects double of algebra with involution]]