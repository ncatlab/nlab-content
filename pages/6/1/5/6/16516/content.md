
> this entry contains one chapter of _[[geometry of physics]]_

> previous chapter: _[[geometry of physics -- manifolds and orbifolds|manifolds and orbifolds]]_

> next chapter: _[[geometry of physics -- BPS charges|BPS charges]]_


#Contents#
* table of contents
{:toc}

## **Supergeometry**

* [[supergeometry]]

* [[super-Cartan geometry]]

* [[super infinity-groupoid]]

* [[super formal smooth infinity-groupoid]]


### **Model layer**


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

(Here the hat in the lowest row indicates an [[extended super Minkowski spacetime]], which involves [[higher Cartan geometry]].)

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


The [[quotient]] of the [[super Poincaré Lie algebra]] by the [[Lorentz Lie algebra]] is [[super-Minkowski spacetime]] regarded as a [[super Lie algebra]]:

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


+-- {: .num_defn #CEAlgebraOfSuperPoincare}
###### Definition

The [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{iso}(\mathbb{R}^{d-1,1|N}))$ is generated by

* elements $\{e^a\}$ and $\{\omega^{ a b}\}$ of degree $(1,even)$

* and elements $\{\psi^\alpha\}$ of degree $(1,odd)$

with the differential defined by

$$
  d_{CE} \, \omega^{a b} = \omega^a{}_b \wedge \omega^{b c}
$$

$$
  d_{CE} \, e^{a } = \omega^a{}_b \wedge e^b + \bar \psi \Gamma^a \psi
$$

$$
  d_{CE} \, \psi = \frac{1}{4} \omega^{ a b} \Gamma_{a b} \psi
  \,.
$$

Discarding the terms involving $\omega$ here this is the CE algebra of the [[super translation algebra]] underlying [[super Minkowski spacetime]].

=--

In this way the super-Poincar&#233; Lie algebra and its extensions is usefully discussed for instance in ([D'Auria-Fr&#233; 82](#DAuriaFre82)) and in ([Azc&#225;rraga-Townsend 89](super+Minkowski+spacetime#AzcarragaTownsend89), [CAIB 99](super+Minkowski+spacetime##CAIB99)). In much of the literature instead the following equivalent notation is popular, which more explicitly involves the [[coordinates]] on [[super Minkowski space]].

+-- {: .num_remark }
###### Remark

The abstract generators in def. \ref{CEAlgebraOfSuperPoincare} are identified with [[left invariant 1-forms]] on the [[super-translation group]] (= [[super Minkowski space]]) as follows.

Let $(x^a, \theta^\alpha)$ be the canonical [[coordinates]] on the [[supermanifold]] $\mathbb{R}^{d|N}$ underlying the super translation group. Then the identification is 

* $\psi^\alpha = d \theta^\alpha$.

* $e^a = d x^a +  \overline{\theta} \Gamma^a d \theta$.

Notice that this then gives the above formula for the differential of the [[super-vielbein]] in def. \ref{CEAlgebraOfSuperPoincare} as

$$ 
  \begin{aligned}
    d e^a & = d (d x^a +  \overline{\theta} \Gamma^a d \theta)
    \\
    & =  d \overline{\theta}\Gamma^a d \theta
    \\
    & =  \overline{\psi}\Gamma^a \psi
  \end{aligned}
  \,.
$$


=--


+-- {: .num_remark #Supertorsion}
###### Remark

The term $\bar \psi \Gamma^a \psi$ is sometimes called the *[[supertorsion]]* of the [[super-vielbein]] $e$, because the defining equation

$$
  d_{CE} e^{a } -\omega^a{}_b \wedge e^b = \bar \psi \Gamma^a \psi
$$

may be read as saying that $e$ is [[torsion]]-free except for that term. Notice that this term is the only one that appears when the differential is applied to "Lorentz scalars", hence to object in $CE(\mathfrak{iso}(\mathbb{R}^{d-1,1\vert N}))$ which have "all indices contracted". See also at _[[torsion constraints in supergravity]]_.

Notably we have 

$$
  d \left( 
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

This remaining operation "$e \mapsto \Psi^2$" of the differential acting on Loretz scalars is sometimes denoted "$t_0$", e.g. in ([Bossard-Howe-Stelle 09, equation (8)](super+Minkowski+spacetime#BossardHoweStelle09)).

This relation is what govers all of the exceptional super Lie algebra cocycles that appear [below](#TheOldBraneScan): for some combinations of $(d,p,N)$ a [[Fierz identity]] implies that the term

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

is a [[cocycle]] in super [[Lie algebra cohomology]].

=--

#### Cohomology of super-Minkowski spacetime

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


##### The old brane scan 
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



##### The full brane scan 

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




###### The M5-brane




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

1. $d \mu_7 = 15 \, g_4 \wedge g_4$

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

given dually by $\psi^\alpha \mapsto \psi^\alpha$, $e^a \mapsto e^a$, $h_3 \mapsto 0$, $g_4 \mapsto 0$, is an equivalence of $L_\infty$-algebras. It factors the morphism $\mathfrak{m}2\mathfrak{brane} \longrightarrow \mathbb{R}^{10,1\vert \mathbf{32}}$ from def. \ref{m2braneLie3Algebra} through a morphism $\mathfrak{m}2\mathfrak{brane}  \longrightarrow \mathbb{R}^{10,1\vert \mathbf{32}}_{res}$ which on [[formal dual]] CE-elements is given by $g_4 \mapsto 0$ and by being the identity on all other generators.


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
    & {}_{\mathllap{\mu_4}}\searrow && \swarrow
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

###### The D-branes

(...)

##### Summary

[[!include brane scan]]


<div style="float:left;margin:0 10px 10px 0;"><img src="https://dl.dropboxusercontent.com/u/12630719/BraneBouquet.JPG" alt="the brane bouquet" /></div>

### **Semantics layer**

#### The modal operators

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

* {#DAuriaFre82}  [[Riccardo D'Auria]], [[Pietro Fré]]; _[[GeometricSupergravity.pdf:file]]_, Nuclear Physics B201 (1982) 101-140


* {#BLNPST97} [[Igor Bandos]], [[Kurt Lechner]], Alexei Nurmagambetov, [[Paolo Pasti]], [[Dmitri Sorokin]], Mario Tonin, _Covariant Action for the Super-Five-Brane of M-Theory_, Phys.Rev.Lett. 78 (1997) 4332-4334 ([arXiv:hep-th/9701149](http://arxiv.org/abs/hep-th/9701149))