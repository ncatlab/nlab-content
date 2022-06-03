+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition ##

Let $F$ be an [[Archimedean field]] and let $I \subseteq F$ be an [[open interval]] in $F$. Let us define the subset $\Delta_{\#}(I) \subseteq I \times I$ of pairs of elements apart from the [[diagonal]] as 

$$\Delta_{\#}(I) \coloneqq \{(x,y):I \times I \vert 0 \lt \vert x - y \vert \}$$

Let $U$ be a set such that $\Delta_{\#}(I) \subseteq U$ and $U \subseteq I \times I$. As a result, for every element $x \in I$, there is an indexed set 

$U(x) \coloneqq \{y \in I \vert (x, y)\}$ 

Given a [[partial function|partial]] binary function $q:U \to F$, the currying of $q$ results in the indexed function

$$q(x): \{y \in U(x) \vert (x,y)\} \to F$$

for every element $x \in I$

A function $g:I \to F$ is a __limit of $q$ approaching the diagonal__ if for all $x \in S$ the limit of the dependent function $q(x)$ approaching $x$ is $g(x)$. We can define a predicate that the $q$ has a limit approaching the diagonal as

$$hasLimitApproachingDiagonal(q) \coloneqq \forall g \colon I \to F. \forall x \in I \lim_{y \to x} q(x)(y) = g(x)$$

The type of all functions in $U \to F$ that have a limit approaching the diagonal is defined as 

$$DiagLimFunc(I, F) \coloneqq \{q \in U \to F \vert hasLimitApproachingDiagonal(q)\}$$

As a result, there exists a function 

$$\lim_{(x, y) \to (x, x)} (-)(x, y): DiagLimFunc(I, F) \to (I \to F)$$ 

which returns the limit of a partial binary function $q:DiagLimFunc(I, F)$ approaching the diagonal and thus satisfies the equation

$$\lim_{y \to x} q(x)(y) = \lim_{(x, y) \to (x, x)} q(x, y)$$

for all $x \in I$

## Properties ##

In an [[Archimedean field]] $F$, the [[algebraic limit theorem]]s are satisfied:

+-- {: .num_prop} 
###### Proposition
**(Limits preserve the zero function)

The limit of a binary function approaching a diagonal preserves the zero function. 

=--

+-- {: .proof} 
###### Proof 

For all $x \in I$, the following is true:

$$\lim_{(x, y) \to (x, x)} 0(x, y) = \lim_{y \to x} 0(x)(y)$$

$$\lim_{(x, y) \to (x, x)} 0(x, y) = 0$$

$$\lim_{(x, y) \to (x, x)} 0(x, y) = 0(x, x)$$

Thus, the limit of a binary function approaching a diagonal preserves the zero function.

=--

+-- {: .num_prop} 
###### Proposition
**(Limits preserve addition of functions)

The limit of a binary function approaching a diagonal preserves addition of functions . 

=--


+-- {: .proof} 
###### Proof 

For all elements $c \in I$ and functions $f:I \to F$ and $g:I \to F$ such that 
$$\lim_{x \to c} f(x) = c \qquad \lim_{x \to c} g(x) = c$$
the following is true:

$$\lim_{(x, y) \to (x, x)} f(x, y) + g(x, y) = \lim_{(x, y) \to (x, x)} (f + g)(x, y)$$

$$\lim_{(x, y) \to (x, x)} f(x, y) + g(x, y) = \lim_{y \to x} (f + g)(x)(y)$$

$$\lim_{(x, y) \to (x, x)} f(x, y) + g(x, y) = \lim_{y \to x} f(x)(y) + g(x)(y)$$

$$\lim_{(x, y) \to (x, x)} f(x, y) + g(x, y) = \lim_{y \to x} f(x)(y) + \lim_{y \to x} g(x)(y)$$

$$\lim_{(x, y) \to (x, x)} f(x, y) + g(x, y) = \lim_{(x, y) \to (x, x)} f(x, y) + \lim_{(x, y) \to (x, x)} g(x, y)$$

Thus, the limit of a binary function approaching a diagonal preserves addition of functions . 

=--

+-- {: .num_prop} 
###### Proposition
**(Limits preserve negation of functions)

The limit of a binary function approaching a diagonal preserves negation of functions. 

=--

+-- {: .proof} 
###### Proof 

For all elements $c \in I$ and functions $f:I \to F$ such that 
$$\lim_{x \to c} f(x) = c$$
the following is true:

$$\lim_{(x, y) \to (x, x)} -f(x, y) = \lim_{y \to x} -f(x)(y)$$

$$\lim_{(x, y) \to (x, x)} -f(x, y) = -\lim_{y \to x} f(x)(y)$$

$$\lim_{(x, y) \to (x, x)} -f(x, y) = -\lim_{(x, y) \to (x, x)} f(x, y)$$

Thus, the limit of a binary function approaching a diagonal preserves negation of functions. 

=--


+-- {: .num_prop} 
###### Proposition
**(Limits preserve subtraction of functions)

The limit of a binary function approaching a diagonal preserves subtraction of functions . 

=--


+-- {: .proof} 
###### Proof 

For all elements $c \in I$ and functions $f:I \to F$ and $g:I \to F$ such that 
$$\lim_{x \to c} f(x) = c \qquad \lim_{x \to c} g(x) = c$$
the following is true:

$$\lim_{(x, y) \to (x, x)} f(x, y) - g(x, y) = \lim_{(x, y) \to (x, x)} (f - g)(x, y)$$

$$\lim_{(x, y) \to (x, x)} f(x, y) - g(x, y) = \lim_{y \to x} (f - g)(x)(y)$$

$$\lim_{(x, y) \to (x, x)} f(x, y) - g(x, y) = \lim_{y \to x} f(x)(y) - g(x)(y)$$

$$\lim_{(x, y) \to (x, x)} f(x, y) - g(x, y) = \lim_{y \to x} f(x)(y) - \lim_{y \to x} g(x)(y)$$

$$\lim_{(x, y) \to (x, x)} f(x, y) - g(x, y) = \lim_{(x, y) \to (x, x)} f(x, y) - \lim_{(x, y) \to (x, x)} g(x, y)$$

Thus, the limit of a binary function approaching a diagonal preserves addition of functions . 

=--

+-- {: .num_prop} 
###### Proposition
**(Limits preserve the left multiplicative $\mathbb{Z}$-action of functions)

The limit of a binary function approaching a diagonal preserves the left multiplicative $\mathbb{Z}$-action of functions. 

=--


+-- {: .proof} 
###### Proof 

For all elements $c \in I$ and functions $f:I \to F$ such that 
$$\lim_{x \to c} f(x) = c$$
and integers $n \in \mathbb{Z}$, the following is true:

$$\lim_{(x, y) \to (x, x)} n f(x, y) = \lim_{(x, y) \to (x, x)} (n f)(x, y)$$

$$\lim_{(x, y) \to (x, x)} n f(x, y) = \lim_{y \to x} (n f)(x)(y)$$

$$\lim_{(x, y) \to (x, x)} n f(x, y) = \lim_{y \to x} n f(x)(y)$$

$$\lim_{(x, y) \to (x, x)} n f(x, y) = n \lim_{y \to x} f(x)(y)$$

$$\lim_{(x, y) \to (x, x)} n f(x, y) = n \lim_{(x, y) \to (x, x)} f(x, y)$$

Thus, the limit of a binary function approaching a diagonal preserves the left multiplicative $\mathbb{Z}$-action of functions. 

=--

+-- {: .num_prop} 
###### Proposition
**(Limits preserve left multiplication by scalars)

The limit of a binary function approaching a diagonal preserves left multiplication by scalars. 

=--

+-- {: .proof} 
###### Proof 

For all elements $c \in I$ and functions $f:I \to F$ such that 
$$\lim_{x \to c} f(x) = c$$
and elements $a \in F$, the following is true:

$$\lim_{(x, y) \to (x, x)} a f(x, y) = \lim_{(x, y) \to (x, x)} (a f)(x, y)$$

$$\lim_{(x, y) \to (x, x)} a f(x, y) = \lim_{y \to x} (a f)(x)(y)$$

$$\lim_{(x, y) \to (x, x)} a f(x, y) = \lim_{y \to x} a f(x)(y)$$

$$\lim_{(x, y) \to (x, x)} a f(x, y) = a \lim_{y \to x} f(x)(y)$$

$$\lim_{(x, y) \to (x, x)} a f(x, y) = a \lim_{(x, y) \to (x, x)} f(x, y)$$

Thus, the limit of a binary function approaching a diagonal preserves left multiplication by scalars. 

=--

+-- {: .num_prop} 
###### Proposition
**(Limits preserve the constant one function)

The limit of a binary function approaching a diagonal preserves the constant one function. 

=--

+-- {: .proof} 
###### Proof 

For all $x \in I$, the following is true:

$$\lim_{(x, y) \to (x, x)} 1(x, y) = \lim_{y \to x} 1(x)(y)$$

$$\lim_{(x, y) \to (x, x)} 1(x, y) = 1$$

$$\lim_{(x, y) \to (x, x)} 1(x, y) = 1(x, x)$$

Thus, the limit of a binary function approaching a diagonal preserves the constant one function.

=--

+-- {: .num_prop} 
###### Proposition
**(Limits preserve multiplication of functions)

The limit of a binary function approaching a diagonal preserves multiplication of functions . 

=--


+-- {: .proof} 
###### Proof 

For all elements $c \in I$ and functions $f:I \to F$ and $g:I \to F$ such that 
$$\lim_{x \to c} f(x) = c \qquad \lim_{x \to c} g(x) = c$$
the following is true:

$$\lim_{(x, y) \to (x, x)} f(x, y) \cdot g(x, y) = \lim_{(x, y) \to (x, x)} (f \cdot g)(x, y)$$

$$\lim_{(x, y) \to (x, x)} f(x, y) \cdot g(x, y) = \lim_{y \to x} (f \cdot g)(x)(y)$$

$$\lim_{(x, y) \to (x, x)} f(x, y) \cdot g(x, y) = \lim_{y \to x} f(x)(y) \cdot g(x)(y)$$

$$\lim_{(x, y) \to (x, x)} f(x, y) \cdot g(x, y) = \lim_{y \to x} f(x)(y) \cdot \lim_{y \to x} g(x)(y)$$

$$\lim_{(x, y) \to (x, x)} f(x, y) \cdot g(x, y) = \lim_{(x, y) \to (x, x)} f(x, y) \cdot \lim_{(x, y) \to (x, x)} g(x, y)$$

Thus, the limit of a binary function approaching a diagonal preserves multiplication of functions . 

=--

+-- {: .num_prop} 
###### Proposition
**(Limits preserve the powers of functions)

The limit of a binary function approaching a diagonal preserves powers of functions. 

=--

+-- {: .proof} 
###### Proof 

For all elements $c \in I$ and functions $f:I \to F$ such that 
$$\lim_{x \to c} f(x) = c$$
and natural number $n \in \mathbb{N}$, the following is true:

$$\lim_{(x, y) \to (x, x)} f(x, y)^n = \lim_{(x, y) \to (x, x)} (f^n)(x, y)$$

$$\lim_{(x, y) \to (x, x)} f(x, y)^n = \lim_{y \to x} (f^n)(x)(y)$$

$$\lim_{(x, y) \to (x, x)} f(x, y)^n = \lim_{y \to x} (f(x)(y))^n$$

$$\lim_{(x, y) \to (x, x)} f(x, y)^n = \left(\lim_{y \to x} f(x)(y)\right)^n$$

$$\lim_{(x, y) \to (x, x)} f(x, y)^n = \left(\lim_{(x, y) \to (x, x)} f(x, y)\right)^n$$

Thus, the limit of a binary function approaching a diagonal preserves powers of functions. 

=--

### Limits preserve reciprocals of functions ###

+-- {: .num_prop} 
###### Proposition
**(Limits preserve reciprocals of functions)

The limit of a binary function approaching a diagonal preserves reciprocals of functions. 

=--

+-- {: .proof} 
###### Proof 

Let $x^{-1}$ be another notation for $\frac{1}{x}$. For all elements $c \in I$ and functions $f:I \to F$ such that 
$$\lim_{x \to c} f(x) = c \qquad \lim_{(x, y) \to (x, x)} f(x, y) \# 0$$
the following is true:

$$\lim_{(x, y) \to (x, x)} f(x, y)^{-1} = \lim_{(x, y) \to (x, x)} (f^{-1})(x, y)$$

$$\lim_{(x, y) \to (x, x)} f(x, y)^{-1} = \lim_{y \to x} (f^{-1})(x)(y)$$

$$\lim_{(x, y) \to (x, x)} f(x, y)^{-1} = \lim_{y \to x} (f(x)(y))^{-1}$$

$$\lim_{(x, y) \to (x, x)} f(x, y)^{-1} = \left(\lim_{y \to x} f(x)(y)\right)^{-1}$$

$$\lim_{(x, y) \to (x, x)} f(x, y)^{-1} = \left(\lim_{(x, y) \to (x, x)} f(x, y)\right)^{-1}$$

Thus, the limit of a binary function approaching a diagonal preserves reciprocals of functions. 

=--

+-- {: .num_prop} 
###### Proposition
**(Limits preserve that the reciprocals of functions are multiplicative inverses)

The limit of a binary function approaching a diagonal preserves that the reciprocals of functions are multiplicative inverses. 

=--

+-- {: .proof} 
###### Proof 

Let $x^{-1}$ be another notation for $\frac{1}{x}$. For all elements $c \in I$ and functions $f:I \to F$ such that 
$$\lim_{x \to c} f(x) = c \qquad \left| \lim_{(x, y) \to (x, x)} f(x, y) \right| \gt 0$$
the following is true:


Where $x^{-1}$ is another notation for $\frac{1}{x}$

$$\lim_{(x, y) \to (x, x)} f(x, y) \cdot {f(x, y)}^{-1} = \lim_{(x, y) \to (x, x)} (f \cdot f^{-1})(x, y)$$

$$\lim_{(x, y) \to (x, x)} f(x, y) \cdot {f(x, y)}^{-1} = \lim_{y \to x} (f \cdot f^{-1})(x)(y)$$

$$\lim_{(x, y) \to (x, x)} f(x, y) \cdot {f(x, y)}^{-1} = \lim_{y \to x} f(x)(y) \cdot {f(x)(y)}^{-1}$$

$$\lim_{(x, y) \to (x, x)} f(x, y) \cdot {f(x, y)}^{-1} = 1$$

Thus, limit of a binary function approaching a diagonal preserves that the reciprocals of functions are multiplicative inverses. 

=--

## See also ##

* [[limit of a function]]

* [[differentiable function]]

* [[difference quotient]]

* [[Newton-Leibniz operator]]