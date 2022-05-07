

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--


# Duoidal categories

* table of contents
{: toc}

## Idea

A *duoidal category* is a [[category]] with two [[monoidal category|monoidal structures]] which [[interchange law|interchange]] laxly.

## Definition

### Duoidal categories

A **duoidal category**, or **2-monoidal category**, is a [[pseudomonoid]] in the [[2-category]] $MonCat_l$ of [[monoidal categories]] and [[lax monoidal functors]].  Thus it is a monoidal category, say $(C,\diamond,I)$, together with an additional monoidal structure $(C,\star,J)$ such that $\star:C\times C\to C$ and $J:1\to C$ are [[lax monoidal functors]] with respect to $(\diamond,I)$ and the [[coherence]] axioms of $(C,\diamond,I)$ are [[monoidal natural transformations]] with respect to $(\diamond,I)$.  The laxity of $\star$ consists of [[natural transformations]]
$$ (A\star B) \diamond (C\star D) \to (A\diamond C) \star (B\diamond D) $$
and
$$ I\to I\star I $$
while the laxity of $J$ consists of transformations
$$ J\diamond J \to J $$
and
$$ I \to J. $$
There are then various axioms, which in particular say that $J$ is a $\diamond$-[[monoid]] and $I$ is a $\star$-[[comonoid]].

It is equivalent to ask that $(C,\diamond,I)$ is a pseudomonoid structure on $(C,\star,J)$ in the 2-category $MonCat_c$ of monoidal categories and *colax* monoidal functors.

The map $I\to J$ is actually determined by the rest of the structure; it is the composite
$$I \xrightarrow{\cong} (J\star I)\diamond (I\star J) \to (J\diamond I) \star (I\diamond J) \xrightarrow{\cong} J $$
as well as the dual composite.  If this map is an isomorphism, the duoidal category is called **normal**.

### Duoidal functors

There are three natural kinds of functors between duoidal categories, which are compatibly lax or colax with respect to $\star$ and $\diamond$.  The possible choices of lax and colax seem like there should be four, but in fact only three of them work; in the fourth case the compatibility condition would involve wrong-way composites due to the non-invertibility of the duoidal interchange constraints.

### Virtual duoidal categories

A **virtual duoidal category** is a pseudomonoid in the 2-category of [[multicategories]].  That is, it is a multicategory with a monoidal structure $(C,\star,J)$: the $\diamond$-monoidal structure is replaced by the multicategory structure.  Since every monoidal category can be regarded as a [[representable multicategory]], and multicategory functors correspond exactly to lax monoidal functors, duoidal categories can be identified with virtual duoidal categories in which the multicategory structure is representable.

In particular, note that $J$ in a virtual duoidal category is a functor of multicategories $1\to C$, i.e. precisely a [[monoid]] in the multicategory $C$.  As part of this monoid structure it has a unit map $()\to J$; we say that the virtual duoidal category $C$ is **normal** if this map exhibits $J$ as a unit object for the multicategory structure.

Nearly all the definitions given below for duoidal categories (except for coduoids and colax/colax functors) make sense just as well for virtual ones.


## Examples

* Any [[braided monoidal category]] can be made into a (normal) duoidal category in which the two monoidal structures agree.  The interchange transformation is built out of the braiding.  Indeed, by the Eckmann-Hilton argument, a duoidal category whose above structure transformations are invertible necessarily arises in this way (up to equivalence).

