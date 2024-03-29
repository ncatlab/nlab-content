
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents

* tic
{: toc}

## Idea

There are many situations in [[algebraic topology]] in which one wants to work in a "Really Big Space".  Often, it is not that important which space is used, so long as it has some basic properties.  A common feature that one wants of these spaces is that certain derived spaces be contractible.  In many cases, it is possible to write down an actual contraction (rather than arguing from general nonsense) and in those cases, the contraction often uses the ability to "shift" pieces of the space from one place to another.  This leads us to consider the notion of a **shift map**, and its cousin a **split map**, which provide enough structure to define the required contractions.

In short, a **shift map** is a generalisation of the obvious shift map $\ell^0 \to \ell^0$ given by $(x_1,x_2,x_3,\dots) \mapsto (0,x_1,x_2,x_3,\dots)$.  It is an inclusion (even an embedding) and its [[eventual image]], $\bigcap_k \im S^k$, is zero.
Note that a shift map on $V$ induces an isomorphism $V \cong \mathbb{R} \oplus V$, but the existence of a shift map is a stronger condition than that.

A **split map** is similar, except that the induced decomposition is $V \cong V \oplus V$.


## Definition

+-- {: .num_definition #defshift}
###### Definition

Let $V$ be a [[LCTVS|locally convex topological vector space]] over $\mathbb{R}$.
Let $k \in \mathbb{N}$.
A **shift map** of order $k$ on $V$ is a continuous linear map $S \colon V \to V$ with the following properties:

1. $S$ is an embedding of $V$ onto a closed subspace of $V$ of codimension $k$ (so that $V \cong \mathbb{R}^k \oplus V$), and
2. $\bigcap_k \im S^k = \{0\}$.

A locally convex topological vector space that admits a shift map will be called a **shiftable space**.  The pair $(V,S)$ will be called a **shift space**.
=--

+-- {: .num_definition #defsplit}
###### Definition

Let $V$ be a [[LCTVS|locally convex topological vector space]] over $\mathbb{R}$.
A **split map** on $V$ is a continuous linear map $S \colon V \to V$ with the following properties:

1. $S$ is an embedding of $V$ onto a closed subspace of $V$ with complement also isomorphic to $V$, (so that $V \cong V \oplus V$), and
2. $\bigcap_k \im S^k = \{0\}$.

A locally convex topological vector space that admits a split map will be called a **splittable space**.  The pair $(V,S)$ will be called a **split space**.
=--

There are obvious generalisations for other fields than $\mathbb{R}$.


## Note on Notation

This is new terminology, invented to give a consistent way to refer to these spaces with their properties.  At time of writing [no existing name for this was known](http://mathoverflow.net/questions/82108/is-there-a-standard-notation-for-a-shift-space-in-functional-analysis).


[[!redirects shift map]]
[[!redirects shift maps]]
[[!redirects Shift map]]
[[!redirects Shift maps]]
[[!redirects shift space]]
[[!redirects shift spaces]]
[[!redirects Shift space]]
[[!redirects Shift spaces]]
[[!redirects shiftable space]]
[[!redirects shiftable spaces]]
[[!redirects Shiftable space]]
[[!redirects Shiftable spaces]]

[[!redirects split map]]
[[!redirects split maps]]
[[!redirects Split map]]
[[!redirects Split maps]]
[[!redirects split space]]
[[!redirects split spaces]]
[[!redirects Split space]]
[[!redirects Split spaces]]
[[!redirects splittable space]]
[[!redirects splittable spaces]]
[[!redirects Splittable space]]
[[!redirects Splittable spaces]]
