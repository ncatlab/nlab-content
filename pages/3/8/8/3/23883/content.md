
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Let $C$ be a [[finitely complete category]]. This means that $C$ is symmetric, and for objects $X$ and $Y$ there exist isomorphisms $B_{X, Y}: X \times Y \cong Y \times X$ and $B_{Y, X}: Y \times X \cong X \times Y$ such that $B_{X, Y} \circ B_{Y, X} = id_{X \times Y}$ and $B_{Y, X} \circ B_{X, Y} = id_{Y \times X}$. Given an [[internal relation]] $R\stackrel{(s,t)}\hookrightarrow X \times Y$, the [[pullback]] of the internal relation $(s,t)$ along the [[braiding]] $B_{Y, X}$ is the **opposite internal relation** [[span]] 
$$R \stackrel{\dagger_{R^\op,R}}\leftarrow R^\op\stackrel{(t,s)}\hookrightarrow Y \times X$$ 
with a morphism $\dagger_{R,R^\op}:R \to R^\op$ such that $\dagger_{R,R^\op} \circ \dagger_{R^\op,R} = id_{R^\op}$ and $\dagger_{R^\op,R} \circ \dagger_{R,R^\op} = id_{R}$. 

## See also

* [[internal relation]]

* [[opposite relation]]

* [[internal antisymmetric relation]]

[[!redirects opposite internal relations]]