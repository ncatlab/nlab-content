
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}


## Idea

A _symplectic $\infty$-groupoid_ is a [[smooth ∞-groupoid]] equipped with a [[symplectic form]], or, more generally, with an [[n-plectic form]].

This is the generalization of the notion of [[symplectic manifold]] to [[higher symplectic geometry]]. It is also the image under [[Lie integration]] of the notion of [[symplectic Lie n-algebroid|symplectic L-∞ algebroid]], which is also a higher analog of symplectic manifolds, but in an [[infinitesimal object|infinitesimal]] way.

Notice that every symplectic manifold is in particular a [[Poisson manifold]] and that the structure of a Poisson manifold is equivalently encoded in the corresponding [[Poisson Lie algebroid]]. A _[[symplectic groupoid]]_ is the [[Lie integration]] of such a Poisson Lie algebroid. Therefore, strictly speaking, already "ordinary" symplectic geometry secretly involves [[Lie groupoid]]s. This insight is exploited in the refinement of [[geometric quantization of symplectic groupoids]]. 

## Definition

For any $n \in \mathbb{N}$, a _[[symplectic Lie n-algebroid]]_ $(\mathfrak{P}, \omega)$ is an [[L-∞ algebroid]] $\mathfrak{P}$ that is equipped with a quadratic and non-degenerate $L_\infty$-[[invariant polynomial]].

Under [[Lie integration]] $\mathfrak{P}$ integrates to a [[smooth infinity-groupoid|smooth n-groupoid]] $\tau_n \exp(\mathfrak{P})$. Under the [[∞-Chern-Weil homomorphism]] the invariant polynomial induces an [[smooth infinity-groupoid -- structures|differential form on an ∞-groupoid]]

$$
  \omega : \tau_n \exp(\mathfrak{P}) \to \flat_{dR} \mathbf{B}^{n+2} \mathbb{R}
$$

representing a class $[\omega] \in H^{n+2}_{dR}(\tau_n \exp(\mathfrak{P}))$.

Let 

$$
  SymplSmooth\infty Grpd
  \hookrightarrow
  Smooth\infty Grpd/(\coprod_{n}\mathbf{\flat}_{dR}\mathbf{B}^{n+2}\mathbb{R})
$$

be the full [[sub-(∞,1)-category]] of the [[over-(∞,1)-topos]] of [[Smooth∞Grpd]] over the de Rham coefficient objects on those objects in the image of this construction.

We say an object on $SymplSmooth \infty Grpd$ is a **symplectic smooth $\infty$-groupoid**.

(There are evident variations of this for the ambient [[Smooth∞Grpd]] replaced by some variant, such as [[SynthDiff∞Grpd]] or [[SmoothSuper∞Grpd]].)

