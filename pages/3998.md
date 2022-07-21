
#Contents#
* automatic table of contents goes here
{:toc}

## Goal

This page deals with the question whether it might be possible to prove the [[irrational number|irrationality]] of $\pi$ by using [[trigonometric identities]].

## Details

We begin with an infinite sequence of functions of some variables $\theta_1,\theta_2,\theta_3,\dots$:

$$
\begin{aligned}
f_0(\theta_1,\theta_2,\theta_3,\dots) &= \sum_{\text{even}\;n \ge 0} (-1)^{n/2} \sum_{|A| = n} \prod_{i \in A} \sin\theta_i \prod_{i \notin A} \cos\theta_i \\
f_1(\theta_1,\theta_2,\theta_3,\dots) &= \sum_{\text{odd}\;n \ge 1} (-1)^{(n-1)/2} \sum_{|A| = n} \prod_{i \in A} \sin\theta_i \prod_{i \notin A} \cos\theta_i \\
f_2(\theta_1,\theta_2,\theta_3,\dots) &= \sum_{\text{even}\;n \ge 2} (-1)^{(n-2)/2} n \sum_{|A| = n} \prod_{i \in A} \sin\theta_i \prod_{i \notin A} \cos\theta_i \\
f_3(\theta_1,\theta_2,\theta_3,\dots) &= \sum_{\text{odd}\;n \ge 3} (-1)^{(n-3)/2} (n-1) \sum_{|A| = n} \prod_{i \in A} \sin\theta_i \prod_{i \notin A} \cos\theta_i \\
f_4(\theta_1,\theta_2,\theta_3,\dots) &= \sum_{\text{even}\;n \ge 4} (-1)^{(n-4)/2} n(n-2) \sum_{|A| = n} \prod_{i \in A} \sin\theta_i \prod_{i \notin A} \cos\theta_i \\
f_5(\theta_1,\theta_2,\theta_3,\dots) &= \sum_{\text{odd}\;n \ge 5} (-1)^{(n-5)/2} (n-1)(n-3) \sum_{|A| = n} \prod_{i \in A} \sin\theta_i \prod_{i \notin A} \cos\theta_i \\
f_6(\theta_1,\theta_2,\theta_3,\dots) &= \sum_{\text{even}\;n \ge 6} (-1)^{(n-6)/2} n(n-2)(n-4) \sum_{|A| = n} \prod_{i \in A} \sin\theta_i \prod_{i \notin A} \cos\theta_i \\
f_7(\theta_1,\theta_2,\theta_3,\dots) &= \sum_{\text{odd}\;n \ge 7} (-1)^{(n-7)/2} (n-1)(n-3)(n-5) \sum_{|A| = n} \prod_{i \in A} \sin\theta_i \prod_{i \notin A} \cos\theta_i \\
& \vdots
\end{aligned}
$$

etc.  In each case we could have said $\text{even}\;n \ge 0$ or $\text{odd}\;n \ge 0$, since the coefficients kill off the terms in which $n$ is smaller than the index---the coefficients are the unique simplest expressions that do that.

* Each of these is a symmetric function of $\theta_1,\theta_2,\theta_3,\dots$.

* 0 is an identity element for each of these, i.e. we have $f_k(0,\theta_2,\theta_3,\theta_4,\dots) = f_k(\theta_2,\theta_3,\theta_4,\dots)$.

* Lemma:
$$
f_k(\theta_1,\theta_2,\theta_3,\theta_4,\theta_5,\dots) - f_k(\theta_1+\theta_2,\theta_3,\theta_4,\theta_5,\dots) = \left.\begin{cases} k & \text{if}\;k \ge 2\;\text{is even} \\
k - 1 & \text{if}\;k \ge 2\;\text{is odd}
\end{cases} \right\} \cdot
 \sin\theta_1\sin\theta_2 f_{k-2}(\theta_3,\theta_4,\theta_5,\dots)
$$
and if $k = 0$ or $1$ then the difference is 0.

* Identities:
$$
\begin{aligned}
f_0(\theta_1,\theta_2,\theta_3,\dots) &= \cos(\theta_1 + \theta_2 + \theta_3 + \cdots). \\
f_1(\theta_1,\theta_2,\theta_3,\dots) &= \sin(\theta_1 + \theta_2 + \theta_3 + \cdots). \\
\text{If}\;\sum_{i \ge 1} \theta_i = \pi,\;\text{then}\;f_2(\theta_1,\theta_2,\theta_3,\dots) &= \sum_{i \ge 1} \sin^2 \theta_i. \\
\text{If}\;\sum_{i \ge 1} \theta_i = \pi,\;\text{then}\;f_3(\theta_1,\theta_2,\theta_3,\dots) &= \sum_{i \ge 1} \frac{\sin(2\theta_i)}{2}.
\end{aligned}
$$

There is a simple geometric interpretation of the expression on the right side of the identity involving  $f_3$.  Suppose $\theta_i, i \ge 1$ are the angles between adjacent diagonals of a polygon inscribed in a circle of unit diameter.  For present purposes we consider the sides of the polygon to be "diagonals".  (All but two of the $\theta_i$ appear at each vertex.  For example, in an octagon, at one vertex the angles are $\theta_1,\dots,\theta_6$ at the next vertex they are $\theta_2,\dots,\theta_7$; at the next they are $\theta_3,\dots,\theta_8$; and then at the next they are $\theta_4,\dots,\theta_8,\theta_1$, and so on.  All eight appear at each vertex if one draws a tangent line to the circle and includes the angles between sides of the polygon and the tangent line.)  Then the value of each side of the identity involving $f_3$ is half the area of the polygon.  Each term on the right side of the identity is half the signed area of a triangle having one vertex at the center of the circle.  As one goes counterclockwise around the polygon, the signed area is positive or negative as the ray from the center is then turning counterclockwise or clockwise.  The terms on the left side may perhaps not admit so simple an interpretation when the number of nonzero $\theta_i$ is more than 4.  The special case involving only three nonzero $\theta_i$ is the well-known (?) identity that says that if $\alpha+\beta+\gamma=\pi$ then $4\sin\alpha\sin\beta\sin\gamma = sin(2\alpha) + \sin(2\beta) + \sin(2\gamma)$.

