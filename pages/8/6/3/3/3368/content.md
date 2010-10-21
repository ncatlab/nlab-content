
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

An ordinary [[category]] is _[[idempotent complete category|idempotent complete]]_ , aka _Karoubi complete_ or _Cauchy complete_ , if every [[idempotent]] splits.  Since the splitting of an idempotent is a limit *or* colimit of that idempotent, any category with [[finitely complete category|all finite limits]] or [[finitely cocomplete category|all finite colimits]] is idempotent complete.

In an [[(∞,1)-category]] the idea is the same, except that the notion of *idempotent* is more complicated.  Instead of just requiring that $e\circ e = e$, we need an [[equivalence]] $e\circ e \simeq e$, together with higher coherence data saying that, for instance, the two derived equivalences $e\circ e\circ e \simeq e$ are equivalent, and so on up.  In particular, *being idempotent* is no longer a [[stuff, structure, property|property]] of a morphism, but *structure* on it.

It is still true that a splitting of an idempotent in an $(\infty,1)$-category is a limit or colimit of that idempotent (now regarded as a diagram with all its higher coherence data), but this limit is no longer a finite limit; thus an $(\infty,1)$-category can have all finite limits without being idempotent-complete.


## Definition

...

## Properties

The following properties generalize those of idempotent-complete 1-categories.

+-- {: .un_theorem}
###### Theorem

A [[small (∞,1)-category]] is idempotent-complete if and only if it is [[accessible (∞,1)-category|accessible]].

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, 5.5.3.6]].

=--

+-- {: .un_theorem}
###### Theorem

For $C$ a [[small (∞,1)-category]] and $\kappa$ a [[regular cardinal]], the [[(∞,1)-Yoneda embedding]] $C \to C' \hookrightarrow Ind_\kappa(C)$ with $C'$ the full subcategory on $\kappa$-[[compact object]]s exhibits $C'$ as the idempotent completion of $C$.

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, lemma 5.4.2.4]].

=--


## References

Section 4.4.5 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ 


[[!redirects idempotent complete (∞,1)-category]]
[[!redirects idempotent-complete (infinity,1)-category]]
[[!redirects idempotent-complete (∞,1)-category]]

[[!redirects idempotent-complete quasi-category]]
[[!redirects idempotent-complete quasi-categories]]
