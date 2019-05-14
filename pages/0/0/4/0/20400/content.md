
## Idea

Proto CLF is a work-in-progress proof assistant design combining ideas from [[Nuprl]], [[LF]], and undecidable [[type checking]] based on subsumptive [[equality types]]. "CLF" abbreviates "Computational Logical Framework". So far, it's just unpublished metatheory development, but information may appear here.

## Syntax

### Term grammar

The main syntactic class is terms. Type expressions are terms. There are also variables and contexts.

variables ($x$, $y$, ...)` ::= `(Written as usual. Complain if you can't tell them apart from metavariables.)

terms ($t$, $a$, $b$, $f$, $T$, $A$, $B$, $R$, ...)` ::=`

* $\lambda x.b \qquad$ (lambda abstraction)
* $f\,a \qquad$ (application)

* $a = b \in C \qquad$ (equality type)
* $\Pi x:A.B \qquad$ (dependent function type)
* $\cap x:A.B \qquad$ (family intersection type)
* $Comp \qquad$ (type of computations (realizers))
* $\{x:A | B\} \qquad$ (subset/separation type)
* $\{x = y | R\} \qquad$ ([[PER]] comprehension type)
* $Bool \qquad$ (type of "booleans") (two-element type)

To be added: an infinite type.

contexts ($\Gamma$, ...)` ::= . | `$\Gamma,x:T$

As usual, the rules will make liberal use of informal list operations to work with contexts.

### Judgment forms

$a \equiv_\beta b \qquad$ (beta conversion)

The only beta reduction is $(\lambda x.b)\,a \longrightarrow_\beta b[a/x]$. Conversion is the congruence closure.

The other judgment forms will be defined inductively by the rules below. They are:

$\Gamma \vdash T\,type \qquad$ (type validity)

$\Gamma \vdash t \Vdash T \qquad$ (element in a type) (realizer of a type)

Note that in Nuprl, the ($\Gamma \vdash t \Vdash T$) form is written ($\Gamma \vdash T\;\lfloor ext t \rfloor$). The "extract" part is computed from a derivation, so the user thinks of the judgment as stating that the type is inhabited.

($\Gamma \vdash t\,:\,T$) is not used in order to avoid the misinterpretation of this judgment form as intrinsic typing of terms. Note the contrast with variables, which *are* intrinsically typed.

## Rules

$\frac{test}{render}$