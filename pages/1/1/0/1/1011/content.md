A **finite category** $C$ is a [[category]] [[internal category|internal to]] the category [[FinSet]] of finite sets.

This means that a finite category consists of
* a finite set of [[object]]s;
* a finite set of [[morphism]]s.

(Notice that the latter implies the former, since for every object there is the [[identity morphism]] on that object).

Similarly, a **locally finite category** is a category [[enriched category|enriched]] over $Fin Set$, that is a category whose [[hom-set]]s are all finite.

(Locally) finite categories may also be called (locally) **$\omega$-small**; this generalises from $\omega$ (the set of [[natural number]]s) to (other) [[inaccessible cardinal]]s (or, equivalently, [[Grothendieck universe]]s).

# Limits and colimits

One is often interested in whether an arbitrary category $D$ has [[limit]]s and [[colimit]]s indexed by finite categories.  A category with all finite limits is called **[[finitely complete category|finitely complete]]** or **left exact** (or **lex** for short).  A category with all finite colimits is called **finitely cocomplete** or **right exact**.

+--{: .query}

[[Eric]]: Is the following statement correct?

>For any finite category $C$, there is a [[directed graph]] $G$ such that its [[quiver]] $Q(G)$ is equivalent to $C$.

[[Mike Shulman]]: No, this is false.  The "walking commutative square"
$$\array{ & \to & \\
  \downarrow && \downarrow\\
  & \to & }$$
is a finite category which is not free on any directed graph.

_Toby_:  The walking commutative triangle is an even simpler counterexample.  Rather, we should say that any finite category is a *[[quotient object|quotient]]* of some quiver; the nontrivial commutation relations (triangles, squares, etc) give us this quotient.  But in fact, there is nothing special about finite categories here; every category is a quotient of the quiver on its underlying graph.  So I think that the only point to be made here is that, for a finite category, the graph may also be taken to be finite, but even that is obvious since the underlying graph is finite.

[[Eric]]: Thanks! That is interesting. This reminds me of the [[ericforgy:differential envelope|universal differential envelope]] on a complete directed graph. Any discrete calculus is a quotient of the universal discrete calculus obtained by removing some edges.

_Toby_:  Sure, there are lots of [[adjunctions]] that work this way.  (I forget the precise adjective that I should put before 'adjunction' here.)

[[Mike Shulman]]: If the "walking commutative triangle" means what I think it does, then it actually is a quiver.  The hypotenuse is freely generated as the composite of the other two sides.

[[Eric]]: Wait a second. Does the "walking commutative square" consist of 4 objects? If so, then the diagonal should be a morphism because it is the composite of two sides so the diagram is not complete as drawn. It should include the diagonal. I'm sure I'm confused. What am I missing?

[[Mike Shulman]]: Yes, the diagonal is a morphism.  I didn't draw it because we don't usually draw the diagonal when we draw a commutative square, just like we don't usually draw identity morphisms.

=--
