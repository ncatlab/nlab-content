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

A _rational homology sphere_ is a [[topological space]] which need not be [[homeomorphism|homeomorphic]] to an [[n-sphere]], but which has the same [[rational homotopy theory|rational homology]] as an $n$-sphere.

## Definition

A $n$-dimensional manifold $\Sigma$ with:
$$
H_k(\Sigma,\mathbb{Q})
=H_k(S^n,\mathbb{Q})
\cong\begin{cases}
\mathbb{Q} & ;k=0\text{ or }k=n \\
1 & ;\text{otherwise}
\end{cases}
$$
is a _rational homology $n$-sphere_.

## Properties

\begin{corollary}
Every [[homology sphere]] is a rational homology sphere.
\end{corollary}

## Examples

\begin{example}
The $n$-[[sphere]] $S^n$ is in particular a rational homology $n$-sphere.
\end{example}
\begin{example}
The [[Klein bottle]] $K$ has two dimensions, but has the same rational homology as the $1$-sphere. Its integral [[homology groups]] are given by: ([Hatcher 02, Ex. 2.47.](#Hatcher02))
$$
H_0(K)
\cong\mathbb{Z};
$$
$$
H_1(K)
\cong\mathbb{Z}\oplus\mathbb{Z}_2;
$$
$$
H_2(K)
\cong 1.
$$
Hence it is _not_ a rational homology sphere, but would be if the requirement to be of same dimension was dropped.
\end{example}
\begin{example}
[[real projective space|Real projective space]] $\mathbb{R}P^n$ is a rational homology $n$-sphere for all $n$ odd. Its integral [[homology groups]] are given by: ([Hatcher 02, Ex. 4.42.](#Hatcher02))
$$
H_k(\mathbb{R}P^n)
\cong\begin{cases}
\mathbb{Z} & ;k=0\text{ or }k=n\text{ if odd} \\
\mathbb{Z}_2 & ;k\text{ odd},0\lt k\lt n \\
1 & ;\text{otherwise}
\end{cases}
$$
$\mathbb{R}P^1\cong S^1$ is the sphere in particular.
\end{example}
\begin{example}
The [[Wu manifold]] $W=SU(3)/SO(3)$ is a [[simply connected]] rational homology $5$-sphere (with non-trivial [[homology]] groups $H_0(W)\cong\mathbb{Z}$, $H_2(W)\cong\mathbb{Z}_2$ and $H_5(W)\cong\mathbb{Z}$), but isn't a [[homotopy sphere|homotopy $5$-sphere]].
\end{example}

## Related concepts

* [[homology sphere]]
* [[homotopy sphere]]
* [[rational homotopy sphere]]

## References

* {#Hatcher02} [[Allen Hatcher]]: *Algebraic Topology*, Cambridge University Press (2002) &lbrack;[ISBN:9780521795401](https://www.cambridge.org/gb/academic/subjects/mathematics/geometry-and-topology/algebraic-topology-1?format=PB&isbn=9780521795401), [webpage](https://pi.math.cornell.edu/~hatcher/AT/ATpage.html)&rbrack;

See also:

* Wikipedia, _[Rational homology sphere](https://en.wikipedia.org/wiki/Rational_homology_sphere)_

[[!redirects rational homology spheres]]