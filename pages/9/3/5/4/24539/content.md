# Premulticategories

* toc
{: toc}

## Idea

A **premulticategory** is to a [[multicategory]] as a [[premonoidal category]] is to a [[monoidal category]].

## Definition

A definition of premulticategory is obtained by starting from a definition of [[multicategory]] in terms of the binary composition operations

$$ \circ_i : C(y_1,\dots,y_i, \dots,y_n; z) \times C(x_1,\dots,x_m; y_i) \to C(y_1,\dots,y_{i-1},x_1,\dots,x_n,y_{i+1},\dots,y_n;z) $$

and removing the "parallel associativity" or "commutativity" which says that composing $h\in C(y_1,\dots,y_n;z)$ with two morphisms $f\in C(x_1,\dots,x_n ; y_i)$ and $g\in C(w_1,\dots,w_p; y_j)$ can be done in either order.

A morphism $f$ is _central_ if for any $g$ and $h$ as above, the two methods of composition commute: $(h \circ f) \circ g = (h \circ g) \circ f$. So a premulticategory is a multicategory precisely if all morphisms are central.

## Relation to premonoidal categories

A premulticategory that has all tensor products and units, in a usual multicategorical sense, is equivalent to a [[premonoidal category]].

## References

* [[Sam Staton]] and [[Paul Blain Levy]], *Universal properties of impure programming languages*.  POPL '13: Proceedings of the 40th annual ACM SIGPLAN-SIGACT symposium on Principles of programming languages, 2013, [doi](https://doi.org/10.1145/2429069.2429091)

[[!redirects premulticategories]]
[[!redirects pre-multicategory]]
[[!redirects pre-multicategories]]
