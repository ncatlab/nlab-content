
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

as descrived at [[function algebras on ∞-stacks]] Here $\mathcal{O}(X)$ is an $(\infty,1)$-algebra of functions on $X$.

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




### Abelian symmetric monoidal categories

+-- {: .un_def}
###### Definition

For $C,D$ two [[symmetric monoidal category|symmetric monoidal]] [[abelian categories]], write

$$
  Func_\otimes(C,D) \subset Func(C,D)
$$

for the [[core]] of the [[subcategory]] of the [[functor category]] on those [[functor]]s that are 

* [[symmetric monoidal functor]]s;

* [[additive functor]]s;

* [[exact functor]];

* preserve flat objects.

=--

+-- {: .un_def}
###### Definition


* For $k$ a [[ring]], write $k Mod$ for its [[abelian category|abelian]] [[symmetric monoidal category]] of [[module]]s

* For $X$ an [[algebraic stack]], write $QC(X)$ for its [[abelian category|abelian]] [[symmetric monoidal category]] of [[quasicoherent sheaves]].

=--

### Geometric stacks {#GeometricStack}

+-- {: .un_def #geometricStack}
###### Definition


A **geometric stack** is

*an [[algebraic stack]] $X$ over $Spec \mathbb{Z}$

* that is quasi-compact, in particular there is an [[epimorphism]] $Spec A \to X$;

* with affine and representable diagonal $X \to X \times X$.

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

This ([Lurie, theorem 5.11](#Lurie)) in view of ([Lurie, remark 4.5](#Lurie)).


+-- {: .un_remark}
###### Remark

This statement justifies thinking of $QC(X)$ as being the "2-algebra" of functions on $X$. This perspective is the basis for [[derived noncommutative geometry]].

=--


## References

* [[Jacob Lurie]], _Tannaka duality for geometric stacks_, ([arXiv:math.AG/0412266](http://arxiv.org/abs/math/0412266))
{#Lurie}
