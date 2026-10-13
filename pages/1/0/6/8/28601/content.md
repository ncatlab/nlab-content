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

## Idea

_Donaldson invariants_, due to [Donaldson 1986](#Donaldson1986), [1990](#Donaldson1990), are [[invariants]] of the [[smooth structure]] of smooth [[4-manifolds]] based on the methods behind [[Donaldson's theorem]], due to [Donaldson 1983](#Donaldson83), [1987](#Donaldson87). In particular, key informations are obtained from the [[Yang-Mills moduli space]] of the [[Yang-Mills equations]] on the [[4-manifold]], which as [[partial differential equations]] depend on the [[smooth structure]]. Donaldson invariants can distinguish these, hence are able to detect [[exotic smooth structures]].

## SU(2) Donaldson invariants

Let $X$ be an [[oriented]] [[closed manifold|closed]] [[smooth]] [[4-manifold]] and $P\twoheadrightarrow X$ be a [[principal SU(2)-bundle]], then there exists a unique [[homotopy class]] represented by a [[classifying map]] $\tau\colon X\rightarrow BSU(2)\cong\mathbb{H}P^\infty$ into the [[BSU(n)|classifying space for SU(2)]] giving a pullback $P=\tau^*ESU(2)=\tau^*S^\infty$. With the [[Kronecker pairing]] and the [[fundamental class]] $[X]\in H_4(X,\mathbb{Z})$ from the [[orientation]], the second [[Chern class]] concretely gives a group isomorphism:
$$
\langle c_2(-),[X]\rangle\colon
Prin_{SU(2)}(X)\xrightarrow\cong\mathbb{Z}.
$$
Let $\mathcal{A}:=\Omega_{Ad}^1(P,\mathfrak{su}(2))$ be the configuration space of connections on $P$, which is an [[affine vector space]] not canonically isomorphic to $\Omega^1(X,Ad(P))$. Let $\mathcal{G}\coloneqq Aut_{SU(2)}(P)$ be the [[gauge group]] of [[gauge transformations]] of $P$, which acts on $\mathcal{A}$. Let $\mathcal{B}\coloneqq\mathcal{A}/\mathcal{G}$ be the [[orbit space]], ([Don. 86, Eq. (2.1)](#Donaldson1986)) then there is a [[weak homotopy equivalence]] $\mathcal{B}\rightarrow Map_P(X,BSU(2))$ in the [[homotopy class]] of the [[classifying map]] of $P$. ([Don. 86, Lem. (2.4)](#Donaldson1986), [Don. & Kro. 97, Prop. 5.1.4](#DonaldsonKronheimer97)) Currying it corresponds to a map $\mathcal{B}\times X\rightarrow BSU(2)$ and through pullback a principal $SU(2)$-bundle $\widetilde{P}\twoheadrightarrow\mathcal{B}\times X$. ([Don. & Kro. 97, Eq. (5.1.5)](#DonaldsonKronheimer97)) For every gauge class $[A]\in\mathcal{B}$, one has $\widetilde{P}\vert_{\{[A]\}\times X}\cong P\twoheadrightarrow X$. With the second [[Chern class]] $c_2(\widetilde{P})\in H^4(\mathcal{B}\times X,\mathbb{Z})$, the [[slant product]] yields a map: ([Don. 86, Def. 2.5](#Donaldson1986), [Fre. & Uhl. 84, p. xi-xii](#FreedUhlenbeck84), [Don. & Kro. 97, p. 176-177](#DonaldsonKronheimer97))
$$
\mu\colon
H_2(X,\mathbb{Z})\rightarrow H^2(\mathcal{B},\mathbb{Z}),
\mu(\alpha)\coloneqq c_2(\widetilde{P})/\alpha.
$$
With the subset $\mathcal{M}\subset\mathcal{B}$ of an (anti) self-dual [[Yang-Mills moduli space]] there is an induced map $H^2(\mathcal{B},\mathbb{Z})\hookrightarrow H^2(\mathcal{M},\mathbb{Z})$, which through postcomposition yields a map $\mu\colon H_2(X,\mathbb{Z})\rightarrow H^2(\mathcal{M},\mathbb{Z})$. With the interpretation of the homology classes as embedded surfaces $i\colon\Sigma\hookrightarrow M$ with $i_*[\Sigma]\in H_2(M,\mathbb{Z})$ and the interpretation of the cohomology classes as [[differential forms]] of second order using [[de Rham cohomology]] $H^2(\mathcal{M},\mathbb{R})\cong H_{dR}^2(\mathcal{M})$, one can see the map $\mu$ as mapping embedded surfaces in $M$ to differential forms of second order in $\mathcal{M}$. Donaldson invariants are defined using the integration of these differential forms, which is disrupted by the missing [[compactness]] and the singularities of the moduli space. A [[compactification]] $\mathcal{M}\subset\overline\mathcal{M}$ can be constructed using [[Uhlenbeck's compactness theorem]] and leads to a $\mathbb{Z}$-linear map $\mu\colon H_2(X,\mathbb{Z})\rightarrow H^2(\overline\mathcal{M},\mathbb{Z})$.

Let $P_k\twoheadrightarrow X$ be the unique [[principal SU(2)-bundle]] with $\langle c_2(P_k),[X]\rangle=k$ according to the above group isomorphism, then $\langle p_1 Ad(P_k),[X]\rangle=-4k$ for the first [[Pontrjagin class]] of the [[adjoint bundle]] and the virtual dimension of its anti self-dual Yang-Mills (ASDYM) moduli space is given with the [[Atiyah-Singer index theorem]] by: ([Sco. 05, p. 355](#Scorpan05))
$$
\dim\mathcal{M}_k
=-8k-3(1-b_1(M)+b_2^+(M)).
$$
If $-b_1(M)+b_2^+(M)$ is odd, then the virtual dimension is an even number $\dim\mathcal{M}_k=2d_k$, potentially negative given the choice of $k$. With a [[fundamental class]] $\left[\mathcal{M}_k\right]\in H_{2d_k}(\mathcal{M}_k,\mathbb{Z})
\cong\mathbb{Z}^{b_0\left(\mathcal{M}_k\right)}$ since the ASDYM moduli space is orientable, the Donaldson invariant is given with the [[cup product]] and the [[Kronecker pairing]]: ([Sco. 05, p. 355](#Scorpan05))
$$
\mathcal{D}_{X,k}\colon
Sym^{d_k}H_2(X,\mathbb{Z})\rightarrow\mathbb{Z},
\mathcal{D}_{X,k}(\alpha_1,\ldots,\alpha_{d_k})\coloneqq\left\langle\mu(\alpha_1)\smile\ldots\smile\mu(\alpha_{d_k}), \left[\mathcal{M}_k\right]\right\rangle.
$$
Considering the second homology classes in a symmetric setting only up to [[permutation]] comes from the symmetry of the cup product, hence the irrelevance of any order. It can furthermore be shown, that the Donaldson invariants also don't depend on the [[Riemannian metric]] and therefore only on the smooth structure.

## Relation to Poincaré duality

Let $e\in H^2(X,\mathbb{Z})$ be a cohomology class class with self-intersection $Q(e,e)=e^2[X]=-1$. If $\widetilde{e}\colon\mathbb{C}P^2\hookrightarrow\mathcal{M}$ is the boundary inclusion of a neighborhood of its singularity and $\widetilde{e}^*\colon H^2(\mathcal{M},\mathbb{Z})\rightarrow H^2(\mathbb{C}P^2,\mathbb{Z})\cong\mathbb{Z}$ is the induced map on cohomology with the latter generated by the first [[Chern class]] $c_1(H)$ of the [[tautological line bundle]] $H\twoheadrightarrow\mathbb{C}P^2$, then its composition is exactly: ([Don. 1986, Lemma 2.28](#Donaldson1986))
$$
\widetilde{e}^*\circ\mu
=-\langle e,-\rangle c_1(H)\colon
H_2(X,\mathbb{Z})\rightarrow H^2(\mathbb{C}P^2,\mathbb{Z})
\cong\mathbb{Z}.
$$
As mentioned in the definition, the boundary of the moduli space $\mathcal{M}$ is $X$ (corresponding to the positions of the instantons when shrinking their scale down and considering the limit) and gives a [[compactification]] $\overline\mathcal{M}=\mathcal{M}\cup X$. If $\tau\colon X\hookrightarrow\overline\mathcal{M}$ is the boundary inclusion and $\tau^*\colon H^2(\overline\mathcal{M},\mathbb{Z})\rightarrow H^2(X,\mathbb{Z})$ is the induced map on cohomology, then its composition with the Donaldson invariant is exactly [[Poincaré duality]]: ([Don. 1986, Lemma 3.8](#Donaldson1986))
$$
PD
=\tau^*\circ\mu\colon
H_2(X,\mathbb{Z})\rightarrow H^2(X,\mathbb{Z})
$$
Both these results can be combined in the [[intersection form]]. Let $\alpha,\beta\in H_2(X,\mathbb{Z})$, then using that pullbacks (like $\tau^*$ and $\widetilde{e}^*$) commute with the [[cup product]] and under the [[Kronecker pairing]] become pushouts (like $\tau_*$ and $\widetilde{e}_*$) yields: ([Don. 1986, p. 291](#Donaldson1986))
$$\begin{aligned}
Q(\alpha,\beta)
&=\langle PD(\alpha)\smile PD(\beta),[X]\rangle
=\langle\tau^*\mu(\alpha)\smile\tau^*\mu(\beta),[X]\rangle \\
&=\langle\mu(\alpha)\smile\mu(\beta),\tau_*[X]\rangle
=\frac{1}{2}\sum_{e^2[X]=-1}\pm_e\langle\mu(\alpha)\smile\mu(\beta),\widetilde{e}_*[\mathbb{C}P^2]\rangle \\
&=\frac{1}{2}\sum_{e^2[X]=-1}\pm_e\langle\widetilde{e}^*\mu(\alpha)\smile\widetilde{e}^*\mu(\beta),[\mathbb{C}P^2]\rangle
=\frac{1}{2}\sum_{e^2[X]=-1}\pm_e\langle\alpha,e\rangle\langle\beta,e\rangle\underbrace{\langle c_1^2(H),[\mathbb{C}P^2]\rangle}_{=1}
\end{aligned}$$
In the middle, the $\pm_e$ account for potential sign differences due to change of [[orientation]] and the [[bordism]] of the moduli space between $X$ and a [[disjoint union]] of $\mathbb{C}P^2$ is used to shift $\tau_*[X]$ to the various $\widetilde{e}_*[\mathbb{C}P^2]$.

## Change of instanton number

According to the above formula, $\dim\mathcal{M}_{k+1}=\dim\mathcal{M}_k+8$ holds under a change of the instanton number, expanding the input of the Donaldson invariant by four new second homology classes. More generally, the slant product yields a $\mathbb{Z}$-linear map $\mu\colon H_n(X,\mathbb{Z})\rightarrow H^{4-n}(\overline\mathcal{M},\mathbb{Z})$, ([Don. & Kro. 97, p. 176-177](#DonaldsonKronheimer97), [Sco. 05, p. 355](#Scorpan05)) so for $X$ connected with $H_0(X,\mathbb{Z})\cong\mathbb{Z}$ a map $\mu\colon\mathbb{Z}\rightarrow H^4(\overline\mathcal{M},\mathbb{Z})$. Hence one can also expand the Donaldson invariant by two images of a generator.

## SO(3) Donaldson invariants

Let $P\twoheadrightarrow X$ be a [[principal SO(3)-bundle]], then there exists a unique [[homotopy class]] represented by a [[classifying map]] $\tau\colon X\rightarrow BSO(3)$ into the [[BSO(n)|classifying space for SO(3)]] giving a pullback $P=\tau^* ESO(3)$. Now the second [[Stiefel-Whitney class]] and the first [[Pontrjagin class]] give a group isomorphism:
$$
(w_2,\langle p_1(-),[X]\rangle)\colon
Prin_{SO(3)}(X)\xrightarrow\cong\{(v,n)\in H^2(X,\mathbb{Z}_2)\times\mathbb{Z}|\langle v^2,[X]\rangle\equiv n mod 4\}.
$$
In this case, the first [[Pontrjagin class]] replaces the second [[Chern class]] in the [[slant product]].

## Donaldson invariants of compactification

### Compactification to two dimensions

According to the classification of surfaces, every oriented closed 2-manifold (surface) is [[homeomorphic]] to a Sigma surface $\Sigma_g=\# gT^2$, given as a connected sum of 2-tori $T^2=S^1\times S^1$ with the convention $\Sigma_0=S^2$. Now the Donaldson invariants can be considered on the [[4-manifold]] $\Sigma_g\times S^2$.

### Compactification to three dimensions

For an oriented closed 3-manifold $Y$, one can consider the Donaldson invariants on the [[4-manifold]] $Y\times S^1$. For general structure groups, they relate to the [[Rozansky-Witten invariant]]s of $Y$ and for the structure group $SU(2)$, they relate to the [[Casson-Walker-Lescop invariant]] of $Y$.

## References

[[Donaldson's theorem]] was introduced and improved in:

* {#Donaldson83} [[Simon Donaldson]]: _An application of gauge theory to four-dimensional topology_, Journal of Differential Geometry. **18** Jahrgang, Nr. 2 (1983) &lbrack;[doi:10.4310/jdg/1214437665](https://projecteuclid.org/journals/journal-of-differential-geometry/volume-18/issue-2/An-application-of-gauge-theory-to-four-dimensional-topology/10.4310/jdg/1214437665.full)&rbrack;

* {#Donaldson87} [[Simon Donaldson]]. _The orientation of Yang-Mills moduli spaces and 4-manifold topology_. In: Journal of Differential Geometry. 26. Jahrgang, Nr. 3, 1. Januar 1987, [doi:10.4310/jdg/1214441485](https://projecteuclid.org/journals/journal-of-differential-geometry/volume-26/issue-3/The-orientation-of-Yang-Mills-moduli-spaces-and-4-manifold/10.4310/jdg/1214441485.full)

Donaldson invariants were introduced and improved in the original articles:

* {#Donaldson1986} [[Simon K. Donaldson]]: *Connections, cohomology and the intersection forms of 4-manifolds*, J. Differential Geom. **24** 3 (1986) 275--341 \[<a href="https:/doi.org/10.4310/jdg/1214440551">doi:10.4310/jdg/1214440551</a>\]

* {#Donaldson1990} [[Simon K. Donaldson]]: *Polynomial invariants for smooth four-manifolds*, Topology, **29** 3 (1990) 257--315 \[<a href="https://doi.org/10.1016/0040-9383(90)90001-Z">doi:10.1016/0040-9383(90)90001-Z</a>\]

Reviews include:

* {#FreedUhlenbeck84} [[Daniel Freed]], [[Karen Uhlenbeck]], _Instantons and Four-Manifolds_ (1984, revised 1991), Mathematical Sciences Research Institute Publications, Springer ([doi:10.1007/978-1-4613-9703-8](https://link.springer.com/book/10.1007/978-1-4613-9703-8))

* {#DonaldsonKronheimer97} [[Simon Donaldson]], [[Peter Kronheimer]]: _The Geometry of Four-Manifolds_ (1990, revised 1997), Oxford University Press and Claredon Press, &lbrack;[oup:52942](https://academic.oup.com/book/52942), [doi:10.1093/oso/9780198535539.001.0001](https://doi.org/10.1093/oso/9780198535539.001.0001), ISBN:978-0198502692, ISSN:0964-9174&rbrack;

* {#Scorpan05} [[Alexandru Scorpan]], _The Wild World of 4-Manifolds_, American Mathematical Society (2005) &lbrack;[ISBN 978-1470468613](https://bookstore.ams.org/fourman)&rbrack;

See also:

* Wikipedia, _[Donaldson invariant](https://en.wikipedia.org/wiki/Donaldson_invariant)_

[[!redirects Donaldson invariants]]