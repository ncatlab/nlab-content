## Idea ##

While Dedekind completeness was traditionally described in the context of the [[real numbers]], it can be stated for any [[total order]]. Intuitively, a total order is _Dedekind complete_ if [[Dedekind cuts]] don't give any 'new' elements.

##Definition##

+--{: .query}
[[David Roberts]]: I lifted the following from [Paul Taylor's page](http://www.paultaylor.eu/ASD/dedras/classical) on Dedekind cuts. It clearly needs expanding.
=--

**Definition**: Let $(S,\lt)$ be a set with a [[total order]]. $S$ is **Dedekind complete** if every pair of subsets $D, U \subset S$ that satisfies the axioms for a cut is of the form
$$D = \{d|d\lt a\},U = \{u|u \lt a\}$$
for some unique $a\in S$.

The set of Dedekind cuts of rational numbers - the real numbers - are Dedekind complete. 

We call any total order $S_D$ which is Dedekind complete equipped with a universal arrow $S \to S_D$ the _Dedekind completion_ of $S$.

+--{: .query}
[[David Roberts]]: Sanity check on the following please. It is a guess.
=--

Since the operation of forming the set of Dedekind cuts is idempotent, the Dedekind completion can be constructed as the set of Dedekind cuts.