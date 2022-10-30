
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# $2$-rigs
* table of contents
{: toc}

## Idea

The notion of  _$2$-rig_ is supposed to be a [[categorification]] of that of a [[rig]].  Several inequivalent formalizations of this idea are in the literature.

Just as a rig is a multiplicative [[monoid]] whose underlying set also has a notion of addition, so a $2$-rig is a [[monoidal category]] whose underlying category also has a notion of addition, and we can describe this notion of addition in a few different ways.

Note that we don\'t expect a $2$-rig to have additive inverses; by the same argument as in the [[Eilenberg swindle]], they are unreasonable to expect.  However, in a monoidal [[abelian category]], we have as close to additive inverses as is reasonable and so a categorification of a [[ring]].

Compare also the notion of [[rig category]].

## Definitions
 {#Definitions}

Since [[categorification]] involves some arbitrary choices that will be determined by the precise intended application, there is a bit of flexibility of what exactly what one may want to call a _2-ring_. We first list some immediate possibilities of classes of monoidal and enriched categories that one may want to think of as 2-rings:

* [Enriched monoidal categories](#EnrichedMonoidalCategories)

But a central aspect of an ordinary ring is the [[distributivity law]] which says that the product in the ring preserves sums. Since sums in a 2-ring are given by [[colimits]], this suggests that a 2-ring should be a cocomplete category which is compatibly [[monoidal category|monoidal]] in that the the tensor product preserves colimits:

* [Compatibly monoidal cocomplete categories](#MonoidalCompleteCateories)

But there are still more properties which one may want to enforce, notably that homomorphisms of 2-rings form a [[2-abelian group]]. This is achieved by demanding the underlying category to be not just cocomplete by [[presentable category|presentable]]:

* [Compatibly monoidal presentable categories](#CompatiblyMonoidalPresentableCategories).


### Enriched monoidal categories
 {#EnrichedMonoidalCategories}

1.  A __$2$-rig__ might be an [[Ab-enriched category]] which is [[enriched monoidal category|enriched monoidal]].

2.  A __$2$-rig__ might be an [[additive category]] which is enriched monoidal.

3.  A __$2$-rig__ might be a [[distributive monoidal category]]: a monoidal category with finite [[coproducts]] such that the monoidal product distributes over the coproducts.

4.  A __$2$-rig__ might be a [[closed monoidal category]] with finite coproducts.

5.  Finally, a __$2$-ring__ is a monoidal [[abelian category]].

Note that (2) is a special case of both (1) and (3), which are independent.  (4) is a special case of (3), by the [[adjoint functor theorem]].  (5) is a special case of (2), of course.



### Compatibly monoidal cocomplete categories
 {#MonoidalCompleteCateories}


In ([Baez-Dolan](#BaezDolan)) a _2-rig_ is defined to be a [[monoidal category|monoidal]] [[colimit|cocomplete category]] where the monoidal product distributes over colimits.   We can define [[braided monoidal category|braided]] and [[symmetric monoidal category|symmetric]] 2-rigs in this sense (and indeed, also in the other senses listed above).  In particular, there is a 2-category $\mathbf{Symm2Rig}$ with:

* symmetric monoidal cocomplete categories where the monoidal product distributes over colimits as objects,

* symmetric monoidal cocontinuous functors as 1-morphisms,

* symmetric monoidal natural transformations as 2-morphisms.

This leads to the following:

+-- {: .un_thm}
###### Conjecture ([[John Baez]])
The initial symmetric 2-rig is $Set$, in a suitably weakened sense.  Namely, if $R$ is any object of $\mathbf{Symm2Rig}$, then there is a 1-morphism $Set \to R$ that is unique up to a 2-isomorphism.  

Furthermore, the free symmetric 2-rig on one object is the category of [[species]], $\widehat{\mathbb{P}}$ --- that is, the category of presheaves on the groupoid of finite sets and bijections, $\mathbb{P}$.  This symmetric 2-rig is free on the object $X$ which is the presheaf sending the one-element set to the one-element set, and every other set to the empty set.  

More precisely: if $R$ is any symmetric 2-rig and $x \in R$, there exists a 1-morphism $F: \widehat{\mathbb{P}} \to R$ with $F(X) = x$, and $F$ is unique up to a 2-isomorphism.
=--

### Compatibly monoidal presentable categories
 {#CompatiblyMonoidalPresentableCategories}

The following refines the [above](#MonoidalCompleteCateories) by demanding the underlying category of a 2-ring to be not just cocomplet but even a [[presentable category]]. This was motivated in ([CJF, remark 2.1.10](#CJF)).

+-- {: .num_defn}
###### Definition

Write 

$$
  2 Ab \in 2Cat
$$ 

for the [[2-category]] of [[presentable categories]] and [[colimit]]-preserving [[functors]] between them.

=--

([CJF, def. 2.1.8](#CJF))

+-- {: .num_remark}
###### Remark

By the [[adjoint functor theorem]] this is equivalently the 2-category of presentable categories and [[left adjoint]] functors between them.

=--

+-- {: .num_example #CategoryOfModulesAs2AbelianGroup}
###### Example

Given an ordinary [[ring]] $R$, its [[category of modules]] $Mod_R$ is presentable, hence may be regarded as a 2-abelian group.


=--

([CJF, example 2.1.5](#CJF))

+-- {: .num_prop}
###### Proposition

The 2-category $2Ab$ is a [[closed monoidal 2-category|closed]] [[symmetric monoidal 2-category]] with respect to the [[tensor product]] $\boxtimes \colon 2Ab \times 2Ab \to 2Ab$ such that for $A,B, C \in 2Ab$, $Hom_{2Ab}(A \boxtimes B, C)$ is equivalently the full [[subcategory]] of [[functor category]] $Hom_{Cat}(A \times B, C)$ on those that are [[bilinear function|bilinear]] in that they preserve [[colimits]] in each argument separately.

=--

See also at [[Pr(∞,1)Cat]] for more on this.

+-- {: .num_example }
###### Example

For $\mathcal{C}$ a [[small category]], the [[category of presheaves]] $Set^{\mathcal{C}}$ is [[presentable category|presentable]] and 

$$
  Set^{\mathcal{C}_1} \boxtimes
  Set^{\mathcal{C}_2}
  \simeq
  Set^{\mathcal{C}_1 \times \mathcal{C}_2}
  \,.
$$

=--

+-- {: .num_example #TensorProductModuleCategoriesAsOf2AbelianGroups}
###### Example

For $R$ a [[ring]] the [[category of modules]] $Mod_R$ is presentable and 

$$
  Mod_{R_1} \boxtimes Mod_{R_2} 
  \simeq
  Mod_{R_1 \otimes R_2}
  \,,
$$

=--

([CJF, example 2.2.7](#CJF))

+-- {: .num_prop #EilenbergWattsTheorem}
###### Proposition

For $R_1, R_2$ two rings,
the category  of 2-abelian group homomorphisms between the [[categories of modules]] is [[natural equivalence|naturally equivalent]] to that of $R_1$-$R_2$-[[bimodules]] and their [[intertwiners]]:

$$
  (-)\otimes (-)
  \;\colon\;
  {}_{R_1}Mod_{R_2}
  \stackrel{\simeq}{\to}  
  Hom_{2Ab}(Mod_{R_1}, Mod_{R_2})
  \,.
$$

The equivalence sends a bimdoule $N$ to the functor given by the [[tensor product]] over $R_1$:

$$
  (-) \otimes N \;\colon\;
  Mod_{R_1} \to Mod_{R_2}
  \,.
$$

=--

This is the [[Eilenberg-Watts theorem]]. 

  
+-- {: .num_defn #2RingAsCompatiblyMonoidalPresentableCategory}
###### Definition

Write

$$
  2Ring \in 2Cat
$$

for the [[2-category]] of [[monoid objects]] [[internalization|internal]] to $2 Ab$. An [[object]] of this 2-category we call a **2-ring**.

Equivalently, a 2-ring in this sense is a [[presentable category]] equipped with the structure of a [[monoidal category]] where the [[tensor product]] preserves [[colimits]]. 

=--

([CJF, def. 2.1.8](#CJF))


+-- {: .num_example}
###### Example

The category [[Set]] with its [[cartesian product]] is a 2-ring and it is the [[initial object]] in $2Ring$.

=--

([CJF, example 2.3.4](#CJF))

+-- {: .num_example}
###### Example

The category [[Ab]] of [[abelian groups]] with its standard [[tensor product of abelian groups]] is a 2-ring. 

=--

+-- {: .num_example #CommutativeRingGivesCommutative2Ring}
###### Example

For $R$ an ordinary [[commutative ring]], $Mod_R$ equipped with its usual [[tensor product of modules]] is a commutative 2-ring.

=--

+-- {: .num_example}
###### Example

For $R$ an ordinary [[ring]] and $Mod_R$ its ordinary [[category of modules]], regarded as a 2-abelian group by example \ref{CategoryOfModulesAs2AbelianGroup}, the structure of a 2-ring on $Mod_R$ is equivalently the structure of a [[sesquiunital sesquialgebra]] on $R$.

If $R$ is in addition a [[commutative ring]] that $Mod_R$ is a commutative 2-ring and is canonically an $Ab$-[[2-algebra]] in that 

$$
  Ab \simeq Mod_{\mathbb{Z}} \to Mod_R
  \,.
$$

=--

([CJF, example 2.3.7](#CJF))

+-- {: .num_defn}
###### Definition

For $A$ a 2-ring, def. \ref{2RingAsCompatiblyMonoidalPresentableCategory}, write

$$
  2Mod_A \in 2Cat
$$

for the [[2-category]] of [[module objects]] over $A$ in $2Ab$. 

This means that a 2-module over $A$ is a [[presentable category]] $N$ equipped with a functor

$$
  A \boxtimes N \to N
$$

which satisfies the evident action property.

=--

([CJF, def. 2.3.3](#CJF))

+-- {: .num_example}
###### Example

Let $R$ be an ordinary [[commutative ring]] and $A$ an ordinary $R$-[[associative algebra|algebra]]. Then by example \ref{CategoryOfModulesAs2AbelianGroup} $Mod_A$ is a 2-abelian group and by example
\ref{CommutativeRingGivesCommutative2Ring} $Mod_R$ is a commutative ring. By example \ref{TensorProductModuleCategoriesAsOf2AbelianGroups} 
$Mod_R$-[[2-module]] structures on $Mod_A$

$$
  Mod_R \boxtimes \Mod_A \to Mod_A
$$

correspond to colimit-preserving functors 

$$
  Mod_{R \otimes_{\mathbb{Z}} A} \to Mod_{A}
$$

that satisfy the action property. Such as presented under the [[Eilenberg-Watts theorem]], prop. \ref{EilenbergWattsTheorem}, by $R \otimes_{\mathbb{Z}} A$-$A$ [[bimodules]]. $A$ itself is canonically such a bimodule and it exhibits a $Mod_R$-[[2-module]] structure on $Mod_A$.

=--


## Properties

### Tannaka duality
 {#TannakaDuality}

[[!include structure on algebras and their module categories - table]]

## Related concepts

* A further slight variant of compatibly monoidal cocomplete categories is that of _monoidal [[vectoids]]_.

* [[distributivity for monoidal structures]]

## References

The proposal that a 2-ring should be a compatibly monoidal cocomplete category is due to

* [[John Baez]], [[James Dolan]], _Higher-dimensional algebra III: $n$-categories and the algebra of opetopes_, _Adv. Math._ **135** (1998), 145-206.  ([arXiv](http://arxiv.org/abs/q-alg/9702014))
 {#BaezDolan}

The proposal that a 2-ring should be a compatibly monoidal presentable category is due to

* [[Alexandru Chirvasitu]], [[Theo Johnson-Freyd]], _The fundamental pro-groupoid of an affine 2-scheme_ ([arXiv:1105.3104](http://arxiv.org/abs/1105.3104))
 {#CJF}

This is related to 

* [[Jacob Lurie]], _[[Tannaka duality for geometric stacks]]_.

A similar notion is that of "monoidal [[vectoid]]" due to

* [[Nikolai Durov]], _Classifying vectoids and generalisations of operads_, Proc. of Steklov Inst. of Math. __273__:1, 48-63 (2011) [arxiv/1105.3114](http://arxiv.org/abs/1105.3114)), the translation of "&#1050;&#1083;&#1072;&#1089;&#1089;&#1080;&#1092;&#1080;&#1094;&#1080;&#1088;&#1091;&#1102;&#1097;&#1080;&#1077; &#1074;&#1077;&#1082;&#1090;&#1086;&#1080;&#1076;&#1099; &#1080; &#1082;&#1083;&#1072;&#1089;&#1089;&#1099; &#1086;&#1087;&#1077;&#1088;&#1072;&#1076;", Trudy MIAN, vol. 273

The role of presentable categories as higher analogs abelian groups in the context of [[(infinity,1)-categories]] have been made by [[Jacob Lurie]],  see at _[[Pr(infinity,1)Cat]]_.

Another, more algebraic, notion of a categorical ring is introduced in

* M. Jibladze , T. Pirashvili, _Third Mac Lane cohomology via categorical rings_, 	J. of homotopy and related structures, __2__(2), 2007, 187&#8211;221 [pdf](http://www.emis.de/journals/JHRS/volumes/2007/n2a10/v2n2a10.pdf) [math.KT/0608519](http://arxiv.org/abs/math/0608519)

[[!redirects 2-rig]]
[[!redirects 2-rigs]]
[[!redirects 2-ring]]
[[!redirects 2-rings]]
