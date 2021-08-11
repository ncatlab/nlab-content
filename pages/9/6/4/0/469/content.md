
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Monoidal categories
+-- {: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A *closed monoidal category* is a [[monoidal category]] $C$ that is also a [[closed category]], in a compatible way:

it has for each [[object]] $X$ a [[functor]] $(-) \otimes X : C \to C$ of forming the [[tensor product]] with $X$, as well as a functor $[X,-] : C \to C$ of forming the [[internal-hom]] with $X$, and these form a pair of [[adjoint functors]].


The strategy for formalizing the idea of a closed category, that "the collection of morphisms from $a$ to $b$ can be regarded as an object of $C$ itself", is to mimic the situation in [[Set]] where for any three objects (sets) $a$, $b$, $c$ we have [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism)
$$
  Hom(a \otimes b, c) \simeq Hom(a, [b,c])
  \,,
$$
[[natural transformation|natural]] in all three [[variables]],
where $\otimes = \times$ is the standard [[cartesian product]] of sets.  This [[natural isomorphism]] is called [[currying]].

Currying can be read as a characterization of the [[internal hom]] $Hom(b,c)$ and is the basis for the following definition.

A closed monoidal category is a special case of the notion of [[closed pseudomonoid]] in a [[monoidal bicategory]].


## Definitions

### Symmetric closed monoidal category

A [[symmetric monoidal category|symmetric]] [[monoidal category]] $C$ is **closed** if for all [[objects]] $b \in C_0$ the [[tensor product]] [[functor]] $ b \otimes - : C \to C$ has a [[right adjoint]] functor $[b,-] \colon C \to C$.

$$
  \underset{b \in C}{\forall}
  \;\;
  C
  \underoverset
    {\underset{[b,-]}{\longrightarrow}}
    {\overset{b \otimes (-)}{\longleftarrow}}
    {\;\;\;\;\;\bot\;\;\;\;\;}
  C
  \,.
$$

This [means](adjoint+functor#InTermsOfHomIsomorphism) that for all $a,b,c \in C_0$ we have a [[natural bijection]]

$$
  Hom_C(a \otimes b, c) 
   \;\simeq\; 
  Hom_C(a, [b,c])
  \,,
$$

[[natural transformation|natural]] in all [[variables|arguments]].

The object $[b,c]$ is called the **[[internal hom]]** of $b$ and $c$. This is commonly also denoted by lower case $hom(b,c)$ (and then sometimes underlined).

### Cartesian closed monoidal category

If the monoidal structure of $C$ is [[cartesian monoidal category|cartesian]] (and so in particular [[symmetric monoidal category|symmetric monoidal]]), then $C$ is called **[[cartesian closed]]**.  In this case the internal hom is often called an **[[exponential object]]** and written $c^b$.

### Left-, right- and bi-closed monoidal category

If $C$ is [[monoidal category|monoidal]] but not necessarily [[symmetric monoidal category|symmetric]] or even [[braided monoidal category|braided]], then left and right [[tensor product]] $-\otimes b$ and $b\otimes -$ may be inequivalent functors, and either one or both may have an adjoint.  The terminology here is less standard, but many people use **left closed**, **right closed**, and **biclosed** monoidal category to indicate, respectively, that the left tensor product, the right tensor product functors or both have [[right adjoints]].  (Other authors simply say **closed** instead of biclosed.)  So in particular a symmetric closed monoidal category is automatically biclosed.

The analogue of exponential objects for monoidal categories are [[residual|left and right residuals]].

## Properties

+-- {: .num_prop #TensorHomIsoInternalizes} 
###### Proposition

For $(\mathcal{C}, \otimes, 1)$ a closed monoidal category with [[internal hom]] denoted $[-,-]$, then not only are there [[natural bijections]]

$$
   Hom_{\mathcal{C}}(X \otimes Y, Z)
  \simeq
   Hom_{\mathcal{C}}(X, [Y,Z])
$$

but these isomorphisms themselves "internalize" to isomorphisms in $\mathcal{C}$ of the form

$$
  [X \otimes Y, Z]
    \simeq
  [X,[Y,Z]]
  \,.
$$


=--

+-- {: .proof}
###### Proof

By the external natural bijections there is for every $A \in \mathcal{C}$ a composite natural bijection

$$
  Hom_{\mathcal{C}}(A, [X \otimes Y, Z])
   \simeq
  Hom_{\mathcal{C}}(A \otimes (X \otimes Y), Z)
   \simeq
  Hom_{\mathcal{C}}((A \otimes X) \otimes Y, Z)
    \simeq
  Hom_{\mathcal{C}}(A \otimes X, [Y,Z])
    \simeq
  Hom_{\mathcal{C}}(A,[X,[Y,Z]])
  \,.
$$

Since this holds for every $A \in \mathcal{C}$, the [[Yoneda lemma]] (namely the [[fully faithful functor|fully faithfulness]] of the [[Yoneda embedding]]) implies that there is already an isomorphism

$$
  [X \otimes Y, Z] \simeq [X,[Y,Z]]
  \,.
$$

=--

## Examples ##

 * The tautological example is the category [[Set]] of sets with its [[Cartesian product]]: the collection of functions between any two sets is itself a set -- the [[function set]].  More generally, any [[topos]] is cartesian closed monoidal.

 * The category [[Ab]] of [[abelian groups]] with its [[tensor product of abelian groups]] is closed: for any two abelian groups $A, B$ the set of homomorphisms $A \to B$ carries (pointwise defined) abelian group structure. 

 * The category of [[modules]] over a given [[commutative ring]] with its usual tensor product is closed monoidal. This is one of the first hom-tensor adjunctions that appeared in algebra.

 * Generalizing the examples above, given a closed monoidal category $C$ with [[equalizers]] and [[coequalizers]] and a [[commutative monad]] $T$, the category of [[algebra over a monad|$T$-algebras]] inherits a closed monoidal structure. See [[tensor product of algebras over a commutative monad]].

* A [[discrete category|discrete]] monoidal category (i.e., a [[monoid]]) is left closed iff it is right closed iff every object has an inverse (i.e., it is a [[group]]).

* The [[delooping]] $\mathbf{B}M$ of a [[commutative monoid]] $M$ is a closed monoidal (in fact, [[compact closed]]) category with one object, with both the tensor and internal hom defined (on morphisms) using the multiplication operation $f \otimes g = [f,g] = f g$.  Conversely, any closed monoidal category with one object must be isomorphic to one constructed from a commutative monoid. (See [Eilenberg and Kelly (1965)](#EilenbergKelly65), IV.3, p.553.)

* Certain [[nice category of spaces|nice categories]] of [[topological spaces]] are cartesian closed: for any two nice enough topological spaces $X$, $Y$ the set of continuous maps $X \to Y$ can be equipped with a topology to become a nice topological space itself.

* Certain nice categories of _[[pointed object|pointed/based]]_  topological spaces are closed symmetric monoidal.  The monoidal structure is the [[smash product]] and the internal-hom is the set of basepoint-preserving maps with topology induced from the space of unbased ones.

* The category [[Cat]] is cartesian closed: the internal-hom is the [[functor category]] of functors and natural transformations.

* The category $2 Cat$ of [[strict 2-category|strict 2-categories]] and strict 2-functors is closed symmetric monoidal under the [[Gray tensor product]].  The internal-hom is the 2-category of strict 2-functors, _pseudo_ natural transformations, and modifications.

* The category of strict $\omega$-[[strict omega-category|categories]] is also biclosed monoidal, under the [[Crans-Gray tensor product]].

* If $M$ is a monoidal category and $Set^{M^{op}}$ is endowed with the tensor product given by the induced [[Day convolution]] product, then the [[category of presheaves]] $Set^{M^{op}}$ is biclosed monoidal. 

* The category of [[species]], with the monoidal structure given by substitution product of species, is closed monoidal (each functor $- \circ G$ admits a right adjoint) but not biclosed monoidal. 

* The category of [[modules]] over any [[Hopf monoid]] in a closed monoidal category, or more generally algebras for any [[Hopf monad]], is again a closed monoidal category.  In particular, the category of modules over any [[group object]] in a [[cartesian closed category]] is (cartesian) closed monoidal. For more on this phenomenon see at _[[Tannaka duality]]_.

* The category of [[locally convex topological vector spaces]] with the [[inductive tensor product]] and internal hom the space of continuous linear maps with the topology of pointwise convergence is symmetric closed monoidal.

### Functor categories

+-- {: .num_theorem}
###### Theorem
Let $C$ be a [[complete category|complete]] closed monoidal category and $I$ any [[small category]].  Then the [[functor category]] $[I,C]$ is closed monoidal with the pointwise tensor product, $(F\otimes G)(x) = F(x) \otimes G(x)$.
=--
+-- {: .proof}
###### Proof
Since $C$ is complete, the category $[I,C]$ is [[comonadic functor|comonadic]] over $C^{ob I}$; the comonad is defined by right [[Kan extension]] along the inclusion $ob I \hookrightarrow I$.  Now for any $F\in [I,C]$, consider the following square:
$$\array{[I,C] & \overset{F\otimes - }{\to} & [I,C] \\
  \downarrow && \downarrow\\
  C^{ob I}& \underset{F_0 \otimes -}{\to} & C^{ob I}}
$$
This commutes because the tensor product in $[I,C]$ is pointwise (here $F_0$ means the family of objects $F(x)$ in $C^{ob I}$).
Since $C$ is closed, $F_0 \otimes -$ has a right adjoint.
Since the vertical functors are comonadic, the (dual of the) [[adjoint lifting theorem]] implies that $F\otimes -$ has a right adjoint as well.
=--

## Related concepts

* [[monoidal category]], [[monoidal (∞,1)-category]]

* [[symmetric monoidal category]], [[symmetric monoidal (∞,1)-category]]

* **closed monoidal category** ,  [[closed monoidal (∞,1)-category]]

  * [[closed monoidal functor]]

  * [[internal hom]]

  * [[indexed closed monoidal category]]

  * [[cartesian closed category]], [[exponential object]]

* [[string diagram]], [[Kelly-Mac Lane diagram]], [[linguistics|natural language syntax]]

##References 

Textbook account for symmetric closed categories:

* {#Borceux94} [[Francis Borceux]], vol 2 section 6.1 of _[[Handbook of Categorical Algebra]]_, Cambridge University Press (1994)

Original articles studying monoidal biclosed categories are

* {#Lambek68} [[Joachim Lambek]], _Deductive systems and categories_, Mathematical Systems Theory 2 (1968), 287-318. 
 
* {#Lambek69} [[Joachim Lambek]], _Deductive systems and categories II_, Lecture Notes in Math. 86, Springer-Verlag (1969), 76-122. 

For more historical development see at _[linear type theory -- History of linear categorical semantics](linear+type+theory#HistoryCategoricalSemantics)_.

In [[enriched category theory]] the enriching category is taken to be closed monoidal. Accordingly the standard textbook on enriched category theory

* [[Max Kelly]], _Basic concepts of enriched category theory_, London Math. Soc. Lec. Note Series __64__, Cambridge Univ. Press 1982, 245 pp. ([ISBN:9780521287029](https://www.cambridge.org/de/academic/subjects/mathematics/logic-categories-and-sets/basic-concepts-enriched-category-theory?format=PB&isbn=9780521287029)); 

  republished as:

  Reprints in Theory and Applications of Categories, No. 10 (2005) pp. 1-136 ([tac:tr10](http://www.tac.mta.ca/tac/reprints/articles/10/tr10abs.html), [pdf](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf))

has a chapter on just closed monoidal categories.

See also the article

* {#EilenbergKelly65} [[Samuel Eilenberg]] and [[Max Kelly]], _Closed categories_.  Proc. Conf. Categorical Algebra (La Jolla, Calif., 1965).

on the concept of [[closed categories]].


[[!redirects closed monoidal category]]
[[!redirects closed monoidal categories]]
[[!redirects monoidal closed category]]
[[!redirects monoidal closed categories]]
[[!redirects closed monoidal structure]]
[[!redirects closed monoidal structures]]

[[!redirects closed symmetric monoidal category]]
[[!redirects closed symmetric monoidal categories]]
[[!redirects symmetric monoidal closed category]]
[[!redirects symmetric monoidal closed categories]]
[[!redirects closed symmetric monoidal structure]]
[[!redirects closed symmetric monoidal structures]]

[[!redirects biclosed monoidal category]]
[[!redirects biclosed monoidal categories]]
[[!redirects monoidal biclosed category]]
[[!redirects monoidal biclosed categories]]
[[!redirects left closed monoidal category]]
[[!redirects left closed monoidal categories]]
[[!redirects right closed monoidal category]]
[[!redirects right closed monoidal categories]]

[[!redirects hom-tensor adjunction]]
[[!redirects hom-tensor adjunctions]]
[[!redirects hom tensor adjunction]]
[[!redirects hom tensor adjunctions]]
