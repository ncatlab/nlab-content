
+--{: .query}
[[Arnold Neumaier]]: I added some comments originating from my 
attempts to read this wieth the interpretation of sets as SEAR 
sets in mind.
=--

A **pure set** is a [[set]] of pure sets.

+--{: .query}
AN: This cannot be true literally when set is a SEAR set. 
The statement should therefore be marked explicitly as informal. 
=--

This is a circular definition; if you interpret it [[recursion|recursively]], then you get **well-founded sets**; if you interpret it [[corecursion|corecursively]], then you allow for **ill-founded sets**.  (But note that the corecursive interpretation includes the well-founded sets as well, an example of the [[red herring principle]].)

At first, the only well-founded set possible is the [[empty set]] $\empty = \{ \}$, the set of no pure sets.  Once you have that, you can form $\star = \{\empty\}$, then $\{\star\}$ and $\{\empty,\star\}$, and so on.  These are the [[hereditarily finite sets]]; using an axiom of infinity, you can jump to the [[countably infinite set]] of all hereditarily finite sets and continue from there.

For ill-founded sets, there are additional possibilities, such as a set $\bullet$ such that $\bullet = \{\bullet\}$ (a suggestive model for the [[point]]), or sets $A$ and $B$ such that $A = \{B\}$ and $B = \{\empty, A\}$.  These may be ruled out by an appropriate [[axiom of foundation]], or explicitly allowed and tamed by the dual axiom of anti-foundation.

## Formalisation ##

In material [[set theory|set theories]] (such as ZFC and its variations), one usually assumes that everything is a pure set (although ur-elements are also sometimes used).  The late addition (von Neumann 1925, Zermelo 1930) of the [[axiom of foundation]] assures that only well-founded sets are included.

In a structural set theory like [[ETCS]], we can model a pure set by its membership tree or by the membership relation on its reflexive-[[transitive set|transitive closure]].

