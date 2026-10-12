+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


\tableofcontents

## Construction

### Construction from the failure of smooth surgery theory

[[exotic smooth structure|Exotic]]$\phantom{,}\mathbb{R}^4$s, i.e. [[smooth manifold|smooth manifolds]] [[homeomorphism|homeomorphic]] but not [[diffeomorphism|diffeomorphic]] to $\mathbb{R}^4$, may be understood by comparison with [[exotic 7-spheres]] such as the *[[Milnor spheres]]*. In both cases there are [[closed manifold|closed]] [[topological manifold|topological]] $n$-manifolds $M$ ($n = 8$ resp. $4$) that admit no [[smooth structure]], but become smoothable once a closed $n$-[[ball]] is removed. The failure lies in gluing the ball back in. The conclusions differ, though. For $n = 8$, a [[neighbourhood]] of the removed ball can be taken to be [[diffeomorphism|diffeomorphic]] to $\Sigma \times \mathbb{R}$, where $\Sigma$ is [[homeomorphism|homeomorphic]] to [[7-sphere|$S^7$]] but not [[diffeomorphism|diffeomorphic]] to it, since otherwise a smooth disc could be glued in along $\Sigma$. So $\Sigma$ is an [[exotic 7-spheres|exotic 7-sphere]]. For $n = 4$ this cannot happen, since [[3-sphere|$S^3$]] has no [[exotic smooth structure]] (by [[Moise's theorem]]). Instead the obstruction lies in an [[exotic smooth structure]] on the 4-dimensional collar $S^3 \times \mathbb{R} \cong \mathbb{R}^4 \setminus \{0\}$ itself. This is a manifestation of the failure of smooth [[surgery theory]] in dimension 4, which also produces exotic $\mathbb{R}^4$s.

#### Construction from the K3 surface

A concrete construction is the [[K3 surface]] $K3$, described by the homogenous equation $x^4+y^4+z^4+w^4=0$ in [[twistor space]] $\mathbb{C}P^3$. According to [[Freedman's classification]], it is [[homeomorphic]] to the [[connected sum]] $2\overline{M_{E_8}}\#3(S^2\times S^2)$ of twice the [[orientation]]-reversed [[E8 manifold]] $M_{E_8}$ and thrice the [[complex surface]] $S^2\times S^2\cong\mathbb{C}P^1\times\mathbb{C}P^1$ gained from the product of the [[Riemann sphere]] with itself. Although $K3$ is a smooth [[4-manifold]], $2\overline{M_{E_8}}\#k(S^2\times S^2)$ isn't for $k=0,1,2$. For $k=0$, this follows from [[Donaldson's theorem]], and for $k=1,2$, it was also shown by [[Simon Donaldson]], although [[Donaldson's theorem]] itself no longer applies. (A simpler argument was later obtained with [[Seiberg-Witten invariants]].) Hence a smooth surgery along the connecting sphere $S^3$ to remove one, two or three $S^2\times S^2$ from the smooth [[K3 surface]] $K3$ must fail. (It is an open question whether this also holds for any connected sum of the [[K3 surface]] $K3$, which is known as [[11/8 conjecture]].) In the simplest surgery of removing three $S^2\times S^2$, the failure spawns an [[exotic R^4]] in $\#3(S^2\times S^2)$.

#### Construction from a nine-fold blow-up

The [[intersection form]] of the smooth [[complex surface]] $\mathbb{C}P^2\#9\overline{\mathbb{C}P^2}$, the simplest example of an [[elliptic surface]] known as [[Dolgachev surface]], is $[+1]\oplus 9[-1]
\cong -E_8\oplus[+1]\oplus[-1]$ with the isomorphism coming from the Hesse-Minkowski theorem. It is therefore the same as for the topological [[4-manifold]] $\overline{M_{E_8}}\#\mathbb{C}P^2\#*\overline{\mathbb{C}P^2}$ using the [[fake second complex projective space]], so [[Freedman's classification]] claims both to be [[homeomorphic]]. In particular, that makes $\overline{M_{E_8}}\#\mathbb{C}P^2\#*\overline{\mathbb{C}P^2}$ [[smoothable]]. But a smooth surgery to remove $\mathbb{C}P^2$ results in the non-[[smoothable]] manifold $\overline{M_{E_8}}\#*\overline{\mathbb{C}P^2}$, which follows from its [[intersection form]] $-E_8\oplus[-1]$ being negative definite and not diagonalizable, which [[Donaldson's theorem]] forbids if it was [[smoothable]]. The failure of this smooth surgery spawns an [[exotic R^4]] in $\mathbb{C}P^2$.

#### Construction from a ten-fold blow-up

The previous construction can be expanded: The [[intersection form]] of the smooth [[complex surface]] $\mathbb{C}P^2\# 10\overline{\mathbb{C}P^9}$ is $[+1]\oplus 10[-1]
\cong -E_8\oplus H\oplus[-1]$, the same as for the topological [[4-manifold]] $\overline{M_{E_8}}\#(S^2\times S^2)\#*\overline{\mathbb{C}P^2}$, so [[Freedman's classification]] claims both to be [[homeomorphic]] and in particular the latter to be [[smoothable]]. But a smooth surgery to remove $S^2\times S^2$ again results in the non-[[smoothable]] manifold $\overline{M_{E_8}}\#*\overline{\mathbb{C}P^2}$. The failure of this smooth surgery spawns an [[exotic R^4]] in $S^2\times S^2$.

### Construction from the failure of the smooth h-cobordism theorem

According to [[Michael Freedman]], the four-dimensional topological [[h-cobordism theorem]] holds, while according to [[Simon Donaldson]], the four-dimensional smooth [[h-cobordism theorem]] doesn't hold. Let $W$ be a smooth [[h-cobordism]] between smooth [[4-manifolds]] $M$ and $N$, for which there is no [[diffeomorphism]] $W\cong M\times[0,1]$, although there must be a [[homeomorphism]] $W\cong M\times[0,1]$. In this case there exists an open sub-cobordism $U\subset W$ with a [[homeomorphism]] $U\cong D^4\times[0,1]\cong\mathbb{R}^4\times[0,1]$ and a [[compact]] [[contractible]] sub-cobordism $K\subset U$, so that $W$ and $U$ are indeed smoothly trivial cobordisms outside of $K$, hence there are diffeomorphisms:
$$
W\setminus K
\cong(M\setminus K)\times[0,1];
$$
$$
U\setminus K
\cong(U\cap M\setminus K)\times[0,1].
$$
Now $U$ connects the two open subsets $U\cap M\setminus K$ and $U\cap N\setminus K$, which are [[homeomorphic]] to $\mathbb{R}^4$, but cannot [[diffeomorphic]] to $\mathbb{R}^4$ as this would cause a diffeomorphism $W\cong M\times[0,1]$.

## Idea

There exists [[exotic smooth structure]] on the [[Euclidean space]] $\mathbb{R}^4$ of [[dimension]] 4.

(For all other dimensions there is a unique smooth structure, the standard one, see at _[[smooth structure]]_).

## Related entries

[[!include four-dimensional geometry and topology -- table]]

## References

* {#Gompf83} [[Robert Gompf]], _Three exotic $\mathbb{R}^4$ and other anomalies_, J. Differential Geom. **18** 2 (1983), pp. 317-328 &lbrack;[doi:10.4310/jdg/1214437666.full](https://projecteuclid.org/journals/journal-of-differential-geometry/volume-18/issue-2/Three-exotic-mathbfR4s-and-other-anomalies/10.4310/jdg/1214437666.full)&rbrack;

* {#Gompf85} [[Robert Gompf]], _An infinite set of exotic $\mathbb{R}^4$'s_, J. Differential Geom. **21** 2 (1985) &lbrack;[doi:10.4310/jdg/1214439566](https://projecteuclid.org/journals/journal-of-differential-geometry/volume-21/issue-2/An-infinite-set-of-exotic-mathbfR4s/10.4310/jdg/1214439566.pdf) [pdf](https://scispace.com/pdf/an-infinite-set-of-exotic-mathbf-r-4-s-3epe5lmc05.pdf)&rbrack;

See also:

* Wikipedia, _[Exotic R4](https://en.wikipedia.org/wiki/Exotic_R4)_

[[!redirects exotic Euclidean space]]