
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

This entry lists and discusses examples and special types of the [[universal constructions]] called  _[[limits]]_ and _[[colimits]]_.

It starts with very elementary and simple examples and eventually passes to more sophisticated ones.

For examples of the other kinds of [[universal constructions]] see

* _[[examples of adjoint functors]]_

* _[[examples of Kan extensions]]_

# Contents
* table of contents
{: toc}


## Limits and colimits of sets 
  {#limcoliminset}


In the [[category]] [[Set]] of [[sets]], the concepts of [[limits]] and [[colimits]] reduce to the familiar operations of 

* [[cartesian product]] of sets;
* [[disjoint union]] of sets;
* [[subsets]] defined by [[equations]]
* [[quotient sets]] of [[equivalence relations]].

### Limits

#### Terminal object

The [[terminal object]] is the limit of the empty functor $F: \emptyset \to Set$. So a [[terminal object]] of $Set$ is a set $X$ such that there is a unique function from any set to $X$. This is given by any [[singleton]] set $\{a\}$, where the unique function $Y \to \{a\}$ from any set $Y$ is the function that sends every element in $Y$ to $a$.

#### Product

Given two sets $A, B$, the categorical [[product]] is the limit of the diagram (with no non-trivial maps)
$$
\array{
  A & B
}.
$$
This is given by the usual product of sets, which can be constructed as the set of [[Kuratowski pairs]]
$$
  A \times B = \{ \{\{a\}, \{a, b\}\}: a \in A, b \in B\}.
$$
We tend to write $(a, b)$ instead of $\{\{a\}, \{a, b\}\}$.

The projection maps $\pi_1: A \times B \to A$ and $\pi_2: A \times B \to B$ are given by
$$
  \pi_1(a, b) = a, \pi_2(a, b) = b.
$$

To see this satisfies the universal property of products, given any pair of maps $f: X \to A$ and $g: X \to B$, we obtain a map $(f, g): X \to A \times B$ given by
$$
  (f, g)(x) = (f(x), g(x)).
$$

More generally, given a (possibility infinite) collection of sets $\{A_\alpha\}_{\alpha \in I}$, the product of the discrete diagram consisting of these sets is the usual product $\prod_{\alpha \in I} A_\alpha$. This can be constructed as
$$
  \prod_{\alpha \in I} A_\alpha = \left\{f: I \to \bigcup_{\alpha \in I} A_\alpha \mid f(\alpha) \in A_\alpha\;\text{ for all }\;\alpha \in I\right\}.
$$
#### Equalizer
Given a pair of functions $f, g: X \to Y$, the [[equalizer]] is the limit of the diagram
$$
\array{
X & \underset{g}{\overset{f}{\rightrightarrows}} & Y
}.
$$
The limit is given by a map $e: A \to X$ such that given any $a: B \to X$, it factors through $e$ if and only if $f \circ a = g \circ a$. In other words, $a$ factors through $e$ if and only if $\im a \subseteq \{x \in X: f(x) = g(x)\}$. Thus the limit of the diagram is given by
$$
  A = \{x \in X: f(x) = g(x)\},
$$
and the map $e: A \to X$ is given by the inclusion.

#### Pullback
Given two maps $f: A \to C$ and $g: B \to C$, the [[pullback]] is the limit of the diagram
$$
\array{
  & & A\\
  & & \downarrow^\mathrlap{f}\\
  B & \underset{g}{\to} & C
}.
$$
This limit is given by
$$
  \{(a, b) \in A \times B: f(a) = g(b)\},
$$
with the maps to $A$ and $B$ given by the projections.

While the definition of a pullback is symmetric in $f$ and $g$, it is usually convenient to think of this as pulling back $f$ along $g$ (or the other way round). This has more natural interpretations in certain special cases.

If $g: B \to C$ is the inclusion of a subset (ie. is a [[monomorphism]]), then the pullback of $f$ along $g$ is given by
$$
  \{a \in A: f(a) \in B\}.
$$
So this is given by restricting $f$ to the elements that are mapped into $B$.

Further, if $f: A \to C$ is *also* the inclusion fo a subset, so that $A$ and $B$ are both subobjects of $C$, then the above formula tells us that the pullback is simply the intersection of the two subsets.

Alternatively, we can view the map $f: A \to C$ as a collection of sets indexed by elements of $C$, where the set indexed by $c \in C$ is given by $A_c = f^{-1}(c)$. Under this interpretation, pulling $f$ back along $g$ gives a collection of sets indexed by elements of $B$, where the set indexed by $b \in B$ is given b $A_{g(b)}$.

#### General limits
Given a general [[Set]]-valued functor $F : D \to Set$, if the limit $lim F$ exists, then by definition, for any set $A$, a function $f: A \to lim F$ is equivalent to a compatible family of maps $f_d: A \to F(d)$ for each $d \in Obj(D)$.

In particular, since an element of a set $X$ bijects with maps $1 \to X$ from the singleton $1 = \{\emptyset\}$, we have
$$
  lim F \cong Set (1, lim F) \cong [D, Set](const_1, F),
$$
where $const_1$ is the functor that constantly takes the value $1$. Thus the limit is given by the set of [[natural transformations]] from $const_1$ to $F$.

More concretely, a compatible family of maps $1 \to F(d)$ is given by an element $s_d \in F(d)$ for each $d \in Obj(d)$, satisfying the appropriate compatibility conditions. Thus, the limit can be realized as a subset of the product $\prod_{d \in Obj(d)} F(d)$ of all objects:
$$
  lim F = \left\{ (s_d)_d \in \prod_d F(d) | \forall (d \stackrel{f}{\to} d') : F(f)(s_{d}) = s_{d'}  \right\}.
$$

### Colimits
#### Initial object
The [[initial object]] in $Set$ is a set $X$ such that there is a unique map from $X$ to any other set. This is given by the empty set $\emptyset$.

#### Coproduct
(...)

#### Coequalizer
(...)

#### Pushout
(...)

#### General colimits
The colimit over a [[nLab:Set|Set]]-valued functor $F : D \to Set$ is a quotient set of the disjoint union $\coprod_{d \in Obj(D)} F(d)$: 
  $$ 
    colim F \simeq \left(\coprod_{d\in D} F(d)\right)/_\sim \,, 
  $$
  where the equivalence relation $\sim$ is that which is _generated_ by 
  $$
    ((x \in F(d)) \sim (x' \in F(d')))\quad if \quad (\exists (f : d \to d') \quad with F(f)(x) = x')
  \,.
  $$
  If $D$ is a [[filtered category]] then the resulting equivalence relation can be described as follows:
  $$
    ((x \in F(d)) \sim (x' \in F(d')))\quad iff \quad (\exists d'', (f : d \to d''), (g: d' \to d'') \quad with F(f)(x) = F(g)(x'))
  \,.
  $$
  (If $D$ is not filtered, then this description doesn't yield an equivalence relation.)


## Limits and colimits of topological spaces
 {#OfTopologicalSpaces}


We discuss limits and colimits in the category [[Top]] of [[topological spaces]].

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
    X_i && \underset{}{\longrightarrow} && X_i
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

W





## Limits and colimits in a preordered set
(..)


## Limits and colimits in functor categories
 {#InFunctorCategories}

The main point is that *[[limits of functors are computed objectwise]]*. See there for more

## Colimit of a representable functor
 {#ColimitOfARepresentablefunctor}

The [[colimit]] of a [[representable functor]] (with values in [[Set]]) is the [[point]], i.e. the [[terminal object]] in [[Set]].

One can readily see this from a [[universal element]]-style argument, by direct inspection of [[cocones]]. 

$$
  \array{
     \mathcal{C}(D,C) && 
       \overset{
         (D \overset{f}{\to}C)^\ast
       }{\longleftarrow}
     && \mathcal{C}(C,C)
     \\
     & \searrow && \swarrow
     \\
     &&
     \left\{
       C \overset{id}{\to}C
     \right\}
  }
$$

However, this style of reasoning does not easily generalize to [[higher category theory]]. The following gives a more abstract argument that is short and generalizes. We state it in [[(∞,1)-category theory]] just for definiteness of notation:

+-- {: .num_prop #HodgeStarFollowedByHodgeStar}  
###### Proposition
**([[homotopy colimit]] over a [[representable functor]] is [[n-truncated object in an (∞,1)-category|contractible]])**

Let $\mathcal{C}$ be a [[small (∞,1)-category]] and consider an [[∞Groupoids|∞-groupoid]]-valued [[(∞,1)-functor]] $F \colon \mathcal{C}^{op} \to Groupoids_\infty$ which is [[representable functor|representable]], i.e. in the [[essential image|image]] of the [[(∞,1)-Yoneda embedding]] $F \simeq y C$: 

$$
  \array{
    \mathcal{C}
    &
    \overset{
      \phantom{AA}
      y
      \phantom{AA}
    }{\longrightarrow}
    &
    Func
    \big(
      \mathcal{C}^{op},
      Groupoids_\infty
    \big)
    \\
    C &\mapsto&
    y C
    \coloneqq
    \mathcal{C}(-,C)
  }
$$

Then the [[(∞,1)-colimit]] over this [[(∞,1)-functor]] is contractible, i.e. is the point, the [[terminal object in an (∞,1)-category|terminal object]] in [[∞Groupoids]]:

$$
  \underset{
    \underset{\mathcal{C}}{\longrightarrow}
  }{\lim}
   (y C)
   \;\simeq\;
   \ast
$$

=--

+-- {: .proof}
###### Proof

The terminal $\infty$-groupoid $\ast$ is characterized by the fact that for each $S \in Groupoids_\infty$ we have $Groupoids_\infty(\ast, S) \simeq S$.
Therefore it is sufficient to show that $\underset{\longrightarrow}{\lim}\big(y C\big)$ has the same property:


$$
  \begin{aligned}
  Groupoids_\infty
  \left(
    \underset{\longrightarrow}{\lim}
    \big(
      y C
    \big)
    ,
    S
  \right)
  & \simeq\;
  Func(
    \mathcal{C}^{op}
    ,\,
    Groupoids_\infty
  )
  \left(
    y C
    ,
    const S
  \right)
  \\
  & \simeq\;
  (const S)(C)
  \\
  & \simeq\;
  S
  \end{aligned}
$$

Here the first step is the [[(∞,1)-adjunction]]

$$
  Func
  \big(
    \mathcal{C}^{op},
    Groupoids_\infty
  \big)
  \underoverset
    {
      \underset{const}{\longleftarrow}
    }
    {
      \overset{ \underset{\longrightarrow}{\lim} }{\longrightarrow}
    }
    {\phantom{AA}\bot\phantom{AA}}
  \Groupoids_\infty
$$

and the second step is the [[(∞,1)-Yoneda lemma]]

=--





## Examples of limits {#examplesoflimits}

In the following examples, $D$ is a [[small category]], $C$ is any category and the limit is taken over a functor $F : D^{op} \to C$.

### Simple diagrams {#limitssimplediagrams}


* the limit of the empty diagram $D = \emptyset$ in $C$ is, if it exists [[nLab:generalized the|the]] [[nLab:terminal object|terminal object]];

* if $D$ is a [[nLab:discrete category|discrete category]], i.e. a category with only identity morphisms, then a diagram $F : D \to C$ is just a collection $c_i$ of objects of $C$. Its limit is the [[nLab:product|product]] $\prod_i c_i$  of these.

* if $D = \{a \stackrel{\to}{\to} b\}$ then $lim F$ is the [[nLab:equalizer|equalizer]] of the two morphisms $F(b) \to F(a)$.

* if $D$ has an [[nLab:terminal object|terminal object]] $I$ (so that $I$ is an [[nLab:initial object|initial object]] in $D^{op}$), then the limit of any $F : D^{op} \to C$ is $F(I)$.

### Filtered limits {#filteredlimits}

* if $D$ is a [[nLab:poset|poset]], then the limit over $D^{op}$ is the supremum over the $F(d)$ with respect to $(F(d) \leq F(d')) \Leftrightarrow (F(d) \stackrel{F(\leq)}{\leftarrow} F(d'))$;

* the generalization of this is where the term "limit" for categorical limit (probably) originates from: for $D$ a [[nLab:filtered category|filtered category]], hence $D^{op}$ a cofiltered category, one may think of $(d \stackrel{f}{\to} d') \mapsto (F(d) \stackrel{F(f)}{\leftarrow} F(d')$ as witnessing that $F(d')$ is "larger than" $F(d)$ in some sense, and $lim F$ is then the "largest" of all these objects, the limiting object. This interpretation is perhaps more evident for filtered [[nLab:colimit|colimits]], where the codomain category $C$ is thought of as being the [[nLab:opposite category|opposite]] $C = E^{op}$. See the motivation at [[nLab:ind-object|ind-object]].

### In terms of other operations {#limitsintermsofotherops}

If products and equalizers exist in $C$, then limit of $F : D^{op} \to C$ can be exhibited as a [[nLab:subobject|subobject]] of the [[nLab:product|product]] of the $F(d)$, namely the [[nLab:equalizer|equalizer]] of

$$
  \prod_{d \in Obj(D)}
  F(d)
  \stackrel{\langle F(f) \circ p_{F(t(f))} \rangle_{f \in Mor(D)} }{\to}  
  \prod_{f \in Mor(D)}
  F(s(f))
$$

and

$$
  \prod_{d \in Obj(D)}
  F(d)
  \stackrel{\langle p_{F(s(f))} \rangle_{f \in Mor(D)} }{\to}  
  \prod_{f \in Mor(D)}
  F(s(f))  
  \,.
$$

See the explicit formula for the limit in [[nLab:Set|Set]]
in terms of a subset of a product set.


In particular therefore, a category has all limits already if it has all products and equalizers.



### Limits in presheaf categories {#limitsinpresheafcat}

Consider limits of functors $F : D^{op} \to PSh(C)$
with values in the [[category of presheaves]] over a [[category]] $C$.

+-- {: .num_prop #LimitsOfPresheaves}
###### Proposition
**([[limits of presheaves are computed objectwise]])**

Limits of presheaves are computed objectwise:

$$
  lim F : c \mapsto lim F(-)(c)
$$ 
Here on the right the limit is over the functor 
$F(-)(c) : D^{op} \to Set$.

Similarly for colimits

=--

Similarly [[colimit]]s of presheaves are computed objectwise.

+-- {: .num_prop}
###### Proposition

The [[Yoneda embedding]] 
$Y : C \to PSh(C)$ commutes with small limits:

Let $F : D^{op} \to C$, then we have
$$
  Y(lim F) \simeq lim (Y\circ F)
$$
if $lim F$ exists.

=--

**Warning** The Yoneda embedding does _not_ in general preserve colimits.

### Limits in under-categories {#limitsinundercat}

Limits in [[under category|under categories]] are a special case of limits in [[comma category|comma categories]]. These are explained elsewhere. It may still be useful to spell out some details for the special case of under-categories. This is what the following does.


+-- {: .num_prop}
###### Proposition

Limits in an [[under category]] are computed as limits in the underlying category.

Precisely: let $C$ be a [[category]], $t \in C$ an [[object]], and $t/C$ the corresponding [[under category]], and $p : t/C \to C$ the obvious projection.

Let $F : D \to t/C$ be any [[functor]]. Then, if it exists, the [[limit]] over $p \circ F$ in $C$ is the image under $p$ of the limit over $F$:

$$
  p(\lim F)  \simeq \lim (p F)
$$

and $\lim F$ is uniquely characterized by $\lim (p F)$.


=--
 
+-- {: .proof}
###### Proof

Over a morphism $\gamma : d \to d'$ in $D$ the limiting cone over $p F$  (which exists by assumption) looks like

$$
  \array{
    && \lim p F
    \\
    & \swarrow && \searrow
    \\
    p F(d) &&\stackrel{p F(\gamma)}{\to}&& p F(d') 
  }
$$


By the universal property of the limit this has a unique
lift to a cone in the [[under category]] $t/C$ over $F$:

$$
  \array{
    && t 
    \\
    & \swarrow &\downarrow & \searrow
    \\
    && \lim p F
    \\
    \downarrow & \swarrow && \searrow & \downarrow
    \\
    p F(d) &&\stackrel{p F(\gamma)}{\to}&& p F(d') 
  }
$$


It therefore remains to show that this is indeed a limiting cone over $F$. Again, this is immediate from the universal property of the limit in $C$. For let $t \to Q$ be another cone over $F$ in $t/C$, then $Q$ is another cone over $p F$ in $C$ and we get in $C$ a universal morphism $Q \to \lim p F$

$$
  \array{
    && t
    \\
    & \swarrow & \downarrow & \searrow
    \\
    && Q
    \\
    \downarrow & \swarrow &\downarrow & \searrow & \downarrow
    \\
    && \lim p F
    \\
    \downarrow & \swarrow && \searrow & \downarrow
    \\
    p F(d) &&\stackrel{p F(\gamma)}{\to}&& p F(d') 
  }
$$


A glance at the diagram above shows that
the composite $t \to Q \to \lim p F$ constitutes a morphism
of cones in $C$ into the limiting cone over $p F$. Hence it must equal our morphism $t \to \lim p F$, by the universal property of $\lim p F$, and hence the above diagram does commute as indicated.

This shows that the morphism $Q \to \lim p F$
which was the unique one giving a cone morphism on $C$ does lift to a
cone morphism in $t/C$, which is then necessarily unique, too.  This demonstrates the required universal property of $t \to \lim p F$ and 
thus identifies it with $\lim F$.


=--

* Remark: One often says "$p$ reflects limits" to express the conclusion of this proposition. A conceptual way to consider this result is by appeal to a more general one: if $U: A \to C$ is [[monadic functor|monadic]] (i.e., has a left adjoint $F$ such that the canonical [[comparison functor]] $A \to (U F)\text{-}Alg$ is an [[equivalence of categories|equivalence]]), then $U$ both reflects and preserves limits. In the present case, the projection $p: A = t/C \to C$ is monadic, is essentially the category of algebras for the monad $T(-) = t + (-)$, at least if $C$ admits binary coproducts. (Added later: the proof is even simpler: if $U: A \to C$ is the underlying functor for the category of algebras of an _endofunctor_ on $C$ (as opposed to algebras of a monad), then $U$ reflects and preserves limits; then apply this to the endofunctor $T$ above.) 










## Further resources

Pedagogical vidoes that explain limits and colimits are at

* [[The Catsters]], [General Limits and Colimits](http://www.youtube.com/watch?v=g47V6qxKQNU)






