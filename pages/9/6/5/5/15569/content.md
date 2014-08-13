
> under construction

#Contents#
* table of contents
{:toc}

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


## Overview

Notice that the idea of "inter-geometric theory" is ancient, it originates with the [[synthetic geometry]] of Euclid which, with the parallel axiom removed, subsumes Euclidean, spherical and hyperbolic geometry. The idea of refining such a [[synthetic mathematics|synthetic reasoning]] to [[differential geometry]] is not as ancient, but far from new, this is known as _[[synthetic differential geometry]]_. For the kinds of applications as mentioned above we need something a bit more expressive, we consider _[[differential cohesion|differentially]] [[cohesive (infinity,1)-topos|cohesive homotopy theory]]_.

A _differentially cohesive homotopy theory_ is a geometric homotopy theory -- hence a context for [[higher geometry]]  -- $\mathbf{H}$ which is equipped with an extra structure that axiomatically encodes that the [[homotopy types]] in $\mathbf{H}$ may have [[infinitesimal object|infinitesimal extension]]. 

| $\mathbf{H}_{reduced}$ | $\hookrightarrow$ | $\mathbf{H}$ | $\longrightarrow$ |  $\mathbf{H}_{infinitesimal}$  |
|---------|---|-------------------|---|------------------|
| [[cohesion]] |  | [[differential cohesion]] |  | [[infinitesimal cohesion]] |
| [[moduli ∞-stacks]] |  | [[synthetic differential ∞-groupoids]] |  |  [[formal moduli problems]] |

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

This is analogous to two situations in arithmetic geometry:

1. in [[arithmetic fracture squares]] ...

1. in [[geometric Langlands duality]] and [[Weil conjecture on Tamagawa numbers]] the moduli of bundles $[X,C]$ are similarly decomposed into bundles on formal disks and complements of points

   $$
     GL_n(\mathbb{Q})\backslash GL_n(\mathbb{A}_{\mathbb{Q}})/GL_n(\mathbb{A}_{\mathbb{Z}})
   $$

(...)

We discuss how arithmetic concepts such as [[adeles]], [[ideles]], the [[idele class group]] etc. have structural analogs in any context of [[differential cohesion]]. We show that specifically in the context of [[complex analytic infinity-groupoid|complex analytic cohesion]] these reproduce the correct analogs of the arithmetic concepts as predicted by the [[function field analogy -- table|function field analogy table]].


## Fracture squares

### In arithmetic geometry

Suppose one studies [[loop spaces]], say the [[Witten genus]]. Then one studies the [[moduli stack of elliptic curves]] $\bar\mathcal{M}_{ell}$. If one is ambitious and considers not just [[modular forms]] but [[topological modular forms]] here, then this is to be taken over [[Spec(Z)]], hence is the stack of solutions of the [[Weierstrass equation]] 

$$
  y^2 + a_1 x y + a_3 y = x^3 + a_2 x^2 + a_4 x + a_6
  \,.
$$

This stack may be hard to analyze. A common approach is to consider elliptic curves over the [[rational numbers]] and over the [[p-adic integers]] and re-built the general case from this.




| [[curve]] | ring of global functions | [[ring of functions]] on a point | [[formal power series]] around a point |   |
|----|----|-----|-----|----|
| [[Spec(Z)]] | $\mathbb{Z}$  |  $\mathbb{F}_p$ ([[finite field]]) | $\mathbb{Z}_p$ ([[p-adic integers]]) |  $= \underset{\leftarrow}{\lim}( \cdots \to \mathbb{Z}/(p^2)\to \mathbb{Z}/(p) )$  |
| $\mathbb{C}$ ([[complex plane]]) | entire [[holomorphic functions]]  | $\mathbb{C}_x$ | $\mathbb{C}[ [ t_x ] ]$ |

This underlies the following fact

+-- {: .num_lemma}
###### Lemma

The canononical maps between the [[commutative rings]] of [[integers]] $\mathbb{Z}$, of [[rational numbers]] $\mathbb{Q}$ of [[integral adeles]] $\mathbb{A}_{\mathbb{Z}}$ and of [[adeles]] $\mathbb{A}_{\mathbb{Q}}$ form a square [[commuting diagram]]


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
$$

in [[CRing]] which is both a [[pullback]] as well as a [[pushout]] square.


=--

(...)

### In homotopy theory

(...)


## Differential cohesion


The synthetic axiomatics which we consider here is the following.

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