The basic theoretical idea is that the class of well-founded sets is the [[initial algebra]] of the covariant [[power set]] functor, while the class of ill-founded sets is the [[terminal coalgebra]] of the same functor.  Of course, neither of these algebras exists (since this would violate [[Cantor's theorem]]), but we can still describe what their elements would be like (and in fact define these algebras as [[discrete category|discrete]] [[large category|large categories]]).

### Membership trees ###

In this representation, a pure set is a _rigid rooted directed tree_, possibly a _well-founded_ one.  We will define this in several stages:
*  A __[[directed graph]]__ (technically, a _simple directed pseudograph_) consists of a set $N$ of __nodes__ and a binary [[relation]] $\to$ on the nodes; a node $i$ is called a __child__ of a node $j$ if $i \to j$.

+--{: .query}
AN: Here and later, I have difficulties clearly understanding the 
meaning of ``consists of''; the same holds later for ``equipped with''
- do these phrases convey the same or something different?

Is the above sentence to be formally understood as saying that a 
directed graph is (a) a single object of a certain type, 
or (b) just a way of speaking?

(a) would mean that there is a metacollection G of graphs, a mapping N 
from G to the metacollection of sets, and a mapping T from G to the 
metacollection of relations , such that for the graph g talked about 
in the above statement, N(g) would be the above $N$ and T(g) would be 
the above $\to$.

(b) would mean that directed graphs are not single objects but only a
shorthand for saying something about a set and a binary relation on 
this set, in the sense of Mike Shulman's comment 
<a href="http://golem.ph.utexas.edu/category/2009/09/towards_a_computeraided_system.html#c026784">here</a>.

In case of (a), I don't understand how the new type comes formally 
into existence in the context of SEAR. 
In case of (b), I don't understand how any family of trees could form 
a model of ZF in the sense of first order logic.
=--


*  Every directed graph (simple or not) generates a [[quiver]], a category whose morphisms are called __paths__.
*  A __tree__ (technically, a _directed rooted tree_) is a simple directed graph equipped with a __root__ node $r$ that is a [[terminal object]] of the quiver (meaning that every node has a unique path to the root).
*  The __full subtree__ of a tree rooted at a node $i$ consists of all of the nodes with a path (necessarily unique) to $i$.
*  A tree is __rigid__ if, whenever two full subtrees rooted to children of the same node are isomorphic (as graphs), then they are the same subtree; equivalently, any graph [[automorphism]] of the tree must be the identity function.

+--{: .query}
AN: Here and later, ``must be'' should be ``is''.
=--


*  A tree is __well-founded__ if $\to$ is a [[well-founded relation]] (note that the [[opposite relation]] $\leftarrow$ is automatically well-founded).  Assuming the principle of [[excluded middle]], this is equivalent to saying that every branch in the tree is of finite length.

These subsidiary notions are also needed:
*  Two trees are __equivalent__ if there exists a graph isomorphism between them; for rigid trees, such an isomorphism must be unique.

+--{: .query}
AN: I don't see the meaning or relevance of this definition.
Equivalent says exactly the same as isomorphic.
=--


*  A tree $X$ is an __immediate subtree__ of a tree $Y$ if $X$ is isomorphic to a tree rooted at one of the children of the root in $Y$; for rigid trees, this can again happen only in one way.

Then rigid trees model ill-founded pure sets; well-founded rigid trees model well-founded pure sets.  The immediate-subtree relation models the global membership relation on pure sets.  Notice that the [[axiom of extensionality]] holds: if two trees have equivalent immediate subtrees, then they are themselves equivalent.  More generally, 

+--{: .query}
AN: I don't see, how this is more general.
It would be more important here to say that:

The immediate-subtree relation models the global membership relation 
on pure sets; being isomorphic models their equality. 
=--


if __[[ETCS]]__ holds for the structural sets (of nodes, etc) used in this definition, then $\mathbf{ZC}^-$ (which is __[[ZFC]]__ without the axioms of [[axiom of replacement|replacement]] and [[axiom of foundation|foundation]]) holds for rigid trees, while $\mathbf{ZC}$ ($\mathbf{ZC}^-$ together with foundation) holds for well-founded rigid trees.  (Similar results hold for [[constructive mathematics|constructive]] weakenings of ETCS and ZFC; other possible changes, such as adding replacement or [[Grothendieck universes]], also correspond.)

+-- {: .query}
This definition needs to be fixed; it gives only Scott-[[extensional relation|extensionality]] rather than strong extensionality.  I\'ll work on it.  ---Toby
=--

#### Examples ####

You should think of the root as representing the pure set itself, the root\'s children as the elements of the pure set, the next level as those elements\' elements, and so on.  

+--{: .query}
AN: I dont understand this piece of moral. Why should I understand a 
particular node of a pure set to represent this pure set? Certainly 
equality of nodes and equality of pure sets are completely different 
things.

It would be more appropriate to say that the tree pictures the 
hierarchy of elements of the pure set if each rooted subtree is mapped 
to its root and the arrow is interpreted as membership.
This is true irrespective of any moral.
=--


Note that the nodes in most of the pictures below have labels, but these are for illustration only; they are *not* part of the structure defining the tree.

First, $\empty = \{ \}$ consists of nothing but a root:
$$ \empty $$

The set $\star = \{\empty\}$ has the empty set attached to the root (which we draw at the top):
$$ \array { \star \\ \uparrow \\ \empty } $$
Notice that $\empty$ is an immediate subtree, so we can write $\empty \in \star$.

Then $2_Z = \{\star\}$ and $2_N = \{\empty, \star\}$ are as follows:
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
This is isomorphic to $\{\empty, \star\}$.


+--{: .query}
AN: I don't understand the relvance of this example. A tree can be 
represented graphically in thousands of ways, and represents either 
the same tree or an isomorphic tree depending on the convention 
for interpreting the graphics.
=--

We might want to write $2_Z$ as $\{\star, \star\}$:
$$ \array { 
         &          & 2_Z \\
         & \nearrow &     & \nwarrow \\
\star    &          &     &          & \star    \\
\uparrow &          &     &          & \uparrow \\
\empty   &          &     &          & \empty
} $$
But this is not rigid, since the obvious vertical symmetry is a non-identity automorphism.

A non-well-founded set will give an infinite picture; here is $\bullet = \{\bullet\}$:
$$ \array { \bullet \\ \uparrow \\ \bullet \\ \uparrow \\ \bullet \\ \uparrow \\ \vdots } $$
Looking at the immediate subtree, we verify that $\bullet \in \bullet$.

+--{: .query}
AN: 1. Do you mean with ``infinite picture'' a finite picture with dots 
on it? 

2. Why can't one write the same picture as a dingle dot with an arrow 
to itself?
=--


Of course, even a well-founded [[infinite set]] has an infinite picture, but each individual branch is finite; 

+--{: .query}
AN: No. $\omega+1$ shows that branches may be infinite. 
Only directed paths are finite.
=--


here is $\omega_N$, the set of von Neumann [[natural numbers]]:
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

By definition, a tree models a _[[hereditarily finite set]]_ if every node has finitely many children; a tree models a well-founded hereditarily finite set if and only if it is finite and $\prec$ is [[decidable subset|decidable]].  The relationship between these two facts and the finite-branch formulation of well-foundedness is a form of [[Konig's lemma|K\u0151nig's Lemma]].

### Reflexive-transitive closures as graphs ###

The picture above may be seen as an _unwrapped_ representation; there is also a _wrapped_ picture.

In this representation, a pure set is an _extensional accessible graph_, again possibly a _well-founded_ one.  Again, we will define this in several stages:
*  A __[[directed graph]]__ again consists of a set $N$ of __nodes__ and a binary [[relation]] $\to$ on the nodes; again, $i$ is a __child__ of $j$ is $i \to j$.
*  Now instead of forming the quiver of paths, we simply form the [[transitive closure]] $\to^*$ of $\to$.  That is, we only care whether there exists a path, not which paths there are.
*  A graph is __accessible__ (technically, _directed accessible pointed_) if it is equipped with a __root__ node $r$ that is a [[top]] of $\to^*$ (meaning that every node has a path to the root).
*  A graph is __extensional__ if $\to$ is an [[extensional relation]]; this is probably the most complicated part.
*  A graph is __well-founded__ if $\to$ is a [[well-founded relation]] (note that the [[opposite relation]] $\leftarrow$ is automatically well-founded for an accessible graph).

These subsidiary notions are also needed:
*  Two graphs are __equivalent__ if there exists a graph isomorphism between them; for extensional graphs, such an isomorphism must be unique.
*  An accessible graph $X$ is an __immediate subgraph__ of an accessible graph $Y$ if $X$ is isomorphic to the $\to^*$-downset of one of the children of the root in $Y$; for extensional graphs, this can again happen only in one way.

In this picture, the nodes are precisely the elements of the reflexive-[[transitive closure]] of the pure set, and the relation $\to$ on them is precisely the membership relation $\in$.

#### Examples ####

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

### Relation between these ###

Peter Aczel\'s general model of a pure set is any _simple directed accessible pointed pseudograph_.  That is, the graph need not be a tree (much less a rigid one), nor need it be extensional.  One can make such a graph extensional by identifying nodes to make the extensional quotient as explained at [[extensional relation]].  Then one can unwrap this extensional graph into a rigid tree by including one copy of each node for each of its paths to the root.  So there are two extreme ways to represent a pure set by an isomorphism class of graphs, but any accessible graph will represent a pure set one way or another.

## References ##

*  Peter Aczel (1988).  Non-well-founded sets.  CSLI 14; Stanford University.  [PDF](http://standish.stanford.edu/pdf/00000056.pdf).

[[!redirects pure sets]]











