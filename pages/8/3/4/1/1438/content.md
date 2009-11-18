An __initial algebra__ for an [[endofunctor]] $F$ on a category $C$ is an [[initial object]] in the category of [[algebra|algebras]] of $F$.

If $F$ has an initial algebra $\alpha: F(X) \to X$, then $X$ is isomorphic to $F(X)$ via $\alpha$; this is **Lambek's theorem**.  In this sense, $X$ is a fixed point of $F$.  Being initial, $X$ is the *smallest* fixed point of $F$ in that there is a map from $X$ to any other fixed point (indeed, any other algebra), and this map is an [[injection]] if $C$ is [[Set]]. 

The dual concept is [[terminal coalgebra]], which is the *largest* fixed point of $F$.


##Proof of Lambek's theorem##  

+-- {: .proof}
Given an initial algebra structure $\alpha: F(X) \to X$, define an algebra structure on $F(X)$ to be $F(\alpha): F(F(X)) \to F(X)$. By initiality, there exists an $F$-algebra map $i: X \to F(X)$, so that 

$$\array{
F(X) & \overset{F(i)}{\to} & F(F(X)) \\
\alpha \downarrow & & \downarrow F(\alpha) \\
X & \underset{i}{\to} & F(X)
}$$ 

commutes. Now it is trivial, in fact tautological that $\alpha$ is itself an $F$-algebra map $F(X) \to X$. Thus $\alpha \circ i = 1_X$, since both sides of the equation are $F$-algebra maps $X \to X$ and $X$ is initial. As a result, $F(\alpha) \circ f(i) = 1_{F(X)}$, so that $i \circ \alpha = 1_{F(X)}$ according to the commutative square. Hence $\alpha$ is an isomorphism, with inverse $i$.
=--

##Examples## 

* Let $A$ be a set, and let $F: Set \to Set$ be the functor $F(X) = 1 + A \times X$. Then the initial $F$-algebra is $A^*$, the free monoid on $A$. The $F$-algebra structure is 
$$(e, m| ): 1 + A \times A^* \to A^*$$ 
where $e: 1 \to A^*$ is the identity and $m|: A \times A^* \to A^*$ is the restriction of the monoid multiplication along the evident inclusion $i \times 1: A \times A^* \to A^* \times A^*$. 

This "fixed point" of $F$ can be thought of as the result of the (slightly nonsensical) calculation 

$$1 + A \times X = X \Rightarrow X = \frac1{1 - A} = 1 + A + A^2 + \ldots = A^*$$ 

which can be made more rigorous by interpreting the initial equality as defining the solution $X$ by recursion. 

* Let $F: Set \to Set$ be the functor $F(X) = 1 + X^2$. Then the initial $F$-algebra is the set $T$ of (isomorphism classes of) finite (planar, rooted) binary trees. The $F$-algebra structure is 
$$(r, j): 1 + T^2 \to T$$ 
where $r: 1 \to T$ names the tree consisting of just a root vertex, and $j: T^2 \to T$ creates a tree $t \vee t'$ from two trees $t$, $t'$ by joining their roots to a new root, so that the root of $t$ becomes the left child and the root of $t'$ the right child of the new root. 

_To be continued_