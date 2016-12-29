
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Syntopogenous spaces
* table of contents
{: toc}

## Idea

A *syntopogenous space* is a common generalization of [[topological spaces]], [[proximity spaces]], and [[uniform spaces]].  The category of syntopogenous spaces includes $Top$, $Prox$, and $Unif$ as full subcategories whose intersection is fairly trivial.


## Definitions

### Topogenous relations

We work with binary [[relation]]s on the [[power set]] $P(X)$ of a [[set]] $X$.  As for [[proximity spaces]], there are three styles of such relation that are classically inter-definable, but in [[constructive mathematics]] the choice matters.  They are notated by $A \;\delta\; B$, $A\bowtie B$, and $A\ll B$; the relationship between them classically is that $\bowtie$ is the [[negation]] of $\delta$, while $A\ll B$ means $A \bowtie (X\setminus B)$.

A relation $\delta$ on $P(X)$ is called **topogenous** (or a **topogenous nearness**) if it satisfies:

1. *Nontriviality* or *reflexivity*: if $A \cap B$ is [[inhabited set|inhabited]], then $A \;\delta\; B$.

2. *Binary additivity*: $A \;\delta\; (B \cup C)$ if and only if $A \;\delta\; B$ or $A \;\delta\; C$; and $(A \cup B) \;\delta\; C$ if and only if $A \;\delta\; C$ or $B \;\delta\; C$.

3. *Nullary additivity*: it is never true that $A \;\delta\; \emptyset$ or $\emptyset \;\delta\; A$ for any $A$.

Note that the "if" directions of binary additivity are equivalent to *isotony*: if $A \supseteq B \;\delta\; C \subseteq D$ implies $A \;\delta\; D$.  We might specify these separately and call only the reverse direction of binary additivity 'binary additivity'.

A relation satisfying merely (2) and (3) is called a __topogeny__ (between $P(X)$ and itself) at [[toddtrimble:topogeny]]; it is slightly easier to work with the lattice of topogenies than the lattice of topogenous relations, but syntopogenous spaces are built only out of those topogenies that satisfy (1). 

+-- {: .num_remark} 
###### Remark 
As is shown at [[toddtrimble:topogeny]], a topogenous nearness can also be regarded as equivalent to a [[reflexive relation]] from $\beta X$ to $\beta X$ (see [[ultrafilter monad]]) in the [[pretopos]] of [[compact Hausdorff spaces]]. In more concrete terms: each topogeny $\delta$ is a union of "basic topogenies" which are those of the form $\mathcal{U} \times \mathcal{V} \subset P X \times P X$ where $\mathcal{U}, \mathcal{V}$ are ultrafilters, and the set of all pairs $(\mathcal{U}, \mathcal{V})$ whose product is contained in $\delta$ forms a closed subspace of $\beta X \times \beta X$. 
=-- 

The axioms of a topogenous nearness can be reinterpreted in terms of $\bowtie$ to yield a **topogenous apartness**, satisfying

1. *Nontriviality* or *reflexivity*: if $A\bowtie B$, then $A \cap B = \emptyset$.

2. *Binary additivity*: $A \bowtie (B \cup C)$ if and only if $A \bowtie B$ and $A \bowtie C$; and $(A \cup B) \bowtie C$ if and only if $A \bowtie C$ and $B \bowtie C$.

3. *Nullary additivity*: it is always true that $A \bowtie \emptyset$ and $\emptyset \bowtie A$ for any $A$.

Similarly, in terms of $\ll$ we obtain a **topogenous order** or **topogenous neighborhood relation**:

1. *Nontriviality* or *reflexivity*: if $A\ll B$, then $A\subseteq B$.

2. *Binary additivity*: $A \ll (B \cap C)$ if and only if $A \ll B$ and $A \ll C$; and $(A \cup B) \ll C$ if and only if $A \ll C$ and $B \ll C$.

3. *Nullary additivity*: it is always true that $A \ll X$ and $\emptyset \ll A$ for any $A$.

