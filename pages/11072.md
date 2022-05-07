+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In full [[linear logic]]/[[linear type theory]] there is assumed a (comonadic) [[modality]] denoted "!" and called the _exponential modality_, whose role is, roughly, to give linear types also a non-linear interpretation. This is also called  the "of course"-modality or the _storage modality_, and sometimes the "bang"-operation.

In classical linear logic (meaning with involutive de Morgan duality), the de Morgan dual of "!" is denoted "?" and called the "why not"-modality.

In [[categorical semantics]] of linear type theory the !-modality typically appears as a kind of [[Fock space]] construction. If one views [[linear logic]] as [[quantum logic]] (as discussed there), then this means that the !-modality produces [[free field theory|free]] [[second quantization]].


## Categorical semantics

Everyone agrees that ! should be a comonad (and ? should be a monad), but there are different ways to proceed from there.  The goal is to capture the syntactic rules allowing assumptions of the form $!A$ to be duplicated and discarded.

### Intuitionistic case

The original definition from [Seely](#Seely89), adapted to the intuitionistic case and modernized, is:

+-- {: .num_defn}
###### Definition
Let $C$ be an [[symmetric monoidal category]] with [[cartesian products]].  A **Seely comonad** on $C$ is a comonad that is a [[strong monoidal functor]] from the [[cartesian monoidal category|cartesian monoidal structure]] to the symmetric monoidal structure, i.e. we have $!(A\times B)\cong !A \otimes !B$ and $!1\cong I$ coherently.  (There is also an additional [[coherence]] [[axiom]] that should be imposed; see [Mellies, section 7.3](#Mellies09).)
=--

(Note that in linear logic, the cartesian monoidal structure $\times$ is sometimes denoted by $\&$.)  This implies that the [[Kleisli category of a comonad|Kleisli category]] of ! (i.e.\ the category of cofree !-coalgebras) is cartesian monoidal.  If $C$ is *closed* symmetric monoidal then the Kleisli category of a [[cartesian closed category]], which is a categorical version of the translation of intuitionistic logic into linear logic.

Of course, the above definition depends on the existence of the cartesian product.  A different definition that doesn't require the existence of $\times$ was given by [Benton, Bierman, de Paiva, and Hyland](#BBPH92):

+-- {: .num_defn}
###### Definition
Let $C$ be a [[symmetric monoidal category]]; a **linear exponential comonad** on $C$ is a [[lax monoidal functor|lax monoidal]] comonad such that every cofree !-coalgebra naturally carries the structure of a [[comonoid object]] in the category of coalgebras (i.e. the cofree-coalgebra functor lifts to the category of comonoids in the category of coalgebras).
=--

It follows automatically that all !-coalgebras are comonoids, and therefore that the category of all !-coalgebras (not just the cofree ones) is cartesian monoidal.  Note that for a comonad on a [[poset]], every coalgebra is free; thus the world of pure propositional "logic" doesn't tell us whether to consider the Kleisli category or the Eilenberg-Moore category for the translation.

A more even-handed approach is the following (see [Benton](#Benton95) and [Mellies](#Mellies09)), based on the observation that both Kleisli and Eilenberg-Moore categories are instances of adjunctions.

+-- {: .num_defn}
###### Definition
A **linear-nonlinear adjunction** is a [[monoidal adjunction]] $F : M \rightleftarrows L : G$ in which $L$ is symmetric monoidal and $M$ is cartesian monoidal.  The induced !-modality is the comonad $F G$ on $L$.
=--

This includes both of the previous definitions where $M$ is taken respectively to be the Kleisli category or the Eilenberg-Moore category of !.  Conversely, in any linear-nonlinear adjunction the induced comonad $F G$ can be shown to be a linear exponential comonad.  Moreover, if $!$ is a linear exponential comonad on a symmetric monoidal category $C$ with finite products, then the cofree !-coalgebra functor is a right adjoint and hence preserves cartesian products; but the cartesian products of coalgebras are the tensor product in $C$, so we have $!(A\times B) \cong !A \otimes !B$, the Seely condition.


### Classical case

For "classical" linear logic, we want $C$ to be not just (closed) symmetric monoidal but $\ast$-[[star-autonomous category|autonomous]].  If an $\ast$-autonomous category has a linear exponential comonad $!$ one can derive a ? from the ! by de Morgan duality, $?A = (!(A^*))^*$.  The resulting relationship between ! and ? was axiomatized in a way not requiring the de Morgan duality by [Blute, Cockett, and Seely](#BCS96):

+-- {: .num_defn}
###### Definition
Let $C$ be a [[linearly distributive category]] with tensor product $\otimes$ and cotensor product $\parr$.  A (!,?)-modality on $C$ consists of:

1. a $\otimes$-monoidal comonad ! and a $\parr$-comonoidal monad ?
1. ? is a !-strong monad, and ! is a ?-strong comonad
1. all free !-coalgebras are naturally commutative $\otimes$-comonoids, and all free ?-algebras are naturally commutative $\parr$-monoids.
=--

Here a functor $F$ is [[strong functor|strong]] with respect to a lax monoidal functor $G$ if there is a natural transformation $F A \otimes G B \to F(A\otimes G B)$ satisfying some natural axioms, and we similarly require compatibility of the monad and comonad structure transformations.  BCS showed that if $C$ is in fact $\ast$-autonomous, it follows from the above definition that $?A = (!(A^*))^*$ as expected.

## Examples

\begin{theorem}
Suppose $F : M \rightleftarrows C : G$ is a linear-nonlinear adjunction, where $C$ is closed symmetric monoidal with finite limits and colimits, and $\bot\in C$ is an object.  Then there is an induced linear-nonlinear adjunction $M \rightleftarrows Chu(C,\bot)$ where $Chu(C,\bot)$ is the [[Chu construction]] $Chu(C,\bot)$, which is $\ast$-autonomous with finite limits and colimits.  Hence $Chu(C,\bot)$ admits a !-modality.
\end{theorem}
\begin{proof}
The embedding of $C$ in $Chu(C,\bot)$ as $A \mapsto (A, [A,\bot], ev)$ is coreflective: the coreflection of $(B^+, B^-, e_B)$ is $(B^+, [B^+,\bot], ev)$.  Moreover, this subcategory is closed under the tensor product of $Chu(C,\bot)$, i.e. the embedding $C\hookrightarrow Chu(C,\bot)$ is strong monoidal, hence the adjunction is a monoidal adjunction.  Therefore, the composite adjunction $M \rightleftarrows C \rightleftarrows Chu(C,\bot)$ is again a linear-nonlinear-adjunction.
\end{proof}

Since a Chu construction is $\ast$-autonomous, this !-modality implies a dual ?-modality.

\begin{corollary}
If $C$ is a cartesian closed category with finite limits and colimits and $\bot\in C$ is an object, then there is a linear-nonlinear adjunction $C \rightleftarrows Chu(C,\bot)$, and hence $Chu(C,\bot)$ admits a !-modality.
\end{corollary}
\begin{proof}
Apply the previous theorem to the identity adjunction $C\rightleftarrows C$.
\end{proof}

Note that the !-modality obtained from the corollary is [[idempotent comonad|idempotent]], while that obtained from the theorem is idempotent if and only if the original one was.  Other ways of constructing !-modalities, such as by cofree coalgebras, may produce examples that are not idempotent.


## Modal term calculi

Girard's original presentation of linear logic involved rules that explicitly assumed the presence of $!$ on hypotheses or on entire contexts, such as [[weakening rule|weakening]] and [[contraction rule|contraction]]:

$$ \frac{\Gamma \vdash B}{\Gamma, !A\vdash B} \qquad \frac{\Gamma,!A,!A \vdash B}{\Gamma, !A\vdash B} $$

and "promotion":

$$ \frac{!\Gamma \vdash A}{!\Gamma\vdash !A} $$

If this is translated into a [[natural deduction]] style term calculus, the resulting rules are more complicated than those of most type formers.  This can be avoided using [[adjoint type theory]] with two context zones, one "nonlinear" one where contraction and weakening are permitted (and [[admissible rule|admissible]]) and one "linear" one where they are not, with $!$ as a modality relating the two zones.

Such a "modal" presentation of linear logic was first introduced by Girard in his work on [[LU]] and then developed by a number of other people such as Plotkin, Wadler, Benton, and Barber.  See the references for details.

This presentation also generalizes naturally to [[dependent linear type theory]], with the nonlinear type theory being dependent, and the linear types depending on the nonlinear ones but nothing depending on linear types.  In this context, the $!$-modality decomposes into "context extension" and a "dependent sum".


## Related concepts

* [[exponential map]]

* [[multiplicative conjunction]]

* [[linear implication]]

## References

The semantics of ! as a comonad is discussed in:

* {#Seely89} [[R. A. G. Seely]],  _Linear logic, $\ast$-autonomous categories and cofree coalgebras_, _Contemporary Mathematics_ 92, 1989.  ([[SeelyLinearLogic.pdf:file]], [ps.gz](http://www.math.mcgill.ca/rags/nets/llsac.ps.gz))
 

* {#BBPH92} [[Nick Benton]], Gavin Bierman, [[Valeria de Paiva]], [[Martin Hyland]], *Linear lambda-Calculus and Categorical Models Revisited* (1992), [citeseer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.31.6958)
 

* {#BCS96} R. F. Blute , J. R. B. Cockett and R. A. G. Seely.  *! and ? &#8211; Storage as tensorial strength* [doi](https://doi.org/10.1017/S0960129500001055), [pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.26.7317&rep=rep1&type=pdf)
 

* {#Mellies09} [[Paul-André Melliès]], *Categorical semantics of linear logic*, 2009. [pdf](https://www.irif.fr/~mellies/papers/panorama.pdf)



* [[Martin Hyland]] and Andreas Schalk, _Glueing and orthogonality for models of linear logic_, [pdf](http://www.cs.man.ac.uk/~schalk/publ/gomll.pdf)
 {#HylandSchalk01}
 
Construction of such comonads based on cofree comonoids can be found in (among other places):

* Mellies and Tabareau and Tasson, *An explicit formula for the free exponential modality of linear logic*. Mathematical Structures in Computer Science, 28(7), 1253-1286. doi:[10.1017/S0960129516000426](https://doi.org/10.1017/S0960129516000426)

* Sergey Slavnov, *On Banach spaces of sequences and free linear logic exponential modality*, Math. Struct. Comp. Sci. 29 (2019) 215-242, [arxiv](https://arxiv.org/abs/1509.03853)


The relation to Fock space is discussed in:

* {#BlutePanangadenSeely94} [[Richard Blute]], [[Prakash Panangaden]], [[R. A. G. Seely]], _Fock Space: A Model of Linear Exponential Types_ (1994) ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.27.6825), [[BPSLinear.pdf:file]])

* {#Fiore07} [[Marcelo Fiore]], _Differential Structure in Models of Multiplicative Biadditive Intuitionistic Linear Logic_, Lecture Notes in Computer Science Volume 4583, 2007, pp 163-177 ([pdf](http://www.cl.cam.ac.uk/~mpf23/papers/Types/diff.pdf))

* {#Vicary07} [[Jamie Vicary]], _A categorical framework for the quantum harmonic oscillator_, International Journal of Theoretical Physics December 2008, Volume 47, Issue 12, pp 3408-3447 ([arXiv:0706.0711](http://arxiv.org/abs/0706.0711))

  (in the context of [[finite quantum mechanics in terms of dagger-compact categories]])

The interpretation of $\Omega^\infty \Sigma^\infty_+$ as an exponential in the context of [[Goodwillie calculus]] is due to 

* {#AroneKankaanrinta95} [[Gregory Arone]], Marja Kankaanrinta,  _The Goodwillie tower of the identity is a logarithm_, 1995 ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.53.8306))

based on

* {#AroneMahowald98} [[Gregory Arone]], [[Mark Mahowald]], _The Goodwillie tower of the identity functor and the unstable periodic homotopy of spheres_, 1998 ([pdf](http://hopf.math.purdue.edu/Arone-Mahowald/ArMahowald.pdf))

The modal approach to a term calculus for the $!$-modality can be found in:

* [[Jean-Yves Girard]].  *On the unity of logic.* Annals  of Pure and Applied  Logic, 59:201-217, 1993.

* G.  Plotkin.  *Type  theory  and  recursion.*   In Proceedings  of  the  Eigth  Symposium  of Logic in Computer Science, Montreal , page 374. IEEE Computer Society Press, 1993.

* N. Benton.  *A mixed linear and non-linear logic; proofs, terms and models.*  In Proceedings of Computer Science Logic '94, number 933 in LNCS. Verlag, June 1995.
 {#Benton95}

* Philip  Wadler.   *A  syntax  for  linear  logic.*   In Ninth  International  Coference  on  the Mathematical Foundations of Programming Semantics , volume 802 of LNCS . Springer Verlag, April 1993

* Andrew Barber, *Dual Intuitionistic Linear Logic*, Technical Report ECS-LFCS-96-347, University of Edinburgh, Edinburgh (1996), [web](http://www.lfcs.inf.ed.ac.uk/reports/96/ECS-LFCS-96-347/)


A [[quantum programming language]] based on this linear/non-linear type theory adunction is [[QWIRE]]:

* [[Jennifer Paykin]], [[Robert Rand]], [[Steve Zdancewic]], *QWIRE: a core language for quantum circuits*, POPL 2017: Proceedings of the 44th ACM SIGPLAN Symposium on Principles of Programming LanguagesJanuary 2017 Pages 846–858 ([doi:10.1145/3009837.3009894](https://doi.org/10.1145/3009837.3009894))

theoretical background:

* [[Jennifer Paykin]], *Linear/non-Linear Types For Embedded Domain-Specific Languages*, 2018 ([upenn:2752](https://repository.upenn.edu/edissertations/2752))

applied to [[verified programming]] after implementation in [[Coq]]:

* [[Robert Rand]], [[Jennifer Paykin]], [[Steve Zdancewic]], *QWIRE Practice: Formal Verification of Quantum Circuits in Coq*, EPTCS 266, 2018, pp. 119-132 ([arXiv:1803.00699](https://arxiv.org/abs/1803.00699))

and using ambient [[homotopy type theory]]:

* [[Jennifer Paykin]], [[Steve Zdancewic]], *A HoTT Quantum Equational Theory*, [talk at QPL2019](http://qpl2019.org/a-hott-quantum-equational-theory/) ([arXiv:1904.04371](https://arxiv.org/abs/1904.04371))


category: logic

[[!redirects of course]]
[[!redirects !]]
[[!redirects why not]]
[[!redirects ?]]
[[!redirects exponential conjunction]]
[[!redirects exponential modality]]
[[!redirects storage modality]]
[[!redirects exponential modalities]]
[[!redirects storage modalities]]