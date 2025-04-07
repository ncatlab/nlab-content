 
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

### In dependent type theory

In [[dependent type theory]], the **axiom of dependent choice** states that if $A$ is an [[inhabited set]] and if $R$ is a [[entire relation]] on $A$, then then there exists a sequence $a:\mathbb{N} \to A$ such that for all $n:\mathbb{N}$, $R(a(n), a(n + 1))$ holds. 

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A, y:A \vdash R(x, y) \; \mathrm{type}}{\Gamma \vdash \mathrm{DC}_{A}^{R}:(\mathrm{isSet}(A) \times [A]) \to \left(\prod_{x:A} \left(\prod_{y:A} \mathrm{isProp}(R(x, y))\right) \times \exists y:A.R(x, y)\right) \to \exists a:\mathbb{N} \to A.\prod_{n:\mathbb{N}} R(a(n), a(n + 1))}$$

If the dependent type theory has a [[type of all propositions]] $\mathrm{Prop}$, this can be simplified down to the [[inference rule]]

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{DC}_{A}:(\mathrm{isSet}(A) \times [A]) \to \prod_{R:A \times A \to \mathrm{Prop}} \left(\prod_{x:A} \exists y:A.R(x, y)\right) \to \exists a:\mathbb{N} \to A.\prod_{n:\mathbb{N}} R(a(n), a(n + 1))}$$

## Applications

Typical applications of dependent choice include [[Kőnig's lemma]] and the [[Baire category theorem]] for [[complete metric spaces]].

## Acceptability

The axiom of dependent choice holds in the [[topos]] of [[condensed sets]] and the [[topos]] of [[light condensed sets]], assuming the [[axiom of choice]] in the [[category of sets]]. 

For a number of schools of [[constructive mathematics]], dependent choice is considered an acceptable alternative to full AC, and the principle holds (assuming that it holds in [[Set]]) in quite a few [[toposes]] of interest in which full AC doesn't hold, including all [[presheaf toposes]] and the [[effective topos]].  In fact, it follows from the stronger [[presentation axiom]], which holds in many of these toposes and also has a constructive justification.

Like countable choice, it fails for sheaves over the space of real numbers.

## Variations

### Dependent $n$-choice and $\infty$-choice

In [[dependent type theory]], the axiom of dependent choice requires that $A$ be a [[set]]. This can be generalised to the **axiom of dependent $n$-choice** by replacing the set requirement with an $n$-truncation requirement for $A$: if $A$ is an inhabited $n$-truncated type and if $R$ is a [[entire relation]] on $A$, then then there exists a sequence $a:\mathbb{N} \to A$ such that for all $n:\mathbb{N}$, $R(a(n), a(n + 1))$ holds. 

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A, y:A \vdash R(x, y) \; \mathrm{type}}{\Gamma \vdash \mathrm{DC}_{n, A}^{R}:(\mathrm{is}n\mathrm{type}(A) \times [A]) \to \left(\prod_{x:A} \left(\prod_{y:A} \mathrm{isProp}(R(x, y))\right) \times \exists y:A.R(x, y)\right) \to \exists a:\mathbb{N} \to A.\prod_{n:\mathbb{N}} R(a(n), a(n + 1))}$$

These are stronger axioms as $n$ increases. 

In the limit as $n$ goes to infinity, this is called the **axiom of dependent infinity-choice**, where $A$ doesn't have any truncation requirements: if $A$ is an inhabited type and if $R$ is a [[entire relation]] on $A$, then then there exists a sequence $a:\mathbb{N} \to A$ such that for all $n:\mathbb{N}$, $R(a(n), a(n + 1))$ holds. 

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A, y:A \vdash R(x, y) \; \mathrm{type}}{\Gamma \vdash \mathrm{DC}_{\infty, A}^{R}:[A] \to \left(\prod_{x:A} \left(\prod_{y:A} \mathrm{isProp}(R(x, y))\right) \times \exists y:A.R(x, y)\right) \to \exists a:\mathbb{N} \to A.\prod_{n:\mathbb{N}} R(a(n), a(n + 1))}$$

### Dependent choice for the natural numbers

Dependent choice for the [[natural numbers]] $\mathrm{DC}_\mathbb{N}$ states that if $R$ is a [[entire relation]] on $\mathbb{N}$, then there exists a sequence $x$ in $\mathbb{N}$ such that $R(x_n, x_{n+1})$ holds for all $n \in \mathbb{N}$. $\mathrm{DC}_\mathbb{N}$ is enough to prove that every [[Dedekind real number]] is a [[Cauchy real number]] (the converse is always true).

In dependent type theory this is given by the following [[inference rule]]:

$$\frac{\Gamma, x:\mathbb{N}, y:\mathbb{N} \vdash R(x, y) \; \mathrm{type}}{\Gamma \vdash \mathrm{DC}_\mathbb{N}^{R}:\left(\prod_{x:\mathbb{N}} \left(\prod_{y:\mathbb{N}} \mathrm{isProp}(R(x, y))\right) \times \exists y:\mathbb{N}.R(x, y)\right) \to \exists a:\mathbb{N} \to \mathbb{N}.\prod_{n:\mathbb{N}} R(a(n), a(n + 1))}$$

If the dependent type theory has a [[type of all propositions]] $\mathrm{Prop}$, this can be simplified down to the [[axiom]]

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{DC}_\mathbb{N}:\prod_{R:\mathbb{N} \times \mathbb{N} \to \mathrm{Prop}} \left(\prod_{x:\mathbb{N}} \exists y:\mathbb{N}.R(x, y)\right) \to \exists a:\mathbb{N} \to \mathbb{N}.\prod_{n:\mathbb{N}} R(a(n), a(n + 1))}$$

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
