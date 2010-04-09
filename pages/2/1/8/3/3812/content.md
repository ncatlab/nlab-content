
#Contents#
* automatic table of contents goes here
{:toc}

## Triangulation

A **triangulation** of a [[topological space]] $Y$ is a [[simplicial set]] $X$ together with a [[homeomorphism]] $h: R X \to Y$, where $R$ denotes the [[geometric realization]] [[functor]]. 

(Often $Y$ here is taken to be a [[simplicial complex]], but the difference does not really matter here.)

Explicitly, $R X$ is given by a [[coend]] formula 

$$\int^{n \in \Delta} X(n) \cdot \sigma(n)$$ 

where $\sigma: \Delta \to Top$ is the standard affine [[simplex]] functor.

## Cubulation

Similarly, a **cubulation** of a [[topological space]] $Y$ is a [[cubical set]] $C$ together with a [[homeomorphism]] $h: R_{cub}C \to Y$ where $R_{cub}$ denotes the realization functor for [[cubical set]]s $Set^{\Box^{op}}$. Explicitly, $R_{cub}C$ is given by a [[coend]] formula 

$$R_{cub}C = \int^{m \in Cube} C(m) \cdot \Box(m)$$ 

where $\Box: Cube \to Top$ is the standard geometric cube functor.

## Discussion

There should be "cubulation" functor for standard simplices, $\Sigma: \Delta \to Set^{\Box^{op}}$, such that the affine simplex functor $\sigma: \Delta \to Top$ is naturally isomorphic to the composite 

$$\Delta \stackrel{\Sigma}{\to} Set^{\Box^{op}} \stackrel{R_{cub}}{\to} Top$$ 

Assuming this works out, then given a triangulation $(X, h: R X \to Y)$ of a space $Y$, we have [[isomorphism]]s 

$$\array{
Y & \cong & \int^n X(n) \cdot \sigma(n) \\
 & \cong & \int^n X(n) \cdot (\int^m \Sigma_n(m) \cdot \Box(m)) \\
 & \cong & \int^m (\int^n X(n) \cdot \Sigma_n(m)) \cdot \Box(m) 
}$$ 

where in the last line we used the [[coend Fubini theorem]] for interchange of coends. Thus, defining the cubical set $C$ by 

$$C(m) = \int^n X(n) \cdot \Sigma_n(m)$$ 

we have a homeomorphism $Y \cong \int^m C(m) \cdot \Box(m) = R_{cub} C$, i.e., we obtain a cubulation of $Y$. 

[[!redirects cubulation]]
[[!redirects triangulations]]