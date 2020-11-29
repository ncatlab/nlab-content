
# Linear topological rings
* table of contents
{: toc}

##Idea

A [[topological ring]] $R$ is said to have a _(left) linear topology_ if it has a [[topological base]] of neighbourhoods of 0 consisting of (left) ideals.

Taking this apart we have a **definition/proposition** of such a topology, given by a left uniform filter:

+-- {: .num_prop}
###### Proposition (Gabriel)
A nonempty family of left ideals in $R$ is a left [[uniform filter]] (=[[topologizing filter]]) of left ideals iff it is a basis of neighborhood of $0$ of some
left linear topology. In other words, the following conditions hold:

[[filter|Filter]] axioms: (0) $\{R\}$ is open and:

(i) If $\mathfrak{a}\subseteq \mathfrak{b}$ are left ideals and $\mathfrak{a}$ is open, then so is $\mathfrak{b}$.

(ii) If $\mathfrak{a}$ and $\mathfrak{b}$ are open left ideas, then so is $\mathfrak{a}\cap\mathfrak{b}$.

Uniform filter condition:

(UF) If $\mathfrak{a}$ is an open left ideal and $r\in R$, then the left ideal

$$(\mathfrak{a}:r)= \{x\in R\mid x r\in \mathfrak{a}\}$$

is open.

=--

Note that if $R$ is commutative then (i) implies (UF).

## Examples

...


## References

* related ideas include [[pseudocompact ring]], [[Gabriel filter]], [[topologizing subcategory]], [[Gabriel-Oberst duality]], [[linearly compact module]]

*  [[Pierre Gabriel]],  __Des cat&#233;gories ab&#233;liennes__, Bulletin de la Soci&#233;t&#233; Math&#233;matique de France, 90 (1962), p. 323-448 ([numdam](http://www.numdam.org/item?id=BSMF_1962__90__323_0))

*  U. Oberst, _Duality theory for Grothendieck categories and linearly compact rings_, J. Algebra __15__ (1970), p. 473 --542, [pdf](http://www.sciencedirect.com/science/article/pii/0021869370900517)


[[!redirects linear topological ring]]
[[!redirects linear topological rings]]
[[!redirects linear topologizing ring]]
[[!redirects linear topologizing rings]]
[[!redirects linear topologising ring]]
[[!redirects linear topologising rings]]
