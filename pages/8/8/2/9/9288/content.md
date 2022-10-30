
This is a sub-entry of _[[geometry of physics]]_. See there for background and context.

***

#Contents#
* table of contents
{:toc}

## **Modules**

In the [previous section](geometry+of+physics#AssociatedNBundle) we have seen [[∞-actions]] of [[∞-groups]] on objects in the ambient [[(∞,1)-topos]]. Here we specialize this to an important class of cases and then generalize from [[∞-actions]] to $(\infty,n)$-actions for $n \in \mathbb{N}$. That special case is the one where all objects involved are required to be equipped with _additive structure_ (in generalization of the sense in which [[abelian groups]] are additive) and where all actions are _linear_ (in generalization of the sense of abelian group [[homomorphisms]], hence  [[linear functions]]). Moreover, we equip groups with additional (linear) monoidal structure such as to become higher analogs of [[rings]]. Linear [[actions]] of a [[ring]] are called _[[modules]]_ and hence here we discuss modules and their higher analogs.

Notice the different role of the "$(r,n)$" index:
| $(r,n)$-ring | presentation  |
|--|--|
| [[ring]] = 1-ring = $(1,1)$-ring |  compatibly monoidal [[abelian group]] |
| [[2-ring]] = $(2,2)$-ring | compatibly [[monoidal category]] |
| commutative $(\infty,1)$-ring  | [[E-∞ ring]] = compatibly monoidal [[∞-group]] / [[spectrum]] | 
| $(\infty,2)$-ring | compatibly [[monoidal (∞,1)-category]]

A special case of modules are [[vector spaces]], which are the modules over a [[ring]] that is a [[field]]. For them the theory of modules is the theory of [[linear algebra]]. But as opposed to the notion of _[[ring]]_, the more specialized notion of _[[field]]_ has in general no natural or useful lift to [[higher category theory]]. Therefore we generally speak here of modules over rings and their higher analogs. But the reader who feels more at home with vector spaces may find it helpful to think of higher modules as being higher analogs of vector spaces.

### 1-Modules

We briefly disucss here some basics of ordinary [[linear algebra]] with an emphasis on the generalization from [[vector spaces]] over [[fields]] to [[modules]] over [[rings]].

#### Physics motivation: Superposition of states and fields

One key aspect of [[quantum mechanics]], that distribuishes it from [[classical mechanics]], is that there is _linear structure_ on [[quantum states]], as follows (the following applies to quantum states in the [[Schrödinger picture]] only, not to states in the sense of [[state on an operator algebra]], which are really the [[expectation values]] of [[observables]] in the states as discussed here):

* The **[[superposition principle]]** in quantum mechanics says that for $\psi_1$ and $\psi_2$ two [[quantum states]] one can form their [[sum]] $\psi_1 + \psi_2$ as well as their difference $\psi_1 - \psi_2$ such that this is again a quantum state. Moreover there is a 0-state such that $\psi + 0 = \psi$ for all $\psi$. Together this means there is the structure of an additive [[abelian group]] on the set of quantum states.

* Quantum states have **complex phases**. This means that for $\psi$ a quantum state and for $c \in \mathbb{C}$ a [[complex number]], there is a new quantum state $c \psi$ and this is such that for two such complex numbers we have  $c_1(c_2 \psi) = (c_1 c_2) \psi$ and for two states we have $c(\psi_1 + \psi_2) = c \psi_1 + c \psi_2$.  This means that multiplying by phases is a linear [[action]] of the [[ring]] of [[complex numbers]] on quantum states.

Together this says equivalently that the additive group of quantum states is a _[[module]]_ over the [[complex numbers]]. Since the ring of complex numbers is special in that it is a [[field]], such a module is equivalently called a _[[complex vector space]]_.

This linear structure is a crucial aspect of quanum theory. It is at the heart of phenomena such [[quantum interference]] and [[entanglement]]

In macroscopic physics similar behaviour is known in [[wave mechanics]] for freely propagating waves. Not unrelated to this is the term _[[wave function]]_ for a quantum state. However, apart from wave mechanics, linearity is not manifest in macoscopic physical phenomena, even though it is fundamentally present; this is called _[[decoherence]]_.

It is this linear structure of quantum theory that, since shortly after its conception, led to a close relaton to [[group]] [[representation theory]] which was unknown in classical physics. (And this came unexpected to physicist at the beginning of the 20th century and was not embraced by all theoreticians at first, see at _[[Gruppenpest]]_.) If a [[symmetry group]] acts on [[field (physics)|field configurations]] of a [[physical system]] and is preserved by [[quantization]], then it still acts on the quantum states and does so in a linear way; hence then the [[space of quantum states]] forms a [[linear representation]] space of the [[symmetry group]]. This relation between quantum mechanical systems with symmetry and linear [[representation theory]] goes so far that under natural assumptions _every_ representation of a group arises as the action of a group of symmetries on a quantum system  -- a relation known as the "[[orbit method]]" in [[geometric quantization]]. Deep results about abstract linear [[representation theory]] have been proven by considering systems [[quantum mechanics]] this way.

But the relation between quantum physics and linear representation theory goes deeper still. Not only do the quantum states form modules over the complex numbers, but already the [[matter]] [[field (physics)|fields]] in fundamental physics form modules over the [[algebra of functions]] on [[spacetime]]. This means in turn that matter fields form an additive [[abelian group]] where for $\phi_1$ and $\phi_2$ two field configurations also $\phi_1 + \phi_2$ is a field configuration, such that with $\phi$ a matter field for each [[smooth function]] $f$ on [[spacetime]] there is also a matter field denoted $f \phi$ and such that $f_1 (f_2 \phi) = (f_1 f_2) \phi$ and $f(\phi_1 + \phi_2) = f \phi_1 + \phi_2$.

There is a more geometric expression of this: in fact the matter fields form a module with special properties (they are what is called _[[projective module|projective]]_ and _[[finitely generated module|finitely generated]]_) and the [[Serre-Swan theorem]] asserty that modules with these special properties consist of [[sections]] of a [[fiber bundle]] whose typical fiber is a [[module]] over the [[complex numbers]], hence a [[complex vector space]]: a complex _[[vector bundle]]_. Moreover, these vector bundles are [[associated bundles]] via [[linear representations]] of the [[gauge group]] of the [[force]] [[field (physics)|fields]] under which the given matter fields are [[charged particle|charged]]. So in addition to being a linear module over the [[algebra of functions]] on [[spacetime]], matter fields also form a [[linear representation]] of the relevant [[gauge group]]. Finally all this combines with the [[symmetry group]] actions as for the quantum states themselves: is a group acts by symmetries on [[spacetime]] -- notably for instance the action of the [[Poincaré group]] on [[Minkowski spacetime]] -- then this translates into a [[linear representation]] of the group on the module of [[matter]] [[field (physics)|fields]], via [[pullback of functions]].  This goes as far as that under suitable conditions one can classify/identify [[particle]] species with [[unitary representation|unitary]] [[irreducible representations]] of the spacetime symmetry group, a relation known as _[[Wigner classification]]_, discussed in more detail at _[[unitary representation of the Poincaré group]]_. A closely related relation is the [[Doplicher-Roberts reconstruction theorem]] which shows that [[superselection sectors]] of a quantum field theory form the [[representation category]] of the global [[gauge group]] of a [[local net of observables]] of a quanutm field theory on spacetime -- a special case of the deep principle of [[Tannaka duality]] in [[representation theory]].

In summary this means that the relation between quantum theory and [[module]] theory/[[linear algebra]]/[[representation theory]] is intimate. 

#### Modules

* [[module]]

#### Vector bundles

* [[vector bundle]]


### $(\infty,n)$-Modules

We turn now to the discussion of the generalization of the notion of [[module]] in [[higher category theory]]. After a motivation from [[physics]]

* [Physics motivation: Higher order states in extended QFT](#PhysicsMotivationHigherOrderStatesInQFT)

we first discuss how the [[2-category]] (i.e. [[(n,r)-category|(2,2)-category]]) of [[2-modules]] and their 2-linear maps is presented by the classical 2-category of [[associative algebras]] with [[bimodules]] between them and [[intertwiners]] between those. 

* [2-Modules](#2Modules).

This serves as an instructive blueprint for all the following generalizations and is in itself a useful theory that neatly subsumes and organizes classical constructions and results such as [[Tannaka duality]] for associative algebras, the [[Eilenberg-Watts theorem]], and the basic [[Morita equivalence|Morita]] [[invariant theory]] of [[commutative rings]] given by [[Brauer group]], [[Picard group]] and [[group of units]].

Next we pass to [[homotopy theory]] proper and 
discuss the construction of the [[(∞,2)-category]] of [[A-∞ algebras]] and [[∞-bimodules]] internal to any compatibly cocomplete [[monoidal (∞,1)-category]]. 

* [(∞,2)-modules](#?2Modules).

By iterating this construction in analogy to the iterative construction of [[(∞,n)-categories]] as $n$-fold [[categories in an (∞,1)-category]], we obtain a notion of [[(∞,n)-modules]]

* [(∞,n)-modules](#?nModule)

#### Physics motivation: Higher order states in extended QFT
 {#PhysicsMotivationHigherOrderStatesInQFT}

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

An [[abelian group]] [[semigroup]] is a set equipped with a commutative  and hence "additive" and unital pairing. A natural [[categorification]] of addition is the [[coproduct]] operation in a category, hence more generally the operation of taking [[colimits]]. Hence a sensible categorification of the notion of additive semigroup is that of _[[category]] with all [[colimits]]_. But in the spirit of [[category theory]] we should not try just to categorify abelian semigroups, but rather the category that these form. The category [[Ab]] of [[abelian groups]] is notably a [[closed monoidal category|closed]] [[symmetric monoidal category]] and accordingly we demand that the [[2-category]] of 2-abelian semigroups to replace it is similarly a closed [[symmetric monoidal 2-category]]. This is achived by restricting attention among all categories with colimits to the _[[presentable categories]]_.
Moreover, since the [[homomorphisms]] of abelian groups are [[linear functions]], hence addition-respecting functions, so the 2-linear maps between these 2-abelian semigroups should be [[colimit]]-preserving [[functors]]. This way we arrive at the following definition.

+-- {: .num_defn #2Category2Ab}
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

+-- {: .num_example }
###### Example

Given a [[small category]] $\mathcal{C}$, the [[presheaf category]] $Set^{\mathcal{C}}$ is a [[presentable category]].

=--

+-- {: .num_remark }
###### Remark

Forming presheaves on $\mathcal{C}$ is the [[free cocompletion]] of $\mathcal{C}$. Under the interpretation of colimits as the categorification of additive sums, this means that $Set^{\mathcal{C}}$ is the 2-[[free abelian group]] generated by the "2-set" $\mathcal{C}$.

Moreover, every [[presentable category]] (as discussed there) is a [[reflective subcategory]] hence a left [[localization]] of a category of presheaves. This means that not every 2-abelian group is 2-free, but is possibly a localization of a 2-free abelian group.

=--

+-- {: .num_example #CategoryOfModulesAs2AbelianGroup}
###### Example

Given an ordinary [[ring]] $R$, its [[category of modules]] $Mod_R$ is presentable, hence may be regarded as a 2-abelian group.
This example we discuss in more detail below in _[Bases for 2-modules: Tannaka duality for associative algebras](BasesFor2ModulesAndTannakaDualityForAssociativeAlgebras)_.

=--

([CJF, example 2.1.5](#CJF))

+-- {: .num_remark }
###### Remark

These two examples are directly analogous from the perspective of [[enriched category theory]]. For $A$ an $R$-algebra write $\mathbf{B}A$ for the corresponding 1-object $Mod_R$-[[enriched category]] with $A$ as its $R$-module of morphisms. Then 

$$
  Mod_A \simeq [\mathbf{B}A, Mod_R]
$$

is the [[enriched functor category]].

Compare oth situation to how an ordinary [[free module]] $N$ (of finite [[rank]]) over a commutative [[ring]] is equivalently an [[algebra of functions]] 

$$
  N \simeq [B,R]
$$

for $B$ a [[basis]] [[set]].

=--

+-- {: .num_prop}
###### Proposition

The 2-category $2Ab = PrCat$ of def. \ref{2Category2Ab} is a [[closed monoidal 2-category|closed]] [[symmetric monoidal 2-category]] with respect to the [[tensor product]] $\boxtimes \colon 2Ab \times 2Ab \to 2Ab$ which corepresents "bi-2-linear" functors; in 
that for $A,B, C \in 2Ab$ the [[hom-category]] $Hom_{2Ab}(A \boxtimes B, C)$ is equivalently the full [[subcategory]] of the [[functor category]] $Hom_{Cat}(A \times B, C)$ on those that preserve [[colimits]] in each argument separately.

=--

See also at [[Pr(∞,1)Cat]] for more on this.

+-- {: .num_remark}
###### Remark

This is analous to the [[Deligne tensor product of abelian categories]].

=--

+-- {: .num_example #SetPresheafCategorisAs2AbelianGroups}
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

+-- {: .num_prop #TensorProductModuleCategoriesAsOf2AbelianGroups}
###### Proposition

For $R$ a [[ring]] the [[category of modules]] $Mod_R$ is presentable and 

$$
  Mod_{R_1} \boxtimes Mod_{R_2} 
  \simeq
  Mod_{R_1 \otimes R_2}
  \,,
$$

=--

([CJF, example 2.2.7](#CJF))

+-- {: .num_remark #SetsAsNonlinearModuleCategories}
###### Remark

As we discuss below 
in _[Bases for 2-modules: Tannaka duality for associative algebras](BasesFor2ModulesAndTannakaDualityForAssociativeAlgebras)_, a category of modules over an $R$-algebra is a [[presheaf category]] in $Mod_R$-[[enriched category theory]]. Notice that in this language a plain presheaf over a [[locally small category]] is a presheaf in [[Set]]-[[enriched category theory]].

Therefore comparison of 
example \ref{SetPresheafCategorisAs2AbelianGroups} with example \ref{TensorProductModuleCategoriesAsOf2AbelianGroups} shows that in the context of 2-abelian semigroups plain sets play a role of a "nonlinear generalization" of linear algebra. We see this in a more pronounced way once we have introduced the notion of [[2-modules]] [below](#2Modules). (It has become fashionable to speak of sets regarded as non-linear module categories as being modules over the "[[field with one element]]".)

=--


#### 2-Rings 

With the ambient [[monoidal 2-category]] $2Ab$ chosen, it is now straightforward to define [[2-rings]] as [[monoids]] [[internalization|internal]] to that.

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

+-- {: .num_prop}
###### Proposition

For $R$ an ordinary [[commutative ring]] and $Mod_R$ its ordinary [[category of modules]], regarded as a 2-abelian group by example \ref{CategoryOfModulesAs2AbelianGroup}, the structure of a 2-ring on $Mod_R$ is equivalently the structure of a [[sesquiunital sesquialgebra]] on $R$.

=--

+-- {: .proof}
###### Proof

By prop. \ref{TensorProductModuleCategoriesAsOf2AbelianGroups}, a 2-linear map

$$
  Mod_A \boxtimes Mod_A \to Mod_A
$$

is equivalently a 2-linear map

$$
  Mod_{A \otimes A} \to Mod_A
  \,.
$$

By the [[Eilenberg-Watts theorem]] (which we discuss in more detail as theorem \ref{EilenbergWattsTheorem} [below](#MatrixCaclulusFor2Modules)) this is equivalently an $A \otimes A$-$A$-[[bimodule]]. Similarly the unit map

$$
  Mod_R \to Mod_A
$$

is equivalently an $R$-$A$-bimodule.

=--

+-- {: .num_prop}
###### Proposition

For $R$ a [[commutative ring]], $Mod_R$ is a commutative 2-ring and is canonically an [[2-algebra]] over the [[2-ring]] $Ab$ in that we have a canonical 2-ring homomorphism

$$
  Ab \simeq Mod_{\mathbb{Z}} \to Mod_R
  \,.
$$

=--

([CJF, example 2.3.7](#CJF))

#### 2-Modules
 {#2Modules}

+-- {: .num_defn #2CategoryOf2Modules}
###### Definition

For $\mathcal{R}$ a 2-ring, def. \ref{2RingAsCompatiblyMonoidalPresentableCategory}, write

$$
  2Mod_{\mathcal{R}} \in 2Cat
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

+-- {: .num_remark}
###### Remark

Coming back to remark \ref{SetsAsNonlinearModuleCategories} we observe that in [[2-module]] theory plain [[presentable categories]] which do not "look linear" in the ordinary sense are naturally regarded as [[Set]]-[[2-modules]], hence as being "[[Set]]-linear", whereas the categories of modules over an algebra that are traditionally regarded as being "$R$-linear categories" are $Mod_R$-[[2-modules]]. This unification of sets as "nonlinear linear structure" has become fashionable as "linear algebra over the [[field with one element]]".

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

So a $\mathcal{V}$-[[enriched category]] $\mathcal{A}$ serves as a _2-[[basis]]_ for a free $\mathcal{V}$-[[2-module]]. Notice that an $R$-algebra $A$ is equivalently a (pointed) $\mathcal{V}$-enriched category $\mathcal{A} = \mathbf{B}A$ with a single object (the [[delooping]] of $A$). Generally, $\mathcal{A}$ may be called  _$R$-[[algebroid]]_.

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

Without further assumptions on $\mathcal{A}$, the category $[\mathcal{A}, \mathcal{V}]$ is just a $\mathcal{V}$-[[2-module]]. But if $\mathcal{A}$ is equipped with further [[extra structure]] and/or [[property]], also $[\mathcal{A}, \mathcal{V}]$ inherits further property. This relation between types of algebras and types of monoidal categories is known as _[[Tannaka duality]]_.

The following table lists the main items of the disctionary of Tannaka duality for associtive algebras that are used in the literature. 

[[!include structure on algebras and their module categories - table]]

##### Matrix calculus for 2-modules: Bimodules and Eilenberg-Watts theorem
 {#MatrixCaclulusFor2Modules}

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

Compare this to how a matrix between two vector spaces equipped with basis sets $B_1, B_2$ is a function

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

For the case at hand where $\mathcal{V} = Mod_R$ and in the special case that $\mathcal{A}_1 = \mathbf{B}A_1$ and $\mathcal{A}_2 = \mathbf{B}A_2$, such a profunctor $\mathbf{B}A_1 \times \mathbf{B}A_2 \to \mathcal{V}$ is equivalently an $A_1$-$A-2$-[[bimodule]] in the traditional sense of associative algebra. Moreover, the [[coend]]-action above is equivalently the traditional [[tensor product of modules]] over the given algebra. Motivated by this example one also generally calls profunctors "bimodules". 

Now one should ask to which extent these "2-matrices" given by profunctors capture all the 2-linear maps between [[2-modules]]. This is what the classical **[[Eilenberg-Watts theorem]]** solves: 

 

+-- {: .num_theorem #EilenbergWattsTheorem}
###### Theorem


There is a [[natural equivalence|natural]] [[equivalence of categories]] 

$$
  (-) \otimes_{A_1} (-)
  \;\colon\;
  {}_{A_1} Mod_{A_2} 
    \stackrel{\simeq}{\to}
  Hom_{2Ab}(Mod_{A_1}, Mod_{A_2})
$$

between [[colimit]]-preserving functors $Mod_{A_1} \to Mod_{A_2}$ between [[categories of modules]] and $A_1$-$A-2$-[[bimodules]], given by sending a bimodule $N$ to the [[tensor product]] functor

$$
  (-) \otimes_{A_1} N \;\colon\; Mod_{A_1} \to Mod_{A_2}
  \,.
$$

=--

In summary we this find that for $R$ a [[commutative ring]], the [[2-category]] $Mod_{Mod_R}$ of $Mod_R$-[[2-modules]] with 2-basis is equivalent to the 2-category $Prof(Mod_R)$ of $Mod_R$-enriched [[profunctors]]. Indeed, another common notation for [[Prof]] is [[Mod]], and so we have the unambiguous notation

$$
  2 Mod_R \simeq Mod(Mod_R)
  \,.
$$

Notice how this is analogous to the identification

$$
  (\infty,2)Cat \simeq Cat(Cat_{(\infty,1)})
$$

discussed at _[[internal (∞,1)-category]]_.


#### 2-Module bundle

* [[2-module bundle]]

#### 2-Lines

+-- {: .num_defn}
###### Definition

For $\mathcal{R}$ a commutative [[2-ring]], def. \ref{2RingAsCompatiblyMonoidalPresentableCategory}, a **[[2-line]]** over $\mathcal{R}$ is an $\mathbb{R}$-[[2-module]], def. \ref{2CategoryOf2Modules} which is invertible under the [[tensor product]] of $\mathbb{R}$-2-modules.

=--

+-- {: .num_defn}
###### Definition

Write 

$$
  Line^\simeq_\mathbb{R} \to Mod_{\mathbb{R}}
$$

for the maximal [[2-groupoid]] of $\mathbb{R}$ 2-lines with 2-basis inside all $\mathbb{R}$-2-modules. This is the **[[Picard 2-groupoid]]** of $\mathcal{R}$. Moreover, by construction it in inherits the structure of a [[3-group]] from the tensor products of 2-modules: as such it is the **[[Picard 3-group]]**.

=--


##### Classification: Azumaya algebras, Brauer group, Picard group

+-- {: .num_prop}
###### Proposition

For $R$ an ordinary [[commutative ring]] and $\mathcal{R} \coloneqq Mod_R$ the [[homotopy groups]] of the [[Picard 2-groupoid]] are

* $\pi_0(2Line^\simeq_R) \simeq Br(R)$ the [[Brauer group]] of $R$;

* $\pi_1(2Line^\simeq_R) \simeq Pic(R)$ the [[Picard group]] of $R$;

* $\pi_2(2Line^\simeq_R) \simeq R^\times$ the [[group of units]] of $R$. 

=--

+-- {: .proof}
###### Proof

By the [[Eilenberg-Watts theorem]], \ref{EilenbergWattsTheorem}, an [[equivalence]] in $2Mod_R$ between 2-modules with 2-basis given by $R$-algebras is a [[Morita equivalence]] of $R$-algebras.

By the prop. \ref{TensorProductModuleCategoriesAsOf2AbelianGroups} and the [[Eilenberg-Watts theorem]], the invertible 2-modules with 2-basis are therefore precisely the [[Azumaya algebras]]. This shows that the connected components of $2Line^\simeq_R$ form the [[Brauer group]] of $R$.

Next, an [[isomorphism class]] of an [[automorphism]] of the canonical base point $Mod_R \in 2Line^\simeq_R$ is by Eilenberg-Watts equivalently an isomorphism class of an $R$-$R$-[[bimodule]] which is invertible under horizontal composition of bimodules. Since $R$ is commutative this just means that it is an isomorphism class of an $R$-module which is invertible under the ordinary [[tensor product of modules]]. But this just means that it is the isomorphism class of an ordinary $R$-[[line]]. This shows that the [[fundamental group]] of $2Line^\simeq_R$ is the ordinary [[Picard group]] of $R$.

Finally an [[automorphism]] of the $R$ regarded as the identity $R$-$R$-[[bimodule]] is an invertible $R$-[[linear function]] $R \to R$, hence is given by multiplication with an invertible element of $R$. This shows that $\pi_2(2Line^\simeq_R)$ is the [[group of units]] of $R$. 

=--

+-- {: .num_remark}
###### Remark

Below in [2-line bundles and their sections](#2LineBundles) we discuss
how forming a [[fiber infinity-bundle|fiber 2-bundle]] of [[2-lines]] as above produces a structure whose [[sections]] are [[twisted bundles]] with typical fiber $Mod_R$, hence for instance [[twisted unitary bundles]] if $R \simeq \mathbb{C}$. This means that the [[characteristic classes]] of $Mod_R$-[[2-line bundles]] are the _twists_ for the [[twisted cohomology]] classifying these twisted bundles. After [[stabilization]] the latter are the [[cocycles]] of [[twisted K-theory]], hence the Brauer group, Picard group and group of units of $R$ are the degree 0, 1, 2-twists of [[twisted K-theory]] over $R$-resectively. Below we discuss two examples of this phenomenon.


=--



##### 2-Line bundles and their sections: twisted K-theory
 {#2LineBundles}

* [[2-line bundle]]

* [[twisted bundle]] / [[Chan-Paton gauge field]] / [[twisted K-theory]]


#### $(\infty,2)$-Abelian groups

(...)

#### $(\infty,2)$-rings

* [[(∞,2)-ring]]

#### $(\infty,2)$-modules
 {#?2Modules}

* [[(∞,2)-module]]

##### Bases for $(\infty,2)$-modules: $A_\infty$-algebras

* [[A-∞ algebra]]


##### Matrix calculus for $(\infty,2)$-modules: $\infty$-Bimodules

* [[∞-bimodule]]

#### $(\infty,n)$-Abelian groups

(...)

#### $(\infty,n)$-rings

* [[(∞,n)-ring]]

#### $(\infty,n)$-modules
 {#?2Modules}

* [[(∞,2)-module]]

##### Bases for $(\infty,n)$-modules

(...)

##### Matrix calculus for $(\infty,n)$-modules

(...)

## References

The notions of [[2-rings]] and [[2-modules]] are nicely set up in 

* [[Alexandru Chirvasitu]], [[Theo Johnson-Freyd]], _The fundamental pro-groupoid of an affine 2-scheme_ ([arXiv:1105.3104](http://arxiv.org/abs/1105.3104))
 {#CJF}

The $(\infty,2)$-category of $A_\infty$-algebras and $\infty$-bimodules between them is constructed in section 3.4 of

* [[Jacob Lurie]], _[[Higher Algebra]]_

For further references see behind the relevant links.
