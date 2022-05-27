
> This entry is about topological orders of directed acyclic graphs in [[graph theory]]. For topological orders of materials in [[condensed matter physics]], see [[topological order]]. 

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn #LinearExtensionOfAPartialOrder}
###### Definition
**(linear extension)**

Given a [[set]] $X$ equipped with a [[partial ordering]] $\leq$, then a _linear extension_ is a [[linear order]] $\leq_{lin}$ on the same set $S$, such that the [[identity function]] $id_S$ is order-preserving

$$
  (S,\leq) \overset{ id_S }{\longrightarrow} \left(S,\leq_{lin}\right)
  \,.
$$

=--

In [[graph theory]], a set equipped with a partial order is a directed acyclic graph, with the partial order representing the reachability relation of the graph, and the linear extension of the reachability relation is called a **topological order**. 

## Properties

+-- {: .num_prop #ExistenceOfLinearExtensions}
###### Proposition
**(existence of linear extensions)**

For [[finite sets]] linear extensions (Def. \ref{LinearExtensionOfAPartialOrder}) always exist. For non-finite sets this is still the case using the [[axiom of choice]].

=--

A proof under [[axiom of choice|AC]] was first published in ([Marczewski 30](#Marczewski30)). The proposition actually follows from the weaker choice principle called the [[ultrafilter theorem|ultrafilter principle]], by appeal to the [[compactness theorem]], as follows. 

+-- {: .proof} 
###### Proof 
It is a very simple matter to show linear extensions exist in the [[finite set|finite]] case: one may proceed by [[induction]]. Any finite $n$-element poset has a [[minimal element]] $x$ (meaning $y \leq x$ implies $y = x$). By induction the restricted partial order on $X \setminus \{x\}$ admits a linear extension, and then one may simply prepend $x$ to that linear order to complete the inductive step. 

The rest is a routine application of compactness for [[propositional theories]]. Let $(X, \leq)$ be a partially ordered set, and introduce a [[signature]] consisting of [[signature|constants]] $c_x$, one for each $x \in X$, and a [[binary relation]] $L$. Introduce [[axioms]] $\neg(c_x = c_y)$ whenever $x \neq y$ in $X$, and $L(c_x, c_y)$ whenever $x \leq y$ in the poset $X$, and axioms stating that $L$ is a linear order. By the previous paragraph, the resulting theory is finitely satisfiable upon interpreting each $c_x$ as $x$. Hence the theory is satisfiable. Taking any [[model]] $M$, and interpreting the constants in $M$, and restricting $L$ to them, we obtain a linear extension on $X$.   
=--

## References

* {#Marczewski30} Edward Marczewski, _Sur l'extension de l'ordre partiel_, Fundamenta Mathematicae, 16: 386–389 (1930) ([pdf](http://matwbn.icm.edu.pl/ksiazki/fm/fm16/fm16125.pdf))

See also

* Wikipedia, _[Linear extension](https://en.wikipedia.org/wiki/Linear_extension)_

* Wikipedia, _[Topological ordering](https://en.wikipedia.org/wiki/Topological_ordering)

[[!redirects linear extensions of partial orders]]
[[!redirects topological ordering]]
[[!redirects topological orderings]]
