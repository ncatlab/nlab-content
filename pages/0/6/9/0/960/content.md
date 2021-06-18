
> This article is about smash products in [[topology]]/[[homotopy theory]]. For the notion of _Hopf smash product_ see at [[crossed product algebra]]. 

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Stable Homotopy theory
+-- {: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The _smash product_ is the canonical [[tensor product]] of [[pointed objects]] in an ambient [[monoidal category]]. It is essentially given by taking the tensor product of the underlying objects and then identifying with a new basepoint all pieces that contain the base point of either factor.

An archetypical special case is the smash product of [[pointed topological spaces]] and hence of pointed [[homotopy types]]. Under [[stabilization]] this induces the important [[smash product of spectra]] in [[stable homotopy theory]].

## Definition

### For pointed sets
 {#ForPointedSets}

+-- {: .num_defn}
###### Definition

The __smash product__ $A \wedge B$ of two [[pointed sets]] $A$ and $B$ is the [[quotient set]] of the [[cartesian product]] $A \times B$ where all points with the basepoint as a coordinate (the one from $A$ or the one from $B$) are identified.

The subset that is 'smashed' here can be identified with the [[wedge sum]] $A \vee B$, so the definition of the smash product can be summarised as follows:
$$ A \wedge B = \frac{A \times B}{A \vee B} $$

=--

+-- {: .num_prop}
###### Proposition

The smash product is the [[tensor product]] in the [[closed monoidal category]] of [[pointed sets]].  
That is, it is characterized by the existence of [[natural isomorphisms]]

$$ 
  Fun_*(A \wedge B, C) \cong Fun_*(A, Fun_*(B, C)) 
$$

where $Fun_*(A,B)$ is the set of basepoint-preserving [[functions]] from $A$ to $B$, itself made into a pointed set by taking as basepoint the [[constant function]] from all of $A$ to the basepoint in $B$.

=--

This is a special case of the general discussion [below](#ForGeneralPointedObjects).


### For general pointed objects
 {#ForGeneralPointedObjects}


Let $(\mathcal{C}, \otimes, 1_{\mathcal{C}})$ be a [[closed monoidal category|closed]] [[symmetric monoidal category]] with ([[finite limit|finite]]) [[limits]] and [[colimits]]. Write $\ast \in \mathcal{C}$ for the [[terminal object]] of $\mathcal{C}$. Write $\mathcal{C}^{\ast/}$ for the category of [[pointed objects]] in $\mathcal{C}$.  

+-- {: .num_defn #GeneralSmashProduct}
###### Definition

For $X,Y \in \mathcal{C}^{\ast/}$ two [[pointed objects]] in $\mathcal{C}$, their _smash product_ is given by the following [[pushout]] of [[pushouts]] and [[tensor products]] all formed in $\mathcal{C}$

$$
  X \wedge Y
  \coloneqq
  \ast \underset{(X \otimes \ast)\coprod (Y \otimes \ast)}{\coprod} (X \otimes Y)
$$

regarded as a pointed object via the induced [[co-projection]] from $\ast$.

=--

In this generality this appears as ([Elmendorf-Mandell 07, construction 4.19](#ElmendorfMandell07)).

+-- {: .num_prop}
###### Proposition

The smash product of def. \ref{GeneralSmashProduct} makes $\mathcal{C}^{\ast/}$ be a [[closed monoidal category|closed]] [[symmetric monoidal category]] with ([[finite limit|finite]]) [[limits]] and [[colimits]].

=--

A proof appears as ([Elmendorf-Mandell 07, lemma 4.20](#ElmendorfMandell07)). For more of these details see at _[Pointed object -- Closed and monoidal structure](pointed+object#ClosedMonoidalStructure)_. For [[base change]] functoriality of these structures see at _[Wirthm&#252;ller context -- Examples -- On pointed objects](Wirthm&#252;ller+context#PointedObjects)_.



+-- {: .num_remark}
###### Remark

The formula for the smash product in def. \ref{GeneralSmashProduct} can be considered in any [[category]] $\mathcal{C}$ with [[finite limits]] and [[colimits]], but unless $\mathcal{C}$ is closed symmetric monoidal, it will not have all these properties. 

If finite [[products]] in $C$ distribute over finite colimits, then the smash product is [[associativity|associative]], and if $C$ is also [[cartesian closed category|cartesian closed]], then it makes the category of pointed objects in $C$ [[closed monoidal category|closed monoidal]].  However, if finite products in $C$ do not distribute over finite colimits, the smash product can fail to be associative.


=--

+-- {: .num_example}
###### Example

Examples of closed symmetric monoidal categories $(\mathcal{C}, \otimes 1_{\mathcal{C}})$ include in particular [[toposes]] with their [[cartesian monoidal category|cartesian monoidal structure]]. For the topos $\mathcal{C} = $ [[Set]] the general discussion here reduces to that [above](#ForPointedSets).

=--

There is a general abstract way to obtain this smash product monoidal structure:

+-- {: .num_prop}
###### Proposition

The category of [[pointed objects]] is the [[Eilenberg-Moore category]] of [[algebras over a monad]] for the "[[maybe monad]]", $X \mapsto X \coprod \ast$. This being a suitably [[monoidal monad]] it canonically induces a monoidal structure on its EM-category, and that is the smash product.

=--

For more on this see at _[maybe monad -- EM-Category and Relation to pointed objects](maybe+monad#EMCategoryAndRelationToPointedObjects)_.


## Examples

### Of pointed topological spaces

The most common case when $\mathcal{C}$ is a category of [[topological spaces]].  In that case, the [[natural transformation|natural]] [[continuous function|map]] $A \wedge (B \wedge C) \to (A\wedge B)\wedge C$ is a [[homeomorphism]] provided $C$ is a [[locally compact Hausdorff space]]. Thus if both $A$ and $C$ are locally compact Hausdorff, then we have the [[associativity]] $A\wedge(B\wedge C)\cong (A\wedge B)\wedge C$. 

Associativity fails in general for the category [[Top]] of all topological spaces; however, it is satisfied for pointed objects in any [[convenient category of topological spaces]], since such a category is cartesian closed.  In particular, the smash product is associative for pointed [[compactly generated spaces]].


+-- {: .num_prop #OnePointCompactificationAndSmashProduct}
###### Proposition
**([[one-point compactification intertwines Cartesian product with smash product]])

On the [[subcategory]] $Top_{LCHaus}$ in [[Top]] of [[locally compact Hausdorff spaces]] with [[proper maps]] between them, the [[functor]] of [[one-point compactification]] (Prop. \ref{OnePointCompactificationFunctor})

$$
  (-)^{cpt}
  \;\colon\;
  Top_{LCHaus}
  \longrightarrow 
  Top^{\ast/}
$$


1. sends [[coproducts]], hence [[disjoint union topological spaces]], to [[wedge sums]] of [[pointed topological spaces]];

1. sends [[Cartesian products]], hence [[product topological spaces]], to [[smash products]] of [[pointed topological spaces]];

hence constitutes a [[strong monoidal functor]] for both [[monoidal category|monoidal]] structures of these [[distributive monoidal categories]] in that there are [[natural transformation|natural]] [[homeomorphism]]

$$
  \big(
    X \sqcup Y 
  \big)^{cpt}
  \;\simeq\;
  X^{cpt} \vee Y^{cpt}
  \,,
$$

and

$$
  \big(
    X \times Y 
  \big)^{cpt}
  \;\simeq\;
  X^{cpt} \wedge Y^{cpt}
  \,.
$$

=--

This is briefly mentioned in [Bredon 93, p. 199](#Bredon93).
The argument is spelled out in: [MO:a/1645794](https://math.stackexchange.com/a/1645794/58526), [Cutler 20, Prop. 1.6](#Cutler20).


### Of spectra

See at _[[symmetric smash product of spectra]]_.

## Properties


[[!include smash-monoidal diagonals -- section]]



## Related concepts

* [[pointed object]]

* [[wedge sum]]

* [[pointed mapping space]]

* While the smash product is not cartesian, it does [[monoidal category with diagonals|admit diagonals]].

## References

Basic accounts:

* {#Bredon93} [[Glen Bredon]], p. 199 of: _Topology and Geometry_, Graduate Texts in Mathematics 139, Springer 1993 ([doi:10.1007/978-1-4757-6848-0](https://link.springer.com/book/10.1007/978-1-4757-6848-0), [pdf](http://virtualmath1.stanford.edu/~ralph/math215b/Bredon.pdf))

Review:

* {#Cutler20} Tyrone Cutler, _The category of pointed topological spaces_, 2020 ([pdf](https://www.math.uni-bielefeld.de/~tcutler/pdf/Elementary%20Homotopy%20Theory%20II%20-%20The%20Pointed%20Category.pdf), [[CutlerPointedTopologicalSpaces.pdf:file]])


On the general definition of smash products via [[closed monoidal category]] structure on [[pointed objects]]:

* {#ElmendorfMandell07} [[Anthony Elmendorf]], [[Michael Mandell]], _Permutative categories, multicategories, and algebraic K-theory_, Algebraic & Geometric Topology 9 (2009) 2391-2441 ([arXiv:0710.0082](http://arxiv.org/abs/0710.0082))
 


On commutativity of smashing with [[homotopy limits]]:

* [[Wolfgang Lueck]], Holger Reich, Marco Varisco, _Commuting homotopy limits and smash products_, K-Theory, 30 (2): 137--165, 2003 ([arXiv:math/0302116](http://arxiv.org/abs/math/0302116))


[[!redirects smash product]]
[[!redirects smash products]]
[[!redirects smash produc]]
