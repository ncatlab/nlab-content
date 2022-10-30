# Duoidal categories

* table of contents
{: toc}

## Idea

A *duoidal category* is a category with two [[monoidal category|monoidal structures]] which [[interchange law|interchange]] laxly.

## Definition

A **duoidal category**, or **2-monoidal category**, is a [[pseudomonoid]] in the 2-category $MonCat_l$ of [[monoidal categories]] and [[lax monoidal functors]].  Thus it is a monoidal category, say $(C,\diamond,I)$, together with an additional monoidal structure $(C,\star,J)$ such that $\star:C\times C\to C$ and $J:1\to C$ are lax monoidal functors with respect to $(\diamond,I)$ and the coherence axioms of $(C,\diamond,I)$ are monoidal transformations with respect to $(\diamond,I)$.  The laxity of $\star$ consists of transformations
$$ (A\star B) \diamond (C\star D) \to (A\diamond C) \star (B\diamond D) $$
and
$$ I\to I\star I $$
while the laxity of $J$ consists of transformations
$$ J\diamond J \to J $$
and
$$ I \to J. $$
There are then various axioms, which in particular say that $J$ is a $\diamond$-monoid and $I$ is a $\star$-comonoid.

It is equivalent to ask that $(C,\diamond,I)$ is a pseudomonoid structure on $(C,\star,J)$ in the 2-category $MonCat_c$ of monoidal categories and *colax* monoidal functors.

The map $I\to J$ is actually determined by the rest of the structure; it is the composite
$$I \xrightarrow{\cong} (J\star I)\diamond (I\star J) \to (J\diamond I) \star (I\diamond J) \xrightarrow{\cong} J $$
as well as the dual composite.

## Examples

* Any [[braided monoidal category]] can be made into a duoidal category in which the two monoidal structures agree.  The interchange transformation is built out of the braiding.  Indeed, by the Eckmann-Hilton argument, a duoidal category whose above structure transformations are invertible necessarily arises in this way (up to equivalence).

* If $(C,\diamond,I)$ is a monoidal category with [[finite products]], then it becomes duoidal with $\star$ the [[cartesian monoidal category|cartesian monoidal structure]].  Dually, if $(C,\star,J)$ is a monoidal category with finite coproducts, then it becomes duoidal with $\diamond$ the cocartesian monoidal structure.

* If $A$ and $B$ are monoidal categories, with $A$ small and $B$ cocomplete and closed, then the functor category $[A,B]$ is duoidal with $\star$ the pointwise tensor product, $(X\star Y)(a) = X(a) \otimes Y(a)$, and $\diamond$ the [[Day convolution]] tensor product.

* In particular, if $A$ is a monoid (in Set) and $B$ a cocomplete closed monoidal category, then the category $B^A$ of "$A$-graded objects of $B$" is duoidal with $\star$ the pointwise (or "Hadamard") product and $\diamond$ the "Cauchy" product, $(X\diamond Y)_a = \sum_{b+c=a} X_a \otimes Y_b$.  If $B$ is [[pointed category|pointed]], then the interchange law in this case is naturally a [[split mono]], and its canonical retraction gives $B^A$ a different duoidal structure with the roles of $\star$ and $\diamond$ switched.

* Similarly, the category $[core(FinSet),Vect]$ of vector [[species]] has both a "Hadamard product" $(p\diamond q)(I) = p(I) \otimes q(I)$. and a "Cauchy product" $(p\star q)(I) = \bigoplus_{I = S\sqcup T} p(S) \otimes q(T)$, and is duoidal in two ways.

* The category $FF(C)$ of [[functorial factorizations]] on a category $C$ is a duoidal category.  The $\star$ product of functorial factorizations $F$ and $F'$ is obtained by $F$-factoring a morphism and then $F'$-factoring the first factor, while the $\diamond$ product is obtained by $F$-factoring a morphism and then $F'$-factoring the *second* factor.

* The category $C=[V,V]$ of endofunctors of a closed symmetric monoidal category $V$ is duoidal, with $\star$ being functor composition and $\diamond$ being Day convolution.  (There are size issues here, which can perhaps be resolved using local-presentability and accessibility.)

* Consider the functor category $[FinSet,Set]$, which is equivalent to the category $[Set,Set]_f$ of [[finitary endofunctors]] of $Set$.  Since the composite of finitary endofunctors is finitary, we have an induced composition monoidal structure $\star$.  We can define $\diamond$ by convolution with the monoidal structure of $FinSet$, making $[FinSet,Set]$ duoidal.

* We can do something similar for [[generalized operads]] with respect to any [[monoidal monad|monoidal]] [[pseudomonad]] on [[Prof]].  For instance, with the pseudomonad for symmetric monoidal categories, we obtain a duoidal structure on the category of [[collections]].


## Structures in duoidal categories

### Bimonoids

In a duoidal category $C$, the category $Mon_\diamond(C)$ of [[monoid]] objects with respect to $\diamond$ is again a monoidal category under the $\star$ product.  Specifically, if $A$ and $B$ are $\diamond$-monoids, then the multiplication of $A\star B$ is 
$$ (A\star B) \diamond (A\star B) \to (A\diamond A) \star (B\diamond B) \to A\star B.$$
We define a **bimonoid** in $C$ to be a [[comonoid]] in the monoidal category $(\Mon_\diamond(C),\star)$.  An equivalent definition is obtained by considering $\diamond$-monoids in the category of $\star$-comonoids.

Of course, if $C$ is braided, this reduces to the usual definition of [[bimonoid]] in a braided monoidal category.

A nontrivially duoidal example is that a bimonoid with respect to the duoidal structure on functorial factorizations described above is precisely an [[algebraic weak factorization system]].

### Near-rings

We can define [[near-rigs]] and [[near-rings]] in a duoidal category, where the additive and multiplicative monoidal structures are expressed with respect to $\star$ and $\diamond$ respectively.  Since the distributive law requires duplication of variables, we need the additive monoidal structure to actually be a [[bimonoid]] (or a [[Hopf monoid]] in the case of a near-ring), and hence that $\star$ is (on its own) braided.

More precisely, let $C$ be a duoidal category such that the tensor $\star$ is braided.  A **near-rig** in $C$ is of an object $R$ together with

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

It is a **near-ring** if the additive bimonoid structure is a [[Hopf monoid]].

Of course, this all makes sense in particular in a braided monoidal category regarded as duoidal.  In particular, in a [[cartesian monoidal category]], it reduces to the obvious internal definition of near-rigs and near-rings (since every object of a cartesian monoidal category is a comonoid in a unique way).


## References

* [[Marcelo Aguiar]] and [[Swapneel Mahajan]], *Monoidal Functors, Species and Hopf Algebras*, [pdf](http://www.math.tamu.edu/&#8764;maguiar/a.pdf).

* [[Richard Garner]], _Understanding the small object argument_, [arXiv](http://arxiv.org/abs/0712.0724).

[[!redirects duoidal categories]]
[[!redirects 2-monoidal category]]
[[!redirects 2-monoidal categories]]