The set of topogenous nearness relations on $X$, ordered by containment, is a [[complete lattice]], as is the set of topogenies.  (If we are working with topogenous apartnesses $\bowtie$ or orders $\ll$ instead of nearnesses $\delta$, then the order relation in these lattices is reversed).

* The [[least element]] is the *discrete topogenous relation*, defined by $A \;\delta\; B$ if and only if $A \cap B$ is [[inhabited subset|inhabited]]. (In the set of topogenies, the least element is the *trivial topogeny*, in which $A \;\delta\; B$ never holds.)
* The [[greatest element]] is the *codiscrete topogenous relation* (also the *cotrivial topogeny*), defined by $A \;\delta\; B$ if and only if both $A$ and $B$ are inhabited.
* The [[union]] of any inhabited set of topogenous relations is topogenous, hence is a [[join]].  To treat inhabited joins and the nullary join (the least element) uniformly, we can take the union of the topogenous relations and the discrete topogenous relation.  (With topogenies, we can just take the union, period.)
* The [[intersection]] of a [[directed set]] of topogenous relations (or topogenies) is again a topogenous relation (or topogeny) and so is a [[meet]].  (This is not provable constructively for topogenous nearnesses $\delta$, but the opposite facts for $\bowtie$ and $\ll$ are: directed unions of topogenous apartnesses and topogenous orders are again such.)
* In general, the intersection of two topogenous relations is not topogenous (or even a topogeny); however, they still have a meet: $A \;\delta\; B$ (where $\delta$ is the meet of $\delta_1$ and $\delta_2$) iff, whenever $A = \bigcup_{i=1}^n A_i$ and $B = \bigcup_{j=1}^m B_j$, there exist $i$ and $j$ such that $A_i \;\delta_1\; B_j$ and $A_i \;\delta_2\; B_j$.

From binary meets (just above), directed meets (above that) and nullary meets (the greatest element), we get all meets (even constructively).  But the [[meet]] of an arbitrary set $\mathcal{D}$ of topogenous relations (or topogenies) can still be easily described explicitly: we have $A \;(\bigwedge\mathcal{D})\;B$ if and only if whenever $A = \bigcup_{i=1}^n A_i$ and $B = \bigcup_{j=1}^m B_j$, there exist $i$ and $j$ such that $A_i \;\delta\; B_j$ for all $\delta\in\mathcal{D}$.

The [[opposite relation]] of a topogenous relation is again topogenous.  A topogenous relation (or topogeny) is called **symmetric** if it is equal to its opposite, i.e. if $A \;\delta\; B$ if and only if $B \;\delta\; A$.  This is easy to reexpress in terms of $\bowtie$.  For $\ll$ the corresponding fact would be $A \ll B$ if, or if and only if, $(X\setminus B)\ll (X\setminus A)$; but constructively the first is too weak and the second too strong.

A topogenous relation is called **perfect** if $A \;\delta\; B$ implies there exists an $x \in A$ with $\{x\} \;\delta\; B$.  It is called **biperfect** if both it and its opposite are perfect.  Of course, a symmetric perfect topogenous relation is automatically biperfect.  Similarly, a topogenous apartness is perfect if $\{x\}\bowtie B$ for all $x\in A$ implies $A\bowtie B$, and a topogenous order is perfect if $\{x\}\ll B$ for all $x\in A$ implies $A\ll B$.  Biperfection for a topogenous order is better expressed without reference to opposites as "if $A\ll B_i$ for all $i$, then $A\ll \bigcap_i B_i$".


### Syntopogenous spaces

A **syntopogeny** (or **syntopogenous structure**) on a set $X$ is a [[filter]] $\mathcal{O}$ of topogenous nearness relations such that

* For any $\delta\in \mathcal{O}$, there exists a $\delta'\in\mathcal{O}$ such that if $A,B\subseteq X$ have the property that for any $D\subseteq X$, either $A\;\delta'\; (X\setminus D)$ or $D\;\delta'\; B$, then $A\;\delta\; B$.

If we are working with apartnesses $\bowtie$ or orders $\ll$, then we instead ask for an [[ideal]] satisfying the analogous properties:

