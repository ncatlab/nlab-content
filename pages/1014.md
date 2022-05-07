
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Pure sets
* table of contents
{: toc}

## Motivation

In [[material set theory]], there is an intuitive conception of what a [[set]] is, which may be stated informally as follows: a set is a collection of sets.  Actually, it is possible to have [[urelements]] in a material set theory (such as [[ZFA]]), although the most common axiom systems do not allow this; in any case we can say that a *pure* set is a collection of pure sets.

The primary motivation for [[structural set theory]] is that this conception of a set is not needed in ordinary [[mathematics]]; it is sufficient to characterise the [[category of sets]] (although a structural set theory can also be described in ways other than category-theoretic).  However, material set theory is itself part of mathematics, and we may want to describe the material notion of a pure set in structural terms.

There is also a very practical point to this exercise: the translation between material and structural set theories.  Any model of a material set theory is already a model of a corresponding structural set theory, but we go through the yoga below to construct a model of a material set theory out of a model of a structural set theory.  In particular, we must do this to prove that two set theories (one material and one structural) are equiconsistent.

See also at _[[material-structural adjunction]]_.


## Idea

Taking a base notion of [[set]] as granted, we wish to define a __pure set__ to be a set of pure sets.  On the face of it, this is a circular definition, but like many such definitions, it can be made precise in (at least) two ways: [[recursion|recursively]] and [[corecursion|corecursively]].

* The 'recursive' meaning is that all pure sets must be *constructed*, starting from nothing, as sets of other previously constructed pure sets.  This results in the **[[well-founded relation|well-founded]] pure sets**.  Thus, at first, the only well-founded set possible is the [[empty set]] $\empty = \{ \}$, the set of no pure sets.  Once you have that, you can form $\star = \{\empty\}$, then $\{\star\}$ and $\{\empty,\star\}$, and so on.  In this way we can obtain at least all [[hereditarily finite sets]]; if we use an [[axiom of infinity]] as well, we can jump to the [[countably infinite set]] of all hereditarily finite sets and continue from there.

* The 'corecursive' meaning is that any pure set can be *deconstructed* into a set of other pure sets, and every possible such deconstruction defines a unique pure set.  In this way we obtain not just well-founded pure sets but also **ill-founded pure sets**.  (The inclusion of well-founded sets among the ill-founded sets is an example of the [[red herring principle]].)  Possible examples of non-well-founded sets include a set $\bullet$ such that $\bullet = \{\bullet\}$ (a suggestive model for the [[point]]), or sets $A$ and $B$ such that $A = \{B\}$ and $B = \{\empty, A\}$.

In addition, the meaning of this definition changes according to whether our [[set theory|set-theoretic]] [[foundations|foundation]] is [[material set theory|material]] or [[structural set theory|structural]].

* If the foundation is 'material' or 'membership-based,' such as [[ZFC]], then the elements of a set can, in fact, *be* other sets.  Therefore, in this case we are defining (either recursively or corecursively) an *adjective* "pure" that can be applied to the noun "set": a set is pure if at no point in its construction or deconstruction into elements do we encounter anything that is not a pure set.

  In the most common material set theories, such as [[ZFC]], *all* sets are pure, since the only 'things' the theory deals with (hence the only things that can be elements of sets) are sets.  However, there are easy modifications of these theories that allow 'atoms' or [[urelement]]s that are not sets, and in this case the pure sets will be those that 'hereditarily' contain no atoms.  Many common material set theories (starting with von Neumann 1925, Zermelo 1930) also include an [[axiom of foundation]] asserting that all (pure) sets are well-founded; the dual [[axiom of anti-foundation]] (due to Aczel) allows and 'tames' the ill-founded sets.

* If the foundation is 'structural' or 'categorial', such as [[ETCS]] or [[SEAR]], then the elements of a set cannot *be* other sets.  Thus, in this case we are defining a single noun "pure set," with no *a priori* relation to the structural notion of "set" that occurs in the foundational theory.  A *pure set*, according to this definition, is a set *equipped with structure* assigning to each of its elements another pure set (interpreted either recursively or corecursively).

  From this point of view, the definition of pure set provides a construction of a model of material set theory within a model of structural set theory: a global relation of $\in$ can be defined between pure sets which will satisfy the axioms of some material set theory.  (Of course, the sets in a model of material set theory always model a structural set theory, so this is the 'difficult' direction of the equivalence between the two types of set theory.)  Whether we use the recursive or corecursive definition determines whether the resulting material set theory will satisfy the axiom of foundation or the axiom of anti-foundation.  Note that using these two choices, the composite operation "material $\to$ structural $\to$ material" reduces to the standard proofs of the relative consistency of the axioms of foundation and anti-foundation, since the passage from material to structural requires neither one.


