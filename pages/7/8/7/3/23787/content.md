+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition 

For a [[commutative ring]] $R$, the **sequence algebra** is the [[commutative algebra|commutative $R$-algebra]] $\mathbb{N} \to R$, with canonical injection $c:R \to (\mathbb{N} \to R)$ which sends each element $r$ in $R$ to a [[constant function]] $c(r)$. The commutative algebra operations are pointwise defined as:

$$c(r)(n) \coloneqq r$$
$$0(n) \coloneqq 0$$
$$(x + y)(n) \coloneqq x(n) + y(n)$$
$$(-x)(n) \coloneqq -x(n)$$
$$(r x)(n) \coloneqq r x(n)$$
$$(1)(n) \coloneqq 1$$
$$(x \cdot y)(n) \coloneqq x(n) \cdot y(n)$$

and thus the sequence set $\mathbb{N} \to R$ is a commutative $R$-algebra. 

## Polynomials 

Given a commutative ring $R$, a **sequential polynomial** is a [[sequence]] $x:\mathbb{N} \to R$ where there exists a natural number $N$ such that for all $i \gt N$, $x(i) = 0$. 

## Operators

### Left shift operator

Given a commutative ring $R$ and a sequence $x:\mathbb{N} \to R$ of terms in $R$, the **left shift operator** 
$$T:(\mathbb{N} \to R) \to (\mathbb{N} \to R)$$
is defined as 
$$T x(i) \coloneqq x(i + 1)$$
for $i \in \mathbb{N}$. 

### Series operator

Given a commutative ring $R$ and a sequence $x:\mathbb{N} \to R$ of terms in $R$, the **series operator** 
$$\Sigma:(\mathbb{N} \to R) \to (\mathbb{N} \to R)$$
is inductively defined as 
$$\Sigma x(0) \coloneqq x(0)$$
$$\Sigma x(i + 1) \coloneqq \Sigma x(i) + x(i + 1)$$
for $i \in \mathbb{N}$. 

For any such sequence $x:\mathbb{N} \to R$, $\Sigma x$ is called a **[[series]]**. 

### Inverse series operator

Given a commutative ring $R$ and a sequence $x:\mathbb{N} \to R$ of terms in $R$, the **inverse series operator** 
$$\Sigma^{-1}:(\mathbb{N} \to R) \to (\mathbb{N} \to R)$$
is inductively defined as 
$$\Sigma^{-1} x(0) \coloneqq x(0)$$
$$\Sigma^{-1} x(i + 1) \coloneqq \Sigma^{-1} x(i) - x(i + 1)$$
for $i \in \mathbb{N}$. 

For any such sequence $x:\mathbb{N} \to R$, $\Sigma^{-1}\Sigma x = x$ and  $\Sigma\Sigma^{-1}x = x$. 

### Infinite product operator

Given a commutative ring $R$ and a sequence $x:\mathbb{N} \to R$ of terms in $R$, the **infinite product operator** 
$$\Pi:(\mathbb{N} \to R) \to (\mathbb{N} \to R)$$
is inductively defined as 
$$\Pi x(0) \coloneqq x(0)$$
$$\Pi x(i + 1) \coloneqq \Pi x(i) \cdot x(i + 1)$$
for $i \in \mathbb{N}$. 

For any such sequence $x:\mathbb{N} \to R$, $\Pi x$ is called an **[[infinite product]]**. 

### Discrete convolution

Given a commutative ring $R$ and sequence $x:\mathbb{N} \to R$ and $y:\mathbb{N} \to R$, the **discrete convolution** 
$$(-)*(-):(\mathbb{N} \to R) \times (\mathbb{N} \to R) \to (\mathbb{N} \to R)$$
is defined as 
$$(x*y)(i) \coloneqq \sum_{n:[0,i]} x(i) y(i - n)$$
for $i \in \mathbb{N}$. 

Given a commutative ring $R$ and sequence $x:\mathbb{N} \to R$ and $y:\mathbb{N} \to R$, the **Cauchy product** of the two series $\Sigma x \cdot \Sigma x$ is the discrete convolution of $x$ and $y$. 

$$\Sigma x \cdot \Sigma y \coloneqq x * y$$

### Sequential derivative

Given a commutative ring $R$ and a sequence $x:\mathbb{N} \to R$ of terms in $R$, the **sequential derivative** 
$$\mathcal{D}:(\mathbb{N} \to R) \to (\mathbb{N} \to R)$$
is defined as 
$$\mathcal{D} x(i) \coloneqq (i + 1) x(i + 1)$$
for $i \in \mathbb{N}$. 

