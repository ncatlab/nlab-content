* toc
{:toc}

# Idea

Informally, a **pure set** is a [[set]] of pure sets.

On the face of it, this is a circular definition, but like many such definitions, it can be made precise in at least two ways: [[recursion|recursively]] and [[corecursion|corecursively]].

* The 'recursive' meaning is that all pure sets must be *constructed*, starting from nothing, as sets of other previously constructed pure sets.  This results in the **[[well-founded relation|well-founded]] pure sets**.  Thus, at first, the only well-founded set possible is the [[empty set]] $\empty = \{ \}$, the set of no pure sets.  Once you have that, you can form $\star = \{\empty\}$, then $\{\star\}$ and $\{\empty,\star\}$, and so on.  In this way we can obtain at least all [[hereditarily finite sets]]; if we use an axiom of infinity as well, we can jump to the [[countably infinite set]] of all hereditarily finite sets and continue from there.

* The 'corecursive' meaning is that any pure set can be *deconstructed* into a set of other pure sets, and every possible such deconstruction defines a unique pure set.  In this way we obtain not just well-founded pure sets but also **ill-founded pure sets**.  (The inclusion of well-founded sets here is an example of the [[red herring principle]].)  Possible examples of non-well-founded sets include a set $\bullet$ such that $\bullet = \{\bullet\}$ (a suggestive model for the [[point]]), or sets $A$ and $B$ such that $A = \{B\}$ and $B = \{\empty, A\}$.

In addition, the meaning of this definition changes according to whether our [[set theory|set-theoretic]] [[foundations|foundation]] is [[material set theory|material]] or [[structural set theory|structural]].

* If the foundation is 'material' or 'membership-based,' such as [[ZFC]], then the elements of a set can, in fact, *be* other sets.  Therefore, in this case we are defining (either recursively or corecursively) an *adjective* "pure" that can be applied to the noun "set:" a set is pure if at no point in its construction or deconstruction into elements do we encounter anything that is not a pure set.

  In the most common material set theories, such as [[ZFC]], *all* sets are pure, since the only 'things' the theory deals with (hence the only things that can be elements of sets) are sets.  However, there are easy modifications of these theories that allow 'atoms' or [[urelement]]s that are not sets, and in this case the pure sets will be those that 'hereditarily' contain no atoms.  Many common material set theories (starting with von Neumann 1925, Zermelo 1930) also include an [[axiom of foundation]] asserting that all (pure) sets are well-founded; the dual [[axiom of anti-foundation]] (due to Aczel) allows and 'tames' the ill-founded sets.

* If the foundation is 'structural' or 'categorial', such as [[ETCS]] or [[SEAR]], then the elements of a set cannot *be* other sets.  Thus, in this case we are defining a single noun "pure set," with no *a priori* relation to the structural notion of "set" that occurs in the foundational theory.  A *pure set*, according to this definition, is a set *equipped with structure* assigning to each of its elements another pure set (interpreted either recursively or corecursively).

  From this point of view, the definition of pure set provides a construction of a model of material set theory within a model of structural set theory: a global relation of $\in$ can be defined between pure sets which will satisfy the axioms of some material set theory.  (Of course, the sets in a model of material set theory always model a structural set theory, so this is the 'difficult' direction of the equivalence between the two types of set theory.)  Whether we use the recursive or corecursive definition determines whether the resulting material set theory will satisfy the axiom of foundation or the axiom of anti-foundation.  Note that using these two choices, the composite operation "material $\to$ structural $\to$ material" reduces to the standard proofs of the relative consistency of the axioms of foundation and anti-foundation, since the passage from material to structural requires neither one.


# Formalisation in material set theory

In material set theory without urelements, every set is a pure set.  If there are urelements, so that not all sets are pure, then it is easy to define the class of pure sets as follows:

+-- {: .un_defn}
###### Definition
A set $x$ is **pure** if given any sequence $x_n \in x_{n-1} \in \dots \in x_1 \in x_0 = x$, all of the $x_i$ are sets.
=--

Whether this produces the well-founded pure sets or the ill-founded ones depends on whether the axiom of foundation is satisfied in the ambient set theory.


# Formalization in structural set theory

In a structural set theory like [[ETCS]] or [[SEAR]], we can model a pure set by a graph describing its hereditary membership relation.

