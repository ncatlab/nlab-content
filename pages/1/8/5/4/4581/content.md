
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Variational calculus
+-- {: .hide}
[[!include variational calculus - contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

For $X$ a ([[spacetime]]) [[manifold]] and $E \to X$ a [[bundle]] (in [[physics]] called the _[[field bundle]]_) with [[jet bundle]] $Jet(E) \to X$, the **variational bicomplex** is essentially the [[de Rham complex]] $\Big(\Omega^\bullet\big(Jet(E)\big),\mathbf{d}\Big)$ of $Jet(E)$ with [[differential forms]] $\Omega^n\big(Jet(E)\big) = \bigoplus_{h+v=n} \Omega^{h,v}(E)$ bigraded by [[horizontal differential form|horizontal]] degree $h$ (with respect to $X$) and vertical degree $v$ (along the [[fiber]]s of $j_\infty E$)). Accordingly, the [[differential]] decomposes as

$$
  \mathbf{d} 
    = 
   d + \delta
  \,,
$$

where $\mathbf{d}$ is the [[de Rham differential]] on $Jet(E)$ and where $d$ is called the **horizontal differential** and $\delta$ is called the **vertical differential**.

With $E \to X$ thought of as a [[field bundle]] over [[spacetime]]/[[worldvolume]], then $d$ is a measure for how quantities change over spacetime, while $\delta$ is the [[variational calculus|variational]] differential that measures how quantities change as the field configurations are varied.


Accordingly, much of the [[variational calculus]] involved in [[classical mechanics]] and [[Lagrangian field theory|Lagrangian]] [[classical field theory]] on $X$ (the "[[principle of extremal action]]") is formalized in terms of the variational bicomplex. For instance 

* a field configuration is a [[section]] of $E$;

* a [[Lagrangian density]] is an element $L \in \Omega^{n,0}(E)$;

* a [[local action functional]] is a map

  $$
    S : \Gamma(E) \to \mathbb{R}
  $$

  of the form

  $$
    S(\phi) = \int_X L(j^\infty \phi)
    \,,
  $$

* the [[Euler-Lagrange equation]] is 

  $$
    E(L) \coloneqq \delta L \mod im d = 0
  $$

* the [[covariant phase space]] is the locus 

  $$
    \big\{
     \phi \in \Gamma(E) | E(L)(j^\infty \phi) = 0
   \big\}
  $$

* a [[conserved current]] is an element $\eta\in \Omega^{n-1,0}(E)$ that is  horizontally closed on the covariant phase space

  $$
    d \eta = 0 \mod E(L)
  $$

* a [[symmetry]] is an [[evolutionary vector field]] $v$ such that
  
  $$
    v(L) = 0 \mod im d
  $$

* [[Noether's theorem]] asserts that every [[symmetry]] induces a [[conserved current]].


## Definition

Let $X$ be a [[smooth manifold]] and $p : E \to X$ some smooth [[bundle]] over $X$. Write $Jet(E) \to X$ for the corresponding [[jet bundle]].

### The bicomplex

The spaces of [[sections]] $\Gamma(E)$ and $\Gamma(Jet(E))$ canonically inherit a generalized smooth structure that makes them [[diffeological spaces]]: we have a [[pullback]] [[diagram]] of diffeological spaces

$$
  \array{
     \Gamma(E) & \longrightarrow & *
     \\
     \downarrow && \downarrow^{id}
     \\
     [X,E] &\stackrel{p_*}{\longrightarrow}& [X,X]
  }
  \,.
$$

This induces the [[evaluation map]]

$$
  X \times \Gamma(E) \to E
  \,.
$$

and composed with the jet prolongation

$$
  j^\infty : \Gamma(E)  \to \Gamma(Jet(E))
$$

it yields a smooth map ([[homomorphism]] of [[diffeological spaces]]) 

\[
  \label{EProlongation}
  e_\infty : X \times \Gamma(E) \stackrel{(id,j^\infty)}{\to}
   X \times \Gamma(Jet(E))
   \stackrel{ev}{\to}
  Jet(E)
  \,.
\]

Write 

$$
  \Omega^{\bullet, \bullet}(X \times \Gamma(E))
$$

for the [[cochain complex]] of smooth differential forms on the [[product]] $X \times \Gamma(E)$, bigraded with respect to the differentials on the two factors

$$
  \mathbf{d} \coloneqq d + \delta
  \,,
$$

where the $\mathbf{d}$, $d$ and $\delta$, are the [[de Rham differentials]] of $X\times\Gamma(E)$, $X$ and $\Gamma(E)$, respectively.


+-- {: .num_defn }
###### Definition

The **variational bicomplex** of $E \to X$ is the sub--bi-complex of $\Omega^{\bullet, \bullet}(X \times \Gamma(E))$ that is the [[image]] of the pullback of forms along the map $e_\infty$ (eq:EProlongation):

$$
  e_\infty^* : \Omega^{\bullet}(Jet(E)) \to 
   \Omega^\bullet(X \times \Gamma(E))
  \,.
$$

We write 

$$
  \Omega^{\bullet, \bullet}_{loc}
  \coloneqq
  im (e_\infty^*)
$$

and speak of the bicomplex of **local forms** on sections on $E$.

=--

The bicomplex structure on $\Omega^{\bullet, \bullet}_{loc}$ is attributed by [Olver 1986](#Olver86) to [Takens 1979](#Takens79). The above formulation as a sub-bicomplex of the evident bicomplex of forms on $X \times \Gamma(E)$ is due to &lbrack;[Zuckerman 87, p. 5](#Zuckerman87)&rbrack;.

<img src="https://ncatlab.org/nlab/files/VariationalBicomplex.jpg" width="550">

### More on the horizontal differential complex
 {#MoreOntheHorizontalComplex}

+-- {: .num_remark #CharacterizationOfHorizontalDifferential}
###### Remark

In terms of a [[coordinate chart]] $(x^i, u^\alpha,u^\alpha_i,u^\alpha_{i j},\cdots)$ of $E$ covering a coordinate chart $(X^i)$ of $X$, the action of the horizontal differential on functions $f \in C^\infty(Jet(E))$ is given by the formula for the [[total derivative]] operation, but with concrete differentials substituted by the respective jet coordinates:

$$
  d_h f 
    \;\coloneqq\; 
  \sum_i
  \left(
    \frac{\partial f}{\partial x^i}
    + 
    \frac{\partial f}{\partial u^\alpha}u^\alpha_i
    +
    \sum_j \frac{\partial f}{\partial u^\alpha_j} u^\alpha_{j i}
    +
    \cdots
  \right)
  d x^i
  \,.
$$

([Anderson 89, p. 10](#Anderson89)). 

=--

More abstractly, the horizontal differential is characterized as follows:

+-- {: .num_prop #HorizontalDifferentialCompatibleWithPullbackAlongJetProlongations}
###### Proposition

The horizontal differential takes horizontal forms to horizontal forms, and for all sections $\phi \in \Gamma(E)$ it respects [[pullback of differential forms]] along the jet prolongation $j_\infty \phi \in \Gamma(Jet(E))$

$$
  (j^\infty \phi)^\ast \circ d_h = d \circ (j^\infty \phi)^\ast
$$

(where on the right we have the ordinary de Rham differential on the base space).


=--

Yet more abstractly, the horizontal complex may be understood in terms of [[differential operators]] and the [[jet comonad]] as follows.

+-- {: .num_remark #HorizontalComplexViaDifferentialOperators}
###### Remark

A horizontal differential $n$-form $\alpha$ on $Jet(E) \to X$ is equivalently a homomorphism of [[bundles]] over $X$ 

$$
  \alpha \colon Jet(E) \longrightarrow \wedge^n T^\ast X
$$

from the [[jet bundle]] $Jet(E)$ to the [[exterior bundle]] $\wedge^n T^\ast X$. This in turn is, by the discussion there, equivalently a [[differential operator]] $\alpha \colon E \to \wedge^n T^\ast X$.

Now of course also the [[de Rham differential]] $d_X$ on $X$ is a differential operator $\wedge^n T^\ast X \to \wedge^n T^\ast X$. In view of this, the horizontal differential of the variational bicomplex is just the [[composition]] operation of differential operators, with horizontal forms regarded as differential operators as above.

By the fact that differential operators are the [[co-Kleisli morphisms]] of the [[Jet comonad]], this means that the horizontal differential is

$$
  d_H \alpha
  \colon
  Jet(F)
  \longrightarrow
  Jet(Jet(F))
  \stackrel{Jet(\alpha)}{\longrightarrow}
  Jet(\wedge^n T^\ast X)
  \stackrel{\tilde d_X}{\longrightarrow}
  \wedge^n T^\ast X
  \,.
$$



=--

(e.g. [Krasil'shchik-Verbovertsky 98, around def. 3.27](#KrasilshchikVerbovertsky98), [Krasil'shchik-Vinogradov 99, ch 4, around def. 1.8](#KrasilshchikVinogradov99)) 


































### Evolutionary vector fields

Vector fields on $J^\infty E$ also split into a direct sum of **vertical** and **horizontal** ones, respectively being annihilated by contraction with any horizontal $1$-forms or with any vertical $1$-forms, $\mathfrak{X}(J^\infty E) = \mathfrak{X}_H(J^\infty E) \oplus \mathfrak{X}_V(J^\infty E)$. A special kind of vertical vector field $v \in \mathfrak{X}_V(J^\infty E)$ is called an **[[evolutionary vector field]]** provided it satisfies $\mathcal{L}_v d = d \mathcal{L}_v$ and $\mathcal{L}_v = \iota_v \delta + \delta \iota_v$, we denote the subspace of evolutionary vector fields as $\mathfrak{X}_{ev}(J^\infty E) \subset \mathfrak{X}_V(J^\infty E)$.


## Properties

### Horizontal, vertical, and total cohomology

Let $E \to X$ be a smooth [[fiber bundle]] over a base [[smooth manifold]] $X$ of [[dimension]] $n.$ Write $J^\infty E \to X$ for the [[jet bundle]] of $E\to X$. 

Write 

$$
  \mathcal{F}^s(J^\infty E) \coloneqq I (\Omega^{n,s}(J^\infty E))
$$ 

for the projection of $(n,s)$-forms to the image of the "interior Euler operator" ([Anderson 89, p. 21 (50/318)](#Anderson89)).

+-- {: .num_prop #ELComplexHasSameCohomologyAsDeRhamComplex}
###### Proposition
**(Takens acyclicity theorem)**


The [[cochain cohomology]] of the [[Euler-Lagrange complex]]

$$
 0 \to \mathbb{R}
 \to
  \Omega^{0,0}(J^\infty E)
  \stackrel{d_H}{\to}
  \Omega^{1,0}(J^\infty E)
  \stackrel{d_H}{\to}
  \cdots 
  \stackrel{d_H}{\to}
  \Omega^{n,0}(J^\infty E)
  \stackrel{E}{\to}
  \mathcal{F}^1(J^\infty E)
  \stackrel{\delta_V}{\to}
  \mathcal{F}^2(J^\infty E)
  \stackrel{\delta_V}{\to}
  \cdots
$$

is [[isomorphism|isomorphic]] to the [[de Rham cohomology]] of the total space $E$ of the given fiber bundle.

=--

For smooth functions of locally bounded jet order this is due to ([Takens 79](#Takens79)). A proof is also in ([Anderson 89, theorem 5.9](#Anderson89)).

For smooth functions of globally bounded order and going up to the Euler-Lagrange operator $E$, this is also shown in ([Deligne 99, vol 1, p.188](#Deligne99)).

### The fundamental variational formula

+-- {: .num_defn }
###### Definition {#BicomplexDefinition}

A **source form** is an element $\alpha$ in $\Omega^{n,1}_{loc}$ such that

$$
  \alpha_\phi(\delta \phi)
$$

depends only on the 0-jet of $\delta \phi$.


=--

+-- {: .num_prop #VariationOfLagrangian}
###### Proposition

Let $L \in \Omega^{n,0}_{loc}$.

Then there is a unique source form $E(L) $ such that

$$
  \delta L = E(L) - d \Theta
  \,.
$$

Moreover

* $E(L)$ is independent of changes of $L$ by $d$-exact terms:

  $$
    E(L) = E(L + d K)
    \,.
  $$

* $\Theta$ is unique up to $d$-exact terms.

=--

This is &lbrack;[Zuckerman 87, theorem 3](#Zuckerman87)&rbrack;.

Here $E$ is the _[[Euler-Lagrange equations|Euler-Lagrange operator]]_ .

+-- {: .num_defn }
###### Definition

Write

$$
  \Omega = \delta \Theta
  \,.
$$

=--

+-- {: .num_remark #HorizontalDOfOmega}
###### Remark

By prop. \ref{VariationOfLagrangian} have

$$
  d \Omega = -\delta E(L)
  \,.
$$

=--

+-- {: .num_prop #SecondOrderVariationVanishesOnShell}
###### Proposition

$\delta E$ vanishes when restricted to vertical tangent vectors based in [[covariant phase space]] (but not necessarily tangential to it).

$$
  \delta E(L) |_{T_{E(L) = 0} \Gamma(E)} = 0
  \,.
$$

=--

This is &lbrack;[Zuckerman 87, lemma 8](#Zuckerman87)&rbrack;.

### Presymplectic covariant phase space

+-- {: .num_cor }
###### Corollary

The form $\Omega$ is a [[conserved current]].

=--

+-- {: .proof}
###### Proof

By remark \ref{HorizontalDOfOmega} and 
prop. \ref{SecondOrderVariationVanishesOnShell}.

=--

+-- {: .num_defn #ThePresymplecticForm}
###### Definition

For $\Sigma \subset X$ a [[compact space|compact]] [[closed manifold|closed]] submanifold of [[dimension]] $n-1$, one says that 

$$
  \omega \coloneqq \int_\Sigma \Omega \in \Omega^{0,2}_{loc}
$$

is the [[presymplectic structure]] on [[covariant phase space]] relative to $\Sigma$.


=--

+-- {: .num_prop }
###### Proposition

The 2-form $\omega$ is indeed closed

$$
  \delta \omega = 0
$$

and in fact exact: 

$$
  \theta \coloneqq \int_\Sigma \Theta
$$

is its _presymplectic potential_ .

$$
  \delta \theta  = \omega
  \,.
$$

=--

### Symmetries

Let $L \in \Omega^{n,0}_{loc}$.

+-- {: .num_defn }
###### Definition

An evolutionary vertical vector field $v \in \mathfrak{X}_{ev}(J^\infty E)$ is a **[[symmetry]]** if

$$
  v(L) = 0 \mod im d
  \,.
$$

=--

+-- {: .num_prop }
###### Proposition

The presymplectic form $\omega$ from def. \ref{ThePresymplecticForm} is annihilated by the Lie derivative of the vector field on $\Gamma(E)$ induced by a symmetry.

=--

This appears as &lbrack;[Zuckerman 87, theorem 13](#Zuckerman87)&rbrack;.

## Elementary formalization in differential cohesion
 {#FormalizationInDifferentialCohesion}

We discuss aspects of an [[elementary (infinity,1)-topos|elementary]] 
formalization in [[differential cohesion]] of the concept of the variational bicomplex .

> under construction

Let $\mathbf{H}$ be a context of [[cohesion]] and [[differential cohesion]], with  

* [[flat modality]] denoted $\flat$;

* [[infinitesimal shape modality]] denoted $\Im$. 

Choose 

1. an [[object]] $\Sigma \in \mathbf{H}$, the _base space_ (or _[[spacetime]]_ or _[[worldvolume]]_);

1. an object $E \in \mathbf{H}_{/\Sigma}$, the _[[field bundle]]_,

1. an object $\mathbf{A} \in Stab(\mathbf{H}_{/\Sigma}) \stackrel{\Omega}{\to} \mathbf{H}_{/\Sigma}$, the _[[differential cohomology|differential]] [[coefficients]]_.

Write 

* $\mathbf{H}_{/\Sigma}
    \stackrel{\overset{\sum_\Sigma}{\longrightarrow}}{\stackrel{\overset{\Sigma^\ast}{\longleftarrow}}{\underset{\prod_\Sigma}{\longrightarrow}}}
    \mathbf{H}$ 
  for the [[base change]] [[adjoint triple]] over $\Sigma$, the [[étale geometric morphism]] of the [[slice (infinity,1)-topos]] $\mathbf{H}_{/\Sigma}$; 

* $\Gamma_X \coloneqq \flat \circ \prod_\Sigma \colon \mathbf{H}_{/\Sigma} \to \mathbf{H}$ for the external [[space of sections]] functor;


* $i \colon \Sigma \longrightarrow \Im(\Sigma)$ for the $\Sigma$-component of the [[unit of a monad|unit]] of $\Im$;

* $Jet_\Sigma \coloneqq i^\ast i_\ast$ for the induced [[jet comonad]];


* $\mathbf{H}_{/\Sigma} \stackrel{\overset{}{\longleftarrow}}{\underset{\iota}{\longrightarrow}} PDE(\mathbf{H})_{\Sigma}$ for the [[Eilenberg-Moore category]] of $Jet_\Sigma$-[[algebras over a monad|coalgebras]] (the objects are [[differential equations]] with [[variables]] in $\Sigma$, the morphisms are [[differential operators]] between these, preserving solution spaces), manifested as a [[topos of coalgebras]] over $\mathbf{H}$;

  the (non-full) [[direct image]] of this [[geometric morphism]] is the [[co-Kleisli category]] of the [[jet comonad]] and so for $\phi \colon free(E) \to free(F)$ a morphism in $PDE(\mathbf{H})_\Sigma$, we write $\tilde f \colon Jet(E) \to F$ for the corresponding co-Kleisli morphism in $\mathbf{H}_{/\Sigma}$;


We record the following simple fact,
which holds generally since the [[jet comonad]] $Jet_\Sigma$ is a [[right adjoint]] 
(to the [[infinitesimal disk bundle]] functor), hence preserves [[terminal objects]], and $\Sigma \in \mathbf{H}_{/\Sigma}$ is the [[terminal object]]:

+-- {: .num_prop #JetSigmaPreservesSigma}
###### Proposition

The essentially unique morphism 

$$
  Jet(\Sigma) \stackrel{\simeq}{\longrightarrow} \Sigma
$$

in $\mathbf{H}_{/\Sigma}$ in an [[equivalence]].

=--

+-- {: .num_defn #JetProlongationInDifferentialCohesion}
###### Definition

The _jet prolongation_ map

$$
  j \colon \Gamma_\Sigma(E) \longrightarrow \Gamma_\Sigma(Jet(E))
$$

is the the Jet functor itself, regarded,
in view of prop. \ref{JetSigmaPreservesSigma}, 
as taking [[sections]] to sections via

$$
  (\Sigma \stackrel{\sigma}{\to} E)
  \;\;\mapsto
  \;\;
  \left(
  \Sigma \stackrel{\simeq}{\to} Jet(\Sigma)
  \stackrel{Jet(\sigma)}{\longrightarrow}
  Jet\left(E\right)
  \right)
  \,.
$$

=--

+-- {: .num_defn #HorizontalFormInDifferentialCohesion}
###### Definition


For $E \in \mathbf{H}_{\Sigma}$ a [[bundle]] over $\Sigma$, 
then a _horizontal $\mathbf{A}$-form_ on the [[jet bundle]]
$Jet(E)$ is a morphism in $PDE(\mathbf{H})_{\Sigma}$ of the form

$$
  \alpha \colon \iota E \to \iota  \mathbf{A}
  \,.
$$

For $d \colon \iota Et_\Sigma\Sigma^\ast \mathbf{A}\to \iota Et_\Sigma\Sigma^\ast \mathbf{A}'$ a morphism in $\mathbf{PDE}(\mathbf{H})_{\Sigma}$, then 
the induced _horizontal differential_ is the operation of horizontal forms sending $\alpha$ to the composite

$$
  d \alpha \colon \iota E 
     \stackrel{\alpha}{\longrightarrow} 
  \iota \mathbf{A} 
   \stackrel{d}{\longrightarrow} \iota \mathbf{A}'
  \,.
$$


=--

+-- {: .num_remark }
###### Remark

Since all objects in def. \ref{HorizontalFormInDifferentialCohesion}
are in the [[co-Kleisli category]] of the [[jet comonad]], the morphism $\alpha$ there is equivalently a morphism in $\mathbf{H}_{/\Sigma}$ of the form

$$
  \tilde \alpha \colon Jet(E) \longrightarrow \mathbf{A}
  \,.
$$

For the special case that $E = \Sigma$ in def. \ref{HorizontalFormInDifferentialCohesion}, then $Jet_{\Sigma}(\Sigma)\simeq\Sigma$ and so a horizontal $\mathbf{A}$-form on $\Sigma$ we call just a an $\mathbf{A}$-form.

=--

+-- {: .num_prop}
###### Proposition

The horizontal differential of def. \ref{HorizontalFormInDifferentialCohesion} commutes with pullback of horizontal differential forms $\alpha$ along the jet prolongation, def. \ref{JetProlongationInDifferentialCohesion}, of any field section $\sigma \in \Gamma_X(E)$.

In detail: for 

* $d \colon \iota Et_\Sigma\Sigma^\ast \mathbf{A} \longrightarrow \iota Et_\Sigma\Sigma^\ast \mathbf{A}'$ a morphism, 

* $\alpha \colon \iota E \to \iota Et_\Sigma\Sigma^\ast \mathbf{A}$ a horizontal $\mathbf{A}$-form on $Jet(E)$, def. \ref{HorizontalFormInDifferentialCohesion};

* $\sigma \in \Gamma_\Sigma(E)$ a [[field (physics)|field]] [[section]],

then there is a [[natural equivalence]]

$$
  j(\sigma)^\ast (d \alpha)
   \simeq
  d (j(\sigma)^\ast \alpha)  
  \,.
$$

=--

+-- {: .proof}
###### Proof


Since all objects are in the [[direct image]] $free\colon \mathbf{H} \to PDE(\mathbf{H})_\Sigma$, this is an equivalence of morphisms in the [[co-Kleisli category]] of the [[jet comonad]], hence is equivalently an equivalence of co-Kleisli composites of morphisms in $\mathbf{H}$.

As such, the left hand side of the equality is given in $\mathbf{H}$ by the composite morphism

$$
  \Sigma
  \stackrel{\simeq}{\to}
  Jet(\Sigma)
   \stackrel{Jet(\sigma)}{\longrightarrow}
  Jet(E)
  \stackrel{}{\to}
  Jet(Jet(E))
  \stackrel{Jet(\tilde \alpha)}{\longrightarrow}
  Jet(\mathbf{A})
  \stackrel{\tilde d}{\longrightarrow}
  \mathbf{A}'
  \,,
$$

thought of as bracketed to the right. By [[natural transformation|naturality]] of the Jet-counit this is equivalently

$$
  Jet(\Sigma) \stackrel{\simeq}{\to} Jet(Jet(\Sigma))
  \stackrel{Jet(Jet(\sigma))}{\longrightarrow}
  Jet(Jet(E))
  \stackrel{Jet(\tilde \alpha)}{\longrightarrow}
  Jet(\mathbf{A})
  \stackrel{\tilde d}{\longrightarrow}
  \mathbf{A}'
  \,,
$$


By functorality of $Jet(-)$ this is equivalent to

$$
  Jet(\Sigma) 
  \stackrel{\simeq}{\to}
  Jet(Jet(\Sigma)) \stackrel{Jet ( \tilde \alpha \circ Jet(\sigma) )}{\longrightarrow}
  Jet(\mathbf{A})
  \stackrel{\tilde d}{\to}
  \mathbf{A}'
$$ 

which is the right hand side of the equivalence to be proven.

=--


## Related concepts

* [[local Lagrangian]], [[Euler-Lagrange form]], [[source form]], [[Lepage form]]

* [[variational calculus]]

* [[secondary differential calculus]]

* [[variational sequence]]

* [[BV-BRST complex]]

* [[BV-BRST variational bicomplex]]

* [[presymplectic current]], [[covariant phase space]]

## References

The earliest occurrence of the variational bicomplex in the literature is in Section 2.2 of

* [[D. B. Fuchs]], A. M. Gabrielov, [[I. M. Gel'fand]], _The Gauss-Bonnet theorem and the Atiyah-Patodi-Singer functionals for the characteristic classes of foliations_, Topology 15:2 (1976), 165-188.  [DOI][FGG]
[FGG]: https://doi.org/10.1016/0040-9383(76)90007-0

which attributes it to [[Israel Gelfand]] and [[Mark Losik]].

Further work appeared independently in

* [[Alexandre Vinogradov]], _A spectral sequence associated with a non-linear differential equation, and the algebro-geometric foundations of Lagrangian field theory with constraints_, Soviet Mathematics Doklady 19:1 (1978) 144–148.  [PDF](https://dmitripavlov.org/scans/vinogradov-a-spectral-sequence-associated-with-a-nonlinear-differential-equation-and-algebro-geometric-foundations-of-lagrangian-field-theory-with-constraints.pdf).  Russian original: А. М. Виноградов, _Одна спектральная последовательность, связанная с нелинейным дифференциальным уравнением и алгебро-геометрические основания лагранжевой теории поля со связями_, Доклады АН СССР, 238:5 (1978), 1028–1031.  [PDF](https://www.mathnet.ru/rus/dan/v238/i5/p1028).

* W. M. Tulczyjew, _The Euler-Lagrange resolution_, Lecture Notes in Mathematics 836 (1980), 22–48.  [DOI](https://doi.org/10.1007/bfb0089725).


See also

* Toru Tsujishita, _On variation bicomplexes associated to differential equations_, Osaka J. Math. 19:2 (1982), 311–363.  [Project Euclid](http://projecteuclid.org/euclid.ojm/1200775039).

* {#Takens79} [[Floris Takens]], _A global version of the inverse problem of the calculus of variations_, J. Diff. Geom. 14:4 (1979) 543–562.  [DOI](https://doi.org/10.4310/jdg/1214435235).

Chapter 2 (Lagrangian Theory of Classical Fields) in

* {#Deligne99} [[Pierre Deligne]], [[Daniel S. Freed]], _Classical Field Theory_, In: _[[Quantum Fields and Strings]]: A Course for Mathematicians_, Volume I, ISBN: 0-8218-1198-3.

An introduction is in 

* [[Ian Anderson]], _Introduction to the variational bicomplex_, in _Mathematical aspects of classical field theory_, Contemp. Math. 132 (1992) 51–73, [PDF](https://digitalcommons.usu.edu/mathsci_facpub/32/).

* Toru Tsujishita, _Formal geometry of systems of differential equations_, Sugaku Expositions 3:1 (1990), 25–73. [PDF](https://dmitripavlov.org/scans/tsujishita-formal-geometry-of-systems-of-differential-equations.pdf).  Japanese original: 辻下 徹. [微分方程式系の形式幾何学](https://doi.org/10.11429/sugaku1947.35.332). 数学 35:4 (1983), 332–357.  

A careful discussion that compares the two versions (one over smooth functions globally of finite jet order, one over smooth functions locally of finite jet order) is in

* G. Giachetta, L. Mangiarotti, [[Gennadi Sardanashvily]], _Cohomology of the variational bicomplex on the infinite order jet space_, Journal of
Mathematical Physics 42, 4272-4282 (2001) ([arXiv:math/0006074](http://arxiv.org/abs/math/0006074))

 
Textbook accounts include

* {#Olver86} [[Peter Olver]], section 5.4 of: *Applications of Lie groups to differential equations*, Graduate Texts in Mathematics **107**, Springer (1986, 1993) &lbrack;[doi:10.1007/978-1-4612-4350-2](https://doi.org/10.1007/978-1-4612-4350-2)&rbrack;

* {#Anderson89} [[Ian Anderson]], _The variational bicomplex_, Utah State University 1989 ([[AndersonVariationalBicomplex.pdf:file]]) 

* {#KrasilshchikVerbovetsky98} [[Joseph Krasil'shchik]], [[Alexander Verbovetsky]], _Homological Methods in Equations of Mathematical Physics_ ([arXiv:math/9808130](http://arxiv.org/abs/math/9808130))
 
* {#KrasilshchikVinogradov99} [[Joseph Krasil'shchik]],  [[Alexandre Vinogradov]] et al. (eds.) _Symmetries and  Conservation Laws for Differential Equations of Mathematical Physics_, AMS 1999

Other surveys include

* Juha Pohjanpelto, _Symmetries, Conservation Laws, and Variational Principles for Differential Equations_ (2014) ([pdf slides](http://math.usask.ca/~cheviakov/bluman2014/talks/Pohjanpelto.pdf))


An early discussion with application to [[covariant phase spaces]] and their [[presymplectic structure]] is in

* {#Zuckerman87} [[Gregg Zuckerman]], *Action principles and global geometry*, in: [[Shing-Tung Yau]] (ed.) *Mathematical Aspects of String Theory*, World Scientific (1987) 259-284 &lbrack;[[ZuckermanVariation.pdf:file]], [doi:10.1142/0383](https://doi.org/10.1142/0383)&rbrack;


An invariant version (under group action) is in

* [[Irina Kogan]], [[Peter Olver]], _The invariant variational bicomplex_, [pdf](http://www4.ncsu.edu/~iakogan/papersPDF/sivKoganOlver.pdf)

A more detailed version of this is in

* [[Irina Kogan]], [[Peter Olver]], _Invariant Euler-Lagrange Equations and the Invariant Variational Bicomplex_, [pdf](http://www4.ncsu.edu/~iakogan/papersPDF/ivbKoganOlver-cor.pdf)

See also 

* [[Victor Kac]], _An explicit construction of the complex of variational calculus and Lie conformal algebra cohomology_, talk at Algebraic Lie Theory, Newton Institute 2009, [video](http://sms.cam.ac.uk/media/538761)

An application to [[multisymplectic geometry]] is discussed in

* Thomas Bridges, Peter Hydon, Jeffrey Lawson, _Multisymplectic structures and the variational bicomplex_  ([pdf](http://personal.maths.surrey.ac.uk/st/T.Bridges/PAPERS/MPCPS-Paper-09024.pdf))

Discussion in the context of [[supergeometry]] is in 

* [[Gennadi Sardanashvily]], _Grassmann-graded Lagrangian theory of even and odd variables_ ([arXiv:1206.2508](https://arxiv.org/abs/1206.2508))

Discussion in the convenient context of [[smooth sets]]:

* {#GiotopoulosSati23} [[Grigorios Giotopoulos]], [[Hisham Sati]], §5.1 & §7.1 in: *Field Theory via Higher Geometry I: [[schreiber:Smooth Sets of Fields]]* &lbrack;[arXiv:2312.16301](https://arxiv.org/abs/2312.16301)&rbrack;


[[!redirects horizontal derivative]]
[[!redirects horizontal derivatives]]

[[!redirects vertical derivative]]
[[!redirects vertical derivatives]]

[[!redirects variational differential form]]
[[!redirects variational differential forms]]

[[!redirects total spacetime derivative]]
[[!redirects total spacetime derivatives]]

[[!redirects horizontal variational complex]]
[[!redirects horizontal variational complexes]]
