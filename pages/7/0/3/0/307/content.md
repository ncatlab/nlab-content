A **terminal object** in a [[category]] $C$ is an [[object]] $1$ of $C$ satisfying the following universal property: for every object $x$ of $C$, there exists a unique [[morphism]] $!:x\to 1$.  The terminal object of any category, if it exists, is unique up to unique [[isomorphism]].  If the terminal object is also [[initial object|initial]], it is called a [[zero object]].

A terminal object is often written $1$, since in [[Set]] it is a 1-element set, and also because it is the unit for the cartesian [[product]].  Other notations for a terminal object include $*$ and $pt$.

A terminal object may also be viewed as a [[limit]] over the empty [[diagram]].  Conversely, a limit over a diagram is a terminal cone over that diagram.

For any object $x$ in a category with terminal object $1$, the categorical [[product]] $x\times 1$ and the [[exponential object]] $x^1$ both exist and are canonically isomorphic to $x$.

Some examples of terminal objects in notable categories follow:
* The terminal object of a [[partial order|poset]] is its [[top]] element, if it exists.
* Any one-element set is a terminal object in the category [[Set]].
* The trivial [[group]] is the terminal object of [[Grp]] and, as an [[abelian group]], of [[Ab]].
* The terminal object of [[Ring]] is the zero ring.  (Note however that if [[ring|rings]] have unities and ring [[homomorphism|homomorphisms]] must preserve them, then the zero ring is not a [[zero object]] of [[Ring]].)
* The terminal object of [[Cat]] is the [[discrete category]] with just one object.
* The terminal object of a [[over category|slice category]] $C/x$ is the [[identity]] $x\to x$.

#Terminal object in higher categories#

## In $(\infty,1)$-categories ##

A **terminal object** in an [[(infinity,1)-category]] is an object $pt$ such that for any other object $c$ the $(\infty,0)$-groupoid $Hom(c,pt)$ is [[contractible]].