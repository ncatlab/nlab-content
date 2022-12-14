
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Formal geometry
+--{: .hide}
[[!include formal geometry -- contents]]
=--
=--
=--

\tableofcontents

## Idea

Since every [[ordered Artinian local ring]] $R$ has [[characteristic zero]], the positive integers $\mathbb{Z}_+$ are a subset of $R$, with [[injection]] $i:\mathbb{Z}_+ \hookrightarrow R$. An **Archimedean ordered Artinian local ring** is an [[ordered Artinian local ring]] which satisfies the [[archimedean property]]: for all elements $a \in R$ and $b \in R$, if $0 \lt a$ and $0 \lt b$, then there exists a positive integer $n \in \mathbb{Z}_+$ such that such that $a \lt i(n) \cdot b$. 

Archimedean ordered Artinian local rings are important because they are the [[ordered local rings]] with [[nilpotent]] [[infinitesimals]] but no [[infinite elements]] or invertible infinitesimals, and thus play an important role in synthetic approaches to [[analysis]] and [[differential geometry]]. 

[[Archimedean ordered fields]] are the Archimedean ordered Artinian local rings in which the [[nilradical]] is the [[trivial|trivial ideal]], or equivalently, in which every non-invertible element is equal to zero. 

## Properties

### Purely real and purely infinitesimal elements

Suppose that $K$ is an [[Archimedean ordered field]] and $A$ is an Archimedean ordered local $K$-algebra. Since $A$ is a [[local ring]], the quotient of $A$ by its ideal of non-invertible elements $I$ is the [[residue field]] $K$ itself, and the canonical function used in defining the quotient is the function $\Re:A \to K$ which takes a number $a \in A$ to its purely real component $\Re(a) \in K$. Since $A$ is an ordered $K$-algebra, there is a [[strictly monotone]] [[ring homomorphism]] $h:K \to A$. An element $a \in A$ is **purely real** if $h(\Re(a)) = a$, and an element $a \in A$ is **purely [[infinitesimal]]** if it is in the [[fiber]] of $\Re$ at $0 \in K$. Zero is the only element in $A$ which is both purely real and purely infinitesimal. 

### Prelattice, pseudometric, and seminorm structure

Now, suppose that the [[Archimedean ordered field]] $K$ has [[lattice]] structure $\min:K \times K \to K$ and $\max:K \times K \to K$. Then the Archimedean ordered local $K$-algebra $A$ has a [[prelattice]] structure given by functions $\min':A \times A \to A$ and $\max':A \times A \to A$, defined by 
$$\min'(a, b) \coloneqq h(\min(\Re(a), \Re(b)))$$
and 
$$\max'(a, b) \coloneqq h(\max(\Re(a), \Re(b)))$$

The [[distance]] function on $A$ is given by the function $\rho:A \times A \to K$, defined as 

$$\rho(a, b) \coloneqq \max(\Re(a), \Re(b)) - \min(\Re(a), \Re(b))$$

and the [[absolute value]] on $A$ is given by the function $\vert-\vert:A \times A \to K$, defined as 

$$\vert a \vert \coloneqq \rho(a, 0)$$

The distance function and absolute value are [[pseudometrics]] and multiplicative [[seminorms]], because every [[Archimedean ordered field]] $K$ embeds into the [[real numbers]] $\mathbb{R}$, and since $\min(a, b) \leq \max(a, b)$, the pseudometric and seminorm are always non-negative. This also implies that in every Archimedean ordered field with lattice structure, the pseudometric defined above is a metric. 

### Smooth and differentiable function structure

Suppose that $K$ is an [[Archimedean ordered field]] with lattice structure, and $A$ is an [[Archimedean ordered local ring|Archimedean ordered]] [[Artinian local algebra|Artinian local $K$-algebra]]. Then [[continuous functions]], [[differentiable functions]], and [[smooth functions]] are each definable on $K$ using the algebraic, order, and metric structure on $K$. 

The ring homomorphism $h:K \to A$ preserves [[smooth functions]]: given a natural number $n \in \mathbb{N}$ and a purely infinitesimal element $\epsilon \in I$ such that $\epsilon^{n + 1} = 0$, then for every [[smooth function]] $f \in C^\omega(K)$, there is a function $f_A:A \to A$ such that for all elements $x \in K$, $f_A(h(x)) = h(f(x))$ and 
$$f_A(h(x) + \epsilon) = \sum_{i = 0}^{n} \frac{1}{i!} h\left(\frac{d^i f}{d x^i}(x)\right) \epsilon^i$$ 

