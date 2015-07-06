
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Russell\'s paradox
* table of contents
{: toc}

## Summary

**Russell's paradox** is a [[paradox]] of naive [[material set theory|material]] [[set theory]] that was first observed by [[Ernst Zermelo]] and then, indepedently, shortly afterwards by the logician [[Bertrand Russell]].  If one assumes a naive, full [[axiom of comprehension]], one can form the [[set]]

$$ R = \{ x | x \notin x \}. $$

One then asks: is $R\in R$?  If so, then $R\notin R$ by definition, whereas if not, then $R\in R$ by definition.  Thus we have both $R\in R$ and $R\notin R$, a [[contradiction]].


## Related ideas

Russell's paradox is closely related to the [[liar paradox]] ("this sentence is false"), to G&#246;del's [[incompleteness theorem]], and to the [[halting problem]] --- all use [[diagonalization]] to produce an object which talks about itself in a contradictory or close-to-contradictory way.

On the other hand, [[Cantor's paradox]] can be said to "[[beta-reduction|beta-reduce]]" to Russell's paradox when we apply [[Cantor's theorem]] to the supposed set of all sets. See [[Cantor's paradox]] for explanation.

Also related:

* [[Burali-Forti's paradox]]


## Resolutions
 {#Resolutions}

There are a number of possible resolutions of Russell's paradox.

* In _[[Principia Mathematica]]_ Russell himself introduced a concept of ""[[ramified types]] (maybe the earliest [[type theory]]) in order to rule out the paradoxical operations.

* The "[[classical mathematics|classical]]" solution, adopted in [[ZFC]] and thus by most mainstream mathematicians, is to restrict the axiom of [[comprehension]] so as to disallow the formation of the set $R$: one requires that the set being constructed be a subset of some already existing set.  The restricted axiom is usually given a different name such as the [[axiom of separation]].

* Essentially the same resolution is used in class theories such as [[NBG]].  Here we may write down the definition of $R$, but from $R \notin R$ we may conclude $R \in R$ only if we already know that $R$ is a set; the $x$ in the definition must be a set.  So we have no contradiction, but only a proof that $R$ is a [[proper class]].

* In the set theory called [[New Foundations]], the axiom of comprehension is restricted in a rather different way, by requiring the set-defining formula to be "stratifiable".  Since the formula $x\notin x$ is not stratifiable, the set $R$ cannot be formed.  A similar (but more complicated) resolution was developed by Russell himself in his theory of [[ramified type]]s.

* In most [[structural set theories]], there is no need to artificially restrict the set-formation rules: if sets cannot be elements of other sets, then the "definition" of $R$ is just a [[type]] error.  The same is true in other structural [[foundations|foundational systems]] such as (modern, non-Russellian) [[type theory]].  However, Russell's paradox can be recreated in structural foundations with inconsistent [[universes]] by constructing [[pure sets]] within them.

* Alternatively, one can change the underlying logic.  Passing to [[constructive logic]] does not help: although there is a seeming appeal to [[excluded middle]] (either $R\in R$ or $R\notin R$), without using excluded middle we can obtain that $R$ is both not in $R$ and not not in $R$, which is also a contradiction.  However, passing to [[linear logic]] (or even [[affine logic]]) does help: there is an unavoidable use of [[contraction rule|contraction]] in the paradox.  There exist consistent [[linear set theory|linear set theories]] with the full comprehension axiom, in which $R\in R$ implies $R\notin R$ and vice versa, but we can never get both $R\in R$ and $R\notin R$ at the same time to produce a paradox.

* Finally, and perhaps most radically, one can decide to *allow* contradictions, choosing to use a [[paraconsistent logic]].  There exist nontrivial paraconsistent set theories with full comprehension in which the set $R$ exists, being both a member of itself and not a member of itself.

## References

Zermelo's observation which is mentioned in a footnote of his 1908 paper on the well-ordering theorem is analyzed in

* B. Rang, W. Thomas, _Zermelo's Discovery of the "Russell Paradox"_ , Hist. Math. **9** no.1 (1981) pp.15-22.

Russell indicated the contradiction leading to the inconsistency of G. Frege's system of "Grundgesetze der Arithmetik" in a famous letter to the latter on June 16th 1902 which together with Frege's reply is reprinted pp.124-128 in

* J. van Heijenoort (ed.), _From Frege to G&#246;del - A Source Book in Mathematical Logic 1879-1931_ , Harvard UP 1967.

The first published account is presumably chapter X in

* B. Russell, _The Principles of Mathematics_ , Cambridge UP 1903.

Discussion of a paradox similar to Russell's in [[type theory]] with [[W-types]] is in 

* [[Thierry Coquand]], _The paradox of trees in Type Theory_ (1991) ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.39.1953))


category: paradox

[[!redirects Russell paradox]]
[[!redirects Russell Paradox]]
[[!redirects Russell's paradox]]
[[!redirects Russell's Paradox]]
[[!redirects Russell's paradox]]
[[!redirects Russell's Paradox]]
[[!redirects Russell\'s paradox]]
[[!redirects Russell\'s Paradox]]
