
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Dependent product types
* table of contents
{: toc}

## Idea

In [[dependent type theory]], a _dependent product type_ $\prod_{x\colon A} B(x)$, for a [[dependent type]] $x\colon A\vdash B(x)\colon Type$ is the [[type]] of "dependently typed [[functions]]" assigning to each $x\colon A$ an element of $B(x)$.

In a [[model]] of the type theory in [[categorical semantics]], this is a [[dependent product]].  In [[set theory]], it is an element of an indexed product.

It includes [[function types]] as the special case when $B$ is not dependent on $A$, and [[product types]] as a special case when $A$ is the type of [[Booleans]].

## Overview

[[!include dependent product natural deduction - table]]

## Definition

Like any type constructor in type theory, a dependent product type is specified by rules saying when we can introduce it as a type, how to construct terms of that type, how to use or "eliminate" terms of that type, and how to compute when we combine the constructors with the eliminators.

The [[type formation rule]] for dependent product type is:

$$\frac{A\colon Type \qquad x\colon A \vdash B(x) \colon Type}{\prod_{x\colon A} B(x)\colon Type}$$


### As a negative type

Dependent product types are almost always defined as [[negative types]].  In this presentation, primacy is given to the eliminators.  The natural eliminator of a dependent product type says that we can *apply* it to any input:

$$\frac{f\colon \prod_{x\colon A} B(x) \qquad a\colon A}{f(a) \colon B(a)}$$

The constructor is then determined as usual for a negative type: to construct a term of $\prod_{x\colon A} B(x)$, we have to specify how it behaves when applied to any input.  In other words, we should have a term of type $B(x)$ containing a free variable $x\colon A$.  This yields the usual "$\lambda$-abstraction" constructor:

$$\frac{x\colon A\vdash b\colon B(x)}{\lambda x.b\colon \prod_{x\colon A} B(x)}$$

The [[beta-reduction]] rule is the obvious one, saying that when we evaluate a $\lambda$-abstraction, we do it by substituting for the bound variable.

$$(\lambda x.b)(a) \;\to_\beta\; b[a/x]$$

If we want an [[eta-conversion]] rule, the natural one says that every dependently typed function is a $\lambda$-abstraction:

$$ \lambda x.f(x) \;\to_\eta\; f$$


### As a positive type

It is also possible to present dependent product types as a [[positive type]].  However, this requires a stronger metatheory, such as a [[logical framework]].  We use the same constructor ($\lambda$-abstraction), but now the eliminator says that to define an operation using a function, it suffices to say what to do in the case that that function is a lambda abstraction.

$$\frac{(x\colon A \vdash b\colon B(x)) \vdash c\colon C \qquad f\colon \prod_{x\colon A} B(x)}{funsplit(c,f)\colon C}$$

This rule cannot be formulated in the usual presentation of type theory, since it involves a "higher-order judgment": the context of the term $c\colon C$ involves a "term of type $B(x)$ containing a free variable $x\colon A$".  However, it is possible to make sense of it.  In [[dependent type theory]], we need additionally to allow $C$ to depend on $\prod_{x\colon A} B(x)$.

The natural $\beta$-reduction rule for this eliminator is

$$ funsplit(c, \lambda x.g) \;\to_\beta c[g/b] $$

and its $\eta$-conversion rule looks something like

$$ funsplit(c[\lambda x.b / g], f) \;\to_\eta\; c[f/g]. $$

Here $g\colon \prod_{x\colon A} B(x) \vdash c\colon C$ is a term containing a free variable of type $\prod_{x\colon A} B(x)$.  By substituting $\lambda x.b$ for $g$, we obtain a term of type $C$ which depends on "a term $b\colon B(x)$ containing a free variable $x\colon A$".  We then apply the positive eliminator at $f\colon \prod_{x\colon A} B(x)$, and the $\eta$-rule says that this can be computed by just substituting $f$ for $g$ in $c$.


### Positive versus negative

As usual, the positive and negative formulations are equivalent in a suitable sense.  They have the same constructor, while we can formulate the eliminators in terms of each other:

$$
\begin{aligned}
  f(a) &\coloneqq funsplit(b[a/x], f)\\
  funsplit(c, f) &\coloneqq c[f(x)/b]
\end{aligned}
$$

The conversion rules also correspond.

In dependent type theory, this definition of $funsplit$ only gives us a properly typed dependent eliminator if the negative dependent product type satisfies $\eta$-conversion.  As usual, if it satisfies [propositional eta-conversion](/nlab/show/eta-conversion#Propositional) then we can transport along that instead---and conversely, the dependent eliminator allows us to prove propositional $\eta$-conversion.  This is the content of Propositions 3.5, 3.6, and 3.7 in [(Garner)](#GarnerSDP).


## Related concepts

* [[dependent product]]
* [[dependent sum type]]
* [[function type]]


## References

The standard rules for type-formation, term introduction/elimination and computation of dependent product type are listed for instance in [part I](http://www.math.unipa.it/~ngambino/Research/Lectures/lecture1.pdf)  of

* [[Nicola Gambino]], _Lectures on dependent type theory_ ([pdf](http://www.cs.le.ac.uk/events/mgs2009/courses/gambino/lecturenotes-gambino.pdf))

See also

* [[Richard Garner]], *On the strength of dependent products in the type theory of Martin-L&#246;f*, [arXiv](http://arxiv.org/abs/0803.4466).
  {#GarnerSDP}


[[!redirects dependent product type]]
[[!redirects dependent product types]]
[[!redirects dependent function type]]
[[!redirects dependent function types]]
[[!redirects Pi-type]]
[[!redirects Pi-types]]
[[!redirects Pi type]]
[[!redirects Pi types]]
[[!redirects Π-type]]
[[!redirects Π-types]]
[[!redirects Π type]]
[[!redirects Π types]]
