
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### $(0,1)$-Category theory
+-- {: .hide}
[[!include (0,1)-category theory - contents]]
=--
#### Monoidal categories
+-- {: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Bouded Linear Logic (BLL) is a refinement of [[linear logic]] (LL) where [[derelictions]] are annotated with a natural number indicating the number of times the associated resource can be used.

This way, well-typed functions do not only satisfy the basic input/output specification (as in the [[simply-typed lambda calculus]]), but also a temporal specification, without the need for a Turing machine with a clock.

**Theorem.** A function from dyadic integers to dyadic integers is computable in polynomial time in the length of its input if and only if it is typable in BLL.

The expressive power of BLL thus lies between that of [[rudimentary linear logic]] (RLL)—which is sequent calculus without the [[weakening rule]] and without the [[contraction rule]]—and full linear logic.

## Related logical systems

Ugo dal Lago and Martin Hofmann have proposed a variant of BLL called QBAL,
which allows for quantification over resource variables
and is also sound and complete for polynomial time.

When the derelictions are annotated with an element
of a(n ordered) [[semiring]] $\mathcal{S}$,
we obtain [[graded linear logic]] ($\mathrm{G}_\mathcal{S}\mathrm{LL}$).

## Related concepts

* [[complexity class]]
* [[graded modality]]

## References

* [[Jean-Yves Girard]], [[Andre Scedrov]], [[Philip J. Scott]], _Bounded linear logic: a modular approach to polynomial-time computability_, Theoretical Computer Science Volume 97, Issue 1, 20 April 1992, Pages 1-66 (<a href="https://doi.org/10.1016/0304-3975(92)90386-T">doi:10.1016/0304-3975(92)90386-T</a>)

* [[Ugo Dal Lago]], [[Martin Hofmann]], _Bounded Linear Logic, Revisited_, Logical Methods in Computer Science, Volume 6, Issue 4 (December 18, 2010) lmcs:1064 ([arXiv:0904.2675](https://arxiv.org/abs/0904.2675))

* _Bounded Linear Logic Workshop_, Fontainebleau, 2-4 December 2013, ([webpage](https://www.cs.bham.ac.uk/~drg/bll.html))

[[!redirects bounded linear logics]]