One way to state the basic theoretical idea is that the class of well-founded sets is the [[initial algebra]] of the covariant [[power set]] functor, while the class of ill-founded sets is the [[terminal coalgebra]] of the same functor.  Of course, neither of these algebras exists as a set, since this would violate [[Cantor's theorem]], but we can still describe what their elements would be like.  We can also define these algebras as [[discrete category|discrete]] [[large category|large categories]], or as proper classes in a structural set-class theory such as [[algebraic set theory]].

The discussion which follows is phrased informally, like most mathematics.  However, it is purely structural and can be interpreted in any structural set theory.  For instance, the definition below of a "graph" as a set with a binary relation should be formalized as a set $G$ together with an injection $R \hookrightarrow N\times N$.

## Membership graphs ##

To describe a pure set, we must give all the elements of that set, each of which is a pure set and thus must have its own elements, which are also pure sets, and so on.  A convenient way to "picture" a pure set is with a *graph*.

+-- {: .un_defn}
###### Definition
For the purposes of this page, a **graph** will mean a set $G$ of __nodes__ equipped with a binary [[relation]] $\to$ on the nodes.  A node $i$ is called a __child__ of a node $j$ if $i \to j$.
=--

The idea of a graph-picture of pure sets is that the *nodes* represent *pure sets*, and we have $i\to j$ precisely when $i\in j$.  Clearly the membership relations between any collection of pure sets should be representable by a graph.  To what extent the converse holds, i.e. which graphs can be interpreted as membership-relations between pure sets, depends on whether the pure sets in question are well-founded or ill-founded.  For purposes of drawing well-founded pure sets, only well-founded graphs should be used, whereas arbitrary graphs can be used to draw ill-founded sets.  (In fact, one form of the [[axiom of anti-foundation]] is that any graph is the picture of some pure sets.)

+-- {: .un_defn}
###### Definition
A set $S$ of nodes in a graph is **$\to$-inductive** if whenever all children of some node $i$ are in $S$, then $i$ itself is in $S$.  A graph is **[[well-founded relation|well-founded]]** if the only $\to$-inductive set of nodes is the set of all nodes.
=--

Assuming the principle of [[excluded middle]], well-foundedness is equivalent to saying that the tree has no infinite paths.

If we want to use a graph to describe a *specific* pure set, then we should single out one particular node as representing *that* set.  Moreover, it makes sense to demand that the graph contain no "superfluous" data other than what is necessary to describe the hereditary membership structure of the particular set in question.

+-- {: .un_defn}
###### Definition
A graph is **pointed** if it is equipped with a specified node $\top$ called the **root**.  A pointed graph is **accessible** if for every node $x$, there exists a path $x = x_0 \to x_1 \to \dots \to x_n =\top$ to the root; this is equivalent to saying that $\top$ is a [[top element]] for the reflexive-[[transitive closure]] of $\to$.  An accessible pointed graph is abbreviated **APG**.
=--

An APG gives all the data necessary to characterize a pure set $X$, and the pure set in question is well-founded iff the APG is well-founded.  We can think of the root as representing $X$ itself, the root\'s children as the elements of $X$, the next level as those elements\' elements, and so on.

If we want to think of these elements as pure sets themselves, then we can "externalize" them into separate APGs.  Specifically, for any node $z$ in a graph $G$, the subgraph consisting of all those nodes which admit some path to $z$ is an APG, which describes the pure set represented by $z$; we write it as $G/z$ and call it the **full subgraph** of $G$ rooted at $z$.  If $G$ is an APG and $z$ is a child of the root, we say that $G/z$ is an **immediate subgraph** of $G$.  The immediate subgraphs of $G$ represent the pure sets that are the "elements" of the pure set represented by $G$.  Thus, the APG $G$ pictures the hierarchy of elements of $X$, where each immediate subgraph $G/z$ corresponds to its root $z$, and $\to$ is interpreted as membership.


## Examples of APGs ##

Note that the nodes in most of the pictures below have labels, but these are for illustration only; they are *not* part of the structure defining the tree.

First, $\empty = \{ \}$ consists of nothing but a root:
$$ \empty $$

The set $\star = \{\empty\}$ has the empty set attached to the root (which we draw at the top):
$$ \array { \star \\ \uparrow \\ \empty } $$
Notice that $\empty$ is an immediate subgraph, so we can write $\empty \in \star$.

Then the two most obvious ways of representing the ordinal $2$ as a pure set, namely $2_Z = \{\star\}$ and $2_N = \{\empty, \star\}$, can be drawn as follows:
$$ \array { 2_Z \\ \uparrow \\ \star \\ \uparrow \\ \empty } \quad \quad \quad \quad \array { 
       &          & 2_N \\
       & \nearrow &     & \nwarrow \\
\empty &          &     &          & \star    \\
       &          &     &          & \uparrow \\
       &          &     &          & \empty
} $$
Looking at immediate subtrees, $\star \in 2_Z$, $\empty \in 2_N$, and $\star \in 2_N$, but $\empty \notin 2_Z$.

$2_N$ can also be represented as $\{\star, \empty\}$:
$$ \array {
         &          & 2_N \\
         & \nearrow &     & \nwarrow \\
\star    &          &     &          & \empty \\
\uparrow \\
\empty
} $$
Of course, as a graph this is isomorphic to $\{\empty, \star\}$, and hence should represent the same pure set.

These sets are all well-founded.  A non-well-founded set can be represented by an infinite picture; here is $\bullet = \{\bullet\}$:
$$ \array { \bullet \\ \uparrow \\ \bullet \\ \uparrow \\ \bullet \\ \uparrow \\ \vdots } $$
Looking at the unique immediate subgraph, we verify that $\bullet \in \bullet$.  Note that $\bullet$ can also be represented by the finite graph with one node that is a child of itself.

Of course, a well-founded [[infinite set]] also has an infinite picture, but there are no infinite paths.  Here is $\omega_N$, the set of von Neumann [[natural numbers]]:
$$ \array {
        &          &          & \omega_N \\
        & \nearrow & \nearrow &          & \nwarrow & \cdots \\
\empty  & \star    &          &          &          & 2_N      & \cdots \\
        & \uparrow &          &          & \nearrow & \uparrow & \cdots \\
        & \empty   &          & \empty   &          & \star    & \cdots \\
        &          &          &          &          & \uparrow & \cdots \\
        &          &          &          &          & \empty   & \cdots \\
        &          &          &          &          &          & \vdots
} $$
So we have $\empty \in \omega_N$, $\star \in \omega_N$, $2_N \in \omega$, etc.

By definition, a tree models a _[[hereditarily finite set]]_ if every node has finitely many children; a tree models a well-founded hereditarily finite set if and only if it is finite and $\prec$ is [[decidable subset|decidable]].  The relationship between these two facts and the no-infinite-path formulation of well-foundedness is a form of [[Konig's lemma|Kőnig's Lemma]].


## Ambiguities ##

APGs are sufficient to describe all pure sets, but multiple APGs, even non-isomorphic ones, can represent the "same" pure set.  Firstly, we have so far not eliminated the possibility of duplicate branches.  For instance, the pure set $2_Z$ can also be represented as $\{\star, \star\}$:
$$ \array { 
         &          & 2_Z \\
         & \nearrow &     & \nwarrow \\
\star    &          &     &          & \star    \\
\uparrow &          &     &          & \uparrow \\
\empty   &          &     &          & \empty
} $$
It is easy to eliminate APGs with such "obviously redundant" branches.

+-- {: .un_defn}
###### Definition
An APG $G$ is **rigid** if whenever $x$ and $y$ are two children of the same node $z$ such that $G/x \cong G/y$, then in fact $x=y$.
=--

Assuming [[excluded middle]], rigidity is equivalent to saying that any graph [[automorphism]] is the identity function.  Note also that if two rigid APGs are isomorphic, they must be uniquely isomorphic.  Thus, for rigid APGs, being isomorphic is a *property*, rather than *structure*.

Even among rigid APGs, however, there are are ambiguities.  For example, the pure set $2_N$ can also be drawn by the APG
$$ \array {
2_N \\
\uparrow & \nwarrow \\
|        &          & \star    \\
|        & \nearrow &  \\
\empty   &          & 
} $$
The issue here is that the "same" pure set can occur in more than one place in the membership hierarchy of a pure set, and we have to choose whether or not to identify them in the graph.  There are three solutions to this problem:

1. Demand that duplicate occurrences of a pure set always be represented separately.
1. Demand that duplicate occurrences always be identified, wherever they occur.
1. Define a notion of "equivalence" between APGs which is looser than isomorphism.

These are of course related; the first two can be seen as specifying a particular isomorphism class within each of the equivalence classes defined by the third.  In particular, they all result in equivalent notions of pure set, when they all apply.  (However, in [[predicative mathematics|predicative]] set theories, it seems that only the first method is applicable.)  We will consider them all in turn.


## Membership trees ##

A natural way to ensure that the same node is never "shared" between two occurrences is to require that our APGs be *trees*.

+-- {: .un_defn}
###### Definition
An pointed graph is a **tree** if every node admits a *unique* path to the root.  Equivalently, $G$ is a tree if its root $\top$ is a [[terminal object]] of the [[quiver]] generated by the relation $\to$.
=--

A tree may or may not be well-founded.  Note, though, that in a tree, the [[opposite relation]] $\leftarrow$ is automatically well-founded: each node has a unique [[natural number]] *height*, namely the length of its unique path to the root, so well-foundedness of $\mathbb{N}$ implies well-foundedness of $\leftarrow$.

It now makes sense to define a *pure set* to be a **rigid accessible pointed tree**.  The idea is that two such trees represent the same pure set iff they are isomorphic.   We define "membership" $G\in H$ between such trees to mean that $G$ is isomorphic to some immediate subtree of $H$ (that is, a tree $H/z$ where $z$ is a child of the root of $H$).

One can then prove the various axioms of material set theory from these definitions.  Specifically, if __[[ETCS]]__ holds for the structural sets (of nodes, etc) used in this definition, then $\mathbf{BZC}^-$ (which is __[[ZFC]]__ with only bounded separation and no axioms of [[axiom of replacement|replacement]] or [[axiom of foundation|foundation]]) holds for rigid trees, while $\mathbf{BZC}$ ($\mathbf{BZC}^-$ together with foundation) holds for well-founded rigid trees.  Similar results hold for [[constructive mathematics|constructive]] weakenings of ETCS and $\mathbf{BZC}^-$, since these definitions involve only function-sets and not power-sets.  Likewise, we can strengthen both sides with axioms of replacement, collection, or separation, or by adding [[Grothendieck universes]].

The argument for the [[axiom of extensionality]] is perhaps the most interesting; it goes as follows.  If each immediate subtree $G/x$ of $G$ is isomorphic to an immediate subtree $H/y$ of $H$ and conversely, then $y$ and $x$ are mutually uniquely determined by rigidity, so we have a bijection between the children of the roots of $G$ and of $H$.  Since the isomorphisms $G/x \cong H/y$ are also unique, again by rigidity, and each $G/x$ is disjoint from $G/x'$ for $x\neq x'$, by the tree property, we can piece together these isomorphisms to define an isomorphism $G\cong H$.  (In particular, the uniqueness of all these isomorphisms means that the [[axiom of choice]] is not needed.)

(Note, though, that this is only the "weak" version of extensionality.  This is sufficient for well-founded sets, but we may need to strengthen rigidity somehow to obtain stronger notions of [[extensional relation|extensionality]], which are generally more appropriate for ill-founded sets.)


## Bisimulations ##

We now consider the *third* solution to the ambiguity problem: defining a looser notion of equivalence between APGs.

+-- {: .un_defn}
###### Definition
If $G$ and $H$ are graphs, a **bisimulation** from $G$ to $H$ is a binary relation $\sim$ from $G$ to $H$ such that for any $x\in G$ and $y\in H$ with $x\sim y$, then:

* For any $a\to x$, there is some $b\in H$ with $b\to y$ and $a\sim b$, and
* For any $b\to y$, there is some $a\in G$ with $a\to x$ and $a\sim b$.

Two APGs $G$ and $H$ are **equivalent** if there is a bisimulation $\sim$ from $G$ to $H$ such that $\top\sim\top$.
=--

The idea is that a bisimulation identifies pairs of nodes which "represent the same pure set."  This interpretation is consistent, since if $\sim$ is a bisimulation from $G$ to $H$ such that $x\sim y$, then the APGs $G/x$ and $H/y$ are equivalent.

We can now define a *pure set* to be an APG, with *equality* represented by *equivalence* in the above sense.  Unsurprisingly, we define "membership" $G\in H$ to mean that $G$ is equivalent to some immediate subgraph of $H$.  One can again prove the various axioms of material set theory with these definitions.  In this case, we obtain the *strong* notion of [[extensional relation|extensionality]] (which is equivalent to the weak one for well-founded sets).

This definition is not predicative, since the notions of equivalence and membership involve quantification over bisimulations, which are relations, i.e. subsets---thus it requires either powersets or an [[axiom of separation]].

+--{: .query}
[[Mike Shulman]]: Here is where I left off reorganizing.
=--

## Reflexive-transitive closures as graphs ##

The picture above may be seen as an _unwrapped_ representation; there is also a _wrapped_ picture.

In this representation, a pure set is an _extensional accessible graph_, again possibly a _well-founded_ one.  Again, we will define this in several stages:
*  A __[[graph|directed graph]]__ again consists of a set $N$ of __nodes__ and a binary [[relation]] $\to$ on the nodes; again, $i$ is a __child__ of $j$ is $i \to j$.
*  Now instead of forming the quiver of paths, we simply form the [[transitive closure]] $\to^*$ of $\to$.  That is, we only care whether there exists a path, not which paths there are.
*  A graph is __accessible__ (technically, _directed accessible pointed_) if it is equipped with a __root__ node $r$ that is a [[top]] of $\to^*$ (meaning that every node has a path to the root).
*  A graph is __extensional__ if $\to$ is an [[extensional relation]]; this is probably the most complicated part.
*  A graph is __well-founded__ if $\to$ is a [[well-founded relation]] (note that the [[opposite relation]] $\leftarrow$ is automatically well-founded for an accessible graph).

These subsidiary notions are also needed:
*  Two graphs are __equivalent__ if there exists a graph isomorphism between them; for extensional graphs, such an isomorphism must be unique.
*  An accessible graph $X$ is an __immediate subgraph__ of an accessible graph $Y$ if $X$ is isomorphic to the $\to^*$-downset of one of the children of the root in $Y$; for extensional graphs, this can again happen only in one way.

In this picture, the nodes are precisely the elements of the reflexive-[[transitive closure]] of the pure set, and the relation $\to$ on them is precisely the membership relation $\in$.


### Examples ###

Again, the root represents the pure set itself, the root\'s children are its elements, and so on.  Now, however, there is no more branching than necessary and no repetition whatsoever among the identities of the nodes.

Again $\empty = \{ \}$ consists of nothing but the root:
$$ \empty $$

The set $\star = \{\empty\}$ still the empty set attached to the root:
$$ \array { \star \\ \uparrow \\ \empty } $$
Again $\empty$ is an immediate subgraph, so we can write $\empty \in \star$.

Even $2_Z = \{\star\}$ looks the same as before, but now $2_N = \{\empty, \star\}$ looks different:
$$ \array { 2_Z \\ \uparrow \\ \star \\ \uparrow \\ \empty } \quad \quad \quad \quad \array { 
2_N         \\
\uparrow    & \nwarrow \\
|           &          & \star    \\
|           & \nearrow \\
\empty
} $$
Looking at immediate subgraphs, again $\star \in 2_Z$, $\empty \in 2_N$, and $\star \in 2_N$.

The non-well-founded set $\bullet = \{\bullet\}$ consists of a loop:
$$ \array {
           & \bullet \\
/          &         & \nwarrow \\
\backslash &         & /        \\
} $$
As the root is a child of itself, the entire subgraph is an immediate subgraph of itself, so $\bullet \in \bullet$.

Finally, here is the set $\omega_N$ of von Neumann [[natural numbers]]:
$$ \array {
         &            & \omega_N \\
         & \nearrow   & \uparrow & \nwarrow & \cdots \\
|        &            & |        &          & 2_N      & \cdots \\
|        &            & |        & \nearrow & \uparrow & \cdots \\
|        &            & \star    &          & |        & \cdots \\
         & \backslash & \uparrow & /        & \cdots   \\
         &            & \empty
} $$
Again we have $\empty \in \omega_N$, $\star \in \omega_N$, $2_N \in \omega$, etc.

Now an extensional accessible graph models a [[hereditarily finite set]] iff the graph itself is finite and $\prec$ is decidable.


## Relation between these ##

Peter Aczel\'s general model of a pure set is any _simple directed accessible pointed pseudograph_.  That is, the graph need not be a tree (much less a rigid one), nor need it be extensional.  One can make such a graph extensional by identifying nodes to make the extensional quotient as explained at [[extensional relation]].  Then one can unwrap this extensional graph into a rigid tree by including one copy of each node for each of its paths to the root.  So there are two extreme ways to represent a pure set by an isomorphism class of graphs, but any accessible graph will represent a pure set one way or another.


# References #

*  Peter Aczel (1988).  Non-well-founded sets.  CSLI 14; Stanford University.  [PDF](http://standish.stanford.edu/pdf/00000056.pdf).


[[!redirects pure sets]]
