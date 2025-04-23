
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--




#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The formal notion of _curvature_ is a formalization and generalization of the intuitive notion of the ("[extrinsic](#Extrinsic)") curvature of a [[surface]] embedded in a [[Cartesian space]] $\mathbb{R}^n$.

This extrinsic curvature of a surface is called [[Gaussian curvature]]. It may also be understood intrinsically as a property of just the surface without reference to the ambient [[Cartesian space]] that it is embedded in: the canonical [[metric]] on $\mathbb{R}^n$ induces a [[Riemannian metric]] on the surface and the surface's curvature is encoded in the [[Levi-Civita connection]] on the [[tangent bundle]] of the surface.

This notion of curvature of a [[Levi-Civita connection]] in turn generalizes straightforwardly to a notion of curvature of any [[connection on a bundle]] and thus gives the name to the general concept. 

For instance in the [[first-order formulation of gravity]] the curvature of [[spacetime]] is literally the curvature of the [[Levi-Civita connection]] on spacetime in this sense. But also the [[Yang-Mills field]] is a connection on a [[principal bundle]] and its curvature encodes the [[field strength]] of the [[Yang-Mills field]], which is a concept rather remote from the intuition of a curved surface (though not unrelated).

Even more generally, the notion of a [[connection on a bundle]] and of a [[Lie algebra]]-valued 1-form generalizes to connections on [[principal 2-bundle]]s and [[principal ∞-bundle]]s and [curvature of ∞-Lie algebroid valued differential forms](#OfInfLieAlgebroidValuedForms). 

In [[generalized (Eilenberg-Steenrod) cohomology|Eilenberg-Steenrod]]-type [[differential cohomology]] describing _abelian_ such higher connections these curvatures appear in the form of generalized [[Chern character]] [[curvature characteristic form]]s. 


## Extrinsic curvature of embedded manifolds {#Extrinsic}

Curvature $\kappa(\gamma)$ of a smooth curve $\gamma$ at a point $p$ of a smooth curve is the (signed) inverse radius of the (oriented) circle having tangency of order 1 with the curve at the point $p$. Every smooth curve in a 3-dimensional space is determined up to isometry by its (parametrised) curvature and torsion. Intuitively, the curvature measures how much curves are bent, when measured in some metrics. [[Frenet-Serret formulas]] express the derivative of Frenet moving frame with respect to the parameter of a  [[naturally parametrized curve]] in $n$-dimensional Euclidean space as an antisymmetric matrix times the Frenet moving frame. The nonzero coefficients of the matrix are, up to the sign, the curvature of the curve, torsion and higher analogues. 
For higher dimensional surfaces one can look at normal curvature which is the curvature of the curve which is intersection of a plane determined by the normal vector to the surface and a given tangent vector. For any 2-dimensional tangent plane, the normal curvature has two extreme values. Their product is called the **Gaussian curvature**. 

**Sectional curvature** of a higher dimensional smooth surface at its point $p$ in an Euclidean space along a tangent 2-dimensional plane is the Gaussian curvature of the curve which is the intersection of the surface with the plane. As a plane is determined by two vectors, the sectional curvature is determined by a surface and a pair of vectors, and all possible sectional curvatures can be read form that 2-form; therefore we talk about the operator of the curvature. 

Curvature can be described also intrinsically, without recourse to the ambient space and its metric. Therefore it makes sense in Riemannian geometry based on the [[metric]] tensor just on a manifold. In 1917, Herman Weyl postulated a more fundamental quantity than a [[Riemannian metric]], the [[connection on a bundle|connection]] on a fibre bundle, giving hence rise to a modern, generalized idea of the curvature. While Riemannian metric gives rise to a [[Levi-Civita connection]] on the [[tangent bundle]] of the Riemannian manifold, not every connection on a vector or principal bundles is induced by metrics. In that sense the connection is a more basic notion in geometry. 

## Curvature of a connection

The _curvature_ of a [[connection on a bundle]] measures how the connection is _locally_ non-trivial.

In as far as the notion of connection on a bundle is generalized by the notion of a cocycle in [[differential cohomology]], curvature is essentially the [[Chern character]].

In as far as cocycles in differential cohomology represent [[gauge field]]s in [[physics]], the curvature is the [[field strength]] of these gauge fields.

After the conception of [[gauge theory]], the term _curvature_ was firmly established in its generalization from this special case to the case of connections on all kinds of [[bundle]]s and [[principal infinity-bundle|higher bundles]].


### Curvature of a Lie-algebra valued form {#OfLieAlgebraValuedForm}


* A connection on a trivial [[line bundle]] on a [[space]] $X$ is just a [[differential forms|1-form]] 

  $$
    A \in \Omega^1(X)
    \,.
  $$ 

  The curvature in this case is the 2-form $F = d A$.

*  A [[connection on a bundle|connection]] on a trivial $G$-[[principal bundle]] for $G$ a [[Lie group]] with [[Lie algebra]] $\mathfrak{g}$ is a $\mathfrak{g}$-valued 1-form (see [[groupoid of Lie-algebra valued forms]])
 
   $$
     A \in \Omega^1(X) \otimes \mathfrak{g}
     \,.
   $$

   Its curvature is the Lie-algebra valued 2-form

   $$
     F_A = \mathbf{d} A + [A \wedge A]
     \,,
   $$

   where $[-,-]$ is the Lie bracket in $\mathfrak{g}$.

* According to the discussion at [[∞-Chern-Weil theory]], a connection on a trivial [[principal ∞-bundle]] is given by a collection of [[∞-Lie algebroid valued differential forms]]. The notion of curvature in this general context is discussed at [curvature of ∞-Lie algebroid valued differential forms](#OfInfLieAlgebroidValuedForms).


### Curvature characteristic forms

* [[curvature characteristic form]]

### Geometric interpretation of curvature 2-forms

For the geometric interpretation of the curvature 2-form of a $\mathfrak{g}$-valued 1-form

$$
  \Omega^\bullet(X)
  \leftarrow
  W(\mathfrak{g})
  : 
  A
$$

it is useful to recall that both the [[deRham complex]] $\Omega^\bullet(X)$ as well as the [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{g})$ are naturally interpreted as function algebras on [[infinitesimal object]]s, as discussed at [[∞-Lie algebroid]].

The [[deRham complex]] may be thought of as the algebra of functions on the infinitesimal path ∞-groupoid $\Pi^{inf}(X)$. This has as [[object]]s the points of $X$, as [[morphism]]s [[infinitesimal object|infinitesimal]] paths

$$
  x \to y
$$

in $X$

as [[2-morphism]]s infinitesimal little surfaces

$$
  \array{  
     x &\to& y_1
     \\
     \downarrow & \searrow & \downarrow
     \\
     y_2 &\to& z
  }
$$

in $X$, and so on.

On the other hand, $CE(\mathfrak{g})$ is the algebra of functions on the infinitesimal version $\mathbf{B}G_{(1)}$ of what is called the [[delooping]] [[groupoid]] $\mathbf{B}G$ of the [[Lie group]] of which $\mathfrak{g}$ is a [[Lie algebra]]. This has a single [[object]] ${*}$, and a morphism is an infinitesimal group element

$$
  {*} \stackrel{e + \lambda^a t_a}{\to} {*}
$$

for $e$ the neutral element of the group (the identity), for $t_a$ an element of the [[nLab:Lie algebra|Lie algebra]] as before and for $\lambda^a$ some coefficient.

A 2-morphism is an infinitesimal surface bounded by such infinitesimal 1-morphisms such that going either way around the surface 

$$
  \array{  
     {*} &\stackrel{e + \lambda^a_1 t_a}{\to}& {*}
     \\
     \downarrow^{\rlap{\lambda_3^a t_a}} 
     & \searrow & \downarrow^{\rlap{\lambda_2^a t_a}}
     \\
     {*} &\stackrel{\lambda_4^a t_a}{\to}& {*}
  }
$$

produces the same result when then morphisms are composed using the product in the Lie group: the top right way around the square here yields

$$
  (e + \lambda_1^a t_a) )(e + \lambda_2^b t_b) )
  =
  e + \lambda_1^a t_a + \lambda_2^b t_b
  +
  \lambda_1^a \lambda_2^b t_a t_b
