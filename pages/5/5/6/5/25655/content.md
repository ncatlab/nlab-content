+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

$n$-Trusses are the [[fundamental categories]] of [[n-mesh|$n$-meshes]]. They are central to the combinatorial classification of [[manifold diagrams]] and play an important role in [[framed combinatorial topology]].

## Definition

Trusses in $n$-dimensions, or $n$-trusses for short, are defined inductively in the dimension $n$.

### 1-Trusses

\begin{defn} 
A _1-truss_ $T \equiv (T,\leq, \preceq, \mathrm{dim})$ is a set $T$ with two [[partial orders]] (the 'face' order $\leq$ and the 'frame' order $\preceq$) as well as a 'dimension' map $\dim : (T,\leq) \to [1]^{\mathrm{op}}$ such that

1. $(T,\preceq) \cong [n] = (0 \to 1 \to ... \to n)$
2. either $i \lt i+1$ or $i + 1 \lt i$ for all $i \prec n$
3. $\dim$ is [[conservative]].

\end{defn}

\begin{defn} \label{defn_1-truss_maps} A _1-truss map_ $F : T \to S$ is a function of sets that preserves both face and frame order. Further,

* $F$ is called _regular_ if $\dim \circ F \Rightarrow \dim$,
* $F$ is called _singular_ if $\dim \circ F \Leftarrow \dim$,
* $F$ is called _dimension-preserving_ if $\dim \circ F = \dim$,

where $\Rightarrow$ and $\Leftarrow$ denote [[natural transformations]] of functors $(T,\leq) \to [1]^{\mathrm{op}} = (0 \leftarrow 1)$.
\end{defn}


\begin{notn} Given a truss $T$, denote by $T_{(i)}$ the subset of objects $x$ with $\dim(x) = i$. 
\end{notn}

### 1-Truss bundles

To define bundles of 1-trusses, we first define what are the valid fiber transitions. We dub these '1-truss bordisms'.

\begin{rmk} Below, a _Boolean profunctor_ is an ordinary [[profunctor]] $H : C$ &#8696; $D$ whose values are either the initial set $\emptyset \equiv \bot$ or the terminal set $\ast \equiv \top$. If $C$ and $D$ are [[discrete category|discrete]], then such a profunctor $H$ is simply a relation of sets. In this case, we call the profunctor $H$ a _function_ if it is a functional relation or a _cofunction_ if the dual profunctor $H^{\mathrm{op}}$ is a function.
\end{rmk}

\begin{rmk} \label{rmk_poset_maps_yield_profunctors} For any map of [[posets]] $F : P \to Q$, the fiber $F^{-1}(x \to y)$ over an arrow $x \to y$ of $Q$ defines a Boolean profunctor $F^{-1}(x)$ &#8696; $F^{-1}(y)$ by mapping $(a,b)$ to $\top$ iff $a \to b$ is an arrow in $P$.
\end{rmk}

\begin{defn} Given 1-trusses $T$ and $S$, a _1-truss bordism_ $R : T$ &#8696; $S$ is a Boolean profunctor $T$ &#8696; $S$ satisfying the following:
    
1. $R$ restricts to a function $R_{(0)} : T_{(0)}$ &#8696; $S_{(0)}$ and a cofunction $R_{(1)} : T_{(1)}$ &#8696; $S_{(1)}$.
2. Whenever $R(t,s) = \top = R(t',s')$, then either $t \prec t'$ or $s' \prec s$ but not both.

\end{defn}

