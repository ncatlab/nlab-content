
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

Now $E_{7(7)} \subset GL(56,\mathbb{R})$ is the [[subgroup]] of the [[general linear group]] acting on $W$ which preserves both the symplectic form $\omega$ as well as the quartic form $q$.

(e.g. [Pacheco-Waldram 08, B.1](#PachecoWaldram08))

## Properties

### Representation

#### $\mathbf{56}$ -- The smallest fundamental representation
 {#SmallestFundamentalRepresentation}

The smallest [[fundamental representation]] of $E_7$ is the defining one, of [[dimension]] $56$. Under the [[special linear group|special linear]] [[subgroup]] $SL(8,\mathbb{R}) \hookrightarrow E_7$ this decomposes as (e.g. [Cacciatori et al. 10, section 4](#CacciatoriEtAl10), also [Pacheco-Waldram 08, appendix B](#PachecoWaldram08))

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

* wikipedia, _[E7](http://en.wikipedia.org/wiki/E%E2%82%87)_

* {#CacciatoriEtAl10} Sergio L. Cacciatori, Francesco Dalla Piazza, Antonio Scotti, _E7 groups from octonionic magic square_ ([arXiv:1007.4758](http://arxiv.org/abs/1007.4758))

### In view of U-duality

The hidden [[E7]]-[[U-duality]] symmetry of the [[KK-compactification]] of [[11-dimensional supergravity]] on a 7-dimensional fiber to [[4d supergravity]] was first noticed in

* [[Eugene Cremmer]], [[Bernard Julia]], _The $SO(8)$ Supergravity_, Nucl. Phys. B 159 (1979) 141 ([spire](http://inspirehep.net/record/140465?ln=en)) 

and more generally in 

* [[Bernard de Wit]], [[Hermann Nicolai]], _D = 11 Supergravity With Local SU(8) Invariance_, Nucl. Phys. B 274, 363 (1986) ([spire](http://inspirehep.net/record/227409?ln=en)),  _Local SU(8) invariance in $d = 11$ supergravity_ ([spire](http://inspirehep.net/record/218601?ln=en))

The proposal to make this hidden $E_7$-symmetry manifest via [[exceptional generalized geometry]] is due to

* {#Hull07} [[Chris Hull]], _Generalised Geometry for M-Theory_, JHEP 0707:079 (2007) ([arXiv:hep-th/0701203](http://arxiv.org/abs/hep-th/0701203))

* {#PachecoWaldram08} Paulo Pires Pacheco, [[Daniel Waldram]], appendix B of _M-theory, exceptional generalised geometry and superpotentials_ ([arXiv:0804.1362](http://arxiv.org/abs/0804.1362))
   
Further discussion includes

* {#GLSW} [[Mariana Graña]], [[Jan Louis]], Aaron Sim, [[Daniel Waldram]], section 3.1 of  _$E_{7(7)}$ formulation of $N=2$ backgrounds_ ([arXiv:0904.2333](http://arxiv.org/abs/0904.2333))
 