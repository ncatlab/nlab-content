
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A 'structure type' is a type of [[extra structure]] that can placed on [[finite set]]s, e.g. a coloring, or ordering.  

## Definition

We define a __structure type__ to be a [[faithful functor]]

$$p: X \to core(FinSet)$$

from some groupoid $X$ to [[core]]([[FinSet]]), which is the [[groupoid]] of [[finite set]]s and [[bijection]]s.  Equivalently, we can think of it as a [[presheaf]] of sets on the groupoid of finite sets and bijections, or in other words a functor

$$F: core(FinSet)^{op} \to Set $$

These two points of view are related by the [[Grothendieck construction]]:

$$F(n) = p^{-1}(n) $$

But since a groupoid is equivalent to its opposite, we can also think of a structure type as a functor

$$core(FinSet) \to Set $$

In this guise, a structure type is more commonly called a __(combinatorial) species of structure__, or [[species]] for short.  

A structure type is a special case of a stuff type, so see [[stuff type]] for more information.


## References

* [[John Baez]], ...


[[!redirects structure type]]
[[!redirects structure types]]
