An **m-cofibrant space** is a [[topological space]] that is [[homotopy equivalence|homotopy equivalent]] to a [[CW complex]].

The importance of m-cofibrant spaces comes from the fact any [[weak homotopy equivalence]] between m-cofibrant spaces is a homotopy equivalence. It is a classical theorem -- the [[Whitehead theorem]] -- that this is true for CW complexes, and it is easy to see that it is a property preserved under homotopy equivalence.  In fact, it is easy to see that m-cofibrant spaces are the largest subcategory $C$ of $Top$ which includes all CW complexes and such that any weak homotopy equivalence between objects of $C$ is a homotopy equivalence.

Moreover, since any space is weakly equivalent to a CW complex, any space is _a fortiori_ weakly equivalent to an m-cofibrant one.  It follows that the [[homotopy category]] of topological spaces in which the weak homotopy equivalences are inverted is equivalent to the homotopy category of m-cofibrant spaces in which homotopic maps are identified.

Therefore, m-cofibrant spaces are a natural place to do [[homotopy theory]] if one is interested in spaces up to weak homotopy type, but doesn't want to have to worry about the distinction between weak homotopy equivalence and homotopy equivalence.  For instance, when higher category theorists say that an $\infty$-[[infinity-groupoid|groupoid]] "is" a topological space, they generally mean an m-cofibrant space, so that $\infty$-functors, natural transformations, and so on can be identified with continuous maps, homotopies, etc.

Milnor, in particular, has argued that the category of m-cofibrant spaces is a convenient category of spaces for algebraic topology.  It is not [[cartesian closed category|cartesian closed]], but Milnor proved that if $Y$ is m-cofibrant and $X$ is [[compact Hausdorff space|compact Hausdorff]], then $Y^X$ is also m-cofibrant.  Hence many desirable constructions are still available, in particular finite and infinite [[loop space]]s.

More recently it has been discovered that there is a [[model category|model structure]] on [[Top]], called the _mixed model structure_, in which the weak equivalences are the weak homotopy equivalences, the cofibrant objects are precisely the m-cofibrant spaces, and the fibrations are the Hurewicz fibrations.  This is where the name "m-cofibrant" comes from; "m-" is for the "mixed" model structure, as contrasted with the "q-" or Quillen model structure and the "h-" or Hurewicz/Str&#248;m model structure (see [[model structure on topological spaces]]).


[[!redirects m-cofibrant spaces]]