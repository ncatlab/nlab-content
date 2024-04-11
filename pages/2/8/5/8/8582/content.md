
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Deduction and Induction
+-- {: .hide}
[[!include deduction and induction - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Deductive systems
* table of contents
{: toc}

## Definition

In [[logic]], [[type theory]], and the [[foundations]] of [[mathematics]], a **deductive system** (or, sometimes, **inference system**) is specified by

1. A collection of [[judgments]], and
2. A collection of *steps*, each of which has a (typically finite) list of judgments as hypotheses and a single judgment as conclusion.  A step is usually written as
   $$ \frac{J_1 \quad \cdots \quad J_n}{J} $$
   If $n=0$, a step is often called an [[axiom]]. In [[set theory]], if $n \gt 0$, a step is usually called an [[axiom schema]]. 

Usually, one generates the steps by using **inference rules**, which are schematic ways of describing collections of steps, generally involving metavariables.

+-- {: .un_remark}
###### Remark
This use of the terminology "deductive system" is not completely standard, but it is not uncommon, and we need *some* name by which to refer to this general notion.
=--

+-- {: .un_example}
###### Example
In the concrete [[algebraic theory]] of [[groups]], the judgments are formal [[equations]] between [[terms]] built out of variables and the symbols $e$, $\cdot$, and $(-)^{-1}$.  Thus, for instance, $x\cdot e = x$ and $x = y \cdot x^{-1}$ are judgments.

The rules of inference express, among other things, that equality is a [[congruence]] relative to the "operations".  For instance, there is a rule
$$ \frac{a=a' \quad b=b'}{a\cdot b = a'\cdot b'} $$
where $a$, $b$, etc. are [[metavariable]]s.  [[substitution|Substituting]] particular terms for these metavariables produces a *step* which is an instance of this rule.
=--

## Proof trees and theorems

A **proof tree** in a deductive system is a rooted tree whose edges are labeled by judgments and whose nodes are labeled by steps.  We usually draw these like so:
$$
\array{\arrayopts{\rowlines{solid}}
\array{\arrayopts{\rowlines{solid}} J_1 \quad J_2 \\ J_3} \quad
\array{\arrayopts{\rowlines{solid}} J_4 \\ J_5} \\
J_6 }
$$
(To draw such trees on the nLab, see the [[HowTo]] for a hack using the `array` command.  For LaTeX papers, there is the [mathpartir](https://www.ctan.org/pkg/mathpartir) package.)

If there is a proof tree with root $J$ and no leaves (which means that every branch must terminate in an axiom), we say that $J$ is a [[theorem]] and write
$$\vdash J.$$
More generally, if there is a proof tree with root $J$ and leaves $J_1,\dots, J_n$, we write
$$ J_1, \dots, J_n \;\vdash\; J. $$
This is equivalent to saying that $J$ is a theorem in the extended deductive system obtained by adding $J_1,\dots,J_n$ as axioms.

+-- {: .un_remark}
###### Remark
This use of $\vdash$ to express a statement *about* the deductive system should be distinguished from its use in particular deductive systems as a syntactic ingredient *in judgments*.  For instance, in [[sequent calculus]] the judgments are [[sequents]], which are sequences of statements connected by a turnstile $\vdash$.  Similarly, in [[type theory]] and [[natural deduction]] one often uses $\vdash$ inside a single judgment when that judgment is of a hypothetical sort.  However, when using a [[logical framework]], these two meanings of $\vdash$ become essentially identified.
=--

## Formal systems {#FormalSystems}

Depending on the strength of the metalanguage used to define the judgments and steps, simply having a deductive system does not in itself necessarily yield an *effective procedure* for enumerating valid proof trees and theorems.  Deductive systems which do yield such an enumeration are sometimes referred to as **formal systems**.  For example, G&#246;del's [[incompleteness theorems]] are statements about formal systems in this sense.  It is worth keeping in mind that more general deductive systems are considered in proof theory and type theory, typically because by side-stepping these coding issues one can give a simpler account of computational phenomena such as [[cut-elimination]].  A well-known example of such a so-called "semi-formal system" is [[first-order arithmetic]] with the [[ω-rule]], used by Sch&#252;tte in order to simplify Gentzen's proof that the consistency of first-order arithmetic may be reduced to well-foundedness of the ordinal $\epsilon_0$.

## Examples and special cases

* [[natural deduction]]
* [[type theory]]
* [[sequent calculus]]
* [[Hilbert system]]

[[!redirects deductive system]]
[[!redirects deductive systems]]
[[!redirects deduction system]]
[[!redirects deduction systems]]
[[!redirects formal system]]
[[!redirects formal systems]]

[[!redirects inference rule]]
[[!redirects inference rules]]

[[!redirects rule of inference]]
[[!redirects rules of inference]]
