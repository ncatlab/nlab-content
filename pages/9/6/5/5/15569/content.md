
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


> under construction

#Contents#
* table of contents
{:toc}

**Abstract** We discuss how the [[synthetic differential geometry]]-like axiomatics of _[[differential cohesion]]_ provides a theory of [[bundles]] and [[differential cohomology]] which has realizations not just in [[higher differential geometry]] but also in [[higher arithmetic geometry]] in a way that systematizes some of the [[analogies]] which motivate the [[geometric Langlands correspondence]].

## Motivation

A fruitful approach to mathematical theory is what might be called "inter-geometric", meaning that definitions and theorems make sense and hold when interpreted in different flavors of geometry. Examples are the [[GAGA principle]], the [[function field analogy]], the [[geometric Langlands correspondence|geometric]] [[Langlands correspondence]] and absolute [[F1]]-geometry. While in these examples the [[analogy]]  between different theories of geometry has been established case-by-case, there is by and large no meta-theory which would systematically imply the analogy. 

This is of practical concern for instance in the [[Langlands program]], where it is an open problem how the methods and insights which are deeply on the side of [[complex analytic geometry]], such as involving [[mirror symmetry]], might have incarnations on the [[arithmetic geometry]]-side. And vice-versa, the complex-analytic version of the conjecture was obtained by educated guessing via analogy from the arithmetic side in the first place, but this guesswork has been questioned ([[Problems in the theory of automorphic forms -- 45 years later|Langlands 14]]). Both of these issue would be resolved if one had an "inter-geometric" from which the correspondence both in [[arithmetic geometry]] and in [[complex-analytic geometry]] would both follow by restriction.

Another example, which maybe hasn't been duly recognized as such yet, is the construction of the refined [[Witten genus]] in the guise of the [[string orientation of tmf]]: here what is initially a concept in [[complex analytic geometry|complex analytic]] ([[supergeometry|super]]-)geometry is constructed by passage (via the construction of [[tmf]]) to the [[moduli stack of elliptic curves]] all the way down in [[arithmetic geometry]], and in fact then via the [[fracture theorems]] by its [[base change|base changes]] to [[p-adic geometry]] and to [[rational homotopy theory]] (and further to [[K(n)-local stable homotopy theory]]). There is thus a kind of [[p-adic string theory]] appearing here, which is however not of the kind that existing literature with such title would shed any light on. 

**[[quantization of 3d Chern-Simons theory]] and [[holographic principle|holographically]] of the [[WZW-model]]/the [[string]] **

| [[geometry]] |  [[worldvolume]]  |  moduli of [[field (physics)|fields]] | moduli of [[polarizations]]  |  [[geometric quantization]]/[[theta functions]] |
|------|----------|------------|---------|----|
| [[differential geometry]] |  [[worldsheet]] | [[moduli stack of bundles]] |   |  |
| [[complex analytic geometry]] | [[complex curve]]  |  [[Jacobian]]/moduli of [[stable vector bundle|(semi-)stable bundles]]  |  [[moduli stack of Riemann surfaces]] |  [[modular functor]], [[Witten genus]], ...  |
| [[arithmetic geometry]] |  [[arithmetic curve]]   | [[geometric Langlands correspondence|geometric Langlands]]/[[Tamagawa measures]] | [[moduli stack of curves]] |  [[equivariant elliptic cohomology]], [[string orientation of tmf]], ...  |

The construction of the bottom right items here is a ground-breaking accomplishment in [[algebraic topology]], but at least in view of the origin of the WZW-string and the [[Witten genus]] in [[string theory]] it maybe raises more questions than it solves: from the perspective of physics these are but the first example of a tower of higher dimensional [[brane]] phenomena, the next instance being the [[partition function]] of the [[M5-brane]] and then that of 10d [[string theory]] itself (see e.g. at _[[self-dual higher gauge theory]]_).  

