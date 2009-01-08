If $E$ and $F$ are [[topos|toposes]], a **geometric morphism** $f:E\to F$ consists of an adjoint pair $(f^*,f_*)$, such that the left adjoint $f^*:F \to E$ also preserves finite limits.

One way to motivate this definition is that if $X$ and $Y$ are [[sober space|sober]] [[topological space]]s (or, more generally, [[locale|locales]]), then every continuous function $f:X \to Y$ induces a unique (up to isomorphism) geometric morphism $f: Sh(X) \to Sh(Y)$ between toposes of [[sheaf|sheaves]], and up to isomorphism every geometric morphism $Sh(X) \to Sh(Y)$ is of this form.

Another motivation has to do with the fact that a functor such as $f^*$ that preserves finite limits and arbitrary colimits (since it is a left adjoint) necessarily preserves all constructions in [[geometric logic]].  See also [[classifying topos]].

Since [[Grothendieck topos]]es satisfy the (dual) hypotheses of Freyd's special [[adjoint functor theorem]], any functor $f^*$ between Grothendieck toposes which preserves all small colimits must have a right adjoint.  Therefore, a geometric morphism between Grothendieck toposes could equivalently be defined as a functor preserving finite limits and all small colimits.
