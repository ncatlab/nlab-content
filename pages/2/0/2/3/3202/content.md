
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The term 'Lebesgue space' can stand for two distinct notions: one is the general notion of [[measure space]] (compare the [Springer Encyclopaedia of Mathematics](http://eom.springer.de/L/l057910.htm)) and another is the notion of $L^p$ space (or $L_p$ space).  Here we discuss the latter.

Sometimes '$L_p$' is used as a synonym for $L^p$; sometimes it is used to mean $L^{1/p}$.


## Definitions

If $1 \leq p \lt \infty$ is a [[real number]] and $(\Omega,\mu)$ is a [[measure space]], one considers the **$L^p$ space** $L_p(\Omega)$ of (equivalence classes of) [[measurable function|measurable]] (complex- or real-valued) functions $f\colon \Omega \to \mathbb{K}$ whose (absolute values of) $p$th powers are integrable; i.e. whose [[norm]] 

$$ {\|f\|_p} = \left(\int_\Omega {|f|^p} \,d\mu\right)^{1/p} $$

is finite.

The $L^p$ spaces are examples of [[Banach spaces]]; they are continuous analogues of $l^p$ spaces of $p$-summable series. (Indeed, $l^p(S)$, for $S$ a [[set]], is simply $L^p(S)$ if $S$ is equipped with [[counting measure]].)

For fixed $f$, the norm ${\|f\|_p}$ is continuous in $p$.  Accordingly, for $p = \infty$, one may take the limit of ${\|f\|}_p$ as $p \to \infty$.  However, this turns out to be the same as the [[essential supremum]] norm $\|f\|_\infty$.  Therefore, $L^\infty(\Omega)$ makes sense as long as $\Omega$ is a [[measurable space]] equipped with a family of [[null sets]] (or [[full sets]]); the measure $\mu$ is otherwise irrelevant.

For $0 \lt p \lt 1$, we can define the $L^p$ space using the same formula; however, it is no longer a Banach space (but still an [[F-space]]).  For $p = 0$, we can again take the limit, or equivalently use the essential infimum; every measurable function on $\Omega$ belongs to $L^0$ (which is no longer even an $F$-space).


## Minkowski's inequality 

We offer here a proof that ${\|f\|_p}$ defines a norm in the case $1 \lt p \lt \infty$; the cases $p = 1$ and $p = \infty$ follow by continuity and are easy to check from first principles. The most usual textbook proofs involve a clever application of [[Hölder's inequality]]; the following proof is more straightforwardly geometric. All functions $f$ may be assumed to be real- or complex-valued. 

+-- {: .un_thm} 
###### Theorem 
Suppose $1 \leq p \leq \infty$, and suppose $\Omega$ is a measure space with measure $\mu$. Then the function ${|(-)|_p}\colon L^p(\Omega, \mu) \to \mathbb{R}$ defined by  
$${\|f\|_p} \coloneqq (\int_\Omega {|f|^p} \,d\mu)^{1/p}$$ 
defines a [[norm]]. 
=-- 

One must verify three things: 

1. Separation axiom: ${\|f\|_p} = 0$ implies $f = 0$. 

1. Scaling axiom: ${\|t f\|}_p = {|t|} \, {\|f\|_p}$. 

1. Triangle inequality: ${\|f + g\|_p} \leq {\|f\|_p} + {\|g\|_p}$. 

The first two properties are obvious, so it remains to prove the last, which is also called __Minkowski's inequality__. 

Our proof of Minkowski's inequality is broken down into a series of simple lemmas. The plan is to boil it down to two things: the scaling axiom, and convexity of the function $x \mapsto {|x|^p}$ (as a function from real or complex numbers to nonnegative real numbers). 

First, some generalities. Let $V$ be a (real or complex) vector space equipped with a function ${\|(-)\|}\colon V \to [0, \infty]$ that satisfies the scaling axiom: ${\|t v\|} = {|t|} \, {\|v\|}$ for all scalars $t$, and the separation axiom: ${\|v\|} = 0$ implies $v = 0$. As usual, we define the [[unit ball]] in $V$ to be $\{v \in V \;|\; {\|v\|} \leq 1\}.$ 

+-- {: .num_lem #conditions}
###### Lemma
Given that the scaling and separation axioms hold, the following conditions are equivalent: 
1. The triangle inequality is satisfied. 
2. The unit ball is convex. 
3. If ${\|u\|} = {\|v\|} = 1$, then ${\|t u + (1-t)v\|} \leq 1$ for all $t \in [0, 1]$.  
=-- 

+-- {: .proof}
###### Proof 
Condition 1. implies condition 2. easily: if $u$ and $v$ are in the unit ball and $0 \leq t \leq 1$, we have 
$$\array{
{\|t u + (1-t)v\|} & \leq & {\|t u\|} + {\|(1-t)v\|} \\
 & = & t {\|u\|} + (1-t) {\|v\|} \\
 & \leq & t + (1-t) = 1.}$$ 
Now 2. implies 3. trivially, so it remains to prove that 3. implies 1.  Suppose ${\|v\|}, {\|v'\|} \in (0, \infty)$. Let $u = \frac{v}{{\|v\|}}$ and $u' = \frac{v'}{{\|v'\|}}$ be the associated unit vectors. 
Then 
$$\array{
\frac{v + v'}{{\|v\|}+{\|v'\|}} & = & (\frac{{\|v\|}}{{\|v\|}+{\|v'\|}})\frac{v}{{\|v\|}} + (\frac{{\|v'\|}}{{\|v\|}+{\|v'\|}})\frac{v'}{{\|v'\|}} \\
 & = & t u + (1-t)u'}$$ 
where $t = \frac{{\|v\|}}{{\|v\|} + {\|v'\|}}$. If condition 3. holds, then 
$${\|t u + (1-t)u'\|} \leq 1$$ 
but by the scaling axiom, this is the same as saying 
$$\frac{{\|v + v'\|}}{{\|v\|} + {\|v'\|}} \leq 1,$$ 
which is the triangle inequality. 
=-- 

Consider now $L^p$ with its $p$-norm ${\|f\|} = {|f|_p}$.  By Lemma \ref{conditions}, this inequality is equivalent to 

* **Condition 4:** If ${|u|_{p}^{p}} = 1$ and ${|v|_{p}^{p}} = 1$, then ${|t u + (1-t)v|_{p}^{p}} \leq 1$ whenever $0 \leq t \leq 1$. 

This allows us to remove the cumbersome exponent $1/p$ in the definition of the $p$-norm. 

The next two lemmas may be proven by elementary calculus; we omit the proofs. (But you can also see the [full details](http://ncatlab.org/toddtrimble/published/p-norms).) 

+-- {: .num_lem #2deriv}
###### Lemma
Let $\alpha, \beta$ be two complex numbers, and define 
$$\gamma(t) = {|\alpha + \beta t|^p}$$ 
for _real_ $t$. Then $\gamma''(t)$ is nonnegative. 
=-- 

+-- {: .num_lem #convex}
###### Lemma
Define $\phi\colon \mathbb{C} \to \mathbb{R}$ by $\phi(x) = |x|^p$.  Then $\phi$ is convex, i.e., for all $x, y$, 
$${|t x + (1-t)y|^p} \leq t{|x|^p} + (1-t){|y|^p}$$ 
for all $t \in [0, 1]$. 
=-- 

+-- {: .proof}
###### Proof of Minkowski's inequality   
Let $u$ and $v$ be unit vectors in $L^p$. By condition 4, it suffices to show that ${|t u + (1-t)v|_p} \leq 1$ for all $t \in [0, 1]$. But 
$$\int_\Omega {|t u + (1-t)v|^p} \,d\mu \leq \int_\Omega t{|u|}^p + (1-t){|v|}^p \,d\mu$$ 
by Lemma \ref{convex}. Using $\int {|u|^p} = 1 = \int {|v|^p}$, we are done. 
=-- 


## References

* W. Rudin, _Functional analysis_, McGraw Hill 1991.

* L. C. Evans, _Partial differential equations_, Amer. Math. Soc. 1998.

* Wikipedia (English): [Lp space](http://en.wikipedia.org/wiki/Lp_space)


[[!redirects Lebesgue space]]
[[!redirects Lebesgue spaces]]
[[!redirects L-p space]]
[[!redirects L-p spaces]]
[[!redirects L-p-space]]
[[!redirects L-p-spaces]]
[[!redirects L^p space]]
[[!redirects L^p spaces]]
[[!redirects L_p space]]
[[!redirects L_p spaces]]

[[!redirects Minkowski inequality]]
[[!redirects Minkowski's inequality]]
[[!redirects Minkowski's inequality]]
[[!redirects Minkowski\'s inequality]]
