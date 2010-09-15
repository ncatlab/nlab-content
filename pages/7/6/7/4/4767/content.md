
# Logarithms
* table of contents
{: toc}

## Idea

Classically, a logarithm is a [[partial function|partially-defined]] [[smooth map|smooth]] [[homomorphism]] from a multiplicative [[group]] of [[number]]s to an additive group of numbers.  As such, it is a [[partial section]] of an [[exponential map]].  As exponential maps can be generalised to [[Lie groups]], so can logarithms.


## Definitions

### Logarithms of real numbers

Consider the [[field]] of [[real numbers]]; these numbers form a [[Lie group]] under addition (which we will call simply $\mathbb{R}$), while the nonzero numbers form a Lie group under multiplication (which we will call $\mathbb{R}^*$).  The multiplicative group has two [[connected components]]; we will focus attention on the [[identity component]] (which we will call $\mathbb{R}^+$), consisting of the positive numbers.

The Lie groups $\mathbb{R}$ and $\mathbb{R}^+$ are in fact [[isomorphic]].  In fact, there is one isomorphism for each positive real number $b$ other than $1$; this number $b$ is called the __base__.  Fixing a base, the map from $\mathbb{R}^+$ to $\mathbb{R}$ is called the __real logarithm with base $b$__, written $x \mapsto \log_b x$; the map from $\mathbb{R}$ to $\mathbb{R}^+$ is the __real [[exponential map]] with base $b$__, written $x \mapsto b^x$.

The real logarithms are handily defined using the [[Riemann integral]] as follows:
\[ \label{integrals} \array {
   \ln x & \coloneqq \int_1^x \frac{1}{x} ;\\
   \log_b x & \coloneqq \frac{\ln x}{\ln b} .\\
} \]
Note that $\ln$ is itself a logarithm, the __natural logarithm__, whose base is $\mathrm{e} = 2.71828182845\ldots$.  (The exponential map may similarly be defined as an infinite series, but I\'ll leave that for its own article.)


### Logarithms of complex numbers

Now consider the [[field]] of [[complex numbers]]; these also form a [[Lie group]] under addition (which we call $\mathbb{C}$), while the nonzero numbers form a Lie group under multiplication (which we call $\mathbb{C}^*$).  Now the multiplicative group is [[connected space|connected]], so we would like to use all of it.

However, $\mathbb{C}$ and $\mathbb{C}^*$ are *not* [[isomorphic]].  In fact, not only is there no isomorphism from $\mathbb{C}^*$ to $\mathbb{C}$; the only such [[homomorphism]] is the [[zero morphism]] $x \mapsto 0$.  (Essentially, this is because $\mathbb{C}$ is [[simply connected space|simply connected]] while $\mathbb{C}^*$ is not.)  On the other hand, we still have plenty of homomorphisms from $\mathbb{C}$ to $\mathbb{C}^*$, one for each nonzero complex number $b$, and these homomorphisms are [[surjections]] whenever $b \ne 1$.

So we have these surjections (the __complex [[exponential map]] with base $b$__, for $b \ne 1$), which are [[regular epimorphisms]] but not [[split epimorphisms]].  However, while they have no [[sections]] (being not split), they have quite a few [[partial section]]s, and the [[domains]] of the [[maximal partial function|maximal]] partial sections are precisely the [[connected space|connected]] [[simply connected space|simply connected]] [[dense subspace|dense]] subspaces $R$ of $\mathbb{C}^*$.  The __complex logarithm with base $b$ on $R$__ is this $R$-defined section of the complex exponential map with base $b$.

The complex logarithms are handily defined using the [[contour integral]] using the same formulas (eq:integrals) as for the real logarithms.  We merely insist that the integral be done along a contour within the region $R$.  (Since $R$ is connected, there is such a contour; since $R$ is simply connected and $x \mapsto 1/x$ is [[holomorphic map|holomorphic]], the result is unique.)  Note that if $x \in \mathbb{R}^+ \subseteq R$, then the real and complex logarithms of $x$ will be equal.


### Logarithms and Lie groups

In the classical examples, the multiplicative groups $\mathbb{R}^+$ and $\mathbb{C}^*$ are both [[Lie groups]].  The additive groups $\mathbb{R}$ and $\mathbb{C}$ are also Lie groups, but they are more than this: they are [[Lie algebras]].  (The additive group of a Lie algebra is always a Lie group.  Actually, since these are [[abelian Lie algebras]], their Lie-algebra structure is easy to miss, but of course they are [[vector spaces]].)  And what\'s more, each additive group is *the* Lie algebra of the corresponding Lie group.

This generalises.  Given any [[Lie group]] $G$, let $\mathfrak{g}$ be its [[Lie algebra]].  Then we have an [[exponential map]] $\exp\colon \mathfrak{g} \to G$, which is [[surjection|surjective]] under certain conditions (most famously when $G$ is [[connected space|connected]] and [[compact space|compact]], but also in the classical cases, even though $G$ is not compact).  More generally, given any [[automorphism]] $\phi$ of $\mathfrak{g}$, we have a map $x \mapsto \exp(\phi(g))$, which is a [[homomorphism]] of Lie groups.  Any [[partial section]] of this map may be called a __logarithm base $\phi$__ on $G$; any partial section of $\exp$ itself may be called a __natural logarithm__ on $G$.


[[!redirects logarithm]]
[[!redirects logarithms]]
[[!redirects natural logarithm]]
[[!redirects natural logarithms]]
