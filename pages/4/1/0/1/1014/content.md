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

The discussion which follows is phrased informally, like most mathematics.  However, it is purely structural and can be interpreted in any structural set theory.  For instance, the definition below of a "graph" as a set with a binary relation should be formalized as a set $N$ together with an injection $R \hookrightarrow N\times N$.

## Membership trees ##

In this representation, a pure set is a _rigid rooted directed tree_, possibly a _well-founded_ one.  We will define this in several stages:

*  A __[[graph|directed graph]]__ (technically, a _directed loop-graph_) consists of a set $N$ of __nodes__ and a binary [[relation]] $\to$ on the nodes; a node $i$ is called a __child__ of a node $j$ if $i \to j$.
   +--{: .query}
   AN: Here and later, I have difficulties clearly understanding the 
   meaning of "consists of"; the same holds later for "equipped with"
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
   [here](http://golem.ph.utexas.edu/category/2009/09/towards_a_computeraided_system.html#c026784).

   In case of (a), I don't understand how the new type comes formally 
   into existence in the context of SEAR. 
   In case of (b), I don't understand how any family of trees could form 
   a model of ZF in the sense of first order logic.

   _Toby_:  For purposes of formalisation in $\mathbf{SEAR}$, take (b) for all that comes below.  But to get a model of $\mathbf{ZFC}$, you need a model of $\mathbf{SEARC}$ to start with.  In this model, you have a set $M$ whose elements model sets of $\mathbf{SEAR}$; out of $M$ you can (whether your metatheory is material or structural) build a set whose elements model directed graphs in the sense of (a).  (The set whose elements model sets of $\mathbf{ZFC}$ will be a subquotient.)

   AN: You shift the burden illegitimately to the metatheory. 
   I never before heard that in order to build a model of the natural numbers in ZF one first needs a model of ZF to start with. This would make model theory impossible, requiring an infinite regress on models.

   If you need a model of SEARC in a language X to be able to give a model of ZFC then you modelled ZFC in X but not in 
   SEARC. Thus you are passing the buck from SEARC to X.
   In fact, this introduces implicit material set theory 
   since you now have an X set of SEARC sets that allows to compare and intersect in X any two SEARC sets.

   Thus the proposed reflection of ZFC in X does not avoid comparing SEARC sets, and hence nullifies your structural efforts from the point of view of foundations. (I think the same holds for ETCS, for which this page was written.)

   [[Mike Shulman]]: Building a model of the natural numbers is not a valid comparison.  A valid comparison is building a model of ZF+CH.  You cannot (if ZF is consistent) build a model of ZF+CH **in** ZF, since then ZF would prove Con(ZF+CH) and hence Con(ZF), violating the incompleteness theorem.  Rather, one starts with a model of ZF in some metatheory (which can be *significantly weaker* than ZF, although what this metatheory is is rarely made formal), and constructs in that metatheory a model of ZF+CH.  The same is true here.

   AN: You contradict yourself. If ''You cannot (if ZF is consistent) build a model of ZF+CH **in** ZF, since then ZF would prove Con(ZF+CH) and hence Con(ZF), violating the incompleteness theorem'' then by the same reasoning you can't start ''with a model of ZF in some metatheory (which can be *significantly weaker* than ZF''.
   But if you allow yourself to do the latter, you can no longer forbid the former.

   *  _Toby_:  In $ZF$, you cannot prove the consistency of either $ZF$ or $SEAR$ (at least, not as far as anybody knows).  But you can assume the consistency of one of these as a hypothesis, and then prove the consistency of the other.  This is what they an _equiconsistency_ result in model theory.  Mike is saying, I think, that you can even formulate and prove this equiconsistency in a theory much weaker than $ZF$; I don\'t know about that.  (Certainly you can *formulate* it in, say, Peano arithmetic.  But I doubt that you can prove it there.)

      [[Mike Shulman|Mike]]: I don't know offhand how strong the metatheory needs to be, but I would be surprised if BZ or HOL didn't suffice, and I think those count as "significantly weaker" than ZF.  Regardless, I think that you (AN) need to learn more about how independence and consistency proofs work before making such assertions; the two statements of mine that you cited are perfectly consistent.  You can't build a model of ZF+CH in ZF.  You can build a model of ZF+CH in ZF+"there exists a model of ZF".  And you can build a model of ZF+CH in T+"there exists a model of ZF" where T is weaker than ZF.

   _Toby_ continued:  The natural numbers also appear below as the example $\omega$.  But there is no difficulty at all in constructing that particular example in $\mathbf{SEARC}$.

   I suppose that a model of $\mathbf{SEARC}$ *would* give a notion of equality of object-sets (depending on what you model it in), but there is still no equality of sets in the language of $\mathbf{SEARC}$; you might as well complain that there is a countable model (in which every type is represented by a countable set) and so there must be a proof in $\mathbf{SEARC}$ that every set is countable.
   =--
*  Every directed graph generates a [[quiver]], a category whose morphisms are called __paths__.
*  A __[[tree]]__ (technically, a _directed rooted tree_) is a simple directed graph equipped with a __root__ node $r$ that is a [[terminal object]] of the quiver (meaning that every node has a unique path to the root).
*  The __full subtree__ of a tree rooted at a node $i$ consists of all of the nodes with a path (necessarily unique) to $i$.
*  A tree is __rigid__ if, whenever two full subtrees rooted to children of the same node are isomorphic (as graphs), then they are the same subtree.  Assuming [[classical logic]], this is equivalent to saying that any graph [[automorphism]] is the identity function.
*  A tree is __well-founded__ if $\to$ is a [[well-founded relation]].  Assuming the principle of [[excluded middle]], this is equivalent to saying that the tree has no infinite paths.  Note that the [[opposite relation]] $\leftarrow$ is automatically well-founded: each node has a unique [[natural number]] *height*, namely the length of its unique path to the root, so well-foundedness of $\mathbb{N}$ implies well-foundedness of $\leftarrow$.

These subsidiary notions are also needed:

*  Two trees are __equivalent__ if there exists a graph isomorphism between them.  Note that between rigid trees, such an isomorphism is unique.
   +--{: .query}
   AN: I don't see the meaning or relevance of this definition.
   Equivalent says exactly the same as isomorphic.

   _Toby_:  The purpose for this is to point out that this notion will be used, 

   AN: I still don't understand. Why not use the notion isomorphic, which says (by definition) exactly the same?

   *  _Toby_:  You mean, why not use the term 'isomorphic'?  Because that is a term of art from category theory (or at least algebra), and I want to use a term appropriate to talking about pure sets.  One normally says that sets are 'equal', in fact, but I avoided that since it could lead to confusion and used its weaker cousin 'equivalent'.  One doesn\'t normally say that sets are 'isomorphic' (unless one means that they are equipollent, which is definitely not what we want here), so I didn\'t want to use that word.  That is, isomorphic well-founded rigid trees are interpreted as equivalent well-founded pure sets.

      AN: But then why are you using ''isomorphic'' in the definition of rigid?

      _Toby_:  Because we\'re still talking about graphs as such.

   _Toby_ continues :
   and that it (not something weaker) is the desired notion of equivalence (anticipating that we must want one to model equality of pure sets).  Actually, that is *wrong* in the ill-founded case, depending on what you take to be the [[axiom of extensionality]] for ill-founded sets, which is what I need to fix here; we *do* want something weaker.  (Or better, replace rigidity with a stricter condition that follows from rigidity when the tree is well-founded.  That is what I\'d really like to do, but I haven\'t found a simple way to express it.  For purposes of $\mathbf{ZFC}$ including the axiom of foundation, however, this should all be correct as it is.)
   =--
*  A tree $X$ is an __immediate subtree__ of a tree $Y$ if $X$ is isomorphic to a tree rooted at one of the children of the root in $Y$; for rigid trees, this can again happen only in one way.

Then rigid trees model ill-founded pure sets; well-founded rigid trees model well-founded pure sets.  The immediate-subtree relation models the global membership relation on pure sets; equivalence models their equality.  Notice that the [[axiom of extensionality]] holds: if two trees have equivalent immediate subtrees, then they are themselves equivalent.  More generally, 
+--{: .query}
AN: I don't see, how this is more general.
It would be more important here to say that:

The immediate-subtree relation models the global membership relation 
on pure sets; being isomorphic models their equality. 

_Toby_:  By 'more generally', I meant that all of the other axioms of $\mathbf{BZC}^-$ hold, not just extensionality.  I agree with your proposed change, and included it (although with the 'equivalence' terminology).
=--
if __[[ETCS]]__ holds for the structural sets (of nodes, etc) used in this definition, then $\mathbf{BZC}^-$ (which is __[[ZFC]]__ with only bounded separation and no axioms of [[axiom of replacement|replacement]] or [[axiom of foundation|foundation]]) holds for rigid trees, while $\mathbf{BZC}$ ($\mathbf{BZC}^-$ together with foundation) holds for well-founded rigid trees.  (Similar results hold for [[constructive mathematics|constructive]] weakenings of ETCS and ZFC; other possible changes, such as adding replacement or [[Grothendieck universes]], also correspond.)

+-- {: .query}
This definition needs to be fixed; it gives only Scott-[[extensional relation|extensionality]] rather than strong extensionality, so it works for well-founded pure sets but not for ill-founded ones.  I\'ll work on it.  ---Toby

AN: Thus you'd say ''seems to hold'' in place of ''holds'' 
since at present you know only this much.

*  _Toby_:  Actually, I know what the definition should be; I just don\'t know how to express it in a nice way.  If nothing else, one could go through the wrapped picture below, which is correct as written (well, barring errors that I\'ve missed!).  Even this version is correct for the well-founded case, which is all that we need to get $\mathbf{ZFC}$.

Also, a reference to why it works for the well-founded case should be provided that gives enough details to merit being called a proof.

_Toby_:  I\'m not sure what you mean by 'should' here.  Do you mean that it would be nice if somebody writes one?  Then I agree!  Do you mean that a paper claiming that $\mathbf{SEARC}$ and $\mathbf{ZFC}$ are equivalent theories should contain such a proof?  Then you\'re probably correct, except that probably much of what is needed could just be cited from the literature by making a detour through $\mathbf{ETCS}$.  Possibly a proof of Collection would be new; I have not gone through that myself and have to trust Mike on it.  If you mean that these details need to be there for you to believe that sets in the style of material set theory can be constructed out of sets in the style of structural set theory at all, then I suggest that you look at Mac Lane & Moerdijk (or perhaps Mike knows a better reference), since that will have pointers to the established literature on this matter.
=--


### Examples ###

You can think of the root as representing the pure set itself, the root\'s children as the elements of the pure set, the next level as those elements\' elements, and so on.  In other words, the tree pictures the hierarchy of elements of the pure set if each rooted subtree is mapped to its root and $\to$ is interpreted as membership.

+--{: .query}
AN: I dont understand this piece of moral. Why should I understand a 
particular node of a pure set to represent this pure set? Certainly 
equality of nodes and equality of pure sets are completely different 
things.

It would be more appropriate to say that the tree pictures the 
hierarchy of elements of the pure set if each rooted subtree is mapped 
to its root and the arrow is interpreted as membership.
This is true irrespective of any moral.

_Toby_:  This wasn\'t meant to be so strict; how is 'can'?  And I also added your version, which is good.
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
This is equivalent to $\{\empty, \star\}$.


+--{: .query}
AN: I don't understand the relvance of this example. A tree can be 
represented graphically in thousands of ways, and represents either 
the same tree or an isomorphic tree depending on the convention 
for interpreting the graphics.

_Toby_:  The point is that a na&#239;ve way of interpreting $\{\star, \empty\}$ gives a different picture, but that is equivalent as it should be.
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
AN:

1. Do you mean with "infinite picture" a finite picture with dots 
on it? 

2. Why can't one write the same picture as a single dot with an arrow 
to itself?

_Toby_:

1. No, I mean an infinite picture, which I was not able to finish drawing.

2. No, since that would not be a tree.  But in the wrapped picture below, that is what it looks like.
=--

Of course, even a well-founded [[infinite set]] has an infinite picture, but there are no infinite paths; 
+--{: .query}
AN: No. $\omega+1$ shows that branches may be infinite. 
Only directed paths are finite.

_Toby_:  By 'branch', I think that I meant only a directed one.  Even so, can you describe the infinite branch in $\omega + 1$?; I don\'t see it.

AN: The branch (immediate subtree) whose root node is $\omega$ is infinite. [You could replace everywhere in the main text the term ''immediate subtree'' by branch]

_Toby_:  Ah, no, that is not what I mean by 'branch'.  Possibly 'path' would be better, except that this term was already defined to mean *finite* path, and the whole point here is whether the path might be infinite.  I would never read 'branch' as immediate subtree, but I agree that it might not work well to mean possibly infinite path either.

AN: I think you misuse the word branch for what you want to say. Conventionally, a branch of a rooted tree is exactly what you call an immediate subtree and not a (finite or infinite) path emanating from there. This corresponds to the notion as is used for trees in bilology, and it is also apparent when we say, at each non-leaf, the tree branches into several pieces (the branches).

_Toby_:  I can only think of 'branch' as being a path in a tree, not an entire subtree.  (In particular, when a tree branches at a node, it branches into the various edges out of or into that node.)  But I have changed the words to talk about infinite 'paths' instead.
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

By definition, a tree models a _[[hereditarily finite set]]_ if every node has finitely many children; a tree models a well-founded hereditarily finite set if and only if it is finite and $\prec$ is [[decidable subset|decidable]].  The relationship between these two facts and the no-infinite-path formulation of well-foundedness is a form of [[Konig's lemma|Kőnig's Lemma]].


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
