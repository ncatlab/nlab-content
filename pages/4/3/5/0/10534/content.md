
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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

A _convex function_ is a [[real numbers|real]]-valued [[function]] defined on a [[convex set]] whose [[graph]] is the boundary of a [[convex set]].

There is another context where people say a function is convex if it is a [[Lipschitz function]] between [[metric spaces]] with Lipschitz constant (or Lipschitz modulus) 1. These are different concepts of convexity, although there are relations between convexity and Lipschitz continuity, as we shall see below. 


## Definition 

Let $D$ be a [[convex space]]. A [[function]] $f \colon D \to \mathbb{R}$ is **convex** if the [[set]] $\{(x, z) \in D \times \mathbb{R}: z \geq f(x)\}$ is a convex subspace of $D \times \mathbb{R}$. Equivalently, $f$ is **convex** if for all $x, y \in D$, 

$$f(t x + (1-t) y) \leq t f(x) + (1-t) f(y)$$ 

whenever $0 \leq t \leq 1$. 

This definition obviously extends to functions $f \colon D \to I$ where $I$ is an [[interval]] of $\mathbb{R}$ (whether open or closed or half-open, it doesn't matter). 

The function $f$ is called **concave** if it satisfy the reverse inequality to the one given above, or equivalently if $-f$ is convex.

A function $f$ is __strictly convex__ if the inequality holds strictly whenever $0 \lt t \lt 1$.  In high-school mathematics, one often says _concave upward_ for strictly convex and _concave downward_ for strictly concave.


## Examples 

* A [[homomorphism]] of [[convex sets]], i.e. a  convex-linear map, $D \to \mathbb{R}$, is of course convex. 

* The [[norm]] function $\mathbb{C} \to \mathbb{R}$ is convex. This follows readily from multiplicativity ${|x y|} = {|x|} \cdot {|y|}$ and the [[triangle inequality]] ${|x + y|} \leq {|x|} + {|y|}$. 

* More generally, for a [[normed vector space]] $V$, the norm function ${\|(-)\|}$ is convex, again by the triangle inequality and the scaling axiom ${\|\alpha v\|} = {|\alpha|} \cdot {\|v\|}$ for [[scalars]] $\alpha$. 

* For any twice-[[differentiable function]] $f \colon (a, b) \to \mathbb{R}$, the second derivative $f''$ is nonnegative iff $f$ is convex; this may be proven using the [[mean value theorem]]. Examples include the [[exponential function]] $\exp: (-\infty, \infty) \to \mathbb{R}$ and the $p$-power function $[0, \infty) \to \mathbb{R}: t \mapsto t^p$ if $p \geq 1$. 

* More generally, for an open convex region $D \subseteq \mathbb{R}^n$ in a [[Euclidean space]], a twice-differentiable function $f: D \to \mathbb{R}$ is convex iff its [[Hessian]] is a [[semidefinite element|positive semidefinite]] [[bilinear form]]. 

* Any positive $\mathbb{R}$-[[linear combination]] of convex functions on $D$ is again convex. 

* The pointwise [[maximum]] of two convex functions on $D$ is again convex. 

* If $g: V \to W$ is a homomorphism or convex-linear map between [[convex spaces]], and if $f: W \to \mathbb{R}$ is convex, then $f \circ g: V \to \mathbb{R}$ is convex. 

In the next two examples, $I \subseteq \mathbb{R}$ is an [[interval]]. 

* It is not generally true that a composition $D \stackrel{g}{\to} I \stackrel{f}{\to} \mathbb{R}$ of convex functions is convex. For example, this fails for the case $D = \mathbb{R}$ and $g(x) = x^2 + 1$ and $f: [1, \infty) \to \mathbb{R}$ given by $f(x) = x^{-1}$. 

* However, if $f: I \to \mathbb{R}$ is both [[monotone function|monotone increasing]] and convex, then for any convex function $g: D \to I$, the composite $f \circ g: D \to \mathbb{R}$ is convex (as is easily shown). 

A special case of the last class of examples are functions of the form $e^f = \exp \circ f$ where $f$ is convex. We say a function $f: D \to (0, \infty)$ is __log-convex__ if $\log f$ is convex. We see then that log-convex functions are also convex.  The [[identity function]] on $\mathbb{R}$ is an example of a convex function that is *not* log-convex (or use $x \mapsto x^2$ for a strict example).


## Properties 

+-- {: .num_lemma #squeeze} 
###### Lemma 
If $f: (a, b) \to \mathbb{R}$ is convex and $u \lt v \lt w \in (a, b)$, then 

$$\frac{f(u) - f(v)}{u - v} \leq \frac{f(u) - f(w)}{u - w} \leq \frac{f(v) - f(w)}{v - w}.$$ 

Consequently, the function $x \mapsto \frac{f(x) - f(v)}{x - v}$ on the domain $u \lt x \lt v$ is increasing and is bounded above by $\frac{f(v)-f(w)}{v-w}$; similarly, this function on the domain $v \lt x \lt w$ is increasing and bounded below by $\frac{f(u)-f(v)}{u-v}$. 
=-- 

The proof is virtually trivial; just write $v$ as a convex combination $t u + (1-t)w$ and use the definition of convexity. 

+-- {: .num_prop} 
###### Proposition 
A convex function $f: (a, b) \to \mathbb{R}$ is continuous. 
=-- 

+-- {: .proof} 
###### Proof 
For any point $x_0 \in (a, b)$ there are $s, t, u, v \in (a, b)$ with $s \lt t \lt x_0 \lt u \lt v$. Then for any $x \in (t, x_0) \cup (x_0, u)$ we have by Lemma \ref{squeeze} 

$$\frac{f(s)-f(t)}{s-t} \leq \frac{f(x) - f(x_0)}{x-x_0} \leq \frac{f(u)-f(v)}{u-v}$$ 

so that $K = \max\{\left\vert \frac{f(s)-f(t)}{s-t}\right\vert, \left\vert \frac{f(u)-f(v)}{u-v}\right\vert\}$ serves as a Lipschitz constant, i.e., we have 

$$|f(x) - f(x_0)| \leq K|x - x_0|$$ 

for all $x \in (t, u)$. This is enough to force continuity at the point $x_0$. 
=-- 

In the converse direction, we have the following result which frequently arises in practice. 

+-- {: .num_prop} 
###### Proposition 
If $D \subseteq \mathbb{R}^n$ is a convex set and $f: D \to \mathbb{R}$ is a continuous function such that 

$$f\left(\frac{x+y}{2}\right) \leq \frac{f(x) + f(y)}{2},$$ 

then $f$ is convex. 
=-- 

+-- {: .proof} 
###### Proof 
For any fixed $x, y \in D$, the function $h: [0, 1] \to \mathbb{R}$ defined by 

$$h(t) = t f(x) + (1-t)f(y) - f(t x + (1-t)y)$$ 

is continuous. The [[inverse image]] $h^{-1}([0, \infty))$ is closed in $[0, 1]$ and, by an easy induction argument, contains the set of [[dyadic rational numbers]] $t \in [0, 1]$, which is dense in $[0, 1]$. Being closed and dense, $h^{-1}([0, \infty))$ is all of $[0, 1]$, i.e., $h(t) \geq 0$ for all $t \in [0, 1]$, but this is precisely the condition that $f$ is convex. 
=-- 

Another easy consequence of Lemma \ref{squeeze} is 

+-- {: .num_prop} 
###### Proposition 
For a convex function $f: (a, b) \to \mathbb{R}$, the right-hand and left-hand derivatives 

$$\underset{x \searrow x_0}{\lim} \frac{f(x)-f(x_0)}{x-x_0}, \qquad \underset{x \nearrow x_0}{\lim} \frac{f(x)-f(x_0)}{x-x_0}$$ 

of $f$ exist at every point $x_0 \in (a, b)$, and the left-hand derivative at $x_0$ is less than or equal to the right-hand derivative at $x_0$. 
=-- 

It further follows from Lemma \ref{squeeze} that if $f$ is convex and we define $(D f)(x_0)$ to be the average of the right-hand and left-hand derivatives, then $D f$ is monotone increasing and hence is discontinuous at at most countable many points of jump discontinuity (whence $D f$ is [[Riemann integration|Riemann-integrable]], for instance). 


## Related concepts

* [[convex analysis]]

* [[Legendre transform]]

* [[Lipschitz function]]

## References

See also

* Wikipedia, _[Convex function](http://en.wikipedia.org/wiki/Convex_function)_

[[!redirects convex map]]
[[!redirects convex maps]] 
[[!redirects convex function]]
[[!redirects convex functions]] 
[[!redirects log-convex function]] 
[[!redirects log-convex functions]] 

[[!redirects concave map]]
[[!redirects concave maps]] 
[[!redirects concave function]]
[[!redirects concave functions]]
[[!redirects log-concave function]] 
[[!redirects log-concave functions]]  