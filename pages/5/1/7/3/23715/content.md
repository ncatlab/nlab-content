
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
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

## Definition ##

### In Heyting fields

Given a [[Heyting field]] $F$, let us define the [[type]] of all [[terms]] in $F$ [[apartness|apart]] from 0:

$$F_{#0} \coloneqq \{a \in F \vert a # 0\}$$

The **reciprocal** or **reciprocal function** is a [[partial function]] $\frac{1}{-}:F_{#0} \to F$ such that for all $a \in F_{#0}$ we have $a \cdot \frac{1}{a} = 1$ and $\frac{1}{a} \cdot a = 1$

In a [[discrete field]], the reciprocal is a function $f:F \to F + 1$ defined as 

$$f(x) \coloneqq \frac{1}{x}$$

for $x \neq 0$ and 

$$f(x) \coloneqq \bot$$

for $x = 0$, where $\bot \in 1$. This is because for a [[discrete field]] $F$, the set $F_{#0} \simeq F_{\neq 0}$ is a [[decidable subset]] of $F$.  

### In dense sequentially Cauchy complete ordered integral domains

Let $R$ be a [[ordered integral domain]], and for all elements $a \in R$ and $b \in R$ let $(a, b)$ be the [[open interval|open subinterval]] containing all elements greater than $a$ and less than $b$. Then the sequences

$$f(p)(x) \coloneqq \sum_{n=0}^{p} x^n$$
$$g(p)(x) \coloneqq \sum_{n=0}^{p} (-1)^n x^n$$

indexed by natural number $p \in \mathbb{N}$ are [[Cauchy sequences]] for all elements $x \in (-1, 1)$, and if $R$ is [[sequentially Cauchy complete]], it has a limit for elements $x \in (-1, 1)$ as 

$$f_\infty(x) \coloneqq \lim_{p \to \infty} \sum_{n=0}^{p} x^n$$
$$g_\infty(x) \coloneqq \lim_{p \to \infty} \sum_{n=0}^{p} (-1)^n x^n$$

If $R$ is also [[dense]] with given element $a \in (0, 1)$, then there are sequences of sequences

$$f'(i)(p)(x) \coloneqq a^i \sum_{n=0}^{p} (-a^i)^n (x-f_\infty(-a^i+1))^n$$
$$g'(i)(p)(x) \coloneqq a^i \sum_{n=0}^{p} (-a^i)^n (x+g_\infty(a^i-1))^n$$

indexed by natural numbers $i \in \mathbb{N}$ and $p \in \mathbb{N}$, the first which is Cauchy for elements $x \in (-2 f_\infty(-a^i+1), 0)$ and the second which is Cauchy for $x \in (0, 2 g_\infty(a^i-1))$. Since $R$ is sequentially Cauchy complete, both have limits as 

$$f_\infty'(i)(x) \coloneqq \lim_{p \to \infty} a^i \sum_{n=0}^{p} (-a^i)^n (x-f_\infty(-a^i+1))^n$$
$$g_\infty'(i)(x) \coloneqq \lim_{p \to \infty} a^i \sum_{n=0}^{p} (-a^i)^n (x+g_\infty(a^i-1))^n$$

which themselves are Cauchy, and thus have limits 
$$f' '(x) \coloneqq \lim_{i \to \infty} f_\infty'(i)(x)$$
$$g' '(x) \coloneqq \lim_{i \to \infty} g_\infty'(i)(x)$$

Since both $f_\infty(-a^i+1)$ and $g_\infty(a^i-1)$ go to infinity as $i$ goes to infinity, the domain of $f' '$ is $(-\infty, 0)$ and the domain of $g' '$ is $(0, \infty)$. 

The __reciprocal__ $\frac{1}{(-)}:(-\infty, 0)\union (0, \infty) \to R$ is a piecewise defined [[partial function]] defined as 

$$
\frac{1}{x} \coloneqq 
\begin{cases}
f' '(x) & x \in (-\infty, 0) \\
g' '(x) & x \in (0, \infty)
\end{cases}
$$

Thus, every dense sequentially Cauchy complete ordered integral domain is an [[ordered field]]. 

### In sequentially Cauchy complete ordered integral rational algebras

Let $R$ be a [[ordered integral domain]] which is a [[rational algebra|$\mathbb{Q}$-algebra]], and for all elements $a \in R$ and $b \in R$ let $(a, b)$ be the [[open interval|open subinterval]] containing all elements greater than $a$ and less than $b$. Then the sequence

$$g(p)(x) \coloneqq \sum_{n=0}^{p} \frac{(-1)^n x^n}{n + 1}$$

indexed by natural number $p \in \mathbb{N}$ is a [[Cauchy sequence]] for all elements $x \in (-1, 1)$, and if $R$ is [[sequentially Cauchy complete]], it has a limit for elements $x \in (-1, 1)$ as 

$$g_\infty(x) \coloneqq \lim_{p \to \infty} \sum_{n=0}^{p} \frac{(-1)^n x^n}{n + 1}$$

There is a sequence of sequences

$$g'(i)(p)(x) \coloneqq i \sum_{n=0}^{p} \frac{(-i)^n (x+g_\infty(i-1))^n}{n + 1}$$

indexed by natural numbers $i \in \mathbb{N}$ and $p \in \mathbb{N}$, which is Cauchy for $x \in (0, 2 g_\infty(i-1))$. 

Since $R$ is sequentially Cauchy complete, the function has a limit as 

$$g_\infty'(i)(x) \coloneqq \lim_{p \to \infty} i \sum_{n=0}^{p} \frac{(-i)^n (x+g_\infty(i-1))^n}{n + 1}$$

which itself is Cauchy, and thus has a limit 
$$\ln(x) \coloneqq \lim_{i \to \infty} g_\infty'(i)(x)$$
called the [[natural logarithm]]. Since $g_\infty(a^i-1)$ goes to infinity as $i$ goes to infinity, the domain of $\ln(x)$ is $(0, \infty)$. 

The [[exponential function]] is defined as as

$$\exp(x) \coloneqq \lim_{n \to \infty} \sum_{i = 0}^{n} \frac{x^i}{i!}$$

and the reciprocal function is defined as

$$
\frac{1}{x} \coloneqq 
\begin{cases}
-\exp(- \ln(-x)) & x \in (-\infty, 0) \\
\exp(- \ln(x)) & x \in (0, \infty)
\end{cases}
$$

## See also ##

* [[Heyting field]]
* [[rational function]]
* [[reciprocal algebra]]
* [[real reciprocal function]]
* [[division]]

[[!redirects reciprocal functions]]

[[!redirects reciprocal]]
[[!redirects reciprocals]]