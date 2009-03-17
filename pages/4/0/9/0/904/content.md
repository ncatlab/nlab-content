# Idea #

The fundamental group $\pi_1(X,a)$ of a pointed space $(X,a)$ is the group of [[loop]]s at $x$ ([[path]]s from $x$ to $x$), with multiplication defined by concatenation (following one path by another).  As concatenation is not actually associative, we have to define things up to homotopy, but it works out.

For a (path)-[[connected space]], all of the fundamental groups are isomorphic, no matter which point is chosen, so one sometimes speaks of 'the' fundamental group of a connected space.  However, this does not follow the yoga of the [[generalized the]], so careful description of the functors involved still requires using a pointed space.

The fundamental group $\pi_1(X,a)$ generalises in one direction to the [[fundamental groupoid]] $\Pi_1(X)$, or in another direction to the [[homotopy group]]s $\pi_n(X,a)$.  (Ultimately, all of this should be contained within the [[fundamental infinity-groupoid]] $\Pi(X)$.)

# Non-locally 'nice' spaces and 'generalised' spaces#
The definition of fundamental group in terms of homotopy classes of loops at a base point does not work well for the spaces that occur in algebraic geometry, nor for many spaces considered in analysis as there may be very few loops.  For instance, for a scheme there are in general very few paths, and Grothendieck gave a definition of a fundamental group in SGA1 which is closely related to the [[Galois group|Galois groups]] of number theory, but in cases where both the path based and this [[algebraic fundamental group]] make sense, the algebraic form tends to be related to the [[profinite completion of a group|profinite completion]] of the topological fundamental group; see the example in that entry.

A similar type of construction gives the [[fundamental group of a topos]]. Other related forms include a Cech version of the fundamental group used in shape theory, and linked to Cech homology groups of a compact space.