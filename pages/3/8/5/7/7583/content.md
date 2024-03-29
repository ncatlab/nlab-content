
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Exhaustive categories

* table of contents
{: toc}

## Idea

A [[category]] is **exhaustive** if it has [[colimits]] of (transfinite) sequences of [[monomorphisms]] which interact well with [[pullbacks]].

## Definition

Given a transfinite sequence 
$$ A_0 \to A_1 \to \cdots $$
(continuing through $A_\alpha$ for all $\alpha\lt\kappa$, where $\kappa$ is some limit [[ordinal]]) for which each transition map $A_\alpha \to A_\beta$ is a [[monomorphism]], if $A_\kappa$ is a colimit of this sequence (a [[transfinite composition]]) we call it a **transfinite union**.

A category $C$ is **exhaustive** if one, hence both, of the following two equivalent conditions hold.

1. $C$ has transfinite unions which are stable under pullback and for which the coprojections $A_\alpha \to A_\kappa$ are also monomorphisms.

1. $C$ has transfinite unions, and given any diagram
   $$\array{
     B_0 & \to & B_1 & \to & \cdots & \to & B_\kappa\\
     \downarrow && \downarrow &&&& \downarrow\\
     A_0 & \to & A_1 & \to & \cdots & \to & A_\kappa\\
   }$$
   in which the bottom row is a transfinite union and for each $\alpha\lt\beta\lt\kappa$, the square
   $$ \array{ B_\alpha & \to & B_\beta \\
     \downarrow && \downarrow \\
     A_\alpha & \to & A_\beta } $$
   is a [[pullback]] (hence $B_\alpha \to B_\beta$ is also monic), then the top row is a transfinite union (i.e. a colimit diagram) if and only if for all $\alpha\lt\kappa$ the square
   $$ \array{ B_\alpha & \to & B_\kappa \\
     \downarrow && \downarrow \\
     A_\alpha & \to & A_\kappa } $$
   is a pullback.  (In other words, transfinite unions are [[van Kampen colimits]].)

Note that half of the second condition is simply that the colimits in the first condition are stable under pullback.  One may obtain various weaker notions by restricting the allowable values of $\kappa$.

We will prove the equivalence of these two characterizations in Propositions \ref{CoprojectionsMonic} and \ref{AlternativeCharacterization} below.


## Examples

* The category [[Set]] is easily verified to be exhaustive.

* Since limits and colimits in [[category of presheaves|presheaf categories]] are pointwise, any presheaf category $[D^{op},Set]$ is also exhaustive.

* Since the condition involves only colimits and finite limits, it is preserved by any [[reflective subcategory|left exact localization]].  Thus, every [[Grothendieck topos]] is exhaustive.

## Properties

We first prove the equivalence of the above two definitions.

