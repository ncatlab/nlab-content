> Not to be confused with the notion of [[coherent space]] in [[topology]].

***

* table of contents
{:toc}

## Idea

The notion of _coherence space_ (sometimes "coherent space") is used for the [[semantics]] of [[linear logic]] in [[proof theory]].  They form a [[star-autonomous category]].

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

* Wikipedia, _[Coherent space](http://en.wikipedia.org/wiki/Coherent_space)_
* LLwiki, _[Coherent semantics](http://llwiki.ens-lyon.fr/mediawiki/index.php/Coherent_semantics)_

[[!redirects coherence space]]
[[!redirects coherence spaces]]
