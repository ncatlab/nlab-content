
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

# Contents #
* table of contents 
{: toc}

## Idea

An extension of a [[fragment]] of [[first-order theory|first order]] [[Peano arithmetic]] as described in [Edward Nelson's paper](#Nelson).

## Definition 

Nelson arithmetic is done by extending the fragment of first order [[Peano arithmetic]] consisting of the following [[axioms]]:

1. $\forall_x \neg s(x) = 0$; 

1. $\forall_{x, y} (s(x) = s(y)) \Rightarrow (x = y)$; 

1. $\forall_x x + 0 = x$, 

1. $\forall_{x, y} x + s(y) = s(x+y)$; 

1. $\forall_x x \cdot 0 = 0$; 

1. $\forall_{x, y} x \cdot s(y) = x \cdot y + x$; 

with a [[predicate]] $\mathcal{C}$ satisfying the following axioms

1. $\mathcal{C}(0)$; 

1. $\forall_{x} \mathcal{C}(x) \Rightarrow \mathcal{C}(s(x))$; 

The predicate $\mathcal{C}$ is supposed to refer to "counting numbers", in the familiar intuitive sense that the [[natural numbers]] are supposed to be for counting. Nelson states in his paper that

> It follows (...) that $0$, $S0$, $SS0$, and so forth, are counting numbers. But we cannot prove that all numbers are counting numbers.

And indeed, there are many [[ nonstandard model of arithmetic|non-standard models of Nelson arithmetic]] where not every number in the model is a "counting number"/"natural number". One example of such a model is the non-negative [[rational numbers]], where zero, [[addition]], and [[multiplication]] are the usual operations on the non-negative rational numbers, $s(n) = n + 1$, and $\mathcal{C}(a)$ is defined to be false for non-negative rational numbers [[denial inequality|not equal to]] every natural number:

$$\forall a \in \{b \in \mathbb{Q} \vert b \geq 0\}. (\forall n \in \mathbb{N}.a \neq n) \implies \neg \mathcal{C}(a)$$

On the other extreme, one could define a model where $\mathcal{C}(a)$ is true for all numbers $a$ in the model, and thus all number trivially are "counting numbers", though in that case the "counting numbers" interpretation of the predicate doesn't make much intuitive sense anymore. 

## Models

We work in a [[dependent type theory]] with [[identity types]], [[empty type]], [[unit type]], and [[booleans]]. A model of Nelson arithmetic is a [[type]] $N$ with 

* an element $0:N$, 
* a function $s:N \to N$, 
* a function $(-)+(-):N \times N \to N$, 
* a function $(-)\cdot(-):N \times N \to N$, 
* a type family $\mathcal{C}(-)$
* a dependent function 
$$\alpha: \prod_{x:N} \prod_{a:\mathcal{C}(x)} \prod_{b:\mathcal{C}(x)} a =_{\mathcal{C}(x)} b$$
* a dependent function 
$$\beta: \prod_{x:N} (s(x) = 0) \to \mathbb{0}$$ 
* a dependent function
$$\gamma: \prod_{x:N} \prod_{y:N} s(x) = s(y) \to x = y$$
* a dependent function
$$\delta: \prod_{x:N} x + 0 = x$$
* a dependent function
$$\epsilon: \prod_{x:N} \prod_{y:N} x + s(y) = s(x+y)$$
* a dependent function
$$\zeta: \prod_{x:N} x \cdot 0 = 0$$
* a dependent function
$$\eta: \prod_{x:N} \prod_{y:N} x \cdot s(y) = x \cdot y + x$$
* a term
$$\iota: \mathcal{C}(0)$$
* a dependent function
$$\kappa: \prod_{x:N} \mathcal{C}(x) \to \mathcal{C}(s(x))$$
* a dependent function 
$$\tau_0: \prod_{x:N} \prod_{y:N}  \prod_{a:x =_N y} \prod_{b:x =_N y} a =_{x = y} b$$

A homomorphism of models of Nelson arithmetic $N$ and $N^{'}$ is a function $f:N \to N^{'}$ with 

* a dependent function 
$$f_\mathcal{C}:\prod_{x:N} \mathcal{C}(x) \to \mathcal{C}(f(x))$$
* a term
$$a:f(0) = 0$$
* a dependent function 
$$b:\prod_{x:N} f(s(x)) = s(f(x))$$
* a dependent function 
$$c:\prod_{x:N} \prod_{y:N} f(x + y) = f(x) + f(y)$$
* a dependent function 
$$d:\prod_{x:N} \prod_{y:N} f(x \cdot y) = f(x) \cdot f(y)$$
* a dependent function 

## Example models

* The set of [[natural numbers]] $\mathbb{N}$ is the initial model of Nelson arithmetic in the [[category]] of models of Nelson arithmetic. 

* The set of non-negative [[rational numbers]] $\mathbb{Q}_{\geq 0}$ with $s(q) \coloneqq q + 1$ and $\mathcal{C}(q)$ for all $q \in \mathbb{Q}_{\geq 0}$ is a model of Nelson arithmetic. 

* The set of non-negative [[real numbers]] $\mathbb{R}_{\geq 0}$ with $s(r) \coloneqq r + 1$ and $\mathcal{C}(r)$ for all $r \in \mathbb{R}_{\geq 0}$ is a model of Nelson arithmetic. 

* Any [[free object|free]] [[commutative algebra|commutative $\mathbb{N}$-algebra]] on a generating set $S$ with $s(r) \coloneqq r + 1$ and $\mathcal{C}(r)$ for all $r \in \mathbb{N}[S]$, is a model of Nelson arithmetic. 

* The [[disjoint union]] set $\mathbb{N} + \mathbb{1}$ where $*:\mathbb{1}$ is the [[singleton]] such that 

1. $s(*) = *$

1. $\forall a \in \mathbb{N}. * + a = *$

1. $\forall a \in \mathbb{N}. a + * = a$

1. $* + * = *$

1. $\forall a \in \mathbb{N}. * \cdot a = *$

1. $\forall a \in \mathbb{N}. a \cdot * = a$

1. $* \cdot * = *$ 

1. $\mathcal{C}(*)$ 

is a model of Nelson arithmetic. 

* The set $\mathbb{2} \times \mathbb{N} + \mathbb{1}$ where $*:\mathbb{1}$  is the [[singleton]] and $0:\mathbb{2}$, and $1:\mathbb{2}$ is the [[booleans]] such that 

1. $\forall x \in \mathbb{2} \times \mathbb{N}. \neg(s(x) = (0,0))$

1. $\forall x \in \mathbb{2} \times \mathbb{N}. \neg(s(x) = (0,1))$

1. $\forall a \in \mathbb{N}. s((0,a)) = (0,s(a))$

1. $\forall a \in \mathbb{N}. s((1,a)) = (1,s(a))$

1. $\forall a \in \mathbb{N}. \forall b \in \mathbb{N}. (0,a) + (0,b) = (0,a+b)$

1. $\forall a \in \mathbb{N}. \forall b \in \mathbb{N}. (0,a) + (1,b) = *$

1. $\forall a \in \mathbb{N}. \forall b \in \mathbb{N}. (1,a) + (0,b) = *$

1. $\forall a \in \mathbb{N}. \forall b \in \mathbb{N}. (1,a) + (1,b) = (1,a+b)$

1. $\forall a \in \mathbb{N}. \forall b \in \mathbb{N}. (0,a) \cdot (0,b) = (0,a\cdot b)$

1. $\forall a \in \mathbb{N}. \forall b \in \mathbb{N}. (0,a) \cdot (1,b) = *$

1. $\forall a \in \mathbb{N}. \forall b \in \mathbb{N}. (1,a) \cdot (0,b) = *$

1. $\forall a \in \mathbb{N}. \forall b \in \mathbb{N}. (1,a) \cdot (1,b) = (1,a \cdot b)$

1. $s(*) = *$

1. $\forall x \in \mathbb{2} \times \mathbb{N}. * + a = *$

1. $\forall x \in \mathbb{2} \times \mathbb{N}. a + * = a$

1. $* + * = *$

1. $\forall x \in \mathbb{2} \times \mathbb{N}. * \cdot a = *$

1. $\forall x \in \mathbb{2} \times \mathbb{N}. a \cdot * = a$

1. $* \cdot * = *$ 

1. $\mathcal{C}(*)$

1. $\mathcal{C}((0,0))$

1. $\mathcal{C}((1,0))$

is a model of Nelson arithmetic. 

## See also

* [[Peano arithmetic]]
* [[finite mathematics]]

## References 

* {#Nelson} [[Edward Nelson]], _Warning Signs of a Possible Collapse of Contemporary Mathematics_ ([pdf](https://web.math.princeton.edu/~nelson/papers/warn.pdf))

