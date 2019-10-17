
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+-- {: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}


## Idea

The pointwise order is the canonical [[order]] on the set of functions into a [[poset]] or [[preorder]].

Using [[negative thinking]], this can be seen as the [[(0,1)-category|(0,1)-decategorification]] of the concept of [[category of functors]].
Just as well, it can be seen as the [[enriched functor category]] for categories enriched in [[truth values]].


## Definition

+-- {: .num_defn}
###### Definition

Let $X$ be a set, and let $Y$ be a [[preorder|preordered set]]. Given $f,g:X\to Y$, we say that $f\le g$ in the **pointwise order** or **product order** if and only of for every $x\in X$ we have $f(x)\le g(x)$. 

=--

The terminology "product order" comes from the fact that the order defined above can be seen as the one of the object
$$
\prod_{x\in X} Y
$$
in the category of preorders (which has products). The underlying set of the object above is indeed naturally isomorphic to the set of functions $X\to Y$.


## 2-cells

Just as [[Cat]] is naturally a [[2-category]], with 2-cells given by [[natural transformations]] (i.e. [[morphisms]] of [[functors]]), many categories of preorders (such as [[Pos]]) are naturally [[locally posetal 2-categories]], with the 2-cells given by the pointwise order. That is, given $f,g:X\to Y$, we draw a 2-cell $f\Rightarrow g$ if and only if $f\le g$ in the pointwise order.
If the morphisms are chosen to be [[monotone]], this choice of 2-cells gives indeed the structure of a [[2-category]]. 


## See also

* [[Pos]]
* [[locally posetal 2-category]]
* [[(0,1)-category]]


[[!redirects product order]]
[[!redirects product ordering]]
[[!redirects pointwise ordering]]
[[!redirects pointwise ordered]]
[[!redirects ordered pointwise]]