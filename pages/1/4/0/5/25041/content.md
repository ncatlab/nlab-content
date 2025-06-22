
#Contents#
* table of contents
{:toc}

## Idea

Informally a doubly indexed category is a unitary [[double functor|lax double functor]] $F : \mathbb{C}^\top \to \mathbf{\mathbb{C}at}$, where the latter is the [[proarrow equipment]] of categories, functors, profunctors and natural transformations.

Formally, it is a right $\mathbb{C}$-module, i.e. it's a right [[action]] of the [[double category]] $\mathbb{C}$.

With this name, they were defined by [[David Jaz Myers]] in [his book on categorical system theory](#MyersBook).

## Definition

\begin{definition}
Let $\mathbb{C} = \mathbf{C}_1 \overset{s,t}\rightrightarrows \mathbf{C}_0$ be a [[double category]], presented as a [[pseudomonad]] in $\mathbf Span(Cat)$.
A *doubly indexed category* over $\mathbb{C}$ is a right $\mathbb{C}$-[[module over a monad|module]], meaning it consists of a functor $\pi : \mathbf F \to C_0$ together with a map $* : \mathbf{C}_1 \times_{C_0} \mathbf{F} \to \mathbf{F}$ over $\mathbf{C}_0$, satisfying the laws of unitality and functoriality of a module.
\end{definition}

The reason one can see this data as given by a unitary lax double functor $F : \mathbb{C}^\top \to \mathbf{\mathbb{C}at}$ is the following.
First, the data of the functor $\pi: \mathbf F \to C_0$ in itself is equivalent to that of a unitary [[lax 2-functor]] into $\mathbf{Prof}$, i.e. a [[displayed category]] (see there for an explanation). This means objects of $\mathbb{C}$ are sent to categories (the fibers of $\pi$) while horizontal maps ([[double category|tight maps]]) in $\mathbb{C}$ act 'profunctorially' on them. This assignment is unitary and lax.

Then the action $*$ gives, for each vertical morphism (loose maps) in $\mathbb{C}$, a functor. Explicitly, if $f: x \to y$ is a vertical map in $\mathbb{C}$, and $a : F(x) = \pi^{-1}(x)$, then $F(f)(a) = f * a : F(y)$.

This part of the action is strict, or at least pseudofunctorial.

## Examples

One of the central exampls of doubly indexed category is given by the 'self double-indexing' any [[finitely complete category]] $\mathbf{C}$ induces.
Specifically, it's the action $\mathbf{C}/-$ of $\mathbf{Span(C)}$.

It is defined as follows:

1. An object $x : \mathbf{C}$ is sent to the slice category $\mathbf{C}/x$
2. A morphism $f:x \to y$ is sent to the profunctor $\mathbf{C}/f: \mathbf{C}/x^{\mathrm{op}} \times \mathbf{C}/y \to \mathbf{C}$ that sends  maps $p : a \to x$, $q:b \to y$ to the set of maps $h:a \to b$ that make the square commute:
$$
\mathbf{C}/f(p, q) := \left\{ \begin{matrix} \ a & \overset{h}\to & b\ \\ p \downarrow && \downarrow q\\ x & \overset{f}\to & y\end{matrix} \right\}
$$
The laxator is defined by sending squares on $f:x \to y$ and $g:y \to z$ agreeing on their $y$ boundary to the obvious composite square lying over $f;g : x \to z$ (thus forgetting the middle boundary).
One can see this assignment is unitary, as $\mathbf{C}/1_x$ is exactly $\mathbf{C}/x(-,=)$ (the [[hom functor|identity profunctor]] on [[slice category|$\mathbf{C}/x$]]).
3. A span $x \overset{l}\leftarrow s \overset{r}\to y$ is sent to the pull-push functor $r_* l^* : \mathbf{C}/x \to \mathbf{C}/y$ which, on a map $p : a \to x$, acts first by [[pullback]] along $l$ and then post-composition it with $r$:
$$
\mathbf{C}/(l, r)(p) = \sigma_r l^*p
$$
4. On squares, it can be defined as...

## Related concepts

* [[indexed category]]

* [[double category]]

* [[module over a monad]]

* [[categorical systems theory]], [[systems theory]]

## References

* [[David Jaz Myers]], *Double Categories of Open Dynamical Systems*, EPTCS **333** (2021) 154-167 &lbrack;[arXiv:2005.05956](https://arxiv.org/abs/2005.05956), [doi:10.4204/EPTCS.333.11](https://doi.org/10.4204/EPTCS.333.11)&rbrack;

* {#MyersBook} [[David Jaz Myers]], *Categorical systems theory*, book project &lbrack;[github](https://github.com/DavidJaz/DynamicalSystemsBook/tree/master/book), [pdf](http://davidjaz.com/Papers/DynamicalBook.pdf)&rbrack;

Exposition:

* [[David Jaz Myers]], *[Categorical systems theory](https://topos.institute/blog/2021/11/categorical-systems-theory/)*, [[Topos Institute]] [Blog](https://topos.institute/blog/) (Nov 2021)

* [[David Jaz Myers]], *Double Categories of Dynamical Systems* (2020) &lbrack;[pdf](http://davidjaz.com/Talks/DJM_Dyn2020.pdf)&rbrack;

Actions of double categories are central in some approaches to [[dependent optics]]:

* [[Matteo Capucci]], *Seeing double through dependent optics* (2022), [arXiv:2204.10708](https://arxiv.org/abs/2204.10708)
