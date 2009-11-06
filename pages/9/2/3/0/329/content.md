# Strict $2$-categories
* tic
{: toc}


##Idea

* A strict 2-category is a [[directed n-graph|directed 2-graph]] equipped with a composition operation on adjacent 1-cells and 2-cells which is strictly unital and associative.

* The concept of a strict 2-category is the simplest generalization of a [[category]] to a [[higher category theory|higher category]]. It is the one-step [[vertical categorification|categorification]] of the concept of a category.


##Definition

A _strict 2-category_, often called simply a _2-category_, is a [[enriched category|category enriched over]] [[Cat]], where $Cat$ is treated as the [[1-category]] of [[strict categories]]. 

+--{.query}
[[Eric]]: Could someone spell this out in a little more detail?

[[Finn Lawler|Finn]]: See **Details** below for a first attempt.
=--

Similarly, a [[strict 2-groupoid]] is a groupoid enriched over groupoids. This is also called a [[geometric shapes for higher structures|globular]] strict 2-groupoid, to emphasise the underlying geometry. The category of strict 2-groupoids is eqivalent to the category  of [[crossed module]]s over groupoids. It is also equivalent to the category of (strict) double groupoids with connections. 

They are also special cases of strict globular omega-groupoids, and the category of these is equivalent to the category of [[crossed complex]]es. 


###Details

Working out the meaning of '$Cat$-enriched category', we find that a strict 2-category $K$ is given by

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


###More details

In even more detail, a strict $2$-category $K$ consists of

*  a collection $Ob K$ or $Ob_K$ of _objects_ or _$0$-cells_,
*  for each object $a$ and object $b$, a collection $K(a,b)$ or $Hom_K(a,b)$ of _morphisms_ or _$1$-cells_ $a \to b$, and
*  for each object $a$, object $b$, morphism $f\colon a \to b$, and morphism $g\colon a \to b$, a collection $K(f,g)$ or $2 Hom_K(f,g)$ of _$2$-morphisms_ or _$2$-cells_ $f \to g$ or $f \Rightarrow g$,

equipped with

*  for each object $a$, an _identity_ $1_a\colon a \to a$ or $\id_a\colon a \to a$,
*  for each $a,b,c$, $f\colon a \to b$, and $g\colon b \to c$, a _composite_ $f ; g\colon a \to c$ or $g \circ f\colon a \to c$,
*  for each $f\colon a \to b$, an _identity_ $1_f\colon f \Rightarrow f$ or $\Id_f\colon f \to f$,
*  for each $f,g,h\colon a \to b$, $\eta\colon f \Rightarrow g$, and $\theta\colon g \Rightarrow h$, a _vertical composite_ $\theta \bullet \eta\colon f \Rightarrow h$,
*  for each $a,b,c$, $f\colon a \to b$, $g,h\colon b \to c$, and $\eta\colon g \Rightarrow h$, a _left whiskering_ $\eta \circ f\colon g \circ f \Rightarrow h \circ f$, and
*  for each $a,b,c$, $f,g\colon a \to b$, $h\colon b \to c$, and $\eta\colon f \Rightarrow g$, a _right whiskering_ $h \circ \eta \colon h \circ f \Rightarrow h \circ g$,

such that

*  for each $f\colon a \to b$, the composites $f \circ \id_a$ and $\id_b \circ f$ each equal $f$,
*  for each $a \overset{f}\to b \overset{g}\to c \overset{h}\to d$, the composites $h \circ (g \circ f)$ and $(h \circ g) \circ f$ are equal,
*  for each $\eta\colon f \Rightarrow g\colon a \to b$, the vertical composites $\eta \bullet \Id_f$ and $\Id_g \bullet \eta$ both equal $\eta$,
*  for each $f \overset{\eta}\to g \overset{\theta}\to h \overset{\iota}\to i$ (with $f,g,h,i\colon a \to b$), the vertical composites $\iota \bullet (\theta \bullet \eta)$ and $(\iota \bullet \theta) \circ \eta$ are equal,
*  (more in a moment, it\'s been half an hour) ...


##Remarks

* A strict 2-category is the same as a [[strict omega-category]] which is trivial in degree $n \geq 3$.

* This is to be contrasted with a _weak 2-category_ called a [[bicategory]]. In a strict 2-category composition of 1-morphisms is strictly associative and comoposition with [[identity morphism]]s strictly satisfies the required identity law. In a weak 2-category these laws may hold only up to coherent 2-morphisms.


[[!redirects strict 2-categories]]