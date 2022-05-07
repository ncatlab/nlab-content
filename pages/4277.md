[[!redirects cobordism ring]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
#### Cobordism theory
+--{: .hide}
[[!include cobordism theory -- contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The **(co)bordism ring** $\Omega_*=\oplus_{n\geq 0}\Omega_n$ is the [[graded ring]] whose 

* degree $n$ elements are classes of $n$-[[dimension|dimensional]] [[smooth manifolds]] modulo [[cobordism]];

* product operation is given by the [[Cartesian product]] of manifolds;

* addition operation is given by the [[disjoint union]] of manifolds.

Instead of bare manifolds one may consider manifolds with extra structure, such as [[orientation]], [[spin structure]], [[string structure]], etc. and accordingly there is 

* the _oriented cobordism ring_ $\Omega^{SO}_*$,  

* the _spin cobordism ring_ $\Omega^{Spin}_*$, 

etc. 

In this general context the bare cobordism ring is also denoted $\Omega^O_*$ or $\Omega^{un}_*$, for emphasis.

A ring [[homomorphism]] out of the cobordism ring is a (multiplicative) _[[genus]]_.

More generally, for $X$ a fixed [[manifold]] there is a relative cobordism ring $\Omega_\bullet(X)$ whose 

* elements are classes modulo cobordism over $X$ of manifolds equipped with [[continuous functions]] to $X$ ("singular manifolds");

* multiplication of $[f_1 \colon \Sigma_1 \to X]$ with $[f_2 \colon \Sigma_2 \to X]$ is given by _transversal intersection_ $\Sigma_1 \cap_X \Sigma_2$ over $X$: perturb $f_1$ such $(f_1',f_2)$ becomes a [[transversal maps]] and then form the [[pullback]] $\Sigma_1 \times_{(f_1',f_2)} \Sigma_2$ in [[Diff]].

This product is graded in that it satisfies the **dimension formula**

$$
  (dim X - dim \Sigma_1) + (dim X - dim \Sigma_2) = dim X - dim (\Sigma_1 \cap_X \Sigma_2)
$$

hence

$$
  dim (\Sigma_1 \cap_X \Sigma_2 ) = (dim \Sigma_1 + dim \Sigma_2) - dim X
  \,.
$$

Still more generally, this may be considered for $\Sigma$ being [[manifolds with boundary]]. Then $\Omega(X,A)$ for $(X,A)$ a [[CW pair]] is the ring of cobordism classes, relative boundary, of singular manifolds $\Sigma \to X$ such that the [[boundary]] of $\Sigma$ lands in in $A$.

The resulting [[functor]]

$$
  (X,A) \mapsto \Omega^G_\bullet(X,A)
$$

constitutes a [[generalized homology theory]] (see e.g. [Buchstaber, II.8](#Buchstaber)). Accordingly this is called _[[bordism homology theory]]_.

The [[spectrum]] that represents this under the [[Brown representability theorem]] is the universal [[Thom spectra]] $M G$ (e.g. [[MO]] for $G=O$ or [[MU]] for $G = U$), which canonically is a [[ring spectrum]] under [[Whitney sum]] of [[universal vector bundles]]. Accordingly the (co-bordism ring) itself is equivalently the bordism homology groups of the point, hence the [[stable homotopy groups]] of the [[Thom spectrum]] (this is _[[Thom's theorem]]_)

$$
  \Omega_\bullet^G \simeq \M G_\bullet(\ast) \simeq \pi_\bullet(M G)
  \,.
$$

This remarkable relation between [[manifolds]] and [[stable homotopy theory]] is known as _[[cobordism theory]]_ (or "Thom theory").

On general grounds this is equivalently the $M G$-[[generalized cohomology]] of the point ([[cobordism cohomology theory]])

$$
  \Omega_\bullet^G \simeq M G^\bullet(\ast)
$$

which justifies calling $\Omega_\bullet^G$ both the "bordism ring" as well as the "cobordism ring".

## Properties

### Relation to cohomotopy
 {#RelationToCohomotopy}

Let $X$ be a [[smooth manifold]] of [[dimension]] $n \in \mathbb{N}$ and let $k \leq n$. Then the [[Pontryagin-Thom construction]] induces a [[bijection]]

$$
  [X, S^k]
  \overset{\simeq}{\longrightarrow}
  \Omega^{n-k}(X)
$$

from the [[cohomotopy]] sets of $X$ to the [[cobordism group]] of $(n-k)$-dimensional [[submanifolds]] with [[normal bundle|normal]] [[framed manifold|framing]] up to normally framed [[cobordism]].

In particular, the natural group structure on [[cobordism group]] (essentially given by [[disjoint union]] of submanifolds) this way induces a group structure on the cohomotopy sets.

This is made explicit for instance in [Kosinski 93, chapter IX](#Kosinski93).



## Examples

### Framed cobordism
 {#FramedCobordism}

By [[Thom's theorem]], for any [[(B,f)-structure]] $\mathcal{B}$, there is an [[isomorphism]] (of [[commutative rings]])

$$
  \Omega^{\mathcal{B}}_\bullet
  \overset{\simeq}{\longrightarrow}
  \pi_\bullet(M\mathcal{B})
$$

from the [[cobordism ring]] of manifolds with stable normal $\mathcal{B}$-structure to the [[homotopy groups of a spectrum|homotopy groups]] of the universal $\mathcal{B}$-[[Thom spectrum]]. 

Now for $\mathcal{B} = Fr$ [[framing]] structure, then 

$$
  M Fr \simeq \mathbb{S}
$$

is equivalently the [[sphere spectrum]]. Hence in this case [[Thom's theorem]] states that there is an isomorphism

$$
  \Omega^{fr}_\bullet
  \overset{\simeq}{\longrightarrow}
  \pi_\bullet(\mathbb{S})
$$

between the framed cobordism ring and the [[stable homotopy groups of spheres]].

For discussion of computation of $\pi_\bullet(\mathbb{S})$ this way, see for instance ([Wang-Xu 10, section 2](#WangXu10)).

For instance 

* $\Omega^{fr}_0 = \mathbb{Z}$ because there are two $k$-framings on a single point, corresponding to $\pi_0(O(k)) \simeq \mathbb{Z}_2$, the negative of a point with one framing is the point with the other framing, and so under disjoint union, the framed points form the group of integers;

* $\Omega^{fr}_1 = \mathbb{Z}_2$ because the only compact connected 1-manifold is the circle, there are two framings on the circle, corresponding to $\pi_1(O(k)) \simeq \mathbb{Z}_2$ and they are their own negatives.




### Oriented cobordism
 {#OrientedCobordismRing}

+-- {: .num_prop #OrientedCobordismOverPoint}
###### Proposition

The cobordism ring over the point for [[orientation|oriented]] manifolds starts out as

| $k$             | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | $\geq 9$ |
|-----------------|---|---|---|---|---|---|---|---|---|---|
| $\Omega^{SO}_k$ | $\mathbb{Z}$ | 0 | 0 | 0 | $\mathbb{Z}$ | $\mathbb{Z}_2$ | 0 | 0 | $\mathbb{Z}\oplus \mathbb{Z}$ | $\neq 0$ |

=--

see e.g. ([ManifoldAtlas](#ManifoldAtlas))

+-- {: .num_prop}
###### Proposition

For $X$ a [[CW-complex]] (for instance a [[manifold]]), then  the oriented cobordism ring is expressed in terms of the [[ordinary homology]] $H_q(X,\Omega^{SO}_{p-q})$ of $X$ with [[coefficients]] in the cobordism ring over the point, prop. \ref{OrientedCobordismOverPoint}, as

$$
  \Omega_p^{SO}(X)
  =
  \oplus_{q = 0}^p
  H_q(X,\Omega_{p-q}^{SO})
  \;
  mod\; odd \; torsion
  \,.
$$

=--

e.g. [Connor-Floyd 62, theorem 14.2](#ConnorFloyd62)

## Related concepts

[[!include flavours of cobordism cohomology theories -- table]]


## References


Original articles:

* {#Thom54} [[René Thom]], _Quelques propri&#233;t&#233;s globales des vari&#233;t&#233;s diff&#233;rentiables_ Comment. Math. Helv. 28, (1954). 17-86 ([digiz:GDZPPN002056259](http://www.digizeitschriften.de/dms/img/?PID=GDZPPN002056259))

* {#Milnor60} [[John Milnor]], _On the cobordism ring &#173;$\Omega^\bullet$ and a complex analogue_, Amer. J. Math. 82 (1960), 505&#8211;521 ([jstor:2372970](https://www.jstor.org/stable/2372970))

* {#Novikov60} [[Sergei Novikov]], _Some problems in the topology of manifolds connected with the theory of Thom spaces_, Dokl. Akad. Nauk. SSSR. 132 (1960), 1031&#8211;1034 (Russian). 

* {#Novikov62} [[Sergei Novikov]], _Homotopy properties of Thom complexes_, Mat. Sbornik 57 (1962), no. 4, 407–442, 407&#8211;442 ([pdf](http://www.mi-ras.ru/~snovikov/6.pdf), [[NovikovThomComplexes.pdf:file]])


Textbook accounts:

* {#Stong68} [[Robert Stong]], _Notes on Cobordism theory_, Princeton University Press, 1968 ([toc pdf](http://pi.math.virginia.edu/StongConf/Stongbookcontents.pdf), [ISBN:9780691649016](http://press.princeton.edu/titles/6465.html), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/stongcob.pdf))

* {#Kochmann96} [[Stanley Kochmann]], section 1.5 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996


Lecture notes:

* {#Buchstaber} [[Victor Buchstaber]], _Geometric cobordism theory_ ([pdf](http://www.maths.manchester.ac.uk/~peter/MATH41101notes07.pdf))

* {#Francis} [[John Francis]] (notes by [[Owen Gwilliam]]), _[Topology of manifolds](http://math.northwestern.edu/~jnkf/classes/mflds/)_, _Lecture 2: Cobordism_ ([pdf](http://math.northwestern.edu/~jnkf/classes/mflds/2cobordism.pdf))

* [[Gerald Höhn]], _Komplexe elliptische Geschlechter und $S^1$-&#228;quivariante Kobordismustheorie_ (german) ([pdf](http://arxiv.org/PS_cache/math/pdf/0405/0405232v1.pdf))

* [[Sander Kupers]], _Oriented bordism: Calculation and application_ ([pdf](http://web.stanford.edu/~kupers/orientedbordism.pdf))

Details for [[framed cobordism]]:

* {#WangXu10} [[Guozhen Wang]], Zhouli Xu, section 2 of _A survey of computations of homotopy groups of Spheres and Cobordisms_, 2010 ([pdf](http://math.mit.edu/~guozhen/homotopy%20groups.pdf))

* {#Putnam} [[Andrew Putman]], _Homotopy groups of spheres and low-dimensional topology_ ([pdf](http://www.math.rice.edu/~andyp/notes/HomotopySpheresLowDimTop.pdf))

The relation to [[cohomotopy]] is made explicit in

* {#Kosinski93} [[Antoni Kosinski]], chapter IX of _Differential manifolds_, Academic Press 1993 ([pdf](http://www.maths.ed.ac.uk/~v1ranick/papers/kosinski.pdf))


Further discussion of oriented cobordism includes

* {#ManifoldAtlas} Manifold Atlas, _[Oriented bordism](http://www.map.mpim-bonn.mpg.de/Oriented_bordism)_

* {#ConnorFloyd62} P. E. Conner, E. E. Floyd, _Differentiable periodic maps_, Bull. Amer. Math. Soc. Volume 68, Number 2 (1962), 76-86. ([Euclid](http://projecteuclid.org/euclid.bams/1183524501), [pdf](http://www.maths.ed.ac.uk/~aar/papers/cf1.pdf))

A historical review in the context of [[complex cobordism cohomology theory]]/[[Brown-Peterson theory]] is in 

* [[Doug Ravenel]], chapter 4, section 2 of _[[Complex cobordism and stable homotopy groups of spheres]]_

On fibered cobordism groups:

* Astey, Greenberg, Micha, Pastor, _Some fibered cobordisms groups are not finitely generated_ ([pdf](http://www.ams.org/journals/proc/1988-104-01/S0002-9939-1988-0958093-3/S0002-9939-1988-0958093-3.pdf))


Discussion of the $G$-equivariant complex coborism ring includes

* G. Comezana and [[Peter May]], _A completion theorem in complex cobordism_, in Equivariant Homotopy and Cohomology Theory, CBMS Regional conference series in Mathematics, American Mathematical Society Publications, Volume 91, Providence, 1996.

* [[Igor Kriz]], _The $\mathbb{Z}/p$&#8211;equivariant complex cobordism ring_, from: "Homotopy invariant algebraic structures (Baltimore, MD, 1998)", Amer. Math. Soc. Providence, RI (1999) 217&#8211;223

* {#Strickland01} [[Neil Strickland]], _Complex cobordism of involutions_, Geom. Topol. 5 (2001) 335-345 ([arXiv:math/0105020](http://arxiv.org/abs/math/0105020))

* William Abrams, _Equivariant complex cobordism_, 2013 ([pdf](http://deepblue.lib.umich.edu/bitstream/handle/2027.42/99796/abramwc_1.pdf))

[[!redirects bordism ring]]

[[!redirects cobordism rings]]

[[!redirects cobordism group]]
[[!redirects cobordism groups]]

[[!redirects bordism ring]]
[[!redirects bordism rings]]
[[!redirects bordism group]]
[[!redirects bordism groups]]

