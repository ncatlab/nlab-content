
## Idea

The [[equations of motion]] of [[classical field theory|classical]] [[electromagnetism]] ([[Maxwell's equations]]) on any [[spacetime manifold]] $(X,g)$ read, in modern [[differential form]]-formulation:

\[
  \label{MaxwellEquationsInTraditionalDifferentialForm}
  \begin{array}{rcl}
    \mathrm{d}\,  F &=& 0 \mathrlap{\,,}
    \\
    \mathrm{d} \, \star_g F &=& j
  \end{array}
\]

where 

* the [[differential 2-form]] $F \,\in\, \Omega^2(X)$ is the [[Faraday tensor]],

* the [[differential 3-form]] $j \,\in\, \Omega^3(X)$ is the electromagnetic [[current]] density

* $\mathrm{d} \,\colon\,\Omega^p(X) \longrightarrow \Omega^{p+1}(X)$ denotes the [[de Rham differential]],


and last not least

* $\star_g \,\colon\, \Omega^p(X) \longrightarrow \Omega^{4-p}(X)$ denotes the [[Hodge star operator]] induced by the [[pseudo-Riemannian metric]] of the given [[Lorentzian manifold]] $(X,g)$.

Often this is considered for $X \simeq \mathbb{R}^{3,1}$ being [[Minkowski spacetime]], hence for $g = \eta$ the [[Minkowski metric]], in which case this describes pure "Maxwell theory", but the exact same formulas apply in the generality that $(X,g)$ is any [[Lorentzian manifold]], in which case they form the sector of the [[equations of motion]] of [[Einstein-Maxwell theory]] which involve the [[electromagnetic field]] and its coupling to [[background field|background]] [[gravity]]. (The remaining sector are the [[Einstein equations]] for the metric field $g$ sourced by the [[stress-energy tensor]] of the Maxwell field).

In order to bring out more manifestly that [[gravity]] (the [[pseudo-Riemannian metric]]) enters *only* through the [[Hodge star operator]], we may evidently re-write the above pair of equations (eq:MaxwellEquationsInTraditionalDifferentialForm) equivalently as follows:

\[
  \label{MaxwellEquationsInPreMetricDifferentialForm}
  \begin{array}{rcl}
    \mathrm{d}\,  F &=& 0 \mathrlap{\,,}
    \\
    \mathrm{d} \, G &=& j
  \end{array}
  \;\;\;\;
  \text{and}
  \;\;\;\;
  G \,=\, \star_g F
  \,.
\]

In fact, this formulation (eq:MaxwellEquationsInPreMetricDifferentialForm) is closer to the (original) formulation of Maxwell's equations used in the case that spacetime $X$ is thought of as possibly filled with a *[[dielectric medium]]* where, *a priori*, one considers four field: 

1. the [[electric field]] $\vec E$ and [[magnetic field|magnetic]] [[flux density]] $\vec B$ 

   which constitute the [[Faraday tensor]]) given (on a local [[coordinate chart]] $(t,x^1, x^2, x^3)$) by

  $$
    F 
      \,=\, 
    E_i \mathrm{d}x^i \wedge \mathrm{d} t 
      \,+\, 
    \epsilon_{i j k} B^i \mathrm{d} x^j \mathrm{d} x^k
  $$

as well as 

1. the actual [[magnetic field]] $\vec H$ and the *dielectric displacement cuurent* $\vec D$ with

   $$
     G 
       \,=\, 
     H_i \mathrm{d}x^i \wedge \mathrm{d} t 
       \,-\, 
     \epsilon_{i j k} D^i \mathrm{d} x^j \mathrm{d} x^k
   $$

and then imposes *constitutive equations* 
relating $(\vec E, \vec B)$ to $(\vec H, \vec D)$ and thereby expressing the [[dielectric]]-property of any electromagneric *medium* that one imagines filling the spacetime $X$.

In general, constitutive equations can be nonlinear (and even multi-valued, reflecting hysteresis effects), but for sufficiently small [[field strength]] they are of the form

$$
  G \,=\, \star_\epsilon F
$$

for a [[linear map]]

$$
  \star_\epsilon
  \,\colon\,
  \Omega^2(X)
  \longrightarrow
  \Omega^2(X)
$$

much like the [[Hodge star operator]] (whence here we use similar notation for both, which is non-standard).


Delphenich called this the "pre-metric formulation" of electromagnetism and had high hopes that it would help towards better understanding of [[Einstein-Maxwell theory]]. 

Completely independently, exactly this idea is actually used in the [[K-theory classification of D-brane charge]]: Here one first adjoins to all the [[RR-field forms]] their would-be Hodge-duals, then imposes equations of motions and *afterwards* tries to re-impose the actual Hodge-duality constraint.

(....)


## References

* Friedrich Kottler, *Maxwell'sche Gleichungen und Metrik*, Sitz. Akad. Wien IIa **131** (1922) 119-146

* [[David van Dantzig]], *The fundamental equations of electromagnetism, independent of metrical geometry*, Mathematical Proceedings of the Cambridge Philosophical Society **30** 4  (1934) 421-427 &lbrack;[doi:10.1017/S0305004100012664](https://doi.org/10.1017/S0305004100012664)&rbrack;

* [[David H. Delphenich]], *On linear electromagnetic constitutive laws that define almost-complex structures*, Annalen Phys. **16** (2007) 207-217 &lbrack;[doi:gr-qc/0610031](https://arxiv.org/abs/gr-qc/0610031), [doi:10.1002/andp.200610227](https://doi.org/10.1002/andp.200610227)&rbrack;

* [[David H. Delphenich]], *Spinors and Pre-Metric Electromagnetism*, Advances in Applied Clifford Algebras **18** (2008) 567–578 &lbrack;[doi:10.1007/s00006-008-0115-6](https://doi.org/10.1007/s00006-008-0115-6)&rbrack;


* [[David H. Delphenich]], *Pre-metric electromagnetism as a path to unification*, in: *Unified Field Mechanics*, World Scientific (2015) 215-220 &lbrack;[arXiv:1512.05183](https://arxiv.org/abs/1512.05183), [doi:10.1142/9789814719063_0023](https://doi.org/10.1142/9789814719063_0023)&rbrack;


***

<center>
<div style="margin:-20px 10px 10px 10px;"><img src="https://ncatlab.org/nlab/files/AdSCFTForSmallN-230613.jpg" width="750">
</div>
</center>



> [40:20](https://youtu.be/trxjCOmg8GY?t=2420) What is the future of this problem &lbrack;Yang-Mills & mass-gap&rbrack; in physics, what could happen?

> [40:24](https://youtu.be/trxjCOmg8GY?t=2424) This is now my personal guess or, if you like, hints &lbrack;or&rbrack; suggestions.

> [40:30](https://youtu.be/trxjCOmg8GY?t=2430) You can try a direct analytical assault. If you are a young man and brave and you have a long way into thre future, you can just get out your hammer and chisel and crack away.

> [40:47](https://youtu.be/trxjCOmg8GY?t=2447) Or you might think that you want something different.

> [40:50](https://youtu.be/trxjCOmg8GY?t=2450) You might find to get a better understanding of the formal structure of quantum field theory of this Yang-Mills type. 

> [40:58](https://youtu.be/trxjCOmg8GY?t=2458) These Yang-Mills theories have very elaborate mathematical formal structure, which incorporates very mysterious dualities of various kinds and also a thing called *supersymmetry*, and many of the applications in mathematics incorporate all these.

> [41:51](https://youtu.be/trxjCOmg8GY?t=2475) So here there is a very elaborate structure, and it is just possible that if we get a better understanding of that structure then that might have given us a better way of trying to lay the foundations.

> [41:25](https://youtu.be/trxjCOmg8GY?t=2485) For example, a problem that can be described in two different ways, by duality, two dual pictures might look quite different, one of them might be practical and the other one might be intractable.

> [41:35](https://youtu.be/trxjCOmg8GY?t=2495) They are certainly not at all unreasonable to think this might be a way starting to understand better these formal operators[?], the formal operators here is very sophisticated.

> [41:47](https://youtu.be/trxjCOmg8GY?t=2507) You could of course sit back and wait, await development in string theory.

> [41:54](https://youtu.be/trxjCOmg8GY?t=2514) String theory and the latest things that follow string theory, called M-theory and every other new theory, develop [at] an enormous rate.

> [42:00](https://youtu.be/trxjCOmg8GY?t=2520) The theoretical physics community here is tremendously active, there are very beautiful things happening every week, new results come out, many of them will have mathematical overtones.

> [42:10](https://youtu.be/trxjCOmg8GY?t=2530) And it could be that if we wait a few years there'll be such a totally new  picture emerging from string theory that we'll get a better idea how to go about attacking the problem, so that's not an unreasonable expectation.

> [42:21](https://youtu.be/trxjCOmg8GY?t=2541) You see, trying to lay the foundations for physics is like an architect trying to lay the foundations that's rapidly going up.

> [42:30](https://youtu.be/trxjCOmg8GY?t=2550) I mean, which do you do first, it's not quite clear: You want to see the design or you want to lay the foundations. Maybe you want the design first.

> [42:39](https://youtu.be/trxjCOmg8GY?t=2559) The, of course, you might also sit back and say: Well, quantum electrodynamics was very hard, because we didn't incorporate extra things like proton and neutrons, we only worried about electrons. Maybe even that isn't enough perhaps we should have incorporated gravity, then we'll have all the forces under control and perhaps at that stage the fundamental theory will be even easier.

> [43:00](https://youtu.be/trxjCOmg8GY?t=2580) People in string theory aim here and this is the ultimate, and perhaps the ultimate theory will be easier than the transitional theories. But who knows.

> [43:09](https://youtu.be/trxjCOmg8GY?t=2589) The big challenge [for] mathematics and the physicists of the 21st century is to really make progress along this program by whatever method they can. Good luck to you.
 







\begin{tikzcd}
  B 
    \ar[d, hook]
    \ar[r, "{ f }"] 
  & 
  L
  \ar[d, gray]
  \\
  A
  \ar[ur, dashed, "{ \underline{f} }"{swap}]
  \ar[r, gray]
  &
  \color{gray}\ast
\end{tikzcd}


A & B

## Polyakov gauge-string duality

> The biggest threat to a good idea are often its proponents, or those who vocally appear to be. 


[[string theory|String theory]] originated in the 1960s as a conceptual strategy for understanding experimental observations about [[non-perturbative quantum field theory|strongly-interacting]] [[fundamental particles]], notably the [[confinement]] of "[[quarks]]" inside [[hadrons]] and the "[[Regge trajectories]]" seen in [[hadron]] [[scattering]]. These are experimental phenomena exhibited by fairly ordinary [[matter]] (all [[atomic nuclei]] are [[bound states]] of [[hadrons]]), and yet (despite frequent advertisement of the success of the [[standard model of particle physics]]) understanding them properly remains an open problem to this day, to the extent that one speaks of a "[Millennium Problem](mass+gap#ReferencesMassGapProblem)".

However, a saga of 5 decades of intellectual twists and sociological turns later, mainstream string theorists as a swarm community largely forgot about the glaring question why quarks are never seen in isolation and somehow ended up, in the 2000s, instead convincing themselves and the public that string theory's  prime contribution to physics is to suggest the imminent detection of "[[squarks]]" at the [[LHC]]-experiment commencing in 2010. The failure of this alleged prediction to materialize is increasingly leading to the sensation of a failure of "string theory". 

In reality, this should be a chance to go back to the roots and re-assess [[string theory]] as a candidate for the elusive theory of strongly-interacting matter systems, both in [[high energy physics]] --- concerning [[quantum hadrodynamics]] in [[QCD]] --- as well as in [[solid-state physics]] --- notably concerning [[topological order|topologically ordered]] [[quantum materials]] ---, both reflected in a "[[mass gap]]" and both related to [[quantum gravity]] via [[holography]] in the original sense of [[Alexander Polyakov]]'s *[[gauge/string duality]]*.

This is the role of string theory that [[Alexander Polyakov]]  [originally envisioned](AdS-CFT+correspondence#PolyakovGaugeStringDualityReferences) (following observations notably by [[Leonard Susskind]] and [[Kenneth Wilson]]) under the name *gauge-string duality*, long before the community came back full circle to this idea with what is now known as *[[AdS/CFT duality]]* and *[[holographic QCD]]* (see further comments [below](#NoticeTheDecisiveInsight)). 

The logic here proceeds in the following steps (cf. [Polyakov (2007), §1](#Polyakov07)):

\begin{imagefromfile}
    "file_name": "HadronicStringInPionScattering.jpg",
    "float": "right",
    "width": 400,
    "unit": "px",
    "margin": {
        "top": -0,
        "bottom": 10,
        "right": 0, 
        "left": 15
    },
    "caption": "From [Veneziano 2012](string+theory#Veneziano12), Fig 2.9"
\end{imagefromfile}


1. **flux tubes confine as dynamical strings**

   The starting point is the [[hypothesis]] that the strong coupling of particles (such as [[quarks]]) by a (non-abelian) [[gauge field]] (such as the [[strong nuclear force]]) is embodied by the formation of "[[flux tubes]]" ("[[Wilson lines]]") between pairs of such particles, which in themselves behave like [[strings]] with a given [[tension]].

   &lbrack;[Kogut & Susskind (1974)](#KogutSusskind74), [(1975)](#KogutSusskind75); [Wilson (1974)](#Wilson74); [Polyakov (1979)](#Polyakov79), [(1980)](#Polyakov80), [(1987)](#Polyakov80); [Makeenko & Migdal (1981)](#MakeenkoMigdal81)&rbrack;

   Under this assumption it would be:

   1. the [[flux tube]]/[[string]]'s [[tension]] which keeps the particles at theirs endpoints [[confinement|confined]], 

   1. the excitation of these [[flux tubes]]/[[strings]] which follow [[Regge trajectories]] (such as of [[hadrons]]);

   1. the [[scattering]] of these [[flux tubes]]/[[strings]] which explains the observed [[Veneziano amplitudes]],

   which are the main qualitative features to be explained.


1. **quantum flux tubes probe effective higher dimensions**

   But if so, famous quantum effects make such [[flux tubes]]/[[strings]] behave like propagating in an effective/emergent higher-dimensional spacetime:

   * either because one regards the string as *a priori* propagating in non-critical [[spacetime]]-[[dimension]] $4$, in which case the [[dilaton field]]/[[Liouville field]] $\phi$ appears to cancel the [[quantum anomaly]] and acts like a warped 5th dimension: 

     this was the point of view published in [Polyakov (1981)](#Polyakov81) but later claimed, in [Polyakov (2008)](#Polyakov08), to have originated already "by the end of '77";
 
   * or because one regards the string as propagating in critical dimension (10 for the [[superstring]]) right away, 

     which is the point of view adopted later in [[AdS-CFT duality]], starting with [Maldacena (1997)](AdS-CFT+correspondence#Maldacena97a)

   with only the endpoints of the [[flux tube]]/[[string]] constrained to lie in the original lower dimensional spacetime 

   &lbrack;[Polyakov (1998)](#Polyakov98), [(1999)](#Polyakov99)&rbrack;

   which now appears (in modern language that Polyakov did not originally use) as a "[[brane]]" inside a higher dimensional [[bulk]] spacetime.

   Notice that in this picture the observable physics that we set out to describe takes place *on the brane* ([[underlying]] which is typically flat [[Minkowski spacetime]]!) at the [[asymptotic boundary|asymptotic]] [[boundary]] of a higher-dimensional [[bulk]] spacetime, while the (potentially large) extra dimensions of a possibly $\sim$ [[AdS]]-bulk remain primarily unobservable. In fact, in Polyakov's original picture the extra 5th dimension is not so much a spacetime dimension but a parameter for the *thickness* of the [[flux tube]], which becomes non-vanishing due to quantum effects &lbrack;cf. [Polyakov (2008), p. 3](#Polyakov08)&rbrack;.


1. **large/small $N$ confined gauge theory is holographic string theory/M-theory**

   Thus the description of strongly coupled matter via [[flux tubes]]/[[strings]] now reveals a [[holography|holographic]] situation where strongly-coupled quantum fields on [[intersecting brane models|intersecting branes]] are equivalently described by a theory of [[quantum gravity]] mediated by [[strings]] propagating in a higher dimensional [[bulk]] [[spacetime]].

   In relation to gauge string duality this is due to [Gubser, Klebanov & Polyakov (1998)](#GubserKlebanovPolyakov98), which is now understood as part of *[[AdS/CFT duality]]*, but it is actually meant to be more general, cf. [Polyakov & Rychkov (2000)](#PolyakovRychkov00).
  

While this dual bulk string theory is itself strongly-coupled unless the "number of coincident branes" is humongous (the "[[large-N limit]]") and thus unrealistic after all, the difference is that with making explicit the [[brane]] as physical objects produces more concrete hints as to its strongly-coupled (non-perturbative) completion, going under the working title *[[M-theory]]*, cf. at *[AdS-CFT -- Small $N$ corrections](AdS-CFT+correspondence#SmallNCorrections)*.

In summary, the plausible approach of understanding strongly-coupled quantum gauge theories by regarding their [[flux tubes]] as dynamical [[strings]] seems to recast the [Millennium Problem](mass+gap#ReferencesMassGapProblem) of understanding strongly-coupled matter into the problem of formulating [[M-theory]]: Given [[M-theory]], it ought to be possible to find [[intersecting brane models]] of single (or a small number of [[coincident branes|coincident]]) [[M-branes]] (such as the *[Witten-Sakai-Sugimoto model](AdS-QCD+correspondence#WittenSakaiSugimotoModel)* [[M5-brane]] system) on whose [[worldvolume]] the desired strongly-coupled field theory is realized (such as [[QCD]]).

{#NoticeTheDecisiveInsight} Notice the decisive early insight of [[Alexander Polyakov]] here: While the idea that [[strings]] somehow describe [[hadron|hadronic]] [[bound states]] was the very origin of [[string theory]] in the early 1970s ("dual resonance models"), the mainstream *abandoned* this perspective in the later 1970s when the critical dimension and the full spectrum of the string became fully understood (cf. *[[Goddard-Thorn no-ghost theorem]]*) and declared that *instead* string should be understood as a [[GUT|grand unified]] [[theory of everything]] including [[quantum gravity]] (see e.g. the historical review of [Veneziano (2012), esp. pp. 30-31](string+theory#Veneziano12) which still clings to this perspective). From here it was only through the long detour of first discovering, inside this grander theory: [[D-branes]] (and [[M5-branes]]) in the 1990s, then their [[near-horizon geometry|near-horizon]] [[AdS-CFT duality]] just before the 2000s and then another decade of exploring [[intersecting D-brane models]] that the community in the 2010s came back full circle to Polyakov's holographic perspective on [[QCD]], now dubbed *[[holographic QCD]]*, in which strings are flux tubes that propagate not (alone) in the observable 4 spacetime dimensions but in a primarily unobservable (meanwhile known as *[[Randall-Sundrum model|Randall-Sundrum]]*-like) higher-dimensional [[bulk]] spacetime -- a holographic description of reality that [Polyakov (1999)](#Polyakov99) referred to as the *wall of the cave*, in allusion to [[Plato]] (cf. also [#Polyakov (2008), p. 6](#Polyakov08)). The whereabouts in this remarkable situation are still often misunderstood today: If string theory is a theory of nature, then, it seems, we see the wall but not the cave: we live on a $\sim$ [[Minkowski spacetime|Minkowskian]] [[intersecting D-brane model|brane intersection]] at the ([[asymptotic boundary|asympotic]]) [[boundary]] of a primarily unobserved $\sim$ [[anti de Sitter spacetime|adS]] [[bulk]] which may better be thought of not as physical space but as a configuration space of quantum flux. 



## References

[[!include Polyakov gauge-string duality -- references]]


****

[[Polyakov gauge-string duality]]

The following over/underlines recently come out tiny when viewed in  

* Chrome, Edge and Opera 

while they still come out as expected in 

* Firefox 

(at least on the systems we tried in discussion [here](https://nforum.ncatlab.org/discussion/12362/twisted-arrow-1category/?Focus=110459#Comment_110459)):

* "`$\overline{ThisShouldRenderWithALooongOverline}$`" 

  renders as: 

  "$\overline{ThisShouldRenderWithALooongOverline}$"

* "`$\overline{ThisShouldRenderWithALooongUnderline}$`" 

  renders as: 

  "$\underline{ThisShouldRenderWithALooongUnderline}$"

Specifically, the rendering with Chrome, Edge and Opera looks (except for horizontal positioning) like that of the `\bar` command:

* "`$\bar{ThisShouldRenderWithATinyOverline}$`" 

  renders as: 

  "$\bar{ThisShouldRenderWithATinyOverline}$"

