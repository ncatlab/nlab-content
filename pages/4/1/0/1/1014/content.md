A **pure set** is a [[set]] of pure sets.

This is a circular definition; if you interpret it [[recursion|recursively]], then you get **well-founded sets**; if you interpret it [[corecursion|corecursively]], then you allow for **ill-founded sets**.  (But note that the corecursive interpretation includes the well-founded sets as well, an example of the [[red herring principle]].)

At first, the only well-founded set possible is the [[empty set]] $\empty = \{ \}$, the set of no pure sets.  Once you have that, you can form $\star = \{\empty\}$, then $\{\star\}$ and $\{\empty,\star\}$, and so on.  These are the [[hereditarily finite set]]s; using an axiom of infinity, you can jump to the countably infinite set of all hereditarily finite sets and continue from there.

For ill-founded sets, there are additional possibilities, such as a set $\bullet$ such that $\bullet = \{\bullet\}$ (a suggestive model for the [[point]]), or sets $A$ and $B$ such that $A = \{B\}$ and $B = \{\empty, A\}$.  These may be ruled out by an appropriate [[axiom of foundation]].

# Formalisation

+--{: .query}
There are some problems here.  I\'ll fix it in a bit.  ---[[Toby Bartels]]
=--

In material [[set theory|set theories]] (such as ZFC and its variations), one usually assumes that everything is a pure set (although ur-elements are also sometimes used).  The late addition (1930) of Zermelo\'s [[axiom of foundation]] assures that only well-founded sets are included.

In a structural set theory like [[ETCS]], we model a pure set by the membership relation on its [[transitive set|transitive closure]].
+--{.query}
If I learnt SVG, I could draw some pictures.  (Or I could draw them in XyPic and upload them.)  ---Toby
=--
The basic idea is that the set of well-founded sets is the [[initial algebra]] of the covariant [[power set]] functor, while the set of ill-founded sets is the [[final coalgebra]] of the same functor.  Of course, neither of these algebras exists (since this would violate [[Cantor's theorem]]), but we can still describe what their elements would be like (and in fact define these algebras as [[discrete category|discrete]] [[large category|large categories]]).

Concretely, it may be easier to define first a __[[transitive set|transitive pure set]]__; this is a [[set]] (in the structural sense) $U$ equipped with an [[extensional relation]] $\in$; $U$ is a __well-founded transitive set__ if $\in$ is a [[well-founded relation]].  Then a pure set is an element of any transitive pure set; a well-founded set is an element of any well-founded transitive set.

So far, this is not very useful, since different transitive sets have no relationship.  However, a _morphism_ of well-founded transitive sets $f: U \to V$ is a [[function]] (on the underlying structural sets) such that
* $f(x) \in f(y)$ if and only if $x \in y$ and
* $f$ induces a [[bijection]] between $\{t \;|\; t \in x\}$ and $\{t \;|\; t \in f(x)\}$.

For general transitive sets, one must use the reflexive-[[transitive closure]] $\in^*$ of $\in$, although then one can combine the two conditions into one:

* $f$ induces an [[isomorphism]] (of sets equipped with a relation $\in$) between $\{t \;|\; t \in^* x\}$ and $\{t \;|\;t \in^* f(x)\}$.

Using the extensionality of $\in$, any two morphisms $f, g: U \to V$ must in fact be equal, so the category of transitive sets is a (large) [[partial order|poset]].  Furthermore, this poset has [[join]]s ([[coproduct]]s); each join (which we think of as the [[union]] of transitive sets) may be constructed as a [[quotient set]] of a [[disjoint union]] of underlying sets.  Actually, all that really matters is that this poset is finitely [[direction|directed]]; we take the [[directed limit|directed colimit]] of the entire poset to get (intuitively speaking) the union of all of the transitive sets.  Of course, this is a large object.

A little less flamboyantly, simply define a __pure set__ to be a transitive set $U$ together with an element $x$ of $U$; then define $(x,U)$ and $(y,V)$ be equal (as pure sets) if $x$ and $y$ become equal in the join $U \cup V$.  We also define that $(x,U)$ is a __member__ of $(y,V)$ if $x$ becomes a member of $y$ ($x \in y$) in the join.  The extensionality condition on $\in$ in $U \cup V$ becomes the [[axiom of extensionality]] for pure sets.

Note that each transitive pure set may itself be interpreted as a pure set.  Given a transitive set $U$, let its __[[successor]]__ $U^+$ be $U \uplus 1$ (as a set) with every element of $U$ a member of the new element of $U \uplus 1$.  Then $U$ can be identified with this new element.  That is, the elements of (the underlying structural set of) $U$ become the members of (the new element of $U \uplus 1$ which is identified with) $U$.