+-- {: .num_prop #CoprojectionsMonic}
###### Proposition
In a category which satisfies the second definition above, given a transfinite union
$$ A_0 \to A_1 \to \cdots \to A_\kappa$$
(so that $A_\alpha \to A_\beta$ is monic for all $\alpha\lt\beta\lt\kappa$), the coprojections $A_\alpha\to A_\kappa$ are also monic.
=--
+-- {: .proof}
###### Proof
For a fixed $\alpha$, consider the diagram
$$\array{
  A_0 & \to & A_1 & \to & \cdots & \to & A_\alpha & \to & A_\alpha & \to & \cdots & \to & A_\alpha\\
  \downarrow && \downarrow &&&& \downarrow && \downarrow &&&& \downarrow\\
  A_0 & \to & A_1 & \to & \cdots & \to & A_\alpha & \to & A_{\alpha+1} & \to & \cdots & \to & A_\kappa\\
}$$
It is easy to see that each intermediate square is a pullback, and of course the top row is a colimit.  Thus, in particular the square
$$\array{ A_\alpha & \to & A_\alpha \\
  \downarrow && \downarrow\\
  A_\alpha & \to & A_\kappa}$$
is a pullback, i.e. $A_\alpha\to A_\kappa$ is monic.
=--

+-- {: .num_prop #AlternativeCharacterization}
###### Proposition
Suppose $C$ satisfies the first condition above, i.e. it has pullback-stable transfinite unions for which the coprojections are also monic.  Then $C$ also satisfies the second condition above.
=--
+-- {: .proof}
###### Proof
It remains to show that given a diagram
$$\array{
  B_0 & \to & B_1 & \to & \cdots & \to & B_\kappa\\
  \downarrow^{f_0} && \downarrow^{f_1} &&&& \downarrow^{f_\kappa}\\
  A_0 & \to & A_1 & \to & \cdots & \to & A_\kappa\\
}$$
in which both rows are transfinite compositions of monomorphisms and the squares
$$ \array{ B_\alpha & \to & B_\beta \\
  \downarrow^{f_\alpha} && \downarrow^{f_\beta} \\
  A_\alpha & \to & A_\beta } $$
are pullbacks, also the squares
$$ \array{ B_\alpha & \to & B_\kappa \\
  \downarrow^{f_\alpha} && \downarrow^{f_\kappa} \\
  A_\alpha & \to & A_\kappa } $$
are pullbacks.

Fix an $\alpha\lt\kappa$, and suppose given $g\colon X\to B_\kappa$ such that $f_\kappa g$ factors through $A_\alpha$; we want to show that $g$ factors through $B_\alpha$.  Pulling back the $B$-colimit along $g$ and the $A$-colimit along $f_\kappa g$, we obtain another morphism of transfinite unions:
$$\array{
  g^*B_0 & \to & g^*B_1 & \to & \cdots & \to & X\\
  \downarrow && \downarrow &&&& \downarrow^{1_X}\\
  (f_\kappa g)^* A_0 & \to & (f_\kappa g)^* A_1 & \to & \cdots & \to & X\\
}$$
and it is easy to verify, by the pasting law for pullbacks, that each square
$$ \array{ g^* B_\beta & \to & g^* B_\gamma \\
  \downarrow^{f_\beta} && \downarrow^{f_\gamma} \\
  (f_\kappa g)^* A_\beta & \to & (f_\kappa g)^* A_\gamma } $$
is a pullback for $\beta\lt\gamma\lt\kappa$.  However, since $f_\kappa g$ factors through $A_\alpha$, the morphism $(f_\kappa g)^* A_\beta \to (f_\kappa g)^* A_\gamma$ is split epic whenever $\alpha\lt\beta\lt\gamma$, hence (since it is also monic) an isomorphism.  Thus, in this case so is its pullback $g^* B_\beta \to g^* B_\gamma$.  Since the coprojections into a transfinite composite of a sequence that eventually consists of isomorphisms are also eventually isomorphisms, $g^* B_\alpha \to X$ is an isomorphism; hence $g$ factors through $B_\alpha$ as desired.
=--

Exhaustiveness also interacts well with other [[exactness properties]]:

+-- {: .num_prop #FinInfExtensive}
###### Proposition
If an exhaustive category is also finitary [[extensive category|extensive]], then it is infinitary extensive.
=--
+-- {: .proof}
###### Proof
A coproduct of cardinality $\kappa$ can be constructed using transfinite compositions and finite coproducts:
$$ \sum_{\alpha\lt 0} A_\alpha \to \sum_{\alpha\lt 1} A_\alpha \to \sum_{\alpha\lt 2} A_\alpha \to \cdots \to \sum_{\alpha\lt \kappa} A_\alpha $$
Finitary extensivity implies that all the transition maps are monic, so that these transfinite composites exist in an exhaustive category.  Pullback-stability of coproducts follows easily from pullback-stability of transfinite unions and of finite coproducts.  Finally, it is known (see [[extensive category]]) that if finite coproducts exist and are disjoint, then any infinite coproducts which exist are also disjoint.
=--

Colimits in an exhaustive category preserve finite limits.

+-- {: .num_lemma #UnionsPreserveIntersections}
###### Lemma
In an exhaustive category, if $X$ is the $\kappa$-indexed transfinite union of a sequence $(A_\alpha)_{\alpha\lt\kappa}$ and also a sequence $(B_\alpha)_{\alpha\lt\kappa}$, then it is also the transfinite union of the sequence $(A_\alpha\cap B_\alpha)_{\alpha\lt\kappa}$ (the [[intersection]] being taken as [[subobjects]] of $X$).
=--
+-- {: .proof}
###### Proof
Since transfinite unions are stable under pullback, $X$ is the colimit of the $(\kappa\times\kappa)$-indexed diagram $(A_\alpha\cap B_\beta)_{\alpha\lt\kappa, \beta\lt\kappa}$.  But $\kappa$ is a [[filtered category]], so its diagonal functor is [[final functor|final]].
=--

+-- {: .num_prop #UnionsPreservePullbacks}
###### Proposition
In an exhaustive category, given a pullback diagram of $\kappa$-indexed transfinite sequences of monomorphisms:
$$ \left(\array{ A_\alpha & \to & B_\alpha \\
    \downarrow && \downarrow\\
    C_\alpha & \to & D_\alpha }\right)_{\alpha\lt\kappa} $$
the induced square of colimits:
$$ \array{ A_\kappa & \to & B_\kappa \\
    \downarrow && \downarrow\\
    C_\kappa & \to & D_\kappa } $$
is also a pullback.
=--
+-- {: .proof}
###### Proof
Define $P$ so that the following square is a pullback:
$$ \array{ P & \overset{f}{\to} & B_\kappa \\
    ^g\downarrow && \downarrow\\
    C_\kappa & \to & D_\kappa } $$
Since pullbacks preserve transfinite unions, $P$ is the transfinite union of the sequnece $(f^* B_\alpha)_{\alpha\lt\kappa}$ and also the sequence $(g^* C_\alpha)_{\alpha\lt\kappa}$.  Thus, by Lemma \ref{UnionsPreserveIntersections}, $P$ is also the transfinite union of $(f^* B_\alpha\cap g^* C_\alpha)_{\alpha\lt\kappa}$.  However, using the fact that the inclusions $D_\alpha \to D_\kappa$ are monic, it is straightforward to verify that
$$f^* B_\alpha\cap g^* C_\alpha \cong B_\alpha \times_{D_\alpha} C_\alpha \cong A_\alpha.$$
Thus, $P$ is the transfinite union of $(A_\alpha)_{\alpha\lt\kappa}$, hence $P\cong A_\kappa$.
=--

+-- {: .num_cor #UnionsPreserveMonos}
###### Corollary
In an exhaustive category, transfinite unions preserve monomorphisms.  That is, given a transformation $(A_\alpha \to B_\alpha)_{\alpha\lt\kappa}$ of transfinite sequences of monomorphisms which is pointwise monic, also the induced map on colimits $A_\kappa\to B_\kappa$ is monic.
=--


## Related pages

* [[exactness property]]

## References

* The name "exhaustive category" is a coinage; there seems to be no established name in the literature for this exactness property.  See [this MO question](http://mathoverflow.net/questions/93567/exactness-for-sequential-unions-of-monomorphisms).

[[!redirects exhaustive category]]
[[!redirects exhaustive categories]]
