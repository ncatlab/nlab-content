There are a number of different types of [[morphism]] bearing the name **fibration**, which are all connected to each other at least by a zigzag of relationships.


# Classical homotopy theory #

In classical [[homotopy theory]], a fibration $p:E\to B$ is a continuous map between [[topological space]]s that has a certain lifting property.  The most basic property is that given a point $e\in E$ and a path in $B$ starting at $p(e)$, the path can be lifted to a path in $E$ starting at $e$.  One generally also assumes the lifting of additional structures (including "higher homotopies") in $B$ which, in particular, imply that the path lifting is unique up to homotopy. Different choices of what can be lifted give rise to different notions of fibration, for example:

* In a [[Hurewicz fibration]], all sorts of homotopies can be lifted.

* In a [[Serre fibration]], topological $n$-cells can be lifted for all $n$.

* In a [[Dold fibration]] or "halb-fibration," all homotopies can be lifted, but the lifting only has to agree with the given initial map up to vertical homotopy.  A Hurewicz fibration is a Dold fibration where the vertical homotopy is stationary.

All three of these definitions give rise to a long exact sequence in homotopy.  In fact, the exact sequence would follow from only requiring up-to-homotopy lifting for cubes.  There doesn't seem to be a name for this sort of map, but there is the following:

* A [[quasifibration]] (not to be confused with the completely different notion related to quasicategories below) is a map which induces a long exact sequence of homotopy groups.  Equivalently, it is a map each of whose fibers is weakly homotopy equivalent to the corresponding homotopy fiber.


# Abstract homotopy theory #

Inspired by the role of fibrations in algebraic topology, part of the structure of a [[model category]] or a [[category of fibrant objects]] is a class of maps called "fibrations," which also possess a lifting property relating them to the rest of the structure (cofibrations and weak equivalences).  Examples include:

* [[Kan fibration]]s between simplicial sets (whose study predates the definition of a model category), which allow lifting of $n$-simplices for every $n$.

* [[isofibration]]s between categories, which allow lifting of isomorphisms.

* [[quasifibration]]s between simplicial sets are a common  generalization of Kan fibrations and isofibrations, just as [[quasi-category|quasicategories]] are a common generalization of [[Kan complex]]es and categories.

Fibrations have many good properties in homotopy theory.  For example, usually the [[pullback]] of a fibration is already a [[homotopy pullback]].  Generally every map can be replaced by a weakly equivalent fibration, which gives one way to compute a homotopy pullback.


# Transports and classifying spaces #

There is a classical thorem that [[covering space]]s $p:E\to B$ (which have _unique_ path lifting) are equivalent to functors $\Pi(B)\to Set$ from the [[fundamental groupoid]] of $B$ to [[Set]].  The functor corresponding to $p:E\to B$ takes a point $b\in B$ to its fiber $p^{-1}(b)$, and a path $\alpha$ from $b$ to $b'$ to the function $p^{-1}(b) \to p^{-1}(b')$ defined by "the endpoint of the lift of $\alpha$."

Generalizing this massively, arbitrary topological fibrations $p:E\to B$ correspond to functors from the fundamental $\infty$-groupoid of $B$ to the $(\infty,1)$-category of spaces, in an analogous way.  Points are sent to fibers, paths to the endpoints of liftings, homotopies between paths to the result of lifting such homotopies, and so on.  This functor is sometimes called the **transport** corresponding to the fibration.  There are a number of ways to make this precise, some of which make sense in classical homotopy theory (e.g. actions by a loop space) and some of which require higher categorical machinery.

More generally, one can consider fibrations in which the fibers are equipped with some extra structure, such as being a vector space or having an action by a group.  This corresponds to restricting the codomain of the transport to some category of spaces with structure and structure-preserving maps.  The most common version of this is a [[bundle]] with some structure [[group]] $G$, in which case the transport lands in $\mathbf{B}G$, the category with one object (thought of as a generic $G$-[[torsor]]) and $G$ as its endomorphisms.  In such cases the word "parallel" is often added in front of "transport."

If we replace the groupoid $\mathbf{B}G$  by its [[classifying space]] $\mathcal{B}G$-- which is the [[geometric realization]] of the [[nerve]] of $\mathbf{B}G$ -- then passing to $\pi_0$ recovers the classical fact that "classifying spaces classify": there is a bijection between $G$-bundles over a space $X$ and homotopy classes of maps $X\to \mathcal{B}G$.  This bijection is realized by pulling back to $X$ the "universal $G$-bundle" $\mathcal{E}G \to \mathcal{B}G$ over the space $\mathcal{B}G$.  There are also classifying spaces for more general types of fibrations, constructed from the relevant subcategories of $Top$.


# Fibrations in category theory #

It is common in category theory to consider the objects of a [[over category|slice category]] $C/X$ as "objects of $C$ varying over $X$."  For example, an object $A\to X$ of $Set/X$ can be identified with an $X$-indexed family $\{A_x\}_{x\in X}$ of sets, where $A_x$ is the [[fiber]] of $A\to X$ over $x\in X$.  Likewise, if $X$ is a [[topological space]], we can regard an object of $Top/X$ as a family of spaces (the fibers) "varying continuously" over $X$.  But as we have seen, in the topological case, in order to make this varying into a "functor" $X\to Top$ we need the map to be a fibration.

