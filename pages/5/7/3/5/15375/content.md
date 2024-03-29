
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A _normed field_ $K$ is a [[normed ring]] whose underlying [[ring]] is a [[field]].

If the product preserves the [[norm]] strictly (so that one has a _multiplicative norm_  or [[absolute value]] in that for all $f,g \in K$ we have the [[equality]] ${\vert f \cdot g\vert} = {\vert f\vert} \cdot {\vert g\vert}$ instead of just the [[inequality]] ${\vert f \cdot g\vert} \leq {\vert f\vert} \cdot {\vert g\vert}$) then one speaks of a _[[valued field]]_  (e.g. [Berkovich 09, def. 1.1.1](#Berkovich09)).

If the underlying [[normed group]] is a [[complete topological space]] then one speaks of a _[[complete field|complete normed field]]_.


## Examples

* Every [[field]] carries the trivial norm (which is [[non-archimedean field|non-archimedean]]), whose value is always $1$ (except that the norm of $0$ is $0$) and is complete with respect to this norm.  (In [[constructive mathematics]], either the field must be a [[discrete field]] or the norm must be allowed to take values in the [[lower real numbers]].)

* The field $\mathbb{R}$ of [[real numbers]] and the field $\mathbb{C}$ of [[complex numbers]], with their usual [[absolute value]] as the norm, are complete [[archimedean field|archimedian]] normed fields.

* For each [[prime number]] $p$, the field $\mathbb{Q}_p$ of $p$-[[adic numbers]] is a complete non-archimedean normed field with respect to the [[p-adic valuation]].

* The field $\mathbb{Q}$ of [[rational numbers]], with any of the norms in the two previous entries, is an incomplete normed field whose completion is $\mathbb{R}$ or $\mathbb{Q}_p$.


## Properties

### Relation to algebraic closure
 {#RelationToAlgebraicClosure}

The norm of a [[non-archimedean field]] extends uniquely to its [[algebraic closure]] and the completion of that with respect to this norm is still algebraically closed ([Bosch-Guntzer-Remmert 84, prop. 3.4.1.3](#BoschGuntzerRemmert84), [Berkovich 09, fact 1.1.4](#Berkovich09)).

For example the [[p-adic complex numbers]] $\mathbb{C}_p$ arise this way from the [[p-adic rational numbers]] $\mathbb{Q}_p$.


## Related concepts

* [[normed division algebra]]

[[!include analytic geometry ingredients -- table]]


## References

* {#Tornheim52} Leonard Tornheim, _Normed fields over the real and complex fields_, Michigan Math. J. Volume 1, Issue 1 (1952), 61-68. ([Euclid](http://projecteuclid.org/euclid.mmj/1028989727))

* {#BoschGuntzerRemmert84} S. Bosch, U. Guntzer, and R. Remmert, _Non-Archimedean analysis_, Grundlehren der Mathematischen Wissenschaften, vol. 261, Springer-Verlag, Berlin, 1984.

* {#Berkovich09} [[Vladimir Berkovich]], _Non-archimedean analytic spaces_, lectures at the _Advanced School on $p$-adic Analysis and Applications_, ICTP, Trieste, 31 August - 11 September 2009 ([pdf](http://www.wisdom.weizmann.ac.il/~vova/Trieste_2009.pdf))


[[!redirects normed field]]
[[!redirects normed fields]]

[[!redirects complete normed field]]
[[!redirects complete normed fields]]