| $k$ | $(4k+3)d$ [[higher dimensional Chern-Simons theory]] | form [[theta characteristics]] $\to$ | $(4k+2)d$ [[self-dual higher gauge theory]] |
|----|--------------|-----------|------------------|
| 0  | [[3d Chern-Simons theory]] |   |  [[WZW-model|chiral WZW-string]]/[[modular functor]]/[[equivariant elliptic cohomology]] |
| 1  | [[7d Chern-Simons theory]] |  |  self-2-2form on [[M5-brane]] |
| 2  | [[11d Chern-Simons theory]] |  | [[RR-fields]] in [[type II string theory]] |

In all of these higher dimensional cases the inter-geometric aspect appears. Where one assigned an [[elliptic cohomology theory]] to [[worldsheets]] equipped with polarization structure, it is only the [[arithmetic geometry]]  cases of [[supersingular elliptic curves]] which contribute; similarly in the higher dimensional cases it is the [[Artin-Mazur formal groups]] in positive [[characteristic]] which induce at the given height to the [[Calabi-Yau cohomology]].

Finding the higher analog of the [[string orientation of tmf]] for these higher dimensional cases is as desirable as it seems to be intractable without some more inter-geometric theory to guide one.
Here we will not present solutions to these rather deep questions. But we do want to discuss something that looks like steps in the right direction.

Notice that the idea of "inter-geometric theory" is ancient, it originates with the [[synthetic geometry]] of Euclid which, with the parallel axiom removed, subsumes Euclidean, elliptic and hyperbolic geometry. 

| [[synthetic geometry]]  |
|-------------------------|
| [[Euclidean geometry]]  |
| [[hyperbolic geometry]] |
| [[elliptic geometry]]   |

The idea of refining such a [[synthetic mathematics|synthetic reasoning]] to [[differential geometry]] is not as ancient, but far from new, this is known as _[[synthetic differential geometry]]_. For the kinds of applications as mentioned above we need something a bit more expressive, we consider _[[differential cohesion|differentially]] [[cohesive (infinity,1)-topos|cohesive homotopy theory]]_.

| [[differential cohesion|higher synthetic differential geometry]] |
|--------------------------------------------|
| [[higher differential geometry]]                 |
| [[higher complex analytic geometry]]       |
| [[higher arithmetic geometry]]             |



## **1)** Langlands correspondence and Weil uniformization

The central idea of the [[Langlands correspondence]] is that given a [[global field]] $K$, then $n$-dimensional [[linear representations]] of its [[Galois group]] are in correspondence with certain linear representations -- called _[[automorphic representations]]_ -- of the [[general linear group]] $GL_n(\mathbb{A}_K)$ with [[coefficients]] in the [[ring of adeles]] $\mathbb{A}_K$ of $K$ on the linear space of [[functions]] on the double [[coset space]] 

$$
  GL_n(K)\backslash GL_n(\mathbb{A}_{K})/GL_n(\mathcal{O}_K)
  \,,
$$

where $\mathbb{O}_K$ denotes the ring of [[integral adeles]]. In particular for the "absolute" case that $K = \mathbb{Q}$ is the [[rational numbers]], this is


$$
  GL_n(\mathbb{Q})\backslash GL_n(\mathbb{A}_{\mathbb{Q}})/GL_n(\mathbb{A}_{\mathbb{Z}})
$$

where 

* $\mathbb{A}_{\mathbb{Z}} = \prod_p \mathbb{Z}_p$ is the [[product]] of all rings of [[p-adic integers]];

* $\mathbb{A}_{\mathbb{Q}} = \mathbb{Q}\otimes \mathbb{A}_{\mathbb{Z}} = \prod_p^{\prime} \mathbb{Q}_{p}$ is the [[restricted product]] of all rings of [[p-adic rational numbers]].

For the case that $n = 1$ then the left part of this quotient is the _[[idele class group]]_, for higher $n$ this is an object in some nonabelian generalization of [[class field theory]].