* For any $\bowtie \in \mathcal{O}$, there exists a $\bowtie'\in \mathcal{O}$ such that if $A\bowtie B$, then there exists $D\subseteq X$ such that $A\bowtie' (X\setminus D)$ and $D\bowtie' B$.

* For any $\ll\in\mathcal{O}$, there exists an $\ll'\in \mathcal{O}$ such that if $A\ll B$, then there exists $D\subseteq X$ such that $A\ll' D \ll' B$.

If we have been working with the lattice of topogenies rather than topogenous relations, then we must explicitly state here that every topogeny in $\mathcal{O}$ satisfies (1).  This requirement actually joins with the requirement above to form an [[unbiased definition]] that is nicely expressed in terms of topogenous orders $\ll$ (and tacitly using isotony to show the equivalence):

* For each [[natural number]] $n$ and each $\ll$ in the syntopogeny $\mathcal{O}$, there is an $\ll'$ in $\mathcal{O}$ such that, whenever $A \ll B$, there is a [[list]] $C_0, \ldots, C_n$ such that $A \subseteq C_0 \ll' C_1 \cdots \ll' C_n \subseteq B$.

A **basis** for a syntopogeny on $X$ is a [[filterbase]] in the complete lattice of topogenous relations (or of topogenies), such that the filter it generates is a syntopogeny.  When $X$ is equipped with a syntopogeny, it is called a **syntopogenous space**.  In constructive mathematics, where it matters whether we choose $\delta$, $\bowtie$, or $\ll$, we may speak for emphasis of *syntopogenous nearness spaces*, *syntopogenous apartness spaces*, or *syntopogenous neighborhood spaces*.

A syntopogeny is called **symmetric**, **perfect**, or **biperfect** if it admits a basis consisting of symmetric, perfect, or biperfect topogenous relations, respectively.  It is called **simple** if it admits a basis that is a [[singleton]] (which must then be a [[quasiproximity]], and a [[proximity]] in the symmetric case).


### Syntopogenous functions

If $\delta$ is a topogenous relation on $Y$ and $f:X\to Y$ is a function, then we have a topogenous relation $f^*\delta$ on $X$ defined by $A\;(f^*\delta)\;B$ iff $f(A) \;\delta\; f(B)$.  That is, $f^*\Delta = (\exists_f \times \exists_f)^{-1}(\delta)$, where $\exists_f : P(X) \to P(Y)$ is the [[quantifier|left adjoint]] of $f^{-1}:P(Y) \to P(X)$.

Now if $(X_1,\mathcal{O}_1)$ and $(X_2,\mathcal{O}_2)$ are syntopogenous spaces, a function $f:X_1\to X_2$ is called **syntopogenous**, or **syntopologically continuous**, if for any $\delta\in\mathcal{O}_2$, we have $f^*\delta\in\mathcal{O}_1$.  This defines the [[category]] $STpg$.

If $(Y,\mathcal{O})$ is a syntopogenous space, then the collection $\{ f^*\delta | \delta\in\mathcal{O}\}$ is a basis for a syntopogeny on $X$, which is the [[initial structure]] induced on $X$ by $f$.  The operation of taking initial structures, as a map from syntopogenies on $Y$ to syntopogenies on $X$, preserves opposites, simplicity, meets, symmetry, and perfectness.

More generally, if $(Y_i,\mathcal{O}_i)$ is a family of syntopogenous spaces and $f_i:X\to Y_i$ are functions, then the meet of the initial structures induced by all the $f_i$ is the initial structure induced by them jointly.  Thus, $STpg\to Set$ is a [[topological concrete category]].


## Relation to other topological structures

### Topological spaces

If $X$ is a [[topological space]], we define $A\;\delta\; B$ to hold if $A\cap \overline{B}$ is inhabited, where $\overline{B}$ denotes the [[closure]] of $B$.  This is a basis for a simple perfect syntopogeny.

Conversely, given a simple perfect syntopogeny, with singleton basis $\{\delta\}$, we define $\overline{B} = \{ x | \{x\}\;\delta\; B \}$; then this is a Kuratowski closure operator and hence defines a topology.

These constructions define an [[equivalence of categories]] between [[Top]] and the full subcategory of $STpg$ on the simple, perfect, syntopogenous spaces.