(Is there any simple geometric interpretation of the identity involving $f_2$?)

### A question

Are these four identities the first four terms in a sequence that continues?

+-- {: .query}
[[Michael Hardy]]:  A student in India whom I encountered via the internet told me that the problem of proving the "conditional identity" that $4\sin\alpha\sin\beta\sin\gamma = sin(2\alpha) + \sin(2\beta) + \sin(2\gamma)$ if $\alpha+\beta+\gamma=\pi$ recurs perennially on the joint entrance exam of the Indian Institutes of Technology.  Hence "well known".
=--

##Inversion formulas

$$
\begin{aligned}
\prod_{i=1}^\infty \cos\theta_i & = f_0 + \frac{1}{2} f_2 + \frac{1}{2 \cdot 4} f_4 + \frac{1}{2 \cdot 4 \cdot 6} f_6 + \frac{1}{2 \cdot 4 \cdot 6 \cdot 8} f_8 + \cdots \\
\sum_{j=1}^\infty \sin\theta_j \prod_{i : i \neq j} \cos\theta_i & = f_1 + \frac{1}{2} f_3 + \frac{1}{2\cdot 4} f_5 + \frac{1}{2\cdot 4\cdot 6} f_7 + \frac{1}{2 \cdot 4 \cdot 6 \cdot 8} f_9 + \cdots \\
\sum_{|A| = 2} \prod_{i \in A} \sin\theta_i \prod_{i \notin A} \cos\theta_i & = \frac{1}{2} \left(f_2 + \frac{1}{2} f_4 + \frac{1}{2\cdot 4} f_6 + \frac{1}{2\cdot 4 \cdot 6} f_8 + \frac{1}{2\cdot 4\cdot 6\cdot 8} f_{10} + \cdots\right) \\
\sum_{|A| = 3} \prod_{i \in A} \sin\theta_i \prod_{i \notin A} \cos\theta_i & = \frac{1}{2} \left(f_3 + \frac{1}{2} f_5 + \frac{1}{2\cdot 4} f_7 + \frac{1}{2\cdot 4 \cdot 6} f_9 + \frac{1}{2\cdot 4\cdot 6\cdot 8} f_{11} + \cdots\right) \\
\sum_{|A| = 4} \prod_{i \in A} \sin\theta_i \prod_{i \notin A} \cos\theta_i & = \frac{1}{2\cdot 4} \left(f_4 + \frac{1}{2} f_6 + \frac{1}{2\cdot 4} f_8 + \frac{1}{2\cdot 4 \cdot 6} f_{10} + \frac{1}{2\cdot 4\cdot 6\cdot 8} f_{12} + \cdots\right) \\
\sum_{|A| = 5} \prod_{i \in A} \sin\theta_i \prod_{i \notin A} \cos\theta_i & = \frac{1}{2\cdot 4} \left(f_5 + \frac{1}{2} f_7 + \frac{1}{2\cdot 4} f_9 + \frac{1}{2\cdot 4 \cdot 6} f_{11} + \frac{1}{2\cdot 4\cdot 6\cdot 8} f_{13} + \cdots\right) \\
& \vdots
\end{aligned}
$$

## What Leonhard Euler and Mary Cartwright did

[[Leonhard Euler]] used something similar to the identities for $f_0$ and $f_1$ in order to derive the [[power-series expansion]]s of the [[sine]] and [[cosine]].  The idea is that to find $\sin x$, one lets $x = \theta+\cdots+\theta$, where $\theta$ is infinitely small and the number of terms is an infinitely large integer, and then apply the identities for $f_0$ and $f_1$.  More precisely, Euler wrote $\cos(n\theta)$ and $\sin(n\theta)$ as functions of $\sin\theta$ and $\cos\theta$ and then supposed $n$ is infinitely large and $n\theta$ is finite.  Then $\sin\theta$ becomes $\theta$ and $\cos\theta$ becomes 1.

If one does with $f_k$, for $k \ge 0$, what Euler did with $f_0$ and $f_1$, one gets an infinite sequence of power series in $x$.  The odd-indexed functions of $x$ in this sequence are the functions $J_n$ that appear in Cartwright's proof of the irrationality of $\pi$.  But in defining those functions, Cartwright used neither trigonometric expressions nor power series.  (The proof was published in an appendix to the third edition of Harold Jeffreys' book ''Scientific Inference''.  It is not in later editions.  It appears in [Wikipedia's article](http://en.wikipedia.org/wiki/Proof_that_%CF%80_is_irrational) on the proof of the irrationality of $\pi$.)

## The main question

Could a proof of the irrationality of $\pi$ using only finitary trigonometric identities be lurking somewhere in all this?  ($\left\{f_k(\theta_1,\dots,\theta_\ell)\right\}_{k,\ell}$ is a doubly indexed sequence each term of which is the a sum of finitely many products of finitely many factors.)