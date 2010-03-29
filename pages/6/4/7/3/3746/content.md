An __entourage__ (aka __vicinity__) is a [[binary relation]] of 'approximate equality' on a [[space]].  Just as a [[topological space]] is given by its [[underlying set]] of points and an appropriate collection of [[open subsets]], so a [[uniform space]] is given by its underlying set of points and an appropriate collection of entourages.  If the intuition behind open subsets is that you can take a point in an open subset, move it a small distance, and get a point in the open subset; then the intuition behind entourages is that you can take any two points related by an entourage, move them anywhere in the space as long as each is only moved a small distance relative to the other, and get two points related by the entourage.


## Examples

*  In a [[metric space]], there is one basic entourage for each positive [[real number]] $\epsilon$:
   $$ x \approx_\epsilon y \;\iff\; d(x,y) \lt \epsilon ,$$
   where $x,y$ are points in the metric space and $d$ is the metric.

*  In a [[gauge space]], there is one basic entourage for each $\epsilon$ and each gauging distance $d$, using the same formula as above.

*  In a [[topological abelian group]], there is one basic entourage for each [[neighbourhood]] $N$ of the identity element:
   $$ x \approx_N y \;\iff\; x/y \in N ,$$
   where $x,y$ are points in the metric space and $/$ is the division operation in the group.

*  In a nonabelian [[topological group]], there are two distinct notions of entourage, one using the same formula as above and the other using $y/x$ in place of $x/y$.

Note that in both cases, there are additional entourages besides these basic ones, by the principle that any relation that contains an entourage is an entourage.


[[!redirects entourage]]
[[!redirects entourages]]
[[!redirects vicinity]]
[[!redirects vicinities]]
