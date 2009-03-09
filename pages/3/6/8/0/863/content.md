# Idea #

A _linear order_ is the irreflexive version of a [[total order]].  In classical mathematics, the distinction between these two concepts is merely a terminological technicality, which is not always observed; more precisely, there is a [[natural isomorphism|natural bijection]] between the set of total orders on a given set $S$ and the set of linear orders on $S$, and one distinguishes them by the notation $\lt$ (for the irreflexive relation) and $\le$ (for the reflexive one).  In [[constructivism|constructive mathematics]], however, they are irreducibly different.

# Definition #

A **linear order** on a set $S$ is a (binary) [[relation]] $\lt$ with the following properties:
* irreflexivity: $x \nless x$;
* asymmetry: $x \lt y$ and $y \lt x$ cannot both be true;
* transitivity: if $x \lt y \lt z$, then $x \lt z$;
* comparison: if $x \lt z$, then $x \lt y$ or $y \lt z $;
* linearity: if $x \nless y$ and $y \nless x$, then $x = y$;
* (in classical mathematics) trichotomy: either $x \lt y$, $x = y$, or $y \lt x$.

Actually, these axioms are overkill.