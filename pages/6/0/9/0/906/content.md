
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea 

A [[topological space]] is _sequential_ if (in a certain sense) you can do topology in it using only [[sequences]] instead of more general [[nets]].

Sequential spaces are a kind of [[nice topological space]].


## Definition 

A __sequential topological space__ is a [[topological space]] $X$ such that a subset $A$ of $X$ is closed if (hence iff) it contains all the limit points of all [[sequences]] of points of $A$---or equivalently, such that $A$ is open if (hence iff) any sequence converging to a point of $A$ must eventually be in $A$.

Equivalently, a topological space is sequential iff it is a [[quotient space]] (in $Top$) of a [[metric space]].


## Examples 

* Every [[Frechet–Uryson space]] is a sequential space.

* Every topological space satisfying the [[first-countable space|first countability axiom]] is Frechet--Uryson, hence a sequential space.  In particular, this includes any [[metric space|metrizable]] space.

* Every [[quotient object|quotient]] of a sequential space is sequential.  In particular, every [[CW complex]] is also a sequential space.  (Conversely, every sequential space is a quotient of a metrizable space, giving the alternative definition).


## Properties

* The category of sequential spaces is a [[coreflective subcategory]] of the category of all topological spaces.

* The category of sequential spaces is a [[reflective subcategory]] of the category of [[subsequential spaces]], much as $Top$ itself is a reflective subcategory of the category of all [[pseudotopological spaces]]. 

* The category of sequential spaces is [[cartesian closed category|cartesian closed]]. See also [[convenient category of topological spaces]]. 


## In constructive mathematics

Everything above assumes [[excluded middle]] (and probably at least [[countable choice]]).  Without that, it\'s hard to prove the existence of any nontrivial sequential spaces.

For example, to prove that the [[real line]] is sequential as a topological space, we must find, given a set $A$ and a point $x$ such that every sequence converging to $x$ is eventually in $A$, a [[positive real number]] $\delta$ such that ${]x - \delta, x + \delta[} \subseteq A$, and it\'s not clear how to construct that number from the data at hand.  (One might consider various specific sequences that converge to $x$, such as $(x + 1/n)_n$ and $(x - 1/n)_n$, and use them to find upper bounds on $\delta$; but no finite set of sequences will give an entire interval around $x$, and proving that an infinite set of sequences that does cover an entire interval has a uniform positive upper bound on $\delta$ is very tricky.)

The usual proof that the real line (or any first-countable topological space) is sequential uses [[excluded middle]] and [[countable choice]]:  Supposing that $A$ is not open, consider $x \in A$ such that $x \notin Int(A)$, pick for each $\delta = 1/n$ (or for each of the countably many basic neighbourhoods $U_n$ of $x$ in a general first-countable space) a point $y_n$ such that $d(x,y_n) \lt 1/n$ (or such that $y_n \in U_n$) but $y_n \notin A$ (which must exist since none of these balls/neighbourhoods are contained in $A$), note that $\lim_n y_n = x$, and get a contradiction.

For this reason, constructive analysis often requires the use of general [[nets]] (or [[filters]]) in situations where classical analysis can get by with sequences.  (It is trivially true, in any topological space, that a set $A$ is open if every *net* that converges to an element $x$ of $A$ belongs eventually to $A$, or equivalently that $A$ belongs to any filter that converges to $x$; you just use the [[neighbourhood filter]] of $x$.)


## References 

* R. Engelking, _General topology_


[[!redirects sequential topological space]]
[[!redirects sequential topological spaces]]
[[!redirects sequential space]]
[[!redirects sequential spaces]]
