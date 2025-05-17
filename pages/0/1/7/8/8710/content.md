
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

**Differential cohesive homotopy type theory** or **elastic homotopy type theory** is the (hypothetical) [[modal type theory]] obtained by adding to [[cohesive homotopy type theory]] an [[adjoint triple]] of [[idempotent monad|idempotent (co)monadic]] [[modalities]]:

$$
  \Re \dashv \Im \dashv \&
$$

called

* [[reduction modality]] $\dashv$ [[infinitesimal shape modality]] $\dashv$ [[infinitesimal flat modality]].

{#AlsoCalledElastic} (Also called *elastic* homotopy theory $[$[[schreiber:Proper Orbifold Cohomology|SS20, §3.1.2]]$]$, see at *[[geometry of physics -- categories and toposes]]* the sections on *[elastic toposes](geometry+of+physics+--+categories+and+toposes#ElasticToposes)* and *[elastic $\infty$-toposes](geometry+of+physics+--+categories+and+toposes#ElasticInfinityToposes)*.)

By the discussion at _[[cohesive (infinity,1)-topos -- infinitesimal cohesion]]_ this language can express at least the following notions

* [[reduced type]], [[infinitesimal path ∞-groupoid]], [[de Rham space]], [[jet bundle]], [[D-geometry]], [[∞-Lie algebra]] (synthetically), [[Lie differentiation]], hence "Formal [[Moduli Problems and DG-Lie Algebras]]" , [[formally etale morphism]], [[formally smooth morphism]], [[formally unramified morphism]], [[smooth etale ∞-groupoid]], hence [[∞-orbifold]] etc. 

No full formalization of such a type theory currently exists, and how to design such a theory is an open question in [[modal type theory]].

## Partial Realizations

Some work has been done on [[synthetic differential geometry]] in modal homotopy type theory.

[[Felix Cherubini]] ([Cherubini18](#Cherubini)) has formalized some synthetic differential geometry using an abstract [[infinitesimal shape modality]] working in plain homotopy type theory.

[[David Jaz Myers]] ([JazMyers22](#JazMyers)) formalized a synthetic theory of [[orbifolds]] working in a type theory extending [[cohesive homotopy type theory]] with axioms such as the [[Kock-Lawvere axiom]] to axiomatize the notion of infinitesimals and defines the [[infinitesimal shape modality]] and [[shape modality]] as [[localizations]] at the infinitesimals and reals respectively.


## Related concepts

* [[cohesive homotopy type theory]]

* [[super homotopy type theory]]

* [[differential cohesive (infinity,1)-topos]]

* [[differential geometry]]

## References

* {#Cherubini} [[Felix Cherubini]], Cartan Geometry in Modal Homotopy Type Theory, ([arXiv:1806.05966](https://arxiv.org/abs/1806.05966))

* {#JazMyers} [[David Jaz Myers]], Orbifolds as microlinear types in synthetic differential cohesive homotopy type theory ([arXiv:2205.15887](https://arxiv.org/abs/2205.15887))

[[!redirects elastic type theory]]
[[!redirects elastic type theories]]

[[!redirects elastic dependent type theory]]
[[!redirects elastic dependent type theories]]

[[!redirects elastic homotopy type theory]]
[[!redirects elastic homotopy type theories]]

[[!redirects differential cohesive type theory]]
[[!redirects differential cohesive type theories]]

[[!redirects differential cohesive dependent type theory]]
[[!redirects differential cohesive dependent type theories]]

[[!redirects differential cohesive homotopy type theory]]
[[!redirects differential cohesive homotopy type theories]]

[[!redirects differential homotopy type theory]]
[[!redirects differential homotopy type theories]]
