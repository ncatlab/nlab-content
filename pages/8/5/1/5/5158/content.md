
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definitions

There are several things that one might mean by a "(possibly [[weak homotopy equivalence|weak]]) [[homotopy equivalence]] of [[toposes]] (or [[(∞,1)-toposes]])."   Some candidates are:

1. A [[geometric morphism]] that induces an [[equivalence]] of the [[fundamental ∞-groupoid of a locally ∞-connected (∞,1)-topos]], or more generally of [[shape of an (∞,1)-topos|shapes]].

1. A geometric morphism which induces an isomorphism on all [[nonabelian cohomology]] with coefficients in [[constant ∞-stacks]].

1. A geometric morphism which induces an [[isomorphism]] on all [[abelian sheaf cohomology]] with coefficients in [[locally constant sheaves|locally constant]] sheaves (of complexes) of [[abelian groups]], as well as [[nonabelian cohomology]] in dimension one (the most classical notion).

1. A geometric morphism which has an inverse up to "homotopy" in the classical sense of a map $E\times [0,1]\to F$, where since $E$ and $F$ are toposes, we have to incarnate $[0,1]$ as the topos $Sh([0,1])$.

Of these, the first three are arguably a notion of *weak* homotopy equivalence.

## Relationship between definitions.

The first two definitions are equivalent, since (viewing a topos $E$ equivalently as the $(\infty,1)$-topos of sheaves on the same [[site]], if necessary), a constant ∞-stack on $E$ is one of the form $LConst A$ for an ∞-groupoid $A$, and the cohomology of $E$ with coefficients in $LConst A$ is just $\pi_0(Hom_E(*,LConst A))$.  But when $E$ is locally $\infty$-connected, $\Pi_E$ is left adjoint to $LConst$, so this is the same as $\pi_0 Hom_{\infty Gpd}(\Pi_E(*),A) = Hom_{Ho(\infty Gpd)}(\Pi_\infty(E),A)$ by definition of $\Pi_\infty(E)$.  Thus, by the Yoneda lemma, a map of toposes induces an equivalence of fundamental ∞-groupoids, i.e. an isomorphism in $Ho(\infty Gpd)$, iff it induces an isomorphism on all such cohomology.  Since in the non--locally-$\infty$-connected case, the [[shape of an (infinity,1)-topos|shape]] is just the functor that would be represented by $\Pi_\infty(E)$ if it existed, the equivalence is even easier in that case.

These first two definitions also imply the third, since the abelian cohomology $H^n(E,A)$ with coefficients in an abelian sheaf $A$ can be identified with nonabelian cohomology in the locally constant stack $B^n A$ which is the $n$-fold [[delooping]] of $A$, and locally constant stacks on $E$ are represented by maps out of $\Pi_\infty(E)$.

+--{: .query}
[[Mike Shulman]]: There's something a little funny here about "constant" versus "locally constant," but I don't have time to figure it out now.  Maybe someone else can explain it.
=--

Conversely, it is proven in Artin-Mazur that (in our language) a geometric morphism of 1-topoi satisfying the third definition necessarily induces isomorphisms on all homotopy progroups.  (The idea is essentially that nonabelian cohomology is controlled by abelian cohomology with local coefficients, via [[Postnikov tower in an (infinity,1)-category|Postnikov decompositions]].)   In the locally $\infty$-connected case, this is equivalent to inducing an equivalence of fundamental $\infty$-groupoids---the first definition.  Thus, at least for locally $\infty$-connected 1-topoi, the first three definitions are all equivalent.

+--{: .query}
[[Mike Shulman]]: Possibly in the non--locally-$\infty$-connected case, the third definition is weaker, since a map of pro-$\infty$-groupoids can induce an isomorphism on all homotopy progroups without being an equivalence?  It's also not immediately obvious whether the result is also true as stated for all $(\infty,1)$-toposes.

I also seem to recall that the last notion of a "paths homotopy equivalence" implies the first few, but I don't remember why.
=--

## Adjunctions induce homotopy equivalences

One important thing to note is that any [[adjunction]] in the [[2-category]] [[Topos]] induces a homotopy equivalence in any of the above senses.  For the first (hence also the second and third) sense, we just observe that $\Pi_\infty$ is 2-functorial, whereas it lands in the (∞,1)-category ?Gpd where all 2-morphisms are invertible; hence adjunctions get sent to adjunctions, which are necessarily equivalences.

For the final definition, we note that has [[weighted limit|tensors]] with the [[interval category]], that are given by [[cartesian product]] with sheaves on the [[Sierpinski space]] $\Sigma$.  Thus, a natural transformation between two geometric morphisms $E\to F$ is the same as a single geometric morphism 
$E\times Sh(\Sigma)\to F$.  Now just pick a map $[0,1]\to \Sigma$ that doesn't identify the endpoints, like the classifying map of $[0,\frac1 2]$, to get an actual "homotopy" between the same two geometric morphisms.  Hence, any 2-morphism in $Topos$ gives a homotopy, so any adjunction gives a homotopy equivalence.

In particular, this means that any [[local geometric morphism]] or [[totally connected geometric morphism]] is a homotopy equivalence.

## References

* M. Artin and B. Mazur, 1969, _Etale homotopy_, No. 100, Lecture Notes in Maths., 
Springer-Verlag, Berlin.

[[!redirects homotopy equivalence of toposes]]
[[!redirects homotopy equivalence of topoi]]
[[!redirects homotopy equivalences of toposes]]
[[!redirects homotopy equivalences of topoi]]
[[!redirects topos homotopy equivalence]]
[[!redirects topos homotopy equivalences]]
[[!redirects weak homotopy equivalence of toposes]]
[[!redirects weak homotopy equivalence of topoi]]
[[!redirects weak homotopy equivalences of toposes]]
[[!redirects weak homotopy equivalences of topoi]]
[[!redirects topos weak homotopy equivalence]]
[[!redirects topos weak homotopy equivalences]]
