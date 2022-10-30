
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Geometric quantization
+--{: .hide}
[[!include geometric quantization - contents]]
=--
=--
=--

> under construction

#Contents#
* table of contents
{:toc}

## Idea

Traditional [[prequantum geometry]] is the [[differential geometry]] of [[smooth manifolds]] which are equipped with a _[[twisted cohomology|twist]]_   in the form of a [[circle group]]-[[principal bundle]] and a circle-[[principal connection]].
In the context of _[[geometric quantization]]_ of [[symplectic manifolds]] these arise as _[[prequantum bundles]]_. Equivalently, prequantum geometry is the _[[contact geometry]]_ of the  total spaces of these bundles, equipped with their [[Ehresmann connection]] [[differential 1-form]] and  thought of as _[[regular contact manifolds]]_.  Prequantum geometry notably studies the [[automorphisms]] of [[prequantum bundles]] covering [[diffeomorphisms]] of the base
-- the _[[prequantum operators]]_ or _[[contactomorphisms]]_ -- and the [[action]] of these on the space of [[sections]] of the [[associated bundle|associated]] [[line bundle]] -- the _[[prequantum states]]_. This is an intermediate step in the genuine _[[geometric quantization]]_ of the [[curvature]] [[differential 2-form]] of these bundles,
which is obtained by "dividing the above data in half" ([[polarization]]), important for instance in the the _[[orbit method]]_.

But prequantum geometry is of interest in its own right. 
For instance the above automorphism group naturally provides the 
[[Lie integration]] of the [[Poisson bracket]] [[Lie algebra]] of the underlying [[symplectic manifold]], together with the canonical
injection into the [[group of bisections]] of the [[Lie integration]] of the  _[[Atiyah Lie algebroid]]_ which is associated with the given circle bundle, all of which are fundamental objects of interest in the study of [[line bundles]] over [[manifolds]].

For a plethora of applications in [[differential geometry]], one wants to generalize this to _[[higher differential geometry]]_ (see at _[[motivation for higher differential geometry]]_) and accordingly study _higher prequantum geometry_.


## Motivation and survey of results

