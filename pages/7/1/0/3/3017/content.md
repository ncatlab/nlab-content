
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

For large classes of examples of [[bicategory|bicategories]] the [[k-morphism|1-morphisms]] naturally are of one of two different types:

1. special morphisms that may be taken to compose strictly among themselves;

1. more general morphisms that behave like [[bimodule]]s.

The archetypical example is indeed the [[bicategory]] whose objects are [[algebra]]s, and whose 1-morphisms are [[bimodule]]s between these: every ordinary algebra homomorphism $f : A \to B$ induces an $A$-$B$-bimodule ${}_f B$ and this operation induces a 2-functor from the [[category]] of algebras and algebra homomorphisms into the [[bicategory]] of algebras and bimodules, which is the identity on objects. 

For usefully working with bicategories of this kind, it is typically of crucial importance to remember this extra information. A _framing_ on a bicategory is a way to encode this.

This is essentially the same as a _[[proarrow equipment]]_ on a [[bicategory]]. See there for more.

**Framed bicategories** are also known as **fibrant double categories**, because they may be characterised by the property that $(L, R) : D_1 \to D_0 \times D_0$ is a [[fibration]] (Theorem 4.1 of [Shulman '08](#Shulman08)). They are called **gregarious double categories** in [DPP10](#DawsonParePronk10).

## See also
* [[companion pair]]
* [[conjunction]]
* [[proarrow equipment]]

## References

* {#Shulman08} [[Mike Shulman]], *Framed bicategories and monoidal fibrations*, Theory and Applications of Categories **20** 18 (2008) 650–738 &lbrack;[tac:2018](http://www.tac.mta.ca/tac/volumes/20/18/20-18abs.html), [arXiv:0706.1286](https://arxiv.org/abs/0706.1286)&rbrack;

*  {#DawsonParePronk10} R. Dawson, [[Robert Paré]], [[Dorette Pronk]], _The span construction_, Theory Appl. Categ. __24__ (2010), No. 13, 302&#8211;377, [TAC](http://www.tac.mta.ca/tac/volumes/24/13/24-13abs.html) [MR2720187](http://www.ams.org/mathscinet-getitem?mr=2720187)

* [[Nicola Gambino]], [[Joachim Kock]], _Polynomial functors and polynomial monads_, ([arXiv:0906.4931](http://arxiv.org/abs/0906.4931))

* [[Thomas Fiore]], [[Nicola Gambino]], [[Joachim Kock]], _Monads in double categories_, ([arXiv:1006.0797](http://arxiv.org/abs/1006.0797))

* [[Patrick Schultz]], _Regular and exact (virtual) double categories_, ([arXiv:1505.00712](http://arxiv.org/abs/1505.00712))

* [[Patrick Schultz]], [[David Spivak]], [[Christina Vasilakopoulou]], Ryan Wisnesky, _Algebraic Databases_, ([arXiv:1602.03501](http://arxiv.org/abs/1602.03501))

* Pierre-Evariste Dagand, [[Conor McBride]], _A Categorical Treatment of Ornaments_, ([arXiv:1212.3806](http://arxiv.org/abs/1212.3806))

[[!redirects framed bicategories]]
[[!redirects fibrant double category]]
[[!redirects fibrant double categories]]
[[!redirects gregarious double category]]
[[!redirects gregarious double categories]]
