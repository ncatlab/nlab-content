
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea 

_Geometric realization_ is the operation that builds from a [[simplicial set]] $X$ a [[topological space]] $|X|$ obtained by interpreting each 
element in $X_n$ -- each abstract $n$-simplex in $X$ -- as one copy of the standard topological $n$-simplex $\Delta^n_{Top}$ and then gluing together all these along their boundaries to a big topological space, using the information encoded in the face and degeneracy maps of $X$ on how these simplices are supposed to be stuck together. It generalises the geometric realization of [[simplicial complex]]es as described at that entry.

This is the special case of the general notion of [[nerve and realization]] that is induced from the standard [[simplicial set|cosimplicial]] [[topological space]] $[n] \mapsto \Delta^n_{Top}$. (N.B.: in this article, $[n]$ denotes the ordinal with $n+1$ elements. The corresponding contravariant representable is denoted $\Delta(-, n)$.) 

In the context of [[homotopy theory]] geometric realization plays a notable role in the [[homotopy hypothesis]], where it is part of the [[Quillen equivalence]] between the [[model structure on topological spaces]] and the standard [[model structure on simplicial sets]].

The construction generalizes naturally to a map from [[simplicial object|simplicial]] [[topological space]]s to plain topological spaces. For more on that see [[geometric realization of simplicial spaces]].

The dual concept is _[[totalization]]_ . 

## Definition

There are various levels of generality in which the notion of (topological) geometric realization makes sense. The basic definition is 

