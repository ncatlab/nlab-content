
> This page seems to follow [Johnstone 2002](#Johnstone02) in considering the [[Ore condition]] with respect to the full class of all morphisms. More generally see at *[[Ore set]]*.

----

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}

### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

In [[category theory]], the (right) **Ore condition** is a simple condition on the [[morphisms]] in a [[category]] $\mathcal{C}$ which ensure that [[sieves]] generated by [[singletons]] $\{ f\}$ behave well under [[pullback]]. It can be viewed as weaker form of the existence of [[pullbacks]] in $\mathcal{C}$.

## Definition

+-- {: .num_def #ore}
###### Definition
A [[category]] $\mathcal{C}$ is said to satisfy the (right) **Ore condition** if for any [[cospan]] [[diagram]]
$$
\array{
  & & A \\
  & & \downarrow\\
  B & \to & C
}
$$
there is an [[object]] $D$ and [[morphisms]] $D \to A, B$ such that the following [[commuting diagram|diagram commutes]]:
$$
\array{
  D & \to & A \\
  \downarrow & & \downarrow\\
  B & \to & C
}
$$
=--

## Properties

\begin{proposition}
When $S$ is a [[sieve]] generated by a [[singleton]] $\{ f\}$ then the pullback sieve $h^\ast (S)$ is [[inhabited set|nonempty]] provided $\mathcal{C}$ satisfies the Ore condition. More generally, a category $\mathcal{C}$ satisfies the Ore condition precisely when the collection of nonempty sieves forms a [[Grothendieck topology]] on $\mathcal{C}$ (cf. *[[atomic site]]*).
\end{proposition}

## Examples

\begin{example}
A category $\mathcal{C}$ obviously satisfies the Ore condition when it has [[pullbacks]].
\end{example}



\begin{example}
A [[presheaf topos]] $Set^{\mathcal{C}^{op}}$ is a *[[De Morgan topos]]* (see there for more) precisely if its [[site]] $\mathcal{C}$ satisfies the Ore condition.
\end{example}


\begin{remark}\label{RelationToAmalgamationProperty}
A category $\mathcal{C}$ satisfies the [[amalgamation property]] precisely if its [[opposite category]] ${\mathcal{C}^{op}}$ satifies the Ore condition. Since the former is an important property in [[model theory]], the De Morgan property is via the Ore condition dually bound to play a similar role.
\end{remark}

## Related entries

* [[atomic site]]

* [[De Morgan topos]]

* [[amalgamation property]]

## Reference

* {#Johnstone02} [[Peter Johnstone]], pp. 79, 1001 in: *[[Sketches of an Elephant]]* vols. I,II, Oxford (2002) 

[[!redirects right Ore condition in a category]]


