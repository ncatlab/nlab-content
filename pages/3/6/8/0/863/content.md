
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

A *pseudo-order* or *strict total order* or *strict linear order* is the irreflexive version of a [[total order]]. This is sometimes called *linear order*, but [[linear order]] is also used to refer to the non-strict [[total order]]. 

A **pseudo-ordered set** or **strictly totally ordered set** is a [[set]] equipped with a pseudo-order.

In [[classical mathematics]], the distinction between strict total orders and total orders is merely a terminological technicality, which is not always observed; more precisely, there is a [[natural isomorphism|natural bijection]] between the set of total orders on a given set $S$ and the set of strict total orders on $S$, and one distinguishes them by the notation $\lt$ (for the strict total orders) and $\leq$ (for the total order).  In [[constructive mathematics]], however, they are irreducibly different.

## Definitions

A **pseudo-order** or **strict total order** on a set $S$ is a (binary) [[relation]] $\lt$ with the following properties:

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

In classical mathematics, there are even more options.  Now weak linearity can be dropped, as it follows from transitivity and connectedness.  Also, one often combines irreflexivity, asymmetry, and connectedness into a single axiom:

* [[trichotomy]]: exactly one of $x \lt y$, $y \lt x$, $x = y$ is true.

Thus the most common definition uses only trichotomy and transitivity.

One can also interpret connectedness not as an axiom but as a definition of [[equality]], getting a pseudo-order on a [[quotient set]] of $S$.  In other words, if $\lt$ is an asymmetric and weakly linear relation on $S$, and we define $x \equiv y$ to mean that neither $x \lt y$ nor $y \lt x$, then $\equiv$ is an equivalence relation and $\lt$ induces a pseudo-order on $S/{\equiv}$.

## Examples

Classically, any [[total order]] defines an example of a pseudo-order (as explained below), and this also holds constructively in [[discrete mathematics]].  Since most pseudo-orders in these cases are usually described in terms of their total orders, the focus here is on [[constructive analysis]].  (The first item, however, is an exception.)

* A [[lexicographic order]], even in a classical or discrete context, is more easily described as a pseudo-order than as a total order.
* The big example in analysis is the field of [[real numbers]].  Both the Dedekind reals and the Cauchy reals (even if [[weak countable choice]] fails so these are not equivalent) have a pseudo-order $\lt$ that extends the (decidable) pseudo-order on the rational numbers.  Since the corresponding partial order $\leq$ cannot be proved total (and in some classically invalid versions of constructive mathematics can even be proved not total), $\lt$ is more directly useful than $\leq$ in constructive analysis.  In any case, $\lt$ is more fundamental, since $\leq$ can be defined in terms of $\lt$ but not the other way around. (The Mac Neille real numbers have both $\lt$ and $\leq$; however, in this case, neither is necessarily a pseudo-order or a total order, nor can they necessarily be defined in terms of one another.)
* [[Baire space of irrational numbers|Baire space]] and [[Cantor space]], being representable as subspaces of the real line, of course are strictly totally ordered.  It\'s also interesting to see them as coming from the (decidable) pseudo-orders on $\mathbf{N}$ and $\mathbf{2}$, which they are $\mathbf{N}$-fold products of.

## Properties

### Relation to total orders

Using excluded middle, one can move between strict linear orders and [[total order]]s using [[negation]]; that is, the negation of a strict linear order is a total order and vice versa.  Actually one usually swaps the order too, as follows:

* $x \lt y$ iff $y \nleq x$;
* $x \leq y$ iff $y \nless x$.

To prove this, it\'s enough to see that the properties of a strict linear order are [[de Morgan duality|dual]] to the properties of a total order, as follows:

| strict linear order  |   | total order    |
| -------------------- | - | -------------- |
| irreflexivity        |   | reflexivity    |
| asymmetry            |   | totality       |
| transitivity         |   | weak linearity |
| weak linearity       |   | transitivity   |
| connectedness        |   | antisymmetry   |

Constructively, these are still the default definitions to use; that is, if one is given a strict linear order or a total order and wants to interpret the other symbol, then one does so using these definitions.  However, the result will not necessarily be a total order or a strict linear order.  To be specific, if one starts with a strict linear order $\lt$ and defines $\leq$ as above, then totality does not follow; and if one starts with a total order $\leq$ and defines $\lt$ as above, then weak linearity does not follow.  Nevertheless, at least $\leq$ will be a [[partial order]], and least $\lt$ will be a [[strict preorder]].  Furthermore, the duality between the axioms is still there, even though negation no longer mediates between them; although weak linearity need not hold for a total order constructively, the duality is preserved if one defines strict linear orders without using transitivity.

One often sees $x \lt y$ defined as $x \le y$ but $x \ne y$; this is equivalent, but doesn\'t show the de Morgan duality explicitly.  Similarly, one often sees $x \leq y$ defined as $x \lt y$ or $x = y$; this is not even equivalent constructively, although it is classically.

Keep in mind, however, that the only use of [[excluded middle]] in the classical theory is the assumption that $x = y$, $x \lt y$, and $x \leq y$ are always either true or false.  There is therefore a perfect correspondence between [[decidable subset|decidable]] strict linear orders and decidable total orders on sets with [[decidable equality]].

## See also

* [[total order]]
* [[strict weak order]]
* [[strict preorder]]
* [[trichotomous relation]]

## References

* Wikipedia, [https://en.wikipedia.org/wiki/Pseudo-order](https://en.wikipedia.org/wiki/Pseudo-order)

* Heyting, Arend (1966). Intuitionism: an introduction (2nd ed.). Amsterdam: North-Holland Pub. Co. p. 106. ISBN:978-0-444-53406-4

[[!redirects pseudo-order]]
[[!redirects pseudo-orders]]
[[!redirects pseudo-ordering]]
[[!redirects pseudo-orderings]]
[[!redirects pseudo-ordered]]
[[!redirects pseudo-ordered set]]
[[!redirects pseudo-ordered sets]]

[[!redirects strict linear order]]
[[!redirects strict linear orders]]
[[!redirects strict linear ordering]]
[[!redirects strict linear orderings]]
[[!redirects strictly linearly ordered]]
[[!redirects strictly linearly ordered set]]
[[!redirects strictly linearly ordered sets]]

[[!redirects strict total order]]
[[!redirects strict total orders]]
[[!redirects strict total ordering]]
[[!redirects strict total orderings]]
[[!redirects strictly totally ordered]]
[[!redirects strictly totally ordered set]]
[[!redirects strictly totally ordered sets]]