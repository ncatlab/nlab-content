
# Rank
* table of contents
{: toc}

## Idea

The term 'rank' is used in many contexts to number levels within a hierarchy.


## Rank of a module

Let $A$ be a [[ring]] and $N$ a [[module]] over $A$. If $A$ is a [[field]], then $N$ is a [[vector space]] and we speak of the _[[dimension]]_ of $N$; in the general case, we may speak of the _rank_.

A collection of elements $(w_i)_{i \in I}$ of $N$ is called a [[basis]] of $N$ (over $A$) if for every $x \in N$ there is a unique collection $(a_i)_{i \in I}$ of elements of $A$ such that $a_i = 0$ for all but finitely many $i \in I$ and $x = \sum_{i \in I} a_i w_i$. 

If $N$ has a basis it is called _free_ (over $A$). For many examples of $A$ (the __invariant basis number rings__), the [[cardinality]] $# I$ only depends on $N$ and not on the choice of basis. It is called the **rank** of $N$ over $A$, notation: $rank_A(M)$. In any case, $N$ is called the __free module of rank $# I$__. If $N$ is a [[finitely generated]] free module then the rank is finite.


## Hereditary rank of a pure set

Every [[pure set]] within the [[von Neumann hierarchy]] appears first at some level given by an [[ordinal number]]; this number is its __hereditary rank__.

We may define this rank explicitly (and [[recursion|recursively]]) as follows:

$$ rank S = \bigcup_{x \in S} (rank x)^+ ,$$

where $\bigcup$ is the [[supremum]] operation on ordinals (literally the [[union]] for [[von Neumann ordinals]]) and $(-)^+$ is the [[successor]] operation (which is $a \mapsto a \cup \{a\}$ for von Neumann ordinals).
