## Idea ##

A _well-order_ on a set $S$ is a [[relation]] $\prec$ that allows one to interpret $S$ as an [[ordinal number]] $\alpha$ and $\prec$ as the relation $\lt$ on the ordinal numbers less than $\alpha$.  In particular, one can do [[induction]] on $S$ over $\prec$ (although the more general [[well-founded relations]] also allow this).

The [[well-ordering theorem]] states precisely that every set may be equipped with a well-order.  This theorem follows from the [[axiom of choice]], and is equivalent to it in the presence of [[excluded middle]].

## Definition ##

A binary [[relation]] $\prec$ on a [[set]] $S$ is a __well-order__ if it is a [[well-founded relation|well-founded]] [[linear order]].  Equivalently, a well-order is a [[transitive relation|transitive]], [[extensional relation|extensional]], well-founded relation.  A set equipped with a well-order is called a __well-ordered set__, or (following '[[partial order|poset]]') a __woset__.  Actually, the term 'well-ordered' came first; 'well-order' is a back formation, which explains the strange grammar.

Sometimes one wants $S$ to have a [[total order]] $\preceq$ instead of a linear order $\prec$ (that is, a reflexive rather than an irreflexive one).  In classical mathematics, at least, the distinction is a technicality: $x \preceq y$ if $y \nprec x$, and $x \prec y$ if $y \npreceq x$.  (In [[constructive mathematics]], $\preceq$ is not sufficient to reconstruct $\prec$, and we really want $\prec$.)

Using either $\prec$ or $\preceq$, we may equivalently define a well order on $S$ to be a linear or total order such that every [[inhabited set|inhabited subset]] has a lowest element.  That is, for all $U \subset S$ with $U \neq \emptyset$ there exists $\bottom_U \in U$ such that no $u \in U$ satisfies $u \prec \bottom_U$ (equivalently, every $u$ satisfies $\bottom_U \leq u$).  This is probably the definition most often found in textbooks.

Note that in [[constructive mathematics]], $\prec$ cannot necessarily be reconstructed from $\preceq$ (which is not necessarily a total order either), and we really want $\prec$.  Also, not every well-ordered set satisfies the property that every inhabited subset has a least element; if it does we call it **classically well-ordered**.  Any classically well-ordered set is a [[choice object|choice set]], and so if any set with at least $2$ elements has a classical well-order, [[excluded middle]] follows.

## Examples ##

* Any [[finite set|finite]] [[linearly ordered set]] $\{x_1 \lt \cdots \lt x_n\}$ is well-ordered.

* The set of [[natural numbers]] is well-ordered under the usual order $\lt$.

* More generally, any set of [[ordinal numbers]] (or even the proper class of all ordinal numbers) is well-ordered under the usual order $\lt$.

* The [[cardinal numbers]] of well-orderable sets are themselves well-ordered.  So by the well-ordering theorem, the class of all cardinal numbers is well-ordered.

## Interpretation as an ordinal number ##

Any well-ordered set $S$ defines an [[ordinal number]] $\alpha$ and an order isomorphism $r$ between $S$ and the set of ordinal numbers less than $\alpha$; as such, $S$ may be identified (up to isomorphism of wosets) with the von Neumann ordinal $\alpha$.  The idea is that the minimal element $\bot$ of $S$ itself (if any) is mapped to the ordinal number $0$, the minimal element of $S \setminus \{\bot\}$ (if any) is mapped to $1$, and so on; after which the next element of $S$ (if any) is mapped to $\omega$, and so on; and so on.

This may be defined immediately (and constructively) as a recursively defined function from $S$ to the class of all ordinal numbers:
$$ r(x) = \sup_{t \prec x} r(t)^+ ;$$
the validity of this sort of recursive definition is precisely what the well-foundedness of $\prec$ allows.  Here, $\beta^+$ is the [[successor]] of the ordinal number $\beta$, and $\sup$ is the [[supremum]] operation on ordinal numbers (which is the [[union]] of von Neumann ordinals).

Since $S$ is a set, the image of $r$ in the class of all ordinals is also a set, and one can now prove that $r$ is an order isomorphism between $S$ and the set of ordinals less than the next ordinal, $\alpha$.

## Simulations ##

Given two well-ordered sets $S$ and $T$, a [[function]] $f: S \to T$ is a __simulation__ of $S$ in $T$ if
*  $f(x) \prec f(y)$ whenever $x \prec y$ and
*  given $t \prec f(x)$, there exists $y \prec x$ with $t = f(y)$.

Note that any simulation of $S$ in $T$ must be unique.  Thus, well-ordered sets and simulations form a category that is in fact a (large) [[poset]].

## Successor ##

A well-ordered set $S$ comes equipped with a **[[successor]]** map
$
  succ : S \to S  
  \,.
$
this sends $a \in S$ to the lowest element of the subset $S_a := \{ s \in S, a \prec s\}$.

+--{: .query}
This need not exist; in particular, $S_a$ may be empty.  What do we really want to say here?  (We could talk about the successor *of* a well-ordered set.)  ---Toby

[[Mike Shulman|Mike]]: Yeah, or we could say that successor is a partial function.  One definition of a limit ordinal is one on which successor is totally defined.
=--


[[!redirects well order]]
[[!redirects well ordered]]
[[!redirects well-ordered]]
[[!redirects well ordered set]]
[[!redirects well ordering]]
[[!redirects well-ordered set]]
[[!redirects well-ordering]]
[[!redirects woset]]
[[!redirects well-orders]]
[[!redirects well orders]]
[[!redirects well ordered sets]]
[[!redirects well orderings]]
[[!redirects well-ordered sets]]
[[!redirects well-orderings]]
[[!redirects wosets]]