
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model theory
+-- {: .hide}
[[!include model theory - contents]]
=--
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--

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

One sometimes adds axioms for [[order]]; however, this is also definable.  (Citation in Wikipedia; I can\'t quite make it work.)

## Category of models of Robinson arithmetic

A model of Robinson arithmetic is a [[set]] $N$ with an element $0 \in N$, a function $s:N \to N$, and binary operations $(-)+(-):N \times N \to N$ and $(-)\cdot(-):N \times N \to N$, such that 

* for all $x \in N$, $\neg s(x) = 0$

* for all $x, y \in N$, $s(x) = s(y)$ implies $x = y$

* for all $x \in N$, $x = 0$ or there exists $y \in N$ where $x = s(y)$

* for all $x \in N$, $x + 0 = x$

* for all $x, y \in N$, $x + s(y) = s(x+y)$

* for all $x \in N$, $x \cdot 0 = 0$

* for all $x, y \in N$, $x \cdot s(y) = x \cdot y + x$

A [[homomorphism]] of models of Robinson arithmetic $N$ and $N^{'}$ is a function $f:N \to N^{'}$ such that

* $f(0_N) = 0_{N^{'}}$

* for all $x \in N$, $f(s_N(x)) = s_{N^{'}}(f(x))$

* for all $x, y \in N$, $f(x +_N y) = f(x) +_{N^{'}} f(y)$

* for all $x, y \in N$, $f(x \cdot_N y) = f(x) \cdot_{N^{'}} f(y)$

The [[category]] of models of Robinson arithmetic in a [[universe]] $\mathcal{U}$ is the category 
$$\mathrm{RobinsonArithmetics}_\mathcal{U}$$ 
whose objects 
$$Ob(\mathrm{RobinsonArithmetics}_\mathcal{U})$$ 
are the models of Nelson arithmetic, and for any two objects 
$$A \in Ob(\mathrm{RobinsonArithmetics}_\mathcal{U})$$ 
and 
$$B \in Ob(\mathrm{RobinsonArithmetics}_\mathcal{U})$$ 
the [[morphisms]] 
$$Mor_{\mathrm{RobinsonArithmetics}_\mathcal{U}}(A, B)$$ 
are the homomorphisms of models of Nelson arithmetic as defined above. 

If $\mathcal{U}$ satisfies the [[axiom of finiteness]], then the category $\mathrm{RobinsonArithmetics}_\mathcal{U}$ has no [[initial object]] and is an [[empty category]]. 

## Theorems

Despite the considerable weakening of what can be proved, the formulas are the same as in Peano arithmetic, and all the background number theory (the [[Chinese remainder theorem]] and the like) needed to develop [[Gödel codings]], [[incompleteness theorems]], and so on is still there. In some sense the axioms are a minimal set needed to carry out this program (and in fact this was in large part the motivation for Robinson).


## Models

Unlike the case for Peano arithmetic, system $Q$ admits tractable computable [[nonstandard model|nonstandard]] [[models]].

The simplest consists of a single nonstandard number $\infty$ (in addition to all of the standard numbers, which exist in every model), with the rules (where $n$ is a standard number):

* $s(\infty) = \infty$,
* $n + \infty, \infty + n, \infty + \infty = \infty$,
* $0 \cdot \infty, \infty \cdot 0 = 0$, $s(n) \cdot \infty, \infty \cdot s(n), \infty \cdot \infty = \infty$.

## See also

* [[Peano arithmetic]]
* [[finite mathematics]]

## References

* Wikipedia, _[Robinson arithmetic](http://en.wikipedia.org/wiki/Robinson_arithmetic)_


[[!redirects Robinson arithmetic]]
