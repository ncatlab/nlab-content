# Colax-distributive rig categories

* table of contents
{: toc}

## Idea

A *colax-distributive rig category* is like a [[rig category]], but where the distributive laws hold only laxly.

## Definition

A **right colax-distributive rig category** is a category $C$ equipped with two monoidal structures $(C,\otimes,I)$ and $(C,\oplus,J)$ and natural transformations
$$ (X\oplus Y) \otimes Z \to (X\otimes Z) \oplus (Y\otimes Z) $$
and
$$ J \otimes Z \to J $$
making the functor $(-\otimes Z)$ [[colax monoidal functor|colax monoidal]] with respect to $\oplus$, and perhaps some other coherence equations.  A **left colax-distributive** rig category has instead transformations
$$ Z \otimes  (X\oplus Y) \to (Z\otimes X) \oplus (Z\otimes Y) $$
and
$$ Z \otimes J \to J$$
making $(Z\otimes -)$ colax monoidal, and a simply **colax-distributive** rig category has both.

## Examples

* Of course, a [[rig category]] is a colax-distributive rig category where the distributivity transformations are isomorphisms.

* If $(C,\otimes,I)$ is *any* monoidal category with finite products, then it becomes a colax-distributive rig category with $(C,\oplus,J)$ the cartesian monoidal structure and the distributivity transformations being induced by the universal property of products.

* If $(D,\diamond,\star)$ is a [[duoidal category]] in which $\star$ is compatibly braided (or perhaps symmetric), then the category $CComon_\star(D)$ of cocommutative comonoids in $D$ inherits a monoidal structure from $\diamond$ and has finite products; hence it is a colax-distributive rig category.

## Structures in colax-distributive rig categories

### Rings and near-rings

In a right colax-distributive rig category $(C,\otimes,I,\oplus,J)$, a **[[near-rig]]** is an object $R$ equipped with an $\oplus$-monoid structure $add:R\oplus R \to R$ called "addition", and an $\otimes$-monoid structure $mult : R\otimes R \to R$ called "multiplication", such that the right distributive law:
$$ \array{
    (R\oplus R) \otimes R & \xrightarrow{add\otimes id} &
    R\otimes R & \xrightarrow{mult} &
    R\\
    \downarrow & & & &
    \uparrow^{add}\\
    (R\otimes R) \oplus (R\otimes R) && \xrightarrow{mult \oplus mult} &&
    R\oplus R
  }
  $$
and the right absorption law:
  $$ \array{ 
    J\otimes R & \to &
    J & \xrightarrow{0} &
    R\\
    & _{0\otimes id}\searrow && \nearrow_\mult \\
    && R\otimes R
  }
  $$
hold.

If also the left distributive and absorption laws hold (which requires $C$ to also be left colax-distributive), then $R$ is a **rig**.  And if $\oplus$ is cartesian and the additive monoidal structure is a group structure, then $R$ is a **(near-)ring**.

In the right colax-distributive category $CComon_\star(D)$ of cocommutative comonoids in a [[duoidal category]] $D$, these agree with the definitions of (cocommutative) (near)-ri(n)gs in $D$ (see [[duoidal category]] for these).

On the other hand, if $C$ is a [[preadditive category|preadditive]] [[distributive monoidal category]] and $\oplus$ is the cartesian monoidal structure (which is also the *cocartesian* structure, so that $C$ is in fact a [[rig category]]), then every object is an $\oplus$-monoid in a unique way, and the distributive and absorption laws are also automatic.  Thus, in this case near-rigs and rigs coincide simply with $\otimes$-monoids.  If $C$ is [[additive category|additive]], then near-rings and rings also coincide with $\otimes$-monoids.


## Related pages

* [[distributivity for monoidal structures]]


[[!redirects colax-distributive rig category]]
[[!redirects colax-distributive rig categories]]
[[!redirects right colax-distributive rig category]]
[[!redirects right colax-distributive rig categories]]
[[!redirects left colax-distributive rig category]]
[[!redirects left colax-distributive rig categories]]

[[!redirects colax-distributive category]]
[[!redirects colax-distributive categories]]
[[!redirects right colax-distributive category]]
[[!redirects right colax-distributive categories]]
[[!redirects left colax-distributive category]]
[[!redirects left colax-distributive categories]]
