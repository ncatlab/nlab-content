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

_Bousfield localization of spectra_ refers generally to [[localization of an (∞,1)-category|localizations]] of the [[stable (∞,1)-category of spectra]] at the collection of [[morphisms]] which become [[equivalences]] under [[smash product]] with a given [[spectrum]] $E$. Since any such $E$ represents a [[generalized homology theory]], this may also be thought of  _$E$-[[homology localization]]_.

More specifically, if the [[stable (∞,1)-category of spectra]] is [[presentable (infinity,1)-category|presented]] by a ([[stable model category|stable]]) [[model category]], then the [[localization of an (∞,1)-category|∞-categorical localization]] can be presented by the operation of  _[[Bousfield localization of model categories]]_. The original article ([Bousfield 79](#Bousfield79)) essentially considered localization at the level of [[homotopy categories]].

Specifically, for $E \in Spec$ a [[spectrum]], the _Bousfield localization at $E$_ of another [[spectrum]] $X$ is the [[universal property|universal map]]

$$
  X \longrightarrow L_E X
$$

to the _$E$-[[local spectrum]]_ $L_E X$, with the property that for $Y$ any $E$-acyclic spectrum in that $Y \wedge E \simeq 0$, every morphism $Y \longrightarrow L_E X$ is null-homotopic (a [[zero morphism]] in the [[stable (∞,1)-category of spectra]]). (see for instance [Lurie 10, Example 4](#LurieLecture))

For $E = M \mathbb{Z}_p$ the [[Moore spectrum]] of the [[cyclic group]] $\mathbb{Z}_p \coloneqq \mathbb{Z}/p\mathbb{Z}$ for some [[prime number]] $p$, this $E$-localization is _[[p-completion]]_. (see for instance [Lurie 10, Examples 7 and 8](#LurieLecture))

## Definition

+-- {: .num_defn #AcyclicAndLocal}
###### Definition


Let $E \in Spec$ be a [[spectrum]]. 

Say that another spectrum
$X \in Spec$ is an **$E$-acyclic spectrum** if the [[smash product]]
is [[zero object|zero]], $E \wedge X \simeq 0$.

Say that $X$ is an **$E$-local spectrum** if every [[morphism]]
$Y \longrightarrow X$ out of an $E$-acyclic spectrum $Y$ is homotopic to the [[zero morphism]]. 

Say that a morphism $f \colon X \to Y$ is an **$E$-equivalence** if it becomes an [[equivalence]] after [[smash product]] with $E$.

=--

(e.g. [Lurie, Lecture 20, example 4](#LurieLecture))

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

(e.g. [Lurie, Lecture 20, example 4](#LurieLecture))

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

## Properties

### At Moore spectra of abelian groups

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



### Fracture theorem

The [[fracture theorem]] says how Bousfield localization at [[coproduct]] of spectra is a [[homotopy pullback]] of Bousfield localization separately. See at _[[fracture theorem]]_ for more on this.


## Examples

### General

+-- {: .num_example #EModulesAreELocal}
###### Example

For $E$ an [[E-∞ ring]], every [[∞-module]] $X$ over $E$ is $E$-local, def. \ref{AcyclicAndLocal}.

=--

(e.g. [Lurie, Lecture 20, example 5](#LurieLecture))

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

be the corresponding [[Moore spectrum]]. Then a spectrum which corresponds to a [[chain complex]] under the [stable Dold-Kan corespondence](module+spectrum#StableDoldKanCorrespondence) is $E$-local, def. \ref{AcyclicAndLocal}, if that chain complex has [[chain homology]] groups being $\mathbb{Z}[p^{-1}]$-modules.

The $E$-localization of a spectrum in this case is  _[[p-completion]]_.

=--

(e.g. [Lurie, Lecture 20, example 8](#LurieLecture))

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

* [[K(n)-local stable homotopy theory]]

## References

Original articles are

* {#Bousfield79} [[Aldridge Bousfield]], _The localization of spectra with respect to homology_ , Topology vol 18 (1979) ([pdf](http://www.uio.no/studier/emner/matnat/math/MAT9580/v12/undervisningsmateriale/bousfield-topology-1979.pdf))

* {#Ravenel84} [[Douglas Ravenel]], _Localization with respect to certain periodic homology theories_, American Journal of Mathematics, Vol. 106, No. 2, (Apr., 1984), pp. 351-414 ([pdf](https://www.math.rochester.edu/people/faculty/doug/mypapers/loc.pdf)) 

Lecture notes include

* N. Aramian, _Bousfield Localization_ ([pdf](http://www.math.uiuc.edu/~aramyan2/bousfield.pdf))

* {#Bauer11} [[Tilman Bauer]], _Bousfield localization and the Hasse square_, 2011  ([pdf](http://math.mit.edu/conferences/talbot/2007/tmfproc/Chapter09/bauer.pdf))
 
* {#VanKoughnett13} [[Paul VanKoughnett]], _Spectra and localization_, 2013 ([[VanKoughnettLocalization.pdf:file]])


Discussion the general context of [[higher algebra]]/[[stable homotopy theory]] includes

* {#LurieLecture} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture notes (2010) ([web](http://www.math.harvard.edu/~lurie/252x.html)),  Lecture 20 _Bousfield localization_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture20.pdf))

* {#LurieProper} [[Jacob Lurie]], section 4 of _[[Proper Morphisms, Completions, and the Grothendieck Existence Theorem]]_ 

Discussion specifically of [[K(n)-local spectra]] includes

* [[Michael Hopkins]], [[Jacob Lurie]], _[[Ambidexterity in K(n)-Local Stable Homotopy Theory]]_

See also

section 2.4 of

* Holger Reeker, _On K(1)-local SU-bordism_ ([arXiv:0907.4299](http://arxiv.org/abs/0907.4299))

[[!redirects local spectrum]]
[[!redirects local spectra]]

[[!redirects localization of a spectrum]]
[[!redirects localization of spectra]]