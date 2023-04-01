
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

Every [[category]] $C$ gives rise to an _arrow category_ $Arr(C)$ such that the [[objects]] of $Arr(C)$ are the [[morphisms]] (or _arrows_, hence the name) of $C$.


## Definition

For $C$ any [[category]], its **arrow category** $Arr(C)$ is the category such that:

* an [[object]] $a$ of $Arr(C)$ is a [[morphism]] $a\colon a_0 \to a_1$ of $C$;
* a [[morphism]] $f\colon a \to b$ of $Arr(C)$ is a [[commutative square]]
  $$ \array {
     a_0 & \overset{f_0}\to & b_0 \\
     \llap{a}\downarrow & & \rlap{b}\downarrow \\
     a_1 & \underset{f_1}\to & b_1
     } $$
  in $C$;
* [[composition]] in $Arr(C)$ is given simply by placing commutative squares side by side to get a commutative oblong.

This is isomorphic to the [[functor category]]
$$
  Arr(C) := Funct(I,C) = [I,C] = C^I
$$
for $I$ the [[interval category]] $\{0 \to 1\}$.  $Arr(C)$ is also written $[\mathbf{2},C]$, $C^{\mathbf{2}}$, $[\Delta[1],C]$, or $C^{\Delta[1]}$, since $\mathbf{2}$ and $\Delta[1]$ (for the $1$-[[simplex]]) are common notations for the interval category.


## Properties

\begin{proposition}
The arrow category $Arr(C)$ is equivalently the [[comma category]] $(id/id)$ for the case that $id\colon C \to C$ is the [[identity functor]].
\end{proposition}
\begin{remark}
$Arr(C)$ plays the role of a [[directed homotopy theory|directed]] [[homotopy|path object]] for categories in that functors
$$
  X \to Arr(Y)
$$
are the same as [[natural transformations]] between functors between $X$ and $Y$.
\end{remark}

\begin{example}\label{SliceCategoriesAndArrowCategory}
**(arrow category is [[Grothendieck construction]] on [[slice categories]])**
\linebreak
For $\mathcal{S}$ any category, let
$$
  \mathcal{S}_{(-)}
  \,\colon\,
  \mathcal{S}
  \longrightarrow
  Cat
$$
be the [[pseudofunctor]] which sends

* an [[object]] $B \,\in\, \mathcal{S}$ to the [[slice category]] $\mathcal{S}_{/B}$,

* a [[morphism]] $f \colon B \to B'$ to the left [[base change]] [[functor]] $f_! \,\colon\, \mathcal{C}_{B} \to \mathcal{C}_{/B'}$ given by post-[[composition]] in $\mathcal{C}$.

The [[Grothendieck construction]] on this functor is the [[arrow category]] $Arr(\mathcal{S})$ of $\mathcal{S}$:

$$
  Arr(\mathcal{S})
  \;\;\;
    \simeq
  \;\;\;
  \int_{B \in \mathcal{S}}
  \mathcal{S}_{/B}
  \mathrlap{\,.}
$$

This follows readily by unwinding the definitions.
In the refinement to the [[Grothendieck construction for model categories]] (here: [[slice model categories]] and [[model structures on functors]]) this equivalence is also considered for instance in [Harpaz & Prasma (2015), above Cor. 6.1.2](Grothendieck+construction+for+model+categories#HarpazPrasma15).

The correponding [[Grothendieck fibration]] is also known as the *[[codomain fibration]]*.
\end{example}




## Related concepts

* [[path space object]]

* [[slice category]], [[undercategory]]

* [[arrow (∞,1)-category]]

* [[arrow (∞,1)-topos]]

* [[twisted arrow category]]


[[!redirects arrow category]]
[[!redirects arrow categories]]
[[!redirects category of morphisms]]
[[!redirects categories of morphisms]]
