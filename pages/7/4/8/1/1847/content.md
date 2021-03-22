
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents#
{: toc}

## Definition 

Recall:

+-- {: .num_defn #LocallyFiniteCover}
###### Definition
**([[locally finite cover]])**

Let $(X,\tau)$ be a [[topological space]].

An [[open cover]] $\{U_i \subset X\}_{i \in I}$ of $X$ is called  _locally finite_ if for each point $x \in X$, there exists a  [[neighbourhood]] $U_x \supset \{x\}$ such that it [[intersection|intersects]] only finitely many elements of the cover, hence such that  $U_x \cap U_i \neq \emptyset$ for only a [[finite number]] of $i \in I$.

=--

+-- {: .num_defn #RefinementOfOpenCovers}
###### Definition
**([[refinement]] of [[open covers]])


Let $(X,\tau)$ be a [[topological space]], and let $\{U_i \subset X\}_{i \in I}$ be a [[open cover]].
 
Then a _[[refinement]]_ of this open cover is a set of open subsets $\{V_j \subset X\}_{j \in J}$ which is still an [[open cover]] in itself and such that for each $j \in J$ there exists an $i \in I$ with $V_j \subset U_i$.

=--

Now:

+-- {: .num_defn #ParacompactSpace}
###### Definition
**(paracompact topological space)**

A [[topological space]] $(X,\tau)$ is called **paracompact** if every [[open cover]] of $X$ has a [[refinement]] (def. \ref{RefinementOfOpenCovers}) by a [[locally finite open cover]] (def. \ref{LocallyFiniteCover}).

=--


+-- {: .num_remark #DifferingTerminology}
###### Remark
**(differing terminology)**

As with the concept of [[compact topological spaces]] ([this remark](compact#space#DifferingTerminology)), some authors demand a paracompact space to also be a [[Hausdorff topological space]]. See at *[[paracompact Hausdorff space]]*.


=--


## Examples 

+-- {: .num_example}
###### Example

Every [[compact space]] is paracompact.

=--

+-- {: .num_example }
###### Example

Every [[locally connected topological space|locally connected]] [[locally compact topological group|locally compact]] [[topological group]] is paracompact ([this prop.](topological+group#ConnectedLocallyCompactTopologicalGroupsAreSigmaCompact)).

=--

+-- {: .num_prop }
###### Proposition

[[locally compact space|locally compact]] and [[second-countable space|second-countable]] [[Hausdorff space]] are paracompact.

=--

+-- {: .num_prop #ParacompactFromLocallyCompactAndSigmacompact}
###### Proposition

[[locally compact and sigma-compact spaces are paracompact]]

=--

+-- {: .num_example #ParacompactEuclideanSpace}
###### Example
**([[Euclidean space]] is paracompact)**

For $n \in \mathbb{N}$, then the [[Euclidean space]] $\mathbb{R}^n$,
regarded with its [[metric topology]]
is paracompact.

=--

+-- {: .proof}
###### Proof

Euclidean space is evidently [[locally compact topological space|locally compact]] and [[sigma-compact topological space|sigma-compact]].
Therefore the statement follows since [[locally compact and sigma-compact spaces are paracompact]] (prop. \ref{ParacompactFromLocallyCompactAndSigmacompact}).

=--




+-- {: .num_prop #ParacompactnessPreservedByDisjointUnion}
###### Proposition

Paracompactness is preserved by forming [[disjoint union spaces]] ([[coproducts]] in [[Top]]).

=--

+--{: .proof}
###### Proof

Consider a disjoint union $X = \coprod X_\lambda$ whose components are paracompact.  As the union is disjoint, the components, that is to say, the $X_\lambda$, are open in $X$.  Thus any open cover, say $\mathcal{U}$, of $X$ has a refinement by open sets, say $\mathcal{V}$, such that each $V \in \mathcal{V}$ is contained in some $X_\lambda$.  Thus we can write $\mathcal{V} = \coprod \mathcal{V}_\lambda$.  As each $X_\lambda$ is paracompact, each $\mathcal{V}_\lambda$ has a locally finite refinement, say $\mathcal{W}_\lambda$.  Then let $\mathcal{W} := \coprod \mathcal{W}_\lambda$.  As each $\mathcal{W}_\lambda$ is a refinement of the corresponding $\mathcal{V}_\lambda$, $\mathcal{W}$ is a refinement of $\mathcal{V}$, and hence of $\mathcal{U}$.  As each point of $X$ has a neighbourhood which meets only elements of _one_ of the $\mathcal{W}_\lambda$, and as that $\mathcal{W}_\lambda$ is locally finite, $\mathcal{W}$ is locally finite.  Thus $\mathcal{U}$ has a locally finite refinement.

=--


* [[manifolds]]

  *  finite-dimensional manifolds are locally compact, so we have the results above, but we also have some converses:

     * a finite-dimensional Hausdorff topological [[manifold]] is paracompact precisely if it is [[metric space|metrizable]]

     * a finite-dimensional Hausdorff topological manifold is paracompact precisely if each component is second-countable

   * [[infinite-dimensional manifolds]] are generally not locally compact, but we still have some results:

     * The [[Frechet manifold|Frechet]] [[smooth loop space]] of a compact finite dimensional manifold is paracompact.


     * More generally, if $E$ is the sequential [[limit]] of separable Hilbert spaces $H_n$, such that the canonical projections
       $$
         p_n : E \to H_n
       $$
       satisfy
       $$
         closure(p_n^{-1}(B)) = p_n^{-1}(closure(B))
       $$

       for any open ball $B$ in $H_n$, then $E$ is paracompact, and furthermore admits _smooth_ partitions of unity. 

       ( [Brylinski, section I.4](#Brylinski))

* [[CW-complexes are paracompact Hausdorff spaces]] ([Miyazaki 52](#Miyazaki52)), see for instance [Hatcher, appendix of section 1.2](#Hatcher). For a discussion that highlights which [[axiom of choice|choice principles]] are involved, see ([Fritsch-Piccinini 90, Theorem 1.3.5 (p. 29 and following)](#FP)).

* metric spaces

  * every [[separable space|separable]] [[metric space]] is paracompact;

  * every [[metric space]] whatsoever is paracompact, assuming the [[axiom of choice]]; see at _[[metric spaces are paracompact]]_

  * pseudometric spaces are paracompact under the same conditions, if one does not require Hausdorffness;

* In particular we have the following implications

  * [[second-countable space]] and regular Hausdorff space
    $\Rightarrow$ [[metric space|metrizable space]]
    $\Rightarrow$ paracompact space

    (the first is Urysohn's metrization theorem, the second is due to [Stone 48](#Stone48), see also at _[[second-countable regular spaces are paracompact]]_ and _[[metric spaces are paracompact]]_)

  * paracompact space and locally metric space
    $\Rightarrow$
    [[metric space|metrizable space]]

    (this is due to Smirnov)


* special cases

  * the [[Sorgenfrey line]] is a good example of a paracompact space that doesn\'t fit into other general classes of paracompact spaces (in particular, it is not [[metrisable topological space|metrisable]], locally compact, or a manifold);

* counterexamples

  * the [[long line]] is *not* paracompact, even though it is a [[manifold]] (unless one specifically requires paracompactness of manifolds) but it fails to be [[second-countable space|second-countable]] (even though it is connected) or metrisable. 

  * the [[Sorgenfrey plane]] (a product of two [[Sorgenfrey lines]]) is not paracompact. This shows that the product of paracompact spaces need not be paracompact. 


## Properties 

### General
 {#PropertiesGeneral}

* a [[closed subspace]] of a paracompact topological space is itself paracompact (e.g. [here](https://www.uio.no/studier/emner/matnat/math/MAT4520/v17/beskjeder/para.pdf#page=1));

* __Dieudonne's theorem__: [[paracompact Hausdorff spaces are normal]] 

* every paracompact [[finite number|finite]]-[[dimension of a manifold|dimensional]] [[topological manifold]] has a [[partition of unity]]

* [[paracompact Hausdorff spaces equivalently admit subordinate partitions of unity]]

  Care should be taken as to in which [[category]] one considers [[partitions of unity]] on paracompact spaces: For example, analytic [[partitions of unity]] generally do not exist on ([[finite number|finite]] -[[dimension of a manifold|dimensional]]) [[smooth manifolds]], even when smooth ones do.

* For paracompact Hausdorff spaces, all [[open covers]] are [[numerable open cover|numerable open covers]].

* [[Michael's theorems]] 

+-- {: .num_example #CountableCoverOfUnionsofOpenSubsetsInsideGivenCover}
###### Lemma

Let $X$ be a [[paracompact Hausdorff space]], and let $\{U_i \subset X\}_{i \in I}$ be an [[open cover]]. Then there exists a [[countable cover]]

$$
  \{V_n \subset X\}_{n \in \mathbb{N}}
$$

such that each element $V_n$ is a [[union]] of [[open subsets]] of $X$ each of which is contained in at least one of the elements $U_i$ of the original cover.

=--

(e.g. [Hatcher, lemma 1.21](#Hatcher))

+-- {: .proof}
###### Proof

Let $\{f_i \colon  X \to [0,1]\}_{i \in I}$ be a [[partition of unity]] subordinate to the original cover, which exists since [[paracompact Hausdorff spaces equivalently admit subordinate partitions of unity]].

For $J \subset I$ a [[finite set]], let 

$$
  V_J
    \;\coloneqq\;
  \left\{
    x \in X 
    \;\vert\;
    \underset{j \in J}{\forall}
    \left(
       \underset{k \in I \setminus J}{\forall}
       \left(
         f_j(x) \gt f_k(x)
       \right)
    \right)
  \right\}
  \,.
$$

By local finiteness there are only a [[finite number]] of $f_k(x)$ greater than zero, hence the condition on the right is a finite number of strict inequalities. Since the $f_i$ are continuous, this implies that $V_J$ is an [[open subset]].

Moreover, $V_J$ is contained in $supp(f_j)$ for $j \in J$ and hence in one of the $U_i$.

Now for $n \in \mathbb{N}$ take

$$
  V_n 
    \;\coloneqq\;
  \underset{ {J \subset I} \atop { {\vert J\vert} = n } }{\cup}
  V_J
$$

to be the union of the $V_J$ over all subset $J$ with precisely $n$ elements.

The set $\{V_n \subset X\}_{n \in \mathbb{N}}$ is a cover because for any $x \in X$ we have $x \in V_{J_x}$ for

$$
 J_x \coloneqq \{ i \in I \;\vert\; f_i(x) \gt 0  \}
$$

(which is finite by local finitness of the partition of unity).


=--


### Colimits

See at _[[colimits of paracompact Hausdorff spaces]]_.

### Homotopy and Cohomology 
 {#HomotopyAndCohomology}

* On paracompact spaces, abelian [[Čech cohomology]] does compute [[abelian sheaf cohomology]], 

  i.e. the canonical morphism $\check{H}(X,A) \to H(X,A)$ for  $A$ any [[chain complex]] of [[sheaf|sheaves]] is an [[isomorphism]] when the [[topological space]] underlying $X$ is paracompact.

+-- {: .num_prop }
###### Proposition

On a paracompact space $X$, every [[hypercover]] of finite height is refined by the [[Čech nerve]] of an ordinary [[open cover]].

=--

For a hypercover of height $n \in \mathbb{N}$, this follows by intersecting the open covers that are produced by the following lemma for $0 \leq k \leq n$.

+-- {: .num_lemma }
###### Lemma

For $X$ a paracompact topological space, let $\{U_\alpha\}_{\alpha \in A}$ be an [[open cover]], and let each $(k+1)$-fold intersection $U_{\alpha_0, \cdots, \alpha_{k}}$ be equipped itself with an open cover $\{V^{\alpha_0, \cdots, \alpha_k}_{\beta}\}$.

Then there exists a refinement $\{U'_{\alpha'}\}$ of the original cover, such that each $(k+1)$-fold intersection $U'_{\alpha'_0, \cdots, \alpha'_k}$ for all indices distinct is contained in one of the $V_\beta$.

=--

This appears as ([[Higher Topos Theory|HTT, lemma 7.2.3.5]]).


## Related concepts

* [[countably paracompact topological space]]

* [[compact topological space]], [[countably compact topological space]], [[locally compact topological space]], [[strongly compact topological space]], [[sequentially compact topological space]]


## References 

The notion of paracompact space was introduced in

* [[Jean Dieudonné]], _Une g&#233;n&#233;ralisation des espaces compacts_, Journal de Math&#233;matiques Pures et Appliqu&#233;es, Neuvi&#232;me S&#233;rie, 23: 65&#8211;76 (1944)

That [[fully normal spaces are equivalently paracompact]] is due to

* {#Stone48} A. H. Stone, _Paracompactness and product spaces_, Bull. Amer. Math. Soc. Volume 54, Number 10 (1948), 977-982. ([Euclid](http://projecteuclid.org/euclid.bams/1183512390))


General accounts include

* R. Engelking, _General topology_, chapter 5 is dedicated to paracompact spaces

* [[Brian Conrad]], _Paracompactness and local compactness_, [pdf](http://math.stanford.edu/~conrad/diffgeomPage/handouts/paracompact.pdf)

* D. K. Burke, _Covering properties_, in: [[K. Kunen]], J.E. Vaughan (eds.), Handbook of Set-Theoretic Topology, North-Holland (1984) Ch. 9, 347&#8211;422

* {#Hatcher} [[Alan Hatcher]], section 1.2 of _Vector bundles & K-theory_ ([web](https://www.math.cornell.edu/~hatcher/VBKT/VBpage.html))


*  English Wikipedia: [paracompact space](http://en.wikipedia.org/wiki/Paracompact_space)

* Springer eom: [paracompact space](http://eom.springer.de/p/p071300.htm), [paracompactness criteria](http://eom.springer.de/p/p071310.htm)

* Some properties of paracompact spaces are listed and proven in [http://www.helsinki.fi/~hjkjunni/top9.pdf](http://www.helsinki.fi/~hjkjunni/top9.pdf)


A basic discussion with an eye towards [[abelian sheaf cohomology]] and abelian [[Čech cohomology]] is around page 32 of

* [[Jean-Luc Brylinski]], _Loop spaces, characteristic classes geoemetric quantization_
{#Brylinski} 

* {#FP} [[Rudolf Fritsch]], Renzo A. Piccinini, _Cellular structures in topology_, Cambridge studies in advanced mathematics Vol. 19, Cambridge University Press (1990). ([pdf](https://epub.ub.uni-muenchen.de/4493/1/4493.pdf)) 
  

Discussion of paracompactness of [[CW-complexes]] includes

* {#Miyazaki52} Hiroshi Miyazaki, _The paracompactness of CW-complexes_, Tohoku Math. J. (2) Volume 4, Number 3 (1952), 309-313. 1952 [Euclid](https://projecteuclid.org/euclid.tmj/1178245380)

[[!redirects paracompact]]
[[!redirects paracompactness]]
[[!redirects Paracompact space]]
[[!redirects Paracompact spaces]]
[[!redirects paracompact space]]
[[!redirects paracompact spaces]]
[[!redirects paracompact topological space]]
[[!redirects paracompact topological spaces]]
[[!redirects paracompactum]]
[[!redirects paracompactums]]
[[!redirects paracompacta]]

[[!redirects Dieudonne's theorem]]
[[!redirects Dieudonne\'s theorem]]
[[!redirects Dieudonne's theorem]]
[[!redirects Dieudonne theorem]]
[[!redirects Dieudonné's theorem]]
[[!redirects Dieudonné\'s theorem]]
[[!redirects Dieudonné's theorem]]
[[!redirects Dieudonné theorem]]
