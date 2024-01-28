
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

\tableofcontents

## Idea ##

Given an integer $n$, The different types of $n$-th [[root]] [[partial functions]] on the [[real numbers]] that satisfy the [[functional equation]] $f(x)^n = x$ on some [[subset]] of the real numbers. 

## Definition ##

Let us define the real numbers to be a [[sequentially Cauchy complete]] Archimedean ordered field, since that is the minimum requirement for which the inverse function theorem is true. 

There exists an $n$-th root function for every integer $n \in \mathbb{Z}$ apart from zero, defined on the positive real numbers by the equation:

$$0 \lt \vert n \vert \vdash \sqrt[n]{x} \coloneqq \exp(\frac{1}{n} \ln(x))$$

Now, assume that $n \gt 1$. Then one could extend the $n$-th root function to a function defined on the half-open interval $[0, \infty)$. Let us define continuous functions $f_k:[0, \infty) \to [0, \infty)$: 
$$f_k(x) = \begin{cases}
1/n^k & \mathrm{when}\; x \leq 1/n^{2 k} \\
\exp(\frac{1}{n} \ln(x)) & \mathrm{when}\; x \geq 1/n^{2 k} \\
\end{cases}$$
As stated, that requires knowing whether $x \leq 1/n^{2 k}$ or $x \geq 1/n^{2 k}$, but it is possible to work around this by patching three functions together:

 * $f^{0}_k:[0,1/n^{2 k}) \to \mathbb{R}$ is the linear function $f(x) = n^k x$,
 * $f^{+}_k:(0,\infty) \to \mathbb{R}$ is defined as $\min(n^k x,\exp(\frac{1}{n} \ln(x)))$.

Since these functions agree on their overlap, and their domains comprise all of $[0, \infty)$ we do get a total function $f_k:[0, \infty) \to [0, \infty)$ as a result. 

Now the sequence of functions $(f_k)_{k=0}^\infty$ so defined converges uniformly on any bounded interval to a continuous function $\sqrt[n]{(-)}:[0, \infty) \to [0, \infty)$ called the **principal nth root** function. It is easily seen that $(\sqrt[n]{x})^n = x$ and $\sqrt[n]{x^n} = x$. 

Additionally, if $n$ is an odd integer greater than 1, then there exist $n$-th root functions defined on the entirety of the real numbers. 

Let us patch this sequence of triples of functions together:

 * $f^{-}_k:(-\infty,0) \to \mathbb{R}$ is defined as $\max(-n^k x,-\exp(\frac{1}{n} \ln(-x)))$
 * $f^{0}_k:(-1/n^{2 k},1/n^{2 k}) \to \mathbb{R}$ is the linear function $f(x) = n^k x$,
 * $f^{+}_k:(0,\infty) \to \mathbb{R}$ is defined as $\min(n^k x,\exp(\frac{1}{n} \ln(x)))$.

Since these functions agree on their overlap, and their domains comprise all of $\mathbb{R}$ we do get a total function $f_k:\mathbb{R} \to \mathbb{R}$ as a result. 

Now the sequence of functions $(f_k)_{k=0}^\infty$ so defined converges uniformly on any bounded interval to a continuous function $\sqrt[n]{(-)}:\mathbb{R} \to \mathbb{R}$ called the **nth root** function for odd integer $n$. It is easily seen that $(\sqrt[n]{x})^n = x$ and $\sqrt[n]{x^n} = x$. 

## Other nth root functions

According to ([Richman 2012](#Richman12)), given the existence of an nth root function, there are an uncountable number of functions that satisfy the [[functional equation]] $f(x)^n = x$ on some [[subset]] of the [[real numbers]]. Each of these could be called a real "nth root function". 

For example, let $1_{\mathbb{Q}}:\mathbb{R} \to \mathbb{R}$ be the constructive Dirichlet indicator function, defined as $1_{\mathbb{Q}}(x) \coloneqq 1$ for every rational number $q \in \mathbb{Q}$, and $1_{\mathbb{Q}}(x) \coloneqq 0$ for every real number $x$ apart from every rational number $q \in \mathbb{Q}$ 

$$\forall q \in \mathbb{Q}. \vert x - q \vert \gt 0$$

Then the function $f(x) \coloneqq (-1)^{1_{\mathbb{Q}}(x)} \sqrt[n]{x}$ is a real nth root function, even though it is nowhere continuous, and not defined on the entire open interval $(n, \infty)$. 

## See also

* [[root]]
* [[real square root function]]

## References 

* {#Richman12} [[Fred Richman]], *Algebraic functions, calculus style*. Communications in Algebra, Volume 40, Issue 7, July 2012, Pages 2671-2683 &lbrack;[doi:10.1080/00927872.2011.584337](https://doi.org/10.1080/00927872.2011.584337)&rbrack;

[[!redirects real nth root function]]
[[!redirects real nth root functions]]

[[!redirects real root function]]
[[!redirects real root functions]]

[[!redirects principal nth root function]]
[[!redirects principal nth root functions]]

[[!redirects principal root function]]
[[!redirects principal root functions]]