## Formalisation in material set theory

In material set theory without urelements, every set is a pure set.  If there are urelements, so that not all sets are pure, then it is easy to define the class of pure sets as follows:

+-- {: .un_defn}
###### Definition
A set $x$ is **pure** if given any finite sequence $x_n \in x_{n-1} \in \dots \in x_2 \in x_1 \in x_0 = x$, all of the $x_i$ are sets.
=--

Whether this produces the well-founded pure sets or the ill-founded ones depends on whether the sets in the ambient set theory are well-founded or ill-founded.

If you are (unusually) working in an ill-founded material set theory and want only the well-founded pure sets, then you simply need to define the other adjective:

+-- {: .un_defn}
###### Definition
A class $C$ of sets is __$\in$-inductive__ if whenever all elements of some set $x$ are in $C$, then $x$ itself is in $C$.  A set $x$ is __well-founded__ if it belongs to every $\in$-inductive class $C$.
=--

(That *all* sets are well-founded is the [[axiom of foundation]].)  If $x$ is well-founded, then there can be no infinite sequence $\in \dots \in x_2 \in x_1 \in x_0 = x$, since the sets with no such sequence form an $\in$-inductive class; the converse (that a set is well-founded if it has no such infinite sequence) holds using [[excluded middle]].  Then a well-founded pure set is simply a set that is both well-founded and pure.

If you are (as usual) working in a well-founded material set theory and want to work with ill-founded pure sets, then you cannot do so directly; instead, follow the structural development in the next section.


## Formalization in structural set theory

In a structural set theory like [[ETCS]] or [[SEAR]], we can model a pure set by a graph describing its hereditary membership relation.

