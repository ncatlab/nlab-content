
> This page is about valuation in [[measure theory]]. For valuation in [[algebra]] (on [[rings]]/[[fields]]) see at _[[valuation]]_.

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A **valuation** is a construction analogous to that of a [[measure]], which is however more compatible with [[constructive mathematics]], and readily generalizable to contexts such as [[point-free topology]].

On most spaces of interest for measure theory and probability (such as [[metric spaces]]) the notions of suitably continuous valuations and measures coincide (see [below](#extending_valuations_to_measures)).


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

Note that, differently from measures, there is no explicit mention of [[complements]]. Moreover, the continuity condition can be interpreted, measure-theoretically, both as an analogue of $\sigma$-additivity, and as an analogue of a regularity condition (more precisely it corresponds to [[τ-additivity]]).
See [[correspondence between measure and valuation theory]] for more on this.

### Valuations on locales and topological spaces

Let $L$ be a [[locale]]. Then a valuation on $L$ is by definition a valuation on its [[frame]] $\mathcal{O}(L)$. Similarly, a valuation on a [[topological space]] is a valuation on the [[lattice of open subsets|lattice of its open sets]].

Valuations on locales are used in the [[topos approach to quantum mechanics]] and the [[Bohr topos]].

## Examples

### Dirac valuation

Let $X$ be a topological space, and let $x\in X$ be a point. The **Dirac valuation** at $x$, which we denote by $\delta_x$, maps an open set $U\subseteq X$ to
$$
\delta_x(U) \;\coloneqq\; 
\begin{cases}
1 & x\in U \\
0 & x\notin U.
\end{cases}
$$ 

These are the valuation analogue of [[Dirac measures]], and give the unit map of [[valuation monads]].
Note the analogy with [[neighborhood filters]]: Dirac measures can be considered a quantitative analogue thereof.

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

Valuations share a number of constructions which are similar to those for [[measures]]. The constructions below are given for the case of continuous valuations on [[topological spaces]].

### Pushforward

Given spaces $X$ and $Y$ and a continuous map $f:X\to Y$, we can map a valuation $\nu$ on $X$ to a valuation $f_*\nu$ on $Y$ in the following way. For every open set $U\subseteq Y$, we set
$$
f_*\nu (U) \coloneqq \nu(f^{-1}(U)) .
$$
The assignment gives a well-defined valuation, which is continuous if $\nu$ is continuous. We call $f_*\nu$ the **pushforward valuation** of $\nu$ along $f$.

Compare with the [[pushforward measure|analogous construction for measures]].

This construction allows to makes the assignment [[functor]], which is even a [[monad]] (see [[monads of probability, measures and valuations#functor_ unit_and_multiplication|measure monads]] for more on this).


### Joints, marginals and products

Given a valuation $\nu$ on a product space $X\times Y$, one calls its pushforward along the projection map $X\times Y\to X$ the **marginal** of $\nu$ on $X$. The same can be done for $Y$. 
The assignment from $\nu$ to the ordered pair of its marginals can be seen as an [[monoidal functor|oplax monoidal structure]] of the [[monads of probability, measures and valuations|valuation monad]].

Given valuations $\nu$ on $X$ and $\rho$ on $Y$, there may be many possible valuations on $X\times Y$ which have $\nu$ and $\rho$ as their marginals. Any such valuation on $X\times Y$ is called a **joint valuation** or **coupling** of $\nu$ and $\rho$.

Between the many joints of $\nu$ and $\rho$ there is always a canonical choice, namely the **product valuation** $\nu\otimes\rho$. 
From the point of view of [[probability theory]], this corresponds to a distribution exhibiting [[independence]] between $\nu$ and $\rho$.
On the [[basis]] of the [[product topology]] of $X\times Y$ given by sets in the form $U\times V$ for $U\subseteq X$ and $V\subseteq Y$ open, the product valuation is given by 
$$
\nu\otimes\rho (U\times V) \coloneqq \nu(U)\cdot\rho(V).
$$
Note that this is not enough to define a valuation a priori. For continuous valuations, however, this turns out to be the well-defined, as proven for example in [Heckmann '96](#Heckmann96).

The assignment to $\nu$ and $\rho$ of their product valuation can be seen as a [[monoidal functor|lax monoidal structure]] of the [[monads of probability, measures and valuations|valuation monad]].
See also [[monads of probability, measures and valuations#monoidal_structure]].


### Null sets and support

Valuations admit a notion of [[support]] similar to that of measures. In particular, continuous valuations, just as [[tau-additive measure|$\tau$-additive measures]], have a well-defined and well-behaved support.

Let $\nu$ be a valuation on a [[locale]] or [[topological space]] $X$, and $U$ an open set of $X$ (i.e. an element of the corresponding [[frame]]). We say that $U$ is a **null** or **measure zero set** for $\nu$ if $\nu(U)=0$. The [[complement]] of $U$, which is a [[closed subspace#locales|closed subspace]] of $X$, is said to have **full measure**.

Since a finite union of null sets is null, null sets form a directed net in the frame. Therefore, if $\nu$ is a continuous valuation, it admits a unique maximal null open set. The [[complement]] of this set, which is the largest closed subspace of full measure, is called the **[[support]]** of $\nu$.

The support induces a [[monad#the_bicategory_of_monads|morphism of monads]] (see [Fritz-Perrone-Rezagholi](#support), section 5). 


### Integration

There is an integration theory for valuation analogous to that of measures, where the [[open sets]] play the role of the [[measurable sets]], and lower [[semicontinuous functions]] play the role of [[measurable functions]]
(see also [[correspondence between measure and valuation theory]]).
Sometimes integration of valuation is known as **lower integration**, since approximations are done from below.

The way to define integration, mutatis mutandis, parallels usual [[Lebesgue integral]] construction.
We sketch the construction for the case of topological spaces.

Let $\nu$ be a valuation on a space $X$.

* Given an open set $U\subseteq X$, and denoting by $1_U$ its [[indicator function]], we define
$$
\int 1_U \, d\nu \;\coloneqq\; \nu(U) .
$$

* A [[simple function|simple]] lower semicontinuous function is a lower semicontinuous function assuming only finitely many values. Such functions can be expressed (nonuniquely) as finite positive linear combinations of indicator functions:
$$
f \;=\; \sum_i r_i \, 1_{U_i} .
$$
We define the integral of a simple $f$ as
$$
\int f \, d\nu \;\coloneqq\; \sum_{i}r_i \nu(U_i) .
$$
This is well-defined, i.e.~it depends only on $f$ and not on the particular way of expressing $f$ as a linear combination of indicators. 

* Every lower semicontinuous function can be written as pointwise directed supremum of simple lower semicontinuous functions. So suppose $g:X\to[0,\infty]$ is lower semicontinuous. Take an increasing net $(g_\alpha)_{\alpha\in A}$ of nonnegative simple lower semicontinuous functions. Then we define 
$$
\int g \, d\nu \;\coloneqq\; \sup_\alpha \int g_\alpha\,d\nu ,
$$
where the integral on the right is the one defined above for simple functions, and the supremum on the right is either the one of real numbers (or lower real numbers), or $+\infty$. 

This integral satisfies analogous properties to the Lebesgue integral, such as [[linear map|linearity]] and [[Scott continuity]] (cfr. the [[monotone convergence theorem|sequential monotone continuity]] of the Lebesgue integral). 


## Monads of valuations

Just as there are several [[monads of measures]] (such as the [[Giry monad]]), there are a number of analogous [[monads]] of valuations.
The most famous are

* The [[extended probabilistic powerdomain]] on the [[Top|category of topological spaces]], which was introduced by [Heckmann 96](#Heckmann96). 

* The [[valuation monad on locales]], defined by [Steve Vickers](#vmonad).

* The [[probabilistic powerdomain]] on the category of [[dcpo|dcpos]], defined by Jones and Plotkin, of wide use in theoretical computer science.

See also the list at [[monads of probability, measures, and valuations]].


## Extending valuations to measures

As we have seen [above](#borel_measures), a [[Borel measure]] always restricts to a valuation. It is natural to ask the converse question of whether a valuation can always be extended to a Borel measure. In general, the answer is negative. In the case of *continuous* valuations, however, one would expect that in many cases the valuation can be extended to a [[tau-additive measure|$\tau$-additive Borel measure]]. 

The question is known, for example, to be true on all regular Hausdorff ($T_3$) spaces: 

+-- {: .num_theorem #ExtensionOfValuationToBorelMeasure}
###### Theorem

A locally finite continuous valuation on a [[regular topological space]]
extends uniquely to a regular τ-smooth [[Borel measure]].
A locally finite continuous valuation on a [[locally compact]] [[sober space]]
extends uniquely to a τ-smooth [[Borel measure]].

=--

([Manilla 02, Theorems 4.4 and 4.12](#Manilla02))

This includes in particular every [[metric space]], and every compact Hausdorff space. So, in many spaces of interest for analysis and probability theory, working with measures and working with valuations is only a difference in the language. 

The more general question of whether one can extend a finite continuous valuation to a Borel measure on any sober space, at the present time, is still open. 

### Particular cases

* Every Dirac valuation can be extended to the corresponding [[Dirac measure]].

* The pushforward of an extendable valuation along a [[continuous map]] is again extendable, and the resulting [[measure]] is the [[pushforward measure]] of the extension. (Equivalently, the restriction of measures to valuations is a [[natural transformation]]).

* The above specializes to the fact that marginals of extendable valuations are extendable, and the resulting measure is the [[marginal measure]]. 

* Somewhat conversely, the product of extendable valuations is extendable, and the resulting measure is the [[product measure]] of the extensions.

* The integration, given by the multiplication map $E: P P X \to P X$ of the [[extended probabilistic powerdomain]], maps extendable valuations to extendable valuations, and the resulting measure is the integral of the extension. Therefore there is a [[monad#the_bicategory_of_monads|morphism of monads]] exhibiting [[τ-additive measures]] as a submonad of valuations. (See also [[extended probabilistic powerdomain#the_measure_monad_on_top|the measure monad on Top]].)

## See also

* [[monads of probability, measures, and valuations]]
* [[correspondence between measure and valuation theory]]
* [[monad]], [[Giry monad]], [[monads in computer science]]
* [[extended probabilistic powerdomain]], [[probabilistic powerdomain]], [[valuation monad on locales]]
* [[probability valuation]]
* [[sigma-continuous valuation]], [[sigma-continuous probability valuation]]
* [[content]], [[probability content]]
* [[measure]], [[τ-additive measure]], [[probability measure]]




## References

* {#Heckmann96} Reinhold Heckmann, _Spaces of valuations_, Papers on General Topology and Ap-plications, 1996 ([doi:10.1111/j.1749-6632.1996.tb49168.x](https://doi.org/10.1111/j.1749-6632.1996.tb49168.x),[pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.45.5845&rep=rep1&type=pdf))

* Mauricio Alvarez-Manilla, Achin Jung, [[Klaus Keimel]], _The probabilistic powerdomain for stably compact spaces_, Theoretical Computer Science 328, 2004 ([doi:10.1016/j.tcs.2004.06.021](https://doi.org/10.1016/j.tcs.2004.06.021))

* {#algebras} [[Jean Goubault-Larrecq]] and Xiaodong Jia, _Algebras of the extended probabilistic powerdomain monad_, ENTCS 345, 2019
([doi:10.1016/j.entcs.2019.07.015](https://doi.org/10.1016/j.entcs.2019.07.015))

* {#support} [[Tobias Fritz]], [[Paolo Perrone]] and Sharwin Rezagholi, _Probability, valuations, hyperspace: Three monads on Top and the support as a morphism_, 2019 ([arXiv:1910.03752](https://arxiv.org/abs/1910.03752))


For valuations on locales, see

* {#vmonad} [[Steve Vickers]], _A monad of valuation locales_, 2011 ([pdf](https://www.cs.bham.ac.uk/~sjv/Riesz.pdf))

For the theory of [integration over valuations](#integration), see 

* {#kirch} Olaf Kirch, _Bereiche und Bewertungen_ (in German), Master Thesis, Technische Hochschule Darmstadt, 1993 ([ps.gz](http://fb04286.mathematik.tu-darmstadt.de/fbereiche/logik/research/Domains/papers/kirch/diplom.ps.gz))

* {#jung} Achim Jung, _Stably compact spaces and the probabilistic powerspace construction_, ENTCS 87, 2004 ([doi:10.1016/j.entcs.2004.10.001](https://doi.org/10.1016/j.entcs.2004.10.001)).



* [[Thierry Coquand]] and [[Bas Spitters]], _Integrals and Valuations_, 2009,  	Logic and Analysis (2009) 1(3) p.1-22 ([arXiv:0808.1522](https://arxiv.org/abs/0808.1522))

Integration on locales can be found in

* {#vintegral} [[Steve Vickers]], _A localic theory of lower and upper integrals_, 2008 ([doi:10.1002/malq.200710028](https://doi.org/10.1002/malq.200710028))


For the problem of [extending valuations to measures](#extending_valuations_to_measures), see

* Mauricio Alvarez-Manilla, Abbas Edalat, and Nasser Saheb-Djahromi, _An extension result for continuous valuations_, 1998 (<a href="https://doi.org/10.1016/S1571-0661(05)80210-5">doi:10.1016/S1571-0661(05)80210-5</a>)

* {#Manilla00} Mauricio Alvarez-Manilla, _Measure theoretic results for continuous valuations on partially ordered spaces_, Dissertation, 2000 ([ps.gz](http://www.cs.tufts.edu/~nr/cs257/archive/mauricio-alvarez-manilla/public.ps.gz))

*  {#Manilla02} Mauricio Alvarez-Manilla, _Extension of valuations on locally compact sober spaces_, Topology and its Applications Volume 124, Issue 3, 20 October 2002, Pages 397-433 (<a href="https://doi.org/10.1016/S0166-8641(01)00249-8">doi:10.1016/S0166-8641(01)00249-8</a>)


* Alex Simpson, [Measure, randomness and sublocales](https://www.sciencedirect.com/science/article/pii/S0168007211001874). 

* [[Klaus Keimel]] and [[Jimmie D. Lawson]], _Measure extension theorems for_
$T_0$ _spaces_, 2004 ([doi:10.1016/j.topol.2004.02.019](https://doi.org/10.1016/j.topol.2004.02.019))

[[!redirects continuous valuation]]
[[!redirects continuous valuations]]
