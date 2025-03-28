
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### $(\infty,2)$-Topos theory
+--{: .hide}
[[!include (infinity,2)-topos theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

An _indexed category_ is a [[2-presheaf]].
 
When doing [[category theory]] relative to a  [[base topos]] $\mathcal{S}$ (or other more general sort of [[category]]), the objects of $\mathcal{S}$ are thought of as replacements for [[sets]].  Since often in category theory we need to speak of "a set-indexed family of objects" of some category, we need a corresponding notion in "category theory over $\mathcal{S}$."  An **$\mathcal{S}$-indexed category** is a [[category]] $\mathbb{C}$ together with, for every [[object]] $X\in \mathcal{S}$, a notion of "$X$-indexed family of objects of $\mathbb{C}$."

## Definition

Let $\mathcal{S}$ be a [[category]].

+-- {: .num_defn}
###### Definition

An **$\mathcal{S}$-indexed category** $\tilde \mathbb{C}$ is a category defined by a [[pseudofunctor]] 

$$
  \mathbb{C} : \mathcal{S}^{op}\to Cat
$$

from the [[opposite category]] of $\mathcal{S}$ to the [[2-category]] [[Cat]] of categories.

Under the [[Grothendieck construction]] [[equivalence of categories|equivalence]] this is equivalently a [[fibered category]] 

$$
  \array{
    \tilde \mathbb{C} \\ \downarrow \\ \mathcal{S}
  }
$$

over $\mathcal{S}$.

Similarly, an $\mathcal{S}$-[[indexed functor]] $\mathbb{C} \to \mathbb{D}$ is a [[pseudonatural transformation]] of pseudofunctors, and an indexed natural transformation is a [[modification]].  

This defines the [[2-category]] $\mathcal{S} IndCat \coloneqq [\mathcal{S}^{op}, Cat]$ of $\mathcal{S}$-indexed categories.


=--

This appears for instance as ([Johnstone, def. B1.2.1](#Johnstone)).

One may also call $\mathbb{C}$ a [[prestack]] in categories over $\mathcal{S}$.

Traditionally one writes the image of an object $X \in \mathcal{S}$ under $\mathbb{C}$ as $\mathbb{C}^X$ and calls it _the category of $X$-indexed families of objects of $\mathbb{C}$_.  Similarly, one writes the image of a [[morphism]] $u\colon X\to Y$ as $u^*\colon \mathbb{C}^Y\to \mathbb{C}^X$.

If $\mathcal{S}$ has a [[terminal object]] $*$ we think of $\mathbb{C}^*$ as the **underlying ordinary category** of the $\mathcal{S}$-indexed category $\mathbb{C}$. Part of the theory of indexed categories is about when and how to extend structures on $\mathbb{C}^*$ to all of $\mathbb{C}$.

A morphism of $S$-indexed categories is an [[indexed functor]].

## Examples

### Self indexing

+-- {: .num_example #CanonicalSelfIndexing}
###### Example
**(canonical self-indexing)**

If $\mathcal{S}$ has [[pullbacks]], then its [[codomain fibration]] is an $\mathcal{S}$-indexed category denoted $\mathbb{S}$. 

This assigns to an object $I$ the corresponding [[over-category]] 

$$
  \mathbb{S}^I \coloneqq \mathcal{S}/I
$$

and to a morphism $f : I \to J$ the functor $f^*$ that sends every $s \to I$ to its [[pullback]] $f^*$ along $f$.

=--

This indexed category represents $\mathcal{S}$ itself (or rather its [[codomain fibration]]) in the world of $\mathcal{S}$-indexed categories. 

### Base change

+-- {: .num_example #BaseChange}
###### Example
**(change of base)**

If $F\colon \mathcal{S}\to \mathcal{T}$ is a [[functor]] and $\mathbb{C}$ is a $\mathcal{T}$-indexed category, then we have an $\mathcal{S}$-indexed category $F^*\mathbb{C}$ defined by 

* $(F^*\mathbb{C})^I = \mathbb{C}^{F(I)}$ for every object $I \in \mathcal{S}$;

* and $x^* = F(x)^*$ for every morphism $x : I \to J$ in $\mathcal{S}$.

=--

### Indexed category of a functor

Combining these previous examples we get

+-- {: .num_example #CartesianFunctorIndexing}
###### Example

For $F : \mathcal{S} \to \mathcal{C}$ a functor and $\mathcal{C}$ a [[finitely complete category]], there is the $\mathcal{S}$-indexed category $F^* \mathbb{C}$ given by

* $(F^* \mathbb{C})^I = \mathcal{C}/F(I)$.

If the functor $F$ preserves [[pullback]]s then this induces a morphism $\mathbb{S} \to F^* \mathbb{C}$ of $\mathcal{S}$-indexed categories.

=--

### Indexed category of a topos over a base topos

This situation frequently arises when $\mathcal{S}$ and $\mathcal{C}$ are [[toposes]] and $F \coloneqq f^*$ is the [[inverse image]] part of a [[geometric morphism]].  

$$
  f 
  : 
  \mathcal{C}
   \stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}}
  \mathcal{S}
 \,.
$$

In this way, if $\mathcal{S}$ is a topos, then to be thought of as a _[[base topos]]_, then any topos *over* $\mathcal{S}$ (i.e. an object of the [[slice 2-category]] [[Topos]]$/S$) gives rise to a topos *relative to* $\mathcal{S}$, i.e. a "topos object" in the 2-category of $\mathcal{S}$-indexed categories, and this operation can be shown to be fully faithful. 

See [[base topos]] for more on this.


Also, via this indexed category, $f$ exhibits $\mathcal{C}$ as a [[2-sheaf]] (see there) over $\mathcal{C}$, with respect to the [[canonical topology]].

### Hyperdoctrine

* [[hyperdoctrine]]

### Indexed monoidal category

See also _[[indexed monoidal category]]_, _[[indexed closed monoidal category]]_ and  _[[dependent linear type theory]]_.

### Indexed $(\infty, 1)$-category

See _[[indexed (infinity, 1)-category]]_.

## Properties

### Extensions of adjunctions to indexed categories

+-- {: .num_prop}
###### Proposition

Let 

$$
  (L \dashv R) : 
   \mathcal{C} \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}} \mathcal{S}
$$ 

be a pair of [[adjoint functor]]s between 
[[finitely complete categories]]. Then $R$ extends to an $\mathcal{S}$-indexed functor

$$
  \mathbb{R} : \mathbb{C} \to \mathbb{S}
$$

where $\mathbb{S}$ is the self-indexing of $\mathcal{S}$ from example \ref{CanonicalSelfIndexing} and $\mathbb{C}$ is the base change indexing of $\mathcal{C}$ from example \ref{CartesianFunctorIndexing}.

By the general properties of adjunctions on [[overcategories]] (see there) we get for each $I \in \mathcal{S}$ an adjunction

$$
  (L/I \dashv R/I) : \mathbb{C}^I = \mathcal{C}/R(I) \to \mathcal{S}/I = \mathbb{S}^I
  \,.
$$

Here $\mathbb{R} : I \mapsto R/I$ is always a $\mathcal{S}$-indexed functor $\mathbb{C} \to \mathbb{S}$, and $\mathbb{L} : I \mapsto L/I$ is if $L$ preserves [[pullback]]s (by example \ref{CartesianFunctorIndexing}). If so, we have an $\mathcal{S}$-indexed adjunction

$$
  (\mathbb{L} \dashv \mathbb{R}) : 
  \mathbb{C} \to \mathbb{S}
$$

=--

This appears as ([Johnstone, lemma B1.2.3](#Johnstone)).

+-- {: .proof}
###### Proof

(...)

=--

### Well-powered indexed categories
 {#WellPoweredness}
 
+-- {: .num_defn}
###### Definition

An $\mathcal{S}$-indexed category $\mathbb{C}$ is called **well-powered** if the [[fibered category]] $\tilde \mathbb{C} \to \mathcal{S}$ corresponding to it under the [[Grothendieck construction]] has the property that the [[forgetful functor]]

$$
  U : Q(2, \tilde \mathbb{C})
   \to
  Rect(*,\tilde \mathbb{C})
$$

has a [[right adjoint]], where $Q(2,\tilde \mathbb{C})$ is the [[full subcategory]] of $Rect(2, \tilde \mathbb{C})$ on vertical [[monomorphism]]s.

=--

This appears as ([Johnstone, example. B1.3.14](#Johnstone)).

+-- {: .num_prop}
###### Proposition

Let $(L \dashv R) : \mathcal{C} \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}} \mathcal{S}$  be a pair of [[adjoint functor]]s such that $L$ preserves pullbacks. Then the $\mathcal{S}$-indexed category $\mathbb{C}$ is well powered if $\mathbb{S}$ is.

=--

This is ([Johnstone, prop. B1.3.17](#Johnstone)).


## Related concepts

* [[indexed functor]]

* [[indexed topos]]

* [[indexed Grothendieck construction]]

* [[indexed monoidal category]]

* [[hyperdoctrine]]

## References
  
The notion of *indexed categories* was introduced in

* {#Grothendieck60} [[Alexander Grothendieck]], §A.1 ([p. 3](http://www.numdam.org/item/SB_1958-1960__5__299_0.pdf#page=3)) of *Technique de descente et théorèmes d’existence en géométrie algébrique. I. Généralités. Descente par morphismes fidèlement plats*, Séminaire [[N. Bourbaki]] exp. no190 (1960) 299-327 &lbrack;[numdam:SB_1958-1960__5__299_0](http://www.numdam.org/item/?id=SB_1958-1960__5__299_0)&rbrack;

but under the name "[[fibered category]]" (*catégorie fibrée*) which later became the standard term, instead, for the ([equivalent](Grothendieck+construction#EquivalenceBetweenFiberedCategoriesAndPsuedofunctors)) [[Grothendieck construction]] on an indexed category, cf.:

* {#Bénabou1975} [[Jean Bénabou]], p. 898 (2 of 41) of: _Fibrations petites et localement petites_, C. R. Acad. Sci. Paris **281** Série A (1975) 897-900 &lbrack;[gallica](http://gallica.bnf.fr/ark:/12148/bpt6k6228235m/f171.image#)&rbrack;

An early monograph:

* [[P. T. Johnstone]], [[R. Paré]], [[R. D. Rosebrugh]], [[D. Schumacher]], [[R. J. Wood]], [[G. C. Wraith]], _Indexed Categories and Their Applications_, Lecture Notes in Mathematics **661** (1978) &lbrack;[doi:10.1007/BFb0061360](https://doi.org/10.1007/BFb0061360)&rbrack;

Early discussion in the context of [[categorical semantics]] in [[computer science]]:

* {#TBG91} [[Andrzej Tarlecki]], [[Rod M. Burstall]] [[Joseph A. Goguen]], *Some fundamental algebraic tools for the semantics of computation: Part 3. indexed categories*, Theoretical Computer Science **91** 2 (1991) 239-264 &lbrack;<a href="https://doi.org/10.1016/0304-3975(91)90085-G">doi:10.1016/0304-3975(91)90085-G</a>&rbrack;

Discussion in a context of [[topos theory]]:

* {#Johnstone} [[Peter Johnstone]], Section B1.2  in: _[[Sketches of an Elephant]]_ (2002)
 

[[!redirects indexed categories]]
