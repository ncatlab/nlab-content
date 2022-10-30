
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In analogy to how in ordinary [[algebra]] the natural [[logarithm]] of [[positive number|positive]] [[rational numbers]] is a [[group]] [[homomorphism]] from the [[group of units]] to the completion of the rationals by the (additive) [[real numbers]]

$$
  log \;\colon\; \mathbb{Q}^\times_{\gt 0}\longrightarrow \mathbb{R}
$$

so in [[higher algebra]] for $E$ an [[E-∞ ring]] there is a natural homomorphism

$$
  \ell_{n,p} \;\colon\; gl_1(E) \longrightarrow L_{K(n)} E
$$

from the [[∞-group of units]] of $E$ to the [[K(n)-local spectrum]] obtained from $E$ (see [Rezk 06, section 1.7](#Rezk06)).

On the [[cohomology theory]] [[Brown representability theorem|represented]] by $E$ this induces a [[cohomology operation]] called, therefore, the "logarithmic cohomology operation".

More in detail, for $X$ the [[homotopy type]] of a  [[topological space]], then the [[cohomology]] [[Brown representability theorem|represented]] by $gl_1(E)$ in degree 0 is the ordinary [[group of units]] in the [[cohomology ring]] of $E$:

$$
  H^0(X, gl_1(E))  \simeq (E^0(X))^\times
  \,.
$$

In positive degree the canonical map of pointed homotopy types $GL_1(E) = \Omega^\infty gl_1(E) \to \Omega^\infty E$ is in fact an [[isomorphism]] on all [[homotopy groups]]

$$
  \pi_{\bullet \geq 1} GL_1(E) \simeq \pi_{\bullet \geq 1} \Omega^\infty E
  \,.
$$

On cohomology elements this map

$$
  \pi_q(gl_1(E)) \simeq \tilde H^0(S^q, gl_1(E)) \simeq  (1+ \tilde R^0(S^q))^\times \subset (R^0(S^q))^\times
$$

is [[logarithm]]-like, in that it sends $1 + x \mapsto x$.

But there is not a homomorphism of [[spectra]] of this form. This only exists after [[K(n)-local stable homotopy theory|K(n)-localization]], and that is the logarithmic cohomology operation.



## Definition

By the [[Bousfield-Kuhn construction]] there is an [[equivalence]] of spectra

$$
  L_{K(n)} gl_1(E) \simeq L_{K(n)}E
$$

between the [[K(n)-local spectrum]] induced by the [[abelian ∞-group|abelian]] [[∞-group of units]] of $E$ (regarded as a [[connective spectrum]]) with that induced by $E$ itself. The logarithm on $E$ is the [[composition|composite]] of that with the [[Bousfield localization of spectra|localization map]]

$$
 \ell_{n,p}
  \;\colon\; 
 gl_1(E) \stackrel{}{\longrightarrow} L_{K(n)}gl_1(E) \stackrel{\simeq}{\to}  L_{K(n)} E
  \,.
$$

(see [Rezk 06, section 3](#Rezk06)).

## Properties

 
### Action on cohomology groups
 {#ActionOnCohomologyGroups}

For every [[E-∞ ring]] $E$ and spaces $X$, [[prime number]] $p$ and [[natural number]] $n$, the logarith induces a homomorphism of [[cohomology groups]] of the form

$$
  \ell_{n,p}
   \;\colon\;
  (E^0(X))^\times
    \longrightarrow
  (L_{K(n)}E)^0(X)
  \,.
$$

### Explicit formula in terms of power operations

Under some conditions there is an explicit formula of the logarithmic cohomology operation by a [[series]] of [[power operations]].


Let $E$ be a [[K(n)-local stable homotopy theory|K(1)-local]] [[E-∞ ring]] such that

* the [[kernel]] of $\pi_0 L_{K(1)}\mathbb{S} \longrightarrow \pi_0 E$ contains the [[torsion subgroup]] of $\pi_0 L_{K(1)}\mathbb{S}$.

(This is for instance the case for $L_{K(1)}$[[tmf]]).

Then on a [[finite CW complex]] $X$ the logarithmic cohomology operation from [above](#ActionOnCohomologyGroups)

$$
  \ell_{1,p}\;\colon\; (E^0(X))^\times \longrightarrow E^0(X)
$$

is given by the [[series]]

$$
  \begin{aligned}
    \ell_{1,p} \colon x 
     & \mapsto 
     \left(
       1 - \frac{1}{p}\psi
     \right)
     log(x)
     \\
     & = \frac{1}{p} log \frac{x^p}{\psi(x)}
     \\
     & = \sum_{k=1}^\infty (-1)^k \frac{p^{k-1}}{k}\left( \frac{\theta(x)}{x^p}\right)^k
     \\
   \end{aligned}
$$

which [[convergence of a sequence|converges]] [[p-adic numbers|p-adically]].

([Rezk 06, theorem 1.9](#Rezk06), see also [Ando-Hopkins-Rezk 10, prop. 4.5](#AndoHopkinsRezk10))

Here $\theta$ ....

In the special case that $x = 1 + \epsilon$ with $\epsilon^2 = 0$ then this reduces to

$$
  \ell_{1,p}(1+ \epsilon)= \epsilon - \frac{1}{p}\psi(\epsilon)
   \,.
$$


### Relation to the string-orientation of $tmf$


The above expression in terms of power operations may be used to establish the [[string orientation of tmf]] ([Ando-Hopkins-Rezk 10](#AndoHopkinsRezk10)).

...

## References
 {#References}

The logarithmic operation for $p$-complete [[K-theory]] was first described in 

* [[Tammo tom Dieck]],  _The Artin-Hasse logarithm for &#955;-rings_, Algebraic topology (Arcata, CA, 1986), 409&#8211;415, Lecture Notes in Math., 1370, Springer, Berlin, 1989.

The formulation in terms of the [[Bousfield-Kuhn functor]] and the expression in terms of [[power operations]] is due to

* {#Rezk06} [[Charles Rezk]], _The units of a ring spectrum and a logarithmic cohomology operation_, J. Amer. Math. Soc. 19 (2006), 969-1014 ([arXiv:math/0407022](http://arxiv.org/abs/math/0407022))

The application of this to the [[string orientation of tmf]] is due to

* {#AndoHopkinsRezk10} [[Matthew Ando]], [[Mike Hopkins]], [[Charles Rezk]], _Multiplicative orientations of KO-theory and the spectrum of topological modular forms_, 2010 ([pdf](http://www.math.uiuc.edu/~mando/papers/koandtmf.pdf))



[[!redirects logarithmic cohomology operations]]