
#Contents#
* table of contents
{:toc}

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


* {#EilenbergKelly65} [[Samuel Eilenberg]], [[G. Max Kelly]],  §I.4 of: *Closed Categories*, in: *[[Proceedings of the Conference on Categorical Algebra - La Jolla 1965]]*, Springer (1966) 421-562 &lbrack;[doi:10.1007/978-3-642-99902-4](https://doi.org/10.1007/978-3-642-99902-4)&rbrack;



[[!redirects closed natural transformations]]
