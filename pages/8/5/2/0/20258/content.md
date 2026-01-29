
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Spheres
+--{: .hide}
[[!include spheres -- contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A [[topological manifold|topological]] [[7-sphere]] equipped with an [[exotic smooth structure]] is called an _exotic 7-sphere_.

## Milnor's construction
 {#Construction}

[Milnor (1956)](#Milnor1956) gave the first examples of exotic smooth structures on the [[7-sphere]], finding at least seven. 

The [[exotic 7-spheres]] constructed in [Milnor 1956](#Milnor1956) are all examples of [[fibre bundles]] over the [[4-sphere]] $S^4$ with [[fibre]] the [[3-sphere]] $S^3$, with [[structure group]] the [[special orthogonal group]] [[SO(4)]] (see also at _[[8-manifold]]_ the section _[With exotic boundary 7-spheres](8-manifold#ExoticBoundary7Spheres)_):

By the classification of bundles on spheres via the [[clutching construction]], these correspond to [[homotopy classes]] of maps $S^3 \to SO(4)$, i.e. elements of $\pi_3(SO(4))$. From the table at [orthogonal group -- Homotopy groups](orthogonal+group#HomotopyGroups), this latter group is $\mathbb{Z}\oplus\mathbb{Z}$. Thus any such bundle can be described, up to [[isomorphism]], by a [[pair]] of [[integers]] $(n,m)$.

Let $E_{m,n}\twoheadrightarrow S^4$ denote the real vector bundle corresponding to the integer pair $m,n\in\mathbb{Z}$. There is an orientation-reversing vector bundle isomorphism $E_{m,n}\cong E_{-m,-n}$. ([McEnroe 15, Lem. 6.14](#McEnroe15)) Let $\alpha\in H^4(S^4)\cong\mathbb{Z}$ be a [[generator]], then its [[Euler class]] and [[fractional first Pontryagin class]] are:
$$
e(E_{m,n})
=-(m+n)\alpha;
$$
$$
\frac{p_1(E_{m,n})}{2}
=(n-m)\alpha.
$$

([McEnroe 15, Eq. (6.17) & Eq. (6.29)](#McEnroe15))

With the choice of a [[Riemannian metric]] on it, one has a disk bundle $D(E_{m,n})\twoheadrightarrow S^4$ by taking the disks $D^4\subset\mathbb{R}^4$ of each fiber, a sphere bundle $S(E_{m,n})=\partial D(E_{m,n})\twoheadrightarrow S^4$ by taking the spheres $S^3\subset\mathbb{R}^4$ of each fiber as well as a [[Thom space]] $Th(E_{m,n})=D(E_{m,n})/S(E_{m,n})$. None of their topological or smooth structures depend on the choice of the [[Riemannian metric]].

A special case is the [[quaternionic Hopf fibration]] $h_\mathbb{H}\colon\mathbb{H}^2\supset S^7\twoheadrightarrow S^4\cong\mathbb{H}P^1,[q,p]\mapsto[q:p]$, which is a [[principal SU(2)-bundle]] and the [[sphere bundle]] of the [[real vector bundle]] $(\gamma_\mathbb{H}^{1,1})_\mathbb{R}\twoheadrightarrow S^4$ represented by the [[continuous map]]:
$$
S^4
\cong\mathbb{H}P^1
\hookrightarrow\mathbb{H}P^\infty
\cong B SU(2)
\hookrightarrow B SO(4),
$$
which corresponds to $m=0$ and $n=1$. ([McEnroe 15, p. 11](#McEnroe15))

More generally for $n+m=1$, a [[Morse function]] with exactly two [[critical points]] on $S(E_{m,n})$ exists, implying that it is [[homeomorphic]] to $S^7$ according to the [[Reeb sphere theorem]]. If it is further [[diffeomorphic]], then it is possible to glue the disk bundle $D(E_{m,n})$ and the disk $D^8$ together along their common boundary $S(E_{m,n})\cong S^7$ using a [[pullback]] to obtain the closed [[8-manifold]]:
$$
M_{m,n}
=D(E_{m,n})+_{S^7}D^8.
$$
Due to $H^4(M_{m,n},\mathbb{Z})\cong\mathbb{Z}$ and $H^8(M_{m,n},\mathbb{Z})\cong\mathbb{Z}$, the [[intersection form]] is described by a single [[integer]] and hence the signature can only be $\sigma(M_{m,n})=1$ with suitable [[orientation]]. According to [[Hirzebruch's signature theorem]], the signature is also given by:
$$
\sigma(M_{m,n})
=\frac{1}{45}\langle 7p_2(M_{m,n})-p_1^2(M_{m,n}),[M_{m,n}]\rangle
$$

([McEnroe 15, Thrm. 6.37](#McEnroe15))

Since the first [[Pontrjagin class]] is known, but the second [[Pontrjagin class]] is not, [[John Milnor]] eliminated it by projecting to the following [[modulo]]-7 [[diffeomorphism]] [[invariant]]:
$$
\begin{aligned}
4(m-n)^2 mod 7
=-\langle p_1^2(M_{m,n}),[M_{m,n}]\rangle mod 7
=45\sigma(M_{m,n}) mod 7
=\pm 45 mod 7
=\pm 3 \\
\Rightarrow
\left(\frac{p_1(E_{m,n})}{2}\right)^2
=(m-n)^2 mod 7
=1.
\end{aligned}
$$

([McEnroe 15, Thrm. 6.44](#McEnroe15))

$S(E_{m,n})$ with $m+n=1$ is then [[diffeomorphic]] to the standard $7$-sphere $S^7$ if and only if this equation holds and hence the [[modulo]]-7 [[diffeomorphism]] [[invariant]] $(m-n)^2-1 mod 7$ vanishes. Examples like $m=1$ and $n=2$ show, that this doesn't have to be true. In this case, the contradiction in [[Hirzebruch's signature theorem]] is resolved by the previously used assumption of $S(E_{m,n})$ and $S^7$ to be [[diffeomorphic]] to obtain the glueing $M_{m,n}$ to not be true. $E_{m,n}$ with $m+n=1$ and $(m-n)^2 mod 7\neq 1$ is then [[homeomorphic]] but not [[diffeomorphic]] to the standard $7$-sphere $S^7$.

By using the [[connected sum]] operation, the set of smooth, non-diffeomorphic structures on the $n$-sphere has the structure of an [[abelian group]]. 
For the [[7-sphere]], it is the [[cyclic group]] $\mathbb{Z}/{28}$ and [Brieskorn (1966)](#Brieskorn66) found the generator $\Sigma$ so that $\underbrace{\Sigma\#\cdots\#\Sigma}_28$ is the standard sphere.

Review includes ([Kreck 10, chapter 19](#Kreck10), [McEnroe 
15](#McEnroe15), [Joachim-Wraith](#JoachimWraith)). 

## Examples

* [[Gromoll-Meyer sphere]]


## Properties

### As near-horizon geometries of black M2-branes
 {#AsNearHorizonGeometriesOfBlackM2Branes}


From the point of view of [[M-theory on 8-manifolds]], these [[8-manifolds]] $X$ with (exotic) [[7-sphere]] [[boundaries]] in [Milnor's construction](#Construction) correspond to [[near horizon limits]] of [[black brane|black]] [[M2 brane]] spacetimes $\mathbb{R}^{2,1} \times X$, where the [[M2-branes]] themselves would be sitting at the center of the [[7-spheres]] (if that were included in the spacetime, see also [[Dirac charge quantization]]).

([Morrison-Plesser 99, section 3.2](#MorrisonPlesser99), [[schreiber:Twisted Cohomotopy implies M-theory anomaly cancellation|FSS 19, 3.8]]))



## References

### General



* {#Milnor1956} [[John Milnor]], _On manifolds homeomorphic to the 7-sphere_, Annals of Mathematics 64 (2): 399&#8211;405 (1956) ([pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/exotic.pdf), [doi:10.1142/9789812836878_0001](https://doi.org/10.1142/9789812836878_0001))


* {#Brieskorn66} [[Egbert Brieskorn]], *Beispiele zur Differentialtopologie von Singularitäten*, Inventiones mathematicae **2** (1966) 1–14 $[$[doi:10.1007/BF01403388](https://doi.org/10.1007/BF01403388)$]$

* {#Kreck10} [[Matthias Kreck]], chapter 19 of _Exotic 7-spheres_ of  _Differential Algebraic Topology -- From Stratifolds to Exotic Spheres_, AMS 2010

* {#McEnroe15} Rachel McEnroe, _Milnor' construction of exotic 7-spheres_, 2015 ([pdf](http://math.uchicago.edu/~may/REU2015/REUPapers/McEnroe.pdf))

* {#JoachimWraith} [[Michael Joachim]], D. J. Wraith, _Exotic spheres and curvature_ ([pdf](https://ivv5hpp.uni-muenster.de/u/joachim/exo.pdf))

* [[Niles Johnson]], _Visualizing 7-manifolds_, 2012 ([nilesjohnson.net/seven-manifolds.html](https://nilesjohnson.net/seven-manifolds.html))

* {#CrowleyEscher03} [[Diarmuid Crowley]], [[Christine Escher]], _A classification of $S^3$-bundles over $S^4$_, Differential Geometry and its Applications Volume 18, Issue 3, May 2003, Pages 363-380 (<a href="https://doi.org/10.1016/S0926-2245(03)00012-3">doi:10.1016/S0926-2245(03)00012-3</a>))

See also:

* Wikipedia, _[Exotic sphere](https://en.wikipedia.org/wiki/Exotic_sphere)_

In relation to [[TQFT]]:

* [[Ben Gripaios]], [[Oscar Randal-Williams]]: *TQFTs do not detect the Milnor sphere* &lbrack;[arXiv:2601.20828](https://arxiv.org/abs/2601.20828)&rbrack;




### In M-theory

* {#MorrisonPlesser99} [[David Morrison]], [[M. Ronen Plesser]], section 3.2 of _Non-Spherical Horizons, I_, Adv. Theor. Math. Phys. 3:1-81, 1999 ([arXiv:hep-th/9810201](https://arxiv.org/abs/hep-th/9810201))


[[!redirects exotic 7-spheres]]


[[!redirects Brieskorn sphere]]
[[!redirects Brieskorn spheres]]

[[!redirects Milnor sphere]]
[[!redirects Milnor spheres]]