$$

and the other way round yields

$$
  (e + \lambda_3^a t_a) )(e + \lambda_4^b t_b) )
  =
  e + \lambda_3^a t_a + \lambda_4^b t_b
  +
  \lambda_3^a \lambda_4^b t_a t_b
  \,.
$$

A morphism of [[nLab:dg-algebra|dg-algebra]]s of the form we have been considering 

$$
  \Omega^\bullet(X) \leftarrow CE(\mathfrak{g})
  :
  A
$$

is now evidently equivalenty a morphism

$$
  A : \Pi^{inf}(X) \to \mathbf{B}G_{(1)}
$$

that sends infinitesimal paths in $X$ to infinitesimal group elements of the form $e + \lambda^a t_a$:

$$
 A : (x \to y) \;\;\mapsto\;\; 
     ({*} \stackrel{e + A^a(x,y) t_a}{\to} {*})
  \,.
$$

If we denote by

$$
  v = y - x
$$

the [[nLab:tangent vector|tangent vector]] that connects the [[nLab:infinitesimal object|infinitesimally]] close points $x$ and $y$ and write $A(x,y) = A_x(v)$ as a function of the first point and the vector pointing away from it, then this reads

$$
 A : (x \to y) \;\;\mapsto\;\; 
     ({*} \stackrel{e + A^a_x(v) t_a}{\to} {*})
  \,.
