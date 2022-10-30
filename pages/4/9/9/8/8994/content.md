## Definition ##
A **linearly distributive category** (also called a **weakly distributive category**) is a [[monoidal category]] in two ways, with monoidal structures $(\otimes, I)$ and $(\bullet, J)$ equipped with extra associator natural transformations
\[ \delta^L:A\otimes (B\bullet C) \to (A \otimes B) \bullet C \]
\[ \delta^R:(A\bullet B) \otimes C \to A \bullet (B \otimes C) \]
and the obvious six pentagon equations and four triangle equations that make the monoidal structures work together nicely.

These extra associators are sometimes called "distributors", and should not be confused with [[profunctors]].  The term is a pun on the distributivity of multiplication over addition, but "linearized" so that each variable only appears once in the result.

**Warning:** a linearly distributive category *cannot* be a [[distributive category]], unless it is a partial order.

## Related pages

* [[distributivity for monoidal structures]]

## References

* [[Robin Cockett]], [[Robert Seely]], [Weakly Distributive Categories](http://www.math.mcgill.ca/rags/linear/wdc.ps.gz). _Journal of Pure and Applied Algebra_, 114(1997)2, pp 133-173.
* [[Paul-André Melliès]], [Categorical Semantics of Linear Logic](http://www.pps.univ-paris-diderot.fr/~mellies/papers/panorama.pdf), published in [[Pierre-Louis Curien]], Hugo Herbelin, Jean-Louis Krivine, Paul-Andr&#233; Melli&#232;s. _Interactive models of computation and program behaviour_, Panoramas et Synth&#232;ses 27, Soci&#233;t&#233; Math&#233;matique de France, 2009. 