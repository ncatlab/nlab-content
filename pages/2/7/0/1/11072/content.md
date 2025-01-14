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
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

In full [[linear logic]] &lbrack;[Girard 1987](#Girard1987)&rbrack; and more generally in [[linear type theory]] there is assumed a (comonadic) [[modality]] traditionally denoted "!" whose role is to model the "underlying" classical [[intuitionistic type theory|(intuitionistic) type]] of a given [[linear type]]. 

This is alternatively called the "exponential modality" (for good reasons discussed [below](#TheExponentialCondition)), or "storage modality" (as it allows to duplicate and hence "store" otherwise linear data) and sometimes pronounced "of course" (intended alongside "necessarily" and "possibly" as used in [[modal logic]]) or even "bang" (just in reference to the symbol "!").

In classical linear logic (meaning with involutive [[de Morgan duality]]), the de Morgan dual of "!" is denoted "?" and then sometimes pronounced "why not".

Today it is understood (cf. [Melliès 2009](#Melliès09), [p. 36](/nlab/files/Mellies-CategoricalSemanticsLinear.pdf#page=36))
that the exponential modality is best and generally to be thought as as, first of all a *[[comonad]]* on [[linear types]] ([Seely 1989  §2](#Seely89), [dePaiva 1989](#dePaiva89), [Benton, Bierman, de Paiva and Hyland 1992](#BBPH92)) which, secondly, is [induced](monad#RelationBetweenAdjunctionsAndMonads) by an adjunction to classical (meaning here: non-linear [[intuitionistic type theory|intuitionistic]]) types with special [[monoidal functor|monoidal]] properties ([Seely 1989  §2](#Seely89), [Bierman 1994 pp. 157](#Bierman94), [Benton 1995](#Benton95)).

In a most elementary and illuminating example (which may not have received the attention it deserves, cf. the history at *[[quantum logic]]*):

* classical intuitionistic types form (are interpreted in) the category of [[Sets]]

  $ClaTypes \,\coloneqq\, Set$

* linear types form (are interpreted in) the category of [[vector spaces]] (cf. [Murfet 2014](linear+logic#Murfet14))

  $LinTypes  \,\coloneqq\, Vect_{\mathbb{K}}$

and the [[adjoint functors]] in question are

* forming the [[linear span]] of a set

  $$
    \array{
      Set &\overset{\mathrm{Q}}{\longrightarrow}& Vect
      \\
      W &\mapsto& \oplus_W \mathbb{1}
    }
  $$

* forming the [[underlying set]] of a [[vector space]]:

  $$
    \array{
      Vect &\overset{\mathrm{C}}{\longrightarrow}& Set
      \\
      \mathscr{V} &\mapsto& Hom(\mathbb{1}, \, \mathscr{V})
    }
  $$

in which case the exponential modality acts by sending a vector space to the linear span of its underlying set

\[
  \array{
     Vect &\overset{\;\; ! \;\;}{\longrightarrow}& Vect
     \\
     \mathscr{V} &\mapsto& \underset{\mathscr{V}}{\bigoplus} \mathbb{1}
     \,.
  }
\]

One sees that this construction takes ([[direct sums|direct]]) sums to ([[tensor product of vector spaces|tensor]]) products

$$
  !(\mathscr{V} \oplus \mathscr{V}')
  \;\simeq\;
  (! \mathscr{V}) \otimes (! \mathscr{V}')
$$

and zero ([[zero object|objects]]) to unit ([[unit object|objects]])

$$
  ! 0 
    \;\simeq\;
  \mathbb{1}
$$

as expected of any [[exponential map]], whence the name "exponential modality".

This example is the 0-sector of the more famous *[[stabilization]]* ([[(infinity,1)-adjoint functor|$\infty$-]])adjunction $(\Sigma_+^\infty \dashv \Omega_+^\infty)$  between (the [[homotopy theory]] of) [[topological spaces]] and (the [[stable homotopy theory]] of) [[module spectra|module]] [[spectra]] equipped with the [[symmetric smash product of spectra]] (given by forming [[suspension spectra]] $X \mapsto \Sigma_+^\infty X$), which points to a deeper origin of the "exponential modality", see [below](#RealizationInLinearHomotopyTypeTheory) and at *[[linear homotopy type theory]]* for more on this.

<center>
<img src="https://ncatlab.org/nlab/files/QuantClassExponential-230821.jpg" width="600"/>
</center>


## Categorical semantics

Following [Seely 1989](#Seely89), [dePaiva 1989](#dePaiva89), [Benton, Bierman, de Paiva and Hyland 1992](#BBPH92) it is common convention that "!" should be a [[comonad]] on the type system (and ? should be a [[monad]], see also at *[[monads in computer science]]*), but there is some room in which further axioms to impose. 
The goal is to capture the syntactic rules allowing assumptions of the form $!A$ to be duplicated and discarded.

### Intuitionistic case

The definition from [Seely](#Seely89), adapted to the intuitionistic case and modernized, is:

+-- {: .num_defn}
###### Definition
Let $LinTypes$ be 

* a [[cartesian monoidal category]], with [[Cartesian product]] "$\times$" and [[tensor unit]] the [[terminal object]] $\ast$.

which *in addition* carries the [[structure]] of 

* a [[symmetric monoidal category]] with respect to a [[tensor product]] $\otimes$ with [[tensor unit]] $\mathbb{1}$.

A **Seely comonad** on $LinTypes$ is a [[comonad]] that is a [[strong monoidal functor|strong monoidal]] as a functor from cartesian monoidal structure $\times$ to the other monoidal structure $\otimes$: 


$$
  (LinTypes, \times)
  \xrightarrow{ \; ! \; }
  (LinTypes, \otimes)
$$

meaning that there are [[natural transformations]] of the form

\[
  \label{StrongMonoidalPropertyOfExponential}
  A,\, B \colon LinTypes
  \;\;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;\;
  !(A \times B) 
   \;\cong\; 
  (!A) \otimes (!B) 
\] 

and

\[
  ! \ast \;\;\simeq\;\; \mathbb{1}
  \,.
\]

=--

(There is also an additional [[coherence]] [[axiom]] that should be imposed; see [Melliès 2009, section 7.3](#Melliès09).)


\begin{remark}\label{TheExponentialCondition}
**(the exponential condition)**
\linebreak
In [[linear logic]], the cartesian monoidal structure on linear types is often denoted "$\&$" ("[[additive conjunction]]"), in which case the condition (eq:StrongMonoidalPropertyOfExponential) reads

\[
  !(A \& B) 
   \;\cong\; 
  (!A) \otimes (!B) 
  \,.
\] 

But in key examples of categories of (the multiplicative fragment of) linear logic (such as [[Vect]], cf. [Murfet 2014](linear+logic#Murfet14)), the [[cartesian product]] is actually a [[biproduct]], hence a [[direct sum]], in which case the condition on the exponential modality is that 

*it takes (direct) sums to (tensor) products*

\[
  !(A \oplus B) 
   \;\cong\; 
  (!A) \otimes (!B) 
\] 

*it takes zero (objects) to unit (objects)*

\[
  ! 0 
    \;\cong\;
  \mathbb{1}
\]

as befits any [[exponential map]] and may explain the choice of terminology here.
\end{remark}


This condition implies that the [[Kleisli category of a comonad|Kleisli category]] of $!$ (i.e. the category of cofree !-coalgebras) is cartesian monoidal.  If $LinTypes$ is *[[closed monoidal category|closed]]* symmetric monoidal then the Kleisli category of a [[cartesian closed category]], which is a categorical version of the translation of intuitionistic logic into linear logic.

Of course, the above definition depends on the existence of the cartesian product.  A different definition that doesn't require the existence of $\times$ was given by [Benton, Bierman, de Paiva, and Hyland](#BBPH92):

+-- {: .num_defn}
###### Definition

Let $LinTypes$ be a [[symmetric monoidal category]]; a **linear exponential comonad** on $LinTypes$ is a [[lax monoidal functor|lax monoidal]] comonad such that every cofree !-coalgebra naturally carries the structure of a [[comonoid object]] in the category of coalgebras (i.e. the cofree-coalgebra functor lifts to the category of comonoids in the category of coalgebras).

=--

It follows automatically that all !-coalgebras are comonoids, and therefore that the category of all !-coalgebras (not just the cofree ones) is cartesian monoidal.  Note that for a comonad on a [[poset]], every coalgebra is free; thus the world of pure propositional "logic" doesn't tell us whether to consider the Kleisli category or the Eilenberg-Moore category for the translation.

A more even-handed approach is the following (see [Benton (1995)](#Benton95) and [Melliès (2009)](#Melliès09)), based on the observation that both Kleisli and Eilenberg-Moore categories are instances of adjunctions.

\begin{definition}
\label{LinearNonlinearAdjunction}

A **linear-nonlinear adjunction** is a [[monoidal adjunction]] $F \colon ClaTypes \rightleftarrows LinTypes \colon G$ in which $LinTypes$ is symmetric monoidal and $ClaTypes$ is cartesian monoidal.  The induced !-modality is the induced [[comonad]] $F G$ on $LinTypes$.

\end{definition}


This includes both of the previous definitions where $M$ is taken respectively to be the Kleisli category or the Eilenberg-Moore category of !.  Conversely, in any linear-nonlinear adjunction the induced comonad $F G$ can be shown to be a linear exponential comonad.  Moreover, if $!$ is a linear exponential comonad on a symmetric monoidal category $LinTypes$ with finite products, then the cofree !-coalgebra functor is a right adjoint and hence preserves cartesian products; but the cartesian products of coalgebras are the tensor products in $C$, so we have $!(A\times B) \cong !A \otimes !B$, the Seely condition.


### Classical case

For "classical" linear logic, we want $LinTypes$ to be not just (closed) symmetric monoidal but $\ast$-[[star-autonomous category|autonomous]].  If an $\ast$-autonomous category has a linear exponential comonad $!$ one can derive a ? from the ! by [[de Morgan duality]], $?A = \big(!(A^*)\big)^*$.  The resulting relationship between ! and ? was axiomatized in a way not requiring the de Morgan duality by [Blute, Cockett & Seely (1996)](#BluteCockettSeely96):

+-- {: .num_defn}
###### Definition
Let $LinTypes$ be a [[linearly distributive category]] with tensor product $\otimes$ and cotensor product $\parr$.  A (!,?)-modality on $LinTypes$ consists of:

1. a $\otimes$-monoidal comonad ! and a $\parr$-comonoidal monad ?

1. ? is a !-strong monad, and ! is a ?-strong comonad

1. all free !-coalgebras are naturally commutative $\otimes$-comonoids, and all free ?-algebras are naturally commutative $\parr$-monoids.

=--

Here a functor $F$ is [[strong functor|strong]] with respect to a [[lax monoidal functor]] $G$ if there is a [[natural transformation]] of the form $F A \otimes G B \to F(A\otimes G B)$ satisfying some natural axioms, and we similarly require compatibility of the monad and comonad structure transformations.  [BCS96](#BluteCockettSeely96) showed that if $LinTypes$ is in fact $\ast$-autonomous, it follows from the above definition that $?A = \big(!(A^*)\big)^*$, as expected.

## Examples

### Relation to Chu construction

\begin{theorem}
Suppose $F \colon M \rightleftarrows C : G$ is a linear-nonlinear adjunction (Def. \ref{LinearNonlinearAdjunction}), where $C$ is closed symmetric monoidal with finite limits and colimits, and $\bot\in C$ is an object.  Then there is an induced linear-nonlinear adjunction $M \rightleftarrows Chu(C,\bot)$ where $Chu(C,\bot)$ is the [[Chu construction]] $Chu(C,\bot)$, which is $\ast$-autonomous with finite limits and colimits.  Hence $Chu(C,\bot)$ admits a !-modality.
\end{theorem}
\begin{proof}
The embedding of $C$ in $Chu(C,\bot)$ as $A \mapsto (A, [A,\bot], ev)$ is coreflective: the coreflection of $(B^+, B^-, e_B)$ is $(B^+, [B^+,\bot], ev)$.  Moreover, this subcategory is closed under the tensor product of $Chu(C,\bot)$, i.e. the embedding $C\hookrightarrow Chu(C,\bot)$ is strong monoidal, hence the adjunction is a monoidal adjunction.  Therefore, the composite adjunction $M \rightleftarrows C \rightleftarrows Chu(C,\bot)$ is again a linear-nonlinear-adjunction.
\end{proof}

Note that this theorem is a direct consequence of the work of [[Yves Lafont]] and [[Thomas Streicher]] on game semantics using the Chu construction, together with Benton's reformulation of linear logic in terms of  monoidal adjunctions. Since a Chu construction is $\ast$-autonomous, this !-modality implies a dual ?-modality.

\begin{corollary}
If $C$ is a cartesian closed category with finite limits and colimits and $\bot\in C$ is an object, then there is a linear-nonlinear adjunction $C \rightleftarrows Chu(C,\bot)$, and hence $Chu(C,\bot)$ admits a !-modality.
\end{corollary}
\begin{proof}
Apply the previous theorem to the identity adjunction $C\rightleftarrows C$.
\end{proof}

Note that the !-modality obtained from the corollary is [[idempotent comonad|idempotent]], while that obtained from the theorem is idempotent if and only if the original one was.  Other ways of constructing !-modalities, such as by cofree coalgebras, may produce examples that are not idempotent.

### Realization in linear homotopy type theory
 {#RealizationInLinearHomotopyTypeTheory}

In [[dependent linear homotopy type theory]] the "linear-nonlinear adjunction" is naturally identified ([Ponto & Shulman (2012), Ex. 4.2](#PontoShulman12), see also [Schreiber (2014), Sec. 4.2](#Schreiber14)) with the [[stabilization]] [[adjoint functor|adjunction]] between [[homotopy types]] and [[stable homotopy types]] ([Riley (2022), Prop. 2.1.31](#Riley22Thesis)), whose [[left adjoint]] (forming [[suspension spectra]] $\Sigma^\infty_+$) is equivalently given (cf. [Riley (2022), Rem. 2.4.13](#Riley22Thesis)) by sending $B \,\colon\, Type$ to the linear [[dependent sum]] $\star_B \mathbb{1} \;\coloneqq\; (p_B)_! (p_B)^\ast \mathbb{1}$ over the monoidal unit in the context $B$. In terms of [quantum modal logic](necessity+and+possibility#ModalQuantumLogic) this is forming the "linear randomization" of the given classical homotopy type (its "[[motive]]"): 

\[
  \label{MotivizationInLHott}
\]

\begin{imagefromfile}
    "file_name": "MotivizationInLHoTT-230825b.jpg",
    "width": "460",
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


Curiously, this homotopy-theoretic realization of the exponential modality (beware the little subtlety of whether or not to reflect onto [[pointed homotopy types]])

$$
  \Sigma^\infty \circ \Omega^\infty
  \;\colon\;
  Spectra \to Spectra
$$

has independently been argued to have properties of an [[exponential map]] in the context of [[Goodwillie calculus]], see [there](Goodwillie+calculus#GoodwillieDerivativeOfExponentialModality).

{#ComonadicityOfClassicalOverLinearHomotopyTypes} Moreover $\Sigma^\infty \dashv \Omega^\infty$ is a [[comonadic adjunction]] on [[simply connected homotopy type|simply connected]] [[homotopy types]] &lbrack;[Blomquist & Harper 2016  Thm. 1.8](#BlomquistHarper16); [Hess & Kedziorek 2017 Thm. 3.11](#HessKedziorek17)&rbrack;, meaning that simply-connected classical (but [[pointed homotopy types|pointed]]) homotopy types are identified with the $\Sigma^\infty \Omega^\infty$-[[modales]] among [[stable homotopy types]].

### Antithesis interpretation

In the [[antithesis interpretation]] of [[affine logic]] into [[impredicative mathematics|impredicative]] [[constructive mathematics]], given the [[set of truth values]] $\Omega$, one can define a [[set]] of [[type of affine propositions|affine propositions]] by the set 

$$\Omega_\pm \coloneqq \{(P^+, P^-) \in \Omega \times \Omega \vdash \neg (P^+ \wedge P^-)\}$$

The !-modality is a function $!:\Omega_\pm \to \Omega_\pm$ is defined for each affine proposition $(P^+, P^-) \in \Omega_\pm$ by 

$$!(P^+, P^-) \coloneqq (P^+, \neg P^+)$$

\begin{theorem}
The !-modality is equal to the [[multiplicative conjunction]] of $(P^+, P^-)$ with itself

$$!(P^+, P^-) = (P^+, P^-) \otimes (P^+, P^-)$$
\end{theorem}

\begin{proof}
The multiplicative conjunction is given by 
$$(P^+, P^-) \otimes (P^+, P^-) = (P^+ \wedge P^+, (P^+ \Rightarrow P^-) \wedge (P^+ \Rightarrow P^-))$$
Given two propositions $P^+$ and $P^-$ such that $\neg (P^+ \wedge P^-)$, we have $\neg P^+ = P^+ \Rightarrow P^-$. Since intuitionistic [[conjunction]] is [[idempotent]], we have 
$$(P^+, P^-) \otimes (P^+, P^-) = (P^+ \wedge P^+, (P^+ \Rightarrow P^-) \wedge (P^+ \Rightarrow P^-)) = (P^+ \wedge P^+, \neg P^+ \wedge \neg P^+) = (P^+, \neg P^+) = !(P^+, P^-)$$
\end{proof}

## Modal term calculi

Girard's original presentation of linear logic involved rules that explicitly assumed the presence of $!$ on hypotheses or on entire contexts, such as [[dereliction rule| dereliction]], [[weakening rule|weakening]] and [[contraction rule|contraction]]:

$$\frac{\Gamma, A \vdash B}{\Gamma, !A \vdash B} \qquad \frac{\Gamma \vdash B}{\Gamma, !A\vdash B} \qquad \frac{\Gamma,!A,!A \vdash B}{\Gamma, !A\vdash B}$$

and "promotion":

$$ \frac{!\Gamma \vdash A}{!\Gamma\vdash !A} $$

If this is translated into a [[natural deduction]] style term calculus, the resulting rules are more complicated than those of most type formers.  This can be avoided using [[adjoint type theory]] with two context zones, one "nonlinear" one where contraction and weakening are permitted (and [[admissible rule|admissible]]) and one "linear" one where they are not, with $!$ as a modality relating the two zones.

Such a "modal" presentation of linear logic was first introduced by [Girard 1993](#Girard93) and then developed by [Plotkin 1993](#Plotkin93), [Wadler 1993](#Wadler93), [Benton 1995](#Benton95), [Barber 1996](#Barber96).

This presentation also generalizes naturally to [[dependent linear type theory]], with the nonlinear type theory being dependent, and the linear types depending on the nonlinear ones but nothing depending on linear types.  In this context, the $!$-modality decomposes into "context extension" and a "dependent sum".


## Related concepts

* [[exponential map]]


[[!include logic symbols -- table]]


## References

### General

The notion of the exponential modality originates in [[linear logic]] with 

* {#Girard1987} [[Jean-Yves Girard]], _Linear logic_,   Theoretical Computer Science **50** 1 (1987)  &lbrack;<a href="https://doi.org/10.1016/0304-3975(87)90045-4">doi:10.1016/0304-3975(87)90045-4</a>, [pdf](http://iml.univ-mrs.fr/~girard/linear.pdf)&rbrack;
 
A streamlined statement of the [[inference rules]] and the observation that these make the exponential a [[comonad]] is due to:

* {#Seely89} [[R. A. G. Seely]], §2 of: *Linear logic, $\ast$-autonomous categories and cofree coalgebras*, in *Categories in Computer Science and Logic*, Contemporary Mathematics **92** (1989)  &lbrack;[[SeelyLinearLogic.pdf:file]], [ps.gz](http://www.math.mcgill.ca/rags/nets/llsac.ps.gz), [ISBN:978-0-8218-5100-5](https://bookstore.ams.org/conm-92)&rbrack;

* {#dePaiva89} [[ Valeria de Paiva]], §2 of: *The Dialectica Categories*, in *Categories in Computer Science and Logic*, Contemporary Mathematics **92** (1989)  &lbrack;[ISBN:978-0-8218-5100-5](https://bookstore.ams.org/conm-92), [doi:10.1090/conm/092](https://doi.org/10.1090/conm/092)&rbrack;

Review:

* [[Anne Sjerp Troelstra]], §12 in: *Lectures on Linear Logic* (1992) &lbrack;[ISBN:0937073776](https://web.stanford.edu/group/cslipublications/cslipublications/site/0937073776.shtml)&rbrack;


Brief survey in a context of [[computer science]]/[[linear type theory]]:

* {#MihályiNovitzká13} Daniel Mihályi, Valerie Novitzká, Section 2.2 of: *What about Linear Logic in Computer Science?*, Acta Polytechnica Hungarica **10** 4 (2013) 147-160 &lbrack;[pdf](http://acta.uni-obuda.hu/Mihalyi_Novitzka_42.pdf), [[MihalyiNovitzka-LinearLogic.pdf:file]]&rbrack;


Further on the semantics of exponential conjunction as a [[comonad]]:

* {#deP1988} [[Valeria de Paiva]], *The Dialectica Categories*, PhD thesis, technical report 213, Computer Laboratory, University of Cambridge (1991) &lbrack;[pdf](https://www.cl.cam.ac.uk/techreports/UCAM-CL-TR-213.pdf), [[dePaivaDialectica.pdf:file]]&rbrack;

* {#BBP92} [[Nick Benton]], [[Gavin Bierman]], [[Valeria de Paiva]], §8 of: *Term assignment for intuitionistic linear logic*, Technical report 262, Computer Laboratory, University of Cambridge (August 1992) &lbrack;[pdf](https://www.cl.cam.ac.uk/techreports/UCAM-CL-TR-262.pdf), [[BentonBiermanDePaiva-TermAssignment.pdf:file]]&rbrack; 

  > (published abridged as [BBPH92](#BBPH92))
  
* {#BBPH92} [[Nick Benton]], [[Gavin Bierman]], [[Valeria de Paiva]], [[Martin Hyland]], *Linear $\lambda$-Calculus and Categorical Models Revisited*, in *Computer Science Logic. CSL 1992*, Lecture Notes in Computer Science **702**, Springer (1993) &lbrack;[doi:10.1007/3-540-56992-8_6](https://doi.org/10.1007/3-540-56992-8_6)&rbrack;

  > (abridged version of [BBP92](#BBP92))
 
* {#BluteCockettSeely96} [[R. F. Blute]] , [[J. R. B. Cockett]], [[R. A. G. Seely]], *! and ? -- Storage as tensorial strength*, Mathematical Structures in Computer Science **6** 4 (1996) 313-351 &lbrack;[doi:10.1017/S0960129500001055](https://doi.org/10.1017/S0960129500001055)&rbrack;
 
* {#HylandSchalk01} [[Martin Hyland]] and Andreas Schalk, _Glueing and orthogonality for models of linear logic_, [pdf](http://www.cs.man.ac.uk/~schalk/publ/gomll.pdf)

and its [resolution](monad#CategoryOfAdjunctionResolutionsOfAMonad) by a [[monoidal adjunction]] between the linear and a classical (intuitionistic) type system:

* {#Bierman94} [[Gavin Bierman]], *On Intuitionistic Linear Logic*, Cambridge (1994)  &lbrack;[[Bierman-LinearLogic.pdf:file]], [pdf](https://www.dropbox.com/s/hdxgubjljb96rmf/Biermanthesis.pdf?dl=0)&rbrack;

* {#Benton95} [[Nick Benton]], *A mixed linear and non-linear logic: Proofs, terms and models*, in *Computer Science Logic. CSL 1994*, Lecture Notes in Computer Science **933** (1995) 121-135 &lbrack;[doi:10.1007/BFb0022251](https://doi.org/10.1007/BFb0022251), [[BentonLinearLogic.pdf:file]]&rbrack;
 


Review:

* {#Melliès02} [[Paul-André Melliès]], *Categorical models of linear logic revisited* (2002) &lbrack;[hal:00154229](https://hal.science/hal-00154229)&rbrack;

* {#Melliès09} [[Paul-André Melliès]], *Categorical semantics of linear logic*, in *[Interactive models of computation and program behaviour](https://smf.emath.fr/publications/modeles-interactifs-de-calcul-et-de-comportement-de-programme)*, Panoramas et synthèses **27** (2009) 1-196 &lbrack;[web](https://smf.emath.fr/publications/semantique-categorielle-de-la-logique-lineaire), [pdf](https://www.irif.fr/~mellies/papers/panorama.pdf), [[Mellies-CategoricalSemanticsLinear.pdf:file]]&rbrack;

 
 
Construction of such comonads based on cofree comonoids:

* Mellies and Tabareau and Tasson, *An explicit formula for the free exponential modality of linear logic*. Mathematical Structures in Computer Science, 28(7), 1253-1286. doi:[10.1017/S0960129516000426](https://doi.org/10.1017/S0960129516000426)

* [[Sergey Slavnov]], *On Banach spaces of sequences and free linear logic exponential modality*, Math. Struct. Comp. Sci. 29 (2019) 215-242, [arXiv:1509.03853](https://arxiv.org/abs/1509.03853)


The relation to [[Fock space]] is discussed in:

* {#BlutePanangadenSeely94} [[Richard Blute]], [[Prakash Panangaden]], [[R. A. G. Seely]], _Fock Space: A Model of Linear Exponential Types_ (1994) ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.27.6825), [[BPSLinear.pdf:file]])

* {#Fiore07} [[Marcelo Fiore]], _Differential Structure in Models of Multiplicative Biadditive Intuitionistic Linear Logic_, Lecture Notes in Computer Science Volume 4583, 2007, pp 163-177 ([pdf](http://www.cl.cam.ac.uk/~mpf23/papers/Types/diff.pdf))

* {#Vicary07} [[Jamie Vicary]], _A categorical framework for the quantum harmonic oscillator_, International Journal of Theoretical Physics December 2008, Volume 47, Issue 12, pp 3408-3447 ([arXiv:0706.0711](http://arxiv.org/abs/0706.0711))

  > (in the context of [[quantum information theory in terms of dagger-compact categories]])

The interpretation of $\Omega^\infty \Sigma^\infty_+$ as an exponential in the context of [[Goodwillie calculus]] is due to 

* {#AroneKankaanrinta95} [[Gregory Arone]], Marja Kankaanrinta,  _The Goodwillie tower of the identity is a logarithm_, 1995 ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.53.8306))

based on

* {#AroneMahowald98} [[Gregory Arone]], [[Mark Mahowald]], _The Goodwillie tower of the identity functor and the unstable periodic homotopy of spheres_, 1998 ([pdf](http://hopf.math.purdue.edu/Arone-Mahowald/ArMahowald.pdf))

On the [[modal type theory]]-approach to a term calculus for the $!$-modality:

* {#Girard93} [[Jean-Yves Girard]].  *On the unity of logic* Annals of Pure and Applied  Logic **59** (1993) 201-217 &lbrack;<a href="https://doi.org/10.1016/0168-0072(93)90093-S">doi:10.1016/0168-0072(93)90093-S</a>&rbrack;

* {#Plotkin93} [[Gordon Plotkin]], *Type theory and recursion*, in: Proceedings  of  the  Eigth  Symposium  of Logic in Computer Science, Montreal , IEEE Computer Society Press (1993) 374 &lbrack;[doi:10.1109/LICS.1993.287571](https://doi.org/10.1109/LICS.1993.287571)&rbrack;

* {#Wadler93} [[Philip  Wadler]], *A syntax for linear logic*, in: *Ninth  International  Coference  on  the Mathematical Foundations of Programming Semantics*, Lecture Notes in Computer Science **802** Springer (1993) &lbrack;[doi:10.1007/3-540-58027-1_24](https://doi.org/10.1007/3-540-58027-1_24)&rbrack;

* [Benton 1995](#Benton95)

* {#Barber96} Andrew Barber, *Dual Intuitionistic Linear Logic*, Technical Report ECS-LFCS-96-347, University of Edinburgh (1996), &lbrack;[web](http://www.lfcs.inf.ed.ac.uk/reports/96/ECS-LFCS-96-347/), [pdf](http://www.lfcs.inf.ed.ac.uk/reports/96/ECS-LFCS-96-347/ECS-LFCS-96-347.pdf), [[Barber-DualIntLinLogic.pdf:file]]&rbrack;


A [[quantum programming language]] based on this linear/non-linear type theory adunction is [[QWIRE]]:

* [[Jennifer Paykin]], [[Robert Rand]], [[Steve Zdancewic]], *QWIRE: a core language for quantum circuits*, POPL 2017: Proceedings of the 44th ACM SIGPLAN Symposium on Principles of Programming LanguagesJanuary 2017 Pages 846–858 ([doi:10.1145/3009837.3009894](https://doi.org/10.1145/3009837.3009894))

theoretical background:

* [[Jennifer Paykin]], *Linear/non-Linear Types For Embedded Domain-Specific Languages*, 2018 ([upenn:2752](https://repository.upenn.edu/edissertations/2752))

applied to [[verified programming]] after implementation in [[Coq]]:

* [[Robert Rand]], [[Jennifer Paykin]], [[Steve Zdancewic]], *QWIRE Practice: Formal Verification of Quantum Circuits in Coq*, EPTCS 266, 2018, pp. 119-132 ([arXiv:1803.00699](https://arxiv.org/abs/1803.00699))

and using ambient [[homotopy type theory]]:

* [[Jennifer Paykin]], [[Steve Zdancewic]], *A HoTT Quantum Equational Theory*, [talk at QPL2019](http://qpl2019.org/a-hott-quantum-equational-theory/) ([arXiv:1904.04371](https://arxiv.org/abs/1904.04371))

The !-modality in [[affine logic]] applied to [[constructive mathematics]]:

* {#Shulman2022} [[Michael Shulman]], *Affine logic for constructive mathematics*. Bulletin of Symbolic Logic, Volume 28, Issue 3, September 2022. pp. 327 - 386 ([doi:10.1017/bsl.2022.28](https://doi.org/10.1017/bsl.2022.28), [arXiv:1805.07518](https://arxiv.org/abs/1805.07518))

### In dependent linear type theory

Discussion of the exponential modality via [[stabilization]] in [[dependent linear homotopy type theory]]:

* {#PontoShulman12} [[Kate Ponto]], [[Mike Shulman]], Ex. 4.2 in: *Duality and traces in indexed monoidal categories*, Theory and Applications of Categories **26** 23 (2012)  &lbrack;[arXiv:1211.1555](http://arxiv.org/abs/1211.1555), [tac:26-23](http://www.tac.mta.ca/tac/volumes/26/23/26-23abs.html),  [blog](http://golem.ph.utexas.edu/category/2011/11/traces_in_indexed_monoidal_cat.html)&rbrack;

* {#Schreiber14} [[Urs Schreiber]], Sec. 4.2 of: *[[schreiber:Quantization via Linear homotopy types]]* &lbrack;[arXiv:1402.7041](http://arxiv.org/abs/1402.7041)&rbrack;

* {#Riley22Thesis} [[Mitchell Riley]], §2.1.2 in: *A Bunched Homotopy Type Theory for Synthetic Stable Homotopy Theory*, PhD Thesis (2022) &lbrack;[doi:10.14418/wes01.3.139](https://doi.org/10.14418/wes01.3.139)&rbrack;

The $\Omega^\infty \Sigma^\infty$ [[comonadic functor|comonadicity]] of simply connected pointed spaces over spectra: 

* {#BlomquistHarper16} Jacobson R. Blomquist, John E. Harper, Thm. 1.8 in: *Suspension spectra and higher stabilization* &lbrack;[arXiv:1612.08623](https://arxiv.org/abs/1612.08623)&rbrack;

* {#HessKedziorek17} [[Kathryn Hess]], [[Magdalena Kedziorek]], Thm. 3.11 in: *The homotopy theory of coalgebras over simplicial comonads*, Homology, Homotopy and Applications **21** 1 (2019) &lbrack;[arXiv:1707.07104](https://arxiv.org/abs/1707.07104), [doi:10.4310/HHA.2019.v21.n1.a11](https://dx.doi.org/10.4310/HHA.2019.v21.n1.a11)&rbrack;


category: logic

[[!redirects of course]]
[[!redirects !]]
[[!redirects !-modality]]
[[!redirects exponential conjunction]]
[[!redirects exponential modality]]
[[!redirects storage modality]]
[[!redirects exponential modalities]]
[[!redirects storage modalities]]

[[!redirects dereliction]]
[[!redirects derelictions]]
[[!redirects dereliction rule]]
[[!redirects dereliction rules]]

