## Idea

A [[set]] is infinite if it is not [[finite set|finite]].

The existence of an infinite set is usually given by an [[axiom of infinity]].  The main example is the set of [[natural number]]s.


## Definitions

As you can see from [[finite set]], there are at least five definitions of that term, which are all equivalent given the [[axiom of choice]].  The [[negation]] of any of these gives a definition of infinite set.

However, the definition usually used in practice in [[constructive mathematics]] is this:

+-- {: .un_defn}
###### Definition

A set $S$ is __infinite__ if, given any [[natural number]] $n$ and a finite [[sequence]] $(x_1, \ldots, x_n)$ of elements of $S$, there exists an element $y$ of $S$ such that $y = x_i$ is always false.
=--

In other words, given any [[function]] $f$ from a Kuratowski-finite set to $S$, there exists an element of $S$ that is not in the [[image]] of $f$.

Note that you can make this definition work without previously assuming the existence of natural numbers, by using an infinity-free definition of Kuratowski-[[finite set]].


## Remarks

Probably a lot to say about the relation between the various definitions of infinite set (the one above, the negations of the definitions of finite set, and others that might be studied).  In the meantime, try [the English Wikipedia](http://secure.wikimedia.org/wikipedia/en/wiki/Dedekind-infinite_set).


[[!redirects infinite sets]]