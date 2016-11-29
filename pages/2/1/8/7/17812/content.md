

> this entry is one section of "[[geometry of physics -- supergeometry and superphysics]]"
> which is one chapter of "[[geometry of physics]]"

> previous section: _[[geometry of physics -- superalgebra]]_

> next section _[[geometry of physics -- supersymmetry]]_

> under construction

$\,$


Supergeometry is the generalization of [[differential geometry]] (or [[algebraic geometry]]) to the situation where [[algebras of functions]]
are generalized from [[commutative algebras]] to [[supercommutative superalgebras]].

In _[[geometry of physics -- superalgebra]]_ we discussed why it is mathematically compelling to pass
to [[supercommutative superalgebra]] and how this implies a dual concept of [[superspace]] in terms of [[affine superschemes]].
Here we discuss how to build a fully-fledged theory of [[geometry]] on these affine [[superspaces]] -- [[supergeometry]] --
in parallel to the discussion of ordinary [[differential geometry]] in _[[geometry of physics -- smooth sets]]_.

Apart from the abstract mathematical motivation for supergeometry, it is also an observational fact that the physical world is
fundamentally described by
[[supergeometry]]. Namely the [[Pauli exclusion principle]] implies that the [[phase space]] of a [[field theory]]
(already of a [[classical field theory]]) with [[fermion]] [[field (physics)|fields]] (such as that of [[electrons]] and [[quarks]])
is a [[superspace]] whose even-graded [[coordinates]] are the configurations of the [[boson]] fields, while the
odd-graded coordinates correspond to the configurations of the [[fermion]] fields. It is impossible to have an
[[action functional]] for fermion fields as a function on a non-super ([[infinite-dimensional manifold|infinite-dimensional]])-[[manifold]].

 The experimental detection of the special properties of [[fermions]] that show their super-geometric nature
 goes back all the way to the [[Stern-Gerlach experiment]] in 1922;
 an early theoretical formulation is the [[Pauli exclusion principle]] from 1925. A little later it was realized that
 the [[axioms]] of [[local field theory]] _imply_ that [[fermions]] need to be described by [[superalgebra]].
 This is the celebrated _[[spin-statistics theorem]]_, whose formulation goes back to
 ([Fierz 1939](spin-statistics+theorem#Fierz39) and [Pauli 1940](#spin-statistics+theorem#Pauli40)).

 Notice that this phenomenon is not a negligible subtlety: the [[Pauli exclusion principle]]
 is what implies [[stability of matter]] by forcing [[electrons]] in an [[atom]] to fill up
 "orbitals" consecutively as opposed to all falling into the ground state, as a bosonic [[condensate]] would do.
 There would be no [[solid state physics]] without supergeometry of [[phase spaces]], no [[matter]] as we know it.
 (In addition, the Pauli [[degeneracy pressure]] controls more exotic phenomena, for instance the
  stability of neutron stars against their gravitational collapse.)

As a slogan:

$\,\,\,\,\,\;$ _**The [[geometry]] of [[phase spaces]] of [[fermions]]/[[matter]] is [[supergeometry]].**_

Nevertheless, few textbooks make the supergeometric aspect in the physics of fermions explicit.
Some discuss it only after [[quantization]] (and some will even claim that femion fields do not exist classically);
some only discuss it in the context of [[spacetime]] [[supersymmetry]]. But notice that
_[[supergeometry]]_ is a subject in itself even without presence or mentioning of spacetime [[supersymmetry]]
(which is [[super Poincaré group]] [[symmetry]]), just as
[[differential geometry]] is a subject in itself even without the presence or mentioning of
[[Poincaré group]] symmetry.

Texts which do make the super-geometric nature of [[fermion fields]] explicit include
([Deligne-Freed 99, &#167;3.4](#DeligneFreed99), [Freed 01, lecture 4](#Freed01), [Giachetta-Mangiarotti-Sardanashvily 09, chapter 3](#GiachettaMangiarottiSardanashvily09) [Sardanashvily 12](#Sardanashvily12), [Sardanashvily 16](#Sardanashvily16)).


#Supergeometry#
* table of contents
{:toc}




In the section _[[geometry of physics -- superalgebra]]_ we discussed the [[category]] of **affine [[super schemes]]**

$$
  Var(sVect_{\mathbb{R}}) \coloneqq sCalg_k^{op} = CMon(sVect_{\mathbb{R}})
$$

[this def.](geometry+of+physics+--+superalgebra#AffineSuperSchemes).

Here we use these as local model spaces to develop [[geometry]] locally modeled on affine superschemes.
Since we are ineterested in [[physics]], and since [[spacetimes]] and [[phase spaces]] in physics
are objects in [[differential geometry]], not in [[algebraic geometry]] (even if sometimes they may come from there),
we consider the [[full subcategory]] of **[[super Cartesian spaces]]** ([this example](geometry+of+physics+--+superalgebra#SuperCartesianSpace))

$$
  SuperCartSp = \{\mathbb{R}^{p\vert q}\}_{p,q \in \mathbb{N}} \hookrightarrow Aff(sVect_k)
  \,,
$$

whose [[algebras of functions]] by definition are [[tensor products]] (over the [[real numbers]] $\mathbb{R}$)
of $\mathbb{R}$-[[associative algebras|algebras]] of [[smooth functions]] with [[Grassmann algebras]]

$$
  \mathcal{O}(\mathbb{R}^{p\vert q})
    \;\coloneqq\;
  C^\infty(\mathbb{R}^q) \otimes_{\mathbb{R}} \wedge^\bullet (\mathbb{R}^\ast)^q
  \,.
$$

These serve as our "abstract super-coordinate systems" that define [[supergeometry]] in direct analogy to how ordinary [[Cartesian spaces]] serve as the abstract coordinate systems that define [[differential geometry]] as discussed at _[[geometry of physics -- smooth sets]]_. 
We now discuss this in detail.


## Coordinate systems: Super Cartesian spaces
 {#CoordinareSystemsSuperCartesianSpaces}


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



We write

$$
  CartSp \hookrightarrow SuperCartSp
$$

for the [[full subcategory]] on ordnary [[Cartesian spaces]] with [[smooth functions]] between them.
These are the "abstract coordinate charts" from the discussion at _[[geometry of physics -- smooth sets]]_,
and so we are evidently entitled to think of the objects in $SuperCartSp$ as **abstract super coordinate systems**
and to develop a geometry induced from these.

Recall the two magic algebraic properties of [[smooth functions]] that make the above algebraic description of 
[[differential geometry]] work:

1. **[[embedding of smooth manifolds into formal duals of R-algebras]]** The functor that assigns [[algebra of functions|algebras of]] [[smooth function]] of [[smooth manifolds]]

   $$
     C^\infty(-) \;\colon\; SmthMfd \hookrightarrow CAlg_{\mathbb{R}}^{op}
   $$
   
   is [[fully faithful functor|fully faithful]].
   
1. **[[smooth Serre-Swan theorem]]** The functor that assigns smooth [[sections]] of smooth [[vector bundles]] 
   of [[finite number|finite]] [[rank]]

   $$
     \Gamma_X(-) \;\colon\; SmthVectBund_{/X} \hookrightarrow C^\infty(X) Mod
   $$
   
   is [[fully faihful functor|fully faithful]] (its [[essential image]] being the [[finitely generated object|finitely generated]] [[projective modules]] over the $\mathbb{R}$-[[algebra of functions|algebra of]] [[smooth function]]).

There is a third such magic algebraic property of smooth functions, which plays a role now:

+-- {: .num_defn #}
###### Proposition
**([[derivations of smooth functions are vector fields]])**

Let $X$ be a [[smooth manifold]]. Write

$$
  der_X \;\colon\; \Gamma(T X) \longrightarrow Der(C^\infty(X))
$$

for the function that sends a smooth [[vector field]] $v \in \Gamma(T X)$ to the [[derivation]]
of the [[algebra of functions|algebra of]] [[smooth functions]] on $X$ given by forming 
[[derivatives]] $der_X(v)(f) \coloneqq v(f)$ (which is a derivation by the [[chain rule]]).

Then this function is a [[bijection]], hence every [[derivation]] of $C^\infty(X) \in CAlg_{\mathbb{R}}$
comes from [[differentiation]] along some smooth vector field, and uniquely so.

=--

Recall further from _[[geometry of physics -- superalgebra]]_ that the category of [[supercommutative superalgebras]]
is related to that of ordinary [[commutative algebras]] over $\mathbb{R}$ by an 
[[adjoint cylinder]] ([this prop](geometry+of+physics+--+superalgebra#InclusionOfCAlgIntosCAlg))

$$
  CAlg_k
    \underoverset
      {\underset{(-)_{even}}{\longleftarrow}}
      {\overset{(-)/(-)_{odd}}{\longleftarrow}}
      {\hookrightarrow}
  sCAlg_k
  \,.
$$

The [[formal dual]] of this statement is that [[affine superschemes]] are related to ordinary [[affine schemes]]
over $\mathbb{R}$ by an [[adjoint cylinder]] of this form

$$
  Aff(Vect_k)
    \underoverset
      {\underset{\rightrightarrows}{\longleftarrow}}
      {\overset{\rightsquigarrow}{\longleftarrow}}
      {\hookrightarrow}
  Aff(sVect_k)
  \,.
$$

Here the notation is to serve as a convenient mnemonic for the nature of these functors:

in a [[Feynman diagram]] 

1. a single [[fermion]] is denoted by a solid arrow "$\to$" and the functor
$\rightrightarrows$ produces a space whose [[algebra of functions]] is generated over
smooth functions by the product of two fermionic functions 

1. a single [[boson]] is denoted by a wiggly arrow $\rightsquigarrow$ and the functor
   denoted by this symbol produces a spaces whose [[algebra of functions]] contains only the
   bosonic smooth functions, no odd-graded functions.


This highlight an important point: while the image of a [[super Cartesian space]] under $\rightsquiqarrow$
is an ordinary [[Cartesian space]]

$$
   \overset{\rightsquiqarrow}(\mathbb{R}^{p\vert q})
   \simeq 
   \mathbb{R}^p
$$

its image under $\rightrightarrows$ is a bosonic space, but not an ordinary manifold. For instance

$$
  \begin{aligned}
   \mathcal{O}\left( \overset{\rightrightarrow}{\mathbb{R}^{0\vert 2}}\right)
    & = 
   \mathcal{O}(\mathbb{R}^{0\vert 2})_{even}
   \\
  & = 
  (\wedge^\bullet(\mathbb{R}^2)^\ast)_{even}
  \\
  &=
  \left\{a_0 + a_1 \, \theta_1 + a_2 \, \theta_2 + a_{12} \theta_1 \theta_2 \,\vert a_\bullet \in \mathbb{R}\,\right\}_{even}
  \\
  &=
  \left\{a_0  + a_{12} \theta_1 \theta_2 \,\vert a_{12} \in \mathbb{R}\,\right\}
  \\
  &=
  \mathbb{R}[\epsilon]/(\epsilon^2 = 0)
  \end{aligned}
$$

where in the last line we renamed $\theta_1 \theta_2$ to $\epsilon$.

This algebra is known as the **[[algebra of dual numbers]]** over $\mathbb{R}$. It is the [[algebra of functions]]
on a bosonic but [[infinitesimally thickened point]], a 1-dimensional neighbourhood of a point which is "so very small"
that the canonical [[coordinate]] function $\epsilon$ on it takes values "so tiny" that its square, which is bound to be
even tinier, is actually indistinguishable from zero.

In generalization of this we say

+-- {: .num_defn #FormalCartSp}
###### Definition

Write

$$
  InfPoint \hookrightarrow CAlg_{\mathbb{R}}^{op}
$$

for the [[full subcategory]] of the [[opposite category]] of [[commutative algebras]] over $\mathbb{R}$ on [[formal duals]] of [[commutative algebras]] over the [[real numbers]] of the form $\mathbb{R}\oplus V$ with $V$ a [[nilpotent ideal]] of [[finite number|finite]]-[[dimension]] 
over $\mathbb{R}$. We call this the category of _[[infinitesimally thickened points]]_.

In [[synthetic differential geometry]] these algebras ar called _[[Weil algebra]]_, while in [[algebraic geometry]] they are known as local [[Artin algebras]] over $\mathbb{R}$.

Write moreover

$$
  FormalCartSp \coloneqq CartSp \rtimes InfPoint \hookrightarrow CAlg_{\mathbb{R}}^{op}
$$

for the [[full subcategory]] on [[formal duals]] of those algebras which are [[tensor products]] of commutative $\mathbb{R}$-algebras of the form

$$
  C^\infty(\mathbb{R}^n) \otimes C^\infty(D)
$$

of algebras $C^\infty(\mathbb{R}^p)$ of [[smooth functions]] $\mathbb{R}^n$ as in def. \ref{EmbeddingOfSmoothManifoldsIntoFormalDualsOfRAlgebras} with algebras corresponding to infinitesimally thickened points $D$ as above.



=--

This kind of construction is traditionally more familiar from the theory of [[formal schemes]], but the same kind of general abstract theory goes through in the context of [[differential geometry]], a point of view known as _[[synthetic differential geometry]]_.

But this means that in passing to commutative superalgebras there are _two_ stages of generalizations of plain differential geometry involved:

1. [[smooth manifolds]] are generalized to [[formal smooth manifolds]];

1. [[formal smooth manifolds]] are further generalized to formal smooth [[supermanifolds]].





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



## Super formal smooth sets

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


+-- {: .num_defn}
###### Definition

Say that a collection of morphisms $\{U_i \to X\}$ in $SuperCartSp$ is [[covering]] if all $U_i$ and the $X$ are $\mathbb{R}^{p|q}$ (for the same $p$ and $q$), the morphisms are the identity on the odd generators $\{\theta_i\}$, and the underlying map of [[Cartesian spaces]] is a [[good open cover]] in the sense of def. \ref{SiteCartSp}. Write

$$
  SuperSmooth0Type \coloneqq Sh(SuperCartSp)
$$

for the [[sheaf topos]] over that site. We call this the collection of _[[smooth super spaces]]_.

=--

This is the [[topos]] that hosts traditional [[supergeometry]]. However for our purposes it is useful to refine this a little more to a context for [[synthetic differential supergeometry]]. To that end first observe that


+-- {: .num_defn}
###### Definition

The [[sheaf topos]]

$$
  FormalSmooth0Type \coloneqq Sh(CartSp \rtimes InfPoint)
$$

is traditionally known as the _[[Cahiers topos]]_.

=--


## Super differential forms
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

This is an issue to be dealt with when describing [[supergravity]] in terms of Cartan fields on [[supermanifolds]] $X$, because the actual [[spacetime]] manifold one cares about is just the [[bosonic modality|bosonic part]] $\stackrel{\rightsquigarrow}{X}$. This issue is dealt with by the concept of [rheonomy](D'Auria-Fre+formulation+of+supergravity#Rheonomy).


=--

## References

* {#DeligneFreed99} [[Pierre Deligne]], [[Daniel Freed]], _Classical field theory_ (1999) ([pdf](https://publications.ias.edu/sites/default/files/79_ClassicalFieldTheory.pdf))

  this is a chapter in

  [[Pierre Deligne|P. Deligne]], [[Pavel Etingof|P. Etingof]], [[Dan Freed|D.S. Freed]], L. Jeffrey, [[David Kazhdan|D. Kazhdan]], J. Morgan, D.R. Morrison, [[Edward Witten|E. Witten]] (eds.)  _[[Quantum Fields and Strings]], A course for mathematicians_, 2 vols. Amer. Math. Soc. Providence 1999. ([web version](http://www.math.ias.edu/qft))


* {#Freed01} [[Daniel Freed]], bottom of p. 48 in _Classical field theory and Supersymmetry_ , IAS/Park City Mathematics Series Volume 11, 2001 ([pdf](https://www.ma.utexas.edu/users/dafr/pcmi.pdf))

* {#GiachettaMangiarottiSardanashvily09} Giovanni Giachetta, Luigi Mangiarotti, [[Gennadi Sardanashvily]], chapter 3 of _Advanced classical field theory_, World Scientific (2009)


* {#Sardanashvily12} [[Gennadi Sardanashvily]], _Grassmann-graded Lagrangian theory of even and odd variables_ ([arXiv:1206.2508](https://arxiv.org/abs/1206.2508))



* {#Sardanashvily16} [[Gennadi Sardanashvily]], _Noether's Theorems: Applications in Mechanics and Field Theory_, Studies in Variational Geometry, 2016

