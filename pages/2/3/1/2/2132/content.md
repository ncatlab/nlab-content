
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

## Definition

### Linear Kähler structure
 {#LinearKählerStructure}

+-- {: .num_defn #KaehlerVectorSpace}
###### Definition
**([[Kähler vector space]])**

Let $V$ be a [[finite dimensional vector space|finite-dimensional]] [[real vector space]]. Then a _linear Kähler structure_ on $V$ is

1. a _[[linear complex structure]]_ on $V$, namely a [[linear map|linear]] [[endomorphism]]

   $$
     J \;\colon\; V \to V
   $$

   whose [[composition]] with itself is minus the [[identity morphism]]:

   $$
     J \circ J = - id_V
   $$

1. a skew-symmetric [[bilinear form]]

   $$
     \omega \in \wedge^2 V^\ast
   $$

such that

1. $\omega(J(-),J(-)) = \omega(-,-)$;

1. $g(-,-) \coloneqq \omega(-,J(-))$ is a [[Riemannian metric]], namely

   a non-degenerate positive-definite [[bilinear form]] on $V$ 

   (necessarily symmetric, due to the other properties: $g(w,v) = \omega(w,J(v)) = -\omega(J(v),w) = + \omega(J(J(v)), J(w)) = \omega(v,J(w)) = g(v,w)$).

=--

(e.g. [Boalch 09, p. 26-27](#Boalch09))

Linear Kähler space structure may conveniently be encoded in terms of [[Hermitian space]] structure:

+-- {: .num_defn #HermitianForm}
###### Definition
**([[Hermitian form]] and [[Hermitian space]])**

Let $V$ be a [[real vector space]] equipped with a [[complex structure]] $J\colon V \to V$. Then a _[[Hermitian form]]_ on $V$ is 

* a complex-valued real-[[bilinear form]]

  $$
    h \;\colon\; V \otimes V \longrightarrow \mathbb{C}
  $$

such that this is _symmetric sesquilinear_, in that:

1. $h$ is complex-linear in the first argument;

1. $h(w,v) = \left(h(v,w) \right)^\ast$ for all $v,w \in V$ 

where $(-)^\ast$ denotes [[complex conjugation]].

A Hermitian form is _positive definite_ (often assumed by default) if for all $v \in V$

1. $h(v,v) \geq 0$

1. $h(v,v) = 0 \phantom{AA} \Leftrightarrow \phantom{AA} v = 0$.

A [[complex vector space]] $(V,J)$ equipped with a (positive definite) Hermitian form $h$ is called a (positive definite) _[[Hermitian space]]_.

=--

+-- {: .num_prop #BasicPropertiesOfHermitianForms}
###### Proposition
**(basic properties of [[Hermitian forms]])**

Let $((V,J),h)$ be a positive definite [[Hermitian space]] (def. \ref{HermitianForm}). Then 

1. the [[real part]] of the [[Hermitian form]] 

   $$
     g(-,-) \;\coloneqq\; Re(h(-,-))
   $$
  
   is a [[Riemannian metric]], hence a symmetric positive-definite real-[[bilinear form]] 

   $$
     g \;\colon\; V \otimes V \to \mathbb{R}
   $$

1. the [[imaginary part]] of the [[Hermitian form]]

   $$
     \omega(-,-) \;\coloneqq\; -Im(h(-,-))
   $$

   is a [[symplectic form]], hence a non-degenerate skew-symmetric real-[[bilinear form]]

   $$
     \omega \;\colon\; V \wedge V \to \mathbb{R}
     \,.
   $$

hence

$$
  h = g - i \omega
  \,.
$$

The two components are related by

$$
  \label{RelationBetweennOmegaAndgOnHermitianSpace}
  \omega(v,w)
  \;=\;
  g(J(v),w)
  \phantom{AAAAA}
  g(v,w)
  \;=\;
  \omega(v,J(v))
  \,.
$$

Finally 

$$
  h(J(-),J(-)) = h(-,-)
$$

and so the  Riemannian metrics $g$ on $V$ appearing from (and fully determining) Hermitian forms $h$ via $h = g - i \omega$ are precisely those for which

$$  
  \label{HermitianMetric}
  g(J(-),J(-)) = g(-,-)
  \,.
$$

These are called the _[[Hermitian metrics]]_.

=--


+-- {: .proof}
###### Proof

The positive-definiteness of $g$ is immediate from that of $h$. The symmetry of $g$ follows from the symmetric sesquilinearity of $h$:

$$
  \begin{aligned}
    g(w,v)
    & \coloneqq
    Re(h(w,v))
    \\
    & =
    Re\left( h(v,w)^\ast\right)
    \\
    & =
    Re(h(v,w))
    \\
    & =
    g(v,w)
    \,.
  \end{aligned}
$$

That $h$ is invariant under $J$ follows from its sesquilinarity

$$
  \begin{aligned}
    h(J(v),J(w))
    &=
    i h(v,J(w))
    \\
    & =
    i (h(J(w),v))^\ast
    \\
    & =
    i (-i) (h(w,v))^\ast
    \\
    & =
    h(v,w)
  \end{aligned}
$$

and this immediately implies the corresponding invariance of $g$ and $\omega$.


Analogously it follows that $\omega$ is skew symmetric:

$$
  \begin{aligned}
    \omega(w,v)
    & \coloneqq
    -Im(h(w,v))
    \\
    & =
    -Im\left( h(v,w)^\ast\right)
    \\
    & =
    Im(h(v,w))
    \\
    & = - \omega(v,w)
    \,,
  \end{aligned}
$$

and the relation between the two components:

$$
  \begin{aligned}
    \omega(v,w)
    & =
    - Im(h(v,w))
    \\
    & =
    Re(i h(v,w))
    \\
    & =
    Re(h(J(v),w))
    \\
    & = 
    g(J(v),w)
  \end{aligned}    
$$

as well as

$$
  \begin{aligned}
    g(v,w)
    & =
    Re(h(v,w)
    \\
    & =
    Im(i h(v,w))
    \\
    & =
    Im(h(J(v),w))
    \\
    & =
    Im(h(J^2(v),J(w)))
    \\
    & = 
    - Im(h(v,J(w)))
    \\
    & = \omega(v,J(w))
    \,.
  \end{aligned}
$$


=--

As a corollary:

+-- {: .num_prop #RelationBetweenKaehlerVectorSpacesAndHermitianSpaces}
###### Proposition
**(relation between [[Kähler vector spaces]] and [[Hermitian spaces]])**

Given a [[real vector space]] $V$ with a [[linear complex structure]] $J$, then the following are equivalent:

1. $\omega \in \wedge^2 V^\ast$ is a [[linear Kähler structure]] (def. \ref{KaehlerVectorSpace});

1. $g \in V \otimes V \to  \mathbb{R}$ is a [[Hermitian metric]] (eq:HermitianMetric)

where $\omega$ and $g$ are related by (eq:RelationBetweennOmegaAndgOnHermitianSpace)

$$
  \omega(v,w)
  \;=\;
  g(J(v),w)
  \phantom{AAAAA}
  g(v,w)
  \;=\;
  \omega(v,J(v))
  \,.
$$

=--

### Kähler manifolds

(...)

### In terms of $G$-Structure
 {#InTermsOfGStructure}

A K&#228;hler manifold is a [[integrability of G-structure|first-order integrable]] [[almost Hermitian structure]], hence a first order integrable [[G-structure]] for $G = U(n) \hookrightarrow GL(2n,\mathbb{R})$ the [[unitary group]].

By the fact (see at _[unitary group -- relation to orthogonal, symplectic and general linear group](unitary+group#RelationToOrthogonalSymplecticAndGeneralLinearGroup)_) that $U(n) \simeq O(2n) \underset{GL(2n,\mathbb{R})}{\times} Sp(2n,\mathbb{R}) \underset{GL(2n,\mathbb{R})}{\times} GL(n,\mathbb{C})$ this means that a K&#228;hler manifold structure is precisely a joint [[orthogonal structure]]/[[Riemannian manifold]] structure, [[symplectic manifold]] structure and [[complex manifold]] structure.

(e.g. [Moroianu 07, 11.1](#Moroianu07), [Verbitsky 09](#Verbitsky09))

## Examples
 {#Examples}

The archetypical elementary example is the following:

+-- {: .num_example #StandardAlmostKaehlerVectorSpaces}
###### Example
**(standard [[Kähler vector space]])**

Let $V \coloneqq \mathbb{R}^2$ be the 2-dimensional [[real vector space]] equipped with the [[complex structure]] $J$ which is given by the canonical identification $\mathbb{R}^2 \simeq \mathbb{C}$, hence, in terms of the canonical [[linear basis]] $(e_i)$ of $\mathbb{R}^2$, this is

$$
  J = (J^i{}_j) 
  \coloneqq 
  \left( 
    \array{
      0 & -1
      \\
      1 & 0
    }
  \right)
  \,.
$$

Moreover let 

$$
  \omega = (\omega_{i j}) \coloneqq \left( \array{0 & 1 \\ -1 & 0} \right)
$$ 

and 

$$
  g = (g_{i j}) \coloneqq \left( \array{ 1 & 0 \\ 0 & 1}  \right)
  \,.
$$ 

Then $(V, J, \omega, g)$ is a [[Kähler vector space]] (def. \ref{KaehlerVectorSpace})


The corresponding [[Kähler manifold]] is $\mathbb{R}^2$ regarded as a [[smooth manifold]] in the standard way and equipped with the [[bilinear forms]] $J, \omega g$ extended as constant rank-2 [[tensors]] over this manifold.

If we write 

$$
  x,y \;\colon\; \mathbb{R}^2 \longrightarrow \mathbb{R}
$$

for the standard [[coordinate functions]] on $\mathbb{R}^2$ with 

$$
  z \coloneqq x + i y \;\coloneqq\; \mathbb{R}^2 \to \mathbb{C}
$$

and

$$
 \overline{z} \coloneqq x - i y \;\coloneqq\; \mathbb{R}^2 \to \mathbb{C}
$$

for the corresponding complex coordinates, then this translates to 

$$
  \omega
  \in
  \Omega^2(\mathbb{R}^2)
$$ 

being the [[differential 2-form]] given by

$$
  \begin{aligned}
    \omega
    & =
    d x \wedge d y
    \\
    & =
    \tfrac{i}{2} d z \wedge d \overline{z}
  \end{aligned}
$$

and with [[Riemannian metric]] [[tensor]] given by

$$
  g = d x \otimes d x + d y \otimes d y
  \,.
$$

The [[Hermitian form]] is given by

$$
  \begin{aligned}
    h 
    & = 
    g - i \omega
    \\
    & = 
    d z \otimes d \overline{z}
    \,.
  \end{aligned}
$$


=--

+-- {: .proof}
###### Proof

This is elementary, but, for the record, here is one way to make it fully explicit (we use [[Einstein summation convention]] and "$\cdot$" denotes [[matrix multiplication]]):

$$
  \begin{aligned}
    \omega_{i j'} J^{j'}{}_j
    & =
    \left(
       \array{
         0 & 1
         \\
         -1 & 0
       }
    \right)
      \cdot
    \left(
      \array{
        0 & -1
        \\
        1 & 0
      }
    \right)
    \\
    & 
    =
    \left(
      \array{
        1 & 0
        \\
        0 & 1
      }
    \right)
    \\
    & =
    g_{i j}
  \end{aligned}
$$


and similarly

$$
  \begin{aligned}
    \omega(J(-),J(-))_{i j}
    & =
    \omega_{i' j'} J^{i'}{}_{i} J^{j'}{}_{j}
    \\
    & =
    (J^t \cdot \omega \cdot J)_{i j}
    \\
    & =
    \left(
    \left(
      \array{
        0 & 1
        \\
        -1 & 0
      }
    \right)
    \cdot
    \left(
      \array{
        0 & 1
        \\
        -1 & 0
      }
    \right)
      \cdot
    \left(
      \array{
        0 & -1
        \\
        1 & 0
      }
    \right)
    \right)_{i j}
    \\
    & =
    \left(
    \left(
      \array{
        -1 & 0
        \\
        0 & -1
      }
    \right)
    \cdot
    \left(
      \array{
        0 & -1
        \\
        1 & 0
      }
    \right)
    \right)_{i j}
    \\
    & = 
    \left(
      \array{
        0 & 1
        \\
        -1 & 0
      }
    \right)_{i j}
    \\
    & = 
    \omega_{i j}
  \end{aligned}
$$

=--

+-- {: .num_example}
###### Example
**([[Fubini-Study metric]])**

There is a unique (up to a scalar) hermitian metric on  [[complex projective space]] (which may be normalized), the _[[Fubini-Study metric]]_. 

All analytic subvarieties of a complex projective space are in fact [[algebraic variety|algebraic subvarieties]] and they inherit the K&#228;hler structure from the projective space. 

Examples include [[complex tori]] $\mathbb{C}^n/L$ where $L$ is a lattice in $\mathbb{C}^n$, [[K3-surfaces]], compact [[Calabi-Yau manifolds]], quadrics, products of projective spaces and so on. 

=--

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

defines a smooth symmetric rank $(2,0)$ [[tensor field]]. This is a
[[Riemannian metric]] precisely if it is fiberwise a [[positive definite bilinear form]]. If it $g(-,-) = \omega(-,J -)$ is hence a Riemannian metric, then $\omega(-,-)$ is called positive definite, too.

The triple of data $(J, \omega, g)$, where $J$ is an [[almost complex structure]], $\omega$ is a real positive $(1,1)$-[[differential form]], and $g$ is the associated [[Riemannian metric]] this way define an *[[almost Hermitian manifold]]*. 

Now the condition for $X$ to be a K&#228;hler is that $X$ be a [[complex manifold]] ($J$ is integrable) and that $d\omega = 0$. 
Equivalently that for the [[Levi-Civita connection]] $\nabla$ of $G$ we have $\nabla \omega = 0$ or $\nabla J = 0$. 

Hence given a [[complex manifold]] $X$, together with a  *closed* real $2$-form $\omega$, the only additional condition required to ensure that it defines a  K&#228;hler metric is that it be a positive $(1,1)$-form.

### Relation to symplectic manifolds

Lifting a [[symplectic manifold]] structure to a K&#228;hler manifold structure is also called choosing a _[[Kähler polarization]]_.

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

### Hodge star operator
 {#HodgeStarOperator}

On a K&#228;hler manifold $\Sigma$ of [[dimension]] $dim_{\mathbb{C}}(\Sigma) = n$ the [[Hodge star operator]] acts on the [[Dolbeault complex]] as

$$
  \star \;\colon\; \Omega^{p,q}(X) \longrightarrow \Omega^{n-q,n-p}(X)
  \,.
$$

(notice the exchange of the role of $p$ and $q$) See e.g. ([BiquerdH&#246;ring 08, p. 79](#BiquerdHoering08)).


### Hodge structure
 {#HodgeStructure}

The [[Hodge theorem]] asserts that for a compact K&#228;hler manifold, the canonical $(p,q)$-grading of its [[differential forms]] descends to its [[de Rham cohomology]]/[[ordinary cohomology]]. The resulting structure is called a _[[Hodge structure]]_, and is indeed the archetypical example of such.


### As $\mathbb{C}$-Riemannian manifolds

[[!include normed division algebra Riemannian geometry -- table]]

## Related concepts

* [[bilinear form]], [[quadratic form]], [[sesquilinear form]]

* [[symplectic form]], [[Hermitian form]]


* **K&#228;hler manifold**, [[hyper-Kähler manifold]], [[quaternionic Kähler manifold]]

  * [[Kähler potential]]

* [[Kähler-Einstein manifold]]

* [[symplectic manifold]]

* [[Lefschetz decomposition]]

* [[Kähler polarization]], [[almost Kähler geometric quantization]], 

* [[Fedosov deformation quantization]]

* [[Hodge filtration]], [[Frölicher spectral sequence]]

* [[Hodge manifold]]

* [[Sasakian manifold]]

[[!include special holonomy table]]


## References

K&#228;hler manifolds were first introduced and studied by P. A. Shirokov (cf. [a historical article](http://dx.doi.org/10.1070/RM1995v050n02ABEH002098)) and later independently by K&#228;hler. 

Textbook accounts include

* {#Voisin02} [[Claire Voisin]], section 3 of _[[Hodge theory and Complex algebraic geometry]] I,II_,  Cambridge Stud. in Adv. Math. __76, 77__, 2002/3


Lecture notes include

* {#Moroianu07} [[Andrei Moroianu]], _Lectures on K&#228;hler Geometry_, Cambridge University Press 2007 ([arXiv:math/0402223](https://arxiv.org/abs/math/0402223) [doi:10.1017/CBO9780511618666](https://doi.org/10.1017/CBO9780511618666), [pdf](https://moroianu.perso.math.cnrs.fr/tex/kg.pdf))

* {#Boalch09} Philip Boalch, _Noncompact complex symplectic and hyperkähler manifolds_, 2009 ([pdf](https://www.math.u-psud.fr/~boalch/cours09/hk.pdf))

Discussion in terms of [[integrability of G-structure|first-order integrable]] [[G-structure]] include

* [Moroianu 07, 11.1](#Moroianu07)

* {#Verbitsky09} Misha Verbitsky, _K&#228;hler manifolds_, lecture notes 2009 ([pdf](http://verbit.ru/MATH/TALKS/Unicamp-kahler-1.pdf))

Discussion of [[spin structures]] in K&#228;hler manifolds is for instance in 

* {#Friedrich97} [[Thomas Friedrich]], _Dirac operators in Riemannian geometry_, Graduate studies in mathematics 25, AMS (1997)
 
Discussion of [[Hodge theory]] on K&#228;hler manifolds is in 

* {#BiquerdHoering08} O. Biquard, A. H&#246;ring, _K&#228;hler geometry and Hodge theory_, 2008 ([pdf](http://math.unice.fr/~hoering/hodge/hodge.pdf))

Discussion of [[Kähler orbifolds]]:


* Thalia D. Jeffres, _Singular Set of Some Kähler Orbifolds_, Transactions of the American Mathematical Society Vol. 349, No. 5 (May, 1997), pp. 1961-1971 ([jstor:2155355 ](https://www.jstor.org/stable/2155355 ))

* Akira Fujiki, _On primitively symplectic compact Kähler V-manifolds_, in:  [[Kenji Ueno]] (ed.), _Classification of Algebraic and Analytic Manifolds: Katata Symposium Proceedings 1982_, Birkhäuser 1983 (ISBN:9780817631376)

* [[Dominic Joyce]], Section 6.5.1 of: _Compact Manifolds with Special Holonomy_, Oxford Mathematical Monographs, Oxford University Press (2000) ([ISBN:9780198506010](https://global.oup.com/academic/product/compact-manifolds-with-special-holonomy-9780198506010?cc=de&lang=en&))


* Miguel Abreu, _Kähler Metrics on Toric Orbifolds_, J. Differential Geom. Volume 58, Number 1 (2001), 151-187 ([euclid:jdg/1090348285](https://projecteuclid.org/euclid.jdg/1090348285))

* Giovanni Bazzoni, Indranil Biswas, Marisa Fernández, Vicente Muñoz, Aleksy Tralle, _Homotopic properties of Kähler orbifolds_, In: Chiossi S., Fino A., Musso E., Podestà F., Vezzoni L. (eds.) _Special Metrics and Group Actions in Geometry_ Springer INdAM Series, vol 23. Springer (2017) ([arXiv:1605.03024](https://arxiv.org/abs/1605.03024), [doi:10.1007/978-3-319-67519-0_2](https://doi.org/10.1007/978-3-319-67519-0_2))


[[!redirects Kähler manifolds]]

[[!redirects Kahler manifold]]
[[!redirects Kahler 2-form]]
[[!redirects almost Kahler manifold]]
[[!redirects Kähler 2-form]]
[[!redirects almost Kähler manifold]]

[[!redirects Kähler form]]
[[!redirects Kähler forms]]

[[!redirects Kähler geometry]]

[[!redirects Kähler orbifold]]
[[!redirects Kähler orbifolds]]


[[!redirects Kähler structure]]
[[!redirects Kähler structures]]
[[!redirects Kaehler structure]]
[[!redirects Kaehler structures]]

[[!redirects almost Kähler manifold]]
[[!redirects almost Kähler manifolds]]

[[!redirects almost Kaehler manifold]]
[[!redirects almost Kaehler manifolds]]


[[!redirects almost Kähler structure]]
[[!redirects almost Kähler structures]]
[[!redirects almost Kaehler structure]]
[[!redirects almost Kaehler structures]]

[[!redirects Kähler manifold structure]]
[[!redirects Kähler manifold structures]]

[[!redirects Kaehler manifold structure]]
[[!redirects Kaehler manifold structures]]



