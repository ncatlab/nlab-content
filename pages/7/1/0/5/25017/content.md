
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
=--
=--

\tableofcontents

## Definition

A [[binary relation]] $R$ on a set $A$ is __tight__ if for all elements $a \in A$ and $b \in A$, $\neg R(a, b)$ implies that $a = b$. 

Every tight relation is a [[connected relation]]. Every connected [[symmetric relation]] is a tight relation. 

## Examples

* A [[tight apartness relation]] is an [[apartness relation]] which is tight. 

## Weakly tight relations

Sometimes in [[constructive mathematics]], what matters for a relation is not that the negation implies equality, but the negation implies the [[double negation]] of equality. Such a relation is called **weakly tight**. 

A [[binary relation]] $R$ on a set $A$ is __weakly tight__ if for all elements $a \in A$ and $b \in A$, $\neg R(a, b)$ implies that $\neg \neg (a = b)$. By intuitionistic [[contraposition]], this implies that for all elements $a \in A$ and $b \in A$, $\neg (a = b)$ implies that $\neg \neg R(a, b)$. 

Important examples of weakly tight relations include [[denial inequality]]. 

## In dependent type theory

An [[irreflexive relation]] $\sim$ with terms $a:A \vdash \mathrm{irr}(a):(a \sim a) \to \emptyset$ is tight if the canonical function
$$\mathrm{idtonotrel}(a, b):(a =_A b) \to ((a \sim b) \to \emptyset)$$
inductively defined by 
$$\mathrm{idtonotrel}(a, a)(\mathrm{refl}_A(a)) \equiv \mathrm{irr}(a):(a \sim a) \to \emptyset$$
is an [[equivalence of types]]
$$\mathrm{conn}(a, b):\mathrm{isEquiv}(\mathrm{idtonotrel}(a, b))$$

## See also

* [[connected relation]]
* [[tight inequality relation]]
* [[tight apartness relation]]

[[!redirects tight]]
[[!redirects tight relation]]
[[!redirects tight relations]]

[[!redirects weakly tight]]
[[!redirects weakly tight relation]]
[[!redirects weakly tight relations]]