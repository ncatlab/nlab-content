
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

* The type of natural numbers $\mathbb{N}$ is the initial model of Nelson arithmetic in the category of models of Nelson arithmetic. 

* The type $\mathbb{N} + \mathbb{1}$ where $*:\mathbb{1}$ is the [[unit type]] such that 
$$s(*) = *$$
$$\prod_{a:\mathbb{N}} * + a = *$$
$$\prod_{a:\mathbb{N}} a + * = a$$
$$* + * = *$$
$$\prod_{a:\mathbb{N}} * \cdot a = *$$
$$\prod_{a:\mathbb{N}} a \cdot * = a$$
$$* \cdot * = *$$ 
$$\mathcal{C}(*)$$
is a model of Nelson arithmetic. 

* The type $\mathbb{2} \times \mathbb{N} + \mathbb{1}$ where $*:\mathbb{1}$  is the [[unit type]] and $0:\mathbb{2}$, and $1:\mathbb{2}$ is the [[booleans]] such that 
$$\prod_{x:\mathbb{2} \times \mathbb{N}} (s(x) = (0,0)) \to \mathbb{0}$$
$$\prod_{x:\mathbb{2} \times \mathbb{N}} (s(x) = (0,1)) \to \mathbb{0}$$
$$\prod_{a:\mathbb{N}} s((0,a)) = (0,s(a))$$
$$\prod_{a:\mathbb{N}} s((1,a)) = (1,s(a))$$
$$\prod_{a:\mathbb{N}} \prod_{b:\mathbb{N}} = (0,a) + (0,b) = (0,a+b)$$
$$\prod_{a:\mathbb{N}} \prod_{b:\mathbb{N}} = (0,a) + (1,b) = *$$
$$\prod_{a:\mathbb{N}} \prod_{b:\mathbb{N}} = (1,a) + (0,b) = *$$
$$\prod_{a:\mathbb{N}} \prod_{b:\mathbb{N}} = (1,a) + (1,b) = (1,a+b)$$
$$\prod_{a:\mathbb{N}} \prod_{b:\mathbb{N}} = (0,a) \cdot (0,b) = (0,a\cdot b)$$
$$\prod_{a:\mathbb{N}} \prod_{b:\mathbb{N}} = (0,a) \cdot (1,b) = *$$
$$\prod_{a:\mathbb{N}} \prod_{b:\mathbb{N}} = (1,a) \cdot (0,b) = *$$
$$\prod_{a:\mathbb{N}} \prod_{b:\mathbb{N}} = (1,a) \cdot (1,b) = (1,a \cdot b)$$
$$s(*) = *$$
$$\prod_{a:\mathbb{2} \times \mathbb{N}} * + a = *$$
$$\prod_{a:\mathbb{2} \times \mathbb{N}} a + * = a$$
$$* + * = *$$
$$\prod_{a:\mathbb{2} \times \mathbb{N}} * \cdot a = *$$
$$\prod_{a:\mathbb{2} \times \mathbb{N}} a \cdot * = a$$
$$* \cdot * = *$$ 
$$\mathcal{C}(*)$$
$$\mathcal{C}((0,0))$$
$$\mathcal{C}((1,0))$$
is a model of Nelson arithmetic. 

## See also

* [[Peano arithmetic]]
* [[finite mathematics]]

## References 

* {#Nelson} [[Edward Nelson]], _Warning Signs of a Possible Collapse of Contemporary Mathematics_ ([pdf](https://web.math.princeton.edu/~nelson/papers/warn.pdf))

