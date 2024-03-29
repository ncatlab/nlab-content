

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

There exist various [[model category]] structures which [[presentable (infinity,1)-category|present]] the [[homotopy theory]] of [[L-∞ algebras]].

By definition [[L-∞ algebras]] are the [[∞-algebras]] in the [[category of chain complexes]] over the [[Lie operad]]. As such they carry a [[model structure on algebras over an operad]]. There is a strictification which leads equivalently to a [[model structure on dg-Lie algebras]].

A more geometric way is to think of [[L-∞ algebras]] as being the [[tangent spaces]] to connected [[smooth ∞-groupoids]], hence to the [[delooping]]/[[moduli ∞-stacks]] $\mathbf{B}G$ of [[smooth ∞-groups]], hence as the first order infinitesimal neighbourhood

$$
  \mathbf{B}\mathfrak{g} \hookrightarrow \mathbf{B}G
$$

of the essentially unique point $* \to \mathbf{B}G$ (see at _[[Lie differentiation]]_). Since this is equivalently the first order neighbourhood of the _[[formal geometry|formal]]_ neighbourhood (the [[jets]]) and the formal neighbourhood can be described purely in terms of [[associative algebra]]/[[coalgebra]] (see at [[smooth algebra]]) many models for $L_\infty$-algebras are formulated in terms of such data.

In particular, one succinct way to present [[L-∞ algebras]] (as discussed there) is as [[dg-coalgebras]]:

