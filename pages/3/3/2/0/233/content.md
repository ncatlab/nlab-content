+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Higher linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

### Basic idea

The basic idea is that a _module_ $V$ is an object equipped with an [[action]] by a [[monoid]] $A$. This is closely related to the concept of a [[representation]] of a [[group]].

A familiar example of a module is a [[vector space]] $V$ over a [[field]] $k$: this is a _module_ over $k$ in the category [[Ab]] of abelian groups: every element in $k$ acts on the vector space by multiplication of vectors, and this action respects the addition of vectors, but nothing in the definition of [[vector space]] really depends on the fact that $k$ here is a [[field]]: more generally it could be any [[commutative ring]] (or even a general [[rig]]) $R$. The analog of a vector space for fields replaced by rings is that of a _module_ over the ring $R$.

This is the traditional and maybe most common notion of modules. But the basic notion is easily much more general.

### Motivation for and role of modules: generalized vector bundles
 {#RelationToVectorBundlesInIntroduction}

The theory of monoids or rings and their modules, its "meaning" and usage, is naturally understood via the [[Isbell duality|duality]] between [[algebra]] and [[geometry]]:

1. a [[ring]] $R$ is to be thought of as the ring of [[functions]] on some [[space]],

1. an $R$-[[module]] is to be thought of as the space of [[sections]] of a [[vector bundle]] on that space.

A classical situation where this correspondence holds precisely is [[topology]], where

1. the [[Gelfand duality]] theorem says that sending a [[compact topological space]] $X$ to its [[C-star algebra]] $C(X,\mathbb{C})$ of [[continuous functions]] with values in the [[complex numbers]] constitutes an [[equivalence of categories]] between compact topological spaces and the [[opposite category]] of commutative $C^\ast$-algebras;

1. the [[Serre-Swan theorem]] says that sending a [[Hausdorff topological space|Hausdorff]] topological complex [[vector bundle]] $E \to X$ over a compact topological space to the $C(X,\mathbb{C})$-module of its continuous [[sections]] establishes an equivalence of categories between that of topological complex vector bundles over $X$ and that of [[finitely generated module|finitely generated]] [[projective modules]] over $C(X,\mathbb{C})$.

In fact, as this example already shows, modules faithfully subsume vector bundles, but are in fact more general. In many contexts one regard modules as the canonical generalization of the notion of vector bundles, with better formal properties.

This identification of vector bundles with $R$-modules being the spaces of sections of a vector bundle on the space whose ring of functions is $R$ can be taken then as the very _definition_: notably in [[algebraic geometry]] Gelfand duality is taken to "hold by definition" in that an [[algebraic variety]] is essentially by definition the formal dual of a given ring, and the Serre-Swan theorem similarly becomes the statement that the space of sections of a vector bundle over a variety is equivalently given by a module over that ring. (See also at [[quasicoherent module]] for more on this.)

This [[Isbell duality|duality]] between geometry and algebra allows us to re-interpret many statement about modules in terms of vector bundles. For instance 

* the [[direct sum]] of modules corresponds to fiberwise direct sum of vector bundles;

* the [[extension of scalars]] of a module along a ring homomorphism corresponds to [[pullback]] of vector bundles along the dual map of spaces;

* etc.

Using this dictionary for instance the notion of [[descent]] of vector bundles can be expressed in terms of [[monadic descent]], see at _[[Sweedler coring]]_ for discussion of this point.


### More general perspectives

The notion of [[monoid]] in a [[monoidal category]] generalizes
directly to that of a monoid in a [[2-category]], where it is called a [[monad]]. Accordingly the notion of module generalizes to this more general case, where however it is called an _algebra over a monad_ . For more on this see [Modules for monoids in 2-categories: algebras over monads](#MonadAlgs) below.

Apart from this direct generalization, there are two distinct and separately important perspective on the notion of module from the [[nPOV]]:

* modules may usefully be thought of in the context of [[enriched category theory]] (and the enrichment may be over a [[2-category]]);

* modules may usefully be thought of in terms of [[abelian category|abelianization]]/[[stabilization]] of [[overcategory|overcategories]].


#### Modules for monoids in 2-categories: modules over monads {#MonadAlgs}

The notion of [[monoid]] generalizes straightforwardly from
monoids in a [[monoidal category]] to monoids in a [[2-category]]:
for the [[2-category]] [[Cat]], and more generally for arbitrary
2-categories, these are called [[monad]]s.

A [[module over a monad]] (see there for more details) is defined essentially exactly as that 
of module over a monoid. For historical reasons, a module over
a monad in [[Cat]] is called an _algebra over a monad_, because the algebras in the sense of [[universal algebra]] can be obtained as algebras/modules over a [[finitary monad]] in $Set$: the modules for a free algebra monad (for certain kind of algebras) on [[Set]], which are the composition of the free algebra functor and its [[right adjoint]] forgetful functor are exactly algebras of that type. Modules over a fixed monad (in $Cat$) are the objects of the [[Eilenberg-Moore category]] of the monad; in arbitrary bicategory, this category generalized to Eilenberg-Moore objects which may or may not exist. 


#### Enriched presheaves

See [[module over an enriched category]].

#### Stabilized overcategories

A module $N$ over a (commutative, unital) ring $R$ may be encoded in another ring: the one that as an abelian group is the [[direct sum]] $R \oplus N$ and whose product is defined by the formulas

$$
  (r_1, n_1) \cdot (r_2,n_2) := (r_1 r_2, r_2 n_1 + r_1 n_2)
  \,.
$$

This is a **square-0 extension** of $R$. It is canonically equipped with a ring homomorphism $R \oplus N \to R$ which is the identity on $R$ and sends all elements of $N$ to 0. As such, $R \oplus N \to R$ is an object in the [[overcategory]] $CRing/R$. But a special such object: it is in fact canonically an abelian [[group object]] in $CRing/R$, where the group operation (over $R$!) is given by addition of elements in $N$.

From this perspective, it makes sense for general [[category|categories]] $C$ to think of the [[abelian category|abelianization]] of their [[overcategory|overcategories]] $C/A$ as categories of modules over the object $A$.

Taken all together, this makes the fiberwise [[abelian category|abelianization]] of their [[codomain fibration]] $cod : [I,C] \to C$ the category of all possible modules over all objects of $C$.

This general perspective has a nice [[vertical categorification]] to the context of [[(∞,1)-category|(∞,1)-categories]]: abelianization becomes [[stabilization]] in this context, and the fiberwise stabilization of the [[codomain fibration]] of any [[(∞,1)-category]] $C$ is the [[tangent (∞,1)-category]] $T_C \to C$. 

For instance for $sAlg_k$ the [[(∞,1)-category]] of [[simplicial ring|simplicial algebras]] over a ground field $k$ of characteristic 0, we have that the [[stabilization]] $Stab(sAlgk/A)$ of the [[over quasi-category|over (∞,1)-category]] over $A$ is equivalent to the $(\infty,1)$-category $A Mod$ of 
$A$-modules.


## Definition
 {#Definitions}

We spell out the definition of _module_ for 

* [modules over a monoid in a monoidal category](#ModuleOverMonoidObject)

Then we give more general definitions

* [modules as presheaves in enriched category theory](#InEnrichedCategory)

* [modules as objects in stabilized overcategories](#DefWithOCat).


### Modules over a monoid in  a monoidal category
 {#ModuleOverMonoidObject}

See [[module over a monoid]].
 
### Presheaves in enriched category theory
 {#InEnrichedCategory}

See [[module over an enriched category]].

### In terms of stabilized overcategories 
 {#DefWithOCat}

There is a general definition of modules in terms of 
stabilized slice-categories of the category of monoids: _[[Beck modules]]_,
_[[tangent (infinity,1)-categories]]_. 

#### Modules over a ring
 {#ModulesOverARingInTermsOfStabilizedSlices}

The ordinary case of modules over rings is phrased 
in terms of stabilized overcategories by the following
observation, which goes back at least to ([Beck 67](#Beck67)), and is found in the important paper of  ([Quillen 70](#Quillen70)); both listed below. For more see at _[[Beck module]]_.

+-- {: .num_prop #Square0ExtensionsOfRingsAreAbelianSliceObjectsAreModules}
###### Proposition

Let $R \in CRing$ be a commutative [[ring]]. Then there is a canonical [[equivalence of categories|equivalence]] between the [[category]] $R Mod$ of $R$-modules and the category $Ab(CRing/R)$ of abelian [[group object]]s in the [[overcategory]] of $CRing$ over $R$

$$
  R Mod \simeq Ab(CRing/R)
  \,.
$$

=--

+-- {: .proof}
###### Proof

We first unwind what the structure of an abelian group object
$(p:  K \to R)$ in the overcategory $CRing/R$ is explicitly

The unit of the abelian group object in $CRing/R$ is a diagram

$$
  \array{
     R &&\to&& K
     \\
     & {}_{\mathllap{Id}}\searrow && \swarrow_{\mathrlap{p}}
     \\
     && R
  }
  \,.
$$

This diagram identifies $K$ with a ring whose underlying [[abelian group]] is the [[direct sum]] $R \oplus ker(p)$ of some ring $R$ with the [[kernel]] of $p$ such that for $r \in R$ and $n \in ker(p)$ we have $r\cdot n \in ker(p)$. 

The [[product]] of $R \oplus N \to R$ with itself in the [[overcategory]] is the [[fiber product]] over $R$ in the original category, hence is $R \oplus N \oplus N$.

The addition operation on the abelian group object is therefore a morphism

$$
  \array{
    R \oplus N \oplus N &&\to&& R \oplus N
    \\
    & \searrow && \swarrow
    \\
    && R
  }
  \,.
$$

With the above unit, the unit axiom on this operation together with the fact that the top morphism is a ring homomorphism says that this morphism is 

$$
    R \oplus N \oplus N \stackrel{Id \oplus (Id + Id)}{\to}
    R \oplus N
  \,.
$$

Since the ring product in the direct product ring $R \oplus N \oplus N$ between two elements in the two copies of $N$ vanishes, it therefore has to vanish between two elements in the same copy, too. 

This says that $R \oplus N$ is a square-0 extension of $R$. Conversely, for every square-0-extension we obtain an abelian group object this way.

=--

For instance the square-0-extension of a ring $R$ corresponding to the canonical $R$-module structure on $R$ itself is the [[ring of dual numbers]] for $R$. 

#### Modules over a group
 {#ModulesOverAGroupInTermsOfStabilizedOvercategories}

Let $G$ be a [[group]]. Taking together the above desriptions

1. of [Modules over a group as modules over the group ring](#AbelianGroupsWithGAction)

1. of [Modules over a ring as stabilized overcategories](#ModulesOverARingInTermsOfStabilizedSlices) 

one finds:

+-- {: .num_prop }
###### Proposition

The [[category]] of $G$-modules is [[equivalence of categories|equivalent]] to the category of [[abelian group objects]] in the [[slice]] of [[Ring]] over the [[group ring]]

$$
  G Mod \simeq Ab(Ring_{/\mathbb{Z}[G]})
  \,.
$$

=--

But there is also a more direct characterization along these lines, not involving the auxiliary construction of group rings.

+-- {: .num_prop }
###### Proposition

The [[category]] of $G$-modules is equivalent to the category of [[abelian group objects]] in the [[slice category]] of [[groups]] over $G$

$$
  G Mod \simeq Ab(Grp_{/G})
  \,.
$$

=--

+-- {: .proof}
###### Proof

The proof is analogous to that of prop. \ref{Square0ExtensionsOfRingsAreAbelianSliceObjectsAreModules}. 
One checks that a group homomorphism $\hat G \to G$ with the structure of an abelian group object over $G$ is a [[central extension]] of $G$ by some [[abelian group]] $A$ which more over is a split extension (the is the neutral element of the abelian group object) and hence is a [[semidirect product group]] $\hat G \simeq G \ltimes A$. By the discussion there these are equivalently given by [[actions]] of $G$ on $A$ by group [[automorphisms]]. This is precisely what it means for $A$ to carry a $G$-module structure.

=--

This construction generalizes to [[∞-groups]]. See at _[[∞-action]]_ the section _[∞-action -- G-modules](infinity-action#GModules)_.

#### Modules over a simplicial ring 
 {#SimpRings}

Let $sAlg_k$ (or $sAlg$ for short) be the [[(∞,1)-category]] of commutative [[simplicial ring|simplicial algebras]] over a base field $k$. 

For $A \in sAlg_k$ there is generally a functor

$$
  A Mod \to Stab(sAlg_k/A)
$$

from the [[stable (∞,1)-category]] of $A$-modules to the [[stabilization]] of the [[overcategory]] of $sAlg$. But in general this functor is neither [[essentially surjective functor|essentially surjective]] nor [[full functor|full]]. If however $k$ has characteristic 0, then this is an equivalence.


### Modules over an algebra over an operad 
 {#OverHigherAndGeneralizedAlgebras}

There is a notion of [[algebra over an operad]]. The corresponding notion of modules is described at _[[module over an algebra over an operad]]_.

### Multiplicatively cancellative module over a rig

A module $M$ over a [[rig]] $S$ is called multiplicatively cancellative (in [Nazari & Ghalandarzadeh (2019), Sec. 3](#NazariGhalandarzadeh19)) if for any $s,s' \in S$ and $0 \neq m \in M$, $sm = s'm$ implies $s = s'$.

## Examples

### Of modules over a ring
 {#ExamplesOfModulesOverARing}

Let $R$ be a [[commutative ring]].

+-- {: .num_example #RingAsModuleOverItself}
###### Example

The ring $R$ is naturally a module over itself, by regarding its multiplication map $R \otimes R \to R$ as a module action $R \otimes N \to N$ with $N \coloneqq R$.

=--

+-- {: .num_example}
###### Example

More generally, for $n \in \mathbb{N}$ the $n$-fold [[direct sum]] of the [[abelian group]] underlying $R$ is naturally a module over $R$

$$
  R^n \coloneqq R^{\oplus_n} \coloneqq \underbrace{R \oplus R \oplus \cdots \oplus R}_{n\;summands}
  \,.
$$

The module action is componentwise:

$$
  r \cdot (r_1, r_2, \cdots, r_n) = (r \cdot r_1, r\cdot r_2, \cdot r \cdot r_n)
  \,.
$$

=--

+-- {: .num_example}
###### Example

Even more generally, for $I \in $ [[Set]] any [[set]], the direct sum
$\oplus_{i \in I} R$ is an $R$-module.


This is the **[[free module]]** (over $R$) on the set $S$.

The set $I$ serves as the [[basis of a free module]]: a general element $v \in \oplus_i R$ is a [[formal linear combination]] of elements of $I$ with [[coefficients]] in $R$.

=--

For special cases of the ring $R$, the notion of $R$-module is equivalent to other notions:


+-- {: .num_example}
###### Example

For $R = \mathbb{Z}$ the [[integers]], an $R$-module is equivalently just an [[abelian group]].

=--

+-- {: .num_example}
###### Example


A $\mathbb{Z}$-module, hence an abelian group, is not a free module if it has a non-trivial [[torsion subgroup]].

=--

+-- {: .num_example #VectorSpacesArekModules}
###### Example

For $R = k$ a [[field]], an $R$-module is equivalently a [[vector space]] over $k$.

Every [[finitely generated module|finitely generated]] [[free module|free]] $k$-module is a [[free module]], hence every finite dimensional vector space has a [[basis of a free module|basis]]. For infinite dimensions this is true if the [[axiom of choice]] holds.

=--

+-- {: .num_example #RestrictionAndExtensionOfScalars}
###### Example

For $f : S \to R$ a [[homomorphism]] of [[rings]],
[[restriction of scalars]] produces $R$-modules $f_* N$ from $S$-modules $N$ and [[extension of scalars]] produces $S$-modules $f_! N$ from $R$-modules $N$.

=--

+-- {: .num_example #SubmodulesInExamples}
###### Example

For $N$ a module and $\{n_i\}_{i \in I}$ a set of elements, the
[[linear span]]

$$
  \langle n_i\rangle_{i \in I} \hookrightarrow N
  \,,
$$

(hence the completion of this set under addition in $N$ and multiplication by $R$) is a [[submodule]] of $N$.

=--

+-- {: .num_example}
###### Example

Consider example \ref{SubmodulesInExamples} for the case that the module is $N = R$, the ring itself, as in example \ref{RingAsModuleOverItself}. Then a [[submodule]] is equivalently (called) an _[[ideal]]_ of $R$.

=--

+-- {: .num_example}
###### Example

Let $X$ be a [[topological space]] and let 

$$
  R \coloneqq  C(X,\mathbb{C})
$$

be the ring of [[continuous functions]] on $X$ with values in the 
[[complex numbers]]. 

Given a complex [[vector bundle]] $E \to X$ on $X$, write $\Gamma(E)$
for its set of continuous sections. Since for each point $x \in X$ the [[fiber]] $E_x$ of $E$ over $x$ is a $\mathbb{C}$-module (by example \ref{VectorSpacesArekModules}), $\Gamma(X)$ is a $C(X,\mathbb{C})$-module.

By the [[Serre-Swan theorem]]
if $X$ is [[Hausdorff topological space|Hausdorff]] and [[compact topological space|compact]], then $\Gamma(X)$ is a [[projective module|projective]] $C(X,\mathbb{C})$-module and indeed there is an equivalence between projective $C(X,\mathbb{C})$-modules and complex vector bundles over $X$.

More on this below in 
_[Vector bundle and modules](#VectorBundlesAndModules)_.


=--

### Vector bundles and modules
 {#VectorBundlesAndModules}

A [[vector space]] is a [[vector bundle]] over the [[point]]. For every [[vector bundle]] $E \to X$ over a [[space]] $X$, its collection $\Gamma(E)$ of [[section]]s is a module over the monoid/ring of functions on $X$. When $X$ is a [[ringed space]], $\Gamma(X)$ is usefully thought of as a [[sheaf]] of modules over the [[structure sheaf]] of $X$:

For describing vector bundles and their generalization it turns out that this perspective of encoding them in terms of their modules of sections is useful. For instance the category of vector bundles on a space typically fails to be an [[abelian category]]. But if instead of looking just as sheaves of modules on $X$ that arise as sections of vector bundles one generalizes to [[coherent sheaf|coherent sheaves of modules]] then one obtains an abelian category, something like the completion of $Vect(X)$ to an abelian category. If one further demands that the category be closed under push-forward operations, such as to obtain a [[bifibration]] of generalized vector bundles over spaces, one arrives at the notion of [[quasicoherent sheaf|quasicoherent sheaves of modules]] over the [[structure sheaf]].

But it turns out that the category of [[quasicoherent sheaf|quasicoherent sheaves]] over a test space (see there for details) is equivalent simply to the category of _all_ modules over the (functions on) this test space. This means that quasicoherent sheaves of modules have a nice description in terms of the general-abstract-nonsense characterization of modules discussed above:

For $C$ our [[(∞,1)-category]] of of test [[space]]s (hence the [[opposite category]] $C^{op}$ our [[(∞,1)-category]] of "functions rings" on test spaces), by the above the assignment of all modules over a test space is given by

$$
  Mod : C^{op} \to (\infty,1)Cat
$$

$$
  Mod : U \mapsto Stab( C/U )
  \,.
$$

Then for $X$ any [[space]] regarded as an [[∞-stack]] on $C$, a "quasicorent $\infty$-stack of modules" on $X$ is a morphism 

$$
  X \to Mod
  \,.
$$


## Related concepts

* [[action]], [[∞-action]]

* **module**, [[(∞,1)-module]], [[2-module]], [[module category]]

  * [[operad for modules over an algebra]]

  * [[linear independence]]

  * [[Noetherian module]]

  * [[completion of a module]]

  * [[quasicoherent module]]

    [[module over a derived stack]]

  * [[Fredholm module]]

  * [[Beck module]]

* [[representation]], [[∞-representation]]

* [[linear combination]]

* [[submodule]], [[quotient module]]

* [[finitely generated module]], [[presentable module]], [[finitely presented module]]

* [[projective module]], [[injective module]], [[free module]], [[flat module]]

* [[super module]], [[N-graded module]]

* [[Banach module]]

* [[module over a monoidal functor]]

* [[module over an algebra over an operad]]

## References

### General 

A standard textbook is

* F.W. Anderson, K.R. Fuller, _Rings and Categories of Modules_, Graduate Texts in Mathematics, Vol. 13, Springer-Verlag, New York, (1992)

Lectures notes on [[sheaves]] of modules / modules over a [[ringed space]] are in

* [[Daniel Murfet]], _Modules over a ringed space_ ([pdf](http://therisingsea.org/notes/RingedSpaceModules.pdf))

Exposition of basics of [[monoidal categories]] and [[categorical algebra]]:

* _[[geometry of physics -- categories and toposes]]_, Section 2: _[Basic notions of categorical algebra](geometry+of+physics+--+categories+and+toposes#BasicNotionsOfCategoricalAlgebra)_


### On modules as enriched presheaves

See also the references at [[enriched category theory]] and at [[profunctor]].

### On modules as stabilized overcategories

The observation that the category of modules over a ring $R$ is equivalent to the category of abelian group objects in the overcategory $CRing/R$ ([[Beck module]]) is due to

* {#Beck67} [[Jon Beck]], _Triples, algebras and cohomology_, Ph.D. thesis, Columbia University, 1967, Reprints in Theory and Applications of Categories, No. 2 (2003) pp 1-59 ([TAC](http://www.tac.mta.ca/tac/reprints/articles/2/tr2abs.html))

* {#Quillen70} [[Daniel G. Quillen]], _On the (co-)homology of commutative rings_, in Proc. Symp. on Categorical Algebra, 65 &#8211; 87, American Math. Soc.,  1970.

The fully abstract higher categorical concept in terms of [[stabilization|stabilized]] [[overcategory|overcategories]] and the [[tangent (∞,1)-category]] appears in 

* [[Jacob Lurie]], _[[Deformation Theory]]_

[[(∞,1)-modules]] over [[A-∞ algebras]] are discussed in section 4.2 of

* [[Jacob Lurie]], _[[Higher Algebra]]_

Multiplicatively cancellative modules over a rig appear in

* {#NazariGhalandarzadeh19} Rafieh Razavi Nazari, Shaban Ghalandarzadeh, _Multiplication semimodules_, 2019 ([arXiv:0704.2106](https://arxiv.org/abs/1904.11729))


[[!redirects module]]
[[!redirects modules]]

[[!redirects left module]]
[[!redirects left modules]]

[[!redirects right module]]
[[!redirects right modules]]

[[!redirects module over a ring]]
[[!redirects modules over a ring]]
[[!redirects module over rings]]

[[!redirects module over a commutative ring]]
[[!redirects modules over a commutative ring]]
[[!redirects modules over commutative rings]]

[[!redirects multiplicatively cancellative module]]
[[!redirects multiplicatively cancellative modules]]
