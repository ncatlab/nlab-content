
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _Stone--Weierstrass theorem_ says given a [[compact Hausdorff space]] $X$, one can uniformly approximate [[continuous functions]] $f \colon X \to \mathbb{R}$ by elements of any subalgebra that has enough elements to distinguish points. It is a far-reaching generalization of a classical theorem of Weierstrass, that real-valued continuous functions on a closed [[interval]] are uniformly approximable by [[polynomial]] functions. 


## Precise statement 

Let $X$ be a [[compact Hausdorff space|compact Hausdorff topological space]]. 

(For a [[constructive mathematics|constructive]] version take $X$ to be a compact regular [[locale]], see at *[[compactum]]*.)

Recall that $C(X)$, the [[algebra of functions|algebra of]] [[real numbers|real]]-valued [[continuous functions]]  $f \colon X \to \mathbb{R}$, is a [[commutative algebra|commutative]] (real) [[Banach algebra]] with [[unit]], under pointwise-defined addition and multiplication, and where the [[norm]] is the sup-norm 

$$
  \| f\| \;\coloneqq\; sup_{x \in X} {|f(x)|}
  \,.
$$ 

A **subalgebra** of $C(X)$ is a [[linear subspace|vector subspace]] $A \subseteq C(X)$ that is closed under the unit and algebra multiplication operations on $C(X)$. A **Banach subalgebra** is a subalgebra $A \subseteq C(X)$ which is closed as a subspace of the metric space $C(X)$ under the sup-norm metric. We say that $A \subseteq C(X)$ **separates points** if, given distinct points $x, y \in X$, there exists $f \in A$ such that $f(x) \neq f(y)$. 

+-- {: .un_thm}
###### Theorem (Stone--Weierstrass)
A subalgebra inclusion $A \subseteq C(X)$ is dense if and only if it separates points. Equivalently, a Banach subalgebra inclusion $A \subseteq C(X)$ is the identity if and only if it separates points. 
=--


## Outline of proof

* The first step is the classical Weierstrass approximation, that polynomial functions $p(x): [a, b] \to \mathbb{R}$ are dense in $C([a, b])$; without loss of generality, take $a = -\frac1{4}$ and $b = \frac1{4}$. We use the method of constructing polynomials which [[approximation of the identity|approximate the identity]] of the convolution product (the [[distribution|Dirac distribution]]). Explicitly, consider the normalizations $K_n = s_n/\|s_n\|_1$ where $s_n(x) = (1 - x^2)^n$ over $[-1, 1]$ and is compactly supported on $[-1, 1]$, so that $K_n$ approximates the Dirac distribution concentrated at 0. Given $f: [-\frac1{4}, \frac1{4}] \to \mathbb{R}$, extend to a function compactly supported on $[-\frac1{2}, \frac1{2}]$. The convolution product 
$$(K_n * f)(x) = \int_{-1}^1 K_n(x-y) f(y) d y$$ 
is polynomial (since by differentiating under the integral enough times, we eventually kill the convolving polynomial factor $K_n$), and one may verify that $(K_n * f)$ converges to $f$ in sup norm (i.e., uniformly) as $n \to \infty$, and in particular when restricted over the interval $[-\frac1{4}, \frac1{4}]$. 

Now suppose given a Banach subalgebra $A \subseteq C(X)$. 

* Given $f \in A \subseteq C(X)$, the values of $f$ are contained in some interval $[a, b]$. If polynomials $p_n$ converge to the absolute value function $|\cdot |: [a, b] \to \mathbb{R}$ in sup norm, then $p_n(f) \in A$ converges to $|f| \in C(X)$ in sup norm. Since $A$ is closed in $C(X)$ with respect to the sup-norm, it follows that $|f| \in A$. 

* Next, $A$ is partially ordered by $f \leq g$ if $f(x) \leq g(x)$ for all $x \in X$, and we claim the poset $A$ is closed under binary meets and binary joins. For, 
$$f \vee g = \frac1{2}(|f - g| + (f + g))$$ 
and $f \wedge g = -((-f) \vee (-g))$, and we showed in the last step that $A$ is closed under the operation $f \mapsto |f|$. 

