
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

The _Adams spectral sequence_ ([Adams 58](#Adams58)) is a type of [[spectral sequences]] used for computations of [[stable homotopy groups]] of [[spectra]] in terms of their [[generalized homology]]/[[generalized cohomology]]. Given a spectrum $X$ and a [[ring spectrum]] $E$, then under mild assumptions the Adams spectral sequence converges to the [[homotopy groups]] of the $E$-[[nilpotent completion]] of $X$, while under stronger assumptions the latter is the $E$-[[Bousfield localization of spectra|Bousfield localization of spectra]]. The second page of the spectral sequence is given by the $E$-[[homology]] of $X$ as [[modules]] over the dual $E$-[[Steenrod operations]]. The Adams spectral sequence may be seen as a variant of the [[Serre spectral sequence]] obtained by replacing a single fibration by an "[[Adams resolution]]". 

The original _[[classical Adams spectral sequence]]_ is the case where $E = H\mathbb{F}_p$ is [[ordinary homology]] mod $p$, while the _[[Adams-Novikov spectral sequence]]_ ([Novikov 67](#Novikov67)) is the case where $E = $ [[MU]] is [[complex cobordism cohomology theory]] or $E = $ [[BP]], [[Brown-Peterson theory]]. 

Generally, for $E$ a suitable [[E-infinity algebra]] there is a corresponding _$E$-Adams(-Novikov) spectral sequence_ whose second page is given by $E$-[[generalized cohomology]] and which arises as the [[spectral sequence of a simplicial stable homotopy type]] of the [[cosimplicial object|cosimplicial]] object which is the [[Cech nerve]]/[[Sweedler coring]]/[[Amitsur complex]] of $E$. As such the Adams spectral sequence is an analog in [[stable homotopy theory]] of the [[Bousfield-Kan spectral sequence|Bousfield-Kan]] [[homotopy spectral sequence]] in unstable [[homotopy theory]].

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



## Details

1. [Via injective resolutions](#ViaInjectiveResolutions)

1. [As derived descent in higher algebra](#DefinitionInHigherAlgebra)


### The $E$-Adams spectral sequence
 {#ViaInjectiveResolutions}

We here discuss Adams spectral sequences for computation of $E$-[[Bousfield localization of spectra|localization]] of [[mapping spectra]] $[Y,X]$ for $E$ a general [[commutative ring spectrum]] which is flat in a certain sense (def. \ref{FlatE} below).

The _[[classical Adams spectral sequence]]_ is the special case with $Y = X = \mathbb{S}$ the [[sphere spectrum]] and $E = $ [[HA|H]]$\mathbb{F}_p$ the [[Eilenberg-MacLane spectrum]] of a [[prime field]], discussed [below](#ClassicalCase).

The _[[Adams-Novikov spectral sequence]]_ is the special case with $Y = X = \mathbb{S}$ and $E = $ [[MU]], discussed [below](#TheAdamsNovikovSpectralSequence).


#### Spectral sequence of a filtered spectrum
 {#SpectralSequenceOfAFilteredSpectrum}

We introduce the types of [[spectral sequences]] of which the $E$-Adams spectral sequences (def. \ref{AdamsEAdamsSpectralSequence} below) are an example.

+-- {: .num_defn #FilteredSpectrum}
###### Definition

A **[[filtered spectrum]]** is a [[spectrum]] $Y \in Ho(Spectra)$ equipped with a sequence $X_\bullet \colon (\mathbb{N}, \gt) \longrightarrow Ho(Spectra)$ in the [[stable homotopy category]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#GradedAbelianGroupStructureOnHomsInTheHomotopyCategory)) of the form

$$
  \cdots 
   \longrightarrow
  Y_3
    \overset{f_2}{\longrightarrow} 
  Y_2 
    \overset{f_1}{\longrightarrow} 
  Y_1 
    \overset{f_0}{\longrightarrow} 
  Y_0 
    \coloneqq 
  Y
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

More generally a [[filtered object in an (infinity,1)-category|filtering]] on an object $X$ in (stable or not) [[homotopy theory]] is a $\mathbb{Z}$-graded sequence $X_\bullet $ such that $X$ is the [[homotopy colimit]]  $X\simeq \underset{\longrightarrow}{\lim} X_\bullet$. But for the present purpose we stick with the simpler special case of def. \ref{FilteredSpectrum}.

=--


+-- {: .num_remark}
###### Remark

There is _no_ condition on the [[morphisms]] in def. \ref{FilteredSpectrum}. In particular, they are _not_ required to be [[n-monomorphisms]] or [[n-epimorphisms]] for any $n$. 

On the other hand, while they are also not explicitly required to have a presentation by [[cofibrations]] or [[fibrations]], this follows automatically: by the existence of the [[model structure on topological sequential spectra]] ([thm.](Introduction+to+Stable+homotopy+theory+--+1-1#StableModelStructureOnSequentialSpectraIsModelCategory)) or equivalently ([thm.](Introduction+to+Stable+homotopy+theory+--+1-2#SequentialSpectraQuillenEquivalence)) the [[model structure on orthogonal spectra]] ([thm.](Introduction+to+Stable+homotopy+theory+--+1-2#OrthogonalSpectraStableModelStructure)), every filtering on a spectrum is equivalent to one in which all morphisms are represented by [[cofibrations]] or by [[fibrations]]. 

This means that we may think of a filtration on a spectrum in the sense of def. \ref{FilteredSpectrum} as equivalently being a [[tower of fibrations]] over that spectrum.

=--

The following definition \ref{UnrolledExactCoupleOfAFiltrationOnASpectrum} unravels the structure encoded in a filtration on a spectrum, and motivates the concepts of [[exact couples]] and their [[spectral sequences]] from these.


+-- {: .num_defn #UnrolledExactCoupleOfAFiltrationOnASpectrum}
###### Definition
**(exact couple of a filtered spectrum)**

Consider a spectrum $X \in Ho(Spectra)$ and a [[filtered spectrum]] $Y_\bullet$ as in def. \ref{FilteredSpectrum}.

Write $A_k$ for the [[homotopy cofiber]] of its $k$th stage, such as to obtain the diagram

$$
  \array{
   \cdots 
     &\stackrel{}{\longrightarrow}& 
   Y_3 
     &\stackrel{f_2}{\longrightarrow}& 
   Y_2 
     &\stackrel{f_1}{\longrightarrow} & 
   Y_1 
     &\stackrel{f_0}{\longrightarrow}& 
   Y
   \\
   && \downarrow^{\mathrlap{g_3}}
   && \downarrow^{\mathrlap{g_2}}
   && \downarrow^{\mathrlap{g_1}}
   && \downarrow^{\mathrlap{g_0}}
   \\
   && A_3 && A_2 && A_1 && A_0
  }
$$

where each stage

$$
 \array{
   Y_{k+1} &\stackrel{f_k}{\longrightarrow}& Y_k   
   \\
   && \downarrow^{\mathrlap{g_k}}
   \\
   && A_k
 }
$$

is a [[homotopy cofiber sequence]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyFiber)), hence equivalently ([prop.](Introduction+to+Stable+homotopy+theory+--+1-1#HomotopyCofiberSequencesAreHomotopyFiberSequencesInSpectra)) a [[homotopy fiber sequence]], hence where

$$
  Y_{k+1} 
    \overset{f_k}{\longrightarrow}
  Y_k
   \overset{g_k}{\longrightarrow}
  A_k
    \overset{h_k}{\longrightarrow}
  \Sigma Y_{k+1}
$$

is an exact triangle ([prop.](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyCategoryIsTriangulated)).


Apply the graded hom-group functor $[X,-]_\bullet$ ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#GradedAbelianGroupStructureOnHomsInTheHomotopyCategory)) to the above tower. This yields a diagram of $\mathbb{Z}$-[[graded abelian groups]] of the form

$$
  \array{
   \cdots 
     &\stackrel{}{\longrightarrow}& 
   [X,Y_3]_\bullet 
     &\stackrel{[X,f_2]_\bullet)}{\longrightarrow}& 
   [X,Y_2]_\bullet 
     &\stackrel{[X,f_1]_\bullet}{\longrightarrow} & 
   [X,Y_1]_\bullet 
     &\stackrel{[X,f_0]_\bullet}{\longrightarrow}& 
   [X,Y_0]_\bullet
   \\
   && \downarrow^{\mathrlap{[X,g_3]_\bullet}}
   && \downarrow^{\mathrlap{[X,g_2]_\bullet}}
   && \downarrow^{\mathrlap{[X,g_1]_\bullet}}
   && \downarrow^{\mathrlap{[X,g_0]_\bullet}}
   \\
   && [X,A_3]_\bullet 
   && [X,A_2]_\bullet 
   && [X,A_1]_\bullet 
   && [X,A_0]_\bullet
  }
  \,,
$$

where each hook at stage $k$ extends to a [[long exact sequence of homotopy groups]] ([prop.](Introduction+to+Stable+homotopy+theory+--+1-1#LongFiberSequencesOfMapsOfSpectra)) via [[connecting homomorphisms]] $[X,h_k]_\bullet$

$$
  \cdots
    \to
  [X,A_k]_{\bullet+1} 
    \stackrel{\delta_{k,\bullet+1}}{\longrightarrow}
  [X,Y_{k+1}]_{\bullet} 
    \stackrel{[X,f_k]_\bullet}{\longrightarrow}
  [X,Y_k]_\bullet
    \stackrel{[X,g_k]_\bullet}{\longrightarrow}
  [X,A_k]_\bullet
   \stackrel{\delta_{k,\bullet}}{\longrightarrow}
  [X,Y_{k+1}]_{\bullet-1}
    \to 
  \cdots
  \,.
$$

If we regard the [[connecting homomorphism]] $[X,h_k]$ as a morphism of degree -1, then all this information fits into one diagram of the form

$$
  \array{
   \cdots 
     &\stackrel{}{\longrightarrow}& 
   [X,Y_3]_\bullet 
     &\stackrel{[X,f_2]_\bullet}{\longrightarrow}& 
   [X,Y_2]_\bullet 
     &\stackrel{[X,f_1]_\bullet}{\longrightarrow} & 
   [X,Y_1]_\bullet 
     &\stackrel{[X,f_0]_\bullet}{\longrightarrow}& 
   [X,Y_0]_\bullet
   \\
   && 
   \downarrow &{}_{\mathllap{ [X,h_2]_\bullet }}\nwarrow & 
   \downarrow &{}_{\mathllap{ [X,h_1]_\bullet }}\nwarrow &
   \downarrow &{}_{\mathllap{ [X,h_0]_\bullet }}\nwarrow
   & \downarrow^{\mathrlap{[X,g_0]_\bullet}}
   \\
   && [X,A_3]_\bullet 
   && [X,A_2]_\bullet 
   && [X,A_1]_\bullet 
   && [X,A_0]_\bullet
  }
  \,,
$$

where each triangle is a rolled-up incarnation of a [[long exact sequence of homotopy groups]] (and in particular is _not_ a commuting diagram!).

If we furthermore consider the [[bigraded object|bigraded]] [[abelian groups]] $[X,Y_\bullet]_{\bullet}$ and $[X,A_\bullet]_{\bullet}$, then this information may further be rolled-up to a single diagram of the form

$$
  \array{
     [X,Y_\bullet]_\bullet
       & \stackrel{[X,f_\bullet]_\bullet}{\longrightarrow} &
     [X,Y_\bullet]_{\bullet}
     \\
       & {}_{\mathllap{ [X, h_\bullet]_\bullet }}\nwarrow 
       & \downarrow^{\mathrlap{[X, g_\bullet]_\bullet }}
     \\
     && 
     [X,A_\bullet]_\bullet
  }
  \,.
$$

Specifically, regard the terms here as the following bigraded abelian groups

$$
  \begin{aligned}
    D^{s,t}(X,Y) & \coloneqq [X,Y_s]_{t-s}
    \\
    E^{s,t}(X,Y) & \coloneqq [X,A_s]_{t-s}
  \end{aligned}
  \,.
$$

Then the bidegree of the morphisms is



| morphism | bidegree |
|----------|----------|
| $[X,f]$  | $(-1,-1)$ |
| $[X,g]$  | $(0,0)$  |
| $[X,h]$ | $(1,0)$ |


This way $t$ counts the cycles of going around the triangles:

$$
  \cdots
   \to 
  D^{s+1,t+1}(X,Y)
    \stackrel{[X,f]}{\longrightarrow}
  D^{s,t}(X,Y)
    \stackrel{[X,g]}{\longrightarrow}
  E^{s,t}(X,Y)
    \stackrel{[X,h]}{\longrightarrow}
  D^{s+1,t}(X,Y)
    \to
  \cdots
$$

Data of this form is called an _[[exact couple]]_, def. \ref{ExactCouple} below. 


=--


+-- {: .num_defn #UnrolledExactCouple}
###### Definition

An _unrolled [[exact couple]]_ (of _Adams-type_) is a diagram of [[abelian groups]] of the form

$$
  \array{
     \cdots 
       &\stackrel{}{\longrightarrow}& 
     \mathcal{D}^{3,\bullet} 
       &\stackrel{i_2}{\longrightarrow}& 
     \mathcal{D}^{2,\bullet} 
       &\stackrel{i_1}{\longrightarrow} & 
     \mathcal{D}^{1,\bullet} 
       &\stackrel{i_0}{\longrightarrow}& 
     \mathcal{D}^{0,\bullet}
     \\
     && 
     \downarrow^{\mathrlap{}}  &{}_{\mathllap{k_2}}\nwarrow & 
     {}^{\mathllap{j_2}}\downarrow &{}_{\mathllap{k_1}}\nwarrow &
     {}^{\mathllap{j_1}}\downarrow &{}_{\mathllap{k_0}}\nwarrow
     & \downarrow_{\mathrlap{j_0}}
     \\
     && \mathcal{E}^{3,\bullet} && \mathcal{E}^{2,\bullet} 
     && \mathcal{E}^{1,\bullet} && \mathcal{E}^{0,\bullet}
   }
$$

such that each triangle is a rolled-up [[long exact sequence]] of [[abelian groups]] of the form

$$
  \cdots
   \to 
  \mathcal{D}^{s+1,t+1}
    \stackrel{i_s}{\longrightarrow}
  \mathcal{D}^{s,t}
    \stackrel{j_s}{\longrightarrow}
  \mathcal{E}^{s,t}
    \stackrel{k_s}{\longrightarrow}
  \mathcal{D}^{s+1,t}
    \to
  \cdots
  \,.
$$


=--

The collection of this "un-rolled" data into a single diagram of [[abelian groups]] is called the corresponding _[[exact couple]]_.


+-- {: .num_defn #ExactCouple}
###### Definition

An _[[exact couple]]_ is a [[diagram]] (non-commuting) of [[abelian groups]] of the form

$$
  \array{
    \mathcal{D}
    &\stackrel{i}{\longrightarrow}&
    \mathcal{D}
    \\
    & {}_{\mathllap{k}}\nwarrow & \downarrow^{\mathrlap{j}}
    \\
    && \mathcal{E}
  }
  \,,
$$

such that this is [[exact sequence|exact]] in each position, hence such that the [[kernel]] of every [[morphism]] is the [[image]] of the preceding one.

=--


The concept of exact couple so far just collects the sequences of long exact sequences given by a filtration. Next we turn to extracting information from this sequence of sequences.

+-- {: .num_remark #Observingd1}
###### Remark

The sequence of long exact sequences in def. \ref{UnrolledExactCoupleOfAFiltrationOnASpectrum} is inter-locking, in that every $[X,Y_s]_{t-s}$ appears _twice_:

$$
  \array{
    && & \searrow && \nearrow
    \\
    && && [X,Y_{s+1}]_{t-s-1}
    \\
    && & {}^{\mathllap{ [X,h] }}\nearrow 
    && \searrow^{\mathrlap{ [X,g]  }}
    && && && \nearrow
    \\
    && [X,A_s]_{t-s} 
    && \underset{d_1 }{\longrightarrow} 
    && [X, A_{s+1}]_{t-s-1}
    && \stackrel{d_1 }{\longrightarrow} 
    && [X,A_{s+2}]_{t-s-2}
    \\
    & \nearrow && && && {}_{\mathllap{ [X,h] }}\searrow 
    && \nearrow_{\mathrlap{ [X,g] }}
    \\
    && && && && [X,Y_{s+2}]_{t-s-2}
    \\
    && && && & \nearrow && \searrow
  }
$$

This gives rise to the horizontal ("[[splicing of short exact sequences|splicing]]") composites $d_1$, as shown, and by the fact that the diagonal sequences are long exact, these are [[differentials]] in that they square to zero: $(d_1)^2 = 0$. Hence there is a [[cochain complex]]:

$$
  \array{
    \cdots 
       & 
     \overset{}{\longrightarrow}
       && 
     [X,A_s]_{t-s} 
       && 
     \overset{d_1}{\longrightarrow} 
       && 
     [X,A_{S+1}]_{t-s-1}
       && 
     \stackrel{d_1 }{\longrightarrow} 
       && 
     [X,A_{s+2}]_{t-s-2}
       &&
     \longrightarrow & \cdots
  }
  \,.
$$

We may read off from these interlocking long exact sequences what these differentials _mean_, as follows. An element $c \in [X,A_s]_{t-s}$ lifts to an element 
 $\hat c \in[X,Y_{s+2}]_{t-s-1} $ precisely if $d_1 c = 0$:

$$
  \array{
    &\hat c \in & [X, Y_{s+2}]_{t-s-1}
    \\
    && & \searrow^{\mathrlap{ [X,f] }} 
    \\
    && && [X,Y_{s+1}]_{t-s-1}
    \\
    && & {}^{\mathllap{ [X,h] }}\nearrow 
    && \searrow^{\mathrlap{ [X,g]  }}
    \\
    & c \in  & [X,A_s]_{t-s}
    && 
    \underset{ d_1 }{\longrightarrow} 
   && [X,A_{s+1}]_{t-s-1}
  }
$$

In order to organize this observation, notice that in terms of the exact couple of remark \ref{UnrolledExactCoupleOfAFiltrationOnASpectrum}, the differential 

$$
  d_1  \;\coloneqq \; [X,g] \circ [X,h]
$$

is the composite 

$$
  d \coloneqq j \circ k
  \,.
$$


=--

Some terminology:

+-- {: .num_defn #PageOfAnExactCouple}
###### Definition

Given an exact couple, def. \ref{ExactCouple}, 

$$
  \array{
    \mathcal{D}^{\bullet,\bullet}
    &\stackrel{i}{\longrightarrow}&
    \mathcal{D}^{\bullet,\bullet}
    \\
    & {}_{\mathllap{k}}\nwarrow & \downarrow^{\mathrlap{j}}
    \\
    && \mathcal{E}^{\bullet,\bullet}
  }
$$

its **page** is the [[graded object|graded]] [[chain complex]]

$$
  (\mathcal{E}^{\bullet,\bullet}, d \coloneqq j \circ  k)
  \,.
$$

=--

+-- {: .num_defn #DerivedExactCouple}
###### Definition

Given an exact couple, def. \ref{ExactCouple}, then its _derived exact couple_ is the diagram

$$
  \array{
    \widetilde {\mathcal{D}}
    &\stackrel{\tilde i}{\longrightarrow}&
    \widetilde {\mathcal{D}}
    \\
    & {}_{\mathllap{\tilde k}}\nwarrow & \downarrow^{\mathrlap{\tilde j}}
    \\
    && \widetilde{\mathcal{E}}
  }
  \;\;\;\;
    \coloneqq
  \;\;\;\;
  \array{
    im(i) 
      &\stackrel{i}{\longrightarrow}&
    im(i)
    \\
    & {}_{\mathllap{k}}\nwarrow & \downarrow {\mathrlap{j \circ i^{-1}}}
    \\
    && H(\mathcal{E}, j \circ k)
  }
$$

with 

1. $\tilde{\mathcal{E}} \coloneqq ker(d)/im(d)$ (with $d \coloneqq j \circ k$ from def. \ref{PageOfAnExactCouple});

1. $\tilde {\mathcal{D}} \coloneqq im(i)$;

1. $\tilde i \coloneqq i|_{im(i)}$;

1. $\tilde j \coloneqq j \circ i^{-1}$ (where $i^{-1}$ is the operation of choosing any preimage under $i$);

1. $\tilde k \coloneqq k|_{ker(d)}$.


=--

By direct inspection one checks that:

+-- {: .num_lemma #DerivedExactCoupleIsExactCouple}
###### Lemma

The derived exact couple in def. \ref{DerivedExactCouple}
is well defined and is itself an exact couple, def. \ref{ExactCouple}.

=--

+-- {: .num_defn #ExactCoupleSpectralSequence}
###### Definition

Given an exact couple, def. \ref{ExactCouple},
then the induced 
**[[spectral sequence]] of the exact couple** 
is the sequence of pages, def. \ref{PageOfAnExactCouple}, of the induced sequence of derived exact couples, def. \ref{DerivedExactCouple}, lemma \ref{DerivedExactCoupleIsExactCouple}. 

The **$r$th page** of the spectral sequence is the page (def. \ref{PageOfAnExactCouple}) of the $r$th exact couple, denoted 

$$
  \{\mathcal{E}_r, d_r\}
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

So the spectral sequence of an exact couple (def. \ref{ExactCoupleSpectralSequence}) is a sequence of cochain complexes $(\mathcal{E}_r, d_r)$, where the cohomology of one is the terms of the next one: $\mathcal{E}_{r+1} \simeq H(\mathcal{E}_r,d_r)$.

In practice this is used as a successive stagewise approximation to the computation of a limiting term $\mathcal{E}_\infty$. What that limiting term is, if it exists at all, is the subject of _convergence_ of the spectral sequence, we come to this [below](#Convergence).

=--

Def. \ref{ExactCoupleSpectralSequence} makes sense without a (bi-)grading on the terms of the exact couple, but much of the power of spectral sequences comes from the cases where such a bigrading is given, since together with the sequence of pages of the spectral sequence, this tends to organize computation of the successive cohomology groups in an efficient way. Therefore consider:

+-- {: .num_defn #AdamsTypeSpectralSequenceOfATower}
###### Definition

Given a [[filtered spectrum]] as in def. \ref{FilteredSpectrum},

$$
  \array{
   \cdots 
     &\stackrel{}{\longrightarrow}& 
   X_3 
     &\stackrel{f_2}{\longrightarrow}& 
   X_2 
     &\stackrel{f_1}{\longrightarrow} & 
   X_1 
     &\stackrel{f_0}{\longrightarrow}& 
   X
   \\
   && \downarrow^{\mathrlap{g_3}}
   && \downarrow^{\mathrlap{g_2}}
   && \downarrow^{\mathrlap{g_1}}
   && \downarrow^{\mathrlap{g_0}}
   \\
   && A_3 && A_2 && A_1 && A_0
  }
$$

and given another spectrum $X \in Ho(Spectra)$, the induced **[[spectral sequence of a filtered spectrum]]** is the [[spectral sequence]] that is induced, by def. \ref{ExactCoupleSpectralSequence} from the [[exact couple]] (def. \ref{ExactCouple}) given by def. \ref{UnrolledExactCoupleOfAFiltrationOnASpectrum}:

$$
  \array{
    \mathcal{D} &\stackrel{i}{\longrightarrow}& \mathcal{D}
    \\
    &{}_{\mathllap{k}}\nwarrow& \downarrow^{\mathrlap{j}}
    \\
    && \mathcal{E}
  }
  \;\;\;\;\;\;
    \coloneqq
  \;\;\;\;\;\;
  \array{
    \underset{s,t}{\oplus} D^{s,t}(X,Y)
      &\overset{[X,f]}{\longrightarrow}&
    \underset{s,t}{\oplus} D^{s,t}(X,Y)
    \\
    & {}_{\mathllap{ [X, h] }}\nwarrow & \downarrow^{[X,g]}
    \\
    && \underset{s,t}{\oplus} E^{s,t}(X,Y)
  }
  \;\;\;\;
   \coloneqq
  \;\;\;\;
  \array{
    \underset{s,t}{\oplus} [X,Y_s]_{t-s}
      &\overset{[X,f]}{\longrightarrow}&
    \underset{s,t}{\oplus} [X,Y_s]_{t-s}
    \\
    & {}_{\mathllap{ [X,h] }}\nwarrow & \downarrow^{\mathrlap{[X,g]}}
    \\
    && [X,A_s]_{t-s}
  }
$$

with the following bidegree of the differentials:

$$
  deg = \;\;\;\;
  \array{
    \mathcal{D} &\stackrel{(-1,-1)}{\longrightarrow}& \mathcal{D}
    \\
    &{}_{\mathllap{(1,0)}}\nwarrow& \downarrow^{\mathrlap{(0,0)}}
    \\
    && \mathcal{E}
  }
  \,.
$$

In particular the first page is

$$
  \mathcal{E}^{s,t}_1 
   =
  [X,A_s]_{t-s}
$$

$$
  d_1 
    =
  [X, g \circ h]
  \,.
$$


As we pass to derived exact couples, by def. \ref{DerivedExactCouple}, 
the bidegree of $i$ and $k$ is preserved, but that of $j$ increases by 
$(1,1)$ with each page, since

$$
  \begin{aligned}
    deg(\tilde j) 
     &
    = deg( j \circ i^{-1}) 
    \\
     &= deg(j) - deg(i)  
    \\
    & = deg(j) + (1,1)
  \end{aligned}
  \,.
$$

hence the differentials on the $r$th page are of the form

$$
  d_r 
    \;\colon\; 
  \mathcal{E}_r^{s,t} 
    \longrightarrow 
  \mathcal{E}_r^{s+r, t+r-1}
  \,.
$$


<div style="float:right;margin:0 10px 10px 0;">
<img src="http://ncatlab.org/nlab/files/adamstypedifferentials.jpg" width="360" > 
</div>

It is conventional to depict this in tables where $s$ increases vertically and $t-s$ increases horizontally. This is the "Adams type" grading convention for spectral sequences, different from the [[Serre spectral sequence|Serre-]][[Atiyah-Hirzebruch spectral sequence]] convention ([prop.](Introduction+to+Stable+homotopy+theory+--+S#AHSSExistence)).

=--


#### $E$-Adams filtrations
 {#AdamsFiltration}

Given a [[homotopy commutative ring spectrum]] $(E,\mu,e)$, then an _$E$-Adams spectral sequence_ is a [[spectral sequence]] as in def. \ref{AdamsTypeSpectralSequenceOfATower}, where each cofiber is induced from the unit morphism $e \;\colon\; \mathbb{S} \longrightarrow E$:

+-- {: .num_defn #AdamsEAdamsSpectralSequence}
###### Definition

Let $X,Y \in Ho(Spectra)$ be two [[spectra]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#TheStableHomotopyCategory)), and let $(E,\mu,e) \in CMon(Ho(Spectra),\wedge, \mathbb{S})$ be a [[homotopy commutative ring spectrum]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyCommutativeRingSpectrum)) in the [[tensor triangulated category|tensor triangulated]] [[stable homotopy category]] $(Ho(Spectra), \wedge, \mathbb{S})$ ([prop.](Introduction+to+Stable+homotopy+theory+--+1-2#TensorTriangulatedStructureOnStableHomotopyCategory)). 

Then the **$E$-[[Adams spectral sequence]]** for the computation of the [[graded abelian group]] 

$$
  [X,Y]_\bullet
  \coloneqq
  [X, \Sigma^{-\bullet} Y]
$$ 

of morphisms in the [[stable homotopy category]]
([def.](Introduction+to+Stable+homotopy+theory+--+1-1#GradedAbelianGroupStructureOnHomsInTheHomotopyCategory)) is the [[spectral sequence of a filtered spectrum]] (def. \ref{AdamsTypeSpectralSequenceOfATower}) of the image under $[X,-]_\bullet$ of the tower

$$
  \array{
    & \vdots
    \\
    & {}^{\mathllap{f_0}}\downarrow
    \\
    & Y_3 &\overset{g_3}{\longrightarrow}& E \wedge Y_3 = A_3
    \\
    & {}^{\mathllap{f_0}}\downarrow
    \\
    & Y_2 &\overset{g_2}{\longrightarrow}& E \wedge Y_2 = A_2
    \\
    & {}^{\mathllap{f_0}}\downarrow
    \\
    & Y_1 &\overset{g_1}{\longrightarrow}& E \wedge Y_1 = A_1
    \\
    & {}^{\mathllap{f_0}}\downarrow
    \\
    Y = & Y_0 &\overset{g_0}{\longrightarrow}& E \wedge Y_0  = A_0
  }
  \,,
$$

where each hook is a [[homotopy fiber sequence]] (equivalently a [[homotopy cofiber sequence]], [prop.](Introduction+to+Stable+homotopy+theory+--+1-1#HomotopyCofiberSequencesAreHomotopyFiberSequencesInSpectra)), hence where each 

$$
  Y_{n+1} 
    \overset{f_n}{\longrightarrow}
  Y_n 
    \overset{g_n}{\longrightarrow}
  A_n
    \overset{h_n}{\longrightarrow}
  \Sigma Y_{n+1}
$$

is an exact triangle ([prop.](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyCategoryIsTriangulated)), where inductively

$$
  A_n \coloneqq E \wedge Y_n
$$ 

is the derived [[smash product of spectra]] ([corollary](Introduction+to+Stable+homotopy+theory+--+1-2#MonoidalStableHomotopyCategory)) of $E$ with the stage $Y_n$ ([cor.](Introduction+to+Stable+homotopy+theory+--+1-2#MonoidalStableHomotopyCategory)), and where

$$
  g_n
  \;\colon\;
  Y_n 
    \underoverset{\simeq}{\ell^{-1}_{Y_n}}{\longrightarrow} 
  \mathbb{S} \wedge Y_n
    \overset{e \wedge id}{\longrightarrow}
  E \wedge Y_{n}
$$

is the composition of the inverse derived [[unitor]] on $Y_n$ ([cor.](Introduction+to+Stable+homotopy+theory+--+1-2#MonoidalStableHomotopyCategory)) with the derived [[smash product of spectra]] of the unit $e$ of $E$ and the identity on $Y_n$.

Hence, by def \ref{AdamsTypeSpectralSequenceOfATower}, the first page is

$$
  E_1^{s,t}(X,Y)
    \;\coloneqq\;
  [X, A_s ]_{t-s}
$$

and the differentials are of the form

$$
  d_r  
    \;\colon\;
  E_r^{s,t}(X,Y)
    \longrightarrow
  E_r^{s+r, t+r-1}(X,Y)
  \,.
$$

=--

([Adams 74, theorem 15.1 page 318](#Adams74))

It is convenient to adopt the following notation for $E$-Adams spectral sequences (def. \ref{AdamsEAdamsSpectralSequence}):

+-- {: .num_defn #HomotopyFiberOfUnitOfCommutativeRingSpectrum}
###### Definition

For $(E,\mu,e) \in CMon(Ho(Spectra),\wedge, \mathbb{S})$ a [[homotopy commutative ring spectrum]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyCommutativeRingSpectrum)), write $\overline{E}$ for the [[homotopy fiber]] of its unit $e \colon \mathbb{S}\to E$, i.e. such that there is a [[homotopy fiber sequence]] (equivalently a [[homotopy cofiber sequence]], [prop.](Introduction+to+Stable+homotopy+theory+--+1-1#HomotopyCofiberSequencesAreHomotopyFiberSequencesInSpectra)) in the [[stable homotopy category]] $Ho(Spectra)$ of the form

$$
  \overline{E} 
    \longrightarrow 
  \mathbb{S}
    \overset{e}{\longrightarrow}
  E
  \,,
$$

equivalently an [[triangulated category|exact triangle]] ([prop.](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyCategoryIsTriangulated)) of the form

$$
  \overline{E} 
    \longrightarrow 
  \mathbb{S}
    \overset{e}{\longrightarrow}
  E
    \longrightarrow
  \Sigma \overline{E}
  \,.
$$

=--

([Adams 74, theorem 15.1 page 319](#Adams74))

+-- {: .num_lemma #Wp}
###### Lemma

The spectra entering the definition of the $E$-[[Adams spectral sequence]] in def. \ref{AdamsEAdamsSpectralSequence} are equivalently

$$
  Y_p 
    \;\simeq\; 
  \overline{E}^p \wedge Y 
$$

and

$$
  A_p
    \;\simeq\;
  E \wedge \overline{E}^p \wedge Y
  \,.
$$

where we write

$$
  \overline{E}^p
  \coloneqq 
  \underset{
    p\; factors
  }{
    \underbrace{
      \overline{E} \wedge \cdots \wedge \overline{E}
  }} \wedge Y
  \,.
$$

Hence the first page of the $E$-Adams spectral sequence reads equivalently

$$
  E^{s,t}_1(X,Y)
   \simeq
  [X, E \wedge {\overline{E}^s} \wedge Y]_{t-s}
  \,.
$$

=---

([Adams 74, theorem 15.1 page 319](#Adams74))


+-- {: .proof}
###### Proof

By definition the statement holds for $p = 0$. Assume then by [[induction]] that it holds for some $p \geq 0$. Since the [[smash product of spectra]]-functor $(-) \wedge \overline{E}^p \wedge Y$ preserves [[homotopy cofiber sequences]] ([lemma](Introduction+to+Stable+homotopy+theory+--+1-2#SmashTensoringWithSpectrumDerivedPreserveshomotopycofibers), this is part of the [[tensor triangulated category|tensor triangulated]] structure of the [[stable homotopy category]]), its application to the homtopy cofiber sequence 

$$
  \overline{E}
    \longrightarrow
  \mathbb{S}
    \overset{e}{\longrightarrow}
  E
$$

from def. \ref{HomotopyFiberOfUnitOfCommutativeRingSpectrum} yields another homotopy cofiber sequence, now of the form

$$
  \overline{E}^{p+1} \wedge Y
    \longrightarrow
  \overline{E}^p \wedge Y
    \overset{g_p}{\longrightarrow}
  E \wedge \overline{E}^p \wedge Y
$$

where the morphism on the right is identified as $g_p$ by the induction assumption, hence $A_{p+1}\simeq E \wedge \overline{E}^p  \wedge Y$. Since $Y_{p+1}$ is defined to be the homotopy fiber of $g_p$, it follows that $Y_{p+1} \simeq \overline{E}^{p+1} \wedge Y$.

=--

We proceed now to analyze the first two pages and then the convergence properties of $E$-Adams spectral sequences (def. \ref{AdamsEAdamsSpectralSequence}).

#### The first page
 {#FirstPageAndHopfAlgebroid}

By lemma \ref{Wp} the first page of an $E$-Adams spectral sequence (def. \ref{AdamsEAdamsSpectralSequence}) looks like

$$
  \begin{aligned}
    E^{s,t}_1(X,Y)
    & 
    \simeq
    [Y, E \wedge \overline{E}^s \wedge Y]_{s-t}
  \end{aligned}
  \,.
$$


We discuss now how, under favorable conditions, these hom-groups may alternatively be computed as morphisms of $E$-[[generalized homology|homology]] equipped with suitable [[comodule]] structure over a [[Hopf algebroid]] structure on the dual $E$-[[Steenrod operations]] $E_\bullet(E)$ (The $E$-[[generalized homology]] of $E$ ([rmk.](Introduction+to+Stable+homotopy+theory+--+1-2#EMHomology))). Then [below](#TheE2TermOfTheEAdamsSpectralSequence) we discuss that, as a result, the $d_1$-cohomology of the first page computes the [[Ext]]-groups from the $E$-homology of $Y$ to the $E$-homology of $X$, regarded as $E_\bullet(E)$-comodules. 

The condition needed for this to work is the following.

+-- {: .num_defn #FlatE}
###### Definition

Call a [[homotopy commutative ring spectrum]] $(E,\mu,e)$ ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyCommutativeRingSpectrum)) **flat** if the right $\pi_\bullet(E)$-[[module]] structure on $E_\bullet(E)$ ([prop.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyGroupsOfHomotopyCommutativeRingSpectrum)) is a [[flat module]].


=--

+-- {: .num_example #ExamplesOfFlatRingSpectra}
###### Example

Examples of [[commutative ring spectra]] that are flat according to def. \ref{FlatE} include
$E = $

* $\mathbb{S}$ -- the [[sphere spectrum]];

* $H \mathbb{F}_p$ -- [[Eilenberg-MacLane spectra]] for [[prime fields]];

* [[MO]], [[MU]], [[MSp]] -- [[Thom spectra]];

* [[KO]], [[KU]] -- [[topological K-theory]] spectra.


=--

([Adams 69, lemma 28](#Adams69))

+-- {: .proof}
###### Proof

For $\mathbb{S}$ we have $\mathbb{S}_\bullet(\mathbb{S}) \coloneqq \pi_\bullet(\mathbb{S} \wedge \mathbb{S}) \simeq \pi_\bullet(\mathbb{S})$, since the [[sphere spectrum]] $\mathbb{S}$ is the [[tensor unit]] for the derived [[smash product of spectra]] ([cor.](Introduction+to+Stable+homotopy+theory+--+1-2#MonoidalStableHomotopyCategory)). Hence the statement follows since every ring is, clearly, flat over itself.

For $H \mathbb{F}_p$ we have that $\pi_\bullet(H \mathbb{F}_p) \simeq \mathbb{F}_p$ ([prop.](Introduction+to+Stable+homotopy+theory+--+1-2#StableHomotopyGroupsOfEMSpectrum)), hence a [[field]] (a [[prime field]]). Every module over a field is a [[projective module]] ([prop.](projective+module#ModuleOverAFieldIsProjective)) and every projective module is flat ([prop.](flat+module#ProjectiveModulesAreFlat)).

=--

+-- {: .num_example}
###### Example

Examples of ring spectra that are _not_ flat in the sense of def. \ref{FlatE} include [[HA|H]][[integers|Z]], and $M S U$.

=--


The key consequence of the assumption that $E$ is flat in the sense of def. \ref{FlatE} is the following.

+-- {: .num_prop #FlatnessOfEImpliesKeyConsequence}
###### Proposition

For $E$ a [[homotopy commutative ring spectrum]] which is flat according to def. \ref{FlatE}, then for all spectra $X \in Ho(Spectra)$ the canonical morphism 

$$
  E_\bullet(E) \otimes_{\pi_\bullet(E)} E_\bullet(X)
    \stackrel{}{\longrightarrow}
  \pi_\bullet(E \wedge E \wedge X)
$$

is a [[natural isomorphism]].


=--

(e.g. [Adams 74, part III, lemma 12.5](#Adams74), [Schwede 12, prop. 6.20](#Schwede12))

+-- {: .proof}
###### Proof

See the proof of [this prop.](Introduction+to+Stable+homotopy+theory+--+1-2#EnHomology).

=--

Using prop. \ref{FlatnessOfEImpliesKeyConsequence}, we find below (prop. \ref{ComoduleHomsInE1PageOfEAdamsSpectralSequence}) that the first page of the $E$-Adams spectral sequence may be equivalently rewritten as hom-groups of [[comodules]] over $E_\bullet(E)$ regarded as a [[graded commutative Hopf algebroid]]. We now first discuss what this means. 


##### Garded commutative Hopf algebroids

The dual $E$-[[Steenrod algebras]] that we consider [below](#DualESteenrodAlgebra) are not just algebras, but carry a richer alegbraic structure called a _[[commutative Hopf algebroid]] structure_. Below in def. \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents} we say explicitly what this means.  But since it involves a lot of structure, it is useful to know that all this structure is just the dual incarnation of the following simple concept:


+-- {: .num_defn #CommutativeHopfAlgebroid}
###### Definition

A **[[graded commutative Hopf algebroid]]** is an [[internal groupoid]] in the [[opposite category]] $gCRing^{op}$ of [[graded commutative rings]], regarded with its [[cartesian monoidal category]] structure.

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

Dually, a [[commutative Hopf algebroid]] $\Gamma \stackrel{\overset{\eta_L}{\longleftarrow}}{\underset{\eta_R}{\longleftarrow}} A$ for which $\eta_L$ and $\eta_R$ happen to coincide is equivalently a commutative **[[Hopf algebra]]** $\Gamma$ over $A$.

=--

Writing out the formally dual axioms of an [[internal groupoid]] as in remark \ref{CommutativeHopfAlgebroidSpelledOut} yields the following equivalent but maybe more explicit definition of commutative Hopf algebroids, def. \ref{CommutativeHopfAlgebroid}

+-- {: .num_defn #CommutativeHopfAlgebroidDefinitionInExplicitComponents}
###### Definition

A **[[commutative Hopf algebroid]]** is

1. two [[commutative rings]], $A$ and $\Gamma$;

1. ring [[homomorphisms]]

   1. (left/right unit) 
  
      $\eta_L,\eta_R \colon A \longrightarrow \Gamma$; 

   1. (comultiplication) 
 
      $\Psi \colon \Gamma \longrightarrow \Gamma \underset{A}{\otimes} \Gamma$;

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

##### Comodules and cotensor product

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

   $(\Psi \otimes_A id_N) \circ \Psi_N = (id_\Gamma \otimes_A \Psi_N)\circ \Psi_N$.

A [[homomorphism]] between comodules $N_1 \to N_2$ is a homomorphism of underlying $A$-modules making [[commuting diagrams]] with the co-action morphism. We write

$$
  \Gamma CoMod
$$

for the resulting [[category]] of left comodules over $\Gamma$. Analogously for right comodules. The notation for the hom-sets in this category is abbreviated to

$$
  Hom_\Gamma(-,-)
  \coloneqq
  Hom_{\Gamma CoMod}(-,-)
  \,.
$$

These are naturally $A$-modules. If $(\Gamma,A)$ is graded then these are naturally graded $A$-modules, which we denote by

$$
  Hom^\bullet_\Gamma(-,-)
  \,.
$$

=--


+-- {: .num_example #GroundRingIsCanonicalComoduleOverHopfAlgebroid}
###### Example

Given a [[commutative Hopf algebroid]] $\Gamma$ over $A$, def. \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents}, then $A$ itself becomes a left $\Gamma$-[[comodule]] (def. \ref{CommutativeHopfAlgebroidComodule}) with [[coaction]] given by

$$
  \Psi_A
    \;\colon\;
  A 
    \overset{\eta_L}{\longrightarrow}
  \Gamma
    \simeq
  \Gamma \otimes_A A
$$

and a right $\Gamma$-comodule with coaction given by

$$
  \Psi_A
    \;\colon\;
  A 
    \overset{\eta_R}{\longrightarrow}
  \Gamma
    \simeq
  \Gamma \otimes_A A
  \,.
$$

=--

More generally:

+-- {: .num_prop #CoFreeComodules}
###### Proposition

Given a [[commutative Hopf algebroid]] $\Gamma$ over $A$, there is a [[free-forgetful adjunction]]

$$
  \Gamma CoMod
    \underoverset
      {\underset{forget}{\longrightarrow}}
      {\overset{co-free}{\longleftarrow}}
      {\bot}
  A Mod
$$

between the [[category]] of $\Gamma$-[[comodules]], def. \ref{CommutativeHopfAlgebroidComodule} and the [[category of modules]] over $A$, where the [[cofree functor]] is [[right adjoint]]. 

The co-free $\Gamma$-[[comodule]] on an $A$-module $N$ is $\Gamma \otimes_A N$ equipped with the [[coaction]] induced by the [[comultiplication]] $\Psi$ in $\Gamma$.

=--


+-- {: .num_prop #LeftComodulesToRightComodules}
###### Proposition

Consider a [[commutative Hopf algebroid]] $\Gamma$ over $A$, def. \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents}.
Any left comodule $N$ over $\Gamma$ (def. \ref{CommutativeHopfAlgebroidComodule}) becomes a right comodule via the coaction

$$
  N
    \overset{\Psi}{\longrightarrow}
  \Gamma \otimes_A N
    \overset{\simeq}{\longrightarrow}
  N \otimes_A \Gamma
    \overset{id \otimes_A c}{\longrightarrow}
  N \otimes_A \Gamma
  \,,
$$

where the isomorphism in the middle the is [[braiding]] in $A Mod$ and where $c$ is the conjugation map of $\Gamma$.

Dually, a right comodule $N$ becoomes a left comodule with the coaction

$$
  N
    \overset{\Psi}{\longrightarrow}
  N \otimes_A \Gamma
    \overset{\simeq}{\longrightarrow}
  \Gamma \otimes_A N
    \overset{c \otimes_A id}{\longrightarrow}
  \Gamma \otimes_A N
  \,.
$$



=--


+-- {: .num_defn #CotensorProductOfComodules}
###### Definition

Given a [[commutative Hopf algebroid]] $\Gamma$ over $A$, def. \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents},
and given $N_1$ a right $\Gamma$-comodule and $N_2$ a left comodule (def. \ref{CommutativeHopfAlgebroidComodule}), then their **[[cotensor product]]** $N_1 \Box_\Gamma N_2$ is the [[kernel]] of the difference of the two coaction morphisms:

$$
  N_1 \Box_\Gamma N_2
    \;\coloneqq\;
  ker
  \left(
    N_1 \otimes_A N_2
    \overset{\Psi_{N_1}\otimes_{A} id - id \otimes_A \Psi_{N_2} }{\longrightarrow}
    N_1 \otimes_A \Gamma \otimes_A N_2
  \right)
  \,.
$$

If both $N_1$ and $N_2$ are left comodules, then their cotensor product is the cotensor product of $N_2$ with $N_1$ regarded as a right comodule via prop. \ref{LeftComodulesToRightComodules}.

=--

e.g. ([Ravenel 86, def. A1.1.4](#Ravenel86)).


+-- {: .num_example #PrimitiveElementInAComodule}
###### Example

Given a [[commutative Hopf algebroid]] $\Gamma$ over $A$, ([def.](commutative+Hopf+algebroid#CommutativeHopfAlgebroidDefinitionInExplicitComponents)), and given $N$ a left $\Gamma$-comodule ([def.](commutative+Hopf+algebroid#CommutativeHopfAlgebroidComodule)). Regard $A$ itself canonically as a right $\Gamma$-comodule via example \ref{GroundRingIsCanonicalComoduleOverHopfAlgebroid}. Then the cotensor product 

$$
  Prim(N) \coloneqq A \Box_\Gamma N
$$

is called the **[[primitive elements]]** of $N$:

$$
  Prim(N) = \{ n \in N \;\vert\; \Psi_N(n) = 1 \otimes n \}
  \,.
$$

=--


+-- {: .num_prop}
###### Proposition

Given a [[commutative Hopf algebroid]] $\Gamma$ over $A$, def. \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents},
and given $N_1, N_2$ two left $\Gamma$-comodules (def. \ref{CommutativeHopfAlgebroidComodule}), then their [[cotensor product]] (def. \ref{CotensorProductOfComodules}) is commutative, in that there is an [[isomorphism]]

$$
  N_1 \Box N_2 \;\simeq\; N_2 \Box N_1
  \,.
$$

=--

(e.g. [Ravenel 86, prop. A1.1.5](#Ravenel86)) 

+-- {: .num_lemma #ComoduleHomInTermsOfCotensorProduct}
###### Lemma

Given a [[commutative Hopf algebroid]] $\Gamma$ over $A$, def. \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents},
and given $N_1, N_2$ two left $\Gamma$-comodules (def. \ref{CommutativeHopfAlgebroidComodule}), such that $N_1$ is [[projective module|projective]] as an $A$-[[module]], then

1. The morphism

   $$
      Hom_A(N_1, A)
       \overset{f \mapsto (id \otimes_A f) \circ \Psi_{N_1}}{\longrightarrow}
      Hom_A(N_1, \Gamma \otimes_A A)
       \simeq
      Hom_A(N_1, \Gamma)
       \simeq
      Hom_A(N_1, A) \otimes_A \Gamma
   $$
 
   gives $Hom_A(N_1,A)$ the structure of a right $\Gamma$-comodule;

1. The [[cotensor product]] (def. \ref{CotensorProductOfComodules}) with respect to this right comodule structure is isomorphic to the hom of $\Gamma$-comodules:

   $$
     Hom_A(N_1, A) \Box_\Gamma N_2
     \simeq
     Hom_\Gamma(N_1, N_2)
     \,.
   $$

   Hence in particular

   $$
     A \Box_\Gamma N_2 
      \;\simeq\;
     Hom_\Gamma(A,N_2)
   $$

=--

(e.g. [Ravenel 86, lemma A1.1.6](#Ravenel86))

+-- {: .num_remark}
###### Remark

In computing the second page of $E$-[[Adams spectral sequences]], the second statement in lemma \ref{ComoduleHomInTermsOfCotensorProduct} is the key translation that makes the comodule [[Ext]]-groups on the page be equivalent to a [[Cotor]]-groups. The latter lend themselves to computation, for instance via [[Lambda-algebra]] or via the [[May spectral sequence]].

=--




##### The dual $E$-Steenrod algebra
 {#DualESteenrodAlgebra}


Now we identify the [[commutative Hopf algebroids]] (def. \ref{CommutativeHopfAlgebroid}) arising in the $E$-Adams spectral sequence (def. \ref{AdamsEAdamsSpectralSequence}):

+-- {: .num_defn #HopfAlgebroidStructureOnDualEOperations}
###### Definition

Let $(E, \mu, e)$ be a [[homotopy commutative ring spectrum]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyCommutativeRingSpectrum)) which is flat according to def. \ref{FlatE}. 

Then the **dual $E$-[[Steenrod algebra]]** is the [[commutative Hopf algebroid]] $(E_\bullet(E), \pi_\bullet(E))$ (def. \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents}) equipped with the following structure maps

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
  \,,
$$

where the horizontal isomorphisms are form prop. \ref{FlatnessOfEImpliesKeyConsequence}.

Analogously for $X \in Ho(Spectra)$ any spectrum then $E_\bullet(X)$ becomes a [[comodule]] over $(E_\bullet(E), \pi_\bullet(E))$ where the [[coaction]] is induced as on the right of the following diagram

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

([Adams 69, pages 60-66](#Adams69))




+-- {: .num_example}
###### Example

Examples of [[commutative ring spectra]] $E$ for which the dual $E$-[[Steenrod algebra]] $E_\bullet(E)$ over $\pi_\bullet(E)$ of def. \ref{HopfAlgebroidStructureOnDualEOperations} happens to be a [[graded commutative Hopf algebra]] over $\pi_\bullet(E)$ instead of a more general [[graded commutative Hopf algebroid]], according to remark \ref{HopfAlgebrasAsHopfAlgebroids}, includes the case $E = $ [[HA|H]]$\mathbb{F}_p$.

=--

##### The first page via homs of Hopf comodules


The key use of the Hopf coalgebroid structure of prop. \ref{HopfAlgebroidStructureOnDualEOperations} for the present purpose is that it is extra structure inherited by morphisms in $E$-homology from morphisms of spectra.

+-- {: .num_example #SmashingMapsWithEFactorsThroughSteenrodComoduleHomomorphisms}
###### Example

For $Y,N$ any two [[spectra]], the morphism (of $\mathbb{Z}$-[[graded abelian groups]]) given by [[smash product of spectra|smash product]] with $E$

$$
  \pi_\bullet(E \wedge -)
    \;\colon\;
  [Y,N]_\bullet
    \longrightarrow
  Hom^\bullet_{Ab}(E_\bullet(Y), E_\bullet(N))
$$

factors through $E_\bullet(E)$-[[comodule]] [[homomorphisms]] over the dual $E$-[[Steenrod algebra]]:

$$
  \pi_\bullet(E \wedge -)
    \;\colon\;
  [Y,N]_\bullet
    \longrightarrow
  Hom^\bullet_{E_\bullet(E)}(E_\bullet(Y), E_\bullet(N))
  \,.
$$

=--

In order to put all this together, we need to invoke a [[universal coefficient theorem]] in the following form.

+-- {: .num_prop #AdamsUCT}
###### Proposition

If at least one of the following conditions is met

* $Y = \mathbb{S}$ is the [[sphere spectrum]];

* $E$ is among the examples [[sphere spectrum|S]], [[HR]] for $R = \mathbb{F}_p$, [[MO]], [[MU]], [[MSp]], [[KO]], [[KU]], 

then for all $E$-[[module spectra]] $N$ with [[action]] $\rho \colon E\wedge N \to N$
the morphism of $\mathbb{Z}$-[[graded abelian groups]]

$$
  [Y,N]_\bullet 
    \stackrel{\phi \mapsto \rho \circ (id\wedge \phi)}{\longrightarrow}
  Hom_{\pi_\bullet(E)}^\bullet(E_\bullet(Y), \pi_\bullet(N))_\bullet
$$

is an [[isomorphism]].


=--

For $Y = \mathbb{S}$ this is trivial. For general $Y$ and $E$ among the above examples this is the [[universal coefficient theorem]] of ([Adams 74, chapter III, prop. 13.5](#Adams74)), see also ([Schwede 12, chapter II, prop. 6.20](#Schwede12)), and see at _[Kronecker pairing -- Universal coefficient theorem](Kronecker+pairing#UniversalCoefficientTheorem)_.

With this we finally get the following statement, which serves to identity maps of certain spectra with their induced maps on $E$-homology:

+-- {: .num_prop #ComoduleHomForENCohomology}
###### Proposition

If the assumption of prop. \ref{AdamsUCT} hold, then for $X,N$ any two [[spectra]], the morphism of $\mathbb{Z}$-[[graded abelian groups]] from example \ref{SmashingMapsWithEFactorsThroughSteenrodComoduleHomomorphisms} of the form

$$
 \pi_\bullet(E\wedge (-))
   \;\colon\;
 [Y, E\wedge N]_\bullet 
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
    [Y, E \wedge N]_\bullet
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

1. the left vertical morphism is an isomorphism by prop. \ref{AdamsUCT}. 

Therefore also the top morphism is an iso.

=--

In conclusion:

+-- {: .num_theorem #ComoduleHomsInE1PageOfEAdamsSpectralSequence}
###### Theorem

Let $X, Y$ be [[spectra]], $E$ a [[homotopy commutative ring spectrum]] 
which is flat (def. \ref{FlatE}). If the assumption of prop. \ref{AdamsUCT} holds then the first page of the $E$-Adams spectral sequence, def. \ref{AdamsEAdamsSpectralSequence}, for $[Y,X]_\bullet$ is isomorphic to the following chain complex of graded homs of [[comodules]] (def. \ref{CommutativeHopfAlgebroidComodule}) over the dual $E$-[[Steenrod algebra]] $(E_\bullet(E), \pi_\bullet(E))$ (prop. \ref{HopfAlgebroidStructureOnDualEOperations}):

$$
  0 
    \to 
  Hom_{E_\bullet(E)}^\bullet(E_\bullet(X),E_\bullet(A_0))
    \stackrel{d_1}{\longrightarrow}
  Hom_{E_\bullet(E)}^\bullet(
     E_\bullet(X),
     E_\bullet(A_1)
  )
    \stackrel{d_1}{\longrightarrow}
  Hom_{E_\bullet(E)}^\bullet(
     E_\bullet(X),
     E_\bullet(A_2)
   )
    \stackrel{d_1}{\longrightarrow}
   \cdots
  \,.
$$

=--

([Adams 74, theorem 15.1 page 323](#Adams74))

+-- {: .proof}
###### Proof

This is prop. \ref{ComoduleHomForENCohomology} applied to def. \ref{AdamsEAdamsSpectralSequence}.

=--

In order to interpret prop. \ref{ComoduleHomsInE1PageOfEAdamsSpectralSequence}, notice that it gives the comodule homs into a resolution of $E_\bullet(Y)$

+-- {: .num_lemma #ResolutionEWp}
###### Lemma

Given an $E$-Adams spectral sequence $(E^{s,t}_r(X,Y),d_r)$ as in def. \ref{AdamsEAdamsSpectralSequence}, then the sequences of morphisms

$$
  0
    \to
  E_\bullet(Y_p)
    \overset{E_\bullet(g_p)}{\longrightarrow}
  E_\bullet(A_p)
    \overset{E_\bullet(h_p)}{\longrightarrow}
  E_{\bullet-1}(Y_{p+1})
   \to
  0
$$

are [[short exact sequences|short exact]], hence their [[splicing of short exact sequences]]

$$
  \array{
    0 
      &\to& 
    E_\bullet(Y)
     && \overset{E_\bullet(f_0)}{\longrightarrow} &&
    E_\bullet(A_0)
     && \overset{\partial}{\longrightarrow} &&
    E_{\bullet-1}(A_1)
     && \overset{\partial}{\longrightarrow} &&
    E_{\bullet-2}(A_2)
     && \longrightarrow &&
    \cdots
    \\
    &&
    &&
    &&
    & {}_{\mathllap{E_\bullet(h_0)}}\searrow && \nearrow_{\mathrlap{E_\bullet(g_1)}}
    &&
    {}_{\mathllap{E_\bullet(h_1)}}\searrow 
    && \nearrow_{\mathrlap{E_\bullet(g_2)}}
    \\
    && 
    &&
    &&
    &&
    E_{\bullet-1}(Y_1) 
    &&
    &&
    E_{\bullet-2}(Y_2)
  }
$$

is a [[long exact sequence]], exhibiting the graded [[chain complex]] $(E_\bullet(A_\bullet), \partial)$ as a resolution of $E_\bullet(Y)$.

=--

([Adams 74, theorem 15.1, page 322](#Adams74))

+-- {: .proof}
###### Proof

Consider the image of the defining [[homotopy cofiber sequence]]

$$
  Y_p 
    \overset{g_p}{\longrightarrow}
  E \wedge Y_p
    \overset{h_p}{\longrightarrow}
  \Sigma Y_{p+1}
$$

under the functor $E \wedge (-)$. This is itself a homotopy cofiber sequence of the form 

$$
  E \wedge Y_p
    \overset{E \wedge g_p}{\longrightarrow}
  E \wedge E \wedge Y_p
    \overset{E \wedge h_p}{\longrightarrow}
  \Sigma E \wedge Y_{p + 1}
$$

(due to the [[tensor triangulated category|tensor triangulated]] structure of the [[stable homotopy category]], [prop.](Introduction+to+Stable+homotopy+theory+--+1-2#TensorTriangulatedStructureOnStableHomotopyCategory)).


Applying the [[stable homotopy groups]] functor $\pi_\bullet(-) \simeq [\mathbb{S},-]_\bullet$ ([lemma](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyGrouspAsHomsOutOfSphereSpectrum)) to this yields a [[long exact sequence]] ([prop.](Introduction+to+Stable+homotopy+theory+--+1-1#LongExactSequenceOfStableHomotopyGroups))

$$
  \cdots
   \longrightarrow
  E_{\bullet}(Y_{p+1})
    \overset{ E_\bullet(f_p) }{\longrightarrow}
  E_\bullet(Y_p)
    \overset{ E_\bullet(g_p) }{\longrightarrow}
  E_\bullet(W_p)
    \overset{ E_\bullet(h_p) }{\longrightarrow}
  E_{\bullet-1}(Y_{p+1})
    \overset{ E_{\bullet-1}(f_p) }{\longrightarrow}
  E_{\bullet-1}(Y_{p})
    \overset{ E_{\bullet-1}(g_p) }{\longrightarrow}
  E_{\bullet-1}(A_p)
   \longrightarrow
  \cdots
  \,.
$$

But in fact this [[split exact sequence|splits]]: by [[unitality]] of $(E,\mu,e)$, the product operation $\mu$ on the [[homotopy commutative ring spectrum]] $E$ is a [[left inverse]] to $g_p$ in that

$$
  id
  \;\colon\;
  E \wedge Y_p
    \overset{E \wedge g_p}{\longrightarrow}
  E \wedge E \wedge Y_p
    \overset{\mu \wedge id}{\longrightarrow}
  E \wedge Y_p
  \,.
$$

Therefore $E_\bullet(g_p)$ is a [[monomorphism]], hence its [[kernel]] is trivial, and so by exactness $E_\bullet(f_p) = 0$. This means that the above long exact sequence collapses to [[short exact sequences]].

=--

Hence the next step is to identify the chain homology of this $d_1$ with the comodule [[Ext]]-groups.




#### The second page
 {#TheE2TermOfTheEAdamsSpectralSequence}


+-- {: .num_theorem #SecondPageOfEAdamsSpectralSequence}
###### Theorem

If 

1. $E$ is flat, def. \ref{FlatE}, and satisfies the conditions of prop. \ref{AdamsUCT}, 

2. $E_\bullet(Y)$ a [[projective module]] over $\pi_\bullet(E)$, 

then the entries of the second page
of the $E$-Adams spectral sequence, def. \ref{AdamsEAdamsSpectralSequence}, for $[X,Y]$ are the [[Ext]]-groups of [[commutative Hopf algebroid]]-[[comodules]] for the [[commutative Hopf algebroid]] structure on $E$-operations $E_\bullet(E)$ from prop.  \ref{HopfAlgebroidStructureOnDualEOperations}:


$$
  \mathcal{E}^{s,t}_2
  \simeq
  Ext^{s,t}_{E_\bullet(E)}(E_\bullet(X), E_\bullet(Y))
  \,.
$$

In the special case that $X = \mathbb{S}$, then (by prop. \ref{ComoduleHomInTermsOfCotensorProduct}) these are equivalently [[Cotor]]-groups

$$
  \mathcal{E}^{s,t}_2
    \simeq
  Cotor^{s,t}_{E_\bullet(E)}(\pi_\bullet(E), E_\bullet(Y))
  \,.
$$

=--

+-- {: .proof}
###### Proof

The first page is given by prop. \ref{ComoduleHomsInE1PageOfEAdamsSpectralSequence}, and so by the standard theory of [[derived functors in homological algebra]] (see the section _[Via acyclic resolutions](derived+functor+in+homological+algebra#ViaAcyclicResolutions)_), it is now sufficient to see that:

1. the category $E_\bullet(E) CoMod$ is an [[abelian category]];

1. the graded chain complex of prop. \ref{ComoduleHomsInE1PageOfEAdamsSpectralSequence} is the image under the [[hom-functor]] $F \coloneqq Hom_{E_\bullet(E)}(E_\bullet(Y),-)$ of an $F$-[[acyclic resolution]] of $E_\bullet(X)$.

We show that $E_\bullet(E) CoMod$ is abelian as prop. \ref{CategoryOfHopfComodulesIsAbelianIfHopfAlgebroidIsFlat} below.

By lemma \ref{ResolutionEWp} we already know that $E_\bullet(A_\bullet)$ is a resolution of $E_\bullet(Y)$. By prop. \ref{FlatnessOfEImpliesKeyConsequence} it is a resolution by cofree comodules (def. \ref{CoFreeComodules}). That these are $F$-acyclic we show as prop. \ref{CoFreeHopfComodulesAreHomNAcyclicForProjectiveN} below.

=--

([Adams 74, theorem 15.1, page 323](#Adams74))

##### Homological co-algebra

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

+-- {: .num_prop #IfCounitOfHopfAlgebroidIsFlatThenCofreeModulesAreInjective}
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
   \underoverset
     {\underset{forget}{\longrightarrow}}
     {\overset{co-free}{\longleftarrow}}
     {\bot}
  A Mod
 \,.
$$

Observe that the [[left adjoint]] is a [[faithful functor]] (being a [[forgetful functor]]) and that, by the proof of prop. \ref{CategoryOfHopfComodulesIsAbelianIfHopfAlgebroidIsFlat}, it is an [[exact functor]]. With this a standard lemma applies ([here](injective+object#TransferOfEnoughInjectivesAlongAdjunctions)) which says that

1. with $I \in A Mod$ an [[injective module]], then the co-free comodule $\Gamma \otimes_A I$ is an [[injective object]] in $\Gamma CoMod$;

1. for $N \in \Gamma CoMod$ any object, and for $i \colon U(N) \hookrightarrow I$ a monomorphism of $A$-modules into an injective $A$-module, then the [[adjunct]] $\tilde i \colon N \hookrightarrow \Gamma\otimes_A I$ is a monomorphism in $\Gamma CoMod$ (and into an injective comodule).

=--


+-- {: .num_prop #CoFreeHopfComodulesAreHomNAcyclicForProjectiveN}
###### Proposition

Let $\Gamma$ be a [[commutative Hopf algebroid]] over $A$, def. \ref{CommutativeHopfAlgebroid}, \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents}, such that $\eta_L, \eta_R \colon A \longrightarrow \Gamma$ is a [[flat morphism]], 
Let $N \in \Gamma CoMod$ be a Hopf [[comodule]], def. \ref{CommutativeHopfAlgebroidComodule}, such that the underlying $A$-module is a [[projective module]] (a [[projective object]] in $A$[[Mod]]). 

Then  (assuming the [[axiom of choice]]) every co-free comodule, prop. \ref{CoFreeComodules}, is an $F$-[[acyclic object]] for $F$ the [[hom functor]] $Hom_{\Gamma CoMod}(N,-)$.

=--

+-- {: .proof}
###### Proof

We need to show that the [[derived functors in homological algebra|derived functors]] $R^{\bullet} Hom_{\Gamma}(N,-)$ vanish in positive degree on all co-free comodules, hence on $\Gamma \otimes_A K$, for $K \in A Mod$. 

To that end, let $I^\bullet$ be an [[injective resolution]] of $K$ in $A Mod$. By prop. \ref{IfCounitOfHopfAlgebroidIsFlatThenCofreeModulesAreInjective} then $\Gamma \otimes_A I^\bullet$ is a sequence of [[injective objects]] in $\Gamma CoMod$ and by the assumption that $\Gamma$ is flat over $A$ it is an [[injective resolution]] of $\Gamma \otimes_A K$ in $\Gamma CoMod$. Therefore the derived functor in question is given by

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

With prop. \ref{CoFreeHopfComodulesAreHomNAcyclicForProjectiveN} the proof of theorem \ref{SecondPageOfEAdamsSpectralSequence} is completed.


#### Convergence 
 {#Convergence}

##### $E$-Nilpotent completion


For $X$ a spectrum and $E$ a [[ring spectrum]], consider the inverse sequence 

$$
  \overline{E}^{\wedge^\bullet} \wedge X
  =
  \left( X \leftarrow \overline{E}\wedge X \leftarrow \overline{E} \wedge \overline{E} \wedge X \leftarrow \cdots
  \right)
$$

associated to the normalized $E$-Adams resolution of $X$, as in example \ref{NormalizedEResolutionAssociatedSequence}. 

+-- {: .num_defn #ENilpotentCompletion}
###### Definition

For $n \in \mathbb{N}$, write

$$
  \overline{E}_n 
   \coloneqq
  hocof( \overline{E}^n \overset{i^n}{\longrightarrow} \mathbb{S})
  \,.
$$

Here $\overline{E}_0 \simeq 0$.

The **[[E-nilpotent completion]]** $X^\wedge E$ of $X$ is the [[homotopy limit]] 

$$
  X^\wedge_E
    \coloneqq
  \underset{\longleftarrow}{\lim}
  \left(
    \cdots
     \longrightarrow
    \overline{E}_2 \wedge X
      \longrightarrow
    \overline{E}_1 \wedge X
      \longrightarrow
    \overline{E}_0 \wedge X
  \right)
$$

or rather the canonical morphism

$$
  X \longrightarrow X^\wedge_E
  \,.
$$


=---

([Bousfield 79, top, middle and bottom of page 272](#Bousfield79), recalled as [Ravenel 84, theorem 1.13](#Ravenel84))


([Ravenel 84, example 1.16](#Ravenel84)

+-- {: .num_defn #SheavesOnCartSp}
###### Definition

In ([Bousfield 79](#Bousfield79)) the $E$-nilpotent completion of $X$ (def. \ref{ENilpotentCompletion}) this is denoted "$E^\wedge X$". The notation we use here is more common among modern authors.

=--

+-- {: .num_remark #CanonicalMapFromELocalizationToTotalization}
###### Remark

The nilpotent completion $X^\wedge_E$ is $E$-local.
This induces a universal morphism

$$
  L_E X 
    \overset{}{\longrightarrow} 
  X^\wedge_E
$$

from the $E$-[[Bousfield localization of spectra]] of $X$ into the $E$-nilmpotent completion

=--

([Bousfield 79, top of page 273](#Bousfield79))

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

Let $E$ be a [[connective spectrum|connective]] [[ring spectrum]] such that the core of $\pi_0(E)$, def. \ref{CoreOfARing}, is either of

* the [[localization of a ring|localization]] of the [[integers]] at a set $J$ of [[primes]], $c \pi_0(E) \simeq \mathbb{Z}[J^{-1}]$;

* $\mathbb{Z}/n\mathbb{Z}$ for $n \geq 2$.

Then the map in remark \ref{CanonicalMapFromELocalizationToTotalization} is an equivalence

$$
  L_E X 
    \stackrel{\simeq}{\longrightarrow} 
  X^\wedge_E
  \,.
$$

=--

([Bousfield 79, theorem 6.5, theorem 6.6](#Bousfield79)).


+-- {: .num_examples #ExamplesOfEnilpotentLocalizations}
###### Example

* $E = H \mathbb{F}_p$ the [[Eilenberg-MacLane spectrum]] of a [[prime field]]. For $X$ a [[connective spectrum]], its $H \mathbb{F}_p$-nilpotent completion is its [[p-completion]]

  $$
    X^\wedge_{(H\mathbb{F}_p)}
    \simeq
    X^{\hat{}}_p 
    \coloneqq
    \underset{\longleftarrow}{\lim}_{n \in \mathbb{N}}
    X  \wedge M(\mathbb{Z}/p^n)
  $$

  (where $M A$ denotes the [[Moore spectrum]] of the [[abelian group]] $A$).

* $E = $ [[MU]]. Every spectrum is alreay $MU$-nilpotently complete 

  $$
    MU\hat{}X \simeq X
    \,.
  $$

* $E = $ [[BP]] at prime $p$. For every spectrum $X$ its $BP$-nilpotent completion is its [[p-localization]] 

  $$
    BP\hat{}X \simeq X_{(p)} \coloneqq X \wedge M \mathbb{Z}_{(p)}
  $$

  (where $\mathbb{Z}_{(p)}\subset \mathbb{Q}$ is the result of inverting all primes different from $p$).

=--


For more discussion of [[E-infinity geometry|E-infinity]] (derived) [[formal completions]] via totalizations of [[Amitsur complexes]], see ([Carlsson 07](completion+of+a+module#Carlsson07)).

+-- {: .num_theorem #ConvergenceOfEAdamsSpectralSequenceToECompletion}
###### Theorem

For $X$ a [[spectrum]] and $E$ a [[ring spectrum]], consider [[generalized the|the]] $E$-Adams spectral sequence $\{\mathcal{E}_r^{\bullet,\bullet}, d_r\}$ of $X$ (def. \ref{EAdamsSpectralSequence}, prop. \ref{UniquenessOfEAdamsSpectralSequence}, prop. \ref{TowerSpectralSequencesOfAdamsTowerAndInverseSequenceCoincide}). If for each $s,t$ there is $r$ such that

$$
  \mathcal{E}_r^{s,t} \simeq \mathcal{E}_\infty^{s,t}
$$

then the $E$-Adams spectral sequence converges strongly ([def.](spectral+sequence#Convergence)) to the [[stable homotopy groups]] of the [[E-nilpotent completion]] of $X$ (def. \ref{ENilpotentCompletion}):

$$
  \mathcal{E}_1^{s,t} \;\Rightarrow\;  \pi_\bullet(E\hat{}X)
  \,.
$$

=--

([Bousfield 79](#Bousfield79), recalled as [Ravenel 84, theorem 1.15](#Ravenel84))


#### Examples

+-- {: .num_example}
###### Examples

* For $X = \mathbb{S}$ and $E = H\mathbb{F}_p$, then theorem \ref{SecondPageOfEAdamsSpectralSequence} and theorem \ref{ConvergenceOfEAdamsSpectralSequenceToECompletion} with example \ref{ExamplesOfEnilpotentLocalizations} gives a spectral sequence

  $$
    Ext_{\mathcal{A}^\ast_p}(\mathbb{F}_p, \mathbb{F}_p)
    \;\Rightarrow\;
    \pi_\bullet(\mathbb{S})\otimes Z^\wedge_p
    \,.
  $$

  This is the _[[classical Adams spectral sequence]]_.

* For $X = \mathbb{S}$ and $E = $ [[MU]], then theorem \ref{SecondPageOfEAdamsSpectralSequence} and theorem \ref{ConvergenceOfEAdamsSpectralSequenceToECompletion} with example \ref{ExamplesOfEnilpotentLocalizations} gives a spectral sequence

  $$
    Ext_{MU_\ast(MU)}(MU_\ast, MU_\ast)
    \;\Rightarrow\;
    \pi_\bullet(\mathbb{S})
    \,.
  $$

  This is the _[[Adams-Novikov spectral sequence]]_.


=--


### $E$-Adams resolutions

A streamlined discussion of $E$-[[Adams resolutions]] in close analogy to [[injective resolutions]] in [[homological algebra]] was given in ([Miller 81](#Miller81)), advertized in ([Hopkins 99](#Hopkins99)) and worked out in more detail in ([Aramian](#Aramian)).


Notice that the standard concept of [[exact sequences]] and [[injective objects]] makes sense in [[abelian categories]], but not in the [[stable homotopy category]] of [[spectra]], as the latter is only an [[additive category]]. Of course this is because the [[stable homotopy theory|stable homotopy theoretic]] analog of what are [[exact sequences]] in abelian categories are [[homotopy fiber sequences]] of spectra. But for computational purposes it turns out useful to consider a blend between these two concepts (due to [Miller 81](#Miller81)), where a sequence of spectra $X_\bullet$ is regarded as exact if the [[homotopical functor]] to the abelian category of [[abelian groups]] that it [[representable functor|represents]] takes values in [[exact sequences]]. With respect to this hybrid concept, $E$-Adams resolutions in the [[stable homotopy category]] are the direct analog of [[injective resolutions]] in an [[abelian category]].



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

By the suspension/looping [[adjunction]]-[[isomorphism]] $[\Sigma A_\bullet, -]\simeq [A_\bullet, \Omega(-)]$ ([prop.](Introduction+to+Stable+homotopy+theory+--+P#AlternativeLoopingAndSuspensionIsQuillenEquivalenceOnStableModelStructure)) and so the statement follows from the assumption that $A_\bullet$ is long exact.

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

Consecutive morphisms in an $E$-exact sequence according to def. \ref{ExactSequences} in general need not compose up to homotopy, to the [[zero morphism]]. But this does become true (lemma \ref{ConsecutiveMapsInEAdamsResolutionComposeToZero} below) for sequences of $E$-injective objects, defined below in def. \ref{EInjective}. 

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

+-- {: .num_lemma #ConsecutiveMapsInEAdamsResolutionComposeToZero}
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

There are two $E$-Adams resolutions that we will consider. Following ([Hopkins 99](#Hopkins99)) we call them the "normalized resolution" and the "standard resolution". But beware that what all the traditional literature ([Adams 74](#Adams74), [Bousfield 79](#Bousfield79), [Ravenel 86](#Ravenel86), ...) considers (and somewhat implicitly) is the "normalized" resolution, not the standard resolution. The standard resolution is standard only from the more recent perspective of [[E-∞ geometry]]: it is the [[Amitsur complex]] of the $\mathbb{S}$-algebra $E$, exhibiting the formal dual of the [[Cech nerve]] of $Spec(E) \to Spec(\mathbb{S})$.

+-- {: .num_example #NormalizedEResolution}
###### Example
**(normalized $E$-Adams resolution)**

Let $\overline{E}$ denote the [[homotopy fiber]] of the unit of the ring spectrum $E$, fitting into a [[homotopy fiber sequence]]

$$
  \overline{E}
    \overset{i}{\longrightarrow}
  \mathbb{S}
    \overset{e}{\longrightarrow}
  E
    \longrightarrow  
  \Sigma \overline{E}
  \,.
$$

For $X$ a spectrum, its **normalized $E$-Adams resolution** is the top row of

$$
  \array{
    X 
      &\overset{(e,id)}{\longrightarrow}& 
    E \wedge X 
      && \longrightarrow  && 
    E \wedge (\Sigma \overline{E}) \wedge X
      && \longrightarrow &&
    E \wedge (\Sigma \overline{E}) \wedge (\Sigma \overline{E}) \wedge X
      && \longrightarrow &&
    \cdots
    \\
    && & \searrow && \nearrow_{\mathrlap{(e,id)}}
    &&    \searrow && \nearrow_{\mathrlap{(e,id)}}
    \\
    && && (\Sigma \overline{E})\wedge X
    &&&&  (\Sigma \overline{E}) \wedge \overline{E} \wedge X
  }
$$

=---

(e.g. [Hopkins 99, corollary 5.3](#Hopkins99)).


+-- {: .num_remark}
###### Remark

The notation for $\overline{E}$ in def. \ref{NormalizedEResolution} follows ([Bousfield 79, section 5](#Bousfield79)). In ([Hopkins 99](#Hopkins99)) the same notation is used not for the homotopy fiber but for the homotopy cofiber. While our notation makes plenty of "$\Sigma$"s appear in the above resolution, the advantage is that in the induced inverse sequence of a normalized resolution below in example \ref{NormalizedEResolutionAssociatedSequence} these all drop out and we are left with the original form of the expressions as considered by ([Adams 74](#Adams74)) and followed in most of the literature. 

=--


+-- {: .num_example #StandardEResolution}
###### Example
**(standard $E$-Adams resolution)**

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

#### $E$-Adams towers

+-- {: .num_defn #EAdamsTower}
###### Definition

An _$E$-Adams tower_ of a spectrum $X$ is a [[commuting diagram]] in the [[stable homotopy category]] of the form

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
     0 \to X \stackrel{i_0}{\to} I_0 \stackrel{i_1}{\to} I_1 \stackrel{}{\to} \cdots
     \,.
   $$

Call this the **associated $E$-Adams resolution** of the $E$-Adams tower.

=--

([Hopkins 99, def. 4.10](#Hopkins99))

The following is the main statement of the above little theory of $E$-injective spectra.

+-- {: .num_prop #RelationBetweenEAdamsTowersAndEAdamsResolutions}
###### Proposition

Every $E$-Adams resolution $X \to I_\bullet$ (def. \ref{EAdamsResolution}) induces an $E$-Adams tower, def. \ref{EAdamsTower} of which it is the associated $E$-Adams resolution.

=--

+-- {: .proof}
###### Proof idea

Given an $E$-Adams resolution

$$
  X \overset{i_0}{\longrightarrow} I_0 \overset{i_1}{\longrightarrow} I_1 \longrightarrow \cdots
$$

consider the induced diagram

$$
  \array{
    && && C_1 && && && && C_3
    \\
    && & {}^{\mathllap{\rho_1}}\nearrow && \searrow^{\mathrlap{\sigma_1}} 
    && && && {}^{\mathllap{\rho_3}}\nearrow
    \\
    && 
    I_0 
    && 
     \underset{i_1}{\longrightarrow} 
    &&
    I_1 
    &&
      \overset{i_2}{\longrightarrow}
    &&
    I_2
    &&
      \underset{i_3}{\longrightarrow}
    & 
    \cdots
    \\
    & {}^{\mathllap{\sigma_0 \coloneqq i_0}}\nearrow
    && && && {}_{\mathllap{\rho_2}}\searrow
    && \nearrow_{\mathrlap{\sigma_2}}
    \\
    C_0 \coloneqq X && && && && C_2
  }
$$

constructed [[induction|inductively]] as follows:

To start with, $\rho_1$ is the [[homotopy cofiber]] of $i_0$, and $\sigma_1$ is the morphism universally induced from this by the fact that $i_1 \circ i_0 \simeq 0$, by lemma \ref{ConsecutiveMapsInEAdamsResolutionComposeToZero}. Observe that  $\sigma_1$ is an $E$-monomorphism and $\rho_1$ is an $E$-epimorphism in the sense of def. \ref{ExactSequences}.

Then assume that an $E$-epi/mono factorization 

$$
  i_n \colon I_{n_1} \overset{\rho_n}{\longrightarrow} C_n \overset{\sigma_n}{\to} I_n
$$ 

has been constructed. Let now $\rho_{n+1}$ be its homotopy cofiber.  Since $\rho_{n}$ is $E$-epi, the equivalence $0 \simeq i_{n+1} \circ i_n = i_{n+1}\circ \sigma_n \circ \rho_n$ from lemma \ref{ConsecutiveMapsInEAdamsResolutionComposeToZero} implies that already $i_{n+1} \circ \sigma_n \simeq 0$. With this, the universal property of the homotopy cofiber induces a morphism $\sigma_{n+1}\colon C_{n+1}\to I_{n+1}$. As before, $\rho_{n+1}$ is $E$-epi and $\sigma_{n+1}$ is $E$-mono, and so the induction proceeds.

Using this, we now construct an $E$-Adams tower as follows (...).

=--

There is another tower associated with an $E$-Adams resolutions:

+-- {: .num_defn #AssociatedInverseSequence}
###### Definition

Given an $E$-Adams resolutions $X \to I_\bullet$ (def. \ref{EAdamsResolution}), its **associated inverse sequence** is 

$$
  \array{
    X 
      = 
    C_0
      &\stackrel{\gamma_0}{\longleftarrow}&
    \Sigma^{-1} C_1 
      &\stackrel{\gamma_1}{\longleftarrow}&
    \Sigma^{-2} C_2 
      &\longleftarrow&
    \cdots
    \\
    \downarrow && \downarrow && \downarrow
    \\
    I_0 && \Sigma^{-1} I_1 && ^\Sigma^{-2} I_2
  }
$$

with the $C_i$ as in the proof of prop. \ref{RelationBetweenEAdamsTowersAndEAdamsResolutions} and 
$\gamma_n \coloneqq \Sigma^{-} hofib(\sigma_n)$.

=--

+-- {: .num_example #NormalizedEResolutionAssociatedSequence}
###### Example

Let $X \to I_\bullet = (E \wedge (\Sigma \overline{E})^{\wedge^{\bullet-1}}\wedge E)$ be a _normalized $E$-Adams resolution_ according to example \ref{NormalizedEResolution}. Then its associated inverse sequence according to def. \ref{AssociatedInverseSequence} is the sequence from def. \ref{EAdamsSpectralSequence}


$$
  \array{
    X 
      &\stackrel{\gamma_0}{\longleftarrow}&
    \overline{E} \wedge X
      &\stackrel{\gamma_1}{\longleftarrow}&
    \overline{E} \wedge \overline{E} \wedge X
      &\longleftarrow&
    \cdots
    \\
    \downarrow && \downarrow && \downarrow
    \\
    E \wedge X 
      && 
    \Sigma^{-1}(E \wedge (\Sigma \overline{E}) \wedge X)
      && 
    \Sigma^{-2}(E \wedge (\Sigma\overline{E}) \wedge (\Sigma \overline{E}) \wedge X
    \\
      && \simeq && \simeq 
    \\
    &&
    E \wedge \overline{E} \wedge X
      && 
    E \wedge \overline{E} \wedge \overline{E} \wedge X
  }
$$

This is the tower of spectra considered in the original texts ([Adams 74, p. 318](#Adams74)) and ([Bousfield 79, p. 271](#Bousfield79)).

=--


+-- {: .num_remark}
###### Remark


In ([Ravenel 84, p. 356](#Ravenel84)) it is the associated inverse sequence as in example \ref{NormalizedEResolutionAssociatedSequence} that is called the "Adams tower", while in ([Ravenel 86, def. 2.21](#Ravenel86)) this is called an "$E$-Adams resolution". We instead follow ([Hopkins 99](#Hopkins99)) in using "$E$-Adams resolution" for "$E$-injective resolution" as in def. \ref{EAdamsResolution}, "$E$-Adams tower" for def. \ref{EAdamsTower} and follow ([Aramian](#Aramian)) in saying "associated inverse sequence" for the above.

=--


#### $E$-Adams spectral sequences


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
    && [Y,X_1] &\stackrel{[Y,\kappa_1]}{\longrightarrow}& [Y,\Omega I_2]
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

Given two $E$-Adams towers, def. \ref{EAdamsTower}, for some $X$, then the corresponding two $E$-Adams spectral sequences, def. \ref{EAdamsSpectralSequence}, are [[isomorphism|isomorphic]] from the $\mathcal{E}_2$-page on.

=--

+-- {: .num_prop #TowerSpectralSequencesOfAdamsTowerAndInverseSequenceCoincide}
###### Proposition

Given an $E$-Adams resolution (def. \ref{EAdamsResolution}), there is an [[isomorphism]] of spectral sequences between 

1. the [[tower spectral sequence]] of its associated $E$-Adams tower (def. \ref{EAdamsTower}), i.e. the spectral sequence of def. \ref{EAdamsSpectralSequence};

1. the [[tower spectral sequence]] of its associated inverse sequence (def. \ref{AssociatedInverseSequence}).

=--

+-- {: .num_remark}
###### Remark

Hence both of these construction are to be called the $E$-Adams spectral sequence. It is in fact the second construction -- for the case of the normalized resolution as in example \ref{NormalizedEResolutionAssociatedSequence} -- that is considered in the original sources ([Adams 74, p. 318](#Adams74), [Bousfield 79, p. 271](#Bousfield79)). 

=--



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
$E_\bullet(E) \coloneqq \pi_\bullet(E \wedge_S E)$ (the dual $E$-[[Steenrod operations]] spring) is such that as a [[module]] over $E_\bullet \coloneqq \pi_\bullet(E)$ it is a [[flat module]], then there is a [[natural equivalence]]

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

* [[equivariant Adams spectral sequence]]

[[!include Lurie spectral sequences -- table]]


## References


### General

The original sources are

* {#Adams58} [[Frank Adams]], _On the structure and applications of the Steenrod algebra_, Comm. Math. Helv. 32 (1958), 180&#8211;214.
 
* {#Novikov67} [[Sergei Novikov]], _The methods of algebraic topology from the viewpoint of cobordism theories_, Izv. Akad. Nauk. SSSR. Ser. Mat. 31 (1967), 855&#8211;951 (Russian). ([[Novikov67.pdf:file]])

* {#Adams74} [[John Frank Adams]],  _[[Stable homotopy and generalized homology]]_, Chicago Lectures in mathematics, 1974

based in parts on 

* {#Adams69} [[John Frank Adams]], _Lectures on generalised cohomology_, in 
[[Peter Hilton]] (ed.) _Category Theory, Homology Theory and Their Applications III_, volume 99 of Lecture Notes in Mathematics (1969), Springer-Verlag Berlin-Heidelberg-New York. 

 
Convergence was notably discussed in

* {#Bousfield79} [[Aldridge Bousfield]], _The localization of spectra with respect to homology_, Topology 18 (1979), no. 4, 257--281. ([pdf](http://www.uio.no/studier/emner/matnat/math/MAT9580/v12/undervisningsmateriale/bousfield-topology-1979.pdf))

* {#Ravenel84} [[Douglas Ravenel]], _Localization with respect to certain periodic homology theories_, American Journal of Mathematics, Vol. 106, No. 2, (Apr., 1984), pp. 351-414 ([pdf](https://www.math.rochester.edu/people/faculty/doug/mypapers/loc.pdf))

The [[spectrum]]-level discussion of the ASS goes back to around

* R. M. F. Moss, _On the composition pairing of Adams spectral sequences_, Proceedings of the London Mathematical Society 3.1 (1968): 179-192.

A streamlined presentation of this which is close in spirit to constructions in [[homological algebra]] was given in

* {#Miller81} [[Haynes Miller]], _On relations between Adams spectral sequences, with an application to the stable homotopy of a Moore space_, J. Pure Appl. Algebra 20 (1981) ([pdf](http://math.mit.edu/~hrm/papers/miller-relations-between-adams-spectral-sequences.pdf))

further highlighted in 

* {#Hopkins99} [[Mike Hopkins]], section 5 of _[[Complex oriented cohomology theories and the language of stacks]]_, course notes 1999 ([pdf](https://www.math.rochester.edu/people/faculty/doug/otherpapers/coctalos.pdf))

and worked out in some more detail in

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