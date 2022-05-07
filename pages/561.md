
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

There are a number of different types of [[morphism]] bearing the name **fibration**, which are all connected to each other at least by a [[zigzag]] of relationships.


#Contents#
* table of contents
{:toc}

## Classical homotopy theory 

In classical [[homotopy theory]], a fibration $p:E\to B$ is a [[continuous function]] between [[topological spaces]] that has a certain [[lifting property]].  The most basic property is that given a point $e\in E$ and a path $[0,1] \to B$ in $B$ starting at $p(e)$, the path can be lifted to a path in $E$ starting at $e$.  

One generally also assumes the lifting of additional structures (including "higher homotopies") in $B$ which, in particular, imply that the path lifting is unique up to [[homotopy]]. Different choices of what can be lifted give rise to different notions of fibration, for example:

* In a [[Hurewicz fibration]], all sorts of homotopies can be lifted.

* In a [[Serre fibration]], topological $n$-cells can be lifted for all $n$.

* In a [[Dold fibration]] or "halb-fibration," all homotopies can be lifted, but the lifting only has to agree with the given initial map up to vertical homotopy.  A Hurewicz fibration is a Dold fibration where the vertical homotopy is stationary.

All three of these definitions give rise to a 
[[long exact sequence of homotopy groups]].  In fact, the [[exact sequence]] would follow from only requiring up-to-homotopy lifting for [[cubes]].  There doesn't seem to be a name for this sort of map, but there is the following:

* A [[quasifibration]] (not to be confused with the completely different notion related to [[quasi-categories]] below) is a map which induces a [[long exact sequence of homotopy groups]].  Equivalently, it is a map each of whose [[fibers]] is [[weak homotopy equivalence|weakly homotopy equivalent]] to the corresponding [[homotopy fiber]].


## Abstract homotopy theory 

Inspired by the role of fibrations in 
[[algebraic topology]], part of the structure of a [[model category]] or a [[category of fibrant objects]] is a class of maps called "fibrations," which also possess a lifting property relating them to the rest of the structure ([[cofibrations]] and [[weak equivalences]]).  Examples include:

* [[Kan fibrations]] between [[simplicial sets]] (whose study predates the definition of a [[model category]]), which allow lifting of $n$-[[simplices]] for every $n$.

* [[isofibration]]s between [[categories]], which allow lifting of [[isomorphisms]].

* fibrations in the [[model structure for quasi-categories]] between [[simplicial sets]] are a common  generalization of [[Kan fibrations]] and [[isofibrations]], just as [[quasi-category|quasicategories]] are a common generalization of [[Kan complex]]es and categories.

Fibrations have many good properties in [[homotopy theory]].  For example, under some extra assumptions [[pullback]] of a fibration is already a [[homotopy pullback]] (see there for details). Sufficient conditions are that in addition all three [[objects]] involved are [[fibrant objects]] or that the model category is a [[right proper model category]].  

Generally, every morphism can be replaced by a 
[[weak equivalence|weakly equivalent]] fibration, which gives one way to compute a homotopy pullback by comuting an ordinary pullback of a fibrant enough weakly quivalent [[cospan]] [[diagram]].


## Transports and classifying spaces 

There is a classical theorem that [[covering spaces]] $p:E\to B$ of a [[locally connected space]] $B$ (which have _unique_ path lifting) are equivalent to functors $\Pi(B)\to Set$ from the [[fundamental groupoid]] of $B$ to [[Set]] (hence to [[permutation representations]] of the [[fundamental group]] ).  

The functor corresponding to $p:E\to B$ takes a point $b\in B$ to its fiber $p^{-1}(b)$, and a path $\alpha$ from $b$ to $b'$ to the function $p^{-1}(b) \to p^{-1}(b')$ defined by "the endpoint of the lift of $\alpha$."

