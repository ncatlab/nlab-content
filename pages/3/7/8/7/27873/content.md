+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Principal SU(2)-bundles_ (or _principal Sp(1)-bundles_) are special [[principal bundles]] with the second [[special unitary group]] $SU(2)$ (isomorphic to the first [[symplectic group]] $Sp(1)$) as [[gauge group]].

Principal SU(2)-bundles appear in multiple areas of mathematics, for example [[Donaldson's theorem]] or [[instanton Floer homology]]. Since $SU(2)$ is the [[gauge group]] of the [[weak interaction]], principal SU(2)-bundles also appear in [[theoretical physics]]. For example, principal SU(2)-bundles over the four-dimensional [[sphere]] $S^4$, which includes the quaternionic [[Hopf fibration]], can be used to describe the [[quantization]] of hypothetical five-dimensional ($\mathbb{R}^5\setminus\{0\}\simeq S^4$) [[magnetic monopoles]], called _[[Yang monopoles]]_, compare also with [[D=4 Yang-Mills theory]]. 

## Classification

Principal SU(2)-bundles are classified by the [[classifying space]] [[BSU(2)]] of the second [[special unitary group]] $SU(2)$, which is the infinite [[quaternionic projective space]] $\mathbb{H}P^\infty$. ($ESU(2)\cong ESp(1)$ is then the [[infinite-dimensional sphere]] $S^\infty$.) For a [[CW complex]] $X$, one has a [[bijection]]:
$$
[X,BSU(2)]
\cong[X,\mathbb{H}P^\infty]
\xrightarrow\cong Prin_{SU(2)}(X),
[f]\mapsto f^*ESU(2)
\cong f^*S^\infty
$$

([Mitchell 11, Theorem 7.4](#Mitchell11))

Since $SU(2)$ rationalized is the rationalized [[Eilenberg-MacLane space]] $K(\mathbb{Z},3)_\mathbb{Q}$, one has that $BSU(2)$ rationalized is $K(\mathbb{Z},4)_\mathbb{Q}$. From the [[Postnikov tower]], one even has a canonical map $c_2\colon BSU(2)\rightarrow K(\mathbb{Z},4)$, which is exactly the second [[Chern class]] and becomes an isomorphism under rationalization. Postcomposition then creates a map to [[singular cohomology]]:
$$
c_2\colon
Prin_{SU(2)}(X)\cong[X,BSU(2)]\rightarrow[X,K(\mathbb{Z},4)]\cong H^4(X,\mathbb{Z})
$$
$\mathbb{H}P^\infty$ is a [[CW complex]], whose $n$-skeleton is $\mathbb{H}P^k$ with the largest natural $k\in\mathbb{N}$ fulfilling $4k\leq n$. ([Hatcher 01, p. 222](#Hatcher01)) For an $n$-dimensional [[CW complex]] $X$, the [[cellular approximation theorem]] ([Hatcher 01, Theorem 4.8.](#Hatcher01)) states that every [[homotopy]] $X\rightarrow\mathbb{H}P^\infty$ is homotopic to a cellular map, which in particular factorizes over the canonical inclusion $\mathbb{H}P^k\hookrightarrow\mathbb{H}P^\infty$. As a result, the postcomposition $[X,\mathbb{H}P^k]\rightarrow[X,\mathbb{H}P^\infty]$ is [[surjective]]. In particular for $X$ having no more than seven dimension, one has $k=1$ with $\mathbb{H}P^1\cong S^4$. Hence there is a connection to [[cohomotopy]]:
$$
\pi^4(X)\rightarrow Prin_{SU(2)}(X) 
$$
Its composition with the second [[Chern class]] is exactly the Hurewicz map $\pi^4(X)\rightarrow H^4(X,\mathbb{Z})$.

## Associated vector bundle

For principal SU(2)-bundles $P\twoheadrightarrow X$, there is an associated complex plane bundle $P\times_{SU(2)}\mathbb{C}^2\twoheadrightarrow X$ using the [[balanced product]].

## Examples

* The canonical projection $S^{4n+3}\twoheadrightarrow\mathbb{H}P^n$ is a principal $SU(2)$-bundle. For $n=1$ using $\mathbb{H}P^1\cong S^4$, the quaternionic [[Hopf fibration]] $S^7\twoheadrightarrow S^4$ is a special case. In the general case, the classifying map is given by the canonical inclusion:
$$
\mathbb{H}P^n\hookrightarrow\mathbb{H}P^\infty
\cong BSU(2).
$$
* One has $S^{2n+1}\cong SU(n+1)/SU(n)$, hence there is a principal SU(2)-bundle $SU(3)\twoheadrightarrow S^5$. Such [[principal bundles]] are classified by:
$$
\pi_5BSU(3)
\cong\pi_4SU(3)
\cong\pi_4S^3
\cong\mathbb{Z}_2.
$$
([Mitchell 11, Corollary 11.2.](#Mitchell11))
$SU(3)\twoheadrightarrow S^5$ is the unique non-trivial principal bundle, which can be detected by the fourth [[homotopy group]]:
$$
\pi_4SU(3)
\cong 1;
$$
$$
\pi_4(S^5\times SU(2))
\cong\pi_4(S^5)\times\pi_4S^3
\cong\mathbb{Z}_2.
$$
([Donaldson 83, p. 295](#Donaldson83))

* One has $S^{4n+3}\cong Sp(n+1)/Sp(n)$, hence there is a principal Sp(1)-bundle $Sp(2)\twoheadrightarrow S^7$. Such [[principal bundles]] are classified by:
$$
\pi_7BSU(3)
\cong\pi_6SU(3)
\cong\pi_6S^3
\cong\mathbb{Z}_{12}.
$$
([Mitchell 11, Corollary 11.2.](#Mitchell11))

## Related entries

* [[principal U(1)-bundles]]

## References

* {#Donaldson83} [[Simon Donaldson]]. _An application of gauge theory to four-dimensional topology_. In: Journal of Differential Geometry. 18. Jahrgang, Nr. 2, 1. Januar 1983, [doi:10.4310/jdg/1214437665](https://projecteuclid.org/journals/journal-of-differential-geometry/volume-18/issue-2/An-application-of-gauge-theory-to-four-dimensional-topology/10.4310/jdg/1214437665.full)
* {#Donaldson87} [[Simon Donaldson]]. _The orientation of Yang-Mills moduli spaces and 4-manifold topology_. In: Journal of Differential Geometry. 26. Jahrgang, Nr. 3, 1. Januar 1987, [doi:10.4310/jdg/1214441485](https://projecteuclid.org/journals/journal-of-differential-geometry/volume-26/issue-3/The-orientation-of-Yang-Mills-moduli-spaces-and-4-manifold/10.4310/jdg/1214441485.full)
* {#FreedUhlenbeck91}  [[Daniel Freed]], [[Karen Uhlenbeck]], _Instantons and Four-Manifolds_, Mathematical Sciences Research Institute Publications, Springer 1991 ([doi:10.1007/978-1-4613-9703-8](https://link.springer.com/book/10.1007/978-1-4613-9703-8))
* {#Hatcher02} [[Allen Hatcher]]: *Algebraic Topology*, Cambridge University Press (2002) &lbrack;[ISBN:9780521795401](https://www.cambridge.org/gb/academic/subjects/mathematics/geometry-and-topology/algebraic-topology-1?format=PB&isbn=9780521795401), [webpage]
(https://pi.math.cornell.edu/~hatcher/AT/ATpage.html)&rbrack;
* {#Mitchell11} [[Stephen A. Mitchell]], _Notes on principal bundles_ (2011), Lecture Notes. University of Washington, 2011 ([pdf](https://sites.math.washington.edu/~mitchell/Notes/prin.pdf), [[MitchellPrincipalBundles.pdf:file]])
* {#Hatcher} [[Allen Hatcher]], _Vector bundles and K-theory_ ([web](https://pi.math.cornell.edu/~hatcher/VBKT/VBpage.html))

See also:

* Wikipedia, _[Principal SU(2)-bundle][pb]_

[pb]: https://en.wikipedia.org/wiki/Principal_SU(2)-bundle 

[[!redirects principal Sp(1)-bundle]]
[[!redirects principal Sp(1)-bundles]]
[[!redirects principal SU(2)-bundles]]