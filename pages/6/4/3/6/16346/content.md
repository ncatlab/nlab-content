

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

While _[[Cartan geometry]]_ was originally conceived of in the context of [[differential geometry]], its principles and constructions make sense much more generally. In particular they make sense in the context of [[supergeometry]]. The implementation of Cartan geometry in supergeometry may well be called _super-Cartan geometry_ or _Cartan super-geometry_. Where the original and motivating example for plain [[Cartan geometry]] was the formulation of [[Einstein gravity]] (via [[pseudo-Riemannian geometry]]), so super-Cartan geometry underlies and finds motivation from the formulation of [[supergravity]], see also the [Survey of (non-)existing literature below](#SurveyOfExistingLiterature).

While the [[abstract general]] [[theory]] of super-Cartan geometry proceeds in direct analogy with that of traditional Cartan geometry, the [[concrete particular]] examples tend to exhibit a richer behaviour. Specifically for the case relevant to [[supergravity]] this is due to two facts:

1. The [[super Euclidean spaces]] and [[super-Minkowski spacetimes]], have, as [[super-translation groups]], [[non-abelian group|non-abelian]] [[supergroup]] structure, which is reflected in the fact that the [[left-invariant 1-forms]] ([[super differential forms]]) on these spaces are _not_ closed. This means that they carry natural intrinsic [[torsion of a G-structure]]. Due to this fact the super-Cartan geometry involved in [[supergravity]] is richer than its bosonic counterpart in a way that goes beyond the addition of "superpartners". For more on this see also at _[[torsion constraints of supergravity]]_.

1. In particular [[super-Minkowski spacetimes]] carry non-trivial exceptional [[super Lie algebra]] [[Lie algebra cohomology|cocycles]]. Their globalization as [[definite forms]] is hence [[analogy|analogous]] to what is known in the bosonic case for instance for [[G2-structure]]. These globalizations play a key role in the discussion of [[super p-brane]] [[sigma-models]] on curved [[supergravity]] backgrounds. Moreover, these cocycles classify [[super L-infinity algebra]] [[L-infinity algebra cohomology|extensions]] of [[super Minkowski spacetime]] known as [[extended super Minkowski spacetimes]]. This is the origin of much of [[higher Cartan geometry]] within super-Cartan geometry.


## Survey of (non-)existing literature
 {#SurveyOfExistingLiterature}

While the specific terminology "super-Cartan geometry" is traditionally not used much  (but see ([Baaklini 77a](#Baaklini77a), [Baaklini 77b](#Baaklini77b), [Egeileh-Chami 13](#EgeilehChami13))), nevertheless the key ingredients of super-Cartan geometry are well known in the literature, and all the more is it useful to make them explicit as what they are.

Physics literature usually refers to the "superspace formulation" of [[supergravity]] when referring to the formulation of the theory in [[supergeometry]] and uses terms such as "Einstein-Cartan theory" to refer to the [[first order formulation of gravity]] (e.g. [Nieuwenhuizen 81](#Nieuwenhuizen81)). But all of the literature on [[supergravity]] formulated this way in "superspace" is implicitly about super-Cartan geometry for the inclusion of a [[spin group]]-[[double cover]] of the [[Lorentz group]] inside a [[super Poincaré group]], in direct analogy to how ordinary [[Einstein gravity]] ([[pseudo-Riemannian geometry]]) is the Cartan geometry of the inclusion of a [[Lorentz group]] inside a plain [[Poincaré group]] -- this in fact being Cartan's original and motivating example for the whole theory. Where physicists speak of "locally gauging [[supersymmetry]]" the mathematical formulation of that is precisely this: the "[[supersymmetry]]" [[supergroup]] is the [[super Poincaré group]] [[action|acting]] on [[super Minkowski spacetime]], and "locally gauging" it means exactly to consider [[spacetimes]] that are locally ([[tangent space]]-wise) modeled on [[super Minkowski space]], while globally varying according to a [[Lorentz group]]-[[G-structure]], hence the super-analog of a [[pseudo-Riemannian metric]]. The main point to be aware of is that physics literature in general tends to by default outright ignore all global issues (such as nontrivial [[principal bundles]]) and instead discuss these only when absolutely necessary as extra phenomena going by names such as _[[instantons]]_ and _[[anomalies]]_.

With this understood, one physics references which explores the super-Cartan-geometric picture of [[supergravity]] in much detail is ([D'Auria-Fre 82](#DAuriaFre82), [Castellani-D'Auria-Fre 91](#CastellaniDAuriaFre91)). (In part I These authors speak of 'Poincar&#233; gravity'. In part II they make even the [[higher Cartan geometry]] hidden here fairly explicit, see there and see at _[[D'Auria-Fré formulation of supergravity]]_). Similarly, discussion of super-[[Klein geometry]] in the context of [[supergravity]] is, even if not exactly in this terminology, rather explicit in ([Figueroa-O'Farrill 08](#FigueroaOFarrill08)). 

An early reference that identifies this [[first order formulation of gravity]] explicitly as a [[Cartan connection]] is ([Baaklini 77a](#Baaklini77a), [Baaklini 77b](#Baaklini77b)), which however seems to have gone unnoticed. (The only non-self citation to this article is in the list of references of the survey ([Nieuwenhuizen 81](#Nieuwenhuizen81)) which however does not actually refer the article in its text.) A much later reference that very clearly identifies the role of the mathematics of supergeometric [[G-structures]] (which is the relevant special class of super-Cartan geometry) in [[supergravity]] in the context of [[supergravity torsion constraints]] is ([Lott 01](#Lott01)). The followup ([Egeileh-Chami 13](#EgeilehChami13)) to that article again makes the terminology "Cartan geometry" fully explicit in this supergeometric context. This last article also observes that from this perspective the traditional concept of _[[Killing spinor]]_ -- which involves an extra "weakening" parameter in addition to the plain concept of a _[[covariantly constant spinor]]_ -- is naturally understood as being in fact a covariantly constant spinor, but for a different model super-[[Klein geometry]] $G/H$.

This provides ample example and application of super-Cartan geometry for the case where $G/H$ is a [[super vector space]], hence for the case corresponding to [[G-structure]]. More general super-Cartan geometry apparently remains to be explored.




## Introduction
 {#Introduction}

It is traditional to introduce [[supergeometry]] as being about [[supermanifolds]] and to introduce the concept of [[supermanifolds]] in the form of [[locally ringed topological spaces]]. There is however a more direct, possibly more illuminating, and certainly more powerful way, following instead the spirit of the discussion at _[[geometry of physics -- smooth sets]]_. 

Below in 

* _[The geometric substance](#TheGeometricSubstance)_

we consider the full [[topos]] of [[supergeometry]] and find how its structure reflects the special qualities of supergeometry. 

Then in 

* _[G-Structure and Cartan geometry](#GStructureAndCartanGeometry)_ 

we discuss how to formulate [[manifolds]] and their [[Cartan geometry]] generally in such a context. Finally in 

* _[Super Cartan geometry](#SuperCartanGeometry)_

we put this together and discuss supermanifolds equipped with super Cartan geometry.



### **1)** The geometric substance
 {#TheGeometricSubstance}

1. _[Coordinate systems: super Cartesian spaces](#CoordinareSystemsSuperCartesianSpaces)_

1. _[The geometric determinations](#TheGeometricDeterminations)_


1. _[Principal bundles and Higher geometry](#PrincipalBundlesAndHigherGeometry)_



#### Coordinate systems: super Cartesian spaces
 {#CoordinareSystemsSuperCartesianSpaces}


Recall the following from the discussion at _[[geometry of physics -- smooth sets]]_. We will set up [[supergeometry]] in direct analogy to this formulation of plain [[differential geometry]].


+-- {: .num_defn #SiteCartSp}
###### Definition

Write [[CartSp]] for the [[category]] of [[Cartesian space]] $\mathbb{R}^n$ for $n \in\mathbb{N}$ with [[smooth functions]] between them. Say that a collection of morphisms $\{U_i \to X\}$ in $CartSp$ is [[covering]] if this is a [[good open cover]] in that every finite non-empty intersection of the charts is [[diffeomorphism|diffeomorphic]] to a Cartesian space.

=--

+-- {: .num_remark}
###### Remark

We may think of this as the category of abstract [[coordinate systems]] on which [[differential geometry]] is to be modeled, see at _[[geometry of physics -- coordinate systems]]_.

=--

+-- {: .num_defn #Smooth0Type}
###### Definition

We say a _[[smooth set]]_ or _smooth 0-type_ is a [[sheaf]] on $CartSp$, write

$$
 Smooth0Type \coloneqq Sh(CartSp) 
$$

for the [[sheaf topos]] of all these.

=--

+-- {: .num_remark}
###### Remark

The useful way to think of def. \ref{Smooth0Type} in the present context is as defining a kind of [[generalized smooth space]] which is _defined_ by which smooth functions from Cartesian spaces it receives (see also at _[[motivation for sheaves, cohomology and higher stacks]]_ for more exposition of this point).

Under the [[Yoneda embedding]] 

$$
  CartSp \hookrightarrow Smooth0Type
$$

every Cartesian space $X$ is naturally regarded as a smooth space itself, namely the one it [[representable functor|represents]] by the assignment

$$
  X \colon \mathbb{R}^n \mapsto C^\infty(\mathbb{R}^n ,X)
  \,.
$$

Hence the set that the Cartesian space $X$, regarded as a sheaf, assigns to a coordinate system $\mathbb{R}^n$ is just the set of all ways of mapping that coordinate system smoothly into $X$.

Hence given any $X \in Smooth0Type$, we are entitled to think of it as a [[generalized smooth space]] which need not be given as a [[set]] equipped with [[smooth structure]], but whose nature instead we detect or _probe_ by mapping Cartesian spaces into it: given  $\mathbb{R}^n$ then we think of the set $X(\mathbb{R}^n)$, which the sheaf $X$ assigns, as playing the role of the set of all smooth functions "$\mathbb{R}^n \longrightarrow X$" into the would-be space $X$. 

The [[Yoneda lemma]] gives that this is not circular, but consistent: once we identify Cartesian spaces themselves as smooth spaces via the [[Yoneda embedding]], then the previous statement becomes literally true and we may remove the quotation marks:

$$
  X(\mathbb{R}^n)
  \simeq
  \left\{
    morphisms\;of\;smooth\;spaces\;
    \mathbb{R}^n \to X
  \right\}
  \,.
$$

=--


+-- {: .num_remark}
###### Remark

The strategy is then to work with this nice category (a [[topos]]) of [[smooth spaces]], and find in their [[subcategories]] of more specific objects having extra properties which one may need in given applications:

$\{$[[coordinate systems]]$\}$ 
 $\hookrightarrow$
$\{$[[smooth manifolds]]$\}$ 
 $\hookrightarrow$
$\{$[[Hilbert manifolds]]$\}$
 $\hookrightarrow$
$\{$[[Banach manifolds]]$\}$
 $\hookrightarrow$
$\{$[[Fréchet manifolds]]$\}$
 $\hookrightarrow$
$\{$[[diffeological spaces]]$\}$ 
 $\hookrightarrow$
$\{$[[smooth spaces]]$\}$ 
 $\hookrightarrow$
$\{$[[orbifold|smooth orbifolds]]$\}$ 
 $\hookrightarrow$
$\{$[[smooth groupoids]]$\}$ 
 $\hookrightarrow $
$\{$[[smooth 2-groupoids]]$\}$ 
 $\hookrightarrow 
 \cdots
 \hookrightarrow $
$\{$[[smooth ∞-groupoids]]$\}$ 

The identification of (super-)[[smooth manifolds]] inside all (super-)[[smooth spaces]] we consider [below](#GStructureAndCartanGeometry).

=--

In view of the above, it is immediate that in order to generalize [[differential geometry]], we should focus on generalizing the category of [[coordinate systems]]. To that end recall a basic fact about [[smooth functions]]:

+-- {: .num_prop #EmbeddingOfSmoothManifoldsIntoFormalDualsOfRAlgebras}
###### Proposition

The [[functor]]

$$
  C^\infty(-) \colon CartSp \longrightarrow CAlg_{\mathbb{R}}^{op}
$$

which sends a [[Cartesian space]] to (the [[formal dual]] of) its $\mathbb{R}$-[[commutative algebra|algebra]] of [[smooth functions]] is a [[full and faithful functor]].


In other words, for two [[Cartesian spaces]] $X,Y$ there is a [[natural bijection]] between the [[smooth functions]] $X \to Y$ and the algebra homomorphisms $C^\infty(X)\leftarrow C^\infty(Y)$.

=--

See at _[[embedding of smooth manifolds into formal duals of R-algebras]]_ for more on this.

+-- {: .num_remark}
###### Remark

One has to be careful that prop. \ref{EmbeddingOfSmoothManifoldsIntoFormalDualsOfRAlgebras} might seem to imply more than it does. In order that all constructions on all commutative algebras have the desired dual effect on formally dual smooth spaces (e.g. construction of [[products]]/[[coproducts]], or construction of [[Kähler differentials]]) one needs to refine plain commutative algebras over $\mathbb{R}$ to _[[smooth algebras]]_. See there for more on this point, which however for our purposes here is not of further concern. 

=--

Now to pass to [[superalgebra]]:

+-- {: .num_remark}
###### Remark

It is an observation from [[experiment]] (from the [[Stern-Gerlach experiment]] via the [[spin-statistics theorem]]), that spaces of [[physical fields]] for [[physical theories]] that contain [[fermions]] behave as if they have [[algebras of functions]] which are not quite [[commutative algebras]], but where the functions depending on the [[fermions]] only commute with each other up to picking up a minus sign. 

=--

+-- {: .num_defn}
###### Definition

A _[[super-commutative superalgebra]]_ (or just _[[commutative superalgebra]]_ for short)  is a $\mathbb{Z}/2\mathbb{Z}$-[[graded algebra|graded]] [[associative algebra]] $A = A_{even} \oplus A_{odd}$ such that for $a,b$ any two elements in homogeneous degree $deg(a), deg(b)\in \mathbb{Z}/2\mathbb{Z}$, then their product is related by ([[Ausdehnunglehre|Grassmann 1844, §37, §55]])

$$
  a \cdot b = (-1)^{deg(a) deg(b)} b \cdot a
  \,.
$$

Write $SuperCAlg_{\mathbb{R}}$ for the [[category]] of commutative superalgebras over $\mathbb{R}$.

=--

+-- {: .num_defn #SuperCartesianSpace}
###### Definition

For $q\in \mathbb{N}$, the real [[Grassmann algebra]] 

$$
  C^\infty(\mathbb{R}^{0|q})
  \coloneqq
  \wedge^\bullet \langle \theta^1, \cdots, \theta^q\rangle
$$ 

is the $\mathbb{R}$-algebra [[free functor|freely]] generated from $q$ generators $\{\theta^i\}_{i = 1}^q$ subject to the relation 

$$
  \theta^i \theta^j = - \theta^j \theta^i
  \,.
$$

For $p,q \in \mathbb{N}$, the [[super-Cartesian space]] $\mathbb{R}^{p|q}$ is the [[formal dual]] of the commutative superalgebra written 
 $C^\infty(\mathbb{R}^{p|q})$ whose underlying 
$\mathbb{Z}/2\mathbb{Z}$-[[graded vector space]] is


$$
  C^\infty(\mathbb{R}^{p|q})
  \coloneqq
  C^\infty(\mathbb{R}^p) \otimes_{\mathbb{R}} \wedge^\bullet\langle\theta^1, \cdots, \theta^q\rangle 
$$

with the product given by the relations

$$
  \begin{aligned}
  \left(
    f \theta^{i_1}\cdots \theta^{i_k}
  \right)
  \left(
    g \theta^{j_1}\cdots \theta^{j_l}
  \right)
  & =
  f \cdot g \; \theta^{i_1}\cdots \theta^{i_k} \theta^{j_1}\cdots \theta^{j_l}
  \\
  & = 
  (-1)^{k l} g\cdot f \; \theta^{j_1}\cdots \theta^{j_l} \theta^{i_1}\cdots \theta^{i_k}
  \end{aligned}
$$

where $f \cdot g$ is the ordinary pointwise product of [[smooth functions]].

Write

$$
 SuperCartSp \hookrightarrow SuperCAlg_{\mathbb{R}}^{op}
$$

for the [[full subcategory]] of the [[opposite category]] of [[commutative superalgebras]] on those of this form. We write 
$\mathbb{R}^{p|q} \in SuperCartSp$ for the [[formal dual]] of 
$C^\infty(\mathbb{R}^{p|q})$.

=--


+-- {: .num_defn}
###### Definition

Say that a collection of morphisms $\{U_i \to X\}$ in $SuperCartSp$ is [[covering]] if all $U_i$ and the $X$ are $\mathbb{R}^{p|q}$ (for the same $p$ and $q$), the morphisms are the identity on the odd generators $\{\theta_i\}$, and the underlying map of [[Cartesian spaces]] is a [[good open cover]] in the sense of def. \ref{SiteCartSp}. Write

$$
  SuperSmooth0Type \coloneqq Sh(SuperCartSp)
$$

for the [[sheaf topos]] over that site. We call this the collection of _[[smooth super spaces]]_.

=--

This is the [[topos]] that hosts traditional [[supergeometry]]. However for our purposes it is useful to refine this a little more to a context for [[synthetic differential supergeometry]]. To that end first observe that

+-- {: .num_remark}
###### Remark

The even-degree part $C^\infty(\mathbb{R}^{p|q})_{even}$ is an ordinary [[commutative algebra]], but if $q \geq 1$ then it is not the algebra of functions on any [[smooth manifold]], because it has a non-trivial [[nilpotent ideal]]. Instead, a nilpotent element of an [[algebra of functions]] may be thought of as a function depending on an _infinitesimal direction_.

For instance $C^\infty(\mathbb{R}^{0|2})_{even}$ is isomorphic to what is known as the [[algebra of dual numbers]] $(\mathbb{R}\oplus \epsilon \mathbb{R})/(\epsilon^2)$ with $\epsilon = \theta^1 \theta^2$.

This is traditionally more familiar from the theory of [[formal schemes]], but the same kind of general abstract theory goes through in the context of [[differential geometry]], a point of view known as _[[synthetic differential geometry]]_.
 
But this means that in passing to commutative superalgebras there are _two_ stages of generalizations of plain differential geometry involved:

1. [[smooth manifolds]] are generalized to [[formal smooth manifolds]];

1. [[formal smooth manifolds]] are further generalized to formal smooth [[supermanifolds]].

=--

It will be useful to make this explicit.


+-- {: .num_defn}
###### Definition

Write 

$$
  InfPoint \hookrightarrow CAlg_{\mathbb{R}}^{op}
$$ 

for the [[full subcategory]] of the [[opposite category]] of [[commutative algebras]] over $\mathbb{R}$ on [[formal duals]] of [[commutative algebras]] over the [[real numbers]] of the form $\mathbb{R}\oplus V$ with $V$ a finite-dimensional  [[nilpotent ideal]]. We call this the category of _[[infinitesimally thickened points]]_.

Write moreover

$$
  CartSp \rtimes InfPoint \hookrightarrow CAlg_{\mathbb{R}}^{op}
$$

for the [[full subcategory]] on [[formal duals]] of those algebras which are [[tensor products]] of commutative $\mathbb{R}$-algebras of the form

$$
  C^\infty(\mathbb{R}^n) \otimes C^\infty(D)
$$

of algebras $C^\infty(\mathbb{R}^p)$ of [[smooth functions]] $\mathbb{R}^n$ as in def. \ref{EmbeddingOfSmoothManifoldsIntoFormalDualsOfRAlgebras} with algebras corresponding to infinitesimally thickened points $D$ as above.

The [[sheaf topos]]

$$
  FormalSmooth0Type \coloneqq Sh(CartSp \rtimes InfPoint)
$$

is traditionally known as the _[[Cahiers topos]]_.

=--

+-- {: .num_example}
###### Example

Write $\mathbb{D}$ for the [[formal dual]] of the [[algebra of dual numbers]]. Then morphisms


$$
  \mathbb{R}^n \times \mathbb{D}\longrightarrow \mathbb{R}^n
$$

which are the identity after restriction along $\mathbb{R}^n \to \mathbb{R}^n \times \mathbb{D}$, are equivalently algebra homomorphisms of the form


$$
  (C^\infty(\mathbb{R}^n)\otimes_{\mathbb{R}} \wedge^\bullet \langle \epsilon\rangle
  \longleftarrow
  C^\infty(\mathbb{R}^n)
$$

which are the identity modulo $\epsilon$. Such a morphism has to take any function $f \in C^\infty(\mathbb{R}^n)$ to 

$$
  f + (\partial f) \epsilon
$$

for some smooth function $(\partial f) \in C^\infty(\mathbb{R}^n)$. The condition that this assignment makes an algebra homomorphism is equivalent to the statement that for all $f_1,f_2 \in C^\infty(\mathbb{R}^n)$

$$
  (f_1 f_2 + (\partial (f_1 f_2))\epsilon )
  =
  (f_1 + (\partial f_1) \epsilon)
  (f_2 + (\partial f_2) \epsilon)
  \,.
$$

Multiplying this out and using that $\epsilon^2 = 0$ this in turn is equivalent to

$$
  \partial(f_1 f_2) = (\partial f_1) f_2 + f_1 (\partial f_2)
  \,.
$$

This in turn means equivalently that $\partial\colon C^\infty(\mathbb{R}^n)\to C^\infty(\mathbb{R}^n)$ is a [[derivation]]. But derivations of algebras of [[smooth functions]] are equivalent to [[vector fields]]. (See at _[[derivations of smooth functions are vector fields]]_).

In particular one finds that maps

$$
  \mathbb{D} \longrightarrow \mathbb{R}^n
$$

are equivalently single [[tangent vectors]].



=--

+-- {: .num_defn}
###### Definition

Write  

$$
  SuperInfPoint \hookrightarrow SuperCAlg_{\mathbb{R}}^{op}
$$ 

for the [[full subcategory]] on those [[formal duals]] of [[commutative superalgebras]] over the [[real numbers]] on those of the form $\mathbb{R}\oplus V$ with $V$ a finite dimensional [[nilpotent ideal]].

We call this the category of [[infinitesimally thickened point|infinitesimally thickened]] [[superpoints]].

Similarly write

$$
  CartSp \rtimes SuperInfPoint
  \hookrightarrow
  SuperCAlg_{\mathbb{R}}^{op}
$$ 

for the [[full subcategory]] on [[formal duals]] of [[tensor products]] of an algebra $C^\infty(\mathbb{R}^n)$ of [[smooth functions]] and an algebra $C^\infty(D)$ on an infinitesimally thickened superpoint.

The [[sheaf topos]]

$$
  SuperSmooth0Type \coloneqq Sh(CartSp \rtimes SuperInfPoint)
$$

we call that of [[super smooth infinity-groupoid|super formal smooth spaces]].

=--


#### The geometric determinations 
 {#TheGeometricDeterminations}

The [[sites]] considered above are related by a sequence of [[reflective 
subcategory|reflections]] and [[coreflective subcategory|coreflections]] as follows

+-- {: .num_defn #InclusionOfSites}
###### Definition

Write

$$
  \ast \hookrightarrow CartSp
  \hookrightarrow
  CartSp\rtimes InfPoint
  \hookrightarrow
  CartSp \rtimes SuperInfPoint 
$$

for the evident [[full inclusions]]:

1. the first one picks the [[terminal object]] $\mathbb{R}^0$;

1. the second one regards $\mathbb{R}^n$ as a [[formal manifold]] equipped with no infinitesimal thickening;

1. the third one regards $\mathbb{R}^n \times D$ as a supergeometric space with no odd-graded (no fermionic) component.

=--


+-- {: .num_prop #CoReflectionsOfSites}
###### Proposition

The full inclusions of def. \ref{InclusionOfSites} have [[adjoints]] as follows

$$
  \ast
  \stackrel{\longleftarrow}{\hookrightarrow}
  CartSp
  \stackrel{\hookrightarrow}{\longleftarrow}
  CartSp\rtimes InfPoint
  \stackrel{\longleftarrow}{\stackrel{\hookrightarrow}{\longleftarrow}}
  CartSp \rtimes SuperInfPoint  
  \,,
$$

where we display [[left adjoints]] vertically above their [[right adjoints]]. In other words the first inclusion is [[reflective subcategory|reflective]], the second is [[coreflective subcategory|coreflective]] and the third is both.

Explicitly, 

1. the first reflection is, necessarily, the trivial one;

1. the second coreflection is [[reduction]]: it sends a [[commutative algebra]] to the [[quotient]] by its [[nilpotent ideal]];

1. the third reflection sends a $\mathbb{Z}/2\mathbb{Z}$-graded algebra to its even-graded part, the co-reflection sends a $\mathbb{Z}_2$-graded algebra to its quotient by the ideal generated by its odd part, see at _[superalgebra -- Adjoints to the inclusion of plain algebras](super+algebra#AdjointsToInclusionOfPlainAlgebra)_.

=--

All the (co-)reflections in prop. \ref{CoReflectionsOfSites} are immediate in themselves, but, as with all [[adjunctions]], it is useful to make them explicit as such. For the last one possibly the only place in the literature where it is made explicit is [Carchedi-Roytenberg 12, example 3.18](http://ncatlab.org/nlab/show/super+algebra#CarchediRoytenberg12).

+-- {: .num_prop #CoReflectonsOfToposes}
###### Proposition

Passing to [[categories of sheaves]], the (co-)reflections on [[sites]] in prop. \ref{CoReflectionsOfSites} yields, via [[Kan extension]], a sequence of [[adjoint quadruples]] as follows:

$$
  \array{
    & && && &\longleftarrow& 
    \\
    & && &\hookrightarrow& &\hookrightarrow& 
    \\
    & &\longleftarrow& &\longleftarrow& &\longleftarrow&
    \\
    \Delta \colon
    & 
    Set
    &\hookrightarrow&
    Smooth0Type
    &\hookrightarrow&
    FormalSmooth0Type
    &\hookrightarrow&
    SuperFormalSmooth0Type
    \\
    & &\longleftarrow& &\longleftarrow&
    \\
    & &\hookrightarrow&
  }
$$

=--

+-- {: .proof}
###### Proof

For the first adjoint quadruple on the left this is the statement that [[smooth spaces]] form a [[cohesive topos]], which follows as discussed there and at _[[cohesive site]]_. 

For the second adjoint quadruple this is the statement that the [[Cahiers topos]] has [[differential cohesion]] relative to that of [[smooth spaces]], as discussed at _[[formal smooth infinity-groupoids]]_.

For the third adjoint quadruple this is the statement that [[super formal smooth infinity-groupoids|super formal smooth spaces]] exhibits [[graded differential cohesion]] over formal smooth spaces.

=--

For convenience, from now on we notationally abbreviate:

$$
  \mathbf{H} \coloneqq SuperFormalSmooth0Type
  \,.
$$

+-- {: .num_remark #FromAdjunctionsToMonads}
###### Remark

Any [[reflective subcategory]]

$$
  \mathcal{C}
  \stackrel{\overset{L}{\longleftarrow}}{\underset{i}{\hookrightarrow}}
  \mathbf{H}
$$

induces an [[idempotent monad]] on $\mathbf{H}$, i.e. an [[endofunctor]]

$$
  \bigcirc \;\coloneqq\; i \circ L \;\colon\; \mathbf{H} \longrightarrow \mathbf{H}
$$

equipped with a [[natural transformation]]

$$
  \epsilon_X \;\colon\; X \longrightarrow \bigcirc X
$$

such that applying $\bigcirc$ again to that transformation it becomes an [[isomorphism]].

Dually, any [[coreflective subcategory]]

$$
  \mathcal{C}
  \stackrel{\overset{i}{\hookrightarrow}}{\underset{R}{\longleftarrow}}
  \mathbf{H}
$$

induces an [[idempotent comonad]]

$$
  \Box \;\coloneqq\; i \circ R \;\colon\; \mathbf{H} \longrightarrow \mathbf{H}
  \,.
$$

If moreover these two cases combine to an [[adjoint triple]] of the form

$$
  \mathcal{C}
   \stackrel{\hookrightarrow}{\stackrel{\longleftarrow}{\hookrightarrow}}
  \mathbf{H}
$$

or of the form

$$
  \mathcal{C}
   \stackrel{\longleftarrow}{\stackrel{\hookrightarrow}{\longleftarrow}}
  \mathbf{H}
$$


then these (co-)monads themselves are [[adjunction|adjoint]] to each other as

$$
  \Box \dashv \bigcirc
$$

or as

$$
  \bigcirc \dashv \Box
  \,,
$$

respectively, forming an "[[adjoint cylinder]]".





=--

Notice the following:

+-- {: .num_prop }
###### Proposition

The total composite labeled $\Delta$ in prop. \ref{CoReflectonsOfToposes}
is indeed the [[locally constant sheaf]]-functor for $SuperFormalSmooth0Type$.

=--

+-- {: .proof}
###### Proof

Let $X$ be any object in image of this total functor, and let $U \times D_s \in CartSp \rtimes SupeInfPoint$. Then by adjunction $SuperFormalSmooth0Type(U\times D_s, X)$ is equivalently homs in $FormalSmooth0Type$ out of the dual of the Weil algebra which is the quotient of the original one by the ideal generated by its odd part. Hence this, in turn, is equivalently homs in $Smooth0Type$ out of $U$ and that finally is equivalently homs in $Set$ out of $\ast$ into the given set.

=--

+-- {: .num_cor #SystemOfModalities}
###### Corollary

Passing, via remark \ref{FromAdjunctionsToMonads}, from the sequence of [[adjoint quadruples]] in prop. \ref{CoReflectonsOfToposes}, yields the following system of [[adjoint triples]] of [[idempotent monads]] and [[idempotent comonads]]:


$$
  \array{
    && id &\dashv& id 
    \\
    && \vee && \vee
    \\
    &\stackrel{fermionic}{}& \e &\dashv& \rightsquigarrow & \stackrel{bosonic}{}
    \\
    && \bot && \bot
    \\
    &\stackrel{bosonic}{} & \rightsquigarrow &\dashv& \R & \stackrel{rheonomic}{}
    \\
    && \vee && \vee
    \\
    &\stackrel{reduced}{} & \Re &\dashv& \Im & \stackrel{infinitesimal}{}
    \\
    && \bot && \bot
    \\
    &\stackrel{infinitesimal}{}& \Im &\dashv& \& & \stackrel{\text{&#233;tale}}{}
    \\
    && \vee && \vee
    \\
    &\stackrel{contractible}{}& &#643; &\dashv& \flat & \stackrel{discrete}{}
    \\
    && \bot && \bot
    \\
    &\stackrel{discrete}{}& \flat &\dashv& \sharp & \stackrel{differential}{}
    \\
    && \vee && \vee
    \\
    && \emptyset &\dashv& \ast
  }
$$

where $\vee$ denotes inclusion of [[modal types]].

=--

We pronounce the operations in corollary \ref{SystemOfModalities} as follows.

* [[solidity]]

  * **[[fermionic modality]] $\e$** -- the spaces it sends to the point are purely fermionic, the [[odd line]];

  * **[[bosonic modality]] $\rightsquigarrow$** -- sends a super-space to the underlying bosonic space;

  * **[[rheonomy modality]] $\R$**;

* [[elasticity]]

  * **[[reduction modality]] $\Re$** -- removes infinitesimal thickening;
 
  * **[[infinitesimal shape modality]] $\Im$** -- sends a space to its [[de Rham space]];

  * **[[infinitesimal flat modality]] $\&$**;

* [[cohesion]]
  
  * **[[shape modality]]  $\int$** -- sends a space to its set $\pi_0$ of [[connected components]]; or rather, once we lift the discussion here from [[sheaves]] to [[infinity-stacks]], then this sends a space to its [[fundamental infinity-groupoid]];

  * **[[flat modality]] $\flat$** -- sends a space to the [[discrete space]] formed by its points;

  * **[[sharp modality]] $\sharp$**.



+-- {: .num_example }
###### Example

* For $X \in SmoothMfd \hookrightarrow Smooth0Type \hookrightarrow FormalSmooth0Type \hookrightarrow SuperFormalSmooth0Type$  any ordinary [[smooth manifold]], this is a [[bosonic modality|bosonic]] [[modal type]] $\stackrel{\rightsquigarrow}{X} \simeq X$.

* The [[odd line]] $\mathbb{R}^{0|1}$ is purely [[fermionic modality|fermionic]] in that it is an $\e$-[[comodal type]]: $\e(\mathbb{R}^{0|1})\simeq \ast$.

* All [[super Cartesian spaces]] $\mathbb{R}^{p|q}$ have [[contractible]] [[shape]] in that $\int \mathbb{R}^{p|q} \simeq \ast$.

=--

By applying [[universal constructions]] to the [[unit of a monad|units]]/[[counit of a comonad|counits]] of these [[modalities]], we obtain various further operations that will be useful

+-- {: .num_defn #InfinitesimalDiskBundle}
###### Definition

Given $X \in \mathbf{H}$, its _infinitesimal disk bundle_ $T_{inf} X\to X$
is the [[pullback]] of the [[unit of a monad|unit]] of the 
[[infinitesimal shape modality]] along itself

$$
  \array{
    T_{inf} X &\stackrel{}{\longrightarrow}& X
    \\
    \downarrow && \downarrow
    \\
    X &\longrightarrow& \Im X
  }
  \,.
$$

Given a point $x \;\colon\;  \ast \to X$, then the [[infinitesimal neighbourhood]] 
$\ast \to \mathbb{D}_x \to X$ of that point is the further [[pullback]] of the infinitesimal disk bundle to this point:

$$
  \array{
    \mathbb{D}_x &\longrightarrow & T_{inf} X &\stackrel{}{\longrightarrow}& X
    \\
    \downarrow && \downarrow && \downarrow
    \\
    \ast &\stackrel{x}{\longrightarrow} & X &\longrightarrow& \Im X
  }
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

This is the input for the formulation of [[frame bundles]] below around 
prop. \ref{FrameBundle}.

=--

It is natural not to pick any point, but to collect all infinitesimal disks around _all_ the points of a space:

+-- {: .num_defn #RelativeFlat}
###### Definition

The _[[relative shape modality]]_ is the operation $\flat^{rel}$ that sends $X \in \mathbf{H}$ to the [[homotopy pullback]]

$$
  \array{
    \flat^{rel} &\longrightarrow& X
    \\
    \downarrow && \downarrow
    \\
    \flat X &\longrightarrow& \Im X
  }
  \,.
$$ 

=--

There are some further relations between the modalities to take note of:

+-- {: .num_prop #Sublations}
###### Proposition
 
We have the following [[Aufhebung]]-relations:

* $\sharp \emptyset \simeq \emptyset$ (the [[codiscrete objects]] form a [[dense subtopos]])

* $\rightsquigarrow \Im \simeq \Im$.

=--

+-- {: .proof}
###### Proof

For any $X \in \mathbf{H}$ and any $U \times D_s\in CartSp \rtimes SuperInfPoint \hookrightarrow \mathbf{H}$ we have by [[adjunction]] [[natural equivalences]]

$$
  \begin{aligned}
    \mathbf{H}(U \times D_s , \stackrel{\rightsquigarrow}{\Im X})
    & \simeq
    \mathbf{H}(\e(U \times D_s) , \Im X)
    \\
    &\simeq 
    \mathbf{H}(\Re(\e(U \times D_s)) , X)
    \\
    & \simeq
    \mathbf{H}(U, X)
    \\
    & \simeq
    \mathbf{H}(\Re(U \times D_s), X)
    \\
    & \simeq \mathbf{H}(U \times D_s, \Im X)
  \end{aligned}
  \,.
$$

=--

#### Principal bundles and Higher geometry 
 {#PrincipalBundlesAndHigherGeometry}


The point of the system of modalities in corollary \ref{SystemOfModalities} is that they allow to carry various geometric [[theory]] across different [[models]] of geometry. If we formulate traditional [[Cartan geometry]] in $FormalSmooth0Type$ with just these operations, then we may just carry that verbatim to $SuperFormalSmooth0Type$ to get a theory of super-Cartan geometry. This we get to below.

In the same vein, we may increase the $n$ in $SuperFormalSmooth n Type$ to $n \gt 0$ and get [[higher Cartan geometry]]. 

In fact at least $ n \geq 1$ is necessary in order to formalize [[frame bundles]] via their [[modulating morphisms]] to the [[delooping]] $\mathbf{B}GL(V)$. The case $n = 1$ is obtained by replacing in the above [[sheaves]] of [[sets]] with [[stacks]] of [[groupoids]]. The case $n = \infty$ is obtained by further refining this to [[infinity-stacks]] of [[infinity-groupoids]].

Here we just recall some bare minimum of this [[higher differential geometry]], for formulating Cartan geometry we need to speak of [[frame bundles]] and hence here we mainly need the concept of [[principal infinity-bundle]], for more see at _[[geometry of physics -- principal bundles]]_.

+-- {: .num_prop}
###### Proposition

The [[(infinity,1)-category theory]] [[analogy|analog]] of prop. \ref{CoReflectonsOfToposes} still holds, and produces via the direct analog corollary \ref{SystemOfModalities} a system of [[modal operators]] on $\mathbf{H} =$ [[SuperFormalSmooth?Type]].


=--


+-- {: .num_prop}
###### Proposition

For $G$ a [[group object]] ([[∞-group]]), the $G$-[[principal infinity-bundle|principal bundles]] $P \to X$ on any $X$ are equivalent to morphisms $X \longrightarrow \mathbf{B}G$ into the [[delooping]] object of $G$, the equivalence being established by sending such a morphism to its [[homotopy fiber]]

$$
  \array{
    P &\longrightarrow & \ast
    \\
    \downarrow && \downarrow
    \\
    X &\longrightarrow& \mathbf{B}G
  }
  \,.
$$

=--


### **2)** General Cartan geometry
 {#GStructureAndCartanGeometry}

Given a [[topos]] of [[differential cohesion]] $\mathbf{H}$ as in corollary \ref{SystemOfModalities} above (hence an [[elastic]] [[substance]]), then on general abstract grounds there is -- and that's the point of this axiomatic formulation -- a good concept and theory of _$V$-[[manifolds]]_ and  _[[G-structures]]_ on these. Applied to the case of [[supergeometry]] as established in prop. \ref{CoReflectonsOfToposes} this hence yields a theory of $G$-structures on $V$-manifolds in supergeometry, and hence of [[Cartan geometry]] modeled on the inclusion $G \to G \rtimes V$. Here we recall the elements of [[abstract general]] [[Cartan geometry]] formulated axiomatically this way. Below in _[Super Cartan geometry](#SuperCartanGeometry)_ we then specify to the [[concrete particular]] super Cartan 
geometry.

1. _[V-Manifolds](#Manifolds)_

1. _[Frame bundles](#FrameBundles)_

1. _[G-Structure](#GStructure)_


#### $V$-Manifolds
 {#Manifolds}

+-- {: .num_defn #LocalDiffeomorphisms}
###### Definition

Given $X,Y\in \mathbf{H}$ then a morphism $f \;\colon\; X\longrightarrow Y$ is a _[[local diffeomorphism]]_ if its naturality square of the [[infinitesimal shape modality]]

$$
  \array{
    X &\longrightarrow& \Im X
    \\
    \downarrow^{\mathrlap{f}} && \downarrow^{\mathrlap{\Im f}}
    \\
    Y &\longrightarrow& \Im Y
  }
$$

is a [[pullback]] square. 

=--

+-- {: .num_remark}
###### Remark

The abstract definition \ref{LocalDiffeomorphisms} comes down to being the appropriate [[synthetic differential supergeometry]]-version  of the traditional statement that $f$ is a [[local diffeomorphism]] if the diagram of [[tangent bundles]]

$$
  \array{
    T X &\longrightarrow& X
    \\
    \downarrow^{\mathrlap{T f}} && \downarrow^{\mathrlap{f}}
    \\
    T Y &\longrightarrow& Y
  }
$$

To see this, notice by the discussion at _[[synthetic differential geometry]]_ that for $D$ an [[infinitesimally thickened point]], then for any $X \in \mathbf{H}$ the [[mapping space]] $[D,X]$ is the [[jet bundle]] of $X$ with jets of order as encoded by the infinitesimal order of $D$. In particular if $\mathbb{D}^1(1)$ is the first order infinitesimal interval defined by the fact that its [[algebra of functions]] is the [[algebra of dual numbers]] $C^\infty(\mathbb{D}^1(1)) = (\mathbb{R} \oplus \epsilon \mathbb{R})/(\epsilon^2)$, and $X$ is a [[smooth manifold]], then 

$$
  [\mathbb{D}^1(1), X]\simeq T X
$$

is the ordinary [[tangent bundle]] of $X$. Now use that the [[internal hom]] $[D,-]$ preserves [[limits]] in its second argument, and that, by the hom-adjunction, $\mathbf{H}(U, [D,X]) \simeq \mathbf{H}(U \times D, X)$ and finally use that $\mathbf{H}(U \times D, \Im X)\simeq \mathbf{H}(\Re(U \times D), X)\simeq \mathbf{H}(U,X)$.


=--

Let now $V \in \mathbf{H}$ be given, equipped with the structure of a [[group]] ([[infinity-group]]).

+-- {: .num_defn #VManifold}
###### Definition

A _$V$-[[manifold]]_ is an $X \in \mathbf{H}$ such that there exists a _$V$-[[atlas]]_, namely a [[correspondence]] of the form

$$
  \array{
    && U
    \\
    & \swarrow && \searrow
    \\
    V && && X
  }
$$

with both morphisms being [[local diffeomorphisms]], def. \ref{LocalDiffeomorphisms}, and the right one in addition being an [[epimorphism]], hence an [[atlas]].

=--


+-- {: .num_prop}
###### Proposition

If $f \;\colon\; X \longrightarrow Y$ is a [[local diffeomorphism]],
def. \ref{LocalDiffeomorphisms}, then so is image
$\stackrel{\rightsquigarrow}{f}\colon \stackrel{\rightsquigarrow}{X} \longrightarrow \stackrel{\rightsquigarrow}{Y}$ under the [[bosonic modality]].

=--

+-- {: .proof}
###### Proof

Since the [[bosonic modality]] provides [[Aufhebung]] for $\Re\dashv \Im$ by prop. \ref{Sublations} we have $\rightsquigarrow \Im \simeq \Im$. Moreover $\Im \rightsquigarrow \simeq \Im$ anyway. Finally $\rightsquigarrow$ preserves [[pullbacks]] (being in particular a [[right adjoint]]). Hence hitting a pullback diagram

$$
  \array{
    X &\longrightarrow& \Im X
    \\
    \downarrow^{\mathrlap{f}} && \downarrow^{\mathrlap{\Im f}}
    \\
    Y &\longrightarrow& \Im Y
  }
$$

with $\rightsquigarrow\;\;$ yields a pullback diagram

$$
  \array{
    \stackrel{\rightsquigarrow}{X} &\longrightarrow& \Im \stackrel{\rightsquigarrow}{X}
    \\
    \downarrow^{\mathrlap{\stackrel{\rightsquigarrow}{f}}} && \downarrow^{\mathrlap{\Im \stackrel{\rightsquigarrow}{f}}}
    \\
    \stackrel{\rightsquigarrow}{Y} &\longrightarrow& \Im \stackrel{\rightsquigarrow}{Y}
  }
$$

=--

+-- {: .num_cor }
###### Corollary

The bosonic space $\stackrel{\rightsquigarrow}{X}$ underlying 
a $V$-manifold $X$, def. \ref{VManifold}, is a $\stackrel{\rightsquigarrow}{V}$-manifold

=--

#### Frame bundles
 {#FrameBundles}

+-- {: .num_defn #GeneralLinearGroup}
###### Definition

The _[[general linear group]]_ $GL(V)$ is the [[automorphism infinity-group]] of the [[infinitesimal neighbourhood]] $\mathbb{D}^V_e$, def. \ref{InfinitesimalDiskBundle}, of the neutral element $e \colon \ast \to \mathbb{D}^V_e \to V$:

$$
  GL(V) \coloneqq \mathbf{Aut}(\mathbb{D}^V_e)
  \,.
$$

=--

+-- {: .num_prop #FrameBundle}
###### Proposition

For $X$ a $V$-manifold, def. \ref{VManifold}, then its infinitesimal disk bundle $T_{inf} X \to X$,
def. \ref{InfinitesimalDiskBundle}, is [[associated infinity-bundle|associated]]
to a $GL(V)$-[[principal infinity-bundle|principal]] $Fr(X) \to X$ -- to be called the _[[frame bundle]]_, [[modulating morphism|modulated]] by a map to be called $\tau_X$, producing [[homotopy pullbacks]] of the form

$$
  \array{
     T_{inf} X &\longrightarrow& V/GL(V)
     \\
     \downarrow && \downarrow
     \\
     X &\stackrel{\tau_X}{\longrightarrow}& \mathbf{B} GL(V)
  }
  \;\;\;
  \array{
     Fr(X) &\longrightarrow& \ast
     \\
     \downarrow && \downarrow
     \\
     X &\stackrel{\tau_X}{\longrightarrow}& \mathbf{B} GL(V)
  }
  \,.
$$

=--

+-- {: .num_defn #Framing}
###### Definition

A [[framing]] of a $V$-manifold is a trivialization of its [[frame bundle]], prop. \ref{FrameBundle}, hence a diagram in $\mathbf{H}$ of the fomr

$$
  \array{
    X && \longrightarrow && \ast
    \\
    & \searrow &\swArrow& \swarrow
    \\
    && \mathbf{B}GL(V)
  }
$$


=--

+-- {: .num_remark #ModuliForFramings}
###### Remark

It is useful to express def. \ref{Framing} in terms of the [[slice topos]] $\mathbf{H}_{/\mathbf{B}GL(V)}$. Write $V\mathbf{Frame}\in \mathbf{H}_{/\mathbf{B}GL(V)}$ for the canonical morphism $\ast \to \mathbf{B}GL(V)$ regarded as an object in the slice. Then a framing as in def. \ref{Framing} is equivalently a morphism

$$
  \phi \colon \tau_X \longrightarrow V\mathbf{Frame}
$$

in $\mathbf{H}_{/\mathbf{B}GL(V)}$.

=--

+-- {: .num_prop #LeftTranslationFraming}
###### Proposition

The[[group object]] $V$, canonically regarded as a $V$-manifold, carries a canonical framing, def. \ref{Framing}, $\phi_{li}$, induced by left translation. 

=--

#### $G$-Structure
 {#GStructure}

+-- {: .num_defn #GStructure}
###### Definition

Given a homomorphism of groups $G \longrightarrow GL(V)$, a _[[G-structure]]_ on a $V$-manifold $X$ is a lift $\mathbf{c}$ of the [[frame bundle]] $\tau_X$ of prop. \ref{FrameBundle} through this map

$$
  \array{
    X && \stackrel{}{\longrightarrow} && G
    \\
    & {}_{\mathllap{\tau_X}}\searrow &\swArrow& \swarrow
    \\
    && \mathbf{B}GL(V)
  }
  \,.
$$

=--

+-- {: .num_remark #ModuliForGStructures}
###### Remark

As in remark \ref{ModuliForFramings}, it is useful to express def. \ref{GStructure} in terms of the [[slice topos]] $\mathbf{H}_{/\mathbf{B}GL(V)}$. Write $G\mathbf{Struc}\in \mathbf{H}_{/\mathbf{B}GL(V)}$ for the given map $\mathbf{B}G\to \mathbf{B}GL(V)$ regarded as an object in the slice. Then a $G$-structure according to def. \ref{GStructure} is equivalently a choice of morphism in $\mathbf{H}_{/\mathbf{B}GL(V)}$ of the form

$$
  \mathbf{c} \;\colon\; \tau_X \longrightarrow G\mathbf{Struc}
  \,.
$$

In other words, $G\mathbf{Struc} \in \mathbf{H}_{/\mathbf{B}GL(v)}$ is the _[[moduli stack]]_ for $G$-structures.

=--

+-- {: .num_example #GStructureFromLeftTranslationFraming}
###### Example

A choice of [[framing]] $\phi$, def. \ref{Framing}, on a $V$-manifold $X$ induces a [[G-structure]] for any $G$, given by the [[pasting diagram]] in $\mathbf{H}$

$$
  \array{
     X &\longrightarrow& \ast &\longrightarrow&
     \\
     & \searrow & \downarrow & \swarrow
     \\
     && \mathbf{B}GL(V)
  }
$$

or equivalently, via remark \ref{ModuliForFramings} and remark \ref{ModuliForGStructures}, given as the [[composition]]

$$
  \mathbf{c}_{li}
  \;\colon\;
  \tau_X \stackrel{\phi}{\longrightarrow} V\mathbf{Frame} \longrightarrow G\mathbf{Struc}\,.
$$

We call this the _left invariant $G$-structure_.

=--

+-- {: .num_defn #IntegrabilityOfGStructure}
###### Definition

For $X$ a $V$-manifold, then 
a [[G-structure]] on $X$, def. \ref{GStructure}, is 
_[[integrable G-structure|integrable]]_ if for any $V$-[[atlas]] $V \leftarrow U \rightarrow X$  the pullback of the $G$-structure on $X$ to $V$ is equivalent there to  the left-inavariant $G$-structure on $V$ of example \ref{GStructureFromLeftTranslationFraming}, i.e. if we have an [[correspondence]] in the double [[slice topos]] $(\mathbf{H}_{/\mathbf{B}GL(V)})_{/G\mathbf{Struc}}$ of the form

$$
  \array{
     && \tau_U
     \\
     & \swarrow && \searrow
     \\
     \tau_V && \swArrow && \tau_X
     \\
     & {}_{\mathllap{\mathbf{c}_{li}}}\searrow && \swarrow_{\mathrlap{\mathbf{c}}}
     \\
     && G \mathbf{Struc}
  }
  \,.
$$

The $G$-structure is _infintesimally integrable_ if this holds true at at after restriction along the [[relative shape modality]] $\flat^{rel} U \to U$, def. \ref{RelativeFlat}, to all the infinitesimal disks in $U$:

$$
  \array{
     && \tau_{\flat^{rel}U}
     \\
     & \swarrow && \searrow
     \\
     \tau_V && \swArrow && \tau_X
     \\
     & {}_{\mathllap{\mathbf{c}_{li}}}\searrow && \swarrow_{\mathrlap{\mathbf{c}}}
     \\
     && G \mathbf{Struc}
  }
  \,.
$$

=--

+-- {: .num_defn #CartanGeometry}
###### Definition


Consider an [[infinity-action]] of $GL(V)$ on $V$ which linearizes to the canonical $GL(V)$-action on $\mathbb{D}^V_e$ by def. \ref{GeneralLinearGroup}. Form the [[semidirect product]] $GL(V) \rtimes V$. Consider any group homomorphism $G\to GL(V)$. 

A _$(G\to G\rtimes V)$-[[Cartan geometry]]_ is a $V$-manifold $X$ equipped with a $G$-structure, def. \ref{GStructure}. The Cartan geometry is called _(infinitesimally) integrable_ if the $G$-structure is so, according to def. \ref{IntegrabilityOfGStructure}.

=--

+-- {: .num_remark}
###### Remark

For $V$ an [[abelian group]], then in traditional contexts the infinitesimal integrability of def. \ref{IntegrabilityOfGStructure} comes down to the [[torsion of a G-structure]] vanishing. But for $V$ a [[nonabelian group]], this definition instead enforces that the torsion is on each [[infinitesimal disk]] the intrinsic left-invariant torsion of $V$ itself.

Traditionally this is rarely considered, matching the fact that ordinary [[vector spaces]], regarded as [[translation groups]] $V$, are [[abelian groups]]. But [[super vector spaces]] regarded (in suitable dimension) as [[super translation groups]] are _[[nonabelian groups]]_ (we discuss this in detail below in _[The super-Klein geometry: super-Minkowski spacetime](#SuperMinkowskiSpacetime)_). Therefore super-vector spaces $V$ may carry intrinsic torsion, and therefore first-order integrable $G$-structures on $V$-manifolds are torsion-ful. 

Indeed, this is a phenomenon known as the [[torsion constraints in supergravity]]. Curiously, as discussed there, for the case of [[11-dimensional supergravity]] the [[equations of motion]] of the gravity theory are _equivalent_ to the super-Cartan geometry satisfying this torsion constraint. This way super-Cartan geometry gives a direct general abstract route right into the heart of [[M-theory]].

=--

This we come to now in _[Super-Cartan geometry for Supergravity](#SuperCartanGeometry)_.


### **3)** Super-Cartan geometry for Supergravity
 {#SuperCartanGeometry}


Above in _[The geometric substance](#TheGeometricSubstance)_ we have prepared a [[topos]] context for [[supergeometry]] with a system of [[modal operators]] that accurately reflect the three levels of geometric structure in supergeometry: smooth structure, infinitesimal thickening and fermionic odd grading.

Then in _[G-Structure and Cartan geometry](#GStructureAndCartanGeometry)_ we have used these [[modal operators]] to formulate Cartan geometry on $V$-manifolds, def. \ref{VManifold}, for any given local model group space $V$.

Here we now consider a [[concrete particular]] choice for such a $V$: [[super-Minkowski spacetimes]].

1. _[Super differential forms](#DeRhamComplexOfSuperDifferentialForms)_

1. _[Super Lie algebra valued super differential forms](#SuperLieAlgebraValuedSuperDifferentialForms)_

1. _[Supersymmetry and Super-Minkowski spacetime](#SuperMinkowskiSpacetime)_

1. _[Poincar&#233; connections: Graviton and gravitino field](#GravitonAndGravitino)_

1. _[Cohomology of super Minkowski spacetime](#CohomologyOfSuperMinkowskiSpacetime)_



#### Super differential forms
 {#DeRhamComplexOfSuperDifferentialForms}

Recall from def. \ref{SuperCartesianSpace}:

A [[super Cartesian space]] $\mathbb{R}^{p|q}$ is the [[formal dual]]
of the [[commutative superalgebra]] 

$$
  C^\infty(\mathbb{R}^{p|q})
  \coloneqq 
  C^\infty(\mathbb{R}^p)\otimes_{\mathbb{R}}\wedge^\bullet \mathbb{R}^q
$$

in that a smooth function 
$\mathbb{R}^{p_1|q_1}\longrightarrow \mathbb{R}^{p_2|q_2}$
is equivalently (by definition!) a superalgebra homomorphism

$$
  C^\infty(\mathbb{R}^{p_1|q_1})
  \longleftarrow
  C^\infty(\mathbb{R}^{p_2|q_2})
  \,.
$$

Notice then that from knowledge of an [[algebra of functions]]
one obtains the corresponding [[de Rham complex]] by the idea
of [[Kähler differentials]]. As discussed there, this statement requires
a little care in the smooth context, but the result is still
immediate:

For $\mathbb{R}^n$ a [[Cartesian space]], then its [[de Rham complex]] is the $\mathbb{Z}$-graded commutative [[dg-algebra]] whose underlying $\mathbb{Z}$-[[graded vector space]] is

$$
  \Omega^\bullet(\mathbb{R}^p)
  =
  C^\infty(\mathbb{R}^p) \otimes_{\mathbb{R}} \wedge^\bullet \langle \mathbf{d}x^1, \cdots, \mathbf{d}x^p\rangle
$$

and whose [[differential]] is defined in degree-0 by

$$
  \mathbf{d} f \coloneqq \sum_{i = 1}^p \frac{\partial f}{\partial x^i} \mathbf{d}x^i
$$

and extended from there to all degree by the graded Leibnitz rule.

It is immediate to generalize this to the super-context, one just needs to be sure to apply the [[signs in supergeometry|sign rule]] throughout.


+-- {: .num_defn #SuperDeRhamComplex}
###### Definition

The de Rham complex of [[super differential forms]] $\Omega^\bullet(\mathbb{R}^{p|q})$ on a [[super Cartesian space]] $\mathbb{R}^{p|q}$ is the $(\mathbb{Z},\mathbb{Z}_2)$-bigraded commutative algebra

$$
  \Omega^\bullet(\mathbb{R}^{p|q})
  =
  C^\infty(\mathbb{R}^{p|q}) 
    \otimes_{\mathbb{R}} 
   \wedge^\bullet \langle 
      \mathbf{d}x^1, \cdots, \mathbf{d}x^p,
      \; 
      \mathbf{d}\theta^1, \cdots, \mathbf{d}\theta^q
   \rangle
$$

whose [[differential]] is defined in degree-0 by

$$
  \mathbf{d} f \coloneqq \sum_{i = 1}^p \frac{\partial f}{\partial x^i} \mathbf{d}x^i
$$

and extended from there to all degree by the graded Leibnitz rule.


=--

+-- {: .num_remark }
###### Remark

We may write 

$$
  (n,\sigma)\in \mathbb{Z} \times \mathbb{Z}_2
$$ 

for elements in this bigrading group. 

In this notation the grading of the elements in $\Omega^\bullet(\mathbb{R}^{p|q})$ is all induced by the fact that the de Rham differential $\mathbf{d}$ itself is a [[derivation]] of degree $(1,even)$.

| generator | bi-degree |
|--|--|
| $x^a$ | (0,even) |
| $\theta^\alpha$ | (0,odd) |
| $\mathbf{d}$ | (1,even) |

Here the last line means that we have

| generator | bi-degree |
|--|--|
| $x^a$ | (0,even) |
| $\theta^\alpha$ | (0,odd) |
| $\mathbf{d}x^a$ | (1,even) |
| $\mathbf{d}\theta^\alpha$ | (1,odd) |


The formula for the "cohomologically- and super-graded commutativity" in $\Omega^\bullet(\mathbb{R}^{p|q})$ is 

$$
  \alpha \wedge \beta 
  = 
  \;
  (- 1)^{n_\alpha n_\beta + \sigma_\alpha \sigma_\beta}
  \;
  \beta \wedge \alpha
$$

for all $\alpha,  \beta \in \Omega^\bullet(\mathbb{R}^{p|q})$ of homogeneous $\mathbb{Z}\times \mathbb{Z}_2$-degree. Hence there are _two_ contributions to the sign picked up when exchanging two super-differential forms in the wedge product:

1. there is a "cohomological sign" which for commuting a $n_1$-forms past an $n_2$-form is $(-1)^{n_1 n_2}$;

1. in addition there is a "super-grading" sich which for commuting a $\sigma_1$-graded coordinate function past a $\sigma_2$-graded coordinate function (possibly under the de Rham differential) is $(-1)^{\sigma_1 \sigma_2}$.

=--

+-- {: .num_example }
###### Example


$$
  x^{a_1} (\mathbf{d}x^{a_2}) = + (\mathbf{d}x^{a_2}) x^{a_1}
$$


$$
  \theta^\alpha (\mathbf{d}x^a) = + (\mathbf{d}x^a) \theta^\alpha
$$

$$
  \theta^{\alpha_1} (\mathbf{d}\theta^{\alpha_2}) 
   = 
  - (\mathbf{d}\theta^{\alpha_2}) \theta^{\alpha_1}
$$

$$
  \mathbf{d}x^{a_1}
  \wedge
  \mathbf{d} x^{a_2}
  =
  -
  \mathbf{d} x^{a_2}
  \wedge
  \mathbf{d} x^{a_1}
$$


$$
  \mathbf{d}x^a
  \wedge
  \mathbf{d} \theta^{\alpha}
  =
  -
  \mathbf{d}\theta^{\alpha}
  \wedge
  \mathbf{d} x^a
$$

$$
  \mathbf{d}\theta^{\alpha_1}
  \wedge
  \mathbf{d} \theta^{\alpha_2}
  =
  +
  \mathbf{d}\theta^{\alpha_2}
  \wedge
  \mathbf{d} \theta^{\alpha_1}
$$

=--

See at _[[signs in supergeometry]]_ for further discussion, for literature, and for mentioning of _another_ popular sign convention, which is different but in the end yields the same cohomology.


#### Super Lie algebra valued super differential forms
 {#SuperLieAlgebraValuedSuperDifferentialForms}


We want to discuss the generalization of the concept of 
[[Lie algebra valued differential forms]] from ordinary 
[[differential geometry]] to [[supergeometry]]. To that end, 
we first recall the following neat formulation of ordinary
Lie algebra valued differential forms due to Cartan. This will lend itself
in fact not only to the generalization to [[super Lie algebras]]
but further to _[[super L-∞ algebras]]_, which is what is needed 
for the desciption of higher dimensional [[supergravity]].


+-- {: .num_defn #CEAlgebra}
###### Definition

The _[[Chevalley-Eilenberg algebra]]_ $CE(\mathfrak{g})$ of a finite dimensional [[Lie algebra]] $\mathfrak{g}$ is the [[semifree dga|semifree]] graded-commutative [[dg-algebra]] whose underlying graded algebra is the [[Grassmann algebra]] 

$$
  \wedge^\bullet \mathfrak{g}^*
  = 
  k \oplus \mathfrak{g}^* \oplus (\mathfrak{g}^* \wedge \mathfrak{g}^* ) \oplus \cdots
$$ 

(with the $n$th skew-symmetrized power in degree $n$)

and whose [[differential]] $d$ (of degree +1) is on $\mathfrak{g}^*$ the dual of the Lie bracket

$$
  d|_{\mathfrak{g}^*} := [-,-]^* : \mathfrak{g}^* \to \mathfrak{g}^* \wedge \mathfrak{g}^*
$$

extended uniquely as a graded [[derivation]] on $\wedge^\bullet \mathfrak{g}^*$.

That this differential indeed squares to 0, $d \circ d = 0$, is precisely the fact that the Lie bracket satisfies the [[Jacobi identity]].

=--

+-- {: .num_remark #CEAlgebraInTermsOfBasis}
###### Remark

If in the situation of prop. \ref{CEAlgebra} we choose a dual basis $\{t^a\}$ of $\mathfrak{g}^*$ and let $\{C^a{}_{b c}\}$ be the structure constants of the Lie bracket in that basis, then the action of the differential on the basis generators is

$$
  d t^a = - \frac{1}{2} C^a{}_{b c} t^b \wedge t^c
  \,,
$$

where here and in the following a sum over repeated indices is implicit.

=--

+-- {: .num_prop #CEIfFullyFaithful}
###### Proposition

The construction of Chevalley-Eilenberg algebras in def. \ref{CEAlgebra}
yields a [[fully faithful functor]]

$$
  CE(-)
  \colon
  LieAlg
  \longrightarrow
  dgAlg^{op}
$$

embedding [[Lie algebras]] into [[formal duals]] of [[differential graded algebras]]. Its image consists of precisely of the [[semifree dg-algebras]], those whose underlying [[graded algebra]] (forgetting the [[differential]]) is a [[Grassmann algebra]] generated on a [[vector space]].

=--



+-- {: .num_defn #WeilForLInfinitityAlgebra}
###### Definition

Given a [[Lie algebra]] $\mathfrak{g}$, its **[[Weil algebra]]** $W(\mathfrak{g})$ is the [[semi-free dga]] whose underlying graded-commutative algebra is the [[exterior algebra]]

$$
  \wedge^\bullet (\mathfrak{g}^* \oplus \mathfrak{g}^*[1])
$$

on $\mathfrak{g}^*$ and a shifted copy of $\mathfrak{g}^*$,
and whose [[differential]] is the sum

$$
  d_{W(\mathfrak{g})} = d_{CE(\mathfrak{g})} + \mathbf{d}
$$

of two graded [[derivations]] of degree +1 defined by

* $\mathbf{d}$ acts by degree shift $\mathfrak{g}^* \to \mathfrak{g}^*[1]$ on elements in $\mathfrak{g}^*$ and by 0 on elements of $\mathfrak{g}^*[1]$;

* $d_{CE(\mathfrak{g})}$ acts on unshifted elements in $\mathfrak{g}^*$ as the differential of the [[Chevalley-Eilenberg algebra]] of $\mathfrak{g}$ and is extended uniquely to shifted generators by graded-commutattivity 
 
  $$
    [d_{CE(\mathfrak{g}}, \mathbf{d}] = 0
  $$

  with $\mathbf{d}$:

  $$
    d_{CE(\mathfrak{g})} \mathbf{d} \omega :=
    - \mathbf{d} d_{CE(\mathfrak{g})} \omega
  $$

  for all $\omega \in \wedge^1 \mathfrak{g}^*$.

=--



+-- {: .num_prop #LieAlgValuedFormsViaDgAlgHoms}
###### Proposition

Given a [[Lie algebra]] $\mathfrak{g}$, then 
a [[Lie algebra valued differential form]] on, say, 
a [[Cartesian space]] $\mathbb{R}^n$, is 
equivalently a dg-algebra homomorphims

$$
  \Omega^\bullet(\mathbb{R}^p)
  \longleftarrow
  W(\mathfrak{g})
  \colon
  A
  \,,
$$ 

hence there is a [[natural bijection]]

$$
  \Omega^1(\mathbb{R}^p, \mathfrak{g})
  \simeq
  Hom_{dgAlg}(W(\mathfrak{g}), \Omega^\bullet(\mathbb{R}^p))
  \,.
$$

The form $A$ is _flat_ in that its [[curvature]] [[differential 2-form]] $F_A$ vanishes, precisely if this morphism factors through the CE-algebra. 

=--

+-- {: .num_remark}
###### Remark

With a choice of basis as in remark \ref{CEAlgebraInTermsOfBasis}, then the content of prop. \ref{LieAlgValuedFormsViaDgAlgHoms} is seen in components as follows:

a dg-algebra homomorphism is first of all a homomorphism of [[graded algebras]], and since the domain $W(\mathfrak{g})$ is free as a graded algebra, such is entirely determined by what it does to the generators

$$
  \array{
    t^a, &\mapsto& A^a & \in \Omega^1(\mathbb{R}^n)
    \\ 
    r^a &\mapsto& F^a & \in \Omega^2(\mathbb{R}^n)
  }
  \,.
$$

But being a dg-algebra homomorphism, this assignment needs to respect the differentials on both sides. For the original generators this gives

$$
  \array{
    t^a &\mapsto&&&  A^a
    \\
    \downarrow^{\mathrlap{d_{W(\mathfrak{g})}}} &&&& \downarrow^{\mathrlap{\mathbf{d}_{dR}}}
    \\
    - \frac{1}{2} C^a{}_{b c} t^b \wedge t^c
    + r^a
    &\mapsto&
    (- \frac{1}{2} C^a{}_{b c} A^b \wedge A^c + F^a)
    &=&
    \mathbf{d}_{dR} A^a 
  }
  \,.
$$

With this satisfied, then, by the very nature of the [[Weil algebra]],
the differential is automatically respected also on the shifted generators. This statement is the _[[Bianchi identity]]_.

=--

Now to pass this to [[superalgebra]]. 

+-- {: .num_defn #SuperGrassmannAlgebra}
###### Definition

For $V = V_{even} \oplus V_{odd}$ a [[super vector space]], then its [[Grassmann algebra]] $\wedge^\bullet V$ is the free $(\mathbb{Z},\mathbb{Z}_2)$-bigraded commutative algebra
subject to

$$
  v_1 \wedge v_2 = (-1) (-1)^{\sigma_1 \sigma_2}
  \,.
$$

=--

In the spirit of prop. \ref{CEIfFullyFaithful} we may then simply say that:

+-- {: .num_defn #SuperLieAlgebraViaCE}
###### Definition

A [[super Lie algebra]] structure on a [[super vector space]] $\mathfrak{g}$ is 
the [[formal dual]] of a $(\mathbb{Z},\mathbb{Z}_2)$-bigraded commutative
differential algebra 

$$
  CE(\mathfrak{g}) = \left(
   \wedge^\bullet V^\ast, \; d
  \right)
$$ 

(with differential $d$ of degree (1,even))
such that the underlying graded algebra is the super Grassmann algebra
$\wedge^\bullet \mathfrak{g}^\ast$ via def. \ref{SuperGrassmannAlgebra}.

We call this again the [[Chevalley-Eilenberg algebra]] of the super Lie algebra
dually defined thereby.

Similarly, the [[Weil algebra]] $W(\mathfrak{g})$ is obtained from this by adding a generator in degree $(2,\sigma)$ for each previous generator in degree $(1,\sigma)$ and extending the differential as in def. \ref{WeilForLInfinitityAlgebra}.

=--

Unwinding what this means, one finds that it is equivalent to the 
following more traditional definition:

+-- {: .num_prop #SuperLieAlgebraTraditional}
###### Proposition

A [[super Lie algebra]] is equivalently

1. a [[super vector space]] $\mathfrak{g} = \mathfrak{g}_{even} \oplus \mathfrak{g}_{odd}$;

1. equipped with a bilinear bracket
 
   $$
     [-,-] : \mathfrak{g}\otimes \mathfrak{g} \to \mathfrak{g}
   $$

   which is _graded_ skew-symmetric: it is skew symmetric on $\mathfrak{g}_{even}$ and _symmetric_ on $\mathfrak{g}_{odd}$.

1. that satisfied the $\mathbb{Z}_2$-graded [[Jacobi identity]] in that for any three elements $x,y,z \in \mathbb{g}$ of homogeneous super-degree $\sigma_x,\sigma_y,\sigma_z)\in \mathbb{Z}_2$ then

   $$
     [x, [y, z]] = [[x,y],z] + (-1)^{\sigma_x \cdot \sigma_y} [y, [x,z]]
     \,.
   $$

=--

But with def. \ref{SuperLieAlgebraViaCE} we immediately known, in view of 
prop. \ref{LieAlgValuedFormsViaDgAlgHoms}, what _super Lie algebra valued super differential forms_ should be:

+-- {: .num_defn #SuperLieAlgValuedDiffForms}
###### Definition


Given a [[super Lie algebra]] $\mathfrak{g}$, def. \ref{SuperLieAlgebraViaCE}, prop. \ref{SuperLieAlgebraTraditional}, then a $\mathfrak{g}$-valued super-differential form on the [[super Cartesian space]] $\mathbb{R}^{p|q}$ is a $(\mathbb{Z},\mathbb{Z}_2)$-graded dg-algebra homomorphism

$$
  \Omega^\bullet(\mathbb{R}^{p|q})
  \longleftarrow
  W(\mathfrak{g})
  \;\colon\;
  A
$$

from the [[Weil algebra]] according to def. \ref{SuperLieAlgebraViaCE}, to the super de Rham complex of def. \ref{SuperDeRhamComplex}.

Accordingly we write

$$
  \Omega^1(\mathbb{R}^{p|q}, \mathfrak{g})
  \coloneqq
  Hom_{dgAlg}(W(\mathfrak{g}), \Omega^\bullet(\mathbb{R}^{p|q}))
  \,.
$$

=--


+-- {: .num_example}
###### Example

Let $\mathfrak{g} \coloneqq \mathbb{R}^{1|0} = \mathbb{R}$ be the ordinary abelian [[line Lie algebra]].
Then

$$
  \Omega^1(\mathbb{R}^{p|q}, \mathbb{R}^{1|0})
  \simeq
  \Omega^1(\mathbb{R}^{p|q})_{even}
$$

is the set of super-differential forms in degree $(1,even)$.

Similarly with $\mathfrak{g} = \mathbb{R}^{0|1}$ the [[odd line]] regarded as an abelian super Lie algebra, then

$$
  \Omega^1(\mathbb{R}^{p|q}, \mathbb{R}^{0|1})
  \simeq
  \Omega^1(\mathbb{R}^{p|q})_{odd}
 \,.
$$

So generally for $\mathfrak{g}$ an ordinary Lie algebra regarded as a super Lie algebra, then $\Omega^1(\mathbb{R}^{p|q}, \mathfrak{g})$ is bigger than $\Omega^1(\mathbb{R}^p,\mathfrak{g})$.

This is an issue to be dealt with when describing [[supergravity]] in terms of Cartan fields on [[supermanifolds]] $X$, because the actual [[spacetime]] manifold one cares about is just the [[bosonic modality|bosonic part]] $\stackrel{\rightsquigarrow}{X}$. This issue is deal with by the concept of [rheonomy](D%27Auria-Fre+formulation+of+supergravity#Rheonomy).


=--


#### Supersymmetry and Super-Minkowski spacetime
 {#SuperMinkowskiSpacetime}

We consider now very specific [[super Lie algebras]], def. \ref{SuperLieAlgebraViaCE}, those of _[[supersymmetry]]_.

Just as traditional [[Cartan geometry]] involves a pair of [[Lie algebras]] $\mathfrak{h} \hookrightarrow \mathfrak{g}$, so super-Cartan geometry involves a similar pair of [[super Lie algebras]].
For describing [[supergravity]], we now
want to establish an [[superalgebra]]-[[analogy|analog]] of the inclusion of the [[Lorentz Lie algebra]] $\mathfrak{h} = \mathfrak{so}(\mathbb{R}^{d-1,1})$ into the [[Poincaré Lie algebra]] $\mathfrak{g} = \mathfrak{Iso}(\mathbb{R}^{d-1,1})$.

| ([[higher Cartan geometry|higher]]-)[[Cartan geometry]] | $\mathfrak{g}$ | $\mathfrak{h}$ | $\mathfrak{g}/\mathfrak{h}$ |
|---------------------|----------------|----------------|-----------------------------|
| [[Einstein gravity]]  | $\mathfrak{Iso}(\mathbb{R}^{d-1,1})$ | $\mathfrak{so}(\mathbb{R}^{d-1,1})$ | $\mathbb{R}^{d-1,1}$ |
| [[supergravity]] | $\mathfrak{Iso}(\mathbb{R}^{d-1,1\vert N})$ | $\mathfrak{so}(\mathbb{R}^{d-1,1})$ | $\mathbb{R}^{d-1,1\vert N}$ |
| [[11-dimensional supergravity]] | $\mathfrak{Iso}(\widehat{\mathbb{R}}^{10,1\vert \mathbf{32}})$ | $\mathfrak{so}(\mathbb{R}^{d-1,1})$ | $\widehat{\mathbb{R}}^{10,1\vert \mathbf{32}}$ |

To that end, consider the structure of any [[super Lie algebra]] 

$$
  \left(
    \mathfrak{Iso}(\mathbb{R}^{d-1,1})\oplus N
    ,
    [-,-]
  \right)
$$ 

that extends the [[Poincaré Lie algebra]] $\mathfrak{Iso}(\mathbb{R}^{d-1,1})$ by some odd-[[graded vector space]] $N$. Any such extension involves involves:

1. the even-odd superbracket $[\mathfrak{so},N]$, which hence is an [[action]] of the [[Lorentz Lie algebra]] on  $N$;

1. the even-even-odd [[Jacobi identity]], which is the action property of that action;

1. the odd-odd superbracket $[N,N]$ which is a _symmetric_ [[bilinear form]] $N \otimes N \to \mathbb{R}^{d-1,1}$

1. the even-odd-odd [[Jacobi identity]], which says that this bilinear form is $\mathfrak{o}(d-1,1)$-[[equivariance|equivariant]].


Such structure exists on [[real structure|real]] [[spin representation]]:

+-- {: .num_prop #RealSpinRepresentations}
###### Proposition

Let $V = \mathbb{R}^{d-1,1}$ be [[Minkowski spacetime]] of some [[dimension]] $d$. 

The following table lists the [[irreducible representation|irreducible]] [[real structure|real]] [[spin representations]] of $Spin(V)$.

| $d$ | $Spin(d-1,1)$ | minimal real spin representation $N$ | $dim_{\mathbb{R}} S\;\;$ |  $V$ in terms of $S^\ast$ |  [[supergravity]] | 
|--|--|--|--|--|--|
| 1 | $\mathbb{Z}_2$ | $N$ real | 1 | $V \simeq (N^\ast)^{\otimes}^2$ |  |
| 2 | $\mathbb{R}^{\gt 0} \times \mathbb{Z}_2$ | $N^+, N^-$ real | 1 | $V \simeq ({N^+}^\ast)^{\otimes^2} \oplus ({N^-}^\ast)^{\otimes 2}$ |  |
| 3 | $SL(2,\mathbb{R})$ | $N$ real | 2 |  $V \simeq Sym^2 N^\ast$ |  |
| 4 | $SL(2,\mathbb{C})$ | $N_{\mathbb{C}} \simeq N' \oplus N''$ | 4 | $V_{\mathbb{C}} \simeq {N'}^\ast \oplus {N''}^\ast$ |  |
| 5 | $Sp(1,1)$ | $N_{\mathbb{C}} \simeq N_0 \otimes_{\mathbb{C}} W$ | 8 |  $\wedge^2 S_0^\ast \simeq \mathbb{C} \oplus V_{\mathbb{C}}$ |  |
| 6 | $SL(2,\mathbb{H})$ | $N^\pm_{\mathbb{C}} \simeq N_0^\pm  \otimes_{\mathbb{C}} W$ | 8 | $V_{\mathbb{C}} \simeq \wedge^2 {N_0^+}^\ast \simeq (\wedge^2 {N_0^-}^\ast)^\ast$ |  |
| 7 |  |  $N_{\mathbb{C}} \simeq N_0 \otimes_{\mathbb{C}} W$ | 16 |  $\wedge^2 S_0^\ast \simeq V_{\mathbb{C}} \oplus \wedge^2 V_{\mathbb{C}}$ |  |
| 8 |  | $N_{\mathbb{C}} \simeq N^\prime \oplus N^{\prime\prime}$ | 16 | ${N'}^\ast {N''}^\ast \simeq V_{\mathbb{C}} \oplus \wedge^3 V_{\mathbb{C}}$ |  |
| 9 |  | $N$ real | 16 |  $Sym^2 N^\ast \simeq \mathbb{R} \oplus V \wedge^4 V$ |  |
| 10 |   | $N^+ , N^-$ real | 16 | $Sym^2(N^\pm)^\ast \simeq V  \oplus \wedge_\pm^5 V$ | [[type II supergravity]] |
| 11 |   | $N$ real | 32 | $Sym^2 N^\ast \simeq V \oplus \wedge^2 V \oplus \wedge^5 V$ | [[11-dimensional supergravity]] |

Here $W$ is the 2-dimensional [[complex vector space]] on which the [[quaternions]] naturally act. 

=--

(e.g. [Freed 99, page 48](#spin+representation#Freed99))

+-- {: .num_remark #BilinearPairingOnSpinors}
###### Remark

The last column in prop. \ref{RealSpinRepresentations} implies that in each dimension there exists a [[linear map]]

$$
  \overline{(-)}\Gamma(-) \;\colon\; S^\ast \otimes S^\ast \longrightarrow \mathbb{R}^{d-1,1}
$$

which is 

1. symmetric;

1. $Spin(V)$-equivariant.

This is what in the [[physics]] literature is expressed in components by the Gamma matrices with "indices lowered" using the _[[charge conjugation matrix]]_.

=--

+-- {: .num_cor}
###### Corollary

Given a real $Spin(\mathbb{R}^{d-1,1})$ representation $N$, 
there exists a [[super Lie algebra]] structure on

$$
  \mathfrak{so}(\mathbb{R}^{d-1,1})\rtimes\mathbb{R}^{d-1,1} 
  \oplus N
$$

extending the [[Poincare Lie algebra]] whose odd-odd-bracket 
is the bilinear pairing of remark \ref{BilinearPairingOnSpinors}.

=--

+-- {: .num_defn #SuperPoincareAndSuperMinkowski}
###### Definition


This is the _[[super Poincaré Lie algebra]]_ $\mathfrak{Iso}(\mathbb{R}^{d-1,1|N})$.
Its [[Lie integration]] to a [[super Lie group]] is the 
[[super Poincaré group]] $Iso(\mathbb{R}^{d-1,1|N})$.


The [[quotient]] of that by the [[spin group]] is [[super-Minkowski spacetime]]

$$
  \mathbb{R}^{d-1,1|N} \coloneqq \mathfrak{Iso}(\mathbb{R}^{d-1,1|N})/\mathfrak{so}(\mathbb{R}^{d-1,1|N})
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

The space underlying the [[super Minkowski spacetime]] $\mathbb{R}^{d-1,1|N}$ in def. \ref{SuperPoincareAndSuperMinkowski} is the [[super Cartesian space]] $\mathbb{R}^{d,dim_{\mathbb{R}}(N)}$, def. \ref{SuperCartesianSpace}.

=--





#### Poincar&#233; connections: Graviton and gravitino field
 {#GravitonAndGravitino}

We may now apply the general discussion of super Lie algebra valued super differential forms, def. \ref{SuperLieAlgValuedDiffForms}, to the case of the [[super Poincare Lie algebra]], def. \ref{SuperPoincareAndSuperMinkowski}.

its [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{Iso}(\mathbb{R}^{d-1,1|N}))$ is generated on 

* elements $\{e^a\}$ and $\{\omega^{ a b}\}$ of degree $(1,even)$

* and elements $\{\psi^\alpha\}$ of degree $(1,odd)$

with the differential defined by

$$
  d_{CE} \, \omega^{a b} = \omega^a{}_b \wedge \omega^{b c}
$$

$$
  d_{CE} \, e^{a } = \omega^a{}_b \wedge e^b + \frac{i}{2}\bar \psi \Gamma^a \psi
$$

$$
  d_{CE} \, \psi = \frac{1}{4} \omega^{ a b} \Gamma_{a b} \psi
  \,.
$$

Accordingly its [[Weil algebra]] 
$W(\mathfrak{Iso}(\mathbb{R}^{d-1,1|N}))$
has these generators together with a further degree-shifted copy of each $\{t^a\}$, $\{r^{a b}\}$ and $\{\rho^{\alpha}\}$ with differential given by

$$
  d_{W} \, \omega^{a b} = \omega^a{}_b \wedge \omega^{b c} + r^{a b}
$$

$$
  d_{W} \, e^{a } = \omega^a{}_b \wedge e^b + \frac{i}{2}\bar \psi \Gamma^a \psi + t^a
$$

$$
  d_{W} \, \psi = \frac{1}{4} \omega^{ a b} \Gamma_{a b} \psi + \rho
  \,.
$$


Differential form data with values in this is a morphism of [[dg-algebras]] from the [[Weil algebra]] $W(\mathfrak{Iso}(\mathbb{R}^{d-1,1|N}))$ to the [[deRham dg-algebra]] $\Omega^\bullet(\mathbb{R}^{p|q})$, def. \ref{SuperDeRhamComplex}

$$
  \Omega^\bullet(X)
   \leftarrow
   W(\mathfrak{Iso}(\mathbb{R}^{d-1,1|N}))
   :
   (A,F_A)  
   \,.
$$

This is [[∞-Lie algebroid valued differential form]] data with [[curvature|∞-Lie algebroid valued curvature]] that is explicitly given by:




* connection forms / field configuration

  * $E \in \Omega^1(X,\mathbb{R}^{d-1,1|N})$ -- the **[[vielbein]]** (part of the _[[graviton]] [[field (physics)|field]]_)

  * $\Omega \in \Omega^1(X, \mathfrak{so}(\mathbb{R}^{d-1,1}))$ -- the **[[spin connection]]** (part of the _[[graviton]] [[field (physics)|field]]_)

  * $\Psi \in \Omega^ 1(X,S)$ -- the **[[spinor]]** (the [[gravitino]] [[field (physics)|field]])


* [[curvature]] forms / [[field strength]]s

  * $T = d E + \Omega \cdot E + \Gamma(\bar \Psi \wedge \Psi) \in \Omega^2(X,\mathbb{R}^{d-1,1})$ - the **[[torsion of a metric connection|torsion]]**

  * $R = d \Omega + [\Omega \wedge \Omega] \in \Omega^2(X, \mathfrak{so}(10,1))$ - the **[[Riemann curvature]]**

  * $\rho = d \Psi + (\Omega \wedge \Psi) \in \Omega^2(X, S)$ -- the **[[covariant derivative]] of the [[gravitino]]**

#### Cohomology of super-Minkowski spacetime 
 {#CohomologyOfSuperMinkowskiSpacetime}

The [[Chevalley-Eilenberg algebras]] which in def. \ref{CEAlgebra} and def. \ref{SuperLieAlgebraViaCE} we used to _characterize_ the corresponding (super) Lie algebras are of course traditionally introduced as the [[cochain complexes]] whose [[cochain cohomology]] is [[Lie algebra cohomology]]. We may conceptualize this as follows:

+-- {: .num_defn #SiteCartSp}
###### Definition

For $n \in \mathbb{N}$ write $\mathbb{R}^{1|0}[n]$ for the _[[line Lie n-algebra|line Lie (n+1)-algebra]]_, the [[super L-infinity algebra]] defined simply as the [[formal dual]] to the $(\mathbb{Z},\mathbb{Z}_2)$-graded commutative [[dg-algebra]]

$$
  CE(\mathbb{R}^{1|0}[n]) \coloneqq
  \left(
    \wedge^\bullet \mathbb{R}^{1|0}[n],
    \;
    d = 0
  \right)
$$

whose underlying [[graded algebra]] is freely generated from a single generator in degree $(n,even)$, and whose differential vanishes.

=--

+-- {: .num_remark #LieAlgebraCohomologAsHomomorphism}
###### Remark

Recall that being a "[[formal dual]]" to a dg-algebra here simply means that for $\mathfrak{g}$ any [[super Lie algebra]], the homomorphisms of [[super L-infinity algebras]] of the form

$$
  \mu \;\colon\; \mathfrak{g} \longrightarrow \mathbb{R}^{1|0}[n]
$$

are equivalently (by definition!) homomorphisms of [[dg-algebras]] of the form

$$
  CE(\mathfrak{g})
  \longleftarrow
  CE(\mathbb{R}^{1|0}[n])
  \,.
$$ 

Since the underlying graded algebra of $CE(\mathbb{R}^{1|0}[n])$ is free on a single generator $c$ in degree $n+1$, such a homomorphism is determined by the image of this generator

$$
  c \mapsto \mu \in CE(\mathfrak{g})
  \,.
$$

Moreover, the condition that this map respects the differentials, and since the differential on $CE(\mathbb{R}^{1|0}[n])$ vanishes by definition, this means that

$$
  \array{
     c &\mapsto& && \mu
     \\
     \downarrow^{\mathrlap{d_{\mathbb{R}^{1|0}[n]}}}
     && &&
    \downarrow^{\mathrlap{d_{\mathfrak{g}}}}
     \\
     0 &\mapsto& 0 &=& d_{\mathfrak{g}}\mu
  }
  \,.
$$

Hence such a moprhism $\mu$ is equivalently a _closed_ element of degree $(n+1)$ in $CE(\mathfrak{g})$, hence is equivalently a [[Lie algebra cohomology|super Lie algebra cocycle]] of degree $n+1$ on $\mathfrak{g}$.

This way [[line Lie n-algebra|line Lie (n+1)-algebra]] $\mathbb{R}^{1|0}[n]$ is the _[[moduli stack|moduli object]]_ for degree-$(n+1)$ Lie algebra cohomology in direct [[analogy]] of how for instance the familiar [[Eilenberg-MacLane space]] $B^{n+1}\mathbb{R} = K(\mathbb{Z},n+1)$ is the classifying space for degree $n+1$ [[ordinary cohomology]] of [[topological spaces]].

=--

One advantange of conceptualizing Lie algebra cocycles as in remark \ref{LieAlgebraCohomologAsHomomorphism} is that it neatly connects to the formulation of [[Lie algebra valued forms]] according to def. \ref{LieAlgValuedFormsViaDgAlgHoms}, def. \ref{SuperLieAlgValuedDiffForms}:


+-- {: .num_remark }
###### Remark

A $\mathbb{R}^{1|0}[n]$-valued differential form is simply an even closed differential $(n+1)$-form:

$$
  \Omega^1(\mathbb{R}^{p|q}, \mathbb{R}^{1|0}[n])
  \simeq
  Hom(CE(\mathbb{R}^{1|0}[n]), \Omega^\bullet(\mathbb{R}^{p|q}))
  \simeq
  \Omega^{n+1}(\mathbb{R}^{p|q})_{even,closed}
  \,.
$$

Hence a super Lie algebra $(n+1)$-cocycle $\mu$ on 
$\mathfrak{g}$ naturally determines a map


$$
  \mu(-)
  \colon
  \Omega^1(\mathbb{R}^{p|q},\mathfrak{g})
  \longrightarrow
  \Omega^{n+1}(\mathbb{R}^{p|q})_{even,closed}
$$

given by forming the composite with the morphism representing the cocycle $\mu$

$$
  \left(
    \Omega^\bullet(\mathbb{R}^{p|q})
     \stackrel{A}{\longleftarrow}
  CE(\mathfrak{g})
  \right)
  \mapsto
  \left(
  \Omega^\bullet(\mathbb{R}^{p|q})
   \stackrel{A}{\longleftarrow}
  CE(\mathfrak{g})
  \stackrel{\mu^\ast}{\longleftarrow}
  CE(\mathbb{R}^{1|0}[n])
  \right)
$$

sending a [[Lie algebra valued form]] $A$ to a closed differential form $\mu(A)$.


=--

But an even closed $(n+1)$-form on $\mathbb{R}^{p|q}$ depending on other field data may be understood as the [[WZW term]] in a [[local Lagrangian]] for the [[sigma-model]] of an $(n-1)$-[[brane]] propagating on $\mathbb{R}^{p|q}$. Therefore it is of key interest to classify these for the case that $\mathfrak{g}$ is a [[super Minkowski spacetime]].



Let $(x^a, \theta^\alpha)$ be the canonical [[coordinates]] on the [[super Minkowski spacetime]] $\mathbb{R}^{d-1,1|N}$ underlying the super translation group. Then the [[left-invariant 1-forms|left invariant]] [[super differential forms|super-differential 1-forms]] are

* $\psi^\alpha = \mathbf{d} \theta^\alpha$.

* $e^a = d x^a + \frac{i}{2} \overline{\theta} \Gamma^a \mathbf{d} \theta$.

This means that there is one non-trivial differential on these:

$$ 
  \begin{aligned}
    \mathbf{d} e^a & = \mathbf{d} (\mathbf{d} x^a + \frac{i}{2} \overline{\theta} \Gamma^a d \theta)
    \\
    & = \frac{i}{2} \mathbf{d} \overline{\theta}\Gamma^a \mathbf{d} \theta
    \\
    & = \frac{i}{2} \overline{\psi}\Gamma^a \psi
  \end{aligned}
  \,.
$$

These relation consistute $CE(\mathbb{R}^{d-1,1|N})$.


+-- {: .num_remark }
###### Remark

The term $\frac{i}{2}\bar \psi \Gamma^a \psi$ is sometimes called the *[[supertorsion]]* of the [[super-vielbein]] $e$, because the defining equation

$$
  d_{CE} e^{a } -\omega^a{}_b \wedge e^b = \frac{i}{2}\bar \psi \Gamma^a \psi
$$

may be read as saying that $e$ is [[torsion]]-free except for that term. Notice that this term is the only one that appears when the differential is applied to "Lorentz scalars", hence to object in $CE(\mathfrak{siso})$ which have "all indices contracted". (See also at _[[torsion constraints in supergravity]]_.)

Notably we have 

$$
  \mathbf{d} \left( 
    \overline{\psi} \wedge \Gamma^{a_1 \cdots a_p} \psi
    \wedge e_{a_1} \wedge \cdots \wedge e_{a_p}
  \right)
  \propto
  \left(
    \overline{\psi} \wedge \Gamma^{a_1 \cdots a_p} \psi
    \wedge e_{a_1} \wedge \cdots \wedge e_{a_{p-1}}
  \right)
  \wedge
  \left(
    \overline{\Psi} \wedge \Gamma_{a_p} \Psi
  \right)
  \,.
$$


This relation is what govers all of the exceptional super Lie algebra cocycles that appear as WZW terms for [[super p-branes]]: for some combinations of $(D,p)$ a [[Fierz identity]] implies that the term

$$
  \left(
    \overline{\psi} \wedge \Gamma^{a_1 \cdots a_p} \psi
    \wedge e_{a_1} \wedge \cdots \wedge e_{a_{p-1}}
  \right)
  \wedge
  \left(
    \overline{\Psi} \wedge \Gamma_{a_p} \Psi
  \right)
$$

vanishes identically, and hence in these dimensions the term

$$
    \overline{\psi} \wedge \Gamma^{a_1 \cdots a_p} \psi
    \wedge e_{a_1} \wedge \cdots \wedge e_{a_p}
$$

is a [[cocycle]]. 

=--

+-- {: .num_prop }
###### Proposition

Lorentz-invariant super Lie algebra cocycles on a 
[[super Minkowski spacetime]] [[super translation Lie algebra]]
$\mathbb{R}^{d-1,1|N}$ in degree $(p+2)$ appear precisely 
once (up to scalar multiple) for each combination $(d,p,N)$
for which in [[string theory]] there is a [[super p-brane]]
propagating on a $d$-dimensional [[supergravity]] background
with $N$-[[supersymmetries]].

[[!include brane scan]]

=--

#### Definite super-froms

In order to extend these [[super p-brane]] [[sigma models]]
not just on [[super Minkowski spacetime]] $\mathbb{R}^{d-1,1|N}$ but on a
$\mathfrak{so}(\mathbb{R}^{d-1,1|N})\hookrightarrow 
\mathfrak{Iso}(\mathbb{R}^{d-1,1|N})$-super Cartan geometry,
the corresponding cocycle form from the [[brane scan]]
above needs to be extended as a [[definite form]] over this spacetime.

This is a direct supergeometry analog of how a [[G2-manifold]]
is a 7-manifold equipped with a [[definite form]] that is definite
on the [[associative 3-form]] on $\mathbb{R}^7$.

In fact this is just a necessary condition, giving the 
globalization of the [[curvature]] of the [[WZW term]].
The full [[WZW term]] is a higher [[Super Gerbes]] which is a
[[higher prequantization]] of this cocycle, and 
hence its definition requires the lift of the definite cocycle form
to a [[parameterized WZW model]] over superspacetime.

Discussion of this [[classical anomaly]]-cancellation problem 
for [[super p-branes]] on curved supergravity targets
is the content at _[[schreiber:Higher Cartan Geometry]]_.



## References

Traditional literature that involves super-Cartan geometry more or less explicitly and in the context of [[supergravity]] includes

* {#Baaklini77a} N. S. Baaklini, _Spin 3/2 Field and Cartan's Geometry_, Letters in Mathematical Physics August 1977, Volume 2, Issue 1, pp 43-47

* {#Baaklini77b} N. S. Baaklini _Cartan's Geometrical Structure of Supergravity_, Lett. Math. Phys. 2 (1977) 115.

* {#Nieuwenhuizen81} [[Peter van Nieuwenhuizen]], _Supergravity_, Physics Reports, Vol. 68, p. 189 - 398, 1981


* {#DAuriaFre82}  [[Riccardo D'Auria]], [[Pietro Fré]] _[[GeometricSupergravity.pdf:file]]_, Nuclear Physics B201 (1982) 101-140 

* {#CastellaniDAuriaFre91} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], _[[Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991)

* {#Lott01} [[John Lott]], _The Geometry of Supergravity Torsion Constraints_ Comm. Math. Phys. 133 (1990), 563&#8211;615, (exposition in [arXiv:0108125](http://arxiv.org/abs/math/0108125))

* {#FigueroaOFarrill08} [[José Figueroa-O'Farrill]], _The homogeneity conjecture for supergravity backgrounds_, J.Phys.Conf.Ser.175:012002, 2009 ([arXiv:0812.1258](http://arxiv.org/abs/0812.1258))

* {#EgeilehChami13} [[Michel Egeileh]], [[Fida El Chami]], _Some remarks on the geometry of superspace supergravity_, J.Geom.Phys. 62 (2012) 53-60 ([spire](http://inspirehep.net/record/1333125))

For references on [[supergeometry]] and [[supermanifolds]] as such, see there. For references on [[supergravity]] as such, see there.

The formalization as discussed above is from

* _[[schreiber:differential cohomology in a cohesive topos]]_

[[!redirects super Cartan geometry]]