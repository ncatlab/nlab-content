[[!redirects orbital $\infty$-category]]
[[!redirects orbital $\infty$-category]]


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

An _orbital $\infty$-category_ is an [[(∞,1)-category]] satisfying a weak axiomatic framework generalizing the properties of the [[orbit category]] of a [[finite group]] allowing for the construction of the [[Burnside category]].

## Definitions

Given $\mathcal{T}$ an [[(∞,1)-category]], we write $\mathbb{F}_{\mathcal{T}} \coloneqq  \mathcal{T}^{\amalg}$ for its finite [[free coproduct completion|coproduct completion]].

\begin{definition}
  An $\infty$-category $\mathcal{T}$ is **orbital** if $\mathbb{F}_{\mathcal{T}}$ admits pullbacks.
\end{definition}

\begin{definition}
  An orbital $\infty$-category $\mathcal{T}$ is **atomic** if every retract in $\mathcal{T}$ is an equivalence.
\end{definition}

## Basic properties

If $\mathcal{T}$ is orbital, then $\mathbb{F}_{\mathcal{T}}$ is [[disjunctive (∞,1)-category|disjunctive]], so we may form the Burnside category
$$
  \mathrm{Span}(\mathbb{F}_{\mathcal{T}}) \coloneqq  A^{\mathrm{eff}}(\mathbb{F}_{\mathcal{T}}),
$$
the latter denoting the [[(infinity,n)-category of correspondences|(∞,1)-category of correspondences]] constructed by [Barwick](#Barwick14).

## Examples
 
The following are all examples of atomic orbital $\infty$-categories.

* [[orbit categories]] of finite groups;  more generally, orbit categories of [[profinite groups]] (where the [[stabilizers]] are required to be [[open subset|open]]); 

* locally finite groups (where the stabilizers are required to be finite); 

* any [[∞-groupoid|space]]; 

* the cyclonic orbit 2-category (see at _[[cyclotomic spectrum]]_); 

* the 2-category of connected finite groupoids and [[covering maps]] (i.e. the [[global homotopy theory|global]] [[orbit category]]); 

* the category of [[finite sets]] of [[cardinality]] $\leq n$ and [[surjective functions]]; 

* the [[topological categories]] of [[finite number|finite]]-[[dimension|dimensional]] [[inner product spaces]] (over $\mathbb{R}$ and $\mathbb{C}$) of dimension $\leq n$ and orthogonal [[projections]].

For many cases of these atomic orbital $\infty$-categories there is a [[conservative (∞,1)-functor]] to a [[poset]], and so they are [[EI (∞,1)-categories]]. 
Essentially finite EI orbital _discrete_ categories have been considered by [Wilson](#Wilson17) on work concerning the slice filtration, where they are called _inductive orbital categories_.


## Related concepts

* [[equivariant symmetric monoidal category]]

* [[G-∞-category]], [[Parametrized Higher Category Theory and Higher Algebra]]

## References

Many of the original papers on this topic:

* {#PHCTIntro} [[Clark Barwick]], Emanuele Dotto, [[Saul Glasman]], [[Denis Nardin]], [[Jay Shah]], _Parametrized higher category theory and higher algebra: A general introduction_, ([arXiv:1608.03654](https://arxiv.org/abs/1608.03654))

* [[Clark Barwick]], _Parametrized higher category theory and parameterized higher algebra_, [video](http://www.birs.ca/events/2016/5-day-workshops/16w5133/videos/watch/201602161030-Barwick.html)

* {#PHCTI} [[Clark Barwick]], Emanuele Dotto, [[Saul Glasman]], [[Denis Nardin]], [[Jay Shah]], _Parametrized higher category theory and higher algebra: Expos&#233; I &#8211; Elements of parametrized higher category theory_, ([arXiv:1608.03657](https://arxiv.org/abs/1608.03657))

* {#Shah18} [[Jay Shah]], _Parametrized higher category theory_, ([arXiv:1809.05892](https://arxiv.org/abs/1809.05892))

* [[Jay Shah]], _Parametrized higher category theory II: Universal constructions_, ([arXiv:2109.11954](https://arxiv.org/abs/2109.11954))

* [[Denis Nardin]], _Parametrized higher category theory and higher algebra: Expos&#233; IV - Stability with respect to an orbital ∞-category_, ([arXiv:1608.07704](https://arxiv.org/abs/1608.07704))

* [[Denis Nardin]], _Stability and distributivity over orbital $\infty$-categories_, ([thesis](https://dspace.mit.edu/handle/1721.1/112895?show=full))

* [[Saul Glasman]], _Stratified categories, geometric fixed points and a generalized Arone-Ching theorem_, ([arxiv:1507.01976](https://arxiv.org/abs/1507.01976))

* [[Saul Glasman]], _Goodwillie calculus and Mackey functors_, ([1507.01976](https://arxiv.org/abs/1507.01976))

On [[disjunctive (∞,1)-categories]]

* {#Barwick14} [[Clark Barwick]], section 4 of _Spectral Mackey functors and equivariant algebraic K-theory (I)_, Adv. Math., 304:646–727 ([arXiv:1404.0108](http://arxiv.org/abs/1404.0108))

On the [[slice filtration]] for inductive orbital categories

* {#Wilson14} [[Dylan Wilson]], _On categories of slices_ ([arXiv:1711.03472v1](https://arxiv.org/abs/1711.03472v1))

[[!redirects orbital category]]
[[!redirects orbital categories]]