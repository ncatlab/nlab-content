##  Portal Theory
Portal theory is a developing field combining multiple branches of mathematics
and  theoretical physics, in the pursuit of studying portals as hypothetical
topological structures.

Unlike wormholes in general relativity, which arise from spacetime curvature, portal theory
explores a broader class of identifications and gluings that may or may not preserve physical
laws.
The field examines the geometric,
topological, and physical implications of portals, often through abstract models and
computational simulations.

Portal theory emerged from online discussions and speculative fiction inspired conversations in
the early 2020s, gaining rigor through contributions from independent researchers. 
It distinguishes between 
*ambient space*, the underlying manifold before portal identification and
*material space*, the resulting quotient space after gluing. Key axioms, such as **surface irrelevance**, assert that portal behavior depends on boundaries and transformations rather than
surface shapes. The field has been modernized by computational visualizations, enabling
empirical exploration of complex configurations.

##  History
## Early Precursors (Pre-2020)
Portals have appeared in mainstream media, popular all across the video game industry, most
notably in the portal series, but also popped in isolated mathematical and computational works.


The famous video game series portal popularized intuitive portal mechanics,
inspiring questions like "what happens if you put a portal in a portal?" However, the games
simplified rules such as no restricted portal placement highlighted gaps between
fiction and rigorous theory.

