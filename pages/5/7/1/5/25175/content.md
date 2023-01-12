
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Mathematics
+-- {: .hide}
[[!include mathematicscontents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

\tableofcontents

## Idea

Coherent mathematics is mathematics done using only [[coherent logic]]. 

Examples of coherent mathematics include mathematics done in an [[arithmetic pretopos]], which can be defined using only [[coherent logic]], as well as mathematics done in any [[dependent type theory]] which does not have [[function types]] and [[dependent function types]]. 

Since coherent logic does not have a negation operator in the logic, it is manifestly [[constructive]], since one cannot express the law of [[excluded middle]] or [[double negation]]. Similarly, coherent mathematics is manifestly [[strongly predicative]], since having [[function sets]] in the theory implies having [[implication]] and $\Delta_0$-[[universal quantifiers]], as every cartesian closed coherent category is a [[Heyting category]]. 

## Equality and apartness

Since coherent mathematics does not have negation, one cannot use negation to define [[denial inequality]] as the [[negation]] of [[equality]]. In particular, what fails is that the definition of denial inequality involves a double implication 
$$((a = b) \implies \bot) \implies (a \neq b)$$ 
which is not allowed in coherent mathematics. On the level of coherent [[sequents]], single implications $\phi \implies \psi$ are expressed as [[entailment]], the sequent $\phi \vdash \psi$. But double implications $(\phi \implies \psi) \implies \varphi$ become the sequent $(\phi \implies \psi) \vdash \varphi$, which cannot be simplified down further to get rid of the remaining implication. Instead, one has to use the positive notion of [[apartness relation]] to express the notion of "not being equal". 

Similarly to the fact that one cannot define denial inequality in coherent mathematics, one cannot define a [[tight apartness relation]], since the definition involves negation of an apartness relation. As a result, concepts such as [[Heyting fields]] which are important in [[constructive mathematics]] cannot be defined, and one has to use alternative concepts such as [[local rings]] instead. 

Other things have to be expressed positively as well - for example, in the definition of a [[local ring]], one cannot say that the non-invertible elements form an [[ideal]]; one has to say that the invertible elements form an [[anti-ideal]]. Furthermore, in the definition of an anti-ideal itself, one cannot say that $0$ is not in the anti-ideal. One has to say that every element in the ideal is apart from zero, $0 \# a$; and this means that anti-ideals are only definable in rings which come equipped with an [[apartness relation]]. 

Sets with [[decidable equality]] are however still definable in coherent mathematics; they are sets $S$ equipped with an [[apartness relation]] such that for all elements $a \in S$ and $b \in S$, $a = b$ or $a \# b$. This means that one could work in predicative [[classical mathematics]] (i.e. a [[Boolean category]]) by stipulating that every set has decidable equality. 

## See also

* [[coherent logic]]
* [[foundations of mathematics]]
* [[constructive mathematics]]
* [[predicative mathematics]]
* [[classical mathematics]]