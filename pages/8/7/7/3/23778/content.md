
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

## Idea ##

The different types of [[square root]] [[partial functions]] on the [[real numbers]] that satisfy the [[functional equation]] $f(x)^2 = x$ on some [[subset]] of the real numbers. 

## Definition ##

### Metric principal square root ###

The **metric principal square root** is a function $\mathrm{sqrt}:[0, \infty) \to \mathbb{R}$ defined by the functional equation $\mathrm{sqrt}(x^2) = \vert x \vert$ for all real numbers $x \in \mathbb{R}$. This is the real square root function used to define the [[metric]] in [[Euclidean spaces]]. However, this square root is not [[constructive mathematics|constructively]] [[pointwise continuous]] at $0$. 

### Continuous principal square root ###

The **continuous principal square root** is a function $\mathrm{sqrt}_\mathrm{cont}:(0, \infty) \to \mathbb{R}$ defined as the [[solution]] to the first order non-linear [[ordinary differential equation]] 

$$(2 \mathrm{sqrt}_\mathrm{cont}) \frac{d \mathrm{sqrt}_\mathrm{cont}}{d x} = 1$$

with initial conditions $\mathrm{sqrt}_\mathrm{cont}(1) = 1$, derived from the [[inverse function theorem]]. This is the real square root function used in constructive versions of the [[real quadratic formula]], or the [[continuous quadratic formula]]. However, $0$ is not in the domain of $\mathrm{sqrt}_\mathrm{cont}$, which means that not every real number with a real square root is in the domain of $\mathrm{sqrt}_\mathrm{cont}$, and it cannot be used in defining the metric for Euclidean spaces. 

### Other square roots

According to ([Richman 2010](#Richman2010)), there are an uncountable number of functions that satisfy the [[functional equation]] $f(x)^2 = x$ on some [[subset]] of the [[real numbers]]. Each of these could be called a real "square root function". 

For example, let $1_{\mathbb{Q}}:\mathbb{R} \to \mathbb{R}$ be the constructive Dirichlet indicator function, defined as $1_{\mathbb{Q}}(x) \coloneqq 1$ for every rational number $q \in \mathbb{Q}$, and $1_{\mathbb{Q}}(x) \coloneqq 0$ for every real number $x$ apart from every rational number $q \in \mathbb{Q}$ 

$$\forall q \in \mathbb{Q}. \vert x - q \vert \gt 0$$

Then the function $f(x) \coloneqq (-1)^{1_{\mathbb{Q}}(x)} \mathrm{sqrt}(x)$ is a real square root function, even though it is nowhere continuous, and not defined on the entire half-open interval $[0, \infty)$. 

## See also

* [[square root]], for square roots in more general mathematical structures

* [[real quadratic function]]

* [[real absolute value]]

* [[sign function]]

* [[Euclidean field]]

## References 

* {#Richman2010} [[Fred Richman]] (2010). _Algebraic functions, calculus style_. [Fred Richman's documents](http://math.fau.edu/richman/html/docs.htm).

[[!redirects square root function]]
[[!redirects square root functions]]
[[!redirects principal square root function]]
[[!redirects principal square root functions]]

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