
{:bluebox: .un_remark style="border:solid #000000;background: #E6DF13;border-width:2px 1px;padding:0 1em;margin:0 1em;"}


***


These are lecture notes giving a detailed introduction to classical _[[homotopy theory]]_, starting with the concept of [[homotopy]] in [[topological spaces]] and motivating from this the "abstract homotopy theory" in general [[model categories]].

$\,$


For background on basic [[topology]] see at _[[Introduction to Topology]]_.

For application to [[homological algebra]] see at _[[schreiber:Introduction to Homological Algebra]]_.

For application to [[stable homotopy theory]] see at  _[[Introduction to Stable homotopy theory]]_.


***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

$\,$


While the field of [[algebraic topology]] clearly originates in [[topology]], it is not actually interested in [[topological spaces]] regarded up to topological [[isomorphism]], namely [[homeomorphism]] ("[[point-set topology]]"), but only in topological spaces regarded up to [[weak homotopy equivalence]] -- hence it is interested only in the "weak [[homotopy types]]" of topological spaces. This is so notably because [[ordinary cohomology]] [[cohomology group|groups]] are [[invariants]] of the (weak) [[homotopy type]] of topological spaces but do not detect their [[homeomorphism]] class.

The [[category]] of topological spaces obtained by [[localization of a category|forcing]] [[weak homotopy equivalences]] to become [[isomorphisms]] is the "[[classical homotopy category]]" [[Ho(Top)]]. This homotopy category however has forgotten a little too much information: homotopy theory really wants the [[weak homotopy equivalences]] not to become plain [[isomorphisms]], but to become actual [[homotopy equivalences]]. The structure that reflects this is called a _[[model category]]_ structure (short for "category of models for [[homotopy types]]"). For classical homotopy theory this is accordingly called the _[[classical model structure on topological spaces]]_. This we review here.


## Topological homotopy theory
 {#BackgroundOnTopologicalHomotopyTheoryFromAlgebraicTopology}

This section recalls relevant concepts from actual [[topology]] ("[[point-set topology]]") and highlights facts that motivate the axiomatics of [[model categories]] [below](#ModelCategoryTheory). We prove two technical lemmas (lemma \ref{CompactSubsetsAreSmallInCellComplexes} and lemma \ref{AcyclicSerreFibrationsAreTheJTopFibrations}) that serve to establish the abstract homotopy theory of topological spaces [further below](#TheClassicalModelStructureOfTopologicalSpaces).

**Literature** ([Hirschhorn 15](#Hirschhorn15))

$\,$

Throughout, let _[[Top]]_ denote the [[category]] whose [[objects]] are [[topological spaces]] and whose [[morphisms]] are [[continuous functions]] between them. Its [[isomorphisms]] are the [[homeomorphisms]].

(Further [below](#ModelStructureOnCompactlyGeneratedTopologicalSpaces) we restrict attention to the [[full subcategory]] of [[compactly generated topological spaces]].)


### Universal constructions

To begin with, we recall some basics on [[universal constructions]] in [[Top]]: [[limits]] and [[colimits]] of [[diagrams]] of [[topological spaces]]; [[exponential objects]].

Generally, recall:

+-- {: .num_defn #LimitsAndColimits}
###### Definition

A **[[diagram]]** in a [[category]] $\mathcal{C}$ is a [[small category]] $I$ and a [[functor]]

$$
  X_\bullet
  \;\colon\;
  I \longrightarrow \mathcal{C}
$$

$$
  (i \overset{\phi}{\longrightarrow} j)
  \;
  \mapsto
  ( X_i \overset{X(\phi)}{\longrightarrow} X_j)
  \,.
$$

A **[[cone]]** over this diagram is an object $Q$ equipped with morphisms $p_i \colon Q \longrightarrow X_i$ for all $i \in I$, such that all these triangles commute:

$$
  \array{
     && Q
     \\
     & {}^{\mathllap{p_i}}\swarrow && \searrow^{\mathrlap{p_j}}
     \\
     X_i && \underset{X(\phi)}{\longrightarrow} && X_j
  }
  \,.
$$

Dually, a **[[co-cone]]** under the diagram is $Q$ equipped with morphisms $q_i \colon X_i \longrightarrow Q$ such that all these triangles commute:

$$
  \array{
    X_i && \overset{X(\phi)}{\longrightarrow} && X_j
    \\
    & {}_{\mathllap{q_i}}\searrow && \swarrow_{\mathrlap{q_j}}
    \\
    && Q
  }
  \,.
$$

A **[[limit]]** over the diagram is a universal cone, denoted $\underset{\longleftarrow}{\lim}_{i \in I} X_i$, that is: a cone such that every other cone uniquely factors through it $Q \longrightarrow \underset{\longleftarrow}{\lim}_{i \in I} X_i$, making all the resulting triangles commute.

Dually, a **[[colimit]]** over the diagram is a universal co-cone, denoted $\underset{\longrightarrow}{\lim}_{i \in I} X_i$.

=--


We now discuss limits and colimits in $\mathcal{C}= $ [[Top]]. The key for understanding these is the fact that there are initial and final topologies:

+-- {: .num_defn #InitialAndFinalTopologies}
###### Definition

Let $\{X_i = (S_i,\tau_i) \in Top\}_{i \in I}$ be a [[set]] of [[topological spaces]], and let $S \in Set$ be a bare [[set]]. Then

1. For $\{S \stackrel{f_i}{\to} S_i \}_{i \in I}$ a set of [[functions]] out of $S$, the **[[initial topology]]** $\tau_{initial}(\{f_i\}_{i \in I})$ is the topology on $S$ with the [[minimum]] collection of [[open subsets]] such that all $f_i \colon (S,\tau_{initial}(\{f_i\}_{i \in I}))\to X_i$ are [[continuous function|continuous]].

1. For $\{S_i \stackrel{f_i}{\to} S\}_{i \in I}$ a set of [[functions]] into $S$, the **[[final topology]]** $\tau_{final}(\{f_i\}_{i \in I})$ is the topology on $S$ with the [[maximum]] collection of [[open subsets]] such that all $f_i \colon X_i \to (S,\tau_{final}(\{f_i\}_{i \in I}))$ are [[continuous function|continuous]].

=--

+-- {: .num_example #TopologicalSubspace}
###### Example

For $X$ a single topological space, and $\iota_S \colon S \hookrightarrow U(X)$ a subset of its underlying set, the initial topology $\tau_{initial}(\iota_S)$, def. \ref{InitialAndFinalTopologies}, is the [[subspace topology]], making

$$
  \iota_S
  \;\colon\;
  (S, \tau_{initial}(\iota_S))
  \hookrightarrow
  X
$$

a [[topological subspace]] inclusion.

=--

+-- {: .num_example #QuotientTopology}
###### Example

Conversely, for $p_S \colon U(X) \longrightarrow S$ an [[epimorphism]], the final topology $\tau_{final}(p_S)$ on $S$ is the _[[quotient topology]]_.

=--


+-- {: .num_prop #DescriptionOfLimitsAndColimitsInTop}
###### Proposition

Let $I$ be a [[small category]] and let $X_\bullet \colon I \longrightarrow Top$ be an $I$-[[diagram]] in [[Top]] (a [[functor]] from $I$ to $Top$), with components denoted $X_i = (S_i, \tau_i)$, where $S_i \in Set$ and $\tau_i$ a topology on $S_i$. Then:

1. The [[limit]] of $X_\bullet$ exists and is given by [[generalized the|the]] topological space whose underlying set is [[generalized the|the]] limit in [[Set]] of the underlying sets in the diagram, and whose topology is the [[initial topology]], def. \ref{InitialAndFinalTopologies}, for the functions $p_i$ which are the limiting [[cone]] components:

   $$
     \array{
       && \underset{\longleftarrow}{\lim}_{i \in I} S_i
       \\
       & {}^{\mathllap{p_i}}\swarrow && \searrow^{\mathrlap{p_j}}
       \\
       S_i && \underset{}{\longrightarrow} && S_j
     }
     \,.
   $$

   Hence

   $$
     \underset{\longleftarrow}{\lim}_{i \in I} X_i
     \simeq
     \left(\underset{\longleftarrow}{\lim}_{i \in I} S_i,\; \tau_{initial}(\{p_i\}_{i \in I})\right)
   $$

1. The [[colimit]] of $X_\bullet$ exists and is the topological space whose underlying set is the colimit in [[Set]] of the underlying diagram of sets, and whose topology is the [[final topology]], def. \ref{InitialAndFinalTopologies} for the component maps $\iota_i$ of the colimiting [[cocone]]

   $$
     \array{
       S_i && \longrightarrow && S_j
       \\
       & {}_{\mathllap{\iota_i}}\searrow && \swarrow_{\mathrlap{\iota_j}}
       \\
       && \underset{\longrightarrow}{\lim}_{i \in I} S_i
     }
     \,.
   $$

   Hence

   $$
     \underset{\longrightarrow}{\lim}_{i \in I} X_i
     \simeq
     \left(\underset{\longrightarrow}{\lim}_{i \in I} S_i,\; \tau_{final}(\{\iota_i\}_{i \in I})\right)
   $$

=--

(e.g. [Bourbaki 71, section I.4](#Bourbaki71))

+-- {: .proof}
###### Proof

The required [[universal property]] of $\left(\underset{\longleftarrow}{\lim}_{i \in I} S_i,\; \tau_{initial}(\{p_i\}_{i \in I})\right)$ (def. \ref{LimitsAndColimits}) is immediate: for

$$
  \array{
    && (S,\tau)
    \\
    & {}^{\mathllap{f_i}}\swarrow && \searrow^{\mathrlap{f_j}}
    \\
    X_i && \underset{}{\longrightarrow} && X_j
  }
$$

any [[cone]] over the diagram, then by construction there is a unique function of underlying sets $S \longrightarrow \underset{\longleftarrow}{\lim}_{i \in I} S_i$ making the required diagrams commute, and so all that is required is that this unique function is always [[continuous function|continuous]]. But this is precisely what the [[initial topology]] ensures.

The case of the colimit is [[formal dual|formally dual]].

=--




+-- {: .num_example #PointTopologicalSpaceAsEmptyLimit}
###### Example

The limit over the empty diagram in $Top$ is the [[point]] $\ast$ with its unique topology.

=--


+-- {: .num_example #DisjointUnionOfTopologicalSpacesIsCoproduct}
###### Example

For $\{X_i\}_{i \in I}$ a set of topological spaces, their [[coproduct]] $\underset{i \in I}{\sqcup} X_i \in Top$ is their _[[disjoint union]]_.

=--


In particular:

+-- {: .num_example #DiscreteTopologicalSpaceAsCoproduct}
###### Example

For $S \in Set$, the $S$-indexed [[coproduct]] of the point, $\underset{s \in S}{\coprod}\ast $  is the set $S$ itself equipped with the [[final topology]], hence is the [[discrete topological space]] on $S$.

=--

+-- {: .num_example #ProductTopologicalSpace}
###### Example

For $\{X_i\}_{i \in I}$ a set of topological spaces, their [[product]] $\underset{i \in I}{\prod} X_i \in Top$ is the [[Cartesian product]] of the underlying sets equipped with the _[[product topology]]_, also called the _[[Tychonoff product]]_.

In the case that $S$ is a [[finite set]], such as for binary product spaces $X \times Y$, then a [[basis for a topology|sub-basis]] for the product topology is given by the [[Cartesian products]] of the open subsets of (a basis for) each factor space.

=--


+-- {: .num_example #EqualizerInTop}
###### Example

The [[equalizer]] of two [[continuous functions]] $f, g \colon X \stackrel{\longrightarrow}{\longrightarrow} Y$ in $Top$ is the equalizer of the underlying functions of sets

$$
  eq(f,g)
   \hookrightarrow
  S_X
    \stackrel{\overset{f}{\longrightarrow}}{\underset{g}{\longrightarrow}}
  S_Y
$$

(hence the largest subset of $S_X$ on which both functions coincide) and equipped with the [[subspace topology]], example \ref{TopologicalSubspace}.

=--


+-- {: .num_example #CoequalizerInTop}
###### Example

The [[coequalizer]] of two [[continuous functions]] $f, g \colon X \stackrel{\longrightarrow}{\longrightarrow} Y$ in $Top$ is the coequalizer of the underlying functions of sets

$$
  S_X
    \stackrel{\overset{f}{\longrightarrow}}{\underset{g}{\longrightarrow}}
  S_Y
    \longrightarrow
  coeq(f,g)
$$

(hence the [[quotient set]] by the [[equivalence relation]] generated by $f(x) \sim g(x)$ for all $x \in X$)  and equipped with the [[quotient topology]], example \ref{QuotientTopology}.

=--

+-- {: .num_example #PushoutInTop}
###### Example

For

$$
  \array{
     A &\overset{g}{\longrightarrow}& Y
     \\
     {}^{\mathllap{f}}\downarrow
     \\
     X
  }
$$

two [[continuous functions]] out of the same [[domain]], the [[colimit]] under this diagram is also called the _[[pushout]]_, denoted

$$
  \array{
     A &\overset{g}{\longrightarrow}& Y
     \\
     {}^{\mathllap{f}}\downarrow && \downarrow^{\mathrlap{g_\ast f}}
     \\
     X &\longrightarrow& X \sqcup_A Y
     \,.
  }
  \,.
$$

(Here $g_\ast f$ is also called the pushout of $f$, or the _[[base change|cobase change]]_ of $f$ along $g$.)

This is equivalently the [[coequalizer]] of the two morphisms from $A$ to the [[coproduct]] of $X$ with $Y$ (example \ref{DisjointUnionOfTopologicalSpacesIsCoproduct}):

$$
  A
   \stackrel{\longrightarrow}{\longrightarrow}
  X \sqcup Y
   \longrightarrow
  X \sqcup_A Y
  \,.
$$


If $g$ is an inclusion, one also writes $X \cup_f Y$ and calls this the _[[attaching space]]_.

<div style="float:left;margin:0 10px 10px 0;"><img src="http://ncatlab.org/nlab/files/AttachingSpace.jpg" width="450"></div>

By example \ref{CoequalizerInTop} the [[pushout]]/[[attaching space]] is the [[quotient topological space]]

$$
  X \sqcup_A Y \simeq (X\sqcup Y)/\sim
$$

of the [[disjoint union]] of $X$ and $Y$ subject to the [[equivalence relation]] which identifies a point in $X$ with a point in $Y$ if they have the same pre-image in $A$.

(graphics from [Aguilar-Gitler-Prieto 02](#AguilarGitlerPrieto02))

Notice that the defining [[universal property]] of this colimit means that completing the [[span]]

$$
  \array{
    A &\longrightarrow& Y
    \\
    \downarrow
    \\
    X
  }
$$

to a [[commuting square]]

$$
  \array{
    A &\longrightarrow& Y
    \\
    \downarrow && \downarrow
    \\
    X &\longrightarrow& Z
  }
$$

is equivalent to finding a morphism

$$
  X \underset{A}{\sqcup} Y \longrightarrow Z
  \,.
$$



=--

+-- {: .num_example #QuotientSpaceAsPushout}
###### Example

For $A\hookrightarrow X$ a [[topological subspace]] inclusion, example \ref{TopologicalSubspace}, the pushout

$$
  \array{
    A &\hookrightarrow& X
    \\
    \downarrow &(po)& \downarrow
    \\
    \ast &\longrightarrow& X/A
  }
$$

is the [[quotient space]] or _[[cofiber]]_, denoted $X/A$.

=--


+-- {: .num_example #TopologicalnSphereIsPushoutOfBoundaryOfnBallInclusionAlongItself}
###### Example

An important special case of example \ref{PushoutInTop}:

For $n \in \mathbb{N}$ write

* $D^n \coloneqq \{ \vec x\in \mathbb{R}^n | \; {\vert \vec x \vert \leq 1}\} \hookrightarrow \mathbb{R}^n$ for the standard topological [[n-disk]] (equipped with its [[subspace topology]] as a subset of [[Cartesian space]]);

* $S^{n-1} = \partial D^n \coloneqq \{ \vec x\in \mathbb{R}^n | \; {\vert \vec x \vert = 1}\} \hookrightarrow \mathbb{R}^n$ for its [[boundary]], the standard topological [[n-sphere]].

Notice that $S^{-1} = \emptyset$ and that $S^0 = \ast \sqcup \ast$.

Let

$$
  i_n \colon S^{n-1}\longrightarrow D^n
$$

be the canonical inclusion of the standard [[n-sphere|(n-1)-sphere]] as the [[boundary]] of the standard [[n-disk]] (both regarded as [[topological spaces]] with their [[subspace topology]] as subspaces of the [[Cartesian space]] $\mathbb{R}^n$).

<div style="float:left;margin:0 10px 10px 0;">
<img src="http://ncatlab.org/nlab/files/GluingHemispheres.jpg" width="400"></div>

Then the colimit in [[Top]] under the diagram

$$
     D^n \overset{i_n}{\longleftarrow} S^{n-1} \overset{i_n}{\longrightarrow}
     D^n
  \,,
$$

i.e. the [[pushout]] of $i_n$ along itself, is the [[n-sphere]] $S^n$:

$$
  \array{
    S^{n-1} &\overset{i_n}{\longrightarrow}& D^n
    \\
    {}^{\mathllap{i_n}}\downarrow &(po)& \downarrow
    \\
    D^n &\longrightarrow& S^n
  }
  \,.
$$

(graphics from Ueno-Shiga-Morita 95)

=--

Another kind of colimit that will play a role for certain technical constructions is [[transfinite composition]]. First recall

+-- {: .num_defn #PosetsWosetTosetsAndOrdinals}
###### Definition

A _[[partial order]]_ is a [[set]] $S$ equipped with a [[relation]] $\leq$ such that for all elements $a,b,c \in S$

1) ([[reflexive relation|reflexivity]]) $a \leq a$;

2) ([[transitive relation|transitivity]]) if $a \leq b$ and $b \leq c$ then $a \leq c$;

3) ([[antisymmetric relation|antisymmetry]]) if $a\leq b$ and $\b \leq a$ then $a = b$.

This we may and will equivalently think of as a [[category]] with [[objects]] the elements of $S$ and a unique morphism $a \to b$ precisely if $a\leq b$. In particular an order-preserving function between partially ordered sets is equivalently a [[functor]] between their corresponding categories.

A _[[bottom element]]_ $\bot$ in a partial order is one such that $\bot \leq a$ for all a. A _[[top element]]_ $\top$ is one for which $a \leq \top$.

A partial order is a _[[total order]]_ if in addition

4) ([[total relation|totality]]) either $a\leq b$ or $b \leq a$.

A total order is a _[[well order]]_ if in addition

5) ([[well-founded relation|well-foundedness]]) every non-empty subset has a least element.

An _[[ordinal]]_ is the [[equivalence class]] of a well-order.

The _[[successor]]_ of an ordinal is the class of the well-order with a [[top element]] freely adjoined.

A _[[limit ordinal]]_ is one that is not a successor.

=--

+-- {: .num_example #ExamplesOfOrdinals}
###### Example

The finite ordinals are labeled by $n \in \mathbb{N}$, corresponding to the well-orders $\{0 \leq 1 \leq 2 \cdots \leq n-1\}$. Here $(n+1)$ is the successor of $n$. The first non-empty limit ordinal is $\omega = [(\mathbb{N}, \leq)]$.

=--

+-- {: .num_defn #TransfiniteComposition}
###### Definition


Let $\mathcal{C}$ be a [[category]], and let $I \subset Mor(\mathcal{C})$ be a [[class]] of its morphisms.

For $\alpha$ an [[ordinal]] (regarded as a [[category]]), an $\alpha$-indexed _transfinite sequence_ of elements in $I$ is a [[diagram]]

$$
  X_\bullet
    \;\colon\;
  \alpha \longrightarrow \mathcal{C}
$$

such that

1. $X_\bullet$ takes all [[successor]] morphisms $\beta \stackrel{\leq}{\to} \beta + 1$ in $\alpha$ to elements in $I$

   $$
     X_{\beta,\beta + 1} \in I
   $$

1. $X_\bullet$ is _continuous_ in that for every nonzero [[limit ordinal]] $\beta \lt \alpha$, $X_\bullet$ restricted to the [[full subcategory|full-subdiagram]] $\{\gamma \;|\; \gamma \leq \beta\}$ is a [[colimit|colimiting cocone]] in $\mathcal{C}$ for $X_\bullet$ restricted to $\{\gamma \;|\; \gamma \lt \beta\}$.

The corresponding **transfinite composition** is the induced morphism

$$
  X_0 \longrightarrow X_\alpha \coloneqq \underset{\longrightarrow}{\lim}X_\bullet
$$

into the [[colimit]] of the diagram, schematically:

$$
  \array{
    X_0 &\stackrel{X_{0,1}}{\to}& X_1
    &\stackrel{X_{1,2}}{\to}& X_2
    &\to& \cdots
    \\
    & \searrow & \downarrow & \swarrow & \cdots
    \\
    &&
    X_\alpha
  }
  \,.
$$

=--


We now turn to the discussion of [[mapping spaces]]/[[exponential objects]].


+-- {: .num_defn #CompactOpenTopology}
###### Definition

For $X$ a [[topological space]] and $Y$ a [[locally compact topological space]] (in that for every point, every [[neighbourhood]] contains a [[compact topological space|compact]] neighbourhood), the **[[mapping space]]**

$$
  X^Y \in Top
$$

is the [[topological space]]

* whose underlying set is the set $Hom_{Top}(Y,X)$ of [[continuous
functions]] $Y \to X$,

* whose [[open subsets]] are [[unions]] of [[finitary intersections]] of the following [[topological base|subbase]] elements of standard open subsets:

  the standard open subset $U^K \subset Hom_{Top}(Y,X)$ for

  * $K \hookrightarrow Y$ a [[compact topological space]] subset

  * $U \hookrightarrow X$ an [[open subset]]

  is the subset of all those [[continuous functions]] $f$ that fit into a [[commuting diagram]] of the form

  $$
    \array{
       K &\hookrightarrow& Y
       \\
       \downarrow && \downarrow^{\mathrlap{f}}
       \\
       U &\hookrightarrow& X
    }
    \,.
  $$

Accordingly this is called the _[[compact-open topology]]_ on the set of functions.

The construction extends to a [[functor]]

$$
  (-)^{(-)} \;\colon\; Top_{lc}^{op} \times Top \longrightarrow Top
  \,.
$$

=--

+-- {: .num_prop #MappingTopologicalSpaceIsExponentialObject}
###### Proposition

For $X$ a [[topological space]] and $Y$ a [[locally compact topological space]] (in that for each point, each open neighbourhood contains a [[compact subset|compact]] [[neighbourhood]]), the **topological [[mapping space]]** $X^Y$ from def. \ref{CompactOpenTopology} is an [[exponential object]], i.e. the functor $(-)^Y$ is [[right adjoint]] to the product functor $Y \times (-)$: there is a [[natural bijection]]

$$
  Hom_{Top}(Z \times Y, X) \simeq Hom_{Top}(Z, X^Y)
$$

between continuous functions out of any [[product topological space]] of $Y$ with any $Z \in Top$ and continuous functions from $Z$ into the mapping space.

=--

A proof is spelled out [here](compact-open+topology#GivesExponentialObject)
(or see e.g. [Aguilar-Gitler-Prieto 02, prop. 1.3.1](#AguilarGitlerPrieto02)).

+-- {: .num_remark #UseOfHausdorffnessInCOTopology}
###### Remark

In the context of prop. \ref{MappingTopologicalSpaceIsExponentialObject} it is often assumed that $Y$ is also a [[Hausdorff topological space]]. But this is not necessary. What assuming Hausdorffness only achieves is that all alternative definitions of "locally compact" become equivalent to the one that is needed for the proposition: for every point, every open neighbourhood contains a compact neighbourhood.

=--


+-- {: .num_remark #ProblemWithExponentialsInTop}
###### Remark

Proposition \ref{MappingTopologicalSpaceIsExponentialObject} fails in general if $Y$ is not locally compact. Therefore the plain category [[Top]] of all topological spaces is not a [[Cartesian closed category]].

This is no problem for the construction of the homotopy theory of topological spaces as such, but it becomes a technical nuisance for various constructions that one would like to perform within that homotopy theory. For instance on general [[pointed topological spaces]] the [[smash product]] is in general not [[associativity|associative]].

On the other hand, without changing any of the following discussion one may just pass to a more [[convenient category of topological spaces]] such as notably the [[full subcategory]] of [[compactly generated topological spaces]] $Top_{cg} \hookrightarrow Top$ (def. \ref{kTop}) which is [[Cartesian closed category|Cartesian closed]]. This we turn to [below](#ModelStructureOnCompactlyGeneratedTopologicalSpaces).

=--




### Homotopy

The fundamental concept of [[homotopy theory]] is clearly that of _[[homotopy]]_. In the context of [[topological spaces]] this is about [[continuous function|continuous]] deformations of [[continuous functions]] parameterized by the standard [[closed interval]]:

+-- {: .num_defn #TopologicalInterval}
###### Definition

Write

$$
  I \coloneqq [0,1] \hookrightarrow \mathbb{R}
$$

for the standard [[topological interval]], a [[compact topological space|compact]] [[connected topological space|connected]] [[topological subspace]] of the [[real line]].

Equipped with the canonical inclusion of its two endpoints

$$
  \ast \sqcup \ast \stackrel{(\delta_0,\delta_1)}{\longrightarrow} I \stackrel{\exists !}{\longrightarrow} \ast
$$

this is the standard [[interval object]] in [[Top]].

For $X \in Top$, the [[product topological space]] $X\times I$, example \ref{ProductTopologicalSpace}, is called the standard _[[cylinder object]]_ over $X$. The endpoint inclusions of the interval make it factor the [[codiagonal]] on $X$

$$
  \nabla_X
    \;\colon\;
  X \sqcup X
  \stackrel{((id,\delta_0),(id,\delta_1))}{\longrightarrow}
  X \times I
  \longrightarrow
  X
  \,.
$$

=--


+-- {: .num_defn #LeftHomotopy}
###### Definition

For $f,g\colon X \longrightarrow Y$ two [[continuous functions]] between [[topological spaces]] $X,Y$, then a **[[left homotopy]]**

$$
  \eta \colon f \,\Rightarrow_L\, g
$$

is a [[continuous function]]

$$
  \eta \;\colon\; X \times I \longrightarrow Y
$$


out of the standard [[cylinder object]] over $X$, def. \ref{TopologicalInterval}, such that this fits into a [[commuting diagram]] of the form

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

+-- {: .num_example #PathsAsLeftHomotopyBetweenPoints}
###### Example

Let $X$ be a [[topological space]] and let $x,y \in X$ be two of its points, regarded as functions $x,y \colon \ast \longrightarrow X$ from the point to $X$. Then a left homotopy, def. \ref{LeftHomotopy}, between these two functions is a commuting diagram of the form

$$
  \array{
     \ast
     \\
     {}^{\mathllap{\delta_0}}\downarrow & \searrow^{\mathrlap{x}}
     \\
     I &\stackrel{\eta}{\longrightarrow}& X
     \\
     {}^{\mathllap{\delta_1}}\uparrow & \nearrow_{\mathrlap{y}}
     \\
     \ast
  }
  \,.
$$

This is simply a continuous path in $X$ whose endpoints are $x$ and $y$.

=--

For instance:

+-- {: .num_example #StandardContractionOfStandardInterval}
###### Example

Let

$$
  const_0 \;\colon\; I \longrightarrow \ast \overset{\delta_0}{\longrightarrow} I
$$

be the [[continuous function]] from the standard interval $I = [0,1]$ to itself that is constant on the value 0. Then there is a left homotopy, def. \ref{LeftHomotopy}, from the identity function

$$
  \eta \;\colon\; id_I \Rightarrow const_0
$$

given by

$$
  \eta(x,t) \coloneqq x(1-t)
  \,.
$$


=--



A key application of the concept of left homotopy is to the definition of [[homotopy groups]]:

+-- {: .num_defn #HomotopyGroupsOftopologicalSpaces}
###### Definition

For $X$ a [[topological space]], then its set $\pi_0(X)$
of _[[connected components]]_, also called the **0-th homotopy set**,
is the set of
[[left homotopy]]-[[equivalence classes]] (def. \ref{LeftHomotopy}) of points $x \colon \ast \to X$, hence the set of path-connected components of $X$ (example \ref{PathsAsLeftHomotopyBetweenPoints}). By [[composition]] this extends to a [[functor]]

$$
  \pi_0 \colon Top \longrightarrow Set
  \,.
$$

For $n \in \mathbb{N}$, $n \geq 1$ and for $x \colon \ast \to X$
any point, the $n$th **[[homotopy group]]** $\pi_n(X,x)$ of $X$ at $x$
is the [[group]]

* whose underlying [[set]] is the set of [[left homotopy]]-[[equivalence classes]] of maps $I^n \longrightarrow X$ that take the [[boundary]] of $I^n$ to $x$ and where the left homotopies $\eta$ are constrained to be constant on the boundary;

* whose [[group]] product operation takes $[\alpha \colon I^n \to X]$ and $[\beta \colon I^n \to X]$ to $[\alpha \cdot \beta]$ with

$$
  \alpha \cdot \beta
  \;\colon\;

  I^n
  \stackrel{\simeq}{\longrightarrow}
  I^n \underset{I^{n-1}}{\sqcup} I^n
  \stackrel{(\alpha,\beta)}{\longrightarrow}
  X
  \,,
$$

where the first map is a [[homeomorphism]] from the unit $n$-[[cube]] to the $n$-cube with one side twice the unit length (e.g. $(x_1, x_2, x_3, \cdots) \mapsto (2 x_1, x_2, x_3, \cdots)$).

By [[composition]], this construction extends to a [[functor]]

$$
  \pi_{\bullet \geq 1}
    \;\colon\;
  Top^{\ast/}
   \longrightarrow
  Grp^{\mathbb{N}_{\geq 1}}
$$

from [[pointed topological spaces]] to [[graded object|graded]] [[groups]].

=--

Notice that often one writes the value of this functor on a morphism $f$ as $f_\ast = \pi_\bullet(f)$.

+-- {: .num_remark}
###### Remark

At this point we don't go further into the abstract reason why def. \ref{HomotopyGroupsOftopologicalSpaces} yields group structure above degree 0, which is that [[positive dimension spheres are H-cogroup objects]]. But this is important, for instance in the proof of the  [[Brown representability theorem]]. See the section _[Brown representability theorem](Introduction+to+Stable+homotopy+theory+--+S#BrownRepresentabilityTheorem)_ in [[Introduction to Stable homotopy theory -- S|Part S]].

=--

+-- {: .num_defn #HomotopyEquivalence}
###### Definition

A [[continuous function]] $f \;\colon\; X \longrightarrow Y$
is called a **[[homotopy equivalence]]** if there exists a
continuous function the other way around,
$g \;\colon\; Y \longrightarrow X$, and [[left homotopies]], def. \ref{LeftHomotopy}, from the two composites to the identity:

$$
  \eta_1 \;\colon\; f\circ g \Rightarrow_L id_Y
$$

and

$$
  \eta_2 \;\colon\; g\circ f \Rightarrow_L id_X
  \,.
$$

If here $\eta_2$ is constant along $I$, $f$ is said to exhibit $X$ as a **[[deformation retract]]** of $Y$.

=--

+-- {: .num_example #ProjectionFromStandardCylinderIsHomotopyEquivalence}
###### Example

For $X$ a [[topological space]] and $X \times I$ its standard [[cylinder object]] of def. \ref{TopologicalInterval}, the projection $p \colon X \times I \longrightarrow X$ and the inclusion $(id, \delta_0) \colon X \longrightarrow X\times I$ are [[homotopy equivalences]], def. \ref{HomotopyEquivalence}, and in fact are homotopy inverses to each other:

The composition

$$
  X \overset{(id,\delta_0)}{\longrightarrow} X\times I \overset{p}{\longrightarrow} X
$$

is immediately the identity on $X$ (i.e. homotopic to the identity by a trivial homotopy), while the composite

$$
  X
    \times I \overset{p}{\longrightarrow}
  X
    \overset{(id, \delta_0)}{\longrightarrow}
  X\times I
$$

is homotopic to the identity on $X \times I$ by a homotopy that is pointwise in $X$ that of example \ref{StandardContractionOfStandardInterval}.


=--


+-- {: .num_defn #WeakHomotopyEquivalenceOfTopologicalSpaces}
###### Definition

A [[continuous function]] $f \colon X \longrightarrow Y$ is called  a **[[weak homotopy equivalence]]** if its image under all the [[homotopy group]] functors of def. \ref{HomotopyGroupsOftopologicalSpaces} is an [[isomorphism]], hence if

$$
  \pi_0(f) \;\colon\; \pi_0(X) \stackrel{\simeq}{\longrightarrow} \pi_0(Y)
$$

and for all $x \in X$ and all $n \geq 1$

$$
  \pi_n(f) \;\colon\; \pi_n(X,x) \stackrel{\simeq}{\longrightarrow} \pi_n(Y,f(x))
  \,.
$$


=--

+-- {: .num_prop #TopologicalHomotopyEquivalencesAreWeakHomotopyEquivalences}
###### Proposition

Every [[homotopy equivalence]], def. \ref{HomotopyEquivalence}, is a weak homotopy equivalence, def. \ref{WeakHomotopyEquivalenceOfTopologicalSpaces}.

In particular a [[deformation retraction]], def. \ref{HomotopyEquivalence}, is a weak homotopy equivalence.

=--

+-- {: .proof}
###### Proof

First observe that for all $X\in$ [[Top]] the inclusion maps

$$
  X \overset{(id,\delta_0)}{\longrightarrow} X \times I
$$

into the standard [[cylinder object]], def. \ref{TopologicalInterval}, are weak homotopy equivalences: by postcomposition with the contracting homotopy of the interval from example \ref{StandardContractionOfStandardInterval} all homotopy groups of $X \times I$ have representatives that factor through this inclusion.

Then given a general [[homotopy equivalence]], apply the homotopy groups functor to the corresponding homotopy diagrams (where for the moment we notationally suppress the choice of basepoint for readability) to get two commuting diagrams

$$
  \array{
     \pi_\bullet(X)
     \\
     {}^{\mathllap{\pi_\bullet(id,\delta_0)}}\downarrow & \searrow^{\mathrlap{\pi_\bullet(f)\circ \pi_\bullet(g)}}
     \\
     \pi_\bullet(X \times I) &\stackrel{\pi_\bullet(\eta)}{\longrightarrow}& \pi_\bullet(X)
     \\
     {}^{\mathllap{\pi_\bullet(id,\delta_1)}}\uparrow & \nearrow_{\mathrlap{\pi_\bullet(id)}}
     \\
     \pi_\bullet(X)
  }
  \;\;\;\;\;\;\;
  \,,
  \;\;\;\;\;\;\;
  \array{
     \pi_\bullet(Y)
     \\
     {}^{\mathllap{\pi_\bullet(id,\delta_0)}}\downarrow & \searrow^{\mathrlap{\pi_\bullet(g)\circ \pi_\bullet(f)}}
     \\
     \pi_\bullet(Y \times I) &\stackrel{\pi_\bullet(\eta)}{\longrightarrow}& \pi_\bullet(Y)
     \\
     {}^{\mathllap{\pi_\bullet(id,\delta_1)}}\uparrow & \nearrow_{\mathrlap{\pi_\bullet(id)}}
     \\
     \pi_\bullet(Y)
  }
  \,.
$$

By the previous observation, the vertical morphisms here are isomorphisms, and hence these diagrams exhibit $\pi_\bullet(f)$ as the inverse of $\pi_\bullet(g)$, hence both as isomorphisms.

=--

+-- {: .num_remark #NotEveryHomotopyEquivalenceIsAWeakHomotopyEquivalence}
###### Remark

The converse of prop. \ref{TopologicalHomotopyEquivalencesAreWeakHomotopyEquivalences} is not true generally: not every [[weak homotopy equivalence]] between topological spaces is a [[homotopy equivalence]].  (For an example with full details spelled out see for instance Fritsch, Piccinini: "Cellular Structures in Topology", p. 289-290).

However, as we will discuss below, it turns out that

1. every weak homotopy equivalence between [[CW-complexes]] is a homotopy equivalence ([[Whitehead's theorem]], cor. \ref{WhiteheadTheorem});

1. every topological space is connected by a weak homotopy equivalence to a CW-complex ([[CW approximation]], remark \ref{EveryTopologicalSpaceWeaklyEquivalentToACWComplex}).

=--


+-- {: .num_example #FactoringTopologicalCodiagonalThroughCylinder}
###### Example

For $X\in Top$, the projection $X\times I \longrightarrow X$
from the [[cylinder object]] of $X$, def. \ref{TopologicalInterval},
is a [[weak homotopy equivalence]], def. \ref{WeakHomotopyEquivalenceOfTopologicalSpaces}.  This means that the factorization

$$
  \nabla_X
    \;\colon\;
  X \sqcup X
    \stackrel{}{\hookrightarrow}
  X\times I
    \stackrel{\simeq}{\longrightarrow}
  X
$$

of the [[codiagonal]] $\nabla_X$ in def. \ref{TopologicalInterval}, which in general is far from being a [[monomorphism]], may be thought of as factoring it through a monomorphism after replacing $X$, up to weak homotopy equivalence, by $X\times I$.


In fact, further below (prop. \ref{StandardContractionOfStandardInterval}) we see that $X \sqcup X \to X \times I$ has better properties than the generic monomorphism has, in particular better homotopy invariant properties:
it has the [[left lifting property]] against all [[Serre fibrations]] $ E \stackrel{p}{\longrightarrow} B$ that are also [[weak homotopy equivalences]].

=--

Of course the concept of left homotopy in def. \ref{LeftHomotopy} is accompanied by a concept of _[[right homotopy]]_. This we turn to now.



+-- {: .num_defn #TopologicalPathSpace}
###### Definition
**([[path space]])**

For $X$ a [[topological space]], its **standard topological [[path space object]]** is the topological [[path space]], hence the [[mapping space]] $X^I$, prop. \ref{MappingTopologicalSpaceIsExponentialObject}, out of the standard interval $I$ of def. \ref{TopologicalInterval}.


=--

+-- {: .num_example}
###### Example

The endpoint inclusion into the standard interval, def. \ref{TopologicalInterval}, makes the path space $X^I$ of def. \ref{TopologicalPathSpace} factor the [[diagonal]] on $X$ through the inclusion of constant paths and the endpoint evaluation of paths:


$$
  \Delta_X
  \;\colon\;
  X \stackrel{X^{I \to \ast}}{\longrightarrow} X^I \stackrel{X^{\ast \sqcup \ast \to I}}{\longrightarrow} X \times X
  \,.
$$

This is the [[formal dual]] to example \ref{TopologicalInterval}. As in that example, below we will see (prop. \ref{TopologicalPathSpaceIsGoodPathSpaceObject}) that this factorization has good properties, in that

1. $X^{I \to \ast}$ is a [[weak homotopy equivalence]];

1. $X^{\ast \sqcup \ast \to I}$ is a [[Serre fibration]].

So while in general the [[diagonal]] $\Delta_X$ is far from being an [[epimorphism]] or even just a [[Serre fibration]], the factorization through the [[path space object]] may be thought of as replacing $X$, up to weak homotopy equivalence, by its path space, such as to turn its diagonal into a Serre fibration after all.

=--

+-- {: .num_defn }
###### Definition

For $f,g\colon X \longrightarrow Y$ two [[continuous functions]] between [[topological spaces]] $X,Y$, then a **[[right homotopy]]** $f \Rightarrow_R g$ is a [[continuous function]]

$$
  \eta \;\colon\; X \longrightarrow Y^I
$$

into the [[path space object]] of $X$, def. \ref{TopologicalPathSpace}, such that this fits into a [[commuting diagram]] of the form

$$
  \array{
    && Y
    \\
    & {}^{\mathllap{f}}\nearrow & \uparrow^{\mathrlap{X^{\delta_0}}}
    \\
    X &\stackrel{\eta}{\longrightarrow}& Y^I
    \\
    & {}_{\mathllap{g}}\searrow & \downarrow^{\mathrlap{Y^{\delta_1}}}
    \\
    && Y
  }
  \,.
$$

=--



### Cell complexes

We consider topological spaces that are built consecutively by [[attaching space|attaching]] basic cells.

+-- {: .num_defn #TopologicalGeneratingCofibrations}
###### Definition

Write

$$
  I_{Top}
    \coloneqq
  \left\{
    S^{n-1} \stackrel{\iota_n}{\hookrightarrow} D^{n}
  \right\}_{n \in \mathbb{N}}
  \;
   \subset
  Mor(Top)
$$

for the set of canonical [[boundary]] inclusion maps of the standard [[n-disks]], example \ref{TopologicalnSphereIsPushoutOfBoundaryOfnBallInclusionAlongItself}. This going to be called the set of standard **topological [[generating cofibrations]]**.

=--

+-- {: .num_defn #TopologicalCellComplex}
###### Definition

For $X \in Top$ and for $n \in \mathbb{N}$, an **$n$-cell attachment** to $X$ is the [[pushout]] ("[[attaching space]]", example \ref{PushoutInTop}) of a generating cofibration, def. \ref{TopologicalGeneratingCofibrations}

$$
  \array{
    S^{n-1} &\stackrel{\phi}{\longrightarrow}& X
    \\
    {}^{\mathllap{\iota_n}}\downarrow &(po)& \downarrow
    \\
    D^n &\longrightarrow& X \underset{S^{n-1}}{\sqcup} D^n & = X \cup_\phi D^n
  }
$$

along some [[continuous function]] $\phi$.

A continuous function $f \colon X \longrightarrow Y$ is called a **topological [[relative cell complex]]** if it is exhibited by a (possibly infinite) sequence of cell [[attaching space|attachments]] to $X$, in that it is a [[transfinite composition]] (def. \ref{TransfiniteComposition}) of [[pushouts]] (example \ref{PushoutInTop})

$$
  \array{
    \underset{i}{\coprod} S^{n_i - 1} &\longrightarrow& X_{k}
    \\
    {}^{\mathllap{\underset{i}{\coprod}\iota_{n_i}}}\downarrow
     &(po)&
    \downarrow
    \\
    \underset{i}{\coprod} D^{n_i} &\longrightarrow& X_{k+1}
  }
$$

of [[coproducts]] (example \ref{DisjointUnionOfTopologicalSpacesIsCoproduct}) of [[generating cofibrations]] (def. \ref{TopologicalGeneratingCofibrations}).

A topological space $X$ is a **[[cell complex]]** if $\emptyset \longrightarrow X$ is a relative cell complex.

A relative cell complex is called a **finite relative cell complex** if it is obtained from a [[finite number]] of cell attachments.

A (relative) cell complex is called a (relative) **[[CW-complex]]** if the above transfinite composition is countable

$$
  \array{
    X = X_0 &\longrightarrow& X_1 &\longrightarrow& X_2 &\longrightarrow& \cdots
    \\
    & {}_{\mathllap{f}}\searrow & \downarrow & \swarrow && \cdots
    \\
    && Y = \underset{\longrightarrow}{\lim} X_\bullet
  }
$$

and if $X_k$ is obtained from $X_{k-1}$ by attaching cells precisely only of [[dimension]] $k$.

=--

+-- {: .num_remark}
###### Remark

Strictly speaking a relative cell complex, def. \ref{TopologicalCellComplex}, is a function $f\colon X \to Y$, _together_ with its cell structure, hence together with the information of the pushout diagrams and the transfinite composition of the pushout maps that exhibit it.

In many applications, however,  all that matters is that there is _some_ (relative) cell decomposition, and then one tends to speak loosely and mean by a (relative) cell complex only a (relative) topological space that admits some cell decomposition.

=--

The following lemma \ref{CompactSubsetsAreSmallInCellComplexes}, together with lemma \ref{AcyclicSerreFibrationsAreTheJTopFibrations} below are the only two statements of the entire development here that involve the [[concrete particular]] nature of [[topological spaces]] ("[[point-set topology]]"), everything beyond that is [[general abstract]] homotopy theory.

+-- {: .num_lemma #CompactSubsetsAreSmallInCellComplexes}
###### Lemma

Assuming the [[axiom of choice]] and the [[law of excluded middle]],
every [[compact topological space|compact]] [[topological subspace|subspace]] of a topological [[cell complex]], def. \ref{TopologicalCellComplex}, intersects the [[interior]] of a [[finite number]] of cells.

=--

(e.g. [Hirschhorn 15, section 3.1](#Hirschhorn15))

+-- {: .proof}
###### Proof

So let $Y$ be a topological cell complex and $C \hookrightarrow Y$ a [[compact topological space|compact]] [[topological subspace|subspace]]. Define a subset

$$
  P \subset Y
$$

by _choosing_ one point in the [[interior]] of the intersection with $C$ of each cell of $Y$ that intersects $C$.

It is now sufficient to show that $P$ has no [[accumulation point]]. Because, by the [[compact topological space|compactness]] of $X$, every non-finite subset of $C$ does have an accumulation point, and hence the lack of such shows that $P$ is a [[finite set]] and hence that $C$ intersects the interior of finitely many cells of $Y$.

To that end, let $c\in C$ be any point. If $c$ is a 0-cell in $Y$, write $U_c \coloneqq \{c\}$. Otherwise write $e_c$ for the unique cell of $Y$ that contains $c$ in its [[interior]]. By construction, there is exactly one point of $P$ in the interior of $e_c$. Hence there is an [[open neighbourhood]] $c \in U_c \subset e_c$ containing no further points of $P$ beyond possibly $c$ itself, if $c$ happens to be that single point of $P$ in $e_c$.

It is now sufficient to show that $U_c$ may be enlarged to an open subset $\tilde U_c$ of $Y$ containing no point of $P$, except for possibly $c$ itself, for that means that $c$ is not an accumulation point of $P$.

To that end, let $\alpha_c$ be the [[ordinal]] that labels the stage $Y_{\alpha_c}$ of the [[transfinite composition]] in the [[cell complex]]-presentation of $Y$ at which the cell $e_c$ above appears. Let $\gamma$ be the ordinal of the full cell complex. Then define the set

$$
  T
  \coloneqq
  \left\{
    \;
    (\beta, U)
    \;|\;
    \alpha_c \leq \beta \leq \gamma
    \;\,,\;
    U \underset{open}{\subset} Y_\beta
    \;\,,\;
    U \cap Y_\alpha = U_c
    \;\,,\;
    U \cap P \in \{ \emptyset, \{c\} \}
    \;
  \right\}
  \,,
$$

and regard this as a [[partially ordered set]] by declaring a partial ordering via

$$
  (\beta_1, U_1) \lt (\beta_2, U_2)
  \;\;\;\;
  \Leftrightarrow
  \;\;\;\;
  \beta_1 \lt \beta_2
  \;\,,\;
  U_2 \cap Y_{\beta_1} = U_1
  \,.
$$

This is set up such that every element $(\beta, U)$ of $T$ with $\beta$ the maximum value $\beta = \gamma$ is an extension $\tilde U_c$ that we are after.

Observe then that for $(\beta_s, U_s)_{s\in S}$ a chain in $(T,\lt)$ (a subset on which the relation $\lt$ restricts to a [[total order]]), it has an upper bound in $T$ given by the [[union]] $({\cup}_s \beta_s ,\cup_s U_s)$. Therefore [[Zorn's lemma]] applies, saying that $(T,\lt)$ contains a [[maximal element]] $(\beta_{max}, U_{max})$.

Hence it is now sufficient to show that $\beta_{max} = \gamma$. We argue this by showing that assuming $\beta_{\max}\lt \gamma$ leads to a contradiction.

So assume $\beta_{max}\lt \gamma$. Then to construct an  element of $T$ that is larger than $(\beta_{max},U_{max})$, consider for each cell $d$ at stage $Y_{\beta_{max}+1}$ its [[attaching map]] $h_d \colon S^{n-1} \to Y_{\beta_{max}}$ and the corresponding preimage open set $h_d^{-1}(U_{max})\subset S^{n-1}$. Enlarging all these  preimages to open subsets of $D^n$ (such that their image back in $X_{\beta_{max}+1}$ does not contain $c$), then $(\beta_{max}, U_{max}) \lt (\beta_{max}+1, \cup_d U_d )$. This is a contradiction. Hence $\beta_{max} = \gamma$, and we are done.

=--


It is immediate and useful to generalize the concept of topological cell complexes as follows.

+-- {: .num_defn #TopologicalCCellComplex}
###### Definition

For $\mathcal{C}$ any category and for $K \subset Mor(\mathcal{C})$ any sub-[[class]] of its morphisms, a **relative $K$-cell complex** is a morphism in $\mathcal{C}$ which is a [[transfinite composition]] (def. \ref{TransfiniteComposition}) of [[pushouts]] of [[coproducts]] of morphisms in $K$.

=--

+-- {: .num_defn #TopologicalGeneratingAcyclicCofibrations}
###### Definition

Write

$$
  J_{Top}
    \coloneqq
  \left\{
    D^n \stackrel{(id,\delta_0)}{\hookrightarrow} D^n \times I
  \right\}_{n \in \mathbb{N}}
  \;
  \subset Mor(Top)
$$

for the [[set]] of inclusions of the topological [[n-disks]], def. \ref{TopologicalGeneratingCofibrations}, into their [[cylinder objects]], def. \ref{TopologicalInterval}, along (for definiteness) the left endpoint inclusion.

These inclusions are similar to the standard topological [[generating cofibrations]] $I_{Top}$ of def. \ref{TopologicalGeneratingCofibrations}, but in contrast to these they are "acyclic" (meaning: trivial on homotopy classes of maps from "cycles" given by [[n-spheres]]) in that they are [[weak homotopy equivalences]] (by prop. \ref{TopologicalHomotopyEquivalencesAreWeakHomotopyEquivalences}).

Accordingly, $J_{Top}$ is to be called the set of standard **topological [[generating acyclic cofibrations]]**.

=--

+-- {: .num_lemma #CylinderOverCWComplexIsJTopRelativeCellComplex}
###### Lemma

For $X$ a [[CW-complex]] (def. \ref{TopologicalCellComplex}), then its inclusion $X \overset{(id, \delta_0)}{\longrightarrow} X\times I$ into its standard [[cylinder object|cylinder]] (def. \ref{TopologicalInterval}) is a $J_{Top}$-[[relative cell complex]] (def. \ref{TopologicalCCellComplex}, def. \ref{TopologicalGeneratingAcyclicCofibrations}).

=--

+-- {: .proof}
###### Proof

First erect a cylinder over all 0-cells

$$
  \array{
     \underset{x \in X_0}{\coprod} D^0 &\longrightarrow& X
     \\
     \downarrow &(po)& \downarrow
     \\
     \underset{x\in X_0}{\coprod} D^1 &\longrightarrow& Y_1
  }
  \,.
$$

Assume then that the cylinder over all $n$-cells of $X$ has been erected using attachment from $J_{Top}$. Then the union of any $(n+1)$-cell $\sigma$ of $X$ with the cylinder over its boundary is homeomorphic to $D^{n+1}$ and is like the cylinder over the cell "with end and interior removed". Hence via [[attaching space|attaching]] along $D^{n+1} \to D^{n+1}\times I$ the cylinder over $\sigma$ is erected.

=--


+-- {: .num_lemma #TopologicalGeneratingAcyclicCofibrationsAreRelativeCellComplexes}
###### Lemma

The maps $D^n \hookrightarrow D^n \times I$ in def. \ref{TopologicalGeneratingAcyclicCofibrations} are finite [[relative cell complexes]], def. \ref{TopologicalCellComplex}. In other words, the elements of $J_{Top}$ are $I_{Top}$-[[relative cell complexes]].

=--


+-- {: .proof}
###### Proof

There is a [[homeomorphism]]

$$
  \array{
     D^n & = & D^n
     \\
     {}^{\mathllap{(id,\delta_0)}}\downarrow  && \downarrow
     \\
     D^n \times I &\simeq& D^{n+1}
  }
$$

such that the map on the right is the inclusion of one hemisphere into the [[boundary]] [[n-sphere]] of $D^{n+1}$. This inclusion is the result of [[attaching space|attaching]] two cells:

$$
  \array{
    S^{n-1} &\overset{\iota_n}{\longrightarrow}& D^n
    \\
    {}^{\mathllap{\iota_n}}\downarrow &(po)& \downarrow
    \\
    D^n &\longrightarrow& S^{n}
    \\
    && \downarrow^{=}
    \\
    S^n &\overset{id}{\longrightarrow}& S^n
    \\
    {}^{\mathllap{\iota_{n+1}}}\downarrow &(po)& \downarrow
    \\
    D^{n+1} &\underset{id}{\longrightarrow}& D^{n+1}
  }
  \,.
$$

here the top pushout is the one from example \ref{TopologicalnSphereIsPushoutOfBoundaryOfnBallInclusionAlongItself}.

=--

+-- {: .num_lemma #JTopRelativeCellComplexesAreWeakHomotopyEquivalences}
###### Lemma

Every $J_{Top}$-[[relative cell complex]] (def. \ref{TopologicalGeneratingAcyclicCofibrations}, def. \ref{TopologicalCCellComplex}) is a [[weak homotopy equivalence]], def. \ref{WeakHomotopyEquivalenceOfTopologicalSpaces}.

=--

+-- {: .proof}
###### Proof

Let $X \longrightarrow \hat X = \underset{\longleftarrow}{\lim}_{\beta \leq \alpha} X_\beta$ be a $J_{Top}$-[[relative cell complex]].

First observe that with the elements $D^n \hookrightarrow D^n \times I$ of $J_{Top}$ being [[homotopy equivalences]] for all $n \in \mathbb{N}$ (by example \ref{ProjectionFromStandardCylinderIsHomotopyEquivalence}), each of the stages $X_{\beta} \longrightarrow X_{\beta + 1}$ in the relative cell complex is also a homotopy equivalence. We make this fully explicit:

By definition, such a stage is a [[pushout]] of the form

$$
  \array{
     \underset{i \in I}{\sqcup} D^{n_i}
     &\longrightarrow&
     X_\beta
     \\
     {}^{\mathllap{\underset{i \in I}{\sqcup} (id, \delta_0)} }\downarrow
      &(po)&
     \downarrow
     \\
     \underset{i \in I}{\sqcup} D^{n_i} \times I
     &\longrightarrow&
     X_{\beta + 1}
  }
  \,.
$$

Then the fact that the projections $p_{n_i} \colon D^{n_i} \times I \to D^{n_i}$ are strict left inverses to the inclusions $(id, \delta_0)$ gives a [[commuting square]] of the form

$$
  \array{
     \underset{i \in I}{\sqcup} D^{n_i}
     &\longrightarrow&
     X_\beta
     \\
     {}^{\mathllap{\underset{i \in I}{\sqcup} (id, \delta_0)} }\downarrow
       &&
     \downarrow^{\mathrlap{id}}
     \\
     \underset{i \in I}{\sqcup} D^{n_i} \times I
     \\
     {}^{\mathllap{\underset{i \in I}{\sqcup} p_{n_i} }}\downarrow && \downarrow
     \\
     \underset{i \in I}{\sqcup} D^{n_i}
       &\longrightarrow&
     X_\beta
  }
$$

and so the [[universal property]] of the [[colimit]] ([[pushout]]) $X_{\beta + 1}$ gives a factorization of the identity morphism on the right through $X_{\beta + 1}$

$$
  \array{
     \underset{i \in I}{\sqcup} D^{n_i}
     &\longrightarrow&
     X_\beta
     \\
     {}^{\mathllap{\underset{i \in I}{\sqcup} (id, \delta_0)} }\downarrow
       &&
     \downarrow^{}
     \\
     \underset{i \in I}{\sqcup} D^{n_i} \times I
       &\longrightarrow&
     X_{\beta + 1}
     \\
     {}^{\mathllap{\underset{i \in I}{\sqcup} p_{n_i} }}\downarrow
       &&
     \downarrow
     \\
     \underset{i \in I}{\sqcup} D^{n_i}
       &\longrightarrow&
     X_\beta
  }
$$

which exhibits $X_{\beta + 1} \to X_\beta$ as a strict left inverse to $X_{\beta} \to X_{\beta + 1}$. Hence it is now sufficient to show that this is also a homotopy right inverse.

To that end, let

$$
  \eta_{n_i} \colon D^{n_i}\times I \longrightarrow D^{n_i} \times I
$$

be the [[left homotopy]] that exhibits $p_{n_i}$ as a homotopy right inverse to $p_{n_i}$ by example \ref{ProjectionFromStandardCylinderIsHomotopyEquivalence}. For each $t \in [0,1]$ consider the [[commuting square]]

$$
  \array{
    \underset{i \in I}{\sqcup} D^{n_i}
      &\longrightarrow&
    X_\beta
    \\
    \downarrow && \downarrow
    \\
    \underset{i \in I}{\sqcup} D^{n_i} \times I
    && X_{\beta + 1}
    \\
    {}^{\mathllap{\eta_{n_i}(-,t)}}\downarrow && \downarrow^{\mathrlap{id}}
    \\
    \underset{i \in I}{\sqcup} D^{n_i} \times I
     &\longrightarrow&
    X_{\beta + 1}
  }
  \,.
$$

Regarded as a [[cocone]] under the [[span]] in the top left, the [[universal property]] of the [[colimit]] ([[pushout]]) $X_{\beta + 1}$ gives a continuous function

$$
  \eta(-,t) \;\colon\; X_{\beta + 1} \longrightarrow X_{\beta + 1}
$$

for each $t \in [0,1]$. For $t = 0$ this construction reduces to the provious one in that $\eta(-,0) \colon X_{\beta +1 } \to X_{\beta} \to X_{\beta + 1}$ is the composite which we need to homotope to the identity; while $\eta(-,1)$ is the identity.
Since $\eta(-,t)$ is clearly also continuous in $t$ it constitutes a continuous function

$$
  \eta \;\colon\; X_{\beta + 1}\times I \longrightarrow X_{\beta + 1}
$$

which exhibits the required left homotopy.


So far this shows that each stage $X_{\beta} \to X_{\beta+1}$ in the [[transfinite composition]] defining $\hat X$ is a [[homotopy equivalence]], hence, by prop.  \ref{TopologicalHomotopyEquivalencesAreWeakHomotopyEquivalences}, a [[weak homotopy equivalence]].

This means that all morphisms in the following diagram (notationally suppressing basepoints and showing only the finite stages)

$$
  \array{
    \pi_n(X)
      &\overset{\simeq}{\longrightarrow}&
    \pi_n(X_1)
      &\overset{\simeq}{\longrightarrow}&
    \pi_n(X_2)
      &\overset{\simeq}{\longrightarrow}&
    \pi_n(X_3)
      &\overset{\simeq}{\longrightarrow}&
    \cdots
    \\
    & {}_{\mathllap{\simeq}}\searrow &
      \downarrow^{\mathrlap{\simeq}}
    & \swarrow_{\mathrlap{\simeq}} & \cdots
    \\
    && \underset{\longleftarrow}{\lim}_\alpha \pi_n(X_\alpha)
  }
$$

are isomorphisms.

Moreover, lemma \ref{CompactSubsetsAreSmallInCellComplexes} gives that every representative and every null homotopy of elements in $\pi_n(\hat X)$ already exists at some finite stage $X_k$. This means that also the universally induced morphism

$$
  \underset{\longleftarrow}{\lim}_\alpha \pi_n(X_\alpha)
  \overset{\simeq}{\longrightarrow}
  \pi_n(\hat X)
$$

is an isomorphism. Hence the composite $\pi_n(X) \overset{\simeq}{\longrightarrow} \pi_n(\hat X)$ is an isomorphism.

=--





### Fibrations

Given a relative $C$-cell complex $\iota \colon  X \to Y$, def. \ref{TopologicalCCellComplex}, it is typically interesting to study the [[extension]] problem along $f$, i.e. to ask which topological spaces $E$ are such that every [[continuous function]] $f\colon X \longrightarrow E$ has an extension $\tilde f$ along $\iota$

$$
  \array{
    X &\stackrel{f}{\longrightarrow}& E
    \\
    {}^{\mathllap{\iota}}\downarrow & \nearrow_{\mathrlap{\exists \tilde f}}
    \\
    Y
  }
  \,.
$$

If such extensions exists, it means that $E$ is sufficiently "spread out" with respect to the maps in $C$. More generally one considers this extension problem fiberwise, i.e. with both $E$ and $Y$ (hence also $X$) equipped with a map to some base space $B$:


+-- {: .num_defn #RightLiftingProperty}
###### Definition

Given a [[category]] $\mathcal{C}$ and a sub-[[class]] $C \subset Mor(\mathcal{C})$ of its [[morphisms]], then a morphism $p \colon E \longrightarrow B$ in $\mathcal{C}$ is said to have the [[right lifting property]] against the morphisms in $C$ if every [[commuting diagram]] in $\mathcal{C}$ of the form

$$
  \array{
    X &\longrightarrow& E
    \\
    {}^{\mathllap{c}}\downarrow && \downarrow^{\mathrlap{p}}
    \\
    Y &\longrightarrow& B
  }
  \,,
$$

with $c \in C$, has a [[lift]] $h$, in that it may be completed to a [[commuting diagram]] of the form

$$
  \array{
    X &\longrightarrow& E
    \\
    {}^{\mathllap{c}}\downarrow &{}^{\mathllap{h}}\nearrow& \downarrow^{\mathrlap{p}}
    \\
    Y &\longrightarrow& B
  }
  \,.
$$

We will also say that $p$ is a **$C$-[[injective morphism]]** if it satisfies the right lifting property against $C$.

=--



+-- {: .num_defn #SerreFibration}
###### Definition

A [[continuous function]] $p \colon E \longrightarrow B$
is called a **[[Serre fibration]]** if it is a $J_{Top}$-[[injective morphism]]; i.e. if it has the [[right lifting property]], def. \ref{RightLiftingProperty}, against all topological generating acylic cofibrations, def. \ref{TopologicalGeneratingAcyclicCofibrations};
hence if for every [[commuting diagram]] of [[continuous functions]] of the form

$$
  \array{
    D^n &\longrightarrow& E
    \\
    {}^{\mathllap{(id,\delta_0)}}\downarrow && \downarrow^{\mathrlap{p}}
    \\
    D^n\times I &\longrightarrow& B
  }
  \,,
$$

has a [[lift]] $h$, in that it may be completed to a [[commuting diagram]] of the form

$$
  \array{
    D^n &\longrightarrow& E
    \\
    {}^{\mathllap{(id,\delta_0)}}\downarrow
     &{}^{\mathllap{h}}\nearrow& \downarrow^{\mathrlap{p}}
    \\
    D^n\times I &\longrightarrow& B
  }
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

Def. \ref{SerreFibration} says, in view of the definition of [[left homotopy]], that a [[Serre fibration]] $p$ is a map with the property that given a [[left homotopy]], def. \ref{LeftHomotopy}, between two functions into its [[codomain]], and given a lift of one the two functions through $p$, then also the homotopy between the two lifts.
Therefore the condition on a [[Serre fibration]] is also called the _[[homotopy lifting property]]_ for maps whose domain is an [[n-disk]].

More generally one may ask functions $p$ to have such [[homotopy lifting property]] for functions with arbitrary domain. These are called _[[Hurewicz fibrations]]_.

=--

+-- {: .num_remark #SerreFibrationsByLiftingAgainstMapsHomeomorphicToDiskInclusions}
###### Remark

The precise shape of $D^n$ and $D^n \times I$ in def. \ref{SerreFibration} turns out not to actually matter much for the nature of Serre fibrations. We will eventually find below (prop. \ref{LiftingPropertyInTheClassicalModelStructureOnTopologicalSpaces}) that what actually matters here is only that the inclusions $D^n \hookrightarrow D^n \times I$ are [[relative cell complexes]] (lemma \ref{TopologicalGeneratingAcyclicCofibrationsAreRelativeCellComplexes}) and [[weak homotopy equivalences]] (prop. \ref{TopologicalHomotopyEquivalencesAreWeakHomotopyEquivalences}) and that all of these may be generated from them in a suitable way.

But for simple special cases this is readily seen directly, too. Notably we could replace the [[n-disks]] in def. \ref{SerreFibration} with any [[homeomorphism|homeomorphic]] topological space. A choice important in the comparison to the [[classical model structure on simplicial sets]] ([below](#GeometricRealizationSection)) is to instead take the topological [[n-simplices]] $\Delta^n$. Hence a Serre fibration is equivalently characterized as having lifts in all diagrams of the form

$$
  \array{
    \Delta^n &\longrightarrow& E
    \\
    {}^{\mathllap{(id,\delta_0)}}\downarrow && \downarrow^{\mathrlap{p}}
    \\
    \Delta^n\times I &\longrightarrow& B
  }
  \,.
$$

Other deformations of the $n$-disks are useful in computations, too. For instance there is a homeomorphism from the $n$-disk to its "cylinder with interior and end removed", formally:

$$
  \array{
    (D^n \times \{0\})\cup (\partial D^n \times I) &\simeq& D^n
    \\
    \downarrow && \downarrow
    \\
    D^n \times I &\simeq& D^n\times I
  }
$$

and hence $f$ is a Serre fibration equivalently also if it admits lifts in all diagrams of the form

$$
  \array{
    (D^n \times \{0\})\cup (\partial D^n \times I) &\longrightarrow& E
    \\
    {}^{\mathllap{(id,\delta_0)}}\downarrow && \downarrow^{\mathrlap{p}}
    \\
    D^n\times I &\longrightarrow& B
  }
  \,.
$$


=--

The following is a general fact about closure of morphisms defined by lifting properties which we prove in generality below as prop. \ref{ClosurePropertiesOfInjectiveAndProjectiveMorphisms}.

+-- {: .num_prop #SerreFibrationHasRightLiftingAgainstJTopRelativeCellComplexes}
###### Proposition

A [[Serre fibration]], def. \ref{SerreFibration} has the [[right lifting property]] against all [[retracts]] (see remark \ref{RetractsOfMorphisms}) of $J_{Top}$-[[relative cell complexes]] (def. \ref{TopologicalGeneratingAcyclicCofibrations}, def. \ref{TopologicalCellComplex}).

=--



The following statement is foreshadowing the [[long exact sequences of homotopy groups]] ([below](#LongSequences)) induced by any [[fiber sequence]], the full version of which we come to [below](HomotopyFiberSequences) (example \ref{LongExactSequeceOfHomotopyGroups}) after having developed more of the abstract homotopy theory.

+-- {: .num_prop #SerreFibrationGivesExactSequenceOfHomotopyGroups}
###### Proposition

Let $f\colon X \longrightarrow Y$ be a [[Serre fibration]], def. \ref{SerreFibration}, let $y \colon \ast \to Y$ be any point and write

$$
  F_y \overset{\iota}{\hookrightarrow} X \overset{f}{\longrightarrow} Y
$$

for the [[fiber]] inclusion over that point. Then for every choice $x \colon \ast \to X$ of lift of the point $y$ through $f$, the induced sequence of [[homotopy groups]]

$$

  \pi_{\bullet}(F_y, x)
    \overset{\iota_\ast}{\longrightarrow}
  \pi_\bullet(X, x)
    \overset{f_\ast}{\longrightarrow}
  \pi_\bullet(Y)
$$

is [[exact sequence|exact]], in that the [[kernel]] of $f_\ast$ is canonically identified with the [[image]] of $\iota_\ast$:

$$
  ker(f_\ast) \simeq im(\iota_\ast)
  \,.
$$

=--

+-- {: .proof}
###### Proof

It is clear that the image of $\iota_\ast$ is in the kernel of $f_\ast$ (every sphere in $F_y\hookrightarrow X$ becomes constant on $y$, hence contractible, when sent forward to $Y$).

For the converse, let $[\alpha]\in \pi_{\bullet}(X,x)$ be represented by some $\alpha \colon S^{n-1} \to X$. Assume that $[\alpha]$ is in the kernel of $f_\ast$. This means equivalently that $\alpha$ fits into a [[commuting diagram]] of the form

$$
  \array{
    S^{n-1} &\overset{\alpha}{\longrightarrow}& X
    \\
    \downarrow && \downarrow^{\mathrlap{f}}
    \\
    D^n &\overset{\kappa}{\longrightarrow}& Y
  }
  \,,
$$

where $\kappa$ is the contracting homotopy witnessing that $f_\ast[\alpha] = 0$.

Now since $x$ is a lift of $y$, there exists a [[left homotopy]]

$$
  \eta  \;\colon\; \kappa \Rightarrow const_y
$$

as follows:

$$
  \array{
    && S^{n-1} &\overset{\alpha}{\longrightarrow}& X
    \\
    && {}^{\mathllap{\iota_n}}\downarrow && \downarrow^{\mathrlap{f}}
    \\
    && D^n &\overset{\kappa}{\longrightarrow}& Y
    \\
    && \downarrow^{\mathrlap{(id,\delta_1)}} && \downarrow^{\mathrlap{id}}
    \\
    D^n &\overset{(id,\delta_0)}{\longrightarrow}& D^n \times I &\overset{\eta}{\longrightarrow}& Y
    \\
    \downarrow && &&  \downarrow
    \\
    \ast && \overset{y}{\longrightarrow} && Y
  }
$$

(for instance: regard $D^n$ as embedded in $\mathbb{R}^n$ such that $0 \in \mathbb{R}^n$ is identified with the basepoint on the boundary of $D^n$ and set $\eta(\vec v,t) \coloneqq \kappa(t \vec v)$).

The [[pasting]] of the top two squares that have appeared this way is equivalent to the following commuting square

$$
  \array{
    S^{n-1} &\longrightarrow& &\overset{\alpha}{\longrightarrow}& X
    \\
    {}^{\mathllap{(id,\delta_1)}}\downarrow
    &&
    && \downarrow^{\mathrlap{f}}
    \\
    S^{n-1} \times I
      &\overset{(\iota_n, id)}{\longrightarrow}&
    D^n \times I
      &\overset{\eta}{\longrightarrow}&
    Y
  }
  \,.
$$

Because $f$ is a [[Serre fibration]] and by lemma \ref{CylinderOverCWComplexIsJTopRelativeCellComplex} and prop. \ref{SerreFibrationHasRightLiftingAgainstJTopRelativeCellComplexes}, this has a [[lift]]

$$
  \tilde \eta \;\colon\; S^{n-1} \times I \longrightarrow X
  \,.
$$


Notice that $\tilde \eta$ is a basepoint preserving [[left homotopy]] from $\alpha = \tilde \eta|_1$ to some $\alpha' \coloneqq \tilde \eta|_0$. Being homotopic, they represent the same element of $\pi_{n-1}(X,x)$:

$$
  [\alpha'] = [\alpha]
  \,.
$$

But the new representative $\alpha'$ has the special property that its image in $Y$ is not just trivializable, but trivialized:
combining $\tilde \eta$ with the previous diagram shows that it sits in the following commuting diagram

$$
  \array{
    \alpha' \colon & S^{n-1} &\overset{(id,\delta_0)}{\longrightarrow}& S^{n-1}\times I &\overset{\tilde \eta}{\longrightarrow}& X
    \\
    & \downarrow^{\iota_n} && \downarrow^{\mathrlap{(\iota_n,id)}} && \downarrow^{\mathrlap{f}}
    \\
    & D^n &\overset{(id,\delta_0)}{\longrightarrow}& D^n \times I &\overset{\eta}{\longrightarrow}& Y
    \\
    & \downarrow && &&  \downarrow
    \\
    & \ast && \overset{y}{\longrightarrow} && Y
  }
  \,.
$$

The commutativity of the outer square says that $f_\ast \alpha'$ is constant, hence that $\alpha'$ is entirely contained in the fiber $F_y$. Said more abstractly, the [[universal property]] of [[fibers]] gives that $\alpha'$ factors through $F_y\overset{\iota}{\hookrightarrow} X$, hence that $[\alpha'] = [\alpha]$ is in the image of $\iota_\ast$.

=--


The following lemma \ref{AcyclicSerreFibrationsAreTheJTopFibrations}, together with lemma \ref{CompactSubsetsAreSmallInCellComplexes} above, are the only two statements of the entire development here that crucially involve the [[concrete particular]] nature of [[topological spaces]] ("[[point-set topology]]"), everything beyond that is [[general abstract]] homotopy theory.

+-- {: .num_lemma #AcyclicSerreFibrationsAreTheJTopFibrations}
###### Lemma

The continuous functions with the [[right lifting property]], def. \ref{RightLiftingProperty} against the set $I_{Top} = \{S^{n-1}\hookrightarrow D^n\}$ of topological [[generating cofibrations]], def. \ref{TopologicalGeneratingCofibrations}, are precisely those which are both [[weak homotopy equivalences]], def. \ref{WeakHomotopyEquivalenceOfTopologicalSpaces} as well as [[Serre fibrations]], def. \ref{SerreFibration}.

=--


+-- {: .proof}
###### Proof

We break this up into three sub-statements:

**A) $I_{Top}$-injective morphisms are in particular weak homotopy equivalences**

Let $p \colon \hat X \to X$ have the [[right lifting property]] against $I_{Top}$

$$
  \array{
    S^{n-1}  &\longrightarrow & \hat X
    \\
    {}^{\mathllap{\iota_n}}\downarrow &{}^{\mathllap{\exists}}\nearrow& \downarrow^{\mathrlap{p}}
    \\
    D^n &\longrightarrow& X
  }
$$

We check that the lifts in these diagrams exhibit $\pi_\bullet(f)$ as being an [[isomorphism]] on all [[homotopy groups]], def. \ref{HomotopyGroupsOftopologicalSpaces}:


For $n = 0$ the existence of these lifts says that every point of $X$ is in the image of $p$, hence that $\pi_0(\hat X) \to \pi_0(X)$ is [[surjection|surjective]]. Let then $S^0 = \ast \coprod \ast \longrightarrow \hat X$ be a map that hits two connected components, then the existence of the lift says that if they have the same image in $\pi_0(X)$ then they were already the same connected component in $\hat X$. Hence $\pi_0(\hat X)\to \pi_0(X)$ is also [[injection|injective]] and hence is a [[bijection]].

Similarly, for $n \geq 1$, if $S^n \to \hat X$ represents an element in $\pi_n(\hat X)$ that becomes trivial in $\pi_n(X)$, then the existence of the lift says that it already represented the trivial element itself. Hence $\pi_n(\hat X) \to \pi_n(X)$ has trivial [[kernel]] and so is injective.

Finally, to see that $\pi_n(\hat X) \to \pi_n(X)$ is also surjective, hence bijective, observe that every elements in $\pi_n(X)$ is equivalently represented by a commuting diagram of the form

$$
  \array{
    S^{n-1} &\longrightarrow& \ast &\longrightarrow& \hat X
    \\
    \downarrow && \downarrow && \downarrow
    \\
    D^n &\longrightarrow& X &=& X
  }
$$

and so here the lift gives a representative of a preimage in $\pi_{n}(\hat X)$.

**B) $I_{Top}$-injective morphisms are in particular Serre fibrations**

By an immediate closure property of lifting problems (we spell this out in generality as prop. \ref{ClosurePropertiesOfInjectiveAndProjectiveMorphisms}, cor. \ref{SaturationOfGeneratingCofibrations} below) an $I_{Top}$-[[injective morphism]] has the [[right lifting property]] against all [[relative cell complexes]], and hence, by lemma \ref{TopologicalGeneratingAcyclicCofibrationsAreRelativeCellComplexes}, it is also a $J_{Top}$-injective morphism, hence a Serre fibration.

**C) Acyclic Serre fibrations are in particular $I_{Top}$-[[injective morphisms]]**

([Hirschhorn 15, section 6](#Hirschhorn15)).

Let $f\colon X \to Y$ be a Serre fibration that induces isomorphisms
on homotopy groups. In degree 0 this means that $f$ is an isomorphism on [[connected components]], and this means that there is a lift in every [[commuting square]] of the form

$$
  \array{
    S^{-1} = \emptyset &\longrightarrow& X
    \\
    \downarrow && \downarrow^{\mathrlap{f}}
    \\
    D^0 = \ast &\longrightarrow& Y
  }
$$

(this is $\pi_0(f)$ being surjective) and in every commuting square of the form

$$
  \array{
    S^0  &\longrightarrow& X
    \\
    {}^{\mathllap{\iota_0}}\downarrow && \downarrow^{\mathrlap{f}}
    \\
    D^1 = \ast &\longrightarrow& Y
  }
$$

(this is $\pi_0(f)$ being injective). Hence we are reduced to showing that for $n \geq 2$ every diagram of the form

$$
  \array{
    S^{n-1}  &\overset{\alpha}{\longrightarrow}& X
    \\
    {}^{\mathllap{\iota_n}}\downarrow && \downarrow^{\mathrlap{f}}
    \\
    D^n  &\overset{\kappa}{\longrightarrow}& Y
  }
$$

has a lift.


To that end, pick a basepoint on $S^{n-1}$ and write $x$ and $y$ for its images in $X$ and $Y$, respectively

Then the diagram above expresses that $f_\ast[\alpha] = 0 \in \pi_{n-1}(Y,y)$ and hence by assumption on $f$ it follows that $[\alpha] = 0 \in \pi_{n-1}(X,x)$, which in turn mean that there is $\kappa'$ making the upper triangle of our lifting problem commute:

$$
  \array{
    S^{n-1} &\overset{\alpha}{\longrightarrow}& X
    \\
    {}^{\mathllap{\iota_n}}\downarrow & \nearrow_{\mathrlap{\kappa'}}
    \\
    D^n
  }
  \,.
$$

It is now sufficient to show that any such $\kappa'$ may be deformed to a $\rho'$ which keeps making this upper triangle commute but also makes the remaining lower triangle commute.

To that end, notice that by the commutativity of the original square, we already have at least this commuting square:

$$
  \array{
    S^{n-1} &\overset{\iota_n}{\longrightarrow}& D^n
    \\
    {}^{\mathllap{\iota_n}}\downarrow && \downarrow^{\mathrlap{f \circ \kappa'}}
    \\
    D^n &\underset{\kappa}{\longrightarrow}& Y
  }
  \,.
$$

This induces the universal map $(\kappa,f \circ \kappa')$ from the [[pushout]] of its [[cospan]] in the top left, which is the [[n-sphere]] (see [this](Top#TopologicalnSphereIsPushoutOfBoundaryOfnBallInclusionAlongItself) example):

$$
  \array{
    S^{n-1} &\overset{\iota_n}{\longrightarrow}& D^n
    \\
    {}^{\mathllap{\iota_n}}\downarrow
    &(po)&
    \downarrow^{\mathrlap{f \circ \kappa'}}
    \\
    D^n &\underset{\kappa}{\longrightarrow}& S^n
    \\
    && & \searrow^{(\kappa,f \circ \kappa')}
    \\
    && && Y
  }
  \,.
$$

This universal morphism represents an element of the $n$th homotopy group:

$$
  [(\kappa,f \circ \kappa')]
   \in
  \pi_n(Y,y)
  \,.
$$

By assumption that $f$ is a weak homotopy equivalence, there is a $[\rho] \in \pi_{n}(X,x)$ with

$$
  f_\ast [\rho] = [(\kappa,f \circ \kappa')]
$$

hence on representatives there is a lift up to homotopy

$$
  \array{
    && X
    \\
    &{}^{\mathllap{\rho}}\nearrow_{\mathrlap{\Downarrow}} & \downarrow^{\mathrlap{f}}
    \\
    S^n
    &\underset{(\kappa,f\circ \kappa')}{\longrightarrow}&
    Y
  }
  \,.
$$

Morever, we may always find $\rho$ of the form $(\rho', \kappa')$ for some $\rho' \colon D^n \to X$. ("Paste $\kappa'$ to the reverse of $\rho$.")

Consider then the map

$$
  S^n \overset{(f\circ \rho', \kappa)}{\longrightarrow} Y
$$

and observe that this represents the trivial class:

$$
  \begin{aligned}
    [(f \circ \rho', \kappa)]
    & =
    [(f\circ \rho', f\circ \kappa')]
     +
      [(f\circ \kappa', \kappa)]
    \\
    & = f_\ast \underset{= [\rho]}{\underbrace{[(\rho',\kappa')]}}
      +
        [(f\circ \kappa', \kappa)]
    \\
    & = [(\kappa,f \circ \kappa')]
      +
        [(f\circ \kappa', \kappa)]
    \\
    & = 0
  \end{aligned}
  \,.
$$

This means equivalently that there is a homotopy

$$
  \phi \; \colon \; f\circ \rho' \Rightarrow \kappa
$$

fixing the boundary of the $n$-disk.

Hence if we denote homotopy by double arrows, then we have now achieved the following situation

$$
  \array{
    S^{n-1} &\overset{\alpha}{\longrightarrow}& X
    \\
    {}^{\mathllap{\iota_n}}\downarrow
    &
      {}^{\rho'}\nearrow_{\Downarrow^{\phi}}
    &
    \downarrow^{\mathrlap{f}}
    \\
    D^n &\longrightarrow& Y
  }
$$

and it now suffices to show that $\phi$ may be lifted to a homotopy of just $\rho'$, fixing the boundary, for then the resulting homotopic $\rho''$ is the desired lift.

To that end, notice that the condition that $\phi \colon D^n \times I \to Y$ fixes the boundary of the $n$-disk means equivalently that it extends to a morphism

$$
  S^{n-1} \underset{S^{n-1}\times I}{\sqcup} D^n \times I
  \overset{(f\circ \alpha,\phi)}{\longrightarrow}
  Y
$$

out of the [[pushout]] that identifies in the cylinder over $D^n$ all points lying over the boundary. Hence we are reduced to finding a lift in

$$
  \array{
    D^n &\overset{\rho'}{\longrightarrow}& X
    \\
    \downarrow && \downarrow^{\mathrlap{f}}
    \\
    S^{n-1}\underset{S^{n-1}\times I}{\sqcup} D^n \times I
    &\overset{(f\circ \alpha,\phi)}{\longrightarrow}&
    Y
  }
  \,.
$$

But inspection of the left map reveals that it is homeomorphic again to $D^n \to D^n \times I$, and hence the lift does indeed exist.

=--



## Abstract homotopy theory
 {#ModelCategoryTheory}


In the [above](#BackgroundOnTopologicalHomotopyTheoryFromAlgebraicTopology) we discussed three classes of [[continuous functions]] between [[topological spaces]]

1. [[weak homotopy equivalences]];

1. [[relative cell complexes]];

1. [[Serre fibrations]]

and we saw first aspects of their interplay via [[lifting properties]].

A fundamental insight due to ([Quillen 67](#Quillen67)) is that in fact _all_ constructions in [[homotopy theory]] are elegantly expressible via just the abstract interplay of these classes of morphisms. This was distilled in ([Quillen 67](#Quillen67)) into a small set of [[axioms]] called a **[[model category]] structure** (because it serves to make all [[objects]] be _models_ for [[homotopy types]].)

This _abstract homotopy theory_ is the royal road for handling any flavor of [[homotopy theory]], in particular the [[stable homotopy theory]] that we are after in _[[Introduction to Stable homotopy theory -- 1|Part 1]]_. Here we discuss the basic constructions and facts in abstract homotopy theory, then [below](#TheClassicalModelStructureOfTopologicalSpaces) we conclude this _Introduction to Homotopy Theory_  by showing that topological spaces equipped with the above system of classes continuous functions is indeed an example of _abstract homotopy theory_ in this sense.

<br>

**Literature** ([Dwyer-Spalinski 95](#DwyerSpalinski95))

<br>


+-- {: .num_defn #CategoryWithWeakEquivalences}
###### Definition

A **[[category with weak equivalences]]** is

1. a [[category]] $\mathcal{C}$;

1. a sub-[[class]] $W \subset Mor(\mathcal{C})$ of its [[morphisms]];

such that

1. $W$ contains all the [[isomorphisms]] of $\mathcal{C}$;

1. $W$ is closed under **[[two-out-of-three]]**: in every [[commuting diagram]] in $\mathcal{C}$ of the form

   $$
     \array{
         && Y
         \\
         & \nearrow&& \searrow
         \\
         X
         &&
         \longrightarrow
         &&
         Z
     }
   $$

   if two of the three morphisms are in $W$, then so is the third.

=--

+-- {: .num_remark}
###### Remark

It turns out that a [[category with weak equivalences]], def. \ref{CategoryWithWeakEquivalences}, already determines a [[homotopy theory]]: the one given given by universally forcing weak equivalences to become actual [[homotopy equivalences]]. This may be made precise and is called the _[[simplicial localization]]_ of a category with weak equivalences ([Dwyer-Kan 80a](simplicial+localization#DwyerKanLocalizations), [Dwyer-Kan 80b](simplicial+localization#DwyerKanCalculating), [Dwyer-Kan 80c](simplicial+localization#DwyerKanFunctionComplexes)). However, without further auxiliary structure, these simplicial localizations are in general intractable. The further axioms of a [[model category]] serve the sole purpose of making the universal homotopy theory induced by a [[category with weak equivalences]] be tractable:

=--

+-- {: .num_defn #ModelCategory}
###### Definition

A **[[model category]]** is

1. a [[category]] $\mathcal{C}$ with all [[limits]] and [[colimits]] (def. \ref{LimitsAndColimits});

1. three sub-[[classes]] $W, Fib, Cof \subset Mor(\mathcal{C})$ of its [[morphisms]];

such that

1. the class $W$ makes $\mathcal{C}$ into a **[[category with weak equivalences]]**, def. \ref{CategoryWithWeakEquivalences};

1. The pairs $(W \cap Cof\;,\; Fib)$ and $(Cof\;,\; W\cap Fib)$ are both [[weak factorization systems]], def. \ref{WeakFactorizationSystem}.

One says:

* elements in $W$ are _[[weak equivalences]]_,

* elements in $Cof$ are _[[cofibrations]]_,

* elements in $Fib$ are _[[fibrations]]_,

* elements in $W\cap Cof$ are _[[acyclic cofibrations]]_,

* elements in $W \cap Fib$ are _[[acyclic fibrations]]_.

=--

The form of def. \ref{ModelCategory} is due to ([Joyal, def. E.1.2](#Joyal)). It implies various other conditions that ([Quillen 67](#Quillen67)) demands explicitly, see prop. \ref{ClosurePropertiesOfInjectiveAndProjectiveMorphisms} and prop. \ref{WeakEquivalencesAreClosedUnderRetracts} below.

We now dicuss the concept of [[weak factorization systems]] appearing in def. \ref{ModelCategory}.



### Factorization systems
 {#WeakFactorizationSystems}


+-- {: .num_defn #LiftingAndExtension}
###### Definition

Let $\mathcal{C}$ be any [[category]].
Given a [[diagram]] in $\mathcal{C}$ of the form

$$
  \array{
     X &\stackrel{f}{\longrightarrow}& Y
     \\
     {}^{\mathllap{p}}\downarrow
     \\
     B
  }
$$

then an *[[extension]]* of the [[morphism]] $f$ along the [[morphism]] $p$ is a completion to a [[commuting diagram]] of the form

$$
  \array{
     X &\stackrel{f}{\longrightarrow}& Y
     \\
     {}^{\mathllap{p}}\downarrow & \nearrow_{\mathrlap{\tilde f}}
     \\
     B
  }
  \,.
$$

Dually, given a [[diagram]] of the form

$$
  \array{
    && A
    \\
    && \downarrow^{\mathrlap{p}}
    \\
    X &\stackrel{f}{\longrightarrow}& Y
  }
$$

then a **[[lift]]** of $f$ through $p$ is a completion to a [[commuting diagram]] of the form

$$
  \array{
    && A
    \\
    &{}^{\mathllap{\tilde f}}\nearrow& \downarrow^{\mathrlap{p}}
    \\
    X &\stackrel{f}{\longrightarrow}& Y
  }
  \,.
$$

Combining these cases: given a [[commuting square]]

$$
  \array{
     X_1 &\stackrel{f_1}{\longrightarrow}& Y_1
     \\
     {}^{\mathllap{p_l}}\downarrow && \downarrow^{\mathrlap{p_r}}
     \\
     X_2 &\stackrel{f_1}{\longrightarrow}& Y_2
  }
$$

then a **[[lifting]]** in the diagram is a completion to a [[commuting diagram]] of the form

$$
  \array{
     X_1 &\stackrel{f_1}{\longrightarrow}& Y_1
     \\
     {}^{\mathllap{p_l}}\downarrow &\nearrow& \downarrow^{\mathrlap{p_r}}
     \\
     X_2 &\stackrel{f_1}{\longrightarrow}& Y_2
  }
  \,.
$$

Given a sub-[[class]] of morphisms $K \subset Mor(\mathcal{C})$, then

* a morphism $p_r$ as above is said to have the **[[right lifting property]] against $K$** or to be a **$K$-[[injective morphism]]** if in all square diagrams with $p_r$ on the right and any $p_l \in K$ on the left a lift exists.

dually:

* a morphism $p_l$ is said to have the **[[left lifting property]] against $K$** or to be a **$K$-[[projective morphism]]**  if in all square diagrams with $p_l$ on the left and any $p_r \in K$ on the right a lift exists.

=--

+-- {: .num_defn #WeakFactorizationSystem}
###### Definition

A **[[weak factorization system]]** (WFS) on a [[category]] $\mathcal{C}$ is a [[pair]] $(Proj,Inj)$ of [[classes]] of [[morphisms]] of $\mathcal{C}$ such that

1. Every [[morphism]] $f \colon X\to Y$ of $\mathcal{C}$ may be factored as the [[composition]] of a morphism in $Proj$ followed by one in $Inj$

   $$
     f\;\colon\;  X \overset{\in Proj}{\longrightarrow} Z \overset{\in Inj}{\longrightarrow} Y
     \,.
   $$

1. The classes are closed under having the [[lifting property]], def. \ref{LiftingAndExtension}, against each other:

   1. $Proj$ is precisely the class of morphisms having the [[left lifting property]] against every morphisms in $Inj$;

   1. $Inj$ is precisely the class of morphisms having the [[right lifting property]] against every morphisms in $Proj$.

=--

+-- {: .num_defn #FunctorialFactorization}
###### Definition

For $\mathcal{C}$ a [[category]], a **[[functorial factorization]]** of the morphisms in $\mathcal{C}$ is a [[functor]]

$$
  fact \;\colon\; \mathcal{C}^{\Delta[1]} \longrightarrow \mathcal{C}^{\Delta[2]}
$$

which is a [[section]] of the [[composition]] functor $d_1 \;\colon \;\mathcal{C}^{\Delta[2]}\to \mathcal{C}^{\Delta[1]}$.

=--

+-- {: .num_remark}
###### Remark

In def. \ref{FunctorialFactorization} we are using the following standard notation, see at _[[simplex category]]_ and at _[[nerve of a category]]_:

Write $[1] = \{0 \to 1\}$ and $[2] = \{0 \to 1 \to 2\}$ for the [[ordinal numbers]], regarded as [[posets]] and hence as [[categories]]. The [[arrow category]] $Arr(\mathcal{C})$ is equivalently the [[functor category]] $\mathcal{C}^{\Delta[1]} \coloneqq Funct(\Delta[1], \mathcal{C})$, while $\mathcal{C}^{\Delta[2]}\coloneqq Funct(\Delta[2], \mathcal{C})$ has as objects pairs of composable morphisms in $\mathcal{C}$. There are three injective functors $\delta_i \colon [1] \rightarrow [2]$, where $\delta_i$ omits the index $i$ in its image.
By precomposition, this induces [[functors]] $d_i  \colon \mathcal{C}^{\Delta[2]} \longrightarrow \mathcal{C}^{\Delta[1]}$. Here

* $d_1$ sends a pair of composable morphisms to their [[composition]];

* $d_2$ sends a pair of composable morphisms to the first morphisms;

* $d_0$ sends a pair of composable morphisms to the second morphisms.

=--

+-- {: .num_defn #FunctorialWeakFactorizationSystem}
###### Definition

A weak factorization system, def. \ref{WeakFactorizationSystem}, is called a **functorial weak factorization system** if the factorization of morphisms may be chosen to be a [[functorial factorization]] $fact$, def. \ref{FunctorialFactorization}, i.e. such that $d_2 \circ fact$ lands in $Proj$ and $d_0\circ fact$ in $Inj$.

=--

+-- {: .num_remark}
###### Remark

Not all weak factorization systems are functorial, def. \ref{FunctorialWeakFactorizationSystem}, although most (including those produced by the [[small object argument]] (prop. \ref{SmallObjectArgument} below), with due care) are.

=--


+-- {: .num_prop #ClosurePropertiesOfInjectiveAndProjectiveMorphisms}
###### Proposition

Let $\mathcal{C}$ be a [[category]] and let $K\subset Mor(\mathcal{C})$ be a [[class]] of [[morphisms]]. Write $K Proj$ and $K Inj$, respectively, for the sub-classes of $K$-[[projective morphisms]] and of $K$-[[injective morphisms]], def. \ref{LiftingAndExtension}. Then:

1. Both classes contain the class of [[isomorphism|isomorphisms]] of $\mathcal{C}$.

1. Both classes are closed under [[composition]] in $\mathcal{C}$.

   $K Proj$ is also closed under [[transfinite composition]].

1. Both classes are closed under forming [[retracts]] in the [[arrow category]] $\mathcal{C}^{\Delta[1]}$ (see remark \ref{RetractsOfMorphisms}).

1. $K Proj$ is closed under forming [[pushouts]] of morphisms in $\mathcal{C}$ ("[[cobase change]]").

   $K Inj$ is closed under forming [[pullback]] of morphisms in $\mathcal{C}$ ("[[base change]]").

1. $K Proj$ is closed under forming [[coproducts]] in $\mathcal{C}^{\Delta[1]}$.

   $K Inj$ is closed under forming [[products]] in $\mathcal{C}^{\Delta[1]}$.

=--

+-- {: .proof}
###### Proof

We go through each item in turn.

**containing isomorphisms**

Given a [[commuting square]]

$$
  \array{
    A &\overset{f}{\rightarrow}& X
    \\
    {}_{\mathllap{\in Iso}}^{\mathllap{i}}\downarrow && \downarrow^{\mathrlap{p}}
    \\
    B &\underset{g}{\longrightarrow}& Y
  }
$$

with the left morphism an isomorphism, then a [[lift]] is given by using the [[inverse]] of this isomorphism ${}^{{f \circ i^{-1}}}\nearrow$. Hence in particular there is a lift when $p \in K$ and so $i \in K Proj$. The other case is [[formal dual|formally dual]].

**closure under composition**

Given a [[commuting square]] of the form

$$
  \array{
    A &\longrightarrow& X
    \\
    \downarrow && \downarrow^{\mathrlap{p_1}}_{\mathrlap{\in K Inj}}
    \\
    {}^{\mathllap{i}}_{\mathllap{\in K}}\downarrow && \downarrow^{\mathrlap{p_2}}_{\mathrlap{\in K Inj}}
    \\
    B &\longrightarrow& Y
  }
$$

consider its [[pasting]] decomposition as

$$
  \array{
    A &\longrightarrow& X
    \\
    \downarrow
    &\searrow& \downarrow^{\mathrlap{p_1}}_{\mathrlap{\in K Inj}}
    \\
    {}^{\mathllap{i}}_{\mathllap{\in K}}\downarrow && \downarrow^{\mathrlap{p_2}}_{\mathrlap{\in K Inj}}
    \\
    B &\longrightarrow& Y
  }
  \,.
$$

Now the bottom commuting square has a lift, by assumption. This yields another [[pasting]] decomposition

$$
  \array{
    A &\longrightarrow& X
    \\
    {}^{\mathllap{i}}_{\mathllap{\in K}}\downarrow
    && \downarrow^{\mathrlap{p_1}}_{\mathrlap{\in K Inj}}
    \\
    \downarrow &\nearrow& \downarrow^{\mathrlap{p_2}}_{\mathrlap{\in K Inj}}
    \\
    B &\longrightarrow& Y
  }
$$

and now the top commuting square has a lift by assumption. This is now equivalently a lift in the total diagram, showing that $p_1\circ p_1$ has the right lifting property against $K$ and is hence in $K Inj$. The case of composing two morphisms in $K Proj$  is [[formal dual|formally dual]]. From this the closure of $K Proj$ under [[transfinite composition]] follows since the latter is given by [[colimits]] of sequential composition and successive lifts against the underlying sequence as above constitutes a [[cocone]], whence the extension of the lift to the colimit follows by its [[universal property]] (cf. eg. [Hirschhorn (2002), Lem. 10.3.1](model+category#Hirschhorn02)).

**closure under retracts**

Let $j$ be the [[retract]] of an $i \in K Proj$, i.e. let there be a [[commuting diagram]] of the form.

$$
  \array{
    id_A \colon & A &\longrightarrow& C &\longrightarrow& A
    \\
    & \downarrow^{\mathrlap{j}} && \downarrow^{\mathrlap{i}}_{\mathrlap{\in K Proj}} && \downarrow^{\mathrlap{j}}
    \\
    id_B \colon & B &\longrightarrow& D &\longrightarrow& B
  }
  \,.
$$

Then for

$$
  \array{
     A &\longrightarrow& X
     \\
     {}^{\mathllap{j}}\downarrow && \downarrow^{\mathrlap{f}}_{\mathrlap{\in K}}
     \\
     B &\longrightarrow& Y
  }
$$

a [[commuting square]], it is equivalent to its [[pasting]] composite with that retract diagram

$$
  \array{
    A &\longrightarrow& C &\longrightarrow& A &\longrightarrow& X
    \\
    \downarrow^{\mathrlap{j}} && \downarrow^{\mathrlap{i}}_{\mathrlap{\in K Proj}} && \downarrow^{\mathrlap{j}} && \downarrow^{\mathrlap{f}}_{\mathrlap{\in K}}
    \\
    B &\longrightarrow& D &\longrightarrow& B &\longrightarrow & Y
  }
  \,.
$$

Here the pasting composite of the two squares on the right has a lift, by assumption:

$$
  \array{
    A &\longrightarrow& C &\longrightarrow& A &\longrightarrow& X
    \\
    \downarrow^{\mathrlap{j}}
      &&
    \downarrow^{\mathrlap{i}}_{}
      &&
    \nearrow
      &&
    \downarrow^{\mathrlap{f}}_{\mathrlap{\in K}}
    \\
    B &\longrightarrow& D &\longrightarrow& B &\longrightarrow & Y
  }
  \,.
$$

By composition, this is also a lift in the total outer rectangle, hence in the original square. Hence $j$ has the left lifting property against all $p \in K$ and hence is in $K Proj$. The other case is [[formal duality|formally dual]].



**closure under pushout and pullback**

Let $p \in K Inj$ and and let

$$
  \array{
    Z \times_f X &\longrightarrow& X
    \\
    {}^{\mathllap{{f^* p}}}\downarrow && \downarrow^{\mathrlap{p}}
    \\
    Z &\stackrel{f}{\longrightarrow} & Y
  }
$$

be a [[pullback]] diagram in $\mathcal{C}$. We need to show that $f^* p$ has the [[right lifting property]] with respect to all $i \in K$. So let

$$
  \array{
     A &\longrightarrow& Z \times_f X
     \\
     {}^{\mathllap{i}}_{\mathllap{\in K}}\downarrow && \downarrow^{\mathrlap{\mathrlap{f^* p}}}
     \\
     B &\stackrel{g}{\longrightarrow}& Z
  }
$$

be a [[commuting square]]. We need to construct a diagonal lift of that square. To that end, first consider the [[pasting]] composite with the pullback square from above to obtain the commuting diagram

$$
  \array{
     A &\longrightarrow& Z \times_f X &\longrightarrow& X
     \\
     {}^{\mathllap{i}}\downarrow && \downarrow^{\mathrlap{f^* p}}
     && \downarrow^{\mathrlap{p}}
     \\
     B &\stackrel{g}{\longrightarrow}& Z &\stackrel{f}{\longrightarrow}& Y
  }
  \,.
$$

By the right lifting property of $p$, there is a diagonal lift of the total outer diagram

$$
  \array{
    A &\longrightarrow& X
    \\
    \downarrow^{\mathrlap{i}} &{}^{\hat {(f g)}}\nearrow&  \downarrow^{\mathrlap{p}}
    \\
    B &\stackrel{f g}{\longrightarrow}& Y
  }
  \,.
$$

By the [[universal property]] of the [[pullback]] this gives rise to the lift $\hat g$ in

$$
  \array{
     && Z \times_f X &\longrightarrow& X
     \\
     &{}^{\hat g} \nearrow& \downarrow^{\mathrlap{f^* p}}
     && \downarrow^{\mathrlap{p}}
     \\
     B &\stackrel{g}{\longrightarrow}& Z &\stackrel{f}{\longrightarrow}& Y
  }
  \,.
$$

In order for $\hat g$ to qualify as the intended lift of the total diagram, it remains to show that

$$
  \array{
     A &\longrightarrow& Z \times_f X
     \\
     \downarrow^{\mathrlap{i}} & {}^{\hat g}\nearrow
     \\
     B
  }
$$

commutes. To do so we notice that we obtain two [[cones]] with tip $A$:

* one is given by the morphisms
  1. $A \to Z \times_f X \to X$
  2. $A \stackrel{i}{\to} B \stackrel{g}{\to} Z$

  with universal morphism into the pullback being

  * $A \to Z \times_f X$

* the other by
  1. $A \stackrel{i}{\to} B \stackrel{\hat g}{\to} Z \times_f X \to X$
  2. $A \stackrel{i}{\to} B \stackrel{g}{\to} Z$.

  with universal morphism into the pullback being

  * $A \stackrel{i}{\to} B \stackrel{\hat g}{\to} Z \times_f X$.

The commutativity of the diagrams that we have established so far shows that the first and second morphisms here equal each other, respectively. By the fact that the universal morphism into a pullback diagram is _unique_ this implies the required identity of morphisms.

The other case is [[formal dual|formally dual]].

**closure under (co-)products**

Let $\{(A_s \overset{i_s}{\to} B_s) \in K Proj\}_{s \in S}$ be a set of elements of $K Proj$. Since [[colimits]] in the [[presheaf category]] $\mathcal{C}^{\Delta[1]}$ are computed componentwise, their [[coproduct]] in this [[arrow category]] is the universal morphism out of the coproduct of objects $\underset{s \in S}{\coprod} A_s$ induced via its [[universal property]] by the set of morphisms $i_s$:

$$
  \underset{s \in S}{\sqcup} A_s
  \overset{(i_s)_{s\in S}}{\longrightarrow}
  \underset{s \in S}{\sqcup} B_s
  \,.
$$

Now let

$$
  \array{
    \underset{s \in S}{\sqcup} A_s &\longrightarrow& X
    \\
    {}^{\mathllap{(i_s)_{s\in S}}}\downarrow && \downarrow^{\mathrlap{f}}_{\mathrlap{\in K}}
    \\
    \underset{s \in S}{\sqcup} B_s
    &\longrightarrow&
    Y
  }
$$

be a [[commuting square]]. This is in particular a [[cocone]] under the [[coproduct]] of objects, hence by the [[universal property]] of the coproduct, this is equivalent to a set of commuting diagrams

$$
  \left\{
  \;\;\;\;\;\;\;\;\;
  \array{
    A_s &\longrightarrow& X
    \\
    {}^{\mathllap{i_s}}_{\mathllap{\in K Proj}}\downarrow
      &&
    \downarrow^{\mathrlap{f}}_{\mathrlap{\in K}}
    \\
    B_s
    &\longrightarrow&
    Y
  }
  \;\;\;\;
  \right\}_{s\in S}
  \,.
$$

By assumption, each of these has a lift $\ell_s$. The collection of these lifts

$$
  \left\{
  \;\;\;\;\;\;\;\;\;
  \array{
    A_s &\longrightarrow& X
    \\
    {}^{\mathllap{i_s}}_{\mathllap{\in Proj}}\downarrow
      &{}^{\ell_s}\nearrow& \downarrow^{\mathrlap{f}}_{\mathrlap{\in K}}
    \\
    B_s
    &\longrightarrow&
    Y
  }
  \;\;\;\;
  \right\}_{s\in S}
$$

is now itself a compatible [[cocone]], and so once more by the [[universal property]] of the coproduct, this is equivalent to a lift $(\ell_s)_{s\in S}$ in the original square

$$
  \array{
    \underset{s \in S}{\sqcup} A_s &\longrightarrow& X
    \\
    {}^{\mathllap{(i_s)_{s\in S}}}\downarrow
     &{}^{(\ell_s)_{s\in S}}\nearrow&
    \downarrow^{\mathrlap{f}}_{\mathrlap{\in K}}
    \\
    \underset{s \in S}{\sqcup} B_s
    &\longrightarrow&
    Y
  }
  \,.
$$

This shows that the coproduct of the $i_s$ has the left lifting property against all $f\in K$ and is hence in $K Proj$. The other case is [[formal dual|formally dual]].



=--

An immediate consequence of prop. \ref{ClosurePropertiesOfInjectiveAndProjectiveMorphisms} is this:

+-- {: .num_prop #SaturationOfGeneratingCofibrations}
###### Corollary

Let $\mathcal{C}$ be a [[category]] with all small [[colimits]],
and let $K\subset Mor(\mathcal{C})$ be a sub-[[class]] of its morphisms.
Then every $K$-[[injective morphism]], def. \ref{LiftingAndExtension}, has the [[right lifting property]], def. \ref{LiftingAndExtension}, against all $K$-[[relative cell complexes]], def. \ref{TopologicalCCellComplex} and their [[retracts]], remark \ref{RetractsOfMorphisms}.

=--




+-- {: .num_remark #RetractsOfMorphisms}
###### Remark

By a [[retract]] of a [[morphism]] $X \stackrel{f}{\longrightarrow} Y$ in some [[category]] $\mathcal{C}$ we mean a retract of $f$ as an object in the [[arrow category]] $\mathcal{C}^{\Delta[1]}$, hence a morphism $A \stackrel{g}{\longrightarrow} B$ such that in $\mathcal{C}^{\Delta[1]}$ there is a factorization of the identity on $g$ through $f$

$$
  id_g \;\colon\;
  g \longrightarrow f \longrightarrow g
  \,.
$$

This means equivalently that in $\mathcal{C}$ there is a [[commuting diagram]] of the form

$$
  \array{
    id_A \colon & A &\longrightarrow& X &\longrightarrow& A
    \\
    & \downarrow^{\mathrlap{g}} && \downarrow^{\mathrlap{f}} && \downarrow^{\mathrlap{g}}
    \\
    id_B \colon & B &\longrightarrow& Y &\longrightarrow& B
  }
  \,.
$$

=--

+-- {: .num_lemma #RetractPreservesIsomorphism}
###### Lemma

In every [[category]] $C$ the class of [[isomorphisms]] is preserved under retracts in the sense of remark \ref{RetractsOfMorphisms}.

=--


+-- {: .proof}
###### Proof

For

$$
  \array{
    id_A \colon & A &\longrightarrow& X &\longrightarrow& A
    \\
    & \downarrow^{\mathrlap{g}} && \downarrow^{\mathrlap{f}} && \downarrow^{\mathrlap{g}}
    \\
    id_B \colon & B &\longrightarrow& Y &\longrightarrow& B
  }
  \,.
$$

a retract diagram and $X \overset{f}{\to} Y$ an isomorphism, the inverse to $A \overset{g}{\to} B$ is given by the composite

$$
  \array{
    &  & & X & \longrightarrow & A
    \\
    & && \uparrow^{\mathrlap{f^{-1}}} &&
    \\
    & B & \longrightarrow& Y&&
  }
  \,.
$$

=--

More generally:


+-- {: .num_prop #WeakEquivalencesAreClosedUnderRetracts}
###### Proposition

Given a [[model category]] in the sense of def. \ref{ModelCategory}, then its class of weak equivalences is closed under forming [[retracts]] (in the [[arrow category]], see remark \ref{RetractsOfMorphisms}).

=--

([Joyal, prop. E.1.3](#Joyal))


+-- {: .proof}
###### Proof

Let

$$
  \array{
    id \colon & A &\longrightarrow& X &\longrightarrow& A
    \\
    &
    {}^{\mathllap{f}}
    \downarrow
      &&
    \downarrow^{\mathrlap{w}}
      &&
    \downarrow^{\mathrlap{f}}
    \\
    id \colon & B &\longrightarrow& Y &\longrightarrow& B
  }
$$

be a [[commuting diagram]] in the given model category, with $w \in W$ a weak equivalence. We need to show that then also $f \in W$.

First consider the case that $f \in Fib$.

In this case, factor $w$ as a cofibration followed by an acyclic fibration. Since $w \in W$ and by [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}) this is even a factorization through an acyclic cofibration followed by an acyclic fibration. Hence we obtain a commuting diagram of the following form:

$$
  \array{
    id \colon
    &
    A
      &\longrightarrow&
    X
      &\overset{\phantom{AAAA}}{\longrightarrow}& A
    \\
    &
    {}^{\mathllap{id}}\downarrow
      &&
    \downarrow^{\mathrlap{\in W \cap Cof}}
      &&
    \downarrow^{\mathrlap{id}}
    \\
    id \colon
    & A' &\overset{s}{\longrightarrow}&
     X'
     &\overset{\phantom{AA}t\phantom{AA}}{\longrightarrow}& A'
    \\
    &
    {}^{\mathllap{f}}_{\mathllap{\in Fib}}
    \downarrow
      &&
    \downarrow^{\mathrlap{\in W \cap Fib}}
      &&
    \downarrow^{\mathrlap{f}}_{\mathrlap{\in Fib}}
    \\
    id \colon & B &\longrightarrow& Y &\underset{\phantom{AAAA}}{\longrightarrow}& B
  }
  \,,
$$

where $s$ is uniquely defined and where $t$ is any lift of the top middle vertical acyclic cofibration against $f$. This now exhibits $f$ as a retract of an acyclic fibration. These are closed under retract by prop. \ref{ClosurePropertiesOfInjectiveAndProjectiveMorphisms}.

Now consider the general case. Factor $f$ as an acyclic cofibration followed by a fibration and form the [[pushout]] in the top left square of the following diagram

$$
  \array{
    id \colon
    &
    A
      &\longrightarrow&
    X
      &\overset{\phantom{AAAA}}{\longrightarrow}& A
    \\
    &
    {}^{\mathllap{\in W \cap Cof}}\downarrow
      &(po)&
    \downarrow^{\mathrlap{\in W \cap Cof}}
      &&
    \downarrow^{\mathrlap{\in W \cap Cof}}
    \\
    id \colon
    & A' &\overset{}{\longrightarrow}&
     X'
     &\overset{\phantom{AA}\phantom{AA}}{\longrightarrow}& A'
    \\
    &
    {}^{\mathllap{\in Fib}}
    \downarrow
      &&
    \downarrow^{\mathrlap{\in W }}
      &&
    \downarrow^{\mathrlap{\in Fib}}
    \\
    id \colon & B &\longrightarrow& Y &\underset{\phantom{AAAA}}{\longrightarrow}& B
  }
  \,,
$$

where the other three squares are induced by the [[universal property]] of the pushout, as is the identification of the middle horizontal composite as the identity on $A'$. Since acyclic cofibrations are closed under forming pushouts by prop. \ref{ClosurePropertiesOfInjectiveAndProjectiveMorphisms}, the top middle vertical morphism is now an acyclic fibration, and hence by assumption and by [[two-out-of-three]] so is the middle bottom vertical morphism.

Thus the previous case now gives that the bottom left vertical morphism is a weak equivalence, and hence the total left vertical composite is.


=--



+-- {: .num_lemma #RetractArgument}
###### Lemma
**([[retract argument]])**

Consider a [[composition|composite]] morphism

$$
  f \;\colon\;
  X \stackrel{i}{\longrightarrow} A \stackrel{p}{\longrightarrow} Y
  \,.
$$

1. If $f$ has the [[left lifting property]] against $p$, then $f$ is a [[retract]] of $i$.

1. If $f$ has the [[right lifting property]] against $i$, then $f$ is a [[retract]] of $p$.

=--

+-- {: .proof}
###### Proof

We discuss the first statement, the second is [[formal duality|formally dual]].

Write the factorization of $f$ as a [[commuting square]] of the form

$$
  \array{
    X &\stackrel{i}{\longrightarrow}& A
    \\
    {}^{\mathllap{f}}\downarrow && \downarrow^{\mathrlap{p}}
    \\
    Y &= & Y
  }
  \,.
$$

By the assumed [[lifting property]] of $f$ against $p$ there exists a diagonal filler $g$ making a [[commuting diagram]] of the form

$$
  \array{
    X &\stackrel{i}{\longrightarrow}& A
    \\
    {}^{\mathllap{f}}\downarrow &{}^{\mathllap{g}}\nearrow& \downarrow^{\mathrlap{p}}
    \\
    Y &= & Y
  }
  \,.
$$

By rearranging this diagram a little, it is equivalent to

$$
  \array{
    & X &=& X
    \\
    & {}^{\mathllap{f}}\downarrow
     &&
    {}^{\mathllap{i}}\downarrow
    \\
    id_Y \colon & Y &\underset{g}{\longrightarrow}& A &\underset{p}{\longrightarrow}&
    Y
  }
  \,.
$$

Completing this to the right, this yields a diagram exhibiting the required retract according to remark \ref{RetractsOfMorphisms}:

$$
  \array{
    id_X \colon & X &=& X &=& X
    \\
    & {}^{\mathllap{f}}\downarrow
     &&
    {}^{\mathllap{i}}\downarrow
     &&
     {}^{\mathllap{f}}\downarrow
    \\
    id_Y \colon & Y &\underset{g}{\longrightarrow}& A &\underset{p}{\longrightarrow}&
    Y
  }
  \,.
$$

=--



**Small object argument**

Given a set $C \subset Mor(\mathcal{C})$ of morphisms in some [[category]] $\mathcal{C}$, a natural question is how to factor any given morphism $f\colon X \longrightarrow Y$ through a relative $C$-cell complex, def. \ref{TopologicalCCellComplex}, followed by a $C$-[[injective morphism]], def. \ref{RightLiftingProperty}

$$
  f
    \;\colon\;
  X
    \stackrel{\in C cell}{\longrightarrow}
  \hat X
    \stackrel{\in C inj}{\longrightarrow}
  Y
  \,.
$$

A first approximation to such a factorization turns out to be given simply by forming $\hat X = X_1$ by attaching **all** possible $C$-cells to $X$. Namely let

$$
  (C/f)
   \coloneqq
  \left\{
    \array{
       dom(c) &\stackrel{}{\longrightarrow}& X
       \\
       {}^{\mathllap{c\in C}}\downarrow && \downarrow^{\mathrlap{f}}
       \\
       cod(c) &\longrightarrow& Y
    }
  \right\}
$$

be the set of **all** ways to find a $C$-cell attachment in $f$, and consider the [[pushout]] $\hat X$ of the [[coproduct]] of morphisms in $C$ over all these:

$$
  \array{
    \underset{c\in(C/f)}{\coprod} dom(c) &\longrightarrow& X
    \\
    {}^{\mathllap{\underset{c\in(C/f)}{\coprod} c}}\downarrow
    &(po)&
    \downarrow^{\mathrlap{}}
    \\
    \underset{c\in(C/f)}{\coprod} cod(c)
    &\longrightarrow&
    X_1
  }
  \,.
$$

This gets already close to producing the intended factorization:

First of all the resulting map $X \to X_1$ is a $C$-relative cell complex, by construction.

Second, by the fact that the coproduct is over all commuting squres to $f$, the morphism $f$ itself makes a [[commuting diagram]]

$$
  \array{
    \underset{c\in(C/f)}{\coprod} dom(c) &\longrightarrow& X
    \\
    {}^{\mathllap{\underset{c\in(C/f)}{\coprod} c}}\downarrow
    &&
    \downarrow^{\mathrlap{f}}
    \\
    \underset{c\in(C/f)}{\coprod} cod(c)
    &\longrightarrow&
    Y
  }
$$

and hence the [[universal property]] of the [[colimit]] means that $f$ is indeed factored through that $C$-cell complex $X_1$; we may suggestively arrange that factorizing diagram like so:

$$
  \array{
    \underset{c\in(C/f)}{\coprod} dom(c)
      &\longrightarrow&
    X
    \\
    {}^{\mathllap{id}}\downarrow
    &&
    \downarrow^{\mathrlap{}}
    \\
    \underset{c\in(C/f)}{\coprod} dom(c)
     &&
    X_1
    \\
    {}^{\mathllap{\underset{c\in(C/f)}{\coprod} c}}\downarrow
    &\nearrow& \downarrow
    \\
    \underset{c\in(C/f)}{\coprod} cod(c)
    &\longrightarrow&
    Y
  }
  \,.
$$

This shows that, finally, the colimiting [[co-cone]] map -- the one that now appears diagonally -- **almost** exhibits the desired right lifting of $X_1 \to Y$ against the $c\in C$. The failure of that to hold on the nose is only the fact that a horizontal map in the middle of the above diagram is missing: the diagonal map obtained above lifts not all commuting diagrams of $c\in C$ into $f$, but only those where the top morphism $dom(c) \to X_1$ factors through $X \to X_1$.

The idea of the [[small object argument]] now is to fix this only remaining problem by iterating the construction: next factor $X_1 \to Y$ in the same way into

$$
  X_1 \longrightarrow X_2 \longrightarrow Y
$$

and so forth. Since relative $C$-cell complexes are closed under composition, at stage $n$ the resulting $X \longrightarrow X_n$ is still a $C$-cell complex, getting bigger and bigger. But accordingly, the failure of the accompanying $X_n \longrightarrow Y$ to be a $C$-[[injective morphism]] becomes smaller and smaller, for it now lifts against all diagrams where $dom(c) \longrightarrow X_n$ factors through $X_{n-1}\longrightarrow X_n$, which intuitively is less and less of a condition as the $X_{n-1}$ grow larger and larger.

The concept of _[[small object]]_ is just what makes this intuition precise and finishes the small object argument. For the present purpose we just need the following simple version:

+-- {: .num_defn #ClassOfMorphismsWithSmallDomains}
###### Definition

For $\mathcal{C}$ a [[category]] and $C \subset Mor(\mathcal{C})$
a sub-[[set]] of its morphisms, say that these have _small [[domains]]_
if there is an [[ordinal]] $\alpha$ (def. \ref{PosetsWosetTosetsAndOrdinals}) such that for every $c\in C$ and for every $C$-[[relative cell complex]] given by a [[transfinite composition]] (def. \ref{TransfiniteComposition})

$$
  f
  \;\colon\;
  X \to X_1 \to X_2 \to \cdots  \to X_\beta \to \cdots  \longrightarrow \hat X
$$

every morphism  $dom(c)\longrightarrow \hat X$ factors through a stage $X_\beta \to \hat X$ of order $\beta \lt \alpha$:

$$
  \array{
     && X_\beta
     \\
     & \nearrow & \downarrow
     \\
     dom(c) &\longrightarrow& \hat X
  }
  \,.
$$

=--

The above discussion proves the following:

+-- {: .num_prop #SmallObjectArgument}
###### Proposition
**(small object argument)**

Let $\mathcal{C}$ be a [[locally small category]] with all small [[colimits]]. If a [[set]] $C\subset Mor(\mathcal{C})$ of morphisms has all small domains in the sense of def. \ref{ClassOfMorphismsWithSmallDomains}, then every morphism $f\colon X\longrightarrow Y$ in $\mathcal{C}$ factors through a $C$-[[relative cell complex]], def. \ref{TopologicalCCellComplex}, followed by a $C$-[[injective morphism]], def. \ref{RightLiftingProperty}

$$
  f \;\colon\;
  X \stackrel{\in C cell}{\longrightarrow} \hat X \stackrel{\in C inj}{\longrightarrow}
  Y
  \,.
$$

=--

([Quillen 67, II.3 lemma](#Quillen67))

### Homotopy
 {#SectionAbstractHomotopy}

We discuss how the concept of [[homotopy]] is abstractly realized in [[model categories]], def. \ref{ModelCategory}.

+-- {: .num_defn #PathAndCylinderObjectsInAModelCategory}
###### Definition

Let $\mathcal{C}$ be a [[model category]], def. \ref{ModelCategory}, and $X \in \mathcal{C}$ an [[object]].

* A **[[path space object]]** $Path(X)$ for $X$ is a factorization of the [[diagonal]] $\Delta_X \;\colon\; X \to X \times X$ as

$$
  \Delta_X
  \;\colon\;
   X \underoverset{\in W}{i}{\longrightarrow} Path(X) \underoverset{\in Fib}{(p_0,p_1)}{\longrightarrow} X \times X
  \,.
$$

where $X\to Path(X)$ is a weak equivalence and $Path(X) \to X \times X$ is a fibration.

* A **[[cylinder object]]** $Cyl(X)$ for $X$ is a factorization of the [[codiagonal]] (or "fold map") $\nabla_X \;\colon\; X \sqcup X \to X$ as

$$
  \nabla_X
  \;\colon\;
  X \sqcup X \underoverset{\in Cof}{(i_0,i_1)}{\longrightarrow} Cyl(X) \underoverset{\in W}{p}{\longrightarrow} X
  \,.
$$

where $Cyl(X) \to X$ is a weak equivalence. and $X \sqcup X \to Cyl(X)$ is a cofibration.

=--

+-- {: .num_remark #RemarkOnChoicesOfNonGoodPathAndCylinderObjects}
###### Remark

For every object $X \in \mathcal{C}$ in a model category, a cylinder object and a path space object according to def. \ref{PathAndCylinderObjectsInAModelCategory} exist: the factorization axioms guarantee that there exists

1. a factorization of the [[codiagonal]] as

   $$
     \nabla_X \;\colon\; X \sqcup X \overset{\in Cof}{\longrightarrow} Cyl(X) \overset{\in W \cap Fib}{\longrightarrow} X
   $$

1. a factorization of the diagonal as

   $$
     \Delta_X
       \;\colon\;
     X
      \overset{\in W \cap Cof}{\longrightarrow}
     Path(X)
      \overset{\in Fib}{\longrightarrow}
     X \times X
     \,.
   $$

The cylinder and path space objects obtained this way are actually better than required by def. \ref{PathAndCylinderObjectsInAModelCategory}: in addition to $Cyl(X)\to X$ being just a weak equivalence, for these this is actually an acyclic fibration, and dually in addition to $X\to Path(X)$ being a weak equivalence, for these it is actually an acyclic cofibration.

Some authors call cylinder/path-space objects with this extra property "very good" cylinder/path-space objects, respectively.

One may also consider dropping a condition in def. \ref{PathAndCylinderObjectsInAModelCategory}: what mainly matters is the weak equivalence, hence some authors take cylinder/path-space objects to be defined as in def. \ref{PathAndCylinderObjectsInAModelCategory} but without the condition that $X \sqcup X\to Cyl(X)$ is a cofibration and without the condition that $Path(X) \to X\times X$ is a fibration. Such authors would then refer to the concept in def. \ref{PathAndCylinderObjectsInAModelCategory} as "good" cylinder/path-space objects.

The terminology in def. \ref{PathAndCylinderObjectsInAModelCategory} follows the original ([Quillen 67, I.1 def. 4](#Quillen67)). With the induced concept of left/right homotopy below in def. \ref{LeftAndRightHomotopyInAModelCategory}, this admits a quick derivation of the key facts in the following, as we spell out below.

=--

+-- {: .num_lemma #ComponentMapsOfCylinderAndPathSpaceInGoodSituation}
###### Lemma

Let $\mathcal{C}$ be a [[model category]]. If $X \in \mathcal{C}$ is cofibrant, then for every [[cylinder object]] $Cyl(X)$ of $X$, def. \ref{PathAndCylinderObjectsInAModelCategory}, not only is $(i_0,i_1) \colon X \sqcup X \to X$ a cofibration, but each

$$
  i_0, i_1 \colon X \longrightarrow Cyl(X)
$$

is an acyclic cofibration separately.

Dually, if $X \in \mathcal{C}$ is fibrant, then for every [[path space object]] $Path(X)$ of $X$, def. \ref{PathAndCylinderObjectsInAModelCategory}, not only is $(p_0,p_1) \colon Path(X)\to X \times X$ a fibration, but each

$$
  p_0, p_1 \colon Path(X) \longrightarrow X
$$

is an acyclic fibration separately.


=--

+-- {: .proof}
###### Proof

We discuss the case of the path space object. The other case is [[formal dual|formally dual]].

First, that the component maps are weak equivalences follows generally: by definition they have a [[right inverse]] $Path(X) \to X$ and so this follows by [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}).

But if $X$ is fibrant, then also the two projection maps out of the product $X \times X \to X$ are fibrations, because they are both pullbacks of the fibration $X \to \ast$

$$
  \array{
      X\times X &\longrightarrow& X
      \\
      \downarrow &(pb)& \downarrow
      \\
      X &\longrightarrow& \ast
  }
  \,.
$$

hence $p_i \colon Path(X)\to X \times X \to X$ is the composite of two fibrations, and hence itself a fibration, by prop. \ref{ClosurePropertiesOfInjectiveAndProjectiveMorphisms}.

=--



Path space objects are very non-unique as objects up to isomorphism:

+-- {: .num_example #ComposedPathSpaceObjects}
###### Example

If $X \in \mathcal{C}$ is a fibrant object in a [[model category]], def. \ref{ModelCategory}, and for $Path_1(X)$ and $Path_2(X)$ two [[path space objects]] for $X$, def. \ref{PathAndCylinderObjectsInAModelCategory}, then the [[fiber product]] $Path_1(X) \times_X Path_2(X)$ is another path space object for $X$: the pullback square

$$
  \array{
     X &\overset{\Delta_X}{\longrightarrow}&  X \times X
     \\
     \downarrow && \downarrow
     \\
     Path_1(X) \underset{X}{\times} Path_2(X)
     &\longrightarrow&
     Path_1(X)\times Path_2(X)
     \\
     {}^{\mathllap{\in Fib}}\downarrow
     &(pb)&
     \downarrow^{\mathrlap{\in Fib}}
     \\
     X \times X \times X
     &\overset{(id,\Delta_X,id)}{\longrightarrow}& X \times X\times X \times X
     \\
     \downarrow^{\mathrlap{(pr_1,pr_3)}}_{\mathrlap{\in Fib}}
     &&
     \downarrow^{\mathrlap{(p_1, p_4)}}
     \\
     X\times X &=& X \times X
  }
$$

gives that the induced projection is again a fibration. Moreover, using lemma \ref{ComponentMapsOfCylinderAndPathSpaceInGoodSituation} and [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}) gives that $X \to Path_1(X) \times_X Path_2(X)$ is a weak equivalence.

For the case of the canonical topological path space objects of def \ref{TopologicalPathSpace}, with $Path_1(X) = Path_2(X) = X^I = X^{[0,1]}$  then this new path space object is $X^{I \vee I} = X^{[0,2]}$, the [[mapping space]] out of the standard interval of length 2 instead of length 1.


=--



+-- {: .num_defn #LeftAndRightHomotopyInAModelCategory}
###### Definition

Let $f,g \colon X \longrightarrow Y$ be two [[parallel morphisms]] in a [[model category]].

* A **left homotopy** $\eta \colon f \Rightarrow_L g$ is a morphism $\eta \colon Cyl(X) \longrightarrow Y$ from a [[cylinder object]] of $X$,  def. \ref{PathAndCylinderObjectsInAModelCategory}, such that it makes this [[commuting diagram|diagram commute]]:

$$
  \array{
    X &\longrightarrow& Cyl(X) &\longleftarrow& X
    \\
    & {}_{\mathllap{f}}\searrow &\downarrow^{\mathrlap{\eta}}& \swarrow_{\mathrlap{g}}
    \\
    &&
    Y
  }
  \,.
$$

* A **right homotopy** $\eta \colon f \Rightarrow_R g$ is a morphism $\eta \colon X \to Path(Y)$ to some [[path space object]] of $Y$, def. \ref{PathAndCylinderObjectsInAModelCategory}, such that this [[commuting diagram|diagram commutes]]:

$$
  \array{
    && X
    \\
    & {}^{\mathllap{f}}\swarrow & \downarrow^{\mathrlap{\eta}} & \searrow^{\mathrlap{g}}
    \\
    Y &\longleftarrow& Path(Y) &\longrightarrow& Y
  }
  \,.
$$

=--



+-- {: .num_lemma #LeftHomotopyWithCofibrantDomainImpliesRightHomotopyAndDually}
###### Lemma

Let $f,g \colon X \to Y$ be two [[parallel morphisms]] in a [[model category]].

1. Let $X$ be cofibrant. If there is a [[left homotopy]] $f \Rightarrow_L g$ then there is also a [[right homotopy]] $f \Rightarrow_R g$ (def. \ref{LeftAndRightHomotopyInAModelCategory}) with respect to any chosen path space object.

1. Let $Y$ be fibrant. If there is a [[right homotopy]] $f \Rightarrow_R g$ then there is also a [[left homotopy]] $f \Rightarrow_L g$ with respect to any chosen cylinder object.

In particular if $X$ is cofibrant and $Y$ is fibrant, then by going back and forth it follows that every left homotopy is exhibited by every cylinder object, and every right homotopy is exhibited by every path space object.

=--

+-- {: .proof}
###### Proof

We discuss the first case, the second is [[formal dual|formally dual]].
Let $\eta \colon Cyl(X) \longrightarrow Y$ be the given left homotopy. Lemma \ref{ComponentMapsOfCylinderAndPathSpaceInGoodSituation} implies that we have a lift $h$ in the following [[commuting diagram]]

$$
  \array{
    X &\overset{i \circ f}{\longrightarrow}& Path(Y)
    \\
    {}^{\mathllap{i_0}}_{\mathllap{\in W \cap Cof}}\downarrow
    &{}^{\mathllap{h}}\nearrow&
    \downarrow^{\mathrlap{p_0,p_1}}_{\mathrlap{\in Fib}}
    \\
    Cyl(X)
    &\underset{(f \circ p,\eta)}{\longrightarrow}& Y \times Y
  }
  \,,
$$

where on the right we have the chosen path space object. Now the composite $\tilde \eta \coloneqq h \circ i_1$ is a right homotopy as required:

$$
  \array{
    && && Path(Y)
    \\
    && &{}^{\mathllap{h}}\nearrow&
    \downarrow^{\mathrlap{p_0,p_1}}_{\mathrlap{\in Fib}}
    \\
    X &\overset{i_1}{\longrightarrow}& Cyl(X)
    &\underset{(f \circ p,\eta)}{\longrightarrow}&
    Y \times Y
  }
  \,.
$$

=--


+-- {: .num_prop #BetweenCofibFibLeftAndRightHomotopyAreEquivalentEquivalenceRelations}
###### Proposition

For $X$ a cofibrant object in a [[model category]] and $Y$ a [[fibrant object]], the [[relations]] of [[left homotopy]] $f \Rightarrow_L g$ and of [[right homotopy]] $f \Rightarrow_R g$ (def. \ref{LeftAndRightHomotopyInAModelCategory}) on the [[hom set]] $Hom(X,Y)$ coincide and are both [[equivalence relations]].

=--


+-- {: .proof}
###### Proof

That both relations coincide under the (co-)fibrancy assumption follows directly from lemma \ref{LeftHomotopyWithCofibrantDomainImpliesRightHomotopyAndDually}.

The [[symmetric relation|symmetry]] and [[reflexive relation|reflexivity]] of the relation is obvious.

That right homotopy (hence also left homotopy) with domain $X$ is a [[transitive relation]] follows from using example \ref{ComposedPathSpaceObjects} to compose path space objects.


=--



### The homotopy category
 {#TheHomotopyCategory}

We discuss the construction that takes a [[model category]], def. \ref{ModelCategory}, and then universally forces all its [[weak equivalences]] into actual [[isomorphisms]].

+-- {: .num_defn #HomotopyCategoryOfAModelCategory}
###### Definition

Let $\mathcal{C}$ be a [[model category]], def. \ref{ModelCategory}. Write $Ho(\mathcal{C})$ for the [[category]] whose

* [[objects]] are those objects of $\mathcal{C}$ which are both fibrant and cofibrant;

* [[morphisms]] are the [[homotopy classes]] of morphisms of $\mathcal{C}$, hence the [[equivalence classes]] of morphism under the equivalence relation of prop. \ref{BetweenCofibFibLeftAndRightHomotopyAreEquivalentEquivalenceRelations};

and whose [[composition]] operation is given on representatives by composition in $\mathcal{C}$.

This is, up to [[equivalence of categories]], the **[[homotopy category of a model category|homotopy category of the model category]]** $\mathcal{C}$.

=--

+-- {: .num_prop}
###### Proposition

Def. \ref{HomotopyCategoryOfAModelCategory} is well defined, in that composition of morphisms between fibrant-cofibrant objects in $\mathcal{C}$ indeed passes to [[homotopy classes]].

=--

+-- {: .proof}
###### Proof

Fix any morphism $X \overset{f}{\to} Y$ between fibrant-cofibrant objects. Then for precomposition

$$
 (-) \circ [f] \;\colon\; Hom_{Ho(\mathcal{C})}(Y,Z) \to Hom_{Ho(\mathcal{C})}(X,Z)
$$

to be well defined, we need that with $(g\sim h)\;\colon\; Y \to Z$ also $(f g \sim f h)\;\colon\; X \to Z$. But by prop \ref{BetweenCofibFibLeftAndRightHomotopyAreEquivalentEquivalenceRelations} we may take the homotopy $\sim$ to be exhibited by a right homotopy $\eta \colon Y \to Path(Z)$, for which case the statement is evident from this diagram:

$$
  \array{
    && && Z
    \\
    && & {}^{\mathllap{g}}\nearrow & \uparrow^{\mathrlap{p_1}}
    \\
    X
      &\overset{f}{\longrightarrow} &
    Y
      &\overset{\eta}{\longrightarrow}&
    Path(Z)
    \\
    && & {}_{\mathllap{h}}\searrow & \downarrow_{\mathrlap{p_0}}
    \\
    && && Z
  }
  \,.
$$

For postcomposition we may choose to exhibit homotopy by left homotopy and argue [[formal dual|dually]].

=--

We now spell out that def. \ref{HomotopyCategoryOfAModelCategory} indeed satisfies the [[universal property]] that defines the [[localization]] of a [[category with weak equivalences]] at its weak equivalences.

+-- {: .num_lemma #WhiteheadTheoremInModelCategories}
###### Lemma
**([[Whitehead theorem]] in model categories)**

Let $\mathcal{C}$ be a [[model category]]. A [[weak equivalence]] between two objects which are both fibrant and cofibrant is a [[homotopy equivalence]].

=--

+-- {: .proof}
###### Proof

By the factorization axioms in the model category $\mathcal{C}$ and by [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}), every weak equivalence $f\colon X \longrightarrow Y$ factors through an object $Z$ as an acyclic cofibration followed by an acyclic fibration. In particular it follows that with $X$ and $Y$ both fibrant and cofibrant, so is $Z$, and hence it is sufficient to prove that acyclic (co-)fibrations between such objects are homotopy equivalences.

So let $f \colon X \longrightarrow Y$ be an acyclic fibration between fibrant-cofibrant objects, the case of acyclic cofibrations is [[formal dual|formally dual]]. Then in fact it has a genuine [[right inverse]] given by a lift $f^{-1}$ in the diagram

$$
  \array{
    \emptyset &\rightarrow& X
    \\
    {}^{\mathllap{\in cof}}\downarrow
     &{}^{{f^{-1}}}\nearrow&
   \downarrow^{\mathrlap{f}}_{\mathrlap{\in Fib \cap W}}
    \\
    Y &=& Y
  }
  \,.
$$

To see that $f^{-1}$ is also a [[left inverse]] up to [[left homotopy]], let $Cyl(X)$ be any [[cylinder object]] on $X$ (def. \ref{PathAndCylinderObjectsInAModelCategory}), hence a factorization of the [[codiagonal]] on $X$ as a cofibration followed by a an acyclic fibration

$$
  X \sqcup X \stackrel{\iota_X}{\longrightarrow} Cyl(X) \stackrel{p}{\longrightarrow} X
$$

and consider the [[commuting square]]

$$
  \array{
    X \sqcup X
    &\stackrel{(f^{-1}\circ f, id)}{\longrightarrow}& X
    \\
    {}^{\mathllap{\iota_X}}{}_{\mathllap{\in Cof}}\downarrow && \downarrow^{\mathrlap{f}}_{\mathrlap{\in W \cap Fib}}
    \\
    Cyl(X) &\underset{f\circ p}{\longrightarrow}& Y
  }
  \,,
$$

which [[commuting square|commutes]] due to $f^{-1}$ being a genuine right inverse of $f$. By construction, this [[commuting square]] now admits a [[lift]] $\eta$, and that constitutes a [[left homotopy]] $\eta \colon f^{-1}\circ f \Rightarrow_L id$.

=--

+-- {: .num_defn #FibrantCofibrantReplacementFunctorToHomotopyCategory}
###### Definition

Given a [[model category]] $\mathcal{C}$, consider a _choice_ for each object $X \in \mathcal{C}$ of

1. a factorization $\emptyset \underoverset{\in Cof}{i_X}{\longrightarrow} Q X \underoverset{\in W \cap Fib}{p_X}{\longrightarrow} X$ of the [[initial object|initial morphism]], such that when $X$ is already cofibrant then $p_X = id_X$;

1. a factorization $X \underoverset{\in W \cap Cof}{j_X}{\longrightarrow} P X \underoverset{\in Fib}{q_X}{\longrightarrow} \ast$ of the [[terminal object|terminal morphism]], such that when $X$ is already fibrant then $j_X = id_X$.

Write then

$$
  \gamma_{P,Q}
  \;\colon\;
  \mathcal{C}
   \longrightarrow
  Ho(\mathcal{C})
$$

for the [[functor]] to the homotopy category, def. \ref{HomotopyCategoryOfAModelCategory}, which sends an object $X$ to the object $P Q X$ and sends a morphism $f \colon X \longrightarrow Y$ to the [[homotopy class]] of the result of first lifting in

$$
  \array{
    \emptyset &\longrightarrow& Q Y
    \\
    {}^{\mathllap{i_X}}\downarrow &{}^{Q f}\nearrow& \downarrow^{\mathrlap{p_Y}}
    \\
    Q X &\underset{f\circ p_X}{\longrightarrow}& Y
  }
$$

and then lifting (here: [[extension|extending]]) in

$$
  \array{
    Q X &\overset{j_{Q Y} \circ Q f}{\longrightarrow}& P Q Y
    \\
    {}^{\mathllap{j_{Q X}}}\downarrow &{}^{P Q f}\nearrow& \downarrow^{\mathrlap{q_{Q Y}}}
    \\
    P Q X
    &\longrightarrow&
    \ast
  }
  \,.
$$

=--

+-- {: .num_lemma #ConstructionOfLocalizationFunctorForModelCategoryIsWellDefined}
###### Lemma

The construction in def. \ref{FibrantCofibrantReplacementFunctorToHomotopyCategory} is indeed well defined.

=--

+-- {: .proof}
###### Proof

First of all, the object $P Q X$ is indeed both fibrant and cofibrant (as well as related by a [[zig-zag]] of weak equivalences to $X$):

$$
  \array{
     \emptyset
     \\
     {}^{\mathllap{\in Cof}}\downarrow & \searrow^{\mathrlap{\in Cof}}
     \\
     Q X &\underset{\in W \cap Cof}{\longrightarrow}& P Q X &\underset{\in Fib}{\longrightarrow}& \ast
     \\
     {}^{\mathllap{\in W}}\downarrow
     \\
     X
  }
  \,.
$$

Now to see that the image on morphisms is well defined. First observe that any two choices $(Q f)_{i}$ of the first lift in the definition are left homotopic to each other, exhibited by lifting in

$$
  \array{
    Q X \sqcup Q X &\stackrel{((Q f)_1, (Q f)_2 )}{\longrightarrow}& Q Y
    \\
    {}^{\mathllap{\in Cof}}\downarrow
     &&
    \downarrow^{\mathrlap{p_{Y}}}_{\mathrlap{\in W \cap Fib}}
    \\
    Cyl(Q X)
    &\underset{f \circ p_{X} \circ \sigma_{Q X}}{\longrightarrow}&
    Y
  }
  \,.
$$

Hence also the composites $j_{Q Y}\circ (Q_f)_i $ are [[left homotopy|left homotopic]] to each other, and since their domain is cofibrant, then by lemma \ref{LeftHomotopyWithCofibrantDomainImpliesRightHomotopyAndDually} they are also [[right homotopy|right homotopic]] by a right homotopy $\kappa$. This implies finally, by lifting in

$$
  \array{
    Q X &\overset{\kappa}{\longrightarrow}& Path(P Q Y)
    \\
    {}^{\mathllap{\in W \cap Cof}}\downarrow
     &&
    \downarrow^{\mathrlap{\in Fib}}
    \\
    P Q X &\underset{(P (Q f)_1, P (Q f)_2)}{\longrightarrow}&
    P Q Y \times P Q Y
  }
$$

that also $P (Q f)_1$ and $P (Q f)_2$ are right homotopic, hence that indeed $P Q f$ represents a well-defined [[homotopy class]].

Finally to see that the assignment is indeed [[functor|functorial]], observe that the commutativity of the lifting diagrams for $Q f$ and $P Q f$ imply that also the following diagram commutes

$$
  \array{
    X &\overset{p_X}{\longleftarrow}& Q X &\overset{j_{Q X}}{\longrightarrow}& P Q X
    \\
    {}^{\mathllap{f}}\downarrow && \downarrow^{\mathrlap{Q f}} && \downarrow^{\mathrlap{P Q f}}
    \\
    Y &\underset{p_y}{\longleftarrow}& Q Y &\underset{j_{Q Y}}{\longrightarrow}& P Q Y
  }
  \,.
$$

Now from the [[pasting]] composite

$$
  \array{
    X &\overset{p_X}{\longleftarrow}& Q X &\overset{j_{Q X}}{\longrightarrow}& P Q X
    \\
    {}^{\mathllap{f}}\downarrow && \downarrow^{\mathrlap{Q f}} && \downarrow^{\mathrlap{P Q f}}
    \\
    Y &\underset{p_Y}{\longleftarrow}& Q Y &\underset{j_{Q Y}}{\longrightarrow}& P Q Y
    \\
    {}^{\mathllap{g}}\downarrow && \downarrow^{\mathrlap{Q g}} && \downarrow^{\mathrlap{P Q g}}
    \\
    Z &\underset{p_Z}{\longleftarrow}& Q Z &\underset{j_{Q Z}}{\longrightarrow}& P Q Z
  }
$$

one sees that $(P Q g)\circ (P Q f)$ is a lift of $g \circ f$ and hence the same argument as above gives that it is homotopic to the chosen $P Q(g \circ f)$.


=--

For the following, recall the concept of [[natural isomorphism]] between [[functors]]: for $F, G \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}$ two functors, then a _[[natural transformation]]_ $\eta \colon F \Rightarrow G$ is for each object $c \in Obj(\mathcal{C})$ a morphism $\eta_c \colon F(c) \longrightarrow G(c)$ in $\mathcal{D}$, such that for each morphism $f \colon c_1 \to c_2$ in $\mathcal{C}$ the following is a [[commuting square]]:

$$
  \array{
    F(c_1) &\overset{\eta_{c_1}}{\longrightarrow}& G(c_1)
    \\
    {}^{\mathllap{F(f)}}\downarrow && \downarrow^{\mathrlap{G(f)}}
    \\
    F(c_2) &\underset{\eta_{c_2}}{\longrightarrow}& G(c_2)
  }
  \,.
$$

Such $\eta$ is called a _[[natural isomorphism]]_ if its $\eta_c$ are [[isomorphisms]] for all objects $c$.

+-- {: .num_defn #HomotopyCategoryOfACategoryWithWeakEquivalences}
###### Definition

For $\mathcal{C}$ a [[category with weak equivalences]], its  **[[localization]] at the weak equivalences** is, if it exists,

1. a [[category]] denoted $\mathcal{C}[W^{-1}]$

1. a [[functor]]

   $$
     \gamma \;\colon\; \mathcal{C} \longrightarrow \mathcal{C}[W^{-1}]
   $$

such that

1. $\gamma$ sends weak equivalences to [[isomorphisms]];

1. $\gamma$ is [[universal property|universal with this property]], in that:

   for $F \colon \mathcal{C} \longrightarrow D$ any [[functor]] out of $\mathcal{C}$ into any [[category]] $D$, such that $F$ takes weak equivalences to [[isomorphisms]], it factors through $\gamma$ up to a [[natural isomorphism]] $\rho$

   $$
     \array{
       \mathcal{C} && \overset{F}{\longrightarrow} && D
       \\
       & {}_{\mathllap{\gamma}}\searrow &\Downarrow^{\rho}& \nearrow_{\mathrlap{\tilde F}}
       \\
       && Ho(\mathcal{C})
     }
   $$

   and this factorization is unique up to unique isomorphism, in that for $(\tilde F_1, \rho_1)$ and $(\tilde F_2, \rho_2)$ two such factorizations, then there is a unique [[natural isomorphism]] $\kappa \colon \tilde F_1 \Rightarrow \tilde F_2$ making the evident diagram of natural isomorphisms commute.

=--


+-- {: .num_theorem #UniversalPropertyOfHomotopyCategoryOfAModelCategory}
###### Theorem

For $\mathcal{C}$ a [[model category]], the functor $\gamma_{P,Q}$ in def. \ref{FibrantCofibrantReplacementFunctorToHomotopyCategory} (for any choice of $P$ and $Q$) exhibits $Ho(\mathcal{C})$ as indeed being the [[localization]] of the underlying [[category with weak equivalences]] at its weak equivalences, in the sense of def. \ref{HomotopyCategoryOfACategoryWithWeakEquivalences}:

$$
  \array{
     \mathcal{C} &=& \mathcal{C}
     \\
     {}^{\mathllap{\gamma_{P,Q}}}\downarrow && \downarrow^{\mathrlap{\gamma}}
     \\
     Ho(\mathcal{C}) &\simeq& \mathcal{C}[W^{-1}]
  }
  \,.
$$

=--

([Quillen 67, I.1 theorem 1](#Quillen67))

+-- {: .proof #ProofOfUniversalPropertyOfHomotopyCategoryOfAModelCategory}
###### Proof

First, to see that that $\gamma_{P,Q}$ indeed takes weak equivalences to isomorphisms: By [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}) applied to the [[commuting diagrams]] shown in the proof of lemma \ref{ConstructionOfLocalizationFunctorForModelCategoryIsWellDefined}, the morphism $P Q f$ is a weak equivalence if $f$ is:

$$
  \array{
    X &\underoverset{\simeq}{p_X}{\longleftarrow}& Q X &\underoverset{\simeq}{j_{Q X}}{\longrightarrow}& P Q X
    \\
    {}^{\mathllap{f}}\downarrow && \downarrow^{\mathrlap{Q f}} && \downarrow^{\mathrlap{P Q f}}
    \\(
    Y &\underoverset{p_y}{\simeq}{\longleftarrow}& Q Y &\underoverset{j_{Q Y}}{\simeq}{\longrightarrow}& P Q Y
  }
$$

With this the "Whitehead theorem for model categories", lemma \ref{WhiteheadTheoremInModelCategories}, implies that $P Q f$ represents an isomorphism in $Ho(\mathcal{C})$.

Now let $F \colon \mathcal{C}\longrightarrow D$ be any functor that sends weak equivalences to isomorphisms. We need to show that it factors as

$$
  \array{
    \mathcal{C} && \overset{F}{\longrightarrow} && D
    \\
    & {}_{\mathllap{\gamma}}\searrow &\Downarrow^{\rho}& \nearrow_{\mathrlap{\tilde F}}
    \\
    && Ho(\mathcal{C})
  }
$$

uniquely up to unique [[natural isomorphism]]. Now by construction of $P$ and $Q$ in def. \ref{FibrantCofibrantReplacementFunctorToHomotopyCategory}, $\gamma_{P,Q}$ is the identity on the [[full subcategory]] of fibrant-cofibrant objects. It follows that if $\tilde F$ exists at all, it must satisfy for all $X \stackrel{f}{\to} Y$ with $X$ and $Y$ both fibrant and cofibrant that

$$
  \tilde F([f]) \simeq F(f)
  \,,
$$

(hence in particular $\tilde F(\gamma_{P,Q}(f)) \simeq F(P Q f)$).

But by def. \ref{HomotopyCategoryOfAModelCategory} that already fixes $\tilde F$ on all of $Ho(\mathcal{C})$, up to unique [[natural isomorphism]]. Hence it only remains to check that with this definition of $\tilde F$ there exists any [[natural isomorphism]] $\rho$ filling the diagram above.

To that end, apply $F$ to the above [[commuting diagram]] to obtain

$$
  \array{
    F(X) &\underoverset{iso}{F(p_X)}{\longleftarrow}& F(Q X) &\underoverset{iso}{F(j_{Q X})}{\longrightarrow}& F(P Q X)
    \\
    {}^{\mathllap{F(f)}}\downarrow && \downarrow^{\mathrlap{F(Q f)}} && \downarrow^{\mathrlap{F(P Q f)}}
    \\
    F(Y) &\underoverset{F(p_y)}{iso}{\longleftarrow}& F(Q Y) &\underoverset{F(j_{Q Y})}{iso}{\longrightarrow}& F(P Q Y)
  }
  \,.
$$

Here now all horizontal morphisms are [[isomorphisms]], by assumption on $F$. It follows that defining $\rho_X \coloneqq F(j_{Q X}) \circ F(p_X)^{-1}$ makes the required natural isomorphism:

$$
  \array{
    \rho_X \colon & F(X) &\underoverset{iso}{F(p_X)^{-1}}{\longrightarrow}& F(Q X) &\underoverset{iso}{F(j_{Q X})}{\longrightarrow}& F(P Q X)
   &=&
   \tilde F(\gamma_{P,Q}(X))
    \\
    & {}^{\mathllap{F(f)}}\downarrow
     &&
     && \downarrow^{\mathrlap{F(P Q f)}}
     && \downarrow^{\tilde F(\gamma_{P,Q}(f))}
    \\
    \rho_Y\colon& F(Y) &\underoverset{F(p_y)^{-1}}{iso}{\longrightarrow}& F(Q Y) &\underoverset{F(j_{Q Y})}{iso}{\longrightarrow}& F(P Q Y)
   &=&
   \tilde F(\gamma_{P,Q}(X))
  }
  \,.
$$

=--

+-- {: .num_remark #EssentialUniquenessOfLocalizationFunctorOfModelCategory}
###### Remark

Due to theorem \ref{UniversalPropertyOfHomotopyCategoryOfAModelCategory} we may suppress the choices of cofibrant $Q$ and fibrant replacement $P$ in def. \ref{FibrantCofibrantReplacementFunctorToHomotopyCategory} and just speak of [[generalized the|the]] [[localization functor]]

$$
  \gamma \;\colon\;
  \mathcal{C}
  \longrightarrow
  Ho(\mathcal{C})
$$

up to [[natural isomorphism]].

=--

In general, the localization $\mathcal{C}[W^{-1}]$ of a [[category with weak equivalences]] $(\mathcal{C},W)$ (def. \ref{HomotopyCategoryOfACategoryWithWeakEquivalences}) may invert _more_ morphisms than just those in $W$. However, if the category admits the structure of a [[model category]] $(\mathcal{C},W,Cof,Fib)$, then its localization precisely only inverts the weak equivalences:

+-- {: .num_prop #MorphismIsWeakEquivalenceIfIsoInHomotopyCategoryForQuillen}
###### Proposition

Let $\mathcal{C}$ be a [[model category]] (def. \ref{ModelCategory}) and let $\gamma \;\colon\; \mathcal{C} \longrightarrow Ho(\mathcal{C})$ be its [[localization]] functor (def. \ref{FibrantCofibrantReplacementFunctorToHomotopyCategory}, theorem \ref{UniversalPropertyOfHomotopyCategoryOfAModelCategory}). Then a morphism $f$ in $\mathcal{C}$ is a [[weak equivalence]] precisely if $\gamma(f)$ is an [[isomorphism]] in $Ho(\mathcal{C})$.

=--

(e.g. [Goerss-Jardine 96, II, prop 1.14 ](Simplicial+homotopy+Theory))


While the construction of the homotopy category in def. \ref{HomotopyCategoryOfAModelCategory} combines the restriction to good (fibrant/cofibrant) objects with the passage to [[homotopy classes]] of morphisms, it is often useful to consider intermediate stages:

+-- {: .num_defn #FullSubcategoriesOfFibrantCofibrantObjects}
###### Definition

Given a [[model category]] $\mathcal{C}$, write

$$
  \array{
   && \mathcal{C}_{f c}
   \\
   & \swarrow && \searrow
   \\
   \mathcal{C}_c && && \mathcal{C}_f
   \\
   & \searrow && \swarrow
   \\
   && \mathcal{C}
  }
$$

for the system of [[full subcategory]] inclusions of:

1. the [[category of fibrant objects]] $\mathcal{C}_f$

1. the [[category of cofibrant objects]] $\mathcal{C}_c$,

1. the category of fibrant-cofibrant objects $\mathcal{C}_{fc}$,

all regarded a [[categories with weak equivalences]] (def. \ref{CategoryWithWeakEquivalences}), via the weak equivalences inherited from $\mathcal{C}$, which we write $(\mathcal{C}_f, W_f)$, $(\mathcal{C}_c, W_c)$ and $(\mathcal{C}_{f c}, W_{f c})$.


=--

+-- {: .num_remark}
###### Remark

Of course the subcategories in def. \ref{FullSubcategoriesOfFibrantCofibrantObjects} inherit more structure than just that of [[categories with weak equivalences]] from $\mathcal{C}$. $\mathcal{C}_f$ and $\mathcal{C}_c$ each inherit "half" of the factorization axioms. One says that $\mathcal{C}_f$ has the structure of a "[[fibration category]]" called a "Brown-[[category of fibrant objects]]", while $\mathcal{C}_c$ has the structure of a "[[cofibration category]]".

We discuss properties of these categories of (co-)fibrant objects below in _[Homotopy fiber sequences](#HomotopyFiberSequences)_.

=--

The proof of theorem \ref{UniversalPropertyOfHomotopyCategoryOfAModelCategory} immediately implies the following:

+-- {: .num_cor #HomotopyCategoryOfSubcategoriesOfModelCategoriesOnGoodObjects}
###### Corollary

For $\mathcal{C}$ a [[model category]], the restriction of the localization functor $\gamma\;\colon\; \mathcal{C} \longrightarrow Ho(\mathcal{C})$ from def. \ref{FibrantCofibrantReplacementFunctorToHomotopyCategory} (using remark \ref{EssentialUniquenessOfLocalizationFunctorOfModelCategory}) to any of the sub-[[categories with weak equivalences]] of def. \ref{FullSubcategoriesOfFibrantCofibrantObjects}

$$
  \array{
   && \mathcal{C}_{f c}
   \\
   & \swarrow && \searrow
   \\
   \mathcal{C}_c && && \mathcal{C}_f
   \\
   & \searrow && \swarrow
   \\
   && \mathcal{C}
   \\
   && \downarrow^{\mathrlap{\gamma}}
   \\
   && Ho(\mathcal{C})
  }
$$

exhibits $Ho(\mathcal{C})$ equivalently as the [[localization]] also of these subcategories with weak equivalences, at their weak equivalences. In particular there are [[equivalences of categories]]

$$
  Ho(\mathcal{C})
    \simeq
  \mathcal{C}[W^{-1}]
   \simeq
  \mathcal{C}_f[W_f^{-1}]
   \simeq
  \mathcal{C}_c[W_c^{-1}]
    \simeq
  \mathcal{C}_{f c}[W_{f c}^{-1}]
  \,.
$$

=--

The following says that for computing the hom-sets in the [[homotopy category of a model category|homotopy category]], even a mixed variant of the above will do; it is sufficient that the domain is cofibrant and the codomain is fibrant:

+-- {: .num_lemma #HomsOutOfCofibrantIntoFibrantComputeHomotopyCategory}
###### Lemma

For $X, Y \in \mathcal{C}$ with $X$ cofibrant and $Y$ fibrant, and for $P, Q$ fibrant/cofibrant replacement functors as in def. \ref{FibrantCofibrantReplacementFunctorToHomotopyCategory}, the morphism

$$
 Hom_{Ho(\mathcal{C})}(P X,Q Y)
  =
 Hom_{\mathcal{C}}(P X, Q Y)/_{\sim}
   \overset{Hom_{\mathcal{C}}(j_X, p_Y)}{\longrightarrow}
 Hom_{\mathcal{C}}(X,Y)/_{\sim}
$$

(on [[homotopy classes]] of morphisms, well defined by prop. \ref{BetweenCofibFibLeftAndRightHomotopyAreEquivalentEquivalenceRelations}) is a [[natural bijection]].

=--

([Quillen 67, I.1 corollary 1](#Quillen67))

+-- {: .proof}
###### Proof

We may factor the morphism in question as the composite

$$
  Hom_{\mathcal{C}}(P X, Q Y)/_{\sim}
    \overset{Hom_{\mathcal{C}}(id_{P X}, p_Y)/_\sim }{\longrightarrow}
  Hom_{\mathcal{C}}(P X, Y)/_{\sim}
    \overset{Hom_{\mathcal{C}}(j_X, id_Y)/_\sim}{\longrightarrow}
  Hom_{\mathcal{C}}(X,Y)/_{\sim}
  \,.
$$

This shows that it is sufficient to see that for $X$ cofibrant and $Y$ fibrant, then

$$
  Hom_{\mathcal{C}}(id_X, p_Y)/_\sim
   \;\colon\;
  Hom_{\mathcal{C}}(X, Q Y)/_\sim \to Hom_{\mathcal{C}}(X,Y)/_\sim
$$

is an isomorphism, and dually that

$$
  Hom_{\mathcal{C}}(j_X, id_Y)/_\sim
  \;\colon\;
  Hom_{\mathcal{C}}(P X, Y)/_\sim \to Hom_{\mathcal{C}}(X,Y)/_\sim
$$

is an isomorphism. We discuss this for the former; the second is [[formal dual|formally dual]]:

First, that $Hom_{\mathcal{C}}(id_X, p_Y)$ is surjective is the [[lifting property]] in

$$
  \array{
    \emptyset &\longrightarrow& Q Y
    \\
    {}^{\mathllap{\in Cof}}\downarrow && \downarrow^{\mathrlap{p_Y}}_{\mathrlap{\in W \cap Fib}}
    \\
    X &\overset{f}{\longrightarrow}& Y
  }
  \,,
$$

which says that any morphism $f \colon X \to Y$ comes from a morphism $\hat f \colon X \to Q Y$ under postcomposition with $Q Y \overset{p_Y}{\to} Y$.

Second, that $Hom_{\mathcal{C}}(id_X, p_Y)$ is injective is the lifting property in

$$
  \array{
    X \sqcup X &\overset{(f,g)}{\longrightarrow}& Q Y
    \\
    {}^{\mathllap{\in Cof}}\downarrow && \downarrow^{\mathrlap{p_Y}}_{\mathrlap{\in W \cap Fib}}
    \\
    Cyl(X) &\underset{\eta}{\longrightarrow}& Y
  }
  \,,
$$

which says that if two morphisms $f, g \colon X \to Q Y$ become homotopic after postcomposition with $p_Y \colon Q X \to Y$, then they were already homotopic before.

=--

We record the following fact which will be used in [[Introduction to Stable homotopy theory -- 1-1|part 1.1]] ([here](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyCategoryIsTriangulated)):

+-- {: .num_lemma #RepresentingHomotopyCommutativeSquaresByCommutativeSquares}
###### Lemma

Let $\mathcal{C}$ be a [[model category]] (def. \ref{ModelCategory}). Then every [[commuting square]] in its [[homotopy category]] $Ho(C)$ (def. \ref{HomotopyCategoryOfAModelCategory}) is, up to [[isomorphism]] of squares, in the image of the [[localization]] functor $\mathcal{C} \longrightarrow Ho(\mathcal{C})$ of a commuting square in $\mathcal{C}$ (i.e.: not just commuting up to homotopy).

=--

+-- {: .proof}
###### Proof

Let

$$
  \array{
    A &\overset{f}{\longrightarrow}& B
    \\
    {}^{\mathllap{a}}\downarrow
      &&
    \downarrow^{\mathrlap{b}}
    \\
    A' &\underset{f'}{\longrightarrow}& B'
  }
  \;\;\;\;\;
  \in Ho(\mathcal{C})
$$

be a commuting square in the homotopy category. Writing the same symbols for fibrant-cofibrant objects in $\mathcal{C}$ and for morphisms in $\mathcal{C}$ representing these, then this means that in $\mathcal{C}$ there is a [[left homotopy]] of the form

$$
  \array{
    A &\overset{f}{\longrightarrow}& B
    \\
    {}^{\mathllap{i_1}}\downarrow && \downarrow^{\mathrlap{b}}
    \\
    Cyl(A) &\underset{\eta}{\longrightarrow}& B'
    \\
    {}^{\mathllap{i_0}}\uparrow && \uparrow^{\mathrlap{f'}}
    \\
    A &\underset{a}{\longrightarrow}& A'
  }
  \,.
$$

Consider the factorization of the top square here through the [[mapping cylinder]] of $f$

$$
  \array{
    A &\overset{f}{\longrightarrow}& B
    \\
    {}^{\mathllap{i_1}}\downarrow &(po)& \downarrow^{\mathrlap{\in W}}
    \\
    Cyl(A) &\underset{}{\longrightarrow}& Cyl(f)
    \\
    {}^{\mathllap{i_0}}\uparrow &{}_{\mathllap{\eta}}\searrow& \downarrow^{\mathrlap{}}
    \\
    A && B'
    \\
    & {}_{\mathllap{a}}\searrow & \uparrow_{\mathrlap{f'}}
    \\
    && A'
  }
$$

This exhibits the composite $A \overset{i_0}{\to} Cyl(A) \to Cyl(f)$ as an alternative representative of $f$ in $Ho(\mathcal{C})$, and $Cyl(f) \to B'$ as an alternative representative for $b$, and the commuting square

$$
  \array{
    A &\overset{}{\longrightarrow}& Cyl(f)
    \\
    {}^{\mathllap{a}}\downarrow
      &&
    \downarrow
    \\
    A' &\underset{f'}{\longrightarrow}& B'
  }
$$

as an alternative representative of the given commuting square in $Ho(\mathcal{C})$.

=--




### Derived functors
 {#DerivedFunctors}


+-- {: .num_defn #HomotopicalFunctor}
###### Definition

For $\mathcal{C}$ and $\mathcal{D}$ two [[categories with weak equivalences]], def. \ref{CategoryWithWeakEquivalences}, then a [[functor]] $F \colon \mathcal{C}\longrightarrow \mathcal{D}$ is called a **[[homotopical functor]]** if it sends weak equivalences to weak equivalences.

=--

+-- {: .num_defn #DerivedFunctorOfAHomotopicalFunctor}
###### Definition

Given a [[homotopical functor]] $F \colon \mathcal{C} \longrightarrow \mathcal{D}$ (def. \ref{HomotopicalFunctor}) between [[categories with weak equivalences]] whose [[homotopy categories]] $Ho(\mathcal{C})$ and $Ho(\mathcal{D})$ exist (def. \ref{HomotopyCategoryOfACategoryWithWeakEquivalences}), then its ("[[total derived functor|total]]") _[[derived functor]]_ is the functor $Ho(F)$ between these homotopy categories which is induced uniquely, up to unique isomorphism, by their universal property (def. \ref{HomotopyCategoryOfACategoryWithWeakEquivalences}):

$$
  \array{
    \mathcal{C} &\overset{F}{\longrightarrow}& \mathcal{D}
    \\
    {}^{\mathllap{\gamma_{\mathcal{C}}}}\downarrow
    &\swArrow_{\simeq}&
    \downarrow^{\mathrlap{\gamma_{\mathcal{D}}}}
    \\
    Ho(\mathcal{C})
      &\underset{\exists \; Ho(F)}{\longrightarrow}&
    Ho(\mathcal{D})
  }
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

While many functors of interest between [[model categories]] are not homotopical in the sense of def. \ref{HomotopicalFunctor}, many become homotopical after restriction to the [[full subcategories]] $\mathcal{C}_f$ [[category of fibrant objects|of fibrant objects]] or $\mathcal{C}_c$ [[category of cofibrant objects|of cofibrant objects]], def. \ref{FullSubcategoriesOfFibrantCofibrantObjects}. By corollary \ref{HomotopyCategoryOfSubcategoriesOfModelCategoriesOnGoodObjects} this is just as good for the purpose of [[homotopy theory]].

=--

Therefore one considers the following generalization of def. \ref{DerivedFunctorOfAHomotopicalFunctor}:

+-- {: .num_defn #LeftAndRightDerivedFunctorsOnModelCategories}
###### Definition
**(left and right [[derived functors]])**

Consider a functor $F \colon \mathcal{C} \longrightarrow \mathcal{D}$ out of a [[model category]] $\mathcal{C}$ (def. \ref{ModelCategory}) into a [[category with weak equivalences]] $\mathcal{D}$ (def. \ref{CategoryWithWeakEquivalences}).

1. If the restriction of $F$ to the [[full subcategory]] $\mathcal{C}_f$ of fibrant object becomes a [[homotopical functor]] (def. \ref{HomotopicalFunctor}), then the [[derived functor]] of that restriction, according to def. \ref{DerivedFunctorOfAHomotopicalFunctor}, is called the _[[right derived functor]]_ of $F$ and denoted by $\mathbb{R}F$:

   $$
     \array{
       & \mathcal{C}_f &\hookrightarrow& \mathcal{C} &\overset{F}{\longrightarrow}& \mathcal{D}
       \\
       &
       {}^{\mathllap{\gamma}_{\mathcal{C}_f}}
       \downarrow
       &&
       \swArrow_{\simeq}
       &&
       \downarrow^{\mathrlap{\gamma_{\mathcal{D}}}}
       \\
       \mathbb{R} F \colon & \mathcal{C}_f[W^{-1}] &\simeq& Ho(\mathcal{C})
       &\underset{Ho(F)}{\longrightarrow}& Ho(\mathcal{D})
     }
     \,,
   $$

   where we use corollary \ref{HomotopyCategoryOfSubcategoriesOfModelCategoriesOnGoodObjects}.

1. If the restriction of $F$ to the [[full subcategory]] $\mathcal{C}_c$ of cofibrant object becomes a homotopical functor (def. \ref{HomotopicalFunctor}), then the [[derived functor]] of that restriction, according to def. \ref{DerivedFunctorOfAHomotopicalFunctor}, is called the _[[left derived functor]]_ of $F$ and denoted by $\mathbb{L}F$:

   $$
     \array{
       & \mathcal{C}_c &\hookrightarrow& \mathcal{C} &\overset{F}{\longrightarrow}& \mathcal{D}
       \\
       &
       {}^{\mathllap{\gamma}_{\mathcal{C}_f}}\downarrow
       &&
       \swArrow_{\simeq}
       &&
       \downarrow^{\mathrlap{\gamma_{\mathcal{D}}}}
       \\
       \mathbb{L} F \colon & \mathcal{C}_c[W^{-1}] &\simeq& Ho(\mathcal{C})
       &\underset{Ho(F)}{\longrightarrow}& Ho(\mathcal{D})
     }
     \,,
   $$

   where again we use corollary \ref{HomotopyCategoryOfSubcategoriesOfModelCategoriesOnGoodObjects}.

=--

The key fact that makes def. \ref{LeftAndRightDerivedFunctorsOnModelCategories} practically relevant is the following:

+-- {: .num_prop #KenBrownLemma}
###### Proposition
**([[Ken Brown's lemma]])**

Let $\mathcal{C}$ be a [[model category]] with [[full subcategories]] $\mathcal{C}_f, \mathcal{C}_c$ [[category of fibrant objects|of fibrant objects]] and [[cofibration category|of cofibrant objects]] respectively (def. \ref{FullSubcategoriesOfFibrantCofibrantObjects}). Let $\mathcal{D}$ be a [[category with weak equivalences]].

1. A [[functor]] out of the [[category of fibrant objects]]

   $$
     F \;\colon\; \mathcal{C}_f \longrightarrow \mathcal{D}
   $$

   is a [[homotopical functor]], def. \ref{HomotopicalFunctor}, already if it sends acylic fibrations to weak equivalences.

1. A [[functor]] out of the [[category of cofibrant objects]]

   $$
     F \;\colon\; \mathcal{C}_c \longrightarrow \mathcal{D}
   $$

   is a [[homotopical functor]], def. \ref{HomotopicalFunctor}, already if it sends acylic cofibrations to weak equivalences.

=--

The following proof refers to the [[factorization lemma]], whose full statement and proof we postpone to further below (lemma \ref{FactorizationLemma}).

+-- {: .proof}
###### Proof

We discuss the case of a functor on a [[category of fibrant objects]] $\mathcal{C}_f$, def. \ref{FullSubcategoriesOfFibrantCofibrantObjects}. The other case is [[formal dual|formally dual]].

Let $f \colon X \longrightarrow Y$ be a weak equivalence in $\mathcal{C}_f$. Choose a [[path space object]] $Path(X)$ (def. \ref{PathAndCylinderObjectsInAModelCategory}) and consider the diagram

$$
  \array{
    Path(f) &\underset{\in W \cap Fib}{\longrightarrow}& X
    \\
    {}^{\mathllap{p_1^\ast f}}_{\mathllap{\in W}}\downarrow
    &(pb)&
    \downarrow^{\mathrlap{f}}_{\mathrlap{\in W}}
    \\
    Path(Y) &\overset{p_1}{\underset{\in W \cap Fib}{\longrightarrow}}& Y
    \\
    {}^{\mathllap{p_0}}_{\mathllap{\in W \cap Fib}}\downarrow
    \\
    Y
  }
  \,,
$$

where the square is a [[pullback]] and $Path(f)$ on the top left is our notation for the universal [[cone]] object. (Below we discuss this in more detail, it is the _[[mapping cocone]]_ of $f$, def. \ref{MappingConeAndMappingCocone}).

Here:

1. $p_i$ are both acyclic fibrations, by lemma \ref{ComponentMapsOfCylinderAndPathSpaceInGoodSituation};

1. $Path(f) \to X$ is an acyclic fibration because it is the pullback of $p_1$.

1. $p_1^\ast f$ is a weak equivalence, because the [[factorization lemma]] \ref{FactorizationLemma} states that the composite vertical morphism factors $f$ through a weak equivalence, hence if $f$ is a weak equivalence, then $p_1^\ast f$ is by [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}).

Now apply the functor $F$ to this diagram and use the assumption that it sends acyclic fibrations to weak equivalences to obtain

$$
  \array{
    F(Path(f)) &\underset{\in W }{\longrightarrow}& F(X)
    \\
    {}^{\mathllap{F(p_1^\ast f)}}_{\mathllap{}}\downarrow && \downarrow^{\mathrlap{F(f)}}
    \\
    F(Path(Y)) &\overset{F(p_1)}{\underset{\in W }{\longrightarrow}}& F(Y)
    \\
    {}^{\mathllap{F(p_0)}}_{\mathllap{\in W}}\downarrow
    \\
    Y
  }
  \,.
$$

But the [[factorization lemma]] \ref{FactorizationLemma}, in addition says that the vertical composite $p_0 \circ p_1^\ast f$ is a fibration, hence an acyclic fibration by the above. Therefore also $F(p_0 \circ p_1^\ast f)$ is a weak equivalence. Now the claim that also $F(f)$ is a weak equivalence follows with applying [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}) twice.

=--

+-- {: .num_cor #LeftAndRightDerivedFunctors}
###### Corollary

Let $\mathcal{C}, \mathcal{D}$ be [[model categories]] and consider $F \colon \mathcal{C}\longrightarrow \mathcal{D}$ a [[functor]]. Then:

1. If $F$ preserves cofibrant objects and acyclic cofibrations between these, then its [[left derived functor]] (def. \ref{LeftAndRightDerivedFunctorsOnModelCategories}) $\mathbb{L}F$ exists, fitting into a [[diagram]]

   $$
     \array{
       \mathcal{C}_{c} &\overset{F}{\longrightarrow}& \mathcal{D}_{c}
       \\
       {}^{\mathllap{\gamma_{\mathcal{C}}}}\downarrow
       &\swArrow_{\simeq}&
       \downarrow^{\mathrlap{\gamma_{\mathcal{D}}}}
       \\
       Ho(\mathcal{C}) &\overset{\mathbb{L}F}{\longrightarrow}& Ho(\mathcal{D})
     }
   $$

1. If $F$ preserves fibrant objects and acyclic fibrants between these, then its [[right derived functor]] (def. \ref{LeftAndRightDerivedFunctorsOnModelCategories}) $\mathbb{R}F$ exists, fitting into a [[diagram]]

   $$
     \array{
       \mathcal{C}_{f} &\overset{F}{\longrightarrow}& \mathcal{D}_{f}
       \\
       {}^{\mathllap{\gamma_{\mathcal{C}}}}\downarrow
       &\swArrow_{\simeq}&
       \downarrow^{\mathrlap{\gamma_{\mathcal{D}}}}
       \\
       Ho(\mathcal{C}) &\underset{\mathbb{R}F}{\longrightarrow}& Ho(\mathcal{D})
     }
     \,.
   $$

=--

+-- {: .num_example #ComputationOfLeftRightDerivedFunctorsViaResolutions}
###### Proposition

Let $F \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}$ be a functor between two [[model categories]] (def. \ref{ModelCategory}).

1. If $F$ preserves fibrant objects and weak equivalences between fibrant objects, then the total [[right derived functor]] $\mathbb{R}F \coloneqq \mathbb{R}(\gamma_{\mathcal{D}}\circ F)$ (def. \ref{LeftAndRightDerivedFunctorsOnModelCategories}) in

   $$
     \array{
       \mathcal{C}_f &\overset{F}{\longrightarrow}& \mathcal{D}
       \\
       {}^{\mathllap{\gamma_{\mathcal{C}_f}}}\downarrow
         &\swArrow_{\simeq}&
       \downarrow^{\mathrlap{\gamma_{\mathcal{D}}}}
       \\
       Ho(\mathcal{C})
         &\underset{\mathbb{R}F}{\longrightarrow}&
       Ho(\mathcal{D})
     }
   $$

   is given, up to isomorphism, on any object $ X\in \mathcal{C} \overset{\gamma_{\mathcal{C}}}{\longrightarrow} Ho(\mathcal{C})$ by applying $F$ to a [[fibrant replacement]] $P X$ of $X$ and then forming a cofibrant replacement $Q(F(P X))$ of the result:


  $$
    \mathbb{R}F(X)
      \simeq
    Q(F(P X))
    \,.
  $$

1. If $F$ preserves cofibrant objects and weak equivalences between cofibrant objects, then the total [[left derived functor]] $\mathbb{L}F \coloneqq \mathbb{L}(\gamma_{\mathcal{D}}\circ F)$ (def. \ref{LeftAndRightDerivedFunctorsOnModelCategories}) in

   $$
     \array{
       \mathcal{C}_c &\overset{F}{\longrightarrow}& \mathcal{D}
       \\
       {}^{\mathllap{\gamma_{\mathcal{C}_c}}}\downarrow
         &\swArrow_{\simeq}&
       \downarrow^{\mathrlap{\gamma_{\mathcal{D}}}}
       \\
       Ho(\mathcal{C})
         &\underset{\mathbb{L}F}{\longrightarrow}&
       Ho(\mathcal{D})
     }
   $$

   is given, up to isomorphism, on any object $ X\in \mathcal{C} \overset{\gamma_{\mathcal{C}}}{\longrightarrow} Ho(\mathcal{C})$ by appying $F$ to a cofibrant replacement $Q X$ of $X$ and then forming a fibrant replacement $P(F(Q X))$ of the result:


  $$
    \mathbb{L}F(X)
      \simeq
    P(F(Q X))
    \,.
  $$



=--

+-- {: .proof}
###### Proof

We discuss the first case, the second is [[formal duality|formally dual]]. By the proof of theorem \ref{UniversalPropertyOfHomotopyCategoryOfAModelCategory} we have

$$
  \begin{aligned}
    \mathbb{R}F(X)
      & \simeq
    \gamma_{\mathcal{D}}(F(\gamma_{\mathcal{C}}))
    \\
      & \simeq
     \gamma_{\mathcal{D}}F(Q(P(X)) )
  \end{aligned}
  \,.
$$

But since $F$ is a homotopical functor on fibrant objects, the cofibrant replacement morphism $F(Q(P(X)))\to F(P(X))$ is a weak equivalence in $\mathcal{D}$, hence becomes an isomorphism under $\gamma_{\mathcal{D}}$. Therefore

$$
  \mathbb{R}F(X)
    \simeq
  \gamma_{\mathcal{D}}(F(P(X)))
  \,.
$$

Now since $F$ is assumed to preserve fibrant objects, $F(P(X))$ is fibrant in $\mathcal{D}$, and hence $\gamma_{\mathcal{D}}$ acts on it (only) by cofibrant replacement.

=--





### Quillen adjunctions
 {#QuillenAdjunctions}

In practice it turns out to be useful to arrange for the assumptions in corollary \ref{LeftAndRightDerivedFunctors} to be satisfied by pairs of [[adjoint functors]]. Recall that this is a pair of [[functors]] $L$ and $R$ going back and forth between two categories

$$
  \mathcal{C}
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{L}{\longleftarrow}}
      {}
  \mathcal{D}
$$

such that there is a [[natural bijection]] between [[hom-sets]] with $L$ on the left and those with $R$ on the right:

$$
  \phi_{d,c}
   \;\colon\;
  Hom_{\mathcal{C}}(L(d),c)
   \underoverset{\simeq}{}{\longrightarrow}
  Hom_{\mathcal{D}}(d, R(c))
$$

for all objects $d\in \mathcal{D}$ and $c \in \mathcal{C}$. This being natural means that $\phi \colon Hom_{\mathcal{D}}(L(-),-) \Rightarrow Hom_{\mathcal{C}}(-, R(-))$ is a [[natural transformation]], hence that for all morphisms $g \colon d_2 \to d_1$ and $f \colon c_1 \to c_2$ the following is a [[commuting square]]:

$$
  \array{
    Hom_{\mathcal{C}}(L(d_1), c_1)
     & \underoverset{\simeq}{\phi_{d_1,c_1}}{\longrightarrow} &
    Hom_{\mathcal{D}}(d_1, R(c_1))
    \\
    {}^{\mathllap{L(f) \circ (-)\circ g}}\downarrow
     &&
    \downarrow^{\mathrlap{g\circ (-)\circ R(g)}}
    \\
    Hom_{\mathcal{C}}(L(d_2), c_2)
     & \underoverset{\phi_{d_2, c_2}}{\simeq}{\longrightarrow} &
    Hom_{\mathcal{D}}(d_2, R(c_2))
  }
  \,.
$$

We write $(L \dashv R)$ to indicate an adjunction and call $L$ the _[[left adjoint]]_ and $R$ the _[[right adjoint]]_ of the adjoint pair.

The archetypical example of a pair of adjoint functors is that consisting of forming [[Cartesian products]] $Y \times (-)$ and forming [[mapping spaces]] $(-)^Y$, as in the category of [[compactly generated topological spaces]] of def. \ref{kTop}.

If $f \colon L(d) \to c$ is any morphism, then the image $\phi_{d,c}(f) \colon d \to R(c)$ is called its _[[adjunct]]_, and conversely. The fact that adjuncts are in bijection is also expressed by the notation

$$
  \frac{
    L(c) \overset{f}{\longrightarrow} d
  }{
    c \overset{\tilde f}{\longrightarrow} R(d)
  }
  \,.
$$

For an object $d\in \mathcal{D}$, the [[adjunct]] of the identity on $L d$ is called the _[[adjunction unit]]_ $\eta_d \;\colon\; d \longrightarrow R L d$.

For an object $c \in \mathcal{C}$, the [[adjunct]] of the identity on $R c$ is called the _[[adjunction counit]]_ $\epsilon_c \;\colon\; L R c \longrightarrow c$.

Adjunction units and counits turn out to encode the [[adjuncts]] of all other morphisms by the formulas

* $\widetilde{(L d\overset{f}{\to}c)} = (d\overset{\eta}{\to} R L d \overset{R f}{\to} R c)$

* $\widetilde{(d\overset{g}{\to} R c)} = (L d \overset{L g}{\to} L R c \overset{\epsilon}{\to} c)$.


+-- {: .num_defn #QuillenAdjunction}
###### Definition

Let $\mathcal{C}, \mathcal{D}$ be [[model categories]]. A pair of [[adjoint functors]] between them

$$
  (L \dashv R)
  \;\colon\;
  \mathcal{C}
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{L}{\longleftarrow}}
      {}
  \mathcal{D}
$$

is called a **[[Quillen adjunction]]** (and $L$,$R$ are called left/right **Quillen functors**, respectively) if the following equivalent conditions are satisfied

1. $L$ preserves cofibrations and $R$ preserves fibrations;

1. $L$ preserves acyclic cofibrations and $R$ preserves acyclic fibrations;

1. $L$ preserves cofibrations and acylic cofibrations;

1. $R$ preserves fibrations and acyclic fibrations.


=--

\begin{proposition}\label{ConditionsOnQuillenAdjunctionAreIndeedEquivalent}
The conditions in def. \ref{QuillenAdjunction} are indeed all equivalent.
\end{proposition}

([Quillen 67, I.4, theorem 3](#Quillen67))

+-- {: .proof}
###### Proof

First observe that

* (i) _A [[left adjoint]] $L$ between [[model categories]] preserves acyclic cofibrations precisely if its [[right adjoint]] $R$ preserves fibrations.

* (ii) _A [[left adjoint]] $L$ between [[model categories]] preserves cofibrations precisely if its [[right adjoint]] $R$ preserves acyclic fibrations.

We discuss statement (i), statement (ii) is [[formal dual|formally dual]].  So let $f\colon A \to B$ be an acyclic cofibration in $\mathcal{D}$ and $g \colon X \to Y$ a fibration in $\mathcal{C}$. Then for every [[commuting diagram]] as on the left of the following, its $(L\dashv R)$-[[adjunct]] is a commuting diagram as on the right here:

$$
  \array{
    A &\longrightarrow& R(X)
    \\
    {}^{\mathllap{f}}\downarrow && \downarrow^{\mathrlap{R(g)}}
    \\
    B &\longrightarrow& R(Y)
  }
  \;\;\;\;\;\;
  \,,
  \;\;\;\;\;\;
  \array{
    L(A) &\longrightarrow& X
    \\
    {}^{\mathllap{L(f)}}\downarrow && \downarrow^{\mathrlap{g}}
    \\
    L(B) &\longrightarrow& Y
  }
  \,.
$$

If $L$ preserves acyclic cofibrations, then the diagram on the right has a [[lift]], and so the $(L\dashv R)$-[[adjunct]] of that lift is a lift of the left diagram. This shows that $R(g)$ has the [[right lifting property]] against all acylic cofibrations and hence is a fibration.
Conversely, if $R$ preserves fibrations, the same argument run from right to left gives that $L$ preserves acyclic fibrations.

Now by repeatedly applying (i) and (ii), all four conditions in question are seen to be equivalent.

=--

+-- {: .num_lemma #LeftRightQuillenFunctorsPreserveCyclinderPathSpaceObjects}
###### Lemma

Let $\mathcal{C} \stackrel{\overset{L}{\longleftarrow}}{\underoverset{R}{\bot}{\longrightarrow}} \mathcal{D}$ be a [[Quillen adjunction]], def. \ref{QuillenAdjunction}.

1. For $X \in \mathcal{C}$ a fibrant object and $Path(X)$ a [[path space object]] (def. \ref{PathAndCylinderObjectsInAModelCategory}), then $R(Path(X))$ is a path space object for $R(X)$.

1. For $X \in \mathcal{C}$ a cofibrant object and $Cyl(X)$ a [[cylinder object]] (def. \ref{PathAndCylinderObjectsInAModelCategory}), then $L(Cyl(X))$ is a cylinder object for $L(X)$.

=--

+-- {: .proof}
###### Proof

Consider the second case, the first is [[formal dual|formally dual]].

First observe that  $L(X \sqcup X) \simeq L X \sqcup L X$ because $L$ is [[left adjoint]] and hence preserves [[colimits]], hence in particular [[coproducts]].

Hence

$$
  L(X \sqcup X \overset{\in Cof}{\to} Cyl(X))
  =
  (L(X) \sqcup L(X) \overset{\in Cof}{\to } L (Cyl(X)))
$$

is a cofibration.

Second, with $X$ cofibrant $i_0 \colon X \to X \sqcup X$ is an acyclic cofibration (lemma \ref{ComponentMapsOfCylinderAndPathSpaceInGoodSituation}), and so then is

$$
  i_0 \; \colon \; L(X) \longrightarrow L(X) \sqcup L(X).
$$

Therefore by [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}) $L$ preserves the weak equivalence $Cyl(X) \to X$.

=--

\begin{proposition}\label{QuillenAdjunctionInducesAdjunctionOnHomotopyCategories}
**([[derived adjunction]])** \linebreak

For $\mathcal{C} \underoverset{\underset{R}{\longrightarrow}}{\overset{L}{\longleftarrow}}{\bot_{Qu}}\mathcal{D}$ a [[Quillen adjunction]], def. \ref{QuillenAdjunction}, then also the corresponding left and right [[derived functors]], def. \ref{LeftAndRightDerivedFunctorsOnModelCategories}, via cor. \ref{LeftAndRightDerivedFunctors}, form a pair of [[adjoint functors]]

$$
  Ho(\mathcal{C})
    \underoverset
      {\underset{\mathbb{R}R}{\longrightarrow}}
      {\overset{\mathbb{L}L}{\longleftarrow}}
      {\bot}
  Ho(\mathcal{D})
  \,.
$$

\end{proposition}

([Quillen 67, I.4 theorem 3](#Quillen67))

+-- {: .proof}
###### Proof

By def. \ref{LeftAndRightDerivedFunctorsOnModelCategories} and lemma \ref{HomsOutOfCofibrantIntoFibrantComputeHomotopyCategory} it is sufficient to see that for $X, Y \in \mathcal{C}$ with $X$ cofibrant and $Y$ fibrant, then there is a [[natural bijection]]

$$
  Hom_{\mathcal{C}}(L X , Y)/_\sim
   \simeq
  Hom_{\mathcal{D}}(X, R Y)/_\sim
  \,.
$$

Since by the [[adjoint functor|adjunction isomorphism]] for $(L \dashv R)$ such a natural bijection exists before passing to homotopy classes $(-)/_\sim$, it is sufficient to see that this respects homotopy classes. To that end, use from lemma \ref{LeftRightQuillenFunctorsPreserveCyclinderPathSpaceObjects} that with $Cyl(Y)$ a [[cylinder object]] for $Y$, def. \ref{PathAndCylinderObjectsInAModelCategory}, then $L(Cyl(Y))$ is a cylinder object for $L(Y)$. This implies that left homotopies

$$
  (f \Rightarrow_L g) \;\colon\;  L X \longrightarrow Y
$$

given by

$$
 \eta \;\colon\; Cyl(L X) =  L Cyl(X) \longrightarrow Y
$$

are in bijection to left homotopies

$$
  (\tilde f \Rightarrow_L \tilde g) \;\colon\; X \longrightarrow R Y
$$

given by

$$
  \tilde \eta \;\colon\; Cyl(X) \longrightarrow R X
  \,.
$$

=--

+-- {: .num_defn #QuillenEquivalence}
###### Definition

For $\mathcal{C}, \mathcal{D}$ two [[model categories]],  a [[Quillen adjunction]] (def.\ref{QuillenAdjunction})

$$
  (L \dashv R)
  \;\colon\;
  \mathcal{C}
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{L}{\longleftarrow}}
      {\bot}
  \mathcal{D}
$$

is called a **[[Quillen equivalence]]**, to be denoted

$$
  \mathcal{C}
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{L}{\longleftarrow}}
      {\simeq_{\mathrlap{Q}}}
  \mathcal{D}
  \,,
$$

if the following equivalent conditions hold.

1. The [[right derived functor]] of $R$ (via prop. \ref{ConditionsOnQuillenAdjunctionAreIndeedEquivalent}, corollary \ref{LeftAndRightDerivedFunctors}) is an [[equivalence of categories]]

   $$
     \mathbb{R}R \colon Ho(\mathcal{C}) \overset{\simeq}{\longrightarrow} Ho(\mathcal{D})
     \,.
   $$

1. The [[left derived functor]] of $L$ (via prop. \ref{ConditionsOnQuillenAdjunctionAreIndeedEquivalent}, corollary \ref{LeftAndRightDerivedFunctors}) is an [[equivalence of categories]]

   $$
     \mathbb{L}L \colon Ho(\mathcal{D}) \overset{\simeq}{\longrightarrow} Ho(\mathcal{C})
     \,.
   $$

1. For every [[cofibrant object]] $d\in \mathcal{D}$, the [[derived adjunction unit]], hence the composite

   $$
     d
       \overset{\eta}{\longrightarrow}
     R(L(d))
       \overset{R(j_{L(d)})}{\longrightarrow}
     R(P(L(d)))
   $$

   (of the [[adjunction unit]] with any [[fibrant replacement]] $P$ as in def. \ref{FibrantCofibrantReplacementFunctorToHomotopyCategory}) is a weak equivalence;

   and for every fibrant object $c \in \mathcal{C}$, the [[derived adjunction counit]], hence the composite

     $$
       L(Q(R(c)))
         \overset{L(p_{R(c)})}{\longrightarrow}
       L(R(c))
         \overset{\epsilon}{\longrightarrow}
       c
     $$

     (of the [[adjunction counit]] with any [[cofibrant replacement]] as in def. \ref{FibrantCofibrantReplacementFunctorToHomotopyCategory}) is a [[weak equivalence]].


1. For every cofibrant object $d \in \mathcal{D}$ and every fibrant object $c \in \mathcal{C}$, a morphism $d \longrightarrow R(c)$ is a weak equivalence precisely if its [[adjunct]] morphism $L(c) \to d$ is:

   $$
      \frac{
        d \overset{\in W_{\mathcal{D}}}{\longrightarrow} R(c)
      }{
         L(d) \overset{\in W_{\mathcal{C}}}{\longrightarrow} c
      }
      \,.
   $$


=--

+-- {: .num_prop #ConditionsForQuillenAdjunctionAreIndeedEquivalent}
###### Proposition

The conditions in def. \ref{QuillenEquivalence} are indeed all equivalent.

=--

([Quillen 67, I.4, theorem 3](#Quillen67))

+-- {: .proof}
###### Proof

That $1) \Leftrightarrow 2)$ follows from prop. \ref{QuillenAdjunctionInducesAdjunctionOnHomotopyCategories} (if in an adjoint pair one is an equivalence, then so is the other).

To see the equivalence $1),2) \Leftrightarrow 3)$, notice ([prop.](adjoint+functor#FullyFaithfulAndInvertibleAdjoints)) that a pair of [[adjoint functors]] is an [[equivalence of categories]] precisely if both the [[adjunction unit]] and the [[adjunction counit]] are [[natural isomorphisms]]. Hence it is sufficient to show that the morphisms called [[derived adjunction unit]] and [[derived adjunction counit]] above indeed represent the adjunction (co-)unit of $(\mathbb{L}L \dashv \mathbb{R}R)$ in the homotopy category.
We show this now for the adjunction unit, the case of the adjunction counit is formally dual.

To that end, first observe that for $d \in \mathcal{D}_c$, then the defining commuting square for the left derived functor from def. \ref{LeftAndRightDerivedFunctorsOnModelCategories}

$$
  \array{
    \mathcal{D}_c &\overset{L}{\longrightarrow}& \mathcal{C}
    \\
    {}^{\mathllap{\gamma_P}}\downarrow
      &\swArrow_{\simeq}&
    \downarrow^{\mathrlap{\gamma_{P,Q}}}
    \\
    Ho(\mathcal{D}) &\underset{\mathbb{L}L}{\longrightarrow}& Ho(\mathcal{C})
  }
$$

(using fibrant and fibrant/cofibrant replacement functors $\gamma_P$, $\gamma_{P,Q}$ from def. \ref{FibrantCofibrantReplacementFunctorToHomotopyCategory} with their universal property from theorem \ref{UniversalPropertyOfHomotopyCategoryOfAModelCategory}, corollary \ref{HomotopyCategoryOfSubcategoriesOfModelCategoriesOnGoodObjects}) gives that

$$
  (\mathbb{L} L ) d \simeq P L P d \simeq P L d \;\;\;\; \in Ho(\mathcal{C})
  \,,
$$

where the second isomorphism holds because the left Quillen functor $L$ sends the acyclic cofibration $j_d \colon d \to P d$ to a weak equivalence.

The adjunction unit of $(\mathbb{L}L \dashv \mathbb{R}R)$ on $P d \in Ho(\mathcal{C})$ is the image of the identity under

$$
  Hom_{Ho(\mathcal{C})}((\mathbb{L}L) P d, (\mathbb{L} L) P d)
  \overset{\simeq}{\to}
  Hom_{Ho(\mathcal{C})}(P d, (\mathbb{R}R)(\mathbb{L}L) P d)
  \,.
$$

By the above and the proof of prop. \ref{QuillenAdjunctionInducesAdjunctionOnHomotopyCategories}, that adjunction isomorphism is equivalently that of $(L \dashv R)$ under the isomorphism

$$
  Hom_{Ho(\mathcal{C})}(P L d , P L d)
    \overset{Hom(j_{L d}, id)}{\longrightarrow}
  Hom_{\mathcal{C}}(L d, P L d)/_\sim
$$

of lemma \ref{HomsOutOfCofibrantIntoFibrantComputeHomotopyCategory}. Hence the [[derived adjunction unit]] is the $(L \dashv R)$-[[adjunct]] of

$$
  L d
    \overset{j_{L d}}{\longrightarrow}
  P L d
    \overset{id}{\to}
  P L d
  \,,
$$

which indeed (by the formula for [[adjuncts]]) is

$$
  X
    \overset{\eta}{\longrightarrow}
  R L d
    \overset{R (j_{L d})}{\longrightarrow}
  R P L d
  \,.
$$

To see that $4) \Rightarrow 3)$:

Consider the weak equivalence $L X \overset{j_{L X}}{\longrightarrow} P L X$. Its $(L \dashv R)$-[[adjunct]] is

$$
  X
    \overset{\eta}{\longrightarrow}
  R L X
    \overset{R j_{L X}}{\longrightarrow}
  R P L X
$$

by assumption 4) this is again a weak equivalence, which is the requirement for the derived unit in 3). Dually for derived counit.

To see $3) \Rightarrow 4)$:

Consider any $f \colon L d \to c$ a weak equivalence for cofibrant $d$, firbant $c$. Its [[adjunct]] $\tilde f$ sits in a commuting diagram

$$
  \array{
    \tilde f \colon & d &\overset{\eta}{\longrightarrow}&  R L d &\overset{R f}{\longrightarrow}& R c
    \\
    & {}^{\mathllap{=}}\downarrow && \downarrow^{\mathrlap{R j_{L d}}} && \downarrow^{\mathrlap{R j_c}}
    \\
    & d &\underset{\in W}{\longrightarrow}& R P L d &\overset{R P f}{\longrightarrow}& R P c
  }
  \,,
$$

where $P f$ is any lift constructed as in def. \ref{FibrantCofibrantReplacementFunctorToHomotopyCategory}.

This exhibits the bottom left morphism as the [[derived adjunction unit]], hence a weak equivalence by assumption. But since $f$ was a weak equivalence, so is $P f$ (by [[two-out-of-three]]).  Thereby also $R P f$ and $R j_c$, are weak equivalences by [[Ken Brown's lemma]] \ref{KenBrownLemma} and the assumed fibrancy of $c$. Therefore by [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}) also the [[adjunct]] $\tilde f$ is a weak equivalence.

=--

In certain situations the conditions on a Quillen equivalence simplify. For instance:

\begin{proposition}
\label{InCaseTheRightAdjointCreatesWeakEquivalences}
If in a [[Quillen adjunction]]  $ \array{\mathcal{C} &\underoverset{\underset{R}{\to}}{\overset{L}{\leftarrow}}{\bot}& \mathcal{D}}$ (def. \ref{QuillenAdjunction}) the [[right adjoint]] $R$ "creates weak equivalences" (in that a morphism $f$ in $\mathcal{C}$ is a weak equivalence precisly if $R(f)$ is) then $(L \dashv R)$ is a [[Quillen equivalence]] (def. \ref{QuillenEquivalence}) precisely already if for all cofibrant objects $d \in \mathcal{D}$ the plain [[adjunction unit]]

$$
  d \overset{\eta}{\longrightarrow} R (L (d))
$$

is a weak equivalence.

\end{proposition}

+-- {: .proof}
###### Proof

By prop. \ref{ConditionsForQuillenAdjunctionAreIndeedEquivalent}, generally, $(L \dashv R)$ is a Quillen equivalence precisely if

1. for every cofibrant object $d\in \mathcal{D}$, the [[derived adjunction unit]]

   $$
     d
       \overset{\eta}{\longrightarrow}
     R(L(d))
       \overset{R(j_{L(d)})}{\longrightarrow}
     R(P(L(d)))
   $$

   is a weak equivalence;

1. for every fibrant object $c \in \mathcal{C}$, the [[derived adjunction counit]]

   $$
     L(Q(R(c)))
       \overset{L(p_{R(c)})}{\longrightarrow}
     L(R(c))
       \overset{\epsilon}{\longrightarrow}
     c
   $$

   is a weak equivalence.

Consider the first condition: Since $R$ preserves the weak equivalence $j_{L(d)}$, then by [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}) the composite in the first item is a weak equivalence precisely if $\eta$ is.

Hence it is now sufficient to show that in this case the second condition above is automatic.

Since $R$ also reflects weak equivalences, the composite in item two is a weak equivalence precisely if its image

$$
  R(L(Q(R(c))))
    \overset{R(L(p_{R(c))})}{\longrightarrow}
  R(L(R(c)))
    \overset{R(\epsilon)}{\longrightarrow}
  R(c)
$$

under $R$ is.

Moreover, assuming, by the above, that $\eta_{Q(R(c))}$ on the cofibrant object $Q(R(c))$ is a weak equivalence, then by [[two-out-of-three]] this composite is a weak equivalence precisely if the further composite with $\eta$ is

$$
  Q(R(c))
    \overset{\eta_{Q(R(c))}}{\longrightarrow}
  R(L(Q(R(c))))
    \overset{R(L(p_{R(c))})}{\longrightarrow}
  R(L(R(c)))
    \overset{R(\epsilon)}{\longrightarrow}
  R(c)
  \,.
$$

By the formula for [[adjuncts]], this composite is the $(L\dashv R)$-adjunct of the original composite, which is just $p_{R(c)}$

$$
  \frac{
     L(Q(R(c)))
       \overset{L(p_{R(c)})}{\longrightarrow}
     L(R(c))
       \overset{\epsilon}{\longrightarrow}
     c
  }{
     Q(R(C)) \overset{p_{R(c)}}{\longrightarrow} R(c)
  }
  \,.
$$

But $p_{R(c)}$ is a weak equivalence by definition of cofibrant replacement.


=--


## The model structure on topological spaces
 {#TheClassicalModelStructureOfTopologicalSpaces}


We now discuss how the category [[Top]] of [[topological spaces]] satisfies the axioms of abstract homotopy theory ([[model category]]) theory, def. \ref{ModelCategory}.


+-- {: .num_defn #ClassesOfMorhismsInTopQuillen}
###### Definition

Say that a [[continuous function]], hence a [[morphism]] in [[Top]], is

* a **classical weak equivalence** if it is a [[weak homotopy equivalence]], def. \ref{WeakHomotopyEquivalenceOfTopologicalSpaces};

* a **classical fibration** if it is a [[Serre fibration]], def. \ref{SerreFibration};

* a **classical cofibration** if it is a [[retract]] (rem. \ref{RetractsOfMorphisms}) of a [[relative cell complex]], def. \ref{TopologicalCellComplex}.


and hence

* a **acyclic classical cofibration** if it is a classical cofibration as well as a classical weak equivalence;

* a **acyclic classical fibration** if it is a classical fibration as well as a classical weak equivalence.

Write

$$
  W_{cl},\;Fib_{cl},\;Cof_{cl}
  \subset
  Mor(Top)
$$

for the classes of these morphisms, respectively.

=--


We first prove now that the classes of morphisms in def. \ref{ClassesOfMorhismsInTopQuillen} satisfy the conditions for a [[model category]] structure, def. \ref{ModelCategory} (after some lemmas, this is theorem \ref{TopQuillenModelStructure} below). Then we discuss the resulting [[classical homotopy category]] ([below](#TheClassicalHomotopyCategory)) and then a few variant model structures whose proof follows immediately along the line of the proof of $Top_{Quillen}$:

* [The model structure on pointed topological spaces](#ModelstructureOnPointedTopologicalSpaces) $Top^{\ast/}_{Quillen}$;

* [The model structure on compactly generated topological spaces](#ModelStructureOnCompactlyGeneratedTopologicalSpaces) $(Top_{cg})_{Quillen}$ and $(Top^{\ast/}_{cg})_{Quillen}$;

* [The model structure on topologically enriched functors](#ModelStructureOnTopEnrichedFunctors) $[\mathcal{C}, (Top_{cg})_{Quillen}]_{proj}$ and $[\mathcal{C},(Top^{\ast}_{cg})_{Quillen}]_{proj}$.


$\,$

+-- {: .num_prop #QuillenWeakEquivalencesSatisfyTwoOutOfThree}
###### Proposition

The classical weak equivalences, def. \ref{ClassesOfMorhismsInTopQuillen}, satify [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}).

=--

+-- {: .proof}
###### Proof

Since [[isomorphisms]] (of [[homotopy groups]]) satisfy 2-out-of-3, this property is directly inherited via the very definition of [[weak homotopy equivalence]], def. \ref{WeakHomotopyEquivalenceOfTopologicalSpaces}.

=--

+-- {: .num_lemma #FactorizationInTopQuillen}
###### Lemma

Every morphism $f\colon X \longrightarrow Y$ in [[Top]] factors as a classical cofibration followed by an acyclic classical fibration, def. \ref{ClassesOfMorhismsInTopQuillen}:

$$
  f
  \;\colon\;
  X
    \stackrel{\in Cof_{cl}}{\longrightarrow}
  \hat X
    \stackrel{\in W_{cl} \cap Fib_{cl}}{\longrightarrow}
  Y
  \,.
$$

=--

+-- {: .proof}
###### Proof

By lemma \ref{CompactSubsetsAreSmallInCellComplexes}
the set $I_{Top} = \{S^{n-1}\hookrightarrow D^n\}$ of
topological [[generating cofibrations]], def. \ref{TopologicalGeneratingCofibrations}, has small domains, in the sense of def. \ref{ClassOfMorphismsWithSmallDomains} (the [[n-spheres]] are [[compact topological space|compact]]). Hence by the [[small object argument]], prop. \ref{SmallObjectArgument}, $f$ factors as an $I_{Top}$-[[relative cell complex]], def. \ref{TopologicalCCellComplex}, hence just a plain relative cell complex, def. \ref{TopologicalCellComplex}, followed by an $I_{Top}$-[[injective morphisms]], def. \ref{RightLiftingProperty}:

$$
  f
  \;\colon\;
  X
   \stackrel{\in Cof_{cl}}{\longrightarrow}
  \hat X
   \stackrel{\in I_{Top} Inj}{\longrightarrow}
  Y
  \,.
$$

By lemma \ref{AcyclicSerreFibrationsAreTheJTopFibrations} the map $\hat X \to Y$ is both a [[weak homotopy equivalence]] as well as a [[Serre fibration]].

=--

+-- {: .num_lemma #ContinuousFunctionsFactorAsQuillenAcyclicCofibrationFollowedBySerreFibration}
###### Lemma

Every morphism $f\colon X \longrightarrow Y$ in [[Top]] factors as an acyclic classical cofibration followed by a fibration, def. \ref{ClassesOfMorhismsInTopQuillen}:

$$
  f
  \;\colon\;
  X
    \stackrel{\in W_{cl} \cap Cof_{cl}}{\longrightarrow}
  \hat X
    \stackrel{\in Fib_{cl}}{\longrightarrow}
  Y
  \,.
$$

=--

+-- {: .proof}
###### Proof

By lemma \ref{CompactSubsetsAreSmallInCellComplexes}
the set $J_{Top} = \{D^n \hookrightarrow D^n\times I\}$ of
topological [[generating acyclic cofibrations]], def. \ref{TopologicalGeneratingAcyclicCofibrations}, has small domains, in the sense of def. \ref{ClassOfMorphismsWithSmallDomains} (the [[n-disks]] are [[compact topological space|compact]]). Hence by the [[small object argument]], prop. \ref{SmallObjectArgument}, $f$ factors as an $J_{Top}$-[[relative cell complex]], def. \ref{TopologicalCCellComplex}, followed by a $J_{top}$-[[injective morphisms]], def. \ref{RightLiftingProperty}:

$$
  f
  \;\colon\;
  X
   \stackrel{\in J_{Top} Cell}{\longrightarrow}
  \hat X
    \stackrel{\in J_{Top} Inj}{\longrightarrow}
  Y
  \,.
$$

By definition this makes $\hat X \to Y$ a [[Serre fibration]], hence a fibration.

By lemma \ref{TopologicalGeneratingAcyclicCofibrationsAreRelativeCellComplexes} a relative $J_{Top}$-cell complex is in particular a relative $I_{Top}$-cell complex. Hence $X \to \hat X$ is a classical cofibration. By lemma \ref{JTopRelativeCellComplexesAreWeakHomotopyEquivalences} it is also a [[weak homotopy equivalence]], hence a clasical weak equivalence.

=--

+-- {: .num_lemma #LiftingPropertyInTheClassicalModelStructureOnTopologicalSpaces}
###### Lemma

Every [[commuting square]] in [[Top]] with the left morphism a classical cofibration and the right morphism a fibration, def. \ref{ClassesOfMorhismsInTopQuillen}

$$
  \array{
    &\longrightarrow&
    \\
    {}^{\mathllap{{g \in} \atop {Cof_{cl}}}}\downarrow && \downarrow^{\mathrlap{{f \in }\atop Fib_{cl}}}
    \\
    &\longrightarrow&
  }
$$

admits a [[lift]] as soon as one of the two is also a classical weak equivalence.


=--

+-- {: .proof}
###### Proof

**A)** If the fibration $f$ is also a weak equivalence, then lemma \ref{AcyclicSerreFibrationsAreTheJTopFibrations} says that it has the right lifting property against the generating cofibrations $I_{Top}$, and cor. \ref{SaturationOfGeneratingCofibrations} implies the claim.

**B)** If the cofibration $g$ on the left is also a weak equivalence, consider any factorization into a relative $J_{Top}$-cell complex, def. \ref{TopologicalGeneratingAcyclicCofibrations}, def. \ref{TopologicalCCellComplex}, followed by a fibration,

$$
  g \;\colon\; \stackrel{\in J_{Top} Cell}{\longrightarrow} \stackrel{\in Fib_{cl}}{\longrightarrow}
  \,,
$$

as in the proof of lemma \ref{ContinuousFunctionsFactorAsQuillenAcyclicCofibrationFollowedBySerreFibration}. By lemma \ref{JTopRelativeCellComplexesAreWeakHomotopyEquivalences} the morphism $\overset{\in J_{Top} Cell}{\longrightarrow}$ is a weak homotopy equivalence, and so by [[two-out-of-three]] (prop. \ref{QuillenWeakEquivalencesSatisfyTwoOutOfThree}) the factorizing fibration is actually an acyclic fibration. By case A), this acyclic fibration has the [[right lifting property]] against the cofibration $g$ itself, and so the [[retract argument]], lemma \ref{RetractArgument} gives that $g$  is a [[retract]] of a relative $J_{Top}$-cell complex. With this, finally cor. \ref{SaturationOfGeneratingCofibrations} implies that $f$ has the [[right lifting property]] against $g$.

=--

Finally:

+-- {: .num_prop #LiftingExhausted}
###### Proposition

The systems $(Cof_{cl} , W_{cl} \cap Fib_{cl})$ and $(W_{cl} \cap Cof_{cl}, Fib_{cl})$ from def. \ref{ClassesOfMorhismsInTopQuillen} are [[weak factorization systems]].

=--

+-- {: .proof}
###### Proof

Since we have already seen the factorization property (lemma \ref{FactorizationInTopQuillen}, lemma \ref{ContinuousFunctionsFactorAsQuillenAcyclicCofibrationFollowedBySerreFibration}) and the lifting properties (lemma \ref{LiftingPropertyInTheClassicalModelStructureOnTopologicalSpaces}), it only remains to see that the given left/right classes exhaust the class of morphisms with the given lifting property.

For the classical fibrations this is by definition, for the the classical acyclic fibrations this is by lemma \ref{AcyclicSerreFibrationsAreTheJTopFibrations}.

The remaining statement for $Cof_{cl}$ and $W_{cl}\cap Cof_{cl}$ follows from a general argument ([here](cofibrantly+generated+model+category#RetractsOfCellComplexesExchaustLLPOfRLP)) for [[cofibrantly generated model categories]] (def. \ref{CofibrantlyGeneratedModelCategory}), which we spell out:

So let $f \colon X \longrightarrow Y$ be in $(I_{Top} Inj) Proj$, we need to show that then $f$ is a retract (remark \ref{RetractsOfMorphisms}) of a [[relative cell complex]]. To that end, apply the [[small object]] argument as in lemma \ref{FactorizationInTopQuillen} to factor $f$ as

$$
  f \;\colon \; X \overset{I_{Top} Cell}{\longrightarrow} \hat Y \overset{\in I_{Top} Inj}{\longrightarrow} Y
  \,.
$$

It follows that $f$ has the [[left lifting property]] against $\hat Y \to Y$, and hence by the [[retract argument]] (lemma \ref{RetractArgument}) it is a retract of $X \overset{I Cell}{\to} \hat Y$. This proves the claim for $Cof_{cl}$.

The analogous argument for $W_{cl} \cap Cof_{cl}$,  using the [[small object argument]] for $J_{Top}$, shows that every $f \in (J_{Top} Inj) Proj$ is a retract of a $J_{Top}$-cell complex. By lemma \ref{TopologicalGeneratingAcyclicCofibrationsAreRelativeCellComplexes} and lemma \ref{JTopRelativeCellComplexesAreWeakHomotopyEquivalences} a $J_{Top}$-cell complex is both an $I_{Top}$-cell complex and a weak homotopy equivalence. Retracts of the former are cofibrations by definition, and retracts of the latter are still weak homotopy equivalences by lemma \ref{RetractPreservesIsomorphism}. Hence such $f$ is an acyclic cofibration.

=--


In conclusion, prop. \ref{QuillenWeakEquivalencesSatisfyTwoOutOfThree} and prop. \ref{LiftingExhausted} say that:

+-- {: .num_theorem #TopQuillenModelStructure}
###### Theorem

The classes of morphisms in $Mor(Top)$ of def.  \ref{ClassesOfMorhismsInTopQuillen},

* $W_{cl} = $ [[weak homotopy equivalences]],

* $Fib_{cl} = $ [[Serre fibrations]]

* $Cof_{cl} = $ [[retracts]] of [[relative cell complexes]]

define a [[model category]] structure (def. \ref{ModelCategory}) $Top_{Quillen}$, the **[[classical model structure on topological spaces]]** or **Serre-Quillen model structure** .

=--

In particular

1. every object in $Top_{Quillen}$ is fibrant;

1. the cofibrant objects in $Top_{Quillen}$ are the [[retracts]] of [[cell complexes]].

Hence in particular the following classical statement is an immediate corollary:

+-- {: .num_cor #WhiteheadTheorem}
###### Corollary
**(Whitehead theorem)**

Every [[weak homotopy equivalence]] (def. \ref{WeakHomotopyEquivalenceOfTopologicalSpaces}) between [[topological spaces]] that are [[homeomorphism|homeomorphic]] to a [[retract]] of a [[cell complex]], in particular to a [[CW-complex]] (def. \ref{TopologicalCellComplex}), is a [[homotopy equivalence]] (def. \ref{HomotopyEquivalence}).

=--

+-- {: .proof}
###### Proof

This is the "Whitehead theorem in model categories", lemma \ref{WhiteheadTheoremInModelCategories}, specialized to $Top_{Quillen}$ via theorem \ref{TopQuillenModelStructure}.

=--


In proving theorem \ref{TopQuillenModelStructure} we have in fact shown a bit more that stated. Looking back, all the structure of $Top_{Quillen}$ is entirely induced by the set $I_{Top}$ (def. \ref{TopologicalGeneratingCofibrations}) of generating cofibrations and the set $J_{Top}$ (def. \ref{TopologicalGeneratingAcyclicCofibrations}) of generating acyclic cofibrations (whence the terminology). This phenomenon will keep recurring and will keep being useful as we construct further model categories, such as the [[classical model structure on pointed topological spaces]] (def. \ref{ClassicalModelStructureOnPointedTopologicalSpaces}), the [[projective model structure on enriched functors|projective model structure on topological functors]] (thm. \ref{ProjectiveModelStructureOnTopologicalFunctors}), and finally various [[model structures on spectra]] which we turn to in the [[Introduction to Stable homotopy theory -- 1|section on stable homotopy theory]].

Therefore we make this situation explicit:

+-- {: .num_defn #CofibrantlyGeneratedModelCategory}
###### Definition

A [[model category]] $\mathcal{C}$ (def. \ref{ModelCategory}) is called **cofibrantly generated** if there exists two subsets

$$
  I, J \subset Mor(\mathcal{C})
$$

of its class of morphisms, such that

1. $I$ and $J$ have small domains according to def. \ref{ClassOfMorphismsWithSmallDomains},

1.  the (acyclic) cofibrations of $\mathcal{C}$ are precisely the [[retracts]], of $I$-[[relative cell complexes]] ($J$-relative cell complexes), def. \ref{TopologicalCCellComplex}.

=--

+-- {: .num_prop #CofibrantlyGeneratedModelCategoryLifting}
###### Proposition

For $\mathcal{C}$ a cofibrantly generated model category, def. \ref{CofibrantlyGeneratedModelCategory}, with generating (acylic) cofibrations $I$ ($J$), then its classes $W, Fib, Cof$ of weak equivalences, fibrations and cofibrations are equivalently expressed as [[injective or projective morphisms]] (def. \ref{LiftingAndExtension}) this way:


1. $Cof = (I Inj) Proj$

1. $W \cap Fib = I Inj$;

1. $W \cap Cof = (J Inj) Proj$;

1. $Fib = J Inj$;


=--

+-- {: .proof}
###### Proof

It is clear from the definition that $I \subset (I Inj) Proj$, so that the closure property of prop. \ref{ClosurePropertiesOfInjectiveAndProjectiveMorphisms} gives an inclusion

$$
  Cof \subset (I Inj) Proj
  \,.
$$

For the converse inclusion, let $f \in (I Inj) Proj$. By the [[small object argument]], prop. \ref{SmallObjectArgument}, there is a factorization $f\colon \overset{\in I Cell}{\longrightarrow}\overset{I Inj}{\longrightarrow}$. Hence by assumption and by the [[retract argument]] lemma \ref{RetractArgument}, $f$ is a retract of an $I$-relative cell complex, hence is in $Cof$.

This proves the first statement. Together with the closure properties of prop. \ref{ClosurePropertiesOfInjectiveAndProjectiveMorphisms}, this implies the second claim.

The proof of the third and fourth item is directly analogous, just with $J$ replaced for $I$.

=--



### The classical homotopy category
 {#TheClassicalHomotopyCategory}

With the [[classical model structure on topological spaces]] in hand, we now have good control over the [[classical homotopy category]]:

+-- {: .num_defn #ClassicalHomotopyCategory}
###### Definition

The **Serre-Quillen [[classical homotopy category]]** is the [[homotopy category of a model category|homotopy category]], def. \ref{HomotopyCategoryOfAModelCategory}, of the [[classical model structure on topological spaces]] $Top_{Quillen}$ from theorem \ref{TopQuillenModelStructure}: we write

$$
  Ho(Top) \coloneqq Ho(Top_{Quillen})
  \,.
$$

=--


+-- {: .num_remark #EveryTopologicalSpaceWeaklyEquivalentToACWComplex}
###### Remark

From just theorem \ref{TopQuillenModelStructure}, the definition \ref{HomotopyCategoryOfAModelCategory} (def. \ref{ClassicalHomotopyCategory}) gives that

$$
  Ho(Top_{Quillen}) \simeq (Top_{Retract(Cell)})/_\sim
$$

is the category whose objects are [[retracts]] of [[cell complexes]] (def. \ref{TopologicalCellComplex}) and whose morphisms are [[homotopy classes]] of [[continuous functions]]. But in fact more is true:


Theorem \ref{TopQuillenModelStructure} in itself implies that every topological space is weakly equivalent to a [[retract]] of a [[cell complex]], def. \ref{TopologicalCellComplex}. But by the existence of [[CW approximations]], this cell complex may even be taken to be a [[CW complex]].

(Better yet, there is [[Quillen equivalence]] to the [[classical model structure on simplicial sets]] which implies a _functorial_ [[CW approximation]] ${\vert Sing X\vert} \overset{\in W_{cl}}{\longrightarrow} X$
given by forming the [[geometric realization]] of the [[singular simplicial complex]] of $X$.)


Hence  the Serre-Quillen [[classical homotopy category]] is also equivalently the category of just the [[CW-complexes]] whith [[homotopy classes]] of [[continuous functions]] between them

$$
  \begin{aligned}
    Ho(Top_{Quillen}) & \simeq (Top_{Retract(Cell)})/_\sim
    \\
    & \simeq (Top_{CW})/_{\sim}
  \end{aligned}
  \,.
$$

It follows that the [[universal property]] of the homotopy category (theorem \ref{UniversalPropertyOfHomotopyCategoryOfAModelCategory})

$$
  Ho(Top_{Quillen}) \simeq Top[W_{cl}^{-1}]
$$

implies that there is a bijection, up to [[natural isomorphism]], between

1. functors out of $Top_{CW}$ which agree on homotopy-equivalent maps;

1. functors out of all of $Top$ which send weak homotopy equivalences to isomorphisms.

This statement in particular serves to show that two different axiomatizations of [[generalized (Eilenberg-Steenrod) cohomology]] theories are equivalent to each other. See at _[[Introduction to Stable homotopy theory -- S]]_ the section _[generalized cohomology functors](Introduction+to+Stable+homotopy+theory+--+S#GeneralizedHomologyAndCohomologyFunctors)_ ([this prop.](Introduction+to+Stable+homotopy+theory+--+S#HomotopyTheoreticVersionOfCohomologyFunctorDefIsEquivalent))

**Beware** that, by remark \ref{NotEveryHomotopyEquivalenceIsAWeakHomotopyEquivalence}, what is **not** equivalent to $Ho(Top_{Quillen})$ is the category

$$
  hTop \coloneqq Top/_\sim
$$

obtained from _all_ topological spaces with morphisms the homotopy classes of continuous functions. This category is "too large", the correct homotopy category is just the genuine [[full subcategory]]

$$
  Ho(Top_{Quillen})
   \simeq
  (Top_{Retract(Cell)})/_\sim
   \hookrightarrow
  Top/_\sim
  \simeq hTop
  \,.
$$

Beware also the ambiguity of terminology: "classical homotopy category" some literature refers to $hTop$ instead of $Ho(Top_{Quillen})$. However, here we never have any use for $hTop$ and will not mention it again.

=--


+-- {: .num_prop #TopologicalCylinderOnCWComplexIsGoodCylinderObject}
###### Proposition

Let $X$ be a [[CW-complex]], def. \ref{TopologicalCellComplex}. Then the standard topological cylinder of def. \ref{TopologicalInterval}

$$
  X \sqcup X
   \overset{(i_0,i_1)}{\longrightarrow}
  X\times I
   \longrightarrow
  X
$$

(obtained by forming the [[product space]] with the standard [[topological interval]] $I = [0,1]$) is indeed a _[[cylinder object]]_ in the abstract sense of def. \ref{PathAndCylinderObjectsInAModelCategory}.


=--

+-- {: .proof}
###### Proof

We describe the proof informally. It is immediate how to turn this into a formal proof, but the notation becomes tedious. (One place where it is spelled out completely is [Ottina 14, prop. 2.9](cylinder+object#Ottina14).)

So let $X_0 \to X_1 \to X_2\to \cdots \to X$ be a presentation of $X$ as a CW-complex. Proceed by induction on the cell dimension.

First observe that the cylinder $X_0 \times I$ over $X_0$ is a cell complex: First $X_0$ itself is a disjoint union of points. Adding a second copy for every point (i.e. [[attaching space|attaching]] along $S^{-1}\to D^0$) yields $X_0 \sqcup X_0$, then attaching an inteval between any two corresponding points (along $S^0 \to D^1$) yields $X_0 \times I$.

So assume that for $n \in \mathbb{N}$ it has been shown that $X_n \times I$ has the structure of a CW-complex of dimension $(n+1)$. Then for each cell of $X_{n+1}$, attach it _twice_ to $X_n \times I$, once at $X_n \times \{0\}$, and once at $X_n \times \{1\}$.

The result is $X_{n+1}$ with a _hollow cylinder_ erected over each of its $(n+1)$-cells. Now fill these hollow cylinders (along $S^{n+1} \to D^{n+1}$) to obtain $X_{n+1}\times I$.

This completes the induction, hence the proof of the CW-structure on $X\times I$.

The construction also manifestly exhibits the inclusion $X \sqcup X \overset{(i_0,i_1)}{\longrightarrow}$ as a [[relative cell complex]].

Finally, it is clear (prop. \ref{TopologicalHomotopyEquivalencesAreWeakHomotopyEquivalences}) that $X \times I \to X$ is a weak homotopy equivalence.

=--

Conversely:

+-- {: .num_prop #TopologicalPathSpaceIsGoodPathSpaceObject}
###### Proposition

Let $X$ be any [[topological space]]. Then the standard topological [[path space object]] (def. \ref{TopologicalPathSpace})

$$
  X
    \longrightarrow
  X^I
    \overset{(X^{\delta_0}, X^{\delta_1})}{\longrightarrow}
  X \times X
$$

(obtained by forming the [[mapping space]], def. \ref{CompactOpenTopology}, with the standard [[topological interval]] $I = [0,1]$) is indeed a _[[path space object]]_ in the abstract sense of def. \ref{PathAndCylinderObjectsInAModelCategory}.

=--

+-- {: .proof}
###### Proof

To see that $const \colon X\to X^I$ is a [[weak homotopy equivalence]] it is sufficient, by prop. \ref{TopologicalHomotopyEquivalencesAreWeakHomotopyEquivalences}, to exhibit a [[homotopy equivalence]]. Let the homotopy inverse be $X^{\delta_0} \colon X^I \to X$. Then the composite

$$
  X \overset{const}{\longrightarrow} X^I \overset{X^{\delta_0}}{\longrightarrow} X
$$

is already equal to the identity. The other we round, the rescaling of paths provides the required homotopy

$$
  \array{
    I \times X^I &\overset{(t,\gamma)\mapsto \gamma(t\cdot(-))}{\longrightarrow}&
    X^I
  }
  \,.
$$


To see that $X^I \to X\times X$ is a fibration, we need to show that every commuting square of the form

$$
  \array{
    D^n &\longrightarrow& X^I
    \\
    {}^{\mathllap{i_0}}\downarrow && \downarrow^{}
    \\
    D^n \times I &\longrightarrow& X \times X
  }
$$

has a lift.

Now first use the [[adjunction]] $(I \times (-))\dashv (-)^I$ from prop. \ref{MappingTopologicalSpaceIsExponentialObject} to rewrite this equivalently as the following commuting square:

$$
  \array{
    D^n \sqcup D^n
      &\overset{(i_0, i_0)}{\longrightarrow}&
    (D^n \times I) \sqcup (D^n \times I)
    \\
    {}^{\mathllap{(i_0, i_1)}}\downarrow && \downarrow
    \\
    D^n \times I &\longrightarrow& X
  }
  \,.
$$

This square is equivalently (example \ref{PushoutInTop}) a morphism out of the [[pushout]]

$$
  D^n \times I
    \underset{D^n \sqcup D^n }{\sqcup}
  \left((D^n \times I) \sqcup (D^n \times I)\right)
  \longrightarrow
  X
  \,.
$$

By the same reasoning, a lift in the original diagram is now equivalently a lifting in

$$
  \array{
    D^n \times I
      \underset{D^n \sqcup D^n }{\sqcup}
    \left((D^n \times I) \sqcup (D^n \times I)\right)
      &\longrightarrow&
    X
    \\
      \downarrow && \downarrow
    \\
    (D^n \times I)\times I &\longrightarrow& \ast
  }
  \,.
$$

Inspection of the component maps shows that the left vertical morphism here is the inclusion into the square times $D^n$ of three of its faces times $D^n$. This is homeomorphic to the inclusion $D^{n+1} \to D^{n+1} \times I$ (as in remark \ref{SerreFibrationsByLiftingAgainstMapsHomeomorphicToDiskInclusions}). Therefore a lift in this square exsists, and hence a lift in the original square exists.

=--

### Model structure on pointed spaces
 {#ModelstructureOnPointedTopologicalSpaces}

A _[[pointed object]]_ $(X,x)$ is of course an [[object]] $X$ equipped with a [[point]] $x \colon \ast \to X$, and a morphism of pointed objects $(X,x) \longrightarrow (Y,y)$ is a morphism $X \longrightarrow Y$ that takes $x$ to $y$. Trivial as this is in itself, it is good to record some basic facts, which we do here.

Passing to pointed objects is also the first step in linearizing classical homotopy theory to [[stable homotopy theory]]. In particular, every category of pointed objects has a [[zero object]], hence has [[zero morphisms]]. And crucially, if the original category had [[Cartesian products]], then its pointed objects canonically inherit a non-cartesian [[tensor product]]: the [[smash product]]. These ingredients will be key below in the [[Introduction to Stable homotopy theory -- 1|section on stable homotopy theory]].

+-- {: .num_defn #SliceCategory}
###### Definition

Let $\mathcal{C}$ be a [[category]] and let $X \in \mathcal{C}$ be an [[object]].

The _[[slice category]]_ $\mathcal{C}_{/X}$ is the category whose

* objects are morphisms $\array{A \\ \downarrow \\ X}$ in $\mathcal{C}$;

* morphisms are [[commuting diagram|commuting triangles]] $\array{ A && \longrightarrow && B \\ & {}_{}\searrow && \swarrow \\ && X}$ in $\mathcal{C}$.

Dually, the _[[coslice category]]_ $\mathcal{C}^{X/}$ is the category whose

* objects are morphisms $\array{X \\ \downarrow \\ A}$ in $\mathcal{C}$;

* morphisms are [[commuting diagram|commuting triangles]] $\array{ && X \\ & \swarrow && \searrow \\ A && \longrightarrow && B }$ in $\mathcal{C}$.

There are the canonical [[forgetful functors]]

$$
  U \;\colon \; \mathcal{C}_{/X}, \mathcal{C}^{X/} \longrightarrow \mathcal{C}
$$

given by forgetting the morphisms to/from $X$.

=--

We here focus on this class of examples:

+-- {: .num_defn #CategoryOfPointedObjects}
###### Definition

For $\mathcal{C}$ a [[category]] with [[terminal object]] $\ast$, the [[coslice category]] (def. \ref{SliceCategory}) $\mathcal{C}^{\ast/}$ is the corresponding _[[category of pointed objects]]_: its

* objects are morphisms in $\mathcal{C}$ of the form $\ast \overset{x}{\to} X$ (hence an object $X$ equipped with a choice of point; i.e. a _[[pointed object]]_);

* morphisms are [[commuting diagram|commuting triangles]] of the form

  $$
    \array{
       && \ast
       \\
       & {}^{\mathllap{x}}\swarrow && \searrow^{\mathrlap{y}}
       \\
       X && \overset{f}{\longrightarrow} && Y
    }
  $$

  (hence morphisms in $\mathcal{C}$ which preserve the chosen points).

=--

+-- {: .num_remark #PointedObjectsHaveZeroObject}
###### Remark

In a [[category of pointed objects]] $\mathcal{C}^{\ast/}$, def. \ref{CategoryOfPointedObjects}, the [[terminal object]] coincides with the [[initial object]], both are given by $\ast \in \mathcal{C}$ itself, pointed in the unique way.

In this situation one says that $\ast$ is a _[[zero object]]_ and that $\mathcal{C}^{\ast/}$ is a _[[pointed category]]_.

It follows that also all [[hom-sets]] $Hom_{\mathcal{C}^{\ast/}}(X,Y)$ of $\mathcal{C}^{\ast/}$ are canonically [[pointed sets]], pointed by the _[[zero morphism]]_

$$
  0
    \;\colon\;
  X
    \overset{\exists !}{\longrightarrow}
  0
    \overset{\exists !}{\longrightarrow} Y
  \,.
$$

=--



+-- {: .num_defn #BasePointAdjoined}
###### Definition

Let $\mathcal{C}$ be a [[category]] with [[terminal object]] and [[finite colimits]]. Then the [[forgetful functor]] $U \colon \mathcal{C}^{\ast/} \to \mathcal{C}$ from its [[category of pointed objects]], def. \ref{CategoryOfPointedObjects}, has a [[left adjoint]]

$$
  \mathcal{C}^{\ast/}
     \underoverset
       {\underset{U}{\longrightarrow}}
       {\overset{(-)_+}{\longleftarrow}}
       {\bot}
  \mathcal{C}
$$

given by forming the [[disjoint union]] ([[coproduct]]) with a base point ("adjoining a base point").

=--

+-- {: .num_prop #LimitsAndColimitsOfPointedObjects}
###### Proposition

Let $\mathcal{C}$ be a [[category]] with all [[limits]] and [[colimits]]. Then also the [[category of pointed objects]] $\mathcal{C}^{\ast/}$, def. \ref{CategoryOfPointedObjects}, has all limits and colimits.

Moreover:

1. the limits are the limits of the underlying diagrams in $\mathcal{C}$, with the base point of the limit induced by its universal property in $\mathcal{C}$;

1. the colimits are the limits in $\mathcal{C}$ of the diagrams _with the basepoint adjoined_.

=--

+-- {: .proof}
###### Proof

It is immediate to check the relevant [[universal property]]. For details see at _[slice category -- limits and colimits](overcategory#LimitsAndColimits)_.

=--

+-- {: .num_example #WedgeSumAsCoproduct}
###### Example

Given two pointed objects $(X,x)$ and $(Y,y)$, then:

1. their [[product]] in $\mathcal{C}^{\ast/}$ is simply $(X\times Y, (x,y))$;

1. their [[coproduct]] in $\mathcal{C}^{\ast/}$ has to be computed using the second clause in prop. \ref{LimitsAndColimitsOfPointedObjects}: since the point $\ast$ has to be adjoined to the diagram, it is given not by the coproduct in $\mathcal{C}$, but by the [[pushout]] in $\mathcal{C}$ of the form:

   $$
     \array{
       \ast &\overset{x}{\longrightarrow}& X
       \\
       {}^{\mathllap{y}}\downarrow &(po)& \downarrow
       \\
       Y &\longrightarrow& X \vee Y
     }
     \,.
   $$

   This is called the _[[wedge sum]]_ operation on pointed objects.

Generally for a set $\{X_i\}_{i \in I}$ in $Top^{\ast/}$

1. their [[product]] is formed in $Top$ as in example \ref{ProductTopologicalSpace}, with the new basepoint canonically induced;

1. their [[coproduct]] is formed by the [[colimit]] in $Top$ over the diagram with a basepoint adjoined, and is called the [[wedge sum]] $\vee_{i \in I} X_i$.

=--

+-- {: .num_example}
###### Example

For $X$ a [[CW-complex]], def. \ref{TopologicalCellComplex} then for every $n \in \mathbb{N}$ the [[quotient]] (example \ref{QuotientSpaceAsPushout}) of its $n$-skeleton by its $(n-1)$-skeleton is the [[wedge sum]], def. \ref{WedgeSumAsCoproduct}, of $n$-spheres, one for each $n$-cell of $X$:

$$
  X^n / X^{n-1} \simeq \underset{i \in I_n}{\vee} S^n
  \,.
$$

=--


+-- {: .num_defn #SmashProductOfPointedObjects}
###### Definition

For $\mathcal{C}^{\ast/}$ a [[category of pointed objects]] with [[finite limits]] and [[finite colimits]], the _[[smash product]]_ is the [[functor]]

$$
  (-)\wedge(-)
  \;\colon\;
  \mathcal{C}^{\ast/}
  \times
  \mathcal{C}^{\ast/}
  \longrightarrow
  \mathcal{C}^{\ast/}
$$

given by

$$
  X \wedge Y
  \;\coloneqq\;
  \ast
  \underset{X\sqcup Y}{\sqcup} (X \times Y)
  \,,
$$

hence by the [[pushout]] in $\mathcal{C}$

$$
  \array{
    X \sqcup Y &\overset{(id_X,y),(x,id_Y) }{\longrightarrow}& X \times Y
    \\
    \downarrow && \downarrow
    \\
    \ast &\longrightarrow& X \wedge Y
  }
  \,.
$$

In terms of the [[wedge sum]] from def. \ref{WedgeSumAsCoproduct}, this may be written concisely as

$$
  X \wedge Y = \frac{X\times Y}{X \vee Y}
  \,.
$$

=--

+-- {: .num_remark #SmashProductOnTopNotAssociative}
###### Remark

For a general category $\mathcal{C}$ in def. \ref{SmashProductOfPointedObjects}, the [[smash product]] need not be [[associativity|associative]], namely it fails to be associative if the functor $(-)\times Z$ does not preserve the [[quotients]] involved in the definition.

In particular this may happen for $\mathcal{C} = $ [[Top]].

A sufficient condition for $(-) \times Z$ to preserve quotients is that it is a [[left adjoint]] functor. This is the case in the smaller subcategory of [[compactly generated topological spaces]], we come to this in prop. \ref{SmashProductInTopcgIsAssociative} below.



=--

These two operations are going to be ubiquituous in [[stable homotopy theory]]:

| symbol | name | category theory |
|--------|------|-----------------|
| $X \vee Y$ | [[wedge sum]] | [[coproduct]] in $\mathcal{C}^{\ast/}$ |
| $X \wedge Y$ | [[smash product]] | [[tensor product]] in $\mathcal{C}^{\ast/}$|


+-- {: .num_example #WedgeAndSmashOfBasePointAdjoinedTopologicalSpaces}
###### Example

For $X, Y \in Top$, with $X_+,Y_+ \in Top^{\ast/}$, def. \ref{BasePointAdjoined}, then

* $X_+ \vee Y_+ \simeq (X \sqcup Y)_+$;

* $X_+ \wedge Y_+ \simeq (X \times Y)_+$.

=--

+-- {: .proof}
###### Proof

By example \ref{WedgeSumAsCoproduct}, $X_+ \vee Y_+$ is given by the colimit in $Top$ over the diagram

$$
  \array{
    && && \ast
    \\
    && & \swarrow && \searrow
    \\
    X &\,\,& \ast && && \ast &\,\,& Y
  }
  \,.
$$

This is clearly $X \sqcup \ast \sqcup Y$. Then, by definition \ref{SmashProductOfPointedObjects}

$$
  \begin{aligned}
    X_+ \wedge Y_+
    & \simeq
    \frac{(X \sqcup \ast) \times (X \sqcup \ast)}{(X\sqcup \ast) \vee (Y \sqcup \ast)}
    \\
    & \simeq
    \frac{X \times Y \sqcup X \sqcup Y \sqcup \ast}{X \sqcup Y \sqcup \ast}
    \\
    & \simeq
    X \times Y \sqcup \ast
    \,.
  \end{aligned}
$$

=--

+-- {: .num_example #StandardReducedCyclinderInTop}
###### Example

Let $\mathcal{C}^{\ast/} = Top^{\ast/}$ be [[pointed topological spaces]]. Then

$$
  I_+ \in Top^{\ast/}
$$

denotes the standard interval object $I = [0,1]$ from def. \ref{TopologicalInterval}, with a djoint basepoint adjoined, def. \ref{BasePointAdjoined}. Now for $X$ any [[pointed topological space]], then

$$
  X \wedge (I_+) = (X \times I)/(\{x_0\} \times I)
$$

is the **[[reduced cylinder]]** over $X$: the result of forming the ordinary cyclinder over $X$ as in def. \ref{TopologicalInterval}, and then identifying the interval over the basepoint of $X$ with the point.

(Generally, any construction in $\mathcal{C}$ properly adapted to pointed objects $\mathcal{C}^{\ast/}$ is called the "reduced" version of the unpointed construction. Notably so for "[[reduced suspension]]" which we come to [below](#MappingCones).)


Just like the ordinary cylinder $X\times I$ receives a canonical injection from the [[coproduct]] $X \sqcup X$ formed in $Top$, so the reduced cyclinder receives a canonical injection from the coproduct $X \sqcup X$ formed in $Top^{\ast/}$, which is the [[wedge sum]] from example \ref{WedgeSumAsCoproduct}:

$$
  X \vee X \longrightarrow X \wedge (I_+)
  \,.
$$

=--

+-- {: .num_example #PointedMappingSpace}
###### Example

For $(X,x),(Y,y)$ [[pointed topological spaces]] with $Y$ a [[locally compact topological space]], then the **[[pointed mapping space]]** is the [[topological subspace]] of the [[mapping space]] of def. \ref{CompactOpenTopology}

$$
  Maps((Y,y),(X,x))_\ast
    \hookrightarrow
  (X^Y, const_x)
$$

on those maps which preserve the basepoints, and pointed by the map constant on the basepoint of $X$.

In particular, the **standard topological pointed path space object** on some pointed $X$ (the pointed variant of def. \ref{TopologicalPathSpace}) is the pointed mapping space $Maps(I_+,X)_\ast$.

The pointed consequence of prop. \ref{MappingTopologicalSpaceIsExponentialObject} then gives that there is a [[natural bijection]]

$$
  Hom_{Top^{\ast/}}((Z,z) \wedge (Y,y), (X,x))
  \simeq
  Hom_{Top^{\ast/}}((Z,z), Maps((Y,y),(X,x))_\ast)
$$

between basepoint-preserving continuous functions out of a [[smash product]], def. \ref{SmashProductOfPointedObjects}, with pointed continuous functions of one variable into the pointed mapping space.

=--

+-- {: .num_example #FiberAndCofiberInPointedObjects}
###### Example

Given a morphism $f \colon X \longrightarrow Y$ in a [[category of pointed objects]] $\mathcal{C}^{\ast/}$, def. \ref{CategoryOfPointedObjects}, with finite limits and colimits,

1. its _[[fiber]]_ or _[[kernel]]_ is the [[pullback]] of the point inclusion

   $$
     \array{
       fib(f) &\longrightarrow& X
       \\
       \downarrow &(pb)& \downarrow^{\mathrlap{f}}
       \\
       \ast &\longrightarrow& Y
     }
   $$

1. its _[[cofiber]]_ or _[[cokernel]]_ is the [[pushout]] of the point projection

   $$
     \array{
       X &\overset{f}{\longrightarrow}& Y
       \\
       \downarrow &(po)& \downarrow
       \\
       \ast &\longrightarrow& cofib(f)
     }
     \,.
   $$

=--

+-- {: .num_remark }
###### Remark

In the situation of example \ref{FiberAndCofiberInPointedObjects}, both the pullback as well as the pushout are equivalently computed in $\mathcal{C}$. For the pullback this is the first clause of prop. \ref{LimitsAndColimitsOfPointedObjects}. The second clause says that for computing the pushout in $\mathcal{C}$, first the point is to be adjoined to the diagram, and then the colimit over the larger diagram

$$
  \array{
    \ast
    \\
    & \searrow
    \\
    & & X &\overset{f}{\longrightarrow}& Y
    \\
    & & \downarrow &&
    \\
    & & \ast &&
   }
$$

be computed. But one readily checks that in this special case this does not affect the result. (The technical jargon is that the inclusion of the smaller diagram into the larger one in this case happens to be a [[final functor]].)

=--

+-- {: .num_prop #ModelStructureOnSliceCategory}
###### Proposition

Let $\mathcal{C}$ be a [[model category]] and let $X \in \mathcal{C}$ be an [[object]]. Then both the [[slice category]] $\mathcal{C}_{/X}$ as well as the [[coslice category]] $\mathcal{C}^{X/}$, def. \ref{SliceCategory}, carry model structures themselves -- the **[[model structure on a slice category|model structure on a (co-)slice category]]**,  where a morphism is a weak equivalence, fibration or cofibration iff its image under the [[forgetful functor]] $U$ is so in $\mathcal{C}$.

In particular the category $\mathcal{C}^{\ast/}$ of [[pointed objects]], def. \ref{CategoryOfPointedObjects}, in a model category $\mathcal{C}$ becomes itself a model category this way.

The corresponding [[homotopy category of a model category]], def. \ref{HomotopyCategoryOfAModelCategory}, we call the **[[pointed category|pointed]] [[homotopy category of a model category|homotopy category]]** $Ho(\mathcal{C}^{\ast/})$.

=--

+-- {: .proof}
###### Proof

This is immediate:

By prop. \ref{LimitsAndColimitsOfPointedObjects} the (co-)slice category has all limits and colimits. By definition of the weak equivalences in the (co-)slice, they satisfy [[two-out-of-three]], def. \ref{CategoryWithWeakEquivalences}, because the do in $\mathcal{C}$.

Similarly, the factorization and lifting is all induced by $\mathcal{C}$: Consider the coslice category $\mathcal{C}^{X/}$, the case of the slice category is formally dual; then if

$$
  \array{
    && X
    \\
    & \swarrow && \searrow
    \\
    A && \underset{f}{\longrightarrow} && B
  }
$$

commutes in $\mathcal{C}$, and a factorization of $f$ exists in $\mathcal{C}$, it uniquely makes this diagram commute

$$
  \array{
    && X
    \\
    & \swarrow &\downarrow& \searrow
    \\
    A &\longrightarrow& C & \longrightarrow& B
  }
  \,.
$$

Similarly, if

$$
  \array{
    A &\longrightarrow& C
    \\
    \downarrow && \downarrow
    \\
    B &\longrightarrow& D
  }
$$

is a [[commuting diagram]] in $\mathcal{C}^{X/}$, hence a commuting diagram in $\mathcal{C}$ as shown, with all objects equipped with compatible morphisms from $X$, then inspection shows that any lift in the diagram necessarily respects the maps from $X$, too.

=--

+-- {: .num_example #HomotopyCategoryOfPointedModelStructureIsEnrichedInPointedSets}
###### Example

For $\mathcal{C}$ any [[model category]], with $\mathcal{C}^{\ast/}$ its [[slice model structure|pointed model structure]] according to prop. \ref{ModelStructureOnSliceCategory}, then the corresponding [[homotopy category of a model category|homotopy category]] (def. \ref{HomotopyCategoryOfAModelCategory}) is, by remark \ref{PointedObjectsHaveZeroObject}, canonically [[enriched category|enriched]] in [[pointed sets]], in that its [[hom-functor]] is of the form

$$
  [-,-]_\ast
    \;\colon\;
  Ho(\mathcal{C}^{\ast/})^\op
    \times
  Ho(\mathcal{C}^{\ast/})
    \longrightarrow
  Set^{\ast/}
  \,.
$$

=--



+-- {: .num_defn #ClassicalModelStructureOnPointedTopologicalSpaces}
###### Definition

Write $Top^{\ast/}_{Quillen}$ for the **[[classical model structure on pointed topological spaces]]**, obtained from the [[classical model structure on topological spaces]] $Top_{Quillen}$ (theorem \ref{TopQuillenModelStructure}) via the induced [[coslice model structure]] of prop. \ref{ModelStructureOnSliceCategory}.

Its [[homotopy category of a model category|homotopy category]], def. \ref{HomotopyCategoryOfAModelCategory},

$$
  Ho(Top^{\ast/})
    \coloneqq
  Ho(Top_{Quillen}^{\ast/})
$$

we call the **[[classical pointed homotopy category]]**.

=--


+-- {: .num_remark #NonDegenerateBasepointAsCofibrantObjects}
###### Remark

The fibrant objects in the pointed model structure $\mathcal{C}^{\ast/}$, prop. \ref{ModelStructureOnSliceCategory}, are those that are fibrant as objects of $\mathcal{C}$. But the cofibrant objects in $\mathcal{C}^{\ast/}$ are now those for which the basepoint inclusion is a cofibration in $X$.

For $\mathcal{C}^{\ast/} = Top^{\ast/}_{Quillen}$ from def. \ref{ClassicalModelStructureOnPointedTopologicalSpaces}, then the corresponding cofibrant pointed topological spaces are tyically referred to as spaces **with non-degenerate basepoints** or . Notice that the point itself is cofibrant in $Top_{Quillen}$, so that cofibrant pointed topological spaces are in particular cofibrant topological spaces.

=--

While the existence of the model structure on $Top^{\ast/}$ is immediate, via prop. \ref{ModelStructureOnSliceCategory}, for the discussion of [[topologically enriched functors]] ([below](#ModelStructureOnTopEnrichedFunctors)) it is useful to record that this, too, is a [[cofibrantly generated model category]] (def. \ref{CofibrantlyGeneratedModelCategory}), as follows:

+-- {: .num_defn #GeneratingCofibrationsForPointedTopologicalSpaces}
###### Definition

Write

$$
  I_{Top^{\ast/}}
  =
 \left\{
    S^{n-1}_+ \overset{(\iota_n)_+}{\longrightarrow} D^n_+
 \right\}
  \;\;
  \subset Mor(Top^{\ast/})
$$

and

$$
  J_{Top^{\ast/}}
  =
 \left\{
    D^n_+ \overset{(id, \delta_0)_+}{\longrightarrow} (D^n \times I)_+
 \right\}
  \;\;\;
  \subset Mor(Top^{\ast/})
 \,,
$$

respectively, for the sets of morphisms obtained from the classical generating cofibrations, def. \ref{TopologicalGeneratingCofibrations}, and the classical generating acyclic cofibrations, def. \ref{TopologicalGeneratingAcyclicCofibrations}, under adjoining of basepoints (def. \ref{BasePointAdjoined}).

=--

+-- {: .num_theorem #CofibrantGenerationOfPointedTopologicalSpaces}
###### Theorem

The sets $I_{Top^{\ast/}}$ and $J_{Top^{\ast/}}$ in def. \ref{GeneratingCofibrationsForPointedTopologicalSpaces} exhibit the [[classical model structure on pointed topological spaces]] $Top^{\ast/}_{Quillen}$ of def. \ref{ClassicalModelStructureOnPointedTopologicalSpaces} as a [[cofibrantly generated model category]], def. \ref{CofibrantlyGeneratedModelCategory}.

=--

(This is also a special case of a general statement about cofibrant generation of [[coslice model structures]], see [this proposition](model+structure+on+an+over+category#ModelStructureInheritsGoodProperties).)

+-- {: .proof}
###### Proof

Due to the fact that in $J_{Top^{\ast/}}$ a basepoint is freely adjoined, lemma \ref{AcyclicSerreFibrationsAreTheJTopFibrations} goes through verbatim for the pointed case, with $J_{Top}$ replaced by $J_{Top^{\ast/}}$, as do the other two lemmas above that depend on [[point-set topology]], lemma \ref{CompactSubsetsAreSmallInCellComplexes} and lemma \ref{JTopRelativeCellComplexesAreWeakHomotopyEquivalences}. With this, the rest of the proof follows by the same general abstract reasoning as [above](#TheClassicalModelStructureOfTopologicalSpaces) in the proof of theorem \ref{TopQuillenModelStructure}.

=--


### Model structure on compactly generated spaces
 {#ModelStructureOnCompactlyGeneratedTopologicalSpaces}

The category [[Top]] has the technical inconvenience that [[mapping spaces]] $X^Y$ (def. \ref{CompactOpenTopology}) satisfying the exponential property (prop. \ref{MappingTopologicalSpaceIsExponentialObject}) exist in general only for $Y$ a [[locally compact topological space]], but fail to exist more generally. In other words: [[Top]] is not [[cartesian closed category|cartesian closed]]. But cartesian closure is necessary for some purposes of homotopy theory, for instance it ensures that

1. the [[smash product]] (def. \ref{SmashProductOfPointedObjects}) on [[pointed topological spaces]] is [[associative]] (prop. \ref{SmashProductInTopcgIsAssociative} below);

1. there is a concept of [[topologically enriched functors]] with values in topological spaces, to which we turn [below](#ModelStructureOnTopEnrichedFunctors);

1. [[geometric realization]] of [[simplicial sets]] preserves [[products]].

The first two of these are crucial for the development of [[stable homotopy theory]] in the [[Introduction to Stable homotopy theory -- 1|next section]], the third is a great convenience in computations.

Now, since the [[homotopy theory]] of topological spaces only cares about the [[CW approximation]] to any topological space (remark \ref{EveryTopologicalSpaceWeaklyEquivalentToACWComplex}), it is plausible to ask for a [[full subcategory]] of [[Top]] which still contains all [[CW-complexes]], still has all [[limits]] and [[colimits]], still supports a model category structure constructed in the same way as above, but which in addition is [[cartesian closed category|cartesian closed]], and preferably such that the model structure interacts well with the cartesian closure.

Such a full subcategory exists, the category of [[compactly generated topological spaces]]. This we briefly describe now.

**Literature** ([Strickland 09](#Strickland09))

$\,$

+-- {: .num_defn #kTop}
###### Definition

Let $X$ be a [[topological space]].

A subset $A \subset X$ is called **compactly closed** (or **$k$-closed**) if for every [[continuous function]] $f \colon K \longrightarrow X$ out of a [[compact topological space|compact]] [[Hausdorff topological space|Hausdorff space]] $K$, then the [[preimage]] $f^{-1}(A)$ is a [[closed subset]] of $K$.

The space $X$ is called **[[compactly generated topological space|compactly generated]]** if its closed subsets exhaust (hence coincide with) the $k$-closed subsets.

Write

$$
  Top_{cg} \hookrightarrow Top
$$

for the [[full subcategory]] of [[Top]] on the compactly generated topological spaces.

=--

+-- {: .num_defn #kfication}
###### Definition

Write

$$
  Top \overset{k}{\longrightarrow} Top_{cg} \hookrightarrow Top
$$

for the [[functor]] which sends any [[topological space]] $X = (S,\tau)$ to the  topological space $(S, k \tau)$ with the same underlying set $S$, but with open subsets $k \tau$ the collection of all $k$-open subsets with respect to $\tau$.

=--


+-- {: .num_lemma #ContinuousFunctionsOutOfCompactlyGeneratedFactorThroughCompactlyGeneratedClosureOfCodomain}
###### Lemma

Let $X \in Top_{cg} \hookrightarrow Top$ and let $Y\in Top$. Then [[continuous functions]]

$$
  X \longrightarrow Y
$$

are also continuous when regarded as functions

$$
  X \longrightarrow k(Y)
$$

with $k$ from def. \ref{kfication}.

=--

+-- {: .proof}
###### Proof

We need to show that for $A \subset X$ a $k$-closed subset, then the [[preimage]] $f^{-1}(A) \subset X$ is closed subset.

Let $\phi \colon K \longrightarrow X$ be any continuous function out of a compact Hausdorff space $K$. Since $A$ is $k$-closed by assumption, we have that $(f \circ \phi)^{-1}(A) = \phi^{-1}(f^{-1}(A))\subset K$ is closed in $K$. This means that $f^{-1}(A)$ is $k$-closed in $X$. But by the assumption that $X$ is compactly generated, it follows that $f^{-1}(A)$ is already closed.

=--

+-- {: .num_cor #kTopIsCoreflectiveSubcategory}
###### Corollary

For $X \in Top_{cg}$ there is a [[natural bijection]]

$$
  Hom_{Top}(X,Y) \simeq Hom_{Top_{cg}}(X, k(Y))
  \,.
$$

This means equivalently that the functor $k$ (def. \ref{kfication}) together with the inclusion from def. \ref{kTop} forms an pair of [[adjoint functors]]

$$
  Top_{cg}
    \underoverset
      {\underset{k}{\longleftarrow}}
      {\hookrightarrow}
      {\bot}
  Top
  \,.
$$

This in turn means equivalently that $Top_{cg} \hookrightarrow Top$ is a [[coreflective subcategory]] with coreflector $k$. In particular $k$ is [[idempotent monad|idemotent]] in that there are [[natural isomorphisms|natural]] [[homeomorphisms]]

$$
  k(k(X))\simeq k(X)
  \,.
$$

Hence [[colimits]] in $Top_{cg}$ exist and are computed as in [[Top]]. Also [[limits]] in $Top_{cg}$ exist, these are obtained by computing the limit in [[Top]] and then applying the functor $k$ to the result.

=--

The following is a slight variant of def. \ref{CompactOpenTopology}, appropriate for the context of $Top_{cg}$.

+-- {: .num_defn #CompactlyGeneratedMappingSpaces}
###### Definition

For $X, Y \in Top_{cg}$ (def. \ref{kTop}) the **compactly generated mapping space** $X^Y \in Top_{cg}$ is the [[compactly generated topological space]] whose underlying set is the set $C(Y,X)$ of [[continuous functions]] $f \colon Y \to X$, and for which a [[topological base|subbase]] for its topology has elements $U^{\phi(K)}$, for $U \subset X$ any [[open subset]] and $\phi \colon K \to Y$ a [[continuous function]] out of a [[compact topological space|compact]] [[Hausdorff space]] $K$ given by

$$
  U^{\phi(\kappa)} \coloneqq \left\{ f\in C(Y,X) | f(\phi(K)) \subset U \right\}
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

If $Y$ is (compactly generated and) a [[Hausdorff space]], then the topology on the compactly generated mapping space $X^Y$ in def. \ref{CompactlyGeneratedMappingSpaces} agrees with the [[compact-open topology]] of def. \ref{CompactOpenTopology}. Beware that it is common to say "compact-open topology" also for the topology of the compactly generated mapping space when $Y$ is not Hausdorff. In that case, however, the two definitions in general disagree.

=--



+-- {: .num_prop #CartesianClosureOfTopcg}
###### Proposition

The category $Top_{cg}$ of def. \ref{kTop} is [[cartesian closed category|cartesian closed]]:

for every $X \in Top_{cg}$ then the operation $X\times (-)$ of forming the [[Cartesian product]] in $Top_{cg}$ (which by cor. \ref{kTopIsCoreflectiveSubcategory} is $k$ applied to the usual [[product topological space]]) together with the operation $(-)^X$ of forming the compactly generated [[mapping space]] (def. \ref{CompactlyGeneratedMappingSpaces}) forms a pair of [[adjoint functors]]

$$
  Top_{cg}
    \underoverset
      {\underset{(-)^X}{\longrightarrow}}
      {\overset{X \times (-)}{\longleftarrow}}
      {\bot}
  Top_{cg}
  \,.
$$


=--

For proof see for instance ([Strickland 09, prop. 2.12](#Strickland09)).


+-- {: .num_cor #SmashHomAdjunctionOnPointedCompactlyGeneratedTopologicalSpaces}
###### Corollary

For $X, Y \in Top_{cg}^{\ast/}$, the operation of forming the [[pointed mapping space]] (example \ref{PointedMappingSpace}) inside the compactly generated mapping space of def. \ref{CompactlyGeneratedMappingSpaces}

$$
  Maps(Y,X)_\ast
  \coloneqq
  fib\left(
    X^Y \overset{ev_y}{\longrightarrow} X
    \;,
    x
  \right)
$$

is [[left adjoint]] to the [[smash product]] operation on [[pointed topological space|pointed]] [[compactly generated topological spaces]].

$$
  Top_{cg}^{\ast/}
    \underoverset
      {\underset{Maps(Y,-)_\ast}{\longrightarrow}}
      {\overset{Y \wedge (-)}{\longleftarrow}}
      {\bot}
  Top_{cg}^{\ast/}
 \,.
$$

=--

+-- {: .num_cor #MappingSpacesSendsColimitsInFirstArgumentToLimits}
###### Corollary

For $I$ a [[small category]] and $X_\bullet \colon I \to Top^{\ast/}_{cg}$ a [[diagram]], then the compactly generated [[mapping space]] construction from def. \ref{CompactlyGeneratedMappingSpaces} preserves [[limits]] in its covariant argument and sends colimits in its contravariant argument to limits:

$$
  Maps(X,\underset{\longleftarrow}{\lim}_i Y_i)_\ast
  \;\simeq\;
  \underset{\longleftarrow}{\lim}_i Maps(X, Y_i)_\ast
$$

and

$$
  Maps( \underset{\longrightarrow}{\lim}_i X_i, \; Y )_\ast
  \simeq
  \underset{\longleftarrow}{\lim}_i
  Maps( X_i, Y )_\ast
  \,.
$$

=--

+-- {: .proof}
###### Proof

The first statement is an immediate implication of $Maps(X,-)_\ast$ being a [[right adjoint]], according to cor. \ref{SmashHomAdjunctionOnPointedCompactlyGeneratedTopologicalSpaces}.

For the second statement, we use that by def. \ref{kTop} a [[compactly generated topological space]] is uniquely determined if one knows all continuous functions out of compact Hausdorff spaces into it. Hence it is sufficient to show that there is a [[natural isomorphism]]

$$
  Hom_{Top_{cg}^{\ast/}}\left( K,\;
    Maps( \underset{\longrightarrow}{\lim}_i X_i, \; Y )_\ast
  \right)
  \simeq
  Hom_{Top^{\ast/}_{cg}}\left( K, \;
    \underset{\longleftarrow}{\lim}_i
    Maps( X_i, Y )_\ast
  \right)
$$

for $K$ any compact Hausdorff space.

With this, the statement follows by cor. \ref{SmashHomAdjunctionOnPointedCompactlyGeneratedTopologicalSpaces} and using that ordinary [[hom-sets]] take colimits in the first argument and limits in the second argument to limits:

$$
  \begin{aligned}
    Hom_{Top^{\ast/}_{cg}}
    \left(
      K, \; Maps(\underset{\longrightarrow}{\lim}_i X_i,\; Y)_\ast
    \right)
    & \simeq
    Hom_{Top^{\ast/}_{cg}}
    \left(
      K \wedge \underset{\longrightarrow}{\lim}_i X_i,\; Y
    \right)
    \\
    & \simeq
    Hom_{Top^{\ast/}_{cg}}
    \left(
      \underset{\longrightarrow}{\lim}_i
      (K \wedge X_i)
      ,\; Y
    \right)
    \\
    & \simeq
    \underset{\longleftarrow}{\lim}_i
    \left(
      Hom_{Top^{\ast/}_{cg}}
      ( K \wedge X_i, \; Y )
    \right)
    \\
    & \simeq
    \underset{\longleftarrow}{\lim}_i
    Hom_{Top^{\ast/}_{cg}}( K, \; Maps(X_i,Y)_\ast )
    \\
    & \simeq
    Hom_{Top^{\ast/}_{cg}}
    \left(
      K,\;
      \underset{\longleftarrow}{\lim}_i Maps(X_i,Y)_\ast
    \right)
  \end{aligned}
  \,.
$$


=--


Moreover, compact generation fixes the associativity of the smash product (remark \ref{SmashProductOnTopNotAssociative}):

+-- {: .num_prop #SmashProductInTopcgIsAssociative}
###### Proposition

On [[pointed topological space|pointed]] (def. \ref{CategoryOfPointedObjects}) [[compactly generated topological spaces]] (def. \ref{kTop}) the [[smash product]] (def. \ref{SmashProductOfPointedObjects})

$$
  (-)\wedge (-)
  \;\colon\;
  Top_{cg}^{\ast/}
    \times
  Top_{cg}^{\ast/}
    \longrightarrow
  Top_{cg}^{\ast/}
$$

is [[associativity|associative]] and the [[0-sphere]] is a [[tensor unit]] for it.

=--

+-- {: .proof}
###### Proof

Since $(-)\times X$ is a [[left adjoint]] by prop. \ref{CartesianClosureOfTopcg}, it presevers [[colimits]] and in particular [[quotient space]] projections. Therefore with $X, Y, Z \in Top_{cg}^{\ast/}$ then

$$
  \begin{aligned}
    (X \wedge Y) \wedge Z
    & =
    \frac{
      \frac{X\times Y}{X \times\{y\} \sqcup \{x\}\times Y}
      \times Z
    }{ (X \wedge Y)\times \{z\} \sqcup \{[x] = [y]\} \times Z}
    \\
    & \simeq
    \frac{\frac{X \times Y \times Z}{X \times \{y\}\times Z \sqcup \{x\}\times Y \times Z}}{
      X \times Y \times \{z\}
    }
   \\
   &\simeq
    \frac{X\times Y \times Z}{X \times \{y\}\times Z \sqcup \{x\}\times Y \times Z \sqcup X \times Y \times \{z\}}
  \end{aligned}
  \,.
$$

The analogous reasoning applies to yield also $X \wedge (Y\wedge Z) \simeq \frac{X\times Y \times Z}{X \times \{y\}\times Z \sqcup \{x\}\times Y \times Z \sqcup X \times Y \times \{z\}}$.

The second statement follows directly with prop. \ref{CartesianClosureOfTopcg}.

=--

+-- {: .num_remark #PointedCompactlyGeneratedTopologicalSpacesIsSymmetricMonoidalClosed}
###### Remark

Corollary \ref{SmashHomAdjunctionOnPointedCompactlyGeneratedTopologicalSpaces} together with prop. \ref{SmashProductInTopcgIsAssociative} says that under the [[smash product]] the category of [[pointed topological spaces|pointed]] [[compactly generated topological spaces]] is a [[closed monoidal category|closed]] [[symmetric monoidal category]] with [[tensor unit]] the [[0-sphere]].

$$
  (Top_{cg}^{\ast/}, \wedge, S^0)
  ,.
$$

Notice that by prop. \ref{CartesianClosureOfTopcg} also unpointed compactly generated spaces under [[Cartesian product]] form a [[closed monoidal category|closed]] [[symmetric monoidal category]], hence a [[cartesian closed category]]

$$
  (Top_{cg}, \times , \ast)
  \,.
$$

The fact that $Top_{cg}^{\ast/}$ is still closed symmetric monoidal but no longer Cartesian exhibits $Top_{cg}^{\ast/}$ as being "more [[linear logic|linear]]" than $Top_{cg}$. The "full linearization" of $Top_{cg}$ is the closed symmteric monoidal category of [[structured spectra]] under [[smash product of spectra]]
which we discuss in [[Introduction to Stable homotopy theory -- 1|section 1]].

=--

Due to the [[idempotent monad|idempotency]] $k \circ k \simeq k$ (cor. \ref{kTopIsCoreflectiveSubcategory}) it is useful to know plenty of conditions under which a given topological space is already compactly generated, for then applying $k$ to it does not change it and one may continue working as in $Top$.

+-- {: .num_example #CWComplexIsCompactlyGenerated}
###### Example

Every [[CW-complex]] is [[compactly generated topological space|compactly generated]].

=--

+-- {: .proof}
###### Proof

Since [[a CW-complex is a Hausdorff space]], by prop. \ref{HausdorffImpliessWeaklyHausdorff} and  prop. \ref{CharacterizationOfCompactClosedSetsInWeaklyHausdorffSpace} its $k$-closed subsets are precisely those whose intersection with every [[compact subspace]] is closed.

Since a CW-complex $X$ is a [[colimit]] in [[Top]] over attachments of standard [[n-disks]] $D^{n_i}$ (its cells), by the characterization of colimits in $Top$ ([prop.](Top#DescriptionOfLimitsAndColimitsInTop)) a subset of $X$ is open or closed precisely if its restriction to each cell is open or closed, respectively. Since the $n$-disks are compact, this implies one direction: if a subset $A$ of $X$ intersected with all compact subsets is closed, then $A$ is closed.

For the converse direction, since [[a CW-complex is a Hausdorff space]] and since [[compact subspaces of Hausdorff spaces are closed]], the intersection of a closed subset with a compact subset is closed.

=--

For completeness we record further classes of examples:

+-- {: .num_example}
###### Example

The category $Top_{cg}$ of [[compactly generated topological spaces]] includes

1. all [[locally compact topological spaces]],

1. all [[first-countable topological spaces]],

   hence in particular

   1. all [[metrizable topological spaces]],

   1. all [[discrete topological spaces]],

   1. all [[codiscrete topological spaces]].

=--

([Lewis 78, p. 148](#Lewis78))

Recall that by corollary \ref{kTopIsCoreflectiveSubcategory}, all [[colimits]] of compactly generated spaces are again compactly generated.

+-- {: .num_example #ProductOfCWWithLocallyCompactCWIsCompactlyGenerated}
###### Example

The [[product topological space]] of a [[CW-complex]] with a [[compact topological space|compact]] CW-complex, and more generally with a [[locally compact topological space|locally compact]] CW-complex, is [[compactly generated topological space|compactly generated]].

=--

([Hatcher "Topology of cell complexes", theorem A.6](CW+complex#HatcherTopologyOfCellComplexes))

More generally:

+-- {: .num_example #ProductOfCompactlyGeneratedWithLocallyCompactHausdorff}
###### Proposition

For $X$ a [[compactly generated space]] and $Y$ a [[locally compact topological space|locally compact]] [[Hausdorff space]], then the [[product topological space]] $X\times Y$ is compactly generated.

=--

e.g. ([Strickland 09, prop. 26](#Strickland09))

Finally we check that the concept of [[homotopy]] and [[homotopy groups]] does not change under passing to compactly generated spaces:

+-- {: .num_prop #kificationComparisonIsWeakHomotopyEquivalence}
###### Proposition

For every topological space $X$, the canonical function $k(X) \longrightarrow X$ (the [[adjunction counit]]) is a [[weak homotopy equivalence]].

=--

+-- {: .proof}
###### Proof

By example \ref{CWComplexIsCompactlyGenerated}, example \ref{ProductOfCWWithLocallyCompactCWIsCompactlyGenerated} and lemma \ref{ContinuousFunctionsOutOfCompactlyGeneratedFactorThroughCompactlyGeneratedClosureOfCodomain}, continuous functions $S^n \to k(X)$ and their left homotopies $S^n \times I \to k(X)$ are in bijection with functions $S^n \to X$ and their homotopies $S^n \times I \to X$.

=--


+-- {: .num_theorem #ClassicalModelStructureOnCompactlyGeneratedTopologicalSpaces}
###### Theorem
**([[model structure on compactly generated topological spaces]])**

The restriction of the [[model category]] structure on $Top_{Quillen}$ from theorem \ref{TopQuillenModelStructure} along the inclusion $Top_{cg} \hookrightarrow Top$ of def. \ref{kTop} is still a model category structure, which is [[cofibrantly generated model category|cofibrantly generated]] by the same sets $I_{Top}$ (def. \ref{TopologicalGeneratingCofibrations}) and $J_{Top}$ (def. \ref{TopologicalGeneratingAcyclicCofibrations}). The [[k-ification]] coreflection of cor. \ref{kTopIsCoreflectiveSubcategory} is a  [[Quillen equivalence]] (def. \ref{QuillenEquivalence})

$$
  (Top_{cg})_{Quillen}
    \underoverset
      {\underset{k}{\longleftarrow}}
      {\hookrightarrow}
      {\bot}
  Top_{Quillen}
  \,.
$$

=--

+-- {: .proof}
###### Proof

By example \ref{CWComplexIsCompactlyGenerated}, the sets $I_{Top}$ and $J_{Top}$ are indeed in $Mor(Top_{cg})$. By example \ref{ProductOfCWWithLocallyCompactCWIsCompactlyGenerated} all arguments above about left homotopies between maps out of these basic cells go through verbatim in $Top_{cg}$. Hence the three technical lemmas above depending on actual [[point-set topology]],  topology, lemma \ref{CompactSubsetsAreSmallInCellComplexes}, lemma \ref{JTopRelativeCellComplexesAreWeakHomotopyEquivalences} and lemma \ref{AcyclicSerreFibrationsAreTheJTopFibrations}, go through verbatim as before. Accordingly, since the remainder of the proof of theorem \ref{TopQuillenModelStructure} of $Top_{Quillen}$ follows by general abstract arguments from these, it also still goes through verbatim for $(Top_{cg})_{Quillen}$ (repeatedly use the [[small object argument]] and the [[retract argument]] to establish the two weak factorization systems).

Hence the (acyclic) cofibrations in $(Top_{cg})_{Quillen}$ are identified with those in $Top_{Quillen}$, and so the inclusion is a part of a [[Quillen adjunction]] (def. \ref{QuillenAdjunction}). To see that this is a [[Quillen equivalence]] (def. \ref{QuillenEquivalence}), it is sufficient to check that for $X$ a compactly generated space then a continuous function $f \colon X \longrightarrow Y$ is a [[weak homotopy equivalence]] (def. \ref{WeakHomotopyEquivalenceOfTopologicalSpaces}) precisely if the [[adjunct]] $\tilde f \colon X \to k(Y)$ is a weak homotopy equivalence. But, by lemma \ref{ContinuousFunctionsOutOfCompactlyGeneratedFactorThroughCompactlyGeneratedClosureOfCodomain}, $\tilde f$ is the same function as $f$, just considered with different codomain. Hence the result follows with prop. \ref{kificationComparisonIsWeakHomotopyEquivalence}.


=--

$\,$

**Compactly generated weakly Hausdorff topological spaces**


While the inclusion $Top_{cg} \hookrightarrow Top$ of def. \ref{kTop} does satisfy the requirement that it gives a [[cartesian closed category]] with all [[limits]] and [[colimits]] and containing all [[CW-complexes]], one may ask for yet smaller subcategories that still share all these properties but potentially exhibit further convenient properties still.

A popular choice introduced in ([McCord 69](weakly+Hausdorff+topological+space#McCord69)) is to add the further restriction to topological spaces which are not only compactly generated but also [[weakly Hausdorff topological space|weakly Hausdorff]]. This was motivated from ([Steenrod 67](compactly+generated+topological+space#Steenrod67)) where compactly generated Hausdorff spaces were used by the observation (([McCord 69, section 2](weakly+Hausdorff+topological+space#McCord69))) that Hausdorffness is not preserved my many colimit operations, notably not by forming [[quotient spaces]].

On the other hand, in above we wouldn't have imposed Hausdorffness in the first place. More intrinsic advantages of $Top_{cgwH}$ over $Top_{cg}$ are the following:

* every [[pushout]] of a morphism in $Top_{cgwH} \hookrightarrow Top$ along a [[closed subspace]] inclusion in $Top$ is again in $Top_{cgwH}$

* in $Top_{cgwH}$ quotient spaces are not only preserved by [[cartesian products]] (as is the case for all compactly generated spaces due to $X\times (-)$ being a left adjoint, according to cor. \ref{kTopIsCoreflectiveSubcategory}) but by all [[pullbacks]]

* in $Top_{cgwH}$ the [[regular monomorphisms]] are the [[closed subspace]] inclusions

We will not need this here or in the following sections, but we briefly mention it for completenes:

+-- {: .num_defn #WeaklyHausdorff}
###### Definition

A [[topological space]] $X$ is called **[[weakly Hausdorff topological space|weakly Hausdorff]]** if for every [[continuous function]]

$$
  f \;\colon\; K \longrightarrow X
$$

out of a [[compact topological space|compact]] [[Hausdorff space]] $K$, its [[image]] $f(K) \subset X$  is a [[closed subset]] of $X$.

=--

+-- {: .num_prop #HausdorffImpliessWeaklyHausdorff}
###### Proposition

Every [[Hausdorff space]] is a [[weakly Hausdorff space]], def. \ref{WeaklyHausdorff}.

=--

+-- {: .proof}
###### Proof

Since [[compact subspaces of Hausdorff spaces are closed]].

=--


+-- {: .num_prop #CharacterizationOfCompactClosedSetsInWeaklyHausdorffSpace}
###### Proposition

For $X$ a [[weakly Hausdorff topological space]], def. \ref{WeaklyHausdorff}, then a subset $A \subset X$ is $k$-closed, def. \ref{kTop}, precisely if for every subset $K \subset X$ that is [[compact subspace|compact]] [[Hausdorff space|Hausdorff]] with respect to the [[subspace topology]], then the [[intersection]] $K \cap A$ is a [[closed subset]] of $X$.

=--

e.g. ([Strickland 09, lemma 1.4 (c)](#Strickland09))






### Topological enrichment
 {#TopologicalEnrichment}

So far the [[classical model structure on topological spaces]] which we established in theorem \ref{TopQuillenModelStructure}, as well as the [[projective model structure on functors|projective model structures on topologically enriched functors]] induced from it in theorem \ref{ProjectiveModelStructureOnTopologicalFunctors}, concern the [[hom-sets]], but not the [[hom-spaces]] (def. \ref{TopEnrichedCategory}), i.e. the model structure so far has not been related to the topology on [[hom-spaces]]. The following statements say that in fact the model structure and the enrichment by topology on the hom-spaces are compatible in a suitable sense: we have an "[[enriched model category]]". This implies in particular that the product/hom-adjunctions are [[Quillen adjunctions]], which is crucial for a decent discusson of the derived functors of the suspension/looping adjunction [below](#TheSuspensionLoopingDiscussion).

+-- {: .num_defn #PushoutProduct}
###### Definition

Let $i_1 \colon X_1 \to Y_1$ and $i_2 \colon X_2 \to Y_2$ be morphisms in $Top_{cg}$, def. \ref{kTop}. Their **[[pushout product]]**

$$
  i_1\Box i_2
   \coloneqq
  ((id, i_2), (i_1,id))
$$

is the universal morphism in the following diagram

$$
  \array{
    && X_1 \times X_2
    \\
    & {}^{\mathllap{(i_1,id)}}\swarrow && \searrow^{\mathrlap{(id,i_2)}}
    \\
    Y_1 \times X_2 && (po) && X_1 \times Y_2
    \\
    & {}_{\mathllap{}}\searrow && \swarrow
    \\
    && (Y_1 \times X_2) \underset{X_1 \times X_2}{\sqcup} (X_1 \times Y_2)
    \\
    && \downarrow^{\mathrlap{((id, i_2), (i_1,id))}}
    \\
    && Y_1 \times Y_2
  }
$$

=--

+-- {: .num_example #PushoutProductOfTwoInclusions}
###### Example

If $i_1 \colon X_1 \hookrightarrow Y_1$ and $i_2 \colon X_2 \hookrightarrow Y_2$ are inclusions, then their pushout product $i_1 \Box i_2$ from def. \ref{PushoutProduct} is the inclusion

$$
  \left(
     X_1 \times Y_2 \;\cup\; Y_1 \times X_2
  \right)
    \hookrightarrow
  Y_1 \times Y_2
  \,.
$$

For instance

$$
  \left(
    \{0\} \hookrightarrow I
  \right)
   \Box
  \left(
    \{0\} \hookrightarrow I
  \right)
$$

is the inclusion of two adjacent edges of a square into the square.

=--

+-- {: .num_example #PushoutProductWithInitialMorphism}
###### Example

The pushout product with an [[initial object|initial]] morphism
is just the ordinary [[Cartesian product]] functor

$$
  (\emptyset \to X) \Box (-)
    \simeq
  X \times (-)
  \,,
$$

i.e.

$$
  (\emptyset \to X) \Box (A \overset{f}{\to} B)
  \simeq
  (X\times A \overset{X \times f}{\longrightarrow} X \times B )
  \,.
$$

=--

+-- {: .proof}
###### Proof

The [[product topological space]] with the [[empty set|empty]] space is the empty space, hence the map $\emptyset \times A \overset{(id,f)}{\longrightarrow} \emptyset \times B$ is an isomorphism, and so the pushout in the pushout product is $X \times A$. From this one reads off the universal map in question to be $X \times  f$:

$$
  \array{
    && \emptyset \times A
    \\
    & {}^{\mathllap{}}\swarrow && \searrow^{\mathrlap{\simeq}}
    \\
    X \times A && (po) && \emptyset \times B
    \\
    & {}_{\mathllap{\simeq}}\searrow && \swarrow
    \\
    && X \times A
    \\
    && \downarrow^{\mathrlap{((id, f), \exists !)}}
    \\
    && X \times B
  }
  \,.
$$

=--

+-- {: .num_example #PushoutProductOfITopwithITopAndJTop}
###### Example

With

$$
  I_{Top} \colon \{ S^{n-1} \overset{i_n}{\hookrightarrow} D^n\}
  \;\;\;
  and
  \;\;\;
  J_{Top} \colon \{ D^n \overset{j_n}{\hookrightarrow} D^n \times I\}
$$

the generating cofibrations (def. \ref{TopologicalGeneratingCofibrations}) and generating acyclic cofibrations (def. \ref{TopologicalGeneratingAcyclicCofibrations}) of $(Top_{cg})_{Quillen}$ (theorem \ref{ClassicalModelStructureOnCompactlyGeneratedTopologicalSpaces}), then
their [[pushout-products]] (def. \ref{PushoutProduct}) are

$$
  \begin{aligned}
  i_{n_1} \Box i_{n_2} & \simeq i_{n_1 + n_2}
  \\
  i_{n_1} \Box j_{n_2} & \simeq j_{n_1 + n_2}
  \end{aligned}
  \,.
$$

=--

+-- {: .proof}
###### Proof

To see this, it is profitable to model [[n-disks]] and [[n-spheres]], up to [[homeomorphism]], as $n$-cubes $D^\n \simeq [0,1]^n \subset \mathbb{R}^n$ and their boundaries $S^{n-1} \simeq \partial [0,1]^n$ . For the idea of the proof, consider the situation in low dimensions, where one readily sees pictorially that

$$
  i_1 \Box i_1
  \;\colon\;
    \left(\;\; = \;\;\cup\;\; \vert\vert\;\;\right)
    \hookrightarrow
    \Box
$$

and

$$
  i_1 \Box j_0
  \;\colon\;
    \left(\;\; = \;\;\cup\;\; \vert \;\; \right)
    \hookrightarrow
    \Box
  \,.
$$

Generally, $D^n$ may be represented as the space of $n$-tuples of elements in $[0,1]$, and $S^n$ as the suspace of tuples for which at least one of the coordinates is equal to 0 or to 1.

Accordingly, $S^{n_1} \times D^{n_2} \hookrightarrow D^{n_1 + n_2}$ is the subspace of $(n_1+n_2)$-tuples, such that at least one of the first $n_1$ coordinates is equal to 0 or 1, while $D^{n_1} \times S^{n_2} \hookrightarrow D^{n_1+ n_2}$ is the subspace of $(n_1 + n_2)$-tuples such that east least one of the last $n_2$ coordinates is equal to 0 or to 1. Therefore

$$
  S^{n_1} \times D^{n_2} \cup D^{n_1} \times S^{n_2} \simeq S^{n_1 + n_2}
  \,.
$$

And of course it is clear that $D^{n_1} \times D^{n_2} \simeq D^{n_1 + n_2}$. This shows the first case.

For the second, use that $S^{n_1} \times D^{n_2} \times I$ is contractible to $S^{n_1} \times D^{n_2}$ in $D^{n_1} \times D^{n_2} \times I$, and that $S^{n_1} \times D^{n_2}$ is a subspace of $D^{n_1} \times D^{n_2}$.

=--


+-- {: .num_defn #PullbackPowering}
###### Definition

Let $i \colon A \to B$ and $p \colon X \to Y$ be two morphisms in $Top_{cg}$, def. \ref{kTop}. Their **pullback powering** is

$$
  p^{\Box i}
    \coloneqq
  (p^B, X^i)
$$

being the universal morphism in

$$
  \array{
    && X^B
    \\
    && \downarrow^{\mathrlap{(p^B, X^i)}}
    \\
    && Y^B \underset{Y^A}{\times} X^A
    \\
    & \swarrow && \searrow
    \\
    Y^B && (pb) && X^A
    \\
    & {}_{\mathllap{Y^i}}\searrow && \swarrow_{\mathrlap{p^A}}
    \\
    && Y^A
  }
$$

=--

+-- {: .num_prop #JoyalTierneyCalculus}
###### Proposition

Let $i_1, i_2 , p$ be three morphisms in $Top_{cg}$, def. \ref{kTop}. Then for their [[pushout-products]] (def. \ref{PushoutProduct}) and pullback-powerings (def. \ref{PullbackPowering}) the following [[lifting properties]] are equivalent ("[[Joyal-Tierney calculus]]"):

$$
  \array{
    &  i_1 \Box i_2 & \text{has LLP against} & p
    \\
    \Leftrightarrow & i_1 &  \text{has LLP against} & p^{\Box i_2}
    \\
    \Leftrightarrow & i_2 &  \text{has LLP against} & p^{\Box i_1}
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

We claim that by the [[cartesian closed category|cartesian closure]] of $Top_{cg}$, and carefully collecting terms, one finds a natural bijection between [[commuting squares]] and their [[lifts]] as follows:

$$
  \array{
    Q &\overset{f}{\longrightarrow}& X^B
    \\
    {}^{\mathllap{i_1}}\downarrow && \downarrow^{\mathrlap{p^{\Box i_2}}}
    \\
    P &\underset{(g_1,g_2)}{\longrightarrow}& Y^B \underset{Y^A}{\times} X^A
  }
  \;\;\;\;\;\;\;
  \leftrightarrow
  \;\;\;\;\;\;\;
  \array{
    Q \times B \underset{Q \times A}{\sqcup} P \times A
    &\overset{(\tilde f, \tilde g_2)}{\longrightarrow}&
    X
    \\
    {}^{\mathllap{i_1 \Box i_2}}\downarrow && \downarrow^{\mathrlap{p}}
    \\
    P \times B & \underset{\tilde g_1}{\longrightarrow} & Y
  }
  \,,
$$

where the tilde denotes product/hom-[[adjuncts]], for instance

$$
  \frac{
    P \overset{g_1}{\longrightarrow} Y^B
  }{
    P \times B \overset{\tilde g_1}{\longrightarrow} Y
  }
$$

etc.

To see this in more detail, observe that both squares above each represent two squares from the two components into the fiber product and out of the pushout, respectively, as well as one more square exhibiting the compatibility condition on these components:

$$
 \begin{aligned}
   &
   \;\;\;\;
  \array{
    Q &\overset{f}{\longrightarrow}& X^B
    \\
    {}^{\mathllap{i_1}}\downarrow && \downarrow^{\mathrlap{p^{\Box i_2}}}
    \\
    P &\underset{(g_1,g_2)}{\longrightarrow}& Y^B \underset{Y^A}{\times} X^A
  }
   \\
  \simeq &
   \;\;\;\;
   \left\{
    \;\;\;\;
    \array{
      Q &\overset{f}{\longrightarrow}& X^B
      \\
      {}^{\mathllap{i_1}}\downarrow && \downarrow^{\mathrlap{p^B}}
      \\
      P &\underset{g_1}{\longrightarrow}& Y^B
    }
  \;\;\;\;\;
  \,,
  \;\;\;\;\;
    \array{
      Q &\overset{f}{\longrightarrow}& X^B
      \\
      {}^{\mathllap{i_1}}\downarrow && \downarrow^{\mathrlap{X^{i_2}}}
      \\
      P &\underset{g_1}{\longrightarrow}& X^A
    }
  \;\;\;\;\;
  \,,
  \;\;\;\;\;
  \array{
    P &\overset{g_2}{\longrightarrow}& X^A
    \\
    {}^{\mathllap{g_1}}\downarrow && \downarrow^{\mathrlap{p^A}}
    \\
    Y^B &\underset{Y^{i_2}}{\longrightarrow}& Y^A
  }
  \;\;\;\;\;
  \right\}
  \\
  \leftrightarrow
  &
  \;\;\;\;
  \left\{
    \;\;\;\;\;
    \array{
      Q \times B &\overset{\tilde f}{\longrightarrow}& X
      \\
      {}^{\mathllap{(i_1,id)}}\downarrow && \downarrow^{\mathrlap{p}}
      \\
      P \times B &\underset{\tilde g_2}{\longrightarrow}& Y
    }
    \;\;\;\;\;
    \,,
    \;\;\;\;\;
    \array{
      Q \times A &\overset{(id,i_2)}{\longrightarrow}& Q \times B
      \\
      {}^{\mathllap{(i_1,id)}}\downarrow && \downarrow^{\mathrlap{\tilde f}}
      \\
      P \times A &\underset{\tilde g_2}{\longrightarrow}& X
    }
    \;\;\;\;\;
    \,,
    \;\;\;\;\;
    \array{
      P \times A &\overset{\tilde g_2}{\longrightarrow}& X
      \\
      {}^{\mathllap{(id,i_2)}}\downarrow && \downarrow^{\mathrlap{p}}
      \\
      P \times B &\underset{\tilde g_1}{\longrightarrow}& Y
    }
    \;\;\;\;\;
  \right\}
  \\
  \simeq
  &
  \;\;\;\;
  \array{
    Q \times B \underset{Q \times A}{\sqcup} P \times A
    &\overset{(\tilde f, \tilde g_2)}{\longrightarrow}&
    X
    \\
    {}^{\mathllap{i_1 \Box i_2}}\downarrow && \downarrow^{\mathrlap{p}}
    \\
    P \times B & \underset{\tilde g_1}{\longrightarrow} & Y
  }
  \end{aligned}
  \,.
$$


=--


+-- {: .num_prop #PushoutProductInTopCGSendsCofCofToCof}
###### Proposition

The [[pushout-product]] in $Top_{cg}$ (def. \ref{kTop}) of two classical cofibrations is a classical cofibration:

$$
  Cof_{cl} \Box Cof_{cl} \subset Cof_{cl}
  \,.
$$

If one of them is acyclic, then so is the pushout-product:

$$
  Cof_{cl} \Box (W_{cl} \cap Cof_{cl}) \subset W_{cl}\cap Cof_{cl}
  \,.
$$


=--

+-- {: .proof}
###### Proof

Regarding the first point:

By example \ref{PushoutProductOfITopwithITopAndJTop} we have

$$
  I_{Top} \Box I_{Top} \subset I_{Top}
$$

Hence

$$
  \array{
    & I_{Top} \Box I_{Top} & \text{has LLP against} & W_{cl} \cap Fib_{cl}
    \\
    \Leftrightarrow
    & I_{Top} & \text{has LLP against} & (W_{cl} \cap Fib_{cl})^{\Box I_{Top}}
    \\
    \Rightarrow
    & Cof_{cl} & \text{has LLP against} & (W_{cl} \cap Fib_{cl})^{\Box I_{Top}}
    \\
    \Leftrightarrow
    &
    I_{Top} \Box Cof_{cl} & \text{has LLP against} & W_{cl} \cap Fib_{cl}
    \\
    \Leftrightarrow
    &
    I_{Top} & \text{has LLP against} & (W_{cl} \cap Fib_{cl})^{Cof_{cl}}
    \\
    \Rightarrow
    & Cof_{cl} & \text{has LLP against} & (W_{cl} \cap Fib_{cl})^{Cof_{cl}}
    \\
    \Leftrightarrow
    & Cof_{cl} \Box \Cof_{cl}  & \text{has LLP against} & W_{cl} \cap Fib_{cl}
  }
  \,,
$$

where all logical equivalences used are those of prop. \ref{JoyalTierneyCalculus} and where all implications appearing are by the closure property of lifting problems, prop. \ref{ClosurePropertiesOfInjectiveAndProjectiveMorphisms}.

Regarding the second point: By example \ref{PushoutProductOfITopwithITopAndJTop} we moreover have

$$
  I_{Top} \Box J_{Top} \subset J_{Top}
$$

and the conclusion follows by the same kind of reasoning.

=--

+-- {: .num_remark}
###### Remark

In [[model category]] theory the property in proposition \ref{PushoutProductInTopCGSendsCofCofToCof} is referred to as saying that the model category $(Top_{cg})_{Quillen}$ from theorem \ref{ClassicalModelStructureOnCompactlyGeneratedTopologicalSpaces}

1. is a [[monoidal model category]] with respect to the [[Cartesian product]] on $Top_{cg}$;

1. is an [[enriched model category]], over itself.


=--

A key point of what this entails is the following:

+-- {: .num_prop #HomProductAdjunctionForCofibrantObjectInTopCGIsQuillen}
###### Proposition

For $X \in (Top_{cg})_{Quillen}$ cofibrant (a [[retract]] of a [[cell complex]]) then the product-hom-adjunction for $Y$ (prop. \ref{CartesianClosureOfTopcg}) is a [[Quillen adjunction]]

$$
  (Top_{cg})_{Quillen}
   \underoverset
     \underset{(-)^X}{\longrightarrow}
     \overset{X \times (-)}{\longleftarrow}
     {\bot}
  (Top_{cg})_{Quillen}
  \,.
$$

=--

+-- {: .proof}
###### Proof

By example \ref{PushoutProductWithInitialMorphism} we have that the [[left adjoint]] functor is equivalently the [[pushout product]] functor with the initial morphism of $X$:

$$
  X \times (-)
  \simeq
  (\emptyset \to X) \Box (-)
  \,.
$$

By assumption $(\emptyset \to X)$ is a cofibration, and hence prop. \ref{PushoutProductInTopCGSendsCofCofToCof} says that this is a left Quillen functor.

=--

The statement and proof of prop. \ref{HomProductAdjunctionForCofibrantObjectInTopCGIsQuillen} has a direct analogue in [[pointed topological spaces]]

+-- {: .num_prop #HomProductAdjunctionForCofibrantObjectInPointedTopCGIsQuillen}
###### Proposition

For $X \in (Top^{\ast/}_{cg})_{Quillen}$ cofibrant with respect to the [[classical model structure on pointed topological spaces|classical model structure on pointed]] [[compactly generated topological spaces]] (theorem \ref{ClassicalModelStructureOnCompactlyGeneratedTopologicalSpaces}, prop. \ref{ModelStructureOnSliceCategory}) (hence a [[retract]] of a [[cell complex]] with non-degenerate basepoint, remark \ref{NonDegenerateBasepointAsCofibrantObjects}) then the pointed product-hom-adjunction from corollary \ref{SmashHomAdjunctionOnPointedCompactlyGeneratedTopologicalSpaces}  is a [[Quillen adjunction]] (def. \ref{QuillenAdjunction}):

$$
  (Top^{\ast/}_{cg})_{Quillen}
   \underoverset
     \underset{Maps(X,-)_\ast}{\longrightarrow}
     \overset{X \wedge (-)}{\longleftarrow}
     {\bot}
  (Top^{\ast/}_{cg})_{Quillen}
  \,.
$$

=--

+-- {: .proof}
###### Proof

Let now $\Box_\wedge$ denote the **smash pushout product** and $(-)^{\Box(-)}$ the **smash pullback powering** defined as in def. \ref{PushoutProduct} and def. \ref{PullbackPowering}, but with [[Cartesian product]] replaced by [[smash product]] (def. \ref{SmashProductOfPointedObjects}) and compactly generated [[mapping space]] replaced by pointed mapping spaces (def. \ref{PointedMappingSpace}).

By theorem \ref{CofibrantGenerationOfPointedTopologicalSpaces} $(Top_{cg}^{\ast/})_{Quillen}$ is [[cofibrantly generated model category|cofibrantly generated]] by $I_{Top^{\ast/}} = (I_{Top})_+$ and $J_{Top^{\ast/}}= (J_{Top})_+$. Example \ref{WedgeAndSmashOfBasePointAdjoinedTopologicalSpaces} gives that for $i_n \in I_{Top}$ and $j_n \in J_{Top}$ then

$$
  (i_{n_1})_+ \Box_\wedge (i_{n_2})_+ \simeq (i_{n_1 + n_2})_+
$$

and

$$
  (i_{n_1})_+ \wedge_\wedge (i_{n_2})_+ \simeq (i_{n_1 + n_2})_+
  \,.
$$

Hence the pointed analog of prop. \ref{PushoutProductInTopCGSendsCofCofToCof} holds and therefore so does the pointed analog of the conclusion in prop. \ref{HomProductAdjunctionForCofibrantObjectInTopCGIsQuillen}.


=--





### Model structure on topological functors
 {#ModelStructureOnTopEnrichedFunctors}

With classical topological homotopy theory in hand (theorem \ref{TopQuillenModelStructure}, theorem \ref{ClassicalModelStructureOnCompactlyGeneratedTopologicalSpaces}), it is straightforward now to generalize this to a homotopy theory of _topological diagrams_. This is going to be the basis for the [[stable homotopy theory]] of [[spectra]], because spectra may be identified with certain topological diagrams ([prop.](Introduction+to+Stable+homotopy+theory+--+1-1#SequentialSpectraAsDiagramSpectra)).

Technically, "topological diagram" here means "[[Top]]-[[enriched functor]]". We now discuss what this means and then observe that as an immediate corollary of theorem \ref{TopQuillenModelStructure} we obtain a model category structure on topological diagrams.

As a by-product, we obtain the model category theory of [[homotopy colimits]] in topological spaces, which will be useful.

In the following we say _[[Top]]-[[enriched category]]_ and _[[Top]]-[[enriched functor]]_ etc. for what often is referred to as "[[topological category]]" and "[[topological functor]]" etc. As discussed there, these latter terms are ambiguous.

**Literature** ([[Categorical Homotopy Theory|Riehl, chapter 3]]) for basics of [[enriched category theory]]; ([Piacenza 91](classical+model+structure+on+topological+spaces#Piacenza91)) for the [[projective model structure on functors|projective model structure on topological functors]].

$\,$


+-- {: .num_defn #TopEnrichedCategory}
###### Definition

A **[[topologically enriched category]]** $\mathcal{C}$ is a $Top_{cg}$-[[enriched category]], hence:

1. a [[class]] $Obj(\mathcal{C})$, called the **class of [[objects]]**;

1. for each $a, b\in Obj(\mathcal{C})$ a [[compactly generated topological space]] (def. \ref{kTop})

   $$
     \mathcal{C}(a,b)\in Top_{cg}
     \,,
   $$

   called the **space of [[morphisms]]** or the **[[hom-space]]** between $a$ and $b$;

1. for each $a,b,c\in Obj(\mathcal{C})$ a [[continuous function]]

   $$
     \circ_{a,b,c} \;\colon\; \mathcal{C}(a,b)\times \mathcal{C}(b,c) \longrightarrow \mathcal{C}(a,c)
   $$

   out of the [[cartesian product]] (by cor. \ref{kTopIsCoreflectiveSubcategory}: the image under $k$ of the [[product topological space]]), called the _[[composition]]_ operation;

1. for each $a \in Obj(\mathcal{C})$ a point $Id_a\in \mathcal{C}(a,a)$, called the _[[identity]]_ morphism on $a$

such that the composition is [[associativity|associative]] and [[unitality|unital]].

Similarly a **pointed topologically enriched category** is such a structure with $Top_{cg}$ replaced by $Top^{\ast/}_{cg}$ (def. \ref{CategoryOfPointedObjects}) and with the [[Cartesian product]] replaced by the [[smash product]] (def. \ref{SmashProductOfPointedObjects}) of pointed topological spaces.

=--

+-- {: .num_remark #UnderlyingCategoryOfTopEnrichedCategory}
###### Remark

Given a (pointed) [[topologically enriched category]] as in def. \ref{TopEnrichedCategory}, then forgetting the topology on the [[hom-spaces]] (along the [[forgetful functor]] $U \colon Top_{cg} \to Set$) yields an ordinary [[locally small category]] with

$$
  Hom_{\mathcal{C}}(a,b) = U(\mathcal{C}(a,b))
  \,.
$$

It is in this sense that $\mathcal{C}$ is a category with [[extra structure]], and hence "[[enriched category|enriched]]".

=--

The archetypical example is $Top_{cg}$ itself:

+-- {: .num_example #TopkAsATopologicallyEnrichedCategory}
###### Example

The category $Top_{cg}$ (def. \ref{kTop}) canonically obtains the structure of a [[topologically enriched category]], def. \ref{TopEnrichedCategory}, with [[hom-spaces]] given by the compactly generated [[mapping spaces]] (def. \ref{CompactlyGeneratedMappingSpaces})

$$
  Top_{cg}(X,Y)
    \coloneqq
  Y^X
$$

and with [[composition]]

$$
  Y^X \times Z^Y
    \longrightarrow
  Z^X
$$

given by the [[adjunct]] under the (product$\dashv$ mapping-space)-[[adjunction]] from prop. \ref{CartesianClosureOfTopcg} of the [[evaluation morphisms]]

$$
  X \times Y^X \times Z^Y
    \overset{(ev, id)}{\longrightarrow}
  Y \times Z^Y
    \overset{ev}{\longrightarrow}
  Z
  \,.
$$

Similarly, [[pointed topological spaces|pointed]] [[compactly generated topological spaces]] $Top_k^{\ast/}$ form a pointed topologically enriched category, using the [[pointed mapping spaces]] from example \ref{PointedMappingSpace}:

$$
  Top^{\ast/}_{cg}(X,Y)
   \coloneqq
  Maps(X,Y)_\ast
  \,.
$$

=--

+-- {: .num_defn #TopologicallyEnrichedFunctor}
###### Definition

A [[topologically enriched functor]] between two [[topologically enriched categories]]

$$
  F \;\colon\;  \mathcal{C}  \longrightarrow \mathcal{D}
$$

is a $Top_{cg}$-[[enriched functor]], hence:

1. a [[function]]

   $$
     F_0 \;\colon\; Obj(\mathcal{C}) \longrightarrow Obj(\mathcal{D})
   $$

   of [[objects]];

1. for each $a,b \in Obj(\mathcal{C})$ a [[continuous function]]

   $$
     F_{a,b} \;\colon\; \mathcal{C}(a,b) \longrightarrow \mathcal{D}(F_0(a), F_0(b))
   $$

   of [[hom-spaces]],

such that this preserves [[composition]] and [[identity]] morphisms in the evident sense.

A [[homomorphism]] of topologically enriched functors

$$
  \eta \;\colon\; F \Rightarrow G
$$

is a $Top_{cg}$-[[enriched natural transformation]]: for each $c \in Obj(\mathcal{C})$ a choice of morphism $\eta_c \in \mathcal{D}(F(c),G(c))$ such that for each pair of objects $c,d \in \mathcal{C}$ the two continuous functions

$$
  \eta_d \circ F(-) \;\colon\; \mathcal{C}(c,d) \longrightarrow \mathcal{D}(F(c), G(d))
$$

and

$$
  G(-) \circ \eta_c \;\colon\; \mathcal{C}(c,d) \longrightarrow \mathcal{D}(F(c), G(d))
$$

agree.

We write $[\mathcal{C}, \mathcal{D}]$ for the resulting category of topologically enriched functors.

=--

+-- {: .num_remark #TopologicallyEnrichedNaturalTransformationIsTransformationOfUnderlyingFunctors}
###### Remark

The condition on an [[enriched natural transformation]] in def. \ref{TopologicallyEnrichedFunctor} is just that on an ordinary [[natural transformation]] on the underlying unenriched functors, saying that for every morphisms $f \colon c \to d$ there is a [[commuting square]]

$$
  f
  \;\;\;\;
  \mapsto
  \;\;\;\;
  \array{
    \mathcal{C}(c,c) \times X &\overset{\eta_c}{\longrightarrow}& F(c)
    \\
    {}^{\mathllap{\mathcal{C}(c,f)}}\downarrow && \downarrow^{\mathrlap{F(f)}}
    \\
    \mathcal{C}(c,d) \times X &\underset{\eta_d}{\longrightarrow}& F(d)
  }
  \,.
$$

=--


+-- {: .num_example #TopologicallyEnrichedFunctorsToTopk}
###### Example

For $\mathcal{C}$ any [[topologically enriched category]], def. \ref{TopEnrichedCategory} then a [[topologically enriched functor]] (def. \ref{TopologicallyEnrichedFunctor})

$$
  F \;\colon\; \mathcal{C} \longrightarrow Top_{cg}
$$

to the archetypical topologically enriched category from example \ref{TopkAsATopologicallyEnrichedCategory} may be thought of as a topologically enriched [[copresheaf]], at least if $\mathcal{C}$ is [[small category|small]] (in that its [[class]] of objects is a proper [[set]]).

Hence the category of topologically enriched functors

$$
  [\mathcal{C}, Top_{cg}]
$$

according to def. \ref{TopologicallyEnrichedFunctor} may be thought of as the ([[copresheaf|co-]])[[presheaf category]] over $\mathcal{C}$ in the realm of topological enriched categories.

A functor $F \in [\mathcal{C}, Top_{cg}]$ is equivalently

1. a [[compactly generated topological space]] $F_a \in Top_{cg}$ for each object $a \in Obj(\mathcal{C})$;

1. a [[continuous function]]

   $$
     F_a \times \mathcal{C}(a,b) \longrightarrow F_b
   $$

   for all pairs of objects $a,b \in Obj(\mathcal{C})$

such that composition is respected, in the evident sense.

For every object $c \in \mathcal{C}$, there is a topologically enriched [[representable functor]], denoted $y(c)$ or $\mathcal{C}(c,-)$ which sends objects to

$$
  y(c)(d) = \mathcal{C}(c,d) \in Top_{cg}
$$

and whose action on morphisms is, under the above identification, just the [[composition]] operation in $\mathcal{C}$.

=--

+-- {: .num_prop #TopologicallyEnrichedCopresheavesHaveAllLimitsAndColimits}
###### Proposition

For $\mathcal{C}$ any [[small category|small]] [[topologically enriched category]], def. \ref{TopEnrichedCategory} then the [[enriched functor category]] $[\mathcal{C}, Top_{cg}]$ from example \ref{TopologicallyEnrichedFunctorsToTopk} has all [[limits]] and [[colimits]], and they are computed objectwise:

if

$$
  F_\bullet
    \;\colon\;
  I
    \longrightarrow
  [\mathcal{C}, Top_{cg}]
$$

is a [[diagram]] of [[functors]] and $c\in \mathcal{C}$ is any object, then

$$
  (\underset{\longleftarrow}{\lim}_i F_i)(c) \simeq \underset{\longleftarrow}{\lim}_i (F_i(c)) \;\;\in Top_{cg}
$$

and

$$
  (\underset{\longrightarrow}{\lim}_i F_i)(c) \simeq \underset{\longrightarrow}{\lim}_i (F_i(c)) \;\; \in Top_{cg}
  \,.
$$

=--

+-- {: .proof}
###### Proof

First consider the underlying diagram of functors $F_i^\circ$ where the topology on the [[hom-spaces]] of $\mathcal{C}$ and of $Top_{cg}$ has been forgotten. Then one finds

$$
  (\underset{\longleftarrow}{\lim}_i F^\circ_i)(c) \simeq \underset{\longleftarrow}{\lim}_i (F^\circ_i(c)) \;\;\in Set
$$

and

$$
  (\underset{\longrightarrow}{\lim}_i F^\circ _i)(c) \simeq \underset{\longrightarrow}{\lim}_i (F^\circ_i(c)) \;\; \in Set
$$

by the [[universal property]] of limits and colimits. (Given a morphism of diagrams then a unique compatible morphism between their limits or colimits, respectively, is induced as the universal factorization of the morphism of diagrams regarded as a cone or cocone, respectvely, over the codomain or domain diagram, respectively).

Hence it only remains to see that equipped with topology, these limits and colimits in $Set$ become limits and colimits in $Top_{cg}$. That is just the statement of prop. \ref{DescriptionOfLimitsAndColimitsInTop} with corollary \ref{kTopIsCoreflectiveSubcategory}.


=--


+-- {: .num_defn #TensoringAndPoweringOfTopologicallyEnrichedCopresheaves}
###### Definition

Let $\mathcal{C}$ be a [[topologically enriched category]], def. \ref{TopEnrichedCategory}, with $[\mathcal{C}, Top_{cg}]$ its category of topologically enriched copresheaves from example \ref{TopologicallyEnrichedFunctorsToTopk}.

1. Define a functor

   $$
     (-)\cdot(-)
       \;\colon\;
     [\mathcal{C}, Top_{cg}] \times Top_{cg}
      \longrightarrow
     [\mathcal{C}, Top_{cg}]
   $$

   by forming objectwise [[cartesian products]] (hence $k$ of [[product topological spaces]])

   $$
     F \cdot X \;\colon\; c \mapsto F(c) \times X
     \,.
   $$

   This is called the **[[tensoring]]** of $[\mathcal{C},Top_{cg}]$ over $Top_{cg}$.

1. Define a functor

   $$
     (-)^{(-)}
       \;\colon\;
     (Top_{cg})^{op} \times [\mathcal{C}, Top_{cg}]
       \longrightarrow
     [\mathcal{C}, Top_{cg}]
   $$

   by forming objectwise compactly generated [[mapping spaces]] (def. \ref{CompactlyGeneratedMappingSpaces})

   $$
     F^X \;\colon\; c \mapsto F(c)^X
     \,.
   $$

   This is called the **[[powering]]** of $[\mathcal{C}, Top_{cg}]$ over $Top_{cg}$.

Analogously, for $\mathcal{C}$ a pointed [[topologically enriched category]], def. \ref{TopEnrichedCategory}, with $[\mathcal{C}, Top_{cg}^{\ast/}]$ its category of pointed topologically enriched copresheaves from example \ref{TopologicallyEnrichedFunctorsToTopk}, then:

1. Define a functor

   $$
     (-)\wedge(-)
       \;\colon\;
     [\mathcal{C}, Top^{\ast/}_{cg}] \times Top^{\ast/}_{cg}
      \longrightarrow
     [\mathcal{C}, Top^{\ast/}_{cg}]
   $$

   by forming objectwise [[smash products]] (def. \ref{SmashProductOfPointedObjects})

   $$
     F \wedge X \;\colon\; c \mapsto F(c) \wedge X
     \,.
   $$

   This is called the **smash [[tensoring]]** of $[\mathcal{C},Top^{\ast/}_{cg}]$ over $Top^{\ast/}_{cg}$.

1. Define a functor

   $$
     Maps(-,-)_\ast
       \;\colon\;
     Top^{\ast/}_{cg} \times [\mathcal{C}, Top^{\ast/}_{cg}]
       \longrightarrow
     [\mathcal{C}, Top^{\ast/}_{cg}]
   $$

   by forming objectwise [[pointed mapping spaces]] (example \ref{PointedMappingSpace})

   $$
     F^X \;\colon\; c \mapsto Maps(X,F(c))_\ast
     \,.
   $$

   This is called the **pointed [[powering]]** of $[\mathcal{C}, Top_{cg}]$ over $Top_{cg}$.


=--

There is a full blown $Top_{cg}$-[[enriched Yoneda lemma]]. The following records a slightly simplified version which is all that is needed here:

+-- {: .num_prop #TopologicallyEnrichedYonedaLemma}
###### Proposition
**(topologically enriched Yoneda-lemma)**

Let $\mathcal{C}$ be a [[topologically enriched category]], def. \ref{TopEnrichedCategory}, write $[\mathcal{C}, Top_{cg}]$ for its category of topologically enriched (co-)presheaves, and for $c\in Obj(\mathcal{C})$ write $y(c) = \mathcal{C}(c,-) \in [\mathcal{C}, Top_k]$ for the topologically enriched functor that it represents, all according to example \ref{TopologicallyEnrichedFunctorsToTopk}. Recall the [[tensoring]] operation $(F,X) \mapsto F \cdot X$ from def. \ref{TensoringAndPoweringOfTopologicallyEnrichedCopresheaves}.

For $c\in Obj(\mathcal{C})$, $X \in Top_{cg}$ and $F \in [\mathcal{C}, Top_{cg}]$, there is a [[natural bijection]] between

1. morphisms $y(c) \cdot X \longrightarrow F$ in $[\mathcal{C}, Top_{cg}]$;

1. morphisms $X \longrightarrow F(c)$ in $Top_{cg}$.

In short:

$$
  \frac{
    y(c)\cdot X \longrightarrow F
  }{
    X \longrightarrow F(c)
  }
$$


=--

+-- {: .proof}
###### Proof

Given a morphism $\eta \colon y(c) \cdot X \longrightarrow F$ consider its component

$$
  \eta_c \;\colon\; \mathcal{C}(c,c)\times X \longrightarrow F(c)
$$

and restrict that to the identity morphism $id_c \in \mathcal{C}(c,c)$ in the first argument

$$
  \eta_c(id_c,-) \;\colon\; X \longrightarrow F(c)
  \,.
$$

We claim that just this $\eta_c(id_c,-)$ already uniquely determines all components

$$
  \eta_d \;\colon\; \mathcal{C}(c,d)\times X \longrightarrow F(d)
$$

of $\eta$, for all $d \in Obj(\mathcal{C})$: By definition of the transformation $\eta$ (def. \ref{TopologicallyEnrichedFunctor}), the two functions

$$
   F(-) \circ \eta_c
  \;\colon\;
  \mathcal{C}(c,d)
  \longrightarrow
  F(d)^{\mathcal{C}(c,c) \times X}
$$

and

$$
  \eta_d  \circ \mathcal{C}(c,-) \times X
  \;\colon\;
  \mathcal{C}(c,d)
  \longrightarrow
  F(d)^{\mathcal{C}(c,c) \times X}
$$

agree. This means (remark \ref{TopologicallyEnrichedNaturalTransformationIsTransformationOfUnderlyingFunctors}) that they may be thought of jointly as a function with values in commuting squares in $Top_{cg}$ of this form:

$$
  f
  \;\;\;\;
  \mapsto
  \;\;\;\;
  \array{
    \mathcal{C}(c,c) \times X &\overset{\eta_c}{\longrightarrow}& F(c)
    \\
    {}^{\mathllap{\mathcal{C}(c,f)}}\downarrow && \downarrow^{\mathrlap{F(f)}}
    \\
    \mathcal{C}(c,d) \times X &\underset{\eta_d}{\longrightarrow}& F(d)
  }
$$

For any $f \in \mathcal{C}(c,d)$, consider the restriction of

$$
  \eta_d \circ \mathcal{C}(c,f) \in F(d)^{\mathcal{C}(c,c) \times X}
$$

to $id_c \in \mathcal{C}(c,c)$, hence restricting the above commuting squares to

$$
  f
  \;\;\;\;
  \mapsto
  \;\;\;\;
  \array{
    \{id_c\} \times X &\overset{\eta_c}{\longrightarrow}& F(c)
    \\
    {}^{\mathllap{\mathcal{C}(c,f)}}\downarrow 
      && 
    \downarrow^{\mathrlap{F(f)}}
    \\
    \{f\} \times X &\underset{\eta_d}{\longrightarrow}& F(d)
  }
$$

This shows that $\eta_d$ is fixed to be the function

$$
  \eta_d(f,x) = F(f)\circ \eta_c(id_c,x)
$$

and this is a continuous function since all the operations it is built from are continuous.

Conversely, given a continuous function $\alpha \colon X \longrightarrow F(c)$, define for each $d$ the function

$$
  \eta_d \colon (f,x) \mapsto F(f) \circ \alpha
  \,.
$$

Running the above analysis backwards shows that this determines a transformation $\eta \colon y(c)\times X \to F$.


=--



+-- {: .num_defn #GeneratingCofibrationsForProjectiveStructureOnFunctors}
###### Definition

For $\mathcal{C}$ a [[small category|small]] topologically enriched category, def. \ref{TopEnrichedCategory}, write

$$
  I_{Top}^{\mathcal{C}}
   \;\coloneqq\;
  \left\{
    y(c)\cdot (S^{n-1} \overset{\iota_n}{\longrightarrow} D^n)
  \right\}_{{n \in \mathbb{N},} \atop {c \in Obj(\mathcal{C})}}
$$

and

$$
  J_{Top}^{\mathcal{C}}
  \;\coloneqq\;
  \left\{
    y(c)\cdot (D^n \overset{(id, \delta_0)}{\longrightarrow} D^n \times I)
  \right\}_{{n \in \mathbb{N},} \atop {c \in Obj(\mathcal{C})}}
$$

for the sets of morphisms given by [[tensoring]] (def. \ref{TensoringAndPoweringOfTopologicallyEnrichedCopresheaves}) the representable functors (example \ref{TopologicallyEnrichedFunctorsToTopk}) with the generating cofibrations (def.\ref{TopologicalGeneratingCofibrations}) and acyclic generating cofibrations (def. \ref{TopologicalGeneratingAcyclicCofibrations}), respectively, of $(Top_{cg})_{Quillen}$ (theorem \ref{ClassicalModelStructureOnCompactlyGeneratedTopologicalSpaces}).

These are going to be called the **[[generating cofibrations]]** and **acyclic generating cofibrations** for the _projective [[model structure on functors|model structure on topologically enriched functors]]_ over $\mathcal{C}$.

Analogously, for $\mathcal{C}$ a [[pointed topological space|pointed topologically]]-[[enriched category]], write

$$
  I_{Top^{\ast/}}^{\mathcal{C}}
  \;\coloneqq\;
  \left\{
    y(c) \wedge (S^{n-1}_+ \overset{(\iota_n)_+}{\longrightarrow} D^n_+)
  \right\}_{{n \in \mathbb{N},} \atop {c \in Obj(\mathcal{C})}}
$$

and

$$
  J_{Top^{\ast/}}^{\mathcal{C}}
  \;\coloneqq\;
  \left\{
    y(c) \wedge (D^n_+ \overset{(id, \delta_0)_+}{\longrightarrow} (D^n \times I)_+)
  \right\}_{{n \in \mathbb{N},} \atop {c \in Obj(\mathcal{C})}}
$$

for the analogous construction applied to the pointed generating (acyclic) cofibrations of def. \ref{GeneratingCofibrationsForPointedTopologicalSpaces}.

=--





+-- {: .num_defn #ClassesOfMorphismsInTheProjectiveModelStructureOnTopEnrichedFunctors}
###### Definition

Given a [[small category|small]] (pointed) [[topologically enriched category]] $\mathcal{C}$, def. \ref{TopEnrichedCategory}, say that a morphism in the category of (pointed) topologically enriched copresheaves $[\mathcal{C}, Top_{cg}]$ ($[\mathcal{C},Top_{cg}^{\ast/}]$), example \ref{TopologicallyEnrichedFunctorsToTopk}, hence a [[natural transformation]] between topologically enriched functors, $\eta \colon F \to G$ is

* a **projective weak equivalence**, if for all $c\in Obj(\mathcal{C})$ the component $\eta_c \colon F(c) \to G(c)$ is a [[weak homotopy equivalence]] (def. \ref{WeakHomotopyEquivalenceOfTopologicalSpaces});

* a **projective fibration** if for all $c\in Obj(\mathcal{C})$ the component $\eta_c \colon F(c) \to G(c)$ is a [[Serre fibration]] (def. \ref{SerreFibration});

* a **projective cofibration** if it is a [[retract]] (rmk. \ref{RetractsOfMorphisms}) of an $I_{Top}^{\mathcal{C}}$-[[relative cell complex]] (def. \ref{TopologicalCCellComplex}, def. \ref{GeneratingCofibrationsForProjectiveStructureOnFunctors}).

Write

$$
  [\mathcal{C}, (Top_{cg})_{Quillen}]_{proj}
$$

and

$$
  [\mathcal{C}, (Top^{\ast/}_{cg})_{Quillen}]_{proj}
$$


for the categories of topologically enriched functors equipped with these classes of morphisms.

=--

+-- {: .num_theorem #ProjectiveModelStructureOnTopologicalFunctors}
###### Theorem

The classes of morphisms in def. \ref{ClassesOfMorphismsInTheProjectiveModelStructureOnTopEnrichedFunctors} constitute a [[model category]] structure on $[\mathcal{C}, Top_{cg}]$ and $[\mathcal{C}, Top^{\ast/}_{cg}]$, called the **[[projective model structure on enriched functors]]**

$$
  [\mathcal{C}, (Top_{cg})_{Quillen}]_{proj}
$$

and

$$
  [\mathcal{C}, (Top^{\ast/}_{cg})_{Quillen}]_{proj}
$$


These are [[cofibrantly generated model category]], def. \ref{CofibrantlyGeneratedModelCategory}, with set of generating (acyclic) cofibrations the sets $I_{Top}^{\mathcal{C}}$, $J_{Top}^{\mathcal{C}}$ and $I_{Top^{\ast/}}^{\mathcal{C}}$, $J_{Top^{\ast/}}^{\mathcal{C}}$ from def. \ref{GeneratingCofibrationsForProjectiveStructureOnFunctors}, respectively.

=--

([Piacenza 91, theorem 5.4](classical+model+structure+on+topological+spaces#Piacenza91))

+-- {: .proof}
###### Proof

By prop. \ref{TopologicallyEnrichedCopresheavesHaveAllLimitsAndColimits} the category has all limits and colimits, hence it remains to check the model structure.

But via the enriched Yoneda lemma (prop. \ref{TopologicallyEnrichedYonedaLemma}) it follows that proving the model structure reduces objectwise to the proof of theorem \ref{TopQuillenModelStructure}, theorem \ref{ClassicalModelStructureOnCompactlyGeneratedTopologicalSpaces}.
In particular, the technical lemmas \ref{CompactSubsetsAreSmallInCellComplexes}, \ref{JTopRelativeCellComplexesAreWeakHomotopyEquivalences} and \ref{AcyclicSerreFibrationsAreTheJTopFibrations} generalize immediately to the present situation, with the evident small change of wording:

For instance, the fact that a morphism of topologically enriched functors $\eta \colon F \to G$ that has the right lifting property against the elements of $I_{Top}^{\mathcal{C}}$ is a projective weak equivalence, follows by noticing that for fixed $\eta \colon F \to G$ the [[enriched Yoneda lemma]] prop. \ref{TopologicallyEnrichedYonedaLemma} gives a [[natural bijection]] of commuting diagrams (and their fillers) of the form

$$
  \left(
  \;\;\;
  \array{
    y(c) \cdot S^{n-1} &\longrightarrow& F
    \\
    {}^{\mathllap{(id\cdot \iota_n)}}\downarrow && \downarrow^{\mathrlap{\eta}}
    \\
    y(c) \cdot D^n &\longrightarrow& G
  }
  \;\;\;
  \right)
  \;\;\;\;\;\leftrightarrow\;\;\;\;\;
  \left(  
  \;\;\;
  \array{
     S^{n-1} &\longrightarrow& F(c)
     \\
     \downarrow && \downarrow^{\mathrlap{\eta_c}}
     \\
     D^n &\longrightarrow& G(c)
  }
  \;\;\;
  \right)
  \,,
$$

and hence the statement follows with part (A) of the proof of lemma \ref{AcyclicSerreFibrationsAreTheJTopFibrations}.

With these three lemmas in hand, the remaining formal part of the proof goes through verbatim as [above](#VerificationOfTopQuillen): repeatedly use the [[small object argument]] (prop. \ref{SmallObjectArgument}) and the [[retract argument]] (prop. \ref{RetractArgument}) to establish the two [[weak factorization systems]]. (While again the structure of a [[category with weak equivalences]] is evident.)

=--

+-- {: .num_example #PreExcisiveFunctors}
###### Example

Given examples \ref{TopkAsATopologicallyEnrichedCategory} and \ref{TopologicallyEnrichedFunctorsToTopk}, the next evident example of a pointed [[topologically enriched category]] besides $Top^{\ast/}_{cg}$ itself is the functor category

$$
  [Top_{cg}^{\ast/}, Top_{cg}^{\ast/}]
  \,.
$$

The only technical problem with this is that $Top^{\ast/}_{cg}$ is not a [[small category]] (it has a [[proper class]] of objects), which means that the existence of all limits and colimits via prop. \ref{TopologicallyEnrichedCopresheavesHaveAllLimitsAndColimits} may (and does) fail.

But so we just restrict to a small topologically enriched subcategory. A good choice is the [[full subcategory]]

$$
  Top^{\ast/}_{cg,fin} \hookrightarrow Top^{\ast/}_{cg}
$$

of topological spaces homoemorphic to [[finite CW-complexes]]. The resulting projective model category (via theorem \ref{ProjectiveModelStructureOnTopologicalFunctors})

$$
  [Top_{cg,fin}^{\ast/}\;,\; (Top^{\ast/}_{cg})_{Quillen}]_{proj}
$$

is also also known as the **strict [[model structure for excisive functors]]**. (This terminology is the special case for $n = 1$ of the terminology "[[n-excisive functors]]" as used in "[[Goodwillie calculus]]", a homotopy-theoretic analog of [[differential calculus]].)  After enlarging its class of weak equivalences while keeping the cofibrations fixed, this will become [[Quillen equivalence|Quillen equivalent]] to a [[model structure for spectra]]. This we discuss in [[Introduction to Stable homotopy theory -- 1-2|part 1.2]], in the section [on pre-excisive functors](Introduction+to+Stable+homotopy+theory+--+1-2#OnPreExcisiveFunctors).

=--


One consequence of theorem \ref{ProjectiveModelStructureOnTopologicalFunctors} is the model category theoretic incarnation of the theory of _[[homotopy colimits]]_.

Observe that ordinary [[limits]] and [[colimits]] (def. \ref{LimitsAndColimits}) are equivalently characterized in terms of [[adjoint functors]]:

Let $\mathcal{C}$ be any [[category]] and let $I$ be a [[small category]]. Write $[I,\mathcal{C}]$ for the corresponding [[functor category]]. We may think of its objects as $I$-shaped [[diagrams]] in $\mathcal{C}$, and of its morphisms as homomorphisms of these diagrams.  There is a canonical functor

$$
  const_I
  \;\colon\;
  \mathcal{C} \overset{}{\longrightarrow} [I,\mathcal{C}]
$$

which sends each object of $\mathcal{C}$ to the diagram that is constant on this object. Inspection of the definition of the [[universal properties]] of [[limits]] and [[colimits]] on one hand, and of [[left adjoint]] and [[right adjoint]] functors on the other hand, shows that

1. precisely when $\mathcal{C}$ has all [[colimits]] of shape $I$, then the functor $const_I$ has a [[left adjoint]] functor, which is the operation of forming these colimits:

   $$
     [I,\mathcal{C}]
       \underoverset
        {\underset{const_I}{\longleftarrow}}
        {\overset{\underset{\longrightarrow}{\lim}_I}{\longrightarrow}}
        {\bot}
     \mathcal{C}
   $$

1. precisely when $\mathcal{C}$ has all [[limits]] of shape $I$, then the functor $const_I$ has a [[right adjoint]] functor, which is the operation of forming these limits.

   $$
     [I,\mathcal{C}]
       \underoverset
        {\underset{\underset{\longleftarrow}{\lim}_I}{\longrightarrow}}
        {\overset{const_I}{\longleftarrow}}
        {\bot}
     \mathcal{C}
   $$

+-- {: .num_prop #ColimitIsLeftQuillenOfProjectiveModelStructureOnFunctors}
###### Proposition

Let $I$ be a [[small category|small]] [[topologically enriched category]] (def. \ref{TopEnrichedCategory}). Then the $(\underset{\longrightarrow}{\lim}_I \dashv const_I)$-[[adjunction]]

$$
  [I,(Top_{cg})_{Quillen}]_{proj}
    \underoverset
      {\underset{const_I}{\longleftarrow}}
      {\overset{\underset{\longrightarrow}{\lim}_I}{\longrightarrow}}
      {\bot}
  (Top_{cg})_{Quillen}
$$

is a [[Quillen adjunction]] (def. \ref{QuillenAdjunction}) between the [[projective model structure on enriched functors|projective model structure on topological functors]] on $I$, from theorem \ref{ProjectiveModelStructureOnTopologicalFunctors}, and the [[classical model structure on topological spaces]] from theorem \ref{ClassicalModelStructureOnCompactlyGeneratedTopologicalSpaces}.

Similarly, if $I$ is [[enriched category|enriched]] in [[pointed topological spaces]], then for the [[classical model structure on pointed topological spaces]] (prop. \ref{ModelStructureOnSliceCategory}, theorem
\ref{CofibrantGenerationOfPointedTopologicalSpaces}) the adjunction

$$
  [I,(Top^{\ast/}_{cg})_{Quillen}]_{proj}
    \underoverset
      {\underset{const}{\longleftarrow}}
      {\overset{\underset{\longrightarrow}{\lim}}{\longrightarrow}}
      {\bot}
  (Top^{\ast/}_{cg})_{Quillen}
$$

is a Quillen adjunction.


=--

+-- {: .proof}
###### Proof

Since the fibrations and weak equivalences in the projective model structure (def. \ref{ClassesOfMorphismsInTheProjectiveModelStructureOnTopEnrichedFunctors}) on the functor category are objectwise those of $(Top_{cg})_{Quillen}$ and of $(Top^{\ast/}_{cg})_{Quillen}$, respectively, it is immediate that the functor $const_I$ preserves these. In particular it preserves fibrations and acyclic fibrations and so the claim follows (prop. \ref{ConditionsOnQuillenAdjunctionAreIndeedEquivalent}).

=--


+-- {: .num_defn #LeftDerivedFunctorOfColimitFunctor}
###### Definition

In the situation of prop. \ref{ColimitIsLeftQuillenOfProjectiveModelStructureOnFunctors} we say that the [[left derived functor]] (def. \ref{LeftAndRightDerivedFunctorsOnModelCategories}) of the [[colimit]] functor is the **[[homotopy colimit]]**

$$
  hocolim_I
    \coloneqq
  \mathbb{L}\underset{\longrightarrow}{\lim}_I
    \;\colon\;
  Ho([I,Top])
    \longrightarrow
  Ho(Top)
$$

and

$$
  hocolim_I
    \coloneqq
  \mathbb{L}\underset{\longrightarrow}{\lim}_I
    \;\colon\;
  Ho([I,Top^{\ast/}])
    \longrightarrow
  Ho(Top^{\ast/})
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

Since every object in $(Top_{cg})_{Quillen}$ and in $(Top^{\ast/}_{cg})_{Quillen}$  is fibrant, the [[homotopy colimit]] of any diagram $X_\bullet$, according to def. \ref{LeftDerivedFunctorOfColimitFunctor}, is (up to [[weak homotopy equivalence]]) the result of forming the ordinary [[colimit]] of any [[projectively cofibrant diagram|projectively cofibrant]] replacement $\hat X_\bullet \overset{\in W_{proj}}{\to} X_\bullet$.

=--

+-- {: .num_example #ProjectiveModelStructureOnNSequencesOfTopologicalSpaces}
###### Example

Write $\mathbb{N}^{\leq}$ for the [[poset]] (def. \ref{PosetsWosetTosetsAndOrdinals}) of [[natural numbers]], hence for the [[small category]] (with at most one morphism from any given object to any other given object) that looks like

$$
  \mathbb{N}^{\leq}
  =
  \left\{
    0 \to 1 \to 2 \to 3 \to \cdots
  \right\}
  \,.
$$

Regard this as a [[topologically enriched category]] with the, necessarily, [[discrete topological space|discrete topology]] on its [[hom-sets]].

Then a [[topologically enriched functor]]

$$
  X_\bullet
    \;\colon\;
  \mathbb{N}^{\leq}
    \longrightarrow
  Top_{cg}
$$

is just a plain functor and is equivalently a sequence of [[continuous functions]] (morphisms in $Top_{cg}$) of the form (also called a _[[cotower]]_)

$$
 X_0
   \overset{f_0}{\longrightarrow}
 X_1
   \overset{f_1}{\longrightarrow}
 X_2
   \overset{f_2}{\longrightarrow}
 X_3
   \longrightarrow
 \cdots
 \,.
$$

It is immediate to check that those sequences $X_\bullet$ which are cofibrant in the projective model structure (theorem \ref{ProjectiveModelStructureOnTopologicalFunctors}) are precisely those for which

1. all component morphisms $f_i$ are cofibrations in $(Top_{cg})_{Quillen}$ or $(Top^{\ast/}_{cg})_{Quillen}$, respectively, hence [[retracts]] (remark \ref{RetractsOfMorphisms}) of [[relative cell complex]] inclusions (def. \ref{TopologicalCellComplex});

1. the object $X_0$, and hence all other objects, are cofibrant, hence are [[retracts]] of [[cell complexes]] (def. \ref{TopologicalCellComplex}).

=--

By example \ref{ProjectiveModelStructureOnNSequencesOfTopologicalSpaces} it is immediate that the operation of forming colimits sends projective (acyclic) cofibrations between sequences of topological spaces to (acyclic) cofibrations in the [[classical model structure on pointed topological spaces]]. On those projectively cofibrant sequences where every map is not just a [[retract]] of a [[relative cell complex]] inclusion, but a plain relative cell complex inclusion, more is true:


+-- {: .num_prop #PropertiesOfColimitOverSequencesOfRelativeCellComplexes}
###### Proposition

In the [[projective model structure on functors|projective model structures]] on [[cotowers]] in topological spaces, $[\mathbb{N}^{\leq}, (Top_{cg})_{Quillen}]_{proj}$ and $[\mathbb{N}^{\leq}, (Top^{\ast/}_{cg})_{Quillen}]_{proj}$ from def. \ref{ProjectiveModelStructureOnNSequencesOfTopologicalSpaces}, the following holds:

1. The [[colimit]] functor preserves fibrations between sequences of [[relative cell complex]] inclusions;

1. Let $I$ be a [[finite category]], let $D_\bullet(-) \colon I \to [\mathbb{N}^{\leq}, Top_{cg}]$ be a finite [[diagram]] of sequences of relative cell complexes. Then there is a [[weak homotopy equivalence]]

   $$
     \underset{\longrightarrow}{\lim}_{n}
      \left(
        \underset{\longleftarrow}{\lim}_i
        D_n(i)
      \right)
       \overset{\in W_{cl}}{\longrightarrow}
     \underset{\longleftarrow}{\lim}_i
      \left(
        \underset{\longrightarrow}{\lim}_{n}
        D_n(i)
      \right)
   $$

   from the colimit over the limit sequnce to the limit of the colimits of sequences.

=--

+-- {: .proof}
###### Proof

Regarding the first statement:

Use that both $(Top_{cg})_{Quillen}$ and $(Top^{\ast/}_{cg})_{Quillen}$ are [[cofibrantly generated model categories]] (theorem \ref{CofibrantGenerationOfPointedTopologicalSpaces}) whose generating acyclic cofibrations have [[compact topological spaces]] as [[domains]] and [[codomains]]. The colimit over a sequence of relative cell complexes (being a [[transfinite composition]]) yields another [[relative cell complex]], and hence lemma \ref{CompactSubsetsAreSmallInCellComplexes} says that every morphism out of the domain or codomain of a generating acyclic cofibration into this colimit factors through a finite stage inclusion. Since a projective fibration is a degreewise fibration, we have the [[lifting property]] at that finite stage, and hence also the lifting property against the morphisms of colimits.

Regarding the second statement:

This is a model category theoretic version of a standard fact of plain [[category theory]], which says that in the category [[Set]] of sets, [filtered colimits commute with finite limits](commutativity+of+limits+and+colimits#FilteredColimitsCommuteWithFiniteLimits) in that there is an isomorphism of sets of the form which we have to prove is a weak homotopy equivalence of topological spaces. But now using that weak homotopy equivalences are detected by forming [[homotopy groups]] (def. \ref{HomotopyGroupsOftopologicalSpaces}), hence [[hom-sets]] out of [[n-spheres]], and since $n$-[[spheres]] are [[compact topological spaces]], lemma \ref{CompactSubsetsAreSmallInCellComplexes} says that homming out of $n$-spheres commutes over the colimits in question. Moreover, generally homming out of anything commutes over [[limits]], in particular [[finite limits]] (every [[hom functor]] is [[left exact functor]] in the second variable). Therefore we find isomorphisms of the form

$$
  Hom\left(
    S^q,
    \underset{\longrightarrow}{\lim}_{n}
      \left(
        \underset{\longleftarrow}{\lim}_i
        D_n(i)
      \right)
  \right)
  \simeq
    \underset{\longrightarrow}{\lim}_{n}
      \left(
        \underset{\longleftarrow}{\lim}_i
        Hom\left(S^q, D_n(i)\right)
      \right)
   \overset{\sim}{\longrightarrow}
    \underset{\longleftarrow}{\lim}_i
      \left(
        \underset{\longrightarrow}{\lim}_{n}
        Hom\left(S^q D_n(i)\right)
      \right)
   \simeq
    Hom\left(
     S^q,
    \underset{\longleftarrow}{\lim}_i
      \left(
        \underset{\longrightarrow}{\lim}_{n}
          D_n(i)
      \right)
   \right)
$$

and similarly for the [[left homotopies]] $Hom(S^q \times I,-)$ (and similarly for the pointed case). This implies the claimed isomorphism on homotopy groups.

=--




## Homotopy fiber sequences
 {#HomotopyFiberSequences}

A key aspect of [[homotopy theory]] is that the [[universal constructions]] of [[category theory]], such as [[limits]] and [[colimits]], receive a refinement whereby their [[universal properties]] hold not just up to [[isomorphism]] but up to ([[weak homotopy equivalence|weak]]) [[homotopy equivalence]]. One speaks of _[[homotopy limits]]_ and _[[homotopy colimits]]_.

We consider this here just for the special case of [[homotopy fibers]] and [[homotopy cofibers]], leading to the phenomenon of [[homotopy fiber sequences]] and their induced [[long exact sequences of homotopy groups]] which control much of the theory to follow.





### Mapping cones
 {#MappingCones}


In the context of [[homotopy theory]], a [[pullback]] diagram, such as in the definition of the [[fiber]] in example \ref{FiberAndCofiberInPointedObjects}

$$
  \array{
     fib(f) &\longrightarrow& X
     \\
     \downarrow && \downarrow^{\mathrlap{f}}
     \\
     \ast &\longrightarrow& Y
  }
$$

ought to [[commuting diagram|commute]] only up to a (left/right) [[homotopy]] (def. \ref{LeftAndRightHomotopyInAModelCategory}) between the outer composite morphisms. Moreover, it should satisfy its [[universal property]] up to such homotopies.

Instead of going through the full theory of what this means, we observe that this is plausibly modeled by the following construction, and then we check ([below](#HomotopyFibers)) that this indeed has the relevant abstract homotopy theoretic properties.


+-- {: .num_defn #MappingConeAndMappingCocone}
###### Definition

Let $\mathcal{C}$ be a [[model category]], def. \ref{ModelCategory} with $\mathcal{C}^{\ast/}$ its model structure on pointed objects, prop. \ref{ModelStructureOnSliceCategory}.
For $f \colon X \longrightarrow Y$ a morphism between cofibrant objects (hence a morphism in $(\mathcal{C}^{\ast/})_c\hookrightarrow \mathcal{C}^{\ast/}$, def. \ref{FullSubcategoriesOfFibrantCofibrantObjects}), its **reduced [[mapping cone]]** is the object

$$
  Cone(f)
  \coloneqq
  \ast \underset{X}{\sqcup} Cyl(X) \underset{X}{\sqcup} Y
$$

in the colimiting diagram

$$
  \array{
    && X &\stackrel{f}{\longrightarrow}& Y
    \\
    && \downarrow^{\mathrlap{i_1}} && \downarrow^{\mathrlap{i}}
    \\
    X &\stackrel{i_0}{\longrightarrow}& Cyl(X)
    \\
    \downarrow && & \searrow^{\mathrlap{\eta}} & \downarrow
    \\
    {*} &\longrightarrow& &\longrightarrow& Cone(f)
  }
  \,,
$$

where $Cyl(X)$ is a [[cylinder object]] for $X$, def. \ref{PathAndCylinderObjectsInAModelCategory}.

Dually, for $f \colon X \longrightarrow Y$ a morphism between fibrant objects (hence a morphism in $(\mathcal{C}^{\ast})_f\hookrightarrow \mathcal{C}^{\ast/}$, def. \ref{FullSubcategoriesOfFibrantCofibrantObjects}), its **[[mapping cocone]]** is the object

$$
  Path_\ast(f) \coloneqq \ast \underset{Y}{\times} Path(Y)\underset{Y}{\times} Y
$$

in the following limit diagram

$$
  \array{
    Path_\ast(f) &\longrightarrow& &\longrightarrow& X
    \\
    \downarrow &\searrow^{\mathrlap{\eta}}& && \downarrow^{\mathrlap{f}}
    \\
      &&  Path(Y) &\underset{p_1}{\longrightarrow}& Y
    \\
    \downarrow && \downarrow^{\mathrlap{p_0}}
    \\
    \ast &\longrightarrow& Y
  }
  \,,
$$

where $Path(Y)$ is a [[path space object]] for $Y$, def. \ref{PathAndCylinderObjectsInAModelCategory}.


=--

+-- {: .num_remark }
###### Remark

When we write homotopies (def. \ref{LeftAndRightHomotopyInAModelCategory}) as double arrows between morphisms, then the limit diagram in def. \ref{MappingConeAndMappingCocone} looks just like the square in the definition of [[fibers]] in example \ref{FiberAndCofiberInPointedObjects}, except that it is filled by the [[right homotopy]] given by the component map denoted $\eta$:

$$
  \array{
    Path_\ast(f) &\longrightarrow& X
    \\
    \downarrow &\swArrow_{\eta}& \downarrow^{\mathrlap{f}}
    \\
    \ast &\longrightarrow& Y
  }
  \,.
$$

Dually, the colimiting diagram for the mapping cone turns to look just like the square for the [[cofiber]], except that it is filled with a [[left homotopy]]

$$
  \array{
    X &\overset{f}{\longrightarrow}& Y
    \\
    \downarrow &\swArrow_{\eta}& \downarrow
    \\
    \ast &\longrightarrow& Cone(f)
  }
$$

=--


+-- {: .num_prop #ConeAndMappingCylinder}
###### Proposition

The colimit appearing in the definition of the reduced [[mapping cone]] in def. \ref{MappingConeAndMappingCocone} is equivalent to three consecutive [[pushouts]]:

$$
  \array{
    && X &\stackrel{f}{\longrightarrow}& Y
    \\
    && \downarrow^{\mathrlap{i_1}} &(po)& \downarrow^{\mathrlap{i}}
    \\
    X &\stackrel{i_0}{\longrightarrow}& Cyl(X) &\longrightarrow& Cyl(f)
    \\
    \downarrow &(po)& \downarrow & (po) & \downarrow
    \\
    {*} &\longrightarrow& Cone(X) &\longrightarrow& Cone(f)
  }
  \,.
$$

The two intermediate objects appearing here are called

* the plain **reduced [[cone]]**  $Cone(X) \coloneqq \ast \underset{X}{\sqcup} Cyl(X)$;

* the **reduced [[mapping cylinder]]** $Cyl(f) \coloneqq Cyl(X) \underset{X}{\sqcup} Y$.

Dually, the limit appearing in the definition of the [[mapping cocone]] in def. \ref{MappingConeAndMappingCocone} is equivalent to three consecutive [[pullbacks]]:

$$
  \array{
    Path_\ast(f) &\longrightarrow& Path(f) &\longrightarrow& X
    \\
    \downarrow &(pb)& \downarrow &(pb)& \downarrow^{\mathrlap{f}}
    \\
    Path_\ast(Y)  &\longrightarrow&  Path(Y) &\underset{p_1}{\longrightarrow}& Y
    \\
    \downarrow &(pb)& \downarrow^{\mathrlap{p_0}}
    \\
    \ast &\longrightarrow& Y
  }
  \,.
$$

The two intermediate objects appearing here are called

* the **based path space object** $Path_\ast(Y) \coloneqq \ast \underset{Y}{\prod} Path(Y)$;

* the **mapping path space** or **mapping co-cylinder** $Path(f) \coloneqq X \underset{Y}{\times} Path(X)$.

=--


+-- {: .num_defn #SuspensionAndLoopSpaceObject}
###### Definition

Let $X \in \mathcal{C}^{\ast/}$ be any [[pointed object]].

1. The [[mapping cone]], def. \ref{ConeAndMappingCylinder}, of $X \to \ast$ is called the  **[[reduced suspension|reduced]] [[suspension]]** of $X$, denoted

   $$
     \Sigma X = Cone(X\to\ast)\,.
   $$

   Via prop. \ref{ConeAndMappingCylinder} this is equivalently the coproduct of two copies of the cone on $X$ over their base:

   $$
     \array{
       && X &\stackrel{}{\longrightarrow}& \ast
       \\
       && \downarrow^{\mathrlap{i_1}} &(po)& \downarrow^{\mathrlap{}}
       \\
       X &\stackrel{i_0}{\longrightarrow}& Cyl(X) &\longrightarrow& Cone(X)
       \\
       \downarrow &(po)& \downarrow & (po) & \downarrow
       \\
       {*} &\longrightarrow& Cone(X) &\longrightarrow& \Sigma X
     }
     \,.
   $$

   This is also equivalently the [[cofiber]], example \ref{FiberAndCofiberInPointedObjects} of $(i_0,i_1)$, hence (example \ref{WedgeSumAsCoproduct}) of the [[wedge sum]] inclusion:

   $$
     X \vee X
      =
     X \sqcup X
      \overset{(i_0,i_1)}{\longrightarrow}
     Cyl(X)
       \overset{cofib(i_0,i_1)}{\longrightarrow}
     \Sigma X
     \,.
   $$


1. The [[mapping cocone]], def. \ref{ConeAndMappingCylinder}, of $\ast \to X$ is called the **[[loop space object]]** of $X$, denoted

   $$
     \Omega X = Path_\ast(\ast \to X)
     \,.
   $$

   Via prop. \ref{ConeAndMappingCylinder} this is equivalently

   $$
     \array{
       \Omega X &\longrightarrow& Path_\ast(X) &\longrightarrow& \ast
       \\
       \downarrow &(pb)& \downarrow &(pb)& \downarrow^{}
       \\
       Path_\ast(X)  &\longrightarrow&  Path(X) &\underset{p_1}{\longrightarrow}& X
       \\
       \downarrow &(pb)& \downarrow^{\mathrlap{p_0}}
       \\
       \ast &\longrightarrow& X
     }
     \,.
   $$

   This is also equivalently the [[fiber]], example \ref{FiberAndCofiberInPointedObjects} of $(p_0,p_1)$:

   $$
     \Omega X
     \overset{fib(p_0,p_1)}{\longrightarrow}
     Path(X) \overset{(p_0,p_1)}{\longrightarrow} X \times X
     \,.
   $$

=--

+-- {: .num_prop #ReducedSuspensionBySmashProductWithCircle}
###### Proposition

In [[pointed topological spaces]] $Top^{\ast/}$,

* the [[reduced suspension]] objects (def. \ref{SuspensionAndLoopSpaceObject}) induced from the standard [[reduced cylinder]] $(-)\wedge (I_+)$ of example \ref{StandardReducedCyclinderInTop} are isomorphic to the [[smash product]] (def. \ref{SmashProductOfPointedObjects}) with the [[1-sphere]], for later purposes we choose to smash **on the left** and write

  $$
    cofib(X \vee X \to X \wedge (I_+)) \simeq S^1 \wedge X
    \,,
  $$

Dually:

* the [[loop space objects]] (def. \ref{SuspensionAndLoopSpaceObject}) induced from the standard pointed path space object $Maps(I_+,-)_\ast$ are isomorphic to the [[pointed mapping space]] (example \ref{PointedMappingSpace})  with the [[1-sphere]]

  $$
    fib(Maps(I_+,X)_\ast \to X \times X)
      \simeq
    Maps(S^1, X)_\ast
    \,.
  $$


=--

+-- {: .proof}
###### Proof

By immediate inspection: For instance the [[fiber]] of $Maps(I_+,X)_\ast \longrightarrow X\times X$ is clearly the subspace of the unpointed mapping space $X^I$ on elements that take the endpoints of $I$ to the basepoint of $X$.

=--



+-- {: .num_example #MappingConesInTopologicalSpaces}
###### Example

<div style="float:right;margin:0 10px 10px 0;">
<img src="http://ncatlab.org/nlab/files/mappingcone.jpg" width="560" >
</div>

For $\mathcal{C} =$ [[Top]] with $Cyl(X) = X\times I$ the standard cyclinder object, def. \ref{TopologicalInterval}, then by example \ref{PushoutInTop}, the [[mapping cone]], def. \ref{MappingConeAndMappingCocone}, of a [[continuous function]] $f \colon X \longrightarrow Y$ is obtained by

1. forming the cylinder over $X$;

1. attaching to one end of that cylinder the space $Y$ as specified by the map $f$.

1. shrinking the other end of the cylinder to the point.

Accordingly the [[suspension]] of a topological space is the result of shrinking both ends of the cylinder on the object two the point. This is homeomoprhic to attaching two copies of the cone on the space at the base of the cone.

(graphics taken from [Muro 2010](#Muro10))

Below in example \ref{StandardTopologicalMappingConeIsHomotopyCofiber} we find the homotopy-theoretic interpretation of this standard topological mapping cone as a model for the _[[homotopy cofiber]]_.

=--

+-- {: .num_remark #UnreducedCone}
###### Remark

The _formula_ for the [[mapping cone]] in prop. \ref{ConeAndMappingCylinder} (as opposed to that of the mapping co-cone) does not require the presence of the basepoint: for $f \colon X \longrightarrow Y$ a morphism in $\mathcal{C}$ (as opposed to in $\mathcal{C}^{\ast/}$) we may still define

$$
  Cone'(f) \coloneqq Y \underset{X}{\sqcup} Cone'(X)
  \,,
$$

where the prime denotes the _unreduced cone_, formed from a cylinder object in $\mathcal{C}$.


=--

+-- {: .num_prop #UnreducedMappingConeAsReducedConeOfBasedPointAdjoined}
###### Proposition

For $f \colon X \longrightarrow Y$ a morphism in [[Top]], then its unreduced mapping cone, remark \ref{UnreducedCone}, with respect to the standard cylinder object $X \times I$ def. \ref{TopologicalInterval}, is isomorphic to the reduced mapping cone, def. \ref{MappingConeAndMappingCocone}, of the morphism $f_+ \colon X_+ \to Y_+$ (with a basepoint adjoined, def. \ref{BasePointAdjoined}) with respect to the standard [[reduced cylinder]] (example \ref{StandardReducedCyclinderInTop}):

$$
  Cone'(f) \simeq Cone(f_+)
  \,.
$$

=--

+-- {: .proof}
###### Proof

By prop. \ref{LimitsAndColimitsOfPointedObjects} and example \ref{WedgeAndSmashOfBasePointAdjoinedTopologicalSpaces}, $Cone(f_+)$ is given by the colimit in $Top$ over the following diagram:

$$
  \array{
    \ast &\longrightarrow& X \sqcup \ast &\overset{(f,id)}{\longrightarrow}& Y \sqcup \ast
    \\
    \downarrow && \downarrow && \downarrow
    \\
    X \sqcup\ast &\longrightarrow& (X \times I) \sqcup \ast
    \\
    \downarrow && && \downarrow
    \\
    \ast &\longrightarrow& &\longrightarrow& Cone(f_+)
  }
  \,.
$$

We may factor the vertical maps to give

$$
  \array{
    \ast &\longrightarrow& X \sqcup \ast &\overset{(f,id)}{\longrightarrow}& Y \sqcup \ast
    \\
    \downarrow && \downarrow && \downarrow
    \\
    X \sqcup\ast &\longrightarrow& (X \times I) \sqcup \ast
    \\
    \downarrow && && \downarrow
    \\
    \ast \sqcup \ast &\longrightarrow& &\longrightarrow& Cone'(f)_+
    \\
    \downarrow && && \downarrow
    \\
    \ast &\longrightarrow& &\longrightarrow& Cone'(f)
  }
  \,.
$$



This way the top part of the diagram (using the [[pasting law]] to compute the colimit in two stages) is manifestly a cocone under the result of applying $(-)_+$ to the diagram for the unreduced cone. Since $(-)_+$ is itself given by a colimit, it preserves colimits, and hence gives the partial colimit $Cone'(f)_+$ as shown. The remaining pushout then contracts the remaining copy of the point away.

=--


Example \ref{MappingConesInTopologicalSpaces} makes it clear that every [[cycle]] $S^n \to Y$ in $Y$ that happens to be in the image of $X$ can be _continuously_ translated in the cylinder-direction, keeping it constant in $Y$, to the other end of the cylinder, where it shrinks away to the point. This means that every [[homotopy group]] of $Y$, def. \ref{HomotopyGroupsOftopologicalSpaces}, in the image of $f$ vanishes in the mapping cone. Hence in the mapping cone **the image of $X$ under $f$ in $Y$ is removed up to homotopy**. This makes it intuitively clear how $Cone(f)$ is a homotopy-version of the [[cokernel]] of $f$. We now discuss this formally.


+-- {: .num_lemma #FactorizationLemma}
###### Lemma
**([[factorization lemma]])**

Let $\mathcal{C}_c$ be a [[category of cofibrant objects]],  def. \ref{FullSubcategoriesOfFibrantCofibrantObjects}. Then for every morphism $f \colon X \longrightarrow Y$ the [[mapping cylinder]]-construction in def. \ref{ConeAndMappingCylinder} provides a cofibration resolution of $f$, in that

1. the composite morphism $X \overset{i_0}{\longrightarrow} Cyl(X) \overset{(i_1)_\ast f}{\longrightarrow} Cyl(f)$ is a cofibration;

1. $f$ factors through this morphism by a weak equivalence left inverse to an acyclic cofibration

   $$
     f
       \;\colon\;
     X
        \underoverset{\in Cof}{(i_1)_\ast f\circ i_0}{\longrightarrow}
     Cyl(f)
       \underset{\in W}{\longrightarrow}
     Y
     \,,
   $$

Dually:

Let $\mathcal{C}_f$ be a [[category of fibrant objects]],  def. \ref{FullSubcategoriesOfFibrantCofibrantObjects}. Then for every morphism $f \colon X \longrightarrow Y$ the [[mapping cocylinder]]-construction in def. \ref{ConeAndMappingCylinder} provides a fibration resolution of $f$, in that

1. the composite morphism $Path(f) \overset{p_1^\ast f}{\longrightarrow} Path(Y) \overset{p_0}{\longrightarrow} Y$ is a fibration;

1. $f$ factors through this morphism by a weak equivalence right inverse to an acyclic fibration:

   $$
     f
       \;\colon\;
     X
       \underset{\in W}{\longrightarrow}
     Path(f)
        \underoverset{\in Fib}{p_0 \circ p_1^\ast f}{\longrightarrow}
     Y
     \,,
   $$

=--

+-- {: .proof #ProofOfFactorizationLemma}
###### Proof

We discuss the second case. The first case is [[formal dual|formally dual]].

So consider the [[mapping cocylinder]]-construction from prop. \ref{ConeAndMappingCylinder}

\[
  \label{ConstructionOfFactorizationInFactorizationLemma}
  \array{
     Path(f) &\overset{\in W \cap Fib}{\longrightarrow}& X
     \\
     {}^{\mathllap{p_1^\ast f}}\downarrow &(pb)& \downarrow^{\mathrlap{f}}
     \\
     Path(Y) &\underoverset{\in W \cap Fib}{p_1}{\longrightarrow}& Y
     \\
     {}^{\mathllap{\in W \cap Fib}}\downarrow^{\mathrlap{p_0}}
     \\
     Y
  }
  \,.
\]


To see that the vertical composite is indeed a fibration, notice that, by the [[pasting law]], the above pullback diagram may be decomposed as a [[pasting]] of two pullback diagram as follows

$$
  \array{
    Path(f)
     &\underoverset{\in Fib}{(f,id)^\ast(p_1,p_0)}{\longrightarrow}&
     X \times Y
     &\stackrel{pr_1}{\to}&
     X
     \\
     \downarrow && \downarrow^{\mathrlap{(f, Id)}} && \downarrow^\mathrlap{f}
     \\
     Path(Y) &\overset{(p_1,p_0) \in Fib }{\longrightarrow}&
     Y \times Y &\stackrel{pr_1}{\longrightarrow}&
     Y
     \\
     {}^{\mathllap{p_0}}\downarrow & \swarrow_{\mathrlap{pr_2 \atop {\in Fib}}}
     \\
     Y
  }
  \,.
$$

Both squares are pullback squares. Since pullbacks of fibrations are fibrations by prop. \ref{ClosurePropertiesOfInjectiveAndProjectiveMorphisms}, the morphism $Path(f) \to X \times Y$ is a fibration.
Similarly, since $X$ is fibrant, also the [[projection]] map $X \times Y \to Y$ is a fibration (being the pullback of $X \to \ast$ along $Y \to \ast$).

Since the vertical composite is thereby exhibited as the composite of two fibrations

$$
   Path(f)
     \overset{(f,id)^\ast(p_1,p_0)}{\longrightarrow}
   X \times Y
     \stackrel{pr_2 \circ (f ,Id) = pr_2}{\longrightarrow}
  Y
  \,,
$$

it is itself a fibration.

Then to see that there is a weak equivalence as claimed:

The [[universal property]] of the [[pullback]] $Path(f)$ induces a right inverse of $Path(f) \to X$ fitting into this diagram

$$
  \array{
     id_X \colon & X &\underoverset{\in W}{\exists}{\longrightarrow}
       & Path(f)
       &
         \overset{\in W \cap Fib}{\longrightarrow}&
       X
     \\
     & {}^{\mathrlap{f}}\downarrow && \downarrow && \downarrow^{\mathrlap{f}}
     \\
     id_Y\colon& Y
       &\underoverset{\in W}{i}{\longrightarrow}&
     Path(Y)
       &\stackrel{p_1}{\to}& Y
     \\
     & & {}_{\mathllap{Id}}\searrow& \downarrow^{\mathrlap{p_0}}
     \\
     & && Y
  }
  \,,
$$

which is a weak equivalence, as indicated, by [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}).

This establishes the claim.

=--





### Categories of fibrant objects

[Below](#HomotopyFibers) we discuss the homotopy-theoretic properties of the [[mapping cone]]- and [[mapping cocone]]-constructions from [above](#MappingCones). Before we do so, we here establish a collection of general facts that hold in [[categories of fibrant objects]] and dually in [[categories of cofibrant objects]], def. \ref{FullSubcategoriesOfFibrantCofibrantObjects}.

**Literature** ([Brown 73, section 4](#Brown73)).


+-- {: .num_lemma #ReplacementOfPathObjects}
###### Lemma

Let $f\colon X \longrightarrow Y$ be a morphism in a [[category of fibrant objects]], def. \ref{FullSubcategoriesOfFibrantCofibrantObjects}. Then given any choice of [[path space objects]] $Path(X)$ and $Path(Y)$, def. \ref{PathAndCylinderObjectsInAModelCategory}, there is a replacement of $Path(X)$ by a path space object $\widetilde{Path(X)}$ along an acylic fibration, such that $\widetilde{Path(X)}$ has a morphism $\phi$ to $Path(Y)$ which is compatible with the structure maps, in that the following diagram commutes

$$
  \array{
    && X &\overset{f}{\longrightarrow}& Y
    \\
    &\swarrow& \downarrow && \downarrow
    \\
    Path(X) &\underset{\in W \cap Fib}{\longleftarrow}& \widetilde{Path(X)} &\overset{\phi}{\longrightarrow}& Path(Y)
    \\
    &{}_{\mathllap{(p^X_0,p^X_1)}}\searrow& \downarrow^{\mathrlap{(\tilde p^X_0,\tilde p^X_1)}} && \downarrow^{\mathrlap{(p^Y_0,p^Y_1)}}
    \\
    && X \times X &\overset{(f,f)}{\longrightarrow}& Y \times Y
  }
  \,.
$$

=--

([Brown 73, section 2, lemma 2](#Brown73))

+-- {: .proof}
###### Proof

Consider the [[commuting square]]

$$
  \array{
    X &\overset{f}{\longrightarrow}& Y &\longrightarrow& Path(Y)
    \\
    \downarrow &&  && \downarrow^{\mathrlap{(p_0^Y, p_1^Y)}}
    \\
    Path(X) &\overset{(p^X_0,p^X_1)}{\longrightarrow}& X \times X
    &\overset{(f,f)}{\longrightarrow}& Y \times Y
  }
  \,.
$$

Then consider its factorization  through the [[pullback]] of the right morphism along the bottom morphism,

$$
  \array{
    X &\longrightarrow& (f \circ p_0^X, f\circ p_1^X)^\ast Path(Y) &\longrightarrow& Path(Y)
    \\
    &{}_{\mathllap{\in W}}\searrow& \downarrow^{\mathrlap{\in Fib}} && \downarrow^{\mathrlap{(p_0^Y, p_1^Y)}}_{\mathrlap{\in Fib}}
    \\
    && Path(X) &\overset{(f \circ p_0^X, f\circ p_1^X)}{\longrightarrow}& Y \times Y
  }
  \,.
$$


Finally use the [[factorization lemma]] \ref{FactorizationLemma} to factor the morphism $X \to (f \circ p_0^X, f\circ p_1^X)^\ast Path(Y)$ through a weak equivalence followed by a fibration, the object this factors through serves as the desired path space resolution

$$
  \array{
    X &\overset{\in W}{\longrightarrow}& \widetilde{Path(X)} &\longrightarrow& Path(Y)
    \\
    &{}_{\mathllap{\in W}}\searrow& \downarrow^{\mathrlap{\in W \cap Fib}} && \downarrow^{\mathrlap{(p_0^Y, p_1^Y)}}
    \\
    && Path(X) &\overset{(f \circ p_0^X, f\circ p_1^X)}{\longrightarrow}& Y \times Y
  }
  \,.
$$


=--


+-- {: .num_lemma #BaseChangePreservesFibrationsAndWeakEquivalences}
###### Lemma

In a [[category of fibrant objects]] $\mathcal{C}_f$, def. \ref{FullSubcategoriesOfFibrantCofibrantObjects}, let

$$
 \array{
  A_1 &&\stackrel{f}{\longrightarrow}&& A_2
  \\
  & {}_{\in Fib}\searrow && \swarrow_{\in Fib}
  \\
  && B
 }
$$

be a morphism over  some object $B$ in $\mathcal{C}_f$
and let $u \colon B' \to B$ be any morphism in
$\mathcal{C}_f$. Let

$$
 \array{
  u^*A_1 &&\stackrel{u^* f}{\longrightarrow}&& u^* A_2
  \\
  & {}_{\in Fib}\searrow && \swarrow_{\in Fib}
  \\
  && B'
 }
$$

be the corresponding morphism pulled back along $u$.

Then

* if $f$ is a fibration then also $u^* f$ is a fibration;

* if $f$ is a weak equivalence then also $u^* f$ is a weak equivalence.

=--

([Brown 73, section 4, lemma 1](#Brown73))

+-- {: .num_proof}
###### Proof

For $f \in Fib$ the statement follows from the [[pasting law]] which says that if in

$$
  \array{
    B' \times_B A_1 &\longrightarrow& A_1
    \\
    \;\;\downarrow^{\mathrlap{u^* f \in Fib}}
    && \;\;\downarrow^{\mathrlap{f \in Fib}}
    \\
    B' \times_B A_2 &\longrightarrow& A_2
    \\
    \;\downarrow^{\mathrlap{\in Fib}} && \;\downarrow^{\mathrlap{\in Fib}}
    \\
    B' &\stackrel{u}{\longrightarrow}& B
  }
$$

the bottom and the total square are pullback squares, then so is the top square. The same reasoning applies for $f \in W \cap Fib$.

Now to see the case that $f\in W$:

Consider the [[full subcategory]] $(\mathcal{C}_{/B})_f$ of the [[slice category]] $\mathcal{C}_{/B}$ (def. \ref{SliceCategory}) on its fibrant objects, i.e. the full subcategory of the slice category on the fibrations

$$
  \array{
    X
    \\
    \downarrow^{\mathrlap{p}}_{\mathrlap{\in Fib}}
    \\
    B
  }
$$

into $B$. By factorizing for every such fibration the [[diagonal morphisms]] into the [[fiber product]] $X \underset{B}{\times} X$ through a weak equivalence followed by a fibration, we obtain path space objects $Path_B(X)$ relative to $B$:

$$
  \array{
   (\Delta_X)/B
   \;\colon
    &
    X
      &\overset{\in W}{\longrightarrow}&
    Path_B(X)
      &\overset{\in Fib}{\longrightarrow}&
    X \underset{B}{\times} X
    \\
    & & {}_{\mathllap{\in Fib}}\searrow & \downarrow & \swarrow_{\mathrlap{\in Fib}}
    \\
    & && B
  }
  \,.
$$

With these, the [[factorization lemma]] (lemma \ref{FactorizationLemma}) applies in $(\mathcal{C}_{/B})_f$.

(Notice that for this we do need the restriction of $\mathcal{C}_{/B}$ to the fibrations, because this ensures that the projections $p_i \colon X_1 \times_B X_2 \to X_i$ are still fibrations, which is used in the proof of the factorization lemma ([here](#ProofOfFactorizationLemma)).)

So now given any

$$
  \array{
    X && \underoverset{\in W}{f}{\longrightarrow} && Y
    \\
    & {}_{\mathllap{\in Fib}}\searrow && \swarrow_{\mathrlap{\in Fib}}
    \\
    && B
  }
$$

apply the [[factorization lemma]] in $(\mathcal{C}_{/B})_f$ to factor it as

$$
  \array{
    X
      &\overset{i \in W}{\longrightarrow}&
    Path_B(f)
      &\overset{\in W \cap Fib}{\longrightarrow}& Y
    \\
    & {}_{\mathllap{\in Fib}}\searrow
     &\downarrow&
    \swarrow_{\mathrlap{\in Fib}}
    \\
    && B
  }
  \,.
$$

By the previous discussion it is sufficient now to show that the base change of $i$ to $B'$ is still a weak equivalence. But by the factorization lemma in $(\mathcal{C}_{/B})_f$, the morphism $i$ is right inverse to another acyclic fibration over $B$:

$$
  \array{
    id_X
    \;\colon
    &
    X
      &\overset{i \in W}{\longrightarrow}&
    Path_B(f)
      &\overset{\in W \cap Fib}{\longrightarrow}& X
    \\
    & &
    {}_{\mathllap{\in Fib}}\searrow
     &\downarrow&
    \swarrow_{\mathrlap{\in Fib}}
    \\
    & && B
  }
  \,.
$$

(Notice that if we had applied the factorization lemma just for $\Delta_X$ in $\mathcal{C}_f$ instead of for $(\Delta_X)/B$ in $(\mathcal{C}_{/B})$ then the corresponding triangle on the right would not be guaranteed commute.)

Now we may reason as before: the base change of the top morphism here is exhibited by the following pasting composite of pullbacks:

$$
  \array{
    B' \underset{B}{\times} X
     &\longrightarrow&
    X
    \\
    \downarrow
      &(pb)&
    \downarrow
    \\
    B' \underset{B}{\times} Path_B(f)
      &\longrightarrow&
    Path_B(f)
    \\
    \downarrow
      &(pb)&
    \downarrow^{\mathrlap{\in W \cap Fib}}
    \\
    B' \underset{B}{\times}X
      &\longrightarrow&
    X
    \\
    \downarrow
      &(pb)&
    \downarrow
    \\
    B'
     &\longrightarrow&
    B
  }
  \,.
$$

The acyclic fibration $Path_B(f)$ is preserved by this pullback, as is the identity $id_X \colon X \to Path_B(X)\to X$. Hence the weak equivalence $X \to Path_B(X)$ is preserved by [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}).

=--

\begin{remark}
\label{InCatOfFibrantObjectsProductPreservesEquivalences}
Lemma \ref{BaseChangePreservesFibrationsAndWeakEquivalences} implies in particular that in a category $\mathcal{C}_f$ of fibrant objects, the operation of [[fiber product]] 
$$
  A \times_B (-)
  \;\colon\;
  \mathcal{C}_f/B
  \longrightarrow
  \mathcal{C}_f/B
$$
with a fibration $A \to B$ preserves fibrations and weak equivalences between fibrations. For $B = \ast$ the [[terminal objects]] this means that the plain Cartesian product
$$
  A \times (-)
  \;\colon\;
  \mathcal{C}_f
  \longrightarrow
  \mathcal{C}_f
$$
preserves fibrations and weak equivalences (cf. [Brown 73, p. 431 ](#Brown73)).
\end{remark}

+-- {: .num_lemma #InCfPullbackAlongFibrationPreservesWeakEquivalences}
###### Lemma

In a [[category of fibrant objects]], def. \ref{FullSubcategoriesOfFibrantCofibrantObjects}, the pullback of a weak equivalence along a fibration is again a weak equivalence.

=--

([Brown 73, section 4, lemma 2](#Brown73))


+-- {: .proof}
###### Proof


Let
$u \colon B' \to B$ be a weak equivalence and
$ p \colon E \to B$ be a fibration. We want to show that the
left vertical morphism in the [[pullback]]

$$
  \array{
    E \times_B B' &\longrightarrow& B'
    \\
    \downarrow^{\mathrlap{\Rightarrow \in W} }
    && \;\downarrow^{\mathrlap{\in W}}
    \\
    E &\stackrel{\in Fib}{\longrightarrow}& B
  }
$$

is a weak equivalence.

First of all, using the [[factorization lemma]] \ref{FactorizationLemma}
we may factor $B' \to B$ as

$$
  B'
    \stackrel{\in W}{\longrightarrow}
  Path(u)
   \stackrel{\in W \cap F}{\longrightarrow}
  B
$$

with the first morphism a weak equivalence that is a right inverse to an acyclic fibration and the right one an acyclic fibration.

Then the pullback diagram in question may be decomposed
into two consecutive pullback diagrams

$$
  \array{
    E \times_B B' &\to& B'
    \\
    \downarrow && \downarrow
    \\
    Q &\stackrel{\in Fib}{\to}& Path(u)
    \\
    \;\;\downarrow^{\mathrlap{\in W \cap Fib}}
    && \;\;\downarrow^{\mathrlap{\in W \cap Fib}}
    \\
    E &\stackrel{\in Fib}{\longrightarrow}& B
  }
  \,,
$$

where the morphisms are indicated as fibrations and
acyclic fibrations using the stability of these
under arbitrary pullback.

This means that the proof reduces to proving that weak equivalences
$u : B' \stackrel{\in W}{\to} B$
that are right inverse to some acyclic fibration
$v : B \stackrel{\in W \cap F}{\to} B'$
map to a weak equivalence under pullback along a fibration.

Given such $u$ with right inverse $v$, consider the pullback diagram


$$
  \array{
    & E
    \\
    &
    {}^{\mathllap{{(p,id)}\atop \in W}}\downarrow
    &
      \searrow^{\mathrlap{id}}
    \\
    E_1 \coloneqq
      &
    B \times_{B'} E
      &
    \stackrel{\in W \cap Fib }{\longrightarrow}
      &
    E
    \\
    & \downarrow^{\mathrlap{\in Fib}} && \downarrow^{\mathrlap{p \in Fib }}
    \\
    & &(pb)& B
    \\
    & \downarrow && \downarrow^{\mathrlap{v \in W \cap Fib}}
    \\
    & B &\overset{v \in Fib \cap W}{\longrightarrow}& B'
  }
  \,.
$$

Notice that the indicated universal morphism  $p \times Id \colon E \stackrel{\in W}{\to} E_1$  into the pullback is a weak equivalence by [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}).

The previous lemma \ref{BaseChangePreservesFibrationsAndWeakEquivalences} says that weak equivalences between fibrations over $B$ are themselves preserved by base extension along $u \colon B' \to B$. In total this yields the following diagram


$$
  \array{
    &&
    u^* E = B' \times_B E
      &\longrightarrow &
    E
    \\
    &&
    {}^{\mathllap{ {u^*(p \times Id)} \atop {\in W} }}\downarrow
      &&
    {}^{\mathllap{ {p \times Id} \atop {\in W}  }}\downarrow
     &
    \searrow^{\mathrlap{id}}
    \\
    &&
    u^* E_1
      &\longrightarrow&
    E_1
      &\stackrel{\in W \cap Fib}{\longrightarrow}&
    E
    \\
    &&\downarrow^{\mathrlap{\in Fib}}&&\downarrow^{\mathrlap{\in Fib}}
    && \downarrow^{\mathrlap{p \in Fib}}
    \\
    &&&&&& B
    \\
    &&\downarrow&&\downarrow && \downarrow^{\mathrlap{v \in W \cap Fib}}
    \\
    &&
    B'
      &\stackrel{u}{\longrightarrow}&
    B
      &\stackrel{v \in W \cap Fib}{\longrightarrow}&
    B'
  }
$$

so that with $p \times Id  : E \to E_1$ a weak equivalence also $u^* (p \times Id)$ is a weak equivalence, as indicated.

Notice that $u^* E = B' \times_B E \to E$ is the morphism that we want to show is a weak equivalence. By [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}) for that it is now sufficient to show that $u^* E_1  \to E_1$ is a weak equivalence.

That finally follows now since, by assumption, the total bottom horizontal morphism is the identity. Hence so is the top horizontal morphism. Therefore $u^\ast E_1  \to E_1$ is right inverse to a weak equivalence, hence is a weak equivalence.

=--

+-- {: .num_lemma #UniquenessOfFibersOfQualizedMorphismsInHoC}
###### Lemma

Let $(\mathcal{C}^{\ast/})_f$ be a [[category of fibrant objects]], def. \ref{FullSubcategoriesOfFibrantCofibrantObjects} in a [[slice model structure|model structure on pointed objects]] (prop. \ref{ModelStructureOnSliceCategory}). Given any [[commuting diagram]] in $\mathcal{C}^{}$ of the form

$$
  \array{
    X'_1 &\underoverset{t}{\in W}{\longrightarrow}& X_1 &\stackrel{\overset{f}{\longrightarrow}}{\underset{g}{\longrightarrow}}& X_2
    \\
    && \downarrow^{\mathrlap{p_1}}_{\mathrlap{\in Fib}}
      &&
    \downarrow^{\mathrlap{p_2}}_{\mathrlap{\in Fib}}
    \\
    && B &\overset{u}{\longrightarrow}& C
  }
$$

(meaning: both squares commute and $t$ equalizes $f$ with $g$) then the [[localization]] functor $\gamma \colon (\mathcal{C}^{\ast/})_f \to Ho(\mathcal{C}^{\ast/})$ (def. \ref{FibrantCofibrantReplacementFunctorToHomotopyCategory}, cor \ref{HomotopyCategoryOfSubcategoriesOfModelCategoriesOnGoodObjects}) takes the morphisms $fib(p_1) \stackrel{\longrightarrow}{\longrightarrow} fib(p_2)$ induced by $f$ and $g$ on [[fibers]] (example \ref{FiberAndCofiberInPointedObjects})  to the same morphism, in the homotopy category.

=--

([Brown 73, section 4, lemma 4](#Brown73))

+-- {: .proof}
###### Proof

First consider the pullback of $p_2$ along $u$: this forms the same kind of diagram but with the bottom morphism an identity. Hence it is sufficient to consider this special case.

Consider the [[full subcategory]] $(\mathcal{C}^{\ast/}_{/B})_f$ of the [[slice category]] $\mathcal{C}^{\ast/}_{/B}$ (def. \ref{SliceCategory}) on its fibrant objects, i.e. the full subcategory of the slice category on the fibrations

$$
  \array{
    X
    \\
    \downarrow^{\mathrlap{p}}_{\mathrlap{\in Fib}}
    \\
    B
  }
$$

into $B$. By factorizing for every such fibration the [[diagonal morphisms]] into the [[fiber product]] $X \underset{B}{\times} X$ through a weak equivalence followed by a fibration, we obtain path space objects $Path_B(X)$ relative to $B$:

$$
  \array{
   (\Delta_X)/B
   \;\colon
    &
    X
      &\overset{\in W}{\longrightarrow}&
    Path_B(X)
      &\overset{\in Fib}{\longrightarrow}&
    X \underset{B}{\times} X
    \\
    & & {}_{\mathllap{\in Fib}}\searrow & \downarrow & \swarrow_{\mathrlap{\in Fib}}
    \\
    & && B
  }
  \,.
$$

With these, the [[factorization lemma]] (lemma \ref{FactorizationLemma}) applies in $(\mathcal{C}^{\ast/}_{/B})_f$.

Let then $X\overset{s}{\to}Path_B(X_2)\overset{(p_0,p_1)}{\to} X_2 \times_B X_2$ be a [[path space object]] for $X_2$ in the slice over $B$ and consider the following commuting square

$$
  \array{
    X'_1 &\overset{s f t}{\longrightarrow}& Path_B(X_2)
    \\
    {}^{\mathllap{t}}_{\mathllap{\in W}}\downarrow && \downarrow^{\mathrlap{(p_0,p_1)}}_{\mathrlap{\in Fib}}
    \\
    X_1 &\overset{(f,g)}{\longrightarrow}& X_2\underset{B}{\times} X_2
  }
  \,.
$$

By factoring this through the pullback $(f,g)^\ast(p_0,p_1)$ and then applying the [[factorization lemma]] \ref{FactorizationLemma} and then [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}) to the factoring morphisms, this may be replaced by a commuting square of the same form, where however the left morphism is an acyclic fibration

$$
  \array{
    X''_1 &\overset{}{\longrightarrow}& Path_B(X_2)
    \\
    {}^{\mathllap{t}}_{\mathllap{\in W\cap Fib}} \downarrow && \downarrow^{\mathrlap{(p_0,p_1)}}_{\mathrlap{\in Fib}}
    \\
    X_1 &\overset{(f,g)}{\longrightarrow}& X_2\underset{B}{\times} X_2
  }
  \,.
$$

This makes also the morphism $X''_1 \to B$ be a fibration, so that the whole diagram may now be regarded as a diagram in the category of fibrant objects $(\mathcal{C}_{/B})_f$ of the [[slice category]] over $B$.

As such, the top horizontal morphism now exhibits a [[right homotopy]] which under [[localization]] $\gamma_B \;\colon\; (\mathcal{C}_{/B})_f \longrightarrow Ho(\mathcal{C}_{/B})$ (def. \ref{FibrantCofibrantReplacementFunctorToHomotopyCategory}) of the [[slice model structure]] (prop. \ref{ModelStructureOnSliceCategory}) we have

$$
  \gamma_B(f) = \gamma_B(g)
  \,.
$$

The result then follows by observing that we have a commuting square of [[functors]]

$$
  \array{
     (\mathcal{C}^{\ast/}_{/B})_f &\overset{fib}{\longrightarrow}& \mathcal{C}^{\ast/}
     \\
     \downarrow^{\mathrlap{\gamma_B}} &\swArrow& \downarrow^{\mathrlap{\gamma}}
     \\
     Ho(\mathcal{C}^{\ast/}_{/B}) &\longrightarrow& Ho(\mathcal{C}^{\ast/})
  }
  \,,
$$

because, by lemma \ref{BaseChangePreservesFibrationsAndWeakEquivalences}, the top and right composite sends weak equivalences to isomorphisms, and hence the bottom filler exists by theorem \ref{UniversalPropertyOfHomotopyCategoryOfAModelCategory}. This implies the claim.

=--






### Homotopy fibers
 {#HomotopyFibers}

We now discuss the homotopy-theoretic properties of the [[mapping cone]]- and [[mapping cocone]]-constructions from [above](#MappingCones).

**Literature** ([Brown 73, section 4](#Brown73)).

+-- {: .num_remark}
###### Remark

The [[factorization lemma]] \ref{FactorizationLemma} with prop. \ref{ConeAndMappingCylinder} says that the [[mapping cocone]] of a morphism $f$, def. \ref{MappingConeAndMappingCocone}, is equivalently the plain [[fiber]], example \ref{FiberAndCofiberInPointedObjects}, of a fibrant resolution $\tilde f$ of $f$:

$$
  \array{
    Path_\ast(f) &\longrightarrow& Path(f)
    \\
    \downarrow &(pb)& \downarrow^{\mathrlap{\tilde f}}
    \\
    \ast &\longrightarrow& Y
  }
  \,.
$$

=--

The following prop. \ref{FiberOfFibrationIsCompatibleWithWeakEquivalences} says that, up to equivalence, this situation is independent of the specific fibration resolution $\tilde f$ provided by the [[factorization lemma]] (hence by the prescription for the [[mapping cocone]]), but only depends on it being _some_ fibration resolution.


+-- {: .num_prop #FiberOfFibrationIsCompatibleWithWeakEquivalences}
###### Proposition

In the [[category of fibrant objects]] $(\mathcal{C}^{\ast/})_f$, def. \ref{FullSubcategoriesOfFibrantCofibrantObjects}, of a [[slice model structure|model structure on pointed objects]] (prop. \ref{ModelStructureOnSliceCategory}) consider a morphism of [[fiber]]-diagrams, hence a [[commuting diagram]] of the form

$$
  \array{
    fib(p_1) &\longrightarrow& X_1 &\underoverset{\in Fib}{p_1}{\longrightarrow}& Y_1
    \\
    \downarrow^{\mathrlap{h}} && \downarrow^{\mathrlap{g}}
    && \downarrow^{\mathrlap{f}}
    \\
    fib(p_2) &\longrightarrow& X_2 &\underoverset{\in Fib}{p_2}{\longrightarrow}& Y_2
  }
  \,.
$$

If $f$ and $g$ weak equivalences, then so is $h$.

=--

+-- {: .proof}
###### Proof

Factor the diagram in question through the pullback of $p_2$ along $f$

$$
  \array{
    fib(p_1)
      &\longrightarrow&
    X_1
    \\
    \downarrow^{\mathrlap{h}}
      &&
    {}^{\mathllap{\in W}}\downarrow
      &
      \searrow^{\mathrlap{p_1}}
      &
    \\
    fib(f^\ast p_2)
      &\longrightarrow&
    f^\ast X_2
      &\underoverset{\in Fib}{f^\ast p_2}{\longrightarrow}&
    Y_1
    \\
    \downarrow^{\mathrlap{\simeq}} && \downarrow^{\mathrlap{\in W}} && \downarrow^{\mathrlap{f}}_{\mathrlap{\in W}}
    \\
    fib(p_2) &\longrightarrow& X_2 &\underoverset{\in Fib}{p_2}{\longrightarrow}& Y_2
  }
$$

and observe that

1. $fib(f^\ast p_2) = pt^\ast f^\ast p_2 = pt^\ast p_2 = fib(p_2)$;

1. $f^\ast X_2 \to X_2$ is a weak equivalence by lemma \ref{InCfPullbackAlongFibrationPreservesWeakEquivalences};

1. $X_1 \to f^\ast X_2$ is a weak equivalence by assumption and by [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences});

Moreover, this diagram exhibits $h \colon fib(p_1)\to fib(f^\ast p_2) = fib(p_2)$ as the base change, along $\ast \to Y_1$, of $X_1 \to f^\ast X_2$. Therefore the claim now follows with lemma \ref{BaseChangePreservesFibrationsAndWeakEquivalences}.

=--

Hence we say:

+-- {: .num_defn #HomotopyFiber}
###### Definition

Let $\mathcal{C}$ be a [[model category]] and $\mathcal{C}^{\ast/}$ its model category of [[pointed objects]], prop. \ref{ModelStructureOnSliceCategory}. For $f \colon X \longrightarrow Y$ any morphism in its [[category of fibrant objects]] $(\mathcal{C}^{\ast/})_f$, def. \ref{FullSubcategoriesOfFibrantCofibrantObjects}, then its **[[homotopy fiber]]**

$$
  hofib(f)\longrightarrow X
$$

is the morphism in the [[homotopy category of a model category|homotopy category]] $Ho(\mathcal{C}^{\ast/})$, def. \ref{HomotopyCategoryOfAModelCategory}, which is represented by the [[fiber]], example \ref{FiberAndCofiberInPointedObjects}, of any fibration resolution $\tilde f$ of $f$ (hence any fibration $\tilde f$ such that $f$ factors through a weak equivalence followed by $\tilde f$).

Dually:

For $f \colon X \longrightarrow Y$ any morphism in its [[category of cofibrant objects]] $(\mathcal{C}^{\ast/})_c$, def. \ref{FullSubcategoriesOfFibrantCofibrantObjects}, then its **[[homotopy cofiber]]**

$$
  Y \longrightarrow hocofib(f)
$$

is the morphism in the [[homotopy category of a model category|homotopy category]] $Ho(\mathcal{C})$, def. \ref{HomotopyCategoryOfAModelCategory}, which is represented by the [[cofiber]], example \ref{FiberAndCofiberInPointedObjects}, of any cofibration resolution of $f$ (hence any cofibration $\tilde f$ such that $f$ factors as $\tilde f$ followed by a weak equivalence).

=--

+-- {: .num_prop #HomotopyFiberIndependentOfChoiceOfFibrantReplacement}
###### Proposition

The homotopy fiber in def. \ref{HomotopyFiber} is indeed well defined, in that for $f_1$ and $f_2$ two fibration replacements of any morphisms $f$ in $\mathcal{C}_f$, then their fibers are isomorphic in $Ho(\mathcal{C}^{\ast/})$.

=--

+-- {: .proof}
###### Proof

It is sufficient to exhibit an isomorphism in $Ho(\mathcal{C}^{\ast/})$ from the fiber of the fibration replacement given by the [[factorization lemma]] \ref{FactorizationLemma} (for any choice of [[path space object]]) to the fiber of any other fibration resolution.

Hence given a morphism $f \colon Y \longrightarrow X$ and a factorization

$$
  f
  \;\colon\;
  X
    \underset{\in W}{\longrightarrow}
  \hat X
   \underoverset{f_1}{\in Fib}{\longrightarrow}
  Y
$$

consider, for any choice $Path(Y)$ of [[path space object]] (def. \ref{PathAndCylinderObjectsInAModelCategory}),  the diagram

$$
  \array{
    Path(f) &\overset{\in W \cap Fib}{\longrightarrow}& X
    \\
    {}^{\mathllap{\in W}}\downarrow
      &(pb)&
    \downarrow^{\mathrlap{\in W}}
    \\
    Path(f_1) &\overset{\in W \cap Fib}{\longrightarrow}& \hat X
    \\
    {}^{\mathllap{\in Fib}}\downarrow
      &(pb)&
    \downarrow^{\mathrlap{ {f_1} \atop {\in Fib}}}
    \\
    Path(Y) &\underoverset{\in W \cap Fib}{p_1}{\longrightarrow}& Y
    \\
    {}^{\mathllap{ {p_0} \atop \in W \cap Fib}}\downarrow
    \\
    Y
  }
$$

as in the proof of lemma \ref{FactorizationLemma}. Now by repeatedly using prop. \ref{FiberOfFibrationIsCompatibleWithWeakEquivalences}:

1. the bottom square gives a weak equivalence from the fiber of $Path(f_1) \to Path(Y)$ to the fiber of $f_1$;

1. The square

   $$
     \array{
        Path(f_1) &\overset{id}{\longrightarrow}& Path(f_1)
        \\
        \downarrow && \downarrow
        \\
        Path(Y) &\underset{p_0}{\longrightarrow}& Y
     }
   $$

   gives a weak equivalence from the fiber of $Path(f_1) \to Path(Y)$ to the fiber of $Path(f_1)\to Y$.

1. Similarly the total vertical composite gives a weak equivalence via

   $$
     \array{
        Path(f) &\overset{\in W}{\longrightarrow}& Path(f_1)
        \\
        \downarrow && \downarrow
        \\
        Y &\underset{id}{\longrightarrow}& Y
     }
   $$


from the fiber of $Path(f) \to Y$ to the fiber of $Path(f_1)\to Y$.

Together this is a [[zig-zag]] of weak equivalences of the form

$$
  fib(f_1)
    \;\overset{\in W}{\longleftarrow}\;
  fib(Path(f_1)\to Path(Y))
    \;\overset{\in W}{\longrightarrow}\;
  fib(Path(f_1)\to Y)
    \;\overset{\in W}{\longleftarrow}\;
  fib(Path(f) \to Y)
$$

between the fiber of $Path(f) \to Y$ and the fiber of $f_1$. This gives an isomorphism in the [[homotopy category of a model category|homotopy category]].

=--


+-- {: .num_example #FibersOfSerreFibrations}
###### Example
**(fibers of Serre fibrations)**

In showing that [[Serre fibrations]] are abstract fibrations in the sense of [[model category]] theory, theorem \ref{TopQuillenModelStructure} implies that the [[fiber]] $F$ (example \ref{FiberAndCofiberInPointedObjects}) of a [[Serre fibration]], def. \ref{SerreFibration}

$$
  \array{
    F &\longrightarrow& X
    \\
    && \downarrow^{\mathrlap{p}}
    \\
    && B
  }
$$

over any point is actually a [[homotopy fiber]] in the sense of def. \ref{HomotopyFiber}. With prop. \ref{FiberOfFibrationIsCompatibleWithWeakEquivalences} this implies that the [[weak homotopy type]] of the fiber only depends on the Serre fibration up to weak homotopy equivalence in that if $p' \colon X' \to B'$ is another Serre fibration fitting into a [[commuting diagram]] of the form

$$
  \array{
    X &\overset{\in W_{cl}}{\longrightarrow}& X'
    \\
    \downarrow^{\mathrlap{p}} && \downarrow^{\mathrlap{p'}}
    \\
    B &\overset{\in W_{cl}}{\longrightarrow}& B'
  }
$$

then $F \overset{\in W_{cl}}{\longrightarrow} F'$.

In particular this gives that the [[weak homotopy type]] of the fiber of a Serre fibration $p \colon X \to B$ does not change as the basepoint is moved in the same connected component. For let $\gamma \colon I \longrightarrow B$ be a path between two points

$$
  b_{0,1}
    \;\colon\;
  \ast
    \underoverset{\in W_{cl}}{i_{0,1}}{\longrightarrow}
  I
    \overset{\gamma}{\longrightarrow}
  B
  \,.
$$

Then since all objects in $(Top_{cg})_{Quillen}$ are fibrant, and since the endpoint inclusions $i_{0,1}$ are weak equivalences, lemma \ref{InCfPullbackAlongFibrationPreservesWeakEquivalences} gives the [[zig-zag]] of top horizontal weak equivalences in the following diagram:

$$
  \array{
    F_{b_0} = & b_0^\ast p
      &\overset{\in W_{cl}}{\longrightarrow}&
    \gamma^{\ast}p
      &\overset{\in W_{cl}}{\longleftarrow}&
    b_1^\ast p
    &
    = F_{b_1}
    \\
    & \downarrow &(pb)& \downarrow{\mathrlap{{\gamma^\ast f} \atop {\in \atop {Fib}}}} &\;\;(pb)& \downarrow
    \\
    & \ast
      &\underoverset{i_0}{\in W_{cl}}{\longrightarrow}&
    I
      &\underoverset{i_1}{\in W_{cl}}{\longleftarrow}&
    \ast
  }
$$

and hence an isomorphism $F_{b_0} \simeq F_{b_1}$ in the [[classical homotopy category]] (def. \ref{ClassicalHomotopyCategory}).

The same kind of argument applied to maps from the square $I^2$ gives that if $\gamma_1, \gamma_2\colon I \to B$ are two homotopic paths with coinciding endpoints, then the isomorphisms between fibers over endpoints which they induce are equal. (But in general the isomorphism between the fibers does depend on the choice of homotopy class of paths connecting the basepoints!)

The same kind of argument also shows that if $B$ has the structure of a [[cell complex]] (def. \ref{TopologicalCellComplex}) then the restriction of the Serre fibration to one cell $D^n$ may be identified in the homotopy category with  $D^n \times F$, and may be canonically identified so if the [[fundamental group]] of $X$ is trivial. This is used when deriving the [[Serre spectral sequence|Serre]]-[[Atiyah-Hirzebruch spectral sequence]] for $p$ ([prop.](Introduction+to+Stable+homotopy+theory+--+S#AHSSExistence)).

=--

+-- {: .num_example #StandardTopologicalMappingConeIsHomotopyCofiber}
###### Example

For every [[continuous function]] $f \colon X \longrightarrow Y$ between [[CW-complexes]], def. \ref{TopologicalCellComplex}, then the standard topological mapping cone is the [[attaching space]] (example \ref{PushoutInTop})

$$
  Y \cup_f Cone(X) \;\; \in Top
$$

of $Y$ with the standard cone $Cone(X)$ given by collapsing one end of the standard topological cyclinder $X \times I$ (def. \ref{TopologicalInterval}) as shown in example \ref{MappingConesInTopologicalSpaces}.

Equipped with the canonical continuous function

$$
  Y \longrightarrow Y \cup_f Cone(X)
$$

this represents the [[homotopy cofiber]], def. \ref{HomotopyFiber}, of $f$ with respect to the [[classical model structure on topological spaces]] $\mathcal{C}= Top_{Quillen}$ from theorem \ref{TopQuillenModelStructure}.

=--

+-- {: .proof}
###### Proof

By prop. \ref{TopologicalCylinderOnCWComplexIsGoodCylinderObject}, for $X$ a [[CW-complex]] then the standard topological cylinder object $X\times I$ is indeed a  cyclinder object in $Top_{Quillen}$. Therefore by prop. \ref{ConeAndMappingCylinder} and the [[factorization lemma]] \ref{FactorizationLemma}, the mapping cone construction indeed produces first a cofibrant replacement of $f$ and then the ordinary cofiber of that, hence a model for the homotopy cofiber.

=--

+-- {: .num_example}
###### Example

The [[homotopy fiber]] of the inclusion of [[classifying spaces]] $B O(n) \hookrightarrow B O(n+1)$ is the [[n-sphere]] $S^n$. See [this prop.](Introduction+to+Stable+homotopy+theory+--+S#HomotopyFiberOfInclusionOfConsecutiveClassifyingSpaces) at _[Classifying spaces and G-structure](Introduction+to+Stable+homotopy+theory+--+S#ClassifyingSpaces)_.

=--


+-- {: .num_example #FiberOfFibrationWeaklyEquivalentToFiberOfItsCocylinder}
###### Example

Suppose a morphism $f \colon X \longrightarrow Y$ already happens to be a fibration between fibrant objects. The [[factorization lemma]] \ref{FactorizationLemma} replaces it by a fibration out of the [[mapping cocylinder]] $Path(f)$, but such that the comparison morphism is a weak equivalence:

$$
  \array{
    fib(f) &\longrightarrow& X &\underoverset{\in Fib}{f}{\longrightarrow}& Y
    \\
    \downarrow^{\mathrlap{\in W}} && \downarrow^{\mathrlap{\in W}} && \downarrow^{\mathrlap{id}}
    \\
    fib(\tilde f) &\longrightarrow& Path(f) &\underoverset{\in Fib}{\tilde f}{\longrightarrow}& Y
  }
  \,.
$$

Hence by prop. \ref{FiberOfFibrationIsCompatibleWithWeakEquivalences} in this case the ordinary fiber of $f$ is weakly equivalent to the [[mapping cocone]], def. \ref{MappingConeAndMappingCocone}.

=--


We may now state the abstract version of the statement of prop. \ref{SerreFibrationGivesExactSequenceOfHomotopyGroups}:

+-- {: .num_prop #ExactSequenceOfHomotopyFiberAtOneStage}
###### Proposition

Let $\mathcal{C}$ be a [[model category]]. For $f \colon X \to Y$ any morphism of [[pointed objects]], and for $A$ a [[pointed object]], def. \ref{CategoryOfPointedObjects}, then the sequence

$$
  [A,hofib(f)]_\ast \overset{i_\ast}{\longrightarrow} [A,X]_\ast \overset{f_\ast}{\longrightarrow} [A,Y]_{\ast}
$$

is [[exact sequence|exact]] as a sequence of [[pointed sets]].

(Where the sequence here is the image of the [[homotopy fiber]] sequence of def. \ref{HomotopyFiber} under the hom-functor $[A,-]_\ast \;\colon\; Ho(\mathcal{C}^{\ast/}) \longrightarrow Set^{\ast/}$ from example \ref{HomotopyCategoryOfPointedModelStructureIsEnrichedInPointedSets}.)


=--

+-- {: .proof}
###### Proof

Let $A$, $X$ and $Y$ denote fibrant-cofibrant objects in $\mathcal{C}^{\ast/}$ representing the given objects of the same name in $Ho(\mathcal{C}^{\ast/})$. Moreover, let $f$ be a fibration in $\mathcal{C}^{\ast/}$ representing the given morphism of the same name in $Ho(\mathcal{C}^{\ast/})$.

Then by def. \ref{HomotopyFiber} and prop.
\ref{HomotopyFiberIndependentOfChoiceOfFibrantReplacement} there is a representative $hofib(f) \in \mathcal{C}$ of the homotopy fiber which fits into a pullback diagram of the form

$$
  \array{
    hofib(f) &\overset{i}{\longrightarrow}& X
    \\
    \downarrow && \downarrow^{\mathrlap{f}}
    \\
    \ast &\longrightarrow& Y
  }
$$

With this the hom-sets in question are represented by genuine morphisms in $\mathcal{C}^{\ast/}$, modulo homotopy. From this it follows immediately that $im(i_\ast)$ includes into $ker(f_\ast)$. Hence it remains to show the converse: that every element in $ker(f_\ast)$ indeed comes from $im(i_\ast)$.

But an element in $ker(f_\ast)$ is represented by a morphism $\alpha \colon A \to X$ such that there is a left homotopy as in the following diagram

$$
  \array{
     && A &\overset{\alpha}{\longrightarrow}& X
     \\
     && {}^{\mathllap{i_0}}\downarrow &{}^{\tilde \eta}\nearrow& \downarrow^{\mathrlap{f}}
     \\
     A &\overset{i_1}{\longrightarrow} & Cyl(A) &\overset{\eta}{\longrightarrow}& Y
     \\
     \downarrow && && \downarrow^{\mathrlap{=}}
     \\
     \ast && \longrightarrow && Y
  }
  \,.
$$

Now by lemma \ref{ComponentMapsOfCylinderAndPathSpaceInGoodSituation} the square here has a lift $\tilde \eta$, as shown. This means that $i_1 \circ\tilde \eta$ is left homotopic to $\alpha$. But by the universal property of the fiber, $i_1 \circ \tilde \eta$ factors through $i \colon hofib(f) \to X$.

=--

With prop. \ref{FiberOfFibrationIsCompatibleWithWeakEquivalences} it also follows notably that the loop space construction becomes well-defined on the homotopy category:

+-- {: .num_remark #ConcatenatedLoopSpaceObject}
###### Remark

Given an object $X \in \mathcal{C}^{\ast/}_f$, and picking any [[path space object]] $Path(X)$, def. \ref{PathAndCylinderObjectsInAModelCategory} with induced [[loop space object]] $\Omega X$, def. \ref{SuspensionAndLoopSpaceObject}, write $Path_2(X) = Path(X) \underset{X}{\times} Path(X)$ for the [[path space object]] given by the fiber product  of $Path(X)$ with itself, via example \ref{ComposedPathSpaceObjects}. From the pullback diagram there, the fiber inclusion $\Omega X \to Path(X)$ induces a morphism

$$
  \Omega X \times \Omega X \longrightarrow (\Omega X)_2
  \,.
$$

In the case where $\mathcal{C}^{\ast/} = Top^{\ast/}$ and $\Omega$ is induced, via def. \ref{SuspensionAndLoopSpaceObject}, from the standard path space object (def. \ref{TopologicalPathSpace}), i.e. in the case that

$$
  \Omega X = fib(Maps(I_+,X)_\ast \longrightarrow X \times X)
  \,,
$$

then this is the operation of concatenating two loops parameterized by $I = [0,1]$ to a single loop parameterized by $[0,2]$.

=--

+-- {: .num_prop #LoopingAsFunctorOnHomotopyCategory}
###### Proposition

Let $\mathcal{C}$ be a [[model category]], def. \ref{ModelCategory}. Then the construction of forming [[loop space objects]] $X\mapsto \Omega X$, def. \ref{SuspensionAndLoopSpaceObject} (which on $\mathcal{C}^{\ast/}_f$ depends on a choice of [[path space objects]], def. \ref{PathAndCylinderObjectsInAModelCategory}) becomes unique up to isomorphism in the [[homotopy category of a model category|homotopy category]] (def. \ref{HomotopyCategoryOfAModelCategory}) of the [[slice model structure|model structure on pointed objects]] (prop. \ref{ModelStructureOnSliceCategory}) and extends to a [[functor]]:

$$
  \Omega
    \;\colon\;
  Ho(\mathcal{C}^{\ast/})
    \longrightarrow
  Ho(\mathcal{C}^{\ast/})
  \,.
$$

Dually, the [[reduced suspension]] operation, def. \ref{SuspensionAndLoopSpaceObject}, which on $\mathcal{C}^{\ast/}$ depends on a choice of [[cylinder object]], becomes a functor on the homotopy category

$$
  \Sigma
   \;\colon\;
  Ho(\mathcal{C}^{\ast/})
    \longrightarrow
  Ho(\mathcal{C}^{\ast/})
  \,.
$$

Moreover, the pairing operation induced on the objects in the image of this functor via remark \ref{ConcatenatedLoopSpaceObject} (concatenation of loops) gives the objects in the image of $\Omega$ [[group object]] structure, and makes this functor lift as

$$
  \Omega
    \;\colon\;
  Ho(\mathcal{C}^{\ast/})
    \longrightarrow
  Grp(Ho(\mathcal{C}^{\ast/}))
  \,.
$$

=--

([Brown 73, section 4, theorem 3](#Brown73))

+-- {: .proof}
###### Proof


Given an object $X \in \mathcal{C}^{\ast/}$ and given two choices of path space objects $Path(X)$ and $\widetilde{Path(X)}$, we need to produce an isomorphism in $Ho(\mathcal{C}^{\ast/})$ between $\Omega X$ and $\tilde \Omega X$.

To that end, first lemma \ref{ReplacementOfPathObjects} implies that any two choices of path space objects are connected via a third path space by a [[span]] of morphisms compatible with the structure maps. By [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}) every morphism of path space objects compatible with the inclusion of the base object is a weak equivalence. With this, lemma \ref{BaseChangePreservesFibrationsAndWeakEquivalences} implies that these morphisms induce weak equivalences on the corresponding loop space objects. This shows that all choices of loop space objects become isomorphic in the homotopy category.

Moreover, all the isomorphisms produced this way are actually equal: this follows from lemma \ref{UniquenessOfFibersOfQualizedMorphismsInHoC} applied to

$$
  \array{
     X &\overset{s}{\longrightarrow}& Path(X) &\stackrel{\longrightarrow}{\longrightarrow}& \widetilde{Path(X)}
     \\
     && \downarrow && \downarrow
     \\
     && X\times X &\overset{id}{\longrightarrow}&  X \times X
  }
  \,.
$$

This way we obtain a functor

$$
  \Omega \;\colon\; \mathcal{C}^{\ast/}_f \longrightarrow Ho(\mathcal{C}^{\ast/})
  \,.
$$

By prop. \ref{FiberOfFibrationIsCompatibleWithWeakEquivalences} and Rem. \ref{InCatOfFibrantObjectsProductPreservesEquivalences} this functor sends weak equivalences to isomorphisms. Therefore the functor on homotopy categories now follows with theorem \ref{UniversalPropertyOfHomotopyCategoryOfAModelCategory}.

It is immediate to see that the operation of loop concatenation from remark \ref{ConcatenatedLoopSpaceObject} gives the objects $\Omega X \in Ho(\mathcal{C}^{\ast/})$ the structure of [[monoids]]. It is now sufficient to see that these are in fact groups:

We claim that the inverse-assigning operation is given by the left map in the following pasting composite

$$
  \array{
    \Omega' X &\longrightarrow& Path'(X) &\overset{}{\longrightarrow}& X \times X
    \\
    \downarrow^{\mathrlap{\simeq}} && \downarrow^{\mathrlap{\simeq}} &(pb)& \downarrow^{\mathrlap{swap}}
    \\
    \Omega X &\longrightarrow& Path(X) &\underset{(p_0,p_1)}{\longrightarrow}& X \times X
  }
  \,,
$$

(where $Path'(X)$, thus defined, is the path space object obtained from $Path(X)$ by "reversing the notion of source and target of a path").

To see that this is indeed an inverse, it is sufficient to see that the two morphisms

$$
  \Omega X \stackrel{\longrightarrow}{\longrightarrow} (\Omega X)_2
$$

induced from

$$
  \array{
  Path(X)
\stackrel{\overset{\Delta}{\longrightarrow}}{\underset{(s\circ p_0,s \circ p_0)}{\longrightarrow}}
  Path(X) \times_X Path'(X)
 }
$$

coincide in the homotopy category. This follows with lemma \ref{UniquenessOfFibersOfQualizedMorphismsInHoC} applied to the following commuting diagram:

$$
  \array{
    X
      &\overset{i}{\longrightarrow}&
    Path(X)
      &\stackrel{\overset{\Delta}{\longrightarrow}}{\underset{(s\circ p_0,s \circ p_0)}{\longrightarrow}}&
    Path(X)\times_X Path'(X)
    \\
    && {}^{\mathllap{(p_0,p_1)}}\downarrow && \downarrow^{\mathrlap{}}
    \\
    && X\times X &\overset{\Delta \circ pr_1}{\longrightarrow}& X \times X
  }
  \,.
$$


=--





### Homotopy pullbacks
 {#HomotopyPullbacks}

The concept of [[homotopy fibers]] of def. \ref{HomotopyFiber} is a special case of the more general concept of [[homotopy pullbacks]].

+-- {: .num_defn #RightProperModelCategory}
###### Definition

A [[model category]] $\mathcal{C}$ (def. \ref{ModelCategory}) is called a **[[right proper model category]]** if [[pullback]] along fibrations preserves weak equivalences.

=--

+-- {: .num_example}
###### Example

By lemma \ref{InCfPullbackAlongFibrationPreservesWeakEquivalences}, a [[model category]] $\mathcal{C}$ (def. \ref{ModelCategory}) in which all objects are fibrant is a [[right proper model category]] (def. \ref{RightProperModelCategory}).

=--


+-- {: .num_defn #HomotopyPullback}
###### Definition

Let $\mathcal{C}$ be a [[right proper model category]] (def. \ref{RightProperModelCategory}). Then a [[commuting square]]

$$
  \array{
    A &\longrightarrow& B
    \\
    \downarrow && \downarrow^{\mathrlap{g}}
    \\
     C &\underset{f}{\longrightarrow}& D
  }
$$

in $\mathcal{C}_f$ is called a **[[homotopy pullback]]** (of $f$ along $g$ and equivalently of $g$ along $f$) if the following equivalent conditions hold:

1. for some factorization of the form

   $$
     g \colon B \overset{\in W }{\longrightarrow} \hat B \overset{\in Fib}{\longrightarrow} D
   $$

   the universally induced morphism from $A$ into the pullback of $\hat B$ along $f$ is a weak equivalence:

   $$
     \array{
       A &\longrightarrow& B
       \\
       {}^{\mathllap{\in W}}\downarrow && \downarrow^{\mathrlap{\in W}}
       \\
       C \underset{D}{\times} \hat B
        &\longrightarrow&
       \hat B
       \\
       \downarrow &(pb)& \downarrow^{\mathrlap{\in Fib}}
       \\
       C &\longrightarrow& D
     }
     \,.
   $$


1. for some factorization of the form

   $$
     f \colon C \overset{\in W }{\longrightarrow} \hat C \overset{\in Fib}{\longrightarrow} D
   $$

   the universally induced morphism from $A$ into the pullback of $\hat D$ along $g$ is a weak equivalence:

   $$
     A \overset{\in W}{\longrightarrow} \hat C \underset{D}{\times} B
     \,.
   $$

1. the above two conditions hold for every such factorization.

=--

(e.g. [Goerss-Jardine 96, II (8.14) ](Simplicial+homotopy+Theory))


+-- {: .num_prop #ConditionsForHomotopyPullbackAreIndeedEquivalent}
###### Proposition

The conditions in def. \ref{HomotopyPullback} are indeed equivalent.

=--

+-- {: .proof}
###### Proof

First assume that the first condition holds, in that

$$
  \array{
    A &\longrightarrow& B
    \\
    {}^{\mathllap{\in W}}\downarrow && \downarrow^{\mathrlap{\in W}}
    \\
    C \underset{D}{\times} \hat B
     &\longrightarrow&
    \hat B
    \\
    \downarrow &(pb)& \downarrow^{\mathrlap{\in Fib}}
    \\
    C &\longrightarrow& D
  }
  \,.
$$

Then let

$$
  f \colon C \overset{\in W }{\longrightarrow} \hat C \overset{\in Fib}{\longrightarrow} D
$$

be any factorization of $f$ and consider the [[pasting]] diagram (using the [[pasting law]] for pullbacks)

$$
  \array{
    A
      &\overset{}{\longrightarrow}&
    \hat C \underset{D}{\times} B
      &\longrightarrow&
    B
    \\
    {}^{\mathllap{\in W}}\downarrow
      &&
    \downarrow^{\mathrlap{\in W}}
      &(pb)&
    \downarrow^{\mathrlap{\in W}}
    \\
    C\underset{D}{\times} \hat B
      &\overset{\in W}{\longrightarrow}&
    \hat C \underset{D}{\times} \hat D
      &\overset{\in Fib}{\longrightarrow}&
    \hat B
    \\
    \downarrow
      &(pb)&
    \downarrow^{\mathrlap{\in \atop Fib}}
      &(pb)&
    \downarrow^{\mathrlap{\in Fib}}
    \\
    C
      &\underset{\in W}{\longrightarrow}&
    \hat C
      &\underset{\in Fib}{\longrightarrow}&
    D
  }
  \,,
$$

where the inner morphisms are fibrations and weak equivalences, as shown, by the pullback stability of fibrations (prop. \ref{ClosurePropertiesOfInjectiveAndProjectiveMorphisms}) and then since pullback along fibrations preserves weak equivalences by assumption of [[right proper model category|right properness]] (def. \ref{RightProperModelCategory}).
Hence it follows by [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}) that also the comparison morphism $A \to \hat C \underset{D}{\times} B$ is a weak equivalence.

In conclusion, if the homotopy pullback condition is satisfied for one factorization of $g$, then it is satisfied for all factorizations of $f$. Since the argument is symmetric in $f$ and $g$, this proves the claim.

=--

+-- {: .num_remark #PullbackOfFibrationWithFibrantObjectsIsHomotopyPullback}
###### Remark

In particular, an ordinary pullback square of fibrant objects, one of whose edges is a fibration, is a homotopy pullback square according to def. \ref{HomotopyPullback}.

=--



+-- {: .num_prop #HomotopyPullbackPreservesWeakEquivalencesOfSpans}
###### Proposition

Let $\mathcal{C}$ be a [[right proper model category]] (def. \ref{RightProperModelCategory}). Given a [[diagram]] in $\mathcal{C}$ of the form

$$
  \array{
    A &\longrightarrow& B &\overset{\in Fib}{\longleftarrow}& C
    \\
    \downarrow^{\mathrlap{\in W}}
      &&
    \downarrow^{\mathrlap{\in W}}
      &&
    \downarrow^{\mathrlap{\in W}}
    \\
    D &\longrightarrow& E &\underset{\in Fib}{\longleftarrow}& F
  }
$$

then the induced morphism on [[pullbacks]] is a weak equivalence

$$
  A \underset{B}{\times} C
   \overset{\in W}{\longrightarrow}
  D \underset{E}{\times} F
  \,.
$$

=--

+-- {: .proof}
###### Proof

(The reader should draw the 3-dimensional cube diagram which we describe in words now.)

First consider the universal morphism $C \to E \underset{F}{\times} C$ and observe that it is a weak equivalence by [[right proper model category|right properness]] (def. \ref{RightProperModelCategory})
and [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}).

Then consider the universal morphism $A \underset{B}{\times}C \to A \underset{B}{\times}(E \underset{F}{\times}C)$ and observe that this is also a weak equivalence, since $A \underset{B}{\times} C$ is the limiting cone of a homotopy pullback square by remark \ref{PullbackOfFibrationWithFibrantObjectsIsHomotopyPullback}, and since the morphism is the comparison morphism to the pullback of the factorization constructed in the first step.

Now by using the [[pasting law]], then the commutativity of the "left" face of the cube, then the pasting law again, one finds that $A \underset{B}{\times} (E \underset{F}{\times} C) \simeq A \underset{D}{\times} (D \underset{E} F{\times})$. Again by [[right proper model category|right properness]] this implies that $A \underset{B}{\times} (E \underset{F}{\times} C)\to D \underset{E}{\times} F$ is a weak equivalence.

With this the claim follows by [[two-out-of-three]].

=--



Homotopy pullbacks satisfy the usual abstract properties of pullbacks:

+-- {: .num_prop #HomotopyPullbackOfWeakEquivalences}
###### Proposition

Let $\mathcal{C}$ be a [[right proper model category]] (def. \ref{RightProperModelCategory}).
If in a [[commuting square]] in $\mathcal{C}$ one edge is a weak equivalence, then the square is a [[homotopy pullback]] square precisely if the opposite edge is a weak equivalence, too.

=--

+-- {: .proof}
###### Proof

Consider a commuting square of the form

$$
  \array{
    A &\longrightarrow& B
    \\
    \downarrow && \downarrow
    \\
    C &\underset{\in W}{\longrightarrow}& D
  }
  \,.
$$

To detect whether this is a homotopy pullback, by def. \ref{HomotopyPullback} and prop. \ref{ConditionsForHomotopyPullbackAreIndeedEquivalent}, we are to choose any factorization of the right vertical morphism to obtain the pasting composite

$$
  \array{
    A &\longrightarrow& B
    \\
    \downarrow && \downarrow^{\mathrlap{\in W}}
    \\
    C \underset{D}{\times} \hat B
      &\overset{\in W}{\longrightarrow}&
    \hat B
    \\
    \downarrow
      &(pb)&
    \downarrow^{\mathrlap{\in Fib}}
    \\
    C &\underset{\in W}{\longrightarrow}& D
  }
  \,.
$$

Here the morphism in the middle is a weak equivalence by [[right proper model category|right properness]] (def. \ref{RightProperModelCategory}). Hence it follows by [[two-out-of-three]] that the top left comparison morphism is a weak equivalence (and so the original square is a homotopy pullback) precisely if the top morphism is a weak equivalence.

=--

+-- {: .num_prop #ClosurePropertiesOfHomotopyPullbacks}
###### Proposition

Let $\mathcal{C}$ be a [[right proper model category]] (def. \ref{RightProperModelCategory}).

1. ([[pasting law]]) If in a [[commuting diagram]]

   $$
     \array{
       A &\longrightarrow& B &\longrightarrow& C
        \\
        \downarrow
          &&
       \downarrow
          &&
        \downarrow
        \\
        D &\longrightarrow& E &\underset{}{\longrightarrow}& F
      }
   $$

   the square on the right is a homotoy pullback (def. \ref{HomotopyPullback}) then the left square is, too, precisely if the total rectangle is;

1. in the presence of [[functorial factorization]] (def. \ref{FunctorialFactorization}) through weak equivalences followed by fibrations:

   every [[retract]] of a homotopy pullback square (in the category $\mathcal{C}_f^{\Box}$ of commuting squares in $\mathcal{C}_f$) is itself a homotopy pullback square.

=--

+-- {: .proof}
###### Proof

For the first statement: choose a factorization of $C \overset{\in W}{\to} \hat F \overset{\in Fib}{\to} F$, pull it back to a factorization $B \to \hat B \overset{\in Fib}{\to} E$ and assume that $B \to \hat B$ is a weak equivalence, i.e. that the right square is a homotopy pullback. Now use the ordinary [[pasting law]] to conclude.


For the second statement: functorially choose a factorization of the two right vertical morphisms of the squares and factor the squares through the pullbacks of the corresponding fibrations along the bottom morphisms, respectively. Now the statement that the squares are homotopy pullbacks is equivalent to their top left vertical morphisms being weak equivalences. Factor these top left morphisms functorially as cofibrations followed by acyclic fibrations. Then the statement that the squares are homotopy pullbacks is equivalent to those top left cofibrations being acyclic. Now the claim follows using that the retract of an acyclic cofibration is an acyclic cofibration (prop. \ref{ClosurePropertiesOfInjectiveAndProjectiveMorphisms}).

=--





### Long sequences
 {#LongSequences}

The ordinary [[fiber]], example \ref{FiberAndCofiberInPointedObjects}, of a morphism has the property that taking it _twice_ is always trivial:

$$
   \ast \simeq fib(fib(f)) \longrightarrow fib(f) \longrightarrow X \overset{f}{\longrightarrow} Y
  \,.
$$

This is crucially different for the [[homotopy fiber]], def. \ref{HomotopyFiber}. Here we discuss how this comes about and what the consequences are.

+-- {: .num_prop #HomotopyFiberOfHomotopyFiberIsLooping}
###### Proposition

Let $\mathcal{C}_f$ be a [[category of fibrant objects]] of a [[model category]], def. \ref{FullSubcategoriesOfFibrantCofibrantObjects} and let $f \colon X \longrightarrow Y$ be a morphism in its [[category of pointed objects]], def. \ref{CategoryOfPointedObjects}. Then the [[homotopy fiber]] of its [[homotopy fiber]], def. \ref{HomotopyFiber}, is isomorphic, in $Ho(\mathcal{C}^{\ast/})$, to the [[loop space object]] $\Omega Y$ of $Y$ (def. \ref{SuspensionAndLoopSpaceObject}, prop. \ref{LoopingAsFunctorOnHomotopyCategory}):

$$
  hofib(hofib(X \overset{f}{\to}Y)) \simeq \Omega Y
  \,.
$$

=--

+-- {: .proof}
###### Proof

Assume without restriction that $f \;\colon\; X \longrightarrow Y$ is already a fibration between fibrant objects in $\mathcal{C}$ (otherwise replace and rename). Then its homotopy fiber is its ordinary fiber, sitting in a [[pullback]] square

$$
  \array{
    hofib(f) \simeq & F &\overset{i}{\longrightarrow}& X
    \\
    & \downarrow && \downarrow^{\mathrlap{f}}
    \\
    & \ast &\longrightarrow& Y
  }
  \,.
$$

In order to compute $hofib(hofib(f))$, i.e. $hofib(i)$, we need to replace the fiber inclusion $i$ by a fibration. Using the [[factorization lemma]] \ref{FactorizationLemma} for this purpose yields, after a choice of [[path space object]] $Path(X)$ (def. \ref{PathAndCylinderObjectsInAModelCategory}), a replacement of the form

$$
  \array{
    F &\overset{\in W}{\longrightarrow}& F \times_X Path(X)
    \\
    &{}_{\mathllap{i}}\searrow& \downarrow^{\mathrlap{\tilde i}}_{\mathrlap{\in Fib}}
    \\
    && X
  }
  \,.
$$

Hence $hofib(i)$ is the ordinary fiber of this map:

$$
  hofib(hofib(f)) \simeq  F \times_X Path(X) \times_X \ast \;\;\;\; \in Ho(\mathcal{C}^{\ast/})
  \,.
$$

Notice that

$$
  F \times_X Path(X) \; \simeq \; \ast \times_Y Path(X)
$$

because of the [[pasting law]]:

$$
  \array{
     F \times_X Path(X) &\longrightarrow& Path(X)
     \\
     \downarrow &(pb)& \downarrow
     \\
     F &\overset{i}{\longrightarrow}& X
     \\
     \downarrow &(pb)& \downarrow^{\mathrlap{f}}
     \\
     \ast &\longrightarrow& Y
  }
  \,.
$$

Hence

$$
  hofib(hofib(f))
    \;\simeq\;
  \ast \times_Y Path(X) \times_X \ast
  \,.
$$

Now we claim that there is a choice of path space objects $Path(X)$ and $Path(Y)$ such that this model for the homotopy fiber (as an object in $\mathcal{C}^{\ast/}$) sits in a [[pullback]] diagram of the following form:

$$
  \array{
    \ast \times_Y Path(X) \times_X \ast &\longrightarrow& Path(X)
    \\
    \downarrow && \downarrow\mathrlap{\in W \cap F}
    \\
    \Omega Y &\longrightarrow& Path(Y)\times_Y X
    \\
    \downarrow &(pb)& \downarrow
    \\
    \ast &\longrightarrow&  Y \times X
  }
  \,.
$$

By the [[pasting law]] and the pullback stability of acyclic fibrations, this will prove the claim.

To see that the bottom square here is indeed a pullback, check the [[universal property]]: A morphism out of any $A$ into $\ast \underset{Y \times X}{\times} Path(Y) \times_Y X$ is a morphism $a \colon A \to Path(Y)$ and a morphism $b \colon A \to X$ such that $p_0(a) = \ast$, $p_1(a) = f(b)$ and $b = \ast$. Hence it is equivalently just a morphism $a \colon A \to Path(Y)$ such that $p_0(a) = \ast$ and $p_1(a) = \ast$. This is the defining universal property of $\Omega Y \coloneqq \ast \underset{Y}{\times} Path(Y) \underset{Y}{\times} \ast$.

Now to construct the right vertical morphism in the top square ([Quillen 67, page 3.1](#Quillen67)): Let $Path(Y)$ be any path space object for $Y$ and let $Path(X)$ be given by a factorization

$$
  (id_X, \; i \circ f, \; id_X)
  \;\colon\;
  X
  \overset{\in W}{\to}
  Path(X)
  \overset{\in Fib}{\longrightarrow}
  X \times_Y Path(Y) \times_Y X
$$

and regarded as a path space object of $X$ by further comoposing with

$$
  (pr_1,pr_3)\colon X \times_Y Path(Y) \times_Y X \overset{\in Fib}{\longrightarrow} X \times X
  \,.
$$

We need to show that $Path(X)\to Path(Y) \times_Y X$ is an acyclic fibration.

It is a fibration because $X\times_Y Path(Y) \times_Y X \to Path(Y)\times_Y X$ is a fibration, this being the pullback of the fibration $X \overset{f}{\to} Y$.

To see that it is also a weak equivalence, first observe that $ Path(Y)\times_Y X \overset{\in W \cap Fib}{\longrightarrow} X$, this being the pullback of the acyclic fibration of lemma \ref{ComponentMapsOfCylinderAndPathSpaceInGoodSituation}. Hence we have a factorization of the identity as

$$
  id_X
  \;\colon\;
  X
    \underoverset{\in W}{i}{\longrightarrow}
  Path(X)
    \overset{}{\longrightarrow}
  Path(Y)\times_Y X
    \underset{\in W \cap Fib}{\longrightarrow}
  X
$$

and so finally the claim follows by [[two-out-of-three]] (def. \ref{CategoryWithWeakEquivalences}).

=--

+-- {: .num_remark #HomotopyCommutativeSquares}
###### Remark

There is a conceptual way to understand prop. \ref{HomotopyFiberOfHomotopyFiberIsLooping} as follows:
If we draw double arrows to indicate [[homotopies]], then a [[homotopy fiber]] (def. \ref{HomotopyFiber}) is depicted by the following filled square:

$$
  \array{
    hofib(f) &\longrightarrow& \ast
    \\
    \downarrow &\swArrow& \downarrow
    \\
    X &\underset{f}{\longrightarrow}& Y
  }
$$

just like the ordinary [[fiber]] (example \ref{FiberAndCofiberInPointedObjects}) is given by a plain square

$$
  \array{
    fib(f) &\longrightarrow& \ast
    \\
    \downarrow && \downarrow
    \\
    X &\underset{f}{\longrightarrow}& Y
  }
  \,.
$$

One may show that just like the fiber is the _universal_ solution to making such a commuting square (a [[pullback]] [[limit|limit cone]] def. \ref{LimitsAndColimits}), so the homotopy fiber is the universal solution up to homotopy to make such a commuting square up to homotopy -- a [[homotopy pullback]] [[homotopy limit|homotopy limit cone]].

Now just like ordinary [[pullbacks]] satisfy the [[pasting law]] saying that attaching two pullback squares gives a pullback rectangle, the analogue is true for homotopy pullbacks. This implies that if we take the homotopy fiber of a homotopy fiber, thereby producing this double homotopy pullback square

$$
  \array{
    hofib(g) &\longrightarrow& hofib(f) &\longrightarrow& \ast
    \\
    \downarrow &\swArrow& \downarrow^{\mathrlap{g}} &\swArrow& \downarrow
    \\
    \ast &\longrightarrow& X &\underset{f}{\longrightarrow}& Y
  }
$$

then the total outer rectangle here is itself a homotopy pullback. But the outer rectangle exhibits the homotopy fiber of the point inclusion, which, via def. \ref{SuspensionAndLoopSpaceObject} and lemma \ref{FactorizationLemma}, is the [[loop space object]]:

$$
  \array{
    \Omega Y &\longrightarrow& \ast
    \\
    \downarrow &\swArrow& \downarrow
    \\
    \ast &\longrightarrow& Y
  }
  \,.
$$

=--


+-- {: .num_prop #LongFiberSequence}
###### Proposition

Let $\mathcal{C}$ be a model category and let $f \colon X \to Y$ be morphism in the pointed homotopy category $Ho(\mathcal{C}^{\ast/})$ (prop. \ref{ModelStructureOnSliceCategory}). Then:

1. There is a long sequence to the left in $\mathcal{C}^{\ast/}$ of the form

   $$
     \cdots
       \longrightarrow
     \Omega X
       \overset{\overline{\Omega} f}{\longrightarrow}
     \Omega Y
       \longrightarrow
     hofib(f)
       \longrightarrow
     X
       \overset{f}{\longrightarrow}
     Y
     \,,
   $$

   where each morphism is the [[homotopy fiber]] (def. \ref{HomotopyFiber}) of the following one: the **[[homotopy fiber sequence]]** of $f$. Here $\overline{\Omega}f$ denotes $\Omega f$ followed by forming inverses with respect to the group structure on $\Omega(-)$ from prop. \ref{LoopingAsFunctorOnHomotopyCategory}.

   Moreover, for $A\in \mathcal{C}^{\ast/}$ any object, then there is a [[long exact sequence]]

   $$
     \cdots
     \to
     [A,\Omega^2 Y]_\ast
     \longrightarrow
     [A,\Omega hofib(f)]_\ast
     \longrightarrow
     [A, \Omega X]_\ast
     \longrightarrow
     [A,\Omega Y]
     \longrightarrow
     [A,hofib(f)]_\ast
     \longrightarrow
     [A,X]_\ast
     \longrightarrow
     [A,Y]_\ast
   $$

   of [[pointed sets]], where $[-,-]_\ast$ denotes the pointed set valued hom-functor of example \ref{HomotopyCategoryOfPointedModelStructureIsEnrichedInPointedSets}.

1. Dually, there is a long sequence to the right in $\mathcal{C}^{\ast/}$ of the form

   $$
     X
       \overset{f}{\longrightarrow}
     Y
       \overset{}{\longrightarrow}
     hocofib(f)
       \longrightarrow
     \Sigma X
       \overset{\overline{\Sigma} f}{\longrightarrow}
     \Sigma Y
       \to \cdots
     \,,
   $$

   where each morphism is the [[homotopy cofiber]] (def. \ref{HomotopyFiber}) of the previous one: the **[[homotopy cofiber sequence]]** of $f$. Moreover, for $A\in \mathcal{C}^{\ast/}$ any object, then there is a [[long exact sequence]]

   $$
     \cdots
     \to
     [\Sigma^2 X, A]_\ast
     \longrightarrow
     [\Sigma hocofib(f), A]_\ast
     \longrightarrow
     [\Sigma Y, A]_\ast
     \longrightarrow
     [\Sigma X, A]
     \longrightarrow
     [hocofib(f),A]_\ast
     \longrightarrow
     [Y,A]_\ast
     \longrightarrow
     [X,A]_\ast
   $$

   of [[pointed sets]], where $[-,-]_\ast$ denotes the pointed set valued hom-functor of example \ref{HomotopyCategoryOfPointedModelStructureIsEnrichedInPointedSets}.


=--

([Quillen 67, I.3, prop. 4](#Quillen67))

+-- {: .proof}
###### Proof

That there are long sequences of this form is the result of combining prop. \ref{HomotopyFiberOfHomotopyFiberIsLooping} and  prop. \ref{ExactSequenceOfHomotopyFiberAtOneStage}.

It only remains to see that it is indeed the morphisms $\overline{\Omega} f$ that appear, as indicated.

In order to see this, it is convenient to adopt the following notation: for $f \colon X \to Y$ a morphism, then we denote the collection of [[generalized element]] of its homotopy fiber as

$$
  hofib(f)
  =
  \left\{
    (x, f(x) \overset{\gamma_1}{\rightsquigarrow} \ast)
  \right\}
$$

indicating that these elements are pairs consisting of an element $x$ of $X$ and a "path" (an element of the given path space object) from $f(x)$ to the basepoint.

This way the canonical map $hofib(f) \to X$ is $(x, f(x) \rightsquigarrow \ast) \mapsto x$. Hence in this notation the homotopy fiber of the homotopy fiber reads

$$
  hofib(hofib(f))
  =
  \left\{
    ( (x, f(x) \overset{\gamma_1}{\rightsquigarrow} \ast),
            x \overset{\gamma_2}{\rightsquigarrow} \ast  )
  \right\}
  \,.
$$

This identifies with $\Omega Y$ by forming the loops

$$
  \gamma_1 \cdot f(\overline{\gamma_2})
  \,,
$$

where the overline denotes reversal and the dot denotes concatenation.

Then consider the next homotopy fiber

$$
  hofib(hofib(hofib(f)))
  =
  \left\{
    \left(
      ( (x, f(x) \overset{\gamma_1}{\rightsquigarrow} \ast), x \overset{\gamma_2}{\rightsquigarrow} \ast  ),
      \left(
      \array{
         x && \overset{\gamma_3}{\rightsquigarrow} && \ast
         \\
         f(x) &&\overset{f(\gamma_3)}{\rightsquigarrow}&& \ast
         \\
         & {}_{\mathllap{\gamma_1}}\searrow & \Rightarrow & \swarrow_{\mathllap{}}
         \\
         && \ast
      }
      \right)
    \right)
  \right\}
  \,,
$$

where on the right we have a path in $hofib(f)$ from $(x, f(x)\overset{\gamma_1}{\rightsquigarrow} \ast)$ to the basepoint element. This is a path $\gamma_3$ together with a path-of-paths which connects $f_1$ to $f(\gamma_3)$.

By the above convention this is identified with the loop in $X$ which is

$$
  \gamma_2 \cdot (\overline{\gamma}_3)
  \,.
$$

But the map to $hofib(hofib(f))$ sends this data to $( (x, f(x) \overset{\gamma_1}{\rightsquigarrow} \ast), x \overset{\gamma_2}{\rightsquigarrow} \ast  )$, hence to the loop

$$
  \begin{aligned}
    \gamma_1 \cdot f( \overline{\gamma_2} )
    & \simeq
    f(\gamma_3) \cdot f(\overline{\gamma_2})
    \\
    & =
    f( \gamma_3 \cdot \overline{\gamma_2} )
    \\
    & =
    f ( \overline{\gamma_2 \cdot \overline{\gamma}_3} )
    \\
    & =
    \overline{f(\gamma_2 \cdot \overline{\gamma}_3) }
  \end{aligned}
  \,,
$$

hence to the reveral of the image under $f$ of the loop in $X$.





=--

+-- {: .num_remark}
###### Remark

In ([Quillen 67, I.3, prop. 3, prop. 4](#Quillen67)) more is shown than stated in prop. \ref{LongFiberSequence}: there the [[connecting homomorphism]] $\Omega  Y \to hofib(f)$ is not just shown to exist, but is described in detail via an [[action]] of $\Omega Y$ on $hofib(f)$ in $Ho(\mathcal{C})$. This takes a good bit more work. For our purposes here, however, it is sufficient to know that such a morphism exists at all, hence that $\Omega Y \simeq hofib(hofib(f))$.

=--


+-- {: .num_example #LongExactSequeceOfHomotopyGroups}
###### Example

Let $\mathcal{C} = (Top_{cg})_{Quillen}$ be the [[classical model structure on topological spaces]] ([[compactly generated topological spaces|compactly generated]]) from theorem \ref{TopQuillenModelStructure}, theorem \ref{ClassicalModelStructureOnCompactlyGeneratedTopologicalSpaces}. Then using the  standard pointed topological path space objects $Maps(I_+,X)$ from def. \ref{TopologicalPathSpace} and example \ref{PointedMappingSpace} as the abstract path space objects in def. \ref{PathAndCylinderObjectsInAModelCategory}, via prop. \ref{TopologicalPathSpaceIsGoodPathSpaceObject}, this gives that

$$
  [\ast, \Omega^n X] \simeq \pi_n(X)
$$

is the $n$th [[homotopy group]], def. \ref{HomotopyGroupsOftopologicalSpaces}, of $X$ at its basepoint.

Hence using $A = \ast$ in the first item of prop. \ref{LongFiberSequence}, the [[long exact sequence]] this gives is of the form

$$
   \cdots
  \to
  \pi_3(X)
   \overset{f_\ast}{\longrightarrow}
  \pi_3(Y)
   \longrightarrow
  \pi_2(hofib(f))
   \overset{}{\longrightarrow}
  \pi_2(X)
   \overset{-f_\ast}{\longrightarrow}
  \pi_2(Y)
   \longrightarrow
  \pi_1(hofib(f))
   \overset{}{\longrightarrow}
  \pi_1(X)
    \overset{f_\ast}{\longrightarrow}
  \pi_1(Y)
   \overset{}{\longrightarrow}
  \ast
  \,.
$$


This is called the **[[long exact sequence of homotopy groups]]** induced by $f$.

=--

+-- {: .num_remark}
###### Remark

As we pass to [[stable homotopy theory]] (in [[Introduction to Stable homotopy theory -- 1|Part 1)]]), the long exact sequences in example \ref{LongExactSequeceOfHomotopyGroups} become long not just to the left, but also to the right. Given then a [[tower of fibrations]], there is an induced sequence of such long exact sequences of homotopy groups, which organizes into an _[[exact couple]]_. For more on this see at _[[Introduction to Stable homotopy theory -- I|Interlude -- Spectral sequences]]_ ([this remark](Introduction+to+Stable+homotopy+theory+--+I#UnrolledExactCoupleOfAFiltrationOnASpectrum)).

=--

+-- {: .num_example}
###### Example

Let again $\mathcal{C} = (Top_{cg})_{Quillen}$ be the [[classical model structure on topological spaces]] ([[compactly generated topological space|compactly generated]]) from theorem \ref{TopQuillenModelStructure}, theorem \ref{ClassicalModelStructureOnCompactlyGeneratedTopologicalSpaces}, as in example \ref{LongExactSequeceOfHomotopyGroups}. For $E \in Top_{cg}^{\ast/}$ any [[pointed topological space]] and $i \colon A \hookrightarrow X$ an inclusion of pointed topological spaces, the exactness of the sequence in the second item of prop. \ref{LongFiberSequence}

$$
  \cdots \to [hocofib(i), E] \longrightarrow [X,E]_\ast \longrightarrow [A,E]_\ast \to \cdots
$$

gives that the functor

$$
  [-,E]_\ast
  \;\colon\;
  (Top^{\ast/}_{CW})^{op}
  \longrightarrow
  Set^{\ast/}
$$

behaves like one degree in an [additive](Introduction+to+Stable+homotopy+theory+--+S#WedgeAxiom) [[reduced cohomology theory]] ([def.](Introduction+to+Stable+homotopy+theory+--+S#ReducedGeneralizedCohomology)). The [[Brown representability theorem]] ([thm.](Introduction+to+Stable+homotopy+theory+--+S#BrownRepresentabilityTraditional)) implies that all additive reduced cohomology theories are degreewise representable this way ([prop.](Introduction+to+Stable+homotopy+theory+--+S#AdditiveReducedCohomologyTheoryRepresentedByOmegaSpectrum)).

=--





## The suspension/looping adjunction
 {#TheSuspensionLoopingDiscussion}

We conclude this discussion of classical homotopy theory with the key statement that leads over to [[stable homotopy theory]] in _[[Introduction to Stable homotopy theory -- 1]]_: the suspension and looping adjunction on the classical pointed homotopy category.


+-- {: .num_prop #SuspensionAndLoopAreAdjointOnHomotopyCategory}
###### Proposition

The canonical [[loop space]] functor $\Omega$ and [[reduced suspension]] functor $\Sigma$ from prop. \ref{LoopingAsFunctorOnHomotopyCategory} on the [[classical pointed homotopy category]] from def. \ref{ClassicalModelStructureOnPointedTopologicalSpaces} are [[adjoint functors]], with $\Sigma$ [[left adjoint]] and $\Omega$ [[right adjoint]]:

$$
  (\Sigma \dashv \Omega)
  \;\colon\;
  Ho(Top^{\ast/})
   \stackrel{\overset{\Sigma}{\longleftarrow}}{\underset{\Omega}{\longrightarrow}}
  Ho(Top^{\ast/})
  \,.
$$

Moreover, this is equivalently the adjoint pair of [[derived functors]], according to prop. \ref{QuillenAdjunctionInducesAdjunctionOnHomotopyCategories}, of the [[Quillen adjunction]]

$$
  (Top_{cg}^{\ast/})_{Quillen}
    \underoverset
      {\underset{Maps(S^1, -)_\ast}{\longrightarrow}}
      {\overset{S^1 \wedge (-)}{\longleftarrow}}
      {\bot}
  (Top_{cg}^{\ast/})_{Quillen}
$$

of cor. \ref{SmashHomAdjunctionOnPointedCompactlyGeneratedTopologicalSpaces}.

=--

+-- {: .proof}
###### Proof


By prop. \ref{LoopingAsFunctorOnHomotopyCategory} we may represent $\Sigma$ and $\Omega$ by any choice of [[cylinder objects]] and [[path space objects]] (def. \ref{PathAndCylinderObjectsInAModelCategory}).

The standard topological path space $(-)^I$ is generally a path space object by prop. \ref{TopologicalPathSpaceIsGoodPathSpaceObject}. With prop. \ref{ReducedSuspensionBySmashProductWithCircle} this shows that

$$
  \Omega  \simeq  \mathbb{R} Maps(S^1,-)_\ast
  \,.
$$

Moreover, by the existence of [[CW-approximations]] (remark \ref{EveryTopologicalSpaceWeaklyEquivalentToACWComplex}) we may represent each object in the homotopy category by a [[CW-complex]]. On such, the standard topological cylinder $(-)\times I$ is a [[cylinder object]] by prop. \ref{TopologicalCylinderOnCWComplexIsGoodCylinderObject}. With prop. \ref{ReducedSuspensionBySmashProductWithCircle} this shows that

$$
  \Sigma \simeq \mathbb{L} (S^1 \wedge (-))
  \,.
$$


=--


+-- {: .num_remark}
###### Final remark

What is called _[[stable homotopy theory]]_ is the result of universally forcing the $(\Sigma\dashv \Omega)$-[[adjunction]] of prop. \ref{SuspensionAndLoopAreAdjointOnHomotopyCategory} to become an [[equivalence of categories]].

=--

This is the topic of the next section at _[[Introduction to Stable homotopy theory -- 1]]_.

$\,$


## References
 {#References}


A concise and yet self-contained re-write of the proof ([Quillen 67](#Quillen67)) of the [[classical model structure on topological spaces]] is provided in

* {#Hirschhorn15} [[Philip Hirschhorn]], _The Quillen model category of topological spaces_ ([arXiv:1508.01942](http://arxiv.org/abs/1508.01942)).

For general [[model category]] theory a decent review is in

* {#DwyerSpalinski95} [[William Dwyer]], J. Spalinski, _[[Homotopy theories and model categories]]_ ([pdf](http://folk.uio.no/paularne/SUPh05/DS.pdf)) in [[Ioan Mackenzie James]] (ed.), _[[Handbook of Algebraic Topology]]_ 1995

The equivalent definition of model categories that we use here is due to

* {#Joyal} [[André Joyal]], appendix E of _The theory of quasi-categories and its applications_ ([pdf](http://www.crm.cat/HigherCategories/hc2.pdf))

The two originals are still a good source to turn to:

* {#Quillen67} [[Daniel Quillen]], _Axiomatic homotopy theory_ in  _Homotopical algebra_, Lecture Notes in Mathematics, No. 43, Berlin (1967)

* {#Brown73} [[Kenneth Brown]], _[[Abstract Homotopy Theory and Generalized Sheaf Cohomology]]_, Transactions of the American Mathematical Society, Vol. 186 (1973), 419-458  ([JSTOR](http://www.jstor.org/stable/1996573))

For the restriction to the [[convenient category of topological spaces|convenient category]] of [[compactly generated topological spaces]] good sources are

* {#Lewis78} [[L. Gaunce Lewis]], _Compactly generated spaces_ ([pdf](http://www.math.uchicago.edu/~may/MISC/GaunceApp.pdf)), appendix A of _The Stable Category and Generalized Thom Spectra_ PhD thesis Chicago, 1978

* {#Strickland09} [[Neil Strickland]], _The category of CGWH spaces_, 2009 ([pdf](http://neil-strickland.staff.shef.ac.uk/courses/homotopy/cgwh.pdf))

Graphics taken from

* {#Muro10} [[Fernando Muro]], _Representability of Cohomology Theories_, Joint Mathematical Conference CSASC 2010, 22–27 January 2010, Prague, Czech Republic ([slides](https://personal.us.es/fmuro/files/slides/praha.pdf))


[[!redirects Introduction to Stable homotopy theory -- P]]
