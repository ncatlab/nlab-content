## Idea

A _pretopological space_ is a slight generalisation of a [[topological space]] where the concept of _neighbourhood_ is taken as primary.


## Definitions

Given a [[set]] $S$, let a __point__ in $S$ be an element of $S$, and let a __set__ in $S$ be a [[subset]] of $S$.  Given a [[relation]] $\stackrel{\circ}\in$ between points in $S$ and sets in $S$, say that the set $U$ is a __neighbourhood__ (or __$\stackrel{\circ}\in$-neighbourhood__ to be precise) of $x$ if $x \stackrel{\circ}\in U$ (which may also be written $x \in \stackrel{\circ}U$).

A __pretopology__ (or __pretopological structure__) on $S$ is such a relation $\stackrel{\circ}\in$ that satisfies these properties:

*  Centred:  If $U$ is a neighbourhood of $x$, then $x$ belongs to $U$:
   $$ x \stackrel{\circ}\in U \;\Rightarrow\; x \in U .$$
*  Isotone:  If $U$ is a neighbourhood of $x$ and $U$ is contained in $V$, then $V$ is a neighbourhood of $x$:
   $$ x \stackrel{\circ}\in U \;\Rightarrow\; U \subseteq V \;\Rightarrow\; x \stackrel{\circ}\in V .$$
*  Filtered:  If $U$ and $V$ are neighbourhoods of $x$, then so is their [[intersection]]:
   $$ x \stackrel{\circ}\in U \;\Rightarrow\; x \stackrel{\circ}\in V \;\Rightarrow\; x \stackrel{\circ}\in U \cap V .$$
*  Nontrivial:  The entire space is a neighbourhood of $x$:
   $$ x \stackrel{\circ}\in S .$$

In other words, the collection of neighbourhoods of $x$ must be a [[filter]] that is refined by the free [[ultrafilter]] at $x$.  This is called the __neighbourhood filter__ of $x$.


A __pretopological space__ is a set equipped with a pretopological structure.


A __continuous map__ from a pretopological space $S$ to a pretopological space $T$ is a [[function]] $f$ from $S$ to $T$ such that:

*  For every point $x$ in $S$, if $U$ is a neighbourhood of $f(x)$ in $T$, then the [[preimage]] $f^*(U)$ is a neighbourhood of $x$ in $S$.


In this way, pretopological spaces and continuous maps form a [[category]] $Pre Top$.


## Convergence structure

If $F$ is a [[filter]] on a pretopological space $S$, then $F$ __converges__ to a point $x$ (written $F \to x$) if $F$ refines (contains) the neighbourhood filter of $x$.

This relation satisfies the following properties:

*  Centred:  The free ultrafilter at $x$ (the collection of all sets that $x$ belongs to) converges to $x$:
   $$ \{ A \;|\; x \in A \} \to x .$$
*  Isotone:  If $F$ converges to $x$ and $G$ refines $F$, then $G$ converges to $x$:
   $$ F \to x \;\Rightarrow\; F \subseteq G \;\Rightarrow\; G \to x .$$
*  Infinitely filtered:  The intersection of all filters that converge to $x$ itself converges to $x$:
   $$ \bigcap \{ F \;|\; F \to x \} \to x .$$

In this way, every pretopological space becomes a [[convergence space]].

In fact, we can recover the pretopological structure from the convergence structure as follows: $x \stackrel{\circ}\in U$ if and only if $U$ belongs to every filter that converges to $x$.  In other words, that intersection that appears in the infinite filtration condition is the neighbourhood filter of $x$.  Furthermore, this definition assigns a pretopological structure to any convergence space satsifying the conditions above, and a map between pretopological spaces is continuous if and only if it is continuous as a map between convergence spaces.

Thus, we can define a pretopological space as an infinitely filtered convergence space, making $Pre Top$ a [[full subcategory]] of the category $Conv$ of convergence spaces.