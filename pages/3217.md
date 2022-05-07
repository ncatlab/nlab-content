
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Higher Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc} 

## Idea

A _foliation_ of a [[manifold]] $X$ is a decomposition into [[submanifolds]]. These submanifolds are called the _leaves_ of the foliation and one says that $X$ is _foliated by the leaves_. In order to have a useful notion, leaves are required to behave sufficiently well locally. In particular, if all leaves have the same [[dimension]], then one speaks of a _regular foliation_, which is the case discussed here. If the dimension of leaves is allowed to vary, one speaks instead a _[[singular foliation]]_; see there for more details.

For [[smooth manifolds]], smooth foliations are decompositions into [[immersion|immersed]] [[submanifolds]] that locally can be expressed as [[fibers]] of a [[submersion]] (the projection to the [[space of leaves]]).

Historically (as they were introduced in [Ehresmann](#Ehresmann) and [Reeb](#Reeb)), one considered foliations for [[smooth manifolds]] $X$ as arising from subbundles of the [[tangent bundle]] $E \hookrightarrow T X$ that are [[integrable distributions]] in the sense that the [[Lie bracket]] of [[vector fields]] that are [[sections]] of $E$ is again a section of $E$: the leaves are the submanifolds whose tangent vectors are sections of $E$. If one thinks of $E$ as encoding a [[differential equation]], then the leaves are the solution spaces to this equation.

Expressed in terms of [[higher Lie theory]] such an integrable distribution is a sub-[[Lie algebroid]] of the [[tangent Lie algebroid]] of $X$. Accordingly, under [[Lie integration]] of this structure foliations of $X$ are also equivalently encodes as [[Lie groupoids]] whose space of objects is $X$ and whose [[orbits]] are the leaves of the foliation.

Moreover, foliations are classified by [[Čech cohomology]] [[cocycles]] with coefficients in a [[topological groupoid]]/[[Lie groupoid]] called the _[[Haefliger groupoid]]_. These relations make foliation theory of sub-topic of [[Lie groupoid]]-theory. See also at _[[motivation for higher differential geometry]]_.

The Haefliger groupoids in fact classifies structures slightly more general than foliations: _[[Haefliger structures]]_.

## Definition

There are several equivalent definitions of foliations.

### Original definition

Let $M$ be an $n$-[[dimension|dimensional]] [[topological manifold]]. A decomposition of $M$ as a [[disjoint union]] of [[connected topological space|connected]] subsets $V_\alpha$, called **leaves**, 

$$ M  = \cup_\alpha V_\alpha $$

is called a **foliation** if there is a [[cover]] of $M$ by a collection of "special" [[charts]] of the form $(U, \phi)$, $\phi = (\phi_1,\ldots,\phi_n) : U \to \mathbb{R}^n$ such that for each "special" chart and each $\alpha$ there is a number $p\leq n$, called the _dimension of the foliation_, such that the intersection of any given leaf $V_\alpha$ with $U$ is one of the level sets, i.e. the solution of the system $\phi_r(x) = const = const(r,U,\alpha)$ for all $r\gt p$.

If the manifold is a [[smooth manifold]], the charts may be required to be smooth too, to obtain the notion of a _smooth foliation_ or _foliation in [[differential geometry]]_. In this case, the $p$-dimensional foliations with underlying manifold $X$ are in 1-1 correspondence with [[integrable distributions]] of hyperplanes of dimension $p$ in the [[tangent bundle]] of $X$. 

### Alternative definitions

The following equivalent definitions and their relation are discussed for instance in ([IfLg, 1.2](#MoerdijkMrcun)).

+-- {: .num_defn}
###### Definition

A **foliation atlas** of a [[manifold]] $X$ of [[dimension]] $n$ and leaf-[[codimension]] $q$ is an [[atlas]] $\{\phi_i^{-1}: R^n \to X\}_i$ such that the transition functions are globally of the form 

$$
  \phi_{i j} : (x,y) \mapsto (g_{i j}(x,y), h_{i j}(y))
$$

with respect to the canonical decomposition $\mathbb{R}^n = \mathbb{R}^{n-q} \times \mathbb{R}^q$.

$$
  \array{
    \mathbb{R}^n &\stackrel{\phi_{i j}}{\to}& \mathbb{R}^n && 
    \\
    \downarrow && \downarrow 
    \\
    \mathbb{R}^q &\stackrel{h_{i j}}{\to}& \mathbb{R}^q
  }
  \,.
$$

=--

+-- {: .num_defn #FoliationAtlasByLocalSubmersions}
###### Definition

A **foliation atlas** of a [[manifold]] $X$ of [[dimension]] $n$ and leaf-[[codimension]] $q$ is an [[open cover]] $\{U_i \to X\}_i$ of $X$ equipped with [[submersions]] $\{ s_i \colon U_i \to \mathbb{R}^q \}$
such that there exists [[diffeomorphisms]]

$$
   \gamma_{i j} \colon s_j(U_i \cap U_j) \to s_i(U_i \cap U_j)
$$

satisfying on each $U_i \cap U_j$ the condition

$$
  s_i = \gamma_{i j} \circ s_j 
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

Given a foliation atlas as in def. \ref{FoliationAtlasByLocalSubmersions},
the [[diffeomorphisms]] $\{\gamma_{i j}\}_{i,j}$ satisfy the [[Cech cohomology|Cech]] [[cocycle]] condition

$$
   \gamma_{i j} \circ \gamma_{j k} = \gamma_{i k}
  \,.
$$

This is called the **[[Haefliger cocycle]]** of the foliation atlas.

=-- 

+-- {: .num_defn #AsIntegrableDistribution}
###### Definition

A smooth foliation of a [[smooth manifold]] $X$ is equivalently an [[integrable distribution]] (or an integrable subbundle) $E \hookrightarrow T X$.

=--

### In terms of Lie algebroids and Lie groupoids
 {#InTermsOfLieAlgebroidsAndLieGroupoids}

Definition \ref{AsIntegrableDistribution} above 
is immediately reformulated equivalently as the following statement
in [[higher Lie theory]].

+-- {: .num_defn #AsLieAlgebroidsWithInjectiveAnchor}
###### Definition

For $X$ a [[smooth manifold]], a foliation of $X$ is equivalently a [[Lie algebroid]] over $X$ such that the [[anchor map]] is an [[injection]].

=--

+-- {: .num_remark}
###### Remark

The [[Lie groupoids]] which under [[Lie differentiation]] give rise to Lie algebroids with injective anchors as in def. \ref{AsLieAlgebroidsWithInjectiveAnchor} are precisely those which are Morita-equivalent to [[étale groupoids]] (hence are the _[[foliation groupoids]]_, see there for more details) ([Crainic-Moerdijk 00, theorem 1](#CrainicMoerdijk)).

=--

One says:

+-- {: .num_defn}
###### Definition

A [[Lie groupoid]] **integrates** a given foliation, if it [[Lie integration|Lie integrates]] the coresponding [[Lie algebroid]], according to def. \ref{AsLieAlgebroidsWithInjectiveAnchor}.

=--

+-- {: .num_example}
###### Example

For a [[simple foliation]] $\mathcal{D}$ of a manifold $X$, example \ref{SimpleFoliation}, hence one where there is a [[submersion]] 

$$ p_{\mathcal{D}} \;\colon\; X \to X/\mathcal{D}$$

to the leaf space, that map itself is the [[atlas]] of a Lie groupoid $\mathcal{G}$ which integrates the foliation, which is the [[Cech nerve]]

$$
  \mathcal{G}_\bullet
  = 
  \left(
     X \underset{X/\mathcal{D}}{\times} X
     \stackrel{\to}{\to}
     X/\mathcal{D}
  \right)
  \,.
$$

=--

+-- {: .num_example}
###### Example

Among all Lie groupoids that integrate a given foliation $\mathcal{F}$ of a manifold $X$, the two special extreme

1. [[holonomy groupoid]] $Hol(X,\mathcal{F})_\bullet$

1. [[monodromy groupoid]] $Monod(X,\mathcal{F})_\bullet$

=--

+-- {: .num_prop}
###### Proposition

Let $\mathcal{G}_\bullet$ be a [[Lie groupoid]] with (for simplicity) [[connected topological space|connected]] source-fibers. 

Then there are maps

$$
  hol
  \;\colon\;
  Monod(X,\mathcal{F})_\bullet
  \stackrel{g_{\mathcal{G}}}{\to}
  \mathcal{G}_\bullet
   \stackrel{hol_G}{\to}
  Hol(X,\mathcal{F})
$$

which are surjective [[local diffeomorphisms]] and such that the composite is the holonomy morphism (...).

=--

This is ([Crainic-Moerdijk 00, prop. 1](#CrainicMoerdijk)).

### Of higher smooth spaces

One can consider the generalization of the notion of foliation of manifolds to foliations of structures in [[higher differential geometry]] such as [[Lie groupoids]] and [[Lie algebroids]]. See at 

* [[foliation of a Lie algebroid]]

* [[foliation of a Lie groupoid]]

### In terms of differential cohesive higher geometry
 {#InCohesiveHigherGeometry}

The following is a suggestion for an axiomatization of foliations in [[higher differential geometry]] in the formalization of [[differential cohesion|differential]] [[cohesion]], followed by some considerations showing how these axioms reproduce traditional theory. 

> Under construction.

+-- {: .num_defn }
###### Definition (Notation)

Let $\mathbf{H}$ be a [[cohesive (∞,1)-topos]] equipped with [[differential cohesion]].

As usual, we write $(\int \dashv \flat \dashv \sharp)$ for the [[adjoint triple]] of [[modalities]] that defines the [[cohesion]] ([[shape modality]] $\dashv$ [[flat modality]] $\dashv$ [[sharp modality]]) and we write $(Red \dashv \int_{inf} \dashv \flat_{inf})$ for the adjoint triple of modalities that defines the [[differential cohesion]] ([[reduction modality]] $\dashv$ [[infinitesimal shape modality]] $\dashv$ [[infinitesimal flat modality]]). 

=--

Below we are going to axiomatize aspects of the traditional description of foliations by [[Lie groupoids]]/[[foliation groupoids]] as discussed [above](#InTermsOfLieAlgebroidsAndLieGroupoids), so we start by briefly setting up some terminology on [[groupoid object in an (infinity,1)-category|groupoid objects]] in [[differential cohesion]].

+-- {: .num_defn #NotationForGroupoidObjects}
###### Definition (Notation for groupoid objects and atlases)

By the [[Giraud-Rezk-Lurie axioms]]
we may think of a [[1-epimorphism]] $\mathcal{G}_0 \to \mathcal{G}$ in $\mathbf{H}$ as an [[atlas]] of the cohesive $\infty$-groupoid $\mathcal{G} \in \mathbf{H}$, exhibiting equivalently the corresponding [[groupoid object in an (infinity,1)-category|groupoid object]] which we write 

$$
  \mathcal{G}_\bullet \coloneqq \mathcal{G}_0^{\times^{\bullet+1}_{\mathcal{G}}}
  \,.
$$

Hence we use notation where omitting the subscript decorationon a groupoid object $\mathcal{G}_\bullet \in \mathbf{H}^{\Delta^{op}}$ refers to its realization 

$$
  \mathcal{G} \coloneqq {\underset{\rightarrow}{\lim}}_n \mathcal{G}_{n}
  \;\;\;
  \in \mathbf{H}
  \,. 
$$

=--

We have the following "geometricity" constraints on groupoid objects.

+-- {: .num_defn #GeometricAndEtale}
###### Definition

For $f \colon X \to Y$ any morphism in $\mathbf{H}$, write 

$$
  X \stackrel{L(f)}{\to} Y \underset{\int_{inf} Y}{\times} \int_{inf} X
$$

for the canonical morphism induced by the [[natural transformation|naturality]] of the $\int_{inf}$-[[unit of an adjunction|unit]]. We say that

1. $f$ is a **[[formally smooth morphism]]** (or _[[submersion]]_) if $L(f)$ is a [[1-epimorphism]];

1. $f$ is a **[[formally étale morphism]]** (or _[[local diffeomorphism]]_) if $L(f)$ is an [[equivalence in an (infinity,1)-category|equivalence]].

Now if $\pi \colon \mathcal{G}_0 \to \mathcal{G}$ is a [[1-epimorphism]], hence an [[atlas]] for the cohesive $\infty$-groupoid $\mathcal{G}$, then we say about the corresponding [[groupoid object in an (infinity,1)-category|groupoid object]] as in def. \ref{NotationForGroupoidObjects}, that

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

a foliation of $X$ by **$\omega$-[[isotropic submanifold|isotropic subspaces]]** is a [[foliation]] $\mathcal{D} \colon X \to X//\mathcal{D}$
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

We now discuss how low-degree examples of this axiomatics interpreted in $\mathbf{H} \coloneqq $ [[SynthDiff∞Grpd]] reproduces the traditional notions of [[foliations]] and [[isotropic submanifolds]] of [[pre-symplectic manifolds]].

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
    & \swarrow && \searrow & &&& &&& \mathcal{G}_0
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

Let $X$ be a smooth manifold and  let $\mathcal{D}$ be a traditional [[foliation]] on $X$ which is a _[[simple foliation]]_, example \ref{SimpleFoliation}, 
in that the [[leaf space]] $X/\mathcal{D}$ exists as a smooth manifold and the projection map $X \to X/\mathcal{D}$ is a [[submersion]].

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

+-- {: .num_remark }
###### Remark

We may suggestively summarize example \ref{TraditionalGeneralFoliation} in words as:

"In cohesive higher geometry, every foliation is a [[simple foliation]]."

Because the quotient map to the leaf space of a general foliation is always a [[submersion]]/[[formally smooth morphism]], just not always onto a manifold, but onto a higher space.


=--

+-- {: .num_remark}
###### Remark

If the $\mathcal{G}_\bullet$ in example \ref{TraditionalGeneralFoliation} is not an [[étale groupoid]] to start with but a more general [[Lie groupoid]], then $LeafDec_{\mathcal{D}}(\mathcal{G}_0)$ in general retains information of non-[[discrete group|discrete]] [[isotropy groups]] of $\mathcal{G}_\bullet$. 

We might decide to rule out this possibility by adding to the axioms in def. \ref{FoliationInDifferentialCohesion} the clause that $X//\mathcal{G}$ (here $\mathcal{G}_0//\mathcal{D}$) be &#233;tale.

However, we might also keep that case and regard it as the first instance of what is certainly a natural phenomenon as we pass to [[higher geometry]], namely that leaves of a foliation no longer need to manifolds but will be (higher) groupoids themselves.
 
=--

Finally, given the above it is clear how [[isotropic submanifold|isotropic]] appear in the cohesive axiomatics.

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

Then for $\mathcal{D} \;\colon\; X \to X//\mathcal{D}$ a traditional [[foliation]] of $X$ regarded as a foliation in  $SynthDiff\infty Grpd$ by example \ref{TraditionalGeneralFoliation}, it follows with the discussion there that $\iota_{\mathcal{D}}^* \omega$ is precisely the collection of restriction of $\omega$ to each of the leaves of the foliation. Therefore this is a foliation by [[isotropic submanifolds]] in the traditional sense precisely if it is an $\omega$-isotropc foliation in the sense of def. \ref{IsotropicFoliationsInDiffCohe}.

=--






## Examples

+-- {: .num_example #SimpleFoliation}
###### Example

For $X \to Y$ a [[submersion]] of [[smooth manifolds]], the connected [[fibers]] of the submersion constitute a foliation of $X$ whose [[codimension]] is the [[dimension]] of $Y$. Foliations of this form are called **[[simple foliations]]**.

=--

+-- {: .num_example}
###### Example

Every [[Lie groupoid]] gives a folitation on its space of [[objects]]: the leaves are the [[orbits]]. Conversely, every regular foliation gives rise to its [[holonomy groupoid]]. This is a (not necessarily Hausdorff) Lie groupoid whose orbits are the leaves of the original foliation, and which in some sense is minimal with this condition.

=--

+-- {: .num_example}
###### Example

Every [[Poisson manifold]] has a canonical structure of a foliation whose leaves are its maximal [[symplectic manifold|symplectic]] submanifolds, called *[[symplectic leaves]]*.

=--
## Properties

### Leaf space

The set of components of a foliation is typically non-[[Hausdorff space|Hausdorff]], which is one of the motivations of the [[Alain Connes|Connes]]-style [[noncommutative geometry]]. 

### Classification

Folitation are classified by the [[Haefliger groupoid]]. See at _[[Haefliger theorem]]_.

### Characteristic classes

There is a theory of [[characteristic classes]] for foliations. A most well known example is the [[Godbillon-Vey characteristic class]] for codimension one foliations. 

## Related concepts

* [[Bott connection]]

* [[holonomy groupoid]], [[monodromy groupoid]]

* [[orbifold]]

* [[Frobenius theorem (differential topology)]]

* [[higher differential geometry applied to plain differential geometry]]



## References
 {#References}

The notion of foliated manifolds was introduced in the 1950s, motivated from [[partial differential equation]] theory, in 


* [[Charles Ehresmann]], ...

* Reeb, ...

* [[Eli Cartan]], _Sur l'int&#233;gration des &#233;quations diff&#233;rentiels completement int&#233;grable_, Oeuvres Compl&#232;tes, Pt. II, Vol. I, 555-561.

A discussion in [[differential geometry]] is in

* Robert Hermann, _On the differential geometry of foliations_, Annals of Mathematics, Second Series, Vol. 72, No. 3 pp. 445-457 ([jstor](http://www.jstor.org/stable/1970226))

A textbook account with a view to the modern formulation in [[Lie groupoid]] theory is 

* [[Ieke Moerdijk]], [[Janez Mr?un]], _[[Introduction to foliations and Lie groupoids]]_, Cambridge Studies in Advanced Mathematics __91__, 2003. x+173 pp. ISBN: 0-521-83197-0
 {#MoerdijkMrcun}

Foliations in [[Lie groupoid]] theory are discussed in more detail in 

* [[Marius Crainic]], [[Ieke Moerdijk]], _Foliation groupoids and their cyclic homology_ ([arXiv:math/0003119](http://arxiv.org/abs/math/0003119))
 {#CrainicMoerdijk}

The corresponding [[groupoid algebras]] are discussed in chapter 2, section 8 of 

* [[Alain Connes]], _[[Noncommutative Geometry]]_

See also

* [wikipedia](http://en.wikipedia.org/wiki/Foliation), Springer Online Enc. of Math.: [foliation](http://eom.springer.de/F/f040740.htm)

A survey by Fuks in Russian Itogi:

* &#1044;. &#1041;. &#1060;&#1091;&#1082;&#1089;, _&#1057;&#1083;&#1086;&#1077;&#1085;&#1080;&#1103;_, &#1048;&#1090;&#1086;&#1075;&#1080; &#1085;&#1072;&#1091;&#1082;&#1080; &#1080; &#1090;&#1077;&#1093;&#1085;. &#1057;&#1077;&#1088;. &#1040;&#1083;&#1075;&#1077;&#1073;&#1088;&#1072;. &#1058;&#1086;&#1087;&#1086;&#1083;. &#1043;&#1077;&#1086;&#1084;., 1981,  &#1090;&#1086;&#1084; __18__, &#1089;&#1090;&#1088;. 151&#8211;-213, [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=inta&paperid=93&what=fullt&option_lang=rus)

Cohomology of formal vector fields and characteristic classes of foliations were originally studied in the papers

* D. B. Fuks, _Cohomology of infinite-dimensional Lie algebras and characteristic classes of foliations_ (book, Rus. and Eng. versions)

* I. M. Gel&#697;fand, B. L. Fe&#301;gin, D. B. Fuks, _Cohomology of the Lie algebra of formal vector fields with coefficients in its dual space and variations of characteristic classes of foliations, Funkcional. Anal. i Prilo&#382;en.  8  (1974), no. 2, 13--29 (Russian original [mathnet.ru](http://www.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=faa&paperid=2326&option_lang=eng), [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=faa&paperid=2326&volume=8&year=1974&issue=2&fpage=13&what=fullt&option_lang=eng))

* Claude Godbillon, _Cohomologies d'alg&#232;bres de Lie de champs de vecteurs formels_, S&#233;minaire Bourbaki, 25&#232;me ann&#233;e (1972/1973), Exp. No. 421, pp. 69--87. Lecture Notes in Math. __383__, Springer 1974. 

* &#1048;. &#1052;. &#1043;&#1077;&#1083;&#1100;&#1092;&#1072;&#1085;&#1076;, &#1044;. &#1041;. &#1060;&#1091;&#1082;&#1089;, _&#1050;&#1086;&#1075;&#1086;&#1084;&#1086;&#1083;&#1086;&#1075;&#1080;&#1080; &#1072;&#1083;&#1075;&#1077;&#1073;&#1088;&#1099; &#1051;&#1080; &#1092;&#1086;&#1088;&#1084;&#1072;&#1083;&#1100;&#1085;&#1099;&#1093; &#1074;&#1077;&#1082;&#1090;&#1086;&#1088;&#1085;&#1099;&#1093; &#1087;&#1086;&#1083;&#1077;&#1081;_, &#1048;&#1079;&#1074;. &#1040;&#1053; &#1057;&#1057;&#1057;&#1056;. &#1057;&#1077;&#1088;. &#1084;&#1072;&#1090;&#1077;&#1084;., 1970,  __34__, &#1074;. 2, &#1089;&#1090;&#1088;. 322&#8211;-337, [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=im&paperid=2418&what=fullt&option_lang=rus)

In a series of works of Connes and Moscovici, the local index formulas in the context of transverse geometry of foliations has been studied in connection to a new cyclic homology of a Hopf algebra arising in this context: 

* [[A. Connes]], H. Moscovici, _Modular Hecke algebras and their Hopf symmetry_, Mosc. Math. J., 4:1 (2004), 67&#8211;109; [math.QA/0301089](http://arxiv.org/abs/math/0301089), [ams](http://www.ams.org/distribution/mmj/vol4-1-2004/connes_moscovici_1.pdf); _Hopf algebras, cyclic cohomology and the transverse index theory_, [math.DG/9806109](http://arxiv.org/abs/math/9806109), Comm. Math. Phys. __198__, n.1, 1998 [MR99m:58186](http://www.ams.org/mathscinet-getitem?mr=1657389) [doi](http://dx.doi.org/10.1007/s002200050477); _Rankin-Cohen brackets and the Hopf algebra of transverse geometry_, Mosc. Math. J., 4:1 (2004), 111&#8211;130; _Differentiable cyclic cohomology and Hopf algebraic structures in transverse geometry_, in: Essays on geometry and related topics, Vol. 1, 2, Monogr. Enseign. Math. __38__, p. 217&#8211;255. Enseignement Math., Geneva, 2001 [MR2003k:58042](http://www.ams.org/mathscinet-getitem?mr=1929328)
* A. Connes, _Cyclic cohomology and the transverse fundamental class of a foliation_, in: Geom. methods in operator algebras (Kyoto, 1983), Pitman Res. Notes in Math. __123__, p. 52&#8211;144, 1986 [MR88k:58149](http://www.ams.org/mathscinet-getitem?mr=866491)

More general issues of index theory in noncommutative geometry applied to foliations is in 

* Yu. A. Kordyukov, _Noncommutative geometry of foliations_, J. K-Theory, 2:2, Special issue in memory of Y. P. Solovyev, Part 1 (2008), 219&#8211;327 [MR2009m:58018](http://www.ams.org/mathscinet-getitem?mr=2456103); _Index theory and non-commutative geometry on foliated manifolds_, Russian Math. Surveys, 64:2 (2009), 273&#8211;391 (original: &#1070;. &#1040;. &#1050;&#1086;&#1088;&#1076;&#1102;&#1082;&#1086;&#1074;, &#1059;&#1052;&#1053;, 64:2(386) (2009), 73&#8211;202); _&#1060;&#1086;&#1088;&#1084;&#1091;&#1083;&#1072; &#1089;&#1083;&#1077;&#1076;&#1086;&#1074; &#1076;&#1083;&#1103; &#1090;&#1088;&#1072;&#1085;&#1089;&#1074;&#1077;&#1088;&#1089;&#1072;&#1083;&#1100;&#1085;&#1086;-&#1101;&#1083;&#1083;&#1080;&#1087;&#1090;&#1080;&#1095;&#1077;&#1089;&#1082;&#1080;&#1093; &#1086;&#1087;&#1077;&#1088;&#1072;&#1090;&#1086;&#1088;&#1086;&#1074; &#1085;&#1072; &#1088;&#1080;&#1084;&#1072;&#1085;&#1086;&#1074;&#1099;&#1093; &#1089;&#1083;&#1086;&#1077;&#1085;&#1080;&#1103;&#1093;_, &#1040;&#1083;&#1075;&#1077;&#1073;&#1088;&#1072; &#1080; &#1072;&#1085;&#1072;&#1083;&#1080;&#1079;, 12:3 (2000), 81&#8211;105 [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=aa&paperid=1108&what=fullt&option_lang=rus)

* W. P. Thurston, _Existence of codimension-one foliations_,  Ann. of Math. (2) __104__  (1976), no. 2, 249--268 ([doi](http://dx.doi.org/10.1007/BF02566730)); _Foliations and groups of diffeomorphisms_, Bull. Amer. Math. Soc. 80  (1974), 304--307 ([pdf](http://www.ams.org/bull/1974-80-02/S0002-9904-1974-13475-0/S0002-9904-1974-13475-0.pdf)); _The theory of foliations of codimension greater than one_,  Comment. Math. Helv.  49  (1974), 214--231 ([link](http://resolver.sub.uni-goettingen.de/purl?GDZPPN00206135X))

The first of a series on foliations in [[derived geometry]]

* [[Bertrand Toën]], [[Gabriele Vezzosi]], _Algebraic foliations and derived geometry: the Riemann-Hilbert correspondence_, ([arXiv:2001.05450](https://arxiv.org/abs/2001.05450))


[[!redirects foliations]]
[[!redirects leaf space]]
[[!redirects leaf spaces]]

[[!redirects space of leaves]]
[[!redirects spaces of leaves]]

[[!redirects foliation theory]]

[[!redirects regular foliation]]
[[!redirects regular foliations]]