* [For cell complexes such as simplicial sets](#OfSimplicialSets).

A generalization of this of central importance is the

* [Geometric realization of simplicial topological spaces](#OfSimplicialTopologicalSpaces)

Up to homotopy, this is a special case of a general notion of

* [Geometric realization of cohesive ∞-groupoids](#OfCohesiveInfinityGroupoids).

At the point-set level, it is also a special case of a general notion of

* [Geometric realization of simplicial objects](#OfSimplicialObjects).


### Of cell complexes such as simplicial sets
 {#OfSimplicialSets}

Let $S$ be one of the categories of [[geometric shapes for higher structures]], such as the [[globe category]] or the [[simplex category]] or the [[cube category]].

There is an obvious functor

 $ st : S \to $ [[Top]]

which sends the standard _cellular_ shape $[n]$ (the standard cellular [[globe]], [[simplex]] or [[cube]], respectively) to the corresponding standard _topological_ shape (for instance  the standard $n$-simplex $ st([n]) := \{ (x_1, \cdots, x_n) | \sum_{i=1}^n x_i = 1, x_i \geq 0 \} \subset \mathbb{R}^{n}$ ) with the obvious induced face and boundary maps.

Using this, in cases where $Top$ can be regarded as [[enriched category|enriched]] over and [[copower|tensored]] over a base category $V$, the **geometric realization** of a [[presheaf]] $K^\bullet : S^{op} \to V$ on $S$ -- e.g., of a [[globular set]], a [[simplicial set]] or a [[cubical set]], respectively  (when $V= Set$) -- is the [[topological space]] given by the [[end|coend]], [[weighted limit|weighted colimit]], or [[tensor product of functors]]

$$
  |K^\bullet| = \int^{[n] \in S} st([n]) \cdot K^n
  \,.
$$

In the case of [[simplicial sets]], see for more discussion also

* [[nerve]], [[homotopy hypothesis]].

Via simplicial [[nerve]] functors geometric realization of simplicial sets induces geometric realizations of many other structures, for instance

* [[geometric realization of categories]]

For the case of [[cubical set|cubical sets]], see [[cubical geometric realisation]].

### Of simplicial topological spaces
 {#OfSimplicialTopologicalSpaces}


See

* [[geometric realization of simplicial topological spaces]]


### Of cohesive $\infty$-groupoids
 {#OfCohesiveInfinityGroupoids}

Every [[cohesive (∞,1)-topos]] $\mathbf{H}$ (in fact every [[locally ∞-connected (∞,1)-topos]]) comes with its intrinsic notion of geometric realization.

The general abstract definition is at [[cohesive (∞,1)-topos]] in the section 
<a href="http://nlab.mathforge.org/nlab/show/cohesive+%28infinity%2C1%29-topos%20--%20structures#Homotopy">Geometric homotopy</a>.

For the choice $\mathbf{H} = $ [[∞Grpd]] this reproduces the [geometric realization of simplicial sets](#OfSimplicialSets), see at [[discrete ∞-groupoid]] the section <a href=""></a>

For the choice $\mathbf{H} = $  [[ETop∞Grpd]] and [[Smooth∞Grpd]] this reproduces [geometric realization of simplicial topological spaces](#OfSimplicialTopologicalSpaces). See the sections <a href="http://nlab.mathforge.org/nlab/show/Euclidean-topological+infinity-groupoid#GeometricHomotopy">ETop∞Grpd -- Geometric homotopy</a> and <a href="http://nlab.mathforge.org/nlab/show/smooth+infinity-groupoid#StrucGeometricHomotopy">Smooth ∞-groupoid --  Geometric homotopy</a>

### Of simplicial objects in a category
 {#OfSimplicialObjects}

Let $M$ be a [[cocomplete category|cocomplete]] [[simplicially enriched category]] with [[copowers]].  A **[[simplicial object]]** in $M$ is a functor $X:\Delta^{op}\to M$, where $\Delta$ is the [[simplex category]].  Its **geometric realization** is defined similarly to the classical case as a [[coend]]:

$$ |X| = \int^{[n]\in\Delta} \Delta[n] \odot X_n $$

where $\odot$ denotes the [[copower]] in $M$.  This operation is a left adjoint which is even a simplicially enriched functor; see [[simplicial object]] for more details.


## Properties ## 

In this section we consider topological [geometric realization of simplicial sets](#OfSimplicialSets), which is the best studied and perhaps most significant case. 

### Realizations as CW complexes ### 

Each ${|X|}$ is a CW complex (see lemma \ref{mono} below), and so geometric realization ${|(-)|}: Set^{\Delta^{op}} \to Top$ takes values in the full subcategory of CW complexes, and therefore in any [[convenient category of topological spaces]], for example in the category $CGHaus$ of compactly generated Hausdorff spaces. Let $Space$ be any convenient category of topological spaces, and let $i \colon Space \to Top$ denote the inclusion. 

+-- {: .un_prop} 
######Proposition
For any simplicial set $X$, there is a natural isomorphism $i(\int^{n: \Delta} X(n) \cdot \sigma(n)) \cong {|X|}$, where the coend on the left is computed in $Space$. 
=-- 

This is obvious: more generally, if $F: J \to A$ is a diagram and $i: A \hookrightarrow B$ is a full replete subcategory, and if the colimit in $B$ of $i \circ F$ lands in $A$, then this is also the colimit of $F$ in $A$. 
(The dual statement also holds, with limits instead of colimits.) 

Below, we let $R: Set^{\Delta^{op}} \to Space$ denote the geometric realization when considered as landing in $Space$. 

### Theorem: Geometric realization is left exact ### 
 {#GeometricRealizationIsLeftExact}

We continue to assume $Space$ is any [[convenient category of topological spaces]]. In this section we prove that geometric realization 

$$R: Set^{\Delta^{op}} \to Space$$ 

is a left [[exact functor]] in that it preserves [[finite limits]]. 

It is important that we use some such "convenience" assumption, because for example 

$${|(-)|}: Set^{\Delta^{op}} \to Top,$$

valued in general [[topological spaces]], does not preserve products. (To get a correct statement, one usual procedure is to "kelley-fy" products by applying the coreflection $k \colon Haus \to CGHaus$ to [[Hausdorff space|Hausdorff]] and [[compactly generated topological spaces]]. This gives the correct isomorphism in the case $Space = CGHaus$, where we have that ${|X \times Y|} \cong {|X|} \times_k {|Y|} \coloneqq k({|X|} \times {|Y|})$; the product on the right has been "kelleyfied" to the product appropriate for $CGHaus$.) 

We reiterate that $R$ denotes the geometric realization functor considered as valued in a convenient category of spaces, whereas ${|(-)|}$ is geometric realization viewed as taking values in $Top$. 

+-- {: .num_theorem #leftexact} 
###### Theorem 
Let $U = \hom(1, -): Space \to Set$ be the underlying-set functor. Then the composite $U R: Set^{\Delta^{op}} \to Set$ is left exact. 
=-- 

+-- {: .proof}
###### Proof
As described at the nLab article on triangulation [here](triangulation#StandardAffineSimplexFunctor), the composite 
$$\Delta \stackrel{\sigma}{\to} Space \stackrel{U}{\to} Set$$ 
can be described as the functor 
$$\Delta \cong FinInt^{op} \hookrightarrow Int^{op} \stackrel{Int(-, I)}{\to} Set$$ 
where $Int$ is the category of intervals (linearly ordered sets with distinct top and bottom). Because every interval, in particular $I$, is a [[filtered colimit]] of finite intervals, and because finite intervals are finitely presentable intervals, it follows that $U \sigma \colon \Delta \to Set$ is a [[flat functor]] (a [[filtered colimit]] of representables). But on general grounds, [[copower|tensoring]] with a flat functor is left exact, which in this case means 
$$U R = - \otimes_\Delta U \sigma: Set^{\Delta^{op}} \to Set$$
is left exact. 
=-- 

Obviously the preceding proof is not sensitive to whether we use $Space$ or $Top$. 

#### Geometric realization preserves equalizers 

+-- {: .num_lemma #mono}
###### Lemma 
If $i: X \to Y$ is a [[monomorphism]] of simplicial sets, then $R(i): R(X) \to R(Y)$ is a [[closed subspace]] inclusion, in fact a [[relative CW-complex]]. In particular, taking $X = \emptyset$, $R(Y)$ is a $CW$-complex. 
=-- 

+-- {: .proof} 
###### Proof 
Any monomorphism $i \colon X \to Y$ in $Set^{\Delta^{op}}$ can be seen as the result of iteratively adjoining nondegenerate $n$-simplices. In other words, there is a chain of inclusions $X = F(0) \hookrightarrow F(1) \hookrightarrow \ldots Y = colim_i F(i)$, where $F: \kappa \to Set^{\Delta^{op}}$ is a functor from some ordinal $\kappa = \{0 \leq 1\leq \ldots\}$ (as [[preorder]]) that preserves directed colimits, and each inclusion $F(\alpha \leq \alpha + 1): F(\alpha) \to F(\alpha + 1)$ fits into a pushout diagram 

$$\array{
\partial \Delta(-, n) & \to & F(\alpha) \\
\mathllap{j} \downarrow & & \downarrow \\
\Delta(-, n) & \to & F(\alpha+1)
}$$ 

where $j$ is the inclusion. Now $R(j)$ is identifiable as the inclusion $S^{n-1} \to D^n$, and since $R$ preserves pushouts (which are calculated as they are in $Top$), we see by [this lemma](/nlab/show/subspace+topology#pushout) that $R F(\alpha) \to R F(\alpha+1)$ is a closed subspace inclusion and evidently a [[relative CW-complex]]. By [another lemma](/nlab/show/subspace+topology#transfinite), it follows that $X \to Y$ is also a closed inclusion and indeed a relative CW-complex. 
=-- 

+-- {: .num_cor}
###### Corollary
$R: Set^{\Delta^{op}} \to Space$ preserves [[equalizers]]. 
=--

+-- {: .proof} 
###### Proof
The equalizer of a pair of maps in $Top$ is computed as the equalizer on the level of underlying sets, equipped with the subspace topology. So if 
$$E \stackrel{i}{\to} X \stackrel{\overset{f}{\longrightarrow}}{\underset{g}{\longrightarrow}} Y$$ 
is an equalizer diagram in $Set^{\Delta^{op}}$, then ${|i|}$ is the equalizer of the pair ${|f|}$, ${|g|}$, because the underlying function $U({|i|})$ is the equalizer of $U({|f|})$, $U({|g|})$ on the underlying set level by the preceding theorem, and because ${|i|}$ is a (closed) subspace inclusion by lemma \ref{mono}. But this $Top$-equalizer ${{|i|}}: {{|E|}} \to {{|X|}}$ lives in the full subcategory $Space$, and therefore $R(i) = {|i|}$ is the equalizer of the pair $R(f) = {|f|}$, $R(g) = {|g|}$. 
=-- 

As the proof indicates, that realization preserves equalizers is not at all sensitive to whether we use $Top$ or a convenient category of spaces $Space$. 

#### Geometric realization preserves finite products

That geometric realization preserves products _is_ sensitive to whether we think of it as valued in $Top$ or in a convenient category $Space$. In particular, the proof uses [[cartesian closed category|cartesian closure]] of $Space$ in an essential way (in the form that [[finite products]] distribute over arbitrary [[colimits]]). 

First, an easy result on products of simplices. 

+-- {: .num_lemma #product}
###### Lemma 
The realization of a product of two representables $\Delta(-, m) \times \Delta(-, n)$ is compact. 
=-- 

+-- {: .proof} 
###### Proof 
It suffices to observe that $\Delta[m] \times \Delta[n]$ has finitely many non-degenerate simplices. That is clear since non-degenerate $k$-simplices in the nerve of a poset $P$ are exactly injective order preserving maps $[k] \to P$.
=--


+-- {: .num_lemma #canonical} 
###### Lemma 
The canonical map 
$${|\Delta(-, m) \times \Delta(-, n)|} \to {|\Delta(-, m)|} \times {|\Delta(-, n)|}$$ 
is a homeomorphism.
=-- 

+-- {: .proof} 
###### Proof
The canonical map is continuous, and a bijection at the underlying set level by theorem \ref{leftexact}. The codomain is the compact Hausdorff space $\sigma(m) \times \sigma(n)$, and the domain is compact by Lemma \ref{product}. But a continuous bijection from a compact space to a Hausdorff space is a homeomorphism. 
=-- 

+-- {: .num_remark} 
###### Remark 
The key properties of $I$ needed for this subsection are (1) the fact it is compact Hausdorff, and (2) the order relation $\leq$ on the interval $I$ defines a closed subset of $I \times I$. These properties ensure that the affine $n$-simplex $\{(x_1, \ldots, x_n) \in I^n: x_1 \leq \ldots \leq x_n\}$ is itself compact Hausdorff, so that the proof of lemma \ref{canonical} goes through. The point is that in place of $I$, we can really use any interval $L$ that satisfies these properties, thus defining an $L$-based geometric realization instead of the standard ($I$-based) geometric realization being developed here. 
=-- 

+-- {: .num_theorem} 
###### Theorem 
The functor $R: Set^{\Delta^{op}} \to Space$ preserves products. 
=-- 

+-- {: .proof} 
###### Proof 
The proof is purely formal. Let $X$ and $Y$ be simplicial sets. By the [[co-Yoneda lemma]], we have isomorphisms 
$$X \cong \int^m X(m) \cdot \Delta(-, m)  \qquad Y \cong \int^n Y(n) \cdot \Delta(-, n)$$ 
and so we calculate 
$$\array{
R(X \times Y) & \cong & R((\int^m X(m) \cdot \Delta(-, m)) \times (\int^n Y(n) \cdot \Delta(-, n))) \\
 & \cong & R(\int^m \int^n X(m) \cdot Y(n) \cdot (\Delta(-, m) \times \Delta(-, n))) \\
 & \cong & \int^m \int^n X(m) \cdot Y(n) \cdot R(\Delta(-, m) \times \Delta(-, n)) \\
 & \cong & \int^m \int^n X(m) \cdot Y(n) \cdot (R(\Delta(-, m)) \times R(\Delta(-, n)) \\
 & \cong & \int^m \int^n X(m) \cdot Y(n) \cdot (\sigma(m) \times \sigma(n)) \\
 & \cong & (\int^m X(m) \cdot \sigma(m)) \times (\int^n Y(n) \cdot \sigma(n)) \\
 & \cong & R(X) \times R(Y)
}$$ 
where in each of the second and penultimate lines, we twice used the fact that $- \times -$ preserves colimits in its separate arguments (i.e., the fact that the nice category $Space$ is cartesian closed), and the remaining lines used the fact that $R$ preserves colimits, and also products of representables by lemma \ref{canonical}. 
=--

* A slightly higher-level rendition of the proof might look like this: 
$$\array{
R(X \times Y) & \cong & R((X \otimes_{\Delta} \hom) \times (Y \otimes_{\Delta} \hom)) \\
 & \cong & R((X \times Y) \otimes_{\Delta \times \Delta} (\hom \times \hom)) \\
 & \cong & (X \times Y) \otimes_{\Delta \times \Delta} R(\hom \times \hom) \\
 & \cong & (X \times Y) \otimes_{\Delta \times \Delta} (R(\hom) \times R(\hom)) \\
 & \cong & (X \otimes_{\Delta} R(\hom)) \times (Y \otimes_{\Delta} R(\hom)) \\
 & \cong & R(X \otimes_{\Delta} \hom) \times R(Y \otimes_{\Delta} \hom) \\
 & \cong & R(X) \times R(Y)
}$$


### A construction of Drinfeld of geometric realization as Hom([0,1],-)


[Drinfeld, On the notion of geometric realization](https://arxiv.org/abs/math/0304064) provides a conceptual explanation of preserving finite limits, and
"reformulates the definitions so that the following facts become obvious:

* geometric realization commutes with finite projective limits (e.g., with Cartesian products);

* the geometric realization of a simplicial set ... (resp. cyclic set) is 
equipped with an action of the group of orientation preserving homeomorphisms 
of the segment $I := [0, 1]$ ... (resp. the circle $S^ 1$)." 
(quote from the paper)

A draft [M.Gavrilovich, K.Pimenov. Geometric realisation as a Skorokhod semi-continuous path space endofunctor](http://mishap.sdf.org/Skorokhod_Geometric_Realisation.pdf) 
attempts to further reformulate this by showing that, in a certain precise sense, 
geometric realisation is an endofunctor of a certain category $sF$ of simplicial sets equipped 
with extra structure of topological nature (a notion of smallness). The underlying
endofunctor of $sSets$ is 
$$HHom ( Hom_{preorders}(-, [0,1]_\leq), Y_.) $$ 

The category $sF$ contains simplicial sets, topological and uniform spaces as full subcategories, 
and has forgetful functors $sF\to sSets$, $sF\to Top$, and $sF\to UniformSpaces$ such that
the following compositions are identity:
$sSets\to sF\to sSets$, $Top\to sF\to Top$, and $UniformSpaces\to sF\to UniformSpaces$. 
Moreover, this endofunctor seems to 
have the right adjoint, defined by the usual construction. 

Here are some details. The category $sF$ may be thought as the category of simplicial sets with 
 extra structure of topological nature, a notion of smallness. 
 Formally it is just the category of simplicial objects in the category of [[filters]]. 
 The endofunctor $HHom ( Hom_{preorders}(-, [0,1]_\leq), Y_.):sF\to sF $ 
 above is the inner hom of sSets equipped with an extra structure motivated by Skorokhod/Levi-Prokhorov convergence. 
 The precise claim is that the geometric realisation of sSets factors as 
$$ sSets  \to sF \to sF \to Top $$

 To gain some intuition, consider $Y_.=\Delta_n=Hom(-,[n])$ the standard simplex. Then
 by Remark  2.4.1-2 of [Grayson](http://www.math.uiuc.edu/~dan/Courses/2003/Spring/416/GraysonKtheory.pdf)
 the standard geometric simplex is the set of monotone functions $[0.1]\to [n]$
 $$Hom_{preorders}([0,1]_\leq), [n] ) = Hom ( Hom_{preorders}(-, [0,1]_\leq), \Delta_n )$$
 equipped with a metric 
 $$\dist(f,g)=\inf \{ \epsilon: \forall x \exists y ( f(x)=f(y) ) \wedge  \forall y \exists x ( f(x)=g(y) ) \}$$
 reminiscent of Skorokhod metric in probability theory. 
Now instead of $\Delta_n$ take an arbitrary simplicial set, and rewrite the definition of Skorokhod convergence in terms of the notion of smallness in $sF$.


### Geometric realization preserves fibrations

\begin{theorem}
The geometric realization of a [[Kan fibration]] is a [[Serre fibration]].
\end{theorem}
\begin{proof}
This is shown in [Quillen 68](#Quillen68).
\end{proof}

This result implies that the geometric realization functor preserves all five classes
of maps in a [[model category]]: [[weak equivalences]], [[cofibrations]], [[acyclic cofibrations]],
[[fibrations]], and [[acyclic fibrations]].

In fact the geometric realization of a Kan fibration is even a [[Hurewicz fibration]] (at least relative to a [[convenient category of spaces]] in which it lives).  This follows from the fact that [[a Serre fibration between CW-complexes is a Hurewicz fibration]]; a direct proof along the lines of Quillen's can be found in [Fritch and Piccinini, Theorem 4.5.25](#FP90).

### Induced properties of the fibrant replacement

The previous two sections show that the geometric realization preserves finite limits and fibrations.  Since its right adjoint, the singular complex functor $Top \to sSet$, also preserves both (much more trivially), and since all objects of $Top$ are fibrant and the adjunction is simplicially enriched, it follows that the composite $sSet \to Top \to sSet$ is a simplicially enriched [[fibrant replacement functor]] on $sSet$ that additionally preserves both finite limits and fibrations.


## Examples 

* For $G$ a [[group]], $\mathbf{B}G$, its one-object [[groupoid]] obtained by [[delooping]], $N(\mathbf{B}G)$ the corresponding simplicial [[nerve]] [[Kan complex]], we have that the geometric realization
  $$
    \mathcal{B}G = |N\mathbf{B}G|
  $$
  is the [[topological space]] that is the [[classifying space]] for $G$-[[principal bundle]]s ([[covering space]]s), as long as we give $G$ the [[discrete topology]].

## Related concepts

* **geometric realization**

  * of [[geometric realization of categories|categories]], [[geometric realization of simplicial topological spaces|simplicial topological spaces]], [[geometric realization of cohesive ∞-groupoids|cohesive ∞-groupoids]], [[geometric realisation of cubical sets|cubical sets]].

* [[totalization]]

* [[singular complex functor]]

## References

### General

* {#Quillen68} [[Daniel Quillen]], *The geometric realization of a Kan fibration is a Serre fibration.  Proc. Amer. Math. Soc. 19 1968 1499--1500.  [pdf](https://www.ams.org/journals/proc/1968-019-06/S0002-9939-1968-0238322-1/S0002-9939-1968-0238322-1.pdf)

* {#FP90} Fritsch and Piccinini, *Cellular Structures in Topology*, Cambridge University Press, 1990, ISBN 0521327849

### Compatibility with homotopy limits

Discussion of sufficient conditions for homotopy geometric realization to be compatible with [[homotopy pullback]] (see also at _[[geometric realization of simplicial topological spaces]]_):

* D. Anderson, _Fibrations and geometric realization_ , 
Bull. Amer. Math. Soc. Volume 84, Number 5 (1978), 765-788. ([euclid:1183541139](http://projecteuclid.org/euclid.bams/1183541139))

* {#Rezk14} [[Charles Rezk]], _When are homotopy colimits compatible with homotopy base change?_, 2014 ([pdf](https://faculty.math.illinois.edu/~rezk/i-hate-the-pi-star-kan-condition.pdf), [[RezkHomotopyColimitsBaseChange.pdf:file]])

* Edoardo Lanari, _Compatibility of homotopy colimits and homotopy pullbacks of simplicial presheaves_ ([pdf](http://algant.eu/documents/theses/lanari.pdf), [[LanariHomotopyColimitsBaseChange.pdf:file]])

  (expanded version of [Rezk 14](#Rezk14))

[[!redirects geometric realisation]]

[[!redirects geometric realizations]]

[[!redirects the geometric realization of a Kan fibration is a Serre fibration]]
[[!redirects the geometric realization of a Kan fibration is a Hurewicz fibration]]

