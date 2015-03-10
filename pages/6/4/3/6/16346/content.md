
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
#### Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

While _[[Cartan geometry]]_ was originally conceived of in the context of [[differential geometry]], its principles and constructions make sense much more generally. In particular they make sense in the context of [[supergeometry]]. The implementation of Cartan geometry in supergeometry may well be called _super-Cartan geometry_ or _Cartan super-geometry_. Where the original and motivating example for plain [[Cartan geometry]] was the formulation of [[Einstein gravity]] (via [[pseudo-Riemannian geometry]]), so super-Cartan geometry underlies and finds motivation from the formulation of [[supergravity]], see also the [Survey of (non-)existing literature below](#SurveyOfExistingLiterature).

While the general abstract [[theory]] of super-Cartan geometry proceeds in direct analogy with that of traditional Cartan geometry, the examples tend to exhibit a richer behaviour. Specifically for the case relevant to [[supergravity]] this is due to two facts:

1. The [[super Euclidean spaces]] and [[super-Minkowski spacetimes]], have, as [[super-translation groups]], [[non-abelian group|non-abelian]] [[supergroup]] structure, which is reflected in the fact that the [[left-invariant 1-forms]] ([[super differential forms]]) on these spaces are _not_ closed. This means that they carry natural intrinsic [[torsion of a G-structure]]. Due to this fact the super-Cartan geometry involved in [[supergravity]] is richer than its bosonic counterpart in a way that goes beyond the addition of "superpartners". For more on this see also at _[[torsion constraints of supergravity]]_.

1. In particular [[super-Minkowski spacetimes]] carry non-trivial exceptional [[super Lie algebra]] [[Lie algebra cohomology|cocycles]]. Their globalization as [[definite forms]] is hence [[analogy|analogy]] to what is known in the bosonic case for instance for [[G2-structure]]. These globalizations play a key role in the discussion of [[super p-brane]] [[sigma-models]] on curved [[supergravity]] backgrounds. Moreover, these cocycles classify [[super L-infinity algebra]] [[L-infinity algebra cohomology|extensions]] of [[super Minkowski spacetime]] known as [[extended super Minkowski spacetimes]]. This is the origin of much of [[higher Cartan geometry]] within super-Cartan geometry.


## Survey of (non-)existing literature
 {#SurveyOfExistingLiterature}

While the terminology "super-Cartan geometry" is not much used traditionally (but see ([Egeileh-Chami 13](#EgeilehChami13))), nevertheless the key ingredients of super-Cartan geometry are well known in the literature, and all the more is it useful to make them explicit as what they are.

Physics literature usually refers to the "superspace formulation" of [[supergravity]] when referring to the formulation of the theory in [[supergeometry]]. Essentially all of the literature on [[supergravity]] formulated in "superspace" is implicitly about super-Cartan geometry for the inclusion of a [[spin group]]-[[double cover]] of the [[Lorentz group]] inside a [[super Poincaré group]], in direct analogy to how ordinary [[Einstein gravity]] ([[pseudo-Riemannian geometry]]) is the Cartan geometry of the inclusion of a [[Lorentz group]] inside a plain [[Poincaré group]] -- this in fact being Cartan's original and motivating example for the whole theory. Where physicists speak of "locally gauging [[supersymmetry]]" the mathematical formulation of that is precisely this: the "[[supersymmetry]]" [[supergroup]] is the [[super Poincaré group]] [[action|acting]] on [[super Minkowski spacetime]], and "locally gauging" it means exactly to consider [[spacetimes]] that are locally ([[tangent space]]-wise) modeled on [[super Minkowski space]], while globally varying according to a [[Lorentz group]]-[[G-structure]], hence the super-analog of a [[pseudo-Riemannian metric]].

One physics references which makes the super-Cartan-geometric picture of [[supergravity]] very explicit is ([D'Auria-Fre 82](#DAuriaFre82), [Castellani-D'Auria-Fre 91](#CastellaniDAuriaFre91)). (These authors in fact also make the [[higher Cartan geometry]] hidden here fairly explicit, see there and see at [[D'Auria-Fré formulation of supergravity]].), even though these authors do not use this mathematical terminology. Similarly, discussion of super-[[Klein geometry]] in the context of [[supergravity]] is, even if not exactly in this terminology, rather explicit in ([Figueroa-O'Farrill 08](#FigueroaOFarrill08)). 

A reference that very clearly identifies the role of the mathematics of supergeometric [[G-structures]] (which is the relevant special class of super-Cartan geometry) in [[supergravity]] is ([Lott 01](#Lott01)). The followup ([Egeileh-Chami 13](#EgeilehChami13)) to that article finally makes the terminology "Cartan geometry" fully explicit in this supergeometric context. These authors observe for instance that from this perspective the traditional concept of _[[Killing spinor]]_ -- which involves an extra "weakening" parameter in addition to the plain concept of a _[[covariantly constant spinor]]_ -- is naturally understood as being in fact a covariantly constant spinor, but for a different model super-[[Klein geometry]] $G/H$.

This provides ample example and application of super-Cartan geometry for the case where $G/H$ is a [[super vector space]], hence for the case corresponding to [[G-structure]]. More general super-Cartan geometry apparently remains to be explored.




## Introduction

### The solid topos

It is traditional to introduce the concept of [[supermanifolds]] in the form of [[locally ringed topological spaces]]. There is however a more direct and maybe more illumimnating way following instead the spirit of the discussion at _[[geometry of physics -- smooth sets]]_.

#### Coordinate systems: super-Cartesian spaces

Recall the following from the discussion at _[[geometry of physics -- smooth sets]]_.


+-- {: .num_defn}
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
 Smooth0Tpye \coloneqq Sh(CartSp) 
$$

for the [[sheaf topos]] of all these.

=--

+-- {: .num_remark}
###### Remark

The useful way to think of def. \ref{Smooth0Type} in the present context is as defining a kind of [[generalized smooth space]] which is _defined_ by which smooth function from Cartesian spaces it receives (see also at _[[motivation for sheaves, cohomology and higher stacks]]_ for more exposition of this point).

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

Hence given any $X \in Smooth0Type$, we are entitled to think of it as a [[generalized smooth space]] which need not be given as a [[set]] equipped with [[smooth structure]], but whose nature we instead we detect or _probe_ by mapping Cartesian spaces into it: given  $\mathbb{R}^n$ then we think of the set $X(\mathbb{R}^n)$ which $X$, being a [[sheaf]] on [[CartSp]], assigns, as playing the role of the set of all smooth functions "$\mathbb{R}^n \longrightarrow X$" into the would-be space $X$. 

The [[Yoneda lemma]] gives that this is not circular, but consistent: once we identify Cartesian spaces themselves as smooth spaces via the Yoneda embedding, then this becomes literally true and we may remove the quotation marks:

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


[[superalgebra]], [[Grassmann algebra]]

[[super-Cartesian space]]

sheaves on that

formal super-Cartesian space

sheaves on that

* [[CartSp]] for the site of [[Cartesian spaces]];

* $InfPoint \coloneqq WAlg^{op}$ for the category of first-order [[infinitesimally thickened points]] (i.e. the [[abstract duality|formal duals]] of [[commutative algebras]] over the [[real numbers]] of the form $\mathbb{R}\oplus V$ with $V$ a finite-dimensional  square-0 [[nilpotent ideal]]).

* $SuperPoint \coloneqq WAlg_{super}^{op}$ for the category of [[superpoints]], by which we here mean the [[formal duals]] to commutative [[superalgebras]] which 
are super-[[Weil algebras]].

There are then "semidirect product" sites $CartSp \rtimes InfinPoint$ and $CartSp \rtimes SuperPoint$ (whose objects are [[Cartesian products]] of the given form inside [[synthetic differential supergeometry]] and whose morphisms are all morphisms in that context (not just the product morphisms)).

Set then 

$$
  FormalSmooth0Type \coloneqq Sh(CartSp \rtimes InfPoint)
$$

for the collection of [[formal smooth ∞-groupoids]] (see there) and finally

$$
  SuperSmooth0Type \coloneqq Sh(CartSp \rtimes SuperPoint)
$$

#### The reflective categories

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
    SuperSmooth \infty Grpd
    \\
    & &\longleftarrow& &\longleftarrow&
    \\
    & &\hookrightarrow&
  }
$$



he total composite labeled $\Delta$ is indeed the [[locally constant infinity-stack]]-functor: let $X$ be any object in its image, and $U \times D_s \in CartSp \rtimes SuperPoint$. Then by adjunction $SuperSmooth\infty Grpd(U\times D_s, X)$ is equivalently homs in $FormalSmooth \infty Grpd$ of out the dual of the Weil algebra which is the quotient of the original one by the ideal generated by its odd part. Hence this, in turn, is equivalently homs in $Smooth\infty Grpd$ out of $U$ and that finally is equivalently homs in $\infty Grpd$ out of $\ast$ into the given $\infty$-groupoid.


Passing to the [[adjoint triples]] of [[idempotent monads]] and [[idempotent comonads]] which this induces, then yields 

* on the left the [[shape modality]] $\int$, [[flat modality]] $\flat$ and [[sharp modality]] $\sharp$, 

* in the middle yields the [[reduction modality]] $\Re$, the [[infinitesimal shape modality]] $\&$ and the [[infinitesimal flat modality]] $\Im$. 

* on the right we get an adjoint triple whose whose middle bit $\rightsquigarrow$ is the [[bosonic modality]] and whose left piece $\e$ produces _super-even_ components, containing all the "[[fermion]] [[currents]]" if one wishes , which in this [[unity of opposites]] hence deserves to be called the _[[fermionic modality]]_. The further right adjoint $\Re$ is the [[rheonomy modality]].

Hence we get a process of [[adjoint modalities]] of the form

$$
  \array{
    && id &\dashv& id 
    \\
    && \vee && \vee
    \\
    &\stackrel{fermionic}{}& \e &\dashv& \rightsquigarrow & \stackrel{bosonic}{}
    \\
    && \bot && \bot
    \\
    &\stackrel{bosonic}{} & \rightsquigarrow &\dashv& \R & \stackrel{rheonomic}{}
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

### Super-Cartan geometry

#### The super-Klein geometry: super-Minkowski spacetime

real [[spin representation]], 

Let $V$ be a quadratic vector space, def. \ref{QuadraticVectorSpace},
over the [[real numbers]] with [[bilinear form]] or Lorentzian [[signature]], hence $V = \mathbb{R}^{d-1,1}$ is [[Minkowski spacetime]] of some [[dimension]] $d$. 

The following table lists the irreducible real representations of $Spin(V)$ ([Freed 99, page 48](#Freed99)).

| $d$ | $Spin(d-1,1)$ | minimal real spin representation $N=S$ | $dim_{\mathbb{R}} S\;\;$ |  $V$ in terms of $S^\ast$ |  [[supergravity]] | 
|--|--|--|--|--|--|
| 1 | $\mathbb{Z}_2$ | $S$ real | 1 | $V \simeq (S^\ast)^{\otimes}^2$ |  |
| 2 | $\mathbb{R}^{\gt 0} \times \mathbb{Z}_2$ | $S^+, S^-$ real | 1 | $V \simeq ({S^+}^\ast)^{\otimes^2} \oplus ({S^-}^\ast)^{\otimes 2}$ |  |
| 3 | $SL(2,\mathbb{R})$ | $S$ real | 2 |  $V \simeq Sym^2 S^\ast$ |  |
| 4 | $SL(2,\mathbb{C})$ | $S_{\mathbb{C}} \simeq S' \oplus S''$ | 4 | $V_{\mathbb{C}} \simeq {S'}^\ast \oplus {S''}^\ast$ |  |
| 5 | $Sp(1,1)$ | $S_{\mathbb{C}} \simeq S_0 \otimes_{\mathbb{C}} W$ | 8 |  $\wedge^2 S_0^\ast \simeq \mathbb{C} \oplus V_{\mathbb{C}}$ |  |
| 6 | $SL(2,\mathbb{H})$ | $S^\pm_{\mathbb{C}} \simeq S_0^\pm  \otimes_{\mathbb{C}} W$ | 8 | $V_{\mathbb{C}} \simeq \wedge^2 {S_0^+}^\ast \simeq (\wedge^2 {S_0^-}^\ast)^\ast$ |  |
| 7 |  |  $S_{\mathbb{C}} \simeq S_0 \otimes_{\mathbb{C}} W$ | 16 |  $\wedge^2 S_0^\ast \simeq V_{\mathbb{C}} \oplus \wedge^2 V_{\mathbb{C}}$ |  |
| 8 |  | $S_{\mathbb{C}} \simeq S^\prime \oplus S^{\prime\prime}$ | 16 | ${S'}^\ast {S''}^\ast \simeq V_{\mathbb{C}} \oplus \wedge^3 V_{\mathbb{C}}$ |  |
| 9 |  | $S$ real | 16 |  $Sym^2 S^\ast \simeq \mathbb{R} \oplus V \wedge^4 V$ |  |
| 10 |   | $S^+ , S^-$ real | 16 | $Sym^2(S^\pm)^\ast \simeq V  \oplus \wedge_\pm^5 V$ | [[type II supergravity]] |
| 11 |   | $S$ real | 32 | $Sym^2 S^\ast \simeq V \oplus \wedge^2 V \oplus \wedge^5 V$ | [[11-dimensional supergravity]] |

Here $W$ is the 2-dimensional [[complex vector space]] on which the [[quaternions]] naturally act. 


The last column implies that in each dimension there exists a [[linear map]]

$$
  \Gamma \;\colon\; S^\ast \otimes S^\ast \longrightarrow \mathbb{R}^{d-1,1}
$$

which is 

1. symmetric;

1. $Spin(V)$-equivariant.

This allows to form the [[super Poincaré Lie algebra]] 
hence the [[super Poincaré group]] $sIso(d-1,1|N)$ in each of these cases. 


[[quotient]] by [[spin group]] is [[super-Minkowski spacetime]]

$$
  \mathbb{R}^{d-1,1|N} = sIso(d-1,1|N)/Spin(d-1,1)
  \,.
$$

#### The curved case

given $X,Y\in SuperSmooth0Type$ then a morphism $f \colon X\longrightarrow Y$ is a _[[local diffeomorphism]]_ if

$$
  \array{
    X &\longrightarrow& \Im X
    \\
    \downarrow^{\mathrlap{f}} && \downarrow^{\mathrlap{\Im f}}
    \\
    Y &\longrightarrow& \Im Y
  }
$$

is a [[pullback]] square. This comes down to being the appropriate [[synthetic differential supergeometry]]-version  of the traditional statement that $f$ is a local diffeo if the diagram of [[tangent bundles]]

$$
  \array{
    T X &\longrightarrow& X
    \\
    \downarrow^{\mathrlap{T f}} && \downarrow^{\mathrlap{f}}
    \\
    T Y &\longrightarrow& Y
  }
$$

given $V$ a [[super vector space]] and $X \in SuperSmooth0Type$, then we say that $X$ is a $V$-[[manifold]] if there is

$$
  \array{
    && U
    \\
    & \swarrow && \searrow
    \\
    V && && X
  }
$$

with both morphisms being local diffeos and the right one in addition being a [[1-epimorphism]].



## References

* {#DAuriaFre82}  [[Riccardo D'Auria]], [[Pietro Fré]] _[[GeometricSupergravity.pdf:file]]_, Nuclear Physics B201 (1982) 101-140 

* {#CastellaniDAuriaFre91} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], _[[Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991)

* {#Lott01} [[John Lott]], _The Geometry of Supergravity Torsion Constraints_ Comm. Math. Phys. 133 (1990), 563&#8211;615, (exposition in [arXiv:0108125](http://arxiv.org/abs/math/0108125))

* {#FigueroaOFarrill08} [[José Figueroa-O'Farrill]], _The homogeneity conjecture for supergravity backgrounds_, J.Phys.Conf.Ser.175:012002, 2009 ([arXiv:0812.1258](http://arxiv.org/abs/0812.1258))

* {#EgeilehChami13} Michel Egeileh, Fida El Chami, _Some remarks on the geometry of superspace supergravity_, J.Geom.Phys. 62 (2012) 53-60 ([spire](http://inspirehep.net/record/1333125))