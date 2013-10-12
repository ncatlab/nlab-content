
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
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

The [[tangent (∞,1)-category]] $T\mathbf{H}$
to a [[cohesive (∞,1)-topos]] is itself cohesive: the 
_tangent cohesive (∞,1)-topos_.
This $T \mathbf{H}$ is the $\infty$-topos of [[parameterized spectra]] in $\mathbf{H}$, hence is the context for cohesive [[stable homotopy theory]].


## Properties

### Stable extension of cohesion

Let $\mathbf{H}$ be a [[cohesive (∞,1)-topos]].

By the discussion at
_[tangent ∞-category -- Examples -- Of an ∞-topos](tangent+%28infinity%2C1%29-category#TangentTopos)_):

$$
  \array{
    Stab(\mathbf{H})
    &
    \stackrel{\overset{L\Pi^{seq}}{\longrightarrow}}{\stackrel{\overset{Disc^{seq}}{\leftarrow}}{\stackrel{\overset{\Gamma^{seq}}{\longrightarrow}}{\underset{coDisc^{seq}}{\leftarrow}}}}
    &
    Stab(\infty Grpd)
    \\
    \downarrow^{\mathrlap{incl}} && \downarrow^{\mathrlap{incl}}
    \\
    T \mathbf{H}
    &
    \stackrel{\overset{L\Pi^{seq}}{\longrightarrow}}{\stackrel{\overset{Disc^{seq}}{\leftarrow}}{\stackrel{\overset{\Gamma^{seq}}{\longrightarrow}}{\underset{coDisc^{seq}}{\leftarrow}}}}
  &
  T \infty Grpd
  \\
  {}^{\mathllap{base}}\downarrow {}^{\mathllap{0}}\uparrow \downarrow^{\mathrlap{base}} \uparrow^{\mathrlap{0}}
  && 
  {}^{\mathllap{base}}\downarrow {}^{\mathllap{0}}\uparrow \downarrow^{\mathrlap{base}} \uparrow^{\mathrlap{0}}
  \\
    \mathbf{H}
    &
    \stackrel{\overset{\Pi}{\longrightarrow}}{\stackrel{\overset{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\longrightarrow}}{\underset{coDisc}{\leftarrow}}}}
  &
  \infty Grpd
  }
  \,.
$$

### Stable homotopy types

In a tangent cohesive $\infty$-topos $T \mathbf{H}$ all the [[homotopy types]] in $T_\ast \mathbf{H} \hookrightarrow T\mathbf{H}$ are [[stable homotopy types]].


### Cohomology -- Twisted bivariant generalized geometric cohomology theory
 {#Cohomology}

Where the [[(∞,1)-categorical hom-space]] in a general [[(∞,1)-topos]] constitute a notion of [[cohomology]], those of a [[tangent (∞,1)-topos]] specifically constitute [[twisted generalized cohomology]], in fact [[twisted bivariant cohomology]].

For consider a [[spectrum object]] $E \in T_\ast \mathbf{H}$ and write $GL_1(E) \in Grp(\mathbf{H})$ for its [[∞-group of units]]. Then the [[∞-action]] of this on $E$ is (by the discussion there) exhibited by an object 

$$
  \left[
   \array{
     E//GL_1(E)
     \\
     \downarrow
     \\
     \mathbf{B}GL_1(E)
   }
  \right]
  \;\;\;
   \in
  \;\;\;
  T_{\mathbf{B}GL_1(E)}\mathbf{H} \hookrightarrow T\mathbf{H}
  \,.
$$

Now for any object $X \in \mathbf{H}$ regarded as the object 

$$
  \left[
   \array{
     E \times X
     \\
     \downarrow
     \\
     X
   }
  \right]
  \;\;\;
   \in
  \;\;\;
  T_{X}\mathbf{H} \hookrightarrow T\mathbf{H}
$$

then morphisms in $T \mathbf{H}$ from the latter to the former

$$
    \left[
   \array{
     E \times X
     \\
     \downarrow
     \\
     X
   }
  \right]
  \longrightarrow
  \left[
   \array{
     E//GL_1(E)
     \\
     \downarrow
     \\
     \mathbf{B}GL_1(E)
   }
  \right]
$$

are equivalently

1. a choice of [[twisted cohomology|twist of E-cohomology]] $\chi \;\colon \; X  \longrightarrow \mathbf{B}GL_1(E)$;

1. an element in the $\chi$-twisted $E$-cohomology of $X$, hence  $c \in E^{\bullet}(X,E)$.

In particular the [[internal hom]] (with respect to the relative [[smash product]]...)

$$
  \left[
    \left[
   \array{
     E \times X
     \\
     \downarrow
     \\
     X
   }
  \right]
  \;,\;
  \left[
   \array{
     E//GL_1(E)
     \\
     \downarrow
     \\
     \mathbf{B}GL_1(E)
   }
  \right]
  \right]
  \;\;
  \in
  T_{[X,\mathbf{B}GL_1(E)]} \mathbf{H}
$$

is the [[twisted cohomology]]-[[spectrum]] [[graded object|graded]] by the type of twists.


### Cohesive and differential refinement
 {#CohesiveAndDifferentialRefinement}

Let $T\mathbf{H}$ be a tangent cohesive $(\infty,1)$-topos and write $T_\ast \mathbf{H}$ for the [[stable (∞,1)-category]] of [[spectrum objects]] inside it.

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

In particular, $A/\flat A$ may be identified with differential cycle data. Indeed, by stability and cohesion it is the [flat de Rham coefficient object](structures in a cohesive infinity-topos#deRhamCohomology)


$$
  A/\flat A = \flat_{dR}\Sigma A
$$

of the [[suspension]] of $A$. So

$$
  \array{
    A &\stackrel{\theta_A}{\longrightarrow}& \flat_{dR}\Sigma A
    \\
    \downarrow &{}^{(pb)}& \downarrow
    \\
    \Pi(A) &\stackrel{}{\longrightarrow}& \Pi(A/\flat A)
  }
$$

exhibits $A$ as a [[differential cohomology]]-coefficient of the [[generalized cohomology theory]] $\Pi(A)$ ([Bunke-Nikolaus-V&#246;lkl 13](#BunkeNikolausVoelkel13)).

=--


## Related concepts

* [[twisted generalized cohomology]]

## References

The idea of forming $T_\ast \mathbf{H}$ as a home for nontrivial [[stable homotopy types]] was originally suggested by [[Joyal]], see the references at _[[tangent (infinity,1)-topos]]_.

Discussion of [[differential cohomology]] in $T_\ast Smooth \infty Grpd \simeq Stab(Smooth \infty Grpd)$ is in

* [[Ulrich Bunke]], [[Thomas Nikolaus]], [[Michael Völkl]], to appear
  {#BunkeNikolausVoelkl13}

[[!redirects cohesive tangent (∞,1)-topos]]

[[!redirects stable cohesive homotopy theory]]
[[!redirects stable cohesive homotopy type theory]]

[[!redirects cohesive stable homotopy theory]]
[[!redirects cohesive stable homotopy type theory]]

[[!redirects tangent cohesion]]

[[!redirects stable cohesion]]
