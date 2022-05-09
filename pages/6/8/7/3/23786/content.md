
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

### Counting numbers

The predicate $\mathcal{C}$ is supposed to refer to "counting numbers", in the familiar intuitive sense that the [[natural numbers]] are supposed to be for counting. Nelson states in his paper that

> It follows (...) that $0$, $S0$, $SS0$, and so forth, are counting numbers. But we cannot prove that all numbers are counting numbers.

And indeed, there are many [[nonstandard model of arithmetic|non-standard models of Nelson arithmetic]] where not every number in the model is a "counting number"/"natural number". One example of such a model is the non-negative [[rational numbers]], where zero, [[addition]], and [[multiplication]] are the usual operations on the non-negative rational numbers, $s(n) = n + 1$, and $\mathcal{C}(a)$ is defined to be false for non-negative rational numbers [[denial inequality|not equal to]] a natural number:

$$\forall a \in \{b \in \mathbb{Q} \vert b \geq 0\}. (\forall n \in \mathbb{N}.a \neq n) \implies \neg \mathcal{C}(a)$$

An [[uncountable set|uncountable]] model of Nelson arithmetic where not every number in the model is a "counting number" is the non-negative [[Dedekind real numbers]], where zero, [[addition]], and [[multiplication]] are the usual operations on the non-negative rational numbers, $s(n) = n + 1$, and $\mathcal{C}(a)$ is defined to be false for non-negative rational numbers whose [[distance]] from every natural number is positive:

$$\forall a \in \{b \in \mathbb{R} \vert b \geq 0\}. (\forall n \in \mathbb{N}.\vert a - n \vert \gt 0) \implies \neg \mathcal{C}(a)$$

On the other extreme, one could define a model where $\mathcal{C}(a)$ is true for all numbers $a$ in the model, and thus all number trivially are "counting numbers", though in that case the "counting numbers" interpretation of the predicate doesn't make much intuitive sense anymore. 

### Additionable, multiplicable, and exponentiable numbers

We define the predicate $\mathcal{A}$ on a model of Nelson arithmetic $N$ to be that $\mathcal{A}(x)$ if for all $x \in N$ such that $\mathcal{C}(x)$, and for all $y \in N$, $\mathcal{C}(y + x)$. Nelson referred to elements where $\mathcal{A}(x)$ is true as "additionable numbers"; however, these are better interpreted as "additionable counting numbers", as Nelson is really talking about the natural numbers. Missing from Nelson's paper is a proof that addition of "additionable numbers" is associative. 

In the same vein, we could define the predicate $\mathcal{M}$ on a model of Nelson arithmetic $N$ to be that $\mathcal{M}(x)$ if for all $x \in N$ such that $\mathcal{C}(x)$, and for all $y \in N$, $\mathcal{C}(y \cdot x)$. Nelson referred to elements where $\mathcal{M}(x)$ is true as "multiplicable numbers"; however, similarly to "additionable counting numbers" these are better interpreted as "multiplicable counting numbers", as Nelson is really talking about the natural numbers. Missing from Nelson's paper is a proof that multiplication of "multiplicable numbers" is associative. 

Now, suppose that there is a [[binary function]] $(-)\uparrow(-):N \times N \to N$ called "exponentiation" such that

* for all $x \in N$, $x \uparrow 0 = s(0)$ 

* for all $x, y \in N$, $x \uparrow s(y) = x \cdot x \uparrow y$

Nelson states that 

> If we attempt to define “exponentiable number” in the same spirit, we are unable to prove that if $x_1$ and $x_2$ are exponentiable numbers then so is $x_1 \uparrow x_2$. There is a radical difference between addition and multiplication on the one hand and exponentiation, superexponentiation, and so forth, on the other hand. The obstacle is that exponentiation is not associative; for example, $(2 \uparrow 2) \uparrow 3 = 4 \uparrow 3 = 64$ whereas $2 \uparrow (2 \uparrow 3) = 2 \uparrow 8 = 256$. For any specific numeral SSS. . . 0 we can indeed prove that it is an exponentiable number, but we cannot prove that the world of exponentiable numbers is closed under exponentiation.

The categorification of Nelson's argument to the [[category]] of [[sets]] would say that the [[function set]] between two [[exponentiable object|exponentiable]] [[finite sets]] cannot be proved to be exponentiable, and thus [[FinSet]] cannot be proved to be [[cartesian closed]], and cannot be proved to be a [[elementary topos]] or a [[Π-pretopos]]. 

### Ultrafinitism 

Categorifying the current axioms to the category of sets, the finite sets (represented by the sets $S$ in which $\mathcal{C}(S)$ is [[inhabited]]) could not be proven to be [[symmetric monoidal]] with respect to either the [[disjoint union]] or the [[Cartesian product]]. Thus, Nelson's [[Set]] forms a framework of mathematics, which is sometimes called "ultrafinite mathematics", that is significantly weaker than [[predicative mathematics|strongly predicative]] [[constructive mathematics|constructive]] [[finite mathematics]]. However, the [[subcategories]] of right-additive finite sets $(S, \alpha:\mathcal{A}(S))$ and right-multiplicative finite sets $(S, \mu:\mathcal{M}(S))$ can be proven to be [[symmetric monoidal]]. 

