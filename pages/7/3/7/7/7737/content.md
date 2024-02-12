
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Geometry
+-- {: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The term *stratified space* usually refers to a [[topological space]] equipped with the structure of a [[stratification]], which decomposes the space into [[topological subspaces]] called *strata*. 

Often strata are required to be "nice" in some sense (for instance, one may require strata to be [[manifolds]], while the stratified space itself need not be a manifold), and the way that strata are linked together is typically controlled by additional conditions. More generally, the term "stratified space" may refer to any notion of [[spaces]] equipped with some type of stratification structure.

Examples are ubiquitous, canonical stratifications are carried by [[polyhedra]], [[cell complexes]], [[algebraic varieties]], [[orbit spaces]] of many [[group actions]] on [[manifolds]], [[mapping cylinders]] of maps between manifolds, and [[moduli stacks of formal groups]] (stratified by [[height of a formal group|height of formal groups]]).

## Variants

There are many different definitions of stratifications on spaces:

* stratifications from [[filtered topological space|filtrations]],

* [[poset-stratified space|poset-stratifications]],

* [[Whitney stratifications]] (cf. the [Wikipedia](https://en.wikipedia.org/wiki/Whitney_conditions)),

* [[Thom-Mather stratifications]] (see e.g. [Wiki entry](https://en.wikipedia.org/wiki/Thom%E2%80%93Mather_stratified_space)),

* [[stratifold|stratifolds]],

* [[orbifold|orbifolds]],

* homotopical stratifications (as developed by [Quinn](#Quinn)),

* conically smooth stratifications (as developed by [Ayala-Francis-Tanaka](#AFT)),

* etc. ...

## Basic features

### Stratification structures
 {#StratificationStructures}

Most of the above variants share the same basic structure, captured by the following definitions.

\begin{terminology}\label{ExitPathPreorder}
**(exit path preorder)** \linebreak
Given a decomposition $f$ of a [[topological space]] $X$ into [[connected space|connected]] [[subspace#topological_subspaces|subspaces]] (denoted, in the following, by lower-case letters such as $s$), the *exit path preorder* $\mathsf{Exit}(f)$ of $f$ is the [[preorder]] of subspaces $s$ in $f$ with a generating arrow $s \to r$ whenever the [[topological closure]] of $r$ intersects $s$ non-trivially.
\end{terminology}

\begin{defn}\label{Stratification}
A **stratification** $f$ on $X$ is a decomposition of $X$ such that $\mathsf{Exit}(f)$ (Trm. \ref{ExitPathPreorder}) is an actual [[poset]].
\end{defn}

The subspaces in a stratification are also called *strata*. The [[opposite category|opposite]] poset $\mathsf{Exit}(f)^{\mathrm{op}}$ is also called the *entrance path poset* and denoted by $\mathsf{Entr}(f)$.

\begin{rmk}\label{CharacteristicMap}
**(characteristic map)** \linebreak
Given a stratification $f$ on $X$, there is a map $X \to \mathrm{Exit}(f)$ mapping points $x \in s$ to $s \in \mathrm{Exit}(f)$, which is sometimes called the **characteristic map** of $f$, and (abusing notation) denoted by $f \colon X \to \mathrm{Exit}(f)$.
\end{rmk}

The characteristic map (Rmk. \ref{CharacteristicMap}) need not be [[continuous map|continuous]] in general (unless the stratification is locally finite, see Rmk \ref{ContinuityOfCharacteristicMap} below); it is, however, continuous on the [[preimage]] of any finite [[full functor|full]] subposet of the exit path poset. It is often convenient to construct stratifications by constructing their characteristic map.

\begin{example}\label{CWStratification}
**(Stratification of CW complexes)**\linebreak
The following are stratifications of the 1- and 2-spheres:
[[SphereStratification.jpg:pic]]

In general, a stratification of a CW complex $X$ is obtained by taking the strata to be the $n$-cells of $X$ (for each $n$), but with the $(n-1)$-skeleton $X_{n-1}$ removed.
\end{example}

\begin{example}\label{PosetStratification}
**(Poset stratifications)** \linebreak
Let $X$ be a [[topological space]], $P$ a [[poset]], and $f \colon X \to P$ a [[continuous map]] (in other words, $f$ is a $P$-[[poset-stratified space|stratification of $X$]]). This determines a stratification $\mathrm{c}(f)$ of $X$ (in the sense of Def. \ref{Stratification} above) whose strata are the [[connected components]] of the [[preimages]] $f^{-1}(x)$, $x \in P$. The map $f$ factors uniquely through the characteristic map $\mathrm{c}(f) \colon X \to \mathsf{Exit}(\mathrm{c}(f))$ by a [[conservative functor|conservative]] poset map $\mathsf{Exit}(\mathrm{c}(f)) \to P$. (Such (characteristic,conservative)-factorizations are essentially unique.)
\end{example}

 The example shows that any poset-stratification determines a unique stratification. However, many poset-stratifications may determine the same stratification in this way.

\begin{example}\label{FilteredSpaces}
**(Filtered spaces)** Any [[filtered topological space]] $X_0 \subset X_1 \subset ... \subset X_n$ in which each $X_i$ is a [[closed subspace]] of $X_{i+1}$ defines a [[continuous map]] $X \to [n] = (0 \to 1 \to ... \to n)$ mapping points in $X_{i+1} \setminus X_{i}$ to $i$, and thus a stratification by Exp. \ref{PosetStratification}. As a concrete instance of this example, the filtration by skeleta of any [[cell complex]] defines the "stratification by cells" in this way.
\end{example}

\begin{example}\label{TrivialStratification}
**(Trivial stratification)** \linebreak
Every [[topological space]] $U$ is trivially stratified (in the sense of Def. \ref{Stratification}) with strata being the [[connected components]] of $U$.
\end{example}

\begin{rmk}\label{ContinuityOfCharacteristicMap}
**(Continuity of characteristic map)** \linebreak
Let $(X,f)$ be a stratified space according to Def. \ref{Stratification}. One says that the stratification $f$ is "locally finite" if each stratum $s$ of $f$ has an [[open neighborhood]] in $X$ which only contains finitely many strata. (If $(X,f)$ satisfies the frontier condition (Rmk. \ref{FrontierCondition} below) then, equivalently, $(X,f)$ is locally finite iff each point $x \in X$ has an [[open neighborhood]] intersecting only finitely many strata.) If $f$ is locally finite, then the characteristic map $f \colon X \to \mathsf{Exit}(f)$ (Def. \ref{CharacteristicMap}) is a [[continuous map]].
\end{rmk}

\begin{rmk}\label{FrontierCondition}
**(Openness of characteristic map)** \linebreak
Let $(X,f)$ be a stratified space (Def. \ref{Stratification}). One says the stratification $f$ satisfies the "frontier condition" (or, as an adjective, that it is "frontier-constructible") if, for any two strata $s, r$, the [[topological closure]] $\overline r$ [[intersection|intersects]] $s$ non-trivially, then $s \subset \overline r$. The stratification $f$ is frontier-constructible iff the characteristic map $f \colon X \to \mathsf{Exit}(f)$ (Def. \ref{CharacteristicMap}) is an [[open map]].
\end{rmk}

It is generally very reasonable to assume stratifications to be locally finite and frontier-constructible.


### The category of stratifications

\begin{defn}\label{StratifiedMap}
A **stratified map** $F \colon (X,f) \to (Y,g)$ of stratified spaces (Def. \ref{Stratification}) is a [[continuous map]] $F \colon X \to Y$ which factors through the characteristic maps $f$ and $g$ (Def. \ref{CharacteristicMap}) by a (then necessarily unique) map, denoted by $\mathsf{Exit}(F) \colon \mathsf{Exit}(f) \to \mathsf{Exit}(g)$.
\end{defn}

Stratified spaces and their maps (Def. \ref{StratifiedMap}) form a [[category]] $\mathbf{Strat}$ of stratification. The construction of exit path posets (Trm. \ref{ExitPathPreorder}) yields a [[functor]] $\mathsf{Exit} : \mathbf{Strat} \to \mathbf{Pos}$ ([[formal duality|dually]], using $(-)^{\mathrm{op}} : \mathbf{Pos} \to \mathbf{Pos}$ one obtains the entrance path poset functor $\mathsf{Entr} \colon \mathbf{Strat} \to \mathbf{Pos}$). The functor has a right inverse, as follows.

\begin{defn}\label{ClassifyingStratification}
Every poset $P$ has a **classifying stratification** $\parallel P \parallel$ (also called the *stratified realization* of $P$), whose [[underlying]] [[topological space]] is the [[classifying space]] $\left|   P \right|$ of $P$ (i.e. the [[topological realization]] of the [[simplicial nerve]] of $P$), and whose characteristic map (Def. \ref{CharacteristicMap}) is the map $\left| P \right| \to P$ that maps $\left| P^{\leq x} \right| \setminus \left| P^{\lt x} \right|$ to $x$ (here, the full subposets $P^{\leq x} = \{y \leq x\}$ and $P^{\lt x} = \{y \lt x\}$ of $P$ are the "lower" resp. "strict lower closures" of an element $x$ in $P$). Moreover, given a poset map $F \colon P \to Q$, the realization of its nerve yields a stratified map ${\parallel F \parallel} \colon {\parallel P \parallel} \to {\parallel Q \parallel}$. We obtain a [[functor]] ${\parallel - \parallel} \colon \mathbf{Pos} \to \mathbf{Strat}$.
\end{defn}

Every classifying stratification is frontier-constructible (Rmk. \ref{FrontierCondition}).

It makes sense to further terminologically distinguish maps of stratifications as follows.

{#stratified_map_types}
\begin{terminology} 
**(Types of stratified maps)** \linebreak
A stratified map $F \colon (X,f) \to (Y,g)$  (Def. \ref{StratifiedMap}) is called:

* a **substratification** if $F \colon X \to Y$ is a [[topological subspace]] and $\mathsf{Exit}(F)$ is [[conservative functor|conservative]]; if, moreover, $X = g^{-1} \circ \mathsf{Exit}(F) \circ f (X)$ then one says the substratification is **constructible**;

* a **coarsening** if $F \colon X \to Y$ is a [[homeomorphism]] (to emphasize the opposite process, one also calls $F$ a **refinement**);

* a **stratified homeomorphism** (or **stratified iso**) if $F \colon X \to Y$ is a [[homeomorphism]] of [[topological spaces]] and $\mathsf{Exit}(F)$ is an [[isomorphism]] of [[posets]].

* {#stratified_bundle} a **stratified bundle** if points $x \in s$ for $s$ a stratum of $(Y,g)$ admit [[open neighbourhoods]] $U_x \subset s$ such that, up to stratified iso, $F$ restricts on $F^{-1}(U_x)$ to a projection $U_x \times f_x \to U_x$ (see Def. \ref{defn_strat_product}) for some 'fiber' stratification $(F^{-1}(x),f_x)$.

\end{terminology}

{#constructible_strat_bun}
\begin{rmk} (Constructible bundles). The preceding definition of stratified bundles is rather weak, and in practice one often finds bundles that satisfy stronger conditions, such as constructibility: a *constructible* stratified bundle is a bundle that, up to bundle isomorphism, can be classified by functorial information associated to the fundamental category (see Def. \ref{defn_exit_path_cat}) of its stratified base space (cf. [Sec. 6.3, Ayala-Francis-Rozenblyum 2015](#AyalaFrancisRozenblyum15)).
\end{rmk}


## Fundamental categories

Just as spaces have [[fundamental infinity-groupoid|fundamental]] $\infty$-[[fundamental infinity-groupoid|groupoids]], stratified spaces also have "[[fundamental category|fundamental categories]]". However, the role of *sets* for spaces is now played by *posets*: the following table illustrates the analogy. (The table is further explained below.)

| base concept | $\infty$-concept | presentation |
| ----- | ----- | ----- |
| [[set|sets]] $\simeq$ $(0,0)$-[[0-category|categories]] | ∞-sets $\simeq$ [[topological space|spaces]] | sets with w.e. |
| [[poset|posets]] $\simeq$ $(0,1)$-[[(0,1)-category|categories]] | ∞-posets $\simeq$ **stratified spaces** | posets with w.e. |
| [[category|categories]] $=$ $(1,1)$-categories | [[(∞,1)-category|∞-categories]] | [[categories with weak equivalences|categories with w.e.]] |

In the table, an "$\infty$-X" is intuitively to be understood as an [[(∞,∞)-category]] which admits a [[conservative functor]] to an X, where X can e.g. stand for "set", "poset", or "category". Yet more generally, X can be an [[(n,r)-category]] for $n,r \lt \infty$. A "set with weak equivalences" means a poset with weak equivalences in which each arrow is a weak equivalence. The left column is related to the middle column by an "$\infty$-zation functor" (which simply includes $1$-structures into $\infty$-structures), and the middle and right columns are related by an "[[category with weak equivalences#InfCatPres|∞-localization functor]]" (which should be a weak equivalence in some sense).

In order to make the above precise, one must work with sufficiently convenient stratifications. We describe two simple ways of constructing/presenting **fundamental $\infty$-posets** below.

### For conical stratificiations {#conical_strat}

\begin{defn} \label{defn_strat_product} Given stratifications $(X,f)$ and $(Y,g)$ their **product** is the stratification of $X \times Y$ with characteristic map $f \times g$.
\end{defn}

\begin{defn} Given a stratification $(X,f)$, the **stratified (open) cone** $(\mathrm{cone}(X), \mathrm{cone}(f))$ stratifies the topological open cone $\mathrm{cone}(X) = X \times [0,1) / X \times \{0\}$ by the product $(X,f) \times (0,1)$ away from the cone point $\{0\}$ (here, the open interval $(0,1)$ is trivially stratified), and by setting the cone point $\{0\}$ to be its own stratum.
\end{defn}

\begin{defn} A **conical** stratification $(X,f)$ is a stratification in which each point $x \in X$ has a neighborhood (i.e. an open substratification) that is a stratified product $U \times (\mathrm{cone}(Z),\mathrm{cone}(l))$ for some "link" stratification $(Z,l)$ and such that $x \in U \times \{0\}$.
\end{defn}

Every conical stratification is frontier-constructible.

\begin{defn} \label{defn_exit_path_cat} Given a conical stratification $(X,f)$, then [Lurie](#LurieHA) constructs **exit path $\infty$-category** $\mathcal{E}\mathrm{xit}(f)$ as a quasicategory: the $k$-simplices of the quasicategory $\mathcal{E}\mathrm{xit}(f)$ are precisely stratified maps $\parallel [k]\parallel \to (X,f)$, where $[k] = (0 \to 1 \to ... \to k)$.
\end{defn}

\begin{rmk} One dually defines the **entrance path $\infty$-category** $\mathcal{E}\mathrm{ntr}(f)$ with $k$-simplices $\parallel [k]^{\mathrm{op}} \parallel \to (X,f)$.
\end{rmk}

{#exit_entrance_conv}
\begin{terminology} An **exit path** in a stratified space $(X,f)$ is a stratified map $f : \parallel [1] \parallel \to (X,f)$; we say $f$ *starts* $f(0)$ and *ends* at $f(1)$ (dually, we say $f$ is an **entrance path** which starts at $f(1)$ and ends at $f(0)$).
\end{terminology}

The construction translates from "stratified spaces" to 
"$\infty$-posets" in the above table: the conservative functor $\mathcal{E}\mathrm{xit}(f) \to \mathsf{Exit}(f)$ takes objects $\parallel [0]\parallel \to X$ to the stratum $s \in \mathsf{Exit}(f)$ that their image lies in.

### For regular stratifications {#regular_strat}

\begin{defn} A stratification $(X,f)$ is **regular** if it admits a refinement $\parallel P \parallel \to (X,f)$ by the stratified realization of some poset $P$.
\end{defn}

\begin{defn} Given a regular stratification $(X,f)$ and a refinement $F : \parallel P\parallel \to (X,f)$, one can construct the **presented exit path $\infty$-category** $\mathcal{PE}\mathrm{xit}(f)$ as a poset with weak equivalences with underlying poset $P$ and weak equivalences $\mathsf{Exit}(F)^{-1}(\mathrm{id})$.
\end{defn}

(Showing that this construction is, in an appropriate sense, independent of the choice of $P$ requires a bit more work...)

\begin{rmk} \label{rmk_cellulable} A special case of the definition asks for refinements by regular cell complexes (or simplicial complexes) in place of classifying stratifications of posets, in which case one speaks of **cellulable** (resp. **triangulable**) stratifications.
\end{rmk}

The construction translates between "stratified spaces" and "posets with weak equivalences" in the above table. Since spaces are trivially stratified spaces, this specializes to a translation between "spaces" and "sets with weak equivalences".

## Related concepts

* [[stratification]]

* [[piecewise flat spacetime]]

## References

A notion of purely topologically stratified sets was introduced in

* [[Frank Quinn]], _Homotopically stratified sets_, J. Amer. Math. Soc. 1 (1988), 441--499. MR 89g:57050
 {#Quinn}

Notions of smoothly stratified spaces were considered by

* H. Whitney, _Local properties of analytic varieties_, Differentiable and combinatorial topology (S. Cairns, ed.), Princeton Univ. Press, Princeton, 1965, pp. 205--244. MR 32:5924

* R. Thom, _Ensembles et morphismes stratifi&#233;s_, Bull. Amer. Math. Soc. 75 (1969), 240--282.
MR 39:970

* J. Mather, _Notes on topological stability_, Harvard Univ., Cambridge, (1970)

Locally conelike stratified spaces have been considered  in

* L. Siebenmann, _Deformations of homeomorphisms on stratified sets_, Comment. Math. Helv. 47 (1971), 123--165. MR 47:7752

These are all special cases of ([Quinn's definition](#Quinn)).

Discussion of [[differential operators]] on stratified spaces is in 

* R. B. Melrose,  _Pseudodifferential operators, corners and singular limits_, Proceedings of the International Congress of Mathematicians, Vol. I, II (Kyoto, 1990), 217--234, Math. Soc.

* Pierre Albin, Eric Leichtnam, Rafe Mazzeo, Paolo Piazza, _The signature package on Witt spaces, I. Index classes_ ([arXiv:0906.1568v2](http://uk.arxiv.org/abs/0906.1568v2))

See also

* Bruce Hughes, _Geometric topology of stratified spaces_ ([pdf](http://aimsciences.org/journals/pdfsnews.jsp?paperID=2468&mode=full))

Discussion of the [[fundamental category]] of a (Whitney&#8209;)stratified space is in 

* [[Jonathan Woolf]], _Transversal homotopy theory_ &lbrack;[arXiv:0910.3322](http://arxiv.org/abs/0910.3322)&rbrack;

* [[Markus Banagl]], *Topological invariants of stratified spaces*, Springer Monographs in Mathematics, Springer (2000) &lbrack;[doi:10.1007/3-540-38587-8](https://doi.org/10.1007/3-540-38587-8)&rbrack;


A [[homotopy hypothesis]] for stratified spaces is discussed in

* {#AyalaFrancisRozenblyum15} [[David Ayala]], [[John Francis]], [[Nick Rozenblyum]], *A stratified homotopy hypothesis*, [arXiv](http://arxiv.org/abs/1502.01713)

* [[Peter J. Haine]], _On the homotopy theory of stratified spaces_ ([arXiv:1811.01119](https://arxiv.org/abs/1811.01119))

The former is based on the notion of stratifications developed in

* {#AFT} David Ayala, John Francis, and Hiro Lee Tanaka. _Local structures on stratified spaces_. Advances in Mathematics 307 (2017): 903-1028.

An earlier paper on exit paths is

* [[David Treumann]], *[Exit paths and constructible stacks](https://www2.bc.edu/david-treumann/epacs.pdf)*, Compositio Math. 145 (2009), 1504&#8211;1532 

Poset-stratified spaces and the conicality condition, as well as the construction of the fundamental $\infty$-poset of a conical stratification as a quasicategory, first appeared in:

* {#LurieHA} [[Jacob Lurie]], *[[Higher Algebra]]*, 2012, in particular Appendix A ([pdf](https://www.math.ias.edu/~lurie/papers/HA.pdf))

Stratified spaces are used to develop a graphical calculus for Gray categories in:

* Benjamin Taylor Hummon, *[Surface Diagrams for Gray-Categories](https://escholarship.org/uc/item/5b24s9cc)*, PhD thesis.


[[!redirects stratified space]]
[[!redirects stratified spaces]]

[[!redirects stratum]]
[[!redirects strata]]
