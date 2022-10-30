

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In abstractly generality, a _differential cohomology diagram_ is the hexagonal [[diagram]] in a [[cohesive (∞,1)-topos]] formed by the two [[fracture squares]] of the [[unit of a monad|unit]] and [[counit of a comonad|counit]] of, respectively, the [[shape modality]] $\Pi$ and the [[flat modality]] $\flat$. The exactness properties of this diagram for any [[stable homotopy type]] $\hat E$ in the corresponding [[tangent cohesive (∞,1)-topos]] express $\hat E$ as being the [[coefficients]] for a [[differential cohomology]] refinement by differential form data $\flat_{dR} \Sigma \hat E$ of the [[generalized (Eilenberg-Steenrod) cohomology theory]] which is [[Brown representability theorem|represented]] by the [[shape modality|shape]] [[spectrum]] $E \coloneqq \Pi(\hat E)$.

Historically, it had been shown in ([Simons-Sullivan 07](#SimonsSullivan07)) for [[ordinary differential cohomology]] and in ([Freed-Lott 10](#FreedLott10), [Simons-Sullivan 08](#SimonsSullivan08)) for [[differential K-theory]] that these cohomology theories are characterized as sittin in the middle of a hexagonal [[diagram]] of interlocking [[exact sequences]] of [[cohomology groups]], which expresses on the one hand how every differential cohomology class has underlying it a non-differential cohomology class ("of a [[principal ∞-bundle]]") as well as a [[curvature]] [[differential form]] datum, and on the other hand how the special cases of trivial underlying classes equipped with differential form datum and of [[flat connection|flat]] differential form data sit inside the differential cohomology classes.

At this schematic conceptual level a differential cohomology diagram looks as follows

$$
  \array{
    &&  connection\;on\;trivial\;bundle && \stackrel{de\;Rham\;differential}{\longrightarrow} && differential\;forms
    \\
    & \nearrow & & \searrow & & \nearrow_{curvature} && \searrow
    \\
    flat\;differential\;forms  && && geometric\;bundle\;with \;connection && && rationalized\;bundle
    \\
    & \searrow &  & \nearrow & & \searrow^{\mathrlap{}} && \nearrow_{\mathrlap{Chern\;character}}
    \\
    && geometric\;bundle\;with\;flat\;connection && \underset{}{\longrightarrow} && shape\;of\;bundle
  }
$$

One characteristic property is that the two outer sequences are [[exact sequences]]. This expresses (at this rough schematic level) for instance (for the upper part) that the connections $A$ on trivial bundles whose curvature vanishes in that $\mathbf{d}A = 0$, are exactly the flat connections; as well as (for the lower part) that bundles with [[flat connections]] have [[torsion subgroup|torsion]] Chern-clases.

So a [[differential cohomology]] theory would be one whose [[cocycles]]/[[cohomology classes]] have the interpretation of (stable) [[principal ∞-bundles]] with [[connection on an ∞-bundle|connection]] such as in the middle of this diagram.

The characterization/construction of [[differential cohomology]] via [[homotopy fiber products]] (of [[mapping spectra]] with [[differential form]] data) due to ([Hopkins-Singer 02](#HopkinsSinger02)) provides an incarnation of this kind of diagram genuinely in [[stable homotopy theory]], so that the outer parts are indeed [[homotopy fiber sequences]] and the two squares are homotopy cartesion (are [[homotopy pullbacks]]/[[homotopy pushouts]]).

In ([Bunke-Nikolaus-V&#246;lkl 13](#BunkeNikolausVoelkl13)) it was observed (see [Schreiber 13, section 4.1.2](#Schreiber13) for the generality in which we present this here) that every [[stable homotopy type]] $\hat E$ in a [[cohesive (∞,1)-topos]] $\mathbf{H}$ canonically sits inside a diagram of this form, being formed from the [[fracture squares]] of the units and counits of the [[shape modality]] $\Pi$ and the [[flat modality]] $\flat$:

$$
  \array{
    &&  \Pi_{dR} \Omega {\hat E} && \longrightarrow && \flat_{dR}\Sigma {\hat E}
    \\
    & \nearrow & & \searrow & & \nearrow_{\mathrlap{\theta_{\hat E}}} && \searrow
    \\
    \flat \Pi_{dR} \Omega {\hat E}  && && {\hat E} && && \Pi \flat_{dR} \Sigma \hat E
    \\
    & \searrow &  & \nearrow & & \searrow && \nearrow_{\mathrlap{\Pi \theta_{\hat E}}}
    \\
    && \flat {\hat E} && \longrightarrow && \Pi \hat E
  }
  \,.
$$

For the special case that $\mathbf{H} = T Smooth\infty Grpd$ is the [[tangent (∞,1)-topos]] of [[smooth ∞-groupoids]] ([[∞-stacks]] over the [[site]] of [[smooth manifolds]]) this subsumes the cases mentioned above. But there are many examples of cohomology theories not of the form of ([Hopkins-Singer 02](#HopkinsSinger02)) but represented by [[stable homotopy types]] in a [[cohesive (∞,1)-topos]] (see [Schreiber 13](#Schreiber13), [BunkeNikolausV&#246;lkl 13](#BunkeNikolausVoelkl13)) and hence fitting into such a diagram, where the interpretation of the pieces of the diagram is just as it should be. 

Therefore it makes sense to define generally that a _differential cohomology diagram_ is the above combined [[fracture squares]] with its outer [[homotopy fiber sequences]] for [[shape modality]] and [[flat modality]] in any [[cohesive (∞,1)-topos]].

## Definition/Construction

Let $\mathbf{H}$ be a [[cohesive (∞,1)-topos]], write $T\mathbf{H}$ for its [[tangent cohesive (∞,1)-topos]] and write $T_\ast \mathbf{H}$ for the [[stable (∞,1)-category]] of [[spectrum objects]] inside it.

Write $\Pi$ for the _stabilized_ [[shape modality]] and $\flat$ for the [[flat modality]] of $Stabl(\mathbf{H}) \hookrightarrow  T \mathbf{H}$, respectively. Write $\flat_{dR}$ for the [[homotopy fiber]] of the $\flat$-[[counit of a comonad|counit]] and $\Pi_{dR}$ for the [[homotopy cofiber]] of the [[unit of a monad|unit]] of $\Pi$. Write 

$$
  \theta \;\colon\; \Omega \longrightarrow \flat_{dR} 
$$

for the canonical morphism (itself the [[homotopy fiber]] of $\flat_{dR} \to \flat$) which has the interpretation of being the [[Maurer-Cartan form]].

+-- {: .num_prop}
###### Proposition


For every $A \in T_\ast \mathbf{H}$ the [[natural transformation|naturality square]] 

$$
  \array{
    A &\stackrel{}{\longrightarrow}& A/\flat A
    \\
    \downarrow &{}^{(pb)}& \downarrow
    \\
    \Pi(A) &\stackrel{}{\longrightarrow}& \Pi(A/\flat A)
  }
$$

(of the [[shape modality]] applied to the [[homotopy cofiber]] of the [[counit of a comonad|counit]] of the [[flat modality]]) is an [[(∞,1)-pullback]] square.

=--

This was observed in ([Bunke-Nikolaus-V&#246;lkl 13](#BunkeNikolausVoelkl13)). It is an incarnation of a [[fracture theorem]].

+-- {: .proof}
###### Proof 

By [[cohesive (infinity,1)-topos|cohesion]] and [[stable (infinity,1)-category|stability]] we have the diagram

$$
  \array{
    \flat A &\longrightarrow & A &\stackrel{}{\longrightarrow}& A/\flat A
    \\
    \downarrow^{\mathrlap{\simeq}} && \downarrow && \downarrow
    \\
    \Pi(\flat A) &\longrightarrow& \Pi(A) &\stackrel{}{\longrightarrow}& \Pi(A/\flat A)
  }
$$

where both rows are [[homotopy fiber sequences]]. By [[cohesive (infinity,1)-topos|cohesion]] the left vertical map is an [[equivalence in an (infinity,1)-category|equivalence]]. The claim now follows with the [homotopy fiber characterization](homotopy+pullback#HomotopyFiberCharacterization) of [[homotopy pullbacks]].

=--

+-- {: .num_remark}
###### Remark


This means that in stable cohesion every cohesive stable homotopy type is in controled sense a cohesive extension/refinement of its [[geometric realization of cohesive infinity-groupoids|geometric realization]] [[discrete infinity-groupoid|geometrically discrete]] ("bare") stable [[homotopy type]] by the non-[[discrete object|discrete]] part of its cohesive structure;

In particular, $A/\flat A$ may be identified with differential cycle data. Indeed, by stability and cohesion it is the [flat de Rham coefficient object](cohesive+%28infinity,1%29-topos+--+structures#deRhamCohomology)


$$
  A/\flat A = \flat_{dR}\Sigma A
$$

of the [[suspension]] of $A$, and the map to this quotient is thus the [[Maurer-Cartan form]] $\theta_A$. So

$$
  \array{
    A &\stackrel{\theta_A}{\longrightarrow}& \flat_{dR}\Sigma A
    \\
    \downarrow &{}^{(pb)}& \downarrow
    \\
    \Pi(A) &\stackrel{}{\longrightarrow}& \Pi(A/\flat A)
  }
$$

exhibits $A$ as a [[differential cohomology]]-coefficient of the [[generalized cohomology theory]] $\Pi(A)$.

It follows by the discussion at [[schreiber:differential cohomology in a cohesive topos]] that the further differential refinement $\hat{A}$ of $A$ should be given by a further [[homotopy pullback]]

$$
  \array{
    \hat{A} &\longrightarrow& \Omega^1(-,Lie(A))
    \\
    \downarrow &{}^{(pb)}& \downarrow
    \\
    A &\stackrel{\theta_A}{\longrightarrow}& \flat_{dR}\Sigma A
    \\
    \downarrow &{}^{(pb)}& \downarrow
    \\
    \Pi(A) &\stackrel{}{\longrightarrow}& \Pi(A/\flat A)
  }
  \,.
$$

But of course by the generality of the above  proposition, such an $\hat{A}$ sits itself again in its fracture-like pullback diagram.

=--

Dually:

+-- {: .num_prop}
###### Proposition

For every $A \in T_\ast \mathbf{H}$ the [[natural transformation|naturality square]] 

$$
  \array{
    \flat(\Pi_{dR} \Sigma^{-1} A) &\longrightarrow & \Pi_{dR}(\Sigma^{-1} A)
    \\
    \downarrow && \downarrow
    \\
    \flat A &\stackrel{}{\longrightarrow}& A 
  }
$$

(of the [[flat modality]] applied to the [[homotopy fiber]] of the [[unit of a monad|unit]] of the [[shape modality]]) is an [[(∞,1)-pullback]] square.

=--

+-- {: .proof}
###### Proof 

As before but dually, the diagram extends to a morphism of 
[[homotopy cofiber]] diagrams of the form

$$
  \array{
    \flat(\Pi_{dR} \Sigma^{-1} A) &\longrightarrow & \Pi_{dR}(\Omega A)
    \\
    \downarrow && \downarrow
    \\
    \flat A &\stackrel{}{\longrightarrow}& A 
    \\
    \downarrow && \downarrow 
    \\
    \flat \Pi(A) &\stackrel{\simeq}{\longrightarrow}& \Pi(A) 
  }
  \,,
$$

and by [[cohesion]] the bottom horizontal morphism is an [[equivalence in an (infinity,1)-category|equivalence]].

=--

Combining these two statements yields the following ([Bunke-Nikolaus-V&#246;lkl 13](#BunkeNikolausVoelkl13)).

+-- {: .num_cor #TheDifferentialDiagram}
###### Corollary

For $\mathbf{H}$ a [[cohesive (∞,1)-topos]]
every [[stable homotopy type]] $A \in Stab(\mathbf{H}) \hookrightarrow T \mathbf{H}$ sits inside a [[diagram]] of the form

$$
  \array{
    &&  \Pi_{dR} \Omega A && \longrightarrow && \flat_{dR}\Sigma A
    \\
    & \nearrow & & \searrow & & \nearrow_{\mathrlap{\theta_A}} && \searrow
    \\
    \flat \Pi_{dR} \Omega A  && && A && && \Pi \flat_{dR}\Sigma A
    \\
    & \searrow &  & \nearrow & & \searrow && \nearrow_{\mathrlap{\Pi \theta_A}}
    \\
    && \flat A && \longrightarrow && \Pi A
  }
  \,,
$$

where the two squares are [[homotopy pullback]] squares, the two diagonals are the [[fiber sequences]] of the [[Maurer-Cartan form]] $\theta_A$ and its dual and the top and bottom outer sequences are [[homotopy fiber sequences]].

=--

+-- {: .proof}
###### Proof 

One the last statement remains to be observed, for that use the [[pasting law]]. For instance that $\Pi_{dR}\Omega A \to \flat_{dR}\Sigma A \to \Pi \flat_{dR}\Sigma A$ is a [[homotopy fiber sequence]] follows since by the fact that the right square in the hexagon is a [[homotopy pullback]] this is equivalently the top-right part of the following pasting diagram of [[homotopy pullbacks]]:

$$
  \array{
    \Pi_{dR} \Omega A  &\to& A &\to& \flat_{dR} \Sigma A
    \\
    \downarrow && \downarrow
    \\
    0 &\to& \Pi A &\to& \Pi \flat_{dR}\Sigma A
  }
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

The bottom horizontal morphisms in the diagram in prop. \ref{TheDifferentialDiagram} are the canonical [points-to-pieces transform](cohesive%20topos#CanonicalComparison).

=--


## References

The differential cohomology hexagon was maybe first highlighted in the context of [[ordinary differential cohomology]]

* {#SimonsSullivan07} [[James Simons]], [[Dennis Sullivan]], _Axiomatic Characterization of Ordinary Differential Cohomology_ ([arXiv:math/0701077](http://arxiv.org/abs/math/0701077))

and in the context of [[differential K-theory]] in 

* {#SimonsSullivan08} [[James Simons]], [[Dennis Sullivan]], _Structured vector bundles define differential K-theory_ ([arXiv:0810.4935](http://arxiv.org/abs/0810.4935))

proven also in

* {#FreedLott10} [[Daniel Freed]], [[John Lott]], _An index theorem in differential K-theory_, Geometry and Topology 14 (2010) ([pdf](http://math.berkeley.edu/~lott/gt-2010-14-021p.pdf))


An artistic impression of the differential cohomology hexagon as a dance choreography inspired by a talk by [[James Simons]] is at

* Kyla Barkin, Aaron Selissen, _Differential Cohomology_, 2011 ([full video (37 min)](http://vimeo.com/32903887), [sequence of "The March Back" (4 min)](http://www.dancemedia.com/v/7044), [press release](http://www.businessinsider.com/jim-simons-mathematical-genius-inspired-a-ballet-2011-1))

That the differential cohomology hexagon exists not just at the level of [[exact sequences]] of [[cohomology classes]] but already at the level of [[homotopy fiber sequences]] of [[cocycle]] spaces was observed for [[ordinary differential cohomology]] and for [[differential K-theory]] in 

* Man-Ho Ho, _Refined hexagons for differential cohomology_ ([arXiv:1310.0582](http://arxiv.org/abs/1310.0582))

That generally the [[homotopy fiber product]]-construction of differential refinements of [[generalized (Eilenberg-Steenrod) cohomology]] theories due to

* {#HopkinsSinger02} [[Mike Hopkins]] and [[Isadore Singer]], _[[Quadratic Functions in Geometry, Topology,and M-Theory]]_ ([arXiv:math/0211216](http://arxiv.org/abs/math/0211216))

constitutes the right one of the two squares in the homotopy-theoretic version of the diagram is discussed explicitly for instance in prop 4.57 of

* {#Bunke12} [[Ulrich Bunke]], _Differential cohomology_ ([arXiv:1208.3961](http://arxiv.org/abs/1208.3961))

That every [[stable homotopy type]] in a [[cohesive (∞,1)-topos]] naturally sits in a differential cohomology diagram was observed (focusing on [[Smooth∞Grpd]]) in 

* {#BunkeNikolausVoelkl13} [[Ulrich Bunke]], [[Thomas Nikolaus]], [[Michael Völkl]], _Differential cohomology theories as sheaves of spectra_ ([arXiv:1311.3188](http://arxiv.org/abs/1311.3188))

following

* {#Schreiber13} [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_ ([arXiv:1310.7930](http://arxiv.org/abs/1310.7930))

where in section 4.1.2 a fully general abstract account is given.




[[!redirects differential cohomology diagrams]] 

[[!redirects differential cohomology hexagon]]