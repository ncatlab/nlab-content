
> This page is about valuation in [[measure theory]]. For valuation in [[algebra]] (on [[rings]]/[[fields]]) see at _[[valuation]]_.

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A **valuation** is a construction analogous to that of a [[measure]], which is however more compatible with [[constructive mathematics]], and readily generalizable to contexts such as [[point-free topology]].

## Definition

### Valuations on lattices

Let $L$ be a [[distributive lattice]] with a [[bottom]] element $\bottom$. A **valuation** or **evaluation** on $L$ is a [[map]] $\nu$ from $L$ into the space of non-negative [[one-sided real number|lower reals]], with the following properties:

* **Monotonicity**: for all $x,y$ in $L$, $x\le y$ implies $\nu(x)\le\nu(y)$;

* **Strictness** (or *[[unitality]]*): $\nu(\bottom)=0$;

* **Modularity**: for all $x,y$ in $L$, 

$$
\nu(x) + \nu(y) = \nu(x \vee y) + \nu(x \wedge y) .
$$

Moreover, we call a valuation *continuous* if the following property holds, which is an instance of [[Scott topology|Scott continuity]], as well as of [[tau-additive measure|$\tau$-additivity]]:

* **Continuity**: for every [[directed set|directed]] [[net]] $\{x_\lambda\}_{\lambda\in\Lambda}$ in $L$ admitting a supremum,

$$
\nu \big( \sup_{\lambda} x_\lambda \big) = \sup_\lambda \nu(x_\lambda) .
$$

