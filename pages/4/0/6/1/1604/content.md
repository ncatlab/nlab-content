# Pretopological spaces
* tic
{: toc}


## Idea

A _pretopological space_ is a slight generalisation of a [[topological space]] where the concept of _neighbourhood_ is taken as primary.


## Definitions

Given a [[set]] $S$, let a __point__ in $S$ be an element of $S$, and let a __set__ in $S$ be a [[subset]] of $S$.  Given a [[relation]] $\stackrel{\circ}\in$ between points in $S$ and sets in $S$, say that the set $U$ is a __neighbourhood__ (or __$\stackrel{\circ}\in$-neighbourhood__ to be precise) of $x$ if $x \stackrel{\circ}\in U$ (which may also be written $x \in \stackrel{\circ}U$).


A __pretopology__ (or __pretopological structure__) on $S$ is such a relation $\stackrel{\circ}\in$ that satisfies these properties:

1.  Centred:  If $U$ is a neighbourhood of $x$, then $x$ belongs to $U$:
    $$ x \stackrel{\circ}\in U \;\Rightarrow\; x \in U .$$
1.  Nontrivial:  Every point $x$ has a neighbourhood.  In light of (4), the entire space is a neighbourhood of $x$:
    $$ x \stackrel{\circ}\in S .$$
    (Some references leave this out, but that seems to be an error.)
1.  Directed:  If $U$ and $V$ are neighbourhoods of $x$, then so is some set contained in their [[intersection]].  In the light of (4), it follows that their intersection is itself a neighbourhood:
    $$ x \stackrel{\circ}\in U \;\Rightarrow\; x \stackrel{\circ}\in V \;\Rightarrow\; x \stackrel{\circ}\in U \cap V .$$
    (Strictly speaking, the relation should not be called [[direction|directed]] unless it is also nontrivial.)
1.  Isotone:  If $U$ is a neighbourhood of $x$ and $U$ is contained in $V$, then $V$ is a neighbourhood of $x$:
    $$ x \stackrel{\circ}\in U \;\Rightarrow\; U \subseteq V \;\Rightarrow\; x \stackrel{\circ}\in V .$$

In other words, the collection of neighbourhoods of $x$ must be a [[filter]] that is refined by the free [[ultrafilter]] at $x$.  This filter is called the __neighbourhood filter__ of $x$.


