
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

# Semi-simplicial sets
* table of contents
{:toc}

## Idea

A *semi-simplicial set* is like a [[simplicial set]], but without the degeneracy maps: it is a sequence $\{X_n\}_{n \in \mathbb{N}}$ of [[sets]] together with [[functions]] called _face maps_ between them which encode that an element in $X_{n+1}$ has $(n+1)$ "faces" (boundary segments) which are elements in $X_{n}$.

The semi-simplicial set version of a [[simplicial complex]] is also called a _[[Delta set]]_.

## Definition

Let $\Delta$ denote the [[simplex category]], which is a [[skeleton]] of the [[category]] of [[inhabited set|inhabited]] [[finite set|finite]] [[totally ordered sets]].   Let $\Delta_+$ denote the [[wide subcategory]] of $\Delta$ containing only the [[injective functions]] (it is sometimes written $\Delta_{inj}$, $\Delta_i$, $\widehat{\Delta}$, $\Delta'$ or $\overline{\Delta}$).   Thus, $\Delta_+$ is equivalent to the category of inhabited finite totally ordered sets and order-preserving injections.  

Recall that a [[simplicial set]] is a [[presheaf]] $X\colon \Delta^{op}\to Set$.  Similarly, a **semi-simplicial set** is a presheaf $X\colon \Delta_+^{op} \to Set$.

More generally, for $\mathcal{C}$ any other category, a functor $\Delta_+^{op} \to \mathcal{C}$ is a _[[semi-simplicial object]]_ in $\mathcal{C}$.

## Properties

### Adjunction with simplicial sets
 {#AdjunctionWithSimplicialSets}

The [[forgetful functor]] from [[SimplicialSets]] to the [[category]] of semi-simplicial sets is given by precomposition with the [[opposite functor]] of the non-[[full subcategory|full]] [[wide subcategory]] inclusion

$$
  \Delta_{inj} \xrightarrow{\;j\;} \Delta
$$

into the [[simplex category]] and hence has both a [[left adjoint]] as well as a [[right adjoint]] given by left/right [[Kan extension]], respectively:

\begin{tikzcd}[column sep=small]
  \mathrm{SemiSimplSets}
  \ar[
    rr,
    shift left=18pt,
    "j_!"{above}
  ]
  \ar[
    rr,
    shift right=18pt,
    "j_\ast"{below}
  ]
  &&
  \mathrm{SimplSets}
  \ar[
    ll,
    "j^\ast"{description}
  ]
  \ar[ll, shift left=10pt, phantom, "\scalebox{.7}{$\bot$}" ]
  \ar[ll, shift right=10pt, phantom, "\scalebox{.7}{$\bot$}" ]
\end{tikzcd}

The [[adjunction unit]] of the left [[adjoint pair]]

$$
  X \xrightarrow{ \;\eta_X\; } j^\ast j_! X
$$

is a [[weak homotopy equivalence]] in the sense that its [[geometric realization]] is so ([Rourke & Sanderson 71, Rem. 5.8](#RourkeSanderson71)).

Notice that 

1. for $X \in $ [[SimplicialSets]], the [[geometric realization]] of the underlying semi-simplicial set $j^\ast X$ is the *[[fat geometric realization]]* of $X$ (see [there](geometric+realization+of+simplicial+topological+spaces#FatGeometricRealization)):

   $$
     \left\Vert X \right\Vert
     \;\coloneqq\;  
     \left\vert j^\ast X \right \vert
   $$

1. There is (by [this Prop.](https://ncatlab.org/nlab/source/geometric+realization+of+simplicial+topological+spaces#FatRealizationOfGoodSimplicialSpaces)) a natural [[weak homotopy equivalence]] from the fat to the ordinay geometric realization of a simplicial set (which is always "[[good simplicial topological space|good]]" when regarded as a simplicial space):

   $$
     \left\vert j^\ast X \right \vert
     \;\simeq_{whe}\;
     \left\vert X \right \vert
     \,.
   $$

It follows (see also [MO:a/75101](https://mathoverflow.net/a/75101/381)) that also the [[adjunction counit]]

$$
  j_! j^\ast X \xrightarrow{\; \epsilon_X \;} X
$$

is a [[simplicial weak equivalence]].

### Relation to semi-categories

The [[nerve]] of a [[semicategory]] is a semi-simplicial set (satisfying the [[Segal conditions]]) just as the nerve of a [[category]] is a [[simplicial set]]. 

### Model category structure

There is a _[[model structure on semi-simplicial sets]]_, [[transferred model structure|transferred]] along the [[right adjoint]] to the [[forgetful functor]] from the [[model structure on simplicial sets]].

### The lattice of subtoposes

Since the maps in $\Delta_+$ are all strictly monotone, any object $[n]$ receives only (finitely many) morphisms from objects $[m]$ with $m\leq n$ whence all [[slice category|slices]] $\Delta_+/[n]$ are [[finite category|finite]]. This is sufficient for all [[Grothendieck topology|Grothendieck topologies]] on $\Delta_+$ to be [[rigid topology|rigid]] whence all subtoposes of $Set^{\Delta_+^{op}}$ are [[level of a topos|essential]] and of [[presheaf topos|presheaf type]] and their [[lattice]] is isomorphic to the lattice of [[Cauchy-complete category|Cauchy-complete]] [[full subcategory|full subcategories]] of $\Delta_+$.

This situation is familiar from $\Delta$ but in the latter case there are fewer Cauchy-complete subcategories available, since an object $[n]$ having non-trivial idempotents its inclusion automatically requires the presence of all $[m]$ with $m\,$<$\,n$ in the subcategory whence there are countably many subtoposes corresponding to the $n$-truncated subcategories on the objects $[0],\dots ,[n]$ (plus the two trivial subcategories).

Recall that an [[essential localization]] of a topos embeds the corresponding [[subtopos]] as a [[reflective subcategory]] (i.e. sheaves for the corresponding topology) as well as a [[coreflective subcategory]]. For a given (essential) topology $j$ we call the presheaves in the image of the latter inclusion _$j$-skeleta_. Recall that the [[Aufhebung]] of such a [[level of a topos|level topology]] $j$ is defined as the largest topology $\hat{j}$ such that all $j$-skeleta are $\hat{j}$-sheaves (if such a $\hat{j}$ exists). This differs somewhat from the definition given at [[Aufhebung]] but will suffice in the present context where all subtoposes are [[level of a topos|levels]].

The [[Lawvere-Tierney topology|Lawvere-Tierney topologies]] $j_w$ on $Set^{\Delta_+^{op}}$ are indexed by infinite words $w$ over the alphabet $\{0,1\}$. They are partially ordered by $j_w\leq j_z$ iff $w_i\leq z_i$ for all letter positions $i=0,1,2,\dots$, where (unsurprisingly) letter 0 counts as smaller than letter 1. We will abbreviate infinite periods $000\dots$ (resp. $111\dots$) by $\bar{0}$ (resp. $\bar{1}$), finite periods of length $m$ by $0^m$ (resp. $1^m$). It is sometimes useful to assume that a finite length of $m=0$ denotes a block of length 0 of that letter (=its absence in that position) e.g. $1^m\bar{0}\;, m=0,1,\dots$ denotes all words that start with a possibly empty finite block of 1s followed by an infinite sequence of 0s (and sometimes by abuse also $\bar{1}$ if $m=\infty$ i.e. $1^\infty$ preempts the occurrence of the second infinite block).

The information contained in the $i$-th letter of $w$ is whether the [[closure operator]] corresponding to $j_w$ adds $i$-dimensional semi-simplices to subobjects ($w_i=1$) or not ($w_i=0$) e.g. $j_{\bar{1}}$ adds all semi-simplices of every dimension implying that the empty subobject is $j_\bar{1}$-dense in every object thereby preventing all non-terminal objects from being $j_\bar{1}$-sheaves i.e. $j_{111\dots}=j_max$ while $j_\bar{0}$ where no semi-simplex of any dimension is added and every presheaf is a $j_\bar{0}$-sheaf corresponds to $j_min$. Another way to view the $i$-th letter in $w$ is as specifying whether $[i]$ is ($w_i=0$) or is not ($w_1=1$) contained in the image of the subcategory inclusion $\Delta_{j_w}\hookrightarrow\Delta_+$ corresponding to $j_w$.


A topology $j_w$ restricts to a topology $j_w|_n$ on the n-truncation $\Delta_+|_n$ by taking the prefix of length $n$+1 e.g. $j_{00},j_{01},j_{10},j_{11}$ are the four topologies on the 1-truncation, the topos of [[quiver|directed graphs]].

The [[initial object]] $0\in Set^{\Delta_+^{op}}$ is a $j_w$-sheaf for the topology $j_w$ precisely when $w_0=0$ since otherwise every $j_w$-sheaf contains exactly one vertex hence these $j_{0w'}$ correspond to the [[dense subtopos|dense subtoposes]] of $Set^{\Delta_+^{op}}$ .

There is a countably infinite number of co-atoms $j_w$ where $w$ contains exactly one 0. These correspond to different copies of $Set$ induced by the inclusion of the one-morphism category on the objects $[n]$ in $\Delta_+$. In particular, the dense [[double negation]] copy $j_{\neg\neg}$ corresponds to $j_{0\bar{1}}$, the $j_{\neg\neg}$-sheaves consisting of semi-simplicial sets with an arbitrary set of $0$-semi-simplexes (= vertices) and exactly one $n$-semi-simplex in the higher dimensions for every configuration of $n$-1-semi-simplices which can bound an $n$-semi-simplex. Since 0 is the only $j_{max}$-skeletal presheaf we see incidentally that $\hat{j}_{max}=j_{\neg\neg}$.

We denote the corresponding [[Boolean topos|quasi-closed]] topologies by $q(k)$ where $k$ indicates the position where the 0 occurs e.g. $q(0)=j_{\neg\neg}\,$. Since the $[k]$ corresponds to the non-trivial [[groupoid|groupoidal]] subcategories of $\Delta_+$ the subtoposes $Sh_{j^0_k}(Set^{\Delta_+^{op}})$ are the only non-trivial [[Boolean topos|Boolean]] subtoposes of $Set^{\Delta_+^{op}}$. The endofunctor of the $j^0_k$-skeletal [[comonad]] on $Set^{\Delta_+^{op}}$ is  given by $X\mapsto \coprod_{X[k]}[k]$ (in particular, the $q(k)$-skeleta are those semi-simplicial sets $X$ with $X\simeq \coprod_{X[k]}[k]$ ). This basically replaces $X$ by its "set" of $k$-semi-simplices in the disconnected form of copies of the standard $k$-semi-simplex and discards everything else.

Since $[k]$ is $q(k)$-skeletal but not $n$-precise (i.e. has precisely one $n$-semi-simplex for any possible scaffold of $n-1$-semi-simplices) for any $0\leq n\leq k+1$, at least if $k\neq 0$, we find that $\hat{q}(k)=o(k+1)$ where $o(m):= j_{0^m\bar{1}}$ are the [[open subtopos|open topologies]] to be described below.

The [[Lawvere-Tierney topology|Lawvere-Tierney topologies]] $j_w$ on [[simplicial set|simplicial sets]] can similarly described by infinite words over $\{0,1\}$ with the same interpretation of the letters but there $w$ has to start with a (possibly empty, possibly infinite) block of zeros expressing that the respective sheaf categories consist of $m$-truncated simplicial sets, where $m+1$ is the length of the block of zeros with which $w$ starts e.g. $j_{00\bar{1}}$ corresponds to the 1-truncation, the topos of [[reflexive graph|reflexive graphs]].

In $Set^{\Delta_+^{op}}$ these topologies $j_w$ with $w=0^m\bar{1},\quad m=0,\dots ,\infty$ correspond precisely to the [[open subtopos|open subtoposes]]. In order to see this, consider the [[terminal object]] 1 of $Set^{\Delta_+^{op}}$: in contrast to [[SSet]] where the degeneracies prevent this, we can truncate 1 at arbitrary dimensions by simply discarding the higher dimensional semi-simplices. Hence there is a countably infinite number of non-trivial [[subterminal object|subterminal objects]] $U_n$ around this time with $U_n([k])=\empty\, ,\, k\geq n+1$. By generalities, the corresponding [[open subtopos]] is equivalent to $Set^{\Delta_+^{op}}/U_n$ but clearly this is equivalent to the full subcategory of semi-simplicial sets $X$ with $X([k])=\empty\, ,\, k\geq n+1$.

These are precisely the $o(m)$-skeleta of the topologies $o(m)$ defined above whereas the $o(m)$-sheaves are presheaves that have unique filling $n$-semi-simplices for $n\geq m$. Hence, a $o(m)$-skeletal presheaf $X$ is an $o(m+1)$-sheaf and in general not a $j_w$-sheaf for any $j_w$ with $w_{m+1}=1$ since $X[m+1]=\empty\,$. Accordingly, $\hat{o}(m)=o(m+1)\,$: the "Hegelian [[Aufhebung]] of $\empty$" starting with $j_{max}=o(0)$ passes stepwise $o(m)\to o(m+1)$ exactly through the open subtoposes except the "subtopos at $\infty$" $o(\infty)=j_min$ for which $\hat{o}(\infty)=o(\infty)$. This contrasts somewhat with the situation in [[SSet]] where $\hat{j}_{0^m\bar{1}}=j_{0^{2m-1}\bar{1}}$ for $m\geq 2$ (cf. [[Aufhebung]] for more on this case).

Before determining the topologies $c(m)$ for the [[closed subtopos|closed subtoposes]], let's have a look at the lattice operations: the [[join]] $j_w\vee j_z$ of two topologies is given by the topology $j_{w\vee z}$ with $(w\vee z)_i=w_i$ in case $w_i=z_i$ or else $(w\vee z)_i=1$. As usual, the sheaf topos corresponding to $j_w\vee j_z$ is given by the intersection of the two sheaf toposes. The [[meet]] $j_w\wedge j_z$ is given by $j_{w\wedge z}$ with $(w\wedge z)_i=w_i$ in case $w_i=z_i$ or else $(w\wedge z)_i=0$. Hence the [[complement]] of a topology $j_w$ is given by $j_{\overline{w}}$ with $\overline{w}_i\neq w_i$ for all $i$ e.g. for an open topology $o(m) =j_{0^m\bar{1}}$ the closed complement $c(m)=\neg o(m)$ is given by $j_{1^m\bar{0}}$.

The open and closed topologies are far from being the only complemented topologies - the letter flipping operation $w\to\overline{w}$ provides a _complement_ $j_\overline{w}$ for _every_ topology $j_w$. Hence, the lattice of topologies is not only as usually a [[Heyting algebra]] but a [[Boolean algebra]], in fact, the product algebra $\prod_\mathbb{N}\mathbf{2}$.

Let us call a topology $j_w$ _locally closed_ when the corresponding sheaf topos is [[locally closed subtopos|locally closed]] i. e. $j_w$ is the join of an open and a closed topology. The locally closed topologies that are neither open nor closed themselves are then necessarily of the form $j_{1^n0^m\bar{1}}$.

For further details on the [[Lawvere-Tierney topology|Lawvere-Tierney topologies]], [[closure operator|closure operators]] and [[sheaf|sheaves]] involved in both cases see [Rosset-Hansen-Endrullis (2024)](#RHE24).


## Historical and terminological remarks
 {#History}

The original paper [Eilenberg & Zilber 50](#EilenbergZilber50) defined both (what we now call) semi-simplicial sets, under the name *semi-simplicial complexes*, and (what we now call) simplicial sets, under the name *complete semi-simplicial complexes*.  The motivation for the name "semi-simplicial" was that a semi-simplicial set is like a [[simplicial complex]], but lacks the property that a [[simplex]] is uniquely determined by its vertices.  Then they added the degeneracies and a corresponding adjective "complete."

Over time it became clear that "complete semi-simplicial complexes" were much more important and useful than the non-complete ones.  This seems to have led first to the omission of the adjective "complete," and then the omission of the prefix "semi" (and at some point the replacement of "complex" by "set"), resulting in the current name [[simplicial sets]].

The concept is essentially the same as that of $\Delta$-set, as used by [Rourke & Sanderson 71](#RourkeSanderson71). Their motivation was from geometric topology.

On the other hand, in other contexts the prefix "semi-" is used to denote absence of identities (such as a [[semigroup]] (which is, admittedly, missing more than identities relative to a group) or a [[semicategory]]),  thus if we start from the modern name "simplicial sets" it makes independent sense to refer to their degeneracy-less variant as "semi-simplicial sets."  This is coincidentally in line with the original terminology of Eilenberg and Zilber, but not of course with the intermediate usage of "semi-simplicial set" for what we now call a "simplicial set."

Note also the existence of an alternative terminology "presimplicial sets", or "pre-simplicial sets", which can be traced back at least to the textbook "Cellular Structures in Topology" by Fritsch and Piccinini in 1990. This terminology is commonly used e.g. in the context of simplicial models for concurrent programs or higher-dimensional [[automata]] (see e.g. "First introduction to simplicial sets" by [[Sina Hazratpour]]).

Similarly, the subcategory of injective functions of the simplex category was written $\Delta$ at some time of the history (e.g. in [Rourke & Sanderson 71](#RourkeSanderson71)) but this is now the standard notation for the [[simplex category]]. In the more recent history, different notations can be found but none seems to be widely adopted. $\Delta_+$ emphasizes that it is the subcategory of $\Delta$ that raise the degree when $\Delta$ is seen as a [[Reedy category]] but the $+$ may also ambiguously suggests that it adds something to $\Delta$. The notation $\Delta_{inj}$  emphasizes that it is the subcategory of injective morphisms of $\Delta$. Similarly for $\Delta_i$ though less explicitly. The notation $\widehat{\Delta}$ (e.g. in [Friedman](#Friedman12)) has the risk of introducing a confusion for readers used with the hat notation for presheaves. The notation $\Delta'$ and $\overline{\Delta}$ (e.g. in [[Sina Hazratpour]]) express that it is a variant of $\Delta$ but without giving precisions.

## Indexed semi-simplicial sets

Classically, a semi-simplicial set is a [[presheaf]] on the category $\Delta_i$, of finite nonempty ordinals and just [[injections]] between them as [[morphisms]]. However, in [[dependent type theory]], by iterating the [[categorical semantics of dependent types|correspondence between fibrations and families]], there is a second way of representing semi-simplicial types: not as a contravariant functor but as a family of families. This can be called "indexed" presentation of semi-simplicial types based on "iterated dependencies".

To illustrate the idea of *indexed semi-simplicial sets* as families of families of $n$-semi-simplices, let us consider the finite-dimensional parts of such semi-simplicial set. 

Let $\mathrm{Set}$ be a [[category of sets]]. Then, 

* A $\mathrm{Set}$-small 0-semi-simplicial set is just a $\mathrm{Set}$-small set $X_0:\mathrm{Set}$.

* A $\mathrm{Set}$-small 1-semi-simplicial set is a $\mathrm{Set}$-small 0-semi-simplicial set $X_0$ with a family of $\mathrm{Set}$-small sets 
$$x_0:X_0, x_1:X_0 \vdash X_1(x_0, x_1):\mathrm{Set}$$

* A $\mathrm{Set}$-small 2-semi-simplicial set is a $\mathrm{Set}$-small 1-semi-simplicial set $(X_0, X_1)$ with a family of $U$-small set
$$x:X_0, x_1:X_0, x_2:X_0, x_{0, 1}:X_1(x_0, x_1), x_{1, 2}:X_1(x_1, x_2), x_{0, 2}:X_1(x_0, x_2) \vdash X_2(x_0, x_1, x_2, x_{0, 1}, x_{1, 2}, x_{0, 2}):\mathrm{Set}$$
representing triangular configurations from $X_0$ and $X_1$. 

* A $\mathrm{Set}$-small 3-semi-simplicial set is a $\mathrm{Set}$-small 2-semi-simplicial set $(X_0, X_1, X_2)$ with a family of $\mathrm{Set}$-small sets 
$$\begin{array}{l}
x:X_0, x_1:X_0, x_2:X_0, x_3:X_0, \\
x_{0, 1}:X_1(x_0, x_1), x_{1, 2}:X_1(x_1, x_2), x_{2, 3}:X_1(x_2, x_3), \\ 
x_{0, 2}:X_1(x_0, x_2), x_{1, 3}:X_1(x_1, x_3), x_{0, 3}:X_1(x_0, x_3), \\ 
x_{0, 1, 2}:X_2(x_0, x_1, x_2, x_{0, 1}, x_{1, 2}, x_{0, 2}), x_{0, 1, 3}:X_2(x_0, x_1, x_3, x_{0, 1}, x_{1, 3}, x_{0, 3}), \\
x_{0, 2, 3}:X_2(x_0, x_2, x_3, x_{0, 2}, x_{2, 3}, x_{0, 3}), x_{1, 2, 3}:X_2(x_1, x_2, x_3, x_{1, 2}, x_{2, 3}, x_{1, 3}), \\
\vdash X_2(x_0, x_1, x_2, x_3, x_{0, 1}, x_{1, 2}, x_{2, 3}, x_{0, 2}, x_{1, 3}, x_{0, 3}, x_{0, 1, 2}, x_{0, 1, 3}, x_{0, 2, 3}, x_{1, 2, 3}):\mathrm{Set}
\end{array}$$
representing tetrahedral configurations from $X_0$, $X_1$ and $X_2$. 

And so on. Then a $\mathrm{Set}$-small semi-simplicial type (i.e. infinity-semi-simplicial sets) should be a set that is an $\mathrm{Set}$-small $n$-semi-simplicial set for all $n$. 

[[Hugo Herbelin]] worked at the IAS on a formalization in [[Coq]] based on the presentation of $\Delta_i$ with face maps $d_i$. In [Herbelin (2014)](#Herbelin14) he describes the construction in [[Coq]] assuming that the types in every [[type universe]] satisfy [[uniqueness of identity proofs]] (UIP), which implies that every type is a [[set]]. What the construction shows is how to define in all details such alternative presentation of semi-simplicial sets based on iterated dependencies, what can also be seen as an effective and generic construction of [[Reedy model structure|matching object]] representatives in a semi-simplicial set.

## Related concepts

* [[simplicial object]]

  * [[simplicial set]]

  * [[simplicial object in an (∞,1)-category]]

* [[semi-simplicial object]]

* [[semicategory]]

* [[semi-Segal space]]

* [[semi-simplicial topological space]]

## References

* {#EilenbergZilber50} [[Samuel Eilenberg]], [[Joseph Zilber]], *Semi-Simplicial Complexes and Singular Homology*, *Annals of Mathematics* vol. 51 no. 3 (1950), 499--513 ([jstor:1969364](https://www.jstor.org/stable/1969364))

* [[Daniel Kan]], *Is an ss complex a css complex?*, Advances in Mathematics
Volume 4, Issue 2, April 1970, Pages 170-171 (<a href="https://doi.org/10.1016/0001-8708(70)90021-6">doi:10.1016/0001-8708(70)90021-6</a>)

*  {#RourkeSanderson71} [[Colin Rourke]],  [[Brian Sanderson]], _&#916;-Sets I: Homotopy Theory_. The Quarterly Journal of Mathematics 22: 321&#8211;338 (1971) ([doi:10.1093/qmath/22.3.321](https://doi.org/10.1093/qmath/22.3.321), [pdf](http://www.maths.ed.ac.uk/~aar/papers/deltars.pdf))

* S. Buoncristiano, [[Colin Rourke]], [[Brian Sanderson]], _A geometric approach to Homology Theory_, LMS Lect. Notes 18, (1976)

* [[Peter Hilton]], _On a generalization of nilpotency to semi-simplicial complexes_ ([pdf](http://plms.oxfordjournals.org/content/s3-10/1/604.full.pdf))

* [[Alex Heller]], _Homotopy resolutions of semi-simplicial complexes_, Transactions of the American Mathematical Society Vol. 80, No. 2 (Nov., 1955), pp. 299-344 ([JSTOR](http://www.jstor.org/stable/1992992))

* [[James McClure]], On semisimplicial sets satisfying the Kan condition ([arXiv:1210.5650](http://arxiv.org/abs/1210.5650)).

* {#Friedman12} [[Greg Friedman]], _An elementary illustrated introduction to simplicial sets_, Rocky Mountain J. Math. 42(2): 353-423 (2012) ([arXiv:0809.4221](http://arxiv.org/abs/0809.4221)).

* [[Andrew Ranicki]], _Algebraic L-Theory and Topological Manifolds_, Cambridge University Press 2002.

See also the references at _[[semi-simplicial object]]_ and:

* Wikipedia, _[Delta sets](http://en.wikipedia.org/wiki/Delta_set)_

* MO, _[Semi-simplicial versus simplicial sets (and simplicial categories)](http://mathoverflow.net/questions/75094/semi-simplicial-versus-simplicial-sets-and-simplicial-categories)_
    _[Degeneracies for semi-simplicial Kan complexes](http://mathoverflow.net/questions/57653/degeneracies-for-semi-simplicial-kan-complexes/)_

On the [[model structure on semi-simplicial sets]]:

* [[Benno van den Berg]], _A note on semisimplicial sets_, 2013 ([[vandenBerg_SemisimplicialSets.pdf:file]])

as a [[weak model category]]:

* {#Henry18} [[Simon Henry]], Theorem 5.5.6 of: *Weak model categories in classical and constructive mathematics*, Theory and Applications of Categories, Vol. 35, 2020, No. 24, pp 875-958.  ([arXiv:1807.02650](https://arxiv.org/abs/1807.02650), [tac:35-24](http://www.tac.mta.ca/tac/volumes/35/24/35-24abs.html))

as a [[semi-model category]]:

* {#Rooduijn2018} Jan Rooduijn, *A right semimodel structure on semisimplicial sets*, Amsterdam 2018 ([pdf](https://eprints.illc.uva.nl/id/eprint/1663/1/MoL-2018-34.text.pdf), [mol:4787](https://msclogic.illc.uva.nl/theses/archive/publication/4787/A-right-semimodel-structure-on-semisimplicial-sets))

as a [[fibration category]] and [[cofibration category]]:

* {#Sattler18} [[Christian Sattler]], *Constructive homotopy theory of marked semisimplicial sets* ([arXiv:1809.11168](https://arxiv.org/abs/1809.11168))

on the lattice of [[Lawvere-Tierney topology|Lawvere-Tierney topologies]]:

* {#RHE24}A. Rosset, H. H. Hansen, J. Endrullis, _Characterisation of Lawvere-Tierney Topologies on Simplicial Sets, Bicolored Graphs, and Fuzzy Sets_, arXiv:2407.04535 (2024). ([abstract](https://arxiv.org/abs/2407.04535)) 

### In dependent type theory

* {#Herbelin14} [[Hugo Herbelin]], *A dependently-typed construction of semi-simplicial types*, Mathematical Structures in Computer Science, Vol 25 (special issue 05), 2015 &lbrack;[pdf](http://pauillac.inria.fr/~herbelin/articles/mscs-Her14-semisimplicial.pdf), [[Herbelin-SemiSimplicial.pdf:file]]&rbrack; &lbrack;Coq [code](http://pauillac.inria.fr/~herbelin/articles/semisimplicial.v)&rbrack;

* [[Thorsten Altenkirch]], [[Paolo Capriotti]], [[Nicolai Kraus]], _Extending Homotopy Type Theory with Strict Equality_, CSL 2016, [arXiv](http://arxiv.org/abs/1604.03799)

The original page about [[semi-simplicial types]] on the wiki of the Univalent Foundations year contained also material related to semi-simplicial sets in general though not to semi-simplicial types properly speaking. It is kept here for historical reasons.

**Update 4/12**: [A note on semisimplicial sets](https://ncatlab.org/ufias2012/files/semisimplicialsets.pdf) by Benno van den Berg.

**Update 4/15**: [A note on a presheaf model for simplicial sets](https://ncatlab.org/ufias2012/files/countermodel.pdf) by Marc Bezem and Thierry Coquand.

**Update 6/24**: Accompanying files to Update 4/15:

* [CL.pl](https://ncatlab.org/ufias2012/files/CL.pl), the prover for coherent logic (requires [SWI-Prolog](http://www.swi-prolog.org/))
* [X.in](https://ncatlab.org/ufias2012/files/X.in), a formalization of the model in coherent logic
* [X.model](https://ncatlab.org/ufias2012/files/X.model), the edges, fill1 and fill2, day by day, generated by the prover from input X.in.
* [X.v](https://ncatlab.org/ufias2012/files/X.v), a Coq script verifying the proof that no homotopy equivalence between the fibers can exist in the model.

[[!redirects Delta set]]
[[!redirects Delta sets]]

[[!redirects semi-simplicial set]]
[[!redirects semi-simplicial sets]]
[[!redirects semisimplicial set]]
[[!redirects semisimplicial sets]]

[[!redirects indexed semi-simplicial set]]
[[!redirects indexed semi-simplicial sets]]
[[!redirects indexed semisimplicial set]]
[[!redirects indexed semisimplicial sets]]

[[!redirects semi-simplicial set in homotopy type theory]]
[[!redirects semi-simplicial sets in homotopy type theory]]
[[!redirects semisimplicial set in homotopy type theory]]
[[!redirects semisimplicial sets in homotopy type theory]]

[[!redirects semi-simplicial set in dependent type theory]]
[[!redirects semi-simplicial sets in dependent type theory]]
[[!redirects semisimplicial set in dependent type theory]]
[[!redirects semisimplicial sets in dependent type theory]]

