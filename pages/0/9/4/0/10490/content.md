
# MacNeille real numbers
* table of contents
{: toc}

## Idea

The MacNeille real numbers are a version of [[real numbers]] defined by forming the [[MacNeille completion]] of the [[rational numbers]], and then perhaps excluding the top and bottom element ($\pm\infty$).  In [[classical mathematics]], this produces the ordinary [[real numbers]] (and if we include $\pm\infty$ it produces the [[extended real numbers]]).  However, in [[constructive mathematics]], it yields something different (and less well behaved); it is not a constructive theorem that every bounded MacNeille number is located (hence a real number in the usual sense of constructive mathematics).


## Definition

Let $\mathbb{Q}$ be the [[poset]] of [[rational numbers]] with its usual [[Archimedean order]].

There are two obvious ways to define the MacNeille real numbers from $\mathbb{Q}$, one based on closed [[Dedekind cut|cuts]] (which matches the general theory of [[MacNeille completions]]) and one based on open cuts (which is compatible with other types of real numbers).  Fortunately, they are equivalent.

Outside of these definitions themselves, we will adopt the open definition, since it relates better to other kinds of real numbers.


### With closed sets

A pair $(L,U)$ of [[subsets]] of $\mathbb{Q}$ is called a __closed Dedekind--MacNeille cut__ in $\mathbb{Q}$ if:

* $U$ is the set of [[upper bounds]] of $L$: that is, $s \in U$ iff for all $r \in L$, $s \geq r$; and
* $L$ is the set of [[lower bounds]] of $U$: that is, $r \in L$ iff for all $s \in U$, $r \leq s$.

Given two such cuts, define $(L_1, U_1) \leq (L_2, U_2)$ to mean:

* $L_1 \subseteq L_2$; and
* $U_1 \supseteq U_2$.

(Actually, either of these assertions alone implies the other.)

Then the set of such cuts becomes a [[poset]], in fact a [[complete lattice]], called the set of **extended MacNeille real numbers**.  The **MacNeille real numbers** are the sub-poset consisting of the pairs $(L,U)$ such that $L$ and $U$ are both [[inhabited set|inhabited]].


### With open sets

A pair $(L,U)$ of [[subsets]] of $\mathbb{Q}$ is called an __open Dedekind--MacNeille cut__ in $\mathbb{Q}$ if:

* $L$ is an extended [[lower real number]] and $U$ is an extended [[upper real number]].  That is, $L$ is an open down-set and $U$ is an open up-set.
* $U$ is the interior of the complement of $L$: that is, $s \in U$ iff there is an $r\lt s$ with $r\notin L$.
* $L$ is the interior of the complement of $U$: that is, $r \in L$ iff there is an $s\gt r$ with $s\notin U$.

Given two such cuts, define $(L_1, U_1) \leq (L_2, U_2)$ to mean:

* $L_1 \subseteq L_2$; and
* $U_1 \supseteq U_2$.

(Actually, either of these assertions alone implies the other.)

Then the set of such cuts becomes a [[poset]], in fact a [[complete lattice]], called the set of **extended MacNeille real numbers**.  The **MacNeille real numbers** are the sub-poset consisting of the pairs $(L,U)$ such that $L$ and $U$ are both [[inhabited set|inhabited]].


### Comparing definitions

The open and closed definitions above are equivalent, even in constructive mathematics.

In one direction, if $(L,U)$ is a closed extended MacNeille real number, define $L^o$ and $U^o$ to be the interiors of $L$ and $U$ respectively.  Then $L^o$ is an extended lower real and $U^o$ is an extended upper real.  If $s\in U^o$, then by definition there is a $t\lt s$ with $t\in U$.  Then if $r$ is such that $t\lt r \lt s$, we have $r\notin L$ (and hence $r\notin L^o$), since if $r\in L$ we would have $r\le t$.  Conversely, if we have $r\lt s$ with $r\notin L^o$, then there does not exist a $t\gt r$ with $t\in L$, which is to say (since the rationals satisfy trichotomy) that for every $t\in L$ we have $t\le r$, i.e. $r\in U$, and hence $s\in U^o$.  The dual proof shows the corresponding axiom for $L^o$, so $(L^o,U^o)$ is an open extended MacNeille real number, which is bounded if $(L,U)$ is.

In the other direction, if $(L,U)$ is an open extended MacNeille real number, define $L^c$ to be the set of lower bounds of $U$, and $U^c$ to be the set of upper bounds of $L$.  (The notation is admittedly a little misleading, since $L^c$ is a function of $U$ rather than $L$.)  Then if $r\in L^c$ and $s\in U^c$ and $r\gt s$, then for a $t$ such that $s\lt t\lt r$ we would have $t\notin U$ and $t\notin L$, hence by the MacNeille condition $r\in L$ and $s\in U$, a contradiction.  Thus, if $r\in L^c$ and $s\in U^c$ then $r\le s$, so $L^c$ consists of lower bounds for $U^c$ and vice versa.  Conversely, if $r$ is a lower bound of $U^c$, then it is also a lower bound of $U$, and so $r\in L^c$.  Thus $(L^c,U^c)$ is a closed extended MacNeille real number, which is bounded if $(L,U)$ is.

