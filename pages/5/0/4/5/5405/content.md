
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Under mild conditions, a given [[site]] $C \subset T Alg^{op}$ of formal duals of [[algebra over a Lawvere theory|algebras over an algebraic theory]] admits [[Isbell duality]] exhibited by an [[adjunction]]

$$
  (\mathcal{O} \dashv Spec) : (T Alg^{\Delta})^{op} \stackrel{\overset{\mathcal{O}}{\leftarrow}}{\underset{Spec}{\to}}
  Sh_{(\infty,1)}(C)
$$

as described at [[function algebras on ∞-stacks]] Here $\mathcal{O}(X)$ is an $(\infty,1)$-algebra of functions on $X$.

This entry describes for certain [[algebraic stacks]] an analog of this situation where the 1-algebras are replaced by 2-algebras in the form of commutative algebra objects in the [[2-category]] of [[abelian categories]]: abelian [[symmetric monoidal categories]], and where the function algebras $\mathcal{O}(X)$ are replaced with category $QC(X)$ of [[quasicoherent sheaves]].

The replacement of the 1-algebra $\mathcal{O}(X)$ by the 2-algebra $QC(X)$ is the starting point for what is called [[derived noncommutative geometry]].

## Setup

### Ringed toposes

All [[topos]]es that we consider are [[Grothendieck topos]]es. A [[ringed topos]] $(S, \mathcal{O}_S)$ is a topos $S$ equipped with a ring object $\mathcal{O}_S$ -- a [[sheaf]] of rings -- called the [[structure sheaf]] -- on whatever [[site]] $S$ is the [[category of sheaves]] on. We write $\mathcal{O}_S Mod$ for the category of [[module]]s in $S$ (sheaves of modules) over $\mathcal{O}_S$.

We write $RngdTopos$ for the category of ringed toposes.

For $X$ a [[scheme]] or more generally an [[algebraic stack]], write $Sh(X_{et})$ for its [[little etale topos]].

