
#Contents#
* table of contents
{:toc}

(work in progress)

## Idea

Differential linear logic is an extension of [[linear logic]]. New inference rules are added which allow to differentiate proofs. Proofs must be understood as morphisms and the new inference rules are here to differentiate them. It was realised than in some denotational models of linear logic, the morphisms of the [[co-Kleisli category]] are differentiable, and it was then reflected in the syntax by these new inference rules. Thus, one really needs to take the point of view of [[computational trinitarianism]] in order to understand the transition from linear logic to differential linear logic. It is more difficult to understand naively the proofs of differential linear logic than the ones of linear logic.

Differential linear logic can be presented in different guises whether we include the additives or not, and whether we include the promotion or not. We start by presenting the version without additives and with promotion. We will refer to this logic as DiLL.

## Syntax

There are two ways to present the syntax in  [[sequent calculus]]. With bilateral sequents or monolateral sequents. The first one is closer to the language of category theory but the second one allows to make the links with the syntax in [[proof nets]] and to divide by two the number of inference rules. Using the monolateral version (or proof nets) require to quotient the formulas by some equalities related to negation and [[De Morgan duality]].

### Formulas - Generalities

There are no novelties concerning formulas compared to linear logic. We will work with the formulas of Multiplicative Exponential Linear Logic (MELL). In the next subsection, the difference between MELL and DiLL will appear as additional inference rules.

Formulas are given by induction starting from atoms and applying connectives. In accordance with the tradition, formulas and atoms are denoted in the same way by upper case letters:

* Atoms are denoted by upper case letter $A,B,...$.
* If we have two formulas $A,B$, we can form $A \otimes B$.
* If we have two formulas $A,B$, we can form $A \parr B$.
* If we have a formula $A$, we can form $!{A}$.
* If we have a formula $A$, we can form $?{A}$.
* If we have a formula $A$, we can form $A^\perp$.
* We have the formula $1$.
* We have the formula $\bot$.

### Formulas - Quotienting by duality in monolateral syntax

If we want to use the monolateral sequent calculus (or proof nets), formulas must be quotiented by the following equalities:

* If we have a formula $A$, we put $A^{\perp\perp} = A$.
* If we have two formulas $A,B$, we put $(A \otimes B)^\perp = A^\perp \parr B^\perp$.
* If we have two formulas $A,B$, we put $(A \parr B)^\perp = A^\perp \otimes B^\perp$.
* If we have a formula $A$, we put $(!{A})^\perp = ?{A^\perp}$.
* If we have a formula $A$, we put $(?{A})^\perp = !{A^\perp}$.
* We have $1^\perp = \bot$.
* We have $\bot^\perp = 1$.

Notice that some equalities are implied by other ones and thus we could give a shorter list. We have preferred writing directly all the equalities of practical use.

### Inference rules - Bilateral syntax

Inference rules will allow us to build proofs. Notice that compared to MELL, we need the ability to sum proofs. We give an explicit rule for this summation of proofs. We give also a rule for null proofs. Finally, the new inference rules are: codereliction, cocontraction, coweakening, sum of proofs, null proof.