Importantly, 1-truss bordisms are morphisms of a category $\mathfrak{T}^1$ that embeds into the category of [[Prof|profunctors]] $\mathbf{Prof}$ (unlike general Boolean profunctors). See the discussion of 'labels' [below](#labels) for details.

\begin{defn} \label{defn_1-truss_bundle}  A _1-truss bundle_ over a 'base' poset $(P,\leq)$ is a poset map $q : (T,\leq) \to (P,\leq)$ in which, for each $x \in P$, the fiber $(T^x,\leq) = q^{-1}(x)$ is equipped with the additional structures $(\preceq,\dim)$ of a 1-truss, and, for each arrow $x \to y$ in $P$, the fiber $q^{-1}(x \to y)$ is a 1-truss bordisms $T^x$ &#8696; $T^y$ (cf. Rmk. \ref{rmk_poset_maps_yield_profunctors}).
\end{defn}

\begin{defn} A _1-truss bundle map_ $F : q_1 \to q_2$ of 1-truss bundles $q_i : T_i \to P_i$ is a map $F : T_1 \to T_2$ that factors through $q_i$ by a 'base' map $F_0 : P_1 \to P_2$, such that $F$ is fiberwise a 1-truss map (cf. Def. \ref{defn_1-truss_maps}). 
We further say $F$ is regular resp. singular resp. dimension-preserving if it is fiberwise so.
\end{defn}

### n-Truss bundles and n-trusses

\begin{defn} An _$n$-truss bundle_ $T$ over a poset $P$ is a tower of 1-truss bundles (see Def. \ref{defn_1-truss_bundle})
\begin{center}
\begin{tikzcd}
	{T_n} & {T_{n-1}} & \cdots & {T_1} & {T_0 = P}
	\arrow["{q_n}", from=1-1, to=1-2]
	\arrow["{q_{n-1}}", from=1-2, to=1-3]
	\arrow["{q_2}", from=1-3, to=1-4]
	\arrow["{q_1}", from=1-4, to=1-5]
\end{tikzcd}
\end{center}
\end{defn}

{#n-truss_bundle_map}
\begin{defn} An _$n$-truss bundle map_ $F : T \to T'$ is a tower of 1-truss bundle maps $F_i : q_i \to q'_i$ where $F_{i-1}$ is the base map of $F_i$ and $F_n \equiv F : T_n \to T'_n$. The adjectives 'regular' resp. 'singular' resp. 'dimension-preserving' apply to $F$ if they apply to all $F_i$. If $T$ and $T'$ have the same base $P$, then $F$ is called _base-preserving_ if $F_0 = \mathrm{id}_P$.
\end{defn}

\begin{terminology} An $n$-truss bundle over the terminal poset $\ast$ is called an _$n$-truss_.
\end{terminology}

We can think of $n$-trusses as the 'fibers' of $n$-truss bundles: indeed, given an $n$-truss bundle $p$ over $P$, then any point $x \in P$ determines an $n$-truss by (iteratively) restricting $p$ over $\{x\}$.


{#labels}
## Labels and classifying categories

### Truss bundles with labels

\begin{defn} Given a [[category]] $C$, a _$C$-labeled $n$-truss bundle_ $T = (\underline T, \mathsf{lbl}_T)$ over $P$ consists of an 'underlying' $n$-truss bundle $\underline T = (T_n \to ... \to T_1 \to P)$ together with a 'labeling' functor $\mathsf{lbl}_T : T_n \to C$. In other words, $T$ is of the form
\begin{center}
\begin{tikzcd}
	C & {T_n} & {T_{n-1}} & \cdots & {T_1} & {T_0 = P}
	\arrow["{q_n}", from=1-2, to=1-3]
	\arrow["{q_{n-1}}", from=1-3, to=1-4]
	\arrow["{q_2}", from=1-4, to=1-5]
	\arrow["{q_1}", from=1-5, to=1-6]
	\arrow["{\mathsf{lbl}_C}"', from=1-2, to=1-1]
\end{tikzcd}
\end{center}
\end{defn}

\begin{rmk} If $C = \ast$ is the terminal category in the previous definition, then we recover ordinary $n$-truss bundles.
\end{rmk}

\begin{defn} A _labeled $n$-truss bundle map_ $F = (\underline F, \mathsf{lbl}_F) : T \to T'$ from a $C$-labeled $n$-truss bundle $T$ to a $C'$-labeled $n$-truss bundle $T'$ consists of an $n$-truss bundle map $\underline F : \underline T \to \underline T'$ and a functor $\mathsf{lbl}_F : C \to C'$ such that $\mathsf{lbl}_{T'} \circ \underline F \cong \mathsf{lbl}_F \circ \mathsf{lbl}_{T}$ commutes up to natural isomorphism. Adjectives 'regular', 'singular', 'dimension-preserving', 'base-preserving' apply if they apply to $\underline F$. Further, we say $F$ is _label-preserving_ if $\mathsf{lbl}_F = \mathrm{id}_C$.
\end{defn}

Labeled truss bundles are a central ingredient in truss theory as the next section will demonstrate.

### Truss bundle classifications

Since fiber transitions in 1-truss bundles are 1-truss bordisms, it comes as no surprise that the category of 1-truss bordisms classifies 1-truss bundles.

\begin{defn}
Given 1-truss bordisms $R : T$ &#8696; $S$ and $Q : S$ &#8696; $U$, their composite profunctor $R \circ Q$  (composed as ordinary profunctors) is again a 1-truss bordism. (In contrast, composites of general Boolean profunctors (composed as ordinary profunctors) in general need not themselves be Boolean.) This defines the _category $\mathfrak{T}^1$ of 1-trusses and their bordisms_.
\end{defn}

\begin{thm} $1$-truss bundles over a base poset $P$ up to dimension-preserving base-preserving isomorphism bijectively correspond to functors $P \to \mathfrak{T}^1$ up to natural isomorphism.
\end{thm}

\begin{proof} Follows from the definition of 1-truss bundles.
\end{proof}

(There are also more categorical phrasings of this theorem, as well as the subsequent theorems below, which replace [[bijection]] with categorical [[equivalence]]; see e.g. [Dorn-Douglas 2021, Ch. 2](#DornDouglas21).)

The theorem now generalizes to labelled 1-truss bundles as follows.

\begin{defn}
Given a category $C$, the _category $\mathfrak{T}^1(C)$ of $C$-labeled 1-trusses and their bordisms_ is defined as follows: objects of $\mathfrak{T}^1(C)$ are $C$-labeled 1-truss bundles over $[0]$; morphisms are $C$-labeled 1-truss bundles over $[1]$ (with domain and codomain given by restricting to fibers over  $0$ resp. $1$); two morphisms compose to a third iff there is a $C$-labeled bundle over $[2]$ that restricts over $(0 \to 1)$, $(1 \to 2)$, and $(0 \to 2)$ to the first, second, resp. third morphism.
The fact that this defines a category is shown in [Dorn-Douglas 2021, Sec. 2.3.1](#DornDouglas21).
\end{defn}

\begin{thm} $C$-labelled $1$-truss bundles over a base poset $P$ up to dimension-preserving base-preserving label-preserving isomorphism bijectively correspond to functors $P \to \mathfrak{T}^1(C)$ up to natural isomorphism.
\end{thm}

\begin{proof} Follows from the definition of $\mathfrak{T}^1(C)$.
\end{proof}

\begin{rmk} _(Recovering the unlabeled case)_. In particular, the preceding two definitions coincide $\mathfrak{T}^1(\ast) \cong \mathfrak{T}^1$ up to (essentially unique!) isomorphism of categories when $C = \ast$ is terminal.
\end{rmk}

\begin{rmk} _(Functoriality of labeled bordism)_.
Importantly, the construction of $\mathfrak{T}(C)$ is functorial in $C$. Indeed, given a functor $F : C \to D$, then $\mathfrak{T}^1(F) : \mathfrak{T}^1(C) \to \mathfrak{T}^1(D)$ acts on objects and morphisms of $\mathfrak{T}^1(C)$ by post-composing their labelings with $F$. This yields the _labeled bordism_ functor
$$
    \mathfrak{T}^1 : \mathbf{Cat} \to \mathbf{Cat}
$$
\end{rmk}


For a given category $C \in \mathbf{Cat}$ we can thus apply the labeled bordism functor $n$ times to it: the resulting category $\mathfrak{T}^n(C)$ classifies $C$-labeled $n$-truss bundless as follows.

\begin{thm} $C$-labelled $n$-truss bundles over a base poset $P$ up to dimension-preserving base-preserving label-preserving isomorphism bijectively correspond to functors $P \to \mathfrak{T}^n(C)$ up to natural isomorphism.
\end{thm}

\begin{proof} Inductively apply the previous theorem, starting with the highest 1-truss bundle and working your way downwards.
\end{proof}

\begin{rmk} _($n$-Truss bundles over categories)_. The theorem makes it evident that nothing would have stopped us from defining $n$-truss bundles over _categories_ $B$ (in place of just posets): indeed, such bundles may be thought of as functors $B \to \mathfrak{T}^n(\ast)$ (or $B \to \mathfrak{T}^n(C)$ in the labeled case).
\end{rmk}

[[Lukas Heidemann]] points out the following nice perspective on the labeled bordism functor.

\begin{rmk} _(Universal construction of the labeled bordism functor)_ Applying the [[Conduché functor#conduch_functors_and_2functors_to_prof|profunctorial Grothendieck construction]] to the (frame-order-forgetting) functor $\mathfrak{T}^1 \to \mathbf{Prof}$, yields an [[Conduché functor|exponentiable fibration]] $E\mathfrak{T}^1 \to \mathfrak{T}^1$. By general nonsense, the composition of the pullback $\mathbf{Cat}_{/ \mathfrak{T}^1} \to \mathbf{Cat}_{/ E\mathfrak{T}^1}$ and forgetful functor $\mathbf{Cat}_{/ E\mathfrak{T}^1} \to \mathbf{Cat}$ has a right adjoint $\mathbf{Cat} \to \mathbf{Cat}_{/ \mathfrak{T}^1}$; this adjoint is exactly the functor $C \mapsto \mathfrak{T}^1(C \to \ast)$. (Note: more generally, this construction applies to all [[normal]] [[pseudofunctors]] $H : D \to \mathbf{Prof}$, where it characterizes the constructions of 'vertical comma categories' $H_{/\!/ C}$ for such functors $H$ (see [Dorn-Douglas 20, Term. 2.3.18](#DornDouglas21)) as right adjoints.)
\end{rmk}

\begin{rmk} _(Labels in $\infty$-categories)_ The construction of $\mathfrak{T}^1(-)$ generalizes to an endofunctor on $\infty$-categories $\mathbf{Cat}_\infty$, which immediately leads to a notion of truss bundles labeled in $\infty$-categories.
\end{rmk}

Thus there is a 'spectrum' of base/label structures on which we can reasonably consider truss bundles, ranging from posets over to categories to $\infty$-categories. Most of the theory works the same across the spectrum. In this article, we work  with the simplest possible choice, i.e. with posets (initially as base structure, but later even as label structures for the purpose of defining 'stratifications').

### Normalization theorem

Another important part of truss theory is normalization.

{#normalizing_map}
\begin{defn} Given $C$-labeled $n$-truss bundles $T$ and $T'$ over $P$, a _normalizing map_ $F : T \to T'$ is a labeled $n$-truss bundle map which is:

1. regular;
2. endpoint-dimension-preserving, meaning it is dimension-preserving on the _endpoints_ of all 1-truss fibers;
3. base-preserving;
4. label-preserving-on-the-nose, meaning that $\mathsf{lbl}_F = \mathrm{id}$ and $\mathsf{lbl}_{T'} \circ F = \mathsf{lbl}_{T}$ commutes strictly.

\end{defn}

(There's a dual version of the definition that replaces 'regular' by 'singular'; cf. the section on 'duality' [below](#duality).)

\begin{terminology} We sometimes write normalizing maps as $F : T \underset{\mathsf{norm}}{\longrightarrow} T'$, and say $T'$ is a _reduct_ of $T$.
\end{terminology}

\begin{terminology} A labeled truss whose only reduct is itself is called _normalized_ (or, said to be _in normal form_).
\end{terminology}

\begin{thm}(Normalization ends in normal forms). The category $\mathsf{Norm}(T)$ of reducts of $T$ and normalizing maps between them has a unique terminal object $[[T]]$ (called the normal form of $T$).
\end{thm}

Various proofs have been given, the first in [Dorn 2018, 5.2.2](#Dorn18) (in the case of open trusses, see Def. \ref{defn_open_trusses}, in which case condition 2. is implied by condition 1. above; the proof generalizes to the case of general trusses, however.), and another (shorter) proof in [Heidemann-Reutter-Vicary 2022](#HRV22) (also for open trusses).

A geometric derivation and interpretation of the normalization theorem can be given in terms of 'the existence of coarsest subdividing framed regular cell complexes of stratification in framed $\mathbb{R}^n$', see [Dorn-Douglas 2021, Ch. 5](#DornDouglas21).

## Combinatorialization theorems

Trusses are the combinatorial analogues (namely, the [[fundamental category|fundamental categorical structures]]) of certain framed stratified topological structures. We describe how this works in two examples.

### Combinatorial meshes

Bare (unlabeled) trusses are combinatorial analogues of [[meshes]]. The relation is given by the following theorem.

\begin{thm} $n$-Meshes up to framed stratified homeomorphism bijectively correspond to $n$-trusses.
\end{thm}

**Proof sketch**. Given an [[n-mesh|$n$-mesh]] $M$
\begin{center}
\begin{tikzcd}
	{M_n} & {M_{n-1}} & \cdots & {M_1} & {\ast}
	\arrow["{p_n}", from=1-1, to=1-2]
	\arrow["{p_{n-1}}", from=1-2, to=1-3]
	\arrow["{p_2}", from=1-3, to=1-4]
	\arrow["{p_1}", from=1-4, to=1-5]
\end{tikzcd}
\end{center}
apply to it the [[stratified space#the_category_of_stratifications|entrance path poset functor]] $\mathsf{Entr}(-)$ to obtain the corresponding $n$-truss
\begin{center}
\begin{tikzcd}
	{\mathsf{Entr}(M_n)} & {\mathsf{Entr}(M_{n-1})} & \cdots & {\mathsf{Entr}(M_1)} & {\ast}
	\arrow["{\mathsf{Entr}(p_n)}", from=1-1, to=1-2]
	\arrow["{\mathsf{Entr}(p_{n-1})}", from=1-2, to=1-3]
	\arrow["{\mathsf{Entr}(p_2)}", from=1-3, to=1-4]
	\arrow["{\mathsf{Entr}(p_1)}", from=1-4, to=1-5]
\end{tikzcd}
\end{center}
(framings and strata dimensions of the mesh canonically induce the required truss structures $\preceq$ and $\dim$). $\square$


\begin{rmk} The theorem has various (more categorical) generalizations, which essentially capture versions of the equivalence
$$
    \mathcal{M}\mathit{esh}_n(B,g) \simeq \mathsf{Truss}_n(\mathcal{E}\mathit{ntr}(B,g))
$$
of the $\infty$-category of mesh bundles over a base stratification $(B,g)$ and the $\infty$-category of truss bundles over the entrance path $\infty$-category $\mathcal{E}\mathit{ntr}(B,g)$ of $g$ (recall, entrance path $\infty$-categories are the duals of [[stratified space#fundamental_categories|exit path $\infty$-categories]]). See [Dorn-Douglas 2021, Ch. 4](#DornDouglas21) for details.
\end{rmk}

{#comb_mdiag}
### Combinatorial manifold diagrams

Certain labeled trusses are the 'combinatorial' analogues of [[manifold diagrams]]. We first define the class of labeled trusses we are interested in. We need four ingredients:

1. Truss stratifications (special case of labelings) 
2. Open trusses (special type of trusses)
3. Open truss neighborhoods and stratifed neighborhoods
4. Truss products (or, more specifically, 'cylinders')

\begin{rmk} (Stratifying posets). Recall a characteristic map $f : X \to \mathsf{Entr}(f)$ of a stratification $(X,f)$ maps points in a stratum $s$ to the corresponding poset element $s \in \mathsf{Entr}(f)$. Considering posets $P$ as spaces (by their [[specialization topology]], with the convention that downward closed subposets are open), we may equally consider stratified posets by characteristic maps $f : P \to \mathsf{Entr}(f)$. Such characteristic maps are exactly poset maps which are poset quotients with connected preimages (see [Dorn-Douglas 2021, App. B.1](#DornDouglas21)).
\end{rmk}

\begin{defn} (Stratified truss). A _stratified $n$-truss_ $T$ is a labeled $n$-truss $T$ whose labeling $\mathsf{lbl}_T$ is a characteristic map.
\end{defn}

{#open_trusses}
\begin{defn} \label{defn_open_trusses} (Open truss). A 1-truss is called _open_ if its endpoint have dimension 1. A (labeled) $n$-truss $T$ is called open if all 1-truss fibers in all 1-truss bundles that comprise $T$ are open.
\end{defn}

\begin{defn} (Open neigborhood). Given an open $n$-truss $T$ and an element $x \in T_n$, define the _neighborhood_ $T^{\leq x}$ of $x$ to be the unique open truss that comes with a dimension-preserving map $F : T^{\leq x} \hookrightarrow T$ such that $F : T^{\leq x}_n \hookrightarrow T_n$ is an inclusion of the downward closure of $x$ into the poset $(T_n,\leq)$.
\end{defn}

{#atomic_trusses_terminology}
\begin{terminology} (Atomic truss). Given an open $n$-truss $T$ with $x \in T_n$ such that $T^{\leq x} = T$, we say $T$ is an _atomic_ open $n$-truss with _cone point_ $x$ (in [Dorn-Douglas 2021, Ch. 2](#DornDouglas21), atomic trusses are called 'truss braces').
\end{terminology}

\begin{defn} (Stratified open neighborhood). Given a stratified open $n$-truss $T$ and an element $x \in T_n$, define the _stratified neighborhood_ $T^{\leq x}$ to be the unique stratified trusses that stratified embeds in $T$ with underlying truss map being the (non-stratified) neighborhood inclusion of $x$.
\end{defn}

\begin{terminology} (Cone types). A stratified open $n$-truss $T$ is said to be a _combinatorial cone type_ if the underlying truss of $T$ is atomic with cone point $x$, and $\{x\} = \mathsf{lbl}^{-1}\circ \mathsf{lbl}(x)$ (in words: '$x$ is its own stratum').
\end{terminology}

\begin{defn} (Cylinders). Given a labeled $m$-truss $T$ defined the _$k$-cylinder_ $\mathbb{I}^k \times T$ of $T$ to be the labeled $(m+k)$ obtained from $T$ be adding $k$ trivial truss bundles $\ast \to \ast$ to its underlying truss.
\end{defn}

\begin{rmk} (Products). More generally, one can similarly define labeled $(k+m)$-trusses $U \times T$ as _products_ between unlabeled $k$-trusses $U$ and labeled $m$-trusses $T$.
\end{rmk}

Recall the definition of [[manifold diagrams]]: these are framed conical (compactly triangulable) stratifications. Putting the preceding notions together, we obtain a combinatorial version of framed conicality as follows.

\begin{defn} A _combinatorial manifold $n$-diagram_ $T$ is a stratifed open $n$-truss such that for all $x \in T$ we have
$$
    [[T^{\leq x}]] = \mathbb{I}^k \times C_x
$$
where $C_x$ is a combinatorial cone type.
\end{defn}

\begin{thm} Manifold diagrams, up to framed stratified homeomorphism, bijectively correspond to normalized combinatorial manifold $n$-diagrams.
\end{thm}

**Proof sketch**. Given a manifold $n$-diagram $(\mathbb{R}^n,f)$ its corresponding normalized combinatorial manifold $n$-diagram can be constructed by first refining $f$ by the unique coarsest $n$-mesh $M$, and then labeling the $n$-truss $\mathsf{Entr}(M)$ with the labeling $\mathsf{Entr}(M \to f)$. $\square$

(See [Dorn-Douglas 2022, Sec. 2](#DornDouglas22) for details.)


{#duality}
## Duality

There is a [[covariant functor|covariant]] _dualization functor_
$$
    \dagger : \mathsf{Truss}_n \to \mathsf{Truss}_n
$$
from the category of $n$-trusses and $n$-truss maps to itself: the functor is defined by dualizing orders $\leq \mapsto \leq^{\mathrm{op}}$ and fiberwise replacing dimension maps $\dim \mapsto \dim^{\mathrm{op}}$ (using that $[1]^{\mathrm{op op}} \cong [1]^{\mathrm{op}}$ uniquely).

Dualization of $n$-trusses is an [[involution]]. It maps:

1. Singular maps to regular maps and vice-versa
2. Open trusses to _closed_ trusses and vice-versa

Geometrically, dualization dualizes stratifications in the sense of [[Poincare duality]], which can for instance be used to translate between [[manifold diagrams]] and cellular [[pasting diagrams]]. This is discussed in e.g. in [Dorn-Douglas 2022](#DornDouglas22).

Dualization can also be applied to truss bordisms, where it yields a [[contravariant functor|contravariant]] _dualization_ functor:

$$
    \dagger : \mathfrak{T}^n \to (\mathfrak{T}^n)^{\mathrm{op}}
$$

(or, in the labeled case: $\dagger : \mathfrak{T}^n(C) \to (\mathfrak{T}^n(C^{\mathrm{op}}))^{\mathrm{op}}$.)



## Related concepts

* [[n-mesh|n-mesh]]
* [[manifold diagram|manifold diagram]]
* [[manifold-diagrammatic n-category]]
* [[framed combinatorial topology]]

## References


* {#Dorn18} [[Christoph Dorn]], _Associative $n$-categories_, PhD thesis ([arXiv:1812.10586](https://arxiv.org/abs/1812.10586)).

* {#DornDouglas21} [[Christoph Dorn]] and [[Christopher Douglas]], _Framed combinatorial topology_, 2021 ([arXiv](https://arxiv.org/abs/2112.14700), [latest](https://cxdorn.github.io/fct-book/))

* {#HRV22} [[Lukas Heidemann]], [[David Reutter]], [[Jamie Vicary]], *Zigzag normalisation for associative $n$-categories*, Proceedings of the Thirty-Seventh Annual ACM/IEEE Symposium on Logic in Computer Science (LICS 2022) &lbrack;[arXiv:2205.08952](https://arxiv.org/abs/2205.08952), [doi:10.1145/3531130.3533352](https://dl.acm.org/doi/10.1145/3531130.3533352)&rbrack;

* {#DornDouglas22} [[Christoph Dorn]] and [[Christopher Douglas]], _Manifold diagrams and tame tangles_, 2022 ([arXiv](https://arxiv.org/abs/2208.13758), [latest](https://cxdorn.github.io/manifold-diagram-paper/))



[[!redirects n-trusses]]
[[!redirects trusses]]