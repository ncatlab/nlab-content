
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

For a detailed introduction see at _[[Introduction to the Adams Spectral Sequence]]_.

Working with the Adams spectral sequence tends to be fairly involved, as is clear from the subtlety of the results it computes (notably [[stable homotopy groups of spheres]]) and as witnessed by the fact that one uses further [[spectral sequences]] just to compute the low pages of the Adams spectral sequence, e.g. the [[May spectral sequence]] and the  [[chromatic spectral sequence]]. 

A clear conceptual picture in [[higher algebra]]  of what happens in the Adams spectral sequence ([Lurie 10](#Lurie10)) has emerged via the re-formulation in ([Miller 81](#Miller81), [Hopkins 99](#Hopkins99)). Survey of this perspective includes ([Wilson 13](#Wilson13)). 

Here one observes that for $E$ a [[ring spectrum]], hence an [[E-∞ ring]], the [[totalization]] of its [[Amitsur complex]] [[cosimplicial object|cosimplicial]] spectrum is really the algebraic dual incarnation of the [[1-image]] factorization of the terminal morphism

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

1. [Via the canonical resolution](#CanonicalResolution)

1. [Via injective resolutions](#ViaInjectiveResolutions)

1. [As derived descent in higher algebra](#DefinitionInHigherAlgebra)


### The $E$-Adams spectral sequence
 {#CanonicalResolution}

We here discuss Adams spectral sequences for computation of $E$-[[Bousfield localization of spectra|localization]] of [[mapping spectra]] $[Y,X]$ for $E$ a [[commutative ring spectrum]] which is flat in a certain sense (def. \ref{FlatE} below), via the "canonical" $E$-Adams resolution introduced in ([Adams 74, theorem 15.1](#Adams74)). There are other resolutions which lead to the same spectral sequence, this we discuss below in the section on [E-Injective resolutions](#ViaInjectiveResolutions).

The _[[classical Adams spectral sequence]]_ is the special case of this general concept of $E$-Adams spectral sequences given by setting $Y = X = \mathbb{S}$ the [[sphere spectrum]] and $E = $ [[HA|H]]$\mathbb{F}_p$ the [[Eilenberg-MacLane spectrum]] of a [[prime field]]. This is discussed [below](#ClassicalCase).

The _[[Adams-Novikov spectral sequence]]_ is the special case given by setting $Y = X = \mathbb{S}$ and $E = $ [[MU]], discussed [below](#TheAdamsNovikovSpectralSequence).

#### The spectral sequence

##### Filtered spectra
 {#SpectralSequenceOfAFilteredSpectrum}

We introduce the types of [[spectral sequences]] of which the $E$-Adams spectral sequences (def. \ref{AdamsEAdamsSpectralSequence} below) are an example.

+-- {: .num_defn #FilteredSpectrum}
###### Definition

A **[[filtered spectrum]]** is a [[spectrum]] $Y \in Ho(Spectra)$ equipped with a sequence $Y_\bullet \colon (\mathbb{N}, \gt) \longrightarrow Ho(Spectra)$ in the [[stable homotopy category]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#GradedAbelianGroupStructureOnHomsInTheHomotopyCategory)) of the form

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
    \stackrel{ [X,h_k]_{\bullet+1} }{\longrightarrow}
  [X,Y_{k+1}]_{\bullet} 
    \stackrel{[X,f_k]_\bullet}{\longrightarrow}
  [X,Y_k]_\bullet
    \stackrel{[X,g_k]_\bullet}{\longrightarrow}
  [X,A_k]_\bullet
   \stackrel{ [X,h_k]_\bullet }{\longrightarrow}
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
   \downarrow &{}_{\mathllap{  }} \underset{[X,h_2]_\bullet}{\nwarrow} & 
   \downarrow &{}_{\mathllap{  }} \underset{[X,h_1]_\bullet}{\nwarrow} &
   \downarrow &{}_{\mathllap{  }} \underset{[X,h_0]_\bullet}{\nwarrow}
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

Specifically, regard the terms here as bigraded in the following way

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
     \downarrow^{\mathrlap{}}  
       &{}_{  } \underset{\mathllap{k_2}}{\nwarrow} & 
       {}^{\mathllap{j_2}}\downarrow &
       \underset{k_1}{\nwarrow}
       &
     {}^{\mathllap{j_1}}\downarrow &{}_{} \underset{\mathllap{k_0}}{\nwarrow}
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
fto     \\
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

observe that the composite

$$
  d \coloneqq j \circ k
$$ 

is a [[differential]] in that it squares to 0, due to the exactness of the exact couple:

$$
  \begin{aligned}
    d \circ d & = j \circ \underset{= 0}{\underbrace{k \circ j}} \circ k
    \\
    & = 0
  \end{aligned}
  \,.
$$

One says that the **page** of the exact couple is the [[graded object|graded]] [[chain complex]]

$$
  (\mathcal{E}^{\bullet,\bullet}, d \coloneqq j \circ  k)
  \,.
$$

Given a cochain complex like this, we are to pass to its [[cochain cohomology]]. Since the cochain complex here has the extra structure that it arises from an exact couple, its cohomology groups should still remember some of that extra structure. Indeed, the following says that the remaining extract structure on the cohomology of the page of an exact couple is itself again an exact couple, called the "derived exact couple".

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


+-- {: .num_lemma #DerivedExactCoupleIsExactCouple}
###### Lemma

The derived exact couple in def. \ref{DerivedExactCouple}
is well defined and is itself an exact couple, def. \ref{ExactCouple}.

=--

+-- {: .proof}
###### Proof

This is straightforward to check. For completeness we spell it out:

First consider that the morphisms are well defined in the first place.

It is clear that $\tilde i$ is well-defined.

That $\tilde j$ lands in $ker(d)$: it lands in the image of $j$ which is in the kernel of $k$, by exactness, hence in the kernel of $d$ by definition.

That $\tilde j$ is independent of the choice of preimage: For any $x \in \tilde {\mathcal{D}} = im(i)$, let $y, y' \in \mathcal{D}$ be two preimages under $i$, hence $i(y) = i(y') = x$. This means that $i(y'-y) = 0$, hence that $y'-y \in ker(i)$, hence that $y'-y \in im(k)$, hence there exists $z \in \mathcal{E}$ such that $y' = y + k(z)$, hence $j(y') = j(y) +  j(k(z)) = j(y) + d(z)$, but $d(z) = 0$ in $\tilde{\mathcal{E}}$.

That $\tilde k$ vanishes on $im(d)$: because $im(d) \subset im(j)$ and hence by exactness.

That $\tilde k$ lands in $im(i)$: since it is defined on $ker(d) = ker(j \circ k)$ it lands in $ker(j)$. By exactness this is $im(i)$.

That the sequence of maps is again exact:

The kernel of $\tilde j$ is those $x \in \im(i)$ such that their preimage $i^{-1}(x)$ is still in $im(x)$ (by exactness of the original exact couple) hence such that $x \in im(i|_{im(i)})$, hence such that $x \in im(\tilde i)$.

The kernel of $\tilde k$ is the intersection of the kernel of $k$ with the kernel of $d = j \circ k$, wich is still the kernel of $k$, hence the image of $j$, by exactness. Indeed this is also still the image of $\tilde j$, since for every $x \in \mathcal{D}$ then $\tilde j(i(x)) = j(x)$.

The kernel of $\tilde i$ is $ker(i) \cap im(i) \simeq im(k) \cap im(i)$, by exactness. Let $x \in \mathcal{E}$ such that $k(x) \in im(i)$, then by exactness $k(x) \in ker(j)$ hence $j(k(x)) = d(x) = 0$, hence $x \in ker(d)$ and so $k(x) = \tilde k(x)$.

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

+-- {: .num_remark #TermsOfNextPageOnSpectralSequence}
###### Remark

So the spectral sequence of an exact couple (def. \ref{ExactCoupleSpectralSequence}) is a sequence of cochain complexes $(\mathcal{E}_r, d_r)$, where the cohomology of one is the terms of the next one: 

$$
  \mathcal{E}_{r+1} \simeq H(\mathcal{E}_r,d_r)
  \,.
$$

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
$(1,1)$ with each page, since (by def. \ref{PageOfAnExactCouple})

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

Similarly the first differential has degree

$$
  \begin{aligned}
    deg(j \circ k )
    & =
    deg(j) + deg(k)
    \\
    &= (1,0) + (0,0)
    \\
    & = (1,0)
  \end{aligned}
$$

<div style="float:right;margin:0 10px 10px 0;">
<img src="http://ncatlab.org/nlab/files/adamstypedifferentials.jpg" width="360" > 
</div>

and so the differentials on the $r$th page are of the form

$$
  d_r 
    \;\colon\; 
  \mathcal{E}_r^{s,t} 
    \longrightarrow 
  \mathcal{E}_r^{s+r, t+r-1}
  \,.
$$


It is conventional to depict this in tables where $s$ increases vertically and upwards and $t-s$ increases horizontally and to the right, so that $d_r$ goes up $r$ steps and always one step to the left. This is the "Adams type" grading convention for spectral sequences (different from the [[Serre spectral sequence|Serre-]][[Atiyah-Hirzebruch spectral sequence]] convention ([prop.](Introduction+to+Stable+homotopy+theory+--+S#AHSSExistence))). One also says that

* $s$ is the _filtration degree_;

* $t-s$ is the _total degree_;

* $t$ is the _internal degree_.

A priori all this is $\mathbb{N}\times \mathbb{Z}$-graded, but we regard it as being $\mathbb{Z} \times \mathbb{Z}$-graded by setting

$$
  \mathcal{D}^{s \lt 0,\bullet} \coloneqq 0
  \;\;\;\;\,,
  \;\;\;\;
  \mathcal{E}^{s \lt 0, \bullet} \coloneqq 0
$$

and trivially extending the definition of the differentials to these zero-groups.


=--


##### $E$-Adams filtrations
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

$$
  d_1 = [X, g \circ h]
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

A priori $E_r^{\bullet,\bullet}(X,Y)$ is $\mathbb{N}\times \mathbb{Z}$-graded, but we regard it as being $\mathbb{Z} \times \mathbb{Z}$-graded by setting


$$
  E_r^{s \lt 0,\bullet}(X,Y) \coloneqq 0
$$

and trivially extending the definition of the differentials to these zero-groups.


=--

([Adams 74, theorem 15.1 page 318](#Adams74))

+-- {: .num_remark}
###### Remark

The morphism

$$
  [X,g_k]
  \;\colon\;
  [X,Y_k]_\bullet
    \overset{[X,e \wedge id_{Y_k}]  }{\longrightarrow}
  [X, E \wedge Y_k]_\bullet
$$

in def. \ref{AdamsEAdamsSpectralSequence} is sometimes called the **[[Boardman homomorphism]]** ([Adams 74, p. 58](#Adams74)).

For $X = \mathbb{S}$ the [[sphere spectrum]] it reduces to a canonical morphism from stable homotopy to [[generalized homology]] ([rmk.](Introduction+to+Stable+homotopy+theory+--+1-2#EMHomology))

$$
 \pi_\bullet(g_k)
    \;\colon\;
  \pi_\bullet(Y_k)
    \longrightarrow
  E_\bullet(Y_k)
  \,.
$$

For $E = $ [[HA]] an [[Eilenberg-MacLane spectrum]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#ReducedALinearizationOfnSphere)) this in turn reduces to the **[[Hurewicz homomorphism]]** for spectra.

This way one may think of the $E$-Adams filtration on $Y$ in def. \ref{AdamsEAdamsSpectralSequence} as the result of filtering any spectrum $Y$ by iteratively projecting out all its $E$-homology. 
This idea was historically the original motivation for the construction of the [[classical Adams spectral sequence]] by [[John Frank Adams]], see the first pages of ([Bruner 09](#Adams+spectral+sequence#Bruner09)) for a historical approach.

=--


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


([Adams 74, theorem 15.1 page 319](#Adams74)) Beware that for instance ([Hopkins 99, proof of corollary 5.3](#Hopkins99)) uses "$\overline{E}$" not for the [[homotopy fiber]] of $\mathbb{S} \overset{e}{\to} E$ but for its [[homotopy cofiber]], hence for what is $\Sigma \overline{E}$ according to ([Adams 74](#Adams74)).



+-- {: .num_lemma #Wp}
###### Lemma

In terms of def. \ref{HomotopyFiberOfUnitOfCommutativeRingSpectrum}, the spectra entering the definition of the $E$-[[Adams spectral sequence]] in def. \ref{AdamsEAdamsSpectralSequence} are equivalently

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

By definition the statement holds for $p = 0$. Assume then by [[induction]] that it holds for some $p \geq 0$. Since the [[smash product of spectra]]-functor $(-) \wedge \overline{E}^p \wedge Y$ preserves [[homotopy cofiber sequences]] ([lemma](Introduction+to+Stable+homotopy+theory+--+1-2#SmashTensoringWithSpectrumDerivedPreserveshomotopycofibers), this is part of the [[tensor triangulated category|tensor triangulated]] structure of the [[stable homotopy category]]), its application to the [[homotopy cofiber sequence]] 

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

+-- {: .num_remark}
###### Remark

Terminology differs across authors. The filtration in def. \ref{AdamsEAdamsSpectralSequence} in the rewriting by lemma \ref{Wp} is due to ([Adams 74, theorem 15.1](#Adams74)), where it is not give any name. In ([Ravenel 84, p. 356](Adams+spectral+sequence#Ravenel84)) it is called the (canonical) **Adams tower** while in ([Ravenel 86, def. 2.21](Adams+spectral+sequence#Ravenel86)) it is called the canonical **Adams resolution**. Several authors follow the latter usage, for instance ([Rognes 12, def. 4.1](#Rognes12)). But ([Hopkins 99](Adams+spectral+sequence#Hopkins99)) uses "Adams resolution" for the "$E$-injective resolutions" that we discuss [below](#ViaInjectiveResolutions) and uses "Adams tower" for yet another concept, def. \ref{EAdamsTower} below. See also remark \ref{TerminologyAssociatedInverseSequence}.

=--

We proceed now to analyze the first two pages and then the convergence properties of $E$-Adams spectral sequences of def. \ref{AdamsEAdamsSpectralSequence}.


#### The first page
 {#FirstPageAndHopfAlgebroid}

By lemma \ref{Wp} the first page of an $E$-Adams spectral sequence (def. \ref{AdamsEAdamsSpectralSequence}) looks like

$$
  \begin{aligned}
    E^{s,t}_1(X,Y)
    & 
    \simeq
    [X, E \wedge \overline{E}^s \wedge Y]_{s-t}
  \end{aligned}
  \,.
$$


We discuss now how, under favorable conditions, these hom-groups may alternatively be computed as morphisms of $E$-[[generalized homology|homology]] equipped with suitable [[comodule]] structure over a [[Hopf algebroid]] structure on the dual $E$-[[Steenrod operations]] $E_\bullet(E)$ (The $E$-[[generalized homology]] of $E$ ([rmk.](Introduction+to+Stable+homotopy+theory+--+1-2#EMHomology))). Then [below](#TheE2TermOfTheEAdamsSpectralSequence) we discuss that, as a result, the $d_1$-cohomology of the first page computes the [[Ext]]-groups from the $E$-homology of $Y$ to the $E$-homology of $X$, regarded as $E_\bullet(E)$-comodules. 

The condition needed for this to work is the following.



##### Flat homotopy ring spectra

+-- {: .num_defn #FlatE}
###### Definition

Call a [[homotopy commutative ring spectrum]] $(E,\mu,e)$ ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyCommutativeRingSpectrum)) **flat** if the canonical right $\pi_\bullet(E)$-[[module]] structure on $E_\bullet(E)$ ([prop.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyGroupsOfHomotopyCommutativeRingSpectrum)) (equivalently the canonical left module struture, see prop. \ref{EETwoLeftModuleStructures} below) is a [[flat module]].


=--



The key consequence of the assumption that $E$ is flat in the sense of def. \ref{FlatE} is the following.

+-- {: .num_prop #EnHomology}
###### Proposition

Let $(E,\mu,e)$ be a [[homotopy commutative ring spectrum]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyCommutativeRingSpectrum)) and let $X \in Ho(Spectra)$ be any [[spectrum]]. Then there is a [[homomorphism]] of [[graded abelian groups]] of the form

$$
  E_\bullet(E)
   \otimes_{\pi_\bullet(E)}
  E_\bullet(X)
    \longrightarrow
  [\mathbb{S}, E \wedge E \wedge X]_\bullet
  =
  \pi_\bullet(E \wedge E \wedge X)
$$

(for $E_\bullet(-)$ the canonical $\pi_\bullet(E)$-modules from [this prop.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyGroupsOfHomotopyCommutativeRingSpectrum))  given on elements

$$
  \Sigma^{n_1}\mathbb{S}
   \overset{\alpha_1}{\longrightarrow}
  E \wedge E
  \;\;\,,
  \;\;
  \Sigma^{n_2} \mathbb{S}
    \overset{\alpha_2}{\longrightarrow}
  E \wedge X
$$

by

$$
  \alpha_1 \cdot \alpha_2
    \;\colon\;
  \Sigma^{n_1 + n_2}\mathbb{S}
    \overset{\simeq}{\longrightarrow}
  \Sigma^{n_1} \mathbb{S} \wedge \Sigma^{n_2}\mathbb{S}
    \overset{\alpha_1 \wedge \alpha_2}{\longrightarrow}
  E \wedge E \wedge E \wedge X
    \overset{id_E \wedge \mu \wedge id_X}{\longrightarrow}
  E \wedge E \wedge X
  \,.
$$

If $E_\bullet(E)$ is a [[flat module]] over $\pi_\bullet(E)$ then this is an [[isomorphism]].

=--


([Adams 69, lecture 3, lemma 1 (p. 68)](#Adams69), [Adams 74, part III, lemma 12.5](#Adams74))

+-- {: .proof}
###### Proof

First of all, that the given pairing is a well defined homomorphism (descends from $E_\bullet(E) \times E_\bullet(X)$ to $E_\bullet(E) \otimes_{\pi_\bullet(E)} E_\bullet(X)$) follows from the associativity of $\mu$.

We discuss that it is an isomorphism when $E_\bullet(E)$ is flat over $\pi_\bullet(E)$:

First consider the case that $X \simeq \Sigma^{n} \mathbb{S}$ is a suspension of the [[sphere spectrum]]. Then (by [this example](Introduction+to+Stable+homotopy+theory+--+1-2#SuspendedSphereSpectrumHomology), using the [[tensor triangulated category|tensor triangulated]] stucture on the [[stable homotopy category]] ([prop.] (Introduction+to+Stable+homotopy+theory+--+1-2#TensorTriangulatedStructureOnStableHomotopyCategory)))


$$
  E_\bullet(X) = E_\bullet(\Sigma^n X) \simeq \pi_{\bullet-n}(E)
$$ 

and 

$$
  \pi_\bullet(E \wedge E \wedge X) 
    =
  \pi_\bullet(E \wedge E \wedge \Sigma^n \mathbb{S})
    \simeq 
  E_{\bullet-n}(E)
$$ 

and 

$$
  E_\bullet(E) \otimes_{\pi_\bullet(E)} \pi_{\bullet-n}(E)
    \simeq
  E_{\bullet-n}(E)
$$

Therefore in this case we have an isomorphism for all $E$.

For general $X$, we may without restriction assume that $X$ is represented by a sequential [[CW-spectrum]] ([prop.](Introduction+to+Stable+homotopy+theory+--+1-1#CWApproximationForSequentialSpectra)). Then the [[homotopy cofibers]] of its cell attachment maps are suspensions of the [[sphere spectrum]] ([rmk.](Introduction+to+Stable+homotopy+theory+--+1-1#StrictModelStructureCellAttachmentToSpectra)).

First consider the case that $X$ is a CW-spectrum with finitely many cells. Consider the [[homotopy cofiber sequence]] of the $(k+1)$st cell attachment (by that [remark](Introduction+to+Stable+homotopy+theory+--+1-1#StrictModelStructureCellAttachmentToSpectra)):

$$
  \array{
    \Sigma^{n_k-1}\mathbb{S}
      &\longrightarrow&
    X_k
      &\longrightarrow&
    X_{k+1}
      &\longrightarrow&
    \Sigma^{n_k}\mathbb{S}
      &\longrightarrow&
    \Sigma X_k
  }
$$

and its image under the natural morphism $E_\bullet(E) \otimes_{\pi_\bullet(E)}E_\bullet(-) \to \pi_\bullet([\mathbb{S}, E \wedge E \wedge (-)])$, which is a [[commuting diagram]] of the form

$$
  \array{
    E_\bullet(E) \otimes_{\pi_\bullet(E)}E_\bullet(\Sigma^{n_k-1}\mathbb{S})
      &\longrightarrow&
    E_\bullet(E) \otimes_{\pi_\bullet(E)}E_\bullet(X_k)
      &\longrightarrow&
    E_\bullet(E) \otimes_{\pi_\bullet(E)}E_\bullet(X_{k+1})
      &\longrightarrow&
    E_\bullet(E) \otimes_{\pi_\bullet(E)}E_\bullet(\Sigma^{n_k}\mathbb{S})
      &\longrightarrow&
    E_\bullet(E) \otimes_{\pi_\bullet(E)}E_\bullet(\Sigma X_k)
    \\
    \downarrow
      &&
    \downarrow
      &&
    \downarrow
      &&
    \downarrow
      &&
    \downarrow
    \\
    [\mathbb{S}, E \wedge E \wedge \Sigma^{n_k-1}\mathbb{S}]_\bullet
      &\longrightarrow&
    [\mathbb{S}, E \wedge E \wedge X_k]_{\bullet}
      &\longrightarrow&
    [\mathbb{S}, E \wedge E \wedge X_{k+1}]_{\bullet}
      &\longrightarrow&
    [\mathbb{S}, E \wedge E \wedge \Sigma^{n_k}\mathbb{S}]_{\bullet}
      &\longrightarrow&
    [\mathbb{S}, E \wedge E \wedge \Sigma X_k]_{\bullet}
  }
  \,.
$$

Here the  bottom row is a [[long exact sequence]] since $E \wedge E \wedge (-)$ preserves homotopy cofiber sequences (by [this lemma](Introduction+to+Stable+homotopy+theory+--+1-2#SmashTensoringWithSpectrumDerivedPreserveshomotopycofibers), part of the [[tensor triangulated category|tensor triangulated]] structure on $Ho(Spectra)$ [prop.](Introduction+to+Stable+homotopy+theory+--+1-2#TensorTriangulatedStructureOnStableHomotopyCategory)), and since $[\mathbb{S},-]_\bullet \simeq \pi_\bullet(-)$ sends [[homotopy cofiber sequences]] to [[long exact sequences]] ([prop.](Introduction+to+Stable+homotopy+theory+--+1-1#LongExactSequenceOfStableHomotopyGroups)). By the same reasoning, $E_\bullet(-)$ of the homotopy cofiber sequence is long exact; and by the assumption that $E_\bullet(E)$ is [[flat module|flat]], the functor $E_\bullet(E)\otimes_{\pi_\bullet(E)}(-)$ preserves this exactness, so that also the top row is a [[long exact sequence]].

Now by [[induction]] over the cells of $X$, the outer four vertical morphisms are [[isomorphisms]]. Hence the [[5-lemma]] implies that also the middle morphism is an isomorphism.

This shows the claim inductively for all finite CW-spectra. For the general statement, now use that

1. every CW-spectrum is the [[filtered colimit]] over its finite CW-subspectra;

1. the [[symmetric monoidal smash product of spectra]] $\wedge$ ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#SsymModuleSymmetricSpectra)) preserves colimits in its arguments separately (since it has a [[right adjoint]] ([prop.](Introduction+to+Stable+homotopy+theory+--+1-2#MonoidalCategoryOfModules)));

1. $[\mathbb{S},-]_\bullet \simeq \pi_\bullet(-)$ commutes over filtered colimits of CW-spectrum inclusions (by [this lemma](Introduction+to+Stable+homotopy+theory+--+P#CompactSubsetsAreSmallInCellComplexes), since spheres are [[compact topological space|compact]]);

1. $E_\bullet(E) \otimes_{\pi_\bullet(E)}(-)$ distributes over colimits (it being a [[left adjoint]]).



=--

Using prop. \ref{EnHomology}, we find below (theorem \ref{ComoduleHomsInE1PageOfEAdamsSpectralSequence}) that the first page of the $E$-Adams spectral sequence may be equivalently rewritten as hom-groups of [[comodules]] over $E_\bullet(E)$ regarded as a [[graded commutative Hopf algebroid]]. We now first discuss what this means. 


##### The $E$-Steenrod algebra
 {#DualESteenrodAlgebra}

We discuss here all the extra structure that exists on the $E$-self homology $E_\bullet(E)$ of a flat homotopy commutative ring spectrum. For $E = H \mathbb{F}_p$ the [[Eilenberg-MacLane spectrum]] on a [[prime field]] this reduces to the classical structure in [[algebraic topology]] called the _dual [[Steenrod algebra]]_ $\mathcal{A}^\ast_p$. Therefore one may generally speak of $E_\bullet(E)$ as being the _dual $E$-Steenrod algebra_.

Without the qualifier "dual" then "$E$-Steenrod algebra" refers to the $E$-self-cohomology $E^\bullet(E)$. For $E = H \mathbb{F}_p$ this _Steenrod algebra_ $\mathcal{A}_p$ (without "dual") is traditionally considered first, and the [[classical Adams spectral sequence]] was originally formulated in terms of $\mathcal{A}_p$ instead of $\mathcal{A}_p^\ast$. But one observes ([Adams 74, p. 280](#Adams74)) that the "dual" Steenrod algebra $E_\bullet(E)$ is much better behaved, at least as long as $E$ is flat in the sense of def. \ref{FlatE}. 

Moreover, the dual $E$-Steenrod algebra $E_\bullet(E)$ is more fundamental in that it reflects a [[higher geometry|stacky geometry]] secretly underlying the $E$-Adams spectral sequence ([Hopkins 99](#Hopkins99)). This is the content of the concept of "[[commutative Hopf algebroid]]" (def. \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents} below) which is equivalently the [[formal dual]] of a [[groupoid]] internal to [[affine schemes]], def. \ref{CommutativeHopfAlgebroid}.

A simple illustrative archetype of the following construction of commutative Hopf algebroids from homotopy commutative ring spectra is the following situation:

For $X$ a [[finite set]] consider

$$
  \array{
    X \times X \times X
    \\
    \downarrow^{\mathrlap{\circ = (pr_1, pr_3)}}
    \\
    X \times X
    \\
    {}^{\mathllap{s = pr_1}}\downarrow 
     \uparrow 
    \downarrow^{\mathrlap{t = pr_2}}
    \\
    X
  }  
$$

as the ("[[codiscrete groupoid|codiscrete]]") [[groupoid]] with $X$ as [[objects]] and precisely one morphism from every object to every other. Hence the [[composition]] operation $\circ$, and the [[source]] and [[target]] maps are simply projections as shown. The identity morphism (going upwards in the above diagram) is the [[diagonal]].

Then consider the image of this structure under forming the [[free abelian groups]] $\mathbb{Z}[X]$, regarded as [[commutative rings]] under pointwise multiplication.

Since 

$$
  \mathbb{Z}[X \times X]
    \simeq
  \mathbb{Z}[X] \otimes \mathbb{Z}[X]
$$

this yields a diagram of homomorphisms of commutative rings of the form

$$
  \array{
    (\mathbb{Z}[X] \otimes \mathbb{Z}[X] )
      \otimes_{\mathbb{Z}[X]}
    (\mathbb{Z}[X] \otimes \mathbb{Z}[X])
    \\
    \uparrow^{\mathrlap{} }
    \\
    \mathbb{Z}[X] \otimes \mathbb{Z}[X]
    \\
    \uparrow 
     \downarrow 
    \uparrow
    \\
    \mathbb{Z}[X]
  }  
$$

satisfying some obvious conditions. Observe that here

1. the two morphisms $\mathbb{Z}[X] \rightrightarrows \mathbb{Z}[X] \otimes \mathbb{Z}[X]$ are $f \mapsto f \otimes e$ and $f \mapsto e \otimes f$, respectively, where $e$ denotes the unit element in $\mathbb{Z}[X]$;

1. the morphism $\mathbb{Z}[X] \otimes \mathbb{Z}[X] \to \mathbb{Z}[X]$ is the multiplication in the ring $\mathbb{Z}[X]$;

1. the morphism 

   $$
     \mathbb{Z}[X] \otimes \mathbb{Z}[X] 
       \longrightarrow 
     \mathbb{Z}[X] \otimes \mathbb{Z}[C] \otimes \mathbb{Z}[C] 
       \overset{\simeq}{\longrightarrow}
     (\mathbb{Z}[X] \otimes \mathbb{Z}[X] ) \otimes_{\mathbb{Z}[X]} (\mathbb{Z}[X] \otimes \mathbb{Z}[X])
   $$ 

   is given by $f \otimes g \mapsto f \otimes e \otimes g$.

All of the following rich structure is directly modeled on this simplistic example. We simply 

1. replace the commutative ring $\mathbb{Z}[X]$ with any flat [[homotopy commutative ring spectrum]] $E$, 

1. replace [[tensor product of abelian groups]] $\otimes$ with derived [[smash product of spectra]];

1. and form the [[stable homotopy groups]] $\pi_\bullet(-)$ of all resulting expressions.



+-- {: .num_defn #HopfAlgebroidStructureOnDualEOperations}
###### Definition

Let $(E, \mu, e)$ be a [[homotopy commutative ring spectrum]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyCommutativeRingSpectrum)) which is flat according to def. \ref{FlatE}. 

Then the **dual $E$-[[Steenrod algebra]]** is the pair of [[graded abelian groups]]

$$
  (E_\bullet(E), \pi_\bullet(E))
$$

([rmk.](Introduction+to+Stable+homotopy+theory+--+1-2#EMHomology)) equipped with the following structure:

1. the [[graded commutative ring]] structure

   $$
     \pi_\bullet(E) \otimes \pi_\bullet(E)
       \longrightarrow
     \pi_\bullet(E)
   $$

   induced from $E$ being a [[homotopy commutative ring spectrum]] ([prop.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyGroupsOfHomotopyCommutativeRingSpectrum));


1. the [[graded commutative ring]] structure

   $$
     E_\bullet(E) \otimes E_\bullet(E) \longrightarrow E_\bullet(E)
   $$

   induced from the fact that with $E$ also $E \wedge E$ is canonically a [[homotopy commutative ring spectrum]] ([exmpl.](Introduction+to+Stable+homotopy+theory+--+1-2#TensorProductOfTwoCommutativeMonoids)), so that also $E_\bullet(E) = \pi_\bullet(E \wedge E)$ is a graded commutative ring ([prop.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyGroupsOfHomotopyCommutativeRingSpectrum));

1. the [[homomorphism]] of [[graded commutative rings]]

   $$ 
     \Psi
       \;\colon\;
     E_\bullet(E)
       \longrightarrow
     E_\bullet(E) \otimes_{\pi_\bullet(E)} E_\bullet(E)
   $$

   induced under $\pi_\bullet(-)$ from

   $$
     E \wedge E 
       \overset{id \wedge e \wedge id}{\longrightarrow}
     E \wedge E \wedge E
   $$

   via prop. \ref{EnHomology};


1. the [[homomorphisms]] of graded commutative rings

   $$
     \eta_L 
       \;\colon\;
     \pi_\bullet(E)
       \longrightarrow
     E_\bullet(E)
   $$

   and

   $$
     \eta_R
       \;\colon\;
     \pi_\bullet(E)
       \longrightarrow
     E_\bullet(E)
   $$

   induced under $\pi_\bullet(-)$ from the homomorphisms of commutative ring spectra

   $$
     E \underoverset{\simeq}{r_{E}^{-1}}{\to} E \wedge \mathbb{S} 
       \overset{id \wedge e}{\longrightarrow}
     E \wedge E
   $$

   and

   $$
     E \underoverset{\simeq}{\ell_E^{-1}}{\to} \mathbb{S} \wedge E
       \overset{id \wedge e}{\longrightarrow}
     E \wedge E
     \,,
   $$

   respectively ([exmpl.](Introduction+to+Stable+homotopy+theory+--+1-2#TensorProductOfTwoCommutativeMonoids));

1. the homomorphism of graded commutative rings

   $$
     \epsilon 
       \;\colon\;
     E_\bullet(E)
       \longrightarrow
     \pi_\bullet(E)
   $$

   induced under $\pi_\bullet(-)$ from 

   $$
     \mu \;\colon\;  E \wedge E \longrightarrow E
   $$

   regarded as a homomorphism of homotopy commutative ring spectra ([exmpl.](Introduction+to+Stable+homotopy+theory+--+1-2#TensorProductOfTwoCommutativeMonoids));

1. the homomorphisms graded commutative rings

   $$
     c 
       \;\colon\;
     E_\bullet(E)
       \longrightarrow
     E_\bullet(E)
   $$

   induced under $\pi_\bullet(-)$ from the [[braiding]]

   $$
     \tau_{E,E} 
       \;\colon\; 
     E \wedge E 
       \longrightarrow 
     E \wedge E
   $$

   regarded as a homomorphism of homotopy commutative ring spectra ([exmpl.](Introduction+to+Stable+homotopy+theory+--+1-2#TensorProductOfTwoCommutativeMonoids)).


=--

([Adams 69, lecture 3, pages 66-68](#Adams69))

Notice that (as verified by direct unwinding of the definitions):

+-- {: .num_lemma}
###### Lemma

For $(E, \mu, e)$ a [[homotopy commutative ring spectrum]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyCommutativeRingSpectrum)), consider $E_\bullet(E)$ with its canonical left and right $\pi_\bullet(E)$-module structure as in [this prop.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyGroupsOfHomotopyCommutativeRingSpectrum). These module structures coincide with those induced by the ring homomorphisms $\eta_L$ and $\eta_R$ from def. \ref{HopfAlgebroidStructureOnDualEOperations}.

=--

These two actions need not strictly coincide, but they are isomorphic:

+-- {: .num_prop #EETwoLeftModuleStructures}
###### Proposition

For $(E, \mu, e)$ a [[homotopy commutative ring spectrum]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyCommutativeRingSpectrum)), consider $E_\bullet(E)$ with its canonical left and right $\pi_\bullet(E)$-module structure ([prop.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyGroupsOfHomotopyCommutativeRingSpectrum)). Since $E$ is a [[commutative monoid]], this right module structure may equivalently be regarded as a left-module, too. Then the [[braiding]]

$$
  E_\bullet(E)
   \simeq
  \pi_\bullet(E \wedge E)
    \overset{\pi_\bullet(\tau_{E,E})}{\longrightarrow}
  \pi_\bullet(E \wedge E)
    \simeq
  E_\bullet(E)
$$

constitutes a module isomorphism ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#ModulesInMonoidalCategory)) between these two left module structures.

=--

+-- {: .proof}
###### Proof

On representatives as in the proof of ([this propo.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyGroupsOfHomotopyCommutativeRingSpectrum)), the original left action is given by (we are notationally suppressing [[associators]] throughout)

$$
  E \wedge E \wedge E
   \overset{\mu \wedge id}{\longrightarrow}
  E \wedge E
  \,,
$$

while the other left action, induced from the canonical right action, is given by

$$
  E \wedge E \wedge E
    \underoverset{\simeq}{\tau_{E, E \wedge E}}{\longrightarrow}
  E \wedge E \wedge E
    \overset{id \wedge \mu}{\longrightarrow}
  E \wedge
  \,.
$$

So in order that $\tau_{E,E}$ represents a module homomorphism under $\pi_\bullet(-)$, it is sufficient that the following diagram commutes (we write $E_i \coloneqq E$ for $i \in \{1,2,3\}$ to make the action of the [[braiding]] more manifest)

$$
  \array{
    E_1 \wedge E_2 \wedge E_3 
      &\overset{id \wedge \tau_{E_2,E_3}}{\longrightarrow}&
    E_1 \wedge E_3 \wedge E_2
    \\
    {}^{\mathllap{id}}\downarrow
      &&
    \downarrow^{\mathrlap{\tau_{E_1, E_3 \wedge E_2}}}
    \\
      &&
    E_3 \wedge E_2 \wedge E_1
    \\
    {}^{\mathllap{\mu \wedge id}}\downarrow
      &&
    \downarrow^{\mathrlap{id \wedge \mu}}
    \\
    E \wedge E_3 
     &\underset{\tau_{E,E_3}}{\longrightarrow}&
    E_3 \wedge E
  }
  \,.
$$

But since $(E,\mu,e)$ is a [[commutative monoid]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#MonoidsInMonoidalCategory)), it satisfies $\mu = \mu \circ \tau$ so that we may factor this diagram as follows:

$$
  \array{
    E_1 \wedge E_2 \wedge E_3 
      &\overset{id \wedge \tau_{E_2,E_3}}{\longrightarrow}&
    E_1 \wedge E_3 \wedge E_2
    \\
    {}^{\mathllap{\tau_{E_1, E_2} \wedge id}}\downarrow
      &&
    \downarrow^{\mathrlap{\tau_{E_1, E_3 \wedge E_2}}}
    \\
    E_2 \wedge E_1 \wedge E_3
      &\overset{\tau_{E_2 \wedge E_1, E_3}}{\longrightarrow}&
    E_3 \wedge E_2 \wedge E_1
    \\
    {}^{\mathllap{\mu \wedge id}}\downarrow
      &&
    \downarrow^{\mathrlap{id \wedge \mu}}
    \\
    E \wedge E_3 
     &\underset{\tau_{E,E_3}}{\longrightarrow}&
    E_3 \wedge E
  }
  \,.
$$

Here the top square commutes by [[coherence theorem for symmetric monoidal categories|coherence]] of the braiding ([rmk](Introduction+to+Stable+homotopy+theory+--+1-2#SymmetricMonoidalCategoriesCoherenceTheorem)) since both composite morphisms correspond to the same [[permutation]], while the bottom square commutesm due to the [[natural transformation|naturality]] of the braiding. Hence the total rectangle commutes.

=--


The dual $E$-[[Steenrod algebras]] of def. \ref{HopfAlgebroidStructureOnDualEOperations} evidently carry a lot of structure. The concept organizing this is that of_[[commutative Hopf algebroids]]_.


+-- {: .num_defn #CommutativeHopfAlgebroid}
###### Definition

A **[[graded commutative Hopf algebroid]]** is an [[internal groupoid]] in the [[opposite category]] $gCRing^{op}$ of $\mathbb{Z}$-[[graded commutative rings]], regarded with its [[cartesian monoidal category]] structure.

=--

(e.g. [Ravenel 86, def. A1.1.1](#Ravenel86))

+-- {: .num_remark #CommutativeHopfAlgebroidSpelledOut}
###### Remark

We unwind def. \ref{CommutativeHopfAlgebroid}.  For $R \in gCRing$, write $Spec(R)$ for the same object, but regarded as an object in $gCRing^{op}$. 

An [[internal category]] in $gCRing^{op}$ is a [[diagram]] in $gCRing^{op}$ of the form

$$
  \array{
    Spec(\Gamma) \underset{Spec(A)}{\times} Spec(\Gamma)
    \\
    \downarrow^{\mathrlap{\circ}}
    \\
    Spec(\Gamma)
    \\
    {}^{\mathllap{s}}\downarrow \; \uparrow_{\mathrlap{i}} \downarrow^{\mathrlap{t}}
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

The key basic fact to use in order to express this equivalently in terms of algebra is that [[tensor product]] of commutative rings exhibits the [[cartesian monoidal category]] structure on $CRing^{op}$, see at _[CRing -- Properties -- Cocartesian comonoidal structure](CRing#CocartesianComnonoidalStructure)_:

$$
  Spec(R_1) \underset{Spec(R_3)}{\times} Spec(R_2) 
  \simeq
  Spec(R_1 \otimes_{R_3} R_2)
  \,.
$$

This means that the above is equivalently a diagram in $gCRing$ of the form

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

* $\eta_L, \eta_R$ are called the left and right _[[unit]] maps_;

* $\epsilon$ is called the _co-unit_;

* $\Psi$ is called the _[[comultiplication]]_;

* $c$ is called the _[[antipode]]_ or _conjugation_


=--

+-- {: .num_remark #HopfAlgebrasAsHopfAlgebroids}
###### Remark

Generally, in a commutative Hopf algebroid, def. \ref{CommutativeHopfAlgebroid}, the two morphisms $\eta_L, \eta_R\colon A \to \Gamma$ from remark \ref{CommutativeHopfAlgebroidSpelledOut} need not coincide, they make $\Gamma$ genuinely into a [[bimodule]] over $A$, and it is the [[tensor product]] of [[bimodules]] that appears in remark \ref{CommutativeHopfAlgebroidSpelledOut}. But it may happen that they coincide:

An [[internal groupoid]] $\mathcal{G}_1 \stackrel{\overset{s}{\longrightarrow}}{\underset{t}{\longrightarrow}} \mathcal{G}_0$ for which the [[domain]] and [[codomain]] morphisms coincide, $s = t$, is euqivalently a [[group object]] in the [[slice category]] over $\mathcal{G}_0$.

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

   1. (identity morphisms respect source and target) 

      $\epsilon \circ \eta_L = \epsilon \circ \eta_R = id_A$;

   1. (identity morphisms are units for composition) 

      $(id_\Gamma \otimes_A \epsilon) \circ \Psi  = (\epsilon \otimes_A id_\Gamma) \circ \Psi = id_\Gamma$;

   1. (composition respects source and target) 

      1. $\Psi \circ \eta_R = (id \otimes_A \eta_R) \circ \eta_R$;

      1. $\Psi \circ \eta_L = (\eta_L \otimes_A id) \circ \eta_L$

1. (co-[[associativity]]) $(id_\Gamma \otimes_A \Psi) \circ \Psi = (\Psi \otimes_A id_\Gamma) \circ \Psi$;

1. ([[inverses]])

   1. (inverting twice is the identity) 

      $c \circ c = id_\Gamma$;

   1. (inversion swaps source and target) 

      $c \circ \eta_L = \eta_R$; $c \circ \eta_R = \eta_L$;

   1. (inverse morphisms are indeed left and right inverses for composition) 

      the morphisms $\alpha$ and $\beta$ induced via the [[coequalizer]] property of the [[tensor product]] from $(-) \cdot c(-)$ and $c(-)\cdot (-)$, respectively

      $$
        \array{
          \Gamma \otimes A \otimes \Gamma
            &
            \underoverset
              {\longrightarrow}
              {\longrightarrow}
              {}
            &
          \Gamma \otimes \Gamma
             &
             \overset{coeq}{\longrightarrow}
             &
          \Gamma \otimes_A \Gamma
           \\
           &&
           {}_{\mathllap{(-)\cdot c(-)}}\downarrow 
           & 
            \swarrow_{\mathrlap{\alpha}}
           \\
           && \Gamma
        }
      $$

      and

      $$
        \array{
          \Gamma \otimes A \otimes \Gamma
            &
            \underoverset
              {\longrightarrow}
              {\longrightarrow}
              {}
            &
          \Gamma \otimes \Gamma
             &
             \overset{coeq}{\longrightarrow}
             &
          \Gamma \otimes_A \Gamma
           \\
           &&
           {}_{\mathllap{c(-)\cdot (-)}}\downarrow 
           & 
            \swarrow_{\mathrlap{\beta}}
           \\
           && \Gamma
        }
      $$

      satisfy 

      $\alpha \circ \Psi = \eta_L \circ \epsilon $

      and

      $\beta \circ \Psi = \eta_R \circ \epsilon $.
   
=--

([Adams 69, lecture 3, pages 62-66](#Adams69), [Ravenel 86, def. A1.1.1](#Ravenel86))

+-- {: .num_remark}
###### Remark

In ([Adams 69, lecture 3, page 60](#Adams69)) the terminology used is "Hopf algebra in a fully satisfactory sense" with emphasis that the left and right module structure may differ. According to ([Ravenel 86, first page of appendix A1](#Ravenel86)) the terminology "Hopf algebroid" for this situation is due to [[Haynes Miller]].

=--


+-- {: .num_example #CommutativeHopfAlgebroidCodiscreteOverCommutativeRing}
###### Example

For $R$ a [[commutative ring]], then $R \otimes R$ becomes a [[commutative Hopf algebroid]] over $R$, formally dual (via def. \ref{CommutativeHopfAlgebroid}) to the [[pair groupoid]] on $Spec(R) \in CRing^{op}$.

For $X$ a [[finite set]] and $R = \mathbb{Z}[X]$, then this reduces to the motivating example from [above](#DualESteenrodAlgebra).

=--

It is now straightforward, if somewhat tedious, to check that:

+-- {: .num_prop #DualESteenrodAlgebrasIsCommutativeHopfAlgebroid}
###### Proposition

Let $(E, \mu, e)$ be a [[homotopy commutative ring spectrum]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyCommutativeRingSpectrum)) which is flat according to def. \ref{FlatE}, then the dual $E$-[[Steenrod algebra]] $ (E_\bullet(E), \pi_\bullet(E))$ with the
structure maps $(\eta_L, \eta_R, \epsilon, c, \Psi)$ from prop. \ref{HopfAlgebroidStructureOnDualEOperations} is a graded commutative Hopf algebroid according to def. \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents}:

$$
  (E_\bullet(E), \pi_\bullet(E))
  \;\in\;
  CommHopfAlgd
$$

=--

([Adams 69, lecture 3, pages 67-71](#Adams69), [Ravenel 86, chapter II, prop. 2.2.8](#Ravenel86)) 

+-- {: .proof}
###### Proof

One observes that $E \wedge E$ satisfies the axioms of a commutative Hopf algebroid object in homotopy commutative ring spectra, over $E$, by direct analogy to example \ref{CommutativeHopfAlgebroidCodiscreteOverCommutativeRing} (one just has to verify that the symmetric [[braidings]] go along coherently, which works by use of the [[coherence theorem for symmetric monoidal categories]] ([rmk.](Introduction+to+Stable+homotopy+theory+--+1-2#SymmetricMonoidalCategoriesCoherenceTheorem))). Applying the functor $\pi_\bullet(-)$ that forms [[stable homotopy groups]] to all structure morphisms of $E \wedge E$ yields the claimed structure morphisms of $E_\bullet(E)$.

=--



We close this subsection on [[commutative Hopf algebroids]] by discussion of their [[isomorphism classes]], when regarded dually as affine [[groupoids]]:


+-- {: .num_defn #IsomorphismClassesOfCOmmutativeHopfAlgebroid}
###### Definition

Given an [[internal groupoid]] in $gCRing^{op}$ (def. \ref{CommutativeHopfAlgebroid}, remark \ref{CommutativeHopfAlgebroidSpelledOut})

$$
  \array{
    Spec(\Gamma) \underset{Spec(A)}{\times} Spec(\Gamma)
    \\
    \downarrow^{\mathrlap{\circ}}
    \\
    Spec(\Gamma)
    \\
    {}^{\mathllap{s}}\downarrow \; \uparrow_{\mathrlap{i}} \downarrow^{\mathrlap{t}}
    \\
    Spec(A)
  }
  \,,
$$

then its affife scheme $Spec(A)_{/\sim}$ of **[[isomorphism classes]] of objects** is the [[coequlizer]] of the source and target morphisms

$$
  Spec(\Gamma)
    \underoverset
     {\underset{t}{\longrightarrow}}
     {\overset{s}{\longleftarrow}}
     {\phantom{AA}}
  Spec(A)
    \overset{equ}{\longrightarrow}
  Spec(A)_{/\sim}
  \,.
$$

Hence this is the [[formal dual]] of the [[equalizer]] of the left and right unit (def. \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents})

$$
  
  A
    \underoverset
      {\underset{\eta_R}{\longrightarrow}}
      {\overset{\eta_L}{\longrightarrow}}
      {\phantom{AA}}
  \Gamma
  \,.
$$


=--

By example \ref{CommutativeHopfAlgebroidCodiscreteOverCommutativeRing} every [[commutative ring]] gives rise to a commutative Hopf algebroid $R \otimes R$ over $R$. The _[[core of a ring|core]]_ of $R$ is the formal dual of the corresponding affine scheme of isomorphism classes according to def. \ref{IsomorphismClassesOfCOmmutativeHopfAlgebroid}:

+-- {: .num_defn #CoreOfARing}
###### Definition

For $R$ a [[commutative ring]], its **[[core of a ring|core]]** $c R$ is the [[equalizer]] in

$$
  c R 
    \longrightarrow 
  R 
    \stackrel{\longrightarrow}{\longrightarrow}
  R \otimes R
  \,.
$$

A ring which is isomorphic to its core is called a **[[solid ring]]**.

=--

([Bousfield-Kan 72, &#167;1, def. 2.1](#BousfieldKan72), [Bousfield 79, 6.4](#Bousfield79))


+-- {: .num_prop #FormingCoreOfARingIsIdempotent}
###### Proposition

The [[core of a ring|core]] of any ring $R$ is solid (def. \ref{CoreOfARing}):

$$
  c c R \simeq c R
  \,.
$$

=--

([Bousfield-Kan 72, prop. 2.2](#BousfieldKan72))


+-- {: .num_prop #ClassificationOfSolidRings}
###### Proposition

The following is the complete list of solid rings (def. \ref{CoreOfARing}) up to [[isomorphism]]:

1. The [[localization of a ring|localization]] of the ring of [[integers]] at a set $J$ of [[prime numbers]] (def. \ref{InvertingPrimes})

   $$
     \mathbb{Z}[J^{-1}]
     \,;
   $$

1. the [[cyclic rings]]

   $$
     \mathbb{Z}/n\mathbb{Z}
   $$

   for $n \geq 2$;

1. the [[Cartesian product|product]] rings 

   $$
     \mathbb{Z}[J^{-1}]
       \times
     \mathbb{Z}/n\mathbb{Z}
     \,,
   $$

   for $n \geq 2$ such that each [[prime factor]] of $n$ is contained in the set of primes $J$;

1. the ring cores of product rings

   $$
     c(\mathbb{Z}[J^{-1}] \times \underset{p \in K}{\prod} \mathbb{Z}/p^{e(p)})
     \,,
   $$

   where $K \subset J$ are infinite sets of primes and $e(p)$ are positive natural numbers.

=--

([Bousfield-Kan 72, prop. 3.5](#BousfieldKan72), [Bousfield 79, p. 276](#Bousfield79))


##### Comodules over the $E$-Steenrod algebra

+-- {: .num_defn #SteenrodComoduleStructureOnSpectrum}
###### Definition

Let $(E, \mu, e)$ be a [[homotopy commutative ring spectrum]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyCommutativeRingSpectrum)) which is flat according to def. \ref{FlatE}. 

For $X \in Ho(Spectra)$ any spectrum, say that the **comodule structure** on $E_\bullet(X)$ ([rmk.](Introduction+to+Stable+homotopy+theory+--+1-2#EMHomology))) **over the dual $E$-Steenrod algebra** (def. \ref{HopfAlgebroidStructureOnDualEOperations})  is

1. the canonical structure of a $\pi_\bullet(E)$-[[module]] (according to [this prop.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyGroupsOfHomotopyCommutativeRingSpectrum));

1. the homomorphism of $\pi_\bullet(E)$-modules

   $$
     \Psi_{E_\bullet(X)}
       \;\colon\;
     E_\bullet(X)
       \longrightarrow
     E_\bullet(E) \otimes_{\pi_\bullet(E)} E_\bullet(X)
   $$ 

   induced under $\pi_\bullet(-)$ and via prop. \ref{EnHomology} from the morphism of spectra 

   $$
     E \wedge X
      \simeq
     E \wedge \mathbb{S} \wedge X
       \overset{id \wedge e \wedge id}{\longrightarrow}
     E \wedge E \wedge X
     \,.
   $$

=--

+-- {: .num_defn #HopfComoduleRing}
###### Definition

Given a [[graded commutative Hopf algebroid]] $\Gamma$ over $A$ as in def. \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents}, hence an [[internal groupoid]] in $gCRing^{op}$, then a **comodule ring** over it is an [[action]] in $CRing^{op}$ of that internal groupoid.

=--

In the same spirit, a **[[comodule]]** over a commutative Hopf algebroid (not necessarily a comodule ring) is a [[quasicoherent sheaf]] on the corresponding [[internal groupoid]] (regarded as a ([[algebraic stack|algebraic]]) [[stack]]) (e.g. [Hopkins 99, prop. 11.6](#Hopkins99)). Explicitly in components:

+-- {: .num_defn #CommutativeHopfAlgebroidComodule}
###### Definition

Given a $\mathbb{Z}$-[[graded commutative Hopf algebroid]] $\Gamma$ over $A$ (def. \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents})
then a **left [[comodule]]** over $\Gamma$ is

1. a $\mathbb{Z}$-[[graded module|graded]] $A$-[[module]] $N$;

1. ([[co-action]]) a [[homomorphism]] of graded $A$-modules

   $\Psi_N \;\colon\; N \longrightarrow \Gamma \otimes_A N$;

such that

1. (co-[[unitality]])

   $(\epsilon \otimes_A id_N) \circ \Psi_N = id_N$;

1. (co-action property)

   $(\Psi \otimes_A id_N) \circ \Psi_N = (id_\Gamma \otimes_A \Psi_N)\circ \Psi_N$.

A [[homomorphism]] between graded comodules $f \colon N_1 \to N_2$ is a homomorphism of underlying graded $A$-modules such that the following [[commuting diagram|diagram commutes]] 

$$
  \array{
    N_1 &\overset{f}{\longrightarrow}& N_1
    \\
    {}^{\mathllap{\Psi_{N_1}}}\downarrow 
      &&
    \downarrow^{\mathrlap{\Psi_{N_2}}}
    \\
    \Gamma \otimes_A N_1
      &\underset{id \otimes_A f}{\longrightarrow}&
    \Gamma \otimes_A N_2
  }
  \,.
$$



We write

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

A priori this is an [[Ab-enriched category]],  but it is naturally further [[enriched category|enriched]] in [[graded abelian groups]]:

we may drop in the above definition of comodule homomorphisms $f\colon N_1 \to N_2$ the condition that the underlying morphism be grading-preserving. Say that $f$ has degree $n$ if it increases degree by $n$. This gives a $\mathbb{Z}$-graded hom-group


$$
  Hom^\bullet_\Gamma(-,-)
  \,.
$$

=--

+-- {: .num_example #ComoduleStructureOnGroundRing}
###### Example

For $(\Gamma,A)$ a [[commutative Hopf algebroid]], then $A$ becomes a left $\Gamma$-comodule (def. \ref{CommutativeHopfAlgebroidComodule}) with coaction given by the right unit

$$
  A \overset{\eta_R}{\longrightarrow} \Gamma \simeq \Gamma \otimes_A A
  \,.
$$

=--

+-- {: .proof}
###### Proof

The required co-unitality property is the dual condition in def. \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents}

$$
  \epsilon \circ \eta_R  = id_A
$$

of the fact in def. \ref{CommutativeHopfAlgebroid} that identity morphisms respect sources:

$$
  id
    \;\colon\;
  A 
    \overset{\eta_R}{\longrightarrow} 
  \Gamma
    \simeq
  \Gamma \otimes_A A
    \overset{\epsilon \otimes_A id}{\longrightarrow}
  A \otimes_A A
    \simeq
  A
$$

The required co-action property is the dual condition 

$$
  \Psi \circ \eta_R = (id \otimes_A \eta_R) \circ \eta_R
$$ 

of the fact in def. \ref{CommutativeHopfAlgebroid} that composition of morphisms in a groupoid respects sources

$$
  \array{
    A 
      &\overset{\eta_R}{\longrightarrow}&
    \Gamma
    \\
    {}^{\mathllap{\eta_R}}\downarrow
      &&
    \downarrow^{\mathrlap{\Psi}}
    \\
    \Gamma \simeq \Gamma \otimes_A A
      &\underset{id \otimes_A \eta_R}{\longrightarrow}&
    \Gamma \otimes_A \Gamma
  }
  \,.
$$


=--


+-- {: .num_prop #IndeedComoduleStructureOnEX}
###### Proposition

Let $(E, \mu, e)$ be a [[homotopy commutative ring spectrum]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyCommutativeRingSpectrum)) which is flat according to def. \ref{FlatE}, and for $X \in Ho(Spectra)$ any spectrum, then the morphism $\Psi_{E_\bullet(X)}$ from def. \ref{SteenrodComoduleStructureOnSpectrum} makes $E_\bullet(X)$ into a [[comodule]] (def. \ref{CommutativeHopfAlgebroidComodule}) over the dual $E$-[[Steenrod algebra]] (def. \ref{HopfAlgebroidStructureOnDualEOperations})

$$
  E_\bullet(X)
  \;\in\;
  E_\bullet(E) CoMod
  \,.
$$

=--

([Adams 69, lecture 3, pages 67-71](#Adams69), [Ravenel 86, chapter II, prop. 2.2.8](#Ravenel86)) 


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
  A Mod
    \underoverset
      {\underset{co-free}{\longrightarrow}}
      {\overset{forget}{\longleftarrow}}
      {\bot}
  \Gamma CoMod
$$

between the [[category]] of $\Gamma$-[[comodules]], def. \ref{CommutativeHopfAlgebroidComodule} and the [[category of modules]] over $A$, where the [[cofree functor]] is [[right adjoint]]. 

Moreover:

1. The co-free $\Gamma$-[[comodule]] on an $A$-module $C$ is $\Gamma \otimes_A C$ equipped with the [[coaction]] induced by the [[comultiplication]] $\Psi$ in $\Gamma$.

1. The [[adjunct]] $\tilde f$ of a comodule homomorphism

   $$
     N \overset{f}{\longrightarrow} \Gamma \otimes_A C
   $$

   is its composite with the counit $\epsilon$ of $\Gamma$

   $$
     \tilde f 
       \;\colon\; 
     N 
       \overset{f}{\longrightarrow} 
     \Gamma \otimes_A C
       \overset{\epsilon \otimes_A id}{\longrightarrow}
     A \otimes_A C
       \simeq
     C
     \,.
   $$

=--

The **proof** is [[formal dual|formally dual]] to the proof that shows that constructing [[free modules]] is [[left adjoint]] to the [[forgetful functor]] from a [[category of modules]] to the underlying [[monoidal category]] ([prop.](Introduction+to+Stable+homotopy+theory+--+1-2#MonoidModuleOverItself)). But since the details of the adjunction isomorphism are important for the following discussion, we spell it out:


+-- {: .proof}
###### Proof


A homomorphism into a co-free $\Gamma$-comodule is a morphism of $A$-modules of the form

$$
  f \;\colon\; N \longrightarrow \Gamma \otimes_A C
$$

making the following [[commuting diagram|diagram commute]]

$$
  \array{
    N &\overset{f}{\longrightarrow}& \Gamma \otimes_A C
    \\
    {}^{\mathllap{\Psi_N}}\downarrow 
      &&
    \downarrow^{\mathrlap{\Psi \otimes_A id}}
    \\
    \Gamma \otimes_A N
      &\underset{id \otimes_A f}{\longrightarrow}&
    \Gamma \otimes_A \Gamma \otimes_A C
  }
  \,.
$$

Consider the composite

$$
  \tilde f
  \;\colon\;
  N 
    \overset{f}{\longrightarrow}
  \Gamma \otimes_A C
    \overset{\epsilon \otimes_A id}{\longrightarrow}
  A \otimes_A C
    \simeq
  C
  \,,
$$

i.e. the "corestriction" of $f$ along the counit of $\Gamma$. By definition this makes the following square commute

$$
  \array{
    \Gamma \otimes_A N 
      &\overset{id \otimes_A f}{\longrightarrow}&
    \Gamma \otimes_A \Gamma \otimes_A C
    \\
    {}^{\mathllap{=}}\downarrow
      &&
    \downarrow^{\mathrlap{id \otimes_A \epsilon \otimes_A id}}
    \\
    \Gamma \otimes_A N
      &\underset{id \otimes_A \tilde f}{\longrightarrow}&
    \Gamma \otimes_A C
  }
  \,.
$$

Pasting this square onto the bottom of the previous one yields

$$
  \array{
    N &\overset{f}{\longrightarrow}& \Gamma \otimes_A C
    \\
    {}^{\mathllap{\Psi_N}}\downarrow 
      &&
    \downarrow^{\mathrlap{\Psi \otimes_A id}}
    \\
    \Gamma \otimes_A N
      &\underset{id \otimes_A f}{\longrightarrow}&
    \Gamma \otimes_A \Gamma \otimes_A C
    \\
    {}^{\mathllap{=}}\downarrow
      &&
    \downarrow^{\mathrlap{id \otimes_A \epsilon \otimes_A id}}
    \\
    \Gamma \otimes_A N
      &\underset{id \otimes_A \tilde f}{\longrightarrow}&
    \Gamma \otimes_A C
  }
  \,.
$$

Now due to co-unitality, the right right vertical composite is the identity on $\Gamma \otimes_A C$. But this means by the commutativity of the outer rectangle that $f$ is uniquely fixed in terms of $\tilde f$ by the relation

$$
  f = (id \otimes_A f) \circ \Psi
  \,.
$$

This establishes a [[natural bijection]] 

$$
  \frac{
    N \overset{f}{\longrightarrow} \Gamma \otimes_A C
  }{
    N \overset{\tilde f}{\longrightarrow} C
  }
$$

and hence the adjunction in question.



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





##### Universal coefficient theorem


The key use of the Hopf coalgebroid structure of prop. \ref{HopfAlgebroidStructureOnDualEOperations} for the present purpose is that it is extra structure inherited by morphisms in $E$-homology from morphisms of spectra. Namely forming $E$-homology $f_\ast \colon E_\bullet(X) \to E_\bullet(Y)$ of a morphism of a spectra $f \colon X \to Y$ does not just produce a morphism of $E$-homology groups

$$
  [X,Y]_\bullet 
    \longrightarrow 
  Hom_{Ab^{\mathbb{Z}}}(E_\bullet(X), E_\bullet(Y))
$$

but in fact produces homomorphisms of comodules over $E_\bullet(E)$

$$
  \alpha
   \;\colon\;  
  [X,Y]_\bullet
    \longrightarrow
  Hom_{E_\bullet(E)}(E_\bullet(X), E_\bullet(Y))
  \,.
$$

This is the statement of lemma \ref{SmashingMapsWithEFactorsThroughSteenrodComoduleHomomorphisms} below. The point is that $E_\bullet(E)$-comodule homomorphism are much more rigid than general abelian group homomorphisms and hence closer to reflecting the underlying morphism of spectra $f \colon X \to Y$. 

In good cases such an approximation of _homotopy_ by _homology_ is in fact accurate, in that $\alpha$ is an [[isomorphism]]. In such a case ([Adams 74, part III, section 13](#Adams74)) speaks of a "[[universal coefficient theorem]]" (the [[coefficients]] here being $E$.)

One such case is exhibited by prop. \ref{ComoduleHomForENCohomology} below. This allows to equivalently re-write the first page of the $E$-Adams spectral sequence in terms of $E$-homology homomorphisms in theorem \ref{ComoduleHomsInE1PageOfEAdamsSpectralSequence} below.

+-- {: .num_lemma #SmashingMapsWithEFactorsThroughSteenrodComoduleHomomorphisms}
###### Lemma

For $X,Y \in Ho(Spectra)$ any two [[spectra]], the morphism (of $\mathbb{Z}$-[[graded abelian groups|graded abelian]]) [[generalized homology|generalized]] [[homology groups]] given by [[smash product of spectra|smash product]] with $E$ ([rmk.](Introduction+to+Stable+homotopy+theory+--+1-2#EMHomology))

$$
  \array{
    \pi_\bullet(E \wedge -)
      &\colon&
    [X,Y]_\bullet
      &\longrightarrow&
    Hom^\bullet_{Ab^{\mathbb{Z}}}(E_\bullet(X), E_\bullet(Y))
    \\
    &&
    (X \overset{f}{\longrightarrow} Y)
      &\mapsto&
    \left(
      E_\bullet(X) 
        \overset{f_\ast}{\longrightarrow}
      E_\bullet(Y)
    \right)
  }
$$

factors through the [[forgetful functor]] from $E_\bullet(E)$-[[comodule]] [[homomorphisms]] (def. \ref{CommutativeHopfAlgebroidComodule}) over the dual $E$-[[Steenrod algebra]] (def. \ref{HopfAlgebroidStructureOnDualEOperations}):

$$
  \array{
    &&  Hom^\bullet_{E_\bullet(E)}(E_\bullet(X), E_\bullet(Y))
    \\
      & {}^{\mathllap{\exists}}\nearrow 
      & \downarrow^{\mathrlap{forget}}
    \\
    [X,N]_\bullet
      &\underset{\pi_\bullet(E \wedge -)}{\longrightarrow}&
    Hom^\bullet_{Ab^{\mathbb{Z}}}(E_\bullet(X), E_\bullet(Y))
  }
  \,,
$$

where $E_\bullet(X)$ and $E_\bullet(Y)$ are regarded as $E$-Steenrod comodules according to def. \ref{CommutativeHopfAlgebroidComodule}, prop. \ref{IndeedComoduleStructureOnEX}.

=--

+-- {: .proof}
###### Proof

By def. \ref{CommutativeHopfAlgebroidComodule} we need to show that for $X \overset{f}{\longrightarrow} Y$ a morphism in $Ho(Spectra)$ then the following [[commuting diagram|diagram commutes]]

$$
  \array{
    E_\bullet(X)
      &\overset{f_\ast}{\longrightarrow}&
    E_\bullet(Y)
    \\
    {}^{\mathllap{\Psi_{E_\bullet(X)}}}\downarrow
      &&
    \downarrow^{\mathrlap{\Psi_{E_\bullet(Y)}}}
    \\
    E_\bullet(E) \otimes_{\pi_\bullet(E)} E_\bullet(X)
      &\underset{id \otimes_{\pi_\bullet(E)} f_\ast }{\longrightarrow}&
    E_\bullet(E) \otimes_{\pi_\bullet(E)} E_\bullet(Y)
  }
  \,.
$$

By def. \ref{CommutativeHopfAlgebroidComodule} and prop. \ref{IndeedComoduleStructureOnEX} this is the image under foming [[stable homotopy groups]] $\pi_\bullet(-)$ of the following diagram in $Ho(Spectra)$:

$$
  \array{
    E \wedge X
      &\overset{id \wedge f}{\longrightarrow}&
    E \wedge Y
    \\
    {}^{\mathllap{\simeq}}\downarrow
      &&
    \downarrow^{\mathrlap{\simeq}}
    \\
    E \wedge \mathbb{S} \wedge X
      &&
    E \wedge \mathbb{S} \wedge Y
    \\
    {}^{\mathllap{id \wedge e \wedge id}}\downarrow
      &&
    \downarrow^{\mathrlap{id \wedge e \wedge id}}
    \\
    E \wedge E \wedge X
      &\underset{id \wedge id \wedge f}{\longrightarrow}&
    E \wedge E \wedge Y
  }
  \,.
$$

But that this diagram commutes is simply the [[functor|functoriality]] of the derived [[smash product of spectra]] as a functor on the [[product category]] $Ho(Spectra) \times Ho(Spectra)$.

=--



+-- {: .num_prop #AdamsUCT}
###### Proposition

Let $(E, \mu, e)$ be a [[homotopy commutative ring spectrum]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyCommutativeRingSpectrum)), and let $X, Y \in Ho(Spectra)$ be two [[spectra]] such that $E_\bullet(X)$ is a [[projective module]] over $\pi_\bullet(E)$ (via [this prop.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyGroupsOfHomotopyCommutativeRingSpectrum)).

Then the homomorphism of [[graded abelian groups]]

$$
  \phi_{UC}
  \;\colon\;
  [X, E \wedge Y]_\bullet 
    \stackrel{}{\longrightarrow}
  Hom_{\pi_\bullet(E)}^\bullet(E_\bullet(X), E_\bullet(Y))_\bullet
$$

given by 

$$
  (X \overset{f}{\longrightarrow} E \wedge Y)
  \;\mapsto\;
  \pi_\bullet
  ( E \wedge X 
     \overset{id \wedge f}{\longrightarrow} 
    E \wedge E \wedge Y
     \overset{\mu \wedge id}{\longrightarrow}
    E \wedge Y
  )
$$

is an [[isomorphism]].


=--

([Schwede 12, chapter II, prop. 6.20](#Schwede12))



+-- {: .proof}
###### Proof

First of all we claim that the morphism in question factors as

$$
  \beta
  \;\colon\;
  [X, E \wedge Y]_\bullet
    \overset{\simeq}{\longrightarrow}
  Hom^\bullet_{E Mod}( E \wedge X , E \wedge Y)
    \overset{\pi_\bullet}{\longrightarrow}
  Hom^\bullet_{\pi_\bullet(E)}( E_\bullet(X), E_\bullet(Y) )
  \,,
$$

where 

1. $E Mod = E Mod(Ho(Spectra), \wedge, \mathbb{S})$ denotes the category of [[homotopy module spectra]] over $E$ ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyCommutativeRingSpectrum))

1. the first morphisms is the [[free-forgetful adjunction]] isomorphism for forming [[free modules|free]] ([prop.](Introduction+to+Stable+homotopy+theory+--+1-2#MonoidModuleOverItself)) $E$-[[homotopy module spectra]] 

1. the second morphism is the respective component of the composite of the [[forgetful functor]] from $E$-[[homotopy module spectra]] back to $Ho(Spectra)$ with the functor $\pi_\bullet$ that forms [[stable homotopy groups]].

This is because (by [this prop.](Introduction+to+Stable+homotopy+theory+--+1-2#MonoidModuleOverItself)) the first map is given by first smashing with $E$ and then postcomposing with the $E$-action on the free module $E \wedge X$, which is the pairing $E \wedge E \overset{\mu}{\to} E$ ([prop.](Introduction+to+Stable+homotopy+theory+--+1-2#MonoidModuleOverItself)). 

Hence it is sufficient to show that the morphism on the right is an isomorphism.

We show more generally that for $N_1, N_2$ any two $E$-[[homotopy module spectra]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyCommutativeRingSpectrum)) such that $\pi_\bullet(N_1)$ is a [[projective module]] over $\pi_\bullet(E)$, then

$$
  Hom^\bullet_{E Mod}( N_1 , N_2)
    \overset{\pi_\bullet}{\longrightarrow}
  Hom^\bullet_{\pi_\bullet(E)}( \pi_\bullet(N_1), \pi_\bullet(N_2) )
$$

is an isomorphism.


To see this, first consider the case that $\pi_\bullet(N_1)$ is in fact a $\pi_\bullet(E)$-[[free module]].

This implies that there is a basis $\mathcal{B} = \{x_i\}_{i \in I}$ and a homomorphism

$$
  \underset{i \in I}{\vee}
  \Sigma^{\vert x_i\vert} 
    E \longrightarrow 
  N_1
$$ 

of $E$-[[homotopy module spectra]], such that this is a [[stable weak homotopy equivalence]].

Observe that this sits in a [[commuting diagram]] of the form

$$
  \array{
    Hom^\bullet_{E Mod}( \underset{i \in I}{\vee} \Sigma^{\vert x_i\vert} E, N_2 )
     &\overset{\pi_\bullet}{\longrightarrow}&
    Hom^\bullet_{\pi_\bullet(E)}(\pi_\bullet(\underset{i \in I}{\vee}\Sigma^{\vert x_i\vert} E) , \pi_\bullet(N_2) )
    \\
    {}^{\mathllap{\simeq}}\downarrow
      &&
    \downarrow^{\mathrlap{\simeq}}
    \\
    \underset{i \in I}{\prod} [ \Sigma^{\vert x_i\vert}\mathbb{S}, N_2 ]_\bullet
     &\underset{\simeq}{\longrightarrow}&
    \underset{i \in I}{\prod}
    \pi_{\bullet + \vert x_i \vert}(N_2)
  }
$$

where

1. the left vertical isomorphism exhibits [[wedge sum]] of spectra as the [[coproduct]] in the [[stable homotopy category]] ([lemma](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyCategoryHasCoproducts));

1. the bottom isomorphism is from [this prop.](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyGrouspAsHomsOutOfSphereSpectrum);

1. the right vertical isomorphism is that of the [[free-forgetful adjunction]] for modules over $\pi_\bullet(E)$.

Hence the top horizontal morphism is an isomorphism, which was to be shown.

Now consider the general case that $\pi_\bullet(N_1)$ is a [[projective module]] over $\pi_\bullet(E)$. Since (graded) projective modules are precisely the [[retracts]] of (graded) [[free modules]] ([prop.](projective+module#NProjectiveIFFHomNExact)), there exists a diagram of $\pi_\bullet(E)$-modules of the form

$$
  id
    \;\colon\;
  \pi_\bullet(N_1)
    \longrightarrow
  \pi_\bullet( \underset{i \in I}{\vee} \Sigma^{\vert x_i \vert} E )
    \longrightarrow
  \pi_\bullet(N_1)
$$

which induces the corresponding [[split idempotent]] of $\pi_\bullet(E)$-modules

$$
  \pi_\bullet( \underset{i \in I}{\vee} \Sigma^{\vert x_i \vert} E )
    \longrightarrow
  \pi_\bullet(N_1)
     \longrightarrow
  \pi_\bullet( \underset{i \in I}{\vee} \Sigma^{\vert x_i \vert} E )
  \,.
$$


As before, by freeness this is actually the image under $\pi_\bullet$ of an idempotent of [[homotopy ring spectra]]

$$
  e_\bullet
    \;\colon\;
  \underset{i \in I}{\vee} \Sigma^{\vert x_i \vert} E
    \longrightarrow
  \underset{i \in I}{\vee} \Sigma^{\vert x_i \vert} E
$$

and so in particular of [[spectra]].

Now in the [[stable homotopy category]] $Ho(Spectra)$ all [[split idempotent|idempotents split]] ([prop.](split+idempotent#InTrinagulatedCategoryWithDirectSumsOfTrianglesAllIdempotentsSplit)), hence there exists a diagram of spectra of the form

$$
  e
  \;\colon\;
  \underset{i \in I}{\vee} \Sigma^{\vert x_i \vert} E
    \longrightarrow
   X
     \longrightarrow
  \underset{i \in I}{\vee} \Sigma^{\vert x_i \vert} E
$$

with $\pi_\bullet(e) = e_\bullet$.

Consider the composite

$$
  X 
    \longrightarrow
  \underset{i \in I}{\vee} \Sigma^{\vert x_i \vert} E
    \longrightarrow
  N_1
  \,.  
$$

Since $\pi_\bullet(e) = e_\bullet$ it follows that under $\pi_\bullet$ this is an isomorphism, then that $X \simeq N_1$ in the [[stable homotopy category]].

In conclusion this exhibits $N_1$ as a [[retract]] of an free $E$-homotopy module spectrum

$$
  id
    \;\colon\;
  N_1 
    \longrightarrow 
  \underset{i \in I}{\vee} \Sigma^{\vert x_i \vert} E
    \longrightarrow
  N_1
  \,,
$$

hence of a spectrum for which the morphism in question is an isomorphism.
 Since the morphism in question is [[natural transformation|natural]], its value on $N_1$ is a retract in the [[arrow category]] of an isomorphism, hence itself an isomorphism ([lemma](Introduction+to+Stable+homotopy+theory+--+P#RetractPreservesIsomorphism)).

=--

+-- {: .num_remark}
###### Remark

A stronger version of the statement of prop. \ref{AdamsUCT}, with the free homotopy $E$-module spectrum $E \wedge Y$ replaced by any homotopy $E$-module spectrum $F$, is considered in ([Adams 74, chapter III, prop. 13.5](#Adams74)) ("[[universal coefficient theorem]]"). Strong conditions are considered that ensure that

$$
  F^\bullet(X) = [X,F]_\bullet
    \longrightarrow 
  Hom^\bullet_{\pi_\bullet(E)}(E_\bullet(X), \pi_\bullet(F))
$$

is an isomormphism (expressing the $F$-cohomology of $X$ as the $\pi_\bullet(E)$-linear dual of the $E$-homology of $X$).

For the following we need only the weaker but much more general statement of prop. \ref{AdamsUCT}, and in fact this is all that ([Adams 74, p. 323](#Adams74)) ends up using, too.


=--


With this we finally get the following statement, which serves to identify maps of certain spectra with their induced maps on $E$-homology:


+-- {: .num_prop #ComoduleHomForENCohomology}
###### Proposition

Let $(E, \mu, e)$ be a [[homotopy commutative ring spectrum]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyCommutativeRingSpectrum)), and let $X, Y \in Ho(Spectra)$ be two [[spectra]] such that 

1. $E$ is flat according to def. \ref{FlatE};

1. $E_\bullet(X)$ is a [[projective module]] over $\pi_\bullet(E)$ (via [this prop.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyGroupsOfHomotopyCommutativeRingSpectrum)).


Then the morphism from lemma \ref{SmashingMapsWithEFactorsThroughSteenrodComoduleHomomorphisms} 

$$
 [X, E \wedge Y]_\bullet 
   \stackrel{\pi_\bullet(E \wedge -)}{\longrightarrow}
  Hom_{E_\bullet(E)}^\bullet(E_\bullet(X), E_\bullet( E \wedge Y)))
   \simeq
  Hom_{E_\bullet(E)}^\bullet(E_\bullet(X),  E_\bullet(E) \otimes_{\pi_\bullet(E)} E_\bullet(Y) ))
$$

is an [[isomorphism]] (where the isomophism on the right is that of prop. \ref{EnHomology}).

=-- 

([Adams 74, part III, page 323](#Adams74))


+-- {: .proof}
###### Proof

Observe that the following [[commuting diagram|diagram commutes]]:

$$
  \array{
    [X, E \wedge Y]_\bullet
     && \overset{\pi_\bullet(E \wedge -)}{\longrightarrow} &&
    Hom_{E_\bullet(E)}^\bullet(E_\bullet(X),  E_\bullet(E) \otimes_{\pi_\bullet(E)} E_\bullet(Y) ))
    \\
    & {}_{\mathllap{\phi_{UC}}}\searrow 
      && 
    \swarrow_{\mathrlap{\epsilon \otimes id \circ (-) }}
    \\
    &&
    Hom^\bullet_{\pi_\bullet(E)}(E_\bullet(X), E_\bullet(Y))
  }
  \,,
$$

where 

1. the top morphism is the one from lemma \ref{SmashingMapsWithEFactorsThroughSteenrodComoduleHomomorphisms}; 

1. the right vertical morphism is the adjunction isomorphism from prop. \ref{CoFreeComodules};

1. the left diagonal morphism is the one from prop. \ref{AdamsUCT}.

To see that this indeed commutes, notice that 

1. the top morphism sends $(X \overset{f}{\to} E \wedge Y)$ to $E_\bullet(X) \overset{E_\bullet(f)}{\to} E_\bullet(E \wedge Y) \simeq \pi_\bullet(E \wedge E \wedge Y) $ by definition;

1. the right vertical morphism sends this further to $E_\bullet(X) \overset{E_\bullet(f)}{\to} \pi_\bullet(E \wedge E \wedge Y) \overset{\pi_\bullet(\mu \wedge id)}{\to} \pi_\bullet(E \wedge Y)$, by the proof of prop. \ref{CoFreeComodules} (which says that the map is given by postcomposition with the counit of $E_\bullet(E)$) and def. \ref{HopfAlgebroidStructureOnDualEOperations} (which says that this counit is represented by $\mu$);

1. by prop. \ref{AdamsUCT} this is the same as the action of the left diagonal morphism.

But now

1. the right vertical morphism is an isomorphism by prop. \ref{EnHomology};

1. the left diagonal morphism is an isomorphism by prop. \ref{AdamsUCT} 

and so it follows that the top horizontal morphism is an isomorphism, too.


=--


In conclusion:

+-- {: .num_theorem #ComoduleHomsInE1PageOfEAdamsSpectralSequence}
###### Theorem

Let $(E, \mu, e)$ be a [[homotopy commutative ring spectrum]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyCommutativeRingSpectrum)), and let $X, Y \in Ho(Spectra)$ be two [[spectra]] such that 

1. $E$ is flat according to def. \ref{FlatE};

1. $E_\bullet(X)$ is a [[projective module]] over $\pi_\bullet(E)$ (via [this prop.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyGroupsOfHomotopyCommutativeRingSpectrum)).

Then the first page of the $E$-Adams spectral sequence, def. \ref{AdamsEAdamsSpectralSequence}, for $[Y,X]_\bullet$ is isomorphic to the following chain complex of graded homs of [[comodules]] (def. \ref{CommutativeHopfAlgebroidComodule}) over the dual $E$-[[Steenrod algebra]] $(E_\bullet(E), \pi_\bullet(E))$ (prop. \ref{HopfAlgebroidStructureOnDualEOperations}):

$$
  E_1^{s,t}(X,Y)
    \;\simeq\;
  Hom^t_{E_\bullet(E)}(E_\bullet(X), E_{\bullet-s}(A_s))
  \;\;\,,
  \;\;\;\;\;
  d_1 
    \;=\;
  Hom_{E_\bullet(E)}(E_\bullet(X), E_\bullet( g \circ h ))
$$

$\,$


$$
  0 
    \to 
  Hom_{E_\bullet(E)}^t(E_\bullet(X),E_\bullet(A_0))
    \stackrel{d_1}{\longrightarrow}
  Hom_{E_\bullet(E)}^t(
     E_\bullet(X),
     E_{\bullet-1}(A_1)
  )
    \stackrel{d_1}{\longrightarrow}
  Hom_{E_\bullet(E)}^t(
     E_\bullet(X),
     E_{\bullet-2}(A_2)
   )
    \stackrel{d_1}{\longrightarrow}
   \cdots
  \,.
$$

=--

([Adams 74, theorem 15.1 page 323](#Adams74))

+-- {: .proof}
###### Proof

This is prop. \ref{ComoduleHomForENCohomology} applied to def. \ref{AdamsEAdamsSpectralSequence}:

$$
  \begin{aligned}
    E_1^{s,t}(X,Y)
    & =
    [X, \underset{A_s}{\underbrace{E \wedge Y_s}}]_{t-s}
    \\
    & \simeq
    Hom^{t-s}_{E_\bullet(E)}( E_\bullet(X), E_\bullet(\underset{A_s}{\underbrace{E \wedge Y_s}}) )
    \\
    &\simeq 
    Hom^{t}_{E_\bullet(E)}( E_\bullet(X), E_{\bullet-s}(A_s) )
  \end{aligned}
$$

=--



#### The second page
 {#TheE2TermOfTheEAdamsSpectralSequence}


+-- {: .num_theorem #SecondPageOfEAdamsSpectralSequence}
###### Theorem

Let $(E, \mu, e)$ be a [[homotopy commutative ring spectrum]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyCommutativeRingSpectrum)), and let $X, Y \in Ho(Spectra)$ be two [[spectra]] such that 

1. $E$ is flat according to def. \ref{FlatE};

1. $E_\bullet(X)$ is a [[projective module]] over $\pi_\bullet(E)$ (via [this prop.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyGroupsOfHomotopyCommutativeRingSpectrum)).

Then the entries of the second page of the $E$-Adams spectral sequence for $[X,Y]_\bullet$ (def. \ref{AdamsEAdamsSpectralSequence}) are the [[Ext]]-groups of [[commutative Hopf algebroid]]-[[comodules]] (def. \ref{CommutativeHopfAlgebroidComodule}) over the [[commutative Hopf algebroid]] structure on the dual $E$-[[Steenrod algebra]] $E_\bullet(E)$ from prop. \ref{HopfAlgebroidStructureOnDualEOperations}:


$$
  E_2^{s,t}(X,Y)
  \simeq
  Ext^{s,t}_{E_\bullet(E)}(E_\bullet(X), E_\bullet(Y))
  \,.
$$

(On the right $s$ is the degree that goes with any [[Ext]]-functor, and the "internal degree" $t$ is the additional degree of morphisms between graded modules from def. \ref{CommutativeHopfAlgebroidComodule}.) 

In the special case that $X = \mathbb{S}$ is the [[sphere spectrum]], then (by prop. \ref{ComoduleHomInTermsOfCotensorProduct}) these are equivalently [[Cotor]]-groups

$$
  E^{s,t}_2(X,Y)
    \simeq
  Cotor^{s,t}_{E_\bullet(E)}(\pi_\bullet(E), E_\bullet(Y))
  \,.
$$

=--

([Adams 74, theorem 15.1, page 323](#Adams74))

+-- {: .proof}
###### Proof

By theorem \ref{ComoduleHomsInE1PageOfEAdamsSpectralSequence}, under the given assumptions the first page reads

$$
  E_1^{s,t}(X,Y)
    \;\simeq\;
  Hom^t_{E_\bullet(E)}(E_\bullet(X), E_{\bullet-s}(A_s))
  \;\;\,,
  \;\;\;\;\;
  d_1 
    \;=\;
  Hom_{E_\bullet(E)}(E_\bullet(X), E_\bullet( g \circ h ))
$$

$\,$


$$
  0 
    \to 
  Hom_{E_\bullet(E)}^t(E_\bullet(X),E_\bullet(A_0))
    \stackrel{d_1}{\longrightarrow}
  Hom_{E_\bullet(E)}^t(
     E_\bullet(X),
     E_{\bullet-1}(A_1)
  )
    \stackrel{d_1}{\longrightarrow}
  Hom_{E_\bullet(E)}^t(
     E_\bullet(X),
     E_{\bullet-2}(A_2)
   )
    \stackrel{d_1}{\longrightarrow}
   \cdots
  \,.
$$

By remark \ref{TermsOfNextPageOnSpectralSequence} the second page is the [[cochain cohomology]] of this complex. Hence by the standard theory of [[derived functors in homological algebra]] (see the section _[Via acyclic resolutions](derived+functor+in+homological+algebra#ViaAcyclicResolutions)_), it is now sufficient to see that:

1. the category $E_\bullet(E) CoMod$ (def. \ref{CommutativeHopfAlgebroidComodule}, prop. \ref{DualESteenrodAlgebrasIsCommutativeHopfAlgebroid}) is an [[abelian category]] with [[enough injectives]] (so that all [[right derived functors|right]] [[derived functor in homological algebra|derived functors]] on $E_\bullet(E) CoMod$ exist);

1. the first page graded chain complex $(E^{\bullet,t}_1(X,Y), d_1)$ is the image under the [[hom-functor]] $F \coloneqq Hom_{E_\bullet(E)}(E_\bullet(Y),-)$ of an $F$-[[acyclic resolution]] of $E_\bullet(X)$ (so that its cohomology indeed computes the [[Ext]]-derived functor ([theorem](derived+functor+in+homological+algebra#DerivedFFromFInjectiveResolution))).

That $E_\bullet(E) CoMod$ is an [[abelian category]] is lemma \ref{CategoryOfHopfComodulesIsAbelianIfHopfAlgebroidIsFlat} below, and that it has enough injectives is lemma \ref{IfCounitOfHopfAlgebroidIsFlatThenCofreeModulesAreInjective}.

Lemma \ref{ResolutionEWp} below shows that $E_\bullet(A_\bullet)$ is a resolution of $E_\bullet(Y)$ in $E_\bullet(E) CoMod$. By prop. \ref{EnHomology} it is a resolution by cofree comodules (def. \ref{CoFreeComodules}). That these are $F$-acyclic is lemma \ref{CoFreeHopfComodulesAreHomNAcyclicForProjectiveN} below.

=--



##### $E$-Adams resolutions

We discuss that the first page of the $E$-Adams spectral sequence indeed exhibits a [[resolution]] as required by the proof of theorem \ref{SecondPageOfEAdamsSpectralSequence}.


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
     && \overset{E_\bullet(g_0)}{\longrightarrow} &&
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

is a [[long exact sequence]], exhibiting the graded [[chain complex]] $(E_\bullet(A_\bullet), \partial)$ as a [[resolution]] of $E_\bullet(Y)$.

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
  E_\bullet(A_p)
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



##### Homological co-algebra

We discuss basic aspects of [[homological algebra]] in [[categories]] of [[comodules]] (def. \ref{CommutativeHopfAlgebroidComodule}) over [[commutative Hopf algebroids]] (def. \ref{CommutativeHopfAlgebroid}), needed in the proof of theorem \ref{SecondPageOfEAdamsSpectralSequence}.


+-- {: .num_lemma #CategoryOfHopfComodulesIsAbelianIfHopfAlgebroidIsFlat}
###### Lemma

Let $(\Gamma, A)$ be a [[commutative Hopf algebroid]] $\Gamma$ over $A$ (def. \ref{CommutativeHopfAlgebroid}, \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents}), such that the right $A$-module structure on $\Gamma$ induced by $\eta_R$ is a [[flat module]].

Then the [[category]] $\Gamma CoMod$ of [[comodules]] over $\Gamma$ (def. \ref{CommutativeHopfAlgebroidComodule}) is an [[abelian category]].

=--

(e.g. [Ravenel 86, theorem A1.1.3](#Ravenel86)) 

+-- {: .proof}
###### Proof

It is clear that, without any condition on the Hopf algebroid, $\Gamma CoMod$ is an [[additive category]]. 

Next we need to show if $\Gamma$ is flat over $A$, that then this is also a [[pre-abelian category]], in that [[kernels]] and [[cokernels]] exist. 

To that end, let $f \colon (N_1,\Psi_{N_1}) \longrightarrow (N_2,\Psi_{N_2})$ be a morphism of comodules, hence a [[commuting diagram]] in $A$[[Mod]] of the form

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
    \mathllap{\exists}\downarrow 
      && 
    \downarrow^{\mathrlap{\Psi_{N_1}}} 
      && 
    \downarrow^{\mathrlap{\Psi_{N_2}}}
    \\
    \Gamma \otimes_A ker(f) 
      &\longrightarrow& 
    \Gamma \otimes_A N_1
      &\stackrel{id_\Gamma \otimes_A f}{\longrightarrow}&
    \Gamma \otimes_A N_2
  }
  \,.
$$

By the assumption that $\Gamma$ is a [[flat module]] over $A$, also $\Gamma \otimes_A ker(f) \simeq ker(\Gamma \otimes_A f)$ is a [[kernel]]. Hence by the [[universal property]] of kernels and the commutativity of the square o the right, there exists a unique vertical morphism as shown on the left, making the left [[commuting square|square commute]]. This means that the $A$-module $ker(f)$ uniquely inherits the structure of a $\Gamma$-comodule such as to make $ker(f) \to N_1$ a comodule homomorphism. By the same universal property it follows that $ker(f)$ with this comodule structure is in fact the kernel of $f$ in $\Gamma CoMod$.

The argument for the existence of [[cokernels]] proceeds [[formal dual|formally dually]]. Hence $\Gamma CoMod$ is a [[pre-abelian category]].


But it also follows from this construction that the comparison morphism

$$
  coker(ker(f)) \longrightarrow ker(coker(f))
$$

formed in $\Gamma CoMod$ has underlying it the corresponding comparison morphism in $A Mod$. There this is an [[isomorphism]] by the fact that the [[category of modules]] $A Mod$ is an [[abelian category]], hence it is an isomorphism also in $\Gamma CoMod$. So the latter is in fact an [[abelian category]] itself.

=--

+-- {: .num_lemma #IfCounitOfHopfAlgebroidIsFlatThenCofreeModulesAreInjective}
###### Lemma

Let $(\Gamma, A)$ be a [[commutative Hopf algebroid]] $\Gamma$ over $A$ (def. \ref{CommutativeHopfAlgebroid}, \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents}), such that the right $A$-module structure on $\Gamma$ induced by $\eta_R$ is a [[flat module]].

Then

1. every co-free $\Gamma$-[[comodule]] (def. \ref{CoFreeComodules}) on an [[injective module]] over $A$ is an [[injective object]] in $\Gamma CoMod$;

1. $\Gamma CoMod$ has [[enough injectives]] ([def.](injective+object#EnoughInjectives)) if the [[axiom of choice]] holds in the ambient [[set theory]].

=--

(e.g. [Ravenel 86, lemma A1.2.2](#Ravenel86))

+-- {: .proof}
###### Proof

First of all, assuming the [[axiom of choice]], then the [[category of modules]] $A Mod$ has [[enough injectives]] (by [this proposition](injective+object#AbHasEnoughInjectives)).

Now by prop. \ref{CoFreeComodules} we have the [[adjunction]]

$$
  A Mod
    \underoverset
      {\underset{co-free}{\longrightarrow}}
      {\overset{forget}{\longleftarrow}}
      {\bot}
  \Gamma CoMod
  \,.
$$

Observe that the [[left adjoint]] is a [[faithful functor]] (being a [[forgetful functor]]) and that, by the proof of lemma \ref{CategoryOfHopfComodulesIsAbelianIfHopfAlgebroidIsFlat}, it is an [[exact functor]]. This implies that

1. for $I \in A Mod$ an [[injective module]], then the co-free comodule $\Gamma \otimes_A I$ is an [[injective object]] in $\Gamma CoMod$ (by [this lemma](injective+module#RightAdjointsOfExactFunctorsPreserveInjectives));

1. for $N \in \Gamma CoMod$ any object, and for $i \colon forget(N) \hookrightarrow I$ a monomorphism of $A$-modules into an injective $A$-module, then the [[adjunct]] $\tilde i \colon N \hookrightarrow \Gamma\otimes_A I$ is a monomorphism (by [this lemma](injective+object#TransferOfEnoughInjectivesAlongAdjunctions))) hence a monomorpism into an injective comodule, by the previous item.

Hence $\Gamma CoMod$ has enough injective objects ([def.](injective+object#EnoughInjectives)).

=--


+-- {: .num_lemma #CoFreeHopfComodulesAreHomNAcyclicForProjectiveN}
###### Lemma

Let $(\Gamma, A)$ be a [[commutative Hopf algebroid]] $\Gamma$ over $A$ (def. \ref{CommutativeHopfAlgebroid}, \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents}), such that the right $A$-module structure on $\Gamma$ induced by $\eta_R$ is a [[flat module]]. Let $N \in \Gamma CoMod$ be a $\Gamma$-[[comodule]] (def. \ref{CommutativeHopfAlgebroidComodule}) such that the underlying $A$-module is a [[projective module]] (a [[projective object]] in $A$[[Mod]]). 

Then  (assuming the [[axiom of choice]] in the ambient set theory) every co-free comodule (prop. \ref{CoFreeComodules}) is an $F$-[[acyclic object]] for $F$ the [[hom functor]] $Hom_{\Gamma CoMod}(N,-)$.

=--

+-- {: .proof}
###### Proof

We need to show that the [[derived functors in homological algebra|derived functors]] $\mathbb{R}^{\bullet} Hom_{\Gamma}(N,-)$ vanish in positive degree on all co-free comodules, hence on $\Gamma \otimes_A K$, for all $K \in A Mod$. 

To that end, let $I^\bullet$ be an [[injective resolution]] of $K$ in $A Mod$. By lemma \ref{IfCounitOfHopfAlgebroidIsFlatThenCofreeModulesAreInjective} then $\Gamma \otimes_A I^\bullet$ is a sequence of [[injective objects]] in $\Gamma CoMod$ and by the assumption that $\Gamma$ is flat over $A$ it is an [[injective resolution]] of $\Gamma \otimes_A K$ in $\Gamma CoMod$. Therefore the derived functor in question is given by

$$
  \begin{aligned}
    \mathbb{R}^{\bullet \geq 1} Hom_\Gamma(N, \Gamma \otimes_A K)
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




#### Convergence 
 {#Convergence}

We discuss the convergence of $E$-Adams spectral sequences (def. \ref{AdamsEAdamsSpectralSequence}), i.e. the identification of the "limit", in an appropriate sense, of the terms $E_r^{s,t}(X,Y)$ on the $r$th page of the spectral sequence as $r$ goes to infinity.

If an $E$-Adams spectral sequence converges, then it converges not necessarily to the full stable homotopy groups $[X,Y]_\bullet$, but to some [[localization of abelian groups|localization]] of them. This typically means, roughly, that only certain $p$-[[torsion subgroups]] in $[X,Y]_\bullet$ for some [[prime numbers]] $p$ are retained. We give a precise discussion below in _[Localization and adic completion of abelian groups](#LocalizationOfAbelianGroups)_.

If one knows that $[X,Y]_q$ is a [[finitely generated object|finitely generated]] [[abelian group]] (as is the case notably for $\pi_q^s = [\mathbb{S},\mathbb{S}]_q$ by the _[[Serre finiteness theorem]]_) then this allows to recover the full information from its pieces: by the _[[fundamental theorem of finitely generated abelian groups]]_ (prop. \ref{FundamentalTheoremOfFinitelyGeneratedAbelianGroups} below) these groups are [[direct sums]] of powers $\mathbb{Z}^n$ of the [[infinite cyclic group]] $\mathbb{Z}$ with finite [[cyclic groups]] of the form $\mathbb{Z}/p^k \mathbb{Z}$, and so all one needs to compute is the powers $k$ "one prime $p$ at a time". This we review below in _[Primary decomposition of abelian groups](#PrimaryDecompositionOfAbelianGroups)_.

The deeper reason that $E$-Adams spectral sequences tend to converge to [[localization of an abelian group|localizations]] of the abelian groups $[X,Y]_\bullet$ of morphisms of spectra, is that they really converge to (the actual homotopy groups of) [[localizations of spectra]]. This is more than just a reformulation, because the localization at the level of spectra determies the [[filtration]] which controls the nature of the convergence. We discuss this localization of spectra below in _[Localization and nilpotent completion of spectra](#LocalizationOfSpectra)_. 

Then we state convergence properties of $E$-Adams spectral sequences below in _[Convergence statements](#ConvergenceStatements)_.



##### Primary decomposition of abelian groups
 {#PrimaryDecompositionOfAbelianGroups}

An $E$-[[Adams spectral sequence]] _typically_ converges (discussed [below](#ConvergenceStatements)) not to the full [[stable homotopy groups]] $[X,Y]_\bullet$, but just to some piece which on the [[finite group|finite]] [[direct summands]] consists only of [[p-primary groups]] for some [[prime numbers]] $p$ that depend on the nature of the [[homotopy ring spectrum]] $E$ . Here we review basic facts about $p$-primary decomposition of finite abelian groups and introduce their graphical calculus (remark \ref{pprimarygraphical} below) which will allow to read off these $p$-primary pieces from the stable page of the $E$-Adams spectral sequnce.


+-- {: .num_theorem #FundamentalTheoremOfFinitelyGeneratedAbelianGroups}
###### Theorem
**(fundamental theorem of finitely generated abelian groups)**

Every [[finitely generated object|finitely generated]] [[abelian group]] $A$ is [[isomorphism|isomorphic]] to a [[direct sum]] of [[p-primary groups|p-primary]] [[cyclic groups]] $\mathbb{Z}/p^k \mathbb{Z}$ (for $p$ a [[prime number]] and $k$ a [[natural number]] ) and copies of the [[infinite cyclic group]] $\mathbb{Z}$:

$$
  A 
  \;\simeq\;
  \mathbb{Z}^n
   \oplus
  \underset{i}{\bigoplus}
   \mathbb{Z}/p_i^{k_i} \mathbb{Z}
  \,.
$$

The summands of the form  $\mathbb{Z}/p^k \mathbb{Z}$ are also called the _[[p-primary group|p-primary]] components_ of $A$. Notice that the $p_i$ need not all be distinct.

**fundamental theorem of finite abelian groups**:

In particular every [[finite group|finite]] [[abelian group]] is of this form  for $n = 0$, hence is a [[direct sum]] of [[cyclic groups]]. 

**fundamental theorem of cyclic groups**: 

In particular every [[cyclic group]] $\mathbb{Z}/n\mathbb{Z}$ is a [[direct sum]] of cyclic groups of the form

$$
  \mathbb{Z}/n\mathbb{Z}
    \simeq
  \underset{i}{\bigoplus} \mathbb{Z}/ p_i^{k_i} \mathbb{Z}
$$

where all the $p_i$ are distinct and $k_i$ is the maximal power of the [[prime factor]] $p_i$ in the prime decomposition of $n$.

Specifically, for each natural number $d$ dividing $n$ it contains $\mathbb{Z}/d\mathbb{Z}$ as the [[subgroup]] generated by $n/d \in \mathbb{Z}\to \mathbb{Z}/n\mathbb{Z}$. In fact the [[lattice of subgroups]] of $\mathbb{Z}/n\mathbb{Z}$ is the [[formal dual]] of the lattice of natural numbers $\leq n$ ordered by inclusion.



=--

(e.g. [Roman 12, theorem 13.4](#Roman12), [Navarro 03](#Navarro03)) for cyclic groups e.g. ([Aluffi 09, pages 83-84](#Aluffi09))

This is a special case of the _[[ structure theorem for finitely generated modules over a principal ideal domain]]_.



+-- {: .num_example #TwoFiniteGroupsOfOrderp2}
###### Example

For $p$ a [[prime number]], there are, up to [[isomorphism]], two [[abelian groups]] of [[order of a group|order]] $p^2$, namely

$$
  (\mathbb{Z}/p\mathbb{Z}) \oplus (\mathbb{Z}/p\mathbb{Z})
$$

and

$$
  \mathbb{Z}/p^2 \mathbb{Z}
  \,.
$$

=--

+-- {: .num_example}
###### Example

For $p_1$ and $p_2$ two distinct [[prime numbers]], $p_1 \neq p_2$, then there is, up to isomorphism, precisely one [[abelian group]] of order $p_1 p_2$, namely

$$
  \mathbb{Z}/p_1 \mathbb{Z}
  \oplus
  \mathbb{Z}/p_2 \mathbb{Z}
  \,.
$$

This is equivalently the [[cyclic group]] 

$$
  \mathbb{Z}/p_1 p_2 \mathbb{Z}
    \simeq
  \mathbb{Z}/p_1 \mathbb{Z}
    \oplus
  \mathbb{Z}/p_2 \mathbb{Z}
  \,.
$$

The isomorphism is given by sending $1$ to $(p_2,p_1)$.

=--

+-- {: .num_example }
###### Example

Moving up, for two distinct prime numbers $p_1$ and $p_2$, there are exactly two abelian groups of order $p_1^2 p_2$, namely $(\mathbb{Z}/p_1 \mathbb{Z})\oplus (\mathbb{Z}/p_1 \mathbb{Z}) \oplus (\mathbb{Z}/p_2 \mathbb{Z})$ and $(\mathbb{Z}/p_1^2 \mathbb{Z})\oplus (\mathbb{Z}/p_2 \mathbb{Z})$.  The latter is the [[cyclic group]] of order $p_1^2 p_2$.  For instance, $\mathbb{Z}/12\mathbb{Z} \cong (\mathbb{Z}/4 \mathbb{Z})\oplus (\mathbb{Z}/3 \mathbb{Z})$.

=--


+-- {: .num_example}
###### Example

Similarly, there are four abelian groups of order $p_1^2 p_2^2$, three abelian groups of order $p_1^3 p_2$, and so on.

More generally, theorem \ref{FundamentalTheoremOfFinitelyGeneratedAbelianGroups} may be used to compute exactly how many abelian groups there are of any finite [[order of a group|order]] $n$ (up to [[isomorphism]]): write down its [[prime factorization]], and then for each prime power $p^k$ appearing therein, consider how many ways it can be written as a product of positive powers of $p$.  That is, each [[partition]] of $k$ yields an abelian group of order $p^k$.  Since the choices can be made independently for each $p$, the numbers of such partitions for each $p$ are then multiplied.

Of all these abelian groups of order $n$, of course, one of them is the [[cyclic group]] of order $n$.  The fundamental theorem of cyclic groups says it is the one that involves the one-element partitions $k= [k]$, i.e. the cyclic groups of order $p^k$ for each $p$.

=--

+-- {: .num_remark #PrimaryDecompositionGraphicalRepresentation}
###### Remark
**(graphical representation of $p$-primary decomposition)**


Theorem \ref{FundamentalTheoremOfFinitelyGeneratedAbelianGroups} says that for any [[prime number]] $p$, the [[p-primary group|p-primary part]] of any finitely generated abelian group is determined uniquely up to [[isomorphism]] by

* a total number $k \in \mathbb{N}$ of powers of $p$;

* a [[partition]] $k = k_1 + k_2 + \cdots + k_q$.

The corresponding [[p-primary group]] is

$$
  \underoverset{i = 1}{q}{\bigoplus} \mathbb{Z}/p^{k_i} \mathbb{Z}
  \,.
$$ 

In the context of [[Adams spectral sequences]] it is conventional to depict this information graphically by

* $k$ dots;

* of which sequences of length $k_i$ are connected by vertical lines, for $i \in \{1, \cdots, q\}$.

For example the graphical representation of the $p$-primary group

$$
  \mathbb{Z}/p\mathbb{Z} 
    \oplus 
  \mathbb{Z}/p\mathbb{Z}
    \oplus 
  \mathbb{Z}/p^3 \mathbb{Z}
    \oplus
  \mathbb{Z}/p^4\mathbb{Z}
$$

is

$$
  \array{
      &&& \bullet
      \\
      && & \vert
      \\
      && \bullet & \bullet
      \\
      && \vert & \vert
      \\
      && \bullet & \bullet
      \\
      && \vert & \vert
      \\
     \bullet & \bullet & \bullet & \bullet
  }
  \,.
$$

This notation comes from the convention of drawing stable pages of [[multiplicative spectral sequence|multiplicative]] [[Adams spectral sequences]] and reading them as encoding the [extension problem](Introduction+to+Stable+homotopy+theory+--+S#ExtensionProblemForSpectralSequences) for computing the homotopy groups that the spectral sequence converges to:

* a dot at the top of a vertical sequence of dots denotes the group $\mathbb{Z}/p\mathbb{Z}$;

* inductively, a dot vetically below a sequence of dots denotes a [[group extension]] of $\mathbb{Z}/p\mathbb{Z}$ by the group represented by the sequence of dots above;

* a vertical line between two dots means that the generator of the group corresponding to the upper dot is, regarded after inclusion into the group extension, the product by $p$ of the generator of the group corresponding to the lower dot, regarded as represented by the generator of the group extension.

So for instance

$$
  \array{
    \bullet
    \\
    \vert
    \\
    \bullet
  }
$$

stands for an [[abelian group]] $A$ which forms a [[group extension]] of the form

$$
  \array{
    \mathbb{Z}/p\mathbb{Z}
    \\
    \downarrow
    \\
    A
    \\
    \downarrow
    \\
    \mathbb{Z}/p\mathbb{Z}
  }
$$

such that multiplication by $p$ takes the generator of the bottom copy of $\mathbb{Z}/p\mathbb{Z}$, regarded as represented by the generator of $A$, to the generator of the image of the top copy of $\mathbb{Z}/p\mathbb{Z}$.

This means that of the two possible choices of extensions (by example \ref{TwoFiniteGroupsOfOrderp2}) $A$ corresponds to the non-trivial extension $A = \mathbb{Z}/p^2\mathbb{Z}$. Because then in

$$
  \array{
    \mathbb{Z}/p\mathbb{Z} & 
    \\
    \downarrow
    \\
    \mathbb{Z}/p^2 \mathbb{Z} & 
    \\
    \downarrow
    \\
    \mathbb{Z}/p\mathbb{Z} & 
  }
$$

the image of the generator 1 of the first group in the middle group is $p = p \cdot 1$.

Conversely, the notation


$$
  \array{
    \bullet
    \\
    \\
    \bullet
  }
$$

stands for an [[abelian group]] $A$ which forms a [[group extension]] of the form

$$
  \array{
    \mathbb{Z}/p\mathbb{Z}
    \\
    \downarrow
    \\
    A
    \\
    \downarrow
    \\
    \mathbb{Z}/p\mathbb{Z}
  }
$$

such that multiplication by $p$ of the generator of the top group in the middle group does _not_ yield the generator of the bottom group. 

This means that of the two possible choices (by example \ref{TwoFiniteGroupsOfOrderp2}) $A$ corresponds to the _trivial_ extension $A = \mathbb{Z}/p\mathbb{Z} \oplus \mathbb{Z}/p\mathbb{Z}$. Because then in

$$
  \array{
    \mathbb{Z}/p\mathbb{Z}
    \\
    \downarrow
    \\
    \mathbb{Z}/p\mathbb{Z} 
      \oplus
    \mathbb{Z}/p\mathbb{Z}
    \\
    \downarrow
    \\
    \mathbb{Z}/p\mathbb{Z}
  }
$$

the generator 1 of the top group maps to the element $(1,0)$ in the middle group, and multiplication of that by $p$ is $(0,0)$ instead of $(0,1)$, where the latter is the generator of the bottom group.

Similarly 

$$
  \array{
    \bullet
    \\
    \vert
    \\
    \bullet
    \\
    \vert
    \\
    \bullet
  }
$$

is to be read as the result of appending to the previous case a dot _below_, so that this now indicates a group extension of the form

$$
  \array{
    \mathbb{Z}/p^2 \mathbb{Z}
    \\
    \downarrow
    \\
    A
    \\
    \downarrow
    \\
    \mathbb{Z}/p \mathbb{Z}
  }
$$

such that $p$-times the generator of the bottom group, regarded as represented by the generator of the middle group, is the image of the generator of the top group. This is again the case for the unique non-trivial extension, and hence in this case the diagram stands for $A = \mathbb{Z}/p^3 \mathbb{Z}$.

And so on.



For example the stable page of the $\mathbb{F}_2$-[[classical Adams spectral sequence]] for computation of the [[p-primary group|2-primary part]] of the [[stable homotopy groups of spheres]] $\pi_{t-s}(\mathbb{S})$  has in ("internal") degree $t-s \leq 13$ the following non-trivial entries:

<img src="http://ncatlab.org/nlab/files/ClassicalAdamsSpectralSequence.jpg" width="600" >

(graphics taken from ([[Symmetric spectra|Schwede 12]]))

Ignoring here the diagonal lines (which denote multiplication by the element $h_1$ that encodes the additional [[ring]] structure on $\pi_\bullet(\mathbb{S})$ which here we are not concerned with) and applying the above prescription, we read off for instance that $\pi_3(\mathbb{S}) \simeq \mathbb{Z}/8\mathbb{Z}$ (because all three dots are connected) while $\pi_8(\mathbb{S}) \simeq \mathbb{Z}/2\mathbb{Z}\oplus \mathbb{Z}/2\mathbb{Z} $ (because here the two dots are not connected). In total

| $k =$ | 0 | 1 | 2 | 3 | 4  | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 | 13 | 
|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|
| $\pi_k(\mathbb{S})_{(2)} = $ | $\mathbb{Z}_{(2)}$  | $\mathbb{Z}/2$  |  $\mathbb{Z}/2$ |  $\mathbb{Z}/8$ |  $0$ |  $0$ | $\mathbb{Z}/2$ |   $\mathbb{Z}/16$ | $(\mathbb{Z}/2)^2$ |  $(\mathbb{Z}/2)^3$ | $\mathbb{Z}/2$ | $\mathbb{Z}/8$ | $0$ | $0$ | 

Here the only entry that needs further explanation is the one for $k = 0$. We discuss the relevant concepts for this below in the section _[Localization and adic completion of abelian groups](#LocalizationOfAbelianGroups)_, but for completeness, here is the quick idea:

The symbol $\mathbb{Z}_{(2)}$ refers to the [[p-adic integers|2-adic integers]] (def. \ref{pAdicIntegers}), i.e. for the [[limit]] of abelian groups

$$
  \mathbb{Z}_{(2)}
  = 
  \underset{\longleftarrow}{\lim}_{n \geq 1} \mathbb{Z}/2^n \mathbb{Z}
$$

This is not [[p-primary group|2-primary]], but it does arise when applying [[p-adic completion|2-adic completion]] of abelian groups (def. \ref{AdicCompletionOfAbelingGroups}) to finitely generated abelian groups as in theorem \ref{FundamentalTheoremOfFinitelyGeneratedAbelianGroups}. The 2-adic integers is the abelian group associated to the diagram

$$
  \array{
    \vdots
    \\
    \vert
    \\    
    \bullet
    \\
    \vert
    \\
    \bullet
    \\
    \vert
    \\
    \bullet
    \\
    \vert
    \\
    \bullet
  }
$$

as in the above figure. Namely by the above prescrption, this infinite sequence should encode an abelian group $A$ such that it is an [[group extension|extension]] of $\mathbb{Z}/p\mathbb{Z}$ by itself of the form

$$
  0 \to A \overset{p \cdot(-)}{\longrightarrow} A \longrightarrow \mathbb{Z}/p\mathbb{Z}
$$

(Because it is supposed to encode an extension of $\mathbb{Z}/p\mathbb{Z}$ by the group corresponding to the result of chopping off the lowest dot, which however in this case does not change the figure.)

Indeed, by lemma \ref{pAdicIntegersAspExtensionofFpByThemselves} below we have a short exact sequence

$$
  0 
    \to
  \mathbb{Z}_{(p)}
    \overset{p \cdot (-)}{\longrightarrow}
  \mathbb{Z}_{(p)}
    \longrightarrow
  \mathbb{Z}/p\mathbb{Z}
    \to
  0
  \,.
$$

=--


##### Localization and adic completion of abelian groups
  {#LocalizationOfAbelianGroups}

+-- {: .num_remark #ExtAb}
###### Remark

Recall that [[Ext]]-groups $\Ext^\bullet(A,B)$ between [[abelian groups]] $A, B \in $ [[Ab]] are concentrated in degrees 0 and 1 ([prop.](free+resolution#AbelianGroupHasFreeResolutionOfLength2)). Since

$$
  Ext^0(A,B) \simeq Hom(A,B)
$$

is the plain [[hom-functor]], this means that there is only one possibly non-vanishing Ext-group $Ext^1$, therefore often abbreviated to just "$Ext$":

$$
  Ext(A,B)
   \coloneqq
  Ext^1(A,B)
  \,.
$$

=--


+-- {: .num_defn #AbelianGroupLocal}
###### Definition

Let $K$ be an [[abelian group]]. 

Then an [[abelian group]] $A$ is called **$K$-local** if all the [[Ext]]-groups from $K$ to $A$ vanish:

$$
  Ext^\bullet(K,A) \simeq 0
$$

hence equivalently (remark \ref{ExtAb}) if

$$
  Hom(K,A) \simeq 0
  \;\;\;\;\;
    and
  \;\;\;\;\;
  Ext(K,A) \simeq 0
  \,.
$$

A [[homomorphism]] of abelian groups $f \colon B \longrightarrow C$ is called **$K$-local** if for all $K$-local groups $A$ the function

$$
  Hom(f,A) \;\colon\; Hom(B,A) \longrightarrow Hom(A,A)
$$

is a [[bijection]]. 

> (**Beware** that here it would seem more natural to use $Ext^\bullet$ instead of $Hom$, but we do use $Hom$. See ([Neisendorfer 08, remark 3.2](localization+of+abelian+groups#Neisendorfer08)).

A homomorphism of abelian groups

$$
  \eta \;\colon\; A \longrightarrow L_K A
$$

is called a **$K$-localization** if

1. $L_K A$ is $K$-local;

1. $\eta$ is a $K$-local morphism.

=--

We now discuss two classes of examples of localization of abelian groups

1. _[Classical localization at/away from primes](#ClassicalLocalizationOfAbelianGroups)_;

1. _[Formal completion at primes](#FormalCompletionOfAbelianGroups)_.

$\,$

**Classical localization at/away from primes**
 {#ClassicalLocalizationOfAbelianGroups}


For $n \in \mathbb{N}$, write $\mathbb{Z}/n\mathbb{Z}$ for the [[cyclic group]] of [[order of a group|order]] $n$.


+-- {: .num_lemma #OutOfCyclicGroupExt1}
###### Lemma

For $n \in \mathbb{N}$ and $A \in Ab$ any [[abelian group]], then 

1. the [[hom-object|hom-group]] out of $\mathbb{Z}/n\mathbb{Z}$ into $A$ is the $n$-[[torsion subgroup]] of $A$

   $$
     Hom(\mathbb{Z}/n\mathbb{Z}, A) 
       \simeq 
     \{
       a \in A \;\vert\; p \cdot a = 0
     \}
   $$

1. the first [[Ext]]-group out of $\mathbb{Z}/n\mathbb{Z}$ into $A$ is

   $$
     Ext^1(\mathbb{Z}/n\mathbb{Z},A)
       \simeq
     A/n A
     \,.
   $$

=--

+-- {: .proof}
###### Proof

Regarding the first item: Since $\mathbb{Z}/p\mathbb{Z}$ is generated by its element 1 a morphism $\mathbb{Z}/p\mathbb{Z} \to A$ is fixed by the image $a$ of this element, and the only relation on 1 in $\mathbb{Z}/p\mathbb{Z}$ is that $p \cdot 1 = 0$.

Regarding the second item:

Consider the canonical [[free resolution]]

$$
  0 \to \mathbb{Z} \overset{p \cdot (-)}{\longrightarrow} \mathbb{Z} \longrightarrow \mathbb{Z}/p\mathbb{Z} \to 0
  \,.
$$

By the general discusson of [[derived functors in homological algebra]] this exhibits the [[Ext]]-group in degree 1 as part of the following [[short exact sequence]]

$$
  0
  \to
  Hom(\mathbb{Z},A)
  \overset{Hom(n\cdot(-),A)}{\longrightarrow}
  Hom(\mathbb{Z}, A)
  \longrightarrow
  Ext^1(\mathbb{Z}/n\mathbb{Z},A)
  \to 0
  \,,
$$

where the morphism on the left is equivalently $A \overset{n \cdot (-)}{\to} A$.

=--

+-- {: .num_example}
###### Example

An [[abelian group]] $A$ is $\mathbb{Z}/p\mathbb{Z}$-local precisely if the operation 

$$
  p \cdot (-)
  \;\colon\;
  A \longrightarrow A
$$

of multiplication by $p$ is an [[isomorphism]], hence if "$p$ is invertible in $A$".

=--

+-- {: .proof}
###### Proof

By the first item of lemma \ref{OutOfCyclicGroupExt1} we have

$$
  Hom(\mathbb{Z}/p\mathbb{Z}, A) 
    \simeq 
  \{
    a \in A \;\vert\; p \cdot a = 0
  \}
$$

By the second item of lemma \ref{OutOfCyclicGroupExt1} we have

$$
  Ext^1(\mathbb{Z}/p\mathbb{Z},A)
    \simeq
  A/p A
  \,.
$$

Hence by def. \ref{AbelianGroupLocal} $A$ is $\mathbb{Z}/p\mathbb{Z}$-local precisely if 

$$
  \{
    a \in A \;\vert\; p \cdot a = 0
  \}
  \simeq
  0
$$

and if

$$
  A / p A \simeq 0
  \,.
$$

Both these conditions are equivalent to multiplication by $p$ being invertible.


=--

+-- {: .num_defn #InvertingPrimes}
###### Definition

For $J \subset \mathbb{N}$ a set of [[prime numbers]], consider the [[direct sum]] $\underset{p \in J}{\oplus} \mathbb{Z}/p\mathbb{Z}$ of [[cyclic groups]] of [[order of a group|order]] $p$.

The operation of $\underset{p \in J}{\otimes} \mathbb{Z}/p\mathbb{Z}$-localization of abelian groups according to def. \ref{AbelianGroupLocal} is called **inverting the primes** in $J$.

Specifically 

1. for $J = \{p\}$ a single prime then $\mathbb{Z}/p\mathbb{Z}$-localization is called **localization away from $p$**;

1. for $J$ the set of all primes except $p$ then $\underset{p \in J}{\otimes} \mathbb{Z}/p\mathbb{Z}$-localization is called **localization at $p$;

1. for $J$ the set of all primes, then $\underset{p \in J}{\otimes} \mathbb{Z}/p\mathbb{Z}$-localizaton is called **[[rationalization]]**..

=--

+-- {: .num_defn #LocalizationOfIntegersAtSetOfPrimes}
###### Definition

For $J \subset Primes \subset \mathbb{N}$ a [[set]] of [[prime numbers]], then 

$$
  \mathbb{Z}[J^{-1}]
    \hookrightarrow
  \mathbb{Q} 
$$

denotes the [[subgroup]] of the [[rational numbers]] on those elements which have an expression as a fraction of natural numbers with denominator a product of elements in $J$.

This is the abelian group underlying the [[localization of a commutative ring]] of the ring of integers at the set $J$ of primes.

If $J = Primes - \{p\}$ is the set of all primes _except_ $p$ one also writes

$$
  \mathbb{Z}_{(p)}
    \coloneqq
  \mathbb{Z}[Primes - \{p\}]
  \,.
$$

Notice the parenthesis, to distinguish from the notation $\mathbb{Z}_{p}$ for the [[p-adic integers]] (def. \ref{pAdicIntegers} below).

=--




+-- {: .num_remark #ClassicalLocalizationSeenFromSpecZ}
###### Remark

The terminology in def. \ref{InvertingPrimes} is motivated by the following perspective of [[arithmetic geometry]]:

Generally for $R$ a [[commutative ring]], then an $R$-[[module]] is equivalently a [[quasicoherent sheaf]] on the [[spectrum of a commutative ring|spectrum of the ring]] $Spec(R)$.

In the present case $R = \mathbb{Z}$ is the [[integers]] and [[abelian groups]] are identified with $\mathbb{Z}$-modules. Hence we may think of an abelian group $A$ equivalently as a [[quasicoherent sheaf]] on [[Spec(Z)]]. 

The "[[ring of functions]]" on [[Spec(Z)]] is the integers, and a point in $Spec(\mathbb{Z})$ is labeled by a [[prime number]] $p$, thought of as generating the ideal of functions on [[Spec(Z)]] which vanish at that point. The [[residue field]] at that point is $\mathbb{F}_p = \mathbb{Z}/p\mathbb{Z}$.

Inverting a prime means [[forcing]] $p$ to become invertible, which, by this characterization, it is precisely _away_ from that point which it labels. The localization of an abelian group at $\mathbb{Z}/p\mathbb{Z}$ hence corresponds to the restriction of the corresponding quasicoherent sheaf over $Spec(\mathbb{Z})$ to the complement of the point labeled by $p$.

Similarly localization _at_ $p$ is localization away from all points except $p$.

See also at _[[function field analogy]]_ for more on this.

=--

+-- {: .num_prop}
###### Proposition


For $J \subset \mathbb{N}$ a set of [[prime numbers]], a homomorphism of abelian groups $f \;\colon\; A \lookrightarrow B $ is local (def. \ref{AbelianGroupLocal}) with respect to  $\underset{p \in J}{\oplus} \mathbb{Z}/p\mathbb{Z}$ (def. \ref{InvertingPrimes}) if under [[tensor product of abelian groups]] with $\mathbb{Z}[J^{-1}]$ (def. \ref{LocalizationOfIntegersAtSetOfPrimes}) it becomes an [[isomorphism]]

$$
  f \otimes \mathbb{Z}[J^{-1}]
    \;\colon\;
  X \otimes \mathbb{Z}[J^{-1}]
    \overset{\simeq}{\longrightarrow}
  Y \otimes \mathbb{Z}[J^{-1}]
  \,.
$$

Moreover, for $A$ any abelian group then its $\underset{p \in J}{\oplus} \mathbb{Z}/p\mathbb{Z}$-localization exists and is given by the canonical projection morphism

$$
  A 
    \longrightarrow
  A \otimes \mathbb{Z}[J^{-1}]
  \,.
$$ 

=--

(e.g. [Neisendorfer 08, theorem 4.2](localization+of+abelian+groups#Neisendorfer08))


$\,$

**Formal completion at primes**
 {#FormalCompletionOfAbelianGroups}

We have seen above in remark \ref{ClassicalLocalizationSeenFromSpecZ} that classical localization of abelian groups at a prime number is geometrically interpreted as restricting a [[quasicoherent sheaf]] over [[Spec(Z)]] to a single point, the point that is labeled by that prime number.

Alternatively one may restrict to the "infinitesimal neighbourhood" of such a point. Technically this is called the _[[formal neighbourhood]]_, because its ring of functions is, by definition, the ring of [[formal power series]] (regarded as an [[adic ring]] or [[pro-ring]]). The corresponding operation on abelian groups is accordingly called _[[formal completion]]_ or _[[adic completion]]_ or just _completion_, for short, of abelian groups.

It turns out that if the abelian group is [[finitely generated object|finitely generated]] then the operation of [[p-completion]] coincides with an operation of _localization_ in the sense of def. \ref{AbelianGroupLocal}, namely localization at the [[p-primary group|p-primary component]] $\mathbb{Z}(p^\infty)$ of the group $\mathbb{Q}/\mathbb{Z}$ (def. \ref{ZpInfinity} below). On the one hand this equivalence is useful for deducing some key properties of [[p-completion]], this we discuss below. On the other hand this situation is a shadow of the relation between [[localization of spectra]] and [[nilpotent completion of spectra]], which is important for characterizing the convergence properties of [[Adams spectral sequences]].


+-- {: .num_defn #AdicCompletionOfAbelingGroups}
###### Definition

For $p$ a [[prime number]], then the **[[p-adic completion]]** of an [[abelian group]] $A$ is the abelian group given by the [[limit]]

$$
  A^\wedge_p
   \coloneqq
  \underset{\longleftarrow}{\lim}
  \left(
    \cdots
      \longrightarrow
    A / p^3 A
      \longrightarrow
    A / p^2 A
      \longrightarrow
    A/p A
  \right)
  \,,
$$

where the morphisms are the evident [[quotient]] morphisms. With these understood we often write

$$
  A^\wedge_p \coloneqq \underset{\longleftarrow}{\lim}_n A/p^n A
$$

for short. Notice that here the indexing starts at $n = 1$.

=--

+-- {: .num_example #pAdicIntegers}
###### Example

The [[p-adic completion]] (def. \ref{AdicCompletionOfAbelingGroups}) of the [[integers]] $\mathbb{Z}$ is called the **[[p-adic integers]]**, often written

$$
  \mathbb{Z}_p
    \coloneqq
  \mathbb{Z}^\wedge_p
    \coloneqq
  \underset{\longleftarrow}{\lim}_n \mathbb{Z}/p^n \mathbb{Z}
  \,,
$$

which is the original example that gives the general concept its name. 

With respect to the canonical [[ring]]-structure on the integers, of course $p \mathbb{Z}$ is a prime ideal. 

Compare this to the ring $\mathcal{O}_{\mathbb{C}}$ of [[holomorphic functions]] on the [[complex plane]]. For $x \in \mathbb{C}$ any point, it contains the prime ideal generated by $(z-x)$ (for $z$ the canonical [[coordinate]] function on $\mathbb{z}$). The [[formal power series ring]] $\mathbb{C}[ [(z.x)] ]$ is the [[adic completion]] of $\mathcal{O}_{\mathbb{C}}$ at this ideal. It has the interpretation of functions defined on a [[formal neighbourhood]] of $X$ in $\mathbb{C}$.

Analogously, the [[p-adic integers]] $\mathbb{Z}_p$ may be thought of as the functions defined on a [[formal neighbourhood]] of the point labeled by $p$ in [[Spec(Z)]].

=--


+-- {: .num_lemma #pAdicIntegersAspExtensionofFpByThemselves}
###### Lemma

There is a [[short exact sequence]]

$$
  0 
    \to
  \mathbb{Z}_p
    \overset{p \cdot (-)}{\longrightarrow}
  \mathbb{Z}_p
    \longrightarrow
  \mathbb{Z}/p\mathbb{Z}
    \to
  0
  \,.
$$

=--

+-- {: .proof}
###### Proof

Consider the following [[commuting diagram]]

$$
  \array{
     \vdots && \vdots && \vdots
     \\
     \downarrow
       &&
     \downarrow
       &&
     \downarrow
     \\
     \mathbb{Z}/p^3\mathbb{Z}
       &\overset{p\cdot (-)}{\longrightarrow}&
     \mathbb{Z}/p^4 \mathbb{Z}
       &\longrightarrow&
     \mathbb{Z}/p\mathbb{Z}
     \\
     \downarrow
       &&
     \downarrow
       &&
     \downarrow
     \\
     \mathbb{Z}/p^2\mathbb{Z}
       &\overset{p\cdot (-)}{\longrightarrow}&
     \mathbb{Z}/p^3 \mathbb{Z}
       &\longrightarrow&
     \mathbb{Z}/p\mathbb{Z}
     \\
     \downarrow
       &&
     \downarrow
       &&
     \downarrow
     \\
     \mathbb{Z}/p\mathbb{Z}
       &\overset{p\cdot (-)}{\longrightarrow}&
     \mathbb{Z}/p^2 \mathbb{Z}
       &\longrightarrow&
     \mathbb{Z}/p\mathbb{Z}
     \\
     \downarrow
       &&
     \downarrow
       &&
     \downarrow
     \\
     0
       &\longrightarrow&
     \mathbb{Z}/p\mathbb{Z}
       &\longrightarrow&
     \mathbb{Z}/p\mathbb{Z}     
  }
  \,.
$$

Each horizontal sequence is exact. Taking the [[limit]] over the vertical sequences yields the sequence in question. Since limits commute over limits, the result follows.

=--


We now consider a concept of $p$-completion that is in general different from def. \ref{AdicCompletionOfAbelingGroups}, but turns out to coincide with it in [[finitely generated object|finitely generated]] abelian groups. 

+-- {: .num_defn  #pInvertedInZ}
###### Definition

For $p$ a [[prime number]], write 

$$
  \mathbb{Z}[1/p]
   \coloneqq
  \underset{\longrightarrow}{\lim}
  \left(
    \mathbb{Z}
      \overset{p \cdot (-)}{\longrightarrow}
    \mathbb{Z}
      \overset{p \cdot (-)}{\longrightarrow}
    \mathbb{Z}
      \overset{}{\longrightarrow}
    \cdots
  \right)
$$

for the [[colimit]] (in [[Ab]]) over iterative applications of multiplication by $p$ on the [[integers]].

This is the [[abelian group]] generated by formal expressions $\frac{1}{p^k}$ for $k \in \mathbb{N}$, subject to the relations

$$
  (p \cdot n) \frac{1}{p^{k+1}}
  =
  n \frac{1}{p^k}
  \,.
$$

Equivalently it is the abelian group underlying the [[localization of a ring|ring localization]] $\mathbb{Z}[1/p]$.

=--

+-- {: .num_defn #AbelianGrouppComplete}
###### Definition

For $p$ a [[prime number]], then localization of abelian groups (def. \ref{AbelianGroupLocal}) at $\mathbb{Z}[1/p]$ (def. \ref{pInvertedInZ}) is called **$p$-completion of abelian groups**.

=--

+-- {: .num_lemma #CharacterizingpCompleteAbelianGroupsBypSequence}
###### Lemma

An [[abelian group]] $A$ is $p$-complete according to def. \ref{AbelianGrouppComplete} precisely if both the [[limit]] as well as the [[lim^1]] of the sequence

$$
  \cdots \overset{}{\longrightarrow}
  A \overset{p}{\longrightarrow}
  A \overset{p}{\longrightarrow}
  A \overset{p}{\longrightarrow} A
$$

vanishes:

$$
  \underset{\longleftarrow}{\lim}
  \left(
      \cdots \overset{}{\longrightarrow}
  A \overset{p}{\longrightarrow}
  A \overset{p}{\longrightarrow}
  A \overset{p}{\longrightarrow} A
  \right)
   \simeq
  0
$$

and

$$
  \underset{\longleftarrow}{\lim}^1
  \left(
      \cdots \overset{}{\longrightarrow}
  A \overset{p}{\longrightarrow}
  A \overset{p}{\longrightarrow}
  A \overset{p}{\longrightarrow} A
  \right)
   \simeq
  0
  \,.
$$

=--

+-- {: .proof}
###### Proof

By def. \ref{AbelianGroupLocal} the group $A$ is $\mathbb{Z}[1/p]$-local precisely if

$$
  Hom(\mathbb{Z}[1/p], A) \simeq 0
  \;\;\;\;\;\;\;
  and
  \;\;\;\;\;\;\;
  Ext^1(\mathbb{Z}[1/p], A) \simeq 0
  \,.
$$

Now use the colimit definition $\mathbb{Z}[1/p] = \underset{\longrightarrow}{\lim}_n \mathbb{Z}$ (def. \ref{pInvertedInZ}) and the fact that the [[hom-functor]] sends colimits in the first argument to limits to deduce that

$$
  \begin{aligned}
    Hom(\mathbb{Z}[1/p], A)
    & =
    Hom( \underset{\longrightarrow}{\lim}_n \mathbb{Z}, A  ) 
    \\
    & \simeq
    \underset{\longleftarrow}{\lim}_n Hom(\mathbb{Z},A)
    \\
    & \simeq
    \underset{\longleftarrow}{\lim}_n A
  \end{aligned}
  \,.
$$

This yields the first statement. For the second, use that for every [[cotower]] over abelian groups $B_\bullet$ there is a [[short exact sequence]] of the form

$$
  0 
    \to 
  \underset{\longleftarrow}{\lim}^1_n Hom(B_n, A)
    \longrightarrow
  Ext^1( \underset{\longrightarrow}{\lim}_n B_n, A )
    \longrightarrow
  \underset{\longleftarrow}{\lim}_n Ext^1( B_n, A)
    \to
  0
$$

(by [this lemma](Introduction+to+Stable+homotopy+theory+--+S#lim1AndExt1)).


In the present case all $B_n \simeq \mathbb{Z}$, which is a [[free abelian group]], hence a [[projective object]], so that all the [[Ext]]-groups out of it vannish. Hence by exactness there is an isomorphism

$$
  Ext^1( \underset{\longrightarrow}{\lim}_n \mathbb{Z}, A )
   \simeq
  \underset{\longleftarrow}{\lim}^1_n Hom(\mathbb{Z}, A)
   \simeq
  \underset{\longleftarrow}{\lim}^1_n A  
  \,.
$$

This gives the second statement.

=--

+-- {: .num_example #pPrimaryGroupsArePComplete}
###### Example

For $p$ a [[prime number]], the [[p-primary group|p-primary]] [[cyclic groups]] of the form $\mathbb{Z}/p^n \mathbb{Z}$ are $p$-complete (def. \ref{AbelianGrouppComplete}).

=--

+-- {: .proof}
###### Proof

By lemma \ref{CharacterizingpCompleteAbelianGroupsBypSequence} we need to check that 

$$
  \underset{\longleftarrow}{\lim}
  \left(
    \cdots
      \overset{p}{\longrightarrow} 
    \mathbb{Z}/p^n \mathbb{Z}
      \overset{p}{\longrightarrow} 
    \mathbb{Z}/p^n \mathbb{Z}
      \overset{p}{\longrightarrow} 
    \mathbb{Z}/p^n \mathbb{Z}
  \right)
  \simeq
  0
$$

and

$$
  \underset{\longleftarrow}{\lim}^1
  \left(
    \cdots
      \overset{p}{\longrightarrow} 
    \mathbb{Z}/p^n \mathbb{Z}
      \overset{p}{\longrightarrow} 
    \mathbb{Z}/p^n \mathbb{Z}
      \overset{p}{\longrightarrow} 
    \mathbb{Z}/p^n \mathbb{Z}
  \right)
  \simeq
  0
  \,.
$$

For the first statement observe that $n$ consecutive stages of the tower compose to the [[zero morphism]]. First of all this directly implies that the limit vanishes, secondly it means that the [[tower]] satisfies the [[Mittag-Leffler condition]] ([def.](Introduction+to+Stable+homotopy+theory+--+S#MittagLefflerCondition)) and this implies that the $\lim^1$ also vanishes ([prop.](Introduction+to+Stable+homotopy+theory+--+S#Lim1VanihesUnderMittagLeffler)).

=--

+-- {: .num_defn #ZpInfinity}
###### Definition

For $p$ a [[prime number]], write

$$
  \mathbb{Z}(p^\infty)
    \coloneqq
  \mathbb{Z}[1/p]/\mathbb{Z}
$$

(the [[p-primary group|p-primary]] part of $\mathbb{Q}/\mathbb{Z}$), where $\mathbb{Z}[1/p] = \underset{\longrightarrow}{\lim}(\mathbb{Z}\overset{p}{\to} \mathbb{Z} \overset{p}{\to} \mathbb{Z} \to \cdots )$ from def. \ref{pInvertedInZ}.

Since [[colimits]] commute over each other, this is equivalently 

$$
  \mathbb{Z}(p^\infty)
    \simeq
  \underset{\longrightarrow}{\lim}
  ( 0 \hookrightarrow \mathbb{Z}/p\mathbb{Z} \hookrightarrow \mathbb{Z}/p^2 \mathbb{Z} \hookrightarrow \cdots )
  \,.
$$

=--


+-- {: .num_theorem #pCompletionOfAbelianGroupsByHomsOutOfZpinfinity}
###### Theorem

For $p$ a [[prime number]], the $\mathbb{Z}[1/p]$-localization 

$$
  A \longrightarrow L_{\mathbb{Z}[1/p]} A
$$

of an abelian group $A$ (def. \ref{pInvertedInZ}, def. \ref{AbelianGroupLocal}), hence the $p$-completion of $A$ according to def. \ref{AbelianGrouppComplete}, is given by the morphism

$$
  A \longrightarrow Ext^1( \mathbb{Z}(p^\infty), A )
$$

into the first [[Ext]]-group into $A$ out of $\mathbb{Z}(p^\infty)$ (def. \ref{ZpInfinity}), which appears as the first [[connecting homomorphism]] $\delta$ in the [[long exact sequence]] of [[Ext]]-groups 

$$
  0 
    \to
  Hom(\mathbb{Z}(p^\infty),A)
    \longrightarrow
  Hom(\mathbb{Z}[1/p],A)
    \longrightarrow
  Hom(\mathbb{Z},A)
    \overset{\delta)}{\longrightarrow}
  Ext^1(\mathbb{Z}(p^\infty), A)
    \to
  \cdots
  \,.
$$

that is induced (via [this prop.](derived+functor+in+homological+algebra#LongExactSequenceOfRightDerivedFunctorsFromShortExactSequence)) from the defining [[short exact sequence]]

$$
  0 
    \to 
  \mathbb{Z}
    \longrightarrow
  \mathbb{Z}[1/p]
    \longrightarrow
  \mathbb{Z}(p^\infty)
    \to 
  0
$$

(def. \ref{ZpInfinity}).

=--

e.g. ([Neisendorfer 08, p. 16](localizatioon+of+abelian+groups#Neisendorfer08))


+-- {: .num_prop}
###### Proposition

If $A$ is a [[finitely generated module|finitely generated]] [[abelian group]], then its $p$-completion (def. \ref{AbelianGrouppComplete}, for any [[prime number]] $p$) is equivalently its [[p-adic completion]] (def. \ref{AdicCompletionOfAbelingGroups})

$$
  \mathbb{Z}[1/p] A
   \simeq
  A^\wedge_p
  \,.
$$

=--

+-- {: .proof}
###### Proof

By theorem \ref{pCompletionOfAbelianGroupsByHomsOutOfZpinfinity} the $p$-completion is $Ext^1(\mathbb{Z}(p^\infty),A)$. By def. \ref{ZpInfinity} there is a [[colimit]]

$$
  \mathbb{Z}(p^\infty)
  =
  \underset{\longrightarrow}{\lim}
  \left(
    \mathbb{Z}/p\mathbb{Z}
      \to
    \mathbb{Z}/p^2 \mathbb{Z}
      \to
    \mathbb{Z}/p^3 \mathbb{Z}
      \to 
    \cdots
  \right)
  \,.
$$

Together this implies, by [this lemma](Introduction+to+Stable+homotopy+theory+--+S#lim1AndExt1), that there is a [[short exact sequence]] of the form

$$
  0 
    \to
  \underset{\longleftarrow}{\lim}^1 Hom(\mathbb{Z}/p^n \mathbb{Z},A)
    \longrightarrow
  X^\wedge_p
    \longrightarrow
  \underset{\longleftarrow}{\lim}_n Ext^1(\mathbb{Z}/p^n \mathbb{Z}, A)
    \to 
  0
  \,.
$$

By lemma \ref{OutOfCyclicGroupExt1} the [[lim^1]] on the left is over the $p^n$-[[torsion subgroups]] of $A$, as $n$ ranges. By the assumption that $A$ is finitely generated, there is a [[maximum]] $n$ such that all torsion elements in $A$ are annihilated by $p^n$. This means that the [[Mittag-Leffler condition]] ([def.](Introduction+to+Stable+homotopy+theory+--+S#MittagLefflerCondition)) is satisfied by the [[tower]] of $p$-torsion subgroups, and hence the [[lim^1]]-term vanishes ([prop.](Introduction+to+Stable+homotopy+theory+--+S#Lim1VanihesUnderMittagLeffler)). 

Therefore by exactness of the above sequence there is an [[isomorphism]]

$$
  \begin{aligned}
    L_{\mathbb{Z}[1/p]}X
      & \simeq
    \underset{\longleftarrow}{\lim}_n Ext^1(\mathbb{Z}/p^n \mathbb{Z}, A)
    \\
    & \simeq
    \underset{\longleftarrow}{\lim}_n A/p^n A
  \end{aligned}
  \,,
$$

where the second isomorphism is by lemma \ref{OutOfCyclicGroupExt1}.

=--

+-- {: .num_prop #pDivisibleGroupsHaveVanishingpCompletion}
###### Proposition

If $A$ is a $p$-[[divisible group]] in that $A \overset{p \cdot (-)}{\longrightarrow} A$ is an [[isomorphism]], then its $p$-completion (def. \ref{AbelianGrouppComplete}) vanishes.

=--

+-- {: .proof}
###### Proof

By theorem \ref{pCompletionOfAbelianGroupsByHomsOutOfZpinfinity} the localization morphism $\delta$ sits in a [[long exact sequence]] of the form

$$
  0 
    \to
  Hom(\mathbb{Z}(p^\infty),A)
    \longrightarrow
  Hom(\mathbb{Z}[1/p],A)
    \overset{\phi}{\longrightarrow}
  Hom(\mathbb{Z},A)
    \overset{\delta}{\longrightarrow}
  Ext^1(\mathbb{Z}(p^\infty), A)
    \to
  \cdots
  \,.
$$

Here by def. \ref{pInvertedInZ} and since the [[hom-functor]] takes [[colimits]] in the first argument to [[limits]], the second term is equivalently the [[limit]]

$$
  Hom(\mathbb{Z}[1/p],A)
    \simeq
  \underset{\longleftarrow}{\lim}
  \left(
     \cdots
     \to 
     A \overset{p \cdot (-)}{\longrightarrow} A \overset{p \cdot (-)}{\longrightarrow} A
  \right)
  \,.
$$

But by assumption all these morphisms $p \cdot (-)$ that the limit is over are [[isomorphisms]], so that the limit collapses to its first term, which means that the morphism $\phi$ in the above sequence is an [[isomorphism]]. But by exactness of the sequence this means that $\delta = 0$.

=--

+-- {: .num_cor}
###### Corollary

Let $p$ be a [[prime number]]. If $A$ is a [[finite abelian group]], then its $p$-completion (def. \ref{AbelianGrouppComplete}) is equivalently its [[p-primary group|p-primary part]].

=--

+-- {: .proof}
###### Proof

By the [[fundamental theorem of finite abelian groups]], $A$ is a finite [[direct sum]] 

$$
  A 
   \simeq
  \underset{i}{\oplus}
  \mathbb{Z}/p_i^{k_i}\mathbb{Z}
$$


of [[cyclic groups]] of [[order of a group|ordr]] $p_i^{k_1}$ for $p_i$ [[prime numbers]] and $k_i \in \mathbb{N}$ ([thm.](finite+abelian+group#FiniteAbelianGroupIsDirectSumOfCyclics)). 

Since finite direct sums are equivalently [[products]] ([[biproducts]]: [[Ab]] is an [[additive category]]) this means that

$$
  Ext^1( \mathbb{Z}(p^\infty), A )
  \simeq
  \underset{i}{\prod}
  Ext^1( \mathbb{Z}(p^\infty), \mathbb{Z}/p_i^{k_1}\mathbb{Z} )
  \,.
$$

By theorem \ref{pCompletionOfAbelianGroupsByHomsOutOfZpinfinity} the $i$th factor here is the $p$-completion of $\mathbb{Z}/p_i^{k_i}\mathbb{Z}$, and since $p \cdot(-)$ is an isomorphism on $\mathbb{Z}/p_i^{k_i}\mathbb{Z}$ if $p_i \neq p$ (because its [[kernel]] evidently vanishes), prop. \ref{pDivisibleGroupsHaveVanishingpCompletion} says that in this case the factor vanishes, so that only the factors with $p_i = p$ remain. On these however $Ext^1(\mathbb{Z}(p^\infty),-)$ is the identity by example \ref{pPrimaryGroupsArePComplete}.

=--


##### Localization and nilpotent completion of spectra
 {#LocalizationOfSpectra}

We discuss 

1. _[Bousfield localization of spectra](#BousfieldLocalizationOfSpectra)_

1. _[Nilpotent completion of spectra](#NilpotentCompletionOfSpectra)_

which are the analogs in [[stable homotopy theory]] of the construction of [[localization of abelian groups]] discussed [above](#LocalizationOfAbelianGroups).

**Literature**: ([Bousfield 79](#Bousfield79))

$\,,$

**Localization of spectra**
 {#BousfieldLocalizationOfSpectra}

+-- {: .num_defn #EAcyclicAndLocalSpectra}
###### Definition

Let $E \in Ho(Spectra)$ be be a [[spectrum]]. Say that 

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

Given $E,X \in Ho(Spectra)$, then an **$E$-[[Bousfield localization of spectra]]** of $X$ is 

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


It remains to see that the [[homotopy fiber]] of $X \to L_E X$ is $E$-acyclic: By the [[tensor triangulated category|tensor triangulated]] structure on $Ho(Spectra)$ ([prop.](Introduction+to+Stable+homotopy+theory+--+1-2#TensorTriangulatedStructureOnStableHomotopyCategory)) it is sufficient to show that the [[homotopy cofiber]] is $E$-acyclic (since it differs from the homotopy fiber only by suspension). By the [[pasting law]], the homotopy cofiber of a [[transfinite composition]] is the transfinite composition of a sequence of homotopy pushouts. By lemma \ref{KappaCellSpectrumWitnessingELocalization} and applying the pasting law again, all these homotopy pushouts produce $E$-acyclic objects. Hence we conclude by observing that the transfinite composition of the morphisms between these $E$-acyclic objects is $E$-acyclic. Since by construction all these morphisms are relative cell complex inclusions, this follows again with the compactness of the $n$-spheres ([lemma](Introduction+to+Stable+homotopy+theory+--+P#CompactSubsetsAreSmallInCellComplexes)).

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


$\,$

**Nilpotent completion of spectra**
 {#NilpotentCompletionOfSpectra}





+-- {: .num_defn #ENilpotentCompletion}
###### Definition

Let $(E, \mu, e)$ be a [[homotopy commutative ring spectrum]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyCommutativeRingSpectrum)) and $Y \in Ho(Spectra)$ any spectrum. Write $\overline{E}$ for the [[homotopy fiber]] of the unit $\mathbb{S}\overset{e}{\to} E$ as in def. \ref{HomotopyFiberOfUnitOfCommutativeRingSpectrum} such that the $E$-Adams filtration of $Y$ (def. \ref{AdamsEAdamsSpectralSequence}) reads (according to lemma \ref{Wp})

$$
  \array{
    \vdots
    \\
    \downarrow
    \\
    \overline{E}^3 \wedge Y
    \\
    \downarrow
    \\
    \overline{E}^2 \wedge Y
    \\
    \downarrow
    \\
    \overline{E} \wedge Y
    \\
    \downarrow
    \\
    Y
  }
  \,.
$$

For $s \in \mathbb{N}$, write

$$
  \overline{E}_{s-1}
    \coloneqq
  hocof( \overline{E}^s \overset{i^s}{\longrightarrow} \mathbb{S})
$$

for the homotopy cofiber. Here $\overline{E}_{-1} \simeq 0$.
By the [[tensor triangulated category|tensor triangulated]] structure of $Ho(Spectra)$ ([prop.](Introduction+to+Stable+homotopy+theory+--+1-2#TensorTriangulatedStructureOnStableHomotopyCategory)), this homotopy cofiber is preserved by forming [[smash product of spectra|smash product]] with $Y$, and so also

$$
  \overline{E}_n \wedge Y
   \simeq
  hocof( \overline{E}^n \wedge Y \overset{}{\longrightarrow} Y)
  \,.
$$

Now let

$$
  \overline{E}_s 
    \overset{p_{s-1}}{\longrightarrow}
  \overline{E}_{s-1}
$$

be the morphism implied by the [[octahedral axiom]] of the [[triangulated category]] $Ho(Spectra)$ ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#CategoryWithCofiberSequences), [prop.](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyCategoryIsTriangulated)):


$$
  \array{
    \overline{E}^{s+1}
      &\overset{i}{\longrightarrow}&
    \overline{E}^s
      &\longrightarrow&
    E \wedge \overline{E}^s
      &\longrightarrow&
    \Sigma \overline{E}^{s+1}
    \\
    {}^{\mathllap{=}}\downarrow
      &&
    \downarrow^{\mathrlap{i^s}}
      &&
    \downarrow^{}
      &&
    \downarrow
    \\
    \overline{E}^{s+1}
      &\longrightarrow& 
    \mathbb{S}
      &\longrightarrow&
    \overline{E}_s
      &\longrightarrow&
    \Sigma \overline{E}^{s+1}
    \\
    &&
    \downarrow 
      &&
    \downarrow^{\mathrlap{p_{s-1}}}
    \\
      &&
    \overline{E}_{s-1}
      &\overset{=}{\longrightarrow}&
    \overline{E}_{s-1}
    \\
    &&
    \downarrow 
      &&
    \downarrow
    \\
      &&
    \Sigma \overline{E}^s
      &\longrightarrow&
     \Sigma E \wedge \overline{E}^s
  }
  \,.
$$

By the [[commuting square]] in the middle and using again the [[tensor triangulated category|tensor triangulated]] structure, this yields an inverse sequence under $Y$:

$$
  Y   
    \simeq
  \mathbb{S} \wedge Y
    \longrightarrow
  \cdots
    \overset{p_3 \wedge id}{\longrightarrow}
  \overline{E}_3 \wedge Y
    \overset{p_2 \wedge id}{\longrightarrow}
  \overline{E}_2 \wedge Y
    \overset{p_1 \wedge id}{\longrightarrow}
  \overline{E}_1 \wedge Y
$$

The **[[E-nilpotent completion]]** $Y^\wedge_E$ of $Y$ is the [[homotopy limit]] over the resulting inverse sequence

$$
  Y^\wedge_E
    \coloneqq
  \mathbb{R}\underset{\longleftarrow}{\lim}_n \overline{E}_n \wedge Y
$$

or rather the canonical morphism into it

$$
  Y \longrightarrow Y^\wedge_E
  \,.
$$

Concretely, if 

$$
  Y   
    \simeq
  \mathbb{S} \wedge Y
    \longrightarrow
  \cdots
    \overset{p_3 \wedge id}{\longrightarrow}
  \overline{E}_3 \wedge Y
    \overset{p_2 \wedge id}{\longrightarrow}
  \overline{E}_2 \wedge Y
    \overset{p_1 \wedge id}{\longrightarrow}
  \overline{E}_1 \wedge Y
$$

is presented by a tower of fibrations between fibrant spectra in the [[model structure on topological sequential spectra]], then $Y^\wedge_E$ is represented by the ordinary [[sequential limit]] over this tower.


=---

([Bousfield 79, top, middle and bottom of page 272](#Bousfield79))


+-- {: .num_remark }
###### Remark

In ([Bousfield 79](#Bousfield79)) the $E$-nilpotent completion of $X$ (def. \ref{ENilpotentCompletion}) is denoted "$E^\wedge X$". The notation "$X^\wedge_E$" which we use here is more common among modern authors. It emphasizes the conceptual relation to [[p-adic completion]] $A^\wedge_p$ of abelian groups (def. \ref{AdicCompletionOfAbelingGroups}) and is less likely to lead to confusion with the smash product of $E$ with $X$. 

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


+-- {: .num_prop #SufficientConditionsForTotalizationToBeELocalization}
###### Proposition

Let $E$ be a [[connective spectrum|connective]] [[ring spectrum]] such that the core of $\pi_0(E)$, def. \ref{CoreOfARing}, is either of

* the [[localization of a ring|localization]] of the [[integers]] at a set $J$ of [[primes]], $c \pi_0(E) \simeq \mathbb{Z}[J^{-1}]$;

* a [[cyclic ring]] $c \pi_0(E) \simeq \mathbb{Z}/n\mathbb{Z}$, for $n \geq 2$.

Then the map in remark \ref{CanonicalMapFromELocalizationToTotalization} is an equivalence

$$
  L_E X 
    \stackrel{\simeq}{\longrightarrow} 
  X^\wedge_E
  \,.
$$

=--

([Bousfield 79, theorem 6.5, theorem 6.6](#Bousfield79)).













##### Convergence theorems
 {#ConvergenceStatements}

We state the two main versions of [[Aldridge Bousfield|Bousfield]]'s convergence theorems for the $E$-[[Adams spectral sequence]], below as theorem \ref{EAdamsConvergenceForCorepi0EBeingZLocalizedAtPrimes} and theorem \ref{EAdamsConvergenceForCorepi0EBeingCyclicGroup}.

First we need to define the concepts that enter the convergence statement: 

1. the infinity-page $E_\infty^{s,t}(X,Y)$ (def. \ref{InfinityPageEAdams}), 

1. a filtration on $[X,Y^\wedge_E]_\bullet$ (def. \ref{EAdamsFiltration})

1. what it means for the former to converge to the latter (def. \ref{EAdamsConvergingCompletely}).

Broadly the statement will be that typically 

1. the $E$-Adams spectral sequence $E_r^{s,t}(X,Y)$ computes the [[stable homotopy groups]] $[X,Y^\wedge_E]$ of maps from $X$ into the [[E-nilpotent completion]] of $Y$;

1. these groups are [[localization of an abelian group|localizations]] of the full groups $[X,Y]_\bullet$ depending on the [[core of a ring|core]] of $\pi_0(E)$.


**Literature**: ([Bousfield 79](#Bousfield79))

$\,$



+-- {: .num_defn #InfinityPageEAdams}
###### Definition

Let $(E, \mu, e)$ be a [[homotopy commutative ring spectrum]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyCommutativeRingSpectrum)) and $X,Y \in Ho(Spectra)$ two [[spectra]] with associated $E$-[[Adams spectral sequence]] $\{E_r^{s,t}, d_r\}$ (def. \ref{AdamsEAdamsSpectralSequence}).

Observe that 

$$
  if \; r \gt s \; then \; \;
  E^{s,\bullet}_{r+1}(X,Y)
   \simeq
  ker(d_r|_{E_r^{s,\bullet}(X,Y)})
  \subset
  E_r^{s,\bullet}(X,Y)  
$$

since the differential $d_r$ on the $r$th page has bidegree $(r,r-1)$, and since $E_r^{s \lt 0,\bullet(X,Y)} \simeq 0$, so that for $r \gt s$ the image of $d_r$ in $E_r^{s,t}(X,Y)$ vanishes.

Thus define the bigraded abelian group

$$
  E_\infty^{s,t}(X,Y)
   \coloneqq
  \underset{r \gt s}{\lim} E_r^{s,t}(X,Y)
  =
  \underset{r \gt s}{\cap} E_r^{s,t}(X,Y)
$$

called the "**infinity page**" of the $E$-Adams spectral sequence.


=--

+-- {: .num_defn #EAdamsFiltration}
###### Definition

Let $(E, \mu, e)$ be a [[homotopy commutative ring spectrum]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyCommutativeRingSpectrum)) and $X,Y \in Ho(Spectra)$ two [[spectra]] with associated $E$-[[Adams spectral sequence]] $\{E_r^{s,t}, d_r\}$ (def. \ref{AdamsEAdamsSpectralSequence}) and [[E-nilpotent completion]] $Y^\wedge_E$ (def. \ref{ENilpotentCompletion}).

Define a [[filtered object|filtration]] 

$$
  \cdots
   \hookrightarrow
  F^3 [X, Y^\wedge_E]_\bullet
   \hookrightarrow
  F^2 [X, Y^\wedge_E]_\bullet
    \hookrightarrow
  F^1 [X,Y^\wedge_E]_\bullet
    =
  [X, Y^\wedge_E ]_\bullet
$$

on the [[graded abelian group]] $[X,Y^\wedge_E]_\bullet$ by

$$
  F^s [X, Y^\wedge_E]_\bullet
    \;\coloneqq\;
  ker( 
   \;
   [X, Y^\wedge_E]_\bullet
     \overset{[X, Y^\wedge_E \to \overline{E}_{s-1} \wedge Y ]}{\longrightarrow}
   [X, \overline{E}_{s-1} \wedge Y]_\bullet
   \; 
  )
  \,,
$$

where the morphisms $Y^\wedge_E \to \overline{E}_{s-1} \wedge Y$ is the canonical one from def. \ref{ENilpotentCompletion}.

=--


+-- {: .num_defn #EAdamsConvergingCompletely}
###### Definition

Let $(E, \mu, e)$ be a [[homotopy commutative ring spectrum]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyCommutativeRingSpectrum)) and $X,Y \in Ho(Spectra)$ two [[spectra]] with associated $E$-[[Adams spectral sequence]] $\{E_r^{s,t}, d_r\}$ (def. \ref{AdamsEAdamsSpectralSequence}) and [[E-nilpotent completion]] $Y^\wedge_E$ (def. \ref{ENilpotentCompletion}).

Say that the $E$-[[Adams spectral sequence]] $\{E_r^{s,t}, d_r\}$ **converges completely** to the [[E-nilpotent completion]] $[X,Y^\wedge_E]_\bullet$ if the following two canonical morphisms are [[isomorphisms]]

1. $
     [X, Y^\wedge_E]_\bullet 
       \longrightarrow 
     \underset{\longleftarrow}{\lim}_s
      [X, Y^\wedge_E]_\bullet / F^s [X, Y^\wedge_E]_\bullet
   $

   (where on the right we have the limit over the tower of [[quotients]] by the stages of the [[filtration]] from def. \ref{EAdamsFiltration})

1. $
     F^s [X, Y^\wedge_E]_{t-s}
     /
     F^{s+1}[X, Y^\wedge]_{t-s}
       \longrightarrow
     E^{s,t}_\infty(X,Y)
     \;\;\;\;\;\;\;\;
     \forall s,t
   $

   (where $F^s [X, Y^\wedge_E]_\bullet$ is the filtration stage from def. \ref{EAdamsFiltration} and $E^{s,t}_\infty(X,Y)$ is the infinity-page from def. \ref{InfinityPageEAdams}).

Notice that the first morphism is always surjective, while the second is necessarily injective, hence the condition is equivalently that the first is also injective, and the second also surjective.

=--

([Bousfield 79, &#167;6](#Bousfield79))

$\,$

Now we state sufficient conditions for complete convergence of the $E$-Adams spectral sequence. It turns out that convergence is controled by the [[core of a ring|core]] (def. \ref{CoreOfARing}) of the ring $\pi_0(E)$. By prop. \ref{ClassificationOfSolidRings} these cores are either localizations of the integers $\mathbb{Z}[J^{-1}]$ at a set $J$ of primes (def. \ref{InvertingPrimes}) or are [[cyclic rings]], or cores of products of these. We discuss the first two cases.


+-- {: .num_theorem #EAdamsConvergenceForCorepi0EBeingZLocalizedAtPrimes}
###### Theorem

Let $(E,\mu,e)$ be a [[homotopy commutative ring spectrum]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyCommutativeRingSpectrum)) and let $X,Y \in Ho(Spectra)$ be two [[spectra]] such that

1. the [[core of a ring|core]] (def. \ref{CoreOfARing}) of the 0-th [[stable homotopy group]] ring of $E$ ([prop.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyGroupsOfHomotopyCommuta
tiveRingSpectrum)) is the [[localization of a ring|localization]] of the [[integers]] at a set $J$ of primes (def. \ref{InvertingPrimes})

   $$
     c \pi_0(E) \simeq \mathbb{Z}[J^{-1}] \subset \mathbb{Q}
   $$

1. $X$ is a [[CW-spectrum]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#CWSpectrum)) with a [[finite number]] of cells ([rmk.](Introduction+to+Stable+homotopy+theory+--+1-1#StrictModelStructureCellAttachmentToSpectra));

then the $E$-[[Adams spectral sequence]] for $[X,Y]_\bullet$ (def. \ref{AdamsEAdamsSpectralSequence}) converges completely (def. \ref{EAdamsConvergingCompletely}) to the localization

$$
  [X, Y^\wedge_E]_\bullet
    =
  \mathbb{Z}[J^{-1}] \otimes [X,Y]_\bullet
$$

of $[X,Y]_\bullet$.

=--

([Bousfield 79, theorem 6.5](#Bousfield79))


+-- {: .num_theorem #EAdamsConvergenceForCorepi0EBeingCyclicGroup}
###### Theorem

Let $(E,\mu,e)$ be a [[homotopy commutative ring spectrum]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyCommutativeRingSpectrum)) and let $X,Y \in Ho(Spectra)$ be two [[spectra]] such that

1. the [[core of a ring|core]] (def. \ref{CoreOfARing}) of the 0-th [[stable homotopy group]] ring of $E$ ([prop.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyGroupsOfHomotopyCommutativeRingSpectrum)) is a [[prime field]]

   $c \pi_0(E) \simeq \mathbb{F}_p$

   for some [[prime number]] $p$;

1. $Y$ is a [[connective spectrum]] in that its [[stable homotopy groups]] $\pi_\bullet(Y)$ vanish in negative degree;

1. $X$ is a [[CW-spectrum]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#CWSpectrum)) with a [[finite number]] of cells ([rmk.](Introduction+to+Stable+homotopy+theory+--+1-1#StrictModelStructureCellAttachmentToSpectra));

1. $[X,Y]_\bullet$ is degreewise a [[finitely generated object|finitely generated]] group
 
then the $E$-[[Adams spectral sequence]] for $[X,Y]_\bullet$ (def. \ref{AdamsEAdamsSpectralSequence}) converges completely (def. \ref{EAdamsConvergingCompletely}) to the $p$-[[adic completion]] (def. \ref{AdicCompletionOfAbelingGroups})

$$
  [X, Y^\wedge_E]_\bullet
    \simeq
  \underset{\longleftarrow}{\lim}_n [X,Y]_\bullet/p^n[X,Y]_\bullet
$$

of $[X,Y]_\bullet$. 

=--

([Bousfield 79, theorem 6.6](#Bousfield79))












### Examples


+-- {: .num_example}
###### Example

Examples of [[commutative ring spectra]] $E$ for which the dual $E$-[[Steenrod algebra]] $E_\bullet(E)$ over $\pi_\bullet(E)$ of def. \ref{HopfAlgebroidStructureOnDualEOperations} where the left and right action of $\pi_\bullet(E)$ are not just isomorphic (via prop. \ref{EETwoLeftModuleStructures}) but actually equal according to remark \ref{HopfAlgebrasAsHopfAlgebroids}, includes the case $E = $ [[HA|H]]$\mathbb{F}_p$.

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

([Adams 69, lecture 1, lemma 28 (p. 45)](#Adams69))

+-- {: .proof}
###### Proof of the first two items

For $E = \mathbb{S}$ we have $\mathbb{S}_\bullet(\mathbb{S}) \coloneqq \pi_\bullet(\mathbb{S} \wedge \mathbb{S}) \simeq \pi_\bullet(\mathbb{S})$, since the [[sphere spectrum]] $\mathbb{S}$ is the [[tensor unit]] for the derived [[smash product of spectra]] ([cor.](Introduction+to+Stable+homotopy+theory+--+1-2#MonoidalStableHomotopyCategory)). Hence the statement follows since every ring is, clearly, flat over itself.

For $E = H \mathbb{F}_p$ we have that $\pi_\bullet(H \mathbb{F}_p) \simeq \mathbb{F}_p$ ([prop.](Introduction+to+Stable+homotopy+theory+--+1-2#StableHomotopyGroupsOfEMSpectrum)), hence a [[field]] (a [[prime field]]). Every module over a field is a [[projective module]] ([prop.](projective+module#ModuleOverAFieldIsProjective)) and every projective module is flat ([prop.](flat+module#ProjectiveModulesAreFlat)).

=--

+-- {: .num_example}
###### Example

Examples of ring spectra that are _not_ flat in the sense of def. \ref{FlatE} include [[HA|H]][[integers|Z]], and $M S U$.

=--



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
    X^\wedge_{MU} \simeq X
    \,.
  $$

* $E = $ [[BP]] at prime $p$. For every spectrum $X$ its $BP$-nilpotent completion is its [[p-localization]] 

  $$
    X^\wedge_{BP} \simeq X_{(p)} \coloneqq X \wedge M \mathbb{Z}_{(p)}
  $$

  (where $\mathbb{Z}_{(p)}\subset \mathbb{Q}$ is the result of inverting all primes different from $p$).

=--


For more discussion of [[E-infinity geometry|E-infinity]] (derived) [[formal completions]] via totalizations of [[Amitsur complexes]], see ([Carlsson 07](completion+of+a+module#Carlsson07)).




#### Classical Adams spectral sequence ($E = H \mathbb{F}_2$, $X = \mathbb{S}$)
 {#ClassicalAdamsSpectralSequence}

We consider now the example of the $E$-[[Adams spectral sequence]] $\{E_r^{s,t}(X,Y), d_r\}$ (def. \ref{AdamsEAdamsSpectralSequence}) for the case that 

1. $E = H \mathbb{F}_p$ is the [[Eilenberg-MacLane spectrum]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#OrthogonalEilenbergMacLaneRingSpectrum)) with [[coefficients]] in a [[prime field]], regarded in $Ho(Spectra)$ with its canonical struture of a [[homotopy commutative ring spectrum]] induced (via [this corollary](Introduction+to+Stable+homotopy+theory+--+1-2#MonoidalStableHomotopyCategory)) from its canonical structure of an [[orthogonal ring spectrum]] (from [this def.](Introduction+to+Stable+homotopy+theory+--+1-2#OrthogonalEilenbergMacLaneRingSpectrum));

1. $X = Y = \mathbb{S}$ are both the [[sphere spectrum]].

This example is called the _[[classical Adams spectral sequence]]_.

The $H\mathbb{F}_p$-dual Steenrod algebra according to the general definition \ref{HopfAlgebroidStructureOnDualEOperations} turns out to be the classical dual [[Steenrod algebra]] $\mathcal{A}_p^\ast$ recalled [below](#TheClassicalDualSteenrodAlgebra) .

Notice that $H \mathbb{F}_2$ satisfies the two assumptions needed to identify the second page of the $H\mathbb{F}_p$-Adams spectral sequence according to theorem \ref{SecondPageOfEAdamsSpectralSequence}:

+-- {: .num_lemma #HFpSatisfiesConditionsForSecondPage}
###### Lemma

The [[Eilenberg-MacLane spectrum]] $H\mathbb{F}_p$ is flat according to \ref{FlatE}, and $H \mathbb{F}_p(\mathbb{S})$ is a [[projective module]] over $\pi_\bullet(H \mathbb{F}_p)$.

=--

+-- {: .proof}
###### Proof

The [[stable homotopy groups]] of $H \mathbb{F}_p$ is the [[prime field]] $\mathbb{F}_p$ itself, regarded as a graded commutative ring concentrated in degree 0 ([prop.](Introduction+to+Stable+homotopy+theory+--+1-2#StableHomotopyGroupsOfEMSpectrum))

$$
  \pi_\bullet(H\mathbb{F}_p)
    \simeq
  \mathbb{F}_p
  \,.
$$

Since this is a [[field]], all [[modules]] over it are [[projective modules]] ([prop.](projective+module#ModuleOverAFieldIsProjective)), hence in particular [[flat modules]] ([prop.](flat+module#ProjectiveModulesAreFlat)).

=--

+-- {: .num_cor #ClassicalAdamsSpectralSequenceEstablished}
###### Corollary

The [[classical Adams spectral sequence]], i.e. the $E$-Adams spectral sequence (def. \ref{AdamsEAdamsSpectralSequence}) for $E = H \mathbb{F}_p$ ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#OrthogonalEilenbergMacLaneRingSpectrum)) and $X = Y = \mathbb{S}$, has on its second page the [[Ext]]-groups of classical dual [[Steenrod algebra]] [[comodules]] from $\mathbb{F}_p \simeq H\mathbb{F}_p(\mathbb{S})$ to itself, and converges completely (def. \ref{EAdamsConvergingCompletely}) to the [[p-adic completion]] (def. \ref{AdicCompletionOfAbelingGroups}) of the [[stable homotopy groups of spheres]], hence in degree 0 to the [[p-adic integers]] and in all other degrees to the $p$-primary part (theorem \ref{FundamentalTheoremOfFinitelyGeneratedAbelianGroups})

$$
  E_2^{s,t}(\mathbb{S},\mathbb{S})
  \;=\;
  Ext^{s,t}_{\mathcal{A}_p^\ast}(\mathbb{F}_p, \mathbb{F}_p)
    \;\Rightarrow\;
  (\pi_{\bullet}(\mathbb{S}))_p
  \,.
$$

=--

+-- {: .proof}
###### Proof

By lemma \ref{HFpSatisfiesConditionsForSecondPage} the conditions of theorem \ref{SecondPageOfEAdamsSpectralSequence} are satisfied, which implies the form of the second page.

For the convergence statement, we check the assumptions in theorem \ref{EAdamsConvergenceForCorepi0EBeingCyclicGroup}:

1. By prop. \ref{FormingCoreOfARingIsIdempotent} and prop. \ref{ClassificationOfSolidRings} the ring $\mathbb{F}_p = \pi_0(H \mathbb{F}_p)$ coincides with its [[core of a ring|core]]:  $c \mathbb{F}_p \simeq \mathbb{F}_p$;

1. $\mathbb{S}$ is clearly a [[connective spectrum]];

1. $\mathbb{S}$ is clearly a finite [[CW-spectrum]];

1. the groups $\pi_\bullet(\mathbb{S}) \simeq [\mathbb{S},\mathbb{S}]_\bullet$ are degreewise finitely generated, by [[Serre's finiteness theorem]].

Hence theorem \ref{EAdamsConvergenceForCorepi0EBeingCyclicGroup} applies and gives the convergence as stated.

Finally, by prop. \ref{DualSteenrodAlgebrasIsHFpHopfAlgebra} the dual $E$-Steenrod algebra in the present case is the classical dual [[Steenrod algebra]].

=--

We now use the [[classical Adams spectral sequence]] from corollary \ref{ClassicalAdamsSpectralSequenceEstablished} to compute the first dozen [[stable homotopy groups of spheres]]. 


##### The dual Steenrod algebra
 {#TheClassicalDualSteenrodAlgebra}


+-- {: .num_defn #SteenrodAlgebraForHFp}
###### Definition

Let $p$ be a [[prime number]]. Write $\mathbb{F}_p$ for the corresponding [[prime field]].

The **mod $p$-[[Steenrod algebra]]** $\mathcal{A}_{p}$ is the graded co-commutative [[Hopf algebra]] over $\mathbb{F}_p$ which is

* for $p = 2$ generated by elements denoted $Sq^n$ for $n \in \mathbb{N}$, $n \geq 1$;

* for $p \gt 2$ generated by elements denoted $\beta$ and $P^n$ for $\in \mathbb{N}$, $n \geq 1$

(called the **Serre-Cartan basis elements**) 

whose product is subject to the following relations (called the **&#193;dem relations**):

**for $p = 2$**:

for $0 \lt h \lt 2k$  the

$$
  Sq^h Sq^k
  \;=\;
  \underoverset{i = 0}{[h/2]}{\sum}
  \left(
    \array{
      k -i - 1
      \\
      h - 2i
    }    
  \right)
  Sq^{h + k -i} Sq^i
  \,,
$$

**for $p \gt 2$**:

for $0 \lt h \lt p k$ then

$$
  P^h P^k
  \;=\;
  \underoverset{i = 0}{[h/p]}{\sum}
  (-1)^{h+i}
  \left(
    \array{
      (p-1)(k-i) - 1
      \\
      h - p i 
    }
  \right)
  P^{h +k - i}P^i
$$

and if $0 \lt h \lt p k$ then

$$
  \begin{aligned}
    P^h \beta P^k
    & =\;
    \underoverset{[h/p]}{i = 0}{\sum}
    (-1)^{h+i}
    \left(
      \array{
        (p-1)(k-i)
        \\
        h - p i
      }
    \right)
    \beta P^{h+k-i}P^i
    \\
    & + 
    \underoverset{[(h-1)/p]}{i = 0}{\sum}
    (-1)^{h+i-1}
    \left(
      \array{
        (p-1)(k-i) - 1
        \\
        h - p i - 1
      }
    \right)
    P^{h+k-i} \beta P^i
  \end{aligned}
$$

and whose coproduct $\Psi$ is subject to the following relations:

**for $p = 2$**:

$$
  \Psi(Sq^n)
  \;=\;
  \underoverset{k = 0}{n}{\sum} Sq^k \otimes Sq^{n-k}
$$

**for $p \gt 2$**:

$$
  \Psi(P^n)
  \;=\;
  \underoverset{n}{k = 0}{\sum}
  P^k \otimes P^{n-k}
$$

and

$$
  \Psi(\beta) = \beta \otimes 1 + 1 \otimes \beta
  \,.
$$

=--

e.g. ([Kochmann 96, p. 52](#Kochmann96))

+-- {: .num_defn #DualSteenrodAlgebraForHPf}
###### Definition

The $\mathbb{F}_p$-[[linear dual]] of the mod $p$-Steenrod algebra (def. \ref{SteenrodAlgebraForHFp}) is itself naturally a graded [[commutative Hopf algebroid|commutative Hopf algebra]] (with coproduct the linear dual of the original product, and vice versa), called the **dual Steenrod algebra** $\mathbb{A}_{\mathbb{F}_p}^\ast$.

=--

+-- {: .num_prop #DualSteenrodAlgebrasIsHFpHopfAlgebra}
###### Proposition

There is an isomorphism

$$
  \mathcal{A}^\ast_{p}
  \simeq
  H_\bullet( H \mathbb{F}_p, \mathbb{F}_p )
  = 
  \pi_\bullet( H \mathbb{F}_p \wedge H \mathbb{F}_p )
  \,.
$$

=--

(e.g. [Ravenel 86, p. 49](#Ravenel86), [Rognes 12, remark 7.24](#Rognes12))


We now give the generators-and-relations description of the dual Steenrod algebra $\mathcal{A}^\ast_{p}$ from def. \ref{DualSteenrodAlgebraForHPf}, in terms of linear duals of the generators for $\mathcal{A}_{p}$ itself, according to def. \ref{SteenrodAlgebraForHFp}.


+-- {: .num_theorem #MilnorTheoremOnDualSteenrodAlgebra}
###### Theorem
**(Milnor's theorem)**


The dual mod $2$-Steenrod algebra $\mathcal{A}^\ast_{2}$ (def. \ref{DualSteenrodAlgebraForHPf}) is, as an [[associative algebra]], the free [[graded commutative algebra]]

$$
  \mathcal{A}^\ast_{p}
    \simeq
  Sym_{\mathbb{F}_p}(\xi_1, \xi_2, \cdots, )
$$

on generators:

* $\xi_n$, $n \geq 1$ being the linear dual to $Sq^{p^{n-1}} Sq^{p^{n-2}} \cdots Sq^p Sq^1$,

  of degree $2^n -1$.


The dual mod $p$-Steenrod algebra $\mathcal{A}^\ast_{p}$ (def. \ref{DualSteenrodAlgebraForHPf}) is, as an [[associative algebra]], the free [[graded commutative algebra]]

$$
  \mathcal{A}^\ast_{p}
    \simeq
  Sym_{\mathbb{F}_p}(\xi_1, \xi_2, \cdots, \;\tau_0, \tau_1, \cdots)
$$

on generators:

* $\xi_n$, $n \geq 1$ being the linear dual to $P^{p^{n-1}} P^{p^{n-2}} \cdots P^p P^1$,

  of degree $2(p^n-1)$.

* $\tau_n$ being linear dual to $P^{p^{n-1}} P^{p^{n-2}} \cdots P^p P^1\beta$.

Moreover, the coproduct on $\mathcal{A}^\ast_{p}$ is given on generators by

$$
  \Psi(\xi_n)
  =
  \underoverset{k = 0}{n}{\sum} \xi_{n-k}^{p^k} \otimes \xi_k
$$

and

$$
  \Psi(\tau_n)
  =
  \tau_n \otimes 1
  + 
  \underoverset{k=0}{n}{\sum}
  \xi_{n-k}^{p^k} \xi_{n-k}^{p^k}\otimes \tau_k
  \,,
$$

where we set $\xi_0 \coloneqq 1$.

(This defines the coproduct on the full algbra by it being an algebra homomorphism.)

=--


This is due to ([Milnor 58](Steenrod+algebra#Milnor58)). See for instance ([Kochmann 96, theorem 2.5.1](#Kochmann96), [Ravenel 86, chapter III, theorem 3.1.1](#Ravenel86))



##### The cobar complex

In order to compute the second page of the classical $H \mathbb{F}_p$-Adams spectral sequence (cor. \ref{ClassicalAdamsSpectralSequenceEstablished}) we consider a suitable [[cochain complex]] whose [[cochain cohomology]] gives the relevant [[Ext]]-groups.

+-- {: .num_defn #UnitCoidealInCommutativeHopfAlgebra}
###### Definition

Let $(\Gamma,A)$ be a [[graded commutative Hopf algebra]], hence a [[commutative Hopf algebroid]] for which the left and right units coincide $\eta \;\colon\; A \longrightarrow \Gamma$ (remark \ref{HopfAlgebrasAsHopfAlgebroids}). 

Then the **unit coideal** of $\Gamma$ is the [[cokernel]] 

$$
  \overline{\Gamma}
    \coloneqq
  coker( A \overset{\eta}{\longrightarrow} \Gamma)
  \,.
$$ 


=--

+-- {: .num_remak #DirectSumDecompositionUnitCoideal}
###### Remark

By co-unitality of graded commutative Hopf algebras (def. \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents}) $\epsilon \circ \eta = id_A$ the defining projection of the unit coideal (def. \ref{UnitCoidealInCommutativeHopfAlgebra}) 

$$
  A 
    \overset{\eta}{\longrightarrow} 
  \Gamma 
    \overset{}{\longrightarrow}
  \overline{\Gamma}
$$

forms a [[split exact sequence]] which exhibits a [[direct sum]] decomposition

$$
  \Gamma \simeq A \oplus \overline{\Gamma}
  \,.
$$



=--

+-- {: .num_lemma #PropertiesOfUnitCoideal}
###### Lemma

Let $(\Gamma,A)$ be a [[commutative Hopf algebra]], hence a [[commutative Hopf algebroid]] for which the left and right units coincide $\eta \;\colon\; 
A \longrightarrow \Gamma$. 

Then the unit coideal $\overline{\Gamma}$ (def. \ref{UnitCoidealInCommutativeHopfAlgebra}) carries the structure of an $A$-[[bimodule]] such that the [[projection]] morphism

$$
  \Gamma \longrightarrow \overline{\Gamma}
$$

is an $A$-bimodule homomorphism. Moreover, the coproduct $\Psi \;\colon\; \Gamma \longrightarrow \Gamma \otimes_A \Gamma$ descends to a morphism $\overline{\Gamma} \;\colon\; \overline{\Gamma} \longrightarrow \overline{\Gamma} \otimes_A \overline{\Gamma}$ such that the projection intertwines the two coproducts.

=--

+-- {: .proof}
###### Proof

For the first statement, consider the [[commuting diagram]]

$$
  \array{
    A \otimes A 
      &\overset{A \otimes \eta}{\longrightarrow}&
    A \otimes \Gamma
      &\longrightarrow&
    A \otimes \overline{\Gamma}
    \\
    \downarrow && \downarrow && \downarrow^{\mathrlap{\exists}}
    \\
    A 
      &\underset{\eta}{\longrightarrow}&
    \Gamma
      &\longrightarrow&
    \overline{\Gamma}
  }
  \,,
$$

where the left [[commuting square]] exhibits the fact that $\eta$ is a homomorphism of left $A$-modules.

Since the [[tensor product of abelian groups]] $\otimes$ is a [[right exact functor]] it preserves cokernels, hence $A \otimes \overline{\Gamma}$ is the cokernel of $A \otimes A \to A\otimes \Gamma$ and hence the right vertical morphisms exists by the [[universal property]] of cokernels. This is the compatible left module structure on $\overline{\Gamma}$. Similarly the right $A$-module structure is obtained.

For the second statement, consider the [[commuting diagram]]

$$
  \array{
    A 
      &\overset{\eta}{\longrightarrow}&
    \Gamma
      &\longrightarrow&
    \overline{\Gamma}
    \\
    {}^{\mathllap{\eta}}\downarrow
      &&
    \downarrow^{\mathrlap{\Psi}}
      &&
    \downarrow^{\mathrlap{\exists}}
    \\
    \Gamma \simeq \Gamma \otimes_A A 
      &\underset{id \otimes_A \eta}{\longrightarrow}&
    \Gamma \otimes_A \Gamma
      &\longrightarrow&
    \overline{\Gamma} \otimes_A \overline{\Gamma}
  }
  \,.
$$

Here the left square commutes by one of the co-unitality conditions on $(\Gamma,A)$, equivalently this is the co-action property of $A$ regarded canonically as a $\Gamma$-comodule. 

Since also the bottom morphism factors through zero, the [[universal property]] of the cokernel $\overline{\Gamma}$ implies the existence of the right vertical morphism as shown.

=--



+-- {: .num_defn #CobarComplex}
###### Definition
**(cobar complex)**

Let $(\Gamma,A)$ be a [[commutative Hopf algebra]], hence a [[commutative Hopf algebroid]] for which the left and right units coincide $A \overset{\eta}{\longrightarrow} \Gamma$. Let $N$ be a left $\Gamma$-comodule.

The **cobar complex** $C^\bullet_\Gamma(N)$ is the [[cochain complex]] of abelian groups with terms

$$
  C^s_\Gamma(N)
   \coloneqq
    \underset{s\; factors}{
    \underbrace{
    \overline{\Gamma}
      \otimes_A
      \cdots
      \otimes_A
    \overline{\Gamma}
    }
    }
  \otimes_A N
$$

(for $\overline{\Gamma}$ the unit coideal of def. \ref{UnitCoidealInCommutativeHopfAlgebra}, with its $A$-bimodule structure via lemma \ref{PropertiesOfUnitCoideal})

and with [[differentials]] $d_s \colon C^s_\Gamma(N) \longrightarrow C^{s+1}_\Gamma(N)$ given by the alternating sum of the coproducts via lemma \ref{PropertiesOfUnitCoideal}.
 
=--

([Ravenel 86, def. A1.2.11](#Ravenel86))


+-- {: .num_prop #CobarComplexGivesExtGroupsOutOfA}
###### Proposition

Let $(\Gamma,A)$ be a [[commutative Hopf algebra]], hence a [[commutative Hopf algebroid]] for which the left and right units coincide $A \overset{\eta}{\longrightarrow} \Gamma$. Let $N$ be a left $\Gamma$-comodule.

Then the [[cochain cohomology]] of the cobar complex $C^\bullet_\Gamma(N)$ (def. \ref{CobarComplex}) is the [[Ext]]-groups of comodules from $A$ (regarded as a left comodule via def. \ref{ComoduleStructureOnGroundRing}) into $N$

$$
  H^\bullet(C^\bullet_\Gamma(N))
    \;\simeq\;
  Ext^\bullet_\Gamma(A,N)
  \,.
$$

=--

([Ravenel 86, cor. A1.2.12](#Ravenel86), [Kochman 96, prop. 5.2.1](#Kochman96))

+-- {: .proof}
###### Proof idea

One first shows that there is a resolution of $N$ by co-free comodules given by the complex

$$
  D^\bullet_\Gamma(N) 
    \coloneqq 
  \Gamma \otimes_A \overline{\Gamma}^{\otimes_A^{\bullet}} \otimes_A N
$$

with differentials given by the alternating sum of the coproducts. This is called the _cobar resolution_ of $N$.

To see that this is indeed a resolution, one observes that a contracting homotopy is given by 

$$
  s (\gamma \gamma_1\vert \cdots \vert \gamma_s n)
  \coloneqq
  \epsilon(\gamma) \gamma_1\vert \cdots \vert \gamma_s n
$$

for $s \gt 0$ and 

$$
  s(\gamma n) \coloneqq 0
  \,.
$$

Now from lemma \ref{CoFreeHopfComodulesAreHomNAcyclicForProjectiveN}, in view of remark \ref{DirectSumDecompositionUnitCoideal}, and since $A$ is trivially projective over itself, it follows that this is an $F$-acyclic resolution for $F \coloneqq Hom_\Gamma(A,-)$.

This means that the resolution serves to compute the [[Ext]]-functor in question and we get

$$
  \begin{aligned}
    Ext^\bullet_\Gamma(A,N)
      & \simeq
    H^\bullet(Hom_\Gamma(A, D^\bullet_\Gamma(N)))
     \\
      & =
    H^\bullet( Hom_\Gamma(A, \Gamma \otimes_A \overline{\Gamma}^{\otimes_A^{\bullet}} \otimes_A N ) )
     \\
     &\simeq
    H^\bullet( Hom_A(A, \overline{\Gamma}^{\otimes_A^{\bullet}} \otimes_A N ) )
    \\
    & \simeq
    H^\bullet( \overline{\Gamma}^{\otimes_A^{\bullet}} \otimes_A N )
    \,,
  \end{aligned}
  \,,
$$

where the second-but-last equivalence is the isomorphism of the co-free/forgetful adjunction 

$$
  A Mod
    \underoverset
      {\underset{co-free}{\longrightarrow}}
      {\overset{forget}{\longleftarrow}}
      {\bot}
  \Gamma CoMod
$$

from prop. \ref{CoFreeComodules}, while the last equivalence is the isomorphism of the free/forgetful adjunction 

$$
  A Mod
   \underoverset
     {\underset{forget}{\longrightarrow}}
     {\overset{free}{\longleftarrow}}
     {\bot}
  Ab
$$


=--


##### The May spectral sequence

The cobar complex (def. \ref{CobarComplex}) realizes the second page of the [[classical Adams spectral sequence]] (cor. \ref{ClassicalAdamsSpectralSequenceEstablished}) as the [[cochain cohomology]] of a [[cochain complex]]. This is still hard to compute directly, but we now discuss that this cochain complex admits a [[filtered complex|filtration]] so that the induced [[spectral sequence of a filtered complex]] is computable and has trivial extension problem ([rmk.](Introduction+to+Stable+homotopy+theory+--+S#ExtensionProblemForSpectralSequences)). This is called the _[[May spectral sequence]]_.

We obtain this spectral sequence in prop. \ref{MaySpectralSequenceForClassicalAdamsSpectralSequence} below. First we need to consider some prerequisites.

+-- {: .num_lemma #CoModuleExtFromAToAForPrimitivelyGeneratedExteriorAlgebra}
###### Lemma

Let $(\Gamma,A)$ be a graded commutative Hopf algebra, i.e. a [[graded commutative Hopf algebroid]] with left and right unit coinciding for which the underlying $A$-algebra of $\Gamma$ is a free graded commutative $A$-algebra on a set of generators $\{x_i\}_{i \in I}$ 

such that 

1. all generators $x_i$ are [[primitive elements]];

1. $A$ is in degree 0;

1. $(i \lt j) \Rightarrow (deg(x_i) \leq deg(x_j))$;

1. there are only finitely many $x_i$ in a given degree,

then the [[Ext]] of $\Gamma$-comodules from $A$ to itself is the free graded commutative algebra on these generators

$$
  Ext_\Gamma(A,A) \simeq A[\{x_i\}_{i \in I}]
  \,.
$$


=--

([Ravenel 86, lemma 3.1.9](#Ravenel86), [Kochman 96, prop. 3.7.5](#Kochman96))

+-- {: .proof}
###### Proof

Consider the co-free left $\Gamma$-comodule ([prop.](commutative+Hopf+algebroid#CoFreeComodules))

$$
  \Gamma \otimes_A A[\{y_i\}_{i \in I}] 
$$

and regard it as a [[chain complex]] of left comodules by defining a [[differential]] via

$$
  d \colon x_i \mapsto y_i
$$

$$
  d \colon y_i \mapsto 0
$$

and extending as a graded [[derivation]]. 

We claim that $d$ is a homomorphism of left comodules: Due to the assumption that all the $x_i$ are primitive we have on generators that

$$
  \begin{aligned}
    (id,d) ( \Psi(x_i)  )
    & =
    (id,d) ( x_i \otimes 1 + 1 \otimes x_i )
    \\
    & =
    \underset{= 0}{x_i  \otimes \underbrace{(d 1)} }
     + 
    \underset{= y_i}{ 1 \otimes \underbrace{(d x_i)} } 
    \\
    & =
    \Psi( d x_i )
  \end{aligned}
$$

and 

$$
  \begin{aligned}
    (id,d)( \Psi(y_i) )
    & =
    (id,d) ( 1, y_i )
    \\
    & =
    (1, d y_i)
    \\
    & =
    0
    \\
    & =
    \Psi( 0 )
    \\
    & =
    \Psi(d y_i)
  \end{aligned}
  \,.
$$

Since $d$ is a graded derivation on a free graded commutative algbra, and $\Psi$ is an algebra homomorphism, this implies the statement for all other elements.

Now observe that the canonical [[chain map]]

$$
  (\Gamma \otimes_A A[\{y_i\}_{i \in I}]  ,\; d)
    \overset{\simeq_{qi}}{\longrightarrow}
  A
$$

(which projects out the generators $x_i$ and $y_i$ and is the identity on $A$), is a [[quasi-isomorphism]], by construction. Therefore it constitutes a co-free resolution of $A$ in left $\Gamma$-comodules.

Since the counit $\eta$ is assumed to be flat, and since $A[\{y_i\}_{i \in I}]$ is degreewise a [[free module]] over $A$, hence in particular a [[projective module]], prop. \ref{CoFreeHopfComodulesAreHomNAcyclicForProjectiveN} says that the above is an [[acyclic resolution]] with respect to the functor $Hom_{\Gamma}(A,-) \colon \Gamma CoMod \longrightarrow A Mod$. Therefore it computes the [[Ext]]-functor. Using that forming co-free comodules is [[right adjoint]] to forgetting $\Gamma$-comodule structure over $A$ (prop. \ref{CoFreeComodules}), this yields:

$$
  \begin{aligned}
    Ext^\bullet_\Gamma(A,A)
    & \simeq
    H_\bullet(Hom_\Gamma(A,  \Gamma \otimes_A A[\{y_i\}_{i \in I}] ), d)
    \\
    & \simeq 
    H_\bullet(Hom_A(A,  A[\{y_i\}_{i \in I}] ), d= 0 )
    \\
    & \simeq
    Hom_A(A,  A[\{y_i\}_{i \in I}] )
    \\
    & \simeq
    A[\{x_i\}_{i \in I}]
  \end{aligned}
  \,.
$$

=--



+-- {: .num_lemma #SpectralSequenceConvergingToExtForFilteredHopfAlgebra}
###### Lemma

If $(\Gamma,A)$ as above is equipped with a [[filtering]], then there is a [[spectral sequence]]

$$
  \mathcal{E}_1
  \;=\;
  Ext_{gr_\bullet \Gamma}(gr_\bullet A, gr_\bullet A)
  \;\Rightarrow\;
  Ext_{\Gamma}(A, A)
$$

converging to the [[Ext]] over $\Gamma$ from $A$ to itself, whose first page is the $Ext$ over the [[associated graded]] Hopf algebra $gr_\bullet \Gamma$.

=--

([Ravenel 86, lemma 3.1.9](#Ravenel86), [Kochman 96, prop. 3.7.5](#Kochman96))

+-- {: .proof}
###### Proof

The filtering induces a filtering on the cobar complex (def. \ref{CobarComplex}) which computes $Ext_\Gamma$ (prop. \ref{CobarComplexGivesExtGroupsOutOfA}). The spectral sequence in question is the corresponding [[spectral sequence of a filtered complex]]. Its first page is the homology of the associated graded complex (by this [prop.](spectral+sequence+of+a+filtered+complex#FirstPages)), which hence is the homology of the cobar complex (def. \ref{CobarComplex}) of the [[associated graded]] Hopf algebra $gr_\bullet \Gamma$. By prop. \ref{CobarComplexGivesExtGroupsOutOfA} this is the [[Ext]]-groups as shown.

=--

Let now $A \coloneqq \mathbb{F}_2$,  $\Gamma \coloneqq \mathcal{A}^\bullet_{2}$ be the mod 2 [[dual Steenrod algebra]]. By [[Milnor's theorem]] (prop. \ref{MilnorTheoremOnDualSteenrodAlgebra}), as an $\mathbb{F}_2$-algebra this is

$$
  \mathcal{A}^\bullet_{2} 
  = 
  Sym_{\mathbb{F}_2}(\xi_1, \xi_2, \cdots)
  \,.
$$

and the coproduct is given by

$$
  \Psi(\xi_n)
  =
  \underoverset{k = 0}{i}{\sum} \xi_{i - k}^{2^k} \otimes \xi_k
  \,,
$$

where we set $\xi_0 \coloneqq 1$.

+-- {: .num_defn #hGeneratorsinClassicalAdamsSpectralSequence}
###### Definition

Introduce new generators

$$
  h_{i,n} 
    \coloneqq 
  \left\{
    \array{
      \xi_i^{2^n} & for \; i \geq 1, \, k \geq 0
      \\
      1 & for \; i = 0
    }
  \right.
$$

=--

+-- {: .num_remark #hGeneratorsForSteenrodAlgebraGiveUniqueDecompositionOfMonomials}
###### Remark


By binary expansion of powers, there is a unique way to express every monomial in $\mathbb{F}_2[\xi_1, \xi_2, \cdots]$ as a product of the new generators in def. \ref{hGeneratorsinClassicalAdamsSpectralSequence}
such that each such element appears at most once in the product. E.g.

$$
  \begin{aligned}
    \xi_i^5 \xi_j^7 
      & = 
    \xi_i^{2^0 + 2^2} \xi_j^{2^0 + 2^1 + 2^2}
     \\
     & = 
     h_{i,0} h_{i,1} h_{j,0} h_{j,1} h_{j,2}
  \end{aligned}
  \,.
$$

=--

+-- {: .num_prop #CoproductOnDualSteenrodInTermsOfAdaptedGenerators}
###### Proposition

In terms of the generators $\{h_{i,n}\}$ from def. \ref{hGeneratorsinClassicalAdamsSpectralSequence}, the coproduct on the dual [[Steenrod algebra]] $\mathcal{A}^\ast_{2}$ takes the following simple form

$$
  \Psi(h_{i,n})
   \;=\; 
  \underoverset{k = 0}{i}{\sum} h_{i-k,n+k}\otimes h_{k,n}
  \,.
$$

=--

+-- {: .proof}
###### Proof

Using that the coproduct of a [[bialgebra]] is a [[homomorphism]] for the algebra structure and using [[freshman's dream]] arithmetic over $\mathbb{F}_2$, one computes:

$$
  \begin{aligned}
    \Psi(h_{i,n})
    & = 
    \Psi\left(\xi_i^{2^n}\right)
    \\
    & = (\Psi(\xi_i))^{2^n}
    \\
    & = 
    \left(\underoverset{k = 0}{i}{\sum} \xi_{i-k}^{2^k} \otimes \xi_k\right)^{2^n}
    \\
    & = \underoverset{k = 0}{i}{\sum} \left(\xi_{i-k}^{2^k}\right)^{2^n} \otimes \xi^{2^n}_k
    \\
    & = \underoverset{k = 0}{i}{\sum} \xi_{i-k}^{2^k \cdot 2^n} \otimes \xi^{2^n}_k
    \\
    & = \underoverset{k = 0}{i}{\sum} \xi_{i-k}^{2^{(k+n)}} \otimes \xi^{2^n}_k
    \\
    & = \underoverset{k = 0}{i}{\sum} h_{i-k,n+k}\otimes h_{k,n}
  \end{aligned}
  \,.
$$

=--



+-- {: .num_prop #MaySpectralSequenceForClassicalAdamsSpectralSequence}
###### Proposition

There exists a converging [[spectral sequence]] of graded $\mathbb{F}_2$-vector spaces of the form

$$
  E_1^{s,t,p}
  =
  \mathbb{F}_2[ \{ h_{i,n} \}_{{i \geq 1,} \atop {n \geq 0}}]  
    \;\Rightarrow\;
  Ext^{s,t}_{\mathcal{A}_2^\ast}(\mathbb{F}_2, \mathbb{F}_2)
  \,,
$$

called the **[[May spectral sequence]]** (where $s$ and $t$ are from the bigrading of the spectral sequence itself, while the index $p$ is that of the graded $\mathbb{F}_2$-vector spaces), with 

1. $h_{i,n} \in E_1^{1, 2^{2^{i+n} - 2^n - 1, 2i - 1 }}$

1. first differential given by

   $$
     d_1 (h_{i,n})
     =
     \underoverset{k = 0}{i}{\sum} h_{i-k,n+k}\otimes h_{k,n}  
     \,;
   $$

1. higher differentials of the form

   $$
     d_r
       \;\colon\;
     E_r^{s,t, p}
       \longrightarrow
     E_r^{s+1, t-1, p-2r+1}
     \,,
   $$

   where the filtration is by maximal degree.

Notice that since everything is $\mathbb{F}_2$-linear, the [extension problem](Introduction+to+Stable+homotopy+theory+--+S#ExtensionProblemForSpectralSequences) of this spectral sequence is trivial.

=--

([Kochman 96, prop. 5.3.1](#Kochman96))


+-- {: .proof}
###### Proof


Define a [[graded algebra|grading]] on the dual [[Steenrod algebra]] $\mathcal{A}^\bullet_{2}$ (theorem \ref{MilnorTheoremOnDualSteenrodAlgebra}) by taking the degree of the generators from def.\ref{hGeneratorsinClassicalAdamsSpectralSequence} to be (this idea is due to ([Ravenel 86, p.69](#Ravenel86)))

$$
  {\vert h_{i,n} \vert}
    \coloneqq
  2i-1
$$

and extending this additively to monomials, via the unique decomposition of remark \ref{hGeneratorsForSteenrodAlgebraGiveUniqueDecompositionOfMonomials}.

For example

$$
  \begin{aligned}
    \vert \xi_i^5 \xi_j^7\vert
    & = 
    {\vert h_{i,0} h_{i,1} h_{j,0} h_{j,1} h_{j,2} \vert} 
    \\
    & =
    2(2i-1) + 3(2j-1)
  \end{aligned}
  \,.
$$

Consider the corresponding increasing [[filtration]]

$$
  \cdots 
   \subset
  F_p \mathcal{A}^\ast_{2}
   \subset
  F_{p+1} \mathcal{A}^\ast_{2}
    \subset 
  \cdots 
    \subset
  \mathcal{A}^\ast_{2}
$$

with filtering stage $p$ containing all elements of total degree $\leq p$.

Observe via prop. \ref{CoproductOnDualSteenrodInTermsOfAdaptedGenerators} that

$$
  \begin{aligned}
    \Psi(h_{i,n})
    &
   =
   \underset{deg = 2i-1}{\underbrace{h_{i,n} \otimes 1}}
   +
    \underoverset{0 \lt k \lt i}{}{\sum} 
     \underset{deg = 2i-2}{\underbrace{h_{i-k,n+k} \otimes h_{k,n}}}
   +
    \underset{deg = 2i-1}{\underbrace{1 \otimes h_{i,n} }}
  \end{aligned}
  \,.
$$

This means that after projection to the [[associated graded]] Hopf algebra

$$
  F_\bullet \mathcal{A}^\ast_{2}
   \longrightarrow
  gr_\bullet \mathcal{A}^\ast_{2}
  \coloneqq
  F_\bullet( \mathcal{A}^\ast_2)/F_{\bullet-1}( \mathcal{A}^\ast_2 ) 
$$ 

all the generators $h_{i,n}$ become [[primitive elements]]:

$$
  \begin{aligned}
    \Psi(h_{i,n})
    &
   =
   h_{i,n}\otimes 1
   +
   1 \otimes h_{i,n}
   \;\;\;\;\;
   \in 
   gr_\bullet \mathcal{A}^\ast_{2}
   \otimes
   gr_\bullet \mathcal{A}^\ast_{2}
  \end{aligned}
  \,.
$$


Hence lemma \ref{CoModuleExtFromAToAForPrimitivelyGeneratedExteriorAlgebra} applies and says that the $Ext$ from $\mathbb{F}_2$ to itself over the [[associated graded]] Hopf algebra is the polynomial algebra in these generators:

$$
  Ext_{gr_\bullet \mathcal{A}^\ast_{2}}(\mathbb{F}_2,\mathbb{F}_2)
    \simeq
  \mathbb{F}_2[\{h_{i,n}\}_{{i \geq 1,} \atop {n \geq 0}}]  
  \,.
$$

Moreover, lemma \ref{SpectralSequenceConvergingToExtForFilteredHopfAlgebra} says that this is the first page of a spectral sequence that converges to the $Ext$ over the original Hopf algebra:

$$
  \mathcal{E}_1 
  = 
  \mathbb{F}_2[\{h_{i,n}\}_{{i \geq 1} \atop {n \geq 0}}]
  \;\Rightarrow\;
  Ext_{\mathcal{A}^\ast_{2}}(\mathbb{F}_2,\mathbb{F}_2)
  \,.
$$

Moreover, again by lemma \ref{SpectralSequenceConvergingToExtForFilteredHopfAlgebra}, the differentials on any $r$-page are the restriction of the differentials of the bar complex to the $r$-almost cycles ([prop.](Introduction+to+Stable+homotopy+theory+--+I#DifferentialsOnAlmostChains)). Now the differential of the cobar complex is the alternating sum of the coproduct on $\mathcal{A}^\ast_{2}$, hence by prop. \ref{CoproductOnDualSteenrodInTermsOfAdaptedGenerators} this is:

$$
  d_1 (h_{i,n})
  =
  \underoverset{k = 0}{i}{\sum} h_{i-k,n+k}\otimes h_{k,n}  \,.
$$

=--

##### The second page

Now we use the [[May spectral sequence]] (prop. \ref{MaySpectralSequenceForClassicalAdamsSpectralSequence}) to compute the second page and in fact the stable page of the [[classical Adams spectral sequence]] (cor. \ref{ClassicalAdamsSpectralSequenceEstablished}) in low internal degrees $t-s$.




+-- {: .num_lemma #TermsOnSecondPageOfMaySpectralSequenceInLowDegrees}
###### Lemma
**(terms on the second page of May spectral sequence)**

In the range $t - s \leq 13$, the second page of the May spectral sequence for $Ext_{\mathbb{A}^\ast_{\mathbb{F}_2}}(\mathbb{F}_2,\mathbb{F}_2)$ has as generators all the 

* $h_n$

* $b_{i,n} \coloneqq (h_{i,n})^2$

as well as the element

*  $x_7 \coloneqq h_{2,0} h_{2,1} + h_{1,1} h_{3,0}$

subject to the relations

* $h_n h_{n+1} = 0$

* $h_2 b_{2,0} = h_0 x_7$

* $h_2 x_7 = h_0 b_{2,1}$.

=--

e.g. ([Ravenel 86, lemma 3.2.8 and lemma 3.2.10](#Ravenel86), [Kochman 96, lemma 5.3.2](#Kochman96))

+-- {: .proof}
###### Proof

Remember that the differential in the cobar complex (def. \ref{CobarComplex}) lands not in $\Gamma = \mathcal{A}^\ast_2$ itself, but in the unit coideal $\overline{\Gamma} \coloneqq coker(\eta)$ where the generator $h_{0,n} = \xi_0 = 1$ disappears.

Using this we find for the differential $d_1$ of the generators in low degree on the first page of the [[May spectral sequence]] (prop. \ref{MaySpectralSequenceForClassicalAdamsSpectralSequence}) via the formula for the differential from prop. \ref{CoproductOnDualSteenrodInTermsOfAdaptedGenerators}, the following expressions:

$$
  \begin{aligned}
    d_1(h_n)
    & \coloneqq
    d_1(h_{1,n})
    \\
    & =   
    \overline{\Psi}(h_{1,n})
    \\
    & =
    h_{1,n} \otimes \underset{= 0}{\underbrace{ h_{0,n} }}
    + 
    \underset{= 0}{\underbrace{ h_{0,n+1} }} \otimes h_{1,n}
    \\
    & = 
    0
  \end{aligned}
$$

and hence all the elements $h_n$ are cocycles on the first page of the May spectral sequence.

Also, since $d_1$ is a [[derivation]] (by definition of the cobar complex, def. \ref{CobarComplex}) and since the product of the image of the cobar complex in the first page of the May spectral sequence is graded commutative, we have for all $n,k$ that

$$
  \begin{aligned}
    d_1 (h_{n,k})^2
    & =
    2 h_{n,k} (d_1 (h_{n,k}))
    \\
    & = 0
  \end{aligned}
$$

(since $2 = 0 \; mod \; 2$).


Similarly we compute $d_1$ on the other generators. These terms do not vanish, but so they impose relations on products in the cobar complex:

$$
  \begin{aligned}
    d_1(h_{2,0}) 
    & = 
    h_{1,1} \otimes h_{1,0}
    \\
    d_1( h_{2,1} )
    & =
    h_{1,2} \otimes h_{1,1}
    \\
    d_1( h_{2,2} )
     & =
    h_{1,3} \otimes h_{1,2}
    \\
    d_1( h_{2,3} )
    & =
    h_{1,4} \otimes h_{1,3}
    \\
    d_1( h_{3,0} )
     & =
    h_{2,1} \otimes h_{1,0}
    +
    h_{1,2} \otimes h_{2,0}
  \end{aligned}
$$

This shows that $h_n h_{n+1} = 0$ in the given range.

The remaining statements follow similarly.

=--

+-- {: .num_remark #PictureFromTermsOnSecondPageOfMaySpectralSequence} 
###### Remark

With lemma \ref{TermsOnSecondPageOfMaySpectralSequenceInLowDegrees}, so far we see the following picture in low degrees.

$$
  \array{
    \vdots & \vdots
    \\
    3 & h_0^4 & & &  {h_1^3},\; {h_0^2 h_2}
    \\
    2 & h_0^2 & & h_1^2 & h_0 h_2
    \\
    1& h_0 & h_1 & & h_2
     \\
     & 0 & 1 & 2& 3 & 4
  }
$$

Here the relation 

$$
  h_0 \otimes h_1 = 0
$$ 

removes a vertical tower of elements above $h_1$.

So far there are two different terms in degree $(s,t-s) = (3,3)$. The next lemma shows that these become identified on the next page.

=--



+-- {: .num_lemma #DifferentialsOnSecondPageOfMaySpectralSequence}
###### Lemma
**(differentials on the second page of the May spectral sequence)**

The differentials on the second page of the [[May spectral sequence]] (prop. \ref{MaySpectralSequenceForClassicalAdamsSpectralSequence}) relevant for internal degrees $t-s \leq 12$ are

1. $d_2(h_{n}) = 0$

1. $d_2(b_{2,n}) = h_n^2 h_{n+2} + h_{n+1}^3$

1. $d_2(x_7) = h_0 h_2^2$

1. $d_2(b_{3,0}) = h_1 b_{2,1} + h_3 b_{2,0}$

=--

([Kochman 96, lemma 5.3.3](#Kochman96))

+-- {: .proof}
###### Proof

The first point follows as before in lemma \ref{TermsOnSecondPageOfMaySpectralSequenceInLowDegrees}, in fact the $h_n$ are infinite cycles in the May spectral sequence.

We spell out the computation for the second item:

We may represent $b_{2,k}$ by $\xi_2^{2^k} \times \xi_2^{2^k}$
plus terms of lower degree. Choose the representative

$$
  B_{2,k}
    =
  \xi_2^{2^k} \otimes \xi_2^{2^k}
    \;+\;
   \xi_1^{2^{k + 1}} \otimes \xi_1^{2^k} \xi_2^{2^k} 
     \;+\;
   \xi_1^{2^{k+1}} \xi^{2^k} \otimes \xi_1^{2^k}
   \,.
$$

Then we compute $d B_{2,k}$, using the definition of the cobar complex (def. \ref{CobarComplex}), the value of the coproduct on dual generators (theorem \ref{MilnorTheoremOnDualSteenrodAlgebra}), remembering that the coproduct $\Psi$ on a Hopf algebra is a homomorphism for the underlying commutative ring, and using [[freshman's dream]] arithmetic to evaluate prime-2 powers of sums. For the three summands we obtain

$$
  \begin{aligned}
    d ( \xi_2^{2^k}  \otimes \xi_2^{2^k})
    & = 
    \overline{\Psi} (\xi_2^{2^k}) \otimes \xi_2^{2^k}
    +  
    \xi_2^{2^k} \otimes \overline{\Psi}(\xi_2^{2 k})
    \\
    & =
    \underset{c_1}{\underbrace{\xi_1^{2^{k+1}} \otimes \xi_1^{2^k} \otimes \xi_2^{2^k}}}
    \;+\; 
    \underset{c_2}{\underbrace{\xi_2^{2^k} \otimes \xi_1^{2^{k+1}} \otimes \xi_1^{2^k}}}
  \end{aligned}
$$

and

$$
  \begin{aligned}
    d ( \xi_1^{2^{k + 1}} \otimes \xi_1^{2^k} \xi_2^{2^k} )
    & =
    \xi_1^{2^k} \otimes \overline{\Psi}( \xi_1^{2^k} \xi_2^{2^k})
    \\
    & = 
    \xi_1^{2^{k + 1}} 
    \otimes
    \left(
      \xi_1^{2^k} \otimes 1
        + 
      1 \otimes \xi_1^{2^k}
    \right)
    \left(
      \xi_2^{2^k} \otimes 1
        +
      \xi_1^{2^{k+1}} \otimes \xi_1^{2^k}
        +
      1 \otimes \xi_2^{2^k}
    \right)
    \\
    & =
    \underset{b}{
    \underbrace{
      \xi_1^{2^{k + 1}} \otimes \xi_1^{2^{k+1}+ 2^k} \otimes \xi_1^{2^k}
    }}
      \;+\;
    \underset{c_1}{\underbrace{
      \xi_1^{2^{k+1}} \otimes \xi_1^{2^k} \otimes \xi_2^{2^k}
    }}
      \;+\; 
    \underset{a}{\underbrace{
      \xi_1^{2^{k+1}} \otimes \xi_2^{2^k} \otimes \xi_1^{2^k}
    }}
      \;+\;
    \xi_1^{2^{k+1}} \otimes \xi_1^{2^{k+1}} \otimes \xi_1^{2^{k+1}}
  \end{aligned}
$$

and

$$
  \begin{aligned}
    d( \xi_1^{2^{k+1}} \xi^{2^k} \otimes \xi_1^{2^k} )
    &
    =
    \overline{\Psi}( \xi_1^{2^{k+1}} \xi^{2^k} ) \otimes \xi_1^{2^k}
    \\
    & =
    \left(
      \xi_1^{2^{k+1}} \otimes 1
        +
      1 \otimes \xi_1^{2^{k+1}}
    \right)
    \left(
      \xi_2^{2^k} \otimes 1
        +
      \xi_1^{2^{k+1}} \otimes \xi_1^{2^k}
        +
      1 \otimes \xi_2^{2^k}
    \right)
      \otimes
    \xi_1^{2^k}
    \\
    & =
    \xi_1^{2^{k+2}} \otimes \xi_1^{2^k} \otimes \xi_1^{2^k}
      \;+\;
    \underset{a}{\underbrace{
      \xi_1^{2^{k+1}} \otimes \xi_2^{2^k} \otimes \xi_1^{2^k}
    }}
      \;+\;
    \underset{c_2}{\underbrace{
      \xi_2^{2^k} \otimes \xi_1^{2^{k+1}} \otimes \xi_1^{2^k} 
    }}
      \;+\;
    \underset{b}{\underbrace{
      \xi_1^{2^{k+1}} \otimes \xi_1^{2^{k+1} + 2^k} \otimes \xi_1^{2^k}
    }}
  \end{aligned}
  \,.
$$

The labeled summands appear twice in $d B_{2,k}$ hence vanish (mod 2). The remaining terms are

$$
  d B_{2,k}
  =
  \xi_1^{2^{k+1}} \otimes \xi_1^{2^{k+1}} \otimes \xi_1^{2^{k+1}}
   \;+\;
  \xi_1^{2^{k+2}} \otimes \xi_1^{2^k} \otimes \xi_1^{2^k}
$$

and these indeed represent the claimed elements.


=--

+-- {: .num_remark } 
###### Remark

With lemma \ref{DifferentialsOnSecondPageOfMaySpectralSequence} the picture from remark \ref{PictureFromTermsOnSecondPageOfMaySpectralSequence} is further refined:

For $k = 0$ the differentia $d_2(b_{2,n}) = h_n^2 h_{n+2} + h_{n+1}^3$ means that on the third page of the May spectral sequence there is an identification

$$
  h_1^3 = h_0^2 h_2
  \,.
$$

Hence where on page two we saw two distinct elements in bidegree $(s,t-s) = (3,3)$, on the next page these merge:


$$
  \array{
    \vdots & \vdots
    \\
    3 & h_0^4 & & &  {h_1^3} = {h_0^2 h_2}
    \\
    2 & h_0^2 & & h_1^2 & h_0 h_2
    \\
    1& h_0 & h_1 & & h_2
     \\
     & 0 & 1 & 2& 3 & 4
  }
$$


=--

Proceeding in this fashion, one keeps going until the 4-page of the May spectral sequence ([Kochman 96, lemma 5.3.5](#Kochman96)). Inspection of degrees shows that this is sufficient, and one obtains:

+-- {: .num_theorem #TheStablePageOfTheClassicalAdamsSpectralSequenceInLowDegree}
###### Theorem
**(stable page of classical Adams spectral sequence)**

In internal degree $t-s \leq 12$ the infinity page (def. \ref{InfinityPageEAdams}) of the [[classical Adams spectral sequence]] (cor. \ref{ClassicalAdamsSpectralSequenceEstablished}) is spanned by the items in the following table

<img src="http://ncatlab.org/nlab/files/ClassicalAdamsSpectralSequence.jpg" width="600" >

Here every dot is a generator for a copy of $\mathbb{Z}/2\mathbb{Z}$. Vertical edges denote multiplication with $h_0$ and diagonal edges denotes multiplication with $h_1$. 

=--

e.g. ([Ravenel 86, theorem 3.2.11](#Ravenel86), [Kochman 96, prop. 5.3.6](#Kochman96)), graphics taken from ([[Symmetric spectra|Schwede 12]]))

##### The first dozen stable stems
 {#StableStems}

Theorem \ref{TheStablePageOfTheClassicalAdamsSpectralSequenceInLowDegree} gives the stable page of the [[classical Adams spectral sequence]] in low degree. By corollary \ref{ClassicalAdamsSpectralSequenceEstablished} and def. \ref{EAdamsConvergingCompletely} we have that a vertical sequence of dots encodes an 2-primary part of the stable homotopy groups of spheres according to the graphical calculus of remark \ref{PrimaryDecompositionGraphicalRepresentation} (the rules for determining group extensions there is just the solution to the extension problem ([rmk.](Introduction+to+Stable+homotopy+theory+--+S#ExtensionProblemForSpectralSequences)) in view of def. \ref{EAdamsConvergingCompletely}):



| $k =$ | 0 | 1 | 2 | 3 | 4  | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 | 13 | 
|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|
| $\pi_k(\mathbb{S}\otimes \mathbb{Z}_{(2)}) = $ | $\mathbb{Z}_{(2)}$  | $\mathbb{Z}/2$  |  $\mathbb{Z}/2$ |  $\mathbb{Z}/8$ |  $0$ |  $0$ | $\mathbb{Z}/2$ |   $\mathbb{Z}/16$ | $(\mathbb{Z}/2)^2$ |  $(\mathbb{Z}/2)^3$ | $\mathbb{Z}/2$ | $\mathbb{Z}/8$ | $0$ | $0$ | 

The full answer in this range turns out to be this:


| $k =$ | 0 | 1 | 2 | 3 | 4  | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 | 13 | 14 | 15 | $\cdots$ | 
|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|
| $\pi_k(\mathbb{S}) = $ | $\mathbb{Z}$  | $\mathbb{Z}_2$  |  $\mathbb{Z}_2$ |  $\mathbb{Z}_{24}$ |  $0$ |  $0$ | $\mathbb{Z}_2$ |   $\mathbb{Z}_{240}$ | $(\mathbb{Z}_2)^2$ |  $(\mathbb{Z}_2)^3$ | $\mathbb{Z}_6$ | $\mathbb{Z}_{504}$ | $0$ | $\mathbb{Z}_3$ | $(\mathbb{Z}_2)^2$ | $\mathbb{Z}_{480} \oplus \mathbb{Z}_2$ | $\cdots$ |

And expanding the range yields this :

<img src="http://www.math.cornell.edu/~hatcher/stemfigs/p%3D2pic.gif" alt="stable homotopy groups of spheres at 2" width="800" />

(graphics taken from [Hatcher's website](http://www.math.cornell.edu/~hatcher/))




































### $E$-injective resolutions
 {#ViaInjectiveResolutions}

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

The notation for $\overline{E}$ in def. \ref{NormalizedEResolution} follows ([Bousfield 79, section 5](#Bousfield79)). In ([Hopkins 99, proof of corollary 5.3](#Hopkins99)) the same notation is used not for the homotopy fiber of $\mathbb{S} \overset{e}{\to} E$ but for its homotopy cofiber. While our notation makes plenty of "$\Sigma$"s appear in the above resolution, the advantage is that in the induced inverse sequence of a normalized resolution below in example \ref{NormalizedEResolutionAssociatedSequence} these all drop out and we are left with the original form of the expressions as considered by ([Adams 74](#Adams74)) and followed in most of the literature. 

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
    I_0 && \Sigma^{-1} I_1 && \Sigma^{-2} I_2
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


+-- {: .num_remark #TerminologyAssociatedInverseSequence}
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



### As derived descent in $E_\infty$-geometry
 {#DefinitionInHigherAlgebra}

It turns out that the [[E-nilpotent completion]] $X^\wedge_E$ according to [[Aldridge Bousfield|Bousfield]]'s original definition \ref{ENilpotentCompletion} -- to which the $E$-Adams spectrum seequence converges under good conditions (theorem \ref{EAdamsConvergenceForCorepi0EBeingZLocalizedAtPrimes}, theorem \ref{EAdamsConvergenceForCorepi0EBeingCyclicGroup}) -- is equivalently the homotopy limit over the tower of [[totalizations]] of the canonical [[cosimplicial object|cosimplicial]] spectrum $E^\bullet \wedge X$ ([prop.](nilpotent+completion+of+spectra#ENilpotentCompletionIsHolimOverTotTower)).

This means that the $E$-[[Adams spectral sequence]] may equivalently be regarded as computing [[descent]] of [[quasicoherent infinity-stacks]] in [[E-infinity geometry]] along the canonical morphisms $Spec(E)\longrightarrow $ [[Spec(S)]]. 

This perspective seems to originate in ([Hopkins 99, remark 5.5 (ii)](#Hopkins99)) and is greatly expanded on in 
([Lurie 10, lectures 8, 9](#Lurie10)).  Exposition of the basic idea is in [Mathew 12](#Mathew12) and with more details in ([Wilson 13](#Wilson13)). The first published proof of the equivalence of this new perspective to the Adams-Bousfield theory is ([Mathew-Naumann-Noel 15, prop. 2.14](#MathewNaumannNoel15)).

We give a survey here.

> under construction

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

* [[d-invariant]], [[e-invariant]], [[f-invariant]]

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

The [[spectrum]]-level discussion of the ASS goes back to around

* R. M. F. Moss, _On the composition pairing of Adams spectral sequences_, Proceedings of the London Mathematical Society 3.1 (1968): 179-192.


The general convergence theorems are due to

* {#Bousfield79} [[Aldridge Bousfield]], _The localization of spectra with respect to homology_, Topology 18 (1979), no. 4, 257--281. ([pdf](http://www.uio.no/studier/emner/matnat/math/MAT9580/v12/undervisningsmateriale/bousfield-topology-1979.pdf))

* {#Ravenel84} [[Douglas Ravenel]], _Localization with respect to certain periodic homology theories_, American Journal of Mathematics, Vol. 106, No. 2, (Apr., 1984), pp. 351-414 ([pdf](https://www.math.rochester.edu/people/faculty/doug/mypapers/loc.pdf))

based on

* {#BousfieldKan72} [[Aldridge Bousfield]], [[Daniel Kan]], _The core of a ring_, Journal of Pure and Applied Algebra, Volume 2, Issue 1, April 1972, Pages 73-81


A streamlined presentation of Adams resolutions and their invariance properties, close in spirit to the theory of injective resolutions in [[homological algebra]] was given in

* {#Miller81} [[Haynes Miller]], _On relations between Adams spectral sequences, with an application to the stable homotopy of a Moore space_, J. Pure Appl. Algebra 20 (1981) ([pdf](http://math.mit.edu/~hrm/papers/miller-relations-between-adams-spectral-sequences.pdf))

further highlighted in 

* {#Hopkins99} [[Mike Hopkins]], section 5 of _[[Complex oriented cohomology theories and the language of stacks]]_, course notes 1999 ([[HopkinsComplexOrientedCohomology.pdf:file]])

and worked out in some more detail in

* {#Aramian} [[Nersés Aramian]], _The Adams spectral sequence_ ([[AramianANSS.pdf:file]])

For full details of some of the steps involved see also ([Schwede 12](#Schwede12)).

Reviews of the traditional theory include

* {#Ravenel86} [[Doug Ravenel]], _[[Complex cobordism and stable homotopy groups of spheres]]_, 1986 onwards

* {#Kochmann96} [[Stanley Kochman]], section 3.6 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* {#McCleary01} [[John McCleary]], chapter 9 of _[A user's guide to spectral sequences](https://pages.vassar.edu/mccleary/books/users-guide-to-spectral-sequences/)_, Cambridge University Press, 2001 

* {#Ravenel06} [[Doug Ravenel]], _A Novice's guide to the Adams-Novikov spectral sequence_, in Geometric Applications of Homotopy Theory II Volume 658 of the series Lecture Notes in Mathematics pp 404-475, 2006(?)

* {#Goerss2007} [[Paul Goerss]], _The Adams-Novikov spectral sequence and the Homotopy Groups of Spheres_, lecture notes 2007 ([pdf](http://www.math.northwestern.edu/~pgoerss/papers/stras1.pdf))

* [[Alan Hatcher]], _[Spectral sequences in algebraic topology](http://www.math.cornell.edu/~hatcher/SSAT/SSATpage.html)_ _II: The Adams spectral sequence_ ([pdf](http://www.math.cornell.edu/~hatcher/SSAT/SSch2.pdf))

* {#Bruner09} [[Robert Bruner]], _An Adams spectral sequence primer_, 2009 ([pdf](http://www.math.wayne.edu/~rrb/papers/adams.pdf))

* {#Schwede12} [[Stefan Schwede]], chapter II, section 10.3 of  _[[Symmetric spectra]]_, 2012

* {#Rognes12} [[John Rognes]], _The Adams spectral sequence_ (following [Bruner 09](#Bruner09)), 2012 ([pdf](http://folk.uio.no/rognes/papers/notes.050612.pdf))

* _[[Introduction to the Adams Spectral Sequence]]_

The modern point of view in terms of derived $E_\infty$-descent is hinted at in ([Hopkins 99, remark 5.5 (ii)](#Hopkins99)) and is consistently adopted in

* {#Lurie10} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_ (2010)

  * lecture 8, _The Adams Spectral Sequence_ ([pdf] (http://www.math.harvard.edu/~lurie/252xnotes/Lecture8.pdf))
  
  * lecture 9, _The Adams Spectral Sequence for $MU$_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture9.pdf))

  * lecture 10, _The proof of Quillen's theorem_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture10.pdf))

  * lecture 30, _Localizations and the Adams-Novikov Spectral Sequence_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture30.pdf))

based on 

* {#Lurie} [[Jacob Lurie]], _[[Higher Algebra]]_

This is nicely surveyed in

* {#Mathew12} [[Akhil Mathew]], _[The Adams spectral sequence as derived descent, and chromotopy](https://amathew.wordpress.com/2012/09/21/3844/)_, 2012

* {#Wilson13} [[Dylan Wilson]], _Spectral Sequences from Sequences of Spectra: Towards the Spectrum of the Category of Spectra_, lecture at [2013 Pre-Talbot Seminar](https://www.hiroleetanaka.com/pretalbot2013/), March 2013 ([[DylanWilsonOnANSS.pdf:file]])

The actual proof that this new perspecive is equivalent the original Adams-Bousfield theory appears as prop. 2.14 in

* {#MathewNaumannNoel15} [[Akhil Mathew]], [[Niko Naumann]], [[Justin Noel]], _Nilpotence and descent in equivariant stable homotopy theory_, Advances in Mathematics Volume 305, 10 January 2017, Pages 994-1084 ([arXiv:1507.06869](http://arxiv.org/abs/1507.06869), [doi:10.1016/j.aim.2016.09.027](https://doi.org/10.1016/j.aim.2016.09.027))


 
### Hopf algebroid $Ext$-structure on $E^2$
 {#ReferencesHopfAlgebroidStructure}

* appendix A.1 of [Ravenel 86](#Ravenel86)

* {#Baker} [[Andrew Baker]], _Brave new Hopf algebroids and the Adams spectral sequence for $R$-modules_ ([pdf](http://www.maths.gla.ac.uk/~ajb/dvi-ps/brave-ha.pdf))
 

* {#BakerLazarev01} [[Andrew Baker]], [[Andrey Lazarev]], _On the Adams Spectral Sequence for $R$-modules_, Algebr. Geom. Topol. 1 (2001) 173-199 ([arXiv:math/0105079](http://arxiv.org/abs/math/0105079))
 

* {#BakerJeanneret02} [[Andrew Baker]] and Alain Jeanneret, _Brave new Hopf algebroids and extensions of $MU$-algebras_, Homology Homotopy Appl. Volume 4, Number 1 (2002), 163-173. ([Euclid](http://projecteuclid.org/euclid.hha/1139840059))
 

* {#Hovey03} [[Mark Hovey]], _Homotopy theory of comodules over a Hopf algebroid_ ([arXiv:math/0301229](http://arxiv.org/abs/math/0301229)) 
 
### Further examples with more general coefficients

For [[tmf]]:

* [[Mark Behrens]], _The Adams spectral sequence for $tmf$_ ([[BehrensANSSfortmf.pdf:file]])

* [[Michael Hill]], _The 3-local $tmf$-homology of $B \Sigma_3$_, Proceedings of the AMS, 2007 ([pdf](http://www.ams.org/journals/proc/2007-135-12/S0002-9939-07-08937-X/S0002-9939-07-08937-X.pdf))

[[!redirects Adams spectral sequences]]

[[!redirects Adams spectral sequences]]
