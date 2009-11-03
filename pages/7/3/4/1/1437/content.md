A __terminal coalgebra__, also called __final coalgebra__, for an [[endofunctor]] $F$ on a category $C$ is a [[terminal object]] in the category of [[coalgebra for an endofunctor|coalgebras]] of $F$.

If $F$ has a terminal coalgebra $\alpha: X \to F(X)$, then $X$ is isomorphic to $F(X)$ (see below); in this sense, $X$ is a fixed point of $F$.  Being terminal, $X$ is the largest fixed point of $F$ in that there is a map to $X$ to any other fixed point (indeed, any other coalgebra), and this map is an [[injection]] if $C$ is [[Set]].

The dual concept is [[initial algebra]]. Just as initial algebras allow for [[induction]] and [[recursion]], so terminal coalgebras allow for [[coinduction]] and [[corecursion]].

##Details##

Given two coalgebras $(x, \eta: x \to F x)$, $(y, \theta: y \to F y)$, a coalgebra map is a morphism $f: x \to y$ which respects the coalgebra structures: 

$$\theta \circ f = F(f) \circ \eta$$

A **terminal coalgebra** (usually called a _final coalgebra_ in the literature) is of course a terminal object in the category of coalgebras. Many data structures can be expressed as terminal coalgebras of suitable endofunctors; a simple but useful theorem says that terminal coalgebras $x$ are "fixed points" of their endofunctors, in that $F x \cong x$. This is the dual form of a theorem discovered long ago by Lambek: 

+-- {: .un_theorem}
###### Theorem

If $(x, \theta: x \to F x)$ is a terminal object in the category of $F$-coalgebras, then $\theta$ is an isomorphism. 
=--

+-- {: .proof}
###### Proof

Define a coalgebra structure on $F x$ by $F\theta: F x \to F F x$. By terminality of $x$, there is a unique coalgebra map $f: F x \to x$. We claim this is inverse to $\theta$. Indeed, by how we defined the coalgebra structure on $F x$, it is tautological that $\theta$ is a coalgebra map. By terminality of $x$ again, this gives an equation of coalgebra maps:

$$f \circ \theta = 1_x.$$

On the other hand, 

$$\theta \circ f = F(f) \circ F(\theta) = F(f \circ \theta) = F(1_x) = 1_{F x}$$

where the first equation holds because $f$ is a coalgebra map. This completes the proof.
=--

To construct terminal coalgebras, the following result is useful and practical: 

+-- {: .un_theorem}
###### Theorem (Adamek)

If $C$ has a terminal object $1$ and the limit $L$ of the diagram 

$$\ldots F^3 1 \stackrel{F^2 !}{\to} F^2 1 \stackrel{F !}{\to} F 1 \stackrel{!}{\to} 1 \qquad (1)$$ 

exists in $C$ and $F$ preserves this limit, then the limit 
carries a structure of terminal coalgebra. 
=--

+-- {: .proof}
###### Proof

Let $\pi_n: L \to F^n 1$ be the $n^{th}$ projection of the limiting cone. Then we have a cone from $F L$ to the diagram (1) whose components are 

$$F L \stackrel{F\pi_n}{\to} F^{n+1} 1 \stackrel{F^n !}{\to} F^n 1$$ 

and the induced map $F L \to L$ to the limit is invertible by hypothesis; let $\theta: L \to F L$ be the inverse. We claim the coalgebra $(L, \theta)$ is terminal. 

Indeed, suppose $(x, \eta: x \to F x)$ is any coalgebra. We recursively define maps $f_n: x \to F^n 1$: let $f_0: x \to 1$ be the unique map, and 

$$f_{n+1} = F(f_n) \circ \eta$$ 

It is easily checked by induction that these maps define a cone from $x$ to the diagram (1), and so we get a map $f: x \to L$. (More later)
=--