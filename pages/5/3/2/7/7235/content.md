
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

One of the [[exceptional Lie groups]].

## Definition
 {#Definition}

Consider the [[vector space]]

$$
   W \coloneqq \wedge^2 \mathbb{R}^8 \oplus \wedge^2 (\mathbb{R}^8)^\ast
$$

of [[dimension]] $56$. This is naturally a [[symplectic vector space]] with [[symplectic form]] $\omega$ given by the natural pairing between [[linear 2-forms]] and [[bivectors]].

In addition, consider on this space the quartic form $q \colon W \to \mathbb{R}$ which sends an element $v = (\{v^{a b}, w_{a b}\}) \in W$ to 

$$
  q(v) 
   \coloneqq 
   v^{a b } w_{b c} v^{c d} w_{d a}
   - 
   \tfrac{1}{4} v^{a b} w_{a b} v^{c d} w_{c d}
   + 
   \tfrac{1}{96}
   \left(
     \epsilon_{a_1 a_2 a_3 a_4 a_5 a_6 a_7 a_8} 
     v^{a_1 a_2}  v^{a_3 a_4}  v^{a_5 a_6}  v^{a_7 a_8} 
     +
     \epsilon^{a_1 a_2 a_3 a_4 a_5 a_6 a_7 a_8} 
     w_{a_1 a_2}  w_{a_3 a_4}  w_{a_5 a_6}  w_{a_7 a_8} 
   \right)
  \,.
$$

Now $E_{7(7)} \subset GL(56,\mathbb{R})$ is the [[subgroup]] of the [[general linear group]] acting on $W$ which preserves both the symplectic form $\omega$ as well as the quartic form $q$. See also [below](#SmallestFundamentalRepresentation).

This presentation is due to [Cartan](#Cartan), for review see [Cremmer-Julia 79, appendix B](#CremmerJulia79), [Pacheco-Waldram 08, B.1](#PachecoWaldram08). A construction via [[octonions]] is due to ([Freudenthal 54](#Freudenthal54)),  one via [[quaternions]] is due to ([Wilson 2014](#Wilson14)).



## Properties

### As part of the ADE pattern

[[!include ADE -- table]]


### Representation

#### $\mathbf{56}$ -- The smallest fundamental representation
 {#SmallestFundamentalRepresentation}

The smallest [[fundamental representation]] of $E_7$ is the defining one (from the definition [above](#Definition)), of [[dimension]] $56$. Under the [[special linear group|special linear]] [[subgroup]] $SL(8,\mathbb{R}) \hookrightarrow E_7$ this decomposes as (e.g. [Cacciatori et al. 10, section 4](#CacciatoriEtAl10), also [Pacheco-Waldram 08, appendix B](#PachecoWaldram08))

$$
  \mathbf{56} 
    \simeq 
  \mathbf{28} \oplus \mathbf{28}^\ast 
    \simeq 
   \wedge^2 \mathbb{R}^8 \oplus \wedge^2 (\mathbb{R}^8)^\ast
  \,.
$$

Under the further subgroup inclusion $SL(7,\mathbb{R}) \hookrightarrow SL(8,\mathbb{R}) \hookrightarrow E_7$ this decomposes further as

$$
  \mathbf{56}
    \simeq
  \underset{\simeq \wedge^2 \mathbb{R}^8}{\underbrace{\mathbb{R}^7 \oplus \wedge^2 (\mathbb{R}^7)^\ast}} 
   \oplus 
  \underset{\simeq \wedge^2 (\mathbb{R}^8)^\ast}{\underbrace{\wedge^5 (\mathbb{R}^7)^\ast \oplus \wedge^6 \mathbb{R}^7}}
  \,,
$$

where $\wedge^2 (\mathbb{R}^7) \subset \wedge^2 (\mathbb{R}^8)^\ast$ is regarded as the subspace of 2-forms with vanishing 8-components, and where  $\wedge^6 \mathbb{R}^7$ is the [[Poincaré duality|Poincaré dual]] to the complementary subspace of $\wedge^2 (\mathbb{R}^8^\ast)$ of 2-forms with non-trivial 8-component.

This is due to [Cartan](#Cartan), for review see [Cremmer-Julia 79, appendix B](#CremmerJulia79) [Pacheco-Waldram 08, B.1](#PachecoWaldram08).


#### $\mathbf{133}$ -- The adjoint representation
 {#AdjointRepresentation}

The [[adjoint representation]] $\mathbf{133}$ of $E_7$ decomposes under $SL(8,\mathbb{R})$ as ([Pacheco-Waldram 08 (B.7)](#PachecoWaldram08))

$$
  \mathfrak{e}_7
  =
  \mathbf{133}
  \simeq
  (\mathbb{R}^8 \otimes (\mathbb{R}^8)^\ast)_{traceless}
  \oplus
  \wedge^4 (\mathbb{R}^8)^\ast
  \,.
$$

In this decomposition the subspace corresponding to the subalgebra $\mathfrak{su}(8) \hookrightarrow \mathfrak{e}_8$ is the vector space

$$
  \mathfrak{su}(8)
  \simeq
  \mathfrak{so}(8)
  \oplus
  (\wedge^4 (\mathbb{R}^8)^\ast)_-
  \,,
$$

where the first summand denotes the skew-symmetric matrices, and the second summand the [[Hodge duality|Hodge anti-self dual]] 4-forms ([Pacheco-Waldram 08 (B.29) (B.30) and below (2.34)](#PachecoWaldram08)).


Under $GL(7,\mathbb{R}) \hookrightarrow SL(8,\mathbb{R})$ the full adjoint representation decomposes further into ([Pacheco-Waldram 08 (B.21)](#PachecoWaldram08))

$$
  \mathbf{133}
  \simeq
  \left(\mathbb{R}^7 \otimes (\mathbb{R}^7)^\ast\right)
  \oplus 
  \left(\wedge^6 \mathbb{R}^7 \oplus \wedge^6 (\mathbb{R}^7)^\ast\right)
  \oplus
  \left(
     \wedge^3 \mathbb{R}^7 \oplus \wedge^3 (\mathbb{R}^7)^\ast
  \right)
  \,.
$$

Here $\wedge^6 (\mathbb{R}^7)^\ast \simeq \mathbb{R}^7$ is the $(-,8)$-component of $\mathbb{R}^7 \oplus (\mathbb{R}^7)^\ast$ and dually, while the $(8,8)$-component carries no information by tracelessness; and $\wedge^3 (\mathbb{R}^7)^\ast$ is the $(-,-,-,8)$-component of $\wedge^4 (\mathbb{R}^8)^\ast$, while $\wedge^3 \mathbb{R}^7$ is the 7-dimensional [[Poincaré duality|Poincaré dual]] of the complement of the $(-,-,-,8)$-component ([Pacheco-Waldram 08 (B.22)](#PachecoWaldram08)).


Taken together this means that under $GL(7,\mathbb{R})$ the subspace $\mathbb{su}(8) \hookrightarrow \mathfrak{e}_8$ is that spanned by

1. $\mathfrak{so}(7)$-elements;

1. sums of a 3-form with its 8d-Hodge+7d-Poincar&#233;-dual 3-vector;

1. sums of a 6-form with its dual 6-vector

hence is

$$
  \mathfrak{su}(8) 
  \simeq
  \mathfrak{so}(8) \oplus \wedge^3 \mathbb{R}^7 \oplus \wedge^6 \mathbb{R}^7
  \,.
$$

Hence the [[tangent space]] to the [[coset]] $E_{7(7)}/(SU(8)/\mathbb{Z}_2)$ may be identified as

$$
  \mathfrak{e}_7/\mathfrak{su}(8)
  \simeq
  \odot^2 (\mathbb{R}^7)^\ast  
  \oplus
  \wedge^3 (\mathbb{R}^7)^\ast
  \oplus
  \wedge^6 (\mathbb{R}^7)^\ast
  \,.
$$




### As U-Duality group of 4d SuGra
 {#AsUDualityGroup}

$E_{7(7)}$ is the [[U-duality]] group (see there) of [[11-dimensional supergravity]] [[KK-compactification|compactified]] on a 7-dimensional fiber to [[4-dimensional supergravity]] (e.g. [[M-theory on G2-manifolds]]).

Specifically, ([Hull 07, section 4.4](#Hull07), [Pacheco-Waldram 08, section 2.2](#PachecoWaldram08)) identifies the [[vector space]] underlying the $SL(7,\mathbb{R})$-decomposition of the [smallest fundamental representation](#SmallestFundamentalRepresentation) 

$$
  \mathbf{56}
  \simeq
  \mathbb{R}^7 \oplus \wedge^2 (\mathbb{R}^7)^\ast \oplus \wedge^5 (\mathbb{R}^7)^\ast \oplus \wedge^6 \mathbb{R}^7
  \,.
$$

as the [[exceptional tangent bundle]]-structure to the 7-dimensional fiber space which one obtains as discussed at _[M-theory supersymmetry algebra -- As an 11-dimensional boundary condition](M-theory+supersymmetry+algebra#AsAn11DimensionalBoundaryCondition)_. Here $\mathbb{R}^7$ is the ordinary [[tangent space]] itself, $\wedge^2 (\mathbb{R}^\ast)^7$ is interpreted as the local incarnation of the possible [[M2-brane]] [[charges]], $\wedge^5 (\mathbb{R}^\ast)^7$ the [[M5-brane]] charges and $\wedge^6 \mathbb{R}^7$ as the charges of [[Kaluza-Klein monopoles]].

[[!include U-duality -- table]]

## Related concepts

* [[exceptional geometry]], [[exceptional generalized geometry]]

* [[G2]], [[F4]],

  [[E6]], **E7**,  [[E8]], [[E9]], [[E10]], [[E11]], $\cdots$


## References

### General

The description of the defining fundamental $\mathbf{56}$-representation of $E_{7(7)}$ is due to

* {#Cartan} [[Eli Cartan]], Thesis, in Oeuvres compl&#232;tes T1, Part I, Gauthier-Villars, Paris 1952

and recalled for instance in 

* {#CremmerJulia79} [[Eugene Cremmer]], [[Bernard Julia]], appendix B of _The $SO(8)$ Supergravity_, Nucl. Phys. B 159 (1979) 141 ([spire](http://inspirehep.net/record/140465?ln=en)) 

See also

* Robert B. Brown, _Groups of type $E _7$_, Jour. Reine Angew. Math. 236 (1969), 79-102.

A construction via the [[octonions]] is due to

* {#Freudenthal54} [[Hans Freudenthal]], _Beziehungen der $\mathfrak{e}_7$ und $\mathfrak{e}_8$ zur Oktavenebene_, I, II, Indag. Math. 16 (1954), 218&#8211;230, 363&#8211;368. III, IV, Indag. Math. 17 (1955), 151&#8211;157, 277&#8211;285. V &#8212; IX, Indag. Math. 21 (1959), 165&#8211;201, 447&#8211;474. X, XI, Indag. Math. 25 (1963) 457&#8211;487 ([dspace](http://dspace.library.uu.nl/handle/1874/7436))

reviewed in 

* [[John Baez]], section 4.5 _[E7](http://math.ucr.edu/home/baez/octonions/node18.html)_ of _The Octonions_ ([arXiv:math/0105155](http://arxiv.org/abs/math/0105155))

* {#CacciatoriEtAl10} Sergio L. Cacciatori, Francesco Dalla Piazza, Antonio Scotti, _E7 groups from octonionic magic square_ ([arXiv:1007.4758](http://arxiv.org/abs/1007.4758))

A [[quaternion|quaternionic]] construction is given in 

* {#Wilson14} [[Robert Wilson]], _A quaternionic approach to $E_7$_, Proc. Amer. Math. Soc. 142 (2014), 867-880. doi:[10.1090/S0002-9939-2013-11838-1](http://dx.doi.org/10.1090/S0002-9939-2013-11838-1), ([pre-publication version](http://www.maths.qmul.ac.uk/~raw/pubs_files/E7quat2.pdf)), ([talk notes](http://www.maths.qmul.ac.uk/~raw/talks_files/E7quattalk2.pdf)).


See also

* wikipedia, _[E7](http://en.wikipedia.org/wiki/E%E2%82%87)_




### In view of U-duality

The hidden [[E7]]-[[U-duality]] symmetry of the [[KK-compactification]] of [[11-dimensional supergravity]] on a 7-dimensional fiber to [[4d supergravity]] was first noticed in ([Cremmer-Julia 79](#CremmerJulia79)) and then expanded on in

* [[Bernard de Wit]], [[Hermann Nicolai]], _D = 11 Supergravity With Local SU(8) Invariance_, Nucl. Phys. B 274, 363 (1986) ([spire](http://inspirehep.net/record/227409?ln=en)),  _Local SU(8) invariance in $d = 11$ supergravity_ ([spire](http://inspirehep.net/record/218601?ln=en))

The proposal to make this hidden $E_7$-symmetry manifest via [[exceptional generalized geometry]] is due to

* {#Hull07} [[Chris Hull]], _Generalised Geometry for M-Theory_, JHEP 0707:079 (2007) ([arXiv:hep-th/0701203](http://arxiv.org/abs/hep-th/0701203))

* {#PachecoWaldram08} Paulo Pires Pacheco, [[Daniel Waldram]], appendix B of _M-theory, exceptional generalised geometry and superpotentials_ ([arXiv:0804.1362](http://arxiv.org/abs/0804.1362))
   
Further discussion includes

* {#GLSW} [[Mariana Graña]], [[Jan Louis]], Aaron Sim, [[Daniel Waldram]], section 3.1 of  _$E_{7(7)}$ formulation of $N=2$ backgrounds_ ([arXiv:0904.2333](http://arxiv.org/abs/0904.2333))



 