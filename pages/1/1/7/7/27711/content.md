
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

A reflexive type family $\mathrm{Br}_A(x, y)$ used in [[internal parametricity]] that behaves like the [[identity type]] but without [[transport]]. 

## Univalence axiom

The [[univalence axiom]] of a [[type universe]] $U$ for bridge types says that there is an [[equivalence of types]] between the bridge type $\mathrm{Br}_U(A, B)$ and the type of correspondences $(A \times B) \to U$. 

## Related concepts

* [[internal parametricity]]

* [[identity type]]

* [[hom type]]

* [[higher observational type theory]]

## References

The terminology "bridge" is first used in this sense in

* [[Andreas Nuyts]], [[Andrea Vezzosi]], [[Dominique Devriese]], *Parametric quantifiers for dependent type theory*, Proceedings of the ACM on Programming Languages (ICFP) **1** (2017) 1-29 &lbrack;[doi:10.1145/3110276](https://doi.org/10.1145/3110276)&rbrack;

Bridge types first appear in an unary form, written as $x \in \llbracket A \rrbracket$ rather than $\mathrm{Br}_A(x)$, in

* {#BM12} [[Jean-Philippe Bernardy]] and [[Guilhem Moulin]]. 2012. *A Computational Interpretation of Parametricity.* In Proceedings of the 27th Annual IEEE Symposium on Logic in Computer Science, LICS 2012, Dubrovnik, Croatia, June 25-28, 2012. IEEE Computer Society, 135–144. &lbrack;[doi:10.1109/LICS.2012.25](https://doi.org/10.1109/LICS.2012.25)&rbrack;

An equivalent of univalence for unary bridge types appears (with inverse conditions given by the Pair-Pred and Surj-Typ equations) in

* {#BCM15} [[Jean-Philippe Bernardy]], [[Thierry Coquand]], and [[Guilhem Moulin]]. 2015. *A Presheaf Model of Parametric Type Theory.* In The 31st Conference on the Mathematical Foundations of Programming Semantics, MFPS 2015, Nijmegen, The Netherlands, June 22-25, 2015 (Electronic Notes in Theoretical Computer Science, Vol. 319), Dan R. Ghica (Ed.). Elsevier, 67–82. &lbrack;[doi:10.1016/j.entcs.2015.12.006](https://doi.org/10.1016/j.entcs.2015.12.006)&rbrack;

The equivalent of univalence for (binary) bridge types is called "relativity" in

* {#CH21} [[Evan Cavallo]] and [[Robert Harper]]. 2021. *Internal Parametricity for Cubical Type Theory.* Log. Methods Comput. Sci. 17, 4 (2021). &lbrack;<a href="(https://doi.org/10.46298/lmcs-17(4:5)2021">doi:10.46298/lmcs-17(4:5)2021</a>&rbrack;

-

* {#ACKS24} [[Thorsten Altenkirch]], [[Yorgo Chamoun]], [[Ambrus Kaposi]], [[Michael Shulman]], *Internal parametricity, without an interval*, Proceedings of the ACM on Programming Languages (POPL) **8** (2024) 2340-2369 &lbrack;[arXiv:2307.06448](https://arxiv.org/abs/2307.06448), [doi:10.1145/3632920](https://doi.org/10.1145/3632920)&rbrack;

Bridge types in [[Narya]]:

* *Parametric Observational Type Theory*, [[Narya]] documentation. ([web](https://narya.readthedocs.io/en/latest/parametric-observational-type-theory.html)) 

[[!redirects bridge type]]
[[!redirects bridge types]]