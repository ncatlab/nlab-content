
{:bluebox: .un_remark style="border:solid #000000;background: #E6DF13;border-width:2px 1px;padding:0 1em;margin:0 1em;"}

***



+-- {: .standout}


[V4D2 -- Algebraic Topology II](https://basis.uni-bonn.de/qisserver/rds?state=verpublish&status=init&vmfile=no&publishid=109556&moduleCall=webInfo&publishConfFile=webInfo&publishSubDir=veranstaltung)

$\;\;\;\;\;\;\;\;\;\;\;$ **Stable Homotopy Theory**

$\;\;\;\;\;\;\;\;\;\;\;$ Dr. [[Urs Schreiber]]

[[Introduction to Stable homotopy theory|Lecture]] and [[Introduction to Stable homotopy theory -- S|Seminar]]

=--

$\,$


**Abstract** _We give an introduction to the [[stable homotopy category]] and to its key computational tool, the [[Adams spectral sequence]]. In the accompanying [[Introduction to Stable homotopy theory -- S|seminar]] we consider applications to [[cobordism theory]] and [[complex oriented cohomology]] such as to converge in the end to a glimpse of the modern picture of [[chromatic homotopy theory]]._



$\,$

***

Lecture notes.

Main page: _[[Introduction to Stable homotopy theory]]_.

Previous section: _[[Introduction to Stable homotopy theory -- 1|Part 1 -- Stable homotopy theory]]_

This section: **Part 2 -- Adams spectral sequences**

Next section: _[[Introduction to Stable homotopy theory -- S|Seminar -- Complex oriented cohomology]]_

***

$\,$

#Contents#
* table of contents
{:toc}


## **Part 2) Adams spectral sequences**

The main result of [[Introduction to Stable homotopy theory -- 1-1|Part 1.1]] was the construction of the [[stable homotopy category]] $Ho(Spectra)$ ([thm.](Introduction+to+Stable+homotopy+theory+--+1-1#StableModelStructureOnSequentialSpectraIsModelCategory), [def.](Introduction+to+Stable+homotopy+theory+--+1-1#TheStableHomotopyCategory)) as a [[triangulated category]] ([prop.](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyCategoryIsTriangulated)) with graded abelian hom groups $[X,Y]_\bullet$ ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#GradedAbelianGroupStructureOnHomsInTheHomotopyCategory)).

These are the basic invariants of [[stable homotopy theory]], the _[[stable homotopy groups]]_. They are as rich and interesting as they are, in general, hard to compute. The archetypical example for this phenonemon are the [[stable homotopy groups of spheres]] $\pi_\bullet(\mathbb{S})$. (We compute the first dozen of these, 2-locally, [below](#StableStems).)

In order to get more control over $Ho(Spectra)$, the main result of [[Introduction to Stable homotopy theory -- 1-2|Part 1.2]] was the construction of [[tensor triangulated category]] structure on $Ho(Spectra)$ ([prop.](Introduction+to+Stable+homotopy+theory+--+1-2#TensorTriangulatedStructureOnStableHomotopyCategory)), induced form a [[symmetric monoidal smash product of spectra]] $\wedge$ ([thm.](Introduction+to+Stable+homotopy+theory+--+1-2#StableModelStructureWithSymmetricMonoidalSmashProductSatisfiesPushoutProductAxiom))

$$
  (Ho(Spectra), \wedge, \mathbb{S})
  \,.
$$

As discussed in _[[Introduction to Stable homotopy theory -- I|Part I]]_ (and briefly reviewed [below](#SpectralSequenceOfAFilteredSpectrum)), the tool of choice to break up the computation of [[stable homotopy groups]] in [[stable homotopy theory]] into tractable computations in [[homological algebra]] are _[[spectral sequences]]_. These break up computations of stable homotopy groups along chosen [[filtered objects|filtrations]] on spectra. Using the [[tensor triangulated category|tensor triangulated structure]], it turns out that every [[homotopy commutative ring spectrum]] $E$ ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyCommutativeRingSpectrum)) induces a well-adapted filtration on spectra that allows to compute the "[[formal neighbourhood]] around $E$" in any spectrum (called the _$E$-[[nilpotent completion]]_) via a spectral sequence. This is the _$E$-[[Adams spectral sequence]]_ which we discuss here.

Where the [[Atiyah-Hirzebruch spectral sequence]] (see [[Introduction to Stable homotopy theory -- S|part S]], [this prop.](Introduction+to+Stable+homotopy+theory+--+S#AHSSExistence)) approximates $[X,Y]_\bullet$ via the [[ordinary cohomology]] $H^\bullet(X,\pi_\bullet(Y))$, the idea of the [[Adams spectral sequence]] is to make use of an auxiliary [[homotopy commutative ring spectrum]] $E$ and approximate maps of spectra $X \to Y$ via their image $E_\bullet(X) \to E_\bullet(Y)$ in $E$-[[generalized homology]] ([rmk](Introduction+to+Stable+homotopy+theory+--+1-2#EMHomology)). 

But in order for maps of homology groups to have a chance to retain enough information, they should be forced to be equivariant with respect to extra structure inherited by forming $E$-homology. 

For instance if $E = $ $H \mathbb{F}_2$ then the [[dual Steenrod algebra]] $\mathcal{A}$ (co-)acts on $E_\bullet(X) = H_\bullet(X,\mathbb{F}_2)$ and a necessary condition for a morphism of homology groups to come from a morphism of spectra is that it is a [[homomorphism]] with respect to this co-action.  The  [[classical Adams spectral sequence]] (discussed [below](#ClassicalAdamsSpectralSequence)), accordingly, approximates $[X,Y]_\bullet$ by $Hom_{\mathcal{A}}(H_\bullet(X,\mathbb{F}_2), H_\bullet(Y,\mathbb{F}_2))$.

More generally, since spectra are equivalently [[module spectra]] over the [[sphere spectrum]] $\mathbb{S}$, the operation of forming $E$-homology spectra $X \mapsto E \wedge S$ is equivalently the [[extension of scalars]] along the ring unit $\mathbb{S}\longrightarrow E$. This means that the extra structure inherited by $E$-homology groups contains the information given by the further extensions along the [[cosimplicial object|cosimplicial]] diagram

$$
  \mathbb{S} \longrightarrow E \stackrel{\longrightarrow}{\longrightarrow} E \wedge E \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}
  E \wedge E \wedge E
  \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}}
  \cdots
 \,.
$$

In good cases this gives $E_\bullet(X)$ the structure of a [[module]] over the [[Hopf algebroid]] $\pi_\bullet(E \wedge E) = E_\bullet(E) \stackrel{\longleftarrow}{\longleftarrow} E_\bullet$ of "dual $E$-Steenrod operations". Accordingly the general $E$-[[Adams spectral sequence]] approximates $[X,Y]_\bullet$ by $Hom_{E_\bullet(E)}(E_\bullet(X),E_\bullet(Y))$.

For $E = $ [[MU]], [[BP]], this is the _[[Adams-Novikov spectral sequence]], considered [below](#AdamsNovikovSpectralSequence).

We discuss first the

* [General theory of E-Adams spectral sequences](#TheoryforAdamsSpectralSequences)

and then consider the classical 

* [Examples and applications](#ExamplesOfAdamsSpectralSequences)

$\,$


### **2.1)** Theory
 {#TheoryforAdamsSpectralSequences}

Here we set up the general theory of $E$-[[Adams spectral sequences]]. (We consider examples and applications further [below](#ExamplesOfAdamsSpectralSequences).)

**Literature** ([Adams 74, part III.15](#Adams74), [Bousfield 79, sections 5 and 6](#Bousfield79), [Ravenel 86, appendix A](#Ravenel86))




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

That $\tilde j$ is indepenent of the choice of preimage: For any $x \in \tilde {\mathcal{D}} = im(i)$, let $y, y' \in \mathcal{D}$ be two preimages under $i$, hence $i(y) = i(y') = x$. This means that $i(y'-y) = 0$, hence that $y'-y \in ker(i)$, hence that $y'-y \in im(k)$, hence there exists $z \in \mathcal{E}$ such that $y' = y + k(z)$, hence $j(y') = j(y) +  j(k(z)) = j(y) + d(z)$, but $d(z) = 0$ in $\tilde{\mathcal{E}}$.

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

+-- {: .num_remark}
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

+-- {: .num_remark}
###### Remark

Terminology differs across authors. The tower/filtration in def. \ref{AdamsEAdamsSpectralSequence} in the rewriting by lemma \ref{Wp} is due to ([Adams 74, theorem 15.1](#Adams74)), where it is not give any name. In ([(Ravenel 84, p. 356](Adams+spectral+sequence#Ravenel84)) it is called the (canonical) **Adams tower** while in ([Ravenel 86, def. 2.21](Adams+spectral+sequence#Ravenel86)) it is called the canonical **Adams resolution**. Several authors follow the latter usage, for instance ([Rognes 12, def. 4.1](#Rognes12)). But ([Hopkins 99](Adams+spectral+sequence#Hopkins99)) uses "Adams resolution" for the "$E$-injective resolutions" that we discuss [below](#ViaInjectiveResolutions) and uses "Adams tower" for yet another concept, def. \ref{EAdamsTower} below. See also remark \ref{TerminologyAssociatedInverseSequence}.

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

Call a [[homotopy commutative ring spectrum]] $(E,\mu,e)$ ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyCommutativeRingSpectrum)) **flat** if the canonical right $\pi_\bullet(E)$-[[module]] structure on $E_\bullet(E)$ ([prop.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyGroupsOfHomotopyCommutativeRingSpectrum)), equivalently the canonical left module struture (prop. \ref{EETwoLeftModuleStructures}) is a [[flat module]].


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

First consider the case that $X \simeq \Sigma^{n} \mathbb{S}$ is a suspension of the [[sphere spectrum]]. Then 

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

Here the  bottom row is a [[long exact sequence]] since $E \wedge E \wedge (-)$ preserves homotopy cofiber sequences (by [this lemma](Introduction+to+Stable+homotopy+theory+--+1-2#SmashTensoringWithSpectrumDerivedPreserveshomotopycofibers), part of the [[tensor triangulated category|tensor triangulated]] structure on $Ho(Spectra)$ [prop.](Introduction+to+Stable+homotopy+theory+--+1-2#TensorTriangulatedStructureOnStableHomotopyCategory)), and since $[\mathbb{S},-]_\bullet \simeq \pi_\bullet(-)$ sends homtopy cofiber sequences to [[long exact sequences]] ([prop.](Introduction+to+Stable+homotopy+theory+--+1-1#LongExactSequenceOfStableHomotopyGroups)). By the same reasoning, $E_\bullet(-)$ of the homotopy cofiber sequence is long exact; and by the assumption that $E_\bullet(E)$ is [[flat module|flat]], the functor $E_\bullet(E)\otimes_{\pi_\bullet(E)}(-)$ preserves this exactness, so that also the top row is a [[long exact sequence]].

Now by [[induction]] over the cells of $X$, the outer four vertical morphisms are [[isomorphisms]]. Hence the [[5-lemma]] implies that also the middle morphism is an isomorphism.

This shows the claim inductively for all finite CW-spectra. For the general statement, now use that

1. every CW-spectrum is the [[filtered colimit]] over its finite CW-subspectra;

1. the [[symmetric monoidal smash product of spectra]] $\wedge$ ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#SsymModuleSymmetricSpectra)) preserves colimits in its arguments separately (since it has a [[right adjoint]] ([prop.](Introduction+to+Stable+homotopy+theory+--+1-2#MonoidalCategoryOfModules)));

1. $[\mathbb{S},-]_\bullet \simeq \pi_\bullet(-)$ commutes over filtered colimits of CW-spectrum inclusions (by [this lemma](Introduction+to+Stable+homotopy+theory+--+P#CompactSubsetsAreSmallInCellComplexes), since spheres are [[compact topological space|compact]]);

1. $E_\bullet(E) \otimes_{\pi_\bullet(E)}(-)$ distributes over colimits (it being a [[left adjoint]]).



=--

Using prop. \ref{EnHomology}, we find below (prop. \ref{ComoduleHomsInE1PageOfEAdamsSpectralSequence}) that the first page of the $E$-Adams spectral sequence may be equivalently rewritten as hom-groups of [[comodules]] over $E_\bullet(E)$ regarded as a [[graded commutative Hopf algebroid]]. We now first discuss what this means. 


##### The $E$-Steenrod algebra
 {#DualESteenrodAlgebra}


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

1. [[homomorphisms]] of graded commutative rings

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

   induced from the homomorphisms of commutative ring spectra

   $$
     E \simeq E \wedge \mathbb{S} 
       \overset{id \wedge e}{\longrightarrow}
     E \wedge E
   $$

   and

   $$
     E \simeq \mathbb{S} \wedge E
       \overset{id \wedge e}{\longrightarrow}
     E \wedge E
     \,,
   $$

   respectively ([exmpl.](Introduction+to+Stable+homotopy+theory+--+1-2#TensorProductOfTwoCommutativeMonoids));

1. a homomorphism of graded commutative rings

   $$
     \epsilon 
       \;\colon\;
     E_\bullet(E)
       \longrightarrow
     \pi_\bullet(E)
   $$

   induced from 

   $$
     \mu \;\colon\;  E \wedge E \longrightarrow E
   $$

   regarded as a homomorphism of homotopy commutative ring spectra ([exmpl.](Introduction+to+Stable+homotopy+theory+--+1-2#TensorProductOfTwoCommutativeMonoids));

1. a homomorphisms graded rings

   $$
     c 
       \;\colon\;
     E_\bullet(E)
       \longrightarrow
     E_\bullet(E)
   $$

   induced from the [[braiding]]

   $$
     \tau_{E,E} 
       \;\colon\; 
     E \wedge E 
       \longrightarrow 
     E \wedge E
   $$

   regarded as a homomorphism of homotopy commutative ring spectra ([exmpl.](Introduction+to+Stable+homotopy+theory+--+1-2#TensorProductOfTwoCommutativeMonoids));

1. a homomorphism of graded rings

   $$ 
     \Psi
       \;\colon\;
     E_\bullet(E)
       \longrightarrow
     E_\bullet(E) \otimes_{\pi_\bullet(E)} E_\bullet(E)
   $$

   induced from

   $$
     E \wedge E 
       \overset{id \wedge e \wedge id}{\longrightarrow}
     E \wedge E \wedge E
   $$

   under prop. \ref{EnHomology}.

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


+-- {: .num_example}
###### Example

Examples of [[commutative ring spectra]] $E$ for which the dual $E$-[[Steenrod algebra]] $E_\bullet(E)$ over $\pi_\bullet(E)$ of def. \ref{HopfAlgebroidStructureOnDualEOperations} where the left and right action of $\pi_\bullet(E)$ are not just isomorphic (via prop. \ref{EETwoLeftModuleStructures}) but actually equal according to remark \ref{HopfAlgebrasAsHopfAlgebroids}, includes the case $E = $ [[HA|H]]$\mathbb{F}_p$.

=--



The dual $E$-[[Steenrod algebras]] of def. \ref{HopfAlgebroidStructureOnDualEOperations} evidently carry a lot of structure. In concept organizing this is that of_[[commutative Hopf algebroids]]_.


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

   1. the morphisms $\alpha$ and $\beta$ induced via the [[coequalizer]] property of the [[tensor product]] from $(-) \cdot c(-)$ and $c(-)\cdot (-)$, respectively

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

It is now striaghtforward, if somewhat tedious, to check that:

+-- {: .num_prop}
###### Proposition

Let $(E, \mu, e)$ be a [[homotopy commutative ring spectrum]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyCommutativeRingSpectrum)) which is flat according to def. \ref{FlatE}, then the dual $E$-[[Steenrod algebra]] $ (E_\bullet(E), \pi_\bullet(E))$ with the
structure maps $(\eta_L, \eta_R, \epsilon, c, \Psi)$ from prop. \ref{HopfAlgebroidStructureOnDualEOperations} is a graded commutative Hopf algebroid accoring to def. \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents}.

=--

([Adams 69, lecture 3, pages 67-71](#Adams69))


+-- {: .num_remark}
###### Remark

In ([Adams 69, lecture 3, page 60](#Adams69)) the terminology used is "Hopf algebra in a fully satisfactory sense" with emphasis that the left and right module structure may differ. Accoring to ([Ravenel 86, first page of appendix A1](#Ravenel86)) the terminology "Hopf algebroid" for this situation is due to [[Haynes Miller]].

=--


##### Comodules over the $E$-Steenrod algebra


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





##### Universal coefficient theorem


The key use of the Hopf coalgebroid structure of prop. \ref{HopfAlgebroidStructureOnDualEOperations} for the present purpose is that it is extra structure inherited by morphisms in $E$-homology from morphisms of spectra.

+-- {: .num_example #SmashingMapsWithEFactorsThroughSteenrodComoduleHomomorphisms}
###### Example

For $X,N$ any two [[spectra]], the morphism (of $\mathbb{Z}$-[[graded abelian groups]]) given by [[smash product of spectra|smash product]] with $E$

$$
  \pi_\bullet(E \wedge -)
    \;\colon\;
  [X,N]_\bullet
    \longrightarrow
  Hom^\bullet_{Ab}(E_\bullet(X), E_\bullet(N))
$$

factors through $E_\bullet(E)$-[[comodule]] [[homomorphisms]] over the dual $E$-[[Steenrod algebra]]:

$$
  \pi_\bullet(E \wedge -)
    \;\colon\;
  [X,N]_\bullet
    \longrightarrow
  Hom^\bullet_{E_\bullet(E)}(E_\bullet(X), E_\bullet(N))
  \,.
$$

=--

In order to put all this together, we need to invoke a [[universal coefficient theorem]] in the following form.

+-- {: .num_prop #AdamsUCT}
###### Proposition

If at least one of the following conditions is met

* $X = \mathbb{S}$ is the [[sphere spectrum]];

* $E$ is among the examples [[sphere spectrum|S]], [[HR]] for $R = \mathbb{F}_p$, [[MO]], [[MU]], [[MSp]], [[KO]], [[KU]], 

then for all $E$-[[module spectra]] $N$ with [[action]] $\rho \colon E\wedge N \to N$ the morphism of $\mathbb{Z}$-[[graded abelian groups]]

$$
  [X,N]_\bullet 
    \stackrel{\phi \mapsto \rho \circ (id\wedge \phi)}{\longrightarrow}
  Hom_{\pi_\bullet(E)}^\bullet(E_\bullet(X), \pi_\bullet(N))_\bullet
$$

is an [[isomorphism]].


=--

For $Y = \mathbb{S}$ this is trivial. For general $Y$ and $E$ among the above examples this is the [[universal coefficient theorem]] of ([Adams 74, chapter III, prop. 13.5](#Adams74)), see also ([Schwede 12, chapter II, prop. 6.20](#Schwede12)), and see at _[Kronecker pairing -- Universal coefficient theorem](Kronecker+pairing#UniversalCoefficientTheorem)_.

With this we finally get the following statement, which serves to identify maps of certain spectra with their induced maps on $E$-homology:

+-- {: .num_prop #ComoduleHomForENCohomology}
###### Proposition

If the assumption of prop. \ref{AdamsUCT} hold, then for $X,N$ any two [[spectra]], the morphism of $\mathbb{Z}$-[[graded abelian groups]] from example \ref{SmashingMapsWithEFactorsThroughSteenrodComoduleHomomorphisms} of the form

$$
 \pi_\bullet(E\wedge (-))
   \;\colon\;
 [X, E\wedge N]_\bullet 
   \stackrel{}{\longrightarrow}
  Hom_{E_\bullet(E)}^\bullet(E_\bullet(X), E_\bullet(N)))
$$

is an [[isomorphism]].

=-- 

([Adams 74, part III, page 323](#Adams74))


+-- {: .proof}
###### Proof

By the general formula for expressing [[adjuncts]], the morphism fits into the following [[commuting diagram]]

$$
  \array{
    [X, E \wedge N]_\bullet
      &\stackrel{\pi_\bullet(E\wedge(-))}{\longrightarrow}&
    Hom_{E_\bullet(E)}(
      E_\bullet(X), 
      E_\bullet(E \wedge N)
    )
    \\
    {}^{\mathllap{{\phi \mapsto} \atop {\mu \circ (id \wedge \phi)}}}
      \downarrow^{\mathrlap{\simeq}}
    && \downarrow^{\mathrlap{\simeq}}
    \\
    Hom_{\pi_\bullet(E)}(E_\bullet(X), E_\bullet(N))
      &\stackrel{\simeq}{\longleftarrow}& 
    Hom_{E_\bullet(E)}(
      E_\bullet(X), 
      E_\bullet(E) \otimes_{\pi_\bullet(E)} E_\bullet(N)
    )
  }
  \,,
$$

where 

1. the right vertical map comes from the isomorphism of prop. \ref{EnHomology};

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

1. $E$ is flat (def. \ref{FlatE}) and satisfies the conditions of prop. \ref{AdamsUCT}, 

2. $E_\bullet(Y)$ a [[projective module]] over $\pi_\bullet(E)$, 

then the entries of the second page of the $E$-Adams spectral sequence, def. \ref{AdamsEAdamsSpectralSequence}, for $[X,Y]_\bullet$ are the [[Ext]]-groups of [[commutative Hopf algebroid]]-[[comodules]] for the [[commutative Hopf algebroid]] structure on $E$-operations $E_\bullet(E)$ from prop.  \ref{HopfAlgebroidStructureOnDualEOperations}:


$$
  E_2^{s,t}(X,Y)
  \simeq
  Ext^{s,t}_{E_\bullet(E)}(E_\bullet(X), E_\bullet(Y))
  \,.
$$

In the special case that $X = \mathbb{S}$, then (by prop. \ref{ComoduleHomInTermsOfCotensorProduct}) these are equivalently [[Cotor]]-groups

$$
  E^{s,t}_2(X,Y)
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

By lemma \ref{ResolutionEWp} we already know that $E_\bullet(A_\bullet)$ is a resolution of $E_\bullet(Y)$. By prop. \ref{EnHomology} it is a resolution by cofree comodules (def. \ref{CoFreeComodules}). That these are $F$-acyclic we show as prop. \ref{CoFreeHopfComodulesAreHomNAcyclicForProjectiveN} below.

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

+-- {: .num_defn }
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





















### **2.2)** Examples
 {#ExamplesOfAdamsSpectralSequences}


We here consider examples applying the general theory of $E$-[[Adams spectral sequences]] [above](#TheoryforAdamsSpectralSequences) in special cases to the concrete computation of certain stable homotopy groups. 

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




#### Classical Adams spectral sequence ($E = H \mathbb{F}_2$, $X = \mathbb{S}$)
 {#ClassicalAdamsSpectralSequence}
 

This is the _[[classical Adams spectral sequence]]_ for computation of 2-primary parts of the [[stable homotopy groups of spheres]]...

([Kochman 96, section 5](#Kochman96))

##### The dual Steenrod algebra

+-- {: .num_defn #SteenrodAlgebraForHFp}
###### Definition

Let $p$ be a [[prime number]]. Write $\mathbb{F}_p$ for the corresponding [[prime field]].

The **mod $p$-[[Steenrod algebra]]** $\mathcal{A}_{\mathbb{F}_p}$ is the graded co-commutative [[Hopf algebra]] over $\mathbb{F}_p$ which is

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
  \underoverset{k = 0}{n}{\sum} Sk^k \otimes Sq^{n-k}
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

There is an isomorphism

$$
  \mathcal{A}^\ast_{\mathbb{F}_p}
  \simeq
  H_\bullet( H \mathbb{F}_p, \mathbb{F}_p )
  = 
  \pi_\bullet( H \mathbb{F}_p \wedge H \mathbb{F}_p )
  \,.
$$

We now give the generators-and-relations description of the dual Steenrod algebra $\mathcal{A}^\ast_{\mathbb{F}_p}$ from def. \ref{DualSteenrodAlgebraForHPf}, in terms of linear duals of the generators for $\mathcal{A}_{\mathbb{F}_p}$ itself, according to def. \ref{SteenrodAlgebraForHFp}.

In the following, we use for $p = 2$ the notation 

$$
  P^n \coloneqq Sq^{2n}
$$

$$
  \beta \coloneqq Sq^1
  \,.
$$

This serves to unify the expressions  for $p = 2$ and for $p \gt 2$ in the following. Notice that for all $p$

* $P^n$ has even degree $deg(P^n) = 2n(p-1)$;

* $\beta$ has odd degree $deg(\beta) = 1$.


+-- {: .num_theorem #MilnorTheoremOnDualSteenrodAlgebra}
###### Theorem
**(Milnor's theorem)**

The dual mod $p$-Steenrod algebra $\mathcal{A}^\ast_{\mathbb{F}_p}$ (def. \ref{DualSteenrodAlgebraForHPf}) is, as an [[associative algebra]], the free [[graded commutative algebra]]

$$
  \mathcal{A}^\ast_{\mathbb{F}_p}
    \simeq
  Sym_{\mathbb{F}_p}(\xi_1, \xi_2, \cdots, \;\tau_0, \tau_1, \cdots)
$$

on generators:

* $\xi_n$ being the linear dual to $P^{p^{n-1}} P^{p^{n-2}} \cdots P^p P^1$;

* $\tau_n$ being linear dual to $P^{p^{n-1}} P^{p^{n-2}} \cdots P^p P^1\beta$.

Moreover, the coproduct on $\mathcal{A}^\ast_{\mathbb{F}_p}$ is given by

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

=--


This is due to ([Milnor 58](Steenrod+algebra#Milnor58)). See for instance ([Kochmann 96, theorem 2.5.1](#Kochmann96))

##### The May spectral sequence

A _May spectral sequence_ ([May 64](May+spectral+sequence#May64), [May 74](May+spectral+sequence#May74), [Ravenel 86, 3.2](#Ravenel86)) is a certain type of [[spectral sequence]] that computes the second page of the [[classical Adams spectral sequence]]. More generally, it computes [[Ext]]-groups (or [[Cotor]]-groups, via [this lemma](cotensor+product#ComoduleHomInTermsOfCotensorProduct)) of [[comodules]] over [[commutative Hopf algebras]] (the [[dual Steenrod algebra]] in the classical case) starting from the corresponding $Ext$-groups over just an [[associated graded]] Hopf algebra.

The May spectral sequence is the [[spectral sequence of a filtered complex]] induced by suitably filtering the canonical (but intractable) [[bar complex]] model for [[Ext]]/[[Cotor]] (see [Ravenel 86, chapter 3, section 2](#Ravenel86), [Kochman 96, section 5.3](#Kochman96)).

Throughout, let $A$ be a [[commutative ring]] and let $\Gamma$ be a graded [[commutative Hopf algebroid|commutative Hopf algebra]] over $A$. We write $(\Gamma,A)$ for this data.


+-- {: .num_lemma #CoModuleExtFromAToAForPrimitivelyGeneratedExteriorAlgebra}
###### Lemma


Let $(\Gamma,A)$ be a graded [[commutative Hopf algebra]] such that 

1. the underlying algebra is free graded commutative;

1. $\eta \colon A \to \Gamma$ is a [[flat morphism]];

1. $\Gamma$ is generated by [[primitive elements]] $\{x_i\}_{i\in I}$

then the [[Ext]] of $\Gamma$-comodules from $A$ and itself is the free graded commutative algebra on these generators


$$
  Ext_\Gamma(A,A) \simeq A[\{x_i\}_{i \in I}]
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

Since the counit $\eta$ is assumed to be flat, and since $A$ is trivially a [[projective module]] over itself, [this prop.](commutative+Hopf+algebroid#CoFreeHopfComodulesAreHomNAcyclicForProjectiveN) now implies that the above is an [[acyclic resolution]] with respect to the functor $Hom_{\Gamma}(A,-) \colon \Gamma CoMod \longrightarrow A Mod$. Therefore it computes the [[Ext]]-functor. Using that forming co-free comodules is [[right adjoint]] to forgetting $\Gamma$-comodule structure over $A$ ([prop.](commutative+Hopf+algebroid#CoFreeComodules)), this yields:

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
    A[\{y_i\}_{i \in I}]
  \end{aligned}
  \,.
$$

=--



+-- {: .num_lemma #SpectralSequenceConvergingToExtForFilteredHopfAlgebra}
###### Lemma


If $(\Gamma,A)$ is equipped with a [[filtering]] right/left $\Gamma$-comodules $N_1$ and $N_2$ are compatibly filtered, then there is a [[spectral sequence]]

$$
  \mathcal{E}_1
  =
  Ext_{gr_\bullet \Gamma}(gr_\bullet N_1, gr_\bullet N_2)
  \;\Rightarrow\;
  Ext_{\Gamma}(N_1, N_2)
$$

converging to the [[Ext]] over $\Gamma$ between $N_1$ and $N_2$, whose first page is the Ext over the [[associated graded]] Hopf algebra $gr_\bullet \Gamma$ between the associated graded modules $gr_\bullet N_1$ and $gr_\bullet N_2$.

=--

([Ravenel 86, lemma 3.1.9](#Ravenel86), [Kochman 96, prop. 3.7.5](#Kochman96))

+-- {: .proof}
###### Proof

The filtering induces a filtering on the standard bar complex which computes $Ext_\Gamma$. The spectral sequence in question is the corresponding [[spectral sequence of a filtered complex]]. Its first page is the homology of the associated graded complex (by this [prop.](spectral+sequence+of+a+filtered+complex#FirstPages)).

=--

Let now $A \coloneqq \mathbb{F}_2$,  $\Gamma \coloneqq \mathcal{A}^\bullet_{\mathbb{F}_2}$ be the mod 2 [[dual Steenrod algebra]]. By [Milnor's theorem](Steenrod+algebra#MilnorTheoremOnDualSteenrodAlgebra), as an $\mathbb{F}_2$-algebra this is

$$
  \mathcal{A}^\bullet_{\mathbb{F}_2} 
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

By binary expansion of powers, there is a unique way to express every monomial in $\mathbb{F}_2[\xi_1, \xi_2, \cdots]$ as a product of elements

$$
  h_{i,n} \coloneqq \xi_i^{2^n}
$$

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

+-- {: .num_prop #CoproductOnDualSteenrodInTermsOfAdaptedGenerators}
###### Proposition

In terms of the generators $\{h_{i,n}\}$, the coproduct on $\mathcal{A}^\ast_{\mathbb{F}_2}$ takes the following simple form

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
    & = (\Psi(\xi_i))^{2n}
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

Define a [[graded algebra|grading]] on $\mathcal{A}^\bullet_{\mathbb{F}_2}$ by setting (this is due to ([Ravenel 86, p.69](#Ravenel86)))

$$
  {\vert h_{i,n} \vert}
    \coloneqq
  2i-1
$$

and extending this additively to these unique representative.


For instance

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


Consider the corresponding [[filtered object|filtering]]

$$
  \cdots 
   \subset
  F_p \mathcal{A}^\ast_{\mathbb{F}_2}
   \subset
  F_{p+1} \mathcal{A}^\ast_{\mathbb{F}_2}
    \subset 
  \cdots 
    \subset
  \mathcal{A}^\ast_{\mathbb{F}_2}
$$

with filtering stage $p$ containing all elements of total degree $\leq p$.

Observe that

$$
  \begin{aligned}
    \Psi(\xi_i)
    &
   =
   \underset{deg = 2i-1}{\underbrace{\xi_{i} \otimes 1}}
   +
    \underoverset{0 \lt k \lt i}{}{\sum} 
     \underset{deg = 2i-2}{\underbrace{\xi_{i-k}^{p^k} \otimes \xi_k}}
   +
    \underset{deg = 2i-1}{\underbrace{1 \otimes \xi_i}}
  \end{aligned}
  \,.
$$

This means that after projection to the [[associated graded]] Hopf algebra

$$
  F_\bullet \mathcal{A}^\ast_{\mathbb{F}_2}
   \longrightarrow
  gr_\bullet \mathcal{A}^\ast_{\mathbb{F}_2}
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
   gr_\bullet \mathcal{A}^\ast_{\mathbb{F}_2}
   \otimes
   gr_\bullet \mathcal{A}^\ast_{\mathbb{F}_2}
  \end{aligned}
  \,.
$$


Hence lemma \ref{CoModuleExtFromAToAForPrimitivelyGeneratedExteriorAlgebra} applies and says that the $Ext$ from $\mathbb{F}_2$ to itself over the [[associated graded]] Hopf algebra is the polynomial algebra in these generators:

$$
  Ext_{gr \mathcal{A}^\ast_{\mathbb{F}_2}}(\mathbb{F}_2,\mathbb{F}_2)
  =
  \mathbb{F}_2[\{h_{i,n}\}_{{i \geq 1,} \atop {n \geq 0}}]  
  \,.
$$

Moreover, lemma \ref{SpectralSequenceConvergingToExtForFilteredHopfAlgebra} says that this is the first page of a spectral sequence that converges to the $Ext$ over the original Hopf algebra:

$$
  \mathcal{E}_1 
  = 
  \mathbb{F}_2[\{h_{i,n}\}_{{i \geq 1} \atop {n \geq 0}}]
  \;\Rightarrow\;
  Ext_{\mathcal{A}^\ast_{\mathbb{F}_2}}(\mathbb{F}_2,\mathbb{F}_2)
  \,.
$$

This is the _May spectral sequence_ for the computation of $Ext_{\mathcal{A}^\ast_{\mathbb{F}_2}}(\mathbb{F}_2,\mathbb{F}_2)$. Notice that since everything is $\mathbb{F}_2$-linear, its [extension problem](spectral+sequence#ExtensionProblem) is trivial.

Moreover, again by lemma \ref{SpectralSequenceConvergingToExtForFilteredHopfAlgebra}, the differentials on any $r$-page are the restriction of the differentials of the bar complex to the $r$-almost cycles ([prop.](Introduction+to+Stable+homotopy+theory+--+I#DifferentialsOnAlmostChains)). The differential of the bar complex is the alternating sum of the coproduct on $\mathcal{A}^\ast_{\mathbb{F}_2}$, hence by prop. \ref{CoproductOnDualSteenrodInTermsOfAdaptedGenerators} this is:

$$
  d_1 (h_{i,n})
  =
  \underoverset{k = 0}{i}{\sum} h_{i-k,n+k}\otimes h_{k,n}  \,.
$$


##### The second page

Now we use the above formula to explicitly compute the cohomology of the second page of the [[classical Adams spectral sequence]].

In doing so it is now crucial that the differential in the standard bar complex resolution for $Ext$ lands in $\overline{\Gamma} \coloneqq coker(\eta)$ where the generator $h_{0,n} = \xi_0 = 1$ disappears:

$$
  d \;\colon\;
  A \otimes_A \Gamma \otimes_A \Gamma
  \longrightarrow
  A \otimes_A \Gamma \otimes_A \Gamma \otimes_A A
$$

$$
  \begin{aligned}
    d(1,h,1) & = 
    (d 1 , h , 1) - (1 , d h , 1) + (1 , h , d 1)
    \\
    & = (1,1,h,1) - (1, \Psi(h) , 1 ) + (1 , h, 1, 1)
  \end{aligned}  
  \,.
$$

Hence we find for instance, using the formula from prop. \ref{CoproductOnDualSteenrodInTermsOfAdaptedGenerators} that

$$
  \begin{aligned}
    d_1(h_n)
    & \coloneqq
    d_1(h_{1,n})
    \\
    & =   
    \Psi(h_{1,n})
    \\
    & =
    h_{1,n+1} \underset{= 0}{\underbrace{ h_{0,n} }}
    + 
    \underset{= 0}{\underbrace{ h_{0,n+1} }} h_{1,n}
    \\
    & = 
    0
  \end{aligned}
$$

and hence all the elements $h_n$ are cocycles.

Similarly for instance

$$
  d_1(h_{2,0}) 
    = 
  h_{2,0} \underset{= 0}{\underbrace{h_{0,0}}}
  + 
  h_{1,1} h_{1,0}
  +
  \underset{= 0}{\underbrace{h_{0,2}}} h_{2,0}
$$

and so this is not a cocycle, but gives the relation that the product

$$
  h_{1,1} h_{1,0} = 0
$$

in cohomology. Proceeding this way by explicit inspection, one obtains:

+-- {: .num_lemma }
###### Lemma

In the range $t - s \leq 13$, the second page of the May spectral sequence for $Ext_{\mathbb{A}^\ast_{\mathbb{F}_2}}(\mathbb{F}_2,\mathbb{F}_2)$ has as generators all the 

* $h_n$

* $b_{i,n} \coloneqq (h_{i,n})^2$

as well as the element

*  $x_7 \coloneqq h_{2,0} h_{2,1} + h_{1,1} h_{3,0}$

subject to the relations

* $h_n h_{n+1} = 0$

* $h_2 b_{2,0} = h_0 x_7$

* $h_2 x_7 = h_0 b_{2,1}$.

The differentials in this range are

1. $d_r(h_{n}) = 0$

1. $d_2(b_{2,n}) = h_n^2 h_{n+2} + h_{n+1}^3$

1. $d_2(x_7) = h_0 h_2^2$

1. $d_2(b_{3,0}) = h_1 b_{2,1} + h_3 b_{2,0}$

1. $d_4(b_{2,0}^2) = h_0^4 h_3$.

=--

e.g. ([Ravenel 86, lemma 3.2.8 and lemma 3.2.10](#Ravenel86), [Kochman 96, lemma 5.3.2 and lemma 5.3.3](#Kochman96))

Hence this solves the May spectral sequence, hence gives the second page of the classical Adams spectral sequence. Inspection just of the degrees then shows that in this range there is no non-trivial differential in the Adams spectral sequece in this range. This way one arrives at:

+-- {: .num_theorem}
###### Theorem

In low $t-s$ the group $Ext_{\mathcal{A}^\ast_{\mathbb{F}_2}}(\mathbb{F}_2,\mathbb{F}_2)$ is spanned by the items in the following table

<img src="http://ncatlab.org/nlab/files/ClassicalAdamsSpectralSequence.jpg" width="600" >



=--

e.g. ([Ravenel 86, theorem 3.2.11](#Ravenel86), [Kochman 96, prop. 5.3.6](#Kochman96)), graphics taken from ([[Symmetric spectra|Schwede 12]]))


##### The first dozen stable stems
 {#StableStems}

Hence we have found



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

#### The case $E = H \mathbb{F}_p$ and $X = M U$ 

used to compute the [[stable homotopy groups]] of the complex [[Thom spectrum]] $M U$ from the [[homology of MU]]

(hence, by [[Thom's theorem]], equivalently the complex [[cobordism ring]] $\Omega_\bullet^U \simeq \pi_\bullet U)$, see at _[Seminar session: Milnor-Quillen theorem on MU](Introduction+to+Stable+homotopy+theory+--+S#ThomTheorem)_) 

This is the _[[Milnor-Quillen theorem on MU]]_, see at _[Seminar session: Milnor-Quillen theorem on MU](Introduction+to+Stable+homotopy+theory+--+S#QuillenTheoremOnMU)_

([Adams 74, part II, around section 8](Introduction+to+Stable+homotopy+theory+--+S#Adams74), [Lurie 10, around lecture 9](Introduction+to+Stable+homotopy+theory+--+S#Lurie10))

#### Adams-Novikov spectral sequence ($E = M U$, $X = \mathbb{S}$)
 {#AdamsNovikovSpectralSequence}

this is the classical _[[Adams-Novikov spectral sequence]]_ ,  converges faster than the classical choice $E = H \mathbb{F}_p$ to the [[stable homotopy groups of spheres]], (...)

([Kochman 96, section 5](#Kochman96))



$\,$

$\,$

***

## References
 {#References}


For the general theory we follow the original

* {#Adams69} [[John Frank Adams]], section 2 of _Lectures on generalised cohomology_, in  [[Peter Hilton]] (ed.) _Category Theory, Homology Theory and Their Applications III_, volume 99 of Lecture Notes in Mathematics (1969), Springer-Verlag Berlin-Heidelberg-New York. 

* {#Adams74} [[Frank Adams]], section III.15 of _[[Stable homotopy and generalized homology]]_, Chicago Lectures in mathematics, 1974

* {#Bousfield79} [[Aldridge Bousfield]], sections 5 and 6 of _The localization of spectra with respect to homology_, Topology 18 (1979), no. 4, 257--281. ([pdf](http://www.uio.no/studier/emner/matnat/math/MAT9580/v12/undervisningsmateriale/bousfield-topology-1979.pdf))


For the homological algebra of comodules over Hopf algebroids we follow appendix A of

* {#Ravenel86} [[Doug Ravenel]], _[[Complex cobordism and stable homotopy groups of spheres]]_, 1986/2003


For the special case of the [[classical Adams spectral sequence]] and of the [[Adams-Novikov spectral sequence]] we follow

* {#Kochman96} [[Stanley Kochman]], chapter 5 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996



