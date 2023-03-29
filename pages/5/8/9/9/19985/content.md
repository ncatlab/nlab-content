[[!redirects associative n-categories]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of *associative $n$-categories* (ANCs, [Dorn 2018](#Dorn18), [Reutter & Vicary 2019](#ReutterVicary19)) is a [[semi-strict infinity-category|semi-strict]] [[algebraic definition of higher categories|algebraic model]] for [[higher category theory]] based on the [[geometric shape for higher structures|geometric shape]] of [[globular sets]] with strictly [[associativity|associative]] [[composition]]: All higher [[coherence law|coherence laws]] in associative $n$-categories are strict, except for weak versions of higher [[exchange laws]].

Due to the tight control over [[coherence]]-issues, the theory of (free) associative $n$-categories lends itself to [[formal proof]], for implementation of corresponding [[proof assistants]] see* [[homotopy.io]]* (and its precursor *[[Globular]]*).

Composition operations in associative $n$-categories naturally have stratified-geometric semantics in [[manifold diagram|manifold diagrams]], which makes them an instance of [[geometric n-category|geometrical $n$-categories]]. In particular, the weak coherence laws of an associative $n$-category can be thought of in terms of a notion of homotopy between composites. This is similar to the case of a [[Gray-category]], which is strictly associative and unital, but which has a weak exchange law. In this sense, ANCs can be seen as a generalization of Gray categories.




## Examples

* An associative 0-category is a [[set]]

* An associative 1-category is an [[biased definition|unbiased]] [[1-category]]

* An associative 2-category is an [[biased definition|unbiased]] [[strict 2-category]]

* An associative 3-category is an [[biased definition|unbiased]] [[Gray-category|Gray 3-category]]

A separate notion of 'free' associative n-categories has been developed. These are instances of [[geometric computad|geometric computads]].

## Remarks

* It is conjectured that every [[weak n-category]] is weakly equivalent to an associative $n$-category with strict units. A (proof-wise) potentially more realistic version of this conjecture concerns the case of free associative $n$-categories, and is (as of 2023) a topic of active research.

* A related conjecture is [[Simpson's conjecture]], which states that fully weak higher categories are (in an appropriate sense) equivalent to weakly unital higher categories.

* The underlying idea of this line of modelling higher structures can be traced back to work on [[Gray-category|Gray 3-categories]] and [[surface diagram|surface diagrams]].

## Related concepts

* [[globular set]]

* [[homotopy.io]], [[Globular]]

* [[semistrict n-category]]

* [[geometric n-category]]

* [[manifold diagram]]

* [[surface diagram]]

* [[Gray-category]]

* [[Simpson's conjecture]]


## References

* [[Christoph Dorn]], _Associative $n$-categories_, talk at _[103rd Peripatetic Seminar on Sheaves and Logic](https://www.math.muni.cz/~loregianf/PSSL103/PSSL103.php)_ ([pdf](https://www.math.muni.cz/~loregianf/PSSL103/slides/Dorn.pdf)).

* {#Dorn18} [[Christoph Dorn]], _Associative $n$-categories_, PhD thesis ([arXiv:1812.10586](https://arxiv.org/abs/1812.10586)).

* {#ReutterVicary19} [[David Reutter]], [[Jamie Vicary]], _High-level methods for homotopy construction in associative $n$-categories_, LICS '19: Proceedings of the 34th Annual ACM/IEEE Symposium on Logic in Computer ScienceJune **62** (2019) 1–13 &lbrack;[arXiv:1902.03831](https://arxiv.org/abs/1902.03831), [doi:10.1109/LICS52264.2021.9470575](https://doi.org/10.1109/LICS52264.2021.9470575)&rbrack;

* [[Lukas Heidemann]], [[David Reutter]], [[Jamie Vicary]], *Zigzag normalisation for associative $n$-categories*, Proceedings of the Thirty-Seventh Annual ACM/IEEE Symposium on Logic in Computer Science (LICS 2022) &lbrack;[arXiv:2205.08952](https://arxiv.org/abs/2205.08952), [doi:10.1145/3531130.3533352](https://dl.acm.org/doi/10.1145/3531130.3533352)&rbrack;


[[!redirects associative n-categories]]

