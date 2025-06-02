
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

The notion in the corresponding [[internal logic]] (i.e. in [[dependent type theory]]) of a [[semi-simplicial object]] in a [[locally cartesian closed (infinity,1)-category]]. 

Similarly to [[semi-simplicial sets]], there are typically two approaches that one can take to defining semi-simplicial types in [[dependent type theory]]: 

* One can define fibered semi-simplicial types as an [[(infinity,1)-presheaf]] on the category $\Delta_+$ of [[finite]] [[inhabited]] [[ordinals]] and [[injections]] via synthetic $(\infty,1)$-category theory. 

* One can define indexed semi-simplicial types as a family of families by iterating the [[categorical semantics of dependent types|correspondence between fibrations and families]] based on "iterated dependencies". 

None of these approaches are currently possible in plain [[dependent type theory]] or [[homotopy type theory]] due to the issue of handling infinity many data in a finitary manner, whether for the iterated families of semi-simplicial types or the coherence laws of $(\infty,1)$-categories. Instead, defining semi-simplicial types requires the extension of dependent type theory with additional features, such as 

* [[modal type theory|modalities]] for [[synthetic (infinity,1)-category theory]] (e.g. [[simplicial type theory]], [[triangulated type theory]]), 

* other levels / non-fibrant types / [[infinitary record types]] (e.g. [[two-level type theory]], [[type theory with shapes]], [[Homotopy Type System]]), 

* [[explicit parametricity]] (e.g. some [[cubical type theory]], [[displayed type theory]], [[cohesive type theory]] with [[sufficient cohesion]])

