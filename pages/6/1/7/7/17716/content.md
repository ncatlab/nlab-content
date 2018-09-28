

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
 An important ingredient of this program is the concept of an _atomic orbital $\infty$-category_ which is defined in terms of two important properties of the [[orbit category]] of $G$:

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


## References

Along with an introduction, nine expos&#233;s are planned:

* {#PHCTIntro} [[Clark Barwick]], Emanuele Dotto, [[Saul Glasman]], [[Denis Nardin]], [[Jay Shah]], _Parametrized higher category theory and higher algebra: A general introduction_, ([arXiv:1608.03654](https://arxiv.org/abs/1608.03654))

* {#PHCTI} [[Clark Barwick]], Emanuele Dotto, [[Saul Glasman]], [[Denis Nardin]], [[Jay Shah]], _Parametrized higher category theory and higher algebra: Expos&#233; I &#8211; Elements of parametrized higher category theory_, ([arXiv:1608.03657](https://arxiv.org/abs/1608.03657))

* {#Shah18} [[Jay Shah]], _Parametrized higher category theory and higher algebra: Expos&#233; II - Indexed homotopy limits and colimits_, ([arXiv:1809.05892](https://arxiv.org/abs/1809.05892))

* [[Denis Nardin]], _Parametrized higher category theory and higher algebra: Expos&#233; IV - Stability with respect to an orbital ∞-category_, ([arXiv:1608.07704](https://arxiv.org/abs/1608.07704))

A survey talk is

* [[Clark Barwick]], _Parametrized higher category theory and parameterized higher algebra_, [video](http://www.birs.ca/events/2016/5-day-workshops/16w5133/videos/watch/201602161030-Barwick.html)


