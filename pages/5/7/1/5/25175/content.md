
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

Examples of coherent mathematics include mathematics done in an [[arithmetic pretopos]], which can be defined using only [[coherent logic]], as well as mathematics done in any [[dependent type theory]] which does not have [[function types]] nor [[dependent function types]], such as the internal type theory of an [[arithmetic pretopos]] as a fragment of [[geometric type theory]]. 

Since coherent logic does not have a [[negation]] operator, it is manifestly [[constructive]], since one cannot even express the law of [[excluded middle]] or [[double negation]]. Similarly, coherent mathematics is manifestly [[strongly predicative]], since having [[function sets]] in the theory implies having [[implication]] and $\Delta_0$-[[universal quantifiers]], as every cartesian closed coherent category is a [[Heyting category]]. 

## Equality and apartness

Since coherent mathematics does not have [[negation]], one cannot use negation to define [[denial inequality]] as the [[negation]] of [[equality]]. In particular, what fails is that the definition of denial inequality involves a double implication 
$$
  \big(
    (a = b) 
      \implies 
    \bot
  \big) 
    \implies 
  (a \neq b)
$$ 
which is not allowed in coherent mathematics. On the level of coherent [[sequents]], single implications $\phi \implies \psi$ are expressed as [[entailment]], the sequent $\phi \vdash \psi$. But double implications $(\phi \implies \psi) \implies \varphi$ become the sequent $(\phi \implies \psi) \vdash \varphi$, which cannot be simplified down further to get rid of the remaining implication. Instead, one has to use the positive notion of [[apartness relation]] $a \# b$ to express the notion of "not being equal". 

Similarly to the fact that one cannot define denial inequality in coherent mathematics, one cannot define a [[tight apartness relation]], since the definition involves negation of an apartness relation implying equality, which is a double implication 
$$((a \# b) \implies \bot) \implies (a = b)$$ 
As a result, concepts such as [[Heyting fields]] which are important in [[constructive mathematics]] cannot be defined, and one has to use alternative concepts such as [[local rings]] instead. 

Other things have to be expressed positively as well - for example, in the definition of a [[local ring]], one cannot say that the non-invertible elements form an [[ideal]] $I \subseteq A$, since that would involve an implication
$$((\exists y \in R.x \cdot y = 1) \implies \bot) \vdash x \in I$$
or in the structural case with injection $i:I \hookrightarrow R$, 
$$((\exists y \in R.x \cdot y = 1) \implies \bot) \vdash \exists z \in I.i(z) = x$$
Instead, one has to say that the invertible elements form an [[anti-ideal]] $A \subseteq R$. 
$$\exists y \in R.x \cdot y = 1 \vdash x \in A \quad \mathrm{material}$$
$$\exists y \in R.x \cdot y = 1 \vdash \exists z \in A.i(z) = x \quad \mathrm{structural}$$
Furthermore, in the definition of an anti-ideal itself, when one says that $0$ is not in the anti-ideal, one has to express it as a sequent $0 \in A \vdash \bot$, or in the structural case with injection $i:A \hookrightarrow R$, that $\exists x \in A.i(x) = 0 \vdash \bot$. Alternatively, if the set has an apartness relation one could just say that every element in the ideal is apart from zero, $0 \# x$. 

The [[degree of a polynomial]] is only well-defined in any ring with an apartness relation. Anything that depends on well-defined degrees of a polynomial, such as [[algebraic closure]], also is only well-defined for a ring with an apartness relation. 

### Classical sets

The [[classical sets]] are however still definable in coherent mathematics; they are sets $S$ equipped with an [[apartness relation]] such that for all elements $a \in S$ and $b \in S$, $a = b$ or $a \# b$. This is expressed by the sequent
$$a \in S, b \in S \vdash (a = b) \vee (a \# b)$$
This means that one could work in predicative [[classical mathematics]] (i.e. a [[Boolean category]]) by stipulating that every set is a classical set. 

Nonetheless, even without assuming the above, a lot of [[algebraic number theory]] is coherent because the rings and [[number fields]] studied are classical sets. 

## Predicates, subsets, and restricted separation

The [[axiom schema]] of [[restricted separation]] in the set theory axioms states that for each set $S$ and each predicate $x \in S \vdash P(x)$, one could construct 

* a set $\{x \in S \vert P(x)\}$ 
* a function $i:\{x \in S \vert P(x)\} \to S$ 
* a predicate $y \in \{x \in S \vert P(x)\}, z \in \{x \in S \vert P(x)\}, i(y) = i(z) \vdash y = z$
* a predicate $x \in R, \exists y \in \{x \in S \vert P(x)\}.x = i(y) \vdash P(x)$,
* a predicate $x \in R, P(x) \vdash \exists y \in \{x \in S \vert P(x)\}.x = i(y)$

This implies that $\{x \in S \vert P(x)\}$ is a [[subset]] of $S$ in the structural sense. 

Assuming that the ambient logic is [[coherent logic]], restricted separation automatically implies that the sets and functions form a [[coherent category]], since the [[poset]] of [[subsets]] of each set being a [[distributive lattice]] follows from the rules for [[coherent logic]] and restricted separation. 

## See also

* [[coherent logic]]
* [[foundations of mathematics]]
* [[constructive mathematics]]
* [[predicative mathematics]]
* [[classical mathematics]]
* [[geometric mathematics]]