In category theory, there is analogous notion of when a functor $p:E\to B$ is a __fibration__, which is exactly what is needed to make the assignment $b \mapsto p^{-1}(b)$ into a pseudo-functor $B\to Cat$.  (Actually, there are two such notions, since a functor on a non-groupoid can be either covariant or contravariant.)  Thus, in this case $Cat$ is the analogue of the "classifying space," and there is a "universal fibration" $Cat_* \to Cat$ of which every other fibration is a pullback (modulo size issues).

Categorical fibrations also have a "lifting" property, but the liftings must satisfy an extra "universality" condition.  For this reason, they are not the fibrations in any model structure on $Cat$.  However, fibrations of this sort between groupoids are the same as isofibrations, and thus are the fibrations in the [[folk model structure]] on $Grpd$.  See [[Grothendieck fibration]] for more details.

A __[[discrete fibration]]__ is one in which we use [[Set]] instead of [[Cat]] as the classifying space.


# Discussion #

The following discussion was prompted by an earlier version of this page.

+--{.query}
[[Tim Porter|Tim]]: I do not quite agree with 'transport' as being the main point of fibrations. Rather 'lifting' is the main point, in particular lifting of homotopies, at least in topological situations.   For transport, one needs connections of some sort to get things working well, but in many cases  there is only a very weak notion of action, so perhaps that should be derived as a property rather than taken as a 'defining property' in some sense.

Perhaps a reference to Stasheff and Wirth 
 
James Wirth & Jim Stasheff

_Homotopy Transition Cocycles_

math.AT/0609220.

and the discussion

http://golem.ph.utexas.edu/category/2006/09/wirth_and_stasheff_on_homotopy.html

on the cafe would be a good idea to add.

_[[Urs Schreiber|Urs]]:_ In situations where one wants
to talk of transport, the fibration usually arises as the
pullback of some "universal fibration", a
[[generalized universal bundle]]. For instance 
(split op-)fibrations of categories are precisely the pullbacks of the universal $Cat$-bundle 
$Cat_* \to Cat$ along a functor $F : C \to Cat$.

If one looks at this kind of situation where we do have an established notion of _(parallel) transport_ one sees:

* it is the classifying functor $F : C \to Cat$ which should be addressed as the "(parallel) transport", while the corresponding fibration is its "action object" as in [[action groupoid]], i.e. the thing whose objects are all possible things that the parallel transport can transport and whose morphisms take these things to the image of that transport. So it's a subtle difference, but an important one.

For instance, to make this more concrete, consider the category of [[generalized smooth space|smooth]] [[groupoid]]s (which is a [[category of fibrant objects]]), let for any manifold $X$ the groupoid $P_1(X)$ be the groupoid of smooth thin-homotopy classes of paths in $X$, let $G$ be any Lie group, $\mathbf{B} G$ the corresponding one-object Lie groupoid and consider the _universal fibration _ $\mathbf{E} G \to \mathbf{B}G$ -- the groupoid incarnation of the universal $G$-bundle as described at [[generalized universal bundle]]. Then

Theorem: $G$-bundles with connection on $X$ are equivalent to functors $tra : \widehat{P_1(X)} \to \mathbf{B}G$ out of acyclic fibrations $\widehat{P_1(X)} \to P_1(X)$ over $P_1(X)$ (i.e. smooth [[anafunctor]]s $P_1(X) \to \mathbf{B}G$). These functors are literally the corresponding "parallel transport": indeed, evaluated on a path $\gamma$ in $X$ there is locally a 1-form $A \in \Omega^1(X, Lie(G))$ such that the group element $tra(\gamma)$ is the traditional parallel transport of that 1-form, $tra(\gamma) = P exp(\int_\gamma A)$.

Now, we can form the fibration which is associated with this parallel transport, namely the pullback

$$
  \array{
     tra^* \mathbf{E} G &\to& \mathbf{E}G
     \\
     \downarrow && \downarrow
     \\
     \widehat{P_2(X)} &\stackrel{tra}{\to}& \mathbf{B}G
     \\
     \downarrow
     \\
     P_2(X)
  }
  \,.
$$

This fibration $tra^* \mathbf{E}G \to \widehat{P_2(X)}$ is what is properly speaking the [[action groupoid]] of $tra$ acting on the fibers of the principal $G$-bundle. 

_[[Mike Shulman|Mike]]_:  Can you clarify the distinction between "lifting" and "transport"?  In what way does the lifting of a path $f$ starting at a point $e$ _not_ transport $e$ along $f$?  Certainly in geometric situations to get a _parallel_ notion of transport, you need a connection, but I see that as a stronger requirement.

