#Idea#

Combining the idea of [[(infinity,1)-category]] with that of [[n-category]], an $(\infty,n)$-category is supposed to be an [[infinity-category]] which behaves like its $k$-morphisms for $k \gt n$ are all [[equivalence]]s. See [[(n,r)-category]].

#Idea in terms of complete Segal spaces#

One definition buidling on that of [[(infinity,1)-category]] in terms of [[complete Segal space]]s was recently proposed by Jacob Lurie ( [p. 34](http://www-math.mit.edu/~lurie/papers/cobordism.pdf#page=34)).

Essentially, in this definition an $(\infty,n)-category$ is an $n$-fold simplicial topological space

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