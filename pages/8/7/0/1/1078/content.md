The __direct sum__, or __weak direct product__, is a concept from algebra that actually makes sense in any [[category]] with [[zero morphism]]s (that is, any category enriched over the [[closed monoidal category]] of [[pointed set]]s).  Note that finitary direct sums are the same as [[product]]s; the infinitary versions are different.

# Terminology #

The name 'weak direct product' comes from the concept of [[direct product]] in algebra for a [[product]] in a [[concrete category]] that is created by the [[forgetful functor]].  Here we will not restrict ourselves to that context.

The term 'direct sum' comes from the (finitary) [[biproduct]] (simultaneously product and coproduct) in [[additive category|additive categories]].  The additive character of these biproducts extends in the infinitary case (where biproducts generally no longer appear) to the direct sum rather than to the product.  (In these cases, the direct sum is often still a [[coproduct]], but the importance of coproducts in algebra was not evident as early.)

# Definition #

Let $C$ be a category with [[zero morphism]]s, and let $(A_i)_{i: I}$ be a family of objects of $C$ indexed by a [[set]] $I$.  Then ...

+--{: .query}
I\'m not sure what to do now.  Let\'s look at some examples.
=--

# Special cases #

In [[Grp]] or [[Ab]], the direct sum of finitely many [[group]]s is the same as the [[direct product]], which is the [[product]] in both categories.  The direct sum of infinitely many groups, however, will not be the product.  In $Ab$, where finite products are also finite [[coproduct]]s, the direct sum continues to be the coproduct, while in $Grp$, it lies between the coproduct (the [[free product]]) and the product in the sense that there exist natural maps
$$ \bigstar_{i: I} A_i \to \bigoplus_{i: I} A_i \to \prod_{i: I} A_i .$$

In fact, we can say in both cases that the direct sum is the [[direct image]] of the natural map from the coproduct to the product that is defined in terms of the [[zero morphism]] as follows:
$$
  \left(
    A_i \to \bigsqcup_i A_i \stackrel{r}{\to} \prod_i A_i \to A_j
  \right)
  =
  \left\{
    \array{
      Id_{A_i} & if i = j
      \\
      0 & if i \neq j
    }
  \right.
  \,
$$

In these examples, the direct sum can also be described in more elementary terms as a [[subgroup]] of the [[direct product]]:
$$ \bigoplus_{i: I} A_i = \{ (a_i)_i \;|\; ess \forall (i: I),\; a_i = 0 \} ,$$
where '$ess \forall$' means 'for all but finitely many'.  This makes it clear that the direct sum equals the direct product when there are only finitely many objects involved.

In the category of [[pointed set]]s, ...

+--{: .query}
OK, so which of these is correct for [[pointed set]]s?  In particular, given pointed sets $A$ and $B$ (where in each we call the basepoint $0$), is the direct sum $A \oplus B$ the [[wedge sum]] $A \vee B$ (the image of the coproduct in the product) or the product $A \times B$ (since there are only $2$ sets)?  I can turn either into a general definition above, but which is the right one?

Or should we use both?  There are, after all, two names: 'direct sum' and 'weak direct product'; I\'d naturally use these for the image-of-coproduct and almost-zero-product versions, respectively.  Is there already a convention in universal algebra?  If not, do people like this terminology?  Or do you know that one is definitely what is wanted while the other is useless?

---[[Toby Bartels]]
=--