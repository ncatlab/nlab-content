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

_Principal SU(2)-bundles_ (or _principal Sp(1)-bundles_) are special [[principal bundles]] with the second [[special unitary group]] [[SU(2)|$SU(2)$]] (isomorphic to the first [[quaternionic unitary group]] [[Sp(1)|$Sp(1)$]]) as [[structure group]]/[[gauge group]].

Principal $SU(2)$-bundles appear in multiple areas of mathematics, for example [[Donaldson's theorem]] or [[instanton Floer homology]]. Since $SU(2)$ is the [[gauge group]] of the [[weak interaction]], principal $SU(2)$-bundles also appear in [[theoretical physics]] (cf. *[[fiber bundles in physics]]*). For example, principal $SU(2)$-bundles over the [[4-sphere]] $S^4$, which includes the [[quaternionic Hopf fibration]], can be used to describe the [[Dirac charge quantization]] of hypothetical five-dimensional ($\mathbb{R}^5\setminus\{0\}\simeq S^4$) [[magnetic monopoles]], called _[[Yang monopoles]]_, compare also with *[[D=4 Yang-Mills theory]]*. 

## Properties

### Classification

Principal $SU(2)$-bundles are classified by the [[classifying space]] [[BSU(2)]] of the second [[special unitary group]] $SU(2)$, which is also the infinite [[quaternionic projective space]] $\mathbb{H}P^\infty$. ($E SU(2)\cong E Sp(1)$ is then the [[infinite-dimensional sphere]] $S^\infty$.) For a [[CW complex]] $X$, one has a [[bijection]]:
$$
  \begin{array}{ccc}
    [X,B SU(2)]
    \cong
  [X,\mathbb{H}P^\infty]
&\xrightarrow{\cong}& 
Prin_{SU(2)}(X),
  \\
  [f] 
  &\mapsto& 
  f^* E SU(2)
  \cong 
  f^*S^\infty
  \mathrlap{\,.}
  \end{array}
$$

([Mitchell 2011, Theorem 7.4](#Mitchell11))

Since $SU(2)$ [[rationalization|rationalized]] is the [[Eilenberg-MacLane space]] $K(\mathbb{Q},3)_\mathbb{Q}$, one has that $BSU(2)$ rationalized is $K(\mathbb{Q},4)$. From the [[Postnikov tower]], one even has a canonical map $c_2\colon B SU(2)\rightarrow K(\mathbb{Z},4)$, which is exactly the second [[Chern class]] and becomes an [[isomorphism]] under [[rationalization]]. [[composition|Postcomposition]] then creates a map to [[singular cohomology]]:
$$
  c_2
    \colon
  Prin_{SU(2)}(X)
    \cong
  [X,B SU(2)]
    \rightarrow
  [X,K(\mathbb{Z},4)]
    \cong 
  H^4(X,\mathbb{Z})
 \,.
$$

The [[quaternionic projective space]] $\mathbb{H}P^\infty$ is a [[CW complex]], whose $n$-[[skeleton]] is $\mathbb{H}P^k$ with the largest natural $k\in\mathbb{N}$ fulfilling $4k\leq n$. ([Hatcher 2001, p. 222](#Hatcher01)). 

For an $n$-dimensional [[CW complex]] $X$, the [[cellular approximation theorem]] ([Hatcher 01, Theorem 4.8.](#Hatcher01)) states that every [[homotopy]] $X\rightarrow\mathbb{H}P^\infty$ is homotopic to a cellular map, which in particular factorizes over the canonical inclusion $\mathbb{H}P^k\hookrightarrow\mathbb{H}P^\infty$. As a result, the postcomposition $[X,\mathbb{H}P^k]\rightarrow[X,\mathbb{H}P^\infty]$ is [[surjective]]. In particular for $X$ having no more than six dimensions, one has $k=1$ with $\mathbb{H}P^1\cong S^4$. Hence there is a connection to [[cohomotopy]]:
$$
  \pi^4(X)
   \rightarrow   
  Prin_{SU(2)}(X) 
  \mathrlap{\,.}
$$
Its composition with the second [[Chern class]] is exactly the [[Hurewicz homomorphism]] $\pi^4(X)\rightarrow H^4(X,\mathbb{Z})$.

### Adjoint vector bundle

\begin{proposition}
For a principal $SU(2)$-bundle, the first [[Pontrjagin class]] of its [[adjoint bundle]] is given by:
$$
p_1Ad(P)
=-4c_2(P).
$$
\end{proposition}

([Donaldson & Kronheimer 91, Eq. 2.1.37](#donaldsonkronheimer91))

(This relation holds in general for principal $SU(n)$-bundles with $p_1 Ad(P)=-2nc_2(P)$.)

### Associated vector bundle

For principal $SU(2)$-bundles $P\twoheadrightarrow X$, there is an [[associated bundle|associated]] complex plane bundle $P\times_{SU(2)}\mathbb{C}^2\twoheadrightarrow X$ using the [[balanced product]].

## Examples

* The canonical projection $S^{4n+3}\twoheadrightarrow\mathbb{H}P^n$ is a principal $SU(2)$-bundle. For $n=1$ using $\mathbb{H}P^1\cong S^4$, the [[quaternionic Hopf fibration]] $S^7\twoheadrightarrow S^4$ is a special case. In the general case, the classifying map is given by the canonical inclusion:
$$
\mathbb{H}P^n\hookrightarrow\mathbb{H}P^\infty
\cong BSU(2).
$$

* One has $S^{2n+1}\cong SU(n+1)/SU(n)$, hence there is a principal SU(2)-bundle $SU(3)\twoheadrightarrow S^5$. Such [[principal bundles]] are classified by:
$$
  \pi_5BSU(2)
    \cong
  \pi_4SU(2)
    \cong
  \pi_4S^3
    \cong
  \mathbb{Z}_2
  \mathrlap{\,.}
$$
([Mitchell 2011, Corollary 11.2.](#Mitchell11))
$SU(3)\twoheadrightarrow S^5$ is the unique non-trivial principal bundle, which can be detected by the fourth [[homotopy group]]:
$$
  \pi_4 SU(3)
  \cong 
  1;
$$
$$
  \pi_4\big(S^5\times SU(2)\big)
    \cong
  \pi_4(S^5)\times\pi_4 S^3
    \cong
  \mathbb{Z}_2
  \mathrlap{\,.}
$$
([Mimura & Toda 63](#MimuraToda63), [Donaldson 1983, p. 295](#Donaldson83))

* One has $S^{4n+3}\cong Sp(n+1)/Sp(n)$, hence there is a principal Sp(1)-bundle $Sp(2)\twoheadrightarrow S^7$. See in particular [[Spin(5)/SU(2) is the 7-sphere]]. Such [[principal bundles]] are classified by:
$$
  \pi_7 B SU(3)
    \cong
  \pi_6 SU(3)
    \cong
  \pi_6 S^3
    \cong
  \mathbb{Z}_{12}
  \mathrlap{\,.}
$$
([Mitchell 2011, Corollary 11.2.](#Mitchell11))

## Application in Yang-Mills theory

\begin{proposition}
Reducible anti self-dual [[Yang-Mills connections]] of a principal $SU(2)$-bundle $E$ over a [[compact]], [[simply connected]], [[oriented]] [[Riemannian manifold|Riemannian]] [[4-manifold]] $X$ are in [[bijective]] correspondence with non-zero pairs $\pm c\in H^2(X,\mathbb{Z})$ with $c^2=-c_2(E)$.
\end{proposition}

([Donaldson & Kronheimer 97, Prop. (4.2.15)](#DonaldsonKronheimer97))

\begin{proposition}
Irreducible anti self-dual [[Yang-Mills connections]] of a principal $SU(2)$-bundle $E$ over a [[simply connected]] [[Riemannian manifold|Riemannian]] [[4-manifold]] $X$ are still irreducible under the restriction to any non-empty open subset.
\end{proposition}

([Donaldson & Kronheimer 97, Lem. (4.3.21)](#DonaldsonKronheimer97))

## Related entries

Particular [[principal bundles]]:

* [[double cover]] (principal O(1)-bundle)
* [[principal O(2)-bundle]]
* [[principal U(1)-bundle]] (principal SO(2)-bundle)
* [[principal U(2)-bundle]] (principal $Spin^\mathrm{c}(3)$-bundle, principal $Spin^\mathrm{h}(2)$-bundle)
* [[principal U(3)-bundle]]
* [[principal SO(3)-bundle]]
* [[principal SO(4)-bundle]]
* [[principal SO(5)-bundle]]
* [[principal SO(6)-bundle]]
* [[principal SO(7)-bundle]]
* [[principal SO(8)-bundle]]
* **principal SU(2)-bundle** (principal Sp(1)-bundle, principal Spin(3)-bundle)
* [[principal SU(3)-bundle]]
* [[principal SU(4)-bundle]] (principal Spin(6)-bundle)
* [[principal Sp(2)-bundle]]

## References

* {#MimuraToda63} [[Mamoru Mimura]] and [[Hiroshi Toda]], _Homotopy Groups of SU(3), SU(4) and Sp(2)_ (1963), Journal of Mathematics of Kyoto University **3** (2), p. 217–250, [doi:10.1215/kjm/1250524818](https://projecteuclid.org/journals/kyoto-journal-of-mathematics/volume-3/issue-2/Homotopy-Groups-of-SU3-SU4-and-Sp2/10.1215/kjm/1250524818.full)

* {#Donaldson83} [[Simon Donaldson]]: _An application of gauge theory to four-dimensional topology_. In: Journal of Differential Geometry. 18. Jahrgang, Nr. 2 (1983) &lbrack;[doi:10.4310/jdg/1214437665](https://projecteuclid.org/journals/journal-of-differential-geometry/volume-18/issue-2/An-application-of-gauge-theory-to-four-dimensional-topology/10.4310/jdg/1214437665.full)&rbrack;

* {#Donaldson87} [[Simon Donaldson]], _The orientation of Yang-Mills moduli spaces and 4-manifold topology_. In: Journal of Differential Geometry. 26. Jahrgang, Nr. 3 (1987) &lbrack;[doi:10.4310/jdg/1214441485](https://projecteuclid.org/journals/journal-of-differential-geometry/volume-26/issue-3/The-orientation-of-Yang-Mills-moduli-spaces-and-4-manifold/10.4310/jdg/1214441485.full)&rbrack;

* {#FreedUhlenbeck91}  [[Daniel Freed]], [[Karen Uhlenbeck]], _Instantons and Four-Manifolds_, Mathematical Sciences Research Institute Publications, Springer (1991) &lbrack;[doi:10.1007/978-1-4613-9703-8](https://link.springer.com/book/10.1007/978-1-4613-9703-8)&rbrack;

* {#DonaldsonKronheimer97} [[Simon Donaldson]], [[Peter Kronheimer]]: _The Geometry of Four-Manifolds_ (1990, revised 1997), Oxford University Press and Claredon Press, &lbrack;[oup:52942](https://academic.oup.com/book/52942), [doi:10.1093/oso/9780198535539.001.0001](https://doi.org/10.1093/oso/9780198535539.001.0001), ISBN:978-0198502692, ISSN:0964-9174&rbrack;

* {#Hatcher02} [[Allen Hatcher]]: *Algebraic Topology*, Cambridge University Press (2002) &lbrack;[ISBN:9780521795401](https://www.cambridge.org/gb/academic/subjects/mathematics/geometry-and-topology/algebraic-topology-1?format=PB&isbn=9780521795401), [webpage](https://pi.math.cornell.edu/~hatcher/AT/ATpage.html)&rbrack;

* {#Mitchell11} [[Stephen A. Mitchell]], _Notes on principal bundles_ (2011), Lecture Notes. University of Washington, 2011 ([pdf](https://sites.math.washington.edu/~mitchell/Notes/prin.pdf), [[MitchellPrincipalBundles.pdf:file]])

* {#Hatcher} [[Allen Hatcher]], _Vector bundles and K-theory_ &lbrack;[web](https://pi.math.cornell.edu/~hatcher/VBKT/VBpage.html)&rbrack;

See also:

* Wikipedia: *<a href="https://en.wikipedia.org/wiki/Principal_SU(2)-bundle">Principal SU(2)-bundle</a>*

[[!redirects principal Sp(1)-bundle]]
[[!redirects principal Sp(1)-bundles]]
[[!redirects principal SU(2)-bundles]]