A pretopology can also be given by a base or subbase.  A __base__ for a pretopology is any relation that satisfies (1--3), using the first version for each of (2,3); a __subbase__ is any relation that satisfies (1).  (It would not really be appropriate to use the symbol '$\stackrel{\circ}\in$' for a mere base or subbase; you\'d probably want to think of it as a family of sets indexed by the points, and use the term 'basic neighourhood' or 'subbasic neighbourhood'.)  You get a base (in fact one satisfying the stronger versions of 2,3) from a subbase by closing under finitary intersections; you get a pretopology from a base by taking supsersets.  (Really, this is just a special case of considering a base or subbase of a [[filter]].)


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
*  Infinitely directed:  The intersection of all filters that converge to $x$ itself converges to $x$:
   $$ \bigcap \{ F \;|\; F \to x \} \to x .$$

In this way, every pretopological space becomes a [[convergence space]].


In fact, we can recover the pretopological structure from the convergence structure as follows: $x \stackrel{\circ}\in U$ if and only if $U$ belongs to every filter that converges to $x$.  In other words, that intersection that appears in the infinite filtration condition is the neighbourhood filter of $x$.  Furthermore, this definition assigns a pretopological structure to any convergence space satsifying the conditions above, and a map between pretopological spaces is continuous if and only if it is continuous as a map between convergence spaces.  Thus, we can define a pretopological space as an infinitely directed convergence space, making $Pre Top$ a [[full subcategory]] of the category $Conv$ of convergence spaces.


Actually, we can do more.  The definition of $\stackrel{\circ}U$ from the convergence structure assigns a pretopological structure to *any* convergence space, although in general this pretopology defines a weaker notion of convergence (more filters converge to more points).  Thus, $Pre Top$ is also a [[reflective subcategory]] of $Conv$.


Every pretopological convergence satisfies the star property, so that $Pre Top$ is a full reflective subcategory of the category $Ps Top$ of [[pseudotopological spaces]].


## Examples

Every [[topological space]] is a pretopological space, using the usual definition of (not necessarily open) neighbourhood: $x \stackrel{\circ}\in U$ if there exists some open set $G$ such that $x \in G$ and $G \subseteq U$.  Also, a map between topological spaces is continuous if and only if it\'s continuous as a map between pretopological spaces.  In this way, the category [[Top]] of topological spaces becomes a full subcategory of $Pre Top$.

In fact, we can easily characterise the topological pretopologies, allowing us to define a topological space as a pretopological space satisfying this axiom:

*  If $U$ is a set, then let $\stackrel{\circ}U$ be the set of all points that $U$ is a neighbourhood of.  Then $\stackrel{\circ}U$ is a neighbourhood of each of its members.  That is,
   $$ x \stackrel{\circ}\in U \;\Rightarrow\; x \stackrel{\circ}\in \{ y \;|\; y \stackrel{\circ}\in U \} .$$

In the terms defined below, a topological space is a pretopological space in which every preinterior is open.


Here is an example of a nontopological pretopological space, although admittedly it is a bit artificial.  (This is based on Section 15.6 of [[HAF]].)  Consider a [[metric space]] $S$; according to the usual pretopology on $S$, $U$ is a neighbourhood of $x$ if there is a positive number $\epsilon$ such that $U$ contains the ball $ \{ y \;|\; d(x,y) \lt \epsilon \} $.  Now given a [[natural number]] $n$, we will give $S^n$ the _plus pretopology_: $U$ is a neighbourhood of $\vec{x} = (x_1,\ldots,x_n)$ if there is a positive number $\epsilon$ such that $U$ contains the $l^0$-ball $ \{ \vec{y} \;|\; \inf_i d(x_i,y_i) \lt \epsilon \} $.  (If $S$ is a line and $n = 2$, then this is a plus sign '+' with $(x_1,x_2)$ at the centre and cross bars of length $2 \epsilon$.)  Then $S^n$ is a pretopological space, but it is topological only if $n \leq 1$ or $S$ is a [[subsingleton]].

This example can probably be generalised to a [[uniform space]] $S$.  Possibly there is some interesting universal property of this 'plus product', although it seems to go from $Unif \times Unif$ to $Pre Top$, so maybe we need to work in a different category.  (There is a notion of [[uniform convergence space]] that generalises uniform spaces much like convergence spaces generalise topological spaces; perhaps the plus product takes place there.)


## Topological structure

Fix a pretopological space $S$.

The __preinterior__ of a set $A$ is the set $\stackrel{\circ}A$ or $A^\circ$ of all points that $A$ is a neighbourhood of:
$$ \stackrel{\circ}A = \{ x \;|\; x \stackrel{\circ}\in A \} .$$
A set $A$ is __open__ if it equals its preinterior.  The __interior__ $Int(A)$ of $A$ is the union of all of the open sets contained in $A$.  Note that we can immediately recover the pretopological structure from the preinterior operation (but not from the interior operation nor from the class of all open sets).

Similarly, the __preclosure__ of $A$ is the set $\bar{A}$ of all points that $A$ meets every neighbourhood of:
$$ \{ x \;|\; \forall{U},\; x \stackrel{\circ}\in U \;\Rightarrow\; A \cap U \neq \empty \} .$$
A set $A$ is __closed__ if it equals its preclosure.  The __closure__ $Cl(A)$ of $A$ is the intersection of all of the closed sets containing $A$.  Again, we can recover the pretopological structure from the preclosure operation; $x \stackrel{\circ}\in U$ iff $U$ meets every set $A$ such that $x \in \bar{A}$.  (This result seems to require [[excluded middle]].)

(Warning: not all references use these terms in the same way.  This terminology is based on the premise that a closure should be closed.)


The duality between (pre)interiors and open sets on the one hand and (pre)closures and closed sets on the other hand is (at least if you assume [[excluded middle]]) just what you would expect: the (pre)interior of a [[complement]] is the complement of the (pre)closure, and a set is open if and only if its complement is closed.  However, a preinterior is generally not open but larger than an interior; similarly, a preclosure is generally not closed but smaller than a closure.  The situation looks like this:
$$ A \supseteq \stackrel{\circ}A \supseteq (\stackrel{\circ}A)^{\circ} \supseteq \cdots \supseteq Int(A) ,$$
and
$$ A \subseteq \bar{A} \subseteq \overline{\bar{A}} \subseteq \cdots \subseteq Cl(A) .$$
In many cases this iteration stabilizes after finitely many terms.  The plus power $S^n$ seems to stabilise after $n$ iterations.  And in a topological space, of course, it only takes one step.


In general, however, there can be transfinitely many terms in these sequences.  For example, let $\Omega$ be any [[ordinal number]] (thought of as the [[well-ordered set]] of all smaller ordinal numbers) with the following pretopology:

* $0 \stackrel{\circ}\in U$ iff $U = \Omega$.
* $\alpha \stackrel{\circ}\in U$, where $\alpha \lt \Omega$ is a nonzero ordinal, iff $[\beta,\Omega) \subseteq U$ for some $\beta \lt \alpha$.

Let $A=[1,\Omega)$.  Then $\stackrel{\circ}A = [2,\Omega)$, $(\stackrel{\circ}A)^\circ = [3,\Omega)$, and so on, the process taking $\Omega$ steps to stabilize at $Int(A)=\emptyset$.


Note that an interior is open, and a closure is closed.  Indeed, the open sets in $S$ form a topological structure on $S$, giving the usual meanings of interior, closure, and closed set.  This topological structure does *not* (in general) give the original pretopology on $S$; instead, this makes $Top$ a [[reflective subcategory]] of $Pre Top$.

In the definition of pretopology, the neighbourhoods of each point may be given completely independently of any other point.  So the notion of topological space may also be seen as requiring some coherence between the neighbourhoods of nearby points.


[[!redirects pretopology]]