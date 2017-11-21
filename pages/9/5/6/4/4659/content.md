
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Definition

A [[Lie algebra]] is __semisimple__ if it is the [[direct sum]] of [[simple Lie algebra]]s.

(Notice that this is not quite the same as a [[semisimple object]] in the [[category]] of Lie algebras, because a simple Lie algebra is not quite the same as a [[simple object]] in the [[LieAlg]]. But this is the standard terminology convention.)

By [[Lie integration]] semisimple Lie algebras correspond to [[Lie group]]s that are [[semisimple Lie group]]s.


## Properties

Every semisimple Lie algebra is a [[reductive Lie algebra]].

A Lie algebra $\mathfrak{g}$ is semisimple precisely if the [[Killing form]] [[invariant polynomial]]

$$
  \langle x,y \rangle \coloneqq tr (ad_x \circ ad_y)
$$

is non-degenerate as a [[bilinear form]].

The corresponding cocycle $\langle -,[-,-]\rangle$ in [[Lie algebra cohomology]] is the one that classifies the [[string Lie 2-algebra]]-extension of $\mathfrak{g}$.


## Classification

Since we can classify [[simple Lie algebras]], we can classify semisimple Lie algebras; for each simple Lie algebra, we simply indicate how many times it appears in the direct-sum decomposition.  (There is a theorem to prove here: that the decomposition of a semisimple Lie algebra is unique.)

## Related concepts

* An infinite-dimensional generalization of semisimple Lie algebras are [[Kac-Moody Lie algebras]].

* [[exceptional Lie algebra]]

## References

* Robert Cahn, _Semisimple Lie algebras and their representation_ ([pdf](http://phyweb.lbl.gov/~rncahn/www/liealgebras/texall.pdf))

Basics of the representation theory of semisimple Lie algebras is surveyed in 

* [[Joseph Bernstein]], _Lectures on Lie Algebras_, in:
Representation Theory, Complex Analysis and Integral Geometry, Birkhauser (2012), 97-133, [pdf](http://wwwmath.tau.ac.il/~bernstei/Publication_list/publication_texts/bernsteinLieNotes_book.pdf)

[[!redirects semisimple Lie algebra]]
[[!redirects semisimple Lie algebras]]
