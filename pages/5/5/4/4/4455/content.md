# Dedekind completions
* table of contents
{: toc}

## Idea

While Dedekind completeness was traditionally described in the context of the [[real numbers]], it can be stated for any [[linear order]]. Intuitively, a linear order is _Dedekind complete_ if [[Dedekind cuts]] don't give any 'new' elements.


## Definitions

+--{: .query}
[[David Roberts]]: I lifted the following definition from Paul Taylor's page on Dedekind cuts. It clearly needs expanding.

_Toby_:  I changed [[total order]] to [[linear order]] as a technicality ($ \leq $ vs $ \lt $; constructively the theory is cleaner with the latter, which you were already using).
=--

+-- {: .un_defn}
###### Definition
Let $(S,\lt)$ be a set with a [[linear order]]. $S$ is **Dedekind complete** if every pair of subsets $D, U \subset S$ that satisfies the axioms for a [[Dedekind cut|cut]] is of the form
$$D = \{d|d\lt a\},U = \{u|u \lt a\}$$
for some unique $a\in S$.

We call any linear order $S_D$ which is Dedekind complete equipped with a universal arrow $S \to S_D$ [[the]] **Dedekind completion** of $S$.
=--

The set of Dedekind cuts of [[rational numbers]] -- the real numbers -- is Dedekind complete. In fact starting with any unbounded, [[dense order|dense]] linearly ordered set $S$, the set of Dedekind cuts is isomorphic to the reals as long as $S$ is a [[countably infinite set]]. 

Since the operation of forming the set of Dedekind cuts is idempotent, the Dedekind completion can be constructed as the set of Dedekind cuts.  More precisely, the Dedekind-complete linear orders form a [[reflective subcategory]] of the category of linear orders, so that Dedekind completion is a kind of [[completion]] in the abstract categorial sense.



## References

*  [[Paul Taylor]]\'s [page on Dedekind cuts](http://www.paultaylor.eu/ASD/dedras/classical)


[[!redirects Dedekind complete]]
[[!redirects Dedekind complete order]]
[[!redirects Dedekind-complete order]]
[[!redirects Dedekind completeness]]
