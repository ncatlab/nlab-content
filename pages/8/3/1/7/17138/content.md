
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

{:bluebox: .un_remark style="border:solid #000000;background: #E6DF13;border-width:2px 1px;padding:0 1em;margin:0 1em;"}


> This entry contains one chapter of _[[geometry of physics]]_, see there for context and background.

> previous chapters: _[[geometry of physics -- homotopy types|homotopy types]]_, _[[geometry of physics -- smooth homotopy types|smooth homotopy types]]_

> next chapters: _[[geometry of physics -- groups|groups]]_, _[[geometry of physics -- geometric quantization with KU-coefficients|geometric quantization with KU-coefficients]]_

***


#Contents#
* table of contents
{:toc}


## Introduction

### Stable homotopy theory

We discuss [[spectra]] in the sense of [[algebraic topology]]: the proper generalization of [[abelian groups]] to [[homotopy theory]]. Since these are universally characterized as being the [[stabilization]] of plain [[homotopy types]] under [[looping and delooping]], one speaks of _[[stable homotopy theory]]_.

$$
  Spaces
  \underoverset{(linearization)}{stabilization}{\mapsto}
  Spectra
  \,.
$$

Most of [[linear algebra]] and [[algebraic geometry]] passes along as [[abelian groups]] are generalized to [[spectra]] and turns into something remarably rich, called _[[brave new algebra]]_, _[[higher algebra]]_ and _[[E-∞ geometry|spectral geometry]]_. In particular the analog of the theory of ([[commutative ring|commutative]]) [[rings]] and their [[modules]] exist, given by ([[commutative ring spectrum|commutative]]) [[ring spectra]] ([[E-∞ rings]], [[A-∞ rings]]) and [[module spectra]] ([[∞-modules]]). 

### Adams-Novikov spectral sequences

Since spectra are considerably richer than abelian groups, stable homotopy is much concerned with "[[fracture theorem|fracturing]]" stable homotopy types into more tractable components:

To that end, notice that from the point of view of [[arithmetic geometry]], an [[abelian group]] $A$ is equivalently a [[quasicoherent sheaf]] over [[Spec(Z)]]. 

$$
  AbelianGroups \simeq QCoh(Spec(\mathbb{Z}))
  \,.
$$

This point of view generalizes to homotopy theory and turns out to be very fruitful there. The analog of the [[integers]] $\mathbb{Z}$ is the [[sphere spectrum]] $\mathbb{S}$, and this is naturally the [[initial object in an (infinity,1)-category|initial]] [[commutative ring spectrum]] ("[[E-∞ ring]]"), just as $\mathbb{Z}$ is the [[initial object|initial]] [[commutative ring]]. The [[formal dual]]  [[Spec(S)]] of $\mathbb{S}$ is hence the [[terminal object in an (infinity,1)-category|terminal]] [[space]] in [[E-∞ arithmetic geometry]] ("[[spectral geometry]]") and [[spectra]] are equivalently the [[quasicoherent ∞-stacks]] over $Spec(\mathbb{S})$

$$
  Spectra \simeq QCoh(Spec(\mathbb{S}))
  \,.
$$

Therefore the study of spectra "[[fracture theorem|fractures]]" into the various [[localizations]] and [[formal completions]] of $Spec(S)$. Since this is like the white light of $Spec(S)$ decomposing into various wavelengths, one speaks of _[[chromatic homotopy theory]]_. 

In particular, an  [[E-∞ ring]] $E$ is [[formal dual|dually]] a morphism of $E_\infty$-algebraic spaces $Spec(E) \longrightarrow Spec(\mathbb{S})$ and under good conditions the [[1-image]] of this map is the formal dual of the [[formal completion]] at $E$:

$$
  Spec(E) \stackrel{epi_1}{\longrightarrow} Spec(\mathbb{S}_E^\wedge) \stackrel{mono_1}{\longrightarrow} Spec(\mathbb{S})
 \,.
$$

This means that $Spec(E) \longrightarrow Spec(\mathbb{S}_E^\wedge)$ is a [[cover]] and that hence $E$-local spectra are equivalently [[quasicoherent ∞-stacks]] on $Spec(E)$ equipped with [[descent data]]: [[formal dual|dually]] they are [[∞-modules]] over $E$ equipped with [[comodule]] structure over the [[Hopf algebroid]] ([[Sweedler coring]]) $E \otimes_{\mathbb{S}} E$.

