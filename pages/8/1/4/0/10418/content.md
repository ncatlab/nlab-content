
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

Given a [[G-structure]], it is _integrable_ or _locally flat_ if over [[germs]] it restricts to the canonical (trivial) $G$-structure. If it restricts to the canonical structure only over order-$k$ [[infinitesimal disks]], then it is called _order $k$ integrable_. The [[obstruction]] to first-order integrability is the [[torsion of a G-structure]], and hence first-order integrable $G$-structures are also called _torsion-free $G$-structures_.

Beware that some authors use the term "integrable" for "torsion-free". This originates in concentration on the case of [[almost symplectic structure]], i.e. $G$-structure for $G = Sp(2n)$ the [[symplectic group]], in which case the [[Darboux theorem]] gives that first order integrability (to [[symplectic structure]]) already implies full integrability. However, in general this is not the case. For instance for [[orthogonal structure]], i.e. $G$-structure for $G = O(n)$ the [[orthogonal group]], then the [[fundamental theorem of Riemannian geometry]] gives that the torsion obstruction to first-order integrability vanishes, exhibited by the [[Levi-Civita connection]], but full integrability here is equivalent to this being a [[flat connection]], which is a strong additional constraint. This is the case from which the terminology "locally flat" for "integrable" derives from.



## Definition
 {#Definition}

### Traditional
 {#DefinitionTraditional}



Let $V$ be a linear local model space, e.g. a [[vector space]] in plain [[differential geometry]] or [[super vector space]] in [[supergeometry]], etc.. Write $GL(V)$ for its [[general linear group]]. Consider a [[group]] [[homomorphism]] $G \longrightarrow GL(V)$.

Write $\mathbf{c}_0$ for the _standard flat $G$-structure_ on $V$ (see at _[G-Structure -- Examples -- Standard flat G-structure](G-structure#TheStandardFlatGStructure)_).

+-- {: .num_defn}
###### Definition

A [[G-structure]] $\mathbf{c}$ on a [[manifold]] $X$ modeled on $V$ (e.g. a [[smooth manifold]] or [[supermanifold]]) is called integrable if

1. there exists [[cover]] $\{U_i \hookrightarrow X\}$ by [[open subsets]]  $U_i \hookrightarrow V$;

1. such that the $G$-structure $\mathbf{c}$ on $X$ restricts on each patch to the default $G$-structure $\mathbf{c}_0$ on $V$:

   $$
     \mathbf{c}|_{U_i} \simeq \mathbf{c}_0|_{U_i}
     \,.
   $$

=--

This is due to ([Sternberg 64, section VII, def. 2.4](#Sternberg64), [Guillemin 65, section 3](#Guillemin65)).  For review see also ([Alekseevskii](#Alekseevskii), [Lott 90, page 4 of the exposition](#Lott90)).


+-- {: .num_remark}
###### Remark


More concretely, if $G$-structure is modeled by $G$-subbundles $P$ of the [[frame bundle]] (as discussed at _[G-structure -- In terms of subbundles of the frame bundle](G-structure#InTermsOfSubbundlesOfTheFrameBundle)_ ), then it is integrable if each $P \hookrightarrow Fr(X)$ restricts on each patch to $P_0 \hookrightarrow Fr(V)$

$$
  \array{
     P_0|_{U_i} &\hookrightarrow& Fr(V)|_{U_i}
     \\
     {}^{\mathllap{\simeq}}\downarrow && \downarrow
     \\
     P|_{U_i} &\hookrightarrow& Fr(X)|_{U_i}
  }
  \,.
$$

=--

+-- {: .num_defn}
###### Definition

For $k \in \mathbb{N}$, a [[G-structure]] $\mathbf{c}$ on a [[manifold]] $X$ modeled on $V$ (e.g. a [[smooth manifold]] or [[supermanifold]]) is called _order-$k$ infinitesimally integrable_ if at each point $x \in X$ its restriction to the order-$k$ [[infinitesimal neighbourhood]] $\mathbb{D}^V_0 \simeq \mathbb{D}_x^X \hookrightarrow X$ is equal to the default $G$-structure $\mathbf{c}_0$.

=--

([Guillemin 65, section 4](#Guillemin65))

### In higher differential cohesive geometry 
 {#IntermOfDifferentialCohesion}


One may formalize the concept of integrable $G$-structure in the generality of [[higher differential geometry]], formalized in [[differential cohesion]].  See also  there at _[differential cohesion -- G-Structure](differential+cohesive+%28infinity%2C1%29-topos#structures)_.

Let $V$ be framed, def. \ref{Framing}, let $G$ be an [[∞-group]] and $G \to GL(V)$ a homomorphism, hence 

$$
  G\mathbf{Struc}\colon \mathbf{B}G \longrightarrow \mathbf{B}GL(V)
$$

a morphism between the [[deloopings]].

+-- {: .num_defn #GStructure}
###### Definition

For $X$ a $V$-manifold, def. \ref{Manifold}, a **[[G-structure]]** on $X$ is a lift of the structure group of its [[frame bundle]], def. \ref{FrameBundleMap}, to $G$, hence a diagram

$$
  \array{
     X && \longrightarrow&&  \mathbf{B}G
     \\
     & {}_{\mathllap{\tau_X}}\searrow && \swarrow_{\mathrlap{G\mathbf{Struc}}}
     \\
     && \mathbf{B}GL(V)
  }
$$

hence a morphism

$$
  \mathbf{c} \colon \tau_X \longrightarrow G\mathbf{Struc}
$$

is the [[slice (∞,1)-topos]].

=--

In fact $G\mathbf{Struc}\in \mathbf{H}_{/\mathbf{B}GL(n)}$ is the [[moduli ∞-stack]] of such $G$-structures.

The double [[slice (∞,1)-topos|slice]] $(\mathbf{H}_{/\mathbf{B}GL(n)})_{/G\mathbf{Struc}}$ is the [[(∞,1)-category]] of such $G$-structures.

+-- {: .num_example #TrivialGStructure}
###### Example


If $V$ is framed, def. \ref{Framing}, then it carries the trivial $G$-structure, which we denote by

$$
  \mathbf{c}_0 \colon \tau_{V} \longrightarrow G\mathbf{Struc}
  \,.
$$

=--

+-- {: .num_defn #IntegrableGStructure}
###### Definition

For $V$ framed, def. \ref{Framing}, and $X$ a $V$-manifold, def. \ref{Manifold}, then  $G$-structure $\mathbf{c}$ on $X$ is _[[integrability of G-structure|integrable]]_ (or _locally flat_) if there exists a $V$-cover

$$
  \array{
     && U
     \\
     & \swarrow && \searrow
     \\
     V && && X
  }
$$

such that the [[correspondence]] of [[frame bundles]] induced via remark \ref{FrameBundlesFunctorial}

$$
  \array{
     && \tau_U
     \\
     & \swarrow && \searrow
     \\
     \tau_V && && \tau_X
  }
$$

(a diagram in $\mathbf{H}_{/\mathbf{B}GL(V)}$) extends to a sliced correspondence between $\mathbf{c}$ and the trivial $G$-structure $\mathbf{c}_0$ on $V$, example \ref{TrivialGStructure}, hence to a diagram in $\mathbf{H}_{/\mathbf{B}GL(V)}$ of the form

$$
  \array{
     && \tau_U
     \\
     & \swarrow && \searrow
     \\
     \tau_V && \swArrow_{\mathrlap{\simeq}}  && \tau_X
     \\
     & {}_{\mathllap{\mathbf{c}_0}}\searrow && \swarrow_{\mathrlap{\mathbf{c}}}
     \\
     && G\mathbf{Struct}
  }
$$

On the other hand, $\mathbf{c}$ is called _infinitesimally integrable_ (or _torsion-free_) if such an extension exists (only) after restriction to all [[infinitesimal disks]] in $X$ and $U$, hence after composition with the [[counit of a comonad|counit]] 

$$
  \flat^{rel} U \longrightarrow U
$$

of the [[relative flat modality]], def. \ref{InducedRelativeShapeAndFlat}:

$$
  \array{
     && \tau_{\flat^{rel} U}
     \\
     & \swarrow && \searrow
     \\
     \tau_V && \swArrow_{\mathrlap{\simeq}}  && \tau_X
     \\
     & {}_{\mathllap{\mathbf{c}_0}}\searrow && \swarrow_{\mathrlap{\mathbf{c}}}
     \\
     && G\mathbf{Struct}
  }
 \,.
$$


=--

+-- {: .num_remark}
###### Remark

As before, if the given [[reduction modality]] encodes order-$k$ infinitesimals, then the infinitesimal integrability in def. \ref{IntegrableGStructure} is order-$k$ integrability. For $k = 1$ this is [[torsion of a G-structure|torsion-freeness]].

=--




## Properties

### Existence and torsion

The [[obstruction]] for a $G$-structure to be integrable to first order is its [[torsion of a G-structure]].

### In terms of adapted coordinate systems

A $G$-structure on $X$ is integrable previsely if there exists an [[atlas]] of $X$ by [[coordinate charts]] with the property that their canonical [[frame fields]] are $G$-frames.

([Sternberg 64, section VII, exercise 2.1](#Sternberg64))

## Examples
 {#Examples}

* [Complex structure](#ExampleComplexStructure)

* [Symplectic structire](#ExampleSymplecticStructure)

* [Orthogonal structure](#ExamplesOrthogonalStructure)

* [G2-structure](#ExampleG2Structure)

### Complex structure
 {#ExampleComplexStructure}

A $GL(n,\mathbb{C}) \to GL(2n,\mathbb{R})$-[[G-structure|structure]] is an _[[almost complex structure]]_. Its [[torsion of a G-structure]] vanishes precisely if its [[Nijenhuis tensor]] vanishes, hence, by the [[Newlander-Nirenberg theorem]], precisely if it is a [[complex structure]]. Since a [[complex manifold]] admits holomorphic [[coordinate charts]], this first-order integrability already implies full integrability.

### Symplectic structure
 {#ExampleSymplecticStructure}

An $Sp(n) \hookrightarrow GL(2n)$-[[G-structure|structure]] is an _[[almost symplectic structure]]_. Its [[torsion of a G-structure]] is the [[de Rham differential]] $\mathbf{d}\omega$ of the corresponding 2-form $\omega$ (recalled e.g. in [Albuquerque-Picken 11](symplectic+manifold#AlbuquerquePicken11)). Hence first-order integrability here amounts precisely to [[symplectic structure]]. The [[Darboux theorem]] asserts that this is already a fully integrable structure.


### Orthogonal structure
 {#ExamplesOrthogonalStructure}

An $O(n)\to GL(n)$-[[G-structure|structure]] is an [[orthogonal structure]], hence a [[vielbein]], hence a [[Riemannian metric]]. The [[fundamental theorem of Riemannian geometry]] says that in this case the [[torsion of a G-structure]] vanishes, exhibited by the existence of the [[Levi-Civita connection]]. The corresponding first-order integrability is the existence of [[Riemann normal coordinates]] (since these identify the given [[vielbein]] at any point to first order with the trivial (identity) vielbein). The higher order obstructions to integrability turn out to all be proportional to combinations of the [[Riemann curvature]]. Full integrability is equivalent to the vanishing of Riemann tensor, hence to the LC-connection being a [[flat connection]]. 

### Unitary structure
 {#UnitaryStructure}

The case of unitary structure is precisely the combination of the above three cases.

By the fact (see at _[unitary group -- relation to orthogonal, symplectic and general linear group](unitary+group#RelationToOrthogonalSymplecticAndGeneralLinearGroup)_) that the [[unitary group]] is the intersection 

$$
  U(n) \simeq O(2n) \underset{GL(2n,\mathbb{R})}{\times} Sp(2n,\mathbb{R}) \underset{GL(2n,\mathbb{R})}{\times} GL(n,\mathbb{C})
$$ 

a $U(n) \hookrightarrow GL(2n,\mathbb{R})$-structure -- called an _[[almost Hermitian structure]]_ -- is precisely a joint [[orthogonal structure]], [[almost symplectic structure]] and [[almost complex structure]]. Hence if first order integrable -- called a [[Kähler manifold]] structure -- this is precisely a joint [[orthogonal structure]]/[[Riemannian manifold]] structure, [[symplectic manifold]] structure, [[complex manifold]] structure.

### $G_2$-Structure
 {#ExampleG2Structure}

A An $G_2 \to GL(7)$-[[G-structure|structure]] is a [[G2-structure]]. Its [[torsion of a G-structure]] vanishes if the corresponding definite 3-form $\omega$ is [[covariant derivative|covariantly constant]] with respect to the induced [[Riemannian metric]], in which case the structure is a [[G2-manifold]]. Beware that some authors refer to first-order integrable $G_2$-structure (or even weaker conditions) as "integrable $G_2$-structure" (see [Bryant 05, remark 2](G2+manifold#Bryant05) for critical discussion of the terminology). The  [[torsion of a G-structure|higher-order torsion invariants]] of $G_2$-structures do not in general vanish (e.g [Bryant 05, (4.7)](G2+manifold#Bryant05)) and so, contrary to the above cases of symplectic and complex structure, $G_2$-manifold structure does not imply integrable $G_2$-structure.

### Further examples

* [[CR-manifold]]

* [[torsion constraints of supergravity]]

## References

* {#Sternberg64} [[Shlomo Sternberg]], chapter VII of _Lectures on differential geometry_, Prentice-Hall (1964)

* {#Guillemin65} [[Victor Guillemin]], _The integrability problem for $G$-structures_, Trans. Amer. Math. Soc. 116 (1965), 544&#8211;560. ([jstor:1994134](https://www.jstor.org/stable/1994134))

* {#Alekseevskii} D. V: Alekseevskii, _$G$-structure on a manifold_ in M. Hazewinkel (ed.) _Encyclopedia of Mathematics, Volume 4_ ([eom:G-structure](https://encyclopediaofmath.org/wiki/G-structure))

Lecture notes include

* [[Marius Crainic]], _[Differential geometry course](https://webspace.science.uu.nl/~crain101/DG-2015/)_, 2015 ([pdf](https://webspace.science.uu.nl/~crain101/DG-2015/main10.pdf), [[CrainicDifferentialGeometry15.pdf:file]])

* {#Pasquotto} [[Federica Pasquotto]], _Linear $G$-structures by examples_ ([pdf](http://www.few.vu.nl/~pasquott/course16.pdf), [[PasquottoGStructures.pdf:file]])


Discussion with an eye towards [[torsion constraints in supergravity]] is in

* {#Lott90} [[John Lott]], _The Geometry of Supergravity Torsion Constraints_, Comm. Math. Phys. 133 (1990), 563&#8211;615, (exposition in [arXiv:0108125](http://arxiv.org/abs/math/0108125))

Discussion with an eye towards [[special holonomy]] is in

* {#Joyce00} [[Dominic Joyce]], _Compact manifolds with special holonomy_, Oxford University Press 2000

Discussion in [[modal homotopy type theory]]:

* {#Wellen17} [[Felix Wellen]], _[[schreiber:thesis Wellen|Formalizing Cartan Geometry in Modal Homotopy Type Theory]]_, 2017

* {#Wellen18} [[Felix Cherubini]] (née Wellen), _Cartan Geometry in Modal Homotopy Type Theory_ ([arXiv:1806.05966](https://arxiv.org/abs/1806.05966))



See also the references at _[[torsion of a Cartan connection]]_ and at _[[torsion constraints in supergravity]]_.

[[!redirects integrability of G-structure]]
[[!redirects integrability of G-structures]]

[[!redirects integrable G-structure]]
[[!redirects integrable G-structures]]

[[!redirects integrable G-stucture]]
[[!redirects integrable G-stuctures]]

[[!redirects first-order integrable G-structure]]
[[!redirects first-order integrable G-structures]]
