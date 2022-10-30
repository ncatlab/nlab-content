

{:bluebox: .un_remark style="border:solid #000000;background: #E6DF13;border-width:2px 1px;padding:0 1em;margin:0 1em;"}

***



$\,$

$\,$


+-- {: .standout}


[V4D2 -- Algebraic Topology II](https://basis.uni-bonn.de/qisserver/rds?state=verpublish&status=init&vmfile=no&publishid=109556&moduleCall=webInfo&publishConfFile=webInfo&publishSubDir=veranstaltung)

$\;\;\;\;\;\;\;\;\;\;\;$ **Stable Homotopy Theory**

$\;\;\;\;\;\;\;\;\;\;\;$ Dr. [[Urs Schreiber]]

[[Introduction to Stable homotopy theory|Lecture]] and [[Introduction to Stable homotopy theory -- S|Seminar]]

=--

$\,$


**Abstract** _We give an introduction to the [[stable homotopy category]] and to its key computational tool, the [[Adams spectral sequence]]. In the accompanying [seminar](#ComplexOrientedCohomology) we work through related classical results in [[cobordism theory]] and [[complex oriented cohomology]] such as to converge in the end to a glimpse of the modern picture of [[chromatic homotopy theory]]._



$\,$

***

Lecture notes.

Main page: _[[Introduction to Stable homotopy theory]]_.

Previous section: _[[Introduction to Stable homotopy theory -- P|Prelude -- Classical homotopy theory]]_

This section: _Part 1 -- Stable homotopy theory_

Next section: _[[Introduction to Stable homotopy theory -- 2|Part 2 -- Adams spectral sequences]]_

***

$\,$


#Contents#
* table of contents
{:toc}

## **Part 1) Stable homotopy theory**
 {#StableHomotopyTheory}


We now set up [[stable homotopy theory]].
 
**Literature.** For a decent quick idea see ([Malkiewich 14](#Malkiewich14)).
For a little more details the original lecture ([Adams 74, part III sections 2-7](#Adams74)) is still recommendable (except where it considers the [[stable homotopy category]] in its incarnation as the [[Adams category]], better to consider the [[homotopy category of a model category|homotopy category]] of the [[model structure on topological sequential spectra]]; we go through this [below](#Spectra)). A detailed modern account is ([Schwede 12](#Schwede12)).

$\,$

Recall from the [[Introduction to Stable homotopy theory -- P|classical homotopy theory]] ([prop.](Introduction+to+Stable+homotopy+theory+--+P#SuspensionAndLoopAreAdjointOnHomotopyCategory)) that the [[loop space]] functor $\Omega$ and the [[reduced suspension]] functor $\Sigma$ on the [[classical homotopy category]] of [[pointed topological spaces]] are [[adjoint functors]], with $\Sigma$ [[left adjoint]] and $\Omega$ [[right adjoint]]:

$$
  (\Sigma \dashv \Omega)
  \;\colon\;
  Ho(Top^{\ast/})
   \longrightarrow
  Ho(Top^{\ast/})
  \,.
$$

The _[[stable homotopy category]]_ $Ho(Spectra)$ is to be the result of stabilizing the adjunction in prop. \ref{SuspensionAndLoopAreAdjointOnHomotopyCategory}, in the sense of forcing it to become an [[equivalence of categories]]:

$$
  \array{
     Ho(Top^{\ast/}) 
      &
      \underoverset{\underset{\Omega}{\longrightarrow}}{\overset{\Sigma}{\longleftarrow}}{} 
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
  \,,
$$

where $(\Sigma^\infty \dashv \Omega^\infty)$ is to be an adjunction universally "localizing" $Ho(Top^{\ast/})$ to $Ho(Spectra)$. 

The notation here is suggestive of the intuition behind how this stabilization will work: The universal way of making a topological space $X$ become stable under suspension is to pass to its infinite suspension in a suitable sense. That suitable sense is going to be called the _[[suspension spectrum]]_ of $X$. Conversely, if an object doesnt's change up to equivalence, by forming its loop spaces, it must give an [[infinite loop space]].

In contrast to the [[classical homotopy category]], the stable homotopy category is a [[triangulated category]] (a shadow of the fact that the [[(∞,1)-category of spectra]] is a [[stable (∞,1)-category]]). As such it may be thought of as a refinement of the [[derived category]] [[category of chain complexes|of chain complexes]] (of [[abelian groups]]): every [[chain complex]] gives rise to a [[spectrum]] and every [[chain map]] to a map between these spectra (the [[stable Dold-Kan correspondence]]), but there are many more spectra and maps between them than arise from chain complexes and chain maps.


There is a variety of different models for the [[stable homotopy theory]] of spectra, some of which roughly fits into a hierarchy like so:

1. [[sequential spectra]] with their [[model structure on sequential spectra]]

1. [[symmetric spectra]] with their [[model structure on symmetric spectra]]

1. [[orthogonal spectra]] with their [[model structure on orthogonal spectra]]

1. [[excisive functors]] with their [[model structure for excisive functors]]

As one moves down this list, the objects modelling the spectra become richer. This means on the one hand that their abstract properties become better as one moves down the list, on the other hand it means that it is more immediate to construct and manipulate examples as one stays further up in the list. 

We start with plain sequential spectra [below](#SequentialSpectra) as a transparent means to see the [[stable homotopy category]]. When we get to the discussion of [[ring spectra]] [eventually](#RingSpectra) with the basic applications in mind, it is convenient to pass to the richer model of [[symmetric spectra]], [further below](#SymmetricSpectra).


### Motivating theorems

But first we now consider some facts in plain ("un-stable") [[algebraic topology]]/[[homotopy theory]] that serve to motivate the passeage to [[stable homotopy theory]] in the first place.


Motivation for stabilization under $(\Sigma \dashv \Omega)$:

* [[Eckmann-Hilton argument]] (...[[May recognition theorem]])

* [[Freudenthal suspension theorem]]

* [[triangulated category]]-structure on [[Spanier-Whitehead category]]

Further motivation which is the subject of the [seminar](#ComplexOrientedCohomology):

* [[generalized cohomology]]

  * [[suspension isomorphism]]

  * [[Brown representability theorem]]

* [[cobordism theory]]

  [[Thom's theorem]]




### **1.1)** Sequential spectra
 {#SequentialSpectraSection}

The most lighweight model for [[spectra]] are _[[sequential spectra]]_. They support most of [[stable homotopy theory]] in a straightforward way, and have the advantage that examples tend to be immediate (for instance the proof of the [[Brown representability theorem]] spits out sequential spectra). 

The key disadvantage of sequential spectra is that they do not support a functorial [[smash product of spectra]] before passing to the [[stable homotopy category]], much less a [[symmetric smash product of spectra]]. This is the structure needed for a decent discussion of the [[higher algebra]] of [[ring spectra]]. To accomodate this, further [below](#SymmetricSpectra) we enhance sequential spectra to the slightly richer model of [[symmetric spectra]]. But both these models are connected by a [[free-forgetful adjunction]] and for workinbg with either model it is useful to pass back and forth.

#### Sequential pre-spectra 

The following def. \ref{SequentialSpectra} is the traditional component-wise definition of [[sequential spectra]], was first stated in ([Lima 58](spectrum#Lima58)) and became widely appreciated with ([Boardman 65](spectrum#Boardman65)).  

> It is generally supposed that [[George Whitehead|G. W. Whitehead]] also had something to do with it, but the latter takes a modest attitude about that. ([Adams 74, p. 131](#Adams74))

Below in prop. \ref{SequentialSpectraAsDiagramSpectra} we discuss an equivalent definition of sequrntial spectra as "topological diagram spectra" ([Mandell-May-Schwede-Shipley 00](#MMSS00)), namely as [[topologically enriched functors]] ([defn.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctor)) on [[n-spheres]], which is useful for establishing the [[stable model category]] structure ([below](#StableModelStructureOnSequentialSpectra)) and for establishing the [[symmetric monoidal smash product of spectra]] (in [1.2](#DiagramSpectra)).

Throughout we say "[[topological space]]" for [[compactly generated topological space]] ([defn.](Introduction+to+Stable+homotopy+theory+--+P#kTop))

+-- {: .num_defn #SequentialSpectra}
###### Definition

A **[[sequential spectrum|sequential]] [[prespectrum]] in [[topological spaces]]**, or just **[[sequential spectrum]]** for short (or even just **[[spectrum]]), is

1. an $\mathbb{N}$-[[graded object|graded]] [[pointed topological space|pointed]] [[compactly generated topological space]]  $X_\bullet = (X_n \in Top_{cg}^{\ast/})_{n \in \mathbb{N}}$ (the **component spaces**); 

1. pointed [[continuous functions]] $\sigma_n \colon S^1 \wedge X_n \to X_{n+1}$ for all $n \in \mathbb{N}$ (the **structure maps**) from the [[smash product]] ([defn.](Introduction+to+Stable+homotopy+theory+--+P#SmashProductOfPointedObjects))  of one component space with the standard [[1-sphere]] to the next component space.

 A [[homomorphism]] $f \colon X \to Y$ of sequential spectra is a sequence $f_\bullet \colon X_\bullet \to Y_\bullet$ of base point-preserving continuous function, such that all [[diagrams]] of the form

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

+-- {: .num_example #SuspensionSpectrum}
###### Example

For $X\in Top^{\ast/_{cg}}$ a [[pointed topological space]], its **[[suspension spectrum]]** $\Sigma^\infty X$ is the [[sequential spectrum]] , def. \ref{SequentialSpectra} with

* $(\Sigma^\infty X)_n \coloneqq S^n \wedge X$;

* $\sigma_n \colon S^1 \wedge S^n \wedge X \overset{\simeq}{\longrightarrow} S^{n+1}X$ the canonical [[homeomorphism]].

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

+-- {: .num_example #SuspensionSpectrum}
###### Example

The [[suspension spectrum]] (example \ref{SuspensionSpectrum}) of the point is the **standard sequential [[sphere spectrum]]** 

$$
  \mathbb{S}_{seq} \coloneqq \Sigma^\infty \ast
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

1. $X \wedge K$ (the **[[smash product|smash]] [[tensoring]]** of $X$ with $K$) is the sequential spectrum with 

   * $(X \wedge K)_n \coloneqq X_n \wedge K$ ([[smash product]] on component spaces ([defn.](Introduction+to+Stable+homotopy+theory+--+P#SmashProductOfPointedObjects)))

   * $\sigma_n^{X \wedge K} \coloneqq \sigma_n^{X} \wedge id_{K}$.

1. $Maps(K,X)_\ast$ (the **[[powering]]** of $K$ into $X$) is the sequential spectrum with

   * $(Maps(K,X)_\ast)_n \coloneqq Maps(K,X_n)_\ast$ (compactly generated [[pointed mapping space]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#CompactlyGeneratedMappingSpaces), [def.](Introduction+to+Stable+homotopy+theory+--+P#PointedMappingSpace)))

   * $\sigma_n^{Maps(K,X)_\ast} \colon S^1 \wedge Maps(K,X_n) \to Maps(K,S^1 \wedge X_n)_\ast \overset{Maps(K,\sigma_n)_\ast}{\longrightarrow} Maps(K,X_{n+1})_\ast$.

These operations canonically extend to [[functors]]

$$
  (-)\wedge (-)
    \;\colon\;
  SeqSpec(Top_{cg}) \times Top^{\ast/}_{cg}
    \longrightarrow
  SeqSpec(Top^{\ast}_{cg})
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


+-- {: .num_prop }
###### Proposition

For any $K \in Top^{\ast/}_{cg}$ the functors of smash tensoring and powering with $K$, from def. \ref{TensoringAndPoweringOfSequentialSpectra}, constitute a pair of [[adjoint functors]]

$$
  SeqSpec(Top_{cg})
    \stackrel{
      \overset{(-) \wedge K}{\longleftarrow}
    }{
      \underoverset{Maps(K,-)_\ast}{\bot}{\longrightarrow}}
  SeqSpec(Top_{cg})
  \,.
$$

=--

+-- {: .proof}
###### Proof

The adjunction

$$
  Top_{cg}^{\ast/}
    \stackrel{\overset{K \wedge (-)}{\longleftarrow}}{\underoverset{Maps(K,-)_\ast}{\bot}{\longrightarrow}}
  Top_{cg}^{\ast/}
$$

(from [this prop.](Introduction+to+Stable+homotopy+theory+--+P#PointedCompactlyGeneratedTopologicalSpacesIsSymmetricMonoidalClosed)) applies componentwise. Since in def. \ref{TensoringAndPoweringOfSequentialSpectra} the structure maps do not interact with the smash product operation, this yields the adjunction in question.

=--

+-- {: .num_example #StandardCylinderSpectrumSequential}
###### Example

For $X \in SeqSpec(Top_{cg})$ a [[sequential spectrum]], def. \ref{SequentialSpectra}, its **standard [[cylinder spectrum]]** is its [[smash product|smash]] [[tensoring]] $X \wedge (I_+)$, def. \ref{TensoringAndPoweringOfSequentialSpectra}, with the standard interval ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopologicalInterval)) with a basepoint freely adjoined ([def.](Introduction+to+Stable+homotopy+theory+--+P#BasePointAdjoined)). The component spaces of the [[cylinder spectrum]] are the standard [[reduced cylinders]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#StandardReducedCyclinderInTop)) of the component spaces of $X$:

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
    \longrightarrow
  X \wedge (I_+)
   \longrightarrow
  X
$$

(where we are using that [[wedge sum]] is the [[coproduct]] in [[pointed topological spaces]] ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#WedgeSumAsCoproduct)).)

=--

+-- {: .num_prop #SigmaInfinityOmegaInfinity}
###### Proposition

The functor $\Sigma^\infty$ that forms [[suspension spectra]] (def. \ref{SuspensionSpectrum}) has a [[right adjoint]] functor $\Omega^\infty$

$$
  (\Sigma^\infty \dashv \Omega^\infty)
  \;\colon\;
  SeqSpec(Top_{cg})
    \stackrel{\overset{\Sigma^\infty}{\longleftarrow}}{\underset{\Omega^{\infty}}{\longrightarrow}}
  Top_{cg}^{\ast/}
  \,,
$$

given by picking the 0-comonent space:

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

##### Suspension and looping

We discuss models for the operation of [[reduced suspension]] and forming [[loop space objects]] of sequential spectra.

+-- {: .num_defn #SequentialSpectrumRealSuspension}
###### Definition

For $X$ a sequential spectrum, then

1. the **standard suspension** of $X$ is $X \wedge S^1$ according to def. \ref{TensoringAndPoweringOfSequentialSpectra};

1. the **standard looping** of $X$ is $Maps(S^1,X)_\ast$ according to def. \ref{TensoringAndPoweringOfSequentialSpectra}.

The standard suspension is equivalently the [[cofiber]] of the canonical inclusion of boundaries into the standard [[cylinder spectrum]]  $X \wedge (I_+)$ of def. \ref{StandardCylinderSpectrumSequential}:

$$
  X \wedge S^1 
    \simeq
  cofib\left(
    X \vee X \to X \wedge (I_+)
  \right)
  \,.
$$

The standard looping is equivalently the [[fiber]] of the canonical projection from the standard path space spectrum $Maps(I_+,X)_\ast$:

$$
  Maps(S^1,X)_\ast 
   \simeq
  fib\left(
    Maps(I_+,X)_\ast \to X \times X
  \right)
  \,.
$$


=--

There are two other models for suspension and looping of spectra, which will turn out to be isomorphic in the stable homotopy category:

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

   1. $(\Sigma X)_n \coloneqq S^1 \wedge X_n$

   1. $\sigma_n^{\Sigma X} \coloneqq S^1 \wedge (\sigma_n)$.

1. the **alternative looping** of $X$ is the sequential spectrum $\Omega X$ with

   1. $(\Omega X)_n \coloneqq Maps(S^1,X_n)_\ast$;

   1. $\tilde \sigma_n^{\Omega X} \coloneqq Maps(S^1,\sigma_n)_\ast$.  

Here $\tilde \Sigma_n$ denotes the $(\Sigma\dashv \Omega)$-[[adjunct]] of $\sigma_n$.

=--

In some references this "alternative suspension" is called the "fake suspension" e.g. ([Jardine 15, section 10.4](sequential+spectrum#Jardine15)).

+-- {: .num_remark #StandardAndAlternativeSuspensionAreNotDirectlyComparable}
###### Remark

There is no direct comparison morphism between the standard suspension (def. \ref{SequentialSpectrumRealSuspension}) and the alternative suspension (def. \ref{SequentialSpectrumFakeSuspension}). This is due to the non-trivial graded commutativity of smash products of spheres (prop. \ref{GradedCommutativityOfSmashOfSpheres}): 

namely a comparison morphism $\Sigma X \longrightarrow X \wedge S^1$ (or alternatively the other way round) would have to make the following diagrams commute:

$$
  \array{
     S^1 \wedge S^1 \wedge X_n &\longrightarrow& S^1 \wedge X_n \wedge S^1
     \\
     {}^{\mathllap{S^1 \wedge \sigma_n}}\downarrow 
       &(nc)& 
     \downarrow^{\mathrlap{\sigma_n \wedge S^1}}
     \\
     S^1 \wedge X_{n-1} &\longrightarrow& X_{n-1} \wedge S^1
  }
$$

Clearly the only way to go about achieving this is to have the horizontal morphisms be the [[braiding]] homomorphisms of the [[smash product]]. To see this more clearly, consider labeling the two copies of the circle appearing here as $S^1_a$ and $S^1_b$. Then the diagram we are dealing with looks like this:

$$
  \array{
     S_a^1 \wedge S_b^1 \wedge X_n &\longrightarrow& S_b^1 \wedge X_n \wedge S_a^1
     \\
     {}^{\mathllap{S^1_a \wedge \sigma_n}}\downarrow 
       &(nc)& 
     \downarrow^{\mathrlap{\sigma_n \wedge S^1_a}}
     \\
     S_a^1 \wedge X_{n-1} &\longrightarrow& X_{n-1} \wedge S_a^1
  }
$$

This makes it manifest that as $S^1_a$ passes along the top and right, it has to be braided past $S^1_b$, while this does not occur as $S^1_a$ passes down and left. Since the braiding $S^1_a \wedge S^1_b \to S^1_b \wedge S^1_a$ is nontrivial (the homotopy class of this map differs from the identity by a minus sign in $\p_2(S^2) = \mathbb{Z}$), there is no way to make this diagram commute.

=--

+-- {: .num_defn #ShiftingCommutesWithLoopingAndSuspensionOfSequentialSpectra}
###### Remark

The looping and suspension operations in def. \ref{SequentialSpectrumRealSuspension} and def. \ref{SequentialSpectrumFakeSuspension} commute with shifting, def. \ref{ShiftedSpectrum}. Therefore in expressions like $\Sigma (X[1])$ etc. we may omit the parenthesis.

=--

+-- {: .num_prop #AdjunctionsBetweenLoopingAndDeloopingForSeqSpec}
###### Proposition

The constructions from def. \ref{ShiftedSpectrum}, def. \ref{SequentialSpectrumRealSuspension} and def. \ref{SequentialSpectrumFakeSuspension} form pairs of [[adjoint functors]] $SeqSpec \to SeqSpec$ like so:

1. $(-)[1] \;\dashv\; (-)[-1] \;\dashv\; (-)[1] \;\dashv\; \cdots $;

1. $(-)\wedge S^1 \dashv (-)^{S^1}$;

1. $\Sigma \dashv \Omega$.

=--

+-- {: .proof}
###### Proof

The first is immediate from the definition. 

The second is just degreewise the adjunction [[smash product]]$\dashv$[[pointed mapping space]] (discussed [here](pointed+object#ClosedMonoidalStructure)), since by definition the smash product and mapping spaces here do not interact non-trivially with the structure maps.

The third follows by applying the [[smash product]]$\dashv$[[pointed mapping space]]-adjunction isomorphism twice, like so:

Morphisms $f\colon \Sigma X \to Y$ are in components given by commuting diagrams of this form:

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

Applying the adjunction isomorphism diagonally gives a bijection to diagrams of this form:

$$
  \array{
   S^1 \wedge X_n &\overset{f_n}{\longrightarrow}& Y_n
   \\
   {}^{\mathllap{\sigma^X_n}}\downarrow && \downarrow^{\mathrlap{\tilde \sigma^Y_n}}
   \\
   X_{n+1} &\underset{\tilde f_{n+1}}{\longrightarrow}& Maps(S^1,Y_{n+1})_\ast
  }
  \,.
$$

Then applying the same isomorphism diagonally once more gives a further bijection to  commuting diagrams of this form:

$$
  \array{
    X_n &\overset{\tilde f_n}{\longrightarrow}& Maps(S^1,Y_n)_\ast
    \\
    {}^{\mathllap{\tilde \sigma_n}}\downarrow 
      && 
    \downarrow^{\mathrlap{Maps(S^1,\tilde \sigma^Y_n)_\ast}}
    \\
    Maps(S^1, X_{n+1})_\ast
      &\underset{(\tilde f_n)^{S^1}}{\longrightarrow}&
    Maps\left(S^1, Maps(S^1,Y_{n+1})_\ast\right)_\ast
  }
  \,.
$$

This finally equivalently exhibits morphisms of the form

$$
  X \longrightarrow \Omega Y
  \,.
$$

=--


##### As topological diagrams

The following is an equivalent reformulation of the component-wise definition of sequential spectra, def. \ref{SequentialSpectra}, as [[topologically enriched functors]] ([defn. ](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctor)). 


+-- {: .num_defn #CategoriesOfStandardSpheres}
###### Definition

Write 

$$
  \iota \;\colon\; StdSpheres \longrightarrow Top_{cg}^{\ast/}
$$

for the non-full [[topologically enriched category|topologically enriched]] [[subcategory]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopEnrichedCategory)) of that of [[pointed topological spaces|pointed]] [[compactly generated topological spaces]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopkAsATopologicallyEnrichedCategory)):

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

* [[composition]] is induced from compistion in $Top^{\ast/}_{cg}$ by regarding the [[hom-space]] $S^k$ above as its [[image]] in $Maps({S^n},S^{k+n})_\ast$ under the [[adjunct]]

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
  [StdSpheres,Top_{cg}^{\ast/}]
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




#### The strict model structure on sequential spectra

The [[model category]] structure on [[sequential spectra]] which [[presentable (infinity,1)-category|presents]] [[stable homotopy theory]] is the "stable model structure" discussed [below](#TheStableModelStructure). Its fibrant-cofibrant objects are (in particular) [[Omega-spectra]], hence are the proper [[spectrum objects]] among the pre-spectrum objects.

But for technical purposes it is useful to also be able to speak of a model structure on pre-spectra, which sees their homotopy theory as sequences of simplicial sets equipped with suspension maps, but not their stable structure. This is called the "strict model structure" for sequential spectra. Its main point is that the stable model structure of interest arises from it via [[Bousfield localization of model categories|left Bousfield localization]].


+-- {: .num_defn #ClassesOfMorphismsOfTheStrictModelStructureOnSequentialSpectra}
###### Definition

Say that a homomorphism $f_\bullet \colon X_\bullet \to Y_\bullet$ in the category $SeqSpec(Top)$, def. \ref{SequentialSpectra} is

* a **strict weak equivalence** if each component $f_n \colon X_n \to Y_n$ is a weak equivalence in the [[classical model structure on topological spaces]] (hence a [[weak homotopy equivalence]]);

* a **strict fibration** if each component $f_n \colon X_n \to Y_n$ is a fibration in the [[classical model structure on topological spaces]] (hence a [[Serre fibration]]);

* a **strict cofibration** if the maps $f_0\colon X_0 \to Y_0$ as well as all [[pushout products]] of $f_n$ with the structure maps of $X$

  $$
    X_{n+1}\underset{S^1 \wedge X_n}{\coprod} S^1 \wedge Y_n
    \longrightarrow
    Y_{n+1}
  $$

  are cofibrations in the  [[classical model structure on topological spaces]] (i.e.: [[retracts]] of [[relative cell complexes]]);

=--

Recall the sets

$$
  I_{Top^{\ast/}} \coloneqq \{S^{n-1}_+ \overset{(\iota_n)_+}{\longrightarrow} D^n_+\}_{n \in \mathbb{N}}
$$

$$
  J_{Top^{\ast/}} \coloneqq \{D^n \overset{(id,\delta_0)_+}{\longrightarrow} D^n \times I\}_{n \in \mathbb{N}}
$$

of standard generating cofibrations and generating acyclic cofibrations, respectively, of the [[classical model structure on pointed topological spaces]].


+-- {: .num_defn #GeneratingAndGeneratingAcyclicCofibrationsForSeqSpecStrict}
###### Definition

Write

$$
  I_{SeqSpec}^{stric} 
    \coloneqq 
  \left\{ 
    y(S^n) \cdot i_+ 
  \right\}_{{S^n \in StdSpheres} \atop {i_+ \in I_{Top^{\ast/}}}}
  \;\;
  \in [StdSpheres, Top^{\ast/}] \simeq SeqSpec(Top)
$$

and

$$
  J_{SeqSpec}^{strict}
    \coloneqq 
  \left\{ 
    y(S^n) \otimes j_+ 
  \right\}_{{ S^n \in StdSpheres} \atop {j_+ \in J_{Top^{\ast/}}}}
  \;\;
  \in [StdSpheres, Top^{\ast/}] \simeq SeqSpec(Top)
  \,,
$$

for the set of morphisms arising as the [[tensoring]] of a [[representable functor|representable]] with a generating acyclic cofibration of the [[classical model structure on pointed topological spaces]].

=--



+-- {: .num_theorem #StrictModelStructureOnSequentialPrespectraIsModelCategory}
###### Theorem

The classes of morphisms in def. \ref{ClassesOfMorphismsOfTheStrictModelStructureOnSequentialSpectra} give the structure of a [[model category]] $SeqSpec(Top)_{strict}$, called the **strict model structure** on sequential spectra.

This is a [[cofibrantly generated model category]] with generating (acyclic) cofibrations the set $I_{SeqSpec}^{strict}$ (resp. $J_{SeqSpec}^{strict}$) from def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForSeqSpecStrict}.

=--



+-- {: .proof}
###### Proof

Prop. \ref{SequentialSpectraAsDiagramSpectra} says that the category of sequential spectra is [[equivalence of categories|equivalently]] an  [[enriched functor category]]

$$
  SeqSpec(Top)
  \simeq
  [StdSpheres, Top_{cg}^{\ast}]
  \,.
$$

Accordingly, this carries the [[projective model structure on enriched functors]], and unwinding the definitions, this gives the statement for the fibrations and the weak equivalences.

It only remains to check that the cofibrations are as claimed. To that end, consider a [[commuting square]] of sequential spectra

$$
  \array{
    X_\bullet &\stackrel{h_\bullet}{\longrightarrow}& A_\bullet
    \\
    \downarrow^{\mathrlap{f_\bullet}} && \downarrow
    \\
    Y_\bullet &\longrightarrow& B_\bullet
  }
  \,.
$$

By definition, this is equivalently a $\mathbb{N}$-collection of commuting diagrams of simplicial sets of the form

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
    X_n &\stackrel{\sigma_n^X}{\longrightarrow}& X_{n+1}
    \\
    \downarrow^{\mathrlap{f_n}} && \downarrow^{\mathrlap{f_{n+1}}}
    \\
    Y_n &\stackrel{\sigma_n^Y}{\longrightarrow}& Y_{n+1}
    \\
    & \searrow && \searrow
    \\
    && B_n &\stackrel{\sigma_n^B}{\longrightarrow}& B_{n+1}
  }
  \;\;\;
  \Rightarrow
  \;\;\;
  \array{
    X_n &\stackrel{\sigma_n^X}{\longrightarrow}& X_{n+1}
    \\
    & \searrow^{\mathrlap{h_n}} && \searrow^{\mathrlap{h_{n+1}}}
    \\
    && A_n &\stackrel{\sigma_n^A}{\longrightarrow}& A_{n+1}
    \\
    && \downarrow && \downarrow
    \\
    && B_n &\stackrel{\sigma_n^B}{\longrightarrow}& B_{n+1}
  }
  \,.
$$

Hence a [[lifting]] in the original diagram is a lifting in each degree $n$, such that the lifting in degree $n+1$ makes these diagrams of structure maps commute.

Since components are parameterized over $\mathbb{N}$, this condition has solutions by [[induction]]. First of all there must be an ordinary lifting in degree 0. Then assume a lifting $l_n$ in degree $n$ has been found

$$
  \array{
    X_n &\stackrel{h_n}{\longrightarrow}& A_n
    \\
    \downarrow^{\mathrlap{f_n}} &\nearrow_{\mathrlap{l_n}}& \downarrow
    \\
    Y_n &\longrightarrow& B_n
  }
$$

the lifting $l_{n+1}$ in the next degree has to also make the following diagram commute

$$
  \array{
    X_n &\stackrel{\sigma_n^X}{\longrightarrow}& X_{n+1}
    \\
    \downarrow^{\mathrlap{f_n}} && \downarrow^{\mathrlap{h_{n+1}}}
    & \searrow 
    \\
    Y_n &\stackrel{\sigma_n^Y}{\longrightarrow}& Y_{n+1}
    && 
    \\
    & \searrow^{\mathrlap{l_n}} && \searrow^{\mathrlap{l_{n+1}}} & \downarrow
    \\
    && A_n &\stackrel{\sigma_n^A}{\longrightarrow}& A_{n+1}
  }
  \,.
$$

This is a [[cocone]] under the the commuting square for the structure maps, and therefore the outer diagram is equivalently a morphism out of the [[domain]] of the [[pushout product]] $f_n \Box \sigma_n^X$, while the compatible lift $l_{n+1}$ is equivalently a lift against this pushout product:

$$
  \array{
    Y_n \underset{X_n}{\sqcup} X_{n+1}
    &\stackrel{(\sigma_n^A l_n,h_{n+1})}{\longrightarrow}&
    A_{n+1}
    \\
    \downarrow &{}^{\mathllap{l_{n+1}}}\nearrow& \downarrow
    \\
    Y_{n+1} &\stackrel{}{\longrightarrow}& B_{n+1}
  }
  \,.
$$


=--

+-- {: .num_defn #CWSpectrum}
###### Definition

A **CW-spectrum** is a [[sequential spectrum]] $X_\bullet\in SeqSpec(Top)$, def. \ref{SequentialSpectra}, such that

1. all component spaces $X_n$ are [[CW-complexes]], 

1. all structure maps $\Sigma X_n \longrightarrow X_{n+1}$ are inclusions of subcomplexes 

=--



+-- {: .num_prop #CellSpectraAreCofibrantInModelStructureOnTopologicalSequentialSpectra}
###### Proposition

A [[sequential spectrum]] $X\in SeqSpec(Top)_{strict}$ is cofibrant in particular if all component spaces are [[cell complexes]] and all its structure morphisms $S^1 \wedge X_n \to X_{n+1}$ are [[relative cell complexes]]. In particular [[CW-spectra]], def. \ref{CWSpectrum} are cofibrant in $SeqSpec(Top)_{strict}$.

=--

+-- {: .proof}
###### Proof

A morphism $\ast \to X$ is a cofibration according to def. \ref{ClassesOfMorphismsOfTheStrictModelStructureOnSequentialSpectra} if 

1. $X_0$ is cofibrant, hence a retract of a [[cell complex]];

1. $$
     \ast_{n+1}\underset{S^1 \wedge \ast_n}{\coprod} S^1 \wedge X_n
     \longrightarrow
     X_{n+1}
   $$

   is a cofibration. But in this case the [[pushout]] reduces to just its second summand, and so this is now equivalent to

   $$
     S^1 \wedge X_n \longrightarrow X_{n+1}
   $$

   being cofibrations; hence [[retracts]] of [[relative cell complexes]].

=--

+-- {: .num_prop #CylinderSpectrumOverCWSpectrumIsGood}
###### Proposition

For $X\in SeqSpec(Top)_{stable}$ a [[CW-spectrum]], def. \ref{CWSpectrum}, then its standard [[cylinder spectrum]] $X \wedge (I_+)$ of def. \ref{StandardCylinderSpectrumSequential} satisfies the conditions on an abstract [[cylinder object]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#PathAndCylinderObjectsInAModelCategory)) in that the inclusion

$$
  X \vee X \longrightarrow X \wedge (I_+)
$$

is a cofibration in $SeqSpec(Top)_{stable}$.

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
  X_{n+1} \wedge I_+
  \,.
$$

Now by the assumption that $X$ is a [[CW-spectrum]], each $X_{n}$ is a CW-complex, and this implies that $X_n \wedge (I_+)$ is a relative cell complex in $Top^{\ast/}$. With this, inspection shows that also the above morphism is a relative cell complex.

=--


#### Omega-spectra

+-- {: .num_defn #StableHomotopyGroups}
###### Definition

The [[stable homotopy groups]] of a [[sequential spectrum]] $X$, def. \ref{SequentialSpectra}, is the $\mathbb{Z}$-[[graded abelian groups]] given by the [[colimit]] of [[homotopy groups]] of the component spaces

$$
  \pi_\bullet(X)
  \coloneqq
  \underset{\longrightarrow}{\lim}_k
  \pi_{\bullet+k}(X_n)
  \,.
$$

This constitutes a [[functor]]

$$
  \pi_\bullet \;\colon\; SeqSpec(Top) \longrightarrow Ab^{\mathbb{Z}}
  \,.
$$

=--

+-- {: .num_defn #StableWeakEquivalenceOfSequentialTopologicalSpectra}
###### Definition

A morphism $f \colon X \longrightarrow Y$ of [[sequential spectra]], def. \ref{SequentialSpectra}, is called a [[stable weak homotopy equivalence]], if its image under the [[stable homotopy group]]-functor of def. \ref{StableHomotopyGroups} is an [[isomorphism]]

$$
  \pi_\bullet(f) \;\colon\; \pi_\bullet(X) \longrightarrow \pi_\bullet(Y)
  \,.
$$

=--


+-- {: .num_defn #OmegaSpectrum}
###### Definition

An **[[Omega-spectrum]]** is a [[sequential spectrum]] $X$ of topological spaces, def. \ref{SequentialSpectra}, such that the ([[smash product]] $\dashv$ [[pointed mapping space]])-[[adjuncts]] $\tilde \sigma_n$ of the structure maps $\sigma_n \colon \Sigma X_n \to X_{n+1}$ of $X$ are [[weak homotopy equivalences]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#WeakHomotopyEquivalenceOfTopologicalSpaces)), hence classical weak equivalences ([def.](Introduction+to+Stable+homotopy+theory+--+P#ClassesOfMorhismsInTopQuillen)):

$$
  \tilde \sigma_n
  \;\colon\;
  X_n  \stackrel{\in W_{cl}}{\longrightarrow}  X_{n+1}^{S^1}
$$

for all $n \in \mathbb{N}$.

=--

+-- {: .num_remark #StableHomotopyGroupsOfOmegaSpectrum}
###### Remark

If a [[sequential spectrum]] $X$ is an [[Omega-spectrum]], def. \ref{OmegaSpectrum}, 
then its colimiting [[stable homotopy groups]], def. \ref{StableHomotopyGroups}, are attained as the actual homotopy groups of its components:

$$
  \pi_k(X) \simeq 
  \simeq
  \left\{
    \array{
      \pi_k X_0  & if\; k \geq 0
      \\
      \pi_0 X_k  & if \; k \lt 0
    }
  \right.
  \,.
$$

=--



+-- {: .num_defn #Spectrification}
###### Definition

The canonical _$\Omega$-[[spectrification]]_ $Q X$ of a  [[CW-spectrum]] $X$, def. \ref{CWSpectrum}, is the operation of forming degreewise the [[colimit]] of higher [[loop space objects]] $\Omega(-)\coloneqq (-)^{S^1}$

$$
  (Q X)_n
  \coloneqq
  \underset{\longrightarrow}{\lim}_{k }
  \Omega^k X_{n+k}
  \,,
$$

where $Sing$ denotes the [[singular simplicial complex]] functor.

=--






#### The stable model structure on sequential spectra
 {#StableModelStructureOnSequentialSpectra}


In order to do [[stable homotopy theory]] with [[sequential spectra]], we need to equip the [[category]] of sequential [[pre-spectra]] of def. \ref{SequentialSpectra} with a [[model category]] structure whose weak equivalences are the [[stable weak homotopy equivalences]] of def. \ref{StableWeakEquivalenceOfSequentialTopologicalSpectra}. This class contains the degreewise weak homotopy equivalences of the strict model structure of def. \ref{ClassesOfMorphismsOfTheStrictModelStructureOnSequentialSpectra} but is strictly larger. There are then different choices for the fibrations and cofibrations, but it is particularly convenient to keep the cofibrations those of the strict model structure, for then we are in the situation of [[Bousfield localization of model categories]]:

+-- {: .num_defn #BousfieldLocalizationOfModelCategories}
###### Definition


A _left [[Bousfield localization of model categories|Bousfield localization]]_ $C_{loc}$ of a [[model category]] $C$ is another model category structure on the same underlying category with the same cofibrations, 

$$
  cof_{C_{loc}} = cof_c
$$

but more weak equivalences

$$
  W_{C_{loc}} \supset W_C
  \,.
$$

=--

While that's a very simple definition, it turns out that something interesting happens to the fibrations when we keep the cofibrations fixed and increase the weak equivalences.

+-- {: .num_remark }
###### Remark 

In def. \ref{BousfieldLocalizationOfModelCategories} it follows directly that 

* $C_{loc}$ has as fibrations a subset of fibrations of $C$

  $$
    fib_{C_{loc}} = rlp(cof_{C_{loc}} \cap W_{C_{loc}})
    \subset rlp(cof_{C_{loc}} \cap W_C) = fib_{C}
    \,.
  $$

* $C_{loc}$ has the same acyclic fibrations as $C$

  $$
    fib_{C_{loc}} \cap W_{C_{loc}}
    =
    rlp(cof_{C_{loc}}) = rlp(cof_C) = fib_C \cap W_C
    \,.
  $$

* on the underlying categories

  * the identity functor $Id : C \to C_{loc}$ preserves cofibrations and weak equivalences

  * the identity functor $Id : C_{loc} \to C$ preserves fibrations and acyclic fibrations

  so that this pair of functors is a [[Quillen adjunction]]

  $$
    C_{loc} \stackrel{\leftarrow}{\to} C
    \,,
  $$

The category $C^\circ$ _modeled_ by a model category $C$ is its [[full subcategory]] on fibrant-cofibrant objects. Under left Bousfield localization the fibrant-cofibrant objects of $C_{loc}$ are a subcollection of those of $C$, so that we have the full subcategory

$$
  (C_{loc})^\circ \subset C^\circ
  \,.
$$

Moreover, as we shall see, every object in $C$ is weakly equivalent in $C_{loc}$ to one in $C_{loc}$: it _reflects into $C_{loc}$_ .

Hence Bousfield localization is a model category version of reflecting onto a [[reflective subcategory]].

=--

We now apply to this localize $SeqSpec(Top)_{strict}$ at "stable weak equivalences" such as to make the fibrant objects become precisely the [[Omega-spectra]].

+-- {: .num_defn #ClassesOfMorphismsOfTheStableModelStructureOnSequentialSpectra}
###### Definition

Say that a homomorphism $f_\bullet \colon X_\bullet \to Y_\bullet$ in the category $SeqSpec(Top)$, def. \ref{SequentialSpectra} is

* a **stable weak equivalence** if for all [[Omega-spectra]] $X$ the morphism $[f,E]_{strict}$ is a [[bijection]] (where $[-,E]_{strict}$ is the [[hom-functor]] of the [[homotopy category of a model category|homotopy category]] of the strict model structure of theorem \ref{StrictModelStructureOnSequentialPrespectraIsModelCategory}.

* a **stable cofibration** if the simplicial maps $f_0\colon X_0 \to Y_0$ as well as all [[pushout products]] of $f_n$ with the structure maps of $X$

  $$
    X_{n+1}\underset{S^1 \wedge X_n}{\coprod} S^1 \wedge Y_n
    \longrightarrow
    Y_{n+1}
  $$

  are cofibrations in the [[classical model structure on topological spaces]] (i.e.: [[retracts]] of [[relative cell complexes]]).

=--

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
   \sqcup
  \{
    k_n \Box i_+
  \}_{{n \in \mathbb{N}} \atop {i_+ \in I_{Top^{\ast/}}}}
$$

for the [[disjoint union]] of the other set of morphisms appearing in def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForSeqSpecStrict} with the set of [[pushout-products]] (under [[tensoring]]) of the morphisms $k_n$ from def. \ref{FreeSequentialSpectra} with the generating cofibrations of the [[classical model structure on pointed topological spaces]].

=--


+-- {: .num_theorem #StableModelStructureOnSequentialSpectraIsModelCategory}
###### Theorem

The classes of morphisms in def. \ref{ClassesOfMorphismsOfTheStableModelStructureOnSequentialSpectra} give the structure of a [[model category]] $SeqSpec(Top)_{stable}$, called the **stable [[model structure on topological sequential spectra]]**.

Its fibrant objects are precisely the [[Omega-spectra]], def. \ref{OmegaSpectrum}.

Moreover, this is a [[cofibrantly generated model category]] with generating (acyclic) cofibrations the sets $I_{SeqSpec}^{stable}$ (and $J_{SeqSpec}^{stable}$) from def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForSeqSpecStable}.

=--

This model structure is mentioned without proof in ([Bousfield-Friedlander 78](#BousfieldFriedlander78)). A full proof appears, generalized to a unified proof of model structures in [[highly structured spectra]] in ([Mandell-May-Schwede-Shipley 01](#MMSS00)), which we follow here. We spell out the proof [below](#ProofOfTheStableModelStructureOnSequentialSpectra), after a few lemmas.

+-- {: .num_lemma #CorepresentationOfAdjunctStructureMaps}
###### Lemma

The morphisms of [[free spectra]] $\{k_n\}_{n \in \mathbb{N}}$ from def. \ref{FreeSequentialSpectra} co-represent the adjunct structure maps of sequential spectra:

for $X \in SeqSpec(Top)$, then 

$$
  \array{
    [F_n S^0, X] &\simeq& X_n
    \\
    {}^{\mathllap{[k_n,X]}}\downarrow && \downarrow^{\mathrlap{\tilde \sigma_n^X}}
    \\
    [F_{n+1}S^1, X] &\simeq& \Omega X_{n+1}
  }
  \,.
$$

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

But that $(n+1)$st component is just the component that similarly determines the precompositon of $f$ with $k_n$, hence $f\circ k_n$ is uniquely determined by the map $\sigma_n^X \circ \Sigma f$. Therefore $[k_n,-]$ is the function

$$
  [k_n,-]
   \;\colon\;
  X_n 
  = 
  [S^0, X_n]
    \stackrel{f \mapsto \sigma_n^X \circ \Sigma f}{\longrightarrow}
  \Maps(S^1, X_{n+1})
  =
  \Omega X_{n+1}
  \,.
$$

It remains to see that this is indeed the $(\Sigma \dashv \Omega)$-[[adjunct]] of $\sigma_n^X$. By the general formula for adjuncts, this is

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

To identify this as a map $S^1 \to X_{n+1}$ we use the adjunction isomorphism once more to throw all the $\Omega$-s on the right back to $\Sigma$-s the left, to finally find that this is indeed

$$
  \sigma_n^X \circ \Sigma f
    \;\colon\;
  S^1 = \Sigma S^0 \stackrel{\Sigma f}{\longrightarrow} \Sigma X_n \stackrel{\sigma_n^X}{\longrightarrow} X_{n+1}
  \,.
$$

=--


+-- {: .num_lemma #StableEquivalencesBetweenOmegaSpectraAreStrictWeakEquivalences}
###### Lemma

1. Every weak equivalence with respect to the strict model structure is a stable weak equivalence.

1. Every stable weak equivalence between [[Omega-spectra]] is a weak equivalence in the strict model structure.

=--

+-- {: .proof}
###### Proof

The first statement follows directly from  the definition of stable weak equivalences, since weak equivalences become isomorphisms in the [[homotopy category of a model category|homotopy category]].

For the second statement, let $f \colon X \to Y$ be a stable weak equivalence between [[Omega-spectra]]. Then by definition, in particular

$$
  [f,X]_{strict} \;\colon\; [Y,X]_{strict} \longrightarrow [X,X]_{strict}
$$

is a [[bijection]]. Therefore the pre-image of $[id_X] \in [X,X]_{strict}$ is an inverse to $f$ in the [[homotopy category]] of the strict model structure. Hence $f$ represents an isomorphism in the strict homotopy category and is hence a weak equivalence in the strict model structure.

=--


+-- {: .num_lemma #ElementsOfKAreStableEquivalencesAndStrictCofibrations}
###### Lemma

Every element in $J_{SeqSpec}^{stable}$ (def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForSeqSpecStable}) is both:

1. a cofibration with respect to the strict model structure of theorem \ref{StrictModelStructureOnSequentialPrespectraIsModelCategory};

1. a stable equivalence (def. \ref{ClassesOfMorphismsOfTheStableModelStructureOnSequentialSpectra}).

=--

+-- {: .proof}
###### Proof 

For the elements in $J_{SeqSpec}^{strict}$ this is part of theorem \ref{StrictModelStructureOnSequentialPrespectraIsModelCategory}.
To see that the $k_n \Box i_+$ are strict cofibrations: By [[Joyal-Tierney calculus]] $k_n \Box i_+$ has left lifting against any acyclic strict fibration $f$ precisely if $k_n$ has left lifting against $f^{i_+}$. By $SeqSpec(Top)_{strict}$ being a $Top_{Quillen}$-[[enriched model category]] the latter is still a strict acyclic fibration. Since $k_n$ is evidently a strict cofibration, the lifting follows and hence also $k_n \Box i_+$ is a strict cofibration.


To see that they are stable equivalences: The morphisms $k_n$ by construction, by [[two-out-of-three]] and by lemma \ref{CorepresentationOfAdjunctStructureMaps} are stable equivalences. Hence the [[derived hom-space]] out of $k_n \Box i_+$ is the homotopy pullback of a weak equivalence, hence is a weak equivalence, hence on the homotopy category an iso.

=--


The point of the set $\{k_n \Box i_+\}$ is to make the following true:

+-- {: .num_lemma #KInjectivesAreAcyclicCofibrations}
###### Lemma

A morphism $f \colon X \to Y$ in $SeqSpec(Top)$ is a $J_{SeqSpec}^{stable}$-[[injective morphism]] precisely if 

1. it is fibration in the strict model structure (hence degreewise a fibration)

1. for all $n \in \mathbb{N}$ the [[commuting squares]] of structure map compatibility on the underlying [[sequential spectra]] 

   $$
     \array{
       X_n  &\overset{\tilde\sigma}{\longrightarrow}& \Omega X_{n+1}
       \\
       \downarrow && \downarrow
       \\
       Y_n &\underset{\tilde \sigma}{\longrightarrow}& \Omega Y_{n+1}
     }
   $$

   exhibit [[homotopy pullbacks]].  


In particular, the $J_{SeqSpec}^{stable}$-[[injective objects]] are precisely the [[Omega-spectra]], def. \ref{OmegaSpectrum}.


=--

+-- {: .proof}
###### Proof

By theorem \ref{StrictModelStructureOnSequentialPrespectraIsModelCategory}, lifting against $J_{SeqSpec}^{stric}$ alone characterizes strict fibrations, hence degreewise fibrations. Lifting against the remaining [[pushout product]] morphism $k_n \Box i_+$ is, by [[Joyal-Tierney calculus]], equivalent to left lifting $i_+$ against the dual pullback product of $f^{k_n}$, which means that $f^{k_n}$ is a weak homotopy equivalence. But by lemma \ref{CorepresentationOfAdjunctStructureMaps}, $f^{k_n}$ is the comparison morphism into the homotopy pullback under consideration. 

=--


+-- {: .num_lemma #KInjectiveStableEquivalencesAreStrictEquivalences}
###### Lemma

A morphism in $SeqSpec(Top)$ which is both 

1. a stable weeak equivalence;

1. a $J_{SeqSpec}^{stable}$-[[injective morphism]] 

is an acyclic fibration in the strict model structure, hence is degreewise a [[weak homotopy equivalence]] and [[Serre fibration]] of topological spaces;

=--


+-- {: .proof}
###### Proof

Let $f\colon E \to B$ be both a stable equivalence as well as a $J_{SeqSpec}^{stable}$-injective morphism. Since $J_{SeqSpec}^{stable}$ contains the generating acyclic cofibrations for the strict model structure, $f$ is in particular a strict fibration, hence a degreewise fibration. Therefore the [[fiber]] $F$ of $f$ is its [[homotopy fiber]] in the strict model structure. This implies that for any $E$ that with $[f,E]_{strict}$ a bijection, by assumption also $[\ast,E]_{strict} \to [F,E]_{strict}$ is a bijection, hence that $F\to \ast$ is also a stable weak equivalence. 

Observe also that $F$, being the pullback of a $J_{SeqSpec}^{stable}$-injective morphisms (by the standard [closure properties](injective+or+projective+morphism#ClosureProperties)) is a $J_{SeqSpec}^{stable}$-[[injective object]], so that by lemma \ref{KInjectivesAreAcyclicCofibrations} $F$ is an [[Omega-spectrum]]. Together this implies with lemma \ref{StableEquivalencesBetweenOmegaSpectraAreStrictWeakEquivalences} that $F \to \ast$ is a weak equivalence in the strict model structure, hence degreewise a [[weak homotopy equivalence]]. From this the [[long exact sequence of homotopy groups]] implies that $\pi_{\bullet \geq 1}(f_n)$ is a [[weak homotopy equivalence]] for all $n$ and for each homotopy group in positive degree. 

To infer from this the remaining case that also $\pi_0(f_0)$ is an isomorphism, observe that, by assumption of $J_{SeqSpec}^{stable}$-injectivity, lemma \ref{KInjectivesAreAcyclicCofibrations} gives that $f_n$ is a homotopy pullback (in pointed topological spaces) of $\Omega (f_{n+1})$. But, by the above, $\Omega (f_{n+1})$ is a weak homotopy equivalence, since $\pi_\bullet(\Omega(-)) = \pi_{\bullet+1}(-)$. Therefore $f_n$ is the homotopy pullback of a weak homotopy equivalence and hence itself a weak homotopy equivalence.

=--

+-- {: .num_lemma #RetractsOfRelativeKCellComplexesAreTheStableEquivalencesAndStrictCofibrations}
###### Lemma

The [[retracts]] of $J_{SeqSpec}^{stable}$-[[relative cell complexes]] are precisely the morphisms which are

1. stable equivalences, 

1. as well as strict cofibrations.

=--


+-- {: .proof}
###### Proof

Since all elements of $J_{SeqSpec}^{stable}$ are stable equivalences and strict cofibrations by lemma \ref{ElementsOfKAreStableEquivalencesAndStrictCofibrations}, it follows that every retract of relative $J_{SeqSpec}^{stable}$-cell complex has the same property.

In the other direction, if $f$ is a stable equivalence and strict cofibration, by the [[small object argument]] it factors $f \colon \stackrel{i}{\to}\stackrel{p}{\to}$ as a relative $J_{SeqSpec}^{stable}$-cell complex $i$ followed by a $J_{SeqSpec}^{stable}$-[[injective morphism]] $p$. By the previous statement $i$ is a stable equivalence, and so by assumption and by [[two-out-of-three]] so is $p$. Therefore lemma \ref{KInjectiveStableEquivalencesAreStrictEquivalences} implies that $p$ is a strict acyclic fibration. But then the assumption that $f$ is a strict cofibration mean that it has the [[left lifting property]] against $p$, and so the [[retract argument]] implies that $f$ is a retract of the relative $K$-cell complex $i$.


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

1. a stable weak equivalence 

1. [[injective morphism|injective]] with respect to the cofibrations of the strict model structure that are also stable equivalences;

precisely if it is an acylic fibration in the strict model structure.

=--


+-- {: .proof}
###### Proof

Every acyclic fibration in the strict model structure in injective with respect to strict cofibrations by the strict model structure; and it is a stable equivalence by item 1 of lemma \ref{StableEquivalencesBetweenOmegaSpectraAreStrictWeakEquivalences}.

Conversely, a morphism injective with respect to strict cofibrations that are stable equivalences is a $K$-[[injective morphism]] by corollary \ref{KInjectivesAreIndeedTheStableFibrations}, and hence if it is also a stable equivalence then by lemma \ref{KInjectiveStableEquivalencesAreStrictEquivalences} it is a strict acylic fibration.

=--

+-- {: .proof #StableModelStructureOnDiagramSpectraProof}
###### Proof
(of theorem \ref{StableModelStructureOnSequentialSpectraIsModelCategory})

The non-trivial points to check are the two [[weak factorization systems]].

That $(Cof_{stable}\cap W_{stable} \;,\; Fib_{stable})$ is a weak factorization system follows from lemma \ref{RetractsOfRelativeKCellComplexesAreTheStableEquivalencesAndStrictCofibrations} and the [[small object argument]]. 

By lemma \ref{StableAcyclicFibrationsAreEquivalentlyStrictAcyclicFibrations} the stable acyclic fibrations are equivalently the strict acyclic fibrations and hence the weak factorization system $(Cof_{stable} \;,\; Fib_{stable} \cap W_{stable})$ is identified with that of the strict model structure $(Cof_{strict} \;,\; Fib_{strict} \cap W_{strict})$.

=--



##### Stability

We discuss that the stable model structure $SeqSpec(Top)_{stable}$ of theorem \ref{StableModelStructureOnSequentialSpectraIsModelCategory} is indeed a [[stable model category]] in that the canonical [[reduced suspension]] operation induced an [[equivalence of categories]] from the [[stable homotopy category]] to itself.

+-- {: .num_defn #StableModelCategory}
###### Definition

A [[pointed category|pointed]] [[model category]] $\mathcal{C}$ is called a **[[stable model category]]** if the canonically induced [[reduced suspension]] and [[loop space object]]-[[functors]] ([prop. ](Introduction+to+Stable+homotopy+theory+--+P#LoopingAsFunctorOnHomotopyCategory)) on its [[homotopy category]] ([defn.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyCategoryOfAModelCategory))is an [[equivalence of categories]]

$$
  (\Sigma \dashv \Omega)
  \;\colon\;
  Ho(\mathcal{C})
   \stackrel{\overset{\Sigma}{\longleftarrow}}{\underoverset{\Omega}{\simeq}{\longrightarrow}}
  Ho(\mathcal{C})
  \,.
$$

=--

+-- {: .num_lemma #IsomorphismBetweenStandardAndAlternativeSuspensionInHomotopyCategory}
###### Lemma

There is a [[natural isomorphism]] in the [[stable homotopy category]]  between the standard suspension (def. \ref{SequentialSpectrumRealSuspension}) and the alternative suspension (def. \ref{SequentialSpectrumFakeSuspension}):

$$
  \Sigma (-)
  \simeq
  (-) \wedge S^1
  \;\;\;
  \in Ho(SeqSpec(Top))
$$

=--


+-- {: .proof}
###### Proof

Let $(L \dashv R) \colon SeqSpec(Top) \leftrightarrow Seq_2Spec(Top)$ for the [[Quillen equivalence]] between standard spectra with structure morphisms $S^1 \wedge X_n \to X_{n+1}$ to doubly-staged sequential spectra with structure morhisms $S^2 \wedge X'_n \to X'_{n+1}$. (...) 


Via the discussion in remark \ref{StandardAndAlternativeSuspensionAreNotDirectlyComparable}, there is a [[natural isomorphism]] in $SeqSpec(Top)$ between the image under $R$ of the two suspension operations

$$
  \tau \colon R (\Sigma(-)) \simeq R((-)\wedge S^1)
  \,,
$$

whose components are given by the [[smash product]]-[[braiding]] isomorphisms

$$
  S^2 \wedge (-) 
    \overset{\simeq}{\longrightarrow}
  (-) \wedge S^2
  \,.
$$

Let $Q$ be any choice of cofibrant replacement, i.e. a factorization for each object $X \in SeqSpec(Top)_{stable}$ of the initial morphism into it as

$$  
  \emptyset
   \overset{\in Cof}{\longrightarrow}
  Q X
   \overset{\in W \cap Fib}{\longrightarrow}
  \,.
$$

For $f \colon X \to Y$ a morphism, let $Q f$ be given by any choice of lift in 

$$
  \array{
    \emptyset && \longrightarrow && Q Y
    \\
    \downarrow &{}^{\mathllap{Q f}}\nearrow& \downarrow
    \\
    Q X &\to& X &\overset{f}{\to}& Y
  }
  \,.
$$


Then because $(L \dahsv R)$ above is a Quillen equivalence, we get the following diagram

$$
  \array{
     && L Q R (\Sigma X)
       &\underoverset{\in W_{st}}{L Q \tau}{\longrightarrow}&
     L Q R (X\wedge S^1)
     \\
     &{}^{\mathllap{\in W_{st}}}
       \swarrow & \downarrow && \downarrow & 
       \searrow^{\mathrlap{\in W_{st}}}
     \\
     \Sigma X
     &\longleftarrow& L R (\Sigma X) 
     & \underoverset{\in Iso \subset W_{st}}{L\tau}{\longrightarrow} &
     L R (X \wedge S^1)
     &\longrightarrow&
     X \wedge S^1
  }
  \,.
$$

This gives an isomorphism $\Sigma X \to X \wedge S^1$ in the homotopy category, and since there the class of $Q f$ is independent of the choice of lift, and since the other morphisms in the diagram are natural, this isomorphism is natural.

=--

+-- {: .num_lemma #FakeLoopingPreservesOmegaSpectra}
###### Lemma

With $\Sigma$ and $\Omega$ the alternative suspension and alternative looping functors from def. \ref{SequentialSpectrumFakeSuspension}:

1. $\Omega$ preserves [[Omega-spectra]] (def. \ref{OmegaSpectrum});

1. $\Sigma$ preserves stable equivalences (def. \ref{StableWeakEquivalenceOfSequentialTopologicalSpectra}).

=--

+-- {: .proof}
###### Proof

The first statement is clear. Moreover it is clear that $\Omega$ preserves strict fibrations and strict acyclic fibrations (since this is equivalently degreewise the statement that $(-)^{S^1} \colon Top^{\ast/}_{Quillen}\to Top^{\ast/}_{Quillen}$ does so). Therefore the adjunction $(\Sigma \dashv \Omega)$ from prop. \ref{AdjunctionsBetweenLoopingAndDeloopingForSeqSpec} is a [[Quillen adjunction]] on $SeqSpec(Top)_{strict}$, hence passes to an adjunction on the [[homotopy category of a model category|homotopy category]]. 

Therefore with $f$ a stable equivalence and $Y$ any Omega-spectrum, then

$$
  [\Sigma f,Y]_{strict}
  =
  [f,\Omega Y]_{strict}
$$

is an isomorphism, and hence $\Sigma f$ is a stable equivalence.

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

   and this is a stable equivalence (def. \ref{ClassesOfMorphismsOfTheStableModelStructureOnSequentialSpectra})

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

Now as in the proof of prop. \ref{AdjunctionsBetweenLoopingAndDeloopingForSeqSpec}, under applying the $(S^1\wedge (-)) \dashv (-)^{S^1}$-adjunction isomorphism twice, these diagrams are in bijection to diagrams for $n \geq 1$ of the form

$$
  \array{
    X_{n-1} &\overset{\tilde \sigma_{n-1}}{\longrightarrow}& (X_n)^{S^1}
    \\
    {}^{\mathllap{\tilde \sigma_{n-1}}}\downarrow 
      && 
    \downarrow^{\mathrlap{\tilde \sigma_n}}
    \\
    (X_n)^{S^1}
      &\underset{(\tilde \sigma_n)^{S^1}}{\longrightarrow}&
    \left((X_n)^{S^1}\right)^{S^1}
  }
  \,.
$$

This gives the claimed morphism $X \to \Omega X[-1]$.

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

By prop. \ref{CylinderSpectrumOverCWSpectrumIsGood}, on [[CW-spectra]] (def. \ref{CWSpectrum}) the canonical suspension functor is given by the "standard suspension" operation of def. \ref{SequentialSpectrumRealSuspension}. By prop. \ref{IsomorphismBetweenStandardAndAlternativeSuspensionInHomotopyCategory} however, this is naturally isomorphic -- on the level of the homotopy category -- to the alternative suspension operation of def. \ref{SequentialSpectrumFakeSuspension}. Therefore the claim follows with prop. \ref{FakeSuspensionInducesEquivalenceOfHomotopyCategories}.

=--

##### Triangulated category structure

The [[homotopy category of a model category|homotopy category]} of a [[stable model category]], def. \ref{StableModelCategory} inherits particularly nice properties that are usefully axiomatized for themselves. This axiomatics is called _[[triangulated category]]_ structure (def. \ref{CategoryWithCofiberSequences} below) where the "triangles" are referring to the structure of the long fiber sequences and long cofiber sequences ([prop.](Introduction+to+Stable+homotopy+theory+--+P#LongFiberSequence)) which happen to coincide in stable model category.

+-- {: .num_defn #AdditiveCategory}
###### Definition

An **[[additive category]]** is an [[Ab]]-[[enriched category]] (hence a [[category]] equipped with the structure of an [[abelian group]] on each [[hom-set]] such that [[composition]] is [[bilinear map|bilinear]]) and such that it has [[finite colimit|finite]] [[coproducts]].

=--

+-- {: .num_remark #BiproductsInAdditiveCategories}
###### Remark

The first condition in def. \ref{AdditiveCategory} means in perticular that there are [[zero morphisms]] and with the second condition this means that the empty coproduct is a [[zero object]]. Since the zero morphisms allow to form the diagrams

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
  }
  \,.
$$

it follows that with the [[coproduct]] $X\sqcup Y$ also the [[product]] $X \times Y$ exists and is canonically identified with the coproduct, and in fact the above diagram is equivalent to

$$
  \array{  
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
  \,.
$$

One calls this a [[biproduct]] and writes

$$
  X \oplus Y \simeq  X \sqcup Y \simeq X \times Y
  \,.
$$

=--

+-- {: .num_defn #AdditiveFunctor}
###### Definition

A [[functor]] $F \colon  \mathcal{A} \to \mathcal{B}$ between [[additive categories]], def. \ref{AdditiveCategory} is called an **[[additive functor]]** if it preserves finite [[biproducts]] (remark \ref{BiproductsInAdditiveCategories}). That is, 

1. $F$ maps a [[zero object]] to a zero object, $F(0) \simeq 0 \in \mathcal{B}$; 

1. given any two [[objects]] $X, Y \in \mathcal{A}$, there is an [[isomorphism]] $F(X \oplus Y) \cong F(x) \oplus F(y)$, and this respects the inclusion and projection maps of the [[direct sum]]:

$$
\array { X &          &            &          & Y \\
           & {}_{\mathllap{i_X}}\searrow &            & \swarrow_{\mathrlap{i_Y}} \\
           &          & X \oplus Y \\
           & {}^{\mathllap{p_X}}\swarrow &            & \searrow^{\mathrlap{p_Y}} \\
         x &          &            &          & y }
\quad\quad\stackrel{F}{\mapsto}\quad\quad
\array { F(X) &          &                                      &          & F(Y) \\
              & {}_{\mathllap{i_{F(X)}}}\searrow &   & \swarrow_{\mathrlap{i_{F(Y)}}} \\
              &          & F(X \oplus Y) \cong F(X) \oplus F(Y) \\
              & {}^{\mathllap{p_{F(X)}}}\swarrow &                                      & \searrow^{\mathrlap{p_{F(Y)}}} \\
         F(X) &          &                                      &          & F(Y) }
$$

=--



+-- {: .num_defn #CategoryWithCofiberSequences}
###### Definition

A **[[triangulated category]]** is

1. an [[additive category]] $Ho$ (def. \ref{AdditiveCategory});

1. an [[additive functor]] (def. \ref{AdditiveFunctor}), called the **suspension functor** or **[[shift functor]]**

   $$
     \Sigma \;\colon\; Ho \overset{\simeq}{\longrightarrow} Ho
   $$

   which is required to be an [[equivalence of categories]];

1. a sub-[[class]] $CofSeq \subset Mor(Ho^{\Delta[3]})$ of the class of triples of composable morphisms, called the class of **distinguished triangles**, where each element is of the form

   $$
     A \overset{}{\longrightarrow} B \overset{}{\longrightarrow} C \overset{}{\longrightarrow} \Sigma A
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


* **T1** For every object $X \in Ho$ then $(0,id_X,0)$ is a distinguished triangle

  $$
    0 \longrightarrow X \overset{id_X}{\longrightarrow} X 
    \overset{}{\longrightarrow} 0
    \,;
  $$


* **T2** If $(f,g,h)$ is a distinguished triangle, then so is $(g,h, - \Sigma f)$ and conversely; hence if

  $$
    A \overset{f}{\longrightarrow} B \overset{g}{\longrightarrow} B/A \overset{h}{\longrightarrow} \Sigma A
  $$

  is, then so is

  $$
    B \overset{g}{\longrightarrow} B/A \overset{h}{\longrightarrow} \Sigma A \overset{-\Sigma f}{\longrightarrow} \Sigma B
  $$

  and conversely.

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

* **T4** 

=--

##### Long fiber-cofiber sequences


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



+-- {: .num_prop}
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

Below in _[S-modules](#SModules)_ we give a unified discussion of all four models of spectra thus obtained (sequential, symmetric, orthogonal, excisive). Further below in _[The stable model structures](#TheStableModelStructures)_ we use this to construction and understand the [[model structures on spectra]] that present [[stable homotopy theory]].

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

In the symmetric case ($Dia = Sym$) the formula is similar except that $S^0 = Seq(q,q)_+$ is replaced by $Sym(q,q)_+ = \Sigma(q)_+$ and the colimit goes over the automorphisms that fix $q-n$ elements, thereby producing the partial smash tensor shown in the statement. Analogously for the orthogonal case ($Dia = Orth$).

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

Let $E$ be an Omega-spectrum. Then by the first item of lemma \ref{PropertiesOfAKindOfAlmostSpectrification}, for every $X$ the morphism

$$
  [X,r_E]_{strict}
    \;\colon\; 
  [X,E]_{strict} 
    \longrightarrow 
  [X, R^\infty E]_{strict}
$$

is an isomorphism. Since $r_{(-)}$ is a [[natural transformation]] (by def. \ref{AKindOfAlmostSpectrification}), the naturality squares gives a factorization of this morphism as

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

By theorem ref. \ref{StableModelStructuresOnDiagramSpectra}, and by lemmas  \ref{KInjectiveStableEquivalencesAreStrictEquivalences} and \ref{RetractsOfRelativeKCellComplexesAreTheStableEquivalencesAndStrictCofibrations}, every stable weak equivalence factors as a $K$-[[relative cell complex]] followed by weak equivalence in the strict model structure. Since the latter is degreewise a [[weak homotopy equivalence]] it is in particular a [[stable weak homotopy equivalence]]. Hence we are reduced to showing that every $K$-[[relative cell complex]] is a stable weak homotopy equivalence.

Observe now that we know this to be true for the elements of $K$ itself (def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra}): first of all, the elements in $F J$ are [[retracts]] of [[deformation retracts]] and therefore stable weak homotopy equivalences. Second, the morphisms denoted $k_n$ in def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra}, which resolve the maps $\lambda_n$ from def. \ref{CorepresentationOfAdjunctsOfStructureMaps}, as stable weak homotopy equivalences by lemma \ref{AdjunctsOfFreeSpectrumInclusionsAreOrAreNotStableWeakHomotopyEquivalences}.  This implies that so are their pushout products $k_n \Box i$. 

=--

This completes the proof of theorem \ref{RelationBetweenStableEquivalencesAndStableWeakHomotopyEquivalencesForDiagramSpectra}.




#### The stable model structures on structured spectra
 {#TheStableModelStructures}

+-- {: .num_theorem #StableModelStructuresOnDiagramSpectra}
###### Theorem

The [[Bousfield localization of model categories|left Bousfield localization]] of the strict model structures of prop. \ref{StrictModelStructureOnDiagramSpectra} at the stable equivalences of def. \ref{StableEquivalencesForDiagramSpectra} exist, to be called the _stable model structures_. 

Explicitly, there is a model structure $\mathbb{S}_{dia} Mod_{stable}$ whose

* cofibrations are those of the strict model structure (prop. \ref{StrictModelStructureOnDiagramSpectra});

* weak equivalences are the stable equivalences (def. \ref{StableEquivalencesForDiagramSpectra})

and the identity functors constitute a [[Quillen adjunction]] of the form

$$
  \mathbb{S}_{dia} Mod_{stable}
    \stackrel{\overset{id}{\longleftarrow}}{\underset{id}{\longrightarrow}}
  \mathbb{S}_{dia} Mod_{strict}
  \,.
$$


Moreover $\mathbb{S}_{dia} Mod_{stable}$ is a

1. [[compactly generated model category]];

1. [[proper model category]];

1. $Top^{\ast/}_{Quillen}$-[[enriched model category]].

=--

([MMSS00, theorem 9.2](#MMSS00)) 

We give the proof of theorem \ref{StableModelStructuresOnDiagramSpectra} [below](#StableModelStructureOnDiagramSpectraProof), it involves the following definitions and lemmas.

The generating cofibrations and acylic cofibrations are going to be the those induced via [[tensoring]] of representables from the [[classical model structure on topological spaces]] (giving the strict model structure), together with an additional set of morphisms to the generating acylic cofibrations that will force fibrant objects to be Omega-spectra. To that end we need the following little preliminary.


+-- {: .num_remark #CorepresentingForAdjunctOfStructureMapsAreStableEquivalences}
###### Remark

By construction, the morphisms $\lambda_n$ of lemma \ref{CorepresentingOfAdjunctsOfStructureMapsExists} are 
stable equivalences according to def. \ref{StableEquivalencesForDiagramSpectra}.

=--

We need to in addition resolve them by suitable cofibrations:

+-- {: .num_defn #ResolutionOfCorepresentationOfAdjunctsOfStructureMaps}
###### Definition

For $n \in \mathbb{N}$ let

$$
  \lambda_n 
    \colon 
  F_{n+} \stackrel{k_n}{\longrightarrow}
    Cyl(\lambda_n)
  \stackrel{def.retr.}{\longrightarrow}
  F_n S^0
$$

be a factorization of the morphism $\lambda_n$ of lemma \ref{CorepresentingOfAdjunctsOfStructureMapsExists} through a strict cofibration followed by a strict weak equivalence (e.g. through its [[mapping cylinder]] followed by a [[deformation retraction]] (see [here](mapping+cylinder#FactorizationOfMapThroughMappingCylinderFollowedByDeformationRetraction))).

=--

With this we may state the classes of morphisms that are going to be shown to be the classes of generating (acyclic) cofibrations for the stable model structures:

+-- {: .num_defn #GeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra}
###### Definition

Recall the sets

$$
  I \coloneqq \{S^{n-1} \hookrightarrow D^n\}_{n \in \mathbb{N}}
$$

$$
  J \coloneqq \{D^n \hookrightarrow D^n \times I\}_{n \in \mathbb{N}}
$$

of generating cofibrations and generating acyclic cofibrations, respectively, of the [[classical model structure on topological spaces]].

For $Dia \in \{Seq, Sym, Orth, Top^{\ast/}_{fin}\}$ any one of the four [[sites]], write

$$
  F I \coloneqq \{ y(x) \otimes i_+ \}_{{x \in Dia} \atop {i \in I}}
$$

for the set of morphisms arising as the [[tensoring]] of a [[representable functor|representable]] with a generating cofibration.
Similarly, write

$$
  F J \coloneqq \{ y(x) \otimes j_+ \}_{{x \in Dia} \atop {j \in J}}
  \,,
$$

for the set of morphisms arising as the [[tensoring]] of a [[representable functor|representable]] with a generating acyclic cofibration of the [[classical model structure on topological spaces]] (with basepoint adjoined).

Finally write 

$$
  K 
  \coloneqq
  F J
  \;\cup\;
  \{
    k_n \Box i_+
  \}_{{n \in \mathbb{N}} \atop {i \in I}}
$$

for the [[disjoint union]] of $F J$ with the [[pushout products]] of the resolved maps $k_n$ from def. \ref{ResolutionOfCorepresentationOfAdjunctsOfStructureMaps} with the elements in $I$.

=--

([MMSS 00, def. 9.3](#MMSS00))

+-- {: .num_lemma #ElementsOfKAreStableEquivalencesAndStrictCofibrations}
###### Lemma

Every element in $K$ (def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra}) is both:

1. a cofibration with respect to the strict model structure (prop. \ref{StrictModelStructureOnDiagramSpectra});

1. a stable equivalence (def. \ref{StableEquivalencesForDiagramSpectra}).

=--

+-- {: .proof}
###### Proof 

First regarding strict cofibrations: By the [[Yoneda lemma]], the elements in $F J$ have [[right lifting property]] against the strict fibrations, hence in particular they are strict cofibrations. Moreover, by [[Joyal-Tierney calculus]], $k_n \Box i_+$ has left lifting against any acyclic strict fibration $f$ precisely if $k_n$ has left lifting against $f^i$. By $\mathbb{S}_{dia} Mod_{strict}$ being a $Top$-[[enriched model category]] the latter is still a strict acyclic fibration. Since $k_n$ by construction is a strict cofibration, the lifting follows and hence also $k_n \Box i_+$ is a strict cofibration.

Regarding stable equivalences: The morphisms in $F J$ by design are strict weak equivalences, hence they are in particular stable equivalences. Similarly, the morphisms $k_n$ by construction, by [[two-out-of-three]] and by remark \ref{CorepresentingForAdjunctOfStructureMapsAreStableEquivalences} are stable equivalences. Hence the derived hom (...expand...) out of $k_n \Box i_+$ is the homotopy pullback of a weak equivalence, hence is a weak equivalence, hence on the homotopy category an iso.

=--


The point of the class $K$ in def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra} is to make the following true:

+-- {: .num_lemma #KInjectivesAreAcyclicCofibrations}
###### Lemma

A morphism $f \colon X \to Y$ in $\mathbb{S}_{dia} Mod$ is a $K$-[[injective morphism]] (for $K$ from def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra}) precisely if 

1. it is fibration in the strict model structure (hence degreewise a fibration)

1. for all $n \in \mathbb{N}$ the [[commuting squares]] of structure map compatibility on the underlying [[sequential spectra]] exhibit [[homotopy pullbacks]].  

=--

([MMSS 00, prop. 9.5](#MMSS00))

+-- {: .proof}
###### Proof

Lifting against $F J$ alone characterizes strict fibrations, hence degreewise fibrations. Lifting against the remaining [[pushout product]] morphism $k_n \Box i_+$ is, by [[Joyal-Tierney calculus]], equivalent to left lifting $i_+$ against the dual pullback product of $f^{k_n}$, which means that $f^{k_n}$ is a weak homotopy equivalence. But by construction (lemma \ref{CorepresentingOfAdjunctsOfStructureMapsExists}) $f^{k_n}$ is the comparison morphism into the homotopy pullback under consideration. 

=--

+-- {: .num_cor #KInjectivesObjectsAreOmegaSpectra}
###### Corollary

A $K$-[[injective object]] (for $K$ from def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra}) is in particular an Omega-spectrum, def. \ref{StableEquivalencesForDiagramSpectra}.

=--


+-- {: .num_lemma #KInjectiveStableEquivalencesAreStrictEquivalences}
###### Lemma

A morphism in $\mathbb{S}_{dia}Mod$ which is both 

1. a stable equivalence (def. \ref{StableEquivalencesForDiagramSpectra});

1. a $K$-[[injective morphisms]] (with respect to $K$ from def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra}) 

is an acyclic fibration in the stric model structure, prop. \ref{StrictModelStructureOnDiagramSpectra}, hence is degreewise a [[weak homotopy equivalence]] and [[Serre fibration]] of topological spaces;

=--

([MMSS 00, corollary 9.8](#MMSS00))

+-- {: .proof}
###### Proof

Let $f\colon E \to B$ be both a stable equivalence as well as a $K$-injective morphism. Since $K$ contains the generating acyclic cofibrations for the strict model structure (prop. \ref{StrictModelStructureOnDiagramSpectra}), $f$ is in particular a strict fibration, hence a degreewise fibration. Therefore the fiber $F$ of $f$ is its [[homotopy fiber]] in the strict model structure. This implies that for any $E$ that with $[f,E]_{strict}$ a bijection, by assumption also $[\ast,E]_{strict} \to [F,E]_{strict}$ is a bijection, hence that $F\to \ast$ is also a stable weak equivalence. 

Observe also that $F$, being the pullback of a $K$-injective morphisms is a $K$-[[injective object]], so that by corollary \ref{KInjectivesObjectsAreOmegaSpectra} $F$ is an Omega-spectrum. Together this implies with prop. \ref{StableEquivalencesBetweenOmegaSpectraAreStrictWeakEquivalences} that $F \to \ast$ is a weak equivalence in the strict model structure, hence degreewise a [[weak homotopy equivalence]]. From this the [[long exact sequence of homotopy groups]] imply that $\pi_{\bullet \geq 1}(f_n)$ is a [[weak homotopy equivalence]] for all $n$ and for each homotopy group in positive degree. 

To infer from this the remaining case that also $\pi_0(f_0)$ is an isomorphism, observe that by assumption of $K$-injectivity lemma \ref{KInjectivesAreAcyclicCofibrations} gives that $f_n$ is a homotopy pullback (in topological spaces) of $\Omega (f_{n+1})$. But by the above $\Omega (f_{n+1})$ is a weak homotopy equivalence, since $\pi_\bullet(\Omega(-)) = \pi_{\bullet+1}(-)$. Therefore $f_n$ is the homotopy pullback of a weak homotopy equivalence and hence itself a weak homotopy equivalence.

=--

+-- {: .num_lemma #RetractsOfRelativeKCellComplexesAreTheStableEquivalencesAndStrictCofibrations}
###### Lemma

For $K$ from def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra}  the [[retracts]] of $K$-[[relative cell complexes]] are precisely the morphisms which are

1. stable equivalences (def. \ref{StableEquivalencesForDiagramSpectra}), 

1. as well as a cofibration with respect to the strict model structure (prop. \ref{StrictModelStructureOnDiagramSpectra}).

=--

([MMSS 00, prop. 9.9 (i)](#MMSS00))


+-- {: .proof}
###### Proof

Since all elements of $K$ are stable equivalences and strict cofibrations by lemma \ref{ElementsOfKAreStableEquivalencesAndStrictCofibrations}, it follows that every retract of relative $K$-cell complex has the same property.

In the other direction, if $f$ is a stable equivalence and strict cofibration, by the [[small object argument]] it factors $f \colon \stackrel{i}{\to}\stackrel{p}{\to}$ as a relative $K$-cell complex $i$ followed by a $K$-[[injective morphism]] $p$. By the previous statement $i$ is a stable equivalence, and so by assumption and by [[two-out-of-three]] so is $p$. Therefore lemma \ref{KInjectiveStableEquivalencesAreStrictEquivalences} implies that $p$ is a strict acyclic fibration. But then the assumption that $f$ is a strict cofibration mean that it has the [[left lifting property]] against $p$, and so the [[retract argument]] implies that $f$ is a retract of the relative $K$-cell complex $i$.


=--

+-- {: .num_cor #KInjectivesAreIndeedTheStableFibrations}
###### Corollary

For $K$ from def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra}  the $K$-[[injective morphisms]]
are precisely those which are
[[injective morphism|injective]] with respect to the cofibrations of the strict model structure that are also stable equivalences.

=--

([MMSS 00, prop. 9.9 (ii)](#MMSS00)) 


+-- {: .num_lemma #StableAcyclicFibrationsAreEquivalentlyStrictAcyclicFibrations}
###### Lemma

A morphism in $\mathbb{S}_{dia}Mod$ is both

1. a stable equivalence (def. \ref{StableEquivalencesForDiagramSpectra})

1. [[injective morphism|injective]] with respect to the cofibrations of the strict model structure that are also stable equivalences;

precisely if it is an acylic fibration in the strict model structure (prop. \ref{StrictModelStructureOnDiagramSpectra}).

=--

([MMSS 00, prop. 9.9 (iii)](#MMSS00))

+-- {: .proof}
###### Proof

Every acyclic fibration in the strict model structure in injective with respect to to strict cofibrations by the strict model structure; and it is a stable equivalence by item 1 of prop. \ref{StableEquivalencesBetweenOmegaSpectraAreStrictWeakEquivalences}.

Conversely, a morphism injective with respect to stricts cofibrations that are stable equivalences is a $K$-[[injective morphism]] by corollary \ref{KInjectivesAreIndeedTheStableFibrations}, and hence if it is also a stable equivalence then by lemma \ref{KInjectiveStableEquivalencesAreStrictEquivalences} it is a strict acylic fibration.

=--

+-- {: .proof #StableModelStructureOnDiagramSpectraProof}
###### Proof
(of theorem \ref{StableModelStructuresOnDiagramSpectra})

The non-trivial points to check are the two [[weak factorization systems]].

That $(cof_{stable}\cap weq_{stable} \;,\; fib_{stable})$ is a weak factorization system follows from lemma \ref{RetractsOfRelativeKCellComplexesAreTheStableEquivalencesAndStrictCofibrations} and the [[small object argument]]. 

By lemma \ref{StableAcyclicFibrationsAreEquivalentlyStrictAcyclicFibrations} the stable acyclic fibrations are equivalently the strict acyclic fibrations and hence the weak factorization system $(cof_{stable} \;,\; fib_{stable} \cap we_{stable})$ is identified with that of the strict model structure $(cof_{strict} \;,\; fib_{strict} \cap we_{strict})$.

=--



#### Quillen equivalences of stable model structures
 {#QuillenEquivalencesOfStableModelStructures}

+-- {: .num_theorem #QuillenEquivalencesBetweenStableModelStructuresOnDiagramSpectra}
###### Theorem

The sequence of [[Quillen adjunctions]] between the strict model structures of prop. \ref{StrictModelStructureOnDiagramSpectra} remain Quillen adjunctions for the stable model structures of theorem \ref{StableModelStructuresOnDiagramSpectra} and indeed become a sequence of [[Quillen equivalences]] 

$$
 \array{
   && OrthSpec(Top)_{stable} && SymSpec(Top)_{stable} && SeqSpec(Top)_{stable}
   \\
   && \downarrow^{\mathrlap{\simeq}}
   && \downarrow^{\mathrlap{\simeq}}
   && \downarrow^{\mathrlap{\simeq}}
   \\
   \mathbb{S} Mod_{stable}
     &\stackrel{\overset{orth_!}{\longleftarrow}}{\underoverset{orth^\ast}{\simeq_{Qu}}{\longrightarrow}}&
   \mathbb{S}_{Orth} Mod_{stable}
     &\stackrel{\overset{sym_!}{\longleftarrow}}{\underoverset{sym^\ast}{\simeq_{Qu}}{\longrightarrow}}&
   \mathbb{S}_{Sym} Mod_{stable}
      &\stackrel{\overset{seq_!}{\longleftarrow}}{\underoverset{seq^\ast}{\simeq_{Qu}}{\longrightarrow}}&
   \mathbb{S}_{Seq} Mod_{stable}
 }
  \,.
$$

=--

([MMSS 00, section 10](#MMSS00))

We give the proof [below](#ProofOfQuillenEquivalencesOfStableModelStructures), after a few preliminaries.


+-- {: .num_lemma #AdjunctionsBetweenDiagramSpectraAreStableQuillenAdjunctions}
###### Lemma

The sequence of adjunctions between the categories $\mathbb{S}_{dia}Mod$ from prop. \ref{SystemOfAdjunctionsForDiagramSpectra} are [[Quillen adjunctions]] with respect to the stable model structures of theorem \ref{StableModelStructuresOnDiagramSpectra}

$$
 \array{
   && OrthSpec(Top)_{stable} && SymSpec(Top)_{stable} && SeqSpec(Top)_{stable}
   \\
   && \downarrow^{\mathrlap{\simeq}}
   && \downarrow^{\mathrlap{\simeq}}
   && \downarrow^{\mathrlap{\simeq}}
   \\
   \mathbb{S} Mod_{stable}
     &\stackrel{\overset{orth_!}{\longleftarrow}}{\underoverset{orth^\ast}{}{\longrightarrow}}&
   \mathbb{S}_{Orth} Mod_{stable}
     &\stackrel{\overset{sym_!}{\longleftarrow}}{\underoverset{sym^\ast}{}{\longrightarrow}}&
   \mathbb{S}_{Sym} Mod_{stable}
      &\stackrel{\overset{seq_!}{\longleftarrow}}{\underoverset{seq^\ast}{}{\longrightarrow}}&
   \mathbb{S}_{Seq} Mod_{stable}
 }
 \,.
$$


=--

([MMSS 00, lemma 10.1](#MMSS00))

+-- {: .proof}
###### Proof

By lemma \ref{RetractsOfRelativeKCellComplexesAreTheStableEquivalencesAndStrictCofibrations} the stable fibrations are equivalently the $K$-[[injective morphisms]].
By lemma \ref{KInjectivesAreAcyclicCofibrations} these are characterized by data that is preserved by right Quillen functors with respect to the strict model structure. Moreover by lemma \ref{StableAcyclicFibrationsAreEquivalentlyStrictAcyclicFibrations} the stable acyclic fibrations are equivalently the strict acyclic fibrations, which are of course also preserved by right Quillen functors for the strict model structure. Therefore the statement follows with prop. \ref{StrictModelStructureOnDiagramSpectra}.

=--

+-- {: .proof #ProofOfQuillenEquivalencesOfStableModelStructures}
###### Proof idea
(of theorem \ref{QuillenEquivalencesBetweenStableModelStructuresOnDiagramSpectra})

With lemma \ref{AdjunctionsBetweenDiagramSpectraAreStableQuillenAdjunctions} it is sufficient to show that all the total [[derived functors]] are [[adjoint equivalences]]. By [[two-out-of-three]] for Quillen equivalences, it is sufficient to show this for all the (composite) adjunctions whose right adjoint does _not_ point to $\mathbb{S}_{Sym}Mod$.

In these cases, theorem \ref{RelationBetweenStableEquivalencesAndStableWeakHomotopyEquivalencesForDiagramSpectra} implies that the right adjoint functor preserves and reflects weak equivalence (a morphism in its domain is a stable equivalence precisely if its image is).

In such a case, for checking a Quillen equivalence it is sufficient to check that the [[adjunction unit]] is a weak equivalence on all cofibrant objects (...citation...).

Since both adjoints in the present case preserve [[colimits]], [[tensoring]] with $Top^{\ast/}$ and the [[homotopy lifting property]], and since (...)

(...)

(...)

=--

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

### Basic reading

For **Prelude) Classical homotopy theory** 

A concise and yet comprehensive and self-contained re-write of the proof ([Quillen 67](#Quillen67)) of the [[classical model structure on topological spaces]] is in

* {#Hirschhorn15} [[Philip Hirschhorn]], _The Quillen model category of topological spaces_ ([arXiv:1508.01942](http://arxiv.org/abs/1508.01942)).

For relevant background on [[algebraic topology]] see also ([Aguilar-Gitler-Prieto 02, chapters 1-6](#AguilarGitlerPrieto02)) below. 

For general [[model category]] theory a decent concise account is in

* {#DwyerSpalinski95} [[William Dwyer]], J. Spalinski, _[[Homotopy theories and model categories]]_ ([pdf](http://folk.uio.no/paularne/SUPh05/DS.pdf)) in [[Ioan Mackenzie James]] (ed.), _[[Handbook of Algebraic Topology]]_ 1995

For the [[classical model structure on simplicial sets]] and its [[Quillen equivalence]] to that on topological spaces, good sources are

* {#GoerssJardine99} [[Paul Goerss]], [[Rick Jardine]], chapter I of_[[Simplicial homotopy theory]]_, Birkh&#228;user, Progress in Mathematics (1999), reprinted as Modern Classics (2009)

* {#JoyalTierney05} [[André Joyal]], [[Myles Tierney]], _An introduction to simplicial homotopy theory_, 2005  ([chapter I](http://hopf.math.purdue.edu/cgi-bin/generate?/Joyal-Tierney/JT-chap-01), more notes [pdf](http://mat.uab.cat/~kock/crm/hocat/advanced-course/Quadern47.pdf))

For the restriction to the [[convenient category of topological spaces|convenient category]] of [[compactly generated topological spaces]] a good source is still

* {#Lewis78} [[Gaunce Lewis]], _Compactly generated spaces_ ([pdf](http://www.math.uchicago.edu/~may/MISC/GaunceApp.pdf)), appendix A of _The Stable Category and Generalized Thom Spectra_ PhD thesis Chicago, 1978


For section **1) Stable homotopy theory** we follow the modern picture of the stable homotopy category in the style of the exposition

* {#Malkiewich14} [[Cary Malkiewich]], _The stable homotopy category_, 2014 ([pdf](http://math.uiuc.edu/~cmalkiew/stable.pdf)).

but fill in the details using the [[model structure on topological sequential spectra]]. The classical account in ([Adams 74, part III sections 2, 4-7](#Adams74)) is still a good read (but ignore the "[[Adams category]]"-construction of the [[stable homotopy category]] in sections III.2 and III.3).

For the discussion of [[ring spectra]] we pass to [[symmetric spectra]]. A comprehensive and account is in

* {#Schwede12} [[Stefan Schwede]], _[[Symmetric spectra]]_, 2012 ([pdf](http://www.math.uni-bonn.de/~schwede/SymSpec-v3.pdf))

In order to construct and understand the [[model structure on symmetric spectra]] via the [[model structure on orthogonal spectra]] we develop the approach of 

* {#MMSS00} [[Michael Mandell]], [[Peter May]], [[Stefan Schwede]], [[Brooke Shipley]], _[[Model categories of diagram spectra]]_, Proceedings of the London Mathematical Society, 82 (2001), 441-512 ([pdf](http://www.math.uchicago.edu/~may/PAPERS/mmssLMSDec30.pdf))

For **Interlude: Spectral sequences** a discussion streamlined for our purposes is in ([Rognes 12, section 2](#Rognes12)).

In **2) Adams spectral sequence** for the general theory we follow ([Hopkins 99, section 5](#Hopkins99)) as worked out in

* {#Aramian} [[Nersés Aramian]], _The Adams spectral sequence_ ([[AramianANSS.pdf:file]])

and we take some further clues from ([Adams 74, III.15](#Adams74)).

For the special case of the classical Adams spectral sequence a comprehensive survey is in 

* {#Bruner09} [[Robert Bruner]], _An Adams spectral sequence primer_, 2009 ([pdf](http://www.math.wayne.edu/~rrb/papers/adams.pdf))

For the **Seminar on Complex oriented cohomology** an excellent textbook to hold on to is

* {#Kochman96} [[Stanley Kochman]], chapters I - IV of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

While this gives detailed proofs, some standard steps used are made more explicit for instance in 

* {#Switzer75} [[Robert Switzer]], _Algebraic Topology - Homotopy and Homology_, Die  Grundlehren der Mathematischen Wissenschaften in Einzeldarstellungen, Vol. 212, Springer-Verlag, New York, N. Y., 1975. 


Specifically for **S.1) Generalized cohomology** a neat account is in:

* {#AguilarGitlerPrieto02} Marcelo Aguilar, [[Samuel Gitler]], Carlos Prieto, section 12 of _Algebraic topology from a homotopical viewpoint_, Springer (2002) ([toc pdf](http://tocs.ulb.tu-darmstadt.de/106999419.pdf))


For **S.2) Cobordism theory** an efficient collection of the highlights is in

* {#Malkiewich11} [[Cary Malkiewich]], _Unoriented cobordism and $M O$_, 2011 ([pdf](http://math.uiuc.edu/~cmalkiew/cobordism.pdf))

except that it omits proof of the [[Leray-Hirsch theorem]]/[[Serre spectral sequence]] and that of the [[Thom isomorphism]], but see the references there and see ([Kochman 96](#Kochman96), [Aguilar-Gitler-Prieto 02, section 11.7](#AguilarGitlerPrieto02)) for details.
 
For **S.3) Complex oriented cohomology** besides ([Kochman 96, chapter 4](#Kochman96)) have a look at part II of 

* {#Adams74} [[Frank Adams]], _[[Stable homotopy and generalized homology]]_, Chicago Lectures in mathematics, 1974

and

* {#Lurie10} [[Jacob Lurie]], lectures 1-10 of _[[Chromatic Homotopy Theory]]_, 2010

(These overlap, pick the one that seems more inviting on first reading.)

### Further reading

The two originals

* {#Quillen67} [[Daniel Quillen]], _Axiomatic homotopy theory_ in  _Homotopical algebra_, Lecture Notes in Mathematics, No. 43 43, Berlin (1967)

* {#Brown73} [[Kenneth Brown]], _[[Abstract Homotopy Theory and Generalized Sheaf Cohomology]]_, Transactions of the American Mathematical Society, Vol. 186 (1973), 419-458  ([JSTOR](http://www.jstor.org/stable/1996573))

are still an excellent source. For further reading on homotopy theory and stable homotopy theory a useful collection is

* {#James95} [[Ioan Mackenzie James]], _[[Handbook of Algebraic Topology]]_ 1995

The modern chromatic picture originates around

* {#Hopkins99} [[Mike Hopkins]], _[[Complex oriented cohomology theories and the language of stacks]]_, 1999 

a useful survey is in

* {#Wilson13} [[Dylan Wilson]] section 1.2 of _Spectral Sequences from Sequences of Spectra: Towards the Spectrum of the Category of Spectra_ lecture at _[2013 Pre-Talbot Seminar](http://math.harvard.edu/~hirolee/pretalbot2013/)_, March 2013 ([[DylanWilsonOnANSS.pdf:file]])

a wealth of details is in

* {#Ravenel86} [[Doug Ravenel]], _[[Complex cobordism and stable homotopy groups of spheres]]_, 1987/2003 ([pdf](http://www.math.rochester.edu/people/faculty/doug/mybooks/ravenelA1.pdf))

and new foundations have been laid in

* {#LurieHigherAlgebra} [[Jacob Lurie]], _[[Higher Algebra]]_

Further useful lecture notes pointed to above include the following:

* {#Hatcher04} [[Alan Hatcher]], _[Spectral sequences in algebraic topology](http://www.math.cornell.edu/~hatcher/SSAT/SSATpage.html)_ _II: The Adams spectral sequence_, 2004 ([pdf](http://www.math.cornell.edu/~hatcher/SSAT/SSch2.pdf))

* {#Rognes12} [[John Rognes]], _The Adams spectral sequence_ (following [Bruner](#Bruner)), 2012 ([pdf](http://folk.uio.no/rognes/papers/notes.050612.pdf))


