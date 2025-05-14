
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

> Note: This page began on the homotopy type theory personal web as an update of a page initially posted on the wiki of the special year on Univalent Foundations at IAS in 2012-13. It was then posted to the main nLab web on 2022-06-09 when the homotopy type theory web was depreciated. This page is currently under revision since a lot of information on this page is out of date, with many dependent type theories developed in the past decade where one can construct semi-simplicial types. 

> The idea is that this page should contain a brief comment that it is unknown how to construct semi-simplicial types in vanilla [[Martin-Löf type theory]] / [[homotopy type theory]], and then detailed descriptions on how semi-simplicial types are defined in various extensions of MLTT/HoTT, such as [[Homotopy Type System]], [[two-level type theory]], [[parametric dependent type theories]] such as [[cubical type theory]] and [[displayed type theory]], [[simplicial type theory]], etc. 

> Right now, the situation is entirely reversed. There is a lot of description that it is unknown how to construct semi-simplicial types in MLTT/HoTT, and brief comments that it is possible to construct semi-simplicial types in various extensions of MLTT/HoTT. 

One interesting open problem (considered by [[Vladimir Voevodsky]] and others): define _[[semi-simplicial object|semi-simplicial]]_ types in Homotopy Type Theory.

Classically, a _[[semi-simplicial object]]_ in some [[category]] is much like a [[simplicial object]], but without any [[degeneracy maps]]; i.e. it is a [[contravariant functor]] from the category $\Delta_i$, of finite nonempty ordinals and just [[injections]] between them as [[morphisms]].

Can we define these internally to [[type theory]], that is as a [[functor]] from $\Delta_i$ to a [[type universe]] $U$ in [[homotopy type theory]], in some way?

The initial idea, proposed at IAS, was to represent semi-simplicial types not as a contravariant functor but, iterating the [[categorical semantics of dependent types|correspondence between fibrations and families]], as a family of families, what could be called an "indexed" presentation of semi-simplicial types based on "iterated dependencies".

## Semi-simplicial types as families of families of $n$-semi-simplices

To illustrate the idea of semi-simplicial types as families of families of $n$-semi-simplices, let us consider the finite-dimensional parts of such semi-simplicial type:

Let $U$ be a [[type universe]]. Then, 

* A $U$-small 0-semi-simplicial type is just a $U$-small type $X_0:U$.

* A $U$-small 1-semi-simplicial type is $U$-small 0-semi-simplicial type $X_0$ with a family of $U$-small types 
$$x_0:X_0, x_1:X_0 \vdash X_1(x_0, x_1):U$$

* A $U$-small 2-semi-simplicial type is a $U$-small 1-semi-simplicial type $(X_0, X_1)$ with a family of $U$-small types
$$x:X_0, x_1:X_0, x_2:X_0, x_{0, 1}:X_1(x_0, x_1), x_{1, 2}:X_1(x_1, x_2), x_{0, 2}:X_1(x_0, x_2) \vdash X_2(x_0, x_1, x_2, x_{0, 1}, x_{1, 2}, x_{0, 2}):U$$
representing triangular configurations from $X_0$ and $X_1$. 

* A $U$-small 3-semi-simplicial type is a $U$-small 2-semi-simplicial type $(X_0, X_1, X_2)$ with a family of $U$-small types 
$$\begin{array}{l}
x:X_0, x_1:X_0, x_2:X_0, x_3:X_0, \\
x_{0, 1}:X_1(x_0, x_1), x_{1, 2}:X_1(x_1, x_2), x_{2, 3}:X_1(x_2, x_3), \\ 
x_{0, 2}:X_1(x_0, x_2), x_{1, 3}:X_1(x_1, x_3), x_{0, 3}:X_1(x_0, x_3), \\ 
x_{0, 1, 2}:X_2(x_0, x_1, x_2, x_{0, 1}, x_{1, 2}, x_{0, 2}), x_{0, 1, 3}:X_2(x_0, x_1, x_3, x_{0, 1}, x_{1, 3}, x_{0, 3}), \\
x_{0, 2, 3}:X_2(x_0, x_2, x_3, x_{0, 2}, x_{2, 3}, x_{0, 3}), x_{1, 2, 3}:X_2(x_1, x_2, x_3, x_{1, 2}, x_{2, 3}, x_{1, 3}), \\
\vdash X_2(x_0, x_1, x_2, x_3, x_{0, 1}, x_{1, 2}, x_{2, 3}, x_{0, 2}, x_{1, 3}, x_{0, 3}, x_{0, 1, 2}, x_{0, 1, 3}, x_{0, 2, 3}, x_{1, 2, 3}):U
\end{array}$$
representing tetrahedral configurations from $X_0$, $X_1$ and $X_2$. 

