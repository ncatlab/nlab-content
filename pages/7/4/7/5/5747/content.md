
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

Since the maps in $\Delta_+$ are all strictly monotone, any object $[n]$ receives only (finitely many) morphisms from objects $[m]$ with $m\leq n$ whence all [[slice category|slices]] $\Delta_+/[n]$ are [[finite category|finite]]. This is sufficient for all [[Grothendieck topology|Grothendieck topologies]] on $\Delta_+$ to be [[rigid topology|rigid]] whence all subtoposes of $Set^{\Delta_+^{op}}$ are [[level of a topos|essential]] and of [[presheaf topos|presheaf type]] and their lattice is isomorphic to the lattice of [[Cauchy-complete category|Cauchy-complete]] [[full subcategory|full subcategories]] of $\Delta_+$.

This situation is familiar from $\Delta$ but in the latter case there are fewer Cauchy-complete subcategories available, since an object $[n]$ having non-trivial idempotents its inclusion automatically requires the presence of all $[m]$ with $m\,$<$\,n$ in the subcategory whence there are countably many subtoposes corresponding to the $n$-truncated subcategories on the objects $[0],\dots ,[n]$ (plus the two trivial subcategories).

The [[Lawvere-Tierney topology|Lawvere-Tierney topologies]] $j_w$ on $Set^{\Delta_+^{op}}$ are indexed by infinite words $w$ over the alphabet $\{0,1\}$. They are partially ordered by $j_w\leq j_v$ iff $w_i\leq v_i$ for all letter positions $i=0,1,2,\dots$, where (unsurprisingly) letter 0 counts as smaller than letter 1. The information contained in the $i$-th letter of $w$ is whether the [[closure operator]] corresponding to $j_w$ adds $i$-dimensional semi-simplices to subobjects ($w_i=1$) or not ($w_i=0$) e.g. $j_{111\dots}$ adds all semi-simplices of every dimension implying that the empty subobject is $j_{111\dots}$-dense in every object thereby preventing all non-terminal objects from being $j_{111\dots}$-sheaves i.e. $j_{111\dots}=j_max$ while $j_{000\dots}$ where no semi-simplex of any dimension is added and every presheaf is a $j_{000\dots}$-sheaf corresponds to $j_min$. A topology $j_w$ corresponds to a [[dense subtopos]] precisely when $w$ starts with 0.

There is a countably infinite number of co-atoms $j_w$ where $w$ contains exactly one 0. These correspond to different copies of $Set$ induced by the inclusion of the one-morphism category on the objects $[n]$ in $\Delta_+$. In particular, the dense [[double negation]] copy $j_{\neg\neg}$ corresponds to $j_{0111\dots}$, the $j_{\neg\neg}$-sheaves consisting of semi-simplicial sets with an arbitrary set of $0$-semi-simplexes (= vertices) and exactly one $n$-semi-simplex in the higher dimensions for every configuration of $n$-1-semi-simplices which can bound an $n$-semi-simplex.

A topology $j_w$ restricts to a topology $j_w|_n$ on the n-truncation $\Delta_+|_n$ by taking the prefix of length $n$+1 e.g. $j_{00},j_{01},j_{10},j_{11}$ are the four topologies on the 1-truncation, the topos of [[quiver|directed graphs]].

A similar description is available for the [[Lawvere-Tierney topology|Lawvere-Tierney topologies]] $j_w$ on [[simplicial set|simplicial sets]] with the same interpretation of the letters but there $w$ has to start with a (possibly empty, possibly infinite) block of zeros expressing that the respective sheaf categories consists of $m$-truncated simplicial sets, where $m+1$ is the length of the block of zeros with which $w$ starts e.g. $j_{00111\dots}$ corresponds to the 1-truncation, the topos of [[reflexive graph|reflexive graphs]].

For further details on the [[Lawvere-Tierney topology|Lawvere-Tierney topologies]], [[closure operator|closure operators]] and [[sheaf|sheaves]] involved in both cases see [Rosset-Hansen-Endrullis (2024)](#RHE24).

## Related concepts

* [[simplicial object]]

  * [[simplicial set]]

  * [[simplicial object in an (∞,1)-category]]

* [[semi-simplicial object]]

* [[semicategory]]

* [[semi-Segal space]]

## Historical and terminological remarks
 {#History}

The original paper [Eilenberg & Zilber 50](#EilenbergZilber50) defined both (what we now call) semi-simplicial sets, under the name *semi-simplicial complexes*, and (what we now call) simplicial sets, under the name *complete semi-simplicial complexes*.  The motivation for the name "semi-simplicial" was that a semi-simplicial set is like a [[simplicial complex]], but lacks the property that a [[simplex]] is uniquely determined by its vertices.  Then they added the degeneracies and a corresponding adjective "complete."

Over time it became clear that "complete semi-simplicial complexes" were much more important and useful than the non-complete ones.  This seems to have led first to the omission of the adjective "complete," and then the omission of the prefix "semi" (and at some point the replacement of "complex" by "set"), resulting in the current name [[simplicial sets]].

The concept is essentially the same as that of $\Delta$-set, as used by [Rourke & Sanderson 71](#RourkeSanderson71). Their motivation was from geometric topology.

On the other hand, in other contexts the prefix "semi-" is used to denote absence of identities (such as a [[semigroup]] (which is, admittedly, missing more than identities relative to a group) or a [[semicategory]]),  thus if we start from the modern name "simplicial sets" it makes independent sense to refer to their degeneracy-less variant as "semi-simplicial sets."  This is coincidentally in line with the original terminology of Eilenberg and Zilber, but not of course with the intermediate usage of "semi-simplicial set" for what we now call a "simplicial set."

Note also the existence of an alternative terminology "presimplicial sets", or "pre-simplicial sets", which can be traced back at least to the textbook "Cellular Structures in Topology" by Fritsch and Piccinini in 1990. This terminology is commonly used e.g. in the context of simplicial models for concurrent programs or higher-dimensional [[automata]] (see e.g. "First introduction to simplicial sets" by [[Sina Hazratpour]]).

Similarly, the subcategory of injective functions of the simplex category was written $\Delta$ at some time of the history (e.g. in [Rourke & Sanderson 71](#RourkeSanderson71)) but this is now the standard notation for the [[simplex category]]. In the more recent history, different notations can be found but none seems to be widely adopted. $\Delta_+$ emphasizes that it is the subcategory of $\Delta$ that raise the degree when $\Delta$ is seen as a [[Reedy category]] but the $+$ may also ambiguously suggests that it adds something to $\Delta$. The notation $\Delta_{inj}$  emphasizes that it is the subcategory of injective morphisms of $\Delta$. Similarly for $\Delta_i$ though less explicitly. The notation $\widehat{\Delta}$ (e.g. in [Friedman](#Friedman12)) has the risk of introducing a confusion for readers used with the hat notation for presheaves. The notation $\Delta'$ and $\overline{\Delta}$ (e.g. in [[Sina Hazratpour]]) express that it is a variant of $\Delta$ but without giving precisions.

## Related concepts

* [[semi-simplicial object]]

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

In [[homotopy type theory]]:

* [[Thorsten Altenkirch]], [[Paolo Capriotti]], [[Nicolai Kraus]], _Extending Homotopy Type Theory with Strict Equality_, CSL 2016, [arXiv](http://arxiv.org/abs/1604.03799)

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


[[!redirects semi-simplicial sets]]
[[!redirects semisimplicial set]]
[[!redirects semisimplicial sets]]


[[!redirects Delta set]]
[[!redirects Delta sets]]
