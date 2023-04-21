
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea 
 {#Idea}

A _Reedy model structure_ is a [[global model structure on functors]]:

given a [[Reedy category]] $R$ and a [[model category]] $C$ the **Reedy model structure** is a [[model category]] structure on the [[functor category]] $[R,C] = Func(R,C)$.

As opposed to the [[global model structure on functors|projective and injective model structure]] on functors this does not require any further structure on $C$, but instead makes a strong assumption on $R$.

If all three exist, then, in a precise sense, the Reedy model structure sits _in between_ the injective and the projective model structure. As such, it has the advantage that _both_ the cofibrations as well as the fibrations can be fairly explicitly described and detected in terms of cofibrations and fibrations in $C$. 


## Definition
 {#Definition}

### Plain version
 {#PlainVersion}

For

* $\mathcal{R}$ a [[Reedy category]] 

* $\mathcal{C}$ a [[model category]].

consider 

* the [[functor category]] $\mathcal{C}^\mathcal{R}$ 

  whose [[objects]] $X \colon \mathcal{R} \to \mathcal{C}$ we refer to as ($\mathcal{R}$-shaped) *[[diagrams]]* in $\mathcal{C}$.

\begin{definition}\label{LatchingAndMatchingObjects}
**(latching and matching objects)**
\linebreak
Given 

1. a [[diagram]] $X \colon \mathcal{R} \to \mathcal{C}$,

2. an [[object]] $ r \in \mathcal{R}$

then:

The **latching object** of $X$ at stage $r$ is the [[colimit]] 

\[
  \label{LatchingObject}
  L_r X 
  \;\coloneqq\;
  \underset{
    s \underset{+}{\to} r
  }{colim} 
  X_s
\]

over the [[full subcategory]] of the [[slice category]] $R_+/r$ containing all objects except the [[identity morphism|identity]] $id_r$.  

[[formal duality|Dually]]:

The **matching object** of $X$ at stage $r$ is the [[limit]]

\[
  \label{MatchingObject}
  M_r X 
  \;\coloneqq\;
  \underset{
    r \underset{-}{\to} s }
  {\lim}
  X_s
  \,,
\]

over the [[full subcategory]] of the [[coslice category]] $r/R_-$ containing all objects except $id_r$.  

By the [[universal property]] of ([[colimit|co]])[[limits]] there are evident [[natural transformations]]:

\[
  \label{ComparisonMapsFromLatchingToMatchingObject}
  L_r X
  \longrightarrow 
  X_r 
  \longrightarrow 
  M_r X
  \,.
\]
\end{definition}
(e.g. [Hovey (1999), Def. 5.2.2](#Hovey99); [Hirschhorn (2002), Def. 15.2.5](#Hirschhorn02))


\begin{example}\label{LatchingOfSimplicialObjects}
**(latching of simplicial objects)**
\linebreak
Consider the case that $\mathcal{R} = \Delta^{op}$ is the [[opposite category|opposite]] [[simplex category]] with its canonical Reedy structure ([here](Reedy+category#ReedyStructureOnSimplexCategory)), where $(\Delta^{op})_+ \,=\, (\Delta_-)^{op}$ is the opposite of the [[surjections]] $[r] \to [r-k]$.

For $X \colon \Delta^{op} \to \mathcal{C}$ a [[simplicial object]], its value on such a morphism is the corresponding [[degeneracy map]].

This means that the [[cocone]] morphism (eq:ComparisonMapsFromLatchingToMatchingObject) out of the the latching object (eq:LatchingObject) has as components in degree $r$ all [inclusions of degenerate simplices](simplicial+identities#DegeneracyMapsAreSplitMono) 
$$
  X_{r-k} \overset{\phantom{--}}{\hookrightarrow} X_r
$$
which $X_r$ receives.

Hence one may often think of the latching object $L_r X$ of a [[simplicial object]] $X$ as the object of _degenerate_ [[n-simplex|$r$-simplices]] sitting inside the object $X_r$ of all $r$-simplices. Cf. Prop. \ref{EveryBisimplicialSetIsReedyCofibrant} and Prop. \ref{LatchingInAbelianCategoryIsDegeneracySubobject} below.
\end{example}

\begin{remark}
Notice that $L_0 X = 0$ is the [[initial object]] and $M_0 X$ is the [[terminal object]], since there are no objects of degree $\lt 0$.
\end{remark}


\begin{example}
When $\mathcal{R} = \alpha$ is an [[ordinal]] (regarded as a [[poset]] and thus as a [[category]]), then $L_{n+1} X = X_n$ and $M_n X = 1$; and dually for $\mathcal{R}=\alpha^{op}$.
\end{example}

\begin{definition}\label{ReedyModelStructure}
A [[morphism]] $f \colon X \to Y$ in the [[functor category]] $\mathcal{C}^{\mathcal{R}}$ (hence a [[natural transformation]] between [[diagrams]]) is called:

* a *Reedy equivalence* if each component morphism $f_r$ is a [[weak equivalence]] in $\mathcal{C}$;

* a *Reedy-cofibration* or *acyclic Reedy-cofibration* if for all $r \in \mathcal{R}$, the map 

  $$
    L_r Y 
     \overset
       {L_r X}
       {\amalg}
    X_r 
      \longrightarrow
    Y_r
  $$

  is a [[cofibration]] or [[acyclic cofibration]] in $\mathcal{C}$, respectively;

* a *Reedy-fibration* or *acyclic Reedy-fibration* if for all $r \in \mathcal{R}$, the map

  $$ 
    X_r 
     \longrightarrow 
    M_r X 
     \underset
     {M_r Y}
     {\times} 
    Y_r
  $$

  is a [[fibration]] or [[acyclic fibration]] in $\mathcal{C}$, respectively.  

\end{definition}
(e.g. [Hirschhorn (2002), Def. 15.3.3](#Hirschhorn02))

\begin{proposition}\label{model}
**(Reedy model structure)**
\linebreak
The classes of morphisms in Def. \ref{ReedyModelStructure} consistute a [[model category]]-[[structure]] on the [[functor category]] $\mathcal{C}^{\mathcal{R}}$, called the *Reedy model structure*.
\end{proposition}
(e.g. [Hovey (1999), Thm. 5.2.5](#Hovey99); [Hirschhorn (2002), Thm 15.3.4](#Hirschhorn02))

\begin{remark}
To see the factorization of a morphism $f \colon X\to Y$ in either of the two necessary ways, construct the factorization $f_r = g_r h_r$ inductively on $r$, by factoring the induced morphism
$$ L_r Z \amalg_{L_r X} X_r \to M_r Z \times_{M_r Y} Y_r$$
in the appropriate way in $\mathcal{C}$.
\end{remark}


### Enriched version

For $V$ a [[cosmos|suitable enriching category]], there is a refinement of the notion of Reedy category to a notion of _$V$-[[enriched Reedy category]]_ such that if $C$ is a $V$-[[enriched model category]] -- in particular when it is a [[simplicial model category]] for $V = $ [[SSet]] -- the [[enriched functor category]] $[R,C]$ is itself a $V$-[[enriched model category]] (see [Angeltveit](#Angeltveit)). 



In the case that we do have extra assumptions on the codomain in that

* $C$ is a [[combinatorial simplicial model category]] 

* with  $C^\circ$ the [[(∞,1)-category]] [[presentable (∞,1)-category|presented]] by $C$ 

* and with the [[Reedy category]] $R$ an ordinary category regarded as a [[SSet]]-[[enriched category]], 

the Reedy model structure, having the same weak equivalences as the [[global model structure on functors]], presents similarly the [[(∞,1)-category of (∞,1)-functors]] $Func_\infty(R,C^\circ)$, from $R$ into the [[(∞,1)-category]] [[presentable (∞,1)-category|presented by]] $C$.


## Remarks

* Any Reedy cofibration or fibration is, in particular, an objectwise one, but the converse does not generally hold.

* An object $X$ is Reedy cofibrant if and only if each map $L_r X \to X_r$ is a cofibration in $M$.  In particular, this implies that each $X_r$ is cofibrant in $M$.

* For some $M$, $M^R$ also admits a [[projective model structure|projective]] or [[injective model structure|injective]] model structures.  For instance for $M = $ [[SSet]] this is the [[global model structure on simplicial presheaves]]. 

  In general the Reedy structure will not be the same as either, but will be a kind of mixture of both. If $R = R_+$ then the Reedy model structure coincides with the [[projective model structure]], if $R = R_-$ it coincides with the [[injective model structure]].

  For a detailed comparison of Reedy and global projective/injective model structures see around example A.2.9.22 in [[Higher Topos Theory|HTT]].

* In addition to its existing for all $C$, another advantage of the Reedy structure is the explicit nature of its cofibrations, fibrations, and factorizations.

* If $R$ admits more than one structure of Reedy category, then $C^R$ will have more than one Reedy model structure.  For instance, if $R = (\cdot\to\cdot)$ is the [[walking arrow]], then we can regard it as either the ordinal $2$ or its opposite $2^{op}$, resulting in two different Reedy model structures on $C^2$.

* For a general Reedy category $R$, the diagonal functor $\Delta : C\to C^R$ need not be either a right or a left [[Quillen adjunction|Quillen functor]] (although, of course, it has left and right adjoints given by colimits and limits over $R$).  $\Delta$ is a left Quillen functor if and only if for all objects $r$, the category $r / R_-$ is either connected or empty.  Dually, $\Delta$ is a right Quillen functor if and only if for all objects $r$, the category $R_+ / r$ is empty or connected.  In these cases, one can construct [[homotopy limit|homotopy limits]] and colimits using the derived functors of the Quillen adjunctions $\mathrm{colim} \dashv \Delta \dashv \mathrm{lim}$.

## Properties 
  {#Properties}

### Combinatorial structure

\begin{proposition}
\label{ReedyStructureCofibrantlyGenerated}
  If $\mathcal{C}$ is a [[cofibrantly generated model category]] then also the Reedy model structure on $\mathcal{C}^{\mathcal{R}}$ is cofibrantly generated.
\end{proposition}
&lbrack;[Hirschhorn (2002), Theorem 15.6.27](#Hirschorn02)&rbrack;

(assuming that [[domains]] of generating (acyclic) cofibrations are relatively [[small objects]])

### Enriched model structure
 {#EnrichedModelStructure}

+-- {: .num_prop }
###### Proposition

For $C$ a [[Reedy category]] and $A$ a [[symmetric monoidal category|symmetric]] [[monoidal model category]], the Reedy model structure on $[C,A]_{Reedy}$ is naturally an $A$-[[enriched model category]].

If in addition $A$ is a $V$-[[enriched model category]] for some symmetric monoidal model category $V$, then so is $[C,A]_{Reedy}$

=--

This appears as ([Barwick, lemma 4.2, corollary 4.3](#Barwick)).

(...check assumptions...)


### Relation to other model structures

+-- {: .num_prop }
###### Proposition

Let $C$ be a [[combinatorial model category]] and $R$ a [[Reedy category]].


The identity functors provide left [[Quillen equivalences]]

$$
  [R,C]_{proj} \stackrel{\simeq_{Quillen}}{\to}
  [R,C]_{Reedy}
  \stackrel{\simeq_{Quillen}}{\to}
  [R,C]_{inj}
$$

from the projective [[model structure on functors]] to the injective one.

=--

See also [[Higher Topos Theory|HTT, remark A.2.9.23]]



## Examples 

### Over the arrow category 

The simplest nontrivial example is obtained for 

$$
  R = I = \{1 \to 0\}
$$ 

the [[interval category]]. 

In this case the [[functor category]] $[I,C]$ is the [[arrow category]] $C$.

We take the degree on the objects to be as indicated. Then $R_- = R$ and $R_+$ contains only the identity morphisms.

For $F : I \to C$ a functor, i.e. a morphism $F(1) \to F(0)$ in $C$, we find  


* the latching object $latch_0 F = colim_{(s \stackrel{+}{\to} 0)} F(s) = \emptyset$;

* the latching object 
  $latch_1 F = colim_{(s\stackrel{+}{\to}1)} F(s) = \emptyset$;

* the matching object $match_0 F = lim_{(0 \stackrel{-}{\to}s)} F(s) = {*}$;

* the matching object $match_1 F = lim_{(1 \stackrel{-}{\to}s)} F(s) = F(0)$

where $\emptyset$ denotes the [[initial object]] and ${*}$ the [[terminal object]] (being the [[colimit]] and [[limit]] over the empty [[diagram]],  respectively).

From this we find that for a [[natural transformation]] $\eta : F \to G$

  $$
    \array{
      F(1) &\stackrel{\eta_1}{\to}& G(1)
      \\
      \downarrow && \downarrow
      \\
      F(0) &\stackrel{\eta_0}{\to}& G(0)
    }
  $$

that 

* it is a Reedy cofibration in $[I,C]$ if

  * $\eta_0 : F(0) \coprod_{\emptyset} \emptyset = F(0) \to G(0)$ is a cofibration

  and

  * $\eta_1 : F(1) \coprod_{\emptyset} \emptyset = F(1) \to G(1)$ is a cofibration


* it is a Reedy fibration in $[I,C]$ if

  * $\eta_0 : F(0) \to G(0) \times_{*} {*} = G(0)$ is a fibration

  * the universal morphism $F(1) \to G(1) \times_{G(0)} F(0)$ 
   
    $$
    \array{
      F(1)
      \\
      & \searrow
      \\
      && F(0) \times_{G(0)} G(1) 
      &\to& G(1)
      \\
      && \downarrow && \downarrow
      \\
      && F(0) &\stackrel{\eta_0}{\to}& G(0)
    }
    $$

    is a fibration.

  Notice that since fibrations are preserved by pullbacks and under composition with themselves, it follows that also $\eta_1 : F(1) \to G(1)$ is a fibration.

* The cofibrant objects in $[I,C]$ are those arrows $F(1) \to F(0)$ in $C$ for which $F(1)$ and $F(0)$ are cofibrant;

* The fibrant objects in $[I,C]$ are those arrows $F(1) \to F(0)$ in $C$ that are fibrations between fibrant objects in $C$.

So in accord with the proposition above one finds that this Reedy model structure on $[I,C]$ coincides with the _injective_ [[global model structure on functors]] on $I$.


### Over the tower category 
 {#OverTheTowerCategory}

Let $R = \mathbb{N}^{op} = \{\cdots \to 2 \to 1 \to 0\}$ be the natural numbers regarded as a [[poset]] using the greater-than  relation.

With the degree as indicated, this is a Reedy category with $R_- = R$ and $R_+$ containing only identity morphisms.

Now the [[functor category]] $[R,C]$ is the category of _towers_ of morphisms in $C$. 

The analysis of the Reedy model structure on this involves just a repetition of the steps involved in the analysis of the arrow category in the above example. One finds:

* a natural transformation $\eta : F \to G$ is a fibration precisely if

  * the component $\eta_0 : F(0) \to G(0)$ is a fibration

  * all universal morphisms $F(n) \to F(n-1) \times_{G(n-1)} G(n)$ are fibrations.

* the fibrant objects are the towers of fibrations on fibrant objects in $C$.

A detailed discussion of the model structure on towers is for instance in ([GoerssJardine, chapter 6](#GoerssJardine))

By duality it follows that analogously there is a model structure on co-towers

$$
  X_0 \to X_1 \to X_2 \to \cdots
$$

in a model category $C$, whose fibrations and weak equivalences are the degreewise ones, and whose cofibrations are those transformations that are a cofibration in degree 0 and where the canonical pushout-morphisms in each square are cofibrations.

### Over the simplex category 
  {#SimplexCategory}

The motivating and central example of [[Reedy categories]] is the 
[[simplex category]] $\Delta$.

Recall that

* a map $[k] \to [n]$ is in $\Delta_+$ precisely if it is an injection;

* a map $[n] \to [k]$ is in $\Delta_-$ precisely if it is a surjection.

Dually, for the [[opposite category]] $\Delta^{op}$

* a morphism $[n] \leftarrow [k]$ is in $(\Delta^{op})_-$ precisely if the map underlying it is an injection;

* a morphism $[k] \leftarrow [n]$ is in $(\Delta^{op})_+$ precisely if the map underlying it is a surjection.


Let $C = sSet_{Quillen}$ be the category [[sSet]] equipped with the standard [[model structure on simplicial sets]] and consider the Reedy model structures on $[\Delta^{op}, sSet_{Quillen}]$ $[\Delta,sSet_{Quillen}]$. 


#### With values in simplicial sets
  {#OverDeltaWithValuesInSimplicialSets}

+-- {: .num_prop}
###### Proposition

For $X  \in [\Delta^{op},Set]$ a [[simplicial object]]
and $n \in \mathbb{N}$,

* the [[latching object]] $L_n X$ is the [[union]] of all degenerate $n$-cells;

* the [[matching object]] is $M_n X \simeq X^{\partial \Delta[n]}$, the [[powering]] of the [[boundary of a simplex|boundary of the n-simplex]] into $X$, hence the $n$-cells of the $(n-1)$-[[skeleton]] of $X$.

=--

More details on this are currently at _[[generalized Reedy model structure]]_. 

\begin{proposition}\label{EveryBisimplicialSetIsReedyCofibrant}
If $\mathcal{C} = sSet$ is the [[classical model structure on simplicial sets]], then every object in $[\Delta^{op}, \mathcal{C}]_{Reedy}$ (i.e. every [[bisimplicial sets]]) is Reedy-cofibrant. 
\end{proposition}

([Hirschhorn (2002), corollary 15.8.8](#Hirschhorn02))

The idea is to observe that the latching objects are the [[sub-objects]] of degeenrate cells, so that the comparison morphism (eq:ComparisonMapsFromLatchingToMatchingObject) is a [[monomorphism]] and hence a [[cofibration]] in the [[classical model structure on simplicial sets]].

Similarly:

+-- {: .num_prop}
###### Proposition

The canonical cosimplicial simplicial set

$$
  \Delta[-] : \Delta \to sSet
$$

is Reedy cofibrant in $[\Delta,sSet_{Quillen}]$.

=--

+-- {: .proof}
###### Proof

The latching object at $n$ is

$$
  L_n(\Delta[-]) = 
  \lim_\to
  \left(
    ([k] \to [n]\; inj.\in\;\Delta) \mapsto
    \Delta[k]
  \right)
  \,.
$$

This is $\partial \Delta[n]$. The inclusion $\partial \Delta[n] \to \Delta[n]$ is a monomorphism, hence a cofibration in $sSet_{Quillen}$ (in fact these are the generating cofibrations).


=--


+-- {: .num_cor}
###### Corollary

Every [[simplicial set]] is the [[homotopy colimit]] over its diagram of simplices (with values in the constant simplicial set on the sets of simplicies $X_n$):

$$
  X \simeq hocolim ( [n] \mapsto const X_n)
  \,.
$$

=--

+-- {: .proof}
###### Proof

Because $X_{(-)} : \Delta^{op} \to sSet$ is Reedy cofibrant by the above, by the discussion at [[homotopy colimit]] we can compute the hocolim by the [[coend]]

$$
  \int^{[n]} Q(*)_n \cdot X_n
  \,,
$$

where $Q(*) : \Delta \to sSet$ is a cofibrant [[resolution]] of the point in $[\Delta, sSet_{Quillen}]_{Reedy}$. Using the above observation, we can take this to be $\Delta[-]$ since this is cofibrant by the above observation and clearly $\Delta[-] \to *$ is objectwise a weak equivalence in $sSet_{Quillen}$.

Therefore the hocolim is (up to equivalence) represented by the simplicial set

$$
  \int^{[n]} \Delta[n] \cdot X_n
  \,.
$$

But by the [[co-Yoneda lemma]] this is in fact [[isomorphism|isomorphic]] to $X$, hence in particular weakly equivalent to $X$.

=--

+-- {: .num_remark}
###### Remark

This kind of argument has many immediate generalizations. For instance for $C = [K^{op}, sSet_{Quillen}]_{inj}$ the injective [[model structure on simplicial presheaves]] over any small category $K$, or any of its left [[Bousfield localization of model categories|Bousfield localizations]], we have that the cofibrations are objectwise those of simplicial sets, hence objectwise monomorphisms, hence it follows that every simplicial presheaf $X$ is the hocolim over its simplicial diagram of component presheaves.

=--

For the following write $\mathbf{\Delta} : \Delta \to sSet$ for the [[fat simplex]].  

+-- {: .num_prop}
###### Proposition

The fat simplex is Reedy cofibrant.

=--


+-- {: .proof}
###### Proof

By the discussion at [[homotopy colimit]], the fat simplex is cofibrant in the projective [[model structure on functors]] $[\Delta, sSet_{Quillen}]_{proj}$. By the [general properties](#Properties) of Reedy model structures, the identity functor $[\Delta, sSet_{Quillen}]_{proj} \to [\Delta, sSet_{Quillen}]_{Reedy}$ is a [[Quillen adjunction|left Quillen functor]], hence preserves cofibrant objects.

=--

#### With values in an addive model category
 {#WithValuesInAnAbelianCategory}

In this section, let $\mathcal{A}$ be an [[additive category|additive]] [[model category]] in which all [[retractions]] exhibit [[direct sums]] (such as in an [[abelian category]], such as in a [[model structure on chain complexes]]).

In this situaiton the [[Dold-Kan correspondence]] applies (see [there](Dold-Kan+correspondence#StatementAdditiveACase)) and can be used to get further information about the Reedy model structure on the category $s\mathcal{A} \coloneqq \mathcal{A}^{(\Delta^{op})}$ of [[simplicial objects]] in $\mathcal{A}$.

\begin{proposition}
  \label{LatchingInAbelianCategoryIsDegeneracySubobject}
Under the above assumptions, for any [[simplicial object]] $X_\bullet \in s\mathcal{A}$ and all $n \in \mathbb{N}$, the comparison morphism (eq:ComparisonMapsFromLatchingToMatchingObject) from the $n$th latching object (Def. \ref{LatchingAndMatchingObjects}) of $X_\bullet$ is a ([[split monomorphism|split]]) [[monomorphism]]:

$$
  L_n X \xhookrightarrow{\phantom{---}} X_n
  \,.
$$
\end{proposition}
This and the following proof spells out a suggestion by [[Charles Rezk]] in [MO:a/300657](https://mathoverflow.net/a/300657/381).
\begin{proof}
  Under the given assumption on $\mathcal{A}$ the [[Dold-Kan correspondence]] applies (see [there](Dold-Kan+correspondence#StatementAdditiveACase)) to [[simplicial objects]] in $\mathcal{A}$ and says that, up to [[isomorphism]], $X_\bullet$ is of the form $X_\bullet \simeq \Gamma(V_\bullet)$ for some [[connective chain complex]] $V_\bullet$ (in fact $V_\bullet \simeq N X_\bullet$ is the [[normalized chain complex]] of $X_\bullet$, but we don't even need this), in that each $X_r$ is the [[direct sum]] of one copy of $V_s$ for each [[surjection]] $[r] \twoheadrightarrow [s]$ in [[simplex category|$\Delta$]] (by [this Prop.](Dold-Kan+correspondence#ExplicitFormOfGamma)):

$$
  X_r 
  \;\simeq\;
  \underset
    {[r] \twoheadrightarrow [s]}
    {\bigoplus}
  V_s
  \;\simeq\;
  \left(
  \underset
    {
      {[r] \overset{p}{\twoheadrightarrow} [s]}
      \atop
      p \neq id_{[r]}
    }
    {\bigoplus}
  V_s
  \right)
  \,\oplus\,
  V_r
  \,.
$$
(On the right we have split off the summand corresponding to the [[identity morphism]], just for emphasis, since this is what matters in a moment).

Moreover (still by [this Prop.](Dold-Kan+correspondence#ExplicitFormOfGamma)), under this identification the [[degeneracy maps]] $X_{[r'] \overset{p}{\twoheadrightarrow} [r]}$ of $X_\bullet$ are simply given on these [[direct sum|direct summands]] by precomposition of their labels with $p$:
$$
  \array{
    X_{r} 
    &
    \overset{X_{[r'] \overset{p}{\twoheadrightarrow} [r]} }{\longrightarrow}
    &
    X_{r'}
    \\
    \big(
      [r] \overset{q}{\twoheadrightarrow} [s]
      ,\,
      v \in V_s
    \big)
    &\mapsto&
    \big(
      [r'] \overset{q \circ p}{\twoheadrightarrow} [s]
      ,\,
      v \in V_s
    \big)
  }
$$

We claim (argument below) that this implies that the colimit defining $L_r X$ consists of [[equivalence classes]] of triples of the form 
$
\Big(  
    [r] 
      \overset{p}{\twoheadrightarrow} 
    [r'] 
      \overset{q}{\twoheadrightarrow}
    [s]
   ,\,
  v \in V_s 
  \Big)
$
for non-identity $p$,
under the [[equivalence relation]] which identifies $(p,q,v)$ with $(p'q',v')$ iff $p \circ q \,=\, p' \circ q'$ and $v = v'$. This will mean that the equivalence classes are simply labeled by pairs $\big([r] {\twoheadrightarrow} [s] ,\,  v \in V_s\big)$ where the surjection is non-identity, hence that the colimit is
$$
  L_r X
  \;\coloneqq\;
  \underset{
    \underset
      {
        { p \colon [r] \twoheadrightarrow [s] }
        \atop
        { p \neq id }
      }
      {\longrightarrow}
  }{\lim}
  X_s
  \;\simeq\;
  \underset{
      {
        { p \colon [r] \twoheadrightarrow [s] }
        \atop
        { p \neq id }
      }
  }{\bigoplus}
  V_s
$$
and that the comparison map $L_r X \to X_r$ is the canonical inclusion of all the non-identity [[direct summands]]:
$$
  L_r X 
  \xhookrightarrow{\phantom{--}}
  L_r X \,\oplus\, V_r
  \;\simeq\;
  X_\bullet
  \,,  
$$
which proves the proposition.

Hence it remains to show the claim about the colimit. For that it is sufficient to observe that whenever we have a [[commuting diagram]] in [[simplex category|$\Delta$]] of the form

\begin{tikzcd}[sep=20pt]
    & 
    {[r]}
    \ar[dl,->>, "{p}"{swap}]
    \ar[dr,->>, "{p'}"]
    \\
    {[s]} 
    \ar[dr,->>, "{q}"{swap}]
    &
    & 
    {[s']}
    \ar[dl,->>, "{q'}"]
    \\
    &
    {[t]}
\end{tikzcd}

we may equivalently factor it as a [[zig-zag]] of diagrams 

\begin{tikzcd}[sep=20pt]
    & 
    {[r]}
    \ar[dl,->>, "{p}"{swap}]
    \ar[dr,->>, "{p'}"]
    \ar[d, ->>]
    \\
    {[s]} 
    \ar[dr,->>, "{q}"{swap}]
    &
    {[t]}
    \ar[d, equals]
    \ar[from=r, ->>]
    \ar[from=l, ->>]
    & 
    {[s']}
    \ar[dl,->>, "{q'}"]
    \\
    &
    {[t]}
\end{tikzcd}

because the left half of this zig-zag is

\begin{tikzcd}[sep=20pt]
    & 
    {[r]}
    \ar[dl,->>, "{ p  }"{swap}]
    \ar[dr,->>, "{ q \,\circ\, p }"]
    \\
    {[s]} 
    \ar[dr,->>, "{q}"{swap}]
    \ar[rr, ->>, "{q}"{description}]
    &
    & 
    {[t]}
    \ar[dl,->>, "{\mathrm{id}}"]
    \\
    &
    {[t]}
\end{tikzcd}

and exhibits that, in the colimit, $(p,q,v)$ is identified with $(q\circ p, id, v) \,=\, (q' \circ p', id, v)$; while, analogously, the right half shows that this in turn is identified with $(p',q',v)$.
\end{proof}

\begin{proposition}
 For $\mathcal{A}$ an [[additive category|additive]] [[model category]] as above, if a [[morphisms]] $f_\bullet \colon X_\bullet \to Y_\bullet$ of [[simplicial objects]] in $\mathcal{A}$ is Reedy cofibrant (Def. \ref{ReedyModelStructure}) then the morphism $N f_\bullet$ of [[normalized chain complexes]] corresponding to it under the [[Dold-Kan correspondence]] is, as a [[chain map]], degreewise a [[cofibration]] in $\mathcal{A}$.
\end{proposition}
\begin{proof}
Recall (from [here](Moore+complex#SplittingOffDegenerateCells)) that the components of the [[normalized chain complex]] $N X_\bullet$ of $X_\bullet$ in any degree $r \in \mathbb{N}$ are [[isomorphism|isomorphically]], the [[quotient]] of $X_r$ by the subgroup of degenerate cells. By Prop. \ref{LatchingInAbelianCategoryIsDegeneracySubobject} that subgroup is equivalently the [[latching object]] in that degree, so that we have [[natural isomorphisms]]
\[
  \label{NormalizedChainAsQuotientByLatching}
  (N X)_r \;\simeq\; X_r/L_r X
  \,.
\]
 
Now consider the following [[commuting diagram]] in $\mathcal{A}$:
$$
  \array{
    L_r X 
      &\longrightarrow& 
    X_r
    \\
    \big\downarrow 
      && 
    \big\downarrow 
      & 
    \searrow\mathrlap{{}^{f_r}}
    \\
    L_r Y 
      & \longrightarrow & 
    L_r Y \overset{L_r X}{\sqcup} X_r 
      & \underset{\in Cof}{\longrightarrow} & 
    Y_r
    \\
    \big\downarrow 
      && 
    \big\downarrow 
      && 
    \big\downarrow
    \\
    0 
      &\longrightarrow& 
    X_r / L_r X 
      &\underset{(N f)_r}{\longrightarrow}& 
    Y_r/L_r Y
  }
$$
Here the top square, the left rectangle and the bottom rectagle are [[pushouts]] by definition of the latching object (Def. \ref{LatchingAndMatchingObjects}) and by the characterization (eq:NormalizedChainAsQuotientByLatching) of normalized chains.
Therefore the [[pasting law]] implies first that the left bottom square and then that the right bottom square is a pushout. 

This exhibits $(N f)_r$ as the pushout of a cofibration, and hence as a cofibration itself.
\end{proof}


#### With values in an arbitrary model category

Let $C$ be a [[model category]].

+-- {: .num_prop}
###### Corollary

For $X \in [\Delta^{op}, C]$ a Reedy cofibrant object, the [[Bousfield-Kan map]]

$$
  \int^{[n]} \mathbf{\Delta}[n] \cdot X_n
  \to
  \int^{[n]} \Delta[n] \cdot X_n  
$$

is a weak equivalence in $C$.

=--

+-- {: .proof}
###### Proof

The [[coend]] over the [[copower|tensor]] is a left [[Quillen bifunctor]]

$$
  \int (-)\cdot (-) : [\Delta,sSet_{Quillen}]_{Reedy} \times
    [\Delta^{op}, C]_{Reedy}
$$

(as discussed there). Therefore with its second argument fixed and cofibrant it is a [[Quillen adjunction|left Quillen functor]] in the remaining argument. As such, it preserves weak equivalences between cofibrant objects (by the [[factorization lemma]]). By the [above discussion](#OverDeltaWithValuesInSimplicialSets), both $\mathbf{\Delta}[n]$ and $\Delta[-]$ are indeed cofibrant in $[\Delta,sSet_{Quillen}]_{Reedy}$. Clearly the functor $\mathbf{\Delta}[-] \to \Delta[-]$ is objectwise a weak equivalence in $sSet_{Quillen}$, hence is a weak equivalence.

=--

#### Enrichment
 {#EnrichmentOverTheSimplexCategory}

The following proposition should be read as a **warning** that 
an obvious idea about simplicial enrichment of Reedy model
structures over the simplex category does _not_ work.

+-- {: .num_prop}
###### Proposition

For $C$ a [[model category]], the [[category of simplicial objects]] $[\Delta^{op}, C]$ in $C$ is canonically an [[sSet]]-[[enriched category]]. 

However, this does **not** in general harmonize with the Reedy model structure to make $[\Delta^{op}, C]_{Reedy}$ a [[simplicial model category]].

More precisely the following parts of the [[pushout-product axiom]] for the $sSet$-[[tensoring]] hold. Let $f : A \to B$ be a cofibration in $[\Delta^{op}, C]_{Reedy}$ and $s : S \to T$ be a cofibration in $sSet_{Quillen}$.

1. the [[pushout-product]] $f \bar \otimes g$ is a cofibration in $[\Delta^{op}, C]_{Reedy}$ ;

1. and it is an acyclic cofibration if $f$ is;

1. it is **not necessarily** acyclic if $s$ is.

=--

That the first two items do hold is discussed for instance as ([Dugger, prop. 4.4](#Dugger)). A counterexample for the third item is in ([Dugger, remark 4.6](#Dugger)).

+-- {: .num_remark}
###### Remark

However, there are [[Bousfield localization of model categories|left Bousfield localizations]] of $[\Delta^{op}, sSet]_{Reedy}$ for which

1. the above $sSet$-enrichment does constitute an $sSet$-[[enriched model category]];

1. the result model structure is Quillen equivalent to $C$ itself.

This is in fact a useful technique for replacing $C$ by a Quillen equivalent
and $sSet$-enriched model structure. More discussion of this point is
at _[[simplicial model category]]_ in the section
_[Simplicial Quillen equivalent models](simplicial+model+category#SimpEquivMods)_.

=--

## Related concepts

* [[generalized Reedy model structure]]

* [[Joyal-Tierney calculus]]

## References 

The original text is

* [[Chris Reedy]], _Homotopy Theory of Model Categories_  ([retyped pdf](http://www-math.mit.edu/~psh/reedy.pdf))

A quick review is in section A.2.9 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ .

Textbook accounts:

* {#Hovey99} [[Mark Hovey]], Section 5.2 of: *[[Model Categories]]*, Mathematical Surveys and Monographs, **63** AMS (1999) &lbrack;[ISBN:978-0-8218-4361-1](https://bookstore.ams.org/surv-63-s), [doi:10.1090/surv/063](https://doi.org/http://dx.doi.org/10.1090/surv/063), [pdf](https://people.math.rochester.edu/faculty/doug/otherpapers/hovey-model-cats.pdf), [Google books](http://books.google.co.uk/books?id=Kfs4uuiTXN0C&printsec=frontcover)&rbrack;

* {#Hirschhorn02} [[Philip Hirschhorn]], Chapter 15 of: _[[Model Categories and Their Localizations]]_, AMS Math. Survey and Monographs Vol 99 (2002) &lbrack;[ISBN:978-0-8218-4917-0](https://bookstore.ams.org/surv-99-s/), [pdf toc](http://www.gbv.de/dms/goettingen/360115845.pdf), [pdf](http://www.maths.ed.ac.uk/~aar/papers/hirschhornloc.pdf)&rbrack;

An overview stressing the role of [[weighted colimit|weighted colimits]] is in

* [[Emily Riehl]], [[Dominic Verity]], _The theory and practice of Reedy categories_, Theory and Applications of Categories **29** no.9 (2014) pp. 256-301. ([abstract](http://www.tac.mta.ca/tac/volumes/29/9/29-09abs.html))

A textbook account is in 

* {#Hirschhorn02} [[Philip Hirschhorn]], chapter 15 of _Model Categories and Their Localizations_, AMS Math. Survey and Monographs Vol 99 (2002) ([AMS](http://www.ams.org/bookstore?fn=20&arg1=whatsnew&item=SURV-99), [pdf toc](http://www.gbv.de/dms/goettingen/360115845.pdf), [pdf](http://www.maths.ed.ac.uk/~aar/papers/hirschhornloc.pdf))

Discussion of functoriality of Reedy model structures is in 

* {#Barwick} [[Clark Barwick]], _On Reedy Model Categories_ ([arXiv:0708.2832](http://arxiv.org/abs/0708.2832))
 

The discussion of enriched Reedy model structures is in

* {#Angeltveit} Vigleik Angeltveit, _Enriched Reedy categories_ ([arXiv](http://arxiv.org/abs/math/0612137))
 

The main statement is theorem 4.7 there.


The Reedy model structure on towers is discussed for instance in chapter 6 of 

* {#GoerssJardine} [[Paul Goerss]], [[Rick Jardine]], _[[Simplicial homotopy theory]]_ ([dvi](http://www.maths.abdn.ac.uk/~bensondj/html/archive/goerss-jardine.html) [PDF](http://dodo.pdmi.ras.ru/~topology/books/goerss-jardine.pdf)) 

The Reedy model structure on categories of simplicial objects is discussed in more detail for instance in 

* {#Dugger} [[Dan Dugger]], _Replacing model categories with simplicial ones_, Trans. Amer. Math. Soc. vol. 353, number 12 (2001), 5003-5027. ([pdf](https://www.ams.org/journals/tran/2001-353-12/S0002-9947-01-02661-7/S0002-9947-01-02661-7.pdf)) 
  
Monoidal Reedy model structures are discussed in

* Moncef Ghazel, Fethi Kadhi, _Reedy diagrams in V-model categories_, [arXiv:1610.06535](https://arxiv.org/abs/1610.06535), [doi:10.1007/s10485-019-09566-w](https://doi.org/10.1007/s10485-019-09566-w).



[[!redirects Reedy model category]]
[[!redirects Reedy model categories]]

[[!redirects latching object]]
[[!redirects latching objects]]
[[!redirects matching object]]
[[!redirects matching objects]]
[[!redirects latching map]]
[[!redirects latching maps]]
[[!redirects matching map]]
[[!redirects matching maps]]

[[!redirects Reedy model structures]]