One way to state the basic theoretical idea is that the class of well-founded sets is the [[initial algebra]] of the covariant [[power set]] functor, while the class of ill-founded sets is the [[terminal coalgebra]] of the same functor.  Of course, neither of these algebras exists as a set, since this would violate [[Cantor's theorem]], but we can still describe what their elements would be like.  We can also define these algebras as [[discrete category|discrete]] [[large category|large categories]], or as proper classes in a structural set-class theory such as [[algebraic set theory]].

The discussion which follows is phrased informally, like most mathematics.  However, it is purely structural and can be interpreted in any structural set theory.  For instance, the definition below of a "graph" as a set with a binary relation should be formalized as a set $G$ together with an injection $R \hookrightarrow G \times G$.


### Membership graphs

To describe a pure set, we must give all the elements of that set, each of which is a pure set and thus must have its own elements, which are also pure sets, and so on.  A convenient way to "picture" a pure set is with a *graph*.

+-- {: .un_defn}
###### Definition
For the purposes of this page, a **graph** will mean a set $G$ of __nodes__ equipped with a binary [[relation]] $\to$ on the nodes.  A node $i$ is called a __child__ of a node $j$ if $i \to j$.
=--

The idea of a graph-picture of pure sets is that the *nodes* represent *pure sets*, and we have $i\to j$ precisely when $i\in j$.  Clearly the membership relations between any collection of pure sets should be representable by a graph.  To what extent the converse holds, i.e. which graphs can be interpreted as membership-relations between pure sets, depends on whether the pure sets in question are well-founded or ill-founded.  For purposes of drawing well-founded pure sets, only well-founded graphs should be used, whereas arbitrary graphs can be used to draw ill-founded sets.  (In fact, one form of the [[axiom of anti-foundation]] is that any graph is the picture of some pure set.)

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


### Examples of APGs

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

These sets are all well-founded.  A non-well-founded set can be represented either by an infinite picture, or by a picture with loops.  Here is an infinite picture of $\bullet = \{\bullet\}$:
$$ \array { \bullet \\ \uparrow \\ \bullet \\ \uparrow \\ \bullet \\ \uparrow \\ \vdots } $$
and here is a finite picture:
$$ \array {
           & \bullet \\
/          &         & \nwarrow \\
\backslash &         & /        \\
} $$
In both cases, the unique immediate subgraphs verify that $\bullet \in \bullet$.


### Ambiguities

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
2. Demand that duplicate occurrences always be identified, wherever they occur.
3. Define a notion of "equivalence" between APGs which is looser than isomorphism.

These are of course related; the first two can be seen as specifying a particular isomorphism class within each of the equivalence classes defined by the third.  In particular, they all result in equivalent notions of pure set, when they all apply.  (However, in [[predicative mathematics|predicative]] set theories, it seems that only the first method is applicable.)  We will consider them all in turn.


### Membership trees

A natural way to ensure that the same node is never "shared" between two occurrences is to require that our APGs be *trees*.

+-- {: .un_defn}
###### Definition
An pointed graph is a **tree** if every node admits a *unique* path to the root.  Equivalently, $G$ is a tree if its root $\top$ is a [[terminal object]] of the [[quiver]] generated by the relation $\to$.
=--

A tree may or may not be well-founded.  Note, though, that in a tree, the [[opposite relation]] $\leftarrow$ is automatically well-founded: each node has a unique [[natural number]] *height*, namely the length of its unique path to the root, so well-foundedness of $\mathbb{N}$ implies well-foundedness of $\leftarrow$.

It now makes sense to define a *pure set* to be a *rigid accessible pointed tree*.  The idea is that two such trees represent the same pure set iff they are isomorphic.   We define "membership" $G\in H$ between such trees to mean that $G$ is isomorphic to some immediate subtree of $H$ (that is, a tree $H/z$ where $z$ is a child of the root of $H$).

For example, the tree representation of $2_N$ is the one we gave first:
$$\array {
       &          & 2_N \\
       & \nearrow &     & \nwarrow \\
\empty &          &     &          & \star    \\
       &          &     &          & \uparrow \\
       &          &     &          & \empty
}
$$
and the tree representation of $\bullet = \{\bullet\}$ is the infinite path:
$$ \array { \bullet \\ \uparrow \\ \bullet \\ \uparrow \\ \bullet \\ \uparrow \\ \vdots .} $$
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

A tree models a _[[hereditarily finite set]]_ if every node has finitely many children; a tree models a well-founded hereditarily finite set if and only if it is finite and $\to$ is [[decidable subset|decidable]].  The relationship between these two facts and the no-infinite-path formulation of well-foundedness is a form of [[Konig's lemma|Kőnig's Lemma]].

Given these definitions, one can prove the various axioms of material set theory.  Specifically, if __[[ETCS]]__ holds for the structural sets (of nodes, etc) used in this definition, then $\mathbf{BZC}^-$ (which is __[[ZFC]]__ with only [[bounded separation]] and no axioms of [[axiom of replacement|replacement]] or [[axiom of foundation|foundation]]) holds for rigid trees, while $\mathbf{BZC}$ ($\mathbf{BZC}^-$ together with foundation) holds for well-founded rigid trees.  Similar results hold for [[constructive mathematics|constructive]] weakenings of ETCS and $\mathbf{BZC}^-$, since these definitions involve only function-sets and not power-sets.  Likewise, we can strengthen both sides with axioms of replacement, collection, or separation, or by adding [[Grothendieck universes]].

The argument for the [[axiom of extensionality]] is perhaps the most interesting; it goes as follows.  If each immediate subtree $G/x$ of $G$ is isomorphic to an immediate subtree $H/y$ of $H$ and conversely, then $y$ and $x$ are mutually uniquely determined by rigidity, so we have a bijection between the children of the roots of $G$ and of $H$.  Since the isomorphisms $G/x \cong H/y$ are also unique, again by rigidity, and each $G/x$ is disjoint from $G/x'$ for $x\neq x'$, by the tree property, we can piece together these isomorphisms to define an isomorphism $G\cong H$.  (In particular, the uniqueness of all these isomorphisms means that the [[axiom of choice]] is not needed.)

(Note, though, that this is only the "weak" version of extensionality.  This is sufficient for well-founded sets, but we may need to strengthen rigidity somehow to obtain stronger notions of [[extensional relation|extensionality]], which are generally more appropriate for ill-founded sets.  More precisely, the well-founded rigid trees model the usual axioms of extensionality and foundation, while arbitrary rigid trees model not Aczel's axiom of anti-foundation AFA, but its "Scott" variant, SAFA.)


### Extensional graphs

The "tree" representation can be thought of as an _unwrapped_ picture; we now consider a _wrapped_ picture in which there is no duplication at all.  The natural way to ensure this is to require our graphs to be [[extensional relation|extensional]].  For well-founded graphs, this is easy: a well-founded graph is *extensional* if for any nodes $x$ and $y$ such that for all $z$, we have $z\to x$ iff $z\to y$, then necessarily $x=y$.  For non-well-founded graphs, we need the notion of "strong extensionality" defined as follows.

+-- {: .un_defn}
###### Definition
If $G$ and $H$ are graphs, a **[[bisimulation]]** from $G$ to $H$ is a binary relation $\sim$ from $G$ to $H$ such that for any $x\in G$ and $y\in H$ with $x\sim y$, then:

* For any $a\to x$, there is some $b\in H$ with $b\to y$ and $a\sim b$, and
* For any $b\to y$, there is some $a\in G$ with $a\to x$ and $a\sim b$.

A graph $G$ is **extensional** if the largest bisimulation from $G$ to $G$ is the identity.
=--

The idea is that a bisimulation identifies pairs of nodes which "represent the same pure set."  One can show that a well-founded graph is extensional in this sense iff it is extensional in the weaker sense given above.  Note also that any extensional APG is necessarily rigid, since any isomorphism $G/x \cong G/y$ induces a bisimulation.

Thus, it also makes sense to define a *pure set* to be an *extensional APG*.  Two such APGs represent the same set iff they are isomorphic, and we define membership in the same way: $G\in H$ if $G\cong H/x$ for some child $x$ of the root of $H$.  Of course, one can again prove the axioms of material set theory from this definition.  If we restrict to well-founded extensional APGs, we get the axiom of foundation, while if we allow all extensional APGs, we get Aczel's axiom af anti-foundation (along with its strong version of the axiom of extensionality).  Note that this definition is not predicative, since the notion of extensionality involves [[quantification]] over bisimulations, which are relations, i.e. subsets.  Thus, it requires at least [[limited separation]].

For example, the extensional representation of $2_N$ is this one:
$$ \array {
2_N \\
\uparrow & \nwarrow \\
|        &          & \star    \\
|        & \nearrow &  \\
\empty   &          &
} $$
while the extensional representation of $\bullet = \{\bullet \}$ is the loop:
$$ \array {
           & \bullet \\
/          &         & \nwarrow \\
\backslash &         & /        \\
} $$
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

Now an extensional accessible graph models a [[hereditarily finite set]] iff the graph itself is finite and $\to$ is decidable.


### Equivalence

Finally, we consider the third solution to the ambiguity problem, and its relation to the first two: defining a looser notion of equivalence between APGs.  Recall the notion of bisimulation.  We say that two APGs $G$ and $H$ are **equivalent** if there is a bisimulation $\sim$ from $G$ to $H$ such that $\top\sim\top$.  Note that if $\sim$ is a bisimulation from $G$ to $H$ such that $x\sim y$, then the APGs $G/x$ and $H/y$ are equivalent; this justifies the interpretation of a bisimulation.

We can now define a *pure set* to be an APG, with *equality* represented by *equivalence* in the above sense.  Likewise, we define "membership" $G\in H$ to mean that $G$ is *equivalent* to some immediate subgraph of $H$.  One can again prove the various axioms of material set theory with these definitions (either using well-founded APGs or arbitrary ones).  As with extensional APGs, in this case we obtain the *strong* notion of [[extensional relation|extensionality]] (which is equivalent to the weak one for well-founded sets).  This definition is also not predicative.

The relationship of this approach to the previous ones is as follows.

1. Every APG is equivalent to an extensional one.  Namely, let $\approx$ be the maximal bisimulation on $G$ (the union of all bisimulations); it is an equivalence relation, and its quotient $G/\approx$ inherits the structure of an extensional APG which is equivalent to $G$.  This is the *extensional quotient*; see [[extensional relation]].

1. Two extensional APGs are equivalent iff they are isomorphic.  For if $\sim$ is a bisimulation from $G$ to $H$, then defining $x\approx y$ in $G$ if there exists a node $z$ in $H$ with $x\sim z$ and $y\sim z$ gives a bisimulation on $G$, which must be the identity, and similarly for $H$; hence $\sim$ must in fact be a bijection.  Thus, the notion of "pure set" obtained from "extensional APGs and isomorphism" is the same as that obtained from "arbitrary APGs and equivalence."

1. Every APG is equivalent to one that is a tree, its "unwrapping".  The nodes of the tree can be taken to be the finite paths $x_n \to \dots \to x_0 = \top$ ending at the root, with any "one-level extension" $x_{n+1} \to x_n \to \dots \to \top$ being a child of $x_n \to \dots\to \top$.  The bisimulation relates each path $x_n \to \dots\to \top$ to its initial node $x_n$.

1. Moreover, every APG is equivalent to a *rigid* accessible pointed tree.  The key here is to first take the extensional quotient, then perform the above "unwrapping" construction: the unwrapping of any extensional graph will always be rigid.

1. Two well-founded rigid accessible pointed trees are equivalent iff they are isomorphic.  For if $\sim$ is a bisimulation from $G$ to $H$, define a new relation $\simeq$ from $G$ to $H$ such that $x\simeq y$ iff there are paths from $x$ and $y$ to the corresponding roots which are pointwise related by $\sim$, i.e. we have $x = x_n \to x_{n-1} \to \cdots \to x_1 \to x_0 = \top$ and $y = y_n \to y_{n-1} \to \cdots \to y_1 \to y_0 = \top$, with $x_i \sim y_i$.  We can then prove by well-founded induction that whenever $x\simeq y$, then $\simeq$ is a bijection between the children of $x$ and of $y$.  For assume that all the children of $x$ and $y$ have this property.  Then if we have $x' \to x$ and $x''\to x$ with $x' \sim y$ and $x'' \sim y$, then by hypothesis $\sim$ is a bijection between $G/x'$ and $H/y$, and between $G/x''$ and $H/y$, hence we have $G/x' \cong G/x''$; thus by rigidity $x'=x''$.  Therefore, $\simeq$ is a bijection between the children of $x$ and the children of $y$.  The construction of $\simeq$ then ensures that for any child $x'\to x$, $\simeq$ relates each node in $X/x'$ to a node in at most one $Y/y'$; hence $\simeq$ is in fact a bijection from $X/x$ to $Y/y$.  Thus, by induction, $\simeq$ is a bijection.

In order to extend this last result to non-well-founded trees, we would need to use a stronger notion of rigidity.  (This makes sense since SAFA is incompatible with AFA.  We could expect to be able to use "Scott-extensionality" in place of extensionality to obtain a theory equivalent to that of rigid trees.)  For example, the following two ill-founded trees are equivalent but not isomorphic, yet both are rigid.

$$ \array{ \bullet \\ \uparrow \\ \bullet \\ \uparrow \\ \bullet \\ \vdots }
\quad\quad\quad\quad
\array{
       &          &          &          & \bullet \\
       &          &          & \nearrow &         & \nwarrow\\
       &          & \bullet  &          &         &          & \bullet\\
       & \nearrow &          &          &         & \nearrow &         & \nwarrow\\
\udots &          &          &          & \bullet &          &         &          & \bullet\\
       &          &          & \nearrow &         &          &         & \nearrow &         & \nwarrow\\
       &          & \udots   &          &         &          & \udots  &          &         &          & \ddots
}
$$

In conclusion, there are two extreme ways to represent a pure set by an isomorphism class of graphs, but any accessible pointed graph will represent a pure set one way or another.  For well-founded sets, the two extreme ways are equivalent, but for ill-founded sets the choice between them can make a difference (and in fact, there are a number of other possible variants, corresponding to the spectrum of anti-foundation axioms discussed by Aczel).

Note that the version on the left is the unwrapping of the loop; we would like a stronger version of rigidity that would rule out the version on the right.  As it is, the best that we have come up with is simply: isomorphic to the unwrapping of some extensional APG.  Technically this works, but it is not very satifsying.


## References

*  Peter Aczel (1988).  Non-well-founded sets.  CSLI 14; Stanford University.  [PDF](http://irafs.org/courses/materials/aczel_set_theory.pdf).


[[!redirects pure set]]
[[!redirects pure sets]]
