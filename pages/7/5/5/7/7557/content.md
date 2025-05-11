+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Systems of _formal_ [[logic]], such as [[type theory]], try to transform expressions into a _canonical form_ which then serves as the end result of the given [[computation]] or [[deduction]]. A formal system is said to enjoy _canonicity_ if every expression reduces to canonical form.

More precisely, in [[type theory]], a [[term]] belonging to some [[type]] is said to be of **canonical form** if it is explicitly built up using the constructors of that type.  A canonical form is in particular a [[normal form]] (one not admitting any reductions), but the converse need not hold.

For example, the terms of type $\mathbb{N}$ (a [[natural numbers type]]) of canonical form are the [[numerals]]
$$ S(S(S(\cdots (0)\cdots ))). $$

A type theory is said to enjoy **canonicity** if every closed term (i.e. a [[term]] in the [[empty context]]) computes to a canonical form.  This is held to be an important meta-theoretic property of type theory, especially considered as a [[programming language]] or as a computational foundation for mathematics.  It is related to [[normalization]], which says that every *open* term can also be reduced to a "[[normal form]]" of some kind.

## Canonicity vs axioms

Adding [[axioms]] to [[Martin-Löf type theory]], such as the principle of [[excluded middle]] or the usual version of the [[univalence axiom]], can destroy canonicity.  The axioms result in "stuck terms" which are not of canonical form, yet neither can they be "computed" any further.

For instance, if we assume the law of excluded middle, then we can build a term $case(LEM(Goldbach),0,1) \colon \mathbb{N}$ which is $0$ or $1$ according as the Goldbach conjecture is true or false.  Clearly this term doesn't "compute", but neither is it of canonical form (a numeral).

Similarly, using the [[univalence axiom]], we can obtain a term $p : (\mathbf{2}=\mathbf{2})$ corresponding to the automorphism of the type $\mathbf{2}$ which switches $0_\mathbf{2}$ and $1_\mathbf{2}$. Then the term $transport(p,0_\mathbf{2})$ also has type $\mathbf{2}$, but doesn't "compute" because the computer gets "stuck" on the univalence term.

On the other hand, this form of univalence can be given a "computational" interpretation while preserving canonicity in [[cubical type theory]] (see e.g. [Huber 2019](#Huber16)). It is conjectured that univalence can also be given a "computational" interpretation while preserving canonicity in [[higher observational type theory]] (see [Altenkirch et al. 2024](#ACKS24)). 

## See also

* [[homotopy canonicity]]

## References

Discussion of canonicity in [[univalent type theory]] is discussed in 

* Simon Huber (with [[Thierry Coquand]]), _Towards a computational justification of the Axiom of Univalence_ , talk at _TYPES 2011_ ([pdf](http://www.cse.chalmers.se/~simonhu/slides/types11.pdf))

* [[Dan Licata]], [[Robert Harper]], _Computing with Univalence_  (2012) ([pdf](http://4wft.fmf.uni-lj.si/wp-content/uploads/2012/04/Licata.pdf))

* {#Licata2011}[[Dan Licata]], _Canonicity for 2-Dimensional Type theory_  (2011) ([web](http://homotopytypetheory.org/2011/07/27/canonicity-for-2-dimensional-type-theory/))

* {#Huber16} [[Simon Huber]], _Canonicity for Cubical Type Theory_, Journal of Automated Reasoning, 63, 2019. ([doi:10.1007/s10817-018-9469-1](https://dx.doi.org/10.1007/s10817-018-9469-1), [arXiv:1607.04156](https://arxiv.org/abs/1607.04156))

* {#ACKS24} [[Thorsten Altenkirch]], [[Yorgo Chamoun]], [[Ambrus Kaposi]], [[Michael Shulman]], *Internal parametricity, without an interval*, Proceedings of the ACM on Programming Languages (POPL) **8** (2024) 2340-2369 &lbrack;[arXiv:2307.06448](https://arxiv.org/abs/2307.06448), [doi:10.1145/3632920](https://doi.org/10.1145/3632920)&rbrack;

[[!redirects canonical form]]
[[!redirects canonical forms]]
[[!redirects canonicity]]
[[!redirects canonicity for type theory]]
[[!redirects type-theoretic canonicity]]

