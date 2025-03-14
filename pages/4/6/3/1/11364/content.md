
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
#### Elliptic cohomology
+-- {: .hide}
[[!include elliptic cohomology -- contents]]
=--
=--
=--

# Contents 
* table of contents 
{: toc}

## Idea 

Let $k$ be a [[field]], and let $\mathbb{P}^1(k)$ be the [[projective line]] over $k$. A _M&#246;bius transformation_ (also called a _homography_, a _linear fractional transformation_, or a _fractional linear transformation_) is a [[function]] $f: \mathbb{P}^1(k) \to \mathbb{P}^1(k)$ defined by the rule 

$$
  f(x)
  = 
  \frac{a x + b}{c x + d}
$$ 

where $a, b, c, d \in k$ and $a d - b c \in k^\times$ (the [[group of units]]). M&#246;bius transformations form a [[group]] under [[composition]], [[isomorphic]] to the [[projective linear group]]

$$
  PGL_2(k)
  \coloneqq  
  GL_2(k)/\{\lambda I: \lambda \in k^\times\}
  \,.
$$ 

If, as in the case $k = \mathbb{C}$ ([[complex numbers]]), each element of $k^\times$ has a [[square root]], then this group is identified with the [[projective special linear group]]

$$
  PSL_2(k) 
  \coloneqq 
  SL_2(k)/\pm I
  \,.
$$ 

Alternatively, a fractional linear transformation can be considered as synonymous with an [[automorphism]] of the [[field]] of [[rational functions]] $k(x)$ as a field over $k$ of [[transcendence degree]] 1. 

