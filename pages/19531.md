


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea 

A _smooth isotopy_ is an [[isotopy]] that varies [[smooth function|smoothly]], hence a isotopy that, as a [[left homotopy]], is a [[smooth homotopy]].

In [[knot theory]], one typically does not want to identify [[knots]] $S^1 \to S^3$ by plain [[isotopy]], as that makes all [[tame knots]] be equivalent. A common fix is to use [[ambient isotopy]] instead. But one may also use smooth isotopy. (see e.g. [Greene 13](#Greene13) or MO discussion [here](https://math.stackexchange.com/a/1312016/58526)).

## Definition

Let $\Sigma$ and $X$ be [[smooth manifolds]], and let 

$$
  \gamma_0, \gamma_1 \;\colon\; \Sigma \hookrightarrow X
$$

be two [[embeddings of smooth manifolds]]. Then a _smooth isotopy_ between them is a _[[smooth homotopy]] between them via [[embeddings of smooth manifolds|embeddings]]_: a [[smooth function]]

$$
  \eta \;\colon\; [0,1] \times \Sigma  \longrightarrow X
$$

such that

$$
  \eta(0,-) \;=\; \gamma_0
  \phantom{AAA}
  \eta(1,-) \;=\; \gamma_1
$$

and such that for each $t \in [0,1]$, 

$$
  \gamma(t,-)
  \;\colon\;
  \Sigma \longrightarrow X
$$

is an [[embedding of smooth manifolds]].

(e.g. [Greene 13, Def. 1.7](#Greene13))

## Related concepts

* [[smooth homotopy]]

## References

* {#Greene13} Josh Greene, _Combinatorial methods in knot theory_, 2013 ([pdf](https://www2.bc.edu/joshua-e-greene/MT885S13/Lecture%201.pdf))