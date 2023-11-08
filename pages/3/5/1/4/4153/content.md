
# Dependent choice
* table of contents
{: toc}

## Statement

### In set theory

In [[set theory]], the axiom of **dependent choice** (DC) states that if $X$ is a nonempty ([[inhabited set|inhabited]]) set and if $R$ is a [[entire relation|total]] binary relation on $X$, then there exists a sequence $x\colon \mathbb{N} \to X$ such that $(x_n, x_{n+1})$ belongs to $R$ for all $n \in \mathbb{N}$. It is strictly weaker than the full [[axiom of choice]], but strictly stronger than the axiom of [[countable choice]]. It is called _dependent_ choice because the available choices for $x_{n+1}$ depend on the choice of $x_n$ made at the previous stage.

### In dependent type theory

In [[dependent type theory]], the **axiom of dependent choice** states that if $A$ is an [[inhabited set]] and if $R$ is a [[entire relation]] on $A$, then then there exists a sequence $a:\mathbb{N} \to A$ such that for all $n:\mathbb{N}$, $R(a(n), a(n + 1))$ holds. 

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash x:A, y:A \vdash R(x, y) \; \mathrm{type}}{\Gamma \vdash \mathrm{DC}_\mathbb{N}^A:(\mathrm{isSet}(A) \times [A]) \to \left(\prod_{x:A} \left(\prod_{y:A} \mathrm{isProp}(R(x, y))\right) \times \exists y:A.R(x, y)\right) \to \exists a:\mathbb{N} \to A.\prod_{n:\mathbb{N}} R(a(n), a(n + 1))}$$

## Applications

Typical applications of dependent choice include [[Kőnig's lemma]] and the [[Baire category theorem]] for [[complete metric spaces]].


## Acceptability

For a number of schools of [[constructive mathematics]], dependent choice is considered an acceptable alternative to full AC, and the principle holds (assuming that it holds in [[Set]]) in quite a few [[toposes]] of interest in which full AC doesn't hold, including all [[presheaf toposes]] and the [[effective topos]].  In fact, it follows from the stronger [[presentation axiom]], which holds in many of these toposes and also has a constructive justification.

Like countable choice, it fails for sheaves over the space of real numbers.

## Related concepts

* [[axiom of choice]]

* [[axiom of countable choice]]

## References

* Wikipedia, [Axiom of dependent choice](https://en.wikipedia.org/wiki/Axiom_of_dependent_choice)


category: foundational axiom

[[!redirects dependent choice]]
[[!redirects dependent choices]]
[[!redirects axiom of dependent choice]]
[[!redirects axiom of dependent choices]]
