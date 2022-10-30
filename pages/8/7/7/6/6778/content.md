
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Factorization systems
+--{: .hide}
[[!include factorization systems - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

In the [[2-topos]] [[Cat]], the pair of classes of morphisms ([[essentially surjective functor|essentially surjective]] and [[full functor|full]] functors, [[faithful functors]]) form a [[factorization system in a 2-category]].  This factorization system can also be restricted to the [[(2,1)-topos]] [[Grpd]].

In fact, an analogous factorization system exists in any [[2-exact 2-category]] and any [[(2,1)-exact (2,1)-category]], including any [[Grothendieck 2-topos]] or [[(2,1)-topos]]; see [[michaelshulman:full morphism|here]].

## Properties

* When restricted to [[Grpd]], this is the special case of the [[n-connected/n-truncated factorization system]] in the [[(∞,1)-topos]] [[∞Grpd]] for the case that $(n = 0)$ and restricted to [[1-truncated]] [[objects]].

* For $f : X \to Y$ a functor between groupoids, its factorization is through a groupoid $im_2 f$ which is, up to equivalence, given as follows;
  
  * [[objects]] are those of $X$;

  * a morphism $[\phi] : x_1 \to x_2$ is an equivalence class of morphisms in $X$ where $[\phi] = [\phi']$ if $f(\phi) = f(\phi')$.

## Related concepts

* [[epi-mono factorization system]]

* [[(eso, fully faithful) factorization system]]
* **(eso+full, faithful)-factorization system**

* [[n-connected/n-truncated factorization system]].

[[!redirects essentially surjective and full/faithful factorization system]]
