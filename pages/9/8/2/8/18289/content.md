
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A [[topological space]] $K$ is called an _absolute extensor_ if for

1. $X$ any [[nice topological space|nice]] [[topological space]]

1. $A \overset{i}{\hookrightarrow} X$ any [[closed subspace]]  

1. $f\colon A \longrightarrow K$ any [[continuous function]] 

there is an [[extension]] to a [[continuous function]] $\tilde{f}:X\to K$, i.e., such that $\tilde{f}=f\circ i$:
$$
  \array{
    A &\overset{f}{\longrightarrow}& K
    \\
    {}^{\mathllap{i}}\downarrow & \nearrow_{\mathrlap{\exists \tilde f}}
    \\
    X
  }
$$

Here "[[nice topological space]]" is variously taken to mean [[metrizable topological space]] or at least [[normal topological space]]. 

A variation of this concept, **absolute neighborhood extension**, only requires the extension to exist over a neighborhood of $A$ in $X$.

## Examples

The [[Tietze extension theorem]] implies that the [[real line]] $\mathbb{R}$ equipped with its [[Euclidean space]] [[metric topology]] is an absolute extensor. It follows that so are the [[closed interval]] [[subspace]] $[0,1] \subset \mathbb{R}$ and the [[circle]] $S^1$.

Products of absolute extensors are absolute extensors, including the [[Hilbert cube]].

The two point discrete space $S^0$ as well as any sphere $S^n$ is an absolute neighborhood extensor, but not an absolute extensor.


## Related concepts

* [[Tietze extension theorem]]

* [[quasi-finite CW-complex]]

* [[absolute retract]]


## References

* [[eom]], _[Absolute neighbourhood extensor](https://www.encyclopediaofmath.org/index.php/Absolute_neighbourhood_extensor)_

[[!redirects absolute extensors]]

[[!redirects absolute neighbourhood extensor]]
[[!redirects absolute neighbourhood extensors]]

[[!redirects absolute neighborhood extensor]]
[[!redirects absolute neighborhood extensors]]
