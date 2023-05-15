
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The generalization of the notion of [[functor category]] from [[category theory]] to [[(∞,1)-category|(∞,1)]]-[[higher category theory]].

## Definition

Let $C$ and $D$ be [[(∞,1)-categories]], taken in their incarnation as [[quasi-category|quasi-categories]]. Then

$$
  Func(C,D) := sSet(C,D)
$$

is the [[simplicial set]] of morphisms of simplicial sets between $C$ and $D$ (in the standard [[sSet]]-[[enriched category|enrichment]] of $SSet$):

$$
  sSet(C,D) := [C,D] := ([n] \mapsto Hom_{sSet}(\Delta[n]\times C,D))
  \,.
$$

The objects in $Fun(C,D)$ are the [[(∞,1)-functors]] from $C$ to $D$, the morphisms are the corresponding [[natural transformations]] or [[homotopy|homotopies]], etc.

+-- {: .num_prop }
###### Proposition

The simplicial set $Fun(C,D)$ is indeed a [[quasi-category]].

In fact, for $C$ and $D$ any simplicial sets, $Fun(C,D)$ is a [[quasi-category]] if $D$ is a [[quasi-category]].

=--

+-- {: .proof}
###### Proof

Using that [[sSet]] is a [[closed monoidal category]] the [[horn]] filling conditions

$$
  \array{
    \Lambda[n]_i &\to& [C,D]
    \\
    \downarrow & \nearrow
    \\
    \Delta[n]
  }
$$

are equivalent to 

$$
  \array{
    C \times \Lambda[n]_i &\to& D
    \\
    \downarrow & \nearrow
    \\
    C \times \Delta[n]
  }
  \,.
$$

Here the vertical map is [[fibrations of quasi-categories|inner anodyne]] for inner horn inclusions $\Lambda[n]_i \hookrightarrow \Delta[n]$, and hence the lift exists whenever $D$ has all inner horn fillers, hence when $D$ is a [[quasi-category]].

=--

For the definition of $(\infty,1)$-functors in other models for $(\infty,1)$-categories see [[(∞,1)-functor]].


## Properties

