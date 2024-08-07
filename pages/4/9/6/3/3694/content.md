
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Equality and Equivalence
+-- {: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

An **ordinary differential equation** is a [[differential equation]] involving [[derivatives]] of a [[function]] with respect to one argument only, i.e. the function is on a [[manifold]] only of [[dimension]] $d = 1$. This function can be vector valued, what is sometimes viewed as a system of possibly coupled equations; still all of them have the derivatives taken with respect to the same parameter. (Note that a higher-order differential equation can be turned into a system of first-order equations.)


## Existence and uniqueness (Picard--Lindel&#246;f theorem) 

A basic theorem concerns existence and uniqueness of local solutions to initial value problems. Let $X$ be a [[Banach space]]; given $(t_0, y_0) \in \mathbb{R} \times X$ and $a, r \gt 0$, put $Q \coloneqq [t_0 - a, t_0 + a] \times B_r(y_0)$m where $B_r(y_0)$ is the closed [[ball]] in $X$ of radius $r$ about $y_0$.

+-- {: .num_theorem}
###### Theorem 
**(Picard--Lindel&#246;f)** 
Suppose $f: Q \to X$ is a [[function]] satisfying the following conditions: 

* ([[continuous function|Continuity]] in $t$): Given any $x \in B_r(y_0)$, the function $f(-,x)$ (that is $t \mapsto f(t, x)$) is continuous from $[t_0 - a, t_0 + a]$ to $X$.

* ([[Lipschitz continuous function|Lipschitz continuity]] in $y$): There is a Lipschitz constant $L$ such that 
$$ {\|f(t, x) - f(t, x')\|} \leq L{\|x - x'\|} $$ 
for all $(t, x) \in Q$; 

* ([[bounded function|Boundedness]]): There is a constant $K$ such that $\sup_{(t, x) \in Q} \|f(t, x)\| \leq K$. 

Then for any $c \leq \min(a, r/K)$, there exists [[uniqueness|exactly one]] solution $y: [t_0 - c, t_0 + c] \to X$ to the initial value problem 

$$ y'(t) = f(t, y(t)), \qquad y(t_0) = y_0 .$$ 
=--

+-- {: .proof} 
###### Proof sketch

We will define an [[infinite sequence]] of approximate solutions to the problem, prove that its [[convergence|limit]] exists, prove that this limit is an exact solution, and prove that this solution is unique.

1. The infinite sequence is given by __Picard iteration__:
Starting with the given constant $y_0$, [[recursion|recursively]] define

   $$ y_{n+1}(t) \coloneqq y_0 + \int_{t=t_0} f(t, y_n(t)) \,\mathrm{d}t ;$$

   that is, $y_{n+1}$ is that [[indefinite integral]] of $f(-,y_n)$ that takes the correct initial value.  (To define $y_1$, use [[abuse of notation]] to interpret $y_0(t)$ as $y_0$; that is, think of $y_0$ as a [[constant function]].)  To prove that this integral exists, use the continuity conditions and an [[inductive proof]] that each $y_n$ is continuous to show that we are integrating a continuous function.

2. Thinking of Picard iteration as an operator between Banach spaces of continuous functions, use Lipschitz continuity and boundedness to show that the [[Banach fixed point theorem]] applies, so that the sequence $(y_1, y_2, \ldots)$ [[uniform convergence|uniformly converges]] to a limit $y$.

3. Since uniform convergence of continuous functions behaves well with integration, the limiting instance of Picard iteration holds:

   $$ y(t) = y_0 + \int_{t=t_0} f(t, y(t)) \,\mathrm{d}t .$$

   By differentiating with respect to $t$, and by evaluating at $t_0$, we confirm that $y$ is a solution of the initial value problem.

4. Given any putative solution $z$, apply [[Groenwall inequality|Grönwall's inequality]] to $z - y$ to prove that $z = y$.
=--

## See also

* [[inverse function theorem]]
* [[real quadratic function]]
* [[continuous square root]]
* [[Runge-Kutta method]]
* [[Chen iterated integral]]

## References

* The [English Wikipedia](https://en.wikipedia.org/wiki/Picard%E2%80%93Lindel%C3%B6f_theorem) has a more detailed proof.  (They assume that $X$ is $\mathbb{R}$, but this is not essential.)


[[!redirects ordinary differential equation]]
[[!redirects ordinary differential equations]]
[[!redirects ODE]]
[[!redirects ODEs]]
[[!redirects ODE-s]]
[[!redirects ODE's]]
[[!redirects ODE\'s]]
[[!redirects ODE/'s]]
[[!redirects ODE's]]

[[!redirects Picard iteration]]
[[!redirects Picard iterate]]
[[!redirects Picard iterates]]

[[!redirects Picard-Lindelof theorem]]
[[!redirects Picard-Lindelöf theorem]]
[[!redirects Picard-Lindeloef theorem]]
[[!redirects Picard–Lindelof theorem]]
[[!redirects Picard–Lindelöf theorem]]
[[!redirects Picard–Lindeloef theorem]]
[[!redirects Picard--Lindelof theorem]]
[[!redirects Picard--Lindelöf theorem]]
[[!redirects Picard--Lindeloef theorem]]
