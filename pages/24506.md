+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of **Hasse-Schmidt derivation**, or **higher deriviation** is an extension of the notion of [[derivation]].

## Definition

Let $R$ be a [[commutative rig]] and $S$ a $R$-[[module]]. A Hasse-Schmidt derivation is a family of [[linear maps]] $(D^{n}:S \rightarrow S)_{n \ge 0}$ such that:

* $D^{0} = Id$
* $D^{n}(ab) = \underset{0 \le k \le n}{\sum}D^{k}(a)D^{n-k}(b)$

Note that $D^{1}$ is then a [[derivation]] in the usual sense.

## References

The notion is explicitely defined in:

* [[Morris Weifeld]]: *Purely Inseparable Extensions and Higher Derivations*, Transactions of the American Mathematical Society, **116** (1965) 435-449 [pdf](https://www.ams.org/journals/tran/1965-116-00/S0002-9947-1965-0191895-1/S0002-9947-1965-0191895-1.pdf)

where it is said that it is due to the paper:

* [[Helmut Hasse]]: *Noch eine Begründung der Theorie der höheren Differrentialquotienten in einem algebraischen Funktionenkörper einer Unbestimmten. (Nach einer brieflichen Mitteilung von [[Friedrich Karl Schmidt|F. K. Schmidt]] in Jena.)*, Reine Angew. Math.  **177** (1937) 215-223 &lbrack;[paper](https://gdz.sub.uni-goettingen.de/id/PPN243919689_0177?tify={%22pages%22:[219],%22view%22:%22export%22})&rbrack;

which defines the [[Hasse-Schmidt derivative]].



