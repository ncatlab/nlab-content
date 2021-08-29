
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Homological algebra
+-- {: .hide}
[[!include homological algebra - contents]]
=--
#### Regular and exact categories
+-- {: .hide}
[[!include regular and exact categories - contents]]
=--
=--
=--

# Puppe-exact category
* table of contents
{: toc}


##Idea
Loosely speaking a **Puppe exact category** is an [[abelian category]] without [[additive category|additivity]]. The remaining [[exact category|exactness]] properties permit a considerable amount of [[homology theory]].

Introduced by [[Dieter Puppe]] ([Puppe (1962)](#Puppe1962)) as a weakening of abelian categories, their homology theory was studied by [[Barry Mitchell]] in his textbook on category theory ([Mitchell (1965)](#Mitchell1965)). They were extensively used by [[Marco Grandis]] in his work on distributive homological algebra in the 1980s.

##Remark

Grandis worked on further generalizations that he called semi-exact or [[homological category|homological]]. This family differs from the concepts around [[semi-abelian categories]] studied in particular in the [2004 monograph](#BorceuxBourn2004) by [[Francis Borceux]] and [[Dominique Bourn]] with respect to the existence of finite limits in the latter. [Grandis (2010)](#Grandis2010) proposed viewing the difference as akin to the difference between projective and affine spaces.


##Definition

A [[well-powered category|well-powered]] category $\mathcal{C}$ is called _Puppe exact_ (or _p-exact_ for short) iff 

* $\mathcal{C}$ has a [[zero object]].

* $\mathcal{C}$ has [[kernels]] and [[cokernels]].

* every [[mono]] is a kernel and every [[epi]] is a cokernel.

* every morphism has an [[factorization system|epi-mono factorization]].

##Related entries

* [[abelian category]], [[semi-abelian category]]

* [[exact category]]

* [[homological category]]


##References

* {#BorceuxBourn2004} [[Francis Borceux]], [[Dominique Bourn]], [[Mal'cev, protomodular, homological and semi-abelian categories]], Mathematics and Its Applications __566__, Kluwer, 2004.

* [[Francis Borceux]] , [[Marco Grandis]], _Jordan-H&#246;lder, modularity and distributivity in non-commutative algebra_, JPAA **208** (2007), pp.665-689. ([doi](https://doi.org/10.1016/j.jpaa.2006.03.004))

* [[Aurelio Carboni]], [[Marco Grandis]], _Categories of projective spaces_, JPAA **110** (1996), pp.241-258. ([web](https://www.sciencedirect.com/science/article/pii/0022404995001115))

* [[Peter Freyd]], A. Scedrov, _Categories, Allegories_, North-Holland Amsterdam 1990.

* [[Marco Grandis]], _Transfer functors and projective spaces_, Math. Nachr. **118** (1984) pp.147-165. ([doi](https://doi.org/10.1002/mana.19841180111))

* {#Grandis2010} [[Marco Grandis]], _Homotopy spectral sequences_, J. Homotopy Relat. Struct. **5** (2010), pp.213-252.  ([arXiv:1007.0632](http://arxiv.org/abs/1007.0632), [pdf](http://tcms.org.ge/Journals/JHRS/xvolumes/2010/n1a12/v5n1a12.pdf))

* {#Mitchell1965} Barry Mitchell, _Theory of categories_, Pure and Applied Mathematics **17**, Academic Press, 1965.

* {#Puppe1962} [[Dieter Puppe]], _Korrespondenzen in abelschen Kategorien_ , Math. Ann. **148** (1962) pp.1-30. ([gdz](http://gdz.sub.uni-goettingen.de/dms/load/pdf/?PPN=GDZPPN002290812))

[[!redirects p-exact category]]