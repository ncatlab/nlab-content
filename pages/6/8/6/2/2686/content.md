
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A [[Poisson manifold]] may be thought of as a [[Poisson Lie algebroid]], a [[Lie algebroid]] with extra structure: called an [[n-symplectic manifold]] for $n = 1$.

By [[Lie integration]] this Lie algebroid should integrate to a [[Lie groupoid]] with extra structure. Symplectic groupoids are supposed to be those objects that integrate [[n-symplectic manifold]] aka [[Poisson manifold]]s in this sense.

The [[category algebra|groupoid algebra]] of these symplectic groupoids are [[C-star algebra]]s that may be regarded as the [[quantization]] of the original [[Poisson manifold]]. This is described in the references below.

## Definition
 {#Definition}

The original definition of [Weinstein 1987](#Weinstein87) is this:

+-- {: .num_defn #WeinsteinsDefintion}
###### Definition

A **symplectic Lie groupoid** is a [[Lie groupoid]] $\mathbf{X}_\bullet$ whose manifold of [[morphisms]] $\mathbf{X}_1$ is equipped with a [[symplectic manifold|symplectic structure]] whose symplectic form $\omega \in \Omega^2_{closed}(\mathbf{X}_1)$ is _multiplicative_ in that the alternating sum of its canonical [[pullback of a differential form|pullbacks]] to the space $\mathbf{X}_2$ of composable morphisms vanishes:

$$
 0 = 
  \delta \omega = pr_1^* \omega - compose^* \omega 
  + pr_2^* \omega
  \,.
$$

=--

+-- {: .num_remark }
###### Remark

The manifold of [[objects]] $\mathbf{X}_0$ of a symplectic Lie groupoid $\mathbf{X}_\bullet$, def. \ref{WeinsteinsDefintion}, carries the structure of a [[Poisson manifold]] which is unique, up to [[isomorphism]], with the property that the target map $t \colon \mathbf{X}_1 \to \mathbf{X}_0$ is a [[homomorphism]] of [[Poisson manifolds]] (canonically regarding the [[symplectic manifold]] $(\mathbf{X}_1, \omega)$ as a Poisson manifold).

The [[Poisson manifolds]] that arise this way as $\mathbf{X}_0$ of a symplectic Lie groupoid are called **integrable Poisson manifolds**.

=--

+-- {: .num_remark }
###### Remark

Reformulated more abstractly, def. \ref{WeinsteinsDefintion} says that the differential form $\omega$, when extended to a triple

$$
  (0, \omega, 0)
  \in
  \oplus_{k = 0,1,2} \Omega^{3-k}(\mathbf{X}_{k})
$$

is a [[cocycle]] of degree 3 in the [[de Rham complex]] of $\mathbf{X}$, identified with the [[simplicial de Rham complex]] of the [[nerve]] $X_\bullet$ of $X$.

=--

This observation leads to the following generalization

+-- {: .num_defn }
###### Definition

A **pre-quasi symplectic groupoid** is a [[Lie groupoid]] $\mathbf{X}$ equipped with a [[differential 2-form]] $\omega_2 \in \Omega^2(\mathbf{X}_1)$ and a differential 3-form $\omega_3 \in \Omega^3(\mathbf{X}_0)$ such that 

$$
  (0, \omega_2, \omega_3) \in \oplus_{k = 0,1,2} \Omega^{3-k}(\mathbf{X}_{k})
$$

is a [[cocycle]] in the [[simplicial de Rham complex]] of $\mathbf{X}_\bullet$, hence such that 

$$
  \delta \omega_2 = 0
$$

$$
  d\omega_2 + \delta \omega_3 = 0
  \,,
$$

where $\delta = \sum_{k} (-1)^k \partial_k^*$ is the alternating sum of the [[pullback of a differential form|pullbacks]] along the face maps of the [[nerve]] $\mathbf{X}_\bullet$.

=--

This appears as ([Xu, def. 2.1](#Xu), [LG-Xu, def. 2.1](#LGX)). This structure is called a **twisted presymplectic groupoid** in ([BCWZ, def. 2.1](#BCWZ)).

+-- {: .num_remark }
###### Remark

Since therefore a (pre-)symplectic groupoid is really a Lie groupoid equipped with a cocycle in degree-3 [[de Rham cohomology]] (instead of degree 2 as for a symplectic manifold),  it is really rather an object in [[2-plectic geometry]].

=--

## Properties 

### Lie integration and Poisson manifolds

Every [[Lie groupoid]] [[Lie integration|integrating]] a [[Poisson Lie algebroid]] is naturally a symplectic Lie groupoid. Picking always the unique source-simply connected integrating [[Lie groupoid]] produces a [[functor]]

$$
  \Sigma : PoissonManifolds \to SymplecticGroupoids
  \,.
$$

When the [[Poisson manifold]] we start with happens to be a [[symplectic manifold]], then its symplectic Lie groupoid is always the [[fundamental groupoid]] of $X$:

$$
  (X,\pi)\;\; symplectic
  \;\;\Rightarrow\;\;
  \Sigma(X,\pi) \simeq_{iso} \Pi(X)
  \,.
$$

When $X$ is [[simply connected topological space|simply connected]] such that $\Pi(X)$ is the [[codiscrete category|codiscrete groupoid]] $Pair(X)$ we have that the symplectic form on $Mor(\Pi(X)) = X \times X$ is $\omega \otimes (-\omega)$, for $\omega$ the [[symplectic manifold|symplectic form]] on $X$.

Conversely, for every symplectic groupoid $\mathbf{X}$ there is a unique [[Poisson manifold]] structure on its manifold $\mathbf{X}_0$ of objects such that the [[codomain]] map $t \colon \mathbf{X}_1 \to \mathbf{X}_0$ is a [[homomorphism]] of [[Poisson manifolds]]. (For instance [Racaniere, theorem 6.3](#Racaniere)) One says also that $\mathbf{X}$ **integrates the Poisson manifold** $\mathbf{X}_0$.

### Symplectic realization

The source map of a symplectic groupoid over a Poisson manifold constitutes a _[[symplectic realization]]_ of this Poisson manifold, hence its canonical desingularization via [[Lie integration]]. See at _[[symplectic realization]]_ for more. 


### In geometric quantization of Poisson manifolds 

In the _groupoid approach to quantization_  symplectic groupoids are used to discuss [[geometric quantization]] not just of [[symplectic manifold]]s but more generally of [[Poisson manifold]]s.

See [[geometric quantization of symplectic groupoids]].

### As Lie integration of Poisson Lie algebroid

(...)

### A reduced phase space of open Poisson sigma-model

The symplectic groupoid of a Poisson manifold is also the 
[[reduced phase space]] of the open sector of the 
corresponding [[Poisson sigma-model]]. ([Cattaneo-Felder 01](#CattaneoFelder01))

## Examples

### Of Lie-Poisson structure
 {#OfLiePoissonStructure}

+-- {: .num_example}
###### Example

Let $G$ be a [[Lie group]] with [[Lie algebra]] $\mathfrak{g}$ and consider the [[dual vector space]] $\mathfrak{g}^*$ equipped with its
[[Lie-Poisson structure]]. Then the [[action groupoid]] $\mathfrak{g}^* \sslash G$ of the [[coadjoint action]] carries a multiplicative symplectic form $\omega$ induced by the identification of the manifold of [[morphisms]] with the [[cotangent bundle]] of the group, $G \times \mathfrak{g}^* \simeq T^* G$, induced by right translation from the [[Poincare form]] on the [[cotangent bundle]]. This makes $(\mathfrak{g}^* //G, \omega)$ a symplectic groupoid which [[Lie integration|Lie integrates]] the [[Lie-Poisson structure]] on $\mathfrak{g}^*$. 

=--

This seems to be due to [Weinstein 1991, ex. 3.2](#Weinstein91), see [Bursztyn & Crainic 2005, ex. 4.3](#BursztynCrainic), [Nuiten 2013, p. 111](#Nuiten13).


## Related concepts

* [[symplectic manifold]]

* [[symplectic Lie n-algebroid]]

* [[symplectic infinity-groupoid]]

[[!include infinity-CS theory for binary non-degenerate invariant polynomial - table]]


## References

The notion of symplectic groupoids was apparently proposed independently by Karas&#235;v, [[Alan Weinstein|Weinstein]], and Zakrzewski, all motiviated from the problem of [[quantization]].

* {#Weinstein87} [[Alan Weinstein]], _Symplectic groupoids and Poisson manifolds_, Bull. Amer. Math. Soc. (N.S.) **16** (1987) 101-104 &lbrack;[euclid:bams/1183553676](https://projecteuclid.org/journals/bulletin-of-the-american-mathematical-society-new-series/volume-16/issue-1/Symplectic-groupoids-and-Poisson-manifolds/bams/1183553676.full)&rbrack;

* [[Alan Weinstein]], _Symplectic groupoids, geometric quantization, and irrational rotation algebras_, in:
_Symplectic geometry, groupoids, and integrable systems_ (Berkeley, CA, 1989), Springer (1991) 281-290 &lbrack;[doi:10.1007/978-1-4613-9719-9_19](https://doi.org/10.1007/978-1-4613-9719-9_19), MR1104934&rbrack;

* [[Alan Weinstein]], _Tangential deformation quantization and polarized symplectic groupoids_, in: _Deformation theory and symplectic geometry_ (Ascona, 1996), 301-314, Kluwer (1997) &lbrack;[ISBN:9780792345251](https://link.springer.com/book/9780792345251), [MR1480730](http://www.ams.org/mathscinet-getitem?mr=1480730)&rbrack;

* M. V. Karas\"ev, _The Maslov quantization conditions in higher cohomology and analogs of notions developed in Lie theory for canonical fibre bundles of symplectic manifolds II_, Selecta Mathematica Sovietica 8, pp. 235&#8211;257, 1989.

* S. Zakrzewski, Quantum and classical pseudogroups I, II, Commun. Math. Phys. 134 (1990)

See also the references at _[[geometric quantization of symplectic groupoids]]_ .

Lecture notes include

* {#Racaniere} S&#233;bastien Racani&#232;re, _Lie algebroids, Lie groupoids and Poisson geometry_ ([pdf](http://empg.maths.ed.ac.uk/Activities/GCY/Racaniere.pdf))
 

The notion of pre-quasi-symplectic groupoids is introduced and the intepretation of symplectic groupoids in [[higher geometry]] is made fairly explicit in 

* {#Xu} [[Ping Xu]], _Momentum Maps and Morita Equivalence_, J. Diff. Geom ([arXiv:math/0307319](http://arxiv.org/abs/math/0307319))
 

* {#LGX} [[Camille Laurent-Gengoux]], [[Ping Xu]], _Quantization of pre-quasi-symplectic groupoids and their Hamiltonian spaces_ in _The Breadth of Symplectic and Poisson Geometry_, Progress in Mathematics **232** (2005)  423-454 &lbrack;[arXiv:math/0311154](http://arxiv.org/abs/math/0311154), [doi:10.1007/0-8176-4419-9_14](https://doi.org/10.1007/0-8176-4419-9_14)&rbrack; 
 


These "pre-quasi-symplectic groupoids" had been called "twisted presymplectic groupoids" in 

* {#BCWZ} [[Henrique Bursztyn]], [[Marius Crainic]], [[Alan Weinstein]], [[Chenchang Zhu]], _Integration of twisted Dirac brackets_ ([arXiv:math/0303180](http://arxiv.org/abs/math/0303180))
 


The identification with reduced phase spaces of the open Poisson sigma-model is in 

* {#CattaneoFelder01} [[Alberto Cattaneo]], [[Giovanni Felder]], _Poisson sigma models and symplectic groupoids_, in _Quantization of Singular Symplectic Quotients_, (ed. [[Klaas Landsman]], M. Pflaum, M. Schlichenmeier), Progress in Mathematics 198 (Birkh&#228;user,
2001), 61&#8211;93. ([arXiv:math/0003023](http://arxiv.org/abs/math/0003023))
 

Further developments:

* {#Weinstein91} [[Alan Weinstein]], *Noncommutative geometry and geometric quantization*, in P. Donato et al. (eds.) _Symplectic geometry and Mathematical physics_, Progr. Math **99** Birkh&#228;user (1991) 446-461.  [doi:10.1007/978-1-4757-2140-9_23](https://doi.org/10.1007/978-1-4757-2140-9_23).

* [[Ping Xu]], _Morita equivalence and symplectic realizations of Poisson manifolds_, Annales scientifiques de l'&#201;cole Normale Sup&#233;rieure, S&#233;r. 4, 25 no. 3 (1992) ([NUMDAM](http://www.numdam.org/item?id=ASENS_1992_4_25_3_307_0))

* {#BursztynCrainic} [[Henrique Bursztyn]], [[Marius Crainic]], *Dirac structures, momentum maps and quasi-Poisson manifolds*, in: *The Breadth of Symplectic and Poisson Geometry*, Progress in Mathematics **232**,  Birkhäuser (2005) 1-40 &lbrack;[doi:10.1007/0-8176-4419-9_1](https://doi.org/10.1007/0-8176-4419-9_1)&rbrack;
 
* F. Bonechi, N. Ciccoli, N. Staffolani, M. Tarlini, _The quantization of the symplectic groupoid of the standard Podles sphere_ ([arXiv:1004.3163](http://arxiv.org/abs/1004.3163))

* {#Nuiten13} [[Joost Nuiten]], pp. 108 in: *[[schreiber:master thesis Nuiten|Cohomological quantization of local prequantum boundary field theory]]*, MSc thesis, Utrecht (August 2013) &lbrack;[pdf](/schreiber/files/thesisNuiten.pdf), [dspace:1874/282756](https://dspace.library.uu.nl/handle/1874/282756), [talk slides](/schreiber/files/thesisNuitenTalk.pdf)&rbrack;

The [[formal groupoid]] version of symplectic groupoids is discussed in

* [[Alberto S. Cattaneo|Alberto Cattaneo]], Benoit Dherin, [[Giovanni Felder]], _Formal symplectic groupoid_, Comm. Math. Phys. __253__ (2005), no. 3, 645&#8211;674 [math.SG/0312380](http://arxiv.org/abs/math/0312380) [doi](HTTP://dx.doi.org/10.1007/s00220-004-1199-z){#CattaneoDherinFelder}; _Formal Lagrangian operad_, [math.SG/0505051](http://arxiv.org/abs/math/0505051)

[[!redirects symplectic Lie groupoid]]
[[!redirects symplectic groupoids]]
[[!redirects symplectic Lie groupoids]]