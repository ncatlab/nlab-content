#Idea#

Combining the idea of [[(infinity,1)-category]] with that of [[n-category]], an $(\infty,n)$-category is supposed to be an [[infinity-category]] which behaves like its $k$-morphisms for $k \gt n$ are all [[equivalence]]s. See [[(n,r)-category]].

#Idea in terms of complete Segal spaces#

One definition buidling on that of [[(infinity,1)-category]] in terms of [[complete Segal space]]s was given in 2005 by Clark Barwick and recently put to use and popularized by Jacob Lurie ( [p. 34](http://www-math.mit.edu/~lurie/papers/cobordism.pdf#page=34)).

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

#Examples#

The motivating example for $(\infty,n)$-categories is the [[(infinity,n)-category of cobordisms]] which plays a central role in the formalization of the [[generalized tangle hypothesis]].