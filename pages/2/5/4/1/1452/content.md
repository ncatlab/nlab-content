
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Philosophy
+-- {: .hide}
[[!include philosophy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The analytic-synthetic distinction has a long history stretching back to the ancient Greeks. It has come to mean different things according to the discipline in which it is employed, but each use can trace its origins to the classical version.

In the classical world, thinkers such as Aristotle, Euclid, Pappus and Proclus, used these terms to distinguish between methods of enquiry. A **synthetic** solution to a problem relies on reasoning from first principles, the kind of reasoning we see displayed in Euclid's _Elements_. The solution is thought to be _put together_ (συντίθημι). The kinds of first principle allowed are definitions, common notions and postulates, the latter being concerned with the specific subject matter at hand. By contrast, an **analytic** solution operates by working backwards from the problem to see what needs to be the case to be able to resolve it. Thus it analyses, or _unravels_ (ἀναλύω), the problem. This exercise might then make contact with things already known from first principles, or lead to new such principles. Often analytic discovery was written up in synthetic fashion.

In the seventeenth century, [[Descartes]] understood the distinction in the same way. When asked by Mersennes why he did not present his philosophical arguments in the synthetic fashion, he replied that he considered presentation according to the analytic method as more persuasive. This allowed the reader to see the necessity of the first principles reached, for instance, famously the _Cogito_, 'I think therefore I am'.

Descartes' approach to geometry via coordinates allowed him to resolve open questions bequeathed by Pappus and others from the ancient world (see [Domski](#Domski)). Since it could be seen as operating according to an analytic method, it was named _analytic geometry_.

## Analytic-synthetic distinction in philosophy

Later in the seventeenth century, we find [[Leibniz]] arguing that for any true statement, universal or singular, necessary or contingent, its subject contains within it the predicate stated to hold of it. For some of these propositions, such as identity statements, this is obvious, but others require considerable work to reveal this to be so:

>Implicit containment (or exclusion) was to be revealed by the sort of "analysis of notions" that Leibniz had already emphasized as a crucial philosophical method in his influential paper "Meditations on Knowledge, Truth, and Ideas", and this role accounts both for the general importance of analysis within German rationalism and for Kant’s choice of the term 'analytic' to describe such containment truths. ([Anderson 15, p. 9](#Anderson15))

[[Kant]] famously disagreed with this claim. For him the truth of some propositions relies unavoidably on intuition or empirical sensation along with conceptual understanding. Thus, an _analytic_ proposition for Kant distinguishes a proposition whose predicate concept is wholly contained in its subject concept. A famous example is 'All bachelors are unmarried.' This is sometimes glossed today as _true by virtue of definition_. By contrast, in a _synthetic_ proposition the predicate concept is not wholly contained in the subject content. Kant gives 'All bodies are heavy' as an example of a synthetic statement, whereas 'All bodies are extended' is analytic. Ascertaining that bodies are heavy unavoidably requires empirical sensation. 

Note, all the same, that Kant continues to use 'analytic' and 'synthetic' in their original methodological sense:

> I have adopted in this work the method that is, I believe, most suitable if one wants to proceed analytically from common cognition to the determination of its supreme principle, and in turn synthetically from the examination of  this principle and its sources back to the common cognition in which  we find it used. (Groundwork of the Metaphysics of Morals, Preface)

With the introduction of his new logic, [[Frege]] defines analyticity in terms of a proposition's logical form. Where Kant had taken contentful mathematical statements as synthetic yet knowable _a priori_ (i.e., not relying on empirical data), Frege now considered arithmetic statements as analytic by virtue of his logicist analysis of number as a class of equinumerous concepts. So where Kant could argue that knowledge of $7+ 5=12$ relied upon intuitive synthesis

>no matter how long I analyze my concept of such a possible sum [of seven and five] I will still not find twelve in it,

for Frege, such a statement may be established purely by logical means. 

In the context of his [[Martin-Löf dependent type theory|dependent type theory]],  [[Per Martin-Löf]] ([ML94](#ML94)) draws on Kant to apply the analytic-synthetic distinction to different forms of judgment. 

Basically, he claims that $a : A$ and $a = b : A$ are judgments of the analytic forms, noting that there is an algorithm to check that judgments of these forms are derivable. For him, the form of judgment $A \text{ true}$ is the synthetic form of judgment, for conceptual analysis alone does not suffice to derive it. Wherever you must construct an element to establish a proposition, that proposition is synthetic. More recently, Bentzen ([B24](#B24)) discusses a number of problems with Martin-Löf's analytic-synthetic distinction in dependent type theory and proposes a revision of his views.

## Analytic and synthetic geometry

A distinction between _analytic_ and _synthetic_ methods is often made in geometry, leading on from the description of Descartes' geometry as analytic. In [Elementary Mathematics from an Advanced Standpoint: Geometry](http://books.google.co.uk/books?id=fj-ryrSBuxAC), Felix Klein wrote in 1908

> _Synthetic geometry is that which studies figures as such, without recourse to formulas, whereas analytic geometry consistently makes use of such formulas as can be written down after the adoption of an appropriate system of coordinates._ Rightly understood, there exists only a _difference of gradation_ between these two kinds of geometry, according as one gives _more prominence to the figures or to the formulas._ Analytic geometry which dispenses entirely with geometric representation can hardly be called geometry; synthetic geometry does not get very far unless it makes use of a suitable language of formulas to give precise expression to its results. (p. 55)

He continues

> In mathematics, however, as everywhere else, men are inclined to form parties, so that there arose _schools of pure synthesists_ and _schools of pure analysts_, who placed chief emphasis upon absolute "purity of method," and who were thus more one-sided than the nature of the subject demanded. Thus the analytic geometricians often lost themselves in blind calculations, devoid of any geometric representation, The synthesists, on the other hand, saw salvation in an artificial avoidance of all formulas, and thus they accomplished nothing more, finally, than to develop their own peculiar language formulas, different from ordinary formulas. (pp. 55-56)

#Related entries#

* [[synthetic mathematics]]
* [[synthetic differential geometry]]

## References

* {#Domski} Mary Domski, _Descartes’ Mathematics_, ([SEP](https://plato.stanford.edu/entries/descartes-mathematics))

* {#ML94} [[Per Martin-Löf]], _Analytic and Synthetic Judgements in Type Theory_, ([article](http://archive-pml.github.io/martin-lof/pdfs/Martin-Lof-Analytic-and-Synthetic-Judgements-in-Type-Theory.pdf))

* {#Anderson15} R. Lanier Anderson, _The Poverty of Conceptual Truth: Kant's Analytic/Synthetic Distinction and the Limits of Metaphysics_, Oxford University Press, 2015.

* {#B24} [[Bruno Bentzen]], _Analyticity and syntheticity in type theory revisited_, Review of Symbolic Logic, 17(4), pp. 1119–1145, 2024 ([article](https://philarchive.org/archive/BENAAS-9))
