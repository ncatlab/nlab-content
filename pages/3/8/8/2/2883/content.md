<div class="rightHandSide toc">
[[!include cohomology - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##

_&Eacute;tale cohomology_ is the [[abelian sheaf cohomology]] for [[sheaf|sheaves]] on the [[etale site]] of a [[scheme]] (which is an analog of the [[category of open subsets]] of a [[topological space]]).

## History ##

Etale cohomology was conceived by Artin, Deligne, [[Alexander Grothendieck|Grothendieck]] and Verdier in 1963. It was used by Deligne to prove the [[Weil conjecture]]s.

Some useful remarks on this are in the begining of

* Spencer Block, Review of Milne's _&Eacute;tale cohomology_ ([pdf](http://www.ams.org/bull/1981-04-02/S0273-0979-1981-14894-1/S0273-0979-1981-14894-1.pdf))

## Details ##

For $X$ a [[scheme]] the [[etale site]] $Et(X)$ is the [[category]] whose [[object]]s are [[etale morphism]]s $Spec R \to X$ and whose morphisms are commuting triangles of these. This category naturally carries a [[Grothendieck topology]] that makes it a [[site]].

The [[etale cohomology]] $H_{et}^\bullet(X,A)$ for $A \in Sh(Et(X), Ab)$ of $X$ is the [[abelian sheaf cohomology]] with respect to this site.