In [[complex analysis]] (which is the usual context when one speaks of M&#246;bius transformations; otherwise one usually calls them by some combination of "linear" and "fractional"), M&#246;bius transformations are precisely the [[biholomorphisms]] of the [[Riemann sphere]], hence exactly its [[bijection|bijective]] [[conformal transformations]]. 

Often, and particularly when $k$ is the the [[commutative ring]] of [[integers]] $\mathbb{Z}$, one considers a _[[modular group]]_ where the coefficients $a, b, c, d$ are assumed to lie in an [[integral domain]] and $a d - b c = 1$. (The [[homotopy quotient]] of the [[upper half-plane]] by the group $PGL_2(\mathbb{Z})$ is the [[moduli stack of elliptic curves]] over the [[complex numbers]].) 

## Properties 

### Cross-ratios 

+-- {: .num_prop} 
###### Proposition 
The action $PGL_2(k) \times \mathbb{P}^1(k) \to \mathbb{P}^1(k)$ is [[transitive action|3-transitive]], i.e., any triplet of distinct points $(a, b, c)$ may be mapped to 
any other triplet of distinct points $(a', b', c')$ by applying a group element. 
=--  

+-- {: .proof} 
###### Proof 
It suffices to consider $a' = 0, b' = 1, c' = \infty$ where one applies the transformation $x \mapsto \frac{(x-a)(b-c)}{(x-c)(b-a)}$. 
=-- 

This motivates the following definition: given a 4-tuple $(a, b, c, d)$ of distinct points in $\mathbb{P}^1(k)$, its _cross-ratio_ is 

$$\gamma(a, b, c, d) = \frac{(d-a)(b-c)}{(d-c)(b-a)}.$$ 

It is not hard to see that the group action preserves the cross-ratio, i.e., $\gamma(g \cdot a, g \cdot b, g \cdot c, g \cdot d) = \gamma(a, b, c, d)$. Moreover, the group action is transitive on each cross-ratio-equivalence class of 4-tuples. 

In the case $k = \mathbb{C}$ where $\mathbb{P}^1$ is interpreted as the Riemann sphere, it turns out that the cross-ratio of a 4-tuple is a [[real number]] if and only if the four points lie on a [[circle]] (or a line which is a circle passing through $\infty$). Hence M&#246;bius = conformal transformations take circles to circles. 

### Action on hyperbolic space 

As explained at [[Poincare group]], the group $PSL_2(\mathbb{C})$ can be identified with those [[linear transformations]] of Minkowski space $\mathbb{R}^4$ that preserve the Minkowski [[quadratic form|form]] $Q$, are [[orientation]]-preserving, and take the forward [[light cone]] $\{v = (\vec{x}, t): Q(v) = 0, t \gt 0\}$ to itself. It follows that $PSL_2(\mathbb{C})$ acts on the hyperboloid sheet 

$$H^3 = \{v = (\vec{x}, t): Q(v) = 1, t \gt 0\}$$ 

which is naturally identified with hyperbolic 3-space. There is a Poincar&#233; disk model for $H^3$; consider the disk $D^3$ that is the intersection of the [[future cone]] $\{v = (\vec{x}, t): Q(v) \geq 0, t \gt 0\}$ with the hyperplane $t = 1$. Its interior is an open 3-disk $int(D^3)$ which can be placed in perspective with $H^3$ by considering lines through the origin in $\mathbb{R}^4$: each line that passes through a unique point in $H^3$ passes through a unique point of $int(D^3)$. In this way, $D^3$ is viewed as a natural compactification of $H^3$, and the action of $PSL_2(\mathbb{C})$ on $H^3$ induces an action of $PSL_2(\mathbb{C})$ on $D^3$. The restriction of this action to the boundary $S^2 = \partial D^3$ ("the heavenly sphere") coincides with the action on the Riemann sphere $S^2 = \mathbb{P}^1(\mathbb{C})$. 

## Modular group 
 {#ModularGroup}

The _[[modular group]]_ $\Gamma$ is the subgroup $PSL_2(\mathbb{Z}) \hookrightarrow PSL_2(\mathbb{C})$ consisting of M&#246;bius transformations with [[integer]] [[coefficients]], hence maps $z \mapsto \frac{a z + b}{c z + d}$ with $a, b, c, d \in \mathbb{Z}$ and $a d - b c = 1$. 

The group $PSL_2(\mathbb{R})$ acts on the [[upper half-plane]] $H = \{z \in \mathbb{C}: Im(z) \geq 0\}$ (or rather $H \cup \{\infty\}$ as a [[subspace]] of the [[Riemann sphere]]), by restriction of the action of $PSL_2(\mathbb{C})$ on the Riemann sphere. Indeed, the action of $PSL_2(\mathbb{R})$ takes the real line $\mathbb{R} \cup \{\infty\}$ to itself, and any element $f(z) = \frac{a z + b}{c z + d}$ takes $i$ to $(b + a i)(d - c i)/(c^2 + d^2)$, whose imaginary part $(ad - b c)/(c^2 + d^2) = 1/(c^2 + d^2)$ is positive. By continuity it follows that the action preserves the sign of the imaginary part, hence takes the upper-half plane $H$ to itself. 

It is illuminating to think of complex numbers $\tau$ such that $Im(\tau) \gt 0$ as representing [[elliptic curves]] $E$. Indeed, the [[field]] of [[meromorphic functions]] on an elliptic curve (i.e., a complex projective curve $E$ of [[genus]] $1$, or a [[torus]] equipped with a structure of complex analytic 1-manifold) can be identified with a field of doubly periodic [[holomorphic functions]] $\mathbb{C}/L \to \mathbb{P}^1(\mathbb{C})$ where $L = \langle \omega_1, \omega_2\rangle$ is a fundamental lattice (a discrete cocompact subgroup of the additive [[topological group]] $\mathbb{C}$) attached to $E$. In essence, this field is generated by [[Weierstrass elliptic functions]] $\wp(z), \wp'(z): \mathbb{C}/L \to \mathbb{P}^1(\mathbb{C})$ (here $\wp'$ is the [[derivative]] of $\wp$) which satisfy a [[cubic curve|cubic algebraic relation]] 

$$(\wp')^2 = 4\wp^3 - g_2\wp - g_3$$ 

where the constants $g_2, g_3$ are expressed as certain [[Eisenstein series]] in the fundamental periods $\omega_1, \omega_2$. The $\mathbb{Z}$-[[linear basis]] elements $\omega_1, \omega_2$ of the [[lattice]] may be arranged so that $\tau = \omega_2/\omega_1$ has positive imaginary part. Of course, if there is a [[homothety]] $z \mapsto \lambda z$ that takes a lattice $L$ to a lattice $L'$, then the elliptic curves $E = \mathbb{C}/L$ and $E' = \mathbb{C}/L'$ are analytically isomorphic, so the map 

$$\tau \mapsto \mathbb{C}/\langle 1, \tau\rangle$$ 

gives a surjection from complex numbers with positive imaginary part to isomorphism classes of smooth elliptic curves. Thus we may restrict attention to lattices of the form $L = \langle 1, \tau \rangle$. 

Of course, $L$ admits more than one such basis $(1, \tau)$, but for any other $(1, \tau')$ there is a [[linear transformation]] $\gamma \in \Gamma \coloneqq PSL_2(\mathbb{Z})$ such that $\gamma(\tau) = \tau'$. In summary, the [[orbit space]] 

$$\{\tau \in \mathbb{C}: Im(\tau) \gt 0\}/\Gamma$$ 

is a coarse [[moduli space]] for elliptic curves. In this context, one often says that elliptic curves are paramatrized by the $j$-[[j-invariant|invariant]], a certain [[modular form]] $j(\tau)$ defined on the upper half-plane such that $j(\tau) = j(\tau')$ if and only if $\tau' = \gamma \cdot \tau$ for some $\gamma \in \Gamma$. 

Of course, in some cases there may be more than one $\gamma \in \Gamma$ that fixes a given $\tau$; this is notably the case when $\tau$ is a fourth root of unity or a sixth root of unity. A more refined approach then is to consider, instead of the coarse orbit space, the (compactified) [[moduli stack]] $(H \cup \{\infty\})//\Gamma$ for elliptic curves, as a central geometric object of interest. 

### Abstract structure of modular group 

As an abstract [[group]], $\Gamma = PSL_2(\mathbb{Z})$ is a [[free product]] $\mathbb{Z}/(2) \ast \mathbb{Z}/(3)$; explicitly, we may take the generator of order $2$ to be given by the Moebius transformation $z \mapsto -1/z$, and the generator of order $3$ to be given by $z \mapsto (z-1)/z$. 

This [[concrete group]] and certain of its subgroups, such as [[congruence subgroups]], are fairly ubiquitous; for example the modular group appears in the theory of [rational tangles](http://ncatlab.org/nlab/show/continued+fraction#rational_tangles) and of  [[combinatorial map|trivalent maps]], and these groups frequently crop up in the theory of buildings (stuff on hyperbolic buildings to be filled in). 

It is also worth pointing out that $\Gamma$ is a quotient of the [[braid group]] $B_3$. Consider the standard Artin presentation of $B_3$, with two generators $\sigma_1$, $\sigma_2$ subject to the relation 

$$\sigma_1 \sigma_2 \sigma_1 = \sigma_2 \sigma_1 \sigma_2.$$ 

Then $z \coloneqq (\sigma_1 \sigma_2)^3$ is a [[center|central element]] of $B_3$, and there is a central extension 

$$1 \to \mathbb{Z} \stackrel{1 \mapsto z}{\to} B_3 \stackrel{q}{\to} \Gamma \to 1$$ 

where $q$ is the unique homomorphism mapping $\sigma_1\sigma_2$ to $\lambda z. (z-1)/z$, and $\sigma_1\sigma_2\sigma_1$ to $\lambda z. \frac{-1}{z}$. 

## Related concepts

* [[SL(2,Z)]]

* [[conformal group]]

* [[Kleinian group]]

* [[elliptic fibration]]

* [[congruence subgroup]]

* [[level n subgroup]], 

* [[modular equivariant elliptic cohomology]]

## References

Named after _[[August Möbius]]_.

* [[Jean-Pierre Serre]], §VII.1 of: *A Course in Arithmetic*, Graduate Texts in Mathematics **7**, Springer (1973) &lbrack;[doi:10.1007/978-1-4684-9884-4](https://doi.org/10.1007/978-1-4684-9884-4), [pdf](https://www.math.purdue.edu/~jlipman/MA598/Serre-Course%20in%20Arithmetic.pdf)&rbrack;


See also:

* Wikipedia, _[Projective linear group](https://en.m.wikipedia.org/wiki/Projective_linear_group)_

[[!redirects PSL(2,C)]]
[[!redirects PSL(2,Z)]]

[[!redirects Moebius transformations]]
[[!redirects moebius transformation]]
[[!redirects moebius transformations]]
[[!redirects Möbius transformation]] 
[[!redirects Möbius transformations]] 
[[!redirects möbius transformation]] 
[[!redirects möbius transformations]] 
[[!redirects linear fractional transformation]]
[[!redirects linear fractional transformations]]
[[!redirects fractional linear transformation]]
[[!redirects fractional linear transformations]]

[[!redirects Möbius group]]
[[!redirects Moebius group]]


