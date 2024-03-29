
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A _well-order_ on a set $S$ is a [[relation]] $\prec$ that allows one to interpret $S$ as an [[ordinal number]] $\alpha$ and $\prec$ as the relation $\lt$ on the ordinal numbers less than $\alpha$.  In particular, one can do [[induction]] on $S$ over $\prec$ (although the more general [[well-founded relations]] also allow this).

The _[[well-ordering theorem]]_ states precisely that every set may be equipped with a well-order.  This theorem follows from the [[axiom of choice]], and is equivalent to it in the presence of [[excluded middle]].


## Definition

A [[binary relation]] $\prec$ on a [[set]] $S$ is a __well-order__ if it is [[transitive relation|transitive]], [[extensional relation|extensional]], and [[well-founded relation|well-founded]].  A set equipped with a well-order is called a __well-ordered set__, or (following '[[partial order|poset]]') a __woset__.  Actually, the term 'well-ordered' came first; 'well-order' is a back formation, which explains the strange grammar.

Other definitions of a well-order may be found in the literature; they are equivalent given [[excluded middle]], but the definition above seems to be the most powerful in [[constructive mathematics]].  Specifically:

*  a well-order is precisely a [[well-founded relation|well-founded]] [[pseudo-order]] $\prec$;
*  a well-order is precisely a [[total order]] $\preceq$ whose strict version $\prec$ (defined by $x \prec y$ iff $x \preceq y$ and $x \ne y$) is [[well-founded relation|well-founded]];
*  (assuming also [[dependent choice]]) a well-order is precisely a pseudo-order $\prec$ with no infinite descending sequence $\cdots \prec x_2 \prec x_1 \prec x_0$;
*  (assuming also [[dependent choice]]) a well-order is precisely a total order $\preceq$ such that every infinite descending sequence $\cdots \preceq x_2 \preceq x_1 \preceq x_0$ has $x_i = x_{i^+}$ for some $i$ (and hence for infinitely many $i$);
*  a well-order on $S$ is precisely a [[pseudo-order]] $\prec$ with the property that every [[inhabited subset]] $U$ of $S$ has a least element (an element $\bot_U$ such that no $x \in U$ satisfies $x \prec \bot_U$;
*  a well-order on $S$ is precisely a [[total order]] $\preceq$ with the property that every [[inhabited subset]] $U$ of $S$ has a least element (an element $\bot_U$ such that every $x \in U$ satisfies $\bot_U \preceq x$.

The really interesting thing here is that every well-order is a pseudo-order; it is a constructive theorem that every pseudo-order is weakly extensional (and so extensional if well-founded) and transitive.  (For a [[weak counterexample]], take the set of [[truth values]] with $x \prec y$ iff $y$ is true and $x$ is false; this is a well-order that\'s a pseudo-order iff [[excluded middle]] holds.)  For the other equivalences, we\'re simply using well-known classical equivalents for well-foundedness and the classical correspondence between a pseudo-order $\prec$ and its [[reflexive closure]] $\preceq$.

For reference, a __classical well-order__ is any order satisfying the last definition (a total order that is classically well-founded).  A classically well-ordered set is a [[choice set]], and so if any set with at least $2$ [[denial inequality|unequal]] elements has a classical well-order, then [[excluded middle]] follows.  (But there are still interesting examples of classically well-ordered sets in constructive mathematics, such as the [[Higgs object|Higgs set]].)


### Well-orders are pseudo-orders 

As stated above, well-founded extensional transitive relations $\prec$ on a set $X$ are pseudo-orders, assuming [[classical logic]].

+-- {: .proof}
###### Proof

Order $X \times X$ [[lexicographic order|lexicographically]]: $(a, b) \prec (a', b')$ if either $a \prec a'$ in $X$ or $a = a'$ and $b \prec b$ in $X$. It is not hard to see that the lexicographic order is well-founded (and in fact a well-order, although we do not need this).  Now let $A \subset X \times X$ be the set of pairs $(x, y)$ of non-equal elements $x$ and $y$ that are incomparable in $X$, and suppose $A$ is inhabited. Then $A$ has a minimal element $(a, b)$ (using excluded middle). Then, for every $x \prec b$, either $a \preceq x$ or $x \preceq a$. If the former holds for some $x$, then $a \prec b$ follows by transitivity, contradiction. Hence $x \prec a$ for every $x \prec b$. Now let $a'$ be minimal such that $x \prec a' \preceq a$ for every $x \prec b$.

Claim: 
$$ \{x: x \prec a'\} = \{x: x \prec b\}. $$ 
We know already the right side is contained in the left. In the other direction, suppose $x \prec a'$. Since $x \prec a$ and $(a, b)$ was chosen minimal in the lexicographic order, $x$ and $b$ are comparable. If $b \preceq x \prec a'$, this contradicts minimality of $a'$. Thus $x \prec b$, i.e., the left side is contained in the right. 

But now, by extensionality, $a' = b$, whence $b \preceq a$, contradiction. Therefore $A$ was empty, so that $X$ is [[connected relation|connected]] and therefore (being already transitive and irreflexive and using excluded middle again) a pseudo-order.
=-- 


## Examples

* Any [[finite set|finite]] [[pseudo-ordered set]] $\{x_1 \lt \cdots \lt x_n\}$ is well-ordered.

* The set of [[natural numbers]] is well-ordered under the usual order $\lt$.

* More generally, any set of [[ordinal numbers]] (or even the [[proper class]] of all ordinal numbers) is well-ordered under the usual order $\lt$ (which, constructively, may not be a pseudo-order).

* The [[cardinal numbers]] of well-orderable sets (the well-orderable cardinals), forming a [[retract]] of the ordinals, are well-ordered.  So by the well-ordering theorem, the class of *all* cardinal numbers is well-ordered.

* A special case of the well-ordering theorem is the existence of a well-order on the set of [[real numbers]]; this is enough for many applications of the [[axiom of choice]] to [[analysis]].


## Interpretation as an ordinal number

Any well-ordered set $S$ defines an [[ordinal number]] $\alpha$ and an order isomorphism $r$ between $S$ and the set of ordinal numbers less than $\alpha$; as such, $S$ may be identified (up to isomorphism of wosets) with the von Neumann ordinal $\alpha$.  The idea is that the minimal element $\bot$ of $S$ itself (if any) is mapped to the ordinal number $0$, the minimal element of $S \setminus \{\bot\}$ (if any) is mapped to $1$, and so on; after which the next element of $S$ (if any) is mapped to $\omega$, and so on; and so on.

This may be defined immediately (and constructively) as a recursively defined function from $S$ to the class of all ordinal numbers:
$$ r(x) = \sup_{t \prec x} r(t)^+ ;$$
the validity of this sort of recursive definition is precisely what the well-foundedness of $\prec$ allows.  Here, $\beta^+$ is the [[successor]] of the ordinal number $\beta$, and $\sup$ is the [[supremum]] operation on ordinal numbers (which is the [[union]] of von Neumann ordinals).

Since $S$ is a set, the image of $r$ in the class of all ordinals is also a set (by the [[axiom of replacement]]), and one can now prove that $r$ is an order isomorphism between $S$ and the set of ordinals less than the next ordinal, $\alpha \coloneqq (\im r)^+$.


## Simulations

Given two well-ordered sets $S$ and $T$, a [[function]] $f\colon S \to T$ is a __[[simulation]]__ of $S$ in $T$ if

*  $f(x) \prec f(y)$ whenever $x \prec y$ and
*  given $t \prec f(x)$, there exists $y \prec x$ with $t = f(y)$.

Note that any simulation of $S$ in $T$ must be unique.  Thus, well-ordered sets and simulations form a category that is in fact a (large) [[preorder]], whose reflection in the category of [[posets]] is in fact the poset of [[ordinal numbers]]. 


## Successor

A well-ordered set $S$ comes equipped with a **[[successor]]**, which is a [[partial function|partial map]] 
$
  succ\colon S \to S  
  \,
$
that sends $a \in S$ to the lowest element of the subset $S_a := \{ s \in S, a \prec s\}$, whenever this set is inhabited. 

+-- {: .num_defn} 
###### Definition 
A **limit** well-order is a well-order $S$ whose successor map is a [[total function]]. 
=-- 

Similarly, one may define a successor [[functor]] on the [[category]] of well-ordered sets, taking $S$ to the well-order obtained by freely adjoining a (new) top element to $S$. Since this category (which is [[thin category|thin]]) can be regarded as itself a well-ordered [[proper class]], this is a special case of the successor operation above.  (Hence the ordinal of all ordinals is a limit ordinal.)


## Related entries

* [[well-quasi-order]]
* [[marked extensional well-founded relation]]


[[!redirects well order]]
[[!redirects well orders]]
[[!redirects well-order]]
[[!redirects well-orders]]
[[!redirects well ordering]]
[[!redirects well orderings]]
[[!redirects well-ordering]]
[[!redirects well-orderings]]

[[!redirects well ordered]]
[[!redirects well-ordered]]
[[!redirects well ordered set]]
[[!redirects well ordered sets]]
[[!redirects well-ordered set]]
[[!redirects well-ordered sets]]
[[!redirects woset]]
[[!redirects wosets]]
