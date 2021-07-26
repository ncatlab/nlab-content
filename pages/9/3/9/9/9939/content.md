
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Bousfield localization of spectra_ refers generally to [[localization of an (∞,1)-category|localizations]] of the [[stable (∞,1)-category of spectra]] (hence [[Bousfield localization of model categories|Bousfield localization]] of [[model categories of spectra]]) at the collection of [[morphisms]] which become [[equivalences]] under [[smash product of spectra|smash product]] with a given [[spectrum]] $E$. Since any such $E$ represents a [[generalized homology theory]], this may also be thought of  _$E$-[[homology localization]]_.

More specifically, if the [[stable (∞,1)-category of spectra]] is [[presentable (infinity,1)-category|presented]] by a ([[stable model category|stable]]) [[model category]], then the [[localization of an (∞,1)-category|∞-categorical localization]] can be presented by the operation of  _[[Bousfield localization of model categories]]_. The original article ([Bousfield 79](#Bousfield79)) essentially considered localization at the level of [[homotopy categories]].

Specifically, for $E \in Spec$ a [[spectrum]], the _Bousfield localization at $E$_ of another [[spectrum]] $X$ is the [[universal property|universal map]]

$$
  X \longrightarrow L_E X
$$

to the _$E$-[[local spectrum]]_ $L_E X$, with the property that for $Y$ any $E$-acyclic spectrum in that $Y \wedge E \simeq 0$, every morphism $Y \longrightarrow L_E X$ is null-homotopic (a [[zero morphism]] in the [[stable (∞,1)-category of spectra]]). (see for instance [Lurie 10, Example 4](#Lurie10))

For $E = M \mathbb{Z}_p$ the [[Moore spectrum]] of the [[cyclic group]] $\mathbb{Z}_p \coloneqq \mathbb{Z}/p\mathbb{Z}$ for some [[prime number]] $p$, this $E$-localization is _[[p-completion]]_. (see for instance [Lurie 10, Examples 7 and 8](#Lurie10))

## Definition

We write $Ho(Spectra)$ for the [[stable homotopy category]]. For $X,Y \in Ho(Spectra)$ two [[spectra]] we write $[X,Y] \in $ [[Ab]] for its [[hom-object|hom-]][[abelian groups]], and $[X,Y]_\bullet \coloneqq [\Sigma^\bullet X,Y]$ for the corresponding [[graded abelian group]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#GradedAbelianGroupStructureOnHomsInTheHomotopyCategory)).


+-- {: .num_defn #EAcyclicAndLocalSpectra}
###### Definition

Let $E \in Ho(Spectra)$ be a [[spectrum]]. Say that 

1. a spectrum $X$ is **$E$-acyclic** if the [[smash product of spectra|smash product]] with $E$ is [[zero object|zero]], $E \wedge X \simeq 0$;

1. a morphism $f \colon X \to Y$ of spectra is an **$E$-equivalence** if $E \wedge f \;\colon\; E \wedge X \to E \wedge Y$ is an [[isomorphism]] in $Ho(Spectra)$, hence if $E_\bullet(f)$ is an isomorphism in $E$-[[generalized homology]];

1. a spectrum $X$ is **$E$-local** if the following equivalent conditions hold

   1. for every $E$-equivalence $f$ then $[f,X]_\bullet$ is an isomorphism;

   1. every [[morphism]] $Y \longrightarrow X$ out of an $E$-acyclic spectrum $Y$ is [[zero morphism|zero]] in $Ho(Spectra)$;

=--

([Bousfield 79, &#167;1](#Bousfield79)) see also for instance ([Lurie, Lecture 20, example 4](#Lurie10))

+-- {: .num_lemma #TwoConditionsOnELocalSpectrumAreEquivalent}
###### Lemma

The two conditions in the last item of def. \ref{EAcyclicAndLocalSpectra} are indeed equivalent.

=--

+-- {: .proof}
###### Proof

Notice that $A \in Ho(Spectra)$ being $E$-acyclic means equivalently that the unique morphism $0 \longrightarrow A$ is an $E$-equivalence. 

Hence one direction of the claim is trivial. For the other direction we need to show that for $[-,X]_\bullet$ to give an isomorphism on all $E$-equivalences $f$, it is sufficient that it gives an isomorphism on all $E$-equivalences of the form $0 \to A$.

Given a morphism $f \colon A \to B$, write $B \longrightarrow B/A$ for its [[homotopy cofiber]]. Then since $Ho(Spectra)$ is a [[triangulated category]] ([prop.](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyCategoryIsTriangulated)) the defining axioms of triangulated categories ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#CategoryWithCofiberSequences), [lemma](Introduction+to+Stable+homotopy+theory+--+1-1#TrianglesMayBeShiftedToTheLeft)) give that there is a [[commuting diagram]] of the form

$$
  \array{
    0
      &\longrightarrow&
    A 
      &\overset{id}{\longrightarrow}&
    A
      &\overset{}{\longrightarrow}&
    0
      &\overset{}{\longrightarrow}&
    \Sigma A
    \\
    \downarrow
      &&
    \downarrow^{\mathrlap{id}}
      &&
    \downarrow^{\mathrlap{f}}
      &&
    \downarrow
      &&
    \downarrow^{\mathrlap{id}}
    \\
    \Sigma^{-1} B/A
      &\longrightarrow&
    A 
      &\underset{f}{\longrightarrow}&
    B
      &\longrightarrow&
    B/A
      &\longrightarrow&
    \Sigma A
  }
  \,,
$$

where both the top as well as the bottom are [[homotopy cofiber sequences]]. Hence applying $[-,X]_\bullet$ to this diagram in $Ho(Spectra)$ yields a diagram of [[graded abelian groups]] of the form

$$
  \array{
    0 
      &\longleftarrow&
    [A,X]_\bullet
      &\longleftarrow&
    [A,X]_\bullet
      &\longleftarrow&
    0
      &\longleftarrow&
    [A,X]_{\bullet+1}
    \\
    \uparrow
      &&
    \uparrow^{\mathrlap{id}}
      &&
    \uparrow^{\mathrlap{[f,X]_\bullet}}
      &&
    \uparrow
      &&
    \uparrow^{\mathrlap{id}}
    \\
    [B/A,X]_{\bullet+1}
      &\longleftarrow&
    [A,X]_\bullet
      &\longleftarrow&
    [B,X]_\bullet
      &\longleftarrow&
    [B/A,X]_\bullet
      &\longleftarrow&
    [A,X]_{\bullet+1}
  }
  \,,
$$

where now both horizontal sequences are [[long exact sequences]] ([prop.](Introduction+to+Stable+homotopy+theory+--+1-1#LongFiberSequencesOfMapsOfSpectra)).

Hence if $[B/A,X]_\bullet \longrightarrow 0$ is an isomorphism, then all four outer vertical morphisms in this diagram are isomorphisms, and then the [[five-lemma]] implies that also $[f,X]_\bullet$ is an isomorphism.

Hence it is now sufficient to observe that with $f \colon A \to B$ an $E$-equivalence, then its homotopy cofiber $B/A$ is $E$-acyclic.  

To see this, notice that by the [[tensor triangulated category|tensor triangulated]] structure on $Ho(Spectra)$ ([prop.](Introduction+to+Stable+homotopy+theory+--+1-2#TensorTriangulatedStructureOnStableHomotopyCategory)) the [[smash product of spectra|smash product]] with $E$ preserves homotopy cofiber sequences, so that there is a homotopy cofiber sequence

$$
  E \wedge A
    \overset{E \wedge f}{\longrightarrow}
  E \wedge B
    \longrightarrow
  E \wedge (B/A)
    \longrightarrow
  E \wedge \Sigma A
  \,.
$$

But if the first morphism here is an isomorphism, then the axioms of a [[triangulated category]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#CategoryWithCofiberSequences)) imply that $E \wedge B / A \simeq 0$. In detail: by the axioms we may form the morphism of homotopy cofiber sequences

$$
  \array{
    E \wedge A
      &\overset{E \wedge f}{\longrightarrow}&
    E \wedge B
      &\longrightarrow&
    E \wedge B/A
      &\longrightarrow&
    E \wedge \Sigma A
    \\
    \downarrow^{\mathrlap{id}}
      &&
    \downarrow^{\mathrlap{(E\wedge f)^{-1}}}
      &&
    \downarrow
      &&
    \downarrow^{\mathrlap{id}}
    \\
    E \wedge A
      &\underset{id}{\longrightarrow}&
    E \wedge A
      &\longrightarrow&
    0
      &\longrightarrow&
    E \wedge \Sigma A
  }
  \,.
$$

Then since two of the three vertical morphisms on the left are isomorphisms, so is the third ([lemma](Introduction+to+Stable+homotopy+theory+--+1-1#TwoOutOfThreeForMorphismsOfDistinguishedTriangles)).

=--

+-- {: .num_defn #ELocalizationOfSpectra}
###### Definition

Given $E,X \in Ho(Spectra)$, then an **$E$-localization** of $X$ is 

1. an $E$-local spectrum $L_E X$

1. an $E$-equivalence $X \longrightarrow L_E X$.

according to def. \ref{EAcyclicAndLocalSpectra}.

=--

We discuss now that $E$-Localizations always exist. The key to this is the following lemma \ref{KappaCellSpectrumWitnessingELocalization}, which asserts that a spectrum being $E$-local is equivalent to it being $A$-null, for some "small" spectrum $A$:


+-- {: .num_lemma #KappaCellSpectrumWitnessingELocalization}
###### Lemma

For every [[spectrum]] $E$ there exists a spectrum $A$ such that any spectrum $X$ is $E$-local (def. \ref{EAcyclicAndLocalSpectra}) precisely if it is $A$-null, i.e.

$$
  X \;is\; E\text{-local}
    \;\;\;\;
  \Leftrightarrow
    \;\;\;\;
  [A,X]_\ast = 0
$$

and such that 

1. $A$ is $E$-acyclic (def. \ref{EAcyclicAndLocalSpectra});
 
1. there exists an infinite [[cardinal number]] $\kappa$ such that $A$ is a $\kappa$-[[CW spectrum]] (hence a [[CW spectrum]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#CWSpectrum)) with at most $\kappa$ many cells);

1. the class of $E$-acyclic spectra (def. \ref{EAcyclicAndLocalSpectra}) is the class generated by $A$ under 

   1. [[wedge sum]] 

   1. the relation that if in a [[homotopy cofiber sequence]] $X_1 \to X_2 \to X_3$ two of the spectra are in the class, then so is the third.

=--

([Bousfield 79, lemma 1.13 with lemma 1.14](#Bousfield79)) review includes ([Bauer 11, p.2,3](Bauer11), [VanKoughnett 13, p. 8](#VanKoughnett13))



+-- {: .num_prop #ELocalizationCofiber}
###### Proposition

For $E \in Ho(Spectra)$ any [[spectrum]], every spectrum $X$ sits in a [[homotopy cofiber sequence]] of the form

$$
  G_E(X) 
    \longrightarrow 
  X 
    \overset{\eta_X}{\longrightarrow}
  L_E(X)
  \,,
$$

and [[natural transformation|natural]] in $X$, such that

1. $G_E(X)$ is $E$-acyclic, 

1. $L_E(X)$ is $E$-local, 

according to def. \ref{EAcyclicAndLocalSpectra}.

=--

([Bousfield 79, theorem 1.1](#Bousfield79)) see also for instance ([Lurie, Lecture 20, example 4](#Lurie10))


+-- {: .proof}
###### Proof 

Consider the $\kappa$-[[CW-spectrum]] spectrum $A$ whose existence is asserted by lemma \ref{KappaCellSpectrumWitnessingELocalization}. Let

$$
  I_A
  \coloneqq
  \{A \to Cone(A)\}
$$

denote the set containing as its single element the canonical morphism (of [[sequential spectra]]) from $A$ into the standard [[cone]] of $A$, i.e.  the cofiber 

$$
  Cone(A) 
    \coloneqq 
  cofib( A \to A \wedge I_+ )
    \simeq
  A \wedge I
$$ 

of the inclusion of $A$ into its standard [[cylinder spectrum]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#StandardCylinderSpectrumSequential)).


Since the standard cylinder spectrum on a CW-spectrum is a [[good cylinder object]] ([prop.](Introduction+to+Stable+homotopy+theory+--+1-1#CylinderSpectrumOverCWSpectrumIsGood)) this means ([lemma](Introduction+to+Stable+homotopy+theory+--+P#HomsOutOfCofibrantIntoFibrantComputeHomotopyCategory)) that for $X$ any fibrant sequential spectrum, and for $A \longrightarrow X$ any morphism, then an extension along the cone inclusion

$$
  \array{
    A &\longrightarrow& X
    \\
    \downarrow & \nearrow
    \\
    Cone(A)
  }
$$

equivalently exhibits a null-homotopy of the top morphism. Hence the $(A \to Cone(A))$-[[injective objects]] in $Ho(Spectra)$ are precisely those spectra $X$ for which $[A,X]_\bullet \simeq 0$.

Moreover, due to the degreewise nature of the smash tensoring $Cone(A) = A \wedge I$ ([def](Introduction+to+Stable+homotopy+theory+--+1-1#TensoringAndPoweringOfSequentialSpectra)), the inclusion morphism $A \to Cone(A)$ is degreewise the inclusion of a [[CW-complex]] into its standard cone, which is a [[relative cell complex]] inclusion ([prop.](Introduction+to+Stable+homotopy+theory+--+P#TopologicalCylinderOnCWComplexIsGoodCylinderObject)).

By [this lemma](Introduction+to+Stable+homotopy+theory+--+1-1#kappaCellSpectrumIsKappaSmall) the $\kappa$-[[cell spectrum]] $A$ is _$\kappa$-small object_ ([def.](Introduction+to+Stable+homotopy+theory+--+P#ClassOfMorphismsWithSmallDomains)) with respect to morphisms of spectra which are degreewise [[relative cell complex]] inclusion  [[small object argument]] . 

Hence the [[small object argument]] applies ([prop.](Introduction+to+Stable+homotopy+theory+--+P#SmallObjectArgument)) and gives for every $X$ a factorization of the terminal morphism $X \to \ast$ as an $I_A$-[[relative cell complex]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopologicalCCellComplex)) followed by an $I_A$-[[injective morphism]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#RightLiftingProperty))

$$
  X
    \overset{I_A Cell}{\longrightarrow} 
  L_E X
    \overset{I_A Inj}{\longrightarrow}
  \ast
  \,.
$$

By the above, this means that $[A, L_E X] = 0$, hence by lemma \ref{KappaCellSpectrumWitnessingELocalization} that $L_E X$ is $E$-local. 


It remains to see that the [[homotopy fiber]] of $X \to L_E X$ is $E$-acyclic: By the [[tensor triangulated category|tensor triangulated]] structure on $Ho(Spectra)$ ([prop.](Introduction+to+Stable+homotopy+theory+--+1-2#TensorTriangulatedStructureOnStableHomotopyCategory)) it is sufficient to show that the [[homotopy cofiber]] is $E$-acyclic (since it differs from the homotopy fiber only by suspension). By the [[pasting law]], the homotopy cofiber of a [[transfinite composition]] is the transfinite composition of a sequence of homotopy pushouts. By lemma \ref{KappaCellSpectrumWitnessingELocalization} and applying the pasting law again, all these homotopy pushouts produce $E$-acyclic objects. Hence we conclude by observing that the the transfinite composition of the morphisms between these $E$-acyclic objects is $E$-acyclic. Since by construction all these morphisms are relative cell complex inclusions, this follows again with the compactness of the $n$-spheres ([lemma](Introduction+to+Stable+homotopy+theory+--+P#CompactSubsetsAreSmallInCellComplexes)).

=--


+-- {: .num_lemma}
###### Lemma

The morphism $X \to L_E (X)$ in prop. \ref{ELocalizationCofiber} exhibits an $E$-localization of $X$ according to def. \ref{ELocalizationOfSpectra} 

=--

+-- {: .proof}
###### Proof

It only remains to show that $X \to L_E X$ is an $E$-equivalence. By the  [[tensor triangulated category|tensor triangulated]] structure on $Ho(Spectra)$ ([prop.](Introduction+to+Stable+homotopy+theory+--+1-2#TensorTriangulatedStructureOnStableHomotopyCategory)) the [[smash product of spectra|smash product]] with $E$ preserves homotopy cofiber sequences, so that 

$$
  E \wedge G_E X
   \longrightarrow
  E \wedge X
    \overset{E \wedge \eta_X}{\longrightarrow}
  E \wedge L_E X
    \longrightarrow
  E \wedge \Sigma G_E X
$$

is also a homotopy cofiber sequence. But now $E \wedge G_E X \simeq 0$ by prop. \ref{ELocalizationCofiber}, and so the axioms ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#CategoryWithCofiberSequences)) of the [[triangulated category|triangulated structure]] on $Ho(Spectra)$ ([prop.](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyCategoryIsTriangulated)) imply that $E \wedge \eta$ is an isomorphism.

=--



+-- {: .num_remark #Acyclification}
###### Remark

Hence where $L_E$ is traditionally called "$E$-localization", $G_E$ might be called "$E$-acyclification", though that terminology is not used commonly. 

=--


## Properties






### Localization at Moore spectra of abelian groups

A basic special case of $E$-localization of spectra is given for $E = S A$ the [[Moore spectrum]] of an [[abelian group]] $A$ ([Bousfield 79, section 2](#Bousfield79)). For $A = \mathbb{Z}_{(p)}$ this is [[p-localization]] and for $A = \mathbb{F}_p$ this is [[p-completion]], see examples \ref{pLocalization} and \ref{pCompletion} below for more.

+-- {: .num_prop}
###### Proposition

For $A_1$ and $A_2$ two [[abelian groups]] then the following are equivalent

1. the Bousfield localizations at their [[Moore spectra]] are equivalent 

   $$
     L_{S A_1} \simeq L_{S A_2}
     \,;
   $$

1. $A_1$ and $A_2$ have the same _type of acyclicity_, meaning that 
 
   1. every [[prime number]] $p$ is invertible in $A_1$ precisely if it is in $A_2$;

   1. $A_1$ is a [[torsion group]] precisely if $A_2$ is.

=--

([Bousfield 79, prop. 2.3](#Bousfield79)) recalled e.g. in ([VanKoughnett 13, prop. 4.2](#VanKoughnett13)).

This means that given an abelian group $A$ then 

* either $A$ is not torsion, then 

  $$
    L_{S A} \simeq L_{S \mathbb{Z}[I^{-1}]}
    \,,
  $$ 

  where $I$ is the set of primes invertible in $A$ and $\mathbb{Z}[I^{-1}] \hookrightarrow \mathbb{Q}$ is the [[localization of a ring|localization]] at these primes of the [[integers]];

* or $A$ is torsion, then 
    
  $$
   L_{S A }\simeq L_{S(\oplus_q \mathbb{F}_q )  }
   \,,
  $$

  where the [[direct sum]] is over all [[cyclic groups]] of order $q$, for $q$ a prime not invertible in $A$.


### Relation to nilpotent completion

Let $E$ be an [[E-∞ ring]] and let $X$ be any [[spectrum]]

+-- {: .num_remark #CanonicalMapFromELocalizationToTotalization}
###### Remark

There is a canonical map

$$
  L_E X \stackrel{}{\longrightarrow} \underset{\leftarrow}{\lim}_n (E^{\wedge^{n+1}_S}\wedge_S X)
$$

from the $E$-[[Bousfield localization of spectra]] of $X$ into the [[totalization]] of the canonical [[cosimplicial object|cosimplicial]] [[spectrum]] (see at _[[nilpotent completion]]_).


=--

We now consider conditions for this morphism to be an [[equivalence]].

+-- {: .num_defn #CoreOfARing}
###### Definition

For $R$ a [[ring]], its _core_ $c R$ is the [[equalizer]] in

$$
  c R 
    \longrightarrow 
  R 
    \stackrel{\longrightarrow}{\longrightarrow}
  R \otimes R
  \,.
$$

=--

+-- {: .num_prop #SufficientConditionsForTotalizationToBeELocalization}
###### Proposition

Let $E$ be a [[connective spectrum|connective]] [[E-∞ ring]] such that the core of $\pi_0(E)$, def. \ref{CoreOfARing}, is either of

* the [[localization of a ring|localization]] of the [[integers]] at a set $J$ of [[primes]], $c \pi_0(E) \simeq \mathbb{Z}[J^{-1}]$;

* $\mathbb{Z}_n$ for $n \geq 2$.

Then the map in remark \ref{CanonicalMapFromELocalizationToTotalization} is an equivalence

$$
  L_E X \stackrel{\simeq}{\longrightarrow} 
  \underset{\leftarrow}{\lim}_n (E^{\wedge^{n+1}_S}\wedge_S X)
  \,.
$$

=--

([Bousfield 79](#Bousfield79)) see also for instance ([Bauer 11, p.2](#Bauer11))

For more discussion of [[E-infinity geometry|E-infinity]] (derived) [[formal completions]] via totalizations of [[Amitsur complexes]], see ([Carlsson 07](completion+of+a+module#Carlsson07)).



### Fracture theorem

The [[fracture theorem]] says how Bousfield localization at a [[coproduct]]/[[wedge sum]] of spectra is a [[homotopy pullback]] of Bousfield localization separately. See at _[[fracture theorem]]_ for more on this.


## Examples

### General

+-- {: .num_example #EModulesAreELocal}
###### Example

For $E$ an [[E-∞ ring]], every [[∞-module]] $X$ over $E$ is $E$-local, def. \ref{EAcyclicAndLocalSpectra}.

=--

(e.g. [Lurie, Lecture 20, example 5](#Lurie10))

+-- {: .num_example}
###### Example

For $E$ an [[E-∞ algebra]] over an [[E-∞ ring]] $S$ and for $X$ an $S$-[[∞-module]], consider the dual [[Cech nerve]] [[cosimplicial object]]

$$
  E^{\wedge_S^{\bullet+1}}\wedge_S X \;\colon\; \Delta \longrightarrow Spectra
  \,.
$$

By example \ref{EModulesAreELocal} each term is $E$-local, so that the map  to the  [[totalization]]

$$
  X \longrightarrow \underset{\leftarrow}{\lim} E^{\wedge_S^{\bullet+1}} \wedge_S X
$$

factors through the $E$-localization of $X$

$$
  X \longrightarrow 
  L_E X
  \longrightarrow
  \underset{\leftarrow}{\lim} E^{\wedge_S^{\bullet+1}} \wedge_S X
  \,.
$$

Under suitable condition the second map here is indeed an [[equivalence]], in which case the [[totalization]] of the dual [[Cech nerve]] exhibits the $E$-localization. This happens for instance in the discussion of the [[Adams spectral sequence]], see the examples given there.

(see also e.g. [Bauer 11, p. 2](#Bauer11))

=--

### Rationalization

+-- {: .num_example #Rationalization}
###### Example

Bousfield localization at the [[Moore spectrum]]/[[Eilenberg-MacLane spectrum]] $S \mathbb{Q}\simeq H\mathbb{Q}$ of the [[rational numbers]] is [[rationalization]] to [[rational homotopy theory]].

The corresponding $\mathbb{Q}$-acyclification (remark \ref{Acyclification}) is _[[torsion approximation]]_.


=--

e.g. ([Bauer 11, example 1.7](#Bauer11))



### $p$-Localization

For $p$ a [[prime number]] write $\mathbb{Z}_{(p)}$ for the  [[localization of a ring|localization]] of the [[integers]] _at_ $(p)$,  for the ring of integers [[localization of a ring|localized at]] $p$, hence with all primes _except_ $p$ inverted; equivalently the subring of the [[rational numbers]] with denominator not divisible by $p$.

+-- {: .num_example #pLocalization}
###### Example

The Bousfield localization at the [[Moore spectrum]] $S \mathbb{Z}_{(p)}$ is [[p-localization]]. 

=--

([Bousfield 79](#Bousfield79)), [Bauer 11, example 1.7](#Bauer11)). See at _[[localization of a space]]_ for details on this.

+-- {: .num_prop #pLocalizationIsSmashing}
###### Proposition

$p$-localization is a [[smashing localization]]:

$$
  L_{S \mathbb{Z}_{(p)}} X
  \simeq
  S \mathbb{Z}_{(p)} \wedge X
  \,.
$$

=--

([Bousfield 79, prop. 2.4](#Bousfield79)) recalled e.g. as ([van Koughnett 13, prop. 4.3](#VanKoughnett13)).


### $p$-Completion

For $p \in \mathbb{N}$ a [[prime number]], 
write 

$$
  \mathbb{F}_p = \mathbb{Z}/(p)
$$

for the [[cyclic group]]/[[finite field]] of [[order of a group|order]] $p$.


+-- {: .num_defn}
###### Definition

Write

$$
  \mathbb{Z}/p^\infty \coloneqq (\mathbb{Z}[p^{-1}])/\mathbb{Z}
$$

for the [[localization of a ring|localization]] of the [[integers]] away from $p$ followed by the quotient by $\mathbb{Z}$.

=--

e.g. ([Bousfield 79, p. 6](#Bousfield79))

+-- {: .num_remark}
###### Remark

The [[short exact sequence]] of [[abelian groups]]

$$
  0 \to \mathbb{Z} \longrightarrow \mathbb{Z}[p^{-1}] \longrightarrow \mathbb{Z}/p^\infty \to 0
$$

induces the [[homotopy fiber sequence]] (in [[spectra]]) of [[Moore spectra]]

$$
  \Omega S(\mathbb{Z}/p^\infty) \longrightarrow S\mathbb{Z} \longrightarrow S(\mathbb{Z}[p^{-1}])
 \,.
$$

As in [Bousfield 79, p. 6](#Bousfield79) one also writes

$$
  S^{-1} (\mathbb{Z}/p^\infty)
  \coloneqq 
  \Omega S(\mathbb{Z}/p^\infty)
  \,.
$$

=--


+-- {: .num_prop}
###### Proposition

The localization of spectra at the [[Moore spectrum]] $S\mathbb{F}_p$ is given by the [[mapping spectrum]] out of $S^{-1} \mathbb{Z}/p^\infty$:

$$
  L_{S \mathbb{F}_p} X
  \simeq
  [\Omega S \mathbb{Z}/p^\infty, X]
  \,.
$$

=--

([Bousfield 79, prop. 2.5](#Bousfield79))


Fact: $\mathbb{F}_p$-localizaton is [[p-completion]], e.g. [Lurie "Proper Morphisms...", section 4](#LurieProper).

+-- {: .num_example}
###### Example

Let 

$$
  E \coloneqq H \mathbb{Z}/p\mathbb{Z}
$$ 

be the corresponding [[Eilenberg-MacLane spectrum]]. Then a spectrum which corresponds to a [[chain complex]] under the [stable Dold-Kan corespondence](module+spectrum#StableDoldKanCorrespondence) is $E$-local, def. \ref{AcyclicAndLocal}, if that chain complex has [[chain homology]] groups being $\mathbb{Z}[p^{-1}]$-modules.

The $E$-localization of a spectrum in this case is  _[[p-completion]]_.

=--

(e.g. [Lurie, Lecture 20, example 8](#Lurie10))

More generally

+-- {: .num_example #pCompletion}
###### Example

Bousfield localization at the [[Moore spectrum]] $S \mathbb{F}_p$ is [[p-completion]] to [[p-adic homotopy theory]].

=--

E.g. ([Bauer 11, example 1.7](#Bauer11)). See at _[[localization of a space]]_ for more on this.


### Telescopic localization

* [[telescopic localization]]


### Chromatic localization

* [[chromatic localization]]


## Related concepts

* [[smashing localization]]

* [[chromatic filtration]], [[chromatic layer]]

* [[KU-local stable homotopy theory]]

* [[K(n)-local stable homotopy theory]]

## References

Original articles are

* {#Bousfield79} [[Aldridge Bousfield]], _The localization of spectra with respect to homology_, Topology Volume 18 Issue 4 (1979) (<a href="https://doi.org/10.1016/0040-9383(79)90018-1">doi:10.1016/0040-9383(79)90018-1</a>, [pdf](http://www.uio.no/studier/emner/matnat/math/MAT9580/v12/undervisningsmateriale/bousfield-topology-1979.pdf))


* {#Ravenel84} [[Douglas Ravenel]], _Localization with respect to certain periodic homology theories_, American Journal of Mathematics, Vol. 106, No. 2, (Apr., 1984), pp. 351-414 ([jstor:2374308](https://www.jstor.org/stable/2374308), [pdf](https://www.math.rochester.edu/people/faculty/doug/mypapers/loc.pdf)) 

Discussion in terms of [[Bousfield localization of model categories]] [[model category of spectra|of spectra]] appears in

* {#EKMM97} [[Anthony Elmendorf]], [[Igor Kriz]], [[Michael Mandell]], [[Peter May]], chapter VIII of _[[Rings, modules and algebras in stable homotopy theory]]_ 1997 ([pdf](http://www.math.uchicago.edu/~may/BOOKS/EKMM.pdf))

* {#SchwedeShipley02} [[Stefan Schwede]], [[Brooke Shipley]], lemma 4.1 in _A uniqueness theorem for stable homotopy theory_, Mathematische Zeitschrift 239 (2002), 803-828 ([arXiv:math/0012021](https://arxiv.org/abs/math/0012021))

see also

* [[Carles Casacuberta]], [[Javier Gutiérrez]], _Homotopical Localizations of Module Spectra_, Transactions of the American Mathematical Society
Vol. 357, No. 7 (Jul., 2005), pp. 2753-2770  ([jstor](http://www.jstor.org/stable/3845180))

Lecture notes include

* [[Nerses Aramian]], _Bousfield Localization_ ([pdf](http://www.math.uiuc.edu/~aramyan2/bousfield.pdf))

* {#Bauer11} [[Tilman Bauer]], _Bousfield localization and the Hasse square_ ([pdf](http://math.mit.edu/conferences/talbot/2007/tmfproc/Chapter09/bauer.pdf), [[Bauer_BousfieldLocalization.pdf:file]]), Chapter 6 in: [[Christopher Douglas]], [[John Francis]], [[André Henriques]], [[Michael Hill]] (eds.), _Topological Modular Forms_, Mathematical Surveys and Monographs Volume 201, AMS 2014  ([ISBN:978-1-4704-1884-7](https://bookstore.ams.org/surv-201))


 
* {#VanKoughnett13} [[Paul VanKoughnett]], _Spectra and localization_, 2013 ([[VanKoughnettLocalization.pdf:file]])


Discussion in the general context of [[higher algebra]]/[[stable homotopy theory]]:

* {#Lurie10} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture notes (2010) ([web](http://www.math.harvard.edu/~lurie/252x.html)),  Lecture 20 _Bousfield localization_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture20.pdf))

* {#LurieProper} [[Jacob Lurie]], section 4 of _[[Proper Morphisms, Completions, and the Grothendieck Existence Theorem]]_ 

Discussion specifically of [[K(n)-local spectra]] includes

* [[Michael Hopkins]], [[Jacob Lurie]], _[[Ambidexterity in K(n)-Local Stable Homotopy Theory]]_

See also

section 2.4 of

* Holger Reeker, _On K(1)-local SU-bordism_ ([arXiv:0907.4299](http://arxiv.org/abs/0907.4299))

Discussion specifically of [[KU-local stable homotopy theory]]:

* [[Jeroen van der Meer]], Chapter 4 of: _A Stack-Theoretic Perspective on $\mathrm{KU}$-Local Stable Homotopy Theory_, 2019 ([pdf](https://www.universiteitleiden.nl/binaries/content/assets/science/mi/scripties/master/2018-2019/jvd-meer-thesisroot.pdf))

[[!redirects local spectrum]]
[[!redirects local spectra]]

[[!redirects localization of a spectrum]]
[[!redirects localization of spectra]]

[[!redirects localization of spectra]]
[[!redirects localizations of spectra]]