* Axiom: $\frac{}{A \vdash A}^{ax}$
* Left exchange: $\frac{\Gamma_{1},A,B,\Gamma_{2} \vdash \Delta}{\Gamma_{1},B,A,\Gamma_{2} \vdash \Delta}$
* Right exchange: $\frac{\Gamma \vdash \Delta_{1},A,B,\Delta_{2}}{\Gamma \vdash \Delta_{1},B,A,\Delta_{2}}$
* Left $\otimes$: $\frac{\Gamma_{1}, A, B, \Gamma_{2} \vdash \Delta}{\Gamma_{1}, A \otimes B, \Gamma_{2} \vdash \Delta}$
* Right $\parr$: $\frac{\Gamma \vdash \Delta_{1}, A, B, \Delta_{2}}{\Gamma \vdash \Delta_{1}, A \parr B, \Delta_{2}}$
* Right $\otimes$: $\frac{\Gamma_{1} \vdash \Delta_{1}, A, \Delta_{2} \qquad \Gamma_{2} \vdash \Delta_{3}, B, \Delta_{4}}{\Gamma_{1}, \Gamma_{2} \vdash \Delta_{1}, \Delta_{3}, A \otimes B, \Delta_{4}, \Delta_{2}}$
* Left $\parr$: $\frac{\Gamma_{1}, A, \Gamma_{2} \vdash \Delta_{1} \qquad \Gamma_{3}, B, \Gamma_{4} \vdash \Delta_{2}}{\Gamma_{1}, \Gamma_{3}, A \parr B, \Gamma_{4}, \Gamma_{2} \vdash \Delta_{1}, \Delta_{2}}$
* Left $1$: $\frac{\Gamma_{1}, \Gamma_{2} \vdash \Delta}{\Gamma_{1}, 1, \Gamma_{2} \vdash \Delta}$
* Right $\bot$: $\frac{\Gamma \vdash \Delta_{1},\Delta_{2}}{\Gamma \vdash \Delta_{1}, \bot, \Delta_{2}}$
* Right $1$: $\frac{}{\vdash 1}$
* Left $\bot$: $\frac{}{\bot \vdash}$
* Left negation: $\frac{\Gamma \vdash A, \Delta}{\Gamma, A^{\perp} \vdash \Delta}$
* Right negation: $\frac{\Gamma, A \vdash \Delta}{\Gamma, \vdash A^{\perp}, \Delta}$
* Left dereliction: $\frac{\Gamma_{1},A ,\Gamma_{2} \vdash \Delta}{\Gamma_{1}, !A, \Gamma_{2} \vdash \Delta}$
* Right dereliction: $\frac{\Gamma \vdash \Delta_{1},A ,\Delta_{2}}{\Gamma \vdash \Delta_{1}, ?A, \Delta_{2}}$
* Left weakening: $\frac{\Gamma_{1},\Gamma_{2} \vdash \Delta}{\Gamma_{1}, !A, \Gamma_{2} \vdash \Delta}$
* Right weakening: $\frac{\Gamma \vdash \Delta_{1}, \Delta_{2}}{\Gamma \vdash \Delta_{1}, ?A, \Delta_{2}}$
* Left contraction: $\frac{\Gamma_{1},!A ,!A, \Gamma_{2} \vdash \Delta}{\Gamma_{1}, !A, \Gamma_{2} \vdash \Delta}$
* Right contraction: $\frac{\Gamma \vdash \Delta_{1},?A , ?A, \Delta_{2}}{\Gamma \vdash \Delta_{1}, ?A, \Delta_{2}}$
* Right Promotion: $\frac{!\Gamma \vdash ?\Delta_{1}, A, ?\Delta_{2}}{!\Gamma \vdash ?\Delta_{1}, !A, ?\Delta_{2}}$
* Left promotion: $\frac{!\Gamma_{1}, A, !\Gamma_{2} \vdash \Delta}{!\Gamma_{1}, ?A, !\Gamma_{2} \vdash \Delta}$
* Right codereliction: $\frac{\Gamma \vdash \Delta_{1}, A, \Delta_{2}}{\Gamma \vdash \Delta_{1}, !A, \Delta_{2}}$
* Left codereliction: $\frac{\Gamma_{1}, A, \Gamma_{2} \vdash \Delta}{\Gamma_{1}, ?A, \Gamma_{2} \vdash \Delta}$
* Right coweakening: $\frac{}{\vdash !A}$
* Left coweakening: $\frac{}{?A \vdash}$
* Right cocontraction: $\frac{\Gamma_{1} \vdash \Delta_{1}, !A, \Delta_{2} \qquad \Gamma_{3} \vdash \Delta_{3}, !A, \Delta_{4}}{\Gamma_{1}, \Gamma_{3} \vdash \Delta_{1}, \Delta_{3}, !A, \Delta_{4}, \Delta_{2}}
$
* Left cocontraction: $\frac{\Gamma_{1}, ?A, \Gamma_{2} \vdash \Delta_{1} \qquad \Gamma_{3}, ?A, \Gamma_{4} \vdash \Delta_{2}}{\Gamma_{1}, \Gamma_{3}, ?A, \Gamma_{4}, \Gamma_{2} \vdash \Delta_{1}, \Delta_{2}}$
* Nul proof: $\frac{}{\Gamma \vdash \Delta}^{0}$
* Sum of proofs: $\frac{\Gamma \vdash \Delta \qquad \Gamma \vdash \Delta}{\Gamma \vdash \Delta}$
* Cut: $\frac{\Gamma_{1} \vdash \Delta_{1}, A, \Delta_{2} \qquad \Gamma_{2}, A, \Gamma_{3} \vdash \Delta_{3}}{\Gamma_{2}, \Gamma_{1}, \Gamma_{3} \vdash \Delta_{1}, \Delta_{3}, \Delta_{2}}$

### Inference rules - Monolateral syntax

## Isomorphisms in bilateral syntax

## Cut elimination

There is a [[rewriting system]] which, given an instance of the cut rule in a proof, reduces the proof by making the cut go higher in the proof. There are key (principal) cases which induce important commuting diagrams in the categorical semantics and there are commuting cases which are less important. The idea is that when a cut arrives at the beginning of the proof, i.e. at the level of the leaves which are axioms, we can finally eliminate it by a last rewriting step. This is, when the cut is made against an axiom rule, that we can eliminate it. We know that this rewriting system is [[strongly normalizing]] and that the [[normal forms]] are the cut-free proofs. It means that by using rewriting rules in the order you want, at the end you obtain a proof without cut, thus the name [[cut-elimination]]. It is important to know actually this rewriting system and not only that we can eliminate the cuts in a proof because this cut-elimination procedure creates the commuting diagrams of the categorical semantics, when we quotient the proofs by these cut-elimination steps.

