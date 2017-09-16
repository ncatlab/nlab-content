A gauge space is a [[topological space]] (necessary completely regular) whose topology is given by a family of [[metric space|pseudometrics]].  More generally, a quasigauge space is a space (not necessarily completely regular) whose topology is given by a family of quasipseudometrics.

Actually, a gauge space has additional structure, so that it can be seen as giving a (completely regular) [[Cauchy space]], a [[uniform space]], or even a generalisation of a [[metric space]] in which the category $Met$ of metric spaces and short maps is a [[full subcategory]].

Please note that, while this is based on the presentation in _[[HAF]]_, the precise definitions of the objects and morphisms of the [[category]] of gauge spaces below constitute original research.  (In particular, _HAF_ really considers the category of pregauge spaces and uniformly continuous maps, which is equivalent to the category of [[uniform space]]s, since it uses them only to study that category.)


## Definitions

Given a [[set]] $X$, a __pregauge__ on $X$ is simply a family of [[metric space|pseudometrics]] on $X$.  A __gauge__ is a $\geq$-[[filter]] of pseudometrics on $X$, that is a collection $G$ of __gauging distances__ such that

1.  There is an element of $G$; in the light of (3), the zero pseudometric $( x, y \mapsto 0 )$ is a gauging distance.
1.  Given $d, e \in G$, some $f \in G$ satisfies
    $$ d(x,y), e(x,y) \leq f(x,y) $$
    for all $x, y$ in $X$; in the light of (3), the pseudometric $( x, y \mapsto max(d(x,y), e(x,y)) )$ is a gauging distance.
1.  Given $d \in G$ and any pseudometric $e$ on $X$, if
    $$ e(x,y) \leq d(x,y) $$
    for all $x, y$ in $X$, then $e \in G$.

A pregauge satisfying axioms (1&2) is a __base__ for a gauge; a base is precisely what generates a gauge by taking the downward closure.  Any pregauge whatsoever is a __subbase__ for a gauge; a subbase is precisely what generates a base by closing under finitary [[join]]s.


A __gauge space__ is a set equipped with a gauge.  A __quasigauge__ is a collection of quasipseudometrics satisfying (1--3); a __quasigauge space__ is a set equipped with a quasigauge.


Given (quasi)gauge spaces $X$ and $X'$, a __short map__ from $X$ to $X'$ is a [[function]] $F$ (on their underlying sets) such that the [[pullback]] along $F$ (or along $F \times F$, to be precise) of any gauging distance on $X'$ is a gauging distance on $X$.  That is,

*  for every $e \in G'$, there is a $d \in G$ such that
   $$ e(F(x),F(y)) \leq d(x,y) $$
   for all $x, y$ in $X$; in the light of (3), the pseudometric $( x, y \mapsto e(F(x),F(y)) )$ (this is the pullback) is a gauging distance.

(Warning: this definition of short map is probably the most significant original research on this page.)


Gauge spaces and short maps between them form the [[category]] $Gau$ of gauge spaces; quasigauge spaces and short maps between them form the category $QGau$ of quasigauge spaces.  Note that any gauge is a base for a quasigauge; in this way, $Gau$ is ([[equivalence of categories|equivalent to]]) a [[full subcategory]] of $QGau$.


## Examples

The categories $Gau$ and $QGau$ are not well known, but some of their subcategories are.

*  A [[metric space]] (or pseudometric space) defines a gauge space, taking its single (pseudo)metric as a base; similarly, a quasi(psuedo)metric space defines a quasigauge space.  Taking short maps (in the usual sense, that is distance-nonincreasing functions) as morphisms, the categories $Met$ and $PsMet$ are full subcategories of $Gau$; similarly, $QMet$ and $QPsMet$ are full subcategories of $QGau$.

*  A [[uniform space]] $X$ defines a gauge space, consisting of all of the pseudometrics on $X$ that are uniformly continuous as maps from $X \times X$ to the real line; similarly, a quasiuniform space defines a quasigauge space.  Taking uniformly continuous maps as morphisms, the category $Unif$ is a full subcategory of $Gau$; similarly, $QUnif$ is a full subcategory of $QGau$.  Thus, uniform spaces can be viewed as gauge spaces whose collection of gauging distances is "saturated."

*  A completely regular [[topological space]] $X$ defines a gauge space, consisting of all the pseudometrics on $X$ that are continuous as maps from $X \times X$ to the real line.  In this way the category $CReg Top$ of completely regular spaces and continuous maps is a full subcategory of $Gau$; it is in fact contained in $Unif$.  (In general, a completely regular space can be uniformized in many ways; this inclusion corresponds to the "initial" uniformity.)

*  An arbitrary topological space defines a quasigauge space in a more complicated way.  Given any open set $U$ in a space $X$, define the pseudometric (in fact a pseudoultrametric) $d_U$ as follows:
   $$ d_U(x,y) = \begin{cases} 0 & if\; x \in U \;\Rightarrow\; y \in U ,\\ 1 & if\; x \in U \;\wedge\; y \notin U ;\end{cases} $$
   then the $d_U$ form a base for a quasigauge, which induces the original topology on $X$.  In other words, every space is "quasigaugeable."  In this way $Top$ also becomes a full subcategory of $QGau$.

Note, though, that these various inclusions are not "compatible."  Any metric induces a uniformity, but the triangle
$$\array{Met &\to& Unif \\ & \searrow &\downarrow \\ && Gau}$$
does not commute.  (In particular, note that $Met\to Unif$ is not full, whereas both inclusions into $Gau$ are.)  Likewise, any uniformity induces a topology, but
$$\array{Unif &\to& Top \\ & \searrow &\downarrow \\ && QGau}$$
does not commute.


## Reflections

Many of these full subcategories of $Gau$ and $QGau$ are [[reflective subcategory|reflective]].

>Details to come


## References

*  Eric Schechter; 1997; [[HAF|Handbook of Analysis and its Foundations]]; Academic Press, 1st ed (1996).