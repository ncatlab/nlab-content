
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

A _vielbein_ or _soldering form_ on a [[manifold]] $X$ is a linear identification of a [[tangent bundle]] with a [[vector bundle]] with explicit [[orthogonal structure]].

Any such choice encodes a [[Riemannian metric]] on $X$. 

## Definition

### In terms of $iso$-connections

A [[Lie algebra valued 1-form]]

$$
  (E,\Omega) : T X \to \mathfrak{iso}(d)
$$

with values in the [[Poincare Lie algebra]] encodes a [[pseudo-Riemannian metric]] on $X$. In this context the component 

$$
  E : T X \to \mathbb{R}^d
$$

of the [[connection on a bundle|connection]] 1-form is called the _vielbein_ . It encodes the metric by

$$
  g = \langle E \otimes E\rangle  \in Sym^2_{C^\infty(X)} \Gamma(T^* X)
  \,,
$$

where $\langle -,-\rangle : \mathbb{R}^d \times \mathbb{R}^d \to \mathbb{R}$ is the canonical [[bilinear form]].

For $d=4$ this is the _vierbein_ , for $d = 3$ the _dreibein_ , etc.

This terminology is used in the [[first-order formulation of gravity]]. 

Globally we have that a $O(n) \hookrightarrow iso(n)$-[[Cartan connection]] on a manifold $X$ encodes a vielben and compatible [[spin connection]].

### In terms of orthogonal structure / twisted cohomology

We discuss the notion of vielbein / [[orthogonal structure]] on a [[smooth manifold]] as a special case of a [[twisted differential c-structure]].

Let $X$ be of [[dimension]] $n$. Write $\mathbf{B} O(n)$ for the [[smooth infinity-groupoid|smooth]] [[moduli stack]] of [[orthogonal group]]-[[principal bundles]]. This is the [[delooping]] of $O(n)$ in $\mathbf{H} = $  [[Smooth∞Grpd]].

Similarly, let $\mathbf{B} GL(n)$ be the [[delooping]] of the [[general linear group]], regarded as a [[Lie group]]. 

The canonical group embedding 

$$
  O(n) \hookrightarrow GL(n)
$$

induces a corresponding morphism of moduli stacks

$$
  \mathbf{B} O(n) \to \mathbf{B} GL(n)
  \,.
$$


Without any choices, there is a canonical morphism of [[smooth infinity-groupoid|smooth stacks]]

$$
  T X : X \to \mathbf{B} GL(n)
$$

corresponding to the [[tangent bundle]] of $X$.

A choice of [[orthogonal structure]] on $T X$ is a factorization of this morphism through $\mathbf{c}$, up to a smooth [[homotopy]].

The [[groupoid]] / [[moduli stack]] of orthogonal structures is the groupoid of "$TX$-twisted" $\mathbf{c}$-structure" (in the sense discussed [[twisted differential c-structure|here]]), the [[homotopy pullback]]

$$
  \array{
    \mathbf{c}Struc_{TX}(X)
    &\to&
    * 
    \\
    \downarrow &\swArrow_{e}^\simeq& \downarrow^{\mathrlap{T X}}
    \\
    \mathbf{H}(X, \mathbf{B} O(n))
    &\stackrel{\mathbf{H}(X, \mathbf{c})}{\to}&
    \mathbf{H}(X, \mathbf{B} GL(n))
  }
  \,.
$$

An object in $\mathbf{c} Struc_{TX}$ is

* a choice of $O(n)$-[[principal bundle]] $P : X \to \mathbf{B} O(n)$ on $X$;

* a choice of [[isomorphism]] of $T X$ with $P$ as $GL(n)$-principal bundles

  $$
    e : T X \stackrel{\simeq}{\to} P 
    \,.
  $$

This is the vielbein. Over a [[coordinate patch]] $\phi : \mathbb{R}^n \to X$ with respect to the induced trivialization of $T X$ and a given chosen trivialization of $P$, this is a [[matrix]]-valued function

$$
  e|_\phi = \{e^q{}_{\mu}\}
  \,.
$$

Next, a [[morphism]] in $\mathbf{c}Struc_{T X}$ is an $O(n)$-[[gauge transformation]] of $P$ and hence of $e$.

Therefore the [[truncated|0-truncation]] of $\mathbf{c}Struc_{T X}$ is the space of [[Riemannian metrics]] / [[orthogonal structures]] on $X$.

We may further lift this discussion to [[differential cohomology]] to get genuine _differential_ $T X$-twisted $\mathbf{c}$-structures. This introduces in addition the [[Levi-Civita connection]] in $X$ with respect to the given vielbein.

## Related concepts

* [[reduction of structure groups]], [[orthogonal structure]]

* [[generalized vielbein]], [[exceptional generalized geometry]]


[[!redirects vielbeine]]
[[!redirects vielbeins]]


[[!redirects soldering form]]
[[!redirects soldering forms]]