## Optozoraxs impact (2020 Onward)
Optozorax Transformed the field around 2023 with his **Portal Explorer** [https://github.com/optozorax/portal], a ray-tracing program
simulating complex interactions like nested portals, or portals with various topologies. This
shifted portal theory from speculation to interactive exploration, resolving paradoxes (e.g.,
seamless portal-in-portal continuity via conceptual splitting) and clarifying properties like
movement and velocity transfer, and answering an age-long debate about relative momentum
between
Inspired by these visualizations, an online community formed and launched the **Portal Theory
Wiki** [https://portaltheory.miraheze.org/wiki/Main_Page] as an attempt to systematize concepts, but suffered from lack
of direction and proper moderation. The wiki closed due to inactivity, underscoring pre-existing
foundational gaps that optozoraxs work addressed.

##  Fundamental Concepts
## Ambient and Material Space
Ambient space refers to the initial manifold(e.g., Euclidean space) before portal creation.
Material space is the quotient space formed by identifying points via gluing. Portals are
constructed by cutting along surfaces and reattaching them, preserving local Euclidean behavior
but altering global topology.

In rigorous terms, ambient space $X$ is a locally compact Hausdorff topological space. A
surface $S \subset X$ satisfies $S = \partial S$, being closed with empty interior. Material
space arises from cutting $X$ along $S$, replacing it with oriented copies (potentially using
orientation double covers for non-orientable surfaces like Möbius strips), and gluing according to
an invertible function $f: S \to S\prime$.
Ambient space is the quotient manifold formed by identifying points via a gluing relation.
Material space is the resulting topological space after gluing, preserving local Euclidean
behavior but altering global topology.

## The Doorway Principle
The foundational insight connecting portals to intuition: a doorway is equivalent to two
back-to-back portals. This principle implies:
# A portal definition is considered valid Iff connecting two portals back-to-back yields a doorway.
# Portal behavior should remain consistent under this transformation.
# Moving portals must preserve this equivalence.

## Axioms and Properties
**Surface Irrelevance**: Portal behavior depends on boundaries and transformations, not on
the surfaces of both entry and exit portals.

**Pocket Dimensions**: When a small portal is placed inside a larger portal a pocket
dimension emerges, an apparently separate space accessible only through the portal
configuration.
Key Properties:
* Finite volume contains infinite space
* Objects exist without touching boundaries
* Space appears "darker" due to light ray entrapment in infinite loops
* No singularities form despite infinite recursion
* Technically exists between portals, not in separate universe
* **Integrity Axiom**: Prevents violations like object overlap or slicing, mainly involves
continuous edges and bijective teleportation.
* **Singularities**: Boundaries create cone points with angle excess (e.g., $2\pi$ for ordinary
portals). One-sided portals form walls as material space boundaries.

##  Mathematical Foundations
## Cut Space
Definition: For ambient space $X$, surface $S \subset X$, and encapsulation $o$:
$Cut(X, S, o) = (X \setminus S)) \sqcup sides(S, o)$
where $sides(S, o)$ represents the set of all sides (directional approaches to surface points).
topology: Generated by:
* Open sets from X \setminus S (subspace topology)
* Sets $O(C, k) = C[k] +$ {$C\prime \in sides(S, o)$ | $C[k]$ strongly touches $C\prime$}
Properties:
* Cut space is Hausdorff
* Homeomorphism-invariant under re-encapsulation
* The "uncut" function uncut: $Cut(X, S) \to X$ is continuous

## Ambiant space


## Material space
Definition: Material space is the quotient:
$M =  Cut(X, S) \setminus \sim$
where $\sim$ identifies sides according to the portal transformation.
For a simple portal: Let $f: S \to S\prime$ be a homeomorphism (portal transformation). The
equivalence relation identifies corresponding points of the doubled boundary according to $f$.
For complex portals: Global gluing patterns specify which sides connect, generalizing the simple
case.

## Surfaces


## Portal functions
A portal function or portal map of a surface $S \subseteq X$ is a homeomorphism 
$h: A \to B$ where $A$ is an open neighborhood of $S$ and $B \subseteq X$

## Topological portals
A topological portal in the ambient space $X$ is the tuple $(S, F, g)$
where $S$ is a a surface in $X$, 
$F$ is a family of portal functions,
and $g$ is a global gluing pattern on $S$ made from $F$

## Monoportals
A monoportal is a topological portal $(S, F, g)$ in standard form where every $h$ in $F$ has codomain $S$. in other words, $h$ is an automorphism.

## Surface Portals
Surface Portals are formally defined as pairs of surfaces $S$ (in) and $S\prime$ (out) in ambient
space $A$, with an invertible function $f: S \to S\prime$. Cutting replaces each with oriented copies
(using double covers for non-orientable cases), then glues right-in to left-out and vice versa.
Material space is the quotient $C \setminus \sim$, where $C$ is cut space and $\sim$ identifies via $f$.

## Portal Surface Independence Theorem
Statement: Let $A$ be an $n$ dimensional manifold. Let $ X, X \prime \setminus A $ with
homeomorphism $ f: X \to X \prime $. Let $S_1, S_2$ be $(n-1)$ dimensional submanifolds of $X$ with
orientations $ O_1, O_2 $ satisfying:
:$ cl(S_1) \ S_1 = cl(S_2) \ S_2 $
Let $f_1= f|_{S_1}$ and $f_2 = f|_{S_2} $.
Conclusion: Material spaces $M_1$ (under $f_1$ with $O_1$) and M_2 (under $f_2$ with
$O_2$) are homeomorphic.

## Types of Portals
Portal theory classifies portals based on construction and properties:


**Spatial Portals**: Geometric artifacts in material space, such as wormholes. They may have
boundaries, take ordinary portals with oval frames as an example or no boundaries like in
spherical portals. This kind of portals include:


**Ordinary Portals**: Standard paired surfaces connecting regions.


**Monoportals**: Single-surface portals mapping to themselves (e.g., under 180° rotation or
point reflection). Variants include regular monoportals, mirroring monoportals, multiple
monoportals, offsetting monoportals, and scaling monoportals.


**Nontrivial Portals**: Complex shapes such as hemispherical portals, trefoil knot portals,
Borromean ring portals, infinite cylindrical portals,  Möbius strip portals, Hopf link portals.


**Distorting Portals**: Alter objects during traversal, including isotropic/anisotropic scaling or
shearing.


**Surface and Transformation Portals**: Constructed by gluing a submanifold $S$ to its image
under an invertible transformation $T$. Affine portals use affine transformations in flat space.
Those can be defined mathematically as the portal surface $S \subset A$ where A is a
manifold, such that $S$ is a submanifold of $A$, and the portal transformation $T: S \to A$ be a
smooth and injective transformation. Material space $X$ is defined as $X = A \setminus \sim$ where
$\sim$ is the smallest equivalence relation such that $ \forall x \in S, x \sim T(x) $.


**Split Doorway Portals**: An alternative definition uses ambient space $A$, a manifold $S$
representing the portal surface, and embeddings $f_1, f_2: S \to A$, identifying these
embeddings. This represents a single abstract surface manifesting in multiple locations.
One formal construction involves an ambient manifold $M$, portal surface $P$ (a manifold of
codimension 1), and a double cover $N$ of $P$ with an involution $f: N \to N$ (fixed-point-free,
$f \circ f = \mathrm{id}$). The material space is the quotient of $M$ with $P$ replaced by $N$,
identifying points via $f$.


**Scanner-Printer Portals**: Non-spatial machines that disassemble and reassemble objects,
conserving velocity in a lab frame. Described mathematically as 
:$P(q) = T(q * O_1) + O_2$,
where $T$ is a linear transformation,
$O_1$ is the origin of the scanner, and
$O_2$ is the origin of
the printer. 
Coupled with axioms like bijectivity and continuity to prevent object tearing.

## Topology
Portal topology studies manifold changes. A pair of ordinary portals in 2D Euclidean space
yields a once-punctured torus (including frames) or homotopy equivalent to a bouquet of circles
(excluding frames). Monoportals have trivial fundamental groups but nontrivial homology.
topological classification of portal-containing spaces:
 
 ... include table


**Observation:** Regular portal motion preserves topological equivalence (homeomorphism type),
but creates pocket dimensions changes.

the topological class (different number of punctures), suggests fundamental constraints on what portal movements are possible.

##  Physical Implications
Portal theory takes major inspiration from physics, mainly kinematics
[https://en.wikipedia.org/wiki/Kinematics] (momentum transformations) and general relativity
[https://en.wikipedia.org/wiki/General_relativity] (accelerating portals creating curvature or
closed timelike curves).

## gravity
TODO add the whole gravity potential stuff
[https://en.wikipedia.org/wiki/Poisson%27s_equation] and gravitational potential.

##  Open Problems
…
##  See Also
* https://en.wikipedia.org/wiki/Topology
* https://en.wikipedia.org/wiki/Wormhole
##  References
* optozoraxs YouTube Channel. https://www.youtube.com/@optozorax_en
* crm4244. Portals GitHub Repository. https://github.com/crm4244/Portals
* crm4244. Proof of Portal Surface Independence.
https://docs.google.com/document/d/1SqYjYLT_yWm8afTKx9RmSxRz5jcswJ-7YT8cd6Sl04Q/
* Portal Theory Wiki. https://portaltheory.miraheze.org/wiki/
