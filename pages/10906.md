> Not to be confused with the notion of *[[coherent space]]* in [[topology]].

***

#Contents#
* table of contents
{:toc}

## Idea

The notion of _coherence space_ ([Girard 1989, §8 ](#Girard89), also sometimes "[[coherent space]]" but beware of the alternative meaning discussed there) is used for the [[semantics]] of [[linear logic]] in [[proof theory]].  They form a [[star-autonomous category]].


Coherence spaces can be defined as [[arity spaces]] for the "subunary" class of arities $\{0,1\}$.

## Definition

A coherence space $X$ is a collection of subsets of a set $|X|$ which verify some conditions. We call:

* $|X|$ the web of $X$
* the elements of $|X|$, the points of $X$
* the elements of $X$, the cliques of $X$

The conditions to be verified are:

* Every subset of a clique is a clique.
* If $a$ is a point, then $\{a\}$ is a clique.
* If $A$ is a family of cliques such that $(x,y \in A) \Rightarrow (x \cup y \in A)$, then $\bigcup A$ is a clique.


## References

The terminology "coherence space" seems to be due to:

* {#Girard89} [[Jean-Yves Girard]] (translated and with appendiced by [[Paul Taylor]] and [[Yves Lafont]]), Section 8 of: *Proofs and Types*, Cambridge University Press (1989) &lbrack;[ISBN:978-0-521-37181-0](), [webpage](http://www.paultaylor.eu/stable/Proofs+Types.html), [pdf](https://www.paultaylor.eu/stable/prot.pdf)&rbrack;

Other references say instead "coherent space":

* Wikipedia, _[Coherent space](http://en.wikipedia.org/wiki/Coherent_space)_

* LLwiki, _[Coherent semantics](http://llwiki.ens-lyon.fr/mediawiki/index.php/Coherent_semantics)_

[[!redirects coherence space]]
[[!redirects coherence spaces]]
