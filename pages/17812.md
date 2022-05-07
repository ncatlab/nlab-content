

> this entry is one section of "[[geometry of physics -- supergeometry and superphysics]]"

> which is one chapter of "[[geometry of physics]]"

> previous sections: _[[geometry of physics -- superalgebra|superalgebra]]_, _[[geometry of physics -- categories and toposes|categories and toposes]]_, _[[geometry of physics -- smooth sets|smooth sets]]_

> following sections: _[[geometry of physics -- supersymmetry]]_, _[[geometry of physics -- smooth homotopy types]]_

$\,$


[[supergeometry|Supergeometry]] is the generalization of [[differential geometry]] (or [[algebraic geometry]]) to the situation where [[algebras of functions]] are generalized from [[commutative algebras]] to [[supercommutative superalgebras]].

In _[[geometry of physics -- superalgebra]]_ we discussed why it is mathematically compelling to pass to [[supercommutative superalgebra]] and how this implies a dual concept of [[superspace]] in terms of [[affine superschemes]]. Here we discuss how to build a fully-fledged theory of [[geometry]] on these affine [[superspaces]] -- [[supergeometry]] --
in parallel to the discussion of ordinary [[differential geometry]] in _[[geometry of physics -- smooth sets]]_.

<div style="float:right;margin:0 20px 10px 20px;">
<a href="#ProgressionOfIdempotentEndofunctors">
<img src="http://ncatlab.org/schreiber/files/ProgressionOfModalities.jpg" width="200">
</a>
</div>


