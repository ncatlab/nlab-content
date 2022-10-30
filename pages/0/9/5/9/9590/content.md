[[!redirects vanish at infinity]]


#Contents#
* table of contents
{:toc}

## Definition

For $A$ a [[Banach space]] and $X$ a [[topological space]], a [[function]] $X \to A$ is said to **vanish at infinity** if for every positive [[real number]] $\epsilon \in \mathbb{R}_+$ there is a [[compact subset]] $K \hookrightarrow X$ such that 

$$
  \underset{{x \in X\backslash K}}{\forall} \;  {\vert f(x)\vert} \lt \epsilon
  \,.
$$


## Properties 

If $X$ is a [[locally compact topological space|locally compact]] [[Hausdorff topological space]], then one way of considering this definition is that one can adjoin to $X$ a point "at infinity", denoted $\infty$, by declaring that the open neighborhoods of $\infty$ are sets of the form $\{\infty\} \cup (X \backslash K)$ for $K \subset X$ compact. This is called the [[one-point compactification]], denoted $X^+$. Then a function $f: X \to A$ vanishes at infinity iff there exists an extension of $f$ to a continuous function $X^+ \to A$ that sends $\infty$ to $0$ (thus literally "vanishing at $\infty$"). 

Equivalently, functions that vanish at infinity are precisely those that can be extended by 0 to [[continuous functions]] on the [[Stone–Čech compactification]] of $X$.

## References

* Wikipedia, _[Locally compact](http://en.wikipedia.org/wiki/Locally_compact)_
