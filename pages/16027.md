
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--



# Infinite products

* table of contents
{: toc}

## Definition

An **infinite product** is a sequence of numbers (usually [[real number|real]] or [[complex number|complex]] $(a_k)_{k\in\mathbb{N}}$ written as $\prod_{k=0}^\infty a_k$.  Like an [[infinite series]], we are interested in knowing whether such a product [[convergence|converges]], and if so, what it converges to.

In a [[cartesian monoidal category]] $C$, let $(G,\cdot)$ be an multiplicative [[semigroup object]], let $(N,0,s)$ be a natural numbers object in $C$, and let $a:N\to G$ be an __sequence object__ of elements in $G$. Then there exists an sequence object $b:N\to G$ called the __infinite product object__ inductively defined by $b(0) = a(0)$ and $b(s(n)) = a(s(n)) \cdot b(n)$. The element $b(n)$ is called the __$n$-th partial product__ of the sequence $a$. 

(Another sort of infinite product is the [[cartesian product]] of an infinite family of [[sets]], or more generally [[objects]] of some [[category]].  For that notion, see [[product]].)

## Convergence

A naive definition of [[convergence]], by [[analogy]] with the [[sum]] of a [[series]], would be that $\underoverset{k=0}{\infty}{\prod} a_k = \underset{N\to\infty}{\lim} \prod_{k=0}^N a_k$ if the latter [[limit of a sequence|limit]] exists.  However, this has the flaw that it could happen that this limit exists and yet $\underset{k\to\infty}{\lim} a_k$ might not, whereas we would like to be able to say that if $\prod_{k=0}^\infty a_k$ converges then $\underset{k\to\infty}{\lim} a_k = 1$ (by analogy with the fact that if $\sum_{k=0}^\infty a_k$ converges then $\underset{k\to\infty}{\lim} a_k = 0$).  This failure can happen for two reasons:

1. If some $a_k = 0$, then $\underset{N\to\infty}{\lim} \prod_{k=0}^N a_k = 0$ since the partial products are eventually $0$, regardless of the eventual behavior of the sequence $(a_k)$.

1. If ${\vert a_k\vert}\le M\lt 1$, then $\underset{N\to\infty}{\lim} \prod_{k=0}^N a_k = 0$, whereas the sequence $(a_k)$ might approach any limit of [[absolute value]] $\lt 1$ or have no limit at all.

To avoid these "pathological" situations, we make the following modified definition.

+-- {: .num_defn}
###### Definition
Suppose at most finitely many of the $a_k$ are zero.  We say that $\prod_{k=0}^\infty a_k$ **converges** if
$$ \underset{N\to\infty}{\lim} \prod_{k=1\quad a_k\neq 0}^\infty a_k $$
exists and is nonzero.  If this is the case, we say that
$$ \prod_{k=0}^\infty a_k =
\begin{cases}
  0 &\quad \text{if some }a_k = 0\\
  \text{the above limit} &\quad\text{otherwise}
\end{cases}
$$
=--

If the above limit equals 0, one sometimes says that $\prod_{k=0}^\infty a_k$ **diverges to 0**.

## Examples

* [[Euler product]]

## Related pages

* [[series]]
* [[analytic function]]

[[!redirects infinite products]]

[[!redirects multiplicative series]]