### Ordinary prequantum geometry in terms of automorphisms in slices
 {#OrdinaryPrequantumGeometryInTermsofAutomorphismsInSlices}

A sequence of time-honored  traditional concepts in [[geometric quantization]]/[[prequantum geometry]] is

| [[Lie groups]]: | [[Heisenberg group]] | $\hookrightarrow$ | [[quantomorphism group]] | $\hookrightarrow$ |   [[gauge group]]  | 
|--|--|--|--|--|--|
| [[Lie algebras]]: | [[Heisenberg Lie algebra]] | $\hookrightarrow$ | [[Poisson Lie algebra]] | $\hookrightarrow$ | twisted [[vector fields]] |

For instance in the [[geometric quantization]] of the [[electromagnetic field|electrically]] [[charged particle|charged]] [[particle]] [[sigma-model]] we have a [[prequantum circle bundle]] $P$ with [[connection on a bundle]] $\nabla$ on a [[cotangent bundle]] $X = T^* Y$ which is essentially the [[pullback]] of the [[electromagnetic field]]-bundle on [[target space|target]] [[spacetime]] $Y$. Its _[[quantomorphism group]]_ is the group of [[diffeomorphisms]] $P \stackrel{\simeq}{\to} P$ of the total space of the prequantum bundle which preserve the connection (also called the _[[contactomorphism]]_ of $(P,\nabla)$ regarded as a [[regular contact manifold]]). For the following it is convenient to say this using the language of _[[moduli stacks]]_: we may regard $X$ as a [[representable functor|representable]] [[sheaf]] on the [[site]] of [[smooth manifolds]] (a "[[smooth space]]") and then moreover as a [[representable functor|representable]] [[stack]] on this site (a "[[smooth groupoid]]") and make use of the tautological existence of the [[moduli stack]] of $U(1)$-[[principal connections]], which we write $\mathbf{B}U(1)_{conn}$ (we don't need further details right now, but they can be found for instance at _[[circle n-bundle with connection]]_ for details). By definition this is such that for any $X$ a map $\nabla \colon X \to \mathbf{B}U(1)_{conn}$ is equivalently a $U(1)$-[[principal connection]] and such that a [[homotopy]] $\eta \colon \nabla_1 \to \nabla_2$ between two such maps is equivalently a [[gauge transformation]] between two such connections. With this formulation a [[quantomorphism]] of the [[prequantum bundle]] $\nabla$ is equivalently a diagram of the form as on the right of

$$
  \mathbf{QuantMorph}(\nabla)
  =
  \left\{
  \array{
    X &&\underoverset{\simeq}{\phi}{\to}&& X
    \\
    & \searrow &\swArrow_{\eta}& \swarrow
    \\
    && \mathbf{B}U(1)_{conn}
  }
  \right\}
$$

in the [[(2,1)-category]] of [[stacks]], namely a [[diffeomorphism]] $\phi \colon X \stackrel{\simeq}{\to} X$ of the base space of the bundle together with a [[gauge transformation]] of $U(1)$-[[principal connections]] $\eta \colon \phi^* \nabla \stackrel{\simeq}{\to} \nabla$.

The [[quantomorphism group]] is naturally an ([[infinite-dimensional Lie group|infinite dimensional]]) [[Lie group]]. Its [[Lie algebra]] is the [[Poisson bracket]] [[Lie algebra]]. If $X$ is equipped with the structure of a [[Lie group]] itself (notably if it is a [[vector space]]), then the sub-Lie algebra of that on the [[invariant differential form|invariant vectors]] is the [[Heisenberg Lie algebra]] and the Lie group corresponding to that is the [[Heisenberg group]].
 
One also says that a triangular diagram as above is an autoequivalence of the "modulating" map $\nabla \colon X \to \mathbf{B}U(1)_{conn}$ in the _[[slice (infinity,1)-category|slice (2,1)-category]]_ of [[stacks]]/[[smooth groupoids]] over $\mathbf{B}U(1)_{conn}$. 

Such autoequivalences in slices are familiar from basic concepts of [[Lie groupoid]] theory. For $\mathcal{G} = (\mathcal{G}_1 \stackrel{\to}{\to} \mathcal{G}_0)$ a [[Lie groupoid]], we may regard the inclusion of its manifold of objects as an [[atlas]] being a map $p_\mathcal{G} \colon\mathcal{G}_0 \to \mathcal{G}$. Regarding this atlas as an object in the [[slice (infinity,1)-category|slice (2,1)-category]] of [[stacks]]/[[smooth groupoids]] over $\mathcal{G}$, its autoequivalences are diagrams as on the right of

$$
  \mathbf{BiSect}(p_{\mathcal{G}})
  =
  \left\{
    \array{
      \mathcal{G}_0 &&\stackrel{\phi}{\to}&& \mathcal{G}_0
      \\
      & \searrow &\swArrow_\eta & \swarrow
      \\
      && \mathcal{G}
    }
  \right\}
  \,.
$$

This is a [[diffeomorphism]] $\phi \colon \mathcal{G}_0 \stackrel{\simeq}{\to} \mathcal{G}_0$ of the [[smooth manifold]] of [[objects]] equipped with a [[natural transformation]] $\eta$ whose component map is a [[smooth function]] that assigns to each point $q\in\mathcal{G}_0$ a [[morphism]] in $\mathcal{G}$ of the form $\eta_q \colon q \to \phi(q)$. This collection of data is known as a _[[bisection]]_ of a [[Lie groupoid]]. Bisections naturally form a group $\mathbf{BiSect}(p_{\mathcal{G}})$ , which is all the more manifest if we understand them as autoequivalences of the atlas in the slice, called the [[group of bisections]].

This perspective of regarding maps of [[smooth groupoids]] as objects in the slice over their codomain (an elementary step in [[higher category theory]]/[[(infinity,1)-topos theory|higher topos theory]], but not common in traditional differential geometry) turns out to be useful and drives all of the refinements, generalizations and theorems that we discuss in the following: we will see that higher [[prequantum geometry]] is essentially the geometry insice [[slice (infinity,1)-topos|higher slice categories]] of [[infinity-stack|higher stacks]] over [[moduli infinity-stack|higher moduli stacks]] of [[principal infinity-connection|higher principal connections]].

Before we get there, notice the following...

### The need for higher prequantum bundles
 {#TheNeedForHigherPrequantumBundles}

The tools of [[geometric quantization]] mainly apply to [[quantum mechanics]] and only partially to [[quantum field theory]]. In particular in the context of _[[extended prequantum field theory]]_ in [[dimension]] $n$ a [[prequantum bundle]] over the ([[phase space|phase]]-)space of [[field (physics)|fields]] is to be refined (de-[[transgression|transgressed]]) to a _[[prequantum n-bundle]]_ over the [[moduli ∞-stack]] of [[field (physics)|fields]]. Therefore in order to apply [[geometric quantization]] to [[extended prequantum field theory]] to obtain [[extended quantum field theory]] we first need extended/higher prequantum geometry.

For instance the [[prequantum n-bundle|prequantum 3-bundle]] for standard [[3d Chern-Simons theory|3d]] [[Spin group]] [[Chern-Simons theory]] is modulated by the differential [[smooth first fractional Pontryagin class]]

$$
  \array{
    \mathbf{B}Spin_{conn} 
     &\stackrel{\tfrac{1}{2}\hat \mathbf{p}_1}{\to}&
    \mathbf{B}^3 U(1)_{conn}
    \\
    \downarrow && \downarrow & forget \; connections
    \\
    \mathbf{B}Spin 
     &\stackrel{\tfrac{1}{2}\mathbf{p}_1}{\to}&
    \mathbf{B}^3 U(1)
    \\
    \downarrow && \downarrow & geometric\;realization
    \\
    B Spin &\stackrel{\tfrac{1}{2}p_1}{\to}& K(\mathbb{Z},4)    
  }
  \,,
$$

modulating/classifying the universal _[[Chern-Simons circle 3-bundle with connection]]_ (also known as a _[[bundle 2-gerbe]]_) over the [[moduli stack]] of [[field (physics)|fields]] of $G$-Chern-Simons theory, which is the moduli stack $\mathbf{B}G_{conn}$ of $G$-[[principal connection]].

Similarly the [[prequantum n-bundle|prequantum 7-bundle]] for [[7d Chern-Simons theory]] on [[string 2-group]] [[principal infinity-connections|principal 2-connections]] is given by the differential [[smooth second fractional Pontryagin class]]

$$
  \array{
    \mathbf{B}String_{conn} 
     &\stackrel{\frac{1}{6}\hat \mathbf{p}_2}{\to}&
    \mathbf{B}^7 U(1)_{conn}
    \\
    \downarrow && \downarrow & forget\; connections
    \\
    \mathbf{B}String 
     &\stackrel{\frac{1}{6}\mathbf{p}_2}{\to}&
    \mathbf{B}^7 U(1)
    \\
    \downarrow && \downarrow & geometric\; realization
    \\
    B String &\stackrel{\frac{1}{6}p_2}{\to}& K(\mathbb{Z},8)
  }
  \,,
$$

modulating/classifying the universal _[[Chern-Simons circle 7-bundle with connection]]_ over the moduli 2-stack $\mathbf{B}String_{conn}$ of [[string 2-group]] [[principal infinity-connection|principal 2-connections]].



Therefore we want to lift the [above](#OrdinaryPrequantumGeometryInTermsofAutomorphismsInSlices) table of traditional notions to [[higher geometry]]...

### Brief recollection: Higher geometry

In order to say this, clearly we need some basics of [[higher geometry]]...

$$
  \array{
     && Groupoids
     \\
     & \swarrow && \searrow^{\mathrlap{nerve}}
     \\
     Categories && &&  Kan complexes
     \\
     & \searrow && \swarrow
     \\
     && (\infty,1)-Categories
  }
  \,.
$$

Important construction principle for [[(∞,1)-categories]]: [[simplicial localization]]. For $\mathcal{C}$ a [[category]] with some subset of morphisms $W \hookrightarrow Mor(\mathcal{C})$ declared to be "[[weak equivalences]]", the [[simplicial localization]] 

$$
  L_W \mathcal{C} \in (\infty,1)Cat
$$

is the [[universal construction|universal]] $(\infty,1)$-category obtained from $\mathcal{C}$ by universally turning each weak equivalence into an actual [[homotopy equivalence]] in the sense of [[homotopy theory]].

In particular let $C$ be a [[site]], assumed for simplicity to have [[point of a topos|enough points]]. Declare then that in the [[functor category]] $Func(C^{op}, KanCplx)$, hence in [[Kan complex]]-valued presheaves, the weak equivalences are the [[stalk|stalkwise]] [[homotopy equivalences]] of Kan complexes. Then

$$
  \mathbf{H} \coloneqq Sh_{\infty}(C) \coloneqq L_{W} Func(C^{op}, KanCplx)
$$

is called the _[[(∞,1)-topos]]_ of [[(∞,1)-sheaves]]/[[∞-stacks]] on $C$.

An [[A-∞ algebra]]-object $G$ in such an $(\infty,1)$-topos such that $\pi_0(G)$ is a [[group]] is called an [[∞-group]] "with geometric structure as encoded by the test spaces $C$". The canonical source of $\infty$-groups are the [[homotopy fiber products]] of point inclusions $* \to X$ of any object X, the [[loop space object]]

$$
  \Omega X \coloneqq {*} \underset{X}{\times} {*}
  \,.
$$

In fact this are _all_ the [[∞-groups]] that there are, up to equivalence: forimg [[loop space objects]] is an [[equivalence of (∞,1)-categories]]

$$
  Grp(\mathbf{H})
   \stackrel{\overset{\Omega}{\leftarrow}}{\underoverset{\mathbf{B}}{\simeq}{\to}}
  \mathbf{H}^{*/}_{\geq 1}
$$

between [[∞-groups]] and [[pointed object|pointed]] [[connected object in an (∞,1)-topos|connected]] objects. The inverse equivalence $\mathbf{B}$ is the _[[delooping]]_ operation.

We say that such an $(\infty,1)$-topos $\mathbf{H}$ is _[[cohesive]]_ if it is equipped with an [[adjoint triple]] of [[idempotent monad|idempotent]] (co)/[[(∞,1)-monads]]

| [[shape modality]] | | [[flat modality]] | | [[sharp modality]]  |
|--|--|--|--|--
| idemp. monad | | idemp. comonad | | idemp. monad |
| $\Pi$ | $\dashv$ | $\flat$ | $\dashv$ | $\sharp$ |

This implies (strictly speaking we need [[differential cohesion]] for that, coming from another adjoint triple of (co)monads) that for every [[braided ∞-group]] $\mathbb{G} \in Grp(\mathbf{H})$ there is a canonical object $\mathbf{B}\mathbb{G}_{conn}$ which modulats $\mathbb{G}$-[[principal ∞-connections]].



### Higher Atiyah groupoids

Looking at the [above](#OrdinaryPrequantumGeometryInTermsofAutomorphismsInSlices) table and noticing the [above](#TheNeedForHigherPrequantumBundles) need for higher prequantum bundles, we should try to find an analogous table of concepts in [[higher geometry]], something like this:

[[!include slice automorphism groups in higher prequantum geometry - table]]


(...)

The way all these notions and theorems work is by considering [[automorphism ∞-groups]] of the classifying (or rather: modulating) maps $\nabla \colon X \to \mathbf{B}\mathbb{G}_{conn}$ of a [[prequantum ∞-bundle]] in the [[slice (∞,1)-topos]] over the domain. For instance

$$
  \mathbf{QuantMorph}(\nabla)  
  =
  \left\{
    \array{
      X && \underoverset{\simeq}{\phi}{\to} && X
      \\
      & {}_{\mathllap{\nabla}}\searrow &\swArrow& \swarrow_{\mathrlap{\nabla}}
      \\
      && \mathbf{B}\mathbb{G}_{conn} 
    }
  \right\}
  \,.
$$

The others are obtained by succesively forgetting connection data. For instance

$$
  \BiSect(Cou(\nabla))  
  =
  \left\{
    \array{
      X && \underoverset{\simeq}{\phi}{\to} && X
      \\
      & {}_{\mathllap{\nabla_1}}\searrow &\swArrow& \swarrow_{\mathrlap{\nabla_1}}
      \\
      && \mathbf{B}(\mathbf{B}\mathbb{G}_{conn})
     }
   \right\}
   \,.
$$

and

$$
  \BiSect(At(\nabla))  
  =
  \left\{
    \array{
      X && \underoverset{\simeq}{\phi}{\to} && X
      \\
      & {}_{\mathllap{\nabla_0}}\searrow &\swArrow& \swarrow_{\mathrlap{\nabla_0}}
      \\
      && \mathbf{B}\mathbb{G}
    }
  \right\}
  \,.
$$

The extension sequence is then schematically simply the following

$$
  \left\{
    \array{
      && X
      \\
      & \swarrow &  & \searrow
      \\
      & \searrow &\swArrow& \swarrow
      \\
      && \mathbf{B}\mathbb{G}_{conn} 
    }
  \right\}
  \; \to \;
  \left\{
    \array{
      X &&\stackrel{\simeq}{\to}&& X
      \\
      & {}_{\mathllap{\nabla}}\searrow &\swArrow& \swarrow_{\mathrlap{\nabla}}
      \\
      && \mathbf{B}\mathbb{G}_{conn}
    }
  \right\}
  \;
  \to
  \;
  \left\{
    \array{
      X && \stackrel{\simeq}{\to} && X
    }
  \right\}
$$

in this generality this now includes various other notions, too:

[[!include higher Atiyah groupoid - table]]



### The central theorem: Quantomorphism $\infty$-group extensions

+-- {: .num_theorem }
###### Theorem

For $\mathbb{G}$ a [[braided ∞-group]] and $\nabla \colon X \to \mathbf{B}\mathbb{G}_{conn}$ a higher prequantum geometry with respect to $\mathbb{G}$ there is a long [[homotopy fiber sequence]]

$$
  \left(\Omega \mathbb{G}\right)\mathbf{FlatConn}\left(\nabla\right)
  \to
  \mathbf{QuantMorph}(\nabla)
  \to 
  \mathbf{HamSympl}(\nabla)
  \stackrel{\nabla \circ (-)}{\to}
  \mathbf{B}\left(\left(\Omega \mathbb{G}\right)\mathbf{FlatConn}\left(\nabla\right) \right) 
  \,.
$$

Similarly there is the [[Heisenberg infinity-group]] extension

$$
  (\Omega \mathbb{G})\mathbf{FlatConn}(X)
   \to
  \mathbf{Heis}(\nabla)
   \to 
  G
$$

=--

+-- {: .num_theorem }
###### Theorem

The [[Lie differentiation]] of the [[∞-group extension]] sequence of prop. \ref{QuantomorphismExtension} is a [[homotopy fiber sequence]] of [[L-∞ algebras]] 

$$
  \mathbf{H}(X, \flat \mathbf{B}^{n-1}\mathbb{R})
  \to
  \mathfrak{Poisson}(X,\omega) \to \mathcal{X}_{Ham}(X,\omega)
  \stackrel{\iota_{(-)\omega}}{\to}
  \mathbf{B}\mathbf{H}(X, \flat \mathbf{B}^{n-1}\mathbb{R})
  \,,
$$

where

* $\mathfrak{Poisson}(X,\omega)$ is the [[Poisson Lie n-algebra]] as defined in ([Rogers 11](#Rogers11)).

* $\mathcal{X}_{Ham}$ is the Lie algebra of [[vector fields]] restricted to the [[Hamiltonian vector fields]];

* $\mathbf{H}(X, \flat (\mathbf{B}^{n-1})\mathbb{R})$ is the [[chain complex]] for flat [[de Rham cohomology]] in the given degree, regarded as an abelian [[L-∞ algebra]].

=--



The following table shows what this sequence reduces to when one chooses $\mathbb{G} = \mathbf{B}^{n-1}U(1)$.

[[!include geometric quantization extensions - table]]

### Examples: $String$ and $Fivebrane$ as Heisenberg $\infty$-groups

+-- {: .num_example }
###### Example

For $G$ a simply connected semisimple compact Lie group such as the [[spin group]], let 

$$
  \nabla \coloneqq
   \exp\left(2 \pi i \int_{S^1} [S^1, \tfrac{1}{2}\hat \mathbf{p}_1]\right)
  \;\colon\; G \to \mathbf{B}^2 U(1)_{conn}
$$ 

be the canonical [[circle 2-bundle with connection]] over it. Then the [[Heisenberg infinity-group|Heisenberg 2-group]] [[infinity-group extension|extension]]

$$
  U(1)\mathbf{FlatConn}(G)
   \to
  \mathbf{Heis}(\nabla)
   \to
  G
$$

is the [[string 2-group]] extension

$$
  \mathbf{B}U(1) \to String(G) \to G
  \,.
$$

=--

(by classification of extensions by cohomology... by Lie 2-algebra computation...)

(and analogously for [[fivebrane 6-group]]...)

$$
 \mathbf{B}^6 U\left(1\right) 
   \to 
  \mathbf{Heis}\left(\exp\left(2 \pi i \int_{S^1} \left[S^1, \tfrac{1}{2}\hat \mathbf{p}_2\right] \right)\right) \to String
$$


## Constructions in higher prequantum geometry

[[!include slice automorphism groups in higher prequantum geometry - table]]

[[!include higher Atiyah groupoid - table]]

[[!include geometric quantization extensions - table]]

## Related entries

* [[Poisson bracket Lie n-algebra]]

* [[definite parameterization of WZW terms]]

* [[definite globalization of WZW terms]]

## References

See also the references at _[[n-plectic geometry]]_ and at _[[higher geometric quantization]]_

* {#FRS13a} [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:Higher geometric prequantum theory|Higher $U(1)$-gerbe connections in geometric prequantization]]_, Rev. Math. Phys., Vol. 28, Issue 06, 1650012 (2016) ([arXiv:1304.0236](http://arxiv.org/abs/1304.0236))

* {#FRS13b} [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:L-∞ algebras of local observables from higher prequantum bundles]]_, Homology, Homotopy and Applications, Volume 16 (2014) Number 2, p. 107 &#8211; 142 ([arXiv:1304.6292](http://arxiv.org/abs/1304.6292))

* {#Schreiber13} [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_ ([arXiv:1310.7930](http://arxiv.org/abs/1310.7930))



[[!redirects higher prequantization]]
[[!redirects higher prequantizations]]

[[!redirects higher pre-quantization]]
[[!redirects higher pre-quantizations]]
