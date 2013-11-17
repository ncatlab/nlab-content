
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
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

The _Adams spectral sequence_ ([Adams 58](#Adams58)) is a type of [[spectral sequences]] used for computations  in [[stable homotopy theory]]. It computes the [[homotopy groups]] of a [[spectrum]] from its [[homology]]/[[cohomology]], as [[modules]]/[[comodules]] over its [[cohomology operations]]. The Adams spectral sequence can be seen as a variant of the [[Serre spectral sequence]] obtained by replacing a single fibration by an "[[Adams resolution]]".

The original Adams spectral sequence for [[ordinary cohomology]] is further refined by the _[[Adams-Novikov spectral sequence]]_ ([Novikov 67](#Novikov67)) by replacing [[ordinary cohomology]] modulo $p$ by [[complex cobordism cohomology theory]] or [[Brown-Peterson theory]] or the like. Generally, for $E$ a suitable [[E-infinity ring]] there is a corresponding $E$-Adams(-Novikov) spectral sequence whose second page is given by $E$-[[generalized cohomology]].

Working with the Adams spectral sequence tends to be fairly involved, as is clear from the subtlety of the results it computes (notably [[stable homotopy groups of spheres]]) and as witnessed by the fact that one uses further [[spectral sequences]] just to compute the low pages of the Adams spectral sequence, e.g. the [[May spectral sequence]] and the  [[chromatic spectral sequence]]. 

A neat conceptual picture of what happens in the Adams spectral sequence has emerged long after its conception with the arrival of [[higher algebra]] in [[stable (infinity,1)-category|stable infinity-category theory]]. A nice, brief, illuminating modern (and funny) account of this is in ([Wilson 13](#Wilson13)), further details are in ([Lurie 10](#Lurie10)).


## Motivation from Hurewicz theorem and Serre spectral sequence
 {#MotivationFromHurewiczTheoremAndSerreSpectralSequence}

The Adams spectral sequence may be motivated from the strategy to 
compute [[homotopy groups]] from [[cohomology groups]] by subsequently applying the [[Hurewicz theorem]] to compute the lowest-degree non-trivial homotopy group from the corresponding [[cohomology group]], then co-killing that by forming its [[homotopy fiber]], finally applying the [[Serre spectral sequence]] to  identify the next lowest non-trivial cohomology group of that fiber, and then iterating this process. The Adams spectral sequence arises when in this kind of strategy instead of co-killing only the lowest lying [[cohomology group]], one at a time, one co-kills _all_ nontrivial cohomology groups, then forms the corresponding [[homotopy fiber]] and so on.

This was apparently historically the way that [[John Adams]] indeed proceeded from [[Jean-Pierre Serre]]'s approach and this is still a good motivation for the whoe construction, a nice exposition is in  ([Wilson 13, 1.1](#Wilson13)).

We now say this again in more detail.

Given $n \in \mathbb{N}$, consider the probem of computing the [[homotopy groups]] $\pi_k(S^n) \;mod \;2$ of the $n$-[[sphere]] $S^n$. For $k \leq n$ this is clear: first for $k \}lt n$ they all vanish, and second for $k = n$ we have, by the very nature of [[Eilenberg-MacLane spaces]] $K(\mathbb{Z}_2, n)$, that the [[ordinary cohomology]] is

$$
  H^n(S^n, \mathbb{Z}_2) \simeq [S^n, K(\mathbb{Z}_2,n)] \simeq \pi_n(K(\mathbb{Z}_2,n)) \simeq \mathbb{Z}_2
$$

so that by the [[Hurewicz theorem]] it follows that also

$$
  \pi_n(S^n) \;mod\;2 \;\simeq \mathbb{Z}_2
  \,.
$$

The [[Hurewicz theorem]] does not say anything beyong the first non-vanishing cohomology group, but so to apply it again we can move up one step in the [[Whitehead tower]] of $S^n$ and hence consider the [[homotopy fiber]]

$$
  \array{
     F_1
     \\
     \downarrow
     \\
     S^n &\stackrel{c_1}{\longrightarrow}& K(\mathbb{Z}_2,n)
  }
$$

of the generator $[c_1] = 1 \in \pi_n(S^n) \simeq \mathbb{Z}_2$.

To apply the [[Hurewicz theorem]] to that fiber we need to know its lowest non-trivial [[cohomology group]] again, and this is computed via the [[Serre spectral sequence]] applied to this [[fiber sequence]]. 

From here on the process repeats, and one moves higher through the [[Whitehead tower]] of $S^n$


$$
  \array{
     \vdots
     \\
     \downarrow
     \\
     F_1 &\stackrel{c_2}{\longrightarrow}& K(\mathbb{Z}_2, n+1)
     \\
     \downarrow
     \\
     S^n &\stackrel{c_1}{\longrightarrow}& K(\mathbb{Z}_2,n)
  }
  \,.
$$

The Adams spectral sequence arises from this strategy by co-killing not just the first non-trivial [[cohomology group]] at each stage, but _all_ nontrivial cohomology groups at a given stage.

This is done in [[stable homotopy theory]], so let now $X$ be a [[spectrum]] (for instance the [[sphere spectrum]] $X = \mathbb{S}$ if we still with the computation of the [[stable homotopy groups of spheres]]). Write $H \mathbb{F}_2$ for the [[Eilenberg-MacLane spectrum]] for [[ordinary cohomology]] with [[coefficients]] in $\mathbb{Z}_2$, so that an element in [[cohomology]]

$$
  [c] \in H^n(X) 
$$

is represented by the [[homotopy class]] of a [[homomorphism]] of [[spectra]] of the form

$$
  c \;\colon\;  X \longrightarrow \Sigma^n H\mathbb{F}_2
$$

(a [[cocycle]]), where "$\Sigma$" denotes [[suspension]], as usual.

If $X$ is a [[finite spectrum]] then there is a [[finite]] $I$ of non-trivial cohomology classes like this, and a choice of [[cocycles]] $c_i$ for each of them gives a single map

$$
  f_0 \coloneqq (c_i)_I \;\; X \longrightarrow K_0 \coloneqq \wedge_{i \in I} \Sigma^{n_i}H \mathbb{F}_2
$$

into a [[generalized Eilenberg-MacLane spectrum]]. As before, this map classifies its [[homotopy fiber]]

$$
  \array{
    F_1
    \\
    \downarrow
    \\
     X &\stackrel{f_0}{\longrightarrow}& K_0
  }
$$

which may be thought of as encoding all information about $X$ beyond its [[cohomology groups]]. Iterating this process gives the corresponding analog of the [[Whitehead tower]], called the _[[Adams resolution]]_ of $X$:

$$
  \array{
    \vdots
    \\
    \downarrow
    \\
    F_2 &\stackrel{f_2}{\longrightarrow}& K_2
    \\
    \downarrow
    \\
    F_1 &\stackrel{f_1}{\longrightarrow}& K_1
    \\
    \downarrow
    \\
     X &\stackrel{f_0}{\longrightarrow}& K_0
  }
  \,.
$$

The Adams spectral sequence is that induced by the [[exact couple]] obtained by applying $\pi_\bullet$ to this [[Adams resolution]].

We now say this more in detail.

The [[long exact sequences of homotopy groups]] for all the [[homotopy fibers]] in this diagram arrange into a diagram of the form

$$
  \array{
    \vdots
    \\
    \downarrow & \nwarrow
    \\
    \pi_\bullet(F_2) &\stackrel{\pi_\bullet(f_2)}{\longrightarrow}& \pi_\bullet(K_2)
    \\
    \downarrow & \nwarrow^{\mathrlap{\partial_2}}
    \\
    \pi_\bullet(F_1) &\stackrel{\pi_\bullet(f_1)}{\longrightarrow}& \pi_\bullet(K_1)
    \\
    \downarrow & \nwarrow^{\mathrlap{\partial_1}}
    \\
    \pi_\bullet(X) &\stackrel{\pi_\bullet(f_0)}{\longrightarrow}& \pi_\bullet(K_0)
  }
  \,,
$$

where the diagonal maps are the [[connecting homomorphisms]] and hence decrease degree in $\pi_\bullet$ by one.
The idea now is to compute the [[homotopy groups]] of $X$ from the decomposed information in this diagram as follows.

First, by construction the homotopy groups $\pi_\bullet(K_s)$ are known, therefore we can identify elements 

$$
  \sigma \in \pi_\bullet(X)
$$

if they come from elements 

$$
  \sigma_s \in \pi_\bullet(X_s)
$$

whose image 

$$
  \pi_\bullet(f_s)(\sigma_s) \in \pi_\bullet(K_s)
$$

we understand. So the task is to understand the image of $\pi_\bullet(f_s)$ in $\pi_\bullet(K_s)$, for each $s$.

By [[exact sequence|exactness]] an element $\kappa_s \in \pi_\bullet(K_s)$ is in this image if its image 

$$
  \rho_{s+1} \coloneqq \partial(\kappa_s) \in \pi_{\bullet-1}(X_{s+1})
$$

vanishes. Now, by construction of the resolution, "evidence" for this is that $f_{s+1}(\partial(\kappa_s)) \in \pi_{\bullet-1}(K_{s+1})$ vanishes, which in turn by [[exact sequence|exactness]] means equivalently that $\partial(\kappa_s)$ is the image of an element  $\rho_{s+2} \in  \pi_{\bullet-1}(X_{s+2}) \to \pi_{\bullet-1}(X_{s+1})$. Now again "evidence" for $\rho_{s+2}$ to vanish is that its image $f_{s+2}(\rho(s+2))$ vanishes, which again means that it comes from an element $\rho_{s+3} \in  \pi_{\bullet-1}(X_{s+3}) \to \pi_{\bullet-1}(X_{s+2})$.

Proceeding by [[induction]] this way, we find that accumulated "evidence" in homotopy groups of $K_\bullet$ for an element $\kappa_s$ to represent an element in $\pi_\bullet(X)$ is that its differential $\partial \kappa_s$ factors through all the $\pi_{\bullet-1}(X_{s+k}) \to \pi_{\bullet-1}(X_s)$. This in turn means that it factors through the [[inverse limit]] $\underset{\leftarrow}{\lim}_s \pi_{\bullet-1}(X_s)$.
Such an element $\kappa_s$ with 

$$
  \partial \kappa_s \in \underset{\leftarrow}{\lim}_s \pi_{\bullet-1}(X_s) \to \pi_{\bullet-1}(X_{s+1})
$$

is called a _permanent cycle_.

In good cases, the [[Adams resolution]] is indeed a [[resolution]] which means that  the [[inverse limit]] $\underset{\leftarrow}{\lim}_s X_s $ is in fact [[contractible]]. This means that all the "evidence" accumulated in a permanent cycle is indeed sufficient evidence to prove the existence of an element $\sigma_s \in \pi_\bullet(X_s)$ and hence of an element $\sigma \in \pi_\bullet(X)$.


A trivial way for this to be the case is that the original $\sigma_s$ is itself in the image under $\partial$ of some element, in which case $\kappa_s = 0$ already all by itself. These elements are called _eventual boundaries_. Therefore if the Adams resolution is indeed a resolution the quotient group

$$
  \frac{permanent\;cycles}{eventual\;bounaries}
$$

gives elements in $\pi_\bullet(S)$, and this quotient is what the Adams spectral sequence computes.






## Definition

> under construction

### Traditional

Given a [[connective spectrum]] $X$ such that $H^\bullet(X)$
has finite type, then for each [[prime number]] $p$ there exists a [[spectral sequence]] which converges to the [[homotopy groups]] of $X$ modulo $p$ $\pi_ast(X) \otimes \mathbb{Z}_p$ and whose $E^2$-page is

$$
  E_2^{s,t} \simeq  Ext_A^{s,t}(H^\bullet(X), \mathbb{Z}/(p) )
$$

where $A$ is the [[Steenrod algebra]]. 

This is built via an [[Adams resolution]]

$$
  \array{
    X = X_0 &\stackrel{g_0}{\leftarrow}&  X_1 &\stackrel{g_1}{\leftarrow}& X_2 &\stackrel{g_2}{\leftarrow}& X_3 &\stackrel{}{\leftarrow}& \cdots
    \\
    \downarrow^{\mathrlap{f_0}} && \downarrow^{\mathrlap{f_1}} && \downarrow^{\mathrlap{f_2}} && \downarrow^{\mathrlap{f_3}} &&
    \\
    K_0 && K_1 && K_2 && K_2
  }
$$

The [[long exact sequence]] induced by this give an [[exact couple]] and the Adams spectral sequence is the corresponding [[spectral sequence]].

This is due to ([Adams 58](#Adams58)). A review is around ([Ravenel, theorem, 2.1.1, def. 2.1.8](#Ravenel)).

### Via cosimplicial spectra 

Let $p$ be a [[prime number]]. Write

$$
  R \coloneqq H \mathbb{F}_p
$$

for the [[Eilenberg-MacLane spectrum]] of the [[field]] $\mathbb{F}_p$. The [[A-∞ algebra]] structure on this induces an [[augmentation|augmented]] [[cosimplicial object|cosimplicial]] [[spectrum]]

$$
  \overline{R}^\bullet \;\colon\; k \mapsto R^{\otimes k}
  \,.
$$

Write $R^\bullet$ for the underlying [[cosimplicial object]] (here and in the following the overline indicates [[augmentation]]).

For $X$ any other [[spectrum]], [[tensor product|tensoring]] induces the (augmented) cosimplicial spectrum

$$
  \overline{X}^\bullet \coloneqq X \otimes \overline{R}^\bullet
  \,.
$$

Now the [[augmentation]] morphism induces a canonical map from $\overline{X}^{-1}$ into the [[totalization]] of $X^\bullet$

$$
  \overline{X}^{-1} \longrightarrow Tot X^\bullet
  \,.
$$

The Adams spectral sequence computes the [[kernels]] of the morphisms on [[homotopy groups]] of this map. 

In this form this appears as ([Lurie 10, theorem 2](#Lurie10)). For the traditional formulation see ([Ravenel, ch. 3, prop. 3.1.2](#Ravenel)).

## Definition 

### Spectral sequences for homotopy groups of filtered objects

Let $\mathcal{C}$ be a [[presentable (∞,1)-category|presentable]] [[stable (∞,1)-category]] such as the [[stable (∞,1)-category of spectra]].

+-- {: .num_defn #GeneralizedFilteredObject}
###### Definition

A _generalized [[filtered object]]_ in $\mathcal{C}$ is
simply a sequential diagram $X \colon (\mathbb{Z}, \lt) \to \mathcal{C}$

$$
  \cdots
  X_{n+1} \to X_n \to X_{n-1} \to \cdots
  \,.
$$

Or rather, the object being filtered is the [[homotopy limit]]

$$
  X \coloneqq \underset{\leftarrow}{\lim}_n X_n
$$

and the sequential diagram exhibits the filtering.

=--

+-- {: .num_defn #ExactCoupleForFilteredObject}
###### Definition

For a generalized filtered object $X_\bullet$, def. \ref{GeneralizedFilteredObject}, write 

$$
  F_n \coloneqq fib(X_n \to X_{n+1})
$$

for the [[homotopy fiber]] of the $n$th structure map, for all $n \in \mathbb{Z}$ and define an [[exact couple]]

$$
  \array{
    && \pi_\bullet(F_\bullet)
    \\
    & \swarrow && \nwarrow
    \\
    \pi_\bullet(X_\bullet)
    && 
       \stackrel{}{\longrightarrow}
    && 
    \pi_\bullet(X_\bullet)
  }
$$

where the maps are given by the [[long exact sequence of homotopy groups]].

=--

+-- {: .num_prop #FiltrationSpectralSequence}
###### Proposition

If $X_n \simeq 0$ for $n \ggt 0$ and Mittag-Lefler conditions are satisfied (...) then the [[spectral sequence]] induced by the [[exact couple]]
of def. \ref{ExactCoupleForFilteredObject} converges to the [[homotopy groups]] of the [[homotopy limit]] $\underset{\leftarrow}{\lim}_n X_n$ of the generalized filted object:

$$
  E^{p,q}_1
  =
  \pi_{p+q} F_{p-1}
  \Rightarrow
  \pi_{p+q} (\underset{\leftarrow}{\lim} X_\bullet) 
$$

=--

This is due to...


### Homotopy groups of totalizations filtered by coskeleta
 {#HomotopyGroupsOfOfTotalizationsFilteredByCoskeleta}

+-- {: .num_defn #FiltrationOfTotalizationByTotalizationOfCoskeleta}
###### Definition

Given an [[cosimplicial object]] 

$$
  Y \;\colon\; \Delta  \longrightarrow \mathcal{C}
$$

its [[totalization]] $Tot Y \simeq \underset{\leftarrow}{\lim}_n Y_n$
is filtered, def. \ref{GeneralizedFilteredObject} by the 
totalizations of its [[coskeleton|coskeleta]]

$$
  Tot Y 
  \to 
  \cdots 
  \to 
  Tot (cosk_2 Y) 
  \to
  Tot (cosk_1 Y) 
  \to
  Tot (cosk_0 Y) 
  \to 0
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

The filtration spectral sequence, prop. \ref{FiltrationSpectralSequence},
applied to the filtration of a [[totalization]] by [[coskeleton|coskeleta]] as in def. \ref{FiltrationOfTotalizationByTotalizationOfCoskeleta}, has as $E_2$-term the [[cohomology groups]] of the [[Moore complex]] associated with the cosimplicial objecz

$$
  E_2^{p,q}
  = 
  H^p(\pi_q(Tot (cosk_\bullet(Y))))
  \Rightarrow
  \pi_{p-q} Tot(Y)
  \,.
$$


=--

This is ([[Higher Algebra|Higher Algebra, remark 1.2.4.4]]). Review is around  ([Wilson 13, theorem 1.2.4](#Wilson13)).

### Canonical cosimplicial resolution of $E_\infty$-algebras


+-- {: .num_defn}
###### Definition

Let $S$ be an [[E-∞ ring]] and let $R$ be an [[E-∞ algebra]] over $S$, hence an [[E-∞ ring]] equipped with a [[homomorphism]]

$$
  S \longrightarrow R
  \,.
$$

The _canonical [[cosimplicial object]]_ 
associated to this (the _[[Sweedler coring]]_) is 

$$
  R^{\wedge^{\bullet+1}_S} \;\colon\; \Delta \to \mathcal{C}
  \,.
$$

More generally, for $X$ an $S$-[[∞-module]], the canonical [[cosimplicial object]] is

$$
  R^{\wedge^{\bullet+1}_S}\wedge_S X \;\colon\; \Delta \to \mathcal{C}
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

If $E$ is such that the self-[[generalized homology]] 
$E_\bullet(E) \coloneqq \pi_\bullet(E \wedge_S E)$ (the dual $E$-[[Steenrod operations]]) is such that as a [[module]] over $E_\bullet \coloneqq \pi_\bullet(E)$ it is a [[flat module]], then 

$$
  \pi_\bullet
  \left(
  \right)
$$

=--



### The $E$-Adams spectral sequence

## Properties

### Relation to Steenrod algebra

The $E_2$-page of the Adams spectral sequence for the $p$-component of 
$\pi_{n+k}(S^n)$  is the ordinary [[Steenrod algebra]] (for given prime $p$).

More generally, For $R$ an [[E-infinity ring]] such that its dual $R$-[[Steenrod algebra]] in the form of the self-[[homology]] $R_\bullet(R)$ is a [[Hopf algebroid]] over $R_\bullet = \pi_\bullet(R)$ (see at [Steenrod algebra -- Hopf algebroid structure](Steenrod+algebra#HopfAlgebraStructure)), then the $E^2$-term of the $E$-Adams spectral sequence is an [[Ext]] of $E_\bullet(E)$-[[comodules]]

$$
  E^2 \simeq Ext_{R_\bullet(R)}(R_\bullet, R_\bullet(X))
  \,.
$$

See the [references below](#ReferencesHopfAlgebroidStructure).

## Related concepts

* [[Adams-Novikov spectral sequence]]

* [[May spectral sequence]]

* [[Steenrod algebra]]

## References

### General

The original articles are

* [[John Adams]], _On the structure and applications of the Steenrod algebra_, Comm. Math. Helv. 32 (1958),
180&#8211;214.
 {#Adams58}

* [[Sergei Novikov]], _The methods of algebraic topology from the viewpoint of cobordism theories_, Izv. Akad. Nauk. SSSR. Ser. Mat. 31 (1967), 855&#8211;951 (Russian).
 {#Novikov67}

Convergence is nicely treated at the end of

* A. K. Bousfield, _The localization of spectra with respect to homology_, Topology 18 (1979), no. 4, 257--281. 

A unique homological perspective is provided in

* [[Haynes Miller]], _On relations between Adams spectral sequences, with an application to the stable homotopy of a Moore space_, J. Pure Appl. Algebra 20 (1981)

Trasditional reviews include

* [[John Adams]], part III of _Stable homotopy and generalised homology, University of Chicago Press, Chicago, Ill., 1974, Chicago Lectures in Mathematics.

* [[Doug Ravenel]], _[[Complex cobordism and stable homotopy groups of spheres]]_, page 8 of chapter I _An introduction to the homotopy groups of spheres_ ([pdf](http://www.math.rochester.edu/people/faculty/doug/mybooks/ravenel1.pdf)) and section 1 of chapter 2
 {#Ravenel}

  also Section A.6 of Ravenel's orange book 1992

* [[Paul Goerss]], _The Adams-Novikov spectral sequence and the Homotopy Groups of Spheres_, lecture notes 2007 ([pdf](http://www.math.northwestern.edu/~pgoerss/papers/stras1.pdf))
 {#Goerss2007}

* [[Alan Hatcher]], _[Spectral sequences in algebraic topology](http://www.math.cornell.edu/~hatcher/SSAT/SSATpage.html)_ _II: The Adams spectral sequence_ ([pdf](http://www.math.cornell.edu/~hatcher/SSAT/SSch2.pdf))

See also

* Nerses Aramian, _The Adams spectral sequence_ ([pdf](http://www.math.uiuc.edu/~bertg/Aramian_ASS.pdf))

* [[Alexander Kupers]], _An introduction to the Adams spectral sequence_ ([pdf](http://math.stanford.edu/~kupers/adamsss.pdf))

* R. Bruner, _An Adams spectral sequence primer_ ([pdf](http://www.math.wayne.edu/~rrb/papers/adams.pdf))

* Michael Adamaszek, _An elementary guide to the Adams-Novikov $Ext$_ ([pdf](http://www.math.uni-bremen.de/~aszek/bp.pdf))

* [pdf](http://www.math.harvard.edu/~sia/notes/classical_topology_adams.pdf)


A nice review from the modern point of view of [[higher algebra]] is in 

* [[Dylan Wilson]] _Spectral Sequences from Sequences of Spectra: Towards the
Spectrum of the Category of Spectra_ lecture at [2013 Pre-Talbot Seminar](http://math.northwestern.edu/~htanaka/pretalbot2013/index.php) ([pdf](http://math.northwestern.edu/~htanaka/pretalbot2013/notes/2013-03-21-Dylan-Wilson-ANSS.pdf))
 {#Wilson13}

More review along these lines is in

* [[Jacob Lurie]], _[Chromatic homotopy theory lecture](http://www.math.harvard.edu/~lurie/252x.html)_, lecture 8, _The Adams Spectral Sequence_, 2010 ([pdf] (http://www.math.harvard.edu/~lurie/252xnotes/Lecture8.pdf))
  {#Lurie10}

* [[Jacob Lurie]], _[Chromatic homotopy theory lecture](http://www.math.harvard.edu/~lurie/252x.html)_, lecture 9, _The Adams Spectral Sequence for $MU$_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture9.pdf))

based on 

* [[Jacob Lurie]], _[[Higher Algebra]]_






### Hopf algebroid $Ext$-structure on $E^2$
 {#ReferencesHopfAlgebroidStructure}


* [[Andrew Baker]], _Brave new Hopf algebroids_ ([pdf](http://www.maths.gla.ac.uk/~ajb/dvi-ps/brave-ha.pdf))
 {#Baker}

* [[Andrew Baker]], [[Andrey Lazarev]], _On the Adams Spectral Sequence for R-modules_, Algebr. Geom. Topol. 1 (2001) 173-199 ([arXiv:http://arxiv.org/abs/math/0105079](http://arxiv.org/abs/math/0105079))
 {#BakerLazarev01}

* [[Andrew Baker]] and Alain Jeanneret, _Brave new Hopf algebroids and extensions of $MU$-algebras_, Homology Homotopy Appl. Volume 4, Number 1 (2002), 163-173. ([Euclid](http://projecteuclid.org/euclid.hha/1139840059))
 {#BakerJeanneret02}

* [[Mark Hovey]], _Homotopy theory of comodules over a Hopf algebroid_ ([arXiv:math/0301229](http://arxiv.org/abs/math/0301229)) 
 {#Hovey03}
 


[[!redirects Adams spectral sequences]]