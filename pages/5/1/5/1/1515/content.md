
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Induction
+-- {: .hide}
[[!include induction - contents]]
=--
=--
=--

# Corecursion
* table of contents
{: toc}

## Idea

Corecursion exploits the existence of a morphism from a [[coalgebra for an endofunctor]] to a [[terminal coalgebra]] for the same endofunctor to define an operation.  It is [[duality|dual]] to [[recursion]]. See also [[coinduction]].


## Examples

\begin{example}
For the endofunctor $H(X) = 1 + X$ on [[Set]], the terminal coalgebra is $\bar{\mathbb{N}}$, the [[extended natural number system]]. Define a function $add\colon \bar{\mathbb{N}} \times \bar{\mathbb{N}} \to 1 + \bar{\mathbb{N}} \times \bar{\mathbb{N}}$:

$$
   add(n, m) =
   \begin{cases}
   (pred(n), m) & if\; n \gt 0; \\
   (0, pred(m)) & if\; n = 0,\; m \gt 0; \\
   * & if\; m = n = 0,
   \end{cases}
$$

where $pred(x)$ is as defined at [[extended natural number]].

Then $(\bar{\mathbb{N}} \times \bar{\mathbb{N}}, add)$ is an $H$-coalgebra. The unique coalgebra morphism ${+}\colon \bar{\mathbb{N}} \times \bar{\mathbb{N}} \to \bar{\mathbb{N}}$ (to the terminal coalgebra $\bar{\mathbb{N}}$) is addition on the extended natural numbers.  From this definition, we may read off these basic facts about $+$:

* $n + m \gt 0$ with $pred(n + m) = pred(n) + m$ if $n \gt 0$,
* $n + m \gt 0$ with $pred(n + m) = 0 + pred(m)$ if $n = 0$ and $m \gt 0$,
* $n + m = 0$ if $n = 0$ and $m = 0$.

(From the last two, it's immediate to prove by [[coinduction]] that $0 + m = m$ for all $m$.)
\end{example}


## Reference

* [[Jiří Adámek]], _Introduction to Coalgebra_, Theory and Applications of Categories **14** 8 (2005) 157-199 &lbrack;[tac:14-8](http://www.tac.mta.ca/tac/volumes/14/8/14-08abs.html), [pdf](http://www.tac.mta.ca/tac/volumes/14/8/14-08.pdf)&rbrack;

* Lawrence Moss, Norman Danner, _On the Foundations of Corecursion_ ([journal](http://jigpal.oxfordjournals.org/content/5/2/231), [pdf](ftp://ftp.cs.indiana.edu/pub/techreports/TR444.pdf))


[[!redirects corecursion]]
[[!redirects corecursive definition]]
[[!redirects corecursive definitions]]
