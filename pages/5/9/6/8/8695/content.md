
#Contents#
* table of contents
{:toc}

## Idea

In a context of [[infinitesimal cohesion]] the **reduced type** $Red(X)$ of a type $X$ is the result of removing all infinitesimal thickening in $X$.


## Definition

+-- {: .num_defn }
###### Definition

Given [[differential cohesion]]

$$
  (\mathbf{H} \coloneqq CohesiveType) 
    \stackrel{i}{\hookrightarrow}
  (\mathbf{H}_{th} \coloneqq InfThickenedCohesiveType)
$$

define the [[monad]]/[[comonad]] [[adjunction]]

$$
  (Red \dashv \Pi_{inf})
  \colon
  \mathbf{H}_{th}
  \stackrel{\overset{i_*}{\leftarrow}}{\underset{i^*}{\to}}
  \mathbf{H}
  \stackrel{\overset{i_!}{\leftarrow}}{\underset{i_*}{\to}}
  \mathbf{H}_{th}
  \,.
$$

We call $Red(X)$ the **reduced type** of $X$ and $\Pi_{inf}(X)$ the [[infinitesimal path ∞-groupoid]] of $X$.

The $(i_* \dashv i^*)$-[[unit of an adjunction|counit]] 

$$
  Red X \to X
$$

we call the **inclusion of the reduced part** of $X$.


For the $(i_* \dashv i^*)$-[[unit of an adjunction|unit]] we write

$$
  InfinitesimalPathInclusion_X \colon X \to \Pi_{inf}(X)
$$

and call it the **constant infinitesimal path inclusion** on $X$.

=--

## Examples

(...)

[[!redirects reduced spaces]]
[[!redirects reduced cohesive ∞-groupoid]]
[[!redirects reduced cohesive ∞-groupoids]]

[[!redirects reduced type]]
[[!redirects reduced types]]

