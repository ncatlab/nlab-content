
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of _enomorphism operad_ is the analog in [[operad]]-theory of the notion of the [[delooping]] [[category]] $\mathbf{B}A$ of an [[endomorphism monoid]] $End(A)$ in [[category theory]].


## Definition ##


For $(C,\otimes, I)$ a [[symmetric monoidal category]] and $X \in C$ any [[object]], the **endomorphism operad** $End_C(X)$ of $X$ in $C$ is the [[operad]] whose set of $n$-ary operations is the [[hom-set]]

$$
  End_C(X)_k := Hom_C(X \otimes \cdots k factors \cdots \otimes X, X)
  \,,
$$

This comes with the obvious composition operation induced from the composition in $C$.

If $C$ is a [[closed monoidal category]] then we may replace the [[hom-set]] by the corresponding [[hom-object]] in $C$ and get an operad in $C$.

Similarly, if $S \in Set$ is a [[set]] ( _of colours_ ) and $\{A_s | s \in S\}$ is a set of objects, the the **$S$-coloured endomorphism operad** $End(\{A_s\})$ is the [[coloured operad]] with objects $A_s$ and hom-objects

$$
  P(s_1, \cdots, s_n;s) :=
  C(A_{s_1} \otimes  \cdots \otimes A_{s_n}; A_{s})
$$

## Properties

For $C$ closed symmetric monoidal category and $P$ a $C$ operad, the structure of an [[algebra over an operad]] on an object $A \in C$ over $P$ is equivalently a [[morphism]] of operads

$$
 \rho : P \to End(A)
$$

## Related concepts

* [[endomorphism]]

* [[endomorphism monoid]], [[endomorphism ring]]

* **endomorphism operad**

[[!redirects endomorphism operads]]