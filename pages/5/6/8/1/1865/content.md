
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea 

_Differential K-theory_ is the refinement of the [[generalized (Eilenberg-Steenrod) cohomology]] theory [[K-theory]] to [[differential cohomology]].

In as far as we can think of cocycles in [[K-theory]] as represented by [[vector bundle]]s or [[vectorial bundle]]s, cocycles in differential K-theory may be represented by [[vector bundle]]s [[connection on a bundle|with connection]].

There are various different models that differ in the concrete realization of these cocycles and in their extra properties.


## The Simons-Sullivan model {#SimonsSullivanModel}

This section discusses the model presented in ([SimonsSullivan](#SimonsSullivan)).


More details will eventually be at

* [[Simons-Sullivan structured bundle]].

### Idea 

In the Simons-Sullivan model cocycles in differential K-theory are represented by ordinary [[vector bundle]]s [[connection on a bundle|with connection]]. The crucial ingredient is that two connections on a vector bundle are taken to be the same representative of a differential K-cocycle if they are related by a [[concordance]] such that the corresponding [[Chern-Simons form]] is exact.

### Details

Let $V \to X$ be a complex [[vector bundle]] with [[connection on a bundle|connection]] $\nabla$ and [[curvature]] 2-form

$$
  F = F_\nabla \in \Omega^2(X,End(V))
  \,.
$$

**Definition**

The **[[Chern character]]** of $\nabla$ is the inhomogenous [[curvature characteristic form]] 

$$
 ch(\nabla) := \sum_{j \in \mathbb{N}}
   k_j
   tr( F_\nabla \wedge \cdots \wedge F_\nabla)
  \;\;
  \in \Omega^{2 \bullet}(X)
  \,,
$$

where on the right we have $j$ wedge factors of the [[curvature]] .

**Definition**

Let $(V,\nabla)$ and $(V',\nabla')$ be two complex
vector bundles with connection.

A [[Chern-Simons form]] for this pair is a differential form

$$
  CS(\nabla,\nabla') + d \omega \in
  \Omega^{2 \bullet + 1}(X)
$$

obtained from the [[concordance]] bundle $\bar V \to X \times [0,1]$ given by [[pullback]] along $X \times [0,1] \to X$ equipped with a connection $\bar \nabla$ such that ..., by

$$
  CS(\nabla,\nabla') =
  \int_0^1 \psi_t^* (\iota_{\partial/\partial t} ch(\bar \nabla))
  + d (...)
  \,.
$$

**Proposition** This is indeed well defined in that it is independent of the chosen [[concordance]], up to an exact term.

**Definition**

A **structured bundle** in the sense of the Simons-Sullivan model is a complex vector bundle $V$ equipped with the equivalence class $[\nabla]$ of a connection under the equivalence relation that identifies two connections $\nabla$ and $\nabla'$ if their Chern-Simons form $CS(\nabla,\nabla')$ is exact.

Two structured bundles are isomorphic if there is a vector bundle isomorphism under which the two equivalence classes of connections are identified.

**Definition** 

Let $Struc(X)$ be the set of [[isomorphism]] classes of structured bundles on $X$. 

Under [[direct sum]] and [[tensor product]] of vector bundles, this becomes a commutatve [[rig]].

Let 
$$
  \hat K(X) := K(Struct(X))
$$

be the additive [[group completion]] of this rig as usual in [[K-theory]].

So as an additive group $\hat K(X)$ is the quotient of the [[monoid]] induced by [[direct sum]] on pairs $(V,W)$ of isomorphism classes in $Struc(X)$, modulo the sub-monoid consisting of pairs $(V,V)$.

Hence the pair $(V,0)$ is the additive inverse to $(0,V)$ and $(V,W)$ may be written as $V - W$.

**Theorem**

$\hat K(X)$ is indeed a [[differential cohomology]] refinement of ordinary K-theory $K(X)$ of $X$ (i.e. of the 0th [[cohomology group]] of [[K-theory spectrum|K-cohomology]]).

Moreover...



## The Bunke-Schick model 

### Idea

[[Uli Bunke]] and [[Thomas Schick]] developed in a series of articles a differential-geometric cocycle model of differential K-theory where cocycles are given by smooth families of [[Dirac operator]]s.

See the reference [below](BunkeSchickReferences).

### Properties

The restriction of the cocycles in the Bunke-Schick model to those whose "auxialiary form" $\omega$ vanishes reproduces the Simons-Sullivan model above.

## The Hopkins-Singer model

See at

* _[[differential function complex]]_

* _[differential cohomology diagram -- Hopkins-Singer differential KU](differential+cohomology+diagram#HSDifferentialKU)_


## More models in smooth spectra

See at _[Differential cohomology diagram -- Differential K-theory](differential+cohomology+diagram#DifferentialKTheory)_.

## Examples 

* In [[gauge theory]] gauge fields are modeled by cocycles in [[differential cohomology]]. The field modeled by differential K-theory is the [[RR-field]]. A kind of [[integral transform]] acting on differential K-theory classes is [[T-duality]].


## Related concepts

* [[flat K-theory]]

* [[K-theory]], [[topological K-theory]]

* [[twisted K-theory]]

* **differential K-theory**

  * [[fiber integration in differential K-theory]]

  * [[algebraic K-theory of smooth manifolds]]

* [[twisted differential K-theory]]

* [[equivariant differential K-theory]], [[orbifold differential K-theory]]

* [[differential algebraic K-theory]]

## References

### General

An early sketch of a general definition, motivated by the description of [[D-brane charge]] in [[string theory]], is in 

* [[Daniel Freed]], _[[Dirac charge quantization and generalized differential cohomology]]_, Surveys in Differential Geometry, Int. Press, Somerville, MA, 2000, pp. 129&#8211;194 ([arXiv:hep-th/0011220](http://arxiv.org/abs/hep-th/0011220))

* [[Daniel Freed]], [[Michael Hopkins]], *On Ramond-Ramond fields and K-theory*, JHEP (2000) 44, 14 &lbrack;[arXiv:hep-th/0002027](http://arxiv.org/abs/hep-th/0002027), [doi:10.1088/1126-6708/2000/05/044](https://doi.org/10.1088/1126-6708/2000/05/044)&rbrack;

Then the general construction of [[differential cohomology]] theories via [[differential function complexes]] of 

* {#HopkinsSinger05} [[Michael Hopkins]], [[Isadore Singer]], _[[Quadratic Functions in Geometry, Topology, and M-Theory]]_,  J. Differential Geom. Volume 70, Number 3 (2005), 329-452 ([arXiv:math.AT/0211216](http://arxiv.org/abs/math.AT/0211216))

(motivated in turn by [[7d Chern-Simons theory]] and the [[M5-brane]] [[partition function]])

provides in particular a model for differential K-theory. 

For more historical remarks see section 1.6 of 

* {#FreedLott10} [[Daniel Freed]], [[John Lott]], _An index theorem in differential K-theory_, Geometry and Topology 14 (2010) ([pdf](http://math.berkeley.edu/~lott/gt-2010-14-021p.pdf))

A discussion of more models and their relation in the context of [[cohesive homotopy type theory]] and the [[differential cohomology hexagon]] then appears in 

* {#BunkeNikolausVoelkl13} [[Ulrich Bunke]], [[Thomas Nikolaus]], [[Michael Völkl]], Section 6 of: _Differential cohomology theories as sheaves of spectra_ ([arXiv:1311.3188](http://arxiv.org/abs/1311.3188))

Survey:

* {#BunkeSchick10} [[Ulrich Bunke]], [[Thomas Schick]], _Differential K-theory. A survey_ ([arXiv:1011.6663](http://arxiv.org/abs/1011.6663)).


Cocycle models via [[vector bundles]] [[bundle with connection]]:

* [[Max Karoubi]], *Homologie cyclique et K-théorie*, Astérisque, no. 149 (1987) ([numdam:AST_1987__149__1_0](http://www.numdam.org/item/AST_1987__149__1_0))

* [[John Lott]], *$\mathbf{R}/\mathbf{Z}$ Index theory*, Communications in Analysis and Geometry **2** 2 (1994) 279-311 ([pdf](https://math.berkeley.edu/~lott/rztheory.pdf))

* {#SimonsSullivan} [[James Simons]], [[Dennis Sullivan]], _Structured vector bundles define differential K-theory_ ([arXiv:0810.4935](http://arxiv.org/abs/0810.4935))
  

The basic article for the Bunke-Schick model is

* {#BunkeSchick09} [[Ulrich Bunke]], [[Thomas Schick]], _Smooth K-Theory_, Astérisque 328 (2009), 45-135 &lbrack;[arXiv:0707.0046](http://arxiv.org/abs/0707.0046), [numdam:AST_2009__328__45_0](http://www.numdam.org/item/?id=AST_2009__328__45_0)&rbrack;

A survey talk is

* [[Ulrich Bunke]], _Differential cohomology in geometry and analysis_ ([pdf slides](http://www.uni-regensburg.de/Fakultaeten/nat_Fak_I/Bunke/Vortrag-Erlangen.pdf))

On differential [[KO-theory]]:

* {#GradySati18} [[Daniel Grady]], [[Hisham Sati]], _Differential KO-theory: Constructions, computations, and applications_, Advances in Mathematics Volume 384, 25 June 2021, 107671 ([arXiv:1809.07059](https://arxiv.org/abs/1809.07059), [doi:10.1016/j.aim.2021.107671](https://doi.org/10.1016/j.aim.2021.107671))

* [[Kiyonori Gomi]], [[Mayuko Yamashita]], *Differential KO-theory via gradations and mass terms* &lbrack;[arXiv:2111.01377](https://arxiv.org/abs/2111.01377)&rbrack;


Of [[twisted K-theory|twisted]] [[differential K-theory|differential]] [[KO-theory|orthogonal]] [[topological K-theory|K-theory]]:

* {#GradySati19} [[Daniel Grady]], [[Hisham Sati]], _Twisted differential KO-theory_ ([arXiv:1905.09085](https://arxiv.org/abs/1905.09085))



The equivalence of these models with the respective special case of the general construction in [Hopkins & Singer 05](#HopkinsSinger05) in terms of [[differential function complexes]] is in 

* Kevin Klonoff, _An Index Theorem in Differential K-Theory_ PdD thesis (2008) ([pdf](http://www.lib.utexas.edu/etd/d/2008/klonoffk16802/klonoffk16802.pdf))

(assuming the existence of a universal connection, which is not strictly proven) and

* Michael L. Ortiz, _Differential Equivariant K-Theory_ ([arXiv:0905.0476](http://arxiv.org/abs/0905.0476))

(not needing that assumption).

A construction of [[differential cobordism cohomology]] theory in terms of explicit geometric cocycles is in

* [[Ulrich Bunke]], [[Thomas Schick]], Ingo Schroeder, Moritz Wiethaup _Landweber exact formal group laws and smooth cohomology theories_ ([arXiv:0711.1134](http://arxiv.org/abs/0711.1134))

By tensoring this with the suitable ring, this also gives a model for differential K-theory, as well as for [[differential elliptic cohomology]].

A variant of this definition with the advantage that there is a natural morphism to [[Cheeger-Simons differential characters]] refining the total [[Chern class]] is (as opposed to the [[Chern character]]) is presented in

* Alain Berthomieu, _A version of smooth K-theory adapted to the
total Chern class_ ([pdf](http://arxiv.org/PS_cache/arxiv/pdf/0806/0806.4728v1.pdf))

Discussion for the [[odd Chern character]] is in

* [[Thomas Tradler]], [[Scott Wilson]], [[Mahmoud Zeinalian]], _An Elementary Differential Extension of Odd K-theory_, J. of K-theory, K-theory and its Applications to Algebra, Geometry, Analysis
and Topology, ([arXiv:1211.4477](http://arxiv.org/abs/1211.4477))

* [[Scott Wilson]], _A loop group extension of the odd Chern character_ ([arXiv:1311.6393](http://arxiv.org/abs/1311.6393))

A model in terms of [[super vector bundles]] is given in

* Jae Min Lee, Byungdo Park, _A Superbundle Description of Differential K-Theory_, Axioms 2023, 12(1), 82, ([doi:10.3390/axioms12010082](https://doi.org/10.3390/axioms12010082)).



### Relation to index theory

Relation to [[index theory]]: 

* Kevin Klonoff, _An Index Theorem in Differential K-Theory_ PdD thesis (2008) ([pdf](http://www.lib.utexas.edu/etd/d/2008/klonoffk16802/klonoffk16802.pdf))

* [[Daniel Freed]], [[John Lott]], _An index theorem in differential K-theory_, Geometry and Topology 14 (2010) ([pdf](http://math.berkeley.edu/~lott/gt-2010-14-021p.pdf))

See also the references at _[[fiber integration in differential K-theory]]_.

### In string theory

A survey of the role of differential $K$-theory in [[quantum field theory]] and [[string theory]] is in 

* [[Daniel Freed]], _K-Theory in Quantum Field Theory_, Current developments in Mathematics (2001) International Press Somerville ([arXiv:math-ph/0206031](http://arxiv.org/abs/math-ph/0206031))

The operation of [[T-duality]] on hypothetical [[twisted differential K-theory]] is discussed in

* [[Alexander Kahle]], [[Alessandro Valentino]], _[[T-Duality and Differential K-Theory]]_

Discussion of [[twisted K-theory|twisted]] [[differential K-theory|differential]] [[topological K-theory|K-theory]] and its relation to [[D-brane charge]] in [[type II string theory]] (see also [there](D-brane#ReferencesKTheoryDescription)):

* {#GradySati19a} [[Daniel Grady]], [[Hisham Sati]], *Ramond-Ramond fields and twisted differential K-theory*, 
Advances in Theoretical and Mathematical Physics **26** (2022) 5 &lbrack;[arXiv:1903.08843](https://arxiv.org/abs/1903.08843), [doi:10.4310/ATMP.2022.v26.n5.a2](https://dx.doi.org/10.4310/ATMP.2022.v26.n5.a2)&rbrack;

Discussion of [[twisted K-theory|twisted]] [[differential K-theory|differential]] [[KO-theory|orthogonal]] [[topological K-theory|K-theory]] and its relation to [[D-brane charge]] in [[type I string theory]] (on [[orientifolds]]):

* {#GradySati19b} [[Daniel Grady]], [[Hisham Sati]], _Twisted differential KO-theory_ ([arXiv:1905.09085](https://arxiv.org/abs/1905.09085))


See also:

* [[Thomas Tradler]], [[Scott Wilson]], [[Mahmoud Zeinalian]], _Loop Differential K-theory_ ([arXiv:1201.4593](http://arxiv.org/abs/1201.4593))
