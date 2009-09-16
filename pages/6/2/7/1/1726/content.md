<div class="rightHandSide toc">
[[!include higher category theory - contents]]
</div>


##Motivation

An ordinary [[complete Segal space]] is a model for an $(\infty,1)$-[[(infinity,1)-category|category]].

One may iterate this construction and define an $n$-fold complete Segal space as an complete Segal space in complete $(n-1)$-fold Segal spaces, roughly.

Then $n$-fold complete Segal spaces are models for $(\infty,n)$-[[(infinity,n)-category|categories]].

##Definition

Recall that a [[complete Segal space]] is to be thought of as the [[nerve]] of a category which is _[[homotopy coherent category theory|homotopically]]_ [[enriched category|enriched]] over [[Top]]: it is a simplicial object in [[Top]], $X^\bullet : \Delta^{op} \to Top$ satisfying some conditions and thought of as a model for an $(\infty,1)$-[[(infinity,1)-category|category]]. 

An $(\infty,n)$-category is in its essence the $(n-1)$-fold iteration of this process: recursively, it is a category which is _[[homotopy coherent category theory|homotopically]]_ [[enriched category|enriched]] over $(\infty,n-1)$-categories.

This implies then in particular that an $(\infty,n)$-category in this sense is an $n$-fold simplicial topological space
$$
  X_\bullet : \Delta^{op} \times 
     \Delta^{op} \times \cdots \times \Delta^{op}
     \to Top
$$

which satisfies the condition of [[complete Segal space|Segal spaces]] (characterizing nerves of categories, recall) in each variable, in that all the squares

$$
  \array{
     X_{m+n,\bullet} &\to& X_{n,\bullet}
     \\
     \downarrow && \downarrow
     \\
     X_{m,\bullet} &\to& X_{0,\bullet}
  }
$$

are [[homotopy coherent category theory|homotopy pullbacks]] of $(n-1)$-fold Segal spaces.


##References#

The definition is apparently due to the currently unpublished PhD thesis of Clark Barwick. It is being popularized and put to use in

* [[Jacob Lurie]], [[On the Classification of Topological Field Theories]]

A more detailed discussion of $(\infty,n)$-categories in terms of $n$-fold complete Segal spaces is in section 1 of

* [[Jacob Lurie]], _$(\infty,2)$-Categories and the Goodwillie Calculus I_ ([arXiv](http://arxiv.org/abs/0905.0462))

[[!redirects n-fold Segal space]]