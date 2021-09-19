
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

An __operator topology__ is an abbreviation of a __[[topology]] on a space of (continuous linear) [[linear operator|operator]]s__ between [[topological vector space]]s over a fixed [[field]] $k$ of [[real number|reals]] or [[complex number|complexes]] (possibly also p-adics, skewfield of [[quaternions]] etc.). In other words the [[hom-sets]] in the category of topological vector spaces as objects and continuous linear operators as morphisms are equipped with an operator topology.

There are many widely used topologies, some with standard names. Let $L(V,W) = Hom_{TVS}(V,W)$ be the set of continuous linear operators. 

* __weak operator topology__ on $L(V,W)$ is given by the basis of open neighborhoods of zero given by sets of the form $U(x,f) = \{A\in L(V,W) : |f(A(x)) \lt 1 \} $ where $x\in V$ and $f\in W^* = Hom_{TVS}(W,k)$. A sequence $(A_n)$ converges to $A$ in weak operator topology iff the sequence $(A_n(x))$ converges to $A(x)$ in the weak topology on $W$. We write $A_n\stackrel{w}\longrightarrow A$ or $w-lim A_n = A$. 

* __strong operator topology__: the basis of neighborhoods of zero is given by sets 
$N(x,U) = \{A\in L(V,W) \,|\, A v \in U\}$, where $v\in V$ and $U$ is a neighborhood of zero in $W$. For convergence of sequences, we write $A_n\stackrel{s}\longrightarrow A$ or $s-lim A_n= A$.

* __uniform operator topology__: here we assume that $V,W$ are normed spaces with norms $p_V$, $p_W$. Then $L(V,W)$ has a uniform operator topology induced by the norm given by the formula  

$$
p(A) = sup_{v\neq 0} \frac{p_W(A v)}{p_V (v)}
$$

* __ultraweak operator topology__ ...


## Properties

### Relation to norm topology

The reason that in the definition of a [[unitary representation]], the strong operator topology on $\mathcal{U}(\mathcal{H})$ is used and not the [[norm topology]], is that only few [[homomorphism]]s turn out to be [[continuous map|continuous]] in the norm topology.

Example: let $G$ be a [[compact topological space|compact]] [[Lie group]] and $L^2(G)$ be the [[Hilbert space]] of square integrable [[measurable function]]s with respect to its [[Haar measure]]. The right [[regular representation]] of $G$ on $L^2(G)$ is defined as

$$
      R: G \to \mathcal{U}(L^2(G))
$$

$$
         g \mapsto (R_g: f(x) \mapsto f(x g))
$$

and this will generally not be continuous in the norm topology, but is always continuous in the strong topology. 

## Related entries

* [[U(ℋ)]]

## References

* A. A. Kirillov, A. D. Gvi&#353;iani, &#1058;&#1077;&#1086;&#1088;&#1077;&#1084;&#1099; &#1080; &#1079;&#1072;&#1076;&#1072;&#1095;&#1080; &#1092;&#1091;&#1085;&#1082;&#1094;&#1080;&#1086;&#1085;&#1072;&#1083;&#1100;&#1085;&#1086;&#1075;&#1086; &#1072;&#1085;&#1072;&#1083;&#1080;&#1079;&#1072; (theorems and exercises in functional analysis), Moskva, Nauka 1979, 1988

[[!redirects operator topologies]]

[[!redirects topology on a space of operators]]
[[!redirects topologies on a space of operators]]

[[!redirects strong operator topology]]
[[!redirects weak operator topology]]
[[!redirects uniform operator topology]]

