
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# The set-theoretic multiverse

* table of contents
{: toc}

## Idea

The **set-theoretic multiverse** is a philosophical perspective on [[set theory]], advocated by [[Joel David Hamkins]], according to which 

> there are many distinct concepts of set, each instantiated in a corresponding set-theoretic universe.

This is in contrast to the "universe view", which 

> asserts that there is an absolute background set concept, with a corresponding absolute set-theoretic universe in which every set-theoretic question has a definite answer.

The set-theoretic multiverse is at least informally analogous to such categorical notions as [[Topos]], the [[2-category]] of [[toposes]], with each topos regarded as a universe of ("variable") sets. See at _[[topos theory]]_ and at _[[categorical logic]]_ for more on this.

## In dependent type theory

In [[dependent type theory]], the set-theoretic multiverse is given by the existence of multiple inequivalent models of [[set theory]] as [[types]] $V$ with [[well-founded relations]] $\in$, which are made into [[Tarski universes]] via the [[dependent sum type]]:

$$x:V \vdash \mathrm{El}(x) \coloneqq \sum_{y:V} y \in x$$

In addition, this extends to any other notion of [[set theory]], such as the categorical models of set theory as [[well-pointed categories]] $\mathcal{E}$, which are made into [[Tarski universes]] by the [[hom-set]]

$$x:V \vdash \mathrm{El}(x) \coloneqq \mathrm{hom}(1, x)$$

where $1:\mathcal{E}$ is the [[terminal object|terminal]] [[separator]] of the category $\mathcal{E}$. 

This all coexists with the usual type theoretic notion of universes of sets as [[Tarski universes]] $U$ with universal type family $T$ in which for every type $A:U$ in the universe, $T(A)$ satisfies [[UIP]]. 

## Related (or unrelated) concepts

* [[multiverse]] (in [[cosmology]])



## References

* {#Hamkins12} [[Joel David Hamkins]], *The set-theoretic multiverse*, Review of Symbolic Logic 5:416-449 (2012), [arxiv](https://arxiv.org/abs/1108.4223)

* [[Claudio Ternullo]], *Maddy on the Multiverse*, in: *[[Reflections on the Foundations of Mathematics]]*, Synthese Library **407** Springer (2019) &lbrack;[doi:10.1007/978-3-030-15655-8_3](https://doi.org/10.1007/978-3-030-15655-8_3), [pdf](https://www.claudioternullo.com/_files/ugd/8787da_7474d586e9034716b2eea201b3e00191.pdf)&rbrack;

* [n-Cafe blog discussion](https://golem.ph.utexas.edu/category/2011/08/the_settheoretic_multiverse.html)
