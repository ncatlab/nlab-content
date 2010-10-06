
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The **delooping hypothesis** is one of the "guiding hypotheses of higher category theory."  Like the [[homotopy hypothesis]], it is generally accepted to be a "litmus test" that any suitable definition of [[n-category]] should satisfy.  It states that:

* [[k-tuply monoidal n-category|k-tuply monoidal n-categories]] can be identified with $(k-j)$-tuply monoidal, $(j-1)$-[[k-tuply connected n-category|simply connected]] $(n+j)$-categories, for any $0\le j \le k$.

The identification involves a degree shift: the $i$-morphisms of a $k$-tuply monoidal $n$-category become $(i+j)$-morphisms in the associated $(k-j)$-tuply monoidal $(n+j)$-category.

Here _$j$-(simply) connected_ means that any two parallel $i$-morphisms are [[equivalence|equivalent]] for $i \leq j$.  Also, _$0$-tuply monoidal_ is interpreted as meaning [[pointed object|pointed]].  We may also allow $n$ to be of the form [[(n,r)-category|(n,r)]] or $(\infty,r)$, with the usual conventions that $(n,r)+j=(n+j,r+j)$, $\infty+j=\infty$, and so on.  In particular, taking $j=k$ we have:

* $k$-tuply monoidal $n$-categories can be identified with pointed $(k-1)$-connected $(n+k)$-categories.

The $(n+j)$-category associated to a $k$-tuply monoidal $n$-category $C$ is called its **$j$-fold delooping** and sometimes written $B^j C$.  Conversely, any $k$-tuply monoidal $n$-category $C$ with a point $*\in C$ has a [[loop space object]] $\Omega C = C(*,*)$ which is a $(k+1)$-tuply monoidal $(n-1)$-category.


## Remarks

* Not infrequently the delooping hypothesis is used to supply a _definition_ of "$k$-tuply monoidal $n$-category."  See [[k-tuply monoidal n-category]] for an investigation in low dimensions.

* The delooping hypothesis is closely related to the [[stabilization hypothesis]].  In delooping language, the stabilization hypothesis says that once you have an $n$-category that can be delooped $n+2$ times, it can automatically be delooped infinitely many times.

* In low dimensions, the delooping hypothesis is a special case of the [[michaelshulman:exactness hypothesis|exactness hypothesis]].


## In homotopy theory

A "groupoidal" version of the delooping hypothesis may be stated as

* $k$-[[k-tuply groupal n-groupoid|tuply groupal]] $n$-groupoids can be identified with $(k-j)$-tuply groupal $(j-1)$-connected $(n+j)$-groupoids, for $0\le j\le k$.

Here "groupal" means "monoidal and such that all objects have inverses."  (This can actually be seen as a special case of the delooping hypothesis for $k$-tuply monoidal $(n,r)$-categories with $r$ set to $-1$.)

When $n=\infty$ the groupoidal delooping hypothesis can be interpreted (via the [[homotopy hypothesis]]) as a standard result of classical [[homotopy theory]]: "grouplike $E_k$-spaces" can be delooped $k$ times.  In particular, grouplike $A_\infty$-[[A-infinity-space|spaces]] can be delooped once, and grouplike $E_\infty$-[[E-infinity-space|spaces]] can be delooped infinitely many times (producing a [[spectrum]]).

Non-grouplike $A_\infty$-spaces can also be "delooped" in classical homotopy theory, but can only be recovered from their delooping up to [[group completion]].  This is because classical homotopy theory only works with $(\infty,0)$-categories, while the higher-categorical delooping of a non-grouplike $A_\infty$-space (that is, a monoidal $(\infty,0)$-category) should be an $(\infty,1)$-category, not an $(\infty,0)$-category.
