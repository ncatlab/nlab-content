
#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn}
###### Definition

A morphism $f \colon \mathbf{A} \to \mathbf{B}$ of [[E-∞ rings]] is an _étale morphism_ if the underlying homomorphism of [[commutative rings]] $\pi_0 f\colon \pi_0 \mathbf{A}\to \pi_0 \mathbf{B}$ is an [[étale morphism]], and the map $\pi_n(A) \otimes_{\pi_0(A)} \pi_0(B) \to \pi_n(B)$ is an isomorphism of abelian groups for every integer $n$.

=--

([Lurie, def.7.5.1.4](#Lurie))

## Properties

&#233;tale morphisms of underlying rings lift essentially uniquely to &#233;tale morphisms of [[E-∞ rings]]:

+-- {: .num_prop #EssentiallyUniqueLiftsFromOrdinaryRings}
###### Proposition

For $\mathbf{A}$ an [[E-∞ ring]] and $\pi_0 \mathbf{A} \to B$ a homomorphism to an ordinary ring $B$, then there is an essentially unique $E_\infty$-ring $\mathbf{B}$ with $\pi_0 \mathbf{B} \simeq B$ and &#233;tale morphism $\mathbf{A}\to \mathbf{B}$.

=--

([Lurie, theorem 7.5.0.6](#Lurie))

+-- {: .num_remark }
###### Remark

Proposition \ref{EssentiallyUniqueLiftsFromOrdinaryRings} is a central ingredient in the characterization of the moduli stack of [[derived elliptic curves]] as having underlying it the ordinaty [[moduli stack of elliptic curves]].

=--

+-- {: .num_remark #LocalizationOfRings}
###### Remark
**(localization of $E_\infty$-rings)**

Proposition \ref{EssentiallyUniqueLiftsFromOrdinaryRings} serves to lift [[localization of rings]] from rings to $E_\infty$-rings: for $\mathbf{A}$ an [[E-∞ ring]] and $a\in \pi_0 A$ an element, then the map $\pi_0 \mathbf{A} \to (\pi_0 \mathbf{A})[a^{-1}]$ of [[localization of a ring]] away from $a$ lifts to yield an [[E-∞ ring]] $\mathbf{A}[a^{-1}]$ with &#233;tale morphism $\mathbf{A} \to \mathbf{A}[a^{-1}]$. See also at _[[localization of a module]]_ for more on this.

=--

## References

* {#Lurie} [[Jacob Lurie]], _[[Higher Algebra]]_

[[!redirects étale morphisms of E-∞ rings]]

[[!redirects etale morphism of E-∞ rings]]