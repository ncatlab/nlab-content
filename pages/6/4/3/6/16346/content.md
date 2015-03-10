
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
#### Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

While _[[Cartan geometry]]_ was originally conceived of in the context of [[differential geometry]], its principles and constructions make sense much more generally. In particular they make sense in the context of [[supergeometry]]. The implementation of Cartan geometry in supergeometry may well be called _super-Cartan geometry_ or _Cartan super-geometry_. Where the original and motivating example for plain [[Cartan geometry]] was the formulation of [[Einstein gravity]] (via [[pseudo-Riemannian geometry]]), so super-Cartan geometry underlies and finds motivation from the formulation of [[supergravity]], see also the [Survey of (non-)existing literature below](#SurveyOfExistingLiterature).

While the general abstract [[theory]] of super-Cartan geometry proceeds in direct analogy with that of traditional Cartan geometry, the examples tend to exhibit a richer behaviour. Specifically for the case relevant to [[supergravity]] this is due to two facts:

1. The [[super Euclidean spaces]] and [[super-Minkowski spacetimes]], have, as [[super-translation groups]], [[non-abelian group|non-abelian]] [[supergroup]] structure, which is reflected in the fact that the [[left-invariant 1-forms]] ([[super differential forms]]) on these spaces are _not_ closed. This means that they carry natural intrinsic [[torsion of a G-structure]]. Due to this fact the super-Cartan geometry involved in [[supergravity]] is richer than its bosonic counterpart in a way that goes beyond the addition of "superpartners". For more on this see also at _[[torsion constraints of supergravity]]_.

1. In particular [[super-Minkowski spacetimes]] carry non-trivial exceptional [[super Lie algebra]] [[Lie algebra cohomology|cocycles]]. Their globalization as [[definite forms]] is hence [[analogy|analogous]] to what is known in the bosonic case for instance for [[G2-structure]]. These globalizations play a key role in the discussion of [[super p-brane]] [[sigma-models]] on curved [[supergravity]] backgrounds. Moreover, these cocycles classify [[super L-infinity algebra]] [[L-infinity algebra cohomology|extensions]] of [[super Minkowski spacetime]] known as [[extended super Minkowski spacetimes]]. This is the origin of much of [[higher Cartan geometry]] within super-Cartan geometry.


## Survey of (non-)existing literature
 {#SurveyOfExistingLiterature}

While the terminology "super-Cartan geometry" is not much used traditionally (but see ([Egeileh-Chami 13](#EgeilehChami13))), nevertheless the key ingredients of super-Cartan geometry are well known in the literature, and all the more is it useful to make them explicit as what they are.

Physics literature usually refers to the "superspace formulation" of [[supergravity]] when referring to the formulation of the theory in [[supergeometry]] and uses terms such as "Einstein-Cartan theory" to refer to the [[first order formulation of gravity]]. Essentially all of the literature on [[supergravity]] formulated this way in "superspace" is more or less implicitly about super-Cartan geometry for the inclusion of a [[spin group]]-[[double cover]] of the [[Lorentz group]] inside a [[super Poincaré group]], in direct analogy to how ordinary [[Einstein gravity]] ([[pseudo-Riemannian geometry]]) is the Cartan geometry of the inclusion of a [[Lorentz group]] inside a plain [[Poincaré group]] -- this in fact being Cartan's original and motivating example for the whole theory. Where physicists speak of "locally gauging [[supersymmetry]]" the mathematical formulation of that is precisely this: the "[[supersymmetry]]" [[supergroup]] is the [[super Poincaré group]] [[action|acting]] on [[super Minkowski spacetime]], and "locally gauging" it means exactly to consider [[spacetimes]] that are locally ([[tangent space]]-wise) modeled on [[super Minkowski space]], while globally varying according to a [[Lorentz group]]-[[G-structure]], hence the super-analog of a [[pseudo-Riemannian metric]].

One physics references which makes the super-Cartan-geometric picture of [[supergravity]] very explicit is ([D'Auria-Fre 82](#DAuriaFre82), [Castellani-D'Auria-Fre 91](#CastellaniDAuriaFre91)). (These authors in fact also make the [[higher Cartan geometry]] hidden here fairly explicit, see there and see at [[D'Auria-Fré formulation of supergravity]].), even though these authors do not use this mathematical terminology. Similarly, discussion of super-[[Klein geometry]] in the context of [[supergravity]] is, even if not exactly in this terminology, rather explicit in ([Figueroa-O'Farrill 08](#FigueroaOFarrill08)). 

An early reference that identifies this [[first order formulation of gravity]] explicitly as a [[Cartan connection]] is ([Baaklini 77a](#Baaklini77a), [Baaklini 77b](#Baaklini77b)), which however seems to have gone unnoticed. The only genuine citation to this article is in the list of references of the survey ([Nieuwenhuizen 81](#Nieuwenhuizen81)) which however does not actually refer the article in its text.  A much later reference that very clearly identifies the role of the mathematics of supergeometric [[G-structures]] (which is the relevant special class of super-Cartan geometry) in [[supergravity]] in the context of [[supergravity torsion constraints]] is ([Lott 01](#Lott01)). The followup ([Egeileh-Chami 13](#EgeilehChami13)) to that article again makes the terminology "Cartan geometry" fully explicit in this supergeometric context. This last article also observes that from this perspective the traditional concept of _[[Killing spinor]]_ -- which involves an extra "weakening" parameter in addition to the plain concept of a _[[covariantly constant spinor]]_ -- is naturally understood as being in fact a covariantly constant spinor, but for a different model super-[[Klein geometry]] $G/H$.

This provides ample example and application of super-Cartan geometry for the case where $G/H$ is a [[super vector space]], hence for the case corresponding to [[G-structure]]. More general super-Cartan geometry apparently remains to be explored.




## Introduction
 {#Introduction}

### The solid topos

It is traditional to introduce the concept of [[supermanifolds]] in the form of [[locally ringed topological spaces]]. There is however a more direct and possibly more illuminating way following instead the spirit of the discussion at _[[geometry of physics -- smooth sets]]_. 

#### Coordinate systems: super-Cartesian spaces
 {#CoordinareSystemsSuperCartesianSpaces}

Recall the following from the discussion at _[[geometry of physics -- smooth sets]]_.


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

The useful way to think of def. \ref{Smooth0Type} in the present context is as defining a kind of [[generalized smooth space]] which is _defined_ by which smooth function from Cartesian spaces it receives (see also at _[[motivation for sheaves, cohomology and higher stacks]]_ for more exposition of this point).

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

Hence given any $X \in Smooth0Type$, we are entitled to think of it as a [[generalized smooth space]] which need not be given as a [[set]] equipped with [[smooth structure]], but whose nature we instead we detect or _probe_ by mapping Cartesian spaces into it: given  $\mathbb{R}^n$ then we think of the set $X(\mathbb{R}^n)$ which $X$, being a [[sheaf]] on [[CartSp]], assigns, as playing the role of the set of all smooth functions "$\mathbb{R}^n \longrightarrow X$" into the would-be space $X$. 

The [[Yoneda lemma]] gives that this is not circular, but consistent: once we identify Cartesian spaces themselves as smooth spaces via the Yoneda embedding, then the previous statement becomes literally true and we may remove the quotation marks:

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

The identification of (super-)[[smooth manifolds]] inside all (super-)[[smooth spaces]] we consider [below](#TheCurvedCase).

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

It is an observation from [[experiment]], originating in the [[Stern-Gerlach experiment]], that spaces of [[physical fields]] for [[physical theories]] that contain [[fermions]] behave as if they have [[algebras of functions]] which are not quite [[commutative algebras]], but where the functions depending on the [[fermions]] ony commute with each other up to picking up a minus sign. 

+-- {: .num_defn}
###### Definition

A _[[super-commutative superalgebra]]_ (or just _[[commutative superalgebra]]_ for short)  is a $\mathbb{Z}/2\mathbb{Z}$-[[graded algebra|graded]] [[associative algebra]] $A = A_{even} \oplus A_{odd}$ such that for $a,b$ any two elements in homogeneous degree $deg(a), deg(b)\in \mathbb{Z}/2\mathbb{Z}$, then their product is related by

$$
  a \cdot b = (-1)^{deg(a) deg(b)} b \cdot a
  \,.
$$

Write $SuperCAlg_{\mathbb{R}}$ for the [[category]] of commutative superalgebras over $\mathbb{R}$.

=--

+-- {: .num_defn}
###### Definition

For $q\in \mathbb{N}$, the real [[Grassmann algebra]] $C^\infty(\mathbb{R}^{0|q})$ is the $\mathbb{R}$-algebra [[free functor|freely]] generated from $q$ generators $\{\theta^i\}_{i = 1}^1$ subject to the relation 

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
  C^\infty(\mathbb{R}^p) \otimes_{\mathbb{R}} \langle\theta^1, \cdots, \theta^q\rangle 
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

For instance $C^\infty(\mathbb{R}^{0|2})_{even}$ is isomorphic to what is known as the [[ring of dual numbers]] $(\mathbb{R}\oplus \epsilon \mathbb{R})/(\epsilon^2)$ with $\epsilon = \theta^1 \theta^2$.

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

which are the identity after restricton along $\mathbb{R}^n \to \mathbb{R}^n \times \mathbb{D}$, are equivalently algebra homomorphisms of the form


$$
  C^\infty(\mathbb{R}^n)\otimes_{\mathbb{R}} \langle \epsilon\rangle
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


#### The reflective categories

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

For the third adjoint quadruple this is the statement that [[super formal smooth infinity-groupoids]] exhibits [[graded differential cohesion]] over formal smooth $\infty$-groupoids.

=--

+-- {: .num_remark }
###### Remark

Any [[reflective subcategory]]

$$
  \mathcal{C}
  \stackrel{\overset{L}{\longleftarrow}}{\underset{i}{\hookrightarrow}}
  \mathbf{H}
$$

induces an [[idempotent monad]] on $\mathbf{H}$, i.e. an [[endofunctor]]

$$
  \bigcirc \;\coloneqq\; i \circ L \colon \mathbf{H} \longrightarrow \mathbf{H}
$$

equipped with a [[natural transformation]]

$$
  \epsilon_X \colon X \longrightarrow \bigcirc X
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
  \Box \;\coloneqq\; i \circ R \colon \mathbf{H} \longrightarrow \mathbf{H}
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

Let $X$ be any object in image of this total funcotr, and let $U \times D_s \in CartSp \rtimes SupeInfPoint$. Then by adjunction $SuperFormalSmooth0Type(U\times D_s, X)$ is equivalently homs in $FormalSmooth0Type$ out of the dual of the Weil algebra which is the quotient of the original one by the ideal generated by its odd part. Hence this, in turn, is equivalently homs in $Smooth0Type$ out of $U$ and that finally is equivalently homs in $Set$ out of $\ast$ into the given set.

=--


Therefore passing to the [[adjoint triples]] of [[idempotent monads]] and [[idempotent comonads]] 


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


* [[graded differential cohesion|solidity]]

  * **[[fermionic modality]] $\e$** -- the spaces it sends to the point are purely fermionic, the [[odd line]]

  * **[[bosonic modality]] $\rightsquigarrow$** -- sends a super-space to the underlying bosonic space;

  * **[[rheonomy modality]] $\R$**

* [[elasticity]]

  * **[[reduction modality]] $\Re$** -- removes infinitesimal thickening;
 
  * **[[infinitesimal shape modality]] $\Im$** -- sends a space to its [[de Rham space]];

  * **[[infinitesimal flat modality]] $\&$**

* [[cohesion]]
  
  * **[[shape modality]]  $\int$** -- sends a space to its set $\pi_0$ of [[connected components]]; or rather, once we lift the discussion here from [[sheaves]] to [[infinity-stacks]], then this sends a space to its [[fundamental infinity-groupoid]];

  * **[[flat modality]] $\flat$** -- sends a space to the [[discrete space]] formed by its points;

  * **[[sharp modality]] $\sharp$**
 

### Super-Cartan geometry

Above we have prepared a [[topos]] context for [[supergeometry]] with a system of [[modal operators]] that accurately reflect the three lebels of geoemtric structure in supergeometry: smooth structure, infinitesimal thinckening and fermionic odd grading.

Here we now formulate super-Cartan geometry in this context and using these operations. 


#### The super-Klein geometry: super-Minkowski spacetime

we want to establish this analogy:

| ([[higher Cartan geometry|higher]]-)[[Cartan geometry]] | $\mathfrak{g}$ | $\mathfrak{h}$ | $\mathfrak{g}/\mathfrak{h}$ |
|---------------------|----------------|----------------|-----------------------------|
| [[Einstein gravity]]  | $\mathfrak{Iso}(\mathbb{R}^{d-1,1})$ | $\mathfrak{o}(d-1,1)$ | $\mathbb{R}^{d-1,1}$ |
| [[supergravity]] | $\mathfrak{Iso}(\mathbb{R}^{d-1,1\vert N})$ | $\mathfrak{o}(d-1,1)$ | $\mathbb{R}^{d-1,1\vert N}$ |
| [[11-dimensional supergravity]] | $\mathfrak{Iso}(\widehat{\mathbb{R}}^{10,1\vert N=1})$ | $\mathfrak{o}(d-1,1)$ | $\widehat{\mathbb{R}}^{10,1\vert N=1}$ |


real [[spin representation]], 

Let $V$ be a quadratic vector space, def. \ref{QuadraticVectorSpace},
over the [[real numbers]] with [[bilinear form]] or Lorentzian [[signature]], hence $V = \mathbb{R}^{d-1,1}$ is [[Minkowski spacetime]] of some [[dimension]] $d$. 

The following table lists the irreducible real representations of $Spin(V)$ ([Freed 99, page 48](#Freed99)).

| $d$ | $Spin(d-1,1)$ | minimal real spin representation $N=S$ | $dim_{\mathbb{R}} S\;\;$ |  $V$ in terms of $S^\ast$ |  [[supergravity]] | 
|--|--|--|--|--|--|
| 1 | $\mathbb{Z}_2$ | $S$ real | 1 | $V \simeq (S^\ast)^{\otimes}^2$ |  |
| 2 | $\mathbb{R}^{\gt 0} \times \mathbb{Z}_2$ | $S^+, S^-$ real | 1 | $V \simeq ({S^+}^\ast)^{\otimes^2} \oplus ({S^-}^\ast)^{\otimes 2}$ |  |
| 3 | $SL(2,\mathbb{R})$ | $S$ real | 2 |  $V \simeq Sym^2 S^\ast$ |  |
| 4 | $SL(2,\mathbb{C})$ | $S_{\mathbb{C}} \simeq S' \oplus S''$ | 4 | $V_{\mathbb{C}} \simeq {S'}^\ast \oplus {S''}^\ast$ |  |
| 5 | $Sp(1,1)$ | $S_{\mathbb{C}} \simeq S_0 \otimes_{\mathbb{C}} W$ | 8 |  $\wedge^2 S_0^\ast \simeq \mathbb{C} \oplus V_{\mathbb{C}}$ |  |
| 6 | $SL(2,\mathbb{H})$ | $S^\pm_{\mathbb{C}} \simeq S_0^\pm  \otimes_{\mathbb{C}} W$ | 8 | $V_{\mathbb{C}} \simeq \wedge^2 {S_0^+}^\ast \simeq (\wedge^2 {S_0^-}^\ast)^\ast$ |  |
| 7 |  |  $S_{\mathbb{C}} \simeq S_0 \otimes_{\mathbb{C}} W$ | 16 |  $\wedge^2 S_0^\ast \simeq V_{\mathbb{C}} \oplus \wedge^2 V_{\mathbb{C}}$ |  |
| 8 |  | $S_{\mathbb{C}} \simeq S^\prime \oplus S^{\prime\prime}$ | 16 | ${S'}^\ast {S''}^\ast \simeq V_{\mathbb{C}} \oplus \wedge^3 V_{\mathbb{C}}$ |  |
| 9 |  | $S$ real | 16 |  $Sym^2 S^\ast \simeq \mathbb{R} \oplus V \wedge^4 V$ |  |
| 10 |   | $S^+ , S^-$ real | 16 | $Sym^2(S^\pm)^\ast \simeq V  \oplus \wedge_\pm^5 V$ | [[type II supergravity]] |
| 11 |   | $S$ real | 32 | $Sym^2 S^\ast \simeq V \oplus \wedge^2 V \oplus \wedge^5 V$ | [[11-dimensional supergravity]] |

Here $W$ is the 2-dimensional [[complex vector space]] on which the [[quaternions]] naturally act. 


The last column implies that in each dimension there exists a [[linear map]]

$$
  \Gamma \;\colon\; S^\ast \otimes S^\ast \longrightarrow \mathbb{R}^{d-1,1}
$$

which is 

1. symmetric;

1. $Spin(V)$-equivariant.


This is what in the [[physics]] literature is expressed in components by the Gamma matrices with "indices lowered" using the _[[charge conjugation matrix]]_.

This allows to form the [[super Poincaré Lie algebra]] 
hence the [[super Poincaré group]] $sIso(d-1,1|N)$ in each of these cases. 

Finally then: 

[[quotient]] by [[spin group]] is [[super-Minkowski spacetime]]

$$
  \mathbb{R}^{d-1,1|N} = sIso(d-1,1|N)/Spin(d-1,1)
  \,.
$$

#### The curved case
 {#TheCurvedCase}

given $X,Y\in SuperSmooth0Type$ then a morphism $f \colon X\longrightarrow Y$ is a _[[local diffeomorphism]]_ if

$$
  \array{
    X &\longrightarrow& \Im X
    \\
    \downarrow^{\mathrlap{f}} && \downarrow^{\mathrlap{\Im f}}
    \\
    Y &\longrightarrow& \Im Y
  }
$$

is a [[pullback]] square. This comes down to being the appropriate [[synthetic differential supergeometry]]-version  of the traditional statement that $f$ is a local diffeo if the diagram of [[tangent bundles]]

$$
  \array{
    T X &\longrightarrow& X
    \\
    \downarrow^{\mathrlap{T f}} && \downarrow^{\mathrlap{f}}
    \\
    T Y &\longrightarrow& Y
  }
$$

given $V$ a [[super vector space]] and $X \in SuperSmooth0Type$, then we say that $X$ is a $V$-[[manifold]] if there is

$$
  \array{
    && U
    \\
    & \swarrow && \searrow
    \\
    V && && X
  }
$$

with both morphisms being local diffeos and the right one in addition being a [[1-epimorphism]].



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

A formalization as discussed above is considered in 

* _[[schreiber:differential cohomology in a cohesive topos]]_