
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Discussion of [[superalgebra]] and [[supergeometry]] involves, by definition, crucial minus signs appearing in certain expressions. While there is a systematic rule for these, when superalgebra/supergeometry is combined with other topics that crucially involve their own signs, such as [[homological algebra]], or ordering of terms, such as in [[noncommutative algebra]], then the combined sign rule may appear intricate. This page here is meant to explicitly list some common expressions with their signs, for easy reference. We follow the article ([Deligne-Freed 99](#DeligneFreed99)) which has the same goal.

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

(e.g. [Castellani-D'Auria-Fr&#233; 91, (II.2.109)](#CastellaniDAuriaFre91))

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


## The sign rule from internalization
 {#TheSignRuleFromInternalization}

Here and in the following we adopt the perpective that [[homological algebra]] in [[superalgebra]] is concerned with the study of [[chain complexes]] [[internalization|internal]] to the [[symmetric monoidal category]] of [[super vector spaces]] ([Deligne 90](#Deligne90)) or equivalently internal to the [[topos]] over [[superpoints]] ([Schwarz 84](#Schwarz84)). This means that there are two contributions to the sign when exchanging two terms, one from the cohomological grading, one from the super-grading. This is "the sign rule" also used for instance in  ([Castellani-D'Auria-Fr&#233; 91, equation (II.2.106)](#CastellaniDAuriaFre91), [Deligne-Freed 99, section 6](#DeligneFreed99)). 

There is however also a different sign rule use in the literature, the relation to which we discuss [below](#SuperOddConvention).


### Differential forms on supermanifolds
 {#DifferentialFormsOnSupermanifolds}

We discuss the sign rules for the [[de Rham complex]] of [[differential forms]] on a [[supermanifold]] ([[superdifferential forms]]). 


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

1. there is a "cohomological sign" which for commuting an $n_1$-forms past an $n_2$-form is $(-1)^{n_1 n_2}$;

1. in addition there is a "super-grading" sich which for commuting a $\sigma_1$-graded coordinate function past a $\sigma_2$-graded coordinate function (possibly under the de Rham differential) is $(-1)^{\sigma_1 \sigma_2}$.


Some examples:

$$
  x^{a_1} x^{a_2} = + x^{a_2} x^{a_1}
$$

$$
  x^a \theta^\alpha = + \theta^\alpha x^a
$$

$$
  \theta^{\alpha_1} \theta^{\alpha_2}
  =
  -
  \theta^{\alpha_2} \theta^{\alpha_1}
$$


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
  e^a \coloneqq \mathbf{d}x^a + \theta \Gamma^a \mathbf{d}\theta
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

### Equivalence of super Lie algebra cohomology in both conventions
 {#EquivalenceOfSuperLieAlgebraCohomology}

The different choice of signs in the de Rham complex
[above](#DifferentialFormsInSuperOddConvention) affects those
of any super-[[Chevalley-Eilenberg algebra]], by the identification of elements in the CE-algebra with [[left invariant differential forms]] on the supegroup.

We show that as [[chain complexes]] the two CE-algebras are [[quasi-isomorphism|quasi-isomorphic]] and hence do have the same [[cochain cohomology]], hence that the definition of super-[[Lie algebra cohomology]] is not affected by the different perspective on signs.

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

* {#CastellaniDAuriaFre91} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], equations (II.2.106) and (II.2.109) in _[[Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991)


* {#DeligneFreed99} [[Pierre Deligne]], [[Dan Freed]], _Sign manifesto_, 1999 ([pdf](http://publications.ias.edu/sites/default/files/79_SignManifesto.pdf)) 
   
  which appears in
 
  * [[Pierre Deligne]], [[Daniel Freed]], _Supersolutions_ ([arXiv:hep-th/9901094](http://arxiv.org/abs/hep-th/9901094)).

    which in turn appears in 

    * [[Pierre Deligne|P. Deligne]], [[Pavel Etingof|P. Etingof]], [[Dan Freed|D.S. Freed]], L. Jeffrey, [[David Kazhdan|D. Kazhdan]], J. Morgan, D.R. Morrison, [[Edward Witten|E. Witten]] (eds.)  _[[Quantum Fields and Strings]], A course for mathematicians_, 2 vols. Amer. Math. Soc. Providence 1999. ([web version](http://www.math.ias.edu/qft))

### Super odd sign rule

...

