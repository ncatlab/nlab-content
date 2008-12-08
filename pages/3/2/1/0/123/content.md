A functor is what goes between [[category|categories]].

More precisely, a _functor_ $F$ from a category $C$ to a category $D$ is a map sending each object $x \in C$ to an object $F(x) \in D$ and each morphisms $f : x \to y$ in $C$ to morphism $F(f) : F(x) \to F(y)$ in $D$.  We demand that:

* $F$ preserves [[composition]]: $F(f g) = F(f) F(g)$ whenever either side is well-defined.

* $F$ preserves identity morphisms: for each object $x \in X$, $F(1_x) = 1_{F(x)}$.

Functors are morphisms in the category [[Cat]].

