A **pure set** is a [[set]] of pure sets.

This is a circular definition; if you interpret it [[recursion|recursively]], then you get **well-founded sets**; if you interpret it [[corecursion|corecursively]], then you allow for **ill-founded sets**.  (But note that the corecursive interpretation includes the well-founded sets as well, an example of the [[red herring principle]].)

At first, the only well-founded set possible is the [[empty set]] $\empty = \{ \}$, the set of no pure sets.  Once you have that, you can form $\star = \{\empty\}$, then $\{\star\}$ and $\{\empty,\star\}$, and so on.  These are the [[hereditarily finite set]]s; using an axiom of infinity, you can jump to the countably infinite set of all hereditarily finite sets and continue from there.

For ill-founded sets, there are additional possibilities, such as a set $\bullet$ such that $\bullet = \{\bullet\}$ (a suggestive model for the [[point]]), or sets $A$ and $B$ such that $A = \{B\}$ and $B = \{\empty, A\}$.  These may be ruled out by an appropriate [[axiom of foundation]] (or explicitly allowed and tamed by the dual axiom of anti-foundation).

## Formalisation ##

In material [[set theory|set theories]] (such as ZFC and its variations), one usually assumes that everything is a pure set (although ur-elements are also sometimes used).  The late addition (1930) of Zermelo\'s [[axiom of foundation]] assures that only well-founded sets are included.

In a structural set theory like [[ETCS]], we can model a pure set by its membership tree or by the membership relation on its [[transitive set|transitive closure]].

