
# Robinson arithmetic
* table of contents
{: toc}

## Idea

Robinson arithmetic (after Raphael M. Robinson) is a finitely axiomatized weakening of [[Peano arithmetic]] in which the [[induction schema]] is dropped and minimal axioms remain. 


## Definition 

Robinson arithmetic, also denoted by Q, is a [[first-order theory]] whose [[signature]] is that of first-order Peano arithmetic: it consists of a constant $0$, an unary function symbol $s$, and binary function symbols $+, \cdot$. The axioms are 

1. $\forall_x \neg s(x) = 0$; 

2. $\forall_{x, y} s(x) = s(y) \Rightarrow x = y$; 

3. $\forall_x x = 0 \vee \exists_y x = s(y)$; 

4. $\forall_x x + 0 = x$, 

5. $\forall_{x, y} x + s(y) = s(x+y)$; 

6. $\forall_x x \cdot 0 = 0$; 

7. $\forall_{x, y} x \cdot s(y) = x \cdot y + x$. 

There is no [[induction scheme]].

One sometimes adds axioms for [[order]]; however, this is also definable.  Specifically, $x \lt y$ may be defined to mean that $y = s(z) + x$ for some $z$; and $x \leq y$ may be defined to mean that $y = z + x$ for some $z$.


## Theorems

Despite the considerable weakening of what can be proved, the formulas are the same as in Peano arithmetic, and all the background number theory (the [[Chinese remainder theorem]] and the like) needed to develop [[Gödel codings]], [[incompleteness theorems]], and so on is still there. In some sense the axioms are a minimal set needed to carry out this program (and in fact this was in large part the motivation for Robinson).


## Models

Unlike the case for Peano arithmetic, system $Q$ admits tractable computable [[nonstandard model|nonstandard]] [[models]].

The simplest consists of a single nonstandard number $\infty$ (in addition to all of the standard numbers, which exist in every model), with the rules (where $n$ is a standard number):

* $s(\infty) = \infty$,
* $n + \infty, \infty + n, \infty + \infty = \infty$,
* $0 \cdot \infty, \infty \cdot 0 = 0$, $s(n) \cdot \infty, \infty \cdot s(n), \infty \cdot \infty = \infty$.


## References

* Wikipedia, _[Robinson arithmetic](http://en.wikipedia.org/wiki/Robinson_arithmetic)_


[[!redirects Robinson arithmetic]]