$$

We can now look at what this assignment $A$ of infinitesimal group elements to infinitesimal paths does to a little square in $X$ as above, with sides spanned by [[nLab:tangent bundle|tangent vector]]s $v_1$ and $v_2$. We find


$$
  A
  \;\;
  :
  \;\;
  \array{  
     x &\stackrel{v_1}{\to}& y_1
     \\
     \downarrow^{v_2} 
     & \searrow & \downarrow
     \\
     y_2 &\to & z
  }
  \;\;\mapsto\;\;
  \array{  
     {*} &\stackrel{e + A_x(v_1) t_a}{\to}& {*}
     \\
     \downarrow^{\rlap{A_x(v_2)^a t_a}} 
     & \searrow & 
    \downarrow^{\rlap{A_{y_1}(v_2)^a t_a}}
     \\
     {*} &\stackrel{A_{y_2}(v_1)^a t_a}{\to}& {*}
  }
  \,.
$$

For the result on the right to qualify as a [[nLab:k-morphism|2-morphism]] in $\mathbf{B}G_{(1)}$ we need that

going around the top right edges, which yields

$$
  e + A_x^a(v_1) t_a + A^b_{y_1}(v_2) t_b
  +
  A_x^a(v_1) A^b_{y_1}(v_2) t_a t_b
$$

is the same as

$$
  e + A_x^a(v_2) t_a + A^b_{y_2}(v_1) t_b
  +
  A_{x}^a(v_2) A^b_{y_2}(v_1) t_a t_b
  \,.
$$

To express what this means as a condition at the point $x$, we may Taylor expand to first order

$$
  A_{y_1} = A_x + \partial_{v_1} A_x
$$

and

$$
  A_{y_2} = A_x + \partial_{v_2} A_x
  \,.
$$

Then some terms cancel and the above condition becomes, to second order

$$
  \partial_{v_1} A^a_x(v_2) t_a
  + 
  A_x^a(v_1) A^b_{x}(v_2) t_a t_b
  =
  \partial_{v_2} A^a_x(v_1) t_a
  + 
  A_x^a(v_2) A^b_{x}(v_1) t_a t_b
  \,.
$$

In other words, the expression

$$
  F_A(v_1,v_2)
  :=
  \partial_{v_1} A^a_x(v_2) t_a
  -
  \partial_{v_2} A^a_x(v_1) t_a
  +
  \frac{1}{2} A_x^a(v_1) A^b_{x}(v_2) [t_a, t_b]
$$

has to vanish. This is the curvature form that we already found above by more algebraic means. 

If this does not vanish, then we don't really have a morphism $A : \Pi^{inf}(X) \to \mathbf{B}G_{(1)}$. But then we instead have some morphism that uses the 1-forms $A^a$ to assigns data to little edges, _and_ that uses the 2-forms $F_A^a$ to assign data to little surfaces. That morphism then will respect a condition as above, but now on little cubes. That condition is the **[[Bianchi identity]]**

$$
  d F_A + [A \wedge F_A] = 0
$$

on the curvature 2-form.



## Curvature of $\infty$-Lie algebroid-valued forms {#OfInfLieAlgebroidValuedForms}