_[[Mike Shulman|Mike]] adds_: In fact, any topological fibration over $X$ (not just a bundle) induces a "transport" map from (the fundamental $\infty$-groupoid of) $X$ to the $(\infty,1)$-category $Top$, taking each point to its fiber.  Putting extra structure on the fibration, such as making it a $G$-bundle, corresponds to restricting the codomain of the transport functor to land in some smaller subcategory, such as $\mathbf{B}G$.  A reference in classical homotopy theory is May's "Classifying spaces and fibrations."

I agree with what Urs said that the "transport" properly refers to the corresponding functor into $Top$, $Cat$, or $\mathbf{B}G$, with the fibration being the "action object."  Then the property of "being a fibration" means "can be equipped with a transport" or "can be obtained from a transport."  These are all important points to be added, but I think that what I wrote is still correct.


-[[Tim Porter|Tim]] The transport aspect of course is there, but as the lifting is not unique the idea of the transport being 'up to coherent homotopy' or '$\infty$-homotopy is much more sophisticated than the simple point of the existence of a 'lifting'.  My point is that although correct your definition may be accused of being 'mathematics made difficult'.  To have a definition of fibration that somehow requires one to have understood $(\infty,1)$-categories and the fundamental $\infty$-groupoid of a space is, to me, the wrong way around.  The simply stated lifting property leads eventually naturally to the beautiful transport description (and is more general, more classically based, and probably more approachable).  That process is  only recently understood and is still only understood by a handful of people who work with fibrations. 

If you look at the classical treatment of fibre spaces (and I found a copy of Grothendieck's 1950s notes on them in a pile of stuff today), there is no thought of transport, just of lifting. Serre, who revolutionised the algebraic topology of fibre spaces and fibrations is using lifting, not transport. The link between the transport functor and the notion of fibration emerged via the 'Grothendieck construction' (due to Ehresmann as well.. and there transport was part of the story that he wanted) but was part of the image of fibre spaces\fibrations as being like semi-direct products and that took a long time to get to the present state.


_[[Mike Shulman|Mike]]_: Well, I think a lot of what we do here could be accused of being "mathematics made difficult."  Cf. the first sentence of [[group]].  But I believe that it is useful and important to have a correct conceptual understanding, in addition to any technically simpler definition that one works with in practice.

For instance, I believe that the "real" definition of a [[monoidal category]] requires that "all diagrams of constraints commute," while the fact that it's enough to check two particular diagrams is a happy accident.  Presenting the pentagon and unit axioms as the God-given definition of a monoidal category, without mentioning that the only reason this is an okay definition is because you can prove a coherence theorem from it, leads the student quite naturally to wonder why God likes pentagons.

Likewise, I believe that the only reason the definition of a fibration via lifting properties is a _correct_ definition is that it _does_ lead to the complete functoriality up to higher homotopies.  (One doesn't need complicated notions of $\infty$-categories to get an intuitive feel for how this works: it's enough to observe that lifting of 2-cells gives you homotopy-uniqueness for lifts of paths, lifting of 3-cells gives you homotopy-uniqueness for lifts of 2-cells, etc.) The fact that it took many years for this to be understood is not, to me, an argument against its truth, or against its expository helpfulness.

Also, I wrote this page not to be just about the topological notion of fibration, but to include categorical (Grothendieck) fibrations as well and show the commonality between them.  And for that I think the notion of transport is indispensable, since categorical fibrations can't be defined by a simple lifting property.


_Mike, again_: Okay, I basically rewrote the whole page, trying to take your comments into account.  What do you think of it now?

[[Tim Porter|Tim]] :  It looks good. My objection was, sort of, pedagogical as I did not want to put off the reader who might be wanting to understand fibrations from the infinity cat point of view.  You nicely ease the way in, suggesting how the understanding of the basic classical notion evolves.  I like it.  Thanks.  

PS. Wikipedia entries for fibration and fibred category exist and could be used if you think they are consistent enough with you wishes for this.  

[[Urs Schreiber|Urs]]: thanks, nice entry. Eventually it would be nice if we could say more about _which fibrations are fibrations_: which notion of fibred ($n$-)categories/groupoids are fibrations with respect to which model structure. I once tried to collect a bit of data on this, but I need to dig out my old notes, and they were likely very incomplete anyway.

[[Ronnie Brown|Ronnie]]: I made a few minor changes, but I also find it odd to define a fibration in terms of a hypothetical fundamental $\infty$-groupoid of $B$. What is this animal? 

With regard to transport I like the old papers of Philip R. Heath on operations and fibrations-

Heath, Philip R. Groupoid operations and fibre-homotopy equivalence. I.  Math. Z.  130  (1973), 207--233.
(the first of 3 papers)

If $p:E \to B$ is a fibration then there is an operation of the paths on the base on the fibres the laws of an operation holding up to homotopy.  

At Hull, Phil and I were amused by the fact that the unit interval $I=[0,1]$ is a cogroupoid up to homotopy  where homotopy is defined using $I$!. This led to his thesis work on fibrations, getting away from the base point approach of the loops on the base operates on the fibre. Maybe effort should be put in to defining and constructing an $\infty$-cogroupoid (up to homotopy)! 

=--