To show that these operations are inverses, suppose first $(L,U)$ is a closed extended MacNeille real.  Then $(L^o)^c$ is the set of lower bounds of the interior of $U$.  Any lower bound of $U$ is of course a lower bound for its interior, so $L\subseteq (L^o)^c$.  On the other hand, if $r$ is a lower bound for $U^o$, to show $r\in L$ it suffices to show $r\le s$ for all $s\in U$.  But if $r\gt s$, then $r\in U^o$, a contradiction since $U^o$ is open.  Thus $L= (L^o)^c$, and dually $U = (U^o)^c$.

On the other side, suppose $(L,U)$ is an open extended MacNeille real.  Then $(L^c)^o$ is the interior of the set of lower bounds of $U$.  Since $L$ consists of lower bounds for $U$, and $L$ is open, we have $L \subseteq (L^c)^o$.  On the other hand, if $r\in (L^c)^o$ then there is an $s\in L^c$ with $r\lt s$.  Then for any $t$ with $r\lt t\lt s$ we have $t\notin U$ (since $s$ is a lower bound for $U$), hence by the MacNeille condition $r\in L$.  Thus $L= (L^o)^c$, and dually $U = (U^o)^c$.

On the rest of this page, we will adopt the open definition, since it relates better to other kinds of real numbers.


## Properties

### Relation to other kinds of real numbers

Any (extended) [[located real number]] is an (extended) MacNeille real number.  The locatedness condition says that if $r\lt s$ then $r\in L$ or $s\in U$, which certainly implies that $(r\notin L)\Rightarrow (s\in U)$ and $(s\notin U)\Rightarrow (r\in L)$.  This gives an order-embedding.

Similarly, if $(L,U)$ is an (extended) MacNeille real number, then by definition $L$ is an (extended) [[lower real number]] and $U$ is an (extended) [[upper real number]].  Since $L$ and $U$ in a MacNeille real are recoverable from each other, this gives two order-embeddings.

If we define an **interval** to be a pair $(L,U)$ where $L$ is an extended lower real, $U$ is an extended upper real, and $L\cap U = \emptyset$, then we can embed both lower reals and upper reals into the poset of intervals by taking the interior of the complement as the other half.  That is, we map $L$ to $(L,int(\neg L))$ and $U$ to $(int(\neg U),U)$ --- two kinds of "singleton" intervals.  These are both order-embeddings, and in fact the lower reals are a [[coreflective subcategory|coreflective]] sub-poset and the upper reals are a [[reflective subcategory|reflective]] sub-poset.  Thus we have an [[adjunction]] between extended lower reals and extended upper reals, and the extended MacNeille reals are the jointly fixed sub-poset.  They are also the set-theoretic [[intersection]] of the lower and upper reals inside the intervals.


### Completeness

Since the extended MacNeille reals are a reflective sub-poset of the extended lower reals and a coreflective sub-poset of the extended upper reals, they are closed in the former under [[infima]] and in the latter under [[suprema]].  In particular, they are a complete lattice.  Note, though, that neither infima nor suprema are constructed as set-theoretic unions (unlike infima of upper reals and suprema of lower reals), which makes them less useful for purposes of constructive analysis.  (On the other hand, the extended located real numbers are not, constructively, a complete lattice at all.)


### Strict ordering

Recall that the MacNeille reals are a poset in which $(L_1, U_1) \leq (L_2, U_2)$ iff $L_1 \subseteq L_2$ iff $U_1 \supseteq U_2$.  This relation $\leq$ may be called the _weak ordering_ on MacNeille reals.

There is also a _strict (or strong) ordering_ $\lt$ defined by

*  $(L_1, U_1) \lt (L_2, U_2)$ iff $U_1$ meets $L_2$ (meaning that the [[intersection]] $U_1 \cap L_2$ is [[inhabited subset|inhabited]]).

That is, $x \lt y$ iff for some rational number $q$, $x \lt q \lt y$.

This restricts to the usual strict order $\lt$ on Dedekind reals.  We also have for any rational number $q$ that $x \lt q$ by this new strict order iff $x \lt q$ in the previously known sense (that $q$ belongs to the upper set of $x$), and similarly for $x \gt q$.

For Dedekind reals, the strict ordering is often taken to be the more basic concept, as the weak ordering can be derived from it ($\leq$ is the [[negation]] of $\gt$).  However, this is not so for the MacNeille reals, and the two orderings (weak and strict) exist separately.

They are not entirely unrelated, however; we do have $x \lt z$ whenever $x \lt y \leq z$ or $x \leq y \lt z$.  Also, while neither of $\leq$ and $\gt$ is the negation of the other, they are mutually exclusive, and it is impossible for both to be false.  As such, the pair of relations $({\leq},{\gt})$ makes the MacNeille real numbers into a tight interpretation of the classical theory of [[total orders]] in the [[antithesis interpretation]].


## References

* Section D4.7 of [[Sketches of an Elephant]]

* In [[Anne Troelstra|Troelstra]] and [[Dirk van Dalen|van Dalen]], *[[Constructivism in Mathematics]]*, section 5.5, the extended MacNeille real numbers are called the "extended real numbers" (and the MacNeille real numbers themselves are called the "bounded extended real numbers").


[[!redirects MacNeille real number]]
[[!redirects MacNeille real numbers]]
[[!redirects MacNeille real]]
[[!redirects MacNeille reals]]
[[!redirects MacNeille number]]
[[!redirects MacNeille numbers]]