And so on.

Each of these can be packed up in single type through [[product types]] and [[dependent function types]]. Thus, given a type universe $U$,

* Can we define a function "$\text{Semi-simplicial}:\mathbb{N} \to U$", such that for $n = 0,1,2,3$, the $U$-small type $\text{Semi-simplicial}(n)$ is (equivalent to) the objects explicitly defined here?

* Can we define a type of $U$-small semi-simplicial types (i.e. infinity-semi-simplicial types) with $n$-simplices for all $n$?

A first sketch of a definition was given in by [Voevodsky (2012)](#Voevodsky12), suggesting that defining such families requires to define restrictions, then to prove that restrictions of restrictions commute, but then also to prove higher-dimensional coherence conditions on restrictions.

[[Hugo Herbelin]] worked at the IAS on a formalization in [[Coq]] based on the presentation of $\Delta_i$ with face maps $d_i$. In [Herbelin (2014)](#Herbelin14) he describes the construction in [[Coq]] extended with the principle of [[uniqueness of identity proofs]] (UIP). UIP was used to cut down the need for higher-dimensional [[coherence]], so morally, it meant that types were actually [[h-sets]]. What the construction shows is how to define in all details such alternative presentation of semi-simplicial sets based on iterated dependencies, what can also be seen as an effective and generic construction of [[Reedy model structure|matching object]] representatives in a semi-simplicial set.

To cut the need for higher-dimensional coherences, several extensions of homotopy type theory were considered:

* [[Vladimir Voevodsky]] proposed *[[Homotopy Type System]]* (HTS), a homotopy type theory extended with non-[[fibrant types]] and with an extra equality which is extensional in the sense of [[extensional type theory]];

* [Part & Luo (2015)](#PartLuo15) proposed a "Logic-enriched Homotopy Type Theory", in particular, they formalized a construction of semi-simplicial types in this logic using the Plastic proof assistant;

* [Altenkirch, Capriotti & Kraus (2016)](#AltenkirchCapriottiKraus16) proposed a two-level type theory generalizing HTT, leading to 2LTT by [[Dannil Annenkov]], [[Paolo Capriotti]], [[Nicolai Kraus]] and [[Christian Sattler]], providing another construction of semi-simplicial types in an extended type theory;

* According to [Kraus (2018)](#Kraus18), semi-simplicial types can also be constructed in Angiuli-Harper-Wilson's computational higher-dimensional type theory. 

* Another approach is to use an [[internal parametricity|internally parametric]] or a [[modal parametricity|modally parametric]] [[dependent type theory]] with [[unary bridge types]], such as [[displayed type theory]] ([Kolomatskaia 2022](#Kolomatskaia22), [Kolomatskaia & Shulman 2023](#KS23), [Narya docs](#NaryaDocs)). The type of semi-simplicial types in a [[type universe]] can be defined as a [[displayed coinductive type]] using the unary bridge type, where each semi-simplicial type has a family of semi-simplicial types, coinductively yielding the above notion of semi-simplicial type. 

## Other approaches

The "indexed" approach as families of families with iterated dependencies is only one possible approach! Other approaches to the problem are also possible, and may be better.

An alternative idea is something like "in the simplicial model, or more generally in other homotopy-theoretic model, they should be equivalent to coherent (possibly: [[Reedy model structure|Reedy-fibrant]]) semi-simplicial objects".

Why not imitate the classical definition, using internal functors from the internally-defined category $\Delta{}_i$? Giving a reasonable definition of $\Delta{}_i$ is not too hard: the objects [n] are very well-behaved. But defining functors out of it is problematic, because there are coherence issues. One would have to specify the functoriality laws using equations, i.e. inhabitants of equality types, which homotopically we treat as paths. But specified paths in homotopy theory have to be coherent to define a useful notion of functor; thus we need equations between our equations (associativity pentagons, etc), then higher equations between those, and so on forever. Thus we end up with the same problem we had before of specifying infinitely much data using a finite description in type theory. 

If one restricts the types involved to [[h-sets]], then this problem go away; but then one has again only defined semi-simplicial [[h-sets]], which are (presumably) strictly less general.

To cut the need for higher-dimensional coherences, one can consider extensions of homotopy type theory: 

* Two such extensions is [[simplicial type theory]] and [[triangulated type theory]], where the coherence conditions of [[functors]] are already satisfied via [[synthetic (infinity,1)-category theory]] using the directed interval primitive. With the [[op modality]] $(-)^\op$, the [[directed univalent]] [[type universe]] $\mathcal{S}$, and the category $\Delta{}_i$, one can define [[semi-simplicial types]] as [[functions]] $X:\Delta{}_i^op \to \mathcal{S}$, which are automatically functors. 

## Why semi-simplicial, not simplicial?

With semi-simplicial sets, the “iterated dependency” approach gives us at least a candidate approach for tackling coherence issues. With simplicial sets, it’s hard to see how one might tackle or avoid them. (Comparing it to the semi-simplicial approach, one requires degeneracy maps and equations between them, which lets loose the spectre of coherence again.) Furthermore, reasoning about Kan simplicial sets seems to insist on classical logic. For example, the classical result stating the homotopy equivalence of fibers of a Kan fibration cannot be proved constructively ([pdf](https://ncatlab.org/ufias2012/files/countermodel.pdf)).

In homotopy-theoretic terms, this is because $\Delta{}_i$ is a [[direct category]], while the [[simplex category]] $\Delta$ is not. 

## About the original page on the wiki of the Univalent Foundations year

The original page about semi-simplicial types on the wiki of the Univalent Foundations year contained also material related to semi-simplicial sets in general though not to semi-simplicial types properly speaking. It is kept here for historical reasons.

**Update 4/12**: [A note on semisimplicial sets](https://ncatlab.org/ufias2012/files/semisimplicialsets.pdf) by Benno van den Berg.

**Update 4/15**: [A note on a presheaf model for simplicial sets](https://ncatlab.org/ufias2012/files/countermodel.pdf) by Marc Bezem and Thierry Coquand.

**Update 6/24**: Accompanying files to Update 4/15:

* [CL.pl](https://ncatlab.org/ufias2012/files/CL.pl), the prover for coherent logic (requires [SWI-Prolog](http://www.swi-prolog.org/))
* [X.in](https://ncatlab.org/ufias2012/files/X.in), a formalization of the model in coherent logic
* [X.model](https://ncatlab.org/ufias2012/files/X.model), the edges, fill1 and fill2, day by day, generated by the prover from input X.in.
* [X.v](https://ncatlab.org/ufias2012/files/X.v), a Coq script verifying the proof that no homotopy equivalence between the fibers can exist in the model.

## Related concepts

* [[open problems in homotopy type theory]]

* [[Homotopy Type System]] ("HTS")

## References

Discussion of formulation of semi-simplicial [[types]] in the context of [[homotopy type theory]] (for use as discussed at _[[category object in an (infinity,1)-category]]_) is in

* {#IAS} [[UF-IAS-2012]], _[Semi-simplicial types](https://web.archive.org/web/20180728221737/http://uf-ias-2012.wikispaces.com/Semi-simplicial+types)_

[[Coq]]-code for semi-simplicial types in [[homotopy type theory]] had been proposed in

* {#Voevodsky12} [[Vladimir Voevodsky]], sketch of a definition (2012) &lbrack;Coq [code](https://ncatlab.org/ufias2012/files/semisimplicial.v)&rbrack;

but its execution requires augmenting [[homotopy type theory]] with an auxilirary [[extensional type theory|extensional]] [[identity type]], discussed in 

* [[Vladimir Voevodsky]], _A type system with two kinds of identity types_ (Feb. 2013) &lbrack;[[Voevodsky-HTS.pdf:file]]&rbrack;

See at _[[Homotopy Type System]]_ ("HTS") for more on this.

* {#BCH13} [[Bruno Barras]], [[Thierry Coquand]], [[Simon Huber]], _A generalization of Takeuti-Gandy Interpretation_  &lbrack;[[BarrasCoquandHuber-TakeutiGandyInterpretation.pdf:file]]&rbrack;

* {#Herbelin14} [[Hugo Herbelin]], *A dependently-typed construction of semi-simplicial types*, Mathematical Structures in Computer Science, Vol 25 (special issue 05), 2015 &lbrack;[pdf](http://pauillac.inria.fr/~herbelin/articles/mscs-Her14-semisimplicial.pdf), [[Herbelin-SemiSimplicial.pdf:file]]&rbrack; &lbrack;Coq [code](http://pauillac.inria.fr/~herbelin/articles/semisimplicial.v)&rbrack;

* {#PartLuo15} [[Fedor Part]], [[Zhaohui Luo]]:  *Semi-simplicial Types in Logic-enriched Homotopy Type Theory* &lbrack;[arXiv:1506.04998](http://arxiv.org/abs/1506.04998)&rbrack; (Submitted on 16 Jun 2015) &lbrack;Plastic [code](https://github.com/part-xx/hott-plastic/tree/master/lib/Univalence/SimplicialTypes)&rbrack;

* {#AltenkirchCapriottiKraus16} [[Thorsten Altenkirch]], [[Paolo Capriotti]], [[Nicolai Kraus]]: *Extending Homotopy Type Theory with Strict Equality* &lbrack;[arXiv:1604.03799](https://arxiv.org/abs/1604.03799)&rbrack; (Submitted on Apr 2016) &lbrack;Agda [code](https://github.com/nicolaikraus/HoTT-Agda/blob/master/nicolai/SemiSimp/SStypes.agda) simulating semi-simplicial types in HoTT with strict equality&rbrack;

* [[Danil Annenkov]], [[Paolo Capriotti]], [[Nicolai Kraus]], [[Christian Sattler]]: *Two-Level Type Theory and Applications* &lbrack;[arXiv:1705.03307](https://arxiv.org/abs/1705.03307)&rbrack; (Submitted on May 2017)

* [[Nicolai Kraus]], [[Christian Sattler]]: *Space-valued diagrams, type-theoretically (extended abstract)* &lbrack;[arXiv:1704.04543](https://arxiv.org/abs/1704.04543)&rbrack; (Submitted on Apr 2017)

* {#Kraus18} [[Nicolai Kraus]]: *On the Role of Semisimplicial Types*, 2018 &lbrack;[pdf](https://www.cs.nott.ac.uk/~psznk/docs/on_semisimplicial_types.pdf)&rbrack;

* {#Kolomatskaia22} [[Astra Kolomatskaia]], *Semi-Simplicial Types*, [[Homotopy Type Theory Electronic Seminar Talks]], 15 December 2022 ([slides](https://www.uwo.ca/math/faculty/kapulkin/seminars/hottestfiles/Kolomaskaia-2022-12-15-HoTTEST.pdf), [video](https://www.youtube.com/watch?v=fQv2FpeFxew))

* {#KS23} [[Astra Kolomatskaia]], [[Michael Shulman]], *Displayed Type Theory and Semi-Simplicial Types* &lbrack;[arXiv:2311.18781](https://arxiv.org/abs/2311.18781)&rbrack; 

Semi-simplicial types in [[Narya]]

* {#NaryaDocs} *Higher datatypes and codatatypes*, [[Narya]] documentation. ([web](https://narya.readthedocs.io/en/latest/higher-types.html))

[[!redirects semi-simplicial type]]
[[!redirects semisimplicial type]]
[[!redirects semi-simplicial types]]
[[!redirects semisimplicial types]]

[[!redirects semi-simplicial type in homotopy type theory]]
[[!redirects semi-simplicial types in homotopy type theory]]
