
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Supergeometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The analog of a [[Cartesian space]] in [[supergeometry]], a [[supermanifold]] with a single canonical [[coordinate chart]].

For suitable even|odd dimension this is naturally equipped with the structure of a [[supergroup]] that makes it a [[super-translation group]]. For Minkowski signature this is [[super-Minkowski spacetime]].


## Definition


For $p,q \in \mathbb{N}$, let $\mathbb{R}^{p|q}$ the _super Cartesian space_ of [[dimension]]_ $(p|q)$. This is the [[supermanifold]] defined by the fact that its [[algebra of functions]] is freely generated, as a [[smooth superalgebra]] by even-graded [[coordinate]]-functions $\langle \{x^a\}_{1}^p$ and odd-graded coordinate function $\{ \theta^\alpha\}_{\alpha= 1}^q$. Equivalently this is the [[tensor product]] of the [[smooth functions]] on $\mathbb{R}^p$ with the real [[Grassmann algebra]] on $q$ generators:

$$
  \begin{aligned}
      C^\infty(\mathbb{R}^{p|q}) 
      & \coloneqq 
      \langle \{x^a\}_{1}^p, \{ \theta^\alpha\}_{\alpha= 1}^q \rangle
      \\
      & = C^\infty(\mathbb{R}^p)\otimes_{\mathbb{R}} \wedge^\bullet \mathbb{R}^q
  \end{aligned}
  \,.
$$

## Details

The following is taken from _[[geometry of physics -- supergeometry]]_, see there for more:

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

for the [[full subcategory]] of the [[opposite category]] of [[commutative algebras]] over $\mathbb{R}$ on [[formal duals]] of [[commutative algebras]] over the [[real numbers]] of the form $\mathbb{R}\oplus V$ with $V$ a [[nilpotent ideal]] of [[finite number|finite]]-[[dimension]] 
over $\mathbb{R}$. We call this the category of _[[infinitesimally thickened points]]_.

In [[synthetic differential geometry]] these algebras ar called **[[Weil algebra]]**, while in [[algebraic geometry]] they are known as **local [[Artin algebras]]** over $\mathbb{R}$.

Write moreover

$$
  FormalCartSp \coloneqq CartSp \rtimes InfPoint \hookrightarrow CAlg_{\mathbb{R}}^{op}
$$

for the [[full subcategory]] on [[formal duals]] of those algebras which are [[tensor products]] of commutative $\mathbb{R}$-algebras of the form

$$
  C^\infty(\mathbb{R}^n) \otimes C^\infty(D)
$$

of algebras $C^\infty(\mathbb{R}^p)$ of [[smooth functions]] $\mathbb{R}^n$ 
with algebras corresponding to infinitesimally thickened points $D$ as above.

=--

This kind of construction is traditionally more familiar from the theory of [[formal schemes]], but the same kind of general abstract theory goes through in the context of [[differential geometry]], a point of view known as _[[synthetic differential geometry]]_.

The crucial property of [[infinitesimally thickened points]] (def. \ref{FormalCartSp}) is that they co-represent
[[tangent vectors]] and [[jets]]:

+-- {: .num_example}
###### Example

Write $\mathbb{D}^1 = Spec(\mathbb{R}[\epsilon]/(\epsilon^2))$ for the [[formal dual]] of the [[algebra of dual numbers]]. Then morphisms


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

This in turn means equivalently that $\partial\colon C^\infty(\mathbb{R}^n)\to C^\infty(\mathbb{R}^n)$ is a [[derivation]]. 
But [[derivations of smooth functions are vector fields]] (prop. \ref{DerivationsOfSmoothFunctions}).

In particular one finds that maps

$$
  \mathbb{D} \longrightarrow \mathbb{R}^n
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
on those of the form

$$
  C^\infty(\mathbb{R}^{p|q}) \otimes_{\mathbb{R}} (\mathbb{R} \oplus V)
$$

where $V$ is a [[nilpotent ideal]] of [[finite number|finite]] [[dimension]] over $\mathbb{R}$.

=--

