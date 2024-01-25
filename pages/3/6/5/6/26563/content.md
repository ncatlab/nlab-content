[[!redirects standard Borel]]
[[!redirects standard Borel]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

*Standard Borel spaces* are particular measurable spaces, well suited for a number of constructions in traditional probability theory, such as for forming [[conditional probability]].

The real line is in particular a standard Borel space.

From the point of view of [[categorical probability]] they form a particularly well-behaved [[Markov category]], [[Stoch#borelstoch|BorelStoch]].



## Definitions

A [[topological space]] is called **completely separably metrizable** if the [[topology]] can be metrized by a [[complete metric|complete]] and [[separable]] [[metric]].
These spaces are also called [[Polish spaces]], see there for more information.

A [[measurable space]] is called a **standard Borel space** if it can be written as a Polish space with its [[Borel sigma-algebra]].

By analogy, a [[measure space]] (for example a [[probability space]]) is called a **standard Borel measure space** if and only if its underlying measurable space is standard Borel as above.


## Examples

* The real line is a standard Borel space.

* Every finite or countable set, equipped with the discrete sigma-algebra, is a standard Borel spaces.

Up to isomorphism of measurable spaces, these are the only examples. Note in particular that all finite powers of the real line and all intervals, as measurable spaces, are isomorphic to the real line.


## Categories of standard Borel spaces

* The [[category]] *BorelMeas* (or *Pol*) has as [[objects]] standard Borel measurable spaces, and as [[morphisms]] [[measurable functions]].
(Sometimes, depending on the author, *Pol* denotes the category of completely metrizable topological spaces and *continuous* maps.)

* The category [[Stoch#borelstoch|BorelStoch]] has as objects standard Borel spaces, and as morphisms [[Markov kernels]] between them.

* The [[category of couplings]] has as objects standard Borel *measure* (not just *measurable*) spaces, and either equivalence classes of Markov kernels between them (under [[Markov kernel#almost_sure_equality|almost sure equality]]), or [[coupling (probability)|couplings]] between them.


## Properties

* The [[sigma-algebra]] of a standard Borel space is countably generated and separating.

This has a number of consequences, for example:

* Every [[Markov kernel]] between standard Borel probability spaces admits a [[Markov kernel#bayesian_inversion|Bayesian inverse]].

* *Disintegration theorem:* For every sub-sigma-algebra of a standard Borel space, conditional expectation gives rise to a [[Markov kernel#regular_conditional_distributions|regular conditional distribution]].

* Standard Borel spaces admit countably [[infinite tensor products]].

* The [[Giry monad]] preserves standard Borel spaces: if $X$ is a standard Borel space, its functorial image $P X$ is standard Borel too. Therefore the Giry monad restricts to a monad on *Pol*, usually known under the same name.






## Related Concepts

* [[quasi-Borel space]]
* [[Polish space]]
* [[measurable space]]
* [[Stoch]]
* [[Markov kernel]]

## References

(...)


[[!redirects standard Borel]]
[[!redirects standard Borel spaces]]
[[!redirects Pol]]