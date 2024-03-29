
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesion
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
#### Discrete and concrete objects
+-- {: .hide}
[[!include discrete and concrete objects - contents]]
=--
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In a context of [[synthetic differential geometry]]/[[differential cohesion]] a _coreduced object_ is one all whose [[infinitesimal space|infinitesimal]] paths are constant.
Compare the [[discrete object|discrete objects]], in which all paths are constant, meaning all discrete objects are also coreduced.

## Definition

A context of [[differential cohesion]] is determined by the existence of an [[adjoint triple]] of  [[modalities]]

$$
  \Re \dashv \Im \dashv \&
  \,,
$$

where $\Re$ and $\&$ are [[idempotent monad|idempotent]] [[comonads]] and $\Im$ is an [[idempotent monad]].

A **coreduced object** or **coreduced type** is one in the [[full subcategory]] defined by the [[infinitesimal shape modality]] $\Im$ or equivalently the [[infinitesimal flat modality]] $\&$.

Note that an object $X$ being coreduced is the same as it being [[formally etale]].

## Examples

* A coreduced [[scheme]] is also called a [[de Rham space]]. The [[cohomology]] over such is [[crystalline cohomology]], the [[quasicoherent sheaves]] over these define [[D-geometry]].
* In a [[differential geometry|differential geometric]] setting, [[formally etale morphism|formally etale maps]] are the [[local diffeomorphism|local diffeomorphisms]], and the coreduced objects are those for which the terminal map $X \to 1$ is a local diffeomorphism.

## Related concepts

[[!include cohesion - table]]

* [[formally smooth morphism]], [[formally etale morphism]], [[formally unramified morphism]]



[[!redirects coreduced objects]]

[[!redirects coreduced type]]
[[!redirects coreduced types]]

[[!redirects coreduced space]]
[[!redirects coreduced spaces]]
