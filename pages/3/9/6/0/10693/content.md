
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

* [Classical definition](#ClassicalDefinition)

* [Via injective resolutions](#ViaInjectiveResolutions)
 
### Classical definition
 {#ClassicalDefinition}

For $X$ a [[spectrum]] and $E^\bullet$ a [[generalized cohomology theory]] [[Brown representability theorem|represented]] by a [[spectrum]] $E$, then an _$E$-Adams resolution_ of $X$ is a [[diagram]] of the form

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
$$

where 

* each $K_i$ is a [[smash product]] of [[suspensions]] of $E$;

* each $F_{n+1} \to F_n \to K_n$ is a [[homotopy fiber sequence]];

* each $f_n$ is a surjection on [[cohomology]].

The original and default case is that where $E = H \mathbb{F}_p$ is an [[Eilenberg-MacLane spectrum]] with mod $p$ [[coefficients]], in which case $E^\bullet$ is [[ordinary cohomology]] with these coefficients.
In this case the $K_i$ are [[generalized Eilenberg-MacLane spectra]].

The [[long exact sequences of homotopy groups]] for all the [[homotopy fibers]] in this diagram arrange into a diagram of the form

$$
  \array{
    \vdots
    \\
    \downarrow & \nwarrow
    \\
    \pi_\bullet(F_2) &\stackrel{\pi_\bullet(f_2)}{\longrightarrow}& \pi_\bullet(K_2)
    \\
    \downarrow & \nwarrow^{\mathrlap{\pi_\bullet(\partial_2)}}
    \\
    \pi_\bullet(F_1) &\stackrel{\pi_\bullet(f_1)}{\longrightarrow}& \pi_\bullet(K_1)
    \\
    \downarrow & \nwarrow^{\mathrlap{\pi_\bullet(\partial_1)}}
    \\
    \pi_\bullet(X) &\stackrel{\pi_\bullet(f_0)}{\longrightarrow}& \pi_\bullet(K_0)
  }
  \,,
$$

where the diagonal maps are the images of the [[connecting homomorphisms]] and hence decrease degree in $\pi_\bullet$ by one. This is an (unrolled) [[exact couple]]. The corresponding [[spectral sequence]] is the [[Adams spectral sequence]] induced by the given Adams resolution.

In the case of $E = H \mathbb{F}_p$, applying [[cohomology]] $H^\bullet(-, \mathbb{F}_p)$ to the original diagram
yields  a [[free resolution]] of the [[cohomology ring]] $H^\bullet(X,\mathbb{Z}_p)$ by a [[chain complex]] of [[free modules]] over the [[Steenrod algebra]] $A_p$. 

$$
  \array{
    H^\bullet(K_0) &\leftarrow& H^\bullet(\Sigma K_1) &\leftarrow& H^\bullet(\Sigma^2 K_2)  &\leftarrow& \cdots
    \\
    \downarrow && \downarrow && \downarrow
    \\
    H^\bullet(X)
    &\leftarrow& 0
    &\leftarrow& 0    
   &\leftarrow&  \cdots  
  }
$$

The computaton of the [[cohomology]] of $X$ by means of this resolution is given by the [[Adams spectral sequence]].

### Via injective resolutions
 {#ViaInjectiveResolutions}

A streamlined discussion of $E$-Adams resolutions in close analogy to [[injective resolutions]] in [[homological algebra]] was given in ([Miller 81](#Miller81)), advertized in ([Hopkins 99](#Hopkins99)) and worked out in more detail in ([Aramian](#Aramian)).

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

+-- {: .num_example}
###### Example
**(standatd resolution)**

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

## Related concepts

* [[Whitehead tower]], [[Postnikov tower]]

* [[Adams spectral sequence]]

## References

Traditional accounts include

* {#Ravenel} [[Doug Ravenel]], around Chapter 2, def. 2.1.3 of _[[Complex cobordism and stable homotopy groups of spheres]]_

A streamlined presentation of this close in spirit to constructions in [[homological algebra]] was given in

* {#Miller81} [[Haynes Miller]], _On relations between Adams spectral sequences, with an application to the stable homotopy of a Moore space_, J. Pure Appl. Algebra 20 (1981) ([pdf](http://math.mit.edu/~hrm/papers/miller-relations-between-adams-spectral-sequences.pdf))

and is reproduced and expanded on in 

* {#Hopkins99} [[Mike Hopkins]], section 5 of _Complex oriented cohomology theories and the language of stacks_, course notes 1999 ([pdf](http://www.math.rochester.edu/u/faculty/doug/otherpapers/coctalos.pdf))

* {#Aramian} [[Nersés Aramian]], _The Adams spectral sequence_ ([[AramianANSS.pdf:file]])


[[!redirects Adams resolutions]]