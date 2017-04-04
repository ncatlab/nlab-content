
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
* automatic table of contents goes here
{:toc}

## Idea

The generalization of the notion of [[flat functor]] from [[category theory]] to [[(∞,1)-category theory]].

## Definition

As for 1-categorical flat functors, there is a general definition of flat functors that restricts, in the case when [[finite limits]] exist, to the condition that these are preserved.

+-- {: .un_defn}
###### Definition

For $\kappa$ a [[regular cardinal]], an [[(∞,1)-functor]] $F : C \to D$ is **$\kappa$-flat**, if, when modeled as a morphism of [[quasicategories]], for any [[left Kan fibration]] $D' \to D$ with $D'$ a $\kappa$-[[cofiltered (∞,1)-category]], the [[pullback]] $C' := C \times_D D'$ (in [[sSet]]) is also $\kappa$-cofiltered.

If $\kappa = \omega$ then we just say $F$ is **flat**.

=--

The dual of this is [[Higher Topos Theory|HTT, def. 5.3.2.1]], under the name "$\kappa$-right exact".  But in 1-category theory, the terminology "left/right exact" is almost universally reserved for the case when finite limits/colimits *do* exist, so we continue that tradition in the $\infty$-case.  We do have:

+-- {: .un_prop}
###### Proposition

If $C$ has $\kappa$-small [[limits]], then $F$ is $\kappa$-flat precisely if it preserves these $\kappa$-small limits.

In particular, if $C$ has all [[finite (infinity,1)-limit|finite limits]], then $F$ is flat precisely if it preserves these.

=--

The dual of this is [[Higher Topos Theory|HTT, prop. 5.3.2.9]].

## Properties

+-- {: .un_prop}
###### Proposition

1. $\kappa$-flat $(\infty,1)$-functors are closed under composition.

1. Every [[(∞,1)-equivalence]] is $\kappa$-flat.

1. An $(\infty,1)$-functor equivalent (in the [[(∞,1)-category of (∞,1)-functors]]) to a $\kappa$-flat one is itsels $\kappa$-flat.

=--

This is [[Higher Topos Theory|HTT, prop. 5.3.2.4]].

## Internal flatness

For 1-categories, there are two notions of [[flat functor]]: the above corresponds to the "representable" one, while (for functors valued in a [[topos]]) there is also a notion of "internal flatness" (and a notion of "covering flatness" that generalizes them both.  I do not know whether internally-flat or covering-flat $(\infty,1)$-functors have been defined, but the following shows that left exact $(\infty,1)$-functors valued in an $(\infty,1)$-topos, at least, satisfy a condition that ought to characterize internally-flat ones.

+-- {: .un_prop}
###### Proposition
If $C$ is an $(\infty,1)$-category with finite limits, $D$ is an $(\infty,1)$-topos, and $F:C\to D$ preserves finite limits, then its Yoneda extension $\mathcal{P}(C) \to D$ also preserves finite limits.
=--

This is [[Higher Topos Theory|HTT, prop. 6.1.5.2]].


## Related concepts

* [[flat functor]]
* [[excisive (∞,1)-functor]]

## References

Section 5.3.2 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ 

[[!redirects flat (infinity,1)-functor]]
[[!redirects flat (∞,1)-functor]]

[[!redirects flat (infinity,1)-functors]]
[[!redirects flat (∞,1)-functors]]

[[!redirects exact (infinity,1)-functor]]
[[!redirects exact (∞,1)-functor]]

[[!redirects exact (infinity,1)-functors]]
[[!redirects exact (∞,1)-functors]]

[[!redirects left exact (∞,1)-functor]]
[[!redirects left exact (infinity,1)-functor]]

[[!redirects left exact (infinity,1)-functors]]
[[!redirects left exact (∞,1)-functors]]

[[!redirects right exact (∞,1)-functor]]
[[!redirects right exact (infinity,1)-functor]]

[[!redirects right exact (infinity,1)-functors]]
[[!redirects right exact (∞,1)-functors]]
