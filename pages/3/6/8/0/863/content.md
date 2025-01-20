
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+-- {: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

A *pseudo-order* is the irreflexive version of a [[total order]]. This is sometimes called *linear order*, but [[linear order]] is also used to refer to [[strict total orders]] or to [[total orders]]; hence this is distinguished by the use of *weak linear order* instead. 

A **pseudo-ordered set** or **weakly linearly ordered set** is a [[set]] equipped with a pseudo-order.

In [[classical mathematics]], the distinction between pseudo-orders and total orders is merely a terminological technicality, which is not always observed; more precisely, there is a [[natural isomorphism|natural bijection]] between the set of total orders on a given set $S$ and the set of pseudo-orders on $S$, and one distinguishes them by the notation $\lt$ (for the pseudo-orders) and $\leq$ (for the total order).  In [[constructive mathematics]], however, they are irreducibly different.

## Definitions

A **pseudo-order** or **weak linear order** on a set $S$ is a (binary) [[relation]] $\lt$ with the following properties:

* [[irreflexive relation|irreflexivity]]: $x \nless x$;
* [[asymmetric relation|asymmetry]]: if $x \lt y$, then $y \nless x$;
* [[transitive relation|transitivity]]: if $x \lt y \lt z$, then $x \lt z$;
* [[weakly linear relation|weak linearity]]: if $x \lt z$, then $x \lt y$ or $y \lt z $;
* [[connected relation|connectedness]]: if $x \nless y$ and $y \nless x$, then $x = y$.

In classical mathematics, one may see these versions of asymmetry and connectedness:

* $x \nless y$ or $y \nless x$;
* $x \lt y$ or $y \lt x$ or $x = y$.

Using [[excluded middle]], these are equivalent to asymmetry and connectedness as given above, but they need not hold for all pseudo-orders in constructive mathematics.

Actually, these axioms are overkill; to begin with, irreflexivity is simply a special case of asymmetry and so can be dropped.  Additionally, one can either drop transitivity or drop asymmetry (which then requires keeping irreflexivity); they will still follow from the other axioms.  Dropping transitivity shows manifestly the duality (see below) between pseudo-orders and total orders (even in constructive mathematics), and dropping asymmetry shows that a pseudo-order is a weakly linear [[strict preorder]]. Keeping transitivity and irreflexivity (thus allowing one to drop asymmetry) shows manifestly that a pseudo-order is a special kind of [[strict preorder]].

Also, because the relation is [[asymmetric]], $x \nless y \vee y \nless x$ holds, which means that the [[inequality relation]] $x \# y$, defined by 
$$x \# y \coloneqq x \lt y \vee y \lt x$$
can equivalently be defined using the [[exclusive disjunction]]:
$$x \# y \coloneqq x \lt y \underline{\vee} y \lt x$$
Thus, the connectedness axiom can be expressed using exclusive disjunction:

* if not ($x \lt y$ [[xor]] $y \lt x$), then $x = y$.

In classical mathematics, there are even more options. Now one can prove that it is a [[strict total order]], since $x \lt y$ is a [[decidable proposition]]. As a result, the proposition $x \lt y \underline{\vee} y \lt x$ is also a [[decidable proposition]] due to asymmetry, which by connectedness implies ($x \lt y$ [[xor]] $y \lt x$) [[xor]] $x = y$. Also, weak linearity can be dropped, as it follows from transitivity and connectedness.

Thus the most common definition uses only trichotomy and transitivity.

One can also interpret connectedness not as an axiom but as a definition of [[equality]], getting a pseudo-order on a [[quotient set]] of $S$.  In other words, if $\lt$ is an asymmetric and weakly linear relation on $S$, and we define $x \equiv y$ to mean that neither $x \lt y$ nor $y \lt x$, then $\equiv$ is an equivalence relation and $\lt$ induces a pseudo-order on $S/{\equiv}$.

## Examples

Classically, any [[total order]] defines an example of a pseudo-order (as explained below), and this also holds constructively in [[discrete mathematics]].  Since most pseudo-orders in these cases are usually described in terms of their total orders, the focus here is on [[constructive analysis]].  (The first item, however, is an exception.)

* A [[lexicographic order]], even in a classical or discrete context, is more easily described as a pseudo-order than as a total order.
* Every [[strict linear order]] is a [[decidable relation|decidable]] [[pseudo-order]]. 
* The big example in analysis is the field of [[real numbers]].  Both the Dedekind reals and the Cauchy reals (even if [[weak countable choice]] fails so these are not equivalent) have a pseudo-order $\lt$ that extends the [[decidable pseudo-order]] on the rational numbers.  Since the corresponding partial order $\leq$ cannot be proved total (and in some classically invalid versions of constructive mathematics can even be proved not total), $\lt$ is more directly useful than $\leq$ in constructive analysis.  In any case, $\lt$ is more fundamental, since $\leq$ can be defined in terms of $\lt$ but not the other way around. (The Mac Neille real numbers have both $\lt$ and $\leq$; however, in this case, neither is necessarily a pseudo-order or a total order, nor can they necessarily be defined in terms of one another.)
* [[Baire space of irrational numbers|Baire space]] and [[Cantor space]], being representable as subspaces of the real line, of course are pseudo-ordered. It\'s also interesting to see them as coming from the (decidable) pseudo-orders on $\mathbf{N}$ and $\mathbf{2}$, which they are $\mathbf{N}$-fold products of.

## Properties

### Relation to total orders

Using excluded middle, one can move between pseudo-orders and [[total order]]s using [[negation]]; that is, the negation of a pseudo-order is a total order and vice versa.  Actually one usually swaps the order too, as follows:

* $x \lt y$ iff $y \nleq x$;
* $x \leq y$ iff $y \nless x$.

To prove this, it\'s enough to see that the properties of a pseudo-order are [[de Morgan duality|dual]] to the properties of a total order, as follows:

| pseudo-order   |   | total order    |
| -------------- | - | -------------- |
| irreflexivity  |   | reflexivity    |
| asymmetry      |   | totality       |
| transitivity   |   | weak linearity |
| weak linearity |   | transitivity   |
| connectedness  |   | antisymmetry   |

Constructively, these are still the default definitions to use; that is, if one is given a pseudo-order or a total order and wants to interpret the other symbol, then one does so using these definitions.  However, the result will not necessarily be a total order or a pseudo-order. To be specific, if one starts with a pseudo-order $\lt$ and defines $\leq$ as above, then totality does not follow; and if one starts with a total order $\leq$ and defines $\lt$ as above, then weak linearity does not follow.  Nevertheless, at least $\leq$ will be a [[partial order]], and least $\lt$ will be a [[strict preorder]].  Furthermore, the duality between the axioms is still there, even though negation no longer mediates between them; although weak linearity need not hold for a total order constructively, the duality is preserved if one defines pseudo-orders without using transitivity.

One often sees $x \lt y$ defined as $x \le y$ but $x \ne y$; this is equivalent, but doesn\'t show the de Morgan duality explicitly.  Similarly, one often sees $x \leq y$ defined as $x \lt y$ or $x = y$; this is not even equivalent constructively, although it is classically.

Keep in mind, however, that the only use of [[excluded middle]] in the classical theory is the assumption that $x \lt y$ is always either true or false, which implies that $x = y$ is [[stable relation|stable]] and [[decidable relation|decidable]] and [[denial inequality]] is an [[apartness relation]], and that $x \leq y$ is a [[total relation]] and its negation is [[weakly linear relation|weakly linear]]. There is therefore a perfect correspondence between [[decidable pseudo-orders]] on [[sets]] and total orders on [[classical sets]].

## See also

* [[total order]]
* [[strict weak order]]
* [[strict preorder]]
* [[trichotomous relation]]
* [[strict linear order]]

## References

* Wikipedia, [https://en.wikipedia.org/wiki/Pseudo-order](https://en.wikipedia.org/wiki/Pseudo-order)

* Heyting, Arend (1966). Intuitionism: an introduction (2nd ed.). Amsterdam: North-Holland Pub. Co. p. 106. ISBN:978-0-444-53406-4

The definition of weak linearity for an order relation is given on page 377 of 

* {#UFP13} [[Univalent Foundations Project]], Section 11.2 of: *[[Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013)

[[!redirects pseudo-order]]
[[!redirects pseudo-orders]]
[[!redirects pseudo-ordering]]
[[!redirects pseudo-orderings]]
[[!redirects pseudo-ordered]]
[[!redirects pseudo-ordered set]]
[[!redirects pseudo-ordered sets]]

[[!redirects weak linear order]]
[[!redirects weak linear orders]]
[[!redirects weak linear ordering]]
[[!redirects weak linear orderings]]
[[!redirects weakly linearly ordered]]
[[!redirects weakly linearly ordered set]]
[[!redirects weakly linearly ordered sets]]