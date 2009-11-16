An __initial algebra__ for an [[endofunctor]] $F$ on a category $C$ is an [[initial object]] in the category of [[algebra|algebras]] of $F$.

If $F$ has an initial algebra $\alpha: F(X) \to X$, then $X$ is isomorphic to $F(X)$ (**Lambek's theorem:** $\alpha$ is an isomorphism); in this sense, $X$ is a fixed point of $F$.  Being initial, $X$ is the smallest fixed point of $F$ in that there is a map from $X$ to any other fixed point (indeed, any other algebra), and this map is an [[injection]] if $C$ is [[Set]]. 

The dual concept is [[terminal coalgebra]].

##Proof of Lambek's theorem##  

Given an initial algebra structure $\alpha: F(X) \to X$, define an algebra structure on $F(X)$ to be $F(\alpha): F(F(X)) \to F(X)$. By initiality, there exists an $F$-algebra map $i: X \to F(X)$, so that 

$$\array{
F(X) & \overset{F(i)}{\to} & F(F(X)) \\
\alpha \downarrow & & \downarrow F(\alpha) \\
X & \underset{i}{\to} & F(X)
}$$ 

commutes. Now it is trivial, in fact tautological that $\alpha$ is itself an $F$-algebra map $F(X) \to X$. Thus $\alpha \circ i = 1_X$, since both sides of the equation are $F$-algebra maps $X \to X$ and $X$ is initial. As a result, $F(\alpha) \circ f(i) = 1_{F(X)}$, so that $i \circ \alpha = 1_{F(X)}$ according to the commutative square. Hence $\alpha$ is an isomorphism, with inverse $i$. $\Box$
