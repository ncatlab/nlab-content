#Contents#
* Contents
{:toc}

## Idea

An ordinal analysis of a formal system precisely measures its proof-theoretic strength, which is its strength at justifying [[transfinite induction]]. In practice, it also measures the system's ability to prove totality of complex computable functions.

Giving a concrete "ordinal notation" that describes the proof-theoretic strength of a system is sometimes seen as providing a constructive justification for the reasoning principles of the system. However, ordinal analysis is not limited to systems that are [[constructive]] in the sense of not assuming [[excluded middle]]. But in practice, classical systems with ordinal notations are interpretable constructively.

### Relation to Predicativity

While it is classically true that any [[deductive system#FormalSystems|effective formal system]] has some limit to its proof-theoretic strength, only systems of limited strength have had their strength concretely described by a good ordinal notation. Specifically, all systems with ordinal analyses so far are significantly weaker than full [[second-order arithmetic]]. Consequently, so far, systems that have been given ordinal notations feel more like [[predicative]] systems than like familiar impredicative systems such as [[ZFC]], [[higher-order logic|higher-order arithmetic]], and [[ETCS]].

Many have argued, however, that the boundary between predicatively-justifiable and impredicative systems lies somewhere within the range of proof-theoretic ordinals already analyzed. In other words, that the stronger systems in the table below are actually slightly impredicative, even when it isn't obvious.

## Definition

+-- {: .num_defn}
###### Definition

The **proof-theoretic ordinal** of a [[theory]] $T$ is (commonly) defined as

$$ {\vert T\vert} = \sup\{ \mathrm{otyp}({\prec}) \mid {\prec}\text{is primitive recursive and}\;
 T \vdash \mathrm{TI}({\prec},X) \}$$

where $\mathrm{otyp}({\prec})$ is the [[order-type]] of the [[well-order]]
$\prec$ and $\mathrm{TI}({\prec},X)$ means that $X$ (a free parameter) satisfies transfinite induction along $\prec$; this is the constructive way to say that $\prec$ is well-ordered. For most theories, this ordinal is equal to the $\Pi^1_1$-ordinal of the theory,

$$ {\vert T\vert}_{\Pi^1_1} := \sup\{ \mathrm{tc}(F) \mid F\;\text{is a}\;\Pi^1_1\text{-sentence and }\;
 T \vdash F \}$$

where $\mathrm{tc}(F)$ is the truth-complexity of the
$\Pi^1_1$-sentence $F$ (if $T$ is a first-order theory, we interpret
$T \vdash \forall X.F(X)$ as $T \vdash F(X)$ with a free set parameter
$X$).

=--

The proof-theoretic ordinal is always a recursive [[ordinal]] ($\lt\omega_1^{\mathrm{CK}}$) if the theory is recursive.

Note that the proof-theoretic ordinal is a rather blunt invariant, because if $F$ is any true $\Sigma^1_1$-sentence, then

$$ {\vert T\vert}_{\Pi^1_1} = {\vert T+F\vert}_{\Pi^1_1} $$

So this tells us nothing about the provable arithmetical sentences of
$T$! And indeed, all true arithmetical sentences have truth-complexity
less than $\omega$.

The solution is to refine the analysis to give a $\Pi^0_2$ ordinal
analysis of the theory, using a measure of the computational
complexity of provable $\Pi^0_2$-sentences/provably recursive
functions. However, there's no natural hierarchy of all subrecursive
functions. We can define such a computational complexity depending on a
choice of starting function and a choice of ordinal notation system
(indeed, the $\Pi^0_2$ ordinal should be thought of as an ordinal
notation, rather than an actual ordinal). But for all the ordinal
analyses we have so far, these choices turn out not to matter,
basically because any _natural ordinal notation system_ will give the
same result. A major issue is, however, that we have no definition of
what a natural ordinal notation system is (but we know one when we see
it!).

All of the ordinal analyses mentioned below also give a $\Pi^0_2$
ordinal analysis, and thus control of the computational complexity of
the provably recursive functions.

## Methods

### Upper bounds

Most ordinal analyses proceed by embedding the theory in an infinitary
proof calculus deriving judgments $\vdash^\alpha_\rho F$ meaning $F$
has an infinitary derivation of height less than $\alpha$ using only
cuts of rank less than $\rho$, or some refinement of such, for
instance using operator controlled derivations. Then one analyzes how
the height of a derivation changes during cut-elimination. For
predicative theories, we'll have

$$ \vdash^\alpha_\rho \Delta \Rightarrow \vdash^{\varphi\rho\alpha}_0 \Delta $$

One sets up the calculus so that $\vdash^\alpha_0 F$ implies
$\mathrm{tc}(F)\lt\alpha$, so this yields upper bounds for the
proof-theoretic ordinal.

### Lower bounds

Lower bounds are usually done by directly deriving
$T \vdash \mathrm{TI}({\prec_n},X)$ for a sequence of primitive recursive
well-orderings $\prec_n$ whose order-types approximate the
proof-theoretic ordinal. We get these primitive recursive
well-orderings from good ordinal notation systems, see below.

## Table of Ordinal Analyses

See below for explanations.

| Ordinal                                      | FOA                                        | SOA                                    | Other                          |
|----------------------------------------------|--------------------------------------------|----------------------------------------|--------------------------------|
| **Finitist systems**                         |                                            |                                        |                                |
| $\omega^3$                                   | EFA                                        | RCA$_0^*$                              |                                |
| $\omega^\omega$                              | PRA,I$\Sigma_1$                            | RCA$_0$, WKL$_0$                       | CPRC                           |
| **Predicative systems**                      |                                            |                                        |                                |
| $\varepsilon_0=\varphi(1,0)$                 | PA                                         | ACA$_0$, $\Delta_1^1$-CA$_0$, $\Sigma^1_1$-AC$_0$ | EM$_0$              |
| $\varphi(1,\varepsilon_0)$                   |                                            | ACA                                    |                                |
| $\varphi(\omega,0)$                          | ID$_1^#$                                   | $\Delta_1^1$-CR                        | EM$_0$+JR                      |
| $\varphi(\varepsilon_0,0)$                   | $\widehat{\mathrm{ID}}_1$                  | $\Delta_1^1$-CA, $\Sigma^1_1$-AC       | EM$_0$+J, ML$_1$               |
| $\Gamma_0=\varphi(1,0,0)$                    | $\widehat{\mathrm{ID}}_{\lt\omega}$, U(PA) | ATR$_0$,$\Delta^1_1$-CA+BR             | ML$_{\lt\omega}$, MLU, KPi$^0$ |
| **Meta-predicative systems**                 |                                            |                                        |                                |
| $\varphi(1,0,\varepsilon_0)$                 | $\widehat{\mathrm{ID}}_{\omega}$           | ATR                                    | KPl$^0$+F-I$_\omega$           |
| $\varphi(1,\omega,0)$                        | $\widehat{\mathrm{ID}}_{\lt\omega^\omega}$ | ATR$_0$+($\Sigma^1_1$-DC)              | KPi$^0$+$\Sigma_1$-I$_\omega$  |
| $\varphi(1,\varepsilon_0,0)$                 | $\widehat{\mathrm{ID}}_{\lt\varepsilon_0}$ | ATR+($\Sigma^1_1$-DC)                  | KPi$^0$+F-I$_\omega$           |
| $\varphi(1,\Gamma_0,0)$                      | $\widehat{\mathrm{ID}}_{\lt\Gamma_0}$      |                                        | MLS                            |
| $\varphi(2,0,0)$                             | Aut($\widehat{\mathrm{ID}}$)               |                                        | KPh$^0$                        |
| $\varphi(\omega,0,0)$                        |                                            |                                        | KPM$^0$                        |
| **Inductive types**                          |                                            |                                        |                                |
| $\psi_\Omega(\varepsilon_{\Omega+1})$        | ID$_1$                                     |                                        | KP$\omega$, CZF, ML$_1$V       |
| $\psi_\Omega(\Gamma_{\Omega+1})$             | U(ID$_1$)                                  |                                        |                                |
| $\psi_\Omega(\Omega_\omega)$                 | ID$_{\lt\omega}$                           | $\Pi^1_1$-CA$_0$,$\Delta^1_2$-CA$_0$   |                                |
| $\psi_\Omega(\Omega_\omega \varepsilon_0)$   | W-ID$_\omega$                              | $\Pi^1_1$-CA                           | W-KPl                          |
| $\psi_\Omega(\varepsilon_{\Omega_\omega+1})$ | ID$_\omega$                                | $\Pi^1_1$-CA+BI                        | KPl                            |
| $\psi_\Omega(\Omega_{\omega^\omega})$        | ID$_{\lt\omega^\omega}$                    | $\Delta^1_2$-CR                        |                                |
| $\psi_\Omega(\Omega_{\varepsilon_0})$        | ID$_{\lt\varepsilon_0}$                    | $\Delta^1_2$-CA, $\Sigma^1_2$-AC       | W-KPi                          |
| $\psi_\Omega(\varepsilon_{I+1})$             |                                            | $\Delta^1_2$-CA+BI, $\Sigma^1_2$-AC+BI | KPi, T$_0$, CZF+REA            |
| $\psi_\Omega(\Omega_{I+\omega})$             |                                            |                                        | ML$_1$W                        |
| $\psi_\Omega(\Omega_L)$                      |                                            |                                        | KPh, ML$_{\lt\omega}$W         |
| **Inductive-recursive types**                |                                            |                                        |                                |
| $\psi_\Omega(\varepsilon_{M+1})$             |                                            | $\Delta^1_2$-CA+BI+(M)                 | CZFM, KPM                      |
| $\psi_\Omega(\Omega_{M+\omega})$             |                                            |                                        | KPM$^+$, MLM, "Agda"           |

The sections of the table corresponds roughly to the kinds of reasoning captured by the systems:

* Finitistic reasoning about the natural numbers (and other finitistic inductive types)
* Predicative reasoning about the natural numbers
* Meta-predicative reasoning about the natural numbers
* Reasoning about general inductive types
* Reasoning about general inductive-recursive types

Note that these are all very much weaker than full second-order arithmetic, and of course much weaker than Zermelo or Zermelo-Fraenkel set theory.

After the meta-predicative systems, all ordinals use a notation which refers to a much larger ordinal, often patterned on a large cardinal.

Rathjen (2005) analyzed systems up to $\Delta^1_2$-CA+BI+$\Pi^1_2$-CA$^-$ (the last part is parameter-free $\Pi^1_2$-comprehension), corresponding to a stable ordinal. Arai has work on systems that are a bit stronger, up to about $\Sigma^1_3$-DC+BI, in terms of ordinal diagrams defined in terms of iterated stability, and has more recently analyzed KP+$\Pi_1$-collection, which is beyond KP+"the stable ordinal are unbounded" in strength.

With current technology, we are very far from having ordinal analyses of stronger systems such as full second order arithmetic, ZFC set theory, or impredicative type theories such as the calculus of (inductive) constructions.

### Ordinal notations

* $\varphi$ is either the binary or the ternary Veblen function
* $\Omega=\Omega_1$ is the first recursively regular ordinal 
* $\Omega_\xi$ is the $\xi$th ordinal that is recursively regular or a limit of smaller recursively regulars
* $I$ is the first recursively inaccessible ordinal
* $L$ is the limit of the first $\omega$ recursively inaccessible ordinals
* $M$ is the first recursively Mahlo ordinal

The $\psi$ functions are ordinal collapsing functions.

### Systems of first-order arithmetic (FOA)

These assert some hierarchy of inductive defined sets of natural numbers.

* EFA is elementary function arithmetic
* PRA is [[primitive recursive arithmetic]]
* PA is first-order Peano arithmetic
* $\widehat{\mathrm{ID}}_\nu$ extends PA by $\nu$ iterated fixed points of monotone operators (not necessarily least).
* ID$_1^#$ is $\widehat{\mathrm{ID}}_1$ with induction only for positive formulas.
* ID$_\nu$, the theory of $\nu$-times [[iterated inductive definitions]], extends PA by $\nu$ iterated least fixed points of monotone operators.

Many of the results in the table concerning these can be summarized as

$$ {\vert \mathrm{ID}_\nu \vert} = \psi_\Omega(\varepsilon_{\Omega_\nu+1}) $$

For any of these, we get the same proof-theoretic ordinal whether we
use classical or intuitionistic logic. For the ID$_\nu$-systems, this
is due to Sieg.

The unfolding systems U(PA) and U(ID$_1$) are not exactly first-order
arithmetic systems, but capture what we can get by predicative
reasoning based on the natural numbers or one generalized inductive
definition, respectively.

### Systems of second-order arithmetic (SOA)

* Comprehension or choice principles.
* RCA$_0^*$ is the second-order version of EFA: $\exp$ is a function symbol.
* WKL is weak K&#246;nig's lemma.
* BR is the bar induction rule.
* BI is the bar induction axiom.
* ATR is arithmetical transfinite recursion.
* (M) says every true $\Pi^1_3$ sentence with parameters holds in a $\beta$-model of $\Delta^1_2$-CA.

A zero subscript indicates that we have the induction axiom rather
than the induction scheme, except for RCA$_0$ which has the
$\Sigma^0_1$-induction scheme.

### Kripke Platek Set theories

* KP$\omega$ is Kripke-Platek set theory, whose universe is an admissible set containing $\omega$.
* KPl asserts that the universe is a limit of admissible sets
* KPi asserts that the universe is inaccessible sets
* KPh asserts that the universe is hyperinaccessible: an inaccessible set and a limit of inaccessible sets
* KPM asserts that the universe is a Mahlo set

A superscript zero indidcates that $\in$-induction is removed.

About the Mahlo level: this also corresponds to inductive-recursive definitions (Dybjer-Setzer).

### Martin-L&#246;f type theories

* CPRC is the Herbelin-Patey Calculus of Primitive Recursive Constructions.
* ML$_n$ is type theory without W-types with $n$ universes.
* ML$_{\lt\omega}$ is type theory without W-types with an infinite hierarchy of universes.
* MLU is type theory with a next universe operator.
* MLS is type theory without W-types with a superuniverse.
* ML$_1$V is type theory with one universe and Aczel's type of iterative sets.
* ML$_1$W is type theory with W-types and one universe.
* ML$_{\lt\omega}$W is type theory with W-types and an infinite hierarchy of universes (this corresponds to the type theory in Lean's HoTT mode).
* MLM is Martin-L&#246;f type theory with a Mahlo universe.

### Constructive Set theories

* CZF is Aczel's constructive set theory.
* REA is the regular extension axiom. 
* CZFM is CZF with a Mahlo universe

### Explicit mathematics systems

* EM$_0$ is basic [[explicit mathematics]] with elementary comprehension
* JR is the join rule, J is the join axioms
* T$_0$ is EM$_0$+J+IG, where IG is inductive generation

## References

* Aczel, The Type Theoretic Interpretation of Constructive Set Theory, Logic Colloquium 1977.

* Arai, A sneak preview of proof theory of ordinals, [arXiv 1102.0596](https://arxiv.org/abs/1102.0596).

* Arai, Proof theory for theories of ordinals III: $\Pi_N$-reflection, [arXiv 1007.0844](https://arxiv.org/abs/1007.0844).

* Arai, An ordinal analysis of $\Pi_1$-Collection, [arXiv 2112.09871](https://arxiv.org/abs/2112.09871)

* Buchholz, A simplified version of local predicativity, Proc. Proof Theory Meeting Leed '90.

* Buchholz, A Note on the Ordinal Analysis of KPM (2002).

* Buchholz, Feferman, Pohlers and Sieg, Iterated inductive definitions and subsystems of analysis: recent proof-theoretical studies, Lecture Notes in Mathematics 897 (1981).

* Dybjer and Setzer, Induction-recursion and initial algebras, APAL 124(1-3), 2003, pp. 1-47. DOI: 10.1016/S0168-0072(02)00096-9

* Feferman: Iterated inductive fixed-point theories: Application to Hancock's conjecture, in: G. Metakides (ed.): Patras Logic Symposium (North-Holland, Amsterdam, (1982), 171&#8211;196.

* J&#228;ger, Kahle, Setzer, and Strahm, The proof-theoretic analysis of transfinitely iterated fixed point theories, Journal of Symbolic Logic

* J&#228;ger and Strahm, Fixed point theories and dependent choice. Archive for Mathematical Logic.

* Rathjen, Ordinal notations based on a weakly Mahlo cardinal, Archive for Mathematical Logic 29 (1990), 249-263.

* Rathjen, Proof-theoretic analysis of KPM, Archive for Mathematical Logic (1991).

* Rathjen, The Recursively Mahlo Property in Second Order Arithmetic, Mathematical Logic Quarterly 42 (1996), 59-66.

* Rathjen, The strength of Martin-L&#246;f type theory with a superuniverse. Part II, 2001, AML, DOI: 10.1007/s001530000051
* Rathjen, The strength of Martin-L&#246;f type theory with a superuniverse. Part I, 2000, AML, DOI: 10.1007/s001530050001

* Rathjen, An ordinal analysis of parameter free $\Pi^1_2$-comprehension. Arch. Math. Log. 44(3), 263&#8211;362 (2005).

* Rathjen, The constructive Hilbert program and the limits of Martin-L&#246;f type theory (2005), Synthese, DOI: 10.1007/s11229-004-6208-4

* Rathjen, Griffor and Palmgren, Inaccessibility in Constructive Set Theory and Type Theory, APAL 94 (1998), 181-200.

* Setzer, An upper bound for the proof theoretical strength of Martin-L&#246;f Type Theory with W-type and one universe (2006)

* Strahm, Autonomous fixed point progressions and fixed point transfinite recursion, Proc. of Logic Colloquium '98, 449-464, [web](http://www.iam.unibe.ch/ltgpub/2000/str00a.pdf)

[[!redirects proof-theoretic ordinal]]
