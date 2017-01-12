
$\,$

$\,$


> this entry is one section of "[[geometry of physics -- supergeometry and superphysics]]"
> which is one chapter of "[[geometry of physics]]"

> previous section: _[[geometry of physics -- supersymmetry]]_

> under construction


$\,$



A remarkable consequence of the general fact that [[supergeometry]] is slightly
[[non-commutative geometry|non-commutative]] is that [[super Minkowski spacetimes]],
regarded as the translational part of [[supersymmetry]] [[super Lie algebras]],
carry non-trivial higher [[spin group|spin]]-[[invariant]] [[cocycles]] in super-[[Lie algebra cohomology]].
Generally, invariant $(p+2)$-cocycles on [[cosets]] $X$ induce interesting
[[action functionals]] for $p+1$-dimensional [[sigma-model]] [[field theories]]
with [[target space]] $X$. These encode the [[dynamics]] of _fundamental $p$-[[branes]]_, in a general sense,
that propagate on (or "in") the space(-time) $X$. For $p = 1$ and $X$ the coset of a [[compact Lie group]],
then this is known as the _[[WZW model]]_ describing a [[string]] that propagates on $X$.
Hence generally we may speak of _[[higher WZW models]]_ here.

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/OldBraneScan.jpg" width="350">
</div>

