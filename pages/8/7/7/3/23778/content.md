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

# Contents
* table of contents
{: toc}

## Idea 

The different types of [[square root]] [[partial functions]] on the [[real numbers]] that satisfy the [[functional equation]] $f(x)^2 = x$ on some [[subset]] of the real numbers. 

## Definition 

There exists a square root function $\mathrm{sqrt}:(0, \infty) \to \mathbb{R}$ defined by 
$$\mathrm{sqrt}(x) \coloneqq e^{\frac{1}{2} \ln(x)}$$
This square root function on positive real numbers is [[differentiable function|differentiable]] and in fact [[analytic function|analytic]] on the positive real numbers. 

One can also define the usual notion of the [[principal square root]] on the non-negative real numbers, which is continuous on non-negative real numbers but not differentiable at zero. 

\begin{definition}
Classically, the **principal square root** function is defined by case analysis:

$$
\sqrt{x} \coloneqq 
\begin{cases}
0 & x = 0 \\
\exp(\frac{1}{2}\ln(x)) & x \gt 0
\end{cases}
$$
\end{definition}

This definition also works in [[constructive mathematics]] for any set of real numbers that satisfy [[analytic LPO]]. In the absence of the [[analytic LPO]], the usual principal square root on non-negative real numbers can still be defined on any [[sequentially Cauchy complete|Cauchy complete]] [[Archimedean ordered field]], but one has to continuously patch the principal square root on positive real numbers to cover zero. 

This following definition of a principal square root function is [[François G. Dorais]]'s construction of a principal square root function in the non-negative real numbers from [Birchfield, Dorais & Strickland 2022](#BDS22): 

\begin{definition}
Let us define continuous functions $f_n:[0, \infty) \to [0, \infty)$: 
$$f_n(x) = \begin{cases}
1/2^n & \mathrm{when}\; x \leq 1/4^n \\
e^{\frac{1}{2} \ln(x)} & \mathrm{when}\; x \geq 1/4^n \\
\end{cases}$$
As stated, that requires knowing whether $x \leq 1/4^n$ or $x \geq 1/4^n$, but it is possible to work around this by patching three functions together:

 * $f^{0}_k:[0,1/4^k) \to \mathbb{R}$ is the linear function $f(x) = 2^k x$,
 * $f^{+}_k:(0,\infty) \to \mathbb{R}$ is defined as $\min(2^k x,\exp(\frac{1}{2} \ln(x)))$.

Since these functions agree on their overlap, and their domains comprise all of $[0, \infty)$ we do get a total function $f_n:[0, \infty) \to [0, \infty)$ as a result. 

Now the sequence of functions $(f_n)_{n=0}^\infty$ so defined converges uniformly on any bounded interval to a continuous function $\sqrt{(-)}:[0, \infty) \to [0, \infty)$ called the **principal square root** function. It is easily seen that $(\sqrt{x})^2 = x$ and $\sqrt{x^2} = x$. 
\end{definition}

The principal square root function is used to define the [[Euclidean metric]] in [[Euclidean spaces]].  

## Other square root functions

