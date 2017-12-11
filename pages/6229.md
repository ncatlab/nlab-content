
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

In _[[probability theory]]_, a _probability space_ is a [[measure space]] $(X,\mu)$ whose [[measure]] $\mu$ is a [[probability distribution]]: its [[integral]] is $\int_X \mu = 1$ (e.g. [Dembo 12, 1.1](#Dembo12)).

One thinks of the elements $x\in X$ as possible configurations of a system subject to randomness, hence of $X$ as a space of "[[possible worlds]]" in the idealized situation under consideration, and for any [[subset]] $U \subset X$ one thinks of $\int_U \mu$ as the [[probability]] that the system is found in a configuration $x$ which lies in $U$.

Accordingly, a [[measurable function]] $f$ on a probability space has the interpretation of a _[[random variable]]_. Its [[integral]] $\langle f\rangle \coloneqq \int_X f \cdot\mu$ is its [[expectation value]].

## Related concepts

* [[random variable]]

* [[expectation value]], [[moment]]

* [[entropy]]

* [[quantum probability space]]

## References

The modern formal concept originates around

* {#Kolmogorov33} [[Andrey Kolmogorov]], _Grundbegriffe der Wahrscheinlichkeitsrechnung_, Ergebnisse der Mathematik und Ihrer Grenzgebiete, Springer Berlin Heidelberg, 1933

Surveys and lecture notes include

* {#Dembo12} [[Amir Dembo]], _Probability theory_, 2012 ([pdf](http://statweb.stanford.edu/~adembo/stat-310a/lnotes.pdf))

[[!redirects probability spaces]]
