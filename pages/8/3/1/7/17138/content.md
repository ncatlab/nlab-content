

{:bluebox: .un_remark style="border:solid #000000;background: #E6DF13;border-width:2px 1px;padding:0 1em;margin:0 1em;"}

***


$\,$

+-- {: .standout}

<div style="float:left;margin:0 10px 10px 0;"> <img width="200" src="http://ncatlab.org/nlab/files/BonnLogo.png"> </div> 

[V4D2 -- Algebraic Topology II](https://basis.uni-bonn.de/qisserver/rds?state=verpublish&status=init&vmfile=no&publishid=109556&moduleCall=webInfo&publishConfFile=webInfo&publishSubDir=veranstaltung)

$\;\;\;\;\;\;\;\;\;\;\;$ **Stable Homotopy Theory**

$\;\;\;\;\;\;\;\;\;\;\;$ Dr. [[Urs Schreiber]]

[Lecture](#Introduction) and [Seminar](#ComplexOrientedCohomology)

=--


$\,$

***

This page contains topics, links, literature.

Eventually lecture notes will be contained here, for the moment these are skeletal.

***


#Contents#
* table of contents
{:toc}


## Introduction
 {#Introduction}

We are concerned with the theory of _[[spectra]]_ in the sense of [[algebraic topology]]: the proper generalization of [[abelian groups]] to [[homotopy theory]]. 

### 1) Stable homotopy theory
 {#StableHomotopyTheory}

A [[group]] in homotopy theory is equivalently a [[loop space]] under concatenation of loops ("[[∞-group]]"). A double loop space is a group with some commutativity structure ("[[Eckmann-Hilton argument]]"), a triple loop space has more commutativity structure, and so forth. A _spectrum_ is where this progression of [[looping and delooping]] _stabilizes_ (an "$\infty$-abelian group"). Therefore one speaks of _[[stable homotopy theory]]_:

$$
  Spaces
  \;\;
  \underoverset{(linearization)}{stabilization}{\mapsto}
  \;\;
  Spectra
  \,.
$$

Most of [[linear algebra]] and [[algebraic geometry]] passes along as [[abelian groups]] are generalized to [[spectra]] and turns into something remarably rich, called _[[brave new algebra]]_, _[[higher algebra]]_ and _[[E-∞ geometry|spectral geometry]]_. In particular the analog of the theory of ([[commutative ring|commutative]]) [[rings]] and their [[modules]] exist, given by ([[commutative ring spectrum|commutative]]) [[ring spectra]] ([[E-∞ rings]], [[A-∞ rings]]) and [[module spectra]] ([[∞-modules]]). 

### 2) Adams spectral sequences
 {#ANSS}

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

In particular, an  [[E-∞ ring]] $E$ is [[formal dual|dually]] a morphism of $E_\infty$-algebraic spaces $Spec(E) \longrightarrow Spec(\mathbb{S})$ and under good conditions the [[1-image]] of this map is the formal dual of the [[Bousfield localization of spectra|localization]] $L_E \mathbb{S}$ at $E$:

$$
  Spec(E) \stackrel{epi_1}{\longrightarrow} Spec(L_E \mathbb{S}) \stackrel{mono_1}{\longrightarrow} Spec(\mathbb{S})
 \,.
$$

This means that $Spec(E) \longrightarrow Spec(L_E \mathbb{S})$ is a [[cover]] and that hence $E$-local spectra are equivalently [[quasicoherent ∞-stacks]] on $Spec(E)$ equipped with [[descent data]]: [[formal dual|dually]] they are [[∞-modules]] over $E$ equipped with [[comodule]] structure over the [[Hopf algebroid]] ([[Sweedler coring]]) $E \otimes_{\mathbb{S}} E$.

The computation of [[homotopy groups]] of spectra that make use of their decomposition this way into $E$-[[∞-modules]] equipped with [[descent]] data is the _$E$-[[Adams spectral sequence]]_, a central tool of the theory.

### S) Complex oriented cohomology

For this reason special importance is carried by those [[E-∞ rings]] such that $Spec(E) \to Spec(\mathbb{S})$ is already a [[covering]], for these the $E$-[[∞-modules]] equipped with descent data give an equivalent, but in general more tractable, incarnation of the stable homotopy theory of spectra.

Curiously, this way a good bit of [[differential topology]], also [[differential geometry]], arises within the abstract stable homotopy theory: the archetypical $Spec(E)$ which covers $Spec(\mathbb{S})$ is $E = $ [[MU]], the [[Thom spectrum]] for [[complex vector bundles]], representing [[complex cobordism cohomology]].

An [[commutative ring spectrum]] $E$ over $MU$, hence a $Spec(E)\to Spec(MU)$ is now a [[multiplicative cohomology theory|multiplicative]] "[[complex oriented cohomology theory]]". 


## **Part 1) Stable homotopy theory**
 
* [[stable homotopy theory]]

We follow ([Schwede 12](#Schwede12), [Schwede 15](#Schwede15)).

### Spectra

+-- {: .num_defn #OrthogonalSpectrum}
###### Definition

An _[[orthogonal spectrum]]_ $X$ consists of for each $n \in \mathbb{N}$

1. a sequence of [[pointed topological spaces]] $X_n$ (the _$n$th level_);

1. a base-point preserving [[continuous function|continuous]] [[action]] of the [[topological group|topological]] [[orthogonal group]] $O(n)$ on $X_n$;

1. based-point preserving [[continuous functions]] $\sigma_n \colon X_n \wedge S^1 \longrightarrow X_{n+1}$ from the [[smash product]] with the [[1-sphere]] (the _$n$th structure map_)

such that for all $n,k \in \mathbb{N}$ with $k \geq 1$

* the [[continuous functions]] $\sigma^k \colon X_n \wedge S^k \longrightarrow X_n \wedge S^k$ given as the [[compositions]]

  $$
    \sigma^k \colon
    X_n \wedge S^k  
     \stackrel{\sigma_n \wedge S^{k-1}}{\longrightarrow}
    X_{n+1} \wedge S^{k-1}
     \stackrel{\sigma_{n-1} \wedge S^{k-2}}{\longrightarrow}
    X_{n+2} \wedge S^{k-2}
     \stackrel{\sigma_{n-2} \wedge S^{k-3}}{\longrightarrow}
     \cdots
     \stackrel{\sigma_{n+k-2} \wedge S^{1}}{\longrightarrow}
   X_{n+k-1} \wedge S^1
     \stackrel{\sigma_{n+k-1} }{\longrightarrow}
    X_{n+k}  
  $$

  is $O(n) \times O(k)$-equivariant

  (with respect to the $O(k)$-[[action]] on $S^k$ regarded as the [[representation sphere]] of the defining action on $\mathbb{R}^k$ and via the diagonal embedding $O(n)\times O(k) \hookrightarrow O(n+k)$).

A [[homomorphism]] $f \colon X \longrightarrow Y$ of orthogonal spectra is a sequence of $O(n)$-equivariant based continuous functions $f_n \colon X_n \longrightarrow Y_n$ [[commuting diagram|commuting]] with the structure maps

$$
  \array{
    X_n \wedge S^1 & \stackrel{\sigma_n^X}{\longrightarrow} & X_{n+1}  
    \\
    \downarrow^{\mathrlap{f_n}} && \downarrow^{\mathrlap{f_{n+1}}}
    \\
    Y_n \wedge S^1 & \stackrel{\sigma_n^Y}{\longrightarrow} & Y_{n+1}      
  }
  \,.
$$

We write $OrthSpectra$ for the [[category]] of orthogonal spectra with homomorphisms between them.

=--

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


#### Stable homotopy category


+-- {: .num_defn #StabilizationMap}
###### Definition

Given an orthogonal spectrum $X$, def. \ref{OrthogonalSpectrum},
then for $n,k \in \mathbb{N}$ the _stabilization map_ $\iota_{n,k}$ on [[homotopy groups]] $\pi_\bullet(X_\bullet)$ of the level spaces $X_\bullet$ is 

$$
  \iota_{n,k}
    \;\colon\;
  \pi_{n+k} X_n
    \stackrel{(-)\wedge S^1}{\longrightarrow}
  \pi_{n+k+1}(X_n \wedge S^1)
    \stackrel{(\sigma_n)_\ast}{\longrightarrow}
  \pi_{n+k+1} X_{n+1}
  \,.
$$

=--

+-- {: .num_defn #StableHomotopyGroup}
###### Definition

Given an orthogonal spectrum $X$, def. \ref{OrthogonalSpectrum}, then for $k \in \mathbb{Z}$ its $k$th _stable [[homotopy group]]_ is the [[colimit]]

$$
  \pi_k X 
  \;\coloneqq\;
  \underset{\longrightarrow}{\lim}_n
  \pi_{n+k} X_n
$$

of the [[homotopy groups]] of the level spaces, taken with respect to the stabilization maps, def. \ref{StabilizationMap}.

=--

+-- {: .num_defn #WeakHomotopyEquivalences}
###### Definition

A homomorphism $f\colon X \longrightarrow Y$ of orthogonal spectra, def. \ref{OrthogonalSpectrum}, is a _[[weak homotopy equivalence]]_ if it induces [[isomorphisms]] (of [[abelian groups]])

$$
  \pi_\bullet(f) \;\colon\;  \pi_\bullet(X) \longrightarrow \pi_\bullet(Y)
$$

on all stable homotopy groups, def. \ref{StableHomotopyGroup}.

=--

+-- {: .num_remark}
###### Remark

The [[localization of a category|localization]]/[[simplicial localization]] of the category of orthogonal spectra, def. \ref{OrthogonalSpectrum}, at the weak homotopy equivalences, def. \ref{WeakHomotopyEquivalences}, is the  [[stable homotopy category]]/[[(infinity,1)-category of spectra]]:

$$
  L_{whe} OrthSpectra \simeq Spectra
  \,.
$$

=--


#### Symmetric monoidal smash product

+-- {: .num_defn #SmashProduct}
###### Definition

Given two orthogonal spectra $X,Y\in OrthSpectra$, def. \ref{OrthogonalSpectrum}, their _[[smash product of spectra]]_ is the orthongal spectrum

$$
  X \wedge Y \in OrthSpectrum
$$

whose $n$th level space is the [[coequalizer]] 

$$
  \left(
    \underset{p+1+q = n}{\bigvee}
     O(n)_+  \underset{O(p)\times 1 \times O(q)}{\wedge} X_p \wedge S^1 \wedge X_q
  \right)
  \stackrel{\overset{}{\longrightarrow}}{\underset{}{\longrightarrow}}
  \left(
   \underset{p+q = n}{\bigvee}
    O(n)_+ \underset{O(p)\times O(q)}{\wedge} X_p \wedge X_q
   \right)
   \longrightarrow
   \left(X\wedge Y\right)_{n}
$$

of the two maps whose components are $\sigma_p^X \wedge Y_q$ and $X_p \wedge \sigma_q^Y \circ X_p \wedge braid_{S^1, Y_q}$, respectively, and whose structure maps are induced, under the coequalizer, by the component maps $X_p\wedge \sigma_q^Y$.

=--

+-- {: .num_prop }
###### Proposition

The [[smash product of spectra]] from def. \ref{SmashProduct} naturally extends to a [[functor]]

$$
  (-)\wedge (-)
  \;\colon\;
  OrthSpectra \times OrthSpectra
  \longrightarrow
  OrthSpectra
$$

which makes $OrthSpectra$ into a [[symmetric monoidal category]] with [[unit]] the orthogonal [[sphere spectrum]] $\mathbb{S}$, example \ref{OrthogonalSphereSpectrum}.

=--

+-- {: .num_defn #BilinearHomomorphisms}
###### Definition

For $X,Y,Z \in OrthSpectrum$, def. \ref{OrthogonalSpectrum}, a _[[bilinear map|bilinear]]-homomorphism_ 
$$
  b 
    \;\colon\;
  (X,Y)
   \longrightarrow
  Z
  \,,
$$

is a collection of, for each $p,q\in \mathbb{N}$, base-point preserving $O(p) \times O(q)$-equivariant [[continuous functions]]

$$
  b_{p,q}
   \;\colon\;
  X_p \wedge X_q 
    \longrightarrow
  Z_{p+q}
$$

(out of the [[smash product]] of [[pointed topological spaces]]) which are _[[bilinear map|bilinear]]_ in that the following [[diagrams]] [[commuting diagram|commutes]]:

$$
  \array{
    X_p \wedge X_q \wedge S^1
     &\stackrel{b_{p,q} \wedge S^1}{\longrightarrow}&
    Z_{p+q} \wedge S^1
    \\
    \downarrow^{\mathrlap{X_p \wedge \sigma_q}} 
      && 
    \downarrow^{\mathrlap{\sigma_{p+q}}}
    \\
    X_p \wedge Y_{q+1}
     &\stackrel{b_{p,q+1}}{\longrightarrow}&
    Z_{p+q+1}
  }
  \;\;\;\;,\;\;\;\;\;
  \array{
    X_p \wedge X_q \wedge S^1
     &\stackrel{b_{p,q} \wedge S^1}{\longrightarrow}&
    Z_{p+q} \wedge S^1
    \\
    \downarrow^{\mathrlap{X_p \wedge braid_{X_q, S^1}}}
     &&
    \downarrow^{\mathrlap{id}}
    \\
    X_p \wedge S^1 \wedge X_q 
     &&
    Z_{p+q} \wedge S^1
    \\
    \downarrow^{\mathrlap{\sigma_p \wedge Y_q}} 
      && 
    \downarrow^{\mathrlap{\sigma_{p+q}}}
    \\
    X_p \wedge Y_{q+1}
     &\stackrel{b_{p,q+1}}{\longrightarrow}&
    Z_{p+q+1}
  }
  \,.
$$

=--

+-- {: .num_prop }
###### Proposition

The smash product of orthogonal spectra $X \wedge Y$, def. \ref{SmashProduct}, is the [[universal construction|universal]] recipient in $OrthSpectra$ of bilinear maps, def. \ref{BilinearHomomorphisms}, out of $(X,Y)$.

=--









### Higher algebra

#### Rings

* [[ring spectrum]], [[E-∞ ring]]

* [[model structure for ring spectra]]

#### Modules

* [[module spectrum]], [[∞-module]]

* [[model structure on algebras over an operad]]



### Localization

* [[Bousfield localization of spectra]]

+-- {: .num_defn #AcyclicAndLocal}
###### Definition

Let $E \in Spec$ be a [[spectrum]]. 

Say that another spectrum $X \in Spec$ is an **$E$-acyclic spectrum** if the [[smash product of spectra|smash product]] is [[zero object|zero]], $E \wedge X \simeq 0$.

Say that $X$ is an **$E$-local spectrum** if every [[morphism]]
$Y \longrightarrow X$ out of an $E$-acyclic spectrum $Y$ is homotopic to the [[zero morphism]]. 

Say that a morphism $f \colon X \to Y$ is an **$E$-equivalence** if it becomes an [[equivalence]] after [[smash product]] with $E$.

=--

(e.g. [Lurie, Lecture 20, example 4](#Lurie10))

+-- {: .num_prop #LocalizationCofiber}
###### Proposition

For $E$ a [[spectrum]], every spectrum sits in an essentially unique [[homotopy cofiber sequence]]

$$
  G_E(X) \to X \to L_E(X)
  \,,
$$

where $G_E(X)$ is $E$-acyclic, and $L_E(X)$ is $E$-local, def. \ref{AcyclicAndLocal}.

Here $X \to L_E (X)$ is characterized by two properties

1. $L_E(X)$ is $E$-local;

1. $X \to L_E(X)$ is an $E$-equivalence

according to def. \ref{AcyclicAndLocal}.

=--

(e.g. [Lurie, Lecture 20, example 4](#Lurie10))

+-- {: .num_remark #Acyclification}
###### Remark

Hence where $L_E$ is traditionally called "$E$-localization", $G_E$ might be called "$E$-acyclification", though that terminology is not used very commonly. 

=--

+-- {: .num_defn}
###### Definition

Given $E \in Spec$, 
the [[natural transformation|natural morphisms]] $X \longrightarrow L_E X$
in prop. \ref{LocalizationCofiber} exhibit the [[localization of an (infinity,1)-category]] called **Bousfield localization** at $E$.

=--


#### Nilpotent completion

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

([Bousfield 79](#Bousfield79)). see also for instance ([Bauer 11, p. 2](#Bauer11))

For more discussion of [[E-infinity geometry|E-infinity]] (derived) [[formal completions]] via totalizations of [[Amitsur complexes]], see ([Carlsson 07](completion+of+a+module#Carlsson07)).


#### Fracturing


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
    { {formal\;completion} \atop {away\; from \;p} }  && &&  &&  && {{{p-torsion} \atop {approximation}} \atop {{of\;p-adic} \atop {residual}}}
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




## **Part 2) Adams spectral sequences**

We follow ([Hopkins 99, section 5](#Hopkins99), [Aramian](#Aramian)).



#### $E$-Adams resolutions

First we consider a concept of $E$-[[injective objects]] in [[Spectra]].

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

The _associated inverse sequence_ is ...

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

Convergence

... $E$-ANSS [[converges conditionally]] to the [[E-nilpotent completion]]...


...([Ravenel 84](#Ravenel84))...


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





#### The case $E = H \mathbb{F}_p$

(... [Hatcher 04](#Hatcher04), [Rognes 12](#Rognes12)... )

#### The case $E = MU$

(...)


## **Seminar: Complex oriented cohomology**
 {#ComplexOrientedCohomology}

$\,$

+-- {: .standout}

<div style="float:left;margin:0 10px 10px 0;"> <img width="200" src="http://ncatlab.org/nlab/files/BonnLogo.png"> </div> 

[S4D2 -- Graduate Seminar on Topology](https://basis.uni-bonn.de/qisserver/rds?state=verpublish&status=init&vmfile=no&publishid=107560&moduleCall=webInfo&publishConfFile=webInfo&publishSubDir=veranstaltung)

$\;\;\;\;\;\;\;\;\;\;\;$ **Complex oriented cohomology**

$\;\;\;\;\;\;\;\;\;\;\;$ Dr. [[Urs Schreiber]]

$\;\;\;\;\;\;\;\;\;\;\;$ 

=---


$\,$

A list of possible topics. Check again a little later for more.

$\,$

### Generalised cohomology


**Cohomology theory and Spectra

See for instance ([Aguilar-Gitler-Prieto 02, chapters 7,8 and 12](#AguilarGitlerPrieto02)).

* [[ordinary cohomology]], [[topological K-theory]]

* [[generalized (Eilenberg-Steenrod) cohomology]]

* [[Brown representability theorem]]


**Cobordism cohomology theory**

See maybe ([Francis 10](#Francis10))

* [[Pontrjagin-Thom construction]]

  * [[Thom isomorphism]]

* [[Thom space]], [[Thom spectrum]], [[MO]]

* [[cobordism]], [[cobordism ring]]

* [[cobordism cohomology theory]]

* [[Thom's theorem]]


### Complex oriented cohomology

See ([Hopkins 99](#Hopkins99), [Lurie 10](#Lurie10)) 

**Complex orientation**

* [[complex oriented cohomology theory]]

  * generalized [[Chern classes]]

* [[complex cobordism cohomology]] 

  * [[MU]]

* [[Lazard's theorem]]

  * [[formal group law]], 

  * [[Lazard ring]], 

* [[Quillen's theorem on MU]]

* [[universal complex orientation on MU]]

* [[Landweber exact functor theorem]]

**Geometry of $Spec(MU)$**

* [[moduli space of formal groups]]

  * [[height of a formal group]]

  * [[moduli space of elliptic curves]]

* [[Landweber-Novikov theorem]]

* [[Adams-Quillen theorem]]

$\,$

***

$\,$

## References

### Basic

For section **1) Stable homotopy theory** we follow

* {#Schwede12} [[Stefan Schwede]], _Symmetric spectra_, 2012 ([pdf](http://www.math.uni-bonn.de/~schwede/SymSpec-v3.pdf))

(for [[symmetric spectra]]) or rather 

* {#Schwede15} [[Stefan Schwede]], _Global homotopy theory_, 2015 ([pdf](http://www.math.uni-bonn.de/people/schwede/global.pdf))

(for [[orthogonal spectra]]; for our purposes take throughout $\mathcal{F} = \{1\}$ on p. 4 to be the trivial collection of groups).

For **2) Adams spectral sequence** we follow the streamlined presentation due to 

* {#Miller81} [[Haynes Miller]], _On relations between Adams spectral sequences, with an application to the stable homotopy of a Moore space_, J. Pure Appl. Algebra 20 (1981) ([pdf](http://math.mit.edu/~hrm/papers/miller-relations-between-adams-spectral-sequences.pdf))

as surveyed in ([Hopkins 99, section 5](#Hopkins99)) and expanded on in

* {#Aramian} [[Nersés Aramian]], _The Adams spectral sequence_ ([[AramianANSS.pdf:file]])

For the case $E =$ [[MU]] we may follow

* {#Adams74} [[Frank Adams]], _Stable homotopy and generalized homology_, Chicago Lectures in mathematics, 1974

For  **S) Complex oriented cohomology ** we follow

* {#AguilarGitlerPrieto02} Marcelo Aguilar, [[Samuel Gitler]], Carlos Prieto, section 12 of _Algebraic topology from a homotopical viewpoint_, Springer (2002) ([toc pdf](http://tocs.ulb.tu-darmstadt.de/106999419.pdf))

* {#Hopkins99} [[Mike Hopkins]], _Complex oriented cohomology theories and the language of stacks_, course notes 1999 ([pdf](http://www.math.rochester.edu/u/faculty/doug/otherpapers/coctalos.pdf))

* {#Lurie10} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, 2010

### Further reading

For further reading on stable homotopy theory an excellent collection is

* {#James95} [[Ioan Mackenzie James]], _[[Handbook of Algebraic Topology]]_ 1995

Useful quick survey of the modern big picture may be found in

* {#Wilson13} [[Dylan Wilson]] section 1.2 of _Spectral Sequences from Sequences of Spectra: Towards the Spectrum of the Category of Spectra_ lecture at _[2013 Pre-Talbot Seminar](http://math.harvard.edu/~hirolee/pretalbot2013/)_, March 2013 ([[DylanWilsonOnANSS.pdf:file]])

* {#MazelGee13} [[Aaron Mazel-Gee]], _You could've invented $tmf$_, April 2013 ([pdf slides](http://math.berkeley.edu/~aaron/writing/ustars-tmf-beamer.pdf), [notes pdf](http://math.berkeley.edu/~aaron/writing/tmf-seminar-talk.pdf))

Further lecture notes pointed to above include

* {#Hatcher04} [[Alan Hatcher]], _[Spectral sequences in algebraic topology](http://www.math.cornell.edu/~hatcher/SSAT/SSATpage.html)_ _II: The Adams spectral sequence_, 2004 ([pdf](http://www.math.cornell.edu/~hatcher/SSAT/SSch2.pdf))

* {#Francis10} [[John Francis]] (notes by [[Owen Gwilliam]]), _[Topology of manifolds](http://math.northwestern.edu/~jnkf/classes/mflds/)_, 2010, _Lecture 2: Cobordism_ ([pdf](http://math.northwestern.edu/~jnkf/classes/mflds/2cobordism.pdf)), _Lecture 3: Thom's theorem_ ([pdf](http://math.northwestern.edu/~jnkf/classes/mflds/3thom.pdf))


* {#Bauer11} [[Tilman Bauer]], _Bousfield localization and the Hasse square_, 2011  ([pdf](http://math.mit.edu/conferences/talbot/2007/tmfproc/Chapter09/bauer.pdf))

* {#Rognes12} [[John Rognes]], _The Adams spectral sequence_ (following [Bruner](#Bruner)), 2012 ([pdf](http://folk.uio.no/rognes/papers/notes.050612.pdf))

Further original references pointed to above include the following:

* {#Bousfield79} [[Aldridge Bousfield]], _The localization of spectra with respect to homology_, Topology 18 (1979), no. 4, 257--281. ([pdf](http://www.uio.no/studier/emner/matnat/math/MAT9580/v12/undervisningsmateriale/bousfield-topology-1979.pdf))

* {#Ravenel84} [[Douglas Ravenel]], _Localization with respect to certain periodic homology theories_, American Journal of Mathematics, Vol. 106, No. 2, (Apr., 1984), pp. 351-414 ([pdf](https://www.math.rochester.edu/people/faculty/doug/mypapers/loc.pdf))

And last not least, there is

* [[Doug Ravenel]], _[[Complex cobordism and stable homotopy groups of spheres]]_, 1987/2003 ([pdf](http://www.math.rochester.edu/people/faculty/doug/mybooks/ravenelA1.pdf))


[[!redirects geometry of physics -- stable homotopy types]]