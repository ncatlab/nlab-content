+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

### Implicit definition

In [[real analysis]], the [[reciprocal]] $\frac{1}{x}$ is a [[partial function]] implicitly defined over the [[apartness|non]]-[[zero]] [[real numbers]] by the [[equation]] $x \left(\frac{1}{x}\right) = 1$. This is the definition commonly used when defining the real numbers as a [[field]]. 

### By the exponential and natural logarithm functions

The __reciprocal__ $\frac{1}{(-)}:(-\infty,0)\union(0,\infty)\to\mathbb{R}$ is piecewise defined as 

$$
\frac{1}{x} \coloneqq 
\begin{cases}
-e^{-\ln(-x)} & x \in (-\infty,0) \\
e^{-\ln(x)} & x \in (0,\infty) 
\end{cases}
$$

This definition implies that the reciprocal is [[analytic function|analytic]] in each of the two [[connected components]] of the [[domain]].


### By power series

Let us define the functions $f \colon (-1,1)\to\mathbb{R}$ and $g:(-1,1)\to\mathbb{R}$ from the [[open interval|open subinterval]] of the real numbers $(-1,1) \subset \mathbb{R}$ to the real numbers $\mathbb{R}$ as the locally [[convergence|convergent]] [[power series]]

$$
  f(x)\coloneqq \sum_{n=0}^{\infty} x^n
$$

$$
  g(x)\coloneqq \sum_{n=0}^{\infty} (-1)^n x^n
$$

The __reciprocal__ $\frac{1}{(-)}:(-\infty,0)\union(0,\infty)\to\mathbb{R}$ is then piecewise defined as 

$$
\frac{1}{x} \coloneqq 
\begin{cases}
\lim_{a\to 0^-} (-a) \sum_{n=0}^{\infty} a^n (x-f(a+1))^n & x \in (-\infty,0) \\
\lim_{a\to 0^+} a \sum_{n=0}^{\infty} (-a)^n (x+g(a-1))^n & x \in (0,\infty) 
\end{cases}
$$

Equivalently, given an element $p \in (0, 1)$, the __reciprocal__ $\frac{1}{(-)}:(-\infty,0)\union(0,\infty)\to\mathbb{R}$ is then piecewise defined as 

$$
\frac{1}{x} \coloneqq 
\begin{cases}
\lim_{i \to \infty} p^i \sum_{n=0}^{\infty} (-p^i)^n (x-f(-p^i+1))^n & x \in (-\infty,0) \\
\lim_{i \to \infty} p^i \sum_{n=0}^{\infty} (-p^i)^n (x+g(p^i-1))^n & x \in (0,\infty) 
\end{cases}
$$

This definition implies that the reciprocal is [[analytic function|analytic]] in each of the two [[connected components]] of the [[domain]].

## Related concepts

* [[logarithm]]

* [[analytic function]]

* [[limit of a function]]

* [[power series]]

* [[reciprocal function]]