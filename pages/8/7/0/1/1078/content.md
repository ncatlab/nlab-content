
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


# Direct sums and weak direct products
* table of contents
{: toc}

## Idea

The notion of __direct sum__, or __weak direct product__, is a concept from [[algebra]] that actually makes sense in any [[category]] $C$ with [[zero morphisms]] (that is, any category [[enriched category|enriched]] over the [[closed monoidal category]] of [[pointed sets]]), as long as the needed ([[colimit|co]])[[limits]] exist.  

A basic and familiar example is the direct sum $V_1 \oplus V_2$  of two [[vector spaces]] $V_1$ and $V_2$ over some [[field]], or, more generally of two [[modules]] over some [[ring]]. Generally, for $I$ a set and $\{V_i\}_{i \in I}$ an $I$-indexed family of vector space or modules, their direct sum $\bigoplus_{i \in I} V_i$ is the collection of [[formal linear combinations]] of elements in each of the $V_i$. This may in part motivate the terminology: _an element in a direct sum is a sum of elements_, at least in these cases.

This generalises in two distinct ways, which we call _direct sums_ and _weak direct products_.  In many cases (as in the example above), these coincide, but not always.  Also in many cases, direct sums will be the same as [[coproducts]].  In any case, finitary weak direct products are the same as [[products]] but the infinitary versions are (almost always) different.


## Terminology

The name 'weak direct product' comes from the concept of [[direct product]] in [[algebra]] for a [[product]] in a [[concrete category]] that is created by the [[forgetful functor]]; the weak direct product will be a [[subobject]] of the direct product (and the entire direct product in finitary cases).  But here we will not restrict ourselves to the context of such a concrete category.

The term 'direct sum' comes from the finitary [[biproduct]] (simultaneously product and coproduct) in [[additive category|additive categories]].  The additive character of these biproducts extends in the infinitary case (where biproducts generally no longer appear) to the coproduct rather than to the product.  Even when the direct sum is not the same as the coproduct, it still retains some of this flavour.

In the classical examples of $C$, the direct sum and weak direct product are the same.  However, the general definitions below distinguish them in some cases, and we use the terms 'direct sum' and 'weak direct product' to best evoke the 'like a coproduct' and 'part of a product' senses.


## Definitions

Let $\mathcal{C}$ be a [[category]] with [[products]] and [[coproducts]], as well as [[zero morphisms]].  Let $I$ be a [[set]], and let $(A_i)_{i \in I}$ be an $I$-indexed [[family]] of [[objects]] in $\mathcal{C}$, hence a [[function]] $A : I \to Obj(\mathcal{C})$.

We now define both the direct sum and weak direct product of this family.  The $A_i$ will be called the __direct summands__ or (weak) __direct factors__.


### Direct sum

Here we must assume moreover that $\mathcal{C}$ is a [[regular category]] (or otherwise has a good concept of [[image]]). 

+-- {: .num_defn}
###### Definition

Let $r$ be the morphism from the [[coproduct]] $\coprod_i A_i$ to the [[product]] $\prod_i A_i$ characterized by having the following components

