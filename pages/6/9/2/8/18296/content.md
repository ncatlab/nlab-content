
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contets#
* table of contents
{:toc}

## Statement

+-- {: .num_prop }
###### Proposition


Let $X$ be a [[topological space]] which is

1. [[locally compact topological space|locally compact]] (in the sense that every point has an [[open neighbourhood]] whose [[topological closure]] is [[compact topological space|compact]]),

1. [[second-countable topological space|second-countable]],

Then $X$ is [[sigma-compact topological space|sigma-compact]].

In particular then $X$ is also [[paracompact topological space|paracompact]] since [[locally compact and sigma-compact spaces are paracompact]].

=--

+-- {: .proof}
###### Proof

We need to produce a [[countable cover]] of $X$ by [[compact subspaces]].

By [[second-countable topological space|second-countability]] there exists a [[countable set|countable]] [[base for a topology|base]] of open subsets

$$
  \beta 
    =
  \left\{
    B_i \subset X
  \right\}_{i \in I}
  \,.
$$

By [[locally compact topological space|local compactness]], every point $x \in X$ has an open neighbourhood $V_x$ whose [[topological closure]] $Cl(V_x)$ is [[compact topological space|compact]].

By definition of [[base of a topology]], there exists $B_x \in \beta$ such that ${x} \subset B_x \subset V_x$, hence $Cl(B_x) \subset Cl(V_x)$. Since $Cl(V_x)$ is compact by assumption, and since [[closed subspaces of compact spaces are compact]] it follows that $B_x$ is compact.

Applying this for each point yields that 

$$
  X = \underset{x \in X}{\cup} Cl(B_x)
  \,.
$$

But since there is only a [[countable set]] of base elements $B$ to begin with, there is a countable subset $J \subset X$ such that 

$$
  X = \underset{x \in J}{\cup} Cl(B_x)
  \,.
$$

Hence

$$
  \{Cl(B_x) \subset X\}_{x \in J}
$$

is a countable cover of $X$ by compact subspaces.

=--

## Related statements

* [[locally compact and sigma-compact spaces are paracompact]]

* [[second-countable regular spaces are paracompact]]

[[!redirects locally compact and second-countable spaces are paracompact]]