+-- {: .num_prop  #LInfinityAlgebraIsQuasiFreeDgCoalgebra}
###### Proposition/Definition

An [[L-∞ algebra]] $(\mathfrak{g}, [-], [-,-], [-,-,-], \cdots)$ structure on a [[graded vector space]] $\mathfrak{g}$ is equivalently a [[dg-coalgebra]] structure on the graded-commutative [[cofree coalgebra]] over $\mathfrak{g}$.

Conversely, the [[category]] of [[L-∞ algebras]] (and general "weak" morphisms between them) is the [[full subcategory]] of that of counital cocommutative [[dg-coalgebras]] on those whose underlying bare graded-commutative [[coalgebra]] (forgetting the codifferential) is free

$$
  L_\infty Alg \hookrightarrow dgCoCAlg
  \,.
$$

=--

Accordingly it is of interest to have also [[model structure on dg-coalgebras]] or dually (on [[pro-objects]] of) [[dg-algebras]] which presents $L_\infty$-algebras. Prop. \ref{LInfinityAlgebraIsFibrantObjectIndgFormalSpace} below identifies the category $L_\infty Alg$ as the ([[full subcategory|full sub-]])[[category of fibrant objects]] inside such a model structure of "differential graded formal spaces", which in turn is related by a [[zig-zag]] of [[Quillen equivalence]] to various other models

+-- {: .num_remark}
###### Remark/Warning

So we write "$L_\infty Alg$" here for the _[[1-category]]_ of $L_\infty$-algebras and general morphisms between them, since this is an entry on model category presentations. If we want to refer to the [[(∞,1)-category]] of $L_\infty$-algebras we here write explicitly "$L_W( L_\infty Alg)$", referring to the [[simplicial localization]] of this 1-category.

=--

+-- {: .num_remark}
###### Remark/Warning

All gradings in the following are $\mathbb{Z}$-gradings, unless explicitly stated otherwise. In terms of the underlying [[geometry]] this means that we are dealing with [[derived geometry]] (see below the section _[Simplicial sheaves over comsimplicial formal spaces](##SheavesOverCosimplicialInfinitesimallyThickenedPoints)_ for details): the algebra elements in positive degree correspond to [[category theory|categorical]]/[[simplicial object|simplicial]]/[[∞-groupoid]]/[[∞-stack]]-degree, and those in negative degree to the [[cosimplicial object|cosimplicial]] degree of the derived site of cosimplicial formal spaces.

Technically this affects for instance the nature of [[fibrations]]: for instance the [[model structure on dg-Lie algebras]] [below](#OndgLieAlgebras) is [[transferred model structure|transferred]] from a [[model structure on chain complexes]]. For unbounded chain complexes this is the "[Categorical projective class structure](model+structure+on+chain+complexes#CategoricalProjectiveClass)" whose fibrations are the [[chain maps]] that are surjective in every degree. This appears for instance in prop. \ref{ModelStructureOnDgLieAlgebras} and prop. \ref{LInfinityAlgebrasAsACategoryOfFibrantObjects} below.

On the other hand, if one considered chain complexes in non-negative degree (for tangent complexes in "higher but non-derived geometry"), then one would use the [Projective structure on chain complexes in non-negative degree](model+structure+on+chain+complexes#ProjectiveStructureOnChainComplexes). This has as fibrations precisely the chain maps that are surjective in every _positive_ degree. This case is (currently) *not* discussed in the following.

=--

+-- {: .num_remark #NonWeakMaps}
###### Remark/Warning

Some of the model structures below are on the category of $L_\infty$-algebras with "strict" morphisms between them, namely for those morphisms which are morphisms of [[algebras over an operad]] for an $L_\infty$-algebra regarded as an algebra over a [[cofibrant resolution]] of the [[Lie operad]]. We write

$$
  L_\infty Alg_{str} \to L_\infty Alg
$$

for the [[wide subcategory]] on the strict $L_\infty$-morphisms.

=--

## Definition as algebras over an operad

As their name indicates, [[L-∞ algebras]] are the [[homotopy algebras]] [[algebra over an operad|over]] the [[Lie operad]] (in a [[category of chain complexes]]). As such, the general theory of [[model structures on algebras over an operad]] provides a [[model category]] structure on the category of $L_\infty$-algebras. 

This we discuss here. But there is also a natural identification of $L_\infty$-algebras with [[infinitesimal object|infinitesimal]] [[derived stack|derived]] [[∞-stacks]]. For expressing this a host of other, Quillen equivalent model structures are available. These we discuss below in _[Definitions as formal/infinitesimal ∞-stacks](#DefinitionsAndQuillenEquivalences)_.

By the general discussion at _[[model structure on dg-algebras over an operad]]_, if $k$ is a [[field]] which contains the field of [[rational numbers]], then for every [[symmetric operad]] (uncolored) $\mathcal{O}$ in the [[category of chain complexes]] (unbounded) $Ch_\bullet(k)$, the [[free-forgetful adjunction]]

$$
  Alg(\mathcal{O})
  \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}}
  Ch_\bullet(k)
$$

between the [[algebras over an operad]] and the underlying chain complexes induces a [[transferred model structure]] from the projective unbounded [[model structure on chain complexes]] where hence on both sides

* the weak equivalences are the morphisms that are [[quasi-isomorphisms]] on the (underlying) chain complexes;

* the fibrations are the morphisms that are degreewise [[surjections]] on the (underlying) chain complexes.

Hence in particular $(F \vdash U)$ is [[Quillen adjunction]] between these model structures. 

([Hinich97, theorem 4.1.1](#Hinich97))

So this is in particular true for $\mathcal{O} = \widehat Lie$ the standard [[cofibrant resolution]] of the [[Lie operad]]. In this case $Alg(\widehat Lie) \simeq L_\infty Alg_{str}$ is the category of (unbounded) $L_\infty$-algebras (with strict $L_\infty$-maps between them as in remark \ref{NonWeakMaps} above) and hence is equipped with a [[transferred model structure]] this way

$$
  L_\infty Alg_{str}(k)
  \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}}
  Ch_\bullet(k)
  \,.
$$

Moreover, by the rectification result discussed at _[[model structure on dg-algebras over an operad]]_, the resolution map $\widehat Lie \stackrel{\simeq}{\to} Lie$ induces a [[Quillen equivalence]]

$$
  L_\infty Alg_{str}(k) \stackrel{\simeq}{\to} dgLieAlg(k)
$$

with the [[model structure on dg-Lie algebras]], similarly [[transferred model structure|transferred]] from the [[model structure on chain complexes]].



## Definitions as formal/infinitesimal $\infty$-stacks  
 {#DefinitionsAndQuillenEquivalences}

We list here definitions of various further [[model category]] structures that all [[presentable (infinity,1)-category|present]] the [[(∞,1)-category]] of [[L-∞ algebras]] and describe a web of [[zig-zags]] of [[Quillen equivalences]] between them. These Quillen equivalences may be thought of as presenting an equivalence between the [[(∞,1)-category]] of $L_\infty$-algebras and that of [[infinitesimal object|infinitesimal]] [[derived stack|derived]] [[∞-stacks]] ("[[formal moduli problems]]").

* [Summary](#DefinitionsAndQuillenEquivalencesSummary)

* [On dg-Lie algebras](#OndgLieAlgebras)

* [On dg-Coalgebras](#OndgCoalgebras)

* [On simplicial sheaves over cosimplicial formal spaces](#SheavesOverCosimplicialInfinitesimallyThickenedPoints)

* [On dg-formal spaces](#OnDgInfinitesimallyThickenedPoints)

### Summary
 {#DefinitionsAndQuillenEquivalencesSummary}

The following tabulates the main categories considered below, the functors relating them and their homotopy theoretic nature. The last row points to the relevant definitions and propositions of the following text. 

|  [[L-∞ algebras]] | form [[Chevalley-Eilenberg algebra]] | [[pro-objects]] in commutative [[Artin algebra|Artin]] [[dg-algebras]] | dualize | commutative [[dg-coalgebra]] | form [[tangent space|tangents]] | [[dg-Lie algebras]] |
|--|--|--|--|--|--|--|
| $L_\infty Alg$ | $\stackrel{CE}{\hookrightarrow}$ | $Pro(dgArtinCAlg)^{op} $ | $\underoverset{\;\simeq\;}{(-)^*}{\longrightarrow}$ | $dgCoCAlg$ | $\stackrel{\mathcal{L}}{\to}$ | $dgLieAlg$ | 
|    |     | $=: dgFormalSpace$ |   |  | | |
| [[category of fibrant objects]] | [[equivalence of (∞,1)-categories]] under [[simplicial localization]] |  [[opposite model structure]] of [[cofibrantly generated model category]] |  [[left adjoint|left]] [[Quillen equivalence]] | [[model category]] |  [[left adjoint|left]] [[Quillen equivalence]] | [[cofibrantly generated model category|cofibrantly generated]] [[model category]] |
| prop. \ref{LInfinityAlgebraIsQuasiFreeDgCoalgebra} | def. \ref{ChevalleyEilenbergAlgebraConstruction} | def. \ref{dgFormalSpace} | prop. \ref{DualizingInclusionOfDGFormalSpaceIntoDgCoalgebras} | def. \ref{DGCoalgebrasCategory} |  prop. \ref{LeftAdjointFromDgCoAlgToDgAlg} | def. \ref{dgLieAlgebraCategory} |

Here we are trying to use suggestive names of the categories involved. The notation used here corresponds to that in ([Pridham](#Pridham)) by the following dictionary 


> (handle with care, may still need attention)

| notation  used here | notation in [Pridham](#Pridham) |
|--|--|
| $DerivedFormalSpace$, def. \ref{DerivedFormalSpace} | $scSp$, def. 1.32 |
| $dgFormalSpace$, def. \ref{dgFormalSpace} | $DG_\mathbb{Z}Sp$. def. 3.1 |
| $FormalSpace^{\Delta^{op}}$ | $sDGSp$, def. 4.6 |

### On dg-Lie algebras
 {#OndgLieAlgebras}

Let $k$ be a [[field]] of [[characteristic]] 0.

+-- {: .num_defn #dgLieAlgebraCategory}
###### Definition

Write $dgLieAlg_k \in Cat$ for the [[category]] of [[dg-Lie algebras]]
over $k$.

=--

+-- {: .num_prop #ModelStructureOnDgLieAlgebras}
###### Proposition

The category $dgLieAlg_k$ carries a 
[[cofibrantly generated model category|cofibrantly generated]] 
[[model category]] structure in which

* [[fibrations]] are the degreewise [[surjective maps]];

* [[weak equivalences]] are the [[quasi-isomorphisms]]

on the underlying [[chain complexes]]. This is the 
[[transferred model structure]] of the corresponding 
[[model structure on chain complexes]] along the [[forgetful functor]]
to the [[category of chain complexes]].

=--

([Pridham, lemma 3.24](#Pridham))

We call this the **[[model structure on dg-Lie algebras]]**.


+-- {: .num_defn #SendingDGLieAlgebraToDgCoalgebra}
###### Definition

Write 

$$
  \mathcal{C} \;\colon\;  dgLieAlg_k \to dgCoCAlg_k
$$

for the [[functor]] which sends a [[dg-Lie algebra]] $(\mathfrak{g},d,[-,-])$ to the [[dg-coalgebra]] whose underlying [[coalgebra]] is free on the underlying [[graded vector space]] $\mathfrak{g}$ and whose [[coderivation]] is given by

$$
  \delta \colon v_1 \mapsto d v_1
$$

$$  
  \delta \colon (v_1, v_2) \mapsto [v_1, v_2]
$$

and then extended as a coderivation.

(The _Chevalley-Eilenberg_ dg-coalgebra.)

=--




+-- {: .num_prop #LeftAdjointFromDgCoAlgToDgAlg}
###### Proposition

The functor from def. \ref{SendingDGLieAlgebraToDgCoalgebra} has 
a [[left adjoint]]

$$
  \mathcal{L} \;\colon\;   dgCoCAlg_k \to dgLieAlg_k
  \,.
$$

=--

([Quillen 69, App. B6](#Quillen69), [Hinich98, 1.2.1, 2.2.5](#Hinich98), see also [Pridham, def. 3.23](#Pridham)).

+-- {: .num_remark}
###### Remark

If one thinks of a [[dg-coalgebra]] as presenting a
a derived formal space, as discuss [below](#SheavesOverCosimplicialInfinitesimallyThickenedPoints)
then its image under $\mathcal{L}$, prop. \ref{LeftAdjointFromDgCoAlgToDgAlg}, 
may be thought of as its _tangent dg-Lie algebra_. Therefore $\mathcal{L}$
is also called the **tangent Lie algebra functor**.

=--

([Hinich98, 1.2.1](#Hinich98))

### On dg-coalgebras
 {#OndgCoalgebras}

Let $k$ be a [[field]] of [[characteristic]] 0.

+-- {: .num_defn #DGCoalgebrasCategory}
###### Definition

Write $dgCoCAlg_k \in Cat$ for the [[category]] of 
co-commutative counital $\mathbb{Z}$-[[graded object|graded]]
[[dg-coalgebras]] over $k$.

=--

+-- {: .num_prop #ModelStructureOnCocommutativeDGCoalgebras}
###### Proposition

There exists a [[model category]] structure on $dgCoCAlg_k$
for which

* the [[cofibrations]] are the morphisms that are degreewise [[injections]];

* the [[weak equivalences]] are the morphisms $f$ whose corresponding morphisms of [[dg-Lie algebras]] $\mathcal{L}(f)$, prop. \ref{LeftAdjointFromDgCoAlgToDgAlg}, is a [[quasi-isomorphism]] on the underlying [[chain complexes]].

=--

([Hinich98, theorem 3.1](#Hinich98)) See also ([Pridham, lemma 3.25](#Pridham)).

We call this the **[[model structure on dg-coalgebras]]**.

+-- {: .num_remark #OndgCoAlgWEs}
###### Remark/Warning

Beware that the class of weak equivalences in prop. \ref{ModelStructureOnCocommutativeDGCoalgebras} is _not_ that of quasi-isomorphisms on the chain complexes underlying the dg-coalgebras. 

=--

But they form a sub-class:

+-- {: .num_prop #dgLieQIsTodgCoAlgs}
###### Proposition

The Chevalley-Eilenberg functor 

$$
  \mathcal{C} \;\colon\;  dgLieAlg_k \to dgCoCAlg_k
$$

from def. \ref{SendingDGLieAlgebraToDgCoalgebra} sends [[quasi-isomorphisms]] on the [[chain complexes]] underlying [[dg-Lie algebras]] to [[quasi-isomorphisms]] on the chain complexes underlying their Chevalley-Eilenberg [[dg-coalgebras]].

=--

([Lurie, prop. 2.2.6](#Lurie))


+-- {: .num_prop #QuillenEquivalenceBetweendgLieAnddgCoCAlg}
###### Proposition

The pair of [[adjoint functors]]

$$
  (\mathcal{L} \dashv \mathcal{C})
  \;\colon\;
  dgLie_k
   \stackrel{\overset{\mathcal{L}}{\leftarrow}}{\underset{\mathcal{C}}{\to}}
  dgCoCAlg_k
$$

from prop. \ref{LeftAdjointFromDgCoAlgToDgAlg} constitutes a [[Quillen equivalence]] between the [[model structure on dg-Lie algebras]], prop. \ref{ModelStructureOnDgLieAlgebras}, and the [[model structure on dg-coalgebras]], prop. \ref{ModelStructureOnCocommutativeDGCoalgebras}.

=--

([Hinich 1998, theorem 3.2](#Hinich98))

+-- {: .num_remark}
###### Remark

Since every object in $dgCoCAlg_k$ is a [[cofibrant object]] and every object in $dgLie_k$ is a [[fibrant object]], the composite

$$
  \mathcal{C}\mathcal{L}
  \colon
  dgCoCAlg_k
  \to 
  dgCocAlg_k
$$

is already its [[derived functor]] and the [[unit of an adjunction|unit]]

$$
  \mathfrak{g} \to \mathcal{C}\mathcal{L}\mathfrak{g}
$$

is a [[weak equivalence]] that exhibits $\mathcal{C}\mathcal{L}\mathfrak{g}$ as a [[fibrant resolution]] and moreover, if $\mathfrak{g}$ was already fibrant, hence by prop. \ref{LInfinityAlgebraIsFibrantObjectIndgFormalSpace} below an [[L-∞ algebra]], as a **strictification** of $\mathfrak{g}$: because a [[dg-Lie algebra]] is an $L_\infty$-algebra in which the Lie bracket satisfies its [[Jacobi identity]] strictly (not just up to a [[homotopy]] measured by the trinary bracket) and in which the "Jacobiator identity" holds strictly, etc.

=--



### On simplicial presheaves over cosimplicial formal spaces 
 {#SheavesOverCosimplicialInfinitesimallyThickenedPoints}


+-- {: .num_defn }
###### Definition

Write 

$$
  InfThPoint \hookrightarrow Alg^{op}
$$

for the category of [[infinitesimally thickened points]], the [[full subcategory]] of the [[opposite category]] of 
[[Artin algebras]] ("Weil alebras" in the language of [[synthetic differential geometry]]). The category of _[[infinitesimally thickened points]]_.

Write

$$
  cInfThPoint \hookrightarrow sAlg^{op} \simeq (Alg^{op})^{\Delta}
$$

for the [[full subcategory]] of the [[opposite category]] on [[simplicial algebras]] on those which are [[Artin algebra|Artinian]] (or "Weil" ): the category of [[cosimplicial object|cosimplicial]] [[infinitesimally thickened points]].

=--

+-- {: .num_defn }
###### Definition

Write

$$
  FormalSpace \coloneqq Fun^{lex}(InfThPoints^{op}, Set)
$$

for the [[full subcategory]] of the [[category of presheaves]] over [[infinitesimally thickened points]] on those given by [[left exact functors]].

=--

In ([Pridham](#Pridham)) this is def. 1.18.

+-- {: .num_defn #DerivedFormalSpace}
###### Definition

Write

$$
  DerivedFormalSpace \coloneqq Fun^{lex}(cInfThPoints^{op}, sSet)
$$

for the [[full subcategory]] of the category of [[simplicial presheaves]] over [[cosimplicial object|cosimplicial]] infinitesimally thickened points on those given by [[left exact functors]].

=--

In ([Pridham](#Pridham)) this is def. 1.32.


+-- {: .num_theorem }
###### Theorem 

There exists a [[cofibrantly generated model category|cofibrantly generated]] [[model category]] structure on $DerivedFormalSpace$ whose

* [[weak equivalences]] are those morphisms $f \colon X \to Y$ which are [[local morphisms]] with respect to quasi-smooth maps $p \colon E \to Y$ in the [[homotopy category]] of the [[slice category]] over $Y$.

(...)

=--

This is ([Pridham, def. 2.7, theorem 2.14](#Pridham))

+-- {: .num_prop }
###### Proposition

Between quasi-smooth objects in $DerivedFormalSpace$ the weak equivalences are precisely the morphisms which are [[weak homotopy equivalences]] of simplicial sets over each object in $cInfThPoint$.

=--

This is ([Pridham, cor. 2.16](#Pridham)).


### On dg formal spaces
 {#OnDgInfinitesimallyThickenedPoints}


+-- {: .num_defn }
###### Definition

Let $\Lambda$ be a [[commutative ring]] which is

1. [[noetherian ring|noetherian]]

1. [[local ring|local]] with 

   1. maximal ideal $\mu$ 

   1. [[residue field]] $k$.

Write 

$$
  ArtCAlg_{\Lambda} 
$$

for the [[category]] of commutative [[local Artin algebras]] over $\Lambda$ whose residue field is also $k$.

=--

[Pridham, 1.2](#Pridham)

+-- {: .num_example }
###### Example

If $\mu = 0$ then $\Lambda = k$ and we just write

$$
  ArtCAlg_k
  \,.
$$

=--

In all of the following this is assumed to be the case, with $k$ of [[characteristic zero]].

([Pridham, below def. 3.3](#Pridham))

+-- {: .num_defn #dgFormalSpace}
###### Definition

Write 

$$
  dgArtCAlg_k \in Cat
$$

for the [[category]] of $\mathbb{Z}$-[[supercommutative superalgebra|graded-commutative]] [[Artin algebra|Artin]] [[dg-algebras]] over $k$ with [[residue field]] $k$.

Write

$$
  Pro(dgArtCAlg_k) \in Cat
$$

for its category of [[pro-objects]] and write

$$
  dgFormalSpace \coloneqq Pro(dgArtCAlg_k)^{op}
$$

for the [[opposite category]] of that.

=--

This is ([Pridham, def. 3.1](#Pridham)) following ([Manetti 02](#Manetti02)).

+-- {: .num_remark #OnProAlg}
###### Remark

While it so happens that every [[nLab:coalgebra]] and [[dg-coalgebra]] is the [[filtered colimit]] of its [[finite number|finite]]-[[dimension|dimensional]] subalgebras (see at _[coalgebra -- As filtered colimits](coalgebra#AsFilteredColimits)_), this is not in general the case for [[algebras]]. But it follows that the [[linear dual]] of a general coalgebra is a [[filtered limit]] of finite-dimensional algebras, hence a [[pro-object]] in finite dimensional algebras. This is the reason for the appearance of [[pro-objects]] in def. \ref{dgFormalSpace}.

=--

+-- {: .num_prop #ModelStructureOnDgFormalSpace}
###### Proposition

There is a [[cofibrantly generated model category|cofibrantly generated]]
[[model category]] structure on $Pro(dgArtinCAlg_k)$, def. \ref{dgFormalSpace} --
hence an [[opposite model category|opposite model structure]] on $dgFormalSpaces$ -- whose [[weak equivalences]] are those morphisms that are [[local morphisms]] relative to quasi-smooth maps in the [[homotopy category]] of the [[slice category]] over their codomain.

=--

This is ([Pridham, prop. 4.36](#Pridham)).

+-- {: .num_defn #ChevalleyEilenbergAlgebraConstruction}
###### Definition

Write 

$$
  CE 
  \;\colon\;
  L_\infty Alg \stackrel{}{\to} Pro(dgArtinCAlg_k)^{op}
$$

for the [[functor]]
which regards an [[L-infinity algebra]] $\mathfrak{g}$ as a [[dg-coalgebra]] by prop. \ref{LInfinityAlgebraIsQuasiFreeDgCoalgebra} and then forms the [[dual vector space|linear dual]] [[dg-algebra]], the **[[Chevalley-Eilenberg algebra]]** $CE(\mathfrak{g})$ of $\mathfrak{g}$ (a pro-dg-algebra according to def. \ref{dgFormalSpace}).

=--

+-- {: .num_prop #LInfinityAlgebraIsFibrantObjectIndgFormalSpace}
###### Proposition

$L_\infty$-algebras are precisely the [[fibrant objects]] in $dgFormalSpace$ (hence in the [[model structure on dg cocommutative coalgebras]], by [Pridham Cor. 4.56](#Pridham)): the [[Chevalley-Eilenberg algebra]] [[functor]] of def. \ref{ChevalleyEilenbergAlgebraConstruction},

$$
  L_\infty Alg 
    \stackrel{CE}{\to} 
  Pro(dgArtinCAlg_k)^{op} 
    \simeq 
  dgFormalSpace
$$

is an [[equivalence of categories]] onto its [[essential image]], which are the [[fibrant objects]] of $dgFormalSpace$:

$$
  CE 
   \;\colon\;
  L_\infty Alg
  \stackrel{\simeq}{\to}
  dgFormalSpace_{fib}
  \hookrightarrow
  dgFormalSpace
  \,.
$$

=--

This is proven inside the proof of ([Pridham, prop. 4.42](#Pridham)).


+-- {: .num_remark #CategoryOfFibrantObjectsLInfinity}
###### Remark

Prop. \ref{LInfinityAlgebraIsFibrantObjectIndgFormalSpace} 
shows in particular that  the category $L_\infty Alg$ 
of prop/def. \ref{LInfinityAlgebraIsQuasiFreeDgCoalgebra} carries the structure of a _[[category of fibrant objects]]_ that presents the [[homotopy theory]] of $L_\infty$-algebras. Notice that, of course, passing to the full subcategory of fibrant objects does not change the [[homotopy theory]] presented by the underlying [[category with weak equivalences]] in that we have an [[equivalence of (∞,1)-categories]] between the [[simplicial localizations]]

$$
  L_W(dgFormalSpace)
  \simeq
  L_W(L_\infty Alg)
  \,.
$$

=--

The following proposition characterizes the structure of this [[category of fibrant objects]].

+-- {: .num_prop #LInfinityAlgebrasAsACategoryOfFibrantObjects}
###### Proposition

The induced structure of a [[category of fibrant objects]] on $L_\infty Alg$ under the inclusion of prop. \ref{LInfinityAlgebraIsFibrantObjectIndgFormalSpace} has

1. [[weak equivalences]] are precisely the maps that are [[quasi-isomorphisms]] on the underlying chain complexes;

1. [[fibrations]] include in particular the maps that are surjections on the underlying chain complexes.


=--

+-- {: .proof}
###### Proof

The first statement is proven in the proof of ([Pridham, prop. 4.42](#Pridham)).

The second statement follows by ([Pridham, def. 4.34](#Pridham)) with the existence of the model structure on $dgFormalSpaces$.

> Should spell out how this follows, using lifting.

=--

+-- {: .num_prop #OnWEsOnLInfinity}
###### Remark/Warning

Beware, as in remark \ref{OndgCoAlgWEs}, that the class of weak equivalences in prop. \ref{LInfinityAlgebrasAsACategoryOfFibrantObjects} differs from that of those maps on associated [[Chevalley-Eilenberg algebras]] which are quasi-isos on the underlying chain complexes of the [[dg-algebra]] (which instead are the weak equivalences in the standard [[model structure on dg-algebras]], hence in particular those used in Sullivan [[rational homotopy theory]]). Instead the weak equivalences correspond to the maps of CE-algebra that are quasi-isomorphisms only on the chain complexes given by the co-unary component of the differential of the CE-algebra.

=--

+-- {: .num_prop}
###### Proposition

There is an [[equivalence of categories]] between the [[homotopy category]] of $dgFormalSpace$ hence of $L_\infty Alg$ according to remark \ref{CategoryOfFibrantObjectsLInfinity}, and the homotopy category of $L_\infty$-algebras according to ([Kontsevich 94](#Kontsevich94)).

=--

([Pridham, prop. 4.42, see above def. 4.29](#Pridham))


+-- {: .num_prop }
###### Proposition

If $k$ is of [[characteristic]] 0 then there is a [[zig-zag]] of [[Quillen equivalences]] between
$DerivedFormalSpace$, def. \ref{DerivedFormalSpace} and $dgFormalSpace$, def. \ref{dgFormalSpace}, hence an [[equivalence of (∞,1)-categories]] between their [[simplicial localizations]]

$$
  L_W DerivedFormalSpace \simeq L_W dgFormalSpace
  \,.
$$

=--

This is ([Pridham, cor. 4.49](#Pridham)).

+-- {: .num_prop }
###### Proposition

For arbitrary $k$, there is a [[Quillen equivalence]]

$$
  dgLie_k \stackrel{\simeq}{\to} dgFormalSpace
  \,.
$$

=--

([Pridham, theorem 4.55](#Pridham))

+-- {: .num_prop #DualizingInclusionOfDGFormalSpaceIntoDgCoalgebras}
###### Proposition

The inclusion

$$
  dgFormalSpace \to dgCoCAlg_k
$$

given by sending an object in $Pro(dgArticCAlg_k)^{op} \coloneqq dgFormalSpace$, hence an [[dg-algebra]] $A$, to its dual dg-coalgebra $A^*$,
is the [[left adjoint]] part of a [[Quillen equivalence]] between the model structure on $dgFormalSpace$, prop. \ref{ModelStructureOnDgFormalSpace}, and the [[model structure on dg-coalgebras]], prop. \ref{ModelStructureOnCocommutativeDGCoalgebras}.

=--

([Pridham, cor. 4.56](#Pridham))


### On cosimplicial algebras (and dual Dold-Kan correspondence)
 {#OnCosimplicialAlgebras}

Also a version of the "[dual monoidal Dold-Kan correspondence](monoidal+Dold-Kan+correspondence#DualDoldKanQuillenEquivalences)" gives a Quillen equivalence between two model structures for $L_\infty$-algebras. This is ([Pridham, section 4.4](#Pridham)). This we discuss now


+-- {: .num_remark }
###### Remark

This equivalence has the nice property that starting with the [[Chevalley-Eilenberg algebra]] and then "denormalizing" it under dual monoidal Dold-Kan to a cosimplicial nilpotent algebra yields manifestly an incarnation of the $L_\infty$-algebra in terms of simplicial complexes of infinitesimal simplices as is implicit in the work of [[Anders Kock]] in [[synthetic differential geometry]]. This is spelled out further in [[schreiber:differential cohomology in a cohesive topos|dcct, section 4.5.1]].

=--

+-- {: .num_defn #CosimplicialDgAlgebras}
###### Definition

Write

$$
  (dg\hat {\mathcal{C}})^{\Delta}
$$

for [[cosimplicial object|cosimplicial]] [[pro-objects]] of [[dg-algebra|dg]]-[[Artin algebras]] ($\mathbb{N}$-graded).

=--

([Pridham, def. 4.6](#Pridham))

+-- {: .num_prop #ModelStructureOnCosimplicialDgAlgebras}
###### Proposition

The category $(dg\hat{\mathcal{C}})^{\Delta}$ of def. \ref{CosimplicialDgAlgebras} carries a [[model category]] structure where

(...)

=--

This is ([Pridham, def. 4.11, prop. 4.12](#Pridham)).



+-- {: .num_defn #dgdgAlgebras}
###### Definition

Write

$$
  DGdg\hat \mathcal{C}
$$

for [[pro-objects]] in [[dg-algebras]] ($\mathbb{N}$-graded) in [[dg-algebras|dg]]-[[Artin algebras]] ($\mathbb{N}$-graded).

=--

([Pridham, def. 4.19](#Pridham))



+-- {: .num_prop }
###### Proposition

The dual [[monoidal Dold-Kan correspondence]] functor
from [[dg-algebras]] to [[cosimplicial algebras]] (the inverse equivalence to the [[normalized cochain complex]] functor) 

$$
  D 
  \;\colon\;
  DGdg\hat \mathcal{C}
  \to 
  (dg\hat \mathcal{C})^{\Delta}
$$

induces on $DGdg\hat \mathcal{C}$ the [[transferred model structure]] from that of prop. \ref{ModelStructureOnCosimplicialDgAlgebras} and is the [[right adjoint]] of a [[Quillen equivalence]] with respect to these model structures

=--

This is ([Pridham, theorem 4.26](#Pridham)).


## Properties

### General

We discuss some further properties of the [above](DefinitionsAndQuillenEquivalences) model category structures. 

+-- {: .num_prop #RightProperness}
###### Proposition

The model category $dgFormalSpace$, def. \ref{dgFormalSpace}, is a [[right proper model category]].

=--

This observation has been communicated privately by [[Jonathan Pridham]]

+-- {: .proof}
###### Proof

We need to show that the [[pullback]] of a weak equivalence $w$ along a fibration $f$ is again a weak equivalence. If $w$ is a fibration, this is automatic, so by factorisation we reduce to the case where $w$ is a cofibration. Now, every trivial cofibration is $Spf$ of a composition of acyclic small extensions, so we may take $w$ to be $Spf$ of an acyclic small extension $A \to B$ with [[kernel]] $I$. Then $f$ is $Spf$ of a quasi-free map $A \to R$, so the pullback is $Spf$ of $R \to R/IR$, and $IR =I\hat{\otimes}_A R$, so $R \to R/IR$ is also an acyclic small extension.

=--

### Homotopies and derived hom spaces
 {#HomotopiesAndDerivedHomSpaces}

In any [[model category]] we have a notion of [[homotopy]] between [[1-morphisms]]. In any [[category of fibrant objects]] we still have a notion of [[right homotopy]], given by maps into a [[path space object]]. So all of the above model category/fibrant object category structures yield models for [[homotopies]] between morphisms of $L_\infty$-algebras.

A discussion of [[path space objects]] of and hence of [[right homotopies]] between $L_\infty$-algebras (in the category of def. \ref{LInfinityAlgebraIsQuasiFreeDgCoalgebra}) is for instance in ([Dolgushev 07, section 5](#Dolgushev07)).

More generally, a description of the full [[derived hom space]] between two $L_\infty$-algebras is obtained via remark \ref{CategoryOfFibrantObjectsLInfinity} from the description of [derived hom-spaces in categories of fibrant objects](category+of+fibrant+objects#DerivedHomSpaces).

### Homotopy fiber products
 {#HomotopyFiberProducts}

Recognizing [[homotopy fiber products]] in any of the model structure above can be a bit subtle. A recognition principle of [[homotopy fibers]] over abelian $L_\infty$-algebras , hence useful for discussion of [∞-Lie algebra extensions](infinity-Lie+algebra+cohomology#Extensions)), is described in ([Fiorenza-Rogers-Schreiber 13, theorem 3.1.13](#FiorenzaRogersSchreiber13)).


## Related concepts

* [[relation between L-∞ algebras and dg-Lie algebras]]

* [[model structure on dg-coalgebras]]

* [[model structure on dg-Lie algebras]]

* [[model structure on simplicial Lie algebras]]

* [[L-∞ operad]], [[model structure on algebras over an operad]]

* [[deformation theory]]

  * [[Lie differentiation]]

  * [[deformation context]]

## References

Precursors for 2-reduced dg-algebras are dicussed in 

* {#Quillen69} [[Dan Quillen]], _Rational homotopy theory_, The Annals of Mathematics, Second Series, Vol. 90, No. 2 (Sep., 1969), pp. 205-295 ([jstor:1970725](http://www.jstor.org/stable/1970725), [pdf](http://www.math.northwestern.edu/~konter/gtrs/rational.pdf))
 

The homotopy-theoretic nature of $L_\infty$-algebras and their relation to deformation problems was then notably amplified in 

* {#Kontsevich94} [[Maxim Kontsevich]], _Topics in algebra &#8212; deformation theory_ Lecture Notes (1994) ([ps](http://www.math.brown.edu/&#8764;abrmovic/kontsdef.ps))


On [[model category]] [[structures]] on [[algebra over an operad|algebras over operads]] in [[chain complexes]]:

* {#Hinich97} [[Vladimir Hinich]],  *Homological algebra of homotopy algebras*, Communications in Algebra **25** 10   (1997) 3291-3323 &lbrack;[arXiv:q-alg/9702015](http://arxiv.org/abs/q-alg/9702015), [doi:10.1080/00927879708826055](https://doi.org/10.1080/00927879708826055), Erratum: ([arXiv:math/0309453](http://arxiv.org/abs/math/0309453))&rbrack;

The full model structure on [[dg-coalgebras]] (in characteristic 0) as a [[model structure for L-infinity algebras|model structure for $L_\infty$-algebras]] and the [[Quillen equivalence]] between [[dg-Lie algebras]] as well as the interpretation in terms of formal $\infty$-stacks ([[L-infinity algebras|$L_\infty$-algebras]]):

* {#Hinich98} [[Vladimir Hinich]], _DG coalgebras as formal stacks_, Journal of Pure and Applied Algebra **162** 2 (2001) 209-250 &lbrack;[arXiv:9812034](http://arxiv.org/abs/math/9812034), <a href="https://doi.org/10.1016/S0022-4049(00)00121-3">doi:10.1016/S0022-4049(00)00121-3</a>&rbrack;

Also:

* {#Valette14} Theorem 2.1 in: [[Bruno Vallette]], _Homotopy theory of homotopy algebras_, Annales de l'Institut Fourier __70__:2 (2020)  683--738 [doi](https://10.5802/aif.3322) [Zbl:1335.18001](https://zbmath.org/?q=an:1335.18001) [arXiv:1411.5533](https://arxiv.org/abs/1411.5533)

The structure of a [[category of fibrant objects]] on connective [[finite type]] $L_\infty$-algebras:

* {#Rogers18} [[Christopher L. Rogers]], _An explicit model for the homotopy theory of finite type Lie $n$-algebras_, Algebr. Geom. Topol. 20 (2020) 1371-1429 ([arXiv:1809.05999](https://arxiv.org/abs/1809.05999), [doi:10.2140/agt.2020.20.1371](https://doi.org/10.2140/agt.2020.20.1371))

(For relation to [Valette 14](#Valette14) see [Rogers 18, below Theorem 5.9](#Rogers18))

 
In 

* {#Lurie} [[Jacob Lurie]], _[[Formal Moduli Problems]]_

the relation to $\infty$-stacks is discussed more in detail.

More model category theoretic developments relating various of the previous approaches and generalizing to arbitrary characteristic are in

* {#Pridham} [[Jonathan Pridham]], _Unifying derived deformation theories_, Adv. Math. 224 (2010), no.3, 772-826 ([arXiv:0705.0344](http://arxiv.org/abs/0705.0344))
 
in parts based on 

* {#Manetti02} [[Marco Manetti]], _Extended deformation functors_, Int. Math. Res. Not., (14):719&#8211;756, 2002 ([arXiv:math/9910071](https://arxiv.org/abs/math/9910071))

A useful summary of that paper is given in the [notes](http://poisson.phc.unipi.it/~maggiolo/wp-content/uploads/2008/12/WDTII_Pridham.pdf), by Stefano Maggiolo.

A discussion of [[path space objects]] for $L_\infty$-algebras is in section 5 of 

* {#Dolgushev07} Vasiliy A. Dolgushev, _Erratum to: "A Proof of Tsygan's Formality Conjecture for an Arbitrary Smooth Manifold"_ ([arXiv:math/0703113](http://arxiv.org/abs/math/0703113))
 

A discussion of [[homotopy fibers]] of morphisms to abelian $L_\infty$-algebras (and hence [∞-Lie algebra extensions](infinity-Lie+algebra+cohomology#Extensions)) is in section 3.1 of

* {#FiorenzaRogersSchreiber13} [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:L-∞ algebras of local observables from higher prequantum bundles]]_ ([arXiv:1304.6292](http://arxiv.org/abs/1304.6292))

See also 

* [[Alexander Berglund]], _Rational homotopy theory of mapping spaces via Lie theory for L-infinity algebras_, Homology, Homotopy and Applications Volume 17 (2015) Number 2 ([arXiv:1110.6145](https://arxiv.org/abs/1110.6145), [doi:10.4310/HHA.2015.v17.n2.a16]( https://dx.doi.org/10.4310/HHA.2015.v17.n2.a16))




[[!redirects model structure for L-∞ algebras]]

[[!redirects model structures for L-∞ algebras]]
[[!redirects model structures for L-infinity algebras]]

[[!redirects homotopy theory of L-∞ algebras]]
[[!redirects homotopy theory of L-infinity algebras]]
