## Idea

Given a category $C$,
suppose $I$ is a set and $D_i\colon K_i\to C$
is a diagram in $C$ for each $i\in I$.
Denote by $E\colon\prod_i K_i\to C$ the diagram
obtained by composing the product of diagrams $\prod_i I_i\to C^I$
with the product functor $C^I\to C$.
We have a canonical comparison morphism $\mathop{\rm colim}E\to\prod_i\mathop{\rm colim}D_i$.
Colimits in&#160;$C$ _distribute over products_ if the comparison morphism is always an isomorphism.

## In sets

In the category of sets filtered colimits distribute over small products
and small colimits distribute over finite products.
However, reflexive coequalizers or sifted colimits do not distribute over infinite products.
See Example&#160;3.20 in&#160;[ARV].

## In algebraic categories

In any [[algebraic category]], i.e., the category of algebras over a small algebraic theory,
filtered colimits distribute over small products and sifted colimits distribute over finite products.
Generally speaking, small colimits do not distribute over finite products.
See Corollary&#160;3.21 in&#160;[ARV].

## In locally finitely presentable categories

In any [[locally finitely presentable category]], equivalently the category of algebras
over some finitary [[essentially algebraic theory]], filtered colimits distribute over small products.
See Theorem&#160;5.13 and Lemma&#160;5.14 in&#160;[ALR].

## For more general types of limits than products

Filtered (or sifted) colimits distribute over a given class of limits in a category&#160;$C$
if the canonical functor $\mathop{\rm Ind}(C)\to C$ (or $\mathop{\rm Sind}(C)\to C$) preserves this class of limits.
See Definition&#160;5.11 in&#160;[ALR].

Even more generally, one can prove
a distributivity theorem for any sound doctrine&#160;$D$ of limits, see Section&#160;6 in [ABLR].

## References

[ARV] J. Ad&#225;mek, J. Rosick&#253;, E. M. Vitale.
Algebraic theories.  A categorical introduction to general algebra.
CUP 2011.

[ALR] J.&#160;Ad&#225;mek, F.&#160;W.&#160;Lawvere, J.&#160;Rosick&#253;.
Continuous Categories Revisited.
TAC 11.

[ABLR] J. Ad&#225;mek, F.&#160;Borceux, S.&#160;Lack, J. Rosick&#253;.
A classification of accessible categories
JPAA 175.