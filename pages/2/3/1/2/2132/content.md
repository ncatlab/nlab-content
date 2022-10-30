
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _K&#228;hler manifold_ is a [[smooth manifold]] compatibly equipped with 

1. [[complex structure]];

1. [[Riemannian structure]];

1. [[symplectic structure]].

If the symplectic structure is not compatibly present, it is just a [[Hermitian manifold]].

| [[complex structure]] | + [[Riemannian structure]] | + [[symplectic structure]] |
|--|--|--|
[[complex structure]] | [[Hermitian structure]] | [[Kähler structure]] |



Where a Riemannian manifold is a real [[smooth manifold]] equipped with a nondegenerate smooth symmetric 2-form $g$ (the [[Riemannian metric]]), an __almost K&#228;hler manifold__ is a [[complex manifold|complex holomorphic manifold]] equipped with a nondegenerate hermitian 2-form $h$ (the __K&#228;hler $2$-form__).  The real [[cotangent bundle]] is replaced with the complex cotangent bundle, and symmetry is replaced with hermitian symmetry. An almost K&#228;hler manifold is a __K&#228;hler manifold__ if it satisfies an additional integrability condition.

The K&#228;hler 2-form can be decomposed as $h = g+i\omega$; here $g$ is a [[Riemannian metric]] and $\omega$ a [[symplectic form]]. 

## Examples

There is a unique up to a scalar hermitian metric on a complex projective space (which can be normalized), the Fubini--Study metric. All analytic subvarieties of a complex projective space are in fact [[algebraic variety|algebraic subvarieties]] and they inherit the K&#228;hler structure from the projective space. Examples include complex tori $\mathbb{C}^n/L$ where $L$ is a lattice in $\mathbb{C}^n$, K3-surfaces, compact Calabi-Yau manifolds, quadrics, products of projective spaces and so on. 

## Properties

### Relation to (almost) complex manifold

> The following based on [this MO comment](http://mathoverflow.net/a/73330/381) by [[Spiro Karigiannis]]

When $(X, J)$ is an [[almost complex manifold]], then there is a notion of smooth complex-valued [[differential forms]] of type $(p,q)$. A complex valued $2$-form $\omega$ is of type $(1,1)$ precisely if it satisfies 

$$
  \omega(J v,J w) = \omega(v,w)
$$ 

for all smooth [[vector fields]] $v,w$ on $X$. Here $\omega$ is a *real* $2$-form of type $(1,1)$, if $\overline \omega = \omega$. Setting

$$
  g(v,w) = \omega(v, J w), 
$$

definesa smooth symmetric rank $(2,0)$ [[tensor field]]. This is a
[[Riemannian metric]] precisely if it is fiberwise a [[positive definite bilinear form]]. If it $g(-,-) = \omega(-,J -)$ is hence a Riemannian metric, then $\omega(-,-)$ is called positive definite, too.

The triple of data $(J, \omega, g)$, where $J$ is an [[almost complex structure]], $\omega$ is a real positive $(1,1)$-[[differential form]], and $g$ is the associated [[Riemannian metric]] this way define an *[[almost Hermitian manifold]]*. 

Now the condition for $X$ to be a K&#228;hler is that $X$ be a [[complex manifold]] ($J$ is integrable) and that $d\omega = 0$. 
Equivalently that for the [[Levi-Civita connection]] $\nabla$ of $G$ we have $\nabla \omega = 0$ or $\nabla J = 0$. 

Hence given a [[complex manifold]] $X$, together with a  *closed* real $2$-form $\omega$, the only additional condition required to ensure that it defines a  K&#228;hler metric is that it be a positive $(1,1)$-form.

### Relation to Spin-structures

+-- {: .num_prop}
###### Proposition

A spin structure on a [[compact topological space|compact]] [[Hermitian manifold]] ([[Kähler manifold]]) $X$ of complex [[dimension]] $n$ exists precisely if, equivalently

* there is a choice of [[square root]] $\sqrt{\Omega^{n,0}}$ of the [[canonical line bundle]] $\Omega^{n,0}$ (a "[[Theta characteristic]]"); 

* there is a trivialization of the [[first Chern class]] $c_1(T X)$ of the [[tangent bundle]].

=--

In this case one has:

+-- {: .num_prop}
###### Proposition

There is a [[natural isomorphism]] 

$$
  S_X \simeq \Omega^{0,\bullet}_X \otimes \sqrt{\Omega^{n,0}}_X
$$ 

of the [[sheaf]] of [[sections]] of the [[spinor bundle]] $S_X$ on $X$ with the [[tensor product]] of the  [[Dolbeault complex]] with the corresponding [[Theta characteristic]];


Moreover, the corresponding [[Dirac operator]] is the [[Dolbeault-Dirac operator]] $\overline{\partial} + \overline{\partial}^\ast$.

=--

This is due to ([Hitchin 74](#Hitchin74)). A textbook account is for instance in ([Friedrich 74, around p. 79 and p. 82](#Friedrich74)).


### Hodge structure
 {#HodgeStructure}

The [[Hodge theorem]] asserts that for a compact K&#228;hler manifold, the canonical $(p,q)$-grading of its [[differential forms]] descends to its [[de Rham cohomology]]/[[ordinary cohomology]]. The resulting structure is called a _[[Hodge structure]]_, and is indeed the archetypical example of such.

## Related concepts

* **K&#228;hler manifold**, [[hyper-Kähler manifold]], [[quaternionic Kähler manifold]]

  * [[Kähler potential]]

* [[Kähler-Einstein manifold]]

* [[symplectic manifold]]

* [[Kähler polarization]]


[[!include special holonomy table]]


## References

K&#228;hler manifolds were first introduced and studied by P. A. Shirokov (cf. [a historical article](http://dx.doi.org/10.1070/RM1995v050n02ABEH002098)) and later independently by K&#228;hler. 

Lecture notes include

* Andrei Moroianu, _Lectures on K&#228;hler Geometry_ ([pdf](http://www.math.polytechnique.fr/~moroianu/tex/kg.pdf))

Discussion of [[spin structures]] in K&#228;hler manifolds is for instance in 

* [[Thomas Friedrich]], _Dirac operators in Riemannian geometry_, Graduate studies in mathematics 25, AMS (1997)
 {#Friedrich97}


[[!redirects Kähler manifolds]]

[[!redirects Kahler manifold]]
[[!redirects Kahler 2-form]]
[[!redirects almost Kahler manifold]]
[[!redirects Kähler 2-form]]
[[!redirects almost Kähler manifold]]

[[!redirects Kähler form]]
[[!redirects Kähler forms]]

[[!redirects Kähler geometry]]

[[!redirects Kähler manifold]]

[[!redirects Kähler structure]]
[[!redirects Kähler structures]]
[[!redirects Kaehler structure]]
[[!redirects Kaehler structures]]

