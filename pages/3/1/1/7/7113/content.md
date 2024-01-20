
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

An _Archimedean ordered field_ is an [[ordered field]] that satisfies the [[archimedean property]].

## Definition

### Using field homomorphisms from the rationals

The [[rational numbers]] are the [[initial]] [[ordered field]], so for every ordered field $F$ there is a field homomorphism $h:\mathbb{Q}\to F$. $F$ is _Archimedean_ if for all elements $a\in F$ and $b\in F$, if $a \lt b$, then there exists a rational number $q\in \mathbb{Q}$ such that $a \lt h(q)$ and $h(q) \lt b$. 

### Using Dedekind cut-like conditions

A [[real number]] in an [[ordered field]] $F$ is an element $x \in F$ which satisfies the [[Dedekind cut]] axioms:

1. there exists a rational number $q \in \mathbb{Q}$ such that $q \lt x$
1. there exists a rational number $r \in \mathbb{Q}$ such that $x \lt r$
1. for all rational numbers $q \in \mathbb{Q}$ and $q' \in \mathbb{Q}$, $q \lt q'$ and $q' \lt x$ implies that $q \lt x$
1. for all rational numbers $r \in \mathbb{Q}$ and $r' \in \mathbb{Q}$, $x \lt r'$ and $r' \lt r$ implies that $x \lt r$
1. for all rational numbers $q \in \mathbb{Q}$, $q \lt x$ implies that there exists a rational number $q' \in \mathbb{Q}$, such that $q \lt q'$ and $q' \lt x$
1. for all rational numbers $r \in \mathbb{Q}$, $x \lt r$ implies that there exists a rational number $r' \in \mathbb{Q}$, such that $x \lt r'$ and $r' \lt r$
1. for all rational numbers $q \in \mathbb{Q}$ and $r \in \mathbb{Q}$, $q \lt x$ and $x \lt r$ implies that $q \lt r$
1. for all rational numbers $q \in \mathbb{Q}$ and $r \in \mathbb{Q}$, $q \lt r$ implies that $q \lt x$ or $x \lt r$

We have the following results:

* The first and second conditions say that every element $x \in F$ is bounded below and above by rational numbers, and thus strictly not an [[infinite]] element. 

* The fifth and sixth conditions imply that every element $x \in F$ is strictly not an [[infinitesimal]] element. 

These four conditions together imply the [[archimedean property]] for the ordered field $F$. 

* The third, fourth, and seventh conditions are always true for all elements $x \in F$ because of transitivity of the [[strict order]] relation. 

* Finally, the eighth condition says that every element $x \in F$ is located, and is true for all elements $x \in F$ because the [[pushout]] of the [[open intervals]] $(q, \infty)$ and $(-\infty, r)$ with canonical inclusions $(q, r) \to (q, \infty)$ and $(q, r) \to (-\infty, r)$ is equivalent to $F$ itself. 

Thus, an **Archimedean ordered field** is an ordered field $F$ where every element $x \in F$ is a real number. 

Note that this definition is not the same as saying that $F$ contains every [[real number]] - the latter definition results in the [[Dedekind real numbers]], which is the union of all Archimedean ordered fields and the [[terminal object|terminal]] Archimedean ordered field. 

## Properties

Every Archimedean ordered field is a [[dense linear order]]. This means that the [[Dedekind completion]] of every Archimedean ordered field is the field of all [[real numbers]]. 

Every Archimedean ordered field is a [[differentiable space]]:

### Pointwise continuous functions

Let $F$ be an Archimedean ordered field. A function $f:F \to F$ is __continuous at a point__ $c \in F$ if 

$$isContinuousAt(f, c) \coloneqq \forall \epsilon \in (0, \infty). \forall x \in F. \exists \delta \in (0, \infty). (\vert x - c \vert \lt \delta) \implies (\vert f(x) - f(c) \vert \lt \epsilon)$$

$f$ is __pointwise continuous__ in $F$ if it is continuous at all points $c$:
$$isPointwiseContinuous(f) \coloneqq \forall c \in F. isContinuousAt(f, c)$$

The set of all pointwise continuous functions is defined as 

$$C^0(F) \coloneqq \{f \in F \to F \vert isPointwiseContinuous(f)\}$$

### Pointwise differentiable functions

Let $F$ be an Archimedean ordered field. A function $f:F \to F$ is __differentiable at a point__ $c \in F$ if 

$$isDifferentiableAt(f, c) \coloneqq isContinuousAt(f, c) \times \exists L \in F. \forall \epsilon \in (0, \infty). \forall x \in F. \exists \delta \in (0, \infty). \forall h \in (-\delta, 0) \cup (0, \delta). \left| \frac{f(c + h) - f(c)}{h} - L \right| \lt \epsilon$$

$f$ is __pointwise differentiable__ in $F$ if it is differentiable at all points $c$:
$$isPointwiseDifferentiable(f) \coloneqq \forall c \in F. isDifferentiableAt(f, c)$$

The set of all pointwise differentiable functions is defined as 

$$D^0(F) \coloneqq \{f \in F \to F \vert isPointwiseDifferentiable(f)\}$$

## Examples

Archimedean ordered fields include

* [[rational numbers]]
* [[real closed fields]]
* [[real numbers]]

Non-Archimedean ordered fields include

* [[finite fields]]

* [[complex numbers]]

* [[p-adic numbers]]

* [[surreal numbers]]

## Related concepts

* [[archimedean valued field]]

* [[archimedean integral domain]]

* [[archimedean group]]

* [[Archimedean ordered Artinian local ring]]

* [[Archimedean ordered reduced local ring]]

* [[Archimedean ordered local integral domain]]

* [[differentiable space]]

## References

The definition of the Archimedean property for an ordered field is given in section 4.3 of

* Auke B. Booij, *Analysis in univalent type theory* (2020) $[$[etheses:10411]( 	http://etheses.bham.ac.uk/id/eprint/10411), [pdf](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf)$]$

[[!redirects archimedean ordered field]]
[[!redirects archimedean ordered fields]]

[[!redirects Archimedean ordered field]]
[[!redirects Archimedean ordered fields]]