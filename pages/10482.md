
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--

<center>
<img src="https://ncatlab.org/nlab/files/GrassmannGradedCommutativityI.jpg" width="460">
</center>
<center>
<img src="https://ncatlab.org/nlab/files/GrassmannGradedCommutativityII.jpg" width="460">
</center>


> from [Grassmann 1844, p. 61 and 84](Ausdehnungslehre#Grassmann44)



#Contents#
* table of contents
{:toc}




## Idea

Discussion of [[superalgebra]] and [[supergeometry]] involves, by definition, crucial minus signs appearing in certain expressions. While there is a systematic rule for these, when superalgebra/supergeometry is combined with other topics that crucially involve their own signs, such as [[homological algebra]], or ordering of terms, such as in [[noncommutative algebra]], then the combined sign rule may appear intricate. This page here is meant to explicitly list two equivalent sign rules for easy reference. We follow ([Deligne-Freed 99](#DeligneFreed99)) which has the same goal.



The main point to notice is that for algebraic terms that have both a [[homological algebra|homological degree]] $n \in \mathbb{Z}$ and a super-degree $\sigma \in \mathbb{Z}_2$ the "internalization sign rule" for the sign when exchanging two such elements is

$$
  \left(
    \left(
      n_1, \sigma_1
    \right)
    ,
    \left(
      n_2, \sigma_2
    \right)
  \right)
   \;\mapsto\;
   (-1)^{n_1 n_2 + \sigma_2 \sigma_2}
   \,.
$$

(e.g. [Castellani-D'Auria-Fr&#233; 91, (II.2.109)](#CastellaniDAuriaFre91), [Bonora-Bregola-Lechner-Pasti-Tonin 87, beginning of section 2](#BonoraBregolaLechnerPastiTonin87))

This we discuss below at _[The sign rule from internalization](#TheSignRuleFromInternalization)_.

Parts of the literature however adops another sign rule, given by

$$
  \left(
    \left(
      n_1, \sigma_1
    \right)
    ,
    \left(
      n_2, \sigma_2
    \right)
  \right)
   \;\mapsto\;
   (-1)^{(n_1 + \sigma_1)(n_2 + \sigma_2)}
   \,.
$$

This we discuss below in _[The super odd sign rule](#SuperOddConvention)_.

In [Deligne-Morgan 99](#DeligneMorgan99), the two sign rules are referred to as _Deligne's convention_ (for the internalization rule) and _Bernstein's convention_ (for the super odd sign rule).

[[!include sign rules in homological superalgebra -- table]]


## The sign rule from internalization
 {#TheSignRuleFromInternalization}

Here and in the following we adopt the perpective that [[homological algebra]] in [[superalgebra]] is concerned with the study of [[chain complexes]] [[internalization|internal]] to the [[symmetric monoidal category]] of [[super vector spaces]] ([Deligne 90](#Deligne90)) or equivalently internal to the [[topos]] over [[superpoints]] ([Schwarz 84](#Schwarz84)). This means that there are two contributions to the sign when exchanging two terms, one from the cohomological grading, one from the super-grading. This is "the sign rule" also used for instance in  ([Castellani-D'Auria-Fr&#233; 91, equation (II.2.106)](#CastellaniDAuriaFre91), [Bonora-Bregola-Lechner-Pasti-Tonin 87](#BonoraBregolaLechnerPastiTonin87) [Deligne-Freed 99, section 6](#DeligneFreed99)). 

There is however also a different sign rule use in the literature, the relation to which we discuss [below](#SuperOddConvention).


### Differential forms on supermanifolds
 {#DifferentialFormsOnSupermanifolds}

We discuss the sign rules for the [[de Rham algebra]] of [[differential forms]] on a [[supermanifold]] ([[superdifferential forms]]), which is a [[differential graded-commutative superalgebra]]. 


For $p,q \in \mathbb{N}$, let $\mathbb{R}^{p|q}$ the [[super Cartesian space]] of [[dimension]] $(p|q)$. This is the [[supermanifold]] defined by the fact that its [[algebra of functions]] is freely generated, as a [[smooth superalgebra]] by even-graded [[coordinate]]-functions $\langle \{x^a\}_{1}^p$ and odd-graded coordinate function $\{ \theta^\alpha\}_{\alpha= 1}^q$

$$
  C^\infty(\mathbb{R}^{p|q}) = \langle \{x^a\}_{1}^p, \{ \theta^\alpha\}_{\alpha= 1}^q \rangle
  \,.
$$

Accordingly, by the discussion at _[[Kähler forms]]_, the [[de Rham complex]] of [[differential forms]] on $\mathbb{R}^{p|q}$ is freely generated as a super-[[module]] over the [[smooth superalgebra]] $C^\infty(\mathbb{R}^{p|q})$ by expressions of the form $\mathbf{d}x^{a_1} \wedge \cdots \wedge \mathbf{d}x^{a_k} \wedge \mathbf{d}\theta^{\alpha_1} \wedge \cdots \wedge \mathbf{d}\theta^{\alpha_l}$.

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

| $\phantom{A}$generator$\phantom{A}$ | $\phantom{A}$bi-degree$\phantom{A}$ |
|--|--|
| $\phantom{A}$$x^a$$\phantom{A}$ | $\phantom{A}$(0,even)$\phantom{A}$ |
| $\phantom{A}$$\theta^\alpha$$\phantom{A}$ | $\phantom{A}$(0,odd)$\phantom{A}$ |
| $\phantom{A}$$\mathbf{d}$$\phantom{A}$ | $\phantom{A}$(1,even)$\phantom{A}$ |

Here the last line means that we have

| $\phantom{A}$generator$\phantom{A}$ | $\phantom{A}$bi-degree$\phantom{A}$ |
|--|--|
| $\phantom{A}$$x^a$$\phantom{A}$ | $\phantom{A}$(0,even)$\phantom{A}$ |
| $\phantom{A}$$\theta^\alpha$$\phantom{A}$ | $\phantom{A}$(0,odd)$\phantom{A}$ |
| $\phantom{A}$$\mathbf{d}x^a$$\phantom{A}$ | $\phantom{A}$(1,even)$\phantom{A}$ |
| $\phantom{A}$$\mathbf{d}\theta^\alpha$$\phantom{A}$ | $\phantom{A}$(1,odd)$\phantom{A}$ |


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

1. there is a "cohomological sign" which for commuting an $n_1$-forms past an $n_2$-form is $(-1)^{n_1 n_2}$;

1. in addition there is a "super-grading" sich which for commuting a $\sigma_1$-graded coordinate function past a $\sigma_2$-graded coordinate function (possibly under the de Rham differential) is $(-1)^{\sigma_1 \sigma_2}$.


Some examples:

| $\phantom{A}$[[signs in supergeometry|sign rule]]$\phantom{A}$  | $\phantom{A}$[Deligne's](signs+in+supergeometry#TheSignRuleFromInternalization)$\phantom{A}$ | [Bernstein's](signs+in+supergeometry#SuperOddConvention)$\phantom{A}$ | 
|---|------------------|-------------------|
| $\phantom{A}$$x^{a} \; x^{b} =$ | $\phantom{A}$$+ x^{b} \; x^{a}$$\phantom{A}$ | $\phantom{A}$$+ x^{b} \; x^{a}$$\phantom{A}$ | 
| $\phantom{A}$$x^a \;\theta^\alpha =$$\phantom{A}$ | $\phantom{A}$$+ \theta^\alpha \; x^a$$\phantom{A}$ | $\phantom{A}$$+ \theta^\alpha \; x^a$$\phantom{A}$ | 
| $\phantom{A}$$\theta^{\alpha} \; \theta^{\beta} =$$\phantom{A}$ | $\phantom{A}$$- \theta^{\beta} \; \theta^{\alpha}$$\phantom{A}$ | $\phantom{A}$$ - \theta^{\beta} \; \theta^{\alpha}$$\phantom{A}$ | 
| $\phantom{A}$$x^{a} (\mathbf{d}x^{a}) =$$\phantom{A}$ | $\phantom{A}$$+ (\mathbf{d}x^{b}) x^{a}$$\phantom{A}$ | $\phantom{A}$$+ (\mathbf{d}x^{b}) x^{a}$$\phantom{A}$ |
| $\phantom{A}$$\theta^\alpha (\mathbf{d}x^a) =$$\phantom{A}$ | $\phantom{A}$$+ (\mathbf{d}x^a) \theta^\alpha$$\phantom{A}$ | $\phantom{A}$${\color{blue}{-}} (\mathbf{d}x^a) \theta^\alpha$$\phantom{A}$ | 
| $\phantom{A}$$\theta^{\alpha} (\mathbf{d}\theta^{\beta})  = $$\phantom{A}$ | $\phantom{A}$$- (\mathbf{d}\theta^{\beta}) \theta^{\alpha}$$\phantom{A}$ | $\phantom{A}$${\color{blue}{+}} (\mathbf{d}\theta^{\beta}) \theta^{\alpha}$$\phantom{A}$ | 
| $\phantom{A}$$ (\mathbf{d}x^{a}) (\mathbf{d} x^{b}) =$$\phantom{A}$ |  $\phantom{A}$$- (\mathbf{d} x^{b}) (\mathbf{d} x^{a})$$\phantom{A}$ | $\phantom{A}$$ - (\mathbf{d} x^{b}) (\mathbf{d} x^{a})$$\phantom{A}$ |
| $\phantom{A}$$ (\mathbf{d}x^a) (\mathbf{d} \theta^{\alpha}) =$$\phantom{A}$ | $\phantom{A}$$ - (\mathbf{d}\theta^{\alpha}) (\mathbf{d} x^a) $$\phantom{A}$ | $\phantom{A}$$ {\color{blue}{+}} (\mathbf{d}\theta^{\alpha}) (\mathbf{d} x^a) $$\phantom{A}$ |
| $\phantom{A}$$(\mathbf{d}\theta^{\alpha}) (\mathbf{d} \theta^{\beta}) =$ | $\phantom{A}$$ + (\mathbf{d}\theta^{\beta}) (\mathbf{d} \theta^{\alpha})$$\phantom{A}$ | $\phantom{A}$$ + (\mathbf{d}\theta^{\beta}) (\mathbf{d} \theta^{\alpha})$$\phantom{A}$ |
{: style='margin:auto'}

### Cohomology of super Minkowski spacetime

The above signs rules for [[differential forms on supermanifolds]] directly translate to the signs rule for [[super Lie algebra]] [[Lie algebra cohomology]], by the identification of elements in the [[Chevalley-Eilenberg algebra]] with the [[left invariant differential forms]] on the corresponding [[super Lie group]].

We discuss now the [[Chevalley-Eilenberg algebra]] of [[super Minkowski spacetime]], regarded as a [[super translation Lie algebra]], equivalently as the [[quotient]] of the [[quotient]] of the 
[[super Poincaré Lie algebra]] by the [[Lorentz Lie algebra]].

This is the sub-algebra of the [above](#DifferentialFormsOnSupermanifolds) de Rham complex of the [[left invariant differential forms]]:

$$
  CE(\mathbb{R}^{d-1,1;N})
  =
  \Omega^\bullet_{li}(\mathbb{R}^{d-1,1;N})
  \hookrightarrow
  \Omega^\bullet(\mathbb{R}^{d-1,1;N})
  \,.
$$

With the [above](#DifferentialFormsOnSupermanifolds) notation these are

$$
  \psi^\alpha \coloneqq \mathbf{d}\theta^\alpha
$$

$$
  e^a \coloneqq \mathbf{d}x^a + \bar{\theta} \Gamma^a \mathbf{d}\theta
  \,.
$$

With the [above](#DifferentialFormsOnSupermanifolds) sign rules it follows that


$$
  e^{a_1} \wedge e^{a_2} = + e^{a_2} \wedge e^{a_1}
$$

$$
  e^{a} \wedge \psi^\alpha = - \psi^\alpha \wedge e^a
$$

$$
  \psi^{\alpha_1} \wedge \psi^{\alpha_2}
  = 
  + 
  \psi^{\alpha_2} \wedge \psi^{\alpha_1}
  \,.
$$

### Super Lie algebra cohomology

More generally, since the super-[[Chevalley-Eilenberg algebra]] of a [[super Lie algebra]] is identified with the [[left invariant differential forms]] on the corresponding [[super Lie group]], the signs from the super de Rham complex [above](#DifferentialFormsOnSupermanifolds) induce the cotresponding sign rule for the computation of super-[[Lie algebra cohomology]].

### Presheaves on superpoints

Write $Superpoint$ for the [[category]] of [[superpoints]], the [[opposite category]] of that of real finitely-generated [[Grassmann algebras]]. 

We list the terms with crucial signs that appear when regarding [[superalgebra]] as algebra [[internalization|internal]] to the [[presheaf topos]] over [[superpoints]] (see at _[[super infinity-groupoid]]_ for background).

#### Super Lie algebras

Given a [[super Lie algebra]] $\mathfrak{g}$, for each [[superpoint]] $\mathbb{R}^{0|q}$ write

$$
  \mathbb{g}(\mathbb{R}^{0|q})
  \coloneqq
  \left(
   \mathfrak{g}\otimes C^\infty(\mathbb{R}^{0|q})
  \right)_{even}
  \in Vect_{\mathbb{R}}
$$

for the [[vector space]] which is the even-degree part of the [[tensor product]] of the underlying [[vector spaces]] of $\mathfrak{g}$ and of the [[Grassmann algebra]] $C^\infty(\mathbb{R}^{0|q})$.

Here if $\{e_a, \psi_\alpha\}$ is a [[basis]] for $\mathfrak{g}$ with $\{e_a\}$ a basis for $\mathfrak{g}_{even}$ and $\{\psi_\alpha\}$ a basis for $\mathfrak{g}_{odd}$, and if we write $\{\epsilon^i\}_{i = 1}^q$ for the generators of $C^\infty(\mathbb{R}^{0|q})$, then $\mathbb{g}(\mathbb{R}^{0|q})$ is generated from elements of the form

$$
  e_a, \; e_a \epsilon^{i_1} \epsilon^{i_2},\;
  e_a \epsilon^{i_1} \epsilon^{i_2} \epsilon^{i_3} \epsilon^{i_4}
  ,\;
  \cdots
$$

and

$$
  \psi_\alpha \epsilon^{i_1} ,\;
  \psi_\alpha \epsilon^{i_1} \epsilon^{i_2} \epsilon^{i_3} 
  ,\;
  \cdots
  \,.
$$

The [[Lie bracket]] on the ordinary vector space $\mathfrak{g}(\mathbb{R}^{0|q})$ is defined on elements 

$$
  x_i \kappa_i \in 
  \left(
   \mathfrak{g}\otimes C^\infty(\mathbb{R}^{0|q})
  \right)_{even}
$$ 

by the formula

$$
  [ x_1 \kappa_1 , x_2 \kappa_2]_{\mathfrak{g}(\mathbb{R}^{0|q})} 
  \coloneqq
  [x_1, x_2]_{\mathfrak{g}} \kappa_1 \kappa_2
  \,.
$$

Some examples:

$$
  [e_{a_1}, e_{a_2}]_{\mathfrak{g}(\mathbb{R}^{0|q})}
  = 
  [e_{a_1}, e_{a_2}]_{\mathfrak{g}}
$$

$$
  [e_{a}, \psi_{\alpha} \epsilon^1]_{\mathfrak{g}(\mathbb{R}^{0|q})}
  = 
  [e_{a}, \psi_{\alpha}]_{\mathfrak{g}} \epsilon^1
$$

$$
  [\psi_{\alpha} \epsilon^1, e_a]_{\mathfrak{g}(\mathbb{R}^{0|q})}
  = 
  [\psi_{\alpha}, e_a]_{\mathfrak{g}} \epsilon^1
$$

From this and from the ordinary skew-symmetry of the [[Lie bracket]] in $\mathfrak{g}(\mathbb{R}^{0|q})$ follows that also in the [[super Lie algebra]] we have 

$$
  [e_a, \psi_{\alpha}] = - [\psi_{\alpha}, e_a]_{\mathfrak{g}}
  \,.
$$

Next, from

$$
  [\psi_{\alpha_1} \epsilon^1, \psi_{\alpha_2} \epsilon^2]_{\mathfrak{g}(\mathbb{R}^{0|q})}
  = 
  [\psi_{\alpha_1}, \psi_{\alpha_2}]_{\mathfrak{g}} \epsilon^1 \epsilon^2
$$

$$
  [\psi_{\alpha_2} \epsilon^2, \psi_{\alpha_1} \epsilon^1]_{\mathfrak{g}(\mathbb{R}^{0|q})}
  = 
  [\psi_{\alpha_2}, \psi_{\alpha_1}]_{\mathfrak{g}} \epsilon^2 \epsilon^1
$$

and the fact that $\epsilon^1  \epsilon^2 = - \epsilon^2  \epsilon^1$ it follows that in the [[super Lie algebra]]

$$
  [\psi_{\alpha_1}, \psi_{\alpha_2}]_{\mathfrak{g}}
  =
  +
  [\psi_{\alpha_2}, \psi_{\alpha_1}]_{\mathfrak{g}}
  \,.
$$

#### Chevalley-Eilenberg algebra

Given a [[super Lie algebra]] $\mathfrak{g}$ as above, 
the [[tensor product]] $\mathfrak{g}\otimes C^\infty(\mathbb{R}^{0|1})$ is the [[free construction|free]] $C^\infty(\mathbb{R}^{0|q})$-[[module]] generated from the [[super vector space]] underlying $\mathfrak{g}$.

(...)

$$
  CE_{C^\infty(\mathbb{R}^{0|q})}( \mathfrak{g}(C^\infty(\mathbb{R}^{0|q}) )_{even}
  \,.
$$

(...)

$$
  (\psi^{\alpha_1} \epsilon^1) 
  \wedge
  (\psi^{\alpha_2} \epsilon^2)
  =
  -  
  (\psi^{\alpha_2} \epsilon^2) 
  \wedge
  (\psi^{\alpha_1} \epsilon^1)
  = 
  \psi^{\alpha_1}
    \wedge 
  \psi^{\alpha^2}
  \epsilon^1 \epsilon^2
$$

(...)

## The super odd sign rule
 {#SuperOddConvention}

In all of the above we used the sign rule induced by setting up all mathematical concepts [[internalization|internal]] to the [[symmetric monoidal category]] of [[super vector spaces]] or [[internalization|internal]] the [[topos]] over [[superpoints]].

There is another sign convention in the literature, for instance in (...). In this convention one considers the map

$$
  ((-)+(-))_{mod\, 2}
  \;\colon\;
  \mathbb{Z} \times \mathbb{Z}_2
  \longrightarrow
  \mathbb{Z}_2
$$

to induce a single $\mathbb{Z}_2$-grading and then lets all signs be induced by that. 

This can motivated from regarding the $\mathbb{Z}_2$-graded [[de Rham complex]] of a [[supermanifold]] as the [[algebra of functions]] on its odd-shifted tangent bundle

$$
  \Omega^\bullet(X) \simeq_{\mathbb{Z}_2} C^\infty(T[1]X)
  \,.
$$

In this convention a term such as $\mathbf{d}\theta^\alpha$ of bidegree $(1,1)$ has single degree $0$ and hence _commutes with every other term_.

### Differential forms on a supermanifold in the super odd convention
 {#DifferentialFormsInSuperOddConvention}

In this other convention the signs in the [[de Rham complex]] of the [[super Cartesian space]] $\mathbb{R}^{p|q}$ are induced as follows:


$$
  (s.o.): \;\;\; x^{a_1} x^{a_2} = + x^{a_2} x^{a_1}
$$

$$
  (s.o.): \;\;\;x^a \theta^\alpha = + \theta^\alpha x^a
$$

$$
  (s.o.): \;\;\;\theta^{\alpha_1} \theta^{\alpha_2}
  =
  +
  \theta^{\alpha_2} \theta^{\alpha_1}
$$

$$
  (s.o.): \;\;\;x^{a_1} (\mathbf{d}x^{a_2}) = + (\mathbf{d}x^{a_2}) x^{a_1}
$$


$$
  (s.o.): \;\;\;\theta^\alpha (\mathbf{d}x^a) = + (\mathbf{d}x^a) \theta^\alpha
$$

$$
  (s.o.): \;\;\;
  \theta^{\alpha_1} (\mathbf{d}\theta^{\alpha_2})
   =
   + (\mathbf{d}\theta^{\alpha_2}) \theta^{\alpha_1}
$$

$$
  (s.o.): \;\;\;
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
  (s.o.): \;\;\;
  \mathbf{d}x^a
  \wedge
  \mathbf{d} \theta^{\alpha}
  =
  +
  \mathbf{d}\theta^{\alpha}
  \wedge
  \mathbf{d} x^a
$$

$$
  (s.o.): \;\;\;
  \mathbf{d}\theta^{\alpha_1}
  \wedge
  \mathbf{d} \theta^{\alpha_2}
  =
  +
  \mathbf{d}\theta^{\alpha_2}
  \wedge
  \mathbf{d} \theta^{\alpha_1}
$$


## Relation between the two sign rules

### Strong symmetric monoidal equivalence
 {#StrongSymmetricMonoidalEquialence}

The two sign rules correspond to two different [[symmetric monoidal category|symmetric braiding]]-[[structures]] on the [[monoidal category]] $Ch(SuperVect)$ of [[chain complexes]] of [[super vector spaces]]. The corresponding two kinds of [[differential graded-commutative superalgebras]] are the [[commutative monoid objects]] with respect to these two choices.

We now show that the two braidings are equivalent (Prop. \ref{EquivalenceTwoSymmetricMonoidalStructuresOnChSuperVect} below), which immediately implies that the two categories of differential graded-commutative algebras are equivalent.

$\,$

+-- {: .num_defn #ChainComplexesOfSuperVectorSpaces}
###### Definition
**([[chain complexes]] of [[super vector spaces]])**

Write $Ch(SuperVect)$ for the [[category of chain complexes]] inside the category of [[super vector spaces]].

Hence for $V_\bullet \in Ch(SuperVect)$ an [[object]], for each $n \in \mathbb{Z}$ there is a [[super vector space]] 

$$
  V_n = (V_n)_{even} \oplus (V_n)_{odd} \;\in SuperVect
$$

where we write the elements of the [[group of order two]] as $\mathbb{Z}/2 =\{even, odd\}$, with $even$ being the [[neutral element]].

Hence we may regard any $V_\bullet \in Ch(SuperVect)$ equivalently as a $\mathbb{Z} \times (\mathbb{Z}/2)$-[[graded object|graded]] [[vector space]] equipped with a [[differential]] of degree $(1,even)$. For $v \in V$ an element in definite ("homogeneous") bi-degree, we denote this degree by

\[
  \label{BidegreeOnChainComplexOfSuperVectorSpaces}
  deg(v) \coloneqq (n_v, \sigma_v) \;\in\; \mathbb{Z} \times (\mathbb{Z}/2) 
  \,.
\]

The category $Ch(SuperVect)$ becomes a [[monoidal category]] under the [[tensor product of chain complexes]] applied to the tensor product of [[super vector spaces]]. This means that for $V, W \in Ch(SuperVect)$, the [[differential]] on a homogeneously graded element $v \otimes w \in V \otimes W$ is

$$
  \partial(v \otimes w)
  \;=\;
  (\partial v) \otimes w 
  +
  (-1)^{ n_v } v \otimes \partial w
  \,.
$$

=--

+-- {: .num_prop #SymmetricStructureOnCategoryOfChainComplexesOfSuperVectorSpaces}
###### Proposition
**([[symmetric monoidal category|symmetric monoidal]] [[structure]] on [[category of chain complexes of super vector spaces]])**

The [[monoidal category|monoidal]] [[category of chain complexes of super vector spaces]] $(Ch(SuperVect), \otimes)$ from Def. \ref{ChainComplexesOfSuperVectorSpaces} becomes a [[symmetric monoidal category|symmetric monoidal]] with each of the following two [[braiding]] [[isomorphisms]], defined on tensor products of elements in homogenous bi-degree (eq:BidegreeOnChainComplexOfSuperVectorSpaces) as follows:

1. $\tau_{Deligne} \;\colon\; v \otimes w \mapsto (-1)^{ (n_v n_w + \sigma_v \sigma_w) } w \otimes v$;

1. $\tau_{Bernst} \;\colon\; v \otimes w \mapsto (-1)^{ (n_v + \sigma_v) (n_w + \sigma_w) } w \otimes v$.

Here in the exponents we are using the canonical [[ring]]-[[structure]] on the [[integers]] $\mathbb{Z}$ and on the [[prime field]] $\mathbb{Z}/2 = \mathbb{F}_2$, the implicit [[ring homomorphism]] $\mathbb{Z} \to \mathbb{Z}/2$ and we understand that $(-1)^{even} = 1$ and $(-1)^{odd} = -1$.

=--

+-- {: .proof}
###### Proof

Since the expressions for both sign factors are symmetric in $v$ and $w$ in both cases, it is clear that $\tau_{w,v} \circ \tau_{v,w} = id_{v \otimes w}$ in both cases. Hence if $\tau$ is indeed a [[braiding]], then it is [[symmetric monoidal category|symmetric]].

To see that $\tau$ is indeed a [[braiding]] in each case, we need to check the [[hexagon identities]]

$$
  \array{
   (V_1 \otimes V_2) \otimes V_3 
   &\overset{a_{V_1, V_2, V_3}}{\longrightarrow}&
   V_1 \otimes (V_2 \otimes V_3)
   &\overset{\tau_{V_1,V_2 \otimes V_3}}{\longrightarrow}&
   (V_2 \otimes V_3) \otimes V_1
   \\
   \Big\downarrow{}^{\tau_{V_1,V_2}\otimes Id}
   &&&&
   \Big\downarrow{}^{a_{V_2,V_3,V_1}}
   \\
   (V_2 \otimes V_1) \otimes V_3
   &\overset{a_{V_2,V_1,V_3}}{\longrightarrow}&
   V_2 \otimes (V_1 \otimes V_3)
   &\overset{Id \otimes \tau_{V_1,V_3}}{\longrightarrow}&
   V_2 \otimes (V_3 \otimes V_1)
  }
$$

and

$$
  \array{
   V_1 \otimes (V_2 \otimes V_3) 
   &\overset{a^{-1}_{V_1,V_2,V_3}}{\longrightarrow}&
   (V_1 \otimes V_2) \otimes V_3
   &\overset{\tau_{V_1 \otimes V_2, V_3}}{\longrightarrow}&
   V_3 \otimes (V_1 \otimes V_2)
   \\
   \Big\downarrow{}^{id \otimes \tau_{V_2,V_3}}
   &&&&
   \Big\downarrow{}^{a^{-1}_{V_3,V_1,V_2}}
   \\
   V_1 \otimes (V_3 \otimes V_2)
   &\overset{a^{-1}_{V_1,V_3,V_2}}{\longrightarrow}&
   (V_1 \otimes V_3) \otimes V_2
   &\overset{\tau_{V_1,V_3} \otimes id}{\longrightarrow}&
   (V_3 \otimes V_1) \otimes V_2
  }
  \,.
$$

Since $\tau$ differs only by multiplication by a sign from the standard symmetric braiding on the [[category of vector spaces]], which does satisfy its hexagon identities, it just remains to check that these sign factors picked up in going both ways around these diagrams agree. 

Hence for $\tau_{Deligne}$ the two hexagon identities are equivalent to the conditions

$$
  (-1)^{ n_1 (n_2 + n_3) + \sigma_1( \sigma_2 + \sigma_3 )  }
  \;=\;
  (-1)^{ n_1 n_2 + \sigma_1 \sigma_2 + n_1 n_3 + \sigma_1 \sigma_3 }
$$

and

$$
  (-1)^{ (n_1 + n_2) n_3 + (\sigma_1 + \sigma_2) \sigma_3 }
  \;=\;
  (-1)^{ n_1 n_3 + \sigma_1 \sigma_3 + n_2 n_3 + \sigma_2 \sigma_3 }
$$

while for $\tau_{Bernst}$ they are equivalent to the conditions

$$
  (-1)^{ (n_1 + \sigma_1)( n_2 + \sigma_2 + n_3 + \sigma_3  ) }
  \;=\;
  (-1)^{ (n_1 + \sigma_1)(n_2 + \sigma_2) + (n_1 + \sigma_1)(n_3 + \sigma_3)  }
$$

and

$$
  (-1)^{ (n_1 + \sigma_1 + n_2 + \sigma_2)(n_3 + \sigma_3) }
  \;=\;
  (-1)^{ (n_1 + \sigma_1)(n_3 + \sigma_3) + (n_2 + \sigma_2)(n_3 + \sigma_3) }
$$

for all triples of bi-degrees $(n_i, \sigma_i) \in \mathbb{Z} \times (\mathbb{Z}/2)$.

In both cases this holds because already the relevant [[exponents]] are equal in each case, by the [[distributive law]] for [[multiplication]] and [[addition]] in $\mathbb{Z}/2 = \mathbb{F}_2$.

=--

+-- {: .num_prop #EquivalenceTwoSymmetricMonoidalStructuresOnChSuperVect}
###### Proposition
**(the two [[symmetric monoidal category|symmetric monoidal]] [[structures]] on the [[category of chain complexes of super vector spaces]] are equivalent)**


The two [[symmetric monoidal category]] [[structures]] $\tau_{Deligne}$ and $\tau_{Bernst}$ on the [[monoidal category|monoidal]] [[category of chain complexes of super vector spaces]] $(Ch(SuperVect), \otimes)$ from Prop. \ref{SymmetricStructureOnCategoryOfChainComplexesOfSuperVectorSpaces} are equivalent

$$
  \tau_{Deligne}
  \;\simeq\;
  \tau_{Bernst}
$$

in that the [[identity functor]] $Ch(SuperVect) \overset{\mu}{\longrightarrow} Ch(SuperVect)$ equipped with the following monoidal [[natural isomorphism]] 

$$
  \array{
    id(V) \otimes id(W) \overset{\mu}{\longrightarrow} id(V \otimes W)
    \\
    v \otimes w
    \;\mapsto\;
    (-1)^{ n_v \sigma_w  } \, v \otimes w
  }
$$

(the second line shows its action on elements of homogeneous bidegree $(n,\sigma) \in \mathbb{Z} \times (\mathbb{Z}/2)$)

becomes a [[nLab:strong monoidal functor|strong]] [[symmetric monoidal functor]] 

$$
  (Ch(SuperVect), \otimes, \tau_{Deligne})
  \underoverset{\simeq}{(id,\mu)}{\longrightarrow}
  (Ch(SuperVect), \otimes, \tau_{Bernst})
  \,.
$$

=--


+-- {: .proof}
###### Proof

First to see that we have a [[strong monoidal functor]], we need to check the [[associativity]] condition


$$
  \array{
    (id(V_1) \otimes id(V_2)) \otimes id(V_3)
      &\underoverset{\simeq}{a_{id(V_1),id(V_2),id(V_3)}}{\longrightarrow}&
    id(V_1) \otimes( id(V_2)\otimes id(V_3) )
    \\
    {}^{\mathllap{\mu_{V_1,V_2} \otimes id}}\downarrow 
      && 
    \Big\downarrow{}^{\mathrlap{id\otimes \mu_{V_2,V_3}}}
    \\
    id(V_1 \otimes V_2) \otimes id(V_3)
     &&
    id(V_1) \otimes id(V_2 \otimes V_3)
    \\
    {}^{\mathllap{\mu_{V_1 \otimes V_2 , V_3} } }\Big\downarrow 
      && 
    \Big\downarrow^{\mathrlap{\mu_{ V_1, V_2 \otimes V_3  }}}
    \\
    id( ( V_1 \otimes V_2 ) \otimes V_3  )
      &\underset{id(a_{V_1,V_2,V_3})}{\longrightarrow}&
    id( V_1 \otimes ( V_2 \otimes V_3 ) )
  }
  \,,
$$

and the [[unitality]] conditions


$$
  \array{
    1 \otimes id(V)
      &\overset{\epsilon \otimes id}{\longrightarrow}&
    id(1) \otimes id(V)
    \\
    {}^{\mathllap{\ell_{id(V)}}}\Big\downarrow 
      && 
    \Big\downarrow{}^{\mathrlap{\mu_{1, V }}}
    \\
    id(V) 
      &\overset{id(\ell_V )}{\longleftarrow}&
    id(1 \otimes V  )
  }
$$

and  

$$
  \array{
    id(V) \otimes  1
      &\overset{id \otimes \epsilon }{\longrightarrow}&
    id(V) \otimes  id(1) 
    \\
    {}^{\mathllap{r_{id(V)}}}\Big\downarrow 
      && 
    \Big\downarrow{}^{\mathrlap{\mu_{V, 1 }}}
    \\
    id(V) 
      &\overset{F(r_V )}{\longleftarrow}&
    id(V \otimes 1  )
  }
  \,,
$$

Since $\mu$ differs from the trivial monoidal isomorphism only by the sign factor, this is equivalent to the condition that the sign factors picked up in going both ways around these diagrams agree.

For [[associativity]] this is the condition

$$
  (-1)^{
    n_1 \sigma_2 + (n_1 + n_2)\sigma_3
  }
  \;=\;
  (-1)^{
    n_2 \sigma_3 + n_1 (\sigma_2 + \sigma_3)
  }
$$

for all bi-degrees $(n_i, \sigma_i) \in \mathbb{Z} \times (\mathbb{Z}/2)$,
which holds, because it already holds for the [[exponents]] themselves, as an identity in $\mathbb{Z}/2 =\mathbb{F}_2$.

For the [[unitality]] condition this is the statement that the sign given by $\mu_{1,x}$ and $\mu_{x,1}$ is the the trivial sign $(-1)^0 = 1$. This is indeed the case because the [[tensor unit]] is in degree $0 = (0,even) \in \mathbb{Z} \times (\mathbb{Z}/2)$.

Now to see that we have a [[symmetric monoidal functor]], we need to show that it intertwines the two [[symmetric monoidal category|symmetruc]] [[braiding]] [[isomorphisms]]


$$
  \array{
    id(V_1) \otimes id(V_2) 
      &\stackrel{\tau_{Bernst}}{\longrightarrow}& id(V_2) \otimes id(V_1)
    \\
    {}^{\mathllap{\mu_{V_1,V_2}}}\Big\downarrow 
    && 
    \Big\downarrow{}^{\mathrlap{\mu_{V_2,V_1}}}
    \\
    id(V_1\otimes V_2) 
      &\overset{id(\tau_{Deligne})}{\longrightarrow}& if(W \otimes V)
  }
$$

As before, this is equivalent to a condition on the signs picked up both ways, which reads:

$$
  (-1)^{ (n_1 + \sigma_1)(n_2 + \sigma_2) + n_2 \sigma_1}
  \;=\;
  (-1)^{ n_1 \sigma_2 + n_1 n_2 + \sigma_1 \sigma_2 }
  \,.
$$

Inspection shows that this is indeed the case: 

The two signs of $\tau_{Deligne}$ and $\tau_{Bernst}$ differ by the "mixed terms" that are produced in [[distributivity|multiplying out]] $(n_v + \sigma_v)(n_w + \sigma_w)$ and these two mixed terms is just what the two occurences $\mu$ provides (using that $+1 = -1 \in \mathbb{F}_2$).


=--

$\,$

### Equivalence of super Lie algebra cohomology in both conventions
 {#EquivalenceOfSuperLieAlgebraCohomology}

The different choice of signs in the de Rham complex
[above](#DifferentialFormsInSuperOddConvention) affects the signs
of any super-[[Chevalley-Eilenberg algebra]], by the identification of elements in the CE-algebra with [[left invariant differential forms]] on the supegroup.

We show now that as [[chain complexes]] the two CE-algebras are [[quasi-isomorphism|quasi-isomorphic]] and hence do have the same [[cochain cohomology]], hence that the definition of super-[[Lie algebra cohomology]] is not affected by the different perspective on signs.

(This follows abstract from Prop. \ref{EquivalenceTwoSymmetricMonoidalStructuresOnChSuperVect}, but we spell it out concretely.)

A chain-isomorphism can be obtained as follows:

Write 

* $CE^\bullet$ for the [[cochain complex]] underlying the [[Chevalley-Eilenberg algebra]] with the signs given by 

  $$
    ((n_1, \sigma_1), (n_2, \sigma_2)) \mapsto (-1)^{n_1 n_2 + \sigma_1 \sigma_2}
  $$

* write $CE^\bullet_{\mathbb{Z}_2}$ for the cochain complex obtained with the sign rule 
 
  $$
    ((n_1, \sigma_1), (n_2, \sigma_2)) \mapsto (-1)^{(n_1 + \sigma_1)(n_2 + \sigma_2)}
    \,.
  $$

Say that a product of generators representing an element in $CE^k$ is in _normal order_ of all the $(\bullet,even)$-graded elements are left of the $(\bullet,odd)$-graded elements, schematically

$$
  e \wedge \cdots e \wedge \psi \wedge \cdots \psi
  \,.
$$

To define a [[linear map]] $CE^k  \longrightarrow CE^\bullet_{\mathbb{Z}_2}$ declare that elements in this normal form go to the elements given by the same expression. 

This defines a linear map in each degree $k$. Notice that this is _not_ a morphism of algebras, in any sense, but it _is_ a [[chain map]]. To see this, notice that acting with the [[differential]] which is of degree $(1,even)$ on a term of the form $e \wedge \cdots e \wedge \psi \wedge \cdots \psi$ produces a sum of such terms where in each summand one generator is replaced by a term of the form $d e$ or by $d \psi$, respectively. These are in turn themselves sums of elements of the form $e \wedge \cdots e \wedge \psi \wedge \cdots \psi$. By commuting them to the middle we see that the differential of the whole term is a sum of terms of the form

$$
  e \wedge \cdots \wedge e \wedge (d e) \wedge \psi \wedge \cdots \wedge \psi
$$

and

$$
  e \wedge \cdots \wedge e \wedge (d \psi)  \wedge \psi \wedge \cdots \wedge \psi
  \,.
$$

Now observe: 

1. for terms of the first type, the signs picked up by commuting $d e$ to the middle are by definition the same in $CE^\bullet$ and in $CE^\bullet_{\mathbb{Z}_2}$;

1. for terms of the second type there are a priori more signs picked up in $CE^\bullet$ than in $CE^\bullet_{\mathbb{Z}_2}$, namely one for every term $\psi$ that one commutes through. But as the differential first passes from the left into the string of $\psi$s and then $d \psi$ in turn is passed back to the left, these extra signs appear in even number and hence cancel out.

In summary this establishes a [[chain map]] $CE^\bullet \longrightarrow CE^\bullet_{\mathbb{Z}_2}$ which is an cochain [[isomorphism]] and hence in particular a [[quasi-isomorphism]], hence an [[isomorphism]] on [[cochain cohomology]].


## References

### Internalization sign rule


The [[internalization]] into the [[topos]] over [[superpoints]] is due to 

* {#Schwarz84} [[Albert Schwarz]], _On the definition of superspace_, Teoret. Mat. Fiz. (1984)  Volume 60,  Number 1, Pages 37&#8211;42, ([russian original pdf](http://www.mathnet.ru/links/b12306f831b8c37d32d5ba8511d60c93/tmf5111.pdf))

The internalization sign rule follows for instance from applying the construction of [[internalization|internal]] [[Grassmann algebras]] in the [[category]] of [[super vector space]] as discussed in 

* {#Deligne90} [[Pierre Deligne]], p. 165  _[[Catégories Tannakiennes]],  [[Grothendieck Festschrift]], vol. II, Birkh&#228;user Progress in Math. 87 (1990) pp.111-195.    
 
The corresponding internal sign rule appears for instance in 

* {#BonoraBregolaLechnerPastiTonin87} [[Loriano Bonora]], M. Bregola, [[Kurt Lechner]], [[Paolo Pasti]], [[Mario Tonin]], section 2 of _Anomaly-free supergravity and super-Yang-Mills theories in ten dimensions_, Nuclear Physics B
Volume 296, Issue 4, 25 January 1988 (<a href="http://dx.doi.org/10.1016/0550-3213(88)90402-6">doi:10.1016/0550-3213(88)90402-6</a>)


* {#CastellaniDAuriaFre91} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], equations (II.2.106) and (II.2.109) in _[[Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991)



* {#DeligneFreed99} [[Pierre Deligne]], [[Dan Freed]], _Sign manifesto_, 1999 ([pdf](http://publications.ias.edu/sites/default/files/79_SignManifesto.pdf), [[DeligneFreedSignManifesto.pdf:file]]) 
   
  which appears in
 
  * [[Pierre Deligne]], [[Daniel Freed]], _Supersolutions_ ([arXiv:hep-th/9901094](http://arxiv.org/abs/hep-th/9901094)).

    which in turn appears in 

    * [[Pierre Deligne|P. Deligne]], [[Pavel Etingof|P. Etingof]], [[Dan Freed|D.S. Freed]], L. Jeffrey, [[David Kazhdan|D. Kazhdan]], [[John Morgan]], [[David Morrison]], [[Edward Witten|E. Witten]] (eds.)  _[[Quantum Fields and Strings]], A course for mathematicians_, 2 vols. Amer. Math. Soc. Providence 1999. ([web version](http://www.math.ias.edu/qft))


And with explicit acknowledgement that there is also the alternative super odd sign rule in:

* {#DeligneMorgan99} [[Pierre Deligne]], [[John Morgan]], _Notes on supersymmetry_, remark 1.2.8 in [[NotesOnNotesOnSupersymmetry.pdf:file]]

  in [[Pierre Deligne|P. Deligne]], [[Pavel Etingof|P. Etingof]], [[Dan Freed|D.S. Freed]], L. Jeffrey, [[David Kazhdan|D. Kazhdan]], [[John Morgan]], [[David Morrison]], [[Edward Witten|E. Witten]] (eds.)  _[[Quantum Fields and Strings]], A course for mathematicians_, 2 vols. Amer. Math. Soc. Providence 1999. ([web version](http://www.math.ias.edu/qft))


* {#Freed01} [[Daniel Freed]], bottom of p. 48 in _Classical field theory and Supersymmetry_, IAS/Park City Mathematics Series Volume 11, 2001 ([pdf](https://www.ma.utexas.edu/users/dafr/pcmi.pdf))

### Super odd sign rule

* {#CarchediRoytenberg12} [[David Carchedi]], [[Dmitry Roytenberg]],  _Homological Algebra for Superalgebras of Differentiable Functions_ ([arXiv:1212.3745](https://arxiv.org/abs/1212.3745))

...


