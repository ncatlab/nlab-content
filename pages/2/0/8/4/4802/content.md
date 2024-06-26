
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

A _vielbein_ or _solder form_ on a [[manifold]] $X$ is a linear identification of the [[tangent bundle]] with a [[vector bundle]] with explicit ([[pseudo-orthogonal structure|pseudo-]])[[orthogonal structure]].

Any such choice encodes a ([[pseudo-Riemannian metric|pseudo-]])[[Riemannian metric]] on $X$. 

## Definition

There are different equivalent perspectives on the notion of vielbein that are closely related:

* [In terms of Cartan geometry](#InTermsOfCartanGeometry)

* [In terms of orthogonal structure](#InTermsOfOrthogonalStructure)

### In terms of Cartan geometry
 {#InTermsOfCartanGeometry}

Let $X$ be a [[smooth manifold]] of [[dimension]] $d$. For definiteness we assume here that $X$ is [[orientation|oriented]], but this is not necessary.

A [[Lie algebra valued 1-form]]

$$
  (E,\Omega) : T X \to \mathfrak{iso}(d)
$$

with values in the [[Poincaré Lie algebra]] encodes a [[pseudo-Riemannian metric]] on $X$ (if non-degenerate, at least). In this context the component 

$$
  E : T X \to \mathbb{R}^d
$$

of the [[connection on a bundle|connection]] 1-form is called the _vielbein_ . It encodes the metric by

$$
  g = \langle E \otimes E\rangle  \in Sym^2_{C^\infty(X)} \Gamma(T^* X)
  \,,
$$

where $\langle -,-\rangle : \mathbb{R}^d \times \mathbb{R}^d \to \mathbb{R}$ is the canonical [[bilinear form]].

In other words, Given an $(SO(d) \hookrightarrow ISO(d))$-[[Cartan connection]] on $X$, the _vielbein_ is the isomorphism in the definition of Cartan connection.

For $d=4$ this is the _vierbein_ , for $d = 3$ the _dreibein_ , etc.

This terminology is used notably in the context of the _[[first-order formulation of gravity]]_. 


### In terms of orthogonal structure 
 {#InTermsOfOrthogonalStructure}

We discuss here how a choice of vielbein on a [[manifold]] is equivalently the [[reduction of structure groups|reduction of the structure group]] of the [[tangent bundle]] from the [[general linear group]] $GL(n)$ to its [[maximal compact subgroup]], the [[orthogonal group]].

The following also introduces the description of this in terms of [[smooth infinity-groupoid|smooth]] [[twisted cohomology|twisted]] [[cohomology]]. While of course this is not necessary to understand vielbeins, it does give a very natural conceptual description with the advantage that it seamlessly generalizes to notions of _[[generalized vielbein]]_ fields and generally to [[twisted differential c-structures]].

#### The class of the tangent bundle
 {#ClassOfTheTangentBundle}

For completeness, we first review how the [[tangent bundle]] of a [[smooth manifold]] is naturally incarnated as a [[cocycle]] in $GL(n)$-valued [[Cech cohomology]] and how this in turn is naturally formulated in terms of [[Lie groupoids]]/[[differentiable stack|smooth]] [[moduli stacks]]. The reader familiar with these basics should skip to the [next section](#ReductionOfTheStructureGroup).

Let $X$ be a [[smooth manifold]] of [[dimension]] $n$. 

By definition this means that there is an [[atlas]] $\{\phi_i^{-1} : \mathbb{R}^n \simeq U_i \hookrightarrow X\}$ of [[coordinate charts]]. On each overlap $U_i \cap U_j$ of two [[coordinate charts]] the [[partial derivatives]] of the corresponding [[coordinate transformations]]

$$
  \phi_j\circ \phi_i^{-1}
  : 
  U_i \cap U_j \subset \mathbb{R}^n \to \mathbb{R}^n
$$

form the [[Jacobian matrix]] of [[smooth functions]]

$$
  ((\lambda_{i j})^{\mu}{}_{\nu})
  \coloneqq
  \left[\frac{d}{d x^\nu} \phi_j \circ \phi_i^{-1} (x^\mu)
  \right]
  :
  U_i \cap U_j 
  \to 
  GL_n
$$

with values in invertible [[matrices]], hence in the
[[general linear group]] $GL(n)$. By construction (by the [[chain rule]]), these functions satisfy on triple overlaps of coordinate charts the [[matrix product]] equations

$$
  (\lambda_{i j})^\mu{}_\lambda (\lambda_{j k})^\lambda{}_{\nu} 
  = 
  (\lambda_{i k})^\mu{}_{\nu}
  \,,
$$

hence the equation

$$
  \lambda_{i j} \cdot \lambda_{j k} = \lambda_{i k}
$$

in the [[group]] $C^\infty(U_i \cap U_j, GL(n))$ of smooth $GL(n)$-valued functions on the chart overlap.

This is the [[cocycle]] condition for a smooth [[Cech cohomology|Cech cocycle]] in degree 1 with coefficients in $GL(n)$ (precisely: with coefficients in the [[sheaf]] of smooth functions with values in $GL(n)$ ):

$$
  [(\lambda_{i j})] \in H^1_{smooth}(X, GL_n)
  \,.
$$

It is useful to formulate this statement in the language of [[Lie groupoids]]/[[differentiable stacks]]. 

* $X$ itself is trivially a Lie groupoid $(X \stackrel{\to}{\to} X)$;

* from the atlas $\{U_i \to X\}$ we get the corresponding [[Cech groupoid]] 
  $$
    C(\{U_i\}) = 
    (\coprod_{i, j} U_i \cap U_j \stackrel{\to}{\to} \coprod_i U_i)
  $$

* any [[Lie group]] $G$ induces its [[delooping]] [[Lie groupoid]] 
  
  $$
    \mathbf{B}G
    = 
    \left(
       G \stackrel{\to}{\to} * 
    \right)
    \,.
  $$

The above situation is neatly encoded in the existence of a [[diagram]] of Lie groupoids of the form

$$
  \array{
     C(\{U_i\}) &\stackrel{\lambda}{\to}& \mathbf{B} GL(n).
     \\
     {}^{\mathllap{\simeq}}\downarrow
     \\
     X
  }
  \,,
$$

where

* the left morphism is [[stalk]]-wise (around small enough [[neighbourhoods]] of each point) an [[equivalence of groupoids]];

* the horizontal functor has as components the functions $\lambda_{i j}$ and its functoriality is the cocycle condition $\lambda_{i j} \cdot \lambda_{j k} = \lambda_{i k}$.

We want to think of such a diagram as being directly a morphism of [[smooth infinity-groupoid|smooth groupoids]]


$$
  T X : X \to \mathbf{B} GL(n) \;\; \in \mathbf{H}
  \,.
$$

This is true in the [[(2,1)-category]] $\mathbf{H}$ in which stalkwise equivalences $W \subset Mor(PSh(SmthMfd, Grpd))$ have been [[simplicial localization|formally inverted]] to become [[homotopy equivalences]].

Since all real [[vector bundles]] on $X$ are encoded by such morphisms, as are their [[gauge transformations]], we say that $\mathbf{B} GL(n)$ is the [[moduli stack]] for real vector bundles. 

Of course there is a "smaller" Lie groupoid that also classifies real vector bundles. Passing to this "smaller" Lie groupoid is what the choice of vielbein accomplishes, to which we now turn.


#### Reduction of the structure group
 {#ReductionOfTheStructureGroup}


Consider the defining inclusion of the [[orthogonal group]] into the [[general linear group]]

$$
  O(n) \hookrightarrow GL(n)
  \,.
$$

We may understand this inclusion geometrically in terms of the canonical [[metric]] on $\mathbb{R}^n$, but we may also understand it purely Lie theoretically as the
the inclusion of the [[maximal compact subgroup]] of $GL(n)$. This makes manifest that the inclusion is trivial at the level of [[homotopy theory]] (it is a [[homotopy equivalence]]) and hence _only_ encodes geometric information.


The inclusion induces a corresponding morphism of moduli stacks

$$
  \mathbf{c} : \mathbf{B} O(n) \to \mathbf{B} GL(n)
  \,.
$$


A choice of [[orthogonal structure]] on $T X$ a [[G-structure]] for $G = O(n)$, hence is a factorization of the above $GL(n)$-valued cocycle through $\mathbf{c}$, up to a smooth [[homotopy]].

$$
  \array{
     X &&\stackrel{h}{\to}&& \mathbf{B} O(n)
     \\
     & {}_{\mathllap{\lambda}}\searrow &\swArrow_{E^{-1}}& \swarrow_{\mathrlap{\mathbf{c}}}
     \\
     && \mathbf{B}GL(n)
  }
  \,.
$$

This consists of two pieces of data

* the morphism $h$ is a $O(n)$-valued 1-cocycle -- a collection of _orthogonal transition functions_ --  hence on each overlap of coordinate patches a smooth function
  
  $$
    ((h_{i j}){}^a{}_b) : U_i \cap U_j \to O(n)
  $$
  
  such that 

  $$
    h_{i j} \cdot h_{j k} = h_{i k}
    \,;
  $$

* the homotopy $E$ is on each chart a function

$$
  E_i  = ((E_i)^a{}_\mu) : U_i \to GL(n)
$$

* such that on each double overlap it intertwines the transition functions $\lambda$ of the tangent bundle with the new orthogonal transition functions, meaning that the equation

  $$
    (E_i)^a{}_{\mu} (\lambda_{i j})^{\mu}{}_\nu
    =
    (h_{i j})^a{}_b (E_j]^b{}_\nu
  $$

  holds. This exhibits the [[natural transformation|naturality]] [[diagram]] of $E$:

  $$
    \array{
       * &\stackrel{E_i}{\to}& * 
       \\
       {}^{\mathllap{h_{i j}}}\downarrow && \downarrow^{\mathrlap{\lambda_{i j}}}
       \\
       * &\stackrel{E_j}{\to}& * 
    }
  $$

Such a lift $(h,E)$ is an [[orthogonal structure]] on $T X$.
The component $E$ is called the corresponding **vielbein**. It exhibits an [[isomorphism]] 

$$
  E : T X \stackrel{\simeq}{\to} V
$$

between a [[vector bundle]] $V \to X$ with [[structure group]] explicitly being the [[orthogonal group]] and the [[tangent bundle]], hence it exhibits the [[reduction of structure groups|reduction of the structure group]] of $T X$ from $GL(n)$ to $O(n)$.

#### Moduli space of orthogonal structures: twisted cohomology
 {#ModuliSpaceOfOrhtogonalStructures}

In order to understand the space of choices of vielbein fields on a given tangent bundle, hence the _[[moduli space]]_ or _[[moduli stack]]_ of [[orthogonal structures]]/[[Riemannian metrics]] on $X$, it is useful to first consider the [[homotopy fiber]] of the morphism $\mathbf{c} : \mathbf{B}O(n) \to \mathbf{B}GL(n)$. One finds that this is the [[coset]] $O(n) \backslash GL(n)$. We may think of the [[fiber sequence]]

$$
  \array{  
    GL(n)/O(n) &\to& \mathbf{B} O(n)
    \\
    && \downarrow
    \\
    && \mathbf{B} GL(n)
  }
$$

as being a bundle in $\mathbf{H}$ over the [[moduli stack]] $\mathbf{B}GL(n)$ with typical fiber $GL(n)/O(n)$. It is  the smooth [[associated infinity-bundle|associated bundle]] to the smooth [[universal principal bundle|universal GL(n)-bundle]] induced by the canonical [[action]] of $GL(n)$ on $O(n)\backslash GL(n)$.

This means that if the tangent bundle $T X$ is trivializable, then the coset space $O(n)\backslash GL(n)$ is the moduli space for vielbein fields on $T X$, in that the space of these is 

$$
  \mathbf{H}(X, O(n)\backslash GL(n)) = C^\infty(X, O(n)\backslash GL(n))
  \,.
$$

However, if $T X$ is not trivial, then this is true only locally: there is then an [[atlas]] $\{U_i \to X\}$ such that restricted to each $U_i$ the moduli space of vielbein fields is $C^\infty(U_i, GL(n)/ O(n))$, but globally these now glue together in a non-trivial way as encoded by the tangent bundle: we may say that 

the tangent bundle _twists_ the functions $X \to GL(n)/O(n)$. If -- as we may -- we think of an ordinary such function as a cocycle in degree-0 cohomology, then this means that a vielbein is a cocycle in $T X$-_[[twisted cohomology]]_ relative to the _twisting coefficient bundle_ $\mathbf{c}$.

We can make this more manifest by writing equivalently

$$
  \array{
    O(n)\backslash GL(n) &\to& (O(n)\backslash GL(n)) // GL(n)
    \\
    && \downarrow   
    \\
    && \mathbf{B}GL(n)
  }
  \,,
$$

where now on the right we have inserted the [[fibration]] resolution of the morphism $\mathbf{c}$ as provided by the [[factorization lemma]]: this is the morphism out of the [[action groupoid]] of the action of $GL(n)$ on $O(n)\backslash GL(n)$.


The pullback

$$
  \array{
    T X \times_{GL(n)} (O(n)\backslash GL(n)) 
      &\to&
    O(n)\backslash GL(n) // GL(n)
    \\
    \downarrow && \downarrow
    \\
    X &\stackrel{T X}{\to}& \mathbf{B}GL(n)
  }  
$$

give the non-linear $T X$-associated bundle whose space of sections is the "twisted $O(n)\backslash GL(n)$-0-cohomology", hence the space of inequivalent vielbein fields.


#### Moduli stack of orthogonal structures

The above says that the space of vielbein fields is the [[cohomology]] of $T X$ in the [[over-(infinity,1)-topos|slice (2,1)-topos]] $\mathbf{H}_{/\mathbf{B}GL(n)}$ with coefficients in $\mathbf{c} : \mathbf{B}O \to \mathbf{B}GL(n)$

$$
  O Struc_{TX}(X) \simeq \mathbf{H}_{/\mathbf{B}GL(n)}(T X, \mathbf{c})
  \,.
$$

But also this space of choices of vielbein fields has a smooth structure, it is itself a smooth [[moduli stack]]. This is obtained by forming the [[internal hom]] in the slice over $\mathbf{B}GL(n)$ of the [[locally cartesian closed (infinity,1)-category|locally cartesian closed (2,1)-category]] $\mathbf{H}$.

$$
  O \mathbf{Struc}_{T X}(X)
  = 
  [X, \mathbf{B}O]_{\mathbf{B}GL(n)}
$$

#### Differential refinement: Spin connection

We may further lift this discussion to [[differential cohomology]] to get genuine _differential_ $T X$-twisted $\mathbf{c}$-structures. 

Write $\mathbf{B}G_{conn}$ for [[groupoid of Lie-algebra valued forms]]. As an object of $\mathbf{H} = $ [[smooth infinity-groupoid|SmoothGrpd]] this the [[moduli stack]] of $G$-[[connection on a bundle|connections]].

The morphism $\mathbf{c}$ has an evident differential refinement

$$
  \mathbf{c}_{conn} : \mathbf{B}O(n)_{conn} \to \mathbf{B}GL(n)_{conn}
  \,.
$$

The [[homotopy fiber]] of this differential refinement is still the same as before

$$
  \array{
    GL(n)/ O(n) &\to& \mathbf{B} O(n)_{conn}
    \\
    && \downarrow
    \\
    && \mathbf{B} GL(n)_{conn}
  }
  \,,
$$

so that the moduli space of "differential vielbein fields" is the same as that of plain vielbein fields.

Consider an [[affine connection]]

$$
  \nabla_{T X} : X \to \mathbf{B}GL(n)
$$

hence a $GL(n)$-[[principal connection]] which locally on out atas is given by the [[Christoffel symbols]] 

$$
  \Gamma_i = ((\Gamma_i)_\mu{}{}^{\alpha}{}_\beta)
  \in 
  \Omega^1(U_i, \mathfrak{gl}(n))
  \,.
$$

A lift $(\nabla_V, E)$ in 

$$
  \array{
    X &&\stackrel{\nabla_{V}}{\to}&& \mathbf{B}O_{conn}
    \\
    & {}_{\mathllap{\nabla_{T X}}}\searrow 
     &\swArrow_{E^{-1}}& 
    \swarrow_{\mathbf{c}_{conn}}
    \\
    && \mathbf{B}GL(n)_{conn}
  }
$$

is in components a "[[spin connection]]"

$$
  \omega_\mu = E d E^{-1} + E \Gamma_\mu E^{-1}
$$

$$
  \omega_\mu{}^a{}_b 
   = 
   E^a{}_\nu \partial_\mu E^\nu{}_b
   +
   E^a{}_\nu \Gamma_\mu{}^\nu{}_\lambda E^\lambda{}_b
   \,.
$$

This is the standard formula for the relation between the [[Christoffel symbols]] and the [[spin connection]] in terms of the vielbein.

#### Generalized and exceptional vielbein fields

The above discussion seamlessly generalizes to many other related cases. For instance

1. For the coefficient bundle

   $$
     \array{
        O(n)\backslash O(n,n) /O(n) &\to& \mathbf{B} (O(n) \times O(n))
      \\
      && \downarrow
      \\
      && \mathbf{B}O(n,n)
     }
   $$

   one gets the [[generalized vielbein]] of [[type II geometry]];

1. for the coefficient bundle

   $$
     \array{
        H_n\backslash E_n &\to& \mathbf{B} H_n
      \\
      && \downarrow
      \\
      && \mathbf{B} E_n
     }
   $$

   coming from the inclusion of the [[maximal compact subgroup]] of an [[exceptional Lie group]] one gets generalized vielbein fields for [[exceptional generalized geometry]];

1. for the coefficient bundle

   $$
     \array{
       && \mathbf{B} E_8
      \\
      && \downarrow^{\mathbf{a}}
      \\
      && \mathbf{B}^3 U(1)
     }
   $$

   coming from the second smooth universal [[Chern class]] of [[E8]] one gets part of the geometry of the [[supergravity C-field]]

and so on. More examples are discussed for instance at 
_[[twisted smooth cohomology in string theory]]_.

### In terms of basic forms on the frame bundle
 {#InTermsOfBasicFormsOnFrameBundle}

A [[G-structure]] on $X$ for $G = O(n)$ the [[orthogonal group]] is equivalently an $O(n)$-[[principal bundle|principal]] subbundle of the [[frame bundle]] $\pi \colon Fr(X)\to X$.

This frame bundle carries a universal "basic" $\mathbb{R}^n$-valued differential form

$$
  \tau_{b} \in \Omega^1(Fr(X), \mathbb{R}^n)
$$

defined on a [[tangent vector]] $v\in \Gamma_{f \in Fr(X)}$ by 

$$
  \tau_b(v) \coloneqq f^{-1}(d \pi(v))
  \,,
$$

where $d\pi \colon T Fr(X)\to T X$ is the [[differential]] of the bundle projection $\pi$ and $f$ is the given frame regarded as a linear [[isomorphism]] $f\colon \mathbb{R}^n \stackrel{\simeq}{\longrightarrow} T_x X$.

Then given an orthogonal structure in the form of an $O(n)$-subbundle $i \colon Fr_O(X) \hookrightarrow Fr(X)$ and given finally a local section $\sigma$ of $Fr_O(X)$, then the vielbein field with respect to that local trivialization is the [[pullback of differential forms|pullback]] form

$$
 \tau = \sigma^\ast i^\ast \tau_b
  \,.
$$

(exposition of this in the wider context of [[integrability of G-structures]] includes [Lott 90, p. 4](#Lott90)).

## Related concepts

* [[reduction of structure groups]], [[orthogonal structure]]

* [integrability of G-structures -- Examples -- Orthogonal structure](integrability+of+G-structures#ExamplesOrthogonalStructure)

* [[super-vielbein]]

* [[generalized vielbein]], [[exceptional generalized geometry]]


See also at [[field (physics)]] the section on _[Ordinary gravity](field%20%28physics%29#OrdinaryGravity)_.

## References

Original discussion in [[Élie Cartan]]'s reformulation of [[Riemannian geometry]] ([[Cartan geometry]]):

* [[Élie Cartan]] (translated by Vladislav Goldberg from Cartan's lectures at the Sorbonne in 1926–27): Chapter 1 of: *Riemannian Geometry in an Orthogonal Frame*, World Scientific (2001) &lbrack;[doi:10.1142/4808](https://doi.org/10.1142/4808), [pdf](https://softbank.iust.ac.ir/MathBooks/c/Cartan%20-%20Riemannian%20Geometry%20in%20an%20Orthogonal%20Frame.pdf)&rbrack;

Lecture notes:

* {#Wang24} [[Zuoqin Wang]], *The method of moving frames*, Lecture 11 in: *Riemannian geometry* (2024) &lbrack;[webpage](http://staff.ustc.edu.cn/~wangzuoq/Courses/24S-RiemGeom/), [pdf](http://staff.ustc.edu.cn/~wangzuoq/Courses/24S-RiemGeom/Notes/Lec11.pdf)&rbrack;



Review in the context of [[first-order formulation of gravity]]:

* [[Pietro Fré]], §3.2.5, §5.2.1 in: *Gravity, a Geometrical Course*, Volume 1: *Development of the Theory and Basic Physical Applications*, Spinger (2013) &lbrack;[doi:10.1007/978-94-007-5361-7](https://doi.org/10.1007/978-94-007-5361-7)&rbrack;


Discussion in the general context of [[G-structures]] includes

* {#Lott90} [[John Lott]], _The Geometry of Supergravity Torsion Constraints_, Comm. Math. Phys. 133 (1990), 563&#8211;615, (exposition in [arXiv:0108125](http://arxiv.org/abs/math/0108125))



[[!redirects vielbeine]]
[[!redirects vielbeins]]

[[!redirects vierbein]]
[[!redirects vierbein field]]


[[!redirects soldering form]]
[[!redirects soldering forms]]

[[!redirects vielbein field]]
[[!redirects vielbein fields]]

[[!redirects solder form]]
[[!redirects solder forms]]


[[!redirects soldering form]]
[[!redirects soldering forms]]

[[!redirects moving frame]]
[[!redirects moving frames]]

[[!redirects Cartan moving frame]]
[[!redirects Cartan moving frames]]



