
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

## Definition

An ordered Artinian local ring is a [[local ring]] which is both an [[ordered local ring]] and an [[Artinian local ring]]: a [[commutative ring]] $R$ with a [[strict order]] $\lt$ such that the positive elements form a [[multiplicative subset]] of $R$, the sum of two positive elements is positive, every element $a \in R$ is invertible if and only if it is positive or negative, and the set of non-invertible elements forms a [[nilradical]]. 

Ordered Artinian local rings are important because they are the [[ordered local rings]] with [[nilpotent]] [[infinitesimals]], and thus play an important role in synthetic approaches to [[analysis]] and [[differential geometry]]. 

Ordered fields are the ordered Artinian local rings in which the [[nilradical]] is the [[trivial|trivial ideal]], or equivalently, in which every non-invertible element is equal to zero. 

## Properties

### Purely real and purely infinitesimal elements

Suppose that $K$ is an [[ordered field]] and $A$ is an ordered Artinian local $K$-algebra with no [[infinite elements]]. Since $A$ is an [[Artinian local ring]], the quotient of $A$ by its nilradical of non-invertible elements $I$ is the [[residue field]] $K$ itself, and the canonical function used in defining the quotient is the function $\Re:A \to K$ which takes a number $a \in A$ to its purely real component $\Re(a) \in K$. Since $A$ is an ordered $K$-algebra, there is a [[strictly monotone]] [[ring homomorphism]] $h:K \to A$. An element $a \in A$ is **purely real** if $h(\Re(a)) = a$, and an element $a \in A$ is **purely [[infinitesimal]]** if it is in the [[fiber]] of $\Re$ at $0 \in K$. Zero is the only element in $A$ which is both purely real and purely infinitesimal. 

### Prelattice structure

Now, suppose that the [[ordered field]] $K$ has [[lattice]] structure $\min:K \times K \to K$ and $\max:K \times K \to K$. The ordered Artinian local $K$-algebra $A$ with no [[infinite elements]] has a [[prelattice]] structure given by functions $\min':A \times A \to A$ and $\max':A \times A \to A$, defined by 
$$\min'(a, b) \coloneqq h(\min(\Re(a), \Re(b)))$$
and 
$$\max'(a, b) \coloneqq h(\max(\Re(a), \Re(b)))$$

### Pseudometric structure

If $K$ is additionally an [[Archimedean ordered field]], then $A$ has no [[infinite elements]], and the [[pseudometric]] on $A$ is given by the function $\rho:A \times A \to K$, defined as 

$$\rho(a, b) \coloneqq \max(\Re(a), \Re(b)) - \min(\Re(a), \Re(b))$$

and the [[absolute value]] on $A$ is given by the function $\vert-\vert:A \times A \to K$, defined as 

$$\vert a \vert \coloneqq \rho(a, 0)$$

These are pseudometrics and absolute values because every ordered field $K$ embeds into the [[real numbers]] $\mathbb{R}$. This also implies that in every ordered field with lattice structure, the pseudometric defined above is a metric. 

### Smooth and differentiable function structure

Suppose that $K$ is an [[Archimedean ordered field]] with lattice structure, and $A$ is an ordered Artinian local $K$-algebra with no [[infinite elements]]. Then [[continuous functions]], [[differentiable functions]], and [[smooth functions]] are each definable on $K$ using the algebraic, order, and metric structure on $K$. 

The ring homomorphism $h:K \to A$ preserves [[smooth functions]]: given a natural number $n \in \mathbb{N}$ and a purely infinitesimal element $\epsilon \in I$ such that $\epsilon^{n + 1} = 0$, then for every [[smooth function]] $f \in C^\omega(K)$, there is a function $f_A:A \to A$ such that for all elements $x \in K$, $f_A(h(x)) = h(f(x))$ and 
$$f_A(h(x) + \epsilon) = \sum_{i = 0}^{n} \frac{1}{i!} h\left(\frac{d^i f}{d x^i}(x)\right) \epsilon^i$$ 

If we restrict to ordered Artinian local $K$-algebras $A$ where every element of the nilradical $I$ is a nilsquare element, where for all $\epsilon \in I$, $\epsilon^2 = 0$, then the ring homomorphism $h:K \to A$ preserves [[differentiable functions]]; for every [[differentiable function]] $f:K \to K$ with given [[derivative]] $f':K \to K$, there is a function $f_A:A \to A$ such that for all elements $x \in K$ and nilpotent elements $\epsilon \in I$, $f_A(h(x)) = h(f(x))$ and 
$$f_A(h(x) + \epsilon) = h(f(x)) + h(f'(x)) \epsilon$$ 

In particular, every [[polynomial function]] $p:K \to K$ lifts to a polynomial function $p_A:A \to A$. 

### Metric square roots

Now, assume that $K$ is an [[Euclidean field]] as well, in addition to being an [[Archimedean ordered field]]. While $K$ has a [[principal square root function]] $\sqrt{-}:[0, \infty) \to [0, \infty)$, not every ordered Artinian local $K$-algebra $A$ without infinite elements has a principal square root function $\sqrt{-}:[0, \infty) \to [0, \infty)$, because purely infinitesimal elements in $A$ are not guaranteed to have [[square roots]]. An ordered Artinian local $K$-algebra without infinite elements is **Euclidean** if every nilpotent element has a square root. 

## See also

* [[ordered local ring]]

* [[Artinian local ring]]

* [[ordered field]]

[[!redirects ordered Artinian local ring]]
[[!redirects ordered Artinian local rings]]

[[!redirects ordered local Artinian ring]]
[[!redirects ordered local Artinian rings]]

[[!redirects ordered Artinian local algebra]]
[[!redirects ordered Artinian local algebras]]

[[!redirects ordered local Artinian algebra]]
[[!redirects ordered local Artinian algebras]]

[[!redirects ordered Artin local ring]]
[[!redirects ordered Artin local rings]]

[[!redirects ordered local Artin ring]]
[[!redirects ordered local Artin rings]]

[[!redirects ordered Artin local algebra]]
[[!redirects ordered Artin local algebras]]

[[!redirects ordered local Artin algebra]]
[[!redirects ordered local Artin algebras]]