
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

+-- {: .un_defn}
###### Definition

A [[functor]] $F:C\to D$ is **conservative** if it is "isomorphism-reflecting", i.e. if $g:a\to b$ is a [[morphism]] in $C$ such that $F(g)$ is an [[isomorphism]] in $D$, then $g$ is an isomorphism in $C$.

=--

+-- {: .un_remark}
###### Remark

Sometimes conservative functors are assumed to be [[faithful functor|faithful]] as well.  If $C$ has, and $F$ preserves, [[equalizer]]s, then conservativity implies faithfulness.

=--

See [[conservative morphism]] for a generalization to an arbitrary [[2-category]].

## Properties

+-- {: .un_prop}
###### Proposition

A conservative functor [[reflected limit|reflects]] all [[limit]]s and [[colimit]]s that it [[preserved limit|preserves]].

=--

+-- {: .proof}
###### Proof

Let $K : J \to C$ be a [[diagram]] in $X$ whose limit $\lim K$ exists and such that $\lim F\circ K \simeq F \lim K$. Then if $const_\theta \to K$ is a [[cone]] in $F$ that is sent to a limiting cone $F const_\theta$ in $D$, then by the [[universal property]] of the limit in $D$ the morphism $F( const_\theta \to \lim K)$ is an isomorphism in $D$, hence must have been an isomorphism in $C$, hence $const_\theta$ must have been a limiting cone in $C$.

The arguments for colimits is analogous.
=--

## Literature

* Geun Bin Im, [[George Maxwell Kelly]], _Some remarks on conservative functors with left adjoints_,  J. Korean Math. Soc. __23__ (1986),  no. 1, 19&#8211;33, [MR87i:18002b](http://www.ams.org/mathscinet-getitem?mr=843247), [pdf](http://mathnet.kaist.ac.kr/mathnet/thesis_file/JKMS-23-1-19-33.pdf); _On classes of morphisms closed under limits_, J. Korean Math. Soc. __23__ (1986), no. 1, 1&#8211;18, _Adjoint-triangle theorems for conservative functors_, Bull. Austral. Math. Soc. __36__ (1987),  no. 1, 133&#8211;136, [MR88k:18005](http://www.ams.org/mathscinet-getitem?mr=897429), [doi](http://dx.doi.org/10.1017/S000497270002637X) 

* ...

[[!redirects conservative functors]]
