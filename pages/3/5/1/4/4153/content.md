 
# Dependent choice
* table of contents
{: toc}

## Statement

### In set theory

In [[set theory]], the axiom of **dependent choice** (DC) states that if $X$ is a nonempty ([[inhabited set|inhabited]]) set and if $R$ is a [[entire relation|total]] binary relation on $X$, then there exists a sequence $x\colon \mathbb{N} \to X$ such that $(x_n, x_{n+1})$ belongs to $R$ for all $n \in \mathbb{N}$. It is strictly weaker than the full [[axiom of choice]], but strictly stronger than the axiom of [[countable choice]]. It is called _dependent_ choice because the available choices for $x_{n+1}$ depend on the choice of $x_n$ made at the previous stage.

There is another way to express the axiom of dependent choice which uses [[surjections]] instead of entire relations: 

The **axiom of dependent choice** states that given a [[family of sets]] $X_n$ and a family of [[surjections]] $f_n:X_{n + 1} \to X_n$ indexed by natural numbers $n \in \mathbb{N}$: 
$$X_0 \overset{f_0}\leftarrow X_1 \overset{f_1}\leftarrow X_1 \overset{f_2}\leftarrow \ldots$$
the projection function to $X_0$ from the [[sequential limit]] $\underset{\leftarrow}\lim X_n$ of the above diagram is a surjection. 

### In a topos or pretopos

More generally, given an [[elementary topos]] or a [[pretopos]] $\mathcal{E}$ with [[sequential limits]], the **axiom of dependent choice** states that given a sequence of objects $X:\mathbb{N} \to \mathrm{Ob}(\mathcal{E})$ and a [[dependent sequence]] of [[epimorphisms]] $f_n:\mathrm{hom}_\mathcal{E}(X_{n + 1}, X_{n})$ indexed by $n \in \mathbb{N}$, the projection function to $X_0$ from the [[sequential limit]] $\underset{\leftarrow}\lim X_n$ of the above diagram is an epimorphism. 

## Applications

Typical applications of dependent choice include [[Kőnig's lemma]] and the [[Baire category theorem]] for [[complete metric spaces]].

## Acceptability

The axiom of dependent choice holds in the [[topos]] of [[condensed sets]] and the [[topos]] of [[light condensed sets]], assuming the [[axiom of choice]] in the [[category of sets]]. 

For a number of schools of [[constructive mathematics]], dependent choice is considered an acceptable alternative to full AC, and the principle holds (assuming that it holds in [[Set]]) in quite a few [[toposes]] of interest in which full AC doesn't hold, including all [[presheaf toposes]] and the [[effective topos]].  In fact, it follows from the stronger [[presentation axiom]], which holds in many of these toposes and also has a constructive justification.

Like countable choice, it fails for sheaves over the space of real numbers.

## Related concepts

* [[axiom of choice]]

* [[axiom of countable choice]]

## References

* Wikipedia, [Axiom of dependent choice](https://en.wikipedia.org/wiki/Axiom_of_dependent_choice)

* {#CCGM24} [[Felix Cherubini]], [[Thierry Coquand]], [[Freek Geerligs]], [[Hugo Moeneclaey]], *A Foundation for Synthetic Stone Duality* ([arXiv:2412.03203](https://arxiv.org/abs/2412.03203), [summary](https://felix-cherubini.de/condensed-summary.pdf))

* {#AB24} [[Mathieu Anel]], [[Reid Barton]], *Choice axioms and Postnikov completeness* ([arXiv:2403.19772](https://arxiv.org/abs/2403.19772))

category: foundational axiom

[[!redirects dependent choice]]
[[!redirects dependent choices]]
[[!redirects axiom of dependent choice]]
[[!redirects axioms of dependent choice]]
[[!redirects axiom of dependent n-choice]]
[[!redirects axioms of dependent n-choice]]
[[!redirects axiom of dependent infinity-choice]]
[[!redirects axioms of dependent infinity-choice]]
