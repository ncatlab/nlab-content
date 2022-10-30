
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

In [[type theory]] a _function type_ $X \to Y$ for two [[types]] $X,Y$ is the [[type]] of [[functions]] from $X$ to $Y$. 

In a [[model]] of the type theory in [[categorical semantics]], this is an [[exponential object]]. In [[set theory]], it is a [[function set]]. In [[dependent type theory]], it is a special case of a [[dependent product type]].

## Overview

[[!include function type natural deduction - table]]

## Definition

Like any type constructor in type theory, a function type is specified by rules saying when we can introduce it as a type, how to [[term introduction|construct terms]] of that type, how to use or "[[term elimination|eliminate]]" terms of that type, and how to compute when we combine the constructors with the eliminators.

The [[type formation]] rule to build a function type is easy:

$$\frac{A\colon Type \qquad B \colon Type}{A\to B\colon Type}$$

### As a negative type

Function types are almost always defined as a [[negative type]].  In this presentation, primacy is given to the eliminators.  The natural eliminator of a function type says that we can [[function application|apply]] it to any input:

$$\frac{f\colon A\to B \qquad a\colon A}{f(a) \colon B}$$

The constructor is then determined as usual for a negative type: to construct a term of $A\to B$, we have to specify how it behaves when applied to any input.  In other words, we should have a term of type $B$ containing a free variable of type $A$.  This yields the usual "$\lambda$-abstraction" constructor:

$$\frac{x\colon A\vdash b\colon B}{\lambda x.b\colon A\to B}$$

The [[∞-reduction]] rule is the obvious one (the ur-example of all $\beta$-reductions), saying that when we evaluate a $\lambda$-abstraction, we do it by substituting for the bound variable.

$$(\lambda x.b)(a) \;\to_\beta\; b[a/x]$$

If we want an [[∞-conversion]] rule, the natural one says that every function is a $\lambda$-abstraction:

$$ \lambda x.f(x) \;\to_\eta\; f$$

### As a positive type

It is also possible to present function types as a [[positive type]].  However, this requires a stronger metatheory, such as a [[logical framework]].  We use the same constructor ($\lambda$-abstraction), but now the eliminator says that to define an operation using a function, it suffices to say what to do in the case that that function is a lambda abstraction.

$$\frac{(x\colon A \vdash b\colon B) \vdash c\colon C \qquad f\colon A\to B}{funsplit(c,f)\colon C}$$

This rule cannot be formulated in the usual presentation of type theory, since it involves a "higher-order judgment": the context of the term $c\colon C$ involves a "term of type $B$ containing a free variable of type $A$".  However, it is possible to make sense of it.  In [[dependent type theory]], we need additionally to allow $C$ to depend on $A\to B$.

The natural $\beta$-reduction rule for this eliminator is

$$ funsplit(c, \lambda x.g) \;\to_\beta c[g/b] $$

and its $\eta$-conversion rule looks something like

$$ funsplit(c[\lambda x.b / g], f) \;\to_\eta\; c[f/g]. $$

Here $g\colon A\to B \vdash c\colon C$ is a term containing a free variable of type $A\to B$.  By substituting $\lambda x.b$ for $g$, we obtain a term of type $C$ which depends on "a term $b\colon B$ containing a free variable $x\colon A$".  We then apply the positive eliminator at $f\colon A\to B$, and the $\eta$-rule says that this can be computed by just substituting $f$ for $g$ in $c$.

### Positive versus negative

As usual, the positive and negative formulations are equivalent in a suitable sense.  They have the same constructor, while we can formulate the eliminators in terms of each other:

$$
\begin{aligned}
  f(a) &\coloneqq funsplit(b[a/x], f)\\
  funsplit(c, f) &\coloneqq c[f(x)/b]
\end{aligned}
$$

The conversion rules also correspond.

In dependent type theory, this definition of $funsplit$ only gives us a properly typed dependent eliminator if the negative function type satisfies $\eta$-conversion.  As usual, if it satisfies [propositional eta-conversion](/nlab/show/eta-conversion#Propositional) then we can transport along that instead---and conversely, the dependent eliminator allows us to prove propositional $\eta$-conversion.  This is the content of Propositions 3.5, 3.6, and 3.7 in [(Garner)](#GarnerSDP).

### As a special case of the dependent product

In [[dependent type theory]] a function type $A \to B$ is the
special case the [[dependent product]] over $a : A$ for the 
special case that $B$ is regarded as an $A$-[[dependent type]] that
actually happens to be $A$-independent

$$
  A \to B =_{def} \prod_{a : A} B
  \,.
$$

In [[categorical semantics]] this is the statement that a [[section]] of a product [[projection]] $A \times B \to A$ is equivalently just a morphism $A \to B$.

## Properties

### Relation to dependent product types

A function type is the special case of a [[dependent product type]] for the case where the [[dependent type]] does not actually depend.

$$
  (X \to A)
  = 
  \prod_{x \colon X} A
  \,.
$$

### Application in logic

In [[logic]], functions types express [[implication]]. More precisely, for $\phi, \psi$ two [[propositions]], under [[propositions as types]] the [[implication]] $\phi \Rightarrow \psi$ is the function type $\phi \to \psi$ (or rather the [[bracket type]] of that if one wishes to force this to be of type $Prop$ again ).

## Related concepts

* [[function application]]
* [[dependent product type]]
* [[lambda calculus]]
* [[implication]]

## References

A textbook account in the context of [[programming languages]] is in section III of

* [[Robert Harper]], _[[Practical Foundations for Programming Languages]]_

See also

* [[Richard Garner]], *On the strength of dependent products in the type theory of Martin-L&#246;f*.
 {#GarnerSDP}

[[!redirects function type]]
[[!redirects function types]]