The striking observation that leads to the conjecture of the [[geometric Langlands correspondence]] is that  under the [[function field analogy]] this double quotient, as a [[stacky quotient]], is [[analogy|analogous]] to the [[moduli stack of vector bundles]] $Bun_(\Sigma)(GL_n)$ over a [[complex curve]] $\Sigma$ in the specific presentation that is given by the [[Weil uniformization theorem]]. This says that choosing any point $x\in \Sigma$ and a [[formal disk]] $x \in D \subset \Sigma$ around it, then $(D \coprod (\Sigma-\{x\}) \to \Sigma$ is a "good enough [[cover]]", hence by [[Cech cohomology]] we have

$$
  \begin{aligned}
    Bung_X(GL_n)
      \simeq
    [X-\{x\}, GL_n] \backslash [D-\{x\}, GL_n] / [D,GL_n]
      =
    \mathbb{O}_{\Sigma}[(z-x)^{-1}]  \backslash GL_n(\mathbb{C}((z-x))) / GL_n(\mathbb{C}[ [(z-x)] ])
  \end{aligned}
 \,.
$$

This is analogous to the [[group of ideles|idelic]] structure of the [[Langlands program]] because under the [[function field analogy]] and the [[F1]]-geometry-analogy

* the [[ring of p-adic integers]]

  $$
    \mathbb{Z}_p = \{ a_0 + a_1 p + a_2 p^2 + \cdots \}
  $$

  is analogous to the [[ring of functions]] on the [[formal disk]] $D$ at $x$, namley the [[power series]] ring

  $$
    \mathbb{C}[ [ (z-x) ] ] = \{ a_0 + a_1 (z-x) + a_2 (z-x)^2 + \cdots \}
  $$

* the [[ring of p-adic numbers]]

  $$
    \mathbb{Q}_p = \{ a_{-k} p^{-k} + \cdots + a_{-1} p^{-1} + a_0 + a_1 p + a_2 p^2 + \cdots  \}
  $$

  is analogous to the [[ring of functions]] on the pointed formal disk $D - \{x\}$, namely the [[Laurent series]] ring

  $$
    \mathbb{C}((z-x)) = \{ a_{-k} (z-x)^{-k} + \cdots + a_{-1} (z-x)^{-1} + a_0 + a_1 (z-x) + a_2 (z-x)^2 + \cdots  \};
  $$ 

* the subring $\mathbb{Z}[p^{-1}] \subset \mathbb{Q}$ of [[rational numbers]] with denominator a power of $p$  is analogous to the subring or [[meromorphic functions]] on $\Sigma$ with possible poles at $x$.


Indeed, in further support of this [[analogy]] one may see that also the [[p-adic integers]] together with the [[rational functions]] form a "good enough cover" of the "[[F1]]-[[arithmetic curve]]" [[Spec(Z)]]. This is the statement of the [[arithmetic fracture square]]:

+-- {: .num_prop #ArithmeticFractureSquare}
###### Proposition

The [[integers]] $\mathbb{Z}$ are the [[fiber product]] of all the [[p-adic integers]] $\underset{p\;prime}{\prod} \mathbb{Z}_p$ with the [[rational numbers]] $\mathbb{Q}$ over the [[rationalization]] of the former, hence there is a [[pullback]] [[diagram]] in [[CRing]] of the form

$$
  \array{
     && \mathbb{Q}
     \\
     & \swarrow && \nwarrow
     \\
     \mathbb{Q}\otimes_{\mathbb{Z}}\left(\underset{p\;prime}{\prod} \mathbb{Z}_p \right) && && \mathbb{Z}
     \\
     & \nwarrow && \swarrow
     \\
     && \underset{p\;prime}{\prod} \mathbb{Z}_p
  }
  \,.
$$

Equivalently this is the [[fiber product]] of the rationals with the [[integral adeles]] $\mathbb{A}_{\mathbb{Z}}$ over the [[ring of adeles]] $\mathbb{A}_{\mathbb{Q}}$

$$
  \array{
     && \mathbb{Q}
     \\
     & \swarrow && \nwarrow
     \\
     \mathbb{A}_{\mathbb{Q}} && && \mathbb{Z}
     \\
     & \nwarrow && \swarrow
     \\
     && \mathbb{A}_{\mathbb{Z}}
  }
  \,,
$$

Since the [[ring of adeles]] is the [[rationalization]] of the integral adeles $\mathbb{A}_{\mathbb{Q}} = \mathbb{Q} \otimes_{\mathbb{Z}} \mathbb{A}_{\mathbb{Z}}$, this is also (by the discussion [here](category+of+monoids#PushoutOfCommutativeMonoids)) a [[pushout]] diagram in [[CRing]], and in fact in topological [[commutative rings]] (for $\mathbb{Q}$ with the [[discrete topology]] and $\mathbb{A}_{\mathbb{Z}}$ with its profinite/[[completion of a ring|completion]] topology).

=--

This statement immediately lifts to flat finitely generated torsion free [[modules]], involving now the rationalization and the [[completion of modules]].
This statement lifts to [[stable homotopy theory]], with [[spectra]] regarded as [[∞-modules]] over the [[sphere spectrum]] $\mathbb{S}$:

+-- {: .num_prop #SullivanArithmeticFracture}
###### Proposition
**(Sullivan arithmetic square)**

For every [[spectrum]] $X$ the canonical square

$$
  \array{
    && X_{\mathbb{Q}}
    \\
    & \swarrow && \nwarrow
    \\
    \left(
      \prod_p X_p^{\wedge}
    \right)_{\mathbb{Q}}
    &&  &&
    X
    \\
     & \nwarrow && \swarrow
    \\
    && \prod_p X_p^\wedge
  }
  \,.
$$

=--

## **2)** Axiomatic twisted differential generalized cohomology

The above [[analogy]] calls for being formalized. We need an axiomatics that allows to implement differential geometry in systematic analogy. Just as back in the old days there was established a systematic analogy

| [[synthetic geometry]]  |
|-------------------------|
| [[Euclidean geometry]]  |
| [[hyperbolic geometry]] |
| [[elliptic geometry]]   |

for modern applications we need a systematic dictionary of the form

| [[differential cohesion|higher synthetic differential geometry]] |
|--------------------------------------------|
| [[higher differential geometry]]           |
| [[higher complex analytic geometry]]       |
| [[higher arithmetic geometry]]             |


+-- {: .num_example #ComplexAnalyticDifferentialCohesion}
###### Example

Let

* $CplMfd$ be the [[site]] of [[complex analytic manifolds]] with the standard [[open cover]] topology

* $InfPt$ the site of [[infinitesimally thickened points]] with the trivial topology;

* $CplMfd_{sd}$ the site of [[formal manifold|formal]] complex analytic manifolds with the local product topology.

The evident projection and inclusion functors then form a 
[[fiber sequence]] of 1-categories

$$
  CplMfd \longleftarrow CplMfd_{sd} \longleftarrow InfPt
  \,.
$$
 
Under forming [[hypercomplete (∞,1)-topos|hypercomple]] [[(∞,1)-sheaf (∞,1)-topos]] this yields

$$
  \mathbb{C}Analytic\infty Grpd
  \longrightarrow

  \mathbb{C}Analytic\infty Grpd_{sd}
  \longrightarrow
  Inf\infty Grpd
$$

from left to right

* [[complex analytic ∞-groupoids]];

* complex analytic [[synthetic differential ∞-groupoids]]:;

* infinitesimal $\infty$-groupoids

Here the last item is essentially [[formal moduli problems]] but without the condition of $\Gamma(-) = \ast$ and without the condition of [[cohesive (∞,1)-presheaf on E-∞ rings|Lurie-infinitesimal cohesion]] (beware the terminology clash), see at [differential cohesion -- Lie theory](differential+cohesive+%28infinity%2C1%29-topos#LieTheory) for more on this.

=--



A _differentially cohesive homotopy theory_ is a geometric homotopy theory -- hence a context for [[higher geometry]]  -- $\mathbf{H}$ which is equipped with an extra structure that axiomatically encodes that the [[homotopy types]] in $\mathbf{H}$ may have [[infinitesimal object|infinitesimal extension]]. 

| $\mathbf{H}_{reduced}$ | $\hookrightarrow$ | $\mathbf{H}$ | $\longrightarrow$ |  $\mathbf{H}_{infinitesimal}$  |
|---------|---|-------------------|---|------------------|
| [[cohesion]] |  | [[differential cohesion]] |  | [[infinitesimal cohesion]] |
| [[moduli ∞-stacks]] |  | [[synthetic differential ∞-groupoids]] |  |  [[formal moduli problems]] |

$$
  \mathbf{H}_{reduced}
    \stackrel{\hookrightarrow}{\stackrel{\longleftarrow}{\stackrel{\overset{}{\hookrightarrow}}{\longleftarrow}}}
  \mathbf{H}
   \stackrel{\longrightarrow}{\stackrel{\hookleftarrow}{\stackrel{\longrightarrow}{\hookleftarrow}}}
  \mathbf{H}_{infinitesimal}
$$

The cohesive structure is reflected in the existence of a 
triple of triples of operations that naturally exist on all objects in $\mathbf{H}$:

1. [[cohesion]]

   * [[shape modality]] $\Pi$ gives [[geometric realization]]/[[classifying spaces]];

   * [[flat modality]] $\flat$ gives underlying point sets and moduli for [[flat ∞-connections]]/[[local systems]];

   * [[sharp modality]] $\sharp$ induces [[moduli stacks]] for non-flat [[∞-connections]];

1. [[infinitesimal cohesion]]

   * relative shape modality $\Pi^{rel}$ has as homotopy fibers over $X$ spaces $\Pi^{rel}_{dR}(X)$ whose function spaces are [[rationalizations]] of function spaces on $X$.

   * relative flat modality $\flat^{rel}$ creates collections of [[formal disks]];


   * relative sharp modality $\sharp^{rel}$ induces synthetic differential moduli stacks of non-flat [[∞-connections]]

1. [[differential cohesion]]

   * [[reduction modality]] $\Re$ removes infinitesimal dimensions;

   * [[infinitesimal shape modality]] $\Pi^{inf}$ produces [[de Rham spaces]], detects [[formally etale morphisms]] and induces [[etale toposes]];

   * [[infinitesimal flat modality]] $\flat^{inf}$ 


Notice that this is an axiomatics with many different geometric incarnations. For instance there is an incarnation in [[higher differential geometry]] and one in [[higher complex analytic geometry]]. The point of the axiomatics is that all statements derivable from it at "inter-geometric" in that they hold for all these geometries.

One such fact is the following: every $X$ in $\mathbf{H}$ sits in a canonical square

$$
  \array{
    && \Pi_{dR} X &&  & && rationalization\;of\;X
    \\
    & \nearrow && \searrow && &
    \\
    \flat^{rel} \Pi^{rel}_{dR}  X
    && &&
    X 
    & 
    \\
    & \searrow && \nearrow && &
    \\
    && \flat^{rel} X && & && formal\;disks\;in\;X
  }
$$

and the [[stabilization]] of this, equivalently the result of passing [[mapping spectrum|spectrum-valued functions]] on this yields

$$
  \array{
    && [\Pi_{dR} X, C] &&  & && rational\;functions
    \\
    & \swarrow && \nwarrow && &
    \\
    [\flat^{rel} \Pi^{rel}_{dR}  X, C]
    && &&
    [X,C] 
    & 
    \\
    & \nwarrow && \swarrow && &
    \\
    && [\flat^{rel} X, C] && & && C-adeles
  }
$$

which is homotopy cartesian.



(...)

We discuss how arithmetic concepts such as [[adeles]], [[ideles]], the [[idele class group]] etc. have structural analogs in any context of [[differential cohesion]]. We show that specifically in the context of [[complex analytic infinity-groupoid|complex analytic cohesion]] these reproduce the correct analogs of the arithmetic concepts as predicted by the [[function field analogy -- table|function field analogy table]].

## **2)** $E_\infty$-Arithmetic differential cohomology

+-- {: .num_prop #CompletionTorsionAdjointModalityForModuleSpectra}
###### Proposition

Let $A$ be an [[E-∞ ring]] and let $\mathfrak{a} \subset \pi_0 A$ be a [[generators and relations|finitely generated]] ideal in its underlying [[commutative ring]].

Then there is an [[adjoint triple]] of [[adjoint (∞,1)-functors]]

$$
  \array{

    \underoverset{
      A Mod_{\mathfrak{a}comp}^{op}}
    {A Mod_{\mathfrak{a}tors}^{op}}
    {\simeq}
    &\stackrel{\overset{\Pi_{\mathfrak{a}}}{\longleftarrow}}{\stackrel{\hookrightarrow}{\underset{\flat_{\mathfrak{a}}}{\longleftarrow}}}&
    A Mod^{op}
  }
$$

where

* $A Mod$ is the [[stable (∞,1)-category|stable]] [[(∞,1)-category of modules]], i.e. of [[∞-modules]] over $A$;

* $A Mod_{\mathfrak{a}tor}$ and $A Mod_{\mathfrak{a} comp}$ are the [[full sub-(∞,1)-categories]] of $\mathfrak{a}$-[[torsion approximation|torsion]] and of $\mathfrak{a}$-[[completion of a module|complete]] $A$-[[∞-modules]], respectively;

* $(-)^{op}$ denotes the [[opposite (∞,1)-category]];

* the [[equivalence of (∞,1)-categories]] on the left is induced by the restriction of $\Pi_{\mathfrak{a}}$ and $\flat_{\mathfrak{a}}$.

=--


This is effectively the content of ([[Proper Morphisms, Completions, and the Grothendieck Existence Theorem|Lurie "Completions", section 4]]):



## Stuff



+-- {: .num_defn }
###### Definition

We say that a context of _differential cohesion with compatible infinitesimals_ is a [[homotopy cofiber sequence]] of  [[cohesive (∞,1)-toposes]] 

$$
  \mathbf{H}_{red}
  \hookrightarrow
  \mathbf{H}
  \longrightarrow
  \mathbf{H}_{inf}
$$

such that 

1. the inclusion on the left exhibits [[differential cohesion]] 

1. $\mathbf{H}_{inf}$ has [[infinitesimal cohesion]] (over the [[base (∞,1)-topos]]).

=--

+-- {: .num_remark }
###### Remark



We will mostly just say "differential cohesion" for short. Given any differential cohesion $H_{red} \hookrightarrow \mathbf{H}$ then of course the homotopy cofiber $\mathbf{H}_{inf}$ of the inclusion always exists as an [[(∞,1)-topos]], but conditions under which this is itself cohesive haven't been discussed yet.

=--



This is ([[schreiber:differential cohomology in a cohesive topos|dcct, section 4.5.1.4]]).

In a context of differential cohesion there are three [[adjoint triples]] of [[modalities]] on $\mathbf{H}$, interlocking with each other. 

+-- {: .num_defn }
###### Definition

We write

*  $\Pi \dashv \flat \dashv \sharp$ for the global [[shape modality]]$\dashv$[[sharp modality]]$\dashv$[[flat modality]] of the [[cohesion]] of $\mathbf{H}$;

* $Red \dashv \Pi_{inf} \dashv \flat_{inf}$ for the [[reduction modality]]$\dashv$[[infinitesimal shape modality]]$\dashv$[[infinitesimal flat modality]] of the [[differential cohesion]] of $\mathbf{H}$;

* $\Pi_{rel} \dashv \flat_{rel} \dashv \sharp_{rel}$ for the corresponding modalities of the cohesion of $\mathbf{H}$ over $\mathbf{H}_{inf}$.

=--




The main reason why we are interested in cohesion in the present context is that every cohesive stable homotopy type is canonically decomposed into two [[fracture squares]], which we are going to relate to traditional fracture squares and to idelic structures.

+-- {: .num_prop }
###### Proposition

For $\hat E$ a cohesive [[stable homotopy type]], then it sits in an hexagonal diagram (the _[[differential cohomology hexagon]]_)

$$
  \array{
    &&  \Pi_{dR} {\hat E} && \stackrel{\mathbf{d}}{\longrightarrow} && \flat_{dR}{\hat E}
    \\
    & \nearrow & & \searrow & & \nearrow_{\mathrlap{\theta_{\hat E}}} && \searrow
    \\
    \flat \Pi_{dR} {\hat E}  && && {\hat E} && && \Pi \flat_{dR}  \hat E
    \\
    & \searrow &  & \nearrow & & \searrow && \nearrow_{\mathrlap{ch_E}}
    \\
    && \flat {\hat E} && \longrightarrow && \Pi \hat E
  }
$$

where 

1. the diagonals are [[homotopy fiber sequences]] and [[homotopy cofiber sequences]];

1. both squares are [[homotopy pullback]] and [[homotopy pushout]] squares;

1. the two boundary sequences are long [[homotopy fiber sequences]] and [[homotopy cofiber sequences]].

=--

The fracture squares allow to decompose complicated objects into their components.
It is useful to iterate this and hence to identify cohesion of slices over objects appearing in the hexagon.

+-- {: .num_lemma }
###### Lemma

Given $X \in \mathbf{H}$ such that $\flat X$ is 0-truncated, then $\mathbf{H}_{/\flat_{rel}X}$ is strongly $\infty$-connected over $(\mathbf{H}_{inf})_{/\flat_{rel}X}$.

=--

+-- {: .proof}
###### Proof

We have an essential geometric morphism given by a composite of [[adjoint
triples]]

$$
  \array{
     \mathbf{H}_{/\flat_{rel}X}
     &
       \stackrel{\overset{\Pi_{rel}}{\longrightarrow}}{\stackrel{\overset{Disc_{rel}}{\longleftarrow}}{\underset{}{\longrightarrow}}} 
     &
     (\mathbf{H}_{inf})_{/\flat_{rel} X}
       \stackrel{\overset{\Pi \simeq \Gamma}{\longrightarrow}}{\stackrel{\overset{\eta_X^\ast \circ Disc}{\longleftarrow}}{\underset{}{\longrightarrow}}} 
  }
  \infty Grpd_{/\flat X}
  \,,
$$

where the top pairs come from the formula 
([here](adjoint+infinity-functor#OnSlices)) for localization of adjunctions to slices, and the bottom one exists in each case by the [[adjoint (∞,1)-functor theorem]],
since the middle one preserves [[(∞,1)-colimits]] (since colimits in slices are computed on the dependent sums, since $Disc$ preserves colimits, and since pullbacks preserve colimits in an $\infty$-topos).  The fact that two top composite preserves the terminal object follows now by the idempotency of the various adjunctions $\Pi_{rel} \flat_{rel} X \simeq \flat_{rel}X$ and then by [[infinitesimal cohesion]] $\Pi \flat_{rel} X \simeq \flat \flat_{rel} X \simeq \flat X$. Finally using that $\flat X$ is 0-connected, hence a set it follows from $\Pi \ast \simeq \ast$ that the composite right adjoint is fully faithful over over $x\in \flat X$, hence is fully faithful on all of $\infty Grpd$.


=--