* Similarly but somewhat more generally, an 2-monoidal category, as a special case of [[iterated monoidal category]] (in the sense of Balteanu, Fiedorowicz, Schw&#228;nzl, and Vogt), is a duoidal category.  More precisely, 2-monoidal categories are the duoidal categories such that $\star$ and $J$ are *normal* lax monoidal functors, meaning concretely that the morphisms $I\to I\star I$ and $I\to J$ are isomorphisms.

* If $(C,\diamond,I)$ is a monoidal category with [[finite products]], then it becomes duoidal with $\star$ the [[cartesian monoidal category|cartesian monoidal structure]].  Dually, if $(C,\star,J)$ is a monoidal category with finite coproducts, then it becomes duoidal with $\diamond$ the cocartesian monoidal structure.

* If $A$ and $B$ are monoidal categories, with $A$ small and $B$ cocomplete and closed, then the functor category $[A,B]$ is duoidal with $\star$ the pointwise tensor product, $(X\star Y)(a) = X(a) \otimes Y(a)$, and $\diamond$ the [[Day convolution]] tensor product.

* In particular, if $A$ is a monoid (in Set) and $B$ a cocomplete closed monoidal category, then the category $B^A$ of "$A$-graded objects of $B$" is duoidal with $\star$ the pointwise (or "Hadamard") product and $\diamond$ the "Cauchy" product, $(X\diamond Y)_a = \sum_{b+c=a} X_a \otimes Y_b$.  If $B$ is [[pointed category|pointed]], then the interchange law in this case is naturally a [[split mono]], and its canonical retraction gives $B^A$ a different duoidal structure with the roles of $\star$ and $\diamond$ switched.

* Similarly, the category $[core(FinSet),Vect]$ of vector [[species]] has both a "Hadamard product" $(p\diamond q)(I) = p(I) \otimes q(I)$. and a "Cauchy product" $(p\star q)(I) = \bigoplus_{I = S\sqcup T} p(S) \otimes q(T)$, and is duoidal in two ways.

* The category $FF(C)$ of [[functorial factorizations]] on a category $C$ is a duoidal category.  The $\star$ product of functorial factorizations $F$ and $F'$ is obtained by $F$-factoring a morphism and then $F'$-factoring the first factor, while the $\diamond$ product is obtained by $F$-factoring a morphism and then $F'$-factoring the *second* factor.

* The category $C=[V,V]$ of endofunctors of a closed symmetric monoidal category $V$ is *virtually* duoidal, with $\star$ being functor composition the multicategory structure being "the one that would be represented by Day convolution if it existed".  That is, a morphism $(F,G) \to H$ is a natural transformation $F\otimes G \to H\circ \otimes$ between functors $V\times V \to V$, and so on.  This multicategory structure is not generally representable, since the convolution product requires colimits of the size of the domain category, but $V$ can't in general be expected to have $V$-sized colimits.  However, if $V$ is monoidally [[locally presentable category|locally presentable]], then we can restrict to the subcategory $End_\kappa(V)$ of $\kappa$-accessible endofunctors, and in this case there is no problem, since $End_\kappa(V) \simeq [V_\kappa,V]$  where $V_\kappa$ is the essentially small subcategory of $\kappa$-presentable objects.  If $V=Set$ then this (virtual) duoidal structure is normal with $I=J$ being the identity functor, but for general $V$ it need not be normal.

* As special case of the preceding when $V=Set$ and $\kappa=\omega$, consider the functor category $[FinSet,Set]$, which is equivalent to the category $[Set,Set]_f$ of [[finitary endofunctors]] of $Set$.  Since the composite of finitary endofunctors is finitary, we have an induced composition monoidal structure $\star$.  We can define $\diamond$ by convolution with the monoidal structure of $FinSet$, making $[FinSet,Set]$ duoidal.

* More generally, instead of $End_\kappa(V) = [V_\kappa,V]$ we can consider any category $[V',V]$ where $V'$ is a small monoidal subcategory of $V$ as long as the category of functors $V\to V$ that are left Kan extended from $V'$ is closed under composition.  For instance, if $A$ is a monoidal category and $V=[A^{op},Set]$ with $V'=A$, then $[V',V] \simeq Prof(A,A)$ is the category of endo-profunctors of $A$, which is therefore duoidal.  More generally, the category of endo-proarrows of any monoidal object in a [[proarrow equipment]] is duoidal by a similar construction: $\star$ is proarrow composition and $\diamond$ is convolution with the monoidal structure on both sides.

* We can do something similar for [[generalized operads]] with respect to any [[monoidal monad|monoidal]] [[pseudomonad]] on [[Prof]].  For instance, with the pseudomonad for symmetric monoidal categories, we obtain a duoidal structure on the category of [[collections]].


## Structures in duoidal categories

### Bimonoids, bicomonoids, and duoids

In a duoidal category $C$, the category $Mon_\diamond(C)$ of [[monoid]] objects with respect to $\diamond$ is again a monoidal category under the $\star$ product.  Specifically, if $A$ and $B$ are $\diamond$-monoids, then the multiplication of $A\star B$ is 
$$ (A\star B) \diamond (A\star B) \to (A\diamond A) \star (B\diamond B) \to A\star B.$$
We define a **[[bimonoid]]** in $C$ to be a [[comonoid]] in the monoidal category $(\Mon_\diamond(C),\star)$.  An equivalent definition is obtained by considering $\diamond$-monoids in the category of $\star$-comonoids.

Of course, if $C$ is [[braided monoidal category|braided]], this reduces to the usual definition of [[bimonoid]] in a braided monoidal category.

A nontrivially duoidal example is that a bimonoid with respect to the duoidal structure on functorial factorizations described above is precisely an [[algebraic weak factorization system]].

Similarly, a **[[duoid]]** is defined to be a $\star$-monoid in the monoidal category $(\Mon_\diamond(C),\star)$ of $\diamond$-monoids, while a *coduoid* is a $\diamond$-comonoid in the category of $\star$-comonoids.  Duoids, bimonoids, and coduoids in $C$ are equivalently duoidal functors $1\to C$ of the three possible kinds (see above).

### Rings and near-rings

We can define [[near-rig|(near-)]][[rigs]] and near-[[rings]] in a duoidal category, where the additive and multiplicative monoidal structures are expressed with respect to $\star$ and $\diamond$ respectively.  Since the distributive law requires duplication of variables, we need the additive monoidal structure to actually be a [[bimonoid]] (or a [[Hopf monoid]] in the case of a ring), and hence that $\star$ is (on its own) braided.

More precisely, let $C$ be a duoidal category such that the tensor $\star$ is braided (and probably some compatibility holds between the braiding and the duoidal structure).  A **near-rig** in $C$ is of an object $R$ together with

* A [[bimonoid]] structure on $R$ with respect to the braided monoidal category $(C,\star,J)$, written as addition $add:R\star R \to R$ and "coaddition" $\Delta:R\to R\star R$;

* A [[monoid]] structure on $R$ with respect to $(C,\diamond,I))$, written as multiplication $mult : R \diamond R \to R$;

* The following diagram commutes, expressing right distributivity:
  $$ \array{
    (R\star R) \diamond R & \xrightarrow{add\diamond id} &
    R\diamond R & \xrightarrow{mult} &
    R\\
    ^{id \diamond \Delta}\downarrow & & & &
    \uparrow^{add}\\
    (R\star R) \diamond (R\star R) &\to &
    (R\diamond R) \star (R\diamond R) & \xrightarrow{mult \star mult} &
    R\star R
  }
  $$

* The following diagram commutes, expressing right absorption:
  $$ \array{ 
    R & \xrightarrow{\epsilon} &
    J & \xrightarrow{0} &
    R\\
    ^\cong\downarrow & & & & \uparrow^{mult} \\
    I\diamond R & \to &
    J \diamond R & \xrightarrow{0\diamond id} &
    R\diamond R
  }
  $$

It is a **near-ring** if the additive bimonoid structure is a [[Hopf monoid]], and a **rig** or **ring** if the left distributive law and left absorption also hold.

Of course, this all makes sense in particular in a braided monoidal category regarded as duoidal.  In particular, in a [[cartesian monoidal category]], it reduces to the obvious internal definition of (near-)rigs and (near-)rings (since every object of a cartesian monoidal category is a comonoid in a unique way).

One can show that for near-rings, cocommutativity is automatic, in which case the Hopf monoid $(R,add,\Delta)$ can equivalently be regarded as a Hopf monoid in the *cartesian* monoidal category $CComon_\star(C)$ of cocommutative comonoids in $(C, \star, J)$.  In this case, the above definitions coincide with the definitions of (near-)rings in the [[colax-distributive rig category]] induced by $\diamond$ and the cartesian structure of $CComon_\star(C)$. However, for general (near)-rigs, the definitions do not coincide, because cocommutativity is not automatic for near-rigs.

### Strong and commutative monoids

Note that the constraints $J\diamond J\to J$ and $I\to J$ make $J$ into a $\diamond$-monoid, and indeed also a bimonoid (since it is certainly a $\star$-comonoid).  Also, just as the category of $\diamond$-monoids is $\star$-monoidal, the category of left, right, or bi-$\diamond$-modules over any bimonoid $A$ is $\star$-monoidal, with actions such as
$$(M\star N) \diamond A \to (M\star N) \diamond (A\star A) \to (M\diamond A) \star (N\diamond A) \to M\star N.$$
If $C$ admits reflexive coequalizers preserved in each variable by $\diamond$, then the category of $(A,\diamond)$-bimodules is in fact duoidal, with $\diamond$ the usual tensor product of bimodules.  (In the absence of such coequalizers, this category is virtually duoidal.)

We define a **bistrong $\star$-monoid** in a duoidal category to be a $\star$-monoid in the monoidal category of $J$-$\diamond$-bimodules.  In the duoidal categories of endofunctors considered above, this reproduces the usual notion of "bistrong functor" (i.e. functor with a compatible left and right [[tensorial strength]]).  Note that in a *normal* duoidal category, every object is uniquely a $J$-bimodule, so every $\star$-monoid is bistrong; and conversely, the duoidal category of $(J,\diamond)$-bimodules is (when it exists) always normal.

If the monoidal structure $\diamond$ is [[braided monoidal category|braided]] (compatibly with $\star$), then a one-sided module automatically acquires a module structure on the other side.  In this case, we define a **strong $\star$-monoid** to be a bistrong one whose $J$-$\diamond$-bimodule structure is obtained in this way.

Now let $S$ and $T$ be arbitrary objects and $M$ a (bi)strong $\star$-monoid.  We say that two morphisms $\sigma:S\to M$ and $\tau:T\to M$ be morphisms **commute** if the following diagram commutes:
$$\array{
  T\diamond S & \xrightarrow{\cong} &
  (T\star J) \diamond (J \star S) & \to &
  (T\diamond J) \star (J\diamond S) \\
  ^\cong\downarrow  &&&& \downarrow^{\tau \star \sigma}\\
  (J\star T) \diamond (S \star J) &&&& M\star M\\
  \downarrow &&&& \downarrow^{mult}\\
  (J\diamond S) \star (T\diamond J) & \xrightarrow{\sigma \star \tau} &
  M\star M & \xrightarrow{mult} & M.
}
$$
We say that $M$ is **commutative** if $id_M$ and $id_M$ commute.

In a braided monoidal category regarded as a normal duoidal one, this reduces to the usual notion of [[commutative monoid]] object.  On the other hand, in the endofunctor-like examples above, it results in the notion of [[commutative monad]] or [[commutative theory]].


## Relation to intercategories

A duoidal category is the same as an [[intercategory]] with one object and only identity horizontal arrows, vertical arrows, horizontal cells, and vertical cells.  The objects of the duoidal category are the basic cells of the intercategory, and its morphisms are the cubes.  Like duoidal categories, intercategories support three (but not four) different kinds of morphism.


## Related concepts

* [[distributivity for monoidal structures]]
* [[intercategory]]

## References

* [[Marcelo Aguiar]] and [[Swapneel Mahajan]], *Monoidal Functors, Species and Hopf Algebras*, [pdf](http://www.math.iitb.ac.in/~swapneel/aguiar.pdf).  Here the notion is called a "2-monoidal category".

* [[Richard Garner]], _Understanding the small object argument_, [arXiv](http://arxiv.org/abs/0712.0724).  Here the notion is called a "2-fold monoidal category", although [[iterated monoidal category|that term]] is also used for the case when the two units coincide.

* [[Michael Batanin]] and [[Martin Markl]], _Centers and homotopy centers in enriched monoidal categories._ Advances in Mathematics 230 , 4-6 (2012), 1811–1858.  Here apparently the term "duoidal category" was introduced.

* [[Richard Garner]], [[Ignacio López Franco]], _Commutativity_, [arXiv](http://arxiv.org/abs/1507.08710).  See also _Commutativity and tensor products of theories, monads, and operads_, talk at CT2013, [slides](https://www.dpmms.cam.ac.uk/~ill20/ct2013-talk.pdf)

* Zoran Petri&#263; and [[Todd Trimble]] 2014, _Symmetric bimonoidal intermuting categories and $\omega \times \omega$ reduced bar constructions_, Applied Categorical Structures 22(3): 467-499, [arXiv:0906.2954](http://arxiv.org/abs/0906.2954)


[[!redirects duoidal category]]
[[!redirects duoidal categories]]
[[!redirects 2-monoidal category]]
[[!redirects 2-monoidal categories]]

[[!redirects virtual duoidal category]]
[[!redirects virtual duoidal categories]]
