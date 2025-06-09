
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea 

Every [[operad]] defines and is defined by a [[category]] -- its _category of operators_ -- whose

* [[object]]s are sequences consisting of colors of the operad; 

* [[morphism]]s are tuples consisting of maps of sets between these sequences of colors, and a $k$-ary operation of the operad for each collection of $k$ source colors that are mapped to the same target color.

This is a universal construction: the category of operators is the free [[semicartesian monoidal category]] on the free semicartesian operad on the given operad.  It also generalizes in a straightforward way to "colored operads", i.e. [[multicategories]].


## Definition

### For symmetric colored operads

Let $FinSet_{*}$ be the category of [[finite set|finite]] [[pointed set]]s. Write $\langle n \rangle = \{*, 1,2, \cdots, n\}$ for [[generalized the|the]] pointed set with $n+1$ elements. 

Let $A$ be a colored [[symmetric operad]] over [[Set]] ( hence a symmetric [[multicategory]]). Its **category of operators** is the [[category]]

* whose [[objects]] are finite sequences $(c_1, \cdots, c_n)$ of colors of $A$;

* whose [[morphisms]] $F : (c_1, \cdots, c_n) \to (d_1, \cdots, d_m)$ are given by a collection consisting of

  * a morphism $\phi : \langle n \rangle \to \langle m\rangle$ in $FinSet_*$;

  * for each $1 \leq i \leq m$ an operation

    $$
      f_i  \in Hom_A((c_k)_{k \in \phi^{-1}(i)}, d_i)
    $$

    from the objects whose indices are mapped to $i$ to the object $d_i$;

* composition is given componentwise by the composition in $FinSet_*$ and in $A$.

### $(\infty,1)$-Category of operators

The above definition has been [[vertical categorification|categorified]] to a notion of  [[(∞,1)-category]] of operators. See at _[[(∞,1)-operad]]_ for more.


## Properties

By construction, the category of operators $C_A$ of a symmetric colored operad is canonically equipped with a [[functor]] $p : C_A \to FinSet_*$.

From this functor, the original operad may be recovered up to canonical equivalence.

### Reconstruction of the operad

Given a functor $p : C_A \to FinSet_*$ from a category of operators of a symmetric colored operad, we reconstruct the operad $A$ as follows:

For $1 \leq i \leq n$ let

$$
  \rho^i : \langle n \rangle \to \langle 1 \rangle
$$

be the map that sends all elements to the point, except the element $i$.

Write $A_{n} := p^{-1}(\langle n\rangle)$ for the [[fiber]] of $p$ over $\langle n\rangle$. $A_1$ is the [[category]] underlying the operad $A$: the category whose morphisms are the unary operations of the operad.

The morphisms $\rho^i$ in $FinSet_*$ induce a functor

$$
  \prod_i \rho^i_* : A_n \to (A_1)^n
$$

which is an [[isomorphism]] that identifies $A_n$ with the $n$-fold cartesian [[product]] of the category $A_1$ with itself.

The morphisms $h \in Hom_A((c_1, \cdots, c_n), d)$ of $A$ are recovered as the collection of morphisms in $C_A$ from $(c_1, \cdots, c_n)$ to $(d)$ that cover the morphism $\langle n\rangle \to \langle 1\rangle$ in $FinSet_*$ whose [[preimage]] of the point contains just the point.


### Relation to underlying multicategories

Forming categories of operators is left 2-adjoint to forming the [[representable multicategory|underlying multicategory]] of a semi-cartesian monoidal category.  (For a left adjoint to the underlying multicategory of an arbitrary monoidal category, see instead  [[props]].)  For the moment, see there for more details.


## Related concepts

* The ([[syntactic category]] of) a (homogeneous) [[globular theory]] is the category of operators of a [[globular operad]].


## References

The notion originates in

* [[Peter May]], [[Robert Thomason]], _The uniqueness of infinite loop space machines_ , Topology  17(3) ([pdf](http://www.math.uchicago.edu/~may/PAPERS/22.pdf))

A discussion of the general logic behind the notion is at

* [[Mike Shulman]], _Generalized operads in classical algebraic topology_ 
([blog](http://golem.ph.utexas.edu/category/2009/10/generalized_operads_in_classic.html))

This summarizes aspects of

* G. Cruttwell, [[Mike Shulman]], _A unified framework for generalized multicategories_ ([arXiv:0907.2460](http://arxiv.org/abs/0907.2460))

See [example 11.20](https://arxiv.org/pdf/0907.2460v1#page=70) there (note that this example is missing from the final version of the paper).

[[!redirects categories of operators]]

[[!redirects (∞,1)-category of operators]]
[[!redirects (infinity,1)-category of operators]]
[[!redirects (∞,1)-categories of operators]]
[[!redirects (infinity,1)-categories of operators]]

