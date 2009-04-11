# Idea #

A _well order_ on a set $S$ is a [[relation]] $\prec$ that allows one to interpret $S$ as an [[ordinal number]] $\alpha$ and $\prec$ as the relation $\lt$ on the ordinal numbers less than $\alpha$.  In particular, one can do [[induction]] on $S$ over $\prec$ (although the more general [[well-founded relation]]s also allow this).

The [[well-ordering theorem]] states precisely that every set may be equipped with a well order.  Assuming the principle of [[excluded middle]], this theorem is equivalent to the [[axiom of choice]].

# Definition #

A binary [[relation]] $\prec$ on a [[set]] $S$ is a __well order__ if it is a [[well-founded relation|well-founded]] [[linear order]].  Equivalently, a well order is a [[transitive relation|transitive]], [[extensional relation|extensional]], well-founded relation.

Sometimes one wants $S$ to have a [[total order]] $\preceq$ instead of a linear order $\prec$.  In classical mathematics, at least, the distinction is a technicality: $x \preceq y$ if $x \prec y$ or $x = y$, and $x \prec y$ if $x \preceq y$ but $x \ne y$.  (In [[constructive mathematics]], $\preceq$ is not sufficient to reconstruct $\prec$.)

With this in mind, we may equivalently define a well order on $S$ to be a total order $\preceq$ such that every [[inhabited set|inhabited subset]] has a lowest element.  That is, for all $U \subset S$ with $U \neq \emptyset$ there exists $\bottom_U \in U$ such that for all $u \in U$ we have $\bottom_U \leq u$.  (Again, in constructive mathematics, this will not work; indeed, it\'s not possible to prove constructively the existence of any well order, in this sense, on any set with at least $2$ elements.)

A set equipped with a well order is called a __well-ordered set__, or (following '[[partial order|poset]]') a __woset__.  Actually, the term 'well-ordered' came first; 'well order' is a back formation.  Accordingly, many writers spell this noun as 'well-order', the cringes of grammarians notwithstanding.

+--{: .query}
I for one would be happy to move this to [[well order]].  Indeed, when I began rewriting it, I naturally used that spelling until I got to the paragraph above.  ---Toby

[[Mike Shulman|Mike]]: Well, I'm not an expert at grammar, so I don't know what the difference is between "well-order" and "well order."  Neither sounds really correct to me, however, since "well" is an _adverb_ but is being used as an adjective modifying "order."

_Toby_:  Actually, 'well' (like 'ill') can be either an adjective or an adverb.  If it were an adverb here, then we wouldn\'t need the hyphen even in 'well ordered', and the noun would be 'good order'.  Note that an 'ordered set' is a set equipped with an order as well as a set that\'s been ordered (and in fact the verb 'order' is derived from the noun); so is a 'well ordered set' a set that\'s been ordered well, or is a 'well-ordered set' a set equipped with a well order?  (Although by this logic, there should be no hyphen in 'well-founded', since 'found' is definitely a verb there and not a noun.)
=--

# Examples #

* Any [[finite set|finite]] [[total order|totally ordered set]] $\{x_1 \lt \cdots \lt x_n\}$ is well-ordered.

* The set of [[natural number]]s is well-orderd under the usual order $\lt$.

* More generally, any set of [[ordinal number]]s (or even the proper class of all ordinal numbers) is well-ordered under the usual order $\lt$.

* The [[cardinal number]]s of well-orderable sets are themselves well-ordered.  So by the well-ordering theorem, the class of all cardinal numbers is well-ordered.

# Successor #

A well-ordered set $S$ comes equipped with a **[[successor]]** map
$
  succ : S \to S  
  \,.
$
this sends $a \in S$ to the lowest element of the subset $S_a := \{ s \in S, a \prec s\}$.
(A slightly more involved argument proves that this map is well-defined constructively.)

# Interpretation as an ordinal number #

Any well-ordered set $S$ defines an [[ordinal number]] $\alpha$ and an order isomorphism $r$ between $S$ and the set of ordinal numbers less than $\alpha$; as such, $S$ may be identified (up to isomorphism of wosets) with the von Neumann ordinal $\alpha$.  The idea is that the minimal element $\bot$ of $S$ itself (if any) is mapped to the ordinal number $0$, the minimal element of $S \setminus \{\bot\}$ (if any) is mapped to $1$, and so on; after which the next element of $S$ (if any) is mapped to $\omega$; and so on; and so on.

This may be defined immediately (and constructively) as a recursively defined function from $S$ to the class of all ordinal numbers:
$$ r(x) = \bigcup_{t \prec x} r(t)+ ;$$
the validity of this sort of recursive definition is precisely what the well-foundedness of $\prec$ allows.  Here, $\beta+$ is the [[successor]] of the ordinal number $\beta$, and $\bigcup$ is the union operation on ordinal numbers (literally the [[union]] of von Neumann ordinals).

Since $S$ is a set, the image of $r$ in the class of all ordinals is also a set, and one can now prove that $r$ is an order isomorphism between $S$ and the set of ordinals less than the next ordinal, $\alpha$.