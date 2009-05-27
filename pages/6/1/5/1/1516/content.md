The extended natural numbers, denoted $\bar{\mathbb{N}}$, is the set theoretic union of the natural numbers and the singleton $\{\infty\}$. It is equipped with a map $pred: \bar{\mathbb{N}} \to 1 + \bar{\mathbb{N}}$

$$
pred(x) = 
\begin{cases}
\{*\} & x = 0, \\
\n - 1 & x = n \gt 0, \\
\infty & x = \infty
\end{cases}
$$

It is a [[coalgebra]] for the endofunctor on [[Set]], $H(X) = 1 + X$, and indeed is the [[terminal coalgebra]] for $H$. 