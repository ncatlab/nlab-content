
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

Let $L$ be a [[lattice]] with a [[bottom]] element $\bottom$. A **valuation** or **evaluation** on $L$ is a [[map]] $\nu \colon L\to\mathbb{R}_{\ge 0}$ with the following properties:

* *Monotonicity*: for all $x,y$ in $L$, $x\le y$ implies $\nu(x)\le\nu(y)$;

* *Strictness* (or [[unitality]]): $\nu(\bottom)=0$;

* *Modularity*: for all $x,y$ in $L$, 

$$
\nu(x) + \nu(y) = \nu(x \vee y) + \nu(x \wedge y) .
$$

The [[real line]] can be replaced, depending on the context, by the space of [[one-sided real number|lower reals]] (see for example [Vickers](#vmonad)).

Moreover, we call a valuation *continuous* if the following property holds, which is an instance of [[Scott topology|Scott continuity]], as well as of [[tau-smoothness|$\tau$-smoothness]]:

* *Continuity*: for every [[directed set|directed]] [[net]] $\{x_\lambda\}_{\lambda\in\Lambda}$ in $L$ admitting a supremum,

$$
\nu \big( \sup_{\lambda} x_\lambda \big) = \sup_\lambda \nu(x_\lambda) .
$$


### Valuations on locales and topological spaces

Let $L$ be a [[locale]]. Then a valuation on $L$ is by definition a valuation on its [[frame]] $\mathcal{O}(L)$. In particular, a valuation on a [[topological space]] is a valuation on the [[lattice of open subsets|lattice of its open sets]].

## Examples

### Dirac valuation

Let $X$ be a topological space, and let $x\in X$ be a point. The **Dirac valuation** at $x$ maps an open set $U\subseteq X$ to $1$ if $x\in U$, and to $0$ otherwise.

### Borel measures

Let $X$ be a topological space, and let $\mu$ be a measure defined on the [[Borel subset|Borel $\sigma$-algebra]] of $X$. Then the restriction of $\mu$ to the open subsets of $X$ is a valuation. The valuation is continuous if and only if $\mu$ is [[tau-smoothness|$\tau$-smooth]]. 



## Properties

(...)

## References

See also

* {#vmonad} [[Steve Vickers]], _A monad of valuation locales_ (<a href="https://www.cs.bham.ac.uk/~sjv/Riesz.pdf">pdf</a>).
 

* Wikipedia, _<a href="https://en.wikipedia.org/wiki/Valuation_(measure_theory)">Valuation (measure theory)</a>_


