
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

## Idea

**Disjunctive logic** is the [[internal logic]] of [[pre-lextensive categories]].  Roughly speaking this means it is [[cartesian logic]], with conjunction and "provably-unique existential quantification", together with "provably-disjoint disjunction".

## Definition

...

## Example

The (coherent) theory of (geometric) [[field|fields]] is obtained from the axioms for the algebraic theory of commutative unital rings by adding the sequents

$$(0=1)\vdash \bot\,\text{ (nontriviality) and }\,\top \vdash_x ((x=0) \vee
((\exists y)(xy=1)))\quad.$$

Since inverse elements in a commutative ring are unique when they exist the second sequent involves a legitimate existential quantification plus a legitimate disjunction (due to the nontriviality) whence the resulting theory is (finitary) disjunctive.

## Properties

...

## Related entries

* [[cartesian logic]]

* [[regular logic]]

* [[geometric logic]]

* [[extensive category]]

* [[disjoint union]]

* [[connected limit]]

## Link

* [category theory mailing list: discussion on extensive categories](http://www.mta.ca/~cat-dist/catlist/1999/extensive)

## References

The main reference on disjunctive logic is Johnstone ([1979](#Johnstone79)) which was inspired by a non-syntactic concept of [[Yves Diers]]. The [elephant](#Johnstone02) has some additional cursory remarks. Freyd ([2002](#Freyd02)) gives disjunctive logic a short treatment under the name 'alternating logic' and discusses the [[real closed field|theory of real closed fields]] as an example. Barr and Wells ([1985](#BarrWells85)) discuss the corresponding class of sketches without mentioning the syntactic side.

* {#AdamekRosicky94}[[Jiří Adámek]], [[Jiří Rosický]], _Locally presentable and accessible categories_,  Cambridge UP 1994. (exercise 5f., p.238)

* {#BarrWells85}[[Michael Barr]], [[Charles Wells]], _Toposes, Triples and Theories_ , Springer Heidelberg 1985. (Reprinted as [TAC reprint no.12](http://www.tac.mta.ca/tac/reprints/articles/12/tr12abs.html) (2005); section 8.2, pp.292f) 

* {#Freyd02}[[Peter Freyd]], _Cartesian Logic_ , Theor. Comp. Sci. **278** (2002) pp.3-21.

* {#Johnstone79}[[Peter Johnstone]], _A Syntactic Approach to Diers' Localizable Categories_ , pp.466-478 in Springer LNM **753** Heidelberg 1979.

* {#Johnstone02}[[Peter Johnstone]], _Sketches of an [[Elephant]] II_, Oxford UP 2002. (D1.3.6 p.834, D2.1.2(e) p.863, D2.2.6 p.872, D2.4.8 p.886)

[[!redirects Disjunctive logic]]
[[!redirects Disjunctive Logic]]
[[!redirects disjunctive theory]]