
This is a sub-entry of _[[geometry of physics]]_. See there for background and context.

***

#Contents#
* table of contents
{:toc}

## **Modules**

In the [previous section](geometry+of+physics#AssociatedNBundle) we have seen [[∞-actions]] of [[∞-groups]] on objects in the ambient [[(∞,1)-topos]]. Here we specialize this to an important class of cases and then generalize from [[∞-actions]] to $(\infty,n)$-actions for $n \in \mathbb{N}$. That special case is the one where all objects involved are required to be equipped with _additive structure_ (in generalization of the sense of [[abelian groups]] are) and where all actions are _linear_ (in generalization of the sense of abelian group [[homomorphisms]] hence  [[linear functions]]). Moreover, we equip groups with additional (linear) monoidal structure such as to become higher analogs of [[rings]]. Linear [[actions]] of a [[ring]] are called _[[modules]]_ and hence here we discuss modules and their higher analogs.

A special case of modules are [[vector spaces]], which are the modules over a [[ring]] that is a [[field]]. For them the theory of modules is the theory of [[linear algebra]]. But as opposed to the notion of _[[ring]]_, the more specialized notion of _[[field]]_ has in general no natural or useful lift to [[higher category theory]]. Therefore we generally speak here of modules over rings and their higher analogs. But the reader who feels more at home with vector spaces may find it helpful to think of higher modules as being higher analogs of vector spaces.

### 1-Modules

#### Physics motivation: Phases and superposition of states

In [[quantum mechanics]]

* [[superposition principle]] says: [[quantum states]] form an additive [[abelian group]];

* complex phases means: [[quantum states]] are acted on by [[complex numbers]].

Together: [[space of quantum states]] is a $\mathbb{C}$-[[module]] = $\mathbb{C}$-[[vector space]].

#### Modules

#### Vector bundles


### $(\infty,n)$-Modules

#### Physics motivation: Higher order states in extended QFT

There two key classes of examples of [[(∞,n)-categories]] of relevance in [[physics]]. One is clearly the [[(∞,n)-categories of cobordisms]] $Bord_n^S$ (with some specified extra structure $S$) which by the theory of [[extended quantum field theory]] are the [[domain]] of [[monoidal (∞,n)-functors]]

$$
  Z \;\colon\; Bord_n^S \to \mathcal{C}
  \,.
$$

In the abstract mathematical discussion the [[codomain]] $\mathcal{C}$ here is usually allowed to be any [[symmetric monoidal (∞,n)-category]]. But we expect that for those quantum field theories of actual relevance in [[physics]] (notably those obtained by [[quantization]] from [[extended prequantum field theories]]) the [[codomain]] here is special. Notably in [[codimension]] 1 for $\Sigma_{n-1}$ a [[closed manifold]] of [[dimension]] $n-1$ the value $Z(\Sigma_{n-1})$ should be the [[space of quantum states]] over $\Sigma_{n-1}$ and thus be a _$\mathbb{C}$-[[module]]_ (a complex [[vector space]]) possibly with some extra properties and structure (e.g. a [[topological vector space]], a [[Hilbert space]], etc., depending on the precise details).

Therefore we expect that for relevant [[theory (physics)|theories of physics]] in [[dimension]] $n$, $\mathcal{C}$ is something that deserves to be called an _[[(∞,n)-category]] of [[(∞,n)-modules]]_ (maybe: [[(∞,n)-vector spaces]])

$$
  \mathcal{C}
  \simeq
  n Mod_{R}
$$

over some base [[E-∞ ring]] $R$.

Here we discuss such $n$-modules.

#### 2-Abelian groups

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

#### 2-Rings 

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
#### 2-Modules

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

+-- {: .num_example #2ModulesOverThe2RingOfAnOrdinaryRing}
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

##### Bases for 2-modules: Tannaka duality for associative algebras
 {#BasesFor2ModulesAndTannakaDualityForAssociativeAlgebras}

The construction in example \ref{2ModulesOverThe2RingOfAnOrdinaryRing}
of 2-modules over the 2-ring induced by an ordinary commutative ring $R$ as categories of 1-modules over some $R$-algebra may be understood as presenting a 2-[[free module]] by a 2-[[basis]].

To see this, write

$$
  \mathcal{V} \coloneqq Mod_R
$$

for the [[closed monoidal category|closed]] [[symmetric monoidal category|symmetric monoidal]] [[category of modules]] and regard it as an [[cosmos|enriching context]] for $\mathcal{V}$-[[enriched category theory]]. 

Then we claim that a $\mathcal{V}$-[[enriched category]] $\mathcal{A}$ serves as a [[basis]]. Notice that an $R$-algebra $A$ is equivalently a (pointed) $\mathcal{V}$-enriched category $\mathcal{A} = \mathbf{B}A$ with a single object (the [[delooping]] of $A$). Generally, $\mathcal{A}$ may be called  _$R$-[[algebroid]]_.

Since [[colimits]] in the category underlying a [[2-abelian group]] [[categorification|categorify]] the sum operation in an [[abelian group]] the 2-analog of the free module on a [[basis]] [[set]] is the [[free cocompletion]] of $\mathcal{A}$ as a $\mathcal{V}$-[[enriched category]]. This is the $\mathcal{V}$-[[presheaf category]], hence the [[enriched functor category]]

$$
  [\mathcal{A}, \mathcal{V}]
  \in 
  \mathcal{V}Cat
  \,.
$$

Compare this to how for a (finite dimensional) vector space a presentation by a basis is a set $B$ such that the vector space is

$$
 Maps(B,k)
  \in 
  Vect_k
$$

Indeed, for $\mathcal{A} = \mathbf{B}A$ this is the ordinary [[category of modules]] over $A$:

$$
  [\mathbf{B}A, \mathcal{V}]
  \simeq
  Mod_A
  \,.
$$

In fact in [[enriched category theory]] it is customary generally to call $\mathcal{V}$-[[enriched functors]] into $\mathcal{V}$ "[[modules]]" (see there).

Without further assumoptions on $\mathcal{A}$, the category $[\mathcal{A}, \mathcal{V}]$ is just a $\mathcal{V}$-[[2-module]]. But if $\mathcal{A}$ is equipped with further [[extra structure]] and/or [[property]], also $[\mathcal{A}, \mathcal{V}]$ inherits further property. This relation between types of algebras and types of monoidal categories is known as _[[Tannaka duality]]_.

The following table lists the main items of the disctionary of Tannaka duality for associtive algebras that are used in the literature. 

[[!include structure on algebras and their module categories - table]]

##### Matrix calculus for 2-modules: Bimodules and Eilenberg-Watts theorem

If a $\mathcal{V} \coloneqq Mod_R$-[[enriched category]] serves as a 2-[[basis]] for a $Mod_R$-[[2-module]] by the [above](#BasesFor2ModulesAndTannakaDualityForAssociativeAlgebras) discussion, there should be an analog of [[matrix calculus]] to present 2-linear maps between [[2-modules]] equipped with such a 2-basis.

Such a higher [[matrix]] is what in [[enriched category theory]] is called a _$\mathcal{V}$-[[profunctor]]_ (or "[[distributor]]"): a profunctor between $\mathcal{V}$-enriched categories $\mathcal{A}_1, \mathcal{A}_2 \in \mathcal{V}Cat$ is a $\mathcal{V}$-[[enriched functor]]

$$
  K
  \;\colon\;
  \mathcal{A}_1^{op}
  \times
  \mathcal{A}_2
  \to
  \mathcal{V}
  \,.
$$

Compare this to how a matric between two vector spaces equipped with basis sets $B_1, B_2$ is a function

$$
  K \colon B_1 \times B_2 \to k
$$

to the [[ground field]]. Notice that if the vector space is given by $[B_1,k]$, then the action of this matrix on a vector $v \colon B_1 \to k$ is given by the vector $K v \colon B_2 \to k$

$$
  b_2 \mapsto \sum_{b_1 \in B_1} v(b_1) \cdot K(b_1,b_2)
  \,.
$$

If we replace in this formula the sum by a [[coend]], then we get the action of the [[profunctor]] $K$ on a $\mathcal{V}$-functor $v \colon \mathcal{A}_1 \to \mathcal{V}$ to yield $K \otimes v \colon \mathcal{A}_2 \to \mathcal{V}$ with

$$
  a_2 \mapsto \int^{a_1 \in A_1} v(a_1) \otimes K(a_1, a_2)
  \,.
$$ 


* [[bimodule]]

* [[Eilenberg-Watts theorem]]

#### 2-Module bundle

* [[2-module bundle]]

#### 2-Lines

* [[2-line]]

##### Classification: Azumaya algebras, Brauer group, Picard group

* [[Picard 3-group]]

  * [[Brauer group]], [[Picard group]], [[group of units]]

##### 2-Line bundles and their sections: twisted K-theory

* [[2-line bundle]]

* [[twisted bundle]] / [[Chan-Paton gauge field]] / [[twisted K-theory]]


#### $(\infty,2)$-Abelian groups

* [[∞-bimodule]]

#### $(\infty,2)$-rings

* [[(∞,2)-ring]]

#### $(\infty,2)$-modules

* [[(∞,2)-module]]


## References

* [[Alexandru Chirvasitu]], [[Theo Johnson-Freyd]], _The fundamental pro-groupoid of an affine 2-scheme_ ([arXiv:1105.3104](http://arxiv.org/abs/1105.3104))
 {#CJF}
