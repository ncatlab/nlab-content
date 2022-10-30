# Syntopogenous spaces
* table of contents
{: toc}

## Idea

A *syntopogenous space* is a common generalization of [[topological spaces]], [[proximity spaces]], and [[uniform spaces]].  The category of syntopogenous spaces includes $Top$, $Prox$, and $Unif$ as full subcategories whose intersection is fairly trivial.

## Definitions

### Topogenous relations

A binary [[relation]] $\delta$ on the [[power set]] $P(X)$ of a [[set]] $X$ is called **topogenous** if it satisfies:

0. *nontriviality*: if $A\cap B$ is [[inhabited set|inhabited]], then $A\;\delta\; B$.

1. *binary additivity*: $A\;\delta\;(B\cup C)$ if and only if either $A\;\delta\;B$ or $A\;\delta\;C$.

2. *nullary additivity*: it is never true that $A\;\delta\; \emptyset$ or $\emptyset\;\delta\;A$ for any $A$.

Note that the "if" direction of binary additivity is equivalent to *isotony*: if $A\subseteq C$ and $B\subseteq D$, then $A\;\delta\;B$ implies $C\;\delta\; D$.

The set of topogenous relations on $X$, ordered by containment, is a [[complete lattice]]:

* Its least element is the *discrete topogenous relation*, defined by $A\;\delta\;B$ if and only if $A\cap B$ is inhabited.
* Its greatest element is the *codiscrete topogenous relation*, defined by $A\;\delta\;B$ if and only if both $A$ and $B$ are inhabited.
* The union of any inhabited set of topogenous relations is topogenous, hence is a [[join]].
* The [[meet]] of a set $\mathcal{D}$ of topogenous relations is not their set-theoretic intersection, but it can be described explicitly: we have $A \;(\bigwedge\mathcal{D})\;B$ if and only if whenever $A = \bigcup_{i=1}^n A_i$ and $B = \bigcup_{j=1}^m B_j$, there exist $i$ and $j$ such that $A_i \;\delta\; B_j$ for all $\delta\in\mathcal{D}$.

The [[opposite relation]] of a topogenous relation is again topogenous.  A topogenous relation is called **symmetric** if it is equal to its opposite, i.e. if $A\;\delta\;B$ if and only if $B\;\delta\; A$.

A topogenous relation is called **perfect** if $A\;\delta\; B$ implies there exists an $x\in A$ with $\{x\}\;\delta\; B$.  It is called **biperfect** if both it and its opposite are perfect.  Of course, a symmetric perfect topogenous relation is automatically biperfect.


### Syntopogenous spaces

A **syntopogeny** (or **syntopogenous structure**) on a set $X$ is a [[filter]] $\mathcal{O}$ of topogenous relations such that

* For any $\delta\in \mathcal{O}$, there exists a $\delta'\in\mathcal{O}$ such that if $A,B\subseteq X$ have the property that whenever $C\cup D = X$, either $A\;\delta'\; C$ or $B\;\delta'\; D$, then $A\;\delta\; B$.

A **basis** for a syntopogeny on $X$ is a [[filterbase]] in the complete lattice of topogenous structures, such that the filter it generates is a syntopogeny.  When $X$ is equipped with a syntopogeny, it is called a **syntopogenous space**.

A syntopogeny is called **symmetric**, **perfect**, or **biperfect** if it admits a basis consisting of symmetric, perfect, or biperfect topogenous relations, respectively.  It is called **simple** if it is a [[principal filter]], i.e. admits a singleton basis.


### Syntopogenous functions

If $(X_1,\mathcal{O}_1)$ and $(X_2,\mathcal{O}_2)$ are syntopogenous spaces, a function $f:X_1\to X_2$ is called **syntopogenous**, or **syntopologically continuous**, if for any $\delta\in\mathcal{O}_2$, its [[inverse image]] $(f\times f)^{-1}(\delta)$ lies in $\mathcal{O}_1$.

This defines the [[category]] $STpg$, which is a [[topological concrete category]] over [[Set]] as follows.  For any function $f:X\to Y$ and any topogenous relation $\delta$ on $Y$, there is a topogenous relation $f^*\delta$ on $X$ defined by
$$ A \;(f^*\delta)\; B \quad\Leftrightarrow\quad f(A) \;\delta\; f(B). $$
If $(Y,\mathcal{O})$ is a syntopogenous space, then the collection $\{ f^*\delta | \delta\in\mathcal{O}\}$ is a basis for a syntopogeny on $X$, which is the [[initial structure]] induced on $X$ by $f$.

