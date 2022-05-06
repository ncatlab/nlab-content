#Contents#
* table of contents
{:toc}

## Idea

In the context of [[2-category theory]], a **cartesian closed 2-category** is a [[2-category]], $\mathcal{B}$, with [[2-limit|finite products]] and a cartesian closed structure. For any $A$, $B$ in $\mathcal{B}$, there is an exponential object $B^A$, an evaluation 1-arrow, $eval_{A, B}: B^A \times A \to B$, and for every $X$ an adjoint equivalence between $\mathcal{B}(X, B^A)$ and $\mathcal{B}(X \times A, B)$.  

The concept was introduced in ([Makkai 96](#Makkai96)). There is no connection to the concept of [[cartesian bicategory]].

## Examples

* the 2-category of generalized [[species]] ([FGHW](#FGHW)).

* the 2-category of cartesian distributors.

* the 2-category of operads.

## Related concepts

* [[cartesian closed category]]

## References

* {#Makkai96} [[Michael Makkai]], _Avoiding the axiom of choice in general category theory_, Journal of Pure and Applied Algebra, 108(2):109 – 173, 1996.

* [[Marcelo Fiore]], Philip Saville, _A type theory for cartesian closed bicategories_, ([arXiv:1904.06538](https://arxiv.org/abs/1904.06538))

* Philip Saville, _Cartesian closed bicategories: type theory and coherence_, ([PhD thesis](http://homepages.inf.ed.ac.uk/psaville/thesis-for-print.pdf), [arXiv:2007.00624](https://arxiv.org/abs/2007.00624))

Discussion of the example of generalised species:

* {#FGHW} M. Fiore, N. Gambino, M. Hyland, G. Winskel, _The cartesian closed bicategory of generalised species of structures_, ([pdf](http://www1.maths.leeds.ac.uk/~pmtng/Publications/generalised-species.pdf))

[[!redirects cartesian closed bicategory]]
[[!redirects cartesian closed bicategories]]
[[!redirects cartesian closed 2-categories]]
