
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Proto CLF is a work-in-progress [[proof assistant]] design combining ideas from [[Nuprl]], [[LF]], and [[decidability|undecidable type checking]] based on subsumptive [[equality types]]. "CLF" abbreviates "Computational Logical Framework". So far, it's just Matt Oliveri's unpublished metatheory development, but information may appear here.

## Syntax

### Term grammar

The main [[syntax|syntactic]] class is [[terms]]. [[type|Type]] expressions are terms. There are also [[variables]] and [[contexts]].

variables ($x$, $y$, ...)` ::= `(Written as usual. Complain if you can't tell them apart from metavariables.)

terms ($t$, $a$, $b$, $f$, $T$, $A$, $B$, $R$, ...)` ::=`

* $\lambda x.b \qquad$ (lambda abstraction)
* $f\,a \qquad$ (application)

* $a = b \in C \qquad$ (equality type)
* $\Pi x:A.B \qquad$ (dependent function type)
* $\bigcap x:A.B \qquad$ (family intersection type)
* $Comp \qquad$ (type of computations ([[realizers]]))
* $\{x:A | B\} \qquad$ (subset/separation type)
* $\{x = y | R\} \qquad$ ([[PER]] comprehension type)
* $Bool \qquad$ (type of "booleans") (two-element type)

To be added: an infinite type.

contexts ($\Gamma$, ...)` ::= `$\cdot$` | `$\Gamma,x:T$

As usual, the rules may make liberal use of informal list operations to work with contexts.

### Judgment forms

$a \equiv_\beta b \qquad$ (beta conversion)

The only [[beta reduction]] is $(\lambda x.b)\,a \longrightarrow_\beta b[a/x]$. Conversion is the congruence closure.

The other [[judgment]] forms will be defined [[induction|inductively]] by the rules below. They are:

$\Gamma \vdash T\,type \qquad$ (type validity)

$\Gamma \vdash t \Vdash T \qquad$ (element in a type) (realizer of a type)

Note that in [[Nuprl]], the ($\Gamma \vdash t \Vdash T$) form is written ($\Gamma \vdash T\;\lfloor ext t \rfloor$). The "extract" part is computed from a derivation, so the user thinks of the judgment as stating that the type is [[inhabited type|inhabited]].

($\Gamma \vdash t\,:\,T$) is not used in order to avoid the misinterpretation of this judgment form as [[intrinsic and extrinsic views of typing|intrinsic typing]] of terms. Note the contrast with variables, which *are* intrinsically typed.

The ($t\,:\,T$) form can be translated to this system as either ($t \Vdash T$) or ($? \Vdash t \in T$). The latter uses the abbreviation "$\in$" defined below, and the abuse of meta-notation that we don't care what goes in the "$?$". With ($t \Vdash T$), we think of $t$ as resulting from the proof of $T$. With ($? \Vdash t \in T$), we think of the "*semantic judgment*" ($t \in T$) as a goal to prove internally. The rules ensure that these two ways of expressing an element of a type are interchangeable. From this point on, ($\Gamma \vdash ? \Vdash T$) will be written as just ($\Gamma \vdash T$), although it remains informal.

### Abbreviations

#### Semantic Judgment Forms

$a \in A\;\coloneqq\;a = a \in A$

$A \to B\;\coloneqq\;\Pi \underline{\;}:A.B$

$A \wedge B\;\coloneqq\;\{\underline{\;}:A | B\}$

"$A$ equality is respected in $B$.":

$A \prec B\;\coloneqq\;\Pi t:Comp.\Pi t':Comp.
(t \in B)\to(t = t' \in A)\to(t = t' \in B)$

"$A$ members are included in $B$.":

$A \subseteq B\;\coloneqq\;\Pi t:Comp.(t \in A)\to(t \in B)$

"$A$ is a subtype of $B$.":

$A \lt\!\!:\;B\;\coloneqq\;(\lambda x.x) \in (A \to B)$

Note: ($A \lt\!\!:\;B$) ought to be logically equivalent to ($A \subseteq B \wedge A \prec B$), using the rules. And also to ($\Pi t:Comp.\Pi t':Comp.(t = t' \in A)\to(t = t' \in B)$). So semantically, thinking of types as PERs, subtypes are subrelations.

"$A$ is a refinement/subquotient of $B$.":

$A \sqsubseteq B\;\coloneqq\;A \subseteq B \wedge B \prec A$

Note the reversal of $\prec$ in $\sqsubseteq$, compared to $\lt\!\!:$. As relations on types, $\subseteq$, $\lt\!\!:$, and $\sqsubseteq$ ought to be preorders. $\prec$ is not transitive.

#### Computations

The Church booleans:

$tru\;\coloneqq\;\lambda t.\lambda f.t$

$fls\;\coloneqq\;\lambda t.\lambda f.f$

#### Type constructors

$\top\;\coloneqq\;tru = tru \in Bool$

$\bottom\;\coloneqq\;tru = fls \in Bool$

"Squash" of $A$:

$\{A\}\;\coloneqq\;\{\underline{\;}:\top | A\}$

## Rules

$\frac{test}{render}$