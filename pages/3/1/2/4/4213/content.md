
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

_Doctrinal Adjunction_ is the title of a 1974 paper ([Kelly](#Kelly)) that gives conditions under which [[adjunction|adjoint morphisms]] $f \dashv u$ in a [[2-category]] $K$, and additionally the unit and counit, may be lifted to $T$-$Alg_l$, for some [[2-monad]] $T$ on $K$.  

Here $T$-$Alg_l$ is the 2-category of strict $T$-algebras, lax $T$-morphisms and $T$-transformations, but the result works as well for pseudo algebras.


## Statement

+-- {: .un_theorem}
###### Theorem

Let $f \dashv u$ be an [[adjunction]] in some [[2-category]] $K$ and let $T$ be a [[2-monad]] on $K$.

There is a [[bijection]] between [[2-morphism]]s $\bar u$ making $(u,\bar u)$ a lax $T$-morphism and 2-morphisms $\tilde f$ making $(f,\tilde f)$ a colax $T$-morphism; it is given by taking [[mates]] with respect to the adjunctions $T f \dashv T u$ and $f \dashv u$.

=--

The proof ([Kelly](#Kelly))
relies solely on the properties of the mate correspondence.

+-- {: .un_proposition}
###### Proposition

For the unit and counit of the adjunction $f \dashv u$ to be $T$-transformations, and hence for the adjunction to live in $T$-$Alg_l$, it is necessary and sufficient that $\tilde f$ have an inverse $\bar f$ that makes $(f,\bar f)$ into a lax $T$-morphism, and hence $(f,\bar f)$ into a strong $T$-morphism.

=--

Again, the proof hinges on the properties of mates:  we take the conditions for the unit and counit to be $T$-transformations and pass to mates wrt $T f \dashv T u$ and $1 \dashv 1$.  Noting that $\tilde f$ is the mate of $\bar u$, the conditions are seen to be equivalent to requiring that $\bar f$ and $\tilde f$ are mutually inverse.

It follows that 

+-- {: .un_prop}
###### Proposition

$(f, \bar f) \dashv (u, \bar u)$ in $T$-$Alg_l$ if and only if $f \dashv u$ in $K$ and $\bar f$ has inverse $\tilde f$ = the mate of $\bar u$.

=--


## In terms of double categories

Doctrinal adjunction can be stated cleanly in terms of [[double categories]].  Namely, for any 2-monad $T$ there is a double category  $T$-**Alg** whose objects are $T$-algebras, whose horizontal arrows are lax $T$-morphisms, whose vertical arrows are colax $T$-morphisms, and whose 2-cells are 2-cells in the base 2-category $K$ that make a certain cube commute.  The horizontal 2-category of this double category is $T$-$Alg_l$, and its vertical 2-category is $T$-$Alg_c$.  There is an obvious forgetful double functor $T \mathbf{Alg} \to \mathbf{Sq}(K)$, where $\mathbf{Sq}(K)$ is the double category of squares or "quintets" in $K$.

It is straightforward to verify that a [[conjunction]] in the double category $T$-**Alg** is precisely an adjunction in $K$ between $T$-algebras whose left adjoint is colax, whose right adjoint is lax, and for which the lax and colax structure maps are mates under the adjunction -- i.e. a "doctrinal adjunction" in the above sense.  Furthermore, an arrow in $T$-**Alg** has a [[companion]] precisely when it is a *strong* (= pseudo) $T$-morphism.  The two central results of Kelly's paper can then be stated as:

1. The forgetful double functor $U\colon T \mathbf{Alg} \to \mathbf{Sq}(K)$ creates conjunctions.  I.e. given a horizontal arrow $u$ in $T \mathbf{Alg}$ and a left conjoint $f$ of $U(u)$ (i.e. a left adjoint of $u$ in $K$), there is a unique left conjoint of $u$ in $T\mathbf{Alg}$ lying over $f$.

1. Let $f\colon A\to B$ be a vertical arrow in $T \mathbf{Alg}$ (i.e. a colax $T$-morphism) and let $f'\colon A\to B$ and $u\colon B\to A$ be horizontal arrows (i.e. lax $T$-morphisms).  Then from any two of the following three data we can uniquely construct the third.
   1. Data making $f'$ a horizontal companion of $f$;
   1. Data making $u$ a right conjoint of $f$;
   1. Data making $f'$ a left adjoint of $u$ in the horizontal 2-category.

Of these, the second is actually a general statement about companions and conjoints in any double category.  Of course, the first is a special property of the forgetful double functor from the double category of $T$-algebras.


## Examples

### Monoidal categories

Let $K = $ [[Cat]] and $T$ the 2-monad whose 2-algebras are [[monoidal categories]]. Then 

* a lax $T$-morphism  is a [[lax monoidal functor]];

* an oplax $T$-morphism is an [[oplax monoidal functor]].

The above theorem then asserts

+-- {: .un_corollary}
###### Corollary

For two [[adjoint functor]]s $(L \dashv R)$ between monoidal categories, $L$ is oplax monoidal precisely if $R$ is lax monoidal.

=--

See [[oplax monoidal functor]] for more details.


## References

* [[Max Kelly]], _Doctrinal Adjunction_ (1974)
{#Kelly}
