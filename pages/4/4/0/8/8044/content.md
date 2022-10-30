
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

## Idea

**Russell's paradox** is a famous [[paradox]] of [[set theory]][^material] that was first observed in 1902 by [[Ernst Zermelo]] and then, independently, shortly afterwards by the logician [[Bertrand Russell]]. The paradox received instantly wide attention as it lead to a contradiction in Frege's monumental "[Foundations of Arithmetic](#Frege03)" (1893/1903) whose second volume was just about to go to print when Frege was informed about the inconsistency by Russell.

The paradox entangles a concept with its own extension in a **vicious circle**. The attempt to overcome this _circularity in set formation_ had a huge impact on subsequent forms of axiomatic set theory and in the aftermath mathematical logic became heavily focussed on consistency proofs for fully specified formal theories: the paradoxes triggered a shift in the foundation of mathematics away from the mathematics to the foundation itself.

[^material]: naive [[material set theory]] that is!

## Statement

>Doch zur Sache selbst! Herr Russell hat einen Widerspruch aufgefunden, der nun dargelegt werden mag. Frege ([1903](#Frege03), p.253)

If one assumes a naive, full [[axiom of comprehension]], one can form the [[set]]

$$ R = \{ x | x \notin x \}. $$

One then asks: is $R\in R$?  If so, then $R\notin R$ by definition, whereas if not, then $R\in R$ by definition.  Thus we have both $R\in R$ and $R\notin R$, a [[contradiction]].


## Related ideas

Russell's paradox is closely related to the classical [[liar paradox]] ("this sentence is false"), to G&#246;del's [[incompleteness theorem]], and to the [[halting problem]] --- all use a [[diagonalization argument]] to produce an object which talks about itself in a contradictory or close-to-contradictory way.

On the other hand, [[Cantor's paradox]] can be said to "[[beta-reduction|beta-reduce]]" to Russell's paradox when we apply [[Cantor's theorem]] to the supposed set of all sets. See [[Cantor's paradox]] for explanation.

Also related:

* [[Burali-Forti's paradox]]


## Resolutions
 {#Resolutions}

There are a number of possible resolutions of Russell's paradox.

* Russell himself (1903,1908,1910) proposed the introduction of [[type theory]] as a solution e.g. in _[[Principia Mathematica]]_ (1910) an intricate system of [[ramified types]] tracks the variables of propositional functions in order to prevent circular propositions. This is inspired by Poincar&#233;'s ideas on [[predicative mathematics|impredicativity]] and can be viewed as a radical generalisation of Frege's ontological distinction between an argument as a satured object and a function or concept as an unsaturated object.

* The "[[classical mathematics|classical]]" solution, adopted in [[ZFC]] and thus by the mathematical "mainstream", is to restrict the axiom of [[comprehension]] so as to disallow the formation of the set $R$: one requires that the set being constructed be a subset of some already existing set.  The restricted axiom is usually given a different name such as the [[axiom of separation]].

* Another solution is to distinguish between sets and proper [[class|classes]] (= collections that are "too big" to be sets) as e.g. in [[NBG]] "set" theory.[^Cantor]  Here we may write down the definition of $R$, but from $R \notin R$ we may conclude $R \in R$ only if we already know that $R$ is a set; the $x$ in the definition must be a set.  So we have no contradiction, but only a proof that $R$ is a [[proper class]].

[^Cantor]: This solution proposed by J. von Neumann in the 1920s can be viewed as related to ideas of G. Cantor. The latter knew about similar phenomena concerning "the set of all sets" (in fact, Russell hit upon the paradox in a reflection on Cantor's proof of the inexistence of a largest cardinal number), and had already pointed out in 1885 in a review of Frege's "Grundlagen der Arithmetik" that not every concept has an extension. Therefore Cantor proposed in letters to Dedekind and Jourdain to differentiate between _'consistent multiplicities'_ ("compossible" multiplicities one could say) where things can coexist or compose to a consistent whole - 'ensemble' (fr.) which correspond to sets in the usual sense and, as completed collections, can in turn be elements in other sets, from _'inconsistent multiplicities'_ whose elements cannot consistently completed to a whole and cannot be member of other collections due to this lack of 'unity'.  

* In the set theory called [[New Foundations]], the axiom of comprehension is restricted in a rather different way, by requiring the set-defining formula to be "stratifiable".  Since the formula $x\notin x$ is not stratifiable, the set $R$ cannot be formed.  This related to Russell's ideas on [[ramified types]].

* In most [[structural set theories]], the featurelessness of the elements of the structural sets secures the consistency of set formation. If sets cannot be elements of other sets, then the "definition" of $R$ is just a [[type]] error. The same is true in other structural [[foundations|foundational systems]] such as (modern, non-Russellian) [[type theory]].  However, Russell's paradox can be recreated in structural foundations with inconsistent [[universes]] by constructing [[pure sets]] within them.

* Alternatively, one can change the underlying logic.  Passing to [[constructive logic]] does not help: although there is a seeming appeal to [[excluded middle]] (either $R\in R$ or $R\notin R$), without using excluded middle we can obtain that $R$ is both not in $R$ and not not in $R$, which is also a contradiction.  However, passing to [[linear logic]] (or even [[affine logic]]) does help: there is an unavoidable use of [[contraction rule|contraction]] in the paradox.  There exist consistent [[linear set theory|linear set theories]] with the full comprehension axiom, in which $R\in R$ implies $R\notin R$ and vice versa, but we can never get both $R\in R$ and $R\notin R$ at the same time to produce a paradox.

* Finally, and perhaps most radically, one can decide to *allow* contradictions, choosing to use a [[paraconsistent logic]].  There exist nontrivial paraconsistent set theories with full comprehension in which the set $R$ exists, being both a member of itself and not a member of itself.

## References

Zermelo's observation which is mentioned in a footnote of his 1908 paper on the [[well-ordering theorem]] is analyzed in

* B. Rang, W. Thomas, _Zermelo's Discovery of the "Russell Paradox"_ , Hist. Math. **9** no.1 (1981) pp.15-22.

Russell indicated the contradiction leading to the inconsistency of G. Frege's system of "Grundgesetze der Arithmetik" in a famous letter to the latter on June 16th 1902 which together with Frege's reply is reprinted pp.124-128 in

* J. van Heijenoort (ed.), _From Frege to G&#246;del - A Source Book in Mathematical Logic 1879-1931_ , Harvard UP 1967.

For an account of Russell's encounter with the paradox:

* I. Grattan-Guinness, _How Russell Discovered his Paradox_ , Hist. Math. **5** no.2 (1978) pp.127-137.

The first published account is presumably in the appendix of

* {#Frege03}G. Frege, _Grundgesetze der Arithmetik II_ , Pohle Jena 1903.

Russell discusses the paradox extensively in chapter X of

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