Generalizing this massively, arbitrary topological fibrations $p:E\to B$ correspond to functors from the fundamental $\infty$-groupoid of $B$ to the $(\infty,1)$-category of spaces, in an analogous way.  Points are sent to fibers, paths to the endpoints of liftings, homotopies between paths to the result of lifting such homotopies, and so on.  This functor is sometimes called the **[[parallel transport]]** corresponding to the fibration.  There are a number of ways to make this precise, some of which make sense in classical homotopy theory (e.g. actions by a loop space) and some of which require higher categorical machinery. A discussion is at [[higher parallel transport]] in the section [Flat ∞-parallel transport in Top](http://ncatlab.org/nlab/show/higher+parallel+transport#FlatInTop).

More generally, one can consider fibrations in which the fibers are equipped with some extra structure, such as being a [[vector space]] or having an [[action]] by a [[group]].  This corresponds to restricting the [[codomain]] of the transport to some category of spaces with structure and structure-preserving maps.  The most common version of this is a [[bundle]] with some structure [[group]] $G$, in which case the transport lands in $\mathbf{B}G$, the [[delooping]] [[groupoid]] of $G$ with a singleobject (thought of as a generic $G$-[[torsor]]) and $G$ as its endomorphisms.  In such cases the word "parallel" is often added in front of "transport."

If we replace the [[topological groupoid]] $\mathbf{B}G$  its  [[classifying space]], $\mathcal{B}G$ -- which is the [[geometric realization of simplicial topological spaces]] of the [[nerve]] of $\mathbf{B}G$ -- then passing to $\pi_0$ recovers the classical fact that "classifying spaces classify": there is a bijection between $G$-bundles over a space $X$ and homotopy classes of maps $X\to \mathcal{B}G$.  This bijection is realized by pulling back to $X$ the "universal $G$-bundle" $\mathcal{E}G \to \mathcal{B}G$ over the space $\mathcal{B}G$.  There are also classifying spaces for more general types of fibrations, constructed from the relevant subcategories of $Top$.


## Fibrations in category theory 

It is common in [[category theory]] to consider the objects of a [[over category|slice category]] $C/X$ as "objects of $C$ varying over $X$."  For example, an object $A\to X$ of $Set/X$ can be identified with an $X$-indexed family $\{A_x\}_{x\in X}$ of sets, where $A_x$ is the [[fiber]] of $A\to X$ over $x\in X$.  Likewise, if $X$ is a [[topological space]], we can regard an object of $Top/X$ as a family of spaces (the fibers) "varying continuously" over $X$.  But as we have seen, in the topological case, in order to make this varying into a "functor" $X\to Top$ we need the map to be a fibration.

In category theory, there is analogous notion of when a functor $p:E\to B$ is a __fibration__ or __[[fibered category]]__ or __[[Grothendieck fibration]]__ or __Cartesian fibration__, which is exactly what is needed to make the assignment $b \mapsto p^{-1}(b)$ into a [[pseudo-functor]] $B\to Cat$.  (Actually, there are two such notions, since a functor on a non-groupoid can be either [[covariant functor|covariant]] or [[contravariant functor|contravariant]].)  Thus, in this case [[Cat]] is the analogue of the "[[classifying space]]", and there is a "[[universal Cartesian fibration]]" $Cat_* \to Cat$ of which every other fibration is a [[pullback]] (modulo size issues).

Categorical fibrations also have a "lifting" property, but the liftings must satisfy an extra "universality" condition.  For this reason, they are not the fibrations in any [[model structure]] on [[Cat]].  However, fibrations of this sort between [[groupoids]] are the same as [[isofibrations]], and thus are the fibrations in the [[folk model structure]] on [[Grpd]].  See [[Grothendieck fibration]] for more details.

A __[[discrete fibration]]__ is one in which we use [[Set]] instead of [[Cat]] as the classifying space.

## Fibrations in higher category theory

* [[fibrations of quasi-categories]]

  * [[Cartesian fibration]]

  * [[left fibration]], [[right fibration]]

  * [[right/left fibration of simplicial spaces]]

  * [[inner Kan fibration]]

  * [[minimal Joyal fibration]]

## Fibrations in type theory

Fibrations are employed in [[type theory]] as the [[categorical models of dependent types]].

## Related concepts

Both forms of [[opposite 2-category|2-categorical dualization]] are commonly encountered in the context of fibrations. Moreover, the distinction between the two is appreciable. [[Cofibrations]] play a role dual to that of fibrations in homotopy theory, notably in the axioms for a [[model category]]. In this context, cofibrations have an entirely different geometric flavor from fibrations. On the other hand, [[opfibrations]] are the same as fibrations homotopically because of the invertibility of 2-cells. The duality between fibrations and opfibrations is more visible in [[category theory]], where it's the same duality as one finds between limits and colimits, for example. Confusingly, some (much?) of the older categorical (and algebro-geometric?) literature uses "cofibration" to mean "opfibration".

An [[object]] such that the unique morphism to the [[terminal object]] is a fibration (in abstract [[homotopy theory]]) is called a _[[fibrant object]]_.

A replacement of a morphism by a weakly equivalent fibration is also called a _[[resolution]]_.

[[!redirects fibrations]]