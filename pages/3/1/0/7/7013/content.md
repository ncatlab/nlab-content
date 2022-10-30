
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

An [[(∞,1)-category]] $C$ has [[finite limit|finite]] [[(∞,1)-limits]] if it has a [[terminal object in a quasi-category|terminal object]] and for every [[object]] $x \in X$, the [[over-(∞,1)-category]] $C_{/x}$ has finite [[products]]. 

We say that such a $C$ is **locally cartesian closed** if moreover $C_{/x}$ is a [[cartesian closed (∞,1)-category]] for every object $x$.  This is equivalent to asking that the pullback functor $f^*\colon C_{\y} \to C_{\x}$, for any $f\colon x\to y$ in $C$, has a right adjoint $\Pi_f$.

## Examples

* Every (Grothendieck) [[(∞,1)-topos]] is locally cartesian closed.  This follows from the [[universal colimit|universality of colimits]] and the [[adjoint functor theorem]].

## Properties

### Internal logic

The [[internal logic]] of locally cartesian closed $(\infty,1)$-categories is conjectured ([Joyal2011](#Joyal)) to be a sort of [[homotopy type theory]] (specifically, that with intensional [[identity types]] and [[dependent products]]).

See also [[internal logic of an (∞,1)-topos]].

### Presentations
 {#Presentations}

The following theorem should be compared with the fact that every [[locally presentable (∞,1)-category]] admits a presentation by a [[Cisinski model category]], indeed by a [[left Bousfield localization]] of a [[global model structure on simplicial presheaves]].

+-- {: .num_theorem #Presentations}
###### Theorem
For a locally presentable $(\infty,1)$-category $C$, the following are equivalent.

1. $C$ is locally cartesian closed.
1. Colimits in $C$ are stable under pullback.
1. $C$ admits a presentation by a [[right proper model category|right proper]] [[Cisinski model category]].
1. $C$ admits a presentation by a right proper left Bousfield localization of an injective model category of simplicial presheaves.

=--
+-- {: .proof}
###### Proof
Since left adjoints preserve colimits, the first condition implies the second.  The converse holds by the [[adjoint functor theorem]] since each slice of $C$ is locally presentable.

Suppose $M$ is a right proper Cisinski model category.  Then pullback along a fibration preserves cofibrations (since they are the monomorphisms) and weak equivalences (since $M$ is right proper).  Since $M$ is a locally cartesian closed 1-category, pullback also has a right adjoint, so it is a left Quillen functor, and hence preserves homotopy colimits.  Thus the third condition implies the second.

Clearly the fourth condition implies the third, so it suffices to show that the second condition implies the fourth.  For that, see [this blog comment](http://golem.ph.utexas.edu/category/2012/05/the_mysterious_nature_of_right.html#c041306) by Denis-Charles Cisinski.
=--


## Related concepts

* [[cartesian closed category]], [[locally cartesian closed category]]

* [[cartesian closed functor]], [[locally cartesian closed functor]]

* [[cartesian closed model category]], [[locally cartesian closed model category]]

* [[cartesian closed (∞,1)-category]], **locally cartesian closed (∞,1)-category**

## References

* [[André Joyal]], _Remarks on homotopical logic_, Oberwolfach (2011) ([pdf](http://hottheory.files.wordpress.com/2011/06/report-11_2011.pdf#page=19))
 {#Joyal}

[[!redirects locally cartesian closed (∞,1)-category]]
[[!redirects locally cartesian closed (infinity,1)-categories]]
[[!redirects locally cartesian closed (∞,1)-categories]]
