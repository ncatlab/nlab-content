
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The field content of 11-dimensional [[nLab:supergravity]] contains a [[higher U(1)-gauge field]] called the _supergravity C-field_ or _M-theory 3-form_ , which is locally a 3-form and globally _some_ variant of a [[circle n-bundle with connection|circle 3-bundle with connection]]. 

There have been several suggestions for what _precisely_ its correct global description must be, see at _[Models](#Models)_ below

## Consistency conditions
 {#ConsistencyConditions}

Several subtle consistency conditions ([[quantum anomaly cancellation]]-conditions) have been argued for the [[charge quantization]] of the supergravity C-field:

1. [Shifted flux quantization condition](#ShiftedCFieldFluxQuantizationCondition)

1. [C-Field tadpole cancellation condition](#CFieldTadpoleCancellationCondition)

### Shifted flux quantization condition
 {#ShiftedCFieldFluxQuantizationCondition}
 

The _[[shifted C-field flux quantization condition]]_ is a [[charge quantization]]-condition on the [[supergravity C-field]] expected in [[M-theory]]. It says that the [[real cohomology]] class of the [[flux density]] ([[field strength]]) [[differential 4-form]] $G_4 \in \Omega^4(X)$ on [[spacetime]] $X$ becomes integral after shifted by one quarter of the [[first Pontryagin class]], hence the condition that with the shifted 4-flux density defined as

\[
  \label{Shiftwed}
  \widetilde G_4 
  \;\coloneqq\;
  G_4 + \tfrac{1}{4}p_1(\nabla_{T X})
  \;\in\;
  \Omega^4(X)
\]

(for $\nabla_{T X}$ any [[affine connection]] on [[spacetime]], in particular the [[Levi-Civita connection]]) we have (using the [[de Rham theorem]] to translate from [[de Rham cohomology]] to [[real cohomology]]) that $\widetilde G_4$ represents an [[integral cohomology]]-class:

$$
  [\widetilde G_4]
  \;\in\;
  H^4(X, \mathbb{Z})
  \overset{H^4(X, \mathbb{Z}\hookrightarrow \mathbb{R})}{\longrightarrow}  
  H^4(X, \mathbb{R})
  \,.
$$


This condition was originally argued for in ([Witten 96a](#Witten96a), [Witten 96b](#Witten96b)) as a sufficient condition for ensuring that the [[prequantum line bundle]] for the [[7d Chern-Simons theory]] on an [[M5-brane]] [[worldvolume]] is divisible by 2.

Proposals for encoding this condition by a [[Wu class]]-shifted variant of [[generalized (Eilenberg-Steenrod) cohomology theory|stable]] [[ordinary differential cohomology]] were considered in [[Quadratic Functions in Geometry, Topology, and M-Theory|Hopkins-Singer 02]], [Diaconescu-Freed-Moore 03](#DiaconescuFreedMoore03), [FSS 12](#FSS12).

It turns out that the shifted flux quantization condition on the C-field is naturally implied ([FSS1 19b, Prop. 4.12](#FSS19b)) by the requirement that $G_4$ is the differential form datum underlying, via [[Sullivan model|Sullivan's theorem]], a [[cocycle]] in unstable [[J-homomorphism|J-]] [[twisted Cohomotopy]] in degree 4 ([[schreiber:Hypothesis H]]).


### C-Field tadpole cancellation condition
 {#CFieldTadpoleCancellationCondition}

In [[M-theory]] [[KK-compactification|compactified]] on 8-dimensional [[compact topological space|compact]] [[fibers]] $X^{(8)}$ (see _[[M-theory on 8-manifolds]]_) [[tadpole cancellation condition for the supergravity C-field]] has been argued ([Sethi-Vafa-Witten 96](shifted+C-field+flux+quantization#SethiVafaWitten96), [Becker-Becker 96](shifted+C-field+flux+quantization#BeckerBecker96), [Dasgupta-Mukhi 97](shifted+C-field+flux+quantization#DasguptaMukhi97)) to be the condition

$$
  N_{M2}
  \;+\;
  \tfrac{1}{2} \big( G_4[X^{(8)}]\big)^2
  \;=\;
  \underset{
    I_8(X^8)
  }{
    \underbrace{
      \tfrac{1}{48}\big( p_2 - (\tfrac{1}{2}p_1)^2  \big)[X^{8}]
    }
  }
  \;\;\;\;
  \overset{!}{\in}
  \mathbb{Z}
  \,,
$$

where

1. $N_{M2}$ is the net number of [[M2-branes]] in the spacetime (whose [[worldvolume]] appears as points in $X^{(8)}$);

1. $G_4$ is the [[field strength]]/flux of the [[supergravity C-field]]

1. $p_1$ is the [[first Pontryagin class]] and $p_2$ the [[second Pontryagin class]] combining to [[I8]], all regarded here in [[rational homotopy theory]].


If $X^{8}$ has 

* [[Spin(7)-structure]] (hence in particular if it is a [[Calabi-Yau manifold]], which has $SU(4) = $ [[Spin(6)]]-structure) 

or 

* [[Sp(2).Sp(1)-structure]] 

then

$$
  \tfrac{1}{2}\big( p_2 - \tfrac{1}{4}(p_1)^2  \big)
  \;=\;
  \chi
$$

is the [[Euler class]] (see [this Prop.](Spin7-manifold#CharacteristicClassesForSpinStructure) and [this Prop.](quaternion-Kähler+manifold#CharacteristicClassesForSpin5Spin3Structure), respectively), hence in these cases the condition is equivalently

\[
  \label{DasguptaMukhiConditionInTermsOfEuler}
  N_{M2}
  \;=\;
  -
  \tfrac{1}{2} \big( G_4[X^{(8)}]\big)^2
  \;+\;
  \tfrac{1}{24}\chi[X^8]
  \;\;\;\;
  \in
  \mathbb{Z}
  \,,
\]

where $\chi[X]$ is the [[Euler characteristic]] of $X$.



## Models
 {#Models}

One proposal for a mathematical model of the C-field is as a [[cocycle]] in a [[Wu class]]-shifted variant of [[ordinary differential cohomology]] in degree 4:

* [The DFM model](#DFMmodel)

Another proposal is that the C-field is simply a [[cocycle]] in [[J-homomorphism|J-]] [[twisted Cohomotopy]] ([[schreiber:Hypothesis H]]):

* [C-field charge quantization in J-twisted Cohomotopy](#ModelByTwistedCohomotopy)


### The DFM-model
 {#DFMmodel}

#### Construction via $E_8$ gauge fields

In ([DFM, section 3](#DiaconescuFreedMoore03)) the following definition is considered and argued to be a good model of the supergravity $C$-field.

+-- {: .num_note #NatureOfE8}
###### Note

The [[homotopy group]]s of the [[classifying space]] $B E_8$ of the [[Lie group]] [[E8]] satisfy

$$
  \pi_i B E_8 = 
   \left\{
     \array{
       \mathbb{Z} | i = 4
       \\
       0 | i \neq 4, i \leq 15
     }
   \right.
  \,.
$$

Therefore for $X$ a [[manifold]] of [[dimension]] $dim X \leq 15$ there is a canonical [[morphism]]

$$
  H^1(X, E_8)
  \simeq
  H^4(X, \mathbb{Z})
  \,.
$$

=--

+-- {: .num_defn #DFMDefinitionOfCField}
###### Definition

Let $X$ be a [[smooth manifold]] of [[dimension]] $dim X \lt 15$.
For each  $a \in H^4(X, \mathbb{Z})$. choose an [[nLab:E8]]-[[nLab:principal bundle]] $P \to X$ which represents $a$ under the above isomorphism.

Write then

$$
  \mathbf{E}(X) \in Grpd
$$

for the [[groupoid]] whose 

* [[object]]s are triples $(P,\nabla,c)$ where 

  * $P$ is one of the chosen $E_8$-bundles, 

  * $\nabla$ is a [[nLab:connection on a bundle|connection]] on $P$;

  * $c \in \Omega^3(X)$ is a degree-3 [[nLab:differential form]] on $X$.

* [[morphism]]s $\omega : (P, \nabla_1, c_1) \to (P, \nabla_2, c_2)$
  are parameterized by their source and target triples together with a closed 3-form  $\omega \in \Omega^3_{\mathbb{Z}}(X)$ with integral [[period]]s, subject to the condition that

  $$
    c_2 -c_1 = CS(\nabla_1,\nabla_2) + \omega
    \,,
  $$

  where $CS(\nabla_1, \nabla_2)$ is the relative [[nLab:Chern-Simons form]] corresponding to the linear path of connections from $\nabla_1$ to $\nabla_2$ 

* the [[composition]] of morphisms 

  $$    
    (\omega_2 \circ \omega_1 )
     :
    (P,\nabla_1, C_1)
      \stackrel{\omega_1}{\to}
    (P, \nabla_2, C_2)
      \stackrel{\omega_2}{\to}
    (P, \nabla_3, C_3)
  $$

  is given by

  $$
    \omega_1 + \omega_2 + \langle (\nabla_2-\nabla_1)\wedge(\nabla_3-\nabla2) \rangle
   \,.
  $$

=--

See ([DFM, (3.22), (3.23)](#DiaconescuFreedMoore03)).

Here we think of $X$ as equipped with a [[pseudo-Riemannian manifold|pseudo]] [[Riemannian manifold|Riemannian structure]] and [[spin connection]] $\omega$ and think of each object $(P,\nabla,C)$ of $\mathbf{E}(X)$ as inducing an degree-4 cocycle in [[ordinary differential cohomology]] with [[curvature]] 4-form

$$
  \mathcal{G}_{\nabla,c} = tr F_\nabla \wedge F_\nabla - \frac{1}{2} tr R_\omega \wedge R_\omega + d c
  \,.
$$

Notice that with the normalization implicit here the second terms is one half of the image of something in integral cohomology. So this is not itself a differential character, but can be regarded as "shifted differential character": a trivialization of the trivial 5-character with global connection 4-form given by $\frac{1}{2} tr R_\omega \wedge R_\omega$. See [below](#DFMOrientationAndFractionalClasses) for more on this.

+-- {: .num_prop #DFModelHomotopyGroups}
###### Claim

The above groupoid has [[homotopy group]]s

* $\pi_0 \simeq H^4_{diff}(Y)$

* $\pi_1(-,(\nabla,c)) \simeq H^2(Y, U(1))$ .

=--

The first, the set of connected components (gauge equivalence classes of $C$-fields) is isomorphic to the set of [[ordinary differential cohomology]] in degree 4 of $X$. In fact $\pi_0$ is naturally a [[torsor]] over this abelian group: the torsor of $\frac{1}{2}tr R^2$-shifted differential characters.

The second, the [[fundamental group]], is that of flat [[circle bundle]]s.


#### Orientation and fractional classes
  {#DFMOrientationAndFractionalClasses}

Ordinarily, given a $Spin \times E_8$-bundle $P \to Y$ with first fractional [[Pontryagin class]]

$$
  \lambda := \frac{1}{2}p_1(P)
$$

and second [[Chern class]]

$$
  a := c_2(P)
$$

the $C$-field is supposed to have a [[curvature]] class in [[de Rham cohomology]] given by 

$$
  a_{dR} + \frac{1}{2} \lambda_{dR} \in H_{dR}^4(Y)
  \,.
$$

Since in general $\lambda = \frac{1}{2}p_1(P)$ is not further divisible in integral cohomology, this means that this cannot be the curvature of any [[differential character]]/[[bundle 2-gerbe]]/[[circle n-bundle with connection|circle 3-bundle with connection]], since these are necessarily the images in de Rham cohomology of their integral classes.

See ([DFM 03, section 12.1](#DiaconescuFreedMoore03), [FSS 12](#FSS12)) 


#### Restriction to the boundary

By [DFM, section 12](#DiaconescuFreedMoore03) on a manifold $Y$ with boundary $X = \partial Y$ we are to impose $C|_{\partial Y} = 0$. 

See the discussion [below](#RestrictionToBoundaryInChernWeil) for how this reproduces the [[Green-Schwarz mechanism]] for heterotic [[supergravity]] on the boundary.





### Description in $\infty$-Chern-Weil theory

Some remarks on ways to regard the $C$-field from the point of view of [[∞-Chern-Weil theory]].

#### Abstract definition

We shall consider the sum of two $C$ fields,  whose curvature is the image in de Rham cohomology of the proper integral class $2 a - \lambda $

Recall from the discussion at [[circle n-bundle with connection]]
that in the [[cohesive (∞,1)-topos]] $\mathbf{H} := $ [[Smooth∞Grpd]] the circle 3-bundles with local 3-form connection over an [[object]] $Y \in \mathbf{H}$ (for instance a [[smooth manifold]], or an [[orbifold]]) are [[object]]s in the [[3-groupoid]] $\mathbf{H}_{diff}(Y, \mathbf{B}^3 U(1))$ that is the [[(∞,1)-pullback]]

$$
  \array{
    \mathbf{H}_{diff}(Y, \mathbf{B}^3 U(1)) &\to& H^4_{dR}(Y)
    \\
    \downarrow && \downarrow
    \\
    \mathbf{H}(Y, \mathbf{B}^3 U(1))
    &\stackrel{curv}{\to}&
    \mathbf{H}(Y, \mathbf{\flat}_{dR} \mathbf{B}^4 U(1))
  }
$$

in [[∞Grpd]].

(Recall from the discussion there that if desired one may pass to the canonical presentation of this by the [[model structure on simplicial presheaves]] over [[CartSp]] and that in this explicit presentation we may replace $H^4_{dR}(Y)$ with the more familiar $\Omega^4_{cl}(Y)$. )

We consider now the analog of this definition for the universal curvature form on $\mathbf{B}^3 U(1)$ replaced by the difference of the differentially refined second [[Chern class]] of [[E8]] and the first fractional [[Pontryagin class]] of the [[spin group]]. The resulting $(\infty,1)$-pullback we tentatively call $C Field(Y)$, though we shall have to discuss to which extend this faithfully models the $C$-field, and which aspects of it.

+-- {: .num_defn #AbstractDefOfCField}
###### Definition

For $Y \in $ [[Smooth∞Grpd]], let $C Field(Y) \in $ [[∞Grpd]] be the [[(∞,1)-pullback]]

$$
  \array{
    C Field(Y) &\to& H^4_{dR}(Y)
    \\
    \downarrow && \downarrow
    \\
    \mathbf{H}(Y, \mathbf{B} (Spin \times E_8))
    &\stackrel{(2\mathbf{c}_2)_{dR}- (\frac{1}{2}\mathbf{p}_1)_{dR}}{\to}&
    \mathbf{H}(Y, \mathbf{\flat}_{dR} \mathbf{B}^4 U(1))
  }
  \,.
$$

=--

+-- {: .num_note #PastingDecompOfAbstractDefOfCField}
###### Note

By its <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#ChernWeilTheory">intrinsic definition</a> we have that the differential characteristic class $(\mathbf{c}_2)_{dR}$ is the composite

$$
  (\mathbf{c}_2)_{dR} : 
  \mathbf{B}E_8
   \stackrel{\mathbf{c}_2}{\to}
  \mathbf{B}^3 U(1)
    \stackrel{curv}{\to}
  \mathbf{\flat}_{dR} \mathbf{B}^4 U(1)
$$ 

of the smooth refinement of the second [[Chern class]] with the <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#CurvatureCharacteristics">universal curvature form</a> on $\mathbf{B}^3 U(1)$. Similarly for $(\frac{1}{2}\mathbf{p}_2)_{dR}$.

=--

Therefore we may either compute the [[(∞,1)-pullback]] in def. \ref{AbstractDefOfCField} directly, or in two consecutive steps. Both methods lead to their insights. 

In 

* [General properties](#CWPerspectiveGeneralProperties)

we consider general abstract consequences of the above definition, mainly making use of the factorization. In

* [Presentation by differential form data](#CWPresentationByDifferentialFormData)

we find a presentation by [[simplicial presheaves]] of the direct [[homotopy pullback]]. 

In the first approach [[connection on a bundle|connections]] on the [[E8]]-[[principal bundle]]s never appear explicitly. In the second approach they appear as [[pseudo-connection]]s, or as genuine connections whose morphisms are however allowed to shift them arbitrarily. This means that these connections are purely auxiliary data that serve to present the required homotopies. They do not survive in cohomology. This is as in the [DFM model](#DFMmodel) above. 

Finally in 

* [Restriction to the boundary](#RestrictionToBoundaryInChernWeil)

we comment how genuine $E_8$-connections may appear inside the second presentation of the $C$-model. 

#### General properties
  {#CWPerspectiveGeneralProperties}


This implies by the [[pasting law]] for [[(∞,1)-pullback]]s that the $(\infty,1)$-pullback from def. \ref{AbstractDefOfCField} may be decomposed into two consecutive pullbacks of the form

$$
  \array{
    C Field(X) &\stackrel{\hat \chi}{\to}& \mathbf{H}_{diff}(X, \mathbf{B}^3 U(1))
     &\stackrel{\omega}{\to}&
     H^4_{dR}(X)
   \\
    \downarrow && \downarrow && \downarrow
   \\
   \mathbf{H}(X, \mathbf{B}(E_8 \times Spin(10,1)))
    &\stackrel{2\mathbf{c}_2- \frac{1}{2}\mathbf{p}_2}{\to}&
   \mathbf{H}(X, \mathbf{B}^3 U(1))
    &\stackrel{curv}{\to}&
   \mathbf{H}(X, \mathbf{\flat}_{dR} \mathbf{B}^4 U(1))
  }
  \,,
$$

where on the right we find the <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#DifferentialCohomology">defining pullback</a> for (the [[cocycle]] [[3-groupoid]] of) [[ordinary differential cohomology]].

=--

This implies the following structure and properties.

+-- {: .num_note #DifferentialCharacterOfCField}
###### Note/Definition

By the above there exists canonically a morphism

$$
  \hat \chi : C Field(X) \to \mathbf{H}(X,\mathbf{B}^3 U(1))
    \stackrel{\tau_{\leq 0}}{\to}
    H^4_{diff}(X)
$$

that maps $C$-field configurations to [[ordinary differential cohomology]] in degree 4, whose [[curvature]] $\omega(\hat \chi)$ is the image $(\mathbf{c}_2)_{dR}- (\frac{1}{2}\mathbf{p}_2)_{dR} :=  curv(2\mathbf{c}_2 - \frac{1}{2}\mathbf{p}_2)$ in de Rham cohomology of the second Chern-class of some $E_8$-bundle.


The differential cocycle $\hat \chi(C)$ has all the general properties that make its [[higher parallel transport]] over [[membrane]] worldvolumes be well-defined. (Apart from the coefficient of $\lambda$, this is the only requirement from which [DFM](#DiaconescuFreedMoore03) deduce their model.)


=--

The following proposition describes the first two [[homotopy group]]s of the [[3-groupoid]] $C Field(Y)$.

+-- {: .num_prop #HomotopyGroupsOfCField}
###### Proposition


Over a fixed $Spin$-[[principal bundle]] $P_{Spin}$ we have a [[short exact sequence]] (of [[pointed object|pointed sets]])

$$
  * \to 
   H^3(Y, U(1))
   \to
   \pi_0 C Field_{P_{Spin}}(Y)
   \to
   H^4_{dR}(Y)_{2 \mathbb{Z}}
   \to *
$$

and

$\pi_0 C Field_{P_{Spin}}(Y)$ is the group of pairs $([c], f) \in H^2(X, U(1)) \times C^\infty(X, E_8)$ where $f$ is a smooth refinement under $E_8 \simeq_{14} B^2 U(1) \simeq K(\mathbb{Z},3)$ of the integral image of $[c]$.


=--

+-- {: .proof}
###### Proof


Notice that we have the [[pasting]] [[diagram]] of [[(∞,1)-pullback]]s

$$
  \array{
    C Field_{\omega(\hat \chi(-)) = 0}(Y) 
     &\to& \mathbf{H}(Y, \mathbf{\flat} \mathbf{B}^3 U(1)) &\to& {*}
    \\
    \downarrow && \downarrow && \downarrow^{\mathrlap{0}} 
    \\
    C Field(Y) 
     &\stackrel{\hat \chi}{\to}& 
    \mathbf{H}_{diff}(Y, \mathbf{B}^3 U(1))
     &\stackrel{\omega}{\to}&
     H^4_{dR}(Y)
    \\
    \downarrow && \downarrow && \downarrow
   \\
   \mathbf{H}(Y, \mathbf{B}E_8)
    &\stackrel{2\mathbf{c}_2}{\to}&
   \mathbf{H}(Y, \mathbf{B}^3 U(1))
    &\stackrel{curv}{\to}&
   \mathbf{H}(Y, \mathbf{\flat}_{dR} \mathbf{B}^4 U(1))
  }
  \,,
$$

where the top right square is discussed at <a href="http://nlab.mathforge.org/nlab/show/cohesive+%28infinity%2C1%29-topos#DifferentialCohomology">cohesive (∞,1)-topos --  Differential cohomology</a>. By the discussion at <a href="http://nlab.mathforge.org/nlab/show/smooth%20infinity-groupoid#StrucFlat">smooth ∞-groupoid -- Flat cohomology</a> we have that $\pi_0 \mathbf{H}(Y, \mathbf{\flat} \mathbf{B}^3 U(1)) \simeq H^3(Y,U(1))$, where on the right we have [[ordinary cohomology]] (for instance realized as [[singular cohomology]]). Finally observe that $\pi_0 \mathbf{H}(Y, \mathbf{E}_8) \simeq \pi_0 \mathbf{H}(Y.\mathbf{B}^3 U(1))$, by the [above remark](#NatureOfE8). Therefore after passing to [[0-connected|connected components]] by applying $\pi_0(-)$ we get on cohomology

$$
  \array{
    H^3(Y, U(1)) & \stackrel{\cdot 2}{\to}& H^3(Y, U(1)) &\to& {*}
    \\
    \downarrow && \downarrow && \downarrow^{\mathrlap{0}} 
    \\
    \pi_0 C Field(Y) 
     &\stackrel{\hat \chi}{\to}& 
    \mathbf{H}_{diff}^4(Y)
     &\stackrel{\omega}{\to}&
     H^4_{dR}(Y)
    \\
    \downarrow && \downarrow && \downarrow
    \\
    H^1(Y, E_8)
    & \stackrel{\cdot 2}{\to}&
    H^4(Y, \mathbb{Z})  
    &\stackrel{curv}{\to}&
    H^4_{dR}(Y)
  }
$$

by reasoning as discussed at [[fiber sequence]]. In parallel to the familiar [[short exact sequence]] for [[ordinary differential cohomology]] 

$$
  * \to H^3(Y, U(1)) \to H^4_{diff}(Y) \to H^4_{dR}(Y)_{\mathbb{Z}} \to *
  \,.
$$


this therefore implies also the [[short exact sequence]]

$$
  * \to H^3(Y, U(1)) \to \pi_0 C Field \to H^4_{dR}(Y)_{2 \mathbb{Z}} \to *
  \,.
$$

Next we redo the entire discussion after applying the [[loop space object]]-construction to everything. Using that

$$
  \Omega \mathbf{H}(Y, \mathbf{B}Q) \simeq
 \mathbf{H}(Y, \Omega \mathbf{B}Q)
  \simeq 
 \mathbf{H}(Y, Q)
$$

on general grounds (see [[fiber sequence]] for details) and that also 

$$
  \Omega (\mathbf{\flat}\mathbf{B}^n U(1)) \simeq \mathbf{\flat}\mathbf{B}^{n-1} U(1)
$$ 

and 

$$
  \Omega (\mathbf{\flat}_{dR}\mathbf{B}^n U(1)) \simeq \mathbf{\flat}_{dR}\mathbf{B}^{n-1} U(1)
$$ 

(since $\mathbf{\flat}$ and $\mathbf{\flat}_{dR}$ are [[right adjoint|right]] [[adjoint (∞,1)-functor]]s -- by the discussion at [[cohesive (∞,1)-topos]] -- and hence commute with the [[(∞,1)-pullback]] that defines $\Omega$), we have then the looped [[pasting]] [[diagram]] of [[(∞,1)-pullback]]s

$$
  \array{
    \Omega C Field(Y)_{P_{Spin}} 
     &\stackrel{\Omega \hat \chi}{\to}& 
    \mathbf{H}_{flat}(Y, \mathbf{B}^2 U(1))
     &\stackrel{\omega}{\to}&
     *
    \\
   \downarrow && \downarrow && \downarrow
   \\
   \mathbf{H}(Y, E_8)
    &\stackrel{2\Omega \mathbf{c}_2}{\to}&
   \mathbf{H}(Y, \mathbf{B}^2 U(1))
    &\stackrel{curv}{\to}&
   \mathbf{H}(Y, \mathbf{\flat}_{dR} \mathbf{B}^3 U(1))
  }
  \,.
$$

Observe that $E_8$ here is a smooth but [[0-truncated]] object: so that 

$$
  \mathbf{H}(Y, E_8) \simeq H^0(Y, E_8) = C^\infty(Y, E_8)
$$

is the set of smooth functions $Y \to E_8$ (to be thought of as the the set of [[gauge transformation]]s from the trivial $E_8$-[[principal bundle]] on $Y$ to itself). 


=--





#### Presentation by differential form data
  {#CWPresentationByDifferentialFormData}

In order to compute the $(\infty,1)$-pullback $C Field(X)$ more explicitly, we follow the discussion at  [[differential string structure]], where presentations of this pullback in terms of [[simplicial presheaves]] arising from  [[Lie integration]] is given.

Write now

$$
  \mathfrak{g} := \mathfrak{e}_8 \times \mathfrak{e}_8 \times \mathfrak{so}(10,1)
$$

for the [[Lie algebra]] of $G := E_8 \times E_8 \times Spin(10,1)$ and write

$$
  \mu := \mu_{\mathfrak{e}_8} + \mu_{\mathfrak{e}_8} - \mu_{\mathfrak{so}(10,1)}
$$

for the sum of the canonical [[Lie algebra cohomology|Lie algebra cocycles]] in [[transgression]] with the respective [[Killing form]] [[invariant polynomial]]s.

Write

$$
  \mathfrak{e}_8 \times \mathfrak{so}(10,1) 
   \to \mathfrak{g}
$$

for the canonical [[diagonal]] embedding
Write 

$$
  \array{
    \mathbf{c} := 
    &
    \mathbf{cosk}_3(
       \exp(\mathfrak{e}_8 \times \mathfrak{so}(10,1))
    )
    &\stackrel{\Delta}{\to}&
    \mathbf{cosk}_3(
       \exp(\mathfrak{g})
    )
     &
      \stackrel{\exp(\mu)}{\to}
     &
    \mathbf{B}^3 U(1)_c
    \\
    \downarrow^{\simeq} 
     \\
     \mathbf{B}G
  }
$$

for the corresponding smooth [[characteristic class]]. See [[∞-Chern-Weil homomorphism]] for details. By the discussion there we present 
$\hat \mathbf{c}$ by

$$
  \array{
    \mathbf{cosk_3} \exp(b \mathbb{R} \to \mathfrak{g}_\mu)_{diff}
    &\to&
    \mathbf{B}^4 \mathbb{R}_{dR}
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbf{B}E_8
  }
  \,.
$$

By the discussion at [[differential string structure]] we have that the top morphism is a [[fibration]] in the global projective [[model structure on simplicial presheaves]] $[CartSp^{op}, sSet]_{proj}$ (there it is shown that the analogous morphism out of $\mathbf{cosk_3} \exp(b \mathbb{R} \to \mathfrak{e}_8)_{ChW}$ is a fibration, but then so is this one, because the components on the left are the same but with fewer conditions on them, so that the lifts that existed before still exist here).

Over some $U \in$ [[CartSp]] and $[k] \in \Delta$ we have that $\exp(b^\mathbb{R} \to \mathfrak{g}_\mu)_{diff}$ is given by differential form data

$$
  \left(
    \array{ 
      F_A =& d A + \frac{1}{2}[A \wedge A]
      \\
      C_3 =& \nabla B := d B + CS(A) - H_3 
      \\
      \mathcal{G}_4  =& d H_3
      \\
      d F_A =& - [A \wedge F_A]
      \\
      d C_3 =&  \langle F_A \wedge F_A\rangle - \mathcal{G}_4
      \\
      d \mathcal{G}_4 =& 0
    }
  \right)_i
  \;\;\;\;
  \stackrel{
    \array{
       t^a & \mapsto A^a
       \\
       r^a & \mapsto F^a_A
       \\
       b & \mapsto B
       \\
       c & \mapsto C_3
       \\
       h & \mapsto H_3
       \\
       g & \mapsto \mathcal{G}_4
    }
  }{\leftarrow}|
  \;\;\;\;
  \left(
    \array{  
       r^a  =& d t^a + \frac{1}{2}C^a{}_{b c} t^b \wedge t^c + 
       \\
       c = & d b + cs - h     
       \\
       g  =& d h
       \\
       d r^a  =&  - C^a{}_{b c} t^b \wedge r^a
       \\
       d c =& \langle -,-\rangle - g 
       \\
       d g =&  0 
    }
  \right)
$$

on $U \times \Delta^k$. Here, recall, $A$ takes values in $\mathfrak{g} = \mathfrak{e}_8 \times \mathfrak{e} \times \mathfrak{so}(10,1)$, so that for instance the $\mathcal{G}_4$-curvature is in detail given by

\[
  \label{TheFourCurvature}
  \mathcal{G}_4
  =
  d H_3  
  = 
  \langle F_{A^L_{\mathfrak{e}_8}} \wedge F_{A^L_{\mathfrak{e}_8}} \rangle
  + 
  \langle F_{A^R_{\mathfrak{e}_8}} \wedge F_{A^R_{\mathfrak{e}_8}} \rangle
  -
  \langle F_{\omega} \wedge F_{\omega} \rangle
  -
  d C_3
  \,,
\]

where $\omega$ denotes the [[spin connection]].

Let $\{U_i \to X\}$ be a differentiably [[good open cover]]. We hit all connected components of $\mathbf{H}(X, \mathbf{B}G)$ by considering in 

$$
  [CartSp^{op}, sSet](C(U_i), \exp(b \mathbb{R} \to \mathfrak{g}_\mu))_{diff}
$$

those cocycles that

* involve genuine $G$-[[connection on a bundle|connections]] (as opposed to the more general [[pseudo-connection]]s that are also contained);

* have a globally defined $C_3$-form.

Write therefore $(P, \nabla, C_3)$ for such a cocycle. 

For gauge transformations between two such pairs, parameterized by the above form data patchwise on  $U \times \Delta^1$, the fact that $\mathcal{G}_4$ vanishes on $\Delta^1$ implies the <a href="http://nlab.mathforge.org/nlab/show/infinity-Chern-Weil+theory+introduction#InfGaugeTrafo">infinitesmal gauge transformation</a> law

$$
  \frac{d}{d t} C = d_U \omega_t 
   + \iota_t \langle F_{\hat A} \wedge F_{\hat A}\rangle
  \,,
$$

where $\hat A\in \Omega^1(U \times \Delta^1, \mathfrak{e}_8)$ is the shift of the 1-forms. This integrates to

\[
  \label{CGaugeTransformation}
  C_2 = C_1 + d \omega + CS(\nabla_1,\nabla_2)
  \,,
\]

where 

* $\omega := \int_{\Delta^1} \omega_t$

* $CS(\nabla_1, \nabla_2) = \int_{\Delta^1} \langle F_{\hat \nabla} \wedge F_{\hat \nabla}\rangle $ is the relative [[Chern-Simons form]] corresponding to the shift of $G$-connection.



#### Restriction to the boundary
  {#RestrictionToBoundaryInChernWeil}

We have seen that $C Field(Y)$ is the 3-groupoid of those [[Cech cohomology|Cech cocycles]] on $Y$ with coefficients in $\exp(b \mathbb{R} \to \mathfrak{g}_\mu)_{diff}$ such that the curvature 4-form $\mathcal{G}_4$ has a fixed globally defined value. 

Consider the [[subobject]] 

$$
  \exp(b \mathbb{R} - \mathfrak{g}_\mu)_{diff}^{C = 0}
  \hookrightarrow
  \exp(b \mathbb{R} - \mathfrak{g}_\mu)_{diff}
$$

of the [[simplicial presheaf]] $\exp(b \mathbb{R} \to \mathfrak{g}_\mu)$ on those [[object]]s and [[k-morphism]]s for which $C = 0$.

By the [[gauge transformation]] law (eq:CGaugeTransformation)

$$
  C_2 = C_1 + d \omega + CS(A_1, A_2)
$$

this means that this picks those [[morphism]]s for which the [[Chern-Simons form]] vanishes

$$
  CS(A_1,A_2) = \int_{\Delta^1} \langle F_{A} \wedge F_{A}\rangle 
  = 0
  \,,
$$

where $A = A_U + \lambda d t \in \Omega^1(U \times \Delta^1, \mathfrak{g})$ is the 1-form datum (with $t$ the canonical coordinate on the 1-[[simplex]] $\Delta^1 = [0,1]$).

+-- {: .num_note #NatureOfGaugedCSForm}
###### Note

In the literature often the relative [[Chern-Simons form]] is considered for "ungauged" paths of connections: for $\lambda = 0$ in the above formula, hence for a $\mathfrak{g}$-valued 1-form on $U \times \Delta^1$ with no leg along the simplex (only depending on the simplex coordinate). Here, however, it is crucially important that we consider the general "gauged" paths.

=--

Notice that on the [[semisimple Lie algebra]] and [[compact Lie algebra]] $\mathfrak{e}_8$ the [[Killing form]] $\langle -,-\rangle$ is non-degenerate and positive definite (or negative definite, depending on convention). The latter condition means that this integral vanishes precisely if

$$
  \iota_{\partial_t} \langle F_A \wedge F_A \rangle = 0
  \,.
$$

This is the case on paths for which $\iota_t F_A = 0 $, but this are exactly the paths that induce genuine [[gauge transformation]]s between $A_1$ and $A_2$, where 

$$
  \frac{d}{d t} A = d_U \lambda + [\lambda , A]
  \,.
$$

This means that cocycles with coefficients in this subobject for $C = 0$ are cocycles as described at [[differential string structure]], exhibiting the [[Green-Schwarz mechanism]] on the heterotic boundary, witnessed by the restriction of the curvature equation (eq:TheFourCurvature) to vanishing $C$-field

\[
  d H_3^L  
  = 
  \langle F_{A^L_{\mathfrak{e}_8}} \wedge F_{A^L_{\mathfrak{e}_8}} \rangle
  -
  \frac{1}{2}\langle F_{\omega} \wedge F_{\omega} \rangle
\]

### Model by twisted Cohomotopy
 {#ModelByTwistedCohomotopy}

It turns out that the [[shifted C-field flux quantization condition]] is naturally implied ([FSS1 19b, Prop. 4.12](#FSS19b)) by the requirement that $G_4$ is the differential form datum underlying, via [[Sullivan model|Sullivan's theorem]], a [[cocycle]] in unstable [[J-homomorphism|J-]] [[twisted Cohomotopy]] in degree 4 ([[schreiber:Hypothesis H]]).


## Related concepts

* [[electromagnetic field]] ("$A$-field")

* [[Kalb-Ramond field]] ("$B$-field") 

* **supergravity $C$-field**

  * [[C-field tadpole cancellation]]

* [[twisted differential c-structure]]

  * [[differential string structure]]

  * [[differential fivebrane structure]]

  * [[differential T-duality]]

[[!include table of branes]]

## References
 {#References}

The C-field in [[D=11 supergravity]] originates as the $A_{\mu\nu\rho}$-field in 

* {#CremmerJuliaScherk78} [[Eugene Cremmer]], [[Bernard Julia]], [[Joël Scherk]], _Supergravity in theory in 11 dimensions_, Phys. Lett. 76B (1978) 409 (<a href="https://doi.org/10.1016/0370-2693(78)90894-8">doi:10.1016/0370-2693(78)90894-8</a>)

Re-derivation in the [[D'Auria-Fré formulation of supergravity]]:

* {#DAuriaFre82}  [[Riccardo D'Auria]], [[Pietro Fré]], (5.11b) of: _[[GeometricSupergravity.pdf:file]]_, Nuclear Physics B201 (1982) 101-140 (<a href="https://doi.org/10.1016/0550-3213(82)90376-5">doi:10.1016/0550-3213(82)90376-5</a>,  [[GeometricSupergravityErrata.pdf:file]]) 

Review in:

* {#CastellaniDAuriaFre} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], III.8.53 of: _[[Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991)

* [[André Miemiec]], [[Igor Schnakenburg]], Section 3.1.3 of: _Basics of M-Theory_, Fortsch. Phys. 54 (2006) 5-72 ([arXiv:hep-th/0509137](http://arxiv.org/abs/hep-th/0509137), [doi:10.1002/prop.200510256]( https://doi.org/10.1002/prop.200510256))


The [[shifted C-field flux quantization condition]] was originally proposed in

* {#Witten96a} [[Edward Witten]], _On Flux Quantization In M-Theory And The Effective Action_, J. Geom. Phys. 22:1-13, 1997 ([arXiv:hep-th/9609122](https://arxiv.org/abs/hep-th/9609122))

* {#Witten96b} [[Edward Witten]], _Five-Brane Effective Action In M-Theory_, J. Geom. Phys. 22:103-133, 1997 ([arXiv:hep-th/9610234](https://arxiv.org/abs/hep-th/9610234))

Proposals to model the condition by a [[Wu class]]-shifted variant of [[ordinary differential cohomology]] include the following:

* {#DiaconescuFreedMoore03} E. Diaconescu, [[Dan Freed]], [[Greg Moore]],  _The $M$-theory 3-form and $E_8$-gauge theory_, chapter in [[Haynes Miller]], [[Douglas Ravenel]] (eds.) _Elliptic Cohomology Geometry, Applications, and Higher Chromatic Analogues_, Cambridge University Press 2007 ([arXiv:hep-th/0312069](http://arxiv.org/abs/hep-th/0312069), [doi:10.1017/CBO9780511721489](https:
//doi.org/10.1017/CBO9780511721489))


A detailed discussion of the [[quantum anomaly]] of the supergravity C-field -- and its cancellation -- is in

* {#FreedMoore04} [[Dan Freed]], [[Greg Moore]], _Setting the [[quantum integrand]] of M-theory_, Communications in Mathematical Physics, Volume 263, Number 1, 89-132, ([arXiv:hep-th/0409135](http://arxiv.org/abs/hep-th/0409135), [doi:10.1007/s00220-005-1482-7](https://doi.org/10.1007/s00220-005-1482-7))
 

A summary and review of this is in 

* [[Greg Moore]], _Anomalies, Gauss laws, and Page charges in M-theory_ ([arXiv:hep-th/0409158](http://arxiv.org/abs/hep-th/0409158))

The discussion in [[twisted differential c-structures|twisted nonabelian differential cohomology]] is given in

* {#FSS12} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]],  _[[schreiber:The moduli 3-stack of the C-field]]_, Communications in Mathematical Physics, Volume 333, Issue 1 (2015), Page 117-151, ([arXiv:1202.2455](http://arxiv.org/abs/1202.2455), [DOI 10.1007/s00220-014-2228-1](http://link.springer.com/article/10.1007%2Fs00220-014-2228-1))

* {#FiSaSc} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:7d Chern-Simons theory and the 5-brane|M5-branes, String 2-connections, and 7d nonabelian Chern-Simons theory]]_ Advances in Theoretical and Mathematical Physics, Volume 18, Number 2 (2014) p. 229?321   ([arXiv:1201.5277](http://arxiv.org/abs/1201.5277), [doi:10.4310/ATMP.2014.v18.n2.a1](https://dx.doi.org/10.4310/ATMP.2014.v18.n2.a1))

Discussion with [[Dirac charge quantization]] of the C-field in [[twisted Cohomotopy]]:

* {#FSS19b} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Twisted Cohomotopy implies M-theory anomaly cancellation]]_ ([arXiv:1904.10207](https://arxiv.org/abs/1904.10207))

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Twisted Cohomotopy implies M5 WZ term level quantization]]_ ([arXiv:1906.07417](https://arxiv.org/abs/1906.07417))

and in [[equivariant Cohomotopy]]:

* [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Equivariant Cohomotopy implies orientifold tadpole cancellation]]_ ([arXiv:1909.12277](https://arxiv.org/abs/1909.12277))
 

Discussion of the dual 6-form field to the 3-form C-field (required notably in the context of [[exceptional generalized geometry]]) includes

* [[Eugene Cremmer]], [[Bernard Julia]], H. Lu, [[Christopher Pope]], _Dualisation of Dualities, II: Twisted self-duality of doubled fields and superdualities_, Nucl.Phys.B535:242-292,1998 ([arXiv:hep-th/9806106](http://arxiv.org/abs/hep-th/9806106))

* [[Eric Bergshoeff]], Mees de Roo, [[Olaf Hohm]], _Can dual gravity be reconciled with E11?_, 	Phys.Lett.B675:371-376,2009 ([arXiv:0903.4384](http://arxiv.org/abs/0903.4384))

Discussion of [[discrete torsion]] ([[orbifold]] [[equivariant cohomology|equivariance]]) for [[circle n-bundle|circle 3-bundles]] describing the [[supergravity C-field]] is discussed in

* [[Eric Sharpe]], _Analogues of Discrete Torsion for the M-Theory Three-Form_, Phys.Rev. D68 (2003) 126004 ([arXiv:hep-th/0008170](https://arxiv.org/abs/hep-th/0008170))

* Shigenori Seki, _Discrete Torsion and Branes in M-theory from Mathematical Viewpoint_, Nucl.Phys. B606 (2001) 689-698 ([arXiv:hep-th/0103117](https://arxiv.org/abs/hep-th/0103117))

and applied to discussion of [[black brane|black]] [[M2-brane]] [[worldvolume]] [[field theory]] ([[ABJM model]]) in

* [[Ofer Aharony]], Oren Bergman, Daniel Louis Jafferis, _Fractional M2-branes_, JHEP 0811:043,2008 ([arXiv:0807.4924](https://arxiv.org/abs/0807.4924))

* [[Mauricio Romo]], _Aspects of ABJM orbifolds with discrete torsion_, J. High Energ. Phys. (2011) 2011 ([arXiv:1011.4733](https://arxiv.org/abs/1011.4733))


[[!redirects C3-field]]
[[!redirects C-field]]

[[!redirects supergravity C-fields]]