
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of *cartesian closed 2-category* is the analog in [[2-category theory]] (hence the [[categorification]]) of the notion of *[[cartesian closed category]]* in [[category theory]]:

A **cartesian closed 2-category** is a [[2-category]], $\mathcal{B}$, with [[2-limit|finite products]] and a cartesian closed structure: For any $A$, $B$ in $\mathcal{B}$, there is an [[exponential object]] $B^A$, an evaluation [[1-morphism]], $eval_{A, B}: B^A \times A \to B$, and for every $X$ an [[adjoint equivalence]] between $\mathcal{B}(X, B^A)$ and $\mathcal{B}(X \times A, B)$.  

The concept was introduced in ([Makkai 96](#Makkai96)). There is no connection to the concept of [[cartesian bicategory]].

## Examples
 {Examples}

The following 2-categories are cartesian closed:

* the  2-categories [[Cat]]($\mathcal{C}$) of [[internal categories]] or [[Grpd]]$(\mathcal{C})$ of [[internal groupoids]] [[internalization|internal to]] a [[cartesian closed category]] $\mathcal{C}$ (e.g. [Niefield & Pronk 2019](#NiefieldPronk19));

* the 2-category of generalized [[species]] ([FGHW](#FGHW));

* the 2-category of cartesian [[distributors]];

* the 2-category of [[operads]].

## Related concepts

* [[cartesian closed category]]

## References

* {#Makkai96} [[Michael Makkai]], _Avoiding the axiom of choice in general category theory_, Journal of Pure and Applied Algebra, 108(2):109 – 173, 1996.

On cartesian closed 2-categories of [[internal categories]] or [[internal groupoids]]:

* {#NiefieldPronk19} [[Susan B. Niefield]], [[Dorette A. Pronk]], *Internal groupoids and exponentiability*, Cahiers de topologie et géométrie différentielle catégoriques, [**LX** 4 (2019)](http://cahierstgdc.com/index.php/volume-lx/) ([pdf](http://cahierstgdc.com/wp-content/uploads/2019/10/Niefield-Pronk-LX-4.pdf))

* [[Enrico Ghiorzi]], Section 1.2 of: *Complete internal categories* ([arXiv:2004.08741](https://arxiv.org/abs/2004.08741))


Discussion of the example of generalised [[species]]:

* {#FGHW} M. Fiore, [[Nicola Gambino]], [[Martin Hyland]], G. Winskel, _The cartesian closed bicategory of generalised species of structures_, ([pdf](http://www1.maths.leeds.ac.uk/~pmtng/Publications/generalised-species.pdf))


Discussion of [[syntax]] for CC 2-categories in [[type theory]]:

* [[Marcelo Fiore]], Philip Saville, _A type theory for cartesian closed bicategories_, ([arXiv:1904.06538](https://arxiv.org/abs/1904.06538))

* Philip Saville, _Cartesian closed bicategories: type theory and coherence_, ([PhD thesis](http://homepages.inf.ed.ac.uk/psaville/thesis-for-print.pdf), [arXiv:2007.00624](https://arxiv.org/abs/2007.00624))


[[!redirects cartesian closed bicategory]]
[[!redirects cartesian closed bicategories]]
[[!redirects cartesian closed 2-categories]]
