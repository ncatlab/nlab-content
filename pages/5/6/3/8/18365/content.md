
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

We discuss in detail the realization of the abstract concept of [[cofiber sequences]] in its explicit incarnation in [[point-set topology]], the way it is traditionally presented in [[topology]] textbooks.

Hence we use the concepts of [[homotopy equivalence]] instead of [[weak homotopy equivalence]]. For discussion using the latter in the context of the [[classical model structure on topological spaces]] see instead at _[[Introduction to Homotopy Theory]]_ the section _[Homotopy fiber sequences](Introduction+to+Homotopy+Theory#HomotopyFiberSequences)_.

## Background

Throughout, write $I \coloneqq [0,1] \subset \mathbb{R}$ for the [[closed interval]] equipped with its [[Euclidean space|Euclidean]] [[metric topology]].


### Homotopy equivalences

+-- {: .num_defn #LeftHomotopy}
###### Definition

For $f,g\colon X \longrightarrow Y$ two [[continuous functions]] between [[topological spaces]] $X,Y$, then a **[[homotopy]]**

$$
  \eta \colon f \,\Rightarrow_L\, g
$$

is a [[continuous function]]

$$
  \eta \;\colon\; X \times I \longrightarrow Y
$$


out of the standard [[cylinder object]] over $X$: the [[product space]] of $X$ with the [[Euclidean space|Euclidean]] [[closed interval]], such that this fits into a [[commuting diagram]] of the form

<div style="float:right;margin:0 10px 10px 0;">
<img src="http://www.ncatlab.org/nlab/files/AHomotopy.jpg" width="400">
</div>


$$
  \array{
     X
     \\
     {}^{\mathllap{(id,\delta_0)}}\downarrow & \searrow^{\mathrlap{f}}
     \\
     X \times I &\stackrel{\eta}{\longrightarrow}& Y
     \\
     {}^{\mathllap{(id,\delta_1)}}\uparrow & \nearrow_{\mathrlap{g}}
     \\
     X
  }
  \,.
$$

(graphics grabbed from J. Tauber [here](http://jtauber.com/blog/2005/07/01/path_homotopy/))

=--

+-- {: .num_defn #HomotopyEquivalence}
###### Definition
**([[homotopy equivalence]])**

A [[continuous function]] $f \colon X \to Y$ is called a _[[homotopy equivalence]]_ if there exist

1. a continuous function $g \colon Y \to X$;

1. homotopies (def. \ref{LeftHomotopy}) of the form

   $g \circ f \Rightarrow id_X \phantom{AAAA} f \circ g \Rightarrow id_Y$

=--


+-- {: .num_example #ContractibleTopologicalSpace}
###### Example
**([[contractible topological space]])**

A [[topological space]] $X$ is called _[[contractible topological space|contractible]]_ if the unique map to the [[point space]] $X \to \ast$ is a [[homotopy equivalence]] (def. \ref{HomotopyEquivalence}).

=--

### Cofibrations

+-- {: .num_defn #HurewiczCofibration}
###### Definition
**([[Hurewicz cofibration]])

A [[continuous function]] $i \colon A \longrightarrow X$ is called a _[[Hurewicz cofibration]]_ or just _cofibration_ if it satisfies the [[homotopy extension property]] in that:

* for any [[topological space]] $Y$,

* for all continuous functions $ f \colon A\to Y$, $\tilde{f}:X\to Y$ such that $\tilde{f}\circ i=f$

  $$
    \array{
       A &\stackrel{f}{\to}& Y
       \\
       {}^{\mathllap{i}}\downarrow & \nearrow_{\mathrlap{\tilde f}}
       \\
       X
    }
  $$


* and any [[left homotopy]] $F \colon A\times I\to Y$ such that $F(-,0)=f$

there is a homotopy $\tilde{F} \colon X\times I\to Y$ such that

* $\tilde{F}\circ(i\times id_I)=F$

  $$
    \array{
       A \times I &\overset{F}{\longrightarrow}& Y
       \\
       {}^{\mathllap{i \times id_I}}\downarrow & \nearrow_{\mathrlap{\tilde F}}
       \\
       X \times I
    }
  $$

* and $\tilde{F}(-,0)=\tilde{f}$

  $$
    \array{
       A &\overset{id_A \times const_0}{\longrightarrow}& A \times I &\overset{F}{\longrightarrow}& Y
       \\
       {}^{\mathllap{i \times id_I}}\downarrow
       && {}^{\mathllap{i \times id_I}}\downarrow & \nearrow_{\mathrlap{\tilde F}}
       \\
       X &\underset{id_X \times const_0}{\longrightarrow}& X \times I
    }
    \phantom{AAA}
      =
    \phantom{AAA}
    \array{
    \array{
       A &\stackrel{f}{\to}& Y
       \\
       {}^{\mathllap{i}}\downarrow & \nearrow_{\mathrlap{\tilde f}}
       \\
       X
    }cco
    }
  $$

If the [[image]] $i(A) \subset X$ is a [[closed subset]], then $i$ is called a _[[closed Hurewicz cofibration]]_.

=--

+-- {: .num_example #RelativeCellComplexInclusionsAreClosedCofibrations}
###### Example
**([[retracts]] of [[relative cell complex]] inclusions are [[closed Hurewicz cofibrations]])

If $A$ is a [[topological space]] and $i \colon A \hookrightarrow X$ is a [[relative cell complex]] inclusion, then $i$ is a [[closed Hurewicz cofibration]] (def. \ref{HurewiczCofibration}).

Also every [[retract]] of such $i$ ([this sense](Introduction+to+Homotopy+Theory#RetractsOfMorphisms)) is a closed Hurewicz cofibration.

=--


### Pushouts / space attachments

Cofiber sequences ([below](#CofiberSequences)) are constructed by iterated _[[pushouts]]_ in the [[category]] [[Top]] of [[topological spaces]] with [[continuous functions]] between them ([[space attachments]]), see at _[Top -- Universal constructions](Top#UniversalConstructions)_.

+-- {: .num_example #QuotientBySubspace}
###### Example
**([[quotient space]] by a [[subspace]])**

Let $X$ be a [[topological space]] and $A \subset X$ a [[inhabited set|non-empty]] [[subset]].
Consider the [[equivalence relation]] on $X$ which identifies all points in $A$ with each other. The resulting [[quotient space]] is denoted $X/A$.

Notice that $X/A$ is canonically a [[pointed topological space]], with base point the [[equivalence class]] $A/A \subset X/A$ of $A$.

If $A = \emptyset$ is the [[empty space]], then one defines

$$
  X/\emptyset \coloneqq X_+ \coloneqq X \sqcup \ast
$$

to be the [[disjoint union space]] of $X$ with the [[point space]]. This is no longer a quotient space, but both constructions are unified by the _[[pushout]]_ $i \colon A \to X$ along the map $A \to \ast$, equivalently the [[cokernel]] of the inclusion:

$$
  \array{
    A &\overset{i}{\hookrightarrow}& X
    \\
    \downarrow &(po)& \downarrow
    \\
    \ast &\longrightarrow& X/A
  }
  \,.
$$

=--



+-- {: .num_example #ClosedSubspacesGluing}
###### Example
**([[union]] of two [[open subset|open]] or two [[closed subset|closed]] [[subspaces]] is [[pushout]])**

Let $X$ be a [[topological space]] and let $A,B \subset X$ be [[subspaces]] such that

1. $A,B \subset X$ are both [[open subsets]] or are both [[closed subsets]];

1. they constitute a [[cover]]: $X = A \cup B$

Write $i_A \colon A \to X$ and $i_B \colon B \to X$ for the corresponding inclusion [[continuous functions]].

Then the [[commuting square]]

$$
  \array{
     A \cap B &\longrightarrow& A
     \\
     \downarrow &(po)& \downarrow^{\mathrlap{i_A}}
     \\
     B &\underset{i_B}{\longrightarrow}& X
  }
$$

is a [[pushout]] square in [[Top]] (see [there](Top#UniversalConstructions)).

By the [[universal property]] of the [[pushout]] this means in particular that for $Y$ any [[topological space]] then a function of underlying sets

$$
  f \;\colon\; X \longrightarrow Y
$$

is a [[continuous function]] as soon as its two restrictions

$$
  f\vert_A \;\colon\; A \longrightarrow Y
  \phantom{AAAA}
  f\vert_A \;\colon\; B \longrightarrow Y
$$

are continuous.

=--

+-- {: .proof}
###### Proof

Clearly the underlying diagram of underlying [[sets]] is a pushout in [[Set]]. Therefore (by [this prop.](Top#DescriptionOfLimitsAndColimitsInTop)) we need to show that the [[topological space|topology]] on $X$ is the [[final topology]] induced by the set of functions $\{i_A, i_B\}$, hence that
a [[subset]] $S \subset X$ is an [[open subset]] precisely if the [[pre-images]] (restrictions)

$$
  i_A^{-1}(S) = S \cap A
   \phantom{AAA}
    \text{and}
   \phantom{AAA}
  i_B^{-1}(S) = S \cap B
$$

are open subsets of $A$ and $B$, respectively.

Now by definition of the [[subspace topology]], if $S \subset X$ is open, then the intersections $A \cap S \subset A$ and $B \cap S \subset B$ are open in these subspaces.

Conversely, assume that $A \cap S \subset A$ and $B \cap S \subset B$ are open. We need to show that then $S \subset X$ is open.

Consider now first the case that $A;B \subset X$ are both open open. Then by the nature of the [[subspace topology]], that $A \cap S$ is open in $A$ means that there is an open subset $S_A \subset X$ such that $A \cap S = A \cap S_A$. Since the intersection of two open subsets is open, this implies that $A \cap S_A$ and hence $A \cap S$ is open.  Similarly $B \cap S$. Therefore

$$
  \begin{aligned}
    S
     & =
    S \cap X
    \\
    & = S \cap (A \cup B)
    \\
    & =  (S \cap A) \cup (S \cap B)
  \end{aligned}
$$

is the union of two open subsets and therefore open.

Now consider the case that $A,B \subset X$ are both closed subsets.

Again by the nature of the subspace topology, that $A \cap S \subset A$ and $B \cap S \subset B$ are open means that there exist open subsets $S_A, S_B \subset X$ such that $A \cap S = A \cap S_A$ and $B \cap S = B \cap S_B$. Since $A,B \subset X$ are closed by assumption, this means that $A \setminus S, B \setminus S \subset X$ are still closed, hence that $X \setminus (A \setminus S), X \setminus (B \setminus S) \subset X$ are open.

Now observe that (by [[de Morgan duality]])

$$
  \begin{aligned}
    S
      & = X \setminus (X \setminus S)
    \\
      & =
    X \setminus ( (A \cup B) \setminus S )
    \\
      & =
    X \setminus ( (A \setminus S) \cup (B \setminus S) )
    \\
     & =
    (X \setminus (A \setminus S)) \cap (X \setminus (B \setminus S))
    \,.
  \end{aligned}
$$

This exhibits $S$ as the intersection of two open subsets, hence as open.

=--

A general abstract fact about pushouts which we will use repeatedly in the proofs below is the following:

+-- {: .num_prop #PastingLaw}
###### Proposition
**([[pasting law]])**

Consider a [[diagram]] in [[Top]] (or in any other [[category]]) of the following form:

$$
  \array{
     &\longrightarrow& &\longrightarrow&
    \\
    \downarrow &(po)& \downarrow && \downarrow
    \\
     &\longrightarrow& &\longrightarrow&
  }
 \,,
$$

where the left square is a [[pushout]].

Then: The total rectangle is a [[pushout]] precisely if the right square is.

=--


We need the following two facts (prop. \ref{CofibrantHomotopyEquivalencePushout} prop. \ref{ContractibleSubcomplexQuotient}) regarding the stability of cofibrations under pushout.

+-- {: .num_prop #CofibrantHomotopyEquivalencePushout}
###### Proposition
**([[pushout]] of cofibrations)

Let $A$ be a [[topological space]] and let
$A \hookrightarrow X$ be a [[closed Hurewicz cofibration]].

Then for every [[continuous function]] $f \colon A \to Y$, the [[pushout]] $f_\ast i$ in

$$
  \array{
     A &\overset{f}{\longrightarrow}& Y
     \\
     {}^{\mathllap{i}}\downarrow &(po)& \downarrow^{\mathrlap{f_\ast i}}
     \\
     X &\longrightarrow& X \underset{A}{\sqcup} Y
  }
$$

is also a [[closed Hurewicz cofibration]]. Moreover, if in addition

1. $i$ is a [[retract]] of a [[relative cell complex]] inclusion, then so is $f_\ast i$,

1. $i$ is a [[homotopy equivalence]], then so is $f_\ast i$.

=--

Prop. \ref{CofibrantHomotopyEquivalencePushout} is a consequence of the existence of the [[Strøm model structure]] $Top_{Strom}$ and the [[classical model structure on topological spaces]] $Top_{Quillen}$ and of the fact that the identity [[functors]] $Top_{Strom} \underoverset{\underset{id}{\longrightarrow}}{\overset{id}{\longleftarrow}}{\bot} Top_{Quillen}$ constitute a [[Quillen adjunction]].


+-- {: .num_prop #ContractibleSubcomplexQuotient}
###### Proposition
**([[quotient space|quotient]] by [[contractible topological space|contractible]] closed subspace)**

Let $i \colon A \longrightarrow X$ be a [[closed Hurewicz cofibration]].

If $f \colon A \to Y$ is a [[homotopy equivalence]] (def. \ref{HomotopyEquivalence}) then its [[pushout]] $i_\ast f$ in

$$
  \array{
     A &\overset{i}{\longrightarrow}& X
     \\
     {}^{\mathllap{f}}\downarrow &(po)& \downarrow^{\mathrlap{i_\ast(f)}}
     \\
     Y &\longrightarrow& Y \underset{A}{\sqcup} X
  }
$$

is also a homotopy equivalence.

In particular if $A$ is a [[contractible topological space]] (example \ref{ContractibleTopologicalSpace}), then the coprojection

$$
  X \longrightarrow X/A
$$

to the [[quotient space]] (example \ref{QuotientBySubspace}) is a [[homotopy equivalence]].

=--

Prop. \ref{ContractibleSubcomplexQuotient} is again a consequence of the existence of the [[Strøm model structure]] $Top_{Strom}$: It is the statement that $Top_{Strom}$ is a [[left proper model category]] which follows ([this cor.](proper%20model%20category#AllObjectsFibrantImpliesRightProper)) since all its objects are evidently cofibrant. An elementary proof in [[point-set topology]] is offered in ([Hatcher, prop. 0.17](algebraic+topology#Hatcher))


## Mapping cones


+-- {: .num_defn #ConeCyclinder}
###### Definition
**(topological [[cylinder]] and cone)**

Let $X$ be a [[topological space]]. Then

1. the _standard [[cylinder]]_ on $X$ is the [[product topological space]]

   $$
     Cyl(X) \coloneqq X \times [0,1]
   $$

1. the _standard [[cone]]_ on $X$ is the [[quotient space]] (example \ref{QuotientBySubspace})

   $$
     Cone(X) \coloneqq Cyl(X) / (X \times \{0\})
   $$

   of the standard cylinder by the [[subspace]] $X \times \{0\} \subset X \times [0,1]$.

   Equivalently this is the following [[pushout]] in [[Top]]

   $$
     \array{
        X \times \{0\} &\hookrightarrow& Cyl(X)
        \\
        \downarrow &(po)& \downarrow
        \\
        \ast &\longrightarrow& Cone(X)
     }
   $$

=--

+-- {: .num_lemma #InclusionIntoCylinderIsHomotopyEquivalence}
###### Lemma

Let $X$ be a topological space. Then the canonical inclusions

$$
  X \longrightarrow Cyl(X)
  \phantom{AAAA}
  \ast \longrightarrow Cone(X)
$$

are [[homotopy equivalences]]. Hence
every [[cone]] is a [contractible topological space]] (example \ref{ContractibleTopologicalSpace}).

=--



+-- {: .num_defn #MappingConeCylinder}
###### Definition
**([[mapping cylinder]] and [[mapping cone]])**

Let $f \colon X \to Y$ be a [[continuous function]] between [[topological spaces]]. Then

1. the _[[mapping cylinder]]_ of $f$ is the [[space attachment]]

   $$
     Cyl(f) \coloneqq Y \cup_f Cyl(X)
   $$

   of $Y$ with the [[cylinder]] on $X$, according to def. \ref{ConeCyclinder}, hence the following [[pushout]] in [[Top]]

   $$
     \array{
       X &\overset{f}{\longrightarrow}& Y
       \\
       \downarrow &(po)& \downarrow
       \\
       Cyl(X) &\longrightarrow& Cyl(f)
     }
   $$

1. the _[[mapping cone]]_ of $f$ is the [[space attachment]]

   $$
     Cone(f) \coloneqq Y \cup_f Cone(X)
   $$

   hence the following [[pushout]] in [[Top]]:

   $$
     \array{
       X &\overset{f}{\longrightarrow}& Y
       \\
       \downarrow &(po)& \downarrow
       \\
       Cone(X) &\longrightarrow& Cone(f)
     }
   $$


=--

+-- {: .num_remark #MappingConePasting}
###### Remark

In summary, def. \ref{ConeCyclinder} and def. \ref{MappingConeCylinder} say that for $f \colon X \to Y$ a [[continuous function]] then we have a [[pasting]] of [[pushout]] diagrams in [[Top]] of the following form:

$$
  \array{
    && X &\stackrel{f}{\to}& Y
    \\
    && \downarrow^{\mathrlap{i_1}} &(po)& \downarrow
    \\
    X &\stackrel{i_0}{\to}& Cyl(X) &\to & Cyl(f)
    \\
    \downarrow &(po)& \downarrow &(po)& \downarrow
    \\
    {*} &\to& Cone(X) &\to& Cone(f)
  }
  \,.
$$

Since $X \to Cone(X)$ is a [[closed Hurewicz cofibration]] , the [[pasting law]] together with prop. \ref{CofibrantHomotopyEquivalencePushout} therefore implies that also $Y \to Cone(f)$ is a closed Hurwicz cofibration.



=--

+-- {: .num_example #Suspension}
###### Example
**([[suspension]])

For $X$ a [[topological space]], then the [[mapping cone]] (def. \ref{MappingConeCylinder})
of the unique function $X \to \ast$ to the [[point space]] is

$$
  S X
    \coloneqq
  Cone(X \to \ast)
   \simeq
  Cone(X) \underset{X}{\sqcup} Cone(X)
  \,.
$$

This is called the _[[suspension]]_ of $X$.

=--




The mapping cone of a map $X \to Y$ is to be thought of as the homotopy-quotient of the $Y$ by $X$, as opposed to be the naive quotient. This is made precise by the following two statements, lemma \ref{RelativeCellComplexInclusionMappingCone} and lemma \ref{ForClosedImageQuotientOfMappingConeByCone}:


+-- {: .num_lemma #RelativeCellComplexInclusionMappingCone}
###### Lemma

If $f \colon X \to Y$ is a [[closed Hurewicz cofibration]] (def. \ref{HurewiczCofibration}), then the coprojection

$$
  Cone(f) \longrightarrow Y/f(X)
$$

from its [[mapping cone]] (def. \ref{MappingConeCylinder}) to the naive [[quotient space]] (example \ref{QuotientBySubspace})  is a [[homotopy equivalence]].


=--

+-- {: .proof}
###### Proof

Consider the diagram

$$
  \array{
     X &\overset{f}{\longrightarrow}& Y
     \\
     \downarrow &(po)& \downarrow
     \\
     Cone(X) &\longrightarrow& Cone(f)
     \\
     \downarrow &(po)& \downarrow
     \\
     \ast &\longrightarrow& Cone(f)/Cone(X)
  }
$$

Since $f$ is a [[closed Hurewicz cofibration]], so is $Cone(X) \to Cone(f)$, by prop. \ref{CofibrantHomotopyEquivalencePushout}. Since $Cone(X) \to \ast$ is a [[homotopy equivalence]] (lemma \ref{InclusionIntoCylinderIsHomotopyEquivalence}), so is
$Cone(f) \to Cone(f)/Cone(X)$, by prop. \ref{ContractibleSubcomplexQuotient}. But by lemma \ref{ForClosedImageQuotientOfMappingConeByCone} there is also a homeomorphism $Cone(f)/Cone(X) \simeq Y/f(X)$.

=--

+-- {: .num_lemma #ForClosedImageQuotientOfMappingConeByCone}
###### Lemma

Let $f \colon X \to Y$ be a [[continuous function]] such that the [[image]] $f(X) \subset Y$ is a [[closed subset]].

Then there is a [[homeomorphism]]

$$
  Cone(f)/Cone(X) \simeq Y / f(X)
$$

between the [[quotient space]] (example \ref{QuotientBySubspace}) of the [[mapping cone]] of $f$ (def. \ref{MappingConeCylinder}) by the [[cone]] of $X$ (def. \ref{ConeCyclinder}) and the [[quotient space]] of $Y$ be the [[image]] of $X$.

=--

+-- {: .proof}
###### Proof

Consider the following [[diagram]] in [[Top]]:

$$
  \array{
     f(X) &\longrightarrow& Y
     \\
     \downarrow &(po)& \downarrow
     \\
     f(Cone(X)) &\longrightarrow& Cone(f)
     \\
     \downarrow &(po)& \downarrow
     \\
     \ast &\longrightarrow& Cone(f)/Cone(X)
  }
$$

Here the top square is a [[pushout]] by example \ref{ClosedSubspacesGluing}, while the bottom square is a pushout by def. \ref{MappingConeCylinder}. Hence the total rectangle is also a pushout, by the [[pasting law]] (prop. \ref{PastingLaw}). But that total rectangle is the defining pushout for $Y/f(X)$ (by example \ref{QuotientBySubspace}). Hence the statement follows by the [[universal property]] of the pushout.

=--




## Cofiber sequences
 {#CofiberSequences}

+-- {: .num_prop #HomotopyEquivalenceSuspensionWithMappingConeOfMappingCone}
###### Proposition

Let $f \colon X \to Y$ be a [[continuous function]] with [[closed subset|closed]] [[image]] $f(X) \subset Y$. Write $Cone(g)$ in

$$
  \array{
    X
      &\overset{f}{\longrightarrow}&
    Y
      &\overset{g}{\longrightarrow}&
    Cone(f)
      &\overset{}{\longrightarrow}&
    Cone(g)
  }
$$

for the [[mapping cone]] (spring) of the inclusion $g$ of $Y$ into the mapping cone of $f$.

Then the canonical quotient coprojection

$$
  Cone(g) \to \Sigma X
$$

to the [[suspension]] of $X$ (example \ref{Suspension}) is a [[homotopy equivalence]] (def. \ref{HomotopyEquivalence}).

=--

+-- {: .proof}
###### Proof

Since $g \colon Y \to Cone(f)$ is a [[closed Hurewicz cofibration]] (by remark \ref{MappingConePasting}), lemma \ref{RelativeCellComplexInclusionMappingCone} gives that

$$
  Cone(g) \to Cone(f)/g(Y)
$$

is a [[homotopy equivalence]].  But then there is the following evident [[homeomorphism]]

$$
  Cone(f)/g(Y)
   =
  (Y \cup_f Cone(X))/Y
   \simeq
  Cone(X)/X
   \simeq
  S X
  \,.
$$

=--

<img src="http://ncatlab.org/nlab/files/mappingcone.jpg" width="660" >

(graphics taken from [Muro 10](http://personal.us.es/fmuro/praha.pdf))

Hence from every $f \colon X \to Y$ with closed image, we get long sequences

$$
  \array{
    X
      &\overset{f}{\longrightarrow}&
    Y
      &\overset{g}{\longrightarrow}&
    Cone(f)
      &\longrightarrow&
    Cone(g)
    \\
    && && &&
    \downarrow^{\mathrlap{\text{homotopy} \atop \text{equivalence}}}
    \\
    && && &&
    S X
      &\overset{S f}{\longrightarrow}&
    S Y
      &\longrightarrow& \cdots
  }
$$

## Pointed cofiber sequence

(...)
