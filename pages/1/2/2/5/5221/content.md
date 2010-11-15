
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An _integral transform_ on [[function]]s is a [[linear map]] between functions on [[space]]s $X$, $Y$ encoded by a function $K$ on the [[product]] space $X \times Y$ and given by a formula of the type

$$
  (function f on X) \mapsto
  \left(y \mapsto
  \int_{X} f(x) K(x,y) \right)
  \,,
$$

where on the right we have some kind of [[integration]] over $X$.

Here $K$ is called the integral **kernel** of the transformation.


Typically the definition of an integral transform on functions involves some delicate technical issues concerning the precise nature of the function space, the [[measure]] with respect to which the integral is defined, etc.

On the other hand, one may understand the general form of an integral transform as the [[decategorification]] of a very natural general abstract construction in [[higher category theory]]: that of [[integral transforms on sheaves]] given by spans of [[base change geometric morphism]]s.

Special cases of such [[categorification|categorified]] integral transforms are discussed at

* [[Fourier-Mukai transform]], [[topological T-duality]]

* [[groupoidification]]

* [[geometric infinity-function theory]].

## Examples

The simplest example is [[matrix multiplication]], which corresponds to the case where $X$ and $Y$ are [[discrete space]]s.

Standard examples involving genuine [[functional analysis]] are for instance the [[Fourier transform]] or the [[Laplace transform]].

Also the [[path integral]] in [[quantum mechanics]] and [[quantum field theory]] is supposed to be a class of examples of an integral kernel.


[[!redirects integral transforms]]