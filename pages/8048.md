
## Definition

A **wild category** is a 1-dimensional approximation of an [[nlab:infinity-category]] that is definable in [[Book HoTT]].  It consists of

* A type $ob A$ of objects
* For objects $x,y$ a type $A(x,y)$ of morphisms
* For each object $x$ an identity $id_x : A(x,x)$
* For objects $x,y,z$ a composition function $\circ : A(y,z) \times A(x,y) \to A(x,z)$
* For objects $x,y$ and a morphism $f:A(x,y)$, equalities $f \circ id_x = f = id_y \circ f$
* For objects $x,y,z,w$ and morphisms $f:A(x,y)$ and $g:A(y,z)$ and $h:A(z,w)$, an equality $h\circ (g\circ f) = (h\circ g)\circ f$.

If each $A(x,y)$ is a [[set]], then a wild category reduces to a [[precategory]], but in general this condition is not imposed.  This means that, for instance, there is a nontrivial pentagon identity for the associativities that does not necessarily commute, and so on.  However, even lacking these coherence data, a wild category is sufficient for some purposes.

For example, we can define an *initial object* in a wild category to be an object $0$ such that $A(0,x)$ is contractible for all $x$.  In cases when the wild category "is" actually a coherent higher category, this still gives the right answer, and it is sufficient for applications such as producing induction principles for [[higher inductive types]].  See the references for more specific examples.

## References

* Paolo Capriotti, Nicolai Kraus, _Univalent Higher Categories via Complete Semi-Segal Types_, [arxiv](https://arxiv.org/abs/1707.03693), 2017

* Nicolai Kraus, Jakob von Raumer, _Path Spaces of Higher Inductive Types in Homotopy Type Theory_, [arxiv](https://arxiv.org/abs/1901.06022), 2019

* Mike Shulman, _Impredicative Encodings, Part 3_, [blog post](https://homotopytypetheory.org/2018/11/26/impredicative-encodings-part-3/), 2018
