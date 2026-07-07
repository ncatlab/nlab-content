
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

A *total order* or *linear order* or *chain order* on a set is a way of ordering its elements to say that some elements precede others, with the understanding that any two elements can be compared one way or the other.

## Definitions

### With a relation

Given a [[set]] $S$, a **total order** or **linear order** or **chain order** on $S$ is a (binary) [[relation]] $\leq$ with the following properties:

* [[reflexive relation|reflexivity]]: for any element $x$ of $S$, $x \leq x$;
* [[transitive relation|transitivity]]: whenever $x \leq y \leq z$, then $x \leq z$;
* [[antisymmetric relation|antisymmetry]]: whenever $x \leq y \leq x$, then $x = y$;
* [[total relation|totality]]: for any $x$ and $y$ in $S$, $x \leq y$ or $y \leq x$.

A **totally ordered set** or **toset** or **linearly ordered set** or **loset** is a set equipped with a total order/linear order.

### With a semigroup operation

A **totally ordered set** or **toset** or **linearly ordered set** or **loset** is a set $S$ equipped with a [[commutative semigroup|commutative]] and [[idempotent]] [[semigroup]] $\min:S \times S \to S$ such that for all $a \in S$ and $b \in S$, $\min(a, b) = a$ or $\min(a, b) = b$. 

## Relation to simplices

The category of finite nonempty totally ordered sets and order-preserving maps is called $\Delta$, the [[simplex category]]. 

The category of *all* finite totally ordered sets and order-preserving maps is called $\Delta_a$, the **augmented** simplex category.

## Relation to pseudolattices

Due to the totality of the order relation $\leq$, every pair of elements $a$ and $b$ has a [[join]] and [[meet]], such that $a \wedge b = a$ and $a \vee b = b$, or $a \wedge b = b$ and $a \vee b = a$. This means that meets distribute over joins and joins distribute over meets, and additionally that both operations are [[associative]], [[commutative]], and [[idempotent]], and so every total order is a [[pseudolattice]], and every bounded total order is a [[lattice]]. 

## Relation to cotransitive partial orders

\begin{definition}
A **cotransitive partial order** or **weakly linear partial order** on a set $S$ is a [[partial order]] $\leq$ which satisfies [[cotransitivity]]/[[weak linearity]]: 

* for all $x \in S$, $y \in S$, and $z \in S$, $x \leq z$ implies that $x \leq y$ or $y \leq z$. 

\end{definition}

\begin{theorem}
Cotransitive partial orders are total orders.
\end{theorem}

\begin{proof}
Cotransitivity of $\leq$ says that for all $x \in S$ and $y \in S$, $x \leq x$ implies that $x \leq y$ or $y \leq x$, and reflexivity says that for all $x$, $x \leq x$ is always true. This implies that for all $x$ and $y$, $x \leq y$ or $y \leq x$ is always true, which is precisely the condition of totality, hence that cotransitive partial order are total orders.
\end{proof}

\begin{theorem}
Total orders are cotransitive partial orders.
\end{theorem}

\begin{proof}
Suppose that $x \leq y$ or $y \leq x$. Then for all $x \leq z$ and elements $y$, by totality, we can decide whether 

1. $y \leq x$, thus $y \leq z$ by transitivity. 
1. $x \leq y$ and $y \leq z$
1. $z \leq y$, thus $x \leq y$ by transitivity. 

In the first two cases, we have $y \leq z$, and in the second two cases, we have $x \leq y$. Thus, in all cases, we have $x \leq y$ or $y \leq z$, and total orders are cotransitive. 
\end{proof}

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

* [[total preorder]]

* [[linear order]]

* [[bounded total order]]

## References

Total orders are defined in the section of chapter 3 titled "Chains":

* [[Eric Schechter]], *[[Handbook of Analysis and its Foundations]]*, Academic Press (1996), (ISBN 0-12-622760-8, [doi:10.1016/B978-0-12-622760-4.X5000-6](https://doi.org/10.1016/B978-0-12-622760-4.X5000-6))

[[!redirects total order]]
[[!redirects total orders]]
[[!redirects toset]]
[[!redirects tosets]]
[[!redirects totally ordered set]]
[[!redirects totally ordered sets]]
[[!redirects total ordering]]
[[!redirects totally ordered]]

[[!redirects chain order]]
[[!redirects chain orders]]
[[!redirects chain ordering]]
[[!redirects chain orderings]]

[[!redirects ordering]]
[[!redirects orderings]]

[[!redirects cotransitive partial order]]
[[!redirects cotransitive partial orders]]
[[!redirects cotransitive partial ordering]]
[[!redirects cotransitive partial orderings]]

[[!redirects cotransitively partial ordered]]
[[!redirects cotransitively partial ordered set]]
[[!redirects cotransitively partial ordered sets]]

[[!redirects weakly linear partial order]]
[[!redirects weakly linear partial orders]]
[[!redirects weakly linear partial ordering]]
[[!redirects weakly linear partial orderings]]

[[!redirects weakly linearly partial ordered]]
[[!redirects weakly linearly partial ordered set]]
[[!redirects weakly linearly partial ordered sets]]