One place where such super formal Cartesian spaces are made explicit is in [Konechny-Schwarz 97](#KonechnySchwarz97)


In conclusion we have the following situation:

+-- {: .num_prop }
###### Proposition


The [[coreflective subcategory]] inclusion of [[Cartesian spaces]] into
[[formal manifold|formal]] [[Cartesian spaces]] from prop. \ref{CartSpCoreflectiveInclusion}
and the coreflective as we all [[reflective subcategory]] inclusion  
of affine schemes into [[affine superschemes]] from prop. \ref{AdjointCylinderOnSuperAffines}
combine to give the following system of [[adjoint functors]] on our local model spaces

$$
  \array{
   {\text{} \atop {\text{differential} \atop \text{geometry}}}
   &&
   {\text{formal} \atop {\text{differential} \atop {geometry}}}
   &&
   {\text{super} \atop {\text{differential} \atop \text{geometry}}}
   \\
   \\
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



## Examples

* [[superpoint]], [[odd line]]

* [[super Minkowski spacetime]]

## Properties

### De Rham complex of differential forms

We discuss the [[de Rham complex]] of [[super differential forms]] on a super Cartesian space. (See also at _[[signs in supergeometry]]_.)

Accordingly, by the discussion at _[[Kähler forms]]_, the [[de Rham complex]] of [[super differential forms]] on $\mathbb{R}^{p|q}$ is freely generated as a super-[[module]] over the [[smooth superalgebra]] $C^\infty(\mathbb{R}^{p|q})$ by expressions of the form $\mathbf{d}x^{a_1} \wedge \cdots \wedge \mathbf{d}x^{a_k} \wedge \mathbf{d}\theta^{\alpha_1} \wedge \cdots \wedge \mathbf{d}\theta^{\alpha_l}$.

$$
  \Omega^\bullet(\mathbb{R}^{p|q})
  = 
  C^\infty(\mathbb{R}^{p|q})
  \left[
   \left\{
     \mathbf{d}x^{a_1} \wedge \cdots \wedge \mathbf{d}x^{a_k} 
     \wedge 
     \mathbf{d}\theta^{\alpha_1} \wedge \cdots \wedge \mathbf{d}\theta^{\alpha_l}
   \right\}
  \right]
  \,.
$$

This [[de Rham complex]] now carries the structure of a 

* differential graded-commutative graded commutative superalgebra 

which should be thought of as bracketet as follows

* differential graded-commutative graded (commutative superalgebra).

This means in effect that elements of $\Omega^\bullet(\mathbb{R}^{p|q})$ carry a $\mathbb{Z} \times \mathbb{Z}_2$-[[graded object|grading]], where we may say that 

* $\mathbb{Z}$ corresponds to the "cohomological grading";

* $\mathbb{Z}_2$ corresponds to the super-grading.

We write 

$$
  (n,\sigma)\in \mathbb{Z} \times \mathbb{Z}_2
$$ 

for elements in this grading group. 

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

1. there is a "cohomological sign" which for commuting a $p_1$-forms past a $p_2$-form is $(-1)^{p_1 p_2}$;

1. in addition there is a "super-grading" sich which for commuting a $\sigma_1$-graded coordinate function past a $\sigma_2$-graded coordinate function (possibly under the de Rham differential) is $(-1)^{\sigma_1 \sigma_2}$.


Some examples:

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

## Related concepts

* [[Euclidean space]]

* [[Euclidean G-space]]

[[!include geometries of physics -- table]]

* [[super-Cartan geometry]]


## References

* {#KonechnySchwarz97} Anatoly Konechny and [[Albert Schwarz]],

  _On $(k \oplus l|q)$-dimensional supermanifolds_ in _Supersymmetry and Quantum Field Theory_ ([[Dmitry Volkov]] memorial volume) 
  Springer-Verlag, 1998, Lecture Notes in Physics, 509 , J. Wess and V. Akulov (editors)([arXiv:hep-th/9706003](http://arxiv.org/abs/hep-th/9706003))

  _Theory of $(k \oplus l|q)$-dimensional supermanifolds_ Sel. math., New ser. 6 (2000) 471 - 486



[[!redirects super Cartesian spaces]]

[[!redirects Cartesian superspace]]
[[!redirects Cartesian superspaces]]

[[!redirects super cartesian space]]
[[!redirects super cartesian spaces]]

[[!redirects super-Cartesian space]]

[[!redirects super Euclidean space]]
[[!redirects super Euclidean spaces]]
[[!redirects super-Euclidean space]]
[[!redirects super-Euclidean spaces]]

[[!redirects super formal Cartesian space]]
[[!redirects super formal Cartesian spaces]]

[[!redirects SuperCartSp]]

[[!redirects SuperFormalCartSp]]
[[!redirects SuperFormalCartSpace]]
