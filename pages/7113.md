+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

An _archimedean field_ is an [[ordered field]] that satisfies the [[archimedean property]].

## Definition

The [[rational numbers]] are the [[initial]] [[ordered field]], so for every ordered field $F$ there is a field homomorphism $h:\mathbb{Q}\to F$. $F$ is _archimedean_ if for all elements $a\in F$ and $b\in F$, if $a \lt b$, then there exists a rational number $q\in \mathbb{Q}$ such that $a \lt h(q)$ and $h(q) \lt b$. 

## Properties

Every archimedean field is a [[dense linear order]]. This means that the [[Dedekind completion]] of every archimedean field is the field of [[real numbers]]. 

Every archimedean field is a [[differentiable space]]:

### Pointwise continuous functions

Let $F$ be an Archimedean field. A function $f:F \to F$ is __continuous at a point__ $c \in F$ if 

$$isContinuousAt(f, c) \coloneqq \forall \epsilon \in (0, \infty). \forall x \in F. \exists \delta \in (0, \infty). (\vert x - c \vert \lt \delta) \implies (\vert f(x) - f(c) \vert \lt \epsilon)$$

$f$ is __pointwise continuous__ in $F$ if it is continuous at all points $c$:
$$isPointwiseContinuous(f) \coloneqq \forall c \in F. isContinuousAt(f, c)$$

The set of all pointwise continuous functions is defined as 

$$C^0(F) \coloneqq \{f \in F \to F \vert isPointwiseContinuous(f)\}$$

### Pointwise differentiable functions

Let $F$ be an Archimedean field. A function $f:F \to F$ is __differentiable at a point__ $c \in F$ if 

$$isDifferentiableAt(f, c) \coloneqq isContinuousAt(f, c) \times \exists L \in F. \forall \epsilon \in (0, \infty). \forall x \in F. \exists \delta \in (0, \infty). \forall h \in (-\delta, 0) \cup (0, \delta). \left| \frac{f(c + h) - f(c)}{h} - L \right| \lt \epsilon$$

$f$ is __pointwise differentiable__ in $F$ if it is differentiable at all points $c$:
$$isPointwiseDifferentiable(f) \coloneqq \forall c \in F. isDifferentiableAt(f, c)$$

The set of all pointwise differentiable functions is defined as 

$$D^0(F) \coloneqq \{f \in F \to F \vert isPointwiseDifferentiable(f)\}$$

## Examples

Archimedean fields include

* [[rational numbers]]
* [[real closed fields]]
* [[real numbers]]

Non-archimedean fields include

* [[finite fields]]

* [[complex numbers]]

* [[p-adic numbers]]

* [[surreal numbers]]

## Related concepts

* [[archimedean valued field]]

* [[archimedean integral domain]]

* [[archimedean group]]

* [[differentiable space]]

## References

The definition of the Archimedean property for an ordered field is given in section 4.3 of

* Auke B. Booij, *Analysis in univalent type theory* (2020) $[$[etheses:10411]( 	http://etheses.bham.ac.uk/id/eprint/10411), [pdf](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf)$]$

[[!redirects archimedean field]]
[[!redirects archimedean fields]]
[[!redirects non-archimedean field]]
[[!redirects non-archimedean fields]]
[[!redirects nonarchimedean field]]
[[!redirects nonarchimedean fields]]

[[!redirects Archimedean field]]
[[!redirects Archimedean fields]]
[[!redirects non-Archimedean field]]
[[!redirects non-Archimedean fields]]
