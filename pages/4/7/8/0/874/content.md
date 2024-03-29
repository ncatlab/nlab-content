

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--



# Contents
* table of contents
{: toc}

## Idea

In the strict sense of the word, a _cartesian product_ is a [[product]] in [[Set]], the [[category]] of [[sets]]. Hence for $S_1$ and $S_2$ two [[sets]], their cartesian product is the set denoted $S_1\times S_2$ whose [[elements]] are [[ordered pairs]] of elements in $S_1$ and $S_2$, respectively.

The abstract concept of such [[products]] generalizes from [[Set]] to any other [[category]] (as a special case of a category-theoretic _[[limit]]_), only that in general products of any given [[objects]] may or may not actually exist in that category. 

(If they all exist, then one speaks of a [[cartesian monoidal category]]. Especially if the category is also a [[monoidal category]] with respect to some other [[tensor product]], then one says "Cartesian product" to distinguish the two. For instance one speaks of the cartesian product on [[Cat]] and on [[2Cat]] in contrast to the [[Gray tensor product]].) 

A product [[created limit|created]] by the [[forgetful functor]] of a [[concrete category]], especially in [[algebra]], is often called a [[direct product]] (for instance a [[direct product of groups]]).


## Definition 
 {#Definition}

### In Sets

Given any family $(A_i)_{i:I}$ of sets, the __cartesian product__ $\prod_i A_i$ of the family is the set of all [[functions]] $f$ from the index set $I$ with $f_j$ in $A_j$ for each $j$ in $I$.

As stated, the [[target]] of such a function depends on the argument, which is natural in dependent [[type theory]]; but if you don't like this, then define $\prod_i A_i$ to be the set of those functions $f$ from $I$ to the [[disjoint union]] $\biguplus_i A_i$ such that $f_j \in A_j$ (treating $A_j$ as a [[subset]] of $\biguplus_i A_i$ as usual) for each $j$ in $I$.

In traditional forms of [[set theory]], one can also take the target of $f$ to be the [[union]] $\bigcup_i A_i$ or even the class of all objects (equivalently, leave it unspecified).

$$\prod_{a \in A} B(a) = \{f \in \left(\bigcup_{a\in A} B(a)\right)^A \vert \forall a, f(a) \in B(a) \}$$

### In a general category
 {#InAGeneraCategory}

Given any [[category]] $\mathcal{C}$, and any set $\{X_i\}_{i \in I}$ of its [[objects]], then the product of all these objects is, if it exists, an object denoted 

$$
  \underset{i \in I}{\prod} X_i
  \in 
  \mathcal{C}
$$ 

and equipped with [[morphisms]] 

$$
  p_i \;\colon\; \left(\underset{i \in I}{\prod} X_i\right)
   \longrightarrow 
  X_i
$$


(the _[[projections]]_), for each $i \in I$, such that it is [[universal property|universal with this property]], i.e. such that given any other object $Q \in \mathcal{C}$ with morphisms 

$$
  Q \overset{f_i}{\longrightarrow}  X_i
$$

for $i \in I$, then there is a _unique_ morphism 

$$
  (f_i)_{i \in I}
  \;\colon\; 
  Q \longrightarrow \underset{i \in I}{\prod} X_i
$$

which factors the $f_i$ through the $p_i$, i.e. such that all these [[commuting diagram|diagrams commute]]:

$$
  \array{
    Q 
    \\  
    {}^{\mathllap{(f_i)_{i \in I}}}\downarrow & \searrow^{\mathrlap{f_i}}
    \\
    \underset{i \in I}{\prod} X_i &\underset{p_i}{\longrightarrow}& X_i
  }
$$

for all $i \in I$.


In the case of a binary product it is also denoted by "$(-)\times(-)$":

$$
  \array{
    && Q
    \\
    & \swarrow &\downarrow^{\mathrlap{\exists !}}& \searrow
    \\
    X_1 &\overset{p_1}{\longleftarrow}& X_1 \times X_2 &\overset{p_2}{\longrightarrow}& X_2
  }
  \,.
$$ 

An important special case is a [[power]] of an object $X$, where (referring to notation above) we take all $X_i$ to be $X$ and form 

$$X^I = \prod_{i \in I} X$$

Referring to notation above, if we take $Q = X$ and all $f_i: Q \to X_i$ to be the [[identity morphism]] $1_X: X \to X$, then the map 

$$(f_i)_{i \in I} = (1_X)_{i \in I}: X \to X^I$$ 

is called the *[[diagonal morphism]]*, typically denoted by $\delta_X$ or $\Delta_X$. For example, we have a diagonal map 

$$\delta_X: X \to X \times X$$ 

for binary products. 


### As a functor 

If a [[category]] $C$ admits $I$-fold products (products over an indexing set $I$), then a product [[functor]] 

$$\prod_I = \prod_{i \in I}: C^I \to C$$ 

can be defined, taking a collection of [[objects]] $(c_i)_{i \in I}$ to their product, and taking a collection of [[morphisms]] $(f_i: c_i \to d_i)_{i \in I}$ to a morphism 

$$\prod_{i \in I} f_i: \prod_{i \in I} c_i \to \prod_{i \in I} d_i$$ 

defined to be $(f_i \circ p_i: \prod_{i \in I} c_i \to d_i)_{i \in I}$, using the notation above. (N.B.: the [[Cat|category of (small) categories]] has itself small products, and the notation $C^I$ makes reference to this fact. With some care, we can remove the restriction to [[small categories]].) 

As a [[functor]], $\prod_I: C^I \to C$ is [[right adjoint]] to the diagonal functor $\Delta: C \to C^I$. The [[adjunction unit|unit of the adjunction]] $1_C \to \prod \Delta$, at the component $c \in Ob(C)$, is the [[diagonal morphism]] 

$$\delta_c: c \to c^I$$ 

and the [[counit]] $\Delta \prod \to 1_{C^I}$ is the $I$-tuple of projection maps: 

$$p_i: \prod_{i \in I} c_i \to c_i$$ 

Following the yoga of [[adjunctions]], we can write the "tupling" $(f_i)_{i \in I}: Q \to \prod_{i \in X_i}$ in terms of the product functor and the unit/diagonal map: 

$$(f_i)_{i \in I} = \left(Q \stackrel{\delta_Q}{\to} \prod_{i \in I} Q \stackrel{\prod_{i \in I} f_i}{\to} \prod_{i \in I} X_i\right)$$ 

while in the other direction, as stated in the [[universal property]] above, we can retrieve the components $f_i: Q \to X_i$ of a general map $f: Q \to \prod_{i \in I} X_i$ in terms of the diagonal functor and the counit/projection maps. It boils down to saying 

$$f_i = \left(Q \stackrel{f}{\to} \prod_{i \in I} X_i \stackrel{p_i}{\to} X_i\right)$$ 


## Examples

### Products of sets

Given [[sets]] $A$ and $B$, the cartesian product of the binary family $(A,B)$ is written $A \times B$; its elements $(a,b)$ are called __[[ordered pairs]]__.  (In [[set theory]], one often makes a special definition for this case, defining
$$ (a,b) = \{\{a\},\{a,b\}\} $$
rather than as a function so that ordered pairs can then be used in the definition of function.  From a structural perspective, however, this is unnecessary.)

Given sets $A_1$ through $A_n$, the cartesian product of the $n$-ary family $(A_1,\ldots,A_n)$ is written $\prod_{i=1}^n A_i$; its elements $(a_1,\ldots,a_n)$ are called __ordered $n$-[[tuples]]__.

Given sets $A_1$, $A_2$, etc, the cartesian product of the countably infinitary family $(A_1,A_2,\ldots)$ is written $\prod_{i=1}^\infty A_i$; its elements $(a_1,a_2,\ldots,)$ are called __infinite [[sequences]]__.

Given a set $A$, the cartesian product of the unary family $(A)$ may be identified with $A$ itself; that is, we identify the __ordered [[singleton]]__ $(a)$ with $a$.

The cartesian product of the empty family $()$ is the [[point]], a set whose only element is the __[[empty list]]__ $()$; we often call this set $1$ (or $\pt$, when we\'re Urs) and write its element as $*$.


### Further examples

* In categories of [[algebras]], products are constructed in the "obvious" manner; see for example [[direct product group]]. 

For [[algebraic categories]] like [[Grp]], where the objects are sets equipped with (globally defined) specified operations that satisfy specified universally quantified identities, products are always constructed in the way you'd expect, viz. by taking products at the level of the underlying sets and endowing them with operations defined in the evident pointwise fashion, just like the way it works in $Grp$. More commentary on this in more general contexts will be given below.  

* For a non-example: The category [[Field]] of [[fields]] does not admit [[products]], even though some might consider that an algebraic example (in some loose or informal sense). 

* In categories of topological type, products are again constructed in a common sense manner; see for instance [[product topological space]] for a prototype. 

For [[topological categories]], which include examples like [[Top]] and [[Preord]], products (e.g. [[product topological spaces]]) are always constructed in the way one expects, by taking products at the level of the underlying sets and endowing them with an initial lift structure; e.g., in the case of $Top$, the smallest or initial topology for which the projection maps are continuous. 

This principle continues to hold even for *infinitary* products, where the correct structure might not be obvious without guidance from categorical considerations. For example, for topological spaces, for an infinite product $\prod_{i \in I} X_i$, we use the [[product topology]], and not say the [[box topology]] which might be the first thing one would try. 

* In any [[presheaf category]], i.e., a category of type $Set^C$ where $C$ is a [[small category]], products are calculated in obvious pointwise fashion, where $(F \times G)(c) = F(c) \times G(c)$ with the pointwise product projection maps. This even works if $C$ is [[large category|large]] (making $Set^C$ 'very large'). 

* If $D$ has products and $C \hookrightarrow D$ is a [[reflective subcategory]], products in $C$ exist and are calculated as they are in $D$. For example, this applies to any [[Grothendieck topos]], as a category of [[sheaves]] on a [[site]] forming a reflective subcategory of a category of presheaves (on the underlying category of the site). 

  * For instance, the category [[Pos]] of [[posets]] is a reflective subcategory of [[Preord]]. 
  * Any [[locally presentable category]] can be exhibited as a reflective subcategory of a presheaf topos; as such we know how to calculate products there. 
  
* Generalizing the last example still further, if $U: A \to X$ is a [[monadic functor]], then products and more generally [[limits]] in $A$ are created (or [[reflected limit|reflected]]) from products/limits in $X$. In other words, products of algebras over a [[monad]] $T: X \to X$ are given by products in $X$, equipped with the evident "pointwise" $T$-algebra structure. 

* If $D$ has products and $i: C \hookrightarrow D$ is a *[[coreflective subcategory|coreflective]]* subcategory, where $i$ has a right adjoint (co-reflector) $r$, then products in $C$ can be formed by taking products in $D$ and then applying $r$. 

  * For example, the category $CG$ of [[compactly generated spaces]] is coreflective in [[Top]]. The product in $CG$ does not coincide in general with the topological product: one may have to add to the product topology still more sets, just enough to ensure that the topology is compactly generated. 

* Products in $C^{op}$ are given by [[coproducts]] in $C$. 

  * In some cases, this formal tautology gives the only sensible way to construct products. For example, to form products $X \times Y$ in the category [[Loc]] of [[locales]], one must take the formal dual of the coproduct (denoted $\mathcal{O}(X) \otimes \mathcal{O}(Y)$) in the category of [[frames]]. 

  * Similarly, the product of two [[affine schemes]] is the formal dual of the coproduct of their corresponding coordinate rings, again given by a tensor product. 

* Relative to a [[symmetric monoidal category]] $C$ with monoidal product $\otimes$, products in the category of [[cocommutative comonoids]] are given by the tensor product $X \otimes Y$ in the underlying smc category. 

  * For instance, this is how products of [[cocommutative coalgebras]] are formed. This applies for instance to cocommutative [[Hopf algebras]]. 
  * In a [[cartesian bicategory]] such as $Rel$, the accompanying category of objects and *maps* (= left adjoint 1-cells) coincides with the category of cocommutative comonoids and comonoid maps between them (which is $Set$ in the case of $Rel$). Thus, at the level of objects, the usual tensor product in $Rel$ coincides with the cartesian product in $Set$. 

* For categories $C$ enriched in the category of [[commutative monoids]], [[finite products]] are [[biproducts]] and hence coincide with coproducts in a controlled fashion (via [[matrices]]). However, this is usually not the case for infinite products. For such examples, finite products are [[absolute limits]]. 

* In the category [[SupLat]] of [[sup-lattices]], arbitrary products coincide with coproducts (and in fact the functor $X \mapsto X^{op}$ that takes a sup-lattice to its posetal opposite is part of a perfect duality $SupLat^{op} \to SupLat$, taking a sup-lattice map $f: X \to Y$ to $g^{op}: Y^{op} \to X^{op}$ where $f \dashv g$). This example descends to $Rel$ itself, so we conclude that products in $Rel$ are actually given by coproducts in $Rel$ which in turn are given by coproducts in $Set$. 

* [[product of simplices]]

* In the [[Cat]] the cartesian product is the [[product of categories]].

* If either [[projection]] out of a Cartesian product is regarded as a ([[fiber bundle|fiber]]) [[bundle]] map, it is called a _[[trivial fiber bundle]]_.



## Properties

### Relation to type theory

Under the [[relation between category theory and type theory]] products in a category correspond to [[product types]] in [[type theory]].

[[!include product natural deduction - table]]


### Foundational status

In [[material set theory]], the existence of binary cartesian products follows from the [[axiom of pairing]] and the axiom of [[weak replacement]] (which is very weak).  In [[structural set theory]], their existence generally must be stated as an axiom: the __axiom of products__.  See [[ordered pair]] for more details.


## Related entries

* [[cartesian monoidal category]]

* [[finite product]]

* [[tensor product]]

* [[sum]]

* [[external product]]

* [[restricted product]]

* [[product type]]

* [[base change]]

  * [[dependent sum]], [[dependent product]]

  * [[dependent sum type]], [[dependent product type]]


## References

Textbook account:

* [[Francis Borceux]], Section 2.1 in Vol. 1: *Basic Category Theory* of: *[[Handbook of Categorical Algebra]]*, Encyclopedia of Mathematics and its Applications **50** Cambridge University Press (1994) ([doi:10.1017/CBO9780511525858](https://doi.org/10.1017/CBO9780511525858))

Categories with one object and binary products are studied in:

* Aaron Gray and Keith Pardue, _Products in a Category with One Object_, [arXiv:1604.03999](https://arxiv.org/abs/1604.03999) (2016).

* Richard Statman, _Products in a category with only one object_, [arXiv:2101.10494](https://arxiv.org/abs/2101.10494) (2021).


category: foundational axiom

[[!redirects cartesian product]]
[[!redirects cartesian products]]
[[!redirects Cartesian product]]
[[!redirects Cartesian products]]
[[!redirects product set]]
[[!redirects product sets]]
[[!redirects product of sets]]
[[!redirects products of sets]]

[[!redirects axiom of cartesian products]]
[[!redirects axiom of Cartesian products]]
[[!redirects axiom of products]]

[[!redirects product]]
[[!redirects products]]


