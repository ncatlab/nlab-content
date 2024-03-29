

#Contents#
* table of contents
{:toc}

## Idea

In a context of [[infinitesimal cohesion]] the **infinitesimal path $\infty$-groupoid** $\Pi_{inf}X \coloneqq \Im(X)$ of a type $X$ is the result of identifying infinitesimally close points in $X$ by adding in further equivalences between all objects (points of $X$) that are infinitesimal neighbours. 


## Definition

+-- {: .num_defn }
###### Definition

Given [[differential cohesion]]

$$
  (\mathbf{H} \coloneqq CohesiveType) 
    \stackrel{i}{\hookrightarrow}
  (\mathbf{H}_{th} \coloneqq InfThickenedCohesiveType)
$$

define the [[reduction modality]]/[[infinitesimal shape modality]] [[adjunction]]

$$
  (\Re \dashv \Im)
  \colon
  \mathbf{H}_{th}
  \stackrel{\overset{i_!}{\leftarrow}}{\underset{i^\ast}{\to}}
  \mathbf{H}
  \stackrel{\overset{i^\ast}{\leftarrow}}{\underset{i_\ast}{\to}}
  \mathbf{H}_{th}
  \,.
$$

We call $\Pi_{inf}(X) \coloneqq \Im(X)$ the **infinitesimal path ∞-groupoid** of $X$ and  $\Re(X)$ the **[[reduced type]]** of $X$. 


For the $(i_* \dashv i^*)$-[[unit of an adjunction|unit]] we write

$$
  InfinitesimalPathInclusion_X \colon X \to \Pi_{inf}(X)
$$

and call it the **constant infinitesimal path inclusion** on $X$.

The $(i_* \dashv i^*)$-[[unit of an adjunction|counit]] 

$$
  \Re (X) \to X
$$

we call the **inclusion of the reduced part** of $X$.

=--

## Examples

* [[de Rham space]]

[[!redirects infinitesimal path infinity-groupoid]]
[[!redirects infinitesimal path ∞-groupoids]]
[[!redirects infinitesimal path infinity-groupoids]]

