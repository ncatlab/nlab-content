

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


***

Lecture notes.

Main page: _[[Introduction to Stable homotopy theory]]_.

Previous section: _[[Introduction to Stable homotopy theory -- P|Prelude -- Classical homotopy theory]]_

This section: **Part 1 -- Stable homotopy theory**

Next section: _[[Introduction to Stable homotopy theory -- 2|Part 2 -- Adams spectral sequences]]_

***

$\,$


#Contents#
* table of contents
{:toc}

## **Part 1) Stable homotopy theory**
 {#StableHomotopyTheory}

 
The _[[Introduction to Stable homotopy theory -- P|Prelude on Classical homotopy theory]]_ ended with the following phenomenon:

+-- {: .num_defn #SuspensionAndLoopingOnPointedTopologicalSpaces}
###### Definition

The [[reduced suspension]]/[[loop space object|looping]] operation on [[pointed topological space|pointed]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#CategoryOfPointedObjects)) [[compactly generated topological spaces]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#kTop)) is the smash-tensor/hom-[[adjunction]] ([cor.](Introduction+to+Stable+homotopy+theory+--+P#SmashHomAdjunctionOnPointedCompactlyGeneratedTopologicalSpaces)) for the standard [[1-sphere]] smash product from the left:

$$
  (\Sigma \dashv \Omega)
  \;\colon\;
  Top_{cg}^{\ast/}
   \;
   \underoverset
     {\underset{Maps(S^1,-)_\ast}{\longrightarrow}}
     {\overset{S^1 \wedge (-)}{\longleftarrow}}
     {\bot}
   \;
  Top_{cg}^{\ast/}
  \,.
$$

=--

+-- {: .num_prop #SuspensionAndLoopAdjunctionInClassicalHomotopyTheory}
###### Proposition

With respect to the [[classical model structure on pointed topological spaces|classical model structure]] on pointed compactly generated topological spaces $(Top^{\ast/}_{cg})_{Quillen}$ ([thm.](Introduction+to+Stable+homotopy+theory+--+P#ClassicalModelStructureOnCompactlyGeneratedTopologicalSpaces), [prop.](Introduction+to+Stable+homotopy+theory+--+P#ModelStructureOnSliceCategory))

1. the adjunction in def. \ref{SuspensionAndLoopingOnPointedTopologicalSpaces} is a [[Quillen adjunction]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#QuillenAdjunction))

   $$
     (\Sigma \dashv \Omega)
     \;\colon\;
     (Top_{cg}^{\ast/})_{Quillen}
      \underoverset
       {\underset{Maps(S^1,-)_\ast}{\longrightarrow}}
       {\overset{S^1 \wedge (-)}{\longleftarrow}}
       {\bot}
     (Top_{cg}^{\ast/})_{Quillen}
     \,,
   $$

1. its induced [[adjoint pair]] of [[derived functors]] on the [[classical pointed homotopy category]] (by [this prop.](Introduction+to+Stable+homotopy+theory+--+P#QuillenAdjunctionInducesAdjunctionOnHomotopyCategories)) is the canonical suspension/looping adjunction (according to [this prop.](Introduction+to+Stable+homotopy+theory+--+P#LoopingAsFunctorOnHomotopyCategory))

   $$
     (\Sigma \dashv \Omega)
       \;\colon\;
     Ho(Top^{\ast/})
      \underoverset
        {\underset{\Omega}{\longrightarrow}}
        {\overset{\Sigma}{\longleftarrow}}
        {\bot}
     Ho(Top^{\ast/})
     \,.
   $$

=--

See ([this prop.](Introduction+to+Stable+homotopy+theory+--+P#SuspensionAndLoopAreAdjointOnHomotopyCategory)).


The _[[stable homotopy category]]_ $Ho(Spectra)$ is to be the result of stabilizing the adjunction in prop. \ref{SuspensionAndLoopAdjunctionInClassicalHomotopyTheory}, in the sense of forcing it to become an [[equivalence of categories]] in a compatible way, i.e. such as to fit into a diagram of categories of the form

$$
  \array{
     Ho(Top^{\ast/}) 
      &
      \underoverset{\underoverset{\Omega}{\bot}{\longrightarrow}}{\overset{\Sigma}{\longleftarrow}}{} 
      &
     Ho(Top^{\ast/})
     \\
     {}^{\mathllap{\Sigma^\infty}}\downarrow \dashv \uparrow^{\mathrlap{\Omega^\infty}}
     &&
     {}^{\mathllap{\Sigma^\infty}}\downarrow \dashv \uparrow^{\mathrlap{\Omega^\infty}}
     \\
     Ho(Spectra) 
     &
     \underoverset{\underset{\Omega}{\longrightarrow}}{\overset{\Sigma}{\longleftarrow}}{\simeq}
     &
     Ho(Spectra)
  }
  \,.
$$

Moreover, for [[stable homotopy theory]] proper we are to refine this situation from [[homotopy categories]] to [[model categories]] and ask it to be the diagram of [[derived functors]] (according to [this prop.](Introduction+to+Stable+homotopy+theory+--+P#QuillenAdjunctionInducesAdjunctionOnHomotopyCategories)) of a diagram of [[Quillen adjunctions]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#QuillenAdjunction))

$$
  \array{
     (Top_{cg}^{\ast/})_{Quillen}
      &
      \underoverset{\underoverset{\Omega}{\bot}{\longrightarrow}}{\overset{\Sigma}{\longleftarrow}}{} 
      &
     (Top^{\ast/}_{cg})_{Quillen}
     \\
     {}^{\mathllap{\Sigma^\infty}}\downarrow \dashv \uparrow^{\mathrlap{\Omega^\infty}}
     &&
     {}^{\mathllap{\Sigma^\infty}}\downarrow \dashv \uparrow^{\mathrlap{\Omega^\infty}}
     \\
     SeqSpec(Top_{cg})_{stable}
     &
     \underoverset{\underset{\Omega}{\longrightarrow}}{\overset{\Sigma}{\longleftarrow}}{\simeq_Q}
     &
     SeqSpec(Top_{cg})_{stable}
  }
  \,,
$$

This we establish in corollary \ref{StableHomotopyCategoryIsIndeedStabilizationOfClassicalHomotopyCategory} below.

The notation $\Sigma^\infty$ and $\Omega^\infty$ is meant to be suggestive of the intuition behind how this stabilization will work: The universal way of making a topological space $X$ become stable under suspension is to pass to its infinite suspension in a suitable sense. That suitable sense is going to be called the _[[suspension spectrum]]_ of $X$ (def. \ref{SuspensionSpectrum} below). Conversely, if an object does not change up to equivalence, by forming its loop spaces, it must give an [[infinite loop space]].

In contrast to the [[classical homotopy category]], the [[stable homotopy category]] is a [[triangulated category]] (a shadow of the fact that the [[(∞,1)-category of spectra]] is a [[stable (∞,1)-category]]). As such it may be thought of as a refinement of the [[derived category]] [[category of chain complexes|of chain complexes]] (of [[abelian groups]]): every [[chain complex]] gives rise to a [[spectrum]] and every [[chain map]] to a map between these spectra (the [[stable Dold-Kan correspondence]]), but there are many more spectra and maps between them than arise from chain complexes and chain maps.


There is a variety of different models for the [[stable homotopy theory]] of spectra, some of which fits into this hierarchy:

1. [[sequential spectra]] with their [[model structure on sequential spectra]]

1. [[symmetric spectra]] with their [[model structure on symmetric spectra]]

1. [[orthogonal spectra]] with their [[model structure on orthogonal spectra]]

1. [[excisive functors]] with their [[model structure for excisive functors]]

As one moves down this list, the objects modelling the spectra become richer. This means on the one hand that their abstract properties become better as one moves down the list, on the other hand it means that it is more immediate to construct and manipulate examples as one stays further up in the list. 

We start with plain sequential spectra in [1.1)](#SequentialSpectraSection) as a transparent means to construct the [[stable homotopy category]]. In order to discuss of [[ring spectra]] below in [1.3)](#HigherAlgebra), it is convenient to first pass to the richer model of [[highly structured spectra]], this we do in [1.2)](#SymmetricSpectra). 



### **1.1)** Sequential spectra
 {#SequentialSpectraSection}

The most lighweight model for [[spectra]] are _[[sequential spectra]]_. They support most of [[stable homotopy theory]] in a straightforward way, and have the advantage that examples tend to be immediate (for instance the proof of the [[Brown representability theorem]] spits out sequential spectra). 

The key disadvantage of sequential spectra is that they do not support a functorial [[smash product of spectra]] before passing to the [[stable homotopy category]], much less a [[symmetric smash product of spectra]]. This is the structure needed for a decent discussion of the [[higher algebra]] of [[ring spectra]]. To accomodate this, further [below](#SymmetricSpectra) we enhance sequential spectra to the more [[highly structured spectrum|highly structured]] models given by [[symmetric spectra]] and [[orthogonal spectra]]. But all these models are connected by a [[free-forgetful adjunction]] and for working with either it is useful to have the means to pass back and forth between them.

#### Sequential pre-spectra 

The following def. \ref{SequentialSpectra} is the traditional component-wise definition of [[sequential spectra]]. It was first stated in ([Lima 58](spectrum#Lima58)) and became widely appreciated with ([Boardman 65](spectrum#Boardman65)).  

> It is generally supposed that [[George Whitehead|G. W. Whitehead]] also had something to do with it, but the latter takes a modest attitude about that. ([Adams 74, p. 131](#Adams74))

Below in prop. \ref{SequentialSpectraAsDiagramSpectra} we discuss an equivalent definition of sequential spectra as "topological diagram spectra" ([Mandell-May-Schwede-Shipley 00](#MMSS00)), namely as [[topologically enriched functors]] ([defn.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctor)) on a [[topologically enriched category]] of [[n-spheres]], which is useful for establishing the [[stable model category]] structure ([below](#StableModelStructureOnSequentialSpectra)) and for establishing the [[symmetric monoidal smash product of spectra]] (in [1.2](#DiagramSpectra)).

Throughout, our ambient [[category]] of [[topological spaces]] is $Top_{cg}$, the category of [[compactly generated topological space]] ([defn.](Introduction+to+Stable+homotopy+theory+--+P#kTop)).

+-- {: .num_defn #SequentialSpectra}
###### Definition

A **[[sequential spectrum|sequential]] [[prespectrum]] in [[topological spaces]]**, or just **[[sequential spectrum]]** for short (or even just **[[spectrum]]), is

1. an $\mathbb{N}$-[[graded object|graded]] [[pointed topological space|pointed]] [[compactly generated topological space]]  

   $$
     X_\bullet = (X_n \in Top_{cg}^{\ast/})_{n \in \mathbb{N}}
   $$ 

   (the **component spaces**); 

1. pointed [[continuous functions]] 

   $$
     \sigma_n \colon S^1 \wedge X_n \to X_{n+1}
   $$ 

   for all $n \in \mathbb{N}$ (the **structure maps**) from the [[smash product]] ([defn.](Introduction+to+Stable+homotopy+theory+--+P#SmashProductOfPointedObjects))  of one component space with the standard [[1-sphere]] to the next component space.

 A [[homomorphism]] $f \colon X \to Y$ of sequential spectra is a sequence $f_\bullet \colon X_\bullet \to Y_\bullet$ of base point-preserving continuous functions between component spaces, such that these respect the structure maps in that all [[diagrams]] of the form

$$
  \array{
    S^1 \wedge X_n &\stackrel{S^1 \wedge f_n}{\longrightarrow}& S^1 \wedge Y_n
    \\
    \downarrow^{\mathrlap{\sigma_n^X}} && \downarrow^{\mathrlap{\sigma_n^Y}}
    \\
    X_{n+1} &\stackrel{f_{n+1}}{\longrightarrow}& Y_{n+1}
  }
$$

[[commuting diagram|commute]].

Write $SeqSpec(Top_{cg})$ for this [[category]] of topological sequential spectra.

=--

Due to the classical [[adjunction]]

$$
  Top_{cg}^{\ast/}
    \underoverset
     {\underset{Maps(S^1,-)_\ast}{\longrightarrow}}
     {\overset{S^1 \wedge (-)}{\longleftarrow}}
     {\bot}
  Top_{cg}^{\ast/}
$$

from [[Introduction to Stable homotopy theory -- P|classical homotopy theory]] ([this prop.](Introduction+to+Stable+homotopy+theory+--+P#PointedCompactlyGeneratedTopologicalSpacesIsSymmetricMonoidalClosed)), the definition of sequential spectra in def. \ref{SequentialSpectra} is equivalent to the following definition

+-- {: .num_defn #SequentialSpectrumViaAdjunctStructureMaps}
###### Definition

A **[[sequential spectrum|sequential]] [[prespectrum]] in [[topological spaces]]**, or just **[[sequential spectrum]]** for short (or even just **[[spectrum]]), is

1. an $\mathbb{N}$-[[graded object|graded]] [[pointed topological space|pointed]] [[compactly generated topological space]]  
  
   $$
     X_\bullet = (X_n \in Top_{cg}^{\ast/})_{n \in \mathbb{N}}
   $$ 

   (the **component spaces**); 

1. pointed [[continuous functions]] 

   $$
     \tilde \sigma_n \colon X_n \to Maps(S^1,X_{n+1})_\ast
   $$ 

   for all $n \in \mathbb{N}$ (the **adjunct structure maps**) from one component space to the pointed [[mapping space]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#CompactlyGeneratedMappingSpaces), [exmpl.](Introduction+to+Stable+homotopy+theory+--+P#PointedMappingSpace)) out of $S^1$ into the next component space.

 A [[homomorphism]] $f \colon X \to Y$ of sequential spectra is a sequence $\widetilde{f_\bullet} \colon X_\bullet \to Y_\bullet$ of base point-preserving continuous function, such that all [[diagrams]] of the form

$$
  \array{
    X_n &\overset{f_n}{\longrightarrow}& Y_n
    \\
    {}^{\mathllap{\tilde \sigma^X_n}}\downarrow && \downarrow^{\mathrlap{\tilde \sigma^Y_n}}
    \\
    Maps(S^1, X_{n+1})_\ast
      &\underset{Maps(S^1,f_{n+1})_\ast}{\longrightarrow}&
    Maps(S^1, Y_{n+1})_\ast
  }
$$

[[commuting diagram|commute]].

=--


+-- {: .num_example #SuspensionSpectrum}
###### Example

For $X\in Top^{\ast/_{cg}}$ a [[pointed topological space]], its **[[suspension spectrum]]** $\Sigma^\infty X$ is the [[sequential spectrum]] , def. \ref{SequentialSpectra}, with

* $(\Sigma^\infty X)_n \coloneqq S^n \wedge X$ ([[smash product]] of $X$ with the [[n-sphere]]);

* $\sigma_n \colon S^1 \wedge S^n \wedge X \overset{\simeq}{\longrightarrow} S^{n+1}X$ (the canonical [[homeomorphism]]).

This construction extends to a [[functor]]

$$
  \Sigma^\infty
    \;\colon\;
  Top^{\ast/}_{cg}
    \longrightarrow
  SeqSpec(Top_{cg})
  \,.
$$


=--

+-- {: .num_example #StandardSphereSpectrum}
###### Example

The [[suspension spectrum]] (example \ref{SuspensionSpectrum}) of the point is the **standard sequential [[sphere spectrum]]** 

$$
  \mathbb{S}_{seq} \coloneqq \Sigma^\infty S^0
  \,.
$$

Its $n$th component space is the standard [[n-sphere]]
 
$$ 
  (\mathbb{S}_{seq})_n = S^n
  \,.
$$

=--

+-- {: .num_defn #TensoringAndPoweringOfSequentialSpectra}
###### Definition

Let $X\in SeqSpec(Top_{cg})$ be a [[sequential spectrum]] (def. \ref{SequentialSpectra}) and $K \in Top^{\ast/}_{cg}$ a [[pointed topological space|pointed]] [[compactly generated topological space]]. Then

1. $X \wedge K$ (the **[[smash product|smash]] [[tensoring]]** of $X$ with $K$) is the sequential spectrum given by

   * $(X \wedge K)_n \coloneqq X_n \wedge K$ ([[smash product]] on component spaces ([defn.](Introduction+to+Stable+homotopy+theory+--+P#SmashProductOfPointedObjects)))

   * $\sigma_n^{X \wedge K} \coloneqq \sigma_n^{X} \wedge id_{K}$.

1. $Maps(K,X)_\ast$ (the **[[powering]]** of $K$ into $X$) is the sequential spectrum with

   * $(Maps(K,X)_\ast)_n \;\coloneqq\; Maps(K,X_n)_\ast$ (compactly generated [[pointed mapping space]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#CompactlyGeneratedMappingSpaces), [def.](Introduction+to+Stable+homotopy+theory+--+P#PointedMappingSpace)))

   * $\sigma_n^{Maps(K,X)_\ast} \;\colon\; S^1 \wedge Maps(K,X_n) \overset{(const,id)}{\longrightarrow} Maps(K,S^1 \wedge X_n)_\ast \overset{Maps(K,\sigma_n)_\ast}{\longrightarrow} Maps(K,X_{n+1})_\ast$,

   where $(const, id) \;\colon\; [s,\phi] \mapsto [const_s,\phi]$.


These operations canonically extend to [[functors]]

$$
  (-)\wedge (-)
    \;\colon\;
  SeqSpec(Top_{cg}) \times Top^{\ast/}_{cg}
    \longrightarrow
  SeqSpec(Top_{cg})
$$

and

$$
  Maps(-,-)_\ast
    \;\colon\;
  (Top^{\ast/}_{cg})^{op}
  \times
  SeqSpec(Top_{cg})
    \longrightarrow
  SeqSpec(Top_{cg})
  \,.
$$

=--

+-- {: .num_example}
###### Example

The tensoring (def. \ref{TensoringAndPoweringOfSequentialSpectra}) of the standard [[sphere spectrum]] $\mathbb{S}_{std}$ (def. \ref{StandardSphereSpectrum}) with a space $X \in Top_{cg}$ is isomorphic to the [[suspension spectrum]] of $X$ (def. \ref{SuspensionSpectrum}):

$$
  \mathbb{S}_{std} \wedge X
    \simeq
  \Sigma^\infty X
  \,.
$$

=--


+-- {: .num_prop #AdjunctionBetweenSmashTensoringAndPowering}
###### Proposition

For any $K \in Top^{\ast/}_{cg}$ the functors of smash tensoring and powering with $K$, from def. \ref{TensoringAndPoweringOfSequentialSpectra}, constitute a pair of [[adjoint functors]]

$$
  SeqSpec(Top_{cg})
    \underoverset
    {
      \underset{Maps(K,-)_\ast}{\longrightarrow}
    }
    {
      \overset{(-) \wedge K}{\longleftarrow}
    }
    {\bot}
  SeqSpec(Top_{cg})
  \,.
$$

=--

+-- {: .proof}
###### Proof

For $X, Y\in SeqSpec(Top_{cg})$ and $K \in Top_{cg}^{\ast/}$, let

$$
  X \wedge K \overset{f}{\longrightarrow} Y
$$

be a morphism, with component maps fitting into commuting squares of the form

$$
  \array{
    S^1 \wedge X_n \wedge K 
      &\overset{S^1 \wedge f_n}{\longrightarrow}&
    S^1 \wedge Y_n
    \\
    {}^{\mathllap{\sigma^X_n \wedge K}}\downarrow 
      && 
    \downarrow^{\sigma^Y_n}
    \\
    X_{n+1} \wedge K
     &\overset{f_{n+1}}{\longrightarrow}&
   Y_{n+1}
  }
  \,.
$$

Applying degreewise the adjunction

$$
  Top_{cg}^{\ast/}
    \underoverset
     {\underset{Maps(K,-)_\ast}{\longrightarrow}}
     {\overset{(-) \wedge K}{\longleftarrow}}
     {\bot}
  Top_{cg}^{\ast/}
$$

from [[Introduction to Stable homotopy theory -- P|classical homotopy theory]] ([this prop.](Introduction+to+Stable+homotopy+theory+--+P#PointedCompactlyGeneratedTopologicalSpacesIsSymmetricMonoidalClosed)) gives that these squares are in [[natural bijection]] with squares of the form

$$
  \array{
    S^1 \wedge X_n
      &\overset{\widetilde{S^1 \wedge f_n}}{\longrightarrow}&
    Maps(K,S^1 \wedge Y_n)_\ast
    \\
    {}^{\mathllap{\sigma_n^X}}\downarrow 
      && 
    \downarrow^{\mathrlap{Maps(K,\sigma_n^Y)_\ast}}
    \\
    X_{n+1} 
      &\overset{\widetilde{f_{n+1}}}{\longrightarrow}&
    Maps(K, Y_{n+1})_\ast
  }
  \,.
$$

But since the map $S^1 \wedge f_n$ is the smash product of two maps, only one of which involves the smash factor of $K$, one sees that here the top map factors through the map $(const,id)$ from def. \ref{TensoringAndPoweringOfSequentialSpectra}.


Hence the commuting square above factors as

$$
  \array{
    S^1 \wedge X_n
      &\overset{S^1 \wedge \widetilde{f_n}}{\longrightarrow}&
    S^1 \wedge Maps(K, Y_n)_\ast
    \\
    {}^{\mathllap{\sigma_n^X}}\downarrow 
      && 
    \downarrow^{\mathrlap{\sigma_n^{Maps(K,Y)_\ast}}}
    \\
    X_{n+1}
      &\overset{\widetilde {f_{n+1}}}{\longrightarrow}&
    Maps(K, Y_{n+1})_\ast
  }
  \,.
$$

This gives the structure maps for a homomorphism

$$
  \tilde f 
    \;\colon\;
  X \longrightarrow Maps(K,Y)_\ast
  \,.
$$

Running this argument backwards shows that the map $f \mapsto \tilde f$ given thereby is a bijection.

=--

+-- {: .num_remark}
###### Remark

For the [[adjunction]] of prop. \ref{AdjunctionBetweenSmashTensoringAndPowering} it is crucial that the smash tensoring in def. \ref{TensoringAndPoweringOfSequentialSpectra} is from the _right_, at least as long as the structure maps in def. \ref{SequentialSpectra} are defined as they are, with the circle smash factor on the left. We could change both jointly: take the structure maps to be from smash products with the circle on the right, and take smash tensoring to be from the left. But having both on the right or both on the left does not work.

=--





+-- {: .num_prop #SigmaInfinityOmegaInfinity}
###### Proposition

The functor $\Sigma^\infty$ that forms [[suspension spectra]] (def. \ref{SuspensionSpectrum}) has a [[right adjoint]] functor $\Omega^\infty$

$$
  (\Sigma^\infty \dashv \Omega^\infty)
  \;\colon\;
  SeqSpec(Top_{cg})
    \underoverset
      {\underset{\Omega^{\infty}}{\longrightarrow}}
      {\overset{\Sigma^\infty}{\longleftarrow}}
      {\bot}
  Top_{cg}^{\ast/}
  \,,
$$

given by picking the 0-component space:

$$
  \Omega^\infty(X) = X_0
  \,.
$$

=--

+-- {: .proof}
###### Proof

By def. \ref{SequentialSpectra} the components $f_n$ of a homomorphism of [[sequential spectra]] of the form 

$$
  \Sigma^\infty X \overset{f}{\longrightarrow} Y
$$ 

have to make these diagrams commute

$$
  \array{
    S^1 \wedge S^n X &\overset{S^1 \wedge f_n}{\longrightarrow}& S^1 \wedge Y_{n}
    \\
    {}^{\mathllap{\simeq}}\downarrow && \downarrow^{\mathrlap{\sigma^Y_n}}
    \\
    S^{n+1} \wedge X
    &\overset{f_{n+1}}{\longrightarrow}& Y_{n+1}
  }
$$

for all $n \in \mathbb{N}$. Since here the left vertical map is an isomorphism by def. \ref{SuspensionSpectrum}, this uniquely fixes $f_{n+1}$ in terms of $f_n$. Hence the only freedom in specifying $f$ is in the choice of the component $f_0 \colon X \longrightarrow Y_0$, which is equivalently a morphism

$$
  X \overset{\tilde f}{\longrightarrow} \Omega^\infty Y
  \,.
$$


=--



##### Stable homotopy groups

In analogy to how [[homotopy groups]] are the fundamental invariants in [[Introduction to Stable homotopy theory -- P|classial homotopy theory]], the fundamental invariants of stable homtopy theory are _stable homtopy groups_:




+-- {: .num_defn #StableHomotopyGroups}
###### Definition

The **[[stable homotopy groups]]** of a [[sequential prespectrum]] $X$, def. \ref{SequentialSpectra}, is the $\mathbb{Z}$-[[graded abelian group]] given by the [[colimit]] of [[homotopy groups]] of the component spaces ([def.](Introduction+to+Stable+homotopy+theory+-+P#HomotopyGroupsOftopologicalSpaces))

$$
  \pi_\bullet(X)
    \coloneqq
  \underset{\longrightarrow}{\lim}_k
  \pi_{\bullet+k}(X_{k})
  \,,
$$

where the colimit is over the [[sequential diagram]] whose component morphisms are given in terms of the structure maps of def. \ref{SequentialSpectra} by

$$
  \pi_{q+k}(X_k)
    \overset{\simeq}{\to}
  [S^{q+k},X_k]_\ast
    \overset{(S^1\wedge(-))_{S^{q+k},X_k}}{\longrightarrow}
  [S^{q+k+1}, S^1 \wedge X_k]_\ast
    \overset{[S^{q+k+1}, \sigma_k]}{\longrightarrow}
  [S^{q+k+1}, X_{k+1}]_\ast
    \overset{\simeq}{\to}
  \pi_{q+k+1}(X_{k+1})
$$

and equivalently are given in terms of the adjunct structure maps of def. \ref{SequentialSpectrumViaAdjunctStructureMaps} by

$$
  \pi_{q+k}(X_k)
    \overset{\simeq}{\longrightarrow}
  [S^{q+k}, X_k]_\ast
    \overset{[S^{q+k}, \tilde \sigma_k]}{\longrightarrow}
  [S^{q+k}, Maps(S^1,X_{k+1})_\ast]_\ast
    \simeq
  [S^1 \wedge S^{q+k}, X_{k+1}]_\ast
    \simeq
  \pi_{q+k+1}(X_{k+1})
  \,.
$$

The colimit starts at

$$
  k = 
  \left\{
    \array{
      0 & if \; q \geq 0
      \\
      {\vert q\vert} & if \; q \lt 0
    }
  \right.
$$

This canonically extends to a [[functor]]

$$
  \pi_\bullet \;\colon\; SeqSpec(Top_{cg}) \longrightarrow Ab^{\mathbb{Z}}
  \,.
$$


=--

+-- {: .num_prop #TwoVersionsOfComponentsForStableHomotopyGroupsAgree}
###### Proposition

The two component morphisms given in def. \ref{StableHomotopyGroups} indeed agree.

=--

+-- {: .proof}
###### Proof

Consider the following instance of the defining naturality square of the $(S^1 \wedge (-)) \dashv Maps(S^1,-)_\ast$-adjunction of prop. \ref{SuspensionAndLoopAdjunctionInClassicalHomotopyTheory}: 

$$
  \array{
    [S^1 \wedge X_k, S^1 \wedge X_k]_\ast
      &\overset{\simeq}{\longrightarrow}&
    [X_k, Maps(S^1, S^1 \wedge X_k)_\ast]_\ast
    \\
    {}^{\mathllap{[S^1 \wedge \alpha, \sigma_k]}}\downarrow 
      && 
    \downarrow^{\mathrlap{[\alpha, Maps(S^1,\sigma_k)_\ast]_\ast}}
    \\
    [S^1 \wedge S^{q+k}, X_{k+1}]_\ast
      &\underset{\simeq}{\longrightarrow}&
    [S^{q+k}, Maps(S^1, X_{k+1})_\ast]_\ast
  }
  \,.
$$

Then consider the identity element in the top left hom-set. Its image under the left vertical map is the first of the two given component morphisms. Its image under going around the other way is the second of the two component morphisms. By the commutativity of the diagram, these two images agree.

=--

+-- {: .num_example}
###### Example

Given $X \in Top^{\ast/}_{cg}$, then the [[stable homotopy groups]] (def. \ref{StableHomotopyGroups}) of its [[suspension spectrum]] (example \ref{SuspensionSpectrum}) are given by

$$
  \begin{aligned}
    \pi_q^S(X)
      & \;\coloneqq\;
    \pi_q(\Sigma^\infty X)
    \\
      & =
    \underset{\longrightarrow}{\lim}_{k} \pi_{q + k}(S^k \wedge X)
    \\
      & \simeq
    \underset{\longrightarrow}{\lim}_{k} \pi_{q}(\Omega^k ( \Sigma^k X))
  \end{aligned}
  \,.
$$

Specifically for $X = S^0$ the [[0-sphere]], with suspension spectrum the standard [[sphere spectrum]] (def. \ref{StandardSphereSpectrum}), its stable homotopy groups are the [[stable homotopy groups of spheres]]:

$$
  \begin{aligned}
    \pi_q^S(S^0)
      & \;\coloneqq\;
    \pi_q(\mathbb{S})
    \\
      & =
    \underset{\longrightarrow}{\lim}_{k} \pi_{q + k}(S^k)
  \end{aligned}
  \,.
$$

Recall the [[Freudenthal suspension theorem]], which states that if $X$ is an [[n-connected topological space|n-connected]] pointed [[CW-complex]] then the comparison map

$$
  \pi_{q}(X) \longrightarrow \pi_{q+1}(\Sigma X)
$$

is an isomorphism for $q \leq 2n$. This implies first of all that every $\Sigma^k X$ is $(k-1)$-connected

$$
  \begin{aligned}
    \pi_0(\Sigma X) & \simeq \ast
    \\    
    \pi_1(\Sigma^2 X) & \simeq \pi_0(\Sigma X) \simeq \ast
    \\
    \pi_2(\Sigma^3 X) & \simeq \pi_1(\Sigma^2 X) \simeq \pi_0(\Sigma X) \simeq \ast
    \\
    \cdots
  \end{aligned}
$$

and then that the $q$th stable homotopy group of $X$ is attained at stage $k = q+2$ in the colimit:

$$
  \pi^S_q(X) \simeq \pi_{q + (q+2)}(\Sigma^{q+2}X)
  \,.
$$
 
Historically, this fact was one of the motivations for finding a [[stable homotopy category]] (def. \ref{TheStableHomotopyCategory} below). 

=--




+-- {: .num_defn #StableWeakHomotopyEquivalenceOfSequentialTopologicalSpectra}
###### Definition

A morphism $f \colon X \longrightarrow Y$ of [[sequential spectra]], def. \ref{SequentialSpectra}, is called a **[[stable weak homotopy equivalence]]**, if its image under the [[stable homotopy group]]-functor of def. \ref{StableHomotopyGroups} is an [[isomorphism]]

$$
  \pi_\bullet(f) 
    \;\colon\; 
  \pi_\bullet(X) 
    \overset{\simeq}{\longrightarrow}
  \pi_\bullet(Y)
  \,.
$$

=--

+-- {: .num_example #OmegaSigmaAdjunctionUnitOnSequentialSpectraIsStableWeakHomotopyEquivalence}
###### Example

For $X \in SeqSpec(Top_{cg})$ then the [[adjunction unit]]

$$
  \eta_X 
  \;\colon\;
  X \longrightarrow Maps(S^1, S^1 \wedge X)_\ast
$$

(of the adjunction from prop. \ref{AdjunctionBetweenSmashTensoringAndPowering})
is a [[stable weak homotopy equivalence]] (def. \ref{StableWeakHomotopyEquivalenceOfSequentialTopologicalSpectra}).


=--

+-- {: .proof}
###### Proof

By the proof of prop. \ref{StableWeakHomotopyEquivalenceOfSequentialTopologicalSpectra}, on component spaces the adjunction is the corresponding adjunction of topological spaces from prop. \ref{SuspensionAndLoopAdjunctionInClassicalHomotopyTheory}. Hence the morphism of directed systems of groups that enter the defininition of stable homotopy groups in def. \ref{StableHomotopyGroups} looks as follows

$$
  \array{
    \cdots 
      &\to&
    [S^{q+k},X_k]_\ast
      &\overset{(S^1\wedge(-))_{S^{q+k},X_k}}{\longrightarrow}&
    [S^{q+k+1}, S^1 \wedge X_k]_\ast
      &\overset{[S^{q+k+1}, \sigma_k]}{\longrightarrow}&
    [S^{q+k+1}, X_{k+1}]_\ast
      &\to&
    \cdots
    \\
    &&
    {}^{\mathllap{[S^{q+k},\eta_{X_k}]_\ast }}\downarrow
    && 
    \downarrow
    &&
    \downarrow
    \\
    \cdots
      &\to&
    [S^{q+k},Maps(S^1, S^1 \wedge X_k)_\ast]_\ast
      &\overset{}{\longrightarrow}&
    [S^{q+k+1}, S^1 \wedge Maps(S^1, S^1 \wedge X_k)_\ast]_\ast
      &\overset{}{\longrightarrow}&
    [S^{q+k+1}, Maps(S^1, S^1 \wedge X_{k+1})_\ast]_\ast    
      &\to&
    \cdots 
  }
  \,.
$$

Observe then that the adjunction isomorphism $[S^{q+k+1}, S^1 \wedge X_k]_\ast \overset{\simeq}{\to} [S^{q+k},Maps(S^1, S^1 \wedge X_k)_\ast]_\ast$ fits into a commuting triangle

$$
  \array{
    [S^{q+k},X_k]_\ast
      &\overset{(S^1\wedge(-))_{S^{q+k},X_k}}{\longrightarrow}&
    [S^{q+k+1}, S^1 \wedge X_k]_\ast
    \\
    {}^{\mathllap{[S^{q+k},\eta_{X_k}]_\ast }}\downarrow
      & \swarrow_{\mathrlap{\simeq}}
    \\
    [S^{q+k},Maps(S^1, S^1 \wedge X_k)_\ast]_\ast
  }
  \,.
$$

To see this in detail, consider for any $\alpha \in [S^{q+k},X_k]$ the adjunction naturality square

$$
  \array{
    [S^1 \wedge X_k, S^1 \wedge X_k]_\ast
      &\overset{\simeq}{\longrightarrow}&
    [X_k, Maps(S^1, S^1 \wedge X_k)_\ast]_\ast
    \\
    {}^{\mathllap{S^1 \wedge \alpha \circ (-) \circ id}}\downarrow 
    &&
    \downarrow^{\mathrlap{\alpha \circ (-) \circ Maps(S^1, id)_\ast}}
    \\
    [S^{q+k+1}, S^1 \wedge X_k]
      &\underset{\simeq}{\longrightarrow}&
    [S^{q+k}, Maps(S^1, S^1 \wedge X_k)]
  }
$$

and chase $id_{S^1 \wedge X_k}$ both ways from top left to bottom right.

These diagonal isomorphism imply that under taking the [[colimit]] over the horizontal sequences, the vertical morphisms induce an isomorphism.

=--

+-- {: .num_example #MorphismsOfSequentialSpectraIsStableWeakHomotopyEquivalencePreviselyIfItsSmashWithCircleIs}
###### Example

A morphsim $f\colon X \to Y$ in $SeqSpec(Top_{cg})$ is a [[stable weak homotopy equivalence]] precisely if its smash tensoring $f \wedge S^1 \colon X \wedge S^1 \to Y \wedge S^1$ is.

=--


+-- {: .num_prop #LongExactSequenceofStableHomotopyGroupsViaMappingCones}
###### Proposition

Let $f \;\colon\; X \longrightarrow Y$ be a morphism in $SeqSpec(Top_{cg})$. Write 

$$ 
  Y \overset{j}{\longrightarrow} Cone(f)
$$

for its [[mapping cone]] and 

$$
  Path_\ast(f) \overset{i}{\longrightarrow} X
$$ 

for its [[mapping cocone]] ([def.](Introduction+to+Stable+homotopy+theory+-+P#MappingConeAndMappingCocone)) formed with respect to the standard [[cylinder spectrum]] from def. \ref{StandardCylinderSpectrumSequential}. 

Then the canonical morphism

$$
  \phi \;\colon\; Path_\ast(f) \longrightarrow Maps(S^1, Cone(f))_\ast
$$

is a [[stable weak homotopy equivalence]] and it sits in a [[commuting diagram]] of [[stable homotopy groups]] $\pi_\bullet$ (def. \ref{StableHomotopyGroups}) of the form

$$
  \array{
     \cdots
       &\to&
     \pi_{\bullet}(Path_\ast(f))
       &\overset{i_\ast}{\longrightarrow}&
     \pi_\bullet(X)
       &\overset{}{\longrightarrow}&
     \pi_\bullet(Y)
       &\longrightarrow&
     \pi_{\bullet-1}(Path_\ast(f))
       &\to&
     \cdots 
     \\
     && 
      {}^{\mathllap{\simeq}}\downarrow^{\phi_\ast}
        &&
      {}^{\mathllap{\simeq}}\downarrow^{\eta_X} 
        && 
      {}^{\mathllap{\simeq}}\downarrow^{\eta_Y} 
        && 
      {}^{\mathllap{\simeq}}\downarrow^{\mathrlap{\phi}}
    \\
    \cdots
      &\to&
    \pi_{\bullet+1}(Cone(f))
     &\longrightarrow&
    \pi_\bullet(X)
      &\overset{f_\ast}{\longrightarrow}&
    \pi_\bullet(Y)
      &\overset{j_\ast}{\longrightarrow}&
    \pi_\bullet(Cone(f)) 
      &\to&
    \cdots
  }
  \,,
$$

where the top and bottom are [[long exact sequences]], and where $\eta_{X}\colon X \to \Omega \Sigma X$ is [[stable weak homotopy equivalence]] from example \ref{OmegaSigmaAdjunctionUnitOnSequentialSpectraIsStableWeakHomotopyEquivalence}.

Dually, the canonical morphism

$$
  \tilde \phi \;\colon\; Path_\ast(f) \wedge S^1 \longrightarrow Cone(f)
$$

is a [[stable weak homotopy equivalence]] and it sits in a similar commuting diagram
 

$$
  \array{
    \cdots
      &\to&
    \pi_{\bullet+1}(Cone(f))
     &\longrightarrow&
    \pi_\bullet(X)
      &\overset{f_\ast}{\longrightarrow}&
    \pi_\bullet(Y)
      &\overset{j_\ast}{\longrightarrow}&
    \pi_\bullet(Cone(f)) 
      &\to&
    \cdots
     \\
     && 
      {}^{\mathllap{\simeq}}\downarrow^{\tiilde \phi_\ast}
        &&
      {}^{\mathllap{\simeq}}\downarrow^{\epsilon_X} 
        && 
      {}^{\mathllap{\simeq}}\downarrow^{\epsilon_Y} 
        && 
      {}^{\mathllap{\simeq}}\downarrow^{\mathrlap{\tilde \phi}}
    \\
     \cdots
       &\to&
     \pi_{\bullet}(Path_\ast(f))
       &\overset{i_\ast}{\longrightarrow}&
     \pi_\bullet(X)
       &\overset{}{\longrightarrow}&
     \pi_\bullet(Y)
       &\longrightarrow&
     \pi_{\bullet-1}(Path_\ast(f))
       &\to&
     \cdots 
  }
  \,,
$$


=--

([Lewis-May-Steinberger 86, lemma 2.1, lemma 2.3, theorem 2.4](#LewisMaySteinberger86), [Mandell-May-Schwede-Shipley 01, theorem 7.4 (vi)](#MMSS00))

+-- {: .proof}
###### Proof

For the following discussion, recall from the nature of the standard sequential cylinder spectrum $X \wedge (I_+)$ and the fact that limits and colimits of sequential spectra are computed degreewise (prop. \ref{LimitsAndColimitsOfSequentialSpectra}) it follows that the mapping cones and mapping cocones of sequential spectra are degreewise the mapping cones and mapping cocones of pointed topological spaces induced from the standard reduced cyclinder construction ([def.](Introduction+to+Stable+homotopy+theory+--+P#StandardReducedCyclinderInTop)) of pointed topological spaces.

We consider the first case. The second is formally dual.

Regarding the exactness of the top sequence:

The ordinary (unstable) [[homotopy groups]] of the component spaces form [[long exact sequences of homotopy groups]] to the left ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#LongExactSequeceOfHomotopyGroups)) yielding [[commuting diagrams]] of the form
$$
  \array{
     \cdots
       &\to&
     \pi_{q+k+1}(Y_k)
       &\longrightarrow&
     \pi_{q+k}(Path_\ast(f_k))
       &\longrightarrow&
     \pi_{q+k}(X_k) 
       &\longrightarrow&
     \pi_{q+k}(Y_k)
     \\
     && \downarrow && \downarrow && \downarrow && \downarrow
     \\
     \cdots
       &\to&
     \pi_{q+k+2}(Y_{k+1})
       &\longrightarrow&
     \pi_{q+k+1}(Path_\ast(f_{k+1}))
       &\longrightarrow&
     \pi_{q+k+1}(X_{k+1}) 
       &\longrightarrow&
     \pi_{q+k+1}(Y_{k+1})
     \\
     && \downarrow && \downarrow && \downarrow && \downarrow
     \\
     \cdots
       &\to&
     \pi_{q+k+3}(Y_{k+2})
       &\longrightarrow&
     \pi_{q+k+2}(Path_\ast(f_{k+2}))
       &\longrightarrow&
     \pi_{q+k+2}(X_{k+2}) 
       &\longrightarrow&
     \pi_{q+k+2}(Y_{k+2})
     \\
     && \downarrow && \downarrow && \downarrow && \downarrow
     \\
     && \vdots && \vdots && \vdots && \vdots
  }
  \,.
$$

Here the vertical morphisms are those entering the definition of stable homotopy groups (def. \ref{StableHomotopyGroups}), and one checks that these indeed make all the squares commute due to the respect of the component maps for the structure maps of the sequential spectra.

Now taking the [[colimit]] over the vertical morphisms yields the sequence

$$
  \array{
     \cdots
       &\to&
     \pi_{\bullet}(Path_\ast(f))
       &\overset{i_\ast}{\longrightarrow}&
     \pi_\bullet(X)
       &\overset{}{\longrightarrow}&
     \pi_\bullet(Y)
       &\longrightarrow&
     \pi_{\bullet-1}(Path_\ast(f))
  }
$$

and that this is exact follows since on the category [[Ab]] of [[abelian group]], forming [[filtered colimits]] is an [[exact functor]] ([prop.](Mod#FilteredColimitsInRModAreExact)).

Now regarding the exactness of the bottom sequence:

Since the mapping cone of the mapping cone inclusion is the suspension, and since by example \ref{OmegaSigmaAdjunctionUnitOnSequentialSpectraIsStableWeakHomotopyEquivalence} there is an isomorphism

$$
  \pi_\bullet(X) \simeq \pi_{\bullet+1}(X \wedge S^1)
$$

it is sufficient to show that for every $f$ and $q$ the sequence

$$
  \pi_q(X) \overset{f_\ast}{\longrightarrow} \pi_q(Y) \overset{j_\ast}{\longrightarrow} \pi_q(Cone(f))
$$

is exact in the middle. It is clear from the construction of the mapping cone that the composite morphism is zero, therefore what remains to be shown is that every element in the [[kernel]] of $j_\ast$ is in the image of $f_\ast$.

So let $\alpha|_k \colon S^{k+q} \longrightarrow Y_k$ be a representative of an element $\alpha \in \pi_q(Y)$ such that $S^{k+q} \overset{\alpha|_k}{\longrightarrow} Y_k \overset{j_k}{\longrightarrow} Cone(f)_k$ is null-homotopic, in that there is a [[left homotopy]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#LeftHomotopy)) $\eta$ of the form

$$
  \array{   
     S^{q+k} &\overset{}{\longrightarrow}& \ast
     \\
     \downarrow && \downarrow 
     \\
     S^{q+k} \wedge (I_+) & \overset{\eta}{\longrightarrow}& Cone(f)_k
     \\
     \uparrow && \uparrow^{\mathrlap{j_k}}
     \\
     S^{q+k} &\underset{\alpha|_k}{\longrightarrow}& Y_k
  }
  \,.
$$ 

In terms of the [[pushout]] of the top square, which is $Cone(S^{q+k})$, this is equivalently a map $\eta'$ forming this [[commuting square]]:

$$
  \array{
    S^{q+k} &\longrightarrow& Cone(S^{q+k})
    \\
    \downarrow^{\mathrlap{\alpha|_k}} && \downarrow^{\mathrlap{\eta'}}
    \\
    Y_k &\underset{j_k}{\longrightarrow}& Cone(f)_k
  }
  \,.
$$

Consider then the induced long cofiber sequences to the right ([prop.](Introduction+to+Stable+homotopy+theory+--+P#LongFiberSequence)), and paste a copy of the structure compatibility square for the homomrphism $f$ to it, to obtain a [[commuting diagram]] of the form

$$
  \array{
      &&
    S^{q+k} 
      &\longrightarrow& 
    Cone(S^{q+k})
      &\longrightarrow& 
    S^{q+k+1} 
      &\overset{\simeq}{\longrightarrow}& 
    S^{q+k+1}
    \\
      &&
    \downarrow^{\mathrlap{\alpha|_k}} 
      && 
    \downarrow^{\mathrlap{\eta'}}
      &&
    \downarrow^{\mathrlap{\kappa}}
      &&
    \downarrow^{\mathrlap{\alpha|_k \wedge S^1}}
    \\
    X_k
      &\overset{f_k}{\longrightarrow}&
    Y_k 
      &\underset{j_k}{\longrightarrow}& 
    Cone(f)_k
      &\longrightarrow&
    X_k \wedge S^1
      &\overset{f_k \wedge S^1}{\longrightarrow}&
    Y_k \wedge S^1
    \\
      && && && 
    \downarrow^{\mathrlap{\sigma^X_k}} 
      && 
    \downarrow^{\mathrlap{\sigma^Y_k}}
    \\
      && && && 
    X_{k+1} &\overset{f_{k+1}}{\longrightarrow}& Y_{k+1}
  }
  \,.
$$

Now the total vertical rectangle on the right appearing here, exhibits an element $\sigma^X_k \circ \kappa$ in $\pi_{k+q+1}(X_{k+1})$ which is a preimage under $f_\ast$ of the original element $\alpha|_k$ exhibited at the successor stage $\alpha|_{k+1}$: in terms of the directed sequence that defines the stable homotopy groups in def. \ref{StableHomotopyGroups}, we find

$$
  \array{
    \alpha|_k  &&  && \alpha|_{k+1} =  f_\ast(\sigma^X_k \circ \kappa)
    \\
    \in && && \in
    \\
    [S^{q+k},X_k]_\ast
      &\overset{(S^1\wedge(-))_{S^{q+k},Y_k}}{\longrightarrow}&
    [S^{q+k+1}, S^1 \wedge X_Y]_\ast
      &\overset{[S^{q+k+1}, \sigma^Y_k]}{\longrightarrow}&
    [S^{q+k+1}, Y_{k+1}]_\ast
  }
  \,.
$$

Finally regarding the vertical morphisms $\phi_\ast$

First notice that $\phi$ makes commuting squares in the first place. Hence in summary we do have a commuting diagram of exact sequences as shown in the statement, and hence the fact that $\phi_\ast$ is an isomorphism follows from exactness via the [[five lemma]]. Hence $\phi$ is a stable weak homotopy equivalence.

=--

+-- {: .num_remark}
###### Remark

Prop. \ref{LongExactSequenceofStableHomotopyGroupsViaMappingCones} says that for sequential spectra there are [[long exact sequences of homotopy groups]] as in classical homotopy theory ([exmpl](Introduction+to+Stable+homotopy+theory+--+P#LongExactSequeceOfHomotopyGroups)), but what used to be long fiber sequences to the left and long cofiber sequences to the right is unified to a single long sequences extending in both directions. 

However, at this point we have not shown yet that these sequences are indeed exhibited by the canonical [[homotopy fiber sequences]] in any [[stable homotopy theory]] of spectra. After seeting up this stable homotopy theory [below](#StableModelStructureOnSequentialSpectra), we prove this further below in prop. \ref{LongExactSequenceOfStableHomotopyGroups}.

=--




##### Omega-spectra
 {#OmegaSpectra}


In order to motivate [[Omega-spectra]] consider the following shadow of the structure they will carry:

+-- {: .num_example #BlueprintForIdeaOfOmegaSpectra}
###### Example

A $\mathbb{Z}$-[[graded abelian group]] is equivalently a sequence $\{A_n\}_{n \mathbb{Z}}$ of $\mathbb{N}$-graded abelian groups $A_n$, together with isomorphisms

$$
  A_n \simeq A_{n+1}[1]
  \,,
$$

(where $[1]$ denotes the operation of shifting all entries in a graded abelian group down in degree by -1). Because this means that the sequence of $\mathbb{N}$-graded abelian groups is of the following form

$$
  \array{
    \vdots && \vdots 
    \\
    a_3 && a_2 && a_1 && \cdots
    \\
    a_2 && a_1 && a_0 && \cdots
    \\
    a_1 && a_0 && a_{-1} && \cdots
    \\
    \underset{A_0}{\underbrace{a_0}}
    &&
    \underset{A_1}{\underbrace{a_{-1}}}
    &&
    \underset{A_2}{\underbrace{a_{-2}}}
    &&
    \cdots
  }
  \,.
$$

This allows to recover the $\mathbb{Z}$-graded abelian group $\{a_n\}_{n \in \mathbb{Z}}$ from an $\mathbb{N}$-sequence of $\mathbb{N}$-graded abelian groups.

Then consider the case that the $\mathbb{N}$-graded abelian groups here are [[homotopy groups]] of some [[topological space]]. Then shifting the degree of the component groups corresponds to forming [[loop spaces]], because for any topological space $X$ then 

$$
  \pi_\bullet(\Omega X) 
  \simeq
  \pi_{\bullet + 1}(X)
  \,.
$$

(This may be seen concretely in point-set topology or abstractly by looking at the [[long exact sequence of homotopy groups]] for the fiber sequence $\Omega X \to Path_*(X) \to X$.)

We find this kind of behaviour for the stable homotopy groups of Omega-spectra below in example \ref{StableHomotopyGroupsOfOmegaSpectrum}.

=--


+-- {: .num_defn #OmegaSpectrum}
###### Definition

An **[[Omega-spectrum]]** is a [[sequential spectrum]] $X$ of topological spaces, def. \ref{SequentialSpectra}, such that the ([[smash product]] $\dashv$ [[pointed mapping space]])-[[adjuncts]] $\tilde \sigma_n$ of the structure maps $\sigma_n \colon \Sigma X_n \to X_{n+1}$ of $X$ are [[weak homotopy equivalences]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#WeakHomotopyEquivalenceOfTopologicalSpaces)), hence classical weak equivalences ([def.](Introduction+to+Stable+homotopy+theory+--+P#ClassesOfMorhismsInTopQuillen)):

$$
  \tilde \sigma_n
  \;\colon\;
  X_n  \stackrel{\in W_{cl}}{\longrightarrow}  Maps(S^1,X_{n+1})_\ast
$$

for all $n \in \mathbb{N}$.

Equivalently: an [[Omega-spectrum]] is a sequential spectrum in the incarnation of def. \ref{SequentialSpectrumViaAdjunctStructureMaps} such that all adjunct structure maps are weak homotopy equivalences.

=--

Omega-spectra are singled out among all sequential pre-spectra as having good behaviour under forming [[stable homotopy groups]].

+-- {: .num_example #StableHomotopyGroupsOfOmegaSpectrum}
###### Example

If a [[sequential spectrum]] $X$ is an [[Omega-spectrum]], def. \ref{OmegaSpectrum}, then its colimiting [[stable homotopy groups]] reduce to the actual homotopy groups of the component spaces, in that:

$$
  X \; \text{Omega-spectrum}
  \;\;\;\;\;
   \Rightarrow
  \;\;\;\;\;
  \pi_k(X)
    \simeq
  \left\{
    \array{
      \pi_k X_0  & if\; k \geq 0
      \\
      \pi_0 X_{\vert k \vert}  & if \; k \lt 0
    }
  \right.
  \,.
$$

(Hence the stable homotopy groups of an Omega-spectrum realize the general pattern discussed in example \ref{BlueprintForIdeaOfOmegaSpectra}.)

=--


+-- {: .proof}
###### Proof

For an Omega-spectrum, the adjunct structure maps $\tilde \sigma_X$ are [[weak homotopy equivalences]], by definition, hence are classical weak equivalences. Hence $[S^1, \tilde \sigma_n]_\ast$ is an isomorphism ([prop.](Introduction+to+Stable+homotopy+theory+--+P#UniversalPropertyOfHomotopyCategoryOfAModelCategory)). Therefore, by prop. \ref{TwoVersionsOfComponentsForStableHomotopyGroupsAgree}, the [[sequential colimit]] in def. \ref{StableHomotopyGroups} is entirely over isomorphisms and hence is given already by the first object of the sequence.

=--


We now show that every sequential pre-spectrum may be completed to an Omega-spectrum, up to stable weak homotopy equivalence:

+-- {: .num_defn #SpectrificationForTopologicalSequentialSpectra}
###### Definition

For $X \in SeqSpec(Top_{cg})$, define a spectrum $Q X \in SeqSpec(Top_{cg})$ and a morphism

$$
  j_X \;\colon\; X \longrightarrow Q X
$$

(to be called the **[[spectrification]]** of $X$) as follows.

First introduce for the given components $X_k$ and adjunct structure maps $\tilde \sigma_k$ of $X$ (from def. \ref{SequentialSpectrumViaAdjunctStructureMaps}) the notation

$$
  Z_{0,k} \coloneqq X_{k}
  \,,
  \;\;\;\;\;\;
  \tilde \sigma_{0,k} \coloneqq \tilde \sigma_k
  \,.
$$

Now assume, by [[induction]], that sets of objects $\{Z_{i,k}\}_{k \in \mathbb{N}}$ and maps $\{Z_{i,k} \overset{\tilde \sigma_{i,k}}{\to} \Omega Z_{i,k+1}\}_{k \in \mathbb{N}}$ have been constructed for some $i \in \mathbb{N}$. 

Then construct $Z_{i+1,k}\in Top_{cg}$ by factorizing $\tilde \sigma_{i,k}$, with respect to the model structure $(Top^{\ast/}_{cg})_{Quillen}$ ([thm.](Introduction+to+Stable+homotopy+theory+--+P#ClassicalModelStructureOnCompactlyGeneratedTopologicalSpaces))  as a classical cofibration followed by a classical weak equivalence. More specifically, apply the [[small object argument]] ([prop.](Introduction+to+Stable+homotopy+theory+--+P#SmallObjectArgument)) with respect to the set of generating cofibrations $I_{Top}$ ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopologicalGeneratingCofibrations)) to produce [[functorial factorizations]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#FunctorialWeakFactorizationSystem)) into a [[relative cell complex]] followed by a [[weak homotopy equivalence]] (just as in the proof of [this lemma](Introduction+to+Stable+homotopy+theory+--+P#FactorizationInTopQuillen)):

$$
  \tilde \sigma_{i,k}
    \;\colon\;
  Z_{i,k}
   \underoverset{\in I_{Top} Cell}{\iota_{i,k}}{\longrightarrow}
  Z_{i+1,k}
   \underoverset{\in W_{cl}}{\phi_{i,k}}{\longrightarrow}
  \Omega Z_{i,k+1}
  \,.
$$

Then define $\tilde \sigma_{i+1,k}$ as the composite

$$
  \tilde \sigma_{i+1,k}
    \;\colon\;
  Z_{i+1,k}
    \overset{\phi_{i,k}}{\longrightarrow}
  \Omega Z_{i,k+1}
    \overset{\Omega (\iota_{i,k+1})}{\longrightarrow}
  \Omega Z_{i+1,k+1} 
  \,.
$$

This produces for each $i \in \mathbb{N}$ a [[commuting diagram]] of the form

$$
  \array{
    X_k = Z_{0,k}
     &\underoverset{\in I_{Top} Cell}{\iota_{0,k}}{\longrightarrow}&
    Z_{1,k}
     &\underoverset{\in I_{Top} Cell}{\iota_{1,k}}{\longrightarrow}&
    Z_{2,k}
     &\underoverset{\in I_{Top} Cell}{\iota_{2,k}}{\longrightarrow}&
    \cdots
    \\
    {}^{\mathllap{\tilde \sigma_k = \tilde \sigma_{0,k}}}\downarrow
    &&
    {}^{\mathllap{\tilde \sigma_{1,k}}}\downarrow
    &&
    {}^{\mathllap{\tilde \sigma_{2,k}}}\downarrow
    &&
    \cdots
    \\
    \Omega X_{k+1}
    =
    \Omega Z_{0,k+1}
    &\overset{\Omega (\iota_{0,k+1})}{\longrightarrow}&
    \Omega Z_{1,k+1}
    &\overset{\Omega (\iota_{1,k+1})}{\longrightarrow}&
    \Omega Z_{2,k+1}
    &\overset{\Omega (\iota_{2,k+1})}{\longrightarrow}&
    \cdots
  }
  \,.
$$

That this indeed commutes is the identity

$$
  \begin{aligned}
    \tilde \sigma_{i+1,k} \circ \iota_{i,k}
    & =
    (\Omega(\iota_{i,k+1}) \circ \phi_{i,k}) \circ \iota_{i,k}
    \\
    & =
    \Omega(\iota_{i,k+1}) \circ (\phi_{i,k} \circ \iota_{i,k})
    \\
    & = 
    \Omega(\iota_{i,k+1}) \circ \tilde \sigma_{i,k}
  \end{aligned}
  \,.
$$

Now let $Q X$ be the spectrum with component spaces the [[colimit]] 

$$
  (Q X)_k \coloneqq \underset{\longrightarrow}{\lim}_i Z_{i,k}
$$

and with adjunct structure maps (via def. \ref{SequentialSpectrumViaAdjunctStructureMaps}) given by the map induced under colimits by the above diagrams

$$
  \tilde \sigma^{Q X}_k
  \;\coloneqq\;
  \underset{\longrightarrow}{\lim} \tilde \sigma_{i,k}
  \;\colon\;
  Q X 
  \longrightarrow \Omega(Q X)
  \,.
$$

Notice that this is indeed well-defined: since each component map $X_{i,k} \to X_{i+1,k}$ is a [[relative cell complex]] and since the [[1-sphere]] $S^1$ is [[compact topological space|compact]], it follows ([lemma](Introduction+to+Stable+homotopy+theory+--+P#CompactSubsetsAreSmallInCellComplexes)) that 

$$
  \begin{aligned}
    \underset{\longrightarrow}{\lim}_{i} \Omega Z_{i,k}
      & =
    \underset{\longrightarrow}{\lim}_{i} Maps(S^1, Z_{i,k})_\ast
    \\
    & \simeq
    Maps(S^1, \underset{\longrightarrow}{\lim}_i Z_{i,k} )_\ast
    \\
     & =  \Omega \underset{\longrightarrow}{\lim}_i Z_{i,k}
    \\
    & \simeq (\Omega Q X)
  \end{aligned}
  \,.
$$


Finally, let 

$$
  j_X \colon X \to Q X
$$ 

be degreewise the inclusion of the first component ($i = 0$) into the colimit. By construction, this is a homomorphism of sequential spectra (according to def. \ref{SequentialSpectrumViaAdjunctStructureMaps}).


=--

+-- {: .num_prop #PropertiesOfSpectrificationForTopologicalSequentialSpectra}
###### Proposition

Let $X\in SeqSpec(Top_{cg})$ be a [[sequential prespectrum]] with $j_X \colon X \to Q X$ from def. \ref{SpectrificationForTopologicalSequentialSpectra}. Then:

1. $Q X$ is an [[Omega-spectrum]] (def. \ref{OmegaSpectrum});

1. $j_X \colon X \to Q X$ is a [[stable weak homotopy equivalence]] (def. \ref{StableWeakHomotopyEquivalenceOfSequentialTopologicalSpectra}):

1. $j_X$ is a level weak equivalence (is in $W_{strict}$, def. \ref{ClassesOfMorphismsOfTheStrictModelStructureOnSequentialSpectra}) precisely if $X$ is an [[Omega-spectrum]];

1. a morphism $f \colon X  \to Y$ is a [[stable weak homotopy equivalence]] (def. \ref{StableWeakHomotopyEquivalenceOfSequentialTopologicalSpectra}), precisely if $Q f \colon Q X \to Q Y$ is a level weak equivalence (is in $W_{strict}$, def. \ref{ClassesOfMorphismsOfTheStrictModelStructureOnSequentialSpectra}).

=--

([Schwede 97, lemma 2.1.3 and remark before section 2.2](#Schwede97))

+-- {: .proof}
###### Proof

Since the colimit defining $Q X$ is a [[transfinite composition]] of [[relative cell complexes]], each component map $X_k \to (Q X)_k$ is itself a relative cell complex. Since [[n-spheres]] are [[compact topological spaces]], it follows ([lemma](Introduction+to+Stable+homotopy+theory+--+P#CompactSubsetsAreSmallInCellComplexes)) that each element of a [[homotopy group]] in $\pi_\bullet((Q X)_k)$ is in the image of a finite stage $\pi_\bullet(Z_{i,k})$ for some $i \in \mathbb{N}$. From this, all statements follow by inspection at finite stages.

Regarding first statement: 

Since each $\tilde \sigma_{i,k}$ by construction is a weak homotopy equivalence followed by an inclusion of stages in the colimit, as any element of $\pi_q((Q X)_k)$ is sent along $\tilde \sigma^{Q X}_k$ it passes through one such $\pi_q(\tilde \sigma_{i ,k})$ at some stage $i$, hence also through all the following, and is hence identically preserved in the colimit. 

Regarding the second statement: 

By the previous statement and by example \ref{StableHomotopyGroupsOfOmegaSpectrum}, the map $\pi_\bullet(j_X) \colon \pi_\bullet(X)\to \pi_\bullet(Q X)$ is given in degree $q \geq 0$ by

$$
  \underset{
    \simeq \underset{\longrightarrow}{\lim}_k  \pi_q \left(\Omega^k X_k\right)
  }
  {
  \underbrace{
    \underset{\longrightarrow}{\lim}_{k \in \mathbb{N}}  \pi_{q+k}(X_k)
  }}
  \longrightarrow
  \underset{
    \simeq
    \pi_q \left(
      \underset{\longrightarrow}{\lim}_k \Omega^k X_k
    \right)
  }{
  \underbrace{
    \pi_q \left(
      (Q X)_0
    \right)
  }}
$$

and similarly in degree $q\lt 0$. That these morphisms are isomorphism, hence that forming homotopy groups commutes over the sequential colimit of relative cell complex inclusions, is again due to the compactness of the $n$-spheres.

Regarding the third statement:

In one direction:

If $X$ is an Omega-spectrum in that all its adjunct structure maps $\tilde \sigma_k$ are [[weak homotopy equivalences]], then by [[two-out-of-three]] also the maps $\iota_{i,k}$ in def. \ref{SpectrificationForTopologicalSequentialSpectra} are weak homotopy equivalences. Hence $(j_X)_k \colon  X_k \to (Q X)_k$ is the map into a sequential colimit over acyclic relative cell complexes, and again by the compactness of the spheres, this means that it is itself a weak homotopy equivalence.

In the other direction:

If $j_X$ is degrewise a weak homotopy equivalence, then by applying [[two-out-of-three]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#CategoryWithWeakEquivalences)) to the compatibility squares for the adjunct structure morphisms (def. \ref{SequentialSpectrumViaAdjunctStructureMaps}), using that $\tilde \sigma^{Q X}_n$ is a weak homotopy equivalence by the first point above

$$
  \array{
    X_n 
      &\underoverset{\in W_{cl}}{(j_X)_n}{\longrightarrow}&
    (Q X)_n
    \\
    {}^{\mathllap{\tilde \sigma^X_n}}\downarrow 
      && 
    \downarrow^{\mathrlap{\tilde \sigma^{Q X}_n}}_{\mathrlap{\in W_{cl}}}
    \\
    Maps(S^1,X_{n+1})
     &\underoverset{\Maps(S^1,(j_X)_{n+1})}{\in W_{cl}}{\longrightarrow}&
    Maps(S^1, (Q X)_{n+1})
  }
$$

implies that also $\tilde \sigma^X_n \in W_{cl}$, hence that $X$ is an Omega-spectrum.

The fourth statement follows with similar reasoning.

=--




##### As topological diagrams

In order to conveniently understand the stable [[model category]] structure on spectra, we now consider an equivalent reformulation of the component-wise definition of sequential spectra, def. \ref{SequentialSpectra}, as [[topologically enriched functors]] ([defn. ](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctor)). 


+-- {: .num_defn #CategoriesOfStandardSpheres}
###### Definition

Write 

$$
  \iota \;\colon\; StdSpheres \longrightarrow Top_{cg}^{\ast/}
$$

for the non-full [[topologically enriched category|topologically enriched]] [[subcategory]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopEnrichedCategory)) of that of [[pointed topological spaces|pointed]] [[compactly generated topological spaces]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopkAsATopologicallyEnrichedCategory)) where:

* [[objects]] are the standard [[n-spheres]] $S^n$, for $n \in \mathbb{N}$, identified as the [[smash product]] powers $S^n \coloneqq (S^1)^{\wedge^n}$ of the standard circle;

* [[hom-spaces]] are

  $$
    StdSpheres(S^{n}, S^{k+n})
      \coloneqq
    \left\{
      \array{
        \ast & for & k \lt 0
        \\
        S^k 
        & otherwise
      }
    \right.
  $$

* [[composition]] is induced from composition in $Top^{\ast/}_{cg}$ by regarding the [[hom-space]] $S^k$ above as its [[image]] in $Maps({S^n},S^{k+n})_\ast$ under the [[adjunct]]

$$
  S^{k} \stackrel{}{\to} Maps({S^n},S^{k+n})_\ast
$$

of the canonical isomorphism

$$
  S^k \wedge S^n \overset{\simeq}{\longrightarrow} S^{k+n}
  \,.
$$

This induces the category 

$$
  [StdSpheres, Top^{\ast/}_{cg}]
$$

of [[topologically enriched functors]] on $StdSpheres$ with values in $Top_{cg}^{\ast/}$ ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctorsToTopk)).

=--


+-- {: .num_prop #SequentialSpectraAsDiagramSpectra}
###### Proposition

There is an [[equivalence of categories]]

$$
  (-)^seq
    \;\colon\;
  [StdSpheres,\; Top_{cg}^{\ast/}]
    \overset{\simeq}{\longrightarrow}
  SeqSpec(Top_{cg})
$$

from the category of [[topologically enriched functors]] on the category of standard spheres of def. \ref{CategoriesOfStandardSpheres} to the category of topological sequential spectra, def. \ref{SequentialSpectra}, which is given on objects by sending $X \in [StdSpheres,Top^{\ast/}]$ to the sequential prespectrum $X^{seq}$ with components

$$
  X^{seq}_n \coloneqq X(S^n)
$$

and with structure maps

$$
  \frac{
    S^1 \wedge X^{seq}_n \stackrel{\sigma_n}{\longrightarrow} X^{seq}_n
  }{
    S^1 \longrightarrow Maps(X^{seq}_n, X^{seq}_{n+1})_\ast
  }
$$

given by

$$
  S^1
    \stackrel{\widetilde{id}}{\longrightarrow}
  Maps(S^n,S^{n+1})_\ast
    \stackrel{X_{S^n, S^{n+1}}}{\longrightarrow}
  Maps(X^{seq}_n, X^{seq}_{n+1})
  \,.
$$

=--

+-- {: .proof}
###### Proof

The action of a given topological functor $X$ on hom-spaces between spheres of consecutive dimension 

$$
  X_{S^n, S^{n+1}}
    \;\colon\;
  S^1 
    \longrightarrow
  Maps(X(S^n), X(S^{n+1}))_\ast
$$

is naturally identified with its [[adjunct]]

$$
  \widetilde {X_{S^n, S^{n+1}}}
    \;\colon\;
  S^1 \wedge X(S^n) \longrightarrow S^{n+1}
  \,.
$$

This gives the structure maps. It only remains to see that from these maps the functor is already uniquely determined. Indeed, by definition the hom-space between non-consecutive spheres $StdSpheres(S^n, S^{n+k})$ is the 
[[smash product]] of the hom-spaces between the consecutive spheres, for instance:

$$
  \array{
    S^1 \wedge S^1 & = & StdSpheres(S^n, S^{n+1}) \wedge StdSpheres(S^{n+1}, S^{n+2})
    \\
    {}^{\mathllap{\simeq}}\downarrow 
      && 
    {}^{\mathllap{\simeq}}\downarrow^{\circ}
    \\
    S^2 & = & StdSpheres(S^n , S^{n+2})
  }
  \,,
$$

and so functoriality completely fixes the former by the latter:


=--

Further [below](#StrictModelStructureOnSequentialSpectra) we use prop. \ref{SequentialSpectraAsDiagramSpectra} to naturally induce a model  structure on the category of topological sequential spectra.

+-- {: .num_remark #TensoringOfSeqSpectraOverSpacesAsSpecialCaseOfTensoringTopologicalFunctors}
###### Remark

Under the equivalence of prop. \ref{SequentialSpectraAsDiagramSpectra}, the general concept of tensoring of [[topologically enriched functors]] over topological spaces (according to [this def.](Introduction+to+Stable+homotopy+theory+--+P#TensoringAndPoweringOfTopologicallyEnrichedCopresheaves)) restricts to the concept of tensoring of sequential spectral over topological spaces according to def. \ref{TensoringAndPoweringOfSequentialSpectra}.

=--

+-- {: .num_prop #LimitsAndColimitsOfSequentialSpectra}
###### Proposition

The category $SeqSpec(Top_{cq})$ of sequential spectra (def. \ref{SequentialSpectra}) has all [[limits]] and [[colimits]], and they are computed objectwise: 

Given

$$
  X_\bullet
    \;\colon\;
  I
    \longrightarrow
  SeqSpec(Top_{cg})
$$

a [[diagram]] of sequential spectra, then:

1. its colimiting spectrum has component spaces the colimit of the component spaces formed in $Top_{cg}$ (via [this prop.](Introduction+to+Stable+homotopy+theory+--+P#DescriptionOfLimitsAndColimitsInTop) and [this corollary](Introduction+to+Stable+homotopy+theory+--+P#kTopIsCoreflectiveSubcategory)):

   $$
     (\underset{\longrightarrow}{\lim}_i X(i))_n
     \simeq
      \underset{\longrightarrow}{\lim}_i X(i)_n
      \,,
   $$

1. its limiting spectrum has component spaces the limit of the component spaces formed in $Top_{cg}$ (via [this prop.](Introduction+to+Stable+homotopy+theory+--+P#DescriptionOfLimitsAndColimitsInTop) and [this corollary](Introduction+to+Stable+homotopy+theory+--+P#kTopIsCoreflectiveSubcategory)):

   $$
     (\underset{\longleftarrow}{\lim}_i X(i))_n
     \simeq
      \underset{\longleftarrow}{\lim}_i X(i)_n
      \,;
   $$

moreover:

1. the colimiting spectrum has structure maps in the sense of def. \ref{SequentialSpectra} given by

   $$
     S^1 \wedge (\underset{\longrightarrow}{\lim}_i X(i)_n)
     \simeq
     \underset{\longrightarrow}{\lim}_i ( S^1 \wedge X(i)_n )
     \overset{\underset{\longrightarrow}{\lim}_i \sigma_n^{X(i)}}{\longrightarrow}
     \underset{\longrightarrow}{\lim}_i X(i)_{n+1}
   $$

   where the first isomorphism exhibits that $S^1 \wedge(-)$ preserves all colimits, since it is a [[left adjoint]] by prop. \ref{SuspensionAndLoopAdjunctionInClassicalHomotopyTheory};

1. the limiting spectrum has adjunct structure maps in the sense of def. \ref{SequentialSpectrumViaAdjunctStructureMaps} given by

   $$
     \underset{\longleftarrow}{\lim}_i X(i)_n
      \overset{\underset{\longleftarrow}{\lim}_i \tilde \sigma_n^{X(i)}}{\longrightarrow}
     \underset{\longleftarrow}{\lim}_i Maps(S^1, X(i)_n)_\ast 
     \simeq
     Maps(S^1, \underset{\longleftarrow}{\lim}_i X(i)_n)_\ast
   $$

   where the last isomorphism exhibits that $Maps(S^1,-)_\ast$ preserves all limits, since it is a [[right adjoint]] by prop. \ref{SuspensionAndLoopAdjunctionInClassicalHomotopyTheory}.

=--

+-- {: .proof}
###### Proof

That the limits and colimits exist and are computed objectwise follows via prop. \ref{SequentialSpectraAsDiagramSpectra} from the general statement for categories of topological functors ([prop.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedCopresheavesHaveAllLimitsAndColimits)). But it is also immediate to directly check the [[universal property]].

=--

+-- {: .num_example #WedgeSumOfSpectra}
###### Example

The [[coproduct]] of [[spectra]] $X, Y \in SeqSpec(Top_{cg})$, called the **wedge sum of spectra** 

$$
  X \vee Y
    \coloneqq
  X \sqcup Y
$$

is componentwise the [[wedge sum]] of pointed topological spaces ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#WedgeSumAsCoproduct))

$$
  (X \vee Y)_n
  =
  X_n \vee Y_n
$$

with structure maps

$$
  \sigma_n^{X \vee Y}
    \;\colon\;
  S^1 \wedge (X \vee Y)
    \simeq
  S^1 \wedge X \,\vee\, S^1 \wedge Y
    \overset{(\sigma_n^X, \sigma_n^Y)}{\longrightarrow}
  X_{n+1} \vee Y_{n+1}
  \,.
$$


=--

+-- {: .num_example #StandardCylinderSpectrumSequential}
###### Example

For $X \in SeqSpec(Top_{cg})$ a [[sequential spectrum]], def. \ref{SequentialSpectra}, its **standard [[cylinder spectrum]]** is its [[smash product|smash]] [[tensoring]] $X \wedge (I_+)$, according to def. \ref{TensoringAndPoweringOfSequentialSpectra}, with the standard interval ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopologicalInterval)) with a basepoint freely adjoined ([def.](Introduction+to+Stable+homotopy+theory+--+P#BasePointAdjoined)). The component spaces of the [[cylinder spectrum]] are the standard [[reduced cylinders]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#StandardReducedCyclinderInTop)) of the component spaces of $X$:

$$
  (X \wedge (I_+))_n
  =
  X_n \wedge I_+
  \,.
$$

By the functoriality of the [[smash product|smash]] [[tensoring]], the factoring 

$$
  \nabla_{S^0} \;\colon\; S^0 \vee S^0 \longrightarrow I_+ \longrightarrow S^0
$$

of the [[codiagonal]] on the [[0-sphere]] through the standard interval with a base point adjoined, gives a factoring of the [[codiagonal]] of $X$ through its standard cylinder spectrum

$$
  \nabla_X
  \;\colon\;
  X \vee X 
    \overset{X \wedge (S^0 \vee S^0  \to I_+)}{\longrightarrow}
  X \wedge (I_+)
   \overset{X \wedge (I_+ \to S^0) }{\longrightarrow}
  X
$$

(where we are using that [[wedge sum]] is the [[coproduct]] in [[pointed topological spaces]] ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#WedgeSumAsCoproduct)).)

=--


##### Suspension and looping

We discuss models for the operation of [[reduced suspension]] and forming [[loop space objects]] of sequential spectra.

+-- {: .num_defn #SequentialSpectrumRealSuspension}
###### Definition

For $X$ a sequential spectrum, then

1. the **standard suspension** of $X$ is the [[smash product]]-[[tensoring]] $X \wedge S^1$ according to def. \ref{TensoringAndPoweringOfSequentialSpectra};

1. the **standard looping** of $X$ is the smash [[powering]] $Maps(S^1,X)_\ast$ according to def. \ref{TensoringAndPoweringOfSequentialSpectra}.

=--

+-- {: .num_prop #StandardSuspensionSpectrumIsCofiberOfStandardCylinderSpectrum}
###### Proposition

For $X\in SeqSpec(Top_{cg})$, the standard suspension $X \wedge S^1$ of def. \ref{SequentialSpectrumRealSuspension} is equivalently the [[cofiber]] (formed via prop. \ref{LimitsAndColimitsOfSequentialSpectra}) of the canonical inclusion of boundaries into the standard [[cylinder spectrum]]  $X \wedge (I_+)$ of example \ref{StandardCylinderSpectrumSequential}:

$$
  X \wedge S^1 
    \simeq
  cofib\left(
    X \vee X \to X \wedge (I_+)
  \right)
  \,.
$$

=--

+-- {: .proof}
###### Proof

This is immediate from the componentwise construction of the smash tensoring and the componentwise computation of colimits of spectra via prop. \ref{LimitsAndColimitsOfSequentialSpectra}.

=--

This means that once we know that $X\vee X \to X \wedge (I_+)$ is suitably a cofibration (to which we turn [below](#CWSpectra)) then the standard suspension is a homotopy-correct model for the suspension operation. However, some properties of suspension are hard to prove directly with the standard suspension model. For such there are two other models for suspension and looping of spectra. These three models are not isomorphic to each other in $SeqSpec(Top_{cg})$, but (this is lemma \ref{IsomorphismBetweenStandardAndAlternativeSuspensionInHomotopyCategory} below) they will become isomorphic in the [[stable homotopy category]] (def. \ref{TheStableHomotopyCategory}).


+-- {: .num_defn #ShiftedSpectrum}
###### Definition

For $X$ a [[sequential spectrum]] (def. \ref{SequentialSpectra}) and $k \in \mathbb{Z}$, the $k$-fold **shifted spectrum** of $X$ is the sequential spectrum denoted $X[k]$ given by

* $(X[k])_n \coloneqq \left\{ \array{X_{n+k} & for \; n+k \geq 0 \\ \ast & otherwise } \right. $;

* $\sigma_n^{X[k]} \coloneqq \left\{ \array{ \sigma^X_{n+k} & for \; n+k \geq 0 \\ 0 & otherwise} \right. $.

=--


+-- {: .num_defn #SequentialSpectrumFakeSuspension}
###### Definition

For $X$ a [[sequential spectrum]], def. \ref{SequentialSpectra}, then

1. the **alternative suspension** of $X$ is the sequential spectrum $\Sigma X$ with 

   1. $(\Sigma X)_n \coloneqq S^1 \wedge X_n$ ([[smash product]] on the left ([defn.](Introduction+to+Stable+homotopy+theory+--+P#SmashProductOfPointedObjects)))

   1. $\sigma_n^{\Sigma X} \coloneqq S^1 \wedge (\sigma^X_n)$.

   in the sense of def. \ref{SequentialSpectra};

1. the **alternative looping** of $X$ is the sequential spectrum $\Omega X$ with

   1. $(\Omega X)_n \coloneqq Maps(S^1,X_n)_\ast$;

   1. $\tilde \sigma_n^{\Omega X} \coloneqq Maps(S^1,\tilde \sigma^X_n)_\ast$

   in the sense of def. \ref{SequentialSpectrumViaAdjunctStructureMaps}.

=--

+-- {: .num_remark}
###### Remark

In various references the "alternative suspension" from def. \ref{SequentialSpectrumFakeSuspension} is called the "fake suspension"  (e.g. [Goerss-Jardine 96, p. 499](#GoerssJardine96), [Jardine 15, section 10.4](sequential+spectrum#Jardine15)).

=--

+-- {: .num_remark #StandardAndAlternativeSuspensionAreNotDirectlyComparable}
###### Remark

There is no direct comparison morphism between the standard suspension (def. \ref{SequentialSpectrumRealSuspension}) and the alternative suspension (def. \ref{SequentialSpectrumFakeSuspension}). This is due to the non-trivial graded commutativity of smash products of spheres (prop. \ref{GradedCommutativityOfSmashOfSpheres}): 

namely a comparison morphism $\Sigma X \longrightarrow X \wedge S^1$ (or alternatively the other way around) would have to make the following diagrams commute:

$$
  \array{
     S^1 \wedge S^1 \wedge X_n &\longrightarrow& S^1 \wedge X_n \wedge S^1
     \\
     {}^{\mathllap{S^1 \wedge \sigma_n}}\downarrow 
       &(nc)& 
     \downarrow^{\mathrlap{\sigma_n \wedge S^1}}
     \\
     S^1 \wedge X_{n+1} &\longrightarrow& X_{n+1} \wedge S^1
  }
$$

Clearly the only way to go about achieving this is to have the horizontal morphisms be the [[braiding]] homomorphisms of the [[smash product]]. To see this more clearly, consider labeling the two copies of the circle appearing here as $S^1_a$ and $S^1_b$. Then the diagram we are dealing with looks like this:

$$
  \array{
     S_a^1 \wedge S_b^1 \wedge X_n 
       &\longrightarrow& 
     S_a^1 \wedge X_n \wedge S_b^1
     \\
     {}^{\mathllap{S^1_a \wedge \sigma_n}}\downarrow 
       &(nc)& 
     \downarrow^{\mathrlap{\sigma_n \wedge S^1_b}}
     \\
     S_a^1 \wedge X_{n+1} &\longrightarrow& X_{n+1} \wedge S_b^1
  }
$$

If we had $S^1_a \wedge \sigma_n$ on the left and $\sigma_n \wedge S^1_a$ on the right, then the [[natural transformation|naturality]] of the [[braiding]] would give a commuting diagram. But since this is not the case, the only way to achieve this would be by exchanging in the top left

$$
  S^1_a \wedge S^1_b \longrightarrow S^1_b \wedge S^1_a
  \,.
$$

However, this map is non-trivial. It represents $-1$ in $[S^2, S^2]_\ast = \pi_2(S^2) = \mathbb{Z}$. Hence inserting this map in the top of the previous diagram still does not make it commute.

But this technical problem points to its own solutions: if we were to restrict to spectra which had structure maps only of the form $S^2 \wedge X_n \to X_{n+2}$, then the braiding required to make the two models of suspension comparable would be

$$
  S^2_a \wedge S^1_b \longrightarrow S^1_b \wedge S^2_a
$$

and this map is indeed trivial. This we turn to in def. \ref{SequentialS2Spectra} below. More generally, the kind of issue encountered here is taken care of by the concept of [[symmetric spectra]], to which we turn [further below](#SymmetricSpectra).

=--

+-- {: .num_defn #ShiftingCommutesWithLoopingAndSuspensionOfSequentialSpectra}
###### Remark

The looping and suspension operations in def. \ref{SequentialSpectrumRealSuspension} and def. \ref{SequentialSpectrumFakeSuspension} commute with shifting, def. \ref{ShiftedSpectrum}. Therefore in expressions like $\Sigma (X[1])$ etc. we may omit the parenthesis.

=--

+-- {: .num_prop #AdjunctionsBetweenLoopingAndDeloopingForSeqSpec}
###### Proposition

The constructions from def. \ref{SequentialSpectrumRealSuspension}, def. \ref{ShiftedSpectrum} and def. \ref{SequentialSpectrumFakeSuspension} form pairs of [[adjoint functors]] $SeqSpec \to SeqSpec$ like so:

1. $(-)[-1] \dashv (-)[1]$;

1. $(-)\wedge S^1 \dashv Maps(S^1,-)_\ast$;

1. $\Sigma \dashv \Omega$.

=--

+-- {: .proof}
###### Proof

Regarding the first statement: 

A morphism of the form 
$f \;\colon\; X[-1] \longrightarrow Y$ has components of the form

$$
  \array{
    \vdots && \vdots
    \\
    X_2 &\overset{f_2}{\longrightarrow}& Y_3  
    \\
    X_1 &\overset{f_2}{\longrightarrow}& Y_2
    \\
    X_0 &\overset{f_1}{\longrightarrow}& Y_1
    \\
    \ast &\overset{f_0 = 0}{\longrightarrow}& Y_0
  }
$$

and the compatibility condition with the structure maps in lowest degree is automatically satisfied

$$
  \array{
    \ast &\overset{(S^1 \wedge f_0) = 0}{\longrightarrow}& S^1 \wedge Y_0
    \\
    {}^{\mathllap{\sigma^{X[-1]}_0 = 0}}\downarrow 
      && 
    \downarrow^{\mathrlap{\sigma^Y_0}}
    \\
    X_0 &\overset{f_1}{\longrightarrow}& Y_1
  }
  \,.
$$

Therefore this is equivalent to components

$$
  \array{
    \vdots && \vdots
    \\
    X_2 &\overset{f_2}{\longrightarrow}& Y_3  
    \\
    X_1 &\overset{f_2}{\longrightarrow}& Y_2
    \\
    X_0 &\overset{f_1}{\longrightarrow}& Y_1
  }
$$

hence to a morphism $X \longrightarrow Y[1]$.




The second statement is a special case of prop. \ref{AdjunctionBetweenSmashTensoringAndPowering}.

Regarding the third statement:

This follows by applying the ([[smash product]]$\dashv$[[pointed mapping space]])-adjunction isomorphism twice, like so:

Morphisms $f\colon \Sigma X \to Y$ in the sense of def. \ref{SequentialSpectra} are in components given by commuting diagrams of this form:

$$
  \array{  
    S^1 \wedge S^1 \wedge X_{n} 
      &\overset{S^1 \wedge f_{n}}{\longrightarrow}&
    S^1 \wedge Y_{n}
    \\
    {}^{\mathllap{S^1 \wedge \sigma_n^X}}\downarrow 
     && 
    \downarrow^{\mathrlap{\sigma^Y_n}}
    \\
    S^1 \wedge X_{n+1} &\underset{f_{n+1}}{\longrightarrow}& Y_{n+1}
  }
  \,.
$$

Applying the adjunction isomorphism diagonally   gives a natural bijection to diagrams of this form:

$$
  \array{
   S^1 \wedge X_n &\overset{f_n}{\longrightarrow}& Y_n
   \\
   {}^{\mathllap{\sigma^X_n}}\downarrow && \downarrow^{\mathrlap{\tilde \sigma^Y_n}}
   \\
   X_{n+1} &\underset{\widetilde {f_{n+1}}}{\longrightarrow}& Maps(S^1,Y_{n+1})_\ast
  }
  \,.
$$

(To see this in full detail, for instance for the [[adjunct]] of the left and bottom morphism: chase the identity $id_{S^1 \wedge X_{n+1}}$ in both ways 

$$
  \array{
    Hom(S^1 \wedge X_{n+1}, S^1 \wedge X_{n+1})
      &\overset{\simeq}{\longrightarrow}&
    Hom(X_{n+1}, Maps(S^1, S^1 \wedge X_{n+1})_\ast)
    \\
    {}^{\mathllap{Hom(S^1 \wedge \sigma^X_n, f_{n+1})}}\downarrow 
    && 
    \downarrow^{\mathrlap{Hom(\sigma^X_n, Maps(S^1, f_{n+1})_\ast)}}
    \\
    Hom(S^1 \wedge S^1 \wedge X_n, Y_{n+1})
     &\overset{\simeq}{\longrightarrow}&
    Hom(S^1 \wedge X_n, Maps(S^1, Y_{n+1})_\ast)
  }
$$

through the adjunction naturality square. The other cases follow analogously.)

Then applying the adjunction isomorphism diagonally once more gives a further bijection to  commuting diagrams of this form:

$$
  \array{
    X_n &\overset{\widetilde {f_n}}{\longrightarrow}& Maps(S^1,Y_n)_\ast
    \\
    {}^{\mathllap{\tilde \sigma_n}}\downarrow 
      && 
    \downarrow^{\mathrlap{Maps(S^1,\tilde \sigma^Y_n)_\ast}}
    \\
    Maps(S^1, X_{n+1})_\ast
      &\underset{Maps(S^1,\widetilde{f_{n+1}})_\ast}{\longrightarrow}&
    Maps\left(S^1, Maps(S^1,Y_{n+1})_\ast\right)_\ast
  }
  \,.
$$

This, finally, equivalently exhibits homomorphisms of the form

$$
  X \longrightarrow \Omega Y
$$

in the sense of def. \ref{SequentialSpectrumViaAdjunctStructureMaps}.

=--


+-- {: .num_prop #StabilizationAdjunctionSquareExists}
###### Proposition

The following diagram of [[adjoint pairs]] of [[functors]] commutes:

$$
  \array{
     Top_{cg}^{\ast/}
      &
      \underoverset{\underoverset{\Omega}{\bot}{\longrightarrow}}{\overset{\Sigma}{\longleftarrow}}{} 
      &
     Top^{\ast/}_{cg}
     \\
     {}^{\mathllap{\Sigma^\infty}}\downarrow \dashv \uparrow^{\mathrlap{\Omega^\infty}}
     &&
     {}^{\mathllap{\Sigma^\infty}}\downarrow \dashv \uparrow^{\mathrlap{\Omega^\infty}}
     \\
     SeqSpec(Top_{cg})
     &
     \underoverset
       {\underset{\Omega}{\longrightarrow}}
       {\overset{\Sigma}{\longleftarrow}}
       {\bot}
     &
     SeqSpec(Top_{cg})
  }
  \,,
$$

Here the top horizontal adjunction is from prop. \ref{SuspensionAndLoopAdjunctionInClassicalHomotopyTheory}, the vertical adjunction is from prop. \ref{AdjunctionBetweenSmashTensoringAndPowering} and the bottom adjunction is from prop. \ref{AdjunctionsBetweenLoopingAndDeloopingForSeqSpec}.

=--

+-- {: .proof}
###### Proof

It is sufficient to check 

$$
  \Sigma^\infty \circ \Sigma \simeq \Sigma \circ \Sigma^\infty 
  \,.
$$

From this the statement

$$
  \Omega^\infty \circ \Omega \simeq \Omega \circ \Omega^\infty
$$

follows by uniqueness of adjoints.

So let $X \in Top_{cg}^{\ast/}$. Then 

* $(\Sigma \Sigma^\infty X)_n = S^1 \wedge S^n \wedge X$,

* $\sigma^{(\Sigma \Sigma^\infty X)}_n \colon S^1 \wedge S^1 \wedge S^n \wedge X \overset{S^1 \wedge id}{\longrightarrow} S^1 \wedge S^{1+n} \wedge X$,

while

* $(\Sigma^\infty \Sigma X)_n = S^n \wedge S^1 \wedge X$,


* $\sigma_n^{(\Sigma^\infty \Sigma X)}\colon S^1\wedge S^n \wedge S^1 \wedge X \overset{id \wedge S^1 \wedge X}{\longrightarrow} S^{1+n} \wedge S^1 \wedge X$,

where we write "id" for the canonical isomorphism. Clearly there is a natural isomorphism given by the canonical identifications

$$
  S^1 \wedge S^n \wedge X
    \overset{\simeq}{\longrightarrow}
  (S^1)^{\wedge^{n+1}}\wedge X
     \overset{\simeq}{\longrightarrow}
  S^n \wedge S^1 \wedge X
  \,.
$$

(As long as we are not smash-permuting the $S^1$ factor with the $S^n$ factor -- and here we are not -- then the fact that they get mixed under this isomorphism is irrelevant. The point where this does become relevant is the content of remark \ref{StandardAndAlternativeSuspensionAreNotDirectlyComparable} below.)

=--



#### The strict model structure on sequential spectra
 {#StrictModelStructureOnSequentialSpectra}

The [[model category]] structure on [[sequential spectra]] which [[presentable (infinity,1)-category|presents]] [[stable homotopy theory]] is the "stable model structure" discussed [below](#TheStableModelStructure). Its fibrant-cofibrant objects are (in particular) [[Omega-spectra]], hence are the proper [[spectrum objects]] among the pre-spectrum objects.

But for technical purposes it is useful to also be able to speak of a model structure on pre-spectra, which sees their homotopy theory as sequences of simplicial sets equipped with suspension maps, but not their stable structure. This is called the "strict model structure" for sequential spectra. Its main point is that the stable model structure of interest arises from it via [[Bousfield localization of model categories|left Bousfield localization]].


+-- {: .num_defn #ClassesOfMorphismsOfTheStrictModelStructureOnSequentialSpectra}
###### Definition

Say that a homomorphism $f_\bullet \colon X_\bullet \to Y_\bullet$ in the category $SeqSpec(Top)$, def. \ref{SequentialSpectra} is

* a **strict weak equivalence** if each component $f_n \colon X_n \to Y_n$ is a weak equivalence in the [[classical model structure on topological spaces]] (hence a [[weak homotopy equivalence]]);

* a **strict fibration** if each component $f_n \colon X_n \to Y_n$ is a fibration in the [[classical model structure on topological spaces]] (hence a [[Serre fibration]]);

* a **strict cofibration** if the maps $f_0\colon X_0 \to Y_0$ as well as for all $n \in \mathbb{N}$ the maps

  $$
    (f_{n+1}, \sigma^Y_n)
      \;\colon\;
    X_{n+1}\underset{S^1 \wedge X_n}{\sqcup} S^1 \wedge Y_n
      \longrightarrow
    Y_{n+1}
  $$

  are cofibrations in the [[classical model structure on topological spaces]] (hence [[retracts]] of [[relative cell complexes]]);

We write $W_{strict}$, $Fib_{strict}$ and $Cof_{strict}$ for these classes of morphisms, respectively.

=--

Recall the sets

$$
  I_{Top^{\ast/}} \coloneqq \{S^{n-1}_+ \overset{(\iota_n)_+}{\longrightarrow} D^n_+\}_{n \in \mathbb{N}}
$$

$$
  J_{Top^{\ast/}} \coloneqq \{D^n \overset{(j_n)_+}{\longrightarrow} D^n \times I\}_{n \in \mathbb{N}}
$$

of standard generating (acyclic) cofibrations ([def.](Introduction+to+Stable+homotopy+theory+--+P#GeneratingCofibrationsForPointedTopologicalSpaces)) of the [[classical model structure on pointed topological spaces]] ([thm.](Introduction+to+Stable+homotopy+theory+--+P#CofibrantGenerationOfPointedTopologicalSpaces)).


+-- {: .num_defn #GeneratingAndGeneratingAcyclicCofibrationsForSeqSpecStrict}
###### Definition

Write

$$
  I_{SeqSpec}^{strict} 
    \coloneqq 
  \left\{ 
    y(S^n) \cdot i_+ 
  \right\}_{{S^n \in StdSpheres,} \atop {i_+ \in I_{Top^{\ast/}}}}
  \;\;
  \in [StdSpheres, Top^{\ast/}] \simeq SeqSpec(Top)
$$

and

$$
  J_{SeqSpec}^{strict}
    \coloneqq 
  \left\{ 
    y(S^n) \cdot j_+ 
  \right\}_{{ S^n \in StdSpheres} \atop {j_+ \in J_{Top^{\ast/}}}}
  \;\;
  \in [StdSpheres, Top^{\ast/}] \simeq SeqSpec(Top)
  \,,
$$

for the set of morphisms arising as the [[tensoring]] (remark \ref{TensoringOfSeqSpectraOverSpacesAsSpecialCaseOfTensoringTopologicalFunctors}) of a [[representable functor|representable]] ([exmpl.](#Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctorsToTopk)) with a generating acyclic cofibration of the [[classical model structure on pointed topological spaces]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#GeneratingCofibrationsForPointedTopologicalSpaces)).

=--



+-- {: .num_theorem #StrictModelStructureOnSequentialPrespectraIsModelCategory}
###### Theorem

The classes of morphisms in def. \ref{ClassesOfMorphismsOfTheStrictModelStructureOnSequentialSpectra} give the structure of a [[model category]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#ModelCategory)) to be denoted $SeqSpec(Top)_{strict}$ and called the **strict [[model structure on topological sequential spectra]]** (or: **level model structure**).

Moreover, this is a [[cofibrantly generated model category]] with generating (acyclic) cofibrations the set $I_{SeqSpec}^{strict}$ (resp. $J_{SeqSpec}^{strict}$) from def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForSeqSpecStrict}.

=--



+-- {: .proof}
###### Proof

Prop. \ref{SequentialSpectraAsDiagramSpectra} says that the category of sequential spectra is [[equivalence of categories|equivalently]] an  [[enriched functor category]]

$$
  SeqSpec(Top)
  \simeq
  [StdSpheres,\; Top_{cg}^{\ast/}]
  \,.
$$

Accordingly, this carries the [[projective model structure on enriched functors]] ([thm.](Introduction+to+Stable+homotopy+theory+--+P#ProjectiveModelStructureOnTopologicalFunctors)). This immediately gives the statement for the fibrations and the weak equivalences.

It only remains to check that the cofibrations are as claimed. To that end, consider a [[commuting square]] of sequential spectra

$$
  \array{
    X &\stackrel{h}{\longrightarrow}& A
    \\
    \downarrow^{\mathrlap{f}} && \downarrow
    \\
    Y &\longrightarrow& B
  }
  \,.
$$

By definition, this is equivalently an $\mathbb{N}$-collection of commuting diagrams in $Top_{cg}$ of the form

$$
  \array{
    X_n &\stackrel{h_n}{\longrightarrow}& A_n
    \\
    \downarrow^{\mathrlap{f_n}} && \downarrow
    \\
    Y_n &\longrightarrow& B_n
  }
$$

such that all structure maps are respected.

$$
  \array{
    S^1 \wedge X_n &\stackrel{\sigma_n^X}{\longrightarrow}& X_{n+1}
    \\
    \downarrow^{\mathrlap{S^1 \wedge f_n}} && \downarrow^{\mathrlap{f_{n+1}}}
    \\
    S^1 \wedge Y_n &\stackrel{\sigma_n^Y}{\longrightarrow}& Y_{n+1}
    \\
    & \searrow && \searrow
    \\
    && S^1 \wedge B_n &\stackrel{\sigma_n^B}{\longrightarrow}& B_{n+1}
  }
  \;\;\;
  =
  \;\;\;
  \array{
    S^1 \wedge X_n &\stackrel{\sigma_n^X}{\longrightarrow}& X_{n+1}
    \\
    & \searrow^{\mathrlap{S^1 \wedge h_n}} && \searrow^{\mathrlap{h_{n+1}}}
    \\
    && S^1 \wedge A_n &\stackrel{\sigma_n^A}{\longrightarrow}& A_{n+1}
    \\
    && \downarrow && \downarrow
    \\
    && S^1 \wedge B_n &\stackrel{\sigma_n^B}{\longrightarrow}& B_{n+1}
  }
  \,.
$$

Hence a [[lifting]] in the original diagram is a lifting in each degree $n$, such that the lifting in degree $n+1$ makes these diagrams of structure maps commute.

Since components are parameterized over $\mathbb{N}$, this condition has solutions by [[induction]]:

First of all there must be an ordinary lifting in degree 0. Since the strict fibrations are degreewise classical fibrations, this gives the condition that for $f_\bullet$ to be a strict cofibration, then $f_0$ is to be a classical cofibration.

Then assume that a lifting $l_n$ in degree $n$ has been found

$$
  \array{
    X_n &\stackrel{h_n}{\longrightarrow}& A_n
    \\
    \downarrow^{\mathrlap{f_n}} &\nearrow_{\mathrlap{l_n}}& \downarrow
    \\
    Y_n &\longrightarrow& B_n
  }
  \,.
$$

Now the lifting $l_{n+1}$ in the next degree has to also make the following diagram commute

$$
  \array{
    S^1 \wedge X_n &\stackrel{\sigma_n^X}{\longrightarrow}& X_{n+1}
    \\
    \downarrow^{\mathrlap{S^1 \wedge f_n}} && \downarrow^{\mathrlap{f_{n+1}}}
    & \searrow^{\mathrlap{h_{n+1}}}
    \\
    S^1 \wedge Y_n &\stackrel{\sigma_n^Y}{\longrightarrow}& Y_{n+1}
    && 
    \\
    & \searrow^{\mathrlap{S^1 \wedge l_n}} && \searrow^{\mathrlap{l_{n+1}}} & \downarrow
    \\
    && S^1 \wedge A_n &\stackrel{\sigma_n^A}{\longrightarrow}& A_{n+1}
  }
  \,.
$$

This is a [[cocone]] under the commuting square for the structure maps, and therefore the outer diagram is equivalently a morphism out of the [[domain]] of the [[pushout product]] $f_n \Box \sigma_n^X$ ([def.](Introduction+to+Stable+homotopy+theory+--+P#PushoutProduct)), while the compatible lift $l_{n+1}$ is equivalently a lift against this [[pushout product]]:

$$
  \array{
    S^1 \wedge Y_n 
      \underset{S^1 \wedge X_n}{\sqcup} 
    X_{n+1}
      &\stackrel{(\sigma_n^A \circ S^1 \wedge l_n,\;h_{n+1})}{\longrightarrow}&
    A_{n+1}
    \\
    {}^{\mathllap{f_n \Box \sigma^X_n}}\downarrow 
      &{}^{\mathllap{l_{n+1}}}\nearrow& 
    \downarrow
    \\
    Y_{n+1} &\stackrel{}{\longrightarrow}& B_{n+1}
  }
  \,.
$$

This shows that $f_\bullet$ is a strict cofibration precisely if, in addition to $f_0$ being a classical cofibration, all these pushout products are classical cofibrations.

=--

##### Suspension and looping

+-- {: .num_prop #SigmaInfinityIsQuillenOnStrictModelStructureOnSequential}
###### Proposition

The $(\Sigma^\infty \dashv \Omega^\infty)$-adjunction from prop. \ref{SigmaInfinityOmegaInfinity} is a [[Quillen adjunction]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#QuillenAdjunction)) between the [[classical model structure on pointed topological spaces]] ([thm.](Introduction+to+Stable+homotopy+theory+--+P#ClassicalModelStructureOnCompactlyGeneratedTopologicalSpaces), [prop.](Introduction+to+Stable+homotopy+theory+--+P#ModelStructureOnSliceCategory)) and the strict [[model structure on topological sequential spectra]] of theorem \ref{StrictModelStructureOnSequentialPrespectraIsModelCategory}:

$$
  (\Sigma^\infty \dashv \Omega^\infty)
  \;\colon\;
  SeqSpec(Top_{cg})_{strict}
    \underoverset
      {\underset{\Omega^{\infty}}{\longrightarrow}}
      {\overset{\Sigma^\infty}{\longleftarrow}}
      {\bot}
  (Top_{cg}^{\ast/})_{Quillen}
  \,.
$$


=--

+-- {: .proof}
###### Proof

Let $f \colon X\longrightarrow Y$ be a morphism in $Top^{\ast/}_{cg}$ and 

$$
  \Sigma^\infty f \colon \Sigma^\infty X \longrightarrow \Sigma^\infty Y
$$

its image.

Since the structure maps in a [[suspension spectrum]], example \ref{SuspensionSpectrum}, are all isomorphisms, we have for all $n \in \mathbb{N}$ an isomorphism

$$
  (\Sigma^\infty X)_{n+1}
    \underset{S^1 \wedge (\Sigma^\infty X)_n}{\coprod} 
   S^1 \wedge (\Sigma^\infty Y)_n
    \simeq 
  S^1 \wedge (\Sigma^\infty Y)_n
  \,.
$$

Therefore $\Sigma^\infty f$ is a strict cofibration, according to def. \ref{ClassesOfMorphismsOfTheStrictModelStructureOnSequentialSpectra}, precisely if $(\Sigma^\infty f)_0 = f$ is a classical cofibration and all the structure maps of $\Sigma^\infty Y$ are classical cofibrations. But the latter are even isomorphisms, so that this is no extra condition ([prop.](Introduction+to+Stable+homotopy+theory+--+P#ClosurePropertiesOfInjectiveAndProjectiveMorphisms)). Hence $\Sigma^\infty$ sends classical cofibrations of spaces to strict cofibrations of sequential spectra.

Furthermore, since $S^n \wedge (-) \colon (Top_{cg}^{\ast/})_{Quillen} \to (Top_{cg}^{\ast/})_{Quillen}$ is a left Quillen functor for all $n \in \mathbb{N}$ by prop. \ref{SuspensionAndLoopAdjunctionInClassicalHomotopyTheory} it sends classical acyclic cofibrations to classical acyclic cofibrations. Hence $\Sigma^\infty$, which is degreewise given by $S^n \wedge(-)$, sends classical acyclic cofibrations to degreewise acyclic cofibrations, hence in particular to degreewise weak equivalences, hence to weak equivalences in the strict model structure on sequential spectra.

This shows that $\Sigma^\infty$ is a left Quillen functor.

=--

+-- {: .num_prop #AlternativeSuspensionIsLeftQuillenOnStrictModelStructureOnSequential}
###### Proposition

The $(\Sigma \dashv \Omega)$-[[adjunction]] from prop. \ref{AdjunctionsBetweenLoopingAndDeloopingForSeqSpec} is a [[Quillen adjunction]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#QuillenAdjunction)) with respect to the strict model structure on sequential spectra of theorem \ref{StrictModelStructureOnSequentialPrespectraIsModelCategory}.

$$
   SeqSpec(Top_{cg})_{strict}  
     \underoverset
       {\underset{\Omega}{\longrightarrow}}
       {\overset{\Sigma}{\longleftarrow}}
       {\bot}
   SeqSpec(Top_{cg})_{strict}   
  \,.
$$

=--

+-- {: .proof}
###### Proof

Since the (acyclic) fibrations of $SeqSpec(Top_{cg})_{strict}$ are by definition those morphisms that are degreewise (acylic) fibrations in $(Top^{\ast/}_{cg})_{Quillen}$, the statement follows immediately from the fact that the right adjoint $\Omega$ is degreewise given by $Maps(S^1, -)_\ast \colon (Top^{\ast/}_{cg})_{Quillen} \to (Top^{\ast/}_{cg})_{Quillen}$, which is a right Quillen functor by prop. \ref{SuspensionAndLoopAdjunctionInClassicalHomotopyTheory}.

=--

In summary, prop. \ref{StabilizationAdjunctionSquareExists}, prop. \ref{SigmaInfinityIsQuillenOnStrictModelStructureOnSequential} and prop.  \ref{AlternativeSuspensionIsLeftQuillenOnStrictModelStructureOnSequential} say that 

+-- {: .num_cor #SuspensionLoopingAdjunctionSystemForStrictModelStructure}
###### Corollary


The commuting square of adjunctions in prop. \ref{StabilizationAdjunctionSquareExists} is a square of [[Quillen adjunctions]] with respect to the [[classical model structure on pointed topological spaces|classical model structure]] on pointed compactly generated topological spaces ([thm.](Introduction+to+Stable+homotopy+theory+--+P#ClassicalModelStructureOnCompactlyGeneratedTopologicalSpaces), [prop.](Introduction+to+Stable+homotopy+theory+--+P#ModelStructureOnSliceCategory)) and the strict [[model structure on topological sequential spectra]] of theorem \ref{StrictModelStructureOnSequentialPrespectraIsModelCategory}:

$$
  \array{
     (Top_{cg}^{\ast/})_{Quillen}
      &
      \underoverset{\underoverset{\Omega}{\bot}{\longrightarrow}}{\overset{\Sigma}{\longleftarrow}}{} 
      &
     (Top^{\ast/}_{cg})_{Quillen}
     \\
     {}^{\mathllap{\Sigma^\infty}}\downarrow \dashv \uparrow^{\mathrlap{\Omega^\infty}}
     &&
     {}^{\mathllap{\Sigma^\infty}}\downarrow \dashv \uparrow^{\mathrlap{\Omega^\infty}}
     \\
     SeqSpec(Top_{cg})_{strict}
     &
     \underoverset
       {\underset{\Omega}{\longrightarrow}}
       {\overset{\Sigma}{\longleftarrow}}
       {\bot}
     &
     SeqSpec(Top_{cg})_{strict}
  }
  \,,
$$


=--

Further [below](#StableModelStructureOnSequentialSpectra) we pass to the stable model structure in order to make the bottom adjunction in this diagram become a [[Quillen equivalence]]. This stable model structure will have more weak equivalences than the strict model structure, but will have the same cofibrations. Therefore we first consider now cofibrancy conditions already in the strict model structure. 

##### CW-spectra
 {#CWSpectra}

+-- {: .num_defn #CWSpectrum}
###### Definition

A **[[CW-spectrum]]** is a [[sequential spectrum]] $X_\bullet\in SeqSpec(Top_{cg})$, def. \ref{SequentialSpectra}, such that

1. all component spaces $X_n$ are [[CW-complexes]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopologicalCellComplex)), 

1. all structure maps $\Sigma X_n \longrightarrow X_{n+1}$ are inclusions of subcomplexes 

=--

+-- {: .num_prop #ClosureOfCWSpectra}
###### Proposition

The class of CW-spectra is closed under the following operations:

* finite [[wedge sum]] (def. \ref{WedgeSumOfSpectra})

* ...

=--



+-- {: .num_prop #CellSpectraAreCofibrantInModelStructureOnTopologicalSequentialSpectra}
###### Proposition

A [[sequential spectrum]] $X \in SeqSpec(Top_{cg})$ is cofibrant in the strict model structure $SeqSpec(Top_{cg})_{strict}$ of theorem \ref{StrictModelStructureOnSequentialPrespectraIsModelCategory} in particular if all component spaces are [[cell complexes]] and all its structure morphisms $S^1 \wedge X_n \to X_{n+1}$ are [[relative cell complexes]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopologicalCellComplex)). In particular [[CW-spectra]], def. \ref{CWSpectrum}, are cofibrant in $SeqSpec(Top)_{strict}$.

=--

+-- {: .proof}
###### Proof

A morphism $\ast \to X$ is a cofibration according to def. \ref{ClassesOfMorphismsOfTheStrictModelStructureOnSequentialSpectra} if 

1. The object $X_0$ is a classical cofibrant, hence a retract of a [[cell complex]];

1. The morphisms

   $$
     \ast_{n+1}\underset{S^1 \wedge \ast_n}{\sqcup} S^1 \wedge X_n
     \longrightarrow
     X_{n+1}
   $$

   are classical cofibrations. But in this case the [[pushout]] reduces to just its second summand, and so this is now equivalent to

   $$
     S^1 \wedge X_n \longrightarrow X_{n+1}
   $$

   being classical cofibrations; hence [[retracts]] of [[relative cell complexes]].

=--

+-- {: .num_prop #CylinderSpectrumOverCWSpectrumIsGood}
###### Proposition

For $X\in SeqSpec(Top)_{stable}$ a [[CW-spectrum]], def. \ref{CWSpectrum}, then its standard [[cylinder spectrum]] $X \wedge (I_+)$ of def. \ref{StandardCylinderSpectrumSequential} satisfies the conditions on an abstract [[cylinder object]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#PathAndCylinderObjectsInAModelCategory)) in that the inclusion

$$
  X \vee X \longrightarrow X \wedge (I_+)
$$

(of the [[wedge sum]] of $X$ with itself, example \ref{WedgeSumOfSpectra}) is a cofibration in $SeqSpec(Top)_{stable}$.

=--

+-- {: .proof}
###### Proof

According to def. \ref{ClassesOfMorphismsOfTheStrictModelStructureOnSequentialSpectra} we need to check that for all $n$ the morphism

$$
  (X \vee X)_{n+1}
  \underset{S^1 \wedge (X\vee X)_n}{\sqcup}
  S^1 \wedge (X \wedge (I_+))_n
  \longrightarrow
  (X \wedge (I_+))_{n+1}
$$

is a retract of a relative cell complex. After distributing indices and smash products over wedge sums, this is equivalently

$$
  (X_{n+1} \vee X_{n+1})
  \underset{(S^1 \wedge X_n )\vee (S^1 \wedge X_n))}{\sqcup}
   S^1 \wedge X_n \wedge (I_+)
  \longrightarrow
  X_{n+1} \wedge (I_+)
  \,.
$$

Now by the assumption that $X$ is a [[CW-spectrum]], each $X_{n}$ is a CW-complex, and this implies that $X_n \wedge (I_+)$ is a relative cell complex in $Top^{\ast/}$. With this, inspection shows that also the above morphism is a relative cell complex.

=--

We now turn to discussion of [[CW-approximation]] of sequential spectra. First recall the relative version of CW-approximation for topological spaces.

For the following, recall that a [[continuous function]] $f \colon X \to Y$ between [[topological spaces]] is called an **[[n-connected map]]** if the unduced morphism on [[homotopy groups]] $\pi_\bullet(f)\colon \pi_\bullet(X,x) \to \pi_\bullet(Y,f(x))$ is

1. an [[isomorphism]] in degree $\lt n$;

1. an [[epimorphism]] in degree $n$.

(Hence an [[weak homotopy equivalence]] is an "$\infty$-connected map".)

+-- {: .num_lemma #nConnectedCWApproximationOfContinuousFunction}
###### Lemma

Let $f \;\colon\; A \longrightarrow X$ be a [[continuous function]] between [[topological spaces]]. Then there exists for each $n \in \mathbb{N}$ a [[relative CW-complex]] $\hat f \colon A \hookrightarrow \hat Y$ together with an [[extension]] $\phi \colon Y \to X$, i.e.

$$
  \array{
    A &\overset{f}{\longrightarrow}& X
    \\
    {}^{\mathllap{\hat f}}\downarrow & \nearrow_{\mathrlap{\phi}}
    \\
    \hat X
  }
$$ 

such that $\phi$ is [[n-connected continuous function|n-connected]].

Moreover:

* if $f$ itself is [[n-connected continuous function|k-connected]], then the relative CW-complex $\hat f$ may be chosen to have cells only of [[dimension]] $k + 1 \leq dim \leq n$.

* if $A$ is already a [[CW-complex]], then $\hat f \colon A \to X$ may be chosen to be a subcomplex inclusion.

=--

([tomDieck 08, theorem 8.6.1](CW+approximation#tomDieck08))

+-- {: .num_prop #CWApproximationForContinuousFunctions}
###### Proposition

For every [[continuous function]] $f \colon A \longrightarrow X$ out of a [[CW-complex]] $A$, there exists a [[relative CW-complex]] $\hat f \colon A \longrightarrow \hat X$ that factors $f$ followed by a [[weak homotopy equivalence]] 

$$
  \array{   
     A && \overset{f}{\longrightarrow} && X
     \\
     & {}_{\mathllap{\hat f}}\searrow && \nearrow_{\mathrlap{{\phi} \atop {\in WHE}}}
     \\
     && \hat X
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

Apply lemma \ref{nConnectedCWApproximationOfContinuousFunction} iteratively for $n \in \mathbb{N}$ to produce a sequence with [[cocone]] of the form

$$
  \array{
    A &\overset{f_0}{\longrightarrow}& X_0 &\overset{f_2}{\longrightarrow}& X_1 &\longrightarrow & \cdots
    \\
    &{}_{\mathllap{f}}\searrow & \downarrow^{\mathrlap{\phi_0}} & \swarrow_{\mathrlap{\phi_1}} & \cdots 
    \\
    && X
  }
  \,,
$$

where each $f_n$ is a [[relative CW-complex]] adding cells exactly of dimension $n$, and where $\phi_n$ in [[n-connected continuous function|n-connected]]. 

Let then $\hat X$ be the [[colimit]] over the sequence (its [[transfinite composition]]) and $\hat f \colon A \to X$ the induced component map. By definition of relative CW-complexes, this $\hat f$ is itself a relative CW-complex.

By the [[universal property]] of the colimit this factors $f$ as

$$
  \array{
    A &\overset{f_0}{\longrightarrow}& X_0 &\overset{f_1}{\longrightarrow}& X_1 &\longrightarrow & \cdots
    \\
    &{}_{\mathllap{}}\searrow & \downarrow^{\mathrlap{}} & \swarrow_{\mathrlap{}} & \cdots 
    \\
    && \hat X
    \\
    && \downarrow^{\mathrlap{\phi}}
    \\
    && X
  }
  \,.
$$

Finally to see that $\phi$ is a weak homotopy equivalence: since [[n-spheres]] are [[compact topological spaces]], then every map $\alpha \colon S^n \to \hat X$ factors through a finite stage $i \in \mathbb{N}$ as $S^n \to X_i \to  \hat X$ (by [this lemma](Introduction+to+Stable+homotopy+theory+--+P#CompactSubsetsAreSmallInCellComplexes)). By possibly including further into higher stages, we may choose $i \gt n$.  But then the above says that further mapping along $\hat X \to X$ is the same as mapping along $\phi_i$, which is $(i \gt n)$-connected and hence an isomorphism on the homotopy class of $\alpha$.

=--

+-- {: .num_prop #CWApproximationForSequentialSpectra}
###### Proposition

For $X$ any topological [[sequential spectrum]] (def.\ref{SequentialSpectra}), then there exists a [[CW-spectrum]] $\hat X$ (def. \ref{CWSpectrum}) and a homomorphism 

$$
  \phi \;\colon\;  \hat X \overset{\in W_{strict}}{\longrightarrow} X
  \,.
$$ 

which is degreewise a [[weak homotopy equivalence]], hence a weak equivalence in the strict model structure of theorem \ref{StrictModelStructureOnSequentialPrespectraIsModelCategory}.

=--

+-- {: .proof}
###### Proof

First let $\hat X_0 \longrightarrow X_0$ be a CW-approximation of the component space in degree 0, via prop. \ref{CWApproximationForContinuousFunctions}. Then proceed by [[induction]]: suppose that for $n \in \mathbb{N}$ a [[CW-approximation]] $\phi_{k \leq n} \colon  \hat X_{k \leq n} \to X_{k \leq n}$ has been found such that all the structure maps are respected. Consider then the continuous function

$$
  S^1 \wedge \hat X_n 
    \overset{S^1 \wedge \phi_n}{\longrightarrow} 
  S^1 \wedge X_n 
    \overset{\sigma_n}{\longrightarrow} 
  X_{n+1}
  \,.
$$

Applying prop. \ref{CWApproximationForContinuousFunctions} to this function factors it as

$$
  S^1 \wedge \hat X_n 
    \hookrightarrow 
  \hat X_{n+1} 
    \overset{\phi_{n+1}}{\longrightarrow} 
  X_{n+1}
  \,.
$$

Hence we have obtained the next stage of the CW-approximation. The respect for the structure maps is just this factorization property:

$$
  \array{  
    S^1 \wedge \hat X_n 
      &\overset{S^1 \wedge \phi_n}{\longrightarrow}& 
    S^1 \wedge X_n
    \\
    {}^{incl}\downarrow && \downarrow^{\mathrlap{\sigma_n}}
    \\
    \hat X_{n+1} &\underset{\phi_{n+1}}{\longrightarrow}& X_{n+1}
  }
  \,.
$$

=--

##### Topological enrichment

We discuss here how the [[hom-set]] of homomorphisms between any two sequential spectra is naturally equipped with a topology, and how these _[[hom-spaces]]_ interact well with the strict model structure on sequential spectra from theorem \ref{StrictModelStructureOnSequentialPrespectraIsModelCategory}. This is in direct analogy to the compatibility of compactly generated [[mapping spaces]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#CompactlyGeneratedMappingSpaces)) with the [[classical model structure on topological spaces|classical model structure on compactly generated topological spaces]] discussed at _[Classical homotopy theory -- Topological enrichment](Introduction+to+Stable+homotopy+theory+--+P#TopologicalEnrichment)_. It gives an improved handle on the analysis of morphisms of spectra below in [the proof of the stable model structure](#ProofOfTheStableModelStructureOnSequentialSpectra) and it paves the way to the discussion of fully fledge _[[mapping spectra]]_ below in _[1.2](#DiagramSpectra)_. There we will give a fully general account of the principles underlying the following. Here we just consider a pragmatic minimum that allows us to proceed.




+-- {: .num_defn #HomSpaceBetweenSequentialSpectra}
###### Definition

For $X, Y \in SeqSpec(Top_{cg})$ two [[sequential spectra]] (def. \ref{SequentialSpectra}) let 

$$
  SeqSpec(X,Y) \in Top_{cg}^{\ast/}
$$

be the [[pointed topological space]] whose underlying set is the [[hom-set]] $Hom_{SeqSpec(Top_{cg})}(X,Y)$ of homomorphisms from $X$ to $Y$, and which is equipped with the [[final topology]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#InitialAndFinalTopologies)) generated by those functions

$$
  \phi 
    \;\colon\;
  K \longrightarrow Hom_{SeqSpec(Top_{cg})}(X,Y)
$$

out of [[compact topological space|compact]] [[Hausdorff spaces]] $K$, for which there exists a homomorphism of spectra

$$
  \tilde \phi 
    \;\colon\;
  X\wedge K
    \longrightarrow
  Y
$$

out of the smash tensoring of $X$ with $K$ (def. \ref{TensoringAndPoweringOfSequentialSpectra}) such that for all $y \in K$, $n \in \mathbb{N}$, $x \in X_n$

$$
  \phi(y)_n(x) = \tilde \phi_n(x,y)
  \,.
$$

By construction this makes $SeqSpec(X,Y)$ indeed into a [[compactly generated topological space]], and it gives a [[natural bijection]]

$$
  Hom_{Top^{\ast/}_{cg}}(K,\, SeqSpec(X,Y))
    \;\simeq\;
  Hom_{SeqSpec(Top^{\ast/}_{cg})}( X \wedge K ,\, Y )
  \,.
$$

=--


In _[[Introduction to Stable homotopy theory -- P|Prelude -- Classical homotopy theory]]_ we discussed, in the section _[Topological enrichment](Introduction+to+Stable+homotopy+theory+--+P#TopologicalEnrichment)_, that the [[classical model structure on topological spaces]] (when restricted to [[compactly generated topological spaces]]) interacts well with forming [[smash products]] and pointed [[mapping spaces]]. Concretely, the smash [[pushout product]] of two classical cofibrations is a classical cofibration, and is acyclic if either of the factors is:

$$
  Cof_{cl} \Box Cof_{cl} \subset Cof_{cl}
  \;\,,
  \;\;\;\;\;\;\;
  (Cof_{cl} \cap W_{cl}) \Box Cof_{cl} \subset Cof_{cl} \cap W_{cl}
  \,.
$$

We saw that. by [[Joyal-Tierney calculus]] ([prop.](Introduction+to+Stable+homotopy+theory+--+P#JoyalTierneyCalculus)), this is equivalent to the _pullback powering_ satisfying the dual relations

$$
  Fib_{cl}^{\Box Cof_{cl}}
  \subset 
  Fib_{cl} 
  \;\,,
  \;\:\;\;
  Fib_{cl}^{\Box (Cof_{cl} \cap W_{cl})}
  \subset 
  Fib_{cl} \cap W_{cl}
  \;\,,
  \;\;\;
  (Fib_{cl} \cap W_{cl})^{\Box Cof_{cl}}
  \subset
  Fib_{cl} \cap W_{cl}  
  \,.
$$ 

Now that we passed from spaces to spectra, def. \ref{TensoringAndPoweringOfSequentialSpectra} generalizes the smash product of spaces to the smash tensoring of sequential spectra by spaces, and the pointed mapping space of spaces to the powering of a space into a sequential spectrum. Accordingly there is now the analogous concept of _[[pushout product]]_ with respect to smash tensoring, and of _pullback powering_ with respect to smash powering. 

From the way things are presented, it is immediate that these operations on spectra satisfy the analogous compatibility condition with the strict model structure on spectra from theorem \ref{StrictModelStructureOnSequentialPrespectraIsModelCategory}, in fact this follows generally for topologically enriched functor categories and is inherited via prop. \ref{SequentialSpectraAsDiagramSpectra}. But since this will be important for some of the discussion to follow, we here make it explicit:


+-- {: .num_defn #PushoutProductWithRespectToSmashTensoring}
###### Definition

Let $f \;\colon \; X \to Y$ be a morphism in $SeqSpec(Top_{cg})$ (def. \ref{SequentialSpectra}) and let $i \;\colon\; A \to B$ a morpism in $Top_{cg}^{\ast/}$. 

Their **[[pushout product]] with respect to smash tensoring** is the universal morphism 

$$
  f \Box i
  \coloneqq
  \left((id,i), (f,id)\right)
$$

in

$$
  \array{
    && X \wedge A
    \\
    & {}^{\mathllap{(f,id)}}\swarrow && \searrow^{\mathrlap{(id,i)}}
    \\
    Y \wedge A && (po) && X \wedge B
    \\
    & {}_{\mathllap{}}\searrow && \swarrow
    \\
    && (Y \wedge A) \underset{X \wedge A}{\sqcup} (X \wedge B)
    \\
    && \downarrow^{\mathrlap{((id, i), (f,id))}}
    \\
    && Y \wedge B
  }
  \,,
$$

where $(-)\wedge(-)$ denotes the smash tensoring from def. \ref{TensoringAndPoweringOfSequentialSpectra}.

Dually, their **pullback powering** is the universal morphism

$$
  f^{\Box i}
  \coloneqq
  (Maps(B,f)_\ast, Maps(i,X)_\ast)
$$

in

$$
  \array{
    && Maps(B,X)_\ast
    \\
    && \downarrow^{\mathrlap{(Maps(B,f)_\ast, Maps(i,X)_\ast)}}
    \\
    && Maps(B,Y)_\ast \underset{Maps(A,Y)_\ast}{\times} Maps(A,X)_\ast
    \\
    & \swarrow && \searrow
    \\
    Maps(B,Y)_\ast && (pb) && Maps(A,X)_\ast
    \\
    & {}_{\mathllap{Maps(i,Y)_\ast}}\searrow 
      && 
    \swarrow_{\mathrlap{Maps(A,p)_\ast}}
    \\
    && Maps(A,Y)_\ast
  }
  \,,
$$

where $Maps(-,-)_\ast$ denotes the smash powering from def. \ref{TensoringAndPoweringOfSequentialSpectra}.

Similarly, for $f \colon X \to Y$ and $i \colon A \to B$ both morphisms of sequential spectra, then their pullback powering is the universal morphism 

$$
  f^{\Box i} \coloneqq (SeqSpec(B,f), SeqSpec(i,X))
$$

in 

$$
  \array{
    && SeqSpec(B,X)_\ast
    \\
    && \downarrow^{\mathrlap{(SeqSpec(B,f)_\ast, SeqSpec(i,X)_\ast)}}
    \\
    && SeqSpec(B,Y)_\ast \underset{SeqSpec(A,Y)_\ast}{\times} SeqSpec(A,X)_\ast
    \\
    & \swarrow && \searrow
    \\
    SeqSpec(B,Y)_\ast && (pb) && SeqSpec(A,X)_\ast
    \\
    & {}_{\mathllap{SeqSpec(i,Y)_\ast}}\searrow 
      && 
    \swarrow_{\mathrlap{SeqSpec(A,p)_\ast}}
    \\
    && SeqSpec(A,Y)_\ast
  }
  \,,
$$

where now $SeqSpec(-,-)$ is the [[hom-space]] functor from def. \ref{HomSpaceBetweenSequentialSpectra}.

=--

+-- {: .num_prop #PushoutProductWithRespectToSmashTensoringSatisfiesEnrichedModelCategoryAxioms}
###### Proposition

The operation of forming pushout products with respect to smash tensoring in def. \ref{PushoutProductWithRespectToSmashTensoring} is compatible with the strict model structure on sequential spectra from theorem \ref{StrictModelStructureOnSequentialPrespectraIsModelCategory} and with the classical model structure on compactly generated pointed topological spaces ([thm.](Introduction+to+Stable+homotopy+theory+--+P#ClassicalModelStructureOnCompactlyGeneratedTopologicalSpaces), [prop.](Introduction+to+Stable+homotopy+theory+--+P#ModelStructureOnSliceCategory)) in that it takes two cofibrations to a cofibration, and to an acyclic cofibration if at least one of the inputs is acyclic:

$$
  \begin{aligned}
    Cof_{strict} \Box Cof_{cl}
    & \subset\;
    Cof_{strict}
    \\
    Cof_{strict} \Box (Cof_{cl} \Box W_{cl})
    & \subset\;
    Cof_{strict} \cap W_{strict}
    \\
    Cof_{strict} \cap (W_{strict})
    \Box
    Cof_{cl}
    & \subset\;
    Cof_{strict} \cap W_{strict}
  \end{aligned}
  \,.
$$

Dually, the pullback powering satisfies

$$
  \begin{aligned}
    Fib_{strict}^{\Box Cof_{cl}}
    & \subset\;
    Fib_{strict}
    \\
    Fib_{strict}^{\Box ( Cof_{cl} \cap W_{cl})}
    & \subset\;
    Fib_{strict}\cap W_{strict}
    \\
    (Fib_{strict} \cap W_{strict})^{\Box Cof_{cl}}
    & \subset\;
    Fib_{strict} \cap W_{strict}
  \end{aligned}
  \,.
$$


=--

+-- {: .proof}
###### Proof

The statement concering the pullback powering follows directly form the analogous statement for topological spaces ([prop.](Introduction+to+Stable+homotopy+theory+--+P#PullbackPowering)) by the fact that via theorem \ref{StrictModelStructureOnSequentialPrespectraIsModelCategory} the fibrations and weak equivalences in $SeqSpec(Top_{cg})_{strict}$ are degree-wise those in $(Top_{cg}^{\ast/})_{Quillen}$. From this the statement about the pushout product follows dually by [[Joyal-Tierney calculus]] ([prop.](Introduction+to+Stable+homotopy+theory+--+P#JoyalTierneyCalculus)).

=--

+-- {: .num_remark #SeqSpecIsTopologicallyEnrichedModelCategory}
###### Remark

In the language of [[model category]]-theory, prop. \ref{PushoutProductWithRespectToSmashTensoringSatisfiesEnrichedModelCategoryAxioms} says that $SeqSpec(Top_{cg})_{strict}$ is an _[[enriched model category]]_, the enrichment being over $(Top_{cg}^{\ast/})_{Quillen}$. This is often referred to simply as a "topological model category".

=--


+-- {: .num_prop #PushoutProductOfspectrumWithSpaceInteractingWithHomSpaces}
###### Proposition

For $X \in SeqSpec(Top_{cg})$ a sequential spectrum, $f \in Mor(SeqSpec(Top_{cg}))$ any morphism of sequential spectra, and for $g  \in Mor(Top_{cpt}^{\ast/})$ a morphism of [[compact topological space|copact]] [[Hausdorff spaces]], then the [[hom-spaces]] of def. \ref{HomSpaceBetweenSequentialSpectra} interact with the pushout-product and pullback-powering from def. \ref{PushoutProductWithRespectToSmashTensoring} in that there is a [[natural isomorphism]]

$$
  SeqSpec(f \box g, X)
    \simeq
  SeqSpec(f,X)^{\Box g}
  \,.
$$

=--

+-- {: .num_prop #ConnectedComponentOfHomSpaceOfSeqentialSpectraLeftHomotopyClasses}
###### Proposition

For $X,Y \in SeqSpec(Top_{cg})$ two sequential spectra with $X$ a [[CW-spectrum]] (def. \ref{CWSpectrum}), then there is a [[natural bijection]]

$$
  \pi_0 SeqSpec(X,Y)
  \simeq
   [X,Y]_{strict}
$$

between the [[connected components]] of the [[hom-space]] from def. \ref{HomSpaceBetweenSequentialSpectra} and the [[hom-set]] in the [[homotopy category of a model category|homotopy category]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyCategoryOfAModelCategory)) of the strict model structure from theorem \ref{StrictModelStructureOnSequentialPrespectraIsModelCategory}.

=--

+-- {: .proof}
###### Proof

By def. \ref{HomSpaceBetweenSequentialSpectra} the path components of the [[hom-space]] are the [[left homotopy]] classes of morphisms of spectra with respect to the standard [[cylinder spectrum]] of def. \ref{StandardCylinderSpectrumSequential}:

$$
  \frac{
    I_+ \longrightarrow SeqSpec(X,Y)
  }{
    X \wedge (I_+) \longrightarrow Y
  }
  \,.
$$

By prop. \ref{CylinderSpectrumOverCWSpectrumIsGood}, for $X$ a [[CW-spectrum]] then the standard [[cylinder spectrum]] $X \wedge (I_+)$ is a good cyclinder object ([def.](Introduction+to+Stable+homotopy+theory+--+P#PathAndCylinderObjectsInAModelCategory)) on a cofibrant object. 

Since moreover every object in $SeqSpec(Top_{cg})_{strict}$ is fibrant, the statement follows (with [this lemma](Introduction+to+Stable+homotopy+theory+--+P#HomsOutOfCofibrantIntoFibrantComputeHomotopyCategory)).

=--


#### The stable model structure on sequential spectra
 {#StableModelStructureOnSequentialSpectra}


The actual spectrum objects of interest in [[stable homotopy theory]] are not the pre-spectra of def. \ref{SequentialSpectra}, but the [[Omega-spectra]] of def. \ref{OmegaSpectrum} among them.  Hence we need to equip the category of  [[sequential pre-spectra]] of def. \ref{SequentialSpectra} with a [[model category|model structure]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#ModelCategory)) whose fibrant-cofibrant objects are, in particular [[Omega-spectra]]. More in detail, it is plausible to require that every pre-spectrum is weakly equivalent to a fibrant-cofibrant one which is both an [[Omega-spectrum]] and a [[CW-spectrum]] as in def. \ref{CWSpectrum}. By prop. \ref{CellSpectraAreCofibrantInModelStructureOnTopologicalSequentialSpectra} this suggests to construct a model category structure on $SeqSpec(Top_{cg})$ that has the same cofibrations as the strict model structure of theorem \ref{StrictModelStructureOnSequentialPrespectraIsModelCategory}, but more weak equivalences (and hence less fibrations), such as to make every sequential pre-spectrum weakly equivalent to an Omega cell spectrum.

Such a situation is called a _[[Bousfield localization of model categories|Bousfield localization of a model category]]_.

##### Bousfield localization

In plain [[category theory]], a _[[localization]]_ of a [[category]] $\mathcal{C}$ is equivalently a [[full subcategory]]

$$
  i
    \;\colon\;
  \mathcal{C}_{loc}
    \hookrightarrow
  \mathcal{C}
$$

such that the inclusion functor has a [[left adjoint]] $L$

$$
  \mathcal{C}_{loc}
    \underoverset
      {\underset{i}{\longrightarrow}}
      {\overset{L}{\longleftarrow}}
      {\bot}
  \mathcal{C}
  \,.
$$

The [[adjunction unit]] $\eta_X \colon X \to L(X)$ "reflects" every object $X$ of $\mathcal{C}$ into one in the $\mathcal{C}_{loc}$, and therefore this is also called a _[[reflective subcategory]]_ inclusion.

It is a classical fact that in this situation

$$
  \mathcal{C}_{loc}
    \simeq
  \mathcal{C}[W^{-1}_L]
$$

is [[equivalence of categories|equivalently]] the [[localization]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyCategoryOfACategoryWithWeakEquivalences)) of $\mathcal{C}$ at the "$L$-equivalences", namely at those morphisms $f$ such that $L(f)$ is an isomorphism. Hence one also speaks of _[[reflective localizations]]_.

The following concept of _[[Bousfield localization of model categories]]_ is the evident lift of this concept of [[reflective localization]] from the realm of categories to the realm of [[model categories]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#ModelCategory)), where isomorphism is generealized to weak equivalence and where [[adjoint functors]] are taken to exhibit [[Quillen adjunctions]].
 
+-- {: .num_defn #BousfieldLocalizationOfModelCategories}
###### Definition


A **[[left Bousfield localization of model categories|left Bousfield localization]]** $\mathcal{C}_{loc}$ of a [[model category]] $\mathcal{C}$ ([def.](Introduction+to+Stable+homotopy+theory+--+P#ModelCategory)) is another model category structure on the same underlying category with the same cofibrations, 

$$
  Cof_{loc} = Cof
$$

but more weak equivalences

$$
  W_{loc} \supset W
  \,.
$$

=--

While that is a very simple definition, it turns out that something interesting happens to the fibrations when we keep the cofibrations fixed and increase the weak equivalences:

+-- {: .num_prop }
###### Proposition

Given a [[left Bousfield localization of model categories|left Bousfield localization]] $\mathcal{C}_{loc}$ of $\mathcal{C}$ as in def. \ref{BousfieldLocalizationOfModelCategories}, then

1. $Fib_{loc} \subset Fib$;


1. $W_{loc} \cap Cof_{loc} = W \cap Cof$;

1. the identity functors constitute a [[Quillen adjunction]]

   $$
     \mathcal{C}_{loc}
       \underoverset
         {\underset{id}{\longrightarrow}}
         {\overset{id}{\longleftarrow}}
         {\bot}
     \mathcal{C}
     \,.
   $$

=--

+-- {: .proof}
###### Proof

Regarding the first two items:

Using the properties of the [[weak factorization systems]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#WeakFactorizationSystem)) of (acyclic cofibratiojns, fibrations) and (cofibrations, acyclic fibrations) for both model structures we get

$$
  \begin{aligned}
    Fib_{loc} 
      &= 
    (Cof_{loc} \cap W_{loc})Inj
    \\
      &\subset 
    (Cof_{loc} \cap W)Inj 
    \\
      & = 
    Fib
  \end{aligned}
$$

and

$$
  \begin{aligned}
    Fib_{loc} \cap W_{loc}
      & =
    Cof_{loc} Inj 
    \\
      & = 
    Cof \, Inj 
    \\
      & = 
    Fib \cap W
  \end{aligned}
 \,.
$$

Regarding the third point:

By construction, $id \colon \mathcal{C}_{loc}\to \mathcal{C}$ preserves cofibrations and acyclic cofibrations, hence is a left Quillen functor.

=--

In plain [[category theory]], given a [[reflective subcategory]] 

$$
  \mathcal{C}_{loc}
    \underoverset
      {\underset{i}{\longrightarrow}}
      {\overset{L}{\longleftarrow}}
      {\bot}
  \mathcal{C}
$$

then the composite

$$
  Q \coloneqq i \circ L  
    \;\colon\; 
  \mathcal{C} 
    \longrightarrow
  \mathcal{C}
$$

is an [[idempotent monad]] on $\mathcal{C}$, hence, in particular, an [[endofunctor]] equipped with a [[natural transformation]] $\eta_X \;\colon\; X \to L X$ (the [[adjunction unit]]) -- which "reflects" every object into one in the image of $L$ -- such that this reflection is a projection in that each $L(\eta_X)$ is an isomorphism. This characterizes the [[reflective subcategory]] $\mathcal{C}_{loc} \hookrightarrow \mathcal{C}$ as the subcategory of those objects $X$ for which $\eta_X$ is an isomorphism.

The following is the lift of this alternative perspective of reflective localization via idempotent monads from category theory to model category theory.


+-- {: .num_defn #QuillenIdempotentMonad}
###### Definition

Let $\mathcal{C}$ be a [[model category]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#ModelCategory)) which is [[right proper model category|right proper]], in that [[pullback]] along fibrations preserves weak equivalences.

Say that a **Quillen idempotent monad** on $\mathcal{C}$ is
 
1. an [[endofunctor]] 

   $Q \;\colon\;  \mathcal{C} \longrightarrow \mathcal{C}$

1. a [[natural transformation]]

   $\eta \colon id_{\mathcal{C}} \longrightarrow Q$

such that

1. ([[homotopical functor]]) $Q$ preserves weak equivalences;

1. (idempotency) for all $X \in \mathcal{C}$ the morphisms

   $$
     Q(\eta_X) \;\colon\; Q(X) \overset{\in W}{\longrightarrow} Q(Q(X))
   $$

   and

   $$
     \eta_{Q(X)} \;\colon\; Q(X) \overset{\in W}{\longrightarrow} Q(Q(X))
   $$

   are weak equivalences;

1. (preservation of homotopy pullbacks) if in a [[pullback]] square in $\mathcal{C}$

   $$
     \array{
       f^\ast W &\stackrel{f^\ast h}{\longrightarrow}& X
       \\
       \downarrow && \downarrow^{\mathrlap{f}}
       \\
       W &\stackrel{h}{\longrightarrow}& Y
     }
   $$

   we have that

   1. $f$ is a fibration and $Y$ is fibrant;

   1. $\eta_X$, $\eta_Y$, and $Q(h)$ are weak equivalences

   then $Q(f^\ast h)$ is a weak equivalence.

=--


+-- {: .num_defn #ClassesOfMorphismsInBousfieldLocalizationAtQuillenIdempotentMonad}
###### Definition

For $Q \colon \mathcal{C} \longrightarrow \mathcal{C}$
a Quillen idempotent monad according to def. \ref{QuillenIdempotentMonad}, say that a morphism $f$ in $\mathcal{C}$ is

1. a **$Q$-weak equivalence** if $Q(f)$ is a weak equivalence;

1. **a $Q$-cofibation** if it is a cofibration.

1. **a $Q$-fibration** if it has the [[right lifting property]] against the morphisms that are both ($Q$-)cofibrations as well as $Q$-weak equivalences.

Write 

$$
  \mathcal{C}_Q
$$ 

for $\mathcal{C}$ equipped with these classes of morphisms. Notice that since $Q$ preserves weak equivalences (by def. \ref{QuillenIdempotentMonad}) then if these classes of morphisms do constitute a [[model category]] structure, then this is a [[Bousfield localization of model categories|left Bousfield localization]] of $\mathcal{C}$, according to def. \ref{BousfieldLocalizationOfModelCategories}.

=--



+-- {: .num_lemma #FirstLemmaForBousfieldFriedlander}
###### Lemma

In the situation of def. \ref{ClassesOfMorphismsInBousfieldLocalizationAtQuillenIdempotentMonad}, 
a morphism is an acyclic fibration in $\mathcal{C}_Q$ precisely if it is an acyclic fibration in $\mathcal{C}$.

=--

+-- {: .proof}
###### Proof

It is clear from the definition that an acyclic fibration is also a  $Q$-acyclic $Q$-fibration (since both are the class of moprhisms with [[right lifting property]] against the respective cofibrations, and the $Q$-cofibrations by definition are just the cofibrations). 

In the other direction, let $f \;\colon\; X \longrightarrow Y $ be a $Q$-acyclic $Q$-fibration. Consider its factorization into a cofibration followed by an acyclic fibration

$$
  f 
    \;\colon\; 
  X  
    \underoverset{\in Cof}{i}{\longrightarrow} 
  Z
    \underoverset{\in W \cap Fib}{p}{\longrightarrow}
  Y
  \,.
$$

Observe that $Q$-equivalences satisfy [[two-out-of-three]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#CategoryWithWeakEquivalences)), by functoriality and since the plain equivalences do. Now the assumption that $Q$ preserves weak equivalences together with [[two-out-of-three]] implies that $i$ is a $Q$-weak equivalence, hence a $Q$-acyclic $Q$-cofibration. This implies, by assumption on $f$, that $f$ has the [[right lifting property]] against $i$. Hence the [[retract argument]] ([prop.](Introduction+to+Stable+homotopy+theory+--+P#RetractArgument)), implies that $f$ is a [[retract]] of the acyclic fibration $p$, and so is itself an acyclic fibration.

=--

+-- {: .num_lemma #SecondLemmaForBousfieldFriedlander}
###### Lemma

In the situation of def. \ref{ClassesOfMorphismsInBousfieldLocalizationAtQuillenIdempotentMonad}, if a morphism $f \colon X \longrightarrow Y$ is a fibration, and $\eta_X, \eta_Y$ are weak equivalences, then $f$ is a $Q$-fibration.

=--

(e.g. [Goerss-Jardine 96, chapter X, lemma 4.4](#GoerssJardine96))

+-- {: .proof}
###### Proof

We need to show that for every [[commuting square]] of the form

$$
  \array{
    A &\overset{\alpha}{\longrightarrow}& X
    \\
    {}^{\mathllap{i}}_{\mathllap{\in W_Q \cap Cof_Q}}\downarrow 
     && 
    \downarrow^{\mathrlap{f}}
    \\
    B &\underset{\beta}{\longrightarrow}& Y
  }
$$

there exists a lifting.

To that end, first consider a factorization of the image under $Q$ of this square as follows:

$$
  \array{
    Q(A) &\overset{Q(\alpha)}{\longrightarrow}& Q(X)
    \\
    {}^{\mathllap{Q(i)}}\downarrow && \downarrow^{\mathrlap{Q(f)}}
    \\
    Q(B) &\underset{Q(\beta)}{\longrightarrow}& Q(Y)
  }
  \;\;\;\;\;\;
  \simeq
  \;\;\;\;\;\;
  \array{
    Q(A) 
     &\underoverset{\in W \cap Cof}{j_\alpha}{\longrightarrow}& 
    Z 
     &\underoverset{\in Fib}{p_\alpha}{\longrightarrow}& 
    Q(X)
    \\
    {}^{\mathllap{Q(i)}}\downarrow 
      &&
    \downarrow^{\pi}
      && 
    \downarrow^{\mathrlap{Q(f)}}
    \\
    Q(B) 
      &\underoverset{j_\beta}{\in W \cap Cof}{\longrightarrow}& 
    W 
      &\underoverset{p_\beta}{\in Fib}{\longrightarrow}& 
    Q(Y)
  }
$$

(This exists even without assuming [[functorial factorization]]: factor the bottom morphism, form the pullback of the resulting $p_\beta$, observe that this is still a fibration, and then factor (through $j_\alpha$) the universal morpism from the outer square into this pullback.)

Now consider the pullback of the right square above along the naturality square of $\eta \colon id \to Q$, take this to be the right square in the following diagram

$$
  \array{
    \alpha \colon
    & 
    A 
      &\overset{(j_\alpha \circ \eta_A, \alpha)}{\longrightarrow}&
    Z \underset{Q(X)}{\times} X
      &\overset{}{\longrightarrow}&
    X
    \\
    & {}^{\mathllap{i}}\downarrow 
      &&
    \downarrow^{\mathrlap{(\pi,f)}}
      &&
    \downarrow^{\mathrlap{f}}&
    \\
    \beta \colon 
    & 
    B 
      &\underset{(j_\beta\circ\eta_B,\beta)}{\longrightarrow}&
    W \underset{Q(Y)}{\times} Y
      &\underset{}{\longrightarrow}&
    Y
  }
  \,,
$$

where the left square is the universal morphism into the pullback which is induced from the naturality squares of $\eta$ on $\alpha$ and $\beta$.

We claim that $(\pi,f)$ here is a weak equivalence. This implies that we find the desired lift by factoring $(\pi,f)$ into an acyclic cofibration followed by an acyclic fibration and then lifting consecutively as follows

$$
  \array{
    \alpha \colon
    & 
    A 
      &\overset{(j_\alpha \circ \eta_A, \alpha)}{\longrightarrow}&
    Z \underset{Q(X)}{\times} X
      &\overset{}{\longrightarrow}&
    X
    \\
    & {}^{\mathllap{id}}\downarrow 
      &&
    {}^{\mathllap{\in W \cap Cof}}\downarrow
      &{}^{\mathllap{\exists}}\nearrow&
    \downarrow^{\mathrlap{f}}_{\mathrlap{\in Fib}}&
    \\
    & 
    A 
      &\longrightarrow& 
      &\overset{\phantom{AAAAAAA}}{\longrightarrow}&
    Y
    \\
    & {}^{\mathllap{i}}_{\mathllap{\in Cof}}\downarrow 
      &{}^{\mathllap{\exists}}\nearrow&
    \downarrow^{\mathrlap{\in W \cap Fib}}
      &&
    \downarrow^{\mathrlap{id}}&
    \\
    \beta \colon & 
    B 
      &\underset{(j_\beta\circ\eta_B,\beta)}{\longrightarrow}&
    W \underset{Q(Y)}{\times} Y
      &\longrightarrow&
    Y
  }
  \,.
$$

To see that $(\phi,f)$ indeed is a weak equivalence:

Consider the diagram

$$
  \array{
     Q(A) 
       &\underoverset{\in W \cap Cof}{j_\alpha}{\longrightarrow}& 
     Z
       &\underoverset{\in W}{pr_1}{\longleftarrow}&
     Z \underset{Q(X)}{\times} X
     \\
     {}^{\mathllap{Q(i)}}_{\mathllap{\in W}}\downarrow 
       && 
     \downarrow^{\mathrlap{\pi}}
       && 
     \downarrow^{\mathrlap{(\pi,f)}}
     \\
     Q(B) 
       &\underoverset{j_\beta}{\in W \cap Cof}{\longrightarrow}& 
     Z
       &\underoverset{pr_2}{\in W}{\longleftarrow}&
     W \underset{Q(X)}{\times} X
  }
  \,.
$$

Here the projections are weak equivalences as shown, because by assumption in def. \ref{QuillenIdempotentMonad} the ambient model category is [[right proper model category|right proper]] and these projections are the pullbacks along the fibrations $p_\alpha$ and $p_\beta$ of the morphisms $\eta_X$ and $\eta_Y$, respectively, where the latter are weak equivalences by assumption. Moreover $Q(i)$ is a weak equivalence, since $i$ is a $Q$-weak equivalence.

Hence now it follows by [[two-out-of-three]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#CategoryWithWeakEquivalences)) that $\pi$ and then $(\pi,f)$ are weak equivalences.

=--


+-- {: .num_prop #BousfieldFriedlanderTheorem}
###### Proposition
**(Bousfield-Friedlander theorem)**

Let $\mathcal{C}$ be a [[model category]]. Let $Q \colon \mathcal{C} \longrightarrow \mathcal{C}$
be a Quillen idempotent monad on according to def. \ref{QuillenIdempotentMonad}.

Then the [[Bousfield localization of model categories|Bousfield localization]] model category $\mathcal{C}_Q$ at the $Q$-weak equivalences (def. \ref{ClassesOfMorphismsInBousfieldLocalizationAtQuillenIdempotentMonad}) exists.

=--

([Bousfield-Friedlander 78, theorem 8.7](#BousfieldFriedlander78), [Bousfield 01, theorem 9.3 ](#Bousfield01), [Goerss-Jardine 96, lemma 4.5, lemma 4.6](#GoerssJardine96)) 

+-- {: .proof}
###### Proof

The existence of [[limits]] and [[colimits]] is guaranteed since $\mathcal{C}$ is already assumed to be a model category.
The [[two-out-of-three]] poperty for $Q$-weak equivalences is an immediate consequence of two-out-of-three for the original weak equivalences of $\mathcal{C}$. 

Moreover, according to lemma \ref{FirstLemmaForBousfieldFriedlander} the pair of classes $(Cof_{Q}, W_Q \cap Fib_Q)$ equals the pair $(Cof, W \cap Fib)$, and this is a [[weak factorization system]] by the model structure $\mathcal{C}$.

Hence it remains to show that $(W_Q \cap Cof_Q, \; Fib_Q)$ is a [[weak factorization system]]. The lifting property here holds by definition of $Fib_Q$. We conclude by showing the existence of factorizations:


First we consider the case of morphisms of the form $f \colon Q(Y) \to Q(Y)$. This may be factored with respect to $\mathcal{C}$ as

$$
  f 
  \;\colon\;
  Q(X)
    \underoverset{\in W \cap Cof}{\in i}{\longrightarrow}
  Z
    \underoverset{\in Fib}{p}{\longrightarrow}
  Q(Y)
  \,.
$$

Here $i$ is already a $Q$-acyclic $Q$-cofibration. Now apply $Q$ to obtain

$$
  \array{
  f 
  \colon
  &
  Q(X)
    &\underoverset{\in W \cap Cof}{i}{\longrightarrow}&
  Z
    &\underoverset{\in Fib}{p}{\longrightarrow}&
  Q(Y)
  \\
  &
  \downarrow^{\mathrlap{\eta_{Q(X)}}}_{\mathrlap{\in W}} 
    && 
  \downarrow^{\mathrlap{\eta_Z}} 
    && 
  \downarrow^{\mathrlap{\eta_{Q(Y)}}}_{\mathrlap{\in W}}
  \\
  &
  Q(Q(X))
    &\underoverset{Q(i)}{\in W}{\longrightarrow}&
  Z
    &\underset{}{\longrightarrow}&
  Q(Y)
  }
  \,,
$$

where $\eta_{Q(X)}$ and $\eta_{Q(Y)}$ are weak equivalences by idempotency, and $Q(i)$ is a weak equivalence since $Q$ preserves weak equivalences. Hence by [[two-out-of-three]] also $\eta_Z$ is a weak equivalence. Therefore lemma \ref{SecondLemmaForBousfieldFriedlander} gives that $p$ is a $Q$-fibration, and hence the above factorization is already as desired

$$
  f 
  \;\colon\;
  Q(X)
    \underoverset{\in W_Q \cap Cof_Q}{\in i}{\longrightarrow}
  Z
    \underoverset{\in Fib_Q}{p}{\longrightarrow}
  Q(Y)
  \,.
$$

Now for $g$ an arbitrary morphism $g \colon X \to Y$, form a factorization of $Q(g)$ as above and then decompose the naturality square for $\eta$ on $f$ into the pullback of the resulting $Q$-fibration along $\eta_Y$:

$$
  \array{
    g \colon
    & 
    X 
      &\overset{\tilde i}{\longrightarrow}&
    Z \underset{Q(Y)}{\times} Y
      &\overset{\tilde p}{\longrightarrow}&
    Y
    \\
    &
    {}^{\mathllap{\eta_X}}_{\mathllap{\in W_Q}}\downarrow 
      && 
    \downarrow^{\mathrlap{\eta'}}_{\mathrlap{}} 
      &(pb)& 
    \downarrow^{\mathrlap{\eta_Y}}_{\mathrlap{\in W_Q}}
    \\
    Q(g)
    \colon
    &
    Q(Y)
      &\underoverset{i}{\in W_Q}{\longrightarrow}& 
    Z
      &\underoverset{p}{\in Fib_Q}{\longrightarrow}&
    Q(Y)
  }
  \,.
$$

This exhibits $\eta'$ as the pullback of a $Q$-weak equivalence along a $Q$-fibration, and hence itself as a $Q$-weak equivalence. This way, [[two-out-of-three]] implies that $\tilde i$ is a $Q$-weak equivalence.

Finally, apply factorization in $(Cof,\; W\cap Fib)$ to $\tilde i$ to obtain the desired factorization

$$
  f 
  \;\colon\;
  \overset{W_Q \cap Cof}{\longrightarrow}
  \overset{W \cap Fib = W_Q \cap Fib_Q}{\longrightarrow}
  \overset{Fib_Q}{\longrightarrow}
  \,.
$$

=--


+-- {: .num_prop #CharacterizationOfFibrationsInBFModelStructures}
###### Proposition

For $Q \colon \mathcal{C} \longrightarrow \mathcal{C}$
a Quillen idempotent monad according to def. \ref{QuillenIdempotentMonad},
then a morphism $f \colon X \to Y$ in $\mathcal{C}$ is a $Q$-fibration (def. \ref{ClassesOfMorphismsInBousfieldLocalizationAtQuillenIdempotentMonad}) precisely if 

1. $f$ is a fibration;

1. the $\eta$-naturality square on $f$ 

   $$
     \array{
       X &\stackrel{\eta_X}{\longrightarrow}& Q(X)
       \\
       {}^{\mathllap{f}}\downarrow &{}^{(pb)^h}& \downarrow^{\mathrlap{Q(f)}}
       \\
       Y &\underset{\eta_Y}{\longrightarrow}& Q(Y)
     }
   $$

   exhibits a [[homotopy pullback]] in $\mathcal{C}$, in that for any factorization of $Q(f)$ trough a weak equivalence followed by a fibration $p$, then the universally induced morphism

  $$
    X \longrightarrow p^\ast Y
  $$

  is weak equivalence (in $\mathcal{C}$).

=--

(e.g. [Goerss-Jardine 96, theorem 4.8](#GoerssJardine96))

+-- {: .proof}
###### Proof

First consider the case that $f$ is a fibration and that the square is a homotopy pullback. We need to show that then $f$ is a $Q$-fibration.

Factor $Q(f)$ as

$$
  Q(f) 
    \;\colon\;
  Q(X)
    \underoverset{\in W \cap Cof}{i}{\longrightarrow}
  Z
    \underoverset{\in Fib}{p}{\longrightarrow}
  Q(Y)  
  \,.
$$

By the proof of prop. \ref{BousfieldFriedlanderTheorem} the morphism $p$ is also a $Q$-fibration. Hence by the existence of the $Q$-local model structure due to prop. \ref{BousfieldFriedlanderTheorem}, its pullback is also a $Q$-fibration

$$
  \array{
    X &\overset{\eta_X}{\longrightarrow}& Q(X)
    \\
    {}^{\mathllap{\tilde i}}_{\mathllap{\in W}}\downarrow 
      && 
    \downarrow^{\mathrlap{i}}_{\mathrlap{\in W}}
    \\
    Y \underset{Q(Y)}{\times} Z 
      &\overset{p^\ast \eta_Y}{\longrightarrow}&
    Z
    \\
    {}^{\mathllap{\tilde p}}_{\mathllap{\in Fib_Q}}\downarrow 
      && 
    \downarrow^{\mathrlap{p}}_{\mathrlap{\in Fib_Q}}
    \\
    Y &\underset{\eta_Y}{\longrightarrow}& Q(Y)
  }
  \,.
$$

Here $\tilde i$ is a weak equivalence by assumption that the diagram exhibits a homotopy pullback. Hence it factors as

$$
  \tilde i
  \;\colon\;
  X 
    \underoverset{\in W \cap Cof}{j}{\longrightarrow}
  W
    \underoverset{\in W \cap Fib = W_Q \cap Fib_Q}{\pi}{\longrightarrow}
  Y \underset{Q(Y)}{\times} Z
  \,.
$$

This yields the situation

$$
  \array{
    X &\overset{=}{\longrightarrow}& X
    \\
    {}^{\mathllap{j}}_{\mathllap{\in W \cap Cof}}\downarrow 
      &{}^{\mathllap{\exists}}\nearrow& 
    \downarrow^{\mathrlap{f}}_{\mathrlap{\in Fib}}
    \\
    W 
      &\underoverset{\tilde p \circ \pi}{\in Fib_Q}{\longrightarrow}&
    Y
  }
$$

As in the [[retract argument]] ([prop.](Introduction+to+Stable+homotopy+theory+--+P#RetractArgument)) this is seen to exhibit $f$ as a [[retract]] (in the [[arrow category]], [rmk.](Introduction+to+Stable+homotopy+theory+--+P#RetractsOfMorphisms)) of the $Q$-fibration $\tilde p \circ \pi$. Hence by the existence of the $Q$-model structure and the closure properties for fibrations ([prop.](Introduction+to+Stable+homotopy+theory+--+P#ClosurePropertiesOfInjectiveAndProjectiveMorphisms)), also $f$ is a $Q$-fibration.

Now for the converse. Assume that $f$ is a $Q$-fibration. Since $\mathcal{C}{C}_Q$ is a [[Bousfield localization of model categories|left Bousfield localization]] of $\mathcal{C}$ it is immediate that $f$ is also a fibration. We need to show that the $\eta$-naturality square on $f$ exhibits a homotopy pullback.

So factor $Q(f)$ as before, and consider the pasting composite of the factorization of the given square with the naturality squares of $\eta$:

$$
  \array{
     &&
    Q(X) 
      &\underoverset{\in W}{\eta_{Q(X)}}{\longrightarrow}&
    Q(Q(X))
    \\
      && 
    {}^{\mathllap{i}}_{\mathllap{\in W}}\downarrow
      && 
    \downarrow^{\mathrlap{Q(i)}}_{\mathrlap{\in W}}
    \\
    Y \underset{Q(Y)}{\times} Z 
      &\underoverset{\in W_Q}{p^\ast \eta_Y}{\longrightarrow}&
    Z
      &\underoverset{\in W}{\eta_Z}{\longrightarrow}&
    Q(Z)
    \\
    {}^{\mathllap{\tilde p}}_{\mathllap{\in Fib_Q}}\downarrow 
      &(pb)& 
    \downarrow^{\mathrlap{p}}_{\mathrlap{\in Fib_Q}}
      &&
    \downarrow^{\mathrlap{Q(p)}}
    \\
    Y 
      &\underoverset{\eta_Y}{\in W_Q}{\longrightarrow}& 
    Q(Y)
      &\underoverset{\eta_{Q(Y)}}{\in W}{\longrightarrow}&
    Q(Q(Y))
  }
  \,.
$$

The top and bottom horizontal weak equivalences are by the idempotency of $Q$, and $Q(i)$ is a weak equivalence since $Q$ preserves weak equivalences. Hence by [[two-out-of-three]] also $\eta_Z$ is a weak equivalence. Finally $p^\ast \eta_Y$ is a $Q$-weak equivalence since it is the pullback of a $Q$-weak equivalence along a fibration between objects whose $\eta$ is a weak equivalence, via the third clause in def. \ref{QuillenIdempotentMonad}.

In particular, therefore the bottom right square is a homotopy pullback, and since the left square is even a genuine pullback, hence a homotopy pullback, the total bottom rectangle here exhibits a homotopy pullback.

Now by [[natural transformation|naturality]] of $\eta$, that total rectangle is the same as

$$
  \array{
    Y \underset{Q(Y)}{\times} Z 
      &\overset{\eta_{\left(Q \underset{Q(Y)}{\times} Z\right)}}{\longrightarrow}&
    Q(Y \underset{Q(Y)}{\times} Z)
      &\underoverset{\in W}{Q(p^\ast \eta_Y)}{\longrightarrow}&
    Q(Z)
    \\
    {}^{\mathllap{\tilde p}}_{\mathllap{\in Fib_Q}}\downarrow 
      && 
    \downarrow^{\mathrlap{Q(\tilde p)}}_{\mathrlap{\in Fib_Q}}
      &&
    \downarrow^{\mathrlap{Q(p)}}
    \\
    Y 
      &\underset{\eta_Y}{\longrightarrow}& 
    Q(Y)
      &\underoverset{Q(\eta_Y)}{\in W}{\longrightarrow}&
    Q(Q(Y))
  }
  \,,
$$

where now $Q(p^\ast \eta_Y) \in W$ since $p^\ast \eta_Y \in W_Q$, by the previous remark. This means that the right square is again a homotopy pullback, and since the total rectangle still is, so is now also the left square.

To conclude, use the observation from the first part of the proof that $f$ is a [[retract]] (in the [[arrow category]], [rmk.](Introduction+to+Stable+homotopy+theory+--+P#RetractsOfMorphisms)) of $\tilde p \circ \pi$, where $\pi$ is an acyclic fibration. Notice that the $\eta$-naturality square of a weak equivalence is a homotopy pullback ($Q$ preserves the weak equivalence) and that the composite of two morphisms with this property still has this property. Therefore $f$ is the retract of a morphism with this property, 

Hence the $\eta$-naturality square of $f$ is the retract of a homotopy pullback square, and so it is itself a homotopy pullback square.

=--



##### Proof of the stable model structure
 {#ProofOfTheStableModelStructure}

We show now that the operation of [[Omega-spectrification]] from def. \ref{SpectrificationForTopologicalSequentialSpectra} is a Quillen idempotent monad in the sense of def. \ref{QuillenIdempotentMonad}. Via the [[Bousfield-Friedlander theorem]] (prop. \ref{BousfieldFriedlanderTheorem}). This establishes a stable model structure on topological sequential spectra.

+-- {: .num_prop #OmegaSpectrificationOnTopologicalSequentialSpectraIsQuillenIdempotentMonad}
###### Proposition

The [[Omega-spectrification]] $(Q,j)$ from def. \ref{SpectrificationForTopologicalSequentialSpectra} is a Quillen idempotent monad in the sense of def. \ref{QuillenIdempotentMonad} on the strict model structre theorem \ref{StrictModelStructureOnSequentialPrespectraIsModelCategory}:

$$
  Q 
    \;\colon\; 
  SeqSpec(Top_{cg})_{strict}
    \longrightarrow
  SeqSpec(Top_{cg})_{strict}  
  \,.
$$

=--

([Schwede 97, lemma 2.1.3 (e), prop. 2.1.5](#Schwede97))


+-- {: .proof}
###### Proof

First notice that the strict model structure is indeed [[right proper model category|right proper]], as demanded in def. \ref{QuillenIdempotentMonad}: Since every object in $SeqSpec(Top_{cg})$ is fibrant (this being so degreewise in $(Top_{cg}^{\ast/})_{Quillen}$) this follows from [this lemma](Introduction+to+Stable+homotopy+theory+--+P#InCfPullbackAlongFibrationPreservesWeakEquivalences).

Now the first two conditions required on a Quillen idempotent monad in def. \ref{QuillenIdempotentMonad} are explicit in prop. \ref{PropertiesOfSpectrificationForTopologicalSequentialSpectra}. It remains to check the third condition:

First we claim that given a [[pullback]] of a strict fibration

$$
  \array{
    X \underset{B}{\times}Y &\longrightarrow& Y
    \\
    \downarrow &(pb)& \downarrow^{\mathrlap{\in Fib_{strict}}}
    \\
    X &\longrightarrow& B
  }
$$

then for any factorization

$$
  Q(Y) 
    \overset{\in W_{strict} Cof_{strict}}{\longrightarrow} 
  \widehat {Q(Y)}
    \overset{\in Fib_{strict}}{\longrightarrow}
  Q(X)
$$

the induced morphism

$$
  Q(X \underset{B}{\times} Y)
    \longrightarrow
  Q(X)\underset{Q(B)}{\times} \widehat {Q(Y)}
$$

is a weak equivalence.

(...)

Now to see that this implies the pullback property in item 3 of \ref{QuillenIdempotentMonad}.

Since in $SeqSpec(Top_{cg})_{strict}$ all objects are fibrant (a property directly inherited from $Top_{cg}^{\ast/}$) it follows (by [this lemma](Introduction+to+Stable+homotopy+theory+--+P#InCfPullbackAlongFibrationPreservesWeakEquivalences)) that pullback along fibrations preserves weak equivalences. Hence

$$
  \array{
    Q(X \underset{B}{\times}Y) &\longrightarrow& Q(Y)
    \\
    {}^{\mathllap{\in W_{strict}}}\downarrow && \downarrow^{\mathrlap{\in W_{strict}}}
    \\
    X \underset{B}{\times} \widehat{Q X} &\overset{\in W_{strict}}{\longrightarrow}& \widehat{Q Y}
    \\
    \downarrow &(pb)& \downarrow^{\mathrlap{\in Fib_{strict}}}
    \\
    X &\underset{\in W_{strict}}{\longrightarrow}& B
  }
$$

Now it follows by [[two-out-of-three]] that also the top morphism is in $W_{strict}$.

=--


+-- {: .num_theorem #StableModelStructureOnSequentialSpectraIsModelCategory}
###### Theorem

The [[Bousfield localization of model categories|left Bousfield localization]] of the strict model structure on sequential spectra (theorem \ref{StrictModelStructureOnSequentialPrespectraIsModelCategory}) at the class of [[stable weak homotopy equivalences]] (def. \ref{StableWeakHomotopyEquivalenceOfSequentialTopologicalSpectra}) exists, called the **stable model structure** on topological sequential spectra

$$
  SeqSpec(Top_{cg})_{stable}
    \underoverset
      {\underset{id}{\longrightarrow}}
      {\overset{id}{\longleftarrow}}
      {\bot}
  SeqSpec(Top_{cg})_{strict}
  \,.
$$

Moreover, its fibrant objects are precisely the [[Omega-spectra]] (def.\ref{OmegaSpectrum}).

=--

+-- {: .proof}
###### Proof

Let $(Q,\eta)$ be the [[Omega-spectrification]] operation from def. \ref{SpectrificationForTopologicalSequentialSpectra}. According to prop. \ref{OmegaSpectrificationOnTopologicalSequentialSpectraIsQuillenIdempotentMonad} this is a Quillen-idempotent monad (def. \ref{QuillenIdempotentMonad}) on $SeqSpec(Top_{cg})_{strict}$. Hence the [[Bousfield-Friedlander theorem]] (prop. \ref{BousfieldFriedlanderTheorem}) asserts that the [[Bousfield localization of model categories|Bousfield localization]] of  the strict model structure at the $Q$-equivalences exists. By prop. \ref{PropertiesOfSpectrificationForTopologicalSequentialSpectra} these are precisely the stable weak homotopy equivalences.

Finally, by prop. \ref{CharacterizationOfFibrationsInBFModelStructures} an object $X \in SeqSpec(Top_{cg})_{stable}$ is fibrant in $SeqSpec(Top_{cg})_{stable}$ precisely if 

$$
  \array{
     X &\overset{\eta_X}{\longrightarrow}& Q(X)
     \\
     \downarrow && \downarrow
     \\
     \ast &\longrightarrow& \ast
  }
$$

exhibits a [[homotopy pullback]] in $SeqSpec(Top_{cg})_{strict}$. Since every  object in $SeqSpec(Top_{cg})_{strict}$ is fibrant, the vertical morphisms here are fibrations. The pullback of $Q(X)$ along $id_\ast$ is just $Q(X)$ itself, and the universally induced morphism into this pullback is just $\eta_X$ itself. Hence the square is a homotopy pullback precisely if $\eta_X$ is a weak equivalence in $SeqSpec(Top_{cg})_{strict}$, hence degreewise a [[weak homotopy equivalence]]. Since $Q(X)$ is an [[Omega-spectrum]] by prop. \ref{PropertiesOfSpectrificationForTopologicalSequentialSpectra}, this means precisely that $X$ is an Omega-spectrum.


=--



##### Stability of the homotopy theory
 {#StabilityOfTheStableModelStructure}

We discuss that the stable model structure $SeqSpec(Top)_{stable}$ of theorem \ref{StableModelStructureOnSequentialSpectraIsModelCategory} is indeed a [[stable model category]] in that the canonical [[reduced suspension]] operation $\Sigma$ is an [[equivalence of categories]] from the [[stable homotopy category]] (def. \ref{TheStableHomotopyCategory}) to itself. This is theorem \ref{StableModelStructureOnSequentiaSpectraIsStableModelCategory} below. 


+-- {: .num_defn #StableModelCategory}
###### Definition

A [[pointed category|pointed]] [[model category]] $\mathcal{C}$ is called a **[[stable model category]]** if the canonically induced [[reduced suspension]] and [[loop space object]]-[[functors]] ([prop. ](Introduction+to+Stable+homotopy+theory+--+P#LoopingAsFunctorOnHomotopyCategory)) on its [[homotopy category]] ([defn.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyCategoryOfAModelCategory)) is an [[equivalence of categories]]

$$
  (\Sigma \dashv \Omega)
  \;\colon\;
  Ho(\mathcal{C})
   \underoverset
     {\underset{\Omega}{\longrightarrow}}
     {\overset{\Sigma}{\longleftarrow}}
     {\simeq}
  Ho(\mathcal{C})
  \,.
$$

=--

In order to prove that this is the case for $SeqSpec(Top_{cg})$ we first relate now the operations of "standard suspension" (def. \ref{SequentialSpectrumRealSuspension}) and of "alternative suspension" (def. \ref{SequentialSpectrumFakeSuspension}) to each other. The former is manifestly a model for the correct suspension, but the latter is better behaved, so we will show that they are naturally isomorphic in the stable homotopy category. According to remark \ref{StandardAndAlternativeSuspensionAreNotDirectlyComparable} both are directly comparable and isomorphic in even degrees, but non-comparable in odd degree. Therefore we now first introduce the concept of sequential spectra with components only in even degree and then use an adjunction back to ordinary sequential spectra.


+-- {: .num_defn #SequentialS2Spectra}
###### Definition

A **sequential $S^2$-spectrum** is a sequence of component spaces $X_{2n} \in Top_{cg}$ for $n \in \mathbb{N}$, and a sequence of structure maps of the form

$$
  \sigma_n \;\colon\; S^2 \wedge X_{2n}  \longrightarrow X_{2n+2}
  \,.
$$

A homomorphism of sequential $S^2$-spectra $f \colon X \to Y$ is a sequence of component maps $f_{2n} \;\colon\; X_{2n} \to Y_{2n}$ such that all these diagrams commute:

$$
  \array{
    S^2 \wedge X_{2n} &\overset{S^2 \wedge f_{2n}}{\longrightarrow}& Y_{2n}
    \\
    {}^{\mathllap{\sigma_n^{X}}}\downarrow && \downarrow^{\mathrlap{\sigma_n^Y}}
    \\
    X_{2n+2} &\underset{f_{2n+2}}{\longrightarrow}& Y_{n+2}
  }
  \,.
$$

Write

$$
  Seq_2Spec(Top_{cg})
$$

for the resulting category of sequential $S^2$-spectra.

=--

+-- {: .num_lemma #AdjunctionBetweenSequentialSpectraAndSequentialS2Spectra}
###### Lemma

There is a pair of [[adjoint functors]]

$$
  SeqSpec(Top_{cg})
    \underoverset  
     {\underset{R_2}{\longrightarrow}}
     {\overset{L_2}{\longleftarrow}}
     {\bot}
  Seq_2Spec(Top_{cg})
$$

between sequential spectra (def. \ref{SequentialSpectra}) and sequential $S^2$-spectra (def. \ref{SequentialS2Spectra})

* where $(R_2 X)_{2 n} \coloneqq X_{2 n}$ and 

  $$
    \sigma_n^{R_2 X} 
      \;\colon\;
    S^2 X_{2n}
      \simeq
    S^1 \wedge S^1 \wedge X_{2n}
      \overset{S^1 \wedge \sigma_{2n}^X}{\longrightarrow}
    S^1 \wedge X_{2n+1}
      \overset{\sigma_{2n+1}^X}{\longrightarrow}
    X_{2n+2}
  $$

* and where 

  $$
   (L_2 \mathcal{X})_n 
     \coloneqq 
   \left\{ 
     \array{ 
        \mathcal{X}_n & if \; n \; even  
        \\ 
        S^1 \wedge \mathcal{X}_{n-1} & if \; n \; odd
     }
   \right.
  $$ 

  and

  $$
    \sigma^{L_2 \mathcal{X}}_{n}
    =
    \left\{
      \array{
        id_{S^1 \wedge \mathcal{X}_n} & if \; n \; even
        \\
        \sigma^{\mathcal{X}}_n & if \; n \; odd
      }
    \right.
    \,.
  $$

Moreover, for each $X \in SeqSpec(Top_{cg})$, the [[adjunction unit]]

$$
  L_2 R_2 X \longrightarrow X
$$

is a [[stable weak homotopy equivalence]] (def. \ref{StableWeakHomotopyEquivalenceOfSequentialTopologicalSpectra}) hence (by lemma \ref{StableWeakHomotopyEquivalenceInSeqSpecIsStableEquivalence}) a stable weak equivalence.

=--

+-- {: .proof}
###### Proof

To see that we have an adjunction, consider a homomorphism

$$
  f \;\colon\;  L_2 \mathcal{X} \longrightarrow Y
  \,.
$$

Given its even-graded component maps, then its odd-graded component maps $f_{2n+1}$ need to fit into [[commuting squares]] of the form

$$
  \array{
    S^1 \wedge \mathcal{X}_{2n}
      &\overset{S^1 \wedge f_{2n}}{\longrightarrow}&
    S^1 \wedge Y_{2n}
    \\
    {}^{\mathllap{id}}\downarrow && \downarrow^{\mathrlap{\sigma_{2n}^Y}}
    \\
    S^1 \wedge \mathcal{X}_{2n} &\underset{f_{2n+1}}{\longrightarrow}&
    Y_{2n+1}
  }
  \,.
$$

Since here the left map is an identity, this uniquely fixes the odd-graded components $f_{2n+1}$ in terms of the even-graded components. Moreover, these components then make the following pasting rectangles comute

$$
  \array{
    S^2 \wedge \mathcal{X}_{2n} &\overset{S^2 \wedge f_{2n}}{\longrightarrow}& 
    S^2 \wedge Y_{2 n}
    \\
    {}^{\mathllap{\simeq}}\downarrow && \downarrow^{\mathrlap{S^1 \wedge \sigma_{2n}^Y}}
    \\
    S^2 \wedge \mathcal{X}_{2n} &\overset{S^1 \wedge f_{2n+1}}{\longrightarrow}& S^1 \wedge Y_{2n+1}
    \\
    {}^{\mathllap{\sigma_{2n}^{\mathcal{X}}}}\downarrow && \downarrow^{\mathrlap{\sigma_{2n+1}^Y}}
    \\
    \mathcal{X}_{2n+2} &\overset{f_{2n+2}}{\longrightarrow}& Y_{2n+2}
  }
  \,.
$$

This equivalently exhibits $f_\bullet$ as a homomorphism

$$
  \tilde f
    \;\colon\;
  \mathcal{X} \longrightarrow R_2 Y
$$

and hence establishes the adjunction isomorphism.

Finally to see that the [[adjunction unit]] is a [[stable weak homotopy equivalence]]: for $X \in SeqSpec(Top_{cg})$ then the morphism of stable homotopy groups induced from 

$$
  L_2 R_2 X \longrightarrow X
$$

is in degree $q$

$$
  \array{
     \underset{\longrightarrow}{\lim} (\cdots &\to& \pi_{q+2k}(X_{2k}) && \longrightarrow && \pi_{q+2k+2}(X_{q+2k+2}) &\to& \cdots ) &=& 
     \pi_q(L_2 R_2 X)
     \\
     && {}^{\mathllap{\simeq}}\downarrow && && {}^{\mathllap{\simeq}}\downarrow && && \downarrow
     \\
     \underset{\longrightarrow}{\lim} (\cdots &\to& \pi_{q+2k}(X_{2k}) &\longrightarrow& \pi_{2+2k+1}(X_{2k+1}) &\longrightarrow& \pi_{q+2k+2}(X_{q+2k+2}) &\to& \cdots ) &=& 
     \pi_q(X)
  }
  \,.
$$

From this it is clear by inspection that the induced vertical map on the right is an isomorphism. Stated more abstractly: the inclusion of [[partially ordered sets]] $\mathbb{N}_{even}^{\leq} \hookrightarrow \mathbb{N}^{\leq}$ is a [[cofinal functor]] and hence restriction along it preserves colimits.

=--


+-- {: .num_lemma #IsomorphismBetweenStandardAndAlternativeSuspensionInHomotopyCategory}
###### Lemma

There is a [[natural isomorphism]] in the [[stable homotopy category]] (def. \ref{TheStableHomotopyCategory}) between the total [[derived functors]] ([prop.](Introduction+to+Stable+homotopy+theory+--+P#QuillenAdjunctionInducesAdjunctionOnHomotopyCategories)) of the standard suspension (def. \ref{SequentialSpectrumRealSuspension}) and of the alternative suspension (def. \ref{SequentialSpectrumFakeSuspension}):

$$
  \Sigma (-)
   \; \simeq \;
  (-) \wedge S^1
  \;\;\;\;\;
  \in Ho(SeqSpec(Top_{cg})_{stable})
$$

=--

(e.g. [Jardine 15, prop. 10.53](sequential#spectrum#Jardine15))

+-- {: .proof}
###### Proof

Consider the adjunction $(L_2 \dashv R_2) \colon SeqSpec(Top) \leftrightarrow Seq_2Spec(Top)$ from lemma \ref{AdjunctionBetweenSequentialSpectraAndSequentialS2Spectra}.

Via the discussion in remark \ref{StandardAndAlternativeSuspensionAreNotDirectlyComparable}, there is a [[natural isomorphism]] in $Seq_2 Spec(Top)$ between the image under $R_2$ of the two suspension operations

$$
  \tau \;\colon\; R_2 (\Sigma(-)) \simeq R_2((-)\wedge S^1)
  \,,
$$

whose components are given by the [[smash product]]-[[braiding]] isomorphisms

$$
  S^2 \wedge (-) 
    \overset{\simeq}{\longrightarrow}
  (-) \wedge S^2
  \,.
$$

By lemma \ref{AdjunctionBetweenSequentialSpectraAndSequentialS2Spectra} the [[adjunction unit]] is a stable weak equivalence, so that we get a natural [[zig-zag]] of stable weak equivalences:

$$
  \Sigma X
    \underset{\in W_{st}}{\longleftarrow} 
  L_2 R_2 (\Sigma X) 
    \underoverset{\in Iso \subset W_{st}}{L\tau}{\longrightarrow}
  L_2 R_2 (X \wedge S^1)
    \underset{\in W_{st}}{\longrightarrow}
  X \wedge S^1
  \,.
$$

So restricted to $X$ a cofibrant-object, this gives a natural isomorphism $\Sigma X \to X \wedge S^1$ in the [[stable homotopy category]] $Ho(SeqSpec(Top_{cg})_{stable})$.

=--



+-- {: .num_lemma #FakeSuspensionInducesEquivalenceOfHomotopyCategories}
###### Lemma

The total [[derived functor]] of the alternative suspension operation $\Sigma$ of def. \ref{SequentialSpectrumFakeSuspension} exists and constitutes an [[equivalence of categories]] from the [[stable homotopy category]] to itself:

$$
  \Sigma
  \;\colon\;
  Ho(SeqSpec(Top)_{stable})
   \overset{\simeq}{\longrightarrow}
  Ho(SeqSpec(Top)_{stable})
  \,.
$$


=--

+-- {: .proof}
###### Proof

The total derived functor of $\Sigma$ exists because by prop. \ref{FakeLoopingPreservesOmegaSpectra} $\Sigma$ preserves stable equivalences. Also the shift functor $[-1]$ from def. \ref{ShiftedSpectrum} clearly preserves stable equivalences, hence both descend to the homotopy category. 
There, by prop. \ref{CounitOfFakeSuspensionAndShiftIsStableEquivalence}
and remark \ref{ShiftingCommutesWithLoopingAndSuspensionOfSequentialSpectra}, they are inverses of each other, up to isomorphism.

=--

+-- {: .num_lemma #StandardSuspensionOfSequentialSpectraRepresentsCanonicalSuspension}
###### Lemma

The canonical suspension functor on the [[homotopy category of a model category|homotopy category]] of any [[model category]] (from [this prop.](Introduction+to+Stable+homotopy+theory+--+P#LoopingAsFunctorOnHomotopyCategory)) in the case of the [[stable homotopy category]] (def. \ref{TheStableHomotopyCategory}) $Ho(Spectra) = Ho(SeqSpec(Top_{cg})_{stable})$ is represented by the "standard suspension" operation of def. \ref{SequentialSpectrumRealSuspension}.

=--

+-- {: .proof}
###### Proof

By [[CW-approximation]] (prop. \ref{CWApproximationForSequentialSpectra}), every object in the stable homotopy category is represented by a [[CW-spectrum]]. 
By prop. \ref{CylinderSpectrumOverCWSpectrumIsGood}, on [[CW-spectra]] the canonical suspension functor on the homotopy category (from [this prop.](Introduction+to+Stable+homotopy+theory+--+P#LoopingAsFunctorOnHomotopyCategory)) is represented by the "standard suspension" operation of def. \ref{SequentialSpectrumRealSuspension}. 

=--

+-- {: .num_theorem #StableModelStructureOnSequentiaSpectraIsStableModelCategory}
###### Theorem

The stable model structure $SeqSpec(Top)_{stable}$ from theorem \ref{StableModelStructureOnSequentialSpectraIsModelCategory} indeed gives a [[stable model category]] (def. \ref{StableModelCategory}) in that the canonically induced [[reduced suspension]] functor ([prop. ](Introduction+to+Stable+homotopy+theory+--+P#LoopingAsFunctorOnHomotopyCategory)) on its [[homotopy category of a model category|homotopy category]] is an [[equivalence of categories]]

$$
  \Sigma 
    \;\colon\;
  Ho(SeqSpec(Top)_{stable})
   \overset{\simeq}{\longrightarrow}
  Ho(SeqSpec(Top)_{stable})
  \,.
$$


=--

+-- {: .proof}
###### Proof

By lemma \ref{StandardSuspensionOfSequentialSpectraRepresentsCanonicalSuspension}, the canonical suspension functor is represented, on fibrant-cofibrant objects, by the standard suspension functor of def. \ref{SequentialSpectrumRealSuspension}.
By prop. \ref{IsomorphismBetweenStandardAndAlternativeSuspensionInHomotopyCategory} however, this is naturally isomorphic -- on the level of the homotopy category -- to the alternative suspension operation of def. \ref{SequentialSpectrumFakeSuspension}. Therefore the claim follows with prop. \ref{FakeSuspensionInducesEquivalenceOfHomotopyCategories}.

=--

In fact this lifts to a Quillen equivalence:

+-- {: .num_prop #AlternativeLoopingAndSuspensionIsQuillenEquivalenceOnStableModelStructure}
###### Proposition

The $(\Sigma \dashv \Omega)$-[[adjunction]] from prop. \ref{AdjunctionsBetweenLoopingAndDeloopingForSeqSpec} is a [[Quillen equivalence]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#QuillenEquivalence)) with respect to the stable model structure of theorem \ref{StableModelStructureOnSequentialSpectraIsModelCategory}:

$$
  SeqSpec(Top_{cg})_{stable}
    \underoverset
     {\underset{\Omega}{\longrightarrow}}
     {\overset{\Sigma}{\longleftarrow}}
     {\simeq_{\mathrlap{Q}}}
  SeqSpec(Top_{cg})_{stable}
  \,.
$$

Its [[derived functors]] ([prop.](Introduction+to+Stable+homotopy+theory+--+P#QuillenAdjunctionInducesAdjunctionOnHomotopyCategories)) exhibit the canonical [[reduced suspension]] and looping operation as an [[adjoint equivalence]] on the [[stable homotopy category]]

$$
  Ho(Spectra)
    \underoverset
     {\underset{\Omega}{\longrightarrow}}
     {\overset{\Sigma}{\longleftarrow}}
     {\simeq}
  Ho(Spectra)
  \,.
$$


=--

+-- {: .proof}
###### Proof

By prop. \ref{AlternativeSuspensionIsLeftQuillenOnStrictModelStructureOnSequential} and the fact that the stable model structure has the same cofibrations as the strict model structure,  $\Sigma$ preserves stable cofibrations. Moreover, by lemma \ref{FakeLoopingPreservesOmegaSpectra} $\Sigma$ preserves in fact all stable weak equivalences. Hence $\Sigma$ is a left Quillen functor and so $(\Sigma \dashv \Omega)$ is a [[Quillen adjunction]].
Finally lemma \ref{FakeSuspensionInducesEquivalenceOfHomotopyCategories} gives that this Quillen adjunction is a Quillen equivalence.

=--

In summary, this concludes the characterization of the [[stable homotopy category]] as the result of stabilizing the canonical $(\Sigma \dashv \Omega)$-adjunction on the [[classical homotopy category]]:

+-- {: .num_cor #StableHomotopyCategoryIsIndeedStabilizationOfClassicalHomotopyCategory}
###### Corollary

The [[classical model structure on pointed topological spaces|classical model structure]] $(Top^{\ast/}_{cg})_{Quillen}$ on [[pointed topological space|pointed]] [[compactly generated topological spaces]] ([thm.](Introduction+to+Stable+homotopy+theory+--+P#ClassicalModelStructureOnCompactlyGeneratedTopologicalSpaces), [prop.](Introduction+to+Stable+homotopy+theory+--+P#ModelStructureOnSliceCategory)) and the stable [[model structure on topological sequential spectra]] $SeqSpec(Top_{cg})$ (theorem \ref{StableModelStructureOnSequentialSpectraIsModelCategory}) sit in a [[commuting diagram]] of [[Quillen adjunctions]] of the form

$$
  \array{
     (Top_{cg}^{\ast/})_{Quillen}
      &
      \underoverset{\underoverset{\Omega}{\bot}{\longrightarrow}}{\overset{\Sigma}{\longleftarrow}}{} 
      &
     (Top^{\ast/}_{cg})_{Quillen}
     \\
     {}^{\mathllap{\Sigma^\infty}}\downarrow \dashv \uparrow^{\mathrlap{\Omega^\infty}}
     &&
     {}^{\mathllap{\Sigma^\infty}}\downarrow \dashv \uparrow^{\mathrlap{\Omega^\infty}}
     \\
     SeqSpec(Top_{cg})_{strict}
     &
     \underoverset
       {\underset{\Omega}{\longrightarrow}}
       {\overset{\Sigma}{\longleftarrow}}
       {\bot}
     &
     SeqSpec(Top_{cg})_{strict}
     \\
     {}^{\mathllap{id}}\downarrow \dashv \uparrow^{\mathrlap{id}}
     &&
     {}^{\mathllap{id}}\downarrow \dashv \uparrow^{\mathrlap{id}}
     \\
     SeqSpec(Top_{cg})_{stable}
     &
     \underoverset
       {\underset{\Omega}{\longrightarrow}}
       {\overset{\Sigma}{\longleftarrow}}
       {\simeq_{\mathrlap{Q}}}
     &
     SeqSpec(Top_{cg})_{stable}
  }
  \,,
$$

where the top parts is from corollary \ref{SuspensionLoopingAdjunctionSystemForStrictModelStructure}, the bottom vertical Quillen adjunction is the [[Bousfield localization of model categories|Bousfield localization]] of theorem \ref{StableModelStructureOnSequentialSpectraIsModelCategory} and the bottom horizontal adjunction is the [[Quillen equivalence]] of prop. \ref{AlternativeLoopingAndSuspensionIsQuillenEquivalenceOnStableModelStructure}.

Hence (by [this prop.](Introduction+to+Stable+homotopy+theory+--+P#QuillenAdjunctionInducesAdjunctionOnHomotopyCategories)) the [[derived functors]] of the functors in this diagram yield a commuting square of [[adjoint functors]] between the [[classical homotopy category]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#ClassicalHomotopyCategory)) and the [[stable homotopy category]] (def. \ref{TheStableHomotopyCategory}) of the form

$$
  \array{
    Ho(Top^{\ast/})
    &
      \underoverset
        {\underset{\Omega}{\longrightarrow}}
        {\overset{\Sigma}{\longleftarrow}}
        {\bot}
    &
    Ho(Top^{\ast/})
    \\
    {}^{\mathllap{\Sigma^\infty}}\downarrow \dashv \uparrow^{\mathrlap{\Omega^\infty}}
    &&
    {}^{\mathllap{\Sigma^\infty}}\downarrow \dashv \uparrow^{\mathrlap{\Omega^\infty}}
    \\
    Ho(Spectra)
    &
      \underoverset
        {\underset{\Omega}{\longrightarrow}}
        {\overset{\Sigma}{\longleftarrow}}
        {\simeq}
    &
    Ho(Spectra)
  }
  \,,
$$

and here the horizontal adjunctions are the canonically induced (via [this prop.](Introduction+to+Stable+homotopy+theory+--+P#LoopingAsFunctorOnHomotopyCategory))suspension/looping functors by prop. \ref{SuspensionAndLoopAdjunctionInClassicalHomotopyTheory} and by lemma \ref{StandardSuspensionOfSequentialSpectraRepresentsCanonicalSuspension} and theorem \ref{StableModelStructureOnSequentiaSpectraIsStableModelCategory}.

=--


##### Cofibrant generation

We construct another [[Bousfield localization of model categories|Bousfield localization]] of $SeqSpec(Top_{cg})_{strict}$, one that manifestly yields a [[cofibrantly generated model category]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#CofibrantlyGeneratedModelCategory)). Theorem \ref{StableEquivalencesOfSequentialSpectraAgreeWithStableWeakHomotopyEquivalences} below states that in fact this model structure coincides with the stable model structure from theorem \ref{StableModelStructureOnSequentialSpectraIsModelCategory}, thereby providing generating (acyclic) cofibrations for the latter.


+-- {: .num_defn #ClassesOfMorphismsOfTheStableModelStructureOnSequentialSpectra}
###### Definition

Say that a homomorphism $f_\bullet \colon X_\bullet \to Y_\bullet$ in the category $SeqSpec(Top_{cg})$, def. \ref{SequentialSpectra} is

* a **stable weak equivalence** if for all [[Omega-spectra]] $E$ the morphism $[f,E]_{strict}$ is a [[bijection]] 

  (where $[-,E]_{strict}$ is the [[hom-functor]] of the [[homotopy category of a model category|homotopy category]] $Ho(SeqSpec(Top_{cg})_{strict})$ ([def.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyCategoryOfAModelCategory)) of the strict model structure of theorem \ref{StrictModelStructureOnSequentialPrespectraIsModelCategory}.

* a **stable cofibration** if it is a strict cofibation (def. \ref{ClassesOfMorphismsOfTheStrictModelStructureOnSequentialSpectra}) hence if the 0th component map $f_0\colon X_0 \to Y_0$ as well as all  

  $$
    (f_{n+1}, \sigma^Y_n)
      \;\colon\;
    X_{n+1}\underset{S^1 \wedge X_n}{\sqcup} S^1 \wedge Y_n
      \longrightarrow
    Y_{n+1}
  $$

  are cofibrations in the [[classical model structure on topological spaces]] (i.e.: [[retracts]] of [[relative cell complexes|relative cell complex inclusions]] ([thm.](Introduction+to+Stable+homotopy+theory+--+P#TopQuillenModelStructure), [thm.](Introduction+to+Stable+homotopy+theory+--+P#ClassicalModelStructureOnCompactlyGeneratedTopologicalSpaces))).

=--

In order for def. \ref{ClassesOfMorphismsOfTheStableModelStructureOnSequentialSpectra} to possibly give a [[Bousfield localization of model categories]] (def. \ref{BousfieldLocalizationOfModelCategories}) we need to verify the following:

+-- {: .num_lemma #StableWeakHomotopyEquivalenceInSeqSpecIsStableEquivalence}
###### Lemma

Every [[stable weak homotopy equivalence]] of sequential spectra (def. \ref{StableWeakHomotopyEquivalenceOfSequentialTopologicalSpectra}) is a stable weak equivalence in the sense of def. \ref{ClassesOfMorphismsOfTheStableModelStructureOnSequentialSpectra}.
 
=--

+-- {: .proof}
###### Proof

Let $E$ be an Omega-spectrum (def. \ref{OmegaSpectrum}). Then by the third item of lemma \ref{PropertiesOfSpectrificationForTopologicalSequentialSpectra}, for every $X$ the morphism obtained by homming $X$ into the [[spectrification]] $j_E$ (def. \ref{SpectrificationForTopologicalSequentialSpectra})

$$
  [X,j_E]_{strict}
    \;\colon\; 
  [X,E]_{strict} 
    \longrightarrow 
  [X, Q E]_{strict}
$$

is an isomorphism. Since $j_{(-)}$ is a [[natural transformation]] (by def. \ref{SpectrificationForTopologicalSequentialSpectra}), the naturality squares give a factorization of this morphism as

$$
  [X,j_E]_{strict}
    \;\colon\;
  [X,E]_{strict} 
    \stackrel{Q}{\longrightarrow}
  [Q X, Q E]_{strict}
    \stackrel{[j_X,E]_{strict}}{\longrightarrow}
  [X, Q]_{strict}  
  \,.
$$

Combining this with vertical morphisms as below, which are isomorphisms again by item 3 of lemma \ref{PropertiesOfSpectrificationForTopologicalSequentialSpectra},

$$
  \array{
     &
      &&
    [Q X, E]_{strict}
      &\stackrel{[j_X, E]_{strict}}{\longrightarrow}&
    [X, E]_{strict}  
    \\
    & &\nearrow& 
    {}^{\mathllap{\simeq}}\downarrow^{\mathrlap{[Q X, j_E]_{strict}}} 
     && 
    {}^{\mathllap{\simeq}}\downarrow^{\mathrlap{[X, j_E]_{strict}}}
    \\
    [X, j_E]_{strict}
      \;\colon\;
     &
    [X,E]_{strict} 
      &\stackrel{Q}{\longrightarrow}&
    [Q X, Q E]_{strict}
      &\stackrel{[j_X, Q E]_{strict}}{\longrightarrow}&
    [X, Q E]_{strict}  
  }
$$

exhibits a [[retraction]] 

$$
  id \;\colon\; [X,E]_{strict} \longrightarrow [Q X,E]_{strict} \longrightarrow [X,E]_{strict}
  \,,
$$ 

which is natural in $X$ (that the bottom and right composite is indeed the identity is again due to the naturality of $j_{(-)}$). This naturality now implies a retraction of morphisms

$$
  \array{
    id_{[Y,E]_{strict}} \colon & [Y,E]_{strict} &\longrightarrow& [Q Y,E]_{strict} &\longrightarrow& [Y,E]_{strict}
    \\
    & \downarrow^{\mathrlap{[f,E]_{strict}}} && \downarrow^{\mathrlap{[Q f,E]_{strict}}}
     &&
     \downarrow^{\mathrlap{[f,E]_{strict}}}
    \\
    id_{[X,E]_{strict}} \colon & [X,E]_{strict} &\longrightarrow& [Q X,E]_{strict} &\longrightarrow& [X,E]_{strict}
  }
  \,.
$$

Finally, by the fourth item of lemma \ref{PropertiesOfSpectrificationForTopologicalSequentialSpectra}, the middle vertical morphism here is an isomorphism, hence $[f^\ast, E]_{strict}$ is the retract of an iso and hence ([prop.](retract#RetractOfIso)) an isomorphism itself, for all Omega-spectra $E$. This means by definition that $f$ is a stable equivalence.

=--


In order to show that a model structure with classes of morphisms as in def. \ref{ClassesOfMorphismsOfTheStableModelStructureOnSequentialSpectra} indeed exists, we will provide generating (acyclic) cofibrations ([def.](Introduction+to+Stable+homotopy+theory+--+P#CofibrantlyGeneratedModelCategory)). In order to express these, we need the following simple but important concept.

+-- {: .num_defn #FreeSequentialSpectra}
###### Definition

For $K \in Top_{cg}^{\ast/}$, and $n \in \mathbb{N}$, write $F_n K \in SeqSpec(Top_{cg})$ for the **[[free spectrum]]** on $K$ at $n$, with components

$$
  (F_n K)_q \coloneqq 
  \left\{
    \array{
      \ast & for \; q \lt n
      \\
      S^{q-n} \wedge K & for \; q \geq n
    }
  \right.
$$

and with structure maps $\sigma_q$ the canonical identifications for $q \geq n$

$$
  \sigma_q
  \;\colon\;
  S^1 \wedge (F_n K)_q
  = 
  S^1 \wedge S^{q-n} \wedge K
  \overset{\simeq}{\longrightarrow}
  S^{q+1-n} \wedge K
  =
  (F_n K)_{q+1}
  \,.
$$

For $n \in \mathbb{N}$, write

$$
  k_n
  \;\colon\;
  F_{n+1}S^1 
  \longrightarrow
  F_n S^0
$$

for the canonical morphisms of free sequential spectra with the following components

$$
  \array{
    & \vdots && \vdots
    \\
    (k_n)_{n+3} & S^3 &\stackrel{id}{\longrightarrow}& S^3
    \\
    (k_n)_{n+2} & S^2 &\stackrel{id}{\longrightarrow}& S^2
    \\
    (k_n)_{n+1} & S^1 &\stackrel{id}{\longrightarrow}& S^1
    \\
    (k_n)_n \colon & \ast &\stackrel{0}{\longrightarrow}& S^0
    \\
    & \ast &\longrightarrow& \ast
    \\
    & \vdots && \vdots
    \\
    & \ast &\longrightarrow& \ast
    \\
    & \underbrace{\,\,\,} && \underbrace{\,\,\,}
    \\
    k_n \colon & F_{n+1} S^1 &\stackrel{}{\longrightarrow}& F_n S^0
  }
$$

=--

+-- {: .num_example}
###### Example

The free spectrum $F_0 S^0$ (def. \ref{FreeSequentialSpectra}) is the standard sequential [[sphere spectrum]] from def. \ref{StandardSphereSpectrum}

$$
  F_0 S^0 \simeq \mathbb{S}_{std}
  \,.
$$

Generally the free spectrum $F_0 K$ is the [[suspension spectrum]] (def. \ref{SuspensionSpectrum}) on $K$:

$$
  F_0 K \simeq \Sigma^\infty K
  \,.
$$

=--

Just as forming suspension spectra is left adjoint to extracting the 0th component space of a sequential spectrum (prop. \ref{SigmaInfinityOmegaInfinity}), so forming the $n$th free spectrum is left adjoint to extracting the $n$th component space:

+-- {: .num_prop #LeftAdjointnessOfFreeSpectrum}
###### Proposition

For $n \in \mathbb{N}$, let

$$
  Ev_n 
    \;\colon\;
  SeqSpec(Top_{cg})
    \longrightarrow
  Top_{cg}^{\ast/}
$$

be the functor from [[sequential spectra]] (def. \ref{SequentialSpectra}) to [[pointed topological spaces]] given by extracting the $n$th component space

$$
  Ev_n(X) \coloneqq X_n
  \,.
$$

Then this functor is [[right adjoint]] to forming $n$th free spectra (def. \ref{FreeSequentialSpectra}):

$$
  (F_n \dashv Ev_n)
  \;\colon\;
  SeqSpec(Top_{cg})
    \underoverset
      {\underset{Ev_n}{\longrightarrow}}
      {\overset{F_n}{\longleftarrow}}
      {\bot}
  Top_{cg}^{\ast/}
  \,.
$$

=--

+-- {: .proof}
###### Proof

The proof is verbatim as that of prop. \ref{SigmaInfinityOmegaInfinity}, just with $n$ zeros inserted at the bottom of the sequences of components maps.

=--



+-- {: .num_defn #GeneratingAndGeneratingAcyclicCofibrationsForSeqSpecStable}
###### Definition

Write 

$$
  I_{SeqSpec}^{stable} 
    \coloneqq 
  I_{SeqSpec}^{strict}
  \;\;
  \in SeqSpec(Top)
$$

for the set of morphisms appearing already in def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForSeqSpecStrict}, and write

$$
  J_{SeqSpec}^{stable}
    \coloneqq 
  J_{SeqSpec}^{strict}
   \;\sqcup\:
  \{
    k_n \Box i_+
  \}_{n \in \mathbb{N},i_+ \in \left(I_{Top^{\ast/}}\right)}
$$

for the [[disjoint union]] of the other set of morphisms appearing in def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForSeqSpecStrict} with the set $ \{k_n \Box i_+\}_{n,i_+}$ of [[pushout-products]] under smash tensoring (according to def. \ref{PushoutProductWithRespectToSmashTensoring}) of the morphisms $k_n$ from def. \ref{FreeSequentialSpectra} with the generating cofibrations of the [[classical model structure on pointed topological spaces]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#GeneratingCofibrationsForPointedTopologicalSpaces)).

=--


+-- {: .num_theorem #AlternativeStableModelStructureOnSequentialSpectraIsModelCategory}
###### Theorem

The classes of morphisms in def. \ref{ClassesOfMorphismsOfTheStableModelStructureOnSequentialSpectra} give the structure of a [[model category]] $SeqSpec(Top)_{stable}$, called the **stable [[model structure on topological sequential spectra]]**. Moreover:

1. its fibrant objects are precisely the [[Omega-spectra]] (def. \ref{OmegaSpectrum});

1. it is a [[cofibrantly generated model category]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#CofibrantlyGeneratedModelCategory)) with generating (acyclic) cofibrations the sets $I_{SeqSpec}^{stable}$ (and $J_{SeqSpec}^{stable}$) from def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForSeqSpecStable};

1. the identity functors

   $$
     SeqSpec(Top_{cg})_{stable}
      \underoverset
       {\underset{id}{\longrightarrow}}
       {\overset{id}{\longleftarrow}}
       {\bot}
     SeqSpec(Top_{cg})_{strict}
   $$

   constitute a [[Quillen adjunction]] exhibiting the stable model structure as a [[Bousfield localization of model categories|left Bousfield localization]] (def. \ref{BousfieldLocalizationOfModelCategories}) of the strict model structure from theorem \ref{StrictModelStructureOnSequentialPrespectraIsModelCategory}.


=--

This is one of the four model categories considered in ([Mandell-May-Schwede-Shipley 01](#MMSS00)) .



We **prove** theorem \ref{AlternativeStableModelStructureOnSequentialSpectraIsModelCategory} [below](#ProofOfTheStableModelStructureOnSequentialSpectra), after proving various lemmas.


+-- {: .num_lemma #CorepresentationOfAdjunctStructureMaps}
###### Lemma

The morphisms of [[free spectra]] $\{k_n\}_{n \in \mathbb{N}}$ from def. \ref{FreeSequentialSpectra} co-represent the adjunct structure maps of sequential spectra from def. \ref{SequentialSpectrumViaAdjunctStructureMaps}, in that for $X \in SeqSpec(Top_{cg})$, then 

$$
  \array{
    SeqSpec(F_n S^0, X) &\simeq& X_n
    \\
    {}^{\mathllap{SeqSpec(k_n,X)}}\downarrow && \downarrow^{\mathrlap{\tilde \sigma_n^X}}
    \\
    SeqSpec(F_{n+1}S^1, X) &\simeq& \Omega X_{n+1}
  }
  \,,
$$

where on the left we have the [[hom-spaces]] of def. \ref{PushoutProductOfspectrumWithSpaceInteractingWithHomSpaces},
and where the horizontal equivalences are via prop. \ref{LeftAdjointnessOfFreeSpectrum}.

=--

+-- {: .proof}
###### Proof

Recall that we are precomposing with

$$
  \array{
    & \vdots && \vdots
    \\
    (k_n)_{n+3} & S^3 &\stackrel{id}{\longrightarrow}& S^3
    \\
    (k_n)_{n+2} & S^2 &\stackrel{id}{\longrightarrow}& S^2
    \\
    (k_n)_{n+1} & S^1 &\stackrel{id}{\longrightarrow}& S^1
    \\
    (k_n)_n \colon & \ast &\stackrel{0}{\longrightarrow}& S^0
    \\
    & \ast &\longrightarrow& \ast
    \\
    & \vdots && \vdots
    \\
    & \ast &\longrightarrow& \ast
    \\
    & \underbrace{\,\,\,} && \underbrace{\,\,\,}
    \\
    k_n \colon & F_{n+1} S^1 &\stackrel{}{\longrightarrow}& F_n S^0
  }
$$


Now for $X$ any sequential spectrum, then a morphism $f \colon F_n S^0 \to X$ is uniquely determined by its $n$th component $f_n \colon S^0 \to X_n$: the compatibility with the structure maps forces the next component, in particular, to be $\sigma_n^X\circ \Sigma f$:

$$
  \array{
    \Sigma S^0 &\stackrel{\Sigma f}{\longrightarrow}& \Sigma X_n
    \\
    \downarrow^{\mathrlap{\simeq}} && \downarrow^{\mathrlap{\sigma_n^X}}
    \\
    S^1 &\stackrel{\sigma_n^X \circ \Sigma f}{\longrightarrow}& X_n
  }
  \,.
$$

But that $(n+1)$st component is just the component that similarly determines the precompositon of $f$ with $k_n$, hence $f\circ k_n$ is uniquely determined by the map $\sigma_n^X \circ \Sigma f$. Therefore $SeqSpec(k_n,-)$ is the function

$$
  SeqSpec(k_n,-)
   \;\colon\;
  X_n 
   = 
  SeqSpec(S^0, X_n)
    \stackrel{f \mapsto \sigma_n^X \circ \Sigma f}{\longrightarrow}
  \Maps(S^1, X_{n+1})_\ast
   =
  \Omega X_{n+1}
  \,.
$$

It remains to see that this is indeed the $(\Sigma \dashv \Omega)$-[[adjunct]] of $\sigma_n^X$. By the general formula for [[adjuncts]], this is

$$
  \tilde \sigma_n^X 
    \;\colon\; 
  X_n 
     \stackrel{\eta}{\longrightarrow} 
  \Omega \Sigma X_n
     \stackrel{\Omega \sigma_n^X}{\longrightarrow}
  \Omega X_{n+1}
  \,.
$$

To compare to the above, we check what this does on points: $S^0 \stackrel{f}{\longrightarrow} X_n$ is sent to the composite

$$
   S^0 
     \stackrel{f}{\longrightarrow}
   X_n 
     \stackrel{\eta}{\longrightarrow} 
   \Omega \Sigma X_n
     \stackrel{\Omega \sigma_0^X}{\longrightarrow}
   \Omega X_{n+1}
   \,.
$$

To identify this as a map $S^1 \to X_{n+1}$, we use the adjunction isomorphism once more to throw all the $\Omega$-s on the right back to $\Sigma$-s the left, to finally find that this is indeed

$$
  \sigma_n^X \circ \Sigma f
    \;\colon\;
  S^1 = \Sigma S^0 \stackrel{\Sigma f}{\longrightarrow} \Sigma X_n \stackrel{\sigma_n^X}{\longrightarrow} X_{n+1}
  \,.
$$

=--


+-- {: .num_lemma #StableEquivalencesBetweenOmegaSpectraAreStrictWeakEquivalencesForSequentialSpectra}
###### Lemma

1. Every weak equivalence with respect to the strict model structure (def. \ref{ClassesOfMorphismsOfTheStrictModelStructureOnSequentialSpectra}) is a stable weak equivalence (def. \ref{ClassesOfMorphismsOfTheStableModelStructureOnSequentialSpectra}): $W_{strict} \subset W_{stable}$

1. Every stable weak equivalence between [[Omega-spectra]] (def. \ref{OmegaSpectrum}) is a weak equivalence in the strict model structure.

=--

+-- {: .proof}
###### Proof

The first statement follows directly from  the definition of stable weak equivalences, since weak equivalences become isomorphisms in the [[homotopy category of a model category|homotopy category]] ([thm.](Introduction+to+Stable+homotopy+theory+--+P#UniversalPropertyOfHomotopyCategoryOfAModelCategory)).

For the second statement, let $f \colon X \to Y$ be a stable weak equivalence between [[Omega-spectra]]. Then by definition, in particular

$$
  [f,X]_{strict} \;\colon\; [Y,X]_{strict} \longrightarrow [X,X]_{strict}
$$

is a [[bijection]]. Therefore the pre-image of $[id_X] \in [X,X]_{strict}$ is an inverse to $f$ in the [[homotopy category]] of the strict model structure. Hence $f$ represents an isomorphism in the strict homotopy category and is hence a weak equivalence in the strict model structure.

=--


+-- {: .num_lemma #ElementsOfKAreStableEquivalencesAndStrictCofibrationsForSequentialSpectra}
###### Lemma

Every element in $J_{SeqSpec}^{stable}$ (def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForSeqSpecStable}) is both:

1. a stable cofibration,

1. a stable equivalence

hence a stable acylic cofibration according to def. \ref{ClassesOfMorphismsOfTheStableModelStructureOnSequentialSpectra}.

=--

+-- {: .proof}
###### Proof 

For the elements in $J_{SeqSpec}^{strict}$ this is part of theorem \ref{StrictModelStructureOnSequentialPrespectraIsModelCategory}.
It only remains to see that the morphisms $k_n \Box i_+$ are stable acyclic cofibrations.

To see that the $k_n \Box i_+$ are strict cofibrations: By [[Joyal-Tierney calculus]] ([prop.](Introduction+to+Stable+homotopy+theory+--+P#JoyalTierneyCalculus)) $k_n \Box i_+$ has left lifting against any acyclic strict fibration $f$ precisely if $k_n$ has left lifting against the pullback powering $f^{\Box i_+}$ (def. \ref{PushoutProductWithRespectToSmashTensoring}). By prop. \ref{PushoutProductWithRespectToSmashTensoringSatisfiesEnrichedModelCategoryAxioms} the latter is still a strict acyclic fibration. Since $k_n$ is evidently a strict cofibration, the lifting follows and hence also $k_n \Box i_+$ is a strict cofibration.


To see that the $k_n \Box i_+$ are stable equivalences: 

First observe that $k_n$ itself is a stable equivalence, since for $E$ any Omega-spectrum then using prop. \ref{ConnectedComponentOfHomSpaceOfSeqentialSpectraLeftHomotopyClasses} and lemma \ref{CorepresentationOfAdjunctStructureMaps} we have

$$
  \begin{aligned}
    [k_n,E]_{strict} 
      & \simeq 
    \pi_0 SeqSpec(k_n,E)
    \\
    &\simeq \pi_0 \tilde \sigma^E_n
  \end{aligned}
$$

and the last map is an isomorphism by definition of Omega-spectra.

Next, use in addition prop. \ref{PushoutProductOfspectrumWithSpaceInteractingWithHomSpaces} to similarly deduce that

$$
  \begin{aligned}
    [k_n \Box i_+, E]_{strict}
    & \simeq
    \pi_0 SeqSpec(k_n \Box i_+, E)
    \\
    & \simeq \pi_0 \left(SeqSpec(k_n,E)^{\Box i_+}\right)
  \end{aligned}
  \,.
$$

Now $SeqSpec(k_n,E)^{\Box id}$ is a weak homotopy equivalence by prop. \ref{CorepresentationOfAdjunctStructureMaps} and because $E$ is an Omega-spectrum, while $id^{\Box i_+}$ is a Serre fibration by the topological enrichment of $Top_{cg}^{\ast/}$ ([prop.](Introduction+to+Stable+homotopy+theory+--+P#PushoutProductInTopCGSendsCofCofToCof)). This means that the [[pullback]] that enters the construction of the pullback powering $SeqSpec(k_n,E)^{\Box i_+}$ is of a weak equivalence along a fibration in the [[classical model structure on pointed topological spaces]], all whose objects are fibrant. Such pullbacks preserve weak equivalences ([lemma](Introduction+to+Stable+homotopy+theory+--+P#InCfPullbackAlongFibrationPreservesWeakEquivalences)). Hence by [[two-out-of-three]] it follows that also the pullback powering $SeqSpec(k_n,E)^{\Box i_+}$ is a weak homotopy equivalence, hence that $\pi_0 \left(SeqSpec(k_n,E)^{\Box i_+}\right)$ is an isomorphism.

=--


The reason for considering the set $\{k_n \Box i_+\}$ is to make the following true:

+-- {: .num_lemma #KInjectivesAreAcyclicCofibrationsForSequentialSpectra}
###### Lemma

A morphism $f \colon X \to Y$ in $SeqSpec(Top)$ is a $J_{SeqSpec}^{stable}$-[[injective morphism]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#LiftingAndExtension)) precisely if 

1. it is fibration in the strict model structure (hence degreewise a fibration);

1. for all $n \in \mathbb{N}$ the [[commuting squares]] of structure map compatibilities on the underlying [[sequential spectra]] 

   $$
     \array{
       X_n  &\overset{\tilde\sigma^X_n}{\longrightarrow}& \Omega X_{n+1}
       \\
       {}^{\mathllap{f_n}}\downarrow && \downarrow^{\mathrlap{\Omega f_{n+1}}}
       \\
       Y_n &\underset{\tilde \sigma^Y_n}{\longrightarrow}& \Omega Y_{n+1}
     }
   $$

   exhibit [[homotopy pullbacks]], in that the comparison map

   $$
      X_n \longrightarrow Y_n \underset{\Omega Y_{n+1}}{\times} \Omega X_{n-1}
   $$

   is a weak homotopy equivalence (notice that $\Omega f_{n+1}$ is a fibration by the previous item and since $\Omega = Maps(S^1,-)_\ast$ is a right Quillen functor by prop. \ref{SuspensionAndLoopAdjunctionInClassicalHomotopyTheory}).


In particular, the $J_{SeqSpec}^{stable}$-[[injective objects]] are precisely the [[Omega-spectra]], def. \ref{OmegaSpectrum}.


=--

+-- {: .proof}
###### Proof

By theorem \ref{StrictModelStructureOnSequentialPrespectraIsModelCategory}, lifting against $J_{SeqSpec}^{stric}$ alone characterizes strict fibrations, hence degreewise fibrations. Lifting against the remaining [[pushout product]] morphism $k_n \Box i_+$ is, by [[Joyal-Tierney calculus]] ([prop.](Introduction+to+Stable+homotopy+theory+--+P#JoyalTierneyCalculus)), equivalent to left lifting $i_+$ against the pullback powering $f^{\Box k_n}$ from def. \ref{PushoutProductWithRespectToSmashTensoring}. Since the $\{i_+\}$ are the generating cofibrations in $Top_{cg}^{\ast/}$  such lifting means that $f^{\Box k_n}$ is a weak homotopy equivalence. But by lemma \ref{CorepresentationOfAdjunctStructureMaps}, $f^{\Box k_n}$ is precisely the comparison morphism in question.

=--


+-- {: .num_lemma #KInjectiveStableEquivalencesAreStrictEquivalencesForSequentialSpectra}
###### Lemma

A morphism in $SeqSpec(Top)$ which is both 

1. a stable weak equivalence (def. \ref{ClassesOfMorphismsOfTheStableModelStructureOnSequentialSpectra});

1. a $J_{SeqSpec}^{stable}$-[[injective morphism]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#LiftingAndExtension))

(according to def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForSeqSpecStable}) is an acyclic fibration in the strict model structure, hence is degreewise a [[weak homotopy equivalence]] and [[Serre fibration]] of topological spaces;

=--


+-- {: .proof}
###### Proof

Let $f \colon X \to B$ be both a stable equivalence as well as a $K$-injective morphism. Since $K$ contains the generating acyclic cofibrations for the strict model structure (prop. \ref{StrictModelStructureOnDiagramSpectra}), $f$ is in particular a strict fibration, hence a degreewise fibration. 

Consider the fiber $F$ of $f$, hence the morphism $F \to \ast$ which is the pullback of $f$ along $\ast \to B$. We claim that 

1. $F$ is an Omega-spectrum;

1. $F\to \ast$ is a stable weak equivalence. 

The first item follows since $F$, being the pullback of a $K$-injective morphisms, is a $K$-[[injective object]] ([prop.](Introduction+to+Stable+homotopy+theory+--+P#ClosurePropertiesOfInjectiveAndProjectiveMorphisms)), so that, by lemma \ref{KInjectivesAreAcyclicCofibrationsForSequentialSpectra}, $F$ it is an Omega-spectrum. 

For the second item: By theorem \ref{StableModelStructureOnSequentialSpectraIsModelCategory} it follows that for $E$ an Omega-spectrum and $X$ any sequential spectrum, then the [[hom-sets]] in the [[homotopy category of a model category|homotopy category]] of the strict model structure from $X$ into $E$ [[natural transformation|naturally]] coincide with those for the stable model structure:

$$
  [X,E]_{strict} \simeq [X,E]_{stable}
  \,.
$$

But for the stable model structure we have (prop. \ref{LongFiberSequencesOfMapsOfSpectra}) that these hom-groups sit in [[long exact sequences]] of the form

$$
  \cdots
    \to 
  [Y,E] 
    \overset{[f,E]}{\longrightarrow}
  [X,E]
    \longrightarrow 
  [F,E]
    \longrightarrow
  [\Omega Y,E] 
    \overset{[f,E]}{\longrightarrow}
  [\Omega X,E]
    \to
  \cdots
$$

Now since $[f,E]$ is an isomorphism for all Omega-spectra $E$, by assumption, hence an isomorphism in the stable model structure, so that also $\Omega f$ is an isomorphism, the exactness of this sequence means that that $[F,E] \simeq \ast$, hence that 

$$
  \ast \simeq [\ast,E]\overset{\simeq}{\longrightarrow} [F,E]
$$

for all Omega-spectra $E$, hence that $F \to \ast$ is a stable weak equivalence. This establishes the second property above.

Now with prop. \ref{StableEquivalencesBetweenOmegaSpectraAreStrictWeakEquivalencesForSequentialSpectra} these two properties imply that $F \to \ast$ is already a weak equivalence in the strict model structure. From this the [[long exact sequence of homotopy groups]] ([exmpl.](Introduction+to+Stable+homotopy+theory+-+P#LongExactSequeceOfHomotopyGroups)) implies that $\pi_{\bullet \geq 1}(f_n)$ is a [[weak homotopy equivalence]] for all $n$ and for each homotopy group in positive degree. 

To deduce the remaining case that also $\pi_0(f_0)$ is an isomorphism, observe that by assumption of $K$-injectivity, lemma \ref{KInjectivesAreAcyclicCofibrationsForSequentialSpectra} gives that $f_0$ is the pullback (in topological spaces) of $\Omega (f_{1})$. But by the above $\Omega f_{1}$ is a weak homotopy equivalence, and since $\Omega = Maps(S^1,-)_\ast$ is a  right Quillen functor (prop. \ref{SuspensionAndLoopAdjunctionInClassicalHomotopyTheory}) it is also a Serre fibration. Therefore $f_0$ is the pullback of an acyclic Serre fibration and hence itself a weak homotopy equivalence.

=--

+-- {: .num_lemma #RetractsOfRelativeKCellComplexesAreTheStableEquivalencesAndStrictCofibrationsForSequentialSpectra}
###### Lemma

The [[retracts]] ([rmk.](Introduction+to+Stable+homotopy+theory+--+P#RetractsOfMorphisms)) of $J_{SeqSpec}^{stable}$-[[relative cell complexes]] are precisely the morphisms which are

1. stable weak equivalences, 

1. as well as strict, hence stable, cofibrations

hence which are the stable acyclic cofibrations according to def. \ref{ClassesOfMorphismsOfTheStableModelStructureOnSequentialSpectra}.

=--


+-- {: .proof}
###### Proof

Since all elements of $J_{SeqSpec}^{stable}$ are stable equivalences and strict cofibrations by  lemma \ref{ElementsOfKAreStableEquivalencesAndStrictCofibrationsForSequentialSpectra}, it follows that every retract of relative $J_{SeqSpec}^{stable}$-cell complex has the same property.

In the other direction, if $f$ is a stable equivalence and strict cofibration, by the [[small object argument]] it factors $f \colon \stackrel{i}{\to}\stackrel{p}{\to}$ as a relative $J_{SeqSpec}^{stable}$-cell complex $i$ followed by a $J_{SeqSpec}^{stable}$-[[injective morphism]] $p$. By the previous statement $i$ is a stable equivalence, and so by assumption and by [[two-out-of-three]] so is $p$. Therefore lemma \ref{KInjectiveStableEquivalencesAreStrictEquivalencesForSequentialSpectra} implies that $p$ is a strict acyclic fibration. But then the assumption that $f$ is a strict cofibration means that it has the [[left lifting property]] against $p$, and so the [[retract argument]] ([prop.](Introduction+to+Stable+homotopy+theory+--+P#RetractArgument)) implies that $f$ is a retract of the relative $\{k_n \Box i_+\}$-cell complex $i$.


=--

+-- {: .num_cor #KInjectivesAreIndeedTheStableFibrations}
###### Corollary

The $J_{SeqSpec}^{stable}$-[[injective morphisms]]
are precisely those which are
[[injective morphism|injective]] with respect to the cofibrations of the strict model structure that are also stable equivalences.

=--


+-- {: .num_lemma #StableAcyclicFibrationsAreEquivalentlyStrictAcyclicFibrations}
###### Lemma

A morphism in $SeqSpec(Top)$ is both

1. a stable weak equivalence (def. \ref{ClassesOfMorphismsOfTheStableModelStructureOnSequentialSpectra});

1. [[injective morphism|injective]] with respect to the cofibrations of the strict model structure that are also stable equivalences;

precisely if it is an acylic fibration in the strict model structure.

=--


+-- {: .proof}
###### Proof

Every acyclic fibration in the strict model structure is injective with respect to strict cofibrations by the strict model structure; and it is a stable equivalence by item 1 of lemma \ref{StableEquivalencesBetweenOmegaSpectraAreStrictWeakEquivalencesForSequentialSpectra}.

Conversely, a morphism injective with respect to strict cofibrations that are stable equivalences is a $\{k_n \Box i_+\}$-[[injective morphism]] by corollary \ref{KInjectivesAreIndeedTheStableFibrations}, and hence if it is also a stable equivalence then by lemma \ref{KInjectiveStableEquivalencesAreStrictEquivalencesForSequentialSpectra} it is a strict acylic fibration.

=--

+-- {: .proof #ProofOfTheStableModelStructureOnSequentialSpectra}
###### Proof
(of theorem \ref{AlternativeStableModelStructureOnSequentialSpectraIsModelCategory})

For the existence of the model structure, the non-trivial points to check are the two [[weak factorization systems]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#WeakFactorizationSystem)).

That $(Cof_{stable}\cap W_{stable} \;,\; Fib_{stable})$ is a weak factorization system follows from lemma \ref{RetractsOfRelativeKCellComplexesAreTheStableEquivalencesAndStrictCofibrationsForSequentialSpectra} and the [[small object argument]] ([prop.](Introduction+to+Stable+homotopy+theory+--+P#SmallObjectArgument)). 

By lemma \ref{StableAcyclicFibrationsAreEquivalentlyStrictAcyclicFibrations} the stable acyclic fibrations are equivalently the strict acyclic fibrations and hence the weak factorization system $(Cof_{stable} \;,\; Fib_{stable} \cap W_{stable})$ is identified with that of the strict model structure $(Cof_{strict} \;,\; Fib_{strict} \cap W_{strict})$.

With this, the statement of the Quillen adjunction to the strict model structure is immediate. The statement about the cofibrant generation holds by construction of the above factorizations. 

The cofibrant generation then implies that the fibrant objects are precisely the Omega-spectra: because lemma \ref{KInjectivesAreAcyclicCofibrationsForSequentialSpectra} says that the Omega-spectrum property is equivalent to being ${k_n \Box i_+}$-injective, and since being $J^{strict}_{SeqSpec}$-injective is no condition on topological sequential spectra (as all topological spaces are fibrant).

=--

##### Stable equivalences

We have constructed two [[Bousfield localization of model categories|Bousfield localizations]] (def. \ref{BousfieldLocalizationOfModelCategories}) of the strict model structure on sequential spectra: one at the [[stable weak homotopy equivalences]] (def. \ref{StableWeakHomotopyEquivalenceOfSequentialTopologicalSpectra}), in theorem \ref{StableModelStructureOnSequentialSpectraIsModelCategory}, and one at the "stable equivalences" (def. \ref{ClassesOfMorphismsOfTheStableModelStructureOnSequentialSpectra}), in theorem \ref{AlternativeStableModelStructureOnSequentialSpectraIsModelCategory}.

Here we show that these two model structures in fact agree, because these two classes of morphisms in fact coincide:


+-- {: .num_theorem #StableEquivalencesOfSequentialSpectraAgreeWithStableWeakHomotopyEquivalences}
###### Theorem

The classes of morphisms of sequential spectra

1. stable weak equivalences (def. \ref{ClassesOfMorphismsOfTheStableModelStructureOnSequentialSpectra}), 

1. [[stable weak homotopy equivalences]] (def. \ref{StableWeakHomotopyEquivalenceOfSequentialTopologicalSpectra})

agree.

=--

This is the statement of lemma \ref{StableWeakHomotopyEquivalenceInSeqSpecIsStableEquivalence} and of prop. \ref{StableEquivalenceInSeqSpecIsStableWeakHomotopyEquivalence} below, which we prove after considering a few lemmas.


+-- {: .num_lemma #FakeLoopingPreservesOmegaSpectra}
###### Lemma

With $\Sigma$ and $\Omega$ the alternative suspension and alternative looping functors from def. \ref{SequentialSpectrumFakeSuspension}:

1. $\Omega$ preserves [[Omega-spectra]] (def. \ref{OmegaSpectrum});

1. $\Sigma$ preserves stable equivalences (def. \ref{ClassesOfMorphismsOfTheStableModelStructureOnSequentialSpectra}).

=--

+-- {: .proof}
###### Proof

Regarding the first statement:

By prop. \ref{SuspensionAndLoopAdjunctionInClassicalHomotopyTheory}, $\Omega$ acts on component spaces and adjunct structure maps as the [[Quillen adjunction|right Quillen functor]]

$$
  Maps(S^1,-)_\ast
  \;\colon\;
  (Top_{cg}^{\ast/})_{Quillen}
    \longrightarrow
  (Top_{cg}^{\ast/})_{Quillen}
$$

on the [[classical model structure on pointed topological spaces|classical model structure]] on pointed compactly generated topological spaces ([thm.](Introduction+to+Stable+homotopy+theory+--+P#ClassicalModelStructureOnCompactlyGeneratedTopologicalSpaces), [prop.](Introduction+to+Stable+homotopy+theory+--+P#ModelStructureOnSliceCategory)). Since in this model structure all objects are fibrants, [[Ken Brown's lemma]] ([prop.](Introduction+to+Stable+homotopy+theory+--+P#KenBrownLemma)) implies that with $\tilde \sigma^X_n$ a [[weak homotopy equivalence]], so is
$\tilde \sigma^{\Omega X}_n = Maps(S^1,\tilde \sigma^X_n)$.

Regarding the second statement: 

By prop. \ref{AlternativeSuspensionIsLeftQuillenOnStrictModelStructureOnSequential} $(\Sigma \dashv \Omega)$ is a [[Quillen adjunction]] for the strict model structure, hence (by [this prop.](Introduction+to+Stable+homotopy+theory+--+P#QuillenAdjunctionInducesAdjunctionOnHomotopyCategories)) it passes to an adjunction of its [[derived functors]] on the [[homotopy category of a model category|homotopy category]]. 

Therefore with $f$ a stable equivalence and $Y$ any Omega-spectrum, then

$$
  [\Sigma f,Y]_{strict}
  =
  [f,\Omega Y]_{strict}
$$

is an isomorphism by the first statement above, and hence $\Sigma f$ is a stable equivalence.

=--


+-- {: .num_lemma #CounitOfFakeSuspensionAndShiftIsStableEquivalence}
###### Lemma

For $X$ a [[sequential spectrum]], then (using remark \ref{ShiftingCommutesWithLoopingAndSuspensionOfSequentialSpectra} to suppress parenthesis)

1. the structure maps constitute a homomorphism

   $$
     \Sigma X[-1]
     \longrightarrow
     X
   $$

   and this is a stable equivalence (def. \ref{ClassesOfMorphismsOfTheStableModelStructureOnSequentialSpectra}),

1. the adjunct structure maps constitute a homomorphism

   $$
     X
     \longrightarrow
     \Omega X[1]
     \,.
   $$

   If $X$ is an [[Omega-spectrum]] (def. \ref{OmegaSpectrum}) then this is a weak equivalence in the strict model structure (def. \ref{ClassesOfMorphismsOfTheStrictModelStructureOnSequentialSpectra}), hence in particular a stable equivalence (def. \ref{ClassesOfMorphismsOfTheStableModelStructureOnSequentialSpectra}).

=--

+-- {: .proof}
###### Proof

The diagrams that need to commute for the structure maps to give a homomorphism as claimed are in degree 0 this one

$$
  \array{
    S^1 \wedge S^1 \wedge \ast &\overset{0}{\longrightarrow}& X_0
    \\
    {}^{\mathllap{S^1 \wedge 0}}\downarrow && \downarrow^{\mathrlap{\sigma_0}}
    \\
    S^1 \wedge X_0 &\underset{\sigma_0}{\longrightarrow}& X_1
  }
$$

and in degree $n \geq 1$ these:

$$
  \array{
     S^1 \wedge S^1 \wedge X_{n-1} 
        &\overset{S^1 \wedge \sigma_{n-1}}{\longrightarrow}& 
     X_n
     \\
     {}^{\mathllap{S^1 \wedge \sigma_{n-1}}}\downarrow
       &&
     \downarrow^{\mathrlap{\sigma_n}}
     \\
     S^1 \wedge X_{n} 
       &\underset{\sigma_n}{\longrightarrow}& 
     X_{n+1}
  }
  \,.
$$

But in all these cases commutativity it trivially satisfied. 

That the adjunct structure maps constitute a morphism $X \to \Omega X[1]$ follows [[formal dual|dually]].

If $X$ is an [[Omega-spectrum]], then by definition this last morphism is already a weak equivalence in the strict model structure, hence in particular a weak equivalence in the stable model structure.

From this it follows that also the first morphism is a stable equivalence, because for every [[Omega-spectrum]] $Y$ then by the adjunctions in prop. \ref{AdjunctionsBetweenLoopingAndDeloopingForSeqSpec}

$$
  \array{
     [X, Y]_{strict} &\overset{}{\longrightarrow}& [\Sigma X[-1],Y]_{strict}
     \\
     {}^{\mathllap{id}}\downarrow && \downarrow^{\mathrlap{\simeq}}
     \\
     [X,Y]_{strict}  &\underset{\simeq}{\longrightarrow}& [X, \Omega Y[1]]_{strict}
  }
  \,.
$$

(To see the commutativity of this last diagram in detail, consider for any $[f] \in [X,Y]_{strict}$ chasing the element $\sigma_n^Y$ in the two possible ways through the natural adjunction isomorphism:

$$
  \array{
    [S^1 \wedge Y_{n-1}, Y_n]
      &\simeq&
    [Y_{n-1}, \Omega Y_n]
    \\
    {}^{\mathllap{[S^1 \wedge f_{n-1}, Y_n]}}\downarrow && \downarrow^{\mathrlap{[f_{n-1}, \Omega Y_n]}}
    \\
    [S^1 \wedge X_{n-1}, Y_n]
      &\simeq&
    [X_{n-1}, \Omega Y_n]
  }
  \,.
$$

Sending $\sigma_n^Y$ down gives $\sigma_n^Y \circ S^1 \wedge f_{n-1}$ which equals (by the homomorphism property) $f_n \circ \sigma_n^X$. Instead sending $\sigma_n^Y$ to the right yields $\tilde \sigma_n^Y$ and then down yields $\tilde \sigma_n^Y \circ f_{n-1}$. By commutativity this is adjunct to $f_n \circ \sigma_n^X$.)

=--




It follows in particular that:

+-- {: .num_prop #SpectrificationIsFibrantReplacement}
###### Proposition

For every $X \in SeqSpec(Top_{cg})$, then the [[spectrification]] from def. \ref{SpectrificationForTopologicalSequentialSpectra} is a fibrant replacement in the stable model structure of theorem \ref{StableModelStructureOnSequentialSpectraIsModelCategory}:

$$  
  X 
    \underoverset{\in W_{stable}}{j_X}{\longrightarrow}
  Q X
    \underset{\in Fib_{stable}}{\longrightarrow}
  \ast
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the first item of prop. \ref{PropertiesOfSpectrificationForTopologicalSequentialSpectra}, $Q X$ is an [[Omega-spectrum]]; by theorem \ref{StableModelStructureOnSequentialSpectraIsModelCategory} these are fibrant in the stable model structure.

By the second item of prop. \ref{PropertiesOfSpectrificationForTopologicalSequentialSpectra} $j_X$ is a stable weak equivalence, and by lemma \ref{StableWeakHomotopyEquivalenceInSeqSpecIsStableEquivalence} these are in $W_{stable}$. 

=--


For the converse to lemma \ref{StableWeakHomotopyEquivalenceInSeqSpecIsStableEquivalence} we use two technical lemmas whose proof we postpone until later (lemma \ref{ExplicitCheckThatWedgeSumIsProductInStableHomotopyCategory} and lemma \ref{CofibrantStableWeakHomotopyEquivalencesPreservedUnderPushout}) below:

+-- {: .num_prop #StableEquivalenceInSeqSpecIsStableWeakHomotopyEquivalence}
###### Proposition

Every stable weak equivalence of sequential spectra (def. \ref{ClassesOfMorphismsOfTheStableModelStructureOnSequentialSpectra})
is a [[stable weak homotopy equivalence]] (def. \ref{StableWeakHomotopyEquivalenceOfSequentialTopologicalSpectra}).
 
=--

+-- {: .proof}
###### Proof

Let $f \colon X \to Y$ be a stable weak equivalence. Use the [[factorization lemma]] ([prop](Introduction+to+Stable+homotopy+theory+--+P#FactorizationLemma)) with respect to the set $J_{SeqSpec}^{stable}$ from def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForSeqSpecStable} to form a factorization

$$
  f \colon X \overset{\in J_{SeqSpec}^{stable} Cell}{\longrightarrow} \hat X \overset{\in Fib_{st} \cap W_{ste}}{\longrightarrow} X
$$

By lemma \ref{KInjectiveStableEquivalencesAreStrictEquivalencesForSequentialSpectra} the morphism on the right is a degreewise weak homotopy equivalence and hence in particular a stable weak homotopy equivalence. Therefore it is now sufficient to prove that every $J_{SeqSpec}^{stable}$-relative cell complex is a stable weak homotopy equivalence. 

Since stable weak homotopy equivalences are preserved under [[transfinite composition]] of $J_{SeqSpec}^{stable}$-relative cell complexes (by the compactness of the [[n-spheres]] ([lemma](Introduction+to+Stable+homotopy+theory+--+P#CompactSubsetsAreSmallInCellComplexes)) taking homotopy groups commutes with the corresponding sequential colimit) we are reduced to  showing that


1. Every element of $J_{SeqSpec}^{stable}$ is a stable weak homtopy equivalence;

1. Every [[pushout]] of [[coproducts]] of elements in $J_{SeqSpec}^{stable}$ is a stable weak homotopy equivalence.


Regarding the first statement: 

It is clear that the elements of $J_{SeqSpec}^{strict}$ are stable weak homotopy equivalences. It remains to see that the [[pushout products]] $k_n \Box i_+$ are stable weak equivalences. Here is is clear from inspection that the [[smash product]] of a $k_n$ with a domain or codomain of $i_+$ is still a stable weak homtopy equivalence. We now invoke lemma \ref{CofibrantStableWeakHomotopyEquivalencesPreservedUnderPushout}, which says that any [[pushout]] of $k_n \wedge S^{k-1}$ is still a weak homotopy equivalence. With this the statement follows by [[two-out-of-three]].

Regarding the second statement: 

The stable homotopy groups of a finite [[wedge sum]] of spectra is the [[direct sum]] of the stable homotopy groups of the wedge summands, by lemma \ref{ExplicitCheckThatWedgeSumIsProductInStableHomotopyCategory}. The analogous statement for non-finite wedge sums follows by taking a colimit. Hence forming wedge sums preserves stable weak homotopy equivalences. 

Finally, with the first statement, lemma \ref{CofibrantStableWeakHomotopyEquivalencesPreservedUnderPushout} (saying that pushouts of stable weak homotopy equivalences which are also cofibrations remain stable weak homotopy equivalences) implies that remainder of the second statement.

=--





#### The stable homotopy category

+-- {: .num_defn #TheStableHomotopyCategory}
###### Definition

Write

$$
  Ho(Spectra)
  \coloneqq
  Ho(SeqSpec(Top_{cg})_{stable})
$$

for the [[homotopy category of a model category|homotopy category]] ([defn.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyCategoryOfAModelCategory)) of the stable [[model structure on topological sequential spectra]] from theorem \ref{StableModelStructureOnSequentialSpectraIsModelCategory}. 

This is called the **[[stable homotopy category]]**.

=--


The [[stable homotopy category]] of def. \ref{TheStableHomotopyCategory} inherits particularly nice properties that are usefully axiomatized for themselves. This axiomatics is called _[[triangulated category]]_ structure (def. \ref{CategoryWithCofiberSequences} below) where the "triangles" are referring to the structure of the long fiber sequences and long cofiber sequences ([prop.](Introduction+to+Stable+homotopy+theory+--+P#LongFiberSequence)) which happen to coincide in stable homotopy theory.


##### Additivity


+-- {: .num_lemma #StableHomotopyCategoryHasCoproducts}
###### Lemma

The [[stable homotopy category]] (def. \ref{TheStableHomotopyCategory}) has [[finite product|finite]] [[coproducts]]. They are represented by [[wedge sums]] (example \ref{WedgeSumOfSpectra}) of [[CW-spectra]] (def. \ref{CWSpectrum}).

=--

+-- {: .proof}
###### Proof

Having finite coproducts means having empty coproducts, which are [[initial objects]], and having binary coproducts. 

Regarding the initial object:

The spectrum $\Sigma^\infty \ast$ ([[suspension spectrum]] (example \ref{SuspensionSpectrum}) on the point) is both an [[initial object]] and a [[terminal object]] in $SeqSpec(Top_{cg})$. This implies in particular that it is both fibrant and cofibrant. Finally its standard [[cylinder spectrum]] (example \ref{StandardCylinderSpectrumSequential}) is trivial $(\Sigma^\infty \ast) \wedge (I_+)\simeq \Sigma^\infty \ast$. All together with means that for $X$ any fibrant-cofibrant spectrum, then 

$$
  Hom_{Ho(Spectra)}(\Sigma^\infty \ast, Z)
  \simeq
  Hom_{SeqSpec}(\Sigma^\infty \ast, Z)/_\sim
  \simeq
  \ast
  \,.
$$

Now regarding binary coproducts:

By prop. \ref{CWApproximationForSequentialSpectra} and prop. \ref{CellSpectraAreCofibrantInModelStructureOnTopologicalSequentialSpectra}, every spectrum has a cofibrant replacement by a [[CW-spectrum]]. By prop. \ref{ClosureOfCWSpectra} the [[wedge sum]] $X \wedge Y$ of two CW-spectra is still a CW-spectrum, hence still cofibrant. 

Let $P$ and $Q$ be fibrant and cofibrant replacement functors, respectively, as in _[Prelude -- The homotopy category](Introduction+to+Stable+homotopy+theory+--+P#TheHomotopyCategory).

We claim now that $P(X \wedge Y) \in Ho(Spectra)$ is the coproduct of $P X$ with $P Y$ in $Ho(Spectra)$. By definition of the [[homotopy category of a model category|homotopy category]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyCategoryOfAModelCategory)) this is equivalent to claiming that for $Z$ any stable fibrant spectrum then there is a [[natural isomorphism]]

$$
  Hom_{SeqSpec}(P(X \wedge Y), Q Z)/_\sim
  \simeq
  Hom_{SeqSpec}(P X, Q Z)/_\sim \times Hom_{SeqSpec}(P Y, Q Z)/_\sim
$$

between [[left homotopy]]-classes of morphisms of sequential spectra.

But since $X \vee Y$ is cofibrant and $Z$ is fibrant, there is a natural isomorphism ([prop.](Introduction+to+Stable+homotopy+theory+--+P#HomsOutOfCofibrantIntoFibrantComputeHomotopyCategory))

$$
  Hom_{SeqSpec}(P(X \wedge Y), Q Z)/_\sim
  \overset{\simeq}{\longrightarrow}
  Hom_{SeqSpec}(X \wedge Y, Z)/_\sim  
  \,.
$$

Now the wedge sum $X \vee Y$ is the coproduct in $SeqSpec(Top_{cg})$, and hence morphisms out of it are indeed in natural bijection with pairs of morphisms out of the two summands. But we need this property to hold still after dividing out left homotopy. The key is that smash tensoring (def. \ref{TensoringAndPoweringOfSequentialSpectra}) distributes over wedge sum

$$
  (X \vee Y) \wedge (I_+) \simeq (X \wedge (I_+)) \vee (Y\wedge (I_+))
$$

(due to the fact that the [[smash product]] of compactly generated [[pointed topological spaces]] distributes this way over wedge sum of pointed spaces). This means that also left homotopies out of $X \vee Y$ are in natural bijection with pairs of left homotopies out of the summands separately, and hence that there is a natural isomorphism

$$
  Hom_{SeqSpec}(X \wedge Y, Z)/_\sim  
  \overset{\simeq}{\longrightarrow}
  Hom_{SeqSpec}(X,Z)/_\sim \times Hom_{SeqSpec}(Y,Z)/_\sim
  \,.
$$

Finally we may apply the inverse of the natural isomorphism used before ([prop.](Introduction+to+Stable+homotopy+theory+--+P#HomsOutOfCofibrantIntoFibrantComputeHomotopyCategory)) to obtain in total

$$
  Hom_{SeqSpec}(X,Z)/_\sim \times Hom_{SeqSpec}(Y,Z)/_\sim
  \overset{\simeq}{\longrightarrow}
  Hom_{SeqSpec}(P X,Q Z)/_\sim \times Hom_{SeqSpec}(P Y,Q Z)/_\sim
  \,.
$$

The composite of all these isomorphisms proves the claim.

=--

+-- {: .num_lemma #StableHomotopyCategoryIsAbEnriched}
###### Lemma

Consider the group structure on [[hom-sets]] of the [[stable homotopy category]] (def. \ref{TheStableHomotopyCategory}) which is induced from the fact ([prop.](Introduction+to+Stable+homotopy+theory+--+P#LoopingAsFunctorOnHomotopyCategory)) that the [[hom-sets]] of any [[homotopy category of a model category|homotopy category]] into an object in the image of the canonical loop space functor $\Omega$ inherit group structure, together with the fact (theorem \ref{StableModelStructureOnSequentiaSpectraIsStableModelCategory}) that on the [[stable homotopy category]] $\Omega$ has an inverse $\Sigma$, so that

$$
  Hom_{Ho(Spectra)}(X,Y)
  \simeq
  Hom_{(Ho(Spectra))}(X, \Omega \Sigma Y)
  \,.
$$

This group structure is [[abelian group|abelian]] and [[composition]] is [[bilinear map|bilinear]] with respect to it. (Hence this makes $Ho(Spectra)$ an _[[Ab-enriched category]]_.)

=--

+-- {: .proof}
###### Proof

Recall ([prop](Introduction+to+Stable+homotopy+theory+--+P#LoopingAsFunctorOnHomotopyCategory), [rmk.](Introduction+to+Stable+homotopy+theory+--+P#ConcatenatedLoopSpaceObject)) that the group structure is given by concatenation of loops 

$$
  X 
    \overset{\Delta_X}{\to}
  X \times X
    \overset{(f,g)}{\longrightarrow}
  \Omega \Sigma X \times \Omega \Sigma X
  \overset{}{\longrightarrow}
  \Omega \Sigma X
  \,.
$$


That the group structure is abelian follows via the [[Eckmann-Hilton argument]] from the fact that there is always a compatible second (and indeed arbitrarily many compatible) further group structures, since 

$$
  Hom_{Ho(Spectra)}(X,Y)
    \simeq
  Hom_{(Ho(Spectra))}(X, \Omega \Sigma Y)
    \simeq
  Hom_{(Ho(Spectra))}(X, \Omega \circ (\Omega \Sigma) \circ \Sigma Y)
    =
  Hom_{(Ho(Spectra))}(X, \Omega^2 \Sigma^2 Y)
  \,.
$$

That composition distributes over composition in this group structure is the naturality of the loop composition map, which is evident from the standard model ([rmk.](Introduction+to+Stable+homotopy+theory+--+P#ConcatenatedLoopSpaceObject))

$$
  \array{
    \Omega \Sigma X \times \Omega \Sigma X
    &\longrightarrow&
    \Omega \Sigma X
    \\
    {}^{\mathllap{(f,f)}}\downarrow && \downarrow^{\mathrlap{f}}
    \\
    \Omega \Sigma Y \times \Omega \Sigma Y
    &\longrightarrow&
    \Omega \Sigma Y
  }
  \,.
$$

=--

In summary, lemma \ref{StableHomotopyCategoryHasCoproducts} and lemma \ref{StableHomotopyCategoryIsAbEnriched} state that the [[stable homotopy category]] is an [[Ab-enriched category]] with finite [[coproducts]]. This is called an _[[additive category]]_:
 
+-- {: .num_defn #AdditiveCategory}
###### Definition

An **[[additive category]]** is a [[category]] which is

1. an [[Ab-enriched category]];

   (sometimes called a [[pre-additive category]]--this means that each [[hom-set]] carries the structure of an [[abelian group]] and composition is [[bilinear map|bilinear]])

1. which admits [[finite limit|finite]] [[coproducts]] 

   (and hence, by prop. \ref{ProductsAreBiproducts} below, finite [[products]] which coincide with the coproducts, hence finite [[biproducts]]).

=--

+-- {: .num_prop #ProductsAreBiproducts}
###### Proposition

In an [[Ab-enriched category]], a [[finite product|finite]] [[product]] is also a [[coproduct]], and dually.  

This statement includes the zero-ary case: any [[terminal object]] is also an [[initial object]], hence a [[zero object]] (and dually), hence every [[additive category]] (def. \ref{AdditiveCategory}) has a [[zero object]].  

More precisely, for $\{X_i\}_{i \in I}$ a [[finite set]] of objects in an Ab-enriched category, then the unique morphism 

$$
  \underset{i \in I}{\coprod} X_i \longrightarrow \underset{j \in I}{\prod} X_j
$$

whose components are identities for $i = j$ and are [[zero morphism|zero]] otherwise is an [[isomorphism]].

=--

+-- {: .proof}
###### Proof

Consider first the zero-ary case. Given an [[initial object]] $\emptyset$ and a [[terminal object]] $\ast$, observe that since the [[hom-sets]] $Hom(\emptyset,\emptyset)$ and $Hom(\ast,\ast)$ by definition contain a single element, this element has to be the zero element in the abelian group structure. But it also has to be the identity morphism, and hence $id_\emptyset = 0$ and $id_{\ast} = 0$. It follows that the 0-element in $Hom(\ast, \emptyset)$ is a left and right inverse to the unique element in $Hom(\emptyset,\ast)$, and so this is an [[isomorphism]]

$$
  0 \;\colon\; \emptyset \overset{\simeq}{\longrightarrow} \ast
  \,.
$$

Consider now the case of binary (co-)products. Using the existence of the [[zero object]], hence of [[zero morphisms]], then in addition to its canonical [[projection]] maps $p_i \colon X_1 \times X_2 \to X_i$, any binary [[product]] also receives "injection" maps $X_i \to X_1 \times X_2$, and dually for the [[coproduct]]:

$$
  \array{  
    X_1 && && X_2
    \\
    & \searrow^{\mathrlap{(id,0)}} && {}^{\mathllap{(0,id)}}\swarrow
    \\
    {}^{\mathllap{id_{X_1}}}\downarrow && X_1 \times X_2 && \downarrow^{\mathrlap{id_{X_2}}}
    \\
    & \swarrow_{\mathrlap{p_{X_1}}} && {}_{\mathllap{p_{X_2}}}\searrow
    \\
    X_1 && && X_2
  }
  \;\;\;\;\;\;\;\;\;\;\;\;\,,\;\;\;\;\;\;\;\;\;\;\;\;
  \array{  
    X_1 && && X_2
    \\
    & \searrow^{\mathrlap{i_{X_1}}} && {}^{\mathllap{i_{X_2}}}\swarrow
    \\
    {}^{\mathllap{id_{X_1}}}\downarrow 
     && X_1 \sqcup X_2 && \downarrow^{\mathrlap{id_{X_2}}}
    \\
    & \swarrow_{\mathrlap{(id,0)}} && {}_{\mathllap{(0,id)}}\searrow
    \\
    X_1 && && X_2
  }
  \,.
$$

Then using the additivity of morphisms, it follows that for $f_i \;\colon\; X_i \to Q$ any two morphisms, the sum 

$$
  \phi \;\colon\; f_1 \circ p_1 + f_2 \circ p_2
$$

gives a morphism of [[cocones]]

$$
  \array{  
    X_1 && && X_2
    \\
    & \searrow^{\mathrlap{(id,0)}} && {}^{\mathllap{(0,id)}}\swarrow
    \\
    {}^{\mathllap{id_{X_1}}}\downarrow && X_1 \times X_2 && \downarrow^{\mathrlap{id_{X_2}}}
    \\
    &  && 
    \\
    X_1 && \downarrow^{\mathrlap{\phi}} && X_2
    \\
    & {}_{\mathllap{f_1}}\searrow && \swarrow_{\mathrlap{f_2}}
    \\
    && Q
  }
  \,.
$$

Moreover, this is in fact unique: suppose $\phi'$ is another morphism filling this diagram, then 

$$
  \begin{aligned}
    (\phi-\phi')
    & = 
    (\phi - \phi') \circ id_{X_1 \times X_2}
    \\
    &= 
    (\phi - \phi') \circ ( (id_{X_1},0) \circ p_1 + (0,id_{X_2})\circ p_2 )
    \\
    & =
    \underset{ = 0}{\underbrace{(\phi - \phi') \circ (id_{X_1}, 0)}} \circ p_1
    + 
    \underset{ = 0}{\underbrace{(\phi - \phi') \circ (0, id_{X_2})}} \circ p_2
    \\
    & = 0
  \end{aligned}
$$

and hence $\phi = \phi'$. This means that $X_1\times X_2$ satisfies the [[universal property]] of a [[coproduct]].

By a [[formal dual|dual]] argument, the binary coproduct $X_1 \sqcup X_2$ is seen to also satisfy the universal property of the binary product. By [[induction]], this implies the statement for all finite (co-)products.

=--


+-- {: .num_remark #BiproductsInAdditiveCategories}
###### Remark

Finite coproducts coinciding with products as in prop. \ref{ProductsAreBiproducts} ar also called _[[biproducts]]_ or _[[direct sums]]_, denoted

$$
  X_1 \oplus X_2 \coloneqq X_1 \sqcup X_2 \simeq X_1 \times X_2
  \,.
$$

The [[zero object]] is denoted "0", of course.

=--

Conversely:

+-- {: .num_defn #SemiadditiveCategory}
###### Definition

A **[[semiadditive category]]** is a [[category]] that has all [[finite products]] which, moreover, are [[biproducts]] in that they coincide with finite [[coproducts]] as in def. \ref{ProductsAreBiproducts}.

=--

+-- {: .num_prop #SemiAdditivityInducesAbelianMonoidEnrichment}
###### Proposition

In a [[semiadditive category]], def. \ref{SemiadditiveCategory}, the [[hom-sets]] acquire the structure of [[commutative monoids]] by defining the sum of two morphisms $f,g \;\colon\; X \longrightarrow Y$ to be

$$
  f + g 
    \;\coloneqq\;
  X \overset{\Delta_X}{\to} X \times X
  \simeq
  X \oplus X
  \overset{f \oplus g}{\longrightarrow}
  Y \oplus Y
  \simeq
  Y \sqcup Y
  \overset{\nabla_X}{\to}
  Y
  \,.
$$

With respect to this operation, [[composition]] is [[bilinear map|bilinear]].

=--

+-- {: .proof}
###### Proof

The [[associativity]] and commutativity of $+$ follows directly from the corresponding properties of $\oplus$. Bilinearity of composition follows from [[natural transformation|naturality]] of the [[diagonal]] $\Delta_X$ and [[codiagonal]] $\nabla_X$.

=--

+-- {: .num_prop #SemiaddtiveStructureUnderlyingAdditiveInducesOriginalEnrichment}
###### Proposition

Given an [[additive category]] according to def. \ref{AdditiveCategory}, then the enrichement in [[commutative monoids]] which is induced on it via prop. \ref{ProductsAreBiproducts} and prop. \ref{SemiAdditivityInducesAbelianMonoidEnrichment} from its underlying [[semiadditive category]] structure coincides with the original enrichment.

=--

+-- {: .proof}
###### Proof

We may write the formula for the addition of two morphisms induced by semiadditve structure equivalently as

$$
  f+g \;\colon\; 
  X \overset{\Delta_X}{\to} X \times X
  \overset{(f,g)}{\longrightarrow}
  Y \times Y
  \overset{p_1 + p_2}{\longrightarrow}
  Y
$$

where the last morphism is identified as the sum of the two projections as in the proof of prop. \ref{ProductsAreBiproducts}. This implies the claim.

=--

+-- {: .num_remark #AdditiveCategoryIsProperty}
###### Remark

Prop. \ref{SemiaddtiveStructureUnderlyingAdditiveInducesOriginalEnrichment} says that being an [[additive category]] is an extra [[property]] on a category, not extra [[structure]]. We may ask whether a given category is additive or not, without specifying beforehand with respect to which abelian group structure on the hom-sets.

=--

In conclusion we have:

+-- {: .num_prop #TheStableHomotopyCategoryIsAdditive}
###### Proposition

The [[stable homotopy category]] (def. \ref{TheStableHomotopyCategory}) is an [[additive category]] (def. \ref{AdditiveCategory}).

=--

+-- {: .proof}
###### Proof

By lemma \ref{StableHomotopyCategoryHasCoproducts} and lemma \ref{StableHomotopyCategoryIsAbEnriched}.

=--

Hence prop. \ref{ProductsAreBiproducts} implies that in the stable homotopy category finite coproducts and finite products agree, in that they are finite [[biproducts]]. We may also check this explicitly:

+-- {: .num_lemma #ExplicitCheckThatWedgeSumIsProductInStableHomotopyCategory}
###### Lemma

For $X,Y \in SeqSpec(Top_{cg})$, then the canonical morphism

$$
  X \vee Y 
   \longrightarrow
  X \times Y
$$

out of the [[coproduct]] ([[wedge sum]], example \ref{WedgeSumOfSpectra}) into the [[product]] (via prop. \ref{LimitsAndColimitsOfSequentialSpectra}), given by

$$
  \array{  
    X && && Y
    \\
    & \searrow^{\mathrlap{i_X}} && {}^{\mathllap{i_X}}\swarrow
    \\
    {}^{\mathllap{id_X}}\downarrow 
     && X \sqcup Y && \downarrow^{\mathrlap{id_Y}}
    \\
    & \swarrow_{\mathrlap{(id,0)}} && {}_{\mathllap{(0,id)}}\searrow
    \\
    X && && Y
    \\
    & \searrow^{\mathrlap{(id,0)}} && {}^{\mathllap{(0,id)}}\swarrow
    \\
    {}^{\mathllap{id_X}}\downarrow && X \times Y && \downarrow^{\mathrlap{id_Y}}
    \\
    & \swarrow_{\mathrlap{p_X}} && {}_{\mathllap{p_Y}}\searrow
    \\
    X && && Y
  }
$$

represents an [[isomorphism]] in the [[stable homotopy category]].

=--

+-- {: .proof}
###### Proof

We may represent both $X$ and $Y$ by [[CW-spectra]] in $(SeqSpec(Top_{cg})_{stable})_c[W_{st}^{-1}]$. Then the canonical morphism 

$$
  i_X \colon X \longrightarrow X \vee Y
$$

is a stable cofibration, because $X_{n+1}\underset{S^1 \wedge X_n}{\sqcup} S^1 (X \vee Y) \simeq X_{n+1} \vee S^1 \wedge Y_n$.

Hence its ordinary cofiber, which is $Y$,  is its homotopy cofiber, hence we have a homotopy cofiber sequence

$$
  X \longrightarrow X \vee Y \longrightarrow Y
$$

moreover, under forming [[stable homotopy groups]], the the inclusion map evidently gives an injection, and the projection map gives a surjection. Hence the [[long exact sequence of homotopy groups]] gives a [[short exact sequence]]

$$
  0 \to
  \pi_\bullet(X)
  \longrightarrow
  \pi_\bullet(X \vee Y)
  \longrightarrow
  \pi_\bullet(Y)
  \to 
  0
  \,.
$$

Moreover, due to the fact that the inclusion and projection for one of the two summands constitute a [[retraction]], this is a [[split exact sequence]], hence exhibits an isomorphism

$$
  \pi_k(X \vee Y)  
  \overset{\simeq}{\longrightarrow}
  \pi_k(X)\oplus \pi_k(Y)
$$

for all $k$. But this just says that $X \vee Y \to X \times Y$ is a [[stable weak homotopy equivalence]].

=--



##### Triangulated structure

**Literature** ([Schwede 12, II.2](#Schwede12))


+-- {: .num_defn #CategoryWithCofiberSequences}
###### Definition

A **[[triangulated category]]** is

1. an [[additive category]] $Ho$ (def. \ref{AdditiveCategory});

1. a functor, called the **suspension functor** or **[[shift functor]]**

   $$
     \Sigma \;\colon\; Ho \overset{\simeq}{\longrightarrow} Ho
   $$

   which is required to be an [[equivalence of categories]];

1. a sub-[[class]] $CofSeq \subset Mor(Ho^{\Delta[3]})$ of the class of triples of composable morphisms, called the class of **distinguished triangles**, where each element is of the form

   $$
     A \overset{}{\longrightarrow} B \overset{}{\longrightarrow}  \overset{}{\longrightarrow} \Sigma A
     \,,
   $$

   which is also denoted as

   $$
     \array{
        A && \overset{f}{\longrightarrow} && B
        \\
        & {}_{\mathllap{[1]}}\nwarrow && \swarrow_{\mathrlap{}}
        \\
        && B/A
     }
   $$

   (whence the name);

such that the following conditions hold:

* **T0** If $(f,g,h)$ is a distinguished triangle and there is a [[commuting diagram]] in $Ho$ of the form

  $$
    \array{    
     A &\overset{}{\longrightarrow}& B &\overset{g}{\longrightarrow}& B/A &\overset{h}{\longrightarrow}& \Sigma A      
     \\
     \downarrow^{\mathrlap{\in Iso}} && \downarrow^{\mathrlap{\in Iso}} 
     && \downarrow^{\mathrlap{\in Iso}}
     && \downarrow^{\mathrlap{\in Iso}}
     \\
     A' &\overset{f'}{\longrightarrow}& B' &\overset{g'}{\longrightarrow}& B'/A' &\overset{h'}{\longrightarrow}& \Sigma A'      
     
    }
  $$

  then $(f',g',h')$ is also a distinguished triangle;
  
  Moreover, for every morphism $f \colon A \to B$ there is a distinguished triangle of the form

  $$
    A \overset{f}{\longrightarrow} B \longrightarrow B/A \longrightarrow \Sigma A
    \,.
  $$

* **T1** For every object $X \in Ho$ then $(0,id_X,0)$ is a distinguished triangle

  $$
    0 \longrightarrow X \overset{id_X}{\longrightarrow} X 
    \overset{}{\longrightarrow} 0
    \,;
  $$


* **T2** If $(f,g,h)$ is a distinguished triangle, then so is $(g,h, - \Sigma f)$; hence if

  $$
    A \overset{f}{\longrightarrow} B \overset{g}{\longrightarrow} B/A \overset{h}{\longrightarrow} \Sigma A
  $$

  is, then so is

  $$
    B \overset{g}{\longrightarrow} B/A \overset{h}{\longrightarrow} \Sigma A \overset{-\Sigma f}{\longrightarrow} \Sigma B
    \,.
  $$

* **T3** Given a [[commuting diagram]] in $Ho$ of the form

  $$
    \array{    
     A &\overset{}{\longrightarrow}& 
     B &\overset{}{\longrightarrow}& 
     B/A &\overset{}{\longrightarrow}& \Sigma A      
     \\
     \downarrow^{\mathrlap{\phi_A}}
     && \downarrow^{\mathrlap{\phi_B}} 
     && 
     && 
     \\
     A' &\overset{}{\longrightarrow}& B' &\overset{}{\longrightarrow}& B'/A' &\overset{}{\longrightarrow}& \Sigma A'           
    }
  $$

  where the top and bottom are distinguished triangles, then there exists a morphism $B/A \to B'/A'$ such as to make the completed diagram commute
  
  $$
    \array{    
     A &\overset{}{\longrightarrow}& B &\overset{}{\longrightarrow}& B/A &\overset{}{\longrightarrow}& \Sigma A      
     \\
     \downarrow^{\mathrlap{\phi_A}}
     && \downarrow^{\mathrlap{\phi_B}} 
     && \downarrow^{\mathrlap{\exists}}
     && \downarrow^{\mathrlap{\Sigma \phi_A}}
     \\
     A' &\overset{}{\longrightarrow}& B' &\overset{}{\longrightarrow}& B'/A' &\overset{}{\longrightarrow}& \Sigma A'           
    }
  $$

* **T4** For every pair of composable morphisms $f \colon A \to B$ and $f' \colon B \to D$ then there is a [[commutative diagram]] of the form
  
  $$
    \array{
      A 
        &\overset{f}{\longrightarrow}& 
      B 
        &\overset{g}{\longrightarrow}& 
      C 
        &\overset{h}{\longrightarrow}&
      \Sigma A
      \\
      {}^{\mathllap{=}}\downarrow && {}^{\mathllap{f'}}\downarrow && \downarrow^{\mathrlap{x}} && \downarrow^{\mathrlap{=}}
      \\
      A 
        &\underset{f' \circ f}{\longrightarrow}&
      B
        &\underset{g''}{\longrightarrow}&
      E
        &\underset{h''}{\longrightarrow}&
      \Sigma A
      \\
      && {}^{\mathllap{g'}}\downarrow && \downarrow^{\mathrlap{y}} && \downarrow^{\mathrlap{\Sigma f}}
      \\
      && 
      F 
       &\underset{=}{\longrightarrow}& 
      F
        &\underset{h'}{\longrightarrow}& 
      \Sigma B
      \\
      && {}^{\mathllap{h'}}\downarrow && \downarrow^{\mathrlap{(\Sigma g)\circ h'}}
      \\
      && \Sigma B &\underset{\Sigma g}{\longrightarrow}& \Sigma C
    }
  $$

  such that the two top horizontal sequences and the two middle vertical sequences each are distinguished triangles.

=--



+-- {: .num_prop #StableHomotopyCategoryIsTriangulated}
###### Proposition

The [[stable homotopy category]] $Ho(Spectra)$ from def. \ref{TheStableHomotopyCategory}, equipped with the canonical suspension functor $\Sigma \colon Ho(Spectra) \overset{\simeq}{\longrightarrow} Ho(Spectra)$ (according to [this prop.](Introduction+to+Stable+homotopy+theory+--+P#LoopingAsFunctorOnHomotopyCategory)) is a [[triangulated category]] (def. \ref{CategoryWithCofiberSequences}) for the distinguished triangles being precisely the images (under localization $SeqSpec(Top_{cg})_{stable} \to Ho(Spectra)$ ([prop.](Introduction+to+Stable+homotopy+theory+--+P#UniversalPropertyOfHomotopyCategoryOfAModelCategory)) of the stable model category of theorem \ref{StableModelStructureOnSequentialSpectraIsModelCategory})
of the canonical long [[homotopy cofiber sequences]] ([prop.](Introduction+to+Stable+homotopy+theory+--+P#LongFiberSequence)) 

$$
  A \overset{f}{\longrightarrow} B 
  \overset{}{\longrightarrow} hocofib(f)
  \longrightarrow
  \Sigma A
  \,.
$$


=--

+-- {: .proof}
###### Proof

By prop. \ref{TheStableHomotopyCategoryIsAdditive} the stable homotopy category is additive, by theorem \ref{StableModelStructureOnSequentiaSpectraIsStableModelCategory} the functor $\Sigma$ is an equivalence.

The axioms T0 and T1 are immediate from the definition of homotopy cofiber sequences. 

The axiom T2 is the very characterization of long homotopy cofiber sequences (from [this prop.](Introduction+to+Stable+homotopy+theory+--+P#LongFiberSequence)).

Regarding axiom T3:

By the factorization axioms of the [[model category]] we may represent the morphisms $A \to A'$ and $B \to B'$ in the homotopy category by cofibrations in the model category. Then $B \to B/A$ and $B' \to B'/A'$ are represented by their ordinary [[cofibers]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyFiber), [prop.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyFiberIndependentOfChoiceOfFibrantReplacement)). This way the morphism $B/A \to B'/A'$ is induced by the  [[universal property]] of ordinary cofibers.  To see that we may also complete the last vertical morphism, observe that generally these [[connecting homomorphisms]] may be represented functorially: 

By the existence of [[CW-approximations]] (prop. \ref{CWApproximationForSequentialSpectra}) we may assume without restriction of generality that all spectra involved are [[CW-spectra]]. For these the standard [[cylinder spectrum]] (example \ref{StandardCylinderSpectrumSequential}) is a good [[cylinder object]] (by prop. \ref{CylinderSpectrumOverCWSpectrumIsGood}), which hence provides a functorial construction $X \maspto X \wedge (I_+)$ of cylinder objects for CW-spectra. Then constructing the connecting homomorphism uniformly by first constructing cofibration replacements via the [[factorization lemma]] ([prop](Introduction+to+Stable+homotopy+theory+--+P#FactorizationLemma)), with respect to these cylinder objects, and then forming cofibers, is functorial, because all three ingredients are (cylinders, replacement, cofibers). 

With this again the universal property of the ordinary cofiber gives the fourth vertical morphism needed for T3.

Axiom T4 follows in the same fashion: we may represent all spectra by CW-spectra and represent $f$ and $f'$ by cofibrations. Then the diagram in question exists and commutes by functoriality of the connecting homomorphisms and by the universal properties of cofibers as above.

=--




##### Long fiber-cofiber sequences

**Literature** ([Schwede 12, II.2](#Schwede12))

+-- {: .num_lemma #CompositesInADistinguishedTriangleAreZero}
###### Lemma

For $(Ho,\Sigma, CofSeq)$ a [[triangulated category]], def. \ref{CategoryWithCofiberSequences}, and 

$$
  A \overset{f}{\longrightarrow} B \overset{g}{\longrightarrow} B/A \overset{h}{\longrightarrow} \Sigma A
$$

a distinguished triangle, then 

$$
  g\circ f = 0
$$

is the [[zero morphism]].

=--

+-- {: .proof}
###### Proof

Consider the [[commuting diagram]]

$$
  \array{
    A 
      &\overset{id}{\longrightarrow}& 
    A 
      &\overset{}{\longrightarrow}&
    0
      &\overset{}{\longrightarrow}&
    \Sigma A
    \\
    \downarrow^{\mathrlap{id}} && \downarrow^{\mathrlap{f}}
    \\
    A 
      &\overset{f}{\longrightarrow}& 
    B 
      &\overset{g}{\longrightarrow}& 
    B/A 
      &\overset{h}{\longrightarrow}& 
    \Sigma A    
  }
  \,.
$$

Observe that the top part is a distinguished triangle by axioms T1 and T2 in def. \ref{CategoryWithCofiberSequences}. Hence by T3 there is an extension to 
a commuting diagram of the form

$$
  \array{
    A 
      &\overset{id}{\longrightarrow}& 
    A 
      &\overset{}{\longrightarrow}&
    0
      &\overset{}{\longrightarrow}&
    \Sigma A
    \\
    \downarrow^{\mathrlap{id}} && \downarrow^{\mathrlap{f}}
    && \downarrow
    && \downarrow^{\mathrlap{\Sigma f}}
    \\
    A 
      &\overset{f}{\longrightarrow}& 
    B 
      &\overset{g}{\longrightarrow}& 
    B/A 
      &\overset{h}{\longrightarrow}& 
    \Sigma A    
  }
  \,.
$$

Now the commutativity of the middle square proves the claim.

=--



+-- {: .num_prop #FiberCofiberSequencesInATriangulatedCategory}
###### Proposition

Let $(Ho,\Sigma, CofSeq)$ be a [[triangulated category]], def. \ref{CategoryWithCofiberSequences}, with [[hom-functor]] denoted by $[-,-]_\ast \colon Ho^{op}\times Ho \to Ab$. For $X\in Ho$ any object, and for $D\in CofSeq$ any distinguished triangle

$$
  D = (A \overset{f}{\longrightarrow} B \overset{g}{\longrightarrow} B/A \overset{h}{\longrightarrow} \Sigma A)
$$

then the sequences of [[abelian groups]]

1. (long cofiber sequence) 
    
   $$
    [\Sigma A, X]_\ast
      \overset{[h,X]_\ast}{\longrightarrow}
    [B/A,X]_\ast
      \overset{[g,X]_\ast}{\longrightarrow}
    [B,X]_\ast
      \overset{[f,X]_\ast}{\longrightarrow}
    [A,X]_\ast
   $$

1. (long fiber sequence)

   $$
     [X,A]_\ast
       \overset{[X,f]_\ast}{\longrightarrow}
     [X,B]_\ast
       \overset{[X,g]_\ast}{\longrightarrow}
     [X,B/A]_\ast
       \overset{[X,h]_\ast}{\longrightarrow}
     [X,\Sigma A]_\ast 
   $$

are [[long exact sequences]].

=--

+-- {: .proof}
###### Proof

Regarding the first case:

Since $g \circ f = 0$ by lemma \ref{CompositesInADistinguishedTriangleAreZero}, we have an inclusion $im([g,X]_\ast) \subset ker([f,X]_\ast)$. Hence it is sufficient to show that if $\psi \colon B \to X$ is in the kernel of $[f,X]_\ast$ in that $\psi \circ f = 0$, then there is $\phi \colon C \to X$ with $\phi \circ g = \psi$. To that end, consider the commuting diagram

$$
  \array{
    A 
      &\overset{f}{\longrightarrow}& 
    B 
      &\overset{g}{\longrightarrow}& 
    B/A 
      &\overset{h}{\longrightarrow}& 
    \Sigma A
    \\
    \downarrow && {}^{\mathllap{\psi}}\downarrow
    \\
    0 
      &\overset{}{\longrightarrow}&
    X
      &\overset{id}{\longrightarrow}&
    X
      &\overset{}{\longrightarrow}&
    0
  }
  \,,
$$

where the commutativity of the left square exhibits our assumption.

The top part of this diagram is a distinguished triangle by assumption, and the bottom part is by condition $T1$ in def. \ref{CategoryWithCofiberSequences}. Hence by condition T3 there exists $\phi$ fitting into a commuting diagram of the form

$$
  \array{
    A 
      &\overset{f}{\longrightarrow}& 
    B 
      &\overset{g}{\longrightarrow}& 
    B/A 
      &\overset{h}{\longrightarrow}& 
    \Sigma A
    \\
    \downarrow && {}^{\mathllap{\psi}}\downarrow && \downarrow^{\mathrlap{\phi}} && \downarrow
    \\
    0 
      &\overset{}{\longrightarrow}&
    X
      &\overset{id}{\longrightarrow}&
    X
      &\overset{}{\longrightarrow}&
    0
  }
  \,.
$$

Here the commutativity of the middle square exhibits the desired conclusion.

This shows that the first sequence in question is exact at $[B,X]_\ast$. Applying the same reasoning to the distinguished traingle $(g,h,-\Sigma f)$ provided by T2 yields exactness at $[C,X]_\ast$.

Regarding the second case: 

Again, from lemma \ref{CompositesInADistinguishedTriangleAreZero} it is immediate that 

$$
  im([X,f]_\ast) \subset ker([X,g]_\ast)
$$

so that we need to show that for $\psi \colon X \to B$ in the kernel of $[X,g]_\ast$, hence such that $g\circ \psi = 0$, then there exists $\phi \colon X \to A$ with $f \circ \phi = \psi$.

To that end, consider the commuting diagram

$$
  \array{
    X &\longrightarrow& 0 &\longrightarrow& \Sigma X &\overset{- id}{\longrightarrow}& \Sigma X
    \\
    \downarrow^{\mathrlap{\psi}} && \downarrow
    \\
     B 
       &\overset{g}{\longrightarrow}&
     B/A
       &\overset{h}{\longrightarrow}&
     \Sigma A
       &\overset{-\Sigma f}{\longrightarrow}&
     \Sigma B
  }
  \,,
$$

where the commutativity of the left square exhibits our assumption.

Now the top part of this diagram is a distinguished triangle by conditions T1 and T2 in def. \ref{CategoryWithCofiberSequences}, while the bottom part is a distinguished triangle by applying T2 to the given distinguished triangle. Hence by T3 there exists $\tilde \phi \colon \Sigma X \to \Sigma A$ such as to extend to a commuting diagram of the form

$$
  \array{
    X &\longrightarrow& 0 &\longrightarrow& \Sigma X &\overset{- id}{\longrightarrow}& \Sigma X
    \\
    \downarrow^{\mathrlap{\psi}} 
      && 
    \downarrow
      &&
    \downarrow^{\mathrlap{\tilde \phi}}
      &&
    \downarrow^{\mathrlap{\Sigma \psi}}
    \\
     B 
       &\overset{g}{\longrightarrow}&
     B/A
       &\overset{h}{\longrightarrow}&
     \Sigma A
       &\overset{-\Sigma f}{\longrightarrow}&
     \Sigma B
  }
  \,,
$$

At this point we appeal to the condition in def. \ref{CategoryWithCofiberSequences} that $\Sigma \colon Ho \to Ho$ is an [[equivalence of categories]], so that in particular it is a [[fully faithful functor]]. It being a [[full functor]] implies that there exists $\phi \colon X \to A$ with $\tilde \phi = \Sigma \phi$. It being faithful then implies that the whole commuting square on the right is the image under $\Sigma$ of a commuting square

$$
  \array{
    X &\overset{-id}{\longrightarrow}& X
    \\
    {}^{\mathllap{\phi}}\downarrow && \downarrow^{\mathrlap{\psi}}
    \\
    A &\underset{-f}{\longrightarrow}& B
  }
  \,.
$$

This exhibits the claim to be shown.

=--

+-- {: .num_lemma #TwoOutOfThreeForMorphismsOfDistinguishedTriangles}
###### Lemma

Consider a morphism of distinguished triangles in a triangulated category (def. \ref{CategoryWithCofiberSequences}):

$$
  \array{    
   A &\overset{}{\longrightarrow}& B &\overset{g}{\longrightarrow}& B/A &\overset{h}{\longrightarrow}& \Sigma A      
   \\
   \downarrow^{\mathrlap{a}} 
   && \downarrow^{\mathrlap{b}} 
   && \downarrow^{\mathrlap{c}}
   && \downarrow^{\mathrlap{\Sigma a}}
   \\
   A' &\overset{}{\longrightarrow}& B' &\overset{}{\longrightarrow}& B'/A' &\overset{}{\longrightarrow}& \Sigma A'          
   }
 \,.
$$

If two out of $\{a,b,c\}$ are isomorphisms, then so is the third.

=--

+-- {: .proof}
###### Proof

Consider the image of the situation under the hom-functor $[X,-]_\ast$ out of any object $X$:

$$
  \array{    
   [X,A]_\ast &\overset{}{\longrightarrow}& [X,B]_\ast &\overset{g}{\longrightarrow}& [X,B/A]_\ast &\overset{h}{\longrightarrow}& [X,\Sigma A]_\ast &\longrightarrow& [X,\Sigma B]_\ast
   \\
   \downarrow^{\mathrlap{a_\ast}} 
   && \downarrow^{\mathrlap{b_\ast}} 
   && \downarrow^{\mathrlap{c_\ast}}
   && \downarrow^{\mathrlap{(\Sigma a)_\ast }}
   && \downarrow^{\mathrlap{(\Sigma b)_\ast }}
   \\
   [X,A']_\ast &\overset{}{\longrightarrow}& [X,B']_\ast &\overset{}{\longrightarrow}& [X,B'/A']_\ast &\overset{}{\longrightarrow}& [X,\Sigma A']_\ast &\longrightarrow& [X,\Sigma B']_\ast           
   }
 \,,
$$

where we extended one step to the right using axiom T2 (def. \ref{CategoryWithCofiberSequences}).

By prop. \ref{FiberCofiberSequencesInATriangulatedCategory} here the top and bottom are [[exact sequences]].

So assume the case that $a$ and $b$ are isomorphisms, hence that $a_\ast$, $b_\ast$, $(\Sigma a)_\ast$ and $(\Sigma b)_\ast$ are isomorphisms. Then by exactness of the horizontal sequences the [[five lemma]] implies that $c_\ast$ is an isomorphism. Since this holds [[natural transformation|naturally]] for all $X$, the [[Yoneda lemma]] then implies that $c$ is an isomorphism.

If instead $b$ and $c$ are isomorphisms, apply this same argument to the triple $(b,c,\Sigma a)$ to conclude that $\Sigma a$ is an isomorphism. Since $\Sigma$ is an [[equivalence of categories]], this implies then that $a$ is an isomorphism.

Analogously for the third case.

=--

+-- {: .num_lemma #TwoOutOfThreeForMorphismsOfDistinguishedTriangles}
###### Lemma

If $(g,h,-\Sigma f)$ is a distinguished triangle in a triangulated category (def. \ref{CategoryWithCofiberSequences}), then so is $(f,g,h)$.

=--

+-- {: .proof}
###### Proof

By T0 there is some distinguished triangle of the form $(f,g',h')$. By T2 this gives a distinguished triangle $(-\Sigma f, -\Sigma g', -\Sigma h')$. By T3 there is a morphism $c'$ giving a commuting diagram

$$
  \array{
    \Sigma A 
      &\overset{-\Sigma f}{\longrightarrow}&
    \Sigma B
      &\overset{-\Sigma g}{\longrightarrow}&
    \Sigma C
      &\overset{-\Sigma h}{\longrightarrow}&    
    \Sigma^2 A
    \\
    {}^{\mathllap{=}}\downarrow
    &&
    {}^{\mathllap{=}}\downarrow
    &&
    {}^{\mathllap{c'}}\downarrow
    &&
    {}^{\mathllap{=}}\downarrow
    \\
    \Sigma A 
      &\overset{-\Sigma f}{\longrightarrow}&
    \Sigma B
      &\overset{-\Sigma g'}{\longrightarrow}&
    \Sigma C
      &\overset{-\Sigma h'}{\longrightarrow}&    
    \Sigma^2 A
  }
  \,.
$$

Now lemma \ref{TwoOutOfThreeForMorphismsOfDistinguishedTriangles} gives that $c'$ is an isomorphism. Since $\Sigma$ is an [[equivalence of categories]], there is an isomorphism $c$ such that $c' = \Sigma c$. This $c$ exhibits an isomorphism between $(f,g,h)$ and $(f,g',h')$. Since the latter is distinguished, so is the former, by T0.

=--

In conclusion: 

+-- {: .num_prop #LongFiberSequencesOfMapsOfSpectra}
###### Proposition

Let 

$$
  X 
    \overset{f}{\longrightarrow} 
  Y
    \overset{g}{\longrightarrow}
  Z
$$ 

be a [[homotopy cofiber sequence]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyFiber)) of spectra in the [[stable homotopy category]] (def. \ref{TheStableHomotopyCategory}) $Ho(Spectra)$. Let $A \in Ho(Spectra)$ be any other spectrum. Then there are [[long exact sequences]] of [[abelian groups]] of the form

$$
   \cdots
    \longrightarrow
  [A, \Omega Y]
    \overset{-\Omega g}{\longrightarrow}
  [A, \Omega Z]_\ast
    \overset{}{\longrightarrow}
  [A,X]_\ast
    \overset{f_\ast}{\longrightarrow}
  [A,Y]_\ast
    \overset{g_\ast}{\longrightarrow}
  [A,Z]
    \overset{}{\longrightarrow}
  [A,\Sigma X]
     \overset{-\Sigma f}{\longrightarrow}
  [A, \Sigma Y]
     \longrightarrow
   \cdots
  \,.
$$

=--

+-- {: .proof}
###### Proof

By prop. \ref{StableHomotopyCategoryIsTriangulated} this is a special case of prop. \ref{FiberCofiberSequencesInATriangulatedCategory}.

=--


In particular there are long exact sequences of [[stable homotopy groups]] extending in both directions:

+-- {: .num_lemma #StableHomotopyGrouspAsHomsOutOfSphereSpectrum}
###### Lemma

Let $X \in SeqSpec(Top_{cg})$ be any [[sequential spectrum]], then there is an [[isomorphism]]

$$
  \pi_0(X)
    \simeq
  [\mathbb{S}, X]_\ast
$$

between its [[stable homotopy group]] in degree 0 (def. \ref{StableHomotopyGroups}) and the hom-group (according to def. \ref{AdditiveCategory}, prop. \ref{TheStableHomotopyCategoryIsAdditive}) in the [[stable homotopy category]] (def. \ref{TheStableHomotopyCategory}) from the [[sphere spectrum]] (def. \ref{StandardSphereSpectrum}) into $X$. 

=--

+-- {: .proof}
###### Proof

The hom-set in the homotopy category is equivalently given by the [[left homotopy]]-equivalence classes out of a cofibrant representative of $\mathbb{S}$ into a fibrant representative of $X$ ([lemma](Introduction+to+Stable+homotopy+theory+--+P#HomsOutOfCofibrantIntoFibrantComputeHomotopyCategory)).

The standard sphere spectrum $\mathbb{S}_{std} \coloneqq \Sigma^\infty S^0$ is a [[CW-spectrum]] and hence cofibrant, by prop. \ref{CellSpectraAreCofibrantInModelStructureOnTopologicalSequentialSpectra}. Moreover, this implies by prop. \ref{CylinderSpectrumOverCWSpectrumIsGood} that left homotopies out of $\mathbb{S}_{str}$ are represented by the standard sequential [[cylinder spectrum]] 

$$
  \mathbb{S}_{std} \wedge (I_+)
  \simeq
  \Sigma^\infty (I_+)
  \,.
$$

By prop. \ref{SpectrificationIsFibrantReplacement} a fibrant replacement for $X$ is provided by its [[spectrification]] $Q X$ according to def. \ref{SpectrificationForTopologicalSequentialSpectra}. 

So it follows that $[\mathbb{S},X]_\ast$ is given by left homotopy classes of morphisms 

$$
  \Sigma^\infty S^0 = \mathbb{S}_{std} \longrightarrow Q X
$$

in $SeqSpec(Top_{cg})$. By the $(\Sigma^\infty \dashv \Omega^\infty)$-adjunction (prop. \ref{SigmaInfinityOmegaInfinity}) these are equivalently morphisms

$$
  S^0 \longrightarrow (Q X)_0
$$

in $Top^{\ast/}_{cg}$. Hence equivalently morphisms

$$
  \ast \longrightarrow (Q X)_0
$$

in $Top_{cg}$, hence equivalently points in $(Q X)_0$. Analogously, a [[left homotopy]] 

$$
  \Sigma^\infty (I_+) \longrightarrow (Q X)_0
$$

in $SeqSpec(Top_{cg})$ is equivalently a path

$$
  I \longrightarrow (Q X)_0
$$

in $Top_{cg}$. 

In conclusion this establishes an isomorphism

$$
  [\mathbb{S},X]_\ast 
    \simeq  
  \pi_0( (Q X)_0 )
$$

with $\pi_0$ of the 0-component of $Q X$. With this the statement follows with example \ref{StableHomotopyGroupsOfOmegaSpectrum}, since $Q X$ is an Omega-spectrum, by prop. \ref{PropertiesOfSpectrificationForTopologicalSequentialSpectra}.

=--

As a consequence, we finally obtain the abstract homotopy theoretic verification of the long exact sequences of stable homotopy groups that we constructed via [[mapping cones]] in prop. \ref{LongExactSequenceofStableHomotopyGroupsViaMappingCones}:

> (the following secretly uses left propertness)

+-- {: .num_prop #LongExactSequenceOfStableHomotopyGroups}
###### Proposition

Let 

$$
  X 
    \overset{f}{\longrightarrow} 
  Y
    \overset{g}{\longrightarrow}
  Z
$$ 

be a [[homotopy cofiber sequence]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyFiber)) in the [[stable homotopy category]] (def. \ref{TheStableHomotopyCategory}). Then there is induced a [[long exact sequence of homotopy groups|long exact sequence]] of [[stable homotopy groups]] (def. \ref{StableHomotopyGroups}) of the form

$$
  \cdots
   \longrightarrow
  \pi_{\bullet + 1}(Z)
    \longrightarrow
  \pi_\bullet(X)
    \overset{f_\ast}{\longrightarrow}
  \pi_\bullet(Y)
    \overset{g_\ast}{\longrightarrow}
  \pi_\bullet(Z)
    \overset{}{\longrightarrow}
  \pi_{\bullet-1}(X)
    \longrightarrow
   \cdots
  \,.
$$


=--

+-- {: .proof}
###### Proof

Via lemmma \ref{StableHomotopyGrouspAsHomsOutOfSphereSpectrum} this is a special case of prop. \ref{LongFiberSequencesOfMapsOfSpectra}.

=--

This finally allows to prove the technical lemma used in prop. \ref{StableEquivalenceInSeqSpecIsStableWeakHomotopyEquivalence}:

+-- {: .num_lemma #CofibrantStableWeakHomotopyEquivalencesPreservedUnderPushout}
###### Lemma

The class of morphisms of sequential spectra that are both stable cofibrations (def. \ref{ClassesOfMorphismsOfTheStableModelStructureOnSequentialSpectra}) as well as [[stable weak homotopy equivalences]] (def. \ref{StableWeakHomotopyEquivalenceOfSequentialTopologicalSpectra}) is preserved under [[pushout]].

=--

+-- {: .proof}
###### Proof

Let $f \colon X \to Y$ be a stable cofibration that is also a stable weak homotopy equivalence, and let $g \colon X \to X'$ be any morphism. Consider the [[pushout]] diagram 

$$
  \array{
     X &\overset{f}{\longrightarrow}& Y &\longrightarrow& cof(f)
     \\
     {}^{\mathllap{g}}\downarrow 
       &(po)& 
     \downarrow
       &&
     \downarrow^{\mathrlap{\simeq}}
     \\
     X' &\underset{g_\ast f}{\longrightarrow}& Y' &\longrightarrow& cof(g_\ast f)
  }
  \,.
$$

The induced map on [[cofibers]] on the right is an isomorphism by the [[pasting law]]. Since $f$ is a cofibration, so is its pushout $g_\ast f$ (by the model structure), and hence both these cofibers are actually [[homotopy cofibers]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyFiber)). Hence by prop. \ref{LongExactSequenceOfStableHomotopyGroups} there is a diagram of [[stable homotopy groups]] of the form

$$
  \array{
     \pi_{\bullet+1}(cof(f))
     &\longrightarrow&
     \pi_\bullet(X) &\overset{f_\ast}{\longrightarrow}& \pi_\bullet(Y) &\longrightarrow& \pi_\bullet(cof(f))
     \\
     {}^{\mathllap{\simeq}}\downarrow 
       && 
     {}^{\mathllap{g_\ast}}\downarrow 
       && 
     \downarrow
       &&
     \downarrow^{\mathrlap{\simeq}}
     \\
     \pi_{\bullet+1}(cof(g_\ast f))
     &\longrightarrow&
     \pi_\bullet(X') &\underset{(g_\ast f)_\ast}{\longrightarrow}& \pi_\bullet(Y') &\longrightarrow& \pi_\bullet(cof(g_\ast f))
  }
$$

where both horizontal sequences are exact. That $f$ is a stable weak homotopy equivalence means precisely that $f_\ast$ is an isomorphism, and hence exactness of the top sequence implies that $\pi_\bullet(cof(f)) = 0$. Then the isomorphisms on the right and left imply that also $\pi_\bullet(cof(g_\ast f)) = 0$ and so exactness of the bottom sequence implies that $(g_\ast f)_\ast$ is an isomorphism, hence that the pushout $g_\ast f$ is a stable weak homotopy equivalence.


=--


### **1.2)** Structured spectra
 {#DiagramSpectra}

Given that [[spectra]] are the analog in [[homotopy theory]] of [[abelian groups]], we want to consider [[algebra]] -- the theory of [[rings]] and their [[modules]] -- [[internalization|internal]] to spectra. This "[[higher algebra]]" ([below](#HigherAlgebra)) accordingly is the theory of [[ring spectra]] and [[module spectra]].

[[!include homological and higher algebra -- table]]

Hence where a [[ring]] is equivalently a [[monoid]] with respect to the [[tensor product of abelian groups]], we are after a corresponding [[tensor product]] of [[spectra]]. This is to be the [[smash product of spectra]], induced by the [[smash product]] on [[pointed topological spaces]]/[[pointed object|pointed]] [[simplicial sets]].


There is a key point to be dealt with here: the [[smash product of spectra]] has to exhibit a certain _graded commutativity_. Informally, there are two ways to see this:

First, we have seen above that under the [[Dold-Kan correspondence]] [[chain complexes]] yield examples of spectra. But the [[tensor product of chain complexes]] is graded commutative.

Second, more fundamentally, we see in the discussion of the [[Brown representability theorem]] ([here](#BrownRepresentabilityTheorem)) that every ([[sequential spectrum|sequential]]) [[spectrum]] $A$ induces a [[generalized homology theory]] given by the formula $X \mapsto \pi_\bullet(E \wedge X)$ (where the smash product is just the degreewise smash of pointed objects). By the [[suspension isomorphism]] this is such that for $X = S^n$ the [[n-sphere]], then $\pi_{\bullet\geq 0}(E \wedge S^n) \simeq \pi_{\bullet \geq 0}(E_n)$. This means that instead of thinking of a [[sequential spectrum]], def. \ref{SequentialSpectra}, as indexed on the [[natural numbers]] equipped with [[addition]] $(\mathbb{N},+)$, it may be more natural to think of sequential spectra as indexed on the [[n-spheres]] equipped with their smash product of pointed spaces $(\{S^n\}_n, \wedge)$. 


+-- {: .num_prop #GradedCommutativityOfSmashOfSpheres}
###### Proposition

There are [[homeomorphisms]] between [[n-spheres]] and their [[smash products]]

$$
  \phi_{n_1,n_2}
  \;\colon\;
  S^{n_1} \wedge S^{n_2}
  \stackrel{\simeq}{\longrightarrow}
  S^{n_1 + n_2}
$$

such that in [[Ho(Top)]] there are [[commuting diagrams]] like so:

$$
  \array{
    (S^{n_1} \wedge S^{n_2}) \wedge S^{n_3}
    &&\stackrel{\simeq}{\longrightarrow}&&
    S^{n_1} \wedge (S^{n_2} \wedge S^{n_3})
    \\
    {}^{\mathllap{\phi_{n_1,n_2} \wedge id}}\downarrow 
    && && \downarrow^{\mathrlap{id \wedge \phi_{n_2,n_3}}}
    \\
    S^{n_1+n_2} \wedge S^{n_3}
    && &&
    S^{n_1}\wedge S^{n_2 + }
    \\
    & {}_{\mathllap{\phi_{n_1+n_2, n_3}}}\searrow && \swarrow_{\mathrlap{\phi_{n_1,n_2+n_3}}}
    \\
    && 
    S^{n_1+n_2 + n_3}
  }
  \,.
$$

and

$$
  \array{
    S^{n_1} \wedge S^{n_2}
    &\stackrel{b_{n_1,n_2}}{\longrightarrow}&
    S^{n_2} \wedge S^{n_1}
    \\
    {}^{\mathllap{\phi_{n_1,n_2}}}\downarrow && \downarrow^{\mathrlap{\phi_{n_2,n_1}}}
    \\
    S^{n_1 + n_2}
    &\stackrel{(-1)^{n_1 n_2}}{\longrightarrow}&
    S^{n_1 + n_2}
  }
  \,,
$$

where here $(-1)^n \colon S^n \to S^n$ denotes the homotopy class of a [[continuous function]] of [[degree of a continuous function|degree]] $(-1)^n \in \mathbb{Z} \simeq [S^n, S^n]$.


=--


+-- {: .proof}
###### Proof

With the [[n-sphere]] $S^n$ realized as the [[one-point compactification]] of the [[Cartesian space]] $\mathbb{R}^n$, then $\phi_{n_1,n_2}$ is given by the identity on [[coordinates]] and the [[braiding]] homeomorphism

$$
  b_{n_1,n_2}
  \;\colon\;
  S^{n_1} \wedge S^{S^2}
  \stackrel{\sigma}{\longrightarrow}
  S^{n_2} \wedge S^{n_2}
$$

is given by permuting the [[coordinates]]:

$$
  (x_1, \cdots, x_{n_1}, y_1, \cdots, y_{n_2})
  \mapsto
  (y_1, \cdots, y_{n_2}, x_1, \cdots, x_{n_1})
  \,.
$$

This has [[degree of a continuous map|degree]] $(-1)^{n_1 n_2}$ .

=--


This phenomenon suggests that if we "[[categorify]]" the [[natural numbers]] to the [[n-spheres]] and think of the $n$th component space of a [[sequential spectrum]] as being the value assigned to the [[n-sphere]]

$$
  E_n \simeq E(S^n)
$$

then there should be a possibly non-trivial [[action]] of the [[symmetric group]] $\Sigma_n$ on $E_n$, due to the fact that there is such an action of $S^n$ which is non-trivial according to prop. \ref{GradedCommutativityOfSmashOfSpheres}.

We discuss two ways of making this precise below in  _[Symmetric and orthogonal spectra](#SymmetricSpectra)_, and we discuss how these are unified by a concept of [[module objects]] over a [[monoid object]] representing the [[sphere spectrum]] below in _[S-modules](#SModules)_.

The general abstract theory for handling this is _[[monoidal category|monoidal]] and [[enriched category theory]]_. We first develop the relevant basics in _[Monoidal and enriched categories](#MonoidalAndEnrichedCategories)_


#### Symmetric and orthogonal spectra
 {#SymmetricSpectra}

**Literature.** ([Schwede 12](#Schwede12)) 

$\,$

In order to accomodate the graded commutativity phenomenon of spheres in prop. \ref{GradedCommutativityOfSmashOfSpheres}, we enrich the model of [[stable homotopy theory]] based on [[sequential spectra]], def. \ref{SequentialSpectra}, by adding in [[mathematical structure|structure]] which captures the fact that the $n$th component $X_n$ of a sequential spectrum $X$ is to be thought of as the evaluation on the [[n-sphere]] and thus ought to be [[action|acted]] on by the [[automorphisms]] of the $n$-sphere. 

Taking into account just the automorphisms by [[coordinate]] [[permutations]] on $S^n \simeq (S^1)^{\wedge^n}$ yields the concept of _[[symmetric spectra]]_.
Taking into account the automorphisms by [[orthogonal group|orthogonal transformations]] on $S^n \simeq (\mathbb{R}^n)^+$ yields the concept of _[[orthogonal spectra]]_. Using _all_ automorphisms yields the concept of _pre-[[excisive functors]]_.

To contrast these more structured models for spectra with the plain [[sequential spectra]], they are sometimes referred to as _[[highly structured spectra]]_.

Below in _[S-modules](#SModules)_ we give a unified discussion of all four models of spectra thus obtained (sequential, symmetric, orthogonal, excisive). Further below in _[The stable model structures](#TheStableModelStructures)_ we use this to construct and understand the [[model structures on spectra]] that present [[stable homotopy theory]].

$\,$

+-- {: .num_defn #SymmetricSpectrum}
###### Definition

A **[[symmetric spectrum]]** $X$ in [[sSet]] is

1. a sequence $\{X_n| n \in \mathbb{N}\}$ of [[pointed object|pointed]] [[simplicial sets]];

1. a baspoint preserving left [[action]] of the [[symmetric group]] $\Sigma_n$ on $X_n$;

1. a sequence of morphisms of pointed simplicial sets $\sigma_n \colon X_n \wedge S^1 \longrightarrow X_{n+1}$ 

such that

* for all $n, k \in \mathbb{N}$ the [[composition|composite]]

  $$
    X_n \wedge S^{k} \stackrel{\sigma_n \wedge id}{\longrightarrow} X_{n+1} \wedge S^{k-1} \stackrel{\sigma_{n+1}\wedge id}{\longrightarrow} \cdots \stackrel{\sigma_{n+k-1}}{\longrightarrow} X_{n+k}
  $$

  [[intertwiner|intertwines]] the $\Sigma_{n+k}$-[[action]].

A [[morphism]] of symmetric spectra $f\colon X \longrightarrow Y$ is

* a sequence of morphisms of pointed simplicial sets $f_n \colon X_n \longrightarrow Y_n$

such that

1. each $f_n$ [[intertwiner|intetwines]] the $\Sigma_n$-[[action]];

1. the following [[commuting diagram|diagrams commute]]

   $$
     \array{
        X_n \wedge S^1 &\stackrel{f_n \wedge id}{\longrightarrow}& Y_n \wedge S^1
        \\
        \downarrow^{\mathrlap{\sigma^X_n}} && \downarrow^{\mathrlap{\sigma^Y_n}}
        \\
        X_{n+1} &\stackrel{f_{n+1}}{\longrightarrow}& Y_{n+1}
     }
     \,.
   $$

=--

+-- {: .num_defn #OrthogonalSpectrum}
###### Definition

An _[[orthogonal spectrum]]_ $X$ consists of for each $n \in \mathbb{N}$

1. a sequence of [[pointed topological spaces]] $X_n$ (the _$n$th level_);

1. a base-point preserving [[continuous function|continuous]] [[action]] of the [[topological group|topological]] [[orthogonal group]] $O(n)$ on $X_n$;

1. based-point preserving [[continuous functions]] $\sigma_n \colon X_n \wedge S^1 \longrightarrow X_{n+1}$ from the [[smash product]] with the [[1-sphere]] (the _$n$th structure map_)

such that for all $n,k \in \mathbb{N}$ with $k \geq 1$

* the [[continuous functions]] $\sigma^k \colon X_n \wedge S^k \longrightarrow X_{n+k}$ given as the [[compositions]]

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


#### Categorical algebra
 {#MonoidalAndEnrichedCategories}

##### Monoidal and enriched categories

* [[monoidal category]] 

  * [[monoidal functor]], [[monoidal adjunction]]

  * [[symmetric monoidal category]]

  * [[symmetric monoidal functor]]  

* [[monoid object]], [[module object]]


* [[enriched category]]

  * [[enriched functor category]]

* [[Day convolution]]


##### Monoidal homotopy theory

We now combine the concepts of [[model category]] and [[monoidal category]].


+-- {: .num_defn #MonoidalModelCategory}
###### Definition

A (symmetric) **monoidal model category** is [[model category]] $\mathcal{C}$
equipped with the structure of a  [[closed monoidal category|closed]] [[symmetric monoidal category]] $(\mathcal{C}, \otimes, I)$
such that the following two compatibility conditions are satisfied

1. ([[pushout-product axiom]]) For every pair of cofibrations $f \colon X \to Y$ and $f' \colon X' \to Y'$, their [[pushout-product]], hence the induced morphism out of the cofibered [[coproduct]] over ways of forming the tensor product of these objects

   $$
     (X \otimes Y') \coprod_{X \otimes X'} (Y \otimes X')
     \longrightarrow
     Y \otimes Y'
     \,,
   $$

   is itself a cofibration, which, furthermore, is acyclic if $f$ or $f'$ is.

   (Equivalently this says that the [[tensor product]] $\otimes : C \times C \to C$ is a left [[Quillen bifunctor]].)

1. (unit axiom) For every cofibrant object $X$ and every cofibrant resolution $\emptyset \hookrightarrow Q I \stackrel{p_I}{\longrightarrow} \ast$ of the [[tensor unit]] $I$, the resulting morphism

   $$
     Q I \otimes X \stackrel{p_I \otimes X}{\longrightarrow} I\otimes X \stackrel{\simeq}{\longrightarrow} X
   $$ 

  is a weak equivalence.


=--

+-- {: .num_remark }
###### Remark

The [[pushout-product axiom]] in def. \ref{MonoidalModelCategory} implies that for $X$ a cofibrant object, then the functor $X \otimes (-)$ preserves cofibrations and acyclic cofibrations.

In particular if the [[tensor unit]] $I$ happens to be cofibrant, then the unit axiom in def. \ref{MonoidalModelCategory} is implied by the pushout-product axiom. 

=--

+-- {: .num_defn #MonoidAxiom}
###### Definition

We say a [[monoidal model category]], def. \ref{MonoidalModelCategory}, satisfies the **[[monoid axiom]]**, def. \ref{MonoidalModelCategory}, if every morphism that is obtained as a [[transfinite composition]] of [[pushouts]] of [[tensor products]] $X\otimes f$ of acyclic cofibrations $f$ with any object $X$ is a weak equivalence.

=--

([Schwede-Shipley 00, def. 3.3.](#SchwedeShipley)).

+-- {: .num_remark}
###### Remark

In particular, the axiom in def. \ref{MonoidAxiom} says that for every object $X$ the functor $X \otimes (-)$ sends acyclic cofibrations to weak equivalences.

=--


+-- {: .num_prop #MonoidalStructureOnHomotopyCategoryOfMonoidalModelCategory}
###### Proposition

Let $(\mathcal{C}, \otimes, I)$ be a [[monoidal model category]]. Then the [[left derived functor]] of the tensor product exsists and makes the [[homotopy category of a model category|homotopy category]] into a [[monoidal category]] $(Ho(\mathcal{C}), \otimes^L, \gamma(I))$.

If in in addition $(\mathcal{C}, \otimes)$ satisfies the [[monoid axiom in a monoidal model category|monoid axiom]], then the [[localization]] functor $\gamma\colon \mathcal{C}\to Ho(\mathcal{C})$ carries the structure of a [[lax monoidal functor]]

$$
  \gamma
  \;\colon\;
  (\mathcal{C}, \otimes, I)
   \longrightarrow
  (Ho(\mathcal{C}), \otimes^L , \gamma(I))
  \,.
$$

=--

+-- {: .proof}
###### Proof

Consider the explicit model of $Ho(\mathcal{C})$ as the category of fibrant-cofibrant objects in $\mathcal{C}$ with left/right-homotopy classes of morphisms between them (discussed at _[[homotopy category of a model category]]_).

A [[derived functor]] exists if its restriction to this subcategory preserves weak equivalences. Now the [[pushout-product axiom]] implies that on the subcategory of cofibrant objects the functor $\otimes$ preserves acyclic cofibrations, and then the preservation of all weak equivalences follows by [[Ken Brown's lemma]]. 

Hence $\otimes^L$ exists and its [[associativity]] follows simply by restriction. It remains to see its [[unitality]].

To that end, consider the construction of the localization functor $\gamma$ via a fixed but arbitrary choice of (co-)fibrant replacements $Q$ and $R$, assumed to be the identity on (co-)fibrant objects. We fix notation as follows:

$$
\emptyset \underoverset{\in Cof}{i_X}{\longrightarrow} Q X \underoverset{\in W \cap Fib}{p_x}{\longrightarrow} X
\;\;\,,\;\;
X \underoverset{\in W \cap Cof}{j_X}{\longrightarrow} R X \underoverset{\in Fib}{q_x}{\longrightarrow} \ast
  \,.
$$

 
Now to see that $\gamma(I)$ is the [[tensor unit]] for $\otimes^L$, notice that in the [[zig-zag]]

$$
  (R Q I) \otimes (R Q X)
    \overset{j_{Q I} \otimes (R Q X)}{\longleftarrow}
  (Q I) \otimes (R Q X)
    \overset{(Q I)\otimes j_{Q X}}{\longleftarrow}
  (Q I) \otimes (Q X)
    \overset{p_I \otimes (Q X)}{\longrightarrow}
  I \otimes Q X
    \simeq
  Q X
$$

all morphisms are weak equivalences: For the first two this is due to the [[pushout-product axiom]], for the third this is due to the unit axiom on a monoidal model category. It follows that under $\gamma(-)$ this zig-zig gives an isomorphism

$$
  \gamma(I) \otimes^L \gamma(X)\simeq \gamma(X)
$$

and similarly for tensoring with $\gamma(I)$ from the right.

To exhibit lax monoidal structure on $\gamma$, we need to construct a [[natural transformation]]

$$
  \gamma(X) \otimes^L \gamma(Y) \longrightarrow \gamma(X \otimes Y)
$$

and show that it satisfies the the appropriate [[associativity]] and [[unitality]] condition.

By the definitions at _[[homotopy category of a model category]]_, the morphism in question is to be of the form

$$
  (R Q X) \otimes (R Q Y) \longrightarrow R Q (X\otimes Y)
$$


To this end, consider the [[zig-zag]]

$$
  (R Q X) \otimes (R Q Y)
   \underoverset{\in Cof \cap W}{j_{Q X} \otimes R Q Y}{\longleftarrow}
  (Q X) \otimes (R Q Y)
    \underoverset{\in Cof \cap W}{(Q X) \otimes  j_{Q Y} }{\longleftarrow}
  (Q X) \otimes (Q Y)
    \overset{p_X \otimes (Q Y)}{\longrightarrow}
  X \otimes (Q Y)
    \overset{Y \otimes p_Y}{\longrightarrow}   
  X \otimes Y
  \,,
$$

and observe that the two morphisms on the left are weak equivalences, as indicated, by the [[pushout-product axiom]] satisfied by $\otimes$.

Hence applying $\gamma$ to this zig-zag, which is given by the two horizontal part of the following digram

$$
  \array{
    (R Q X) \otimes (R Q Y) &\longleftarrow& R( Q X \otimes Q Y ) &\longrightarrow& R Q (X \otimes Y)
    \\
    \uparrow^{\mathrlap{id}} && \uparrow^{\mathrlap{j_{Q X \otimes Q Y}}} && \uparrow^{\mathrlap{j_{Q(X \otimes Y)}}}
    \\
    \downarrow^{\mathrlap{id}} && \downarrow^{\mathrlap{id}} && \downarrow^{\mathrlap{p_{X\otimes Y}}}
    \\
    (R Q X) \otimes (R Q Y)
     &\underoverset{\in Cof \cap W}{j_{Q X} \otimes j_{Q Y}}{\longleftarrow}&
    (Q X) \otimes (Q Y)
      &\overset{p_X \otimes p_Y}{\longrightarrow}&
    X \otimes Y
  }
  \,,
$$

and inverting the first two morphisms, this yields a natural transformation as required. 


To see that this satisfies associativity if the monoid axiom holds, tensor the entire diagram above on the right with $(R Q Z)$ and consider the following [[pasting]] composite:

$$
  \array{
    (R Q X) \otimes (R Q Y) \otimes (R Q Z) &\longleftarrow& R( Q X \otimes Q Y ) \otimes (R Q Z) &\longrightarrow& (R Q (X \otimes Y)) \otimes (R Q Z)
    \\
    \uparrow^{\mathrlap{id}} && \uparrow^{\mathrlap{j_{Q X \otimes Q Y} \otimes id }} && \uparrow^{\mathrlap{j_{Q(X \otimes Y)}\otimes id }}
    \\
    && && Q(X \otimes Y) \otimes (R Q Z) &\overset{id \otimes j_{Q Z}}{\longleftarrow}& Q(X\otimes Y) \otimes (Q Z)
    \\
       \downarrow^{\mathrlap{id}} && \downarrow^{\mathrlap{id}} 
    && 
      \downarrow^{\mathrlap{p_{(X\otimes Y)} \otimes id }} 
    &(\star)& 
     \downarrow^{\mathrlap{p_{(X \otimes Y)} \otimes id}}
    \\
    (R Q X) \otimes (R Q Y) \otimes (R Q Z)
     &\underoverset{\in Cof \cap W}{j_{Q X} \otimes j_{Q Y} \otimes id}{\longleftarrow}&
    (Q X) \otimes (Q Y) \otimes (R Q Z)
      &\overset{p_X \otimes p_Y \otimes id}{\longrightarrow}&
    X \otimes Y \otimes (R Q Z)
      &\underset{id \otimes j_{Q Z}}{\longleftarrow}&
    X\otimes Y \otimes Q Z 
      &\overset{id \otimes p_Z}{\longrightarrow}& 
    X \otimes Y \otimes Z  
  }
  \,,
$$

Observe that under $\gamma$ the total top [[zig-zag]] in this diagram gives

$$
  (\gamma(X) \otimes^L \gamma(Y)) \otimes^L \gamma(Z)
  \to \gamma(X\otimes Y)\otimes^L \gamma(Z)
  \,.
$$

Now by the [[monoid axiom in a monoidal model category|monoid axiom]] (but not by the pushout-product axiom!), the horizontal maps in the square in the bottom right (labeled $\star$) are weak equivalences. This implies that the total horizontal part of the diagram is a [[zig-zag]] in the first place, and that under $\gamma$ the total top zig-zag is equal to the image of that total bottom zig-zag. But by functoriality of $\otimes$, that image of the bottom zig-zag is 

$$
  \gamma(p_X \otimes p_Y \otimes p_Z) 
  \circ 
  \gamma(j_{Q X} \otimes j_{Q Y} \otimes j_{Q Z})^{-1}
  \,.
$$

The same argument applies to left tensoring with $R Q Z$ instead of right tensoring, and so in both cases we reduce to the same morphism in the homotopy category, thus showing the associativity condition on the transformation that exhibits $\gamma$ as a lax monoidal functor.

=--



#### $\mathbb{S}$-Modules
 {#SModules}

We now give a unified discussion of the categories of

1. [[sequential spectra]]

1. [[symmetric spectra]]

1. [[orthogonal spectra]]

1. pre-[[excisive functors]]

(all in [[topological spaces]]) as [[categories of modules]] with respect to [[Day convolution]] monoidal structures on [[Top]]-[[enriched functor categories]] over restrictions to [[faithful functor|faithful]] sub-[[sites]] of the canonical representative of the [[sphere spectrum]] as an excisive functor on $Top^{\ast/}_{fin}$.

This approach is due to ([Mandell-May-Schwede-Shipley 00](#MMSS00)).

##### Diagram spectra

+-- {: .num_defn #TopologicalDiagramCategoriesForSpectra}
###### Definition

Define the following [[pointed topologically enriched categories|pointed topologically enriched]] [[symmetric monoidal category|symmetric]] [[closed monoidal categories]] (the [[tensor product]] is a [[pointed topologically enriched functor]]):

1. $Seq$ has as objects the [[natural numbers]] and has only identity morphisms, tensor product is the addition of natural numbers, tensor unit is 0. As a $Top^{\ast/}$-[[enriched category]] the hom-spaces are

   $$
     Seq(n_1,n_2) = 
     \left\{
       \array{
          S^0 & for\; n_1 = n_2
          \\
          \ast & otherwise
       }
    \right.
   $$

1. $Sym$ is the standard [[skeletal category|skeleton]] of the [[core]] of [[FinSet]], objects are the sets $\{1, \cdots,n\}$ for $n \in \mathbb{N}$, all morphisms are [[automorphisms]] and the [[automorphism group]] of $\{1,\cdots,n\}$ is the [[symmetric group]] $\Sigma_n$, tensor product is the [[disjoint union]] of sets, tensor unit is the [[empty set]]; we turn this into a $Top^{\ast/}$-[[enriched category]] by adjoining a basepoint:

   $$
     Sym(n_1, n_2) =
     \left\{
       \array{
          (\Sigma_{n_1})_+ & for \; n_1 = n_2
          \\
          \ast & otherwise
       }
     \right.
   $$

1. $Orth$ has as objects finite dimenional real linear [[inner product spaces]] $(V, \langle -,-\rangle)$ and as morphisms the [[linear map|linear]] [[isometry|isometric]] [[isomorphisms]] between these; hence the [[automorphism group]] of the object $(V, \langle -,-\rangle)$ is the [[orthogonal group]] $O(V)$; the monoidal product is [[direct sum]] of linear spaces, the tensor unit is the 0-vector space; again we turn this into a $Top^{\ast/}$-enriched category by adjoining a basepoint to the hom-spaces;
  
  $$
    Orth(V_1,V_2) 
    \simeq
    \left\{
       \array{
         O(V_1)_+ & for \; dim(V_1) = dim(V_2)
         \\
         \ast & otherwise
       }
    \right.
  $$


1. $Top_{fin}^{\ast/}$ is the [[full subcategory]] of [[pointed topological space]] on those [[homeomorphism|homeomorphic]] to [[finite CW-complexes]], tensor product is their [[smash product]], tensor unit is the [[0-sphere]] $S^0$.

Denote the canonical [[faithful functor|faithful]] [[subcategory]] inclusions by

$$
 \array{
   Seq 
     &\stackrel{seq}{\hookrightarrow}& 
   Sym 
    &\stackrel{sym}{\hookrightarrow}& 
   Orth 
     &\stackrel{orth}{\hookrightarrow}& 
   Top_{fin}^{\ast/}
   \\
   n 
    &\mapsto& 
   \{1,\cdots, n\} 
     &\mapsto& 
   \mathbb{R}^n 
    &\mapsto& 
   S^n
   \\
    && 
    && 
   V
    &\mapsto& 
   S^V
  }
  \,,
$$

where $S^V$ denotes the [[one-point compactification]] of $V$. On morphisms $sym \colon (\Sigma_n)_+ \hookrightarrow (O(n))_+$ is the inclusion of [[permutation]] matrices into [[orthogonal group|orthogonal]] matrices and $orth \colon O(V)_+ \hookrightarrow Aut(S^V)$ is on $O(V)$ the topological subspace inclusions of the pointed [[homeomorphisms]] $S^V \to S^V$ that are induced under forming [[one-point compactification]] from linear isometries of $V$.

=--

+-- {: .num_prop #PropertiesOfTopologicalDiagramCategoriesForSpectra}
###### Proposition

The sequence of inclusions in def. \ref{TopologicalDiagramCategoriesForSpectra} satisfies the following properties:

1. All three inclusions are [[strong monoidal functors]].

1. Under passing to [[enriched functor categories]], restriction $(-)^\ast$ along these inclusions and [[left Kan extension]] $(-)_!$ along them yields a sequence of [[adjunctions]]

   $$
    \array{
      [Top_{fin}^{\ast/}, Top^{\ast/}]
        \stackrel{\overset{orth_!}{\longleftarrow}}{\underset{orth^\ast}{\longrightarrow}}
      [Orth, Top^{\ast/}]
        \stackrel{\overset{sym_!}{\longleftarrow}}{\underset{sym^\ast}{\longrightarrow}}
      [Sym, Top^{\ast/}] 
        \stackrel{\overset{seq_!}{\longleftarrow}}{\underset{seq^\ast}{\longrightarrow}}
      [Seq, Top^{\ast/}] 
    }
     \,.
   $$

1. All four [[enriched functor categories]] become [[symmetric monoidal categories]] with the [[Day convolution]] monoidal product structure induced by the monoidal structure of their [[sites]]. 

1. With respect to this all [[adjunctions]] above are symmetric [[monoidal adjunctions]] (the [[right adjoint]] is a [[symmetric monoidal functor|symmetric]] [[lax monoidal functor]], the [[left adjoint]] is even a [[symmetric monoidal functor|symmetric]] [[strong monoidal functor]]).

=--

(e.g. [MMSS 00, I.3](#MMSS00))



Notice the following:

+-- {: .num_lemma #DayConvolutionTensorUnitIsYonedaImageOfTensorUnitInSite}
###### Lemma

For $\mathcal{C}$ a $V$-[[enriched category|enriched]] [[monoidal category]], under the [[Yoneda embedding]]

$$
  y \colon \mathcal{C}^{op} \hookrightarrow [\mathcal{C}, Top^{\ast/}]
$$

the [[tensor unit]] in $\mathcal{C}$ goes to the tensor unit of the induced [[Day convolution]] structure on $[\mathcal{C}, Top^{\ast/}]$.

=--

(see at _[[Day convolution]]_ [this lemma](Day+convolution#DayConvolutionTensorUnitIsYonedaImageOfTensorUnitInSite))


+-- {: .num_defn #StandardRepresentativeOfTheSphereSpectrum}
###### Definition

Write

$$
  \mathbb{S} \coloneqq y(S^0) \in [Top_{fin}^{\ast/}, Top^{\ast/}]
$$

for the image under the [[Yoneda embedding]] of the [[tensor unit]] in $Top_{fin}^{\ast/}$ with its [[smash product]] (the [[0-sphere]]), which by lemma \ref{DayConvolutionTensorUnitIsYonedaImageOfTensorUnitInSite} is the tensor unit in $([Top_{fin}^{\ast/}, Top^{\ast/}], \otimes_{Day})$.

Since this is going to be the standard presentation of the [[sphere spectrum]] in the [[model structure for excisive functors]] on $[Top_{fin}^{\ast/}, Top^{\ast/}]$ we refer to it as _[[generalized the|the]] [[sphere spectrum]]_.

For its restrictions along the above sub-site inclusions, prop. \ref{PropertiesOfTopologicalDiagramCategoriesForSpectra}, write

$$
  \mathbb{S}_{Orth} \coloneqq orth^\ast \mathbb{S} 
  \,,
  \;
  \mathbb{S}_{Sym} \coloneqq sym^\ast \mathbb{S}_{orth} 
  \,,
  \;
  \mathbb{S}_{Seq} \coloneqq seq^\ast \mathbb{S}_{sym} 
  \,.
$$


=--

+-- {: .num_remark #RestrictionsOfSphereSpectrumAreStillMonoidObjects}
###### Remark

While $\mathbb{S}$ in def. \ref{StandardRepresentativeOfTheSphereSpectrum} is the [[tensor unit]] in $([Top_{fin}^{\ast/}, Top^{\ast/}], \otimes_{Day})$, neither of its restrictions $\mathbb{S}_{Orth},\mathbb{S}_{Sym}, \mathbb{S}_{Seq}$ is the tensor unit in $([Orth, Top^{\ast/}],\otimes_{Day}), ([Sym, Top^{\ast/}],\otimes_{Day}), ([Seq, Top^{\ast/}],\otimes_{Day})$, respectively. 

Nevertheless, because by prop. \ref{PropertiesOfTopologicalDiagramCategoriesForSpectra} the restriction functors are [[strong monoidal functors]] and because the tensor unit $\mathbb{S}$ canonically has the structure of a [[monoid object]], each of $\mathbb{S}_{Orth},\mathbb{S}_{Sym}, \mathbb{S}_{Seq}$ inherts the structure of a [[monoid object]] in the respective [[Day convolution]] [[monoidal category]].

Moreover, $\mathbb{S}_{Orth}$ and $\mathbb{S}_{Sym}$ are [[commutative monoid objects]], while $\mathbb{S}_{Seq}$ is not commutative (due to the [graded commutativity in the smash product of spheres](smash+product+of+spectra#GradedCommutativity) which is not reflected in the trivial symmetry of the tensor product on $Seq$).

| | $\mathbb{S}$ | $\mathbb{S}_{Orth}$ | $\mathbb{S}_{Sym}$ | $\mathbb{S}_{Seq}$ |
|--|--------------|---------------------|--------------------|-------------------|
| [[monoid object]] | yes | yes | yes | yes |
| [[commutative monoid object]] | yes | yes | yes | no |
| [[tensor unit]] | yes | no | no | no |

Explicitly, by the discussion at _[Day convolutions -- Properties -- Monoids](Day+convolution#Monoids)_, monoids with resepct to Day convolution are equivalently [[lax monoidal functors]] on the site, and as such $\mathbb{S}_{Orth}$ is the one given by the canonical [[natural transformations]]

$$
  S^{V_1} \wedge S^{V_2} \longrightarrow S^{V_1 \oplus V_2}
$$

and $\mathbb{S}_{Sym}$ and $\mathbb{S}_{Seq}$ the ones given by the canonical natural transformations

$$
  S^{n_1} \wedge S^{n_2} \longrightarrow S^{n_1 + n_2}
  \,.
$$


=--


Therefore we may consider [[module objects]] over the restrictions of [[generalized the|the]] [[sphere spectrum]] from def. \ref{StandardRepresentativeOfTheSphereSpectrum}.

+-- {: .num_prop #HighlyStructuredSpectraAsDayConvolutionSModules}
###### Proposition

The category of right [[module objects]] over $\mathbb{S}_{Orth}$, $\mathbb{S}_{Sym}$ and $\mathbb{S}_{Seq}$ from def. \ref{StandardRepresentativeOfTheSphereSpectrum}, which are [[monoid objects]] by prop. \ref{PropertiesOfTopologicalDiagramCategoriesForSpectra}, remark \ref{RestrictionsOfSphereSpectrumAreStillMonoidObjects}, are [[equivalence of categories|equivalent]], respectively, to the categories of [[orthogonal spectra]], [[symmetric spectra]] and [[sequential spectra]] (in [[compactly generated topological spaces]]):

$$
  \mathbb{S}_{Orth} Mod_r \simeq OrthSpec(Top)
$$

$$
  \mathbb{S}_{Sym} Mod_r \simeq SymSpec(Top)
$$

$$
  \mathbb{S}_{Seq} Mod_r \simeq SeqSpec(Top)
  \,.
$$

=--

+-- {: .proof}
###### Proof

Write $\mathbb{S}_{dia}$ for any of the three monoids. By the discussion at _[Day convolutions -- Properties -- Monoids](Day+convolution#Monoids)_, right modules with respect to [[Day convolution]] are equivalently right [[modules over monoidal functors]] over the monoidal functor corresponding to $\mathbb{S}_{dia}$ as in remark \ref{RestrictionsOfSphereSpectrumAreStillMonoidObjects}. This means that for $\mathbb{S}_{Sym}$ and $\mathbb{S}_{Seq}$ they are functors $X \colon Sym \longrightarrow sSet^{\ast/}$ or $X \colon Seq \longrightarrow sSet^{\ast/}$, respectively equipped with [[natural transformations]]

$$
  X_p \wedge S^{q}  \longrightarrow X_{p+q}
$$

satisfying the evident [[categorification|categorified]] [[action]] property. In the present case this action property says that these morphisms are determined by 

$$
  X_p \wedge S^1 \longrightarrow X_{p+1}
$$

under the isomorphisms $S^p \simeq S^1 \wedge S^{p-1}$. Naturality of all these morphisms as functors on $Sym$ is the equivariance under the symmetric group actions in the definition of [[symmetric spectra]]. 

Similarly, modules over $\mathbb{S}_{Orth}$ are equivalently functors

$$
  X_V \wedge S^{W}  \longrightarrow X_{V \oplus W}
$$

etc. and their functoriality embodies the [[orthogonal group]]-equivariance in the definition of [[orthogonal spectra]].


=--

+-- {: .num_remark #PreExcisiveFunctorsAreSModules}
###### Remark

For completeness, we may, trivially, add to the three statements in prop. \ref{HighlyStructuredSpectraAsDayConvolutionSModules} the equivalence

$$
  \mathbb{S} Mod_r \simeq [Top^{\ast/}_{fin}, Top^{\ast/}]
  \,,
$$

which holds tautologically because by def. \ref{StandardRepresentativeOfTheSphereSpectrum} $\mathbb{S}$ is in fact the [[tensor unit]] in $([Top^{\ast/}_{fin}, Top^{\ast/}],\otimes_{Day})$, so that every object here is canonically a module object over $\mathbb{S}$.

Now the [[model structure on excisive functors]] shows that the category $[Top^{\ast/}_{fin}, Top^{\ast/}]$ constitutes a model for [[stable homotopy theory]], while this is not the case for either of its restrictions. 

Hence we may read prop. \ref{HighlyStructuredSpectraAsDayConvolutionSModules} as saying that while restricting the domain of [[excisive functors]] breaks their property of being a model for [[stable homotopy theory]], but at the same time retaining the correspondingly restricted [[sphere spectrum]]-[[module]] structure first of all becomes non-tautological after restriction and second restores the property of the objects to model spectra.

=--

+-- {: .num_defn #SymmetricSmashProductOfDiagramSpectra}
###### Definition

By remark \ref{RestrictionsOfSphereSpectrumAreStillMonoidObjects} the categories $\mathbb{S}_{Sym} Mod_r$, $\mathbb{S}_{Orth} Mod_r$ and $\mathbb{S}_{Orth} Mod_r$ are [[categories of modules]] over a [[commutative monoid object]] and as such they inherit [[symmetric monoidal category]] structure themselves.  Via prop. \ref{HighlyStructuredSpectraAsDayConvolutionSModules} this is equivalently symmetric monoidal product structure 

$$
  (SymSpec(Top), \wedge)
$$

on the category of [[symmetric spectra]] and 

$$
  (OrthSpec(Top), \wedge)
$$

on that of [[orthogonal spectra]]. This is called the _[[symmetric monoidal smash product of spectra]]_.

=--


+-- {: .num_remark #SystemOfStructuredSpectraAndDiagrams}
###### Remark

Combined with the [[free-forgetful adjunctions]] for [[module objects]] ([[free modules]] $\dashv$ underlying objects) the situation described by prop. \ref{PropertiesOfTopologicalDiagramCategoriesForSpectra} and prop. \ref{HighlyStructuredSpectraAsDayConvolutionSModules} jointly is the following diagram of [[adjunctions]]

$$
 \array{
   && OrthSpec(Top) && SymSpec(Top) && SeqSpec(Top)
   \\
   && \downarrow^{\mathrlap{\simeq}}
   && \downarrow^{\mathrlap{\simeq}}
   && \downarrow^{\mathrlap{\simeq}}
   \\
   \mathbb{S} Mod_r && \mathbb{S}_{Orth} Mod_r && \mathbb{S}_{Sym} Mod_r && \mathbb{S}_{Seq} Mod_r
   \\
   {}^{\mathllap{U}}\downarrow \uparrow^{\mathrlap{F}}
   &&
   {}^{\mathllap{U}}\downarrow \uparrow^{\mathrlap{F}}
   &&
   {}^{\mathllap{U}}\downarrow \uparrow^{\mathrlap{F}}
   &&
   {}^{\mathllap{U}}\downarrow \uparrow^{\mathrlap{F}}
   \\
   [Top_{fin}^{\ast/}, Top^{\ast/}]
     &\stackrel{\overset{orth_!}{\longleftarrow}}{\underset{orth^\ast}{\longrightarrow}}&
   [Orth, Top^{\ast/}]
     &\stackrel{\overset{sym_!}{\longleftarrow}}{\underset{sym^\ast}{\longrightarrow}}&
   [Sym, Top^{\ast/}] 
      &\stackrel{\overset{seq_!}{\longleftarrow}}{\underset{seq^\ast}{\longrightarrow}}&
   [Seq, Top^{\ast/}] 
 }
  \,.
$$

=--

In order to conveniently speak about all columns of the system of adjunctions in remark \ref{SystemOfStructuredSpectraAndDiagrams} in a unified way, we introduce the following notation.

+-- {: .num_defn #NotationForGenericDiagramSpectra}
###### Definition

We write $dia \in \{Top^{\ast/, Orth, Sym, Seq}\}$ generically for any one of the four sites in def. \ref{TopologicalDiagramCategoriesForSpectra}.

Accordingly we write $\mathbb{S}_{dia} \in \{\mathbb{S}, \mathbb{S}_{Orth}, \mathbb{S}_{Sym}, \mathbb{S}_{Seq}\}$ generically for any one of the four incarnations of [[generalized the|the]] [[sphere spectrum]] according to def. \ref{StandardRepresentativeOfTheSphereSpectrum}, over these sites.

Finally we will write


$$
  \mathbb{S}_{dia}Mod 
   \stackrel{\overset{seq!}{\longleftarrow}}{\underset{seq^\ast}{\longrightarrow}}
  \mathbb{S}_{Seq}Mod
  \simeq
  SeqSpec(Top)
$$

for the [[composition]] of the sequence of [[adjunctions]] to the right of the corresponding category of modules in the diagram below in prop. \ref{SystemOfAdjunctionsForDiagramSpectra}, regarded via prop. \ref{HighlyStructuredSpectraAsDayConvolutionSModules} and landing in the category of [[sequential spectra]].

=--



We would like to lift the horizontal adjunctions in the diagram in remark \ref{SystemOfStructuredSpectraAndDiagrams} from the bottom row to the top row. To that end, oberve that the [[categories of modules]] involved here are themselves still [[enriched functor categories]]:

+-- {: .num_lemma #SModulesAsEnrichedFunctors}
###### Lemma

Let ${dia} \in \{Top^{\ast/}, {Orth}, {Sym}, {Seq}\}$ be any one of the sites in def. \ref{TopologicalDiagramCategoriesForSpectra}. 

1. There is an [[equivalence of categories]]

   $$
     \mathbb{S}_{dia} Mod \simeq [ \mathbb{S}_{dia} FreeMod^{op}, Top^{\ast/} ]
   $$

   between the corresponding [[category of modules]] (prop.   \ref{HighlyStructuredSpectraAsDayConvolutionSModules}) and the $Top^{\ast/}$-[[enriched functor category]] over the [[opposite category|opposite]] of its [[full subcategory]] on the [[free modules]].

1. If $\mathbb{S}_{dia}$ is a [[commutative monoid]] (hence for $dia \in \{Top^\ast/, Orth,Sym\}$ but not for $dia = Seq$) then $\mathbb{S}_{dia} FreeMod^{op}$ carries a [[symmetric monoidal category]] structure such that under the above equivalence its [[Day convolution]] is the [[tensor product of modules]].

1. There is a $Top^{\ast/}$-[[enriched functor]]

   $$
     \delta \colon dia \longrightarrow \mathbb{S}_{dia} FreeMod^{op}
   $$

   which is monoidal when $\mathbb{S}_{dia}$ is commutative and which is such that the ([[free module]]$\dashv$[[forgetful functor]])-adjunction is equivalently the [[base change]] along $\delta$:

   $$
     \array{
       \mathbb{S}_{dia} Mod 
         &\simeq&
       [ \mathbb{S}_{dia} FreeMod^{op}, Top^{\ast/}] 
       \\
       {}^{\mathllap{U}}\downarrow \uparrow^{\mathrlap{F}}
       &&
       {}^{\mathllap{\delta^\ast}}\downarrow \uparrow^{\mathrlap{\delta_!}}
       \\
       [dia, Top^{\ast/}] 
         &=&
       [dia, Top^{\ast/}] 
     }
     \,.
   $$

=--


This is a general statement about modules with respect to [[Day convolution]] monoidal structures, see [this proposition](Day+convolution#ModulesInDayConvolutionAreFunctorsOnFreeModulesOp)  ([MMSS 00, theorem 2.2](#MMSS00)). 

+-- {: .num_example #SequentialSpectraAsFunctorsOnFreeSSequModules}
###### Example

For the sequential case $dia = Seq$, then the opposite category $\mathbb{S}_{Seq} FreeMod^{op}$ of [[free modules]] over $\mathbb{S}_{Seq}$ (def. \ref{StandardRepresentativeOfTheSphereSpectrum}) in lemma \ref{SModulesAsEnrichedFunctors} is identified as the non-full subcategory $StdSpheres$ of $Top^{\ast/}$ whose objects are the standard spheres $S^n \coloneqq (S^1)^{\wedge^n}$ and whose hom spaces are the canonical image of $S^{n_2-n_1}$ in the hom space $Top^{\ast/}(S^{n_1},S^{n_2})$ (the image under the smash$\dashv$hom-[[adjunct]] of the identity) if $n_2 \gt n_1$, and the point otherwise:

$$
  \begin{aligned}
    \mathbb{S}_{Seq}FreeMod^{op}(F(n_1), F(n_2))
    & =
    StdSpheres(S^{n_1}, S^{n_2})
    \\
    & \coloneqq
    \left\{
      \array{
        im(S^{n_2-n_2} \to Top^{\ast/}(S^{n_1}, S^{n_2})) & for \; n_1 \leq n_2
        \\
        \ast & otherwise
      }
    \right.
  \end{aligned}
  \,.
$$

Hence according to lemma \ref{SModulesAsEnrichedFunctors} [[sequential spectra]] are equivalently $Top^{\ast/}$-enriched functors on StdSpheres:

$$
  SeqSpec
  \simeq
  [StdSpheres, Top^{\ast/}]
  \,.
$$

=--

In this form the statement appears also as ([Lydakis 98, prop. 4.3](#Lydakis98)). See also at _[sequential spectra -- As diagram spectra](sequential+spectrum#AsDiagramSpectra)_.


+-- {: .proof}
###### Proof

The free $\mathbb{S}_{Dia}$ modules are those of the form $y(d)\wedge \mathbb{S}_{Dia}$, where $d \in Dia$ is an object, and $y$ denotes the [[Yoneda embedding]]. For the case $Dia = Seq$ this means that they are labeled by $k \in \mathbb{N}$, their underlying functor $F(k) \in [Seq,Top^{\ast/}]$ is given by

$$
  F(k)
  \;\colon\;
  n 
  \mapsto
  \left\{
    \array{
      S^{n-k} & for\; n \geq k
      \\
      \ast & otherwise
    }
  \right.
$$

and the $\mathbb{S}_{Seq}$-[[action]] on these is, expressed as [[modules over monoidal functors]] (via [this fact](Day+convolution#DayMonoidsAreLaxMonoidalFunctorsOnTheSite) about modules with respect to [[Day convolution]]) by the canonical identifications

$$
  S^{n_1} \wedge F(k)_{n_2}
  =
  S^{n_1} \wedge S^{n_2-k}
  \overset{}{\longrightarrow}
  S^{n_1 + n_2 - k}
  =
  F(k)_{n_1+ n_2}
$$

whenever $n_2 \geq k$, and by the [[zero morphism]] otherwise.

Now for $R$ any other $\mathbb{S}_{Seq}$-module, with action

$$
  S^{n_1} \wedge R_{n_2} \overset{\rho_{n_1,n_2}}{\longrightarrow} R_{n_1 + n_2}
$$

then a homomorphism of $\mathbb{S}_{Seq}$-modules $\phi \colon F(k)\to R$ has components $\phi_{n}\colon S^{n-k} \to R_n$ fitting into commuting diagrams of the form

$$
  \array{
     S^{n_1} \wedge S^{n_2 - k} &\overset{\simeq}{\longrightarrow}& S^{n_1 + n_2 - k}
     \\
     {}^{\mathllap{(id,\phi_{n_2})}}\downarrow 
       && 
     \downarrow^{\mathrlap{\phi_{n_1+n_2}}}
     \\
     S^{n_1} \wedge R_{n_2} &\overset{\rho_{n_1,n_2}}{\longrightarrow}& R_{n_1+n_2}
  }
$$

for $n_2 \geq k$. By the fact that the top morphism here is an isomorphism, all the components $\phi_{n \geq k}$ are uniquely fixed by the component $\phi_k$ as 

$$
  \phi_{n geq k} = \rho_{n-k,k} \circ \phi_k 
$$

(and $\phi_{n \lt k} = 0$). Of course this just confirms the [[free property]] of free spectra: morphisms of $\mathbb{S}_{Seq}$-modules $F(k) \longrightarrow R$ are equivalent to morphisms in $[Seq,Top^{\ast/}]$ from $y(k)$ to $R$, which by the [[Yoneda lemma]] form the space $R_k \in Top^{\ast/}$.

Specialized to $R$ a free spectrum itself this verifies that the hom-spaces between free $\mathbb{S}_{Seq}$-modules are as claimed:

$$
  \mathbb{S}_{Seq}FreeMod(F(k_2),F(k_1))
  \simeq
  F(k_1)_{k_2} 
  \simeq
  \left\{
    \array{
      S^{k_2-k_1} & for \; k_2 \geq k_1
      \\
      \ast & otherwise
    }
  \right.
  \,.
$$

Of course this is just the defining free property. But now comparison with the above commuting square for the case $n_1 = k_1$ and $n_2 = k_2$ shows that composition in $\mathbb{S}_{Seq} FreeMod^{op}$ is indeed the composition in $Top^{\ast/}$ under the identification of $F(k)$ with $S^k$ and of the above hom-space $S^{k_2-k_1}$ with its image under $S^{k_2-k_1} \to Top^{\ast/}(S^{k_1},S^{k_2})$.

=--


From lemma \ref{SModulesAsEnrichedFunctors} we immediately get the following:


+-- {: .num_prop #SystemOfAdjunctionsForDiagramSpectra}
###### Proposition

The horizontal adjunctions in remark \ref{SystemOfStructuredSpectraAndDiagrams} lift to adjunctions between categories of modules, such as to give a [[commuting diagram]] of adjunctions as follows:

$$
 \array{
   && OrthSpec(Top) && SymSpec(Top) && SeqSpec(Top)
   \\
   && \downarrow^{\mathrlap{\simeq}}
   && \downarrow^{\mathrlap{\simeq}}
   && \downarrow^{\mathrlap{\simeq}}
   \\
   \mathbb{S} Mod_r 
     &\stackrel{\overset{orth_!}{\longleftarrow}}{\underset{orth^\ast}{\longrightarrow}}&
   \mathbb{S}_{Orth} Mod_r 
     &\stackrel{\overset{sym_!}{\longleftarrow}}{\underset{sym^\ast}{\longrightarrow}}&
   \mathbb{S}_{Sym} Mod_r 
      &\stackrel{\overset{seq_!}{\longleftarrow}}{\underset{seq^\ast}{\longrightarrow}}&
   \mathbb{S}_{Seq} Mod_r
   \\
   {}^{\mathllap{U}}\downarrow \uparrow^{\mathrlap{F}}
   &&
   {}^{\mathllap{U}}\downarrow \uparrow^{\mathrlap{F}}
   &&
   {}^{\mathllap{U}}\downarrow \uparrow^{\mathrlap{F}}
   &&
   {}^{\mathllap{U}}\downarrow \uparrow^{\mathrlap{F}}
   \\
   [Top_{fin}^{\ast/}, Top^{\ast/}]
     &\stackrel{\overset{orth_!}{\longleftarrow}}{\underset{orth^\ast}{\longrightarrow}}&
   [Orth, Top^{\ast/}]
     &\stackrel{\overset{sym_!}{\longleftarrow}}{\underset{sym^\ast}{\longrightarrow}}&
   [Sym, Top^{\ast/}] 
      &\stackrel{\overset{seq_!}{\longleftarrow}}{\underset{seq^\ast}{\longrightarrow}}&
   [Seq, Top^{\ast/}] 
 }
  \,.
$$

=--

([MMSS 00, prop. 3.4 with construction 2.1](#MMSS00))


We consider now, prop. \ref{StrictModelStructureOnDiagramSpectra} below, "strict" [[model category]] structures on the above categories of spectra, which regard spectra only as diagrams of topological spaces, ignoring the fact that it is not the degreewise [[homotopy groups]] but the [[stable homotopy groups]] that are to be invariants of [[stable homotopy types]] (this is def. \ref{StableEquivalencesForDiagramSpectra} below with an extra subtlety in the case of symmetric spectra, see prop. \ref{RelationBetweenStableEquivalencesAndStableWeakHomotopyEquivalencesForDiagramSpectra} below). Incorporating the latter is accomplished by a [[Bousfield localization of model categories|left Bousfield localizatiob]] of the strict model structures to the genuine stable model structures [below](#ProofOfTheStableModelStructure).

+-- {: .num_prop #StrictModelStructureOnDiagramSpectra}
###### Proposition

Write $[Seq, Top^{\ast/}_{Quillen}]$ for the [[model category]] structure on $\mathbb{N}$-parameterized sequences of pointed topological spaces, whose weak equivalences, fibrations and cofibrations are degreewise those of the [[classical model structure on pointed topological spaces]]. (This is equivalently the injective as well as the  projective [[model structure on functors]] over the discrete category $\mathbb{N}$).

Then for each of the categories in the diagram of prop. \ref{SystemOfAdjunctionsForDiagramSpectra}, say that the **strict model structure** on it is the [[transferred model structure]] from $[Seq, Top^{\ast/}_{Quillen}]$ along the composite adjunction connecting the two in that diagram, so that we get a diagram of [[Quillen adjunctions]]

$$
 \array{
   && OrthSpec(Top)_{strict} && SymSpec(Top)_{strict} && SeqSpec(Top)_{strict}
   \\
   && \downarrow^{\mathrlap{\simeq}}
   && \downarrow^{\mathrlap{\simeq}}
   && \downarrow^{\mathrlap{\simeq}}
   \\
   \mathbb{S} Mod_{strict}
     &\stackrel{\overset{orth_!}{\longleftarrow}}{\underset{orth^\ast}{\longrightarrow}}&
   \mathbb{S}_{Orth} Mod_{strict}
     &\stackrel{\overset{sym_!}{\longleftarrow}}{\underset{sym^\ast}{\longrightarrow}}&
   \mathbb{S}_{Sym} Mod_{strict}
      &\stackrel{\overset{seq_!}{\longleftarrow}}{\underset{seq^\ast}{\longrightarrow}}&
   \mathbb{S}_{Seq} Mod_{strict}
   \\
   {}^{\mathllap{U}}\downarrow \uparrow^{\mathrlap{F}}
   &&
   {}^{\mathllap{U}}\downarrow \uparrow^{\mathrlap{F}}
   &&
   {}^{\mathllap{U}}\downarrow \uparrow^{\mathrlap{F}}
   &&
   {}^{\mathllap{U}}\downarrow \uparrow^{\mathrlap{F}}
   \\
   [Top_{fin}^{\ast/}, Top^{\ast/}]_{strict}
     &\stackrel{\overset{orth_!}{\longleftarrow}}{\underset{orth^\ast}{\longrightarrow}}&
   [Orth, Top^{\ast/}]_{strict}
     &\stackrel{\overset{sym_!}{\longleftarrow}}{\underset{sym^\ast}{\longrightarrow}}&
   [Sym, Top^{\ast/}]_{strict} 
      &\stackrel{\overset{seq_!}{\longleftarrow}}{\underset{seq^\ast}{\longrightarrow}}&
   [Seq, Top^{\ast/}_{Quillen}] 
 }
  \,.
$$

=--

(see [MMSS 00, Variant 6.10](#MMSS00))

+-- {: .proof}
###### Proof

To see that indeed all the adjunctions here are [[Quillen adjunctions]], use that by prop. \ref{PropertiesOfTopologicalDiagramCategoriesForSpectra} and lemma \ref{SModulesAsEnrichedFunctors} all [[right adjoints]] are given by restrictions of [[sites]]. By definition of the strict model structures and transferred moddel structures their fibrations and acyclic fibrations are objectwise so, and hence are preserved by these restriction functors.

=--



The strict model structures of prop. \ref{StrictModelStructureOnDiagramSpectra} [[presentable (infinity,1)-category|present]] the [[homotopy theory]] of the given diagrams of homotopy types, hence a homotopy theory of pre-spectra. To obtain from this the genuine [[stable homotopy theory]] of genuine spectra we need to restrict this to [[Omega-spectra]], in the following sense.

+-- {: .num_defn #StableEquivalencesForDiagramSpectra}
###### Definition

For any of the four categories of spectra in prop. \ref{SystemOfAdjunctionsForDiagramSpectra}, we say (with notation from def. \ref{NotationForGenericDiagramSpectra}) that:

1. an object $X$ is an _Omega-spectrum_ if $seq^\ast X $ is an [[Omega spectrum]] in the standard sense of [[sequential spectra]];

1. a morphism $f$ is a _stable weak homotopy equivalence_ if $seq^\ast(f)$ is a [[stable weak homotopy equivalence]] in the standard sense of [[sequential spectra]] (an [[isomorphism]] on all [[stable homotopy groups]] of sequential spectra);

1. a morphism $f$ is a _stable equivalence_ if for all Omega-spectra $X$ in the above sense, the morphism $[f,E]_{strict}$ is a [[bijection]] (where $[-,E]_{strict}$ is the [[hom-functor]] of the [[homotopy category]] of the strict model structure of prop. \ref{StrictModelStructureOnDiagramSpectra}.


=--

([MMSS00, def. 8.3 with the notation from p. 21](#MMSS00))


The following proposition says that def. \ref{StableEquivalencesForDiagramSpectra} makes sense, in that if the [[Bousfield localization of model categories|left Bousfield localization]] of the strict model structures at the stable equivalences exists (which we check [below](ProofOfTheStableModelStructure)) then it indeed localizes the homotopy theory to the [[Omega-spectra]].

+-- {: .num_prop #StableEquivalencesBetweenOmegaSpectraAreStrictWeakEquivalences}
###### Proposition

The weak equivalences in the strict model structure (prop. \ref{StrictModelStructureOnDiagramSpectra}) and the stable equivalences of def. \ref{StableEquivalencesForDiagramSpectra} are related as follows:

1. Every weak equivalence with respect to the strict model structure is a stable equivalence.

1. Every stable equivalence between Omega-spectra (def. \ref{StableEquivalencesForDiagramSpectra}) is a weak equivalence in the strict model structure.

=--

([MMSS 00, lemma 8.11](#MMSS00))

+-- {: .proof}
###### Proof

The first statement follows by def. \ref{StableEquivalencesForDiagramSpectra} since weak equivalences become isomorphisms in the [[homotopy category]].

For the second statement, let $f \colon X \to Y$ be a stable equivalence between Omega-spectra. Then by definition, in particular

$$
  [f,X]_{strict} \;\colon\; [Y,X]_{strict} \longrightarrow [X,X]_{strict}
$$

is a [[bijection]]. Therefore the pre-image of $[id_X] \in [X,X]_{strict}$ is an inverse to $f$ in the [[homotopy category]] of the strict model structure. Hence $f$ represents an isomorphism in the strict homotopy category and is hence a weak equivalence in the strict model structure.

=--



##### Free spectra
 {#FreeSpectra}

> This is a technical section with discussion of certain [[free construction|free]] objects  in the categories of spectra of prop. \ref{HighlyStructuredSpectraAsDayConvolutionSModules}. The discussion here provides technical lemmas that are used in the proof of the stable model structures [below](#ProofOfTheStableModelStructure), the proof of the Quillen equivalences between them [further below](#QuillenEquivalencesOfStableModelStructures) and [then](#MonoidalStableModelStructure) the proof that the model structure is monoidal.

The concept of _[[free spectrum]]_ is a generalization of that of _[[suspension spectrum]]_. In fact the [[stable homotopy types]] of free spectra are precisely those of iterated [[loop space objects]] of [[suspension spectra]]. But for the development of the theory what matters is free spectra before passing to stable homotopy types, for as such they play the role of the basic cells for the stable [[model structures on spectra]] analogous to the role of the [[n-spheres]] in the [[classical model structure on topological spaces]] (def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra} below).

Moreover, while free [[sequential spectra]] are just re-indexed [[suspension spectra]], free [[symmetric spectra]] and free [[orthogonal spectra]] in addition come with suitably freely generated [[actions]] of the [[symmetric group]] and the [[orthogonal group]]. It turns out that this is not entirely trivial; it leads to a subtle issue (lemma \ref{AdjunctsOfFreeSpectrumInclusionsAreOrAreNotStableWeakHomotopyEquivalences} below) where the [[adjuncts]] of certain canonical inclusions of free spectra are [[stable weak homotopy equivalences]] for sequential and orthogonal spectra, but _not_ for symmetric spectra.  The fine analysis of this phenomenon is crucial in the proof of the [[Quillen equivalences]] between the stable model structures on the four models of spectra (theorem \ref{QuillenEquivalencesBetweenStableModelStructuresOnDiagramSpectra}). 


+-- {: .num_defn #FreeStructuredSpectrum}
###### Definition

For $dia \in \{Top^{\ast/}_{fin}, Orth, Sym, Seq\}$ and for each $n \in \mathbb{N}$, the functor 

$$
  (-)_n
  \;\colon\;
  \mathbb{S}_{dia}Mod \stackrel{seq^\ast}{\longrightarrow} \mathbb{S}_{Seq}Mod \simeq SeqSpec(Top) \stackrel{(-)_n}{\longrightarrow} Top^{\ast/}
$$

that sends a [[structured spectrum]] (notation as in def. \ref{NotationForGenericDiagramSpectra}) to the $n$th component space of its underlying [[sequential spectrum]] has a [[left adjoint]]

$$
  F^{dia}_n \;\colon\; Top^{\ast/} \longrightarrow \mathbb{S}_{dia}Mod
  \,.
$$

This is called the _[[free structured spectrum]]_-functor.

The [[adjunction units]] in the sequence of adjunctions equip these with canonical [[natural transformations]]

$$
  F_n^{Seq}
    \stackrel{f_n^{Seq}}{\longrightarrow}
  F_n^{Sym}
    \stackrel{f_n^{Sym}}{\longrightarrow}
  F_n^{Orth}
    \stackrel{f_n^{Orth}}{\longrightarrow}
  F_n^{Top^{\ast/}_{fin}}
  \,.
$$

=--

([MMSS 00, section 8](#MMSS00))

+-- {: .num_lemma #ExplicitExpressionForFreeSpectra}
###### Lemma

Under the equivalence of lemma \ref{SModulesAsEnrichedFunctors}

1. the [[free spectrum]] on $K \in Top^{\ast/}$ is 

   $$
     F^{dia}_n K
      \;=\;
     \mathbb{S}_{dia}FreeMod( - , y(n)\wedge \mathbb{S}_{dia} ) \wedge K
      \;\in\; 
     [ \mathbb{S}_{dia} FreeMod^{op}, Top^{\ast/}]
      \;\stackrel{\simeq}{\to}\;
     \mathbb{S}_{dia}Mod
     \,,
   $$

   where $y(n)$ denotes the [[representable functor|functor represented]] by $dia(n)$ (i.e. by $n$ if $dia = Seq$, by $\{1,\cdots,n\}$ if $dia = Sym$, by $\mathbb{R}^n$ if $dia = Orth$ and by $S^n$ if $dia = Top^{\ast/}_{fin}$).

1. On the free $\mathbb{S}_{dia}$-module on $e \in Dia^{op} \stackrel{y}{\hookrightarrow} [Dia, Top^{\ast/}]$ this takes the value

  $$
    (F^{dia}_n K)(e)
      \;=\;
    \underset{\underset{e_1 \otimes e_2 \to e}{\longrightarrow}}{\lim}
    Dia(n,e_1)\wedge \mathbb{S}_{dia}(e_2) \wedge K
    \,.
  $$

=--

([MMSS00, p. 7 with theorem 2.2](#MMSS00))

+-- {: .proof}
###### Proof

Generally, for $\mathcal{C}$ a $V$-[[enriched category|enriched]] [[symmetric monoidal category]], and for $c\in \mathcal{C}$ an object, then there is an [[adjunction]]

$$
  [\mathcal{C}, V]
    \stackrel{\overset{y(d)\otimes(-)}{\longleftarrow}}{\underset{(-)_c}{\longrightarrow}}
  V
$$

whose characterizing [[natural isomorphism]] is the combination of that of [[tensoring]] with the [[Yoneda embedding]]:

$$
  [\mathcal{C},V]( y(d) \otimes K, F )
    \simeq
  V( K, [\mathcal{C},V]( y(d), F ) )
    \simeq
  V(K, F(d))
  \,.
$$ 

Specializing this to our case with $V = Top^{\ast/}$ and $\mathcal{C} = \mathbb{S}_{dia} FreeMod^{op}$ yields the first statement. The second follows from similar yoga, see the formula at _[Day convolution -- Modules](Day+convolution#FreeModulesOverAMonoidInDayConvolution)_.

=--

+-- {: .num_prop #ExplicitFormOfFreeSpectra}
###### Proposition

Explicitly, the [[free spectra]] according to def. \ref{FreeStructuredSpectrum}, look as follows:

For [[sequential spectra]]: $(F^{Seq}_n K)_q \simeq K \wedge S^{q-n}$;

for [[symmetric spectra]]: $(F^{Sym}_n K)_q \simeq \Sigma(q)_+ \wedge_{\Sigma(q-n)} K \wedge S^{q-n}$.

for [[orthogonal spectra]]: $(F^{Orth}_n K)_q \simeq O(q)_+ \wedge_{O(q-n)} K \wedge S^{q-n}$.

In particular: 

1. $F_0 K = \Sigma^\infty K$;

1. $F_n^{Seq}S^n$ is like the [[suspension spectrum]] of the point (the standard sequential [[sphere spectrum]]) but with its first $n$ components simply removed.


=--

(e.g. [Schwede 12, example 3.20](#Schwede12))

+-- {: .proof}
###### Proof

By working out the formula in item 2 of lemma \ref{ExplicitExpressionForFreeSpectra}. In the sequential case $(Dia = Seq)$ there exists a morphism $k_1 \otimes k_2 \to k_3$ only if $k_1 + k_2 = k_3$ and then there is a unique such. Hence here the colimit in the formula becomes a [[coproduct]] and we find

$$
  \begin{aligned}
    (F^{Seq}_n K)(q)
      & \simeq
    \underset{e_1+e_2 = q}{\coprod} 
    \underset{\simeq\left\{ \array{S^0 & if\, n = e_1 \\ \ast & otherwise}\right.}{\underbrace{Seq(n,e_1)}} \wedge \mathbb{S}_{dia}(e_2) \wedge K
    \\
     & \simeq
      S^{q-n}\wedge K
  \end{aligned}
  \,.
$$

In the symmetric case ($Dia = Sym$) the formula is similar, except that $S^0 = Seq(q,q)_+$ is replaced by $Sym(q,q)_+ = \Sigma(q)_+$ and the colimit goes over the automorphisms that fix $q-n$ elements, thereby producing the partial smash tensor shown in the statement. Analogously for the orthogonal case ($Dia = Orth$).

=--

One use of free spectra, important in the verification of the stable model structures [below](#ProofOfTheStableModelStructure) and in the dicussion of the stable equivalences [further below](#RelatingStableEquivalencesAndStableWeakHomotopyEquivalences), is that they serve to co-represent adjuncts of structure morphisms of spectra. To this end, first consider the following general existence statement.

+-- {: .num_lemma #CorepresentingOfAdjunctsOfStructureMapsExists}
###### Lemma

For each $n \in \mathbb{N}$ there exists a morphism

$$
  \lambda_n
    \;\colon\;
  F_{n+1}^{dia}S^1
    \longrightarrow
  F_n^{dia} S^0
$$

such that for every $X\in \mathbb{S}_{dia} Mod$ precomposition $\lambda_n^\ast$ forms a [[commuting diagram]] of the form

$$
  \array{
    \mathbb{S}_{dia}Mod(F^{dia}_n S^0, X) &\simeq& Top^{\ast/}(S^0,X_n) &\simeq& X_n
    \\
    \downarrow^{\mathrlap{\lambda_n^\ast}}
    && &&
    \downarrow^{\mathrlap{\tilde \sigma^X_n}}
    \\
    \mathbb{S}_{dia}Mod(F^{dia}_{n+1} S^1, X)
    &\simeq&
    Top^{\ast/}(S^1, X_{n+1})
    &\simeq&
    \Omega X_{n+1}
  }
  \,,
$$

where the horizontal equivalences are the [[adjunction]] isomorphisms and the canonical identification, and where the right morphism is the $(\Sigma \dashv \Omega)$-[[adjunct]] of the structure map $\sigma_n$ of the [[sequential spectrum]] $seq^\ast X$ underlying $X$ (def. \ref{NotationForGenericDiagramSpectra}).

=--

+-- {: .proof}
###### Proof

Since all prescribed morphisms in the diagram are [[natural transformations]], this is in fact a diagram of copreheaves on $\mathbb{S}_{dia} Mod$

$$
  \array{
    \mathbb{S}_{dia}Mod(F^{dia}_n S^0, -) &\simeq& Top^{\ast/}(S^0,(-)_n) &\simeq& (-)_n
    \\
    \downarrow^{\mathrlap{}}
    && &&
    \downarrow^{\mathrlap{\tilde \sigma^{(-)}_n}}
    \\
    \mathbb{S}_{dia}Mod(F^{dia}_{n+1} S^1, -)
    &\simeq&
    Top^{\ast/}(S^1, (-)_{n+1})
    &\simeq&
    \Omega (-)_{n+1}
  }
  \,.
$$

With this the statement follows by the [[Yoneda lemma]].

=--

Now we say explicitly what these maps are:

+-- {: .num_defn #CorepresentationOfAdjunctsOfStructureMaps}
###### Definition

For $n \in \mathbb{N}$, write

$$
  \lambda_n \;\colon\; F_{n+1} S^1 \longrightarrow F_n S^0
$$

for the [[adjunct]] under the ([[free structured spectrum]] $\dashv$ $n$-component)-[[adjunction]] in def. \ref{FreeStructuredSpectrum} of the composite morphism

$$
  S^1 
    \stackrel{=}{\to}
  (F_n^{Seq}(S^0))_{n+1}
    \stackrel{(f_n^{Seq})_{n+1}}{\hookrightarrow} 
  (F^{dia}_n S^0)_{n+1}
  \,,
$$

where the first morphism is via prop. \ref{ExplicitFormOfFreeSpectra} and the second comes from the adjunction units according to def. \ref{FreeStructuredSpectrum}.

=--

([MMSS 00, def. 8.4](#MMSS00), [Schwede 12, example 4.26](#Schwede12))

+-- {: .num_lemma #IndeedCorepresentationOfAdjunctsOfStructureMaps}
###### Lemma

The morphisms of def. \ref{CorepresentationOfAdjunctsOfStructureMaps} are those whose existence is asserted by prop. \ref{CorepresentingOfAdjunctsOfStructureMapsExists}.
 
=--

([MMSS 00, lemma 8.5](#MMSS00), following [Hovey-Shipley-Smith 00, remark 2.2.12](#HoveyShipleySmith00))


+-- {: .proof}
###### Proof

Consider the case $Dia = Seq$ and $n = 0$. All other cases work analogously.

By lemma \ref{ExplicitFormOfFreeSpectra}, in this case the morphism $\lambda_0$ has components like so:

$$
  \array{
    \vdots && \vdots
    \\
    S^3 &\stackrel{id}{\longrightarrow}& S^3
    \\
    S^2 &\stackrel{id}{\longrightarrow}& S^2
    \\
    S^1 &\stackrel{id}{\longrightarrow}& S^1
    \\
    \ast &\stackrel{0}{\longrightarrow}& S^0
    \\
    \underbrace{\,\,\,} && \underbrace{\,\,\,}
    \\
    F_1 S^1 &\stackrel{\lambda_0}{\longrightarrow}& F_0 S^0
  }
  \,.
$$

Now for $X$ any sequential spectrum, then a morphism $f \colon F_0 S^0 \to X$ is uniquely determined by its 0th components $f_0 \colon S^0 \to X_0$ (that's of course the very free property of $F_0 S^0$); as the compatibility with the structure maps forces the first component, in particular, to be $\sigma_0^X\circ \Sigma f$:

$$
  \array{
    \Sigma S^0 &\stackrel{\Sigma f}{\longrightarrow}& \Sigma X_0
    \\
    \downarrow^{\mathrlap{\simeq}} && \downarrow^{\mathrlap{\sigma_0^X}}
    \\
    S^1 &\stackrel{\sigma_0^X \circ \Sigma f}{\longrightarrow}& X_1
  }
$$

But that first component is just the component that similarly determines the precompositon of $f$ with $\lambda_0$, hence $\lambda_0^\ast f$ is fully fixed as being the map $\sigma_0^X \circ \Sigma f$. Therefore $\lambda_0^\ast$ is the function

$$
  \lambda_0^\ast
  \;\colon\;
  X_0 
  = 
  Maps(S^0, X_0)
  \stackrel{f \mapsto \sigma_0^X \circ \Sigma f}{\longrightarrow}
  \Maps(S^1, X_1)
  =
  \Omega X_1
  \,.
$$

It remains to see that this is the $(\Sigma \dashv \Omega)$-[[adjunct]] of $\sigma_0^X$. By the general formula for adjuncts, this is

$$
  \tilde \sigma_0^X 
    \;\colon\; 
  X_0 
     \stackrel{\eta}{\longrightarrow} 
  \Omega \Sigma X_0
     \stackrel{\Omega \sigma_0^X}{\longrightarrow}
  \Omega X_1
  \,.
$$

To compare to the above, we check what this does on points: $S^0 \stackrel{f_0}{\longrightarrow} X_0$ is sent to the composite

$$
   S^0 
     \stackrel{f_0}{\longrightarrow}
   X_0 
     \stackrel{\eta}{\longrightarrow} 
   \Omega \Sigma X_0
     \stackrel{\Omega \sigma_0^X}{\longrightarrow}
   \Omega X_1
   \,.
$$

To identify this as a map $S^1 \to X_1$ we use the adjunction isomorphism once more to throw all the $\Omega$-s on the right back to $\Sigma$-s the left, to finally find that this is indeed

$$
  \sigma_0^X \circ \Sigma f
    \;\colon\;
  S^1 = \Sigma S^0 \stackrel{\Sigma f}{\longrightarrow} \Sigma X_0 \stackrel{\sigma_0^X}{\longrightarrow} X_1
  \,.
$$

=--

The following property of the maps from def. \ref{CorepresentationOfAdjunctsOfStructureMaps} to be or not to be stable weak homotopy equivalences will be the key technical fact that implies ([below](#RelatingStableEquivalencesAndStableWeakHomotopyEquivalences)) that stable equivalences of spectra are or are not the same as stable weak homotopy equivalences.

+-- {: .num_lemma #AdjunctsOfFreeSpectrumInclusionsAreOrAreNotStableWeakHomotopyEquivalences}
###### Lemma

The maps $\lambda_n \;\colon\; F_{n+1} S^1 \longrightarrow F_n S^0$  in def. \ref{CorepresentationOfAdjunctsOfStructureMaps} are 

1. stable equivalences, according to def. \ref{StableEquivalencesForDiagramSpectra}, for all four cases of spectra, ${Dia} \in \{Top^{\ast/}, Orth, Sym, Seq\}$;

1. stable weak homotopy equivalences, according to def. \ref{StableEquivalencesForDiagramSpectra}, for sequential spectra, symmetric spectra and pre-excisive functors ${Dia} \in \{Top^{\ast/}, Orth, Seq\}$;


1. **not** stable weak homotopy equivalences for the case of symmetric spectra ${Dia} = {Sym}$.



=--

([Hovey-Shipley-Smith 00, example 3.1.10](#HoveyShipleySmith00), [MMSS 00, lemma 8.6](#MMSS00), [Schwede 12, example 4.26](#Schwede12))

+-- {: .proof}
###### Proof

The first statement is an immediate consequence of lemma \ref{IndeedCorepresentationOfAdjunctsOfStructureMaps}.

The other two statements follow from inspection of the explicit form of the maps, via prop. \ref{ExplicitFormOfFreeSpectra}, in each case separately:

**sequential case**

Here the components of the morphism eventually stabilize to isomorphisms

$$
  \array{
    & \vdots && \vdots
    \\
    (\lambda_n)_{n+3} & S^3 &\stackrel{id}{\longrightarrow}& S^3
    \\
    (\lambda_n)_{n+2} & S^2 &\stackrel{id}{\longrightarrow}& S^2
    \\
    (\lambda_n)_{n+1} & S^1 &\stackrel{id}{\longrightarrow}& S^1
    \\
    (\lambda_n)_n \colon & \ast &\stackrel{0}{\longrightarrow}& S^0
    \\
    & \ast &\longrightarrow& \ast
    \\
    & \vdots && \vdots
    \\
    & \ast &\longrightarrow& \ast
    \\
    & \underbrace{\,\,\,} && \underbrace{\,\,\,}
    \\
    \lambda_n \colon & F_{n+1} S^1 &\stackrel{}{\longrightarrow}& F_n S^0
  }
$$

and this immediately gives that $\lambda_n$ is an isomorphism on stable homotopy groups.

**orthogonal case**

Here for $q \geq n+1$ the $q$-component of $\lambda_n$ is the [[quotient]] map

$$
  (\lambda_n)_q 
    \;\colon\;
  O(q)_+ \wedge_{O(q-n-1)} S^{q-n}
   \simeq
  O(q)_+ \wedge_{O(q-n-1)} S^1 \wedge S^{q-n-1}
  \longrightarrow
  O(q)_+ \wedge_{O(q-n)}S^{q-n}
  \,.
$$

By the [suspension isomorphism](homotopy+group+of+a+spectrum#SuspensionIsomorphismOfStableHomotopyGroups) for [[stable homotopy groups]], $\lambda_n$ is a stable weak homotopy equivalence precisely if any of its [[reduced suspension|suspensions]] is. Hence consider instead $\Sigma^n \lambda_n \coloneqq S^n \wedge \lambda_n$, whose $q$-component is 

$$
  (\Sigma^n\lambda_n)_q 
    \;\colon\;
  O(q)_+ \wedge_{O(q-n-1)} S^{q}
    \longrightarrow
  O(q)_+ \wedge_{O(q-n)}S^{q}
  \,.
$$

Now due to the fact that $O(q-k)$-action on $S^q$ lifts to an $O(q)$-action, the quotients of the diagonal action of $O(q-k)$ equivalently become quotients of just the left action. Formally this is due to the existence of the [[commuting diagram]]

$$
  \array{
    O(q)_+ \wedge S^q 
     &\stackrel{id}{\longrightarrow}& 
    O(q)_+ \wedge S^q 
     &\stackrel{id}{\longrightarrow}& 
    O(q)_+ \wedge S^q 
    \\
    \downarrow && \downarrow && \downarrow^{\mathrlap{p_2}}
    \\
    Q(q)_+ \wedge_{Q(q-k)} S^q 
     &\longrightarrow&
    Q(q)_+ \wedge_{Q(q)} S^q
    & \stackrel{\simeq}{\longrightarrow} & S^q
  }
$$

which says that the image of any $(g,s) \in O(q)_+  \wedge S^q$ in the quotient $Q(q)_+ \wedge_{Q(q-k)} S^q$ is labeled by $([g],s)$.

It follows that $(\Sigma^n\lambda_n)_q$ is the smash product of a projection map of [[coset spaces]] with the identity on the sphere:

$$
  (\Sigma^n\lambda_n)_q 
    \simeq
  proj_+ \wedge id_{S^q} 
    \;\colon\;
  O(q)/O(q-n-1)_+ \wedge S^q
    \longrightarrow
  O(q)/O(q-n)_+ \wedge S^{q}
  \,.
$$

Now finally observe that this projection function

$$
  proj
  \;\colon\;
  O(q)/O(q-n-1) 
    \longrightarrow
  O(q)/O(q-n)
$$

is $(q - n -1 )$-connected (see [here](coset+space#CofiberSequencesOfCosetsOfOrthogonalGroups)). Hence its smash product with $S^q$ is $(2q - n -1 )$-connected.

The key here is the fast growth of the connectivity with $q$. This implies that for each $s$ there exists $q$ such that $\pi_{s+q}((\Sigma^n \lambda_n)_q)$ becomes an isomorphism. Hence $\Sigma^n \lambda_n$ is a stable weak homotopy equivalence and therefore so is $\lambda_n$.

**symmetric case**
 
Here the morphism $\lambda_n$ has the same form as in the orthogonal case above, except that all occurences of [[orthogonal groups]] are replaced by just their sub-[[symmetric groups]].

Accordingly, the analysis then proceeds entirely analogously, with the key difference that the projection

$$
  \Sigma(q)/\Sigma(q-n-1) 
    \longrightarrow
  \Sigma(q)/\Sigma(q-n)
$$

does _not_ become highly connected as $q$ increases, due to the [[discrete topological space]] underlying the symmetric group. Accordingly the conclusion now is the opposite: $\lambda_n$ is not a stable weak homotopy equivalence in this case.

=--

Another use of free spectra is that their [[pushout products]] may be explicitly analyzed, and checking the [[pushout-product axiom]] for general cofibrations may be reduced to checking it on morphisms between free spectra.

+-- {: .num_lemma #SmashProductOfFreeSpectra}
###### Lemma

For $A, B \in Top^{\ast/}$ and for $k,\ell \in \mathbb{N}$, then the [[symmetric monoidal smash product of spectra]], def. \ref{SymmetricSmashProductOfDiagramSpectra}, applied to the corresponding [[free spectra]] from def. \ref{FreeStructuredSpectrum} relates to the plain [[smash product]] of [[pointed topological spaces]] via [[natural isomorphisms]]

$$
  (F_k A)\wedge_{\mathbb{S}_{dia}} (F_\ell B)
  \simeq
  F_{k+\ell}(A\wedge B)
  \,.
$$

=--

([MMSS 00, lemma 1.8, lemma 21.3](#MMSS00))

+-- {: .proof}
###### Proof

Consider the following sequence of [[natural isomorphisms]]

$$
  \begin{aligned}
    [\mathbb{S}_{dia} FreeMod^{op},Top^{\ast/}]((F_k A)\wedge_{\mathbb{S}_{dia}} (F_\ell B), Z)
    & \simeq
     [\mathbb{S}_{dia} FreeMod^{op}\times \mathbb{S}_{dia} FreeMod^{op}, Top^{\ast/}]((F_k A)\tilde \wedge (F_\ell B), Z \circ \wedge)
    \\
    & \simeq 
    Top^{\ast/}( A\wedge B, F_{k+\ell})
    \\
    & \simeq
    [\mathbb{S}_{dia} FreeMod^{op},Top^{\ast/}](
      F_{k+\ell}(A \wedge B), Z
    )    
  \end{aligned}
  \,,
$$

where we used the adjoint characterization ([here](Day+convolution#DayConvolutionViaNaturalIsosInvolvingExternalTensorAndTensor)) of the [[Day convolution]]. Since this is natural in $Z$, the [[Yoneda lemma]] implies the claim.

=--

+-- {: .num_lemma #PushoutSmashProductOfFreeSpectraOnGeneratingCofibrationsOfTop}
###### Lemma

The [[symmetric monoidal smash product of spectra]] of the [[free spectrum]] constructions (def. \ref{FreeStructuredSpectrum}) on the generating cofibrations $\{S^{n-1}\overset{i_n}{\hookrightarrow} D^n\}_{n \in \mathbb{B}}$ of the [[classical model structure on topological spaces]] is given by addition of indices

$$
  (F_k i_{n_1}) \Box_{\mathbb{S}_{dia}} (F_\ell i_{n_2})
  \simeq
  F_{k+\ell}( i_{n_1 + n_2})
  \,.
$$

=--

+-- {: .proof}
###### Proof

By lemma \ref{SmashProductOfFreeSpectra} the [[commuting diagram]] defining the [[pushout product]] of [[free spectra]]

$$
  \array{
    && F_k S^{n_1-1}_+ \wedge_{\mathbb{S}_{dia}} F_{\ell} S^{n_2-1}_+
    \\
    & \swarrow && \searrow
    \\
    F_k D^{n_1}_+ \wedge_{\mathbb{S}_{dia}} F_{\ell} S^{n_2-1}_+
    &&
    &&
    F_k S^{n_1-1}_+ \wedge_{\mathbb{S}_{dia}} F_{\ell} D^{n_2-1}_+
    \\
    & \searrow && \swarrow
    \\
    && F_k D^{n_1-1}_+ \wedge_{\mathbb{S}_{dia}} F_k D^{n_2-1}_+
  }
$$

is equivalent to this diagram:

$$
  \array{
    && F_{k+\ell}((S^{n_1-1}\times S^{n_2-1})_+)
    \\
    & \swarrow && \searrow
    \\
    F_{k+\ell}((D^{n_1} \times S^{n_2-1})_+)
    &&
    &&
    F_{k+\ell}((S^{n_1-1} \times D^{n_2})_+)
    \\
    & \searrow && \swarrow
    \\
    && F_{k+ \ell}( (D^{n_1}\times D^{n_2})_+ )
  }
  \,.
$$

Since the [[free spectrum]] construction is a left adjoint, it preserves pushouts, and so 

$$
  (F_{k}i_{n_1}) 
    \Box_{\mathbb{S}_{dia}}
  (F_{\ell}i_{n_2})
   \simeq
  F_{k + \ell}( i_{n_1} \Box i_{n_2})
   \simeq
  F_{k + \ell}( i_{n_1 + n_2})
 \,,
$$

where in the second step we used [this lemma](pushout-product#PushoutProductOfSpheresInclusionsIntoDisks).

=--

##### Stable equivalences

We discuss that the two concepts of _stable equivalences_ and of _stable weak homotopy equivalences_ in def. \ref{StableEquivalencesForDiagramSpectra} actually agree in the cases of a) pre-[[excisive functors]], b) [[orthogonal spectra]] and c) [[sequential spectra]], while in the case of [[symmetric spectra]] the class of stable equivalences includes but is strictly larger than that of stable weak homotopy equivalences. 

This is important in practice, since the stable equivalences are the weakequivalences in the stable model structure of theorem \ref{StableModelStructuresOnDiagramSpectra}, while the [[stable weak homotopy equivalences]] are typically more readily identified.


> Parts of the proof in the following rely on the verification of the stable model structure established further [below](#TheStableModelStructures), which is independent of the discussion here.

+-- {: .num_theorem #RelationBetweenStableEquivalencesAndStableWeakHomotopyEquivalencesForDiagramSpectra}
###### Theorem

In $\mathbb{S}Mod$, $\mathbb{S}_{Orth} Mod$ and in $\mathbb{S}_{Seq} Mod$ we have for the concepts from def. \ref{StableEquivalencesForDiagramSpectra} that

$$
  stable\;weak\;homotopy\;equivalence 
  \;\Leftrightarrow\;
  stable \; equivalence
  \,.
$$

In $\mathbb{S}_{Sym}Mod$ however we only have

$$
  stable\;weak\;homotopy\;equivalence 
  \;\Rightarrow\;
  stable \; equivalence
$$

but the reverse implication is false.

=--

([MMSS00, prop. 8.7, prop. 8.8](#MMSS00))

We break up this statement below as prop. \ref{StableWeakHomotopyEquivalenceIsStableEquivalence} and prop. \ref{StableEquivalencesThatAreStableWeakHomotopyEquivalences}.

The argument that every stable weak homotopy equivalence is in particular a stable equivalence is fairly formal; this we turn to first in prop. \ref{StableWeakHomotopyEquivalenceIsStableEquivalence} below. The converse statement in prop. \ref{StableEquivalencesThatAreStableWeakHomotopyEquivalences} however relies on explicit analysis of the class $K$ of generating acylic cofibrations in def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra}. 

+-- {: .num_defn #AKindOfAlmostSpectrification}
###### Definition

For $\lambda_0 \colon F^{dia}_1 S^1 \to F^{dia}_0 S^0$ from lemma \ref{CorepresentingOfAdjunctsOfStructureMapsExists}, consider the [[natural transformation]] in $X \in \mathbb{S}_{dia}Mod$ given by the left vertical morphism in 

$$
  \array{
    X &\simeq& \mathbb{S}_{dia} Mod(F^{dia}_0 S^0, X)
    \\
    \downarrow^{\mathrlap{\lambda_0^\ast(X)}} && \downarrow^{\mathrlap{\mathbb{S}_{dia}Mod(\lambda_0, X)}}
    \\
    R X &\coloneqq& \mathbb{S}_{dia}Mod(F^{dia}_1 S^1, X)
  }
  \,,
$$

where the top morphism is the $(F^{dia}_0 \dashv (-)_0)$-adjunction isomorphism.
Write

$$
  R^\infty X
  \coloneqq
  \underset{\longrightarrow}{\lim}
  \left(
    X 
     \stackrel{\lambda_0^\ast(X)}{\longrightarrow}
    R X
     \stackrel{R(\lambda_0^\ast(X))}{\longrightarrow}
    R R X  
     \stackrel{R R(\lambda_0^\ast(X))}{\longrightarrow}
    \cdots
  \right)
$$

for the [[homotopy colimit]] over the resulting sequence of iterations. Write 

$$
  r_X \colon X \longrightarrow R^\infty X
$$

for the 0th-component map into the colimit.

=--


+-- {: .num_lemma #PropertiesOfAKindOfAlmostSpectrification}
###### Lemma

The functor $R^\infty$ from def. \ref{AKindOfAlmostSpectrification} has the following properties.

1. for $E$ an Omega-spectrum according to def. \ref{StableEquivalencesForDiagramSpectra}, then, by lemma \ref{CorepresentingOfAdjunctsOfStructureMapsExists}, $\lambda_0^\ast(E)$ is weak equivalence in the strict model structure (prop. \ref{StrictModelStructureOnDiagramSpectra}), and hence so is $r_E$;

1. for $f\colon X \longrightarrow Y$ a stable weak homotopy equivalence according to def. \ref{StableEquivalencesForDiagramSpectra}, then $R^\infty f \colon R^\infty X \longrightarrow R^\infty Y$ is a weak equivalence in the strict model structure.

=--

([MMSS 00, prop. 8.8](#MMSS00))


+-- {: .num_prop #StableWeakHomotopyEquivalenceIsStableEquivalence}
###### Proposition

In def. \ref{StableEquivalencesForDiagramSpectra} every stable weak homotopy equivalence is a stable equivalence.

=--

([MMSS 00, prop. 8.8](#MMSS00), following [Hovey-Shipley-Smith 00, theorem 3.1.11](#HoveyShipleySmith00))


+-- {: .proof}
###### Proof

Let $E$ be an Omega-spectrum. Then by the first item of lemma \ref{PropertiesOfAKindOfAlmostSpectrification}, for every $X$ the morphism obtained by homming $X$ into  $r_E$ of $E$ 

$$
  [X,r_E]_{strict}
    \;\colon\; 
  [X,E]_{strict} 
    \longrightarrow 
  [X, R^\infty E]_{strict}
$$

(in the [[homotopy category of a model category|homotopy category]] of the strict model structure from theorem \ref{StrictModelStructureOnSequentialPrespectraIsModelCategory}) is an isomorphism. Since $r_{(-)}$ is a [[natural transformation]] (by def. \ref{AKindOfAlmostSpectrification}), the naturality squares gives a factorization of this morphism as

$$
  [X,r_E]_{strict}
    \;\colon\;
  [X,E]_{strict} 
    \stackrel{R^\infty}{\longrightarrow}
  [R^\infty X, R^\infty E]_{strict}
    \stackrel{[r_X,E]_{strict}}{\longrightarrow}
  [X, R^\infty E]_{strict}  
$$

Combining this with vertical morphisms as below, which are isomorphisms again by item 1 of lemma \ref{AKindOfAlmostSpectrification},

$$
  \array{
     &
      &&
    [R^\infty X, E]_{strict}
      &\stackrel{}{\longrightarrow}&
    [X, E]_{strict}  
    \\
    & &\nearrow& 
    {}^{\mathllap{\simeq}}\downarrow^{\mathrlap{[R^\infty X,r_E]}} 
     && 
    {}^{\mathllap{\simeq}}\downarrow^{\mathrlap{[X,r_E]}}
    \\
    [X,r_E]_{strict}
      \;\colon\;
     &
    [X,E]_{strict} 
      &\stackrel{R^\infty}{\longrightarrow}&
    [R^\infty X, R^\infty E]_{strict}
      &\stackrel{[r_X,E]_{strict}}{\longrightarrow}&
    [X, R^\infty E]_{strict}  
  }
$$

exhibits a [[retraction]] 

$$
  id \colon [X,E]_{strict} \longrightarrow [R^\infty X,E]_{strict} \longrightarrow [X,E]_{strict}
  \,,
$$ 

which is natural in $X$. This naturality now implies a retraction of morphisms

$$
  \array{
    id_{[Y,E]_{strict}} \colon & [Y,E]_{strict} &\longrightarrow& [R^\infty Y,E]_{strict} &\longrightarrow& [Y,E]_{strict}
    \\
    & \downarrow^{\mathrlap{[f,E]_{strict}}} && \downarrow^{\mathrlap{[R^\infty f,E]_{strict}}}
     &&
     \downarrow^{\mathrlap{[f,E]_{strict}}}
    \\
    id_{[X,E]_{strict}} \colon & [X,E]_{strict} &\longrightarrow& [R^\infty X,E]_{strict} &\longrightarrow& [X,E]_{strict}
  }
  \,.
$$

Finally, by the second item of lemma \ref{PropertiesOfAKindOfAlmostSpectrification}, the middle vertical morphism here is an isomorphism, hence $[f^\ast, E]_{strict}$ is the retract of an iso and hence ([here](retract#RetractOfIso)) an isomorphism itself, for all Omega-spectra $E$. This means by definition that $f^\ast$ is a stable equivalence.


=--


Now for the converse.



+-- {: .num_prop #StableEquivalencesThatAreStableWeakHomotopyEquivalences}
###### Proposition

In the case $Dia \in \{Top^{\ast/}, Orth, Seq\}$, hence for [[sequential spectra]], [[orthogonal spectra]] and pre-[[excisive functors]], stable equivalences are stable weak homotopy equivalences (def. \ref{StableEquivalencesForDiagramSpectra}).

=--

([MMSS 00, p.31-32](#MMSS00))

+-- {: .proof}
###### Proof idea

By theorem ref. \ref{StableModelStructuresOnDiagramSpectra}, and by lemmas  \ref{KInjectiveStableEquivalencesAreStrictEquivalences} and \ref{RetractsOfRelativeKCellComplexesAreTheStableEquivalencesAndStrictCofibrationsForSequentialSpectra}, every stable weak equivalence factors as a $K$-[[relative cell complex]] followed by weak equivalence in the strict model structure. Since the latter is degreewise a [[weak homotopy equivalence]] it is in particular a [[stable weak homotopy equivalence]]. Hence we are reduced to showing that every $K$-[[relative cell complex]] is a stable weak homotopy equivalence.

Observe now that we know this to be true for the elements of $K$ itself (def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra}): first of all, the elements in $F J$ are [[retracts]] of [[deformation retracts]] and therefore stable weak homotopy equivalences. Second, the morphisms denoted $k_n$ in def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra}, which resolve the maps $\lambda_n$ from def. \ref{CorepresentationOfAdjunctsOfStructureMaps}, as stable weak homotopy equivalences by lemma \ref{AdjunctsOfFreeSpectrumInclusionsAreOrAreNotStableWeakHomotopyEquivalences}.  This implies that so are their pushout products $k_n \Box i$. 

=--

This completes the proof of theorem \ref{RelationBetweenStableEquivalencesAndStableWeakHomotopyEquivalencesForDiagramSpectra}.





#### Symmetric smash monoidal model structure
 {#MonoidalStableModelStructure}


+-- {: .num_theorem}
###### Theorem

The stable model structures from theorem \ref{StableModelStructuresOnDiagramSpectra} on the [[categories of modules]] from prop. \ref{HighlyStructuredSpectraAsDayConvolutionSModules}, remark \ref{PreExcisiveFunctorsAreSModules}

$$
  \mathbb{S}Mod_r \simeq [Top_{fin}^{\ast/}, Top^{\ast/}]
$$

$$
  \mathbb{S}_{Orth} Mod_r \simeq OrthSpec(Top)
$$

$$
  \mathbb{S}_{Sym} Mod_r \simeq SymSpec(Top)
$$

are compatible with their [[monoidal category]] structure given by the [[symmetric monoidal smash product of spectra]] $\wedge$ of def. \ref{SymmetricSmashProductOfDiagramSpectra}, in that $(\mathbb{S}_{dia} Mod_{stable}, \wedge_{\mathbb{S}_{dia}})$ in these cases

1. is a [[stable model category]];

1. satisfying the [[monoid axiom in a monoidal model category]].

=--

([MMSS 00, theorem 12.1 (iii) with prop. 12.3](#MMSS00)) 

We give the proof below (...) after a sequence of lemmas.

+-- {: .num_lemma #PushoutSmashProductOfStableCofibsIsStableCofib}
###### Lemma

The [[pushout product]] of two cofibrations in $\mathbb{S}_{dia}Mod_{stable}$ is again a cofibration.

=--

+-- {: .proof}
###### Proof

A general abstract fact about [[pushout-products]] ([Hovey-Shipley-Smith 00, prop. 5.3.4](#HoveyShipleySmith00), see _[here](pushout-product#PushoutProductOfCofClassIsCofClassOfPushoutProduct)_) is that for $I_1, I_2$ two classes of morphisms in a [[symmetric monoidal category|closed]] [[symmetric monoidal category]] with [[finite limits]] and [[finite colimits]], and writing $I_i Cof$ for their saturated classes, then under [[pushout-product]] $\Box$:

$$
  (I_1 Cof) \Box (I_2 Cof)
  \subset 
  (I_1 \Box I_2) Cof
  \,.
$$

Since the cofibrations of the stable model structure, theorem \ref{StableModelStructuresOnDiagramSpectra}, are elements in


$$
  Cof_{stable} = (F I) Cof
$$

with $F I$ the class of [[free spectra]] on the class of generating cofibrations $I$ of the [[classical model structure on topological spaces]], def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra}, this implies in the present case that 

$$
  Cof_{stable} \Box Cof_{stable}
  \subset
  (F I \Box F I) Cof
  \,.
$$

Now lemma \ref{PushoutSmashProductOfFreeSpectraOnGeneratingCofibrationsOfTop} implies that 

$$
  F I \Box F I
  =
  F(I \Box I)
  =
  F I 
$$

and hence the claim follows.

=--



+-- {: .num_lemma }
###### Lemma

Let $Y \in \mathbb{S}_{dia} Mod_{stable}$ be cofibrant.
Then the [[smash product of spectra]]-[[functor]] (def. \ref{SymmetricSmashProductOfDiagramSpectra})

$$
  X \wedge_{\mathbb{S}_{dia}}(-)
    \;\colon\;
  \mathbb{S}_{dia} Mod
    \longrightarrow
  \mathbb{S}_{dia} Mod
$$

preserves [[stable weak homotopy equivalences]] as well as stable equivalences (def. \ref{StableEquivalencesForDiagramSpectra}).

=--

([MMSS 00, prop. 12.3](#MMSS00))

+-- {: .num_lemma }
###### Lemma

The functor

$$
  X \wedge_{\mathbb{S}_{dia}}(-)
    \;\colon\;
  \mathbb{S}_{dia} Mod
    \longrightarrow
  \mathbb{S}_{dia} Mod
$$

sends acylic cofibrations in the stable model structure to morphisms that are stable equivalences and [[h-cofibrations]].

=--

([MMSS 00, prop. 12.5](#MMSS00))

+-- {: .num_prop #StableModelStructureWithSymmetricMonoidalSmashProductSatisfiesPushoutProductAxiom}
###### Proposition

The [[symmetric monoidal smash product of spectra]] $\wedge_{\mathbb{S}_{dia}}$ on $\mathbb{S}_{dia} Mod$, def. \ref{SymmetricSmashProductOfDiagramSpectra} satisfies the [[pushout-product axiom]] with respect to the stable model structure $\mathbb{S}_{dia} Mod$ of theorem \ref{StableModelStructuresOnDiagramSpectra}.

=--

([MMSS 00, prop. 12.6](#MMSS00))

+-- {: .proof}
###### Proof

That the pushout product of two stable cofibrations is again a stable cofibration is the content of lemma \ref{PushoutSmashProductOfStableCofibsIsStableCofib}. It remains to show that if at least one of them is a stanble equivalence, def. \ref{StableEquivalencesForDiagramSpectra}, then so is the pushout-product.
That follows with a laborious argument using the above lemmas (...).

=--

(...)



### **1.3)** Higher algebra
 {#HigherAlgebra}


[[!include homological and higher algebra -- table]]

#### Ring spectra
 {#RingSpectra}

[[ring spectra]]


#### Module spectra

[[module spectra]]

* [[module object]]



#### Examples: $HA, KO, KU, \cdots, MO, MU\, (BP), S$
 {#Examples}

[[HA]], [[KO]], [[KU]], [[MO]], ... [[MU]] ([[BP]]), [[S]]



### Localization
 {#Localization}

[[Bousfield localization of spectra]]

[[fracture theorem]]

[[Bousfield-Kan spectral sequence]]

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

([Bousfield 79](#Bousfield79))

For more discussion of [[E-infinity geometry|E-infinity]] (derived) [[formal completions]] via totalizations of [[Amitsur complexes]], see ([Carlsson 07](completion+of+a+module#Carlsson07)).



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

Original statements of this include ([Bousfield 79](#Bousfield79), [Sullivan 05, prop. 3.20](#Sullivan05)). Review includes ([van Koughnett 13, prop. 4.5](#VanKoughnett13)). 


So the [[arithmetic fracture square]] from [[Weil uniformization theorem|Weil uniformization]] over [[Spec(S)]] synthesizes spectra from their formal completion and torsion approximation:


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

(and there is further fracturing of the $p$-local part by [[chromatic homotopy theory]]).

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

The first statement originates around ([Bousfield 79, prop. 2.6](Bousfield+localization+of+spectra#Bousfield79)), review includes ([van Koughnett 13, prop. 4.4](Bousfield+localization+of+spectra#VanKoughnett13)); the second is highlighted in ([Strickland 12, MO comment](http://mathoverflow.net/a/91057/381)).


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

## References
 {#References}

We give the modern picture of the stable homotopy category, for which a quick survey may be found in

* {#Malkiewich14} [[Cary Malkiewich]], _The stable homotopy category_, 2014 ([pdf](http://math.uiuc.edu/~cmalkiew/stable.pdf)).

A classical textbook  on stable homotopy theory for "unstructured" spectra is

* {#Adams74} [[Frank Adams]], part III sections 2, 4-7 of _[[Stable homotopy and generalized homology]]_, Chicago Lectures in mathematics, 1974

For establishing the stable model structure on spectra we use the [[Bousfield-Friedlander theorem]] as discussed in 

* {#GoerssJardine96} [[Paul Goerss]], [[Rick Jardine]], section X.4 of _[[Simplicial homotopy theory]]_, (1996)

and applied to general Omega-spectrification functors as in 

* {#Schwede97} [[Stefan Schwede]], _Spectra in model categories and applications to the algebraic cotangent complex_, Journal of Pure and Applied Algebra 120 (1997) 77-104 ([pdf](http://www.math.uni-bonn.de/people/schwede/modelspec.pdf))

For the discussion of [[ring spectra]] we pass to [[symmetric spectra]] and [[orthogonal spectra]]. A comprehensive account of the former is in

* {#Schwede12} [[Stefan Schwede]], _[[Symmetric spectra]]_, 2012 ([pdf](http://www.math.uni-bonn.de/~schwede/SymSpec-v3.pdf))

