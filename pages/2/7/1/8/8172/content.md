
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
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

The _Adams spectral sequence_ ([Adams 58](#Adams58)) is a type of [[spectral sequences]] used for computations  in [[stable homotopy theory]]. It computes the [[homotopy groups]] of a certain [[nilpotent completion]] of a [[spectrum]] (sometimes, but not necessarily, a [[Bousfield localization of spectra|Bousfield localization of spectra]]) from its [[homology]]/[[cohomology]], as [[modules]]/[[comodules]] over its [[cohomology operations]]. The Adams spectral sequence can be seen as a variant of the [[Serre spectral sequence]] obtained by replacing a single fibration by an "[[Adams resolution]]". 

The original Adams spectral sequence for [[ordinary cohomology]] is further refined by the _[[Adams-Novikov spectral sequence]]_ ([Novikov 67](#Novikov67)) by replacing [[ordinary cohomology]] modulo $p$ by [[complex cobordism cohomology theory]] or [[Brown-Peterson theory]] or the like. Generally, for $E$ a suitable [[E-infinity algebra]] there is a corresponding $E$-Adams(-Novikov) spectral sequence whose second page is given by $E$-[[generalized cohomology]] and which arises as the [[spectral sequence of a simplicial stable homotopy type]] of the [[cosimplicial object|cosimplicial]] object which is the [[Cech nerve]]/[[Sweedler coring]]/[[Amitsur complex]] of $E$. As such the Adams spectral sequence is an analog in [[stable homotopy theory]] of the [[Bousfield-Kan spectral sequence|Bousfield-Kan]] [[homotopy spectral sequence]].

Working with the Adams spectral sequence tends to be fairly involved, as is clear from the subtlety of the results it computes (notably [[stable homotopy groups of spheres]]) and as witnessed by the fact that one uses further [[spectral sequences]] just to compute the low pages of the Adams spectral sequence, e.g. the [[May spectral sequence]] and the  [[chromatic spectral sequence]]. 

A clear conceptual picture in [[higher algebra]]  of what happens in the Adams spectral sequence ([Lurie 10](#Lurie10)) has emerged via the re-formulation in ([Miller 81](#Miller81), [Hopkins 99](#Hopkins99)). Survey of this perspective includes ([Wilson 13](#Wilson13)). 

Here one observes that for $E$ a [[ring spectrum]], hence an [[E-∞ ring]], the [[totalization]] of its [[Amitsur complex]] [[cosimplicial object|cosimplicial]] spectrum is really the algebraic dual incarnation of the [[1-image]] factorization of the the terminal morphism

$$
  \array{
    Spec(E) &\longrightarrow& Spec(Tot(E^{\wedge^\bullet}))
    \\
    \downarrow & \swarrow_{\mathrlap{p}}
    \\
    Spec(\mathbb{S})
  }
$$

in [[E-∞ geometry]]/[[spectral geometry]].

Moreover, a [[spectrum]] $X$ is equivalently a [[quasicoherent sheaf]] on $Spec(S)$ and $E^{\wedge^\bullet} \wedge X$ is accordingly the [[Sweedler coring]] that expresses the [[descent]] property of $X$ pullled back along the cover $p$, dually the $E$-[[localization]] of $X$. The Adams spectral sequence may then be seen to be the computation of the [[homotopy groups]] of the $E$-localization of $X$ in terms of its restriction to that cover. 

In general, notably for $E = H \mathbb{F}_p$, the [[1-image]] of $Spec(E) \to Spec(\mathbb{S})$ is smaller than $Spec(\mathbb{S})$ and therefore this process computes not all of $X$, but just the restriction to that one image (for instance just the $p$-local component). Examples of ring spectra which are "complete" with respect to the sphere spectrum in that the above 1-image coincides with $Spec(S)$ notably includes the [[complex cobordism cohomology]] spectrum $E = $[[MU]] ([Hopkins 99, p. 70](#Hopkins99)). 

That explains the relevance of the [[Adams-Novikov spectral sequence]] (noticing that the wedge summands of $MU_{(p)}$ are the [[Brown-Peterson spectrum|BP-spectra]]) and the close interplay between the ANSS and [[chromatic homotopy theory]].  



### Via iterated Hurewicz theorem and Serre spectral sequence
 {#MotivationFromHurewiczTheoremAndSerreSpectralSequence}

The Adams spectral sequence may be motivated from the strategy to 
compute [[homotopy groups]] from [[cohomology groups]] by subsequently applying the [[Hurewicz theorem]] to compute the lowest-degree non-trivial homotopy group from the corresponding [[cohomology group]], then co-killing that by forming its [[homotopy fiber]], finally applying the [[Serre spectral sequence]] to  identify the next lowest non-trivial cohomology group of that fiber, and then iterating this process. The Adams spectral sequence arises when in this kind of strategy instead of co-killing only the lowest lying [[cohomology group]], one at a time, one co-kills _all_ nontrivial cohomology groups, then forms the corresponding [[homotopy fiber]] and so on.

This was apparently historically the way that [[John Adams]] indeed proceeded from [[Jean-Pierre Serre]]'s approach and this is still a good motivation for the whoe construction, a nice exposition is in  ([Wilson 13, 1.1](#Wilson13)).

We now say this again in more detail.

Given $n \in \mathbb{N}$, consider the probem of computing the [[homotopy groups]] $\pi_k(S^n) \;mod \;2$ of the $n$-[[sphere]] $S^n$. For $k \leq n$ this is clear: first for $k \lt n$ they all vanish, and second for $k = n$ we have, by the very nature of [[Eilenberg-MacLane spaces]] $K(\mathbb{Z}_2, n)$, that the [[ordinary cohomology]] is

$$
  H^n(S^n, \mathbb{Z}_2) \simeq [S^n, K(\mathbb{Z}_2,n)] \simeq \pi_n(K(\mathbb{Z}_2,n)) \simeq \mathbb{Z}_2
$$

so that by the [[Hurewicz theorem]] it follows that also

$$
  \pi_n(S^n) \;mod\;2 \;\simeq \mathbb{Z}_2
  \,.
$$

The [[Hurewicz theorem]] does not say anything beyond the first non-vanishing cohomology group, but so to apply it again we can move up one step in the [[Whitehead tower]] of $S^n$ and hence consider the [[homotopy fiber]]

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

If $X$ is a [[spectrum]] of [[finite type]] then there is a [[finite]] $I$ of non-trivial cohomology classes like this, and a choice of [[cocycles]] $c_i$ for each of them gives a single map

$$
  f_0 
    \coloneqq 
   (c_i)_I \;\colon\; 
   X \longrightarrow K_0 \coloneqq \bigvee_{i \in I} \Sigma^{n_i}H \mathbb{F}_2
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


A trivial way for this to be the case is that the original $\sigma_s$ is itself in the image under $\partial$ of some element, in which case $\kappa_s = 0$ already all by itself. These elements are called _eventual boundaries_. Therefore if the Adams resolution is indeed a resolution, then the quotient group

$$
  \frac{permanent\;cycles}{eventual\;boundaries}
$$

gives elements in $\pi_\bullet(S)$, and this quotient is what the Adams spectral sequence computes.



## Details

1. [Classical discussion](#ClassicalDiscussion)

1. [Via injective resolutions](#ViaInjectiveResolutions)

1. [As derived descent in higher algebra](#DefinitionInHigherAlgebra)

### Classical discussion
 {#ClassicalDiscussion}

> under construction

Given a [[connective spectrum]] $X$ such that $H^\bullet(X)$
has finite type, then for each [[prime number]] $p$ there exists a [[spectral sequence]] which converges to the [[homotopy groups]] of $X$ modulo $p$ -- $\pi_\ast(X) \otimes \mathbb{Z}_p$ -- and whose $E^2$-page is

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



### Via injective resolutions
 {#ViaInjectiveResolutions}


A streamlined discussion of $E$-[[Adams resolutions]] in close analogy to [[injective resolutions]] in [[homological algebra]] was given in ([Miller 81](#Miller81)), advertized in ([Hopkins 99](#Hopkins99)) and worked out in more detail in ([Aramian](#Aramian)).

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

#### Convergence and $E$-completion

... [[converges conditionally]] to the [[E-nilpotent completion]]

([Ravenel 84](#Ravenel84))...

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


### As derived descent in higher algebra
 {#DefinitionInHigherAlgebra}

We discuss the general definition of $E$-[[Adams-Novikov spectral sequences]] for suitable [[E-∞ rings]] $E$ expressed in [[higher algebra]], as in ([Lurie, Higher Algebra](#Lurie)). We follow [Lurie 10](#Lurie10), a nice exposition is in ([Wilson 13](#Wilson13)).

First we recall

* [Spectral sequences computing homotopy groups of filtered objects](#SpectralSequencesForHomotopyGroupsOfFilteredObjects)

for the general case of filtered objects in suitable [[stable (∞,1)-categories]]. Then we consider the specialization of that to the


* [Homotopy groups of cosimplicial totalizations filtered by coskeleta](#HomotopyGroupsOfOfTotalizationsFilteredByCoskeleta).

Finally we consider specifically the examples of such given by

* [Canonical cosimplicial resolutions of E-∞ algebras](#CanonicalCosimplicialResolutionOfEInfinityAlgebras).

In conclusion this yields for each suitable [[E-∞ algebra]] $E$ over $S$  and $S$-[[∞-module]] $X$ a [[spectral sequence]] converging to the [[homotopy groups]] of the $E$-[[Bousfield localization of spectra|localization]] of $X$, and this is

* [The E-Adams-Novikov spectral sequence](#TheEAdamsSpectralSequence).


The quick idea is this: Given an $S$ -module $X$, regard it as a quasicoherent sheaf on $Spec(S)$. Choose a map $Spec(E) \to Spec(S)$. This is a cover of its [[1-image]]
 $Spec(E) \to Spec(S)^\wedge_{Spec(E)}$, which is the derived [[formal completion]] of $Spec(S)$ at the image of $Spec(E)$. Restrict attention then to the restriction of $X$ to that formal completion $X^\wedge_{Spec(E)}$. (So if $Spec(E) \to Spec(S)$ was already an atlas, hence was already complete, we stick with the original $X$). Then pull back $S$ to the [[Cech nerve]] of the cover $Spec(E) \to Spec(S)^wedge_{Spec(E)}$. The realization of this Cech nerve reproduces the completed image, and hence the canonical filtration on the Cech nerve gives a filtration spectral sequence for $X^\wedge_{Spec(E)}$.


#### Spectral sequences computing homotopy groups of filtered objects
 {#SpectralSequencesForHomotopyGroupsOfFilteredObjects}

Let thoughout $\mathcal{C}$ be a [[stable (∞,1)-category]] equipped with a [[t-structure]] such that its [[heart of a stable (∞,1)-category|heart]] is an [[abelian category]]. 

+-- {: .num_example}
###### Example

For instance 

* $\mathcal{C} = Spec$  the [[stable (∞,1)-category of spectra]]. 

=--

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

This appears as ([[Higher Algebra|Higher Algebra, def. 1.2.2.9]]).


+-- {: .num_defn #ExactCoupleForFilteredObject}
###### Definition

For a generalized filtered object $X_\bullet$, def. \ref{GeneralizedFilteredObject}, write 

$$
  F_n \coloneqq fib(X_n \to X_{n+1})
$$

for the [[homotopy fiber]] of the $n$th structure map, for all $n \in \mathbb{Z}$, and define an [[exact couple]]

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

where the maps are given by the [[long exact sequences of homotopy groups]]

$$
  \cdots
  \to
  \pi_\bullet(X_{n+1})
  \to 
  \pi_\bullet(F_n) \to  \pi_\bullet(X_n) \to \pi_\bullet(X_{n+1}) \to \pi_{\bullet+1}(F_n) \to \cdots
$$

=--

We now have the [[spectral sequence of a filtered stable homotopy type]].

+-- {: .num_prop #FiltrationSpectralSequence}
###### Proposition

Let $\mathcal{C}$ be a [[stable (∞,1)-category]] equipped with a [[t-structure]] such that its [[heart of a stable (∞,1)-category|heart]] is an [[abelian category]]. 

If $\mathcal{C}$ has [[sequential limits]] and if  $X_n \simeq 0$ for all $n \gt n_0$ then the [[spectral sequence]] induced by the [[exact couple]]
of def. \ref{ExactCoupleForFilteredObject} converges to the [[homotopy groups]] of the [[homotopy limit]] $\underset{\leftarrow}{\lim}_n X_n$ of the generalized filtered object:

$$
  E^{p,q}_1
  =
  \pi_{p+q} F_{p-1}
  \Rightarrow
  \pi_{p+q} (\underset{\leftarrow}{\lim} X_\bullet) 
$$

=--

This is due to ([[Higher Algebra|Higher Algebra, prop. 1.2.2.14]]). Review is in ([Wilson 13, theorem 1.2.1](#Wilson13)).

For the traditional statement in the [[category of chain complexes]] see at _[[spectral sequence of a filtered complex]]_.


#### Homotopy groups of cosimplicial totalizations filtered by coskeleta
 {#HomotopyGroupsOfOfTotalizationsFilteredByCoskeleta}

+-- {: .num_defn #FiltrationOfTotalizationByTotalizationOfCoskeleta}
###### Definition

Given an [[cosimplicial object]] 

$$
  Y \;\colon\; \Delta  \longrightarrow \mathcal{C}
$$

its [[totalization]] $Tot Y \simeq \underset{\leftarrow}{\lim}_n Y_n$
is filtered, def. \ref{GeneralizedFilteredObject}, by the 
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

+-- {: .num_prop #E2PageByMooreComplex}
###### Proposition

The filtration spectral sequence, prop. \ref{FiltrationSpectralSequence},
applied to the filtration of a [[totalization]] by [[coskeleton|coskeleta]] as in def. \ref{FiltrationOfTotalizationByTotalizationOfCoskeleta}, has as $E_2$-term the [[cohomology groups]] of the [[Moore complex]] associated with the cosimplicial object

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



#### Canonical cosimplicial resolution of $E_\infty$-algebras
 {#CanonicalCosimplicialResolutionOfEInfinityAlgebras}

We discuss now the special case of coskeletally filtered 
totalizations coming from the canonical cosimplicial objects
induced from [[E-∞ algebras]] ("[[Amitsur complexes]]", "[[Sweedler corings]]").

In this form this appears as ([Lurie 10, theorem 2](#Lurie10)). A review is in ([Wilson 13, 1.3](#Wilson13)). For the analog of this in the traditional formulation see ([Ravenel, ch. 3, prop. 3.1.2](#Ravenel)).



+-- {: .num_defn}
###### Definition

Let $S$ be an [[E-∞ ring]] and let $E$ be an [[E-∞ algebra]] over $S$, hence an [[E-∞ ring]] equipped with a [[homomorphism]]

$$
  S \longrightarrow E
  \,.
$$

The _canonical [[cosimplicial object]]_ 
associated to this (the "$\infty$-[[Sweedler coring]]" or "[[Amitsur complex]]") is that given by the iterated [[smash product]]/[[tensor product]] over $S$:

$$
  E^{\wedge^{\bullet+1}_S} \;\colon\; \Delta \to \mathcal{C}
  \,.
$$

More generally, for $X$ an $S$-[[∞-module]], the canonical [[cosimplicial object]] is

$$
  E^{\wedge^{\bullet+1}_S}\wedge_S X \;\colon\; \Delta \to \mathcal{C}
  \,.
$$

=--

+-- {: .num_prop #FlatnessCondition}
###### Proposition

If $E$ is such that the self-[[generalized homology]] 
$E_\bullet(E) \coloneqq \pi_\bullet(E \wedge_S E)$ (the dual $E$-[[Steenrod operations]]) is such that as a [[module]] over $E_\bullet \coloneqq \pi_\bullet(E)$ it is a [[flat module]], then there is a [[natural equivalence]]

$$
  \pi_\bullet
  \left(
    E^{\wedge^{n+1}_S}
    \wedge_S 
    X
  \right)
  \simeq
  E_\bullet(E^{\wedge^n_S})
  \otimes_{E_\bullet}
  E_\bullet(X)
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

This makes $(E_\bullet, E_\bullet(E))$ be the [[Hopf algebroid]]
formed by the  $E$-[[Steenrod algebra]]. See there for more on this.

=--

+-- {: .num_example}
###### Example

The condition in prop. \ref{FlatnessCondition} is
satisfied for 

* $E = H \mathbb{F}_p$ an [[Eilenberg-MacLane spectrum]] with $mod\;p$ [[coefficients]];

* $E = B P$ the [[Brown-Peterson spectrum]];

* $E = MU$ the [[complex cobordism cohomology theory|complex cobordism spectrum]].

It is NOT satisfied for

* $E = H \mathbb{Z}$ the [[Eilenberg-MacLane spectrum]] for [[integers|integer]] [[coefficients]];

* $E = M S U$.

=--

+-- {: .num_remark #ExtGroupsByMooreComplex}
###### Remark

Under good conditions (...), $\pi_\bullet$ of the canonical [[cosimplicial object]] provides a [[resolution]] of [[comodule]] [[tensor product]] and hence computes the [[Ext]]-groups over the [[Hopf algebroid]]:

$$
  H^p(\pi_q(Tot(cosk_\bullet(E^{\wedge^{\bullet+1}_S } \wedge_S X))))
  \simeq
  Ext^p_{E_\bullet(E)}(\Sigma^q E_\bullet, E_\bullet(X))
  \,.
$$

(...)

=--

Here the homotopy groups are expressed by [[Ext]]-groups using a [[universal coefficient theorem]] 
[for generalized cohomology](universal+coefficient+theorem#ForGeneralizedCohomology)  ([Adams 74, III.13](#Adams74)).


(e.g. [Wilson 13, theorem 1.3.5](#Wilson13), based on [Bousfield 79](Bousfield+localization+of+spectra#Bousfield79))



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

#### The $E$-Adams-Novikov spectral sequence
 {#TheEAdamsSpectralSequence}

Summing this up yields the general $E$-Adams(-Novikov) spectral sequence

+-- {: .num_cor}
###### Corollary

Let $E$ a [[connective spectrum|connective]] [[E-∞ ring]] 
that satisfies the conditions of prop. \ref{SufficientConditionsForTotalizationToBeELocalization}. 
Then by prop. \ref{FiltrationSpectralSequence} and prop. \ref{SufficientConditionsForTotalizationToBeELocalization} there is a strongly convergent multiplicative
[[spectral sequence]]

$$
  E^{p,q}_\bullet \Rightarrow \pi_{q-p} L_{c \pi_0 E} X
$$

converging to the [[homotopy groups]] of the  $ c \pi_0(E)$-[[Bousfield localization of spectra|localization]] of $X$. If moreover the dual $E$-[[Steenrod algebra]] $E_\bullet(E)$ is [[flat module|flat]] as a [[module]] over $E_\bullet$, then, by prop. \ref{E2PageByMooreComplex} and remark \ref{ExtGroupsByMooreComplex}, the $E_2$-term of this spectral sequence is given by the [[Ext]]-groups over the $E$-[[Steenrod algebra|Steenrod]] [[Hopf algebroid]].

$$
  E^{p,q}_\bullet
  =
  Ext^p_{E_\bullet(E)}(\Sigma^q E_\bullet, E_\bullet X)
  \,.
$$


=--


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

* [[May spectral sequence]], [[chromatic spectral sequence]]

* [[Steenrod algebra]]

* [[descent spectral sequence]]

[[!include Lurie spectral sequences -- table]]


## References

### General

The original articles are

* {#Adams58} [[John Adams]], _On the structure and applications of the Steenrod algebra_, Comm. Math. Helv. 32 (1958), 180&#8211;214.
 

* {#Novikov67} [[Sergei Novikov]], _The methods of algebraic topology from the viewpoint of cobordism theories_, Izv. Akad. Nauk. SSSR. Ser. Mat. 31 (1967), 855&#8211;951 (Russian).
 
Convergence was notably discussed in

* {#Bousfield79} [[Aldridge Bousfield]], _The localization of spectra with respect to homology_, Topology 18 (1979), no. 4, 257--281. ([pdf](http://www.uio.no/studier/emner/matnat/math/MAT9580/v12/undervisningsmateriale/bousfield-topology-1979.pdf))

* {#Ravenel84} [[Douglas Ravenel]], _Localization with respect to certain periodic homology theories_, American Journal of Mathematics, Vol. 106, No. 2, (Apr., 1984), pp. 351-414 ([pdf](https://www.math.rochester.edu/people/faculty/doug/mypapers/loc.pdf))

The [[spectrum]]-level discussion of the ASS goes back to around

* R. M. F. Moss, _On the composition pairing of Adams spectral sequences_, Proceedings of the London Mathematical Society 3.1 (1968): 179-192.

A streamlined presentation of this close in spirit to constructions in [[homological algebra]] was given in

* {#Miller81} [[Haynes Miller]], _On relations between Adams spectral sequences, with an application to the stable homotopy of a Moore space_, J. Pure Appl. Algebra 20 (1981) ([pdf](http://math.mit.edu/~hrm/papers/miller-relations-between-adams-spectral-sequences.pdf))

and is reproduced in 

* {#Hopkins99} [[Mike Hopkins]], section 5 of _Complex oriented cohomology theories and the language of stacks_, course notes 1999 ([pdf](https://www.math.rochester.edu/people/faculty/doug/otherpapers/coctalos.pdf))

* {#Aramian} [[Nersés Aramian]], _The Adams spectral sequence_ ([[AramianANSS.pdf:file]])

Traditional reviews include

* {#Adams74} [[John Adams]], part III of _Stable homotopy and generalised homology, University of Chicago Press, Chicago, Ill., 1974, Chicago Lectures in Mathematics.

* {#Ravenel06} [[Doug Ravenel]], _A Novice's guide to the Adams-Novikov spectral sequence_, in Geometric Applications of Homotopy Theory II Volume 658 of the series Lecture Notes in Mathematics pp 404-475

* {#Ravenel} [[Doug Ravenel]], _[[Complex cobordism and stable homotopy groups of spheres]]_, 

* {#Goerss2007} [[Paul Goerss]], _The Adams-Novikov spectral sequence and the Homotopy Groups of Spheres_, lecture notes 2007 ([pdf](http://www.math.northwestern.edu/~pgoerss/papers/stras1.pdf))

* [[Alan Hatcher]], _[Spectral sequences in algebraic topology](http://www.math.cornell.edu/~hatcher/SSAT/SSATpage.html)_ _II: The Adams spectral sequence_ ([pdf](http://www.math.cornell.edu/~hatcher/SSAT/SSch2.pdf))

* {#Bruner} R. Bruner, _An Adams spectral sequence primer_ ([pdf](http://www.math.wayne.edu/~rrb/papers/adams.pdf))

* {#Rognes12} [[John Rognes]], _The Adams spectral sequence_ (following [Bruner](#Bruner)), 2012 ([pdf](http://folk.uio.no/rognes/papers/notes.050612.pdf))

Other notes that are available include

* [[Alexander Kupers]], _An introduction to the Adams spectral sequence_ (following [Rognes 12](#Rognes12)) ([pdf](http://math.stanford.edu/~kupers/adamsss.pdf))

* Michael Adamaszek, _An elementary guide to the Adams-Novikov $Ext$_ ([pdf](http://www.math.uni-bremen.de/~aszek/bp.pdf))

* [pdf](http://www.math.harvard.edu/~sia/notes/classical_topology_adams.pdf)


The modern point of view of [[higher algebra]] is in 

* {#Lurie10} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_ (2010)

  * lecture 8, _The Adams Spectral Sequence_ ([pdf] (http://www.math.harvard.edu/~lurie/252xnotes/Lecture8.pdf))
  
  * lecture 9, _The Adams Spectral Sequence for $MU$_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture9.pdf))

  * lecture 10, _The proof of Quillen's theorem_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture10.pdf))

  * lecture 30, _Localizations and the Adams-Novikov Spectral Sequence_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture30.pdf))

based on 

* {#Lurie} [[Jacob Lurie]], _[[Higher Algebra]]_

and nicely surveyed in

* [[Akhil Mathew]], _[The Adams spectral sequence as derived descent, and chromotopy](https://amathew.wordpress.com/2012/09/21/3844/)_, 2012

* {#Wilson13} [[Dylan Wilson]] _Spectral Sequences from Sequences of Spectra: Towards the Spectrum of the Category of Spectra_ lecture at [2013 Pre-Talbot Seminar](http://math.harvard.edu/~hirolee/pretalbot2013/index.php) ([[DylanWilsonOnANSS.pdf:file]])

### For more general coefficients

For [[tmf]]

* [[Mark Behrens]], _The Adams spectral sequence for $tmf$_ ([[BehrensANSSfortmf.pdf:file]])
 
### Hopf algebroid $Ext$-structure on $E^2$
 {#ReferencesHopfAlgebroidStructure}

* appendix A.1 of [Ravenel](#Ravenel)

* {#Baker} [[Andrew Baker]], _Brave new Hopf algebroids_ ([pdf](http://www.maths.gla.ac.uk/~ajb/dvi-ps/brave-ha.pdf))
 

* {#BakerLazarev01} [[Andrew Baker]], [[Andrey Lazarev]], _On the Adams Spectral Sequence for R-modules_, Algebr. Geom. Topol. 1 (2001) 173-199 ([arXiv:http://arxiv.org/abs/math/0105079](http://arxiv.org/abs/math/0105079))
 

* {#BakerJeanneret02} [[Andrew Baker]] and Alain Jeanneret, _Brave new Hopf algebroids and extensions of $MU$-algebras_, Homology Homotopy Appl. Volume 4, Number 1 (2002), 163-173. ([Euclid](http://projecteuclid.org/euclid.hha/1139840059))
 

* {#Hovey03} [[Mark Hovey]], _Homotopy theory of comodules over a Hopf algebroid_ ([arXiv:math/0301229](http://arxiv.org/abs/math/0301229)) 
 
 


[[!redirects Adams spectral sequences]]