Historically, the “iterated dependency” approach to semi-simplicial sets has given dependent type theorists a candidate approach for tackling coherence issues in dependent type theory. With simplicial sets, it’s hard to see how one might tackle or avoid them. (Comparing it to the semi-simplicial approach, one requires degeneracy maps and equations between them, which lets loose the spectre of coherence again.) Furthermore, reasoning about Kan simplicial sets seems to insist on classical logic. For example, the classical result stating the homotopy equivalence of fibers of a Kan fibration cannot be proved constructively ([pdf](https://ncatlab.org/ufias2012/files/countermodel.pdf)). In homotopy-theoretic terms, this is because $\Delta_+$ is a [[direct category]], while the [[simplex category]] $\Delta$ is not. 

## Definition

### Fibered semi-simplicial types

We work in a [[dependent type theory]] which supports [[synthetic (infinity,1)-category theory|synthetic $(\infty,1)$-category theory]], such as [[simplicial type theory]] or [[triangulated type theory]]. 

With the [[op modality]] $(-)^\op$, the [[directed univalent]] [[type universe]] $\mathcal{S}$, and the $(\infty,1)$-subcategory $\Delta_+ \subseteq \mathcal{S}$ of [[finite]] [[inhabited]] [[ordinals]] and [[injections]], a **semi-simplicial type** is simply a [[function]] $X:\Delta_+^op \to \mathcal{S}$, which is provably an [[(infinity,1)-presheaf|$(\infty,1)$-presheaf]] by the directed structure identity principle on $(\infty,1)$-presheaf $(\infty,1)$-categories. 

### Indexed semi-simplicial types

To illustrate the idea of indexed semi-simplicial types as families of families of $n$-semi-simplices, let us consider the finite-dimensional parts of such an indexed semi-simplicial type:

Let $U$ be a [[type universe]]. Then, 

* A $U$-small indexed 0-semi-simplicial type is just a $U$-small type $X_0:U$.

* A $U$-small indexed 1-semi-simplicial type is $U$-small indexed 0-semi-simplicial type $X_0$ with a family of $U$-small types 
$$x_0:X_0, x_1:X_0 \vdash X_1(x_0, x_1):U$$

* A $U$-small indexed 2-semi-simplicial type is a $U$-small indexed 1-semi-simplicial type $(X_0, X_1)$ with a family of $U$-small types
$$x:X_0, x_1:X_0, x_2:X_0, x_{0, 1}:X_1(x_0, x_1), x_{1, 2}:X_1(x_1, x_2), x_{0, 2}:X_1(x_0, x_2) \vdash X_2(x_0, x_1, x_2, x_{0, 1}, x_{1, 2}, x_{0, 2}):U$$
representing triangular configurations from $X_0$ and $X_1$. 

* A $U$-small indexed 3-semi-simplicial type is a $U$-small indexed 2-semi-simplicial type $(X_0, X_1, X_2)$ with a family of $U$-small types 
$$\begin{array}{l}
x:X_0, x_1:X_0, x_2:X_0, x_3:X_0, \\
x_{0, 1}:X_1(x_0, x_1), x_{1, 2}:X_1(x_1, x_2), x_{2, 3}:X_1(x_2, x_3), \\ 
x_{0, 2}:X_1(x_0, x_2), x_{1, 3}:X_1(x_1, x_3), x_{0, 3}:X_1(x_0, x_3), \\ 
x_{0, 1, 2}:X_2(x_0, x_1, x_2, x_{0, 1}, x_{1, 2}, x_{0, 2}), x_{0, 1, 3}:X_2(x_0, x_1, x_3, x_{0, 1}, x_{1, 3}, x_{0, 3}), \\
x_{0, 2, 3}:X_2(x_0, x_2, x_3, x_{0, 2}, x_{2, 3}, x_{0, 3}), x_{1, 2, 3}:X_2(x_1, x_2, x_3, x_{1, 2}, x_{2, 3}, x_{1, 3}), \\
\vdash X_2(x_0, x_1, x_2, x_3, x_{0, 1}, x_{1, 2}, x_{2, 3}, x_{0, 2}, x_{1, 3}, x_{0, 3}, x_{0, 1, 2}, x_{0, 1, 3}, x_{0, 2, 3}, x_{1, 2, 3}):U
\end{array}$$
representing tetrahedral configurations from $X_0$, $X_1$ and $X_2$. 

And so on. Then a $U$-small indexed semi-simplicial type (i.e. indexed infinity-semi-simplicial types) should be a type that is an indexed $n$-semi-simplicial type for all $n$. 

#### In explicit parametricity

Suppose that the [[dependent type theory]] has [[explicit parametricity]] with [[unary bridge types]] $(\mathrm{Br}_A(x))_{x:A}$. Then given a [[Tarski universe]] $(U, T)$, the type of $U$-[[small type|small]] indexed semi-simplicial types $U^{\Delta_{+}^\op}$ is a [[displayed coinductive type]] cogenerated by 

  * a function $Z^+:U^{\Delta_{+}^\op} \to U$ and 

  * a dependent function 
$$S^+:\prod_{X:U^{\Delta_{+}^\op}} T(Z^+(X)) \to \mathrm{Br}_{U^{\Delta_{+}^\op}}(X)$$

An indexed semi-simplicial type is simply an element of $U^{\Delta_{+}^\op}$, and the iterated dependencies are given by iterated bridge types. See e.g. [Kolomatskaia 2022](#Kolomatskaia22), [Kolomatskaia & Shulman 2023](#KS23), [Narya docs](#NaryaDocs). 

#### In other dependent type theories

There are other dependent type theories in which it is possible to define indexed semi-simplicial types in a universe:

* A first sketch of a definition was given in by [Voevodsky (2012)](#Voevodsky12). 

* [[Vladimir Voevodsky]] proposed *[[Homotopy Type System]]* (HTS), a homotopy type theory extended with non-[[fibrant types]] and with an extra equality which is extensional in the sense of [[extensional type theory]];

* [Part & Luo (2015)](#PartLuo15) proposed a "Logic-enriched Homotopy Type Theory", in particular, they formalized a construction of semi-simplicial types in this logic using the Plastic proof assistant;

* [Altenkirch, Capriotti & Kraus (2016)](#AltenkirchCapriottiKraus16) proposed a two-level type theory generalizing HTT, leading to 2LTT by [[Dannil Annenkov]], [[Paolo Capriotti]], [[Nicolai Kraus]] and [[Christian Sattler]], providing another construction of semi-simplicial types in an extended type theory;

* According to [Kraus (2018)](#Kraus18), semi-simplicial types can also be constructed in Angiuli-Harper-Wilson's computational higher-dimensional type theory. 

## Related concepts

* [[semi-simplicial object]]

  * [[semi-simplicial set]]

  * **semi-simplicial type**

* [[open problems in homotopy type theory]]

## References

Discussion of formulation of semi-simplicial [[types]] in the context of [[homotopy type theory]] (for use as discussed at _[[category object in an (infinity,1)-category]]_) is in

* {#IAS} [[UF-IAS-2012]], _[Semi-simplicial types](https://web.archive.org/web/20180728221737/http://uf-ias-2012.wikispaces.com/Semi-simplicial+types)_

[[Coq]]-code for semi-simplicial types in [[homotopy type theory]] had been proposed in

* {#Voevodsky12} [[Vladimir Voevodsky]], sketch of a definition (2012) &lbrack;Coq [code](https://ncatlab.org/ufias2012/files/semisimplicial.v)&rbrack;

but its execution requires augmenting [[homotopy type theory]] with an auxilirary [[extensional type theory|extensional]] [[identity type]], discussed in 

* [[Vladimir Voevodsky]], _A type system with two kinds of identity types_ (Feb. 2013) &lbrack;[[Voevodsky-HTS.pdf:file]]&rbrack;

See at _[[Homotopy Type System]]_ ("HTS") for more on this.

* {#BCH13} [[Bruno Barras]], [[Thierry Coquand]], [[Simon Huber]], _A generalization of Takeuti-Gandy Interpretation_  &lbrack;[[BarrasCoquandHuber-TakeutiGandyInterpretation.pdf:file]]&rbrack;

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
[[!redirects semi-simplicial types]]
[[!redirects semisimplicial type]]
[[!redirects semisimplicial types]]

[[!redirects indexed semi-simplicial type]]
[[!redirects indexed semi-simplicial types]]
[[!redirects indexed semisimplicial type]]
[[!redirects indexed semisimplicial types]]

[[!redirects fibered semi-simplicial type]]
[[!redirects fibered semi-simplicial types]]
[[!redirects fibered semisimplicial type]]
[[!redirects fibered semisimplicial types]]

[[!redirects fibred semi-simplicial type]]
[[!redirects fibred semi-simplicial types]]
[[!redirects fibred semisimplicial type]]
[[!redirects fibred semisimplicial types]]

[[!redirects semi-simplicial type in homotopy type theory]]
[[!redirects semi-simplicial types in homotopy type theory]]
