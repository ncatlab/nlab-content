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
obtained by composing the [[product]] of diagrams $\prod_i I_i\to C^I$
with the product functor $C^I\to C$.
We have a canonical comparison [[morphism]] $\mathop{\rm colim}E\to\prod_i\mathop{\rm colim}D_i$.
[[colimit|Colimits]] in&#160;$C$ _distribute over products_ if the comparison morphism is always an [[isomorphism]].

## In sets

In the category [[Set]] of sets [[filtered colimits]] distribute over small [[products]]
and small colimits distribute over [[finite products]].
However, [[reflexive coequalizers]] or [[sifted colimits]] do not distribute over infinite products. See Example&#160;3.20 in&#160;[ARV](#ARV).

## In algebraic categories

In any [[algebraic category]], i.e., the category of algebras over a small algebraic theory, [[filtered colimits]] distribute over small products and sifted colimits distribute over finite products.
Generally speaking, small colimits do not distribute over finite products.
See Corollary&#160;3.21 in&#160;[ARV](#ARV).

## In algebraically exact categories

In any [[algebraically exact category]], in particular,
in any [[variety]], sifted colimits distribute over small limits,
i.e., the functor $colim: Sind(C)\to C$ is continuous,
see Theorem&#160;3.11.(3) in [ALRalg](#ALRalg).

## In locally finitely presentable categories

In any [[locally finitely presentable category]], equivalently the category of algebras
over some finitary [[essentially algebraic theory]], filtered colimits distribute over small products.
See Theorem&#160;5.13 and Lemma&#160;5.14 in&#160;[ALR](#ALR).

## For more general types of limits than products

Filtered (or sifted) colimits distribute over a given class of limits in a category&#160;$C$
if the canonical functor $\mathop{\rm Ind}(C)\to C$ (or $\mathop{\rm Sind}(C)\to C$) preserves this class of limits.
See Definition&#160;5.11 in&#160;[ALR](#ALR).

Even more generally, one can prove
a distributivity theorem for any sound doctrine&#160;$D$ of limits, see Section&#160;6 in [ABLR](#ABLR).

## Related entries

* [[commutativity of limits and colimits]]

## References

* {#ARV} [[Jiří Adámek]], [[Jiří Rosický]], [[Enrico Vitale]], _Algebraic theories.  A categorical introduction to general algebra_ CUP 2011.

* {#ALR} [[Jiří Adámek]], [[William Lawvere]], [[Jiří Rosický]], _Continuous Categories Revisited_ TAC 11.

* {#ALRalg} [[Jiří Adámek]], [[William Lawvere]], [[Jiří Rosický]], _How algebraic is algebra_ TAC 8.

* {#ABLR} [[Jiří Adámek]], [[Francis Borceux]], [[Stephen Lack]], [[Jiří Rosický]], _A classification of accessible categories_ JPAA 175.
