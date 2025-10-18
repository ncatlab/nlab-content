
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Spheres
+--{: .hide}
[[!include spheres -- contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _rational homotopy sphere_ is a [[topological space]] which need not be [[homeomorphism|homeomorphic]] to an [[n-sphere]], but which has the same [[rational homotopy type]] as an $n$-sphere, hence whose [[rationalization]] is [[weak homotopy equivalence|weakly homotopy equivalent]] to a [[rational n-sphere]].

## Definition

A $n$-dimensional manifold $\Sigma$ with:
$$
\pi_k(\Sigma)\otimes\mathbb{Q}
=\pi_k(S^n)\otimes\mathbb{Q}
\cong\begin{cases}
\mathbb{Z} & ;k=n\text{ if }n\text{ even} \\
\mathbb{Z} & ;k=n,2n-1\text{ if }n\text{ odd} \\
1 & ;\text{otherwise}
\end{cases}
$$
is a _rational homotopy $n$-sphere_.

## Properties

\begin{corollary}
Every [[homotopy sphere]] is a rational homotopy sphere.
\end{corollary}

## Examples

\begin{example}
The $n$-[[sphere]] $S^n$ is in particular a rational homology $n$-sphere.
\end{example}
\begin{example}
[[real projective space|Real projective space]] $\mathbb{R}P^n$ is a rational homotopy $n$-sphere for all $n\gt 0$. The [[fiber bundle]] $S^0\hookrightarrow S^n\twoheadrightarrow\mathbb{R}P^n$ ([Hatcher 02, Ex. 4.44.](#Hatcher02)) yields with the [[long exact sequence]] of homotopy groups ([Hatcher 02, Thrm. 4.41.](#Hatcher02)) that $\pi_k(\mathbb{R}P^n)\cong\pi_k(S^n)$ for $k\gt 1$ and $n\gt 0$ as well as $\pi_1(\mathbb{R}P^1)=\mathbb{Z}$ and $\pi_1(\mathbb{R}P^n)=\mathbb{Z}_2$ for $n\gt 1$, which vanishes after rationalization. $\mathbb{R}P^1\cong S^1$ is the sphere in particular.
\end{example}

## Related concepts

* [[homotopy sphere]]
* [[homology sphere]]
* [[rational homology sphere]]

## References

* {#Hatcher02} [[Allen Hatcher]]: *Algebraic Topology*, Cambridge University Press (2002) &lbrack;[ISBN:9780521795401](https://www.cambridge.org/gb/academic/subjects/mathematics/geometry-and-topology/algebraic-topology-1?format=PB&isbn=9780521795401), [webpage](https://pi.math.cornell.edu/~hatcher/AT/ATpage.html)&rbrack;

See also:

* Wikipedia, _[Rational homotopy sphere](https://en.wikipedia.org/wiki/Rational_homotopy_sphere)_

[[!redirects rational homotopy spheres]]