### Model category presentation 
 {#ModelCategoryPresentation}

The projective and injective [[global model structure on functors]] (as well as the [[Reedy model structure]] if $C$ is a [[Reedy category]]) [[presentable (infinity,1)-category|presents]] $(\infty,1)$-categories of $(\infty,1)$-functors, at least when there exists [[combinatorial simplicial model category|combinatorial simplicial]]-[[structure]] model on the [[codomain]] [[model category]].

Let 

* $C$ be a [[small category|small]] [[sSet]]-[[enriched category]];	

* $A$ a [[combinatorial simplicial model category]] and 

  $A^\circ$ its [[full subcategory|full]] [[sSet-enriched category|sSet-]][[subcategory]] of [[bifibrant objects]];

* $[C,A]$ the [[sSet]]-[[enriched functor category]] equipped with the projective[^1] [[global model structure on functors]], and
  
  $[C,A]^\circ$ its full [[sSet]]-[[subcategory]]  on [[bifibrant objects]].

* $N \colon sSet\text{-}Cat \to sSet$ the [[homotopy coherent nerve]]. 

[^1]: [Lurie's Remark 4.2.4.5](#Lurie) claims that Prop. \ref{PresentationByModelStructuresOnFunctors} also works also for the injective structure, but this is not so clear, see also [MO:q/440965](https://mathoverflow.net/q/440965/381).


[[right adjoints preserve limits|Since]]$\;N$ is a [[right adjoint]] it [[preserved limit|preserves]] [[products]] so that we obtain a morphism

\[
  \label{}
  N(C) \times N\big([C,A]\big) 
   \xrightarrow{\; \sim \;}
  N\big(C \times [C,A]\big)
   \xrightarrow{\; N(ev) \;}
  N(A)
\]

induced from the [[internal hom]]-[[adjunct]] of $Id \colon [C,A] \to [C,A]$.

Noticing that the [[bifibrant objects]] of $[C,A]$ are [[enriched functors]] that, in particular, take values in [[bifibrant objects]] of $A$, this restricts to a morphism of the form

$$
  N(C) \times N\big([C,A]^\circ\big) 
  \xrightarrow{\;\; N(ev) \;\;}
  N\big(A^\circ\big)
  \,,
$$

which, by the [[internal hom]]-[[adjunction]], corresponds to a morphism

$$
  N\big([C,A]^\circ\big) 
  \xrightarrow{\phantom{--}}
  sSet\big(
    N(C)
    ,\,  
    N(A^\circ)
  \big)
  \,.
$$

Here $A^\circ$ is [[Kan complex]]-[[enriched category|enriched]], by the [[axioms]] of an [[classical model structure on simplicial sets|$sSet_{Quillen}$-]][[enriched model category]], and so $N(A^\circ)$ is a [[quasi-category]]. Therefore we may write this as

$$
  \cdots 
  \;=\; 
  Func\big(
    N(C)
    ,\, 
    N(A^\circ)
  \big)
  \,.
$$


\begin{proposition}
\label{PresentationByModelStructuresOnFunctors}
This canonical morphism

\[
  \label{TheNerveComparisonEquivalence}
  N\big([C,A]^\circ\big) 
    \xrightarrow{\phantom{---}}
  Func\big(
    N(C)
    ,\,  
    N(A^\circ)
  \big)
\]

is an [[equivalence of (infinity,1)-categories|equivalence of $\infty$-categories]] in that it is a [[weak equivalence]] in the [[model structure for quasi-categories]].
\end{proposition}
This is [Lurie (2009), Prop. 4.2.4.4](#Lurie).

\begin{proof}
The strategy is to show that the objects on both sides are both [[exponential objects]] in the [[homotopy category]] of [[Joyal model structure|$sSet_{Joyal}$]], which, by the [uniqueness of adjoints](adjoint+functor#UniquenessOfAdjoints), implies that they are [[isomorphism|isomorphic]] in the homotopy category, which finally is equivalent to the statement to be proven.

That $Func\big(N(C), N(A^\circ)\big) \simeq \big(N(A^\circ)\big)^{N(C)}$
is an [[exponential object]] in the [[homotopy category]] is pretty immediate.

That the left hand is an isomorphic exponential follows from [Lurie 09, corollary  A.3.4.12](#Lurie), which asserts that for $C$ and $D$ [[sSet-enriched categories]] with $C$ [[cofibrant object|cofibrant]] and $A$ as above, we have that [[composition]] with the [[evaluation map]] induces a [[bijection]]

$$
  Hom_{Ho(sSet Cat)}\big(D, [C,A]^\circ\big)
  \xrightarrow{\simeq}
  Hom_{Ho(sSet Cat)}\big(C \times D, A^\circ\big)
  \,.
$$

Since $Ho(sSet Cat_{Bergner}) \simeq Ho(sSet_{Joyal})$ this 
identifies also $N\big([C,A]^\circ\big)$ with the exponential object in question.
\end{proof}


> The following proof is fresh, still needs double-checking.

\begin{corollary}
\label{CompatibilityOfModelPresentationWithPrecomposition}
  In the above situation, consider an [[sSet]]-[[enriched functor]] $f \,\colon\, C' \longrightarrow C$ between any [[small category|small]] [[sSet-enriched categories]]. Then under the identification of Prop. \ref{PresentationByModelStructuresOnFunctors} the two $\infty$-functors given by

1. [[homotopy coherent nerve]] of the [[derived functor]] $\mathbb{R}f^\ast$ of precomposition with $f$

1. the precomposition with the [[homotopy coherent nerve]] of $f$

are related by a [[natural equivalence]] of $\infty$-functors:

\begin{tikzcd}[sep=30pt]
  N\big(
    [C,A]^\circ
  \big)
  \ar[dd, "{ N\big( \mathbb{R}f^\ast \big) }"{description}]
  \ar[rr, "{ \sim }"]
  &&
  \mathrm{Func}\big(
    N(C)
    ,\,
    N(A^\circ)
  \big)
  \ar[dd, "{ N(f)^\ast }"{description}]
  \\ 
  \\
  N\big(
    [C',A]^\circ
  \big)
  \ar[uurr, Rightarrow, shorten=50pt, "{ \sim }"{sloped}]
  \ar[rr, "{ \sim }"]
  &&
  \mathrm{Func}\big(
    N(C')
    ,\,
    N(A^\circ)
  \big)
\end{tikzcd}

\end{corollary}
\begin{proof}
\label{ProofOfCompatibilityOfModelPresentationWithPrecomposition}
Consider the following diagram of [[simplicial sets]] (the outer ones being [[quasi-categories]]):


\begin{tikzcd}[
  row sep=30pt,
  column sep=20pt
]
  N\big(
    [C,A]^\circ
  \big)
  \ar[dr, hook]
  \ar[rrrr]
  \ar[ddddd, "{ N(\mathbb{R}f^\ast) }"{description} ]
  &[-10pt]
  &&
  &[-35pt]
  \mathrm{Func}\big(
    N(C)
    ,\,
    N(A^\circ)
  \big)
  \ar[dl, hook]
  \ar[ddddd, "{ N(f)^\ast }"{description}]
  \\
  &
  N\big(
    [C,A]
  \big)
  \ar[rr]
  \ar[dd, "{ N(f^\ast) }"{description} ]
  &&
  \mathrm{Func}\big(
    N(C)
    ,\,
    N(A)
  \big)
  \ar[dd, "{ N(f)^\ast }"{description}]
  \\
  \\
  &
  N\big(
    [C',A]
  \big)
  \ar[rr]
  \ar[d, "{ N(Q) }"{description}]
  \ar[dr, "{\mathrm{id}}"{description}, "{\ }"{name=t, swap}]
  &&
  \mathrm{Func}\big(
    N(C')
    ,\,
    N(A)
  \big)
  \\
  {}
  &
  N\big(
    [C',A]
  \big)
  \ar[r, "{ \mathrm{id} }"{description} ]
  \ar[to=t, Rightarrow]
  &
  N\big(
    [C',A]
  \big) 
  \ar[ur]
  && 
  \\[-10pt]
  N\big(
    [C',A]^\circ
  \big)
  \ar[ur, hook]
  \ar[rrrr]
  &&&&
  \mathrm{Func}\big(
    N(C')
    ,\,
    N(A^\circ)
  \big)
  \ar[uul, hook]
\end{tikzcd}

Here $Q$ denotes any [[functorial factorization|functorial]] [[cofibrant replacement]] (which exists, by [this Example](functorial+factorization#InCombinatorialModelCategories), since $[C',A]$ is a [[combinatorial model category]] by the above discussion) and the double arrow denotes  (the image under the hc-nerve of) the [[natural transformation]] with components the corresponding resolution equivalences $Q(\text{-}) \xrightarrow{\;\sim\;} (\text{-})$ (which are components of a [[natural transformation]], by the nature of [[functorial factorization]]). 

The left square commutes by the construction of right derived functors of [[right Quillen functors]] (eg. [this Prop.](Introduction+to+Homotopy+Theory#ComputationOfLeftRightDerivedFunctorsViaResolutions)) and the middle square is the [[naturality square]] of the comparison map discussed [above](#ModelCategoryPresentation). The remaining outer squares just exhibit the restriction to [[bifibrant objects]], as discussed above.
 
The total diagram is of the claimed from. It just remains to see that the 2-morphism filling it is really an equivalence, but this follows by Prop. \ref{EquivalencesDetectedOnObjects}.
\end{proof}


\linebreak

### Limits and colimits {#Limits}

For $C$ an ordinary [[category]] that admits small [[limit]]s and [[colimit]]s, and for $K$ a [[small category]], the [[functor category]] $Func(D,C)$ has all small limits and colimits, and these are computed objectwise. See [[limits and colimits by example]]. The analogous statement is true for $(\infty,1)$-categories of $(\infty,1)$-functors

\begin{proposition}
Let $K$ and $C$ be [[quasi-categories]], such that $C$ has all [[limit in a quasi-category|colimits]] indexed by $K$. 

Let $D$ be a small quasi-category. Then 

* The $(\infty,1)$-category $Func(D,C)$ has all $K$-indexed colimits;

* A morphism $K^\triangleright \to Func(D,C)$ is a colimiting cocone precisely if for each object $d \in D$ the induced morphism $K^\triangleright \to C$ is a colimiting cocone.

\end{proposition}


This is ([Lurie, corollary 5.1.2.3](#Lurie)).


### Equivalences


\begin{proposition}
\label{EquivalencesDetectedOnObjects}
**(equivalences of $\infty$-functors detected on objects)**
\linebreak
A morphism $\alpha$ in $Func(D,C)$ (that is, a [[natural transformation]]) is an [[equivalence in an (infinity,1)-category|equivalence]] if and only if each component $\alpha_d$ is an equivalence in $C$.  
\end{proposition}

This is due to [Joyal (2008), Chapter 5, Theorem C ([p. 125](https://ncatlab.org/nlab/files/JoyalTheoryOfQuasiCategories.pdf#page=125))](#Joyal08).


## Examples

* Between ordinary categories, it reproduces the ordinary [[category of functors]].

* Since the standard [[model structure on simplicial sets]] presents [[∞Grpd]] 

  $$
    (sSet_{Quillen})^\circ \simeq \infty Grpd
  $$

  the [[model structure on simplicial presheaves]] (more precisely and more generally the [[model structure on sSet-enriched presheaves]]) on the [[opposite (∞,1)-category]] $C^{op}$ [[presentable (infinity,1)-category|presents]] the [[(∞,1)-category of (∞,1)-presheaves]] on $C$:

  $$
    N([C^{op},sSet_{Quillen}]^\circ) \simeq Func(C^{op},\infty Grpd)
    = PSh_{(\infty,1)}(C)
    \,.
  $$

## Related concepts

* [[functor category]]

* [[2-functor 2-category]]

## References

The intrinsic definition is in section 1.2.7 of

* {#Lurie} [[Jacob Lurie]], _[[Higher Topos Theory]]_
 

The discussion of [[model category]] models is in A.3.4.

The theorem about equivalences (Prop. \ref{EquivalencesDetectedOnObjects}) is due to:

* {#Joyal08} [[André Joyal]], *[[The Theory of Quasi-Categories and its Applications]]*, lectures at *[Advanced Course on Simplicial Methods in Higher Categories](https://lists.lehigh.edu/pipermail/algtop-l/2007q4/000017.html)*, CRM (2008) &lbrack;[pdf](http://mat.uab.cat/~kock/crm/hocat/advanced-course/Quadern45-2.pdf), [[JoyalTheoryOfQuasiCategories.pdf:file]]&rbrack;


[[!redirects (∞,1)-category of (∞,1)-functors]]

[[!redirects (∞,1)-categories of (∞,1)-functors]]

[[!redirects (infinity,1)-functor category]]
[[!redirects (infinity,1)-functor categories]]

[[!redirects (infinity,1)-functor (infinity,1)-category]]
[[!redirects (infinity,1)-functor (infinity,1)-categories]]


[[!redirects functor (infinity,1)-category]]
[[!redirects (∞,1)-functor categories]]
[[!redirects functor (∞,1)-categories]]
[[!redirects (infinity,1)-functor category]]
[[!redirects functor (infinity,1)-category]]
[[!redirects (∞,1)-functor categories]]
[[!redirects functor (∞,1)-categories]]
[[!redirects functor (∞,1)-category]]

[[!redirects (∞,1)-functor (∞,1)-category]]
[[!redirects (∞,1)-functor (∞,1)-categories]]

[[!redirects infinity1-category of infinity1-functors]]