For now, see more in [Vickers](#vmonad).


### Valuations on locales and topological spaces

Let $L$ be a [[locale]]. Then a valuation on $L$ is by definition a valuation on its [[frame]] $\mathcal{O}(L)$. Similarly, a valuation on a [[topological space]] is a valuation on the [[lattice of open subsets|lattice of its open sets]].

Valuations on locales are used in the [[topos approach to quantum mechanics]] and the [[Bohr topos]].

## Examples

### Dirac valuation

Let $X$ be a topological space, and let $x\in X$ be a point. The **Dirac valuation** at $x$, which we denote by $\delta_x$, maps an open set $U\subseteq X$ to $1$ if $x\in U$, and to $0$ otherwise.

### Simple valuations

On a topological space, a **simple valuation** is a finite convex (or linear) combination of Dirac valuations, i.e. a valuation in the form 
$$
\nu = \sum_{i=1}^n \alpha_i\,\delta_{x_i} ,
$$
for $x_i\in X$, and for positive (lower) real numbers $\alpha_i$, possibly summing to one.

### Borel measures

For more on this, see [[tau-additive measure|$\tau$-additive measure]].

Let $X$ be a topological space, and let $\mu$ be a measure defined on the [[Borel subset|Borel $\sigma$-algebra]] of $X$. Then the restriction of $\mu$ to the open subsets of $X$ is a valuation. The valuation is continuous if and only if $\mu$ is [[tau-additive measure|$\tau$-additive]]. 

The converse problem of whether a valuation is the restriction of a Borel measure is more difficult, see [below](#extending_valuations_to_measures).


## Measure-theoretic structures and properties

### Null sets and support

Valuations admit a notion of [[support]] similar to that of measures. In particular, continuous valuations, just as [[tau-additive measure|$\tau$-additive measures]], have a well-defined and well-behaved support.

Let $\nu$ be a valuation on a [[locale]] or [[topological space]] $X$, and $U$ an open set of $X$ (i.e. an element of the corresponding [[frame]]). We say that $U$ is a **null** or **measure zero set** for $\nu$ if $\nu(U)=0$. The [[complement]] of $U$, which is a [[closed subspace#locales|closed subspace]] of $X$, is said to have **full measure**.

Since a finite union of null sets is null, null sets form a directed net in the frame. Therefore, if $\nu$ is a continuous valuation, it admits a unique maximal null open set. The [[complement]] of this set, which is the largest closed subspace of full measure, is called the **[[support]]** of $\nu$.

The support induces a [[monad#the_bicategory_of_monads|morphism of monads]] (see [Fritz-Perrone-Rezagholi](#support), section 5). 


### Integration

There is an integration theory for valuation analogous to that of measures, where lower semicontinuous functions play the role of measurable functions
(see also [[correspondence between measure and valuation theory]]).

(...)


## Monads of valuations

Just as there are several [[monad|monads]] of probability measures (see [[Giry monad]]), there are a number of analogous monads of valuations.
The most famous are

* The [[probabilistic powerdomain]] on the category of [[dcpo|dcpos]], defined by Jones and Plotkin, of wide use in theoretical computer science.

* The **extended probabilistic powerdomain** on the [[Top|category of topological spaces]] It was introduced by [Heckmann](#monad). Its algebras have recently been studied by [Goubault-Larrecq and Jia](#algebras).

* The **valuation monad on the [[Loc|category of locales]]**, defined by [Steve Vickers](#vmonad).


## Extending valuations to measures

As we have seen [above](#borel_measures), a [[Borel subset|Borel measure]] always restricts to a valuation. It is natural to ask the converse question of whether a valuation can always be extended to a Borel measure. In general, the answer is negative. In the case of *continuous* valuations, however, one would expect that in many cases the valuation can be extended to a [[tau-additive measure|$\tau$-additive Borel measure]]. 

The question is known, for example, to be true on all regular Hausdorff ($T_3$) spaces: 

**Theorem** (see [Manilla, Theorems 3.23 and 3.27](#mthesis)). On every $T_3$ topological space, and on every locally compact [[sober space]], a locally finite continuous valuation extends uniquely to a regular, [[tau-additive measure|$\tau$-additive Borel measure]].

This includes in particular every [[metric space]], and every compact Hausdorff space. So, in many spaces of interest for analysis and probability theory, working with measures and working with valuations is only a difference in the language. 

The more general question of whether one can extend a finite continuous valuation to a Borel measure on any sober space, at the present time, is still open. 

However, we do have the following result for regular spaces.

**Theorem** (Theorem 4.4 in [Manilla](#mpaper)).
Any locally finite continuous valuation on a [[regular]] topological space
extends uniquely to a regular τ-smooth Borel measure.


## References

* {#monad} Reinhold Heckmann, _Spaces of valuations_, Papers on General Topology and Ap-plications, 1996. [Link here](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.45.5845&rep=rep1&type=pdf).

* Mauricio Alvarez-Manilla, Achin Jung, Klaus Keimel, _The probabilistic powerdomain for stably compact spaces_, Theoretical Computer Science 328, 2004. [Link here](https://www.sciencedirect.com/science/article/pii/S0304397504004074).

* {#algebras} Jean Goubault-Larrecq and Xiaodong Jia, _Algebras of the extended probabilistic powerdomain monad_, ENTCS 345, 2019. [Link here](https://www.sciencedirect.com/science/article/pii/S1571066119300349).

* {#support} [[Tobias Fritz]], Paolo Perrone and Sharwin Rezagholi, _Probability, valuations, hyperspace: Three monads on Top and the support as a morphism_, 2019. [Link here](https://arxiv.org/abs/1910.03752).


For valuations on locales, see

* {#vmonad} [[Steve Vickers]], _A monad of valuation locales_, 2011. [Link here](https://www.cs.bham.ac.uk/~sjv/Riesz.pdf).

For the theory of [integration over valuations](#integration), see 

* {#kirch} Olaf Kirch, _Bereiche und Bewertungen_ (in German), Master Thesis, Technische Hochschule Darmstadt, 1993. [Link here](http://fb04286.mathematik.tu-darmstadt.de/fbereiche/logik/research/Domains/papers/kirch/diplom.ps.gz).

* {#jung} Achim Jung, _Stably compact spaces and the probabilistic powerspace construction_, ENTCS 87, 2004. [Link here](https://www.sciencedirect.com/science/article/pii/S1571066104051345).



* [[Thierry Coquand]] and [[Bas Spitters]], _Integrals and Valuations_, 2009. [Link here](http://logicandanalysis.org/index.php/jla/article/view/14/12).

Integration on locales can be found in

* {#vintegral} [[Steve Vickers]], _A localic theory of lower and upper integrals_, 2008. [Link here](https://onlinelibrary.wiley.com/doi/abs/10.1002/malq.200710028).


For the problem of [extending valuations to measures](#extending_valuations_to_measures), see

*  {#mpaper} Mauricio Alvarez-Manilla,
_Extension of valuations on locally compact sober spaces_.

* Mauricio Alvarez Manilla, Abbas Edalat, and Nasser Saheb-Djahromi, _An extension result for continuous valuations_, 1998. [Link here](https://www.sciencedirect.com/science/article/pii/S1571066105802105#!).

* {#mthesis} Mauricio Alvarez Manilla, _Measure theoretic results for continuous valuations on partially ordered spaces_, Dissertation, 2000. [Link here](http://www.cs.tufts.edu/~nr/cs257/archive/mauricio-alvarez-manilla/public.ps.gz).

* Klaus Keimel and Jimmie D. Lawson, _Measure extension theorems for_
$T_0$ _spaces_, 2004. [Link here](https://www.sciencedirect.com/science/article/pii/S0166864104002755).

[[!redirects continuous valuation]]
[[!redirects continuous valuations]]
