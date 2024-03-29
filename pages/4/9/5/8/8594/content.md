
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

A _topological ring_ is a [[ring]] [[internalization|internal to]] [[Top]], a [[ring object]] in [[Top]]:

a [[topological space]] $R$ equipped with the structure of a [[ring]] on its underlying [[set]], such that [[addition]] $+$ and [[multiplication]] $\cdot$ are [[continuous functions]]. 

Remarks:

* The structure of a topological ring $(R,+,\cdot)$ makes $R$ a [[uniform space]]. 

* It is automatic that negation in a topological unital ring is continuous, since it is the operation of multiplication with $-1$, and multiplication is continuous in each argument. Hence for $(R,+,\cdot)$ a topological ring, then $(R,+)$ is a [[topological group]].

* A _[[topological field]]_ is a topological ring $K$ whose underlying ring is in fact a [[field]] and such that reciprocation $(-)^{-1}: K \setminus \{0\} \to K \setminus \{0\}$ is continuous. This latter condition is the same as demanding that the subspace topology on $K \setminus \{0\}$ induced by the embedding $K \setminus \{0\} \hookrightarrow K$ coincide with the subspace topology induced by the embedding $K \setminus \{0\} \to K \times K: x \mapsto (x, x^{-1})$. More at [[topological field]]. 

+-- {: .num_remark} 
###### Remark 
In a topological ring, the closure of $\{0\}$ is an [[ideal]]. It follows that for a topological field $F$, either $0$ is a closed point (so that $F$ is $T_1$ and therefore [[Tychonoff space|completely regular Hausdorff]], by standard arguments in the theory of uniform spaces), or is a [[codiscrete space]]. 
=-- 

A [[topological algebra]] over a topological ring $R$ is a topological ring $S$ together with a topological ring map $R \to S$ that makes $S$ an $R$-algebra at the underlying set level (a topological [[associative algebra]]). 


## Examples

* The [[real numbers]] form a topological field.

* Any [[pseudocompact ring]] such as the completed [[group ring]] of a [[profinite group]] is a topological ring.

*  For any prime $p$, the ring of [[p-adic integers]] is a topological ring.
  
* A [[Banach algebra]] is in particular a [[topological algebra]], hence a topological ring. Hence so is a [[C-star-algebra]].

## Related concepts

* [[topological monoid]]

* [[normed ring]]

* [[local field]]

* [[completion of a ring]]

* [[linear topological ring]]

* [[real homotopy theory]]

* [[topological vector space]]

## References

Lecture notes include

* [[Daniel Murfet]], _Topological rings_ ([pdf](http://therisingsea.org/notes/TopologicalRings.pdf))
 
See also

* [[eom]], _[Topological ring](https://www.encyclopediaofmath.org/index.php/Topological_ring)_

* [[Stacks Project]], _[Topological ring](http://stacks.math.columbia.edu/tag/07E8)_

* Wikipedia, _[Topological ring](https://en.wikipedia.org/wiki/Topological_ring)_



[[!redirects topological rings]]

