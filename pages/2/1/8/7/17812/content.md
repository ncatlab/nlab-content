
$\,$

$\,$

> this entry is one section of "[[geometry of physics -- supergeometry and superphysics]]"
> which is one chapter of "[[geometry of physics]]"

> previous section: _[[geometry of physics -- superalgebra]]_

> next section: _[[geometry of physics -- supersymmetry]]_

> under construction

$\,$


Supergeometry is the generalization of [[differential geometry]] (or [[algebraic geometry]]) to the situation where [[algebras of functions]]
are generalized from [[commutative algebras]] to [[supercommutative superalgebras]].

In _[[geometry of physics -- superalgebra]]_ we discussed why it is mathematically compelling to pass
to [[supercommutative superalgebra]] and how this implies a dual concept of [[superspace]] in terms of [[affine superschemes]].
Here we discuss how to build a fully-fledged theory of [[geometry]] on these affine [[superspaces]] -- [[supergeometry]] --
in parallel to the discussion of ordinary [[differential geometry]] in _[[geometry of physics -- smooth sets]]_.

<div style="float:right;margin:0 20px 10px 20px;">
<img src="http://ncatlab.org/schreiber/files/ProgressionOfModalities.jpg" width="200">
</div>


Apart from the abstract mathematical motivation for supergeometry, it is also an observational fact that the
[[observable universe]] is fundamentally described by
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
 [Fierz in 1939](spin-statistics+theorem#Fierz39) and [Pauli in 1940](#spin-statistics+theorem#Pauli40).

 Notice that this phenomenon is not a negligible subtlety: the [[Pauli exclusion principle]]
 is what implies [[stability of matter]] by forcing [[electrons]] in an [[atom]] to fill up
 "orbitals" consecutively as opposed to all falling into the ground state, as a bosonic [[condensate]] would do.
 There would be no [[solid state physics]] without supergeometry of [[phase spaces]], no [[matter]] as we know it.
 (In addition, the Pauli [[degeneracy pressure]] controls more exotic phenomena, for instance the
  stability of neutron stars against their gravitational collapse.)

As a slogan:

$\,\,\,\,\,\;$ _**The [[geometry]] of [[phase spaces]] for [[fermions]], hence for [[matter]] fields, is [[supergeometry]].**_

Nevertheless, few textbooks make the supergeometric aspect in the physics of fermions explicit.
Some discuss it only after [[quantization]] (and some will even claim that femion fields do not exist classically);
some only discuss it in the context of [[spacetime]] [[supersymmetry]]. But notice that
_[[supergeometry]]_ is a subject in itself even without presence or mentioning of spacetime [[supersymmetry]]
(which is [[super Poincaré group]] [[symmetry]]), just as
[[differential geometry]] is a subject in itself even without the presence or mentioning of
[[Poincaré group]] symmetry.

Texts which do make the super-geometric nature of [[fermion fields]] explicit include
[Deligne-Freed 99, &#167;3.4](#DeligneFreed99), [Freed 01, lecture 4](#Freed01), [Giachetta-Mangiarotti-Sardanashvily 09, chapter 3](#GiachettaMangiarottiSardanashvily09), [Sardanashvily 12](#Sardanashvily12), [Sardanashvily 16](#Sardanashvily16).


#Supergeometry#
* table of contents
{:toc}




In the section _[[geometry of physics -- superalgebra]]_ we discussed the [[category]] of **[[affine super schemes]]**
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
  C^\infty(\mathbb{R}^q) \otimes_{\mathbb{R}} \wedge^\bullet (\mathbb{R}^\ast)^q
  \,.
$$

These serve as our "abstract super-coordinate systems" that define [[supergeometry]] in direct analogy to how ordinary [[Cartesian spaces]] serve as the abstract coordinate systems that define [[differential geometry]] as found at
_[[geometry of physics -- coordinate systems]]_  and_[[geometry of physics -- smooth sets]]_.
We now discuss this in detail.


## Super Cartesian spaces
 {#CoordinareSystemsSuperCartesianSpaces}


+-- {: .num_defn #SuperCartesianSpace}
###### Definition

For $q\in \mathbb{N}$, the real [[Grassmann algebra]]

$$
  C^\infty(\mathbb{R}^{0|q})
  \coloneqq
  \wedge^\bullet \langle \theta^1, \cdots, \theta^q\rangle
$$

is the $\mathbb{R}$-algebra [[free functor|freely]] generated from $q$ generators $\{\theta^i\}_{i = 1}^q$ subject to the relations

$$
  \theta^i \theta^j = - \theta^j \theta^i
$$

for all $i,j \in \{1,\cdots, q\}$.

For $p,q \in \mathbb{N}$, the [[super-Cartesian space]] $\mathbb{R}^{p|q}$ is the [[formal dual]] of the [[supercommutative superalgebra]] written $\mathcal{O}(\mathbb{R}^{p\vert q})$ or $C^\infty(\mathbb{R}^{p|q})$ whose underlying
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
 SuperCartSp \hookrightarrow sCAlg_{\mathbb{R}}^{op}
$$

for the [[full subcategory]] of the [[opposite category]] of [[commutative superalgebras]] on those of this form. We write
$\mathbb{R}^{p|q} \in SuperCartSp$ for the [[formal dual]] of
$C^\infty(\mathbb{R}^{p|q})$.

=--



We write

$$
  CartSp \hookrightarrow SuperCartSp
$$

for the [[full subcategory]] on ordinary [[Cartesian spaces]] with [[smooth functions]] between them.
These are the "abstract coordinate charts" from the discussion at _[[geometry of physics -- smooth sets]]_,
and so we are evidently entitled to think of the objects in $SuperCartSp$ as **abstract super coordinate systems**
and to develop a geometry induced from these.

Recall the two magic algebraic properties of [[smooth functions]] that make the above algebraic description of
[[differential geometry]] work:

1. (**[[embedding of smooth manifolds into formal duals of R-algebras]]**) The functor that assigns [[algebra of functions|algebras of]] [[smooth function]] of [[smooth manifolds]]

   $$
     C^\infty(-) \;\colon\; SmthMfd \hookrightarrow CAlg_{\mathbb{R}}^{op}
   $$

   is [[fully faithful functor|fully faithful]].

1. (**[[smooth Serre-Swan theorem]]**) The functor that assigns smooth [[sections]] of smooth [[vector bundles]]
   of [[finite number|finite]] [[rank]]

   $$
     \Gamma_X(-) \;\colon\; SmthVectBund_{/X} \hookrightarrow C^\infty(X) Mod
   $$

   is [[fully faithful functor|fully faithful]] (its [[essential image]] being the [[finitely generated object|finitely generated]] [[projective modules]] over the $\mathbb{R}$-[[algebra of functions|algebra of]] [[smooth function]]).

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
is related to that of ordinary [[commutative algebras]] over $\mathbb{R}$ by an
[[adjoint cylinder]] ([this prop.](geometry+of+physics+--+superalgebra#InclusionOfCAlgIntosCAlg)):

+-- {: .num_prop #AdjointCylinderOnSuperAffines}
###### Proposition

The canonical inclusion of [[commutative algebras]] into [[supercommutative superalgebra]] is
part of an [[adjoint triple]] of the form

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
      {\underset
        {
          \phantom{AA}
          \overset
            {\phantom{A}}
            {\overset{\rightsquigarrow}{(-)}}
          \phantom{AA}
         }
         {\longleftarrow}
      }
      {\overset
         {
          \phantom{AA}
           \underset
            {\phantom{A}}
            { \overset{\rightrightarrows}{(-)} }
          \phantom{AA}
        }
        {\longleftarrow}
      }
      {\hookrightarrow}
  Aff(sVect_k)
  \,.
$$

(Beware that $\overset{\rightsquigarrow}{(-)}$ is the formal dual of $(-)/(-)_{odd}$ while $\overset{\rightrightarrows}{(-)}$ is the
formal dual of $(-)_{even}$. That they change position in the diagrams is because we always draw [[left adjoints]] on top of [[right adjoints]] and  the handedness of [[adjoints]] changes as we pass to [[opposite categories]].)

=--



The notation in prop. \ref{AdjointCylinderOnSuperAffines} is to serve as a convenient mnemonic for the nature of these functors:

In a [[Feynman diagram]]

1. a single [[fermion]] is denoted by a solid arrow "$\to$" and the functor
$\overset{\rightrightarrows}{(-)}$ produces a space whose [[algebra of functions]] is generated over
smooth functions by the product of two fermionic functions

1. a single [[boson]] is denoted by a wiggly arrow $\rightsquigarrow$ and the functor
   denoted by this symbol produces a spaces whose [[algebra of functions]] contains only the
   bosonic smooth functions, no odd-graded functions.


This highlights an important point: while the image of a [[super Cartesian space]] under $\rightsquigarrow$
is an ordinary [[Cartesian space]]

$$
   \overset{\rightsquigarrow}{\mathbb{R}^{p\vert q}}
   \simeq
   \mathbb{R}^p
$$

its image under $\overset{\rightrightarrows}{(-)}$ is a bosonic space, but not an ordinary manifold. For instance

$$
  \begin{aligned}
   \mathcal{O}\left( \overset{\rightrightarrows}{\mathbb{R}^{0\vert 2}}\right)
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

This algebra $\mathbb{R}[\epsilon]/(\epsilon^2)$
is known as the **[[algebra of dual numbers]]** over $\mathbb{R}$. It is to be thouhgt of as the [[algebra of functions]]
on a bosonic but [[infinitesimally thickened point]], a 1-dimensional neighbourhood of a point which is "so very small"
that the canonical [[coordinate]] function $\epsilon$ on it takes values "so tiny" that its square, which is bound to be
even tinier, is actually indistinguishable from zero.

In generalization of this we make the following definitions

+-- {: .num_defn #FormalCartSp}
###### Definition

Write

$$
  InfPoint \hookrightarrow CAlg_{\mathbb{R}}^{op}
$$

for the [[full subcategory]] of the [[opposite category]] of [[commutative algebras]] over $\mathbb{R}$ on [[formal duals]]
$\mathbb{D}$ of [[commutative algebras]] over the [[real numbers]] of the form

$$
  \mathcal{O}(\mathbb{D})
    \coloneqq
  \mathbb{R}\oplus V
$$

with $V$ a [[nilpotent ideal]] of [[finite number|finite]]-[[dimension]]
over $\mathbb{R}$. We call this the category of _[[infinitesimally thickened points]]_.

In [[synthetic differential geometry]] these algebras are called **[[Weil algebra]]**, while in [[algebraic geometry]] they are known as **local [[Artin algebras]]** over $\mathbb{R}$.

Write moreover

$$
  FormalCartSp \coloneqq CartSp \rtimes InfPoint \hookrightarrow CAlg_{\mathbb{R}}^{op}
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

This kind of construction is traditionally more familiar from the theory of [[formal schemes]], but the same kind of general abstract theory goes through in the context of [[differential geometry]], a point of view known as _[[synthetic differential geometry]]_.

The crucial property of [[infinitesimally thickened points]] (def. \ref{FormalCartSp}) is that they co-represent
[[tangent vectors]] and [[jets]]:

+-- {: .num_prop}
###### Proposition

Write $\mathbb{D}^1 = Spec(\mathbb{R}[\epsilon]/(\epsilon^2))$ for the [[formal dual]] of the [[algebra of dual numbers]].

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

This in turn means equivalently that $\partial\colon C^\infty(\mathbb{R}^n)\to C^\infty(\mathbb{R}^n)$ is a [[derivation]].
But [[derivations of smooth functions are vector fields]] (prop. \ref{DerivationsOfSmoothFunctions}).


=--

+-- {: .num_prop #CartSpCoreflectiveInclusion}
###### Proposition

The canonical inclusion $i$ of the category of ordinary [[Cartesian spaces]] into that of [[formal manifold|formal]] [[Cartesian spaces]]
has a [[left adjoint]] $\Re$

$$
  CartSp
    \underoverset
      {\underset{\Re}{\longleftarrow}}
      {\overset{i}{\hookrightarrow}}
      {\phantom{AAAA}}
  FormalCartSp
$$

given by

$$
  \Re(\mathbb{R}^n \times \mathbb{D}) \coloneqq \mathbb{R}^n
  \,.
$$

Hence exhibits $CartSp$ as a [[coreflective subcategory]] of that of formal cartesian spaces.

We say that $\mathbb{R}^n$ is the **[[reduced scheme]]** of $\mathbb{R}^n \times \mathbb{D}$.

=--

+-- {: .proof}
###### Proof

We check the [[natural isomorphism]] on [[hom-sets]] that characterizes a pair of [[adjoint functors]]:

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

where all elements $v \in V$ are nilpotent, in that there exists $n_v \in \mathbb{N}$
such that $(v)^{n_v} = 0$. Every algebra homomorphism needs to preserve this
equation, and hence needs to send nilpotent elements to nilpotent elements. But the
only nilpotent element in the ordinary function algebra $C^\infty(\mathbb{R}^n)$
is the zero-function, and so it follows that the above homomorphism has to vanish on all of $V$, hence has
to factor (necessarily uniquely) through a homomorphism of the form

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

In order to make this explicit, it is convenient to introduce the following slight generalization of
[[super Cartesian spaces]] (def. \ref{SuperCartesianSpace}), which are simply [[Cartesian products]]
of ordinary [[Cartesian spaces]] with an [[infinitesimally thickened point]] that may have both even and
odd graded elements in its [[algebra of functions]].


+-- {: .num_defn #SuperFormalCartSp}
###### Definition

Write

$$
  SuperFormalCartSp
    \hookrightarrow
  sCAlg_{\mathbb{R}}^{op}
$$

for the [[full subcategory]] of that of the [[opposite category]] of [[supercommutative superalgebras]]
on whose of the form

$$
  C^\infty(\mathbb{R}^p) \otimes_{\mathbb{R}} (\mathbb{R} \oplus V)
$$

where $V$ is a [[nilpotent ideal]] of [[finite number|finite]] [[dimension]] over $\mathbb{R}$.

=--

One place where such super formal Cartesian spaces are made explicit is in [Konechny-Schwarz 97](#KonechnySchwarz97).
Just as formal Cartesian spaces may be thought of as local model spaces for [[synthetic differential geometry]],
[[super formal Cartesian spaces]] may be thought of as a model for [[synthetic differential supergeometry]].
This we come to [below](#SuperSmoothSets).


In conclusion, the various [[extra structure]] on local model spaces (abstract coordinate systems) which we
considered is organized in the following [[diagram]].

+-- {: .num_prop #SystemOfSites}
###### Proposition


The [[coreflective subcategory]] inclusion of [[Cartesian spaces]] into
[[formal manifold|formal]] [[Cartesian spaces]] from prop. \ref{CartSpCoreflectiveInclusion}
and the coreflective as we all [[reflective subcategory]] inclusion
of affine schemes into [[affine superschemes]] from prop. \ref{AdjointCylinderOnSuperAffines}
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
    \underoverset
      {\hookrightarrow}
      {\overset{\pi}{\longleftarrow}}
      {}
   &
  CartSp
   &
    \underoverset
      {\underset{\Re}{\longleftarrow}}
      {\overset{}{\hookrightarrow}}
      {}
   &
  FormalCartSp
  &
    \underoverset
      {\underset
        {
          \phantom{AA}
          \overset
            {\phantom{A}}
            {\overset{\rightsquigarrow}{(-)}}
          \phantom{AA}
         }
         {\longleftarrow}
      }
      {\overset
         {
          \phantom{AA}
           \underset
            {\phantom{A}}
            { \overset{\rightrightarrows}{(-)} }
          \phantom{AA}
        }
        {\longleftarrow}
      }
      {\hookrightarrow}
  &
  SuperFormalCartSp
  }
  \,.
$$

=--












## Super smooth sets
 {#SuperSmoothSets}


[Above](#CoordinareSystemsSuperCartesianSpaces) we discussed ([[formal manifold|formal]]) [[super Cartesian spaces]]. What we are after is geometry which is "locally modeled" on these. In order to do so we

1. consider very general [[superspaces]] whose collection forms a "good category" (the [[sheaf topos]] over super Cartesian space) in that lots of [[universal constructions]] on general superspaces ([[limits]], [[colimits]]) still yield general superspaces;

2. use special properties of this nice category ([[differential cohesion]]) in order to characterize and construct the good, tame superspaces, such as actual [[supermanifolds]].

The construction proceeds in direct anology to the non-super version discussed at _[[geometry of physics -- smooth sets]]_
and at _[[geometry of physics -- manifolds and orbifolds]]_. For reference we first briefly recall this bosonic situation.



+-- {: .num_defn #SiteCartSp}
###### Definition

Write [[CartSp]] for the [[category]] of [[Cartesian space]] $\mathbb{R}^n$ for $n \in\mathbb{N}$ with [[smooth functions]] between them. Say that a collection of morphisms $\{U_i \to X\}$ in $CartSp$ is [[covering]] if this is a [[good open cover]] in that every finite non-empty intersection of the charts is [[diffeomorphism|diffeomorphic]] to a Cartesian space.
This defines a [[coverage]] on [[CartSp]] and hence makes it a [[site]].

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

Namely a smooth set $X$ in the sense of def. \ref{Smooth0Type} is first of all a rule

$$
  \mathbb{R}^p \maptos X(\mathbb{R}^p) \in Set
$$

which assigns a set to each Cartesian space. We are to think of this set as the set of smooth functions "$\mathbb{R}^n \stackrel{}{\to} X$", only that there is no pre-defined concept of smoothness of functions into $X$, instead it is defined by that very rule.
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

which we are to think of as being the precomosition operation

$$
  (\text{"}\mathbb{R}^{n_2} \stackrel{\phi}{\to} X\text{"})
     \;\mapsto\;
  (\text{"}f^\ast \phi \colon \mathbb{R}^{n_1} \overset{f}{\to} \mathbb{R}^{n_2} \overset{\phi}{\to} X\text{"})
  \,.
$$

This is required to satisfy the evident conditions that [[composition]] and [[identity]] is respected, in that
$(g \circ f)^\ast = g^\ast \circ f^\ast $ and $id^\ast = id$. Together these conditions say that $X$ is a
[[presheaf]].

In addition, the requirement that $X$ be a [[sheaf]] on the [[site]] of Cartesian space from def. \ref{SiteCartSp}
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
  CartSp \hookrightarrow Smooth0Type
$$

called the _[[Yoneda embedding]]_.

The same construction works for $X$ any [[smooth manifold]]: it is regarded as a smooth set defined by the rule

$$
  \mathbb{R}^n \mapsto C^\infty(\mathbb{R}^n ,X)
$$

which assigns actual sets of smooth functions.

Notice that now that Cartesian spaces (and smooth manifolds) themselves are understood as special cases of smooth sets, there appers now an
actual concept of smooth functions of the form $\mathbb{R}^n \to X$, for every smooth set $X$, without quotation marks:
namely this is a morphism in the category $Smooth0Type$ of smooth sets.

Now there might be a worry: given any smooth set $X$ and any Cartesian space $\mathbb{R}^n$, we seem to have _two different_
concepts of what the set of smooth functions from $\mathbb{R}^n$ to $X$ is: the set $X(\mathbb{R}^n)$
of "smooth functions by fiat" (maps with quotation marks) and the actual [[hom-set]] $Hom_{Smooth0Type}(\mathbb{R}^n, X)$
(maps without quotation mark).

That these two sets are in fact in [[natural bijection]], hence that the interpretation of a sheaf $X$ as a generalized smooth space
is consistent, is the statement of the _[[Yoneda lemma]]_

$$
  Hom_{Smooth0Type}(\mathbb{R}^n, X)
  \;
    \simeq
  \;
  X(\mathbb{R}^n)
  \,.
$$

Hence we may remove the quotation marks:

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
$\{$[[smooth sets]]$\}$
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

=--


By the same strategy we now pass to generalized spaces which are locally modeled not
just on plain Cartesian spaces, but also on formal Cartesian spaces and on
[[super Cartesian spaces]].


+-- {: .num_defn #FormalSmoothSets}
###### Definition

Define a [[coverage]] on the categories $FormalCartSp$ (def. \ref{FormalCartSp}
and on $SuperFormalCartSp$ (def. \ref{SuperFormalCartSp}) by declaring the [[covering]]
families of any object $\mathbb{R}^n \times \mathbb{D}$ (hence for $\mathbb{D}$
with $\mathcal{O}(\mathbb{D}) = (\mathbb{R} \oplus V)$ any infinitesimally thickened
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

In analogy with def. \ref{Smooth0Type} we say that

1. a [[sheaf]] on $FormalCartSp$ is a **formal smooth set** or **formal smooth [[0-type]]** and we write

  $$
    FormalSmooth0Type \coloneq FormalSmoothSet \coloneqq Sh(FormalCartSp)
  $$

  for the [[sheaf topos]] of all of these;

1. a [[sheaf]] on $FormalCartSp$ is a **[[super formal smooth set]]** or **super formal smooth [[0-type]]** and we write

  $$
    SuperFormalSmooth0Type \coloneqq SuperFormalSmoothSet \coloneqq Sh(FormalCartSp)
  $$

  for the [[sheaf topos]] of all of these;

=--

The category of formal smooth sets from def. \ref{FormalSmoothSets} is often known as the _[[Cahiers topos]]_. It was introduced in ([Dubuc 79](Cahiers+topos#Dubuc79) as a well-adapted model for the [[Kock-Lawvere axioms]] for [[synthetic differential geometry]].



+-- {: .num_prop}
###### Proposition

There exists an essentially unique system of [[functors]] between the categories of [[sets]],
[[smooth sets]] (def. \ref{Smooth0Type}), formal smooth sets and super formal smooth sets (def. \ref{FormalSmoothSets})
as shown in the second and third row of the following diagram, such that

1. every moprhism show _below_ another morphism is [[right adjoint]] to the top morphism;

1. on [[representables]] the functors coincide with the corresponding functors between [[sites]] shown
   in the first row (from prop. \ref{SystemOfSites}).

<img src="https://ncatlab.org/nlab/files/AjunctionsForSuperCohesion.png" width="600">


=--

+-- {: .proof}
###### Proof

The functors between the [[sheaf toposes]] are given by left and right [[Kan extensions]] of sheaves along the
functors between the [[sites]]:

For a single functor $F \colon \mathal{C} \to \mathcal{D}$ precomposition with this functor
defines a functor $F^\ast \colon PSh(\mathcal{D}) \to PSh(\mathcal{C})$ and this has both a [[left adjoint]]
and a [[right adjoint]] called the left and right [[Kan extension]] $F_!$ and $F^\ast$, respectively
(an [[adjoint triple]]).

$$
  PSh(\mathcal{C})
    &
    \underoverset
     {\underset{\phantom{AA}F_\ast\phantom{AA}}{\longrightarrow}}
     {\overset{\phantom{AA}F_!\phantom{AA}}{\longrightarrow}}
     {\overset{\phantom{AA}F^\ast\phantom{AA}}{\longleftarrow}}
    &
  PSh(\mathcal{D})
  \,.
$$

It is a basic fact of [[category theory]] ([this prop](Kan+extension#LeftKanExtensionBasicProp)) that on representables $c \in \mathcal{C} \overset{y}{\hookrightarrow} PSh(\mathcal{C})$
then $F_!(y(c)) = y(F(c))$. Moreover, since every presheaf is a [[colimit]] of [[representables]] (the "[[co-Yoneda lemma]]")
and since left adjoint functors preserve [[colimits]], this property completely characterizes the left Kan extension.


Now if $F$ itself has a [[right adjoint]]

$$
  \mathcal{C}
    \underoverset
      {\underset{\phantom{AA}G\phantom{AA}}{\longleftarrow}}
      {\overset{\phantom{AA}F\phantom{AA}}{\longrightarrow}}
      {}
  \mathcal{D}
$$

then the two [[adjoint triples]] induced by both functors overlap to give an [[adjoint quadruple]]
in that there are [[natural isomorphisms]] of the form

$$
  F^\ast \simeq G_! \;\;\;\;\; F_\ast \simeq G^\ast
  \,.
$$

To see this, it is sufficient to see the left hand side. It implies the right hand side because [[adjoint functors]]
are essentially unique, if they exist. Moreover, since both functors on the left are [[left adjoints]]
which hence preserve [[colimits]] and since all presheaves are [[colimits]] of [[representable functors|representables]]
it is sufficient to check this natural isomorphisms on representables.

Hence for any $X \in \mathcal{D} \overset{y}{\hookrightarrow} PSh(\mathcal{D})$ 
and $c \in \mathcal{C} \overset{y}{\hookrightarrow} PSh(\mathcal{C})$ we check that 
we have the following [[natural isomorphism]]

$$
  \begin{aligned}
    (F^\ast X)(c)
      & =
    X(F(c))
    \\
    & \simeq
    Hom(F(c),X)
    \\
    & \simeq
    Hom(-,G(c))
  \end{aligned}
  \,.
$$

Here the first equality is the definition of $F^\ast$, then the isomorphism is the 
[[Yoneda lemma]] and the last isomorphism is the one that characterizes the adjunction
$F \dashv G$.

Here a priori the Kan extension only exists on
the categories of presheaves, but one checks that for our sites they descent to sheaves. Since the [[coverage]] we use
is nontrivial only along $CartSp$, the leftmost adjoint quadruple is the only nontrivial one. That it exists is the statement that
$CartSp$ is an [[infinity-cohesive site]], see the discussion there.

The third diagram inducates that two extra adjoints to _composites_ of functors appear. Here the functor
$SmoothSet \longleftarrow SuperFormalSmoothSet$ exists because the inclusion $CartSp \hookrightarrow SuperFormalCartSp$
is of the same coreflective nature as the inclusion $CartSp \hookrightarrow FormalCartSp$, and for the same reason.
Similarly then the bottom most full inclusion $Set \hookrightarrow SuperFormalSmoothSet$ exists because also
$SuperFormalCartSp$ is an [[infinity-cohesive site]].


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

### General

Some historically influential general considerations are in

* [[Yuri Manin]], _[[New Dimensions in Geometry]]_, talk at Arbeitstagung, Bonn 1984

Introductory lecture notes include

* [[Yuri Manin]], chapter 4 of _[[Gauge Field Theory and Complex Geometry]]_, Grundlehren der Mathematischen Wissenschaften 289, Springer 1988

* [[Daniel Freed]], _[[Five lectures on supersymmetry]]_

* L. Caston, R. Fioresi, _Mathematical Foundations of Supersymmetry_ ([arXiv:0710.5742](http://arxiv.org/abs/0710.5742))

* [[Gennadi Sardanashvily]], _Lectures on supergeometry_ ([arXiv:0910.0092](http://arxiv.org/abs/0910.0092))

### In the topos over superpoints

The observation that the study of super-structures in mathematics is usefully regarded as taking place over the [[base topos]] on the [[site]] of [[super points]] has been made around 1984 in

* [[Albert Schwarz]], _On the definition of superspace_, Teoret. Mat. Fiz. (1984)  Volume 60,  Number 1, Pages 37&#8211;42, ([russian original pdf](http://www.mathnet.ru/links/b12306f831b8c37d32d5ba8511d60c93/tmf5111.pdf))

* [[Alexander Voronov]], _Maps of supermanifolds_ , Teoret. Mat. Fiz. (1984)  Volume 60,  Number 1, Pages 43&#8211;48

and in

* V. Molotkov., _Infinite-dimensional $\mathbb{Z}_2^k$-supermanifolds_ , ICTP
preprints, IC/84/183, 1984.


A summary/review is in the appendix of

* {#KonechnySchwarz97} Anatoly Konechny and [[Albert Schwarz]],

  _On $(k \oplus l|q)$-dimensional supermanifolds_ in [[Julius Wess]], V. Akulov (eds.) _Supersymmetry and Quantum Field Theory_ (D. Volkov memorial volume) Springer-Verlag, 1998, Lecture Notes in Physics, 509 ,  ([arXiv:hep-th/9706003](http://arxiv.org/abs/hep-th/9706003))

  _Theory of $(k \oplus l|q)$-dimensional supermanifolds_ Sel. math., New ser. 6 (2000) 471 - 486


* [[Albert Schwarz]], I- Shapiro, _Supergeometry and Arithmetic Geometry_ ([arXiv:hep-th/0605119](http://arxiv.org/abs/hep-th/0605119))


A review of all this as geometry in the [[topos]] over the category of [[superpoints]] is in

* {#Sachse} [[Christoph Sachse]], _A Categorical Formulation of Superalgebra and Supergeometry_ ([arXiv:0802.4067](http://arxiv.org/abs/0802.4067))



### For field theories with fermions

Discussion of [[classical field theory]] with [[fermions]] as taking place on [[supermanifolds]] ([[field bundle]], [[phase space]]) includes the following references:

* {#DeligneFreed99} [[Pierre Deligne]], [[Daniel Freed]], _Classical field theory_ (1999) ([pdf](https://publications.ias.edu/sites/default/files/79_ClassicalFieldTheory.pdf))

  this is a chapter in

  [[Pierre Deligne|P. Deligne]], [[Pavel Etingof|P. Etingof]], [[Dan Freed|D.S. Freed]], L. Jeffrey, [[David Kazhdan|D. Kazhdan]], J. Morgan, D.R. Morrison, [[Edward Witten|E. Witten]] (eds.)  _[[Quantum Fields and Strings]], A course for mathematicians_, 2 vols. Amer. Math. Soc. Providence 1999. ([web version](http://www.math.ias.edu/qft))


* {#Freed01} [[Daniel Freed]], _Classical field theory and Supersymmetry_, IAS/Park City Mathematics Series Volume 11 (2001) ([pdf](https://www.ma.utexas.edu/users/dafr/pcmi.pdf))

* {#GiachettaMangiarottiSardanashvily09} Giovanni Giachetta, Luigi Mangiarotti, [[Gennadi Sardanashvily]], chapter 3 of _Advanced classical field theory_, World Scientific (2009)


* {#Sardanashvily12} [[Gennadi Sardanashvily]], _Grassmann-graded Lagrangian theory of even and odd variables_ ([arXiv:1206.2508](https://arxiv.org/abs/1206.2508))



* {#Sardanashvily16} [[Gennadi Sardanashvily]], _Noether's Theorems: Applications in Mechanics and Field Theory_, Studies in Variational Geometry, 2016




