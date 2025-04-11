
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]
=--
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
#### Directed Type Theory
+-- {: .hide}
[[!include directed homotopy type theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

Triangulated type theory is a variation of [[simplicial type theory]] where the directed interval type $\mathbb{I}$ is only required to be a [[distributive lattice]] instead of a [[bounded total order]]. As a result, not all types are [[simplicial types]], and instead there is an idempotent lex monad which takes a type $A$ to a simplicial type $\Box A$. 

Triangulated type theory has semantics in the [[cohesive (infinity,1)-topos|cohesive]] [[locally cartesian closed (infinity,1)-category|locally cartesian closed]] [[(infinity,1)-category|$(\infty,1)$-category]] $\mathbf{H}^{\Box^\op}$ of [[cubical object in an (infinity,1)-category|cubical objects]] in a locally cartesian closed $(\infty,1)$-category $\mathbf{H}$, where $\Box$ is the [[cube category]] of [[finite set|finite]] [[flat distributive lattices]]. 

## Related concepts

* [[simplicial type theory]]

* [[simplicial type]]

## References

* {#GWB24} [[Daniel Gratzer]], [[Jonathan Weinberger]], [[Ulrik Buchholtz]], *Directed univalence in simplicial homotopy type theory* ([arXiv:2407.09146](https://arxiv.org/abs/2407.09146))

[[!redirects triangulated type theory]]
[[!redirects triangulated homotopy type theory]]