In constructive mathematics, the three kinds of (simple, perfect) syntopogenous spaces can be identified with three no-longer-equivalent notions of "topological space": the nearness ones correspond, as described above, with [[closure spaces]], the apartness ones with [[point-set apartness spaces]], and the neighborhood onse with ordinary [[topological spaces]].


### Proximity spaces

A simple symmetric syntopogeny is easily seen to be precisely a [[proximity]] (of the appropriate sort: nearness, apartness, or neighborhood).  In this way we have an equivalence of categories between $Prox$ and the full subcategory of $STpg$ on the simple, symmetric, syntopogenous spaces.

More generally, an arbitrary simple syntopogeny can be identified with a [[quasiproximity]], and we have an equivalence of categories between $QPrxo$ and the subcategory of simple syntopogenous spaces.


### Uniform spaces

If $\delta$ is a biperfect topogenous relation, then we have $A\;\delta\;B$ if and only if there exist $x\in A$ and $y\in B$ with $\{x\}\;\delta\;\{y\}$.  Therefore, $\delta$ is completely determined by a binary relation $U\subseteq X\times X$ on $X$, which contains the diagonal $\Delta_X$.  Conversely, any binary relation on $X$ containing the diagonal defines a biperfect topogenous relation.  (For a biperfect topogeny, remove the requirement that $U$ contain the diagonal.)

It follows that biperfect syntopogenies are equivalent to [[quasi-uniformities]], which are like [[uniformities]] but lack the symmetry axiom.  We have an equivalence of categories between $QUnif$ and the full subcategory of $STpg$ on the biperfect syntopogenous spaces, which easily restricts to an equivalence between $Unif$ and the category of symmetric, (bi)perfect topogenous spaces.

Constructively, this equivalence still holds for both nearness *and* neighborhood syntopogenous spaces.  In general, topogenous nearnesses and topogenous neighborhood relations are not equivalent, but a *biperfect* topogenous neighborhood relation is determined by giving for each $x$ the smallest set $B$ such that $\{x\}\ll B$, and as $x$ varies these sets again determine exactly a binary relation on $X$ (containing the diagonal).  Syntopogenous apartness spaces, on the other hand, correspond to [[uniform apartness spaces]].


### Preorders and setoids

A syntopogeny which is both simple and biperfect is determined uniquely by a single relation on $X$ which must be both [[reflexive relation|reflexive]] and [[transitive relation|transitive]], i.e. a [[preorder]].  Thus, the intersection $Top \cap QUnif$ inside $STpg$ is equivalent to $Preord$.

Of course, it follows that a simple, symmetric, (bi)perfect syntopogeny is determined uniquely by a relation on $X$ that is reflexive, transitive, and also symmetric -- i.e. an [[equivalence relation]].  Thus, the intersections $Top \cap Unif$, $Top \cap Prox$, and $Prox\cap (Q)Unif$ inside $STpg$ are all equivalent to the category $Setoid$ of [[setoids]] (sets equipped with an equivalence relation).


## Some coreflections

In the preorder of topogenous relations on any set $X$, the following sub-preorders are coreflective:

* The symmetric elements.  The symmetric coreflection of $\delta$ is the meet $\delta^s \coloneqq \delta \wedge \delta^{op}$.
* The perfect elements.  The perfect coreflection of $\delta$ is defined by $A\;\delta^p\;B$ iff there exists $x\in A$ with $\{x\}\;\delta\;B$.
* The biperfect elements.  The byperfect coreflection of $\delta$ is defined by $A\;\delta^b\;B$ iff there exist $x\in A$ and $y\in B$ with $\{x\}\;\delta\;\{y\}$.

It follows that in the preorder of syntopogenous structures on $X$, the symmetric, perfect, and biperfect elements are also reflective; the coreflections are obtained by applying the above one to each topogenous relation in turn.  Moreover, the simple syntopogenous structures on $X$ are also coreflective; the coreflection just takes the intersection of all relations belonging to the filter (this is a directed intersection, hence automatically again a topogenous relation --- although constructively this only works in the dual cases of $\bowtie$ and $\ll$).

