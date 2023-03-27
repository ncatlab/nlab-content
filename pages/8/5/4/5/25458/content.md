
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Generally, by a "doubly closed monoidal category" one may mean a [[category]] equipped with not just one but two different [[closed monoidal category]]-[[structures]] &lbrack;[O'Hearn (2003), §2.2](O'Hearn03)&rbrack;.

A common and relevant special case is that of a [[cartesian closed category]] which is equipped with further non-cartesian [[closed monoidal category]]-[[structure]], in which case one may speak of *cartesian doubly closed monoidal categories* &lbrack;[Jeltsch (2016), Def. 3](#Jeltsch16)&rbrack;.

Examples of these commonly arise as "parameterized" generalizations of plain [[closed monoidal categories]]. For example, categories *[[VectBund]]* of [[finite number|finite]] [[rank of a vector bundle|rank]] [[vector bundles]] over base spaces taken from [[convenient categories of topological spaces]] (or just over [[Sets]]), whose [[morphisms]] admit [[base change]], are cartesian doubly closed monoidal, with the further non-cartesian tensor product being the [[external tensor product]] of [[vector bundles]]. In the same vein, [[tangent (infinity,1)-toposes|tangent $\infty$-toposes]] of [[parameterized spectra|parameterized]] ([[module spectra|module]]-)[[spectra]] form cartesian doubly [[monoidal (infinity,1)-category|closed monoidal $\infty$-categories]].

The [[internal language]] of such cartesian double closed monoidal categories is a combination of classical ([[intuitionistic type theory|intuitionistc]]) [[type theory]] for the cartesian closed [[fragment]], and some kind of [[linear type theory]] for the non-cartesian closed [[fragment]]: Where a [[context]] in [[intuitionistic type theory]] is an iterated cartesian ([[dependent product type|dependent]]) [[product type]] $(-)\times (-)$ and a context in [[linear type theory]] is an iterated [[multiplicative conjunction]] $(-) \otimes (-)$, so a context in the [[internal language]] of cartesian doubly monoidal categories is obtained as an alternation of these two construction principles, forming a [[tree]] with nodes or "bunches" labeled either "$\times$" or "$\otimes$" --- this is the topic of *[[bunched type theory]]*.

## Related concepts


* [[closed monoidal category]]

* [[bunched type theory]]

## References

Discussion of doubly closed monoidal categories as [[categorical semantics]] for [[bunched logic]]/[[bunched type theory]]:

* {#O'Hearn03} [[Peter O'Hearn]], §2.2 in: *On bunched typing*, Journal of Functional Programming **13** 4 (2003) 747-796 &lbrack;[doi:10.1017/S0956796802004495](https://doi.org/10.1017/S0956796802004495)&rbrack;

* {#Jeltsch16} Wolfgang Jeltsch, *Abstract categorical semantics for resourceful functional reactive programming*, Elsevier Journal of Logical and Algebraic Methods in Programming **85** 6 (2016) 1177-1200 &lbrack;[doi:10.1016/j.jlamp.2016.07.001](https://doi.org/10.1016/j.jlamp.2016.07.001)&rbrack;

Discussion of cartesian doubly [[monoidal (infinity,1)-category|closed monoidal $\infty$-categories]] of [[parameterized spectra|parameterized]] ([[module spectra|module]]-)[[spectra]] as [[categorical semantics]] of bunched [[linear homotopy type theory]]:

* {#Riley22Thesis} [[Mitchell Riley]], *A Bunched Homotopy Type Theory for Synthetic Stable Homotopy Theory*, PhD Thesis (2022) &lbrack;[doi:10.14418/wes01.3.139](https://doi.org/10.14418/wes01.3.139), [ir:3269](https://digitalcollections.wesleyan.edu/object/ir%3A3269), [pdf](https://mvr.hosting.nyu.edu/pubs/thesis.pdf)&rbrack;

[[!redirects doubly closed monoidal categories]]

[[!redirects cartesian doubly closed monoidal category]]
[[!redirects cartesian doubly closed monoidal categories]]



[[!redirects doubly closed monoidal (infinity,1)-category]]
[[!redirects doubly closed monoidal (infinity,1)-categories]]

[[!redirects doubly closed monoidal (∞,1)-category]]
[[!redirects doubly closed monoidal (∞,1)-categories]]



[[!redirects cartesian doubly closed monoidal (infinity,1)-category]]
[[!redirects cartesian doubly closed monoidal (infinity,1)-categories]]

[[!redirects cartesian doubly closed monoidal (∞,1)-category]]
[[!redirects cartesian doubly closed monoidal (∞,1)-categories]]






