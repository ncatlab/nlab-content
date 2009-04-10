A [[functor]] $F: C \to D$ between [[additive category|additive categories]] is itself __additive__ if it preserves finite [[biproduct]]s.

That is, $F$ maps a [[zero object]] to a zero object; and, given objects $x$ and $y$ of $C$, not only is $F(x \oplus y) \cong F(x) \oplus F(y)$, but $F$ even preserves the inclusion and projection maps:
$$
\array { x &          &            &          & y \\
           & \searrow &            & \swarrow \\
           &          & x \oplus y \\
           & \swarrow &            & \searrow \\
         x &          &            &          & y }
\quad\quad\stackrel{F}{\mapsto}\quad\quad
\array { F(x) &          &                                      &          & y \\
              & \searrow &                                      & \swarrow \\
              &          & F(x \oplus y) \cong F(x) \oplus F(y) \\
              & \swarrow &                                      & \searrow \\
         F(x) &          &                                      &          & y }
$$

Additive categories are always [[enriched category|enriched]] over [[Ab]], and an additive functor is always an [[enriched functor]] accordingly.  This need not be stated as a requirement; it follows from preserving biproducts, since the $Ab$-enrichment structure may be recovered from the biproducts (as described at [[biproduct]]).  Conversely, any $Ab$-enriched functor automatically preserves any finite biproducts that may exist, since finite biproducts in [[Ab-enriched category|Ab-enriched categories]] are [[Cauchy complete category|Cauchy colimits]].

In practice, functors between additive categories are generally assumed to be additive.
