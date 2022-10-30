## Idea

The **density** of a subset $S \subseteq X$ is a measure of how "large" the subset is, or what proportion of $X$ one can consider $S$ to take up.

## Definition

Density is usually defined for subsets $S \subseteq \mathbb{N}$ of the natural numbers, or other countable sets, but the concept generalises to sets $X$ equipped with an exhaustive countable filtration $\emptyset \subseteq F_1 \subseteq F_2 \cdots \subseteq X$ (i.e., one such that $\bigcup_{n\in \mathbb{N}} F_n = X$), where each $F_n$ is equipped with a measure $\mu_n$ satisfying $\mu_n(F_n) \lt \infty$ and where each inclusion $F_n \to F_{n+1}$ is measure-preserving. We call such a filtration and system of measures $\mathcal{F} = \{F_n,\mu_n\}$ a _measured filtration_  on $X$.


The key example is of a totally ordered countable set $A = \{a_1,a_2,\ldots\}$ equipped with the filtration $F_n = \{a_1,\ldots a_n\}$ and the counting measure. For instance, $A$ could be the [[natural numbers]] $\mathbb{N}$, or any countable subset with the inherited ordering, such as the primes.

Notice that any finite set can also be given the structure of a measured filtration, with a filtration that stabilises after finitely many steps, and with the counting measure.

In the other direction, a $\sigma$-finite [[measure space]] $(M,\mu)$ can be equipped (by definition) with a measured filtration by measurable subsets, with the induced measures.

+-- {: .un_defn}
###### Definition
Given a measured filtration $(X,\mathcal{F})$, a subset $S \subseteq X$ with the property that $S\cap F_n$ is measurable for all $n$, the **$\mathcal{F}$-density of $S$** is defined to be the number
$$
    d_\mathcal{F}(S) = \lim_{n\to \infty} \frac{\mu_n(S\cap F_n)}{\mu_n(F_n)} \in [0,1],
$$
if this limit exists.

=--

For a finite set $B=\{b_1,\ldots,b_n\}$ equipped with any measured filtration $\mathcal{F}$, the $\mathcal{F}$-density of a subset $S \subseteq B$ agrees with the simple ratio $|S|/|B|$. 

Likewise, for any measure space $(M,\mu)$ of finite total measure and $S$ a measurable subset, we can relate $d_\mathcal{F}(S)$ to $\mu(S)/\mu(M)$ for various choices of measured filtration on $M$ ([[David Roberts|DR]]: does this depend on the choice of filtration?)


## Applications

Density arguments are of importance in counting [[prime numbers]] with certain properties, and have shown great utility in proving partial results about the Birch and Swinnerton-Dyer conjecture on [[elliptic curves]] (namely that it is true for a set of elliptic curves over $\mathbb{Q}$ with density roughly 67%). In this latter example, there are a number of filtrations on can place on the set of elliptic curves up to isomorphism, which only makes small changes to final calculated densities.

Any $\sigma$-finite measure $\mu$ of a set $M$ is equivalent, as a measure, to a [[probability measure]]. This is constructed by considering a filtration arising from a countable disjoint partition into measurable sets of finite measure.


## Upper and lower asymptotic density

One can also consider, instead of the _limit_ in the definition of density, which may or may not exist, the _lim sup_ or the _lim inf_. These give the **upper** and **lower (asymptotic) densities**, respectively.

## Related pages

* [[∞-finite measure]]


## References

* Wikipedia, [Natural density](https://en.wikipedia.org/wiki/Natural_density) (which deals only with the case of sets of natural numbers)

See also

* Wikipedia, [$\sigma$-finite measure](https://en.wikipedia.org/wiki/%CE%A3-finite_measure)

A great number of other definitions of densities of sets of natural numbers (clearly generalisable to other countable ordered sets) are given at

* [[OEIS]] wiki, [Density](https://oeis.org/wiki/Density)