...


## Relation to other topological structures

### Topological spaces

If $X$ is a [[topological space]], we define $A\;\delta\; B$ to hold if $A\cap \overline{B}$ is inhabited, where $\overline{B}$ denotes the [[closure]] of $B$.  This is a basis for a simple perfect syntopogeny.

Conversely, given a simple perfect syntopogeny, with singleton basis $\{\delta\}$, we define $\overline{B} = \{ x | \{x\}\;\delta\; B \}$; then this is a Kuratowski closure operator and hence defines a topology.

These constructions define an [[equivalence of categories]] between [[Top]] and the full subcategory of $STpg$ on the simple, perfect, syntopogenous spaces.


### Proximity spaces

A simple symmetric syntopogeny is easily seen to be precisely a [[proximity]].  In this way we have an equivalence of categories between $Prox$ and the full subcategory of $STpg$ on the simple, symmetric, syntopogenous spaces.


### Uniform spaces

If $\delta$ is a biperfect syntopogenous relation, then we have $A\;\delta\;B$ if and only if there exist $x\in A$ and $y\in B$ with $\{x\}\;\delta\;\{y\}$.  Therefore, $\delta$ is completely determined by a binary relation $U\subseteq X\times X$ on $X$, which contains the diagonal $\Delta_X$.  Conversely, any binary relation on $X$ containing the diagonal defines a biperfect syntopogenous relation.

It follows that biperfect syntopogenies are equivalent to [[quasi-uniformities]], which are like [[uniformities]] but lack the symmetry axiom.  We have an equivalence of categories between $QUnif$ and the full subcategory of $STpg$ on the biperfect syntopogenous spaces, which easily restricts to an equivalence between $Unif$ and the category of symmetric, (bi)perfect topogenous spaces.


### Preorders and setoids

A syntopogeny which is both simple and biperfect is determined uniquely by a single relation on $X$ which must be both [[reflexive relation|reflexive]] and [[transitive relation|transitive]], i.e. a [[preorder]].  Thus, the intersection $Top \cap QUnif$ inside $STpg$ is equivalent to $Preord$.

Of course, it follows that a simple, symmetric, (bi)perfect syntopogeny is determined uniquely by a relation on $X$ that is reflexive, transitive, and also symmetric -- i.e. an [[equivalence relation]].  Thus, the intersections $Top \cap Unif$, $Top \cap Prox$, and $Prox\cap (Q)Unif$ inside $STpg$ are all equivalent to the category $Setoid$ of [[setoids]] (sets equipped with an equivalence relation).


## Reflections and coreflections

We first note that for any function $f:X\to Y$, the preimage function mapping syntopogenies on $Y$ to syntopogenies on $X$ preserves joins, meets, simplicity, perfectness, and symmetry.

...


## References

* &#193;kos Cs&#225;sz&#225;r, *Foundations of General Topology*, 1963

Cs&#225;sz&#225;r speaks of *topogenous orders* $\ll$ rather than our topogenous relations; there is a one-to-one correspondence between them, defined by $A\ll B$ if and only if it is not the case that $A \;\delta\; (X\setminus B)$.  One could equivalently axiomatize the negation of $\delta$ itself, and so on.  Of course, in [[constructive mathematics]] these will no longer be equivalent, and one must make a suitable choice.

Note that the containment relation on topogenous orders is reversed from topogenous relations, so that instead of filters we have [[ideals]].  Cs&#225;sz&#225;r also defines a syntopogenous structure to be what we have called a *basis* for one.  As usual, this is convenient for concreteness (especially in the simple case), but has the disadvantage that distinct structures can nevertheless be isomorphic via an identity function, i.e. the forgetful functor to $Set$ is not [[amnestic functor|amnestic]].  On this page, we have followed the traditional practice for other topological structures in choosing to make this functor amnestic.

[[!redirects syntopogenous spaces]]
[[!redirects syntopogenous structure]]
[[!redirects syntopogenous structures]]
[[!redirects syntopogeny]]
[[!redirects syntopogenies]]
[[!redirects topogenous relation]]
[[!redirects topogenous relations]]
[[!redirects topogenous order]]
[[!redirects topogenous orders]]