### Cut elimination steps

### What is an isomorphism?

## Semantics

### Categorical semantics

We need a [[*-autonomous category]] in order to interpret the connectives and rules related to these connectives: $\otimes, \parr, 1, \bot, {}^{\perp}$.

This category must be enriched over commutative monoids in order to be able to interpret the sum of proofs and null proofs.

\begin{definition}
We say that a [[*-autonomous category]] $\mathcal{C}$ is enriched over commutative monoids if it is enriched over commutative monoids as a [[symmetric monoidal category]] i.e. every hom-set $\mathcal{C}[A,B]$ is a commutative monoid and $-\otimes-$ as well as $-;-$ are bilinear over morphisms i.e. preserve addition and zero in every variable.
\end{definition}

The tricky part is to interpret the exponentials $!,?$. We just need to add enough to interpret $!$, the interpretation of $?$ will follow by the $*$-autonomous structure. We need:

* A natural transformation $!A \otimes !A \rightarrow !A$ to interpret the cocontraction.
* A natural transformation $!A \rightarrow !A \otimes !A$ to interpret the contraction.
* A natural transformation $I \rightarrow !A$ to interpret the coweakening.
* A natural transformation $!A \rightarrow I$ to interpret the weakening.
* A natural transformation $A \rightarrow !A$ to interpret the codereliction.
* A natural transformation $!A \rightarrow A$ to interpret the dereliction.

Thus, for every object $A$, we will have that $!A$ is a [[bimonoid]]. $!$ will be a [[comonad]]. The codereliction is added on top of this structure.

(...)

### Concrete models

(...)

## The logic at work

### The co-Kleisli category

### Differentiating a proof

We start from a proof of $!A \vdash B$ and by using as only exponential rules cocontraction and codereliction, we obtain a proof of $!A \vdash A \multimap B$. In the co-Kleisli category we thus go from a morphism $f:A \rightarrow B$, which must be interpreted as a smooth function, to a morphism $df: A \rightarrow (A \multimap B)$. It is the differential of $f$ which associates to every point of $A$ the linear approximation of $f$ around this point.

$$
\frac{\frac{\frac{\frac{\frac{}{!A \vdash !A}^{ax} \frac{\frac{}{A \vdash A}^{ax}}{A \vdash !A}}{!A,A \vdash !A} !A \vdash B}{!A,A \vdash B}}{!A \vdash A^{\perp},B}}{!A \vdash A \multimap B}
$$

## Categorical semantics of differential linear logic and differential categories

(...)

## Additives and Seely isomorphisms

## Related concepts

* [[linear logic]]

* [[differential calculus]]

* [[differential category]]


## References

Original articles:

* {#EhrhardtRegnier09} [[Thomas Ehrhard]], [[Laurent Regnier]]: _The differential lambda-calculus_, Theor. Comput. Sci. **309** 1 (2003) 1–41  (<a href="https://doi.org/10.1016/S0304-3975(03)00392-X">doi:10.1016/S0304-3975(03)00392-X</a>)

* [[Thomas Ehrhard]], [[Laurent Regnier]]: _Differential interaction nets,_ Theor. Comput. Sci. **364** 2 (2006) 166–195 ([doi:10.1016/j.tcs.2006.08.003](https://doi.org/10.1016/j.tcs.2006.08.003))

Review:

* [[Thomas Ehrhard]], *An introduction to Differential Linear Logic: proof-nets, models and antiderivatives*, Mathematical Structure in Computer Science **28** 7 (2018) 995-1060 ([arXiv:1606.01642](https://arxiv.org/abs/1606.01642), [doi:10.1017/S0960129516000372](https://doi.org/10.1017/S0960129516000372))

Recent work on categorical semantics:

* [[R. F. Blute]], [[J. R. B. Cockett]], [[Jean-Simon Lemay]], [[R. A. G. Seely]], *Differential Categories Revisited*, Appl Categor Struct **28** (2020) 171-235 ([arXiv:1806.04804](https://arxiv.org/abs/1806.04804), [doi:10.1007/s10485-019-09572-y](https://doi.org/10.1007/s10485-019-09572-y))

Relation to [[monoidal bicategories]] and [[analytic functors]]:

* [[Marcelo Fiore]], [[Nicola Gambino]], [[Martin Hyland]], _Monoidal bicategories, differential linear logic, and analytic functors_ &lbrack;[arXiv:2405.05774](https://arxiv.org/abs/2405.05774)&rbrack;

[[!redirects Differential linear logic]]



