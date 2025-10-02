
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

\begin{definition}
A _topological ring_ is a [[ring]] [[internalization|internal to]] the [[category]] [[Top]] of [[topological spaces]], hence: a [[ring object]] [[internalization|in]] [[Top]]:

a [[topological space]] $R$ equipped with the [[structure]] of a [[ring]] on its underlying [[set]], such that [[addition]] $+$ and [[multiplication]] $\cdot$ are [[continuous functions]]. 
\end{definition}

\begin{definition}
A _[[topological field]]_ is a topological ring $K$ whose [[underlying]] ring is in fact a [[field]] and such that reciprocation $(-)^{-1}: K \setminus \{0\} \to K \setminus \{0\}$ is [[continuous map|continuous]]. This latter condition is the same as demanding that the [[subspace]] [[topological space|topology]] on $K \setminus \{0\}$ induced by the embedding $K \setminus \{0\} \hookrightarrow K$ coincide with the subspace topology induced by the embedding $K \setminus \{0\} \to K \times K: x \mapsto (x, x^{-1})$. More at *[[topological field]]*.
\end{definition}

\begin{definition}
A *[[topological algebra]]* ---  namely a topological [[associative algebra]] ---, over a topological ring $R$ is a topological ring $S$ together with a topological ring [[homomorphism]] $R \to S$ that makes $S$ an [[associative algebra|$R$-algebra]] on the [[underlying set]]. 
\end{definition}

## Properties

* The structure of a topological ring $(R,+,\cdot)$ makes $R$ a [[uniform space]]. 

* It is automatic that [[negation]] in a topological unital ring is continuous, since it is the operation of multiplication with $-1$, and multiplication is continuous in each argument. Hence for $(R,+,\cdot)$ a topological ring, then $(R,+)$ is a [[topological group]].


* In a topological ring, the [[topological closure|closure]] of $\{0\}$ is an [[ideal]]. It follows that for a [[topological field]] $F$, either $0$ is a [[closed point]] (so that $F$ is $T_1$ and therefore [[Tychonoff space|completely regular Hausdorff]], by standard arguments in the theory of [[uniform spaces]]), or is a [[codiscrete space]]. 





## Examples

* The [[real numbers]] and [[complex numbers]] form topological rings, in fact [[topological fields]].

* Any [[pseudocompact ring]] such as the completed [[group ring]] of a [[profinite group]] is a topological ring.

*  For any [[prime number]] $p$, the ring of [[p-adic integers]] is a topological ring.
  
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

Lecture notes:

* [[Daniel Murfet]], _Topological rings_ (2005) &lbrack;[pdf](http://therisingsea.org/notes/TopologicalRings.pdf)&rbrack;
 
See also:

* [[eom]]: _[Topological ring](https://www.encyclopediaofmath.org/index.php/Topological_ring)_

* [[Stacks Project]]: _[Topological ring](http://stacks.math.columbia.edu/tag/07E8)_

* Wikipedia: _[Topological ring](https://en.wikipedia.org/wiki/Topological_ring)_



[[!redirects topological rings]]