+-- {: .un_def #localWRTEtaleTopology}
###### Definition

A ringed topos $(S,\mathcal{O}_S)$ is a **[[locally ringed topos]]** with respect to the [[étale topology]] if for every object $U \in S$ and every family $\{Spec R_i \to Spec \mathcal{O}_S(U)\}$ of [[étale morphism]]s such that 

$$
  \mathcal{O}_S(U) \to \prod_i R_i
$$

is [[faithfully flat]], there exists morphisms $E_i \to E$ in $S$ and factorizations $\mathcal{O}_S(U) \to R_i \to  \mathcal{O}_S(E_i)$ such that 

$$
  \coprod_i E_i \to E
$$

is an [[epimorphism]].

=--

+-- {: .un_prop}
###### Proposition

If $S$ has [[point of a topos|enough points]] then $(S, \mathcal{O}_S)$ is local for the &#233;tale topology precisely if the [[stalk]] $\mathcal{O}_S(x)$ at every [[point of a topos|point]] $x : Set \to S$ is a strictly [[Henselian ring|Henselian]] [[local ring]].  

=--

This is ([Lurie, remark 4.4](#Lurie)).


+-- {: .un_prop}
###### Example

* The [[little étale topos]] $Sh(X_{et})$ of a [[Deligne-Mumford stack]] $X$ is locally ringed with respect to the &#233;tale topology.

=--




### Abelian tensor categories


+-- {: .un_def #AbelianTensorCategory}
###### Definition

An **abelian tensor category** (for the purposes of the present discusission) is a [[symmetric monoidal category]] $(C, \otimes)$ such that

* $C$ is an [[abelian category]];

* for every $x \in C$ the functor $(-) \otimes x : C\to C$ is additive and right-[[exact functor|exact]]: it commutes with finite [[colimit]]s.

A **complete abelian tensor category** is an abelian tensor category such that 

* it satisfies the axiom AB5 at [[additive and abelian categories]];

* $(-) \otimes x$ commutes with _all small_ colimits.

  (equivalently, we have a  [[closed monoidal category]]).

An abelian tensor category is called **tame** if for any [[short exact sequence]]

$$
  0 \to M'\to M \to M''\to 0
$$

with $M''$ a _flat object_ (such that $x \mapsto x \otimes M''$ is an [[exact functor]]) and any $N \in C$ also the induced sequence

$$
  0 \to M'\otimes N \to M\otimes N \to M''\otimes N \to 0
$$

is exact.

=--

This appears as ([Lurie, def. 5.2](#Lurie)) together with the paragraph below remark 5.3.


+-- {: .un_def #TCAbTens}
###### Definition

For $C,D$ two [complete abelian tensor categories](#AbelianTensorCategory) write

$$
  Func_\otimes(C,D) \subset Func(C,D)
$$

for the [[core]] of the [[subcategory]] of the [[functor category]] on those [[functor]]s that 

* are [[symmetric monoidal functor]]s;

* commute with all small [[colimit]]s (which implies they are [[additive functor|additive]] and [[exact functor|right exact]]) 

* preserve flat objects and short exact sequences whose last object is flat.

Write

$$
  TCAbTens
$$

for the ([[strict 2-category|strict]]) [[(2,1)-category]] of [tame complete abelian tensor categories](#AbelianTensorCategory) with hom-[[groupoid]]s given by this $Func_\otimes$.

=--

This appears as ([Lurie, def 5.9](#Lurie)) together with the following remarks.



+-- {: .un_lemma}
###### Example

For $k$ a [[ring]], write $k Mod$ for its [[abelian category|abelian]] [[symmetric monoidal category]] of [[module]]s

Let $(S,\mathcal{O}_S)$ be a [[ringed topos]]. Then 

$$
  \mathcal{O}_S Mod
$$ 

(the category of sheaves of $\mathcal{O}_S$-[[module]]s) is a tame [complete abelian tensor category](#AbelianTensorCategory).  

=--

This is ([Lurie, example 5.7](#Lurie)).


+-- {: .un_lemma}
###### Example


For $X$ an [[algebraic stack]], write 

$$
  QC(X)
$$ 

for its category [[quasicoherent sheaves]].

This is a [complete abelian tensor category](#AbelianTensorCategory)

=--

+-- {: .un_lemma}
###### Lemma

If $X$ is a Noetherian geometric stack, then $QC(X)$ is the category of [[ind-object]]s of its full [[subcategory]] $Coh(X) \subset QC(X)$ of [[coherent sheaves]]

$$
  QC(X) \simeq Ind(Coh(X))
  \,.
$$

=--

This appears as ([Lurie, lemma 3.9](#Lurie)).


### Geometric stacks {#GeometricStack}

+-- {: .un_def #geometricStack}
###### Definition


A **[[geometric stack]]** is

* an [[algebraic stack]] $X$ over $Spec \mathbb{Z}$

* that is quasi-compact, in particular there is an [[epimorphism]] $Spec A \to X$;

* with affine and [[representable morphism of stacks|representable]] diagonal $X \to X \times X$.

=--

+-- {: .un_prop}
###### Example

* A quasicompact [[separated scheme]] is a geometric stack.

* The classifying stack of a [[smooth scheme|smooth]] affine [[group object|group]] [[scheme]] is a geometric stack.

=--

The geometricity condition on an algebraic stack implies that there are "enough" [[quasicoherent sheaves]] on it, as formalized by the following statement.

+-- {: .un_theorem}
###### Theorem

If $X$ is a [geometric stack](#geometricStack) then the [[bounded chain complex|bounded-below]] [[derived category]] of [[quasicoherent sheaves]] on $X$ is naturally [[equivalence of categories|equivalent]] to the full [[subcategory]] of the left-bounded derived category of smooth-[[etale site|etale]] $\mathcal{O}_X$-modules whose [[chain cohomology]] sheaves are quasicoherent.

=--
 
This is ([Lurie, theorem 3.8](#Lurie)).


## Tannaka duality for geometric stacks

+-- {: .un_theorem}
###### Theorem

Let $X$ be a [geometric stack](#GeometricStack).

Then for every ring $A$ there is an [[equivalence of categories]]

$$
  RngdTopos(Sh((Spec A)_{et}),Sh(X_{et})) \simeq Hom_\otimes(QC(X), A Mod)
$$

hence (by the [[2-Yoneda lemma]])

$$
  X(Spec A) \simeq Hom_\otimes(QC(X), QC(Spec A))
  \,.
$$


More generally, for $(S, \mathcal{O}_S)$ any [etale-locally](#localWRTEtaleTopology) [[ringed topos]], we have

$$
  RngdTopos(S,Sh(X_{et})) \simeq Hom_\otimes(QC(X), \mathcal{O}_S Mod)
  \,.
$$


=--

This is ([Lurie, theorem 5.11](#Lurie)) in view of ([Lurie, remark 4.5](#Lurie)).


+-- {: .un_remark}
###### Remark

It follows that forming [[quasicoherent sheaves]]  constitutes a [[full and faithful (infinity,1)-functor|full and faithful (2,1)-functor]] 

$$
  QC : GeomStacks \to TCAbTens^{op}
$$

from geometric stacks to [tame complete abelian tensor categories](#TCAbTens).

This statement justifies thinking of $QC(X)$ as being the "2-algebra" of functions on $X$. This perspective is the basis for [[derived noncommutative geometry]].

=--

## Related concepts

* [[analytification]]

* [[2-algebraic geometry]]

* [[spectrum of a tensor triangulated category]]

* [[prime spectrum of a symmetric monoidal stable (∞,1)-category]]

* [[Tannaka duality for Lie groupoids]]

* [[Bondal-Orlov reconstruction theorem]]

* [[2-ring]]

## References

The above material is taken from

* {#Lurie} [[Jacob Lurie]], _Tannaka duality for geometric stacks_, ([arXiv:math.AG/0412266](http://arxiv.org/abs/math/0412266))


The generalization to geometric stacks in the context of [[Spectral Schemes]] is in 

* [[Jacob Lurie]], _[[Quasi-Coherent Sheaves and Tannaka Duality Theorems]]_

Related discussion is in 

* [[Martin Brandenburg]], [[Alexandru Chirvasitu]], _Tensor functors between categories of quasi-coherent sheaves_ ([arXiv:abs/1202.5147](http://arxiv.org/abs/1202.5147))

