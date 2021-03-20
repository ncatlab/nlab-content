
{:bluebox: .un_remark style="border:solid #000000;background: #E6DF13;border-width:2px 1px;padding:0 1em;margin:0 1em;"}


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--



> This page originates in notes prepared for a talk "Fractures, Ideles and the Differential Hexagon" at _[CUNY workshop on differential cohomologies](http://qcpages.qc.cuny.edu/~swilson/cunyworkshop14.html)_, New York, August 2014 ([video recording](http://videostreaming.gc.cuny.edu/videos/video/1806/))

#Contents#
* table of contents
{:toc}

+-- {: bluebox}

**Abstract** We discuss how the [[synthetic differential geometry]]-like axiomatics of _[[differential cohesion]]_ provides a theory of [[twisted cohomology|twisted]] [[generalized (Eilenberg-Steenrod) cohomology|generalized]]/[[nonabelian cohomology|nonabelian]] _[[differential cohomology]]_ which has realizations not just in [[higher differential geometry]] but also notably in [[higher complex analytic geometry]] and moreover in "[[higher arithmetic geometry]]" ([[E-∞ arithmetic geometry]]) in a way that systematizes some of the [[analogies]] which motivate the [[geometric Langlands correspondence]].

=--

## Motivation

A fruitful approach to mathematical theory is what might be called "inter-geometric", meaning that definitions and theorems make sense and hold when interpreted in different flavors of geometry. Classical examples are the [[GAGA principle]], the [[function field analogy]], the [[geometric Langlands correspondence|geometric]] [[Langlands correspondence]], more recent are various approaches to [[F1]]-geometry and [[global analytic geometry]]. While in these examples the [[analogy]]  between different theories of geometry has been established case-by-case, there is by and large no meta-theory which would systematically imply the analogy. 

This is of practical concern for instance in the [[Langlands program]], where it is an open problem how the methods and insights which are deeply on the side of [[complex analytic geometry]], such as involving [[mirror symmetry]], might have incarnations on the [[arithmetic geometry]]-side. And vice-versa, the complex-analytic version of the conjecture was obtained by educated guessing via analogy from the arithmetic side in the first place, but this guesswork has been questioned ([[Problems in the theory of automorphic forms -- 45 years later|Langlands 14]]). Both of these issues would be resolved if one had an "inter-geometric" theory from which the correspondence both in [[arithmetic geometry]] and in [[complex-analytic geometry]] would both follow systematically.

More generally, inter-geometric theory is relevant in [[higher geometric quantization]], where choices of [[polarizations]] correspond to descending to more rigid geometries (for introduction and review see [Schreiber 14](#Schreiber14)).

A noteworthy example in this context is the construction of the refined [[Witten genus]] in the guise of the [[string orientation of tmf]]: here what is initially a concept in [[complex analytic geometry|complex analytic]] ([[supergeometry|super]]-)geometry is constructed by passage (via the construction of [[tmf]]) to the [[moduli stack of elliptic curves]] all the way down in [[arithmetic geometry]], and in fact then via the [[fracture theorems]] by its [[base change|base changes]] to [[p-adic geometry]] and to [[rational homotopy theory]] (and further to [[K(n)-local stable homotopy theory]]). In fact, the [[supersingular elliptic curves]] which are the ones that contribute at [[height of a formal group law|height]] 2 and hence make for the genuinely stringy ([[chromatic filtration|second chromatic level]]) contribution to the [[topological modular forms|refined]] [[Witten genus]] exist only in [[positive characteristic]], invisible to complex geometry. There is thus a kind of [[p-adic string theory]] (closed string theory!) appearing here, which is however not of the kind that existing literature with such title would shed any light on.f

The role of more "[[rigid analytic geometry|rigid]]" [[arithmetic geometry]] -- closer to the bottom [[Borger's absolute geometry|absolute geometry]] -- in [[quantization]] might be summarized in parts by the following table:

**[[quantization of 3d Chern-Simons theory]] and [[holographic principle|holographically]] of the [[WZW-model]]/the [[string]] **

| [[geometry]] |  [[worldvolume]]  |  moduli of [[field (physics)|fields]] | moduli of [[polarizations]]  |  [[geometric quantization]]/[[theta functions]] |
|------|----------|------------|---------|----|
| [[differential geometry]] |  [[worldsheet]] | [[moduli stack of flat connections]] |   |  |
| [[complex analytic geometry]] | [[complex curve]]  |  [[Jacobian]]/moduli of [[stable vector bundle|(semi-)stable bundles]]  |  [[moduli stack of Riemann surfaces]] |  [[modular functor]], [[Witten genus]], ...  |
| [[arithmetic geometry]] |  [[arithmetic curve]]   | [[Galois representations]]  and [[automorphic forms]] (via [[Langlands correspondence]]) (in particular [[Tamagawa measures]], etc.) | [[moduli stack of curves]] |  [[equivariant elliptic cohomology]], [[string orientation of tmf]], ...  |

The construction of the bottom right items here is a ground-breaking accomplishment in [[algebraic topology]], but at least in view of the origin of the WZW-string and the [[Witten genus]] in [[string theory]] it maybe raises more questions than it solves: from the perspective of physics these are but the first example of a tower of higher dimensional [[brane]] phenomena, the next instance being the [[partition function]] of the [[M5-brane]] and then that of 10d [[string theory]] itself (see e.g. at _[[self-dual higher gauge theory]]_).  

| $k$ | $(4k+3)d$ [[higher dimensional Chern-Simons theory]] | form [[theta characteristics]] $\to$ | $(4k+2)d$ [[self-dual higher gauge theory]] |
|----|--------------|-----------|------------------|
| 0  | [[3d Chern-Simons theory]] |   |  [[WZW-model|chiral WZW-string]]/[[modular functor]]/[[equivariant elliptic cohomology]] |
| 1  | [[7d Chern-Simons theory]] |  |  self-2-2form on [[M5-brane]] |
| 2  | [[11d Chern-Simons theory]] |  | [[RR-fields]] in [[type II string theory]] |

In all of these higher dimensional cases the inter-geometric aspect appears. Where one assigned an [[elliptic cohomology theory]] to [[worldsheets]] equipped with polarization structure, it is only the [[arithmetic geometry]]  cases of [[supersingular elliptic curves]] which contribute; similarly in the higher dimensional cases it is the [[Artin-Mazur formal groups]] in positive [[characteristic]] which induce at the given height to the [[Calabi-Yau cohomology]].
Finding the higher analog of the [[string orientation of tmf]] for these higher dimensional cases is as desirable as it seems to be intractable without some more inter-geometric theory to guide one.

Here we will not present solutions to these rather deep questions. But we do want to discuss something that looks like steps in the right direction.

Notice that the idea of "inter-geometric theory" is ancient, it originates with the [[synthetic geometry]] of Euclid which, with the parallel axiom removed, subsumes Euclidean, elliptic and hyperbolic geometry:

| [[synthetic geometry]]  |
|-------------------------|
| [[Euclidean geometry]]  |
| [[hyperbolic geometry]] |
| [[elliptic geometry]]   |

The idea of refining such a [[synthetic mathematics|synthetic reasoning]] to [[differential geometry]] is not as ancient, but far from new, this is known as _[[synthetic differential geometry]]_. For the kinds of applications as mentioned above we need something a bit more expressive, we consider _[[differential cohesion|differentially]] [[cohesive (infinity,1)-topos|cohesive homotopy theory]]_:

| [[differential cohesion|higher synthetic differential geometry]] |
|--------------------------------------------|
| [[higher differential geometry]]                 |
| [[higher complex analytic geometry]]       |
| [[E-∞ arithmetic geometry|higher arithmetic geometry]]             |

This we review and discuss [below](#AxiomaticDifferentialCohomology). First we recall now the key motivating ingredients of the [[function field analogy]] and the [[Langlands correspondence]].


## **1)** Langlands correspondence and Weil uniformization
 {#LanglandsAndWeil}

The central idea of the [[Langlands correspondence]] (see for instance ([Frenkel 05](#Frenkel05)) for a review of the basic aspects that we refer to) is that given a [[global field]] $K$, then $n$-dimensional [[linear representations]] of its [[Galois group]] are in correspondence with certain linear representations -- called _[[automorphic representations]]_ -- of the [[general linear group]] $GL_n(\mathbb{A}_K)$ with [[coefficients]] in the [[ring of adeles]] $\mathbb{A}_K$ of $K$ on the linear space of [[functions]] on the [[double coset space]] 

$$
  GL_n(K) \;\backslash\; GL_n(\mathbb{A}_{K}) \;/\; GL_n(\mathbb{O}_K)
  \,,
$$

where $\mathbb{O}_K$ denotes the ring of [[integral adeles]]. In particular for the "absolute" case that $K = \mathbb{Q}$ is the [[rational numbers]], this is


$$
  GL_n(\mathbb{Q})
   \;\backslash\;
   GL_n(\mathbb{A}_{\mathbb{Q}})
    \;/\;
  GL_n(\mathbb{A}_{\mathbb{Z}})
$$

where 

* $\mathbb{A}_{\mathbb{Z}} = \prod_p \mathbb{Z}_p$ is the [[product]] of all rings of [[p-adic integers]] -- the _[[ring of integral adeles]]_ (finite integral adeles);

* $\mathbb{A}_{\mathbb{Q}} = \mathbb{Q}\otimes \mathbb{A}_{\mathbb{Z}} = \prod_p^{\prime} \mathbb{Q}_{p}$ is the [[restricted product]] of all rings of [[p-adic rational numbers]] -- the _[[ring of adeles]]_ ([[ring of finite adeles]]).

For the case that $n = 1$ then the left part of this quotient is the _[[idele class group]]_, for higher $n$ this is an object in some nonabelian generalization of [[class field theory]].

The striking observation that leads to the conjecture of the [[geometric Langlands correspondence]] is that  under the [[function field analogy]] this double quotient, as a [[stacky quotient]], is [[analogy|analogous]] to the [[moduli stack of vector bundles]] $Bun_{\Sigma}(GL_n)$ over a [[complex curve]] $\Sigma$ in the specific presentation that is given by the [[Weil uniformization theorem]]. Namely, this says that choosing any point $x\in \Sigma$ and a [[formal disk]] $x \in D \subset \Sigma$ around it, then the formal disk $D$ around $x$ together with the complement $\Sigma-\{x\}$ of the point

$$
  \array{
     && \Sigma-\{x\}
     \\
     &  && \searrow
     \\
     && && \Sigma
     \\
     & && \nearrow
     \\
     && D
  }
$$

is a "good enough [[cover]]", hence by [[Cech cohomology]] we have

$$
  \begin{aligned}
    Bun_\Sigma(GL_n)
      & \simeq
    [\Sigma-\{x\}, GL_n] \;\backslash \;[D-\{x\}, GL_n] \;/\; [D,GL_n]
      \\
       & =
    \mathbb{O}_{\Sigma}[(z-x)^{-1}]  \;\backslash\; GL_n(\mathbb{C}((z-x))) \;/\; GL_n(\mathbb{C}[ [(z-x)] ])
  \end{aligned}
 \,,
$$

expressing the [[groupoid]] ([[stack]]) of $GL_n$-[[principal bundles]] on $\Sigma$ as the groupoid of $GL_n$-valued transitions functions on the space of double intersections of the cover, which is $D-\{x\}$, subject to [[gauge transformations]] given by $GL_n$-valued functions on the cover itself, hence on $\Sigma-\{x\}$ and on $D$. But ([[holomorphic functions|holomorphic]]) 

* functions on the formal disk $D$ at $x$ are, essentially by definition, [[formal power series]] in $(z-x)$;

* functions on the punctured formal disk $D -\{x\}$ are formal power series which need not converge at the missing point, hence are [[Laurent series]] in $(z-x)$;

* functions on the complement $\Sigma-\{x\}$ are, similarly, [[meromorphic functions]] on $\Sigma$ with poles allowed at $x$.

The expression for $Bun_\Sigma(GL_n)$ obtained this way in the second line above is [[analogy|analogous]] to the [[group of ideles|idelic]] space appearing the [[Langlands program]]. This analogy proceeds via the [[function field analogy]] and the [[F1]]-geometry-analogy, which say that:

* the [[ring of p-adic integers]]

  $$
    \mathbb{Z}_p = \{ a_0 + a_1 p + a_2 p^2 + \cdots \}
  $$

  is analogous to the [[ring of functions]] on the [[formal disk]] $D$ at $x$, namely the [[power series]] ring

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

* the subring $\mathbb{Z}[p^{-1}] \subset \mathbb{Q}$ of [[rational numbers]] with denominator a power of $p$  is analogous to the subring of [[meromorphic functions]] on $\Sigma$ with possible poles at $x$.

Notice that the [[cover]] of the [[complex curve]] $\Sigma$ involved in the [[Weil uniformization theorem]] is exhibited by the following [[fiber product]] diagram

$$
  \array{
     && \Sigma-\{x\}
     \\
     &  \nearrow && \searrow
     \\
     D-\{x\} && && \Sigma
     \\
     & \searrow && \nearrow
     \\
     && D
  }
$$


Indeed, in further support of this [[analogy]] one may see that also the [[p-adic integers]] together with the [[rational functions]] form a "good enough cover" of the "[[F1]]-[[arithmetic curve]]" [[Spec(Z)]] of this form. This is the statement of the [[arithmetic fracture square]]:

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



The statement of prop. \ref{ArithmeticFractureSquare} immediately lifts to flat finitely generated torsion free [[modules]], involving now the rationalization and the [[completion of modules]].
It then naturally lifts futher to [[stable homotopy theory]], now with [[spectra]] regarded as [[∞-modules]] over the [[sphere spectrum]] $\mathbb{S}$:


+-- {: .num_prop #SullivanArithmeticFracture}
###### Proposition
**(Sullivan [[arithmetic fracture square]])**

For every [[spectrum]] $X$ the canonical square diagram

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
$$

formed by [[p-completion]] and [[rationalization]] of spectra is a [[homotopy pullback]] square (hence a [[homotopy pushout]] square).

=--

Moreover, the [[geometric Langlands correspondence]] eventually relates the [[moduli stack of bundles]]  $Bun_{\Sigma}(G)$ realized via [[Weil uniformization]] with respect to such "fracture cover" to a [[moduli stack of local systems]] ([[flat connections]]) by identifying [[quasicoherent sheaves]] on one side with [[D-modules]] on the other

"$ \mathcal{O}Mod(Loc_{\Sigma}({{}^L G}))
    \stackrel{\simeq}{\longrightarrow}
  \mathcal{D} Mod( Bun_{\Sigma}(G)) $"

Hence in order to systematize the implementation of such consideration in various flavors of [[geometry]], we need an "inter-geometric" axiomatics that incorporates these ingredients, notably

1. [[differential cohomology]];

1. [[D-geometry]].

Such an axiomatics we turn to now, recalling how it has implementations in [[higher differential geometry]] and [[higher complex analytic geometry]]. Then at the end [below](#ArithmeticCohesion) we discuss how the axioms also have implementation in a [[E-∞ arithmetic geometry]], where moreover they reproduce precisely the classical number-theoretic [[fracture squares]] and hence an "automorphic" incarnation of all [[moduli ∞-stacks]] of [[higher gauge fields]].


## **2)** Axiomatic twisted differential generalized cohomology
 {#AxiomaticDifferentialCohomology}

The [above](LanglandsAndWeil) [[analogy]] calls for being formalized. We need an axiomatics that allows to implement differential geometry in systematic analogy. Just as back in the old days there was established a systematic analogy

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
| [[E-∞ arithmetic geometry|higher arithmetic geometry]]             |


We will discuss here how this may be done via the axiomatics called _[[cohesive homotopy theory]]_ and _[[differential cohesion]]_ in ([Schreiber 13](#Schreiber13)).

### Differential generalized cohomology

To that end, first consider the following flavors of geometry.

+-- {: .num_example #TheSites}
###### Example


Let $S$ denote either of the following [[sites]]:

* $SmoothMfd$ [[smooth manifolds]];

* $ComplexAnalyticMfd$ [[complex analytic manifolds]];

* $SuperMfd$ [[supermanifolds]];

* $FormalSmoothhMfd$, $FormalComplexAnalyticMfd$, $FormalSuperMfd$ [[formal manifolds]];

* any [[site]] such that 

  1. it has [[finite products]];

  1. every object is locally of [[contractible space|contractible]] [[etale homotopy type]];

  1. $Hom(\ast, -)$ preserves [[split hypercovers]].

Write

$$
  \mathbf{H} \coloneqq Sh_\infty(S) \simeq L_{lwhe} sPSh(S)
$$

for the [[homotopy theory]] obtained from the [[category]] of [[simplicial presheaves]] on $S$ by universally turning local (stalkwise) [[weak homotopy equivalences]] into actual [[homotopy equivalences]] (i.e. the [[hypercomplete (∞,1)-topos|hypercomplete]] [[(∞,1)-category of (∞,1)-sheaves]] over this site.

Write specifically

* $Smooth \infty Grpd\coloneqq Sh_\infty(SmoothMfd)$ -- [[smooth ∞-groupoids]];

* $ComplexAnalytic \infty Grpd\coloneqq Sh_\infty(ComplexAnalyticMfd)$ -- [[complex analytic ∞-groupoids]];

* $SmoothSuper \infty Grpd\coloneqq Sh_\infty(SmoothSuperMfd)$ -- [[smooth super ∞-groupoids]];

* $FormalSmooth\infty Grpd \coloneqq Sh_\infty(FormalSmoothMfd)$ -- [[synthetic differential ∞-groupoid|formal smooth ∞-groupoids]].

=--

+-- {: .num_prop #TheHomotopyTheoriesAreCohesive}
###### Proposition

The [[homotopy theories]] $\mathbf{H}$ from example \ref{TheSites} have the property that there is an [[adjoint quadruple]] of [[derived functors]] ([[(∞,1)-functors]])

$$
  \mathbf{H} \stackrel{\longrightarrow}{\stackrel{\hookleftarrow}{\stackrel{\longrightarrow}{\hookleftarrow}}}
  \infty Grpd \simeq L_{whe} Top
$$

such that the top [[left adjoint]] preserves [[finite products]] and the bottom [[right adjoint]] is a [[full and faithful (∞,1)-functor|fully faithful embedding]].


By going back and forth this induces an [[adjoint triple]] of [[idempotent (∞,1)-monads|(∞,1)-comonads]] on $\mathbf{H}$ which we write

$$
  (\Pi \dashv \flat \dashv \sharp) \colon \mathbf{H} \to \mathbf{H}
$$


and call, respectively: _[[shape modality]]_ $\dashv$ _[[flat modality]]_ $\dashv$ _[[sharp modality]]_.


=--

Following 1-categorical terminology proposed by [[William Lawvere]] (see at _[[cohesive topos]]_) we say:



+-- {: .num_defn}
###### Definition

[[homotopy theory|Homotopy theories]] with the properties as in prop. \ref{TheHomotopyTheoriesAreCohesive} we call _[[cohesive homotopy theories]]_ ([[cohesive (∞,1)-toposes]]).

=--


It is commonplace that a single [[idempotent (∞,1)-monad]] such as $\Pi$ is equivalently a [[localization of an (∞,1)-category|localization]] of a homotopy theory, and that a sincle idempotent co-monad such as $\flat$ is equivalently a co-localization.

Lawvere argued since the 1990s (see [here](cohesive%20topos#References)) is that the presence of [[adjoint pairs]] and more so of [[adjoint triples]] of these on a category -- "[[adjoint modalities]]" -- is a remarkably expressive structure for axiomatizing [[synthetic differential geometry]]. What ([Schreiber 13](#Schreiber13)) observes is that in [[homotopy theory]] this is considerably more so the case:

+-- {: .num_prop #Structures}
###### Claim

* the [[shape modality]] $\Pi$ is naturally thought of as sending each [[geometric homotopy type]] $X \in \mathbf{H}$ to its **[[fundamental ∞-groupoid]]** $\Pi X$ of geometric paths inside it, equivalently to its **[[geometric realization]]**;


* the [[flat modality]] $\flat$ is naturally thought of as sending each [[moduli ∞-stack]] $\mathbf{B}G$ of $G$-[[principal ∞-bundles]] to the [[moduli ∞-stack]] $\flat\mathbf{B}G$ of **$G$-[[flat ∞-connections|principal flat ∞-connections]]**;


* the [[homotopy fiber]] $\flat_{\mathrm{dR}}G$ of the [[counit of a comonad|counit]] $\flat \mathbf{B}G \to \mathbf{B}G$ is naturally thought of as sending the moduli $\infty$-stack of **$\mathfrak{g}$-[[L-∞ algebra valued differential forms]]**;

* the canonical map $\theta \colon G \longrightarrow \flat_{dR} G$ is naturally thought of as the **$G$-[[Maurer-Cartan form]]**;


* for [[braided ∞-groups]] $G$ the various [[homotopy fibers]] of $\theta \colon G \longrightarrow \flat_{dR} G$ are moduli $\infty$-stacks $\mathbf{B}G_{conn}$ of non-flat **$G$-[[principal ∞-connections]]**;

* the [[sharp modality]] $\sharp$ serves to produce various more suble **[[moduli ∞-stacks]]**, for instance:

  * given a [[Hodge filtration]] on $\flat_{dR} G$ then $BunConn_\Sigma(G)$ -- the **moduli $\infty$-stack  of all [[principal ∞-connections]]** on a given base space $\Sigma$ -- is obtained by "[[differential concretification]]" (see [[schreiber:Differential cohomology is Cohesive homotopy theory|Schreiber 14]] for more);

  * for $Type_{\mathbf{H}}$ the [[object classifier]] of $\mathbf{H}$, then for any bare [[homotopy type]] $\Sigma \in \infty Grpd \hookrightarrow \mathbf{H}$ the [[homotopy pullback]] $\mathcal{M}_{\Sigma}$ in 

    $$
      \array{
        \mathcal{M}_{\Sigma} &\longrightarrow& &\longrightarrow& \ast
        \\
        \downarrow && && \downarrow^{\mathrlap{\dashv \Sigma}}
        \\
        Type_{\mathbf{H}} &\stackrel{}{\to}& \sharp Type_{\mathbf{H}} & \stackrel{\Pi}{\longrightarrow} & \sharp Type_{\mathbf{H}}
      }
    $$

    For instance for $\mathbf{H} = ComplexAnalytic\infty Gprd$ then this is a **[[moduli stack of complex structures]]** on $\Sigma$.
    

=--

This is quite a bit of structure, concisely axiomatized by the presence of the [[adjoint modalities]] $\Pi \dashv \flat \dashv \sharp$. And more is implied:

+-- {: .num_prop }

###### Proposition

For any [[cohesive (∞,1)-topos]] $\mathbf{H}$ over [[∞Grpd]], then its _Goodwillie tangent space_, the [[tangent (∞,1)-category]] $T \mathbf{H}$ of [[parametrized spectrum|parameterized spectrum objects]] in $\mathbf{H}$ is itself a cohesive $(\infty,1)$-topos over bare [[parameterized spectra]] $T \infty Grpd$ -- the _[[tangent cohesive (∞,1)-topos]]_:

$$
  T \mathbf{H}
   \stackrel{\longrightarrow}{\stackrel{\hookleftarrow}{\stackrel{\longrightarrow}{\hookleftarrow}}}  
  T \infty Grpd

  \,.

$$

=--

This is an extension of $\mathbf{H}$ by [[stable homotopy theory]]


$$
  \array{
    Spectra(\mathbf{H}) &\hookrightarrow& T \mathbf{H}
    \\
    && \downarrow 
    \\
    && \mathbf{H}
  }
  \,.
$$

In ([Bunke-Nikolaus-V&#246;lkl 13](#BunkeNikolausVoelkl13)) it was observed that:

+-- {: .num_prop  #HexagonExactness}
###### Proposition

For $\hat E \in Spectra(\mathbf{H}) \hookrightarrow T \mathbf{H}$ a [[stable homotopy type|stable]] [[cohesive homotopy type]], then the canonical [[diagram]] formed from the [[unit of a monad|unit]] of the [[shape modality]] $\Pi$ and the [[counit]] of the [[flat modality]] $\flat$

$$
  \array{
    &&  \Pi_{dR} {\hat E} && \stackrel{\mathbf{d}}{\longrightarrow} && \flat_{dR}{\hat E}
    \\
    & \nearrow & & \searrow & & \nearrow_{\mathrlap{\theta_{\hat E}}} && \searrow
    \\
    \Pi_{dR} \flat  {\hat E}  && && {\hat E} && && \Pi \flat_{dR}  \hat E
    \\
    & \searrow &  & \nearrow & & \searrow && \nearrow_{\mathrlap{ch_E}}
    \\
    && \flat {\hat E} && \longrightarrow && \Pi \hat E
  }
$$

is homotopy exact in that

1. both squares are [[homotopy pullback]] (and hence [[homotopy pushout]]) squares;

1. the diagonals are [[homotopy fiber sequences]] (and hence [[homotopy cofiber sequences]]);

1. also the long top and bottom sequences are [[homotopy fiber sequences]] (and hence [[homotopy cofiber sequences]]).

=--

+-- {: .num_remark }
###### Remark

In view of claim \ref{Structures} the [[differential cohomology hexagon]] of prop. \ref{HexagonExactness} has the following interpretation:

$$
  \array{
    &&  connection\;forms\;on\;trivial\;bundles && \stackrel{de\;Rham\;differential}{\longrightarrow} && curvature\;forms
    \\
    & \nearrow & & \searrow & & \nearrow_{\mathrlap{curvature}} && \searrow^{\mathrlap{de\;Rham\;theorem}}
    \\
    flat\;differential\;forms  && && geometric\;bundles\;with \;connection && && rationalized\;bundle
    \\
    & \searrow &  & \nearrow & & \searrow^{\mathrlap{topol.\;class}} && \nearrow_{\mathrlap{Chern\;character}}
    \\
    && geometric\;bundles\;with\;flat\;connection && \underset{comparison}{\longrightarrow} && shape\;of\;bundle
  }
$$

In particular, when applied to sheaves of spectra of the form considered in ([Bunke-Gepner 13](#BunkeGepner13)), which effectively embody the construction of [[generalized (Eilenberg-Steenrod) cohomology|generalized]] [[differential cohomology]] that was proposed in ([[Quadratic Functions in Geometry, Topology, and M-Theory|Hopkins-Singer 02]]), then the right part of the hexagon reproduces their defining decomposition as [[homotopy pullbacks]] of [[L-∞ algebra valued differential form]] along the [[Chern character]] map $E \to E \wedge H \mathbb{R}$ of plain  [[spectra]] $E$ (see at _[differential cohomology diagram -- Hopkins-Singer coefficients](differential+cohomology+diagram#HopkinsSingerCoefficients)_).

In view of this it is natural to ask if there are more general sheaves of spectra than those proposed in ([[Quadratic Functions in Geometry, Topology, and M-Theory|Hopkins-Singer 02]], [Bunke-Gepner 13](#BunkeGepner13)) which could still be sensibly regarded as encoding a kind of [[differential cohomology]]. Proposition \ref{HexagonExactness} in view of claim \ref{Structures} answers this in the most encompassing way: _every_ sheaf of spectra on smooth manifolds, and in fact more generally every [[stable homotopy type|stable]] [[cohesive homotopy type]] is meaningfully regarded as a [[generalized (Eilenberg-Steenrod) cohomology|generalized]] [[differential cohomology]] theory, in that the axiomatics of [[cohesion]] provides a detailed decomposition of any such into data which behaves just right.

It may therefore be useful to regard prop. \ref{HexagonExactness} as the differential refinement of the [[Brown representability theorem]]:

| [[Brown representability theorem]] | $\;\;\;$ proposition \ref{HexagonExactness} |
|------------------------------------|-------------------------------------|
| [[cohomology theory]] = [[spectrum]] | [[differential cohomology|differential cohomology theory]] = [[cohesive homotopy type|cohesive]] spectrum |  

=--

### Twisted differential generalized cohomology

More is true, also [[twisted cohomology]] is naturally encoded by the axiomatics of [[cohesive homotopy theory]], as we pass from the fiber $Spectra(\mathbf{H})$ of the [[tangent cohesive (∞,1)-topos]] $T\mathbf{H}$ over the point to general cohesive [[parameterized spectrum]] objects:

+-- {: .num_prop }
###### Proposition

For $\hat E \in Spectra(\mathbf{H}) \hookrightarrow T\mathbf{H}$ a spectrum object, the canonical [[∞-action]] of its [[automorphism ∞-group]] is exhibited by the universal $\hat E$-[[fiber ∞-bundle]]

$$
  \left[
   \array{
    \hat E &\to& \hat E//Aut(\hat E)
    \\
    && \downarrow
    \\
    && \mathbf{B}Aut(\hat E)
   }
  \right]
  \in 
   T \mathbf{H}
  \,.
$$

=--

[NSS 12](#NSS12)

+-- {: .num_prop }
###### Proposition

For any unstable [[cohesive homotopy type]] $X \in \mathbf{H} \hookrightarrow T \mathbf{H}$ the [[mapping stack]]

$$
  [X,\hat E//Aut(\hat E)]
  \in 
  T \mathbf{H}
$$

is the [[parameterized spectrum|bundle of spectra]] which over a twist 
$\tau \colon X \to Pic(\hat E)$ is the $\tau$-twisted $\hat E$-cohomology of $X$.

=--


See [here](tangent+cohesion#Cohomology) for details and further discussion.

So [[cohesion]] faithfully axiomatizes "inter-geometric" twisted differential generalized cohomology. 
In order to find also an "inter-geometric" [[Weil uniformization theorem]] for this we need however to add another axiom, one that makes [[infinitesimal objects]] such as [[formal disks]] appear explicitly. 


### Weil uniformization for twisted differential generalized cohomology
 {#WeilUniformizationForTwistedDifferentialCohomology}

To that end, consider again first an example

+-- {: .num_example #ComplexAnalyticDifferentialCohesion}
###### Example

Let $S_{reduced} \longleftarrow S \longleftarrow S_{infinitesimal}$ be one of the following fiber sequence of [[sites]]

* $SmoothMfd \longleftarrow FormalSmoothMfd \hookleftarrow FormalPts$ 

* $ComplexAnalyticMfd \longleftarrow FormalComplexAnalyticMfd \hookleftarrow FormalPts$ 

where $FormalPts$ is the site of [[infinitesimally thickened points]] with the trivial topology;
 
Under forming [[hypercomplete (∞,1)-topos|hypercomplete]] [[(∞,1)-sheaf (∞,1)-topos]] this yields

$$ 
  \array{
    \mathbf{H}_{reduced} &\hookrightarrow& \mathbf{H}
    &\longrightarrow& \mathbf{H}_{infinitesimal}
    \\
    ComplexAnalytic\infty Grpd 
    & \longrightarrow & FormalComplexAnalytic\infty Grpds 
    & \longrightarrow & 
    Infinitesimal\infty Grpd 
  }
$$

Here the last item is essentially [[formal moduli problems]] but without the condition of $\Gamma(-) = \ast$ and without the condition of [[cohesive (∞,1)-presheaf on E-∞ rings|Lurie-infinitesimal cohesion]] (beware the terminology clash), see at [differential cohesion -- Lie theory](differential+cohesive+%28infinity%2C1%29-topos#LieTheory) for more on this.


=--

+-- {: .num_prop #TheDifferentialCohesion}
###### Proposition

In example \ref{ComplexAnalyticDifferentialCohesion} we have

$$
  \mathbf{H}_{reduced}
    \stackrel{\hookrightarrow}{\stackrel{\longleftarrow}{\stackrel{\overset{}{\hookrightarrow}}{\longleftarrow}}}
  \mathbf{H}
   \stackrel{\longrightarrow}{\stackrel{\hookleftarrow}{\stackrel{\longrightarrow}{\hookleftarrow}}}
  \mathbf{H}_{infinitesimal}
$$

By going back and forth, the [[adjoint quadruple]] on the left induces a further [[adjoint triple]] of [[adjoint modalities]] which we write

$$
  (\Re \dashv \Im \dashv \&)

  \colon 
  \mathbf{H} \to \mathbf{H}
$$

which we call _[[reduction modality]]_ $\dashv$ _[[infinitesimal shape modality]]_ $\dashv$ _[[infinitesimal flat modality]]_ .

Moreover, $\mathbf{H}_{infinitesimal}$ satisfies _[[infinitesimal cohesion]]_ in that for all objects in here the [[points-to-pieces transform]] $\flat \to \Pi$ is an [[equivalence]].

=--


| $\mathbf{H}_{reduced}$ | $\hookrightarrow$ | $\mathbf{H}$ | $\longrightarrow$ |  $\mathbf{H}_{infinitesimal}$  |
|---------|---|-------------------|---|------------------|
| [[cohesion]] |  | [[differential cohesion]] |  | [[infinitesimal cohesion]] |
| [[moduli ∞-stacks]] |  | [[formal smooth ∞-groupoids]] |  |  [[formal moduli problems]] |

+-- {: .num_prop #PiInf}
###### Claim

The [[infinitesimal shape modality]] $\Im$ is naturally thought of as producing [[de Rham space]] objects. In particular: 

1. for $G \in Grp(\mathbf{H})$ an [[∞-group]] object then the [[mapping stack]]

   $$
     Loc_\Sigma(G) \coloneqq [\Im \Sigma, \mathbf{B}G]
   $$

   is the [[moduli ∞-stack]] of $G$-[[local systems]] on any $\Sigma \in \mathbf{H}$;

1. [[quasicoherent sheaves]] on $\Im X$ are [[D-modules]] on $X$.

=--


+-- {: .num_remark}
###### Remark

In terms of claim \ref{PiInf} then the statement of the [[geometric Langlands correspondence]] is that there is a natural [[correspondence]] between
$\Im[\Sigma, \mathbf{B}G]$ and $[\Im\Sigma, \mathbf{B}{}^L G]$.


=--

+-- {: .num_defn #relativecohesionmodalities}
###### Definition

Since by prop. \ref{TheDifferentialCohesion} $\mathbf{H}$ is cohesive also over $\mathbf{H}_{infinitesimal}$, this gives _relative_ modalities


$$
  (\Pi^{rel} \dashv \flat^{rel} \dashv \sharp^{rel})
  \;\colon\;
  \mathbf{H} \to \mathbf{H}_{infinitesimal} \to \mathbf{H}
$$

which we call the _[[relative shape modality]]_, _[[relative flat modality]]_ and _[[relative sharp modality]]_, respectively.

=--

See ([Schreiber 13, 3.10.10](#Schreiber13)).

+-- {: .num_prop }
###### Proposition

For $\Sigma\in ComplexAnalyticMfd \hookrightarrow ComplexAnalytic\infty Grpd$ then the relative flat modality, def. \ref{relativecohesionmodalities}, is given by forming the [[disjoint union]] 

$$
  \flat^{rel} \Sigma \simeq \underset{x \in \Sigma}{\coprod} D_{x}
$$

of all [[formal disks]] $D_x \hookrightarrow \Sigma$ around points $x \in \Sigma$.

=--

See ([Schreiber 13, 5.6.1.4](#Schreiber13)).


+-- {: .num_remark }
###### Remark


In summary, the [[differential cohesion|differential cohesive]] structure is reflected in the existence of a  triple of triples of operations that naturally exist on all objects in $\mathbf{H}$:

1. [[cohesion]]

   * [[shape modality]] $\Pi$ gives [[geometric realization]]/[[classifying spaces]];

   * [[flat modality]] $\flat$ gives underlying point sets and moduli for [[flat ∞-connections]]/[[local systems]];


   * [[sharp modality]] $\sharp$ induces [[moduli stacks]] for non-flat [[∞-connections]] (via [[differential concretification]] of the naive mapping stacks);

1. [[infinitesimal cohesion]]

   * relative shape modality $\Pi^{rel}$ has as homotopy fibers over $X$ spaces $\Pi^{rel}_{dR}(X)$ whose function spaces are [[rationalizations]] of function spaces on $X$.

   * relative flat modality $\flat^{rel}$ creates collections of [[formal disks]];


   * relative sharp modality $\sharp^{rel}$ induces synthetic differential moduli stacks of non-flat [[∞-connections]]

1. relative [[differential cohesion]]

   * [[reduction modality]] $\Re$ removes infinitesimal dimensions;

   * [[infinitesimal shape modality]] $\Im$ produces [[de Rham spaces]], detects [[formally etale morphisms]] and induces [[etale toposes]];

   * [[infinitesimal flat modality]] $\&$ 

=--

+-- {: .num_example #WeilUniformizationFromTheRelativeDifferentialHexagon}
###### Example


Every $X$ in $\mathbf{H}$ sits in a canonical square

$$
  \array{
    && \Pi^{rel}_{dR} X &&  & && rationalization\;of\;X
    \\
    & \nearrow && \searrow && &
    \\
    \Pi^{rel}_{dR} \flat^{rel}  X
    && &&
    X 
    & 
    \\
    & \searrow && \nearrow && &
    \\
    && \flat^{rel} X && & && formal\;disks\;in\;X
  }
$$

and the [[stabilization]] of this, equivalently the result of passing to $\hat E$-[[mapping spectrum|spectrum-valued functions]] on this yields

$$
  \array{
    && [\Pi^{rel}_{dR} X, \hat E] &&  & && rational\;\hat E-functions
    \\
    & \swarrow && \nwarrow && &
    \\
    [\Pi^{rel}_{dR}\flat^{rel}   X, \hat E]
    && &&
    [X,\hat E] 
    & 
    \\
    & \nwarrow && \swarrow && &
    \\
    && [\flat^{rel} X, \hat E] && & && \hat E-adeles
  }
$$

which is homotopy cartesian.

=--



## **3)** $E_\infty$-Arithmetic differential cohomology
 {#ArithmeticCohesion}

Above we found general synthetic axioms for differential cohomology and realization of these axioms in [[higher differential geometry]] and [[higher complex analytic geometry]]. Both turned out to exhibit also _relative_ [[differential cohesion]], def. \ref{relativecohesionmodalities}, over "[[formal moduli problems]]".

While [[higher arithmetic geometry]] (i.e. [[E-∞ arithmetic geometry]]) is not [[cohesion|cohesive]] over the standard [[base (∞,1)-topos]] [[∞Grpd]], it does turn out to exhibit this kind of relative [[differential cohesion]] in a way that the corresponding relative [[differential cohomology hexagon]] subsumes the traditional [[arithmetic fracture square]] of prop. \ref{ArithmeticFractureSquare}:


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


This is effectively the content of ([Lurie "Completions", section 4](#LurieProper)), a refinement to [[stable homotopy theory]] of what in [[homological algebra]] is sometimes known as _[Greenlees-May duality](fracture+theorem#CompletionAndTorsionOnDerivedCategories)_.

For our purposes we notice the following immediate consequence.

+-- {: .num_cor #FractureFromCohesion}
###### Corollary

The traditional arithmetic fracture square of prop. \ref{SullivanArithmeticFracture} is the left part of the "[differential cohomology diagram](differential+cohomology+diagram#TheHexagonDiagram)" induced by the [[adjoint modality]] $(\Pi_{\mathfrak{a}} \dashv \flat_{\mathfrak{a}} )$ of prop. \ref{CompletionTorsionAdjointModalityForModuleSpectra}, for the special case that $A = \mathbb{S}$ is the [[sphere spectrum]] and $\mathfrak{a} = (p)$ a [[prime ideal]]

$$
  \array{
    &&  \Pi_{\mathfrak{a}dR} X && \stackrel{\mathbf{d}}{\longrightarrow} && \flat_{\mathfrak{a}dR} X 
    \\
    & \nearrow & & \searrow & & \nearrow && \searrow
    \\
    \Pi_{\mathfrak{a}dR} \flat   X  &&  && X &&  && \Pi_{\mathfrak{a}} \flat_{\mathfrak{a}dR} X
    \\
    & \searrow &  & \nearrow & & \searrow && \nearrow
    \\
    && \flat_{\mathfrak{a}} X && \longrightarrow && \Pi_{\mathfrak{a}} X
  }
  \,,
$$

=--

+-- {: .num_remark #FracturingOnEInfinityAlgebras}
###### Remark

By the discussion at _[[completion of modules]]_ in the section _[Monoidalness](completion+of+a+module#Monoidalness)_, the [[adjoint modality]] of prop. \ref{CompletionTorsionAdjointModalityForModuleSpectra} is a [[monoidal (∞,1)-functor]] without, possibly, respect the [[tensor unit]] in $A Mod$. This means that $(\Pi_{\mathfrak{a}}\dashv \flat_{\mathfrak{a}})$ passes to "[[commutative monoid in a symmetric monoidal (∞,1)-category|commutative ∞-monoids]]-without unit" in $A Mod$, hence to ([[Isbell duality|formal duals of]]) [[nonunital E-∞ algebras]]. 
By [this proposition](nonunital+Ek-algebra#RelationToAugmentedEkAlgebras) ([Lurie "Algebra", prop. 5.2.3.15](#LurieAlgebra)) [[nonunital E-∞ rings]]  are [[equivalence of (∞,1)-categories|equivalent]] to [[augmented E-∞ rings]] over the [[sphere spectrum]], hence this is [[E-∞ arithmetic geometry]] under $Spec(\mathbb{S})$.

Notice that in addition $\Pi_{\mathfrak{a}}$ here should preserve [[finite products]] (because by the discussion at  [completion of a module -- monoidalness](completion%20of%20a%20module#Monoidalness) the underlying $\Pi_{\mathfrak{a}} \colon A Mod \to A Mod$ preserves all small [[(∞,1)-colimits]] and because by 
[this proposition](commutative+monoid+in+a+symmetric+monoidal+%28infinity%2C1%29-category#LimitsInCRing) finite coproducts in $CRng(A Mod)$ are computed in the underlying $A Mod$.

Therefore we may think of $\Pi_{\mathfrak{a}}$ as a [[shape modality]] and of $\flat_{\mathfrak{a}}$ as a [[sharp modality]] on affine [[E-∞ geometry|E-∞]]-[[arithmetic geometry]] under $Spec(\mathbb{S})$ -- namely on [[Isbell duality|formal duals]] of [[nonunital E-∞ rings]] .

(It may be entertaining to note that on the level of [[∞-groups of units]] then [[E-∞ arithmetic geometry]] under $Spec(\mathbb{S})$ translates to [[abelian ∞-groups]] of [[twisted cohomology|twists]] over the [[sphere spectrum]] -- which has been argued to be the homotopy-theoretic incarnation of [[superalgebra]], see at _[superalgebra -- abstract idea](super+algebra#AbstractIdea)_ for more on this.)

=--

In conclusion, the situation is summarized by the following table.

+-- {: bluebox}

[[!include arithmetic cohesion -- table]]

=--



## References

* {#BunkeGepner13} [[Ulrich Bunke]], [[David Gepner]], _Differential function spectra, the differential Becker-Gottlieb transfer, and applications to differential algebraic K-theory_ ([arXiv:1306.0247](http://arxiv.org/abs/1306.0247))

* {#BunkeNikolausVoelkl13} [[Ulrich Bunke]], [[Thomas Nikolaus]], [[Michael Völkl]], _Differential cohomology theories as sheaves of spectra_ ([arXiv:1311.3188](http://arxiv.org/abs/1311.3188))


* {#Frenkel05} [[Edward Frenkel]], _Lectures on the Langlands Program and Conformal Field Theory_, in _Frontiers in number theory, physics, and geometry II_, Springer Berlin Heidelberg, 2007. 387-533. ([arXiv:hep-th/0512172](http://arxiv.org/abs/hep-th/0512172))

* {#LurieProper} [[Jacob Lurie]], section 4 of _[[Proper Morphisms, Completions, and the Grothendieck Existence Theorem]]_

* {#LurieAlgebra} [[Jacob Lurie]], _[[Higher Algebra]]_

* {#NSS12} [[Thomas Nikolaus]], [[Urs Schreiber]], [[Danny Stevenson]], _[[schreiber:Principal ∞-bundles -- theory, presentations and applications|Principal ∞-bundles -- General theory]]_, Journal of Homotopy and Related Structures, June 2014 ([arXiv:1207.0248](http://arxiv.org/abs/1207.0248))

* {#Schreiber13} [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos|Differential cohomology in a cohesive ∞-topos]]_, based on Habilitation thesis, Hamburg 2011 ([arXiv:1310.7930](http://arxiv.org/abs/1310.7930))

* {#Schreiber14} [[Urs Schreiber]], _[[schreiber:What, and for what is Higher geometric quantization]]_, notes for a talk given at _[Symmetries and correspondences in number theory, geometry, algebra, physics: intra-disciplinary trends](https://www.maths.nottingham.ac.uk/personal/ibf/files/sc3.html)_, Oxford, July 5-8 2014

Related talk notes:

* [[Urs Schreiber]], _[[schreiber:Differential cohesion and Arithmetic geometry]]_, talk at [Karslruher Weihnachts-Workshop 2015](http://www.math.kit.edu/iag3/~herrlich/seite/weihnachts-workshops)
