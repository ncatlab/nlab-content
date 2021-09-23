
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# The separation axioms
* table of contents
{: toc}

## Idea
 {#Idea}

The plain definition of _[[topological space]]_ happens to allow examples where distinct points or distinct subsets of the underlying set of a topological space appear as as more-or-less unseparable as seen by the topology on that set. In many applications one wants to exclude at least some of such degenerate examples from the discussion. The relevant conditions to be imposed on top of the plain [[axioms]] of a [[topological space]] are hence known as _separation axioms_.

These axioms are all of the form of saying that two [[subsets]] (of certain forms) in the topological space are 'separated' from each other in one sense if they are 'separated' in a (generally) weaker sense. Most of these conditions can be expressed as [[separation axioms in terms of lifting properties|lifting properties with respect to maps of finite topological spaces or the real line]]. For example the weakest axiom (called $T_0$) demands that if two points are distinct as elements of the [[underlying]] set, then there exists at least one [[open subset]] that contains one but not the other,
i.e. the function determined by two distinct points is not [[continuous function|continuous]] as a map from the [[indiscrete space]].

In this fashion one may impose a hierarchy of stronger axioms. For example demanding that given two distinct points, then each of them is contained in some open subset not containing the other ($T_1$), i.e. 
any map from the space with one open point and one closed is necessarily trivial, or that such a pair of open subsets around two distinct points may in addition be chosen to be disjoint ($T_2$).  
This last condition, $T_2$, also called the _[[Hausdorff topological space|Hausdorff condition]]_ is the most common among all separation axioms. Often (but by far not always) this is considered by default.

Rewriting the [[separation axioms in terms of lifting properties]] 
with respect to maps of finite topological spaces, i.e. monotone maps of preorders, provides a combinatorial point of view on this hierachy,
and simplifies certain universal constructions such as 
[reflection](#Reflection) or  [Kolmogorov quotient](#KolmogorovQuotient). 


The main separation axioms are these:

{#TableOfMainSeparationAxioms}
[[!include main separation axioms -- table]]

Originally in [Tietze 23](#Tietze23) the four separation axioms $T_2, T_3, T_4, T_5$ were considered (see at _[History](#History)_ below for more); nowadays one considers various more. Besides the extrapolation of the original sequence from $T_0$ through $T_6$ (with $T_{2\frac{1}{2}}$ and $T_{3\frac{1}{2}}$ interpolated), there is a similar sequence of axioms called $R_0, R_1, R_2, R_3$ (with their extrapolations and interpolations) of the same form, except that they do not start with mentioning two set-theoretically distinct points, but two points satisfying the conclusion of $T_0$. This and more is spelled out [below](#TheClassicalTheory).

There are also axioms that do not follow the pattern of "if certain two subsets are separated in some weak sense, then they are also separated in some stronger sense", but that still axiomatize some kind of separatedness. For example the condition on a [[topological space]] being [[sober topological space|sober]] is of a different nature, but is implied by $T_2$ and implies $T_0$. Notice that via their [[full subcategory|full embedding]] into [[locales]], [[sober topological spaces]] may be understood without reference to their underlying set of points at all.

All separation axioms are satisfied by [[metric spaces]], from whom the concept of topological space was originally abstracted. Hence imposing some of them may also be understood as gauging just how far one allows topological spaces to generalize away from metric spaces.

Several separation axioms may also be interpreted in broader contexts that plain topological spaces, for instance for [[convergence space]] or for [[locales]]; or the may be considered under weaker assumptions, such as those of [[constructive mathematics]] and [[predicative mathematics]].



## The classical theory
 {#TheClassicalTheory}

First, we will consider how, for topological spaces in [[classical mathematics]], the separation axioms are about sets\' being 'separated' as stated above.  Throughout, fix a [[topological space]] $S$.


### Separation conditions

Fix two sets ([[subsets]]) $F$ and $G$ of $S$.

*  The sets $F$ and $G$ are __[[disjoint sets|disjoint]]__ if their [[intersection]] is [[empty set|empty]]:
   $$ F \cap G = \empty .$$
*  They are __topologically disjoint__ if there exists a [[neighbourhood]] of one set that is disjoint from the other set:
   $$ (\exists\; U \stackrel{\circ}\supseteq F,\; U \cap G = \empty) \;\vee\; (\exists\; V \stackrel{\circ}\supseteq G,\; F \cap V = \empty) .$$
   Notice that topologically disjoint sets must be disjoint.
*  They are __separated__ if each set has a neighbourhood that is disjoint from the other set:
   $$ (\exists\; U \stackrel{\circ}\supseteq F,\; U \cap G = \empty) \;\wedge\; (\exists\; V \stackrel{\circ}\supseteq G,\; F \cap V = \empty)
   \;\;\equiv\;\;
   \exists\; U \stackrel{\circ}\supseteq F,\; \exists\; V \stackrel{\circ}\supseteq G,\; U \cap G = \empty \;\wedge\; F \cap V = \empty .$$
   Notice that separated sets must be topologically disjoint.

*  {#SeparatedByNeighbourhoods} They are __separated by neighbourhoods__ if they have disjoint neighbourhoods:
   $$ \exists\; U \stackrel{\circ}\supseteq F,\; \exists\; V \stackrel{\circ}\supseteq G,\; U \cap V = \empty .$$
   Notice that sets separated by neighbourhoods must be separated.

*  They are __separated by closed neighbourhoods__ if they have disjoint closed neighbourhoods:
   $$ \exists\; U \stackrel{\circ}\supseteq F,\; \exists\; V \stackrel{\circ}\supseteq G,\; Cl(U) \cap Cl(V) = \empty .$$
   Notice that sets separated by closed neighbourhoods must be separated by neighbourhoods.
*  They are __separated by a function__ if there exists a continuous [[real number|real]]-valued [[function]] on the space that maps $F$ to $0$ and $G$ to $1$:
   $$ \exists\; f: S \to \mathbf{R},\; F \subseteq f^*(\{0\}) \;\wedge\; G \subseteq f^*(\{1\}) .$$
   Notice that sets separated by a function must be separated by closed neighbourhoods (the preimages of $[-\epsilon, \epsilon]$ and $[1-\epsilon, 1+\epsilon]$).
*  Finally, they are __precisely separated by a function__ if there exists a continuous real-valued function on the space that maps precisely $F$ to $0$ and $G$ to $1$:
   $$ \exists\; f: S \to \mathbf{R},\; F = f^*(\{0\}) \;\wedge\; G = f^*(\{1\}) .$$
   Notice that sets precisely separated by a function must be separated by a function.

Often $F$ and $G$ will be points (identified with their [[singleton]] subsets); in that case, one usually says _distinct_ in place of _disjoint_.

Often $F$ or $G$ will be closed sets; notice that disjoint closed sets are automatically separated, while a closed set and a point, if disjoint, are automatically topologically disjoint.


### Separation axioms

The classical separation axioms are all statements of the form

*  When $F$ is a (point/closed) set and $G$ is a (point/closed) set, if $F$ and $G$ are (separated in some weak sense), then they are (separated in some strong sense).

The axioms with names (at least with known to the authors so far of this article) are summarised in the tables below.  When a row or column is missing from a table, either no name is known or the implication follows from the converses mentioned after the separation conditions above in the context of that table; there are two potential tables that are completely blank for the latter reason.  When an entry in a table is repeated, that corresponds to a theorem that one separation axiom implies another.

When both sets are points:
<table><tr><th>Stronger condition &#8595;\Weaker condition &#8594;</th> <th>Distinct</th> <th>Topologically distinct</th></tr>
<tr><th>Topologically distinct</th> <td markdown="1">$T_0$</td></tr>
<tr><th>Separated</th> <td markdown="1">$T_1$</td> <td markdown="1">$R_0$</td></tr>
<tr><th>Separated by neighbourhoods</th> <td markdown="1">$T_2$</td> <td markdown="1">$R_1$</td></tr>
<tr><th>Separated by closed neighbourhoods</th> <td markdown="1">$T_{2\frac{1}{2}}$</td> <td markdown="1">$R_{1\frac{1}{2}}$</td></tr>
<tr><th>Separated by a function</th> <td markdown="1">Completely $T_2$</td> <td markdown="1">Completely $R_1$</td></tr></table>

When one set is a point and the other is closed:
<table markdown="1"><tr><th>Stronger condition &#8595;\Weaker condition &#8594;</th> <th>Disjoint</th></tr>
<tr><th>Separated by neighbourhoods</th> <td>Regular</td></tr>
<tr><th>Separated by closed neighbourhoods</th> <td>Regular</td></tr>
<tr><th>Separated by a function</th> <td>Completely regular</td></tr></table>

When both sets are closed:
<table markdown="1"><tr><th>Stronger condition &#8595;\Weaker condition &#8594;</th> <th>Disjoint</th></tr>
<tr><th>Separated by neighbourhoods</th> <td>Normal</td></tr>
<tr><th>Separated by closed neighbourhoods</th> <td>Normal</td></tr>
<tr><th>Separated by a function</th> <td>Normal</td></tr>
<tr><th>Precisely separated by a function</th> <td>Perfectly normal</td></tr></table>

When the sets are arbitrary:
<table markdown="1"><tr><th>Stronger condition &#8595;\Weaker condition &#8594;</th> <th>Separated</th></tr>
<tr><th>Separated by neighbourhoods</th> <td>Completely normal ($T_5$)</td></tr></table>



### Reformulation in terms of topological closures
 {#EquivalentIncarnationsOfTheAxioms}

Many of the separation axioms have a useful equivalent formulation in terms of certain  [[topological closures]].

+-- {: .num_prop #T0InTermsOfClosureOfPoints}
###### Proposition
**($T_0$ in terms of topological closures)**

A [[topological space]] $(X,\tau)$ is $T_0$ 
precisely if the function $Cl(\{-\})$
from the underlying set of $X$ to the set of [[irreducible closed subsets]] of $X$, is [[injective function|injective]]:

$$
  Cl(\{-\}) \;\colon\; X \hookrightarrow IrrClSub(X)
$$


=--

(This statement also motivates the definition of [[sober topological spaces]], for which $Cl(\{-\})$ is required to be a [[bijection]]).

+-- {: .proof}
###### Proof

Assume first that $X$ is $T_0$. Then we need to show that if $x,y \in X$ are such that
$Cl(\{x\}) = Cl(\{y\})$ then $x = y$. Hence assume that $Cl(\{x\}) = Cl(\{y\})$.
Since the closure of a point is the [[complement]] of the union of the open subsets not containing the point
(lemma \ref{UnionOfOpensGivesClosure}),
this means that the union of open subsets that do not contain $x$
is the same as the union of open subsets that do not contain $y$:

$$
  \underset{ {U \subset X \, \text{open}} \atop { U \subset X\backslash \{x\} } }{\cup} \left( U \right)
  \;=\;
  \underset{ {U \subset X \, \text{open}} \atop { U \subset X\backslash \{y\} } }{\cup} \left( U \right)
$$

But if the two points were distinct, $x \neq y$, then by $T_0$ one of the above unions would contain $x$ or $y$, while the other would not, in contradiction to the above equality. Hence we have a [[proof by contradiction]].

Conversely, assume that $\left( Cl\{x\} = Cl\{y\}\right) \Rightarrow \left( x = y\right)$, and assume that $x \neq y$.
Hence by [[contraposition]] $\mathrm{Cl}(\{x\}) \neq \mathrm{Cl}(\{y\})$. We need to show that there exists
an open set which contains one of the two points, but not the other.

Assume there were no such open subset. By lemma [this lemma](Introduction+to+Topology+--+1#UnionOfOpensGivesClosure) this would mean
that $x \in \mathrm{Cl}(\{y\})$ and that $y \in \mathrm{Cl}(\{x\})$. But this would imply that
$Cl(\{x\}) \subset \mathrm{Cl}(\{y\})$ and that $\mathrm{Cl}(\{y\}) \subset \mathrm{Cl}(\{x\})$,
hence that $\mathrm{Cl}(\{x\}) = \mathrm{Cl}(\{y\})$. This is a [[proof by contradiction]].

=--

+-- {: .num_prop #T1InTermsOfClosureOfPoints}
###### Proposition
**($T_1$ in terms of topological closures)**

A [[topological space]] $(X,\tau)$ is $T_1$ precisely if
all its points are [[closed points]].

=--

+-- {: .proof}
###### Proof

Assume first that $(X,\tau)$ is $T_1$. We need to show that for every point $x \in X$ we have
$Cl(\{x\}) = \{x\}$. Since the closure of a point is the [[complement]] of the union of all open subsets not containing this point,
this is the case precisely if the union of all open subsets not containing $x$ is $X \backslash \{x\}$, hence
if every point $y \neq x$ is member of at least one open subset not containing $x$. This is true by $T_1$.

Conversely, assume that for all $x \in X$ then $Cl(\{x\}) = \{x\}$. Then for $x \neq y \in X$ two
distinct points we need to produce an open subset of $y$ that does not contain $x$. But as before,
since $Cl(\{x\})$ is the complement of the union of all open subsets that do not contain $x$, and
the assumption $Cl\{x\} = \{x\}$ means that $y$ is member of one of these open subsets that do not
contain $x$.

=--

+-- {: .num_prop #T2InTermsOfClosedDiagonal}
###### Proposition
**($T_2$ in terms of topological closures)**

A [[topological space]] $(X,\tau_X)$ is $T_2$=[[Hausdorff topological space|Hausdorff]] 
precisely if the [[image]] of the [[diagonal]] 

$$
  \array{
     X &\overset{\Delta_X}{\longrightarrow}& X \times X
     \\
     x &\overset{\phantom{AAA}}{\mapsto}& (x,x)
  }
$$ 

is a [[closed subset]] in the [[product topological space]]
$(X \times X, \tau_{X \times X})$.

=--

+-- {: .proof}
###### Proof

The Hausdorff condition, that for $x \neq y \in X$ then there exist disjoint open neighbourhood $U_x, U_y \subset X$, is equivalently rephrased in terms of the product topology as: Every point $(x,y) \in X$ which is not on the diagonal has an open neighbourhood $U_x \times U_y$ which still does not intersect the diagonal.

Hence if $X$ is Hausdorff, then the diagonal $\Delta_X(X) \subset X \times X$ is the complement of a union of such open sets, and hence is closed. 

Conversely, if the diagonal is closed, then (by [this lemma](Introduction+to+Topology+--+1#UnionOfOpensGivesClosure)) every point $(x,y)$ not on the diagonal, hence with $x \neq y$, has an open neighbourhood $U_x \times U_y$ still not intersecting the diagonal, hence so that $U_x \cap U_y = \emptyset$. Thus $(X,\tau)$ is Hausdorff.

=--

+-- {: .num_remark}
###### Remark

The characterization of the Hausdorff separation condition via the closure of the diagonal in prop. \ref{T2InTermsOfClosedDiagonal} is the basis for the definition of _[[separated scheme]]_.

=--


+-- {: .num_prop #T3InTermsOfTopologicalClosures}
###### Proposition
**($T_3$ in terms of topological closures)**

A [[topological space]] $(X,\tau)$ is [[regular topological space|regular]], precisely if for all [[closed subsets]] $x \in X$ with [[open neighbourhood]] $U \supset \{x\}$ there exists a smaller open neighbourhood $V \supset \{x\}$ whose [[topological closure]] $Cl(V)$ is still contained in $U$:

$$
  \{x\} \subset V \subset Cl(V) \subset U
  \,.
$$

=--

The **proof** of prop. \re{T3InTermsOfTopologicalClosures} is the direct  specialization of the following proof for prop. \ref{T4InTermsOfTopologicalClosures} to the case that $C = \{x\}$ (using that by $T_1$, which is part of the definition of $T_3$, the singleton subset is indeed closed by prop. \ref{T1InTermsOfClosureOfPoints}).


+-- {: .num_prop #T4InTermsOfTopologicalClosures}
###### Proposition
**($T_4$ in terms of topological closures)**

A [[topological space]] $(X,\tau)$ is [[normal topological space|normal]], precisely if for all [[closed subsets]] $C \subset X$ with [[open neighbourhood]] $U \supset C$ there exists a smaller open neighbourhood $V \supset C$ whose [[topological closure]] $Cl(V)$ is still contained in $U$:

$$
  C \subset V \subset Cl(V) \subset U
  \,.
$$

=--

+-- {: .proof}
###### Proof

In one direction, assume that $(X,\tau)$ is normal, and consider $C \subset U$. It follows that the [[complement]] of the open subset $U$ is closed and disjoint from $C$:

$$
  C \cap X \backslash U = \emptyset
  \,.
$$

Therefore by assumption of normality of $(X,\tau)$, there exists open neighbourhoods $V \supset C$ and $W \supset X \backslash U$ with

$$
  V \cap W = \emptyset
  \,.
$$

But this means that 

$$
  V \subset X \backslash W
$$

and since the [[complement]] $X \backslash W$ of the open set $W$ is closed, it still contains the closure of $V$, so that we have

$$
  C \subset V \subset Cl(V) \subset X \backslash W \subset U
  \,.
$$

In the other direction, assume that for every open neighbourhood $U \supset C$ of a closed subset $C$ there exists a smaller open neighbourhood $V$ with $C \subset V \subset Cl(V) \subset U$. Consider disjoint closed subsets $C_1, C_2 \subset X$. We need to produce disjoint open neighbourhoods for them. 

From their disjointness it follows that $X \backslash C_2 \supset C_1$ is an open neighbourhood. Hence by assumption there is an open neighbourhood $V$ with 

$$
  C_1 \subset V \subset Cl(V) \subset X \backslash C_2
  \,.
$$

Thus $V \supset C_1$ and $X \backslash Cl(X) \supset C_2$ are two disjoint open neighbourhoods, as required.

=--




### Relations between the axioms

First of all, notice (prop. \ref{T1InTermsOfClosureOfPoints}) that the $T_1$ condition, saying that distinct points are separated, is equivalent to the condition that every point is closed.  Thus, $T_1$ serves as a linchpin between conditions on points and conditions on closed sets.

Many implications between separation axioms can be seen in the following Hasse diagram:

<img src="http://ncatlab.org/nlab/files/separation.png" width="472" alt="" />

Here, there are two entries at each node; the one on the right includes the $T_0$ axiom, while the one on the left does not.  This diagram shows the separation axioms as a meet sub-[[semilattice]] of the lattice of all conditions on topological spaces; for example, you can see, by following the diagram upwards, that any space that is both **n**ormal and **r**egular must be $R_3$.  And since $R_3$ never appears in the tables above, you can take this as a *definition* of $R_3$.

In general, the names in this diagram are:

*  'P' for 'perfectly',
*  'C' for 'complete',
*  'N' for '[[normal space|normal]]',
*  'R' (without a subscript) for '[[regular space|regular]]'
*  'T' or 'R' with a subscript are written and pronounced that way.

Warning: $T_i$ for $i \geq 3$ has been used in different ways in the past, and perhaps by some schools still.  Also, all of the $R_i$ terms are rare.  It is safest to say, for example, 'normal Hausdorff' for $T_4$ and clearer to say, for example, 'normal regular' for $R_3$.  If you want to avoid the subscript terms entirely, then you can, by doing the above and the following:

* $T_{2\tfrac{1}{2}}$ = [[Urysohn space|Urysohn]]
*  $T_2$ = [[Hausdorff space|Hausdorff]],
*  $T_1$ = accessible,
*  $T_0$ = [[Kolmogorov space|Kolmogorov]],
*  $R_1$ = reciprocal,
*  $R_0$ = symmetric.

On the other hand, if you want to use *more* symbols, then you can:

*  $R_2$ = regular,
*  $R_{2\frac{1}{2}}$ = completely regular.

It would be easy to invent an $N_i$ series for the various kinds of normal spaces, but nobody seems to have done so yet.

Other terms are also in use, principally 'Tychonoff' for [[Tychonoff space|completely regular Hausdorff]] ($T_{3\frac{1}{2}}$).



### Reflection
 {#Reflection}

+-- {: .num_prop #HausdorffReflection}
###### Proposition
**($T_n$-reflection)**

Let $n \in \{0,1,2\}$. Then for every [[topological space]] $X$ there exists
a $T_n$-topological space $T_n X$ and a [[continuous function]] of the forma

$$
  t_n(X)
    \;\colon\;
  X \longrightarrow T_n X
$$

which is the  "closest approximation from the left" to $X$ by a $T_n$-topological space, in that
for $Y$ any $T_n$-space, then [[continuous functions]] of the form

$$
  f \;\colon\; X \longrightarrow Y
$$

are in [[bijection]] with [[continuous function]] of the form

$$
  \tilde f \;\colon\; T_n X \longrightarrow Y
$$

and such that the bijection is constituted by

$$
  f = \tilde f \circ t_n(X)
  \;\colon\;
    X
      \overset{t_n(X)}{\longrightarrow}
    T_n X
      \overset{\tilde f}{\longrightarrow}
    Y
  \,.
$$

Here $X \overset{t_n(X)}{\longrightarrow} T_n(X)$ is called the _$T_n$-reflection_ of $X$.

* For $n = 0$ this is known as the _[[Kolmogorov quotient]]_ construction (see prop. \ref{KolmogorovQuotient} below). 

* For $n = 2$ this is known as _[[Hausdorff reflection]]_ or _Hausdorffication_ or similar.



Moreover, the operation $T_n(-)$ extends to [[continuous functions]] $f \colon X \to Y$

$$
  (X \overset{f}{\to} Y)
    \;\mapsto\;
  (T_n X \overset{T_n f}{\to} T_n Y)
$$

such as to preserve [[composition]] of functions as well as [[identity functions]]:

$$
  (T_n g) \circ (T_n f) = T_n(g \circ f)
  \phantom{AA}
  \,,
  \phantom{AA}
  T_n (id_X) = id_{T_n X}
  \,
$$

Finally, the comparison map is compatible with this in that for all continuous functions $f \colon X \to Y$ then 

$$
  t_n(Y) \circ f
   =
  T_n(f)\circ t_n(X)
$$


hence then follows [[commuting squares|squares commutes]]:

$$
  \array{
      X &\overset{f}{\longrightarrow}& Y
      \\
      {}^{\mathllap{t_n(X)}}\downarrow && \downarrow^{\mathrlap{t_n(Y)}}
      \\
      T_n X &\underset{T_n f}{\longrightarrow}& T_n Y
  }
  \,.
$$


=--

We give a **proof** of the existence of this reflection below as the proof of prop. \ref{HausdorffReflectionViaHomsIntoAllHausdorffSpaces}.


+-- {: .num_remark }
###### Remark
**([[reflective subcategories]])**

In the language of [[category theory]] the $T_n$-reflection of prop. \ref{HausdorffReflection}
says that

1. $T_n(-)$ is a _[[functor]]_ $T_n \;\colon\; Top \longrightarrow Top_{T_n}$ from the [[category]] [[Top]] of [[topological spaces]] to the [[full subcategory]] $Top_{T_n} \overset{\iota}{\hookrightarrow} Top$ of Hausdorff topological spaces;

1. $t_n(X) \colon X \to T_n X$ is a _[[natural transformation]]_ from the [[identity functor]] on [[Top]] to the functor $\iota \circ T_n$

1. $T_n$-topological spaces form a [[reflective subcategory]] of all [[topological spaces]] in that $T_n$ is [[left adjoint]] to the inclusion functor $\iota$; this situation is denoted as follows:

   $$
     Top_{T_n}
       \underoverset{\underset{\iota}{\hookrightarrow}}{\overset{H}{\longleftarrow}}{\bot}
     Top
     \,.
   $$

Generally, an _[[adjoint functor|adjunction]]_ between two [[functors]] 

$$
  L \;\colon\; \mathcal{C} \leftrightarrow \mathcal{D} \;\colon\; R
$$

is for all pairs of objects $c \in \mathcal{C}$, $d \in \mathcal{D}$ a [[bijection]] between sets of [[morphisms]] of the form

$$
  \left\{
     L(c) \longrightarrow d
  \right\}
  \simeq
  \left\{
    c \longrightarrow R(d)
  \right\}
  \,.
$$

i.e.

$$
  Hom_{\mathcal{D}}(L(c), d)
  \underoverset{\simeq}{\phi_{c,d}}{\longrightarrow}
  Hom_{\mathcal{C}}(c, R(d))
$$

and such that these bijections are "[[natural bijection|natural]]" in that they for all pairs of morphisms $f \colon c' \to c$ and $g \colon d \to d'$ then the folowing [[commuting diagram|diagram commutes]]:

$$
  \array{
    Hom_{\mathcal{D}}(L(c), d)
      &\underoverset{\simeq}{\phi_{c,d}}{\longrightarrow}&
    Hom_{\mathcal{C}}(c, R(d))
    \\
    {\mathllap{g \circ (-) \circ L(f)}}\downarrow 
       &&
    \downarrow{\mathrlap{ R(g) \circ (-) \circ f }}
    \\
    Hom_{\mathcal{C}}(L(c'), d')
     &\underoverset{\simeq}{\phi_{c',d'}}{\longrightarrow}&
    Hom_{\mathcal{D}}(c', R(d'))
  }
  \,.
$$


=--

There are various ways to see the existence and to construct the $T_n$-reflections. The following is the quickest way to see the existence, even if to some tastes the construction seems more implicit or abstract than the previous one.


+-- {: .num_prop #HausdorffReflectionViaHomsIntoAllHausdorffSpaces}
###### Proposition
**($T_n$-reflection via surjections into $T_n$-spaces)**

Let $n \in \{0,1,2\}$. Let $(X,\tau)$ be a [[topological space]] and consider the [[equivalence relation]] $\sim$ on the underlying set $X$
for which $x \sim y$ precisely if for every [[surjective function|surjective]] [[continuous function]] $f \colon X \to Y$ into any
$T_n$-topological space $Y$ we have $f(x) = f(y)$.

Then the set of [[equivalence classes]]

$$
  T_n X \coloneqq X /{\sim}
$$

equipped with the [[quotient topology]] is a $T_n$-topological space, and the quotient map $t_n(X) \;\colon\; X \to X/{\sim}$ exhibits the $T_n$-reflection of $X$, according to prop. \ref{HausdorffReflection}.

=--

+-- {: .proof}
###### Proof

First we observe that every continuous function $f \colon X \longrightarrow Y$ into a $T_n$-topological space $Y$
factors uniquely via $t_n(X)$ through a continuous function $\tilde f$

$$
  f = \tilde f \circ h_X
$$

where

$$
  \tilde f \colon [x] \mapsto f(x)
  \,.
$$

To see this, first factor $f$ through its [[image]] $f(X)$

$$
  f \;\colon\; X \longrightarrow f(X) \hookrightarrow Y
$$

equipped with its [[topological subspace|subspace topology]] as a subspace of $Y$. It follows that $f(X)$ is a $T_n$-topological space if $Y$ is. 

It follows by definition of $t_n(X)$ that the factorization exists at the level of sets as stated, 
since if $x_1, x_2 \in X$ have the same [[equivalence class]] $[x_1] = [x_2]$ in $T_n X$, then 
by definition they have the same image under all continuous surjective functions to a $T_n$-space, hence in particular
under $X \to f(X)$. This means that $\tilde f$ as above is well defined. Moreover, it is clear that this is the unique factorization.

To see that $\tilde f$ is continuous, consider $U \in Y$ an open subset. We need to show that $\tilde f^{-1}(U)$ is open in $X/\sim$. But by definition of the [[topological quotient space|quotient topology]], this is open precisely if its pre-image under the quotient projection $t_n(X)$ is open, hence precisely if

$$
  (t_n(X))^{-1}(\tilde f^{-1}(U))
  =
  ( \tilde f \circ t_n(X) )^{-1}(U)
  =
  f(U)
$$

is open in $X$. But this is the case by the assumption that $f$ is continuous.


What remains to be seen is that $T_n X$ as constructed is indeed a $T_n$-topological space. 
Hence assume that $[x] \neq [y] \in T_n X$ are two distinct points. We need to open neighbourhoods
around one or both of these point not containing the other point and possibly disjoint to each other.

Now by definition of $T_n X$ this means that there exists a $T_n$-topological space $Y$ and a surjective continuous function
$f \colon X \longrightarrow Y$ such that $f(x) \neq f(y) \in Y$. Accordingly, since $Y$ is $T_n$,
there exist the respective kinds of neighbourhoods around these image points in $Y$. Moreover, by the previous statement there
exists a continuous function $\tilde f \colon T_n X \to Y$ with $\tilde f([x]) = f(x)$ and $\tilde f([y]) = f(y)$.
By the nature of continuous functions,
the pre-images of these open neighbourhoods in $Y$ are still open in $X$ and still
satisfy the required disjunction properties. Therefore $T_n X$ is a $T_n$-space.

=--

Here are alternative constructions of the reflections:

+-- {: .num_prop #KolmogorovQuotient}
###### Proposition
**([[Kolmogorov quotient]])**

Let $(X,\tau)$ be a [[topological space]]. Consider the [[relation]] on the underlying set
by which $x_1 \sim x_1$ precisely if neighther $x_i$ has an [[open neighbourhood]] not containing the other.
This is an [[equivalence relation]]. The [[quotient topological space]] $X \to X/\sim$ by this
equivalence relation  exhibits the $T_0$-reflection of $X$ according to prop. \ref{HausdorffReflection}.

=--

+-- {: .num_prop #HausdorffReflectionViaTransitiveClosureOfDiagonal}
###### Proposition
**([[Hausdorff reflection]])**

For $(Y,\tau_Y)$ a [[topological space]], write $r_Y \subset Y \times Y$
for the [[transitive relation|transitive closure]] of tthe [[relation]] given by the [[topological closure]] $Cl(\Delta_Y)$ of the [[image]] of the [[diagonal]] $\Delta_Y \colon Y \hookrightarrow Y \times Y$.

$$
  r_Y \coloneqq Trans(Cl(Delta_Y))
  \,.
$$

Now for $(X,\tau_X)$ a [[topological space]], define by [[induction]] for each [[ordinal number]] $\alpha$ an [[equivalence relation]] $r^\alpha$ on $X$ as follows, where we write $q^\alpha \colon X \to H^\alpha(X)$ for the corresponding [[quotient topological space]] projection:

We start the induction with the trivial equivalence relation:

* $r^0_X \coloneqq \Delta_X$;

For a [[successor ordinal]] we set

* $r_X^{\alpha+1} \coloneqq \left\{ (a,b) \in X \times X  \,\vert\, (q^\alpha(a), q^\alpha(b)) \in r_{H^\alpha(X)} \right\}$

and for a [[limit ordinal]] $\alpha$ we set

* $r_X^\alpha \coloneqq \underset{\beta \lt \alpha}{\cup} r_X^\beta$.

Then:

1. there exists an ordinal $\alpha$ such that $r_X^\alpha = r_X^{\alpha+1}$

1. for this $\alpha$ then $H^\alpha(X) = H(X)$ is the Hausdorff reflection from prop. \ref{HausdorffReflectionViaHomsIntoAllHausdorffSpaces}.


=--

([vanMunster 14, section 4](Hausdorff+space#vanMunster14))







### Other axioms

There are other axioms sometimes included among the separation axioms that don\'t fit the preceding pattern; but like the others, they all hold of a metric space:

*  [[sober space|sober]] and having enough points,
*  [[semiregular space|semiregular]],
*  [[fully normal topological space|fully normal]] and fully $T_4$, which are related to [[paracompact space|paracompactness]] (see at _[[fully normal spaces are equivalently paracompact]]_).


## Beyond the classical theory

The axioms $T_1$ and below can be phrased entirely in terms of the [[specialisation order]], as follows:

*  In general, the specialisation order is a [[preorder]].
*  The space is $T_0$ if and only if the specialisation order is a [[partial order]].
*  The space is $R_0$ if and only if the specialisation order is an [[equivalence relation]].
*  The space is $T_1$ if and only if the sepcification order is the [[equality relation]].

Note that *any* preorder is the specialisation order for its own [[specialisation topology]].


The separation conditions that appear in $T_2$ and below, or rather their [[negation]]s, can be easily phrased in terms of the [[convergence space|convergence structure]], as follows:

*  Two points are not distinct if and only if they are equal (of course).
*  They are __topologically indistinguishable__ (that is, not topologically distinct) if and only if every [[net]] (or [[filter]]) that [[convergnce|converges]] to one must also converge to the other; it\'s enough to check the [[ultrafilters]] generated by the two points.
*  They are not separated if and only there exists a net (or proper filter) that converges to both.

So by taking contrapositives, it\'s easy to generalise $T_2$ and below to [[convergence spaces]].  (All of the axioms *can* be generalised to convergence spaces, since the convergence structure determines the topology, but there are several ways to do so, and it\'s not clear in general which is best.)


For [[locales]], the axioms at the other end are clearest.  Here we want to put everything in terms of open sets, so we simply work with the [[complements]] of the closed sets that appear in those axioms.  Rather than talk about a closed set $F$ and a neighbourhood $U$ of $F$, we talk about an open set $G$ and an open set $U$ such that $G \cup U$ is the entire space.  Now the axioms at the low end are tricky, although there is a standard answer as far down as $T_2$.  (Note that every locale is $T_0$, indeed sober.)


In [[constructive mathematics]], while the classical definitions all make sense, they are never quite what is wanted.  For the low axioms, one may use, as with convergence spaces, conditions that are classically the negations of the separation conditions; for the high axioms, one may use the open sets that are classically the complements of the closed sets in the axioms.  In the middle axioms, these work together; for example, the condition that a point $x$ is disjoint from a closed set $F$ becomes the condition that $x$ belongs to an open set $G$.


Specific examples should be found on the pages for specific separation axioms.

## History
 {#History}

In [Tietze 23, part B, starting on page 300](#Tietze23). 4 axioms are discussed, called (in words, not numbers) the first, second, third, and fourth separation axioms (*erstes, zweites, drittes, und viertes Trennbarkeitsaxiom*).  The first of these is $T_2$, the second is $T_3$, the third is $T_4$, and the fourth is $T_5$.  So while this paper may be the first to consider a hierarchy of separation axioms, it is not the source of our $T_i$ notation, and it does not number them in the same way.

All of these after the first are stated in such a way as to not imply the first, and those after the second are similarly stated in such a way as not to imply the second.  However, Tietze does seem to want them to be a hierarchy.  For one thing, his general definition of topological space &#8212; stated in multiple equivalent ways in part A &#8212; includes the first separation axiom, so in context it seems that the others are meant to be postulated only of spaces that are already Hausdorff.  

Also, after stating the axioms, he immediately provides examples of spaces that satisfy one property but not a higher one, taking care to list both the first and the second separation axiom among those that the third is independent of, but leaving out the second, listing only the first and the third, when listing the axioms that the fourth is independent of.  He does eventually give an example of a space that satisfies the second and third but not the first (so a normal regular space that is not Hausdorff), but it is later and more of an afterthought (and the only non-Hausdorff space in this paper).  He never asks whether there exists of a regular space that is not normal.

Immediately after this example of a non-Hausdorff space, [Tietze 23](#Tietze23) lists the $T_1$ axiom after all!  But it is not on the same level as the others to him.  Instead, it is merely an alternative form of the first separation axiom that may be used in the presence of the second.  It still appears that non-Hausdorff spaces are not considered to be real topological spaces worthy of one\'s attention.

## Related concepts

* [[nice topological space]]

* [[separation axioms in terms of lifting properties]]


## References

An original article is

* {#Tietze23} Heinrich Tietze, _Beitrage zur allgemeinen Topologie. I. Axiome f&#252;r verschiedene Fassungen des Umgebungsbegriffs_, Mathematische Annalen, vol 88, pages 290-311 (1923) ([online scan](https://www.digizeitschriften.de/en/dms/img/?PID=GDZPPN00226921X&physid=phys298#navi))

Lecture notes include

* {#Naik} [[Vipul Naik]], _Topology: The journey into separation axioms_ ([pdf](http://www.cmi.ac.in/~vipul/mathjourneys/contytopologysep.pdf))

See also the entry

* Wikipedia, _[Separation axiom](http://secure.wikimedia.org/wikipedia/en/wiki/Separation_axiom)_

(This is not really an independent reference, since one of the main authors of the present entry is also one of the main authors of the Wikipedia entry.)


[[!redirects separation axiom]]
[[!redirects separation axioms]]
[[!redirects separation property]]
[[!redirects separation properties]]


[[!redirects topologically distinct point]]
[[!redirects topologically distinct points]]

[[!redirects topologically disjoint set]]
[[!redirects topologically disjoint sets]]
[[!redirects topologically disjoint subset]]
[[!redirects topologically disjoint subsets]]
[[!redirects topologically disjoint subspace]]
[[!redirects topologically disjoint subspaces]]

[[!redirects separated set]]
[[!redirects separated sets]]
[[!redirects separated subset]]
[[!redirects separated subsets]]
[[!redirects separated subspace]]
[[!redirects separated subspaces]]


[[!redirects T1]]

[[!redirects T1 space]]
[[!redirects T1 spaces]]
[[!redirects T1-space]]
[[!redirects T1-spaces]]
[[!redirects T_1 space]]
[[!redirects T_1 spaces]]
[[!redirects T_1-space]]
[[!redirects T_1-spaces]]

[[!redirects T1 topological space]]
[[!redirects T1 topological spaces]]
[[!redirects T1-topological space]]
[[!redirects T1-topological spaces]]
[[!redirects T_1 topological space]]
[[!redirects T_1 topological spaces]]
[[!redirects T_1-topological space]]
[[!redirects T_1-topological spaces]]



[[!redirects perfectly normal topological space]]
[[!redirects perfectly normal topological spaces]]
[[!redirects perfectly normal space]]
[[!redirects perfectly normal spaces]]

