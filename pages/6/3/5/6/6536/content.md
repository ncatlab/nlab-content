
# Positive $n$-forms
* table of contents
{: toc}

## Idea

Let $X$ be an [[orientation|oriented]] $n$-[[dimension|dimensional]] [[differentiable manifold]].  The $n$-[[differential form|forms]] on $X$ have a [[partial order]] $\leq$, which we define (via subtraction) through the notion of positive $n$-form.  This makes the [[line bundle]] of $n$-forms on $X$ into an [[oriented line bundle]].


## Definitions

An $n$-form $\omega$ is __positive semidefinite__ or just __positive__ (denoted $\omega \geq 0$) if the following equivalent conditions hold:

*  the [[integral]] of $\omega$ on any [[open submanifold]] of $X$ is nonnegative;
*  the coordinate of $\omega$ in any oriented local [[coordinate system]] on $X$ is nonnegative;
*  the value of $\omega$ at any point $p$, when applied to any positively oriented collection of $n$ [[tangent vectors]] at $p$, is nonnegative.

Supposing $X$ is unoriented, an $n$-[[pseudoform]] $\omega$ is __positive semidefinite__ if the following equivalent conditions hold:

*  the [[integral]] of $\omega$ on any [[open submanifold]] of $X$ is nonnegative;
*  the coordinate of $\omega$ in any local [[coordinate system]] on $X$ is nonnegative;
*  the value of $\omega$ at any point $p$, when applied relative to either local orientation $o$ at $p$ to any $o$-oriented collection of $n$ [[tangent vectors]] at $p$, is nonnegative.

Arguably, positivity of pseudoforms is fundamental; an orientation allows one to interpret forms as pseudoforms.

A (pseudo)-form is __positive definite__ (denoted $\omega \gt 0$) if it is also nondegenerate (nowhere zero), or equivalently if the conditions above hold with "strictly positive" in place of "nonzero" (taking integrals over only [[inhabited subset|inhabited]] submanifolds).  A positive definite form can be interpreted as a [[volume form|volume]] (pseudo)-form on $X$.


## Properties

If $X$ is oriented, then every $n$-form $\omega$ has an [[absolute value]] ${|\omega|}$, which is a positive $n$-form.  However, even if $\omega$ is [[smooth map|smooth]], still ${|\omega|}$ may only be [[continuous map|continuous]].  However, if $\omega$ is nondegenerate, then not only will ${|\omega|}$ be also nondegenerate, it will be smooth (if $\omega$ is).  Even if $X$ is unoriented, still any $n$-form or $n$-pseudoform $\omega$ will have a positive $n$-pseudoform ${|\omega|}$ as absolute value.


[[!redirects positive n-form]]
[[!redirects positive n-forms]]
[[!redirects positive n-pseudoform]]
[[!redirects positive n-pseudoforms]]

[[!redirects positive definite n-form]]
[[!redirects positive definite n-forms]]
[[!redirects positive definite n-pseudoform]]
[[!redirects positive definite n-pseudoforms]]
