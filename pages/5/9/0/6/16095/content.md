
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

### For scalar-valued functions

The **inverse function theorem** says that given any [[sequentially Cauchy complete]] [[Archimedean field]] $\mathbb{R}$ and a [[continuously differentiable function]] $f:I \to \mathbb{R}$ from an [[open interval]] $I \subseteq \mathbb{R}$ such that for all points $a \in I$,
$$\left| \frac{d f}{d x}(a) \right| \gt 0$$
the [[inverse function]] $f^{-1}:\mathrm{im}(f) \to \mathbb{R}$ exists and is unique and is defined by the first-order nonlinear [[ordinary differential equation]]

$$\left(\frac{d f}{d x} \circ f^{-1}\right) \frac{d f^{-1}}{d x} = 1$$

with initial condition $f^{-1}(f(a)) = a$. Classically, $\mathbb{R}$ is essentially unique, but constructively, there are multiple inequivalent [[sequentially Cauchy complete]] [[Archimedean fields]]. 

### For vector-valued functions

To be done...

## Proof 

This proof is adapted from the Wikipedia article on the inverse function theorem, in the section "A proof using the contraction mapping principle", the contraction mapping principle being another name for the [[Banach fixed-point theorem]]. 

\begin{lemma}
Let $(-r, r)$ denote an [[open interval]] in $\mathbb{R}$ with radius $r$ and centre $0$. If $g:(-r, r) \to \mathbb{R}$ is a map such that $g(0) = 0$ and there exists a rational constant $0 \lt c \lt 1$ such that $\vert g(y) - g(x) \vert = c \vert y - x \vert$ for all $x \in (-r, r)$ and $y \in (-r, r)$, then $f = \mathrm{id}_\mathbb{R} + g$ is injective on $(-r, r)$ and 
$$(-(1 - c)r, (1 - c)r) \subset f((-r, r)) \subset (-(1 + c)r, (1 + c)r)$$
where $\mathrm{id}_\mathbb{R}$ is the identity map on the real numbers, restricted in the domain to $(-r, r)$, and given an open interval $I \subseteq \mathbb{R}$, $f(I)$ is the [[image]] of $f$ under $I$.
\end{lemma}

\begin{proof}
First, the map $f$ is injective on $(-r, r)$, since if $f(x) = f(y)$, then $g(y) - g(x) = x - y$ and so $\vert g(y) - g(x) \vert = \vert y - x \vert$,
which is a contradiction unless $y = x$. Next we show 
$$(-(1 - c)r, (1 - c)r) \subset f((-r, r))$$ 
The idea is to note that this is equivalent to, given a point $y$ in $(-(1-c) r, (1-c) r)$, find a fixed point of the map
$$F : [-r, r] \to [-r', r']$$
defined as $F(x) = y - g(x)$ where $0 \lt r' \lt r$ such that $\vert y \vert \leq (1-c)r'$ and the bar means a closed ball. To find a fixed point, we use the [[Banach fixed-point theorem]] and checking that $F$ is a well-defined strict-contraction mapping is straightforward. Finally, we have: 
$$f((-r, r)) \subset (-(1 + c)r, (1 + c)r)$$ 
since
$$\vert f(x) \vert = \vert x + g(x) - g(0) \vert \le (1+c) \vert x \vert$$
\end{proof}

Now that we have established the lemma, we could proved the main theorem:

\begin{proof}
It is enough to prove the special case when $a = 0, b = f(a) = 0$ and $f'(0) = \mathrm{id}_\mathbb{R}$. Let $g = f - \mathrm{id}_\mathbb{R}$. The [[mean value theorem]] applied to $t \mapsto g(x + t(y - x))$ says:
$$\vert g(y) - g(x) \vert \leq \vert y - x \vert \sup_{0 \lt t \lt 1} \vert g'(x + t(y - x)) \vert$$
Since $g'(0) = \mathrm{id}_\mathbb{R} - \mathrm{id}_\mathbb{R} = 0$ and $g'$ is continuous, we can find an $r \gt 0$ such that
$$\vert g(y) - g(x)\vert \leq 2^{-1} \vert y - x \vert$$
for all $x, y$ in $(-r, r)$. Then the earlier lemma says that $f = g + \mathrm{id}_\mathbb{R}$ is injective on $(-r, r)$ and $(-r/2, r/2) \subset (-r, r)$. Then
$$f : (-r, r) \cap f^{-1}((-r/2, r/2)) \to (-r/2, r/2)$$
is bijective and thus has the inverse, where given an open interval $I \subseteq \mathbb{R}$, $f^{-1}(I)$ is the [[inverse image]] of $f$ over $I$.

