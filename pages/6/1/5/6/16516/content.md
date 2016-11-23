
> this entry contains one chapter of _[[geometry of physics]]_

> previous chapter: _[[geometry of physics -- manifolds and orbifolds|manifolds and orbifolds]]_

> next chapter: _[[geometry of physics -- BPS charges|BPS charges]]_

>

> Presently this entry is under construction. It is being incrementally expanded as this lecture series progresses: _[[schreiber:From the Superpoint to T-Folds]]_.

#Contents#
* table of contents
{:toc}


In [[nLab:Klein geometry]] and [[nLab:Cartan geometry]] the fundamental geometric concept is the [[nLab:symmetry group]] $G$ of the local model [[nLab:space]], which is then recovered as some [[nLab:coset space]] $G/H$. These symmetry groups $G$ are reflected in their [[nLab:categories of representations]] $Rep(G)$, which are certain nice [[nLab:tensor categories]]. In terms of [[nLab:physics]] via [[nLab:Wigner classification]], the [[nLab:irreducible objects]] in  $Rep(G)$ label the possible [[nLab:fundamental particle]] species on the [[nLab:spacetime]] $G/H$. Hence if we regard the [[nLab:tensor category]] $Rep(G)$ as the actual fundamental concept, then the natural question is that of _[[nLab:Tannaka duality|Tannaka reconstruction]]_: Given any nice [[nLab:tensor category]], is it [[nLab:equivalence of categories|equivalent]] to $Rep(G)$ for some symmetry group $G$? For [[nLab:rigid monoidal category|rigid]] [[nLab:tensor categories]] in [[nLab:characteristic zero]] subject only to a mild size constraint this is answered by **[[nLab:Deligne's theorem on tensor categories]]** (theorem \ref{TheTheorem} below) : all of them are, but only if we allow $G$ to be a "[[nLab:supergroup]]".

(...)

## **Model layer**

* _[Superalgebra](#Superalgebra)_

* _[Supergeometry](#Supergeometry)_

* ...

### Superalgebra
  {#Superalgebra}

this section is at _[[geometry of physics -- superalgebra]]_



### Supergeometry
 {#Supergeometry}

(...)

> under construction

#### Coordinate systems: super Cartesian spaces
 {#CoordinareSystemsSuperCartesianSpaces}


Recall the following from the discussion at _[[geometry of physics -- smooth sets]]_. We will set up [[supergeometry]] in direct analogy to this formulation of plain [[differential geometry]]. See also at _[[geometry of physics -- manifolds and orbifolds]]_ and _[[geometry of physics -- supergeometry]]_.


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

A _[[super-commutative superalgebra]]_ (or just _[[commutative superalgebra]]_ for short)  is a $\mathbb{Z}/2\mathbb{Z}$-[[graded algebra|graded]] [[associative algebra]] $A = A_{even} \oplus A_{odd}$ such that for $a,b$ any two elements in homogeneous degree $deg(a), deg(b)\in \mathbb{Z}/2\mathbb{Z}$, then their product is related by ([[Ausdehnungslehre|Grassmann 1844, §37, §55]])

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
  (C^\infty(\mathbb{R}^n) \oplus \epsilon C^\infty(\mathbb{R}^n))
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


### Spacetime supersymmetry



this section is at _[[geometry of physics -- supersymmetry]]_



### Fundamental super $p$-branes

(...)


#### Motivation and survey


The _[[Green-Schwarz action functional]]_ is an [[action functional]] for a [[sigma-model]] that describes the propagation of a fundamental $p$-[[brane]] $\Sigma$ on a [[supermanifold]] [[spacetime]].

* For $p = 0$ this is the **Green-Schwarz [[superparticle]]**.

* For $p = 1$ the **Green-Schwarz [[superstring]]** (at the center of attention in [[string theory]]). This model is in contrast to the _[[NSR-string]]_ model, which instead has manifest [[worldsheet]] [[supersymmetry]]. See at _[[superstring]]_ for more on this.


[[perturbation theory|Perturbative]] [[string theory]] on geometric backgrounds is defined by the [[Neveu-Schwarz-Ramond model]], namely by [[sigma-model]] [[2d super conformal field theories]] (of [[central charge]] 15) on [[worldsheets]] $\Sigma$ that are [[super Riemann surfaces]], with [[target spaces]] $X$ that are ordinary (i.e. "bosonic") [[spacetime]] [[manifolds]].

These worldsheet field theories are induced from _[[action functionals]]_, namely variants of the standard [[energy functional]] ([[Polyakov action]]) on the space $[\Sigma,X]$ of smooth functions

$$
  \phi \;\colon\; \Sigma \longrightarrow X
  \,.
$$

The central theorem of perturbative superstring theory says that the spectrum of such a 2d SCFT are the quanta of the [[perturbation theory|perturbations]] of a higher dimensional [[effective field theory|effective]] [[supergravity]] [[field theory]] on target spacetime, hence transforms under [[supersymmetry]] on target spacetime.

This is the fundamental prediction of the assumption of fundamental strings: assuming 1) that the particles that run in [[Feynman diagrams]] are fundamentally strings, and demanding 2) that there are fermionic particles among these, first implies that the strings must be [[spinning strings]] (have fermions on their worldsheet), which implies that they are [[superstrings]] (worldsheet [[supersymmetry]] mixes the worldsheet bosons and fermions), which then in addition implies that their target space [[effective field theory]] is [[supergravity]], hence that also the effective target space fields exhibit local supersymmetry.

$$
  \underset{spinning\; string}{\underbrace{fermions \;+\; strings}}
  \;=\;
  superstring \;\Rightarrow\; supergravity
  \,.
$$

The first step in this implications (spinning string is superstring) is straightforward, but the second step appears as a miracle from the point of view of the NSR string. It comes out this way by non-trivial computation, but is not manifest in the theory.

In order to improve on this situation, Green and Schwarz searched and found ([Green-Schwarz 81](#GreenSchwarz81), [Green-Schwarz 82](#GreenSchwarz82) [Green-Schwarz 84](#GreenSchwarz84), for the history see [Schwarz 16, slides 24-25](#Schwarz16)) a suitably equivalent string [[action functional]]  that would manifestly exhibit spacetime supersymmetry. This is now called the _[[Green-Schwarz action functional]]_.

| [[action functional]] for [[superstring]] | manifest [[supersymmetry]] |
|----|---|
| [[Ramond-Neveu-Schwarz string]] | on [[worldsheet]]  |
| Green-Schwarz string | on [[target space|target]] [[spacetime]] |

The basic idea is to pass to the evident [[supergeometry|supergeometric]] analogue of the bosonic string action:

Let $\Sigma$ be a [[closed manifold]] of [[dimension]] 2 -- representing the abstract _[[worldsheet]]_ of a string. Let $(X,g)$ be a [[pseudo-Riemannian manifold]] -- representing a purely [[gravity|gravitational]] [[spacetime]] background. Then the [[action functional]] governing the [[bosonic string]] propagating in this spacetime is the functional

$$
  \exp(\tfrac{i}{\hbar} S_{bos})
  \;\colon\;
  [\Sigma,X]
   \longrightarrow
  \mathbb{R}/_{\hbar}\mathbb{Z}
$$

on the [[smooth space|smooth]] [[mapping space]] $[\Sigma,X]$ of [[smooth functions]] $\Sigma \to X$, that simply assigns the proper relativistic [[volume]] of the image of the [[worldsheet]] $\Sigma$ in [[spacetime]]:

$$
  (\Sigma\overset{\phi}{\longrightarrow} X)
    \;\mapsto\;
  \int_\Sigma vol_{\phi^\ast g}
  \,.
$$

(This is the _[[Nambu-Goto action]]_. It is classically equivalently to the [[Polyakov action]] which is the genuine starting point for the quantum [[Neveu-Schwarz-Ramond string]]. Howver, since, as we discuss below, the Green-Schwarz action naturally generalizes to that of other $p$-[[branes]] it is more natural to consider the Nambu-Goto form of the action here.)

When here $(X,g)$ is generalized to a [[superspacetime]] [[supermanifold]] with [[orthogonal structure]] encoded by a [[super-vielbein]] $e$ (see at _[[super Cartan geometry]]_ for details), then the same form of the action functional still makes sense and produces a functional on the [[supergeometry|supergeometric]] [[mapping space]] $[\Sigma,X]$. Moreover, by construction this action functional is invariant under the [[superisometry group]] of $(X,g)$, hence under spacetime [[supersymmetry]].


$$
\array{
  \text{symmetry of worldsheet theory}
  \\
  \array{
    && \Sigma
    \\
    & {}^{\mathllap{\phi}}\swarrow && \searrow^{\mathrlap{\phi'}}
    \\
    X &&\underset{\simeq}{\longrightarrow}&& X
  }
  \\
  \text{super-isometry of target spacetime}
}
$$

However, Green and Schwarz noticed that this [[kinetic action]] functional $\phi \mapsto \int_\Sigma vol_{\phi^\ast e}$ does _not_ quite yield dynamics that is equivalent to that of the NSR string: when the [[equations of motion]] hold ("on shell") it has more fermionic degrees of freedom than present in the NSR string. The key insight of Green and Schwarz was that one may add an extra summand to the action functional to the plain super-Nambu-Goto action, such that the resulting functional enjoys a further 1-parameter symmetry, called _[[kappa-symmetry]]_,  and such that restricting to the $\kappa$-symmetric states, then the action functionals do become classically equivalent.

Moreover, they showed that in [[light-cone gauge]] the resulting quantum dynamics is equivalent to that of the [[NSR string]], thus providing a conceptual proof for the observed local spacetime supersymmetry for backgrounds that admit two lightlike Killing vectors. (The quantization of the GS-string away from lightcone gauge however remains an open problem.)


Green-Schwarz's extra [[kappa-symmetry]] term serves a clear purpose, but originally its geometrically meaning was mysterious. However, in ([Henneaux-Mezincescu 85](#HenneauxMezincescu85)) it was observed (expanded on in ([Rabin 87](#Rabin87), [Azcarraga-Townsend 89](#AzcarragaTownsend89), [Azcarraga-Izquierdo 95,chapter 8](#AzcarragaIzquierdo95))), that the Green-Schwarz-action functional describing the string in $d+1$-dimensions has a neat geometrical interpretation: it is simply the ([[parameterized WZW model|parameterized]]) [[WZW-model]] for

1. target space being locally [[super Minkowski spacetime]] $\mathbb{R}^{d-1,1|\mathbf{N}}$ regarded as the [[coset]] [[supergroup]]

   $$
     \mathbb{R}^{d-1,1\vert \mathbf{N}}
       \;\simeq\;
     Iso(\mathbb{R}^{d-1,1\vert \mathbf{N}}) / Spin(d-1,1)
   $$

   for $\mathbf{N}$ a real [[spin representation]] (the "number of supersymmetries"), $Iso(\mathbb{R}^{d-1,1\vert \mathbf{N}})$ the corresponding [[super Poincaré group]] and $Spin(d-1,1)$ its [[Lorentzian manifold|Lorentz-signature]] [[spin group|Spin]] [[subgroup]];

1. [[WZW-term]] being a local potential for the the unique (up to rescaling, if it exists) $Spin(d-1,1)$-invariant [[group cocycle|group 3-cocycle]] $\mu_3$ on $Iso(\mathbb{R}^{d-1,1\vert \mathbf{N}})$, with component locally given by the Gamma-matrices of the given [[Clifford algebra]] representation.

More in detail, just as ordinary [[Minkowski spacetime]] $\mathbb{R}^{d-1,1}$ may be identified with the [[translation group]] with canonical basis of [[left invariant 1-forms]] given by the canonical [[vielbein]] field

$$
  \{e^a \coloneqq \mathbf{d}x^a\}_{a = 0}^{d-1}
  \,,
$$

where $\{x^a\}$ are the canonical [[coordinates]] on $\mathbb{R}^{d-1,1}$, so [[super Minkowski spacetime]] $\mathbb{R}^{d-1,1\vert \mathbf{N}}$ for some real [[spin representation]] $\mathbf{N}$ is characterized as the [[supergroup]] whose [[left invariant 1-forms]] consitute the $\mathbb{Z} \times \mathbb{Z}/2\mathbb{Z}$-bigraded differential with generators the [[super-vielbein]]

$$
  \underset{deg = (1,even)}{\underbrace{e^a}}
    \;\coloneqq\;
  \mathbf{d}x^a + \tfrac{i}{2}\overline{\theta}\Gamma^a \mathbf{d} \theta
  \;\;\;\,,\;\;\;\;\;\;\;\;\;\;
  \underset{deg = (1,odd)}{\underbrace{\psi^\alpha}} \;\coloneqq\; \mathbf{d}\theta^\alpha
  \,,
$$

where $(x^a, \theta^\alpha)$ are the canonical coordinates on $\mathbb{R}^{d-1,1\vert \mathbf{N}}$, with the odd-graded elements $\{\theta^\alpha\}$ spanning the given real [[spin representation|Spin(d-1,1)-representation]] $\mathbf{N}$ with [[Clifford algebra]] generators $\{\Gamma^a\}$.

Now while ordinary [[Minkowski spacetime]] $\mathbb{R}^{d-1,1}$ is an [[abelian group]], reflected by the fact that its [[left-invariant 1-forms]] are all closed

$$
  \mathbf{d}e^a = 0 \;\;\;\;\;\; on \; \mathbb{R}^{d-1,1}
  \,,
$$

the key phenomenon of [[supersymmetry]] (that two [[fermions]] pair to a [[bosons]]) means that $\mathbb{R}^{d-1,1\vert \mathbf{N}}$ is slightly non-abelian, reflected by the fact that the [[super-vielbein]] is not closed

$$
  \mathbf{d} e^a = \tfrac{i}{2} \overline{\psi} \Gamma^a \psi
  \;\,,\;\;\;\;\;\;
  \mathbf{d} \psi^\alpha = 0
  \,.
$$

This is the source of all the rich structure seen in Green-Schwarz theory.

In particular, for special combinations of spacetime dimension $d$ and number of supersymmetries $\mathbf{N}$ the 3-form


$$
  \mu_3 \;\coloneqq\;  \overline{\psi} \wedge \Gamma_a \psi \wedge e^a
$$

is a non-trivial [[super Lie algebra|super]] [[Lie algebra cocycle]] on $\mathbb{R}^{d-1,1\vert \mathbf{N}}$, in that $\mathbf{d}\mu_3 = 0$ and so that there is no [[left invariant differential form]] $b$ with $\mathbf{d}b = \mu_3$.

This happens notably for $d = 10$ and $\mathbf{N} = (1,0)$ ([[heterotic string]]) or $\mathbf{N} = (2,0)$ ([[type IIB superstring]]) and $\mathbf{N} = (1,1)$ ([[type IIA superstring]]). (It also happens in some lower dimensions, where however the corresponding NSR-string develops a [[conformal anomaly]] after quantization ("non-critical strings"). This classification of cocycles is part of what has come to be known as the _[[brane scan]]_ in superstring theory, see below.)

In this equivalent formulation, the Green-Schwarz action functional for the superstring has the following simple form:

Let $(X,e)$ be a [[superspacetime]], hence a [[supermanifold]] $X$ equipped with a [[super-vielbein]] $e$ (super-[[orthogonal structure]]) which is locally modeled on $\mathbb{R}^{d-1,1\vert \mathbf{N}}$ (technically: a [[torsion of a G-structure|torsion]]-free [[super-Cartan geometry]] modeled on $Spin(d-1,1) \hookrightarrow Iso(\mathbb{R}^{d-1,1\vert \mathbf{N}})$). Write $\mu_3^X \in \Omega^3(X)$ be the [[super differential form]] on $X$ which is the induced [[definite globalization of WZW term|definite globalization]] of the cocycle $\mu_3$ over $X$. For $U \subset X$ any contractible subspace, then the restriction of $\mu^X_3|_{U} \in \Omega^3(U)$ of $\mu_3^X$ to $U$ is exact, and hence admits a potential $B_U \in \Omega^2(U)$, i.e. such that $d B = \mu^X_3|_U$.

Then for $\Sigma$ a 2-dimensional [[closed manifold]], the Green-Schwarz action functional

$$
  \exp(\tfrac{i}{\hbar} S_{GS})
  \;\colon\;
  [\Sigma,X]_U
    \longrightarrow
  \mathbb{R}/_{\hbar} \mathbb{Z}
$$

is the function on the super-[[smooth space]] $[\Sigma,X]_U$ of smooth maps of supermanifolds $\phi \colon \Sigma \to X$ which factor through $U$, given by

$$
  \phi
    \;\mapsto\;
  \int_\Sigma vol_{\phi^\ast e}
   \;+\;
  \int_\Sigma \phi^\ast B_U
  \;\;\;\,,\;\;\;\;\;\;\;\;\;
  \mathbf{d} B_U = \mu^X_3|_U
  \,.
$$

In order to get rid of the restriction to some $U \subset X$ one needs to add global data. The need for this is at least mentioned briefly in ([Witten 86, p. 261 (17 of 20)](#Witten86)), but had otherwise been ignored in the physics literature. The general solution is to promote the local potentials $B$ to the connection $\hat B$ on a [[Super Gerbes|super gerbe]] ([Fiorenza-Sati-Schreiber 13](#FiorenzaSatiSchreiber13)). This is a choice of [[higher prequantization]]

$$
  \array{
    && \mathbf{B}^{2}(\mathbb{R}/_\hbar \mathbb{Z}) & \text{prequantization}
    \\
    & {}^{\mathllap{\hat B}}\nearrow & \downarrow^{\mathrlap{curv}}
    \\
    X
     &\underset{\mu^X_3}{\longrightarrow}&
    \mathbf{\Omega}^3
    &
    \text{3-form curvature}
  }
  \,.
$$


Writing $\int_\Sigma \phi^\ast \hat B$ for the [[volume holonomy]] of a [[circle 2-bundle with connection]] $\hat B$, then the globally defined Green-Schwarz sigma model

$$
  \exp(\tfrac{i}{\hbar} S_{GS})
  \;\colon\;
  [\Sigma, X]
    \longrightarrow
  \mathbb{R}/_\hbar\mathbb{Z}
$$

is given by

$$
  \phi \;\mapsto\; \int_\Sigma vol_{\phi^\ast} + \int_\Sigma \phi^\ast \hat B
  \;\;\,,
  \;\;\;\;\;\;\;
  curv(\hat B) = \mu_3^X
  \,.
$$

This form of the Green-Schwarz action functional for the string has evident generalization to other $p$-[[branes]]. Whenever there is a Lorentz-invariant $(p+2)$-cocycle $\mu_{p+2}$ on $\mathbb{R}^{d-1,1\vert \mathbf{N}}$, then one may ask for a higher gerbe ([[higher prequantum line bundle]]) $\hat C$ with [[curvature]] $\mu^X_{p+2}$ and consider the analogous functional.

The triples $(d,\mathbf{N},p)$ (spacetime dimension, number of supersymmetries, dimension of brane) such that

$$
  \mu_{p+2}
    \;\coloneqq\;
  \overline{\psi} \wedge \Gamma^{a_1 \cdots a_p} \psi \wedge e_{a_1} \wedge \cdots \wedge e_{a_p}
$$

is a nontrivial cocycle, hence for which there is such a Green-Schwarz action functional for $p$-branes on $\mathbb{R}^{d-1,1\vert \mathbf{N}}$ may be classified and form what is called the _[[brane scan]]_ ([Ach&#250;carro-Evans-TownsendWiltshire 87](#AETW87), [Brandt 12-13](#Brandt12-13)):

{#DuffBraneScan} <div style="float:left;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/DuffBraneScan.jpg" height="600">
</div>

The graphics on the left is from ([Duff 87](#Duff87)). The diagonal lines indicate [[double dimensional reduction]], taking a $(p+1)$-brane in $(d+1)$ dimensions to a $p$-brane in $d$-dimensions.

For instance for $(d = 11, \; \mathbf{N} = \mathbf{32}, \; p = 2)$ one finds a cocycle, and the corresponding GS-action functional is that of the fundamental [[M2-brane]].

This was a striking confluence of brane physics and classification of [[super Lie algebra|super]] [[Lie algebra cohomology]]. But just as striking as the matching, was what it lacked to match: the [[D-branes]] and the [[M5-brane]] ($d = 11$, $p = 5$) are lacking from the old brane scan. Incidentally, these lacking branes are precisely those branes on which the branes that do appear on the brane scan may end, equivalently those branes that have [[higher gauge fields]] on their [[worldvolume]] (tensor multiplets).

An action functional for the [[M5-brane]] vaguely analogous to a Green-Schwarz action functional was found in ([BLNPST 97](#BLNPST97), [APPS 97](#APPS97)). It is again the sum of a kinetic term and a WZW-like term, but the WZW-like term does not come from a cocycle on a (super-)group.

In order to deal with this, it was suggested in ([CAIB 99](#CAIB99), [Sakaguchi 00](#Sakaguchi00), [Azcarraga-Izquierdo 01](#AzcarragaIzquierdo01)) that there is an algebraic structure called "[[extended super-Minkowski spacetimes]]" that generalizes [[super Minkowski spacetime]] and serves to unify the Green-Schwarz-like models for the D-branes and the M5-brane with the original Green-Schwarz models for the string and the M2-brane.

These [[extended super-Minkowski spacetimes]] carry algebraic analogs of super Lie algebra cocycles, such that the relevant terms for the [[D-branes]] and the [[M5-brane]] do appear after all, hence such that all the branes in [[string theory]]/[[M-theory]] are unified. In fact these "[[extended super-Minkowski spacetimes]]" are precisely the "FDA"s that have been introduced before in the [[D'Auria-Fré formulation of supergravity]] and what became identified as the 7-cocycle for the [[M5-brane]] this way had earlier been recognized algebraically as an stepping stone for an elegant re-derivation of [[11-dimensional supergravity]] ([D'Auria-Fr&#233; 82](#DAuriaFre82)).

The ([[higher differential geometry|higher]]) geometric meaning of these constructions was found in ([Fiorenza-Sati-Schreiber 13](#FiorezaSatiSchreiber13)): these algebraic structures of "[[extended super-Minkowski spacetimes]]"/FDAs are precisely the [[Chevalley-Eilenberg algebras]] of [[super Lie n-algebra]]-extensions of [[super-Minkowski spacetime]] which are classified by the cocycles that serve as the GS-WZW terms of the $p_1$-branes that may end on those $p_2$-branes whose cocycles are carried by the extended super-Minkowski spacetime.

Hence the missing $p$-branes in the old [[brane scan]] (classifying just cocycles on [[super Lie algebras]]) do appear as one generalizes (super) Lie algebras to (super) [[strong homotopy Lie algebras]] = [[L-infinity algebras]]. Moreover, each brane intersection law (one brane species may end on another) is now matched to a super $L_\infty$-algebra [[extension]] and so the old brane scan is generalized to a tree of branes _[[schreiber:The brane bouquet]]_:

<img src="https://dl.dropboxusercontent.com/u/12630719/BraneBouquet.JPG" alt="the brane bouquet" width="900" />

Each item in this bouquet denotes a [[super L-infinity algebra]] and each arrow denotes an [[L-infinity extension]] classified by a cocycle which encodes the GS-WZW term of the brane named by the domain of the arrow. Moreover, arrows pass exactly from one brane species to the brane species that may end on the former.

In ([Fiorenza-Sati-Schreiber 13](#FiorenzaSatiSchreiber13)) it is shown that all these [[super L-infinity algebras]] [[Lie integration|Lie integrate]] to [[smooth super-n-groups]], and all the cocycles [[Lie integration|Lie integrate]] to [[Super Gerbes|super-gerbes]] on these, such that the induced [[volume holonomy]] is the relevant generalized GS-WZW term. For detailed exposition see at _[[schreiber:Structure Theory for Higher WZW Terms]]_.

With this generalized perspective, now the Green-Schwarz-type action functionals describe _all_ the [[p-branes]] in [[string theory]]/[[M-theory]].

Again, in order to make this generally true one needs to apply a [[higher prequantization]] -- a choice of [[line n-bundle with connection|line (p+1)-bundle with connection]] -- in order to globalize the [[WZW-terms]] ([Fiorenza-Sati-Schreiber 13](#FiorenzaSatiSchreiber13))

$$
  \array{
    && \mathbf{B}^{p+1}(\mathbb{R}/_\hbar \mathbb{Z}) & \text{prequantization}
    \\
    & {}^{\mathllap{\hat A_{p+1}}}\nearrow & \downarrow^{\mathrlap{curv}}
    \\
    X
     &\underset{\mu^X_{p+2}}{\longrightarrow}&
    \mathbf{\Omega}^{p+2}
    &
    (p+2)\text{-form curvature}
  }
  \,.
$$

Hence $\hat A_{p+1}$ is the actual [[background field]] that the $p$-brane couples to. There is considerably more information in $\hat A_p$ than in its curvature $curv(\hat A_{p+1}) = \mu_{p+2}$. For instance for the [[M2-brane]] one may find the local super [[moduli space]] for local choices of $\hat A_{p+1}$ for the given $\mu_{4}$ on [[KK-compactifications]] to $d = 4$. It turns out that the bosonic [[body]] of this moduli space is the [[exceptional tangent bundle]] on which the [[U-duality]] group [[E7]] has a canonical action (see at _[[schreiber:From higher to exceptional geometry]]_).

This highlights that Green-Schwarz functionals capture fundamental ("microscopic") aspects of $p$-branes. In contrast, often $p$-branes are discussed in their [[soliton|solitonic]] incarnation as _[[black branes]]_. These solitonic branes sit at asymptotic boundaries of [[anti-de Sitter spacetime]] and carry [[conformal field theories]], related to the ambient [[supergravity]] by [[AdS-CFT duality]].

This phenomenon is indeed a consequence of the fundamental Green-Schwarz branes:

Consider a 1/2-[[BPS state]] solution of [[type II supergravity]] or [[11-dimensional supergravity]], respectively. These solutions locally happen to have the same classification as the Green-Schwarz branes. Hence we may consider a configuration $\phi \colon \Sigma \to X$ of the corresponding fundamental $p$-brane which embeds $\Sigma$ into the asymptotic AdS boundary of the given 1/2 BPS spacetime $X$. Then it turns out that restricting the Green-Schwarz action functional to small fluctuations around this configuration, and applying a [[diffeomorphism]] [[gauge fixing]], then the resulting action functional is that of a [[supersymmetry|supersymmetric]] [[conformal field theory]] on $\Sigma$ as in the [[AdS-CFT]] dictionary:

| fundamental $p$-brane | -fluctuations about asymptotic AdS configuration$\to$ |  solitonic $p$-brane |
|----|-----|---|
| Green-Schwarz action functional |  | [[supersymmetric|super]]-[[conformal field theory]] |

([Claus-Kallosh-Proeyen 97](#ClausKalloshProeyen97), [Claus-Kallosh-Kumar-Townsend 98](#ClausKalloshKumarTownsend98), [AFFFTT 98](#AFFFTT98) [Pasti-Sorokin-Tonin 99](#PastiSorokinTonin99))

In fact the [[BPS-state]] condition itself is neatly encoded in the Green-Schwarz action functionals: by construction they are invariant under the [[spacetime]] [[superisometry group]]. Hence the [[Noether theorem]] implies that there are corresponding [[conserved currents]], whose [[Dickey bracket]] forms a super-[[Lie algebra extension]] of the Lie algebra of supersymmetries.

$$
  \array{
    \left\{
    \array{
      X && \overset{=}{\longrightarrow} && X
      \\
      & {}_{\mathllap{\hat C}}\searrow
        &\swArrow&
      \swarrow_{\mathrlap{\hat C}}
      \\
      && \mathbf{B}^{p+1}(\mathbb{R}/_{\hbar} \mathbb{Z})
    }
    \right\}
      &\longrightarrow&
    \left\{
    \array{
      X && \overset{\simeq}{\longrightarrow} && X
      \\
      & {}_{\mathllap{\hat C}}\searrow
        &\swArrow&
      \swarrow_{\mathrlap{\hat C}}
      \\
      && \mathbf{B}^{p+1}(\mathbb{R}/_{\hbar} \mathbb{Z})
    }
    \right\}
     &\longrightarrow&
    \left\{
      \array{
        X && \overset{\simeq}{\longrightarrow} && X
      }
    \right\}
    \\
    \text{topological currents}
    &&
    \text{Noether currents}
    &&
    \text{symmetries}
  }
$$

Here the "$\swArrow$" filling the triangles is the non-trivial gauge transformation by which the [[WZW term]] (as any WZW term) is preserved under the symmetries (instead of being fixed identically). It is the information in this transformations which makes the currents form an extension of the symmetries.

Here this yields the famous brane charge extensions of the super-isometry super Lie algebra of the schematic form

$$
  \{Q_\alpha, Q_\beta\}
  \;=\;
  (C \Gamma^a_{\alpha \beta}) P_a
  \;+\;
  (C \Gamma^{a_1 \cdots a_p})_{\alpha \beta} Z_{a_1, \cdots, a_p}
$$

(for $Q$ a [[Killing spinor]] and $P$ its corresponding [[Killing vector]]) known as the [[type II supersymmetry algebra]] and the [[M-theory supersymmetry algebra]], respectively ([Azc&#225;rraga-Gauntlett-Izquierdo-Townsend 89](#AGIT89)). In fact it yields super-[[L-infinity algebra extensions|Lie n-algebra extensions]] of which the familiar super Lie algebra extensions are the 0-truncation ([Sati-Schreiber 15](#SatiSchreiber15), [[schreiber:Local prequantum field theory|Khavkine-Schreiber 16]]).

In summary, the nature and classification of Green-Schwarz action functionals captures in a mathematically precise way a good deal of the core structure of [[string theory|string]]/[[M-theory]].

In fact, the [[super L-infinity algebra|super L-infinity algebraic]] perspective on the Green-Schwarz functionals via [[schreiber:The brane bouquet]] also solves the following open problem on [[M-branes]]:

it is famously known from [[Freed-Witten anomaly]]-cancellation that the [[D-brane charges]] are not in fact just in [[de Rham cohomology]] in every second degree, but are in [[twisted K-theory]], hence [[rational homotopy theory|rationally]] in [[twisted de Rham cohomology]], with the twist being the [[F1-brane]] charge (from the fundamental). It is an open problem to determine what becomes of these [[twisted K-theory]] charge groups as one lifts F1/D$p$-branes in string theory to M2/M5-branes in [[M-theory]].


|   | intersecting branes | charges in [[generalized cohomology theory]]
|-----|--------------|----------------------|
| [[string theory]] | [[F1-brane|F1]]/[[D-brane|Dp-branes]] | [[twisted K-theory]] |
| [[M-theory]]  | [[M2-brane|M2]]/[[M5-branes]] | ??? |

Notice that there are "microscopic degrees of freedom" of the theory encoded by the choice of [[generalized cohomology theory]] here, generalizing the extra degrees of freedom in the choice of a WZW-term already mentioned above. In general for $E$ a cohomology theory and $E \longrightarrow E \otimes \mathbb{Q}$ its [[Chern character]] map (for instance from [[topological K-theory]] to [[ordinary cohomology]] in every second degree), then a choice of genuine charges is the extra information encoded in a lift

$$
  \array{
    && E
    \\
    & {}^{\mathllap{\text{true charge}}}\nearrow & \downarrow^{\mathrlap{ch}}
    \\
    X &\underset{\text{rational} \atop  \text{charge}}{\longrightarrow}& E \otimes \mathbb{Q}
  }
$$

But [[rational homotopy theory|rationally]] [[schreiber:The brane bouquet]] allows to derive this from first principles:

Above we saw that the naive cocycles of the [[D-branes]] and of the [[M5-brane]] are not defined on the actual [[spacetime]],  but on some "extended" spacetime, which is really a [[smooth super infinity-groupoid]] extension of spacetime. Hence we should ask if these cocycles [[descent|descend]] to the actual super-spacetime while picking up some twists.

One may prove that:

* the F1/D$p$-brane GS-WZW cocycles descend to 10d type II superspacetime to form a single cocycle in rational twisted K-theory, just as the traditional lore reqires ([Fiorenza-Sati-Schreiber 16](#FiorenzaSatiSchreiber16));

* the M2/M5 GS-WZW cocycles descent to 11d superspacetime to form a single cocycle with values in the [[rational n-sphere|rational 4-sphere]] ([Fiorenza-Sati-Schreiber 16](#FiorenzaSatiSchreiber16)).

This has implications on some open conjectures regarding [[M-theory]], for more on this see _[[schreiber:Equivariant cohomology of M2/M5-branes]]_.









#### Super Lie $n$-algebras

(...) 

 [[super L-infinity algebra]] 
 
 (...)

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











#### The old brane scan
 {#TheOldBraneScan}

+-- {: .num_defn #LineLienAlgebra}
###### Definition

For $p \in \mathbb{N}$ write $b^{p+1}\mathbb{R}$ for the [[line Lie n-algebra|Line Lie (p+2)-algebra]], given by the [[Chevalley-Eilenberg algebra]] of the form

$$
  CE(b^{p+1}\mathbb{R})
  \coloneqq
  (\langle g_{p+2} \rangle,  d g_{p+2} = 0)
  \,.
$$

=--


+-- {: .num_defn #ThePsiPsiTermsInCEOfSuperMinkowski}
###### Definition

For $\mathbb{R}^{d-1,1\vert \mathbf{N}}$ a [[super Minkowski spacetime]], def. \ref{SuperPoincareAndSuperMinkowski}, regarded as a [[super Lie algebra]], write

$$
  \mu_{p+2}\in CE(\mathbb{R}^{d-1,1\vert \mathbf{N}})
$$

for the element of its [[Chevalley-Eilenberg algebra]] of the form

$$
  \mu_{p+2}
  \coloneqq
  \overline{\psi} \wedge \Gamma^{a_1 \cdots a_p} \psi \wedge e_{a_1} \wedge \cdots \wedge e_{a_p}
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

The study of the CE-elements in def. \ref{ThePsiPsiTermsInCEOfSuperMinkowski} goes back to ([D'Auria-Fr&#233; 82](#DAuriaFre82)). These authors write $\frac{i}{2}\overline{(-)}\Gamma (-)$ for the bilinear pairing which we write just $\overline{(-)}\Gamma (-)$.

=--

One finds that the elements $\mu_{p+2}$ in def. \ref{ThePsiPsiTermsInCEOfSuperMinkowski} are CE-closed, hence are super Lie algebra cocycles for given $(d,p,N)$, precisely if there is a [[super p-brane]] in $N$-supersymmetric super-Minkowski spacetime on which no other super $p$-brane may end. For "$N=1$" there are (non-trivial) cocycles in dimension $d$ and degree $(p+2)$ as shown in this table:

| $\stackrel{d}{=}$ |  $p =$ | 1 | 2 | 3 | 4 | 5 | 6 | 7 |  8 |  9 |
|--|--------|---|---|---|---|---|---|---|----|----|
| 11 | |  |  [[M2-brane|M2]] |  |   |  |   |   |   |   |
| 10 |  | [[F1-brane|F1]]   |   |  |   | [[NS5-brane|NS5]] |   |   |   |   |
| 9 | |   |   |  | $\ast$  |  |   |   |   |   |
| 8 | |   |   | $\ast$ |   |  |   |   |   |   |
| 7 | |   | $\ast$  |  |   |  |   |   |   |   |
| 6 | |  $\ast$  |  | [[3-brane in 6d|S3]] |   |  |   |   |   |   |
| 5 | |  | $\ast$   | |   |  |   |   |   |   |
| 4 | | $\ast$  | [[super 2-brane in 4d|M2]]$_{cmp}$   | |   |  |   |   |   |   |
| 3 | | [[super 1-brane in 3d|F1]]$_{cmp}$  |  | |   |  |   |   |   |   |










#### The full brane scan

Every Lie algebra cocycle $\mu_{p+2} \colon \mathfrak{g} \longrightarrow b^{p+1}\mathbb{R}$ induces a [[L-∞ algebra cohomology|higher extension]] of its domain, namely the [[Lie n-algebra|Lie (p+1)-algebra]] $\hat \mathfrak{g}$ which is the [[homotopy fiber]] of $\mu_{p+2}$ in the [[homotopy theory of L-∞ algebras]]:

$$
  \array{
     \hat \mathfrak{g}
     \\
     \downarrow
     \\
     \mathfrak{g}
     &\stackrel{\mu_{p+2}}{\longrightarrow}&
     b^{p+1}\mathbb{R}
  }
  \,.
$$

For the cocycles on [[super Minkowski spacetime]] from the [old brane scan](#TheOldBraneScan) these extensions are known as _[[extended super Minkowski spacetimes]]_.

$$
  \array{
     \hat \mathbb{R}^{d-1,1\vert \mathbf{N}}
     \\
     \downarrow
     \\
     \mathbb{R}^{d-1,1\vert \mathbf{N}}
     &\stackrel{\mu_{p+2}}{\longrightarrow}&
     b^{p+1}\mathbb{R}
  }
  \,.
$$

Now the extended super Minkowski spacetime $\hat \mathbb{R}^{d-1,1\vert \mathbf{N}}$ may carry further cocycles, that do not come from ordinary super Minkowski spacetime. Including these yields the full brane scan.

This complete brane scan is no longer just a table, but is a tree, a bouquet, where each edge is an $L_\infty$-extension.









##### The M5-brane




+-- {: .num_defn #RationalSphereAlgebra}
###### Definition

For $p \in \mathbb{N}_{even}$, write

$b^{2p+2} \mathbb{R}/b^p \mathbb{R}$ for the [[L-∞ algebra]] given by the [[Chevalley-Eilenberg algebra]]

$$

  CE(b^{2p+2} \mathbb{R}/b^p \mathbb{R})
  =
  \left(\left\langle g_{p+2}, g_{2p+3}\right\rangle), {{d g_{p+2} = 0} \atop {d g_{2p+3} = g_{p+2} \wedge g_{p+2}}}\right)
  \,.
$$

=--

+-- {: .num_remark #RationalSpheres}
###### Remark

Regarded as a [[Sullivan model]] in [[rational homotopy theory]], then the [[dg-algebra]] of def. \ref{RationalSphereAlgebra} is a minimal model for the [[rationalization]] of the $(p+2)$-[[sphere]].

=--

By the [recognition theorem for L-∞ extensions](model+structure+for+L-infinity+algebras#HomotopyFiberProducts) we get:

+-- {: .num_prop #b2RactionOnb2p2R}
###### Proposition

For $p \in \mathbb{N}_{even}$, there is a [[homotopy fiber sequence]] in the [[homotopy theory of L-∞ algebras]] of the form

$$
  \array{
    b^{2p+2} \mathbb{R}
    \\
    \downarrow
    \\
    b^{2p+2} \mathbb{R}/b^{p}\mathbb{R}
    &\stackrel{}{\longrightarrow}&
    b^{p+1}\mathbb{R}
  }
$$

where on [[formal dual]] [[Chevalley-Eilenberg algebras]] in terms of our defining generating elements the horizontal map is given by $g_{p+4}\mapsto g_{p+4}$ and the vertical map by $g_{p+4}\mapsto 0$ and $g_{2p+3}\mapsto g_{2p+3}$.

By the discussion at _[[∞-action]]_ this exhibits a $b^{p}\mathbb{R}$-action on $b^{2p+2}\mathbb{R}$, for which $b^{2p+2} \mathbb{R}/b^{p}\mathbb{R}$ is the [[homotopy quotient]], whence the notation.

=--

+-- {: .num_example}
###### Example

For $p=2$ and regarded as a statement in [[rational homotopy theory]] via remark \ref{RationalSpheres}, then the extension in prop. \ref{b2RactionOnb2p2R} is a [[Sullivan minimal model]] for the rationalized [[Hopf fibration]]

$$
  \array{
    S^3 &\longrightarrow& S^7
    \\
    && \downarrow
    \\
    && S^4
  }
$$

=--


+-- {: .num_defn #CocyclesOn11dSuperMinkowski}
###### Proposition

The elements $\mu_4, \mu_7 \in CE(\mathbb{R}^{10,1\vert \mathbf{32}})$,
def. \ref{ThePsiPsiTermsInCEOfSuperMinkowski}, satisfy

1. $d \mu_4 = 0$;

1. $d \mu_7 = 15 \, \mu_4 \wedge \mu_4$

=--

As a mathematical statement prop. \ref{CocyclesOn11dSuperMinkowski} is originally due to ([D'Auria-Fr&#233; 82, p.18](#DAuriaFre82)), where it is considered as an ingredient for constructing the [[action functional]] of [[11-dimensional supergravity]] in the [[D'Auria-Fré formulation of supergravity]]. The statement has been rediscovered in ([BLNPST 97, (9)](#BLNPST97)), finding its interpretation as giving the [[geometry of physics -- WZW terms|WZW term]] of the [[Green-Schwarz sigma model]] for the [[M5-brane]].


+-- {: .num_defn #m2braneLie3Algebra}
###### Definition

Write $\mathfrak{m}2\mathfrak{brane} \in sL_\infty Alg$ for the [[super L-∞ algebra]] which is the [[homotopy fiber]] of $\mu_4$ in prop. \ref{CocyclesOn11dSuperMinkowski}.

$$
  \array{
     \mathfrak{m}2\mathfrak{brane}
     \\
     \downarrow
     \\
     \mathbb{R}^{10,1\vert \mathbf{32}}
     &\stackrel{\mu_4}{\longrightarrow}&
     b^3 \mathbb{R}
  }
  \,.
$$

and specifically for the representive of this homotopy fiber which, by the [recognition theorem for L-∞ extensions](model+structure+for+L-infinity+algebras#HomotopyFiberProducts), is given by having the [[Chevalley-Eilenberg algebra]]

$$
  CE(\mathfrak{m}2\mathfrak{brane}) = (CE(\mathbb{R}^{10,1\vert \mathbf{32}})\otimes \langle h_3\rangle, d h_3 = -\mu_4)
  \,.
$$

=--

In terms of def. \ref{m2braneLie3Algebra}, the second item in prop. \ref{CocyclesOn11dSuperMinkowski} reads as follows:


+-- {: .num_cor #The7CocycleOnm2brane}
###### Corollary

There is a super $L_\infty$-cocycle of the form

$$
  \mathfrak{m}2\mathfrak{brane}
  \stackrel{h_3 \wedge \mu_4 + \frac{1}{15} \mu_7}{\longrightarrow}
  b^6 \mathbb{R}
  \,.
$$

=--

But since $\mathfrak{m}2\mathfrak{brane}$ is a $b^2 \mathbb{R}$-[[principal ∞-bundle]], it is natural to ask whether $h_3 \wedge \mu_4 + \frac{1}{15} \mu_7$ is $b^2 \mathbb{R}$-[[equivariant cohomology|equivariant]] with respect to some natural $b^2\mathbb{R}$-[[∞-action]] on $b^6 \mathbb{R}$. Such a natural action is given by prop. \ref{b2RactionOnb2p2R}. To exhibit in components the equivariance of the 7-cocycle in corollary \ref{The7CocycleOnm2brane} with respect to this action we need a [[resolution]] of [[super Minkowski spacetime]]:

+-- {: .num_defn}
###### Definition

Write $\mathbb{R}_{res}^{10,1\vert \mathbf{32}}$ for the [[super L-∞ algebra]] whose [[Chevalley-Eilenberg algebra]] is obtained from that of [[super Minkowski spacetime]] by


$$
  CE\left(
   \mathbb{R}_{res}^{10,1\vert \mathbf{32}}
  \right)
  \coloneqq
  \left(
   CE\left(
     \mathbb{R}^{10,1\vert \mathbf{32}}\right)\otimes \left\langle h_3, g_4\right\rangle ,
     {{d h_3 = g_4 - \mu_4} \atop {d g_4 = 0}}
  \right)
  \,.
$$


=--

+-- {: .num_prop}
###### Proposition

The canonical morphism

$$
  \mathbb{R}_{res}^{10,1\vert \mathbf{32}}
  \stackrel{\simeq}{\longrightarrow}
  \mathbb{R}^{10,1\vert \mathbf{32}}
$$

given dually by $\psi^\alpha \mapsto \psi^\alpha$, $e^a \mapsto e^a$, is an equivalence of $L_\infty$-algebras. It factors the morphism $\mathfrak{m}2\mathfrak{brane} \longrightarrow \mathbb{R}^{10,1\vert \mathbf{32}}$ from def. \ref{m2braneLie3Algebra} through a morphism $\mathfrak{m}2\mathfrak{brane}  \longrightarrow \mathbb{R}^{10,1\vert \mathbf{32}}_{res}$ which on [[nLab:formal dual]] CE-elements is given by $h_3 \mapsto 0$, $g_4 \mapsto 0$ and by being the identity on all other generators.


=--

+-- {: .num_prop #7CocycleOnM2BraneDescends}
###### Proposition

There is a [[diagram]] of [[L-∞ algebras]] of the form

$$
  \array{
    && \vdots && && \vdots
    \\
    && \downarrow \downarrow && && \downarrow \downarrow
    \\
    &&
    \mathfrak{m}2\mathfrak{brane}
    &&
      \stackrel{h_3 \wedge \mu_4  + \frac{1}{15}\mu_7 }{\longrightarrow}
    &&
    b^6 \mathbb{R}
    \\
    &&
    \downarrow && && \downarrow
    \\
    \mathbb{R}^{10,1\vert\mathbf{32}}
    &\stackrel{\simeq}{\longleftarrow}&
    \mathbb{R}_{res}^{10,1\vert\mathbf{32}}
    &&
      \stackrel{h_3 \wedge (g_4 + \mu_4) + \frac{1}{15}\mu_7 }{\longrightarrow}
    &&
    b^6 \mathbb{R}/b^2 \mathbb{R}
    \\
    &&
    & {}_{\mathllap{}}\searrow && \swarrow
    \\
    &&
    && b^3 \mathbb{R}
  }
$$

=--

+-- {: .proof}
###### Proof

That the diagram exists and commutes at the level of the underlying graded algebras of the [[formal dual]] CE-algebras is immediate in terms of the defining generators: each generator is mapped to the generator of the same name, if present, in the codomain, or to zero otherwise, except for $g_7 \in CE(b^6 \mathbb{R})$ which is sent to $h_3 \wedge \mu_4  + \frac{1}{15}\mu_7$ and $g_7 \in CE(b^6 \mathbb{R}/b^2 \mathbb{R})$, which is sent to $h_3 \wedge (g_4 + \mu_4) + \frac{1}{15}\mu_7 $, as indicated.

It remains to check that the middle horizontal map respects the CE-differentials: by prop. \ref{CocyclesOn11dSuperMinkowski} we have

$$
  \begin{aligned}
    d(h_3 \wedge (g_4 + \mu_4) + \frac{1}{15}\mu_7)
    &=
    (g_4 - \mu_4) \wedge (g_4 + \mu_4) + \mu_4 \wedge \mu_4
    \\
    & = g_4 \wedge g_4
  \end{aligned}
$$

and by def. \ref{RationalSphereAlgebra} this says indeed that $g_7 \mapsto h_3 \wedge (g_4 + \mu_4) + \frac{1}{15}\mu_7$ respects the CE-differentials.

=--

+-- {: .num_remark}
###### Remark

The form of the equivariant cocycle in prop. \ref{7CocycleOnM2BraneDescends} is that of the [[curvature]] of the [[geometry of physics -- WZW terms|WZW term]] of the [[sigma model]] describing the [[M5-brane]] as considered in ([BLNPST 97, (6),(8)](#BLNPST97)).

=--


+-- {: .num_remark}
###### Remark

In view of remark \ref{RationalSpheres}, prop. \ref{7CocycleOnM2BraneDescends} says that the CE-elements $\mu_4$ and $\mu_7$ of prop. \ref{CocyclesOn11dSuperMinkowski} define a cocycle with values in the rational 4-sphere. In the discussions in _[[geometry of physics -- WZW terms]]_ and _[[geometry of physics -- BPS charges]]_ we see that under [[Lie integration]] and globalization in [[higher Cartan geometry]], these elements encode the [[supergravity C-field]] and its [[electric-magnetic duality|magnetic dual]]. That these fields should take values in the 4-sphere was first suggested in ([Sati 13, section 2.5](Hisham+Sati#Sati13)).

=--










##### The D-branes

(...)








#### Summary

[[!include brane scan]]


<div style="float:left;margin:0 10px 10px 0;"><img src="https://dl.dropboxusercontent.com/u/12630719/BraneBouquet.JPG" alt="the brane bouquet" /></div>








## **Semantics layer**









### The modal operators

+-- {: .num_remark #SequenceOfSites}
###### Remark

The [[sites]] in question are alternatingly (co-)[[reflective subcategories]] of each other (we always display [[left adjoints]] above their right adjoints)

$$
  \ast
  \stackrel{\longleftarrow}{\hookrightarrow}
  CartSp
  \stackrel{\hookrightarrow}{\longleftarrow}
  CartSp\rtimes InfPoint
  \stackrel{\longleftarrow}{\stackrel{\hookrightarrow}{\longleftarrow}}
  CartSp \rtimes SuperPoint
  \,.
$$


Here

* the first inclusion picks the [[terminal object]] $\mathbb{R}^0$;

* the second inclusion is that of [[reduced objects]]; the coreflection is [[reduction]], sending an algebra to its [[reduced algebra]];

* the third inclusion is that of even-graded algebras, the reflection sends a $\mathbb{Z}_2$-graded algebra to its even-graded part, the co-reflection sends a $\mathbb{Z}_2$-graded algebra to its quotient by the ideal generated by its odd part, see at _[superalgebra -- Adjoints to the inclusion of plain algebras](super+algebra#AdjointsToInclusionOfPlainAlgebra)_.

=--

+-- {: .num_remark }
###### Remark

Passing to [[(∞,1)-categories of (∞,1)-sheaves]], this yields, via [[(∞,1)-Kan extension]], a sequence of [[adjoint quadruples]] as follows:

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
    \infty Grpd
    &\hookrightarrow&
    Smooth \infty Grpd
    &\hookrightarrow&
    FormalSmooth \infty Grpd
    &\hookrightarrow&
    SuperFormalSmooth \infty Grpd
    \\
    & &\longleftarrow& &\longleftarrow&
    \\
    & &\hookrightarrow&
  }
$$

=--

+-- {: .num_prop #TheProcessOfModalities}
###### Proposition

Passing to the [[adjoint triples]] of [[idempotent monads]] and [[idempotent comonads]] which this induces, then yields

* on the left the [[shape modality]] $\int$, [[flat modality]] $\flat$ and [[sharp modality]] $\sharp$,

* in the middle yields the [[reduction modality]] $\Re$, the [[infinitesimal shape modality]] $\Im$ and the [[infinitesimal flat modality]] $\&$.

* on the right we get an adjoint triple whose whose middle bit $\rightsquigarrow$ is the [[bosonic modality]] and whose left piece $\rightrightarrows$ produces _super-even_ components, containing all the "[[fermion]] [[currents]]" if one wishes , which in this [[unity of opposites]] hence deserves to be called the _[[fermionic modality]]_. The further right adjoint $R$ is the [[rheonomy modality]].

Hence we get a process of [[adjoint modalities]] of the form

$$
  \array{
    && id &\dashv& id
    \\
    && \vee && \vee
    \\
    &\stackrel{fermionic}{}& \rightrightarrows &\dashv& \rightsquigarrow & \stackrel{bosonic}{}
    \\
    && \bot && \bot
    \\
    &\stackrel{bosonic}{} & \rightsquigarrow &\dashv& Rh & \stackrel{rheonomic}{}
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

where "$\vee$" denotes inclusion of [[modal types]]. The first level is [[cohesion]], the second is [[differential cohesion]] ([[elasticity]]), the third is a further refinement given by supergeometry, which takes further "square roots" of all infinitesimal generators.

=--

+-- {: .proof}
###### Proof

All the sites are [[∞-cohesive sites]], which gives that we have an [[cohesive (infinity,1)-topos]]. The composite inclusion on the right is an [∞-cohesive neighbourhood site](differential+cohesive+%28infinity%2C1%29-topos#PresentationOnInfinitesimalNeighbourhoodSites), whence the inclusion $Smooth\infty Gpd\hookrightarrow SuperFormalSmooth\infty Grpd$ exhibits [[differential cohesion]].

With this the rightmost adjoint quadruple gives the [[Aufhebung]] of $\Re \dashv \Im$ by $\rightsquigarrow \dashv \R$ and the further opposition $\rightrightarrows \dashv \rightsquigarrow$.


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
    &\stackrel{fermionic}{}& \rightrightarrows  &\dashv& \rightsquigarrow & \stackrel{bosonic}{}
    \\
    && \bot && \bot
    \\
    &\stackrel{bosonic}{} & \rightsquigarrow &\dashv& Rh & \stackrel{rheonomic}{}
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

  * **[[fermionic modality]] $\rightrightarrows$** -- the spaces it sends to the point are purely fermionic, the [[odd line]];

  * **[[bosonic modality]] $\rightsquigarrow$** -- sends a super-space to the underlying bosonic space;

  * **[[rheonomy modality]] $\Rh$**;

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

* The [[odd line]] $\mathbb{R}^{0|1}$ is purely [[fermionic modality|fermionic]] in that it is an $\e$-[[comodal type]]: $\stackrel{\rightrightarrows}{\mathbb{R}^{0|1}}\simeq \ast$.

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
    \mathbf{H}(\stackrel{\rightrightarrows}{U \times D_s} , \Im X)
    \\
    &\simeq
    \mathbf{H}(\Re(\stackrel{\rightrightarrows}{U \times D_s}) , X)
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





## References

The following first mentions

* [General accounts](#GeneralReading)

that might usefully be held on to during the seminar. Then I list

* [Special literature](#MoreDetails)

with refernces to original results and to reviews of these. Then I list pointers to my own work with collaborators on

* [Higher super Cartan geometry](#ReferencesHigherSuperCartan)


### General accounts
 {#GeneralReading}

An excellent general textbook for our purposes is

* {#CDF} [[nLab:Leonardo Castellani]], [[nLab:Riccardo D'Auria]], [[nLab:Pietro Fré]], _[[nLab:Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991)

This is written by physicists in physics style, but the development is careful and thorough, and the "geometric perspective" in the title is nothing but the perspective of higher [[nLab:super Cartan geometry]] in slight disguise. See also at _[[nLab:D'Auria-Fré formulation of supergravity]]_.

Lecture notes closely related to the seminar are in

* {#StructureTheory} [[nLab:Urs Schreiber]], _[[Structure Theory for Higher WZW Terms]]_, lectures at _[Higher Structures in String Theory and Quantum Field Theory](http://www.esi.ac.at/activities/events/2015/higher-structures-in-string-theory-and-quantum-field-theory)_, ESI Vienna, November 30-December 4, 2015

### More specialized literature
 {#MoreDetails}

[[nLab:Deligne's theorem on tensor categories]] is due to

* {#Deligne02} [[nLab:Pierre Deligne]], _Cat&#233;gorie Tensorielle_, Moscow Math. Journal 2 (2002) no. 2, 227-248. ([pdf](https://www.math.ias.edu/files/deligne/Tensorielles.pdf))

building on his general work on [[nLab:Tannakian categories]]

* [[nLab:Pierre Deligne]], _[[nLab:Catégories Tannakiennes]]_, Grothendieck Festschrift, vol. II, Birkh&#228;user Progress in Math. 87 (1990) pp.111-195. ([pdf](https://publications.ias.edu/sites/default/files/60_categoriestanna.pdf))

A brief survey is in

* {#Ostrik04} [[nLab:Victor Ostrik]], _Tensor categories (after P. Deligne)_ ([arXiv:math/0401347](http://arxiv.org/abs/math/0401347))

and a more comprehensive texbook account is in chapter 9.11 of

* {#EGNO15} [[nLab:Pavel Etingof]], Shlomo Gelaki, Dmitri Nikshych, [[nLab:Victor Ostrik]], _Tensor categories_, Mathematical Surveys and Monographs, Volume 205, American Mathematical Society, 2015 ([pdf](http://www-math.mit.edu/~etingof/egnobookfinal.pdf
))



The observation that [[nLab:supergeometry]] is naturally regarded as ordinary geometry inside the [[nLab:sheaf topos]] over [[nLab:superpoints]] is due to

* {#Schwarz84} [[nLab:Albert Schwarz]], _On the definition of superspace_, Teoret. Mat. Fiz. (1984)  Volume 60,  Number 1, Pages 37&#8211;42, ([russian original pdf](http://www.mathnet.ru/links/b12306f831b8c37d32d5ba8511d60c93/tmf5111.pdf))

* {#KonechnySchwarz97} Anatoly Konechny, [[nLab:Albert Schwarz]],  _On $(k \oplus l|q)$-dimensional supermanifolds_ in _Supersymmetry and Quantum Field Theory_ (D. Volkov memorial volume) Springer-Verlag, 1998, Lecture Notes in Physics, 509 , J. Wess and V. Akulov (editors)([arXiv:hep-th/9706003](http://arxiv.org/abs/hep-th/9706003))

  _Theory of $(k \oplus l|q)$-dimensional supermanifolds_ Sel. math., New ser. 6 (2000) 471 - 486

A nice account is in

* {#Sachse08} [[nLab:Christoph Sachse]], _A Categorical Formulation of Superalgebra and Supergeometry_ ([arXiv:0802.4067](http://arxiv.org/abs/0802.4067))

Useful discussion of [[nLab:Majorana spinors]] and the induced [[nLab:supersymmetry]] algebras includes

* [CDF, II.7.3](#II.7.3)

* {#FigueroaOFarrill} [[nLab:José Figueroa-O'Farrill]], _Majorana spinors_ ([pdf](http://www.maths.ed.ac.uk/~jmf/Teaching/Lectures/Majorana.pdf))

The close relation between [[nLab:supersymmetry and division algebras]] was first observed in

* {#KugoTownsend83} Taichiro Kugo, [[nLab:Paul Townsend]], _Supersymmetry and the division algebras_, Nuclear Physics B, Volume 221, Issue 2 (1983) p. 357-380. ([spires](http://inspirehep.net/record/181889), [pdf](http://cds.cern.ch/record/140183/files/198301032.pdf))

A clean survey is in

* {#BH09} [[nLab:John Baez]], [[nLab:John Huerta]], _Division algebras and supersymmetry I_, in  R. Doran, G. Friedman, [[nLab:Jonathan Rosenberg]](eds.) _Superstrings, Geometry, Topology, and $C^\ast$-algebras_,  Proc. Symp. Pure Math. 81, AMS, Providence, 2010, pp. 65-80 ([arXiv:0909.0551](http://arxiv.org/abs/0909.0551))

and the discussion of the spinor bilinear pairings from this perspective is in

* {#BH10} [[nLab:John Baez]], [[nLab:John Huerta]], _Division algebras and supersymmetry II_, Adv. Math. Theor. Phys. 15 (2011), 1373-1410 ([arXiv:1003.34360](http://arxiv.org/abs/1003.3436))

The seminal analysis of [[nLab:torsion of G-structures]] is due to

* {#Guillemin65} [[nLab:Victor Guillemin]], _The integrability problem for $G$-structures_, Trans. Amer. Math. Soc. 116 (1965), 544&#8211;560. ([JSTOR](http://www.jstor.org/stable/1994134))

Discussion of [[nLab:torsion of G-structures]] in the context of [[nLab:supergeometry]] ([[nLab:supertorsion]]) is in

* {#Lott01} [[nLab:John Lott]], _The Geometry of Supergravity Torsion Constraints_ Comm. Math. Phys. 133 (1990), 563&#8211;615, (exposition in [arXiv:0108125](http://arxiv.org/abs/math/0108125))

An elegant construction of [[nLab:11-dimensional supergravity]], right in the spirit of [[nLab:super Cartan geometry]], is due to

* {#DAuriaFre82}  [[nLab:Riccardo D'Auria]], [[nLab:Pietro Fré]]; _Geometric Superravity in D=11 and its hidden supergroup_, Nuclear Physics B201 (1982) 101-140 ([pdf](https://ncatlab.org/nlab/files/GeometricSupergravity.pdf))

This is the main original result on which the [[nLab:D'Auria-Fré formulation of supergravity]] is based, as laid out in [CDF](#CDF).

The observation that the [[nLab:equations of motion]] of bosonic solutions of [[nLab:11-dimensional supergravity]] are equivalent simply to vanishing of the [[nLab:supertorsion]] is due to

*  {#CandielloLechner93} A. Candiello, K. Lechner, _Duality in Supergravity Theories_, Nucl.Phys. B412 (1994) 479-501 ([arXiv:hep-th/9309143](http://arxiv.org/abs/hep-th/9309143))

* {#Howe97} [[nLab:Paul Howe]], _Weyl Superspace_, Physics Letters B
Volume 415, Issue 2, 11 December 1997, Pages 149&#8211;155 ([arXiv:hep-th/9707184](http://arxiv.org/abs/hep-th/9707184))

Discussion of [[nLab:Fierz identities]] includes

* [CDF, II.8](#CDF)

The classification of the invariant super Lie algebra cocycles on super-Minkowski spacetime, hence that of [[nLab:super p-branes]] without gauge fields on their worldvolume, is due to

* {#AETW87} Anna Ach&#250;carro, [[nLab:Jonathan Evans]], [[nLab:Paul Townsend]], [[nLab:David Wiltshire]], _Super $p$-Branes_, Phys. Lett. B **198** (1987) 441 ([spire](http://inspirehep.net/record/22286?ln=en))

The extension of this classification to [[nLab:D-branes]] and to the [[nLab:M5-brane]] using [[nLab:extended super Minkowski spacetime]] is due to

* {#CAIB99} C. Chrysso&#8204;malakos, [[nLab:José de Azcárraga]], J. M. Izquierdo and C. P&#233;rez Bueno, _The geometry of branes and extended superspaces_, Nuclear Physics B Volume 567, Issues 1&#8211;2, 14 February 2000, Pages 293&#8211;330 ([arXiv:hep-th/9904137](http://arxiv.org/abs/hep-th/9904137))

* {#Sakaguchi00} Makoto Sakaguchi, _IIB-Branes and New Spacetime Superalgebras_, JHEP 0004 (2000) 019 ([arXiv:hep-th/9909143](https://arxiv.org/abs/hep-th/9909143))

The M5-brane cocycle on the "M2-brane extended super-Minkowski spacetime" that appears here has in fact been observed, as a cocycle, all the way back in [D'Auria-Fr&#233; 82](#DAuriaFre82). But there it was seen just as a means for constructing [[nlab:11-dimensional supergravity]]. That it indeed gives the [[nLab:higher WZW term]] in the [[nLab:Green-Schwarz action functional|Green-Schwarz type action functional]] that defines the fundamental [[nLab:M5-brane]] has been argued in

* {#BLNPST97} [[nLab:Igor Bandos]], [[nLab:Kurt Lechner]], Alexei Nurmagambetov, [[nLab:Paolo Pasti]], [[nLab:Dmitri Sorokin]], Mario Tonin, _Covariant Action for the Super-Five-Brane of M-Theory_, Phys.Rev.Lett. 78 (1997) 4332-4334 ([arXiv:hep-th/9701149](http://arxiv.org/abs/hep-th/9701149))

The observation that [[nLab:super p-branes]] on curved [[nLab:super spacetimes]] require [[nLab:definite globalization of WZW term|definite globalization]] of super Lie algebra cocycles from Minkowski spacetime over the supermanifold is due to

* {#BergshoeffSezginTownsend86} [[nLab:Eric Bergshoeff]], [[nLab:Ergin Sezgin]], [[nLab:Paul Townsend]], _Superstring actions in $D = 3, 4, 6, 10$ curved superspace_, Phys.Lett., B169, 191, (1986) ([spire](http://inspirehep.net/record/223138/?ln=en))

* {#BergshoeffSezginTownsend87}  [[nLab:Eric Bergshoeff]], [[nLab:Ergin Sezgin]], [[nLab:Paul Townsend]], _Supermembranes and eleven dimensional supergravity_, Phys.Lett. B189 (1987) 75-78, In [[nLab:Mike Duff]],  (ed.), _[[nLab:The World in Eleven Dimensions]]_ 69-72 ([pdf](http://streaming.ictp.trieste.it/preprints/P/87/010.pdf), [spire](http://inspirehep.net/record/248230?ln=en))

The formulation of [[nLab:topological T-duality]] is due to

* {#BouwknegtEvslinMathai04} [[nLab:Peter Bouwknegt]], [[nLab:Jarah Evslin]], [[nLab:Varghese Mathai]], _T-Duality: Topology Change from H-flux_, Commun.Math.Phys.249:383-415,2004 ([hep-th/0306062](http://arxiv.org/abs/hep-th/0306062))

and in an alternative form due to

* {#BunkeRumpfSchick08} {#BunkeRumpfSchick08} [[nLab:Ulrich Bunke]], P. Rumpf, [[nLab:Thomas Schick]], _The topology of $T$-duality for $T^n$-bundles_,  Rev. Math. Phys. 18, 1103 (2006). ([arXiv:math.GT/0501487](http://arxiv.org/abs/math.GT/0501487))



The suggestion that there ought to be "[[nLab:T-folds]]" or "[[nLab:double field theory|doubled geometry]]" is due to

* {#Hull04} [[nLab:Chris Hull]], _A Geometry for Non-Geometric String Backgrounds_, JHEP0510:065,2005 ([arXiv:hep-th/0406102](http://arxiv.org/abs/hep-th/0406102))

* {#Hull06} [[nLab:Chris Hull]], _Doubled geometry and T-folds_ JHEP0707:080,2007  ([arXiv:hep-th/0605149](http://arxiv.org/abs/hep-th/0605149))

The mathematical formalization of this idea in terms of [[nLab:principal 2-bundles]] for the [[nLab:T-duality 2-group]] was claimed in

* {#Nikolaus14} [[nLab:Thomas Nikolaus]], _T-Duality in K-theory and elliptic cohomology_, talk at _String Geometry Network Meeting_, Feb 2014, ESI Vienna ([website](http://www.ingvet.kau.se/juerfuch/conf/esi14/esi14_34.html))


### Higher super Cartan geometry
 {#ReferencesHigherSuperCartan}

The following articles develop the higher super Cartan geometry that we give an exposition of in the second part of the seminar.

The mathematical foundation of higher supergeometry:

* {#dcct} [[nLab:Urs Schreiber]], _[[differential cohomology in a cohesive topos]]_, Thesis, ([v1 arXiv:1310.7930](http://arxiv.org/abs/1310.7930v1), [v2](https://dl.dropboxusercontent.com/u/12630719/dcct.pdf))

The general idea of [[The brane bouquet]] and the general construction of [[nLab:higher WZW terms]] from higher $L_\infty$-cocycles:

* {#FSS13} [[nLab:Domenico Fiorenza]], [[nLab:Hisham Sati]], [[nLab:Urs Schreiber]],   _[[The brane bouquet|Super Lie n-algebra extensions, higher WZW models and super p-branes with tensor multiplet fields]]_ International Journal of Geometric Methods in Modern Physics Volume 12, Issue 02 (2015) 1550018, ([arXiv:1308.5264](http://arxiv.org/abs/1308.5264))

The homotopy-[[nLab:descent]] of the [[nLab:M5-brane]] cocycle and of the type IIA [[nLab:D-brane]] cocycles:

* {#FSS16} [[nLab:Domenico Fiorenza]], [[nLab:Hisham Sati]], [[nLab:Urs Schreiber]], _[[Rational sphere valued supercocycles in M-theory]]_, to appear in Journal of Geometry and Physics ([arXiv:1606.03206](http://arxiv.org/abs/1606.03206))

The derivation of supersymmetric [[nLab:topological T-duality]], rationally, and of the higher super Cartan geometry for [[nLab:super T-folds]]:

* {#FSS16a} [[nLab:Domenico Fiorenza]], [[nLab:Hisham Sati]], [[nLab:Urs Schreiber]], _[[T-Duality from super Lie n-algebra cocycles for super p-branes]]_ ([arXiv:1611.06536](https://arxiv.org/abs/1611.06536))

The derivation of the process of higher invariant extensions that leads from the [[nLab:superpoint]] to [[nLab:11-dimensional supergravity]]:

* {#MTheoryFromTheSuperpoint} [[nLab:John Huerta]], [[nLab:Urs Schreiber]], _[[M-Theory from the Superpoint]]_


