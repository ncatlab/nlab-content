
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

### Traditional definition

A [[submanifold]] of a [[symplectic manifold]] each [[tangent space]] of which is an [[isotropic subspace]] with respect to the ambient symplectic structure is an **isotropic submanifold**.

### In cohesive higher geometry

The following is a suggestion for an axiomatization of ([[foliations]] by) isotropic subspaces in the context [[differential cohesion]], followed by some considerations showing how these axioms reproduce traditional theory. 

> Under construction.

So let $\mathbf{H}$ be a [[cohesive (∞,1)-topos]] equipped with [[differential cohesion]].

As usual, we write $(\int \dashv \flat \dashv \sharp)$ for the [[adjoint triple]] of [[modalities]] that defines the [[cohesion]] ([[shape modality]] $\dashv$ [[flat modality]] $\dashv$ [[sharp modality]]) and we write $(Red \dashv \int_{inf} \dashv \flat_{inf})$ for the adjoint triple of of modalities that defines the [[differential cohesion]] ([[reduction modality]] $\dashv$ [[infinitesimal shape modality]] $\dashv$ [[infinitesimal flat modality]]). 

Below we are going to axiomatize aspects of the traditional description of [[foliations]] by [[Lie groupoids]]/[[foliation groupoids]], so we start by briefly setting up some terminology on groupoids in differential cohesion.

If we think of a [[1-epimorphism]] $\mathcal{G}_0 \to \mathcal{G}$ in $\mathbf{H}$ as the [[atlas]] on the cohesive $\infty$-groupoid $\mathcal{G} \in \mathbf{H}$, hence, by the [[Giraud-Rezk-Lurie axioms]], equivalently as a [[groupoid object in an (infinity,1)-category|groupoid object]] $\mathcal{G}_\bullet = \mathcal{G}_0^{\times^{\bullet+1}_{\mathcal{G}}}$, then we have the following "geometricity" constraints on groupoid objects

