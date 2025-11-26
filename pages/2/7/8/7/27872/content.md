
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

_Principal $U(1)$-bundles_ (or _principal $SO(2)$-bundles_) are [[principal bundles]] whose [[structure group]] is the [[unitary group]] [[U(1)|$U(1)$]] (equivalently: the [[circle group]], and [[special orthogonal group]] [[SO(2)|$SO(2)$]]).

Principal $U(1)$-bundles appear in multiple areas of [[mathematics]], for example the [[Seiberg-Witten equations]] or monopole Floer homology. Since $U(1)$ is the [[gauge group]] of [[electromagnetism]], principal $U(1)$-bundles also appear promiently in [[theoretical physics]] (cf. *[[fiber bundles in physics]]*). For example, principal $U(1)$-bundles over the [[2-sphere]] $S^2$, which includes the [[complex Hopf fibration]], can be used to describe the [[Dirac charge quantization]] of hypothetical three-dimensional ($\mathbb{R}^3\setminus\{0\}\simeq S^2$) [[magnetic monopoles]], called _Dirac monopoles_, compare also with *[[D=2 Yang-Mills theory]]*.

## Properties

### Classification

Principal $U(1)$-bundles are classified by the [[classifying space]] [[BU(1)]] of the first [[unitary group]] $U(1)$, which is the infinite [[complex projective space]] $\mathbb{C}P^\infty$. ($E U(1)\cong E SO(2)$ is then the [[infinite-dimensional sphere]] $S^\infty$.) For a [[CW complex]] $X$, one has a [[bijection]]:
$$
  \begin{array}{ccc}
  [X,BU(1)]
    \cong
  [X,\mathbb{C}P^\infty]
    &\xrightarrow{\cong}& 
  Prin_{U(1)}(X)
  \\
  [f] 
    &\mapsto& 
  f^*E U(1)
  \cong f^*S^\infty
  \end{array}
$$

