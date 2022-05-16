
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Categorification
+-- {: .hide}
[[!include categorification - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

In [[category theory]], the notion of a *magmoidal groupoid* is the [[groupoidal categorification]] of the notion of *[[magma]]*, hence a magmoidal groupoid is simply a [[groupoid]] equipped with a "[[binary operation]]" on it.
Similarly, under the [[relation between category theory and type theory]],
in [[homotopy type theory]] a *magmoidal groupoid* is a [[1-truncated type]] equipped with a binary operation.  

## Definitions

### In type theory

In [[intensional type theory]] with [[function extensionality]], a [[groupoid]] is a [[n-truncated|1-truncated]] [[type]] and a __binary operation__ on a [[groupoid]] $G$ is a [[function]] $(-)\otimes (-) \colon G \times G \to G$ from the [[product type|product groupoid]] $G \times G$ to $G$. A __magmoidal groupoid__ $(G,\otimes)$ is a [[groupoid]] equipped with a binary operation on it. 

### In category theory

In [[category theory]], a [[groupoid]] is a [[dagger category]] where every [[morphism]] is [[unitary morphism|unitary]], and a __binary operation__ on a [[groupoid]] $G$ is a [[dagger functor]] $(-)\otimes (-) \colon G \times G \to G$ from the [[product groupoid]] $G \times G$ to $G$. A __magmoidal groupoid__ $(G,\otimes)$ is a [[groupoid]] equipped with a binary operation on it. 

## See also

* [[magma]]
* [[magmoidal category]]
* [[H-spatial groupoid]]

[[!redirects magmoidal groupoids]]
