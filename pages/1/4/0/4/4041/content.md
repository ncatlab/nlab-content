Let $U: C\to D$ be a [[forgetful functor]] and $x\in D$.  A **free $C$-object** on $x$ is an object of $C$ that satisfies the universal property that $F(x)$ would have, if $F$ were a left adjoint to $U$ (the corresponding [[free functor]]).  If $U$ actually has a left adjoint, then $F(x)$ is a free $C$-object on $x$ for every $x$, and conversely if there exists a free $C$-object on every $x\in D$ then $U$ has a left adjoint.  But individual free objects can exist without the whole left adjoint functor exist.

More precisely: a __free $C$-object on $x$__ consists of an object $y\in C$ together with a morphism $\eta_x \colon x\to U y$ in $D$ such that for any other $z\in C$ and morphism $f\colon x\to U z$ in $D$, there exists a unique $g\colon y\to z$ in $C$ with $U(g) \circ \eta_x = f$.  In other words, it is an [[initial object]] of the [[comma category]] $(x/U)$.  A free $C$-object on $x$ is also sometimes called a **universal arrow** from $x$ to the functor $U$.

Similarly, a __cofree object__ (or __fascist object__) is given by a [[cofree functor]].


[[!redirects free object]]
[[!redirects free objects]]

[[!redirects cofree object]]
[[!redirects cofree objects]]
[[!redirects co-free object]]
[[!redirects co-free objects]]
[[!redirects fascist object]]
[[!redirects fascist objects]]
