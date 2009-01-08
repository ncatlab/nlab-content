#Idea#

In the context of [[homotopy coherent category theory]] one wishes to nicely pair [[enriched category theory]] with [[homotopy theory]] for the case that the category $V$ being enriched over is a [[model category]] or at least a [[homotopical category]].

The idea is that a _closed (symmetric) monoidal homotopical category_ is a [[closed monoidal category]] which is also  [[homotopical category|homotopical]] such that its [[homotopy category]] $Ho_V$ is still itself [[closed monoidal category|closed monoidal]].

A category enriched over such $V$ may be an [[enriched homotopical category]].

#Definition#

A _closed (symmetric) monoidal homotopical category_ $V_0$ is a [[closed monoidal category|closed]], [[monoidal category|symmetric monoidal]] [[homotopical category|homotopical]] category which is furthermore equipped with a [[closed monoidal deformation retract]].

#Examples#

The most obvious example is:

* Any (symmetric) [[monoidal model category]] is a closed (symmetric) monoidal homotopical category.

In this case, the cofibrant and fibrant replacements serve as a closed monoidal deformation retract.   Closed monoidal homotopical categories that are not monoidal model categories seem surprisingly hard to come by, given how much stronger the axioms of a monoidal model category appear.  One other example that can probably be extracted from the theory of homotopy tensor products in Shulman ([below](http://arxiv.org/abs/math.AT/0610194)) is:

* If $V$ is a closed symmetric monoidal homotopical category (such as a monoidal model category) and $C$ is any small category, then the functor category $V^C$, with its [[Day tensor product]] and levelwise homotopical structure, is a closed symmetric monoidal homotopical category.  The closed monoidal deformation retract is provided by the deformations in $V$ combined with the [[bar construction]].


#Properties#

+-- {: .un_prop}
###### Proposition
The [[homotopy category]] $Ho_V$ of a closed (symmetric)
monoidal homotopical category $V$ is itself 
closed (symmetric) monoidal.
=--


#References#

The definition appears as [definition 15.3, p. 44](http://arxiv.org/PS_cache/math/pdf/0610/0610194v1.pdf#page=44) in Shulman: [Homotopy limits and colimits in enriched homotopy theory](http://arxiv.org/abs/math.AT/0610194v1),
the proposition as [proposition 15.4, p. 45](http://arxiv.org/PS_cache/math/pdf/0610/0610194v1.pdf#page=45).