The basic theoretical idea is that the set of well-founded sets is the [[initial algebra]] of the covariant [[power set]] functor, while the set of ill-founded sets is the [[final coalgebra]] of the same functor.  Of course, neither of these algebras exists (since this would violate [[Cantor's theorem]]), but we can still describe what their elements would be like (and in fact define these algebras as [[discrete category|discrete]] [[large category|large categories]]).

## Membership trees ##

In the representation, a pure set is a _fixed rooted directed tree_, possibly a _well-founded_ one.  We will define this in several stages:
*  A __[[digraph|directed graph]]__ (technically, a _simple_ directed _pseudo_graph) consists of a set $N$ of _nodes_ and a binary _directed adjacency_ [[relation]] $\to$ on the nodes.
*  Every directed graph (simple or not) generates a [[quiver]], a category whose morphisms are called _paths_.
*  A __tree__ (technically, a _directed_ _rooted_ tree) is a simple directed graph equipped with a _root_ node $r$ that is a [[terminal object]] of the quiver (meaning that every node has a unique path to the root).
*  A __well-founded tree__ is a tree such that $\to$ is a [[well-founded relation]] (note that the [[opposite relation]] $\leftarrow$ is automatically well-founded).  Assuming the principal of [[excluded middle]], this equivalent to saying that every branch in the tree is of finite length
*  A tree (well-founded or not) is __fixed__ if, whenever two subtrees rooted to the same node are isomorphic (as graphs), then they are the same subtree; equivalently, any graph-automorphism of the tree must be the identity map.

These subsidiary notions are also needed:
*  Two extensional trees are __equal__ if there exists a graph isomorphism between them; note that (thanks to fixedness) such an isomorphism must be unique.
*  One extensional tree $X$ is an __immediate subtree__ of a tree $Y$ if $X$ is isomorphic to a tree rooted at one of the children of the root in $Y$; again (thanks to fixedness) this can happen only in one way.

Then fixed trees model ill-founded pure sets; well-founded fixed trees model well-founded pure sets.  The immediate-subtree relation models the global membership relation on pure sets.  Notice that the [[axiom of extensionality]] holds: if two tree have the same (isomorphic) immediate subtrees, then they are themselves equal (isomorphic).  More generally, if [[ETCS]] holds for the structural sets (of nodes, etc) used in this definition, then ZC ([[ZFC]] without the axioms of [[axiom of replacement|replacement]] and [[axiom of foundation|foundation]]) holds for fixed trees, while ZC and foundation hold for well-founded fixed trees.  (Similar results hold for [[constructive mathematics|constructive]] weakenings of ETCS and ZFC; other possible changes, such as adding replacement or [[Grothendieck universe]]s, also correspond.)

### Examples ###

You should think of the root as representing the pure set itself, the root\'s children as the elements of the pure set, the next level as those elements\' elements, and so on.

So $\empty = \{ \}$ consists of nothing but a root:
$$ \empty $$

The set $\star = \{\empty\}$ has the empty set attached to the root (which we draw at the top):
$$ \array { \star \\ \uparrow \\ \empty } $$

Then $2_Z = \{\star\}$ and $2_N = \{\empty, \star\}$ are as follows:
$$ \array { 2_Z \\ \uparrow \\ \star \\ \uparrow \\ \empty } \quad \quad \quad \quad \array { 
       &          & 2_N \\
       & \nearrow &     & \nwarrow \\
\empty &          &     &          & \star    \\
       &          &     &          & \uparrow \\
       &          &     &          & \empty
} $$

At first, $\{\star, \empty\}$ might appear different:
$$ \array {
         &          & \bullet \\
         & \nearrow &         & \nwarrow \\
\bullet  &          &         &          & \bullet  \\
\uparrow \\
\bullet
} $$
But this is isomorphic to $\{\empty, \star\}$.

Na&#239;vely, $\{\star, \star\}$ looks like this:
$$ \array { 
         &          & \bullet \\
         & \nearrow &         & \nwarrow \\
\bullet  &          &         &          & \bullet  \\
\uparrow &          &         &          & \uparrow \\
\bullet  &          &         &          & \bullet
} $$
But this is not fixed, since the obvious vertical symmetry is a non-identity automorphism.  Really we should use $\{\star\}$ again.

A non-well-founded set will give an infinite picture; here is $\bullet = \{\bullet\}$:
$$ \array { \bullet \\ \uparrow \\ \bullet \\ \uparrow \\ \bullet \\ \uparrow \\ \vdots } $$

Of course, even a well-founded infinite set has an infinite picture, but each individual branch is finite; here is $\omega$, the set of von Neumann [[natural number]]s:
$$ \array {
        &          &          & \omega  \\
        & \nearrow & \nearrow &         & \nwarrow & \cdots \\
\empty  &          & \star    &         &          & 2_N      & \cdots \\
        &          & \uparrow &         & \nearrow & \uparrow & \cdots \\
        &          & \empty   & \empty  &          & \star    & \cdots \\
        &          &          &         &          & \uparrow & \cdots \\
        &          &          &         &          & \empty   & \cdots \\
        &          &          &         &          &          & \vdots } $$

By definition, a tree models a _[[hereditarily finite set]]_ if every node has finitely many children; classically (at least) a tree models a well-founded hereditarily finite set if and only if it is finite.  The relation between these two facts and the finite-branch formulation of well-foundedness is a form of K&#337;nig's Lemma.

## Transitive pure sets ##

The picture above may be seen as an _unwrapped_ representation; there is also a _wrapped_ picture.

+--{: .query}
There remainder is largely wrong.  I\'ll fix it later, or you can look at [Aczel](http://standish.stanford.edu/pdf/00000056.pdf) to help.  ---[[Toby Bartels]]
=--

Concretely, it may be easier to define first a __[[transitive set|transitive pure set]]__; this is a [[set]] (in the structural sense) $U$ equipped with an [[extensional relation]] $\in$; $U$ is a __well-founded transitive set__ if $\in$ is a [[well-founded relation]].  Then a pure set is an element of any transitive pure set; a well-founded set is an element of any well-founded transitive set.

So far, this is not very useful, since different transitive sets have no relationship.  However, a _morphism_ of well-founded transitive sets $f: U \to V$ is a [[function]] (on the underlying structural sets) such that
* $f(x) \in f(y)$ if and only if $x \in y$ and
* $f$ induces a [[bijection]] between $\{t \;|\; t \in x\}$ and $\{t \;|\; t \in f(x)\}$.

For general transitive sets, one must use the reflexive-[[transitive closure]] $\in^*$ of $\in$, although then one can combine the two conditions into one:

* $f$ induces an [[isomorphism]] (of sets equipped with a relation $\in$) between $\{t \;|\; t \in^* x\}$ and $\{t \;|\;t \in^* f(x)\}$.

Using the extensionality of $\in$, any two morphisms $f, g: U \to V$ must in fact be equal, so the category of transitive sets is a (large) [[partial order|poset]].  Furthermore, this poset has [[join]]s ([[coproduct]]s); each join (which we think of as the [[union]] of transitive sets) may be constructed as a [[quotient set]] of a [[disjoint union]] of underlying sets.  Actually, all that really matters is that this poset is finitely [[direction|directed]]; we take the [[directed limit|directed colimit]] of the entire poset to get (intuitively speaking) the union of all of the transitive sets.  Of course, this is a large object.

A little less flamboyantly, simply define a __pure set__ to be a transitive set $U$ together with an element $x$ of $U$; then define $(x,U)$ and $(y,V)$ be equal (as pure sets) if $x$ and $y$ become equal in the join $U \cup V$.  We also define that $(x,U)$ is a __member__ of $(y,V)$ if $x$ becomes a member of $y$ ($x \in y$) in the join.  The extensionality condition on $\in$ in $U \cup V$ becomes the [[axiom of extensionality]] for pure sets.

Note that each transitive pure set may itself be interpreted as a pure set.  Given a transitive set $U$, let its __[[successor]]__ $U^+$ be $U \uplus 1$ (as a set) with every element of $U$ a member of the new element of $U \uplus 1$.  Then $U$ can be identified with this new element.  That is, the elements of (the underlying structural set of) $U$ become the members of (the new element of $U \uplus 1$ which is identified with) $U$.