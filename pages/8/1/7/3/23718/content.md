[[!redirects algebraic limit fields]]
[[!redirects algebraic limit theorem]]
[[!redirects algebraic limit theorems]]

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

## Idea ##

A field with a notion of a limit of a function that satisfy the algebraic limit theorems. 

## Definition ##

Let $F$ be a [[Heyting field]] and a [[function limit space]], where $x^{-1}$ is another notation for the [[reciprocal function]] $\frac{1}{x}$. $F$ is a __algebraic limit field__ if the __algebraic limit theorems__ are satisfied, i.e. if the limit preserves the field operations:

* for all elements $c \in S$, 
$$\lim_{x \to c} 0(x) = 0$$

* for all elements $c \in S$ and functions $f:S \to C$ and $g:S \to C$ such that 
$$\lim_{x \to c} f(x) = c \qquad \lim_{x \to c} g(x) = c$$
$$\lim_{x \to c} f(x) + g(x) = \lim_{x \to c} f(x) + \lim_{x \to c} g(x)$$

* for all elements $c \in S$ and functions $f:S \to C$ such that 
$$\lim_{x \to c} f(x) = c$$
$$\lim_{x \to c} -f(x) = -\lim_{x \to c} f(x)$$

* for all elements $c \in S$ and functions $f:S \to C$ and $g:S \to C$ such that
$$\lim_{x \to c} f(x) = c \qquad \lim_{x \to c} g(x) = c$$
$$\lim_{x \to c} f(x) - g(x) = \lim_{x \to c} f(x) - \lim_{x \to c} g(x)$$

* for all elements $c \in S$, integers $a \in \mathbb{Z}$, and functions $f:S \to C$, such that 
$$\lim_{x \to c} f(x) = c$$
$$\lim_{x \to c} a f(x) = a \lim_{x \to c} f(x)$$

* for all elements $c \in S$ and $a \in S$, and functions $f:S \to C$, such that 
$$\lim_{x \to c} f(x) = c$$
$$\lim_{x \to c} a f(x) = a \lim_{x \to c} f(x)$$

* for all elements $c \in S$, 
$$\lim_{x \to c} 1(x) = 1$$

* for all elements $c \in S$ and functions $f:S \to C$ and $g:S \to C$ such that 
$$\lim_{x \to c} f(x) = c \qquad \lim_{x \to c} g(x) = c$$
$$\lim_{x \to c} f(x) \cdot g(x) = \lim_{x \to c} f(x) \cdot \lim_{x \to c} g(x)$$

* for all elements $c \in S$, natural numbers $n \in \mathbb{N}$, and functions $f:S \to C$, such that 
$$\lim_{x \to c} f(x) = c$$
$$\lim_{x \to c} {f(x)}^n = {\left(\lim_{x \to c} f(x)\right)}^n$$

* for all elements $c \in S$, and functions $f:S \to C$, such that 
$$\lim_{x \to c} f(x) = c$$
if 
$$\lim_{x \to c} f(x) \# 0$$
then 
$$\lim_{x \to c} {f(x)}^{-1} = {\left(\lim_{x \to c} f(x)\right)}^{-1}$$

* for all elements $c \in S$, and functions $f:S \to C$, such that 
$$\lim_{x \to c} f(x) = c$$
if 
$$\lim_{x \to c} f(x) \# 0$$
then 
$$\lim_{x \to c} f(x) \cdot {f(x)}^{-1} = 1$$

## See also ##

* [[function limit space]]
* [[difference quotient]]
* [[algebraic limit vector space]]
* [[Newton-Leibniz operator]]
* [[differentiable space]]