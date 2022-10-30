
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

The _Adams spectral sequence_ is that induced by the [[exact couple]] obtained by applying $\pi_\bullet$ to this [[Adams resolution]].

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

1. [Via injective resolutions](#ViaInjectiveResolutions)

1. [As derived descent in higher algebra](#DefinitionInHigherAlgebra)


### The $E$-Adams spectral sequence
 {#ViaInjectiveResolutions}

We here discuss Adams spectral sequences for computation of $E$-[[Bousfield localization of spectra|localization]] of [[mapping spectra]] $[Y,X]$ for by $E$ a general [[commutative ring spectrum]] which is flat in a certain sense (def. \ref{FlatE} below).

The classical Adams spectral sequence is the special case with $Y = X = \mathbb{S}$ and $E = $ [[HA|A]]$\mathbb{F}_p$, discussed [below](#ClassicalCase).

The _[[Adams-Novikov spectral sequence]]_ is the special case with $Y = X = \mathbb{S}$ and $E = $ [[MU]], discussed [below](#TheAdamsNovikovSpectralSequence).


#### $E$-Adams resolutions

A streamlined discussion of $E$-[[Adams resolutions]] in close analogy to [[injective resolutions]] in [[homological algebra]] was given in ([Miller 81](#Miller81)), advertized in ([Hopkins 99](#Hopkins99)) and worked out in more detail in ([Aramian](#Aramian)).


Notice that the standard concept of [[exact sequences]] and [[injective objects]] makes sense in [[abelian categories]], but not in the [[stable homotopy theory]] of [[spectra]]; for instance the true homotopy theoretic analog of exact sequences are [[homotopy fiber sequences]]. But for computational purposes we may consider a variant (due to [Miller 81](#Miller81)), where a sequence of spectra $X_\bullet$ is regarded as exact if the [[homotopical functor]] to abelian groups that it represents sends objects to standard exact sequences.  




+-- {: .num_defn #HomotopicalFunctorCoRepresentedByASpectrum}
###### Definition

For $X$ a [[spectrum]], we say that the _[[homotopical functor]]_
that it [[representable functor|co-represents]] is the functor of [[stable homotopy groups]] of the [[mapping spectrum]]-construction out of $X$, regarded as a functor on the [[stable homotopy category]]:

$$
  \pi_\bullet[X, -] \colon Ho(Spectra) \longrightarrow Ab^{\mathbb{Z}}
  \,.
$$

(Regarded as an [[(∞,1)-functor]] on the [[stable (∞,1)-category of spectra]] this is also called the _[[homological functor]]_ co-represented by $X$.)

=--

+-- {: .num_example}
###### Example

For $X = \mathbb{S}$ the [[sphere spectrum]] then the homotopical functor that it co-represents according to def. \ref{HomotopicalFunctorCoRepresentedByASpectrum}

$$
  \pi_\bullet[\mathbb{S},- ]\simeq \pi_\bullet(-)
$$

is the [[stable homotopy group]]-functor.

=--


Throughout,$E$ is a [[ring spectrum]].

+-- {: .num_defn #ExactSequences}
###### Definition

Say that 

1. a sequence of [[spectra]]

   $$
     A_1 \longrightarrow A_2 \longrightarrow \cdots \longrightarrow A_n
   $$

   is 

   1. a (long) _exact sequence_ if the induced sequence of [[homotopy functors]] according to def. \ref{HomotopicalFunctorCoRepresentedByASpectrum}, is a [[long exact sequence]] in $[HoSpectra,Ab^{\mathbb{Z}}]$;

   2. (for $n = 2$) a _short exact sequence_ if

      $$
        0 \longrightarrow A_1 \longrightarrow A_2 \longrightarrow A_3 \longrightarrow 0
      $$

      is (long) exact in the above sense;


1. a morphism $A \longrightarrow B$  is 

   1. a _monomorphism_ if $0 \longrightarrow A \longrightarrow B$ is an exact sequence in the above sense;

   1. an _epimorphism_ if $A \longrightarrow B \longrightarrow 0$ is an exact sequence in the above sense.

For $E$ a [[ring spectrum]], then a sequence of spectra is called (long/short) _$E$-exact_ and a morphism is epi/mono, respectively, if becomes long/short exact or epi/mono, respectively, after taking [[smash product of spectra|smash product]] with $E$.

=--

+-- {: .num_example #HomotopyCofiberSequencesAreExactSequencesOfSpectra}
###### Example

Every [[homotopy cofiber sequence]] of spectra is exact in the sense of def. \ref{ExactSequences}. 

=--

+-- {: .num_example #SuspensionPreservesExactSequencesOfSpectra}
###### Example

The [[suspension]] functor $\Sigma \colon Ho(Spectra) \to Ho(Spectra)$ preserves exact sequences in the sense of def. \ref{ExactSequences}.

=--

+-- {: .proof}
###### Proof

By the [[adjunction]]-[[isomorphism]] $[\Sigma A_\bullet, -]\simeq [A_\bullet, \Omega(-)]$ and so the statement follows from the assumption that $A_\bullet$ is long exact.

=--

+-- {: .num_example #HomotopyRetractionsAreMonomorphismsOfSpectra}
###### Example

If a morphism, $s \colon A \to B$ has a [[retraction]] $r \colon B \to A$ in [[Ho(Spectra)]] then it is a monomorphism in the sense of def. \ref{ExactSequences}.

=--

+-- {: .proof}
###### Proof

We need to check that for every $X$ the morphism $i^\ast \colon [B, X]\to [A,X]$ is surjective. By retraction, given $f \colon A \to X$, then $r \circ f \colon B \stackrel{r}{\to} A \stackrel{f}{\to} X$ is a preimage.

=--

+-- {: .num_example #TensoringWithUnitOfRingSpectrumIsMonomorphismOfSpectra}
###### Example

For any spectrum $X$ the morphism

$$
  X \simeq \mathbb{S} \wedge X \stackrel{e \wedge id}{\longrightarrow}
  E \wedge X
$$

is an $E$-monomorphism in the sense of def. \ref{ExactSequences}.

=--

+-- {: .proof}
###### Proof

We need to check that $E \wedge X \stackrel{id \wedge e \wedge id}{\longrightarrow} E \wedge E \wedge X$ is a monomorphism in the sense of def. \ref{ExactSequences}. Observe that this morphism has a [[retraction]] given by $\mu \wedge id$. Therefore it is a monomorphism by 
example  \ref{HomotopyRetractionsAreMonomorphismsOfSpectra}.

=--

+-- {: .num_remark}
###### Remark/Warning

Consecutive morphisms in an $E$-exact sequence according to def. \ref{ExactSequences} in general need not compose up to homotopy, to the [[zero morphism]]. But this does become true for sequences of $E$-injective objects, defined below in def. \ref{EInjective}.

=--

+-- {: .num_lemma #CharacterizationOfEpiMonomorphismsOfSpectra}
###### Lemma

1. If $f \colon B\longrightarrow A$ is a monomorphism in the sense of def. \ref{ExactSequences}, then there exists a morphism $g \colon C \longrightarrow A$ such that the [[wedge sum]] morphism is a [[weak homotopy equivalence]]

   $$
     f \vee g \;\colon\; B \wedge C \stackrel{\simeq}{\longrightarrow} A
     \,.
   $$

   In particular, every morphism in [[Ho(Spectra)]] has an [[extension]] along a monomorphism in this sense. 

1. If $f \colon A \longrightarrow B$ is an epimorpimsm in the sense of def. \ref{ExactSequences}, then there exists a homotopy [[section]] $s \colon B\to A$, i.e. $f\circ s\simeq Id$, together with a morphism $g \colon C \to A$ such that the [[wedge sum]] morphism is a [[weak homotopy equivalence]]

   $$
     s \vee f \colon B\vee C \stackrel{\simeq}{\longrightarrow} A
     \,.
   $$

=--

+-- {: .proof}
###### Proof

Given a monomorphism $f \colon A \longrightarrow B$, consider the correspondiing [[homotopy cofiber sequence]]

$$
  A\stackrel{f}{\longrightarrow} B \stackrel{r}{\longrightarrow} C  \stackrel{\delta}{\longrightarrow} \Sigma A \stackrel{-\Sigma f}{\longrightarrow} \Sigma B
  \,.
$$

We first observe that the [[connecting homomorphism]] is equivalent to the [[zero morphism]] $\delta \simeq 0$. This follows because by example \ref{HomotopyCofiberSequencesAreExactSequencesOfSpectra} the sequence

$$
  [C,X] 
    \stackrel{\delta^\ast_\bullet}{\longleftarrow} 
  [\Sigma A, X]
    \stackrel{(-\Sigma f)^\ast_\bullet}{\longleftarrow}
  [\Sigma B, X]
$$

is an [[exact sequence]] (of homotopy groups) for every $X$, while by example \ref{SuspensionPreservesExactSequencesOfSpectra} the morphism on the right is epi, so that $\delta^\ast_\bullet = 0$.

Now since $B \stackrel{r}{\longrightarrow} C \stackrel{\delta \simeq 0}{\longrightarrow}$ is also a [[homotopy fiber sequence]], the [[pasting law]] identifies $B \simeq C \times A \simeq C \vee A$:

$$
  \array{
    B \simeq C \times A &\longrightarrow& A &\longrightarrow& 0 
    \\
    \downarrow && \downarrow && \downarrow
    \\
    C &\longrightarrow& 0 &\longrightarrow& \Sigma A
  }
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

+-- {: .num_lemma #EInjectiveSpectraAreRetractsOfFreeEModules}
###### Lemma

A spectrum is $E$-injective in the sense of def. \ref{EInjective}, precisely if it is a [[retract]] in [[HoSpectra]] of a free $E$-modules, hence of $E \wedge X$ for some spectrum $X$.

=--

+-- {: .proof}
###### Proof

In one direction, assume that $S$ is $E$-injective and consider the diagram

$$
  \array{
    S &\stackrel{id}{\longrightarrow}& S
    \\
    {}^{\mathllap{e \wedge id}}\downarrow
    \\
    E \wedge S
  }
  \,.
$$

By example \ref{TensoringWithUnitOfRingSpectrumIsMonomorphismOfSpectra} here the vertical morphism is an $E$-monomorphism, and so by assumption there is a lift

$$
  \array{
    S &\stackrel{id}{\longrightarrow}& S
    \\
    \downarrow & \nearrow
    \\
    E \wedge S
  }
$$

which exhibits $S$ as a retract of $E \wedge S$.

In the other direction, given a retraction $S \stackrel{\overset{r}{\longleftarrow}}{\underset{s}{\longrightarrow}} E \wedge X$ we show that there exist extensions in

$$
  \array{
    A &\stackrel{g}{\longrightarrow} & S
    \\
    {}^{\mathllap{f}}\downarrow 
    \\
    B
  }
$$

whenever the vertical morphism is an $E$-monomorphism. To see this, complete the extension problem to the following [[commuting diagram]]

$$
  \array{
    A &&& \stackrel{e \wedge id}{\longrightarrow} &&& E \wedge A
    \\
    {}^{\mathllap{f}}\downarrow &\searrow^{\mathrlap{g}} & &&  & {}^{\mathllap{{\mu \wedge id} \atop {\circ id \wedge s g }}}\swarrow & \downarrow^{\mathrlap{id \wedge f}}
    \\
    && S &\stackrel{r}{\longleftarrow}& E \wedge X
    \\
    \downarrow && &&  && \downarrow
    \\
    B &&& \stackrel{e \wedge id}{\longrightarrow} &&& E \wedge B
  }
  \,.
$$

Now, since $f$ is assumed to be an $E$-monomorphism, the morphism $Eid\wedge f$ on the right is a monomorphism in the sense of def. \ref{ExactSequences}, and so by lemma \ref{CharacterizationOfEpiMonomorphismsOfSpectra} there exists an extension $h$ in 

$$
  \array{
    A &&& \stackrel{e \wedge id}{\longrightarrow} &&& E \wedge A
    \\
    {}^{\mathllap{f}}\downarrow &\searrow^{\mathrlap{g}} & &&  & {}^{\mathllap{{\mu \wedge id} \atop {\circ id \wedge s g }}}\swarrow & \downarrow^{\mathrlap{id \wedge f}}
    \\
    && S &\stackrel{r}{\longleftarrow}& E \wedge X
    \\
    \downarrow && &&  &\nwarrow^{\mathrlap{h}}& \downarrow
    \\
    B &&& \stackrel{e \wedge id}{\longrightarrow} &&& E \wedge B
  }
  \,.
$$

By composition and commutativity, this gives the required extension of $g$ along $f$.


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

Any two consecutive maps in an $E$-Adams resolution, def. \ref{EAdamsResolution}, compose to the [[zero morphism]].

=--

The following lemma says that $E$-Adams resolutions may be [[extension|extended]] along morphisms.

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

Any [[ring spectrum]] $E$ gives rise to an [[augmentation|augmented]] [[cosimplicial object|cosimplicial]] [[spectrum]]  (its _[[bar construction]]_)

$$
  \mathbb{S} \longrightarrow E 
    \stackrel{\longrightarrow}{\longrightarrow} 
  E \wedge E 
    \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}
  E \wedge E \wedge E 
    \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}}
 \cdots
$$

whose

* coface maps are given by inserting the unit $\mathbb{S} \stackrel{e}{\to} E$

  $$
    d^i 
      \colon
    E^{\wedge^n}
      \simeq
    E^{\wedge^i} \wedge \mathbb{S} \wedge E^{\wedge^{n-i}}
      \stackrel{id \wedge e \wedge id}{\longrightarrow}
    E^{\wedge^{n+1}}
    \,;
  $$

* codegeneracy maps are given by the product operation $\mu \colon E \wedge E \to E$

  $$
    s^j
      \colon
    E^{\wedge^{n+1}}
      \simeq
    E^{\wedge^{i}} \wedge E \wedge E \wedge E^{\wedge n-1-i}
      \stackrel{id \wedge \mu \wedge id}{\longrightarrow}
    E^n
    \,.
  $$

The corresponding [[Amitsur complex]] is given by forming alternating sums of the coface maps

$$
  \mathbb{S}
    \stackrel{e}{\longrightarrow}
  E
    \stackrel{e\wedge id - id \wedge e}{\longrightarrow}
  E \wedge E
    \stackrel{e \wedge id - id\wedge e \wedge id + id \wedge e}{\longrightarrow}
  E \wedge E \wedge E
    \stackrel{}{\longrightarrow}
  \cdots
  \,.
$$

Given any [[spectrum]] $X$, then forming the [[smash product]] $(-)\wedge X$ with this sequence yields a sequence of the form

$$
  X
    \stackrel{}{\longrightarrow}
  E \wedge X
    \stackrel{}{\longrightarrow}
  E \wedge E \wedge X
    \stackrel{}{\longrightarrow}
  E \wedge E \wedge E \wedge X
    \stackrel{}{\longrightarrow}
  \cdots
  \,.
$$

This is called the **standard $E$-Adams resolution** of $X$.

=--

(e.g. [Hopkins 99, def. 5.4](#Hopkins99)).

+-- {: .num_prop #StandardAdamsResolutionIsIndeedAdamsResolution}
###### Proposition

The standard resolution of example \ref{StandardEResolution}
is indeed an $E$-Adams resolution of $X$ in the sense of def. \ref{EAdamsResolution}.

=--

+-- {: .proof}
###### Proof

As generally for [[bar resolutions]], one checks that the alternating sum of the codegeneracy maps constitute homotopy operators that give contracting homotopies when commuted with the alternating sum of the coface maps. This gives that the sequence is $E$-exact.
Moreover, the terms in the sequence are all $E$-injective by lemma \ref{EInjectiveSpectraAreRetractsOfFreeEModules}.

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

The _associated inverse sequence_ is

$$
  X = X_0 \stackrel{\gamma_0}{\longleftarrow} \Omega C_1 \stackrel{\gamma_1}{\longleftarrow} C_2 \longleftarrow \cdots
$$

where $C_{k+1} \coloneqq hocofib(i_k)$.

=--

+-- {: .num_remark}
###### Remark

In ([Ravenel 86](#Ravenel86)) it is is the associated inverse sequence that is called an $E$-Adams resolution.

=--

Finally, the following is the main statement of the above little theory of $E$-injective spectra.

+-- {: .num_prop #RelationBetweenEAdamsTowersAndEAdamsResolutions}
###### Proposition

Every $E$-Adams resolution of $X$, def. \ref{EAdamsResolution}, induces an $E$-Adams tower, def. \ref{EAdamsTower} of which it is the associated $E$-Adams resolution.

=--

+-- {: .proof}
###### Proof idea

Given an $E$-Adams resolution

$$
  X \to I_0 \to I_1 \to \cdots
$$

the associated $E$-Adams tower starts out as

$$
  \array{
    X_1 \coloneqq fib(I_0 \to I_1)
    \\
    \downarrow
    \\
    X_0 \coloneqq I_0
  }
  \,.
$$

From there one one proceeds
carefully by [[induction]]. This takes a bit of work, crucially using properties of $E$-injectives.

=--


+-- {: .num_defn #EAdamsSpectralSequence}
###### Definition

Given [[spectra]] $X$ and $Y$, and given an $E$-Adams resolution of $X$, def. \ref{EAdamsResolution}, or equivalently (by prop. \ref{RelationBetweenEAdamsTowersAndEAdamsResolutions}) an $E$-Adams tower over $X$, def. \ref{EAdamsTower}, 

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


then the corresponding **$E$-Adams spectral sequence** for the [[mapping spectrum]] $[Y,X]$ is the associated [[spectral sequence of a tower of fibrations]] of the image of that [[tower of fibrations]] under the [[mapping spectrum]] operation $[Y,-]$:

$$
  \array{
    && \vdots
    \\
    && \downarrow^{\mathrlap{[Y,p_2]}}
    \\
    && [Y,X_2] &\stackrel{[Y,\kappa_2]}{\longrightarrow}& [Y,\Omega^2 I_3]
    \\
    &\nearrow& \downarrow^{\mathrlap{[Y,p_1]}}
    \\
    && X_1 &\stackrel{[Y,\kappa_1]}{\longrightarrow}& [Y,\Omega I_2]
    \\
    &\nearrow& \downarrow^{\mathrlap{[Y,p_0]}}
    \\
    [Y,X] 
    &\underset{}{\longrightarrow}&
    [Y,X_0] = [Y,I_0]
    &\stackrel{[Y,\kappa_0]}{\longrightarrow}&
    [Y,I_1]
  }
  \,.
$$


More in detail, the associated [[exact couple]] of the tower is

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
  \oplus_{s,t} \pi_{t-s}([Y,X_s])
$$

$$
  \mathcal{E} \coloneqq 
  \oplus_{s,t} \mathcal{E}^{s+1,t}
  \coloneqq
  \oplus_{s,t} \pi_{t-s}([Y,\Omega^s I_{s+1}])
$$

and

$$
  p 
    \colon 
  \pi_{t-s}([Y,X_{s+1}])
    \stackrel{\pi_{t-s}([Y,p_s])}{\longrightarrow}
   X_{t-s}([Y,X_s])
$$

$$
  \kappa 
    \colon 
  \pi_{t-s}([Y,X_s])
    \stackrel{\pi_{t-s}([Y,\kappa_s])}{\longrightarrow} 
  \pi_{t-s}([Y,\Omega^s I_{s+1}])
$$

$$
  \partial 
    \colon 
  \pi_{t-s}([Y,\Omega^s I_{s+1}])
    \stackrel{\pi_{t-s}([Y,\partial_s])}{\longrightarrow}
  \pi_{t-s}([Y,\Sigma X_{s+1}])
  \,.
$$

The _$E$-Adams spectral sequence_ of the $E$-Adams tower is the [spectral sequence induced](exact+couple#SpectralSequencesFromExactCouples) by this [[exact couple]].

=--


+-- {: .num_prop #UniquenessOfEAdamsSpectralSequence}
###### Proposition

Given two $E$-Adams towers, def. \ref{EAdamsTower}, for some $X$, then the corresponding two $E$-Adams spectral sequences, def. \ref{EAdamsSpectralSequence}, are [[isomorphism|isomorphic]] from the $\mathcal{E}_2$-page on

=--

#### The first page and Hopf algebroids
 {#FirstPageAndHopfAlgebroid}

Due to prop. \ref{UniquenessOfEAdamsSpectralSequence}, 
for understanding the $\mathcal{E}_2$-page of any $E$-Adams spectral sequence, def. \ref{EAdamsSpectralSequence}, 
it is sufficient to understand the $\mathcal{E}_1$-page 
of the $E$-Adams spectral sequence that is induced by the
standard $E$-resolution of example \ref{StandardEResolution}.
By construction, that page is 

$$
  \mathcal{E}_1^{s,\bullet}
    \simeq
  \pi_\bullet(\;[Y,E^{\wedge (s+1)}\wedge X] \;)
$$

with the differentials being the image under $\pi_\bullet$ of the alternating sum of the morphisms that insert unit elements. 

We discuss now how, under favorable conditions, these homotopy groups of mapping spectra of the form $[Y,E^{\wedge (s+1)}\wedge X]$ may alternatively be computed as morphisms of $E$-[[generalized homology|homology]] equipped with suitable [[comodule]] structure over a [[Hopf algebroid]] structure on the dual $E$-[[Steenrod operations]] $E_\bullet(E)$. Then [below](#TheE2TermOfTheEAdamsSpectralSequence) we discuss that, as a result, the $d_1$-homology of the $\mathcal{E}_1$-page is seen to compute the [[Ext]]-groups from the $E$-homology of $Y$ to the $E$-homology of $X$, regarded as $E_\bullet(E)$-comodules. This re-formulation of the $\mathcal{E}_2$-page is the one that makes it be useful for computations.

The first condition needed for this to work is the following.

+-- {: .num_defn #FlatE}
###### Definition

Call the [[commutative ring spectrum]] $E$ _flat_ if one, equivalently both, of the morphisms

$$
  \eta_L \coloneqq \pi_\bullet(e \wedge id) 
  \;\colon\; 
  E_\bullet \longrightarrow E_\bullet(E)
$$

$$
  \eta_r 
  \;\coloneqq\; 
  \pi_\bullet(id \wedge e) \colon E_\bullet \longrightarrow E_\bullet(E)
$$

is a [[flat morphism]].

=--

+-- {: .num_example #ExamplesOfFlatRingSpectra}
###### Example

Examples of [[commutative ring spectra]] that are flat according to def. \ref{FlatE} include
$E = $

* [[sphere spectrum|S]], 

* [[HR]] for $R = \mathbb{F}_p$ a [[prime field]],

* [[MO]], [[MU]], [[MSp]], 

* [[KO]], [[KU]].


=--

+-- {: .num_example}
###### Example

Examples of ring spectra that are _not_ flat in the sense of def. \ref{FlatE} include [[HA|H]][[integers|Z]], and $M S U$.

=--


The key consequence of the assumption that $E$ is flat in the sense of def. \ref{FlatE} is the following.

+-- {: .num_prop #FlatnessOfEImpliesKeyConsequence}
###### Proposition

If $E$ is flat, def. \ref{FlatE}, then for all spectra $X$ there is a [[natural isomorphisms]]

$$
  E_\bullet(E) \otimes_{\pi_\bullet(E)} E_\bullet(X)
    \stackrel{}{\longrightarrow}
  \pi_\bullet(E \wedge E \wedge X)
$$

and hence for all $n \in \mathbb{N}$ there are isomorphisms

$$
  \pi_\bullet(E^{\wedge^{(n+2)}}\wedge X  )
    \simeq
  \underset{n+1\,factors}{
  \underbrace{E_\bullet(E)
    \otimes_{\pi_\bullet(E)}
    \cdots
    \otimes_{\pi_\bullet(E)}
  E_\bullet(E)
  }}
    \otimes_{\pi_\bullet(E)}
  E_\bullet(X)
  \,.
$$


=--

(e.g. [Adams 74, part III, lemma 12.5](#Adams74), [Schwede 12, prop. 6.20](#Schwede12))

+-- {: .proof}
###### Proof

The desired natural homomorphism

$$
  E_\bullet(E) \otimes_{\pi_\bullet(E)} E_\bullet(X)
  \longrightarrow
  \pi_\bullet(E \wedge E \wedge X)
$$

is given on $[\alpha] \in \pi_\bullet(E \wedge E)$ and $[\beta] \in \pi_\bullet(E \wedge X)$ by $([\alpha, \beta])\mapsto [(id \wedge \mu \wedge id) \circ (\alpha \wedge \beta)]$.

To see that this is an isomorphism, observe that by flatness of $E$, the assignment $X \mapsto E_\bullet(E) \otimes_{\pi_\bullet(E)} E_\bullet(-)$ is a [[generalized homology]] functor, hence [[Brown representability theorem|represented]] by some spectrum. The above morphism, natural in $X$, thus constitutes a homomorphism  of generalized homology theories. By the [Whitehead theorem for generalized homology](generalized+Eilenberg-Steenrod+cohomology#WhiteheadTheorem) for this to be an isomorphism it is sufficient to check that it induces isomorphisms on the point. This is manifestly the case.

Finally we get the claimed isomorphisms for all $n$ by [[induction]]:

$$
  \begin{aligned}
    \pi_\bullet(E^{\wedge^{n+2}} \wedge X)
    & \simeq
    \pi_\bullet(E \wedge E \wedge E^{\wedge^n} \wedge X))
    \\
    &\simeq 
     E_\bullet(E) 
         \otimes_{\pi_\bullet(E)} 
     E_\bullet( E^{\wedge^n} \wedge X )
     \\
     & = 
     E_\bullet(E) 
         \otimes_{\pi_\bullet(E)} 
     \pi_\bullet( E^{\wedge^{n+1}} \wedge X )       
  \end{aligned}
  \,.
$$

=--

spring

+-- {: .num_defn #CommutativeHopfAlgebroid}
###### Definition

A **[[commutative Hopf algebroid]]** is an [[internal groupoid]] in the [[opposite category]] [[CRing]]${}^{op}$ of [[commutative rings]], regarded with its [[cartesian monoidal category]] structure.

=--

(e.g. [Ravenel 86, def. A1.1.1](#Ravenel86))

+-- {: .num_remark #CommutativeHopfAlgebroidSpelledOut}
###### Remark

We unwind def. \ref{CommutativeHopfAlgebroid}.  For $R \in CRing$, write $Spec(R)$ for same same object, but regarded as an object in $CRing^{op}$. 

An [[internal category]] in $CRing^{op}$ is a [[diagram]] in $CRing^{op}$ of the form

$$
  \array{
    Spec(\Gamma) \underset{Spec(A)}{\times} Spec(\Gamma)
    \\
    \downarrow^{\mathrlap{\circ}}
    \\
    Spec(\Gamma)
    \\
    {}^{\mathllap{s}}\downarrow \; \uparrow^{\mathrlap{i}} \downarrow^{\mathrlap{t}}
    \\
    Spec(A)
  }
  \,,
$$

(where the [[fiber product]] at the top is over $s$ on the left and $t$ on the right) such that the pairing $\circ$ defines an [[associativity law|associative]] [[composition]] over $Spec(A)$, [[unitality|unital]] with respect to $i$. This is an [[internal groupoid]] if it is furthemore equipped with a morphism

$$
  inv \;\colon\; Spec(\Gamma) \longrightarrow Spec(\Gamma)
$$

acting as assigning [[inverses]] with respect to $\circ$.

The key basic fact to use now is that [[tensor product]] of commutative rings exhibits the [[cartesian monoidal category]] structure on $CRing^{op}$, see at _[CRing -- Properties -- Cocartesian comonoidal structure](CRing#CocartesianComnonoidalStructure)_:

$$
  Spec(R_1) \underset{Spec(R_3)}{\times} Spec(R_2) 
  \simeq
  Spec(R_1 \otimes_{R_3} R_2)
  \,.
$$

This means that the above is equivalently a diagram in [[CRing]] of the form

$$
  \array{
    \Gamma \underset{A}{\otimes} \Gamma
    \\
    \uparrow^{\mathrlap{\Psi}}
    \\
    \Gamma 
    \\
    {}^{\mathllap{\eta_L}}\uparrow 
    \downarrow^{\mathrlap{\epsilon}} \;
    \uparrow^{\mathrlap{\eta_R}}
    \\
    A
  }
$$

as well as

$$
  c \; \colon \; \Gamma \longrightarrow \Gamma
$$

and satisfying [[formal duality|formally dual]] conditions, spelled out as def. \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents} below. Here 

* $\eta_L, \etaR$ are called the left and right _[[unit]] maps_;

* $\epsilon$ is called the _co-unit_;

* $\Psi$ is called the _[[comultiplication]]_;

* $c$ is called the _[[antipode]]_ or _conjugation_



=--

+-- {: .num_remark #HopfAlgebrasAsHopfAlgebroids}
###### Remark

Generally, in a commutative Hopf algebroid, def. \ref{CommutativeHopfAlgebroid}, the two morphisms $\eta_L, \eta_R\colon A \to \Gamma$ from remark \ref{CommutativeHopfAlgebroidSpelledOut} need not coincide, they make $\Gamma$ genuinely into a [[bimodule]] over $A$, and it is the [[tensor product]] of [[bimodules]] that appears in remark \ref{CommutativeHopfAlgebroidSpelledOut}. But it may happen that they coincide:

An [[internal groupoid]] $\mathcal{G}_1 \stackrel{\overset{s}{\longrightarrow}}{\underset{t}{\longrightarrow}}$ for which the [[domain]] and [[codomain]] morphisms coincide, $s = t$, is euqivalently a [[group object]] in the [[slice category]] over $\mathcal{G}_0$.

Dually, a [[commutative Hopf algebroid]] $\Gamma \stackrel{\overset{\eta_L}{\longleftarrow}}{\underset{\eta_R}{\longleftarrow}} A$ for which $\eta_L$ and $\eta_R$ happen to coincide is equivalently a commutative [[Hopf algebra]] $\Gamma$ over $A$.

=--

Writing out the formally dual axioms of an [[internal groupoid]] as in remark \ref{CommutativeHopfAlgebroidSpelledOut} yields the following equivalent but maybe more explicit definition of commutative Hopf algebroids, def. \ref{CommutativeHopfAlgebroid}

+-- {: .num_defn #CommutativeHopfAlgebroidDefinitionInExplicitComponents}
###### Definition

A **[[commutative Hopf algebroid]]** is

1. two [[commutative rings]], $R$ and $\Gamma$;

1. ring [[homomorphisms]]

   1. (left/right unit) 
  
      $\eta_L,\eta_R \colon A \longrightarrow \Gamma$; 

   1. (comultiplication) 
 
      $\Psi \colon \Gamma \longrightarrow \Gamma \underset{A}{\otimes} A$;

   1. (counit) 
 
      $\epsilon \colon \Gamma \longrightarrow A$;

   1. (conjugation) 

      $c \colon \Gamma \longrightarrow \Gamma$

such that

1. (co-[[unitality]])

   1.  $\epsilon \circ \eta_L = \epsilon \circ \eta_R = id_A$;

   1. $(id_\Gamma\otimes_A\epsilon) \circ \Delta  = (\epsilon \otimes_A id_\Gamma) \circ \Delta = id_\Gamma$;

1. (co-[[associativity]]) $(id_\Gamma \otimes_A \Psi) \circ \Psi = (\Psi \otimes_A id_\Gamma) \circ \Psi$;

1. ([[inverses]])

   1. $c \circ c = id_\Gamma$;

   1. $c\circ \eta_L = \eta_R$; $c \circ \eta_R = \eta_L$;

   1. the universally induced $\nabla_c \colon \Gamma \otimes_A \Gamma \longrightarrow \Gamma$ satifies

      $\nabla_c \circ \Psi = \epsilon \circ \eta_L = \epsilon \circ \eta_R$.
   
=--

+-- {: .num_defn #HopfComoduleRing}
###### Definition

Given a [[commutative Hopf algebroid]] $\Gamma$ over $A$ as in def. \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents}, hence an [[internal groupoid]] in $CRing^{op}$, then a **comodule ring** over it is an [[action]] in $CRing^{op}$ of that internal groupoid.

=--

In the same spirit, a **[[comodule]]** over a commutative Hopf algebroid (not necessarily a comodule ring) is a [[quasicoherent sheaf]] on the corresponding [[internal groupoid]] (regarded as a ([[algebraic stack|algebraic]]) [[stack]]) (e.g. [Hopkins 99, prop. 11.6](#Hopkins99)). Explicitly in components:

+-- {: .num_defn #CommutativeHopfAlgebroidComodule}
###### Definition

Given a [[commutative Hopf algebroid]] $\Gamma$ over $A$, def. \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents},
then a **left [[comodule]]** over $\Gamma$ is

1. an $A$-[[module]] $N$;

1. an $A$-[[module]] [[homomorphism]] (co-action)

   $\Psi_N \;\colon\; N \longrightarrow \Gamma \otimes_A N$;

such that

1. ([[unitality]])

   $(\epsilon \otimes_A id_N) \circ \Psi_N = id_N$;

1. ([[associativity]])

   $(\Psi \otimes_A N) \circ \Psi_N = (id_\Gamma \otimes_A \Psi_N)\circ \Psi_N$.

A [[homomorphism]] between comodules $N_1 \to N_2$ is a homomorphism of underlying $A$-modules making [[commuting diagrams]] with the co-action morphism. Write

$$
  \Gamma CoMod
$$

for the resulting [[category]] of (left) comodules over $\Gamma$.

=--


+-- {: .num_prop #CoFreeComodules}
###### Proposition

Given a [[commutative Hopf algebroid]] $\Gamma$ over $A$, there is a [[free-forgetful adjunction]]

$$
  \Gamma CoMod
   \stackrel{\overset{co-free}{\longleftarrow}}{\underset{forget}{\longrightarrow}}
  A Mod
$$

between the [[category]] of $\Gamma$-[[comodules]], def. \ref{CommutativeHopfAlgebroidComodule} and the [[category of modules]] over $A$, where the [[cofree functor]] is [[right adjoint]]. 

The co-free $\Gamma$-[[comodule]] on an $A$-module $N$ is $\Gamma \otimes_A N$ equipped with the [[coaction]] induced by the [[comultiplication]] $\Psi$ in $\Gamma$.

=--


Now we identify the [[commutative Hopf algebroids]] arising in the $E$-Adams spectral sequence:

+-- {: .num_prop #HopfAlgebroidStructureOnDualEOperations}
###### Proposition

If $E$ is flat according to def. \ref{FlatE}, then,
via the isomorphism of proposition \ref{FlatnessOfEImpliesKeyConsequence}, the cosimplicial spectrum $E^{\wedge^\bullet} \wedge X$ (the $E$-standard resolution of $X$ from example \ref{StandardEResolution}) exhibits:

1. for $X = E$: [[Hopf algebroid]]-structure, def. \ref{CommutativeHopfAlgebroid}, remark \ref{CommutativeHopfAlgebroidSpelledOut}, on $E_\bullet(E)$ over $\pi_\bullet(E)$ -- called the **dual $E$-[[Steenrod algebra]]**;

1. for general $X$: [[comodule]]-structure on $E_\bullet(X)$ over the dual $E$-[[Steenrod algebra]].

=--

(e.g. [Baker-Lazarev 01, theorem 1.1](#BakerLazarev01))

+-- {: .proof}
###### Proof

Via prop. \ref{FlatnessOfEImpliesKeyConsequence}, the image under $\pi_\bullet(-)$ of the cosimplicial spectrum $E^{\wedge^\bullet}(E)$ is identified as on the right of the following diagram

$$
  \array{
    \pi_\bullet(E\wedge E \wedge E) &\simeq& E_\bullet(E) \otimes_{\pi_\bullet(E)} E_\bullet(E)
    \\
    \uparrow^{\mathrlap{\pi_\bullet(id \wedge e \wedge id)}}
    &&
    \uparrow^{\mathrlap{\Psi}}
    \\
    \pi_\bullet(E \wedge E) &=& E_\bullet(E)
    \\
    {}^{\mathllap{\pi_\bullet(e \wedge id)}}\uparrow
     \downarrow^{\mathrlap{\pi_\bullet(\mu)}}
     \;\;\;\;\;\;
     \uparrow^{\mathrlap{\pi_\bullet(id \wedge e)}}
     &&
     {}^{\mathllap{\eta_L}}\uparrow 
     \downarrow^{\mathrlap{\epsilon}} 
     \uparrow^{\mathrlap{\eta_R}}
    \\
    \pi_\bullet(E) &=& \pi_\bullet(E)
  }
  \,.
$$

Analogously the [[coaction]] is induced as on the right of the following diagram

$$
  \array{
    \pi_\bullet(E\wedge E \wedge X) &\simeq& E_\bullet(E) \otimes_{\pi_\bullet(E)} E_\bullet(X)
    \\
    \uparrow^{\mathrlap{\pi_\bullet(id \wedge e \wedge id)}}
    &&
    \uparrow^{\mathrlap{\Psi_X}}
    \\
    \pi_\bullet(E \wedge X) &=& E_\bullet(X)
  }
  \,.
$$

=--


+-- {: .num_example}
###### Example

Examples of [[commutative ring spectra]] $E$ for which the dual $E$-[[Steenrod algebra]] $E_\bullet(E)$ over $\pi_\bullet(E)$ of corollary \ref{HopfAlgebroidStructureOnDualEOperations} happens to be a [[commutative Hopf algebra]] over $\pi_\bullet(E)$ instead of a more general [[commutative Hopf algebroid]], according to remark \ref{HopfAlgebrasAsHopfAlgebroids}, includes the cases

$E = $

* [[HA|H]]$\mathbb{F}_p$,

* ...

=--

The key use of the Hopf coalgebroid structure of prop. \ref{HopfAlgebroidStructureOnDualEOperations} for the present purpose is that it is extra structure inherited from maps of spectra under smashing with $E$:

+-- {: .num_example #SmashingMapsWithEFactorsThroughSteenrodComoduleHomomorphisms}
###### Example

For $Y,N$ any two [[spectra]], the morphism (of $\mathbb{Z}$-[[graded abelian groups]]) given by [[smash product of spectra|smash product]] with $E$

$$
  \pi_\bullet(E \wedge -)
    \;\colon\;
  \pi_\bullet([Y,N])
    \longrightarrow
  Hom^\bullet_{Ab}(E_\bullet(Y), E_\bullet(N))
$$

factors through $E_\bullet(E)$-[[comodule]] [[homomorphisms]] over the dual $E$-[[Steenrod algebra]]:

$$
  \pi_\bullet(E \wedge -)
    \;\colon\;
  \pi_\bullet([Y,N])
    \longrightarrow
  Hom^\bullet_{E_\bullet(E)}(E_\bullet(Y), E_\bullet(N))
    \longrightarrow
  Hom^\bullet_{Ab}(E_\bullet(Y), E_\bullet(N))
  \,.
$$

=--

In order to put all this together, we need to invoke a [[universal coefficient theorem]] in the following form.

+-- {: .num_prop #AdamsUCT}
###### Proposition

If $E$ is among the examples [[sphere spectrum|S]], [[HR]] for $R = \mathbb{F}_p$, [[MO]], [[MU]], [[MSp]], [[KO]], [[KU]], then for all $E$-[[module spectra]] $N$ with [[action]] $\rho \colon E\wedge N \to N$
the morphism of $\mathbb{Z}$-[[graded abelian groups]]

$$
 \pi_\bullet[Y,N] 
   \stackrel{\phi \mapsto \rho \circ (id\wedge \phi)}{\longrightarrow}
  Hom_{\pi_\bullet(E)}^\bullet(E_\bullet(Y), \pi_\bullet N)_\bullet
$$

(from the [[stable homotopy group]] of the [[mapping spectrum]] to the [[hom-object|hom groups]] of $\pi_\bullet(E)$-[[modules]])

is an [[isomorphism]].


=--

This is the [[universal coefficient theorem]] of ([Adams 74, chapter III, prop. 13.5](#Adams74)), see also ([Schwede 12, chapter II, prop. 6.20](#Schwede12)).

With this we finally get the following statement, which serves to identity maps of certain spectra with their induced maps on $E$-homology:

+-- {: .num_prop}
###### Proposition

If the assumptions of prop. \ref{AdamsUCT} hold, then for $X,N$ any two [[spectra]], the morphism of $\mathbb{Z}$-[[graded abelian groups]] from example \ref{SmashingMapsWithEFactorsThroughSteenrodComoduleHomomorphisms} in the form

$$
 \pi_\bullet(E\wedge (-))
   \;\colon\;
 \pi_\bullet[Y, E\wedge N] 
   \stackrel{}{\longrightarrow}
  Hom_{E_\bullet(E)}^\bullet(E_\bullet(Y), E_\bullet(Y)))
$$

is an [[isomorphism]].

=-- 

([Adams 74, part III, page 323](#Adams74))


+-- {: .proof}
###### Proof

By the general formula for expressing [[adjuncts]], the morphism fits into the following [[commuting diagram]]

$$
  \array{
    [Y, E \wedge N]
      &\stackrel{\pi_\bullet(E\wedge(-))}{\longrightarrow}&
    Hom_{E_\bullet(E)}(
      E_\bullet(Y), 
      E_\bullet(E \wedge N)
    )
    \\
    {}^{\mathllap{{\phi \mapsto} \atop {\mu \circ (id \wedge \phi)}}}
      \downarrow^{\mathrlap{\simeq}}
    && \downarrow^{\mathrlap{\simeq}}
    \\
    Hom_{\pi_\bullet(E)}(E_\bullet(Y), E_\bullet(N))
      &\stackrel{\simeq}{\longleftarrow}& 
    Hom_{E_\bullet(E)}(
      E_\bullet(Y), 
      E_\bullet(E) \otimes_{\pi_\bullet(E)} E_\bullet(E)
    )
  }
  \,,
$$

where 

1. the right vertical map comes from the isomorphism of prop. \ref{FlatnessOfEImpliesKeyConsequence};

1. the bottom isomorphism is the cofree/forgetful [[adjunction]] isomorphism of prop. \ref{CoFreeComodules};

1. the the left vertical morphism is an isomorphism by prop. \ref{AdamsUCT}. 

Therefore also the top morphism is an iso.

=--

In conclusion:

+-- {: .num_prop #E1PageOfStandardEAdamsSpectralSequenceIsEBarComplex}
###### Proposition

For $X, Y$ [[spectra]], and for $E$ a [[commutative ring spectrum]] from the list in example \ref{ExamplesOfFlatRingSpectra}, then the $\mathcal{E}_1$-page of the $E$-Adams spectral sequence, def. \ref{EAdamsSpectralSequence}, for $[Y,X]$, induced by of the standard $E$-Adams resolution for $X$, example \ref{StandardEResolution}, is of the form

$$
  0 
    \to 
  Hom_{E_\bullet(E)}^\bullet(E_\bullet(Y),E_\bullet(X))
    \stackrel{d_1}{\longrightarrow}
  Hom_{E_\bullet(E)}^\bullet(
     E_\bullet(Y),
     E_\bullet(E) \otimes_{\pi_\bullet(E)} E_\bullet(X)
  )
    \stackrel{d_1}{\longrightarrow}
  Hom_{E_\bullet(E)}^\bullet(
     E_\bullet(Y),
     E_\bullet(E) \otimes_{\pi_\bullet(E)}  E_\bullet(E) \otimes_{\pi_\bullet(E)} E_\bullet(X)
   )
    \stackrel{d_1}{\longrightarrow}
   \cdots
  \,.
$$

=--

The next step is to identify the chain homology of this $d_1$ with the comodule [[Ext]]-groups.

#### The second page and homological co-algebra
 {#TheE2TermOfTheEAdamsSpectralSequence}


+-- {: .num_theorem #SecondPageOfEAdamsSpectralSequence}
###### Theorem

If $E$ is flat, def. \ref{FlatE}, and satisfies the conditions of prop. \ref{AdamsUCT}, and $E_\bullet(Y)$ a [[projective module]] over $\pi_\bullet(E)$, then the entries of the $\mathcal{E}_2$-page
of any $E$-Adams spectral sequence, def. \ref{EAdamsSpectralSequence}, for $[Y,X]$ are the [[Ext]]-groups of [[commutative Hopf algebroid]]-[[comodules]] for the [[commutative Hopf algebroid]] structure on $E$-operations $E_\bullet(E)$ from prop.  \ref{HopfAlgebroidStructureOnDualEOperations}:

$$
  \mathcal{E}^{s,t}_2
  \simeq
  Ext^{s,t}_{E_\bullet(E)}(E_\bullet(Y), E_\bullet(X))
  \,,
$$


=--

+-- {: .proof}
###### Proof

By prop. \ref{UniquenessOfEAdamsSpectralSequence} it is sufficient to show this for the standard $E$-Adams resolution of prop. \ref{StandardAdamsResolutionIsIndeedAdamsResolution}. 
For that case the $\mathcal{E}_1$ page is given by prop. \ref{E1PageOfStandardEAdamsSpectralSequenceIsEBarComplex}, and so by the standard theory of [[derived functors in homological algebra]] (see the section _[Via acyclic resolutions](derived+functor+in+homological+algebra#ViaAcyclicResolutions)_), it is now sufficient to see that:

1. the category $E_\bullet(E) CoMod$ is an [[abelian category]];

1. the graded chain complex of prop. \ref{E1PageOfStandardEAdamsSpectralSequenceIsEBarComplex} is the image under the [[hom-functor]] $F \coloneqq Hom_{E_\bullet(E)}(E_\bullet(Y),-)$ of an $F$-[[acyclic resolution]] of $E_\bullet(X)$.

These two statements are prop. \ref{CategoryOfHopfComodulesIsAbelianIfHopfAlgebroidIsFlat} and lemma \ref{CoFreeHopfComodulesAreHomNAcyclicForProjectiveN} below.

=--


We now discuss the relevant general aspects of [[homological algebra]] in [[categories]] of [[comodules]] over [[commutative Hopf algebroids]] needed for the proof of theorem \ref{SecondPageOfEAdamsSpectralSequence} from prop. \ref{E1PageOfStandardEAdamsSpectralSequenceIsEBarComplex}.

+-- {: .num_prop #CategoryOfHopfComodulesIsAbelianIfHopfAlgebroidIsFlat}
###### Proposition

If a [[commutative Hopf algebroid]] $\Gamma$ over $A$, def. \ref{CommutativeHopfAlgebroid}, \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents} is such that $\eta_L, \eta_R \colon A \longrightarrow \Gamma$ is a [[flat morphism]], then the [[category]] $\Gamma CoMod$ of [[comodules]] over $\Gamma$, def. \ref{CommutativeHopfAlgebroidComodule}, is an [[abelian category]].

=--

(e.g. [Ravenel 86, theorem A1.1.3](#Ravenel86)) 

+-- {: .proof}
###### Proof

It is clear that, without any condition the Hopf algebroid, $\Gamma CoMod$ is an [[additive category]]. 

We need to show that with the assumption that $\Gamma$ is flat over $A$, then this is also a [[pre-abelian category]] in that [[kernels]] and [[cokernels]] exist. Let $f \colon (N_1,\Psi_{N_1}) \longrightarrow (N_2,\Psi_{N_2})$ be a morphism of comodules, hence a [[commuting diagram]] in $A$[[Mod]] of the form

$$
  \array{
    N_1 &\stackrel{f}{\longrightarrow}& N_2
    \\
    \downarrow^{\mathrlap{\Psi_{N_1}}} && \downarrow^{\mathrlap{\Psi_{N_2}}}
    \\
    \Gamma \otimes_A N_1
    &\stackrel{id_\Gamma \otimes_A f}{\longrightarrow}&
    \Gamma \otimes_A N_2
  }
  \,.
$$

Consider the kernel $ker(f)$ of $f$ in $A$[[Mod]] and its image under $\Gamma \otimes_A (-)$

$$
  \array{
    ker(f) &\longrightarrow& N_1 &\stackrel{f}{\longrightarrow}& N_2
    \\
    \downarrow && \downarrow^{\mathrlap{\Psi_{N_1}}} && \downarrow^{\mathrlap{\Psi_{N_2}}}
    \\
    \Gamma \otimes_A ker(f) 
      &\longrightarrow& 
    \Gamma \otimes_A N_1
      &\stackrel{id_\Gamma \otimes_A f}{\longrightarrow}&
    \Gamma \otimes_A N_2
  }
  \,.
$$

By the assumption that $\Gamma$ is a [[flat module]] over $A$, also $\Gamma \otimes_A ker(f) \simeq ker(\Gamma \otimes_A f)$ is a [[kernel]]. By its [[universal property]] this induces uniquely a morphism as shown on the left, making the above [[commuting diagram|diagram commute]]. This means that the $A$-module $ker(f)$ uniquely inherits the structure of a $\Gamma$-comodule such as to make $ker(f) \to N_1$ a comodule homomorphism. By the same universal property it follows that $ker(f)$ with this comodule structure is in fact the kernel of $f$ in $\Gamma CoMod$.

The argument for the existence of [[cokernels]] proceeds [[formal dual|formally dually]]. Therefore it follows that the comparison morphism

$$
  coker(ker(f)) \longrightarrow ker(coker(f))
$$

formed in $\Gamma CoMod$ has underlying it the corresponding comparison morphism in $A Mod$. There this is an [[isomorphism]], hence it is an isomorphism also in $\Gamma CoMod$, and so the latter is not just a [[pre-abelian category]] but in fact an [[abelian category]] itself.

=--

+-- {: .num_prop #CategoryOfHopfComodulesIsAbelianIfHopfAlgebroidIsFlat}
###### Proposition

If a [[commutative Hopf algebroid]] $\Gamma$ over $A$, def. \ref{CommutativeHopfAlgebroid}, \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents} is such that $\eta_L, \eta_R \colon A \longrightarrow \Gamma$ is a [[flat morphism]], then 

1. every co-free $\Gamma$-[[comodule]], def. \ref{CoFreeComodules}, on an [[injective module]] over $A$ is an [[injective object]] in $\Gamma CoMod$;

1. $\Gamma CoMod$ has [[enough injectives]] (if the [[axiom of choice]] holds in the ambient [[set theory]]).

=--

(e.g. [Ravenel 86, lemma A1.2.2](#Ravenel86))

+-- {: .proof}
###### Proof

First of all, assuming the [[axiom of choice]], then the [[category of modules]] $A Mod$ has [[enough injectives]] (see [this proposition](injective+object#AbHasEnoughInjectives)).
Now by prop. \ref{CoFreeComodules} we have the [[adjunction]]

$$
  \Gamma CoMod
   \stackrel{\overset{co-free}{\longleftarrow}}{\underset{forget}{\longrightarrow}}
  A Mod
 \,.
$$

Observe that the [[left adjoint]] is a [[faithful functor]] (being a [[forgetful functor]]) and that, by the proof of prop. \ref{CategoryOfHopfComodulesIsAbelianIfHopfAlgebroidIsFlat}, it is an [[exact functor]]. With this a standard lemma applies ([here](injective+object#TransferOfEnoughInjectivesAlongAdjunctions)) which says that

1. with $I \in A Mod$ an [[injective module]], then the co-free comodule $\Gamma \otimes_A I$ is an [[injective object]] in $\Gamma CoMod$;

1. for $N \in \Gamma CoMod$ any object, and for $i \colon U(N) \hookrightarrow I$ a monomorphism of $A$-modules into an injective $A$-module, then the [[adjunct]] $\tilde i \colon N \hookrightarrow \Gamma\otimes_A I$ is a monomorphism in $\Gamma CoMod$ (and into an injective comodule).

=--


+-- {: .num_lemma #CoFreeHopfComodulesAreHomNAcyclicForProjectiveN}
###### Lemma

Let $\Gamma$ be a [[commutative Hopf algebroid]] over $A$, def. \ref{CommutativeHopfAlgebroid}, \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents}, such that $\eta_L, \eta_R \colon A \longrightarrow \Gamma$ is a [[flat morphism]], 
Let $N \in \Gamma CoMod$ be a Hopf [[comodule]], def. \ref{CommutativeHopfAlgebroidComodule}, such that the underlying $A$-module is a [[projective module]] (a [[projective object]] in $A$[[Mod]]). 

Then  (assuming the [[axiom of choice]]) every co-free commodule, prop. \ref{CoFreeComodules}, is an $F$-[[acyclic object]] for $F$ the [[hom functor]] $Hom_{\Gamma CoMod}(N,-)$.

=--

+-- {: .proof}
###### Proof

We need to show that the [[derived functors in homological algebra|derived functors]] $R^{\bullet} Hom_{\Gamma}(N,-)$ vanish in positive degree on all co-free comodules, hence on $\Gamma \otimes_A K$, for $K \in A Mod$. 

To that end, let $I^\bullet$ be an [[injective resolution]] of $K$ in $A Mod$. By prop. \ref{CategoryOfHopfComodulesIsAbelianIfHopfAlgebroidIsFlat} then $\Gamma \otimes_A I^\bullet$ is a sequence of [[injective objects]] in $\Gamma CoMod$ and by the assumption that $\Gamma$ is flat over $A$ it is an [[injective resolution]] of $\Gamma \otimes_A K$ in $\Gamma CoMod$. Therefore the derived functor in question is given by

$$
  \begin{aligned}
    R^{\bullet \geq 1} Hom_\Gamma(N, \Gamma \otimes_A K)
    & \simeq
    H_{\bullet \geq 1}( Hom_\Gamma( N, \Gamma \otimes_A I^\bullet ) )
    \\
    & \simeq H_{\bullet \geq 1}( Hom_A(N, I^\bullet) )
    \\
    & \simeq 0
  \end{aligned}
  \,.
$$

Here the second equivalence is the cofree/forgetful adjunction isomorphism of prop. \ref{CoFreeComodules}, while the last equality then follows from the assumption that the $A$-module underlying $N$ is a [[projective module]] (since [[hom functors]] out of [[projective objects]] are [[exact functors]] ([here](projective+object#EquivalenceOfDefinitionsInAbelian)) and since derived functors of exact functors vanish in positive degree ([here](derived+functor+in+homological+algebra#DerivedFunctorOfExactFunctor))).


=--

With lemma \ref{CoFreeHopfComodulesAreHomNAcyclicForProjectiveN} the proof of theorem \ref{SecondPageOfEAdamsSpectralSequence} is completed.


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



#### The classical case $X = \mathbb{S}$ and $E = H \mathbb{F}_p$
 {#ClassicalCase}

(...)

([Bruner 09](#Bruner09))

(...)

<img src="http://ncatlab.org/nlab/files/ClassicalAdamsSpectralSequence.jpg" width="600" >

(graphics taken from ([[Symmetric spectra|Schwede 12]]))

(...)


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

This is due to ([Adams 58](#Adams58)). Review includes([Ravenel 86, theorem, 2.1.1, def. 2.1.8](#Ravenel86), [Bruner 09](#Bruner09)).

(...)



#### The case $X = \mathbb{S}$ and $E = MU$
 {#TheAdamsNovikovSpectralSequence}


(...)

[[Adams-Novikov spectral sequence]]

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

In this form this appears as ([Lurie 10, theorem 2](#Lurie10)). A review is in ([Wilson 13, 1.3](#Wilson13)). For the analog of this in the traditional formulation see ([Ravenel 86, ch. 3, prop. 3.1.2](#Ravenel86)).



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



## Related concepts

* [[change of rings theorem]]

* [[Adams-Novikov spectral sequence]]

* [[Bousfield-Kan spectral sequence]]

* [[May spectral sequence]], [[chromatic spectral sequence]]


* [[Steenrod algebra]]

* [[descent spectral sequence]]

[[!include Lurie spectral sequences -- table]]


## References


### General

The original sources are

* {#Adams58} [[Frank Adams]], _On the structure and applications of the Steenrod algebra_, Comm. Math. Helv. 32 (1958), 180&#8211;214.
 
* {#Novikov67} [[Sergei Novikov]], _The methods of algebraic topology from the viewpoint of cobordism theories_, Izv. Akad. Nauk. SSSR. Ser. Mat. 31 (1967), 855&#8211;951 (Russian). ([[Novikov67.pdf:file]])

* {#Adams74} [[Frank Adams]],  _[[Stable homotopy and generalized homology]]_, Chicago Lectures in mathematics, 1974
 
Convergence was notably discussed in

* {#Bousfield79} [[Aldridge Bousfield]], _The localization of spectra with respect to homology_, Topology 18 (1979), no. 4, 257--281. ([pdf](http://www.uio.no/studier/emner/matnat/math/MAT9580/v12/undervisningsmateriale/bousfield-topology-1979.pdf))

* {#Ravenel84} [[Douglas Ravenel]], _Localization with respect to certain periodic homology theories_, American Journal of Mathematics, Vol. 106, No. 2, (Apr., 1984), pp. 351-414 ([pdf](https://www.math.rochester.edu/people/faculty/doug/mypapers/loc.pdf))

The [[spectrum]]-level discussion of the ASS goes back to around

* R. M. F. Moss, _On the composition pairing of Adams spectral sequences_, Proceedings of the London Mathematical Society 3.1 (1968): 179-192.

A streamlined presentation of this close in spirit to constructions in [[homological algebra]] was given in

* {#Miller81} [[Haynes Miller]], _On relations between Adams spectral sequences, with an application to the stable homotopy of a Moore space_, J. Pure Appl. Algebra 20 (1981) ([pdf](http://math.mit.edu/~hrm/papers/miller-relations-between-adams-spectral-sequences.pdf))

and is reproduced in 

* {#Hopkins99} [[Mike Hopkins]], section 5 of _[[Complex oriented cohomology theories and the language of stacks]]_, course notes 1999 ([pdf](https://www.math.rochester.edu/people/faculty/doug/otherpapers/coctalos.pdf))

* {#Aramian} [[Nersés Aramian]], _The Adams spectral sequence_ ([[AramianANSS.pdf:file]])

For full details of some of the steps involved see also ([Schwede 12](#Schwede12)).


Reviews include

* {#Ravenel86} [[Doug Ravenel]], _[[Complex cobordism and stable homotopy groups of spheres]]_, 1986 onwards

* {#Kochmann96} [[Stanley Kochman]], section 3.6 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* {#McCleary01} [[John McCleary]], chapter 9 of _[A user's guide to spectral sequences](https://pages.vassar.edu/mccleary/books/users-guide-to-spectral-sequences/)_, Cambridge University Press, 2001 

* {#Ravenel06} [[Doug Ravenel]], _A Novice's guide to the Adams-Novikov spectral sequence_, in Geometric Applications of Homotopy Theory II Volume 658 of the series Lecture Notes in Mathematics pp 404-475, 2006(?)

* {#Goerss2007} [[Paul Goerss]], _The Adams-Novikov spectral sequence and the Homotopy Groups of Spheres_, lecture notes 2007 ([pdf](http://www.math.northwestern.edu/~pgoerss/papers/stras1.pdf))

* [[Alan Hatcher]], _[Spectral sequences in algebraic topology](http://www.math.cornell.edu/~hatcher/SSAT/SSATpage.html)_ _II: The Adams spectral sequence_ ([pdf](http://www.math.cornell.edu/~hatcher/SSAT/SSch2.pdf))

* {#Bruner09} [[Robert Bruner]], _An Adams spectral sequence primer_, 2009 ([pdf](http://www.math.wayne.edu/~rrb/papers/adams.pdf))

* {#Schwede12} [[Stefan Schwede]], chapter II, section 10.3 of  _[[Symmetric spectra]]_, 2012

* {#Rognes12} [[John Rognes]], _The Adams spectral sequence_ (following [Bruner 09](#Bruner09)), 2012 ([pdf](http://folk.uio.no/rognes/papers/notes.050612.pdf))

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

* {#Wilson13} [[Dylan Wilson]] _Spectral Sequences from Sequences of Spectra: Towards the Spectrum of the Category of Spectra_ lecture at [2013 Pre-Talbot Seminar](http://math.harvard.edu/~hirolee/pretalbot2013/), March 2013 ([[DylanWilsonOnANSS.pdf:file]])


 
### Hopf algebroid $Ext$-structure on $E^2$
 {#ReferencesHopfAlgebroidStructure}

* appendix A.1 of [Ravenel 86](#Ravenel86)

* {#Baker} [[Andrew Baker]], _Brave new Hopf algebroids and the Adams spectral sequence for $R$-modules_ ([pdf](http://www.maths.gla.ac.uk/~ajb/dvi-ps/brave-ha.pdf))
 

* {#BakerLazarev01} [[Andrew Baker]], [[Andrey Lazarev]], _On the Adams Spectral Sequence for $R$-modules_, Algebr. Geom. Topol. 1 (2001) 173-199 ([arXiv:math/0105079](http://arxiv.org/abs/math/0105079))
 

* {#BakerJeanneret02} [[Andrew Baker]] and Alain Jeanneret, _Brave new Hopf algebroids and extensions of $MU$-algebras_, Homology Homotopy Appl. Volume 4, Number 1 (2002), 163-173. ([Euclid](http://projecteuclid.org/euclid.hha/1139840059))
 

* {#Hovey03} [[Mark Hovey]], _Homotopy theory of comodules over a Hopf algebroid_ ([arXiv:math/0301229](http://arxiv.org/abs/math/0301229)) 
 
### Further examples with more general coefficients

For [[tmf]]

* [[Mark Behrens]], _The Adams spectral sequence for $tmf$_ ([[BehrensANSSfortmf.pdf:file]])

* [[Michael Hill]], _The 3-local $tmf$-homology of $B \Sigma_3$_, Proceedings of the AMS, 2007 ([pdf](http://www.ams.org/journals/proc/2007-135-12/S0002-9939-07-08937-X/S0002-9939-07-08937-X.pdf))

[[!redirects Adams spectral sequences]]