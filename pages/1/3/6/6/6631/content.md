## Idea

The *Hausdorff metric* is a [[metric space|metric]] on the set of [[subsets]] of a given [[metric space]].

## Definition

Let $A$ be a [[metric space]], regarded as a [[category]] [[enriched category|enriched]] over $V = [0,\infty]$ (a [[Lawvere metric space]]).  The enriched [[functor category]] $[A,V]$ is, concretely, the set of distance-nonincreasing functions $A\to [0,\infty]$ with the [[supremum metric]], and the contravariant [[Yoneda embedding]] $A^{op}\to [A,V]$ sends $a$ to $d(a,-)$.

Now, for any subset $X \subseteq A$, each point $x\in X$ gives rise to the representable $d(x,-)$, and we can define the functor $d(X,-):A\to V$ to be the [[coproduct]] these representables over all $x\in X$.  Concretely, this means

$$d(X,a)=inf_{x\in X} d(x,a).$$

Note that if $X$ is [[closed subset|closed]], then it can be recovered from $d(X,-)$ as the set of points $x$ such that $d(X,x)=0$.  If $X$ is not closed, then in this way we recover its [[closure]].

Finally, since $[A,V]$ is also a Lawvere metric space, we obtain an induced metric on the set of subspaces of $A$:

$$d(X,Y) = d(d(X,-), d(Y,-)).$$

This metric is not symmetric; its [[symmetrization of a metric|symmetrization]] is the **Hausdorff metric**.  Equivalently, we could start out by considering instead the functor category $[A, V_{sym}]$ where $V_{sym}$ is the symmetrization of $V = [0,\infty]$.

## References

* _Taking categories seriously_, Reprints in Theory and Applications of Categories, No. 8, 2005, pp. 1&#8211;24. ([pdf](http://www.emis.de/journals/TAC/reprints/articles/8/tr8.pdf))