Finally, for any function $f:X\to Y$, the preimage function $f^*$, mapping syntopogenous structures on $Y$ to those on $X$, preserves all of these coreflections.  Therefore, the full subcategories of

* simple,
* symmetric,
* perfect, and
* biperfect

syntopogenous spaces are all coreflective in $STpg$, with coreflections written $(-)^t$, $(-)^s$, $(-)^p$, and $(-)^b$ respectively.

In general, of course, coreflections into distinct subcategories do not commute or even preserve each other's subcategories.  However, by construction, we see that the coreflections $(-)^s$, $(-)^p$, and $(-)^b$ all preserve simplicity.  Therefore, the full subcategories of

* simple symmetric (i.e. proximity),
* simple perfect (i.e. topological), and
* simple biperfect (i.e. preorders)

syntopogenous spaces are all coreflective in $STpg$, with coreflections $(-)^{t s}$, $(-)^{t p}$, and $(-)^{t b}$ respectively.  Finally, it is evident by construction that $(-)^b$ preserves symmetry, so the full subcategories of

* symmetric biperfect, and
* simple symmetric biperfect (i.e. setoids)

syntopogenous spaces are also both coreflective in $STpg$, with coreflections $(-)^{s b}$ and $(-)^{t s b}$ respectively.

It is straightforward to verify the following.

1. When applied to a (quasi)-proximity space or a (quasi)-uniform space, the coreflection $(-)^{t p}$ into topological spaces computes the underlying topology of these structures, as usually defined.

2. When applied to a uniform space, the coreflection $(-)^{t s}$ computes its underlying proximity, as usually defined.  The same is true in the non-symmetric case for quasi-uniformities and quasi-proximities.

3. When applied to any syntopogenous space, the coreflection $(-)^{t b}$ computes the [[specialization order]] of its underlying topology (i.e. its image under $(-)^{t p}$).  In particular, this is the case for topological spaces, proximity spaces, and uniform spaces.


## Related concepts

* [[funcoid]]

[[!include generalized uniform structures - table]]


## References

* &#193;kos Cs&#225;sz&#225;r, *Foundations of General Topology*, 1963

Cs&#225;sz&#225;r uses topogenous orders $\ll$.  Cs&#225;sz&#225;r also defines a syntopogenous structure to be what we have called a *basis* for one.  As usual, this is convenient for concreteness (especially in the simple case), but has the disadvantage that distinct structures can nevertheless be isomorphic via an identity function, i.e. the forgetful functor to $Set$ is not [[amnestic functor|amnestic]].  On this page, we have followed the traditional practice for other topological structures in choosing to make this functor amnestic.


[[!redirects syntopogenous space]]
[[!redirects syntopogenous spaces]]
[[!redirects syntopogenous structure]]
[[!redirects syntopogenous structures]]
[[!redirects syntopogeny]]
[[!redirects syntopogenies]]

[[!redirects symmetric syntopogenous space]]
[[!redirects symmetric syntopogenous spaces]]
[[!redirects symmetric syntopogenous structure]]
[[!redirects symmetric syntopogenous structures]]
[[!redirects symmetric syntopogeny]]
[[!redirects symmetric syntopogenies]]

[[!redirects topogenous relation]]
[[!redirects topogenous relations]]
[[!redirects topogenous nearness relation]]
[[!redirects topogenous nearness relations]]
[[!redirects topogenous nearness]]
[[!redirects topogenous nearnesses]]
[[!redirects topogenous apartness relation]]
[[!redirects topogenous apartness relations]]
[[!redirects topogenous apartness]]
[[!redirects topogenous apartnesses]]
[[!redirects topogenous order relation]]
[[!redirects topogenous order relations]]
[[!redirects topogenous order]]
[[!redirects topogenous orders]]

[[!redirects syntopogenous nearness space]]
[[!redirects syntopogenous nearness spaces]]
[[!redirects syntopogenous apartness space]]
[[!redirects syntopogenous apartness spaces]]
[[!redirects syntopogenous neighborhood space]]
[[!redirects syntopogenous neighborhood spaces]]
