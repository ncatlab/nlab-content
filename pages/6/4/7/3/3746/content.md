
# Entourages
* table of contents
{: toc}

## Idea

An _entourage_ (aka _vicinity_) is a [[binary relation]] of 'approximate equality' on a [[space]], generally a [[uniform space]].  Just as a [[topological space]] is given by its [[underlying set]] of points and an appropriate collection of [[open subsets]], so a [[uniform space]] is given by its underlying set of points and an appropriate collection of entourages.

Entourages are actually a uniformization of [[neighbourhoods]] rather than of open sets as such.  Given a point $x$, a neighbourhood $U$ of $x$ defines a generalized notion of distance from $x$; a point $y$ is [less than] this distance from $x$ iff $y \in U$.  Uniformizing this, an entourage $E$ defines a generalized notion of uniform distance; two points $x$ and $y$ are [less than] this distance from each other iff $(x,y) \in E$.  Or said another way, if $U$ is a neighbourhood of $x$, then any point $y$ that is sufficiently close to $x$ will be in $U$; if $E$ is an entourage, then any two points $x$ and $y$ that are sufficiently close together will be related by $E$.


## Definitions

The precise definition depends on the context.

*  In a [[metric space]], a relation $\approx$ is an __entourage__ if there exists a positive [[real number]] $\epsilon$ such that
   $$ d(x,y) \lt \epsilon \;\implies\; x \approx y ,$$
   where $x,y$ are points in the metric space and $d$ is the metric.

*  In a [[gauge space]], $\approx$ is an __entourage__ if there exists an $\epsilon$ and a gauging distance $d$ such that the preceding condition holds.

*  In a [[topological abelian group]], $\approx$ is an __entourage__ if there is a [[neighbourhood]] $N$ of the identity element such that
   $$ x/y \in N \;\implies\; x \approx y ,$$
   where $x,y$ are points in the metric space and $/$ is the division operation in the group.

*  In a nonabelian [[topological group]], there are two distinct notions of entourage, one using the same formula as above and the other using $y/x$ in place of $x/y$.

*  Of course, the most general kind of entourage is that occurring in the definition of a [[uniform space]], in the same way that [[open sets]] occur in the definition of a [[topological space]].


## Infinitesimal entourages

In [[nonstandard analysis]], every point $x$ in a [[topological space]] $X$ has an infinitesimal neighbourhood in the nonstandard extension $X^*$, called the [[halo]] (or monad) of $x$.  This is to be thought of as the set $\{ y \in X^* \;|\; y \simeq x \}$ of all of the [[hyperpoint]]s that are infinitely close ([[adequality|adequal]]) to $x$.  Similarly, any [[uniform space]] $X$ has an infinitesimal entourage in its nonstandard extension $X^*$, a binary relation $\{ x \in X^*,\; y \in X^* \;|\; y \simeq x \}$ that relates two hyperpoints iff they are infinitely close to each other.  (So the infinitesimal entourage is simply the [[adequality]] relation.)


[[!redirects entourage]]
[[!redirects entourages]]
[[!redirects vicinity]]
[[!redirects vicinities]]
