
# Properads
* table of contents
{: toc}

## Definition

A __properad__ in a [[symmetric monoidal
category]]&#160;$C$ is a [[monoid]] in the [[monoidal
category]] of [[symmetric sequence|bisymmetric sequences]] in&#160;$C$ (i.e.,
functors $\Sigma\times\Sigma\to C$) equipped
with a version of [[substitution product]]
modeled on connected directed graphs with 2 levels
instead of corollas, which are used for [[operads]].
See &#167;1.2 in [Vallette](#Vallette) for details.
The idea is that operations in a properad can
have multiple inputs and outputs, as opposed
to a single output in an operad.

### Relation to polycategories, dioperads and PROPs

The notion of coloured properads is more general than that of [[polycategories]] in that properads have [[composition]]-operations along more than one object. See at *[polycategory -- Relation to properads](polycategory#RelationToProperads)* for a more detailed explanation.

Properads are less general than [[PROPs]], which also allow a "composition" of nonconnected graphs, by tensoring morphisms with $\otimes$.

## Related concepts

* [[PROP]]
* [[polycategory]]
* [[dioperad]]
* [[multicategory]]
* [[operad]]

The **pluricategories** of [Kavanagh](#Kavanagh) (Definition 2.1.11) are similar to properads, except that they have identity morphisms for each list of objects, rather than a unary morphism for each object.

## References

* {#Vallette} [[Bruno Vallette]], A Koszul duality for props.
[arXiv:math/0411542](http://arxiv.org/abs/math/0411542)

Properads are called **compact polycategories** in:

* Ross Duncan. "Types for quantum computing." Phd thesis (2006).

The notion of **pluricategory** is defined in:

* {#Kavanagh} Ryan Kavanagh. _Communication-Based Semantics for Recursive Session-Typed Processes_. Thesis. Carnegie Mellon University, 2021 ([pdf](https://rak.ac/publication/2021-communication-based-semantics-for-recursive-session-typed-processes/thesis.pdf))

About the [[(∞,1)-category]] version

* Shaul Barkan, Jan Steinebrunner, _The equifibered approach to ∞-properads_ ([arXiv:2211.02576](https://arxiv.org/abs/2211.02576)).


[[!redirects properads]]
[[!redirects Properads]]
[[!redirects pluricategory]]
[[!redirects pluricategories]]
[[!redirects compact polycategory]]
[[!redirects compact polycategories]]