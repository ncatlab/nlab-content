##Note##

The purpose of this entry is simply to state and prove a result of Dowker that was mentioned at [[Vietoris complex]].  To keep the discussion fairly self contained, certain ideas will be repeated from that, and possibly other, entries.

##The two nerves of a relation: Dowker's construction##

Let $X, Y$ be sets and $R$ a relation between $X$ and $Y$, so $R
\subseteqq X \times Y$. We write $x Ry$ for $(x, y) \in R$.

**Example**
(In addition to those given in [[Vietoris complex]].)

If $K$ is a [[simplicial complex]], its structure is specified by a
collection of non-empty finite subsets of its set of vertices
namely those sets of vertices declared to be simplices. This
collection of simplices is supposed to be downward closed, i.e.,
if $\sigma$ is a simplex and $\tau \subseteqq \sigma$ with $\tau \neq \emptyset$, then $\tau$
is a simplex. For our purposes here, set $X = V_K$ to be the set
of vertices of $K$ and $Y = S_K$, the set of simplices of $K$ with
$x Ry$ if $x$ is a vertex of the simplex $y$. 

**Returning to the general situation** we define two [[simplicial
complex|simplicial
complexes]] associated to $R$, as follows:

1. $K = K_R:$

   * the set of vertices is the set $X$;
   * a $p$-simplex of $K$ is a set $\{x_0, \cdots, x_p\}\subseteq X$ such that there is some $y \in Y$ with $x_i Ry$ for $i = 0, 1, \cdots, p$.

2. $L = L_R :$

   * the set of vertices is the set, $Y$;
   *  $p$-simplex of $K$ is a set $\{y_0, \cdots, y_p\}\subseteq Y$ such that there is some $x \in X$ with $x Ry_j$ for $j  = 0, 1, \cdots, p$.

Clearly the two constructions are in some sense dual to each
other.

**Note** These two simplicial complexes were denoted $V(R)$ and $C(R)$ at [[Vietoris complex]].

We next need some classical subdivision ideas.

###Barycentric  subdivisions###

Combinatorially, if $K$ is a simplicial complex with vertex set $V_K$,
then one associates to $K$ the partially ordered set of its
simplices. Explicitly we write $S_K$ for the set of simplices of $K$
and $(S_K, \subseteq)$ for the partially ordered set with $\subseteq$
being the obvious inclusion. The **barycentric subdivision**, $K'$, of $K$
has $S_K$ as its set of vertices and a finite set of vertices of $K'$
(i.e. simplices of $K$) is a simplex of $K'$ if it can be totally
ordered by inclusion. (Thus $K'$ is the simplicial complex given by
taking the nerve of the poset, $(S_K, \subseteq)$.)