## Idea ##

A space is _connected_ if it can\'t be split up into two independent parts.  Every space is a [[disjoint union]] (but *not* necessarily a [[coproduct]] in the category of spaces) of connected _components_.  One often studies topological ideas first for connected spaces and then generalises to general spaces; this is especially true if one is studying such [[nice topological space]]s that every space *is* a coproduct of connected components.

## Definitions ##

Speaking category-theoretically a [[topological space]] $X$ is **connected** if the [[representable functor]]
$$ hom(X, -): Top \to Set $$
preserves [[coproduct]]s. It\'s actually enough to require that it preserves binary coproducts; in that case, notice that we always have a map
$$ hom(X,Y) + hom(X,Z) \to hom(X,Y + Z) ,$$
so $X$ is connected if this is always a [[bijection]]. This definition generalises to the notion of [[connected object]] in an [[extensive category]].

Here are some equivalent ways to say that $X$ is connected in more elementary terms:
* Whenever $X \cong Y + Z$, where the right side is the coproduct of spaces $Y, Z$ (so that $Y, Z$ are identified with disjoint open subspaces of $X$), then exactly one of $Y, Z$ is [[inhabited set|inhabited]] (so the other is [[empty set|empty]], making the inhabited one homeomorphic to $X$).
* If $K \subseteq X$ is clopen (both closed and open), then $K = X$ if and only if $K$ is inhabited.

Many authors allow the [[empty space]] to be connected.  You can get this concept from the elementary definitions above by changing 'exactly one' to 'at most one' and changing 'if and only if' to 'if'.  Categorially, this version of connectedness requires only that the maps
$$ hom(X,Y) + hom(X,Z) \to hom(X,Y + Z) $$
be [[surjection]]s.  However, many results come out more cleanly by disqualifying the empty space (much as one disqualifies $1$ when one defines the notion of [[prime number]]).  See also the discussion at [[empty space]].

The elementary definitions above have been carefully phrased to be correct in [[constructive mathematics]].  One may also see classically equivalent forms that are constructively weaker.

## Basic results ##

1. The [[image]] of a connected space $X$ under a continuous map $f: X \to Y$ is connected.

1. Wide [[pushout]]s (that is [[cofibered coproduct]]s) of connected spaces are connected. (This would of course be false if the empty space were considered to be connected.) This follows from the hom-functor definition of connectedness, plus the fact that coproducts in $Top$ commute with wide pullbacks ([[fibered product]]s). More memorably: connected colimits of connected spaces are connected. 

1. An arbitrary [[product]] of connected spaces is connected.

1. The interval $[0, 1]$, as a subspace of $\mathbb{R}$, is connected. (This is the topological underpinning of the intermediate value theorem.)

1. If $S \subseteq X$ is a connected subspace and $S \subseteq T \subseteq \overline{S}$ (i.e. if $T$ is between $S$ and its closure), then $T$ is connected.

## Connected components ##

Every topological space $X$ admits an [[equivalence relation]] $\sim$ where $x \sim y$ means that $x$ and $y$ belong to some subspace which is connected. The equivalence class $Conn(x)$ of an element $x$ is thus the union of all connected subspaces containing $x$; it follows readily from the basic results above that $Conn(x)$ is itself connected. It is called the **connected component** of $x$. It is closed, by one of the basic results above.

Alternatively, observe that if $x \in C$ and $x \in K$, where $C$ is a connected subspace and $K$ is clopen, then $C \subseteq K$. Moreover, the intersection of all clopens containing $x$ is itself connected (because it cannot be further subdivided by a clopen). Hence
$$ Conn(x) = \bigcap \{ clopen K \;:\; x \in K \} .$$
If we define connected components with this formula, then we can define a space to be connected if and only if it has exactly one connected component (or at most one, if you allow the empty space to be connected).

+-- {: .un_remark}
###### Warning

It is not generally true that a space is the coproduct (in $Top$) of its connected components. For example, the connected components in [[Cantor space]] $2^{\mathbb{N}}$ (with its topology as a product of 2-point discrete spaces) are just the singletons, but the coproduct of the singleton subspaces carries the discrete topology; another example with this feature is the set of rational numbers with its absolute-value topology (the one induced as a subset of the real line).
=--

Indeed, a space is the coproduct of its connected components precisely when it is **locally connected** (meaning that every point has a connected neighborhood). This occurs for example if there are only finitely many connected components (because then each connected component will be both closed and open).

A space $X$ is **totally disconnected** if its connected components are precisely the singletons of $X$. 

## Path-connectedness ##

An important variation on the theme of connectedness is path-connectedness. If $X$ is a space, define the path component $[x]$ to be the subspace of all $y \in X$ for which there exists a continuous map $h: [0, 1] \to X$ where $h(0) = x$, $h(1) = y$. We say $X$ is **path-connected** if it has exactly one path component.

It follows easily from the basic results above that each path component $[x]$ is connected. However, it need not be closed (and therefore need not be the connected component of $x$). The **topologist's sine curve**
$$ \{ (x, y) \in \mathbb{R}^2 \;:\; (0 \lt x \leq 1 \;\wedge\; y = sin(1/x)) \;\vee\; (0 = x \;\wedge\; -1 \leq y \leq 1) \} $$
provides a classic example of this happenstance. However, the path components and connected components coincide if $X$ is **locally path-connected** (meaning each point has an open neighborhood which is path-connected).

The basic categorical results 1., 2., and 3. above carry over upon replacing "connected" by "path-connected". (As of course does 4., trivially.)


[[!redirects path-connected space]]