to be continued... 
\end{proof}

## In constructive mathematics

The given proof of the inverse function theorem above relies on the [[mean value theorem]], which in [[constructive mathematics]] is only true for [[uniformly differentiable functions]]. There might be other proofs which might not rely on the [[mean value theorem]] and could prove the inverse function theorem for continuously differentiable functions. 

## As an axiom for Archimedean ordered fields

While [[continuously differentiable functions]] and [[locally uniformly differentiable functions]] are well-defined in every [[Archimedean ordered field]], the inverse function theorem does not hold in all Archimedean ordered fields. One could instead consider adding the inverse function theorem as an axiom to an arbitrary Archimedean ordered field $R$. There are a few axioms which could be used here 

* For any Archimedean ordered field $R$, the **continuously differentiable inverse function axiom** for $R$ states that given any differentiable function $f:I \to R$ on an open subinterval $I \subseteq R$ such that its derivative $\frac{d f}{d x}:I \to R$ is pointwise continuous and always apart from zero, there is a unique differentiable function $f^{-1}:\mathrm{im}(f) \to R$ called the **inverse function** with pointwise continuous derivative $\frac{d f^{-1}}{d x}:\mathrm{im}(f) \to R$ such that $f^{-1}(f(a)) = a$ and for all elements $a \in \mathrm{im}(f)$ and
$$\frac{d f}{d x}\left(f^{-1}(a)\right) \cdot \frac{d f^{-1}}{d x}\left(a\right) = 1$$

* For any Archimedean ordered field $R$, the **locally uniformly differentiable inverse function axiom** for $R$ states that given any differentiable function $f:I \to R$ on an open subinterval $I \subseteq R$ such that its derivative $\frac{d f}{d x}:I \to R$ is locally uniformly continuous and always apart from zero, there is a unique differentiable function $f^{-1}:\mathrm{im}(f) \to R$ called the **inverse function** with locally uniformly continuous derivative $\frac{d f^{-1}}{d x}:\mathrm{im}(f) \to R$ such that $f^{-1}(f(a)) = a$ and for all elements $a \in \mathrm{im}(f)$ and
$$\frac{d f}{d x}\left(f^{-1}(a)\right) \cdot \frac{d f^{-1}}{d x}\left(a\right) = 1$$

The former is stronger than the latter, although they are equivalent in the presence of [[excluded middle]]. If $R$ satisfies the locally uniformly continuous inverse function axiom, then $R$ is a [[real closed field]]. 

There is also a third possible axiom, where differentiablility is defined using [[nilpotent]] [[infinitesimals]], and is valid for all subsets of $R$, rather than the open subintervals of $R$: Given subset $I \subseteq R$, a function $f:I \to R$ is **synthetically differentiable** if it has a function $\frac{d f}{d x}:I \to R$ such that for all [[Archimedean ordered Artinian local ring|Archimedean ordered Artinian local $R$-algebras]] $A$ with ring homomorphism $h:R \to A$ such that for all $\epsilon \in I$, $\epsilon^2 = 0$, for all nilpotent elements $\epsilon \in I$,
$$f_A(h(a) + \epsilon) = h(f(a)) + h\left(\frac{d f}{d x}(a)\right) \epsilon$$ 

* For any Archimedean ordered field $R$, the **synthetically differentiable inverse function axiom** for $R$ states that given any synthetically differentiable function $f:I \to R$ such that its derivative $\frac{d f}{d x}:I \to R$ is always apart from zero, there is a unique differentiable function $f^{-1}:\mathrm{im}(f) \to R$ called the **inverse function** with derivative $\frac{d f^{-1}}{d x}:\mathrm{im}(f) \to R$ such that $f^{-1}(f(a)) = a$ and for all elements $a \in \mathrm{im}(f)$ and
$$\frac{d f}{d x}\left(f^{-1}(a)\right) \cdot \frac{d f^{-1}}{d x}\left(a\right) = 1$$

## Related concepts

* [[mean value theorem]]

* [[Banach fixed-point theorem]]

* [[Picard–Lindelöf theorem]]

* [[regular value]]

* [[Mather's stability theorem]]

* [[real quadratic function]]

* [[real square root]]

## References

* [[Terence Tao]], *Analysis II. Texts and Readings in Mathematics.* (1st ed. 2016 edition). New Delhi: Hindustan Book Agency. ISBN:978-9380250656

See also:

* Wikipedia, _[Inverse function theorem](https://en.wikipedia.org/wiki/Inverse_function_theorem)_


[[!redirects inverse function axiom]]
[[!redirects inverse function principle]]