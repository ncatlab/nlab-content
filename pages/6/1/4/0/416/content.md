
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--



#Contents#
* automatic table of contents goes here
{:toc}

## Definition 

Let $V$ be a [[closed monoidal category|closed]] [[symmetric monoidal category]].  In a $V$-[[enriched category]] $C$, the **power** of an object $y\in C$ by an object $k\in V$ is an object $\pitchfork(k,y) \in C$ with a [[natural isomorphism]]

$$
  C(x, \pitchfork(k,y)) \cong V(k, C(x,y))
$$

where $C(-,-)$ is the $V$-valued hom of $C$ and $V(-,-)$ is the internal-hom of $V$.

## Remarks 

* In the $V$-category $V$, the power is just the internal-hom of $V$.

* Powers are a special sort of [[weighted limit]].  Conversely, all weighted limits can be constructed from powers together with [[conical limit]]s.  The dual colimit notion of a power is a [[copower]].

* Powers are frequently called _cotensors_ and a $V$-category having all powers is called _cotensored_, while the word "power" is reserved for the case $V=Set$.  However, there seems to be no good reason for making this distinction.  Moreover, the word "tensor" is fairly overused, and unfortunate since a tensor (= a [[copower]]) is a colimit, while a cotensor (= power) is a limit.

[[!redirects cotensor]]
[[!redirects cotensoring]]

[[!redirects powers]]
[[!redirects cotensors]]
[[!redirects cotensored category]]
