
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

A **tricategory** is a particular [[algebraic definition of higher category|algebraic]] notion of _weak_ [[3-category]]. 
The idea is that a tricategory is a category _weakly_ [[enriched category|enriched]] over [[Bicat]]: the [[hom-object|hom-objects]] of a tricategory are [[bicategories]], and the associativity and unity laws of [[enriched category|enriched categories]] hold only up to coherent equivalence.

## Coherence theorems
{#Coherence}

One way to state the coherence theorem for tricategories is that every tricategory is [[equivalence|equivalent]] to a [[Gray-category]], which is a sort of semi-strict 3-category (everything is strict except for the [[interchange law]]).

## Examples {#Examples}

For $R$ a commutative [[ring]], there is a [[symmetric monoidal bicategory]] $Alg(R)$ whose 

* [[object]]s are $R$-[[algebra]]s;

* [[morphism]]s are algebra [[bimodule]]s;

* [[2-morphisms|k-morphism]] are bimodule homomorphisms.

The monoidal product is given by [[tensor product]] over $R$.

By [[delooping]] this once, this gives an example of a [[tricategory]] with a single object.

The tricategory statement follows from Theorem 24 in either the journal version, or the arXiv:0711.1761v2 version of:

* [[Richard Garner]], [[Nick Gurski]]: The low-dimensional structures formed by tricategories. Math. Proc. Camb. Phil. Soc. 146 (2009),pp. 551--589, ([arXiv:0711.1761](http://arxiv.org/abs/0711.1761))

This, and that the monoidal bicategory is even symmetric monoidal is given by the main theorem in

* [[Mike Shulman]], _Constructing symmetric monoidal bicategories_ ([arXiv:1004.0993](http://arxiv.org/abs/1004.0993))



## Related entries 

*  [[strict 3-category]]
*  [[bicategory]]
*  [[tetracategory]]

## References

The original source:

* [[Robert Gordon]], [[A. John Power]], [[Ross Street]], _Coherence for tricategories_, Mem. Amer. Math Soc. 117 (1995) no 558 ([ISBN:978-1-4704-0137-5](https://bookstore.ams.org/memo-117-558))

refined in:

* [[Nick Gurski]], _An algebraic theory of tricategories_ ([pdf](http://gauss.math.yale.edu/~mg622/tricats.pdf))

See also:

Textbook account:

* {#JohnsonYau20} [[Niles Johnson]], [[Donald Yau]], Section 11.2 of: _2-Dimensional Categories_, Oxford University Press 2021 ([arXiv:2002.06055](http://arxiv.org/abs/2002.06055), [doi:10.1093/oso/9780198871378.001.0001](https://oxford.universitypressscholarship.com/view/10.1093/oso/9780198871378.001.0001/oso-9780198871378))


A discussion of [[monoidal category|monoidal]] tricategories, regarded by the discussion at [[k-tuply monoidal (n,r)-category]] as one-object [[tetracategories]], is in section 3 of

* [[Alex Hoffnung]], _Spans in 2-Categories: A monoidal tricategory_ ([arXiv:1112.0560](http://arxiv.org/abs/1112.0560))

See also

* [[Richard Garner]], [[Nick Gurski]], *The low-dimensional structures that tricategories form* ([arXiv:0711.1761](http://arxiv.org/abs/0711.1761))


* Peter Guthmann, _The tricategory of formal composites and its strictification_ ([arXiv:1903.05777](https://arxiv.org/abs/1903.05777))



[[!redirects tricategories]]
[[!redirects coherence theorem for tricategories]]