The computation of [[homotopy groups]] of spectra that make use of their decomposition this way into $E$-[[∞-modules]] equipped with [[descent]] data is the _$E$-[[Adams spectral sequence]]_, a central tool of the theory.

### Geometry over $Spec(\mathbb{S})$

For this reason special importance is carried by those [[E-∞ rings]] such that $Spec(E) \to Spec(\mathbb{S})$ is already a [[covering]], for these the $E$-[[∞-modules]] equipped with descent data give an equivalent, but in general more tractable, incarnation of the stable homotopy theory of spectra.

Curiously, a good bit of [[differential geometry]] and of structures known from [[physics]] arises within the abstract stable homotopy theory this way: the archetypical $Spec(E)$ which covers $Spec(\mathbb{S})$ is $E = $ [[MU]], the [[Thom spectrum]] for [[complex vector bundles]].

Now [[Quillen's theorem on MU]] says that $Spec(MU)$ is a refined version of the [[moduli stack of formal groups]] $\mathcal{M}_{fg}$. This in turn naturally admits a [[stratification]] by the [[height of formal groups]]. 

[[!include chromatic tower examples - table]]
 

## **1)** Stable homotopy theory
 
### Spectra

* [[spectrum]], [[symmetric smash product of spectra]]

* [[symmetric spectra]]

* [[suspension spectrum]], [[sphere spectrum]]

* [[Thom spectrum]]

* [[stable homotopy category]]

* [[smash product of spectra]],

* [[model structures on symmetric spectra]]


### Ring spectra

* [[ring spectrum]], [[E-∞ ring]]

* model structure for ring spectra

### Module spectra

* [[module spectrum]], [[∞-module]]

* model structure for module spectra

## **2)** Adams-Novikov spectral sequences

Write $HoSpectra$ for the [[stable homotopy category]] and write 

$$
  [-,-] \;\colon\; HoSpectra^{op} \times HoSpectra \longrightarrow Ab
$$

for the [[hom-functor]] with values in [[abelian groups]].

+-- {: .num_defn #HomotopyFunctor}
###### Definition

For $S \in HoSpectra$, the _homotopy functor it represents_ it to me the [[representable functor]]

$$
  [S,-] \;\colon\; HoSpectra \longrightarrow Ab
$$

(as opposed to the other, contravariant, functor).

=--

+-- {: .num_example}
###### Example

For $S = \Sigma^\infty S^n \simeq \Sigma^n \mathbb{N}$ then 

$$
  [\Sigma^\infty S^n ,- ]\simeq \pi_n
$$

is the $n$th [[homotopy group]]-functor.

=--


Throughout, let $E$ be a [[ring spectrum]]. 



#### $E$-Injective spectra

First we consider a concept of of $E$-[[injective objects]] in [[Spectra]].


+-- {: .num_defn #ExactSequences}
###### Definition

Say that 

1. a sequence of spectra

   $$
     A_1 \longrightarrow A_2 \longrightarrow \cdots \longrightarrow A_n
   $$

   is 

   1. a (long) _exact sequence_ if the induced sequence of homotopy functors, def. \ref{HomotopyFunctor}, is a [[long exact sequence]] in $[HoSpectra,Ab]$;

   2. (for $n = 2$) a _short exact sequence_ if

      $$
        0 \longrightarrow A_1 \longrightarrow A_2 \longrightarrow A_3 \longrightarrow 0
      $$

      is (long) exact;


1. a morphism $A \longrightarrow B$  is 

   1. a _monomorphism_ if $0 \longrightarrow A \longrightarrow B$ is an exact sequence;

   1. an _epimorphism_ if $A \longrightarrow B \longrightarrow 0$ is an exact sequence.

For $E$ a [[ring spectrum]], then a sequence of spectra is (long/short) _$E$-exact_ and a morphism is epi/mono, respectively, if becomes long/short exact or epi/mono, respectively, after taking [[smash product of spectra|smash product]] with $E$.

=--

+-- {: .num_example}
###### Example

Every [[homotopy cofiber sequence]] of spectra is exact in the sense of def. \ref{ExactSequences}. 

=--

+-- {: .num_remark}
###### Remark/Warning

Consecutive morphisms in an $E$-exact sequence according to def. \ref{ExactSequences} in general need not compose up to homotopy, to the [[zero morphism]]. But this does become true for sequences of $E$-injective objects, defined below in def. \ref{EInjective}.

=--

+-- {: .num_lemma}
###### Lemma

1. If $f \colon B\longrightarrow A$ is a monomorphism in the sense of def. \ref{ExactSequences}, then there exists a morphism $g \colon C \longrrightarrow A$ such that the [[wedge sum]] morphism is a [[weak homotopy equivalence]]

   $$
     f \vee g \;\colon\; B \wedge C \stackrel{\simeq}{\longrightarrow} A
     \,.
   $$

1. If $f \colon A \longrightarrow B$ is an epimorpimsm in the sense of def. \ref{ExactSequences}, then there exists a homotopy [[section]] $s \colon B\to A$, i.e. $f\circ s\simeq Id$, together with a morphism $g \colon C \to A$ such that the [[wedge sum]] morphism is a [[weak homotopy equivalence]]

   $$
     s \vee f \colon B\vee C \stackrel{\simeq}{\longrightarrow} A
     \,.
   $$

=--

+-- {: .num_defn #EInjective}
###### Definition

For $E$ a [[ring spectrum]], say that a spectrum $S$ is _$E$-injective_ if for each morphism $A \longrightarrow S$ and  each $E$-monomorphism $f \colon A \longrightarrow S$ in the sense of def. \ref{ExactSequences}, there is a [[diagram]] in [[HoSpectra]] of the form

$$
  \array{
    A &\longrightarrow & S 
    \\
    \downarrow & \nearrow_{\mathrlap{\exists}}
    \\
    B
  }
  \,.
$$

=--

+-- {: .num_lemma}
###### Lemma

If $S$ is $E$-injective in the sense of def. \ref{EInjective}, then there exists a spectrum $X$ such that $S$ is a [[retract]] in [[HoSpectra]] of $E \wedge X$.

=--

#### $E$-Adams resolutions

+-- {: .num_defn #EAdamsResolution}
###### Definition

For $E$ a [[ring spectrum]], then an _$E$-Adams resolution_ of an spectrum $S$ is a long exact sequence, in the sense of def. \ref{ExactSequences}, of the form


$$
  0 \longrightarrow S \longrightarrow I_0 \longrightarrow I_1 \longrightarrow I_2 \longrightarrow \cdots
$$

such that each $I_j$ is $E$-injective, def. \ref{EInjective}.

=--

+-- {: .num_lemma}
###### Lemma

Any two consecutive maps in an $E$-Adams resolution compose to the [[zero morphism]].

=--


+-- {: .num_lemma}
###### Lemma

For $X \to X_\bullet$ an $E$-Adams resolution, def. \ref{EAdamsResolution}, and for $X \longrightarrow Y$ any morphism, then there exists an $E$-Adams resolution $Y \to J_\bullet$ and a [[commuting diagram]]

$$
  \array{
     X &\longrightarrow& I_\bullet
     \\
     \downarrow^{\mathrlap{f}} && \downarrow^{\mathrlap{g_\bullet}}
     \\
     Y &\longrightarrow& J_\bullet
  }
  \,.
$$

=--

+-- {: .num_example #StandardEResolution}
###### Example
**(standard resolution)**

Consider the augmented [[cosimplicial object|cosimplicial]] which is the $\mathbb{S} \to E$-[[Amitsur complex]] [[smash product of spectra|smashed]] with $X$:

$$
  X \longrightarrow E \wedge X \stackrel{\longrightarrow}{\longrightarrow} E \wedge E \wedge X \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}
  E \wedge E \wedge E \wedge X
 \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}}
 \cdots
  \,.
$$

Its corresponding [[Moore complex]] (the sequence whose maps are the alternating sum of the above coface maps) is an $E$-Adams resolution, def. \ref{EAdamsResolution}.

=--

#### $E$-Adams towers

+-- {: .num_defn #EAdamsTower}
###### Definition

An _$E$-Adams tower_ of a spectrum $X$ is a [[commuting diagram]] in [[HoSpectra]] of the form

$$
  \array{
    && \vdots
    \\
    && \downarrow^{\mathrlap{p_2}}
    \\
    && X_2 &\stackrel{\kappa_2}{\longrightarrow}& \Omega^2 I_3
    \\
    &\nearrow& \downarrow^{\mathrlap{p_1}}
    \\
    && X_1 &\stackrel{\kappa_1}{\longrightarrow}& \Omega I_2
    \\
    &\nearrow& \downarrow^{\mathrlap{p_0}}
    \\
    X 
    &\underset{}{\longrightarrow}&
    X_0 = I_0
    &\stackrel{\kappa_0}{\longrightarrow}&
    I_1
  }
$$

such that 

1. each hook is a [[homotopy fiber sequence]];

1. the [[composition]] of the $(\Sigma \dashv \Omega)$-[[adjuncts]] of $\Sigma_{p_{n-1}}$ with $\Sigma^n \kappa_n$

   $$
     i_{n+1} \;\colon\; I_n \stackrel{\widetilde {\Sigma p_{n-1}}}{\longrightarrow}
     \Sigma^n X_n \stackrel{\Sigma^{n}\kappa_n}{\longrightarrow} I_{n+1}
   $$

   constitute an $E$-Adams resolution of $X$, def. \ref{EAdamsResolution}:

   $$
     0 \to X \stackrel{i_0}{\to} I_0 \stackrel{i_2}{\to} I_2 \stackrel{}{\to} \cdots
     \,.
   $$

Call this the _associated $E$-Adams resolution_ of the $E$-Adams tower.

The _associated inverse sequence_ is

$$
  X = X_0 \stackrel{\gamma_0}{\longleftarrow} \Omega C_1 \stackrel{\gamma_1}{\longleftarrow} C_2 \longleftarrow \cdots
$$

where $C_{k+1} \coloneqq hocofib(i_k)$.

=--

+-- {: .num_remark}
###### Remark

In ([Ravenel](#Ravenel)) it is is the associated inverse sequence that is called an $E$-Adams resolution.

=--
+-- {: .num_example}
###### Example

Every $E$-Adams resolution of $X$, def. \ref{EAdamsResolution}, induces an $E$-Adams tower, def. \ref{EAdamsTower} of which it is the associated $E$-Adams resolution.

=--

#### $E$-Adams spectral sequence

+-- {: .num_defn #EAdamsSpectralSequence}
###### Definition

Given an $E$-Adams tower as in  def. \ref{EAdamsTower}, the associated [[exact couple]] is

$$
  \array{
    \mathcal{D} && \stackrel{p}{\longrightarrow} &&  \mathcal{D}
    \\
    & {}_{\mathllap{\partial}}\nwarrow && \swarrow_{\mathrlap{\kappa}} 
    \\
    && \mathcal{E}    
  }
$$

with 

$$
  \mathcal{D} \coloneqq
  \oplus_{s,t} \mathcal{D}^{s,t}
  \coloneqq
  \oplus_{s,t} \pi_{t-s}(X_s)
$$

$$
  \mathcal{E} \coloneqq 
  \oplus_{s,t} \mathcal{E}^{s+1,t}
  \coloneqq
  \oplus_{s,t} \pi_{t-s}(\Omega^s I_{s+1})
$$

and

$$
  p \colon \pi_{t-s}(X_{s+1})\stackrel{\pi_{t-s}(p_s)}{\longrightarrow}
   X_{t-s}(X_s)
$$

$$
  \kappa \colon \pi_{t-s}(X_s)
  \stackrel{\pi_{t-s}(\kappa_s)}{\longrightarrow} \pi_{t-s}(\Omega^s I_{s+1})
$$

$$
  \partial \colon \pi_{t-s}(\Omega^s I_{s+1})
  \stackrel{\pi_{t-s}(\partial_s)}{\longrightarrow}
  \pi_{t-s}(\Sigma X_{s+1})
  \,.
$$

The $E$-Adams spectral sequence of the $E$-Adams tower is the [spectral sequence induced](exact+couple#SpectralSequencesFromExactCouples) by this exact couple.

=--

+-- {: .num_prop #UniquenessOfEAdamsSpectralSequence}
###### Proposition

Given two $E$-Adams towers, def. \ref{EAdamsTower}, for some $X$, then the corresponding two $E$-Adams spectral sequences, def. \ref{EAdamsSpectralSequence}, are [[isomorphism|isomorphic]] from the $\mathcal{E}_2$-page on

=--

#### The $\mathcal{E}_1$-term and Hopf algebroid structure

Due to prop. \ref{UniquenessOfEAdamsSpectralSequence}
we may focus attention on the standard $E$-resolution, def. \ref{StandardEResolution}.

For this one gets

$$
  \mathcal{E}_1^{s,\bullet}
  \simeq
  \pi_\bullet(E^{\wedge (s+1)}\wedge X )
  \,.
$$

+-- {: .num_defn #FlatE}
###### Definition

Call the [[ring spectrum]] $E$ _flat_ if

$$
  \eta_L,\eta_R \colon E_\bullet \longrightarrow E_\bullet(E)
$$

is a [[flat morphism]].

=--

+-- {: .num_example}
###### Example

Examples of ring spectra that are flat according to def. \ref{FlatE} include

* $E = H \mathbb{F}_p$ an [[Eilenberg-MacLane spectrum]] with $mod\;p$ [[coefficients]];

* $E = B P$ the [[Brown-Peterson spectrum]];

* $E = MU$ the [[complex cobordism cohomology theory|complex cobordism spectrum]];

Examples of ring spectra that are _not_ flat include

* $E = H \mathbb{Z}$ the [[Eilenberg-MacLane spectrum]] for [[integers|integer]] [[coefficients]];

* $E = M S U$.

=--



+-- {: .num_prop}
###### Proposition

For $E$ flat, def. \ref{FlatE}, then
$(E_\bullet, E_\bullet(E))$ (the dual $E$-[[Steenrod operations]]) is canonically a [[Hopf algebroid]].

=--

+-- {: .num_prop}
###### Proposition

For $E$ flat, def. \ref{FlatE}, the canonical map

$$
  E_\bullet(E^{\wedge n}) \otimes_{\pi_\bullet} E_\bullet(X)
  \longrightarrow
  \pi_\bullet(E^{\wedge^{(n+1)}}\wedge X  )
$$

is an [[isomorphism]].

=--

#### The $\mathcal{E}_2$-term and homological algebra of Hopf modules

+-- {: .num_prop}
###### Proposition

For $E$ flat, def. \ref{FlatE}, then the $\mathcal{E}_2$-page
of any $E$-Adams spectral sequence over $X$ is

$$
  \mathcal{E}^{s,t}_\bullet
  \simeq
  Ext^{s,t}_{E_\bullet(E)}(E_\bullet, E_\bullet(X))
  \,,
$$

where $Ext^{s,t}_{\Gamma}(-,-)$ denotes the $t$th graded piece of the $s$-th [[Ext]]-functor in the category of $\Gamma$-[[comodules]].

=--

#### Convergence, $E$-nilpotent completion and $E$-localization

... $E$-ANSS [[converges conditionally]] to the [[E-nilpotent completion]]...

...([Ravenel 84](#Ravenel84))...


...[[Bousfield localization of spectra]]... $L_E$


+-- {: .num_remark #CanonicalMapFromELocalizationToTotalization}
###### Remark

There is a canonical map

$$
  L_E X \stackrel{}{\longrightarrow} \underset{\leftarrow}{\lim}_n (E^{\wedge^{n+1}_S}\wedge_S X)
$$

from the $E$-[[Bousfield localization of spectra]] of $X$ into the [[totalization]].


=--

We consider now conditions for this morphism to be an [[equivalence]].

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

([Bousfield 79](#Bousfield79)).

For more discussion of [[E-infinity geometry|E-infinity]] (derived) [[formal completions]] via totalizations of [[Amitsur complexes]], see ([Carlsson 07](completion+of+a+module#Carlsson07)).


#### The case $E = H \mathbb{F}_p$

(...)

#### The case $E = MU$

(...)


## **3)** Geometry over $Spec(\mathbb{S})$


### Fracturing

+-- {: .num_prop #SullivanArithmeticFracture}
###### Proposition
**(Sullivan arithmetic square)**

For every [[spectrum]] $X$ the canonical square

$$
  \array{
    && L_{\mathbb{Q}}X
    \\
    & \swarrow && \nwarrow
    \\
    L_{\mathbb{Q}}
    \left(
      \prod_p L_p X
    \right)
    &&  &&
    X
    \\
     & \nwarrow && \swarrow
    \\
    && \prod_p L_p X
  }
$$

is a [[homotopy pushout]] (hence also a [[homotopy pullback]]).

=--

Original statements of this include ([Bousfield 79](#Bousfield79), [Sullivan 05, prop. 3.20](#Sullivan05)). Review includes ([van Koughnett 13, prop. 4.5](#VanKoughnett13), [Bauer 11, lemma 2.1](#Bauer11)). 


So the [[nLab:arithmetic fracture square]] from [[nLab:Weil uniformization theorem|Weil uniformization]] over [[nLab:Spec(S)]] synthesizes spectra from their formal completion and torsion approximation:

$$
  \array{
    &&  {{localization} \atop {away\;from\;p}} && \stackrel{}{\longrightarrow} && {{p-adic} \atop {residual}}
    \\
    & \nearrow & & \searrow & & \nearrow && \searrow
    \\
    { {formal\;completion} \atop {away\; from \;p} }  && && {{geometric\;bundles} \atop {with \;connection}} &&  && {{{p-torsion} \atop {approximation}} \atop {{of\;p-adic} \atop {residual}}}
    \\
    & \searrow &  & \nearrow & & \searrow && \nearrow
    \\
    && { {formal\;completion} \atop {at\;p} }
    \; && \longrightarrow && {{p-torsion} \atop {approximation}}
  }
  \,,
$$

(and there is further fracturing of the $p$-local part by [[nLab:chromatic homotopy theory]]).

+-- {: .num_prop #ReformulationOfProdOverPComletionByLocalizationAtCoproduct}
###### Proposition

The product of all [[p-completions]] is equivalently the [[Bousfield localization of spectra]] at the [[wedge sum]] $\vee_p S \mathbb{F}_p$ of all [[Moore spectra]]


$$
  \prod_p L_p X
  \simeq
   L_{\vee_p S \mathbb{F}_p} X
  \,.
$$

Moreover there is a  [[Bousfield equivalence]] 

$$
  S (\mathbb{Q}/\mathbb{Z}) \simeq_{Bousf} \vee_p S \mathbb{F}_p
  \,,
$$ 

and therefore also an equivalence

$$
  \prod_p L_p X
  \simeq
   L_{S (\mathbb{Q}/\mathbb{Z})} X
  \,.
$$


=--

The first statement originates around ([Bousfield 79, prop. 2.6](Bousfield+localization+of+spectra#Bousfield79)), review includes ([van Koughnett 13, prop. 4.4](Bousfield+localization+of+spectra#VanKoughnett13), [Bauer 11, below prop. 2.2](#Bauer11)); the second is highlighted in ([Strickland 12, MO comment](http://mathoverflow.net/a/91057/381)).


By prop. \ref{ReformulationOfProdOverPComletionByLocalizationAtCoproduct}
the arithmetic fracture square of prop. \ref{SullivanArithmeticFracture} is equivalently of the form

$$
  \array{

    && L_{H\mathbb{Q}}X
    \\
    & \swarrow && \nwarrow
    \\
    L_{H\mathbb{Q}}
    L_{S \mathbb{Q}/\mathbb{Z}} X
    &&  &&
    X
    \\
     & \nwarrow && \swarrow
    \\
    && L_{S \mathbb{Q}/\mathbb{Z}} X
  }
  \,.
$$

In this form the statement holds much more generally:

+-- {: .num_prop #GeneralFractureSquare}
###### Proposition

Let $E, F, X$ be [[spectra]] such that the $F$-[[Bousfield localization of spectra|localization]] of $X$ is $E$-acyclic, i.e.  $E_\bullet(L_F X) \simeq 0$, then the canonical square [[diagram]]


$$
  \array{
    && L_F X
    \\
    & \swarrow && \nwarrow
    \\
    L_F
    L_E X
    &&  &&
    L_{E\vee F} X
    \\
     & \nwarrow && \swarrow
    \\
    && L_E X
  }
$$

is a [[homotopy pullback]] (and hence by stability also a [[homotopy pushout]]).


=--

e.g. ([Bauer 11, prop. 2.2](#Bauer11))



### Complex oriented cohomology and $MU$, $BP$

* [[MU]], 

* [[formal group law]], [[Lazard ring]], [[Quillen's theorem on MU]]

* [[complex oriented cohomology theory]]

* [[Brown-Peterson spectrum]]

### Chromatic fracturing

+-- {: .num_remark #ExampleOfChromaticFracturing}
###### Remark

The general version of the fracture statement in prop. \ref{GeneralFractureSquare} is used frequently in [[chromatic homotopy theory]] for decomposition in [[Morava K-theory]] and [[Morava E-theory]]-localizations. For example there is a **chromatic** fracture square:

$$
  \array{
    && L_{E(n-1)} X
    \\
    & \swarrow && \nwarrow
    \\
    L_{E(n-1)}
    L_{K(n)} X
    &&  &&
    L_{E(n)} X
    \\
     & \nwarrow && \swarrow
    \\
    && L_{K(n)} X
  }
$$

In particular it is used for instance in the construction of [[tmf]], see example \ref{ConstructionOfTmf} below.

=--


### $E_\infty$-stacks

* [[stack]], [[derived stack]]

* [[A Survey of Elliptic Cohomology - the derived moduli stack of derived elliptic curves]]


## References

For section **1) Stable homotopy theory** we follow

* {#Schwede12} [[Stefan Schwede]], _Symmetric spectra_, 2012 ([pdf](http://www.math.uni-bonn.de/~schwede/SymSpec-v3.pdf))

For further reading an excellent collection is

* {#James95} [[Ioan Mackenzie James]],_[[Handbook of Algebraic Topology]]_ 1995

For **2) Adams-Novikov spectral sequence** we follow the streamlined presentation due to 

* {#Miller81} [[Haynes Miller]], _On relations between Adams spectral sequences, with an application to the stable homotopy of a Moore space_, J. Pure Appl. Algebra 20 (1981) ([pdf](http://math.mit.edu/~hrm/papers/miller-relations-between-adams-spectral-sequences.pdf))

as surveyed in ([Hopkins 99, section 5](#Hopkins99)) and expanded on in

* {#Aramian} [[Nersés Aramian]], _The Adams spectral sequence_ ([[AramianANSS.pdf:file]])

For the case $E =$ [[MU]] we may follow

* {#Adams74} [[Frank Adams]], _Stable homotopy and generalized homology_, Chicago Lectures in mathematics, 1974

For the modern picture of **3) spectral geometry over $Spec(\mathbb{S})$** we follow

* {#Hopkins99} [[Mike Hopkins]], _Complex oriented cohomology theories and the language of stacks_, course notes 1999 ([pdf](http://www.math.rochester.edu/u/faculty/doug/otherpapers/coctalos.pdf))

* [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, 2010

Useful **survey** of this picture has been given in

* {#Wilson13} [[Dylan Wilson]] section 1.2 of _Spectral Sequences from Sequences of Spectra: Towards the Spectrum of the Category of Spectra_ lecture at _[2013 Pre-Talbot Seminar](http://math.northwestern.edu/~htanaka/pretalbot2013/index.php)_ ([pdf](http://math.northwestern.edu/~htanaka/pretalbot2013/notes/2013-03-21-Dylan-Wilson-ANSS.pdf))

* {#MazelGee13} [[Aaron Mazel-Gee]], _You could've invented $tmf$_, April 2013 ([pdf slides](http://math.berkeley.edu/~aaron/writing/ustars-tmf-beamer.pdf), [notes pdf](http://math.berkeley.edu/~aaron/writing/tmf-seminar-talk.pdf))

Further references pointed to above include the following.

* {#Bousfield79} [[Aldridge Bousfield]], _The localization of spectra with respect to homology_, Topology 18 (1979), no. 4, 257--281. ([pdf](http://www.uio.no/studier/emner/matnat/math/MAT9580/v12/undervisningsmateriale/bousfield-topology-1979.pdf))

* {#Ravenel84} [[Douglas Ravenel]], _Localization with respect to certain periodic homology theories_, American Journal of Mathematics, Vol. 106, No. 2, (Apr., 1984), pp. 351-414 ([pdf](https://www.math.rochester.edu/people/faculty/doug/mypapers/loc.pdf))