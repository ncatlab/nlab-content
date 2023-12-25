
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--



# Total orders
* table of contents
{: toc}


## Idea

A _total order_ or _linear order_ on a set is a way of ordering its elements to say that some elements precede others, with the understanding that any two elements can be compared one way or the other.

## Definitions

Given a [[set]] $S$, a __total order__ or __linear order__ on $S$ is a (binary) [[relation]] $\leq$ with the following properties:

* [[reflexive relation|reflexivity]]: for any element $x$ of $S$, $x \leq x$;
* [[transitive relation|transitivity]]: whenever $x \leq y \leq z$, then $x \leq z$;
* [[antisymmetric relation|antisymmetry]]: whenever $x \leq y \leq x$, then $x = y$;
* [[total relation|totality]]: for any $x$ and $y$ in $S$, $x \leq y$ or $y \leq x$.

A __totally ordered set__ or __toset__ or __linearly ordered set__ or __loset__ is a set equipped with a total order/linear order.

## Relation to simplices

The category of finite nonempty totally ordered sets and order-preserving maps is called $\Delta$, the [[simplex category]]. 

The category of *all* finite totally ordered sets and order-preserving maps is called $\Delta_a$, the **augmented** simplex category.

## Relation to pseudolattices

Due to the totality of the order relation $\leq$, every pair of elements $a$ and $b$ has a [[join]] and [[meet]], such that $a \wedge b = a$ and $a \vee b = b$, or $a \wedge b = b$ and $a \vee b = a$. This means that meets distribute over joins and joins distribute over meets, and additionally that both operations are [[associative]], [[commutative]], and [[idempotent]], and so every total order is a [[pseudolattice]], and every bounded total order is a [[lattice]]. 

## Relation to strict total orders

A [[strict total order]] is much like a total order, except that it is based on an irreflexive relation $\lt$.

Using [[excluded middle]], one can move between strict total orders and total orders using [[negation]]; that is, the negation of a total order is a strict total order and vice versa.  Actually one usually swaps the order too, as follows:

* $x \leq y$ iff $y \nless x$;
* $x \lt y$ iff $y \nleq x$.

One often sees $x \lt y$ defined as $x \le y$ but $x \ne y$; this is equivalent, but doesn\'t show the duality explicitly.  Similarly, one often sees $x \leq y$ defined as $x \lt y$ or $x = y$; this is not even equivalent constructively, although it is classically.

In [[classical mathematics]], the distinction between total orders and strict total orders is merely a terminological technicality, which is not always observed; more precisely, there is a [[natural isomorphism|natural bijection]] between the set of total orders on a given set $S$ and the set of strict total orders on $S$, and one distinguishes them by their notation.  In [[constructive mathematics]], however, they are irreducibly different.

For more, including why strict total orders are more often useful in constructive mathematics, see [[strict total order]].

## Classifying topos

There is a [[classifying topos]] for [[inhabited set|inhabited]] linear orders. It is given by the [[category]] of [[cosimplicial sets]], hence by the [[presheaf topos]] over the [[opposite category]] of the [[simplicial category]]. 

For more see at _[[classifying topos]]_ the section _[For (inhabited) linear orders](http://ncatlab.org/nlab/show/classifying+topos#ForLinearOrders)_.

## Related concepts

* [[order topology]]

[[!redirects total order]]
[[!redirects total orders]]
[[!redirects toset]]
[[!redirects tosets]]
[[!redirects totally ordered set]]
[[!redirects totally ordered sets]]
[[!redirects total ordering]]
[[!redirects totally ordered]]

[[!redirects linear order]]
[[!redirects linear orders]]
[[!redirects linear ordering]]
[[!redirects linear orderings]]
[[!redirects linearly ordered]]
[[!redirects linearly ordered set]]
[[!redirects linearly ordered sets]]
[[!redirects loset]]
[[!redirects losets]]

[[!redirects ordering]]
[[!redirects orderings]]
