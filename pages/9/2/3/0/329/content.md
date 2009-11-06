#Idea

* A strict 2-category is a [[directed n-graph|directed 2-graph]] equipped with a composition operation on adjacent 1-cells and 2-cells which is strictly unital and associative.

* The concept of a strict 2-category is the simplest generalization of a [[category]] to a [[higher category theory|higher category]]. It is the one-step [[vertical categorification|categorification]] of the concept of a category.

#Definition

A _strict 2-category_, often called simply a _2-category_, is a [[enriched category|category enriched over]] [[Cat]]. 

+--{.query}
[[Eric]]: Could someone spell this out in a little more detail?

[[Finn Lawler|Finn]]: See **Details** below for a first attempt.
=--

Similarly, a [[strict 2-groupoid]] is a groupoid enriched over groupoids. This is also called a [[geometric shapes for higher structures|globular]] strict 2-groupoid, to emphasise the underlying geometry. The category of strict 2-groupoids is eqivalent to the category  of [[crossed module]]s over groupoids. It is also equivalent to the category of (strict) double groupoids with connections. 

They are also special cases of strict globular omega-groupoids, and the category of these is equivalent to the category of [[crossed complex]]es. 

#Details

Working out the meaning of '$Cat$-enriched category', we find that a 2-category $K$ is given by

* a collection $ob K$ of objects $a,b,c,\ldots$, together with
* a hom-[[category]] $K(a,b)$ for each $a,b$, and
* a [[functor]] $1_a : \mathbf{1} \to K(a,a)$ and a functor $comp : K(b,c) \times K(a,b) \to K(a,c)$

satisfying associativity and identity axioms (given [[enriched category|here]]).

As for ordinary ($Set$-enriched) categories, an object $f \in K(a,b)$ is called a _morphism_ or _1-cell_ from $a$ to $b$ and written $f:a\to b$ as usual.  But given $f,g:a\to b$, it is now possible to have non-trivial arrows $\alpha:f\to g \in K(a,b)$, called _2-cells_ from $f$ to $g$ and written as $\alpha : f \Rightarrow g$.  Because the hom-objects $K(a,b)$ are by definition categories, 2-cells carry an associative and unital operation called _vertical composition_.

The functor $1_a$ simply picks an endo-1-cell that serves as the identity arrow of $a$.  Composition is more interesting: 1-cells can be composed as usual, but because $comp$ is a functor we get two extra things:

* an operation of _horizontal composition_ on 2-cells.  Functoriality of $comp$ then says that given $\alpha : f \Rightarrow g : a\to b$ and $\beta : f' \Rightarrow g' : b\to c$, the composite $\comp(\beta,\alpha)$ is a 2-cell $\beta \alpha : f'f \Rightarrow g'g : a \to c$.

* the _interchange law_: because $comp$ is a functor it commutes with composition in the hom-categories, so we have (writing vertical composition with $\circ$ and horizontal as juxtaposition):
$$
 (\beta' \circ \beta)(\alpha' \circ \alpha) = (\beta' \alpha') \circ (\beta \alpha)
$$

#Remarks

* A strict 2-category is the same as a [[strict omega-category]] which is trivial in degree $n \geq 3$.

* This is to be contrasted with a _weak 2-category_ called a [[bicategory]]. In a strict 2-category composition of 1-morphisms is strictly associative and comoposition with [[identity morphism]]s strictly satisfies the required identity law. In a weak 2-category these laws may hold only up to coherent 2-morphisms.


[[!redirects strict 2-categories]]