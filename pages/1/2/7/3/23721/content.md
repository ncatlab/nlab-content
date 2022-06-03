[[!redirects D operator]]
[[!redirects derivative]]

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

Given an [[Archimedean field]] $F$, an [[open interval]] $I \subseteq F$, a [[pointwise continuous function]] $f:C^0(I, F)$ is __differentiable__ if the [[difference quotient]] has a [[limit of a binary function approaching a diagonal|limit approaching the diagonal]]

$$isDifferentiable(f) := hasLimitApproachingDiagonal\left(\frac{f(x) - f(y)}{x - y}\right)$$

Let us define the type of differentiable functions $D^1(I, F)$ on $I$ as the type of pointwise continuous functions that are differentiable.  
$$D^1(I, F) := \{f \in C^0(I, F) \vert isDifferentiable(f)\}$$

The __Newton–Leibniz operator__ or __D operator__ $\tilde{D}: D^1(I, F) \to (I \to F)$ is a function from the type of [[differentiable function]]s $D^1(I, F)$ to the type of functions $I \to F$, and is pointwise defined as 
$$\tilde{D}(f) \coloneqq \lim_{(x, y) \to (x, x)} \frac{f(x) - f(y)}{x - y}$$ 
for a [[differentiable function]] $f:D^1(I, F)$. For any differentiable function $f:D^1(I, F)$, the function $\tilde{D}(f)$ is called the __derivative__ of $f$. 

## Properties ##

These all follow from the [[algebraic limit theorem]]s of the [[limit of a binary function approaching a diagonal]].

### Constant function rule ###

Let $c:I \to F$ be a constant function. With constant functions the function $c:I \to F$ and the value of the function $c:F$ are usually written with the same symbol. For all constant functions $c:I \to F$, 

$$\tilde{D}(c) = \lim_{(x, y) \to (x, x)} \frac{c - c}{x - y}$$ 

$$\tilde{D}(c) = \lim_{(x, y) \to (x, x)} \frac{0}{x - y}$$ 

$$\tilde{D}(c) = \lim_{(x, y) \to (x, x)} 0$$ 

$$\tilde{D}(c) = 0$$ 

### Identity function rule ###

Where $\frac{x}{x}$ is another notation for $x \cdot x^{-1}$

$$\tilde{D}(id_F) = \lim_{(x, y) \to (x, x)} \frac{x - y}{x - y}$$ 

$$\tilde{D}(id_F) = 1$$ 

### Linearity ###

For all elements $a \in F$ and $b \in F$ and functions $f:I \to F$ and $g:I \to F$, 

$$\tilde{D}(a \cdot f + b \cdot g) = \lim_{(x, y) \to (x, x)} \frac{(a \cdot f(x) + b \cdot g(x)) - (a \cdot f(y) + b \cdot g(y)}{x - y}$$ 

$$\tilde{D}(a \cdot f + b \cdot g) = \lim_{(x, y) \to (x, x)} \frac{(a \cdot f(x) - a \cdot f(y)) + (b \cdot g(x) - b \cdot g(y)}{x - y}$$ 

$$\tilde{D}(a \cdot f + b \cdot g) = \lim_{(x, y) \to (x, x)} \frac{(a \cdot (f(x) - f(y)) + (b \cdot (g(x) - g(y))}{x - y}$$ 

$$\tilde{D}(a \cdot f + b \cdot g) = \lim_{(x, y) \to (x, x)} \frac{a \cdot (f(x) - f(y)}{x - y} + \frac{b \cdot (g(x) - g(y)}{x - y}$$ 

$$\tilde{D}(a \cdot f + b \cdot g) = a \cdot \lim_{(x, y) \to (x, x)} \frac{(f(x) - f(y)}{x - y} + b \cdot \lim_{(x, y) \to (x, x)} \frac{(g(x) - g(y)}{x - y}$$ 

$$\tilde{D}(a \cdot f + b \cdot g) = a \cdot \tilde{D}(f) + b \cdot \tilde{D}(g)$$ 

### Leibniz rule ###

For all functions $f:I \to F$ and $g:I \to F$, 

$$\tilde{D}(f \cdot g) = \lim_{(x, y) \to (x, x)} \frac{(f(x) \cdot g(x)) - (f(y) \cdot g(y)}{x - y}$$ 

$$\tilde{D}(f \cdot g) = \lim_{(x, y) \to (x, x)} \frac{(f(x) \cdot g(x)) - (f(x) \cdot g(y)) + (f(x) \cdot g(y)) - (f(y) \cdot g(y)}{x - y}$$ 

$$\tilde{D}(f \cdot g) = \lim_{(x, y) \to (x, x)} \frac{(f(x) \cdot (g(x) - g(y)) + ((f(x) - f(y)) \cdot g(y))}{x - y}$$ 

$$\tilde{D}(f \cdot g) = \lim_{(x, y) \to (x, x)} \frac{f(x) \cdot (g(x) - g(y)}{x - y} + \frac{(f(x) - f(y)) \cdot g(y)}{x - y}$$ 

$$\tilde{D}(f \cdot g) = f \cdot \left(\lim_{(x, y) \to (x, x)} \frac{g(x) - g(y)}{x - y}\right) + \left(\lim_{(x, y) \to (x, x)} \frac{f(x) - f(y)}{x - y}\right) \cdot g$$ 

$$\tilde{D}(f \cdot g) = f \cdot \tilde{D}(g) + \tilde{D}(f) \cdot g$$ 

### Power rule ###

For all functions $f:I \to F$ and natural numbers $n \in \mathbf{N}$,

$$\tilde{D}(f^n) = \lim_{(x, y) \to (x, x)} \frac{f(x)^n - f(y)^n}{x - y}$$ 

We proceed by induction on the natural numbers. The base case $n = 0$: For all functions $f:I \to F$,

$$\tilde{D}(f^0) = \lim_{(x, y) \to (x, x)} \frac{f(x)^0 - f(y)^0}{x - y}$$ 

$$\tilde{D}(f^0) = \lim_{(x, y) \to (x, x)} \frac{1 - 1}{x - y}$$ 

$$\tilde{D}(f^0) = \tilde{D}(1)$$ 

Then the inductive case: For all functions $f:I \to F$ and natural numbers $n \in \mathbf{N}$,

$$\tilde{D}(f^{n+1}) = \lim_{(x, y) \to (x, x)} \frac{f(x)^{n+1} - f(y)^{n+1}}{x - y}$$ 

$$\tilde{D}(f^{n+1}) = \lim_{(x, y) \to (x, x)} \frac{f(x) \cdot f(x)^{n} - f(y) \cdot f(y)^{n}}{x - y}$$ 

$$\tilde{D}(f^{n+1}) = \tilde{D}(f) \cdot f^n + \tilde{D}(f^n) \cdot f$$ 

$$\tilde{D}(f^{n+1}) = \sum_{n=0}^{n} \tilde{D}(f) \cdot f^n$$ 

### Reciprocal rule ###

## See also ##

* [[differentiable function]]

* [[iterated differentiable function]]

* [[smooth function]]

* [[antiderivative]]