+-- {: .num_defn #GeometricAndEtale}
###### Definition

For $f \colon X \to Y$ any morphism in $\mathbf{H}$, write 

$$
  X \stackrel{L(f)}{\to} Y \underset{\int_{inf} Y}{\times} \int_{inf} X
$$

for the canonical morphism induced by the [[natural transformation|naturality]] of the $\int_{inf}$-[[unit of an adjunction|unit]]. We say that

1. $f$ is a **[[formally smooth morphism]]** (or _[[submersion]]_) if $L(f)$ is a [[1-epimorphism]]

1. $f$ is a **[[formally étale morphism]]** (or _[[local diffeomorphism]]_) if $L(f)$ is an [[equivalence in an (infinity,1)-category|equivalence]].

Moreover, if $\pi \colon \mathcal{G}_0 \to \mathcal{G}$ is a [[1-epimorphism]], hence an [[atlas]] for the cohesive $\infty$-groupoid $\mathcal{G}$, then we say about the corresponding [[groupoid object in an (infinity,1)-category|groupoid object]] that

1. $\mathcal{G}_\bullet$ is an **[[geometric ∞-groupoid]]** if its [[atlas]] $\pi$ is a [[formally smooth morphism]]/[[submersion]].

1. $\mathcal{G}_\bullet$ is an **[[étale ∞-groupoid]]** if its [[atlas]] $\pi$ is a [[formally étale morphism]]/[[local diffeomorphism]].

=--

+-- {: .num_defn #FoliationInDifferentialCohesion}
###### Definition

For $X \in \mathbf{H}$, a **[[foliation]]** of $X$ is 
a morphism $\mathcal{D} \colon X \to X//\mathcal{D}$ in $\mathbf{H}$ which is 

1. a [[1-epimorphism]];

1. a [[formally smooth morphism]].

Equivalently a foliation of $X$ is a map that exhibits $X$ as an [[atlas]]
for a [[geometric ∞-groupoid]], def. \ref{GeometricAndEtale}.

Given a foliation $\mathcal{D}$ on $X$ we say that the **leaf decomposition** of $X$ induced by the foliation is the [[(∞,1)-pullback]] 

$$
  LeafDec(\mathcal{D})
  \coloneqq
  \flat(X//\mathcal{D}) \underset{X//\mathcal{D}}{\times} X
$$ 

in 

$$
  \array{
    LeafDec(\mathcal{D}) &\stackrel{\iota_{\mathcal{D}}}{\to}& X
    \\
    \downarrow && \downarrow^{\mathrlap{\mathcal{D}}}
    \\
    \flat (X//\mathcal{D}) &\to& X//\mathcal{D}
  }
  \,,
$$

where the bottom map is the [[counit of an adjunction|counit]] of the [[flat modality]].

=--


Now let $\mathbb{G} \in Grp_2(\mathbf{H})$ a [[braided ∞-group]]. Write

$$
  \Omega^2_{cl} := \Omega^2_{flat}(-,\mathbb{G})
$$ 

for the corresponding coefficient object for [[curvature]] forms of $\mathbb{G}$-[[principal ∞-connections]] (as discussed there).

+-- {: .num_defn #IsotropicFoliationsInDiffCohe}
###### Definition

Given a closed 2-form 

$$
  \omega \;\colon\; X \to \Omega^2_{cl}
$$

a foliation of $X$ by **$\omega$-isotropic subspaces** is a [[foliation]] $\mathcal{D} \colon X \to X//\mathcal{D}$
as in def. \ref{FoliationInDifferentialCohesion} such that the restriction of $\omega$ to the leaf decomposition is equivalent to the 0-form

$$
  \iota_{\mathcal{D}}^* \omega \simeq 0
  \,,
$$

hence such that the top composite morphism in the diagram

$$
  \array{
    (\flat \mathcal{E}) \underset{\mathcal{E}}{\times} X
    &\to& X &\stackrel{\omega}{\to}& \Omega^2_{cl}
    \\
    \downarrow && \downarrow
    \\
    \flat (X//\mathcal{D}) &\to& X//\mathcal{D}
  }
$$

factors through the point.

=-- 

We now discuss how low-degree examples of this axiomatics interpreted in $\mathbf{H} \coloneqq $ [[SynthDiff∞Grpd]] reproduces the traditional notions of [[foliations]] and isotropic submanifolds of [[pre-symplectic manifolds]].

In the following we regard [[smooth manifolds]] canonically under the embedding

[[SmoothMfd]] $\hookrightarrow $ [[Smooth∞Grpd]] $\stackrel{i_!}{\hookrightarrow}$ [[SynthDiff∞Grpd]] $= \mathbf{H}$ 

as [[reduced object|reduced]] [[synthetic differential ∞-groupoids]].

+-- {: .num_example #TraditionalSubmersions}
###### Example

A [[smooth function]] $f \colon X \to Y$ between [[smooth manifolds]] is

1. a [[local diffeomorphism]] in the traditional sense precisely if it is a [[formally étale morphism]] in the sense of def. \ref{GeometricAndEtale};

1. a [[submersion]] in the traditional sense precisely if it is a [[formally smooth morphism]] in the sense of def. \ref{GeometricAndEtale}.

=--

This is discussed at _[[SynthDiff∞Grpd]]_. The idea of the proof is to use the [[∞-cohesive site]] of definition [[CartSp]]${}_{synthdiff}$ and evaluate the [[homotopy pullback]] in def. \ref{GeometricAndEtale} first on all representables of the form $U \times D_1$ where $U$ ranges over [[Cartesian spaces]] and where $D_1$ is the first order ininfitesimal neighbourhood of the origin on $\mathbb{R}^1$ (whose [[smooth algebra]] of fucntions is the [[ring of dual numbers]]). Then the homotopy pullback is represented as an ordinary pullback of sheaves over Cartesian spaces and the naturality diagram in question is the diagram of [[tangent bundles]]

$$
  \array{
    T X &\stackrel{d f}{\to}& T Y
    \\
    \downarrow && \downarrow
    \\
    X &\stackrel{f}{\to}& Y
  }
  \,.
$$

With this now the claim is reduced to the traditional characterization of [[submersions]] and [[local diffeomorphisms]].

+-- {: .num_example #LieAndEtaleGroupoids}
###### Example

Let $\mathcal{G}$ be a [[smooth groupoid]] which has a presentation by a [[simplicial presheaf]] $\mathcal{G}_\bullet$ with values in 2-coskeletak Kan complexes where objects and morphisms are represented by a [[smooth manifold]] each, and consider it equipped with the induced [[atlas]] $\mathcal{G}_0 \to \mathcal{G}$. Then

* if the presentation $\mathcal{G}_\bullet$ is a [[Lie groupoid]] then $\mathcal{G}_0 \to \mathcal{G}$ is a [[geometric ∞-groupoid]] 

* if the presentation $\mathcal{G}_\bullet$ is an [[étale groupoid]] then $\mathcal{G}_0 \to \mathcal{G}$ is an [[étale ∞-groupoid]]

in the sense of def. \ref{GeometricAndEtale}.

=--

This follows by the corresponding discussion at [[SynthDiff∞Grpd]]. The idea of the proof is that one presents the atlas in the projective [[model structure on simplicial presheaves]] by the [[décalage]] [[fibration]] [[resolution]], schematically

$$
  \array{
    && g
    \\
    & \swarrow && \searrow & &&& \mathcal{G}_0
    \\
    g_1 &&\to&& g_2
    \\
    \\
    &&&& &&&&&& \downarrow
    \\
    \\
    g_1 &&\to&& g_2 &&&&&& \mathcal{G}    
  }
  \,.
$$

Then the [[homotopy pullback]] $\mathcal{G} \underset{\int_{inf}\mathcal{G}} {\times}\int_{inf} X $ is presented by an ordinary pullback and so 
example \ref{TraditionalSubmersions} applies degreewise. In degree 0 the above resolution is the target map in the groupoid $\mathcal{G}$ and so by example \ref{TraditionalSubmersions} this is a [[submersion]] or [[local diffeomorphism]], respectively, as claimed.


+-- {: .num_example }
###### Example

Let $X$ be a smooth manifold and  let $\mathcal{D}$ be a traditional [[foliation]] on $X$ which is _simple_ in that the [[leaf space]] $X/\mathcal{D}$ exists as a smooth manifold and the projection map $X \to X/\mathcal{D}$ is a [[submersion]].

Then by the discussion at [[synthetic differential ∞-groupoid]], this projection map is also a [[formally smooth morphism]] in $\mathbf{H}$ according to def. \ref{GeometricAndEtale}. Moreover, being a quotient projection it is a [[1-epimorphism]] and hence exhibits the corresponding [[foliation groupoid]]

$$
  \left(
    X \underset{X/\mathcal{D}}{\times} X
    \stackrel{\to}{\to}
    X/\mathcal{D}
  \right)
$$

as a [[geometric ∞-groupoid]] in the sense of def. \ref{GeometricAndEtale}. 

Now $\flat ( X// \mathcal{D}) $ is the underlying set of points of the [[leaf space]], regarded as a [[discrete ∞-groupoid]]. So we have the [[pasting]] diagram of pullbacks 

$$
  \array{
    L_{l} &\to& \coprod_{l \in X/\mathcal{D}} L_l &\to& X
    \\
    \downarrow && \downarrow && \downarrow^{\mathrlap{\mathcal{D}}}
    \\
    {*} &\stackrel{\vdash l}{\to}& \coprod_{l \in D/\mathcal{X}}{*}
    &\to&
    X/\mathcal{D}
  }
$$

for every [[leaf]] $L_l$ labeled by the point $l \in X/\mathcal{D}$ in leaf space, which exhibits the leaf decomposition of $X$ under $\mathcal{D}$ according to def. \ref{FoliationInDifferentialCohesion} as the disjoint union of the leaves of $(X,\mathcal{D})$ in the traditional sense, injected into $X$ in the canonical way.

=--

+-- {: .num_example #TraditionalGeneralFoliation}
###### Example

Consider now $\mathcal{G}_\bullet$ any [[Lie groupoid]], hence in particular a [[smooth groupoid]] $\mathcal{G} \in \mathbf{H}$ equipped with an [[atlas]] $\mathcal{G}_0 \to \mathcal{G}$, which hence by example \ref{LieAndEtaleGroupoids} exhibits a [[geometric ∞-groupoid]] in the sense of def. \ref{GeometricAndEtale}, hence a foliation 
$\mathcal{D} \;\colon\; \mathcal{G}_0 \to \mathcal{G}$ in the sense of def. \ref{FoliationInDifferentialCohesion}.

Computation of the [[homotopy pullback]]

$$
  \array{
    LeafDec_{\mathcal{D}}(\mathcal{G}_0) &\to& \mathcal{G}_0
    \\
    \downarrow && \downarrow^{\mathrlap{\mathcal{D}}}
    \\
    \flat( \mathcal{G} ) &\to& \mathcal{G} & = \mathcal{G}_0//\mathcal{D}
  }
$$

by the method as in example \ref{LieAndEtaleGroupoids} shows that $LeafDec_{\mathcal{D}}(\mathcal{G}_0)$ is the [[smooth groupoid]] presented by the presheaf of groupoids whose

* smoothyl $U$-parameterized collection of objects are smoothly $U$-parameterized collections of morphisms $\{g_0 \to g(u)\}_{u \in U}$ in $\mathcal{G}_\bullet$ with $g_0$ held fixed;

* morphisms are given by precomposing these collections with a fixed (not varying with $U$) morphism in $\mathcal{G}_\bullet$.

This means that if $\mathcal{G}_\bullet$ is an [[étale groupoid]] to start with, then $LeafDec_{\mathcal{D}}(\mathcal{G}_0)$ is the disjoint union of all its [[orbit]] leaves (as smooth manifolds), hence that the abstractly defined $LeafDec_{\mathcal{D}}(\mathcal{G}_0)$ reproduces the decomposition of $\mathcal{G}_0$ by the [[foliation]] encoded by the [[foliation groupoid]] $\mathcal{G}_\bullet$ as in traditional theory.


=--

+-- {: .num_remark}
###### Remark

If the $\mathcal{G}_\bullet$ in example \ref{TraditionalGeneralFoliation} is not an [[étale groupoid]] to start with but a more general [[Lie groupoid]], then $LeafDec_{\mathcal{D}}(\mathcal{G}_0)$ in general retains information of non-[[discrete group|discrete]] [[isotropy groups]] of $\mathcal{G}_\bullet$. 

We might decide to rule out this possibility by adding to the axioms in def. \ref{FoliationInDifferentialCohesion} the clause that $X//\mathcal{G}$ (here $\mathcal{G}_0//\mathcal{D}$) be &#233;tale.

However, we might also keep that case and regard it as the first instance of what is certainly a natural phenomenon as we pass to [[higher geometry]], namely that leaves of a foliation no longer need to manifolds but will be (higher) groupoids themselves.
 
=--

Finally, given the above it is clear how isotropic foliations come out.

+-- {: .num_example}
###### Example

For $\mathbb{G} = U(1)$ the smooth [[circle group]], $\Omega^2_{cl}$ is the ordinary sheaf of closed [[differential 2-forms]] under the canonical embedding

$$
  Sh(CartSp) \hookrightarrow
  Sh_\infty(CartSp)
  \simeq
  Smooth\infty Grpd
  \stackrel{i_!}{\hookrightarrow}
  SynthDiff\infty\mathrm{Grpd}
  \,.
$$

Then for $X$ a [[smooth manifold]] a morphism $\omega \;\colon\; X \to \Omega^2_{cl}$ is equivalently a [[differential 2-form]].

Then for $\mathcal{D} \;\colon\; X \to X//\mathcal{D}$ a traditional [[foliation]] of $X$ regarded as a foliation in  $SynthDiff\infty Grpd$ by example \ref{TraditionalGeneralFoliation}, it follows with the discussion there that $\iota_{\mathcal{D}}^* \omega$ is precisely the collection of restriction of $\omega$ to each of the leaves of the foliation. Therefore this is a foliation by isotropic submanifolds in the traditional sense precisely if it is an $\omega$-isotropc foliation in the sense of def. \ref{IsotropicFoliationsInDiffCohe}.

=--




## Related concepts

* [[coisotropic submanifold]]

[[!redirects isotropic submanifolds]]