According to ([Richman 2012](#Richman12)), given the existence of a principal square root function, there are an uncountable number of functions that satisfy the [[functional equation]] $f(x)^2 = x$ on some [[subset]] of the [[real numbers]]. Each of these could be called a real "square root function". 

For example, let $1_{\mathbb{Q}}:\mathbb{R} \to \mathbb{R}$ be the Dirichlet indicator function, defined as $1_{\mathbb{Q}}(x) \coloneqq 1$ for every rational number $q \in \mathbb{Q}$, and $1_{\mathbb{Q}}(x) \coloneqq 0$ for every real number $x$ apart from every rational number $q \in \mathbb{Q}$ 

$$\forall q \in \mathbb{Q}. \vert x - q \vert \gt 0$$

Then the function $f(x) \coloneqq (-1)^{1_{\mathbb{Q}}(x)} \sqrt{x}$ is a real square root function, even though it is nowhere continuous. 

In constructive mathematics, the Dirchelet indicator function is only defined on the subset of the real numbers which are decidably rational or [[strongly irrational number|strongly irrational]]. This domain is equivalent to the entire real numbers if and only if [[analytic LPO]] holds of the real numbers. As a result, the resulting square root function is in general only a partial function on the entire half-open interval $[0, \infty)$. 

## Approximate square root functions

Sometimes, the square root function cannot be defined exactly to satisfy the equation $\mathrm{sqrt}(x)^2 = x$. This is the case in some parts of [[numerical analysis]] where the focus is on computation and numerical [[algorithms]], and the real numbers end up as rational numbers since the medium which stores the data for the computation, such as physical paper or the calculator or the computer, cannot store an infinite amount of data required to define a real number exactly.

Instead, there are various notions of **approximate square root functions**. These include the **$\epsilon$-tolerant square root functions**, which, for a given [[positive]] [[rational number]] $\epsilon \in \mathbb{Q}_+$ representing the [[tolerance]], is a function $f$ from the [[non-negative]] [[real numbers]] to the real numbers, which satisfies the following inequality for all non-negative real numbers:

$$\vert f(x)^2 - x \vert \lt \epsilon$$

There are multiple possible $\epsilon$-tolerant square root functions for each tolerance $\epsilon$. 

## See also

* [[square root]], for square roots in more general mathematical structures

* [[real quadratic function]]

* [[real absolute value]]

* [[sign function]]

* [[Euclidean field]]

* [[real nth root function]]

## References 

* {#Richman12} [[Fred Richman]], *Algebraic functions, calculus style*. Communications in Algebra, Volume 40, Issue 7, July 2012, Pages 2671-2683 &lbrack;[doi:10.1080/00927872.2011.584337](https://doi.org/10.1080/00927872.2011.584337)&rbrack;

* {#BDS22} [[Madeleine Birchfield]], [[François G. Dorais]], [[Neil Strickland]], *Proof in constructive mathematics that the principal square root function exists in any Cauchy complete Archimedean ordered field* , MathOverflow, [website](https://mathoverflow.net/questions/426103/proof-in-constructive-mathematics-that-the-principal-square-root-function-exists)

[[!redirects real square root]]
[[!redirects real square roots]]
[[!redirects real principal square root]]

[[!redirects real square root function]]
[[!redirects real square root functions]]
[[!redirects real principal square root function]]

[[!redirects metric square root]]
[[!redirects metric square roots]]
[[!redirects metric principal square root]]

[[!redirects metric square root function]]
[[!redirects metric square root functions]]
[[!redirects metric principal square root function]]

[[!redirects continuous square root]]
[[!redirects continuous square roots]]
[[!redirects continuous principal square root]]

[[!redirects continuous square root function]]
[[!redirects continuous square root functions]]
[[!redirects continuous principal square root function]]

[[!redirects differentiable square root]]
[[!redirects differentiable square roots]]
[[!redirects differentiable principal square root]]

[[!redirects differentiable square root function]]
[[!redirects differentiable square root functions]]
[[!redirects differentiable principal square root function]]

[[!redirects smooth square root]]
[[!redirects smooth square roots]]
[[!redirects smooth principal square root]]

[[!redirects smooth square root function]]
[[!redirects smooth square root functions]]
[[!redirects smooth principal square root function]]

[[!redirects analytic square root]]
[[!redirects analytic square roots]]
[[!redirects analytic principal square root]]

[[!redirects analytic square root function]]
[[!redirects analytic square root functions]]
[[!redirects analytic principal square root function]]

[[!redirects approximate square root function]]
[[!redirects approximate square root functions]]
[[!redirects approximate principal square root function]]

[[!redirects epsilon-tolerant square root function]]
[[!redirects epsilon-tolerant square root functions]]
[[!redirects epsilon-tolerant principal square root function]]