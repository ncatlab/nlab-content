
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An _elliptic spectrum_ is a [[spectrum]] which [[Brown representability theorem|represents]] an [[elliptic cohomology theory]]. 

## Definition

For $E$ a [[ring spectrum]], write $E^\bullet(\ast)$ for its coefficient ring and generally $E^\bullet(X)$ for its [[generalized cohomology theory|generalized]] [[cohomology ring]] over any $X$.

+-- {: .num_defn #EllipticSpectrum}
###### Definition

An _elliptic spectrum_ is a [[triple]] consisting of 

1. an [[elliptic curve]] $A$ over the coefficient ring $E^\bullet(\ast)$;

1. an [[even cohomology theory|even]] [[periodic ring spectrum]] $E$; 

1. an [[equivalence]]

   $$
     Spec E^\bullet(BU(1)) \stackrel{\simeq}{\longrightarrow} Pic_A^0
   $$

   between the [[spectrum of a commutative ring|algebraic spectrum]] of the $E$-[[cohomology ring]] over the [[classifying space]] for [[complex line bundles]] (see at _[[complex oriented cohomology theory]]_) and the [[formal Picard group]] $Pic_A^0$ of $A$.

=--

This is due to ([Ando-Hopkins-Strickland01, def. 1.2](AndoHopkinsStrickland01)). See for instance also ([Gepner 05, def. 15](#Gepner05)).

+-- {: .num_remark #RoleOfFormalPicardScheme}
###### Remark
**(role of the [[formal Picard scheme]])**

Originally (and still in many or even most references), def. \ref{EllipticSpectrum} is stated with the [[formal Picard group]] $Pic_A^0$ replaced by the [[formal completion]] $\hat A$ of $A$ at its neutral element.

These two versions of the definition in itself are equivalent, since [[elliptic curves]] are self-[[dual abelian varieties]] equipped with a canonical [[isomorphism]] $\hat A \simeq Pic^0_A$exhibited by the [[Poincaré line bundle]].

But for the development of the theory, notably for application to [[equivariant elliptic cohomology]], for the relation of [[elliptic cohomology]] to [[loop group representations]] etc., it is crucial to understand that $E^\bullet(B U(1))$ is the space of [[sections]] of a [[line bundle]] over a (formal) [[moduli space]] of [[line bundles]] on, in turn, the elliptic curve, instead of directly on the elliptic curve itself.

Indeed, generally for $G$ a [[compact Lie group]], we have that $E^\bullet(B G)$ is the [[space of sections]] of the [[WZW model]]-[[line bundle]] for [[conformal blocks]] (the [[prequantum line bundle]] of the $G$-[[Chern-Simons theory]]) on the (formal) [[moduli space of flat connections]] on $G$-[[principal bundles]] over the elliptic curve. This is the central statement at _[[equivariant elliptic cohomology]]_. As the appearance of the [[WZW model]] here shows, this is also crucial for understanding the role of elliptic spectra in [[quantum field theory]]/[[string theory]], see at _[equivariant elliptic cohomology -- Interpretation in Quantum field theory/String theory](equivariant%20elliptic%20cohomology#InterpretationInQuantumFieldTheory)_ for more on this.

Moreover, understanding $Spec E^\bullet(BU(1))$ as being about [[moduli space of (higher) line bundles|moduli of line bundles]] on the elliptic curve is crucial for understanding the generalization of the concept of elliptic spectra, for instance to [[K3-spectra]]. This is indicated in the following table

[[!include moduli of higher lines -- table]]


=--



## Related concepts

* [[elliptic cohomology]], [[elliptic genus]], [[tmf]]

* [[Eilenberg-MacLane spectrum]]

* [[K3-spectrum]]


## References

The concept of elliptic spectrum was introduced in

* {#AndoHopkinsStrickland01} [[Matthew Ando]], [[Michael Hopkins]], [[Neil Strickland]], _Elliptic spectra, the Witten genus, and the theorem of the cube_, Inventiones Mathematicae, 146:595&#8211;687, 2001, DOI 10.1007/s002220100175 ([pdf](http://www.math.rochester.edu/people/faculty/doug/otherpapers/musix.pdf))

A brief review is for instance in  of 

* {#Gepner05} [[David Gepner]], section 1 of _[[Homotopy topoi and equivariant elliptic cohomology]]_, 2005.

Survey includes

* [[Jacob Lurie]], _[[A Survey of Elliptic Cohomology]]_

* [[Charles Rezk]], _Elliptic cohomology and elliptic curves_, Felix Klein Lectures, Bonn  2015 ([web](http://www.hcm.uni-bonn.de/fkl-rezk/))   


[[!redirects elliptic spectra]]