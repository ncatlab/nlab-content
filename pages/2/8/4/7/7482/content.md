
# Tuples
* table of contents
{: toc}

## Idea

The generalisation of [[ordered pair]] to something having more positions is usually called a *tuple* (or _ordered tuple_). More particularly one gets the term _$n$-tuple_, which refers to a list, $(x_1, \ldots, x_n)$, with $n$ entries from some set, $X$; here $n$ is a [[natural number]].  It thus corresponds to an element in the $n$-fold [[product set]], $X^n$. The various elements $x_i$ of the $n$-tuple are usually called its **components** and sometimes it is useful to call the set of components the **support** or **range** of the tuple.


## Variations

*  An [[ordered pair]] is a $2$-tuple.  A $3$-tuple is a _[[triple]]_, a $4$-tuple is a _[[quadruple]]_, a $5$-tuple is a _[[quintuple]]_ etc.

*  The notion of $1$-tuple is trivial; a $1$-tuple from $X$ is equivalent to an element of $X$.  But if you wish to emphasize that you have a $1$-tuple, then it may be called a _[[singleton list|singleton]]_.

*  The notion of $0$-tuple is also trivial, but in a different way; there is (for each set $X$) a single $0$-tuple from $X$.  See [[empty list]] for notations, but in the end it hardly matters what you call it.

*  The term 'tuple' is usually used for an $n$-tuple for a *specific* number $n$.  If we wish to speak of an $n$-tuple for an *arbitrary* $n$ (particularly without specifying that $n$), then we may speak of a [[list]] (which has other terminology, described on that page).  Then the set of lists is the [[disjoint union]] over $n$ of the sets of $n$-tuples.

*  The term 'tuple' is usually used for an $n$-tuple for a *finite* number $n$.  If we wish to speak of an $n$-tuple for an *infinite* (or possibly infinite) $n$, then we may speak of a [[sequence]].


## Formalisation

See [[ordered pair]] for methods of formalising ordered pairs (which are $2$-tuples) in various [[foundations of mathematics]].  Some of these generalise immediately to $n$-tuples for arbitrary $n$; otherwise, we may define $n$-tuples [[recursion|recursively]]: a triple is an ordered pair whose (say) first component is an ordered pair; a quadruple is an ordered pair whose first component is a triple, etc.


## Related concepts

* A 2-tuple is a [[pair]].

* A 3-tuple is [[triple]].


[[!redirects tuple]]
[[!redirects tuples]]
[[!redirects n-tuple]]
[[!redirects n-tuples]]
[[!redirects ordered tuple]]
[[!redirects ordered tuples]]
[[!redirects ordered n-tuple]]
[[!redirects ordered n-tuples]]
