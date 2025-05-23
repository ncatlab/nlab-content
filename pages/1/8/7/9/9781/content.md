+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
#### Variational calculus
+-- {: .hide}
[[!include variational calculus - contents]]
=--
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _Fr&#233;chet derivative_ is a kind of [[functional derivative]].

There are various ways to set up [[differentiation]] in finite dimensions, the most common being the *total derivative* and the *directional derivatives*.  In [[infinite-dimensional manifold|infinite dimensions]], these become the *Fr&#233;chet derivative* and the *[[Gâteaux derivative]]* respectively.

The definition of the **Fr&#233;chet derivative** of a function is a generalisation of the notion of the *total derivative* of a function in finite dimensions.  In finite dimensions, the total derivative of a function $f \colon \mathbb{R}^n \to \mathbb{R}$ at a point $x \in \mathbb{R}^n$ is defined to be (assuming that it exists) the unique linear operator $D f_x \colon \mathbb{R}^n \to \mathbb{R}$ such that:

$$
\lim_{h \to 0} \frac{f(x + h) - f(x) - D f_x h}{{\|h\|}} = 0
$$

As all norms in finite dimensions are norm-equivalent, the choice of norm does not matter.

This generalises most easily to [[normed vector spaces]].  As it involves limits, it is generally most convenient to work with [[Banach spaces]].

## Definition

+-- {: .num_defn #frderiv}
###### Definition
Let $E$ and $F$ be [[Banach spaces]] with [[norms]] ${\|\cdot\|_E}$ and ${\|\cdot\|_F}$ respectively.
Let $U \subseteq E$ be an open subset.
A (possibly non-linear) function $f \colon U \to F$ is said to be **Fr&#233;chet differentiable** at $x \in U$ if there is a continuous linear operator $A_x \colon E \to F$ such that:
$$
\lim_{h \to 0} \frac{\|f(x + h) - f(x) - A_x h\|_F}{\|h\|_E} = 0
$$

The operator $A_x$ is called the **Fr&#233;chet derivative** of $f$ at $x$ and is written $D f_x$ or $D f(x)$.
=--

## Properties

If the Fr&#233;chet derivative exists, it is unique.

## Extensions

With the notation of Definition \ref{frderiv}, a function $f U \supseteq E \to F$ is said to be of class $C^1$ on $U$ if it is Fr&#233;chet differentiable throughout $U$ and the resulting function $x \mapsto D f_x$ is continuous as a function $U \to L(E,F)$, where $L(E,F)$ is the Banach space of continuous linear operators from $E$ to $F$.

The differentiability of $x \mapsto D f_x$ can then be questioned, and for $n \in \mathbb{N}$, the class $C^n$ is defined by iteration in the obvious way.


[[!redirects Frechet derivative]]
[[!redirects Fréchet derivatives]]
[[!redirects Frechet derivatives]]
[[!redirects Fréchet differentiable]]
[[!redirects Frechet differentiable]]