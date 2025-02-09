
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
#### Integration theory
+--{: .hide}
[[!include integration theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The term 'Lebesgue space' can stand for two distinct notions: one is the general notion of [[measure space]] (compare the [Springer Encyclopaedia of Mathematics](http://eom.springer.de/L/l057910.htm)) and another is the notion of $L^p$ space (or $L_p$ space).  Here we discuss the latter.

Lebesgue spaces $L^p$ in this sense are [[normed vector spaces]] of [[functions]] on a [[measure space]], equipped with the suitable version of the [[p-norm]].

Beware that sometimes the notation '$L_p$' is used as a synonym for $L^p$; sometimes it is used to mean $L^{1/p}$.

## Notation

For historical reasons (starting with the original paper by Riesz), the exponent $p$ is traditionally taken to be the [[reciprocal]] of the “correct” exponent.

If we take $M^p=L^{1/p}$, the spaces
$M^p$ form a $\mathbf{C}$-[[graded algebra]], where $\mathbf{C}$ denotes [[complex numbers]].

This is a conceptual explanation for the appearance of formulas like $1/p+1/q=1/r$ in [[Hölder's inequality]].

In [[differential geometry]], the notion of [[density]] does use the “correct” grading.

In the [[Tomita–Takesaki theory]], the parameter $t$ for [[modular automorphism group]] is almost the “correct” grading, except that it is multiplied by the [[imaginary unit]] $i$.

## Definitions
 {#Definition}

If $1 \leq p \lt \infty$ is a [[real number]] and $(\Omega,\mu)$ is a [[measure space]], one considers the **$L^p$ space** $L_p(\Omega)$, which is the [[vector space]] of [[equivalence classes]] of those [[measurable function|measurable]] (complex- or real-valued) functions $f\colon \Omega \to \mathbb{K}$ whose (absolute values of) $p$th powers are integrable, in that the [[integration|integral]]

$$ 
  {\|f\|_p} 
    \;\coloneqq\; 
  \left(
    \textstyle{\int}_\Omega {|f|^p} \,d\mu
  \right)^{1/p} 
    \;\lt\; 
  \infty
$$

exists. Two such are taken to be equivalent, $f \sim g$, if ${\|f-g\|_p} = 0$. For $p = 2$ this is the space $L^2$ of [[square integrable functions]].

On these spaces $L^p(X)$ of equivalence classes of $p$-power integrable functions, the function ${\|f\|_p}$ satisfies the [[triangle inequality]] (due to [[Minkowski's inequality]], see [below](#MinkowskiInequality)) and hence defines a [[norm]], the _[[p-norm]]_, making them [[normed vector spaces]].

The $L^p$ spaces are examples of [[Banach spaces]]; they are continuous analogues of $l^p$ spaces of $p$-summable series. (Indeed, $l^p(S)$, for $S$ a [[set]], is simply $L^p(S)$ if $S$ is equipped with [[counting measure]].)

For fixed $f$, the norm ${\|f\|_p}$ is continuous in $p$.  Accordingly, for $p = \infty$, one may take the limit of ${\|f\|}_p$ as $p \to \infty$.  However, this turns out to be the same as the [[essential supremum]] norm $\|f\|_\infty$.  Therefore, $L^\infty(\Omega)$ makes sense as long as $\Omega$ is a [[measurable space]] equipped with a family of [[null sets]] (or [[full sets]]); the measure $\mu$ is otherwise irrelevant.

For $0 \leq p \lt 1$, one can modify the definition to make $L^p$ into an [[F-space]] (but not a Banach space).  See the definitions at [[p-norm]].


## Minkowski's inequality 
 {#MinkowskiInequality}
 
We offer here a proof that ${\|f\|_p}$ indeed defines a norm in the case $1 \lt p \lt \infty$, in that it satisfies the [[triangle inequality]]. This is usually known as *[[Minkowski's inequality]]*.

(The cases $p = 1$ and $p = \infty$ follow by continuity and are easy to check from first principles.) 

The most usual textbook proofs involve a clever application of [[Hölder's inequality]]; the following proof is more straightforwardly geometric. All functions $f$ may be assumed to be real- or complex-valued. 

+-- {: .num_theorem} 
###### Theorem 

Suppose $1 \leq p \leq \infty$, and suppose $\Omega$ is a [[measure space]] with [[measure]] $\mu$. Then the function ${|(-)|_p} \,\colon\, L^p(\Omega, \mu) \to \mathbb{R}$ defined by  
$$
  {\|f\|_p} 
    \;\coloneqq\; 
  \big(
    \textstyle{\int}_\Omega {|f|^p} \,d\mu
  \big)^{1/p}
$$ 
defines a [[norm]]. 

=-- 

One must verify three things: 

1. Separation axiom: ${\|f\|_p} = 0$ implies $f = 0$. 

1. Scaling axiom: ${\|t f\|}_p = {|t|} \, {\|f\|_p}$. 

1. Triangle inequality: ${\|f + g\|_p} \leq {\|f\|_p} + {\|g\|_p}$. 

The first two properties are obvious, so it remains to prove the last, which is also called __[[Minkowski's inequality]]__. 

Our proof of Minkowski's inequality is broken down into a series of simple lemmas. The plan is to boil it down to two things: the scaling axiom, and convexity of the function $x \mapsto {|x|^p}$ (as a function from real or complex numbers to nonnegative real numbers). 

First, some generalities. Let $V$ be a (real or complex) vector space equipped with a function ${\|(-)\|}\colon V \to [0, \infty]$ that satisfies the scaling axiom: ${\|t v\|} = {|t|} \, {\|v\|}$ for all scalars $t$, and the separation axiom: ${\|v\|} = 0$ implies $v = 0$. As usual, we define the [[unit ball]] in $V$ to be $\{v \in V \;|\; {\|v\|} \leq 1\}.$ 

+-- {: .num_lemma #conditions}
###### Lemma
Given that the scaling and separation axioms hold, the following conditions are equivalent: 

1. The triangle inequality is satisfied. 
1. The unit ball is convex. 
1. If ${\|u\|} = {\|v\|} = 1$, then ${\|t u + (1-t)v\|} \leq 1$ for all $t \in [0, 1]$.  
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

+-- {: .num_lemma #2deriv}
###### Lemma
Let $\alpha, \beta$ be two complex numbers, and define 
$$\gamma(t) = {|\alpha + \beta t|^p}$$ 
for _real_ $t$. Then $\gamma''(t)$ is nonnegative. 
=-- 

+-- {: .num_lemma #convex}
###### Lemma
Define $\phi\colon \mathbb{C} \to \mathbb{R}$ by $\phi(x) = |x|^p$.  Then $\phi$ is convex, i.e., for all $x, y$, 
$${|t x + (1-t)y|^p} \leq t{|x|^p} + (1-t){|y|^p}$$ 
for all $t \in [0, 1]$. 
=-- 

+-- {: .proof}
###### Proof of Minkowski's inequality   
Let $u$ and $v$ be unit vectors in $L^p$. By condition 4, it suffices to show that ${|t u + (1-t)v|_p} \leq 1$ for all $t \in [0, 1]$. But 
$$
  \textstyle{\int}_\Omega {|t u + (1-t)v|^p} \,d\mu 
    \;\leq\; 
  \textstyle{\int}_\Omega t{|u|}^p + (1-t){|v|}^p \,d\mu
  \,,
$$ 
by Lemma \ref{convex}. Using $\int {|u|^p} = 1 = \int {|v|^p}$, we are done. 
=-- 


## Independence from the measure

In this section, we exhibit a construction of $L^p$-spaces that only makes use of an [[enhanced measurable space]] $(X,M,N)$ (a set $X$ with a [[σ-algebra]] $M$ of measurable sets and a [[σ-ideal]] $N$ of negligible sets), and not the full data of a [[measure space]] $(X,M,\mu)$ (where $\mu$ is a [[measure]] on $(X,M)$ that vanishes on $N$).

This makes it clear that $L^p(X,M,\mu)$ does not really depend on $\mu$, so we can also write $L^p(X,M,N)$ instead.

We set $\mathcal{L}^p = L^{1/p}$, to ensure we get a $\mathbf{C}$-graded algebra.
In particular,

* $\mathcal{L}^0 = L^\infty$ (bounded measurable functions),

* $\mathcal{L}^{1/2}=L^2$ (the Hilbert space of half-densities),

* $\mathcal{L}^1=L^1$ (the space of finite measures).


Given $p\in\mathbf{C}$, we define $\mathcal{L}^p(X,M,N)$ as a quotient.
The underlying set is $\mathcal{L}^0(X,M,N)\times \mathcal{L}^1(X,M,N)$, the set of (equivalence classes of) bounded measurable complex-valued functions on $(X,M,N)$ times the set of of finite complex-valued measures on $(X,M)$ that vanish on $N$.

The equivalence relation is defined as follows: $(f,g\cdot\mu)\sim(f g^p,\mu)$, for every nonnegative measurable function $g$ on $(X,M,N)$.
Here $g\cdot\mu$ is a unique [[measure]] supplied by applying the [[Radon–Nikodym theorem]] in reverse:
$$(g\cdot\mu)(A) = \int_A g d\mu.$$

For $p=1$, the map $(f,\mu)\mapsto f\cdot \mu$
establishes an isomorphism from $\mathcal{L}^1(X,M,N)$ to the vector space of finite complex-valued measures on $(X,M,N)$.

For $p=0$, the map $(f,\mu)\mapsto f supp(\mu)$ establishes an isomorphism from $\mathcal{L}^0(X,M,N)$ to the vector space of bounded complex-valued functions on $(X,M,N)$.

Given a [[measure space]] $(X,M,\mu)$, the map $f \mapsto f \mu^p$ establishes an isomorphism
$$\mathcal{L}^p(X,M,\mu)\to\mathcal{L}^p(X,M,N),$$
where the left side is the usual $L^p$-space from analysis (with the reciprocal index $p$).

## Related concepts

* [[square integrable function]]

* [[canonical Hilbert space of half-densities]]

* [[tempered distribution]]

## References

Named after [[Henri Lebesgue]].

* W. Rudin, _Functional analysis_, McGraw Hill 1991.

* L. C. Evans, _Partial differential equations_, Amer. Math. Soc. 1998.

* Wikipedia (English): [Lp space](http://en.wikipedia.org/wiki/Lp_space)


category: analysis


[[!redirects Lebesgue space]]
[[!redirects Lebesgue spaces]]

[[!redirects L-p space]]
[[!redirects L-p spaces]]
[[!redirects L-p-space]]
[[!redirects L-p-spaces]]
[[!redirects L^p space]]
[[!redirects L^p spaces]]
[[!redirects L^p-space]]
[[!redirects L^p-spaces]]
[[!redirects L_p space]]
[[!redirects L_p spaces]]

[[!redirects L-1 space]]
[[!redirects L-1 spaces]]
[[!redirects L-1-space]]
[[!redirects L-1-spaces]]
[[!redirects L^1 space]]
[[!redirects L^1 spaces]]
[[!redirects L^1-space]]
[[!redirects L^1-spaces]]
[[!redirects L_1 space]]
[[!redirects L_1 spaces]]

[[!redirects L-2 space]]
[[!redirects L-2 spaces]]
[[!redirects L-2-space]]
[[!redirects L-2-spaces]]
[[!redirects L^2 space]]
[[!redirects L^2 spaces]]
[[!redirects L^2-space]]
[[!redirects L^2-spaces]]
[[!redirects L_2 space]]
[[!redirects L_2 spaces]]
