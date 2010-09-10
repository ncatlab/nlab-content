
# Direct sums and weak direct products
* table of contents
{: toc}

## Idea

The __direct sum__, or __weak direct product__, is a concept from algebra that actually makes sense in any [[category]] $C$ with [[zero morphisms]] (that is, any category enriched over the [[closed monoidal category]] of [[pointed sets]]), as long as the needed (co)[[limits]] exist.  In many cases, direct sums and weak direct products are the same, but not always.  Also in many cases, direct sums will be the same as [[coproducts]].  In any case, finitary weak direct products are the same as [[products]] but the infinitary versions are (almost always) different.


## Terminology

The name 'weak direct product' comes from the concept of [[direct product]] in algebra for a [[product]] in a [[concrete category]] that is created by the [[forgetful functor]]; the weak direct product will be a [[subobject]] of the direct product (and the entire direct product in finitary cases).  But here we will not restrict ourselves to the context of such a concrete category.

The term 'direct sum' comes from the finitary [[biproduct]] (simultaneously product and coproduct) in [[additive category|additive categories]].  The additive character of these biproducts extends in the infinitary case (where biproducts generally no longer appear) to the coproduct rather than to the product.  Even when the direct sum is not the same as the coproduct, it still retains some of this flavour.

In the classical examples of $C$, the direct sum and weak direct product are the same.  However, the general definitions below distinguish them in some cases, and we use the terms 'direct sum' and 'weak direct product' to best evoke the 'like a coproduct' and 'part of a product' senses.


## Definitions

Let $C$ be a category with [[zero morphisms]], and let $(A_i)_{i: I}$ be a family of objects of $C$ indexed by a [[set]] $I$.  Then ...


### Direct sum

... then consider the natural map $r$ from the [[coproduct]] $\coprod_i A_i$ to the product $\prod_i A_i$ that is defined in terms of the [[zero morphism]] as follows:
$$
  \left(
    A_i \to \coprod A \stackrel{r}{\to} \prod A \to A_j
  \right)
  =
  \left\{
    \array{
      Id_{A_i} & if i = j
      \\
      0_{ij} & if i \neq j
    ,}
  \right.
  \,
$$
where $0_{ij}$ is the zero morphism from $A_i$ to $A_j$.

Then if $C$ is a [[regular category]] or otherwise has a good concept of [[image]], we define the __direct sum__ $\bigoplus_i A_i$ to be the image of the map $r$.

In [[constructive mathematics]], the definition of $r$ requires that the index set $I$ have [[decidable equality]], which is the case in most applications of interest.  An arbitrary index set will still work if $C$ is enriched over the category of sets and [[partial functions]]; this may be embedded as a [[full subcategory]] of the category of pointed sets, and the embedding is an [[equivalence of categories]] if and only if the law of [[excluded middle]] holds.  But the usual examples of $C$ are not (constructively) so enriched.  Fortunately, the usual examples of $I$ have decidable equality.


### Weak direct product

... then consider the finitary [[products]]
$$ \prod_{i \in F} A_i $$
as $F$ varies over the [[finite set|finite subsets]] of the index set $I$.  (In [[constructive mathematics]], use the 'finitely indexed' or 'Kuratowski' notion of finiteness here ... although if $I$ has [[decidable equality]], as is the case in the usual examples, then every finitely indexed subset of $I$ is actually finite in the strictest sense.)

These finite products form a [[directed limit|direct system]] indexed by the [[direction|directed set]] $\mathcal{P}_{fin}I$ of finite subsets of $I$ (ordered by inclusion) with the map
$$ \prod_{i \in F} A_i \to \prod_{i \in G} A_i ,$$
where $F \subseteq G$, given by
$$ \prod_{i \in F} A_i \cong \prod_{i \in F} A_i \times \prod_{i \in G \setminus F} 1 \stackrel{(id, 0)}{\to} \prod_{i \in F} A_i \times \prod_{i \in G \setminus F} A_i \cong \prod_{i \in G} A_i .$$

Then if it exists, the __weak direct product__ $\prod^wk_i A_i$ is defined to be the [[directed limit|directed colimit]] of this direct system.


## Examples

In [[Grp]] or [[Ab]], the direct sum and weak direct product agree.  For finitely many objects, it is the same as the [[direct product]], which is the [[product]] in both categories.  In $Ab$, where finite products are also finite [[coproducts]], the direct sum continues to be the coproduct, while in $Grp$, it lies between the coproduct (the [[free product]]) and the product.

In these examples, the direct sum can also be described in more elementary terms as a [[subgroup]] of the direct product:
$$ \bigoplus_{i: I} A_i = \{ (a_i)_i \;|\; ess \forall (i: I),\; a_i = 0 \} ,$$
where '$ess \forall$' means 'for all but finitely many'.  This makes it clear that the direct sum equals the direct product when there are only finitely many objects involved.

In the category of [[pointed sets]], the direct sum and weak direct product are different.  The weak direct product is still given as a pointed subset of the direct product as above.  The direct sum, on the other hand, is the same as the [[wedge sum]], which is the same as the coproduct in this category.  Even for $2$ pointed sets, this is different from the weak direct product (which is, as always, the same as the product for finitely many objects).


## Discussion

OK, so which of these is correct for [[pointed sets]]?  In particular, given pointed sets $A$ and $B$ (where in each we call the basepoint $0$), do we want the wedge sum $A \vee B$ (the image of the coproduct in the product) or the direct product $A \times B$ (the product, since there are only $2$ sets)?  I can turn either into a general definition above, but which is the right one?

Or should we use both?  There are, after all, two names: 'direct sum' and 'weak direct product'; I naturally use these for the image-of-coproduct and almost-zero-product versions, respectively.  Is there already a convention in universal algebra?  If not, do people like this terminology?  Or do you know that one is definitely what is wanted while the other is useless?

---[[Toby Bartels]]

[[Mike Shulman|Mike]]: I've only ever heard "direct sum" used to mean "coproduct," or sometimes "finite biproduct," in an [[additive category]].

_Toby_:  Well, it\'s definitely also used in the sense of [direct sum of groups](http://secure.wikimedia.org/wikipedia/en/wiki/Direct_sum_of_groups); the same concept is also called 'weak direct product'.  I thought that I once knew how this worked in general, from a universal-algebra perspective, but when I started writing this, I found that I had forgotten (or never really understood) ....


[[!redirects direct sum]]
[[!redirects direct sums]]

[[!redirects weak direct product]]
[[!redirects weak direct products]]
