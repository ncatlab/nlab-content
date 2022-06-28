
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Stable homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea

### General

A _stability condition_ ([Bridgeland 02](#Bridgeland02)) on a [[triangulated category]] ([hence](triangulated+category#FromStableModelCategories) on a [[stable model category]]/[[stable (∞,1)-category]]) $\mathcal{D}$ (Def. \ref{StabilityCondition} below) singles out some of its [[objects]], to be called the "stable objects" (Def. \ref{StableObjects} below), that behave, to some extent, like [[indecomposable objects]] (whence "stable"), in that a version of [[Schur's lemma]] applies to them (Prop. \ref{SchurLemma} below).

Indeed, in the degenerate case that $\mathcal{D}$ is the [[derived category]] of a [[semisimple category]], the stable objects are just the [[irreducible objects]].

In the case where $\mathcal{D}$ is the bounded [[derived category]] of [[coherent sheaves]] on some [[complex manifold]], the general notion of stability reduces to the classical notion of [[slope of a coherent sheaf|slope]]-[[stable coherent sheaf|stability of coherent sheaves]] ("$\mu$-stability", see Example \ref{SlopeStability} below). 

In other examples Bridgeland stability reproduces the derived analogue of [[David Mumford]]'s concept of [[GIT-stable point|stability]] in [[geometric invariant theory]] ([King 94](#King94)).

There are in general different stability conditions on one and the same [[triangulated category]], in fact their [[moduli space]] $Stab(\mathcal{D})$ forms a [[complex manifold]] (Prop. \ref{SpaceOfStabilityConditions} below). The collection of stable objects in $\mathcal{D}$ in general depends on the choice of stability conditions, hence of the choice of point in this [[moduli space]]: There are in general [[codimension]]-1 [[submanifolds]] of $Stab(\mathcal{D})$, called _walls_, such that the set of stable objects is constant close to both sides of these walls, but changes as the wall is crossed. This phenomenon is hence known as _[[wall crossing]]_.

The purely mathematical motivation for these definitions is, to a large extent, just their intrinsic richness. The concept finds its meaning in the concept of stability of [[D-branes]] in [[string theory]] and was abstracted from informal considerations about [[B-branes]] of the [[B-model]] [[topological string]] due to ([Douglas-Fiol-Romerlsberger 00](#DouglasFiolRomerlsberger00)) and followups ("$\Pi$-stability"). 

This [[string theory|string-theoretic]] interpretation also sheds light on the older notion of [[slope of a coherent sheaf|slope]]-[[stable coherent sheaf|stability of coherent sheaves]], we discuss this [below](#AsStabilityOfBPSDBranes).


### As stability of BPS D-branes
 {#AsStabilityOfBPSDBranes}

We explain here how to understand the mathematical formulation of stability conditions as a formalization of the concept of stable [[BPS states]] of [[D-branes]], hence of [[extremal black hole|extremal]] [[black branes]]. This yields a very simple and beautiful picture, which may be hard to extract from the original proposal due to [Douglas-Fiol-Romerlsberger 00](#DouglasFiolRomerlsberger00) (as witnessed by various reviews of the concept, see for instance [Stellari 15, slide 9](#Stellari15)).

A key point to notice is that _[[coherent sheaves]]_ and with them most of the kinds of [[objects]] in [[triangulated categories]] of relevance here, may be thought of as models for [[D-branes]] carrying [[D-brane charge]].

Specifically, for $X$ a [[space]], to be thought of as [[spacetime]], a [[coherent sheaf]] $E$ over $X$ may be thought of as an [[abelian sheaf]] of [[sections]] of a kind of  [[complex vector bundle]] over $X$, whose [[fiber]] [[dimension]] is allowed to jump in some controlled way. Hence coherent sheaves are a slight generalization of _[[complex vector bundles]]_.

When considering [[D-branes]] on $X$, such coherent sheaves/vector bundles $E$ appear as the [[Chan-Paton gauge fields]] on the D-brane.

$$
  \text{object}\, E
  \phantom{AA}\leftrightarrow\phantom{AA}
  \text{D-brane carrying mass and charge}
$$

From this perspective, the [[rank of a vector bundle|rank]] 

$$
  rank(E)
  \;\in\;
  \mathbb{R}
$$ 

of $E$ is the number of coincident D-branes (there may be [[fractional D-branes]], and, once we pass to the [[derived category]], there may be [[anti D-branes]], so that this number need not be a [[positive integer]]). 

The [[D-branes]] have a fixed [[tension]] and hence a fixed [[mass]]-density, so that the total [[mass]] of the D-branes corresponding to $E$ is proportional to this rank. Ignoring the constant proportionality factor, we make this explicit by re-writing the rank as

$$
  M(E)
  \;\coloneqq\;
  rank(E)
  \,.
$$

In addition to their mass, the D-branes carry [[charge]], called [[RR-field|RR-charge]]. This is a generalization of the classical [[magnetic charge]] known from [[Dirac charge quantization]]. As explained there, magnetic charge reflected in a [[complex line bundle]], as sourced by magnetic [[monopoles]] ([[D0-branes]]) is measured by the [[first Chern class]]  $c_1(E)$. In generalization of this, the total [[D-brane charge]] reflected in a [[Chan-Paton gauge field]] $E$ is proportional its [[Chern character]] $ch(E)$.

$$
  Q(E) 
    \;\in\;
  \mathbb{R}
  \,.
$$

For coherent sheaves this is essentially what is classically called the _[[degree of a coherent sheaf]]_. Interpreting this as the [[charge]] carried by the D-brane, we may write


$$
  Q(E)
  \;=\;
  degree(E)
$$

Accordingly, [[D-branes]] $E$ have a _charge density_ proportional to

$$
  ChargeDensity(E) 
    \;\coloneqq\; 
  \frac{ Q(E) }{ M(E) }
    \;=\;
  \frac{ degree(E) }{ rank(E) }
    \;=\;
   slope(E)
  \,.
$$

This quotient is what is classically called the _[[slope of a coherent sheaf|slope]]_, as shown on the right. The terminology comes from thinking of the [[pair]] ([[mass]], [[charge]]), hence the pair ([[rank of a coherent sheaf|rank]], [[degree of a coherent sheaf|degree]]) as specifying a [[point]] in the [[plane]]

$$
  (M(E), \; Q(E))
   \;=\;
  ( rank(E), \; degree(E) )
  \;\in\;
  \mathbb{R}^2
$$

Under this identification the charge density is the [[slope of a line]] of the [[line]] in the [[Cartesian space|Cartesian]] [[plane]] which goes through [[zero]] and through $(M(E), Q(E))$, whence the term _[[slope of a coherent sheaf]]_. But understanding this not as a slope but as a _charge density_ reveals why this has anything to do with "stability", as we proceed to explain now.

First notice that, alternatively, we may identify the [[real numbers|real]] [[plane]] with the [[complex plane]] and thus unify the [[mass]] and [[charge]] of [[D-branes]] into a single [[complex number]]

\[
  \label{TheComplexifiedMassInIdeaSection}
  \begin{aligned}
    Z(E)
    & \coloneqq\;
    M(E) + i \, Q(E)
    \\
    & = m(E) \, \exp( i \pi \phi(E) )
    \;\in\;
    \mathbb{C}
  \end{aligned}
\]

with an [[absolute value]] $m(E)$ and a [[complex phase]] (modulo $\pi$) $\phi(E)$. 

(Such unification of two different quantities into a single complex quantity appears all over [[supersymmetry|supersymmetric]] theory, for instance also in the definition of [[complex volume]] or the complex coupling constant appearing in the context of [[S-duality]].)


Finally to see what all this has to do with "stability":

In a [[supersymmetry|supersymmetric]] theory such as [[superstring theory]] the stable states are supposed to be the [[BPS-states]]. When thinking of [[D-branes]] as [[black branes]], being higher dimensional generalizations of charged [[black holes]], the BPS states correspond to the higher dimensional analog of the _[[extremal black holes]]_, namely those that carry maximum [[charge]] for given [[mass]], hence that _maximize their charge density_ 
 
$$
  \text{stable D-brane}
  \;\;\Leftrightarrow\;\;
  \text{BPS/extremal black D-brane}
  \;\;\Leftrightarrow\;\;
  \text{ maximum charge density }\, Q/M   
$$

Now it is plausible that a D-brane $E$ maximizes its potential charge density if removing any part $e$ of it reveals that $e$ by itself has lower charge density.

More formally, $E$ should maximize its charge density $Q(E)/M(E)$ and hence be _stable_ if for all sub-parts

$$
  e \subset E
$$ 

hence for all _[[subobjects]]_ in the relevant [[category]] (such as that of [[coherent sheaves]]) we have that the charge density of the part is smaller than the charge density of the whole: 

\[
  \frac{Q(e)}{M(e)}
  \;\lt\; 
   \frac{ Q(E) }{ M(E) }
\]

Conversely, this means that a D-brane state $e$ can increase its charge density, hence get close to being BPS and hence stable, by forming a [[bound state]] to be come an $E$.

In the case of coherent sheaves, where the D-brane charge density is called the _[[slope of a coherent sheaf]]_ $slope(E) = Q(E)/M(E)$, as above, this says that $E$ is a [[stable coherent sheaf]] precisely if for all [[subobjects]] $e \subset E$ we have

$$
  slope(e) \;\lt\; slope(E)
  \,.
$$

This is the classical formulation of _[[stable coherent sheaf|slope stability]]_ or _$\mu$-stability_ of [[coherent sheaves]].

Of course we may equivalently re-express in terms of the [[complex phase]] $\phi(E)$ induced by the complexified mass/charge from (eq:TheComplexifiedMassInIdeaSection). Since the slope of a [[complex number]] (regarded as a [[vector]] in the [[plane]]) equals the [[tan]] of its [[complex phase]] we have

$$
  \frac{Q(E)}{M(E)}
  \;=\;
  tan\big( \phi(E)/2 \big)
  \,.
$$

But since $tan((-)/2)$ is a [[monotone function]] on the [[domain]] $(-\pi/2, \pi/2)$, then if we agree to regard $\phi$ as taking values in that [[interval]], then the above stability condition becomes equivalently the statement that for all [[subobjects]] $e \hookrightarrow E$ we have

$$
  \phi(e) \;\lt\; \phi(E)
  \,.
$$

This is the form in which [Bridgeland 02](#Bridgeland02) phrases the stability condition, see Def. \ref{StableObjects} below.

But the upshot is that this is still equivalent to saying that $E$ is stable precisely if it maximizes its [[charge]]- over [[mass]]-density, as befits an [[extremal black hole]] and, more generally, a [[BPS state|BPS]] [[black brane]].

$\,$

## Definition


+-- {: .num_defn #StabilityFunction}
###### Definition
**(stability function)**

Let $\mathcal{A}$ be an [[additive category]]. 

A **stability function** (sometimes also called a _central charge_) is a  [[linear map]] 

\[
  \label{StabilityFunction}
  Z 
  \;\colon\; 
  K(\mathcal{A})
  \longrightarrow 
  \mathbb{C}
\] 

from [[Grothendieck group]] $K(\mathcal{A})$ to the [[abelian group|additive group]] of [[complex numbers]], 
such that for all non-[[zero objects]] $E \in \mathcal{A}$, the [[image]] $Z(E)$ lies in the [[upper half-plane|semi-upper half plane]] 

$$
  H
  \;=\;
  \big\{
    r exp(i\pi \phi) 
    \;\vert\; 
    r \gt 0
    \;\text{and}\;
    0 \lt \phi \leq 1
  \big\}
$$ 

The _phase_ 

\[
  \label{PhaseOfAnObject}
  \phi(E)
  \;\coloneqq\;
  \tfrac{1}{\pi}
  arg\big( 
    Z(E)
  \big)
  \;\in\;
  (0,1]
\] 

of an non-[[zero object]] $E \in \mathcal{A}$ is just the [[complex phase]] $\phi$ that occurs in the representation from $H$. Alternatively, by plotting $Z(E)$ in the  [[complex plane]], the phase is the argument (slope) divided by $\pi$. 

=--

([Bridgeland 02, Def. 2.1](#Bridgeland02))


+-- {: .num_defn #StableObjects}
###### Definition
**((semi-)stable objects)**

For $\mathcal{A}$ an [[abelian category]] equipped with a stability function $Z = r exp(i\pi \phi)$ (Def. \ref{StabilityFunction}). Then a non-[[zero object]] $E \in \mathcal{A}$ is called

1. a _semi-stable object_ if for all non-[[zero object|zero]] [[subobjects]] $F\subset E$ the phase (eq:PhaseOfAnObject) of $F$ is smaller or equal that of $E$

   \[
     \label{SemiStability}
     \phi(F)
       \;\leq\; 
     \phi(E)
   \]


1. a _stable object_ if for all non-[[zero object|zero]], proper [[subobjects]] $F \subset E$ the phase (eq:PhaseOfAnObject) of $F$ is strictly smaller than that of $E$:

   \[
     \label{Stability}
     \phi(F) 
       \;\lt\;
     \phi(E)
     \,.
   \]

=--

([Bridgeland 02, Def. 2.2](#Bridgeland02))



+-- {: .num_defn #HarderNarasimhanProperty}
###### Definition
**(Harder-Narasimhan property)**

A stability function $Z \;\colon\; K(\mathcal{A})\to \mathbb{C}$ (Def. \ref{StabilityFunction}) is said to have the _Harder-Narasimhan property_ if for any non-[[zero object]] $E$ there exists a finite [[filtered object|filtration]] by [[subobjects]] 

$$
  0=E_0 \subset E_1 \subset \cdots \subset E_n =E
$$ 

such that the [[quotients]] 

$$
  F_i
   =
  E_i/E_{i-1}
$$ 

are all semi-stable (eq:SemiStability) and satisfy 

$$
  \phi(F_1) \gt \phi(F_2) \gt \cdots \gt\phi(F_n)
  \,.
$$


=--

([Bridgeland 02, Def. 2.3](#Bridgeland02))


+-- {: .num_defn #Slicing}
###### Definition
**(slicing)**

Let $\mathcal{D}$ be a [[triangulated category]] (usually arising as the [[derived category]] of some [[abelian category]]). 

A _slicing_  $\mathcal{P}$ on $\mathcal{D}$ is a choice of [[additive category|additive]] [[full subcategories]] $\mathcal{P}(\phi) \subset \mathcal{D}$ for each $\phi \in \mathbb{R}$ satisfying 

1. $\mathcal{P}(\phi +1)=\mathcal{P}(\phi)[1]$

2. If $\phi_1 \gt \phi_2$ and $A_j\in \mathcal{P}(\phi_j)$, then $Hom(A_1, A_2)=0$.

3. Any object has a finite [[filtration]] by the slicing: 

   If $E\in \mathcal{D}$, then there exists $\phi_1 \gt \cdots \gt \phi_n$ and a sequence $0=E_0\to E_1 \to \cdots \to E_n = E$ such that the [[mapping cone]] $E_{j-1}\to E_j \to F_j \to E_{j-1}[1]$ satisfies $F_j\in \mathcal{P}(\phi_j)$.

=--

([Bridgeland 02, Def. 3.3](#Bridgeland02))


+-- {: .num_defn #StabilityCondition}
###### Definition
**(stability condition)**

A **stability condition** on a [[triangulated category]] $\mathcal{D}$ is a [[pair]] $\sigma = (Z, \mathcal{P})$ consisting of 

1. a stability function (Def. \ref{StabilityFunction})

1. a slicing (Def. \ref{Slicing})

satisfying the relation that given a non-[[zero object]] $E\in \mathcal{P}(\phi)$, then there is a [[positive number|positive]] [[real number]] $m(E)$ such that the value $Z(E)$ of the stability function (Def. \ref{StabilityCondition}) is

$$
  Z(E)
  \;=\; 
  m(E)
  \,
  exp(i\pi \phi)
  \,.
$$

=--

([Bridgeland 02, Def. 5.1](#Bridgeland02))

This justifies the repeated notation of $\phi$, since this says that if an object lies in a particular slice $\mathcal{P}(\phi)$, then it must also have [[complex phase]] $\phi$.


$\,$

## Properties

### In terms of hearts of t-structures

Bridgeland proves that an equivalent way to give a stability is to specify a heart of a bounded [[t-structure]] on $\mathcal{D}$ and give a stability function the heart that satisfies the Harder-Narasimhan property.


### Schur's lemma
 {#LemmaSchur}

+-- {: .num_prop #SchurLemma}
###### Proposition
**([[Schur's lemma]])**

Let $\mathcal{A}$ be an [[abelian category]] equipped with a stability condition (Def. \ref{StabilityCondition}).

For $E \in \mathcal{A}$ a stable object (Def \ref{StableObjects}), every [[endomorphism]] of $E$ is either the [[zero morphism]] or is an [[isomorphism]]; in particular if $\mathcal{A}$ is [[enriched category|enriched]] in [[vector spaces]] over an [[algebraically closed field]] $k$, then $End(E) \simeq k$.

More generally, for $E_1, E_2 \in \mathcal{A}$ two stable objects of the same slope/phase, $\phi(E_1) =\phi(E_2)$, any [[morphism]] $E_1 \to E_2$ is either the [[zero morphism]] or is an [[isomorphism]].


=--

e.g. ([Bayer 11, 2.3 Exercise 1](#Bayer11),  [Martinez 13, prop. 3](#Martinez13)) 


### Space of stability conditions
 {#SpaceOfStabilityConditions}


+-- {: .num_prop #SpaceOfStabilityConditions}
###### Proposition
**(space of stability conditions)**

Under reasonable hypotheses (...), one can put a natural [[topological manifold|topology]] on the space $Stab(\mathcal{D})$ of all stability conditions (Def. \ref{StabilityCondition}) , under which the space becomes a [[complex manifold]]. 
=--

([Bridgeland 02, theorem 1.2](#Bridgeland02), reviewed in [Bridgeland 09, 3.2](#Bridgeland09))

Most work using this fact has been done in the case of the [[bounded derived category of coherent sheaves]] $\mathcal{D}=D^b(Coh(X))$ where $X$ is a smooth, projective [[algebraic variety|variety]] over $\mathbb{C}$ so that $\mathcal{D}$ is $\mathbb{C}$-linear and $K(\mathcal{D})$ is finitely generated.


The space of stability conditions $Stab(X)$ has a locally finite wall and chamber decomposition. The philosophy is that if one fixes a numerical condition $v$ and considers the [[moduli space]] of $\sigma$-stable sheaves as $\sigma$ varies through $Stab(X)$, then the moduli spaces $M_\sigma(v)\simeq M_{\sigma '}(v)$ should be isomorphic if $\sigma$ and $\sigma'$ are in the same chamber. Bayer and Macri have shown this is true for K3 surfaces, and upon [[wall crossing|crossing a wall]] the moduli spaces are related by a [[birational map]].





## Examples

### Slope-stability of vector bundles / coherent sheaves
 {#SlopeStabilityOfVectorBundles}

A motivating example for the concept of Bridgeland stability is the following classical notion.

+-- {: .num_example #SlopeStability}
###### Example
**([[slope of a coherent sheaf|slope]]-[[stable coherent sheaf|stability of coherent sheaves]])**


Let $X$ be a non-singular, [[algebraic curve|projective curve]] over $\mathbb{C}$. Let $\mathcal{A}=Coh(X)$ be the [[category]] of [[coherent sheaves]] on $X$. 

In this case the standard stability function (Def. \ref{StabilityFunction}) is 

\[
  \label{StandardStabilityFunctionForVectorBundles}
  Z(E)
    \;\coloneqq\;
  -deg(E) + i rk(E)
\] 

where $deg$ is the _[[degree of a coherent sheaf|degree]]_ and $rk$ the _[[rank of a coherent sheaf|rank]]_ of a [[coherent sheaf]] $E$.

The classical notion of the _[[slope of a coherent sheaf|slope]] of a vector bundle is 

$$
  \mu(E)
  \;\coloneqq\;
  \frac{deg(E)}{rk(E)}
$$ 

When constructing a [[moduli space]] of vector bundles using [[geometric invariant theory|GIT]] one needs to consider only [[slope of a coherent sheaf|slope]] (semi-)[[stable vector bundles]] (see e.g. [Reineke 08, sections 3 and 4](#Reineke08)).

One can immediately see that a [[vector bundle]]/[[coherent sheaf]] is [[slope of a vector bundle|slope]] (semi-)[[stable vector bundle|stable]] if and only if it is (semi-)stable with respect to this stability function (eq:StandardStabilityFunctionForVectorBundles). 

=--

Thus Bridgeland stability generalizes the classical notions of [[stable vector bundle|stability of vector bundles]].



### Over resolutions of ADE-singularities
 {#OverResolutionsOfADESingularities}

For $G_{ADE} \subset SU(2)$ a [[finite subgroup of SU(2)]], 
let $\tilde X$ be the [[resolution of singularities|resolution]] of the corresponding [[ADE-singularity]]. 

Then the [[connected component]] of the space of stability conditions (Def. \ref{StabilityCondition}) on the bounded [[derived category]] of [[coherent sheaves]] over $\tilde X$ can be described explicitly ([Thomas 02](#Thomas02), [Bridgeland 05](#Bridgeland05), [Brav-Thomas 09](#BravThomas09)). 

Specifically for type-A singularities the space of stability conditions (Prop. \ref{SpaceOfStabilityConditions}) is in fact [[connected topological space|connected]] and [[simply-connected topological space]] ([Ishii-Ueda-Uehara 10](#IshiiUedaUehara10)). In fact spaces of stability structures over [[Dynkin quivers]] are [[contractible space|contractible]] ([Qiu-Woold 14](#QiuWoold14))

Brief review is in [Bridgeland 09, section 6.3](#Bridgeland09).

## Related concepts

* [[BPS states]]

* [[wall crossing]]

* [[geometric invariant theory]]


$\,$

## References


### General

The general definition is due to

* {#Bridgeland02} [[Tom Bridgeland]], _Stability conditions on triangulated categories_, Ann. of Math. 166 (2007) 317&#8211;345 ([math.AG/0212237](http://arxiv.org/abs/math/0212237))

generalizing the classical concept of [[slope of a vector bundle|slope]]-[[stable vector bundle|stability of vector bundles]] and of [[modules]] as in 

* {#King94} [[Alastair King]], _Moduli of representations of finite dimensional algebras_, The Quarterly Journal of Mathematics 45.4 (1994): 515-530 ([pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.623.649&rep=rep1&type=pdf))

and motivated by informal arguments in [[string theory]] about the "$\Pi$-stability" for [[B-branes]] of the [[B-model]] [[topological string]], due to [Douglas-Fiol-Römerlsberger 00](#DouglasFiolRomerlsberger00) and expanded on in [Douglas 01](#Douglas01), [Douglas 02](#Douglas02), [Aspinwall 04](#Aspinwall04) and other articles.
 
Further developments include

* R. Pandharipande, R.P. Thomas, _Stable pairs and BPS invariants_, [arXiv:0711.3899](http://arxiv.org/abs/0711.3899)

* [[Maxim Kontsevich]], [[Yan Soibelman]], _Stability structures, motivic Donaldson-Thomas invariants and cluster transformations_, [arXiv:0811.2435](http://arxiv.org/abs/0811.2435)

* Rina Anno, Roman Bezrukavnikov, Ivan Mirkovi&#263;, _A thin stringy moduli space for Slodowy slices_, [arxiv/1108.1563](http://arxiv.org/abs/1108.1563) 

* Arend Bayer, Emaneule Macri, _Projectivity and Birational Geometry of Bridgeland Moduli Spaces_ ([arXiv:1203.4613](http://arxiv.org/abs/1203.4613))

* [[Tom Bridgeland]], Ivan Smith, _Quadratic differentials as stability conditions_, [arxiv/1302.7030](http://arxiv.org/abs/1302.7030)
 
* {#Martinez13} Cristian Martinez, _Duality, Bridgeland wall-crossing and flips of secant varieties_ ([arXiv:1311.1183](https://arxiv.org/abs/1311.1183))


### Introduction and review

* {#Bridgeland09} [[Tom Bridgeland]], _Spaces of stability conditions_, Proc. of symposia in pure math. __80__, 2009 ([math/0611510](http://arxiv.org/abs/math/0611510))

* {#Reineke08} Markus Reineke, _Moduli of representations of quivers_ ([arXiv:0802.2147](https://arxiv.org/abs/0802.2147))

* {#Bayer11} Arend Bayer, _A tour to stability conditions on derived categories_, 2011 ([pdf](https://www.maths.ed.ac.uk/~abayer/dc-lecture-notes.pdf))

* [[Daniel Huybrechts]], _Introduction to stability conditions_ ([arXiv:1111.1745](https://arxiv.org/abs/1111.1745))

* Jan Engenhorst, _Bridgeland Stability Conditions in Algebra, Geometry and Physics_, 2014 ([pdf](https://www.freidok.uni-freiburg.de/fedora/objects/freidok:9595/datastreams/FILE1/content))

* {#Stellari15} Paolo Stellari, _A tour on Bridgeland stability_, 2015 ([pdf](https://users.unimi.it/stellari/Research/Slides/LucidiStabCondBeamer.pdf))

### Examples

Discussion of examples of stability conditions 

over [[resolution of singularities|resolutions]] of [[ADE-singularities]]:

* {#Thomas02} R. P. Thomas, _Stability conditions and the braid group_, Communications in Analysis and Geometry 14, 135-161, 2006 ([arXiv:math/0212214](https://arxiv.org/abs/math/0212214))

* {#Bridgeland05} [[Tom Bridgeland]], _Stability conditions and Kleinian singularities_, International Mathematics Research Notices 2009.21 (2009): 4142-4157 ([arXiv:0508257](https://arxiv.org/abs/math/0508257))

* {#IshiiUedaUehara10} Akira Ishii, Kazushi Ueda, Hokuto Uehara, _Stability conditions on $A_n$-singularities_, Journal of Differential Geometry 84 (2010) 87-126 ([arXiv:math/0609551](https://arxiv.org/abs/math/0609551))

* {#BravThomas09} [[Christopher Brav]], Hugh Thomas, _Braid groups and Kleinian singularities_ ([arXiv:0910.2521](https://arxiv.org/abs/0910.2521))

* {#QiuWoold14} [[Yu Qiu]], Jon Woolf, _Contractible stability spaces and faithful braid group actions_ ([arXiv:1407.5986](https://arxiv.org/abs/1407.5986))


* {#Qiu15} [[Yu Qiu]], Def. 2.1 _Stability conditions and quantum dilogarithm identities for Dynkin quivers_, Adv. Math., 269 (2015), pp 220-264 ([arXiv:1111.1010](https://arxiv.org/abs/1111.1010))

* [[Tom Bridgeland]], [[Yu Qiu]], Tom Sutherland, _Stability conditions and the $A_2$ quiver_ ([arXiv:1406.2566](https://arxiv.org/abs/1406.2566))



### Relation to stable branes in string theory
 {#RelationToStableBranesInStringTheory}

The proposal that slope-stability of vector bundles should generalize to a notion of stability ("$\Pi$-stability") of [[B-branes]]/[[D-branes]] originates with

* {#DouglasFiolRomerlsberger00} [[Michael Douglas]], Bartomeu Fiol, Christian Römelsberger, _Stability and BPS branes_, JHEP 0509:006, 2005 ([arXiv:hep-th/0002037](https://arxiv.org/abs/hep-th/0002037))

In terms of stability ($\Pi$-stability) of [[B-branes]] of the [[B-model]] [[topological string]]:

* {#Douglas01} [[Michael Douglas]], _D-branes, categories and $N=1$ supersymmetry, J.Math.Phys. __42__ (2001) 2818&#8211;2843;  

* {#Douglas02} [[Michael Douglas]],  _Dirichlet branes, homological mirror symmetry, and stability_, Proc. ICM, Vol. III (Beijing, 2002), 395&#8211;408, Higher Ed. Press, Beijing, 2002

* {#Aspinwall04} [[Paul Aspinwall]], _D-Branes on Calabi-Yau Manifolds_ ([arXiv:hep-th/0403166](https://arxiv.org/abs/hep-th/0403166))

* [[Aaron Bergman]], _Stability Conditions and Branes at Singularities_,  Journal of High Energy Physics 2008.10 (2008): 07 ([arXiv:hep-th/0702092](http://arxiv.org/abs/hep-th/0702092))

* {#MalyshevVerlinde07} Dmitry Malyshev, [[Herman Verlinde]], _D-branes at Singularities and String Phenomenology_, Nucl.Phys.Proc.Suppl.171:139-163, 2007 ([arXiv:0711.2451](https://arxiv.org/abs/0711.2451))

On marginally stable branes:

* [[Paul Aspinwall]], Alexander Maloney, Aaron Simons, _Black Hole Entropy, Marginal Stability and Mirror Symmetry_, JHEP0707:034, 2007 ([arxiv:hep-th/0610033](https://arxiv.org/abs/hep-th/0610033))



[[!redirects Bridgeland stability conditions]]

[[!redirects Bridgeland stability]]

[[!redirects stability condition]]
[[!redirects stability conditions]]

[[!redirects stability function]]
[[!redirects stability functions]]


