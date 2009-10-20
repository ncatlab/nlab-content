A **finite category** $C$ is a [[category]] [[internal category|internal to]] the category [[FinSet]] of finite sets.

This means that a finite category consists of
* a finite set of [[object]]s;
* a finite set of [[morphism]]s.

(Notice that the latter implies the former, since for every object there is the [[identity morphism]] on that object).

Similarly, a **locally finite category** is a category [[enriched category|enriched]] over $Fin Set$, that is a category whose [[hom-set]]s are all finite.

(Locally) finite categories may also be called (locally) **$\omega$-small**; this generalises from $\omega$ (the set of [[natural number]]s) to (other) [[inaccessible cardinal]]s (or, equivalently, [[Grothendieck universe]]s).

# Limits and colimits

One is often interested in whether an arbitrary category $D$ has [[limit]]s and [[colimit]]s indexed by finite categories.  A category with all finite limits is called **[[finitely complete category|finitely complete]]** or **left exact** (or **lex** for short).  A category with all finite colimits is called **finitely cocomplete** or **right exact**.

# Quiver #

**This section may not be correct and needs review.**

For any finite category $C$, there is a [[directed graph]] $G$ such that its [[quiver]] $Q(G)$ is equivalent to $C$.

+--{: .query}
[[Mike Shulman]]: No, this is false.  The "walking commutative square"
$$\array{ & \to & \\
  \downarrow && \downarrow\\
  & \to & }$$
is a finite category which is not free on any directed graph.

_Toby_:  The walking commutative triangle is an even simpler counterexample.  Rather, we should say that any finite category is a *[[quotient object|quotient]]* of some quiver; the nontrivial commutation relations (triangles, squares, etc) give us this quotient.  But in fact, there is nothing special about finite categories here; every category is a quotient of the quiver on its underlying graph.  So I think that the only point to be made here is that, for a finite category, the graph may also be taken to be finite, but even that is obvious since the underlying graph is finite.
=--
