
#Contents#
* table of contents
{:toc}

##Idea##

A **generalized graph** in the sense of [HRY](#HRY) is a generalization of the notion of a pseudograph given at [[graph]] (see in particular [Definition in terms action on a set of half edges](https://ncatlab.org/nlab/show/graph#definition_in_terms_of_action_on_a_set_of_halfedges)). By adding structure like directions for the edges, we can define a [[wheeled graph]] which is a generalization of a [[directed pseudograph]]. What differentiates a generalized graph from a pseudograph and a wheeled graph from a [[directed pseudograph]] is the notion of an "exceptional cell," which should be thought of as a set of half edges which have no vertices. 

A generalized graph can be visualized as a set of vertices with half edges attached to them, a rule for attaching half edges to glue the vertices together, and potentially some half edges (flags) that are attached to only one or zero vertices. For instance, a particularly simple generalized graph is one with no vertices and one edge. 

## Definitions ##
 The following is Definition 2.2 of [HRY](#HRY):

+-- {: .num_defn }
###### Definition

A generalized graph $G$ is a finite set $Flag(G)$ with:

   * a partition of $Flag(G)=\coprod_{\alpha\in A} F_\alpha$ into **cells** with $A$ finite,

   * a distinguished partition subset $F_\epsilon$ called the **exceptional cell**,

   * an involution $\iota$ satisfying $\iota F_\epsilon\subseteq F_\epsilon$,

   * and a free involution $\pi$ on the set of $\iota$-fixed points of $F_\epsilon$. 
=--

Given a generalized graph $G$, Definition 2.3 of [HRY](#HRY) gives some useful terminology:

+-- {: .num_defn }
###### Definition
1. The elements of $Flag(G)$ are called **flags**. A flag in a non-exceptional (resp. exceptional) cell is called an **ordinary flag** (resp. **exceptional flag**).
1. Call $G$ an **ordinary graph** if $F_\epsilon$ is empty.
1. Each non-exceptional partition subset $F_\alpha\neq F_\epsilon$ is called a **vertex**. The set of vertices is denoted by $Vt(G)$. An empty vertex is an **isolated vertex**. A flag in a vertex is said to be **adjacent to** or **attached to** that vertex.
1. An $\iota$-fixed point is a **leg** of $G$. The set of legs is denoted by $Leg(G)$. An **ordinary leg** (resp. **exceptional leg**) is an ordinary (resp. exceptional) flag that is also a leg. For an $\iota$-fixed point $x\in F_\epsilon$, the pair $\{x,\pi x\}$ is called an **exceptional edge**.
1. A 2-cycle of $\iota$ consisting of ordinary flags is called an **ordinary edge**. A 2-cycle of $\iota$ contained in a vertex is a **loop**. A vertex that does not contain any loop is called **loop free**. A 2-cycle of $\iota$ contained in the exceptional cell is called an **exceptional loop**. 
1. An **internal edge** is any 2-cycle of $\iota$. An **edge** is an internal edge, an exceptional edge, or an ordinary leg. The set of edges of $G$ (resp. internal edges) is denoted $Edge(G)$ (resp. Edge_i(G))$. 
1. An ordinary edge $e=\{e_0,e_1\}$ is said to be **adjacent to** or **attached to** a vertex $v$ if either $e_0$, $e_1$ or both are adjacent to $v$.  
=--


##Extra Structure##

There are a number of important structures that a generalized graph can possess which will be useful in using them to describe [[properads]]. The following is again from [HRY](#HRY):

+-- {: .num_defn }
###### Definition 

Suppose $G$ is a generalized graph. Fix a (possibly infinite) set of _colors_ $\mathcal{C}$.

1. A **coloring** of $G$ is a function $Flag(G)\overset{\kappa}\to \mathcal{C}$ that is constant on orbits of $\iota$ and $\pi$.

1. A **direction** for $G$ is a function $Flag(G)\overset{\delta}\to \{-1,1\}$ such that
    * if $\iota x\neq x$, then $\delta(\iota x)=-\delta(x)$, 
    * and if $x \in F_\epsilon$, then $\delta(\pi x)=-\delta (x)$.  

1. For $G$ with direction, an **input** (resp. **output**) of a vertex $v$ is a flag $x\in v$ such that $\delta(x)=1$ (resp. $\delta(x)=-1$). An **input** (resp. **output**) of $G$ is a leg $x$ such that $\delta(x)=1$ (resp. $\delta(x)=-1$). For $u\in Vt(G)\cup \{G\}$, the set of inputs (resp. outputs) of $u$ is written $in(u)$ (resp. $out(u)$).

1. A **listing** for $G$ with direction is a choice for each $u\in Vt(G)\cup \{G\}$ of a bijection of pairs of sets 
$$
(in(u),out(u))\overset{l_u}\to(\{1,\ldots,|in(u)|\},\{1,\ldots,|out(u)|\}).
$$
=--

Thus, using these properties, we can model [[PROPs]] and [[properads]] with generalized graphs. See there and [[wheeled graph]] for more. 

## Related concepts

* [[graph]]

* [[quiver]]

## References




* {#HRY}  [[Philip Hackney]], [[Marcy Robertson]] and [[Donald Yau]]. _Infinity Properads and Infinity Wheeled Properads_,  Lecture Notes in Mathematics, 2147. Springer, Cham, 2015. [(arxiv version)](http://arxiv.org/pdf/1410.6716v2.pdf)


* {#kock} [[Joachim Kock]]. _Graphs, hypergraphs, and properads_, [arXiv:1407.3744](https://arxiv.org/pdf/1407.3744v3.pdf). 




