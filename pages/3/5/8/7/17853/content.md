
# Uniformly regular spaces
* table of contents
{: toc}

## Idea

In [[classical mathematics]], every [[uniform space]] is a [[regular space]], and indeed a [[completely regular space]].  In [[constructive mathematics]], however, this fails to be true.  The notion of *uniformly regular* uniform space is an intermediate notion in between regularity and complete regularity for uniform spaces, which is frequently useful in the constructive theory of uniform spaces; classically every uniform space is uniformly regular.  (Indeed, some authors include uniform regularity in the constructive *definition* of a uniform space.)


## Definition

Let $X$ be a [[uniform space]].  When the uniformity of $X$ is defined in terms of entourages, then $X$ is **uniformly regular** if it satisfies the following property:

* For every entourage $U$, there exists an entourage $V$ such that $\neg{V} \cup U = X \times X$, where $\neg{V}$ is the [[complement]] of $V$. That is,
  $$ \forall U,\; \exists V,\; \forall x, y,\; x \approx_U y \;\vee\; x \mathbin{&#8777;}_V y .$$

With [[excluded middle]], we can take $V$ to be $U$ itself, so every uniform structure is uniformly regular in classical mathematics.  Note that any uniformity induced by a [[gauge space|gauge]] is uniformly regular (as long as the gauging distances take values in [[located real numbers]] as is usually understood).

When the uniformity of $X$ is defined in terms of uniform covers, then the equivalent condition is:

*  If $C$ is a uniform cover, there exists a uniform cover $C'$ such that, for any two points $x, y$, either $x, y \in A$ for some $A \in C$ or $x, y \in B$ for no $B \in C'$.

With [[excluded middle]], we can take $C'$ to be $C$.

Note that uniform regularity is not literally a "uniformization" of [[regular space|regularity]] but rather of [[locally decomposable space|local decomposability]]; so it could also be called **uniform local decomposability**.  In the case of uniform spaces, it implies regularity (see below), so we generally call it uniform regularity; however, for [[quasi-uniform spaces]] we should probably speak instead about uniform local decomposability.


## Examples

* Every [[metric space]], and indeed any [[gauge space]], is uniformly regular, as long as the metric(s) take values in [[located real numbers]].  It suffices to consider a basic entourage $U_{d,\varepsilon} = \{ (x,y) \mid d(x,y)\lt\varepsilon \}$, in which case we can take $V = \{ (x,y) \mid d(x,y)\lt\varepsilon/2 \}$ and use the fact that every located real number is either $\lt \varepsilon$ or $\gt \varepsilon/2$.

* A [[discrete space|discrete]] uniform space is uniformly regular if and only if the underlying set has [[decidable equality]].  (Indeed, a discrete topological space is [[regular space|regular]] if and only if it has decidable equality.)  Thus, the statement "every uniform space is (uniformly) regular" is equivalent to [[excluded middle]].

* In particular, not every [[topological group]] is uniformly regular: any group without decidable equality can be equipped with the discrete topology.  However, the classical examples of Lie groups and [[topological vector spaces]] (TVSs) are uniformly regular.

* However, if a topological group is a [[regular space]], then it is uniformly regular.  For if $U$ is any neighborhood of the identity $e$ in a topological group $X$, by regularity we have a neighborhood $V$ of $e$ and an open set $G$ with $V\cap G = \emptyset$ and $G\cup U = X$, and in particular $\neg V\cup U = X$, whence the entourages defined by $U$ and $V$ satisfy the desired condition.

* Every [[completely regular space|completely regular]] uniform space should be uniformly regular, although the correct constructive definition of "completely regular" is not entirely clear.


### Compact spaces

The examples above show that uniform regularity coincides with regularity for discrete uniform spaces and topological groups.  Another class of spaces for which this holds are compact ones.

+--{: .un_theorem}
###### Theorem
Every [[compact space|compact]] [[regular space]] admits a unique compatible uniformity that is uniformly regular.
=--

+--{: .proof}
###### Proof
Let $X$ be compact regular.  Since compactness and regularity are properties of the open-set lattice, $X$ is still compact regular when regarded as a locale, and hence also Hausdorff as a locale.  Moreover, it is locally compact, and hence the locale and spatial products $X\times X$ coincide.  Furthermore, $X\times X$ is also compact regular.

Define the entourages to be all the neighborhoods of the diagonal in $X\times X$; this obviously satisfies all the axioms of a uniformity except possibly the square-root (and uniform regularity).

Let $U$ be a neighborhood of the diagonal in $X\times X$.  Since $X\times X$ is regular, and using the definition of the product topology, for each $x\in X$ there is a square neighborhood $V_x\times V_x$ and an open set $G_x\subseteq X\times X$ such that $(V_x\times V_x)\cap G_x = \emptyset$ and $G_x \cup U = X\times X$.  The open sets $V_x$ cover the compact space $X$, hence finitely many of them suffice.  Let $V = (V_{x_1}\times V_{x_1}) \cup \cdots \cup (V_{x_n}\times V_{x_n})$, and $G = G_{x_1} \cap \cdots \cap G_{x_n}$.  Then $V$ is a neighborhood of the diagonal, and $G$ an open set such that $G\cup U = X\times X$ and $V \cap G = \emptyset$.  In particular, $\neg V \cup U \subseteq G\cup G = X\times X$, so this uniformity (if it exists) is uniformly regular.

Now, $G$ is the union of rectangular open neighborhoods $A\times B$.  Note that since $G$ is disjoint from the diagonal, any $A\times B \subseteq G$ satisfies $A\cap B = \emptyset$.  Moreover, since $X$ is regular, each $A$ and $B$ is the union of open sets that are well-inside it; thus $G$ is the union of rectangular open neighborhoods $C\times D$ such that there are opens $A,B$ with $C\triangleleft A$ and $D\triangleleft B$ and $A\cap B = \emptyset$.  Since $G\cup U = X\times X$ and $X\times X$ is compact, we can cover it by $U$ together with finitely many such rectangles $C\times D$, say $X\times X = U \cup (C_1\times D_1) \cup\cdots \cup (C_m \times D_m)$.

For each of these rectangles $C_i\times D_i$, let $E_i$ be an open set such that $E_i \cup A_i \cup B_i = X$ and $E_i \cap (C_i \cup D_i) = \emptyset$, and let $W_i = (A_i\times A_i) \cup (B_i \times B_i) \cup (E_i \times E_I)$.  Then $W_i$ is a neighborhood of the diagonal; let $W = W_1 \cap \cdots \cap W_m$.

We claim $W\circ W \subseteq U$.  Let $(x,z) \in W\circ W$, so that there is a $y$ with $(x,y)\in W$ and $(y,z) \in W$.  Now we have either $(x,z)\in U$ (which is what we want) or $(x,z) \in C_i\times D_i$ for some $i$, so it suffices to rule out the latter possibility.  Since $(x,y)\in W$, we have $(x,y) \in W_i$, hence $(x,y)\in A_i\times A_i$ or $(x,y)\in B_i\times B_i$ or $(x,y)\in E_i\times E_i$.  But $x\in C_i$, which is disjoint from $B_i$ and $E_i$, so it must be that $(x,y)\in A_i\times A_i$ and hence $y\in A_i$.  Similarly, we conclude that $(y,z)\in B_i\times B_i$ so that $y\in B_i$.  But $A_i\cap B_i = \emptyset$, a contradiction.

It remains to show that the uniform topology on $X$ is the original one.  Clearly if $U$ is an entourage then each $U[x]$ is a neighborhood of $x$.  Conversely, if $V$ is a neighborhood of $x$, then by regularity we have a neighborhood $W$ of $x$ and an open $G$ with $W\cap G = \emptyset$ and $G\cup V = X$.  Then $Z = (V\times V) \cup (G\times G)$ is a neighborhood of the diagonal, i.e. an entourage, such that $Z[x] =V$.

Finally, we show this is the unique uniformity compatible with a compact regular topology.  Suppose $X$ is any compact regular uniform space, and $U$ any neighborhood of the diagonal; we want to show $U$ is an entourage.  For any $x\in X$, there is an entourage $V$ such that $V_x[x] \times V_x[x] \subseteq U$.  Let $W_x$ be an entourage such that $W_x \circ W_x \subseteq V_x$.  Since $X$ is compact, it is covered by finitely many of the neighborhoods $W_x[x]$, say $X = W_{x_1}[x_1] \cup \cdots\cup W_{x_k}[x_k]$.  Let $W = W_1 \cap \cdots \cap W_k$; we claim $W\subseteq U$.  For let $(y,z)\in W$; then we have $y\in W_{x_k}[x_k]$ for some $k$, whence also $z\in V_{x_k}[x_k]$, and thus $(y,z) \in V_{x_k}[x_k]\times V_{x_k}[x_k] \subseteq U$.
=--


## Properties

### Regularity

Every uniformly regular uniform space is a [[regular topological space]] in its uniform topology.  For if $U[a]$ is a uniform neighborhood of $a$, let $V$ be an entourage such that $\neg V\cup U = X\times X$, and $W$ an entourage such that $W\circ W \subseteq V$.  Then $W[a]$ is a neighborhood of $a$, and the interior of $W[\neg V[a]]$ is an open set $G$, such that $G\cap W[a] = \emptyset$ and $G\cup U[a] = X$.

It appears to be unknown whether there exist regular uniform spaces that are not uniformly regular.  Regularity implies uniform regularity for at least three large classes of uniform spaces: discrete ones, compact ones, and topological groups (plus, trivially, metric and gauge spaces, which are automatically uniformly regular).


### Apartness

Recall that every uniform space $X$ has a [[inequality relation]] (an [[irreflexive]] [[symmetric relation]]) where "$x # y$" means that there exists an entourage $U$ such that $x \mathbin{&#8777;}_U y$.  If $X$ is uniformly regular, then this is an [[apartness relation]], i.e. it is also a [[comparison]].  For if $x \mathbin{&#8777;}_U z$, let $V \circ V \subseteq U$ and $\neg{W} \cup V = X \times X$.  Then for any $y$, we cannot have both $x \approx_V y$ and $y\approx_V z$, so we must have either $x \mathbin{&#8777;}_W y$ or $y \mathbin{&#8777;}_W z$, whence either $x # y$ or $y # z$.  (In fact, this is a special case of the fact that any [[regular space]] admits an apartness relation, discussed at [[regular space]]).


### Locatedness

Uniform regularity has some nice consequences for the existence of (almost/uniformly) [[located subsets]]: see there for details.


### Uniform apartness spaces

A uniformly regular uniform space can be equivalently described in terms of the *complements* of entourages, i.e. by giving notions of when two points are "at least $\varepsilon$ apart" rather than "at least $\varepsilon$ close".

+-- {: .un_defn}
###### Definition
A **uniform apartness space** is a set $X$ equipped with a collection of binary relations $A\subseteq X\times X$ called *co-entourages* such that

1. $(x,x)\notin A$ for $x\in X$ and co-entourages $A$, i.e. each co-entourage is [[irreflexive relation|irreflexive]].
2. For every co-entourage $A$, there exists a co-entourage $B$ such that whenever $(x,z)\in A$, for any $y$ we have either $(x,y)\in B$ or $(y,z)\in B$.
3. For every co-entourage $A$, there exists a co-entourage $B$ such that $A\subseteq B^{op}$ (hence, by axiom (6), $A^{op}$ is a co-entourage).
4. There exists a co-entourage (hence, by axiom (6), the empty set is a co-entourage).
5. If $A$ and $B$ are co-entourages, so is some superset of $A\cup B$ (hence, by axiom (6), $A\cup B$ is itself).
6. If $A$ is a co-entourage and $B\subseteq A$, then $B$ is a co-entourage.
=--

If $X$ is a uniform space, we can try to make it a uniform apartness space by declaring the co-entourages to be the sets contained in the complement of some entourage, i.e. $A$ is a co-entourage if $A \subseteq \neg U = (X\setminus U)$ for some entourage $U$.  This satisfies axioms (1), (3), (4), (5), and (6) for any uniform space.  (Axiom (5) needs only the direction of de Morgan's law that is true constructively, $\neg U \cup \neg V \subseteq \neg (U\cap V)$.)

For axiom (2), however, we seem to need uniform regularity.  Given $A\subseteq \neg U$, let $V$ be an entourage such that $V\circ V \subseteq U$, and $W$ an entourage such that $V \cup \neg W = X\times X$, and let $B = \neg W$.  Suppose $(x,z)\in A$, hence $(x,z)\notin U$.  Then either $(x,y)\in V$ or $(x,y)\notin W$, and either $(y,z)\in V$ or $(y,z)\notin W$.  If $(x,y)\notin W$ or $(y,z)\notin W$, then $(x,y)\in B$ or $(y,z)\in B$ respectively, so it remains to rule out the case when both $(x,y)\in V$ and $(y,z)\in V$.  But then $(x,z)\in U$, contradicting our assumption.

Thus, any uniformly regular uniform space gives rise to a uniform apartness space.  Moreover, this uniform apartness space is again "uniformly regular" in the sense that for any co-entourage $A$ there is a co-entourage $B$ such that $\neg A\cup B = X\times X$: if $A\subseteq \neg U$, let $B = \neg V$ where $U\cup \neg V = X\times X$.

In the converse direction, *any* uniform apartness space gives rise to a uniform space whose entourages are the supersets of the complements of the co-entourages.  Uniform regularity is not necessary for this direction, since we only need the one of [[de Morgan's laws]] that does hold constructively.  We do of course need a uniform apartness space to be uniformly regular for it to give rise to a uniformly regular uniform space.

To show that these constructions are inverse, it suffices to show that any entourage $U$ in a uniformly regular uniform space contains the double-complement $\neg\neg V$ of some entourage $V$, and dually for any co-entourage $A$ in a uniformly regular uniform apartness space there is a co-entourage $B$ containing $\neg\neg A$.  But for the first it suffices to have $U\cup \neg V = X\times X$, and for the second it suffices to have $\neg A \cup B = X\times X$.  Thus, there is a bijection between uniformly regular uniformities and uniformly regular uniform apartnesses on any set $X$.

We define a function $f:X\to Y$ between uniform apartness spaces to be *uniformly continuous* if for every co-entourage $B$ in $Y$, there is a co-entourage $A$ in $X$ such that if $(f(x),f(y))\in B$ then $(x,y)\in A$.  Since a conditional implies its contrapositive, it follows that this is equivalent to uniform continuity with respect to the corresponding uniform structures.  Thus we have proven:

+-- {: .un_theorem}
###### Theorem
The categories of uniformly regular uniform spaces and uniformly regular uniform apartness spaces are isomorphic over $Set$.
=--


## Related pages

* [[uniform space]]
* [[regular topological space]]


category: topology

[[!redirects uniformly regular space]]
[[!redirects uniformly regular spaces]]
[[!redirects uniformly regular uniform space]]
[[!redirects uniformly regular uniform spaces]]
[[!redirects uniformly regular]]
[[!redirects uniform regularity]]
[[!redirects located uniform space]]
[[!redirects located uniform spaces]]
[[!redirects uniform apartness space]]
[[!redirects uniform apartness spaces]]
[[!redirects uniformly locally decomposable space]]
[[!redirects uniformly locally decomposable spaces]]
