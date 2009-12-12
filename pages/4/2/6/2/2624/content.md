A _short map_ is a well-behaved sort of [[morphism]] of [[metric spaces]] (or a generalisation of metric spaces, such as the extended quasi-pseudo-versions, or [[gauge spaces]] or [[prometric spaces]]).  Short maps go by many names in the literature, often ad hoc, such as _distance-nonincreasing maps_ and _weak contractions_, but 'short map' seems to be increasing in popularity.


## Definition

A [[function]] $f\colon X \to Y$ is __short__ if $d_Y(f(a),f(b)) \leq d_X(a,b)$ for every $a,b \in X$.  Here $d_X$ and $d_Y$ are the [[metrics]] (or generalisations of metrics) on $X$ and $Y$.  If $X$ and $Y$ are (or may be) gauge spaces and so have several (pseudo)metrics on them, then we require that, for every gauging distance $d_X$ on $X$, there exists a gauging distance $d_Y$ on $Y$ such that the above inequality holds; here, $d_Y$ must be independent of $a$ and $b$.


## Justification

There are many other kinds of maps between metric spaces; [[continuous maps]] and [[uniformly continuous map]]s are more general, while [[isometries]] and [[contraction]]s are more restrictive.  What\'s so special about short maps that we consider them the proper morphisms between metric spaces?

One answer is to look at [[Lawvere]]\'s characterisation of metric spaces as certain [[enriched categories]]; see [[Lawvere metric space]].  Then the short maps are precisely the [[enriched functors]] between metric spaces.

Another answer is to consider what the [[isomorphisms]] between metric spaces are; these are clearly (by the definition of metric spaces as [[structured sets]]) the global isometries.  So for a good notion of morphism, we need to recover global isometries as isomorphisms.  Using continuous or uniformly continuous maps, we recover [[homeomorphisms]] or uniform homeomorphisms as isomorphisms, which are too general; this really gives us the category of metrisable [[topological spaces]] or of metrisable [[uniform spaces]] rather than the category of metric spaces.  Using contractions, we do not even get a category; the [[identity function]] is not a contraction.  We could still use global isometries themselves as morphisms, but since this defines a [[groupoid]], we should look for a more general notion of morphism that still gives global isometries as isomorphism.  And short maps do that.

Short maps give the [[Met|category of metric spaces]] some nice properties.  In particular, $Met$ is [[complete category|complete]], which does not hold using either global isometries or distance-preserving maps as morphisms.  This interacts with the properties of the category of [[Banach spaces]]; as a Banach space may be defined as a set with compatible vector-space and metric-space structures, so a Banach space morphism is a function that is both linear and short.

[[!redirects short maps]]
[[!redirects distance-nonincreasing map]]
[[!redirects distance-nonincreasing maps]]
[[!redirects weak contraction]]
[[!redirects weak contractions]]
