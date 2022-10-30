
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
 {#StableExtensionOfCohesion}

Let $\mathbf{H}$ be a [[cohesive (∞,1)-topos]].

By the discussion at
_[tangent ∞-category -- Examples -- Of an ∞-topos](tangent+%28infinity%2C1%29-category#TangentTopos)_ the tangent $\infty$-topos $T \mathbf{H}$ constitutes an [[extension]] of $\mathbf{H}$ by its [[stabilization]] $Stab(\mathbf{H})$:
 
$$
  \array{
    && Stab(\mathbf{H})
    &
    \stackrel{\overset{L\Pi^{seq}}{\longrightarrow}}{\stackrel{\overset{Disc^{seq}}{\leftarrow}}{\stackrel{\overset{\Gamma^{seq}}{\longrightarrow}}{\underset{coDisc^{seq}}{\leftarrow}}}}
    &
    Stab(\infty Grpd) \simeq Spectra
    \\
    && \simeq && \simeq
    \\
    && T_\ast \mathbf{H} && T_\ast \infty Grpd
    \\
    && \downarrow^{\mathrlap{incl}} && \downarrow^{\mathrlap{incl}}
    \\
    \mathbf{H}
    &\stackrel{\overset{d}{\longrightarrow}}{\underset{\Omega^\infty \circ tot}{\leftarrow}}&
    T \mathbf{H}
    &
    \stackrel{\overset{L\Pi^{seq}}{\longrightarrow}}{\stackrel{\overset{Disc^{seq}}{\leftarrow}}{\stackrel{\overset{\Gamma^{seq}}{\longrightarrow}}{\underset{coDisc^{seq}}{\leftarrow}}}}
  &
  T \infty Grpd
  \\
  &&
  {}^{\mathllap{base}}\downarrow \uparrow^{\mathrlap{0}} 
  && 
  {}^{\mathllap{base}}\downarrow \uparrow^{\mathrlap{0}} 
  \\
  &&
    \mathbf{H}
    &
    \stackrel{\overset{\Pi}{\longrightarrow}}{\stackrel{\overset{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\longrightarrow}}{\underset{coDisc}{\leftarrow}}}}
  &
  \infty Grpd
  }
  \,.
$$

Here

* $\Omega^\infty \circ tot \;\colon\; T \mathbf{H} \longrightarrow \mathbf{H}$ assigns the _total space_ of a spectrum bundle;

  its [[left adjoint]] is the [tangent complex functor](tangent+%28infinity%2C1%29-category#CotangentComplex);

* $base \;\colon\; T \mathbf{H} \longrightarrow \mathbf{H}$ assigns the _base space_ of a spectrum bundle;

  its [[left adjoint]] produces the 0-bundle;

  together these exhibit $T \mathbf{H}$ as an [[infinitesimal cohesive (infinity,1)-topos]] over $\mathbf{H}$.



### Stable homotopy types

In a tangent cohesive $\infty$-topos $T \mathbf{H}$ all the [[homotopy types]] in $T_\ast \mathbf{H} \hookrightarrow T\mathbf{H}$ are [[stable homotopy types]].


### Cohomology -- Twisted bivariant generalized geometric cohomology theory
 {#Cohomology}

Where the [[(∞,1)-categorical hom-space]] in a general [[(∞,1)-topos]] constitute a notion of [[cohomology]], those of a [[tangent (∞,1)-topos]] specifically constitute [[twisted generalized cohomology]], in fact [[twisted bivariant cohomology]].

For consider a [[spectrum object]] $E \in T_\ast \mathbf{H}$ and write $GL_1(E) \in Grp(\mathbf{H})$ for its [[∞-group of units]]. Then the [[∞-action]] of this on $E$ is (by the discussion there) exhibited by an object 

$$
  \left(
   \array{
     E//GL_1(E)
     \\
     \downarrow
     \\
     \mathbf{B}GL_1(E)
   }
  \right)
  \;\;\;
   \in
  \;\;\;
  T_{\mathbf{B}GL_1(E)}\mathbf{H} \hookrightarrow T\mathbf{H}
  \,.
$$

More generally, for $Pic(E) \in \mathbf{H}$ the [[Picard ∞-groupoid]] of $E$ there is the universal [[(∞,1)-line bundle]]

$$
  (\widehat{Pic(E)} \to Pic(E)) \in T \mathbf{H}
  \,.
$$

Now for any object $X \in \mathbf{H}$ we have the trivial [[sphere spectrum]] [[spectrum bundle]] over $X$

$$
  X \times \mathbb{S}
  \simeq
  \left(
   \array{
     X \times \mathbb{S}
     \\
     \downarrow
     \\
     X
   }
  \right)
  \;\;\;
   \in
  \;\;\;
  T_{X}\mathbf{H} \hookrightarrow T\mathbf{H}
  \,.
$$

then morphisms in $T \mathbf{H}$ from the latter to the former

$$
    \left(
   \array{
     X \times \mathbb{S}
     \\
     \downarrow
     \\
     X
   }
  \right)
  \longrightarrow
  \left(
   \array{
     E//GL_1(E)
     \\
     \downarrow
     \\
     \mathbf{B}GL_1(E)
   }
  \right)
$$

are equivalently [[homotopy]] [[commuting diagrams]] of the form


$$
  \array{
    X \times \mathbb{S} &\stackrel{\sigma}{\longrightarrow}& E//GL_1(E)
    \\
    \downarrow && \downarrow
    \\
    X &\stackrel{\chi}{\longrightarrow}& \mathbf{B}GL_1(E)
  }
$$

and hence

1. a choice of [[twisted cohomology|twist of E-cohomology]] $\chi \;\colon \; X  \longrightarrow \mathbf{B}GL_1(E)$, modulating a $GL_1(E)$-[[principal ∞-bundle]];

1. an element in the $\chi$-twisted $E$-cohomology of $X$, $\sigma \in E^{\bullet + \chi}(X,E)$, hence a [[section]] of the [[associated ∞-bundle|associated]] [[(∞,1)-line bundle]].

If we consider the [[internal hom]] instead of the external [[(∞,1)-categorical hom space]] then things work even more nicely and we can use just $X$ instead of $X \times \mathbb{S}$:

+-- {: .num_prop #MappingSpectrumOutOfUnstableTypeAsCartesianInternalHom}
###### Proposition

For $X \in \mathbf{H} \stackrel{0}{\hookrightarrow} T \mathbf{H}$ a [[geometric homotopy type]] and $E \in Stab(\mathbf{H}) \simeq T_\ast \mathbf{H} \hookrightarrow T \mathbf{H}$ a [[spectrum object]], then the [[internal hom]]/[[mapping stack]]

$$
  [X,E]_{T \mathbf{H}} \in T \mathbf{H}
$$

(with respect to the Cartesian [[closed monoidal (∞,1)-category]] structure on the [[(∞,1)-topos]] is equivalently the [[mapping spectrum]]

$$
  [\Sigma^\infty X, E]_{Stab(\mathbf{H})} \in Stab(\mathbf{H}) \hookrightarrow T \mathbf{H}
  \,,
$$

in that 

$$
  [X,E]_{T \mathbf{H}} \simeq [\Sigma^\infty X,E]_{Stab(\mathbf{H})}
  \,.
$$

=--

+-- {: .proof}
###### Proof 

Notice that as an object of $T \mathbf{H} \hookrightarrow \mathbf{H}^{seq}$, the object $X$ is the constant [[(∞,1)-presheaf]] on $seq$. By the formula for the [[internal hom]] in an [[(∞,1)-category of (∞,1)-presheaves]] we have

$$
  [X,E]_\bullet \simeq \mathbf{H}^{seq}(X \times \bullet, E)
  \,.
$$

But since $X$ is constant the object $X \times \bullet$ is for each object of $seq$ the [[representable functor|presheaf represented]] by that object. Therefore by the [[(∞,1)-Yoneda lemma]] it follows that

$$
  [X,E]_\bullet \simeq [X,E_\bullet]
  \,.
$$

This is manifestly the same formula as for the [[mapping spectrum]] out of $\Sigma^\infty X$.

=--

Similar kind of arguments give the following more general statement.

+-- {: .num_prop}
###### Proposition

For $X \in \mathbf{H} \stackrel{0}{\hookrightarrow} T \mathbf{H}$ a [[geometric homotopy type]], for $E \in E_\infty(\mathbf{H})$ an [[E-∞ ring]]  with $(\widehat{Pic(E)} \to Pic(E)) \hookrightarrow T \mathbf{H}$ its universal [[(∞,1)-line bundle]] over its [[Picard ∞-groupoid]], then the [[internal hom]]/[[mapping stack]]

$$
  [X,\widehat{Pic(E)}]_{T \mathbf{H}} \in T \mathbf{H}
$$

is the object whose

* base homotopy type is the [[E-∞ ring]] $[X, Pic(E)]$ of $E$-[[twisted cohomology|twist]] on $X$;

* whose [[spectrum bundle]] is the collection of $\chi$-[[twisted cohomology|twisted E-cohomology spectra]] for all twists $\chi$.

=--

In full generality we may formulate the [[internal hom]] [[mapping space]] in $T \mathbf{H}$ in [[homotopy type theory]] notation as follows.

+-- {: .num_prop #InternalHomGeneral}
###### Proposition

For 

$$
  (a \colon A) \;\vdash\; E_a \colon Spectra(\mathbf{H})
$$

and

$$
  (b \colon B) \;\vdash\; F_b \colon Spectra(\mathbf{H})
$$

two [[spectrum bundle]] [[dependent type|dependent types]] over base [[homotopy types]], $A,B \colon \mathbf{H}$, respectively, then the [[function type]] $(E \to F) \colon T\mathbf{H}$ between them (regarded as [[homotopy types]] in $T \mathbf{H}$) is

$$
  \chi \colon (A \to B); \sigma \colon \underset{a \colon A}{\prod} SpMap(E_a,F_{\chi(a)})
  \;\vdash\;
  \underset{a \colon A}{\prod} F_{\chi(a)}
  \,.
$$

=--
+-- {: .proof}
###### Proof
Let $(x:X)\vdash M_x : Spectra$ be another [[spectrum bundle]].  The [[cartesian product]] $M\times E$ in $T \mathbf{H}$ is then $(x:X),(a:A) \vdash M_x \oplus E_a$, with $\oplus$ also the [[coproduct]] (hence the [[direct sum]]), since [[spectra]] are [[stable (infinity,1)-category|stable]] and hence [[additive (infinity,1)-category|additive]].  We compute the [[mapping space]] $T\mathbf{H}(M\times E,F)$ as follows:
$$
\begin{aligned}
  \sum_{(\phi:X\times A \to B)} \prod_{((x,a):X\times A)} SpMap(M_x\oplus E_a,F_{\phi(x,a)})
  &=& \sum_{(\phi:X \to A \to B)} \prod_{(x:X)} \prod_{(a:A)} SpMap(E_a,F_{\phi(x,a)}) \times SpMap(M_x,F_{\phi(x,a)})\\
  &=& \prod_{(x:X)} \sum_{(\chi:A \to B)} \left(\prod_{(a:A)} SpMap(E_a,F_{\chi(a)})\right) \times \left( \prod_{(a:A)} SpMap(M_x,F_{\chi(a)}) \right)\\
  &=& \prod_{(x:X)} \sum_{\psi : \sum_{(\chi:A \to B)} \prod_{(a:A)} SpMap(E_a,F_{\chi(a)})} SpMap\left(M_x, \prod_{(a:A)} F_{pr_1(\psi)(a)}\right)\\
  &=& \sum_{\rho : X \to \sum_{(\chi:A \to B)} \prod_{(a:A)} SpMap(E_a,F_{\chi(a)})} \prod_{(x:A)} SpMap\left(M_x, \prod_{(a:A)} F_{pr_1(\rho(x))(a)}\right)
\end{aligned}
$$
In the first line, we [[currying|curry]] $\phi$, apply the [[induction principle]] for [[dependent type|dependent]] maps out of $X\times A$, and also apply the [[universal property]] of the [[coproduct]] $M_x \oplus E_a$.  In the second line, we apply the [[universal property]] for mapping into [[∞-types]] (the "[[type-theoretic axiom of choice]]") and also that for dependent functions into a [[Cartesian product|product]].  In the third line we apply the associativity of [[∞-types]], and also the [[universal property]] for mapping into the [[dependent product]] $\prod$ of [[spectra]].  Finally, in the fourth line, we apply the [[type-theoretic axiom of choice]] again in the other direction.  The resulting [[type]] is the [[mapping space]] from $M$ to the claimed [[function type]] $(E\to F)$ defined above.  (See also [this discussion](http://nforum.mathforge.org/discussion/5321/parameterized-cohesive-spectra/?Focus=42394#Comment_42394).)
=--


+-- {: .num_example}
###### Example

We have the following special cases of prop. \ref{InternalHomGeneral}.

1. If $E_a = 0$ for all $a \colon A$, and if $B = \ast$, then the function type is

   $$
     \vdash \; \underset{a \colon A}{\prod} F
   $$

   which reproduces the [[mapping spectrum]] $SpMap(\Sigma^\infty A, F)$ from prop. \ref{MappingSpectrumOutOfUnstableTypeAsCartesianInternalHom}.

1. If $A = B = \ast$ then then the mapping type is 

   $$
     \sigma \colon SpMap(E,F) \;\vdash \; F \colon Spectra
   $$

1. If $E_a = 0$ for all $a \colon A$ and $F_b = 0$ for all $b \colon B$ then the mapping type is 

   $$
     \chi \colon (A \to B)\;\vdash \; 0 \colon Spectra
     \,.
   $$

=--


### Cohesive and differential refinement
 {#CohesiveAndDifferentialRefinement}

Let $T\mathbf{H}$ be a tangent cohesive $(\infty,1)$-topos and write $T_\ast \mathbf{H}$ for the [[stable (∞,1)-category]] of [[spectrum objects]] inside it. We discuss how every [[stable homotopy type]] here canonically sits in the middle of a _[[differential cohomology diagram]]_.

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

It follows by the discussion at [[schreiber:differential cohomology in a cohesive topos]] that the further differential refinement $\widehat{A}$ of $A$ should be given by a further [[homotopy pullback]]

$$
  \array{
    \widehat{A} &\longrightarrow& \Omega^1(-,Lie(A))
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

But of course by the generality of the above  proposition, such an $\widehat{A}$ sits itself again in its fracture-like pullback diagram.

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

where the two squares are [[homotopy pullback]] squares and the two diagonals are the [[fiber sequences]] of the [[Maurer-Cartan form]] $\theta_A$ and its dual.

=--

+-- {: .num_remark}
###### Remark

The bottom horizontal morphisms in the diagram in prop. \ref{TheDifferentialDiagram} are the canonical [points-to-pieces transform](cohesive%20topos#CanonicalComparison).

=--

+-- {: .num_remark}
###### Remark

This kind of diagram under forming $\pi_0$ has been traditionally known from [[ordinary differential cohomology]] and from [[differential K-theory]], and had been used in proposals to axiomatize [[differential cohomology]], see for instance ([Bunke 12, prop. 4.57](http://arxiv.org/abs/1208.3961)) and see at _[[differential cohomology diagram]]_. Here we see that this holds fully generally for every stable cohesive homotopy type. If one still regards this diagram as characteristic of "differential" refinement it hence exhibits every cohesive stable type as a [[coefficients]] of _some_ [[differential cohomology]] theory. This is a strong version of the synthetic notion 
"[[schreiber:differential cohomology in a cohesive topos]]" . For more on this see also at _[[smooth spectrum]]_.

=--



## Related concepts

* [[sheaf of spectra]]

* [[smooth spectrum]]

* [[twisted generalized cohomology]]

* [[twisted bivariant cohomology]]

* [[twisted differential cohomology]]

* [[twisted smooth cohomology in string theory]]

## References

The idea of forming $T_\ast \mathbf{H}$ as a home for nontrivial [[stable homotopy types]] was originally suggested by [[Georg Biedermann]] and [[André Joyal]], see section 35 of 

* {#Joyal08} [[André Joyal]], _Notes on Logoi_, 2008 ([pdf](http://www.math.uchicago.edu/~may/IMA/JOYAL/Joyal.pdf))
  

and see the further references at _[[tangent (infinity,1)-topos]]_.

Discussion of [[differential cohomology]] in $T_\ast Smooth \infty Grpd \simeq Stab(Smooth \infty Grpd)$ is in

* {#BunkeNikolausVoelkl13} [[Ulrich Bunke]], [[Thomas Nikolaus]], [[Michael Völkl]], _Differential cohomology theories as sheaves of spectra_ ([arXiv:1311.3188](http://arxiv.org/abs/1311.3188))
  

The above discussion of geometric twisted generalized cohomology as cohomology in the tangent cohesive $\infty$-topos was presented in

* {#SchreiberTwists2013} [[Urs Schreiber]], talk at _[Twists, generalised cohomology and applications](http://wwwmath.uni-muenster.de/sfb/sfb878/2013/twists.html)_, October 2013 ([talk notes](twisted+smooth+cohomology+in+string+theory#LocalPrequantumFieldTheory))
  

Discussion in a comprehensive context of cohesion is in section 4.2.3 of 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_ ([arXiv:1310.7930](http://arxiv.org/abs/1310.7930))



[[!redirects cohesive tangent (∞,1)-topos]]

[[!redirects stable cohesive homotopy theory]]
[[!redirects stable cohesive homotopy type theory]]

[[!redirects cohesive stable homotopy theory]]
[[!redirects cohesive stable homotopy type theory]]

[[!redirects tangent cohesion]]

[[!redirects stable cohesion]]

[[!redirects tangent cohesive ∞-topos]]
[[!redirects tangent cohesive ∞-toposes]]
[[!redirects tangent cohesive infinity-topos]]
[[!redirects tangent cohesive infinity-toposes]]
