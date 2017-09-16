An ordinary [[complete Segal space]] is a model for an [[(infinity,1)-category]].

One may iterate this constructoin and define an $n$-fold complete Segal space as an complete Segal space in complete $(n-1)$-fold Segal spaces, roughly.

$n$-fold complete Segal spaces are models for [[(infinity,n)-category|(infinity,n)-categories]].

Recall that a [[complete Segal space]] is to be thought of as the nerve of a category which is _[[homotopy coherent category theory|homotopically]]_ [[enriched category|enriched]] over [[Top]]: it is a simplicial object in [[Top]], $X^\bullet : \Delta^{op} \to Top$ satisfying some conditions and thought of as a model for an [[(infinity,1)-category]]. 

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

#References#

The definition is apparently due to the currently unpublished PhD thesis of Clark Barwick. It is being popularized and put to use in

* [[Jacob Lurie]], [[On the Classification of Topological Field Theories]]