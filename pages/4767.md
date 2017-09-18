
# Logarithms
* table of contents
{: toc}

## Idea

Classically, a logarithm is a [[partial function|partially-defined]] [[smooth map|smooth]] [[homomorphism]] from a multiplicative [[group]] of [[number]]s to an additive group of numbers.  As such, it is a [[local section]] of an [[exponential map]].  As exponential maps can be generalised to [[Lie groups]], so can logarithms.


## Definitions

### Logarithms of real numbers

Consider the [[field]] of [[real numbers]]; these numbers form a [[Lie group]] under addition (which we will call simply $\mathbb{R}$), while the nonzero numbers form a Lie group under multiplication (which we will call $\mathbb{R}^*$).  The multiplicative group has two [[connected components]]; we will focus attention on the [[identity component]] (which we will call $\mathbb{R}^+$), consisting of the positive numbers.

The Lie groups $\mathbb{R}$ and $\mathbb{R}^+$ are in fact [[isomorphic]].  In fact, there is one isomorphism for each positive real number $b$ other than $1$; this number $b$ is called the __base__.  Fixing a base, the map from $\mathbb{R}^+$ to $\mathbb{R}$ is called the __real logarithm with base $b$__, written $x \mapsto \log_b x$; the map from $\mathbb{R}$ to $\mathbb{R}^+$ is the __real [[exponential map]] with base $b$__, written $x \mapsto b^x$.

