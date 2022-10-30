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

**Note:** These two simplicial complexes were denoted $V(R)$ and $C(R)$ at [[Vietoris complex]].

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

**Note:**

It is important to note that there is in general _no_ natural simplicial
map from $K'$ to $K$. If however $V_K$ is ordered in such a way that
the vertices of any simplex in $K$ are totally ordered (for instance
by picking a total order on $V_K$), then one can easily specify a map

$$ \varphi : K' \rightarrow K$$

by:

if $\sigma' = \{ x_0, \cdots, x_p\}$ is a vertex of $K'$ (so $\sigma'
\in S_K$), let $\varphi \sigma'$ be the least vertex of $\sigma'$ in
the given fixed order.

This preserves simplices, but reverses order so
if $\sigma_1' \subset \sigma_2'$ then $\varphi (\sigma_1') \geq
\varphi(\sigma_2')$.


If one changes the order, then the resulting map is
_contiguous_:

##Contiguity##

 Let $\varphi,~ \psi : K \rightarrow L$ be
two simplicial maps between [[simplicial complex|simplicial complexes]]. They are **contiguous** if for any simplex $\sigma$ of $K$, $\varphi (\sigma) \cup \psi
(\sigma)$ forms a simplex in $L$.


Contiguity gives a constructive form of homotopy applicable to
simplicial maps.

If $\psi : K \rightarrow L$ is a simplicial map, then it induces
$\psi' : K' \rightarrow L'$ after subdivision. As there is no way
of knowing / picking compatible orders on $V_K$ and $V_L$ in
advance, we get that on constructing

$$\varphi_K : K' \rightarrow K$$

and

$$\varphi_L : L' \rightarrow L$$

that $\varphi_L \psi'$ and $\psi \varphi_K$ will be contiguous to each
other but rarely equal.

**Returning to $K_R$ and $L_R$,** we order the elements of $X$ and
$Y$. Then suppose $y'$ is a vertex of $L'_R$, so $y' = \{y_0,
\cdots, y_p\}$, a simplex of $L_R$ and there is an element $x \in
X$ with $x Ry_i, i = 0, 1, \cdots, p$. Set $\psi y' = x$ for one
such $x$.

If $\sigma = \{ y'_0, \cdots, y'_q\}$ is a $q$-simplex of $L'_R$,
assume $y'_0$ is its least vertex (in the inclusion ordering)

$$\varphi_L (y^\prime_0) \in y'_0 \subset y^\prime  for each  y_i \in
\sigma$$

hence $\psi y'_i R \varphi_L (y'_0)$ and the elements $\psi y'_0,
\cdots, \psi y'_q$ form a simplex in $K_R$, so $\psi : L'_R
\rightarrow K_R$ is a simplicial map. It, of course, depends on the
ordering used and on the choice of $x$,  but any other choice $\bar x$
for $\psi y'$ gives a contiguous map.

Reversing the roles of $X$ and $Y$ in the above we get a
simplicial map

$$\bar\psi : K_R' \rightarrow L_R.$$

Applying barycentric subdivisions again gives

$$\bar\psi' : K_R'' \rightarrow L_R'$$

and composing with $\psi : L_R' \rightarrow K_R$ gives a map

$$\psi \bar\psi' : K_R'' \rightarrow K_R.$$

Of course, there is also a map

$$\varphi_K \varphi'_K : K_R''\rightarrow K_R.$$

+--{:. un_proposition}
###### Proposition
(Dowker, 1952, p.88). 

The two maps $\varphi_K \varphi'_K$ and $\psi \bar\psi'$ are contiguous.
=--

Before proving this, note that contiguity implies homotopy and that
$\varphi \varphi'$ is homotopic to the identity map on $K_R$ after
realisation, i.e., this shows that

+--{:.un_theorem}
######Theorem

$|K_R| \simeq |L_R|.$

=--


The homotopy depends on the ordering of the vertices and so is not
natural. 

+--{:.proof}

######Proof of Proposition

Let $\sigma''' = \{ x_0'', x_1'', \cdots, x_q''\}$ be a simplex of
$K_R''$ and as usual assume $x_0''$ is its least vertex, then for all
$i \gt 0$

$$x_0'' \subset x_i''.$$

We have that $\varphi'_K$ is clearly order reversing so $\varphi'_K
x_i'' \subseteq \varphi'_K x_0''$. Let $y = \bar\varphi \varphi'_K
x_0''$, then for each $x \in \varphi'_K x_0''$, $x Ry$. Since $\varphi_K
\varphi'_K x_i'' \in \varphi'_K x_i'' \subseteq \varphi'_K x_0''$, we
have $\varphi_K \varphi'_K x_i'' Ry$.

For each vertex $x'$ of $x_i'', \bar \psi x' \in \bar \psi'
x_i''$, hence as $\varphi'_K x_0'' \in x_0'' \subset x_i'', y =
\bar \psi \varphi'_K xx_0'' \in \bar \psi' x_i''$ for each $x_i
''$, so for each $x_i'', \psi \bar \psi' x_i'' Ry$, however we
therefore have 

$$ \varphi_k \varphi'_K (\sigma '') \cup \psi \bar \psi (\sigma''') = \bigcup \varphi_k \varphi'_K (x_i'')\cup \psi \bar \psi; x_i ''$$ 

forms a simplex in $K_R$, i.e.
$\varphi_K \varphi'_K$ and $\psi \bar \psi'$ are contiguous.

=--