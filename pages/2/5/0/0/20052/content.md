
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

Let $L$ be a [[locale]]. Then a valuation on $L$ is by definition a valuation on its [[frame]] $\mathcal{O}(L)$. In particular, a valuation on a [[topological space]] is a valuation on the [[lattice of open subsets|lattice of its open sets]].

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

Let $\nu$ be a valuation on a [[locale]] $X$, and $U$ an open set of $X$ (i.e. an element of the corresponding [[frame]]). We say that $U$ is a **null** or **measure zero set** for $\nu$ if $\nu(U)=0$. 

Since a finite union of null sets is null, null sets form a directed net in the frame. Therefore, if $\nu$ is a continuous valuation, it admits a unique maximal null open set. The [[complement]] of this set, which is a [[closed subspace#locales|closed subspace]] of $X$, is called the **[[support]]** of $\nu$.

### Integration

(...)


## Extending valuations to measures

As we have seen [above](#borel_measures), a [[Borel subset|Borel measure]] always restricts to a valuation. It is natural to ask the converse question of whether a valuation can always be extended to a Borel measure. In general, the answer is negative. In the case of *continuous* valuations, however, one would expect that in many cases the valuation can be extended to a [[tau-additive measure|$\tau$-additive Borel measure]]. 

The question is known, for example, to be true on all regular Hausdorff ($T_3$) spaces: 

**Theorem** (see [Manilla, Theorem 3.23](#mthesis)). On every $T_3$ topological space, a locally finite continuous valuation extends uniquely to a regular, [[tau-additive measure|$\tau$-additive Borel measure]].

This includes in particular every [[metric space]].

Moreover, the following is known:


**Theorem** (see [Manilla, Theorem 3.27](#mthesis)). On every locally compact [[sober space]], a locally finite continuous valuation extends uniquely to a regular, [[tau-additive measure|$\tau$-additive Borel measure]].

The question of whether one can extend a finite continuous valuation to a Borel measure on any sober space, at the present time, is still open. 


## References


For a general treatment, see

* {#vmonad} [[Steve Vickers]], _A monad of valuation locales_, 2011. [Link here](https://www.cs.bham.ac.uk/~sjv/Riesz.pdf).

* Wikipedia, _<a href="https://en.wikipedia.org/wiki/Valuation_(measure_theory)">Valuation (measure theory)</a>_


For the theory of [integration over valuations](#integration), see 

* {#vintegral} [[Steve Vickers]], _A localic theory of lower and upper integrals_, 2008. [Link here](https://onlinelibrary.wiley.com/doi/abs/10.1002/malq.200710028).

* [[Thierry Coquand]] and [[Bas Spitters]], _Integrals and Valuations_, 2009. [Link here](http://logicandanalysis.org/index.php/jla/article/view/14/12).


For the problem of [extending valuations to measures](#extending_valuations_to_measures), see

* Mauricio Alvarez Manilla, Abbas Edalat, and Nasser Saheb-Djahromi, _An extension result for continuous valuations_, 1998. [Link here](https://www.sciencedirect.com/science/article/pii/S1571066105802105#!).

* {#mthesis} Mauricio Alvarez Manilla, _Measure theoretic results for continuous valuations on partially ordered spaces_, Dissertation, 2000. [Link here](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=1&ved=2ahUKEwimwZ2P1fTfAhWxtIsKHcMoB8AQFjAAegQIBBAC&url=http%3A%2F%2Fwww.cs.tufts.edu%2F~nr%2Fcs257%2Farchive%2Fmauricio-alvarez-manilla%2Fpublic.ps.gz&usg=AOvVaw38Hpk__TIWXKxUqAssXN3E).

* Klaus Keimel and Jimmie D. Lawson, _Measure extension theorems for_
$T_0$ _spaces_, 2004. [Link here](https://www.sciencedirect.com/science/article/pii/S0166864104002755).
