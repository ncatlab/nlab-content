+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

**Top** denotes the [[category]] whose [[objects]] are [[topological spaces]] and whose [[morphisms]] are [[continuous functions]] between them. Its [[isomorphisms]] are the [[homeomorphisms]]. 

For exposition see _[[Introduction to Topology -- 1|Introduction to point-set topology]]_.

Often one considers (sometimes by default) [[subcategories]] of [[nice topological spaces]] such as [[compactly generated topological spaces]], notably because these are [[cartesian closed category|cartesian closed]]. There other other [[convenient categories of topological spaces]]. With any one such choice understood, it is often useful to regard it as "the" category of topological spaces.

The [[homotopy category]] of $Top$ given by its [[localization]] at the [[weak homotopy equivalences]] is the [[classical homotopy category]] [[Ho(Top)]]. This is the central object of study in [[homotopy theory]], see also at _[[classical model structure on topological spaces]]_.  The [[simplicial localization]] of [[Top]] at the [[weak homotopy equivalences]] is the archetypical [[(∞,1)-category]], [[equivalence of (infinity,1)-categories|equivalent]] to [[∞Grpd]] (see at _[[homotopy hypothesis]]_).

## Properties



### Universal constructions
 {#UniversalConstructions}

We discuss [[universal constructions]] in [[Top]], such as [[limits]]/[[colimits]], etc. The following definition suggests that universal constructions be seen in the context of $Top$ as a [[topological concrete category]] (see Proposition \ref{topcat} below).

$\,$

[[!include universal constructions of topological spaces -- table]]

$\,$


+-- {: .num_defn #InitialAndFinalTopologies}
###### Definition

Let $\{X_i = (S_i,\tau_i) \in Top\}_{i \in I}$ be a [[class]] of [[topological spaces]], and let $S \in Set$ be a bare [[set]]. Then

* For $\{S \stackrel{f_i}{\to} S_i \}_{i \in I}$ a set of [[functions]] out of $S$, the _[[initial topology]]_ $\tau_{initial}(\{f_i\}_{i \in I})$ is the topology on $S$ with the [[minimum]] collection of [[open subsets]] such that all $f_i \colon (S,\tau_{initial}(\{f_i\}_{i \in I}))\to X_i$ are [[continuous function|continuous]].

* For $\{S_i \stackrel{f_i}{\to} S\}_{i \in I}$ a set of [[functions]] into $S$, the _[[final topology]]_ $\tau_{final}(\{f_i\}_{i \in I})$ is the topology on $S$ with the [[maximum]] collection of [[open subsets]] such that all $f_i \colon X_i \to (S,\tau_{final}(\{f_i\}_{i \in I}))$ are [[continuous function|continuous]].

=--

+-- {: .num_example #TopologicalSubspace}
###### Example

For $X$ a single topological space, and $\iota_S \colon S \hookrightarrow U(X)$ a subset of its underlying set, then the initial topology $\tau_{intial}(\iota_S)$, def. \ref{InitialAndFinalTopologies}, is the [[subspace topology]], making

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

Conversely, for $p_S \colon U(X) \longrightarrow S$ an [[epimorphism]], then the final topology $\tau_{final}(p_S)$ on $S$ is the _[[quotient topology]]_.

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

The required [[universal property]] of $\left(\underset{\longleftarrow}{\lim}_{i \in I} S_i,\; \tau_{initial}(\{p_i\}_{i \in I})\right)$ is immediate: for 

$$
  \array{
    && (S,\tau)
    \\
    & {}^{\mathllap{f_i}}\swarrow && \searrow^{\mathrlap{f_j}} 
    \\
    X_i && \underset{}{\longrightarrow} && X_j
  }
$$

any [[cone]] over the diagram, then by construction there is a unique function of underlying sets $S \longrightarrow \underset{\longleftarrow}{\lim}_{i \in I} S_i$ making the required diagrams commute, and so all that is required is that this unique function is always [[continuous function|continuous]]. But this is precisely what the initial topology ensures.

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

For $S \in Set$, the $S$-indexed [[coproduct]] of the point, $\underset{s \in S}{\coprod}\ast $,  is the set $S$ itself equipped with the [[final topology]], hence is the [[discrete topological space]] on $S$.

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

(hence the largets subset of $S_X$ on which both functions coincide) and equipped with the [[subspace topology]], example \ref{TopologicalSubspace}.

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

two [[continuous functions]] out of the same [[domain]], then the [[colimit]] under this diagram is also called the _[[pushout]]_, denoted

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

(Here $g_\ast f$ is also called the pushout of $f$, or the _[[base change|cobase change]]_ of $f$ along $g$.) If $g$ is an inclusion, one also write $X \cup_f Y$ and calls this the _[[attaching space]]_.

<div style="float:left;margin:0 10px 10px 0;"><img src="http://ncatlab.org/nlab/files/AttachingSpace.jpg" width="450"></div>

By example \ref{CoequalizerInTop} the [[pushout]]/[[attaching space]] is the [[quotient topological space]]

$$
  X \sqcup_A Y \simeq (X\sqcup Y)/\sim
$$

of the [[disjoint union]] of $X$ and $Y$ subject to the [[equivalence relation]] which identifies a point in $X$ with a point in $Y$ if they have the same pre-image in $A$.

(graphics from [Aguilar-Gitler-Prieto 02](#AguilarGitlerPrieto02))

=--

+-- {: .num_example #TopologicalnSphereIsPushoutOfBoundaryOfnBallInclusionAlongItself}
###### Example

As an important special case of example \ref{PushoutInTop},  let 

$$
  i_n \colon S^{n-1}\longrightarrow D^n
$$

be the canonical inclusion of the standard [[n-sphere|(n-1)-sphere]] as the [[boundary]] of the standard [[n-disk]] (both regarded as [[topological spaces]] with their [[subspace topology]] as subspaces of the [[Cartesian space]] $\mathbb{R}^n$).


<div style="float:left;margin:0 10px 10px 0;">
<img src="http://ncatlab.org/nlab/files/GluingHemispheres.jpg" width="400"></div>

Then the colimit in [[Top]] under the diagram, i.e. the [[pushout]] of $i_n$ along itself,

$$
  \left\{
     D^n \overset{i_n}{\longleftarrow} S^{n-1} \overset{i_n}{\longrightarrow}
     D^n
  \right\}
  \,,
$$

is the [[n-sphere]] $S^n$:

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
     \downarrow && \downarrow^{\mathrlap{i_A}}
     \\
     B &\underset{i_B}{\longrightarrow}& X
  }
$$

is a [[pushout]] square in $Top$ (example \ref{PushoutInTop}).

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

Clearly the underlying diagram of underlying [[sets]] is a pushout in [[Set]]. Therefore by prop. \ref{DescriptionOfLimitsAndColimitsInTop} we need to show that the [[topological space|topology]] on $X$ is the [[final topology]] induced by the set of functions $\{i_A, i_B\}$, hence that 
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


+-- {: .num_example #attach} 
###### Example
If $X, Y, Z$ are [[normal topological spaces]] and $h: X \to Z$ is a [[closed embedding of topological spaces]] and $f: X \to Y$ is a [[continuous function]], then in the [[pushout]] diagram in $Top$ (example \ref{PushoutInTop})

$$\array{
X & \stackrel{h}{\to} & Z \\ 
\mathllap{f} \downarrow & & \downarrow \mathrlap{g} \\ 
Y & \underset{k}{\to} & W,
}$$

the space $W$ is normal and $k: Y \to W$ is a closed embedding.

=-- 

For **proof** of this and related statements see at _[[colimits of normal spaces]]_.


### Relation with $Set$

Write [[Set]] for the [[category]] of [[sets]].

+-- {: .num_defn #ForgetfulFunctorFromTopToSet}
###### Definition

Write

$$
  U \colon Top \longrightarrow Set
$$

for the [[forgetful functor]] that sends a topological space $X = (S,\tau)$ to its underlying set $U(X) = S \in Set$ and which regards a [[continuous function]] as a plain [[function]] on the underlying sets.

=--

Prop. \ref{DescriptionOfLimitsAndColimitsInTop} means in particular that:

+-- {: .num_prop }
###### Proposition

The category [[Top]] has all small [[limits]] and [[colimits]]. The [[forgetful functor]] $U \colon Top \to Set$ from def. \ref{ForgetfulFunctorFromTopToSet} [[preserved limit|preserves]] and [[lifted limit|lifts]] limits and colimits.

=--

(But it does not [[created limit|create]] or [[reflected limit|reflect]] them.)



+-- {: .num_prop}
###### Proposition

The [[forgetful functor]] $U$ from def. \ref{ForgetfulFunctorFromTopToSet} has a [[left adjoint]] $disc$, given by sending a [[set]] $S$ to the corresponding [[discrete topological space]], example \ref{DiscreteTopologicalSpaceAsCoproduct}

$$
  Top
  \stackrel{\overset{disc}{\longleftarrow}}{\underset{U}{\longrightarrow}}
  Set
  \,.
$$

=--

+-- {: .num_prop #topcat}
###### Proposition

The [[forgetful functor]] $U$ from def. \ref{ForgetfulFunctorFromTopToSet} exhibits $Top$ as 

* a [[concrete category]]

* a [[topological concrete category]].

=--


### Mono-/Epimorphisms
 {#MonoEpiMorphisms}

+-- {: .num_prop #SubspaceInclusionsAreRegularMonos}
###### Proposition
**([[regular monomorphisms]] of [[topological spaces]])**

In the [[category]] [[Top]] of [[topological space]], 

1. the [[monomorphisms]] are the those [[continuous functions]] which are [[injective functions]];

1. the [[regular monomorphisms]] are the [[topological embeddings]] (i.e. those continuous functions which are [[homeomorphisms]] onto their [[images]] equipped with the [[subspace topology]]).

=--

+-- {: .proof}
###### Proof 

Regarding the first statement: An injective continuous function $f \colon X \to Y$ clearly has the cancellation property that defines monomorphisms: for parallel continuous functions $g_1,g_2 \colon Z \to X$: if $f \circ g_1 = f \circ g_1$, then $g_1 = g_2$ because continuous functions are equal precisely if their underlying functions of sets are equal. Conversely, if $f$ has the cancellation property, then testing on points $g_1, g_2 \colon \ast \to X$ gives that $f$ is injective.

Regarding the second statement: from the construction of [[equalizers]] in [[Top]] (example \ref{EqualizerInTop}) we have that these are topological subspace inclusions.

Conversely, let  $i \colon X \to Y$ be a [[topological subspace embedding]]. We need to show that this is the equalizer of some pair of parallel morphisms.

To that end, form the [[cokernel pair]] $(i_1, i_2)$ by taking the [[pushout]] of $i$ against itself (in the category of sets, and using the [[quotient topology]] on a [[disjoint union space]]). By [this prop.](regular+monomorphism#RegEquEff), the equalizer of that pair is the set-theoretic equalizer of that pair of functions endowed with the [[subspace topology]]. Since monomorphisms in [[Set]] are regular, we get the function $i$ back, and again by example \ref{EqualizerInTop}, it gets equipped with the subspace topology. This completes the proof. 

=--

### Intersections and quotients

+-- {: .num_lemma #pushout} 
###### Lemma 

The [[pushout]] in [[Top]] of any (closed/open) [[topological subspace]] inclusion $i \colon A \hookrightarrow B$, example \ref{TopologicalSubspace}, along any [[continuous function]] $f \colon A \to C$ is itself an a (closed/open) subspace $j \colon C \hookrightarrow D$. 

=-- 

For proof see [there](subspace+topology#pushout).




## Related concepts

* [[topological concrete category]] 

* [[Ho(Top)]], [[∞Grpd]]

* [[convenient category of topological spaces]]

* [[TopGrp]]

## References

For general references see those listed at _[[topology]]_, such as

* {#Bourbaki71} [[Nicolas Bourbaki]], chapter 1 _Topological Structures_ of _Elements of Mathematics III: General topology_, Springer 1971, 1990

See also 

* {#AguilarGitlerPrieto02} Marcelo Aguilar, [[Samuel Gitler]], Carlos Prieto, section 12 of _Algebraic topology from a homotopical viewpoint_, Springer (2002) ([toc pdf](http://tocs.ulb.tu-darmstadt.de/106999419.pdf))

An axiomatic desciption of $Top$ along the lines of [[ETCS]] for [[Set]] is discussed in

* Dana Schlomiuk, _An elementary theory of the category of topological space_, Transactions of the AMS, volume 149 (1970)


category: category

[[!redirects TopologicalSpaces]]
[[!redirects category of topological spaces]]

[[!redirects TopSp]]

