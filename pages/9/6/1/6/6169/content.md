
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

+-- {: .num_defn }
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

$SmoothMfd \hookrightarrow $ [[Smooth∞Grpd]] $\stackrel{i_!}{\hookrightarrow}$ [[SynthDiff∞Grpd]] $= \mathbf{H}$ is [[reduced object|reduced]] [[synthetic differential ∞-groupoids]].

+-- {: .num_example #TraditionalSubmersions}
###### Example

A [[smooth function]] $f \colon X \to Y$ between [[smooth manifolds]] is

1. a [[local diffeomorphism]] in the traditional sense precisely if it is a [[formally étale morphism]] in the sense of def. \ref{GeometricAndEtale};

1. a [[submersion]] in the traditional sense precisely if it is a [[formally smooth morphism]] in the sense of def. \ref{GeometricAndEtale}.

=--

This is discussed at _[[SynthDiff∞Grpd]]_.

+-- {: .num_example }
###### Example

Let $\mathcal{G}$ be a [[smooth groupoid]] which has a presentation $\mathcal{G}_\bullet$ where objects and morphisms are represented by a [[smooth manifold]] each, and consider it equipped with the induced [[atlas]] $\mathcal{G}_0 \to \mathcal{G}$. Then

* if the presentation $\mathcal{G}_\bullet$ is a [[Lie groupoid]] then $\mathcal{G}_0 \to \mathcal{G}$ is a [[geometric ∞-groupoid]] 

* if the presentation $\mathcal{G}_\bullet$ is an [[étale groupoid]] then $\mathcal{G}_0 \to \mathcal{G}$ is an [[étale ∞-groupoid]]

in the sense of def. \ref{GeometricAndEtale}.

=--

This follows by the corresponding discussion at [[SynthDiff∞Grpd]]. The idea of the proof is that one presents the atlas in the [[projective model struture on simplicial presheaves]] by the [[décalage]] [[fibration]] [[resolution]], schematiccally

$$
  \array{
    && g
    \\
    & \swarrow && \searrow & &&& \mathcal{G}_0
    \\
    g_1 &&\to&& g_2
    \\
    \\
    &&&& &&& \downarrow
    \\
    \\
    g_1 &&\to&& g_2 &&& \mathcal{G}    
  }
  \,.
$$

Then the [[homotopy pullback]] $\mathcal{G} \underset{\int_{inf}\mathcal{G}} {\times}\int_{inf} X $ is presented by an ordinary pullback and so 
example \ref{TraditionalSubmersions} applies degreewise. In degree 0 the above resolution is the target map in the groupoid $\mathcal{G}$ and so by example \ref{TraditionalSubmersions} this is a [[submersion]] or [[local diffeomorphism]], respectively, as claimed.



+-- {: .num_example }
###### Example

Let $X \in SmoothMfd \hookrightarrow $ [[Smooth∞Grpd]] $\stackrel{i_!}{\hookrightarrow}$ [[SynthDiff∞Grpd]] $= \mathbf{H}$ be a [[smooth manifold]], regarded canonically as a [[reduced object|reduced]] [[synthetic differential ∞-groupoid]]. Let $\mathcal{D}$ be a [[foliation]] on $X$ which is _simple_ in that the [[leaf space]] $X/\mathcal{D}$ exists as a smooth manifold and the projection map $X \to X/\mathcal{D}$ is a [[submersion]].

Then by the discussion at [[synthetic differential ∞-groupoid]], this projection map is also a [[formally smooth morphism]] in $\mathbf{H}$ according to def. \ref{GeometricAndEtale}. Moreover, being a quotient projection it is a [[1-epimorphism]] and hence exhibits the corresponding [[foliation groupoid]]

$$
  \left(
    X \underset{X//\mathcal{D}}{\times} X
    \stackrel{\to}{\to}
    X//\mathcal{D}
  \right)
$$

as a [[geometric ∞-groupoid]] in the sense of def. \ref{GeometricAndEtale}. 

=--

(...)



## Related concepts

* [[coisotropic submanifold]]

[[!redirects isotropic submanifolds]]