([Mitchell 2011, Theorem 7.4](#Mitchell11)).

Since $U(1)$ is the [[Eilenberg-MacLane space]] $K(\mathbb{Z},1)$, one has that $B U(1)$ is $K(\mathbb{Z},2)$. ([Hatcher 2001, Example 4.50.](#Hatcher01)). Due to this, one can consider the [[identity]] $c_1\colon B U(1)\rightarrow K(\mathbb{Z},2)$, which is exactly the [[first Chern class]] and an [[isomorphism]] ([Hatcher 2017, Theorem 3.10.](#Hatcher)). [[postcomposition|Postcomposition]] then creates a [[bijection]] to [[singular cohomology]]:
$$
  c_1
    \colon
  Prin_{U(1)}(X)
    \cong
  [X,BU(1)]
    \xrightarrow{\cong} 
  [X,K(\mathbb{Z},2)]
    \cong 
  H^2(X,\mathbb{Z})
  \mathrlap{\,.}
$$

The infinite [[complex projective space]] $\mathbb{C}P^\infty$ is a [[CW complex]], whose $n$-[[skeleton]] is $\mathbb{C}P^k$ with the largest natural $k\in\mathbb{N}$ fulfilling $2k\leq n$. For an $n$-dimensional [[CW complex]] $X$, the [[cellular approximation theorem]] ([Hatcher 2001, Theorem 4.8.](#Hatcher01)) states that every [[map]] $X \rightarrow \mathbb{H}P^\infty$ is [[homotopy|homotopic]] to a cellular map, which in particular factorizes over the canonical inclusion $\mathbb{C}P^k\hookrightarrow\mathbb{C}P^\infty$. As a result, the [[composition|postcomposition]] $[X,\mathbb{C}P^k]\rightarrow[X,\mathbb{C}P^\infty]$ is [[surjective]]. In particular for $X$ having no more than three dimension, one has $k=1$ with $\mathbb{C}P^1\cong S^2$. Hence there is a connection to [[cohomotopy]]:
$$
  \pi^2(X) \rightarrow Prin_{U(1)}(X) 
$$
Its composition with the first [[Chern class]] is exactly the [[Hurewicz homomorphism]] $\pi^2(X)\rightarrow H^2(X,\mathbb{Z})$.

### Associated vector bundle

For principal $U(1)$-bundles $P\twoheadrightarrow X$, there is an [[associated fiber bundle|associated]] [[complex line bundle]] $L=P\times_{U(1)}\mathbb{C}\twoheadrightarrow X$ using the [[balanced product]]. If $Q$ is the induced [[principal SU(2)-bundle]] (using the canonical inclusion $U(1)\hookrightarrow SU(2),z\mapsto diag(z,z^{-1})$), then its [[adjoint bundle]] is given by:
$$
Ad(Q)
=L^2\oplus\underline{\mathbb{R}}.
$$

([Donaldson & Kronheimer 91, Eq. (4.2.12)](#donaldsonkronheimer91))

## Examples

* The canonical projection $S^{2n+1}\twoheadrightarrow\mathbb{C}P^n$ is a principal $U(1)$-bundle. For $n=1$ using $\mathbb{C}P^1\cong S^2$, the complex [[Hopf fibration]] $S^3\twoheadrightarrow S^2$ is a special case. In the general case, the classifying map is given by the canonical inclusion:
$$
  \mathbb{C}P^n
    \hookrightarrow
  \mathbb{C}P^\infty
    \cong 
  B U(1).
$$

* One has $S^{2n+1}\cong U(n+1)/U(n)$, hence there is a principal U(1)-bundle $S^3\twoheadrightarrow U(2)$. Such [[principal bundles]] are classified by:
$$
  \pi_3 B U(1)
    \cong
  \pi_2 U(1)
    \cong 
  1\mathrlap{\,.}
$$
([Mitchell 2011, Corollary 11.2.](#Mitchell11))

Hence the principal bundle is trivial, which fits $SU(2)\cong S^3$ and $U(n)\cong\SU(n)\times U(1)$.
* One has $S^n\cong SO(n+1)/SO(n)$, hence there is a principal SO(2)-bundle $SO(3)\twoheadrightarrow S^2$. Such [[principal bundles]] are classified by:
$$
  \pi_2 B U(1)
    \cong
  \pi_1 U(1)
    \cong
  \pi_1 S^1
    \cong
  \mathbb{Z}.
$$

([Mitchell 2011, Corollary 11.2.](#Mitchell11))

## Related entries

* [[circle n-bundle with connection]]

* [[complex oriented cohomology]]

Particular [[principal bundles]]:

* [[double cover]] (principal O(1)-bundle)
* [[principal O(2)-bundle]]
* **principal U(1)-bundle** (principal SO(2)-bundle)
* [[principal U(2)-bundle]] (principal $Spin^\mathrm{c}(3)$-bundle, principal $Spin^\mathrm{h}(2)$-bundle)
* [[principal U(3)-bundle]]
* [[principal SO(3)-bundle]]
* [[principal SO(4)-bundle]]
* [[principal SO(5)-bundle]]
* [[principal SO(6)-bundle]]
* [[principal SO(7)-bundle]]
* [[principal SO(8)-bundle]]
* [[principal SU(2)-bundle]] (principal Sp(1)-bundle, principal Spin(3)-bundle)
* [[principal SU(3)-bundle]]
* [[principal SU(4)-bundle]] (principal Spin(6)-bundle)
* [[principal Sp(2)-bundle]]

## References

* {#FreedUhlenbeck91}  [[Daniel Freed]], [[Karen Uhlenbeck]], _Instantons and Four-Manifolds_, Mathematical Sciences Research Institute Publications, Springer (1991) &lbrack;[doi:10.1007/978-1-4613-9703-8](https://link.springer.com/book/10.1007/978-1-4613-9703-8))&rbrack;

* {#DonaldsonKronheimer97} [[Simon Donaldson]], [[Peter Kronheimer]]: _The Geometry of Four-Manifolds_ (1990, revised 1997), Oxford University Press and Claredon Press, &lbrack;[oup:52942](https://academic.oup.com/book/52942), [doi:10.1093/oso/9780198535539.001.0001](https://doi.org/10.1093/oso/9780198535539.001.0001), ISBN:978-0198502692, ISSN:0964-9174&rbrack;

* {#Hatcher02} [[Allen Hatcher]]: *Algebraic Topology*, Cambridge University Press (2002) &lbrack;[ISBN:9780521795401](https://www.cambridge.org/gb/academic/subjects/mathematics/geometry-and-topology/algebraic-topology-1?format=PB&isbn=9780521795401), [webpage](https://pi.math.cornell.edu/~hatcher/AT/ATpage.html)&rbrack;

* {#Mitchell11} [[Stephen A. Mitchell]], _Notes on principal bundles_ (2011), Lecture Notes. University of Washington, 2011 &lbrack;[pdf](https://sites.math.washington.edu/~mitchell/Notes/prin.pdf), [[MitchellPrincipalBundles.pdf:file]]&rbrack;

* {#Hatcher} [[Allen Hatcher]], _Vector bundles and K-theory_ &lbrack;[web](https://pi.math.cornell.edu/~hatcher/VBKT/VBpage.html)&rbrack;

See also:

* Wikipedia: *<a href="https://en.wikipedia.org/wiki/Principal_U(1)-bundle">Principal U(1)-bundle</a>*


[[!redirects principal U(1)-bundles]] 

[[!redirects U(1)-principal bundle]]
[[!redirects U(1)-principal bundles]]

[[!redirects principal SO(2)-bundle]] 
[[!redirects principal SO(2)-bundles]] 