$$
  \left(
    A_i \to \coprod A \stackrel{r}{\to} \prod A \to A_j
  \right)
  =
  \left\{
    \array{
      Id_{A_i} & if\; i = j
      \\
      0_{ij} & if\; i \neq j
    ,}
  \right.
  \,
$$

where $0_{ij}$ is the [[zero morphism]] from $A_i$ to $A_j$.

The __direct sum__ over the family $\{A_i\}$ is the [[image]] 

$$
  \coprod_i A_i \overset{\coim r}\to \bigoplus_i A_i \overset{\im r}\to \prod_i A_i
$$

of the morphism $r$.

=--

+-- {: .num_remark}
###### Remark

In [[constructive mathematics]], the definition of $r$ requires that the index set $I$ have [[decidable equality]], which is the case in most applications of interest.  An arbitrary index set will still work if $\mathcal{C}$ is [[enriched category|enriched]] over the category of sets and [[partial functions]]; this may be embedded as a [[full subcategory]] of the category of pointed sets, and the embedding is an [[equivalence of categories]] if and only if the law of [[excluded middle]] holds.  But the usual examples of $\mathcal{C}$ are not (constructively) so enriched.  Fortunately, the usual examples of $I$ have decidable equality.

=--

### Weak direct product

Here we consider the finitary [[products]]
$$ \prod_{i \in F} A_i $$
as $F$ varies over the [[finite set|finite subsets]] of the index set $I$.  (In [[constructive mathematics]], use 'finitely indexed' or '[[Kuratowski finite]]' here ... although if $I$ has [[decidable equality]], as is the case in the usual examples, then every finitely indexed subset of $I$ is actually finite in the strictest sense.)

These finite products form a [[directed limit|direct system]] indexed by the [[direction|directed set]] $\mathcal{P}_{fin}I$ of finite subsets of $I$ (ordered by inclusion) with the map
$$ \prod_{i \in F} A_i \to \prod_{i \in G} A_i ,$$
where $F \subseteq G$, given by
$$ \prod_{i \in F} A_i \cong \prod_{i \in F} A_i \times \prod_{i \in G \setminus F} 1 \stackrel{(id, 0)}{\to} \prod_{i \in F} A_i \times \prod_{i \in G \setminus F} A_i \cong \prod_{i \in G} A_i .$$

+-- {: .num_defn}
###### Definition

If it exists, the __weak direct product__ $\prod^wk_i A_i$ is defined to be the [[directed limit|directed colimit]] of this direct system.
=--


## Examples


+-- {: .num_example}
###### Example

In the categories [[Grp]] or [[Ab]] of ([[abelian group|abelian]]) [[groups]], the direct sum and weak direct product agree.  For finitely many objects, it is the same as the [[direct product]], which is the [[product]] in both categories.  

=--

+-- {: .num_remark}
###### Remark

In [[Ab]], where finite products are also finite [[coproducts]], the direct sum continues to be the coproduct, while in [[Grp]], it lies between the coproduct (the [[free product]]) and the product.

So in [[Ab]] the direct sum is the object equipped with a collection of morphisms

\begin{center}
\begin{tikzcd}
A_j \arrow[rd, "\iota_j"'] & \dots                   & A_k \arrow[ld, "\iota_k"] \\
                           & \bigoplus_{i \in I} A_i &                          
\end{tikzcd}
\end{center}

which is characterized up to unique [[isomorphism]] by the following [[universal property]]: for every other abelian group $K$ equipped with maps 

\begin{center}
\begin{tikzcd}
A_j \arrow[rd, "f_j"'] & \dots & A_k \arrow[ld, "f_k"] \\
                       & K     &                      
\end{tikzcd}
\end{center}

there is a unique homomorphism $\phi : \bigoplus_{i \in I} A_i \to K$ such that 
$ f_i = \phi \circ \iota_i$ for all $i \in I$.

=--





+-- {: .num_prop}
###### Proposition

In these examples, the direct sum can also be described in more elementary terms as a [[subgroup]] of the direct product:

$$ 
  \bigoplus_{i: I} A_i = 
  \left\{ 
    (a_i)_{i : I} \;|\; ess \forall (i: I),\; a_i = 0 
   \right\} 
  \,,
$$

where '$ess \forall$' means 'for all but finitely many'.  This makes it clear that the direct sum equals the direct product when there are only finitely many objects involved.

For $\mathcal{C} = $ [[Ab]], $R$[[Mod]] this is the group of [[formal linear combinations]] of elements in the summands.

=--


+-- {: .num_example}
###### Example

For $R$ a [[ring]], the direct sums in the category $R$[[Mod]] or [[modules]] over $R$ are given by those on the underlying abelian groups.

=--


+-- {: .num_example}
###### Example

In the category of [[pointed sets]], the direct sum and weak direct product are different.  The weak direct product is still given as a pointed subset of the direct product as above.  The direct sum, on the other hand, is the same as the [[wedge sum]], which is the same as the coproduct in this category.  Even for $2$ pointed sets, this is different from the weak direct product (which is, as always, the same as the product for finitely many objects).

=--

+-- {: .num_example}
###### Example

In the category of [[Banach spaces]] (with [[short linear maps]]), the direct sum is the $l^1$ direct sum, while the weak direct product is the $l^\infty$ direct sum.  (There is in fact a range of $l^p$ direct sums for $1 \leq p \leq \infty$, although I don\'t know what if any [[universal properties]] they all satisfy.)  In this case, the direct sum is the same as the coproduct, while the weak direct product is the same as the product even for infinitely many objects.  See [[direct sum of Banach spaces]].

=--


## Internal direct sums
 {#InternalDirectSum}

Given an object $B$ and a [[family]] of [[subobjects]] $A_i$ of $B$ (or more generally a family of morphisms $A_i \to B$, or equivalently a map $\coprod_i A_i \to B$), suppose that the direct sum $\bigoplus_i A_i$ exists.  Suppose further that the map $\coprod_i A_i \to B$ factors through the map $\coprod_i A_i \to \bigoplus_i A_i$ (which means that it factors uniquely if $\coprod_i A_i \to \bigoplus_i A_i$ is an [[epimorphism]], as it must be in a [[regular category]]).  Finally, suppose that the (or a) [[quotient map]] $\bigoplus_i A_i \to B$ is an [[isomorphism]].  Then we say that $B$ is the __[[internal direct sum]]__ of the $A_i$.

In contrast, the abstractly defined direct sum $\bigoplus_i A_i$ may be called an __external direct sum__.  These terms are usually used with [[concrete categories]] where the $A_i$ may either be given independently (for an external direct sum) or as [[subsets]] of some ambient space (either $B$ or something of which $B$ is a subset) for an internal direct sum.  In too abstract a context, there is no difference: on the one hand, any internal direct sum is a fortiori isomorphic to any external direct sum; on the other hand, given an external direct sum, there is a natural map $\coprod_i A_i \to \bigoplus_i A_i$, relative to which the external direct sum is an internal direct sum.


## Related concepts

* [[direct sum of vector bundles]]/[[Whitney sum]]

* [[additive disjunction]], [[quantum parallelism]]

## References

* [[Masaki Kashiwara]], [[Pierre Schapira]]: Ntn. 8.2.5 in: *[[Categories and Sheaves]]*, Grundlehren der Mathematischen Wissenschaften __332__, Springer (2006) &lbrack;[doi:10.1007/3-540-27950-4](https://link.springer.com/book/10.1007/3-540-27950-4), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/kashiwara2.pdf)&rbrack;



[[!redirects direct sum]]
[[!redirects direct sums]]

[[!redirects direct summand]]
[[!redirects direct summands]]

[[!redirects external direct sum]]

[[!redirects weak direct product]]
[[!redirects weak direct products]]

[[!redirects direct sum of groups]]
[[!redirects direct sums of groups]]

[[!redirects direct sum of abelian groups]]
[[!redirects direct sums of abelian groups]]

[[!redirects direct sum of vector spaces]]
[[!redirects direct sums of vector spaces]]

