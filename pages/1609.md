_Partially ordered category_ is a category together with partial order on the set of its morphisms with the additional requirement that
$f_1 \subseteq f_2 \wedge g_1 \subseteq g_2 \Rightarrow g_1 \circ f_1 \subseteq g_2 \circ f_2$ for any morphisms $f_1$, $g_1$, $f_2$, $g_2$ such that $\mathrm{Dst} f_1 =
\mathrm{Src} g_1 \wedge \mathrm{Dst} f_2 = \mathrm{Src} g_2$

For a _partially ordered category_ its set of objects is partially ordered by the formula $A \subseteq B \Leftrightarrow 1_A \subseteq 1_B$.

**TODO: Create special page for _categories with inverses_.**

  I will call a _precategory with inverses_ a precategory together
  with a function $x \mapsto x^{- 1}$ defined on the set of morphisms, which
  reverses source and destination of the morphism subject to following
  equalities for any morphisms $f$, $g$:
 $(f^{- 1})^{- 1} = f$;
 $(g \circ f)^{- 1} = f^{- 1} \circ g^{- 1}$.

  I will call a _category with inverses_ a precategory with inverses
  which is a category with additional requirement that for any isomorphism its
  inverse is the reverse isomorphism.

For a partially ordered (pre)category with inverses I will additionally
require (for any morphisms $f$ and $g$)
\[ f^{- 1} \subseteq g^{- 1} \Leftrightarrow f \subseteq g. \]

  For a partially ordered category with inverses I will call
  _monovalued_ morphism such a morphism $f$ that $f \circ f^{- 1}
  \subseteq 1_{\mathrm{Dst} f}$.

  For a partially ordered category with inverses I will call _entirely defined morphism_ such a morphism $f$ that $f^{- 1} \circ f \supseteq
  1_{\mathrm{Src} f}$.

See more in [this online article](http://www.mathematics21.org/binaries/ordered-cats-with-inv.pdf). Feel free to copy the information from this my article to nLab wiki.

See also [[generalized continuity]].