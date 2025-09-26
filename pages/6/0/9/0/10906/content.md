> Not to be confused with the notion of *[[coherent space]]* in [[topology]].

***

#Contents#
* table of contents
{:toc}

## Idea

The notion of _coherence space_ ([Girard 1989, §8 ](#Girard89), also sometimes "[[coherent space]]" but beware of the alternative meaning discussed there) is used for the [[semantics]] of [[linear logic]] in [[proof theory]].  They form a [[star-autonomous category]].

A coherence space is analogous to a [[locale]] defined by a [[topological base|basis]] for its [[frame]] of opens. A coherence space has a set of "tokens" we think of as "primitive observations" along with a coherence relation that says when primitive observations are "coherent" in that they can both be satisfied by the same point of the space. A point of the space can then be defined as a [[clique]] of observations: a set of observations such that every pair in the set is coherent.

## Definitions

### As a Set of Cliques

A coherence space $X$ is a collection of subsets of a set $|X|$ which verify some conditions. We call:

* $|X|$ the web of $X$
* the elements of $|X|$, the points of $X$
* the elements of $X$, the cliques of $X$

The conditions to be verified are:

* Every subset of a clique is a clique.
* If $a$ is a point, then $\{a\}$ is a clique.
* If $A$ is a family of cliques such that $(x,y \in A) \Rightarrow (x \cup y \in X)$, then $\bigcup A$ is a clique.

### As an Undirected Graph

Equivalently, a coherence space $X$ consists of

1. A set $|X|$, called the web of $X$, whose elements are called "tokens"
2. A reflexive, symmetric binary relation $~$ on $|X|$ called the _coherence_ relation

A clique is then a subset of $|X|$ such that each pair of elements is coherent. A co-clique is a subset of $|X|$ where any two *distinct* elements $x \neq y$ are *incoherent* $\neg (x ~ y)$.

### As an Arity Space

Coherence spaces can be defined as [[arity spaces]] for the "subunary" class of arities $\{0,1\}$.

## Morphisms

A linear function of coherence spaces $f : X \multimap Y$ is a relation $f \subseteq |X|\times|Y|$ that

1. preserves cliques: if $U$ is a $X$-clique then $f_*(U) = \{ y \in Y | \exists x \in U. f(x,y) \}$ is a $Y$-clique .
2. reflects co-cliques: if $V$ is a $Y$-co-clique then $f^*(U) = \{ x \in X | \exists y \in V. f(x,y)\}$ is an $X$-co-clique.

## Properties

The notion in terms of a set of cliques and a coherence relation are equivalent by the following:
\begin{proposition}
The map which send an [[undirected simple graph]] $G$ to the pair $(C(G), V(G))$ where $V(G)$ is the set of all the vertices of $G$ and $C(G)$ is the set of all the [[cliques]] of $G$ is a bijection between undirected simple graphs and coherence spaces where the coherence space associated to $G$ is $C(G)$ with $|C(G)|=V(G)$. The reciprocal map associates to a coherence space $X$ the undirected simple graph $G$ obtained by taking $V(G)=|X|$ and the set $E(G)$ of edges equal to the set of all cliques of cardinal $2$.
\end{proposition}

## References

The terminology "coherence space" seems to be due to:

* {#Girard89} [[Jean-Yves Girard]] (translated and with appendiced by [[Paul Taylor]] and [[Yves Lafont]]), Section 8 of: *Proofs and Types*, Cambridge University Press (1989) &lbrack;[ISBN:978-0-521-37181-0](), [webpage](http://www.paultaylor.eu/stable/Proofs+Types.html), [pdf](https://www.paultaylor.eu/stable/prot.pdf)&rbrack;

Other references say instead "coherent space":

* Wikipedia, _[Coherent space](http://en.wikipedia.org/wiki/Coherent_space)_

* LLwiki, _[Coherent semantics](http://llwiki.ens-lyon.fr/mediawiki/index.php/Coherent_semantics)_

*  [[Jean-Yves Girard]], _Linear logic_,   Theoretical Computer Science 50:1, 1987.  ([pdf](http://iml.univ-mrs.fr/~girard/linear.pdf))

[[!redirects coherence space]]
[[!redirects coherence spaces]]
