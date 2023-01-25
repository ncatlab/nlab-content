
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

_Dependent type theory_ is the flavor of [[type theory]] that admits _[[dependent types]]_.

Its [[categorical semantics]] is in [[locally cartesian closed categories]] $C$, where a [[dependent type]]

$$
  x : X \vdash E(x) \; \mathrm{type}
$$

is interpreted as a [[morphism]]  $E \to X$, hence an [[object]] in the [[slice category]] $C_{/X}$.

Then change of [[context]] corresponds to [[base change]] in $C$. See also _[[dependent sum]]_ and _[[dependent product]]_.

Dependent type systems are heavily used for _[[certified programming|software certification]]_. 

They also seem to support a [[foundations]] of mathematics in terms of [[homotopy type theory]].

## Description

### Judgments for types and terms

[[!include judgements for types and terms - table]]

## Properties

+-- {: .num_theorem}
###### Theorem

The [[functors]] 

* $Cont$, that form a [[category of contexts]] of a [[dependent type theory]];

* $Lang$ that forms the [[internal language]] of a [[locally cartesian closed category]]

constitute an [[equivalence of categories]]

$$
  DependentTypeTheories
    \stackrel{\overset{Lang}{\leftarrow}}{\underset{Cont}{\to}}
  LocallyCartesianClosedCategories
  \,.
$$

=--

This ([Seely, theorem 6.3](#Seely)).  It is somewhat more complicated than this, because we need to strictify the category theory to match the category theory; see [[categorical model of dependent types]].  For a more detailed discussion see at
_[[relation between type theory and category theory]]_.

## Examples

* [[objective type theory]]
* [[book HoTT]]
* [[Martin-Löf type theory]]
* [[cubical type theory]]
* [[higher observational type theory]]
* [[univalent type theory]]
* [[propositional logic as a dependent type theory]]


## Related concepts

* [[linear dependent type theory]]
* [[dependent type theoretic methods in natural language semantics]]
* [[set theory and dependent type theory]]


## References

For original references see at *[[Martin-Löf dependent type theory]]*, such as:

* {#Hofmann95} [[Martin Hofmann]], *Syntax and semantics of dependent types*, Chapter 2 in: _Extensional concepts in intensional type theory_, Ph.D. thesis, University of Edinburgh (1995), Distinguished Dissertations, Springer (1997) &lbrack;[ECS-LFCS-95-327](http://www.lfcs.inf.ed.ac.uk/reports/95/ECS-LFCS-95-327/), [[HofmannExtensionalIntensionalTypeTheory.pdf:file]], [doi:10.1007/978-1-4471-0963-1](https://doi.org/10.1007/978-1-4471-0963-1)&rbrack;

also published as:

* [[Martin Hofmann]], *Syntax and semantics of dependent types*, in *Semantics and logics of computation*, Publ. Newton Inst. **14**, Cambridge Univ. Press (1997) 79-130 &lbrack;[doi:10.1017/CBO9780511526619.004](https://doi.org/10.1017/CBO9780511526619.004)&rbrack;


Introductory accounts:

* {#Thompson91} [[Simon Thompson]], §6.3 in: *[[Type Theory and Functional Programming]]*, Addison-Wesley (1991) &lbrack;ISBN:0-201-41667-0, [webpage](http://www.cs.kent.ac.uk/people/staff/sjt/TTFP), [pdf](http://www.cs.kent.ac.uk/people/staff/sjt/TTFP/ttfp.pdf)&rbrack;

* {#Jacobs98} [[Bart Jacobs]], Chapter 10 in: *Categorical Logic and Type Theory*, Studies in Logic and the Foundations of Mathematics **141**, Elsevier (1998)  &lbrack;[ISBN:978-0-444-50170-7](https://www.sciencedirect.com/bookseries/studies-in-logic-and-the-foundations-of-mathematics/vol/141), [pdf](https://people.mpi-sws.org/~dreyer/courses/catlogic/jacobs.pdf)&rbrack;

  > (emphasis on the [[categorical model of dependent types]])


Introduction with parallel details on using [[proof assistants]]:

for [[Coq]]:

* [[Adam Chlipala]], _Certified programming with dependent types_, MIT Press 2013 &lbrack;[ISBN:9780262026659 ](https://mitpress.mit.edu/books/certified-programming-dependent-types), [pdf](http://adam.chlipala.net/cpdt/cpdt.pdf),  [book webpage](http://adam.chlipala.net/cpdt/)&rbrack;

* [[Théo Winterhalter]], *Formalisation and Meta-Theory of Type Theory*, Nantes (2020) &lbrack;[pdf](https://github.com/TheoWinterhalter/phd-thesis/releases/download/v1.2.1/TheoWinterhalter-PhD-v1.2.1.pdf), [github](https://github.com/TheoWinterhalter/phd-thesis)&rbrack;


for [[Agda]]:

* {#Norell08} [[Ulf Norell]], *Dependently Typed Programming in Agda*, p. 230-266 in: *Advanced Functional Programming* AFP 2008. Lecture Notes in Computer Science **5832** (2009) &lbrack;[doi:10.1007/978-3-642-04652-0_5](https://doi.org/10.1007/978-3-642-04652-0_5), [pdf](https://www.cse.chalmers.se/~ulfn/papers/afp08/tutorial.pdf)&rbrack;

* [[Agda]] Tutorial: _Introduction to dependent type theory_ ([webpage](http://ocvs.cfv.jp/Agda/tutorial/node128.html))

Original  discussion of dependent type theory as the [[internal language]] of [[locally cartesian closed categories]] is in 

* {#Seely} [[R. A. G. Seely]], _Locally cartesian closed categories and type theory_, Math. Proc. Camb. Phil. Soc. (1984) 95 ([pdf](http://www.math.mcgill.ca/rags/LCCC/LCCC.pdf))

A formal definition of dependent type theories beyond [[Martin-Löf dependent type theory]]:

* {#BauerHaselwarterLumsdaine20} [[Andrej Bauer]], [[Philipp G. Haselwarter]], [[Peter LeFanu Lumsdaine]], *A general definition of dependent type theories* &lbrack;[arXiv:2009.05539](https://arxiv.org/abs/2009.05539)&rbrack;

{#CSystemsReferences} On ([[essentially algebraic theory|essentially algebraic]])  formulations of dependent type theory (see [here](categorical+model+of+dependent+types#ContextualCategoriesOrCSystems) at *[[categorical models of dependent type theory]]*):

* [[Egbert Rijke]], _An algebraic formulation of dependent type theory_, ([mailing list discussion](https://groups.google.com/forum/#!topic/homotopytypetheory/OraMqbnCYy8/discussion))
* Vladimir Voevodsky, _B-systems_, ([arXiv:1410.5389](http://arxiv.org/abs/1410.5389))
* Vladimir Voevodsky, _A C-system defined by a universe in a category_, ([arXiv:1406.7413](http://arxiv.org/abs/1409.7925))
* Vladimir Voevodsky, _C-system of a module over a monad on sets_, ([arXiv:1406.7413](http://arxiv.org/abs/1407.3394))
* Vladimir Voevodsky, _Subsystems and regular quotients of C-systems_, ([arXiv:1406.7413](http://arxiv.org/abs/1406.7413))

For more see the references at _[[Martin-Löf dependent type theory]]_.

[[!redirects dependent type theories]]
[[!redirects Dependent type theories]]
[[!redirects Dependent type theory]]