Finally, suppose the Banach subalgebra $A$ separates points. Given $g \in C(X)$ and $\varepsilon \gt 0$, the last step is to show there exists $f \in A$ such that $\|f - g\| \leq \varepsilon$. 

* +-- {: .un_lemma}
  ###### Lemma
  Given $x \in X$, there exists $f_x \in A$ such that $f_x(x) = g(x)$ and $g(y) \leq f_x(y) + \varepsilon$ for all $y \in X$.
  =--
  +-- {: .proof}
  ###### Proof
  For each $y \in X$, $y \neq x$ we can choose $s \in A$ such that $s(x) \neq s(y)$, since $A$ separates points. Thus, given any $x, y$, there exist $s \in A$ and scalars $a$ and $b$ such that 
  $$a + b \cdot s(x) = g(x), \qquad a + b \cdot s(y) = g(y)$$ 
  Denote $a \cdot 1 + b s$ by $f_{x, y}$ (to indicate dependence on $x$ and $y$). For each $y$, choose a neighborhood $V_y$ so that $g(z) \leq f_{x, y}(z) + \varepsilon$ for all $z \in V_y$. Finitely many such neighborhoods $V_{y_1}, \ldots, V_{y_n}$ cover $X$; let $f_x$ be the join of $f_{x, y_1}, \ldots, f_{x, y_n}$. Then $g(y) \leq f_x(y) + \varepsilon$ for all $y \in X$. 
  =--

* Given a choice of $f_x$ for each $x \in X$, as in the preceding lemma, we may choose a neighborhood $V_x$ such that $f_x(z) - \varepsilon \leq g(z)$ for all $z \in V_x$. Finitely many such neighborhoods $V_{x_1}, \ldots, V_{x_n}$ cover $X$; let $f$ be the meet of $f_{x_1}, \ldots, f_{x_n}$. Then 
$$f(y) - \varepsilon \leq g(y) \leq f(y) + \varepsilon$$ 
for all $y \in X$, as was to be shown. 


## Variations 

There is a complex-valued version of Stone--Weierstrass. Let $C(X, \mathbb{C})$ denote the commutative $C^*$-[[C-star algebra|algebra]] of complex-valued functions $f: X \to \mathbb{C}$, where the star operation is pointwise-defined conjugation. A $C^*$-**subalgebra** is a subalgebra $A \subseteq C(X, \mathbb{C})$ which is closed under the star operation. 

+-- {: .un_thm}
###### Theorem

A $C^*$-subalgebra $A \subseteq C(X, \mathbb{C})$ is dense if and only if it separates points. 

=--

There is also a [[locally compact space|locally compact]] version. Let $X$ be a locally compact Hausdorff space and let $C_0(X)$ be the space of (say complex-valued) functions $f$ which "vanish at infinity": for every $\varepsilon \gt 0$ there exists a compact set $K \subseteq X$ such that $|f(x)| \lt \varepsilon$ for all $x$ outside $K$. Under pointwise multiplication, $C_0(X)$ is a commutative algebra _without_ unit. In fact, under the sup norm, it is a Banach algebra and even a $C^\ast$-algebra (see for instance [here](vanishing+at+infinity#FunctionsVanInftyAreCstar)). 

As before, we have a notion of subalgebra $A \subseteq C_0(X)$. 

+-- {: .un_thm}
###### Theorem
$A \subseteq C_0(X)$ is dense if and only if it separates points and for no $x \in X$ is it true that every $f \in A$ vanishes at $x$. 
=--

## References

Named after [[Karl Weierstraß]] and [[Marshall Stone]].

See alsoL

* Wikipedia: _[Stone-Weierstrass theorem](https://en.wikipedia.org/wiki/Stone%E2%80%93Weierstrass_theorem)_

Discussion in [[constructive mathematics]]:

* [[B. Banaschewski]], [[C. J. Mulvey]], *A constructive proof of the Stone-Weierstrass theorem*, J. Pure Appl. Algebra __116__ (1997) 25-40 &lbrack;<a href="https://doi.org/10.1016/S0022-4049(96)00160-0">doi:10.1016/S0022-4049(96)00160-0</a>&rbrack;


[[!redirects Stone–Weierstrass theorem]]
[[!redirects Stone--Weierstrass theorem]]
