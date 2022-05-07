
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

### Broad idea

The _Green-Schwarz action functional_ is an [[action functional]] for a [[sigma-model]] that describes the propagation of a fundamental super $p$-[[brane]] $\Sigma$ in a [[super spacetime]] [[supermanifold]].

* For $p = 0$ this is the **Green-Schwarz [[superparticle]]**.

* For $p = 1$ this is the **Green-Schwarz [[superstring]]** ([Green-Schwarz 84](#GreenSchwarz84))

* For $p =2$ this is the **Green-Schwarz [[supermembrane]]** ([Bergshoeff-Sezgin-Townsend 87](#BergshoeffSezginTownsend87))

The Green-Schwarz model of the superstring is in contrast to the _[[NSR-string]]_ model (the original [[spinning string]]), which has manifest [[worldsheet]] [[supersymmetry]] but no manifest spacetime supersymmetry. It is a non-trivial theorem that the spectrum of the [[NSR-string]] enjoys spacetime supersymmetry (after [[GSO projection]]) and may hence be identified with [[perturbation theory|perturbative]] excitations of a [[supergravity]] background.
The construction of the Green-Schwarz functional was motivated by the desire to find an equivalent alternative formulation in which 
spacetime supersymmetry is manifest (see e.g. [Schwarz 16, slides 24-25](#Schwarz16)). 

[[!include worldvolume-target supersymmetry of brane sigma-models]]


For more discussion see also at _[[geometry of physics -- fundamental super p-branes]]_.


### More details

[[perturbation theory|Perturbative]] [[string theory]] on geometric backgrounds is defined by the [[Neveu-Schwarz-Ramond model]], namely by [[sigma-model]] [[2d super conformal field theories]] (of [[central charge]] 15) on [[worldsheets]] $\Sigma$ that are [[super Riemann surfaces]], with [[target spaces]] $X$ that are ordinary (i.e. "bosonic") [[spacetime]] [[manifolds]].

These [[worldsheet]] [[field theories]] are induced from _[[action functionals]]_, namely from variants of the standard [[energy functional]] ([[Polyakov action]]) on the [[mapping space]] $[\Sigma,X]$ of smooth functions

$$
  \phi \;\colon\; \Sigma \longrightarrow X
$$

from the [[worldsheet]] $\Sigma$ to target [[spacetime]] $X$.

The central theorem of perturbative superstring theory 
(the no ghost theorem with [[GSO projection]]) says that the excitation spectrum of such a [[2d SCFT]] are the quanta of the [[perturbation theory|perturbations]] of a higher dimensional [[effective field theory|effective]] [[supergravity]] [[field theory]] on target spacetime, hence transforms under [[supersymmetry]] on target spacetime.

This is the fundamental prediction of the assumption of fundamental strings: 

1. assuming that the [[fundamental particles]] that run in [[Feynman diagrams]] are fundamentally (at high energy) the ground state modes of a fundamental [[string]],

1. demanding that there are [[fermion|fermionic]] particles among these, 

implies 

1. that the string must be the [[spinning string]] (have fermions in its [[worldsheet]] theory), which in turn implies...

1. that it is the [[superstring]] (worldsheet [[supersymmetry]] mixes the worldsheet bosons and fermions), precisely: the [[Neveu-Schwarz-Ramond superstring]], which then in addition implies...

1. that its [[target space]] [[effective field theory]] is a [[supergravity]] theory, hence that also the effective target space fields exhibit _local_ [[supersymmetry]] (i.e. "high energy supersymmetry", different from "low energy supersymmetry" that the [[LHC]] was looking for).

| main theorem of [[perturbative string theory|perturbative super-string theory]] |
|-------------------------------------------------------------------------------------------------|
| $ \underset{\text{spinning string}}{\underbrace{\text{fermions} \;+\; \text{strings}}} \;=\; \text{superstring} \;\Rightarrow\; \text{supergravity} $ |

The first step in this implication (identifying the [[spinning string]] as the [[superstring]]) is fairly straightforward
(in fact this is how the concept of [[supersymmetry]] was discovered in "the west", in the first place), 
but the second step (that the superstring excitations necessarily are quanta of a [[spacetime]] [[supergravity]] theory) 
appears as a miracle from the point of view of the [[Neveu-Schwarz-Ramond superstring]].
It comes out this way by non-trivial computation, but is not manifest in the theory.

In order to improve on this situation, [[Michael Green]] and [[John Schwarz]] searched for and found ([Green-Schwarz 81](#GreenSchwarz81), [Green-Schwarz 82](#GreenSchwarz82) [Green-Schwarz 84](#GreenSchwarz84), for the history see [Schwarz 16, slides 24-25](#Schwarz16)) a suitably equivalent string [[action functional]] that would manifestly exhibit [[spacetime]] [[supersymmetry]]. 
Acordingly, this is now called the _[[Green-Schwarz action functional]]_.

| [[action functional]] for [[superstring]] | manifest [[supersymmetry]] |
|----|---|
| [[Neveu-Ramond-Schwarz super-string]] | on [[worldsheet]]  |
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

(This is the _[[Nambu-Goto action]]_. It is classically equivalent to the [[Polyakov action]] which is the genuine starting point for the quantum [[Neveu-Ramond-Schwarz super-string]]. However, since, as we discuss below, the Green-Schwarz action naturally generalizes to that of other [[p-branes]] it is more natural to consider the Nambu-Goto form of the action here.)

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

1. [[WZW-term]] being a local potential for the unique (up to rescaling, if it exists) $Spin(d-1,1)$-[[invariant]] [[Lie algebra cohomology|super Lie algebra 3-cocycle]] $\mu_{F1}$ on the [[super Poincaré Lie algebra]] $\mathfrak{iso}(\mathbb{R}^{d-1,1\vert \mathbf{N}})$, with components locally given by the Gamma-matrices of the given [[Clifford algebra]] representation; in terms of the [[super vielbein]] $(e^a, \psi^\alpha)$:

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
$\mathbf{d}\mu_{F1} = 0$ and so that there is no [[left invariant differential form]] $b$ with $\mathbf{d}b = \mu_{F1}$
(beware here the left-invariance condition: there are of course non-left-invariant potentials for $\mu_{F1}$,
and in fact these are exactly the possible [[Lagrangian densities]] for the WZW action functional $S_{WZW}$).

This happens notably for 

1. $d = 10$ and $\mathbf{N} = (1,0) = \mathbf{16}$ ([[heterotic string]]) 

1. $d = 10$ and $\mathbf{N} = (2,0) = \mathbf{16} + \mathbf{16}$ ([[type IIB superstring]]) 

1. $d = 10$ and $\mathbf{N} = (1,1) = \mathbf{16} + \mathbf{16}^\ast$ ([[type IIA superstring]]). 

(It also happens in some lower dimensions, where however the corresponding [[Neveu-Schwarz-Ramond string]] develops a [[conformal anomaly]] after [[quantization]] ("non-critical strings"). This classification of cocycles is part of what has come to be known as the _[[brane scan]]_ in superstring theory, see below.)

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



## Definition

The Green-Schwarz action functionals are of the standard [[sigma-model]] form for [[target spaces]] that are [[supermanifold|super]]-[[homogeneous spaces]]  $G/H$ for $G$ a [[Lie supergroup]] and $H$ a sub-super-group, and for  [[background gauge fields]] that are
super-[[WZW model|WZW]]-[[circle n-bundles with connection]]/[[bundle gerbes]] on $G$.

* for branes on [[super Minkowski spacetime]]: $\mathfrak{g}$ is the [[super Poincaré Lie algebra]] and $\mathfrak{h}$ the [[Lorentz Lie algebra]];


These action functionals were first considered in ([Green-Schwarz 84](#GreenSchwarz84)) for [[superstrings]] in various dimensions. The full interpretation of the action functional as an higher [[Wess-Zumino-Witten theory]]-type action controled by the [[Lie algebra cohomology]] of the [[super Poincaré Lie algebra]] (or rather of the [[super translation Lie algebra]] inside it)  is due to ([Azc&#225;rraga-Townsend89](#AzcarragaTownsend89)).

* for branes on [[super anti de Sitter spacetime]], $G$ is a [[superconformal group]] (e.g. [Metsaev-Tseytlin 98, section 3](#MetsaevTseytlin98))


### Supercoordinates
 {#Supercoordinates}

We briefly review some basics of the canonical [[coordinates]] and the super [[Lie algebra cohomology]] of the [[super Poincaré Lie algebra]] and [[super Minkowski space]], which are referred to below (see for instance [Azc&#225;rraga-Townsend 89](#AzcarragaTownsend89), and see at _[[super Cartesian space]]_ and at _[[signs in supergeometry]]_.).

By the general discussion at [[Chevalley-Eilenberg algebra]], we may characterize the [[super Poincaré Lie algebra]] $\mathfrak{siso}(D-1,1)$ by its CE-algebra $CE(\mathfrak{siso}(D-1,1))$ "of [[left-invariant 1-forms]]" on its group manifold.

+-- {: .num_defn #CEAlgebraOfSuperPoincare}
###### Definition

The [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{siso}(d-1,1))$ is generated on

* elements $\{e^a\}$ and $\{\omega^{ a b}\}$ of degree $(1,even)$

* and elements $\{\psi^\alpha\}$ of degree $(1,odd)$

with the differential defined by

$$
  d_{CE} \omega^{a b} = \omega^a{}_b \wedge \omega^{b c}
$$

$$
  d_{CE} e^{a } = \omega^a{}_b \wedge e^b + \frac{i}{2}\bar \psi \Gamma^a \psi
$$

$$
  d_{CE} \psi = \frac{1}{4} \omega^{ a b} \Gamma_{a b} \psi
  \,.
$$

Removing the terms involving $\omega$ here this is the [[super translation algebra]].

=--

In this way the [[super-Poincaré Lie algebra]] and its extensions is usefully discussed for instance in ([D'Auria-Fr&#233; 82](#DAuriaFre82)) and in ([Azc&#225;rraga-Townsend 89](#AzcarragaTownsend89), [CAIB 99](#CAIB99)). In much of the literature instead the following equivalent notation is popular, which more explicitly involves the [[coordinates]] on [[super Minkowski space]].

+-- {: .num_remark }
###### Remark

The abstract generators in def. \ref{CEAlgebraOfSuperPoincare} are identified with [[left invariant 1-forms]] on the [[super-translation group]] (= [[super Minkowski space]]) as follows.

Let $(x^a, \theta^\alpha)$ be the canonical [[coordinates]] on the [[supermanifold]] $\mathbb{R}^{d|N}$ underlying the super translation group. Then the identification is

* $\psi^\alpha = d \theta^\alpha$.

* $e^a = d x^a + \frac{i}{2} \overline{\theta} \Gamma^a d \theta$.

Notice that this then gives the above formula for the differential of the [[super-vielbein]] in def. \ref{CEAlgebraOfSuperPoincare} as

$$
  \begin{aligned}
    d e^a & = d (d x^a + \frac{i}{2} \overline{\theta} \Gamma^a d \theta)
    \\
    & = \frac{i}{2} d \overline{\theta}\Gamma^a d \theta
    \\
    & = \frac{i}{2} \overline{\psi}\Gamma^a \psi
  \end{aligned}
  \,.
$$


=--


+-- {: .num_remark }
###### Remark

The term $\frac{i}{2}\bar \psi \Gamma^a \psi$ is sometimes called the *[[supertorsion]]* of the [[super-vielbein]] $e$, because the defining equation

$$
  d_{CE} e^{a } -\omega^a{}_b \wedge e^b = \frac{i}{2}\bar \psi \Gamma^a \psi
$$

may be read as saying that $e$ is [[torsion]]-free except for that term. Notice that this term is the only one that appears when the differential is applied to "Lorentz scalars", hence to object in $CE(\mathfrak{siso})$ which have "all indices contracted". (See also at _[[torsion constraints in supergravity]]_.)

Notably we have

$$
  d \left(
    \overline{\psi} \wedge \Gamma^{a_1 \cdots a_p} \psi
    \wedge e_{a_1} \wedge \cdots \wedge e_{a_p}
  \right)
  \propto
  \left(
    \overline{\psi} \wedge \Gamma^{a_1 \cdots a_p} \psi
    \wedge e_{a_1} \wedge \cdots \wedge e_{a_{p-1}}
  \right)
  \wedge
  \left(
    \overline{\Psi} \wedge \Gamma_{a_p} \Psi
  \right)
  \,.
$$

This remaining operation "$e \mapsto \Psi^2$" of the differential acting on Loretz scalars is sometimes denoted "$t_0$", e.g. in ([Bossard-Howe-Stelle 09, equation (8)](#BossardHoweStelle09)).

This relation is what govers all of the exceptional super Lie algebra cocycles that appear as WZW terms for the Green-Schwarz action below: for some combinations of $(D,p)$ a [[Fierz identity]] implies that the term

$$
  \left(
    \overline{\psi} \wedge \Gamma^{a_1 \cdots a_p} \psi
    \wedge e_{a_1} \wedge \cdots \wedge e_{a_{p-1}}
  \right)
  \wedge
  \left(
    \overline{\Psi} \wedge \Gamma_{a_p} \Psi
  \right)
$$

vanishes identically, and hence in these dimensions the term

$$
    \overline{\psi} \wedge \Gamma^{a_1 \cdots a_p} \psi
    \wedge e_{a_1} \wedge \cdots \wedge e_{a_p}
$$

is a [[cocycle]]. See also the [brane scan](#BraneScan) table below.

=--


### Kinetic term

(...)

[[kinetic action]]

$$
  \int_\Sigma \langle \phi^\ast\Pi^a, \phi^\ast \Pi^b \eta_{a b}\rangle
$$

(...)

### WZW term
 {#DefinitionWZWTerm}

Let $(e^a, \omega^{a b}, \psi^\alpha)$ be the standard generators
of the [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{siso}(d,1))$ of the [[super Poincaré Lie algebra]], as discussed there.

The part of the [[Lie algebra cohomology]] of the super translation Lie algebra
that is invariant under the [[special orthogonal Lie algebra|Lorentz]]
transformations is spanned by closed elements of the form

$$
  \mu =
  (d \bar \theta \Gamma_{a_1, \cdots, a_p} \wedge d \theta)
  \wedge
  \Pi^{a_1} \wedge \cdots \wedge \Pi^{a_p}
  \,.
$$

These exist (are closed) only for certain combinations of
$d$ and $p$. The possible values are listed [below](#BraneScan).

For a bosonic [[WZW model]] the [[background gauge field]]
induced by such a cocycle would be the corresponding [[Lie integration]]
to a [[circle n-bundle with connection]]. Here, since the super
translation group is contractible, a [[Poincaré lemma]] applies
and these circle $n$-connections are simply given by globally
defined [[connection on an infinity-bundle|connection]] form
$\beta$ satisfying

$$
  d \beta = \mu
  \,.
$$

The WZW part of the GS action is then

$$
  S_{WZW } : \phi \mapsto \int_\Sigma \phi^* \beta
$$

(...)


## Properties

### Siegel- or $\kappa$-symmetry
 {#KappaSymmetry}

The Green-Schwarz action has an extra fermionic symmetry, on top of the genuine supersymmetry, first observed in ([Siegel 83](#Siegel83)) for the [[superparticle]] and in ([Siegel 84](#Siegel84)) for the [[super 1-brane in 3d]], and finally in ([GreenSchwarz 84](#GreenSchwarz)) for the critical superstring in 10-dimensions. This is also called **[[kappa-symmetry]]**. It has a natural interpretation in terms of the [[supergeometry|super]]-[[Cartan geometry]] of [[target space]] ([McArthur](#McArthur), [GKW](#GKW)). Discussion from the point of view of the [[D'Auria-Fré formulation of supergravity]] is in ([AFFFTT 98, section 3](#AFFFTT98), [Fr&#233;-Grassi 07, section 2.2](#FreGrassi07)).



### Dimensions -- the brane scan
 {#BraneScan}

The Green-Schwarz action functional of a $p$-brane propagating on an $d$-dimensional target spacetimes makes sense only for special combinations of $(p,d)$, for which there are suitanble [[Lie algebra cohomology|super Lie algebra cocycles]] on the super translation Lie algebra
(see [above](#DefinitionWZWTerm)).

The corresponding table has been called the **brane scan** in the literature, now often called the "old brane scan", since it has meanwhile been further completed (see below). In ([Duff 87](#Duff87)) the "old brane scan" is displayed as follows.

<img src="https://ncatlab.org/nlab/files/DuffBraneScan.jpg" height="500">

In the $D = 10$-row we see the critical [[superstring]] of [[string theory]] and
its [[electric-magnetic duality|magnetic dual]], the [[NS5-brane]].
The top row shows the [[M2-brane]] in [[11-dimensional supergravity]].

Moving down and left the diagonals corresponds to _[[double dimensional reduction]]_.


+-- {: .num_remark }
###### Remark

The first non-empty column of the table is a reflection of the exceptional isomorphisms of the [[spin group]] in low dimensions and the [[normed division algebras]]:

[[!include exceptional spinors and division algebras -- table]]

=--

+-- {: .num_remark }
###### Remark

What is missing in the "old brane scan" are the [[D-branes]] in $D = 10$ and the [[M5-brane]] in $D = 11$ (See also [BPST](#BPST)).
The reason is that the M5 corresponds to a 7-cocycle not on the ordinary [[super Poincaré Lie algebra]], but on its [[infinity-Lie algebra cohomology|L-infinity algebra extension]], the [[supergravity Lie 3-algebra]]. The completion in [[super L-infinity algebra]] theory is discussed in ([FSS 13](#FiorenzaSatiSchreiber13)), as _[[schreiber:The brane bouquet]]_.

=--


So (with notation as [above](#Supercoordinates)) we have the following.

[[!include brane scan]]


### On curved spacetime and supergravity equations of motion
 {#OnCurvedSpacetime}


In the [[first order formulation of gravity]]
a [[field (physics)|field]] configuration on a [[spacetime]]
[[manifold]] $X$ is a [[Cartan connection]]

$$
  \nabla \colon X \to \mathbf{B} SuperPoincare(d-1,1)_{conn}
$$

hence a [[principal connection]] for the [[super Poincaré group]] such such that at each point $x \in X$ it identifies the [[tangent space]] with $\mathbb{R}^{d;N} = \mathfrak{siso}(d-1,1)/\mathfrak{o}(d-1,1)$

$$
  T_x X \stackrel{\nabla}{\longrightarrow}
  \mathfrak{siso}(d-1,1)
  \longrightarrow
  \mathbb{R}^{d;N}
  \,.
$$

Hence given a [[Lie algebra cocycle]]

$$
  \mathfrak{g} \longrightarrow \mathbb{R}[2]
$$

as for the Green-Schwarz superstring we can [[pullback of differential forms|pull it back]] along this [[Cartan connection]] to a [[differential 3-form]] on [[spacetime]].

In general this 3-form is no longer _closed_. If it is closed, then the Green-Schwarz superstring is again well defined on $(X,\nabla)$ as a [[WZW model]].

 The claim now is that requiring this 3-form still to be closed is, as a condition on the field of [[gravity]] $\nabla$, precisely the [[equations of motion]] of [[supergravity]] (the super-[[Einstein equations]]).

This is due to ([Nilsson 81](#Nilsson81), [Bergshoeff-Sezgin-Townsend 86](#BergshoeffSezginTownsend86)) and others, see the references [below](#ReferencesSupergravityBackgroundEquationsOfMotion).

#### Membrane in 11d SuGra background
 {#MembraneIn11dSuGraBackground}

For the [[membrane]]([[M2-brane]]) in a background of [[11-dimensional supergravity]] ([Bergshoeff-Sezgin-Townsend 87](#BergshoeffSezginTownsend87))
find that consistency requires that (in a given [[coordinate chart]] with [[super-vielbein field]] $(E^A) = (E^a, \Psi^\alpha)$) the 4-form flux is of the form


\[
  \label{HConstraintEquationForMembraneIn11d}
  \begin{aligned}
     H & = \overline{\Psi}\wedge\Gamma^{ab} \Psi \wedge E_a \wedge E_b + \mathbf{d}C_3
     \\
     & =
     \Gamma_{a b \alpha \beta} E^a \wedge E^b \wedge E^\alpha \wedge E^\beta +
    \mathbf{d}C_3
  \end{aligned}
\]

where the first summand is the super-Lie algebra cocycle that classifies the [[supergravity Lie 3-algebra]] and the second is the [[field strength]] of the [[supergravity C-field]] proper (hence a purely bosonic differential form). In the second line we have rewritten this more manifestly in terms of the [[super-vielbein]] $(E^A) = (E^a, E^\alpha) = (E^a, \Psi^\alpha)$, this way the expression is directly analogous to that of definite 3-forms in the theory of [[G2-manifolds]] (see [this example](G2+manifold#DefiniteFormsInTermsOfVielbeinFields) for details).

Moreover the [[torsion]] tensor $T$ is to have its $(T^a)^\alpha{}_\beta$-component equal to $(\Gamma^a)^\alpha{}_\beta$, see at _[[torsion constraints in supergravity]]_.

In addition the [[Bianchi identities]] have to hold:

* $\nabla T^A = E^B \wedge R_{B}{}^{A}$

* $\nabla H = 0$ ([[covariant derivative|covariant constancy]]).

All this is implied by the [[equations of motion]] of [[11-dimensional supergravity]].

Notice that in view of the above analogy to [[G2-structure]], the covariant constancy condition is precisely the analog of [[G2-manifold]] structure.

Discussion of this in the somewhat more streamlined [[D'Auria-Fré formulation of supergravity]] is in ([AFFFTT 98, section 3.1](#AFFFTT98)).

#### Heterotic string

Discussion that for the GS-version of the [[heterotic string]] consistency of the background is equivalent to the equations of motion of [[heterotic supergravity]] is in  ([Shapiro-Taylor 87](#ShapiroTaylor87)).

Discussion with the hetetoric gauge field included is in ([Atick-Dhar-Ratra 86](#AtickDharRatra86)).


#### Type II string

Discussion for the GS-version of the [[type II superstring]] in [[type II supergravity]]-backgrounds is in ([GHMNT 85](#GHMNT85)), and for the [[D-branes]] in type II in ([CGNSW 97](#CGNSW97)).


### Conserved currents
 {#ConservedCurrents}

The super-WZW term of the GS action functionals is invariant under [[supersymmetry]] only up to a [[divergence]]. Hence the [[Noether theorem]] in its generality for "weak" symmetries applies and gives that the [[conserved currents]] receive an extra contribution from this divergence term. The resulting algebra is a central extension of the given [[super translation Lie algebra]], extending to the famous [polyvector extensions](super+Poincare+Lie+algebra#PolyvectorExtensions) "by brane charges" of the [[super Poincaré Lie algebra]] ([AGIT 89](#AGIT89)).

### As part of the AdS-CFT correspondence
 {#AsPartOfTheAdSCFTCorrespodence}

By the above discussion, Green-Schwarz super $p$-branes are consistent on [[superspacetimes]] that satisfy the respective higher [[supergravity]] [[equations of motion]]. These turn out to have solutions which exhibit [[black branes]] in essentially just the combinations of dimensions and supersymmetries that the original Green-Schwarz sigma-models exist in, hence they look precisely like the [[non-perturbative quantum field theory|non-perturbative]] avatars of whatever these [[sigma models]] give the [[perturbation theory]] of by [[second quantization]]. (See at [[black holes in string theory]] for more on this correspondence between branes in string perturbation theory and black branes in supergravity.)

Moreover, the near-horizon geometries of these [[black branes]] are always [[anti de Sitter spacetime]] times orthogonal directions.

Therefore it is natural to consider the perturbation of the Green-Schwarz sigma-models around their asymptotic embeddings into AdS spaces, hence effectively the perturbation theory of the degrees of freedom at those naked singularity at which the corresponding black brane sits.

After [[diffeomorphism]] [[gauge fixing]] one finds that the resulting field theories now on the $p$-brane [[worldvolumes]] are precisely the [[superconformal field theories]] for all the  [allowed superconformal supersymmetries](supersymmetry#ClassificationSuperconformalInDimgt2) (see also at _[[singleton representation]]_):

| $d$ | $N$ | [[superconformal super Lie algebra]] | [[R-symmetry]] | [[brane]] [[worldvolume]] theory |
|-----|-----|--|---|--|
| 3   |  $2k+1$ | $B(k,2) \simeq $ [[osp]]$(2k+1/4)$ | $SO(2k+1)$ | |
| 3   | $2k$ | $D(k,2)\simeq $ [[osp]]$(2k/4)$ | $SO(2k)$ | [[M2-brane]] |
| 4   | $k+1$  | $A(3,k)\simeq \mathfrak{sl}(4/k+1)$ | $U(k+1)$ | [[D3-brane]] |
| 5   |  1  | $F(4)$ | $SO(3)$  |  |
| 6   | $k$ | $D(4,k) \simeq$ [[osp]]$(8/2k)$ | $Sp(k)$  | [[M5-brane]] |

This is effectively the [[AdS-CFT correspondence]].

Detailed discussion of the above steps is in ([AFFFTT 98](#AFFFTT98), [Pasti-Sorokin-Tonin 99](#PastiSorokinTonin99)).

### Quantization

The [[quantization]] of the Green-Schwarz super $p$-brane [[sigma models]] is discussed in the literature in terms of [[light-cone gauge quantization]].

This is actually how the Green-Schwarz superstring was first introduced in ([Green-Schwarz 81](#GreenSchwarz81), [Green-Schwarz 82](#GreenSchwarz82)) before its [[general covariance|generally covariant]] formulation was found in ([Green-Schwarz 84](#GreenSchwarz84)). A textbook account of this is in ([Green-Schwarz-Witten, section 5](#GreenSchwarzWitten)).

While, by the [[brane scan]] discussed above, the action functional for the Green-Schwarz superstring exists for target [[super Minkowski spacetimes]] of dimension $d = 3$, 4, 6, and 10, its [[light-cone gauge quantization]] produces a [[quantum anomaly]] for the spacetime [[Lorentz group]] symmetry in dimension $d = 4$ and $d = 6$. For $d = 10$ the anomaly disappears and the thus quantized Green-Schwarz string becomes equivalent to the quantum [[NSR string]], hence to "the" critical string (of [[heterotic string theory]], [[type II string theory]]).

Curiously, the light-cone gauge quantization of the GS-string also does wor however for $d = 3$, see at _[[super 1-brane in 3d]]_ for more on this.

(...)


## Related entries

* [[supersymmetry]]

* [[sigma-model]], [[brane]]

  * [[relativistic particle]], [[spinning particle]], [[superparticle]]

  * [[string]], [[spinning string]], [[superstring]]

  * [[membrane]]

* [[geometry of physics -- fundamental super p-branes]]

## References

### Super-string as a GS-sigma model
 {#SuperStringAsAGSSigmaModel}

A precursor to the actual Green-Schwarz action functional is

* {#GreenSchwarz81} [[Michael Green]], [[John Schwarz]], _Supersymmetrical Dual String Theory_, Nucl. Phys. B 181 (1981) 502;

* {#GreenSchwarz82} [[Michael Green]], [[John Schwarz]], _Supersymmetrical Dual String Theory. 2. Vertices and Trees_, Nucl. Phys. B 198 (1982) 252.

which presented a [[light-cone gauge quantization]] of superstring with manifest [[target space|target]] [[spacetime]] [[supersymmetry]].

The observation that this has a [[general covariance|generally covariant]] formulation lead to what is now called the Green-Schwarz action functional proper, for the superstring:

* {#GreenSchwarz84} [[Michael Green]], [[John Schwarz]], _Covariant description of superstrings_, Phys. Lett. B136 (1984), 367&#8211;370 ([spire:193596](http://inspirehep.net/record/193596), <a href="https://doi.org/10.1016/0370-2693(84)92021-5">arXiv;10.1016/0370-2693(84)92021-5</a>)

* {#GreenSchwarz84b} [[Michael Green]], [[John Schwarz]], _Properties of the Covariant Formulation of Superstring Theories_, Nucl. Phys. B 243 (1984) 285 ([spire:196623](http://inspirehep.net/record/196623), <a href="https://doi.org/10.1016/0550-3213(84)90030-0">doi:10.1016/0550-3213(84)90030-0</a>)

See also the historical comments in

* {#Schwarz16} [[John Schwarz]], slides 24-25 of _String Theory in the Twentieth Century_, talk at [Strings 2016](http://ymsc.tsinghua.edu.cn:8090/strings/) ([pdf](http://ymsc.tsinghua.edu.cn:8090/strings/slides/8.1/Schwarz.pdf))


A standard textbook reference for the GS superstring is

* {#GreenSchwarzWitten} [[Michael Green]], [[John Schwarz]], [[Edward Witten]], volume 1, section 5 of _Superstring theory_, 3 vols. Cambridge Monographs on Mathematical Physics

and a brief paragraph in Volume II, section 10.2, page 983 of

* [[Eric D'Hoker]], _String theory -- lecture 10: Supersymmetry and supergravity_ , in part 3 of

  [[Pierre Deligne]], [[Pavel Etingof]], [[Dan Freed]], L. Jeffrey,
[[David Kazhdan]], [[John Morgan]], D.R. Morrison and [[Edward Witten]], eds.  _[[Quantum Fields and Strings]], A course for mathematicians_, 2 vols. Amer. Math. Soc. Providence 1999. ([web version](http://www.math.ias.edu/qft))

Textbook discussion of the Green-Schwarz version of the [[heterotic string]] is in 

* {#CastellaniDAuriaFre91} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], vol 3, section VI.9.7 of _[[Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991)

There is also a kind of review in

* [[Joan Simón]], _Brane Effective Actions, Kappa-Symmetry and Applications_, Living Reviews in Relativity ([arXiv:1110.2422](http://arxiv.org/abs/1110.2422))

Quantization of the Green-Schwarz string using [[pure spinors]] is discussed in

* P. A. Grassi, G. Policastro, [[Peter van Nieuwenhuizen]], _An Introduction to the Covariant Quantization of Superstrings_, Class.Quant.Grav. 20 (2003) S395-S410 ([arXiv:hep-th/0302147](https://arxiv.org/abs/hep-th/0302147))

* P.A. Grassi, Y. Oz, _Non-Critical Covariant Superstrings_ ([arXiv:hep-th/0507168](https://arxiv.org/abs/hep-th/0507168))


Review from the bigger perspective that also includes worlsheet supermanifolds is in

* {#Sorokin99} [[Dmitri Sorokin]], _Superbranes and Superembeddings_, Phys.Rept.329:1-101,2000 ([arXiv:hep-th/9906142](http://arxiv.org/abs/hep-th/9906142))

The observation that the Green-Schwarz action functional is an example of a [[WZW-model]] on [[super-Minkowski spacetime]] is due to

* {#HenneauxMezincescu85} [[Marc Henneaux]], Luca Mezincescu, _A Sigma Model Interpretation of Green-Schwarz Covariant Superstring Action_, Phys.Lett. B152 (1985) 340 ([web](http://inspirehep.net/record/15922?ln=en), <a href="https://doi.org/10.1016/0370-2693(85)90507-6">doi:10.1016/0370-2693(85)90507-6</a>)

For more references on this WZW perspective see [below](#ReferencesWZWTerm).

For references on curved backgrounds see [below](#ReferencesSupergravityBackgroundEquationsOfMotion).

[[!include fundamental M2-brane sigma-model -- references]]

### D-branes as GS-sigma models
 {#ReferencesForDBranes}

Green-Schwarz action functionals for the [[D-branes]] (including the [[DBI action]]):

* {#CGNSW96} [[Martin Cederwall]], Alexander von Gussich, [[Bengt Nilsson]], Per Sundell, Anders Westerberg, _The Dirichlet Super-p-Branes in Ten-Dimensional Type IIA and IIB Supergravity_, Nucl.Phys. B490 (1997) 179-201 ([arXiv:hep-th/9611159](http://arxiv.org/abs/hep-th/9611159))

* {#APPS97b} [[Mina Aganagic]], [[Jaemo Park]], Costin Popescu, [[John Schwarz]], _Dual D-Brane Actions_, Nucl. Phys. B496 (1997) 215-230 ([arXiv:hep-th/9702133](https://arxiv.org/abs/hep-th/9702133))

* [CAIB 99](#CAIB99)

* [Sakaguchi 00](#Sakaguchi00)




### Dualities

Discussion of [[T-duality]] for the Green-Schwarz string is in

* [[Mirjam Cvetic]], H. Lu, [[Christopher Pope]], [[Kellogg Stelle]], _T-Duality in the Green-Schwarz Formalism, and the Massless/Massive IIA Duality Map_, Nucl.Phys.B573:149-176,2000 ([arXiv:hep-th/9907202](https://arxiv.org/abs/hep-th/9907202))

* Bogdan Kulik, Radu Roiban, _T-duality of the Green-Schwarz superstring_, JHEP 0209 (2002) 007 ([arXiv:hep-th/0012010](https://arxiv.org/abs/hep-th/0012010))

* {#BandosJulia03} [[Igor Bandos]], [[Bernard Julia]], _Superfield T-duality rules_, JHEP 0308 (2003) 032 ([arXiv:hep-th/0303075](https://arxiv.org/abs/hep-th/0303075))

  reviewed in _Superfield T-duality rules in ten dimensions with one isometry_ ([arXiv:hep-th/0312299](https://arxiv.org/abs/hep-th/0312299))


### WZW terms, super Lie algebra cohomology and the brane scan
 {#ReferencesWZWTerm}

The WZW nature of the second term in the GS action, recognized in ([Henneaux-Mezincescu 85](#HenneauxMezincescu85)) is
discussed in

* {#Rabin87} [[Jeffrey Rabin]], _Supermanifold Cohomology and the Wess-Zumino Term of the Covariant Superstring Action_, Commun Math. Phys. 108, 375-389 (1987) ([Euclid:1104116532](https://projecteuclid.org/euclid.cmp/1104116532))

* B. Milewski, _Superstrings from sigma models_,  Classical and Quantum Gravity, Volume 4, Number 3 (1987)

* A.P. Isaev, E.A. Ivanov, _On Sigma Model Formulation of Green-Schwarz Superstring_, Mod.Phys.Lett. A4 (1989) 351-359 ([spire:266793](http://inspirehep.net/record/266793), [doi:10.1142/S0217732389000423](https://www.worldscientific.com/doi/abs/10.1142/S0217732389000423)) 

* {#AzcarragaTownsend89} [[José de Azcárraga]], [[Paul Townsend]], _Superspace geometry and the classification of supersymmetric extended objects_, Physical Review Letters Volume 62, Number 22 (1989) ([spire](http://inspirehep.net/record/284635?ln=en))

an with its [[infinity-Lie theory|Lie theoretic]] meaning
made fully explicit (in "FDA" language) in

* {#AzcarragaIzquierdo95} [[José de Azcárraga]], Jos&#233; Izquierdo, chapter 8 of _Lie Groups, Lie Algebras, Cohomology and Some Applications in Physics_, Cambridge monographs of mathematical physics, (1995)


The original "brane scan" classification of GS action functionals by WZW terms:

* {#AETW87} Anna Ach&#250;carro, [[Jonathan Evans]], [[Paul Townsend]], [[David Wiltshire]], _Super $p$-Branes_, Phys. Lett. B **198** (1987) 441 ([spire:22286](http://inspirehep.net/record/22286), <a href="https://doi.org/10.1016/0370-2693(87)90896-3">doi:10.1016/0370-2693(87)90896-3</a>, [pdf](https://ir.canterbury.ac.nz/xmlui/bitstream/handle/10092/9041/12616571_pbrane.pdf?sequence=1&isAllowed=y), [[SuperpBranes.pdf:file]])

A complete rigorous classification of all the relevant cocycles on the [[super Poincaré Lie algebra]] was given in

* {#Brandt12-13} [[Friedemann Brandt]], _Supersymmetry algebra cohomology_

  _I: Definition and general structure_  J. Math. Phys.51:122302, 2010, ([arXiv:0911.2118](http://arxiv.org/abs/0911.2118))

  _II: Primitive elements in 2 and 3 dimensions_, J. Math. Phys. 51 (2010) 112303 ([arXiv:1004.2978](http://arxiv.org/abs/1004.2978))

  _III: Primitive elements in four and five dimensions_, J. Math. Phys. 52:052301, 2011 ([arXiv:1005.2102](http://arxiv.org/abs/1005.2102))

  _IV: Primitive elements in all dimensions from $D=4$ to $D=11$_, J. Math. Phys. 54, 052302 (2013) ([arXiv:1303.6211](http://arxiv.org/abs/1303.6211))



For $d = 11$ the relevant [[super Lie algebra]] [[Lie algebra cohomology|cocycles]] have also been discussed (but not related to the Green-Schwarz action functional) in

* {#DAuriaFre82} [[Riccardo D'Auria]], [[Pietro Fré]], _[[GeometricSupergravity.pdf:file]]_, Nuclear Physics B201 (1982)


A review is in

* {#Duff87} [[Michael Duff]], _Supermembranes: the first fifteen weeks_, Class. Quant. Grav. 5 (1988) 189 ([doi:10.1088/0264-9381/5/1/023](https://doi.org/10.1088/0264-9381/5/1/023), [spire:248034](https://inspirehep.net/record/248034))

from which the above table is taken.


Systematic review and discussion of the 3- and 4-cocycles in the old [[brane scan]] via the relation between [[division algebras and supersymmetry]] is in

* {#BaezHuerta10} [[John Baez]], [[John Huerta]], _Division algebras and supersymmetry II_, Adv. Math. Theor. Phys. 15 (2011), 1373-1410  ([arXiv:1003.34360](http://arxiv.org/abs/1003.3436))


See also

* I. Bars, C. Deliduman and D. Minic, Phys. Rev D59 (1999) 125004;
Phys. Lett. B457 (1999) 275. ([arXiv:hep-th/9812161](http://arxiv.org/abs/hep-th/9812161))

More along these lines is in

* [[Michael Duff]], S. Ferrara, _Four curious supergravities_ ([arXiv](http://arxiv.org/abs/1010.3173))

The Green-Schwarz-type action for the [[M5-brane]] was found in

* {#BLNPST97} [[Igor Bandos]], Kurt Lechner, Alexei Nurmagambetov, Paolo Pasti, [[Dmitri Sorokin]], Mario Tonin, _Covariant Action for the Super-Five-Brane of M-Theory_ ([arXiv:hep-th/9701149](http://arxiv.org/abs/hep-th/9701149))

* {#APPS97} Mina Aganagic, Jaemo Park, Costin Popescu, [[John Schwarz]], _World-Volume Action of the M Theory Five-Brane_ ([arXiv:hep-th/9701166](http://arxiv.org/abs/hep-th/9701166))



The 7-cocycle on the [[supergravity Lie 3-algebra]] which gives the [[supergravity Lie 6-algebra]] appears in these articles (somewhat secretly) in equation ([BLNPST, equation (9)](#BLNPST97)).

See also

* {#BPST} [[Igor Bandos]], Paolo Pasti, [[Dmitri Sorokin]], Mario Tonin, _Superbrane Actions and Geometrical Approach_ ([arXiv:hep-th/9705064](http://arxiv.org/abs/hep-th/9705064))

The 7-cocycle for the M5-brane on the [[supergravity Lie 3-algebra]] is equation (8.8) there.

The interpretation of the cocycles for the [[D-branes]] and for the [[M5-brane]] as cocycles on "[[extended super-Minkowski spacetime]]" is due to


* {#CAIB99} C. Chrysso&#8204;malakos, [[José de Azcárraga]], J. M. Izquierdo and C. P&#233;rez Bueno, _The geometry of branes and extended superspaces_, Nuclear Physics B Volume 567, Issues 1&#8211;2, 14 February 2000, Pages 293&#8211;330 ([arXiv:hep-th/9904137](http://arxiv.org/abs/hep-th/9904137))

* {#Sakaguchi00} Makoto Sakaguchi, _IIB-Branes and New Spacetime Superalgebras_, JHEP 0004 (2000) 019 ([arXiv:hep-th/9909143](https://arxiv.org/abs/hep-th/9909143))


* {#AzcarragaIzquierdo01} [[José de Azcárraga]], J. M. Izquierdo, _Superalgebra cohomology, the geometry of extended superspaces and superbranes_ ([arXiv:hep-th/0105125](http://arxiv.org/abs/hep-th/0105125))


See also _[[division algebras and supersymmetry]]_.

A corresponding refinement of the brane scan to a "brane bouquet" of [[super L-∞ algebra]] [[infinity-Lie algebra cohomology|extensions]] (hence in [[infinity-Lie theory]] via [[schreiber:∞-Wess-Zumino-Witten theory]]) is discussed in

* {#FiorenzaSatiSchreiber13} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The brane bouquet|Super Lie n-algebra extensions, higher WZW models and super p-branes with tensor multiplet fields]]_, International Journal of Geometric Methods in Modern Physics Volume 12, Issue 02 (2015) 1550018 ([arXiv:1308.5264](http://arxiv.org/abs/1308.5264))

* {#FiorenzaSatiSchreiber15} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]] _[[schreiber:The WZW term of the M5-brane and differential cohomotopy]]_, J. Math. Phys. 56, 102301 (2015) ([arXiv:1506.07557](http://arxiv.org/abs/1506.07557))


* {#FiorenzaSatiSchreiber16} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Rational sphere valued supercocycles in M-theory and type IIA string theory]]_ ([arXiv:1606.03206](http://arxiv.org/abs/1606.03206))

* [[Vincent Braunack-Mayer]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Gauge enhancement of Super M-Branes]]_ ([arXiv:1806.01115](https://arxiv.org/abs/1806.01115))


These cohomological arguments also appear in what is called the "ectoplasm" method for invariants in [[super Yang-Mills theory]] in

* G. Bossard, [[Paul Howe]], K.S. Stelle, _A note on the UV behaviour of maximally supersymmetric Yang-Mills theories_, Phys. Lett. B682:137-142 (2009) ([arXiv:0908.3883](http://arxiv.org/abs/0908.3883))
 {#BossardHoweStelle09}

* [[Paul Howe]], T. G. Pugh, K. S. Stelle, C. Strickland-Constable, _Ectoplasm with an Edge_, JHEP 1108:081,2011 ([arXiv:1104.4387](http://arxiv.org/abs/1104.4387))

* G. Bossard, [[Paul Howe]], [[Ulf Lindström]], [[Kellogg Stelle]], L. Wulff, _Integral invariants in maximally supersymmetric Yang-Mills theories_ ([arXiv:1012.3142](http://arxiv.org/abs/1012.3142))

The connection is made in

* [[Paul Howe]], O. Raetzel, [[Ergin Sezgin]], _On Brane Actions and Superembeddings_, JHEP 9808 (1998) 011 ([arXiv:hep-th/9804051](http://arxiv.org/abs/hep-th/9804051))


The other brane scan, listing consistent asymptotic AdS geometries is due to

* M.P. Blencowea, [[Mike Duff]], _Supersingletons_, Physics letters B, Volume 203, Issue 3, 31 March 1988, Pages 229&#8211;236 .

with further developments discussed in

* [[Michael Duff]], _Near-horizon brane-scan revived_,  Nucl. Phys. B 810:193-209,2009 ([arXiv:0804.3675](http://arxiv.org/abs/0804.3675))


### Anti de Sitter backgrounds
 {#ReferencesAdSBackgrounds}

Discussion of Green-Schwarz strings on [[super anti de Sitter spacetimes]] includes the following.

General:

* {#HatsudaSakaguchi02} Machiko Hatsuda, Makoto Sakaguchi, _Wess-Zumino term for AdS superstring_, Phys.Rev. D66 (2002) 045020 ([arXiv:hep-th/0205092](http://arxiv.org/abs/hep-th/0205092), [doi:10.1103/PhysRevD.66.045020](https://doi.org/10.1103/PhysRevD.66.045020))

* {#HatsudaSakaguchi01} Machiko Hatsuda, Makoto Sakaguchi, _Wess-Zumino term for the AdS superstring and generalized Inonu-Wigner contraction_, Prog.Theor.Phys. 109 (2003) 853-867 ([arXiv:hep-th/0106114](http://arxiv.org/abs/hep-th/0106114))


#### $AdS_5$
 {#ReferencesAdS5Background}

The super 3-cocycle for the Green-Schwarz  [[superstring]] on the [[super anti de Sitter spacetime]] $AdS_5 \times S^5$ (i.e. on $\frac{SU(2,2 \vert 5)}{Spin(4,1)\times SO(5)}$) is originally due to 

* {#MetsaevTseytlin98} [[Ruslan Metsaev]], [[Arkady Tseytlin]], _Type IIB superstring action in $AdS_5 \times S^5$ background_, Nucl. Phys.B533:109-126, 1998 ([arXiv:hep-th/9805028](https://arxiv.org/abs/hep-th/9805028))

However, a supersymmetric trivialization of this cocycle seems to have been obtained in 

* {#RoibanSiegel00} Radu Roiban, [[Warren Siegel]], _Superstrings on $AdS_5 \times S^5$ supertwistor space_, JHEP 0011:024, 2000 ([arXiv:hep-th/0010104](https://arxiv.org/abs/hep-th/0010104))

see [Hatsuda-Sakaguchi 02, around (1.2) and (2.6)](#HatsudaSakaguchi02), [Hatsuda-Sakaguchi 01, around (1.2)](#HatsudaSakaguchi01)

(amplified in [arxiv:1808.04470, p. 5 and equation (5.5)](https://arxiv.org/abs/1808.04470)).

See also

* [[Gleb Arutyunov]], [[Sergey Frolov]], _Foundations of the $AdS_5 x S^5$ Superstring. Part I_, J. Phys. A 42 (2009) ([arXiv:0901.4937](http://arxiv.org/abs/0901.4937))

* [[John Schwarz]], _The $AdS_5 \times S^5$ Superstring_ ([arXiv:2004.09661](https://arxiv.org/abs/2004.09661))



#### $AdS_4$ and $AdS_7$
 {#ReferencesAdS4Background}

For the [[superstring]]:

* [[Gleb Arutyunov]], [[Sergey Frolov]], _Superstrings on $AdS_4 \times \mathbb{C}P^3$ as a Coset Sigma-model_, JHEP 0809:129,2008 ([arXiv:0806.4940](http://arxiv.org/abs/0806.4940))

* [[Pietro Fré]], [[Pietro Antonio Grassi]], _Pure Spinor Formalism for $Osp(N|4)$ backgrounds_ ([arXiv:0807.0044](http://arxiv.org/abs/0807.0044))

* [[Riccardo D'Auria]], [[Pietro Fré]], Pietro Antonio Grassi, Mario Trigiante, _Superstrings on $AdS_4 \times \mathbb{C}P^3$ from Supergravity_ ([arXiv:0808.1282](http://arxiv.org/abs/0808.1282))

* D. V. Uvarov, _$AdS_4 x \mathbb{C}P^3$ superstring in the light-cone gauge_, Nucl.Phys.B826:294-312,2010 ([arXiv:0906.4699](http://arxiv.org/abs/0906.4699))

For the [[M2-brane]]:

* {#deWitPeetersPlefkaSevrin98} [[Bernard de Wit]], [[Kasper Peeters]], [[Jan Plefka]], Alexander Sevrin, _The M-Theory Two-Brane in $AdS_4 \times S^7$ and $AdS_7 \times S^4$_, Phys.Lett. B443 (1998) 153-158 ([arXiv:hep-th/9808052](http://arxiv.org/abs/hep-th/9808052))

* Makoto Sakaguchi, Hyeonjoon Shin, Kentaroh Yoshida, _Semiclassical Analysis of M2-brane in $AdS_4 \times S^7 / \mathbb{Z}_k$_, JHEP 1012:012,2010 ([arXiv:1007.3354](http://arxiv.org/abs/1007.3354))

For the [[M2-brane]] and the [[M5-brane]]:

* {#Claus98} P. Claus, _Super M-brane actions in $adS_4 \times S^7$ and $adS_7 \times S^4$_, Phys. Rev. D59 (1999) 066003 ([arXiv:hep-th/9809045](http://arxiv.org/abs/hep-th/9809045))

* Makoto Sakaguchi, Kentaroh Yoshida, _Open M-branes on $AdS_{4/7} \times S^{7/4}$ Revisited_,  Nucl.Phys. B714 (2005) 51-66 ([arXiv:hep-th/0405109](http://arxiv.org/abs/hep-th/0405109))

### Self-dual strings in 6d

Discussion of the [[self-dual string]] in 6d as a Green-Schwarz-type sigma model includes

* Par Arvidsson, Erik Flink, [[Mans Henningson]], _Supersymmetric coupling of a self-dual string to a $(2,0)$ tensor multiplet background_, JHEP0311:015,2003 ([arXiv:hep-th/0309244](http://arxiv.org/abs/hep-th/0309244))

### General curved backgrounds and Supergravity background equations of motion
 {#ReferencesSupergravityBackgroundEquationsOfMotion}

The consistency of the Green-Schwarz action functional for the superstring in a [[supergravity]] [[background gauge field|background]] should be equivalent to the background satiyfying the [[supergravity]] [[equations of motion]]. For the superstring this is due to

* {#BergshoeffSezginTownsend86} [[Eric Bergshoeff]], [[Ergin Sezgin]], [[Paul Townsend]], _Superstring actions in $D = 3, 4, 6, 10$ curved superspace_, Phys.Lett., B169, 191, (1986) ([spire](http://inspirehep.net/record/223138/?ln=en))

and for the supermembrane due to

* {#BergshoeffSezginTownsend87}  [[Eric Bergshoeff]], [[Ergin Sezgin]], [[Paul Townsend]], _Supermembranes and eleven dimensional supergravity_, Phys.Lett. B189 (1987) 75-78, In [[Mike Duff]],  (ed.), _[[The World in Eleven Dimensions]]_ 69-72 ([spire](http://inspirehep.net/record/248230?ln=en))

with a quick re-derivation using that the [[torsion constraints in supergravity|torsion constraint in 11d supergravity]] already imples the sugra equations of motion is in

* [[Paul Howe]], [[Ergin Sezgin]], section 2.1 of _The supermembrane revisited_, ([arXiv:hep-th/0412245](http://arxiv.org/abs/hep-th/0412245))


These authors amplify the role of closed $(p+2)$-forms in super $p$-brane backgrounds (p. 3) and clearly state the consistency conditions for the [[M2-brane]] in a curved backround in terms of the [[Bianchi identities]] on p. 7-8, amounting to the statment that the 4-form field strength has to be the pullback of the cocycle $\overline{\psi}\wedge e^a \wedge e^b \wedge \Gamma^{a b} \psi$ plus the [[supergravity C-field]] [[curvature]] and has to be closed.


That the [[heterotic supergravity]] equations of motion are sufficient for the 3-form super field strength $H$ to be closed was first argued in

* {#Nilsson81} [[Bengt Nilsson]], _Simple 10-dimensional supergravity in superspace_, Nuclear Physics B188 (1981) 176-192 ([spire](http://inspirehep.net/record/164253?ln=de))

and the computation there was highlighted and a little simplified around p. 17 of

* {#Witten86} [[Edward Witten]], _Twistor-like transform in ten dimensions_, Nuclear Physics B266 (1986) ([spire](http://inspirehep.net/record/214192/?ln=en))

A more comprehensive result arguing that the heterotic supergravity equations of motion of the background are not just sufficient but also necessary for (and hence equivalent to) the heterotic GS-string on that background being consistent was then claimed in

* {#ShapiroTaylor87} [[Joel Shapiro]], Cyrus Taylor, _Superspace supergravity from the superstring_, Physics letter B volume 186, number 1, 1987 ([pdf](http://ccdb5fs.kek.jp/cgi-bin/img/allpdf?198609078))

Discussion of this with the heterotic gauge-field included (hence including the [[Green-Schwarz anomaly cancellation]]) is in

* {#AtickDharRatra86} [[Joseph Atick]], Avinash Dhar, Bharat Ratra, _Superspace Formulation of Ten-dimensional $N=1$ Supergravity Coupled to $N=1$ Super Yang-Mills Theory_, Phys.Rev. D33 (1986) 2824 ([spire](https://inspirehep.net/record/219734), [pdf](http://ccdb5fs.kek.jp/cgi-bin/img/allpdf?198602074))

Similar arguments for the [[type II string]] in [[type II supergravity]] appeared in

* {#GHMNT85} [[Marcus Grisaru]], [[Paul Howe]], L. Mezincescu, [[Bengt Nilsson]], [[Paul Townsend]], _$N=2$-Superstring in a supergravity background_, Physics Letters Volume 162B, number 1,2,3 (1985) ([spire](http://inspirehep.net/record/17010))

and for GS sigma-model [[D-branes]] in

* {#CGNSW97} [[Martin Cederwall]], Alexander von Gussich, [[Bengt Nilsson]], Per Sundell, Anders Westerberg, _The Dirichlet Super-p-Branes in Ten-Dimensional Type IIA and IIB Supergravity_, Nucl.Phys. B490 (1997) 179-201 ([arXiv:hep-th/9611159](http://arxiv.org/abs/hep-th/9611159))



That the [[M2-brane]] [[sigma-model]] is consistent on backgrounds of [[11-dimensional supergravity]] that satisfy their equations of motion is discussed in ([Bergshoeff-Sezgin-Townsend 87](#BergshoeffSezginTownsend87)).

The role of the 4-form here is also amplified around (2.29) in

* [[Igor Bandos]], Carlos Meliveo, _Supermembrane interaction with dynamical D=4 N=1 supergravity. Superfield Lagrangian description and spacetime equations of motion_ ([arXiv:arXiv:1205.5885](http://arxiv.org/abs/arXiv:1205.5885))

and in section 2.2 of

* [[Igor Bandos]], Carlos Meliveo, _Three form potential in (special) minimal supergravity superspace and supermembrane supercurrent_ ([arXiv:1107.3232](http://arxiv.org/abs/1107.3232))

following

* {#OvrutWaldram97} [[Burt Ovrut]], [[Daniel Waldram]], _Membranes and Three-form Supergravity_, Nucl.Phys. B506 (1997) 236-266 ([arXiv:hep-th/9704045](http://arxiv.org/abs/hep-th/9704045))

See also

* Bernard de Wit, Kasper Peeters, Jan Plefka, _Superspace Geometry for Supermembrane Backgrounds_, Nucl.Phys. B532 (1998) 99-123 ([arXiv:hep-th/9803209](http://arxiv.org/abs/hep-th/9803209))

All this is actually subsumed by imposing the [[Bianchi identities]] of the corresponding [[supergravity Lie 3-algebra]] etc. in "rheonomic parameterization", of the _[[D'Auria-Fré formulation of supergravity]]_, this is discussed in ([AFFFTT 98, section 3.1](#AFFFTT98), [Fr&#233;-Grassi 07](#FreGrassi07)).

Discussion including also the [[RR-field]] background includes

* R. R. Metsaev, _Type IIB Green-Schwarz superstring in plane wave Ramond-Ramond background_ ([arXiv:hep-th/0112044](http://arxiv.org/abs/hep-th/0112044))

### Relation to AdS-CFT
 {#ReferencesRelationToAdSCFT}

The emergence of [[conformal field theory]] in the perturbations of the [[super-membrane]] around a classical solution stretched along the [[asymptotic boundary]] of [[anti de Sitter spacetime]] is due to 

* {#DuffSutton88} [[Mike Duff]], C. Sutton, _The Membrane at the End of the Universe_, New Sci. 118 (1988) 67-71 ([spire:268230](http://inspirehep.net/record/268230?ln=en))

predating the modern formulation of the [[AdS-CFT correspondence]]. The relation was amplified in 

* {#Duff98} [[Mike Duff]], _Anti-de Sitter space, branes, singletons, superconformal field theories and all that_, Int. J. Mod. Phys. A14:815-844, 1999 ([arXiv:hep-th/9808100](https://arxiv.org/abs/hep-th/9808100))

Further discussion of how Green-Schwarz action functionals for super $p$-branes in [[anti de Sitter spacetimes]] induce -- after restricting to small fluctuations about a background solution and after [[diffeomorphism]] [[gauge fixing]] -- superconformal field theory on the [[worldvolumes]] -- the [[AdS-CFT correspondence]] -- includes

for the [[M2-brane]]:

* {#AFFFTT98} Gianguido Dall'Agata, Davide Fabbri, Christophe Fraser, [[Pietro Fré]], Piet Termonia, Mario Trigiante, _The $Osp(8|4)$ singleton action from the supermembrane_, Nucl. Phys. B542:157-194, 1999 ([arXiv:hep-th/9807115](http://arxiv.org/abs/hep-th/9807115))

* {#PastiSorokinTonin99} [[Paolo Pasti]], [[Dmitri Sorokin]], Mario Tonin, _Branes in Super-AdS Backgrounds and Superconformal Theories_, Talk given by D.S. at the International Workshop "Supersymmetry and Quantum Symmetries", JINR, Dubna, Russia, July 26-31, 1999 ([arXiv:hep-th/9912076](http://arxiv.org/abs/hep-th/9912076))

for the [[M5-brane]]:

* {#ClausKalloshProeyen97} Piet Claus, [[Renata Kallosh]], [[Antoine Van Proeyen]], _M 5-brane and superconformal $(0,2)$ tensor multiplet in 6 dimensions_, Nucl. Phys. B518 (1998) 117-150 ([arXiv:hep-th/9711161](http://arxiv.org/abs/hep-th/9711161))

and more generally:

* {#ClausKalloshKumarTownsend98} Piet Claus, [[Renata Kallosh]], J. Kumar, [[Paul Townsend]], [[Antoine Van Proeyen]], _Conformal Theory of M2, D3, M5 and 'D1+D5' Branes_, JHEP 9806 (1998) 004 ([arXiv:hep-th/9801206](http://arxiv.org/abs/hep-th/9801206))

### Conserved current algebra
 {#ReferencesConservedCurrentAlgebra}

That higher WZW functionals and hence Green-Schwarz super $p$-brane action functionals have [[conserved current]] [[BPS charge]] algebras which are [polyvector extensions](super+Poincare+Lie+algebra#PolyvectorExtensions) of the supersymmetry algebras was observed in

* {#AGIT89} [[José de Azcárraga]], [[Jerome Gauntlett]], J.M. Izquierdo, [[Paul Townsend]], _Topological Extensions of the Supersymmetry Algebra for Extended Objects_, Phys. Rev. Lett. 63 (1989) 2443 ([spire](http://inspirehep.net/record/26393?ln=en))

reviewed in

* [[José de Azcárraga]], Jos&#233; M. Izquierdo, section 8.8. of _Lie Groups, Lie Algebras, Cohomology and Some Applications in Physics_ , Cambridge monographs of mathematical physics, (1995)

and generalized to super-[[Lie n-algebras]] of BPS charges in

* {#SatiSchreiber15} [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Lie n-algebras of BPS charges]]_ ([arXiv:1507.08692](http://arxiv.org/abs/1507.08692))



This is for branes in the old [[brane scan]] ([[strings]], [[membranes]], [[NS5-branes]]), excluding [[D-branes]] and [[M5-brane]].

The generalization oft this perspective to the [[M5-brane]] is discussed in

* {#SorokinTownsend97} [[Dmitri Sorokin]], [[Paul Townsend]], _M-theory superalgebra from the M-5-brane_, Phys.Lett. B412 (1997) 265-273 ([arXiv:hep-th/9708003](http://arxiv.org/abs/hep-th/9708003))

and the generalizatin to [[D-branes]] is discussed in

* Hanno Hammer, _Topological Extensions of Noether Charge Algebras carried by D-p-branes_, Nucl.Phys. B521 (1998) 503-546 ([arXiv:hep-th/9711009](http://arxiv.org/abs/hep-th/9711009))


### $\kappa$-Symmetry

The existence of [[kappa-symmetry]] was first noticed around

* {#Siegel83} Warren Siegel, _Hidden Local Supersymmetry In The Supersymmetric Particle Action_ Phys. Lett. B 128, 397 (1983)

* {#Siegel84} Warren Siegel, _Light Cone Analysis Of Covariant Superstring_ , Nucl. Phys. B 236, 311 (1984).


* {#GreenSchwarz} [[Michael Green]], [[John Schwarz]], _Covariant Description Of Superstrings_ , Phys. Lett. B 136, 367 (1984) ([web](http://adsabs.harvard.edu/abs/1984PhLB..136..367G))


The meaning of $\kappa$-symmetry in terms of the [[supergeometry|super]]-[[Cartan geometry]] of super-[[target space]] is discussed in

* {#McArthur} I.N. McArthur, _Kappa-Symmetry of Green-Schwarz Actions in Coset Superspaces_ ([arXiv:hep-th/9908045](http://arxiv.org/abs/hep-th/9908045))


* {#GKW} [[Joaquim Gomis]], Kiyoshi Kamimura, [[Peter West]], _Diffeomorphism, kappa transformations and the theory of non-linear realisations_ ([arXiv:hep-th/0607104](http://arxiv.org/abs/hep-th/0607104))

Discussion from the point of view of [[D'Auria-Fré formulation of supergravity]] is in

* {#AFFFTT98} Gianguido Dall'Agata, Davide Fabbri, Christophe Fraser, [[Pietro Fré]], Piet Termonia, Mario Trigiante, _The $Osp(8|4)$ singleton action from the supermembrane_, Nucl. Phys. B542:157-194,1999, ([arXiv:hep-th/9807115](http://arxiv.org/abs/hep-th/9807115))

* {#FreGrassi07} [[Pietro Fré]], [[Pietro Antonio Grassi]], _Pure Spinors, Free Differential Algebras, and the Supermembrane_, Nucl. Phys. B763:1-34,2007 ([arXiv:hep-th/0606171](http://arxiv.org/abs/hep-th/0606171))


### Open branes ending on other branes

Discussion of the Green-Schwarz action for the open [[M2-brane]] ending on the [[M5-brane]] is in

* C.S. Chu, [[Ergin Sezgin]], _M-Fivebrane from the Open Supermembrane_,  JHEP 9712 (1997) 001 ([arXiv:hep-th/9710223](http://arxiv.org/abs/hep-th/9710223))

* Ph. Brax, J. Mourad, _Open Supermembranes Coupled to M-Theory Five-Branes_, Phys. Lett. B416 (1998) 295-302 ([arXiv:hep-th/9707246](http://arxiv.org/abs/hep-th/9707246))



[[!redirects Green-Schwarz action]]

[[!redirects Green-Schwarz action functionals]]

[[!redirects Green-Schwarz string]]
[[!redirects Green-Schwarz superstring]]

[[!redirects Green-Schwarz strings]]
[[!redirects Green-Schwarz superstrings]]

[[!redirects super p-brane]]
[[!redirects super p-branes]]

[[!redirects Green-Schwarz sigma-model]]
[[!redirects Green-Schwarz sigma-models]]

[[!redirects Green-Schwarz sigma model]]
[[!redirects Green-Schwarz sigma models]]

[[!redirects Green-Schwarz super p-brane sigma model]]
[[!redirects Green-Schwarz super p-brane sigma models]]
[[!redirects Green-Schwarz super p-brane sigma-model]]
[[!redirects Green-Schwarz super p-brane sigma-models]]


[[!redirects Green-Schwarz super p-brane]]
[[!redirects Green-Schwarz super p-branes]]

[[!redirects super p-brane sigma-model]]
[[!redirects super p-brane sigma-models]]

[[!redirects super p-brane sigma model]]
[[!redirects super p-brane sigma models]]

[[!redirects Green-Schwarz-type sigma model]]
[[!redirects Green-Schwarz-type sigma models]]

[[!redirects Green-Schwarz-type sigma-model]]
[[!redirects Green-Schwarz-type sigma-models]]

[[!redirects Green-Schwarz super-string]]
[[!redirects Green-Schwarz super-strings]]

[[!redirects Green-Schwarz super-p brane sigma model]]
[[!redirects Green-Schwarz super-p brane sigma models]]

[[!redirects Green-Schwarz sigma-model for super p-branes]]
[[!redirects Green-Schwarz sigma-models for super p-branes]] 

[[!redirects fundamental super p-brane]]
[[!redirects fundamental super p-branes]]

