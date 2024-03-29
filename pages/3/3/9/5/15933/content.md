# Contents 
* table of contents 
{:toc} 

## Idea 

A Dehn twist is a type of self-[[homeomorphism]] on a surface (a 2-dimensional [[topological manifold]]), especially an [[orientation|orientable]] [[closed manifold]] (of dimension 2). 

## Definition 

Let $\Sigma$ be an orientable surface of [[genus]] $g$, and consider an embedded circle $i: S^1 \hookrightarrow \Sigma$. (For example, one may imagine a circle representing one of $2 g$ generators of $H^1(\Sigma, \mathbb{Z})$.) The embedded circle has a [[tubular neighborhood]] in $\Sigma$, homeomorphic to an annulus $S^1 \times [0, 1]$. Representing elements of $S^1$ by [[complex numbers]] $z$ of [[norm]] 1, a *twist* on the annulus may be defined by sending $(z, t) \mapsto (\exp(2\pi i t) z, t)$, which equals the identity on the boundary circles where $t = 0, t = 1$. This defines a self-homeomorphism (mod boundary) on the annulus. 

The corresponding Dehn twist on $\Sigma$ is obtained by extending the self-homeomorphism on the annulus to the entire surface, by taking a point $p$ to itself if $p$ is outside the annulus. (If we are working in the category of smooth manifolds, one may modify the twist on the annulus by taking $(z, t) \mapsto (\exp(2\pi i f(t))z, t)$ where $f$ is a smooth [[bump function]] such that $f(t) = 0$ on a small neighborhood of $t = 0$ and $f(t) = 1$ on a small neighborhood of $t=1$. This modification ensures that we get a self-[[diffeomorphism]] on the surface $\Sigma$ as smooth manifold.) 

## Properties 

The following theorem was first proved by MaxDehn, with later simplifications by Lickorish: 

+-- {: .num_theorem} 
###### Theorem 
**("Lickorish twist")** 
The Dehn twists generate the [[mapping class group]] of $\Sigma$, of orientation-preserving homeomorphisms considered modulo [[isotopy]]. (In fact Lickorish described $3g-1$ explicit embedded circles for a surface $\Sigma$ of genus $g$ whose corresponding twists give the generators.) 
=-- 

One example that is easily visualized is the mapping class group $MCG(\Sigma)$ of the [[torus]] $\Sigma = S^1 \times S^1$. Here the canonical map $MCG(\Sigma) \to Aut(\pi_1(\Sigma)) \cong Aut(\mathbb{Z} \times \mathbb{Z})$ is an isomorphism (where automorphisms of $\mathbb{Z}$ are required to preserve orientation, i.e., are elements of the group $SL_2(\mathbb{Z})$; cf. [[modular group]]). Thus in this case the Dehn twists can be visualized in terms of their action on loops representing elements of $\pi_1(\Sigma)$; the [Wikipedia article](#WP) has some decent pictures of this action. 


## Related concepts

* [[mapping class group]] 

* [[Dehn surgery]] 

## References

* Wikipedia, _[Dehn twist](http://en.wikipedia.org/wiki/Dehn_twist)_ 
 {#WP} 

[[!redirects Dehn twists]]