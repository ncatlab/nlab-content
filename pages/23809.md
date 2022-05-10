
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Cup-$i$ products extend [[cup products]].

They can be used to define [[Steenrod squares]]
in the same manner as ordinary [[cup products]] can be used to define the square of a cohomology class.

## Definition

Given a [[simplicial set]] $X$ and $i\ge0$, we define
the cup-$i$ product as the map on simplicial cochains on $X$
with coefficients in $\mathbf{Z}/2$ induced by the map on simplicial chains
$$\Delta_i: C(X,\mathbf{Z}/2) \to C(X,\mathbf{Z}/2)\otimes C(X,\mathbf{Z}/2),$$
where $\Delta_i$ evaluate on an $n$-simplex $x\in X_n$
is 0 if $i\gt n$ and
$$\sum_U d_{U^0}(x)\otimes d_{U^1}(x),$$
where $U\subset \{0,\ldots,n\}$ has cardinality $n-i$
and
$$U^k=\{u\in U\mid r(u)+k=u \pmod2\},$$
where $r(u)=\#\{v\in U\mid v\le u\}$.

Thus, we have
$$(x \cup_i y)(c) = (x\otimes y)(\Delta_i(c)).$$

## Properties

We have
$$Sq^i(x) = x \cup_i x,$$
where $Sq^i$ denotes the $i$th [[Steenrod square]].

## Related concepts

* [[cup product]]

* [[Steenrod square]]

## References

* [[Anibal M. Medina-Mardones]], _New formulas for cup-$i$ products and fast computation of Steenrod squares_, [arXiv](arXiv:2105.08025).

* [[Ralph M. Kaufmann]], [[Anibal M. Medina-Mardones]], _Cochain level May-Steenrod operations_, [arXiv](https://arxiv.org/abs/2010.02571).

* [[Anibal M. Medina-Mardones]], _An axiomatic characterization of Steenrod's cup-i products_, [arXiv](https://arxiv.org/abs/1810.06505).

[[!redirects cup-i products]]
