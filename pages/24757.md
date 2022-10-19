> This article is about support of a [[function]]. For other notions of support, see [[support]]. 

---

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

\tableofcontents

## Definition

### In set theory

Given a [[pointed set]] $A$ with specified [[element]] $0 \in A$, a [[set]] $X$, and a [[function]] $f \colon X \to A$, the _support_ of $f$ is the [[subset]] of $X$ on which $f$ is not equal to $0$.

#### In constructive mathematics

In [[constructive mathematics]], there are multiple notions of [[inequality]], due to the failure of the [[double negation law]]. As a result, there are multiple notion of support of a function. Thus, we define the following:

Given a [[pointed set]] $A$ with specified [[element]] $0 \in A$, a [[set]] $X$, and a [[function]] $f \colon X \to A$, the **support** of $f$ is the [[subset]] of $X$ on which $f$ is not equal to $0$.

Given a [[pointed set]] $A$ with an [[tight apartness relation]] $\#$ and specified [[element]] $0 \in A$, a [[set]] $X$, and a [[function]] $f \colon X \to A$, the **strong support** of $f$ is the [[subset]] of $X$ on which $f$ is apart from $0$.

### In topology

 {#InTopology}

In [[topology]] the support of a [[continuous function]] $f \colon X \to A$ as above is the [[topological closure]] of the set of points on which $f$ does not vanish:

$$
  Supp(f) = Cl(\{x \in X \vert f(x) \neq 0 \in A\})
  \,.
$$

If $Supp(f) \subset X$ is a [[compact subspace]], then one says that $f$ has _[[compact support]]_.

## See also

* [[compact support]]
* [[compactly supported cohomology]]
* [[support of a distribution]]

## References

* Wikipedia, _[Support (mathematics)](https://en.wikipedia.org/wiki/Support_%28mathematics%29)_