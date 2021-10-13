[[!redirects pullback stability]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea


There are several contexts in which it is of relevance that a certain property of a [[morphism]] $f : A \to B$ is preserved (or __stable__) under [[pullback]], i.e. also shared by the the morphism $\tilde{f}: X \times_B A \to X$ for any pullback diagram

$$
  \array{
     X \times_B A 
       &\longrightarrow& 
     A
     \\
     {}^{\mathllap{\tilde{f}}}
     \big\downarrow 
       && 
     \big\downarrow
     {}^{\mathrlap{f}}
     \\
     X 
       &\longrightarrow& 
     B
  }
  \,.
$$

Geometers prefer to say "stable under [[base change]]".

## Examples

*  [[monomorphism|Monomorphisms]] are always stable under pullback; that is, if $f$ is a monomorphism, then so is $\tilde{f}$.

*  In many important kinds of categories; some or all [[colimits]] are stable under pullback; this is discussed at [[commutativity of limits and colimits]].

*  The right [[lifting property]]:  Generally, the property of a morphism of having a [[weak factorization system|right lifting property]] is stable under pullback. Therefore for instance [[fibrations]] and acyclic fibrations in a [[model category]] are stable under pullback. If also [[weak equivalences]] are stable under pullback along fibrations, then one speaks of a right proper [[model category]].

*  Similarly, the property of being right [[orthogonality|orthogonal]] to a class of morphisms is stable under pullback.  Thus, the right class in any [[orthogonal factorization system]] is stable under pullback.  If the left class is also pullback-stable, the OFS is called [[stable factorization system|stable]].

## Related concepts

* [[pullback-stable colimit]]

* [[stable factorization system]]

* [[extensive category]]

[[!redirects pullback-stability]]
