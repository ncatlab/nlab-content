
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

What is commonly known as _Minkowski's inequality_ is the statement that the [[p-norm]] ${\Vert f\Vert_p} \coloneqq \root{p}{\int_X {\vert f\vert^p} d\mu}$ on [[Lebesgue spaces]] indeed satisfies the [[triangle inequality]].


## Proofs

Our proof of Minkowski's inequality is broken down into a few simple lemmas. The plan is to boil it down to two things: the scaling axiom, and convexity of the function $x \mapsto {|x|^p}$ (as a function from real or complex numbers to nonnegative real numbers). 

First, some generalities. Let $V$ be a (real or complex) vector space equipped with a function ${\|(-)\|}\colon V \to [0, \infty]$ that satisfies the scaling axiom: ${\|t v\|} = {|t|} \, {\|v\|}$ for all scalars $t$, and the separation axiom: ${\|v\|} = 0$ implies $v = 0$. As usual, we define the [[unit ball]] in $V$ to be $\{v \in V \;|\; {\|v\|} \leq 1\}.$ 

+-- {: .num_lemma #conditions}
###### Lemma
Given that the scaling and separation axioms hold, the following conditions are equivalent: 

1. The triangle inequality is satisfied. 
1. The unit ball is [[convex set|convex]]. 
1. If ${\|u\|} = {\|v\|} = 1$, then ${\|t u + (1-t)v\|} \leq 1$ for all $t \in [0, 1]$.  
=-- 

+-- {: .proof}
###### Proof 
Since conditions 2. and 3. are pretty obviously equivalent, we just prove 1. and 3. are equivalent. Condition 1. implies condition 3. easily: if $\|u\| = 1 = \|v\|$ and $0 \leq t \leq 1$, we have 

$$\array{
{\|t u + (1-t)v\|} & \leq & {\|t u\|} + {\|(1-t)v\|} \\
 & = & t {\|u\|} + (1-t) {\|v\|} \\
 & = & t + (1-t) = 1.}$$ 

Now we prove that 3. implies 1.  Suppose ${\|v\|}, {\|v'\|} \in (0, \infty)$. Let $u = \frac{v}{{\|v\|}}$ and $u' = \frac{v'}{{\|v'\|}}$ be the associated unit vectors. 
Then 
$$\array{
\frac{v + v'}{{\|v\|}+{\|v'\|}} & = & \left(\frac{{\|v\|}}{{\|v\|}+{\|v'\|}}\right)\frac{v}{{\|v\|}} + \left(\frac{{\|v'\|}}{{\|v\|}+{\|v'\|}}\right)\frac{v'}{{\|v'\|}} \\
 & = & t u + (1-t)u'}$$ 
where $t = \frac{{\|v\|}}{{\|v\|} + {\|v'\|}}$. If condition 3. holds, then 
$${\|t u + (1-t)u'\|} \leq 1$$ 
but by the scaling axiom, this is the same as saying 
$$\frac{{\|v + v'\|}}{{\|v\|} + {\|v'\|}} \leq 1,$$ 
which is the triangle inequality. 
=-- 

Consider now $L^p$ with its $p$-norm ${\|f\|} = {|f|_p}$.  By Lemma \ref{conditions}, the Minkowski inequality is equivalent to 

* **Condition 4:** If ${|u|_{p}^{p}} = 1$ and ${|v|_{p}^{p}} = 1$, then ${|t u + (1-t)v|_{p}^{p}} \leq 1$ whenever $0 \leq t \leq 1$. 

This allows us to remove the cumbersome exponent $1/p$ in the definition of the $p$-norm. 

+-- {: .num_lemma #convex}
###### Lemma
Define $\phi\colon \mathbb{C} \to \mathbb{R}$ by $\phi(x) = |x|^p$.  Then $\phi$ is convex, i.e., for all $x, y$, 
$${|t x + (1-t)y|^p} \leq t{|x|^p} + (1-t){|y|^p}$$ 
for all $t \in [0, 1]$. 
=-- 

+-- {: .proof} 
###### Proof 
The function $g: x \mapsto {|x|}$ is convex, and for $1 \lt p$ the function $f: t \mapsto t^p$ for $t \geq 0$ is monotone increasing and convex, by the first and second derivative tests. Thus $g(t x + (1-t)y) \leq t g(x) + (1-t)g(y)$ and then 

$$\array{
f(g(t x + (1-t)y)) & \leq & f(t g(x) + (1-t)g(y)) \\
 & \leq & t f(g(x)) + (1-t)f(g(y))
}$$ 

so $f \circ g: x \mapsto {|x|^p}$ is convex. 
=-- 

+-- {: .proof}
###### Proof of Minkowski's inequality   
Let $u$ and $v$ be unit vectors in $L^p$. By condition 4, it suffices to show that ${|t u + (1-t)v|_p^p} \leq 1$ for all $t \in [0, 1]$. But 
$$\int_X {|t u + (1-t)v|^p} \,d\mu \leq \int_X t{|u|}^p + (1-t){|v|}^p \,d\mu$$ 
by Lemma \ref{convex}. Using $\int {|u|^p} = 1 = \int {|v|^p}$, we are done. 
=-- 

Another commonly seen proof of Minkowski's inequality derives it with the help of [[Hölder's inequality]]; see there for some commentary on this. But this is probably not the first thing one would think of unless one knows the trick, whereas the alternative proof given above seems geometrically motivated and fairly simple. 

## Related concepts

* [[Hölder's inequality]]


## References

* [[Todd Trimble]], _[[toddtrimble:p-norms]]_

* Wikipedia, _[Minowski's inequality](https://en.wikipedia.org/wiki/Minkowski_inequality)_

* [[eom]], _[Minkowski inequality](https://www.encyclopediaofmath.org/index.php/Minkowski_inequality)_


[[!redirects Minkowski inequality]]

[[!redirects Minkowski's inequality]]
[[!redirects Minkowski\'s inequality]]
[[!redirects Minkowski/'s inequality]]
