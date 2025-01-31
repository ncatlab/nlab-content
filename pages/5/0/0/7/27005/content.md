+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
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

*Shifts* are particular [[dynamical systems]] on spaces of [[sequences]], or more generally on [[products]], which intuitively act on the *position* of the components (also by possibly copying and discarding them), but do not on the internal *values* of the coordinates. 

Shifts are ubiquitous in the theory of [[dynamical systems]] (and related fields, such as [[ergodic theory]] and [[information theory]]).
From the point of view of [[category theory]], they are a universal ([[right adjoint]]) way of forming dynamical systems from the objects of a category. 


## Definition

Let $X$ be a [[set]], and consider the countably infinite [[product]] $X^\mathbb{N}$. The **shift** is the map 
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
row sep=0,%
]
X^\mathbb{N} \ar{r}{\sigma} & X^\mathbb{N} \\
(x_0,x_1,x_2,\dots) \ar[mapsto]{r} & (x_1,x_2,x_3,\dots) ,
\end{tikzcd}
which one can interpret as a "shift to the left". 

Equivalently, it is the [[product projection]]
$$
X^\mathbb{N} \cong X \times X^\mathbb{N} \to X^\mathbb{N} .
$$

## Generalizations

### In other categories

A similar definition of shift can be given in other [[categories]] with [[products]], and more generally in any [[copy-discard category]]. In the field of [[dynamical systems]], for example, the following categories are of interest:

* The category of [[compact]] [[metric spaces]];
* The [[Meas|category of measurable spaces and measurable maps]];
* The [[Prob|category of probability spaces and measure-preserving maps]];
* The [[Krn|category of probability spaces and measure preserving Markov kernels]].

(Outside the cartesian case, one needs a notion of [[infinite tensor product]].)


### For generic actions

One can generalize the definition as follows. 
Let $M$ be a [[monoid]] with an [[action]] on a finite set $S=\{1,\dots,n\}$, and denote the action by $m:S\to S$ for each $m\in M$. 

Given an object $X$ in a [[category]], consider the $S$-fold [[product]] $X^S$. We have an action of $M$ on $X^S$ given as follows. For each $m\in M$, we define the map $m^*:X^S\to X^S$ in terms of its product projections $\pi_i\circ m^*:X^S\to X$ given by
$$
\pi_i\circ m^* \;\coloneqq\; \pi_{m(i)} .
$$

Similarly, if $S$ is an infinite set, we define the action of $M$ on the infinite product $X^S$ whose finitary product projections are in the form above.

Even more generally, one can replace the product with an [[infinitary tensor product]], and define the action analogously.


#### Examples

* The [usual shift](#definition) $\sigma:X^\mathbb{N}\to X^\mathbb{N}$ is induced by the action of $\mathbb{N}$ on itself via addition.
* The [[exchangeability|action of finite permutations]] on $X^\mathbb{N}$ is induced by the action of finite permutations on $\mathbb{N}$.


## Universal property

Let $M$ be a monoid, and let $C$ be a [[category]] with [[products]]. Denote by $B M$ the [[delooping]] of $M$, and by $[B M, C]$ the [[functor category]], i.e. the category of objects of $C$ equipped with an [[action]] of $M$, and [[equivariant maps]] as morphisms.

The forgetful functor $U:[B M,C]\to C$ has a [[right adjoint]], given by the action of $M$ via shifts: on objects, it maps an object $X$ of $C$ to the product $X^M$, with the action of $M$ via shifts induced by the right-multiplication $M\times M\to M$.

On $C$, this adjunction induces a [[comonad]], the [[stream comonad]].

(...)


## See also

* [[exchangeability]], [[action]]
* [[stationary stochastic process]]
* [[stream comonad]]


## References

* Mike Behrisch, Sebastian Kerkhoff, Reinhard Pöschel, Friedrich Martin Schneider, Stefan Siegmund, _Dynamical systems in categories_. Applied Categorical Structures 25, 2017. ([link](https://tud.qucosa.de/api/qucosa%3A27340/attachment/ATT-0/))

* [[Paolo Perrone]], _Starting Category Theory_, World Scientific, 2024. ([website](https://www.worldscientific.com/worldscibooks/10.1142/13670))

(...)


category: probability


[[!redirects shifts]]
[[!redirects shift map]]
[[!redirects shift invariant]]
[[!redirects shift-invariant]]
[[!redirects shift invariance]]
[[!redirects shift-invariance]]