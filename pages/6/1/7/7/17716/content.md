

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
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

##Idea

This entry relates to a series of papers, beginning with [Barwick-Dotto-Glasman-Nardin-Shah 16](#PHCTIntro) which aim to provide common foundations for several different parts of [[homotopy theory]], among which [[equivariant homotopy theory]], [[parametrized homotopy theory]], [[global homotopy theory]] and [[Goodwillie calculus]].

For $G$ a [[finite group]], various concepts in [[equivariant homotopy theory]] are constructed as [[indexed (∞,1)-category|indexed]] over an [[orbit category]], such as the [[homotopy theory]] of [[topological G-spaces]] or of $G$-[[equivariant spectra]], when regarded via [[Elmendorf's theorem]]. 

{#AtomicOrbital}
 An important ingredient of this program is the concept of an _atomic [[orbital $\infty$-category]]_ which is defined in terms of two important properties of the [[orbit category]] of $G$:

1. **Orbital**: Fiber products of representable presheaves are finite disjoint unions of representable presheaves, a restatement of the fact that the category of finite $G$-sets has pullbacks ([Mackey decomposition](double+coset#MackeyFormula)), so a version of the [[Beck-Chevalley condition]];

1. **Atomic**: The triviality of retracts (that is every retraction is an equivalence).

Examples of such $(\infty, 1)$-categories satisfying these two properties include: 

1. [[orbit categories]] of finite groups; 

1. more generally, orbit categories of [[profinite groups]] (where the [[stabilizers]] are required to be [[open subset|open]]); 

1. locally finite groups (where the stabilizers are required to be finite); 

1. any [[∞-groupoid]]; 

1. the cyclonic orbit 2-category (see at _[[cyclotomic spectrum]]_); 

1. the 2-category of connected finite groupoids and [[covering maps]]; 

1. the category of [[finite sets]] of [[cardinality]] $\leq n$ and [[surjective functions]]; 

1. the [[topological categories]] of [[finite number|finite]]-[[dimension|dimensional]] [[inner product spaces]] (over $\mathbb{R}$ and $\mathbb{C}$) of dimension $\leq n$ and orthogonal [[projections]].

The program looks to generate results which hold for all atomic orbital $\infty$-categories, for any instance of which, $T$, there are the associated concepts of $T$-$\infty$-category, $T$-space and $T$-spectrum.

For many cases of these atomic orbital $\infty$-categories there is a [[conservative (∞,1)-functor]] to a [[poset]], and so they are [[EI (∞,1)-categories]]. 

## Related concepts

* [[G-∞-category]], [[equivariant symmetric monoidal category|G-symmetric monoidal category]]

* [[G-operad]]

## References

Along with an introduction, nine expos&#233;s were planned, leading to the following material:

* {#PHCTIntro} [[Clark Barwick]], Emanuele Dotto, [[Saul Glasman]], [[Denis Nardin]], [[Jay Shah]], _Parametrized higher category theory and higher algebra: A general introduction_, ([arXiv:1608.03654](https://arxiv.org/abs/1608.03654))

* [[Clark Barwick]], _Parametrized higher category theory and parameterized higher algebra_, [video](http://www.birs.ca/events/2016/5-day-workshops/16w5133/videos/watch/201602161030-Barwick.html)

* {#PHCTI} [[Clark Barwick]], Emanuele Dotto, [[Saul Glasman]], [[Denis Nardin]], [[Jay Shah]], _Parametrized higher category theory and higher algebra: Expos&#233; I &#8211; Elements of parametrized higher category theory_, ([arXiv:1608.03657](https://arxiv.org/abs/1608.03657))

* {#Shah18} [[Jay Shah]], _Parametrized higher category theory_, ([arXiv:1809.05892](https://arxiv.org/abs/1809.05892))

* [[Jay Shah]], _Parametrized higher category theory II: Universal constructions_, ([arXiv:2109.11954](https://arxiv.org/abs/2109.11954))

* [[Denis Nardin]], _Parametrized higher category theory and higher algebra: Expos&#233; IV - Stability with respect to an orbital ∞-category_, ([arXiv:1608.07704](https://arxiv.org/abs/1608.07704))

On isotropy separation:

* [[Saul Glasman]], _Stratified categories, geometric fixed points and a generalized Arone-Ching theorem_, ([arxiv:1507.01976](https://arxiv.org/abs/1507.01976))

* [[Saul Glasman]], _Goodwillie calculus and Mackey functors_, ([1507.01976](https://arxiv.org/abs/1507.01976))

On $G$-operads and algebras:

* [[Denis Nardin]], [[Jay Shah]], _Parametrized and equivariant higher algebra_, ([arxiv:2203.00072](https://arxiv.org/abs/2203.00072))

* [[Shaul Barkan]], [[Rune Haugseng]], [[Jan Steinebrunner]], _Envelopes for Algebraic Patterns_, ([arxiv:2203.00072](https://arxiv.org/abs/1610.03127))

On factorization homology, THH and the $\mathbb{E}_V$ operad:

* Asaf Horev, _Genuine equivariant factorization homology_, ([arXiv:1910.07226](https://arxiv.org/abs/1910.07226))

* [[Jeremy Hahn]], Asaf Horev, [[Inbar Klang]], [[Dylan Wilson]], [[Foling Zou]], _Equivariant nonabelian Poincaré duality and equivariant factorization homology of Thom spectra_, ([arXiv:2006.13348](https://arxiv.org/abs/2006.13348))

On presentability, semiadditivity and stability:

* [[Kaif Hilman]], _Parameterized presentability over orbital categories_, ([arxiv:2202.02594](https://arxiv.org/abs/2202.02594))

* [[Bastiaan Cnossen]], [[Tobias Lenz]], [[Sil Linskens]], _Parametrized stability and the universal property of global spectra_, ([arXiv:2301.08240](https://arxiv.org/abs/2301.08240)),

* [[Bastiaan Cnossen]], _Twisted ambidexterity in equivariant homotopy theory_, ([arXiv:2303.00736](https://arxiv.org/abs/2303.00736)), 

* [[Bastiaan Cnossen]], [[Tobias Lenz]], [[Sil Linskens]], _Partial parametrized presentability and the universal property of equivariant spectra_, ([arxiv:2307.11001](https://arxiv.org/abs/2307.11001)) 

* [[Sil Linskens]], _Globalizing and stabilizing global $\infty$-categories_, ([ arXiv:2401.02264](https://arxiv.org/abs/2403.07676))

* [[Bastiaan Cnossen]], [[Tobias Lenz]], [[Sil Linskens]], _Parametrized stability and the universal property of global spectra_, ([arXiv: arXiv:2403.07676](https://arxiv.org/abs/2301.08240))

On noncommutative motives:

* [[Kaif Hilman]], _Parametrised noncommutative motives and equivariant cubical descent in algebraic K-theory_, ([arXiv:2202.02591](https://arxiv.org/abs/2202.02591))