## Examples
  {#ByLieIntegration}

The [[symplectic form]] $\omega$ on a [[symplectic Lie n-algebroid]] $\mathfrak{a}$ is Lie theoretically an [[invariant polynomial]]. Therefore by [[infinity-Chern-Weil theory]] it induces a moprhism

$$
  \exp(\omega) 
    :  
  \tau_n\exp(\mathfrak{a}) 
    \to 
  \mathbf{\flat}_{dR} \mathbf{B}^{n+2} \mathbb{R}
$$

from the [[Lie integration]] of $\mathfrak{a}$ to the de Rham coefficient object: this is an $(n+2)$-form on a [[smooth ∞-groupoid]] (as discussed at [smooth ∞-groupoid -- structures -- de Rham cohomology](http://ncatlab.org/nlab/show/smooth+infinity-groupoid+--+structures#StrucDeRham)) and hence equips $\exp(\mathfrak{a})$ with the structure of a symplectic $\infty$-groupoid. 

We spell this out in some special cases.

### $n = 0$ -- Symplectic manifolds

A [[symplectic Lie n-algebroid|symplectic Lie 0-algebroid]] is simply a [[symplectic manifold]], and so is its [[Lie integration]].

### $n = 1$ -- Symplectic groupoids from Poisson Lie algebroids
 {#SymplecticGroupoidsFromPoissonLieAlgebroids}

We discuss the [[Lie integration]] of [[Poisson Lie algebroids]] to [[symplectic groupoids]]. For more details and applications of this see at _[[extended geometric quantization of 2d Chern-Simons theory]]_.

Let $\mathfrak{P}$ be the [[Poisson Lie algebroid]] corresponding to a [[Poisson manifold]] that comes from a [[symplectic manifold]] $(X,\omega)$.

The [[symplectic groupoid]] associated to this is (by the discussion there) supposed to be the [[fundamental groupoid]] 
$\Pi_1(X)$ of $X$ equipped on its space of morphisms with the differential form $p_1^* \omega - p_2^* \omega$, where $p_1,p_2$ are the two endpoint projections from paths in $X$ to $X$.

We demonstrate in the following how this is indeed the result of applying the [[∞-Chern-Weil homomorphism]] to this situation.

For simplicity we shall start with the simple situation where $(X,\omega)$ has a global [[Darboux coordinate chart]] $\{x^i\}$. Write $\{\omega_{i j}\}$ for the components of the [[symplectic form]] in these coordinates, and $\{\omega^{i j}\}$ for the components of the [[inverse]].


Then the [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{P})$ is generated from $\{x^i\}$ in degree 0 and $\{\partial_i\}$ in degree 1, with differential given by

$$
  d_{CE} x^i = - \omega^{i j} \partial_j
$$

$$
  d_{CE} \partial_i = \frac{\partial \pi^{j k}}{\partial x^i} \partial_j \wedge \partial_k = 0
  \,.
$$

The differential in the corresponding [[Weil algebra]] is hence

$$
  d_{W} x^i = - \omega^{i j} \partial_j + \mathbf{d}x^i
$$

$$
  d_{W} \partial_i = \mathbf{d} \partial_i
  \,.
$$


By the discussion at [[Poisson Lie algebroid]], the symplectic [[invariant polynomial]] is

$$
  \mathbf{\omega} = \mathbf{d} x^i \wedge \mathbf{d} \partial_i \in W(\mathfrak{P})
  \,.
$$

Clearly it is useful to introduce a new basis of generators with

$$
  \partial^i := -\omega^{i j} \partial_j
  \,.
$$

In this new basis we have a manifest isomorphism

$$
  CE(\mathfrak{P}) = CE(\mathfrak{T}X)
$$

with the [[Chevalley-Eilenberg algebra]] of the [[tangent Lie algebroid]] of $X$. 

Therefore the [[Lie integration]] of $\mathfrak{P}$ is the [[fundamental groupoid]] of $X$, which, since we have assumed global Darboux oordinates and hence [[contractible]] $X$, is just the [[pair groupoid]]:

$$
  \tau_1 \exp(\mathfrak{P}) = \Pi_1(X) = (X \times X \stackrel{\overset{p_2}{\to}}{\underset{p_1}{\to}} X)
  \,.
$$

It remains to show that the symplectic form on $\mathfrak{P}$ makes this a [[symplectic groupoid]].

Notice that in the new basis the invariant polynomial reads

$$
  \begin{aligned}
    \mathbf{\omega} 
      &= 
     - \omega_{i j} \mathbf{d}x^i \wedge \mathbf{d} \partial^j 
     \\
      & = \mathbf{d}( \omega_{i j} \partial^i \wedge \mathbf{d}x^j)
   \end{aligned}
$$

and that we may regard this as a morphism of $L_\infty$-algebroids

$$
  \mathbf{\omega}
   : 
  \mathfrak{T}\mathfrak{P} \to \mathfrak{T}b^3 \mathbb{R}
$$

The corresponding [[infinity-Chern-Weil theory|infinity-Chern-Weil homomorphism]] that we need to compute is given by the [[∞-anafunctor]]

$$
  \array{
    \exp(\mathfrak{P})_{diff}
     &\stackrel{\exp(\mathbf{\omega})}{\to}&
    \exp(b \mathbb{R})_{dR}
    &\stackrel{\int_{\Delta^\bullet}}{\to}&
    \mathbf{\flat}_{dR}\mathbf{B}^3 \mathbb{R} 
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \exp(\mathfrak{P})
  }
  \,.
$$


Over a test space $U$ in degree 1 an element in $\exp(\mathfrak{P})_{diff}$ is a pair
$(X^i, \eta^i)$

$$
  X^i \in C^\infty(U \times \Delta^1)
$$

$$
  \eta^i \in \Omega^1_{vert}(U \times \Delta^1)
$$

subject to the verticality constraint, which says that along $\Delta^1$ we have

$$
  d_{\Delta^1} X^i + \eta^i_{\Delta^1} = 0
  \,.
$$

The vertical morphism $\exp(\mathfrak{P})_{diff} \to \exp(\mathfrak{P})$ has in fact a [[section]] whose image is given by those pairs for which $\eta^i$ has no leg along $U$. We therefore find the desired form on $\exp(\mathfrak{P})$ by evaluating the top morphism on pairs of this form. 

Such a pair is taken by the top morphism to

$$
  \begin{aligned}
    (X^i, \eta^j) 
     & \mapsto 
   \int_{\Delta^1}
    \omega_{i j} F_{X^i} \wedge F_{\partial^j}
   \\
    & =
  \int_{\Delta^1}
    \omega_{i j} (d_{dR} X^i + \eta^i) \wedge d_{dR} \eta^j
  \in 
  \Omega^3(U)
  \end{aligned}
  \,.
$$

Using the above verticality constraint and the condition that $\eta^i$ has no leg along $U$, this becomes

$$
  \cdots = 
  \int_{\Delta^1}
  \omega_{i j}
    d_U X^i 
  \wedge
    d_U d_{\Delta^1} X^j 
  \,.
$$

By the [[Stokes theorem]] the integration over $\Delta^1$ yields

$$
  \cdots 
    =
  \omega_{i j} d_{dR} x^i \wedge \eta^j|_{0}
   -
  \omega_{i j} d_{dR} x^i \wedge \eta^j|_{1}
  \,.
$$

This completes the proof.

### $n = 2$ -- Symplectic 2-groupoids from Courant Lie 2-algebroids

## Geometric quantization of symplectic $\infty$-groupoids
  {#HigherGeometricQuantization}

### Idea
 {#GeometricQuantizationIdea}

The notion of _[[symplectic manifold]]_ formalizes in [[physics]] the concept of a _[[classical mechanical system]]_ . The notion of _[[geometric quantization]]_ of a symplectic manifold is one formalization of the general concept in physics of _[[quantization]]_ of such a system to a _[[quantum mechanical system]]_ . 

Or rather, the notion of [[symplectic manifold]] does not quite capture the most general systems of [[classical mechanics]]. One generalization requires passage to _[[Poisson manifolds]]_ . The original methods of [[geometric quantization]] become meaningless on a Poisson manifold that is not symplectic. 

However, a Poisson structure on a manifold $X$ is equivalent to the structure of a [[Poisson Lie algebroid]] $\mathfrak{P}$ over $X$. This is noteworthy, because the latter _is_ again symplectic, as a [[Lie algebroid]], even if the underlying Poisson manifold is not symplectic: it is a _[[symplectic Lie n-algebroid|symplectic Lie algebroid]]_ . 

Based on related observations it was suggested that the notion of _[[symplectic groupoid]]_ (see the references there) should naturally replace that of _symplectic manifold_ for the purposes of geometric quantization to yield a notion of _[[geometric quantization of symplectic groupoids]]_ . 

Since a symplectic manifold can be regarded as a [[symplectic Lie n-algebroid|symplectic Lie 0-algebroid]] and also as a symplectic [[smooth infinity-groupoid|smooth 0-groupoid]], this step amounts to a kind of [[categorification]] of [[symplectic geometry]]. 

More or less implicitly, there has been strong evidence that this shift in perspective is substantial: the _[[deformation quantization]]_ (see there for references) of a [[Poisson manifold]] turns out to be constructible in terms of [[correlator]]s of the 2-dimensional [[TQFT]] called the _[[Poisson sigma-model]]_ associated with the corresponding [[Poisson Lie algebroid]]. The fact that this is 2-dimensional and not 1-dimensional, as the [[quantum mechanical system]] that it thus encodes, is a direct reflection of this [[categorification]] shift of degree -- see _[[holographic principle]]_ for more on this.

On general abstract grounds this already suggests that it makes sense to pass via [[higher category theory|higher categorification]] further to 
[[Courant Lie 2-algebroid|symplectic Lie 2-algebroid]]s, and generally [[symplectic Lie n-algebroid]]s, as well as to symplectic [[2-groupoid]]s, symplectic [[3-groupoids]], etc. up to symplectic $\infty$-groupoids.

Formal hints for such a generalization had been noted in ([&#352;evera](#Severa)), in particular in its concluding table. More indirect -- but all the more noteworthy -- hints came from [[quantum field theory]], where it was observed that a generalization of symplectic geometry to _[[multisymplectic geometry]]_ of degree $n$ more naturally captures the description of $n$-dimensional [[QFT]] (notice that [[quantum mechanics]] may be understood as $(0+1)$-dimensional QFT). For, observe that the symplectic form on a [[symplectic Lie n-algebroid]] is, while always "binary", nevertheless a representative of [[de Rham cohomology]] in degree $(n+2)$.

There is a natural formalization of these higher symplectic structures in the context of any [[cohesive (∞,1)-topos]]. Moreover, with ([FRS](#FRS)) we may observe that symplectic forms on [[L-∞ algebroid]]s have a natural interpretation in [[∞-Lie theory]]: they are $L_\infty$-[[invariant polynomial]]s. This means that the [[∞-Chern-Weil homomorphism]] applies to them. 

We shall show below that all notions of geometric quantization of symplectic $\infty$-groupoids have a natural interpretation in terms of these canonical structures. For instance the higher "prequantum line bundle" is nothing but the [[circle n-bundle with connection]] that the [[∞-Chern-Weil homomorphism]] assigns to the symplectic form, regarded as an $L_\infty$-[[invariant polynomial]], and the corresponding "[[holographic principle|holographic]]" [[TQFT]] -- the _[[AKSZ sigma-model]]_ -- is that given by the induced [[schreiber:∞-Chern-Simons theory|∞-Chern-Simons functional]].


### Prequantum circle $(n+1)$-bundle 
 {#PrequantumBundles}


#### Idea

What is called _[[geometric quantization|(geometric) prequantization]]_ is a refinement of symplectic 2-forms to [[curvature]] 2-forms on a [[line bundle]] with [[connection on a bundle|connection]]. This is called a choice of _prequantum line bundle_ for the given symplectic form.  

This has an evident generalization to closed forms of degree $(n+2)$. If integral, these may be refined to a [[curvature]] $(n+2)$-form on a _[[circle n-bundle with connection]]_ . Since in the context of [[smooth ∞-groupoid]]s we can have circle $n$-bundles over other smooth $\infty$-groupoids, this means that we canonically have the notion of **prequantum circle $(n+1)$-bundles** on a symplectic $n$-groupoid.

Moreover, since, as discussed above, the symplectic form on a symplectic $n$-groupoid may be regarded as the image of an [[invariant polynomial]] under the unrefined [[∞-Chern-Weil homomorphism]]

$$
  \omega : X \to \mathbf{\flat}_{dR} \mathbf{B}^{n+2}\mathbb{R}
  \,,
$$

the passage to the prequantum $(n+1)$-bundle with connection corresponds to passing to the _refined_ [[∞-Chern-Weil homomorphism]] 

$$
  \hat \omega : X \to \mathbf{B}^{n+1}U(1)_{conn}
$$

(as discussed there).

#### Definition

Let $(X, \omega)$ be a symplectic $\infty$-groupoid. Then $\omega$ represents a class

$$
  [\omega] \in H^{n+2}_{dR}(X)
  \,.
$$

We say this form is _integral_ if it is in the image of the [[curvature]]-projection 

$$
  curv : H^{n+1}_{diff}(X,U(1)) \to H^{n+2}_{dR}(X)
$$

from the [[ordinary differential cohomology]] of $X$.

In this case we say a **prequantum [[circle n-bundle with connection|circle (n+1)-bundle with connection]]** for $(X,\omega)$ is a lift of $\omega$ to $\mathbf{H}_{diff}(X, \mathbf{B}^{n+1}U(1))$.

Write $\hat X \to X$ for the underlying [[circle n-group|circle (n+1)-group]]-[[principal ∞-bundle]].

+-- {: .num_prop}
###### Proposition

If $(X, \omega)$ indeed comes from the [[Lie integration]] of a [[symplectic Lie n-algebroid]] $(\mathfrak{P}, \omega)$ such that the [[period]]s of the [[L-∞ cocycle]] $\pi$ that $\omega$ [[Chern-Simons element|transgresses to]] are integral, then $\hat X$ is the [[Lie integration]] of the [[L-∞ extension]] 

$$
  b^{n}\mathbb{R} \to  \hat \mathfrak{P} \to \mathfrak{P}
$$

classified by $\pi$:

$$
  \hat X \simeq \tau_{n+1} \exp(\hat \mathfrak{P})
  \,.
$$

=--

#### Examples

##### $n= 1$ -- Ordinary prequantum line bundle

See [[geometric quantization of symplectic groupoids]].

##### $n = 2$ -- String Lie 2-algebra

For $\mathfrak{g}$ a [[semisimple Lie algebra]] with  quadratic [[invariant polynomial]] $\omega$, the pair $(b \mathfrak{g}, \omega)$ is a [[symplectic Lie n-algebroid|symplectic Lie 2-algebroid]] ([[Courant Lie 2-algebroid]]) over the point.

In this case the infinitesimal prequantum line 2-bundle is the [[delooping]] of the [[string Lie 2-algebra]]

$$
  \widehat b \mathfrak{g} \simeq b \mathfrak{string}
$$

and the prequantum [[circle n-group|circle 2-group]] [[principal 2-bundle]] is the [[delooping]] of the [[smooth string 2-group]]

$$
  (\hat X \to X) = 
  (\mathbf{B}String \to \mathbf{B}G)
  \,.
$$

## Poisson $L_\infty$-algebras 
 {#HamiltonianVectorFields}

### Idea

A [[Hamiltonian vector field]] on an ordinary [[symplectic manifold]] is a [[vector field]] $v$ whose contraction with the [[symplectic form]] yields an exact form

$$
  \iota_v \omega = d \alpha
  \,.
$$

This definition generalizes verbatim to [[n-plectic geometry]]. 

We observe [below](#OrdinaryHamiltonianVectorFields) that this condition is equivalent to the fact that the [[flow]] $\exp(v) : X \to X$ of $v$ preserves the connection on any [[prequantum line bundle]], up to homotopy (up to [[gauge transformation]]). In this form the definition has an immediate generalization to symplectic $n$-groupoids.

### Definition

+-- {: .num_defn #HamiltonianVectorFieldsOnGrpd}
###### Definition

Let $\omega : X \to \mathbf{\flat}_{dR} \mathbf{B}^{n+2} U(1)$ be a symplectic $(n-1)$-groupoid and let

$$
  \hat \omega
  : 
  X \to  \mathbf{B}^{n+2} U(1)_{conn}
$$

be a [prequantization](#PrequantumBundles) [[circle n-bundle with connection]].

Regard it as an object in the [[over-(∞,1)-topos]] $\mathbf{H}/\mathbf{B}^{n+2}U(1)_{conn}$.

Consider the internal [[automorphism ∞-group]]

$$
  \underline{Aut}_{\mathbf{H}/\mathbf{B}^{n+1}U(1)_{conn}}(X)
  \in \mathbf{H}
$$

of auto-[[equivalence in an (infinity,1)-category|equivalences]] that respect the [[connection on an infinity-bundle|∞-connection]] that refines $\omega$. 

* Its image under $p_! : \mathbf{H}_{/\mathbf{B}^n U(1)_{conn}} \to \mathbf{H}$ we call the **[[Hamiltonian symplectomorphism]] $\infty$-group.

* Its [[∞-Lie algebra]] we call the **[[Poisson algebra|Poisson ∞-Lie algebra]]** of $(X, \omega)$.

=--

### Examples

#### Ordinary Hamiltonian vector fields
 {#OrdinaryHamiltonianVectorFields}

+-- {: .num_prop}
###### Proposition

For $\omega : X \to \mathbf{\flat}_{dR} \mathbf{B}^2 U(1)$ an ordinary [[symplectic manifold]], regarded as a symplectic 0-groupoid, the general definition \ref{HamiltonianVectorFieldsOnGrpd} reproduces the standard notion of [[Hamiltonian vector fields]].

=--

+-- {: .proof}
###### Proof

An Hamiltonian diffeomorphism is given by a diagram

$$
  \array{
     X &&\stackrel{\phi}{\to} && X
     \\
     & {}_{\mathllap{\hat \omega}}\searrow 
     &\swArrow_{\alpha}& 
     \swarrow_{\mathrlap{\hat \omega}}
     \\
     && \mathbf{B} U(1)_{conn}
  }
  \,,
$$

where $\phi$ is an ordinary [[diffeomorphism]]. To compute the Lie algebra of this, we need to consider smooth 1-parameter families of such and differentiate them. 

Assume first that the connection 1-form in $\hat \omega$ is globally defined $A \in \Omega^1(X)$ with $d A = \omega$. Then the above diagram is equivalent to

$$
  (\phi(t)^* A - A) = d \alpha(t)
  \,,
$$

where $\alpha(t) \in C^\infty(X)$. Differentiating this at 0 yields the [[Lie derivative]]

$$
  \mathcal{L}_v A = d \alpha'
  \,,
$$

where $v$ is the [[vector field]] of which $t \mapsto \phi(t)$ is the [[flow]].

By [[Cartan calculus]] this is

$$
  d \iota_v A + \iota_v d_{dR} A  = d \alpha'
$$

hence

$$
  \iota_v \omega = d (\alpha' - \iota_v A)
  \,.
$$

This says that for $v$ to be Hamiltonian, its contraction with $\omega$ must be exact. This is precisely the definition of [[Hamiltonian vector field]]s. The corresponding [[Hamiltonian]] here is $\alpha'-\iota_v A$.

In the general case that the prequantum [[circle n-bundle with connection]] is not trivial, we can present it by a [[Cech cohomology|Cech cocycle]] on the [[Cech nerve]] $C(P_* X \to X)$ of the based [[path space]] [[surjective submersion]] (regarding $P_* X$ as a [[diffeological space]] and choosing one base point per connected component, or else assuming without restriction that $X$ is connected).

Any [[diffeomorphism]] $\phi = \exp(v) : X \to X$ lifts to a diffeomorphism $ P_*\phi : P_* X \to P_* X$ by setting $P_* \phi(\gamma) : (t \in [0,1]) \mapsto \exp(t v)(\gamma(t))$.

So we get a diagram 

$$
  \array{
     C(P_* \to X) &&\stackrel{P_*\phi}{\to} && C(P_* \to X)
     \\
     & {}_{\mathllap{\hat \omega}}\searrow 
     &\swArrow_{\alpha}& 
     \swarrow_{\mathrlap{\hat \omega}}
     \\
     && \mathbf{B} U(1)_{conn}
  }
$$

of [[simplicial presheaves]]. Now the same argument as above applies on $P_* X$.


=--


## Related concepts

* [[higher symplectic geometry]]

  * [[symplectic Lie n-algebroid]] 

  * [[symplectic groupoid]]

* [[higher geometric quantization]]

[[!include infinity-CS theory for binary non-degenerate invariant polynomial - table]]

## References

Some ideas pointing to higher symplectic groupoids were indicated in 

* [[Pavol Ševera]], _Some title containing the words "homotopy" and "symplectic", e.g. this one_ ([arXiv:math/0105080](http://arxiv.org/abs/math/0105080)).
 {#Severa}

Aspects of the relation to [[multisymplectic geometry]] are in

* [[Chris Rogers]], _Higher symplectic geometry_ PhD thesis (2011) ([arXiv:1106.4068](http://arxiv.org/abs/1106.4068))
 {#Rogers}


A discussion of higher symplectic geometry in a general context is in 

* [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:Higher geometric prequantization]]_

See also section 4.3 of 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_ .

Some ingredients for the geometric quantization of symplectic Lie $n$-algebroids are constructed in 

* [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:Higher Chern-Weil Derivation of AKSZ Sigma-Models]]_
  {#FRS}

[[!redirects symplectic ∞-groupoid]]
[[!redirects symplectic ∞-groupoids]]
[[!redirects symplectic infinity-groupoids]]

[[!redirects geometric quantization of symplectic ∞-groupoids]]
[[!redirects geometric quantization of symplectic infinity-groupoids]]

[[!redirects n-plectic ∞-groupoid]]
[[!redirects n-plectic infinity-groupoid]]
[[!redirects n-plectic ∞-groupoids]]
[[!redirects n-plectic infinity-groupoids]]

[[!redirects n-plectic smooth ∞-groupoid]]
[[!redirects n-plectic smooth infinity-groupoid]]
[[!redirects n-plectic smooth ∞-groupoids]]
[[!redirects n-plectic smooth infinity-groupoids]]