The real logarithms are handily defined using the [[Riemann integral]] as follows:
\[ \label{integrals} \array {
   \ln x & \coloneqq \int_1^x \frac{1}{t} \,\mathrm{d}t ;\\
   \log_b x & \coloneqq \frac{\ln x}{\ln b} .\\
} \]
Note that $\ln$ is itself a logarithm, the __natural logarithm__, whose base is $\mathrm{e} = 2.71828182845\ldots$.  (The exponential map may similarly be defined as an infinite series, but I\'ll leave that for its own article.)


### Logarithms of complex numbers

Now consider the [[field]] of [[complex numbers]]; these also form a [[Lie group]] under addition (which we call $\mathbb{C}$), while the nonzero numbers form a Lie group under multiplication (which we call $\mathbb{C}^*$).  Now the multiplicative group is [[connected space|connected]], so we would like to use all of it.

However, $\mathbb{C}$ and $\mathbb{C}^*$ are *not* [[isomorphic]]. Indeed, the multiplication map 

$$\mathbb{R}^* \times S^1 \to \mathbb{C}^*$$ 

exhibits $\mathbb{C}^*$ as a [[biproduct]] of $\mathbb{R}^*$ and the [[circle group]] $S^1$, so that homomorphisms $\mathbb{C}^* \to \mathbb{C}$ are given by pairs of homomorphisms $f \colon \mathbb{R}^* \to \mathbb{C}$, $g \colon S^1 \to \mathbb{C}$. But every homomorphisms $g \colon S^1 \to \mathbb{C}$ is trivial: the restriction of $g$ to the [[torsion subgroup]] of $S^1$ is trivial since $\mathbb{C}$ is torsionfree, and since the torsion subgroup is dense in $S^1$, any Lie group homomorphism $S^1 \to \mathbb{C}$ must also be trivial. Therefore, every homomorphism $h \colon \mathbb{C}^* \to \mathbb{C}$ factors through the projection $\mathbb{C}^* \to \mathbb{R}^*$. It quickly follows that no such $h$ can be injective, nor can such $h$ be surjective. 

Taking advantage of biproduct representations $\mathbb{C} \cong \mathbb{R} \oplus \mathbb{R}$ and $\mathbb{C}^* \cong \mathbb{R}^* \oplus S^1$, we can classify homomorphisms from $\mathbb{C}$ to $\mathbb{C}^*$. Each is given by a 4-tuple of real numbers $(a, b, c, d)$: 

$$\phi_{a, b, c, d}(x + i y) = e^{a x} e^{i b x} e^{c y} e^{i d y}.$$ 

The cases where $a = d$, $b = -c$ correspond to those homomorphisms that are [[holomorphic functions]] (i.e., that satisfy the [[Cauchy-Riemann equations]]). Putting $w = a + b i$, we have 

$$\phi_{a, b, -b, a}(z) = e^{w z}$$ 

with one such homomorphism for each complex number $w$, and these homomorphisms are [[surjections]] whenever $w \ne 0$. (N.B.: these homomorphisms are not uniquely determined by their values at $z = 1$, since we have $e^w = e^{w'}$ whenever $w - w'$ is an integer multiple of $2 \pi i$, and yet the homomorphisms $z \mapsto e^{w z}$ and $z \mapsto e^{w' z}$ will be different unless $w = w'$.) 

So we have these surjections (the __complex [[exponential map]]__ $z \mapsto e^{w z}$, for $w \ne 0$), which are [[regular epimorphisms]] but not [[split epimorphisms]].  However, while they have no [[sections]] (being not split), they have quite a few [[local sections]], and the [[domains]] of the [[maximal local sections]] are precisely the [[connected space|connected]] [[simply connected space|simply connected]] [[open subspace|open]] [[dense subspace|dense]] subspaces $R$ of $\mathbb{C}^*$.  A __complex logarithm with exponential base $w$ on $R$__ is this $R$-defined section of the complex exponential map $z \mapsto e^{w z}$. Supposing $R$ given, we denote this by $\log_{[w]}$ (but please note that in the context of real logarithms, this would ordinarily be denoted $\log_b$ where $b = e^w$). 

If $1 \in R$, then a complex natural logarithm on $R$ may be defined using the [[contour integral]] with the same formula (eq:integrals) as for the real natural logarithm.  We merely insist that the integral be done along a contour within the region $R$.  (Since $R$ is connected, there is such a contour; since $R$ is simply connected and $t \mapsto 1/t$ is [[holomorphic map|holomorphic]], the result is unique.)  Note that if $x \in \mathbb{R}^+ \subseteq R$, then the real and complex natural logarithms of $x$ will be equal. 

The natural exponential map is [[periodic function|periodic]] (with period $2 \pi \mathrm{i}$), and it is possible to add any multiple of this period to the natural logarithm of any $x \ne 1$ by suitably changing the region $R$.  We then obtain the most general notion of maximally-defined complex logarithm with any base by using the formulas
$$ \array {
   \ln x & \coloneqq C + \int_{\mathrm{e}^C}^x \frac{1}{t} \,\mathrm{d}t,\\
   \log_{[w]} x & \coloneqq \frac{\ln x}{w} .\\
} \]


### Logarithms and Lie groups

In the classical examples, the multiplicative groups $\mathbb{R}^+$ and $\mathbb{C}^*$ are both [[Lie groups]].  The additive groups $\mathbb{R}$ and $\mathbb{C}$ are also Lie groups, but they are more than this: they are [[Lie algebras]].  (The additive group of a Lie algebra is always a Lie group.  Actually, since these are [[abelian Lie algebras]], their Lie-algebra structure is easy to miss, but of course they are [[vector spaces]].)  And what\'s more, each additive group is *the* Lie algebra of the corresponding Lie group.

This generalises.  Given any [[Lie group]] $G$, let $\mathfrak{g}$ be its [[Lie algebra]].  Then we have an [[exponential map]] $\exp\colon \mathfrak{g} \to G$, which is [[surjection|surjective]] under certain conditions (most famously when $G$ is [[connected space|connected]] and [[compact space|compact]], but also in the classical cases, even though $G$ is not compact).  More generally, given any [[automorphism]] $\phi$ of $\mathfrak{g}$, we have a map $x \mapsto \exp(\phi(x))$, which is a [[homomorphism]] of Lie groups.  Any [[local section]] of this map may be called a __logarithm base $\phi$__ on $G$ (denoted $\log_{[\phi]}$ with the bracket as in the previous section); any local section of $\exp$ itself may be called a __natural logarithm__ on $G$.


## Related concepts

* [[logarithmic integral function]]

* [[logarithmic cohomology operation]]


[[!redirects logarithm]]
[[!redirects logarithms]]
[[!redirects logarithmic]]

[[!redirects natural logarithm]]
[[!redirects natural logarithms]]