The notion of curvature of a [[Lie-algebra valued 1-form]] discussed [above](#OfLieAlgebraValuedForm) generalizes to that of [[∞-Lie algebroid valued differential forms]].

### Definition

Let $\mathfrak{g}$ be an [[∞-Lie algebra]]. A $\mathfrak{g}$-valued differential form on a [[smooth manifold]] $X$ is a morphism

$$
  \Omega^\bullet(X) \leftarrow
  W(\mathfrak{g})
  : A
$$

of [[dg-algebra]]s, where $\Omega^\bullet(X)$ is the [[de Rham complex]] and $W(\mathfrak{g})$ is the [[Weil algebra]].

There is a canonical inclusion of [[graded vector space]]s 

$$
  W(\mathfrak{g}) \leftarrow \mathfrak{g}^*[1] : F_{(-)}
  \,.
$$

The **curvature of the $\infty$-Lie algebroid valued form $A$** is the composite

$$
  \Omega^\bullet(X) \stackrel{A}{\leftarrow}
  W(\mathfrak{g})
  \stackrel{F_{(-)}}{\leftarrow}
  \mathfrak{g}^*[1]
  :
  F_A
  \,.
$$

This consists, in general, of a tower of components: write $\mathfrak{g}_n$ for the degree $n$-part of the $\infty$-Lie algebra, then we have the further restrictions

$$
  \Omega^\bullet(X) \stackrel{A}{\leftarrow}
  W(\mathfrak{g})
  \stackrel{F_{(-)}}{\leftarrow}
  \mathfrak{g}_{k}^*[1]
  :
  (F_A)_{k+1}
  \,.
$$

So 

$$
  (F_A)_n
  \in
  \Omega^n(X, \mathfrak{g}_{n-1})
$$ 

is a $\mathfrak{g}_{n-1}$-valued $n$-form on $X$.

One may speak of the **2-form curvature**, the **3-form curvature**, the **4-form curvature** and so on.

If instead of just an $\infty$-Lie algebra $\mathfrak{g}$ we take more generally an [[∞-Lie algebroid]], then there is also a **1-form curvature component**.

**Remark** In some places in the literature, the lower curvature form components have been called _fake curvature_ ([BreenMessing](http://arxiv.org/abs/math/0106083)). 


### Properties

#### Obstruction to flatness

Precisely if the curvatures $F_A$ vanish does the morphism $A : W(\mathfrak{g}) \to \Omega^\bullet(X)$ factor through the [[Chevalley-Eilenberg algebra]] $W(\mathfrak{g}) \to CE(\mathfrak{g})$.

$$
  (F_A = 0) 
  \;\;\Leftrightarrow
  \;\;
  \left(
  \array{
     && CE(\mathfrak{g})
     \\
     & {}^{\mathllap{\exists A_{flat}}}\swarrow & \uparrow
     \\
     \Omega^\bullet(X) &\stackrel{A}{\leftarrow}& W(\mathfrak{g})     
  }
  \right)
$$

in which case we call $A$ **flat**.


#### Bianchi identity

By the fact that $A$ is a [[dg-algebra]] [[homomorphism]], its curvature forms satisfy

$$
  d_{dR} F_A + A(d_{W(\mathfrak{g})}(-)) = 0
  \,.
$$

This is the [[Bianchi identity]].

### Curvature characteristic forms

The algebra $inv(\mathfrak{g})$ of [[invariant polynomial]]s embeds into the Weil algebra

$$
  W(\mathfrak{g}) \leftarrow inv(\mathfrak{g})
  \,.
$$

For $A$ a $\mathfrak{g}$-valued form, and $\langle - \rangle \in inv(\mathfrak{g})$, the ordinary closed $n$-form

$$
  \Omega^\bullet(X)
  \stackrel{A}{\leftarrow}
  W(\mathfrak{g})
  \stackrel{}{\leftarrow}
  inv(\mathfrak{g})
  \stackrel{\langle - \rangle}{\leftarrow}
  CE(b^{n-1} \mathbb{R})
  :
  \langle F_A \rangle
$$

is the corresponding [[curvature characteristic form]].





## Curved dg-algebras

(TO ADD: Something about curved $A_\infty$ algebras and curved dg algebras.)


## Related concepts

* [[∞-Lie algebroid valued differential forms]]

* [[connection on an ∞-bundle]]

* [[Bianchi identity]]

* [[curvature characteristic form]]

* [[Chern-Simons form]]

[[!include curvature in Riemannian geometry -- table]] 

$\,$

[[!include gauge field - table]]


## References

### General

* [[Mikio Nakahara]], Section 10.3 of: _[[Geometry, Topology and Physics]]_, IOP 2003 ([doi:10.1201/9781315275826](https://doi.org/10.1201/9781315275826), <a href="http://alpha.sinp.msu.ru/~panov/LibBooks/GRAV/(Graduate_Student_Series_in_Physics)Mikio_Nakahara-Geometry,_Topology_and_Physics,_Second_Edition_(Graduate_Student_Series_in_Physics)-Institute_of_Physics_Publishing(2003).pdf">pdf</a>)


[[!include Cartan structural equations and Bianchi identities -- references]]

[[!redirects curvatures]]

[[!redirects curvature form]]
[[!redirects curvature forms]]

[[!redirects curvature 2-form]]
[[!redirects curvature 2-forms]]

[[!redirects curvature differential form]]
[[!redirects curvature differential forms]]
