
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

* [[special orthogonal Lie algebra]]

* [[string Lie 2-algebra]]

* **fivebrane Lie 6-algebra**

***

#Contents#
* table of contents
{:toc}

## Idea

The _fivebrane Lie 6-algebra_ is the second step in the [[∞-Lie algebra]]-[[Whitehead tower]] (read as the [[Whitehead tower in an (∞,1)-topos]] in [[?LieGrpd]]) of the [[special orthogonal group]].



## Definition

Let $\mathfrak{g}$ be the [[special orthogonal Lie algebra]]. The first two [[∞-Lie algebra cocycle]]s on it are in degree 3 and 7.

$$
  \mu_3 : \mathfrak{g} \to b^2 \mathbb{R}
$$

$$
  \mu_7 : \mathfrak{g} \to b^6 \mathbb{R}
  \,.
$$

The [[∞-Lie algebra cohomology|extension]] classified by the first is the [[string Lie 2-algebra]]

$$
  b \mathbb{R} \to \mathfrak{string} \to \mathfrak{so}
  \,.
$$

But $\mu_7$ is still also a [[∞-Lie algebra cocycle]] on $\mathfrak{string}$:

$$
  \mu_7 : \mathfrak{string} \to b^6 \mathbb{R}
  \,.
$$

The extension classified by this is the **fivebrane Lie 6-algebra**

$$
  b^5 \mathbb{R} \to \mathfrak{fivebrane} \to \mathfrak{string}
  \,.
$$

## Properties

The [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{fivebrane})$ is the relative [[Sullivan algebra]] obtained by gluing the two cocoycles.

Under [[Lie integration]] the Lie 6-algebra $\mathfrak{fivebrane}$  yields the [[fivebrane 6-group]].


## References

As with many of these [[∞-Lie algebra]]-constructions, the existence of the object itself, regarded dually as a [[dg-algebra]] is a triviality in [[rational homotopy theory]], but the interpretation in $\infty$-Lie theory adds a new perspective to it. In this context the fivebrane Lie 6-algebra was introduced in

* SSSI (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSI">web</a>)

and its relation to [[fivebrane structure]]s and [[quantum anomaly]]-cancellation in [[dual heterotic string theory]] was discussed in 

* SSSII (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSII">web</a>)
