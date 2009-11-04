# Idea #

A homotopy $1$-type is a space where we consider its properties with regard to the [[fundamental group]]s $\pi_1$ of its components.

# Definition #

A continuous map $X \to Y$ is a **homotopy $1$-equivalence** if it induces isomorphisms on $\pi_0$ and $\pi_1$ at each basepoint.  Two spaces share the same **homotopy $1$-type** if they are linked by a zig-zag chain of homotopy $1$-equivalences.

For any space $X$, you can kill its homotopy groups in higher dimensions by attaching cells, thus constructing a new space $Y$ so that the inclusion of $X$ into $Y$ is a homotopy $1$-equivalence; up to (weak) [[homotopy equivalence]], the result is the same for any space with the same homotopy $1$-type.  Accordingly, a **homotopy $1$-type** may alternatively be defined as a space with trivial $\pi_i$ for $i \gt 1$, or as the unique (weak) [[homotopy type]] of such a space, or as its fundamental $\infty$-[[fundamental infinity-groupoid|groupoid]] (which will be a $1$-[[1-groupoid|groupoid]]).

See the general discussion in [[homotopy n-type]].

# Classification #

A connected pointed homotopy 1-type is completely determined, up to (weak) homotopy equivalence, by the one [[group]] $\pi_1$.  A connected homotopy 1-type with $\pi_1 = G$ is  an [[Eilenberg-Mac Lane space]] and is often written $K(G,1)$.  A general homotopy 1-type can then be written as a disjoint union of such $K(G,1)$s, and is completely determined by its [[fundamental groupoid]].

In the other direction, for any (discrete) group $G$ one can construct its [[classifying space]] $\mathcal{B}G$, which is a $K(G,1)$.  In fact, many versions of this construction (such as the geometric realization of the simplicial nerve $nerve(G)$; see [[Dold-Kan correspondence]]) apply just as well to any [[groupoid]].  We can obtain any 1-type in this way,  since a groupoid is up to homotopy type (of groupoids!) a disjoint union of groups. However this description is not natural in the category of groupoids, and is analogous to choosing a basis for a vector space. 

Moreover, every continuous map between $K(G,1)$s is induced by a group homomorphism, every map between 1-types is induced by a [[functor]] between groupoids, and every homotopy is induced by a conjugation (aka a [[natural transformation]] between groupoids).  In fact, one can show that the $(\infty,1)$-[[(infinity,1)-category|category]] of homotopy 1-types is equivalent to the 2-category [[Grpd]] of [[groupoid]]s, via the above-described correspondence..

There are further aspects to this relationship; for instance, the [[van Kampen theorem]] for the fundamental groupoid shows how the algebra of groupoids models the gluing of spaces.  The general result for non-connected spaces is possible because groupoids model homotopy 1-types, having structure in dimensions 0 and 1.  For the search for algebraic structures that play an analogous role to groupoids for $n$-types with $n\gt 1$, see the pages [[homotopy hypothesis]], [[fundamental infinity-groupoid]], [[cat-n-group]], [[classifying space]], [[crossed complex]], and probably others.

[[!redirects homotopy 1-types]]