The sequential derivative is a [[derivation]], where linearity is satisfied by addition and scalar multiplication of sequences and the [[Leibniz rule]] is satisfied for the Cauchy product of sequences. As a result, every sequence algebra is a [[differential algebra]]. 

### Right shift operators

Given a commutative ring $R$ and a sequence $x:\mathbb{N} \to R$, the set of right shifted sequences of $x$ is the [[fiber]] of the left shift operator at $x$:

$$\{y:\mathbb{N} \to R \vert T y = x\}$$

A right shift operator is an element of the above set. 

Every sequence in $R$ has a right shift operator $T^{-1}_s:(\mathbb{N} \to R) \to (\mathbb{N} \to R)$ for every term $r \in R$, 
defined as
$$T^{-1}_r x(0) = r$$
$$T^{-1}_r x(i + i) \coloneqq x(i)$$
for $i \in \mathbb{N}$. 

### Sequential antiderivatives

Given a commutative ring $R$ and a sequence $x:\mathbb{N} \to R$, the set of sequential antiderivatives of $x$ is the [[fiber]] of the sequential derivative at $x$:

$$\{y:\mathbb{N} \to R \vert \mathcal{D} y = x\}$$

A __sequential antiderivative__ is a element of the above set. 

If $R$ is a commutative $\mathbb{Q}$-algebra, then every sequence in $R$ has an antiderivative operator $\mathcal{D}^{-1}_r:(\mathbb{N} \to R) \to (\mathbb{N} \to R)$ for every term $r \in R$, 
defined as
$$\mathcal{D}^{-1}_r x(0) = r$$
$$\mathcal{D}^{-1}_r x(i + i) \coloneqq \frac{1}{i} x(i)$$
for $i \in \mathbb{N}$.  

## Sequence functions

Given a commutative ring $R$, a **sequence function** is a function $f:R \to (\mathbb{N} \to R)$. 

### Functional shift operator

Given a commutative ring $R$ and a sequence function $f:R \to (\mathbb{N} \to R)$, the **functional shift operator** 
$$\mathcal{T}:R \to (R \to (\mathbb{N} \to R)) \to (R \to (\mathbb{N} \to R))$$
is defined as 
$$\mathcal{T}_c f(r)(i) \coloneqq f(r - c)(i)$$
for $c \in R$, and $r \in R$, and $i \in \mathbb{N}$. 

### Power sequence functions

Given a commutative ring $R$ and a sequence $x:\mathbb{N} \to R$ of terms in $R$, the **power sequence function** 
$$\mathcal{P}:(\mathbb{N} \to R) \to (R \to (\mathbb{N} \to R))$$
is defined as 
$$\mathcal{P}_x (r)(i) \coloneqq x(i) r^i$$
for $i \in \mathbb{N}$ and $r \in R$. 

### Functional derivative

Given a commutative ring $R$, the **functional derivative** of the power sequence function $f:R \to (\mathbb{N} \to R)$
$$\tilde{D}:(R \to (\mathbb{N} \to R)) \to (R \to (\mathbb{N} \to R))$$
is defined as
$$(\tilde{D} \mathcal{P}_x)(r)(i) \coloneqq (\mathcal{D} x(i)) r^i $$

### Power series

For any such sequence $x:\mathbb{N} \to R$, $\Sigma\mathcal{P}_x(r)$ is called a **formal [[power series]]** or **formal [[Maclaurin series]]**. For any such sequence $x:\mathbb{N} \to R$ and element $c \in R$, $\Sigma \mathcal{T}_c \mathcal{P}_x (r)$ is called a **formal [[Taylor series]]**. 

### Analytic functions

Suppose $R$ is a commutative ring with a [[partial function]]
$$\lim_{n \to \infty} (-)(n): (\mathbb{N} \to R) \to R$$
making $R$ into a [[sequentially Hausdorff space]]. 

Then, a [[partial function]] $f:R \to R$ is an **analytic function** if there exists an element $c \in R$ and sequence $x:\mathbb{N} \to R$ such that 

$$f(r) = \lim_{n \to \infty} \Sigma \mathcal{T}_c \mathcal{P}_x (r)(n)$$

for all elements $r \in \dom f$.

## See also 

* [[sequence]]

* [[sequence space]]

* [[function algebra]]

* [[differential algebra]]

* [[sequentially Hausdorff space]]

* [[analytic function]]