Apart from the abstract mathematical motivation for supergeometry, it is also an [[experimental observation|experimental]] fact that the
[[observable universe]] is fundamentally described by
[[supergeometry]]. Namely the [[Pauli exclusion principle]], in its refined form of the
[[spin-statistics theorem]], implies that the [[phase space]] of a [[field theory]]
(already of a [[classical field theory]]) with [[fermion]] [[field (physics)|fields]] (such as that of [[electrons]] and [[quarks]])
is a [[superspace]] whose even-graded [[coordinates]] are the configurations of the [[boson]] fields, while the
odd-graded coordinates correspond to the configurations of the [[fermion]] fields. It is impossible to have an
[[action functional]] for fermion fields as a function on a non-super ([[infinite-dimensional manifold|infinite-dimensional]])-[[manifold]].

 This is an old insight:
 The experimental detection of the special properties of [[fermions]] that show their super-geometric nature
 goes back all the way to the [[Stern-Gerlach experiment]] in 1922, which revealed that [[electrons]] are [[spinors]].
 The [[Pauli exclusion principle]] ([Pauli 1925](#Pauli25)) -- [[deduction|deduced]] from the nature of energy levels of [[electrons]]
 in [[atoms]] --  says that no two such [[spinors]]
 may occupy the exact same [[quantum state]]. Technically this says that the spinor [[field (physics)|field]] variable $\psi$ has
 to satisfy
 $$
   \psi \psi = 0
   \,.
 $$
 A little later it was realized that
 the [[axioms]] of [[local field theory]] _imply_ that all [[spinor]] fields need to be [[fermions]]
 in that for any two [[classical field theory|classical]] spinor field variables $\psi_1$, $\psi_2$ the Grassmann sign rule
 holds ([Grassmann 1844](geometry+of+physics+--+-superalgebra#Grassmann1844)):
 $$
   \psi_1 \psi_2 = - \psi_2 \psi_1
 $$
 (which of course immediately implies the [[Pauli exclusion principle]]).
 This is the celebrated _[[spin-statistics theorem]]_, whose formulation goes back to
 [Fierz in 1939](#Fierz39) and [Pauli in 1940](#Pauli40). And that sign rule is of course precisely the sign rule in a [[supercommutative superalgebra]], for the fermion field observables $\psi_i$ being odd-graded functions on a supergeometric [[phase space]].

 Notice that this phenomenon is not a negligible subtlety: the [[Pauli exclusion principle]]
 is what implies [[stability of matter]] by forcing [[electrons]] in an [[atom]] to fill up
 "orbitals" consecutively as opposed to all falling into the ground state, as a bosonic [[condensate]] would do.
 There would be no [[solid state physics]] without supergeometry of [[phase spaces]], no [[solidity|solid]] [[matter]].
 (In addition, the Pauli [[degeneracy pressure]] controls more exotic phenomena, for instance the
  stability of neutron stars against their gravitational collapse.)

As a slogan:

$\,\,\,\,\,\;$ _**The [[geometry]] of [[phase spaces]] for [[fermions]],**_

$\,\,\,\,\,\;$ _**hence for [[matter]] fields admitting [[solid state physics|solid states]],**_

$\,\,\,\,\,\;$ _**is [[supergeometry]].**_

Nevertheless, few textbooks make the supergeometric aspect in the physics of fermions explicit.
Some discuss it only after [[quantization]] (and some will even claim that fermion fields do not exist classically);
some only discuss it in the context of [[spacetime]] [[supersymmetry]]. But notice that
_[[supergeometry]]_ is a subject in itself even without presence or mentioning of spacetime [[supersymmetry]]
(which is [[super Poincaré group]] [[symmetry]]), just as
[[differential geometry]] is a subject in itself even without the presence or mentioning of
[[Poincaré group]] symmetry. Hence this we discuss independently in _[[geometry of physics -- supersymmetry]]_.

Texts which do make the super-geometric nature of [[fermion fields]] explicit include

* [Deligne-Freed 99, &#167;3.4](#DeligneFreed99), [Freed 01, lecture 4](#Freed01),

* [Giachetta-Mangiarotti-Sardanashvily 09, chapter 3](#GiachettaMangiarottiSardanashvily09),

* [Sardanashvily 12](#Sardanashvily12), [Sardanashvily 16](#Sardanashvily16).

This we discuss elsewhere.

$\,$

$\,$

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--


#Supergeometry#
* table of contents
{:toc}


$\,$

$\,$

In the section _[[geometry of physics -- superalgebra]]_ we had discussed the [[category]] of **[[affine super schemes]]**
(in [this definition](geometry+of+physics+--+superalgebra#AffineSuperSchemes))

$$
  Var(sVect_{\mathbb{R}}) \coloneqq sCalg_k^{op} = CMon(sVect_{\mathbb{R}})
  \,.
$$


Here we use these as local model spaces to develop [[geometry]] locally modeled on affine superschemes.
Since we are interested in [[physics]], and since [[spacetimes]] and [[phase spaces]] in physics
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
  C^\infty(\mathbb{R}^p) \otimes_{\mathbb{R}} \wedge^\bullet (\mathbb{R}^\ast)^q
  \,.
$$

These serve as our "abstract super-coordinate systems" that define [[supergeometry]] in direct analogy to how ordinary [[Cartesian spaces]] serve as the abstract coordinate systems that define [[differential geometry]] as found at
_[[geometry of physics -- coordinate systems]]_  and_[[geometry of physics -- smooth sets]]_.

Then a general superspace is modeled as a [[sheaf]] on the category of super Cartesian spaces,
possibly satisfying some suitable properties. see remark \ref{ASheafAsASpace} below for explanation of this perspective.


This means that we follow the perspective of "**[[functorial geometry]]**" due to [Grothendieck 65](#Grothendieck65),
where a [[scheme]] is regarded as a [[sheaf]] over the category of [[affine schemes]] (its "[[functor of points]]")
satisfying the condition that it is covered by ([[representable functor|representables]] of) affines via [[formally étale morphism]].
We explain all this below.

Beware that -- despite the urging in [Grothendieck 73](#Grothendieck73) that the definition of [[schemes]] as
[[locally ringed spaces]] should be abandoned in favour of the perspective of [[functorial geometry]] -- most textbooks on [[supergeometry]]
do stick with the point of view of [[locally ringed spaces]].
(One might argue that in smooth supergeometry this is a particularly heavy violation of [Grothendieck's urging](#Grothendieck73),
since, in contrast to algebraic schemes, every supermanifold is already affine.)

An exception is the approach propagated in [Schwarz 84](#Schwarz84), [Molotkov 84](#Molotkov84), [Konechny-Schwarz 97](KonechnySchwarz97)
of which a clean account is given in [Sachse 08](#Sachse08). These authors consider (pre-)sheaves on the category of
[[superpoints]]. This gives the "super" in "super-geometry" a functorial interpretation, but the
(smooth) "geometry" still needs to be added in by hand. Hence this approach satisfies [Grothendieck's urging](#Grothendieck73)
half-way.

The full application of the perspective of [[functorial geometry]] to [[supergeometry]] is known as
_[[synthetic differential supergeometry]]_, where one considers sheaves over the full category of formal
[[super Cartesian spaces]] ([Yetter 88, section 3](#Yetter88)). This is essentially the perspective which we adopt here.
We do however not refer to the (super-)[[Kock-Lawvere axioms]] for [[synthetic differential geometry]] but instead
use the axiomatics of "[[differential cohesion]]" ([Schreiber 13](#Schreiber)). This we explain [below](#SuperSmoothSets).





## Super Cartesian spaces
 {#CoordinareSystemsSuperCartesianSpaces}

For reference, recall:

+-- {: .num_defn #SuperCartesianSpace}
###### Definition
**([[Grassmann algebra]])**

For $q\in \mathbb{N}$, the real [[Grassmann algebra]]

$$
  C^\infty(\mathbb{R}^{0|q})
  \coloneqq
  \wedge^\bullet \langle \theta_1, \cdots, \theta_q\rangle
$$

is the $\mathbb{R}$-algebra [[free functor|freely]] generated from $q$ generators $\{\theta_i\}_{i = 1}^q$
(now regarded as being in odd degree), subject to the relations

$$
  \theta_i \theta_j = - \theta_j \theta_i
$$

for all $i,j \in \{1,\cdots, q\}$. In particular

$$
  \theta_i \theta_i = 0
$$

for all $i \in \{1, \cdots, q\}$ (since $\mathbb{R}$ has [[characteristic zero]] and in particular $char(\mathbb{R}) \neq 2$).

For $p,q \in \mathbb{N}$, the [[super-Cartesian space]] $\mathbb{R}^{p|q}$ is the [[formal dual]] of the [[supercommutative superalgebra]] written $\mathcal{O}(\mathbb{R}^{p\vert q})$ or $C^\infty(\mathbb{R}^{p|q})$ whose underlying
$\mathbb{Z}/2\mathbb{Z}$-[[graded vector space]] is


$$
  C^\infty(\mathbb{R}^{p|q})
  \coloneqq
  C^\infty(\mathbb{R}^p) \otimes_{\mathbb{R}} \wedge^\bullet\langle\theta_1, \cdots, \theta_q\rangle
$$

with the product given by the relations

$$
  \begin{aligned}
  \left(
    f \theta_{i_1}\cdots \theta_{i_k}
  \right)
  \left(
    g \theta_{j_1}\cdots \theta_{j_l}
  \right)
  & =
  f \cdot g \; \theta_{i_1}\cdots \theta_{i_k} \theta_{j_1}\cdots \theta_{j_l}
  \\
  & =
  (-1)^{k l} g\cdot f \; \theta_{j_1}\cdots \theta_{j_l} \theta_{i_1}\cdots \theta_{i_k}
  \end{aligned}
$$

where $f \cdot g$ is the ordinary pointwise product of [[smooth functions]]:

$$
  \mathbb{R}^{p \vert q}
    \coloneqq
  Spec( C^\infty(\mathbb{R}^p) \otimes_{\mathbb{R}} \wedge^\bullet (\mathbb{R}^q)^\ast )
  \,.
$$

Write

$$
 SuperCartSp \hookrightarrow sCAlg_{\mathbb{R}}^{op}
$$

for the [[full subcategory]] of the [[opposite category]] of [[commutative superalgebras]] on those of this form. We write
$\mathbb{R}^{p|q} \in SuperCartSp$ for the [[formal dual]] of
$C^\infty(\mathbb{R}^{p|q})$.

=--



Moreover, we write

$$
  CartSp 
    \overset{\phantom{AAAA}}{\hookrightarrow}
  SuperCartSp
$$

for the [[full subcategory]] on ordinary [[Cartesian spaces]] with [[smooth functions]] between them. These are the "abstract coordinate charts" from the discussion at _[[geometry of physics -- smooth sets]]_,
and so we are evidently entitled to think of the objects in $SuperCartSp$ as **abstract super coordinate systems** and to develop a geometry induced from these.

Recall the three magic algebraic properties of [[smooth functions]] that make the above algebraic description of [[differential geometry]] work:

+-- {: .num_prop #FirstTwoMagicPropertiesOfAlgebrasOfSmoothFunctions}
###### Proposition
**(first two magic properties of [[algebra of functions|algebras of]] [[smooth functions]])**


1. (**[[embedding of smooth manifolds into formal duals of R-algebras]]**)

   The [[functor]] that assigns [[algebra of functions|algebras of]] [[smooth functions]] to [[smooth manifolds]]

   $$
     C^\infty(-) 
       \;\colon\; 
     SmthMfd 
      \overset{\phantom{AAAA}}{\hookrightarrow} 
     CAlg_{\mathbb{R}}^{op}
      \overset{\phantom{AAAA}}{\hookrightarrow}
     sCAlg_{\mathbb{R}}^{op}
   $$

   is [[fully faithful functor|fully faithful]] ([this Def.](geometry+of+physics+--+categories+and+toposes#FullyFaithfulFunctor)).

1. (**[[smooth Serre-Swan theorem]]**)

   The functor that assigns smooth [[sections]] of smooth [[vector bundles]]
   of [[finite number|finite]] [[rank]]

   $$
     \Gamma_X(-) \;\colon\; SmthVectBund_{/X} \hookrightarrow C^\infty(X) Mod
   $$

   is [[fully faithful functor|fully faithful]] (its [[essential image]] being the [[finitely generated object|finitely generated]] [[projective modules]] over the $\mathbb{R}$-[[algebra of functions|algebra of]] [[smooth functions]]).

   ([Nestruev 03, theorem 11.32](smooth+Serre-Swan+theorem#Nestruev03))

   Moreover, the [[modules]] over the $\mathbb{R}$-algebra $C^\infty(X)$
   of [[smooth functions]] on $X$ which arise this way as [[sections]] of [[smooth vector bundles]] over a [[Cartesian space]] $X$ are precisely the [[finitely generated module|finitely generated]] [[free modules]] over $C^\infty(X)$.

   ([Nestruev 03, theorem 11.32](smooth+Serre-Swan+theorem#Nestruev03))

=--

There is a third such magic algebraic property of smooth functions, which plays a role now:

+-- {: .num_defn #DerivationsOfSmoothFunctions}
###### Proposition
**([[derivations of smooth functions are vector fields]])**

Let $X$ be a [[smooth manifold]]. Write

$$
  der_X \;\colon\; \Gamma(T X) \longrightarrow Der(C^\infty(X))
$$

for the function that sends a smooth [[vector field]] $v \in \Gamma(T X)$ to the [[derivation]]
of the [[algebra of functions|algebra of]] [[smooth functions]] on $X$ given by forming
[[derivatives]]: $der_X(v)(f) \coloneqq v(f)$. This is a [[derivation]] by the [[chain rule]].

Then this function is a [[bijection]], hence every [[derivation]] of $C^\infty(X) \in CAlg_{\mathbb{R}}$
comes from [[differentiation]] along some smooth vector field, which is uniquely defined thereby.

=--

+-- {: .proof}
###### Proof

By the existence of [[partitions of unity]] we may restrict to the situation where $X = \mathbb{R}^n$ is a [[Cartesian space]].
By the [[Hadamard lemma]] every [[smooth function]] $f \in C^\infty(\mathbb{R}^n)$ may be written as

$$
  f(x) = f(0) + \sum_i x_i g_i(x)
$$

for [[smooth functions]] $\{g_i \in C^\infty(X)\}$ with $g_i(0) = \frac{\partial f}{\partial x_i}(0)$. Since any derivation $\delta : C^\infty(X) \to C^\infty(X)$ by definition satisfies the Leibniz rule, it follows that

$$
  \delta(f)(0) = \sum_i \delta(x_i) \frac{\partial f}{\partial x_i}(0)
  \,.
$$

Similarly, by translation, at all other points. Therefore $\delta$ is already fixed by its action of the coordinate functions $\{x_i \in C^\infty(X)\}$. Let $v_\delta \in T \mathbb{R}^n$ be the [[vector field]]

$$
  v_\delta \coloneqq \sum_i \delta(x_i) \frac{\partial}{\partial x_i}
$$

then it follows that $\delta$ is the derivation coming from $v_\delta$ under $\Gamma_X(T X) \to Der(C^\infty(X))$.
=--


Recall further from _[[geometry of physics -- superalgebra]]_ that the category of [[supercommutative superalgebras]]
is related to that of ordinary [[commutative algebras]] over $\mathbb{R}$ by an [[adjoint cylinder]] ([this prop.](geometry+of+physics+--+superalgebra#InclusionOfCAlgIntosCAlg)):

+-- {: .num_prop #AdjointCylinderOnSuperAffines}
###### Proposition
**([[adjoint modality]] of [[fermionic modality|even fermionic]] and [[bosonic modality|bosonic]] in [[superalgebras]])**

The canonical inclusion of [[commutative algebras]] into [[supercommutative superalgebra|supercommutative superalgebras]] is
part of an [[fully faithful functor|fully faithful]] [[adjoint triple]] ([this Def.](geometry+of+physics+--+categories+and+toposes#AdjointModality)) of the form

$$
  (-)_{even}
  \;\dashv\;
  \iota^{op}
  \;\dashv\;
  (-)/(-)_{odd}
  \;\;\colon\;\;
  CAlg_k
    \underoverset
      {\underset{\phantom{AA}(-)_{even}\phantom{AA}}{\longleftarrow}}
      {\overset{\phantom{AA}(-)/(-)_{odd}\phantom{AA}}{\longleftarrow}}
      {\overset{\phantom{AAAA}\iota^{op}\phantom{AAAA}}{\hookrightarrow}}
  sCAlg_k
  \,.
$$

(Here and in the following we display pairs of [[adjoint functors]] ([this Def.](geometry+of+physics+–+basic+notions+of+category+theory#AdjointFunctorsInTermsOfNaturalBijectionOfHomSets)) such that the [[left adjoint]] is on top and the right adjoint is on the bottom.)

The [[formal dual]] ([this Def.](geometry+of+physics+--+categories+and+toposes#OppositeCategory)) of this statement is that [[affine superschemes]] are related to ordinary [[affine schemes]] over $\mathbb{R}$ by an [[adjoint modality]] of this form

$$
  even
    \;\dashv\;
  \iota_{sup}
    \;\;\colon\;\;
  Disc_{sup}
  Aff(Vect_k)
    \underoverset
      {\underset
        {
          \phantom{AA}
            \Pi_{sup}
          \phantom{AA}
         }
         {\longleftarrow}
      }
      {\overset
         {
          \phantom{AA}
           even
          \phantom{AA}
        }
        {\longleftarrow}
      }
      {\overset{ \phantom{AAA} \iota \phantom{AAA} }{\hookrightarrow}}
  Aff(sVect_k)
  \,.
$$

=--

Beware that

1. $\Pi_{sup}$ is the [[formal dual]] of $(-)/(-)_{odd}$,

1. $even$ is the [[formal dual]] of $(-)_{even}$.

That they change position in the diagrams is because we always draw [[left adjoints]] on top of [[right adjoints]] and  the handedness of [[adjoints]] changes as we pass to [[opposite categories]].


+-- {: .num_example #EvenPartOfDimTwoSuperpoint}
###### Example

The [[algebra of functions]] on $even({\mathbb{R}^{0\vert 2}})$ is

$$
  \begin{aligned}
   \mathcal{O}\left( even({\mathbb{R}^{0\vert 2}})\right)
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
  \mathbb{R}[\epsilon]/(\epsilon^2)
  \end{aligned}
$$

where in the last line we renamed $\theta_1 \theta_2$ to $\epsilon$.


This algebra $\mathbb{R}[\epsilon]/(\epsilon^2)$
is known as the **[[algebra of dual numbers]]** over $\mathbb{R}$. It is to be thought of as the [[algebra of functions]]
on a bosonic but [[infinitesimally thickened point]], an [[infinitesimal neighbourhood]] of a point inside the [[real line]] which is "so very small"
that the canonical [[coordinate]] function $\epsilon$ on it takes values "so tiny" that its square, which is bound to be even tinier, is actually indistinguishable from [[zero]].

We will write

$$
  \mathbb{D}^1
    \;\coloneqq\; Spec(\mathbb{R}[\epsilon]/(\epsilon^2))
  \;\in\;
  Aff(sVect_k)
$$

for the [[space]] [[formal dual|formally dual]] to this [[algebra of dual numbers]] and think of it as the _1-dimensional first order [[infinitesimal disk]]_.


=--

In generalization of this we make the following definitions:

+-- {: .num_defn #FormalCartSp}
###### Definition
**([[formal Cartesian spaces]])**

Write

$$
  \array{
    InfPoint 
      &\overset{\phantom{AAA}}{\hookrightarrow}&
    CAlg_{\mathbb{R}}^{op}
    \\
    \mathbb{D}_V
    &\mapsto&
    \mathbb{R} \oplus V
  }
$$

for the [[full subcategory]] ([this Example](geometry+of+physics+--+categories+and+toposes#FullSubcategoryOnClassOfObjects)) of the [[opposite category]] ([this Example](geometry+of+physics+--+categories+and+toposes#OppositeCategory)) of [[commutative algebras]] over $\mathbb{R}$ on [[formal duals]]
$\mathbb{D}$ of [[commutative algebras]] over the [[real numbers]] of the form

$$
  \mathcal{O}(\mathbb{D}_V)
    \;\coloneqq\;
  (\mathbb{R}\oplus V)
  \,,
$$

with $V$ a [[nilpotent ideal]] of [[finite number|finite]]-[[dimension]]
over $\mathbb{R}$ (the [[direct sum]] on the right is that of underlying [[vector spaces]], not of algebras).

We call this the [[category]] of _[[infinitesimally thickened points]]_.

Alternative terminology:

1. In [[synthetic differential geometry]] these algebras are called [[Weil algebra|Weil algebras]]**,

1. in [[algebraic geometry]] they are known as _[[local ring|local]] [[real numbers|real]] [[Artin algebras]]_.

Write moreover

$$
  \array{
    FormalCartSp
     &\overset{\phantom{AAAA}}{\hookrightarrow}&
    CAlg_{\mathbb{R}}^{op}
    \\
    \mathbb{R}^n \times \mathbb{D}_V
    &\mapsto&
    C^\infty(\mathbb{R}^n) \otimes_{\mathbb{R}} (\mathbb{R} \oplus V)
  }
$$

for the [[full subcategory]] on [[formal duals]] $\mathbb{R}^n \times \mathbb{D}$ of those algebras which are [[tensor products]] of commutative $\mathbb{R}$-algebras of the form

$$
  \mathcal{O}(\mathbb{R}^n \times \mathbb{D})
    \coloneqq
   C^\infty(\mathbb{R}^n) \otimes_{\mathbb{R}} C^\infty(\mathbb{D})
$$

of algebras $C^\infty(\mathbb{R}^p)$ of [[smooth functions]] $\mathbb{R}^n$
with algebras corresponding to infinitesimally thickened points $\mathbb{D}$ as above.

=--

+-- {: .num_remark #FormalSchemesAndSDG}
###### Remark
**([[formal schemes]] and [[synthetic differential geometry]])**

This kind of construction in Def. \ref{FormalCartSp} is traditionally more familiar from the theory of [[formal schemes]], but the same kind of general abstract theory goes through in the context of [[differential geometry]], a point of view known as _[[synthetic differential geometry]]_ ([[Toposes of laws of motion|Lawvere 97]]), preconfigured already in the prespective of _[[functorial geometry]]_ of [Grothendieck 65](functorial+geometry#Grothendieck65).

=--

The crucial property of [[infinitesimally thickened points]] (def. \ref{FormalCartSp}) is that they co-represent [[tangent vectors]] and [[jets]]:

+-- {: .num_example #HomsOutOfFirstOrderInfinitesimalLine}
###### Example
**([[morphisms]] out of [[infinitesimally thickened point]] are [[tangent vectors]])**

Write $\mathbb{D}^1 = Spec(\mathbb{R}[\epsilon]/(\epsilon^2))$ for the [[formal dual]] of the [[algebra of dual numbers]]
(example \ref{EvenPartOfDimTwoSuperpoint}).
Then morphisms in $FormalCartSp$ (def. \ref{FormalCartSp}) of the form

$$
  \mathbb{R}^n \times \mathbb{D}^1 \longrightarrow \mathbb{R}^n
$$

which are the identity after restriction along $\mathbb{R}^n \to  \mathbb{R}^n \times \mathbb{D}^1$, are in [[natural bijection]]
with smooth [[vector fields]] on $\mathbb{R}^n$.

Moreover, morphisms of the form

$$
  \mathbb{D}^1 \longrightarrow \mathbb{R}^n
$$

are equivalently single [[tangent vectors]], hence for every $\mathbb{R}^n$ there is a [[natural bijection]]

$$
  Hom_{FormalCartSp}(\mathbb{D}^1, \mathbb{R}^n)
   \simeq
  \underset{\text{underlying} \atop \text{set}}{\underbrace{T \mathbb{R}^n}}
$$

between the [[hom-set]] from the formal dual of the [[ring of dual numbers]]
and the set of [[tangent vectors]].

=--

+-- {: .proof}
###### Proof

By definition, morphisms

$$
  \mathbb{R}^n \times \mathbb{D}\longrightarrow \mathbb{R}^n
$$

which are the identity after restriction along $\mathbb{R}^n \to \mathbb{R}^n \times \mathbb{D}$, are
equivalently algebra homomorphisms of the form


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

This means equivalently that $\partial\colon C^\infty(\mathbb{R}^n)\to C^\infty(\mathbb{R}^n)$ is a [[derivation]].
But [[derivations of smooth functions are vector fields]] (prop. \ref{DerivationsOfSmoothFunctions}).

=--

We now explore further the relations between [[Cartesian spaces]], [[formal Cartesian spaces]], and [[super formal Cartesian spaces]].

+-- {: .num_prop #CartSpCoreflectiveInclusion}
###### Proposition
**([[coreflective subcategory|co-reflection]] of [[Cartesian spaces]] inside [[formal Cartesian spaces]])**

The canonical inclusion $\iota$ of the [[category]] of ordinary [[Cartesian spaces]] into that of [[formal manifold|formal]] [[Cartesian spaces]]
has a [[left adjoint]] ([this Def.](geometry+of+physics+–+basic+notions+of+category+theory#AdjointFunctorsInTermsOfNaturalBijectionOfHomSets)) $\Re$ ("[[reduction modality|reduction]]")

$$
  CartSp
    \underoverset
      {\underset{\phantom{AA}\Pi_{inf} \phantom{AA}}{\longleftarrow}}
      {\overset{\phantom{AA}\iota_{inf} \phantom{AA}}{\hookrightarrow}}
      {\bot}
  FormalCartSp
$$

given by

$$
  \Pi_{inf}(\mathbb{R}^n \times \mathbb{D}) \coloneqq \mathbb{R}^n
  \,.
$$

Hence $\iota$ exhibits $CartSp$ as a [[coreflective subcategory]] ([this Def.](geometry+of+physics+--+categories+and+toposes#ReflectiveSubcategory)) of $FormalCartSp$

We say that $\mathbb{R}^n$ is the **[[reduced scheme]]** of $\mathbb{R}^n \times \mathbb{D}$.

=--

+-- {: .proof}
###### Proof

We check the [[natural isomorphism]] on [[hom-sets]] that characterizes a pair of [[adjoint functors]] ([here](geometry+of+physics+--+categories+and+toposes#eq:HomIsomorphismForAdjointFunctors)):

By definition, a morphism of the form

$$
  f \;\colon\; i(\mathbb{R}^{n_1}) \longrightarrow \mathbb{R}^{n_2} \times \mathbb{D}
$$

is equivalently a [[homomorphism]] of [[commutative algebras]] of the form

$$
  f^\ast
   \;\colon\;
  C^\infty(\mathbb{R}^{n_1})
    \longleftarrow
  C^\infty(\mathbb{R}^{n_2}) \otimes_{\mathbb{R}} (\mathbb{R} \oplus V)
$$

where all elements $v \in V$ are nilpotent, in that there exists $n_v \in \mathbb{N}$ such that $(v)^{n_v} = 0$. Every algebra homomorphism needs to preserve this equation, and hence needs to send nilpotent elements to nilpotent elements. But the only nilpotent element in the ordinary function algebra $C^\infty(\mathbb{R}^n)$ is the zero-function, and so it follows that the above homomorphism has to vanish on all of $V$, hence has to factor (necessarily uniquely) through a homomorphism of the form

$$
  \tilde f^\ast
   \;\colon\;
  C^\infty(\mathbb{R}^{n_1})
    \longleftarrow
  C^\infty(\mathbb{R}^{n_2})
  \,.
$$

This is dually a morphism of the form

$$
  \tilde f \;\colon\; \mathbb{R}^{n_1} \longrightarrow \mathbb{R}^{n_2}
$$

in $CartSp$. This establishes a natural bijection $f \leftrightarrow \tilde f$.


=--



The above discussion following prop. \ref{AdjointCylinderOnSuperAffines} means that in passing to commutative superalgebras there are _two_ stages of generalizations of plain differential geometry involved:

1. [[Cartesian spaces]] are generalized to [[formal manifold|formal]] [[Cartesian spaces]];

1. [[formal manifold|formal]] [[Cartesian spaces]] are further generalized to [[super formal Cartesian spaces]].

In order to make this explicit, it is convenient to introduce the following slight generalization of [[super Cartesian spaces]] (def. \ref{SuperCartesianSpace}), which are simply [[Cartesian products]]
of ordinary [[Cartesian spaces]] with an [[infinitesimally thickened point]] that may have both even and odd graded elements in its [[algebra of functions]].


+-- {: .num_defn #SuperFormalCartSp}
###### Definition
**([[super formal Cartesian spaces]])**

Write

$$
  \array{
    SuperFormalCartSp
      &\overset{ \phantom{AA} \iota \phantom{AA} }{\hookrightarrow}&
    sCAlg_{\mathbb{R}}^{op}
    \\
    \mathbb{R}^{n\vert q} \times \mathbb{D}_V
    =
    \mathbb{R}^n \times \mathbb{R}^{0 \vert q}  \times \mathbb{D}_V
    &
    \mapsto
    &
    C^\infty( \mathbb{R}^{n} )
    \otimes_{\mathbb{R}}
    \wedge^\bullet( \mathbb{R}^q )
    \otimes_{\mathbb{R}}
    (\mathbb{R} \oplus V)
  }
$$

for the [[full subcategory]] ([this Example](geometry+of+physics+--+categories+and+toposes#FullSubcategoryOnClassOfObjects)) of that of the [[opposite category]] of [[supercommutative superalgebras]] on those which are [[tensor product of algebras|tensor products of commutative algebras]] of 

1. the [[algebra of functions|algebra of]] [[smooth functions]] on a [[Cartesian space]],

1. a [[Grassmann algebra]] (Def. \ref{SuperCartesianSpace}),

1. a [[Weil algebra]] (Def. \ref{FormalCartSp})

=--

One place in the literature where such [[super formal Cartesian spaces]] are made explicit is in [Konechny-Schwarz 97](#KonechnySchwarz97).

Just as formal Cartesian spaces may be thought of as local model spaces for [[synthetic differential geometry]], [[super formal Cartesian spaces]] may be thought of as a model for [[synthetic differential supergeometry]].
This we come to [below](#SuperSmoothSets).

For completeness it is useful to compare the [[coreflective subcategory|coreflection]] of prop. \ref{CartSpCoreflectiveInclusion}
to the following simple [[reflective subcategory|reflection]].

Write

$$
  \ast \in Cat
$$

for the [[category]] with a single object and a single morphism (the [[identity]]) on that object.
We will think of this as the category containing just the point space, which we want to think
of as the local model space for _[[discrete topological space|discrete geometry]]_.


+-- {: .num_prop #ReflectionOfPointInCartSp}
###### Proposition

There is a pair of [[adjoint functors]]

$$
  \ast
  \;
    \underoverset
      {\underset{}{\hookrightarrow}}
      {\overset{\Pi}{\longleftarrow}}
      {}
  \;CartSp
$$

into the category of [[Cartesian spaces]],
where the bottom functor sends the unique object to the point $\mathbb{R}^0$, and where its [[left adjoint]] on
top is, necessarily, the unique functor constant on the unique object on the left.

=--

+-- {: .proof}
###### Proof

The [[natural isomorphism]] between [[hom sets]] characterizing this pair of [[adjoint functors]]
simply expresses the fact that $\mathbb{R}^0$ is the [[terminal object]] in $CartSp$, hence that
for $\mathbb{R}^n$ any [[Cartesian space]], then there is a unique [[smooth function]] of the form
$\mathbb{R}^n \to \mathbb{R}^0$.

=--

In conclusion, the various [[extra structures]] on local model spaces (abstract coordinate systems) which we
considered are organized in the following [[diagram]]:

+-- {: .num_prop #SystemOfSites}
###### Proposition
**(progression of ([[coreflective subcategory|co-]])[[reflective subcategory|reflective]] [[site]]-inclusions)**

The [[coreflective subcategory]] inclusion of [[Cartesian spaces]] into
[[formal manifold|formal]] [[Cartesian spaces]] from prop. \ref{CartSpCoreflectiveInclusion}
and the coreflective as well as [[reflective subcategory]] inclusion
of affine schemes into [[affine superschemes]] from prop. \ref{AdjointCylinderOnSuperAffines}
and the terminal inclusion of prop. \ref{ReflectionOfPointInCartSp}
combine to give the following system of [[adjoint functors]] on our local model spaces


$$
  \array{
   { \text{}  \atop { \text{discrete} \atop {\text{geometry}} } }
   &&
   {\text{} \atop {\text{differential} \atop \text{geometry}}}
   &&
   {\text{formal} \atop {\text{differential} \atop {geometry}}}
   &&
   {\text{super} \atop {\text{differential} \atop \text{geometry}}}
   \\
   \\
   \ast
   &
   \array{
     \overset{\phantom{AA}\Pi\phantom{AA}}{\longleftarrow}
     \\
     \overset{\phantom{AA}Disc\phantom{AA}}{\hookrightarrow}
   }
   &
  CartSp
   &
   \array{
     \overset{\phantom{AA}\iota_{inf}\phantom{AA}}{\hookrightarrow}
     \\
     \overset{\phantom{AA}\Pi_{inf}\phantom{AA}}{\longleftarrow}
     \\
     \phantom{A}
     \\
     \phantom{A \atop A}
   }
   &
  FormalCartSp
  &
   \array{
     \overset{\phantom{AA}even\phantom{AA}}{\longleftarrow}
     \\
     \overset{\phantom{AA}\iota_{sup}\phantom{AA}}{\hookrightarrow}
     \\
     \overset{\phantom{AA}\Pi_{sup}\phantom{AA}}{\longleftarrow}
     \\
     \phantom{A}
     \\
     \phantom{A \atop A}
     \\
     \phantom{A \atop A}
   }
  &
  SuperFormalCartSp
  }
  \,.
$$

=--





## Super smooth sets
 {#SuperSmoothSets}

[Above](#CoordinareSystemsSuperCartesianSpaces) we discussed ([[formal manifold|formal]]) [[super Cartesian spaces]]. What we are after is geometry of [[generalized space]] which is "locally modeled" on these, in the sense explained in the chapter _[[geometry of physics -- categories and toposes|on categories and toposes]]_ . In order to do so we

1. consider [[generalized space|generalized]] [[superspaces]] whose collection forms a "good category" (the [[sheaf topos]] over super Cartesian space) in that lots of [[universal constructions]] on general superspaces ([[limits]], [[colimits]]) still yield general superspaces;

2. use special properties of this nice category ([[differential cohesion]]) in order to characterize and construct the good, tame superspaces, such as actual [[supermanifolds]].


The construction proceeds in direct anology to the non-super version discussed in the chapters _[[geometry of physics -- smooth sets|on smooth sets]]_ and _[[geometry of physics -- manifolds and orbifolds|on manifolds and orbifolds]]_. For reference we first briefly recall this [[bosonic modality|bosonic]] situation.

The following simple definitions \ref{SmoothSet} and \ref{FormalSmoothSets} are key to the whole theory. They embody the perspective of _[[functorial geometry]]_ ([Grothendieck 65](#Grothendieck65)).
See remark \ref{ASheafAsASpace} below for exegesis and illustration.


+-- {: .num_defn #SiteCartSp}
###### Definition
**([[CartSp]])**

Write [[CartSp]] for the [[category]] of [[Cartesian space]] $\mathbb{R}^n$ for $n \in\mathbb{N}$ with [[smooth functions]] between them. Say that a collection of morphisms $\{U_i \to X\}$ in $CartSp$ is [[covering]] if this is a [[good open cover]] in that every finite non-empty intersection of the charts is [[diffeomorphism|diffeomorphic]] to a Cartesian space.
This defines a [[coverage]] on [[CartSp]] and hence makes it a [[site]].

=--


+-- {: .num_defn #SmoothSet}
###### Definition
**([[smooth set]])**

We say a _[[smooth set]]_ ([this Def.](geometry+of+physics+--+smooth sets#CategoryOfSmoothSets)) is, equivalently, a [[sheaf]] on [[CartSp]] (Def. \ref{SiteCartSp}), according to [this Prop.](geometry+of+physics+--+smooth sets#SmoothSetsAreSheavesOnCartSp). We write

$$
 SmoothSet \;\coloneqq\; Sh(CartSp)
$$

for the [[sheaf topos]] ([this Def.](geometry+of+physics+--+categories+and+toposes#Sheaf)) of smooth set.

=--

+-- {: .num_remark #ASheafAsASpace}
###### Remark
**([[functorial geometry]])**

The useful way to think of def. \ref{SmoothSet} in the present context is as defining a kind of [[generalized smooth space]] which is _defined_ by which smooth functions from Cartesian spaces it receives (see also at _[[motivation for sheaves, cohomology and higher stacks]]_ for more exposition of this point).

Namely a smooth set $X$ in the sense of def. \ref{SmoothSet} is first of all a rule

$$
  \mathbb{R}^p \mapsto  X(\mathbb{R}^p) \in Set
$$


which assigns a set to each Cartesian space. We are to think of this set $X(\mathbb{R}^n)$ as the set of smooth functions {"$\mathbb{R}^n \stackrel{}{\to} X$"}, only that there is no pre-defined concept of smoothness of functions into $X$, instead it is defined by that very rule.
Moreover, for every smooth function
$f$ between Cartesian spaces, there is to be a corresponding function $f^\ast$ between these sets, going in the opposite direction

$$
  \array{
    \mathbb{R}^{n_1}
    \\
    \downarrow^{\mathrlap{f}}
    \\
    \mathbb{R}^{n_2}
  }
  \;\;\;
    \mapsto
  \;\;\;
  \array{
    X(\mathbb{R}^{n_1})
    \\
    \uparrow^{\mathrlap{f^\ast}}
    \\
    X(\mathbb{R}^{n_2})
  }
$$

which we are to think of as being the precomposition operation

$$
  (\text{"}\mathbb{R}^{n_2} \stackrel{\phi}{\to} X\text{"})
     \;\mapsto\;
  (\text{"}f^\ast \phi \colon \mathbb{R}^{n_1} \overset{f}{\to} \mathbb{R}^{n_2} \overset{\phi}{\to} X\text{"})
  \,.
$$

This is required to satisfy the evident conditions that [[composition]] and [[identity]] is respected, in that
$(g \circ f)^\ast = g^\ast \circ f^\ast $ and $id^\ast = id$. Together these conditions say that $X$ is a
[[presheaf]] on the category of test spaces -- the "[[functor of points]]" ([Grothendieck 65](#Grothendieck65)).

In addition, the requirement that $X$ be a [[sheaf]] on the [[site]] of Cartesian spaces from def. \ref{SiteCartSp}
means that the assignment $\mathbb{R}^n \mapsto X(\mathbb{R}^n)$ knows that one coordinate system
$\mathbb{R}^n$ may be covered by other coordinate systems. Namely let $\{U_i \overset{\phi_i}{\to}\}$
be an [[open cover]] by [[open balls]] $U_i$ (each of which may be identified with $\mathbb{R}^n$ itself, by a [[diffeomorphism]])
then the condition is that the function

$$
  (\text{"}\mathbb{R}^n \to X\text{"})
    \mapsto
  \left\{
    \text{"}U_i \overset{\phi_i}{\to} \mathbb{R}^n \to X\text{"}
  \right\}
$$

is a [[bijection]] from $X(\mathbb{R}^n)$ to the subset of the [[Cartesian product]] $\underset{i}{\prod} X(U_i)$
of those [[tuples]] of functions $U_i \stackrel{f_i}{\to} X$ which coincide on all [[intersections]]:
$f_i |_{U_i \cap U_j} = f_j |_{U_i \cap U_j}$ ("[[matching families]]").

For example every [[Cartesian space]] $X$ defines a smooth set by the rule

$$
  \mathbb{R}^n \mapsto C^\infty(\mathbb{R}^n ,X)
$$

which says that the set of would-be smooth functions into $X$ is the actual set of smooth functions into $X$.
One also says that $X$ [[representable functor|represents]] a sheaf on $CartSp$,

This defines a [[full subcategory]] inclusion of Cartesian spaces into smooth sets

$$
  y \;\colon\; CartSp \hookrightarrow SmoothSet
$$

called the _[[Yoneda embedding]]_.

The same construction works for $X$ any [[smooth manifold]]: it is regarded as a smooth set defined by the rule

$$
  \mathbb{R}^n \mapsto C^\infty(\mathbb{R}^n ,X)
$$

which assigns actual sets of smooth functions.

Notice that since Cartesian spaces (and smooth manifolds) themselves are understood as special cases of smooth sets, there now appears an
actual concept of smooth functions of the form $\mathbb{R}^n \to X$, for every smooth set $X$, without quotation marks:
namely this is a morphism in the category $SmoothSet$ of smooth sets.

Now there might be a worry: given any smooth set $X$ and any Cartesian space $\mathbb{R}^n$, we seem to have _two different_
concepts of what the set of smooth functions from $\mathbb{R}^n$ to $X$ is: the set $X(\mathbb{R}^n)$
of "smooth functions by fiat" (maps with quotation marks) and the actual [[hom-set]] $Hom_{SmoothSet}(\mathbb{R}^n, X)$
(maps without quotation mark).

That these two sets are in fact in [[natural bijection]], hence that the interpretation of a sheaf $X$ as a generalized smooth space
is consistent, is the statement of the _[[Yoneda lemma]]_:

$$
  Hom_{SmoothSet}(\mathbb{R}^n, X)
  \;
    \simeq
  \;
  X(\mathbb{R}^n)
  \,.
$$

Hence the [[Yoneda lemma]] says that we may remove the quotation marks:

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

+-- {: .num_remark #GeneralizedSpaces}
###### Remark
**([[generalized spaces]])**

The strategy is now to work in the nice category $SmoothSets$ of [[generalized smooth spaces]] (a [[topos]]),
and find in there [[full subcategories]] of more specific types of smooth spaces having extra properties which one may need in given applications. There is a long list of such subcategories of relevance, some of these we briefly discuss now:

$\{$[[Cartesian spaces]]$\}$
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
 $\cdots$
 $\hookrightarrow$
$\{$[[smooth sets]]$\}$
 $\hookrightarrow$
$\{$[[formal smooth sets]]$\}$
 $\hookrightarrow$
$\{$[[super formal smooth sets]]$\}$

and similarly for their supergeometric version (which we turn to below, def. \ref{FormalSmoothSets})

$\{$[[Cartesian spaces]]$\}$
 $\hookrightarrow$
$\{$[[super Cartesian spaces]]$\}$
 $\hookrightarrow$
$\{$[[supermanifolds]]$\}$
 $\hookrightarrow$
 $\cdots$
 $\hookrightarrow$
$\{$[[super formal smooth sets|super smooth sets]]$\}$ .

=--




By the strategy of remark \ref{GeneralizedSpaces} we now pass to generalized spaces which are locally modeled not just on plain Cartesian spaces, but also on [[formal Cartesian spaces]] and [[super formal Cartesian spaces]]


+-- {: .num_defn #FormalSmoothSets}
###### Definition
**([[super formal smooth sets]])**

Define a [[coverage]] on the categories $FormalCartSp$ (def. \ref{FormalCartSp}) and on $SuperFormalCartSp$ (def. \ref{SuperFormalCartSp}) by declaring the [[covering]] families of any object $\mathbb{R}^n \times \mathbb{D}$ (hence for $\mathbb{D}$ with $\mathcal{O}(\mathbb{D}) = (\mathbb{R} \oplus V)$ any infinitesimally thickened
superpoint) to be those of the form

$$
  \left\{
    U_i \times \mathbb{D}
      \overset{\phi_i \times id}{\longrightarrow}
    \mathbb{R}^n \times \mathbb{D}
  \right\}
$$

for

$$
  \left\{
    U_i
      \overset{\phi_i }{\longrightarrow}
    \mathbb{R}^n
  \right\}
$$

a [[good open cover]] as in def. \ref{SiteCartSp}.

In analogy with def. \ref{SmoothSet} we say that

1. a [[sheaf]] on $FormalCartSp$ is a **[[formal smooth set]]** or **formal smooth [[0-type]]** and we write

  $$
    FormalSmoothSet \coloneqq FormalSmoothSet \coloneqq Sh(FormalCartSp)
  $$

  for the [[sheaf topos]] of all of these;

1. a [[sheaf]] on $FormalCartSp$ is a **[[super formal smooth set]]** or **super formal smooth [[0-type]]** and we write

  $$
    SuperFormalSmoothSet \coloneqq SuperFormalSmoothSet \coloneqq Sh(FormalCartSp)
  $$

  for the [[sheaf topos]] of all of these;

=--

The category of [[formal smooth sets]] from def. \ref{FormalSmoothSets} is often known as the _[[Cahiers topos]]_. It was introduced in ([Dubuc 79](Cahiers+topos#Dubuc79)) as a well-adapted model for the [[Kock-Lawvere axioms]] for [[synthetic differential geometry]].
The category of [[super formal smooth sets]] from def. \ref{FormalSmoothSets} was considered in [Yetter 88](#Yetter88), called the _super Dubuc topos_ there.

We have now defined four sites
and considered the corresponding [[categories of sheaves]] (noticing that $Sh(\ast) = $ [[Set]])

$$
  \array{
    \mathcal{C} = & \ast & CartSp & FormalCartSp & SuperFormalCartSp
    \\
    \\
    Sh(\mathcal{C}) =  & Set & SmoothSet & FormalSmoothSet & SuperFormalSmoothSet
  }
  \,.
$$

Moreover, by prop. \ref{SystemOfSites} these four sites form a [[filtration]] of the site $SuperFormalCartSp$
by consecutively smaller subsites, where each inclusion is either [[reflective subcategory|reflective]]
or [[coreflective subcategory|coreflective]] or both. The following states that this filtration of sites extends to their categories of sheaves.



+-- {: .num_prop #SuperSmoothSetsSystemOfAdjunctions}
###### Proposition
**(progression of ([[coreflective subcategory|co-]])[[reflective subcategories]] of [[SuperFormalSmoothSet]])**

The [[sheaf topos]] [[SuperFormalSmoothSet]] (Def. \ref{FormalSmoothSets}) is a _[[solid topos]]_ over [[FormalSmoothSet]], in that:

There exists an essentially unique system of [[functors]] between the categories of [[sets]], [[smooth sets]] (def. \ref{SmoothSet}), [[formal smooth sets]] and [[super formal smooth sets]] (def. \ref{FormalSmoothSets})
as shown in the second and third row of the following diagram, such that

1. every [[pair]] of consecutive [[functors]] is an [[adjoint pair]] ([this Def.](geometry+of+physics+--+categories+and+toposes#AdjointFunctorsInTermsOfNaturalBijectionOfHomSets)), with the functor above being [[left adjoint]] and the functor below being [[right adjoint]]

1. on [[representables]] the top two functors on the left, the top two functors in the middle, and the top three functors on the right coincide with the corresponding functors between [[sites]] shown in the first row (from prop. \ref{SystemOfSites}):


<center>
<img src="https://ncatlab.org/nlab/files/AjunctionsForSuperCohesion.png" width="600">
</center>

In such a situation we also say that in the third row

1. the bottom four functors exhibit [[SuperFormalSmoothSet]] as a  [[cohesive topos]] ([this Def.](geometry+of+physics+--+categories+and+toposes#CohesiveTopos))

1. the middle four functors exhibit [[SuperFormalSmoothSet]] as [[differentially cohesive topos]] (elastic topos) relative to [[SmoothSet]] ([this Def.](https://ncatlab.org/nlab/show/geometry+of+physics+--+categories+and+toposes#DifferentialCohesion));

1. the top four functors exhibit $SuperFormalSmoothSet$ as _solid topos_ relative to [[FormalSmoothSet]] ([this Def.](geometry+of+physics+--+categories+and+toposes#SuperDifferentialCohesion))

=--

+-- {: .proof}
###### Proof

The system of functors between sites in Prop. \ref{SystemOfSites}



$$
  \array{
   { \text{}  \atop { \text{discrete} \atop {\text{geometry}} } }
   &&
   {\text{} \atop {\text{differential} \atop \text{geometry}}}
   &&
   {\text{formal} \atop {\text{differential} \atop {geometry}}}
   &&
   {\text{super} \atop {\text{differential} \atop \text{geometry}}}
   \\
   \\
   \ast
   &
   \array{
     \overset{\phantom{AA}\Pi\phantom{AA}}{\longleftarrow}
     \\
     \overset{\phantom{AA}Disc\phantom{AA}}{\hookrightarrow}
   }
   &
  CartSp
   &
   \array{
     \overset{\phantom{AA}\iota_{inf}\phantom{AA}}{\hookrightarrow}
     \\
     \overset{\phantom{AA}\Pi_{inf}\phantom{AA}}{\longleftarrow}
     \\
     \phantom{A}
     \\
     \phantom{A \atop A}
   }
   &
  FormalCartSp
  &
   \array{
     \overset{\phantom{AA}even\phantom{AA}}{\longleftarrow}
     \\
     \overset{\phantom{AA}\iota_{sup}\phantom{AA}}{\hookrightarrow}
     \\
     \overset{\phantom{AA}\Pi_{sup}\phantom{AA}}{\longleftarrow}
     \\
     \phantom{A}
     \\
     \phantom{A \atop A}
     \\
     \phantom{A \atop A}
   }
  &
  SuperFormalCartSp
  }
  \,.
$$

induces the claimed [[adjoint quadruples]] between [[presheaf toposes]] in the second row, by [[Kan extension]] ([this Example](geometry+of+physics+--+categories+and+toposes#KanExtensionOfAdjointPairIsAdjointQuadruple) in the chapter _[[geometry of physics -- categories and toposes|on categories and toposes]]_). 

That the [[adjoint quadruple]] on the left ([[corestriction|co-]])[[restriction|restricts]] to [[sheaves]], exhibiting [[SmoothSet]] as a [[cohesive topos]], is [this Prop.](geometry+of+physics+--+smooth+sets#SmoothSetsFormACohesiveTopos) in the chapter [[geometry of physics -- smooth sets|on smooth sets]].

For the other two [[adjoint quadruples]] the ([[corestriction|co-]])[[restriction|restricts]] to [[sheaves]] is trivial, since this concerns only the [[coverages]] along the infinitsimal directions in [[FormalCartSp]] and [[SuperFormalCartSp]], which are [[trivial coverage|trivial]] ([this Example](geometry+of+physics+--+categories+and+toposes#TrivialCoverage)), by definition.

This establishes the system of [[adjoint quadruples]] between [[sheaf toposes]] in the second row.

The diagram in the third row states that two extra adjoints to _composites_ of the functors appear. Here 

1. the [[right adjoint]] functor

   $$
     SmoothSet \longleftarrow SuperFormalSmoothSet
   $$ 

   exists as part of the [[adjoint quadruple]] which is induced ([this Example](geometry+of+physics+--+categories+and+toposes#KanExtensionOfAdjointPairIsAdjointQuadruple)) from the _[[composition|composite]]_ [[coreflective subcategory|coreflective inclusion]]

   $$
     CartSp
     \array{
       \overset{\phantom{A}\iota_{inf}\phantom{A}}{\hookrightarrow}
       \\
       \overset{\phantom{AA} \Pi_{inf} \phantom{AA}}{\longleftarrow} 
       \\
       \phantom{\overset{\phantom{AA} \Pi_{sup} \phantom{AA}}{\longleftarrow}}     
     }
     FormalCartSp
     \array{
       \overset{\phantom{A}\iota_{sup}\phantom{A}}{\hookrightarrow}
       \\
       \overset{\phantom{AA} \Pi_{sup} \phantom{AA}}{\longleftarrow} 
       \\
       \phantom{\overset{\phantom{AA} \overset{\rightrightarrows}{(-)} \phantom{AA}}{\longleftarrow}}     
     }
     SuperFormalCartSp
   $$

   and using that composites of adjoints are adjoint, and that adjoints are unique, when they exist ([this prop.](geometry+of+physics+--+categories+and+toposes#UniquenessOfAdjoints))

1. Notice that also [[SuperFormalCartSp]] is a [[cohesive site]]: since the [[coverage]] along the infinitesimal directions is [[trivial coverage|trivial]], while that along the finite directions is the same as that on [[CartSp]], this follows with the same [[proof]] as for [[CartSp]] ([this Prop.](geometry+of+physics+--+smooth+sets#SmoothSetsFormACohesiveTopos)). 

   Moreover, the [[composition|composite]] 

   $$
     Disc
     \;\colon\;
     Set 
       \hookrightarrow 
     SmoothSet 
       \hookrightarrow 
     FormalSmoothSet
       \hookrightarrow 
     SuperFormalSmoothSet
   $$

   from the second row above equals the functor 

   $$
     \array{
        Set 
          &\overset{Disc}{\longrightarrow}&
        SuperFormalSmoothSet
        \\
        S &\mapsto& const_S
     }
   $$

   which is part of the [[adjoint quadruple]] of the [[cohesion]] of $SuperFormalSmoothSet$ (via [that Prop.](geometry+of+physics+--+smooth+sets#SmoothSetsFormACohesiveTopos))): This is because all these inclusion functors are [[right adjoints]], and hence [[preserved limit|preserve]] the [[terminal object]] $\ast$ ([this Prop.](geometry+of+physics+--+categories+and+toposes#LeftAdjointFunctorPreservesEpi)), but also [[left adjoints]], and hence [[preserved limit]] [[coproducts]] ([this Prop.](geometry+of+physics+--+categories+and+toposes#AdjointsPreserveCoLimits)). This implies the claim because every [[set]] is a [[coproduct]] of [[generalized the|the]] [[singleton]], which is the [[terminal object]] in [[Set]]. 

   This implies, again by uniqueness of adjoints ([this Prop.](geometry+of+physics+--+categories+and+toposes#UniquenessOfAdjoints)) that the composite functor $Set\longleftarrow SuperFormalSmoothSet$ from the previous item is in fact the functor $\Gamma_{SuperFormalSmoothSet}$ from the [[cohesive topos]]-structure on [[SuperFormalSmoothSet]] and hence, finally, that there is the bottom right adjoint 

   $$
     coDisc \;\colon\; Set \overset{\phantom{AA}}{\hookrightarrow} SuperFormalSmoothSet
   $$ 

   as claimed.

Finally, that every second functor is a [[full subcategory]]  inclusion (a [[fully faithful functor]]) as shown follows because

1. left Kan extension along [[fully faithful functors]] is itself fully faithful ([this prop.](Kan+extension#LeftKanExtensionBasicProp));

1. in an [[adjoint triple]] the leftmost adjoint is [[fully faithful functor|fully faithful]] precisely if the rightmost adjoint is ([this prop.](adjoint+triple#FullyFaithful)).

=--

Proposition \ref{SuperSmoothSetsSystemOfAdjunctions} says that the basic operations on local model spaces,
such as

1. forming the underlying bosonic space,

1. forming the underlying formal bosonic space of bi-fermions,

1. forming the underlying reduced space

extend from local model spaces to the generalized spaces modeled on them,
while retaining their relation to each other and to the respective
inclusions, and such that yet further operations accompanying them are induced.

To record what all these operations are, it is useful to compose the
functors above in pairs, with one functor projecting down to the left, and the next one including back with either a left or right adjoint of the projection.

For example given a [[generalized space|generalized]] [[superspace]], then
applying the top-most functor in prop. \ref{SuperSmoothSetsSystemOfAdjunctions} to it
yields its underlying bi-fermionic formal smooth space, regarded as an object in [[FormalSmoothSet]]. But if we work in [[supergeometry]], then we want this result to be understood as a superspace again, one that just so happens to have no odd directions, so we re-include it by the inclusion right adjoint to the top projection. This composite operation of projection and re-embedding defines a _[[modal operator]]_ ([this Def.](geometry+of+physics+--+categories+and+toposes#ModalOperator)), on [[SuperFormalSmoothSet]], which we denote by

$$
  \overset{\rightrightarrows}{(-)}
  \;\coloneqq\;
  \iota_{sup} \circ even
  \;\colon\;
  SuperFormalSmoothSet
    \overset{\phantom{AAAA}}{\longrightarrow}
  SuperFormalSmoothSet
  \,.
$$

Similarly, composing the projection which is the left Kan extension of the underlying bosonic space operation with the canonical re-embedding yields an endofunctor that has the interpretation of sending any generalized superspace to its underlying generalized bosonic space

$$
  \overset{\rightsquigarrow}{(-)}
  \coloneqq
  \iota_{sup} \circ \Pi_{sup}
  \;\colon\;
  SuperFormalSmoothSet
    \longrightarrow
  SuperFormalSmoothSet
  \,.
$$

In fact, since these two [[endofunctors]] are obtained from the two possible composites in an [[adjoint triple]] whose middle functor is [[fully faithful functor|fully faithful]] -- corresponding to an  [[adjoint modality]] ([this Def.](geometry+of+physics+--+categories+and+toposes#AdjointModality)) --
it is immediate to see that:

1. $\overset{\rightsquigarrow}{(-)}$ has the structure of a [[comodal operator]]

1. $\overset{\rightrightarrows}{(-)}$ has the structure of an [[modal operator]]

1. together they form an [[adjoint modality]] $\overset{\rightrightarrows}{(-)} \dashv \overset{\rightsquigarrow}{(-)}$.

Moreover, by prop. \ref{SuperSmoothSetsSystemOfAdjunctions}, this adjoint triple between $SuperFormalSmoothSet$ and $FormalSmoothSet$ extends to an
[[adjoint quadruple]], there is yet one more [[endofunctor]] which is a further [[right adjoint]]  [[idempotent comonad]].
Later we will see that this further opration is related to the concept of "[[rheonomy]]" in supergravity, and therefore
we denote it by

$$
  Rh
  \;\coloneqq\;
  Disc_{sup} \circ \Pi_{sup}
  \;\colon\; SuperFormalSmoothSet \longrightarrow SuperFormalSmoothSet
  \,.
$$

But prop. \ref{SuperSmoothSetsSystemOfAdjunctions} says that there are yet further adjoints, however
these no longer go between $SuperFormalSmoothSet$ and $FormalSmoothSet$, but between the former and
$SmoothSet$ or even just between the former and $Set$. For instance there is the composite projection

$$
  SmoothSet \longleftarrow FormalSmoothSet \longleftarrow SuperFormalSmoothSet
$$

which first forms the bosonic underlying space, and then forms the reduced underlying space of what remains.
The total result of this operation is just plain reduction, removing all infinitesimal directions,
whether odd graded or even graded.
Therefore, the result of composing this operation with its right adjoint canonical re-embedding yields an endofunctor which
we should call

$$
  \Re
  \coloneqq
  \iota_{inf} \circ \Pi_{inf}
  \;\colon\;
  SuperFormalSmoothSet \longrightarrow SuperFormalSmoothSet
$$

and think of as the operation of reduction on generalized [[super formal smooth sets]].

Notice that [[reflective subcategory]] embeddings

$$
  \underoverset
   {\underset{i}{\hookrightarrow}}
   {\overset{L}{\longleftarrow}}
   {}
$$

are [[localizations]], in that first including an object and then projecting it back to the subcategory
is the identity operation $L \circ i \simeq id$; and analogously for a [[coreflective subcategory|coreflection]]
([this prop.](adjoint+functor#FullyFaithfulAndInvertibleAdjoints)).

In our situation this first of all means that all of the [[endofunctors]] above are idempotent, as already
mentioned. But next it implies that first applying a "deep" projection in the diagram in
prop. \ref{SuperSmoothSetsSystemOfAdjunctions}, and then applying a "more shallow" projection
with functors at the same vertical stage in the diagram does not change the result further.
For example there is a [[natural isomorphism]]

$$
  \overset{\rightsquigarrow}{\Re(X)}
    \simeq
  \Re(X)
$$

saying that if a space is reduced, then it has no infinitesimal directions whatsoever, in particular no odd-graded ones,
hence it is already bosonic.

We will denote this situation by an inclusion sign

$$
  \Re \;\lt\; \overset{\rightsquigarrow}{(-)}
$$

to be read "reduced implies bosonic". This is an example of the _[[preorder]] on [[modalities]]_ ([this Def.](geometry+of+physics+--+categories+and+toposes#PreorderOnModalities))

We may proceed this way with all the remaining functors in prop. \ref{SuperSmoothSetsSystemOfAdjunctions}, consecutively
turning them into [[endofunctors]] on $SuperFormalCartSp$ which are all related to each other by
[[adjunctions]] or by this inclusion relation of projection operators.

The result is a system of 9 endofunctors, or 12 if we inclue the [[bottom]] [[adjoint modality]] and the [[top]] [[adjoint modality]] ([this Example](geometry+of+physics+--+categories+and+toposes#InitialAndFinalAdjointModality)):

| $\phantom{A}$ [[shape modality]] $\phantom{A}$ | $\phantom{A}$ [[flat modality]] $\phantom{A}$ | $\phantom{A}$ [[sharp modality]] $\phantom{A}$ |
|--------------------|-------------------|--------------------|
|   $\phantom{A}$  $&#643; \;\coloneqq\; Disc \circ \Pi_0$  $\phantom{A}$ | $\phantom{A}$ $\flat \;\coloneqq\; Disc \circ \Gamma$ $\phantom{A}$  | $\phantom{A}$ $\sharp \;\coloneqq\; coDisc \circ \Gamma $ $\phantom{A}$  |
|   |    |   |
| $\phantom{A}$ [[reduction modality]] $\phantom{A}$ | $\phantom{A}$ [[infinitesimal shape modality]] $\phantom{A}$ | $\phantom{A}$ [[infinitesimal flat modality]] $\phantom{A}$ |
|   $\phantom{A}$  $\Re \;\coloneqq\; \iota_{inf} \circ \Pi_{inf}$  $\phantom{A}$ | $\phantom{A}$ $\Im \;\coloneqq\; Disc_{inf} \circ \Pi_{inf}$ $\phantom{A}$  | $\phantom{A}$ $ \& \;\coloneqq\; Disc_{inf} \circ \Gamma_{inf} $ $\phantom{A}$  |
{: style='margin:auto}

+-- {: .num_prop #ProgressionOfIdempotentEndofunctors}
###### Proposition
**(progression of [[adjoint modalities]] on [[SuperFormalSmoothSet]])**

We have a system of [[adjoint modalities]] ([this Def.](geometry+of+physics+--+categories+and+toposes#AdjointModality)) and their [[preordering]] ([this Def.](geometry+of+physics+--+categories+and+toposes#PreorderOnModalities)) on [[SuperFormalSmoothSet]] (Def. \ref{FormalSmoothSets}) that is induced (via [this Prop.](geometry+of+physics+--+categories+and+toposes#ModalOperatorsEquivalentToReflectiveSubcategories)) by the system of [[adjoint functors]] in Prop. \ref{SuperSmoothSetsSystemOfAdjunctions}, as follows:

\[
  \label{ProgressionOfModalitiesOnSuperFormalSmoothSet}
  \array{
    id &\dashv& id
    \\
    \vee &\vert& \vee
    \\
    \rightrightarrows &\dashv& \rightsquigarrow &\dashv& Rh
    \\
    && \vee &\backslash& \vee
    \\
    && \Re &\dashv& \Im &\dashv& \&
    \\
    && && \vee &\vert& \vee
    \\
    && && &#643; &\dashv&  \flat &\dashv& \sharp
    \\
    && && && \vee &/& \vee
    \\
    && && && \emptyset &\dashv& \ast
  }
\]

Moreover, the progression exhibits [[Aufhebung]] ([this Def.](geometry+of+physics+--+categories+and+toposes#Aufhebung), [this Remark](geometry+of+physics+--+categories+and+toposes#TrivialAufhebung)) at each stage, as indicated.

Finally, the [[rheonomy modality]]  is [[homotopy localization]] at $\mathbb{R}^{0\vert 1}$ (the [[superpoint]]) in the sense of [this Def.](geometry+of+physics+--+categories+and+toposes#HomotopyLocalizationOn1Categories):

$$
  Rh \simeq \bigcirc\!\!\!\!\!\!\!\!\mathbb{R}^{0\vert 1}
  \,.
$$


=--


+-- {: .proof}
###### Proof

The progression of modalities follows with Prop. \ref{SuperSmoothSetsSystemOfAdjunctions} by [this Prop.](geometry+of+physics+--+categories+and+toposes#ProgressionOfModalitiesOnSolidTopos).

The right [[Aufhebung]]  at the first stage says that $\sharp \emptyset \simeq \emptyset$, which means equivalently that for each $\mathbb{R}^{n\vert q} \times \mathbb{D}_V \in $ [[SuperFormalCartSp]] we have

$$
  Hom(\mathbb{R}^{n\vert q} \times \mathbb{D}_V, \sharp \emptyset)
  \simeq
  \emptyset
$$

But by the $\flat \dashv \sharp$ [[adjunction]] hom-isomorphism ([here](geometry+of+physics+--+categories+and+toposes#eq:HomIsomorphismForAdjointFunctors)) and the fact that $\flat X = Disc X(\ast)$ (by the proof of [this Prop.](geometry+of+physics+--+categories+and+toposes#CategoriesOfSheavesOnCohesiveSiteIsCohesive)) and that $\mathbb{R}^{n\vert q} \times \mathbb{D}_V(\ast) \neq \emptyset$ we have indeed

$$
  Hom(\mathbb{R}^{n\vert q} \times \mathbb{D}_V, \sharp \emptyset)
  \simeq
  Hom( \flat \mathbb{R}^{n\vert q} \times \mathbb{D}_V , \emptyset)
  =
  \emptyset
  \,.
$$

The left [[Aufhebung]] at the third stage says that 

$$
  \rightsquigarrow \Im \simeq \Im
  \,.
$$

This means equivalenty that for each $X \in SuperFormalSmoothSet$ and $\mathbb{R}^{n\vert q} \times \mathbb{D}_V \in SuperFormalCartSp$ we have

$$
  Hom(\mathbb{R}^{n\vert q} \times \mathbb{D}_V, \overset{\rightsquigarrow}{\Im X})
  \simeq
  Hom(\mathbb{R}^{n\vert q} \times \mathbb{D}_V, \overset{}{\Im X})
$$

Again by the adjunction isomorphisms we verify:

$$
  \array{
    Hom(\mathbb{R}^{n\vert q} \times \mathbb{D}_V, \overset{\rightsquigarrow}{\Im X})
    & \simeq
    Hom\left(
      \overset{\rightrightarrows}{\mathbb{R}^{n\vert q} \times \mathbb{D}_V}, \overset{}{\Im X}\right)    
    \\
    & \simeq
    Hom\left(
      \overset{\rightrightarrows}{\mathbb{R}^{n\vert q} \times \mathbb{D}_V},
      \overset{}{\Im X}
    \right) 
    \\
    & 
    Hom\left(
      \Re\left(\overset{\rightrightarrows}{\mathbb{R}^{n\vert q} \times \mathbb{D}_V}\right),
      \overset{}{ X}
    \right) 
    \\
    & \simeq
    Hom\left(
      \Re\left(\overset{}{\mathbb{R}^{n\vert q} \times \mathbb{D}_V}\right),
      \overset{}{ X}
    \right) 
    \\
    & \simeq
    Hom\left(
      \overset{}{\mathbb{R}^{n\vert q} \times \mathbb{D}_V},
      \overset{}{ \Im X}
    \right) 
  }   
$$

Here we used that on representables 

$$
  \Re \overset{\rightrightarrows}{(-)} \simeq \Re(-)
  \,,
$$

which holds by direct inspection: it says that the odd-graded elements in a [[supercommutative superalgebra]] are all nilpotent.

Finally for the equivalence
$$
  Rh \simeq \bigcirc\!\!\!\!\!\!\!\!\mathbb{R}^{0\vert 1}
$$

the proof is directly analogous to that of the analogous statement in the chapter _[[geometry of physics -- smooth sets|on smooth sets]]_,  [this Prop](geometry+of+physics+--+smooth+sets#ShapeModalityOnSmoothSetsIsR1Localization):

As in that proof, the $\mathbb{R}^{0\vert 1}$-[[local objects]] among all [[super formal smooth sets]] are equivalently those which are [[local objects]] with respect to the following [[small set]] of morphisms:

$$
  \left\{
    \mathbb{R}^{n} \times \mathbb{D}_V \times \mathbb{R}^{0\vert q + 1}
    \longrightarrow
    \mathbb{R}^{n} \times \mathbb{D}_V \times \mathbb{R}^{0\vert q}
  \right\}
  \,.
$$

By [[induction]] over $q \in \mathbb{N}$, these are equivalently the objects which are local with respect to the following small set:

$$
  \left\{
    \mathbb{R}^{n} \times \mathbb{D}_V \times \mathbb{R}^{0\vert q}
    \longrightarrow
    \mathbb{R}^{n} \times \mathbb{D}_V
  \right\}
  \,.
$$

But these are manifestly the objects $A \in SuperFormalSmoothSet$ which are in the image of $Disc_{sup}$:

$$
  \begin{aligned}
    Hom\left(
      \mathbb{R}^{n} \times \mathbb{D}_V \times \mathbb{R}^{0\vert q}, 
      Disc(B)
    \right)
    & \simeq
  Hom\left(
    \Pi_{sup}(\mathbb{R}^{n} \times \mathbb{D}_V \times \mathbb{R}^{0\vert q}), B
    \right)
    \\
    & \simeq
    Hom\left(\mathbb{R}^{n} \times \mathbb{D}_V), B\right)
  \end{aligned}  
$$


=--


Sometimes it is illuminating to re-arrange the diagram in Prop. \ref{ProgressionOfIdempotentEndofunctors} equivalently as follows. Here we label each
projection operator by the property of superspaces that it "projects out".

$$
  \array{
    && id &\dashv& id
    \\
    && \vee && \vee
    \\
    &\stackrel{fermionic}{}& \rightrightarrows &\dashv& \rightsquigarrow & \stackrel{bosonic}{}
    \\
    && \bot &\stackrel{solidity}{}& \bot
    \\
    &\stackrel{bosonic}{} & \rightsquigarrow &\dashv& Rh & \stackrel{rheonomic}{}
    \\
    && \vee && \vee
    \\
    &\stackrel{reduced}{} & \Re &\dashv& \Im & \stackrel{infinitesimal}{}
    \\
    && \bot &\stackrel{elasticity}{}& \bot
    \\
    &\stackrel{infinitesimal}{}& \Im &\dashv& \& & \stackrel{\text{&#233;tale}}{}
    \\
    && \vee && \vee
    \\
    &\stackrel{connected}{}& &#643; &\dashv& \flat & \stackrel{disconnected}{}
    \\
    && \bot &\stackrel{cohesion}{}& \bot &&
    \\
    &\stackrel{discrete}{}& \flat &\dashv& \sharp & \stackrel{continuous}{}
    \\
    && \vee && \vee
    \\
    && \emptyset &\dashv& \ast
  }
$$



[Below](#Supermanifolds) we use these operations to identify within all generalized superspaces those that are [[supermanifolds]].
But first we consider now some general important constructions of [[super formal smooth sets]], such as  [[mapping spaces]].

$\,$



## Super mapping spaces
 {#SuperMappingSpaces}

We now discuss [[mapping spaces]] in [[supergeometry]]. These are interesting in two ways:

1. for the theory -- mapping spaces nicely exhibit the usage and the power of the [[functor of points]] perspective (remark \ref{ASheafAsASpace});

1. for applications -- in [[physics]] a [[superfield]] is really a [[generalized element]] of a mapping space, and hence  the [[phase spaces]] of interest in [[physics]] are [[mapping spaces]] (in the generality of spaces of [[spaces of sections]], namely of a [[field bundle]]).

The key idea is that [[sets]] of functions between sets have the following [[universal property]]:

+-- {: .num_example #FunctionSet}
###### Example

Let $X,Y \in $ [[Set]] be two [[sets]], then the set

$$
  Y^X \coloneqq \{X \to Y\}
$$

of [[functions]] from $X$ to $Y$ is characterized by the fact that for $Z \in Set$ any further set,
there is a [[natural bijection]]

$$
  Hom( Z \times X, Y ) \stackrel{\simeq}{\longrightarrow} Hom(Z, Y^X)
$$

between functions of two [[variables]] into $Y$ and functions of one variable into $Y^X$. This is given by sending
any function $f(-,-)$ of two variables to the function $\tilde f$ which sends any $z$ to the function
$x \mapsto f(z,x)$. Hence this simply reinterprets "taking two arguments at once" by "taking two arguments consecutively".

=--

It is immediate how to generalize example \ref{FunctionSet}:

+-- {: .num_defn #InternalHom}
###### Definition
**([[mapping space]]/[[internal hom]])**

Let $\mathcal{C}$ be a [[category]] with [[Cartesian products]] of its [[objects]],
hence a [[cartesian monoidal category]]. Then an [[internal hom]]-functor for $\mathcal{C}$
is, if it exists, a functor of the form

$$
  [-,-] \;\colon\; \mathcal{C}^{op} \times \mathcal{C} \longrightarrow \mathcal{C}
$$

such that there is a [[natural bijection]] between [[hom sets]] of the form

$$
  Hom_{\mathcal{C}}(Z \times X, Y)
  \simeq
  Hom_{\mathcal{C}}(Z, [X,Y])
$$

for all [[objects]] $X,Y,Z \in \mathcal{C}$.

=--

The class of examples that we are interested in is the following:

+-- {: .num_prop #SheavesHomInternal}
###### Proposition

Let $\mathcal{C} = Sh(\mathcal{S})$ be a [[category of sheaves]] over some [[site]] $\mathcal{S}$.

Then the [[Cartesian product]] between any two sheaves $X,Y \in Sh(\mathcal{C})$ exists and
is given objectwise by the [[Cartesian product]] of sets:

$$
  (X \times Y) \;\colon\; U \mapsto X(U) \times Y(U)
$$

for $U \in \mathcal{S}$.

Moreover, an [[internal hom]]-functor according to def. \ref{InternalHom} exists ("generalized [[mapping space]]").
It sends any two [[sheaves]] $X,Y \in Sh(\mathcal{S})$ to the sheaf

$$
  [X,Y] \;\colon\; \mathcal{S}^{op} \longrightarrow Set
$$

given by

$$
  U \mapsto Hom_{Sh(\mathcal{S})}( X \times y(U), Y )
  \,,
$$

where $y \colon \mathcal{S} \hookrightarrow Sh(\mathcal{S})$ is the [[Yoneda embedding]].

=--

For the **proof** see at _[[closed monoidal structure on presheaves]]_.

Notice how prop. \ref{SheavesHomInternal} expresses an intuitively most obvious statement: Applied to
geometric sheaf toposes such
as [[smooth set|SmoothSet]] or [[super formal smooth set|SuperFormalSmoothSet]] (def. \ref{FormalSmoothSets}) it says that a
$U$-parameterized smooth family of points in a [[mapping space]] $[X,Y]$ is a smooth map of the form
$X \times U \to Y$, hence a family of smooth functions $X \to Y$ which is smoothly parameterized by $U$.

The following shows formally that the concept of [[internal homs]] in the [[topos]] of [[generalized smooth spaces]]
does generalize the traditional concept of smooth [[mapping spaces]]:

+-- {: .num_example #SmoothManifoldsMappingSpace}
###### Example

Let $\Sigma$ be a [[compact topological space|compact]] [[smooth manifold]] and let $X$ be any [[smooth manifold]].
Then the set of [[smooth functions]] $C^\infty(\Sigma,X)$ carries the structure of an
[[infinite-dimensional manifold|infinite dimensional]] (in general) [[Fréchet manifold]] $Maps(\Sigma,X)_{Frechet}$.
Under the embedding $i \colon FrechetMfd \hookrightarrow SmoothSet$ of prop. \ref{SmoothSetsContainSmoothManifolds}
this coincides with  [[internal hom]] $[\Sigma,X]$ formed in $SmoothSet$ according to prop. \ref{SheavesHomInternal}:

$$
  [\Sigma, X] \simeq  i(Maps(\Sigma, X)_{Frechet})
  \,.
$$

In particular for instance the smooth [[loop space]] of a smooth manifold $X$ is simply the internal hom $[S^1,X]$.


=--

A **proof** is given in  [Waldorf 09, lemma A.1.7](diffeological+space#Waldorf09).

But in the topos [[super formal smooth set|SuperFormalSmoothSet]] (def. \ref{FormalSmoothSets}) we have also mapping spaces much more general than the traditional ones of
example \ref{SmoothManifoldsMappingSpace}. We now look at some examples of these.


+-- {: .num_example #CorepresentingTangentSpace}
###### Example

Let

$$
  \mathbb{D}^1 = Spec(\mathbb{R}[\epsilon]/(\epsilon^2))
    \in
  InfPoint \hookrightarrow SuperFomalSmoothSet
$$

be the [[formal dual]] of the [[ring of dual numbers]] (example \ref{EvenPartOfDimTwoSuperpoint}).
Observe that there is a unique morphism of the form $\ast \to \mathbb{D}^1$, picking the base point.

Then for

$$
  X \in SmoothMfd \hookrightarrow SuperFormalSmoothSet
$$

a [[smooth manifold]], regarded as a [[super formal smooth set]] ([this Prop.](geometry+of+physics+--+smooth sets#InclusionOfSmoothManifoldsIntoSmoothSets)),
the [[internal hom]] out of $\mathbb{D}^1$ with this basepoint is the smooth [[tangent bundle]] of $X$ (again under the embedding of [this Prop.](geometry+of+physics+--+smooth sets#InclusionOfSmoothManifoldsIntoSmoothSets)):

$$
  \array{
    [\mathbb{D}^1, X] &\simeq& T X
    \\
    {}^{\mathllap{[\ast \to \mathbb{D}^1,X]}}\downarrow && \downarrow
    \\
    [\ast,\X] &\simeq& X
  }
  \,.
$$

=--


+-- {: .proof}
###### Proof

By prop. \ref{SheavesHomInternal} the rule for the [[smooth set]] $[\mathbb{D}^1,X]$ is

$$
  \mathbb{R}^n \mapsto Hom_{SmoothSet}( \mathbb{R}^n \times \mathbb{D}^1, X )
  \,.
$$

By prop. \ref{HomsOutOfFirstOrderInfinitesimalLine}, the set on the right is naturally identified with the set of
of smoothly $\mathbb{R}^n$-parameterized families of [[tangent vectors]] in $X$. But this is the set that
$T X$, regarded as a smooth set, assigns to $\mathbb{R}^n$.

Moreover, looking at the proof of prop. \ref{HomsOutOfFirstOrderInfinitesimalLine} it is immediate that composing
a morphism

$$
  \mathbb{D}^1 \to X
$$

representing some tangent vector in $X$ with the global point inclusion of $\mathbb{D}^1$ yields the point in $X$

$$
  \ast \to \mathbb{D}^1 \to X
$$

at which this tangent vector is based. This shows that the vertical map in the above claim is indeed the projection from the
[[tangent bundle]] to the base manifold.

=--

Example \ref{CorepresentingTangentSpace} is a key observation that motivated the development of
[[synthetic differential geometry]] ([[Toposes of laws of motion|Lawvere 97]]).

The following is the supergeometric analog of this situation:


+-- {: .num_example #MappingSpaceOddTangentBundle}
###### Example
**([[odd tangent bundle]] as [[mapping space]])**

Let $X$ be any [[smooth manifold]]. Then the [[internal hom]] in $SuperFormalSmoothSet$ out of the
[[superpoint]] $\mathbb{R}^{0\vert 1}$ into $X$, according to prop. \ref{SheavesHomInternal},
is the [[odd tangent bundle]] from def. \ref{OddTangentBundle} $\Pi T X$:

$$
  \array{
    [\mathbb{R}^{0\vert 1}, X] &\simeq& \Pi T X
    \\
    {}^{\mathllap{[\ast \to \mathbb{R}^{0\vert 1},X]}}\downarrow && \downarrow
    \\
    [\ast,\X] &\simeq& X
  }
  \,.
$$


=--

+-- {: .proof}
###### Proof

Let $\mathbb{R}^n$ be a [[bosonic object|bosonic]] [[Cartesian space]].
By prop. \ref{SheavesHomInternal} the set of plots of the smooth set $[\mathbb{R}^{0\vert 1}, X]$ on this test space is

$$
  [\mathbb{R}^{0\vert 1},X](\mathbb{R}^n)
  =
  Hom_{SuperFormalSmoothSet}( \mathbb{R}^{n\vert 1}, X )
  \,.
$$

But since $X$ is bosonic (an ordinary smooth manifold), this is equivalently just

$$
  [\mathbb{R}^{0\vert 1},X](\mathbb{R}^n)
  =
  Hom_{SuperFormalSmoothSet}( \mathbb{R}^{n}, X )
  \simeq
  X(\mathbb{R}^n)
  \,,
$$

which shows that the bosonic super smooth set underlying $[\mathbb{R}^{0\vert 1},X]$ is just $X$ itself.

But then consider probes parameterized by the [[superpoint]] $\mathbb{R}^{0\vert 1}$:

$$
  \begin{aligned}
    [\mathbb{R}^{0\vert 1},X](\mathbb{R}^{n\vert 1})
    & \simeq
    Hom( \mathbb{R}^{n\vert 2}, X )
    \\
    & \simeq
    Hom( \mathbb{R}^{n\vert 2}, \overset{\rightsquigarrow}{X} )
    \\
    & \simeq
    Hom(  \overset{\rightrightarrows}{\mathbb{R}^{n \vert 2}}, X )
    \\
    & \simeq
    Hom(  \mathbb{R}^n \times \mathbb{D}^1 , X )
    \\
    & \simeq
    Hom(\mathbb{R}^n, T X)
  \end{aligned}
  \,,
$$

where we used the [[adjunction]] $\rightrightarrows \dashv \rightsquigarrow$ from prop. \ref{SuperSmoothSetsSystemOfAdjunctions}, Prop. \ref{ProgressionOfIdempotentEndofunctors}, then example \ref{EvenPartOfDimTwoSuperpoint} and finally example \ref{CorepresentingTangentSpace}.

=--


Notice the curious difference between the bosonic and the odd-graded version of the [[synthetic tangent bundle]] as seen by its [[algebra of functions]]

* $[[\mathbb{D}^1, X], \mathbb{R}] \;\simeq\; C^\infty(T X)$

* $[[\mathbb{R}^{0\vert 1}, X], \mathbb{R}] \simeq \Omega^\bullet(X)$

In the first case the, smooth functions on the [[tangent bundle]] $T X$ do not know about the linear structure on [[fibers]]. But in the second case, they do: the [[differential forms]] in the second case appear as the sub-space of that of all smooth functions on those which are graded [[polynomials]] (over the algebra of smooth functions on $X$) in fiber-wise _[[linear functions]]_.

$\,$


More generally, this is the concept if _[[superfields]]_ as used in the [[physics]] literature:

+-- {: .num_example #Superfields}
###### Example
**([[superfields]])**

Let $X$ be a [[supermanifold]] (for instance a [[super spacetime]]) and consider
the super-[[mapping space]] (def. \ref{InternalHom}) $[X,\mathbb{R}]$ (or $[X,\mathbb{C}]$) of real (or complex)
valued functions on $X$ ("[[scalar fields]]"). We may
understand the [[generalized elements]] of this superspace via its [[functor of points]] which,
via prop. \ref{SheavesHomInternal}, is given by the assignment

$$
  \begin{aligned}
    \mathbb{R}^{0\vert q}
      & \mapsto
    Hom( X \times \mathbb{R}^{0\vert q}, \mathbb{R} )
    \\
    &
      \simeq
    C^\infty(X \times \mathbb{R}^{0\vert q})_{even}
    \\
    &
      \simeq
    \left( C^\infty(X) \otimes_{\mathbb{R}} \wedge^\bullet \langle \theta_1, \cdots, \theta_q\rangle\right)_{even}
  \end{aligned}
  \,.
$$

Here in the first line on the right we have the set of maps of supermanifolds of the form $X \times \mathbb{R}^{0\vert q} \to \mathbb{R}$,
which, by the [[Yoneda lemma]], is equivalently just the even subalgebra of the super-algebra of functions
on $X \times \mathbb{R}^{0\vert q}$, which finally is equivalently the even elements in the
[[tensor product]] of the super-algebra of functions on $X$ with the [[Grassmann algebra]] on $q$ odd generators
$\theta_i$.

Now an element in this tensor product is of the form

$$
  f
  +
  \underoverset{i = 1}{q}{\sum}
  g_i \theta_i
  +
  \underoverset{i,j = 1}{q}{\sum}
    f_{i j} \theta_i \theta_j
  +
  \underoverset{i,j,k = 1}{q}{\sum}
  g_{i j k} \theta_i \theta_j \theta_j
  +
  \cdots
$$

for any  $f_{\cdots} \in C^\infty(X)_{even}$ and $g_{\cdots} \in C^\infty(X)_{odd}$.

(Notice that here if $X$ is of superdimension $(d_X,q_X)$, then this expansion becomes redundant for
$q \gt q_X$: The [[functor of points]] provides an arbitrary supply of auxiliary Grassmann coordinates
$\theta$, only some of which will typically be of non-redundant use for any given superspace.)

In [[physics]], such a [[linear combination]] of even and odd component functions multipled with
Grassmann algebra elements to yield a homogeneously graded sum is called a _[[superfield]]_.

In order to make sense of this, some physics textbooks (e.g. [[Bryce DeWitt|de Witt]] 92) posit a single "infinite dimensional Grassmann algebra"
from which to draw the elements $\theta_i$. This approach has its pitfalls [Sachse 08, section 5.2](#Sachse08).
The [[functorial geometry]] perspecive (remark \ref{ASheafAsASpace}) fixes this: the "arbitrary supply"
of Grassmann variables is encoded by saying that

1. for each finite dimensional Grassmann algebra $\wedge^\bullet \langle \theta_1, \cdots, \theta_q\rangle = C^\infty(\mathbb{R}^{0\vert q})$
   superfields have an expansion in terms of the generators $\theta_i$;

1. these expressions are _covariant_ with respect to change of Grassmann coordinates $\mathbb{R}^{0\vert q} \to \mathbb{R}^{0\vert q'}$.

There are of course the evident generalizations of the scalar valued superfields along the same lines.
In general there is a (super-)[[fiber bundle]] $E \overset{\pi}{\to} X$ over ([[super spacetime|super]]) [[spacetime]] $X$
called the (super)-[[field bundle]] such that a field on $X$ is a [[section]] of the field bundle
(see also at _[[fiber bundles in physics]]_). The super-space of sections of $E$ is the following
[[fiber product]] of the [[mapping space]]

$$
  \Gamma_X(E)
    \;\coloneqq\;
  [X,E] \underset{[X,X]}{\times} \{id_X\}
  \,,
$$

i.e. the super-space with the [[universal property]] that it makes the follwing [[commuting square|square commute]]:

$$
  \array{
    \Gamma_X(E) &\longrightarrow& [X,E]
    \\
    \downarrow && \downarrow^{\mathrlap{X,\pi}}
    \\
    \{id_X\} &\hookrightarrow& [X,X]
  }
  \,.
$$

Then a [[superfield]] with values in $E$ is a [[generalized element]] of $\Gamma_X(E)$. By the
[[functorial geometry]]this means that field is over every
superpoint $\mathbb{R}^{0\vert q}$ a homomorphism $\psi \colon X \times \mathbb{R}^{0\vert q}$
such that

$$
  \array{
    && E
    \\
    & {}^{\mathllap{\psi}}\nearrow & \downarrow^{\mathrlap{\pi}}
    \\
    X \times \mathbb{R}^{0 \vert q}
    &\underset{pr_1}{\longrightarrow}&
    X
  }
  \,.
$$

In a typical example $X$ is an ordinary [[smooth manifold]] with [[spin structure]] and $E = \Pi S$
is the odd version (according to example \ref{OddTangentBundle}) of a [[spinor bundle]] on $X$.

Then an element of $[X,\Pi S]$ is

1. over $\mathbb{R}^{0\vert 0}$ no information;

1. over $\mathbb{R}^{0 \vert 1}$ an element $\psi \theta$ with $\psi \in \Gamma_X(S)$ an ordinary section of the
   [[spinor bundle]] (hence a [[spinor field]]).

and so on.

This may be combined: For example if $\underline{\mathbb{C}} \oplus_X \Pi $ is the [[direct sum of vector bundles]] of the
[[trivial vector bundle|trivial]] [[complex line bundle]] with an odd [[spinor bundle]], then a [[generalized element]]
of $\Gamma_X\left(\underline{\mathbb{C}} \oplus_X \Pi S \right)$ is over $\mathbb{R}^{0\vert 1}$ of the form

$$
  \sigma = \phi + \psi \theta
  \,,
$$

where $\phi$ is a complex-vaued [[scalar field]] and $\psi$ again a section of the spinor bundle.

This way [[bosonic fields]] and [[fermionic fields]] may be combined into a singe [[superfield]]
(see also at _[[super multiplet]]_).

=--






## Supermanifolds
 {#Supermanifolds}

We now define and then discuss the analog of [[smooth manifolds]] in [[supergeometry]] -- [[supermanifolds]].
In the spirit of the entire presentation, we do so by applying a [[general abstract]] definition of
"[[V-manifold]]" or "$V$-scheme" locally modeled on any given kind of model spaces to the special
case where the local model spaces are [[super Cartesian spaces]] as discussed above.
This general method is also discussed at _[[geometry of physics -- manifolds and orbifolds]]_,
but we recall the relevant points below.

Recall the [[adjoint pair]] of [[endofunctors]]

$$
  (\Re \dashv \Im)
   \;\colon\;
  SuperFormalSmoothSet
    \longrightarrow
  SuperFormalSmoothSet
$$

from Prop. \ref{ProgressionOfIdempotentEndofunctors}. By prop. \ref{SuperSmoothSetsSystemOfAdjunctions} and prop. \ref{CartSpCoreflectiveInclusion} we know that $\Re$ sends a (formal) [[super Cartesian space]] to its underlying
reduced ordinary [[Cartesian space]]. For instance

$$
  \Re(\mathbb{R}^{p\vert q}) \simeq \mathbb{R}^p
$$

and generally

$$
  \Re(\mathbb{R}^n \times \mathbb{D}) \simeq \mathbb{D}^n
$$

for $\mathbb{D}$ any [[infinitesimally thickened point|infinitesimally thickened superpoint]].

This is enough to find what its [[right adjoint]] operation $\Im$ is doing:

+-- {: .num_prop #ImAction}
###### Proposition

For $X \in SuperFormalSmoothSet$ (def. \ref{FormalSmoothSets}), then $\Im X$ is the [[super formal smooth set]] whose [[functor of points]] is given by

$$
  \Im X
  \;\colon\;
    \mathbb{R}^n \times \mathbb{D}
  \mapsto
  X(\mathbb{R}^n)
$$

where $n \in \mathbb{N}$ and for $\mathbb{D}$ any [[infinitesimally thickened point|infinitesimally thickened superpoint]].

=--

+-- {: .proof}
###### Proof

By applying the [[Yoneda lemma]], the [[natural bijection]] between [[hom-sets]] that
characterizes the [[adjoint pair]] $\Re \dashv \Im$ and using the characterization of $\Re$ we
get the following sequence of [[natural isomorphisms]]:

$$
  \begin{aligned}
    (\Im X)(\mathbb{R}^n \times \mathbb{D})
    & \simeq
    Hom( \mathbb{R}^n \times \mathbb{D} , \Im X)
    \\
    & \simeq
    Hom(\Re(\mathbb{R}^n \times \mathbb{D}), X)
    \\
    & \simeq
    Hom(\mathbb{R}^n, X)
    \\
    & \simeq
    X(\mathbb{R}^n)
  \end{aligned}
  \,.
$$

=--

Proposition \ref{ImAction} means that for $X$ for instance an ordinary [[smooth manifold]]
(regarded as a [[super formal smooth set]] via prop. \ref{SmoothSetsContainSmoothManifolds})
then $\Im X$ is a rather exotic kind of [[generalized smooth space]]: it has the same finite smooth curves and other
finite smooth shapes as $X$ does, but every _infinitesimal_ curve or shape inside it is necessarily constant.
A good way to think about this (which is also the precise way to think about it, if we speak in the [[internal language]]
of the [[sheaf topos]]) is that $\Im X$ is the result obtained from $X$ by **identifying all infinitesimally close points**
with each other. In [[algebraic geometry]] this construction is often known as forming the _[[de Rham shape]]_ of $X$
([Simpson 96](#de+Rham+space#Simpson96)). Here we will say **[[infinitesimal shape]]**.

Another useful perspective on $\Im X$ is the following:

+-- {: .num_defn #DiskBundle}
###### Definition
**([[infinitesimal disk bundle]])**

For $X \in SuperFormalSmoothSet$ (def. \ref{FormalSmoothSets}) then we say that its
[[infinitesimal disk bundle]] $T^\infty X$ is the left vertical morphism in the following [[pullback]] diagram

$$
  \array{
    T^\infty X &\longrightarrow& X
    \\
    {}^{\mathllap{p}}\downarrow &\stackrel{(pb)}{}& \downarrow^{\mathrlap{\eta_X}}
    \\
    X &\underset{\eta_X}{\longrightarrow}& \Im X
  }
  \,.
$$

Moreover, for $x \colon \ast \to X$ any [[global point]] of $X$, then
we say that the [[formal disk]] in $X$ at $x$ is the [[fiber]] of the infinitesimal disk bundle
over that point

$$
  \array{
    \mathbb{D}_x &\longrightarrow& T^\infty X &\longrightarrow& X
    \\
    \downarrow &\stackrel{(pb)}{}& {}^{\mathllap{p}}\downarrow &\stackrel{(pb)}{}& \downarrow^{\mathrlap{\eta_X}}
    \\
    \ast &\underset{x}{\longrightarrow}& X &\underset{\eta_X}{\longrightarrow}& \Im X
  }
  \,.
$$



=--



+-- {: .num_defn #LocalDiffeomorphisms}
###### Definition
**([[formally étale morphism]])**

Given $X,Y\in SuperFormalSmoothSet$ then a morphism $f \;\colon\; X\longrightarrow Y$ is called a _[[formally étale morphism]]_ if its
[[natural transformation|naturality square]] of the [[infinitesimal shape modality]] (prop. \ref{ImAction})

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

We often indicate that a morphism satisfies this condition by labeling it "et" , hence

$$
  \array{
    X &&&& X &\longrightarrow& \Im X
    \\
    {}^{\mathllap{f}}\downarrow^{\mathrlap{et}} &&\Leftrightarrow&& {}^{\mathllap{f}}\downarrow &\stackrel{(pb)}{}& \downarrow^{\mathrlap{\Im f}}
    \\
    Y &&&& Y &\longrightarrow& \Im Y
  }
  \,.
$$


=--

We unwind definition \ref{LocalDiffeomorphisms} a little:

+-- {: .num_remark #FormallyEtaleUnwinding}
###### Remark

Let $\mathbb{D}$ be an [[infinitesimally thickened point]]. This means that its reduction is the actual point,
$\Re \mathbb{D} \simeq \ast$. By the [[adjunction]] $\Re \dashv \Im$ from Prop. \ref{ProgressionOfIdempotentEndofunctors}
it follows that the image of the naturality square in def. \ref{LocalDiffeomorphisms} under forming the
[[internal hom]] (def. \ref{InternalHom}) out of $\mathbb{D}$ is

$$
  \array{
    X^{\mathbb{D}} &\longrightarrow& X
    \\
    \downarrow^{\mathrlap{f^\mathbb{D}}} && \downarrow^f
    \\
    Y^{\mathbb{D}} &\longrightarrow& Y
  }
$$

Since the internal hom preserves [[limits]] in its second argument (being [[right adjoint]] to $\mathbb{D} \times (-)$)
this is a [[pullback]] square if $f$ is a [[formally étale morphism]] according to def. \ref{LocalDiffeomorphisms}.
In this form the condition appears in [Yetter 88, def. 3.3.1](#Yetter88).

If here we specify $\mathbb{D} = Spec(\mathbb{R}[\epsilon]/\epsilon^2)$ to be the [[formal dual]] of the [[ring of dual numbers]],
then $X^{\mathbb{D}}$, $Y^{\mathbb{D}}$ are the respective [[tangent bundles]] by example \ref{CorepresentingTangentSpace}.
Hence in this case the condition that $f$ is a [[formally étale morphism]] according to def. \ref{LocalDiffeomorphisms}
implies that the square

$$
  \array{
    T X &\longrightarrow& X
    \\
    \downarrow^{\mathrlap{T f}} && \downarrow^{\mathrlap{f}}
    \\
    T Y &\longrightarrow& Y
  }
$$

is a pullback square. For $X,Y$ ordinary smooth manifolds via prop. \ref{SmoothSetsContainSmoothManifolds}, this condition
is the traditional definition that $f$ be a [[local diffeomorphism]].

=--

+-- {: .num_prop}
###### Proposition

For $X,Y \in SuperFormalSmoothSet$ two ordinary [[smooth manifolds]] via prop. \ref{SmoothSetsContainSmoothManifolds}, then
a morphism between them is a [[formally étale morphism]] according to def. \ref{LocalDiffeomorphisms}
precisely if it is a [[local diffeomorphism]] in the traditional sense.

=--

+-- {: .proof}
###### Proof

By remark \ref{FormallyEtaleUnwinding} the condition of
def. \ref{LocalDiffeomorphisms} on morphisms between smooth manifolds is equivalent
to the traditional condition of being locally diffeo already when seen just under
the internal hom out of $Spec(\mathbb{R}[\epsilon](\epsilon^2))$.

But, as the name suggests, a [[local diffeomorphism]] of smooth manifolds is in particular
also a [[local homeomorphism]]. This means that around each point of $X$ there is
actually an [[open neighbourhood]] such that $f$ restricts to a [[diffeomorphism]]
on that neighbourhood. This implies that the full condition in def. \ref{LocalDiffeomorphisms}
holds, by an argument as in example \ref{ProjectioonOutOfCoproductIsFormllyEtale}.

=--

+-- {: .num_example #ProjectioonOutOfCoproductIsFormllyEtale}
###### Example

For $V \in SuperFormalSmoothSet$ be given (def. \ref{FormalSmoothSets}) and for $I$ any set,
then the canonical morphism out of the [[coproduct]] ([[disjoint union]]) of $I$ copies of $V$
to itself is a local diffeomorphism according to def. \ref{LocalDiffeomorphisms}:

$$
  \array{
    \underset{i \in I}{\coprod} V
    \\
    {}^{\mathllap{et}}\downarrow^{\mathrlap{(id_i)_{i \in I}}}
    \\
    V
  }
$$

=--


+-- {: .proof}
###### Proof

Since $\Im$ is a [[left adjoint]] by prop. \ref{SuperSmoothSetsSystemOfAdjunctions}, Prop. \ref{ProgressionOfIdempotentEndofunctors},
it preserves all [[colimits]] and hence in particular [[coproducts]], hence the image of the morphism under
$\Im$ is

$$
  \array{
    \underset{i \in I}{\coprod} \Im V
    \\
    {}^{\mathllap{et}}\downarrow^{\mathrlap{(id_i)_{i \in I}}}
    \\
    \Im V
  }
  \,.
$$

Moreover, in any [[sheaf topos]] [[universal colimits|colimits are universal]], which means that maps out of colimits
are preserved under [[pullback]]. Moreover, the pullback of an [[isomorphism]] is an isomorphism,
and so we deduce that we have a pullback diagram of the form

$$
  \array{
    \underset{i \in I}{\coprod}V_i  &\longrightarrow& \underset{i \in I}{\coprod} \Im V
    \\
    {}^{{\mathllap{(id_i)_{i \in I}}}}\downarrow &(pb)& \downarrow^{\mathrlap{(id_i)_{i \in I}}}
    \\
    V &\underset{\eta_V}{\longrightarrow}& \Im V
  }
  \,.
$$

But, again because $\Im$ preserves colimits, this is manifestly the $\Im$-naturality square of the
original morphism.

=--


+-- {: .num_defn #VManifold}
###### Definition

Let $V \in SuperFormalSmoothSet$ be given (def. \ref{FormalSmoothSets}), equipped with the structure of a [[group object]].

A _[[V-manifold]]_ is an $X \in SuperFormalSmoothSet$ such that there exists a _$V$-[[atlas]]_, namely a [[correspondence]] of the form

$$
  \array{
    && U
    \\
    & {}^{\mathllap{et}}\swarrow && \searrow^{\mathrlap{et, epi}}
    \\
    V && && X
  }
$$

with both morphisms being [[local diffeomorphisms]], def. \ref{LocalDiffeomorphisms}, and the right one in addition being an [[epimorphism]].

By prop. \ref{ProjectioonOutOfCoproductIsFormllyEtale} this means that $X$ is in particular a [[V-manifold]]
if there exists a [[set]] $I$ and a morphism out of the [[coproduct]] of $I$ copies of $V$ to $X$ which is a locally diffeomorphic
epimorphism:

$$
  \array{
    \underset{i \in I}{\coprod} V
    \\
     \downarrow^{\mathrlap{et}}_{\mathrlap{epi}}
    \\
    X
  }
$$

Specifically if $V = \mathbb{R}^{p\vert q}$ be a [[super Cartesian space]] regarded as a [[group object]] under a
[[translation supergroup]] action. Then we say that $X$ is a **[[supermanifold]]** of [[dimension]] $(p\vert q)$
if there exists

$$
  \array{
    \underset{i \in I}{\coprod} \mathbb{R}^{p\vert q}
    \\
     \downarrow^{\mathrlap{et}}_{\mathrlap{epi}}
    \\
    X
  }
$$

=--

+-- {: .num_remark}
###### Remark

There are in general several [[translation supergroup]] structures carried by a super Cartesian space.
For instance in the discussion at _[[geometry of physics -- supersymmetry]]_ we will consider
[[super Minkowski spacetime|super Minkowski]] supergroup structure which exists for special
pairs $(p,q)$.
Just the existence of a supermanifold structure in def. \ref{VManifold} does not depend
on the choice of group structure on $V$ (and could be ignored for much of the present purpose).
But later on the choice affects for instance the concept of [[torsion of a G-structure]] on the [[V-manifold]].

=--

+-- {: .num_example #OddTangentBundle}
###### Example
**([[odd tangent bundle]])**

Let $X$ be a [[smooth manifold]] of [[dimension]] $n$ and $E \to X$ a smooth [[vector bundle]] over $X$ of [[rank]]
$k \in \mathbb{N}$. Then there is a [[supermanifold]] (def. \ref{VManifold}) of dimension
$(n \vert k)$, denoted $\Pi E$, as follows.

Write

$$
  \mathcal{O}(\Pi E)
    \;\coloneqq\;
  \wedge^\bullet_{C^\infty(X)} \Gamma_X(E)
  =
  C^\infty(X)
    \;\oplus\;
  \Gamma_X(E^\ast)
    \;\oplus\;
  \left(\Gamma_X(E^\ast) \wedge_{C^\infty(X)} \Gamma_X(E^\ast)\right)
    \;\oplus\;
  \cdots
$$

for the [[supercommutative superalgebra]] which is the [[exterior algebra]] over $C^\infty(x)$ of the $C^\infty(X)$-[[module]]
$\Gamma_X(E^\ast)$ of [[smooth sections]] (as in the [[smooth Serre-Swan theorem]], Prop. \ref{FirstTwoMagicPropertiesOfAlgebrasOfSmoothFunctions}) of the [[dual vector bundle]] $E^\ast$.

The underlying [[functor of points]] of $\Pi E$  (remark \ref{ASheafAsASpace})

$$
  \Pi E \;\colon\; SuperCartSp^{op} \longrightarrow Set
$$

is the one that is [[representable functor|represented]]
by this algebra:

$$
  \Pi E \;\colon\; \mathbb{R}^{p \vert q}
   \mapsto
   Hom_{sCalg_{\mathbb{R}}}(
     \wedge^\bullet_{C^\infty(X)} \Gamma_X(E) , \;
     C^\infty(\mathbb{R}^n) \otimes_{\mathbb{R}} \wedge^\bullet_{\mathbb{R}} (\mathbb{R}^q)^\ast
  )
  \,.
$$

For instance if $E = T X$ is the [[tangent bundle]] of $X$, so that the dual bundle is the [[cotangent bundle]], then

$$
  \mathcal{O}(\Pi T X)
  \simeq
  \Omega^\bullet(X)
    \coloneqq
  \wedge^\bullet_{C^\infty(X)}\Gamma_X(T^\ast X)
$$

is the superalgebra of smooth [[differential forms]] on $X$ with respect to the wedge product, with any $p$-form
regarded as being in degree $p \,mod\, 2 \in \mathbb{Z}/2$.

This $\Pi T X$ is often called the **[[odd tangent bundle]]**.

Notice that generally we may think of $\Pi E$ as being the [[superspace]] which is obtained from the base manifold
$X$ by adding an (odd-graded) infinitesimal thickening where an "infinitesimal step" away from some point $x \in X$
is a [[vector]] in the [[fiber]] $E_x$. This is particularly suggestive in the case that $E$ is the tangent bundle,
because tangent vectors precisely want to be thought of as the infinitesimal paths in $X$.

Below we see that this is not a coincidence, and discuss the formal proof that $\Pi T X$ is the superspace of
(odd-graded) infinitesimal paths in $X$.

=--




+-- {: .num_prop #BosonicModalityPreservesLocalDiffeomorphism}
###### Proposition
**([[bosonic modality]] preserves [[formally étale morphisms]])**

If $f \;\colon\; X \longrightarrow Y$ is a [[formally étale morphism]],
def. \ref{LocalDiffeomorphisms}, then so is its image
$\stackrel{\rightsquigarrow}{f}\colon \stackrel{\rightsquigarrow}{X} \longrightarrow \stackrel{\rightsquigarrow}{Y}$ under the [[bosonic modality]].

=--

+-- {: .proof }
###### Proof

By Prop. \ref{SuperSmoothSetsSystemOfAdjunctions} we have equivalences

$$
  \overset{\rightsquigarrow}{\Im(-)}
  \;\simeq\;
  \Im(-)
  \;\simeq\;
  \Im \overset{\rightsquigarrow}{(-)}
  \,.
$$

The first of these equivalences is the "left [[Aufhebung]]" which is explicit in Prop. \ref{SuperSmoothSetsSystemOfAdjunctions}. The second equivalence is under the [[Yoneda embedding]], equivalent to the "[[adjunct]] equivalence"

$$
  \overset{\rightrightarrows}{\Re(-)} \;\simeq\; \Re(-)
$$

which follows from the progression in Prop. \ref{SuperSmoothSetsSystemOfAdjunctions} since $\rightrightarrows$ and $\rightsquigarrow$ have the same [[full subcategory]] of [[modal objects]] $FormalSmoothset \overset{\iota_{sup}}{\hookrightarrow} SuperFormalSmoothSet$, and since $\rightsquigarrow \gt \Re$, by (eq:ProgressionOfModalitiesOnSuperFormalSmoothSet).

Moreover, since $\rightsquigarrow$ [[preserved limit|preserves]] [[pullbacks]] (being a [[right adjoint]], by [this Prop.](geometry+of+physics+--+categories+and+toposes#AdjointsPreserveCoLimits)). Hence hitting a pullback diagram which exhibits a [[formally étale morphism]] $f$ (Def. \ref{LocalDiffeomorphisms})

$$
  \array{
    X &\longrightarrow& \Im X
    \\
    \downarrow^{\mathrlap{f}} &(pb)& \downarrow^{\mathrlap{\Im f}}
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

that witnesses $\overset{\rightsquigarrow}{\f}$ as being [[formally étale morphisms]] formally étale.

=--

+-- {: .num_cor }
###### Corollary

The bosonic space $\stackrel{\rightsquigarrow}{X}$ underlying
a [[V-manifold]] $X$, def. \ref{VManifold}, is a $\stackrel{\rightsquigarrow}{V}$-manifold.

=--



$\,$









## Super differential forms
 {#DeRhamComplexOfSuperDifferentialForms}

We discuss the super-geometric analog of [[differential forms]] on [[supermanifolds]], first with
[[coefficients]] in $\mathbb{R}$, then with coefficients in a [[super Lie algebra]].

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

and extended from there to all degrees by the graded Leibniz rule.

It is immediate to generalize this to [[supergeometry]], one just needs to be sure to apply the [[signs in supergeometry|sign rule]] throughout.


+-- {: .num_defn #SuperDeRhamComplex}
###### Definition
**([[de Rham complex]] of [[super differential forms]])**

The [[de Rham complex]] of [[super differential forms]] $\Omega^\bullet(\mathbb{R}^{p|q})$ on a [[super Cartesian space]] $\mathbb{R}^{p|q}$ is the $(\mathbb{Z},\mathbb{Z}_2)$-bigraded commutative algebra


$$
  \array{
    &
    \Omega^\bullet(\mathbb{R}^{p|q})
     &=&
     C^\infty(\mathbb{R}^{p|q})
      &
       \otimes_{\mathbb{R}}
      &
      \wedge^\bullet \langle
      &
       \mathbf{d}x^1, \cdots, \mathbf{d}x^p,
      &
        \mathbf{d}\theta^1, \cdots, \mathbf{d}\theta^q
      &
     \rangle
     \\
     \text{bidegree:}
     &
     &&
     (0,even)
     &&&
     (1,even)
     &
     (1,odd)
  }
$$

whose [[differential]] is defined in degree-0 by

$$
  \mathbf{d} f \coloneqq \sum_{i = 1}^p \frac{\partial f}{\partial x^i} \mathbf{d}x^i
$$

and extended from there to all degree by the graded Leibniz rule.


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

1. in addition there is a "super-grading" which for commuting a $\sigma_1$-graded coordinate function past a $\sigma_2$-graded coordinate function (possibly under the de Rham differential) is $(-1)^{\sigma_1 \sigma_2}$.

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
for the description of higher dimensional [[supergravity]].


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

   which is _graded_ skew-symmetric: for $x,y \in \mathfrak{g}$ two elements of homogeneous degree $\sigma_x$, $\sigma_y$, respectively, then

   $$
     [x,y] = -(-1)^{\sigma_x \sigma_y} [y,x]
     \,,
   $$

1. that satisfies the $\mathbb{Z}/2$-graded [[Jacobi identity]] in that
for any three elements $x,y,z \in \mathfrak{g}$ of homogeneous super-degree $\sigma_x,\sigma_y,\sigma_z\in \mathbb{Z}_2$ then

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



### General theory

Some historically influential remarks on [[supergeometry]] are due to

* [[Yuri Manin]], _[[New Dimensions in Geometry]]_, talk at Arbeitstagung, Bonn 1984

Introductory lecture notes include

* [[Yuri Manin]], chapter 4 of _[[Gauge Field Theory and Complex Geometry]]_, Grundlehren der Mathematischen Wissenschaften 289, Springer 1988

* [[Gennadi Sardanashvily]], _Lectures on supergeometry_ ([arXiv:0910.0092](http://arxiv.org/abs/0910.0092))

Many texts discuss supergeometry only in the context of [[supersymmetry]], but notice that the former exists and is relevant even if the latter does not or is not.

* [[Daniel Freed]], _[[Five lectures on supersymmetry]]_

* L. Caston, R. Fioresi, _Mathematical Foundations of Supersymmetry_ ([arXiv:0710.5742](http://arxiv.org/abs/0710.5742))



### For classical field theories with fermions

The [[experiment|experimental]] observation that [[phase spaces]] of [[classical field theories]] with [[fermions]] (such as [[electrons]] or [[quarks]]) are [[superspaces]] goes back to

* {#Pauli25} [[Wolfgang Pauli]], _&#220;ber den Zusammenhang des Abschlusses der Elektronengruppen im Atom mit der Komplexstruktur der Spektren_, Zeitschrift f&#252;r Physik, February 1925, Volume 31, Issue 1, pp 765-783

* {#Fierz39} [[Markus Fierz]],  _&#220;ber die relativistische Theorie kr&#228;ftefreier Teilchen mit beliebigem Spin_. Helvetica Physica Acta. 12 (1): 3&#8211;37. (1939) [doi:10.5169/seals-110930](https://dx.doi.org/10.5169%2Fseals-110930)

* {#Pauli40} [[Wolfgang Pauli]], _The connection between spin and statistics_, Phys. Rev. 58, 716&#8211;722 (1940)



Discussion of [[classical field theory]] with [[fermions]] as taking place on [[supermanifolds]] (supergometric [[field bundles]] and [[phase space]]) includes the following references:

* {#DeligneFreed99} [[Pierre Deligne]], [[Daniel Freed]], _Classical field theory_ (1999) ([pdf](https://publications.ias.edu/sites/default/files/79_ClassicalFieldTheory.pdf))

  this is a chapter in

  [[Pierre Deligne|P. Deligne]], [[Pavel Etingof|P. Etingof]], [[Dan Freed|D.S. Freed]], L. Jeffrey, [[David Kazhdan|D. Kazhdan]], J. Morgan, D.R. Morrison, [[Edward Witten|E. Witten]] (eds.)  _[[Quantum Fields and Strings]], A course for mathematicians_, 2 vols. Amer. Math. Soc. Providence 1999. ([web version](http://www.math.ias.edu/qft))


* {#Freed01} [[Daniel Freed]], _Classical field theory and Supersymmetry_, IAS/Park City Mathematics Series Volume 11 (2001) ([pdf](https://www.ma.utexas.edu/users/dafr/pcmi.pdf))

* {#GiachettaMangiarottiSardanashvily09} Giovanni Giachetta, Luigi Mangiarotti, [[Gennadi Sardanashvily]], chapter 3 of _Advanced classical field theory_, World Scientific (2009)

* {#Sardanashvily12} [[Gennadi Sardanashvily]], _Grassmann-graded Lagrangian theory of even and odd variables_ ([arXiv:1206.2508](https://arxiv.org/abs/1206.2508))

* {#Sardanashvily16} [[Gennadi Sardanashvily]], _Noether's Theorems: Applications in Mechanics and Field Theory_, Studies in Variational Geometry, 2016







### In the topos over superpoints
 {#ReferencesOverSuperpoints}

The observation that the study of super-structures in mathematics is usefully regarded as taking place over the [[base topos]] on the [[site]] of [[super points]] has been made around 1984 in

* {#Schwarz84} [[Albert Schwarz]], _On the definition of superspace_, Teoret. Mat. Fiz. (1984)  Volume 60,  Number 1, Pages 37&#8211;42, ([russian original pdf](http://www.mathnet.ru/links/b12306f831b8c37d32d5ba8511d60c93/tmf5111.pdf))

* [[Alexander Voronov]], _Maps of supermanifolds_ , Teoret. Mat. Fiz. (1984)  Volume 60,  Number 1, Pages 43&#8211;48

and in

* {#Molotkov84} V. Molotkov., _Infinite-dimensional $\mathbb{Z}_2^k$-supermanifolds_ , ICTP
preprints, IC/84/183, 1984.


A summary/review is in the appendix of

* {#KonechnySchwarz97} Anatoly Konechny and [[Albert Schwarz]],

  _On $(k \oplus l|q)$-dimensional supermanifolds_ in [[Julius Wess]], V. Akulov (eds.) _Supersymmetry and Quantum Field Theory_ (D. Volkov memorial volume) Springer-Verlag, 1998, Lecture Notes in Physics, 509 ,  ([arXiv:hep-th/9706003](http://arxiv.org/abs/hep-th/9706003))

  _Theory of $(k \oplus l|q)$-dimensional supermanifolds_ Sel. math., New ser. 6 (2000) 471 - 486


* [[Albert Schwarz]], I- Shapiro, _Supergeometry and Arithmetic Geometry_ ([arXiv:hep-th/0605119](http://arxiv.org/abs/hep-th/0605119))


A review of all this as geometry in the [[topos]] over the category of [[superpoints]] is in

* {#Sachse08} [[Christoph Sachse]], _A Categorical Formulation of Superalgebra and Supergeometry_ ([arXiv:0802.4067](http://arxiv.org/abs/0802.4067))

### In the topos over super Cartesian spaces

The [above](#ReferencesOverSuperpoints) perspective of supergeometry in the topos over superpoints is a restriction of the
perspective in the topos over [[super Cartesian spaces]] which we use here. This in turn is
essentially just the specification to [[supercommutative superalgebra]] of [[Alexander Grothendieck]]'s concept of "[[functorial geometry]]" as laid out in

* {#Grothendieck65} [[Alexander Grothendieck]], _Introduction au langage fonctoriel_, course in Algiers in November 1965, lecture notes by [[Max Karoubi]], [pdf scan](http://webusers.imj-prg.fr/~leila.schneps/grothendieckcircle/GrothAlgiers.pdf).

Grothendieck amplified that this functorial perspective is superior to the
perspective on schemes as [[locally ringed spaces]] in the lecture

* {#Grothendieck73} [[Alexander Grothendieck]], _Introduction to functorial algebraic geometry, part 1: affine algebraic geometry_, summer school in Buffalo, 1973, lecture notes by Federico Gaeta ([pdf scan](http://matematicas.unex.es/~navarro/res/ifag.pdf))

Further amplification of Grothendieck's amplification may be found in the short text

* {#Lawvere03} [[William Lawvere]], _Grothendieck's 1973 Buffalo Colloquium_, posting to the mailing list _categories@mta.ca_, March 2003 ([gmane archive](http://permalink.gmane.org/gmane.science.mathematics.categories/2228))

The application of this perspective to supergeometry is sometimes known as [[synthetic differential supergeometry]]:

* {#Yetter88} [[David Yetter]], _Models for synthetic supergeometry_, Cahiers, 29, 2 (1988) ([NUMDAM](http://www.numdam.org/item?id=CTGDC_1988__29_2_87_0))


The formulation via the axioms of [[differential cohesion]] that we use here follows

* {#Schreiber} [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

* [[Hisham Sati]], [[Urs Schreiber]], Sec. 3.1.3 of: *[[schreiber:Proper Orbifold Cohomology]]* ([arXiv:2008.01101](https://arxiv.org/abs/2008.01101))

* [[Igor Khavkine]], [[Urs Schreiber]], _[[schreiber:Synthetic variational calculus|Synthetic geometry of differential equations Part I -- Jets and comonad structure]]_ ([arXiv:1701.06238](https://arxiv.org/abs/1701.06238))

* [[Felix Wellen]], _[[schreiber:thesis Wellen|Formalizing Cartan Geometry in Modal Homotopy Type Theory]]_, 2017 ([arXiv:1806.05966](https://arxiv.org/abs/1806.05966), [pdf](http://www.math.kit.edu/iag3/~wellen/media/diss.pdf))



