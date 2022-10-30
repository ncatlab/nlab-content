[[!redirects distributivity of colimits over limits]]
[[!redirects distributivity of products and colimits]]
[[!redirects distributivity of products and colimits]]
[[!redirects distributivity of products and colimits]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Given a [[category]] $C$,
suppose $I$ is a [[set]] and $D_i\colon K_i\to C$
is a [[diagram]] in $C$ for each $i\in I$.
Denote by $E\colon\prod_i K_i\to C$ the diagram
obtained by composing the [[product]] of diagrams $\prod_i D_i: \prod_i K_i \to C^I$ with the product functor $C^I\to C$.
We have a canonical comparison [[morphism]] $colim E \to \prod_i colim D_i$.
[[colimit|Colimits]] in&#160;$C$ _distribute over products_ if the comparison morphism is always an [[isomorphism]].

## In sets

In the category [[Set]] of sets small [[limits]]
distribute over [[sifted colimits]]
and [[finite products]] distribute over small [[colimits]].

## In precontinuos categories and locally finitely presentable categories

According to Definition 5.11 in [ALR](#ALR),
a category is _precontinuous_
if it admits small limits and filtered colimits,
and small limits distribute over filtered colimits,
i.e., the functor $colim: Ind(C)\to C$ is continuous.
Here Ind denotes the free cocompletion with respect
to filtered colimits.

In particular, any [[locally finitely presentable category]], equivalently the category of algebras
over some finitary [[essentially algebraic theory]],
is precontinuous.
See Theorem 5.13 and Lemma 5.14 in [ALR](#ALR).

## In algebraically exact categories and varieties of algebras

According to Definition 4.5 in [ALRalg](#ALRalg),
a category is _algebraically exact_
if it admits small limits and sifted colimits,
and small limits distribute over sifted colimits,
i.e., the functor $colim: Sind(C)\to C$ is continuous.
Here Sind denotes the free cocompletion with respect
to sifted colimits in complete analogy to Ind, the free
cocompletion with respect to filtered colimits.

In particular (Example 5.3 in [ALRalg](#ALRalg)),
any [[variety of algebras]]
is an algebraically exact category.

In fact, as shown in [ALRalg](#ALRalg), algebraically exact
categories with continuous functors that preserve sifted colimits
form the accessible [[equational hull]] of the bicategory
of [[varieties of algebras]] and continuous functors
that preserve sifted colimits.

Generally speaking, small colimits do not distribute over finite products.

## For more general types of limits than products

Even more generally, one can prove
a distributivity theorem for any sound doctrine&#160;$D$ of limits, see Section&#160;6 in [ABLR](#ABLR).

## Related entries

* [[commutativity of limits and colimits]]

## References

* {#ARV} [[Jiří Adámek]], [[Jiří Rosický]], [[Enrico Vitale]], _Algebraic theories.  A categorical introduction to general algebra_ CUP 2011.

* {#ALR} [[Jiří Adámek]], [[William Lawvere]], [[Jiří Rosický]], _Continuous Categories Revisited_ TAC 11.

* {#ALRalg} [[Jiří Adámek]], [[William Lawvere]], [[Jiří Rosický]], _How algebraic is algebra_ TAC 8.

* {#ABLR} [[Jiří Adámek]], [[Francis Borceux]], [[Stephen Lack]], [[Jiří Rosický]], _A classification of accessible categories_ JPAA 175.