If we restrict to Archimedean ordered Artinian local $K$-algebras $A$ where every element of the nilradical $I$ is a nilsquare element, where for all $\epsilon \in I$, $\epsilon^2 = 0$, then the ring homomorphism $h:K \to A$ preserves [[differentiable functions]]; for every [[differentiable function]] $f:K \to K$ with given [[derivative]] $f':K \to K$, there is a function $f_A:A \to A$ such that for all elements $x \in K$ and nilpotent elements $\epsilon \in I$, $f_A(h(x)) = h(f(x))$ and 
$$f_A(h(x) + \epsilon) = h(f(x)) + h(f'(x)) \epsilon$$ 

In particular, every [[polynomial function]] $p:K \to K$ lifts to a polynomial function $p_A:A \to A$. 

Alternatively, one could use this property to define differentiable and smooth functions in $K$, such as the [[exponential function]], [[natural logarithm]], [[sine function]], and [[cosine function]]. 

One could also work with [[partial functions]] instead. Given a predicate $P$ on the real numbers $\mathbb{R}$, let $I$ denote the set of all elements in $\mathbb{R}$ for which $P$ holds. A [[partial function]] $f:\mathbb{R} \to \mathbb{R}$ is equivalently a function $f:I \to \mathbb{R}$ for any such predicate $P$ and set $I$. 

A function $f:I \to \mathbb{R}$ is **smooth at a subset** $S \subseteq I$ with injection $j:S \hookrightarrow \mathbb{R}$ if it has a function $\frac{d^{-} f}{d x^{-}}:\mathbb{N} \times S \to \mathbb{R}$ with $(D^0 j)(a) = a$ for all $a \in S$, such that for all Archimedean ordered Artinian local $\mathbb{R}$-algebras $A$ with ring homomorphism $h_A:\mathbb{R} \to A$, natural numbers $n \in \mathbb{N}$, and purely infinitesimal elements $\epsilon \in I$ such that $\epsilon^{n + 1} = 0$
$$f_A(h_A(j(a)) + \epsilon) = \sum_{i = 0}^{n} \frac{1}{i!} h_A\left(\frac{d^i f}{d x^i}\left(a\right)\right) \epsilon^i$$ 

A function $f:I \to \mathbb{R}$ is **smooth at an element** $a \in I$ if it is smooth at the [[singleton subset]] $\{a\}$, and a function $f:I \to \mathbb{R}$ is **smooth** if it is smooth at the [[improper subset]] of $I$. 

A function $f:I \to \mathbb{R}$ is **differentiable at a subset** $S \subseteq I$ with injection $j:S \hookrightarrow \mathbb{R}$ if it has a function $\frac{d f}{d x}:S \to \mathbb{R}$ such that for all Archimedean ordered Artinian local $K$-algebras $A$ with ring homomorphism $h:K \to A$ such that for all $\epsilon \in I$, $\epsilon^2 = 0$, for all nilpotent elements $\epsilon \in I$,
$$f_A(h(j(a)) + \epsilon) = h(j(a)) + h\left(\frac{d f}{d x}(a)\right) \epsilon$$ 

A function $f:I \to \mathbb{R}$ is **differentiable at an element** $a \in I$ if it is differentiable at the [[singleton subset]] $\{a\}$, and a function $f:I \to \mathbb{R}$ is **differentiable** if it is differentiable at the [[improper subset]] of $I$. 

### Square roots and Euclidean pseudometric structure

Now, assume that $K$ is an [[Euclidean field]] as well, in addition to being an [[Archimedean ordered field]]. While $K$ has a [[principal square root function]] $\sqrt{-}:[0, \infty) \to [0, \infty)$, not every Archimedean ordered local $K$-algebra $A$ has a principal square root function $\sqrt{-}:[0, \infty) \to [0, \infty)$, because purely infinitesimal elements in $A$ are not guaranteed to have [[square roots]]. An Archimedean ordered Artinian local $K$-algebra is **Euclidean** if every nilpotent element has a square root. 

However, given an Archimedean ordered Artinian local $K$-algebra $A$, every [[rank]] $n$ $A$-module $V$ with basis $v:\mathrm{Fin}(n) \to V$ has a [[Euclidean pseudometric]] $\rho_V:V \times V \to K$, given by 

$$\rho_V(a, b) \coloneqq \sqrt{\sum_{i \in \mathrm{Fin}(n)} \rho(a_i, b_i)^2}$$
for module elements $a \in V$ and $b \in V$ and scalars $a_i \in A$ and $b_i \in A$ for index $i \in \mathrm{Fin}(n)$, where
$$a = \sum_{i \in \mathrm{Fin}(n)} a_i v_i \quad b = \sum_{i \in \mathrm{Fin}(n)} b_i v_i$$

If $A$ is an [[ordered field]], then the Euclidean pseudometric on $V$ is a [[metric]].  

## See also

* [[Archimedean ordered field]]
* [[Archimedean ordered local ring]]
* [[ordered Artinian local ring]]

[[!redirects Archimedean ordered Artinian local ring]]
[[!redirects Archimedean ordered Artinian local rings]]

[[!redirects Archimedean ordered local Artinian ring]]
[[!redirects Archimedean ordered local Artinian rings]]

[[!redirects Archimedean ordered Artinian local algebra]]
[[!redirects Archimedean ordered Artinian local algebras]]

[[!redirects Archimedean ordered local Artinian algebra]]
[[!redirects Archimedean ordered local Artinian algebras]]

[[!redirects Archimedean ordered Artin local ring]]
[[!redirects Archimedean ordered Artin local rings]]

[[!redirects Archimedean ordered local Artin ring]]
[[!redirects Archimedean ordered local Artin rings]]

[[!redirects Archimedean ordered Artin local algebra]]
[[!redirects Archimedean ordered Artin local algebras]]

[[!redirects Archimedean ordered local Artin algebra]]
[[!redirects Archimedean ordered local Artin algebras]]
