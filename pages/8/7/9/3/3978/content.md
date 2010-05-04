## Idea

A *closed natural transformation* is the appropriate sort of [[natural transformation]] relating [[closed functors]] between [[closed categories]].

## Definition

Let $F,G\colon C\to D$ be closed functors.  A **closed natural transformation** $\alpha\colon F\to G$ is simply an ordinary natural transformation such that:

* The following diagram commutes:
  $$\array{I_D & \overset{F^0}{\to} & F(I_C)\\
   & _{G^0}\searrow & \downarrow^{\alpha}\\
  &  & G(I_C)}$$

* The following diagram commutes for any $X,Y$:
  $$\array{F([X,Y]) & \overset{\hat{F}}{\to} & [F(X),F(Y)]\\
  && \downarrow^{[1,\alpha]}\\
  ^{\alpha }\downarrow && [F(X),G(Y)]\\
  && \uparrow^{[\alpha,1]}\\
  G([X,Y])& \underset{\hat{G}}{\to} & [G(X),G(Y)]}$$

## Examples

* Just as [[closed functors]] between [[closed monoidal categories]] are in bijective correspondence with (lax) [[monoidal functors]], closed natural transformations between such are in bijective corrrespondence with monoidal transformations.

* The same is true for transformations between closed unital [[multicategories]], regarded as closed categories.

## References

* Samuel Eilenberg and Max Kelly, _Closed categories._ Proc. Conf. Categorical Algebra (La Jolla, Calif., 1965).

[[!redirects closed natural transformations]]
