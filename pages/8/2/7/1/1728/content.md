
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Functorial quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A ([[prequantum field theory|pre]]-)[[quantum field theory|quantum]] [[field theory]] _with defects_ is, roughly a [[field theory]] that assigns data not just to plain [[manifolds]]/[[cobordisms]], but to spaces that may carry certain singularities and/or colorings. At the locus of such a singularity the [[bulk]] field theory may then undergo transitions.

Such defects are known by many names. In [[codimension]] 1 they are often called [[domain walls]]. If they are [[boundaries]] they are often called _[[branes]]_, the corresponding domain walls are then sometimes called [[bi-branes]]. Examples of Dimension-1 defects are [[Wilson lines]] and [[cosmic strings]] (at least in [[gauge theory]]) and dimension-0 defects are often called [[monopoles]].

## Definition

### General
 {#DefinitionGeneral}

A plain $n$-dimensional local [[FQFT]] (a [[bulk]] field theory) is a [[monoidal (∞,n)-functor|symmetric monoidal]] [[(∞,n)-functor]] from the [[(∞,n)-category of cobordisms]]. 

$$  
  Z : Bord_n \to \mathcal{C}^\otimes
  \,.
$$

If one replaces plain [[cobordisms]] here with cobordisms $Bord_n^{Def}$ "with singularities" including [[boundaries]] and [[corners]] but also partitions labeled in a certain index set $Def$, one calls a morphism

$$
  Z : Bord_n^{Def} \to \mathcal{C}
$$

a TQFT _with defects_. A general formalization is in ([Lurie 09, section 4.3](#Lurie09)), see at _[Cobordism theorem -- For cobordisms with singuarities (boundaries/branes and defects/domain walls)](cobordism+hypothesis#ForCobordismsWithSingularities)_. See also ([Davydov, Runkel & Kong 2011](#DavydovRunkelKong11) and [Carqueville-Runkel-Schaumann](#CarquevilleRunkelSchaumann)).

Such a morphism carries data as follows:

* for each label in $Def$ of codimension 0 there is an ordinary [[bulk]] field theory;

* for each label in $Def$ of codimension 1 data on how to "connect" the two TQFTs on both sides

* etc.

So one may think of the codimension $k$ colors as _defects_ where the TQFT that one is looking at changes its nature.

In particular, when the QFT on one side of the defect is trivial, then the defect behaves like a _boundary condition_ for the remaining QFT. Since at least for $n=2$ QFT such boundary conditions are also called _[[branes]]_, defects are also called _[[bi-branes]]_.

The statement of the **cobordism theorem with singularities** ([Lurie 09, theorem 4.3.11](#Lurie09)) is essentially the following: 

Given a [[symmetric monoidal (∞,n)-category]] $\mathcal{C}^\otimes$, then for every choice of [[pasting diagram]] of [[k-morphisms]] for all $k$, there is a type of manifolds with singularity $Def$, such that $Bord_n^Def$ is the free symmetric monoidal $(\infty,n)$-category on this data, hence such that TFTs with defects $(Bord_n^Def)^\otimes \to \mathcal{C}^\otimes$ are equivalently given by realizing such a pasting diagram in $\mathcal{C}$, where each of the given [[k-morphism]] appears as the value of a codimension $(n-k)$-defect. (See also [Lurie 09, remark 4.3.14](#Lurie09)).


### Topological defects from spontaneously broken symmetry
 {#DefectsFromBrokenSymmetry}

An old notion of _[[defects]]_ in field theory -- well preceding the [above](#DefinitionGeneral) general notion in the context of [[FQFT]] -- is that of **[[topological defects]] in the [[vacuum]] structure of [[gauge theories]] that exhibit [[spontaneous symmetry breaking]] (such as a [[Higgs mechanism]]).

A comprehensive review is [Vilenkin & Shellard 1994](#VilenkinShellard94). Steps towards conceptually systematizing these broken-symmetry defects and their interaction are made by  [Preskill & Vilenkin 1992](#PreskillVilenkin92). We now discuss how this may be translated to and formalized in the general [[FQFT]] definition [above](#DefinitionGeneral) along the lines of [Fiorenza & Valentino](#FiorenzaValentino) and [FSS](#FSS).

\linebreak

Let $G$ be a [[Lie group]], to be thought of as the (local or global) [[gauge group]] of some [[gauge theory]]. Let $H \hookrightarrow G$ a [[subgroup]], to be thought of as the [[subgroup]] of global symmetries preserved by some [[vacuum]] configuration (which "[[spontaneous symmetry breaking|spontaneously breaks]]" the symmetry from $G$ to $H$, the archetypical example is the [[Higgs mechanism]]). 

Then the space of such vacuum configurations is the [[coset]] space $G/H$. So given a [[manifold]] $X$ ([[spacetime]]), [[vacuum]] configuratons are given by [[functions]] $X \to G/H$. Hence $G/H_1$ is the "[[moduli space]] of vacua" or "vacuum space" in this context.

The functions $X \to G/H$ are to be [[smooth functions]] in the [[bulk]] of spacetime. If they are allowed to be non-smooth or even non-[[continuous function|continuous]] along given strata of $X$, then these are called **defects** in the sense of broken gauge symmetry.

In particular (with counting adapted to $dim X = 4$)

* if $X \to G/H$ is not smooth but is smooth on the pre-image of each element of $\pi_0(G/H)$ and becomes a smooth function on $X-S_1$ where $S_1 \hookrightarrow X$ is a [[codimension]]-1 [[submanifold]], then $S_1$ is said to be a [[domain wall]] for vacuum configurations.

* if $X \to G/H$ is not smooth but becomes smooth on $X-S_2$, where $S_2$ is a codimension-2 submanifold, then $S_2$ is calld a [[cosmic string]]-defect of the vacuum configurations;

* if $X \to G/H$ is not smooth but becomes smooth on $X-S_3$, where $S_3$ is a codimension-3 submanifold, then $S_3$ is calld a [[monopole]]-defect of the vacuum configurations.

> hm, need to fine-tune the technical conditions here, to make the following statement come out right...


So 

* [[domain walls]] can appear when $\pi_0(G/H)$ is non-trivial;

* [[cosmic strings]] can appear when $\pi_1(G/H)$ is non-trivial;

* [[monopoles]] can appear when $\pi_2(G/H)$ is non-trivial.


Next consider a sequence of [[subgroups]]

$$
  H_2 \hookrightarrow H_1 \hookrightarrow H_0 \coloneqq G
$$

to be thought of as coming from two consecutive steps of [[spontaneous symmetry breaking]], the first one down to $H_1$ at some [[energy]]-scale $E_1$, and the second at some lower energy scale $E_2 \lt E_1$.

Then we say that vacuum defects at energy $E_2$ of codimension-$k$ which wind around an element $\pi_k(H_1/H_2)$ are **metastable** if they become unstable at energy $E_1$, hence if their image in $\pi_k(H_0/H_2)$ is trivial.

So if we add to the singular cobordism category the $k$-morphism which is the $k$-dimenional unit cube with an open $k$-[[ball]] removed, then the boundary field data for metastable codimension $n-k$-defects is


$$
  \array{
     [0,1]^k - D^k &\to & \Pi(H_1/H_2)
     \\
     \downarrow &\swArrow& \downarrow
     \\
     [0,1]^k &\to& \Pi(H_0/H_2) &\to& \Pi(H_0/H_1)
  }
$$

we have a [[homotopy fiber sequence]]

$$
  \Pi(H_1/H_2) \to \Pi(H_0/H_2) \to \Pi(H_0/H_1)
  \,.
$$

This induces a [[long exact sequence of homotopy groups]]

$$
   \cdots \to \pi_{k+1}(H_0/H_1) \to \pi_k(H_1/H_2) \to \pi_k(H_0/H_2) \to \pi_k(H_0/H_1)
  \to 
  \pi_{k-1}(H_1/H_2) \to \cdots
  \,.
$$

So for every metastable defect of codimension $n-k$ given by $c \in ker(\pi_k(H_1/H_2) \to \pi_k(H_0/H_2))$ there is an element in $\pi_{k+1}(H_0/H_1)$ of one codimension higher. One says ([Preskill & Vilenkin 1992](#PreskillVilenkin92)) that the codimenion $(n-k)$-defect may end on that codimension $(n-k-1)$-defect.

(...)

In order to formalize this we introduce, following the [[cobordism theorem]] with singularities, cells in $Span_n(\mathbf{H})$ which label spontaneous-symmetriy-breaking defects as well as their defects-of-defects which exhibit their decay by higher codimension defects.

Consider a span of the form

$$
  \array{
    [\Pi(S^{k-1}), \Pi(H_1/H_2)]
    &\leftarrow&
    [\Pi(S^{k-1}), \Pi(H_1/H_2)]
    &\rightarrow&  
    \ast
  }
  \,.
$$

Comparing this to the span that comes from the "cap" $S^{k-1} \to D^{k} \leftarrow \emptyset$ in the theory at energy level $E_2$, which is just 

$$
  \array{
    [\Pi(S^{k-1}), \Pi(H_1/H_2)]
    &\leftarrow&
    [\Pi(D^{k}), \Pi(H_1/H_2)]
    &\rightarrow&  
    \ast
  }
$$

shows that the former models a $k$-disk which is not filled with spacetime, but nevertheless closes the disk. This is the defect given as a removal of a piece of spacetime.

In order to formalize how these defects may decay at higher energy, consider next  a [[span]] of [[field (physics)|field]] configurations of the form

$$
  \array{
    [\Pi(S^{k-1}), \Pi(H_1/H_2)]
    &\leftarrow&
    [\Pi(S^{k}), \Pi(H_0/H_1)]
    &\rightarrow&  
    [\ast, \Pi(H_0/H_2)]
  }
  \,.
$$

Comparing again to the span that comes from the "cap" $S^{k-1} \to D^{k} \leftarrow \emptyset$ in the theory at energy level $E_2$, which is just 

$$
  \array{
    [\Pi(S^{k-1}), \Pi(H_1/H_2)]
    &\leftarrow&
    [\Pi(D^{k}), \Pi(H_1/H_2)]
    &\rightarrow&  
    \ast
  }
$$

shows that the former models a $k$-disk whose center point carries a singularity: the fields at the bounding $S^{k-1}$ take values in the moduli space of the ambient theory $\Pi(H_1/H_2)$, but then at the tip of the "cap" there is a "field insertion" of a field with values in $\Pi(H_0/H_2)$. Hence this labels a defect of codimension $k$.

To construct such a decay-process span that captures the above story from [Preskill & Vilenkin 1992](#PreskillVilenkin92), consider the following diagram:

$$
  \array{
     && [\Pi(S^{k}), \Pi(H_0/H_1)]
     \\
     && \downarrow
     \\
     && [\Pi(S^{k-1}), \Omega\Pi(H_0/H_1)]
     \\
     & \swarrow && \searrow
     \\
     [\Pi(S^{k-1}), \Pi(H_1/H_2)] && (pb) && [\Pi(D^k), \Pi(H_0/H_2)] & \simeq & [\ast, \Pi(H_0/H_2)]
     \\
     & \searrow & & \swarrow
     \\
     && [\Pi(S^{k-1}), \Pi(H_0/H_2)]
  }
$$

This may be read as follows: 

1. on the far left $[\Pi(S^k), \Pi(H_1/H_2)]$ is the space of fields of the ambient theory at energy scale $E_2$ around the defect;

1. the bottom left map is the "fluctuation" map that sends these fields to fields at the higher energy scale $E_1$;

1. the bottom right map exhibt the possible "decays": a lift through this map takes a field configuration that winds around a $k$-ball and contracts it through that $k$-ball, hence going forth and back through the bottom two maps corresponds to carrying a defect over the energy barrier from $E_2$ to $E_1$ and there having it decay away.

1. these decaying configurations are therefore given by the [[homotopy fiber product]] of the bottom two functions, which is $[\Pi(S^{k-1}), \Omega\Pi(H_0/H_1)]$, as indicated. But this space is really given by field configurations at energy scale $E_1$ that wind around a $(k+1)$-ball, as shown at the very top.

Hence the top part of this diagram is a span that exhibits a defect-of-defects which tells just the story that ([Preskill & Vilenkin 1992](#PreskillVilenkin92)) is telling: a codimension-$k$ defect of the low energy theory decays at higher energy, and the decay is witnessed by the appearance of a codimension $(k+1)$-defect of the high energy theory.

$$
  \array{
     && {high\;energy \atop codim-(k+1)\;defects}
     \\
     && \downarrow
     \\
     && {low\;energy\;codim-k\;defects \atop with\;their\;decay\;processes}
     \\
     & \swarrow && \searrow
     \\
     {low\;energy \atop codim-k\;defects} && (pb) && {high\;energy \atop decay\;processes}
     \\
     & {}_{\mathllap{tunnel}}\searrow & & \swarrow_{\mathrlap{apply}}
     \\
     && {codim-k\;defects \atop raised\;to\;higher\;energy}
  }
$$


(...)




## Related concepts

* [[defect brane]]

* [[anyon]], [[braid group statistics]], [[loop braid group]]

* [[generalized global symmetry]]

\linebreak

[[!include field theory with boundaries and defects - table]]



## References

### General

A general formulation via an [[(∞,n)-category of cobordisms]] with defects:

* {#Lurie09} [[Jacob Lurie]], section 4.3 of: _[[On the Classification of Topological Field Theories]]_,  Current Developments in Mathematics Volume 2008 (2009) 129-280 &lbrack;[arXiv:0905.0465](http://arxiv.org/abs/0905.0465), [doi:10.4310/CDM.2008.v2008.n1.a3](https://dx.doi.org/10.4310/CDM.2008.v2008.n1.a3)&rbrack;

Defect TQFTs as 1-functors on stratified decorated bordisms are discussed in 

* {#DavydovRunkelKong11} [[Alexei Davydov]], [[Ingo Runkel]], [[Liang Kong]], _Field theories with defects and the centre functor_ &lbrack;[arXiv:1107.0495](https://arxiv.org/abs/1107.0495)&rbrack;, in [[Hisham Sati]], [[Urs Schreiber]] (eds.) _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ AMS (2011) &lbrack;[ams:pspum-83](https://bookstore.ams.org/pspum-83)&rbrack;
 
* {#CarquevilleRunkelSchaumann} [[Nils Carqueville]], [[Ingo Runkel]], [[Gregor Schaumann]], _Orbifolds of $n$-dimensional defect TQFTs_, Geom. Topol. **23** (2019) 781-864 *lbrack;[arXiv:1705.06085](http://arxiv.org/abs/1705.06085), [doi:10.2140/gt.2019.23.781](https://doi.org/10.2140/gt.2019.23.781)&rbrack;

Details in dimension 2 and 3 are discussed in

* [[Chris Schommer-Pries]], _Topological Defects and Classification of Local TQFTs in Low Dimension_, [[Oberwolfach Workshop, June 2009 -- Strings, Fields, Topology]] ([pdf](https://ncatlab.org/nlab/files/SchommerPriesDefects.pdf))

* {#FuchsSchweigertValentino13} [[Jürgen Fuchs]], [[Christoph Schweigert]], [[Alessandro Valentino]], *Bicategories for boundary conditions and for surface defects in 3-d TFT*, Commun. Math. Phys. **321**  (2013) 543–575 &lbrack;[arXiv:1203.4568](https://arxiv.org/abs/1203.4568), [doi:10.1007/s00220-013-1723-0](https://doi.org/10.1007/s00220-013-1723-0)&rbrack;

* [[Nils Carqueville]], [[Catherine Meusburger]], [[Gregor Schaumann]], *3-dimensional defect TQFTs and their tricategories*,  Advances in Mathematics **364** (2020), &lbrack;[arXiv:1603.01171](http://arxiv.org/abs/1603.01171), [doi:10.1016/j.aim.2020.107024](https://doi.org/10.1016/j.aim.2020.107024)&rbrack;

Review:

* [[Andrew Neitzke]], *Some uses of defects in quantum field theory* (2016?) &lbrack;[html](https://gauss.math.yale.edu/~an592/talks/html/defects-aspen/talk.html)&rbrack;

* [[Nils Carqueville]], [[Michele Del Zotto]], [[Ingo Runkel]], *Topological defects*, in: *[[Encyclopedia of Mathematical Physics 2nd ed]]* &lbrack;[arXiv:2311.02449](https://arxiv.org/abs/2311.02449)&rbrack;

Discussion of defects in [[prequantum field theory]], hence for [[coefficients]] in an [[(∞,n)-category of spans]] is in 

* {#FiorenzaValentino} [[Domenico Fiorenza]], [[Alessandro Valentino]], *Boundary Conditions for Topological Quantum Field Theories, Anomalies and Projective Modular Functors*,  Commun. Math. Phys. **338** (2015) 1043–1074  &lbrack;[arXiv:1409.5723](https://arxiv.org/abs/1409.5723), [doi:10.1007/s00220-015-2371-3](https://doi.org/10.1007/s00220-015-2371-3)&rbrack;
 

* {#FSS} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]] et. al, _[[schreiber:Higher Chern-Simons local prequantum field theory]]_

DIscussion with emphasis on [[Koszul duality]] such as in [[holography as Koszul duality]]:

* [[Natalie Paquette]], Brian R. Williams, *Koszul duality in quantum field theory* ([arXiv:2110.10257](https://arxiv.org/abs/2110.10257))
 

### Examples

#### General

Examples in physics of interaction of defects of various dimension is discussed in

* Muneto Nitta, _Defect formation from defect--anti-defect annihilations_,  Phys. Rev. D85:101702,2012 ([arXiv:1205.2442](http://arxiv.org/abs/1205.2442)) 


#### In 2d field theory



Defects in [[2-dimensional conformal field theory]] have a long history in real-world application, for instance in [[Kramers-Wannier duality]]. Formalization by [[higher algebra|higher]] [[categorical algebra]] via the [[FRS theorem on rational 2d CFT]] is due to:

* {#FRS04} [[Jürg Fröhlich]], [[Jürgen Fuchs]], [[Ingo Runkel]], [[Christoph Schweigert]], *Kramers-Wannier duality from conformal defects*, Phys. Rev. Lett. **93** (2004) 070601 &lbrack;[doi:10.1103/PhysRevLett.93.070601](https://doi.org/10.1103/PhysRevLett.93.070601), [arXiv:cond-mat/0404051](http://arxiv.org/abs/cond-mat/0404051)&rbrack;

with a comprehensive review in

* {#FFRS07} [[Jürg Fröhlich]], [[Jürgen Fuchs]], [[Ingo Runkel]], [[Christoph Schweigert]], *Duality and defects in rational conformal field theory*, Nucl. Phys. B **763** (2007) 354-430 &lbrack;[arXiv:hep-th/0607247](http://arxiv.org/abs/hep-th/0607247), [doi:10.1016/j.nuclphysb.2006.11.017](https://doi.org/10.1016/j.nuclphysb.2006.11.017)&rbrack;

Realization in [[lattice field theory]]:

* David Aasen, Roger S. K. Mong, Paul Fendley, *Topological Defects on the Lattice I: The Ising model*, J. Phys. A: Math. Theor. **49** (2016) 354001 &lbrack;[arXiv:1601.07185](https://arxiv.org/abs/1601.07185), [doi:10.1088/1751-8113/49/35/354001](https://doi.org/10.1088/1751-8113/49/35/354001)&rbrack;

* David Aasen, Paul Fendley, Roger S. K. Mong, *Topological Defects on the Lattice: Dualities and Degeneracies* &lbrack;[arXiv:2008.08598](https://arxiv.org/abs/2008.08598), [inspire:1812559](https://inspirehep.net/literature/1812559)&rbrack;

* Mao Tian Tan, Yifan Wang, Aditi Mitra, *Topological Defects in Floquet Circuits* &lbrack;[arXiv:2206.06272](https://arxiv.org/abs/2206.06272)&rbrack;

and simulation on a [[quantum computer]]:

* Sutapa Samanta, Derek S. Wang, Armin Rahmani, Aditi Mitra, *Isolated Majorana mode in a quantum computer from a duality twist* &lbrack;[arXiv:2308.02387](https://arxiv.org/abs/2308.02387)&rbrack;



Defects in 2-dimensional [[topological field theory]] have been studied a lot in the context of genus-0 TFT, where they are described using the language of [[planar algebras]]. 
See discussion at *[Planar Algebras, TFTs with Defects](http://golem.ph.utexas.edu/category/2008/09/planar_algebras_tfts_with_defe.html)*.

Lecture notes:

* [[Nils Carqueville]], _Lecture notes on 2-dimensional defect TQFT_ &lbrack;[arXiv:1607.05747](http://arxiv.org/abs/1607.05747)&rbrack;

On the derivation of the relevant topological term in 2d theories with defects through the use of bi-branes and inter-bi-branes:

* [[Ingo Runkel]], Rafal R. Suszek. *Gerbe-holonomy for surfaces with defect networks* (2008). ([arXiv:0808.1419](https://arxiv.org/abs/0808.1419)).

* [[Jürgen Fuchs]], [[Thomas Nikolaus]], [[Christoph Schweigert]], [[Konrad Waldorf]]. *Bundle Gerbes and Surface Holonomy* (2009). ([arXiv:0901.2085](https://arxiv.org/abs/0901.2085)).

* Rafal R. Suszek. *Defects, dualities and the geometry of strings via gerbes. I. Dualities and state fusion through defects* (2011). ([arXiv:1101.1126](https://arxiv.org/abs/1101.1126)).

* Rafal R. Suszek. *Defects, dualities and the geometry of strings via gerbes II. Generalised geometries with a twist, the gauge anomaly and the gauge-symmetry defect* (2012). ([arXiv:1209.2334](https://arxiv.org/abs/1209.2334)).

Defects in Landau-Ginburg theory: 

* [[Ilka Brunner]], Daniel Roggenkamp. *B-type defects in Landau-Ginzburg models* ([arXiv:0707.0922](https://arxiv.org/abs/0707.0922))

* [[Nils Carqueville]], [[Daniel Murfet]], *Adjunctions and defects in Landau-Ginzburg models*, ([arXiv:1208.1481](https://arxiv.org/abs/1208.1481))

* [[Nils Carqueville]], [[Ingo Runkel]], *Orbifold completion of defect bicategories*, ([arXiv:1210.6363](https://arxiv.org/abs/1210.6363))


#### In Chern-Simons theory

* An old example is the class of [[Turaev-Reshetikhin TQFT]], which is a functor on 3-dimensional [[cobordisms]] with codimension 3 and 2 defects. This is supposed to be the would-be result of [[Chern-Simons theory]], where the defect lines are the original [[Wilson lines]] in this context.

Defects in [[Chern-Simons theory]] and related systems are discussed in

* [[Davide Gaiotto]], [[Edward Witten]], _S-Duality of Boundary Conditions In N=4 Super Yang-Mills Theory_ ([arXiv:0807.3720](http://arxiv.org/abs/0807.3720))

* [[Anton Kapustin]], Mikhail Tikhonov, _Abelian duality, walls and boundary conditions in diverse dimensions_, JHEP 0911:006,2009 ([arXiv:0904.0840](http://arxiv.org/abs/0904.0840))

* [[Anton Kapustin]], [[Natalia Saulina]], _Surface operators in 3d TFT and 2d Rational CFT_ in [[Hisham Sati]], [[Urs Schreiber]] (eds.) _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ AMS, 2011

* [[Nils Carqueville]], [[Ingo Runkel]], [[Gregor Schaumann]], _Line and surface defects in Reshetikhin-Turaev TQFT_,  Quantum Topology **10** (2019), 399-439 ([arXiv:1710.10214](https://arxiv.org/abs/1710.10214))

In the context of the [[3d-3d correspondence]]:

* Dongmin Gang, Nakwoo Kim, Mauricio Romo, Masahito Yamazaki, _Aspects of Defects in 3d-3d Correspondence_, J. High Energ. Phys. (2016) ([arXiv:1510.05011](https://arxiv.org/abs/1510.05011))


Defects in [[higher dimensional Chern-Simons theory]] on [[manifolds with corners]] are discussed in

* [[Hisham Sati]], _Corners in M-theory_, J.Phys.A44:255402,2011 ([arXiv:1101.2793](http://arxiv.org/abs/1101.2793))


#### In Rozansky-Witten theory

* [[Anton Kapustin]], [[Lev Rozansky]], [[Natalia Saulina]], _Three-dimensional topological field theory and symplectic algebraic geometry I_ ([arXiv:0810.5415](https://arxiv.org/abs/0810.5415))

* [[Ilka Brunner]], [[Nils Carqueville]], [[Daniel Roggenkamp]], _Truncated affine Rozansky-Witten models as extended TQFTs_, Comm. Math. Phys. (2023), ([arXiv:2201.03284](https://arxiv.org/abs/2201.03284))

* [[Ilka Brunner]], [[Nils Carqueville]], Pantelis Fragkos, [[Daniel Roggenkamp]], _Truncated affine Rozansky-Witten models as extended defect TQFTs_, ([arXiv:2307.06284](https://arxiv.org/abs/2307.06284))


#### Topological defects in gauge theories with broken symmetry
 {#TopologicalDefectsInGaugeTheories}

The following references discuss the traditional notion of _[[topological defects]] in the [[vacuum]] structure of gauge theory with [[spontaneous symmetry breaking]]_ such as [[domain walls]], [[cosmic strings]] and [[monopoles]].

Discussion of [[topological defects]] of higher [[codimension]]  in [[gauge theory]]:

* {#PreskillVilenkin92} [[John Preskill]], [[Alexander Vilenkin]]: *Decay of Metastable Topological Defects*, Phys. Rev. D **47** (1993) 2324-2342 &lbrack;[arXiv:hep-ph/9209210](http://arxiv.org/abs/hep-ph/9209210), [doi:10.1103/PhysRevD.47.2324](https://doi.org/10.1103/PhysRevD.47.2324)&rbrack;
 
* {#VilenkinShellard94} [[Alexander Vilenkin]], E. P. S. Shellard: *Cosmic strings and other topological defects*, Cambridge University Press (1994) &lbrack;[ISBN:9780521654760](https://www.cambridge.org/us/universitypress/subjects/physics/theoretical-physics-and-mathematical-physics/cosmic-strings-and-other-topological-defects?format=PB&isbn=9780521654760)&rbrack;
 


#### In solid state physics

Defects field theory motivated from [[solid state physics]] is discussed in

* {#KitaevKong11} [[Alexei Kitaev]], [[Liang Kong]], _Models for gapped boundaries and domain walls_ Commun. Math. Phys. 313 (2012) 351-373  ([arXiv:1104.5047](http://arxiv.org/abs/1104.5047))
 


[[!include defect anyons -- references]]




[[!redirects QFTs with defects]]

[[!redirects defect]]
[[!redirects defects]]

[[!redirects field theory with singularities]]

[[!redirects defect field theory]]
[[!redirects defect field theories]]

[[!redirects defect QFT]]
[[!redirects defect QFTs]]


