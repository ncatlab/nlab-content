
# DCPOs
* table of contents
{: toc}

## Idea

A DCPO, or directed-complete partial order, is a [[poset]] with all [[directed joins]].  Often a DCPO is required to have a [[bottom element]] $\bot$; then it is called a pointed DCPO or a CPO (but this term is ambiguous).

The [[morphisms]] between DCPOs preserve the directed joins; equivalently, they are [[Scott continuity|Scott-continuous]].  Morphisms between pointed DCPOs may or may not be required to preserve $\bot$, depending on the application.

In [[domain theory]], a DCPO $P$ is interpreted as a [[type]] (in a programming sense), and its elements are possible partial (in the sense of a [[partial function]]) results of a computation.  The bottom element (if there is one) indicates that no result has been obtained; if $x \leq y$ in $P$, then $x$ consists of part of the information in $y$.  A [[directed set|directed subset]] $D$ of $P$ indicates a collection of partial results which are mutually consistent, since for any two results $x, y \in D$, there is a partial result that subsumes them both.  The required join of $D$ is then a partial result encoding the same information as $D$ itself.


## Definitions

Recall that a [[poset]] $P$ consists of a collection of [[elements]] equipped with a [[binary relation]] $\leq$ such that $x \leq x$ always and $x \leq z$ whenever $x \leq y$ and $y \leq z$; we also consider $x$ and $y$ to be equal whenever $x \leq y$ and $y \leq x$.

Recall that a [[subset]] $D$ of $P$ is [[directed set|semidirected]] iff, whenever $x, y \in D$, there is some $z \in D$ such that $x \leq z$ and $y \leq z$.  Then $D$ is directed iff it is semidirected and [[inhabited subset|inhabited]].

Recall that an [[upper bound]] of a subset $D$ of $P$ is an element $x$ such that $y \leq x$ whenever $y \in D$, and a [[join]] of $D$ is an upper bound $x$ such that $x \leq y$ whenever $y$ is an upper bound of $D$.  The join of $D$, if one exists, is unique, and we write it $\bigvee D$ (or even put a little arrow on the right flank of the symbol when $D$ is directed).  A [[bottom element]] is a join of the [[empty subset]].

A __directed-complete partial order__ (__DCPO__) or __predomain__ is a poset in which every directed subset has a join.  A __pointed DCPO__ or __complete partial order__ (__CPO__) or __inductive partial order__ (__IPO__) or __semidirected-complete partial order__ or __domain__ or __lift algebra__ is a DCPO with a bottom element, equivalently a poset in which every semidirected subset has a join.


## The Scott topology

Every poset $P$ becomes a [[topological space]] under the [[Scott topology]], but this is particularly nice for DCPOs, so we review it.

A [[subset]] $A$ of a DCPO is Scott-[[open subset|open]] iff it's an [[upper subset]] and any directed subset of $P$ whose join belongs to $A$ must meet $A$; it\'s Scott-[[closed subset|closed]] iff it is a [[lower subset]] that is directed-complete in its own right.

The [[specialisation order]] of the Scott topology of a DCPO is its original order (but the Scott topology is finer than the [[specialisation topology]]).

## Related entries

* [[domain theory]]

* [[continuous lattice]]

[[!redirects dcpo]]
[[!redirects dcpo's]]
[[!redirects dcpos]]
[[!redirects DCPO]]
[[!redirects DCPO's]]
[[!redirects DCPOs]]
[[!redirects directed-complete partial order]]
[[!redirects directed-complete partial orders]]
[[!redirects directed complete partial order]]
[[!redirects directed complete partial orders]]

[[!redirects cpo]]
[[!redirects cpo's]]
[[!redirects cpos]]
[[!redirects CPO]]
[[!redirects CPO's]]
[[!redirects CPOs]]
[[!redirects complete partial order]]
[[!redirects complete partial orders]]
