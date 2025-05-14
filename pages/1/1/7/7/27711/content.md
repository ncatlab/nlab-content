
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

A reflexive type family used in [[internal parametricity]] and [[modal parametricity]]. 

Bridge types come in $n$-ary forms, for any natural number $n$. Examples include

* Unary bridge types $\mathrm{Br}_A(x)$, in [Bernardy & Moulin 2012](#BM12), [Bernardy, Coquand, & Moulin 2015](#BCM15), [Kolomatskaia & Shulman 2023](#KS23)

* Binary bridge types $\mathrm{Br}_A(x, y)$, in [Cavallo & Harper 2021](#CH21)

[[Narya]] has $n$-ary bridge types for $1 \leq n \leq 9$. 

Binary bridge types behave like [[identity types]] but without [[transport]]. 

## Univalence axiom

* The [[univalence axiom]] of a [[type universe]] $U$ for nullary bridge types says that there is an [[equivalence of types]] between the bridge type $\mathrm{Br}_U$ and the type of types $U$. 

* The [[univalence axiom]] of a [[type universe]] $U$ for unary bridge types says that there is an [[equivalence of types]] between the bridge type $\mathrm{Br}_U(A)$ and the type of type families $A \to U$. 

* The [[univalence axiom]] of a [[type universe]] $U$ for binary bridge types says that there is an [[equivalence of types]] between the bridge type $\mathrm{Br}_U(A, B)$ and the type of correspondences $A \to B \to U$. 

## Related concepts

* [[internal parametricity]]

* [[identity type]]

* [[hom type]]

* [[displayed coinductive type]]

* [[cubical type theory]]

* [[higher observational type theory]]

* [[displayed type theory]]

* [[symmetric cube category]]

## References

The terminology "bridge" is first used in this sense in

* [[Andreas Nuyts]], [[Andrea Vezzosi]], [[Dominique Devriese]], *Parametric quantifiers for dependent type theory*, Proceedings of the ACM on Programming Languages (ICFP) **1** (2017) 1-29 &lbrack;[doi:10.1145/3110276](https://doi.org/10.1145/3110276)&rbrack;

Bridge types first appear in an unary form, written as $x \in \llbracket A \rrbracket$ rather than $\mathrm{Br}_A(x)$, in

* {#BM12} [[Jean-Philippe Bernardy]] and [[Guilhem Moulin]]. 2012. *A Computational Interpretation of Parametricity.* In Proceedings of the 27th Annual IEEE Symposium on Logic in Computer Science, LICS 2012, Dubrovnik, Croatia, June 25-28, 2012. IEEE Computer Society, 135–144. &lbrack;[doi:10.1109/LICS.2012.25](https://doi.org/10.1109/LICS.2012.25)&rbrack;

An equivalent of univalence for unary bridge types appears (with inverse conditions given by the Pair-Pred and Surj-Typ equations) in

* {#BCM15} [[Jean-Philippe Bernardy]], [[Thierry Coquand]], and [[Guilhem Moulin]]. 2015. *A Presheaf Model of Parametric Type Theory.* In The 31st Conference on the Mathematical Foundations of Programming Semantics, MFPS 2015, Nijmegen, The Netherlands, June 22-25, 2015 (Electronic Notes in Theoretical Computer Science, Vol. 319), Dan R. Ghica (Ed.). Elsevier, 67–82. &lbrack;[doi:10.1016/j.entcs.2015.12.006](https://doi.org/10.1016/j.entcs.2015.12.006)&rbrack;

The equivalent of univalence for (binary) bridge types is called "relativity" in

* {#CH21} [[Evan Cavallo]] and [[Robert Harper]]. 2021. *Internal Parametricity for Cubical Type Theory.* Log. Methods Comput. Sci. 17, 4 (2021). &lbrack;<a href="https://doi.org/10.46298/lmcs-17(4:5)2021">doi:10.46298/lmcs-17(4:5)2021</a>, [arXiv:2005.11290](https://arxiv.org/abs/2005.11290)&rbrack;

A unary bridge type called "display" and written as $A^d(x)$ instead of $\mathrm{Br}_A(x)$ appears in

* {#KS23} [[Astra Kolomatskaia]], [[Michael Shulman]], *Displayed Type Theory and Semi-Simplicial Types* &lbrack;[arXiv:2311.18781](https://arxiv.org/abs/2311.18781)&rbrack; 

A fibered version of bridge types is defined in:

* {#ACKS24} [[Thorsten Altenkirch]], [[Yorgo Chamoun]], [[Ambrus Kaposi]], [[Michael Shulman]], *Internal parametricity, without an interval*, Proceedings of the ACM on Programming Languages (POPL) **8** (2024) 2340-2369 &lbrack;[arXiv:2307.06448](https://arxiv.org/abs/2307.06448), [doi:10.1145/3632920](https://doi.org/10.1145/3632920)&rbrack;

Bridge types in [[Narya]]:

* *Parametric Observational Type Theory*, [[Narya]] documentation. ([web](https://narya.readthedocs.io/en/latest/parametric-observational-type-theory.html)) 

[[!redirects bridge type]]
[[!redirects bridge types]]

[[!redirects unary bridge type]]
[[!redirects unary bridge types]]

[[!redirects binary bridge type]]
[[!redirects binary bridge types]]

[[!redirects n-ary bridge type]]
[[!redirects n-ary bridge types]]