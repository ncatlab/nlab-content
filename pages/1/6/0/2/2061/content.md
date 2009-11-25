There are several contexts in which it is of relevance that a certain property of a [[morphism]] $f : A \to B$ is preserved (or __stable__) under [[pullback]], i.e. also shared by the the morphism $\tilde{f}: X \times_B A \to X$ for any pullback diagram

$$
  \array{
     X \times_B A &\to& A
     \\
     _{\tilde{f}}\downarrow && \downarrow_f
     \\
     X &\to& B
  }
  \,.
$$
Geometers prefer to say "stable under [[base change]]".

## Examples

*  [[monomorphism|Monomorphisms]] are always stable under pullback; that is, if $f$ is a monomorphism, then so is $\tilde{f}$.

*  In many important kinds of categories; some or all [[colimits]] are stable under pullback; this is discussed at [[commutativity of limits and colimits]].

*  The right [[lifting property]]:  Generally, the property of a morphism of having a [[weak factorization system|right lifting property]] is stable under pullback. Therefore for instance [[fibrations]] and acyclic fibrations in a [[model category]] are stable under pullback. If also [[weak equivalences]] are stable under pullback then one speaks of a left proper [[model category]].