## Category of models of Nelson arithmetic

A model of Nelson arithmetic is a [[set]] $N$ with an element $0 \in N$, a function $s:N \to N$, binary operations $(-)+(-):N \times N \to N$ and $(-)\cdot(-):N \times N \to N$, and a predicate $\mathcal{C}:N \to \mathrm{Prop}$, such that 

* for all $x \in N$, $\neg s(x) = 0$

* for all $x, y \in N$, $s(x) = s(y)$ implies $x = y$

* for all $x \in N$, $x + 0 = x$

* for all $x, y \in N$, $x + s(y) = s(x+y)$

* for all $x \in N$, $x \cdot 0 = 0$

* for all $x, y \in N$, $x \cdot s(y) = x \cdot y + x$

* $\mathcal{C}(0)$

* for all $x \in N$, $\mathcal{C}(x)$ implies $\mathcal{C}(s(x))$; 

A [[homomorphism]] of models of Nelson arithmetic $N$ and $N^{'}$ is a function $f:N \to N^{'}$ such that

* $f(0_N) = 0_{N^{'}}$

* for all $x \in N$, $\mathcal{C}_N(x)$ implies $\mathcal{C}_{N^{'}}(f(x))$

* for all $x \in N$, $f(s_N(x)) = s_{N^{'}}(f(x))$

* for all $x, y \in N$, $f(x +_N y) = f(x) +_{N^{'}} f(y)$

* for all $x, y \in N$, $f(x \cdot_N y) = f(x) \cdot_{N^{'}} f(y)$

The [[category]] of models of Nelson arithmetic in a [[universe]] $\mathcal{U}$ is the category $\mathrm{NelsonArithmetics}_\mathcal{U}$ whose objects $Ob(\mathrm{NelsonArithmetics}_\mathcal{U})$ are the models of Nelson arithmetic, and for any two objects $A \in Ob(\mathrm{NelsonArithmetics}_\mathcal{U})$ and $B \in Ob(\mathrm{NelsonArithmetics}_\mathcal{U})$ the [[morphisms]] $Mor_{\mathrm{NelsonArithmetics}_\mathcal{U}}(A, B)$ are the homomorphisms of models of Nelson arithmetic as defined above. 

If $\mathcal{U}$ satisfies the [[axiom of finiteness]], then the category $\mathrm{NelsonArithmetics}_\mathcal{U}$ has no [[initial object]] and is an [[empty category]]. 

## Standard and nonstandard models

* The set of [[natural numbers]] $\mathbb{N}$ is the standard model of Nelson arithmetic, and is the initial model of Nelson arithmetic in the [[category]] of models of Nelson arithmetic. 

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

## Groupoidal categorification

The [[groupoidal categorification]] of Nelson arithmetic is a [[groupoid]] $\mathcal{G}$ with 

* an object $0 \in \mathcal{G}$, 

* a [[functor]] $S:\mathcal{G} \to \mathcal{G}$, 

* a functor $(-)+(-):\mathcal{G} \times \mathcal{G} \to \mathcal{G}$ 

* a functor $(-)\cdot(-):\mathcal{G} \times \mathcal{G} \to \mathcal{G}$

* for all $A \in \mathcal{G}$, a function set $(S(A) \cong 0) \to \emptyset$ from the [[set]] of [[isomorphisms]] $S(A) \cong 0$ to the [[empty set]]

* for all $A, B \in \mathcal{G}$, a function set $(S(A) \cong S(B)) \to (A \cong B)$ from the set of isomorphism $S(A) \cong S(B)$ to the set of isomorphisms $A \cong B$

* for all $A \in \mathcal{G}$, a set of isomorphisms $A + 0 \cong A$

* for all $A, B \in \mathcal{G}$, a set of isomorphisms $A + S(B) \cong S(A+B)$

* for all $A \in \mathcal{G}$, a set of isomorphisms $A \cdot 0 \cong A$

* for all $A, B \in \mathcal{G}$, a set of isomorphisms $A \cdot S(B) \cong A \cdot B + A$

* a [[Set]]-valued functor $\mathcal{C}:\mathcal{G} \to \mathrm{Set}$ 

* an element $p \in \mathcal{C}(0)$ 

* for all $A \in \mathcal{G}$, a function $f_A:\mathcal{C}(A) \to \mathcal{C}(S(A))$ 

## See also

* [[Peano arithmetic]]
* [[finite mathematics]]

## References 

* {#Nelson} [[Edward Nelson]], _Warning Signs of a Possible Collapse of Contemporary Mathematics_ ([pdf](https://web.math.princeton.edu/~nelson/papers/warn.pdf))