Accordingly,  each of the exceptional invariant cocycles on [[super Minkowski spacetime]] defines a [[super p-brane]]
[[sigma model]]. These happen to be the _fundamental [[Green-Schwarz superstring]]_ and the _fundamental [[supermembrane]]_
that appear in, or rather that _define_ [[string theory]] and [[M-theory]] ("M-theory" is a "non-committal" shorthand for "membrane theory", [(Ho&#345;ava-Witten 95, p. 2](#M-theory#NonCommittal)) -- a fact known as the "old [[brane scan]]" ([Ach&#250;carro-Evans-TownsendWiltshire 87](#AETW87)).

<div style="float:left;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/schreiber/files/SecondBraneExtensions.png" width="350">
</div>

Now in higher generalization of how an invariant 2-cocycle on some [[super Minkowski spacetime]] corresponds to a [[central extension|central]]
super-[[Lie algebra extension]] of it to a higher dimensional spacetime, so ever higher cocycle,
i.e. every $p+2$-cocycle for $p \geq 1$, corresponds to a [[super Lie n-algebra|super Lie (p+1)-algebra]] extension
of [[super Minkowski spacetime]], sometimes called an "[[extended super Minkowski spacetime]]".
It turns out that on the [[super Lie n-algebra]] extensions defined by the cocycles for the [[super-string]] and the [[super-membrane]]
make further invariant higher cocycles appear. Interpreting these in turn as [[higher WZW models]] for [[super p-branes]]
it turns out that they correspond to the [[D-branes]] and to the [[M5-brane]] that appear in [[string theory]]/[[M-theory]].
This generalizes the old [[brane scan]] to a tree-like structure of higher invariant extensions that may be called the
_[[schreiber:brane bouquet]]_ of [[string theory]]/[[M-theory]], since it neatly organizes the complete [[super p-brane]] content
purely in terms of [[super Lie n-algebra]] theory ([FSS 13](#FSS13)).

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/schreiber/files/BraneBouquetWithDualities.jpg" alt="the brane bouquet" width="550" />
</div>

Moreover, it turns out that on [[cocycles]] of [[super Lie n-algebras]] there is a natural [[higher Lie theory|higher Lie theoretic]]
operation of _[[double dimensional reduction]]_: the image in [[rational homotopy theory]] of the [[adjunction unit]]
for the "[[cyclic homology|cyclification]]" [[adjunction]] ([[free loop space]] [[homotopy quotient|homotopy quotiented]] by loop rotation). Applying this to the [[schreiber:brane bouquet]] turns out to yield
relations between the super Lie $n$-algebraic cocycles that embody all the [[dualities in string theory]]
at the level of [[rational homotopy theory]]:
the [[KK-compactification]] from [[M-theory]] to [[type IIA string theory]], the [[T-duality]] of the latter to
[[type IIB string theory]], the [[S-duality]] of the latter, and its relation  to [[F-theory]] ([FSS 16a](#FSS16a), [FSS 16b](#FSS16b)).

Notice that all this concerns _fundamental_ [[super p-branes]] (sometimes referred to as "probe $p$-branes")
-- in generalization of "[[fundamental particles]]" and "fundamental string" --
and in contrast to "solitonic $p$-branes" or "[[black p-branes|black branes]]".
In fact the [[black branes]] (that appear for notably in the [[AdS/CFT correspondence]]) follow from
the fundamental [[super p-branes]]: their [[worldvolumes]] are the [[BPS state]] solutions to the [[supergravity]] [[equations of motion]]
which express but the consistent globalization of the fundamental [[super p-brane]] [[sigma models]]
([Bergshoeff-Sezgin-Townsend 87](#BergshoeffSezginTownsend87)), and moreover their [[worldvolume]] theories
are but the [[perturbation theory]] of the fundamental [[super p-branes]] about these asymptotic singular loci
([Claus-Kallosh-vanProeyen 97](#ClausKalloshProeyen97), [Claus-Kallosh-Kumar-Townsend 98](#ClausKalloshKumarTownsend98)).


<div style="float:left;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/TheMTheoryAmoeba.jpg" alt="the brane bouquet" width="300" />
</div>

Hence a fair bit of the folklore structure of [[string theory]]/[[M-theory]] is (re-)discovered by systematic classification of
the invariant higher extensions of
[[super Minkowski spacetimes]] in [[super Lie n-algebra]] [[homotopy theory]]. But by the
discussion at _[[geometry of physics -- supersymmetry]]_, the relevant [[super-Minkowski spacetimes]]
themselves are themselves already classified as the consecutive ordinary invariant extensions of just the
[[superpoint]] (we review this [below](#SuperMinowskiSpacetimes)).
In conclusion then, a fair bit of the structure of [[string theory]]/[[M-theory]]
is (re-)discovered by a systematic classification of the consecutive invariant higher extension
of the [[superpoint]] in [[super Lie n-algebra]] [[homotopy theory]]. This is what we discuss here.

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/ComputationWithYoungTableaux.jpg" width="300">
</div>

Computationally, all the these cocycles in the [[schreiber:brane bouquet]] exist
due to special _[[Fierz identities]]_ (which we discuss [below](#FierzIdentities)),
namely due to special spinoral higher [[Clebsch-Gordan coefficients]] that
express the [[tensor product of representations|tensor-product]] operation in the [[real spin representation|real]] [[representation ring]] of the [[spin groups]]
in the given dimensions ([D'Auria-Fr&#233;-Maina-Regge 82](#DAuriaFreMainaRegge82), [D'Auria-Fr&#233; 82a](#DAuriaFre82a),
[D'Auria-Fr&#233; 82b](#DAuriaFre82b))).

Hence there is a tight interplay between spinorial [[representation theory]], [[superalgebra|super-algebraic]] [[higher Lie theory]],
[[spacetime]] that gives rise to a finite system of [[universal exceptionalism|exceptional]] structures: the [[super p-branes]].
This is what we discuss here.


$\,$

$\,$

$\,$



#Fundamental super p-branes#
* table of contents
{:toc}


$\,$

$\,$

In order to put our discussion in perspective, we start by surveying some

* _[History and background](#HistoryAndBackground)_.

Then in order to lay the basis of all our discussion to follow, which is super [[higher Lie theory]],
we recall [[super Lie algebras]] and discuss their generalization to [[super L-∞ algebras]]
(whose [[formal duals]] are called "[[FDA]]"s in the physics literature):

* _[Super L-infinity cohomology and FDAs](#SuperLInfinityCohomologyAndFDAs)_.

The basic example of [[super Lie algebras]] that induces all phenomena to follow are
the super-translation parts of [[supersymmetry]] algebras, the [[super Minkowski spacetimes]]
introduced in detail in _[[geometry of physics -- supersymmetry]]_. Since here we
frequently need to refer to these structures, we recall their definition again in

* _[Super Minkowski spacetimes](#SuperMinowskiSpacetimes)_.

The key phenomena to be discussed are then the non-trivial invariant [[cocycles]] in the
super-[[Lie algebra cohomology]] of [[super Minkowski spacetimes]] (sometimes called _[[tau cohomology]]_
in the physics literature). Computationally these correspond to certain identities satisfied by
qadrilinear expressions in [[Majorana spinors]]. Such relations are an example of _[[Fierz identities]]_
and so we pause to explain these in

* _[Fierz identities](#FierzIdentities)_.

This then gives rise to the "old [[brane scan]]" of [[Green-Schwarz super-string]] and [[super-membranes]],
which is the classification of the $Spin$-invariant
super-[[Lie algebra cohomology]] of [[super Minkowski spacetimes]] ([[tau cohomology]]):


* _[The super-string and the super-membrane](#TheSuperStringAndTheSuperMembrane)_.

Using our previously established general theory of super-[[L-∞ algebra cohomology]],
we see that the cocycles in the old [[brane scan]] classify
_higher_ central extensions of [[super Minkowski spacetimes]], namely [[super Lie n-algebras]]
called _[[extended super Minkowski spacetimes]]_:

* _[Extended super Minkowski spacetimes](#ExtendedSuperMinkowskiSpacetime)_

A key point then is that these [[super Lie n-algebras]] obtained from [[super Minkowski spacetime]],
turn out to carry _further_ super $L_\infty$-cocycles, not present on the plain
[[super Minkowski spacetimes]]. These correspond to all the [[D-branes]] and to the [[M5-branes]].
This we discuss in

* _[The super D-branes and the M5-brane](#TheSuperDBranes)_

This gives a tree of consecutive higher central [[super Lie n-algebra]] extensions, originating from the [[superpoint]],
the _[[schreiber:brane bouquet]]_. Next we [[descent|descend]] these iterated central extensions to  single but non-central
higher cocycles. The result turns out to be the image in [[rational homotopy theory]] of the classifying maps of the
[[background fields]] in [[string theory]]/[[M-theory]]: the [[B-field]]-twisted [[RR-fields]] and the M-flux fields.
This we discuss in

* _[Fields](#Fields)_.

There turn out to be special relations among these. In particular passing from  super-[[L-∞ algebra cohomology]]
to the corresponding _[[cyclic cohomology]]_ turns out to be the [[formal dual]] operation of what in
physics is called [[double dimensional reduction]] of [[branes]] (here: of their [[background fields]]). This
crucial operation we discuss in

* _[Double dimensional reduction](#DoubleDimensionalReduction)_ .

By systematically applying this [[super Lie n-algebra|super Lie n-algebraic]] formalization of [[double dimensional reduction]] via [[cyclic cohomology]], we discover all the pertinent [[dualities in string theory]], [[rational homotopy theory|rationally]]:

* _[Dualities](#Dualities)_.







## History and background
 {#HistoryAndBackground}

Below we present fundamental [[super p-branes]] as [[universal exceptionalism|exceptional]]
algebro-geometric structures that are discovered by applying the magnifying glass
(namely a [[Whitehead tower]] construction) of [[super Lie n-algebra]] [[homotopy theory]]
to the atom of [[superspace]]: the [[superpoint]], following ([FSS 13](#FSS13), [FSS 15](#FSS15), [FSS 16a](#FSS16a), [FSS 16b](#FSS16b)).

This is not the perspective from which [[super p-branes]] were arrived at historically. In order
to put our discussion into perspective, here we briefly review some of the historical background.

$\,$

[[perturbation theory|Perturbative]] [[string theory]] on geometric backgrounds is defined by the [[Neveu-Schwarz-Ramond model]], namely by [[sigma-model]] [[2d super conformal field theories]] (of [[central charge]] 15) on [[worldsheets]] $\Sigma$ that are [[super Riemann surfaces]], with [[target spaces]] $X$ that are ordinary (i.e. "bosonic") [[spacetime]] [[manifolds]].

These [[worldsheet]] [[field theories]] are induced from _[[action functionals]]_, namely from variants of the standard [[energy functional]] ([[Polyakov action]]) on the [[mapping space]] $[\Sigma,X]$ of smooth functions

$$
  \phi \;\colon\; \Sigma \longrightarrow X
$$

from the [[worldsheet]] $\Sigma$ to target [[spacetime]] $X$.

The central theorem of perturbative superstring theory
(the no ghost theorem with[[GSO projection]]) says that the excitation spectrum of such a [[2d SCFT]] are the quanta of the [[perturbation theory|perturbations]] of a higher dimensional [[effective field theory|effective]] [[supergravity]] [[field theory]] on target spacetime, hence transforms under [[supersymmetry]] on target spacetime.

This is the fundamental prediction of the assumption of fundamental strings:

1. assuming that the [[fundamental particles]] that run in [[Feynman diagrams]] are fundamentally (at high energy) the ground state modes of a fundamental [[string]],

1. demanding that there are [[fermion|fermionic]] particles among these,

implies

1. that the string must be the [[spinning string]] (have fermions in its [[worldsheet]] theory), which in turn implies...

1. that it is the [[superstring]] (worldsheet [[supersymmetry]] mixes the worldsheet bosons and fermions), precisely: the [[Neveu-Schwarz-Ramond superstring]], which then in addition implies...

1. that its [[target space]] [[effective field theory]] is a [[supergravity]] theory, hence that also the effective target space fields exhibit _local_ [[supersymmetry]] (i.e. "high energy supersymmetry", different from "low energy supersymettry" that the [[LHC]] was looking for).

| main theorem of [[perturbative string theory|perturbative super-string theory]] |
|-------------------------------------------------------------------------------------------------|
| $ \underset{\text{spinning string}}{\underbrace{\text{fermions} \;+\; \text{strings}}} \;=\; \text{superstring} \;\Rightarrow\; \text{supergravity} $ |

The first step in this implication (identifying the [[spinning string]] as the [[superstring]]) is fairly straightforward
(in fact this is how the concept of [[supersymmetry]] was discovered in "the west", in the first place),
but the second step (that the superstring excitations necessarily are quanta of a [[spacetime]] [[supergravity]] theory)
appears as a miracle from the point of view of the [[Neveu-Schwarz-Ramond superstring]].
It comes out this way by non-trivial computation, but is not manifest in the theory.

In order to improve on this situation, [[Michael Green]] and [[John Schwarz]] searched for and found ([Green-Schwarz 81](#GreenSchwarz81), [Green-Schwarz 82](#GreenSchwarz82) [Green-Schwarz 84](#GreenSchwarz84), for the history see [Schwarz 16, slides 24-25](#Schwarz16)) a suitably equivalent string [[action functional]] that would manifestly exhibit [[spacetime]] [[supersymmetry]].
Acordingly, the this is now called the _[[Green-Schwarz action functional]]_.

| [[action functional]] for [[superstring]] | manifest [[supersymmetry]] |
|----|---|
| [Neveu-Ramond-Schwarz super-string]] | on [[worldsheet]]  |
| Green-Schwarz super-string | on [[target space|target]] [[spacetime]] |

The basic idea is to pass to the evident [[supergeometry|supergeometric]] analogue of the bosonic string action:

Let $\Sigma$ be a [[closed manifold]] of [[dimension]] 2 -- representing the abstract _[[worldsheet]]_ of a string. Let $(X,g)$ be a [[pseudo-Riemannian manifold]] -- representing a purely [[gravity|gravitational]] [[spacetime]] background. Then the [[action functional]] governing the [[bosonic string]] propagating in this spacetime is the functional

$$
  \exp(\tfrac{i}{\hbar} S_{bos})
  \;\colon\;
  [\Sigma,X]
   \longrightarrow
  \mathbb{R}/_{\hbar}\mathbb{Z}
$$

on the [[smooth space|smooth]] [[mapping space]] $[\Sigma,X]$ (of [[smooth functions]] $\Sigma \to X$), that simply assigns the proper [[relativity|relativistic]] [[volume]] of the image of the [[worldsheet]] $\Sigma$ in [[spacetime]]:

$$
  (\Sigma\overset{\phi}{\longrightarrow} X)
    \;\mapsto\;
  S_{kin}(\phi)
  \coloneqq
  \int_\Sigma vol_{\phi^\ast g}
  \,.
$$

(This is the _[[Nambu-Goto action]]_. It is classically equivalently to the [[Polyakov action]] which is the genuine starting point for the quantum [[Neveu-Ramond-Schwarz super-string]]. Howver, since, as we discuss below, the Green-Schwarz action naturally generalizes to that of other [[p-branes]] it is more natural to consider the Nambu-Goto form of the action here.)

When here $(X,g)$ is generalized to a [[superspacetime]] [[supermanifold]] with [[orthogonal structure]] encoded by a [[super-vielbein]] $e$, then the same form of the action functional still makes sense and produces a functional on the [[supergeometry|supergeometric]] [[mapping space]] $[\Sigma,X]$. Moreover, by construction this action functional now is invariant under the [[superisometry group]] of $(X,g)$, hence under global spacetime [[supersymmetry]].


$$
\array{
  \text{symmetry of worldsheet theory}
  \\
  \array{
    && \Sigma
    \\
    & {}^{\mathllap{\phi}}\swarrow && \searrow^{\mathrlap{\phi'}}
    \\
    X &&\underset{\simeq}{\longrightarrow}&& X
  }
  \\
  \text{super-isometry of target spacetime}
}
$$

However, [[Michael Green|Green]] and [[John Schwarz|Schwarz]] noticed that this [[kinetic action]] functional $\phi \mapsto \int_\Sigma vol_{\phi^\ast e}$ does _not_ quite yield dynamics that is equivalent to that of the [[Neveu-Schwarz-Ramond super-string]]: when the [[equations of motion]] hold ("on [[shell]]") it has more fermionic degrees of freedom than present in the [[Neveu-Ramond-Schwarz super-string]]. The key insight of Green and Schwarz was that one may add an extra summand $S_{WZW}$ (whose notation we explain in a moment) to the plain super-[[Nambu-Goto action]] $S_{kin}$, such that the resulting [[action functional]] enjoys a further 1-parameter [[symmetry]], called _[[kappa-symmetry]]_. This is the [[Green-Schwarz action functional]]:

$$
  S_{GS} = S_{kin} + S_{WZW}
  \,.
$$

Moreover, they showed that restricting the
[[dynamics]] of the [[Green-Schwarz superstring]] to the $\kappa$-symmetric states, then it does become equivalent, classically
to that of the [[Neveu-Ramond-Schwarz super-string]].

Finally they showed that when [[gauge fixing]] the [[Green-Schwarz action functional]] to [[light-cone gauge]]
(which is possible whenever [[target spacetime]] admits two [[lightlike]] [[Killing vector]]) then the [[Green-Schwarz string]]
may be [[quantization|quantized]] by a standard procedure and the resulting
[[quantum system|quantum]] dynamics is equivalent to that of the [[Neveu-Schwarz-Ramond super-string]].
This provides the desired conceptual [[proof]] for the observed local [[target spacetime]] [[supersymmetry]]
of super-string [[effective field theory]], at least for backgrounds that admit two lightlike Killing vectors.
(The [[quantization]] of the [[Green-Schwarz superstring]] away from [[light cone gauge]] remains an open problem.)


While Green-Schwarz's extra [[kappa-symmetry]] term $S_{WZW}$ this serves a clear purpose as a means to an end, originally its geometric meaning was mysterious. However, in ([Henneaux-Mezincescu 85](#HenneauxMezincescu85)) it was observed (expanded on in ([Rabin 87](#Rabin87), [Azcarraga-Townsend 89](#AzcarragaTownsend89), [Azcarraga-Izquierdo 95,chapter 8](#AzcarragaIzquierdo95))), that the
[[Green-Schwarz action functional]] describing the [[super-string]] in $d+1$-dimensions does have a neat geometrical interpretation: it is simply the ([[parameterized WZW model|parameterized]]) _[[Wess-Zumino-Witten model]]_ for

1. [[target space]] being locally [[super Minkowski spacetime]] $\mathbb{R}^{d-1,1|\mathbf{N}}$ regarded as the [[coset]] [[supergroup]]

   $$
     \mathbb{R}^{d-1,1\vert \mathbf{N}}
       \;\simeq\;
     Iso(\mathbb{R}^{d-1,1\vert \mathbf{N}}) / Spin(d-1,1)
   $$

   for $\mathbf{N}$ a [[real spin representation]] (the "number of supersymmetries"), $Iso(\mathbb{R}^{d-1,1\vert \mathbf{N}})$ the corresponding [[super Poincaré group]] and $Spin(d-1,1)$ its [[Lorentzian manifold|Lorentz-signature]] [[spin group|Spin]] [[subgroup]];

1. [[WZW-term]] being a local potential for the unique (up to rescaling, if it exists) $Spin(d-1,1)$-[[invariant]] [[Lie algebra cohomology|super Lie algebra 3-cocycle]] $\mu_[F1}$ on the [[super Poincaré Lie algebra]] $\mathfrak{iso}(\mathbb{R}^{d-1,1\vert \mathbf{N}})$, with components locally given by the Gamma-matrices of the given [[Clifford algebra]] representation; in terms of the [[super vielbein]] $(e^a, \psi^\alpha)$:

   $$
     \mu_{F1} = \overline{\psi} \wedge \Gamma_A \psi \wedge e_a
   $$

   and so in components the bi-fermionic component of $\mu_{F1}$ is

   $$
     (\mu_{F1})_{a \alpha \beta} = \Gamma_{a \alpha \beta}
   $$

   and all other components vanish.

More in detail, just as ordinary [[Minkowski spacetime]] $\mathbb{R}^{d-1,1}$ may be identified with the [[translation group]]
along itself, with canonical [[linear basis]] of [[left invariant 1-forms]] given by the canonical [[vielbein]] field

$$
  \{e^a \coloneqq \mathbf{d}x^a\}_{a = 0}^{d-1}
  \,,
$$

where $\{x^a\}$ are the canonical [[coordinates]] on $\mathbb{R}^{d-1,1}$, so [[super Minkowski spacetime]] $\mathbb{R}^{d-1,1\vert \mathbf{N}}$ for some [[real spin representation]] $\mathbf{N}$ is characterized as the [[supergroup]] whose [[left invariant 1-forms]] constitute the $\mathbb{Z} \times \mathbb{Z}/2\mathbb{Z}$-bigraded differential with generators the [[super-vielbein]]

$$
  \underset{deg = (1,even)}{\underbrace{e^a}}
    \;\coloneqq\;
  \mathbf{d}x^a + \overline{\theta}\Gamma^a \mathbf{d} \theta
  \;\;\;\,,\;\;\;\;\;\;\;\;\;\;
  \underset{deg = (1,odd)}{\underbrace{\psi^\alpha}} \;\coloneqq\; \mathbf{d}\theta^\alpha
  \,,
$$

where $(x^a, \theta^\alpha)$ are the canonical coordinates on $\mathbb{R}^{d-1,1\vert \mathbf{N}}$, with the odd-graded elements $\{\theta^\alpha\}$ spanning the given real [[spin representation|Spin(d-1,1)-representation]] $\mathbf{N}$ with [[Clifford algebra]] generators $\{\Gamma^a\}$.

Now while ordinary [[Minkowski spacetime]] $\mathbb{R}^{d-1,1}$ is an [[abelian group]], reflected by the fact that its [[left-invariant 1-forms]] are all closed

$$
  \mathbf{d}e^a = 0 \;\;\;\;\;\; on \; \mathbb{R}^{d-1,1}
  \,,
$$

the key phenomenon of [[supersymmetry]] (that two [[fermions]] pair to a [[bosons]]) means that $\mathbb{R}^{d-1,1\vert \mathbf{N}}$ is slightly non-abelian, reflected by the fact that the [[super-vielbein]] is not closed

$$
  \mathbf{d} e^a =  \overline{\psi} \wedge \Gamma^a \psi
  \;\,,\;\;\;\;\;\;
  \mathbf{d} \psi^\alpha = 0
  \,.
$$

This elementary effect is the source of all the rich structure seen in the [[Green-Schwarz super-string]]
and generally in all [[super p-brane]] theory.
(The above differential is equivalently that in the [[Chevalley-Eilenberg algebra]] of [[super Minkowski spacetime]],
hence its [[cohomology]] is the super-[[Lie algebra cohomology]] of [[super Minkowski spacetime]]. In parts of the
[[physics]] literature this is referred to a "[[tau cohomology]]".)

In particular, for special combinations of [[spacetime]] [[dimension]] $d$ and number of [[supersymmetries]] $\mathbf{N}$
(i.e. [[real spin representation]] $N$) then the 3-form

$$
  \mu_{F1} =  \overline{\psi} \wedge \Gamma_a \psi \wedge e^a
$$

is a non-trivial [[super Lie algebra|super]] [[Lie algebra cocycle]] on $\mathbb{R}^{d-1,1\vert \mathbf{N}}$, in that
$\mathbf{d}\mu_{F1} = 0$ and so that there is no [[left invariant differential form]] $b$ with $\mathbf{d}b = \mu_[F1}$
(beware here the left-invariance condition: there are of course non-left-invariant potentials for $\mu_{F1}$,
and in fact these are exactly the possible [[Lagrangian densities]] for the WZW action functional $S_{WZW}$).

This happens notably for

1. $d = 10$ and $\mathbf{N} = (1,0) = \mathbf{16}$ ([[heterotic string]])

1. $d = 10$ and $\mathbf{N} = (2,0) = \mathbf{16} + \mathbf{16}$ ([[type IIB superstring]])

1. $d = 10$ and $\mathbf{N} = (1,1) = \mathbf{16} + \mathbf{16}^\ast$ ([[type IIA superstring]]).

(It also happens in some lower dimensions, where however the corresponding [[Neveu-Schwarz-Ramond string]] develops a [[conformal anomaly]] after [8quantization]] ("non-critical strings"). This classification of cocycles is part of what has come to be known as the _[[brane scan]]_ in superstring theory, see below.)

In this equivalent formulation, the [[Green-Schwarz action functional]] for the superstring has the following simple form:

Let $(X,e)$ be a [[superspacetime]], hence a [[supermanifold]] $X$ equipped with a [[super-vielbein]] $e$ (super-[[orthogonal structure]]) which is locally modeled on $\mathbb{R}^{d-1,1\vert \mathbf{N}}$ (technically: a [[torsion of a G-structure|torsion]]-free [[super-Cartan geometry]] modeled on $Spin(d-1,1) \hookrightarrow Iso(\mathbb{R}^{d-1,1\vert \mathbf{N}})$). Write $\mu_{F1}^X \in \Omega^3(X)$ for the [[super differential form]] on $X$ which is the induced [[definite globalization of WZW term|definite globalization]] of the cocycle $\mu_{F1}$ over $X$. For $U \subset X$ any [[contractible topological space|contractible]] [[subspace]], then the restriction of $\mu^X_{F1}|_{U} \in \Omega^3(U)$ of $\mu_{F1}^X$ to $U$ is exact, and hence admits a potential $B_U \in \Omega^2(U)$, i.e. such that $\mathbf{d} B = \mu^X_{F1}|_U$.

Then for $\Sigma$ a 2-dimensional [[closed manifold]], the [[Green-Schwarz action functional]]

$$
  \exp(\tfrac{i}{\hbar} S_{GS})
  \;\colon\;
  [\Sigma,X]_U
    \longrightarrow
  \mathbb{R}/_{\hbar} \mathbb{Z}
$$

is the function on the super-[[smooth mapping space]] $[\Sigma,X]_U$ of morphisms of [[supermanifolds]] $\phi \colon \Sigma \to X$ which factor through $U$, given by

$$
  \phi
    \;\mapsto\;
  \int_\Sigma vol_{\phi^\ast e}
   \;+\;
  \int_\Sigma \phi^\ast B_U
  \;\;\;\,,\;\;\;\;\;\;\;\;\;
  \mathbf{d} B_U = \mu^X_3|_U
  \,.
$$

In order to get rid of the restriction to some [[chart]] $U \subset X$ one needs to add global data. The need for this is at least mentioned briefly in ([Witten 86, p. 261 (17 of 20)](#Witten86)), but seems to have otherwise been ignored in the physics literature. The general solution is to promote the local potentials $B$ to the connection $\hat B$ on a [[Super Gerbes|super gerbe]] ([FSS 13](#FiorenzaSatiSchreiber13)). This is a choice of [[higher prequantization]]

$$
  \array{
    && \mathbf{B}^{2}(\mathbb{R}/_\hbar \mathbb{Z}) & \text{prequantization}
    \\
    & {}^{\mathllap{\hat B}}\nearrow & \downarrow^{\mathrlap{curv}}
    \\
    X
     &\underset{\mu^X_{F1}}{\longrightarrow}&
    \mathbf{\Omega}^3
    &
    \text{3-form curvature}
  }
  \,.
$$


Writing $\int_\Sigma \phi^\ast \hat B$ for the [[volume holonomy]] of a [[circle 2-bundle with connection]] $\hat B$, then the globally defined Green-Schwarz sigma model

$$
  \exp(\tfrac{i}{\hbar} S_{GS})
  \;\colon\;
  [\Sigma, X]
    \longrightarrow
  \mathbb{R}/_\hbar\mathbb{Z}
$$

is given by

$$
  \phi \;\mapsto\; \int_\Sigma vol_{\phi^\ast} + \int_\Sigma \phi^\ast \hat B
  \;\;\,,
  \;\;\;\;\;\;\;
  curv(\hat B) = \mu_{F1}^X
  \,.
$$

This form of the Green-Schwarz action functional for the string has evident generalization to other [[p-branes]]. Whenever there is a [[spin group|Spin(d-1,1)]]-[[invariant]] $(p+2)$-cocycle $\mu_{p+2}$ on $\mathbb{R}^{d-1,1\vert \mathbf{N}}$, then one may ask for a higher gerbe ([[higher prequantum line bundle]]) $\hat C$ with [[curvature]] $\mu^X_{p+2}$ and consider the analogous functional.

The triples $(d,\mathbf{N},p)$ (spacetime dimension, number of supersymmetries, dimension of brane) such that

$$
  \mu_{p+2}
    \;\coloneqq\;
  \overline{\psi} \wedge \Gamma^{a_1 \cdots a_p} \psi \wedge e_{a_1} \wedge \cdots \wedge e_{a_p}
$$

is a nontrivial cocycle, hence for which there is such a Green-Schwarz action functional for $p$-branes on $\mathbb{R}^{d-1,1\vert \mathbf{N}}$ may be classified and form what is called the _[[brane scan]]_ ([Ach&#250;carro-Evans-TownsendWiltshire 87](#AETW87), [Brandt 12-13](#Brandt12-13)):

{#DuffBraneScan} <div style="float:left;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/DuffBraneScan.jpg" height="600">
</div>

The graphics on the left is from ([Duff 87](#Duff87)). The diagonal lines indicate [[double dimensional reduction]], taking a $(p+1)$-brane in $(d+1)$ dimensions to a $p$-brane in $d$-dimensions.

For instance for $(d = 11, \; \mathbf{N} = \mathbf{32}, \; p = 2)$ one finds a cocycle, and the corresponding GS-action functional is that of the fundamental [[M2-brane]].

This was a striking confluence of brane physics and classification of [[super Lie algebra|super]] [[Lie algebra cohomology]]. But just as striking as the matching, was what it lacked to match: the [[D-branes]] and the [[M5-brane]] ($d = 11$, $p = 5$) are lacking from the old brane scan. Incidentally, these lacking branes are precisely those branes on which the branes that do appear on the brane scan may end, equivalently those branes that have [[higher gauge fields]] on their [[worldvolume]] (tensor multiplets).

An action functional for the [[M5-brane]] analogous to a Green-Schwarz action functional was found in ([BLNPST 97](#BLNPST97), [APPS 97](#APPS97)). It is again the sum of a kinetic term and a WZW-like term, but the WZW-like term does not come from a cocycle on a (super-)group.

In order to deal with this, it was suggested in ([CAIB 99](#CAIB99), [Sakaguchi 00](#Sakaguchi00), [Azcarraga-Izquierdo 01](#AzcarragaIzquierdo01)) that there is an algebraic structure called "[[extended super-Minkowski spacetimes]]" that generalizes [[super Minkowski spacetime]] and serves to unify the Green-Schwarz-like models for the D-branes and the M5-brane with the original Green-Schwarz models for the string and the M2-brane.

These [[extended super-Minkowski spacetimes]] carry algebraic analogs of super Lie algebra cocycles, such that the relevant terms for the [[D-branes]] and the [[M5-brane]] do appear after all, hence such that all the branes in [[string theory]]/[[M-theory]] are unified. In fact these "[[extended super-Minkowski spacetimes]]" are precisely the "FDA"s that have been introduced before in the [[D'Auria-Fré formulation of supergravity]] and what became identified as the 7-cocycle for the [[M5-brane]] this way had earlier been recognized algebraically as an stepping stone for an elegant re-derivation of [[11-dimensional supergravity]] ([D'Auria-Fr&#233; 82](#DAuriaFre82)).

The ([[higher differential geometry|higher]]) geometric meaning of these constructions was found in ([Fiorenza-Sati-Schreiber 13](#FiorezaSatiSchreiber13)): these algebraic structures of "[[extended super-Minkowski spacetimes]]"/FDAs are precisely the [[Chevalley-Eilenberg algebras]] of [[super Lie n-algebra]]-extensions of [[super-Minkowski spacetime]] which are classified by the cocycles that serve as the GS-WZW terms of the $p_1$-branes that may end on those $p_2$-branes whose cocycles are carried by the extended super-Minkowski spacetime.

Hence the missing $p$-branes in the old [[brane scan]] (classifying just cocycles on [[super Lie algebras]]) do appear as one generalizes (super) Lie algebras to (super) [[strong homotopy Lie algebras]] = [[L-infinity algebras]]. Moreover, each brane intersection law (one brane species may end on another) is now matched to a super $L_\infty$-algebra [[extension]] and so the old brane scan is generalized to a tree of branes _[[schreiber:The brane bouquet]]_:

<img src="https://ncatlab.org/schreiber/files/BraneBouquetWithDualities.jpg" alt="the brane bouquet" width="900" />

Each item in this bouquet denotes a [[super L-infinity algebra]] and each arrow denotes an [[L-infinity extension]] classified by a cocycle which encodes the GS-WZW term of the brane named by the domain of the arrow. Moreover, arrows pass exactly from one brane species to the brane species that may end on the former.

In ([Fiorenza-Sati-Schreiber 13](#FiorenzaSatiSchreiber13)) it is shown that all these [[super L-infinity algebras]] [[Lie integration|Lie integrate]] to [[smooth super-n-groups]], and all the cocycles [[Lie integration|Lie integrate]] to [[Super Gerbes|super-gerbes]] on these, such that the induced [[volume holonomy]] is the relevant generalized GS-WZW term. For detailed exposition see at _[[schreiber:Structure Theory for Higher WZW Terms]]_.

With this generalized perspective, now the Green-Schwarz-type action functionals describe _all_ the [[p-branes]] in [[string theory]]/[[M-theory]].

Again, in order to make this generally true one needs to apply a [[higher prequantization]] -- a choice of [[line n-bundle with connection|line (p+1)-bundle with connection]] -- in order to globalize the [[WZW-terms]] ([Fiorenza-Sati-Schreiber 13](#FiorenzaSatiSchreiber13))

$$
  \array{
    && \mathbf{B}^{p+1}(\mathbb{R}/_\hbar \mathbb{Z}) & \text{prequantization}
    \\
    & {}^{\mathllap{\hat A_{p+1}}}\nearrow & \downarrow^{\mathrlap{curv}}
    \\
    X
     &\underset{\mu^X_{p+2}}{\longrightarrow}&
    \mathbf{\Omega}^{p+2}
    &
    (p+2)\text{-form curvature}
  }
  \,.
$$

Hence $\hat A_{p+1}$ is the actual [[background field]] that the $p$-brane couples to. There is considerably more information in $\hat A_p$ than in its curvature $curv(\hat A_{p+1}) = \mu_{p+2}$. For instance for the [[M2-brane]] one may find the local super [[moduli space]] for local choices of $\hat A_{p+1}$ for the given $\mu_{4}$ on [[KK-compactifications]] to $d = 4$. It turns out that the bosonic [[body]] of this moduli space is the [[exceptional tangent bundle]] on which the [[U-duality]] group [[E7]] has a canonical action (see at _[[schreiber:From higher to exceptional geometry]]_).

This highlights that Green-Schwarz functionals capture fundamental ("microscopic") aspects of $p$-branes. In contrast, often $p$-branes are discussed in their [[soliton|solitonic]] incarnation as _[[black branes]]_. These solitonic branes sit at asymptotic boundaries of [[anti-de Sitter spacetime]] and carry [[conformal field theories]], related to the ambient [[supergravity]] by [[AdS-CFT duality]].

This phenomenon is indeed a consequence of the fundamental Green-Schwarz branes:

Consider a 1/2-[[BPS state]] solution of [[type II supergravity]] or [[11-dimensional supergravity]], respectively. These solutions locally happen to have the same classification as the Green-Schwarz branes. Hence we may consider a configuration $\phi \colon \Sigma \to X$ of the corresponding fundamental $p$-brane which embeds $\Sigma$ into the asymptotic AdS boundary of the given 1/2 BPS spacetime $X$. Then it turns out that restricting the Green-Schwarz action functional to small fluctuations around this configuration, and applying a [[diffeomorphism]] [[gauge fixing]], then the resulting action functional is that of a [[supersymmetry|supersymmetric]] [[conformal field theory]] on $\Sigma$ as in the [[AdS-CFT]] dictionary:

| fundamental $p$-brane | -fluctuations about asymptotic AdS configuration$\to$ |  solitonic $p$-brane |
|----|-----|---|
| Green-Schwarz action functional |  | [[supersymmetric|super]]-[[conformal field theory]] |

([Claus-Kallosh-Proeyen 97](#ClausKalloshProeyen97), [Claus-Kallosh-Kumar-Townsend 98](#ClausKalloshKumarTownsend98), [AFFFTT 98](#AFFFTT98) [Pasti-Sorokin-Tonin 99](#PastiSorokinTonin99))

In fact the [[BPS-state]] condition itself is neatly encoded in the Green-Schwarz action functionals: by construction they are invariant under the [[spacetime]] [[superisometry group]]. Hence the [[Noether theorem]] implies that there are corresponding [[conserved currents]], whose [[Dickey bracket]] forms a super-[[Lie algebra extension]] of the Lie algebra of supersymmetries.

$$
  \array{
    \left\{
    \array{
      X && \overset{=}{\longrightarrow} && X
      \\
      & {}_{\mathllap{\hat C}}\searrow
        &\swArrow&
      \swarrow_{\mathrlap{\hat C}}
      \\
      && \mathbf{B}^{p+1}(\mathbb{R}/_{\hbar} \mathbb{Z})
    }
    \right\}
      &\longrightarrow&
    \left\{
    \array{
      X && \overset{\simeq}{\longrightarrow} && X
      \\
      & {}_{\mathllap{\hat C}}\searrow
        &\swArrow&
      \swarrow_{\mathrlap{\hat C}}
      \\
      && \mathbf{B}^{p+1}(\mathbb{R}/_{\hbar} \mathbb{Z})
    }
    \right\}
     &\longrightarrow&
    \left\{
      \array{
        X && \overset{\simeq}{\longrightarrow} && X
      }
    \right\}
    \\
    \text{topological currents}
    &&
    \text{Noether currents}
    &&
    \text{symmetries}
  }
$$

Here the "$\swArrow$" filling the triangles is the non-trivial gauge transformation by which the [[WZW term]] (as any WZW term) is preserved under the symmetries (instead of being fixed identically). It is the information in this transformations which makes the currents form an extension of the symmetries.

Here this yields the famous brane charge extensions of the super-isometry super Lie algebra of the schematic form

$$
  \{Q_\alpha, Q_\beta\}
  \;=\;
  (C \Gamma^a_{\alpha \beta}) P_a
  \;+\;
  (C \Gamma^{a_1 \cdots a_p})_{\alpha \beta} Z_{a_1, \cdots, a_p}
$$

(for $Q$ a [[Killing spinor]] and $P$ its corresponding [[Killing vector]]) known as the [[type II supersymmetry algebra]] and the [[M-theory supersymmetry algebra]], respectively ([Azc&#225;rraga-Gauntlett-Izquierdo-Townsend 89](#AGIT89)). In fact it yields super-[[L-infinity algebra extensions|Lie n-algebra extensions]] of which the familiar super Lie algebra extensions are the 0-truncation ([Sati-Schreiber 15](#SatiSchreiber15), [[schreiber:Local prequantum field theory|Khavkine-Schreiber 16]]).

In summary, the nature and classification of Green-Schwarz action functionals captures in a mathematically precise way a good deal of the core structure of [[string theory|string]]/[[M-theory]].

In fact, the [[super L-infinity algebra|super Lie-n algebraic]] perspective on the Green-Schwarz functionals via the [[schreiber:brane bouquet]] also solves the following open problem on [[M-branes]]:

it is famously known from [[Freed-Witten anomaly]]-cancellation that the [[D-brane charges]] are not in fact just in [[de Rham cohomology]] in every second degree, but are in [[twisted K-theory]], hence [[rational homotopy theory|rationally]] in [[twisted de Rham cohomology]], with the twist being the [[F1-brane]] charge (from the fundamental). It is an open problem to determine what becomes of these [[twisted K-theory]] charge groups as one lifts F1/D$p$-branes in string theory to M2/M5-branes in [[M-theory]].


|   | intersecting branes | charges in [[generalized cohomology theory]]
|-----|--------------|----------------------|
| [[string theory]] | [[F1-brane|F1]]/[[D-brane|Dp-branes]] | [[twisted K-theory]] |
| [[M-theory]]  | [[M2-brane|M2]]/[[M5-branes]] | ??? |

Notice that there are "microscopic degrees of freedom" of the theory encoded by the choice of [[generalized cohomology theory]] here, generalizing the extra degrees of freedom in the choice of a WZW-term already mentioned above. In general for $E$ a cohomology theory and $E \longrightarrow E \otimes \mathbb{Q}$ its [[Chern character]] map (for instance from [[topological K-theory]] to [[ordinary cohomology]] in every second degree), then a choice of genuine charges is the extra information encoded in a lift

$$
  \array{
    && E
    \\
    & {}^{\mathllap{\text{true charge}}}\nearrow & \downarrow^{\mathrlap{ch}}
    \\
    X &\underset{\text{rational} \atop  \text{charge}}{\longrightarrow}& E \otimes \mathbb{Q}
  }
$$

But [[rational homotopy theory|rationally]] [[schreiber:The brane bouquet]] allows to derive this from first principles:

Above we saw that the naive cocycles of the [[D-branes]] and of the [[M5-brane]] are not defined on the actual [[spacetime]],  but on some "extended" spacetime, which is really a [[smooth super infinity-groupoid]] extension of spacetime. Hence we should ask if these cocycles [[descent|descend]] to the actual super-spacetime while picking up some twists.

One may prove that:

* the F1/D$p$-brane GS-WZW cocycles descend to 10d type II superspacetime to form a single cocycle in rational twisted K-theory, just as the traditional lore reqires ([Fiorenza-Sati-Schreiber 16](#FiorenzaSatiSchreiber16));

* the M2/M5 GS-WZW cocycles descent to 11d superspacetime to form a single cocycle with values in the [[rational n-sphere|rational 4-sphere]] ([Fiorenza-Sati-Schreiber 16](#FiorenzaSatiSchreiber16)).

This has implications on some open conjectures regarding [[M-theory]], for more on this see _[[schreiber:Equivariant cohomology of M2/M5-branes]]_.


$\,$

We now explain all this in detail.

$\,$










## Super $L_\infty$-cohomology and FDAs
 {#SuperLInfinityCohomologyAndFDAs}

We recall [[super Lie algebras]], and amplify their [[formal dual]] description in terms of their
[[Chevalley-Eilenberg algebras]]. This makes it immediate to see what [[super L-∞ algebras]] are,
again they are conveniently expressed (if they are of [[finite type]]) via their [[formal dual]] [[Chevalley-Eilenberg algebras]].


+-- {: .num_defn #SuperLieAlgebraAsLieAlgebraInternalToSuperVectorSpaces}
###### Definition

A _[[super Lie algebra]]_ is a [[Lie algebra]] [[internalization|internal]]
to the [[symmetric monoidal category]] $sVect = (Vect^{\mathbb{Z}/2}, \otimes_k, \tau^{super} )$ of [[super vector spaces]].
Hence this is

1. a [[super vector space]] $\mathfrak{g}$;

1. a homomorphism

   $$
     [-,-] \;\colon\; \mathfrak{g} \otimes_k \mathfrak{g} \longrightarrow \mathfrak{g}
   $$

   of super vector spaces (the _super Lie bracket_)

such that

1. the bracket is skew-symmetric in that the following [[commuting diagram|diagram commutes]]

   $$
     \array{
       \mathfrak{g} \otimes_k \mathfrak{g}
         &
           \overset{\tau^{super}_{\mathfrak{g},\mathfrak{g}}}{\longrightarrow}
         &
       \mathfrak{g} \otimes_k \mathfrak{g}
       \\
       {}^{\mathllap{[-,-]}}\downarrow && \downarrow^{\mathrlap{[-,-]}}
       \\
       \mathfrak{g} &\underset{-1}{\longrightarrow}& \mathfrak{g}
     }
   $$

   (here $\tau^{super}$ is the [[braiding]] [[natural isomorphism]] in the category of [[super vector spaces]])

1. the [[Jacobi identity]] holds in that the following [[commuting diagram|diagram commutes]]

   $$
     \array{
       \mathfrak{g} \otimes_k \mathfrak{g} \otimes_k \mathfrak{g}
       &&
         \overset{\tau^{super}_{\mathfrak{g}, \mathfrak{g}} \otimes_k id }{\longrightarrow}
       &&
       \mathfrak{g} \otimes_k \mathfrak{g} \otimes_k \mathfrak{g}
       \\
       & {}_{\mathllap{[-,[-,-]]} - [[-,-],-] }\searrow && \swarrow_{\mathrlap{[-,[-,-]]}}
       \\
       && \mathfrak{g}
     }
     \,.
   $$

=--

Externally this means the following:

+-- {: .num_prop #SuperLieAlgebraTraditional}
###### Proposition

A [[super Lie algebra]] according to def. \ref{SuperLieAlgebraAsLieAlgebraInternalToSuperVectorSpaces} is equivalently

1. a $\mathbb{Z}/2$-[[graded vector space]] $\mathfrak{g}_{even} \oplus \mathfrak{g}_{odd}$;

1. equipped with a [[bilinear map]] (the _super Lie bracket_)

   $$
     [-,-] : \mathfrak{g}\otimes_k \mathfrak{g} \to \mathfrak{g}
   $$

   which is _graded_ skew-symmetric: for $x,y \in \mathfrak{g}$ two elements of homogeneous degree $\sigma_x$, $\sigma_y$, respectively, then

   $$
     [x,y] = -(-1)^{\sigma_x \sigma_y} [y,x]
     \,,
   $$

1. that satisfies the $\mathbb{Z}/2$-graded [[Jacobi identity]] in that
for any three elements $x,y,z \in \mathfrak{g}$ of homogeneous super-degree $\sigma_x,\sigma_y,\sigma_z\in \mathbb{Z}_2$ then

   $$
     [x, [y, z]] = [[x,y],z] + (-1)^{\sigma_x \cdot \sigma_y} [y, [x,z]]
     \,.
   $$

A [[homomorphism]] of super Lie algebras is a homomorphisms of the underlying [[super vector spaces]]
which preserves the Lie bracket. We write

$$
  sLieAlg
$$

for the resulting [[category]] of super Lie algebras.

=--


+-- {: .num_defn #CEAlgebraofSuperLieAlgebra}
###### Definition

For $\mathfrak{g}$ a [[super Lie algebra]] of [[finite number|finite]] [[dimension]], then its _[[Chevalley-Eilenberg algebra]]_ $CE(\mathfrak{g})$ is the super-[[Grassmann algebra]] on the [[dual vector space|dual]] super vector space

$$
  \wedge^\bullet  \mathfrak{g}^\ast
$$

equipped with a [[differential]] $d_{\mathfrak{g}}$ that on generators is the linear dual of the super Lie bracket

$$
  d_{\mathfrak{g}} \;\coloneqq\; [-,-]^\ast \;\colon\; \mathfrak{g}^\ast \to \mathfrak{g}^\ast \wedge \mathfrak{g}^\ast
$$

and which is extended to $\wedge^\bullet \mathfrak{g}^\ast$ by the graded Leibniz rule (i.e. as a graded [[derivation]]).

$\,$

Here all elements are $(\mathbb{Z} \times \mathbb{Z}/2)$-bigraded, the first being the _cohomological grading_ $n$ in $\wedge^\n \mathfrak{g}^\ast$, the second being the _super-grading_ $\sigma$ (even/odd).

For $\alpha_i \in CE(\mathfrak{g})$ two elements of homogeneous bi-degree $(n_i, \sigma_i)$, respectively,
the [[signs in supergeometry|sign rule]] is

$$
  \alpha_1 \wedge \alpha_2 = (-1)^{n_1 n_2} (-1)^{\sigma_1 \sigma_2}\; \alpha_2 \wedge \alpha_1
  \,.
$$

(See at _[[signs in supergeometry]]_ for discussion of this sign rule and of an alternative sign rule that is also in use. )

=--

We may think of $CE(\mathfrak{g})$ equivalently as the [[dg-algebra]] of [[invariant differential form|left-invariant]]
[[super differential forms]] on the [[Lie theory|corresponding]] simply connected [[super Lie group]] .


The concept of [[Chevalley-Eilenberg algebras]] is traditionally introduced as a means to define
[[Lie algebra cohomology]]:

+-- {: .num_defn #SuperLieAlgebraCohomology}
###### Definition

Given a [[super Lie algebra]] $\mathfrak{g}$, then

1. an _$n$-cocycle_ on $\mathfrak{g}$ (with [[coefficients]] in $\mathbb{R}$) is an element of degree $(n,even)$ in its [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{g})$ (def. \ref{CEAlgebraofSuperLieAlgebra}) which is $d_{\mathbb{g}}$ closed.

1. the cocycle is non-trivial if it is not $d_{\mathfrak{g}}$-exact

1. hene the _super-[[Lie algebra cohomology]]_ of $\mathfrak{g}$ (with [[coefficients]] in $\mathbb{R}$) is the [[cochain cohomology]] of its [[Chevalley-Eilenberg algebra]]

   $$
     H^\bullet(\mathfrak{g}, \mathbb{R}) = H^\bullet(CE(\mathfrak{g}))
     \,.
   $$

=--



The following says that the [[Chevalley-Eilenberg algebra]] is an equivalent incarnation of the [[super Lie algebra]]:

+-- {: .num_prop #FormalDualCE}
###### Proposition

The functor

$$
  CE \;\colon\; sLieAlg^{fin}  \hookrightarrow dgAlg^{op}
$$

that sends a finite dimensional [[super Lie algebra]] $\mathfrak{g}$ to its [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{g})$
(def. \ref{CEAlgebraofSuperLieAlgebra}) is a [[fully faithful functor]] which hence exibits [[super Lie algebras]]
as a [[full subcategory]] of the [[opposite category]] of [[differential-graded algebras]].

=--

This makes it immediate how to generalize to [[super L-infinity algebras]]:

+-- {: .num_defn #SuperLInfinityAlgebra}
###### Definition

A **[[super L-∞ algebra]]** is an [[L-∞ algebra]] [[internalization|internal to]] the [[symmetric monoidal category]] of [[super vector spaces]] (def. \ref{CategoryOfSuperVectorSpaces}).

=--

Explicitly this means the following:

+-- {: .num_defn #SuperGradedSignatureOfPermutation}
###### Definition
**(super graded signature of a permutation)**

Let $V$ be a $\mathbb{Z}$-[[graded object|graded]] [[super vector space]], hence a $\mathbb{Z} \times (\mathbb{Z}/2)$-bigraded vector space.

For $n \in \mathbb{N}$ let

$$
  \mathbf{v} = (v_1, v_2, \cdots, v_n)
$$

be an [[n-tuple]] of elements of $V$ of homogeneous degree $(n_i, s_i) \in \mathbb{Z} \times \mathbb{Z}/2$, i.e. such that $v_i \in V_{(n_i,s_i)}$.

For $\sigma$ a [[permutation]] of $n$ elements, write $(-1)^{\vert \sigma \vert}$ for the [[signature of a permutation|signature of the permutation]], which is by definition equal to $(-1)^k$ if $\sigma$ is the composite of $k \in \mathbb{N}$ permutations that each exchange precisely one pair of neighboring elements.

We say that the _super $\mathbf{v}$-graded signature of $\sigma$_

$$
  \chi(\sigma, v_1, \cdots, v_n) \;\in\; \{-1,+1\}
$$

is the product of the [[signature of a permutation|signature of the permutation]] $(-1)^{\vert \sigma \vert}$ with a factor of

$$
  (-1)^{n_i n_j}(-1)^{s_i s_j}
$$

for each interchange of neighbours $(\cdots v_i,v_j, \cdots )$ to $(\cdots v_j,v_i, \cdots )$ involved in the decomposition of the permuation as a sequence of swapping neighbour pairs (see at _[[signs in supergeometry]]_ for discussion of this combination of super-grading and homological grading).

=--

Now def. \ref{SuperLInfinityAlgebra} is equivalent to the following def. \ref{sLInfinityDefinitionViaGeneralizedJacobiIdentity}. This is just the definiton for [L-infinity algebras](#L-infinity-algebra#DefinitionViaHigherBrackets), with the pertinent sign $\chi$ now given by def. \ref{SuperGradedSignatureOfPermutation}.


+-- {: .num_defn #sLInfinityDefinitionViaGeneralizedJacobiIdentity}
###### Definition

An _[[super L-∞ algebra]]_ is

1. a $\mathbb{Z} \times (\mathbb{Z}/2)$-[[graded object|graded]] [[vector space]] $\mathfrak{g}$;

1. for each $n \in \mathbb{N}$ a [[multilinear map]], called the _$n$-ary bracket_, of the form

   $$
     l_n(\cdots)
       \;\coloneqq\;
     [-,-, \cdots, -]_n
     \;\colon\;
       \underset{n \; \text{copies}}{\underbrace{\mathfrak{g} \otimes \cdots \otimes \mathfrak{g}}}
       \longrightarrow
       \mathfrak{g}
   $$

   and of degree $n-2$

such that the following conditions hold:

1. (**super graded skew symmetry**) each $l_n$ is graded antisymmetric, in that for every [[permutation]] $\sigma$ of $n$ elements and for every [[n-tuple]] $(v_1, \cdots, v_n)$ of  homogeneously graded elements $v_i \in \mathfrak{g}_{\vert v_i \vert}$ then

   $$
     l_n(v_{\sigma(1)}, v_{\sigma(2)},\cdots ,v_{\sigma(n)})
     =
     \chi(\sigma,v_1,\cdots, v_n) \cdot l_n(v_1, v_2, \cdots v_n)
   $$

   where $\chi(\sigma,v_1,\cdots, v_n)$ is the super $(v_1,\cdots,v_n)$-graded signature of the permuation $\sigma$, according to def. \ref{SuperGradedSignatureOfPermutation};

1. (**strong homotopy [[Jacobi identity]]**) for all $n \in \mathbb{N}$, and for all [[n-tuple|(n+1)-tuples]] $(v_1, \cdots, v_{n+1})$ of homogeneously graded elements $v_i \in \mathfrak{g}_{\vert v_i \vert}$ the followig [[equation]] holds

   \[
     \label{LInfinityJacobiIdentity}
     \sum_{{i,j \in \mathbb{N}} \atop {i+j = n+1}}
     \sum_{\sigma \in UnShuff(i,j)}
     \chi(\sigma,v_1, \cdots, v_{n})
     (-1)^{i(j-1)}
      l_{j} \left(
        l_i \left( v_{\sigma(1)}, \cdots, v_{\sigma(i)} \right),
        v_{\sigma(i+1)} , \cdots , v_{\sigma(n)}
      \right)
     = 0
     \,,
   \]

   where the inner sum runs over all $(i,j)$-[[unshuffles]] $\sigma$ and where $\chi$ is the super graded signature sign from def. \ref{SuperGradedSignatureOfPermutation}.


A _strict [[homomorphism]]_ of super $L_\infty$-algebras

$$is
  \mathfrak{g}_1 \longrightarrow \mathfrak{g}_2
$$

is a [[linear map]] that preserves the bidegree and all the brackets, in an evident sens.

A _strong homotopy homomorphism_ ("sh map") of super $L_\infty$-algebras is something weaker than that, best defined in [[formal duals]], below in def. \ref{SuperLInfinityCEAlgebra}.

=--

+-- {: .num_remark #LInfinityTerminology}
###### Remark

Special cases of the general concept of [[super L-∞ algebras]] def. \ref{sLInfinityDefinitionViaGeneralizedJacobiIdentity} go by special names:

Let $\mathfrak{g}$ be a [[super L-∞ algebra]].

If $\mathfrak{g}$ is concentrated in even $\mathbb{Z}/2$-degree, it is called an _[[L-∞ algebra]]_.

If the only possibly non-vanishing brackets of $\mathfrak{g}$ are the unary one $[-]$ (which induces the structure of a [[chain complex]] on $\mathfrak{g}$) and the binary one, then $\mathfrak{g}$ is equivalently a (super-)[[dg-Lie algebra]].

If $\mathfrak{g}$ is concentrated in $\mathbb{Z}$-degrees 0 to $n-1$ then it is called a _[[super Lie n-algebra]]_.

In particular if $\mathfrak{g}$ is concentrated in degree 0, then it is equivalently a [[super Lie algebra]].

Combining this, if $\mathfrak{g}$ is concentrated in even $\mathbb{Z}/2$-degree and in $\mathbb{Z}$-degree 0 through $n-1$, then it is called a _[[Lie n-algebra]]_.

In particular if $\mathfrak{g}$ is concentrated in $\mathbb{Z}$-degree 0 and in even $\mathbb{Z}/2$-degree, then it is
equivalently a plain [[Lie algebra]].

=--


+-- {: .num_defn #SuperLInfinityCEAlgebra}
###### Definition

A super $L_\infty$ algebra $\mathfrak{g}$ is of _[[finite type]]_ if the underlying $\mathbb{Z} \times (\mathbb{Z}/2)$-[[graded vector space]] is degreewise of [[finite number|finite]] [[dimension]].

If $\mathfrak{g}$ is of finite type, then its [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{g})$ is the [[dg-algebra]] whose underlying [[graded algebra]] is the super-Grassmann algebra

$$
  \wedge^\bullet \mathfrak{g}^{\ast}
$$

of the graded degreewise [[dual vector space]] $\mathfrak{g}^\ast$, equipped with the [[differential]] which on generators is the sum of the [[dual linear maps]] of the $n$-ary brackets:

$$
  d_{\mathfrak{g}}
   \coloneqq
  [-]^\ast + [-,-]^\ast + [-,-,-]^\ast + \cdots
  \;\colon\;
  \wedge^1 \mathfrak{g}^\ast
    \longrightarrow
  \wedge^\bullet \mathfrak{g}^\ast
$$

and extended to all of $\wedge^\bullet \mathfrak{g}^\ast$ as a super-graded [[derivation]] of degree $(1,even)$.

Notice that here the [[signs in supergeometry]] are such that for $\alpha_i \in \mathfrak{g}^\ast_{(n_i,s_i)}$ elements of homogenous bidegree, then

$$
  \alpha_1 \wedge \alpha_2
  \;=\;
  -(-1)^{n_1 n_2} (-)^{s_1 s_2}
$$

and

$$
  d_{\mathfrak{g}}
  (\alpha_1 \wedge \alpha_2)
  \;=\;
  (d_{\mathfrak{g}} \alpha_1) \wedge \alpha_2
  +
  (-1)^{n_1} \alpha_1 \wedge (d_{\mathfrak{g}} \alpha_2)
  \,.
$$

(see at _[[signs in supergeometry]]_ for more on this).

A _strong homotopy homomorphism_ ("sh-map") between super $L_\infty$-algbras of [[finite type]]

$$
 f \;\colon\; \mathfrak{g}_1 \longrightarrow \mathfrak{g}_2
$$

is defined to be a homomorphism of [[dg-algebras]] between their [[Chevalley-Eilenberg algebras]] going the other way:


$$
  CE(\mathfrak{g}_1) \longleftarrow CE(\mathfrak{g}_2)
    \;\colon\;
  f^\ast
$$

(here $f^\ast$ is the primitive concept, and $f$ is defined as the [[formal dual]] of $f$). Hence the [[category]] of super $L_\infty$-algebras of [[finite type]] is the [[full subcategory]]

$$
  s L_\infty Alg \hookrightarrow dgAlg^{op}
$$

of the [[opposite category]] of [[dg-algebras]] on those that are CE-algebras as above.

Finally, the [[cochain cohomology]] of the [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{g})$ of a super $L_\infty$ algebra of [[finite type]] is its _[[L-∞ algebra cohomology]]_ with [[coefficients]] in $\mathbb{R}$:

$$
  H^\bullet(\mathfrak{g}, \mathbb{R})
   \;=\;
  H^\bullet(CE(\mathfrak{g}))
  \,.
$$


=--




+-- {: .num_remark #SuperLInfintiyAsFDA}
###### Remark
**(history of the concept of (super-)$L_\infty$ algebras)**

The identification of the concept of (super-)$L_\infty$-algebras has a non-linear history:

[[L-∞ algebras]] in the incarnation of higher brackets satisfying a higher Jacobi identity, 
def. \ref{sLInfinityDefinitionViaGeneralizedJacobiIdentity}
and remark \ref{LInfinityTerminology}, were introduced in
[Lada-Stasheff 92](https://ncatlab.org/nlab/show/L-infinity-algebra#LadaStasheff92), based on the 
example of such a structure on the [[BRST complex]] of the [[bosonic string]] that 
was found in the construction of [[closed string field theory]] in [Zwiebach 92](string+field+theory#Zwiebach93).
Some of this history is recalled in [Stasheff 16](#L-infinity-algebra#Stasheff16).

The observation that these systems of higher brackets are fully characterized by their Chevalley-Eilenberg dg-(co-)algebras
(def. \ref{SuperLInfinityCEAlgebra})
is due to [Lada-Markl 94](https://ncatlab.org/nlab/show/L-infinity-algebra#LadaMarkl94).
See [Sati-Schreiber-Stasheff 08, around def. 13](#SatiSchreiberStasheff08).

But in this dual incarnation, [[L-∞ algebras]] and more generally [[super L-∞ algebras]] (of [[finite type]]) 
had secretly been introduced within the [[supergravity]] literature already in [D'Auria-Fr&#233;-Regge 80](#DAuriaFreRegge80) and explicitly in [van Nieuwenhuizen 82](#Nieuwenhuizen82).
The concept was picked up in the [[D'Auria-Fré formulation of supergravity]] ([D'Auria-Fr&#233; 82](#DAuriaFre82)) and eventually came to be referred to as "FDA"s (short for "free differential algebra") in the [[supergravity]] literature (but beware that these dg-algebras 
are in general [[free construction|free]] only as graded-[[supercommutative superalgebras]], not as differential algebras)
The relation between super $L_\infty$-algebras and the "FDA"s of the [[supergravity]] literature is made explicit in ([FSS 13](#FSS13)).

| [[higher Lie theory]] | [[supergravity]] |
|----------------------------|-----------------------|
| $\,$ [[super Lie n-algebra]] $\mathfrak{g}$ $\,$ | $\,$ "FDA" $CE(\mathfrak{g})$ $\,$ |

The construction in [van Nieuwenhuizen 82](#Nieuwenhuizen82) in turn was motivated by the [[Sullivan algebras]]
in [[rational homotopy theory]] ([Sullivan 77](#rational+homotopy+theory#Sullivan77)). Indeed, their
dual incarnations in rational homotopy theory are [[dg-Lie algebras]] ([Quillen 69](#rational+homotopy+theory#Quillen69)),
hence a special case of $L_\infty$-algebras (remark \ref{LInfinityTerminology})

This close relation between [[rational homotopy theory]] and [[higher Lie theory]] might have remained less of a
secret had it not been for the focus of [[Sullivan minimal models]] on the non-[[simply connected topological space|simply connected]]
case, which excludes the ordinary [[Lie algebras]] from the picture. But the Quillen model of
[[rational homotopy theory]] effectively says that for $X$ a [[rational topological space]] then its [[loop space]]
[[∞-group]] $\Omega X$ is reflected, infinitesimally, by an [[L-∞ algebra]]. This perspective began to 
receive more attention when the [[Sullivan construction]] in [[rational homotopy theory]] was
concretely identified as higher [[Lie integration]] in [Henriques 08](#Lie+integration#Henriques).
A modern review that makes this [[L-∞ algebra]]-theoretic nature of [[rational homotopy theory]] manifest is in 
[Buijs-F&#233;lix-Murillo 12, section 2](rational+homotopy+theory#BuijsFelixMurillo12).

=--




However, what has not been used in the "FDA" literature is that super $L_\infty$-algebras are objects in _[[homotopy theory]]_:


+-- {: .num_prop}
###### Proposition
**([Pridham 10, prop. 4.36](https://ncatlab.org/nlab/show/model+structure+for+L-infinity+algebras#Pridham))**

There exists a [[model category]] such that

1. its [[fibrant objects]] are the (super-)[[L-∞ algebras]]

   with the above [[homomorphisms]] between them;

1. and

   * the weak equivalences between (super-)$L_\infty$-algebras are the [[quasi-isomorphisms]];

   * fibrations between (super-)$L_\infty$-algebras are the surjections

   on the underlying [[chain complex]] (using the unary part of the differential).

For more see at _[[model structure for L-infinity algebras]]_.

=--

$\,$

Concretely, this implies in particular that every [[homomorphisms]] of [[super L-∞ algebras]]

$$
  \array{
    \mathfrak{g}_1
    \\
    & {}_{\mathllap{f}}\searrow
    \\
    && \mathfrak{g}_2
  }
$$

is the composite of a [[quasi-isomorphism]] followed by a surjection

$$
  \array{
    \mathfrak{g}_1
     && \overset{\text{quasi-iso}}{\longrightarrow} &&
    \widetilde \mathfrak{g}_1
    \\
    & {}_{\mathllap{f}}\searrow && \swarrow_{\mathrlap{ {f_{fib}} \atop {\text{surjection}}}}
    \\
    && \mathfrak{g}_2
  }
  \,.
$$

That surjective homomorphism $f_{fib}$

is called a _[[fibrant replacement]]_ of $f$.

$\,$

+-- {: .num_defn }
###### Definition

Given [[homomorphisms]] of [[super L-∞ algebras]]

$$
  \mathfrak{g}_1 \overset{f}{\longrightarrow} \mathfrak{g}_2
$$

then its **[[homotopy fiber]]** $hofib(f)$

is the [[kernel]] of any fibrant replacement

$$
  hofib(f)
   \;\coloneqq\;
  ker(f_{fib})
  \,.
$$

=--

Standard facts in [[homotopy theory]] assert

that $hofib(f)$ is well-defined

up to [[quasi-isomorphism]].

See at _[Introduction to homotopy theory -- Homotopy fibers](https://ncatlab.org/nlab/show/Introduction+to+Stable+homotopy+theory+--+P#HomotopyFibers)_.

$\,$

+-- {: .num_prop}
###### Proposition
**([Fiorenza-Sati-Schreiber 13, prop. 3.5](#FSS13))**

Write

$$
  B^{p+1}\mathbb{R}
$$

for the **[[line Lie n-algebra|line Lie (p+1)-algebra]]**, given by

$$
  CE(B^{p+1}\mathbb{R})
   \;=\;
  \left(
    \wedge^\bullet \underset{\text{single generator} \atop \text{in deg.} \, (p+2,even)}{\underbrace{\langle c_{p+2} \rangle}}
    \;,\;
    d_{B^{p+1}\mathbb{R}} = 0
  \right)
  \,.
$$


A $(p+2)$-cocycle on an $L_\infty$-algebra is equivalently a homomorphim

$$
  \mu_{p+2} \;\colon\; \mathfrak{g} \longrightarrow B^{p+1}\mathbb{R}
  \,.
$$

The [[homotopy fiber]] of this map

$$
  \array{
    \widehat{\mathfrak{g}}
    \\
    {}^{\mathllap{hofib(\mu_{p+2})}}\downarrow
    \\
    \mathfrak{g}
    &\underset{\mu_{p+2}}{\longrightarrow}& B^{p+1}\mathbb{R}
  }
$$

is given by adjoining to $CE(\mathfrak{g})$ a single generator $b_{p+1}$

forced to be a potential for $\mu_{p+2}$:

$$
  CE(\widehat{\mathfrak{g}})
  \;\simeq\;
  CE(\mathfrak{g})[b_{p+1}]/(d b_{p+1} = \mu_{p+2})
  \,.
$$

=--

+-- {: .num_example}
###### Example

$\,$

The homotopy fiber of a 2-cocycle

is the classical [[central extension]]

that it classifies.

=--


$\,$

**Conclusion.**

$\;\;$ _The higher central extensions_

$\;\;$ _classified by higher cocycles_

$\;\;$ _are their homotopy fibers._

$\,$



some more stuff

$\,$

$\,$


The [[Chevalley-Eilenberg algebras]] which in def. \ref{CEAlgebra} and def. \ref{SuperLieAlgebraViaCE} we used to _characterize_ the corresponding (super) Lie algebras are of course traditionally introduced as the [[cochain complexes]] whose [[cochain cohomology]] is [[Lie algebra cohomology]]. We may conceptualize this as follows:

+-- {: .num_defn #SiteCartSp}
###### Definition

For $n \in \mathbb{N}$ write $\mathbb{R}^{1|0}[n]$ for the _[[line Lie n-algebra|line Lie (n+1)-algebra]]_, the [[super L-infinity algebra]] defined simply as the [[formal dual]] to the $(\mathbb{Z},\mathbb{Z}_2)$-graded commutative [[dg-algebra]]

$$
  CE(\mathbb{R}^{1|0}[n]) \coloneqq
  \left(
    \wedge^\bullet \mathbb{R}^{1|0}[n],
    \;
    d = 0
  \right)
$$

whose underlying [[graded algebra]] is freely generated from a single generator in degree $(n,even)$, and whose differential vanishes.

=--

+-- {: .num_remark #LieAlgebraCohomologAsHomomorphism}
###### Remark

Recall that being a "[[formal dual]]" to a dg-algebra here simply means that for $\mathfrak{g}$ any [[super Lie algebra]], the homomorphisms of [[super L-infinity algebras]] of the form

$$
  \mu \;\colon\; \mathfrak{g} \longrightarrow \mathbb{R}^{1|0}[n]
$$

are equivalently (by definition!) homomorphisms of [[dg-algebras]] of the form

$$
  CE(\mathfrak{g})
  \longleftarrow
  CE(\mathbb{R}^{1|0}[n])
  \,.
$$

Since the underlying graded algebra of $CE(\mathbb{R}^{1|0}[n])$ is free on a single generator $c$ in degree $n+1$, such a homomorphism is determined by the image of this generator

$$
  c \mapsto \mu \in CE(\mathfrak{g})
  \,.
$$

Moreover, the condition that this map respects the differentials, and since the differential on $CE(\mathbb{R}^{1|0}[n])$ vanishes by definition, this means that

$$
  \array{
     c &\mapsto& && \mu
     \\
     \downarrow^{\mathrlap{d_{\mathbb{R}^{1|0}[n]}}}
     && &&
    \downarrow^{\mathrlap{d_{\mathfrak{g}}}}
     \\
     0 &\mapsto& 0 &=& d_{\mathfrak{g}}\mu
  }
  \,.
$$

Hence such a moprhism $\mu$ is equivalently a _closed_ element of degree $(n+1)$ in $CE(\mathfrak{g})$, hence is equivalently a [[Lie algebra cohomology|super Lie algebra cocycle]] of degree $n+1$ on $\mathfrak{g}$.

This way [[line Lie n-algebra|line Lie (n+1)-algebra]] $\mathbb{R}^{1|0}[n]$ is the _[[moduli stack|moduli object]]_ for degree-$(n+1)$ Lie algebra cohomology in direct [[analogy]] of how for instance the familiar [[Eilenberg-MacLane space]] $B^{n+1}\mathbb{R} = K(\mathbb{Z},n+1)$ is the classifying space for degree $n+1$ [[ordinary cohomology]] of [[topological spaces]].

=--

One advantange of conceptualizing Lie algebra cocycles as in remark \ref{LieAlgebraCohomologAsHomomorphism} is that it neatly connects to the formulation of [[Lie algebra valued forms]] according to def. \ref{LieAlgValuedFormsViaDgAlgHoms}, def. \ref{SuperLieAlgValuedDiffForms}:


+-- {: .num_remark }
###### Remark

A $\mathbb{R}^{1|0}[n]$-valued differential form is simply an even closed differential $(n+1)$-form:

$$
  \Omega^1(\mathbb{R}^{p|q}, \mathbb{R}^{1|0}[n])
  \simeq
  Hom(CE(\mathbb{R}^{1|0}[n]), \Omega^\bullet(\mathbb{R}^{p|q}))
  \simeq
  \Omega^{n+1}(\mathbb{R}^{p|q})_{even,closed}
  \,.
$$

Hence a super Lie algebra $(n+1)$-cocycle $\mu$ on
$\mathfrak{g}$ naturally determines a map


$$
  \mu(-)
  \colon
  \Omega^1(\mathbb{R}^{p|q},\mathfrak{g})
  \longrightarrow
  \Omega^{n+1}(\mathbb{R}^{p|q})_{even,closed}
$$

given by forming the composite with the morphism representing the cocycle $\mu$

$$
  \left(
    \Omega^\bullet(\mathbb{R}^{p|q})
     \stackrel{A}{\longleftarrow}
  CE(\mathfrak{g})
  \right)
  \mapsto
  \left(
  \Omega^\bullet(\mathbb{R}^{p|q})
   \stackrel{A}{\longleftarrow}
  CE(\mathfrak{g})
  \stackrel{\mu^\ast}{\longleftarrow}
  CE(\mathbb{R}^{1|0}[n])
  \right)
$$

sending a [[Lie algebra valued form]] $A$ to a closed differential form $\mu(A)$.


=--














## Super Minkowski spacetimes
 {#SuperMinowskiSpacetimes}


In order set the scene, and for reference, we recall the nature of [[super Minkowski spacetimes]] from _[[geometry of physics -- supersymmetry]]_.

In all of the following it is most convenient to regard [[super Lie algebras]] dually
via their [[Chevalley-Eilenberg algebras]] ("[[FDA]]"s), via def. \ref{CEAlgebraofSuperLieAlgebra} and prop. \ref{FormalDualCE}:




+-- {: .num_defn #SuperMinkowskiSpacetime}
###### Definition

Let

$$
  d \in \mathbb{N}
$$

be a [[spacetime]] [[dimension]] and let

$$
  N \in Rep_{\mathbb{R}}(Spin(d-1,1))
$$

be a [[real spin representation]] of the [[spin group]] cover $Spin(d-1,1)$ of the [[Lorentz group]] $O(d-1,1)$
in this dimension. Then the _$d$-dimensional $N$-supersymmetric [[super-Minkowski spacetime]]_ $\mathbb{R}^{d-1,1|N}$
is the [[super Lie algebra]] that is characterized by the fact that its [[Chevalley-Eilenberg algebra]]
$CE(\mathbb{R}^{d-1,1})$ (def. \ref{CEAlgebraofSuperLieAlgebra}) is as follows:

The algebra has generators (as an [[associative algebra]] over $\mathbb{R}$)

$$
   \underset{deg = (1,even)}{\underbrace{e^a}}
   \;\;\;\;
   \text{and}
   \;\;\;\;
   \underset{deg = (1,odd)}{\underbrace{\psi^\alpha}}
$$

for $a \in \{0,1,2, \cdots, 9\}$ and $\alpha \in \{1, 2, \cdots dim_{\mathbb{R}}(N)\}$ subjects to the [[generators and relations|relations]]

$$
  \begin{aligned}
    e^a \wedge e^b = - e^b \wedge e^a
    \\
    \psi^\alpha \wedge \psi^\beta = + \psi^\beta \wedge \psi^\alpha
    \\
    e^a \wedge \psi^\alpha = - \psi^\alpha \wedge e^a
  \end{aligned}
$$

(see at _[[signs in supergeometry]]_), and the [[differential]] $d_{CE}$ acts on the generators as follows:

$$
  \begin{aligned}
    d_{\mathbb{R}^{d-1,1\vert N}} \; \psi^\alpha &
      \coloneqq
      0
    \\
    d_{\mathbb{R}^{d-1,1\vert N}} \; e^a
      & \coloneqq \overline{\psi} \wedge \Gamma^a \psi
    \\
    & \coloneqq   \left(C_{\alpha \alpha'} {\Gamma^a}^{\alpha'}{}_\beta\right)  \psi^\alpha \wedge \psi^\beta
  \end{aligned}
    \,,
$$

where

1. $\overline{\psi} \wedge \Gamma^a \psi$ denotes the $a$-component of the $Spin(d-1,1)$-invariant spinor bilinear pairing $N \otime N \to \mathbb{R}^d$ that comes with every [[real spin representation]] applied to $\psi \wedge \psi$ regarded as an $N \otimes N$-valued form;

1. hence in components (if $N$ is a [[Majorana spinor]] representation, by [this prop.](geometry+of+physics+--+supersymmetry#SpinorToVectorBilinearPairing)):

   1. $C = (C_{\alpha \alpha'})$ is the [[charge conjugation matrix]] (as discussed at _[[Majorana spinor]]_);

   1. $\Gamma^a = ((\Gamma^a)^{\alpha}{}_\beta)$ are the [[matrices]] representing the [[Clifford algebra]] action on $N$ in the [[linear basis]] $\{\psi^\alpha\}_{\alpha = 1}^{dim_{\mathbb{R}}(N)}$

1. [[Einstein summation convention|summation over paired indices]] is understood.

That this indeed yields a [[super Lie algebra]] follows by the symmetry and equivariance of the bilinear spinor pairing (via [this prop.](geometry+of+physics+--+supersymmetry#SpinorToVectorPairing)).

There is a canonical [[Lie algebra action]] of the [[special orthogonal Lie algebra]]

$$
  Lie(Spin(d-1,1)) \simeq \mathfrak{so}(d-1,1)
$$

on $\mathbb{R}^{d-1,1\vert 1}$. The _$N$-supersymmetric [[super Poincaré Lie algebra]] $\mathfrak{iso}(\mathbb{R}^{d-1,1\vert N})$ in dimension $d$_ is the [[super Lie algebra]] which is the [[semidirect product Lie algebra]] of this [[Lie algebra action]]

$$
  \mathfrak{iso}(\mathbb{R}^{d-1,1\vert N})
   =
  \mathbb{R}^{d-1,1\vert N} \rtimes \mathfrak{so}(d-1,1)
  \,.
$$

This is characterized by the fact that its [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{iso}(\mathbb{R}^{d-1,1\vert N}))$
is as follows:

it is [[generators and relations|generated]] from elements

$$
   \underset{deg = (1,even)}{\underbrace{e^a}}
   \;\;\;\;
   and
   \;\;\;\;
   \underset{deg = (1,odd)}{\underbrace{\psi^\alpha}}
   \;\;\;\;
   and
   \;\;\;\;
   \underset{deg = (1,even)}{\underbrace{\omega^{a b} = - \omega^{b a}}}
$$

with the [[super vielbein]] $(e^a, \psi^\alpha)$ as before, and with $\omega^{a b}$ the
[[dual basis]] of the induced [[linear basis]] for vectro space of skew-symmetric matricces
underlying the [[special orthogonal Lie algebra]]. The commutation relations are as before,
together with the relation that the generators $\omega^{a b}$ anti-commute with every generator.
Finally the [[differential]] $d_{\mathfrak{iso}(\mathbb{R}^{d-1,1\vert N})}$ acts on
these generators as follows:

$$
  \begin{aligned}
    d_{\mathfrak{iso}(\mathbb{R}^{d-1,1\vert N})} \; \psi^\alpha
      & \coloneqq
      \left(\tfrac{1}{4}\omega^{a b} \Gamma_{a b} \psi \right)^\alpha
      \\
      & \coloneqq
      \left(\tfrac{1}{4} (\Gamma_{a b})^\alpha{}_{\beta} \right) \omega^{a b} \wedge \psi^\beta
    \\
    d_{\mathfrak{iso}(\mathbb{R}^{d-1,1\vert N})} \; e^a
      & \coloneqq \overline{\psi} \wedge \Gamma^a \psi - \omega^a{}_b \wedge e^b
    \\
    & \coloneqq
       \left(
           C_{\alpha \alpha'} {\Gamma^a}^{\alpha'}{}_\beta
       \right)
       \psi^\alpha \wedge \psi^\beta - \omega^a{}_b \wedge e^b
    \\
  \end{aligned}
    \,,
$$


where we are shifting spacetime indicices with the Lorentz metric

$$
  (\eta_{a b}) \coloneqq diag(-1,1,1,\cdots, 1)
  \,.
$$

The canonical maps between these [[super Lie algebras]], dually between their [[Chevalley-Eilenberg algebras]], that send each generator to itself, if present, or to zero if not, constitute the [[diagram]]

$$
  \array{
    \mathbb{R}^{d-1,1\vert N}
      &\hookrightarrow&
    \mathfrak{iso}(\mathbb{R}^{d-1,1\vert N})
    \\
    && \downarrow
    \\
    && \mathfrak{so}(d-1,1)
  }
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

If we think of [[super Minkowski spacetime]] $\mathbb{R}^{d-1,1\vert N}$  as the [[supermanifold]] with

* even [[coordinates]] $\{x^a\}_{a = 0}^{d-1}$;

* odd [[coordinates]] $\{\theta_\alpha\}_{\alpha = 1}^{dim_{\mathbb{R}}(N) }$

then the algebra generators $e^a$ and $\psi^\alpha$ in def. \ref{SuperMinkowskiSpacetime}  correspond to these [[super differential forms]]:

$$
  \begin{aligned}
    e^a & = d_{dR} x^a + \underset{\text{correction term}}{\underbrace{\overline{\theta} \Gamma^a d_{dR} \theta}}
    \\
    \psi^\alpha & = d_{dR} \theta^\alpha
  \end{aligned}
$$

the **super-[[vielbein]]**.


Notice that $d_{dR} x^a$ alone fails to be a left [[invariant differential form]], in that it is not annihilated by the [[supersymmetry]] vector fields

$$
  D_\alpha
    \;\coloneqq\;
  \partial_{\theta^\alpha} - \overline{\theta}_{\alpha'} \Gamma^a{}^{\alpha'}{}_\alpha \partial_{x^a}\,.
$$

Therefore the all-important correction term  above.

=--


+-- {: .num_remark #SuperMinkowskiInvariantCocycles}
###### Remark

By def. \ref{SuperLieAlgebraCohomology} the super-[[Lie algebra cohomology]]
of [[super Minkowski spacetimes]] (def. \ref{SuperMinkowskiSpacetime}) is the cohomology of the [[differential]]

$$
  d_{CE} \, e^a = \overline{\psi} \wedge \Gamma^a \psi
  \;\;\;\,,\;\;\;
  d_{CE} \, \psi^\alpha = 0
  \,.
$$

(also called "[[tau-cohomology]]").

This may superficially look fairly trivial, but in fact it turns out to me very rich. 
Specifically we are interested in the $Spin(d-1,1)$-[[invariant]] cohomology. A $Spin$-[[invariant]]
[[cochain]] in the [[Chevalley-Eilenberg algebra]] $CE(\mathbb{R}^{d-1,1\vert M})$ is easily seen to 
be equivalently a sum of wedge products of the above generators, such that all indices are
contracted with $\Gamma$-matrices. Hence these are the monomials of the form

$$
  \mu_{p+2}
  \;\coloneqq\;
  \overline{\psi} \Gamma_{a_1 \cdots a_p} \psi
  \,.
$$

We immediately find that the differential takes these to the following expressions (using the fact that the differential is a graded [[derivation]]):


$$
  d_{CE} \mu_{p+2}
    \;=\;
  p 
  \;
  \left(
    \overline{\psi} \wedge \Gamma_{a_1 \cdots a_{p-1} b} \psi
  \right)
  \wedge 
  \left(
    \overline{\psi} \wedge \Gamma^b \psi
  \right)
  \wedge
  e^{a_1}\wedge \cdots \wedge e^{p_{p-1}}
  \,.
$$

For the these expressions to vanish, all their components have to vanish, hence all the following [[multilinear map|quadrilinear]]
expressions in the [[spinors]] have to vanish identicaly:

$$
  d_{CE} \mu_{p+2} = 0
  \;\;\;\; \Leftrightarrow
  \;\;\;\;
  \left(
    \overline{\psi} \wedge \Gamma_{a_1 \cdots a_{p-1} b} \psi
  \right)
  \wedge
  \left(
    \overline{\psi} \wedge \Gamma^b \psi
  \right)
  = 0
  \,.
$$

=--

Such relation among spinors are known as [[Fierz identities]]. These we discuss now in 
_[Fierz identities](#FierzIdentities)_.



## Fierz identities
 {#FierzIdentities}


What are called _[[Fierz identities]]_ in [[physics]] are the relations that hold between [[multilinear map|multilinear]]  expression in [[spinors]]. For example for all [[Majorana spinors]] $\psi$ in Lorentian spacetime dimension 4,5,7, 11, then the following identity holds (example \ref{TheM2andM5CocyclesAsFierzIdentities} below):

$$
  \left(\overline{\psi} \wedge \Gamma_{a b} \psi\right)
  \wedge
  \left(\overline{\psi} \wedge \Gamma^b \psi\right)

  \;=\;
  0
  \,.
$$

(Here $\overline{(-)}$ denotes the Majorana conjugate, $\Gamma_a$ are a Clifford representations, the "$\wedge$"-signs denotes symmetrization in the spinor components and summation over repeated indices is understood. The details of this are discussed [below](#BilinearFierzIdentities).)

In [D'Auria-Fr&#233;-Maina-Regge 82](#DAuriaFreMainaRegge82) it was pointed out that all Fierz identities may be understood as expressing the product operation in the [[representation ring]] of the [[spin group]] (in some given dimension): for $\{S_i\}_{i \in I}$ denoting [[isomorphism classes]] of [[irreducible representations|irreducible]] [[spin representations]], then, by definition of [[irreps]], their [[tensor product of representations]] decomposes again as a [[direct sum]] of [[irreducible representations]]

$$
  S_i \otimes S_j  = \underset{k}{\oplus} C_{i j}{}^k S_k
$$

with "[[Clebsch-Gordan coefficients]]" $C_{i j}{}^k$. These coefficients are effectively the Fierz identities.

For example for Lorentzian dimension 11 with $(\tfrac{1}{2})^5$ denoting the unique irreducible [[Majorana spinor]] representation, then one finds ([D'Auria-Fr&#233; 82b, section 3](#DAuriaFre82b)) that the symmetric part in the quadruple tensor product of this representation with itself decomposes as a direct sum of irreps as follows

$$
  \left\{
    (\tfrac{1}{2})^5
      \otimes
    (\tfrac{1}{2})^5
      \otimes
    (\tfrac{1}{2})^5
      \otimes
    (\tfrac{1}{2})^5
  \right\}_{sym}
   \;\simeq\;
  (0)^5
    \;\oplus\;
  (1)^3 (0)^2
    \;\oplus\;
  (1)^4 (0)
    \;\oplus\;
  (1)^5
    \;\oplus\;
  (2) (0)^4
    \;\oplus\;
  (2)(1)(0)^3
    \;\oplus\;
  (2)^2 (0)^3
    \;\oplus\;
  (2)^2 (1)^3
    \;\oplus\;
  (2)^5
$$

where the symbols refer to [[Young diagrams]] canonically labeling representations (details are in example \ref{11dQuadrilinearCGCoefficients} below).

The point is that the expression $ \left(\overline{\psi} \wedge \Gamma_{a b} \psi\right) \wedge \left(\overline{\psi} \wedge \Gamma^b \psi\right)$ from above is a spinor quadrilinear which transforms in the vector representation $(1)(0)^4$ (due to its one free spacetime index). But that vector representation $(1)(0)^4$ is missing from the [[direct sum]] above, meaning that the spinor quadrilinear has vanishing components in this vector representation, hence that this expression vanishes identically.

We discuss Fierz identities as identities among multispinorial elements of the [[Chevalley-Eilenberg algebra]] $CE(\mathbb{R}^{d-1,1\vert N})$ of [[super-Minkowski spacetime]] $\mathbb{R}^{d-1,1\vert N}$, regarded as the super-translation [[supersymmetry]] [[super Lie algebra]]. In this form Fierz identities encode [[cocycles]] in the [[supersymmetry]] super-[[Lie algebra cohomology]], such as those which serve as [[higher WZW terms]] characterizing [[super p-branes]]. We follow [Castellani-D'Auria-Fr&#233; 82, section II.8](#CDF).


### Bilinear Fierz identities
  {#BilinearFierzIdentities}

Given a fixed [[real spin representation]] $N$, then the
odd [[coordinates]] $\{\theta^\alpha\}_{\alpha = 1}^{dim_{\mathbb{R}}(N) }$ of the [[super Minkowski spacetime]] [[supermanifold]]
$\mathbb{R}^{d-1,1\vert N}$ span, by construction, precisely that representation space, and hence so do the
spinorial components of the [[super vielbein]] form

$$
  \psi^\alpha = \mathbf{d}\theta^\alpha
   \;\;\;
   \in \Omega^{\bullet}_{li}(\mathbb{R}^{d-1,1\vert N})
   \simeq
    CE(\mathbb{R}^{d-1,1\vert N})
  \,,
$$

since in the construction of [[super differential forms]] on $\mathbb{R}^{d-1,1\vert N}$, the de Rham operator
$\mathbf{d}$ acts on the odd coordinates just formally, by sending the generator $\theta^\alpha$ to the new generator
named $\mathbf{d} \theta^\alpha$.

Therefore we may identify the [[spin representation]] $N$ with the [[linear span]] (over $\mathbb{R}$) of these elements

$$
  N  \simeq \langle \mathbf{d}\theta^\alpha \rangle_{\alpha = 1}^{dim_{\mathbb{R}}(N) }
  \,,
$$

were the [[spin group]] acts on the elements on the right in the defining way (see at _[[geometry of physics -- supersymmetry]]_): a spinorial rotation in a plane $\omega = \{\omega^{a b}\}$ by an angle $\alpha$ acts by

$$
  R_\omega(\psi) \coloneqq \exp(\tfrac{\alpha}{4} \omega^{a b} \Gamma_{a b} ) \psi
  \,.
$$

We may build new [[spin representations]] from this one by forming multilinear expressions in the [[super vielbein]]. For example the elements in $CE(\mathbb{R}^{d-1,1\vert N})$ of the form

$$
  \begin{aligned}
    \overline{\psi} \wedge \Gamma_a \psi
    &=
    \left(C_{\alpha \alpha'} \Gamma_a{}^{\alpha'}_{\beta}\right) \, \psi^\alpha \wedge \psi^{\beta}
    \\
    & =
    \left(C_{\alpha \alpha'} \Gamma_a{}^{\alpha'}_{\beta}\right) \, \mathbf{d}\theta^\alpha \wedge \mathbf{d}\theta^\beta
  \end{aligned}
$$

span, as the spacetime index $a$ ranges in $\{0, 1, \cdots, d-1\}$, a $d$-dimensional [[real vector space]]

$$
  \left\langle
     \,\overline{\psi} \wedge \Gamma_a \psi\,
  \right\rangle_{a = 0}^{d-1}
$$

which still carries a linear [[action]] of the [[spin group]], induced from the spin action on the $\psi$-s:

$$
  \begin{aligned}
    R_\omega(\overline{\psi} \wedge \Gamma_a \psi)
    & =
    \overline{\left( \exp(\tfrac{\alpha}{4}\omega^{a b}\Gamma_{a b} ) \psi \right)}
      \wedge \Gamma_a
    \left( \exp(\tfrac{\alpha}{4}\omega^{a b}\Gamma_{a b} \psi ) \right)
    \\
    & =
    \overline{\psi} \wedge \exp(-\tfrac{\alpha}{4} \omega^{a b} \Gamma_{a b}) \Gamma_a \exp(\tfrac{\alpha}{2}\omega^{a b} \Gamma_{a b})
     \psi
    \\
    & =
    \overline{\psi}
      \wedge
      (R_\omega(\Gamma_a))
    \psi
    \end{aligned}
  \,.
$$

Of course similarly we obtain elements

$$
  \overline{\psi} \Gamma_{a_1 \cdots a_p} \psi
$$

which, if they are non-vanishing at all, span the representation

$$
  \wedge^p \mathbb{R}^d
$$

Now observe that we may say all this more abstractly as follows:

1. the elements $(\psi \wedge \overline{\psi})^{\alpha \beta}$ span the symmetrized [[tensor product of representations]]

   $$
     \{N \otimes N\}_{sym}
       \;\simeq\;
     \langle
       \,  (\psi \wedge \overline{\psi})^\alpha{}_\beta \,
     \rangle_{\alpha,\beta = 1}^{dim_{\mathbb{R}}(N)}
   $$

1. for given $p \in \mathbb{N}$, then the elements of the form $\overline{\psi} \wedge \Gamma_{a_1 \cdots a_p} \psi$ form a [[subrepresentation]] thereof, equivalent to the vector representation $\wedge^p\mathbb{R}^{d}$

1. hence there is a [[direct sum]] decomposition

   $$
     \left\{N \otimes N\right\}_{sym}
       \;\simeq\;
      \underset{p \in \mathbb{N}}{\bigoplus}
      c_p \left(\wedge^p \mathbb{R}^d\right)
   $$

   in the [[category of representations]] of the [[spin group]], which expresses the (symmetrized) [[tensor product of representations]] of the [[Majorana spinor]] representation as a [[direct sum]] of skew-symmetrized tensor products of the vector representation.

Indeed this direct sum decomposition is exhaustive:

+-- {: .num_prop #BilinearFierzDecomposition}
###### Proposition

For $d \in \mathbb{N}$ and $N$ a [[Majorana spinor]] representation of $Spin(d-1,1)$, then the following identity holds:

$$
  (\psi \wedge \overline{\psi})^\alpha{}_\beta
   \;=\;
  \tfrac{1}{dim_{\mathbb{R}}(N)}
  \left(
     \left(
       \overline{\psi}\psi
     \right)
     +
     \left(
       \overline{\psi} \Gamma_a \psi
     \right)
     (\Gamma^a)^\alpha{}_\beta
     +
     \tfrac{1}{2!}
     \left(
       \overline{\psi} \Gamma_{a_1 a_2} \psi
     \right)
     (\Gamma^{a_1 a_2})^\alpha{}_\beta
      +
     \cdots
  \right)
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the discussion there, the [[Majorana spinor]] representation is a real sub-representation of a complex _Dirac representation_ $\mathbb{C}^{(2^\nu)}$. The latter has the special property that

1. the [[Clifford algebra]] contains the full [[matrix algebra]];

1. for $p \geq 1$ the Clifford elements $\Gamma_{a_1 \cdots a_p}$ have vanishing [[trace]].

The first point implies that there exists coefficients $X^{a_1 \cdots a_p} \in \mathbb{C}$ for $p \in \mathbb{N}$ such that

$$
  \psi \wedge \overline{\psi}
    =
  \tfrac{1}{dim_{\mathbb{R}}(N)}
  \left(
    X
    +
    X^a \Gamma_a
    +
    X^{a b} \Gamma_{a b}
    +
    \cdots
  \right)
  \,.
$$

The second condition then implies that multiplying this expression with $\Gamma^{a_1 \cdots a_p}$ and taking the trace projects out the coefficient $X^{a_1 \cdots a_p}$:

$$
  \begin{aligned}
    X^{a_1 \cdots a_p}
      & =
    \frac{1}{p! dim_{\mathbb{R}}(N)}
    tr_N
    \left(
      \left(
        X
        +
        X^a \Gamma_a
        +
        X^{a b} \Gamma_{a b}
        +
        \cdots
      \right)
      \Gamma^{a_1 \cdots a_p}
   \right)
   \\
   & =
   \tfrac{1}{p!}
   tr_N
   \left(
     \psi \wedge \overline{\psi} \, \Gamma^{a_1 \cdots a_p}
   \right)
   \\
   & =
   \tfrac{1}{p!}
   \left(
     \overline \psi \wedge \Gamma^{a_1 \cdots a_p} \psi
   \right)
  \end{aligned}
  \,.
$$

Notice that it is the last step, identifying the trace over $\psi \wedge \overline{\psi} \Gamma^{a_1 \cdots a_p}$ with the $\psi$-$\psi$ component of the matrix $\Gamma^{a_1 \cdots a_p}$, where we use the _symmetrization_ of the spinor tensor product, namely the identity $\psi^\alpha \wedge \overline{\psi}_\beta = \overline{\psi}_\beta \wedge \psi^\alpha$.

=--


Some of the coefficients in prop. \ref{BilinearFierzDecomposition} may vanish identically. These are the _bilinear Fierz identities_, of the form

$$
  \overline{\psi} \Gamma_{a_1 \cdots a_p} \psi = 0
  \,.
$$

+-- {: .num_example}
###### Example

Let $d = 11$. Write $\mathbf{32}$ or $(\tfrac{1}{2})^5$ for the [[Majorana spinor]] representation of $Spin(d-1,1)$. Then

$$
  \left\{
    (\tfrac{1}{2})^5
      \otimes
    (\tfrac{1}{2})^5
  \right\}_{sym}
     \;\simeq\;
  \underset{\simeq \mathbb{R}^d}{\underbrace{(1)^1 (0)^4}}
    \;\oplus\;
  \underset{\simeq \wedge^2 \mathbb{R}^d}{\underbrace{(1)^2 (0)^3}}
    \;\oplus\;
  \underset{\wedge^5 \mathbb{R}^d}{\underbrace{(1)^5}}
  \,.
$$

=--

([D'Auria-Fr&#233; 82b (3.1)](#DAuriaFre82b))


+-- {: .proof}
###### Proof

Since we know from prop. \ref{BilinearFierzDecomposition} that the right hand side has to be some direct sum of representations of the form $\wedge^p \mathbb{R}^d$, it is sufficient to check that there is only one choice of sum such that [[dimensions]] match on both sides of the equation.

Now the dimension of $\{N \otimes N\}_{sym}$ is that of the space of symmetric $32 \times 32$ matrices:

$$
  dim_{\mathbb{R}}
  \left(
     \{\mathbf{32} \otimes \mathbf{32}\}_{sym}
  \right)
   \;=\;
  \frac{1}{2}
  \left(
    32 \times 33
  \right)
   =
  528
$$

while the dimension of $\wedge^p \mathbb{R}^d$ is the [[binomial coefficient]]

$$
  dim_{\mathbb{R}}(\wedge^p \mathbb{R}^d)
   \;=\;
  \left(
    11 \atop p
  \right)
  \,.
$$


Hence the claim follows from the fact that

$$
  \begin{aligned}
    582
     & = 11 + 55 + 462
    \\
    & =
  \left(11 \atop 1\right)
   +
  \left(11 \atop 2\right)
   +
  \left(11 \atop 5\right)
  \end{aligned}
  \,.
$$

=--









### Quadrilinear Fierz identities
  {#QuadraticFierzIdentities}


Now we consider the [[direct sum]] decomposition of the [[tensor product of representations]] of _four_ copies of a [[spin representation]]. This yields the quadrilinear Fierz identities.

+-- {: .num_example #11dQuadrilinearCGCoefficients}
###### Example

The group $Spin(10,1)$ has [[rank of a Lie group|rank]] 5, and hene its [[irreducible representation|irreducible]] vector representations are labeled by [[Young diagrams]] consisting of five rows. For instance

$$
  (2)^2 (1)^2 (0)
$$

denotes the representation whose elements may be identified with tensors of the form

$$
  X_{\array{ a_1 & a_2 \\ a_3 & a_4 \\ a_5 }}
$$

which are

1. skew-symmetric in indices in the same column;

1. symmetric and trace-less in indices in the same row.

Write again $(\tfrac{1}{2})^5$ for the [[Majorana spinor]] representation. Then the following identity holds in the [[representation ring]]:


$$
  \left\{
    (\tfrac{1}{2})^5
      \otimes
    (\tfrac{1}{2})^5
      \otimes
    (\tfrac{1}{2})^5
      \otimes
    (\tfrac{1}{2})^5
  \right\}_{sym}
   \;\simeq\;
  \left.
    \array{
    (0)^5
    \\
    \oplus
    \\
    (2) (0)^4
    \\
    \oplus
    \\
    (1)^3 (0)^2 \oplus  (2)(1)(0)^3
    \\
    \oplus
    \\
    (1)^4 (0) \oplus (2)^2 (0)^3
    \\
    \oplus
     \\
    (1)^5
     \\
     \oplus
     \\
    (2)^2 (1)^3
    \\
    \oplus
    \\
    (2)^5
   }
  \right.
$$

=--

([D'Auria-Fr&#233; 82b (3.3) ](#DAuriaFre82b))

+-- {: .proof}
###### Proof

As before, this is supposed to follow already by matching total dimensions on both sides


$$
  \frac{32 \times 33 \times 34 \times 35}{4 \times 3 \times 2}
   \;=\;
  \left.
    \array{
    1
    \\
    +
    \\
    65
    \\
    +
    \\
    165 +  429
    \\
    +
    \\
    330 + 1144
    \\
    +
     \\
    462
     \\
     +
     \\
    17160
    \\
    +
    \\
    32604
   }
  \right.
$$

=--

More in detail we have the following decompositions, in the notation from [above](#QuadraticFierzIdentities).

\[
  \label{Fierz11dA}
  \left(\overline{\psi} \wedge \Gamma_{a_1} \psi\right)
   \wedge
  \left( \overline{\psi} \wedge \Gamma_{a_2} \psi \right)
   \;=\;
  X^{(\mathbf{65})}_{\array{a_1 \\ a_2}}
   +
  \frac{1}{11} \delta_{\array{a_1 a_2}}X^{(\mathbf{1})}
\]

Here for instance the symbol $X^{(\mathbf{65})}_{\array{a_1 \\ a_2}}$ denotes the projection of the term on the left into the direct summand given by the [[representation]] $(2)(0)^4$ of dimension $65$. Similarly:

\[
  \label{Fierz11dB}
  \left(\overline{\psi} \wedge \Gamma_{a_1 a_2} \psi\right)
    \wedge
  \left(\overline{\psi} \wedge \Gamma_{a_3}\right)
    \;=\;
  X^{(\mathbf{429})}_{\array{ a_1 & a_2 \\ a_3}}
   +
  X^{(\mathbf{165})}_{\array{a_1 a_2 a_3}}
\]

\[
  \label{Fierz11dC}
  \left(
    \overline{\psi}\Gamma_{a_1 a_2} \psi
  \right)
  \left(
    \overline{\psi} \Gamma_{a_3 a_4}
  \right)
   \;=\;
  X^{(\mathbf{1144})}_{\array{a_1 a_2 \\ a_3 a_4}}
   +
  X^{(\mathbf{330})}_{\array{a_1 a_2 a_3 a_4}}
   +
  \tfrac{4}{9}\delta_{\array{ [a_1 \\ [a_3} } X^{(\mathbf{65})}_{\array{a_2] \\ a_4] } }
  -
  \tfrac{2}{11} \delta_{\array{a_1 & a_2 \\ a_3 & a_4}} X^{(\mathbf{1})}
\]

\[
  \label{Fierz11dD}
  \left(
    \overline{\psi}
      \wedge
      \Gamma_{a_1 \cdots a_5}
    \psi
  \right)
  \wedge
  \left(
    \overline{\psi}
      \wedge
    \Gamma_{a_6}
   \psi
  \right)
  \;=\;
  \epsilon_{a_1 \cdots a_6}{}^{b_1 \cdots b_5}
  X^{(\mathbf{462})}_{b_1 \cdots b_5}
  +
  X^{(\mathbf{4290})}_{\array{a_1 & \cdots & a_5 \\ a_6}}
  +
  \frac{15}{7}
  \delta_{a_6 [ a_1} X^{(\mathbf{330})}_{\array{a_2 & \cdots & a_5}}
\]

and some more.

([D'Auria-Fr&#233; 82b table 2 ](#DAuriaFre82b))



As a corollary:

+-- {: .num_example #TheM2andM5CocyclesAsFierzIdentities}
###### Example

For $d = 11$ then

1. the following Fierz identity holds:

   $$
     \left(
       \overline{\psi} \wedge \Gamma_{a b} \psi
     \right)
     \wedge
     \left(
        \overline{\psi} \wedge \Gamma^b \psi
     \right)
     \;= \; 0
     \,.
   $$

   (we will see below that this is the cocycle condition for the [[higher WZW term]] of the [[M2-brane]] ([Bergshoeff-Sezgin-Townsend 87](#BergshoeffSezginTownsend87)), [AETW 87](#AETW87))

1. the following Fierz identity holds:

   $$
     \left(
       \overline{\psi}
         \wedge
         \Gamma_{a_1 \cdots a_4 b}
       \psi
     \right)
     \wedge
     \left(
       \overline{\psi}
        \wedge
        \Gamma^{b}
        \psi
     \right)
     \;=\;
     3
     \left(
     \overline{\psi}
        \Gamma_{[a_1 a_2}
     \psi
     \right)
     \wedge
     \left(
       \overline{\psi}
          \Gamma_{a_3 a_4]}
       \psi
     \right)
   $$

   (we will see below that this is the cocycle condition for the [[higher WZW term]] of the [[M5-brane]] ([BLNPST 97](#BLNPST97), [FSS 15](#FSS15))).

=--

This is due to ([D'Auria-Fr&#233; 82b (3.13) and (3.28) ](#DAuriaFre82b))

+-- {: .proof}
###### Proof

The first identity is the result of equation (eq:Fierz11dB) after tracing over the indices $a_2$ and $a_3$. Under this trace both summands on the right of (eq:Fierz11dB) vanish: $X^{(\mathbf{429})}_{\array{ a_1 & a_2 \\ a_3}}$ because it is trace-free in indices in a column, and $X^{(\mathbf{165})}_{\array{a_1 a_2 a_3}}$ because it is skew-symmetric in all indices.

The second identity follows from taking the trace over the indices $a_5 and a_6$ in (eq:Fierz11dD) and of skew-symmetrizing over all indices in (eq:Fierz11dC). By the symmetry properties of the tensors on the right of both equations, in both cases all tensors vanish except, in both cases, the contribution proportional to $X^{(\mathbf{330})}_{[a_1 \cdots a_3]}$, which both identities share. So it only remains to check that the proportionality factor is 3, as claimed. By writing out the skew-symmetrization in the last term in (eq:Fierz11dD) one finds:

{#ComputationOfRelativeCoefficientInM5Cocycle}
$$
  \begin{aligned}
    \frac{15}{7}
    \delta^{a_1 a_6}
    \delta_{a_6 [a_1}
    X^{(\mathbf{330})}_{a_2 \cdots a_5]}
    & =
    \frac{15}{7}
    \delta^{a_1}{}_{[a_1} X^{(\mathbf{330})}_{a_2 \cdots a_5]}
    \\
    & =
    \frac{15}{7}
    \frac{1}{5!}
    \sum_{ \left\{\sigma \atop { {\text{permutation of}} \atop {\{1,\cdots , 5\}} } \right\}}
    (-1)^{\vert \sigma\vert }
    \delta^{a_1}{}_{a_{\sigma(1)}}
    X_{a_{\sigma(2)} \cdots a_{(\sigma(5))}}
    \\
    & =
    \frac{15}{7}
    \frac{1}{5!}
    \sum_{\left\{\sigma \atop { {\text{permutation of}} \atop {\{1,\cdots , 4\}} } \right\} }
    (-1)^{\vert \sigma\vert }
    \left(
      \underset{= 11}{\underbrace{\delta^{a_1}_{a_1}}}
      X^{(\mathbf{330})}_{a_{\sigma(1)}\cdots a_{\sigma(4)}}
      -
      4
      \delta^{a_1}{}_{a_{\sigma(1)}}
      X_{a_1 a_{\sigma(2)} \cdots a_{\sigma(4)}}
    \right)
   \\
   & =
    \frac{15}{7}
    (11-4)
    \frac{1}{5}
    \;
    \underset{X^{(\mathbf{330})}_{a_1\cdots a_4}}{
    \underbrace{
    \frac{1}{4!}
    \sum_{ \left\{ \sigma \atop { {\text{permutation of}} \atop {\{1,\cdots , 4\}} } \right\} }
    (-1)^{\vert \sigma\vert}
    X^{(\mathbf{330})}_{a_{\sigma(1)}\cdots a_{\sigma(4)}}
    }
    }
    \\
    & =
    3 \; X^{(\mathbf{330})}_{a_{\sigma(1)} \cdots a_{\sigma(4)}}
  \end{aligned}
$$

where we used that $X^{(\mathbf{330})}_{a_1 \cdots a_4}$ is already skew-symmetric in all indices.

=--



## Branes


Below we will obtain all [[super p-branes]] by consecutive invariant higher [[super Lie n-algebra]] extensions of
[[super Minkowski spacetime]]. To put this in perspective,
recall from the end of _[[geometry of physics -- supersymmetry]]_ how
the relevant [[super Minkowski spacetimes]] in dimensions 3,4,6,10 and 11 themselves emerged from the [[superpoint]] in a progression of
ordinary invariant [[central extensions]] of [[super Lie algebras]]:

### Super-Minkowski spacetimes

+-- {: .num_prop}
###### Proposition

Consider the [[superpoint]]

$$
  \;\;\;\;\;\; \mathbb{R}^{0\vert 1}
$$

regarded as an abelian [[super Lie algebra]] (def. \ref{SuperLieAlgebraAsLieAlgebraInternalToSuperVectorSpaces}, prop. \ref{SuperLieAlgebraTraditional}). Its maximal [[central extension]] is the $N = 1$ super-[[worldline]] of the [[superparticle]]:

$$
  \array{
    \mathbb{R}^{0,1\vert \mathbf{1}}
    \\
    \downarrow
    \\
    \mathbb{R}^{0\vert 1}
  }
  \,.
$$

* whose even part is spanned by one generator $H$

* whose odd part is spanned by one generator $Q$

* the only non-trivial bracket is

  $$
    \{Q, Q\} = H
  $$

Then consider the [[superpoint]]

$$
  \;\;\;\;\;\; \mathbb{R}^{0\vert 2}
  \,.
$$


Its maximal [[central extension]] is

the $d = 3$, $N = 1$ [[super Minkowski spacetime]]

$$
  \array{
    \mathbb{R}^{2,1\vert \mathbf{2}}
    \\
    \downarrow
    \\
    \mathbb{R}^{0\vert 2}
  }
  \,.
$$

* whose even part is $\mathbb{R}^3$, spanned by generators $P_0, P_1, P_2$

* whose odd part is $\mathbb{R}^2$, regarded as

  the [[Majorana spinor]] representation $\mathbf{2}$

  of $Spin(2,1) \simeq SL(2,\mathbb{R})$

* the only non-trivial bracket is the spinor bilinear pairing

  $$
    \{Q_\alpha, Q'_\beta\}
    =
     C_{\alpha \alpha'} \Gamma_a{}^{\alpha'}{}_\beta
    \,P^a
  $$

where $C_{\alpha \beta}$ is the [[charge conjugation matrix]].

=--

This phenomenon continues:


+-- {: .num_theorem}
###### Theorem
**([J. Huerta](#MTheoryFromTheSuperpoint))

The [[diagram]] of [[super Lie algebras]] shown on the right

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/schreiber/files/SpacetimeExtensions.png" width="250">
</div>

is obtained by consecutively forming maximal central extensions invariant with respect to the maximal subgroup of automorphisms for which there are invariant cocycles at all. Here $\mathbb{R}^{d-1,1\vert \mathbf{N}}$ is the $d$, $\mathbf{N}$ super-translation [[supersymmetry]] algebra. And these subgroups are the [[spin group]] covers $Spin(d-1,1)$ of the [[Lorentz groups]] $O(d-1,1)$.

=--


+-- {: .num_remark}
###### Remark

That every [[super Minkowski spacetime]] is _some_ [[central extension]] of some [[superpoint]]  is elementary.
This was highlighted in ([Chryssomalakos-Azc&#225;rraga-Izquierdo-Bueno 99,
2.1](https://ncatlab.org/nlab/show/Green-Schwarz+action+functional#CAIB99)).
But most central extensions of superpoints
are nothing like super-Minkowksi spacetimes.
The point of the above proposition
is to restrict attention to _iterated invariant_ central extensions
and to find that these single out the super-Minkowski spacetimes.

=--


**Conclusion:**

Just from studying iterated invariant [[central extensions]]

of [[super Lie algebras]],

starting with the [[superpoint]],

we  (re-)discover

1. [[pseudo-Riemannian geometry|Lorentzian geometry]],

1. [[spin geometry]].

1. [[super spacetimes]].




$\,$

There are no further invariant 2-cocycles on <img src="https://ncatlab.org/schreiber/files/10dSpacetimes.png" width="250">

But there is an invariant 3-cocycle.

$\,$

There are no further invariant 2-cocycles on $\mathbb{R}^{10,1\vert \mathbf{32}}$

But there is an invariant 4-cocycle.

$\,$

So:

_What are higher super Lie algebra cocycles?_

_And what kind of extensions do they classify?_

$\,$

Quick answer:

_Higher cocycles are closed elements in a [[Chevalley-Eilenberg algebra]]._

_They classify [[super Lie-∞ algebra]] [[L-∞ algebra cohomology|extensions]]._

$\,$

This we explain now.



$\,$


+-- {: .num_example #D0Cocycle}
###### Example

$\,$

The 2-cocycle that classifies the extension

$$
  \array{
    \mathbb{R}^{10,1\vert \mathbf{32}} && 11d, N = 1
    \\
    \downarrow
    \\
    \mathbb{R}^{9,1\vert \mathbf{16}+ \overline{\mathbf{16}}} && 10d, \text{type IIA}
  }
$$

is

$$
  i \, \overline{\psi} \wedge \Gamma_{11} \psi
  \;\in\;
  CE(\mathbb{R}^{9,1\vert \mathbf{16}+ \overline{\mathbf{16}}})
$$

Regarded as a 2-form on $\mathbb{R}^{9,1\vert \mathbf{32}}$,

this is the [[curvature]] of the [[WZW-term]]

in the [[Green-Schwarz sigma-model]] for the [[D0-brane]].

See below.

=--
























### The super-string and the super-membrane
 {#TheSuperStringAndTheSuperMembrane}



+-- {: .num_prop}
###### Proposition
**([Ach&#250;carro-Evans-Townsend-Wiltshire 87](https://ncatlab.org/nlab/show/Green-Schwarz+action+functional#AETW87), [Brandt 12-13](https://ncatlab.org/nlab/show/Green-Schwarz+action+functional#Brandt12-13))**

The maximal invariant 3-cocycle on 10d [[super Minkowski spacetime]] (according to remark \ref{SuperMinkowskiInvariantCocycles}) is

$$
  \mu_{F1} = \left(\overline{\psi} \wedge \Gamma_a \psi\right) \wedge e^a
$$

This is the [[WZW term]] for the [[Green-Schwarz superstring]] ([Green-Schwarz 84](https://ncatlab.org/nlab/show/Green-Schwarz+action+functional#GreenSchwarz84)).

The maximal invariant 4-cocycle on [[super Minkowski spacetime]] is

$$
  \mu_{M2} = i \left(\overline{\psi} \wedge \Gamma_{a b} \psi \right) \wedge e^a \wedge e^b
$$

This is the [[higher WZW term]] for the [[supermembrane]]
([Bergshoeff-Sezgin-Townsend 87](https://ncatlab.org/nlab/show/M2-brane#BergshoeffSezginTownsend87)).

This classification is also known as

the **old [[brane scan]]**.

=--

| $\stackrel{d}{=}$ |  $p =$ | 1 | 2 | 3 | 4 | 5 | 6 | 7 |  8 |  9 |
|--|--------|---|---|---|---|---|---|---|----|----|
| 11 | |  |  [[M2-brane|M2]] |  |   |  |   |   |   |   |
| 10 |  | [[F1-brane|F1]]   |   |  |   | [[NS5-brane|NS5]] |   |   |   |   |
| 9 | |   |   |  | $\ast$  |  |   |   |   |   |
| 8 | |   |   | $\ast$ |   |  |   |   |   |   |
| 7 | |   | $\ast$  |  |   |  |   |   |   |   |
| 6 | |  $\ast$  |  | [[3-brane in 6d|S3]] |   |  |   |   |   |   |
| 5 | |  | $\ast$   | |   |  |   |   |   |   |
| 4 | | $\ast$  | [[super 2-brane in 4d|M2]]$_{cmp}$   | |   |  |   |   |   |   |
| 3 | | [[super 1-brane in 3d|F1]]$_{cmp}$  |  | |   |  |   |   |   |   |



$\,$

Here "**[[higher WZW term]]**" means the following:

$\,$

Regard $\mu_{F1} = \left(\overline{\psi} \wedge \Gamma_a \psi\right) \wedge e^a$

as a left [[invariant differential form]]

on [[super-Minkowski spacetime]].

Choose any differential form potential $B_{F1}$

i.e. such that

$$
  d_{dR} B_{F1} = \left(\overline{\psi} \wedge \Gamma_a \psi\right) \wedge e^a
  \,.
$$

(This $B_{F1}$ will _not be left-invariant_.)

Then the [[Green-Schwarz action functional]] for the [[superstring]]

is the function on the space of [[sigma-model]] [[field (physics)|fields]]

$$
  \phi \;\colon\; \underset{\text{worldsheet}}{\underbrace{\Sigma_2}}
    \longrightarrow
    \underset{\text{super-spacetime}}{\underbrace{\mathbb{R}^{9,1\vert \mathbf{N}}}}
$$

(morphisms of [[supermanifolds]])

given by

$$
  \phi
    \;\mapsto\;
  \underset{\text{kinetic action}}{
  \underbrace{
  \int_{\Sigma_2}
  \sqrt{
    -det(\partial_{\sigma^i} e^a(\phi) \partial_{\sigma_j} e_b(\phi))
  }
  \,
  d \sigma^1 \wedge d\sigma^2
  }}
  +
  \underset{\text{WZW term}}{
  \underbrace{
    \int_{\Sigma^2} \phi^\ast B_{F1}
  }
  }
  \,.
$$

The first term is the [[Nambu-Goto action]]

the second is a [[WZW term]].

$\,$

Originally [Green-Schwarz 84](https://ncatlab.org/nlab/show/Green-Schwarz+action+functional#GreenSchwarz84) introduced $B_{F1}$

to ensure an additional fermionic symmetry: "[[kappa-symmetry]]".

Notice that $B_{F1}$ looks somewhat complicated

and is not unique.

That it is simply a [[WZW-term]]

for the [[supersymmetry]] [[supergroup]]

$$
  \mathbb{R}^{9,1\vert \mathbf{N}}
   =
  Iso(\mathbb{R}^{9,1\vert \mathbf{N}}) / Spin(9,1)
$$

was observed in [Henneaux-Mezincescu 85](https://ncatlab.org/nlab/source/Green-Schwarz+action+functional#HenneauxMezincescu85).

$\,$

Similarly,

choose any differential form potential $C_{M2}$ such that

$$
  d_{dR} C_{M2} = \left(\overline{\psi} \wedge \Gamma_{a b} \psi\right) \wedge e^a \wedge e^b
  \,.
$$

(This $C_{M2}$ will _not be left-invariant_.)

Then the [[Green-Schwarz action functional|Green-Schwarz type action functional]]

for the [[supermembrane]] is the function on [[sigma-model]] [[field (physics)|fields]]

$$
  \phi \;\colon\; \underset{\text{worldvolume}}{\underbrace{\Sigma_3}} \longrightarrow \mathbb{R}^{10,1\vert \mathbf{32}}
$$

given by

$$
  \phi
    \;\mapsto\;
  \underset{\text{kinetic action}}{
  \underbrace{
  \int_{\Sigma_2}
  \sqrt{
    -det(\partial_{\sigma^i} e^a(\phi)\partial_{\sigma_j} e_b(\phi))
  }
  \,
  d \sigma^1 \wedge d\sigma^2 \wedge d\sigma^3
  }}
  +
  \underset{\text{WZW term}}{
  \underbrace{
    \int_{\Sigma^3} \phi^\ast C_{M2}
  }
  }
  \,.
$$

On the right this is

the [[higher WZW term]].

$\,$

Now we discuss that higher cocycles classify higher extensions:

$\,$

First observe that

+-- {: .num_prop }
###### Proposition

[[homomorphisms|Homomorphisms]] of [[super Lie algebras]]

$$
  \mathfrak{g}_1 \longrightarrow \mathfrak{g}_2
$$

are in [[natural bijection]] with the [[homomorphisms]] of [[dg-algebras]]

between their [[Chevalley-Eilenberg algebra]], going the opposite direction:

$$
  CE(\mathfrak{g}_1) \longleftarrow CE(\mathfrak{g}_2)
  \,.
$$

=--

This means that we may _identify_ [[super Lie algebras]] with their CE-algebras.

In the terminology of [[category theory]]: the [[functor]]

$$
  CE
   \;\colon\;
  s LieAlg_{\mathbb{R}}
    \hookrightarrow
  dgAlg_{\mathbb{R}}^{op}
$$

given by

$$
  \mathfrak{g} \mapsto CE(\mathfrak{g}) = (\wedge^\bullet \mathfrak{g}^\ast, [-,-]^\ast)
$$

is [[fully faithful functor|fully faithful]].

$\,$

Therefore is natural to make the following definition.

$\,$















### Extended super Minkowski spacetime
 {#ExtendedSuperMinkowskiSpacetime}


This way we may finally continue the progression of invariant central extensions to higher central extensions:


$\,$

+-- {: .num_defn }
###### Definition

$\,$

Name the [[homotopy fibers]] of the cocycles

which are the [[higher WZW terms]]

of the [[superstring]] and the [[supermembrane]]

as follows


$$
  \array{
    \mathfrak{m}2\mathfrak{brane}
    \\
    {}^{\mathllap{hofib}(\mu_{M2})}\downarrow
    \\
    \mathbb{R}^{10,1\vert \mathbf{32}}
    &\underset{\mu_{M2}}{\longrightarrow}&
    B^3 \mathbb{R}
  }
$$


$\,$

$\,$

$$
  \array{
    \mathfrak{string}_{IIB}
    \\
    {}^{\mathllap{hofib}(\mu_{F1}^B)}\downarrow
    \\
    \mathbb{R}^{9,1\vert \mathbf{16}+ \mathbf{16}}
    &\underset{\mu_{F1}^B}{\longrightarrow}&
    B^2 \mathbb{R}
  }
  \;\;\;\;\;\;\;\;\;\;\;\;\;\;\;
  \array{
    \mathfrak{string}_{het}
    \\
    {}^{\mathllap{hofib}(\mu_{F1}^{het})}\downarrow
    \\
    \mathbb{R}^{9,1\vert \mathbf{16}}
    &\underset{\mu_{F1}^{het}}{\longrightarrow}&
    B^2 \mathbb{R}
  }
  \;\;\;\;\;\;\;\;\;\;\;\;\;\;\;
  \array{
    \mathfrak{string}_{IIA}
    \\
    {}^{\mathllap{hofib}(\mu_{F1}^A)}\downarrow
    \\
    \mathbb{R}^{9,1\vert \mathbf{16}+ \overline{\mathbf{16}}}
    &\underset{\mu_{F1}^A}{\longrightarrow}&
    B^2 \mathbb{R}
  }
$$

$\,$

The super Lie 2-algebra $\mathfrak{string}_{het}$ is given by

$$
  CE(\mathfrak{string}_{het})
  =
  \left\{
    \array{
      d e^a = \overline{\psi} \Gamma^a \psi,
      \; d \psi^\alpha = 0
      \\
      d b_2 = \mu_{F1}^{het} = (\overline{\psi} \wedge \Gamma_a \psi)\wedge e^a
    }
  \right\}
$$

This is a super-version of the _[[string Lie 2-algebra]]_ ([Baez-Crans-Schreiber-Stevenson 05](#BCSS05)

which controls [[Green-Schwarz anomaly cancellation]] ([Sati-Schreiber-Stasheff 12](#SatiSchreiberStasheff12))

and the topology of the [[supergravity C-field]] ([Fiorenza-Sati-Schreiber 12a](#FiorenzaSatiSchreiber12a), [12b](#FiorenzaSatiSchreiber12b)).

$\,$

The [[supergravity Lie 3-algebra|membrane super Lie 3-algebra]] $\mathfrak{m}2\mathfrak{brane}$ is given by

$$
  CE(\mathfrak{m}2\mathfrak{brane})
  =
  \left\{
    \array{
      d e^a = \overline{\psi} \wedge \Gamma^a \psi, \; d \psi^\alpha = 0
      \\
      d b_3 = i (\overline{\psi} \wedge \Gamma_{a b} \psi) \wedge e^a \wedge e^b
    }
  \right\}
$$

This dg-algebra was first considered  in [D'Auria-Fr&#233; 82 (3.15)](https://ncatlab.org/nlab/show/D'Auria-Fre+formulation+of+supergravity#DAuriaFre)

as a tool for constructing [[11-dimensional supergravity]].

For exposition from the point of view of [[Lie 3-algebras]] see also [Baez-Huerta 10](https://arxiv.org/abs/1003.3436).

=--

$\,$

Hence the progression

of maximal invariant extensions of the superpoint

continues as a [[diagram]]

of [[super L-∞ algebras]] like so:

$\,$

<img src="https://ncatlab.org/schreiber/files/FirstBraneExtensions.png" width="450">

$\,$

(While every extension displayed is a maximal invariant higher central extension, not all invariant higher central extensions are displayed.
For instance there are string and membrane GS-WZW-terms / cocycles also on the lower dimensional super-Minkowski spacetimes ("non-critical"), e.g. the [[super 1-brane in 3d]] and the [[super 2-brane in 4d]].)

$\,$

The "old [[brane scan]]" ran into a conundrum:

Given that  [[superstrings]] and [[supermembranes]]

are nicely classified by [[super Lie algebra]] [[Lie algebra cohomology|cohomology]]

why do the other [[super p-branes]] not show up similarly?

Where are the [[D-branes]] and the [[M5-brane]]?

$\,$

But now we see that we should look for

further higher cocycles

not on [[super Lie algebras]]

but on [[super L-∞ algebras]].

$\,$


+-- {: .num_prop}
###### Proposition
**([Chryssomalakos-Azc&#225;rraga-Izquierdo-Bueno 99](https://ncatlab.org/nlab/show/Green-Schwarz+action+functional#CAIB99), [Sakaguchi 99](https://ncatlab.org/nlab/show/Green-Schwarz+action+functional#Sakaguchi00), [Fiorenza-Sati-Schreiber 13](#FSS13))**

The [[higher WZW terms]] for the [[D-branes]]

are invariant super $L_\infty$-cocycles

on the higher [[extended super Minkowski spacetimes]] from above

$$
  \mu_{D p}
  \;\colon\;
  \mathfrak{string}
    \stackrel{\phantom{AAAAAAAA}}{\longrightarrow}
  B^{p+1}\mathbb{R}
  \,.
$$

Similarly,

the [[higher WZW term]] for the [[M5-brane]]

is an invariant super $L_\infty$ 7-cocycle

of the form

$$
  \mu_{M5}
    \;\colon\;
  \mathfrak{m}2\mathfrak{brane}
    \stackrel{\phantom{AAAAAAAAA}}{\longrightarrow}
  B^6 \mathbb{R}
  \,.
$$

=--

$\,$

By the above, these cocycles classify

further higher super $L_\infty$-algebra extensions

$$
  \array{
    \mathfrak{d}p\mathfrak{brane}
    \\
    {}^{\mathllap{hofib(\mu_{D p})}}\downarrow
    \\
   \mathfrak{string}_{IIA/B}
     &\underset{\mu_{D p}}{\longrightarrow}&
   B^{p+1}\mathbb{R}
  }
  \;\;\;\;\;\;\;\;\,\;\;\;\;\;\;\;\;\;\;\;
  \array{
    \mathfrak{m}5\mathfrak{brane}
    \\
    {}^{\mathllap{hofib(\mu_{M5})}}\downarrow
    \\
    \mathfrak{m}2\mathfrak{brane}
      &\underset{\mu_{M5}}{\longrightarrow}&
    B^6 \mathbb{R}
  }
$$

$\,$

Notice that all these are higher cocycles

except for that of the [[D0-brane]], which is just a 2-cocycle.

The ordinary central extension that this classifies

is just that which grows the 11th M-theory dimension by the above example \ref{D0Cocycle}.

$$
  \array{
    \mathbb{R}^{10,1\vert \mathbf{32}}
    \\
    {}^{\mathllap{hofib(\mu_{D0})}} \downarrow
    \\
    \mathbb{R}^{9,1\vert \mathbf{16} + \overline{\mathbf{16}}}
       &\underset{\mu_{D0} =  i \, \overline{\psi} \Gamma_{11} \psi }{\longrightarrow}&
    B \mathbb{R}
  }
$$

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/schreiber/files/PolchinskiD0Condensation.png" width="350">
</div>
This may be thought of

as a super $L_\infty$-theoretic incarnation

of D0-brane [[condensate|condensation]]

([Polchinski 99, around p. 8](https://ncatlab.org/nlab/show/D0-brane#Polchinski99)).


$\,$

In **conclusion**:

by forming

iterated (maximal) invariant higher central super $L_\infty$-extensions

of the superpoint,

we obtain the following "[[schreiber:brane bouquet]]"

$\,$

<img src="https://ncatlab.org/schreiber/files/SecondBraneExtensions.png" width="550">

$\,$

Each object in this [[diagram]] of [[super L-∞ algebras]]

is a [[super spacetime]] or [[super p-brane]] of [[string theory]] / [[M-theory]].

$\,$

Moreover, this diagram knows the brane intersection laws:

there is a morphism $p_2\mathfrak{brane} \longrightarrow p_1 \mathfrak{brane}$

precisely if the given species of $p_1$-branes may end on the given species of $p_2$-branes

(more discussion of this is in [Fiorenza-Sati-Schreiber 13, section 3](#FSS13)).

$\,$


> Perhaps we need to understand the nature of time itself better. $[...]$ One natural way to approach that question would be to understand in what sense time itself is an emergent concept, and one natural way to make sense of such a notion is to understand how pseudo-Riemannian geometry can emerge from more fundamental and abstract notions such as categories of branes. ([[Greg Moore|G. Moore]], p.41 of "[[Physical Mathematics and the Future]]", talk at [Strings 2014](http://physics.princeton.edu/strings2014/))


$\,$

But how are we to think of the [[extended super Minkowski spacetimes]] geometrically?

This is clarified by the following result:

$\,$

+-- {: .num_prop}
###### Proposition
**([Fiorenza-Sati-Schreiber 13, section 5](#FSS13))**

Write $\widetilde {String_{IIA}}$ for the [[super formal smooth infinity-groupoid|super 2-group]]

that [[Lie integration|Lie integrates]] the super [[Lie 2-algebra]] $\mathfrak{string}_{IIA}$

subject to the condition that it carries a globally defined [[Maurer-Cartan form]].

Then for $\Sigma_{p+1}$ a [[worldvolume]] [[smooth manifold]]

there is a [[natural equivalence]]

$$
  \left\{
     \Sigma_{p+1}
       \stackrel{\Phi}{\longrightarrow}
     \widetilde{String_{IIA}}
  \right\}
  \;\;\;
    \leftrightarrow
  \;\;\;
  \left\{
    \array{
      \Sigma_{p+1} \stackrel{\phi}{\longrightarrow} \mathbb{R}^{9,1\vert \mathbf{16}+ \overline{\mathbf{16}} },
      \\
      \nabla \in Conn(\Sigma_{p+1}, \phi^\ast  \mu_{string_{IIA}} )
    }
  \right\}
$$

between "higher Sigma-model fields" $\Phi$

and pairs, consisting of

an ordinary sigma-model field $\phi$

and a [[gauge field]] $\nabla$ on the [[worldvolume]] of the D-brane

twisted by the [[Kalb-Ramond field]].

This is the _[[Chan-Paton gauge field]]_ on the D-brane.

$\,$

Similarly:

Write $\widetilde {M2Brane}$ for the [[super formal smooth infinity-groupoid|super 3-group]]

that [[Lie integration|Lie integrates]] the super [[Lie 3-algebra]] $\mathfrak{m}2\mathfrak{brane}$

subject to the condition that it carries a globally defined [[Maurer-Cartan form]].

Then for $\Sigma_{5+1}$ a [[worldvolume]] [[smooth manifold]]

there is a [[natural equivalence]]

$$
  \left\{
     \Sigma_{5+1}
       \stackrel{\Phi}{\longrightarrow}
     \widetilde{M2Brane}
  \right\}
  \;\;\;
    \leftrightarrow
  \;\;\;
  \left\{
    \array{
      \Sigma_{5+1} \stackrel{\phi}{\longrightarrow} \mathbb{R}^{10,1\vert \mathbf{32}  },
      \\
      \nabla \in 2Conn(\Sigma_{p+1}, \phi^\ast  \mu_{M2} )
    }
  \right\}
$$

between "higher Sigma-model fields" $\Phi$

and pairs, consisting of

an ordinary sigma-model field $\phi$

and a [[higher gauge field]] $\nabla$ on the [[worldvolume]] of the [[M5-brane]]

and twisted by the [[supergravity C-field]].

=--

$\,$

(See also at _[[schreiber:Structure Theory for Higher WZW Terms]]_, session II).






### The super D-branes and the super M5-brane
 {#TheSuperDBranes}

+-- {: .num_defn #RationalSphereAlgebra}
###### Definition

For $p \in \mathbb{N}_{even}$, write

$b^{2p+2} \mathbb{R}/b^p \mathbb{R}$ for the [[L-∞ algebra]] given by the [[Chevalley-Eilenberg algebra]]

$$

  CE(b^{2p+2} \mathbb{R}/b^p \mathbb{R})
  =
  \left(\left\langle g_{p+2}, g_{2p+3}\right\rangle), {{d g_{p+2} = 0} \atop {d g_{2p+3} = g_{p+2} \wedge g_{p+2}}}\right)
  \,.
$$

=--

+-- {: .num_remark #RationalSpheres}
###### Remark

Regarded as a [[Sullivan model]] in [[rational homotopy theory]], then the [[dg-algebra]] of def. \ref{RationalSphereAlgebra} is a minimal model for the [[rationalization]] of the $(p+2)$-[[sphere]].

=--

By the [recognition theorem for L-∞ extensions](model+structure+for+L-infinity+algebras#HomotopyFiberProducts) we get:

+-- {: .num_prop #b2RactionOnb2p2R}
###### Proposition

For $p \in \mathbb{N}_{even}$, there is a [[homotopy fiber sequence]] in the [[homotopy theory of L-∞ algebras]] of the form

$$
  \array{
    b^{2p+2} \mathbb{R}
    \\
    \downarrow
    \\
    b^{2p+2} \mathbb{R}/b^{p}\mathbb{R}
    &\stackrel{}{\longrightarrow}&
    b^{p+1}\mathbb{R}
  }
$$

where on [[formal dual]] [[Chevalley-Eilenberg algebras]] in terms of our defining generating elements the horizontal map is given by $g_{p+4}\mapsto g_{p+4}$ and the vertical map by $g_{p+4}\mapsto 0$ and $g_{2p+3}\mapsto g_{2p+3}$.

By the discussion at _[[∞-action]]_ this exhibits a $b^{p}\mathbb{R}$-action on $b^{2p+2}\mathbb{R}$, for which $b^{2p+2} \mathbb{R}/b^{p}\mathbb{R}$ is the [[homotopy quotient]], whence the notation.

=--

+-- {: .num_example}
###### Example

For $p=2$ and regarded as a statement in [[rational homotopy theory]] via remark \ref{RationalSpheres}, then the extension in prop. \ref{b2RactionOnb2p2R} is a [[Sullivan minimal model]] for the rationalized [[Hopf fibration]]

$$
  \array{
    S^3 &\longrightarrow& S^7
    \\
    && \downarrow
    \\
    && S^4
  }
$$

=--


+-- {: .num_defn #CocyclesOn11dSuperMinkowski}
###### Proposition

The elements $\mu_4, \mu_7 \in CE(\mathbb{R}^{10,1\vert \mathbf{32}})$,
def. \ref{ThePsiPsiTermsInCEOfSuperMinkowski}, satisfy

1. $d \mu_4 = 0$;

1. $d \mu_7 = 15 \, \mu_4 \wedge \mu_4$

=--

As a mathematical statement prop. \ref{CocyclesOn11dSuperMinkowski} is originally due to ([D'Auria-Fr&#233; 82, p.18](#DAuriaFre82)), where it is considered as an ingredient for constructing the [[action functional]] of [[11-dimensional supergravity]] in the [[D'Auria-Fré formulation of supergravity]]. The statement has been rediscovered in ([BLNPST 97, (9)](#BLNPST97)), finding its interpretation as giving the [[geometry of physics -- WZW terms|WZW term]] of the [[Green-Schwarz sigma model]] for the [[M5-brane]].


+-- {: .num_defn #m2braneLie3Algebra}
###### Definition

Write $\mathfrak{m}2\mathfrak{brane} \in sL_\infty Alg$ for the [[super L-∞ algebra]] which is the [[homotopy fiber]] of $\mu_4$ in prop. \ref{CocyclesOn11dSuperMinkowski}.

$$
  \array{
     \mathfrak{m}2\mathfrak{brane}
     \\
     \downarrow
     \\
     \mathbb{R}^{10,1\vert \mathbf{32}}
     &\stackrel{\mu_4}{\longrightarrow}&
     b^3 \mathbb{R}
  }
  \,.
$$

and specifically for the representive of this homotopy fiber which, by the [recognition theorem for L-∞ extensions](model+structure+for+L-infinity+algebras#HomotopyFiberProducts), is given by having the [[Chevalley-Eilenberg algebra]]

$$
  CE(\mathfrak{m}2\mathfrak{brane}) = (CE(\mathbb{R}^{10,1\vert \mathbf{32}})\otimes \langle h_3\rangle, d h_3 = -\mu_4)
  \,.
$$

=--

In terms of def. \ref{m2braneLie3Algebra}, the second item in prop. \ref{CocyclesOn11dSuperMinkowski} reads as follows:


+-- {: .num_cor #The7CocycleOnm2brane}
###### Corollary

There is a super $L_\infty$-cocycle of the form

$$
  \mathfrak{m}2\mathfrak{brane}
  \stackrel{h_3 \wedge \mu_4 + \frac{1}{15} \mu_7}{\longrightarrow}
  b^6 \mathbb{R}
  \,.
$$

=--

But since $\mathfrak{m}2\mathfrak{brane}$ is a $b^2 \mathbb{R}$-[[principal ∞-bundle]], it is natural to ask whether $h_3 \wedge \mu_4 + \frac{1}{15} \mu_7$ is $b^2 \mathbb{R}$-[[equivariant cohomology|equivariant]] with respect to some natural $b^2\mathbb{R}$-[[∞-action]] on $b^6 \mathbb{R}$. Such a natural action is given by prop. \ref{b2RactionOnb2p2R}. To exhibit in components the equivariance of the 7-cocycle in corollary \ref{The7CocycleOnm2brane} with respect to this action we need a [[resolution]] of [[super Minkowski spacetime]]:

+-- {: .num_defn}
###### Definition

Write $\mathbb{R}_{res}^{10,1\vert \mathbf{32}}$ for the [[super L-∞ algebra]] whose [[Chevalley-Eilenberg algebra]] is obtained from that of [[super Minkowski spacetime]] by


$$
  CE\left(
   \mathbb{R}_{res}^{10,1\vert \mathbf{32}}
  \right)
  \coloneqq
  \left(
   CE\left(
     \mathbb{R}^{10,1\vert \mathbf{32}}\right)\otimes \left\langle h_3, g_4\right\rangle ,
     {{d h_3 = g_4 - \mu_4} \atop {d g_4 = 0}}
  \right)
  \,.
$$


=--

+-- {: .num_prop}
###### Proposition

The canonical morphism

$$
  \mathbb{R}_{res}^{10,1\vert \mathbf{32}}
  \stackrel{\simeq}{\longrightarrow}
  \mathbb{R}^{10,1\vert \mathbf{32}}
$$

given dually by $\psi^\alpha \mapsto \psi^\alpha$, $e^a \mapsto e^a$, is an equivalence of $L_\infty$-algebras. It factors the morphism $\mathfrak{m}2\mathfrak{brane} \longrightarrow \mathbb{R}^{10,1\vert \mathbf{32}}$ from def. \ref{m2braneLie3Algebra} through a morphism $\mathfrak{m}2\mathfrak{brane}  \longrightarrow \mathbb{R}^{10,1\vert \mathbf{32}}_{res}$ which on [[formal dual]] CE-elements is given by $h_3 \mapsto 0$, $g_4 \mapsto 0$ and by being the identity on all other generators.


=--

+-- {: .num_prop #7CocycleOnM2BraneDescends}
###### Proposition

There is a [[diagram]] of [[L-∞ algebras]] of the form

$$
  \array{
    && \vdots && && \vdots
    \\
    && \downarrow \downarrow && && \downarrow \downarrow
    \\
    &&
    \mathfrak{m}2\mathfrak{brane}
    &&
      \stackrel{h_3 \wedge \mu_4  + \frac{1}{15}\mu_7 }{\longrightarrow}
    &&
    b^6 \mathbb{R}
    \\
    &&
    \downarrow && && \downarrow
    \\
    \mathbb{R}^{10,1\vert\mathbf{32}}
    &\stackrel{\simeq}{\longleftarrow}&
    \mathbb{R}_{res}^{10,1\vert\mathbf{32}}
    &&
      \stackrel{h_3 \wedge (g_4 + \mu_4) + \frac{1}{15}\mu_7 }{\longrightarrow}
    &&
    b^6 \mathbb{R}/b^2 \mathbb{R}
    \\
    &&
    & {}_{\mathllap{}}\searrow && \swarrow
    \\
    &&
    && b^3 \mathbb{R}
  }
$$

=--

+-- {: .proof}
###### Proof

That the diagram exists and commutes at the level of the underlying graded algebras of the [[formal dual]] CE-algebras is immediate in terms of the defining generators: each generator is mapped to the generator of the same name, if present, in the codomain, or to zero otherwise, except for $g_7 \in CE(b^6 \mathbb{R})$ which is sent to $h_3 \wedge \mu_4  + \frac{1}{15}\mu_7$ and $g_7 \in CE(b^6 \mathbb{R}/b^2 \mathbb{R})$, which is sent to $h_3 \wedge (g_4 + \mu_4) + \frac{1}{15}\mu_7 $, as indicated.

It remains to check that the middle horizontal map respects the CE-differentials: by prop. \ref{CocyclesOn11dSuperMinkowski} we have

$$
  \begin{aligned}
    d(h_3 \wedge (g_4 + \mu_4) + \frac{1}{15}\mu_7)
    &=
    (g_4 - \mu_4) \wedge (g_4 + \mu_4) + \mu_4 \wedge \mu_4
    \\
    & = g_4 \wedge g_4
  \end{aligned}
$$

and by def. \ref{RationalSphereAlgebra} this says indeed that $g_7 \mapsto h_3 \wedge (g_4 + \mu_4) + \frac{1}{15}\mu_7$ respects the CE-differentials.

=--

+-- {: .num_remark}
###### Remark

The form of the equivariant cocycle in prop. \ref{7CocycleOnM2BraneDescends} is that of the [[curvature]] of the [[geometry of physics -- WZW terms|WZW term]] of the [[sigma model]] describing the [[M5-brane]] as considered in ([BLNPST 97, (6),(8)](#BLNPST97)).

=--


+-- {: .num_remark}
###### Remark

In view of remark \ref{RationalSpheres}, prop. \ref{7CocycleOnM2BraneDescends} says that the CE-elements $\mu_4$ and $\mu_7$ of prop. \ref{CocyclesOn11dSuperMinkowski} define a cocycle with values in the rational 4-sphere. In the discussions in _[[geometry of physics -- WZW terms]]_ and _[[geometry of physics -- BPS charges]]_ we see that under [[Lie integration]] and globalization in [[higher Cartan geometry]], these elements encode the [[supergravity C-field]] and its [[electric-magnetic duality|magnetic dual]]. That these fields should take values in the 4-sphere was first suggested in ([Sati 13, section 2.5](Hisham+Sati#Sati13)).

=--







$\,$

In **conclusion** this shows that

given a cocycle $\mu_{p_1+2}$ for some super $p_1$-brane species

inducing an [[extended super Minkowski spacetime]] via its [[homotopy fiber]]

and then given a consecutive cocycle $\mu_{p_2+2}$ for a $p_2$-brane species on that homotopy fiber

then $p_1$-branes may end on $p_2$-branes

and the $p_2$-branes propagating in the extended spacetime $p_1 \mathfrak{brane}$

see a higher gauge field on their worldvolume

of the kind sourced by boundaries of $p_1$-branes.

$\,$

$$
  \array{
    {
      \text{spacetime}
      \atop
      \text{with}\,p_1\text{-brane condensate}
    }
    && p_1 \mathfrak{brane} &\overset{\mu_{p_2+2}}{\longrightarrow}& B^{p_2+2}
    \\
    && {}^{\mathllap{hofib(\mu_{p_1+2})}}\downarrow
    \\
    \text{spacetime}
    && \mathbb{R}^{d-1,1\vert \mathbf{N}}
      &\underset{\mu_{p_1+2}}{\longrightarrow}&
    B^{p_1+1}\mathbb{R}
  }
$$

$\,$

Hence the [[extended super Minkowski spacetime]] $p_1 \mathfrak{brane}$

is like the original super spacetime $\mathbb{R}^{d-1,1\vert \mathbf{N}}$

but filled with a [[condensation|condensate]] of $p_1$-branes

whose boundaries source a [[higher gauge field]].


$\,$

While this is good,

it means that at each stage of the [[schreiber:brane bouquet]]

we are describing $p_2$-brane dynamics

on a fixed $p_1$-brane [[background field]].

But more generally

we would like to describe the joint dynamics

of all brane species at once.

$\,$

This we turn to now.

$\,$







## Fields
 {#Fields}


We now discuss that

$\;\;\;\;$There is homotopy [[descent]] of $p$-brane WZW terms

$\;\;\;\;$from [[extended super Minkowski spacetime]]

$\;\;\;\;$down to ordinary [[super Minkowski spacetime]]

$\;\;\;\;$which yields cocycles in [[twisted cohomology]]

$\;\;\;\;$for the [[RR-field]] and the M-flux fields.


([Fiorenza-Sati-Schreiber 15](#FSS15), [16a](#FSS16a)).



$\,$

In order to explain this we now first recall

the general nature of [[twisted cohomology]]

and its role in [[string theory]].

$\,$

### Twisted generalized cohomology

$\,$

It is often stated that a

[[Chan-Paton gauge field]] on $n$ coincident [[D-branes]]

is an [[special unitary group|SU(n)]]-[[vector bundle]] $V$,

hence a cocycle in [[nonabelian cohomology]] in degree 1.

$\,$

But this is not quite true.

In general there are $n$ [[D-branes]] and $n'$ [[anti-D-branes]] coinciding,

carrying [[Chan-Paton gauge fields]]

$V_{brane}$ (of [[rank]] $n$) and $V_{\text{anti-brane}}$ (of rank $n'$), respectively,

yielding a pair of [[vector bundles]]

$$
  (V_{\text{brane}}, V_{\text{anti-brane}})
  \,.
$$

Such pairs are also called _[[virtual vector bundles]]_.

$\,$

But [[D-branes]] annihilate with [[anti-D-branes]] ([Sen 98](https://ncatlab.org/nlab/show/anti+D-brane#Sen98))

when they have exact opposite [[D-brane charge]],

which here means that they carry the same [[Chan-Paton gauge field|Chan-Paton]] vector bundle.

In other words, pairs as above of the special form

$(W,W)$ are equivalent to pairs of the form $(0,0)$.

$$
  (W,W)
    \;\sim\;
  0
  \,.
$$

Hene the net Chan-Paton charge of coincident branes and anti-branes

is the [[equivalence class]] of $(V_{\text{brane}}, V_{\text{anti-brane}})$

under the [[equivalence relation]] which is generated by the [[relation]]

$$
  (V_{\text{brane}} \oplus W\,,\; V_{\text{anti-brane}} \oplus W)
    \;\sim\;
  (V_{brane}\,,\; V_{anti-brane})
$$

for all [[complex vector bundles]] $W$ ([Witten 98](https://ncatlab.org/nlab/show/anti+D-brane#Witten98),
[Witten 00](https://ncatlab.org/nlab/show/D-brane#Witten00)).

$\,$

The additive [[abelian group]] of such equivalence classes of [[virtual vector bundles]]

is called the _[[topological K-theory]].

$\,$

It follows that also the [[RR-fields]] are in K-theory ([Moore-Witten 00](https://ncatlab.org/nlab/show/anti+D-brane#MooreWitten99)).

$\,$

Topological K-theory is similar to [[ordinary cohomology]]

but is a [[generalized (Eilenberg-Steenrod) cohomology theory]].

A [[generalized cohomology theory]] is [[Brown representability theorem|represented]] by a _[[spectrum]]_

(in the sense of [[stable homotopy theory]]):

A [[spectrum]] is sequence of [[pointed topological spaces]]

$$
  E_n \;\;\;\; n \in \mathbb{N}
$$

equipped with [[weak homotopy equivalences]]

$$
  E_n
    \overset{\phantom{AA}\simeq\phantom{AA}}{\longrightarrow}
  \Omega E_{n+1}
$$

from one to the [[loop space]] of the next.


$\$

Given this, then the $E$-cohomology of any [[topological space]] $X$ is

$$
  E^n(X) \coloneqq \underset{\text{homotopy classes of maps}}{\underbrace{\pi_0\left\{  X \overset{\phantom{AAAAAA}}{\longrightarrow} E_n \right\} }}
  \,.
$$

For [[topological K-theory]] one writes

$$
  E = KU
$$

with

$$
  KU_{2n} \simeq B U \times \mathbb{Z}
  \;\;\,,\;\;
  KU_{2n+1} \simeq U
$$

with $U$ the [[stable unitary group]],

and $B U$ the [[classifying space]] for [[complex vector bundles]].

$\,$

But above we saw

that the [[Chan-Paton gauge field]] on a D-brane

is actually a [[twisted vector bundle]]

with twist given by the [[Kalb-Ramond field]]

sourced by a string condensate.

([[Freed-Witten anomaly cancellation]])

$\,$



Such _[[twisted cohomology]]_ [[generalized cohomology]] is given by

1. a classifying space of twists $B G$

1. a spectrum object in the [[slice category]] $Top_{/B G}$, namely a sequence of spaces $E_n/G$ equipped with maps

   $$
     id \;\colon\; B G \to E_n/G \to B G
   $$

   and weak equivalences

   $$
     E_n/G
       \overset{\phantom{AA}\simeq\phantom{AA} }{\longrightarrow}
    \Omega_{B G} (E_{n+1}/G)
      \coloneqq
    \underset{\text{homotopy} \atop {\text{fiber} \atop \text{product} } }{\underbrace{
     B G
       \underoverset{E_{n+1}/G}{h}{\times}
     B G
     }}
   $$

Extremal **examples**:

1. an ordinary spectrum $E$

   is a parameterized spectrum over the point;

   $$
     \array{
       E
       \\
       \downarrow
       \\
       \ast
     }
   $$

1. an ordinary space $X$

   is identified with the zero-spectrum parameterized over $X$:

   $$
     \array{
       X
       \\
       \downarrow
       \\
       X
     }
   $$


Then

1. a _twist_ $\tau$ for $E$-cohomology of $X$ is a map

   $$
     \array{
       X
       \\
       & {}_{\mathllap{\tau}}\searrow
       \\
       && B G
     }
   $$

1. the $\tau$-twisted $E$-cohomology of $X$ is

   $$
    E^{n+\tau}(X)
      \;\coloneqq\;
    \pi_0
    \left\{
     \array{
       X && \longrightarrow && E_n/G
       \\
       & {}_{\mathllap{\tau}} \searrow && \swarrow_{\mathrlap{}}
       \\
       && B G
     }
     \right\}
   $$

There is a [[homotopy fiber sequence]] (in parameterized spectra)

$$
  \array{
    E &\longrightarrow& E/G
    \\
    && \downarrow
    \\
    && B G
  }
$$

and this equivalently exhibits $E/G$ as the [[homotopy quotient]] of an ordinary spectrum $E$ by a $G$-[[infinity-action]].

([Nikolaus-Schreiber-Stevenson 12, section 4.1](#NSS12))

$\,$

Assume that $B G$ is simply connected, i.e. of the form $B^2 G$.

$\,$

We now translate this situation to [[super L-∞ algebras]]

via the central theorem of [[rational homotopy theory]].

$\,$

### Rational homotopy theory

$\,$

On every [[loop space]] $\Omega X$,

the operation of concatenation of loops

gives the structure of a [[group]] up to [[coherence|coherent]] [[higher homotopy]]

called a "grouplike [[A-∞ space]]"

or **[[∞-group]]** for short.

$\,$

**[[May recognition theorem]]:**

Conversely, for $G$ an [[∞-group]]

there is an essentially unique [[connected topological space|connected]] space $B G$

with $G \;\simeq\; \Omega B G$.


$\,$

Every double loop space $\Omega \Omega X$

becomes a "first order abelian" [[∞-group]]

by exchanging loop directons

called a _[[braided ∞-group]]_,

$\,$

For $G$ a [[braided ∞-group]] then

$B G$ is itself an [[∞-group]]

and so there exists an essentially unique [[simply connected topological space|simply connected]] space

$$
  B^2 G \coloneqq B (B G)
$$

with

$$
  G \;\simeq\; \Omega^2 B^2 G
  \,.
$$

$\,$


And so forth:

Every triple loop space $\Omega^3 X$

becomes a "second order abelian" [[∞-group]]

by exchanging loop directons

called a _[[sylleptic ∞-group]]_.

etc.

$\,$

In a [[spectrum]] $E$,

the maps $E_n \stackrel{\simeq}{\to} \Omega E_{n+1}$

exhbit $E_0$ as an [[infinite loop space]]

hence as a fully [[abelian ∞-group]].

$\,$

It turns out that by a [[homotopy theory|theoretic]] version of [[Lie theory]],

there is an [[L-∞ algebra]] $\mathfrak{g}$ associated with any [[∞-group]]

$$
  \mathfrak{g} \simeq  \mathfrak{l} B G
  \,.
$$

or

$$
  B\mathfrak{g} \simeq  \mathfrak{l} B^2 G
$$

etc.

$\,$

Its [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{B g})$

is called a _[[Sullivan model]]_ for $B^2 G$.

$\,$

For **example** the $L_\infty$-algebra associated with an [[Eilenberg-MacLane space]]

$$
  K(\mathbb{Z},n+1) \simeq B^{n+1}\mathbb{Z}
$$

is the [[line Lie-n algebra]] from above:

$$
  \mathfrak{l}(B^{n+1} \mathbb{Z})
    \;\simeq\;
  B^n \mathbb{R}
  \,.
$$

$\,$

The **main theorem of [[rational homotopy theory]]**  ([Quillen 69](https://ncatlab.org/nlab/show/rational+homotopy+theory#Quillen69),
[Sullivan 77](https://ncatlab.org/nlab/show/rational+homotopy+theory#Sullivan77))

says that the [[L-∞ algebra]] $\mathfrak{l}(B^2 G)$ equivalently reflects the _[[rationalization]]_ of $B^2 G$

(in fact the real-ification, since we are considering $L_\infty$-algebras over the real numbers).

This means that weak equivalence between $L_\infty$-algebras correspond to maps between spaces

that induce [[isomorphism]] on real-ified [[homotopy groups]]

$$
  \left\{
    \;\;\;\;\;
    \array{
      B^2 G_1
        \overset{\phantom{AA}f\phantom{AA}}{\longrightarrow}
      B^2 G_2
      \\
      \text{such that:}
      \\
      \pi_\bullet(B^2 G_1)\otimes_{\mathbb{Z}} \mathbb{R}
         \underoverset{\simeq}{\pi_\bullet(f) \otimes_{\mathbb{Z}} \mathbb{R}   }{\longrightarrow}
      \pi_\bullet(B^2 G_2) \otimes_{\mathbb{Z}} \mathbb{R}
    }
    \;\;\;\;\;
  \right\}
  \;\;\;\leftrightarrow\;\;\;
  \left\{
  \;
  \mathfrak{l}(B^2 G_1)
    \stackrel{\simeq}{\longrightarrow}
  \mathfrak{l}(B^2 G_2)
  \;
  \right\}
  \,.
$$

For concise review in the language that we use here see [Buijs-F&#233;lix-Murillo 12, section 2](https://ncatlab.org/nlab/show/rational+homotopy+theory#BuijsFelixMurillo12).


$\,$

We apply this [[rational homotopy theory]] functor

$$
  \mathfrak{l}(-)
    \;\colon\;
  \text{Spaces}
    \longrightarrow
  L_\infty\text{-Algebras}
$$

to find the $L_\infty$-algebraic version of [[parameterized spectra]]

hence of [[twisted cohomology]]:

$\,$

$$
  \array{
  {
  \text{parameterized}
    \atop
  \text{spectrum}
  }
  \;\;\;&\;\;\;\;
  \left\{
  \array{
    id : B^2 G \to E_n/ B G \to B^2 G
    \\
    E_n/ B G \stackrel{\simeq}{\longrightarrow} \Omega_{B^2 G} (E_{n+1}/ B G)
  }
  \right\}
  \;&\;\leftrightarrow\;&\;
  \left(
  \array{
    E &\longrightarrow& E/B G
    \\
    && \downarrow
    \\
    && B^2 G
  }
  \right)
  \\
  & \mathfrak{l}(-)\downarrow
  \\
  L_\infty\text{Algebra}
  \;\;\;&\;\;\;\;
  \left\{
  \array{
    id : \mathfrak{l}(B^2 G) \to \mathfrak{l}(E_n/ B G) \to \mathfrak{l}(B^2 G)
    \\
    \mathfrak{l}(E_n/ B G) \stackrel{\simeq}{\longrightarrow} \Omega_{\mathfrak{l}(B^2 G)} \mathfrak{l}(E_{n+1}/ B G)
  }
  \right\}
  \;&\;\leftrightarrow\;&\;
  \left(
  \array{
    V[1] &\longrightarrow& V[1]/\mathfrak{g}
    \\
    && \downarrow
    \\
    && B \mathfrak{g}
  }
  \right)
  }
$$

$\,$

Here $V \simeq E \otimes \mathbb{R}$ is a chain complex

underlying the real-ification of the spectrum $E$

([[stable Dold-Kan correspondence]]).

$\,$

So for $\mathbb{R}^{d-1,1\vert \mathbf{N}}$ some [[super Minkowski spacetime]],
a cocycle in $\mathfrak{g}$-twisted $V$-cohomology is a diagram of the form

$$
  \array{
    \mathbb{R}^{d-1,1\vert \mathbf{N}}
      && \overset{}{\longrightarrow} &&
    V/\mathfrak{g}
    \\
    & \searrow && \swarrow
    \\
    && B \mathfrak{g}
  }
$$

$\,$


Now given one stage in the [[schreiber:brane bouquet]]

$$
  \array{
    \widehat{\widehat{\mathfrak{g}}}
    \\
    {}^{\mathllap{hofib(\mu_{p_2})}}\downarrow
    \\
    \hat \mathfrak{g}
    &
      \stackrel{\mu_{p_2}}{\longrightarrow}
    &
    B\mathfrak{h}_2
    \\
    {}^{\mathllap{hofib(\mu_{p_1})}}\downarrow
    \\
    \mathfrak{g}
    &\overset{\mu_{p_1}}{\longrightarrow}&
    B\mathfrak{h}_1
  }
$$

we want to descent $\mu_{p_2}$ to $\mathfrak{g}$.

$\,$

By the general theory of [[principal ∞-bundles]] ([Nikolaus-Schreiber-Stevenson 12](#NSS12)):

1. $\widehat{\mathfrak{g}}$ has a $\mathfrak{h}_1$-[[∞-action]]

1. equipping $B \mathfrak{h}_2$ with an $\mathfrak{h}_1$-[[∞-action]]

   is equivalent to finding a [[homotopy fiber sequence]] as on the right here:

   $$
     \array{
       \hat \mathfrak{g}
       &&
         \stackrel{\mu_2}{\longrightarrow}
       &&
       \mathbf{B}\mathfrak{h}_2
       \\
       {}^{\mathllap{hofib(\mu_1)}}\downarrow
       && &&
       \downarrow^{\mathrlap{hofib(p_\rho)}}
       \\
       \mathfrak{g}
       && &&
       (\mathbf{B}\mathfrak{h}_2)/\mathfrak{h}_1
       \\
       & {}_{\mathllap{\mu_1}}\searrow  && \swarrow_{\mathrlap{p_\rho}}
       \\
       && \mathbf{B}\mathfrak{h}_1
     }
     \,.
   $$

1. $\mu_2$ is $\mathfrak{h}_1$-equivariant precisely if it descends to a morphism

   $$
     \mu_2/\mathfrak{h}_1
     \;\colon\;
     \mathfrak{g}
     \longrightarrow
     (\mathbf{B}\mathfrak{h}_2)/\mathfrak{h}_1
   $$

   such that this [[diagram]] [[commuting diagram|commute]] up to homotopy:

   $$
     \array{
       \hat \mathfrak{g}
       &&
         \stackrel{\mu_2}{\longrightarrow}
       &&
       \mathbf{B}\mathfrak{h}_2
       \\
       {}^{\mathllap{hofib(\mu_1)}}\downarrow
       && &&
       \downarrow^{\mathrlap{hofib(p_\rho)}}
       \\
       \mathfrak{g}
       &&
         \stackrel{\mu_2/\mathfrak{h}_1}{\longrightarrow}
       &&
       (\mathbf{B}\mathfrak{h}_2)/\mathfrak{h}_1
       \\
       & {}_{\mathllap{\mu_1}}\searrow  && \swarrow_{\mathrlap{p_\rho}}
       \\
       && \mathbf{B}\mathfrak{h}_1
     }
     \,.
   $$

1. if so, then resulting triangle diagram

   $$
     \array{
       \mathfrak{g}
       &&
         \stackrel{\mu_2/\mathfrak{h}_1}{\longrightarrow}
       &&
       (\mathbf{B}\mathfrak{h}_2)/\mathfrak{h}_1
       \\
       & {}_{\mathllap{\mu_1}}\searrow  && \swarrow_{\mathrlap{p_\rho}}
       \\
       && \mathbf{B}\mathfrak{h}_1
     }
   $$

   exhibits $\mu_2/\mathfrak{h}_1$  as a [[cocycle]] in ([[rational homotopy theory|rational]]) _$\mu_1$-[[twisted cohomology]]_

   with respect to the [[local coefficient bundle]] $p_\rho$.


$\,$

We now work out this general prescription

for the cocycles in the [[schreiber:brane bouquet]].

$\,$

### RR-fields

$\,$

By the [[schreiber:brane bouquet]] above

the type IIA [[D-branes]]

are given by super $L_\infty$ cocycles of the form

$$
  \mathfrak{string}_{IIA }
    \overset{\mu_{Dp}}{\longrightarrow}
  B^{p+1}\mathbb{R}
$$

for $p \in \{0,2,4,6,8,10\}$.

$\,$

Notice that

$$
  H^\bullet(B U, \mathbb{Z})
$$

has one generator in each even degree, the [[universal Chern classes]].

Hence the $L_\infty$-algebra

$$
  \mathfrak{l}(KU)
$$

is given by

$$
  CE(\mathfrak{l}(KU))
    \;\simeq\;
  \left\{
    d \omega_{2p+2} = 0
    \;\vert\;
    p \in \mathbb{Z}
  \right\}
  \,.
$$

This allows to unify the D-brane cocycles

into a single morphism of super $L_\infty$-algebras of the form


$$
  \array{
     \mathfrak{string}_{IIA}
     &&
     \stackrel{\phantom{AA}\mu_D\phantom{AA}}{\longrightarrow}
     &&
     \mathfrak{l}(KU)
     \\
     {}^{\mathllap{hofib(\mu_{F1})}}\downarrow
     \\
     \mathbb{R}^{9,1\vert \mathbf{16}+ \overline{\mathbf{16}}}
     \\
     & {}_{\mathllap{\mu_{F1}}}\searrow
     \\
     &&
     \mathbf{B}^2 \mathbb{R}
  }
  \,.
$$

$\,$

By the above prescription, descending $\mu_D$ is equivalent

to finding a [[commuting diagram]] in the [[homotopy category]] of super $L_\infty$-algebras

of the form

$$
  \array{
     \mathfrak{string}_{IIA}
     &&
     \stackrel{\phantom{AA}\mu_D\phantom{AA}}{\longrightarrow}
     &&
     \mathfrak{l}(KU)
     \\
     {}^{\mathllap{hofib(\mu_{F1})}}\downarrow
       && &&
     \downarrow^{\mathrlap{hofib(\phi)}}
     \\
     \mathbb{R}^{9,1\vert \mathbf{16}+ \overline{\mathbf{16}}}
       &&\overset{\phantom{AA}\mu_{D}/B \mathbb{R}\phantom{AA} }{\longrightarrow}&&
     \text{something}
     \\
     & {}_{\mathllap{\mu_{F1}}}\searrow && \swarrow_{\mathrlap{\phi}}
     \\
     &&
     \mathbf{B}^2 \mathbb{R}
  }
  \,.
$$

$\,$

This turns out to exist as follows ([Fiorenza-Sati-Schreiber 16a, section 5](#FSS16a)):

Define the $L_\infty$-algebra

$$
  \mathfrak{l}(KU / BU(1))
$$

by

$$
  CE\left(\mathfrak{l}(KU / BU(1))\right)
  \;=\;
  \left\{
    \array{
      d h_3 = 0\;,\;
      \\
      d \omega_{2p+2} = h_3 \wedge \omega_{2p}
    }
  \right\}
  \,.
$$

Moreover write

$$
  \mathbb{R}^{9,1\vert \mathbf{16} + \overline{\mathbf{16}}}_{res}
$$

for the super $L_\infty$-algebra whose [[Chevalley-Eilenberg algebra]] is

$$
  CE\left(
    \mathbb{R}^{9,1\vert \mathbf{16} + \overline{\mathbf{16}}}_{res}
  \right)[f_2,h_3]/(d f_2 = \mu_{F1} + h_3)
$$


$\,$

+-- {: .num_prop #DescentOfIIACocycles}
###### Proposition
**([Fiorenza-Sati-Schreiber 16a, theorem 4.16](#FSS16a))**

The super $L_\infty$-algebra $\mathbb{R}^{9,1\vert \mathbf{16} + \overline{\mathbf{16}}}_{res}$

is a [[resolution]] of type IIA [[super-Minkowski spacetime]].

in that there is a weak equivalence

$$
 \mathbb{R}^{9,1\vert \mathbf{16} + \overline{\mathbf{16}}}_{res}
   \stackrel{\phantom{AA}\simeq\phantom{AA}}{\longrightarrow}
  \mathbb{R}^{9,1\vert \mathbf{16} + \overline{\mathbf{16}}}
  \,.
$$

This fits into a [[commuting diagram]] of the form


$$
  \array{
     \left\{ {{d e^a = \overline{\psi}\Gamma^a \wedge \psi } \atop {d \psi^\alpha = 0}} \atop { d f_2 = \mu_{F1}} \right\}
     &&
     \mathfrak{string}_{IIA}
     && \stackrel{ \mu_D  }{\longrightarrow} &&
     \mathfrak{l}(KU)
     &&
     \left\{
       d \omega_{2 p+2} = 0
     \right\}
     \\
     && \downarrow^{\mathrlap{hofib(\mu_{F1})}} && && \downarrow^{\mathrlap{\phi}}
     \\
     \left\{ {{d e^a = \overline{\psi}\Gamma^a \wedge \psi } \atop {d \psi^\alpha = 0}} \atop { d f_2 = \mu_{F1} + h_3 } \right\}
     &
     &
     \mathbb{R}_{res}^{9,1\vert \mathbf{16}+ \overline{\mathbf{16}}}
     &&
      \stackrel{ \mu_{F1/D} }{\longrightarrow}
     &&
      \mathfrak{l}(KU / B U(1))
     &&
     \left\{
        d\omega_{2p+2} = h_3\wedge \omega_{2p}
     \right\}
     \\
     && & {}_{\mathllap{\mu_{F 1}}}\searrow && \swarrow_{\mathrlap{\phi}}
     \\
     && && \mathbf{B}^2 \mathbb{R}
     \\
     && && \left\{ d h_3 = 0 \right\}
  }
  \,.
$$

=--

$\,$

In **conclusion**

$\;\;$_the type IIA [[F1-brane]] and [[D-brane]] cocycles with $\mathbb{R}$-[[coefficients]]_

$\;\;$_do descent to super-Minkowski spacetime_

$\;\;$_as one single cocycle with [[coefficients]]_

$\;\;$_in rationalized [[twisted K-theory]]_.

<img src="https://ncatlab.org/schreiber/files/CocyclesInTwistedKTheory.png" width="650">

$\,$

### M-flux fields

$\,$

The part of the [[schreiber:brane bouquet]] giving the [[M-branes]] is


$$
  \array{
     \mathfrak{m}2\mathfrak{brane}
     &\stackrel{\mu_{M5}}{\longrightarrow}&
     \mathbf{B}^6 \mathbb{R}
     \\
     {}^{\mathllap{hofib(\mu_{M2})}}\downarrow
     \\
     \mathbb{R}^{10,1\vert \mathbf{32}}
     & \stackrel{\mu_{M2}}{\longrightarrow} &
     \mathbf{B}^3 \mathbb{R}
     \\
     {}^{\mathllap{hofib(\mu_{D 0})}}\downarrow
     \\
     \mathbb{R}^{9,1\vert \mathbf{16} + \overline{\mathbf{16}}}
  }
$$

$\,$

In order to descend this, consider the $L_\infty$-algebra corresponding to the [[4-sphere]]

$$
  \mathfrak{l}(S^4)
  \,.
$$

By standard results on [[rational n-spheres]], this is given by

$$
  CE(\mathfrak{l}S^4)
   \;\simeq\;
  \left\{
    \array{
      d \, g_4 = 0\,,\,
      \\
      d\, g_7 + \tfrac{1}{2} g_4 \wedge _4 = 0
    }
  \right\}
  \,.
$$

+-- {: .num_prop #MBraneDescent}
###### Proposition
[Fiorenza-Sati-Schreiber 15, section 3](FSS15)

There is a [[homotopy fiber sequence]] of $L_\infty$-algebras as on the right

$$
  \left(
  \array{
    && S^7
    \\
    && \downarrow
    \\
    && S^4
    \\
    & \swarrow
    \\
    B SU(2)
    \\
    \downarrow^{\mathrlap{c_2}}
    \\
    B^3 U(1)
  }
  \right)
    \;\;
    \stackrel{\phantom{AA}\mathfrak{l}(-)\phantom{AA} }{\mapsto}
    \;\;
  \left(
  \array{
    && B^6 \mathbb{R}
    \\
    && \downarrow^{\mathrlap{ hofib(\mathfrak{l}(c_2)) } }
    \\
    &&\mathfrak{l}(S^4)
    \\
    & \swarrow_{\mathfrak{l}(c_2)}
    \\
    B^3 \mathbb{R}
  }
  \;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;
  \right)
$$


which is the image under $\mathfrak{l}(-)$ of the [[quaternionic Hopf fibration]].

This makes a [[commuting diagram]]

in the [[homotopy category]] of super $L_\infty$-algebas

of the form

$$
  \array{
    \left\{
      { { d e^a = \overline{\psi}\wedge \Gamma^a \wedge \psi }
       \atop
      { d \psi^\alpha = 0 } }
      \atop
      d h_3 = - \mu_{M2}
    \right\}
    &&
    \mathfrak{m}2\mathfrak{brane}
    &&
      \stackrel{ \mu_{M5} }{\longrightarrow}
    &&
    B^6 \mathbb{R}
    &&
    \left\{
      d g_7 = 0
    \right\}
    \\
    &&
    \downarrow^{\mathrlap{hofib(\mu_{M2})}} && && \downarrow^{\mathrlap{hofib(\mathfrak{l}(c_2))}}
    \\
    \left\{
      { { d e^a = \overline{\psi}\wedge \Gamma^a \wedge \psi }
       \atop
      { d \psi^\alpha = 0 } }
      \atop
      d h_3 = g_4 - \mu_{M2}
    \right\}
    &&
    \mathbb{R}_{res}^{10,1\vert\mathbf{32}}
    &&
      \stackrel{ \mu_{M2/M5} }{\longrightarrow}
    &&
    \mathfrak{l} S^4
    &&
    \left\{
      {d g_4 = 0} \atop {d g_7 + \tfrac{1}{2} g_4 \wedge g_4 = 0}
    \right\}
    \\
    &&
    & {}_{\mathllap{\mu_{M2}}}\searrow && \swarrow_{\mathrlap{\mathfrak{l}(c_2)}}
    \\
    &&
    && \mathbf{B}^3 \mathbb{R}
    \\
    && && \left\{ d g_4 = 0\right\}
  }
$$

=--

In **conclusion**

$\;\;$_this says that, rationally,_

$\;\;$_M2-brane charge is in degree-4 ordinary cohomology_

$\;\;$_and it twists M5-brane charge_

$\;\;$_which is, rationally,  in unstable degree-4 [[cohomotopy]]._

$\,$

This confirms a conjecture due to

([Sati 10, section 6.3](https://ncatlab.org/schreiber/show/Equivariant+cohomology+of+M2/M5-branes#Sati10), [Sati 13, section 2.5](https://ncatlab.org/schreiber/show/Equivariant+cohomology+of+M2/M5-branes#Sati13)).

based on the observation that

the [[equations of motion]] of [[11-dimensional supergravity]]

for the [[supergravity C-field]] [[field strength]] $G_4$  say that

$$
  d G_7 + \tfrac{1}{2} G_4 \wedge G_4 = 0
$$

with $G_7 = \ast G_4$ the [[Hodge dual]]

and this is just the algebraic relation for the Sullivan model of the [[rational n-sphere|rational 4-sphere]].


$\,$

Notice that, unstably, the [[4-sphere]]

is just the space whose [[torsion subgroup|non-torsion]] [[homotopy groups]]

hence those that are visible in [[rational homotopy theory]]

are in degrees 2+2 and 5+2:

| k | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
|---|---|---|---|---|---|---|---|
| $\phantom{AA}\pi_k(S^4)\phantom{AA}$ | $\phantom{AA}0\phantom{AA}$ | $\phantom{AA}0\phantom{AA}$ | $\phantom{AA}0\phantom{AA}$ | $\phantom{AA}\mathbb{Z}\phantom{AA}$ | $\phantom{AA}\mathbb{Z}/2\phantom{AA}$ | $\phantom{AA}\mathbb{Z}/2\phantom{AA}$ | $\phantom{AA}\mathbb{Z} \oplus \mathbb{Z}/{12}\phantom{AA}$ |

$\,$

But the correct non-rational lift of the $\mathfrak{l}(S^4)$-coefficients

will also have to be such that it somehow gives rise to [[twisted K-theory]]

under (double) dimensional reduction. This is still an **open problem**.

For further comments see the talk

_[[schreiber:Equivariant cohomology of M2/M5-branes]]_

$\,$

$\,$

Now that we have found

the descended $L_\infty$-cocycles

for all super $p$-branes

in twisted cohomology, rationally,

we may analyze their behaviour under [[double dimensional reduction]]

and discover the super $L_\infty$-algebraic incarnation

of various [[dualities in string theory]].


$\,$

## Double dimensional reduction
 {#DoubleDimensionalReduction}

$\,$


+-- {: .num_defn #Cyclification}
###### Definition

For $\mathfrak{g}$ any [[super L-∞ algebra]] of [[finite type]], its **cyclification**

$$
  \mathfrak{L}\mathfrak{g}/\mathbb{R}
  \in
  s L_\infty Alg_{\mathbb{R}}
$$

is defined by having [[Chevalley-Eilenberg algebra]] of the form

$$
  CE(\mathfrak{L}\mathfrak{g}/\mathbb{R})
  \coloneqq
  \left(
    \wedge^\bullet
      \left(
        \underset{\text{original}}{\underbrace{\mathfrak{g}^\ast}}
        \oplus
         \underset{\text{shifted copy}}{\underbrace{s\mathfrak{g}^\ast}}
          \oplus
         \underset{\text{new generator} \atop \text{in degree 2}}{\underbrace{\langle \omega_2 \rangle}}
      \right)
      \;,\;
  d_{\mathfrak{d}\mathfrak{g}/\mathbb{R}}
  \;\colon\;
  \left\{
    \array{
      \omega_2 &\mapsto& 0
      \\
      \alpha &\mapsto& d_{\mathfrak{g}} \alpha + \omega_2 \wedge s \alpha
      \\
      s \alpha &\mapsto&  - s d_{\mathfrak{g}} \alpha
    }
  \right.
  \right)
$$

where

$$
  s \mathfrak{g}^\ast
$$

is a copy of $\mathfrak{g}^\ast$ with cohomological degrees shifted _down_ by one, and where $\omega$ is a new generator in degree 2.

The differential is given for $\alpha \in \wedge^1 \mathfrak{g}^\ast$ by


$$
  d_{\mathfrak{d}\mathfrak{g}/\mathbb{R}}
  \;\colon\;
  \left\{
    \array{
      \omega_2 &\mapsto& 0
      \\
      \alpha &\mapsto& d_{\mathfrak{g}} \alpha \pm \omega_2 \wedge s \alpha
      \\
      s \alpha &\mapsto&  - s d_{\mathfrak{g}} \alpha
    }
  \right.
$$

where on the right we are extendng $s$ as a graded derivation.

Define

$$
  \mathfrak{L}\mathfrak{g}
  \in
  s L_\infty Alg_{\mathbb{R}}
$$

in the same way, but with $\omega_2 \coloneqq 0$.

=--


For every $\mathfrak{g}$ there is a [[homotopy fiber sequence]]

$$
  \array{
     && \mathfrak{L}\mathfrak{g}
     \\
     && \downarrow
     \\
     && \mathfrak{L} \mathfrak{g}/\mathbb{R}
     \\
     & \swarrow_{\mathrlap{\omega_2}}
     \\
     B \mathbb{R}
  }
$$

which hence exhibits $\mathfrak{L} \mathfrak{g}/\mathbb{R}$ as the [[homotopy quotient]]
of $\mathfrak{L}\mathfrak{g}$ by an $\mathbb{R}$-action.


+-- {: .num_prop #FreeLoopSpaceInRarionalHomotopyTheory}
###### Proposition
**([Vigu&#233;-Sullivan 76](https://ncatlab.org/nlab/show/Sullivan+model+of+free+loop+space#VigueSullivan76),
[Vigu&#233;-Burghelea 85](https://ncatlab.org/nlab/show/Sullivan+model+of+free+loop+space#VigueBurghelea85))**

If

$$
  \mathfrak{g} = \mathfrak{l}(X)
$$

is the $L_\infty$-algebra associated by [[rational homotopy theory]]
to a  [[simply connected topological space]] $X$, then

$$
  \mathfrak{L}( \mathfrak{l}(X) )
    \simeq
  \mathfrak{l}( \mathcal{L}X )
$$

corresponds to the [[free loop space]] of $X$ and

$$
  \mathfrak{L}( \;\mathfrak{l}( X )\; )/\mathbb{R}
    \simeq
  \mathfrak{l}( \;\mathcal{L}X/S^1\; )
$$

corresponds to the [[homotopy quotient]] of the [[free loop space]] by the [[circle group]] [[action]] which rotates the loops.

The [[cochain cohomology]] of the [[Chevalley-Eilenberg algebra]]

$$
  CE(\mathfrak{l}( \;\mathcal{L}X/S^1\; ))
$$

computes the [[cyclic cohomology]] of $X$ with [[coefficients]] in $\mathbb{R}$.

(Whence "cyclification".)

Moreover the homotopy fiber sequence of the cyclification corresponds to that of the [[free loop space]]:

$$
  \left(
    \array{
      \mathcal{L}X
      \\
      \downarrow^{\mathrlap{hofib(p)}}
      \\
      \mathcal{L}X/S^1
      \\
      \downarrow^{\mathrlap{p}}
      \\
      B S^1
    }
    \;\;\;\;\;\;\;\;
  \right)
  \;\;\;\;
    \stackrel{\phantom{AA}\mathfrak{l}(-)\phantom{AA}}{\mapsto}
  \;\;\;\;
  \left(
  \array{
   \mathfrak{L} \mathfrak{l}(X)
   \\
   \downarrow^{ \mathrlap{ hofib( \mathfrak{l}(p) ) } }
   \\
   \mathfrak{L}\mathfrak{l}(X)/\mathbb{R}
   \\
   \downarrow^{\mathrlap{\mathfrak{l}(p)}}
   \\
   B \mathbb{R}
  }
    \;\;\;\;\;\;\;\;
  \right)
$$

=--

$\,$

The following gives an $L_\infty$-theoretic formalization

of "[[double dimensional reduction]]"

by which both the spacetime dimension is reduced

while at the same time the [[brane]] dimension

reduces (if [[wrapped brane|wrapping]] the reduced dimension).

$\,$

+-- {: .num_prop #DimensionalReduction}
###### Proposition
**([Fiorenza-Sati-Schreiber 16b, prop. 3.5](#FSS16b))**

For

$$
  \array{
     \widehat{\mathfrak{g}}
     \\
     \downarrow
     \\
     \mathfrak{g}
     \\
     & {}_{\mathllap{\mu_2}}\searrow
     \\
     && B \mathbb{R}
  }
$$

a [[central extension]] of [[super Lie-∞ algebras]], then the operation

of sending a super $L_\infty$-homomorphsm of the form

$$
  \widehat{\mathfrak{g}} \overset{\phi}{\longrightarrow} \mathfrak{h}
$$

to the composite

$$
  \mathfrak{g}
    \longrightarrow
  \mathfrak{L}\widehat{\mathfrak{g}}/\mathbb{R}
    \overset{\mathfrak{L}\phi/\mathbb{R}}{\longrightarrow}
  \mathfrak{L}\mathfrak{h}/\mathbb{R}
$$

gives a [[natural bijection]]

$$
  \array{
    Hom( \widehat{\mathfrak{g}}, \mathfrak{h} )
     \;&\;
      \underoverset
        {\underset{oxidation}{\longleftarrow}}
        {\overset{reduction}{\longrightarrow}}
        {\simeq}
      \;&\;
    Hom_{/B\mathbb{R}}( \mathfrak{g}, \mathfrak{L}\mathfrak{h}/\mathbb{R} )
    \\
    \\
    \left(
      \array{
        \widehat{\mathfrak{g}}
           \overset{}{\longrightarrow}
        \mathfrak{h}
      }
    \right)
      \;&\;
      \leftrightarrow
       \;&\;
    \left(
      \array{
         \mathfrak{g}
           &&
             \overset{}{\longrightarrow}
           &&
         \mathfrak{L}\mathfrak{h}/\mathbb{R}
         \\
         & {}_{\mathllap{\mu_2}}\searrow && \swarrow_{\mathrlap{\omega_2}}
         \\
         && B \mathbb{R}
      }
    \right)
  }
$$

between super $L_\infty$-homomorphisms out of the exteded super $L_\infty$-algebra $\widehat{\mathfrak{g}}$

and homomorphism out of the base $\mathfrak{g}$ into the cyclification of the original coefficients

with the latter constrained so that

the canonical 2-cocycle on the cyclification is taken to the 2-cocycle classifying the given extension.

=--

It is straightforward, if somewhat tedious, to check this explicitly.

+-- {: .num_remark}
###### Remark

  The general theory of [[adjoint functors]]  provides insight as to the geometric nature of the
  super $L_\infty$-algebraic formalization of dimensional reduction  from prop. \ref{DimensionalReduction}.
  Namely given any pair of [[adjoint functors]] $L \dashv R$, then there is a canonical
  natural morphism $\eta_x : x \to R L x$ (called the _[[unit of an adjunction|unit of the adjunction]]_) such that
  the [[natural bijection]] between [[hom-sets]]
  $$
    \mathrm{Hom}(L x, y) \overset{\simeq}{\longrightarrow} \mathrm{Hom}(x,R x)
  $$
  is given by sending any morphism of the form $\phi : L x \to y$ to the composite
  $$
    x \overset{\eta_x}{\longrightarrow} R L x
     \overset{R \phi}{\longrightarrow}
    R y
    \,.
  $$
  Specified to the situation in Prop. \ref{DimensionalReduction}, this means that the [[double dimensional reduction]]
  of a super $L_\infty$-homomorphism
  $$
    \widehat{\mathfrak{g}} \overset{\phi}{\longrightarrow} \mathfrak{h}
  $$
  on a central $\mathbb{R}$-extension $\widehat{\mathfrak{g}}$ of some super $L_\infty$-algebra $\mathfrak{g}$ is the following composite:
  $$
    \mathfrak{g}
      \overset{\eta_{\mathfrak{g}}}{\longrightarrow}
    \mathfrak{L} \widehat{\mathfrak{g}} / \mathbb{R}
      \overset{\mathfrak{L}(\phi)/\mathbb{R}}{\longrightarrow}
    \mathfrak{L}\mathfrak{h}/\mathbb{R}
    \,.
  $$
  In terms of the geometric interpretation via [[rational homotopy theory]]
  from prop. \ref{FreeLoopSpaceInRarionalHomotopyTheory}
  the morphism $\eta_{\mathfrak{g}}$ here has the following interpretation:

  Let $\widehat X \to X$ be a principal circle bundle. Then there is a map
  $$
    X \longrightarrow \mathcal{L}\widehat X/ S^1
  $$
  which sends each point of $X$ to the loop that winds around the circle fiber over that point, at unit speed.
  As a map to the free loop space $\mathcal{L}\widehat{X}$ this would not be well defined unless the circle bundle
  were trivial, because by definition of principal circle bundles its fibers are identified with the typical
  fiber (the circle) only up to rigid rotation of that circle. But this is precisely the relation that is
  divided out by passing to the cyclified space $\mathfrak{L}\widehat{X}/S^1$, which makes the above well defined.

  Hence given any map of spaces $\widehat{X} \overset{f}{\longrightarrow} H$
  we may pass to the induced map on loops in $\widehat{X}$ modulo rigid rotation, and then
  precompose with the above fiber-assigning map
  $$
    X
      \longrightarrow
    \mathcal{L}\widehat{X}/S^1
      \overset{\mathcal{L}f/S^1}{\longrightarrow}
    \mathcal{L}H/S^1
    \,.
  $$
  Under the Quillen-Sullivan functor from spaces to their associated $L_\infty$-algebras in rational homotopy theory,
  this is the $L_\infty$-algebraic construction above.

  And this shows just how this formalizes the intuitive picture of dimensional reduction.
  For let $\Sigma_{p+1}$ be a manifold of dimension $p+1$
  and let $\Sigma_{p+1} \longrightarrow X$ be the worldvolume of some $p$-brane in $X$. Thinking of
  $f : \widehat{X} \to H$
  as classifying a background field for $(p+1)$-branes on $\widehat{X}$
  (for instance for $H = K(\mathbb{Z},p+3)$, the classifying space for ordinary cohomology)
  then the dimensionally reduced coupling term is given by the composite
  $$
    \Sigma_{p+1}
      \longrightarrow
    X
      \longrightarrow
    \mathcal{L}\widehat{X}/S^1
      \overset{\mathcal{L}f/S^1}{\longrightarrow}
    \mathcal{L}H/S^1
    \,.
  $$
  To see what this does, consider what happens locally over some chart $U$ on which the circle extension $\widehat{X} \to X$
  is topologically trivial. Then by the adjunction $S^1 \times (-) \dashv [S^1,-] = \mathcal{L}(-)$ this is equivalently
  the composite
  $$
    \Sigma_{p+1} \times S^1
      \longrightarrow
    \widehat U
      \overset{f|_U}{\longrightarrow}
    H
    \,.
  $$
  But this is nothing than the value of the background field $f$ not on the $p$-brane worldvolume
  $\Sigma_{p+1}$, but on the worldvolume $\Sigma_{p+1} \times S^1$ of a $(p+1)$-brane, which
  "[[wrapped brane|wraps]]" the circle fiber in $\widehat U = U \times S^1$.
  This is the physical picture of [[double dimensional reduction]].

=--

For entertainment of the homotopy theory cognoscenti, I mention that this formalization of
[[double dimensional reduction]] from prop. \ref{DimensionalReduction} is but a special
case of the following very general fact in [[(∞,1)-topos theory]].

+-- {: .num_prop}
###### Proposition

Let $G$ be an [[∞-group]] in an [[(∞,1)-topos]] $\mathbf{H}$
then there is a pair of [[adjoint ∞-functors]] of the form

$$
  \mathbf{H}
    \underoverset
      {\underset{[G,-]/G}{\longrightarrow}}
      {\overset{hofib}{\longleftarrow}}
      {\bot}
  \mathbf{H}_{/\mathbf{B}G}
  \,,
$$


where $[G,-]]$ denotes the [[internal hom]] in $\mathbf{H}$, $[G,-]/G$ denotes the
[[homotopy quotient]] by the [[conjugation action|conjugation]]
[[∞-action]] for $G$ equipped with its canonical [[∞-action]] by left multiplication and the argument
regarded as equipped with its trivial $G$-$\infty$-action.

=--

+-- {: .proof #DimensionalReductionAbstractly}
###### Proof


First observe that the [[conjugation action]] on $[G,X]$ is the [[internal hom]] in
the [[(∞,1)-category]] of $G$-[[∞-actions]] $Act_G(\mathbf{H})$.
Under the [[equivalence of (∞,1)-categories]]

$$
  Act_G(\mathbf{H}) \simeq \mathbf{H}_{/\mathbf{B}G}
$$

(from [Nikolaus-Schreiber-Stevenson 12](#NSS12)) then $G$ with its canonical [[∞-action]] is $(\ast \to \mathbf{B}G)$
and $X$ with the trivial action is $(X \times \mathbf{B}G \to \mathbf{B}G)$.

Hence

$$
  [G,X]/G
    \simeq
  [\ast, X \times \mathbf{B}G]_{\mathbf{B}G}
  \;\;\;\;\;
  \in
   \mathbf{H}_{/\mathbf{B}G}
  \,.
$$

Actually, this is the very definition of what $[G,X]/G \in \mathbf{H}_{/\mathbf{B}G}$ is to mean in the first place, abstractly.

But now since the [[slice (∞,1)-topos]] $\mathbf{H}_{/\mathbf{B}G}$ is itself cartesian closed, via

$$
  E \times_{\mathbf{B}G}(-)
  \;\;\;
   \dashv
  \;\;\;
  [E,-]_{\mathbf{B}G}
$$

it is immediate that
there is the following sequence of [[natural equivalences]]

$$
  \begin{aligned}
   \mathbf{H}_{/\mathbf{B}G}(Y, [G,X]/G)
   & \simeq
   \mathbf{H}_{/\mathbf{B}G}(Y, [\ast, X \times \mathbf{B}G]_{\mathbf{B}G})
   \\
   & \simeq
   \mathbf{H}_{/\mathbf{B}G}(
     Y \times_{\mathbf{B}G} \ast,
     \underset{p^\ast X}{\underbrace{X \times \mathbf{B}G }}
  )
  \\
  & \simeq
  \mathbf{H}(
     \underset{hofib(Y)}{\underbrace{p_!(Y \times_{\mathbf{B}G} \ast)}},
     X
  )
  \\
  & \simeq
  \mathbf{H}(hofib(Y),X)
  \end{aligned}
$$

Here $p \colon \mathbf{B}G \to \ast$ denotes the terminal morphism and $p_! \dashv p^\ast$
denotes the [[base change]] along it.



=--




$\,$

## Dualities
 {#Dualities}

$\,$

We discuss now how

by repeatedly applying

the super $L_\infty$-algebraic dimensional reduction/oxidation isomorphism of prop. \ref{DimensionalReduction}

to the descended cocycles from the [[schreiber:brane bouquet]]

yields super $L_\infty$-algebraic equivalences

that reflect the pertinent [[dualities in string theory]]

1. between [[M-theory]] and [[type IIA string theory]];

1. between [[type IIA string theory]] and [[type IIB string theory]] ([[T-duality]])

1. between [[type IIB string theory]] and [[F-theory]].

$\,$

### M/IIA

+-- {: .num_prop}
###### Proposition
([Fiorenza-Sati-Schreiber 16a, section 3](#FSS16a))


The cyclification of the M-brane coefficient $\mathfrak{l}(S^4)$

is the truncated IIA F1/D-brane coefficient $\mathfrak{l}( KU\langle 0,6 \rangle ( B U(1) )$

with an extra twist for the [[NS5-brane]]:

$$
  CE\left(
    \mathfrak{L} S^4 / \mathbb{R}
  \right)
  \;\simeq\;
  CE\left(\,
     \underset{\text{F1/Dp-branes}}{\underbrace{
     \mathfrak{l}(KU\langle 0,6\rangle/B U(1))
     }}
     \,
  \right)
  \underset{\text{NS5-brane}}{\underbrace{
    [h_7]/(d h_7 = \omega_2 \wedge \omega_6 - \omega_4 \wedge \omega_4)
  }}
  \,.
$$


Under this identification

the $L_\infty$-theoretic dimensional reduction according to prop. \ref{DimensionalReduction}

of the unified M-brane cocycle $\mu_{M2/M5}$ of prop. \ref{MBraneDescent}

along the M-theory extension from example \ref{D0Cocycle}

is the unified type IIA F1/D-brane cocycle from prop. \ref{DescentOfIIACocycles}:

$$
  \array{
    11d, N = 1 && \mathbb{R}^{10,1\vert \mathbf{32}}  &\overset{\mu_{M2/M5}}{\longrightarrow}& \mathfrak{l}(S^4)
    \\
    && \downarrow
    \\
    10d, \text{type IIA} && \mathbb{R}^{9,1\vert \mathbf{16}+ \overline{\mathbf{16}}}
     &\overset{ \mathfrak{L}(\mu_{M2/M5})/\mathbb{R}  }{\longrightarrow}&
    \mathfrak{l}(\mathcal{L}S^4/S^1)
    \\
    && & {}_{\mathllap{\mu^{A}_{F1/D{\leq 4}}}}\searrow & \downarrow
    \\
    && && \mathfrak{l}( KU\langle 0,6\rangle/B U(1) )
  }
$$


=--





### IIA/IIB

(...)

[FSS16b, sections 5 and 6](#FSS16b)

(...)


### IIB/F

(...)

[FSS16b, section 7](#FSS16b)

(...)

























## Summary

(...)

old [[brane scan]]


| $\stackrel{d}{=}$ |  $p =$ | 1 | 2 | 3 | 4 | 5 | 6 | 7 |  8 |  9 |
|--|--------|---|---|---|---|---|---|---|----|----|
| 11 | |  |  [[M2-brane|M2]] |  |   |  |   |   |   |   |
| 10 |  | [[F1-brane|F1]]   |   |  |   | [[NS5-brane|NS5]] |   |   |   |   |
| 9 | |   |   |  | $\ast$  |  |   |   |   |   |
| 8 | |   |   | $\ast$ |   |  |   |   |   |   |
| 7 | |   | $\ast$  |  |   |  |   |   |   |   |
| 6 | |  $\ast$  |  | [[3-brane in 6d|S3]] |   |  |   |   |   |   |
| 5 | |  | $\ast$   | |   |  |   |   |   |   |
| 4 | | $\ast$  | [[super 2-brane in 4d|M2]]$_{cmp}$   | |   |  |   |   |   |   |
| 3 | | [[super 1-brane in 3d|F1]]$_{cmp}$  |  | |   |  |   |   |   |   |

$\,$

(...)

the completed brane scan

(...)

[[!include brane scan]]

(...)


<div style="float:left;margin:0 10px 10px 0;"><img src="https://ncatlab.org/schreiber/files/BraneBouquetWithDualities.jpg" alt="the brane bouquet" /></div>

## References

The interpretation of [[Fierz identities]] as relations satisfied by [[Clebsch-Gordan coefficients]] in the [[representation ring]] of the [[spin group]] originates in

* {#DAuriaFreMainaRegge82} [[Riccardo D'Auria]], [[Pietro Fré]],  E. Maina, [[Tullio Regge]]  _A New Group Theoretical Technique for the Analysis of Bianchi Identities and Its Application to the Auxiliary Field Problem of $D=5$ Supergravity_, Annals Phys. 139 (1982) 93 ([doi:10.1016/0003-4916(82)90007-0](http://dx.doi.org/10.1016/0003-4916(82)90007-0), [spire](http://inspirehep.net/record/167640/))

where it was applied to $Spin(4,1)$, relevant in [[5-dimensional supergravity]].

By this method the Fierz identities for $Spin(9,1)$ (relevant in [[heterotic supergravity]] and [[type II supergravity]]) are discussed in

* {#DAuriaFre82a} [[Riccardo D'Auria]], [[Pietro Fré]], _Geometric Structure of $N=1, D=10$ and $N=4, D=4$ Super Yang-Mills Theory_, Nucl. Phys. B196 (1982) 205 ([spire](http://inspirehep.net/record/167639))

see also appendix C of

* [[José Figueroa-O'Farrill]], Emily Hackett-Jones, George Moutsopoulos, _The Killing superalgebra of ten-dimensional supergravity backgrounds_, Class.Quant.Grav.24:3291-3308,2007 ([arXiv:hep-th/0703192](http://arxiv.org/abs/hep-th/0703192))

and the Fierz identities for $Spin(10,1)$ (relevant in [[11-dimensional supergravity]]) were tabulated in

* {#DAuriaFre82b} [[Riccardo D'Auria]], [[Pietro Fré]], pages 12, 13 of _[[GeometricSupergravity.pdf:file]]_, Nuclear Physics B201 (1982) ([[GeometricSupergravityErrata.pdf:file]])

see also

* S. Naito, K. Osada, T. Fukui, _Fierz Identities and Invariance of Eleven-dimensional Supergravity Action_, Phys.Rev. D34 (1986) 536-552 ([spire](http://inspirehep.net/record/236376/?ln=de))

A textbook account of the representation ring method and summary of these results is in

* {#CDF} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], chapter II.8 of _[[Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991)

See also

* C. C. Nishi, _Simple derivation of general Fierz-type identities_,  	Am. J. Phys. 73 (2005) 1160-1163 ([arXiv:hep-ph/0412245](http://arxiv.org/abs/hep-ph/0412245))

From the point of view of [[division algebras and supersymmetry]]
the Fierz identities that give the vanishing of trilinear and of quadratic terms in spinors in certain dimensions are discussed in

* [[John Huerta]], section 2.4 _Division Algebras, Supersymmetry and Higher Gauge Theory_ ([arXiv:1106.3385](http://arxiv.org/abs/1106.3385))


The recognition of some [[Fierz identities]] as cocycle conditions defining the [[higher WZW terms]] of the [[super p-branes]] is due to

* {#HenneauxMezincescu85} [[Marc Henneaux]], Luca Mezincescu, _A Sigma Model Interpretation of Green-Schwarz Covariant Superstring Action_, Phys.Lett. B152 (1985) 340 ([web](http://inspirehep.net/record/15922?ln=en))

* {#BergshoeffSezginTownsend87}  [[Eric Bergshoeff]], [[Ergin Sezgin]], [[Paul Townsend]], _Supermembranes and eleven dimensional supergravity_, Phys.Lett. B189 (1987) 75-78, In [[Mike Duff]],  (ed.), _[[The World in Eleven Dimensions]]_ 69-72 ([pdf](http://streaming.ictp.trieste.it/preprints/P/87/010.pdf), [spire](http://inspirehep.net/record/248230?ln=en))

* {#AETW87} Anna Ach&#250;carro, [[Jonathan Evans]], [[Paul Townsend]], [[David Wiltshire]], _Super $p$-Branes_, Phys. Lett. B **198** (1987) 441 ([spire](http://inspirehep.net/record/22286?ln=en), [pdf](https://ir.canterbury.ac.nz/xmlui/bitstream/handle/10092/9041/12616571_pbrane.pdf?sequence=1&isAllowed=y))

* {#BLNPST97} [[Igor Bandos]], [[Kurt Lechner]], Alexei Nurmagambetov, [[Paolo Pasti]], [[Dmitri Sorokin]], Mario Tonin, _Covariant Action for the Super-Five-Brane of M-Theory_, Phys. Rev. Lett. 78 (1997) 4332-4334 ([arXiv:hep-th/9701149](http://arxiv.org/abs/hep-th/9701149))

The identification of the [[worldvolume]] [[conformal field theories]] on solitonic branes ([[black branes]])
as the [[perturbation theory]] of fundamenal [[super p-branes]] about asymptotic singular loci in [[BPS state]]
[[supergravity]] solutions is due to

* {#ClausKalloshProeyen97} Piet Claus, [[Renata Kallosh]], [[Antoine Van Proeyen]], _M 5-brane and superconformal $(0,2)$ tensor multiplet in 6 dimensions_, Nucl.Phys. B518 (1998) 117-150 ([arXiv:hep-th/9711161](http://arxiv.org/abs/hep-th/9711161))

* {#ClausKalloshKumarTownsend98} Piet Claus, [[Renata Kallosh]], J. Kumar, [[Paul Townsend]], [[Antoine Van Proeyen]], _Conformal Theory of M2, D3, M5 and 'D1+D5' Branes_, JHEP 9806 (1998) 004 ([arXiv:hep-th/9801206](http://arxiv.org/abs/hep-th/9801206))

* {#AFFFTT98} Gianguido Dall'Agata, Davide Fabbri, Christophe Fraser, [[Pietro Fré]], Piet Termonia, Mario Trigiante, _The $Osp(8|4)$ singleton action from the supermembrane_, Nucl.Phys.B542:157-194, 1999 ([arXiv:hep-th/9807115](http://arxiv.org/abs/hep-th/9807115))

* {#PastiSorokinTonin99} [[Paolo Pasti]], [[Dmitri Sorokin]], Mario Tonin, _Branes in Super-AdS Backgrounds and Superconformal Theories_, Talk given by D.S. at the International Workshop ``Supersymmetry and Quantum Symmetries'', JINR, Dubna, Russia, July 26-31, 1999 ([arXiv:hep-th/9912076](http://arxiv.org/abs/hep-th/9912076))






The bosonic [[string Lie 2-algebra]] is discussed in the appendix of

* {#BCSS05} [[John Baez]], Alissa Crans, [[Urs Schreiber]], [[Danny Stevenson]], _From loop groups to 2-groups_, Homology Homotopy Appl. Volume 9, Number 2 (2007), 101-135. ([arXiv:math/0504123](https://arxiv.org/abs/math/0504123))

Its role in [[Green-Schwarz anomaly cancellation]] is discussed in

* {#SatiSchreiberStasheff12} [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _[[schreiber:Twisted Differential String and Fivebrane Structures]]_, Communications in Mathematical Physics, Volume 315, Issue 1 (2012)  ([arXiv:0910.4001](http://arxiv.org/abs/0910.4001))

and its role in the flux quantization of the [[supergravity C-field]] in

* {#FiorenzaSatiSchreiber12a} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The moduli 3-stack of the C-field]]_, Communications in Mathematical Physics, Volume 333, Issue 1 (2015), Page 117-151 ([arXiv:1202.2455](http://arxiv.org/abs/1202.2455))

and

* {#FiorenzaSatiSchreiber12b} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:7d Chern-Simons theory and the 5-brane|Multiple M5-branes, String 2-connections, and 7d nonabelian Chern-Simons theory]]_, Advances in Theoretical and Mathematical Physics, Volume 18, Number 2 (2014)  ([arXiv:1201.5277](http://arxiv.org/abs/1201.5277))



Our discussion of [[L-infinity algebra cohomology]] is due to

* {#SatiSchreiberStasheff08} [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _L-infinity algebra connections and applications to String- and Chern-Simons n-transport_, in Quantum Field Theory, Birkh&#228;user (2009) 303-424 ([arXiv:0801.3480](http://arxiv.org/abs/0801.3480))


The observation of the [[schreiber:brane bouquet]] in super $L_\infty$-algebra and the general construction of [[higher WZW terms]] from higher $L_\infty$-cocycles is due to

* {#FSS13} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]],   _[[schreiber:The brane bouquet|Super Lie n-algebra extensions, higher WZW models and super p-branes with tensor multiplet fields]]_ International Journal of Geometric Methods in Modern Physics Volume 12, Issue 02 (2015) 1550018, ([arXiv:1308.5264](http://arxiv.org/abs/1308.5264))

The homotopy-[[descent]] of the [[M5-brane]] cocycle and of the type IIA [[D-brane]] cocycles is due to

* {#FSS15} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The WZW term of the M5-brane|The WZW term of the M5-brane and differential cohomotopy]]_, J. Math. Phys. 56, 102301 (2015) ([arXiv:1506.07557](https://arxiv.org/abs/1506.07557))

* {#FSS16a} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Rational sphere valued supercocycles in M-theory]]_, Journal of Geometry and Physics, Volume 114 (2017) ([arXiv:1606.03206](http://arxiv.org/abs/1606.03206))

The derivation of supersymmetric [[topological T-duality]], rationally, and of the higher super Cartan geometry for [[super T-folds]] is due to

* {#FSS16b} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:T-Duality from super Lie n-algebra cocycles for super p-branes]]_ ([arXiv:1611.06536](https://arxiv.org/abs/1611.06536))

The derivation of the process of higher invariant extensions that leads from the [[superpoint]] to [[11-dimensional supergravity]]:

* {#MTheoryFromTheSuperpoint} [[John Huerta]], [[Urs Schreiber]], _[[schreiber:M-Theory from the Superpoint]]_

General discussion of [[twisted cohomology]] is in

* {#NSS12} [[Thomas Nikolaus]], [[Urs Schreiber]], [[Danny Stevenson]], _[[schreiber:Principal ∞-bundles -- theory, presentations and applications|Principal ∞-bundles -- General theory]]_, Journal of Homotopy and Related Structures, Volume 10, Issue 4 (2015) ([arXiv:1207.0248](http://arxiv.org/abs/1207.0248))

A textbook account of much of the story is in

* {#dcct} [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_, Thesis



